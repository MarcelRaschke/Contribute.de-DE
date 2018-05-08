---
title: GitHub-Beitragsworkflow für geringfügige oder selten vorkommende Änderungen
description: In diesem Artikel erfahren Sie, wie Sie den Beitragsworkflow für geringfügige Änderungen bei der Mitwirkung an docs.microsoft.com-Artikeln verwenden.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>GitHub-Beitragsworkflow für geringfügige oder selten vorkommende Änderungen

> [!IMPORTANT]
> Für alle Repositorys, die in „docs.microsoft.com“ veröffentlichen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache). Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys werden durch die [docs.microsoft.com - Nutzungsbestimmungen](https://docs.microsoft.com/legal/termsofuse) abgedeckt. Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind. Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request annehmen können.

## <a name="overview"></a>Übersicht

Dieser Workflow eignet sich dazu, geringfügige oder selten vorkommende Änderungen mithilfe des webbasierten Markdown-Editors von GitHub vorzunehmen. Ihre Bearbeitungsmöglichkeiten im GitHub-Editor sind eingeschränkt, da die Benutzeroberfläche nicht alle Git-Vorgänge und Erstellungsszenarios unterstützt. Wenn Sie umfangreichere Beiträge erstellen müssen oder Unterstützung zu fortgeschrittenen Git-Features benötigen (z.B. Branchingverwaltung, fortgeschrittene Zusammenführungs-Konfliktlösung), beachten Sie bitte die Informationen zum [Beitragsworkflow für größere oder langfristige Änderungen](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Prozedur für die Verwendung des GitHub-Editors zum Vorschlagen Ihrer Änderungen

1. Durchsuchen Sie das GitHub-Repository und die Markdowndatei des Artikels. Dazu können Sie eine der folgenden Methoden verwenden:

   - Suchen Sie den Artikel, indem Sie die Markdowndateien im zugehörigen GitHub-Repository durchsuchen.
   - Navigieren Sie unter [https://docs.microsoft.com/](https://docs.microsoft.com/) zum Artikel, und klicken Sie dann rechts oben auf der Seite auf den Link **Bearbeiten**.

     ![Ort des Links „Bearbeiten“](./media/light-workflow/contributetogit.png)

2. Wählen Sie das Bleistiftsymbol für **Diese Datei bearbeiten** oben rechts aus, um in den Bearbeitungsmodus zu wechseln:

    ![Ort des Bleistiftsymbols](./media/light-workflow/editicon.png)

3. Nehmen Sie Änderungen vor, indem Sie Markdown auf der Registerkarte **Edit file** (Datei bearbeiten) verwenden, und zeigen Sie eine Vorschau Ihrer Änderungen auf der Registerkarte **Preview changes** (Vorschau der Änderungen) an. Die Verwendung des Editors ist recht einfach. Sollten Sie trotzdem Hilfe benötigen, nutzen Sie folgende Handbücher:

   - [Verwendung von Markdown](how-to-write-use-markdown.md)
   - [Erstellen von Dateien auf GitHub](https://github.com/blog/1327-creating-files-on-github)
   - [Hochladen von Dateien in Ihre Repositorys](https://github.com/blog/2105-upload-files-to-your-repositories)

4. Scrollen Sie zum unteren Rand der Seite, wo Sie eine der folgenden Optionen sehen:

   - **Propose file change** (Dateiänderung vorschlagen): Wird angezeigt, wenn Sie schreibgeschützten Zugriff auf das Repository haben, wie in [Editing files in another user's repository (Bearbeiten von Dateien im Repository eines anderen Benutzers)](https://help.github.com/articles/editing-files-in-another-user-s-repository/) beschrieben. In diesem Fall erstellt GitHub einen „Patch“-Branch in Ihrem Fork des Repositorys (und automatisch einen Fork, sofern nicht vorhanden). Nachdem Sie auf **Propose file change** (Dateiänderung vorschlagen) geklickt haben, wird die Seite **Comparing changes** (Änderungen vergleichen) angezeigt, damit Sie Ihre Änderungen überprüfen können. Klicken Sie dann auf die Schaltfläche **Create pull request** (Pull Request erstellen), um Ihre Änderungen an die Pull Request-Warteschlange zu übermitteln, und fahren Sie mit dem [nächsten Abschnitt](#pull-request-processing) fort.

   - **Commit changes** (Änderungen übernehmen): Wird angezeigt, wenn Sie über Schreibberechtigungen in einem Repository verfügen, wie in [Editing files in your own repository (Bearbeiten von Dateien in Ihrem eigenen Repository)](https://help.github.com/articles/editing-files-in-your-repository/) beschrieben. In diesem Fall bietet GitHub Ihnen zwei Optionen zum Speichern Ihrer Änderungen an:

     - **Commit directly to the `<branch-name>` branch** (Direkt an den Branche <Name des Branchs> übergeben), wobei `<branch-name>` der Name des Branchs ist, in dem Sie sich befanden, als Sie auf die Schaltfläche zur **Bearbeitung** geklickt haben. Hiermit werden Ihre Änderungen anstelle der Verwendung eines Pull Requests direkt auf den Branch angewandt. Jetzt sind Sie fertig!

     - **Erstellen Sie einen neuen Branch für diesen Commit und starten Sie einen Pull Request**. Dabei wird eine Eingabeaufforderung mit einem Standardnamen zum Erstellen eines neuen Branchs angezeigt. Nachdem Sie auf **Propose file change** (Dateiänderung vorschlagen) geklickt haben, wird die Seite **Comparing changes** (Änderungen vergleichen) angezeigt, damit Sie Ihre Änderungen überprüfen können. Klicken Sie dann auf die Schaltfläche **Create pull request** (Pull Request erstellen), um Ihre Änderungen an die Pull Request-Warteschlange zu übermitteln, und fahren Sie mit dem [nächsten Abschnitt](#pull-request-processing) fort.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Nächste Schritte

- Fahren Sie mit den Artikeln zu Schreibgrundlagen fort, um mehr über Themen wie Markdown, Markdownerweiterungssyntax usw. zu erfahren.
