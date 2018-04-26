---
title: Installieren von Tools für die Inhaltsentwicklung
description: In diesem Artikel werden das Herunterladen und Installieren der Clienttools erläutert, die Sie für Git und das Bearbeiten von Markdowndateien benötigen.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>Installieren von Tools für die Inhaltsentwicklung

Dieser Artikel beschreibt die Schritte, die erforderlich sind, um Git-Clienttools und Visual Studio Code interaktiv zu installieren.
> [!div class="checklist"]
> * Installieren von [Git für Windows](https://git-scm.com/download/win)
> * Installieren von [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> Wenn Sie nur geringfügige Änderungen an einem Artikel vornehmen, müssen Sie die in diesem Artikel erläuterten Schritte *nicht* durchführen und können direkt mit dem Workflow für [geringfügige oder seltene Änderungen](light-workflow.md) fortfahren.
>
> Wichtige Mitwirkende sollten diese Schritte ausführen, da ihnen dadurch die Verwendung des [Workflows für größere Änderungen oder Änderungen mit langer Ausführungszeit](full-workflow.md) ermöglicht wird. Auch wenn Sie über Schreibberechtigungen im Hauptrepository verfügen, *wird ausdrücklich empfohlen, das Repository zu forken und zu klonen (dies wird in diesem Leitfaden vorausgesetzt)*, damit Sie über die Schreib- bzw. Leseberechtigungen verfügen, um vorgeschlagene Änderungen in Ihrem Fork zu speichern.

## <a name="install-git-client-tools-on-windows"></a>Installieren der Git-Clienttools unter Windows

 Installieren Sie die aktuelle Version der [Git-Clienttools von Software Freedom](https://git-scm.com/download/). Die Installation umfasst das Versionskontrollsystem von Git sowie Git Bash, die Befehlszeilen-App, die Sie zur Interaktion mit Ihrem lokalen Git-Repository verwenden.

Wenn Sie eine grafische Benutzeroberfläche (Graphical User Interface, GUI) gegenüber einer Befehlszeilenschnittstelle (Command-Line Interface, CLI) vorziehen, finden Sie einige gängige Optionen auf der [Seite zu GUI Clients von Software Freedom Conservancy](https://git-scm.com/downloads/guis), unter [GitHub Desktop auf GitHub](https://desktop.github.com/) oder [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).

Befolgen Sie die Anweisungen für die Installation und Konfiguration für Ihren Client.

Im nächsten Artikel geht es um das [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).

   Hier finden Sie weitere Git-Ressourcen (in englischer Sprache): [Git-Terminologie](https://help.github.com/articles/github-glossary) | [Git-Grundlagen](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Lernressourcen für Git und GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Grundlegendes zu Markdown-Editoren

Markdown ist eine leichte Markupsprache, die sowohl einfach zu lesen als auch zu lernen ist. Aus diesem Grund ist sie schnell zu einem Branchenstandard geworden. Um Artikel in Markdown zu schreiben, sollten Sie zuerst einen Markdown-Editor herunterladen und installieren.  [Visual Studio Code](https://code.visualstudio.com/) ist das bei Microsoft bevorzugte Tool zum Bearbeiten von Markdown. [Atom](https://atom.io) ist ein weiteres beliebtes Tool für die Markdownbearbeitung.

Markdowntext wird in Dateien mit der Erweiterung „MD“ gespeichert.

Nähere Informationen zum Schreiben mit Markdown, inklusive der Grundlagen von Markdown und der von benutzerdefinierten OPS-Markdownerweiterungen unterstützten Features werden später im Artikel [Verwenden von Markdown](how-to-write-use-markdown.md) behandelt.

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), auch als VS Code bezeichnet, ist ein schlanker Editor, der unter Windows, Linux und Mac verwendet werden kann. Er umfasst die Git-Integration sowie Unterstützung für Erweiterungen.

Laden Sie [VS Code](https://code.visualstudio.com/) herunter, und installieren Sie es. Die VS Code-Startseite sollte Ihr Betriebssystem erkennen.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Um VS Code zu starten und den aktuellen Ordner zu öffnen, führen Sie den Befehl `code .` an der Befehlszeile oder in der Bash-Shell aus. Wenn der aktuelle Ordner zu einem lokalen Git-Repository gehört, wird die GitHub-Integration automatisch in Visual Studio Code angezeigt.

## <a name="next-steps"></a>Nächste Schritte

Jetzt sind Sie bereit zum [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).
