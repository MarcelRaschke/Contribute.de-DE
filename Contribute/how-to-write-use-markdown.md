---
title: Verwenden von Markdown für das Schreiben von Dokumentationsartikeln
description: Dieser Artikel enthält grundlegende Informationen und Verweise zu Markdown, das als Sprache zum Schreiben von docs.microsoft.com-Artikeln verwendet wird.
ms.date: 07/13/2017
ms.openlocfilehash: 21194c4bd6020d847b526a4d9544c826aa199e2a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609520"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="7ea9e-103">Verwenden von Markdown für das Schreiben von Dokumentationsartikeln</span><span class="sxs-lookup"><span data-stu-id="7ea9e-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="7ea9e-104">Artikel auf [docs.microsoft.com](http://docs.microsoft.com) sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="7ea9e-105">Darum ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="7ea9e-106">Da Dokumentationsinhalte auf GitHub gespeichert werden, können sie ein als Superset von Markdown bezeichnetes [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) verwenden, das zusätzliche Funktionalität für gängige Formatierungsanforderungen bietet.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="7ea9e-107">Außerdem implementiert Open Publishing Services (OPS) „Markdig Markdown Parser“.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="7ea9e-108">Markdig weist eine hohe Kompatibilität mit GFM auf und verfügt über Möglichkeiten zur Aktivierung von dokumentationsspezifischen Features.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="7ea9e-109">Markdig ist ein schneller, leistungsstarker und mit CommonMark kompatibler erweiterbarer Markdown-Prozessor für .NET.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="7ea9e-110">Bessere Unterstützung durch die Community</span><span class="sxs-lookup"><span data-stu-id="7ea9e-110">Better community support</span></span>
* <span data-ttu-id="7ea9e-111">Bessere Unterstützung für Standards</span><span class="sxs-lookup"><span data-stu-id="7ea9e-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="7ea9e-112">Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="7ea9e-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="7ea9e-113">Überschriften</span><span class="sxs-lookup"><span data-stu-id="7ea9e-113">Headings</span></span>

<span data-ttu-id="7ea9e-114">Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="7ea9e-115">Überschriften sollten im ATX-Format verfasst werden. Verwenden Sie also 1–6 Rautezeichen (#) am Anfang der Zeile, um eine Überschrift zu kennzeichnen. Diese entsprechen den HTML-Überschriftenebenen H1 bis H6.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="7ea9e-116">Oben sehen Sie Beispiele für Überschriften von der ersten bis zur vierten Ebene.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="7ea9e-117">Es darf **nur eine** Überschrift auf der ersten Ebene (H1) in Ihrem Artikel geben. Diese wird als Titel der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="7ea9e-118">Wenn Ihre Überschrift auf `#` endet, müssen Sie ein weiteres `#`-Zeichen hinzufügen, damit der Titel ordnungsgemäß gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="7ea9e-119">Beispiel: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="7ea9e-120">Überschriften auf der zweiten Ebene generieren das Inhaltsverzeichnis auf der Seite, das unter „In diesem Artikel“ neben dem Titel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="7ea9e-121">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="7ea9e-121">Bold and italic text</span></span>

<span data-ttu-id="7ea9e-122">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="7ea9e-123">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="7ea9e-124">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="7ea9e-125">Blockzitate</span><span class="sxs-lookup"><span data-stu-id="7ea9e-125">Blockquotes</span></span>

<span data-ttu-id="7ea9e-126">Blockzitate werden mit dem `>`-Zeichen generiert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="7ea9e-127">Das vorherige Beispiel wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="7ea9e-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="7ea9e-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="7ea9e-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="7ea9e-131">Listen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="7ea9e-132">Ungeordnete Liste</span><span class="sxs-lookup"><span data-stu-id="7ea9e-132">Unordered list</span></span>

<span data-ttu-id="7ea9e-133">Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="7ea9e-134">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="7ea9e-135">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-135">will be rendered as:</span></span>

- <span data-ttu-id="7ea9e-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="7ea9e-136">List item 1</span></span>
- <span data-ttu-id="7ea9e-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="7ea9e-137">List item 2</span></span>
- <span data-ttu-id="7ea9e-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="7ea9e-138">List item 3</span></span>

<span data-ttu-id="7ea9e-139">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7ea9e-140">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="7ea9e-141">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-141">will be rendered as:</span></span>

- <span data-ttu-id="7ea9e-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="7ea9e-142">List item 1</span></span>
  - <span data-ttu-id="7ea9e-143">List item A</span><span class="sxs-lookup"><span data-stu-id="7ea9e-143">List item A</span></span>
  - <span data-ttu-id="7ea9e-144">List item B</span><span class="sxs-lookup"><span data-stu-id="7ea9e-144">List item B</span></span>
- <span data-ttu-id="7ea9e-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="7ea9e-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="7ea9e-146">Geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="7ea9e-146">Ordered list</span></span>

<span data-ttu-id="7ea9e-147">Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="7ea9e-148">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="7ea9e-149">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-149">will be rendered as:</span></span>

1. <span data-ttu-id="7ea9e-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-150">First instruction</span></span>
2. <span data-ttu-id="7ea9e-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-151">Second instruction</span></span>
3. <span data-ttu-id="7ea9e-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-152">Third instruction</span></span>

<span data-ttu-id="7ea9e-153">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7ea9e-154">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="7ea9e-155">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-155">will be rendered as:</span></span>

1. <span data-ttu-id="7ea9e-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-156">First instruction</span></span>
   1. <span data-ttu-id="7ea9e-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-157">Sub-instruction</span></span>
   2. <span data-ttu-id="7ea9e-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-158">Sub-instruction</span></span>
2. <span data-ttu-id="7ea9e-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="7ea9e-159">Second instruction</span></span>

<span data-ttu-id="7ea9e-160">Wir haben für alle Einträge</span><span class="sxs-lookup"><span data-stu-id="7ea9e-160">Note that we use '1.'</span></span> <span data-ttu-id="7ea9e-161">„1.“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-161">for all entries.</span></span> <span data-ttu-id="7ea9e-162">Dadurch ist es leichter, Änderungen zu prüfen, wenn durch diese Schritte hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="7ea9e-163">Tables</span><span class="sxs-lookup"><span data-stu-id="7ea9e-163">Tables</span></span>

<span data-ttu-id="7ea9e-164">Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="7ea9e-165">Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="7ea9e-166">Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="7ea9e-167">Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="7ea9e-168">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="7ea9e-169">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-169">will be rendered as:</span></span>

| <span data-ttu-id="7ea9e-170">Fun</span><span class="sxs-lookup"><span data-stu-id="7ea9e-170">Fun</span></span>                  | <span data-ttu-id="7ea9e-171">With</span><span class="sxs-lookup"><span data-stu-id="7ea9e-171">With</span></span>                 | <span data-ttu-id="7ea9e-172">Tables</span><span class="sxs-lookup"><span data-stu-id="7ea9e-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="7ea9e-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="7ea9e-173">left-aligned column</span></span>  | <span data-ttu-id="7ea9e-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="7ea9e-174">right-aligned column</span></span> | <span data-ttu-id="7ea9e-175">centered column</span><span class="sxs-lookup"><span data-stu-id="7ea9e-175">centered column</span></span> |
| <span data-ttu-id="7ea9e-176">$100</span><span class="sxs-lookup"><span data-stu-id="7ea9e-176">$100</span></span>                 | <span data-ttu-id="7ea9e-177">$100</span><span class="sxs-lookup"><span data-stu-id="7ea9e-177">$100</span></span>                 | <span data-ttu-id="7ea9e-178">$100</span><span class="sxs-lookup"><span data-stu-id="7ea9e-178">$100</span></span>            |
| <span data-ttu-id="7ea9e-179">$10</span><span class="sxs-lookup"><span data-stu-id="7ea9e-179">$10</span></span>                  | <span data-ttu-id="7ea9e-180">$10</span><span class="sxs-lookup"><span data-stu-id="7ea9e-180">$10</span></span>                  | <span data-ttu-id="7ea9e-181">$10</span><span class="sxs-lookup"><span data-stu-id="7ea9e-181">$10</span></span>             |
| <span data-ttu-id="7ea9e-182">$1</span><span class="sxs-lookup"><span data-stu-id="7ea9e-182">$1</span></span>                   | <span data-ttu-id="7ea9e-183">$1</span><span class="sxs-lookup"><span data-stu-id="7ea9e-183">$1</span></span>                   | <span data-ttu-id="7ea9e-184">$1</span><span class="sxs-lookup"><span data-stu-id="7ea9e-184">$1</span></span>              |

<span data-ttu-id="7ea9e-185">Weitere Informationen zum Erstellen von Tabellen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="7ea9e-186">Dem Abschnitt zum [Tabellenumbruchfeature](#table-wrapping) von Markdig, das bei der Formatierung breiter Tabellen hilfreich sein kann</span><span class="sxs-lookup"><span data-stu-id="7ea9e-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="7ea9e-187">[Organizing information with tables (Organisieren von Daten mit Tabellen)](https://help.github.com/articles/organizing-information-with-tables/) von GitHub</span><span class="sxs-lookup"><span data-stu-id="7ea9e-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="7ea9e-188">Der Web-App [Markdown Tables Generator (Markdowntabellengenerator)](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="7ea9e-189">[Adam Pritchard's Markdown Cheatsheet (Cheatsheet für Markdown von Adam Pritchard)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="7ea9e-190">[Michel Fortin's Markdown Extra (Markdown Extra von Michel Fortin)](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="7ea9e-191">[Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="7ea9e-192">Links</span><span class="sxs-lookup"><span data-stu-id="7ea9e-192">Links</span></span>

<span data-ttu-id="7ea9e-193">Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="7ea9e-194">Weitere Informationen zur Verknüpfung finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-194">For more information on linking, see:</span></span>

- <span data-ttu-id="7ea9e-195">Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="7ea9e-196">Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält ausführliche Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="7ea9e-197">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="7ea9e-197">Code snippets</span></span>

<span data-ttu-id="7ea9e-198">Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="7ea9e-199">Nähere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-199">For details, see:</span></span>

- <span data-ttu-id="7ea9e-200">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="7ea9e-201">[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="7ea9e-202">Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="7ea9e-203">Das allgemeine Format für umzäunte Codeblöcke ist:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="7ea9e-204">Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="7ea9e-205">Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="7ea9e-206">Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="7ea9e-207">Name</span><span class="sxs-lookup"><span data-stu-id="7ea9e-207">Name</span></span>|<span data-ttu-id="7ea9e-208">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="7ea9e-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="7ea9e-209">.NET-Konsole</span><span class="sxs-lookup"><span data-stu-id="7ea9e-209">.NET Console</span></span>|<span data-ttu-id="7ea9e-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="7ea9e-210">dotnetcli</span></span>|
|<span data-ttu-id="7ea9e-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-211">ASP.NET (C#)</span></span>|<span data-ttu-id="7ea9e-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="7ea9e-212">aspx-csharp</span></span>|
|<span data-ttu-id="7ea9e-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-213">ASP.NET (VB)</span></span>|<span data-ttu-id="7ea9e-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="7ea9e-214">aspx-vb</span></span>|
|<span data-ttu-id="7ea9e-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="7ea9e-215">AzCopy</span></span>|<span data-ttu-id="7ea9e-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="7ea9e-216">azcopy</span></span>|
|<span data-ttu-id="7ea9e-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="7ea9e-217">Azure CLI</span></span>|<span data-ttu-id="7ea9e-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="7ea9e-218">azurecli</span></span>|
|<span data-ttu-id="7ea9e-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ea9e-219">Azure PowerShell</span></span>|<span data-ttu-id="7ea9e-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="7ea9e-220">azurepowershell</span></span>|
|<span data-ttu-id="7ea9e-221">C++</span><span class="sxs-lookup"><span data-stu-id="7ea9e-221">C++</span></span>|<span data-ttu-id="7ea9e-222">cpp</span><span class="sxs-lookup"><span data-stu-id="7ea9e-222">cpp</span></span>|
|<span data-ttu-id="7ea9e-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="7ea9e-223">C++/CX</span></span>|<span data-ttu-id="7ea9e-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="7ea9e-224">cppcx</span></span>|
|<span data-ttu-id="7ea9e-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="7ea9e-225">C++/WinRT</span></span>|<span data-ttu-id="7ea9e-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="7ea9e-226">cppwinrt</span></span>|
|<span data-ttu-id="7ea9e-227">C#</span><span class="sxs-lookup"><span data-stu-id="7ea9e-227">C#</span></span>|<span data-ttu-id="7ea9e-228">csharp</span><span class="sxs-lookup"><span data-stu-id="7ea9e-228">csharp</span></span>|
|<span data-ttu-id="7ea9e-229">C# im Browser</span><span class="sxs-lookup"><span data-stu-id="7ea9e-229">C# in browser</span></span>|<span data-ttu-id="7ea9e-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="7ea9e-230">csharp-interactive</span></span>|
|<span data-ttu-id="7ea9e-231">Konsole</span><span class="sxs-lookup"><span data-stu-id="7ea9e-231">Console</span></span>|<span data-ttu-id="7ea9e-232">console</span><span class="sxs-lookup"><span data-stu-id="7ea9e-232">console</span></span>|
|<span data-ttu-id="7ea9e-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="7ea9e-233">CSHTML</span></span>|<span data-ttu-id="7ea9e-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="7ea9e-234">cshtml</span></span>|
|<span data-ttu-id="7ea9e-235">DAX</span><span class="sxs-lookup"><span data-stu-id="7ea9e-235">DAX</span></span>|<span data-ttu-id="7ea9e-236">dax</span><span class="sxs-lookup"><span data-stu-id="7ea9e-236">dax</span></span>|
|<span data-ttu-id="7ea9e-237">F#</span><span class="sxs-lookup"><span data-stu-id="7ea9e-237">F#</span></span>|<span data-ttu-id="7ea9e-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="7ea9e-238">fsharp</span></span>|
|<span data-ttu-id="7ea9e-239">Go</span><span class="sxs-lookup"><span data-stu-id="7ea9e-239">Go</span></span>|<span data-ttu-id="7ea9e-240">go</span><span class="sxs-lookup"><span data-stu-id="7ea9e-240">go</span></span>|
|<span data-ttu-id="7ea9e-241">HTML</span><span class="sxs-lookup"><span data-stu-id="7ea9e-241">HTML</span></span>|<span data-ttu-id="7ea9e-242">html</span><span class="sxs-lookup"><span data-stu-id="7ea9e-242">html</span></span>|
|<span data-ttu-id="7ea9e-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="7ea9e-243">HTTP</span></span>|<span data-ttu-id="7ea9e-244">http</span><span class="sxs-lookup"><span data-stu-id="7ea9e-244">http</span></span>|
|<span data-ttu-id="7ea9e-245">Java</span><span class="sxs-lookup"><span data-stu-id="7ea9e-245">Java</span></span>|<span data-ttu-id="7ea9e-246">java</span><span class="sxs-lookup"><span data-stu-id="7ea9e-246">java</span></span>|
|<span data-ttu-id="7ea9e-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7ea9e-247">JavaScript</span></span>|<span data-ttu-id="7ea9e-248">javascript</span><span class="sxs-lookup"><span data-stu-id="7ea9e-248">javascript</span></span>|
|<span data-ttu-id="7ea9e-249">JSON</span><span class="sxs-lookup"><span data-stu-id="7ea9e-249">JSON</span></span>|<span data-ttu-id="7ea9e-250">json</span><span class="sxs-lookup"><span data-stu-id="7ea9e-250">json</span></span>|
|<span data-ttu-id="7ea9e-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="7ea9e-251">Markdown</span></span>|<span data-ttu-id="7ea9e-252">md</span><span class="sxs-lookup"><span data-stu-id="7ea9e-252">md</span></span>|
|<span data-ttu-id="7ea9e-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="7ea9e-253">NodeJS</span></span>|<span data-ttu-id="7ea9e-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="7ea9e-254">nodejs</span></span>|
|<span data-ttu-id="7ea9e-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="7ea9e-255">Objective-C</span></span>|<span data-ttu-id="7ea9e-256">objc</span><span class="sxs-lookup"><span data-stu-id="7ea9e-256">objc</span></span>|
|<span data-ttu-id="7ea9e-257">OData</span><span class="sxs-lookup"><span data-stu-id="7ea9e-257">OData</span></span>|<span data-ttu-id="7ea9e-258">odata</span><span class="sxs-lookup"><span data-stu-id="7ea9e-258">odata</span></span>|
|<span data-ttu-id="7ea9e-259">PHP</span><span class="sxs-lookup"><span data-stu-id="7ea9e-259">PHP</span></span>|<span data-ttu-id="7ea9e-260">php</span><span class="sxs-lookup"><span data-stu-id="7ea9e-260">php</span></span>|
|<span data-ttu-id="7ea9e-261">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="7ea9e-261">Power Apps Formula</span></span>|<span data-ttu-id="7ea9e-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="7ea9e-262">powerappsfl</span></span>|
|<span data-ttu-id="7ea9e-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ea9e-263">PowerShell</span></span>|<span data-ttu-id="7ea9e-264">powershell</span><span class="sxs-lookup"><span data-stu-id="7ea9e-264">powershell</span></span>|
|<span data-ttu-id="7ea9e-265">Python</span><span class="sxs-lookup"><span data-stu-id="7ea9e-265">Python</span></span>|<span data-ttu-id="7ea9e-266">python</span><span class="sxs-lookup"><span data-stu-id="7ea9e-266">python</span></span>|
|<span data-ttu-id="7ea9e-267">Q#</span><span class="sxs-lookup"><span data-stu-id="7ea9e-267">Q#</span></span>|<span data-ttu-id="7ea9e-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="7ea9e-268">qsharp</span></span>|
|<span data-ttu-id="7ea9e-269">R</span><span class="sxs-lookup"><span data-stu-id="7ea9e-269">R</span></span>|<span data-ttu-id="7ea9e-270">r</span><span class="sxs-lookup"><span data-stu-id="7ea9e-270">r</span></span>|
|<span data-ttu-id="7ea9e-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="7ea9e-271">Ruby</span></span>|<span data-ttu-id="7ea9e-272">ruby</span><span class="sxs-lookup"><span data-stu-id="7ea9e-272">ruby</span></span>|
|<span data-ttu-id="7ea9e-273">SQL</span><span class="sxs-lookup"><span data-stu-id="7ea9e-273">SQL</span></span>|<span data-ttu-id="7ea9e-274">sql</span><span class="sxs-lookup"><span data-stu-id="7ea9e-274">sql</span></span>|
|<span data-ttu-id="7ea9e-275">Swift</span><span class="sxs-lookup"><span data-stu-id="7ea9e-275">Swift</span></span>|<span data-ttu-id="7ea9e-276">swift</span><span class="sxs-lookup"><span data-stu-id="7ea9e-276">swift</span></span>|
|<span data-ttu-id="7ea9e-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="7ea9e-277">TypeScript</span></span>|<span data-ttu-id="7ea9e-278">typescript</span><span class="sxs-lookup"><span data-stu-id="7ea9e-278">typescript</span></span>|
|<span data-ttu-id="7ea9e-279">VB</span><span class="sxs-lookup"><span data-stu-id="7ea9e-279">VB</span></span>|<span data-ttu-id="7ea9e-280">vb</span><span class="sxs-lookup"><span data-stu-id="7ea9e-280">vb</span></span>|
|<span data-ttu-id="7ea9e-281">VSTS-CLI</span><span class="sxs-lookup"><span data-stu-id="7ea9e-281">VSTS CLI</span></span>|<span data-ttu-id="7ea9e-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="7ea9e-282">vstscli</span></span>|
|<span data-ttu-id="7ea9e-283">XAML</span><span class="sxs-lookup"><span data-stu-id="7ea9e-283">XAML</span></span>|<span data-ttu-id="7ea9e-284">xaml</span><span class="sxs-lookup"><span data-stu-id="7ea9e-284">xaml</span></span>|
|<span data-ttu-id="7ea9e-285">XML</span><span class="sxs-lookup"><span data-stu-id="7ea9e-285">XML</span></span>|<span data-ttu-id="7ea9e-286">xml</span><span class="sxs-lookup"><span data-stu-id="7ea9e-286">xml</span></span>|

<span data-ttu-id="7ea9e-287">Die Markdownbezeichnung `csharp-interactive` gibt C# als Sprache an. Die Beispiele können über den Browser ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="7ea9e-288">Diese Ausschnitt werden in einem Docker-Container kompiliert und ausgeführt. Die Ergebnisse dieser Ausführung werden im Browserfenster des Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="7ea9e-289">Beispiel: C\#</span><span class="sxs-lookup"><span data-stu-id="7ea9e-289">Example: C\#</span></span>

<span data-ttu-id="7ea9e-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7ea9e-290">__Markdown__</span></span>

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

<span data-ttu-id="7ea9e-291">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="7ea9e-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="7ea9e-292">Beispiel: SQL</span><span class="sxs-lookup"><span data-stu-id="7ea9e-292">Example: SQL</span></span>

<span data-ttu-id="7ea9e-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7ea9e-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="7ea9e-294">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="7ea9e-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="7ea9e-295">OPS: benutzerdefinierte Markdownerweiterungen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="7ea9e-296">In Open Publishing Services (OPS) ist der Markdig-Parser für Markdown implementiert, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="7ea9e-297">Markdig fügt Funktionen über Markuperweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="7ea9e-298">Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="7ea9e-299">(Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="7ea9e-300">GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="7ea9e-301">Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="7ea9e-302">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="7ea9e-302">Note blocks</span></span>
- <span data-ttu-id="7ea9e-303">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-303">Includes</span></span>
- <span data-ttu-id="7ea9e-304">Selektoren</span><span class="sxs-lookup"><span data-stu-id="7ea9e-304">Selectors</span></span>
- <span data-ttu-id="7ea9e-305">Eingebettete Videos</span><span class="sxs-lookup"><span data-stu-id="7ea9e-305">Embedded videos</span></span>
- <span data-ttu-id="7ea9e-306">Codeausschnitte/-beispiele</span><span class="sxs-lookup"><span data-stu-id="7ea9e-306">Code snippets/samples</span></span>

<span data-ttu-id="7ea9e-307">Die vollständige Liste finden Sie unter „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="7ea9e-308">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="7ea9e-308">Note blocks</span></span>

<span data-ttu-id="7ea9e-309">Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="7ea9e-310">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="7ea9e-310">NOTE</span></span>
- <span data-ttu-id="7ea9e-311">WARNUNG</span><span class="sxs-lookup"><span data-stu-id="7ea9e-311">WARNING</span></span>
- <span data-ttu-id="7ea9e-312">TIPP</span><span class="sxs-lookup"><span data-stu-id="7ea9e-312">TIP</span></span>
- <span data-ttu-id="7ea9e-313">WICHTIG</span><span class="sxs-lookup"><span data-stu-id="7ea9e-313">IMPORTANT</span></span>

<span data-ttu-id="7ea9e-314">Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="7ea9e-315">Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="7ea9e-316">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-316">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="7ea9e-317">Diese werden wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="7ea9e-318">This is a NOTE</span><span class="sxs-lookup"><span data-stu-id="7ea9e-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="7ea9e-319">This is a WARNING</span><span class="sxs-lookup"><span data-stu-id="7ea9e-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="7ea9e-320">This is a TIP</span><span class="sxs-lookup"><span data-stu-id="7ea9e-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ea9e-321">This is IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="7ea9e-321">This is IMPORTANT</span></span>

### <a name="includes"></a><span data-ttu-id="7ea9e-322">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-322">Includes</span></span>

<span data-ttu-id="7ea9e-323">Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="7ea9e-324">Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="7ea9e-325">Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Einbeziehungstypen verwenden:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-325">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="7ea9e-326">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="7ea9e-327">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="7ea9e-328">Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="7ea9e-329">Inline- oder Blockeinbeziehungen sind einfache Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9e-329">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="7ea9e-330">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="7ea9e-331">Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="7ea9e-332">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="7ea9e-333">Die Anforderungen und Überlegungen zu Einbeziehungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-333">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="7ea9e-334">Verwenden Sie stets dann Einbeziehungen, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-334">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="7ea9e-335">Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-335">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="7ea9e-336">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="7ea9e-337">Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-337">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="7ea9e-338">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="7ea9e-339">Stellen Sie sicher, dass sämtlicher Text in einer Einbeziehung in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Einbeziehung verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-339">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="7ea9e-340">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="7ea9e-341">Betten Sie keine Einbeziehungen in andere Einbeziehungen ein.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-341">Don't embed includes within other includes.</span></span> <span data-ttu-id="7ea9e-342">Sie werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-342">They are not supported.</span></span>
- <span data-ttu-id="7ea9e-343">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media).</span><span class="sxs-lookup"><span data-stu-id="7ea9e-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="7ea9e-344">Der Stamm des Medienverzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="7ea9e-345">Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-345">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="7ea9e-346">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="7ea9e-347">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-347">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="7ea9e-348">Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-348">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="7ea9e-349">Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-349">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="7ea9e-350">Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-350">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="7ea9e-351">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="7ea9e-352">Selektoren</span><span class="sxs-lookup"><span data-stu-id="7ea9e-352">Selectors</span></span>

<span data-ttu-id="7ea9e-353">Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="7ea9e-354">Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="7ea9e-355">Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="7ea9e-356">Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Einbeziehung platzieren.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="7ea9e-357">Dann können Sie auf diese Einbeziehung in allen Artikeln, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-357">Then you can reference that include in all your articles that use the same selector.</span></span>

<span data-ttu-id="7ea9e-358">Hier ist ein Beispielselektor dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="7ea9e-359">In der [Azure-Dokumentation](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) können Sie sich die Selektoren in Aktion ansehen.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-includes"></a><span data-ttu-id="7ea9e-360">Einschließen von Code</span><span class="sxs-lookup"><span data-stu-id="7ea9e-360">Code includes</span></span>

<span data-ttu-id="7ea9e-361">Markdig unterstützt über die Codeausschnitterweiterung die erweiterte Einbeziehung von Code in einen Artikel.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="7ea9e-362">DFM bietet erweitertes Rendern, das auf GFM-Funktionen wie Programmieren der Sprachauswahl und farbiger Syntaxmarkierung sowie netten Funktionen wie den folgenden basiert:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="7ea9e-363">Einbeziehung zentralisierter Codebeispiele bzw. -ausschnitte aus einem externen Repository</span><span class="sxs-lookup"><span data-stu-id="7ea9e-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="7ea9e-364">Benutzeroberfläche mit Registerkarten zur Anzeige mehrerer Versionen von Codebeispielen in verschiedenen Sprachen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="7ea9e-365">Häufige Fehler und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="7ea9e-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="7ea9e-366">Alternativtext</span><span class="sxs-lookup"><span data-stu-id="7ea9e-366">Alt text</span></span>

<span data-ttu-id="7ea9e-367">Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="7ea9e-368">Verwenden Sie beispielsweise anstelle von</span><span class="sxs-lookup"><span data-stu-id="7ea9e-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="7ea9e-369">diese Möglichkeit zur Umgehung von Unterstrichen:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="7ea9e-370">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="7ea9e-371">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="7ea9e-372">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="7ea9e-373">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="7ea9e-374">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="7ea9e-375">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="7ea9e-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="7ea9e-376">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="7ea9e-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="7ea9e-377">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="7ea9e-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="7ea9e-378">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="7ea9e-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="7ea9e-379">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="7ea9e-379">Angle brackets</span></span>

<span data-ttu-id="7ea9e-380">Spitze Klammern werden häufig zum Kennzeichnen eines Platzhalters verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="7ea9e-381">Wenn Sie dies im Text nutzen (nicht im Code), müssen Sie die spitzen Klammern codieren.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="7ea9e-382">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="7ea9e-383">Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="7ea9e-384">Siehe auch:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="7ea9e-385">Markdownressourcen</span><span class="sxs-lookup"><span data-stu-id="7ea9e-385">Markdown resources</span></span>

- <span data-ttu-id="7ea9e-386">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="7ea9e-387">Cheatsheet zur Markdown-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7ea9e-387">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="7ea9e-388">[Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="7ea9e-388">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- [<span data-ttu-id="7ea9e-389">The Markdown Guide (Das Markdown-Handbuch)</span><span class="sxs-lookup"><span data-stu-id="7ea9e-389">The Markdown Guide</span></span>](https://www.markdownguide.org/)
