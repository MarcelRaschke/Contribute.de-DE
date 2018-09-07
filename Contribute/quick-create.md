---
title: 'Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI | Microsoft-Dokumentation'
description: 'Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308822"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Schnellstartanleitung: Festlegen eines Geheimnisses und Abrufen des Geheimnisses aus Azure Key Vault mithilfe der Azure CLI

In dieser Schnellstartanleitung erfahren Sie, wie Sie ein Geheimnis in Key Vault speichern und es über eine Web-App abrufen. Um den Wert des Geheimnisses anzuzeigen, müssen Sie die folgenden Schritte in Azure ausführen. Diese Schnellstartanleitung verwendet Node.js und verwaltete Dienstidentitäten (Managed Service Identities, MSIs)

> [!div class="checklist"]
> * Erstellen Sie eine Key Vault-Instanz.
> * Speichern Sie ein Geheimnis in Key Vault.
> * Rufen Sie ein Geheimnis aus Key Vault ab.
> * Erstellen Sie eine Azure-Webanwendung.
> * [Aktivieren Sie verwaltete Dienstidentitäten](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Erteilen Sie die erforderlichen Berechtigungen zum Lesen von Daten aus Key Vault für die Webanwendung.

Bevor Sie fortfahren, stellen Sie sicher, dass Sie mit den [grundlegenden Konzepte](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts) vertraut sind.

> [!NOTE]
> Sie müssen mit ein paar Konzepten vertraut sein, um zu verstehen, warum das folgende Tutorial die empfohlene Vorgehensweise ist. Key Vault ist ein zentrales Repository zum programmgesteuerten Speichern von Geheimnissen. Dafür müssen sich Anwendungen oder Benutzer jedoch zuerst bei Key Vault authentifizieren, d.h. sie müssen ein Geheimnis angeben. Aus Sicherheitsgründen muss das erste Geheimnis außerdem regelmäßig rotiert werden. Dank der [verwalteten Dienstidentität](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) erhalten in Azure ausgeführte Anwendungen jedoch eine Identität, die automatisch von Azure verwaltet wird. Das macht die **Einführung von Geheimnissen weniger problematisch**, da Benutzer/Anwendungen die empfohlene Vorgehensweise verwenden können und sich nicht um die Rotation des ersten Geheimnisses kümmern müssen.

## <a name="prerequisites"></a>Voraussetzungen

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"
* [Visual Studio 2017 Version 15.7.3 oder höher](https://www.microsoft.com/net/download/windows) mit den folgenden Workloads:
  * ASP.NET und Webentwicklung
  * Plattformübergreifende .NET Core-Entwicklung
* [.NET Core 2.1 SDK oder höher](https://www.microsoft.com/net/download/windows) ::: zone-end
* Git ([Download](https://git-scm.com/downloads)).
* Ein Azure-Abonnement. Wenn Sie kein Azure-Abonnement besitzen, können Sie ein [kostenloses Konto](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) erstellen, bevor Sie beginnen.
* [Azure-Befehlszeilenschnittstelle](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest), Version 2.0.4 oder höher. Diese Version ist für Windows, Mac und Linux verfügbar.

## <a name="login-to-azure"></a>Anmelden bei Azure

Geben Sie Folgendes ein, um sich über die Befehlszeilenschnittstelle bei Azure anzumelden:

```azurecli
az login
```

## <a name="create-resource-group"></a>Erstellen einer Ressourcengruppe

Erstellen Sie eine Ressourcengruppe mit dem Befehl [az group create](/cli/azure/group#az-group-create). Eine Azure-Ressourcengruppe ist ein logischer Container, in dem Azure-Ressourcen bereitgestellt und verwaltet werden.

Wählen Sie einen Namen für die Ressourcengruppe aus, und fügen Sie den Platzhalter ein.
Im folgenden Beispiel wird eine Ressourcengruppe mit dem Namen *<YourResourceGroupName>* am Speicherort *eastus* erstellt.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

Die eben erstellte Ressourcengruppe wird im gesamten Tutorial verwendet.

## <a name="create-an-azure-key-vault"></a>Erstellen einer Azure Key Vault-Instanz

Als Nächstes erstellen Sie eine Key Vault-Instanz mithilfe der Ressourcengruppe, die Sie im vorherigen Schritt erstellt haben. In diesem Artikel lautet der Name für die Key Vault-Instanz zwar „ContosoKeyVault“, Sie müssen jedoch einen eindeutigen Namen verwenden. Geben Sie die folgenden Informationen ein:

* Tresorname: **Wählen Sie hier einen Key Vault-Namen aus**.
* Ressourcengruppenname: **Wählen Sie hier einen Ressourcengruppennamen aus**.
* Speicherort: Hier wird **East US** (USA, Osten) verwendet.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

An diesem Punkt ist nur Ihr Azure-Konto zum Ausführen von Vorgängen für den neuen Tresor autorisiert.

## <a name="add-a-secret-to-key-vault"></a>Hinzufügen eines Geheimnisses zu Key Vault

Wir fügen ein Geheimnis hinzu, um die Vorgehensweise zu veranschaulichen. Sie können eine SQL-Verbindungszeichenfolge oder beliebige andere Informationen speichern, die sicher aufbewahrt, aber für Ihre Anwendung verfügbar gemacht werden müssen. In diesem Tutorial heißt das Kennwort **AppSecret**, und darin wird der Wert **MySecret** gespeichert.

Geben Sie die folgenden Befehle ein, um in Key Vault ein Geheimnis namens **AppSecret** mit dem Wert **MySecret** zu erstellen:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Geben Sie Folgendes ein, um den Wert im Geheimnis als Nur-Text anzuzeigen:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Mit diesem Befehl werden die Geheimnisinformationen einschließlich des URI angezeigt. Nach der Ausführung dieser Schritte sollten Sie einen URI zu einem Geheimnis in einer Azure Key Vault-Instanz besitzen. Notieren Sie sich diese Informationen. Sie benötigen sie in einem späteren Schritt.

## <a name="clone-the-repo"></a>Klonen des Repositorys

Klonen Sie das Repository, um eine lokale Kopie zu erstellen, damit Sie die Quelle bearbeiten können. Führen Sie hierzu den folgenden Befehl aus:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Installieren von Abhängigkeiten

Im Folgenden installieren wir die Abhängigkeiten. Führen Sie die folgenden Befehle aus: cd key-vault-node-quickstart npm install

Dieses Projekt verwendet zwei Node-Module:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Veröffentlichen der Webanwendung in Azure

Im Folgenden finden Sie die Schritte, die erforderlich sind.

* Der erste Schritt besteht darin, einen [Azure App Service](https://azure.microsoft.com/services/app-service/)-Plan zu erstellen. In diesem Plan können Sie mehrere Web-Apps speichern.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Als Nächstes erstellen Sie eine Web-App. Ersetzen Sie im folgenden Beispiel <app_name> durch einen global eindeutigen App-Namen (gültige Zeichen sind a–z, 0–9 und -). Die Runtime ist auf NODE|6.9 festgelegt. Führen Sie zum Anzeigen aller unterstützten Runtimes den folgenden Befehl aus: az webapp list-runtimes.

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Nach Erstellung der Web-App zeigt die Azure CLI eine Ausgabe wie im folgenden Beispiel an:

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
    Navigieren Sie zu Ihrer neu erstellten Web-App. Ihnen sollte nun eine funktionsfähige Web-App angezeigt werden. Ersetzen Sie <app_name> durch einen eindeutigen App-Namen.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Der o.g. Befehl erstellt auch eine Git-fähige App, mit der Sie Bereitstellungen in Azure aus Ihrem lokalen Git-Repository durchführen können. 
    Das lokale Git-Repository ist mit der folgenden URL konfiguriert: https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git

* Erstellen Sie einen Bereitstellungsbenutzer. Nach Abschluss des vorherigen Befehls können Sie Ihrem lokalen Git-Repository eine Azure-Remoteinstanz hinzufügen. Ersetzen Sie <url> durch die URL des Git-Remoterepositorys, die Sie beim Aktivieren von Git für die App erhalten haben.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>Öffnen und Bearbeiten der Lösung

Bearbeiten Sie die Datei „program.cs“, um das Beispiel mit Ihrem spezifischen Schlüsseltresornamen auszuführen:

1. Navigieren Sie zum Ordner „key-vault-dotnet-core-quickstart“.
2. Öffnen Sie die Datei „key-vault-dotnet-core-quickstart.sln“ in Visual Studio 2017.
3. Öffnen Sie die Datei „Program.cs“, und aktualisieren Sie den Platzhalter *YourKeyVaultName* mit dem Namen Ihres Schlüsseltresors, den Sie weiter oben erstellt haben.

Für diese Lösung werden die NuGet-Bibliotheken [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) und [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) verwendet.

## <a name="run-the-app"></a>Ausführen der App

Wählen Sie im Hauptmenü von Visual Studio 2017 die Option **Debuggen** > **Ohne Debuggen starten**. Navigieren Sie im angezeigten Browser zur Seite **Info**. Der Wert für **AppSecret** wird angezeigt.

## <a name="publish-the-web-application-to-azure"></a>Veröffentlichen der Webanwendung in Azure

Veröffentlichen Sie diese App in Azure, um sie live als Web-App zu verwenden und zu überprüfen, ob Sie den Geheimniswert abrufen können:

1. Wählen Sie in Visual Studio das Projekt **key-vault-dotnet-core-quickstart** aus.
2. Wählen Sie **Veröffentlichen** > **Starten** aus.
3. Erstellen Sie eine neue Instanz von **App Service**, und wählen Sie dann **Veröffentlichen** aus.
4. Ändern Sie den App-Namen in **keyvaultdotnetcorequickstart**.
5. Wählen Sie **Erstellen** aus.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>Aktivieren von verwalteten Dienstidentitäten

Azure Key Vault bietet eine Möglichkeit zum sicheren Speichern von Anmeldeinformationen und anderen Schlüsseln und Geheimnissen. Um diese abrufen zu können, muss sich Ihr Code aber bei Azure Key Vault authentifizieren. Mithilfe der verwalteten Dienstidentität (Managed Service Identity, MSI) kann dieser Vorgang vereinfacht werden, indem für Azure-Dienste eine automatisch verwaltete Identität in Azure Active Directory (Azure AD) bereitgestellt wird. Sie können diese Identität für die Authentifizierung bei jedem Dienst einschließlich Key Vault verwenden, der die Azure AD-Authentifizierung unterstützt. Hierfür müssen keine Anmeldeinformationen im Code enthalten sein.

1. Kehren Sie zur Azure-Befehlszeilenschnittstelle zurück.
2. Führen Sie den Befehl „assign-identity“ aus, um die Identität für diese Anwendung zu erstellen:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>Der Befehl in diesem Verfahren entspricht dem Aufrufen des Portals und dem Festlegen von **Verwaltete Dienstidentität** auf **Ein** in den Webanwendungseigenschaften.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Zuweisen von Berechtigungen zu Ihrer Anwendung für das Lesen von Geheimnissen aus Key Vault

Notieren Sie sich die Ausgabe, wenn Sie die Anwendung in Azure veröffentlichen. Sie sollte das folgende Format haben:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Führen Sie anschließend diesen Befehl aus, indem Sie den Namen Ihres Schlüsseltresors und den Wert von **PrincipalId** verwenden:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Bereitstellen der Node-App in Azure und Abrufen des Geheimniswerts

Nachdem Sie nun alles eingerichtet haben, führen Sie den folgenden Befehl aus, um die App in Azure bereitzustellen:

```bash
git push azure master
```

Wenn Sie anschließend zu https://<app_name>.azurewebsites.net navigieren, wird Ihnen der Geheimniswert angezeigt.
Stellen Sie sicher, dass Sie den Namen <YourKeyVaultName> durch Ihren Tresornamen ersetzt haben.

::: zone-end

::: zone pivot="dotnet" Wenn Sie die Anwendung nun ausführen, sollte der Wert des Geheimnisses abgerufen werden.
::: zone-end

## <a name="next-steps"></a>Nächste Schritte

::: zone pivot="nodejs"
* [Azure Key Vault – Startseite](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault – Dokumentation](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK für Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [REST-API-Referenz für Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault – Startseite](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault – Dokumentation](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK für .NET](https://github.com/Azure/azure-sdk-for-net)
* [REST-API-Referenz für Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end
