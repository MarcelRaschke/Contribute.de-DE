---
title: Verwenden von Markdown für das Schreiben von Dokumentationsartikeln
description: Dieser Artikel enthält grundlegende Informationen und Verweise zu Markdown, das als Sprache zum Schreiben von docs.microsoft.com-Artikeln verwendet wird.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 1f43cecb450c988e4f546aa5ecc5907061521f34
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188284"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="82e1a-103">Verwenden von Markdown für das Schreiben von Dokumentationsartikeln</span><span class="sxs-lookup"><span data-stu-id="82e1a-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="82e1a-104">Artikel auf [docs.microsoft.com](https://docs.microsoft.com) sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="82e1a-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="82e1a-105">Darum ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="82e1a-106">Die „docs.microsoft.com“-Website verwendet die [Markdig-Variante](#markdown-flavor) von Markdown.</span><span class="sxs-lookup"><span data-stu-id="82e1a-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="82e1a-107">Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="82e1a-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="82e1a-108">Überschriften</span><span class="sxs-lookup"><span data-stu-id="82e1a-108">Headings</span></span>

<span data-ttu-id="82e1a-109">Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="82e1a-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="82e1a-110">Überschriften sollten im ATX-Format verfasst werden. Verwenden Sie also 1–6 Rautezeichen (#) am Anfang der Zeile, um eine Überschrift zu kennzeichnen. Diese entsprechen den HTML-Überschriftenebenen H1 bis H6.</span><span class="sxs-lookup"><span data-stu-id="82e1a-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="82e1a-111">Oben sehen Sie Beispiele für Überschriften von der ersten bis zur vierten Ebene.</span><span class="sxs-lookup"><span data-stu-id="82e1a-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="82e1a-112">Es darf **nur eine** Überschrift auf der ersten Ebene (H1) in Ihrem Artikel geben. Diese wird als Titel der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="82e1a-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="82e1a-113">Wenn Ihre Überschrift auf `#` endet, müssen Sie ein weiteres `#`-Zeichen hinzufügen, damit der Titel ordnungsgemäß gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="82e1a-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="82e1a-114">Beispiel: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="82e1a-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="82e1a-115">Überschriften auf der zweiten Ebene generieren das Inhaltsverzeichnis auf der Seite, das unter „In diesem Artikel“ neben dem Titel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="82e1a-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="82e1a-116">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="82e1a-116">Bold and italic text</span></span>

<span data-ttu-id="82e1a-117">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="82e1a-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="82e1a-118">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="82e1a-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="82e1a-119">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="82e1a-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="82e1a-120">Blockzitate</span><span class="sxs-lookup"><span data-stu-id="82e1a-120">Blockquotes</span></span>

<span data-ttu-id="82e1a-121">Blockzitate werden mit dem `>`-Zeichen generiert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="82e1a-122">Das vorherige Beispiel wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="82e1a-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="82e1a-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="82e1a-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="82e1a-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="82e1a-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="82e1a-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="82e1a-126">Listen</span><span class="sxs-lookup"><span data-stu-id="82e1a-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="82e1a-127">Ungeordnete Liste</span><span class="sxs-lookup"><span data-stu-id="82e1a-127">Unordered list</span></span>

<span data-ttu-id="82e1a-128">Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="82e1a-129">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="82e1a-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="82e1a-130">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-130">will be rendered as:</span></span>

- <span data-ttu-id="82e1a-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="82e1a-131">List item 1</span></span>
- <span data-ttu-id="82e1a-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="82e1a-132">List item 2</span></span>
- <span data-ttu-id="82e1a-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="82e1a-133">List item 3</span></span>

<span data-ttu-id="82e1a-134">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="82e1a-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="82e1a-135">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="82e1a-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="82e1a-136">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-136">will be rendered as:</span></span>

- <span data-ttu-id="82e1a-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="82e1a-137">List item 1</span></span>
  - <span data-ttu-id="82e1a-138">List item A</span><span class="sxs-lookup"><span data-stu-id="82e1a-138">List item A</span></span>
  - <span data-ttu-id="82e1a-139">List item B</span><span class="sxs-lookup"><span data-stu-id="82e1a-139">List item B</span></span>
- <span data-ttu-id="82e1a-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="82e1a-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="82e1a-141">Geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="82e1a-141">Ordered list</span></span>

<span data-ttu-id="82e1a-142">Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="82e1a-143">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="82e1a-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="82e1a-144">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-144">will be rendered as:</span></span>

1. <span data-ttu-id="82e1a-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-145">First instruction</span></span>
2. <span data-ttu-id="82e1a-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-146">Second instruction</span></span>
3. <span data-ttu-id="82e1a-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-147">Third instruction</span></span>

<span data-ttu-id="82e1a-148">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="82e1a-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="82e1a-149">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="82e1a-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="82e1a-150">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-150">will be rendered as:</span></span>

1. <span data-ttu-id="82e1a-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-151">First instruction</span></span>
   1. <span data-ttu-id="82e1a-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-152">Sub-instruction</span></span>
   2. <span data-ttu-id="82e1a-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-153">Sub-instruction</span></span>
2. <span data-ttu-id="82e1a-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="82e1a-154">Second instruction</span></span>

<span data-ttu-id="82e1a-155">Wir haben für alle Einträge</span><span class="sxs-lookup"><span data-stu-id="82e1a-155">Note that we use '1.'</span></span> <span data-ttu-id="82e1a-156">„1.“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="82e1a-156">for all entries.</span></span> <span data-ttu-id="82e1a-157">Dadurch ist es leichter, Änderungen zu prüfen, wenn durch diese Schritte hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="82e1a-158">Tables</span><span class="sxs-lookup"><span data-stu-id="82e1a-158">Tables</span></span>

<span data-ttu-id="82e1a-159">Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="82e1a-160">Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="82e1a-161">Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="82e1a-162">Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="82e1a-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="82e1a-163">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="82e1a-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="82e1a-164">folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-164">Will be rendered as:</span></span>

| <span data-ttu-id="82e1a-165">Fun</span><span class="sxs-lookup"><span data-stu-id="82e1a-165">Fun</span></span>                  | <span data-ttu-id="82e1a-166">With</span><span class="sxs-lookup"><span data-stu-id="82e1a-166">With</span></span>                 | <span data-ttu-id="82e1a-167">Tables</span><span class="sxs-lookup"><span data-stu-id="82e1a-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="82e1a-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="82e1a-168">left-aligned column</span></span>  | <span data-ttu-id="82e1a-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="82e1a-169">right-aligned column</span></span> | <span data-ttu-id="82e1a-170">centered column</span><span class="sxs-lookup"><span data-stu-id="82e1a-170">centered column</span></span> |
| <span data-ttu-id="82e1a-171">$100</span><span class="sxs-lookup"><span data-stu-id="82e1a-171">$100</span></span>                 | <span data-ttu-id="82e1a-172">$100</span><span class="sxs-lookup"><span data-stu-id="82e1a-172">$100</span></span>                 | <span data-ttu-id="82e1a-173">$100</span><span class="sxs-lookup"><span data-stu-id="82e1a-173">$100</span></span>            |
| <span data-ttu-id="82e1a-174">$10</span><span class="sxs-lookup"><span data-stu-id="82e1a-174">$10</span></span>                  | <span data-ttu-id="82e1a-175">$10</span><span class="sxs-lookup"><span data-stu-id="82e1a-175">$10</span></span>                  | <span data-ttu-id="82e1a-176">$10</span><span class="sxs-lookup"><span data-stu-id="82e1a-176">$10</span></span>             |
| <span data-ttu-id="82e1a-177">$1</span><span class="sxs-lookup"><span data-stu-id="82e1a-177">$1</span></span>                   | <span data-ttu-id="82e1a-178">$1</span><span class="sxs-lookup"><span data-stu-id="82e1a-178">$1</span></span>                   | <span data-ttu-id="82e1a-179">$1</span><span class="sxs-lookup"><span data-stu-id="82e1a-179">$1</span></span>              |

<span data-ttu-id="82e1a-180">Weitere Informationen zum Erstellen von Tabellen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="82e1a-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="82e1a-181">[Organizing information with tables (Organisieren von Daten mit Tabellen)](https://help.github.com/articles/organizing-information-with-tables/) von GitHub</span><span class="sxs-lookup"><span data-stu-id="82e1a-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="82e1a-182">Der Web-App [Markdown Tables Generator (Markdowntabellengenerator)](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="82e1a-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="82e1a-183">[Adam Pritchard's Markdown Cheatsheet (Cheatsheet für Markdown von Adam Pritchard)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="82e1a-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="82e1a-184">[Michel Fortin's Markdown Extra (Markdown Extra von Michel Fortin)](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="82e1a-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="82e1a-185">[Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="82e1a-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="82e1a-186">Links</span><span class="sxs-lookup"><span data-stu-id="82e1a-186">Links</span></span>

<span data-ttu-id="82e1a-187">Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:</span><span class="sxs-lookup"><span data-stu-id="82e1a-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="82e1a-188">Weitere Informationen zur Verknüpfung finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="82e1a-188">For more information on linking, see:</span></span>

- <span data-ttu-id="82e1a-189">Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.</span><span class="sxs-lookup"><span data-stu-id="82e1a-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="82e1a-190">Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält ausführliche Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.</span><span class="sxs-lookup"><span data-stu-id="82e1a-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="82e1a-191">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="82e1a-191">Code snippets</span></span>

<span data-ttu-id="82e1a-192">Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="82e1a-193">Nähere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="82e1a-193">For details, see:</span></span>

- <span data-ttu-id="82e1a-194">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)</span><span class="sxs-lookup"><span data-stu-id="82e1a-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="82e1a-195">[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)</span><span class="sxs-lookup"><span data-stu-id="82e1a-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="82e1a-196">Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82e1a-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="82e1a-197">Das allgemeine Format für umzäunte Codeblöcke ist:</span><span class="sxs-lookup"><span data-stu-id="82e1a-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="82e1a-198">Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="82e1a-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="82e1a-199">Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:</span><span class="sxs-lookup"><span data-stu-id="82e1a-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="82e1a-200">Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="82e1a-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="82e1a-201">Name</span><span class="sxs-lookup"><span data-stu-id="82e1a-201">Name</span></span>|<span data-ttu-id="82e1a-202">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="82e1a-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="82e1a-203">.NET-Konsole</span><span class="sxs-lookup"><span data-stu-id="82e1a-203">.NET Console</span></span>|<span data-ttu-id="82e1a-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="82e1a-204">dotnetcli</span></span>|
|<span data-ttu-id="82e1a-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="82e1a-205">ASP.NET (C#)</span></span>|<span data-ttu-id="82e1a-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="82e1a-206">aspx-csharp</span></span>|
|<span data-ttu-id="82e1a-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="82e1a-207">ASP.NET (VB)</span></span>|<span data-ttu-id="82e1a-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="82e1a-208">aspx-vb</span></span>|
|<span data-ttu-id="82e1a-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="82e1a-209">AzCopy</span></span>|<span data-ttu-id="82e1a-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="82e1a-210">azcopy</span></span>|
|<span data-ttu-id="82e1a-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="82e1a-211">Azure CLI</span></span>|<span data-ttu-id="82e1a-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="82e1a-212">azurecli</span></span>|
|<span data-ttu-id="82e1a-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="82e1a-213">Azure PowerShell</span></span>|<span data-ttu-id="82e1a-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="82e1a-214">azurepowershell</span></span>|
|<span data-ttu-id="82e1a-215">Bash</span><span class="sxs-lookup"><span data-stu-id="82e1a-215">Bash</span></span>|<span data-ttu-id="82e1a-216">bash</span><span class="sxs-lookup"><span data-stu-id="82e1a-216">bash</span></span>|
|<span data-ttu-id="82e1a-217">C++</span><span class="sxs-lookup"><span data-stu-id="82e1a-217">C++</span></span>|<span data-ttu-id="82e1a-218">cpp</span><span class="sxs-lookup"><span data-stu-id="82e1a-218">cpp</span></span>|
|<span data-ttu-id="82e1a-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="82e1a-219">C++/CX</span></span>|<span data-ttu-id="82e1a-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="82e1a-220">cppcx</span></span>|
|<span data-ttu-id="82e1a-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="82e1a-221">C++/WinRT</span></span>|<span data-ttu-id="82e1a-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="82e1a-222">cppwinrt</span></span>|
|<span data-ttu-id="82e1a-223">C#</span><span class="sxs-lookup"><span data-stu-id="82e1a-223">C#</span></span>|<span data-ttu-id="82e1a-224">csharp</span><span class="sxs-lookup"><span data-stu-id="82e1a-224">csharp</span></span>|
|<span data-ttu-id="82e1a-225">C# im Browser</span><span class="sxs-lookup"><span data-stu-id="82e1a-225">C# in browser</span></span>|<span data-ttu-id="82e1a-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="82e1a-226">csharp-interactive</span></span>|
|<span data-ttu-id="82e1a-227">Konsole</span><span class="sxs-lookup"><span data-stu-id="82e1a-227">Console</span></span>|<span data-ttu-id="82e1a-228">console</span><span class="sxs-lookup"><span data-stu-id="82e1a-228">console</span></span>|
|<span data-ttu-id="82e1a-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="82e1a-229">CSHTML</span></span>|<span data-ttu-id="82e1a-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="82e1a-230">cshtml</span></span>|
|<span data-ttu-id="82e1a-231">DAX</span><span class="sxs-lookup"><span data-stu-id="82e1a-231">DAX</span></span>|<span data-ttu-id="82e1a-232">dax</span><span class="sxs-lookup"><span data-stu-id="82e1a-232">dax</span></span>|
|<span data-ttu-id="82e1a-233">Docker</span><span class="sxs-lookup"><span data-stu-id="82e1a-233">Docker</span></span>|<span data-ttu-id="82e1a-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="82e1a-234">dockerfile</span></span>|
|<span data-ttu-id="82e1a-235">F#</span><span class="sxs-lookup"><span data-stu-id="82e1a-235">F#</span></span>|<span data-ttu-id="82e1a-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="82e1a-236">fsharp</span></span>|
|<span data-ttu-id="82e1a-237">Go</span><span class="sxs-lookup"><span data-stu-id="82e1a-237">Go</span></span>|<span data-ttu-id="82e1a-238">go</span><span class="sxs-lookup"><span data-stu-id="82e1a-238">go</span></span>|
|<span data-ttu-id="82e1a-239">HTML</span><span class="sxs-lookup"><span data-stu-id="82e1a-239">HTML</span></span>|<span data-ttu-id="82e1a-240">html</span><span class="sxs-lookup"><span data-stu-id="82e1a-240">html</span></span>|
|<span data-ttu-id="82e1a-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="82e1a-241">HTTP</span></span>|<span data-ttu-id="82e1a-242">http</span><span class="sxs-lookup"><span data-stu-id="82e1a-242">http</span></span>|
|<span data-ttu-id="82e1a-243">Java</span><span class="sxs-lookup"><span data-stu-id="82e1a-243">Java</span></span>|<span data-ttu-id="82e1a-244">java</span><span class="sxs-lookup"><span data-stu-id="82e1a-244">java</span></span>|
|<span data-ttu-id="82e1a-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="82e1a-245">JavaScript</span></span>|<span data-ttu-id="82e1a-246">javascript</span><span class="sxs-lookup"><span data-stu-id="82e1a-246">javascript</span></span>|
|<span data-ttu-id="82e1a-247">JSON</span><span class="sxs-lookup"><span data-stu-id="82e1a-247">JSON</span></span>|<span data-ttu-id="82e1a-248">json</span><span class="sxs-lookup"><span data-stu-id="82e1a-248">json</span></span>|
|<span data-ttu-id="82e1a-249">Kusto-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="82e1a-249">Kusto Query Language</span></span>|<span data-ttu-id="82e1a-250">kusto</span><span class="sxs-lookup"><span data-stu-id="82e1a-250">kusto</span></span>|
|<span data-ttu-id="82e1a-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="82e1a-251">Markdown</span></span>|<span data-ttu-id="82e1a-252">md</span><span class="sxs-lookup"><span data-stu-id="82e1a-252">md</span></span>|
|<span data-ttu-id="82e1a-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="82e1a-253">Objective-C</span></span>|<span data-ttu-id="82e1a-254">objc</span><span class="sxs-lookup"><span data-stu-id="82e1a-254">objc</span></span>|
|<span data-ttu-id="82e1a-255">OData</span><span class="sxs-lookup"><span data-stu-id="82e1a-255">OData</span></span>|<span data-ttu-id="82e1a-256">odata</span><span class="sxs-lookup"><span data-stu-id="82e1a-256">odata</span></span>|
|<span data-ttu-id="82e1a-257">PHP</span><span class="sxs-lookup"><span data-stu-id="82e1a-257">PHP</span></span>|<span data-ttu-id="82e1a-258">php</span><span class="sxs-lookup"><span data-stu-id="82e1a-258">php</span></span>|
|<span data-ttu-id="82e1a-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="82e1a-259">protobuf</span></span>|<span data-ttu-id="82e1a-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="82e1a-260">protobuf</span></span>|
|<span data-ttu-id="82e1a-261">PowerApps (Punkt als Dezimaltrennzeichen)</span><span class="sxs-lookup"><span data-stu-id="82e1a-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="82e1a-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="82e1a-262">powerapps-dot</span></span>|
|<span data-ttu-id="82e1a-263">PowerApps (Komma als Dezimaltrennzeichen)</span><span class="sxs-lookup"><span data-stu-id="82e1a-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="82e1a-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="82e1a-264">powerapps-comma</span></span>|
|<span data-ttu-id="82e1a-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="82e1a-265">PowerShell</span></span>|<span data-ttu-id="82e1a-266">powershell</span><span class="sxs-lookup"><span data-stu-id="82e1a-266">powershell</span></span>|
|<span data-ttu-id="82e1a-267">Python</span><span class="sxs-lookup"><span data-stu-id="82e1a-267">Python</span></span>|<span data-ttu-id="82e1a-268">python</span><span class="sxs-lookup"><span data-stu-id="82e1a-268">python</span></span>|
|<span data-ttu-id="82e1a-269">Q#</span><span class="sxs-lookup"><span data-stu-id="82e1a-269">Q#</span></span>|<span data-ttu-id="82e1a-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="82e1a-270">qsharp</span></span>|
|<span data-ttu-id="82e1a-271">R</span><span class="sxs-lookup"><span data-stu-id="82e1a-271">R</span></span>|<span data-ttu-id="82e1a-272">r</span><span class="sxs-lookup"><span data-stu-id="82e1a-272">r</span></span>|
|<span data-ttu-id="82e1a-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="82e1a-273">Ruby</span></span>|<span data-ttu-id="82e1a-274">ruby</span><span class="sxs-lookup"><span data-stu-id="82e1a-274">ruby</span></span>|
|<span data-ttu-id="82e1a-275">SQL</span><span class="sxs-lookup"><span data-stu-id="82e1a-275">SQL</span></span>|<span data-ttu-id="82e1a-276">sql</span><span class="sxs-lookup"><span data-stu-id="82e1a-276">sql</span></span>|
|<span data-ttu-id="82e1a-277">Swift</span><span class="sxs-lookup"><span data-stu-id="82e1a-277">Swift</span></span>|<span data-ttu-id="82e1a-278">swift</span><span class="sxs-lookup"><span data-stu-id="82e1a-278">swift</span></span>|
|<span data-ttu-id="82e1a-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="82e1a-279">TypeScript</span></span>|<span data-ttu-id="82e1a-280">typescript</span><span class="sxs-lookup"><span data-stu-id="82e1a-280">typescript</span></span>|
|<span data-ttu-id="82e1a-281">VB</span><span class="sxs-lookup"><span data-stu-id="82e1a-281">VB</span></span>|<span data-ttu-id="82e1a-282">vb</span><span class="sxs-lookup"><span data-stu-id="82e1a-282">vb</span></span>|
|<span data-ttu-id="82e1a-283">XAML</span><span class="sxs-lookup"><span data-stu-id="82e1a-283">XAML</span></span>|<span data-ttu-id="82e1a-284">xaml</span><span class="sxs-lookup"><span data-stu-id="82e1a-284">xaml</span></span>|
|<span data-ttu-id="82e1a-285">XML</span><span class="sxs-lookup"><span data-stu-id="82e1a-285">XML</span></span>|<span data-ttu-id="82e1a-286">xml</span><span class="sxs-lookup"><span data-stu-id="82e1a-286">xml</span></span>|

<span data-ttu-id="82e1a-287">Die Markdownbezeichnung `csharp-interactive` gibt C# als Sprache an. Die Beispiele können über den Browser ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="82e1a-288">Diese Ausschnitt werden in einem Docker-Container kompiliert und ausgeführt. Die Ergebnisse dieser Ausführung werden im Browserfenster des Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="82e1a-289">Beispiel: C\#</span><span class="sxs-lookup"><span data-stu-id="82e1a-289">Example: C\#</span></span>

<span data-ttu-id="82e1a-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="82e1a-290">__Markdown__</span></span>

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

<span data-ttu-id="82e1a-291">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="82e1a-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="82e1a-292">Beispiel: SQL</span><span class="sxs-lookup"><span data-stu-id="82e1a-292">Example: SQL</span></span>

<span data-ttu-id="82e1a-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="82e1a-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="82e1a-294">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="82e1a-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="82e1a-295">Benutzerdefinierte Markdownerweiterungen in Docs</span><span class="sxs-lookup"><span data-stu-id="82e1a-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="82e1a-296">Docs.Microsoft.com (Docs) implementiert einen Markdig-Parser für Markdown, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist.</span><span class="sxs-lookup"><span data-stu-id="82e1a-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="82e1a-297">Markdig fügt Funktionen über Markuperweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="82e1a-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="82e1a-298">Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="82e1a-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="82e1a-299">(Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)</span><span class="sxs-lookup"><span data-stu-id="82e1a-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="82e1a-300">GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="82e1a-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="82e1a-301">Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="82e1a-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="82e1a-302">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="82e1a-302">Note blocks</span></span>
- <span data-ttu-id="82e1a-303">Includedateien</span><span class="sxs-lookup"><span data-stu-id="82e1a-303">Include files</span></span>
- <span data-ttu-id="82e1a-304">Selektoren</span><span class="sxs-lookup"><span data-stu-id="82e1a-304">Selectors</span></span>
- <span data-ttu-id="82e1a-305">Eingebettete Videos</span><span class="sxs-lookup"><span data-stu-id="82e1a-305">Embedded videos</span></span>
- <span data-ttu-id="82e1a-306">Codeausschnitte/-beispiele</span><span class="sxs-lookup"><span data-stu-id="82e1a-306">Code snippets/samples</span></span>

<span data-ttu-id="82e1a-307">Die vollständige Liste finden Sie unter „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="82e1a-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="82e1a-308">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="82e1a-308">Note blocks</span></span>

<span data-ttu-id="82e1a-309">Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:</span><span class="sxs-lookup"><span data-stu-id="82e1a-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="82e1a-310">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="82e1a-310">NOTE</span></span>
- <span data-ttu-id="82e1a-311">WARNUNG</span><span class="sxs-lookup"><span data-stu-id="82e1a-311">WARNING</span></span>
- <span data-ttu-id="82e1a-312">TIPP</span><span class="sxs-lookup"><span data-stu-id="82e1a-312">TIP</span></span>
- <span data-ttu-id="82e1a-313">WICHTIG</span><span class="sxs-lookup"><span data-stu-id="82e1a-313">IMPORTANT</span></span>

<span data-ttu-id="82e1a-314">Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können.</span><span class="sxs-lookup"><span data-stu-id="82e1a-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="82e1a-315">Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="82e1a-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="82e1a-316">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="82e1a-316">Examples:</span></span>

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

<span data-ttu-id="82e1a-317">Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="82e1a-317">These alerts look like this on docs.microsoft.com:</span></span>

![Hier wird dargestellt, wie Warnungen im vorherigen Beispiel auf der veröffentlichten Dokumentationsseite mit unterschiedlichen Symbolen und Farben aussieht.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="82e1a-319">Includedateien</span><span class="sxs-lookup"><span data-stu-id="82e1a-319">Include files</span></span>

<span data-ttu-id="82e1a-320">Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="82e1a-321">Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist.</span><span class="sxs-lookup"><span data-stu-id="82e1a-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="82e1a-322">Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Arten von Includeverweisen verwenden:</span><span class="sxs-lookup"><span data-stu-id="82e1a-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="82e1a-323">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="82e1a-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="82e1a-324">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="82e1a-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="82e1a-325">Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.</span><span class="sxs-lookup"><span data-stu-id="82e1a-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="82e1a-326">Inline- oder Blockincludedateien sind einfache Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="82e1a-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="82e1a-327">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="82e1a-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="82e1a-328">Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="82e1a-329">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="82e1a-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="82e1a-330">Die Anforderungen und Überlegungen zu Includedateien lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="82e1a-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="82e1a-331">Verwenden Sie stets dann eine Includedatei, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="82e1a-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="82e1a-332">Verwenden Sie einen Blockincludeverweis für umfangreiche Inhaltsmengen, d.h. für ein oder zwei Absätze, ein gemeinsames Verfahren oder einen gemeinsamen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="82e1a-333">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="82e1a-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="82e1a-334">Includeverweise werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="82e1a-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="82e1a-335">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="82e1a-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="82e1a-336">Stellen Sie sicher, dass sämtlicher Text in einer Includedatei in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Includedatei verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="82e1a-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="82e1a-337">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="82e1a-338">Betten Sie keine Includeverweise in andere Includedateien ein.</span><span class="sxs-lookup"><span data-stu-id="82e1a-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="82e1a-339">Sie werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-339">They are not supported.</span></span>
- <span data-ttu-id="82e1a-340">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media).</span><span class="sxs-lookup"><span data-stu-id="82e1a-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="82e1a-341">Der Stamm des Medienverzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="82e1a-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="82e1a-342">Wenn die Includedatei keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82e1a-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="82e1a-343">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="82e1a-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="82e1a-344">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Includedatei und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="82e1a-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="82e1a-345">Speichern Sie die Mediendatei in dem Medienordner, der der Includedatei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="82e1a-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="82e1a-346">Verwenden Sie eine Includedatei nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="82e1a-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="82e1a-347">Includedateien sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="82e1a-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="82e1a-348">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82e1a-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="82e1a-349">Selektoren</span><span class="sxs-lookup"><span data-stu-id="82e1a-349">Selectors</span></span>

<span data-ttu-id="82e1a-350">Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="82e1a-351">Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="82e1a-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="82e1a-352">Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="82e1a-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="82e1a-353">Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Includedatei platzieren.</span><span class="sxs-lookup"><span data-stu-id="82e1a-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="82e1a-354">Dann können Sie auf diese Includedatei in allen Artikeln, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="82e1a-355">Hier ist ein Beispielselektor dargestellt:</span><span class="sxs-lookup"><span data-stu-id="82e1a-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="82e1a-356">In der [Azure-Dokumentation](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) können Sie sich die Selektoren in Aktion ansehen.</span><span class="sxs-lookup"><span data-stu-id="82e1a-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="82e1a-357">Codeincludeverweise</span><span class="sxs-lookup"><span data-stu-id="82e1a-357">Code include references</span></span>

<span data-ttu-id="82e1a-358">Markdig unterstützt über die Codeausschnitterweiterung die erweiterte Einbeziehung von Code in einen Artikel.</span><span class="sxs-lookup"><span data-stu-id="82e1a-358">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="82e1a-359">DFM bietet erweitertes Rendern, das auf GFM-Funktionen wie Programmieren der Sprachauswahl und farbiger Syntaxmarkierung sowie netten Funktionen wie den folgenden basiert:</span><span class="sxs-lookup"><span data-stu-id="82e1a-359">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="82e1a-360">Einbeziehung zentralisierter Codebeispiele bzw. -ausschnitte aus einem externen Repository</span><span class="sxs-lookup"><span data-stu-id="82e1a-360">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="82e1a-361">Benutzeroberfläche mit Registerkarten zur Anzeige mehrerer Versionen von Codebeispielen in verschiedenen Sprachen</span><span class="sxs-lookup"><span data-stu-id="82e1a-361">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="82e1a-362">Häufige Fehler und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="82e1a-362">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="82e1a-363">Alternativtext</span><span class="sxs-lookup"><span data-stu-id="82e1a-363">Alt text</span></span>

<span data-ttu-id="82e1a-364">Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert.</span><span class="sxs-lookup"><span data-stu-id="82e1a-364">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="82e1a-365">Verwenden Sie beispielsweise anstelle von</span><span class="sxs-lookup"><span data-stu-id="82e1a-365">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="82e1a-366">diese Möglichkeit zur Umgehung von Unterstrichen:</span><span class="sxs-lookup"><span data-stu-id="82e1a-366">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="82e1a-367">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="82e1a-367">Apostrophes and quotation marks</span></span>

<span data-ttu-id="82e1a-368">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="82e1a-368">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="82e1a-369">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="82e1a-369">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="82e1a-370">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="82e1a-370">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="82e1a-371">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="82e1a-371">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="82e1a-372">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="82e1a-372">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="82e1a-373">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="82e1a-373">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="82e1a-374">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="82e1a-374">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="82e1a-375">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="82e1a-375">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="82e1a-376">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="82e1a-376">Angle brackets</span></span>

<span data-ttu-id="82e1a-377">Spitze Klammern werden häufig zum Kennzeichnen eines Platzhalters verwendet.</span><span class="sxs-lookup"><span data-stu-id="82e1a-377">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="82e1a-378">Wenn Sie dies im Text nutzen (nicht im Code), müssen Sie die spitzen Klammern codieren.</span><span class="sxs-lookup"><span data-stu-id="82e1a-378">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="82e1a-379">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="82e1a-379">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="82e1a-380">Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="82e1a-380">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="82e1a-381">Markdown-Variante</span><span class="sxs-lookup"><span data-stu-id="82e1a-381">Markdown flavor</span></span>

<span data-ttu-id="82e1a-382">Das Back-End der Website „docs.microsoft.com“ unterstützt ein kompatibles [CommonMark](https://commonmark.org/)-Markdown, das von der [Markdig](https://github.com/lunet-io/markdig)-Analyse-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="82e1a-382">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="82e1a-383">Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="82e1a-383">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="82e1a-384">Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="82e1a-384">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="82e1a-385">Siehe auch:</span><span class="sxs-lookup"><span data-stu-id="82e1a-385">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="82e1a-386">Markdownressourcen</span><span class="sxs-lookup"><span data-stu-id="82e1a-386">Markdown resources</span></span>

- <span data-ttu-id="82e1a-387">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)</span><span class="sxs-lookup"><span data-stu-id="82e1a-387">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="82e1a-388">Cheatsheet zur Markdown-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="82e1a-388">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="82e1a-389">[Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="82e1a-389">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- [<span data-ttu-id="82e1a-390">The Markdown Guide (Das Markdown-Handbuch)</span><span class="sxs-lookup"><span data-stu-id="82e1a-390">The Markdown Guide</span></span>](https://www.markdownguide.org/)
