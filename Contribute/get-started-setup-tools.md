---
title: Installieren von Tools für die Inhaltsentwicklung
description: In diesem Artikel werden das Herunterladen und Installieren der Clienttools erläutert, die Sie für Git und das Bearbeiten von Markdowndateien benötigen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
ms.openlocfilehash: 24d47c4e094c318be75a27dbaaec11d8ead94452
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288557"
---
# <a name="install-content-authoring-tools"></a>Installieren von Tools für die Inhaltsentwicklung

Dieser Artikel beschreibt die Schritte, die erforderlich sind, um Git-Clienttools und Visual Studio Code interaktiv zu installieren.
> [!div class="checklist"]
> * Installieren von [Git](https://git-scm.com/)
> * Installieren von [Visual Studio Code](https://code.visualstudio.com/)
> * Installieren von [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> Wenn Sie nur geringfügige Änderungen an einem Artikel vornehmen, müssen Sie die in diesem Artikel erläuterten Schritte *nicht* durchführen und können direkt mit dem Workflow für [schnelle Änderungen](index.md#quick-edits-to-existing-documents) fortfahren.
>
> Wichtige Mitwirkende sollten diese Schritte ausführen, da ihnen dadurch die Verwendung des [Workflows für größere Änderungen oder Änderungen mit langer Ausführungszeit](how-to-write-workflows-major.md) ermöglicht wird. Auch wenn Sie über Schreibberechtigungen im Hauptrepository verfügen, *wird ausdrücklich empfohlen, das Repository zu forken und zu klonen (dies wird in diesem Leitfaden vorausgesetzt)* , damit Sie über die Schreib- bzw. Leseberechtigungen verfügen, um vorgeschlagene Änderungen in Ihrem Fork zu speichern.

## <a name="install-git-client-tools"></a>Installieren der Git-Clienttools 

 Installieren Sie die aktuelle Version der [Git-Clienttools von Software Freedom](https://git-scm.com/download/) für Ihre Plattform. 

* [Git für Windows](https://git-scm.com/download/win): Diese Installation umfasst das Versionskontrollsystem von Git sowie Git Bash, die Befehlszeilen-App, die Sie zur Interaktion mit Ihrem lokalen Git-Repository verwenden.
* Git für Mac ist Teil der Xcode Command Line Tools. Führen Sie einfach `git` über die Befehlszeile aus. Sie werden ggf. aufgefordert, die Befehlszeilentools zu installieren. Sie können auch [Git für Mac](https://git-scm.com/download/mac) von Software Freedom Conservancy herunterladen.
* [Git für Linux und Unix](https://git-scm.com/download/linux)

Wenn Sie eine grafische Benutzeroberfläche (Graphical User Interface, GUI) gegenüber einer Befehlszeilenschnittstelle (Command-Line Interface, CLI) vorziehen, finden Sie einige gängige Optionen auf der [Seite zu GUI Clients von Software Freedom Conservancy](https://git-scm.com/downloads/guis), unter [GitHub Desktop auf GitHub](https://desktop.github.com/) oder [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).

Befolgen Sie die Anweisungen für die Installation und Konfiguration für Ihren Client.

Im nächsten Artikel geht es um das [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).

   Weitere Git-Ressourcen sind hier verfügbar: [Git-Terminologie](https://help.github.com/articles/github-glossary) | [Git-Grundlagen](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git und GitHub lernen](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Grundlegendes zu Markdown-Editoren

Markdown ist eine leichte Markupsprache, die sowohl einfach zu lesen als auch zu lernen ist. Aus diesem Grund ist sie schnell zu einem Branchenstandard geworden. Um Artikel in Markdown zu schreiben, sollten Sie zuerst einen Markdown-Editor herunterladen und installieren.  [Visual Studio Code](https://code.visualstudio.com/) ist das bei Microsoft bevorzugte Tool zum Bearbeiten von Markdown. [Atom](https://atom.io) ist ein weiteres beliebtes Tool für die Markdownbearbeitung.

Markdowntext wird in Dateien mit der Erweiterung „MD“ gespeichert.

Nähere Informationen zum Schreiben mit Markdown, inklusive der Grundlagen von Markdown und der von benutzerdefinierten Open Publishing Services-Markdownerweiterungen (OPS) unterstützten Features werden in den Artikeln [Verwenden von Markdown für das Schreiben von Dokumentationsartikeln](how-to-write-use-markdown.md) und [Markdownreferenz für OPS](markdown-reference.md) behandelt.

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), auch als VS Code bezeichnet, ist ein schlanker Editor, der unter Windows, Linux und Mac verwendet werden kann. Er umfasst die Git-Integration sowie Unterstützung für Erweiterungen.

Laden Sie [VS Code](https://code.visualstudio.com/) herunter, und installieren Sie es. Die VS Code-Startseite sollte Ihr Betriebssystem erkennen.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Um VS Code zu starten und den aktuellen Ordner zu öffnen, führen Sie den Befehl `code .` an der Befehlszeile oder in der Bash-Shell aus. Wenn der aktuelle Ordner zu einem lokalen Git-Repository gehört, wird die GitHub-Integration automatisch in Visual Studio Code angezeigt.

## <a name="docs-authoring-pack"></a>Docs Authoring Pack
Installieren Sie das Docs Authoring Pack für Visual Studio Code. Dieser Satz von Erweiterungen bietet grundlegende Unterstützung zum Schreiben von Markdown-Texten und eine Vorschaufunktion, sodass Sie sehen können, wie der Markdown-Text im Stil der Website „docs.microsoft.com“ aussieht.

   Besuchen Sie diese [Marketplace-Seite](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), und wählen Sie **Installieren** aus, oder suchen Sie im VS Code-Fenster in Ihrer Erweiterungenliste nach `docsmsft.docs-authoring-pack`. 

   Um auf das Docs Authoring Pack zuzugreifen, drücken Sie im VS Code-Fenster auf Alt+M. Die Symbolleiste ist standardmäßig ausgeblendet, kann aber angezeigt werden. Bearbeiten Sie die VS Code-Einstellungen (STRG+Komma), und fügen Sie die Benutzereinstellung `"markdown.showToolbar": true` hinzu, um die Symbolleiste anzuzeigen.

   Weitere Informationen finden Sie auf der [Docs Authoring Pack](how-to-write-docs-auth-pack.md)-Seite.


## <a name="next-steps"></a>Nächste Schritte

Jetzt sind Sie bereit zum [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).
