---
title: Vorlage und Spickzettel für PowerShell-Artikel
description: Dieser Artikel enthält eine praktische Vorlage, die Sie zum Erstellen neuer Artikel für die PowerShell-Dokumentationen verwenden können.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290355"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>Markdown-Styleguide für PowerShell-Dokumentationen

Dieser Artikel enthält stilistische Anweisungen für PowerShell-Dokumentationen.

Andere Leitfäden zum Schreibstil finden Sie im [Microsoft-Styleguide](https://docs.microsoft.com/style-guide/welcome/).

## <a name="metadata"></a>Metadaten

Diese Vorlage enthält Beispiele für die Markdownsyntax sowie Anweisungen zum Einstellen der Metadaten.
Beim Erstellen einer Markdowndatei sollten Sie die enthaltene Vorlage in eine neue Datei kopieren, die Metadaten wie unten gezeigt ausfüllen und den Titel des Artikels in der obigen H1-Überschrift festlegen.

Der erforderliche Metadatenblock befindet sich im folgenden Metadatenblockbeispiel:

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Sie **müssen** zwischen dem Doppelpunkt („:“) und dem Wert eines Metadatenelements ein Leerzeichen setzen.
- Doppelpunkte in einem Wert (z.B. in einem Titel) unterbrechen den Metadatenparser. In diesem Fall müssen Sie doppelte Anführungszeichen um den Titel setzen (z.B. `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author**: Das Feld „author“ (Autor) sollte den **GitHub-Benutzernamen** des Autors enthalten.
- **description**: Zusammenfassung des Artikelinhalts. Für gewöhnlich wird diese Beschreibung in den Suchergebnissen angezeigt, jedoch wird sie nicht für die Suchrangfolge verwendet. Einschließlich der Leerzeichen sollte die Länge der Beschreibung zwischen 115 und 145 Zeichen liegen.
- **ms.date**: Das Datum des letzten wichtigen Updates. Aktualisieren Sie dieses Datum bei vorhandenen Artikeln, wenn Sie einen gesamten Artikel prüfen und aktualisieren. Kleine Fehlerbehebungen, z. B. Tippfehler oder ähnliches, rechtfertigen ein Update nicht.
- **title**: Wird in den Ergebnissen von Suchmaschinen angezeigt. Der Titel sollte nicht mit dem Titel in Ihrer H1-Überschrift übereinstimmen und darf maximal 60 Zeichen enthalten.

An jeden Artikel werden weitere Metadaten angefügt, allerdings werden die meisten Metadatenwerte in der Regel auf der Ordnerebene angewendet. Dies wird in der Datei **docfx.json** angegeben.

## <a name="product-terminology"></a>Produktterminologie

Es gibt verschiedene Varianten von PowerShell. In der folgenden Tabelle werden einige verschiedene Begriffe definiert, die bei der Erörterung von PowerShell verwendet werden.

- **PowerShell:** Dies ist die Standardversion. PowerShell ist das von Microsoft veröffentlichte Produkt. Der Begriff PowerShell kann verwendet werden, um eine beliebige Edition des Produkts zu beschreiben.
- **PowerShell Core:** Dies ist PowerShell basierend auf der .NET CoreCLR (Common Language Runtime) für unterstützte Plattformen.
- **Windows PowerShell:** Dies ist PowerShell basierend auf der .NET Framework-CLR. Windows PowerShell wird nur für Windows bereitgestellt und umfasst die vollständige .NET Framework-CLR.

„Windows PowerShell“ kann im Allgemeinen in „PowerShell“ geändert werden.
„Windows PowerShell“ sollte **nicht** geändert werden, wenn Windows-spezifische Technologien behandelt werden.

## <a name="basic-markdown-gfm-and-special-characters"></a>Grundlegendes Markdown, GFM und Sonderzeichen

Die Grundlagen von Markdown, GFM (GitHub Flavored Markdown) und OPS-spezifischen Erweiterungen können Sie anhand des allgemeinen Artikels zu [Markdown](../how-to-write-use-markdown.md) und der [Markdownreferenz](../markdown-reference.md) erlernen.

Markdown nutzt Sonderzeichen wie \*, \` und \# für die Formatierung. Wenn Sie eines dieser Zeichen in Ihren Inhalt einfügen möchten, müssen Sie eine der folgenden Vorgehensweisen anwenden:

- Versehen Sie das Sonderzeichen mit einem umgekehrten Schrägstrich als Escapezeichen (z.B. `\*` für \*).
- Verwenden Sie den [HTML-Code](http://www.ascii.cl/htmlcodes.htm) für das Zeichen (z.B. `&#42;` für &#42;).
- Markdowndateien sollten nur ASCII-Text oder die UTF-8-Codierung verwenden. Vermeiden Sie jedoch die Verwendung von UTF-8-Zeichen mit mehreren Bytes. Verwenden Sie stattdessen eine HTML-Entität. Verwenden Sie beispielsweise für Copyrightsymbole `&copy;`.
  Es wird als „&copy;“ gerendert.

## <a name="hyperlinks"></a>Links

- Vermeiden Sie die Verwendung bloßer URLs. Verwenden Sie für Links die Markdownsyntax `[friendlyname](url-or-path)`.
- Links sollten einen Anzeigenamen haben. In den meisten Fällen eignet sich der Titel des Artikels.
- Alle Elemente im Abschnitt „Verwandte Links“ ganz unten sollten Links sein.
- Verwenden Sie relative Links, wenn Sie Links zu anderen Inhalten auf **docs.microsoft.com** verwenden.
- Verwenden Sie innerhalb der Klammern eines Links keine Backticks, keinen Fettdruck und kein anderes Markup.

Ausführlichere Informationen zu Links finden Sie unter [Verwenden von Links in der Dokumentation](../how-to-write-links.md).

## <a name="filenames"></a>Dateinamen

Dateinamen unterliegen folgenden Regeln:

- Sie dürfen nur Buchstaben, Zahlen und Bindestriche enthalten.
- Leer- oder Satzzeichen sind nicht erlaubt. Worte und Zahlen im Dateinamen werden durch Bindestriche getrennt.
- Verwenden Sie Verben, die den Zweck angeben, z.B. develop, buy, build, troubleshoot. Auf „-ing“ endenden Worte dürfen nicht verwendet werden.
- Kurze Worte wie a, and, the, in, or usw. sind nicht erlaubt.
- Das Markdownformat und die Erweiterung „.md“ sind erforderlich.
- Verwenden Sie angemessene, kurze Dateinamen. Sie sind Teil der URL für Ihre Artikel.

## <a name="blank-lines-spaces-and-tabs"></a>Leerzeilen, Leerzeichen und Tabstopps

Entfernen Sie doppelte Leerzeilen. Mehrere Leerzeilen werden in HTML als eine Leerzeile dargestellt, mehrere Leerzeilen haben also keinen Zweck.

Leerzeilen geben außerdem das Ende eines Blocks in Markdown an. Es sollte eine einzelne Leerzeile zwischen Markdownblöcken mit verschiedenen Typen geben (z. B. zwischen einem Paragraphen und einer Liste oder Überschrift).

> [!NOTE]
> Abstände sind in Markdown wichtig. Verwenden Sie immer Leerzeichen anstelle von harten Tabstopps. Entfernen Sie zusätzliche Leerzeichen am Ende von Zeilen.

## <a name="titles-and-headings"></a>Titel und Überschriften

Verwenden Sie nur [ATX-Überschriften][atx] (#-Format, anstatt `=`- oder `-`-Überschriften).

- Befolgen Sie die Rechtschreibregeln gemäß Duden (empfohlene Schreibweise).
- Zwischen `#` und dem ersten Buchstaben der Überschrift muss ein einzelnes Leerzeichen stehen.
- Überschriften sollten von einzelnen Leerzeilen umgeben sein.
- Für jedes Dokument ist nur eine H1-Überschrift zulässig.
- Überschriftstufen sollten immer um eine Stufe erhöht werden. Überspringen Sie keine Stufen.
- Verwenden Sie keine Backticks, keinen Fettdruck und kein anderes Markup in Überschriften.

> [!CAUTION]
> Das von [PlatyPS][platyPS] erzwungene Schema für die Cmdlet-Referenz erfordert spezifische H2- und H3-Überschriften. Das Hinzufügen oder Entfernen von Überschriften kann den Build unterbrechen. Weitere Informationen finden Sie im [Styleguide für die Cmdlet-Referenz](powershell-style-reference.md).

## <a name="limit-line-length-to-100-characters"></a>Schränken Sie die Zeilenlänge auf 100 Zeichen ein.

Dadurch wird die Befehlszeilenausgabe für Unterschiede und Verläufe vereinfacht.

Für den Großteil der vorhandenen Inhalte der PowerShell-Dokumentationen war diese Regel noch nicht in Kraft, sie wird jedoch im Laufe der Zeit implementiert. Sie können uns dabei gerne unterstützen. Die [Reflow-Erweiterung][reflow] für Visual Studio Code (VS Code) vereinfacht das erneute Formatieren von Paragraphen gemäß dieser Regel.

## <a name="lists"></a>Listen

Wenn Ihre Liste mehrere Sätze oder Paragraphen enthält, sollten Sie Unterüberschriften anstelle einer Liste in Betracht ziehen.

Listen sollten von einzelnen Leerzeilen umgeben sein.

### <a name="unordered-lists"></a>Unsortierte Listen

Beenden Sie Listenelemente nicht mit einem Punkt, es sei denn, sie enthalten mehrere Sätze. Verwenden Sie das Bindestrichzeichen (`-`) für Aufzählungen von Listenelementen. Dadurch wird Verwirrung mit Markup für Fett und Kursiv vermieden, die das Sternchenzeichen [`*`] verwenden. Fügen Sie einen Zeilenumbruch ein, und passen Sie den Einzug an das erste Zeichen der Aufzählung an, um einen Paragraphen oder andere Elemente unter ein Aufzählungselement einzufügen.

Beispiel:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

Dies ist eine Liste, die untergeordnete Elemente unter einem Aufzählungselement enthält.

- Erstes Aufzählungselement

  Satz zur Erläuterung des ersten Elements.

  - Untergeordnetes Aufzählungselement

    Satz zur Erläuterung des untergeordneten Elements.

- Zweites Aufzählungselement
- Drittes Aufzählungselement

### <a name="ordered-lists"></a>Sortierte Listen

Passen Sie den Einzug an das erste Zeichen nach der Elementnummer an, um einen Paragraphen oder andere Elemente unter einem nummerierten Element einzufügen.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

So erhalten Sie diese Ausgabe:

> 1. Fügen Sie für das erste Element ein einzelnes Leerzeichen nach der „1“ ein. Lange Sätze sollten einen Zeilenumbruch enthalten und müssen am ersten Zeichen nach dem Marker für die nummerierte Liste ausgerichtet werden.
>
>    Fügen Sie einen Zeilenumbruch nach dem ersten Element ein, und passen Sie die Einzüge an, um ein zweites Element (wie dieses hier) einzufügen. Der Einzug des zweiten Elements muss am ersten Zeichen nach dem Marker für die nummerierte Liste ausgerichtet werden. Für einstellige Ziffernelemente, wie dieses, fügen Sie einen Einzug bis Spalte 4 ein. Für zweistellige Ziffernelemente, z. B. ein Element mit der Nummer 10, fügen Sie einen Einzug bis Spalte 5 ein.
>
> 1. Das nächste nummerierte Element beginnt hier.

Alle Elemente in einer nummerierten Liste sollten die Zahl `1.` enthalten, anstatt die Zahl für jedes Element zu erhöhen.
Das Markdownrendering erhöht den Wert automatisch. Dadurch wird das Neuanordnen von Elementen einfacher und der Einzug von untergeordneten Inhalten wird standardisiert.

## <a name="formatting-command-syntax-elements"></a>Formatieren von Befehlssyntaxelementen

- Namen von PowerShell-Cmdlets werden mit der [Pascal-Schreibweise][pascal-case] geschrieben. Verben werden mithilfe eines Bindestrichs von Substantiven getrennt. Verwenden Sie immer den vollständigen Namen in der Pascal-Schreibweise für Cmdlets und Parameter. Vermeiden Sie die Verwendung von Aliasen, es sei denn, Sie schreiben spezifisch über Aliase.

- Schlüsselwörter der Sprache, Cmdlet-Namen und Variablenverweise sollten in Paragraphen von Backtickzeichen (`` ` ``) umschlossen werden. Eigenschaft, Parameter und Klassennamen sollten **Fett** sein.

  Beispiel:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- Wenn Sie einen Parameter bei Namen nennen, sollte der Name **fett** geschrieben werden. Wenn Sie die Verwendung eines Parameters mithilfe eines Bindestrichs als Präfix darstellen, sollte der Parameter von Backticks umschlossen werden. Beispiel:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- Wenn Sie über externe Befehle (EXE-Dateien, Skripts usw.) schreiben, sollte der Befehlsname fett und in Kleinbuchstaben (oder am Anfang eines Satzes groß) geschrieben werden sowie die entsprechende Dateierweiterung enthalten. Beispiel:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- Wenn Sie die Verwendung eines externen Befehls veranschaulichen, sollte das Beispiel von Backticks umschlossen werden.
  Wenn ein Namenskonflikt mit einem Alias vorliegt, müssen Sie die Dateierweiterung in das Befehlsbeispiel einfügen. Beispiel:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- Wenn Sie einen Konzeptartikel schreiben (im Gegensatz zu Referenzinhalten), sollte das erste Vorkommnis eines Cmdlet-Namens ein Link zur Dokumentation des Cmdlets sein. Verwenden Sie innerhalb der Klammern eines Links keine Backticks, keinen Fettdruck und kein anderes Markup.

  Beispiel:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  Weitere Informationen finden Sie im Abschnitt [Links](#hyperlinks) des Styleguides.

## <a name="images"></a>Bilder

Verwenden Sie zum Einbetten eines Bilds die folgende Syntax:

```Syntax
![[alt text]](<folderPath>)
```

Beispiel:

```markdown
![Introduction](./media/overview/Introduction.png)
```

`alt text` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild. Für visuell eingeschränkte Menschen ist Alternativtext erforderlich. Dies ist außerdem nützlich, wenn auf der Website ein Fehler auftritt, durch den das Bild nicht angezeigt werden kann.

Bilder sollten in einem `media/<article-name>`-Ordner innerhalb des Ordners gespeichert werden, der Ihren Artikel enthält. Ein Bild sollte nicht in mehreren Artikeln verwendet werden. Erstellen Sie einen Ordner, der mit dem Dateinamen Ihres Artikels im `media`-Ordner übereinstimmt. Kopieren Sie die Bilder für diesen Artikel in diesen neuen Ordner. Wenn ein Bild in mehreren Artikeln verwendet wird, muss jeder Bildordner eine Kopie dieser Bilddatei enthalten. Durch diese Vorgehensweise wird verhindert, dass eine Änderung an einem Bild in einem Artikel sich auf einen anderen Artikel auswirkt.

In manchen Fällen möchten Sie Bilder, z. B. Logos und Symbole, in mehreren Artikeln verwenden. Diese Bilder werden im `/media/shared`-Ordner im Stammverzeichnis des Repositorys gespeichert.

Die folgenden Bilddateitypen werden unterstützt: „*.png“, „*.gif“, „*.jpeg“, „*.jpg“, „*.svg“.

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
