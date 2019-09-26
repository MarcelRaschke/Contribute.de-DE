---
title: Lokales Einrichten eines Git-Repositorys
description: Dieser Artikel enthält Anweisungen zum Erstellen eines lokalen Git-Repositorys und zum Mitwirken an der Dokumentation, einschließlich des Fork- und Klonvorgangs.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 285c25fe0e5df067ceeaa5a42da1bad5533d2c84
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247402"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="9fda3-103">Lokales Einrichten von Git für die Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9fda3-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="9fda3-104">Dieser Artikel beschreibt die Schritte zum Einrichten eines Git-Repositorys auf Ihrem lokalen Computer in der Absicht, zur Microsoft-Dokumentation beizutragen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="9fda3-105">Mitwirkende können ein lokal geklontes Repository verwenden, um neue Artikel hinzuzufügen, größere Änderungen an vorhandenen Artikel vorzunehmen oder Grafiken zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9fda3-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="9fda3-106">Sie müssen die folgenden Einrichtungsaktivitäten einmalig ausführen, um mit der Mitwirkung zu beginnen:</span><span class="sxs-lookup"><span data-stu-id="9fda3-106">You run these one-time setup activities to start contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="9fda3-107">Ermitteln des geeigneten Repositorys</span><span class="sxs-lookup"><span data-stu-id="9fda3-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="9fda3-108">Forken des Repositorys zu Ihrem GitHub-Konto</span><span class="sxs-lookup"><span data-stu-id="9fda3-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="9fda3-109">Auswählen eines lokalen Ordners für die geklonten Dateien</span><span class="sxs-lookup"><span data-stu-id="9fda3-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="9fda3-110">Klonen des Repositorys auf Ihrem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="9fda3-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="9fda3-111">Konfigurieren des Upstreamremotewerts</span><span class="sxs-lookup"><span data-stu-id="9fda3-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fda3-112">Wenn Sie nur kleine Änderungen an einem Artikel vornehmen, müssen Sie die Schritte in dieser Anleitung *nicht durchführen*.</span><span class="sxs-lookup"><span data-stu-id="9fda3-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="9fda3-113">Sie können direkt mit dem [Workflow für schnelle Änderungen](index.md#quick-edits-to-existing-documents) fortfahren.</span><span class="sxs-lookup"><span data-stu-id="9fda3-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="9fda3-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9fda3-114">Overview</span></span>

<span data-ttu-id="9fda3-115">Um an der Dokumentationswebsite von Microsoft mitzuwirken, können Sie Markdowndateien lokal erstellen und bearbeiten, indem Sie das entsprechende Dokumentationsrepository klonen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="9fda3-116">Microsoft erfordert, dass Sie das entsprechende Repository in Ihr eigenes GitHub-Konto forken, damit Sie dort über Lese-/Schreibberechtigungen verfügen, um Ihre Änderungsvorschläge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9fda3-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="9fda3-117">Dann verwenden Sie Pullanforderungen, um die Änderungen in das schreibgeschützte gemeinsam genutzte Zentralrepository zu mergen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub-Dreieck](./media/git-and-github-initial-setup.png)

<span data-ttu-id="9fda3-119">Wenn Sie nicht mit GitHub vertraut sind, sehen Sie sich das folgende Video an, das einen Überblick über das Konzept des Verzweigungs- und Klonvorgangs vermittelt:</span><span class="sxs-lookup"><span data-stu-id="9fda3-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="9fda3-120">Ermitteln des Repositorys</span><span class="sxs-lookup"><span data-stu-id="9fda3-120">Determine the repository</span></span>

<span data-ttu-id="9fda3-121">Die Dokumentation, die auf [docs.microsoft.com](https://docs.microsoft.com) gehostet wird, befindet sich auf [github.com](https://www.github.com) in verschiedenen Repositorys.</span><span class="sxs-lookup"><span data-stu-id="9fda3-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="9fda3-122">Wenn Sie nicht sicher sind, welches Repository Sie verwenden sollen, öffnen Sie den Artikel auf [docs.microsoft.com](https://docs.microsoft.com) über Ihren Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="9fda3-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="9fda3-123">Klicken Sie auf den Link **Bearbeiten** (Bleistiftsymbol) oben rechts im Artikel.</span><span class="sxs-lookup"><span data-stu-id="9fda3-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Klicken Sie auf „Bearbeiten“, um das Repository und den Dateispeicherort zu ermitteln.](media/index/edit-article.png)

2. <span data-ttu-id="9fda3-125">Dieser Link leitet Sie zum github.com-Speicherort für die entsprechende Markdowndatei im richtigen Repository weiter.</span><span class="sxs-lookup"><span data-stu-id="9fda3-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="9fda3-126">Beachten Sie die URL, die den Namen des Repositorys angibt.</span><span class="sxs-lookup"><span data-stu-id="9fda3-126">Note the URL to view the repository name.</span></span>

   ![Beachten Sie die URL, um den Namen des Repositorys zu ermitteln.](media/public-repo.png)

   <span data-ttu-id="9fda3-128">Beispielsweise stehen die folgenden beliebten Repositorys für öffentliche Beiträge zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9fda3-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="9fda3-129">Azure-Dokumentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="9fda3-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="9fda3-130">SQL Server-Dokumentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="9fda3-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="9fda3-131">Visual Studio-Dokumentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="9fda3-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="9fda3-132">.NET-Dokumentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="9fda3-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="9fda3-133">Dokumentation zu Azure .NET SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="9fda3-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>
   - <span data-ttu-id="9fda3-134">ConfigMgr-Dokumentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span><span class="sxs-lookup"><span data-stu-id="9fda3-134">ConfigMgr documentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="9fda3-135">Forken des Repositorys</span><span class="sxs-lookup"><span data-stu-id="9fda3-135">Fork the repository</span></span>
<span data-ttu-id="9fda3-136">Mit dem entsprechenden Repository können Sie mithilfe der GitHub-Website eine Verzweigung des Repositorys in Ihrem GitHub-Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-136">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="9fda3-137">Ein persönlicher Fork ist erforderlich, da alle Hauptrepositorys für die Kommunikation nur schreibgeschützten Zugriff bieten.</span><span class="sxs-lookup"><span data-stu-id="9fda3-137">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="9fda3-138">Um Änderungen vornehmen zu können, müssen Sie einen [Pull Request](git-github-fundamentals.md#pull-requests) von der Verzweigung an das Hauptrepository senden.</span><span class="sxs-lookup"><span data-stu-id="9fda3-138">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="9fda3-139">Zur Vereinfachung dieses Vorgangs müssen Sie zuerst eine eigene Kopie des Repositorys erstellen, in dem Sie über Schreibzugriff verfügen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-139">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="9fda3-140">Eine GitHub-*Verzweigung* wird zu diesem Zweck erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fda3-140">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="9fda3-141">Wechseln Sie zur GitHub-Seite des Hauptrepositorys, und klicken Sie oben rechts auf die Schaltfläche **Verzweigung**.</span><span class="sxs-lookup"><span data-stu-id="9fda3-141">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Beispiel eines GitHub-Profils](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="9fda3-143">Wählen Sie nach entsprechender Aufforderung die Kachel Ihres GitHub-Kontos als Ziel aus, in dem die Verzweigung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fda3-143">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="9fda3-144">Hierdurch wird eine Kopie des Repositorys in Ihrem GitHub-Konto erstellt, die als Verzweigung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9fda3-144">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="9fda3-145">Auswählen eines lokalen Ordners</span><span class="sxs-lookup"><span data-stu-id="9fda3-145">Choose a local folder</span></span>
<span data-ttu-id="9fda3-146">Erstellen Sie einen lokalen Ordner, der lokal eine Kopie des Repositorys enthält.</span><span class="sxs-lookup"><span data-stu-id="9fda3-146">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="9fda3-147">Repositorys können bisweilen groß sein, bei „azure-docs“ z.B. bis zu 5 GB.</span><span class="sxs-lookup"><span data-stu-id="9fda3-147">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="9fda3-148">Wählen Sie einen Speicherort mit genügend verfügbarem Speicherplatz aus.</span><span class="sxs-lookup"><span data-stu-id="9fda3-148">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="9fda3-149">Wählen Sie einen Ordnernamen aus, der leicht zu merken und einzugeben ist.</span><span class="sxs-lookup"><span data-stu-id="9fda3-149">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="9fda3-150">Benennen Sie den Stammordner beispielsweise `C:\docs\`, oder erstellen Sie einen Ordner `~/Documents/docs/` in Ihrem Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9fda3-150">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="9fda3-151">Wählen Sie keinen lokalen Ordnerpfad aus, der in einem anderen Speicherort eines Git-Repositoryordners geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="9fda3-151">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="9fda3-152">Geklonte Git-Ordner können zwar nebeneinander gespeichert, aber nicht ineinander geschachtelt werden, da dies bei der Nachverfolgung der Dateien Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="9fda3-152">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="9fda3-153">Starten Sie Git Bash.</span><span class="sxs-lookup"><span data-stu-id="9fda3-153">Launch Git Bash</span></span>

   ![Starten Sie Git Bash.](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="9fda3-155">Der Standardspeicherort für den Start von Git Bash ist in der Regel das Basisverzeichnis (~) bzw. `/c/users/<Windows-user-account>/` unter einem Windows-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="9fda3-155">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="9fda3-156">Geben Sie zum Bestimmen des aktuellen Verzeichnisses bei der $-Eingabeaufforderung `pwd` ein.</span><span class="sxs-lookup"><span data-stu-id="9fda3-156">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="9fda3-157">Wechseln Sie in das Verzeichnis des Ordners, den Sie zum lokalen Hosten des Repositorys erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9fda3-157">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="9fda3-158">Beachten Sie, dass in Git Bash die in Linux üblichen Schrägstriche anstelle von umgekehrten Schrägstrichen für Ordnerpfade verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fda3-158">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="9fda3-159">Beispiel: `cd /c/docs/ ` oder `cd ~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="9fda3-159">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="9fda3-160">Erstellen eines lokalen Klons</span><span class="sxs-lookup"><span data-stu-id="9fda3-160">Create a local clone</span></span>

<span data-ttu-id="9fda3-161">Mithilfe von Git Bash werden Sie auf die Ausführung des Befehls **Klonen** vorbereitet, um die Kopie eines Repositorys (d.h. die Verzweigung) auf Ihrem Gerät im aktuellen Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-161">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="9fda3-162">Authentifizieren mit Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="9fda3-162">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="9fda3-163">Wenn Sie die neueste Version von Git für Windows installiert und der Standardinstallation zugestimmt haben, wird standardmäßig Git Credential Manager aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9fda3-163">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="9fda3-164">Git Credential Manager vereinfacht die Authentifizierung um ein Vielfaches, da Sie Ihr persönliches Zugriffstoken nicht erneut aufrufen müssen, wenn Sie erneut authentifizierte Verbindungen und Remoteverbindungen mit GitHub herstellen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-164">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="9fda3-165">Führen Sie den Befehl **Klonen** aus, indem Sie den Namen des Repositorys angeben.</span><span class="sxs-lookup"><span data-stu-id="9fda3-165">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="9fda3-166">Beim Klonen wird das verzweigte Repository auf Ihren lokalen Computer heruntergeladen (geklont).</span><span class="sxs-lookup"><span data-stu-id="9fda3-166">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="9fda3-167">Mit der Schaltfläche **Clone or download** (Klonen oder Herunterladen) auf der GitHub-Benutzeroberfläche können Sie die GitHub-URL Ihrer Verzweigung für den Befehl zum Klonen abrufen:</span><span class="sxs-lookup"><span data-stu-id="9fda3-167">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Klonen oder Herunterladen](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="9fda3-169">Geben Sie während des Klonvorgangs den Pfad zu *Ihrer Verzweigung* an, nicht das Hauptrepository, über das Sie die Verzweigung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9fda3-169">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="9fda3-170">Andernfalls können Sie nicht durch Änderungen mitwirken.</span><span class="sxs-lookup"><span data-stu-id="9fda3-170">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="9fda3-171">Über Ihr persönliches GitHub-Benutzerkonto wird auf Ihre Verzweigung verwiesen, wie etwa `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="9fda3-171">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="9fda3-172">Der Befehl zum Klonen sollte in etwa wie in folgendem Beispiel aussehen:</span><span class="sxs-lookup"><span data-stu-id="9fda3-172">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="9fda3-173">Geben Sie Ihre GitHub-Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9fda3-173">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub – Anmeldung](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="9fda3-175">Geben Sie Ihren Code für die zweistufige Authentifizierung ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9fda3-175">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub – Zweistufige Authentifizierung](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="9fda3-177">Ihre Anmeldeinformationen werden zur Authentifizierung zukünftiger GitHub-Anforderungen gespeichert und verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fda3-177">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="9fda3-178">Diese Authentifizierung müssen Sie nur einmal pro Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-178">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="9fda3-179">Durch den Befehl „Klonen“ wird eine Kopie der Dateien im Repository von Ihrer Verzweigung in den neuen Ordner auf dem lokalen Datenträger heruntergeladen und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fda3-179">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="9fda3-180">Es wird ein neuer Ordner innerhalb des aktuellen Ordners erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fda3-180">A new folder is made within the current folder.</span></span> <span data-ttu-id="9fda3-181">Dies kann je nach Größe des Repositorys einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="9fda3-181">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="9fda3-182">Sobald der Vorgang abgeschlossen ist, können Sie den Ordner durchsuchen, um seine Struktur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-182">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="9fda3-183">Konfigurieren von Remoteupstream</span><span class="sxs-lookup"><span data-stu-id="9fda3-183">Configure remote upstream</span></span>
<span data-ttu-id="9fda3-184">Richten Sie nach dem Klonen des Repositorys eine Remoteverbindung mit Lesezugriff zum Hauptrepository namens **Upstream** ein.</span><span class="sxs-lookup"><span data-stu-id="9fda3-184">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="9fda3-185">Die Upstream-URL wird genutzt, um Ihr lokales Repository mit den letzten Änderungen anderer Benutzer zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9fda3-185">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="9fda3-186">Der Befehl **git remote** wird zum Festlegen der Konfigurationswerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fda3-186">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="9fda3-187">Verwenden Sie den Befehl **fetch**, um die Branchinformationen des Upstreamrepositorys zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9fda3-187">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="9fda3-188">Wenn Sie **Git Credential Manager** verwenden, nutzen Sie folgende Befehle.</span><span class="sxs-lookup"><span data-stu-id="9fda3-188">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="9fda3-189">Ersetzen Sie die Platzhalter \<repo\> und \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="9fda3-189">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="9fda3-190">Zeigen Sie die konfigurierten Werte an, und bestätigen Sie, dass die URLs korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="9fda3-190">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="9fda3-191">Vergewissern Sie sich, dass die **Ursprungs-URLs** auf Ihre persönliche Verzweigung verweisen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-191">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="9fda3-192">Vergewissern Sie sich zudem, dass die **Upstream**-URLs auf das Hauptrepository verweisen, wie etwa „MicrosoftDocs“ oder „Azure“.</span><span class="sxs-lookup"><span data-stu-id="9fda3-192">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="9fda3-193">Das folgende Beispiel zeigt eine Remoteausgabe.</span><span class="sxs-lookup"><span data-stu-id="9fda3-193">Example remote output is shown.</span></span> <span data-ttu-id="9fda3-194">Das fiktive Git-Konto „MyGitAccount“ wird mit einem persönlichen Zugriffstoken konfiguriert, um den Zugriff auf das Repository „azure-docs“ zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="9fda3-194">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="9fda3-195">Falls Sie einen Fehler gemacht haben, können Sie die Remotewerte entfernen.</span><span class="sxs-lookup"><span data-stu-id="9fda3-195">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="9fda3-196">Führen Sie zum Entfernen des Upstreamwerts den Befehl `git remote remove upstream` aus.</span><span class="sxs-lookup"><span data-stu-id="9fda3-196">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9fda3-197">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9fda3-197">Next steps</span></span>
- <span data-ttu-id="9fda3-198">Fahren Sie mit der Seite [GitHub-Beitragsworkflow](how-to-write-workflows-major.md) fort, um mehr über das Hinzufügen und Aktualisieren von Inhalt zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="9fda3-198">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
