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
# <a name="set-up-git-repository-locally-for-documentation"></a>Lokales Einrichten von Git für die Dokumentation

Dieser Artikel beschreibt die Schritte zum Einrichten eines Git-Repositorys auf Ihrem lokalen Computer in der Absicht, zur Microsoft-Dokumentation beizutragen. Mitwirkende können ein lokal geklontes Repository verwenden, um neue Artikel hinzuzufügen, größere Änderungen an vorhandenen Artikel vorzunehmen oder Grafiken zu ändern.

Sie müssen die folgenden Einrichtungsaktivitäten einmalig ausführen, um mit der Mitwirkung zu beginnen:
> [!div class="checklist"]
> * Ermitteln des geeigneten Repositorys
> * Forken des Repositorys zu Ihrem GitHub-Konto
> * Auswählen eines lokalen Ordners für die geklonten Dateien
> * Klonen des Repositorys auf Ihrem lokalen Computer
> * Konfigurieren des Upstreamremotewerts

> [!IMPORTANT]
> Wenn Sie nur kleine Änderungen an einem Artikel vornehmen, müssen Sie die Schritte in dieser Anleitung *nicht durchführen*. Sie können direkt mit dem [Workflow für schnelle Änderungen](index.md#quick-edits-to-existing-documents) fortfahren.
>

## <a name="overview"></a>Übersicht

Um an der Dokumentationswebsite von Microsoft mitzuwirken, können Sie Markdowndateien lokal erstellen und bearbeiten, indem Sie das entsprechende Dokumentationsrepository klonen. Microsoft erfordert, dass Sie das entsprechende Repository in Ihr eigenes GitHub-Konto forken, damit Sie dort über Lese-/Schreibberechtigungen verfügen, um Ihre Änderungsvorschläge zu speichern. Dann verwenden Sie Pullanforderungen, um die Änderungen in das schreibgeschützte gemeinsam genutzte Zentralrepository zu mergen.

![GitHub-Dreieck](./media/git-and-github-initial-setup.png)

Wenn Sie nicht mit GitHub vertraut sind, sehen Sie sich das folgende Video an, das einen Überblick über das Konzept des Verzweigungs- und Klonvorgangs vermittelt:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>Ermitteln des Repositorys

Die Dokumentation, die auf [docs.microsoft.com](https://docs.microsoft.com) gehostet wird, befindet sich auf [github.com](https://www.github.com) in verschiedenen Repositorys.

1. Wenn Sie nicht sicher sind, welches Repository Sie verwenden sollen, öffnen Sie den Artikel auf [docs.microsoft.com](https://docs.microsoft.com) über Ihren Webbrowser. Klicken Sie auf den Link **Bearbeiten** (Bleistiftsymbol) oben rechts im Artikel.

   ![Klicken Sie auf „Bearbeiten“, um das Repository und den Dateispeicherort zu ermitteln.](media/index/edit-article.png)

2. Dieser Link leitet Sie zum github.com-Speicherort für die entsprechende Markdowndatei im richtigen Repository weiter. Beachten Sie die URL, die den Namen des Repositorys angibt.

   ![Beachten Sie die URL, um den Namen des Repositorys zu ermitteln.](media/public-repo.png)

   Beispielsweise stehen die folgenden beliebten Repositorys für öffentliche Beiträge zur Verfügung:
   - Azure-Dokumentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - SQL Server-Dokumentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Visual Studio-Dokumentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - .NET-Dokumentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Dokumentation zu Azure .NET SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   - ConfigMgr-Dokumentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)

## <a name="fork-the-repository"></a>Forken des Repositorys
Mit dem entsprechenden Repository können Sie mithilfe der GitHub-Website eine Verzweigung des Repositorys in Ihrem GitHub-Konto erstellen.

Ein persönlicher Fork ist erforderlich, da alle Hauptrepositorys für die Kommunikation nur schreibgeschützten Zugriff bieten. Um Änderungen vornehmen zu können, müssen Sie einen [Pull Request](git-github-fundamentals.md#pull-requests) von der Verzweigung an das Hauptrepository senden. Zur Vereinfachung dieses Vorgangs müssen Sie zuerst eine eigene Kopie des Repositorys erstellen, in dem Sie über Schreibzugriff verfügen. Eine GitHub-*Verzweigung* wird zu diesem Zweck erstellt.

1. Wechseln Sie zur GitHub-Seite des Hauptrepositorys, und klicken Sie oben rechts auf die Schaltfläche **Verzweigung**.

   ![Beispiel eines GitHub-Profils](./media/contribute-get-started-setup-local/fork.png)

2. Wählen Sie nach entsprechender Aufforderung die Kachel Ihres GitHub-Kontos als Ziel aus, in dem die Verzweigung erstellt werden soll. Hierdurch wird eine Kopie des Repositorys in Ihrem GitHub-Konto erstellt, die als Verzweigung bezeichnet wird.

## <a name="choose-a-local-folder"></a>Auswählen eines lokalen Ordners
Erstellen Sie einen lokalen Ordner, der lokal eine Kopie des Repositorys enthält. Repositorys können bisweilen groß sein, bei „azure-docs“ z.B. bis zu 5 GB. Wählen Sie einen Speicherort mit genügend verfügbarem Speicherplatz aus.

1. Wählen Sie einen Ordnernamen aus, der leicht zu merken und einzugeben ist. Benennen Sie den Stammordner beispielsweise `C:\docs\`, oder erstellen Sie einen Ordner `~/Documents/docs/` in Ihrem Benutzerprofilverzeichnis.

   > [!IMPORTANT]
   > Wählen Sie keinen lokalen Ordnerpfad aus, der in einem anderen Speicherort eines Git-Repositoryordners geschachtelt ist. Geklonte Git-Ordner können zwar nebeneinander gespeichert, aber nicht ineinander geschachtelt werden, da dies bei der Nachverfolgung der Dateien Fehler verursacht.

2. Starten Sie Git Bash.

   ![Starten Sie Git Bash.](./media/contribute-get-started-setup-local/gitbash-start.png)

   Der Standardspeicherort für den Start von Git Bash ist in der Regel das Basisverzeichnis (~) bzw. `/c/users/<Windows-user-account>/` unter einem Windows-Betriebssystem.

   Geben Sie zum Bestimmen des aktuellen Verzeichnisses bei der $-Eingabeaufforderung `pwd` ein. 

3. Wechseln Sie in das Verzeichnis des Ordners, den Sie zum lokalen Hosten des Repositorys erstellt haben. Beachten Sie, dass in Git Bash die in Linux üblichen Schrägstriche anstelle von umgekehrten Schrägstrichen für Ordnerpfade verwendet werden.

   Beispiel: `cd /c/docs/ ` oder `cd ~/Documents/docs/`.

## <a name="create-a-local-clone"></a>Erstellen eines lokalen Klons

Mithilfe von Git Bash werden Sie auf die Ausführung des Befehls **Klonen** vorbereitet, um die Kopie eines Repositorys (d.h. die Verzweigung) auf Ihrem Gerät im aktuellen Verzeichnis zu erstellen. 

### <a name="authenticate-by-using-git-credential-manager"></a>Authentifizieren mit Git Credential Manager
Wenn Sie die neueste Version von Git für Windows installiert und der Standardinstallation zugestimmt haben, wird standardmäßig Git Credential Manager aktiviert. Git Credential Manager vereinfacht die Authentifizierung um ein Vielfaches, da Sie Ihr persönliches Zugriffstoken nicht erneut aufrufen müssen, wenn Sie erneut authentifizierte Verbindungen und Remoteverbindungen mit GitHub herstellen.

1. Führen Sie den Befehl **Klonen** aus, indem Sie den Namen des Repositorys angeben. Beim Klonen wird das verzweigte Repository auf Ihren lokalen Computer heruntergeladen (geklont). 

    > [!Tip]
    > Mit der Schaltfläche **Clone or download** (Klonen oder Herunterladen) auf der GitHub-Benutzeroberfläche können Sie die GitHub-URL Ihrer Verzweigung für den Befehl zum Klonen abrufen:
    >
    > ![Klonen oder Herunterladen](./media/contribute-get-started-setup-local/clone-or-download.png)

    Geben Sie während des Klonvorgangs den Pfad zu *Ihrer Verzweigung* an, nicht das Hauptrepository, über das Sie die Verzweigung erstellt haben. Andernfalls können Sie nicht durch Änderungen mitwirken. Über Ihr persönliches GitHub-Benutzerkonto wird auf Ihre Verzweigung verwiesen, wie etwa `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Der Befehl zum Klonen sollte in etwa wie in folgendem Beispiel aussehen:

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. Geben Sie Ihre GitHub-Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.

    ![GitHub – Anmeldung](./media/contribute-get-started-setup-local/github-login.png)

3. Geben Sie Ihren Code für die zweistufige Authentifizierung ein, wenn Sie dazu aufgefordert werden.

    ![GitHub – Zweistufige Authentifizierung](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Ihre Anmeldeinformationen werden zur Authentifizierung zukünftiger GitHub-Anforderungen gespeichert und verwendet. Diese Authentifizierung müssen Sie nur einmal pro Computer durchführen. 

4. Durch den Befehl „Klonen“ wird eine Kopie der Dateien im Repository von Ihrer Verzweigung in den neuen Ordner auf dem lokalen Datenträger heruntergeladen und ausgeführt. Es wird ein neuer Ordner innerhalb des aktuellen Ordners erstellt. Dies kann je nach Größe des Repositorys einige Minuten dauern. Sobald der Vorgang abgeschlossen ist, können Sie den Ordner durchsuchen, um seine Struktur anzuzeigen.

## <a name="configure-remote-upstream"></a>Konfigurieren von Remoteupstream
Richten Sie nach dem Klonen des Repositorys eine Remoteverbindung mit Lesezugriff zum Hauptrepository namens **Upstream** ein. Die Upstream-URL wird genutzt, um Ihr lokales Repository mit den letzten Änderungen anderer Benutzer zu synchronisieren. Der Befehl **git remote** wird zum Festlegen der Konfigurationswerte verwendet. Verwenden Sie den Befehl **fetch**, um die Branchinformationen des Upstreamrepositorys zu aktualisieren.

1. Wenn Sie **Git Credential Manager** verwenden, nutzen Sie folgende Befehle. Ersetzen Sie die Platzhalter \<repo\> und \<organization\>.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Zeigen Sie die konfigurierten Werte an, und bestätigen Sie, dass die URLs korrekt sind. Vergewissern Sie sich, dass die **Ursprungs-URLs** auf Ihre persönliche Verzweigung verweisen. Vergewissern Sie sich zudem, dass die **Upstream**-URLs auf das Hauptrepository verweisen, wie etwa „MicrosoftDocs“ oder „Azure“. 
   ```bash
   git remote -v 
   ```

   Das folgende Beispiel zeigt eine Remoteausgabe. Das fiktive Git-Konto „MyGitAccount“ wird mit einem persönlichen Zugriffstoken konfiguriert, um den Zugriff auf das Repository „azure-docs“ zu ermöglichen:
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Falls Sie einen Fehler gemacht haben, können Sie die Remotewerte entfernen. Führen Sie zum Entfernen des Upstreamwerts den Befehl `git remote remove upstream` aus.

## <a name="next-steps"></a>Nächste Schritte
- Fahren Sie mit der Seite [GitHub-Beitragsworkflow](how-to-write-workflows-major.md) fort, um mehr über das Hinzufügen und Aktualisieren von Inhalt zu erfahren.
