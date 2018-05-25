---
title: Verwenden von Markdown für das Schreiben von Dokumentationsartikeln
description: Dieser Artikel enthält grundlegende Informationen und Verweise zu Markdown, das als Sprache zum Schreiben von docs.microsoft.com-Artikeln verwendet wird.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Verwenden von Markdown für das Schreiben von Dokumentationsartikeln

Docs.Microsoft.Com-Artikel sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist. Darum ist sie schnell zu einem Branchenstandard geworden.

Da Dokumentationsinhalte in GitHub gespeichert werden, können sie ein als Superset von Markdown bezeichnetes [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) verwenden, das zusätzliche Funktionalität für gängige Formatierungsanforderungen bietet. Außerdem implementiert Open Publishing Services (OPS) „Markdig Markdown Parser“. Markdig weist eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) auf und verfügt über Möglichkeiten zur Aktivierung von dokumentationsspezifischen Funktionen.

* Markdig ist ein schneller, leistungsstarker und mit CommonMark kompatibler erweiterbarer Markdown-Prozessor für .NET.
* https://github.com/lunet-io/markdig
* Bessere Unterstützung durch die Community
* Bessere Unterstützung für Standards

## <a name="markdown-basics"></a>Grundlegendes zu Markdown

### <a name="headings"></a>Überschriften

Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>Fetter und kursiver Text

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
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>Listen

#### <a name="unordered-list"></a>Ungeordnete Liste

Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden. Beispielsweise wird das folgende Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

so gerendert:

- List item 1
- List item 2
- List item 3

Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein. Beispielsweise wird das folgende Markdown:

```markdown
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

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

so gerendert:

1. First instruction
2. Second instruction
3. Third instruction

Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein. Beispielsweise wird das folgende Markdown:

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

so gerendert:

1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction

### <a name="tables"></a>Tables

Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt. Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen. Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt. Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.

Beispielsweise wird das folgende Markdown:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

so gerendert:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Weitere Informationen zum Erstellen von Tabellen finden Sie unter:

- Abschnitt zur Markdig-[Tabellenumbruchfunktion](#table-wrapping), die bei der Formatierung breiter Tabellen hilfreich sein kann
- [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organisieren von Daten mit Tabellen) von GitHub
- Die [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)-Web-App (Markdowntabellengenerator)
- [Markdown Cheatsheet von Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Markdown Extra von Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table)
- [Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>Links

Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:

 `[link text](file-name.md)`

Weitere Informationen zur Verknüpfung finden Sie hier:

- Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.
- Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält nähere Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.

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

Der Alias nach den anfänglichen drei „`“-Zeichen definiert die zu verwendende Syntaxhervorhebung. Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:

Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.

|Name|Markdownbezeichnung|
|-----|-------|
|.NET-Konsole|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS-CLI|vstscli|
|XAML|xaml|
|XML|xml|

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

## <a name="ops-custom-markdown-extensions"></a>OPS: benutzerdefinierte Markdownerweiterungen

> [!NOTE]
> In Open Publishing Services (OPS) ist der Markdig-Parser für Markdown implementiert, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist. Markdig fügt Funktionen über Markuperweiterungen hinzu. Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten. (Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)

GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet. Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:

- Notizzettel
- Einbeziehungen
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

### <a name="includes"></a>Einbeziehungen

Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden. Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist. Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Einbeziehungstypen verwenden:

- Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.
- Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.
- Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.

Inline- oder Blockeinbeziehungen sind einfache Markdowndateien (.md). Sie können jeglichen gültigen Markdowncode enthalten. Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden. Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.

Die Anforderungen und Überlegungen zu Einbeziehungen lauten wie folgt:

- Verwenden Sie stets dann Einbeziehungen, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.
- Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt. Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.
- Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind. Sie werden erst nach der Veröffentlichung gerendert.
- Stellen Sie sicher, dass sämtlicher Text in einer Einbeziehung in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Einbeziehung verweist, abhängig sind. Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.
- Betten Sie keine Einbeziehungen in andere Einbeziehungen ein. Sie werden nicht unterstützt.
- Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media). Der Stamm des Medienverzeichnisses darf keine Bilder enthalten. Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.
- Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei. Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel. Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.
- Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.  Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.

### <a name="selectors"></a>Selektoren

Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen. Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten. Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.

Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Einbeziehung platzieren. Dann können Sie auf diese Einbeziehung in allen Artikeln, die denselben Selektor verwenden, verweisen.

### <a name="code-snippets"></a>Codeausschnitte

Markdig unterstützt über die Codeausschnitterweiterung die erweiterte Einbeziehung von Code in einen Artikel. DFM bietet erweitertes Rendern, das auf GFM-Funktionen wie Programmieren der Sprachauswahl und farbiger Syntaxmarkierung sowie netten Funktionen wie den folgenden basiert:

- Einbeziehung zentralisierter Codebeispiele bzw. -ausschnitte aus einem externen Repository
- Benutzeroberfläche mit Registerkarten zur Anzeige mehrerer Versionen von Codebeispielen in verschiedenen Sprachen

## <a name="gotchas-and-troubleshooting"></a>Häufige Fehler und Problembehandlung

### <a name="alt-text"></a>Alternativtext

Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert. Verwenden Sie beispielsweise anstelle von

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

diese Möglichkeit zur Umgehung von Unterstrichen:

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrophe und Anführungszeichen

Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten. Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden. Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s.

Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:

- Linkes (öffnendes) Anführungszeichen: `&#8220;`
- Rechtes (schließendes) Anführungszeichen: `&#8221;`
- Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`
- Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`

### <a name="angle-brackets"></a>Geschweifte Klammern

Wenn Sie in Ihrer Datei geschweifte Klammern im Text (nicht Code) verwenden, z.B. zur Bezeichnung eines Platzhalters, müssen Sie die geschweiften Klammern manuell codieren. Andernfalls interpretiert Markdown sie als HTML-Tag.

Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.

## <a name="see-also"></a>Siehe auch

### <a name="markdown-resources"></a>Markdownressourcen

- [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)
- [Cheatsheet zur Markdown-Dokumentation](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown
