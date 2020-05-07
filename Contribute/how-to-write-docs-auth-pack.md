---
title: Docs Authoring Pack für Visual Studio Code
description: In diesem Artikel wird das Visual Studio Code-Erweiterungspaket zur vereinfachten Markdown-Dokumenterstellung für docs.microsoft.com beschrieben.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336389"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Pack zur Dokumenterstellung für VS Code

Das Pack zur Dokumenterstellung ist eine Sammlung von VS Code-Erweiterungen zum vereinfachten Erstellen von Dokumenten für docs.microsoft.com. Das Pack kann im [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) heruntergeladen werden und enthält die folgenden Erweiterungen:

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Stellt Unterstützung bei der Markdowndokumenterstellung für docs.microsoft.com (Docs)-Inhalte bereit, einschließlich grundlegender Unterstützung für Markdown sowie Unterstützung für benutzerdefinierte Markdownsyntax in Docs, z. B. Warnungen, Codeausschnitte und nicht lokalisierbaren Text. Enthalten ist nun auch grundlegende Unterstützung bei der YAML-Dokumenterstellung, z. B. Einfügen von Inhaltsverzeichniseinträgen.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Beliebter Markdownlinter von David Anson, mit dem sichergestellt werden kann, dass Ihr Markdown gültig ist.
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Eine vollständige Offline-Rechtschreibprüfung von Street Side Software.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Verwendet das docs.microsoft.com-CSS für präzisere Markdownvorschau inklusive benutzerdefinierten Markdowns.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Ermöglicht Benutzern den Gerüstbau für Lernmodule und die Anwendung von Markdownentwurfsinhalt auf neue Dateien.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Stellt Docs YAML-Schemavalidierung und automatische Vervollständigung bereit.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): Ermöglicht die Komprimierung und das Ändern der Größe von Bildern für Ordner und einzelne Dateien als Hilfe für Autoren von docs.microsoft.com.

## <a name="prerequisites-and-assumptions"></a>Voraussetzungen und Annahmen

Damit Sie relative Links, Bilder und andere eingebettete Inhalte mit der Erweiterung „Docs Markdown“ einfügen können, muss der VS Code-Arbeitsbereich dem Stamm Ihres geklonten OPS-Repositorys (Open Publishing System) zugeordnet sein. Wenn Sie z. B. das Dokumentenrepository nach `C:\git\SomeDocsRepo\` geklont haben, öffnen Sie diesen Ordner oder einen Unterordner in VS Code: **Datei** > Menü **Ordner öffnen** oder `code C:\git\SomeDocsRepo\` über die Befehlszeile.

Ein Teil der von der Erweiterung unterstützten Syntax, wie z. B. Warnungen und Codeausschnitte, stellt für OPS benutzerdefiniertes Markdown dar. Benutzerdefiniertes Markdown wird nur korrekt gerendert, wenn es über OPS veröffentlicht wird.

## <a name="how-to-use-the-docs-markdown-extension"></a>Verwenden der Erweiterung „Docs Markdown“

Drücken Sie <kbd>ALT+M</kbd>, um auf das **Docs Markdown**-Menü zuzugreifen. Zum Auswählen des gewünschten Befehls können Sie klicken oder die NACH-OBEN-/NACH-UNTEN-TASTEN verwenden. Sie können auch zum Filtern mit der Eingabe beginnen und die <kbd>EINGABETASTE</kbd> drücken, sobald die gewünschte Funktion im Menü hervorgehoben wird.

Eine aktuelle Liste der Befehle finden Sie in der [Infodatei zu Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown).

## <a name="how-to-generate-a-master-redirect-file"></a>Generieren einer Masterumleitungsdatei

Die Erweiterung „Docs Markdown“ enthält ein Skript zum Generieren oder Aktualisieren einer Masterumleitungsdatei für ein Repository, das auf den `redirect_url`-Metadaten in einzelnen Dateien basiert. Mit diesem Skript werden alle Markdowndateien im Repository auf `redirect_url` überprüft, die Umleitungsmetadaten der Masterumleitungsdatei ( *.openpublishing.redirection.json*) für das Repository hinzugefügt und die umgeleiteten Dateien in einen Ordner außerhalb des Repositorys verschoben. So führen Sie das Skript aus:

1. Drücken Sie <kbd>F1</kbd>, um die VS Code-Befehlspalette zu öffnen.
2. Beginnen Sie mit der Eingabe „Docs: Generate...“
3. Wählen Sie den Befehl `Docs: Generate master redirection file` aus.
4. Wenn die Ausführung des Skripts abgeschlossen ist, werden die Umleitungsergebnisse im VS Code-Ausgabebereich angezeigt, und die entfernten Markdowndateien werden dem Ordner „Docs Authoring\redirects“ unter Ihrem Standardpfad hinzugefügt.
5. Überprüfen Sie die Ergebnisse. Wenn sie den Erwartungen entsprechen, senden Sie einen Pull Request, um das Repository zu aktualisieren.

## <a name="how-to-assign-keyboard-shortcuts"></a>Zuweisen von Tastenkombinationen

1. Drücken Sie <kbd>STRG+K</kbd> und dann <kbd>STRG+S</kbd>, um die Liste mit den **Tastenkombinationen** zu öffnen.
1. Suchen Sie den Befehl, z. B. `formatBold`, für den Sie eine benutzerdefinierte Tastenzuordnung erstellen möchten.
1. Klicken Sie auf das Pluszeichen, das neben dem Befehlsnamen angezeigt wird, wenn Sie mit der Maus auf die Zeile zeigen.
1. Geben Sie in das neu angezeigte Eingabefeld die Tastenkombination ein, die mit diesem bestimmten Befehl verknüpft werden soll. Geben Sie z. B. <kbd>STRG+B</kbd> ein, um die gängige Tastenkombination für Fettdruck zu verwenden.
1. Es wird empfohlen, in die Tastenzuordnung eine `when`-Klausel einzufügen, damit die Zuordnung nur in Markdowndateien verfügbar ist. Öffnen Sie hierzu *keybindings.json*, und fügen Sie die folgende Zeile unterhalb des Befehlsnamens ein (achten Sie dabei auf das Komma zwischen den Zeilen):

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Die fertige benutzerdefinierte Tastenzuordnung sollte in *keybindings.json* wie folgt aussehen:

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > Fügen Sie Ihre Tastenzuordnung in diese Datei ein, um die Standardwerte zu überschreiben

1. Speichern Sie die Datei *keybindings.json*.

Weitere Informationen zu Tastenzuordnungen finden Sie in der [VS Code-Dokumentation](https://code.visualstudio.com/docs/getstarted/keybindings).

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Anzeigen der Symbolleiste „Gauntlet“ der Vorgängerversion

Die Symbolleiste zur Dokumenterstellung aus dem Erweiterungscode „Gauntlet“ der Vorgängerversion wird nicht mehr unten im VS Code-Fenster angezeigt, wenn die Erweiterung „Docs Markdown“ installiert wurde. Dies liegt daran, dass die Symbolleiste in der VS Code-Statusleiste viel Platz in Anspruch nahm und nicht den bewährten Methoden für Benutzerfreundlichkeit entsprach, weshalb sie in der neuen Erweiterung verworfen wurde. Sie können die Symbolleiste jedoch optional anzeigen, indem Sie die VS Code-Datei „settings.json“ wie folgt aktualisieren:

1. Navigieren Sie in VS Code zu **Datei** > **Einstellungen** > **Einstellungen**, oder drücken Sie <kbd>STRG+,</kbd>.
1. Wählen Sie **Benutzereinstellungen** aus, um die Einstellungen für sämtliche VS Code-Arbeitsbereiche zu ändern, oder **Arbeitsbereichseinstellungen**, um nur die Einstellungen für den aktuellen Arbeitsbereich zu ändern.
1. Wählen Sie **Erweiterungen** > **Docs Markdown-Erweiterungskonfiguration** und dann die Option zum**Anzeigen der Symbolleiste der Vorgängerversion in der Statusleiste am unteren Rand aus**.

   ![Einstellung für das Anzeigen der Symbolleiste der Vorgängerversion in VS Code](docs-authoring/media/show-gauntlet-bar.png)

Nachdem Sie Ihre Auswahl getroffen haben, aktualisiert VS Code die Datei *settings.json*. Anschließend werden Sie aufgefordert, das Fenster neu zu laden, damit die Änderungen wirksam werden.

Neuere Befehle, die der Erweiterung hinzugefügt wurden, sind nicht über die Symbolleiste verfügbar.

## <a name="how-to-use-docs-templates"></a>Verwenden von Docs-Vorlagen

Mit der „Docs Article Templates“-Erweiterung können Autoren in VS Code eine Markdown-Vorlage aus einem zentralen Speicher pullen und auf eine Datei anwenden. Vorlagen können dazu beitragen, sicherzustellen, dass erforderliche Metadaten in Artikel einbezogen, Inhaltsstandards befolgt werden usw. Vorlagen werden als Markdown-Dateien in einem öffentlichen GitHub-Repository verwaltet.

### <a name="to-apply-a-template-in-vs-code"></a>So wenden Sie eine Vorlage in VS Code an

1. Stellen Sie sicher, dass die Erweiterung „Docs Article Templates“ installiert und aktiviert ist.
1. Wenn Sie die Erweiterung „Docs Markdown“ nicht installiert haben, öffnen Sie mit <kbd>F1</kbd> die Befehlspalette, geben Sie „template“ zum Filtern ein, und klicken Sie auf `Docs: Template`. Wenn Sie „Docs Markdown“ installiert haben, können Sie entweder die Befehlspalette verwenden, oder drücken Sie <kbd>ALT+M</kbd>, um das „Docs Markdown QuickPick“-Menü aufzurufen, und wählen Sie `Template` in der Liste aus.
1. Wählen Sie die gewünschte Vorlage in der angezeigten Liste aus.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>So fügen Sie Ihre GitHub-ID und/oder Ihren Microsoft-Alias Ihren VS Code-Einstellungen hinzu

Die Erweiterung „Templates“ unterstützt drei dynamische Metadatenfelder: „author“, „ms.author“ und „ms.date“. Dies bedeutet: Wenn ein Vorlagenersteller diese Felder im Metadatenheader einer Markdown-Vorlage verwendet, werden sie automatisch wie folgt in Ihrer Datei gefüllt, wenn Sie die Vorlage anwenden:

| Metadatenfeld | Wert |
|--|--|
| `author` | Ihr GitHub-Alias, sofern in Ihrer VS Code-Einstellungendatei angegeben. |
| `ms.author` | Ihr Microsoft-Alias, sofern in Ihrer VS Code-Einstellungendatei angegeben. Wenn Sie kein Microsoft-Mitarbeiter sind, geben Sie hier nichts an. |
| `ms.date` | Das aktuelle Datum im Docs-unterstützten Format `MM/DD/YYYY`. Wenn Sie die Datei anschließend aktualisieren, wird das Datum nicht automatisch aktualisiert. Sie müssen diese Aktualisierung manuell vornehmen. Mit diesem Feld wird die Aktualität des Artikels angezeigt. |

### <a name="to-set-author-andor-msauthor"></a>Festlegen von „author“ und/oder „ms.author“

1. Navigieren Sie in VS Code zu **Datei** > **Einstellungen** > **Einstellungen**, oder drücken Sie <kbd>STRG+,</kbd>.
1. Wählen Sie **Benutzereinstellungen** aus, um die Einstellungen für sämtliche VS Code-Arbeitsbereiche zu ändern, oder **Arbeitsbereichseinstellungen**, um nur die Einstellungen für den aktuellen Arbeitsbereich zu ändern.
1. Suchen Sie links im Bereich „Standardeinstellungen“ die Option **Docs Article Templates-Erweiterungskonfiguration**, klicken Sie auf das Stiftsymbol neben der gewünschten Einstellung und dann auf „In Einstellungen ersetzen“.
1. Der Bereich **Benutzereinstellungen** wird mit einem neuen Eintrag am unteren Rand parallel angezeigt.
1. Fügen Sie Ihre GitHub-ID oder Ihren Microsoft-E-Mail-Alias hinzu, und speichern Sie die Datei.
1. Möglicherweise müssen Sie VS Code schließen und neu starten, damit die Änderungen wirksam werden.
1. Wenn Sie jetzt eine Vorlage anwenden, die dynamische Felder verwendet, wird Ihre GitHub-ID und/oder Ihr Microsoft-Alias im Metadatenheader automatisch eingetragen.

### <a name="to-make-a-new-template-available-in-vs-code"></a>Bereitstellen einer neuen Vorlage in VS Code

1. Entwerfen Sie Ihre Vorlage als Markdowndatei.
1. Senden Sie einen Pull Request für den Vorlagenordner des Repositorys [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates).

Das docs.microsoft.com-Team überprüft Ihre Vorlage und führt den PR zusammen, sofern die Richtlinien des docs.microsoft.com-Styleguides erfüllt sind. Nach der Zusammenführung steht die Vorlage allen Benutzern der Erweiterung „Docs Article Templates“ zur Verfügung.

## <a name="demo-several-features"></a>Demo zu mehreren Features

Es folgt ein kurzes Video, in dem die folgenden Features des Docs Authoring Pack veranschaulicht werden:

* **YAML-Dateien**
  * Unterstützung für „Docs: Link zu Datei im Repository“
* **Markdowndateien**
  * Kontextmenüoption zum Aktualisieren des Metadatenwerts „ms.date“
  * Unterstützung für automatische Vervollständigung von Code für Sprachen-IDs im Codefence
  * Unterstützung von Warnungen/automatischer Korrektur für nicht erkannte Sprachen-IDs im Codefence
  * Auswahl aufsteigend sortieren (A bis Z)
  * Auswahl absteigend sortieren (Z bis A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>Zu erwartende Zeit für Beiträge

Die Docs Authoring Pack-Erweiterung ist Open Source, und jeder Benutzer mit einem GitHub-Konto kann Beiträge dazu erstellen. Es gibt ein eigenes internes Microsoft-Team, das aktiv an diesem Projekt arbeitet. Dieses Team überwacht Probleme und Pull Requests. Die Vereinbarung zum Service Level (SLA) und die erwartete Zeit für die Überprüfung eines Pull Request beträgt derzeit eine Woche. Das Team ist derzeit um eine Automatisierung bemüht, um diesen Zeitraum zu verkürzen.

## <a name="next-steps"></a>Nächste Schritte

Lernen Sie die verschiedenen Features kennen, die im Docs Authoring Pack, einer Visual Studio Code-Erweiterung, verfügbar sind.

* [Vervollständigung von Entwicklungssprachen](docs-authoring/dev-lang-completion.md)
* [Bildkomprimierung](docs-authoring/image-compression.md)
* [Metadatenaktualisierungen](docs-authoring/metadata-updates.md)
* [Neuformatieren von Tabellen](docs-authoring/reformat-table.md)
* [Austausch typografischer Anführungszeichen](docs-authoring/smart-quote-replacement.md)
* [Sortieren von Umleitungen](docs-authoring/sort-redirects.md)
* [Sortierauswahl](docs-authoring/sort-selection.md)
