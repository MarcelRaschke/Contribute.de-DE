---
title: Markdownreferenz für docs.microsoft.com
description: Lernen Sie die in der Microsoft-Dokumentation-Plattform verwendeten Markdownfeatures und -syntax kennen.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 2a0595e03e145c560df701f3db8a43bbb76ef724
ms.sourcegitcommit: 48d9a16cd3854cdf3c8c492dab1675edcdfbbd7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103481186"
---
# <a name="docs-markdown-reference"></a>Docs Markdown-Referenz

In diesem Artikel werden die wichtigsten Konzepte zum Schreiben von Markdown für doc.microsoft.com (Docs) in alphabetischer Reihenfolge erläutert.

[Markdown](https://daringfireball.net/projects/markdown/) ist eine schlanke Markupsprache mit Nur-Text-Formatierungssyntax. Docs unterstützt ein kompatibles [CommonMark](https://commonmark.org/)-Markdown, das von der [Markdig](https://github.com/lunet-io/markdig)-Analyse-Engine analysiert wird. Docs unterstützt auch benutzerdefinierte Markdownerweiterungen, die umfangreicheren Inhalt auf der Docs-Website bereitstellen.

Sie können Markdown in einem beliebigen Text-Editor schreiben, es wird jedoch empfohlen, [Visual Studio Code](https://code.visualstudio.com/) mit dem [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) zu verwenden. Das Docs Authoring Pack bietet Bearbeitungstools und Vorschaufunktionen, mit denen Sie sehen können, wie Ihre Artikel beim Rendern auf Docs aussehen werden.

## <a name="alerts-note-tip-important-caution-warning"></a>Warnungen (Hinweis, Tipp, Wichtig, Achtung, Warnung)

Warnungen sind eine Markdownerweiterung zum Erstellen von Blockzitaten, die auf docs.microsoft.com mit Farben und Symbolen gerendert werden, die die Bedeutung des Inhalts anzeigen. Die folgenden Warnungstypen werden unterstützt:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Gefährliche Folgen einer Aktion.

### <a name="angle-brackets"></a>Geschweifte Klammern

Wenn Sie in Ihrer Datei spitze Klammern im Text verwenden, z. B. zur Bezeichnung eines Platzhalters, müssen Sie die spitzen Klammern manuell codieren. Andernfalls interpretiert Markdown sie als HTML-Tag.

Codieren Sie `<script name>` z. B. als `&lt;script name&gt;` oder `\<script name>`.

Spitze Klammern müssen in Text, der als Inlinecode oder in Codeblöcken formatiert ist, nicht mit einem Escapezeichen versehen werden.

## <a name="apostrophes-and-quotation-marks"></a>Apostrophe und Anführungszeichen

Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten. Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden. Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ&euro;&trade;s.

Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:

- Linkes (öffnendes) Anführungszeichen: `&#8220;`
- Rechtes (schließendes) Anführungszeichen: `&#8221;`
- Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`
- Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`

## <a name="blockquotes"></a>Blockquotes

Blockzitate werden mit dem `>`-Zeichen generiert:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

Das vorherige Beispiel wird wie folgt gerendert:

> Dies ist ein Blockzitat. Es wird normalerweise eingerückt und mit einer anderen Hintergrundfarbe gerendert.

## <a name="bold-and-italic-text"></a>Fetter und kursiver Text

Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:

```markdown
This text is **bold**.
```

Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:

```markdown
This text is *italic*.
```

Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Codeausschnitte

Docs Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „umgrenzter“ Block zwischen Sätzen. Weitere Informationen finden Sie unter [Hinzufügen von Code zu Dokumenten](code-in-docs.md).

## <a name="columns"></a>Spalten

Die Markdownerweiterung **columns** ermöglicht es Dokumentationsautoren, spaltenbasierte Inhaltslayouts hinzuzufügen, die flexibler und leistungsfähiger als einfache Markdowntabellen sind, die sich nur für echte Tabellendaten eignen. Sie können bis zu vier Spalten hinzufügen und das optionale Attribut `span` verwenden, um zwei oder mehr Spalten zusammenzuführen.

Die Syntax für Spalten sieht wie folgt aus:

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

Spalten sollten nur einfaches Markdown, einschließlich Bildern, enthalten. Überschriften, Tabellen, Registerkarten und andere komplexe Strukturen sollten nicht eingeschlossen werden. Eine Zeile darf keinen Inhalt außerhalb der Spalte enthalten.

Beispielsweise erstellt das folgende Markdown eine Spalte, die zwei Spaltenbreiten umfasst, sowie eine Standardspalte (ohne `span`):

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

Dies wird wie folgt gerendert:

:::row:::
   :::column span="2":::
      **Spalte mit doppelter Spaltenbreite und viel Text**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **Spalte mit einfacher Spaltenbreite und einem Bild**

      ![Dok.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>Überschriften

Microsoft-Dokumentation unterstützt sechs Markdownüberschriftenebenen:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Zwischen dem letzten `#` und dem Überschriftentext muss ein Leerzeichen stehen.
- Jede Markdowndatei darf lediglich eine H1-Überschrift aufweisen.
- Die H1-Überschrift muss nach dem YML-Metadatenblock der erste Inhalt in der Datei sein.
- H2-Überschriften werden automatisch rechts in einem Navigationsmenü der veröffentlichten Datei angezeigt. Überschriften auf niedrigeren Ebenen werden nicht angezeigt. Verwenden Sie H2s an sinnvollen Stellen, damit Leser gut durch Ihre Artikel navigieren können.
- HTML-Überschriften, wie z. B. `<h1>`, werden nicht empfohlen und führen in einigen Fällen zu Buildwarnungen.
- Über [Lesezeichenlinks](how-to-write-links.md#explicit-anchor-links) können Sie Links zu einzelnen Überschriften einer Datei einfügen.

## <a name="html"></a>HTML

Markdown unterstützt zwar Inline-HTML, aber HTML wird für die Veröffentlichung auf Docs nicht empfohlen. HTML führt zu Buildfehlern oder -warnungen (einige Werte sind davon ausgenommen).

## <a name="images"></a>Bilder

Die folgenden Dateitypen werden standardmäßig für Bilder unterstützt:

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>Standarddarstellung von Bildern (standardmäßiges Markdown)

Die grundlegende Markdownsyntax zum Einbetten eines Bilds sieht wie folgt aus:

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`<alt text>` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild. Für visuell eingeschränkte Menschen ist Alternativtext erforderlich. Dieser Text ist zudem nützlich bei einem Seitenladefehler, durch den ein Bild nicht gerendert wird.

Unterstriche in Alternativtext werden nicht korrekt gerendert, es sei denn, Sie stellen ihnen einen umgekehrten Schrägstrich (`\_`) als Escapezeichen voran. Kopieren Sie jedoch keine Dateinamen zur Verwendung als Alternativtext. Schreiben Sie beispielsweise nicht Folgendes:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Schreiben Sie stattdessen Folgendes:

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Standarddarstellung von Bildern (Docs Markdown)

Die benutzerdefinierte Docs-Erweiterung `:::image:::`unterstützt Standardbilder, komplexe Bilder und Symbole.

Bei Standardbildern funktioniert die ältere Markdownsyntax weiterhin, doch wird die neue Erweiterung empfohlen, da sie leistungsfähigere Funktionen unterstützt, wie z. B. das Angeben eines Lokalisierungsbereichs, der sich vom übergeordneten Thema unterscheidet. Weitere erweiterte Funktionen, z. B. das Auswählen aus der Shared Image Gallery statt Angabe eines lokalen Bilds, werden in Zukunft verfügbar sein. Die neue Syntax sieht wie folgt aus:

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

Wenn `type="content"` (Standard), sind sowohl `source` als auch `alt-text` erforderlich.

### <a name="complex-images-with-long-descriptions"></a>Komplexe Bilder mit langen Beschreibungen

Sie können diese Erweiterung auch zum Hinzufügen eines Bilds mit einer langen Beschreibung verwenden, die von Sprachausgaben gelesen, aber nicht visuell auf der veröffentlichten Seite gerendert wird. Lange Beschreibungen sind eine Anforderung hinsichtlich der Barrierefreiheit bei komplexen Bildern, z. B. Diagrammen. Die Syntax sieht wie folgt aus:

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

Wenn `type="complex"`, sind `source`, `alt-text`, eine lange Beschreibung und das `:::image-end:::`-Tag erforderlich.

### <a name="specifying-loc-scope"></a>Festlegen des Lokalisierungsbereichs

Manchmal unterscheidet sich der Lokalisierungsbereich eines Bilds von dem des Artikels oder Moduls, in dem es enthalten ist. Dies kann zu einer falschen globalen Darstellung führen, wenn z. B. der Screenshot eines Produkts versehentlich in eine Sprache lokalisiert wird, in der das Produkt nicht verfügbar ist. Um das zu verhindern, können Sie das optionale Attribut `loc-scope` in Bildern vom Typ `content` und `complex` angeben.

### <a name="icons"></a>Symbole

Die Bilderweiterung unterstützt Symbole, bei denen es sich um dekorative Bilder handelt und die keinen Alternativtext aufweisen sollten. Die Syntax für Symbole sieht wie folgt aus:

```Markdown
:::image type="icon" source="<folderPath>":::
```

Wenn `type="icon"`, sollte nur `source` angegeben werden.

## <a name="included-markdown-files"></a>Einbezogene Markdowndateien

Wenn Markdowndateien in mehreren Artikeln wiederholt werden müssen, können Sie eine Includedatei verwenden. Die Einbeziehungsfunktion weist Docs an, den Verweis zum Zeitpunkt der Erstellung durch den Inhalt der Includedatei zu ersetzen. Sie können Einbeziehungen auf folgende Arten verwenden:

- Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines Satzes wieder.
- Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.

Inline- oder Blockincludedateien sind Markdowndateien (.md). Sie können jeglichen gültigen Markdowncode enthalten. Includedateien befinden sich normalerweise in einem allgemeinen Unterverzeichnis *includes* im Stammverzeichnis des Repositorys. Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.

### <a name="includes-syntax"></a>Einbeziehungssyntax

Blockeinbeziehungen befinden sich in einer eigenen Zeile:

```markdown
[!INCLUDE [<title>](<filepath>)]
```

Inlineeinbeziehungen befinden sich innerhalb einer Zeile:

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

Dabei ist `<title>` der Name der Datei, und `<filepath>` ist der relative Pfad zur Datei. `INCLUDE` muss groß geschrieben werden, und es muss ein Leerzeichen vor `<title>` vorhanden sein.

Die Anforderungen und Überlegungen zu Includedateien lauten wie folgt:

- Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt. Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.
- Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Docs-Erweiterungen abhängig sind. Sie werden erst nach der Veröffentlichung gerendert.
- Stellen Sie sicher, dass sämtlicher Text in einer Includedatei in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Includedatei verweist, abhängig sind. Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt.
- Betten Sie keine Includedateien in andere Includedateien ein.
- Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z. B. der Ordner `<repo>` */includes/media*). Der Stamm des *media*-Verzeichnisses darf keine Bilder enthalten. Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes *media*-Verzeichnis erforderlich.
- Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei. Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel. Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.
- Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.  Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.

## <a name="links"></a>Links

Weitere Informationen zur Syntax von Links finden Sie unter [Verwenden von Links in der Dokumentation](how-to-write-links.md).

## <a name="lists-numbered-bulleted-checklist"></a>Listen (Nummeriert, Aufzählungszeichen, Checkliste)

### <a name="numbered-list"></a>Nummerierte Liste

Zum Erstellen einer nummerierten Liste können Sie für alle Punkte Einsen verwenden. Die Zahlen werden bei der Veröffentlichung in aufsteigender Reihenfolge als sequenzielle Liste gerendert. Für eine bessere Lesbarkeit der Quelle können Sie Ihre Listen manuell inkrementieren.

Verwenden Sie keine Buchstaben für Listen, auch nicht für geschachtelte Listen. Diese werden bei der Veröffentlichung auf Docs nicht fehlerfrei gerendert. Geschachtelte nummerierte Listen werden mit Kleinbuchstaben gerendert, wenn sie veröffentlicht werden. Beispiel:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Dies wird wie folgt gerendert:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>Liste mit Aufzählungszeichen

Verwenden Sie für eine Liste mit Aufzählungszeichen `-` oder `*` gefolgt von einem Leerzeichen am Anfang jeder Zeile:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Dies wird wie folgt gerendert:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

Unabhängig davon, welche Syntax Sie verwenden (`-` oder `*`), verwenden Sie diese jeweils konsistent innerhalb eines Artikels.

### <a name="checklist"></a>Checkliste

Checklisten können auf Docs mit einer benutzerdefinierten Markdownerweiterung verwendet werden:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Dieses Beispiel wird auf Docs folgendermaßen gerendert:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Verwenden Sie Checklisten am Anfang oder Ende eines Artikels, um zusammenzufassen, was der Leser lernen wird bzw. gelernt hat. Fügen Sie keine sinnlosen Checklisten in der Mitte des Artikels ein.

## <a name="next-step-action"></a>Aktion „Nächste Schritte“

Sie können eine benutzerdefinierte Erweiterung verwenden, um eine Schaltfläche für weitere Schritte hinzuzufügen.

Die Syntax ist wie folgt:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Beispiel:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Dies wird wie folgt gerendert:

> [!div class="nextstepaction"]
> [Informationen zum Hinzufügen von Code zu Artikeln](code-in-docs.md)

Sie können für nächste Schritte jede unterstützte Linkart verwenden, auch einen Markdownlink zu einer anderen Webseite. In den meisten Fällen ist der Link für die nächsten Schritte ein relativer Link zu einer anderen Datei im gleichen Docset.

## <a name="non-localized-strings"></a>Nicht lokalisierte Zeichenfolgen

Sie können die benutzerdefinierte Markdownerweiterung `no-loc` verwenden, um Inhaltszeichenfolgen anzugeben, die beim Lokalisierungsprozess ignoriert werden sollen.

Bei allen angegebenen Zeichenfolgen wird die Groß-/Kleinschreibung beachtet. Das heißt, die Zeichenfolge muss genau übereinstimmen, um bei der Lokalisierung ignoriert zu werden.

Verwenden Sie die folgende Syntax, um eine einzelne Zeichenfolge als nicht lokalisierbar zu markieren:

```markdown
:::no-loc text="String":::
```

Im folgenden Beispiel wird nur die einzelne Instanz von `Document` während des Lokalisierungsprozesses ignoriert:

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> Verwenden Sie `\`, um Sonderzeichen mit Escapezeichen zu versehen:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

Sie können auch Metadaten im YAML-Header verwenden, um alle Instanzen einer Zeichenfolge innerhalb der aktuellen Markdowndatei als nicht lokalisierbar zu markieren:

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> Die „no-loc“-Metadaten werden in der Datei *docfx.json* nicht als globale Metadaten unterstützt. Die Lokalisierungspipeline liest die Datei *docfx.json* nicht, sodass die „no-loc“-Metadaten in jeder einzelnen Quelldatei hinzugefügt werden müssen.

Im folgenden Beispiel werden sowohl in `title` der Metadaten als auch im Markdownheader das Wort `Document` während des Lokalisierungsprozesses ignoriert.

In `description` der Metadaten und im Markdownhauptinhalt wird das Wort `document` lokalisiert, da es nicht mit dem Großbuchstaben `D` beginnt.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>Selektoren

Selektoren sind Elemente der Benutzeroberfläche, mit denen der Benutzer zwischen mehreren Varianten desselben Artikels wechseln kann. Sie werden in einigen Docsets verwendet, um unterschiedlichen Implementierungen bei verschiedenen Technologien oder Plattformen zu entsprechen. Selektoren sind in der Regel besonders für unsere Inhalte für mobile Plattformen geeignet, die sich an Entwickler richten.

Da derselbe Markdownselektor in jeder Artikeldatei enthalten ist, die diesen Selektor verwendet, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Includedatei platzieren. Dann können Sie auf diese Includedatei in allen Artikeldateien, die denselben Selektor verwenden, verweisen.

Es gibt zwei Selektortypen: einen einfachen und einen Mehrfachselektor.

### <a name="single-selector"></a>Einfache Auswahl

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

Dieser Code wird wie folgt gerendert:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Mehrfachauswahl

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

Dieser Code wird wie folgt gerendert:

> [!div class="op_multi_selector" title1="Plattform" title2="Back-End"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | JavaScript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | JavaScript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | JavaScript)](how-to-write-links.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-links.md)
> - [(Xamarin Android | JavaScript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>Tiefgestellt und Hochgestellt

Sie sollten tief- und hochgestelle Zeichen nur verwenden, wenn dies aus Gründen der technischen Genauigkeit erforderlich ist, z. B. beim Schreiben mathematischer Formeln. Verwenden Sie diesen Zeichentyp nicht für nicht standardmäßige Stile, wie z. B. Fußnoten.

Verwenden Sie sowohl für tiefgestellte als auch hochgestellte Zeichen HTML:

```html
Hello <sub>This is subscript!</sub>
```

Dies wird wie folgt gerendert:

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Dies wird wie folgt gerendert:

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Tabellen

Die einfachste Möglichkeit zum Erstellen einer Tabelle in Markdown ist die Verwendung von senkrechten Strichen und Unterstrichen. Fügen Sie unter der ersten Zeile Unterstriche ein, um eine Standardtabelle mit Kopfzeile zu erstellen:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Dies wird wie folgt gerendert:

|This is   |a simple   |table header|
|----------|-----------|------------|
|Tisch     |data       |hier        |
|it doesn't|actually   |have to line up nicely!|

Sie können die Spalten mithilfe von Doppelpunkten ausrichten:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Dieser Code wird folgendermaßen gerendert:

| Fun                  | With                 | Tabellen          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| 10 USD                  | 10 USD                  | 10 USD             |
| $1                   | $1                   | $1              |

> [!TIP]
> Mit der Erweiterung „Docs Authoring Pack“ für VS Code können Sie einfache Tabellen unkompliziert hinzufügen.
>
> Sie können auch den [Tables Generator](http://www.tablesgenerator.com/markdown_tables) verwenden.

### <a name="line-breaks-within-words-in-any-table-cell"></a>Zeilenumbrüche innerhalb von Wörtern in einer Tabellenzelle

Lange Wörter in einer Markdowntabelle können dazu führen, dass die Tabelle in den rechten Navigationsbereich hineinreicht und nicht mehr lesbar ist. Sie können dieses Problem lösen, indem Sie beim Rendern auf Docs zulassen, dass bei Bedarf automatisch Zeilenumbrüche in Wörter eingefügt werden. Dafür müssen Sie die Tabelle nur mit der benutzerdefinierten Klasse `[!div class="mx-tdBreakAll"]` umschließen.

Im Folgenden finden Sie ein Markdownbeispiel einer Tabelle mit drei Zeilen, die von einem `div`-Element mit dem Klassennamen `mx-tdBreakAll` umschlossen wird.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Dieser Code wird wie folgt gerendert:

> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Erforderlich für die unbeaufsichtigte Installation?|Beschreibung|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Ja|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Unterdrückt alle Neustartversuche. Standardmäßig wird vor dem Neustart auf der Benutzeroberfläche eine Eingabeaufforderung angezeigt.|
> |Hilfe|/help|Nein|Stellt Hilfe und eine Kurzübersicht bereit. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Zeilenumbrüche innerhalb von Wörtern in Tabellenzellen der zweiten Spalte

Möglicherweise möchten Sie, dass Zeilenumbrüche innerhalb von Wörtern nur in der zweiten Spalte einer Tabelle automatisch eingefügt werden. Um Zeilenumbrüche auf die zweite Spalte zu beschränken, wenden Sie die Klasse `mx-tdCol2BreakAll` wie oben gezeigt mithilfe der `div`-Wrappersyntax an.

### <a name="data-matrix-tables"></a>Datenmatrixtabellen

Eine Datenmatrixtabelle weist sowohl einen Header als auch eine gewichtete erste Spalte auf, sodass eine Matrix mit einer leeren Zelle in der oberen linken Ecke erstellt wird. Die Dokumente enthalten benutzerdefiniertes Markdown für Datenmatrixtabellen:

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

In der ersten Spalte muss jeder Eintrag fett formatiert sein (`**bold**`). Andernfalls sind die Tabellen für die Sprachausgabe nicht zugänglich und für Dokumente ungültig.

### <a name="html-tables"></a>HTML-Tabellen

HTML-Tabellen werden für docs.microsoft.com nicht empfohlen. Sie können in der Quelle nicht von Menschen gelesen werden, was jedoch ein wichtiges Merkmal von Markdown ist.
