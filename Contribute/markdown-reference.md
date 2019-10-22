---
title: Markdownreferenz für docs.microsoft.com
description: Lernen Sie die in der Microsoft-Dokumentation-Plattform verwendeten Markdownfeatures und -syntax kennen.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 3142b1aee8cadb69f82bfbcd3f89c701fac5b356
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288308"
---
# <a name="markdown-reference"></a>Markdownreferenz

Markdown ist eine schlanke Markupsprache mit Nur-Text-Formatierungssyntax. Die Dokumentationsplattform unterstützt den CommonMark-Standard für Markdown sowie einige Markdownerweiterungen, die umfangreicheren Inhalt auf docs.microsoft.com bereitstellen können. In diesem Artikel werden die wichtigsten Konzepte bezüglich Markdown für doc.microsoft.com in alphabetischer Reihenfolge erläutert.

Sie können Markdown in einem beliebigen Text-Editor schreiben. Wenn Sie einen Editor verwenden möchten, der das Einfügen von Markdownstandardsyntax und von benutzerdefinierten Dokumentationserweiterungen unterstützt, wird [VS Code](https://code.visualstudio.com/) mit installiertem [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) empfohlen.

Microsoft-Dokumentation nutzt die Markdown-Engine von Markdig. Unter [https://babelmark.github.io/](https://babelmark.github.io/) können Sie das Rendern von Markdown in Markdig und mit anderen Engines testen.

## <a name="alerts-note-tip-important-caution-warning"></a>Warnungen (Hinweis, Tipp, Wichtig, Achtung, Warnung)

Damit wird eine Markdownerweiterungen für Microsoft-Dokumentation angewiesen, Blockzitate zu erzeugen, die auf docs.microsoft.com mit anderen Hintergrundfarben und Symbolen gerendert werden, die den Inhalt hervorheben. Die folgenden Warnungstypen werden unterstützt:

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
> Dangerous certain consequences of an action.

## <a name="code-snippets"></a>Codeausschnitte

Sie können Codeausschnitte in Ihre Markdowndatei einbetten:

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Überschriften

Microsoft-Dokumentation unterstützt sechs Markdownüberschriftenebenen:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Zwischen dem letzten `#` und dem Überschriftentext muss ein Leerzeichen stehen.
- Jede Markdowndatei darf lediglich eine H1 aufweisen.
- Die H1 muss nach dem YML-Metadatenblock der erste Inhalt in der Datei sein.
- H2s werden automatisch rechts in einem Navigationsmenü der veröffentlichten Datei angezeigt. Dies gilt nicht für Überschriften auf niedrigeren Ebenen. Verwenden Sie H2s an sinnvollen Stellen, damit Leser gut durch Ihre Artikel navigieren können.
- HTML-Überschriften, wie z.B. `<h1>`, werden nicht empfohlen und führen in einigen Fällen zu Buildwarnungen.
- Über [Lesezeichenlinks](#bookmark-links) können Sie Links zu einzelnen Überschriften einer Datei einfügen.

## <a name="html"></a>HTML

Markdown unterstützt zwar Inline-HTML, aber HTML wird für die Veröffentlichung auf Microsoft-Dokumentation nicht empfohlen. HTML führt zu Buildfehlern oder -warnungen (einige Werte sind davon ausgenommen).

## <a name="images"></a>Bilder

Verwenden Sie zum Einbetten eines Bilds die folgende Syntax:

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`alt text` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild. Für visuell eingeschränkte Menschen ist Alternativtext erforderlich. Dieser Text ist zudem nützlich bei einem Seitenladefehler, durch den ein Bild nicht gerendert wird.

Bilder sollten in einem `/media`-Ordner in Ihrem Docset gespeichert werden. Die folgenden Dateitypen werden standardmäßig für Bilder unterstützt:

- .jpg
- .png

Andere Bildtypen werden unterstützt, wenn Sie diese als Ressourcen zur „docfx.json“-Datei<!--add link to reference when available--> für Ihr Docset hinzufügen.

## <a name="links"></a>Links

In den meisten Fällen verwendet Microsoft-Dokumentation Standardmarkdownlinks zu anderen Dateien und Seiten. Die Linktypen werden weiter unten erläutert.

> [!TIP]
> Mit dem Docs Authoring Pack für VS Code können Sie relative Links und Lesezeichenlinks problemlos einfügen, ohne sich um den Pfad Gedanken machen zu müssen.

> [!IMPORTANT]
> Beziehen Sie in die Links zu Microsoft-Seiten keine Gebietsschemacodes ein (z.B. „de-de“). Hartcodierte Gebietsschemacodes verhindern, dass lokalisierter Inhalt gerendert wird. So wird die Benutzung für Leser in anderen Gebietsschemas erschwert und führt zu hohen Lokalisierungskosten. Wenn Sie eine URL aus dem Browser kopieren, wird der Gebietsschemacode standardmäßig mit kopiert. Deshalb müssen Sie diesen manuell löschen, wenn Sie einen Link erstellen. Verwenden Sie z.B. Folgendes:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Und nicht:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Relative Links im gleichen Docset

Ein relativer Pfad ist ein Pfad zu einer Zieldatei, der in einem relativen Verhältnis zur aktuellen Datei steht. Auf Microsoft-Dokumentation können Sie einen relativen Pfad verwenden, um einen Link zu einer anderen Datei im gleichen Docset einzufügen. Die Syntax für einen relativen Pfad sieht wie folgt aus:

```markdown
[link text](../../folder/filename.md)
```

`../` gibt eine höhere Ebene in der Hierarchie an.

- Der relative Pfad wird während des Builds aufgelöst. Auch die Erweiterung „.md“ wird entfernt.
- Sie können „../“ verwenden, um einen Link zu einer Datei im übergeordneten Ordner zu erstellen. Diese Datei muss sich allerdings im gleichen Docset befinden. Sie können „../“ nicht zum Erstellen eines Links zu einer Datei in einem anderen Docset verwenden.
- Microsoft-Dokumentation unterstützt zudem eine Sonderform von relativen Pfaden, die mit „~“ beginnt (z.B. ~/foo/bar.md). Diese Syntax gibt eine Datei an, die abhängig vom Stammordner eines Docsets ist. Diese Art von Pfad wird ebenfalls während des Erstellungsvorgangs überprüft und aufgelöst.

> [!IMPORTANT]
> Beziehen Sie die Erweiterung mit in den relativen Pfad ein. Der Build prüft das Vorhandensein der Zieldatei dieses relativen Pfads. Wenn der relative Pfad keine Erweiterung enthält, ist es wahrscheinlich, dass der Build einen fehlerhaften Link meldet. Verwenden Sie z.B. Folgendes:
>
> `[link text](../../folder/filename.md)`
>
> Und nicht:
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Links relativ zur Website zu anderen Dateien auf Microsoft-Dokumentation

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Beziehen Sie nicht die Erweiterung (.md) ein. Dadurch wird ein Link zur Linux-Übersichtsdatei außerhalb des Docsets mit Azure-Artikeln erstellt.

### <a name="links-to-external-sites"></a>Links zu externen Websites

```markdown
[Microsoft](https://www.microsoft.com)
```

Ein URL-basierter Link zu einer anderen Webseite (muss „https://“ enthalten).

### <a name="bookmark-links"></a>Lesezeichenlinks

Lesezeichenlink zu Überschriften in einer anderen Datei im gleichen Repository. Beispiel:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Lesezeichenlink zu einer Überschrift in der aktuellen Datei:

```markdown
[Managed Disks](#managed-disks)
```

Verwenden Sie ein Rautenzeichen (`#`) gefolgt von der Überschrift. So ändern Sie den Text der Überschrift in Linktext:
- Verwenden Sie nur Kleinbuchstaben.
- Entfernen Sie alle Satzzeichen.
- Ersetzen Sie Leerzeichen durch Bindestriche.

Wenn die Überschrift beispielsweise „2.2 Security concerns“ lautet, entspricht der Linktext des Lesezeichens „#22-security-concerns“.

### <a name="explicit-anchor-links"></a>Explizite Ankerlinks

Explizite Ankerlinks mit dem HTML-Tag `<a>` **sind nicht erforderlich und werden nicht empfohlen** (Ausnahmen: im Hub und auf der Landing Page). Verwenden Sie Lesezeichenlinks wie oben beschrieben in allgemeinen Markdowndateien. Verwenden Sie für den Hub und die Landing Page Anker. Orientieren Sie sich dafür an folgendem Format:

`## <a id="AnchorText"> </a>Header text` oder `## <a name="AnchorText"> </a>Header text`

Verwenden Sie die folgende Syntax, um Links zu expliziten Ankern herzustellen:

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Xref-Links

Verwenden Sie Xref-Links mit einer eindeutigen ID (UID), um automatisch generierte Links zu API-Referenzen im aktuellen Docset oder in anderen Docsets hinzuzufügen.

> [!NOTE]
> Fügen Sie die Konfiguration `xrefService` in der Datei `docfx.json` hinzu, um auf API-Referenzseiten in anderen Docsets zu verweisen.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

Die UID entspricht dem vollqualifizierten Klassen- und Membernamen. Wenn Sie ein Sternchen (*) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API. Verwenden Sie z.B. `List<T>.BinarySearch*`, um einen Link zur Seite der BinarySearch-Methode statt einen Link zu einer bestimmten Überladung wie `List<T>.BinarySearch(T, IComparer<T>)` hinzuzufügen.

Sie können eine der folgenden Syntaxvarianten auswählen:

- Automatischer Link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  Der optionale Abfrageparameter `displayProperty` erzeugt einen vollqualifizierten Linktext. Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.

- Markdownlink: `[link text](xref:UID)`
  
  Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.

Beispiele:

- `<xref:System.String>` wird als „String“ gerendert.
- `<xref:System.String?displayProperty=nameWithType>` wird als „System.String“ gerendert.
- `[String class](xref:System.String)` wird als „String class“ gerendert.

Im Moment gibt es keine einfache Möglichkeit, die UIDs zu suchen. <!-- ? -->Die beste Möglichkeit, die UID für eine API zu suchen, ist die Anzeige der Quelle für die API-Seite, zu der Sie eine Verknüpfung herstellen möchten, und den Wert „ms.assetid“ zu suchen. Einzelne Überladungswerte werden in der Quelle nicht angezeigt. Wir erarbeiten ein besseres System für die Zukunft.

Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert als `%60`, `%23` und `%2A` im HTML-Format codiert werden. Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.

Beispiele:

- System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor wird `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Listen (Nummeriert, Aufzählungszeichen, Checkliste)

### <a name="numbered-list"></a>Nummerierte Liste

Für eine nummerierte Liste können Sie für alle Punkte Einsen verwenden. Diese werden bei der Veröffentlichung als aufsteigende Zahlenfolge gerendert. Für eine bessere Lesbarkeit der Quelle können Sie Ihre Listen inkrementieren.

Verwenden Sie keine Buchstaben für Listen, auch nicht für geschachtelte Listen. Diese werden nicht fehlerfrei gerendert, wenn sie auf der Seite von Microsoft-Dokumentation veröffentlicht werden. Geschachtelte nummerierte Listen werden mit Kleinbuchstaben gerendert, wenn sie veröffentlicht werden. Beispiel:

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

Verwenden Sie für eine Liste mit Aufzählungszeichen `-` gefolgt von einem Leerzeichen am Anfang jeder Zeile:

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

### <a name="checklist"></a>Checkliste

Checklisten können (nur) auf docs.microsoft.com mit einer benutzerdefinierten Markdownerweiterung verwendet werden:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Dieses Beispiel wird auf docs.microsoft.com folgendermaßen gerendert:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Verwenden Sie Checklisten am Anfang oder Ende eines Artikels, um zusammenzufassen, was der Leser lernen wird bzw. gelernt hat. Fügen Sie keine sinnlosen Checklisten in der Mitte des Artikels ein.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Aktion „Nächste Schritte“

Sie können eine benutzerdefinierte Erweiterung verwenden, um eine Schaltfläche für weitere Schritte hinzuzufügen (nur auf docs.microsoft.com).

Die Syntax sieht wie folgt aus:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Beispiel:

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Dies wird wie folgt gerendert:

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

Sie können für nächste Schritte jede unterstützte Linkart verwenden, auch einen Markdownlink zu einer anderen Webseite. In den meisten Fällen ist der Link für die nächsten Schritte ein relativer Link zu einer anderen Datei im gleichen Docset.

## <a name="section-definition"></a>Definition von Abschnitten

<!-- more info about this would be helpful! -->
Gelegentlich müssen Sie Abschnitte definieren. Diese Syntax wird in den meisten Fällen für Codetabellen verwendet.
Sehen Sie sich folgendes Beispiel an:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Dieser blockquote-Markdowntext wird folgendermaßen gerendert:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Selektoren

<!-- could be more clear! -->
Sie können einen Selektor verwenden, wenn Sie für denselben Artikel verschiedene Seiten verbinden möchten. Dann können die Leser zwischen diesen Seiten wechseln.

> [!NOTE]
> Diese Erweiterung funktioniert in docs.microsoft.com und MSDN unterschiedlich. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Einfache Auswahl

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

Dieser Code wird wie folgt gerendert:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Mehrfachauswahl

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

Dieser Code wird wie folgt gerendert:

> [!div class="op_multi_selector" title1="Plattform" title2="Back-End"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | JavaScript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | JavaScript)](how-to-write-workflows-major.md)

## <a name="tables"></a>Tables

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
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

Sie können eine Tabelle auch ohne Kopfzeile erstellen. Mit folgendem Code können Sie z.B. eine Liste mit mehreren Spalten erstellen:

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

Dieser Code wird folgendermaßen gerendert:

|   |   |
| - | - |
| This | table |
| has no | header |

Sie können die Spalten mithilfe von Doppelpunkten ausrichten:

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Dieser Code wird folgendermaßen gerendert:

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> Mit der Erweiterung „Docs Authoring Pack“ für VS Code können Sie einfache Tabellen unkompliziert hinzufügen.
>
> Sie können auch den [Tables Generator](http://www.tablesgenerator.com/markdown_tables) verwenden.

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Das funktioniert nur auf docs.microsoft.com.

Wenn Sie eine Tabelle in Markdown erstellen, kann diese in den rechten Navigationsbereich hineinreichen und damit nicht lesbar sein. Dieses Problem lässt sich lösen, indem Sie bei der Dokumentausgabe zulassen, dass Tabellen bei Bedarf umbrochen werden. Dafür müssen Sie die Tabelle nur mit der benutzerdefinierten Klasse `[!div class="mx-tdBreakAll"]` umschließen.

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
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Das funktioniert nur auf docs.microsoft.com.

Von Zeit zu Zeit enthält die zweite Spalte einer Tabelle sehr lange Wörter. Um sicherzustellen, dass lange Wörter sinnvoll unterteilt werden, können Sie die Klasse `mx-tdCol2BreakAll` wie oben gezeigt mithilfe der `div`-Wrappersyntax anwenden.

### <a name="html-tables"></a>HTML-Tabellen

HTML-Tabellen werden für docs.microsoft.com nicht empfohlen. Sie können in der Quelle nicht von Menschen gelesen werden, was jedoch ein wichtiges Merkmal von Markdown ist.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Videos

### <a name="embedding-videos-into-a-markdown-page"></a>Einbetten von Videos in eine Markdownseite

Momentan unterstützt Microsoft-Dokumentation Videos, die auf einer der folgenden Plattformen veröffentlicht wurden:

- YouTube
- Channel 9
- OnePlayer von Microsoft

Sie können mit der folgenden Syntax ein Video einbetten, das von Microsoft-Dokumentation gerendert wird.

```markdown
> [!VIDEO <embedded_video_link>]
```

Beispiel:

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

Dieser Code wird folgendermaßen gerendert:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

Auf veröffentlichten Seiten wird er wie folgt angezeigt:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> Die URL für ein CH9-Video muss mit `https` beginnen und mit `/player` enden. Andernfalls wird nicht nur das Video, sondern die gesamte Seite eingebettet.

### <a name="uploading-new-videos"></a>Hochladen neuer Videos

Es wird empfohlen, neue Videos folgendermaßen hochzuladen:

1. Treten Sie der Gruppe **docs_video_users** auf IDWEB bei.
1. Navigieren Sie zu https://aka.ms/VideoUploadRequest, und machen Sie Angaben zu Ihrem Video. Sie müssen Folgendes angeben (diese Informationen werden später nicht öffentlich verfügbar sein):
    1. Einen Videotitel.
    1. Eine Liste der Produkte/Dienste, mit denen Ihr Video in Zusammenhang steht.
    1. Die Zielseite oder das Zieldocset (wenn Sie noch keine Seite haben), wo Ihr Video gehostet werden soll.
    1. Einen Link zur MP4-Datei des Videos (wenn Sie nicht wissen, wo Sie die Datei speichern sollen, können Sie sie vorübergehend hier speichern: `\\scratch2\scratch\apex`). MP4-Dateien sollten mindestens eine Auflösung von 720p haben.
    1. Eine Beschreibung des Videos.
1. Übermitteln (speichern) Sie die Aufgabe.
1. Das Video wird innerhalb von zwei Werktagen hochgeladen. Der Link, den Sie zur Einbettung benötigen, wird im Arbeitselement platziert. Dann wird das Arbeitselement *wieder Ihnen zugewiesen*.
1. Sie können das Arbeitselement schließen, sobald Sie den Link kopiert haben.
1. Der Videolink kann dann mit der folgenden Syntax in Ihrem Beitrag eingefügt werden:

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
