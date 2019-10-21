---
title: Mitwirken an Repositorys der PowerShell-Dokumentation
description: In diesem Artikel erhalten Sie eine Einführung, in der Sie erfahren, wie Sie an den Repositorys der PowerShell-Dokumentation mitwirken können. Sie lernen die verwendeten Repositorys, die Vorgehensweise für das Ordnen von Inhalten und die Richtlinien für das Verwalten von Codebeispielen und anderen Ressourcen kennen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290194"
---
# <a name="process-for-contributing-to-powershell-docs"></a>Mitwirken an der PowerShell-Dokumentation

Wir schätzen Beiträge zur Dokumentation, die aus der Community kommen. Im Folgenden sind einige Leitlinien aufgelistet, die Sie beachten sollten, wenn Sie an der PowerShell-Dokumentation mitwirken:

- **Keine** unvermittelten großen Pull Requests. Eröffnen Sie stattdessen ein Issue, und beginnen Sie eine Diskussion, sodass sich die Teilnehmer auf eine Richtung einigen können, bevor Sie viel Zeit investieren.
- **Befolgen** Sie diesen Anweisungen und den Styleguides für [Code](powershell-style-code.md) und [Verweis](powershell-style-reference.md).
- **Verwenden Sie** die [Vorlage](powershell-style-basic-markdown.md) als Ausgangspunkt für Ihre Arbeit.
- **Erstellen Sie** einen separaten Branch in Ihrer Fork, bevor Sie an einem Artikel arbeiten.
- **Befolgen Sie** den [Workflow für GitHub Flow](../how-to-write-workflows-major.md).
- **Bloggen oder twittern Sie** regelmäßig über Ihre Beiträge.

Durch diese Richtlinien wird der Ablauf für Sie und für uns erleichtert.

## <a name="make-a-contribution-to-powershell-docs"></a>So tragen Sie zur PowerShell-Dokumentation bei

Sie können aus den folgenden [Issues](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose) auswählen.
Je nachdem, was Sie interessiert und wie viel Zeit Sie investieren möchten, fällt der Aufwand dafür in die folgenden Kategorien:

- **Kleine Änderungen**. Wenn Sie nur kleine Änderungen vornehmen müssen, finden Sie die entsprechenden Anweisungen für das Bearbeiten in GitHub auf der [Startseite](../index.md#quick-edits-to-existing-documents) des Leitfadens für Mitwirkende. Kleine Änderungen umfassen:

  - Das Beheben von Tipp- und Rechtschreibfehlern
  - Das Verbessern der Grammatik und Formatierung
  - Kleinere technische oder faktische Bearbeitungen

- **Korrekturen:** Zu dieser Kategorie zählen einfache Beiträge, z.B. das Korrigieren von fehlerhaften Links, das Hinzufügen von fehlenden Codebeispielen oder das Beheben von Problemen mit beschränktem Inhalt. Manchmal können diese Probleme viele Dateien betreffen. In diesem Fall sollten Sie uns darüber informieren, woran Sie arbeiten möchten, bevor Sie damit beginnen. Fügen Sie einen Kommentar zum Issue hinzu, um uns mitzuteilen, dass Sie daran arbeiten.

- **Inhaltsaktualisierung:** Durch die Größe der Dokumentation kann der Inhalt schnell veralten und muss überprüft werden. Außerdem sind manche Inhalte doppelt oder dreifach vorhanden. Beim Aktualisieren des Inhalts müssen Sie sicherstellen, dass einzelne Artikel aktuell sind oder den Inhalt in einem Featurebereich überprüfen, um Duplizierungen zu entfernen und sicherzustellen, dass einmaliger Inhalt in der kleineren Dokumentation beibehalten wird.

- **Erstellen neuer Inhalte:** Wenn Sie einen neuen Artikel erstellen möchten, finden Sie in diesen Issues die Themen, von denen bekannt ist, dass sie in einem Docset noch fehlen. Sie sollten uns allerdings mitteilen, dass Sie an einem Artikel arbeiten möchten, bevor Sie damit beginnen. Wenn Sie einen Artikel erstellen möchten, der nicht aufgeführt ist, eröffnen Sie ein Issue.

Sobald Sie einen Artikel ausgewählt haben, an dem Sie arbeiten möchten, befolgen Sie den [Leitfaden für die ersten Schritte](../get-started-setup-github.md), um ein GitHub-Konto zu erstellen und Ihre Umgebung einzurichten.

### <a name="making-large-changes"></a>Vornehmen größerer Änderungen

**Schritt 1:** Wenn Sie neue Inhalte erstellen oder bestehenden Inhalt überprüfen möchten, öffnen Sie ein Issue, in dem Sie beschreiben, was Sie vorhaben.

**Schritt 2:** Forken Sie das `MicrosoftDocs/PowerShell-Docs`-Repository, und erstellen Sie einen Arbeitsbranch für Ihre Änderungen.

**Schritt 3:** Nehmen Sie Änderungen in diesem neuen Branch vor.

Wenn es sich um ein neues Thema handelt, verwenden Sie die Vorlage im [Styleguide](powershell-style-basic-markdown.md) als Startpunkt. Dieser Styleguide enthält die Richtlinien für das Schreiben und erläutert die Metadaten, die für jeden Artikel erforderlich sind.

Navigieren Sie zu dem Ordner, der der Position im Inhaltsverzeichnis entspricht, die Sie in Schritt 1 für Ihren Artikel festgelegt haben.
Dieser Ordner enthält die Markdowndateien für alle Artikel in diesem Abschnitt. Erstellen Sie bei Bedarf einen neuen Ordner, in dem Sie die Dateien speichern können, aus denen Ihr Inhalt besteht. Der Hauptartikel für diesen Abschnitt heißt *index.md*.
Erstellen Sie für Bilder und andere statische Ressourcen einen Unterordner namens **media** in dem Ordner, der Ihren Artikel enthält (falls noch nicht vorhanden). Erstellen Sie im Ordner **media** einen Unterordner mit dem Namen des Artikels (außer für die Indexdatei).

Stellen Sie sicher, dass Sie die richtige Markdownsyntax verwenden. Bitte lesen Sie den [Styleguide](powershell-style-basic-markdown.md) für detaillierte Anweisungen und Beispiele.

**Beispielstruktur**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**Schritt 4:** Senden Sie einen Pull Request (PR) von Ihrem Branch zum *Staging*-Branch.

Jeder Pull Request sollte in der Regel nur ein Problem beheben. Mit einem Pull Request können eine oder mehrere Dateien geändert werden. Wenn Sie mehrere Probleme in verschiedenen Dateien beheben, sollten Sie mehrere Pull Requests erstellen.

Wenn Ihr Pull Request ein vorhandenes Problem behebt, fügen Sie das Schlüsselwort `Fixes #Issue_Number` zur Commitnachricht oder zur Beschreibung des Pull Requests hinzu. Dadurch wird das Issue automatisch geschlossen, wenn der Pull Request gemerget wurde. Weitere Informationen finden Sie unter [Closing issues via commit messages (Schließen von Issues über Commitnachrichten)](https://help.github.com/articles/closing-issues-via-commit-messages/).

Das PowerShell-Team überprüft Ihren Pull Request anschließend und teilt Ihnen mit, ob weitere Änderungen nötig sind, um diesen zu genehmigen.

**Schritt 5:** Nehmen Sie gemäß der Absprache mit dem Team die erforderlichen Änderungen an Ihrem Branch vor.

Sobald der Pull Request genehmigt ist, führen die Verwalter Ihren Pull Request im *Staging*-Branch ein. Regelmäßig werden alle Commits vom *Staging*-Branch in den *Live*-Branch gepusht. Sobald Ihr Beitrag live ist, können Sie ihn auf der Seite der [PowerShell-Dokumentation](https://docs.microsoft.com/PowerShell/) sehen. In der Regel veröffentlichen wir Beiträge zwei- bis dreimal in der Arbeitswoche.

## <a name="contributor-license-agreement"></a>Lizenzvereinbarung für Mitwirkende

Sie müssen die [Lizenzvereinbarung für Mitwirkende (Contribution License Agreement, CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) unterschreiben, bevor Ihr Pull Request gemergt wird. Dies ist eine einmalige Anforderung, wenn Sie zu unserer Dokumentation beitragen.

Sie müssen diese nicht im Voraus unterschreiben. Sie können Ihren Pull Request wie gewohnt klonen, forken und senden.
Wenn Ihr Pull Request erstellt wird, wird dieser von einem CLA-Bot klassifiziert. Wenn es sich nur um eine geringfügige Änderung handelt (z.B. das Korrigieren eines Tippfehlers), wird der Pull Request mit `cla-not-required` gekennzeichnet. Andernfalls wird er als `cla-required` klassifiziert. Sobald Sie die Lizenzvereinbarung für Mitwirkende (CLA) unterschrieben haben, werden alle aktuellen und zukünftigen Pull Requests als `cla-signed` gekennzeichnet.
