---
title: 'Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI | Microsoft-Dokumentation'
description: 'Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239553"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="be3ed-103">Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI</span><span class="sxs-lookup"><span data-stu-id="be3ed-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="be3ed-104">In dieser Schnellstartanleitung erfahren Sie, wie Sie ein Geheimnis in Key Vault speichern und es über eine Web-App abrufen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="be3ed-105">Um den Wert des Geheimnisses anzuzeigen, müssen Sie die folgenden Schritte in Azure ausführen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="be3ed-106">Diese Schnellstartanleitung verwendet Node.js und verwaltete Dienstidentitäten (Managed Service Identities, MSIs)</span><span class="sxs-lookup"><span data-stu-id="be3ed-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="be3ed-107">Erstellen Sie eine Key Vault-Instanz.</span><span class="sxs-lookup"><span data-stu-id="be3ed-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="be3ed-108">Speichern Sie ein Geheimnis in Key Vault.</span><span class="sxs-lookup"><span data-stu-id="be3ed-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="be3ed-109">Rufen Sie ein Geheimnis aus Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="be3ed-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="be3ed-110">Erstellen Sie eine Azure-Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="be3ed-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="be3ed-111">[Aktivieren Sie verwaltete Dienstidentitäten](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="be3ed-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="be3ed-112">Erteilen Sie die erforderlichen Berechtigungen zum Lesen von Daten aus Key Vault für die Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="be3ed-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="be3ed-113">Bevor Sie fortfahren, stellen Sie sicher, dass Sie mit den [grundlegenden Konzepte](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts) vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="be3ed-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

>[!NOTE]
<span data-ttu-id="be3ed-114">Sie müssen mit ein paar Konzepten vertraut sein, um zu verstehen, warum das folgende Tutorial die empfohlene Vorgehensweise ist.</span><span class="sxs-lookup"><span data-stu-id="be3ed-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="be3ed-115">Key Vault ist ein zentrales Repository zum programmgesteuerten Speichern von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="be3ed-116">Dafür müssen sich Anwendungen oder Benutzer jedoch zuerst bei Key Vault authentifizieren, d.h. sie müssen ein Geheimnis angeben.</span><span class="sxs-lookup"><span data-stu-id="be3ed-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="be3ed-117">Aus Sicherheitsgründen muss das erste Geheimnis außerdem regelmäßig rotiert werden.</span><span class="sxs-lookup"><span data-stu-id="be3ed-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="be3ed-118">Dank der [verwalteten Dienstidentität](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) erhalten in Azure ausgeführte Anwendungen jedoch eine Identität, die automatisch von Azure verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="be3ed-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="be3ed-119">Das macht die **Einführung von Geheimnissen weniger problematisch**, da Benutzer/Anwendungen die empfohlene Vorgehensweise verwenden können und sich nicht um die Rotation des ersten Geheimnisses kümmern müssen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="be3ed-120">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="be3ed-120">Prerequisites</span></span>

<span data-ttu-id="be3ed-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="be3ed-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="be3ed-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span></span>

<span data-ttu-id="be3ed-123">::: zone pivot="dotnet, windows"</span><span class="sxs-lookup"><span data-stu-id="be3ed-123">::: zone pivot="dotnet, windows"</span></span>
* <span data-ttu-id="be3ed-124">[Visual Studio 2017 Version 15.7.3 oder höher](https://www.microsoft.com/net/download/windows) mit den folgenden Workloads:</span><span class="sxs-lookup"><span data-stu-id="be3ed-124">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="be3ed-125">ASP.NET und Webentwicklung</span><span class="sxs-lookup"><span data-stu-id="be3ed-125">ASP.NET and web development</span></span>
  * <span data-ttu-id="be3ed-126">Plattformübergreifende .NET Core-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="be3ed-126">.NET Core cross-platform development</span></span>
* <span data-ttu-id="be3ed-127">[.NET Core 2.1 SDK oder höher](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-127">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) :::zone-end</span></span>

<span data-ttu-id="be3ed-128">::: zone pivot="dotnet, mac"</span><span class="sxs-lookup"><span data-stu-id="be3ed-128">::: zone pivot="dotnet, mac"</span></span>
* <span data-ttu-id="be3ed-129">Siehe [Neues in Visual Studio für Mac](https://visualstudio.microsoft.com/vs/mac/).</span><span class="sxs-lookup"><span data-stu-id="be3ed-129">See [What’s New in Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).</span></span>
<span data-ttu-id="be3ed-130">:::zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-130">:::zone-end</span></span>

* <span data-ttu-id="be3ed-131">Git ([Download](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="be3ed-131">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="be3ed-132">Ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be3ed-132">An Azure subscription.</span></span> <span data-ttu-id="be3ed-133">Wenn Sie kein Azure-Abonnement besitzen, können Sie ein [kostenloses Konto](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) erstellen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-133">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="be3ed-134">[Azure-Befehlszeilenschnittstelle](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest), Version 2.0.4 oder höher.</span><span class="sxs-lookup"><span data-stu-id="be3ed-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="be3ed-135">Diese Version ist für Windows, Mac und Linux verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be3ed-135">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="be3ed-136">Anmelden bei Azure</span><span class="sxs-lookup"><span data-stu-id="be3ed-136">Login to Azure</span></span>

<span data-ttu-id="be3ed-137">Geben Sie Folgendes ein, um sich über die Befehlszeilenschnittstelle bei Azure anzumelden:</span><span class="sxs-lookup"><span data-stu-id="be3ed-137">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="be3ed-138">Erstellen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="be3ed-138">Create resource group</span></span>

<span data-ttu-id="be3ed-139">Erstellen Sie eine Ressourcengruppe mit dem Befehl [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="be3ed-139">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="be3ed-140">Eine Azure-Ressourcengruppe ist ein logischer Container, in dem Azure-Ressourcen bereitgestellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="be3ed-140">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="be3ed-141">Wählen Sie einen Namen für die Ressourcengruppe aus, und fügen Sie den Platzhalter ein.</span><span class="sxs-lookup"><span data-stu-id="be3ed-141">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="be3ed-142">Im folgenden Beispiel wird eine Ressourcengruppe mit dem Namen *<YourResourceGroupName>* am Speicherort *eastus* erstellt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-142">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="be3ed-143">Die eben erstellte Ressourcengruppe wird im gesamten Tutorial verwendet.</span><span class="sxs-lookup"><span data-stu-id="be3ed-143">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="be3ed-144">Erstellen einer Azure Key Vault-Instanz</span><span class="sxs-lookup"><span data-stu-id="be3ed-144">Create an Azure Key Vault</span></span>

<span data-ttu-id="be3ed-145">Als Nächstes erstellen Sie eine Key Vault-Instanz mithilfe der Ressourcengruppe, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="be3ed-145">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="be3ed-146">In diesem Artikel lautet der Name für die Key Vault-Instanz zwar „ContosoKeyVault“, Sie müssen jedoch einen eindeutigen Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="be3ed-146">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="be3ed-147">Geben Sie die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="be3ed-147">Provide the following information:</span></span>

* <span data-ttu-id="be3ed-148">Tresorname: **Wählen Sie hier einen Key Vault-Namen aus**.</span><span class="sxs-lookup"><span data-stu-id="be3ed-148">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="be3ed-149">Ressourcengruppenname: **Wählen Sie hier einen Ressourcengruppennamen aus**.</span><span class="sxs-lookup"><span data-stu-id="be3ed-149">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="be3ed-150">Speicherort: Hier wird **East US** (USA, Osten) verwendet.</span><span class="sxs-lookup"><span data-stu-id="be3ed-150">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="be3ed-151">An diesem Punkt ist nur Ihr Azure-Konto zum Ausführen von Vorgängen für den neuen Tresor autorisiert.</span><span class="sxs-lookup"><span data-stu-id="be3ed-151">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="be3ed-152">Hinzufügen eines Geheimnisses zu Key Vault</span><span class="sxs-lookup"><span data-stu-id="be3ed-152">Add a secret to key vault</span></span>

<span data-ttu-id="be3ed-153">Wir fügen ein Geheimnis hinzu, um die Vorgehensweise zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-153">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="be3ed-154">Sie können eine SQL-Verbindungszeichenfolge oder beliebige andere Informationen speichern, die sicher aufbewahrt, aber für Ihre Anwendung verfügbar gemacht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-154">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="be3ed-155">In diesem Tutorial heißt das Kennwort **AppSecret**, und darin wird der Wert **MySecret** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="be3ed-155">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="be3ed-156">Geben Sie die folgenden Befehle ein, um in Key Vault ein Geheimnis namens **AppSecret** mit dem Wert **MySecret** zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="be3ed-156">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="be3ed-157">Geben Sie Folgendes ein, um den Wert im Geheimnis als Nur-Text anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="be3ed-157">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="be3ed-158">Mit diesem Befehl werden die Geheimnisinformationen einschließlich des URI angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-158">This command shows the secret information including the URI.</span></span> <span data-ttu-id="be3ed-159">Nach der Ausführung dieser Schritte sollten Sie einen URI zu einem Geheimnis in einer Azure Key Vault-Instanz besitzen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-159">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="be3ed-160">Notieren Sie sich diese Informationen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-160">Write this information down.</span></span> <span data-ttu-id="be3ed-161">Sie benötigen sie in einem späteren Schritt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-161">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="be3ed-162">Klonen des Repositorys</span><span class="sxs-lookup"><span data-stu-id="be3ed-162">Clone the Repo</span></span>

<span data-ttu-id="be3ed-163">Klonen Sie das Repository, um eine lokale Kopie zu erstellen, damit Sie die Quelle bearbeiten können. Führen Sie hierzu den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="be3ed-163">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="be3ed-164">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="be3ed-164">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="be3ed-165">Installieren von Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="be3ed-165">Install dependencies</span></span>

<span data-ttu-id="be3ed-166">Im Folgenden installieren wir die Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="be3ed-166">Here we install the dependencies.</span></span> <span data-ttu-id="be3ed-167">Führen Sie die folgenden Befehle aus: cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="be3ed-167">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="be3ed-168">Dieses Projekt verwendet zwei Node-Module:</span><span class="sxs-lookup"><span data-stu-id="be3ed-168">This project used 2 node modules:</span></span>

* [<span data-ttu-id="be3ed-169">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="be3ed-169">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="be3ed-170">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="be3ed-170">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="be3ed-171">Veröffentlichen der Webanwendung in Azure</span><span class="sxs-lookup"><span data-stu-id="be3ed-171">Publish the web application to Azure</span></span>

<span data-ttu-id="be3ed-172">Im Folgenden finden Sie die Schritte, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="be3ed-172">Below are the few steps we need to do</span></span>

* <span data-ttu-id="be3ed-173">Der erste Schritt besteht darin, einen [Azure App Service](https://azure.microsoft.com/services/app-service/)-Plan zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-173">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="be3ed-174">In diesem Plan können Sie mehrere Web-Apps speichern.</span><span class="sxs-lookup"><span data-stu-id="be3ed-174">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="be3ed-175">Als Nächstes erstellen Sie eine Web-App.</span><span class="sxs-lookup"><span data-stu-id="be3ed-175">Next we create a web app.</span></span> <span data-ttu-id="be3ed-176">Ersetzen Sie im folgenden Beispiel <app_name> durch einen global eindeutigen App-Namen (gültige Zeichen sind a–z, 0–9 und -).</span><span class="sxs-lookup"><span data-stu-id="be3ed-176">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="be3ed-177">Die Runtime ist auf NODE|6.9 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-177">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="be3ed-178">Führen Sie zum Anzeigen aller unterstützten Runtimes den folgenden Befehl aus: az webapp list-runtimes.</span><span class="sxs-lookup"><span data-stu-id="be3ed-178">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="be3ed-179">Nach Erstellung der Web-App zeigt die Azure CLI eine Ausgabe wie im folgenden Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="be3ed-179">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    <span data-ttu-id="be3ed-180">Navigieren Sie zu Ihrer neu erstellten Web-App. Ihnen sollte nun eine funktionsfähige Web-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="be3ed-180">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="be3ed-181">Ersetzen Sie <app_name> durch einen eindeutigen App-Namen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-181">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="be3ed-182">Der o.g. Befehl erstellt auch eine Git-fähige App, mit der Sie Bereitstellungen in Azure aus Ihrem lokalen Git-Repository durchführen können.</span><span class="sxs-lookup"><span data-stu-id="be3ed-182">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="be3ed-183">Das lokale Git-Repository ist mit der folgenden URL konfiguriert: https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git</span><span class="sxs-lookup"><span data-stu-id="be3ed-183">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="be3ed-184">Erstellen Sie einen Bereitstellungsbenutzer. Nach Abschluss des vorherigen Befehls können Sie Ihrem lokalen Git-Repository eine Azure-Remoteinstanz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-184">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="be3ed-185">Ersetzen Sie <url> durch die URL des Git-Remoterepositorys, die Sie beim Aktivieren von Git für die App erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="be3ed-185">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
<span data-ttu-id="be3ed-186">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-186">::: zone-end</span></span>

<span data-ttu-id="be3ed-187">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="be3ed-187">::: zone pivot="dotnet"</span></span>

## <a name="open-and-edit-the-solution"></a><span data-ttu-id="be3ed-188">Öffnen und Bearbeiten der Lösung</span><span class="sxs-lookup"><span data-stu-id="be3ed-188">Open and edit the solution</span></span>

<span data-ttu-id="be3ed-189">Bearbeiten Sie die Datei „program.cs“, um das Beispiel mit Ihrem spezifischen Schlüsseltresornamen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="be3ed-189">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="be3ed-190">Navigieren Sie zum Ordner „key-vault-dotnet-core-quickstart“.</span><span class="sxs-lookup"><span data-stu-id="be3ed-190">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="be3ed-191">Öffnen Sie die Datei „key-vault-dotnet-core-quickstart.sln“ in Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="be3ed-191">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="be3ed-192">Öffnen Sie die Datei „Program.cs“, und aktualisieren Sie den Platzhalter *YourKeyVaultName* mit dem Namen Ihres Schlüsseltresors, den Sie weiter oben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="be3ed-192">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="be3ed-193">Für diese Lösung werden die NuGet-Bibliotheken [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) und [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) verwendet.</span><span class="sxs-lookup"><span data-stu-id="be3ed-193">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="be3ed-194">Ausführen der App</span><span class="sxs-lookup"><span data-stu-id="be3ed-194">Run the app</span></span>

<span data-ttu-id="be3ed-195">Wählen Sie im Hauptmenü von Visual Studio 2017 die Option **Debuggen** > **Ohne Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="be3ed-195">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="be3ed-196">Navigieren Sie im angezeigten Browser zur Seite **Info**.</span><span class="sxs-lookup"><span data-stu-id="be3ed-196">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="be3ed-197">Der Wert für **AppSecret** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-197">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="be3ed-198">Veröffentlichen der Webanwendung in Azure</span><span class="sxs-lookup"><span data-stu-id="be3ed-198">Publish the web application to Azure</span></span>

<span data-ttu-id="be3ed-199">Veröffentlichen Sie diese App in Azure, um sie live als Web-App zu verwenden und zu überprüfen, ob Sie den Geheimniswert abrufen können:</span><span class="sxs-lookup"><span data-stu-id="be3ed-199">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="be3ed-200">Wählen Sie in Visual Studio das Projekt **key-vault-dotnet-core-quickstart** aus.</span><span class="sxs-lookup"><span data-stu-id="be3ed-200">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="be3ed-201">Wählen Sie **Veröffentlichen** > **Starten** aus.</span><span class="sxs-lookup"><span data-stu-id="be3ed-201">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="be3ed-202">Erstellen Sie eine neue Instanz von **App Service**, und wählen Sie dann **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="be3ed-202">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="be3ed-203">Ändern Sie den App-Namen in **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="be3ed-203">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="be3ed-204">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="be3ed-204">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

<span data-ttu-id="be3ed-205">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-205">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="be3ed-206">Aktivieren von verwalteten Dienstidentitäten</span><span class="sxs-lookup"><span data-stu-id="be3ed-206">Enable managed service identities</span></span>

<span data-ttu-id="be3ed-207">Azure Key Vault bietet eine Möglichkeit zum sicheren Speichern von Anmeldeinformationen und anderen Schlüsseln und Geheimnissen. Um diese abrufen zu können, muss sich Ihr Code aber bei Azure Key Vault authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="be3ed-207">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="be3ed-208">Mithilfe der verwalteten Dienstidentität (Managed Service Identity, MSI) kann dieser Vorgang vereinfacht werden, indem für Azure-Dienste eine automatisch verwaltete Identität in Azure Active Directory (Azure AD) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="be3ed-208">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="be3ed-209">Sie können diese Identität für die Authentifizierung bei jedem Dienst einschließlich Key Vault verwenden, der die Azure AD-Authentifizierung unterstützt. Hierfür müssen keine Anmeldeinformationen im Code enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="be3ed-209">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="be3ed-210">Kehren Sie zur Azure-Befehlszeilenschnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="be3ed-210">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="be3ed-211">Führen Sie den Befehl „assign-identity“ aus, um die Identität für diese Anwendung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="be3ed-211">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="be3ed-212">Der Befehl in diesem Verfahren entspricht dem Aufrufen des Portals und dem Festlegen von **Verwaltete Dienstidentität** auf **Ein** in den Webanwendungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be3ed-212">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="be3ed-213">Zuweisen von Berechtigungen zu Ihrer Anwendung für das Lesen von Geheimnissen aus Key Vault</span><span class="sxs-lookup"><span data-stu-id="be3ed-213">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="be3ed-214">Notieren Sie sich die Ausgabe, wenn Sie die Anwendung in Azure veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="be3ed-214">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="be3ed-215">Sie sollte das folgende Format haben:</span><span class="sxs-lookup"><span data-stu-id="be3ed-215">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="be3ed-216">Führen Sie anschließend diesen Befehl aus, indem Sie den Namen Ihres Schlüsseltresors und den Wert von **PrincipalId** verwenden:</span><span class="sxs-lookup"><span data-stu-id="be3ed-216">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="be3ed-217">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="be3ed-217">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="be3ed-218">Bereitstellen der Node-App in Azure und Abrufen des Geheimniswerts</span><span class="sxs-lookup"><span data-stu-id="be3ed-218">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="be3ed-219">Nachdem Sie nun alles eingerichtet haben,</span><span class="sxs-lookup"><span data-stu-id="be3ed-219">Now that everything is set.</span></span> <span data-ttu-id="be3ed-220">führen Sie den folgenden Befehl aus, um die App in Azure bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="be3ed-220">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="be3ed-221">Wenn Sie anschließend zu https://<app_name>.azurewebsites.net navigieren, wird Ihnen der Geheimniswert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be3ed-221">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="be3ed-222">Stellen Sie sicher, dass Sie den Namen <YourKeyVaultName> durch Ihren Tresornamen ersetzt haben. ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-222">Make sure that you replaced the name <YourKeyVaultName> with your vault name ::: zone-end</span></span>

<span data-ttu-id="be3ed-223">::: zone pivot="dotnet" Wenn Sie die Anwendung nun ausführen, sollte der Wert des Geheimnisses abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="be3ed-223">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="be3ed-224">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-224">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="be3ed-225">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="be3ed-225">Next steps</span></span>

<span data-ttu-id="be3ed-226">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="be3ed-226">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="be3ed-227">Azure Key Vault – Startseite</span><span class="sxs-lookup"><span data-stu-id="be3ed-227">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="be3ed-228">Azure Key Vault – Dokumentation</span><span class="sxs-lookup"><span data-stu-id="be3ed-228">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="be3ed-229">Azure SDK für Node</span><span class="sxs-lookup"><span data-stu-id="be3ed-229">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="be3ed-230">[REST-API-Referenz für Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-230">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="be3ed-231">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="be3ed-231">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="be3ed-232">Azure Key Vault – Startseite</span><span class="sxs-lookup"><span data-stu-id="be3ed-232">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="be3ed-233">Azure Key Vault – Dokumentation</span><span class="sxs-lookup"><span data-stu-id="be3ed-233">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="be3ed-234">Azure SDK für .NET</span><span class="sxs-lookup"><span data-stu-id="be3ed-234">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="be3ed-235">[REST-API-Referenz für Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="be3ed-235">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>