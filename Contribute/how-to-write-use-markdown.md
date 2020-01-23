---
title: Verwenden von Markdown für das Schreiben von Dokumentationsartikeln
description: Dieser Artikel enthält grundlegende Informationen und Verweise zu Markdown, das als Sprache zum Schreiben von docs.microsoft.com-Artikeln verwendet wird.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111069"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Verwenden von Markdown für das Schreiben von Dokumentationsartikeln

Artikel auf [docs.microsoft.com](https://docs.microsoft.com) sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist. Darum ist sie schnell zu einem Branchenstandard geworden. Die „docs.microsoft.com“-Website verwendet die [Markdig-Variante](#markdown-flavor) von Markdown.


## <a name="markdown-basics"></a>Grundlegendes zu Markdown

### <a name="headings"></a>Überschriften

Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Überschriften sollten im ATX-Format verfasst werden. Verwenden Sie also 1–6 Rautezeichen (#) am Anfang der Zeile, um eine Überschrift zu kennzeichnen. Diese entsprechen den HTML-Überschriftenebenen H1 bis H6. Oben sehen Sie Beispiele für Überschriften von der ersten bis zur vierten Ebene.

Es darf **nur eine** Überschrift auf der ersten Ebene (H1) in Ihrem Artikel geben. Diese wird als Titel der Seite verwendet.

Wenn Ihre Überschrift auf `#` endet, müssen Sie ein weiteres `#`-Zeichen hinzufügen, damit der Titel ordnungsgemäß gerendert wird. Beispiel: `# Async Programming in F# #`.

Überschriften auf der zweiten Ebene generieren das Inhaltsverzeichnis auf der Seite, das unter „In diesem Artikel“ neben dem Titel angezeigt wird.

### <a name="bold-and-italic-text"></a>Fetter und kursiver Text

Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:

```md
This text is **bold**.
```

Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:

```md
This text is *italic*.
```

Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Blockzitate

Blockzitate werden mit dem `>`-Zeichen generiert:

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Das vorherige Beispiel wird wie folgt gerendert:

> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.

### <a name="lists"></a>Listen

#### <a name="unordered-list"></a>Ungeordnete Liste

Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden. Beispielsweise wird das folgende Markdown:

```md
- List item 1
- List item 2
- List item 3
```

so gerendert:

- List item 1
- List item 2
- List item 3

Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein. Beispielsweise wird das folgende Markdown:

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

so gerendert:

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>Geordnete Liste

Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen. Beispielsweise wird das folgende Markdown:

```md
1. First instruction
1. Second instruction
1. Third instruction
```

so gerendert:

1. First instruction
2. Second instruction
3. Third instruction

Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein. Beispielsweise wird das folgende Markdown:

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

so gerendert:

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

Wir haben für alle Einträge „1.“ verwendet. Dadurch ist es leichter, Änderungen zu prüfen, wenn durch diese Schritte hinzugefügt oder entfernt werden.

### <a name="tables"></a>Tables

Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt. Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen. Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt. Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.

Beispielsweise wird das folgende Markdown:

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

folgendermaßen gerendert:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Weitere Informationen zum Erstellen von Tabellen finden Sie unter:

- [Organizing information with tables (Organisieren von Daten mit Tabellen)](https://help.github.com/articles/organizing-information-with-tables/) von GitHub
- Der Web-App [Markdown Tables Generator (Markdowntabellengenerator)](https://www.tablesgenerator.com/markdown_tables)
- [Adam Pritchard's Markdown Cheatsheet (Cheatsheet für Markdown von Adam Pritchard)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Michel Fortin's Markdown Extra (Markdown Extra von Michel Fortin)](https://michelf.ca/projects/php-markdown/extra/#table)
- [Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>Links

Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:

 `[link text](file-name.md)`

Weitere Informationen zur Verknüpfung finden Sie hier:

- Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.
- Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält ausführliche Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.

### <a name="code-snippets"></a>Codeausschnitte

Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen. Nähere Informationen finden Sie unter:

- [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)
- [Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)

Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren. Das allgemeine Format für umzäunte Codeblöcke ist:

    ```alias
    ...
    your code goes in here
    ...
    ```

Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung. Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:

Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.

|Name|Markdownbezeichnung|
|-----|-------|
|.NET-Konsole|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# im Browser|csharp-interactive|
|Konsole|console|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Kusto-Abfragesprache|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps (Punkt als Dezimaltrennzeichen)|powerapps-dot|
|PowerApps (Komma als Dezimaltrennzeichen)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

Die Markdownbezeichnung `csharp-interactive` gibt C# als Sprache an. Die Beispiele können über den Browser ausgeführt werden. Diese Ausschnitt werden in einem Docker-Container kompiliert und ausgeführt. Die Ergebnisse dieser Ausführung werden im Browserfenster des Benutzers angezeigt.

#### <a name="example-c"></a>Beispiel: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Darstellung__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Beispiel: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Darstellung__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a>Benutzerdefinierte Markdownerweiterungen in Docs

> [!NOTE]
> Docs.Microsoft.com (Docs) implementiert einen Markdig-Parser für Markdown, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist. Markdig fügt Funktionen über Markuperweiterungen hinzu. Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten. (Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)

GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet. Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:

- Notizzettel
- Includedateien
- Selektoren
- Eingebettete Videos
- Codeausschnitte/-beispiele

Die vollständige Liste finden Sie unter „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.

### <a name="note-blocks"></a>Notizzettel

Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:

- HINWEIS
- WARNUNG
- TIPP
- WICHTIG

Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können. Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.

Beispiele:

```md
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

![Hier wird dargestellt, wie Warnungen im vorherigen Beispiel auf der veröffentlichten Dokumentationsseite mit unterschiedlichen Symbolen und Farben aussieht.](media/alerts-rendering.png)

### <a name="include-files"></a>Includedateien

Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden. Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist. Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Arten von Includeverweisen verwenden:

- Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.
- Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.
- Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.

Inline- oder Blockincludedateien sind einfache Markdowndateien (.md). Sie können jeglichen gültigen Markdowncode enthalten. Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden. Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.

Die Anforderungen und Überlegungen zu Includedateien lauten wie folgt:

- Verwenden Sie stets dann eine Includedatei, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.
- Verwenden Sie einen Blockincludeverweis für umfangreiche Inhaltsmengen, d.h. für ein oder zwei Absätze, ein gemeinsames Verfahren oder einen gemeinsamen Abschnitt. Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.
- Includeverweise werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind. Sie werden erst nach der Veröffentlichung gerendert.
- Stellen Sie sicher, dass sämtlicher Text in einer Includedatei in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Includedatei verweist, abhängig sind. Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.
- Betten Sie keine Includeverweise in andere Includedateien ein. Sie werden nicht unterstützt.
- Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media). Der Stamm des Medienverzeichnisses darf keine Bilder enthalten. Wenn die Includedatei keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.
- Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei. Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Includedatei und jeden Artikel. Speichern Sie die Mediendatei in dem Medienordner, der der Includedatei zugeordnet ist.
- Verwenden Sie eine Includedatei nicht als ausschließlichen Inhalt eines Artikels.  Includedateien sind als Ergänzung des übrigen Artikelinhalts gedacht.

Beispiel:

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Selektoren

Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen. Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten. Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.

Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Includedatei platzieren. Dann können Sie auf diese Includedatei in allen Artikeln, die denselben Selektor verwenden, verweisen.

Hier ist ein Beispielselektor dargestellt:

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

In der [Azure-Dokumentation](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) können Sie sich die Selektoren in Aktion ansehen.

### <a name="code-include-references"></a>Codeincludeverweise

Mit der Markdownerweiterung für Codeausschnitte in der Dokumentation können Sie Codebeispiele in Ihre Artikel einbetten und diese mit sprachspezifischer Syntaxfärbung darstellen. Sie können Code aus dem aktuellen oder einem anderen Repository verwenden. Im Folgenden finden Sie einen Überblick über die Verwendung des Features mit dem [Authoring Pack für docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack). In Visual Studio Code können Sie eine Vorschau für die Codeausschnitte anzeigen, indem Sie die **Vorschau** öffnen. Die Vorschau ist nicht interaktiv, und es werden keine Hervorhebungen dargestellt.

> [!NOTE]
> Die Erweiterung unterstützt das interne Inlineeinfügen von Codeinhalten nicht. Dieser Vorgang muss über die Markdownkonvention ``` (drei Backticks) erfolgen.

#### <a name="code-from-current-repository"></a>Code aus dem aktuellen Repository

1. Drücken Sie in Visual Studio Code **ALT+M** oder **WAHLTASTE+M**, und klicken Sie auf „Codeausschnitt“.
2. Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen. Wählen Sie „Full Local Search“ (Vollständige lokale Suche) aus, wenn Sie lokal suchen möchten.
3. Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen. Wählen Sie die Datei aus, wenn sie gefunden wurde.
4. Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen. Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).
5. Geben Sie je nach Auswahl in Schritt 4 einen Wert an.

Die gesamte Codedatei wird angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Ein Teil einer Codedatei wird durch Angabe von Zeilennummern angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Ein Teil einer Codedatei wird durch einen Codeausschnittnamen angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>Code aus einem anderen Repository

1. Drücken Sie in Visual Studio Code **ALT+M** oder **WAHLTASTE+M**, und klicken Sie auf „Codeausschnitt“.
2. Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen. Wählen Sie „Cross-Repository Reference“ (Repositoryübergreifender Verweis) aus, um repositoryübergreifend zu suchen.
3. Daraufhin wird eine Auswahl der Repositorys angezeigt, die sich in *.openpublishing.publish.config.json* befinden. Wählen Sie ein Repository aus.
3. Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen. Wählen Sie die Datei aus, wenn sie gefunden wurde.
4. Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen. Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).
5. Geben Sie je nach Auswahl in Schritt 5 einen Wert an.

Ihr Codeausschnittverweis sieht folgendermaßen aus:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>Pfad zur Codedatei

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Das Beispiel stammt aus der Artikeldatei [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) des ASP.NET-Dokumentenrepositorys. Auf die Codedatei wird über einen relativen Pfad zu [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) im selben Repository verwiesen.

#### <a name="selected-line-numbers"></a>Ausgewählte Zeilennummern

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

In diesem Beispiel werden nur die Zeilen 2–24 und 26 der Codedatei *StudentController.cs* angezeigt.

Bevorzugen Sie Ausschnitte gegenüber hartcodierten Zeilennummern, wie im nächsten Abschnitt erläutert.

#### <a name="named-snippet"></a>Benannter Codeausschnitt

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Verwenden Sie für den Namen nur Buchstaben und Unterstriche.

Das Beispiel zeigt den Abschnitt `snippet_Create` der Codedatei. Die Codedatei für dieses Beispiel verfügt über einen C#-Bereich namens `snippet_Create`:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Wenn möglich, sollten Sie immer auf einen benannten Abschnitt verweisen anstatt Zeilennummern anzugeben. Zeilennummernverweise sind fehleranfällig, weil sich Codedateien zwangsläufig in einer Weise ändern, die die Zeilennummern verändern.
Über solche Änderungen werden Sie nicht unbedingt informiert. In Ihrem Artikel werden dann die falschen Zeilen angezeigt, und Sie haben keine Ahnung, dass sich überhaupt etwas geändert hat.

#### <a name="highlighting-selected-lines"></a>Hervorheben ausgewählter Zeilen

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

Im Beispiel werden die Zeilen 2 und 5 hervorgehoben, gezählt vom Anfang des angezeigten Ausschnitts. (Bei hervorzuhebenden Zeilennummern wird mit dem Zählen nicht am Anfang der Codedatei begonnen.) Die Zeilen 3 und 6 der Codedatei werden also hervorgehoben.

#### <a name="interactive-code-snippets"></a>Interaktive Codeausschnitte

Sie können den interaktiven Modus für Codeausschnitte aktivieren, die per Verweis eingebunden werden. Hier finden Sie Beispiele:

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

Verwenden Sie das Attribut `interactive`, um dieses Feature für einen bestimmten Codeblock zu aktivieren. Folgende Attributwerte sind verfügbar:

- `cloudshell-powershell`: Aktiviert wie im vorherigen Beispiel PowerShell für Azure Cloud Shell
- `cloudshell-bash`: Aktiviert Azure Cloud Shell
- `try-dotnet`: Aktiviert Try .NET
- `try-dotnet-class`: Aktiviert Try .NET mit Klassengerüsten
- `try-dotnet-method`: Aktiviert Try .NET mit Methodengerüsten

Es gibt kompatible Kombinationen von `language` und `interactive`. Wenn `interactive` beispielsweise den Wert `try-dotnet` aufweist, muss die Sprache `csharp` sein. Ebenso funktioniert `cloudshell-powershell` nur mit `powershell`, und `cloudshell-bash` würde nur mit `bash` als Sprache funktionieren.

Für Azure Cloud Shell und PowerShell Cloud Shell können Benutzer Befehle nur für ihr eigenes Azure-Konto ausführen.

[Try .NET](https://github.com/dotnet/try) aktiviert die interaktive Ausführung von .NET-Code (C#) im Browser. Für Try .NET gibt es drei Interaktivitätsoptionen: `try-dotnet`, `try-dotnet-class` und `try-dotnet-method`. Wenn Sie diese Optionen verwenden, ist keine zusätzliche Konfiguration im Codeausschnitt erforderlich. Folgende Namespaces sind derzeit standardmäßig verfügbar:

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

Mit dem Attributwert `try-dotnet` können Benutzer C#-Code im Browser ausführen, ohne den Code mit benutzerdefiniertem Code zu umschließen.

Beispiel:

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

Der Wert `try-dotnet-class` wendet ein Klassengerüst auf den Code an, der an die interaktive Komponente übergeben wird.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

Beispiel:

Codeausschnitt ohne Klassengerüst

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

Codeausschnitt mit Klassengerüst

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

Der Wert `try-dotnet-method` wendet ein Methodengerüst auf den Code an, der an die interaktive Komponente übergeben wird.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

Beispiel:

Codeausschnitt ohne Methodengerüst

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

Codeausschnitt mit Methodengerüst

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>Verweissyntax für Codeausschnitte

Sie können auf Codeausschnitte verweisen, die in Ihrem Repository gespeichert sind, indem Sie die angegebene Codesprache verwenden. Die Inhalte des angegebenen Codepfads werden erweitert und in Ihre Datei eingebunden.

Für die Ordnerstruktur von Codeausschnitten gibt es keinerlei Einschränkungen. Sie können die Codeausschnitte als normalen Quellcode verwalten.

Syntax:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Diese Syntax ist ein Blockmarkdown-Erweiterung. Sie muss in einer eigenen Zeile verwendet werden.

- `<language>` (*optional*)
  - Sprache des Codeausschnitts. Weitere Informationen finden Sie im Abschnitt [Unterstützte Sprachen](#supported-languages) weiter unten in diesem Artikel.

- `<path>` (*obligatorisch*)
  - Relativer Pfad im Dateisystem, der die Codeausschnittdatei angibt, auf die verwiesen wird.

- `<attribute>` und `<attribute-value>` (*optional*)
  - Zusammen verwendet, um anzugeben, wie der Code aus der Datei abgerufen werden sollen:
    - `range`: `1,3-5` Ein Bereich von Zeilen. Dieses Beispiel enthält die Zeilen 1, 3, 4 und 5.
    - `id`: `snippet_Create`: Die ID des Codeausschnitts, der aus der Codedatei eingefügt werden soll. Dieser Wert kann nicht gleichzeitig mit „range“ vorhanden sein.
    - `highlight`: `2-4,6`: Der Bereich und/oder die Zeilennummern, die im generierten Codeausschnitt hervorgehoben werden sollen. Die Nummerierung ist relativ zum Codeausschnitt, nicht zum importierten Bereich.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method`: Der Zeichenfolgenwert legt fest, welche Arten von Interaktivität aktiviert sind.

#### <a name="supported-languages"></a>Unterstützte Sprachen

|Name|Markdownbezeichnung|
|-----|-------|
|.NET Core-CLI|`dotnetcli`|
|ASP.NET mit C#|`aspx-csharp`|
|ASP.NET mit VB|`aspx-vb`|
|Azure CLI|`azurecli`|
|Azure CLI im Browser|`azurecli-interactive`|
|Azure PowerShell im Browser|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|C# im Browser|`csharp-interactive`|
|Konsole|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Kusto-Abfragesprache|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|Power Query M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>Codeerweiterungen

|Name|Markdownbezeichnung|Dateierweiterung|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xaml|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>Häufige Fehler und Problembehandlung

### <a name="alt-text"></a>Alternativtext

Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert. Verwenden Sie beispielsweise anstelle von

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

diese Möglichkeit zur Umgehung von Unterstrichen:

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrophe und Anführungszeichen

Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten. Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden. Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s

Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:

- Linkes (öffnendes) Anführungszeichen: `&#8220;`
- Rechtes (schließendes) Anführungszeichen: `&#8221;`
- Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`
- Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`

### <a name="angle-brackets"></a>Geschweifte Klammern

Spitze Klammern werden häufig zum Kennzeichnen eines Platzhalters verwendet. Wenn Sie dies im Text nutzen (nicht im Code), müssen Sie die spitzen Klammern codieren. Andernfalls interpretiert Markdown sie als HTML-Tag.

Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.

## <a name="markdown-flavor"></a>Markdown-Variante

Das Back-End der Website „docs.microsoft.com“ unterstützt ein kompatibles [CommonMark](https://commonmark.org/)-Markdown, das von der [Markdig](https://github.com/lunet-io/markdig)-Analyse-Engine analysiert wird. Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können. Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.

## <a name="see-also"></a>Siehe auch:

### <a name="markdown-resources"></a>Markdownressourcen

- [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)
- [Cheatsheet zur Markdown-Dokumentation](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown
- [The Markdown Guide (Das Markdown-Handbuch)](https://www.markdownguide.org/)
