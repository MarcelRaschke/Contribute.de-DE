---
title: Lokales Einrichten eines Git-Repositorys
description: Dieser Artikel enthält Anweisungen zum Erstellen eines lokalen Git-Repositorys und zum Mitwirken an der Dokumentation, einschließlich des Fork- und Klonvorgangs.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 5373bf34399105c15caabe0abdc1ea0692c46a4a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609497"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="5a93a-103">Lokales Einrichten von Git für die Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5a93a-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="5a93a-104">Dieser Artikel beschreibt die Schritte zum Einrichten eines Git-Repositorys auf Ihrem lokalen Computer in der Absicht, zur Microsoft-Dokumentation beizutragen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="5a93a-105">Mitwirkende können ein lokal geklontes Repository verwenden, um neue Artikel hinzuzufügen, größere Änderungen an vorhandenen Artikel vorzunehmen oder Grafiken zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5a93a-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="5a93a-106">Sie müssen folgende Einrichtungsaktivitäten nur einmal ausführen, um mit der Mitwirkung zu beginnen:</span><span class="sxs-lookup"><span data-stu-id="5a93a-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="5a93a-107">Ermitteln des geeigneten Repositorys</span><span class="sxs-lookup"><span data-stu-id="5a93a-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="5a93a-108">Forken des Repositorys zu Ihrem GitHub-Konto</span><span class="sxs-lookup"><span data-stu-id="5a93a-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="5a93a-109">Auswählen eines lokalen Ordners für die geklonten Dateien</span><span class="sxs-lookup"><span data-stu-id="5a93a-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="5a93a-110">Klonen des Repositorys auf Ihrem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="5a93a-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="5a93a-111">Konfigurieren des Upstreamremotewerts</span><span class="sxs-lookup"><span data-stu-id="5a93a-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a93a-112">Wenn Sie nur kleine Änderungen an einem Artikel vornehmen, müssen Sie die Schritte in dieser Anleitung *nicht durchführen*.</span><span class="sxs-lookup"><span data-stu-id="5a93a-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="5a93a-113">Sie können direkt mit dem [Workflow für schnelle Änderungen](index.md#quick-edits-to-existing-documents) fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5a93a-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="5a93a-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5a93a-114">Overview</span></span>

<span data-ttu-id="5a93a-115">Um an der Dokumentationswebsite von Microsoft mitzuwirken, können Sie Markdowndateien lokal erstellen und bearbeiten, indem Sie das entsprechende Dokumentationsrepository klonen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="5a93a-116">Microsoft erfordert, dass Sie das entsprechende Repository in Ihr eigenes GitHub-Konto forken, damit Sie dort über Lese-/Schreibberechtigungen verfügen, um Ihre Änderungsvorschläge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5a93a-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="5a93a-117">Dann verwenden Sie Pullanforderungen, um die Änderungen in das schreibgeschützte gemeinsam genutzte Zentralrepository zu mergen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub-Dreieck](./media/git-and-github-initial-setup.png)

<span data-ttu-id="5a93a-119">Wenn Sie nicht mit GitHub vertraut sind, sehen Sie sich das folgende Video an, das einen Überblick über das Konzept des Verzweigungs- und Klonvorgangs vermittelt:</span><span class="sxs-lookup"><span data-stu-id="5a93a-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="5a93a-120">Ermitteln des Repositorys</span><span class="sxs-lookup"><span data-stu-id="5a93a-120">Determine the repository</span></span>

<span data-ttu-id="5a93a-121">Die Dokumentation, die auf [docs.microsoft.com](https://docs.microsoft.com) gehostet wird, befindet sich auf [github.com](https://www.github.com) in verschiedenen Repositorys.</span><span class="sxs-lookup"><span data-stu-id="5a93a-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="5a93a-122">Wenn Sie nicht sicher sind, welches Repository Sie verwenden sollen, öffnen Sie den Artikel auf [docs.microsoft.com](https://docs.microsoft.com) über Ihren Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="5a93a-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="5a93a-123">Klicken Sie auf den Link **Bearbeiten** (Bleistiftsymbol) oben rechts im Artikel.</span><span class="sxs-lookup"><span data-stu-id="5a93a-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Klicken Sie auf „Bearbeiten“, um das Repository und den Dateispeicherort zu ermitteln.](media/index/edit-article.png)

2. <span data-ttu-id="5a93a-125">Dieser Link leitet Sie zum github.com-Speicherort für die entsprechende Markdowndatei im richtigen Repository weiter.</span><span class="sxs-lookup"><span data-stu-id="5a93a-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="5a93a-126">Beachten Sie die URL, die den Namen des Repositorys angibt.</span><span class="sxs-lookup"><span data-stu-id="5a93a-126">Note the URL to view the repository name.</span></span>

   ![Beachten Sie die URL, um den Namen des Repositorys zu ermitteln.](media/public-repo.png)

   <span data-ttu-id="5a93a-128">Beispielsweise stehen die folgenden beliebten Repositorys für öffentliche Beiträge zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="5a93a-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="5a93a-129">Azure-Dokumentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="5a93a-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="5a93a-130">SQL Server-Dokumentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="5a93a-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="5a93a-131">Visual Studio-Dokumentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="5a93a-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="5a93a-132">.NET-Dokumentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="5a93a-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="5a93a-133">Dokumentation zu Azure .NET SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="5a93a-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="5a93a-134">Forken des Repositorys</span><span class="sxs-lookup"><span data-stu-id="5a93a-134">Fork the repository</span></span>
<span data-ttu-id="5a93a-135">Mit dem entsprechenden Repository können Sie mithilfe der GitHub-Website eine Verzweigung des Repositorys in Ihrem GitHub-Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="5a93a-136">Ein persönlicher Fork ist erforderlich, da alle Hauptrepositorys für die Kommunikation nur schreibgeschützten Zugriff bieten.</span><span class="sxs-lookup"><span data-stu-id="5a93a-136">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="5a93a-137">Um Änderungen vornehmen zu können, müssen Sie einen [Pull Request](git-github-fundamentals.md#pull-requests) von der Verzweigung an das Hauptrepository senden.</span><span class="sxs-lookup"><span data-stu-id="5a93a-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="5a93a-138">Zur Vereinfachung dieses Vorgangs müssen Sie zuerst eine eigene Kopie des Repositorys erstellen, in dem Sie über Schreibzugriff verfügen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="5a93a-139">Eine GitHub-*Verzweigung* wird zu diesem Zweck erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a93a-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="5a93a-140">Wechseln Sie zur GitHub-Seite des Hauptrepositorys, und klicken Sie oben rechts auf die Schaltfläche **Verzweigung**.</span><span class="sxs-lookup"><span data-stu-id="5a93a-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Beispiel eines GitHub-Profils](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="5a93a-142">Wählen Sie nach entsprechender Aufforderung die Kachel Ihres GitHub-Kontos als Ziel aus, in dem die Verzweigung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a93a-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="5a93a-143">Hierdurch wird eine Kopie des Repositorys in Ihrem GitHub-Konto erstellt, die als Verzweigung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a93a-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="5a93a-144">Auswählen eines lokalen Ordners</span><span class="sxs-lookup"><span data-stu-id="5a93a-144">Choose a local folder</span></span>
<span data-ttu-id="5a93a-145">Erstellen Sie einen lokalen Ordner, der lokal eine Kopie des Repositorys enthält.</span><span class="sxs-lookup"><span data-stu-id="5a93a-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="5a93a-146">Repositorys können bisweilen groß sein, bei „azure-docs“ z.B. bis zu 5 GB.</span><span class="sxs-lookup"><span data-stu-id="5a93a-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="5a93a-147">Wählen Sie einen Speicherort mit genügend verfügbarem Speicherplatz aus.</span><span class="sxs-lookup"><span data-stu-id="5a93a-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="5a93a-148">Wählen Sie einen Ordnernamen aus, der leicht zu merken und einzugeben ist.</span><span class="sxs-lookup"><span data-stu-id="5a93a-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="5a93a-149">Benennen Sie den Stammordner beispielsweise `C:\docs\`, oder erstellen Sie einen Ordner `~/Documents/docs/` in Ihrem Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5a93a-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5a93a-150">Wählen Sie keinen lokalen Ordnerpfad aus, der in einem anderen Speicherort eines Git-Repositoryordners geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="5a93a-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="5a93a-151">Geklonte Git-Ordner können zwar nebeneinander gespeichert, aber nicht ineinander geschachtelt werden, da dies bei der Nachverfolgung der Dateien Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="5a93a-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="5a93a-152">Starten Sie Git Bash.</span><span class="sxs-lookup"><span data-stu-id="5a93a-152">Launch Git Bash</span></span>

   ![Starten Sie Git Bash.](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="5a93a-154">Der Standardspeicherort für den Start von Git Bash ist in der Regel das Basisverzeichnis (~) bzw. `/c/users/<Windows-user-account>/` unter einem Windows-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="5a93a-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="5a93a-155">Geben Sie zum Bestimmen des aktuellen Verzeichnisses bei der $-Eingabeaufforderung `pwd` ein.</span><span class="sxs-lookup"><span data-stu-id="5a93a-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="5a93a-156">Wechseln Sie in das Verzeichnis des Ordners, den Sie zum lokalen Hosten des Repositorys erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5a93a-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="5a93a-157">Beachten Sie, dass in Git Bash die in Linux üblichen Schrägstriche anstelle von umgekehrten Schrägstrichen für Ordnerpfade verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a93a-157">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="5a93a-158">Beispiel: `cd /c/docs/ ` oder `cd ~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="5a93a-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="5a93a-159">Erstellen eines lokalen Klons</span><span class="sxs-lookup"><span data-stu-id="5a93a-159">Create a local clone</span></span>

<span data-ttu-id="5a93a-160">Mithilfe von Git Bash werden Sie auf die Ausführung des Befehls **Klonen** vorbereitet, um die Kopie eines Repositorys (d.h. die Verzweigung) auf Ihrem Gerät im aktuellen Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="5a93a-161">Authentifizieren mit Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="5a93a-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="5a93a-162">Wenn Sie die neueste Version von Git für Windows installiert und der Standardinstallation zugestimmt haben, wird standardmäßig Git Credential Manager aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a93a-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="5a93a-163">Git Credential Manager vereinfacht die Authentifizierung um ein Vielfaches, da Sie Ihr persönliches Zugriffstoken nicht erneut aufrufen müssen, wenn Sie erneut authentifizierte Verbindungen und Remoteverbindungen mit GitHub herstellen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-163">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="5a93a-164">Führen Sie den Befehl **Klonen** aus, indem Sie den Namen des Repositorys angeben.</span><span class="sxs-lookup"><span data-stu-id="5a93a-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="5a93a-165">Beim Klonen wird das verzweigte Repository auf Ihren lokalen Computer heruntergeladen (geklont).</span><span class="sxs-lookup"><span data-stu-id="5a93a-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="5a93a-166">Mit der Schaltfläche **Clone or download** (Klonen oder Herunterladen) auf der GitHub-Benutzeroberfläche können Sie die GitHub-URL Ihrer Verzweigung für den Befehl zum Klonen abrufen:</span><span class="sxs-lookup"><span data-stu-id="5a93a-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Klonen oder Herunterladen](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="5a93a-168">Geben Sie während des Klonvorgangs den Pfad zu *Ihrer Verzweigung* an, nicht das Hauptrepository, über das Sie die Verzweigung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5a93a-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="5a93a-169">Andernfalls können Sie nicht durch Änderungen mitwirken.</span><span class="sxs-lookup"><span data-stu-id="5a93a-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="5a93a-170">Über Ihr persönliches GitHub-Benutzerkonto wird auf Ihre Verzweigung verwiesen, wie etwa `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="5a93a-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="5a93a-171">Der Befehl zum Klonen sollte in etwa wie in folgendem Beispiel aussehen:</span><span class="sxs-lookup"><span data-stu-id="5a93a-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="5a93a-172">Geben Sie Ihre GitHub-Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5a93a-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub – Anmeldung](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="5a93a-174">Geben Sie Ihren Code für die zweistufige Authentifizierung ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5a93a-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub – Zweistufige Authentifizierung](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="5a93a-176">Ihre Anmeldeinformationen werden zur Authentifizierung zukünftiger GitHub-Anforderungen gespeichert und verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a93a-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="5a93a-177">Diese Authentifizierung müssen Sie nur einmal pro Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="5a93a-178">Durch den Befehl „Klonen“ wird eine Kopie der Dateien im Repository von Ihrer Verzweigung in den neuen Ordner auf dem lokalen Datenträger heruntergeladen und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a93a-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="5a93a-179">Es wird ein neuer Ordner innerhalb des aktuellen Ordners erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a93a-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="5a93a-180">Dies kann je nach Größe des Repositorys einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="5a93a-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="5a93a-181">Sobald der Vorgang abgeschlossen ist, können Sie den Ordner durchsuchen, um seine Struktur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="5a93a-182">Konfigurieren von Remoteupstream</span><span class="sxs-lookup"><span data-stu-id="5a93a-182">Configure remote upstream</span></span>
<span data-ttu-id="5a93a-183">Richten Sie nach dem Klonen des Repositorys eine Remoteverbindung mit Lesezugriff zum Hauptrepository namens **Upstream** ein.</span><span class="sxs-lookup"><span data-stu-id="5a93a-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="5a93a-184">Die Upstream-URL wird genutzt, um Ihr lokales Repository mit den letzten Änderungen anderer Benutzer zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5a93a-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="5a93a-185">Der Befehl **git remote** wird zum Festlegen der Konfigurationswerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a93a-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="5a93a-186">Verwenden Sie den Befehl **fetch**, um die Branchinformationen des Upstreamrepositorys zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5a93a-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="5a93a-187">Wenn Sie **Git Credential Manager** verwenden, nutzen Sie folgende Befehle.</span><span class="sxs-lookup"><span data-stu-id="5a93a-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="5a93a-188">Ersetzen Sie die Platzhalter \<repo\> und \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="5a93a-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="5a93a-189">Zeigen Sie die konfigurierten Werte an, und bestätigen Sie, dass die URLs korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="5a93a-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="5a93a-190">Vergewissern Sie sich, dass die **Ursprungs-URLs** auf Ihre persönliche Verzweigung verweisen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="5a93a-191">Vergewissern Sie sich zudem, dass die **Upstream**-URLs auf das Hauptrepository verweisen, wie etwa „MicrosoftDocs“ oder „Azure“.</span><span class="sxs-lookup"><span data-stu-id="5a93a-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="5a93a-192">Das folgende Beispiel zeigt eine Remoteausgabe.</span><span class="sxs-lookup"><span data-stu-id="5a93a-192">Example remote output is shown.</span></span> <span data-ttu-id="5a93a-193">Das fiktive Git-Konto „MyGitAccount“ wird mit einem persönlichen Zugriffstoken konfiguriert, um den Zugriff auf das Repository „azure-docs“ zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="5a93a-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="5a93a-194">Falls Sie einen Fehler gemacht haben, können Sie die Remotewerte entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a93a-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="5a93a-195">Führen Sie zum Entfernen des Upstreamwerts den Befehl `git remote remove upstream` aus.</span><span class="sxs-lookup"><span data-stu-id="5a93a-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5a93a-196">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="5a93a-196">Next steps</span></span>
- <span data-ttu-id="5a93a-197">Fahren Sie mit der Seite [GitHub-Beitragsworkflow](how-to-write-workflows-major.md) fort, um mehr über das Hinzufügen und Aktualisieren von Inhalt zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="5a93a-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
