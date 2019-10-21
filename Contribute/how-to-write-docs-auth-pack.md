---
title: Docs Authoring Pack für Visual Studio Code
description: In diesem Artikel wird das Visual Studio Code-Erweiterungspaket zur vereinfachten Markdown-Dokumenterstellung für docs.microsoft.com beschrieben.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 11f18ce4f769b478108d399b780937f927e0e12d
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288330"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Pack zur Dokumenterstellung für VS Code

Das Docs Authoring Pack (Pack zur Dokumenterstellung) ist eine Sammlung von Visual Studio Code-Erweiterungen zum vereinfachten Erstellen von Dokumenten für docs.microsoft.com. Das Pack kann im [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) heruntergeladen werden und enthält die folgenden Erweiterungen:

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Beliebter Markdownlinter von David Anson, der die Nutzung bewährter Methoden durch Markdown sicherstellt.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Eine vollständige Offline-Rechtschreibprüfung von Street Side Software.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Verwendet das docs.microsoft.com-CSS für präzisere Markdownvorschau inklusive benutzerdefinierten Markdowns.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Stellt Unterstützung bei der Markdowndokumenterstellung von docs.microsoft.com-Inhalten im Open Publishing System (OPS) bereit, einschließlich Basic-Support für Markdown sowie Unterstützung für benutzerdefinierte Markdownsyntax in OPS. Die weiteren Abschnitte dieses Themas behandeln die Erweiterung „Docs Markdown“.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Ermöglicht Benutzern die Anwendung von Markdownentwurfsinhalt auf neue Dateien.

## <a name="prerequisites-and-assumptions"></a>Voraussetzungen und Annahmen

Damit Sie relative Links, Images und andere eingebettete Inhalte mit der Erweiterung „Docs Markdown“ korrekt einfügen können, muss der VS Code-Arbeitsbereich dem Stamm Ihres geklonten OPS-Repositorys (Open Publishing System) zugeordnet sein.

Ein Teil der von der Erweiterung unterstützten Syntax, wie z.B. Warnungen und Codeausschnitte, stellt für OPS ein benutzerdefiniertes Markdown dar. Diese Syntax wird daher nur korrekt gerendert, wenn sie über OPS veröffentlicht wird.

## <a name="how-to-use-the-docs-markdown-extension"></a>Verwenden der Erweiterung „Docs Markdown“

Drücken Sie `ALT+M`, um auf das Docs Markdown-Menü zuzugreifen. Klicken Sie auf die gewünschte Funktion, oder verwenden Sie dazu die NACH-OBEN-/NACH-UNTEN-TASTEN. Sie können zum Filtern auch mit der Eingabe des Namens beginnen und `ENTER` drücken, sobald die gewünschte Funktion im Menü hervorgehoben wird. Folgende Funktionen sind verfügbar:

|Funktion     |Description           |
|-------------|----------------------|
|Vorschau      |Mithilfe der Erweiterung „Docs Preview“ wird das aktive Thema in einem Vorschaufenster parallel angezeigt. Diese Option ist nur verfügbar, wenn „Docs Preview“ installiert ist.|
|Fett         |Text wird **fett** formatiert.|
|Kursiv       |Text wird *kursiv* formatiert.|
|Code         |Text wird als `inline code` formatiert, wenn höchstens eine Zeile ausgewählt ist.<br><br>Bei mehreren ausgewählten Zeilen werden diese als umgrenzter Codeblock formatiert. Sie können in diesem Fall optional auch eine von OPS unterstützte Programmiersprache festlegen.|
|Warnung        |Es wird „Hinweis“, „Wichtig“, „Warnung“ oder „Tipp“ eingefügt.<br><br>Klicken Sie im Menü auf „Warnung“, und wählen Sie anschließend den Warnungstyp aus. Bereits ausgewählter Text wird in die Syntax der ausgewählten Warnung eingeschlossen. Wenn Sie noch keinen Text ausgewählt haben, wird eine neue Warnung mit Platzhaltertext hinzugefügt.|
|Nummerierte Liste|Eine nummerierte Liste wird eingefügt.<br><br> Bei mehreren ausgewählten Zeilen wird jede Zeile zu einem Element der Liste. Beachten Sie, dass bei nummerierten Listen alle Elemente im Markdown mit einer 1 angezeigt werden. Auf docs.microsoft.com werden sie hingegen als fortlaufende Zahlen oder bei geschachtelten Listen als Buchstaben gerendert. Verwenden Sie zum Erstellen einer geschachtelten nummerierten Liste den Tabstopp innerhalb der übergeordneten Liste.|
|Liste mit Aufzählungszeichen|Eine Liste mit Aufzählungszeichen wird eingefügt.|
|Tabelle        |Eine Markdown-Tabellenstruktur wird eingefügt.<br><br>Geben Sie nach dem Auswählen des Befehls „Tabelle“ die Anzahl der Spalten und Zeilen im Format „Spalten:Zeilen“ an, z.B. „3:4“. Beachten Sie, dass die maximale Spaltenanzahl, die mithilfe der Erweiterung angegeben werden kann, 5 beträgt. Dies ist auch die empfohlene Höchstzahl für Spalten, um eine optimale Lesbarkeit zu gewährleisten.|
|Link zu Datei im Repository|Fügt einen relativen Link zu einer anderen Datei im aktuellen Repository ein. Nachdem Sie diese Option ausgewählt haben, geben Sie im Befehlsfenster Text ein, um die Dateien nach Namen zu filtern. Klicken Sie anschließend auf die gewünschte Datei. Wenn Sie zuvor Text ausgewählt haben, wird er nun zum Linktext. Andernfalls wird H1 der Zieldatei als Linktext verwendet.|
|Link zur Webseite    |Fügt einen Link zu einer Webseite ein. Fügen Sie nach Auswahl dieser Option den URI in das Befehlsfenster ein, bzw. tippen Sie ihn ein. `https://` ist erforderlich. Wenn Sie zuvor Text ausgewählt haben, wird er nun zum Linktext. Andernfalls wird der URI als Linktext verwendet.|
|Link zur Überschrift     |Links zu einer Textmarke in der aktuellen Datei oder einer anderen Datei im Repository.<br>`Bookmark in this file`: Treffen Sie in der aktuellen Datei in einer Liste mit Überschriften eine Auswahl, um ein korrekt formatiertes Lesezeichen einzufügen.<br>`Bookmark in another file`: Filtern Sie zunächst nach Dateinamen, und wählen Sie die Datei aus, auf die der Link verweisen soll. Wählen Sie dann die entsprechende Überschrift in der ausgewählten Datei aus.|
|Image        |Geben Sie Alternativtext ein (für die Barrierefreiheit erforderlich), und wählen Sie ihn aus. Rufen Sie dann diesen Befehl auf, um die Liste der unterstützten Bilddateien im Repository zu filtern, und wählen Sie die gewünschte Datei aus. Wenn Sie beim Aufrufen dieses Befehls keinen Alternativtext ausgewählt haben, werden Sie zu einer Eingabe aufgefordert, bevor Sie die Bilddatei auswählen können.|
|Einschließen      |Eine Datei wird gesucht, die in die aktuelle Datei eingebettet werden soll.|
|Codeausschnitt      |Im Repository wird ein Codeausschnitt gesucht, der in die aktuelle Datei eingebettet werden soll.|
|Bewegte Bilder        |Ein eingebettetes Video wird hinzugefügt.|
|Vorlage     |Erstellen Sie eine neue Datei, und wenden Sie eine Markdown-Vorlage an. Weitere Informationen finden Sie unten unter [Vorlagen](#how-to-use-docs-templates).|

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

## <a name="how-to-show-the-legacy-toolbar"></a>Anzeigen der Symbolleiste der Vorgängerversion

Benutzern der Vorabversion der Erweiterung wird auffallen, dass die Symbolleiste zur Dokumenterstellung nicht mehr unten im VS Code-Fenster angezeigt wird, wenn die Erweiterung „Docs Markdown“ installiert wurde. Dies liegt daran, dass die Symbolleiste in der VS Code-Statusleiste viel Platz in Anspruch nahm und nicht den bewährten Methoden für Benutzerfreundlichkeit entsprach, weshalb sie in der neuen Erweiterung verworfen wurde. Sie können die Symbolleiste jedoch optional anzeigen, indem Sie die VS Code-Datei „settings.json“ wie folgt aktualisieren:

1. Gehen Sie in VS Code zu „Datei“ > „Einstellungen“ > „Einstellungen“ (`CTRL+Comma`).
1. Wählen Sie „Benutzereinstellungen“ aus, um die Einstellungen für sämtliche VS Code-Arbeitsbereiche zu ändern, oder „Arbeitsbereichseinstellungen“, um nur die Einstellungen für den aktuellen Arbeitsbereich zu ändern.
1. Suchen Sie im Bereich „Standardeinstellungen“ nach der Konfiguration für die Erweiterung „Docs Authoring“, und klicken Sie auf das Bleistiftsymbol neben der gewünschten Einstellung. Als Nächstes werden Sie aufgefordert, `true` oder `false` auszuwählen. Anschließend wird der Wert durch VS Code automatisch der Datei „settings.json“ hinzugefügt. Sie werden nun aufgefordert, das Fenster erneut zu laden, damit die Änderungen wirksam werden.

## <a name="how-to-use-docs-templates"></a>Verwenden von Docs-Vorlagen

Mit der „Docs Article Templates“-Erweiterung können Autoren in VS Code eine Markdown-Vorlage aus einem zentralen Speicher pullen und auf eine Datei anwenden. Vorlagen können dazu beitragen, sicherzustellen, dass erforderliche Metadaten in Artikel einbezogen, Inhaltsstandards befolgt werden usw. Vorlagen werden als Markdown-Dateien in einem öffentlichen GitHub-Repository verwaltet.

### <a name="to-apply-a-template-in-vs-code"></a>So wenden Sie eine Vorlage in VS Code an

1. Wenn Sie die Erweiterung „Docs Markdown“ nicht installiert haben, öffnen Sie mit F1 die Befehlspalette, geben Sie „template“ zum Filtern ein, und klicken Sie auf `Docs: Template`. Wenn Sie „Docs Markdown“ installiert haben, können Sie entweder die Befehlspalette verwenden, oder klicken Sie auf `Alt+M`, um das „Docs Markdown QuickPick“-Menü aufzurufen, und wählen Sie `Template` in der Liste aus.
1. Wählen Sie die gewünschte Vorlage in der angezeigten Liste aus.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>So fügen Sie Ihre GitHub-ID und/oder Ihren Microsoft-Alias Ihren VS Code-Einstellungen hinzu

Die Erweiterung „Templates“ unterstützt drei dynamische Metadatenfelder: „author“, „ms.author“ und „ms.date“. Dies bedeutet: Wenn ein Vorlagenersteller diese Felder im Metadatenheader einer Markdown-Vorlage verwendet, werden sie automatisch wie folgt in Ihrer Datei gefüllt, wenn Sie die Vorlage anwenden:

|Metadaten  |Wert|
|----------|---------------|
|author    |Ihre GitHub-ID, sofern in Ihrer VS Code-Einstellungendatei angegeben.|
|ms.author |Ihr Microsoft-Alias, sofern in Ihrer VS Code-Einstellungendatei angegeben. Wenn Sie kein Microsoft-Mitarbeiter sind, geben Sie hier nichts an.|
|ms.date   |Das aktuelle Datum im Docs-unterstützten Format, MM/TT/JJJJ. Beachten Sie, dass das Datum nicht automatisch aktualisiert wird, wenn Sie die Datei anschließend aktualisieren. Sie müssen den Wert „ms.date“ manuell aktualisieren, um das neueste Veröffentlichungsdatum auf der Website „docs.microsoft.com“ anzugeben.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>So legen Sie „author“ (GitHub-ID) und/oder „ms.author“ (Microsoft-Alias) fest

1. Gehen Sie in VS Code zu „Datei“ > „Einstellungen“ > „Einstellungen“ (`CTRL+Comma`).
1. Wählen Sie „Benutzereinstellungen“ aus, um die Einstellungen für sämtliche VS Code-Arbeitsbereiche zu ändern, oder „Arbeitsbereichseinstellungen“, um nur die Einstellungen für den aktuellen Arbeitsbereich zu ändern.
1. Suchen Sie links im Bereich „Standardeinstellungen“ „Docs Article Templates-Erweiterungskonfiguration“, klicken Sie auf das Stiftsymbol neben der gewünschten Einstellung und dann auf „In Einstellungen ersetzen“.
1. Der Bereich „Benutzereinstellungen“ wird mit einem neuen Eintrag am unteren Rand parallel angezeigt.
1. Fügen Sie Ihre GitHub-ID oder Ihren Microsoft-E-Mail-Alias hinzu, und speichern Sie die Datei.
1. Möglicherweise müssen Sie VS Code schließen und neu starten, damit die Änderungen wirksam werden.
1. Wenn Sie jetzt eine Vorlage anwenden, die dynamische Felder verwendet, wird Ihre GitHub-ID und/oder Ihr Microsoft-Alias im Metadatenheader automatisch eingetragen.
