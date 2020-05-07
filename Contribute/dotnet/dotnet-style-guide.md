---
title: Vorlage und Spickzettel für .NET-Artikel
description: In diesem Artikel ist eine praktische Vorlage enthalten, die Sie zum Erstellen neuer Artikel für die Repositorys der .NET-Dokumentation verwenden können.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: a520112cd77f4c4807e7719c2c4dbd43a762f062
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "80759550"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>Metadaten und Markdownvorlage für .NET-Dokumentationen

Diese dotnet/docs-Vorlage enthält Beispiele für die Markdownsyntax sowie Anweisungen zum Einstellen der Metadaten.

Beim Erstellen einer Markdowndatei sollten Sie die enthaltene Vorlage in eine neue Datei kopieren, die Metadaten wie unten gezeigt ausfüllen und den Titel des Artikels in der obigen H1-Überschrift festlegen.

## <a name="metadata"></a>Metadaten

Der erforderliche Metadatenblock befindet sich im folgenden Metadatenblockbeispiel:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Sie **müssen** zwischen dem Doppelpunkt („:“) und dem Wert eines Metadatenelements ein Leerzeichen setzen.
- Doppelpunkte in einem Wert (z.B. in einem Titel) unterbrechen den Metadatenparser. In diesem Fall müssen Sie doppelte Anführungszeichen um den Titel setzen (z.B. `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title**: Wird in den Ergebnissen von Suchmaschinen angezeigt. Der Titel sollte nicht mit dem Titel in Ihrer H1-Überschrift übereinstimmen und darf maximal 60 Zeichen enthalten.
- **description**: Zusammenfassung des Artikelinhalts. Für gewöhnlich wird diese Beschreibung in den Suchergebnissen angezeigt, jedoch wird sie nicht für die Suchrangfolge verwendet. Einschließlich der Leerzeichen sollte die Länge der Beschreibung zwischen 115 und 145 Zeichen liegen.
- **author**: Das Feld „author“ (Autor) sollte den **GitHub-Benutzernamen** des Autors enthalten.
- **ms.date**: Das Datum des letzten wichtigen Updates. Aktualisieren Sie dieses Datum bei vorhandenen Artikeln, wenn Sie einen gesamten Artikel prüfen und aktualisieren. Kleine Fehlerbehebungen, z.B. Tippfehler oder ähnliches, rechtfertigen ein Update nicht.

An jeden Artikel werden weitere Metadaten angefügt, allerdings werden die meisten Metadatenwerte in der Regel auf der Ordnerebene angewendet. Dies wird in der Datei **docfx.json** angegeben.

## <a name="basic-markdown-gfm-and-special-characters"></a>Grundlegendes Markdown, GFM und Sonderzeichen

Die Grundlagen von Markdown, GFM (GitHub Flavored Markdown) und OPS-spezifischen Erweiterungen können Sie anhand des Artikels [Markdownreferenz](../markdown-reference.md) erlernen.

Markdown nutzt Sonderzeichen wie \*, \` und \# für die Formatierung. Wenn Sie eines dieser Zeichen in Ihren Inhalt einfügen möchten, müssen Sie eine der folgenden Vorgehensweisen anwenden:

- Versehen Sie das Sonderzeichen mit einem umgekehrten Schrägstrich als Escapezeichen (z.B. `\*` für \*).
- Verwenden Sie den [HTML-Code](http://www.ascii.cl/htmlcodes.htm) für das Zeichen (z.B. `&#42;` für &#42;).

## <a name="file-names"></a>Dateinamen

Dateinamen unterliegen folgenden Regeln:

* Nur Kleinbuchstaben, Zahlen und Bindestriche sind zulässig.
* Leer- oder Satzzeichen sind nicht erlaubt. Worte und Zahlen im Dateinamen werden durch Bindestriche getrennt.
* Verwenden Sie Verben, die den Zweck angeben, z.B. develop, buy, build, troubleshoot. Auf „-ing“ endenden Worte dürfen nicht verwendet werden.
* Kurze Worte wie a, and, the, in, or usw. sind nicht erlaubt.
* Das Markdownformat und die Erweiterung „.md“ sind erforderlich.
* Verwenden Sie angemessene, kurze Dateinamen. Sie sind Teil der URL für Ihre Artikel.

## <a name="headings"></a>Überschriften

Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung. Schreiben Sie das erste Wort einer Überschrift immer groß.

## <a name="text-styling"></a>Textformatierung

*Kursiv:* Für Dateien, Ordner, Pfade (für lange Elemente, die in Ihre eigene Zeile getrennt werden) und neue Begriffe

**Fett:** Für Benutzeroberflächenelemente

`Code` für Inlinecode, Schlüsselwörter der Sprache, NuGet-Paketnamen, Befehlszeilenbefehle, Datenbanktabellen- und Spaltennamen sowie URLs, die nicht klickbar sein sollen

## <a name="links"></a>Links

Informationen zu Ankern, internen Links, Links zu anderen Dokumenten, Codeeinfügungen und externen Links finden Sie im allgemeinen Artikel zu [Links](../how-to-write-links.md).

Das Team für die .NET-Dokumentation wendet folgende Konventionen an:

- In den meisten Fällen werden relative Links verwendet. Von der Verwendung von `~/` wird in Links abgeraten, weil relative Links zur Quelle auf GitHub führen. Allerdings wird das Zeichen `~/` für Links zu Dateien in abhängigen Repositorys verwendet, um den Pfad anzugeben. Da die Dateien im abhängigen Repository sich auf GitHub an einem anderen Speicherort befinden, werden die Links mit relativen Links, unabhängig davon, wie sie geschrieben sind, nicht richtig aufgelöst.
- Die C#-Sprachspezifikation und die Visual Basic-Sprachspezifikation sind in den .NET-Dokumentationen enthalten, indem die Quelle der Sprach-Repositorys eingebunden wird. Die Markdownquellen werden in den Repositorys [csharplang](https://github.com/dotnet/csharplang) und [vblang](https://github.com/dotnet/vblang) verwaltet.

Links zu den Sprachspezifikationen müssen zu den Quellverzeichnissen zeigen, in denen diese Spezifikationen enthalten sind. Für C# ist das Verzeichnis **~/_csharplang/spec**, und für Visual Basic ist das Verzeichnis **~/_vblang/spec**. Dies wird im folgenden Beispiel veranschaulicht:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>Links zu APIs

Das Buildsystem verfügt über einige Erweiterungen, mit denen Sie Links zu .NET-APIs erstellen können, ohne externe Links verwenden zu müssen. Verwenden Sie eine der folgenden Syntaxvarianten:

1. Automatische Verknüpfung: `<xref:UID>` oder `<xref:UID?displayProperty=nameWithType>`

   Der `displayProperty`-Abfrageparameter erzeugt einen vollqualifizierten Linktext. Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.

2. Markdownlink: `[link text](xref:UID)`

   Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.

Beispiele:

- `<xref:System.String>` wird als [Zeichenfolge](https://docs.microsoft.com/dotnet/api/system.string) gerendert
- `<xref:System.String?displayProperty=nameWithType>` wird als [System.String](https://docs.microsoft.com/dotnet/api/system.string) gerendert
- `[String class](xref:System.String)` wird als [Zeichenfolgenklasse](https://docs.microsoft.com/dotnet/api/system.string) gerendert

Weitere Informationen zur Verwendung dieser Notation finden Sie unter [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Verwenden des Querverweises).

Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert jeweils als `%60`, `%23` und `%2A` im HTML-Format codiert werden. Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.

Beispiele:

- System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor wird `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

Die UIDs von Typen, eine Liste von überladenen Membern oder einen bestimmten überladenen Member finden Sie über `https://xref.docs.microsoft.com/autocomplete`. Die Abfragezeichenfolge `?text=*\<type-member-name>*` gibt den Typ oder Member an, dessen UIDs Sie abrufen möchten. `https://xref.docs.microsoft.com/autocomplete?text=string.format` ruft beispielsweise die Überladungen [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) ab. Das Tool sucht in der UID nach dem angegebenen Abfrageparameter `text`. Zum Beispiel können Sie nach Membernamen (ToString), partiellen Membernamen (ToStri), Typen und Membernamen (Double.ToString) und mehr suchen.

Wenn Sie \* (oder `%2A`) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API. Dies können Sie z.B. verwenden, wenn Sie eine Verknüpfung mit der Seite [List\<T>.BinarySearch-Methode](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) auf generische Weise als Alternative zu einer bestimmten Überladung wie [List\<T>.BinarySearch (T, IComparer\<T >)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) herstellen möchten. Sie können auch \* verwenden, um einen Link zu einer Memberseite zu erstellen, wenn der Member nicht überladen ist. Damit ersparen Sie sich das Einfügen der Parameterliste in die UID.

Sie müssen den vollqualifizierten Namen des Typs jedes Parameters der Methode einfügen, um einen Link zu einer spezifischen Methodenüberladung zu erstellen. Zum Beispiel führt \<xref:System.DateTime.ToString> zu der parameterlosen Methode [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), und \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> führt zu der Methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).

Verwenden Sie zum Verknüpfen eines generischen Typs (z.B. [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)) das Zeichen \` (`%60`) gefolgt von der Anzahl generischer Typparameter. Zum Beispiel verknüpft `<xref:System.Nullable%601>` den Typ [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), und `<xref:System.Func%602>` verknüpft den Delegaten [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).

## <a name="code"></a>Code

Die beste Methode zum Einfügen von Code besteht darin, Ausschnitte aus einem funktionstüchtigen Beispiel einzufügen. Erstellen Sie Ihr Beispiel anhand der Anweisungen im Artikel [Contributing to .NET (Mitwirken an .NET)](dotnet-contribute.md#contributing-to-samples). Die grundlegenden Regeln zum Einfügen von Code finden Sie im allgemeinen Leitfaden für [Code](../code-in-docs.md).

Sie können den Code mithilfe der folgenden Syntax einfügen:

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (*optional*, aber *empfohlen*)
  * Sprache des referenzierten Codeausschnitts.

* `<name>` (*optional*)
  * Name des Codeausschnitts. Er wirkt sich nicht auf die HTML-Ausgabe aus, Sie können ihn jedoch verwenden, um die Lesbarkeit Ihrer Markdownquelle zu verbessern.

* `<pathToFile>` (*obligatorisch*)
  * Relativer Pfad im Dateisystem, der die Codeausschnittdatei angibt, auf die verwiesen wird. Dies kann sich aufgrund der verschiedenen Repositorys, aus denen die .NET-Dokumentation besteht, als kompliziert erweisen. Die .NET-Beispiele befinden sich im Repository „dotnet/samples“. Alle Pfade für Codeausschnitte beginnen mit `~/samples`, der Rest ist der Pfad vom Stamm zur Quelle des Repositorys.

* `<queryoption>` (*optional*)
  * Wird verwendet, um anzugeben, wie der Code aus der Datei abgerufen werden soll:
    * `#`: `#{tagname}` (Tagname) *oder* `#L{startlinenumber}-L{endlinenumber}` (Zeilenbereich).
    Von der Verwendung von Zeilennummern wird abgeraten, da sie sehr fehleranfällig sind. Zum Referenzieren von Codeausschnitten werden Tagnamen empfohlen. Verwenden Sie aussagekräftige Tagnamen. (Viele Codeausschnitte wurden aus einer vorherigen Plattform migriert, und die Tags haben Namen wie `Snippet1`, `Snippet2` usw. Diese Vorgehensweise ist weitaus schwerer zu verwalten.)
    * `range`: `?range=1,3-5` Ein Bereich von Zeilen. Dieses Beispiel enthält die Zeilen 1, 3, 4 und 5.

Es wird empfohlen, wenn möglich die Option zum Benennen der Tags zu verwenden. Der Tagname ist der Name eines Bereichs oder eines Codekommentars im im Quellcode enthaltenen Format `Snippettagname`. Im folgenden Beispiel wird veranschaulicht, wie der Tagname `BasicThrow` referenziert wird:

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

Der relative Pfad zur Quelle im Repository **dotnet/samples** folgt dem Pfad `~/samples`.

In [dieser Quelldatei](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) wird dargestellt, wie Tags von Ausschnitten strukturiert sind. Details zur Darstellung des Tagnamens in den Quelldateien des Codeausschnitts pro Sprache finden Sie unter [DocFX-Richtlinien](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

Im folgenden Beispiel wird Code in allen drei .NET-Sprachen gezeigt:

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

Durch Einfügen von Ausschnitten aus vollständigen Programmen wird sichergestellt, dass der gesamte Code das CI-System (Continuous Integration) durchläuft. Wenn Sie jedoch etwas veranschaulichen müssen, das zu Fehlern zur Kompilier- oder Laufzeit führt, können Sie Inlinecodeblöcke verwenden.

## <a name="images"></a>Bilder

### <a name="static-image-or-animated-gif"></a>Statisches Bild oder animiertes GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Verknüpftes Bild

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Videos

Derzeit können Sie mithilfe der folgenden Syntax sowohl Channel 9- als auch YouTube-Videos einbetten:

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

Wählen Sie die Registerkarte **Embed** (Einbetten) unter dem Video aus, und kopieren Sie die URL aus dem `<iframe>`-Element, um die richtige URL des Videos abzurufen. Beispiel:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Klicken Sie mit der rechten Maustaste auf das Video, und wählen Sie **Einbettungscode kopieren** aus `<iframe>`, um die richtige URL des Videos abzurufen.

```markdown
> [!VIDEO <youtube_video_link>]
```

Beispiel:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>Erweiterungen für docs.microsoft

Einige zusätzliche Erweiterungen für GitHub Flavored Markdown werden von docs.microsoft bereitgestellt.

### <a name="checked-lists"></a>Listen mit Häkchen

Für Listen ist eine benutzerdefinierte Formatvorlage verfügbar. Sie können Listen mit grünen Häkchen ausgeben.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Dies wird wie folgt dargestellt:

> [!div class="checklist"]
> * Erstellen einer .NET Core-App
> * Hinzufügen eines Verweises zum Microsoft.XmlSerializer.Generator-Paket
> * Bearbeiten Ihrer MyApp.csproj-Datei zum Hinzufügen von Abhängigkeiten
> * Hinzufügen von „XmlSerializer“ und einer Klasse
> * Erstellen und Ausführen der Anwendung

Ein Beispiel der Liste mit Häkchen finden Sie in dieser [.NET Core-Dokumentation](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).

### <a name="buttons"></a>Schaltflächen

Schaltflächenlinks:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Dies wird wie folgt dargestellt:

> [!div class="button"]
> [Schaltflächenlinks](dotnet-contribute.md)

Ein Beispiel solcher Schaltflächen finden Sie in dieser [Visual Studio-Dokumentation](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).

### <a name="step-by-steps"></a>Exemplarische Vorgehensweisen

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

Ein Beispiel für exemplarische Vorgehensweisen finden Sie in diesem [C#-Leitfaden](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).
