---
title: Pack zur Dokumenterstellung für VS Code
description: VS Code-Erweiterungspaket zur vereinfachten Markdown-Dokumenterstellung für docs.microsoft.com
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.article: contributor-guide
ms.prod: n.a
ms.service: n.a
ms.technology: n.a
ms.openlocfilehash: 5c857deb07e28e1f6744c895a291bf78a6acf1df
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>Pack zur Dokumenterstellung für VS Code

Das Pack zur Dokumenterstellung ist eine Sammlung von VS Code-Erweiterungen zum vereinfachten Erstellen von Dokumenten für docs.microsoft.com. Das Pack kann im [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) heruntergeladen werden und enthält die folgenden Erweiterungen:

- **DocFX:** Stellt eine Markdownvorschau speziell für docs.microsoft.com zur Verfügung. Weitere Informationen finden Sie unter [DocFX](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX).
- **markdownlint:** Beliebter Markdownlinter von David Anson, der die Nutzung bewährter Methoden durch Markdown sicherstellt. Weitere Informationen finden Sie unter [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).
- **Docs Markdown:** Stellt Unterstützung bei der Markdown-Dokumenterstellung von docs.microsoft.com-Inhalten im Open Publishing System (OPS) bereit, einschließlich Basic-Support für Markdown sowie Unterstützung für benutzerdefinierte Markdownsyntax in OPS. Die weiteren Abschnitte dieses Themas behandeln die Erweiterung „Docs Markdown“.

## <a name="prerequisites-and-assumptions"></a>Voraussetzungen und Annahmen

Damit Sie relative Links, Images und andere eingebettete Inhalte mit der Erweiterung „Docs Markdown“ korrekt einfügen können, muss der VS Code-Arbeitsbereich dem Stamm Ihres geklonten OPS-Repositorys zugeordnet sein.

Ein Teil der von der Erweiterung unterstützten Syntax, wie z.B. Warnungen und Codeausschnitte, stellt für OPS ein benutzerdefiniertes Markdown dar. Diese Syntax wird daher nur korrekt gerendert, wenn sie über OPS veröffentlicht wird.

## <a name="how-to-use-the-docs-markdown-extension"></a>Verwenden der Erweiterung „Docs Markdown“

Drücken Sie `ALT+M`, um auf das Docs Markdown-Menü zuzugreifen. Klicken Sie auf die gewünschte Funktion, oder verwenden Sie dazu die NACH-OBEN-/NACH-UNTEN-TASTEN. Sie können zum Filtern auch mit der Eingabe des Namens beginnen und `ENTER` drücken, sobald die gewünschte Funktion im Menü hervorgehoben wird. Folgende Funktionen sind verfügbar:

|Funktion     |Befehl             |Beschreibung           |
|-------------|--------------------|----------------------|
|Fett         |`formatBold`        |Text wird **fett** formatiert.|
|Kursiv       |`formatItalic`      |Text wird *kursiv* formatiert.|
|Code         |`formatCode`        |Text wird als `inline code` formatiert, wenn höchstens eine Zeile ausgewählt ist.<br><br>Bei mehreren ausgewählten Zeilen werden diese als umgrenzter Codeblock formatiert. Sie können in diesem Fall optional auch eine von OPS unterstützte Programmiersprache festlegen.|
|Warnung        |`insertAlert`       |Es wird „Hinweis“, „Wichtig“, „Warnung“ oder „Tipp“ eingefügt.<br><br>Klicken Sie im Menü auf „Warnung“, und wählen Sie anschließend den Warnungstyp aus. Bereits ausgewählter Text wird in die Syntax der ausgewählten Warnung eingeschlossen. Wenn Sie noch keinen Text ausgewählt haben, wird eine neue Warnung mit Platzhaltertext hinzugefügt.|
|Nummerierte Liste|`insertNumberedList` |Eine nummerierte Liste wird eingefügt.<br><br> Bei mehreren ausgewählten Zeilen wird jede Zeile zu einem Element der Liste. Beachten Sie, dass bei nummerierten Listen alle Elemente im Markdown mit einer 1 angezeigt werden. Auf docs.microsoft.com werden sie hingegen als fortlaufende Zahlen oder bei geschachtelten Listen als Buchstaben gerendert. Verwenden Sie zum Erstellen einer geschachtelten nummerierten Liste den Tabstopp innerhalb der übergeordneten Liste.|
|Liste mit Aufzählungszeichen|`insertBulletedList` |Eine Liste mit Aufzählungszeichen wird eingefügt.|
|Tabelle        |`insertTable`        |Eine Markdown-Tabellenstruktur wird eingefügt.<br><br>Geben Sie nach dem Auswählen des Befehls „Tabelle“ die Anzahl der Spalten und Zeilen im Format „Spalten:Zeilen“ an, z.B. „3:4“. Beachten Sie, dass die maximale Spaltenanzahl, die mithilfe der Erweiterung angegeben werden kann, 5 beträgt. Dies ist auch die empfohlene Höchstzahl für Spalten, um eine optimale Lesbarkeit zu gewährleisten.|
|Link         |`selectLinkType`      |Ein Link wird eingefügt. Wenn Sie diesen Befehl auswählen, wird das folgende Untermenü angezeigt:<br><br>`External`: Link zu einer Webseite über den URI. Muss „http“ oder „https“ beinhalten.<br>`Internal`: Relativer Link zu einer anderen Datei im selben Repository. Nachdem Sie diese Option ausgewählt haben, geben Sie im Befehlsfenster Text ein, um die Dateien nach Namen zu filtern. Klicken Sie anschließend auf die gewünschte Datei. <br>`Bookmark in this file`: Treffen Sie in der aktuellen Datei in einer Liste mit Überschriften eine Auswahl, um ein korrekt formatiertes Lesezeichen einzufügen.<br>`Bookmark in another file`: Filtern Sie zunächst nach Dateinamen, und wählen Sie die Datei aus, auf die der Link verweisen soll. Wählen Sie dann die entsprechende Überschrift in der ausgewählten Datei aus.|
|Image        |`insertImage`     |Geben Sie Alternativtext ein (für die Barrierefreiheit erforderlich), und wählen Sie ihn aus. Rufen Sie dann diesen Befehl auf, um die Liste der unterstützten Bilddateien im Repository zu filtern, und wählen Sie die gewünschte Datei aus. Wenn Sie beim Aufrufen dieses Befehls keinen Alternativtext ausgewählt haben, werden Sie zu einer Eingabe aufgefordert, bevor Sie die Bilddatei auswählen können.|
|Einschließen      |`insertInclude`   |Eine Datei wird gesucht, die in die aktuelle Datei eingebettet werden soll.|
|Codeausschnitt      |`insertSnippet`   |Im Repository wird ein Codeausschnitt gesucht, der in die aktuelle Datei eingebettet werden soll.|
|Bewegte Bilder        |`insertVideo`     |Ein eingebettetes Video wird hinzugefügt.|
|Vorschau      |`previewTopic`    |Mithilfe der Erweiterung „DocFX“ wird das aktive Thema in einem Vorschaufenster parallel angezeigt.  Wenn die Erweiterung „DocFX“ nicht installiert ist, oder wenn sie zwar installiert jedoch deaktiviert ist, wird das Thema nicht gerendert.


## <a name="how-to-assign-keyboard-shortcuts"></a>Zuweisen von Tastenkombinationen

1. Drücken Sie zum Öffnen der Liste mit den Tastenkombinationen zuerst `CTRL+K` und anschließend `CTRL+S`.
1. Suchen Sie den Befehl, z.B. `formatBold`, für den Sie eine benutzerdefinierte Tastenzuordnung erstellen möchten.
1. Klicken Sie auf das Pluszeichen, das neben dem Befehlsnamen angezeigt wird, wenn Sie mit der Maus auf die Zeile zeigen.
1. Geben Sie in das neu angezeigte Eingabefeld die Tastenkombination ein, die mit diesem bestimmten Befehl verknüpft werden soll. Geben Sie z.B. `ctrl+b` ein, um die gängige Tastenkombination für Fettdruck zu verwenden.
1. Es wird empfohlen, in die Tastenzuordnung eine `when`-Klausel einzufügen, damit die Zuordnung nur in Markdowndateien verfügbar ist. Öffnen Sie hierzu *keybindings.json*, und fügen Sie die folgende Zeile unterhalb des Befehlsnamens ein (achten Sie dabei auf das Komma zwischen den Zeilen):
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Die fertige benutzerdefinierte Tastenzuordnung sollte in „keybindings.json“ wie folgt aussehen:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Speichern Sie die Datei „keybindings.json“.

Weitere Informationen finden Sie unter [Keybindings (Tastenzuordnungen)](https://code.visualstudio.com/docs/getstarted/keybindings) in der VS Code-Dokumentation.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Anzeigen der Symbolleiste „Gauntlet“ der Vorgängerversion

Die Symbolleiste zur Dokumenterstellung aus dem Erweiterungscode „Gauntlet“ der Vorgängerversion wird nicht mehr unten im VS Code-Fenster angezeigt, wenn die Erweiterung „Docs Markdown“ installiert wurde. Dies liegt daran, dass die Symbolleiste in der VS Code-Statusleiste viel Platz in Anspruch nahm und nicht den bewährten Methoden für Benutzerfreundlichkeit entsprach, weshalb sie in der neuen Erweiterung verworfen wurde. Sie können die Symbolleiste jedoch optional anzeigen, indem Sie die VS Code-Datei „settings.json“ wie folgt aktualisieren:

1. Gehen Sie in VS Code zu „Datei“ > „Einstellungen“ > „Einstellungen“ (`CTRL+Comma`).
1. Wählen Sie „Benutzereinstellungen“ aus, um die Einstellungen für sämtliche VS Code-Arbeitsbereiche zu ändern, oder „Arbeitsbereichseinstellungen“, um nur die Einstellungen für den aktuellen Arbeitsbereich zu ändern.
1. Suchen Sie im Bereich „Standardeinstellungen“ nach der Konfiguration für die Erweiterung „Docs Authoring“, und klicken Sie auf das Bleistiftsymbol neben der gewünschten Einstellung. Als Nächstes werden Sie aufgefordert, `true` oder `false` auszuwählen. Anschließend wird der Wert durch VS Code automatisch der Datei „settings.json“ hinzugefügt. Sie werden nun aufgefordert, das Fenster erneut zu laden, damit die Änderungen wirksam werden.

## <a name="known-issues"></a>Bekannte Probleme

- [DocFX Preview]: MacOS und Linux: Die Vorschau wird von DocFX Preview nicht korrekt gestartet (die Standardvorschau für diese Plattformen lautet „VS Code Markdown-Vorschau“).
- [DocFX Preview]: Alle Plattformen: Ein Teil der Syntax, z.B. XRef-Links (Querverweise) zu APIs, wird in der Vorschau nicht korrekt gerendert, wodurch in einigen Fällen Lücken im Inhalt entstehen.
- [External bookmarks]: Linux: Die Dateiliste wird angezeigt, jedoch keine Überschriften, die ausgewählt werden können.
- [Includes]: Linux: Die Dateiliste wird angezeigt, doch nach der Auswahl wird kein Link hinzugefügt.