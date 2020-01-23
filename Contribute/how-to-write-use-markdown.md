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
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="bd701-103">Verwenden von Markdown für das Schreiben von Dokumentationsartikeln</span><span class="sxs-lookup"><span data-stu-id="bd701-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="bd701-104">Artikel auf [docs.microsoft.com](https://docs.microsoft.com) sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="bd701-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="bd701-105">Darum ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="bd701-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="bd701-106">Die „docs.microsoft.com“-Website verwendet die [Markdig-Variante](#markdown-flavor) von Markdown.</span><span class="sxs-lookup"><span data-stu-id="bd701-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="bd701-107">Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="bd701-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="bd701-108">Überschriften</span><span class="sxs-lookup"><span data-stu-id="bd701-108">Headings</span></span>

<span data-ttu-id="bd701-109">Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bd701-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="bd701-110">Überschriften sollten im ATX-Format verfasst werden. Verwenden Sie also 1–6 Rautezeichen (#) am Anfang der Zeile, um eine Überschrift zu kennzeichnen. Diese entsprechen den HTML-Überschriftenebenen H1 bis H6.</span><span class="sxs-lookup"><span data-stu-id="bd701-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="bd701-111">Oben sehen Sie Beispiele für Überschriften von der ersten bis zur vierten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bd701-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="bd701-112">Es darf **nur eine** Überschrift auf der ersten Ebene (H1) in Ihrem Artikel geben. Diese wird als Titel der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd701-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="bd701-113">Wenn Ihre Überschrift auf `#` endet, müssen Sie ein weiteres `#`-Zeichen hinzufügen, damit der Titel ordnungsgemäß gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="bd701-114">Beispiel: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="bd701-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="bd701-115">Überschriften auf der zweiten Ebene generieren das Inhaltsverzeichnis auf der Seite, das unter „In diesem Artikel“ neben dem Titel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="bd701-116">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="bd701-116">Bold and italic text</span></span>

<span data-ttu-id="bd701-117">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="bd701-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="bd701-118">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="bd701-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="bd701-119">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="bd701-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="bd701-120">Blockzitate</span><span class="sxs-lookup"><span data-stu-id="bd701-120">Blockquotes</span></span>

<span data-ttu-id="bd701-121">Blockzitate werden mit dem `>`-Zeichen generiert:</span><span class="sxs-lookup"><span data-stu-id="bd701-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="bd701-122">Das vorherige Beispiel wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="bd701-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="bd701-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="bd701-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="bd701-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="bd701-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="bd701-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="bd701-126">Listen</span><span class="sxs-lookup"><span data-stu-id="bd701-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="bd701-127">Ungeordnete Liste</span><span class="sxs-lookup"><span data-stu-id="bd701-127">Unordered list</span></span>

<span data-ttu-id="bd701-128">Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd701-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="bd701-129">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="bd701-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="bd701-130">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-130">will be rendered as:</span></span>

- <span data-ttu-id="bd701-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="bd701-131">List item 1</span></span>
- <span data-ttu-id="bd701-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="bd701-132">List item 2</span></span>
- <span data-ttu-id="bd701-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="bd701-133">List item 3</span></span>

<span data-ttu-id="bd701-134">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="bd701-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="bd701-135">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="bd701-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="bd701-136">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-136">will be rendered as:</span></span>

- <span data-ttu-id="bd701-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="bd701-137">List item 1</span></span>
  - <span data-ttu-id="bd701-138">List item A</span><span class="sxs-lookup"><span data-stu-id="bd701-138">List item A</span></span>
  - <span data-ttu-id="bd701-139">List item B</span><span class="sxs-lookup"><span data-stu-id="bd701-139">List item B</span></span>
- <span data-ttu-id="bd701-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="bd701-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="bd701-141">Geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="bd701-141">Ordered list</span></span>

<span data-ttu-id="bd701-142">Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen.</span><span class="sxs-lookup"><span data-stu-id="bd701-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="bd701-143">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="bd701-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="bd701-144">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-144">will be rendered as:</span></span>

1. <span data-ttu-id="bd701-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-145">First instruction</span></span>
2. <span data-ttu-id="bd701-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-146">Second instruction</span></span>
3. <span data-ttu-id="bd701-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-147">Third instruction</span></span>

<span data-ttu-id="bd701-148">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="bd701-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="bd701-149">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="bd701-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="bd701-150">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-150">will be rendered as:</span></span>

1. <span data-ttu-id="bd701-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-151">First instruction</span></span>
   1. <span data-ttu-id="bd701-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-152">Sub-instruction</span></span>
   2. <span data-ttu-id="bd701-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-153">Sub-instruction</span></span>
2. <span data-ttu-id="bd701-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="bd701-154">Second instruction</span></span>

<span data-ttu-id="bd701-155">Wir haben für alle Einträge</span><span class="sxs-lookup"><span data-stu-id="bd701-155">Note that we use '1.'</span></span> <span data-ttu-id="bd701-156">„1.“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd701-156">for all entries.</span></span> <span data-ttu-id="bd701-157">Dadurch ist es leichter, Änderungen zu prüfen, wenn durch diese Schritte hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="bd701-158">Tables</span><span class="sxs-lookup"><span data-stu-id="bd701-158">Tables</span></span>

<span data-ttu-id="bd701-159">Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd701-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="bd701-160">Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd701-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="bd701-161">Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="bd701-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="bd701-162">Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="bd701-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="bd701-163">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="bd701-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="bd701-164">folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="bd701-164">Will be rendered as:</span></span>

| <span data-ttu-id="bd701-165">Fun</span><span class="sxs-lookup"><span data-stu-id="bd701-165">Fun</span></span>                  | <span data-ttu-id="bd701-166">With</span><span class="sxs-lookup"><span data-stu-id="bd701-166">With</span></span>                 | <span data-ttu-id="bd701-167">Tables</span><span class="sxs-lookup"><span data-stu-id="bd701-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="bd701-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="bd701-168">left-aligned column</span></span>  | <span data-ttu-id="bd701-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="bd701-169">right-aligned column</span></span> | <span data-ttu-id="bd701-170">centered column</span><span class="sxs-lookup"><span data-stu-id="bd701-170">centered column</span></span> |
| <span data-ttu-id="bd701-171">$100</span><span class="sxs-lookup"><span data-stu-id="bd701-171">$100</span></span>                 | <span data-ttu-id="bd701-172">$100</span><span class="sxs-lookup"><span data-stu-id="bd701-172">$100</span></span>                 | <span data-ttu-id="bd701-173">$100</span><span class="sxs-lookup"><span data-stu-id="bd701-173">$100</span></span>            |
| <span data-ttu-id="bd701-174">$10</span><span class="sxs-lookup"><span data-stu-id="bd701-174">$10</span></span>                  | <span data-ttu-id="bd701-175">$10</span><span class="sxs-lookup"><span data-stu-id="bd701-175">$10</span></span>                  | <span data-ttu-id="bd701-176">$10</span><span class="sxs-lookup"><span data-stu-id="bd701-176">$10</span></span>             |
| <span data-ttu-id="bd701-177">$1</span><span class="sxs-lookup"><span data-stu-id="bd701-177">$1</span></span>                   | <span data-ttu-id="bd701-178">$1</span><span class="sxs-lookup"><span data-stu-id="bd701-178">$1</span></span>                   | <span data-ttu-id="bd701-179">$1</span><span class="sxs-lookup"><span data-stu-id="bd701-179">$1</span></span>              |

<span data-ttu-id="bd701-180">Weitere Informationen zum Erstellen von Tabellen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="bd701-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="bd701-181">[Organizing information with tables (Organisieren von Daten mit Tabellen)](https://help.github.com/articles/organizing-information-with-tables/) von GitHub</span><span class="sxs-lookup"><span data-stu-id="bd701-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="bd701-182">Der Web-App [Markdown Tables Generator (Markdowntabellengenerator)](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="bd701-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="bd701-183">[Adam Pritchard's Markdown Cheatsheet (Cheatsheet für Markdown von Adam Pritchard)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="bd701-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="bd701-184">[Michel Fortin's Markdown Extra (Markdown Extra von Michel Fortin)](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="bd701-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="bd701-185">[Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="bd701-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="bd701-186">Links</span><span class="sxs-lookup"><span data-stu-id="bd701-186">Links</span></span>

<span data-ttu-id="bd701-187">Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:</span><span class="sxs-lookup"><span data-stu-id="bd701-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="bd701-188">Weitere Informationen zur Verknüpfung finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="bd701-188">For more information on linking, see:</span></span>

- <span data-ttu-id="bd701-189">Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.</span><span class="sxs-lookup"><span data-stu-id="bd701-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="bd701-190">Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält ausführliche Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.</span><span class="sxs-lookup"><span data-stu-id="bd701-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="bd701-191">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="bd701-191">Code snippets</span></span>

<span data-ttu-id="bd701-192">Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="bd701-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="bd701-193">Nähere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="bd701-193">For details, see:</span></span>

- <span data-ttu-id="bd701-194">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)</span><span class="sxs-lookup"><span data-stu-id="bd701-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="bd701-195">[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)</span><span class="sxs-lookup"><span data-stu-id="bd701-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="bd701-196">Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bd701-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="bd701-197">Das allgemeine Format für umzäunte Codeblöcke ist:</span><span class="sxs-lookup"><span data-stu-id="bd701-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="bd701-198">Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="bd701-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="bd701-199">Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:</span><span class="sxs-lookup"><span data-stu-id="bd701-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="bd701-200">Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="bd701-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="bd701-201">Name</span><span class="sxs-lookup"><span data-stu-id="bd701-201">Name</span></span>|<span data-ttu-id="bd701-202">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="bd701-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="bd701-203">.NET-Konsole</span><span class="sxs-lookup"><span data-stu-id="bd701-203">.NET Console</span></span>|<span data-ttu-id="bd701-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="bd701-204">dotnetcli</span></span>|
|<span data-ttu-id="bd701-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="bd701-205">ASP.NET (C#)</span></span>|<span data-ttu-id="bd701-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="bd701-206">aspx-csharp</span></span>|
|<span data-ttu-id="bd701-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="bd701-207">ASP.NET (VB)</span></span>|<span data-ttu-id="bd701-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="bd701-208">aspx-vb</span></span>|
|<span data-ttu-id="bd701-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="bd701-209">AzCopy</span></span>|<span data-ttu-id="bd701-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="bd701-210">azcopy</span></span>|
|<span data-ttu-id="bd701-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="bd701-211">Azure CLI</span></span>|<span data-ttu-id="bd701-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="bd701-212">azurecli</span></span>|
|<span data-ttu-id="bd701-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd701-213">Azure PowerShell</span></span>|<span data-ttu-id="bd701-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="bd701-214">azurepowershell</span></span>|
|<span data-ttu-id="bd701-215">Bash</span><span class="sxs-lookup"><span data-stu-id="bd701-215">Bash</span></span>|<span data-ttu-id="bd701-216">bash</span><span class="sxs-lookup"><span data-stu-id="bd701-216">bash</span></span>|
|<span data-ttu-id="bd701-217">C++</span><span class="sxs-lookup"><span data-stu-id="bd701-217">C++</span></span>|<span data-ttu-id="bd701-218">cpp</span><span class="sxs-lookup"><span data-stu-id="bd701-218">cpp</span></span>|
|<span data-ttu-id="bd701-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="bd701-219">C++/CX</span></span>|<span data-ttu-id="bd701-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="bd701-220">cppcx</span></span>|
|<span data-ttu-id="bd701-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="bd701-221">C++/WinRT</span></span>|<span data-ttu-id="bd701-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="bd701-222">cppwinrt</span></span>|
|<span data-ttu-id="bd701-223">C#</span><span class="sxs-lookup"><span data-stu-id="bd701-223">C#</span></span>|<span data-ttu-id="bd701-224">csharp</span><span class="sxs-lookup"><span data-stu-id="bd701-224">csharp</span></span>|
|<span data-ttu-id="bd701-225">C# im Browser</span><span class="sxs-lookup"><span data-stu-id="bd701-225">C# in browser</span></span>|<span data-ttu-id="bd701-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="bd701-226">csharp-interactive</span></span>|
|<span data-ttu-id="bd701-227">Konsole</span><span class="sxs-lookup"><span data-stu-id="bd701-227">Console</span></span>|<span data-ttu-id="bd701-228">console</span><span class="sxs-lookup"><span data-stu-id="bd701-228">console</span></span>|
|<span data-ttu-id="bd701-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="bd701-229">CSHTML</span></span>|<span data-ttu-id="bd701-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="bd701-230">cshtml</span></span>|
|<span data-ttu-id="bd701-231">DAX</span><span class="sxs-lookup"><span data-stu-id="bd701-231">DAX</span></span>|<span data-ttu-id="bd701-232">dax</span><span class="sxs-lookup"><span data-stu-id="bd701-232">dax</span></span>|
|<span data-ttu-id="bd701-233">Docker</span><span class="sxs-lookup"><span data-stu-id="bd701-233">Docker</span></span>|<span data-ttu-id="bd701-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="bd701-234">dockerfile</span></span>|
|<span data-ttu-id="bd701-235">F#</span><span class="sxs-lookup"><span data-stu-id="bd701-235">F#</span></span>|<span data-ttu-id="bd701-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="bd701-236">fsharp</span></span>|
|<span data-ttu-id="bd701-237">Go</span><span class="sxs-lookup"><span data-stu-id="bd701-237">Go</span></span>|<span data-ttu-id="bd701-238">go</span><span class="sxs-lookup"><span data-stu-id="bd701-238">go</span></span>|
|<span data-ttu-id="bd701-239">HTML</span><span class="sxs-lookup"><span data-stu-id="bd701-239">HTML</span></span>|<span data-ttu-id="bd701-240">html</span><span class="sxs-lookup"><span data-stu-id="bd701-240">html</span></span>|
|<span data-ttu-id="bd701-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="bd701-241">HTTP</span></span>|<span data-ttu-id="bd701-242">http</span><span class="sxs-lookup"><span data-stu-id="bd701-242">http</span></span>|
|<span data-ttu-id="bd701-243">Java</span><span class="sxs-lookup"><span data-stu-id="bd701-243">Java</span></span>|<span data-ttu-id="bd701-244">java</span><span class="sxs-lookup"><span data-stu-id="bd701-244">java</span></span>|
|<span data-ttu-id="bd701-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd701-245">JavaScript</span></span>|<span data-ttu-id="bd701-246">javascript</span><span class="sxs-lookup"><span data-stu-id="bd701-246">javascript</span></span>|
|<span data-ttu-id="bd701-247">JSON</span><span class="sxs-lookup"><span data-stu-id="bd701-247">JSON</span></span>|<span data-ttu-id="bd701-248">json</span><span class="sxs-lookup"><span data-stu-id="bd701-248">json</span></span>|
|<span data-ttu-id="bd701-249">Kusto-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="bd701-249">Kusto Query Language</span></span>|<span data-ttu-id="bd701-250">kusto</span><span class="sxs-lookup"><span data-stu-id="bd701-250">kusto</span></span>|
|<span data-ttu-id="bd701-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="bd701-251">Markdown</span></span>|<span data-ttu-id="bd701-252">md</span><span class="sxs-lookup"><span data-stu-id="bd701-252">md</span></span>|
|<span data-ttu-id="bd701-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="bd701-253">Objective-C</span></span>|<span data-ttu-id="bd701-254">objc</span><span class="sxs-lookup"><span data-stu-id="bd701-254">objc</span></span>|
|<span data-ttu-id="bd701-255">OData</span><span class="sxs-lookup"><span data-stu-id="bd701-255">OData</span></span>|<span data-ttu-id="bd701-256">odata</span><span class="sxs-lookup"><span data-stu-id="bd701-256">odata</span></span>|
|<span data-ttu-id="bd701-257">PHP</span><span class="sxs-lookup"><span data-stu-id="bd701-257">PHP</span></span>|<span data-ttu-id="bd701-258">php</span><span class="sxs-lookup"><span data-stu-id="bd701-258">php</span></span>|
|<span data-ttu-id="bd701-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="bd701-259">protobuf</span></span>|<span data-ttu-id="bd701-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="bd701-260">protobuf</span></span>|
|<span data-ttu-id="bd701-261">PowerApps (Punkt als Dezimaltrennzeichen)</span><span class="sxs-lookup"><span data-stu-id="bd701-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="bd701-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="bd701-262">powerapps-dot</span></span>|
|<span data-ttu-id="bd701-263">PowerApps (Komma als Dezimaltrennzeichen)</span><span class="sxs-lookup"><span data-stu-id="bd701-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="bd701-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="bd701-264">powerapps-comma</span></span>|
|<span data-ttu-id="bd701-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd701-265">PowerShell</span></span>|<span data-ttu-id="bd701-266">powershell</span><span class="sxs-lookup"><span data-stu-id="bd701-266">powershell</span></span>|
|<span data-ttu-id="bd701-267">Python</span><span class="sxs-lookup"><span data-stu-id="bd701-267">Python</span></span>|<span data-ttu-id="bd701-268">python</span><span class="sxs-lookup"><span data-stu-id="bd701-268">python</span></span>|
|<span data-ttu-id="bd701-269">Q#</span><span class="sxs-lookup"><span data-stu-id="bd701-269">Q#</span></span>|<span data-ttu-id="bd701-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="bd701-270">qsharp</span></span>|
|<span data-ttu-id="bd701-271">R</span><span class="sxs-lookup"><span data-stu-id="bd701-271">R</span></span>|<span data-ttu-id="bd701-272">r</span><span class="sxs-lookup"><span data-stu-id="bd701-272">r</span></span>|
|<span data-ttu-id="bd701-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="bd701-273">Ruby</span></span>|<span data-ttu-id="bd701-274">ruby</span><span class="sxs-lookup"><span data-stu-id="bd701-274">ruby</span></span>|
|<span data-ttu-id="bd701-275">SQL</span><span class="sxs-lookup"><span data-stu-id="bd701-275">SQL</span></span>|<span data-ttu-id="bd701-276">sql</span><span class="sxs-lookup"><span data-stu-id="bd701-276">sql</span></span>|
|<span data-ttu-id="bd701-277">Swift</span><span class="sxs-lookup"><span data-stu-id="bd701-277">Swift</span></span>|<span data-ttu-id="bd701-278">swift</span><span class="sxs-lookup"><span data-stu-id="bd701-278">swift</span></span>|
|<span data-ttu-id="bd701-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="bd701-279">TypeScript</span></span>|<span data-ttu-id="bd701-280">typescript</span><span class="sxs-lookup"><span data-stu-id="bd701-280">typescript</span></span>|
|<span data-ttu-id="bd701-281">VB</span><span class="sxs-lookup"><span data-stu-id="bd701-281">VB</span></span>|<span data-ttu-id="bd701-282">vb</span><span class="sxs-lookup"><span data-stu-id="bd701-282">vb</span></span>|
|<span data-ttu-id="bd701-283">XAML</span><span class="sxs-lookup"><span data-stu-id="bd701-283">XAML</span></span>|<span data-ttu-id="bd701-284">xaml</span><span class="sxs-lookup"><span data-stu-id="bd701-284">xaml</span></span>|
|<span data-ttu-id="bd701-285">XML</span><span class="sxs-lookup"><span data-stu-id="bd701-285">XML</span></span>|<span data-ttu-id="bd701-286">xml</span><span class="sxs-lookup"><span data-stu-id="bd701-286">xml</span></span>|

<span data-ttu-id="bd701-287">Die Markdownbezeichnung `csharp-interactive` gibt C# als Sprache an. Die Beispiele können über den Browser ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="bd701-288">Diese Ausschnitt werden in einem Docker-Container kompiliert und ausgeführt. Die Ergebnisse dieser Ausführung werden im Browserfenster des Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd701-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="bd701-289">Beispiel: C\#</span><span class="sxs-lookup"><span data-stu-id="bd701-289">Example: C\#</span></span>

<span data-ttu-id="bd701-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="bd701-290">__Markdown__</span></span>

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

<span data-ttu-id="bd701-291">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="bd701-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="bd701-292">Beispiel: SQL</span><span class="sxs-lookup"><span data-stu-id="bd701-292">Example: SQL</span></span>

<span data-ttu-id="bd701-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="bd701-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="bd701-294">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="bd701-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="bd701-295">Benutzerdefinierte Markdownerweiterungen in Docs</span><span class="sxs-lookup"><span data-stu-id="bd701-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="bd701-296">Docs.Microsoft.com (Docs) implementiert einen Markdig-Parser für Markdown, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist.</span><span class="sxs-lookup"><span data-stu-id="bd701-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="bd701-297">Markdig fügt Funktionen über Markuperweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="bd701-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="bd701-298">Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd701-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="bd701-299">(Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)</span><span class="sxs-lookup"><span data-stu-id="bd701-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="bd701-300">GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd701-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="bd701-301">Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="bd701-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="bd701-302">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="bd701-302">Note blocks</span></span>
- <span data-ttu-id="bd701-303">Includedateien</span><span class="sxs-lookup"><span data-stu-id="bd701-303">Include files</span></span>
- <span data-ttu-id="bd701-304">Selektoren</span><span class="sxs-lookup"><span data-stu-id="bd701-304">Selectors</span></span>
- <span data-ttu-id="bd701-305">Eingebettete Videos</span><span class="sxs-lookup"><span data-stu-id="bd701-305">Embedded videos</span></span>
- <span data-ttu-id="bd701-306">Codeausschnitte/-beispiele</span><span class="sxs-lookup"><span data-stu-id="bd701-306">Code snippets/samples</span></span>

<span data-ttu-id="bd701-307">Die vollständige Liste finden Sie unter „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="bd701-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="bd701-308">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="bd701-308">Note blocks</span></span>

<span data-ttu-id="bd701-309">Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:</span><span class="sxs-lookup"><span data-stu-id="bd701-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="bd701-310">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="bd701-310">NOTE</span></span>
- <span data-ttu-id="bd701-311">WARNUNG</span><span class="sxs-lookup"><span data-stu-id="bd701-311">WARNING</span></span>
- <span data-ttu-id="bd701-312">TIPP</span><span class="sxs-lookup"><span data-stu-id="bd701-312">TIP</span></span>
- <span data-ttu-id="bd701-313">WICHTIG</span><span class="sxs-lookup"><span data-stu-id="bd701-313">IMPORTANT</span></span>

<span data-ttu-id="bd701-314">Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können.</span><span class="sxs-lookup"><span data-stu-id="bd701-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="bd701-315">Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="bd701-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="bd701-316">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bd701-316">Examples:</span></span>

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

<span data-ttu-id="bd701-317">Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="bd701-317">These alerts look like this on docs.microsoft.com:</span></span>

![Hier wird dargestellt, wie Warnungen im vorherigen Beispiel auf der veröffentlichten Dokumentationsseite mit unterschiedlichen Symbolen und Farben aussieht.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="bd701-319">Includedateien</span><span class="sxs-lookup"><span data-stu-id="bd701-319">Include files</span></span>

<span data-ttu-id="bd701-320">Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd701-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="bd701-321">Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist.</span><span class="sxs-lookup"><span data-stu-id="bd701-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="bd701-322">Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Arten von Includeverweisen verwenden:</span><span class="sxs-lookup"><span data-stu-id="bd701-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="bd701-323">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="bd701-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="bd701-324">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="bd701-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="bd701-325">Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.</span><span class="sxs-lookup"><span data-stu-id="bd701-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="bd701-326">Inline- oder Blockincludedateien sind einfache Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="bd701-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="bd701-327">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd701-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="bd701-328">Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="bd701-329">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="bd701-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="bd701-330">Die Anforderungen und Überlegungen zu Includedateien lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bd701-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="bd701-331">Verwenden Sie stets dann eine Includedatei, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="bd701-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="bd701-332">Verwenden Sie einen Blockincludeverweis für umfangreiche Inhaltsmengen, d.h. für ein oder zwei Absätze, ein gemeinsames Verfahren oder einen gemeinsamen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="bd701-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="bd701-333">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="bd701-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="bd701-334">Includeverweise werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="bd701-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="bd701-335">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="bd701-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="bd701-336">Stellen Sie sicher, dass sämtlicher Text in einer Includedatei in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Includedatei verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="bd701-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="bd701-337">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="bd701-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="bd701-338">Betten Sie keine Includeverweise in andere Includedateien ein.</span><span class="sxs-lookup"><span data-stu-id="bd701-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="bd701-339">Sie werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd701-339">They are not supported.</span></span>
- <span data-ttu-id="bd701-340">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media).</span><span class="sxs-lookup"><span data-stu-id="bd701-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="bd701-341">Der Stamm des Medienverzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd701-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="bd701-342">Wenn die Includedatei keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd701-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="bd701-343">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="bd701-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="bd701-344">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Includedatei und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="bd701-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="bd701-345">Speichern Sie die Mediendatei in dem Medienordner, der der Includedatei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bd701-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="bd701-346">Verwenden Sie eine Includedatei nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="bd701-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="bd701-347">Includedateien sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="bd701-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="bd701-348">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="bd701-349">Selektoren</span><span class="sxs-lookup"><span data-stu-id="bd701-349">Selectors</span></span>

<span data-ttu-id="bd701-350">Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="bd701-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="bd701-351">Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="bd701-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="bd701-352">Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="bd701-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="bd701-353">Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Includedatei platzieren.</span><span class="sxs-lookup"><span data-stu-id="bd701-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="bd701-354">Dann können Sie auf diese Includedatei in allen Artikeln, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="bd701-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="bd701-355">Hier ist ein Beispielselektor dargestellt:</span><span class="sxs-lookup"><span data-stu-id="bd701-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="bd701-356">In der [Azure-Dokumentation](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) können Sie sich die Selektoren in Aktion ansehen.</span><span class="sxs-lookup"><span data-stu-id="bd701-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="bd701-357">Codeincludeverweise</span><span class="sxs-lookup"><span data-stu-id="bd701-357">Code include references</span></span>

<span data-ttu-id="bd701-358">Mit der Markdownerweiterung für Codeausschnitte in der Dokumentation können Sie Codebeispiele in Ihre Artikel einbetten und diese mit sprachspezifischer Syntaxfärbung darstellen.</span><span class="sxs-lookup"><span data-stu-id="bd701-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="bd701-359">Sie können Code aus dem aktuellen oder einem anderen Repository verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd701-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="bd701-360">Im Folgenden finden Sie einen Überblick über die Verwendung des Features mit dem [Authoring Pack für docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="bd701-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="bd701-361">In Visual Studio Code können Sie eine Vorschau für die Codeausschnitte anzeigen, indem Sie die **Vorschau** öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd701-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="bd701-362">Die Vorschau ist nicht interaktiv, und es werden keine Hervorhebungen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd701-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="bd701-363">Die Erweiterung unterstützt das interne Inlineeinfügen von Codeinhalten nicht. Dieser Vorgang muss über die Markdownkonvention \`\`\` (drei Backticks) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bd701-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="bd701-364">Code aus dem aktuellen Repository</span><span class="sxs-lookup"><span data-stu-id="bd701-364">Code from current repository</span></span>

1. <span data-ttu-id="bd701-365">Drücken Sie in Visual Studio Code **ALT+M** oder **WAHLTASTE+M**, und klicken Sie auf „Codeausschnitt“.</span><span class="sxs-lookup"><span data-stu-id="bd701-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="bd701-366">Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bd701-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="bd701-367">Wählen Sie „Full Local Search“ (Vollständige lokale Suche) aus, wenn Sie lokal suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="bd701-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="bd701-368">Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bd701-368">Enter a search term to find the file.</span></span> <span data-ttu-id="bd701-369">Wählen Sie die Datei aus, wenn sie gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="bd701-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="bd701-370">Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="bd701-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="bd701-371">Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).</span><span class="sxs-lookup"><span data-stu-id="bd701-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="bd701-372">Geben Sie je nach Auswahl in Schritt 4 einen Wert an.</span><span class="sxs-lookup"><span data-stu-id="bd701-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="bd701-373">Die gesamte Codedatei wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bd701-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="bd701-374">Ein Teil einer Codedatei wird durch Angabe von Zeilennummern angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bd701-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="bd701-375">Ein Teil einer Codedatei wird durch einen Codeausschnittnamen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bd701-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="bd701-376">Code aus einem anderen Repository</span><span class="sxs-lookup"><span data-stu-id="bd701-376">Code from another repository</span></span>

1. <span data-ttu-id="bd701-377">Drücken Sie in Visual Studio Code **ALT+M** oder **WAHLTASTE+M**, und klicken Sie auf „Codeausschnitt“.</span><span class="sxs-lookup"><span data-stu-id="bd701-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="bd701-378">Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bd701-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="bd701-379">Wählen Sie „Cross-Repository Reference“ (Repositoryübergreifender Verweis) aus, um repositoryübergreifend zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bd701-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="bd701-380">Daraufhin wird eine Auswahl der Repositorys angezeigt, die sich in *.openpublishing.publish.config.json* befinden.</span><span class="sxs-lookup"><span data-stu-id="bd701-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="bd701-381">Wählen Sie ein Repository aus.</span><span class="sxs-lookup"><span data-stu-id="bd701-381">Select a repository.</span></span>
3. <span data-ttu-id="bd701-382">Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bd701-382">Enter a search term to find the file.</span></span> <span data-ttu-id="bd701-383">Wählen Sie die Datei aus, wenn sie gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="bd701-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="bd701-384">Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="bd701-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="bd701-385">Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).</span><span class="sxs-lookup"><span data-stu-id="bd701-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="bd701-386">Geben Sie je nach Auswahl in Schritt 5 einen Wert an.</span><span class="sxs-lookup"><span data-stu-id="bd701-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="bd701-387">Ihr Codeausschnittverweis sieht folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="bd701-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="bd701-388">Pfad zur Codedatei</span><span class="sxs-lookup"><span data-stu-id="bd701-388">Path to code file</span></span>

<span data-ttu-id="bd701-389">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="bd701-390">Das Beispiel stammt aus der Artikeldatei [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) des ASP.NET-Dokumentenrepositorys.</span><span class="sxs-lookup"><span data-stu-id="bd701-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="bd701-391">Auf die Codedatei wird über einen relativen Pfad zu [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) im selben Repository verwiesen.</span><span class="sxs-lookup"><span data-stu-id="bd701-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="bd701-392">Ausgewählte Zeilennummern</span><span class="sxs-lookup"><span data-stu-id="bd701-392">Selected line numbers</span></span>

<span data-ttu-id="bd701-393">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="bd701-394">In diesem Beispiel werden nur die Zeilen 2–24 und 26 der Codedatei *StudentController.cs* angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd701-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="bd701-395">Bevorzugen Sie Ausschnitte gegenüber hartcodierten Zeilennummern, wie im nächsten Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd701-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="bd701-396">Benannter Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="bd701-396">Named snippet</span></span>

<span data-ttu-id="bd701-397">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="bd701-398">Verwenden Sie für den Namen nur Buchstaben und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="bd701-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="bd701-399">Das Beispiel zeigt den Abschnitt `snippet_Create` der Codedatei.</span><span class="sxs-lookup"><span data-stu-id="bd701-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="bd701-400">Die Codedatei für dieses Beispiel verfügt über einen C#-Bereich namens `snippet_Create`:</span><span class="sxs-lookup"><span data-stu-id="bd701-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="bd701-401">Wenn möglich, sollten Sie immer auf einen benannten Abschnitt verweisen anstatt Zeilennummern anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bd701-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="bd701-402">Zeilennummernverweise sind fehleranfällig, weil sich Codedateien zwangsläufig in einer Weise ändern, die die Zeilennummern verändern.</span><span class="sxs-lookup"><span data-stu-id="bd701-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="bd701-403">Über solche Änderungen werden Sie nicht unbedingt informiert.</span><span class="sxs-lookup"><span data-stu-id="bd701-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="bd701-404">In Ihrem Artikel werden dann die falschen Zeilen angezeigt, und Sie haben keine Ahnung, dass sich überhaupt etwas geändert hat.</span><span class="sxs-lookup"><span data-stu-id="bd701-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="bd701-405">Hervorheben ausgewählter Zeilen</span><span class="sxs-lookup"><span data-stu-id="bd701-405">Highlighting selected lines</span></span>

<span data-ttu-id="bd701-406">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="bd701-407">Im Beispiel werden die Zeilen 2 und 5 hervorgehoben, gezählt vom Anfang des angezeigten Ausschnitts.</span><span class="sxs-lookup"><span data-stu-id="bd701-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="bd701-408">(Bei hervorzuhebenden Zeilennummern wird mit dem Zählen nicht am Anfang der Codedatei begonnen.) Die Zeilen 3 und 6 der Codedatei werden also hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="bd701-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="bd701-409">Interaktive Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="bd701-409">Interactive code snippets</span></span>

<span data-ttu-id="bd701-410">Sie können den interaktiven Modus für Codeausschnitte aktivieren, die per Verweis eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="bd701-411">Hier finden Sie Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bd701-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="bd701-412">Verwenden Sie das Attribut `interactive`, um dieses Feature für einen bestimmten Codeblock zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bd701-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="bd701-413">Folgende Attributwerte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="bd701-413">The available attribute values are:</span></span>

- <span data-ttu-id="bd701-414">`cloudshell-powershell`: Aktiviert wie im vorherigen Beispiel PowerShell für Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="bd701-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="bd701-415">`cloudshell-bash`: Aktiviert Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="bd701-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="bd701-416">`try-dotnet`: Aktiviert Try .NET</span><span class="sxs-lookup"><span data-stu-id="bd701-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="bd701-417">`try-dotnet-class`: Aktiviert Try .NET mit Klassengerüsten</span><span class="sxs-lookup"><span data-stu-id="bd701-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="bd701-418">`try-dotnet-method`: Aktiviert Try .NET mit Methodengerüsten</span><span class="sxs-lookup"><span data-stu-id="bd701-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="bd701-419">Es gibt kompatible Kombinationen von `language` und `interactive`.</span><span class="sxs-lookup"><span data-stu-id="bd701-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="bd701-420">Wenn `interactive` beispielsweise den Wert `try-dotnet` aufweist, muss die Sprache `csharp` sein.</span><span class="sxs-lookup"><span data-stu-id="bd701-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="bd701-421">Ebenso funktioniert `cloudshell-powershell` nur mit `powershell`, und `cloudshell-bash` würde nur mit `bash` als Sprache funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bd701-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="bd701-422">Für Azure Cloud Shell und PowerShell Cloud Shell können Benutzer Befehle nur für ihr eigenes Azure-Konto ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd701-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="bd701-423">[Try .NET](https://github.com/dotnet/try) aktiviert die interaktive Ausführung von .NET-Code (C#) im Browser.</span><span class="sxs-lookup"><span data-stu-id="bd701-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="bd701-424">Für Try .NET gibt es drei Interaktivitätsoptionen: `try-dotnet`, `try-dotnet-class` und `try-dotnet-method`.</span><span class="sxs-lookup"><span data-stu-id="bd701-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="bd701-425">Wenn Sie diese Optionen verwenden, ist keine zusätzliche Konfiguration im Codeausschnitt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd701-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="bd701-426">Folgende Namespaces sind derzeit standardmäßig verfügbar:</span><span class="sxs-lookup"><span data-stu-id="bd701-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="bd701-427">System</span><span class="sxs-lookup"><span data-stu-id="bd701-427">System</span></span>
- <span data-ttu-id="bd701-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="bd701-428">System.Linq</span></span>
- <span data-ttu-id="bd701-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="bd701-429">System.Collections.Generic</span></span>
- <span data-ttu-id="bd701-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="bd701-430">System.Text</span></span>
- <span data-ttu-id="bd701-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="bd701-431">System.Globalization</span></span>
- <span data-ttu-id="bd701-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="bd701-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="bd701-433">Mit dem Attributwert `try-dotnet` können Benutzer C#-Code im Browser ausführen, ohne den Code mit benutzerdefiniertem Code zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="bd701-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="bd701-434">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="bd701-435">Der Wert `try-dotnet-class` wendet ein Klassengerüst auf den Code an, der an die interaktive Komponente übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="bd701-436">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-436">Example:</span></span>

<span data-ttu-id="bd701-437">Codeausschnitt ohne Klassengerüst</span><span class="sxs-lookup"><span data-stu-id="bd701-437">Code Snippet without Class Scaffolding Applied</span></span>

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

<span data-ttu-id="bd701-438">Codeausschnitt mit Klassengerüst</span><span class="sxs-lookup"><span data-stu-id="bd701-438">Code Snippet with Class Scaffolding Applied</span></span>

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

<span data-ttu-id="bd701-439">Der Wert `try-dotnet-method` wendet ein Methodengerüst auf den Code an, der an die interaktive Komponente übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="bd701-440">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd701-440">Example:</span></span>

<span data-ttu-id="bd701-441">Codeausschnitt ohne Methodengerüst</span><span class="sxs-lookup"><span data-stu-id="bd701-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="bd701-442">Codeausschnitt mit Methodengerüst</span><span class="sxs-lookup"><span data-stu-id="bd701-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="bd701-443">Verweissyntax für Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="bd701-443">Snippet syntax reference</span></span>

<span data-ttu-id="bd701-444">Sie können auf Codeausschnitte verweisen, die in Ihrem Repository gespeichert sind, indem Sie die angegebene Codesprache verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd701-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="bd701-445">Die Inhalte des angegebenen Codepfads werden erweitert und in Ihre Datei eingebunden.</span><span class="sxs-lookup"><span data-stu-id="bd701-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="bd701-446">Für die Ordnerstruktur von Codeausschnitten gibt es keinerlei Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="bd701-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="bd701-447">Sie können die Codeausschnitte als normalen Quellcode verwalten.</span><span class="sxs-lookup"><span data-stu-id="bd701-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="bd701-448">Syntax:</span><span class="sxs-lookup"><span data-stu-id="bd701-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="bd701-449">Diese Syntax ist ein Blockmarkdown-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bd701-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="bd701-450">Sie muss in einer eigenen Zeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-450">It must be used on its own line.</span></span>

- <span data-ttu-id="bd701-451">`<language>` (*optional*)</span><span class="sxs-lookup"><span data-stu-id="bd701-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="bd701-452">Sprache des Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="bd701-452">Language of the code snippet.</span></span> <span data-ttu-id="bd701-453">Weitere Informationen finden Sie im Abschnitt [Unterstützte Sprachen](#supported-languages) weiter unten in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="bd701-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="bd701-454">`<path>` (*obligatorisch*)</span><span class="sxs-lookup"><span data-stu-id="bd701-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="bd701-455">Relativer Pfad im Dateisystem, der die Codeausschnittdatei angibt, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="bd701-456">`<attribute>` und `<attribute-value>` (*optional*)</span><span class="sxs-lookup"><span data-stu-id="bd701-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="bd701-457">Zusammen verwendet, um anzugeben, wie der Code aus der Datei abgerufen werden sollen:</span><span class="sxs-lookup"><span data-stu-id="bd701-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="bd701-458">`range`: `1,3-5` Ein Bereich von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="bd701-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="bd701-459">Dieses Beispiel enthält die Zeilen 1, 3, 4 und 5.</span><span class="sxs-lookup"><span data-stu-id="bd701-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="bd701-460">`id`: `snippet_Create`: Die ID des Codeausschnitts, der aus der Codedatei eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd701-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="bd701-461">Dieser Wert kann nicht gleichzeitig mit „range“ vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="bd701-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="bd701-462">`highlight`: `2-4,6`: Der Bereich und/oder die Zeilennummern, die im generierten Codeausschnitt hervorgehoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd701-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="bd701-463">Die Nummerierung ist relativ zum Codeausschnitt, nicht zum importierten Bereich.</span><span class="sxs-lookup"><span data-stu-id="bd701-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="bd701-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method`: Der Zeichenfolgenwert legt fest, welche Arten von Interaktivität aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="bd701-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="bd701-465">Unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="bd701-465">Supported languages</span></span>

|<span data-ttu-id="bd701-466">Name</span><span class="sxs-lookup"><span data-stu-id="bd701-466">Name</span></span>|<span data-ttu-id="bd701-467">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="bd701-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="bd701-468">.NET Core-CLI</span><span class="sxs-lookup"><span data-stu-id="bd701-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="bd701-469">ASP.NET mit C#</span><span class="sxs-lookup"><span data-stu-id="bd701-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="bd701-470">ASP.NET mit VB</span><span class="sxs-lookup"><span data-stu-id="bd701-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="bd701-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="bd701-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="bd701-472">Azure CLI im Browser</span><span class="sxs-lookup"><span data-stu-id="bd701-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="bd701-473">Azure PowerShell im Browser</span><span class="sxs-lookup"><span data-stu-id="bd701-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="bd701-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="bd701-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="bd701-475">Bash</span><span class="sxs-lookup"><span data-stu-id="bd701-475">Bash</span></span>|`bash`|
|<span data-ttu-id="bd701-476">C++</span><span class="sxs-lookup"><span data-stu-id="bd701-476">C++</span></span>|`cpp`|
|<span data-ttu-id="bd701-477">C#</span><span class="sxs-lookup"><span data-stu-id="bd701-477">C#</span></span>|`csharp`|
|<span data-ttu-id="bd701-478">C# im Browser</span><span class="sxs-lookup"><span data-stu-id="bd701-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="bd701-479">Konsole</span><span class="sxs-lookup"><span data-stu-id="bd701-479">Console</span></span>|`console`|
|<span data-ttu-id="bd701-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="bd701-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="bd701-481">DAX</span><span class="sxs-lookup"><span data-stu-id="bd701-481">DAX</span></span>|`dax`|
|<span data-ttu-id="bd701-482">Docker</span><span class="sxs-lookup"><span data-stu-id="bd701-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="bd701-483">F#</span><span class="sxs-lookup"><span data-stu-id="bd701-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="bd701-484">HTML</span><span class="sxs-lookup"><span data-stu-id="bd701-484">HTML</span></span>|`html`|
|<span data-ttu-id="bd701-485">Java</span><span class="sxs-lookup"><span data-stu-id="bd701-485">Java</span></span>|`java`|
|<span data-ttu-id="bd701-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd701-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="bd701-487">JSON</span><span class="sxs-lookup"><span data-stu-id="bd701-487">JSON</span></span>|`json`|
|<span data-ttu-id="bd701-488">Kusto-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="bd701-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="bd701-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="bd701-489">Markdown</span></span>|`md`|
|<span data-ttu-id="bd701-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="bd701-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="bd701-491">PHP</span><span class="sxs-lookup"><span data-stu-id="bd701-491">PHP</span></span>|`php`|
|<span data-ttu-id="bd701-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd701-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="bd701-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="bd701-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="bd701-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="bd701-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="bd701-495">Python</span><span class="sxs-lookup"><span data-stu-id="bd701-495">Python</span></span>|`python`|
|<span data-ttu-id="bd701-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="bd701-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="bd701-497">SQL</span><span class="sxs-lookup"><span data-stu-id="bd701-497">SQL</span></span>|`sql`|
|<span data-ttu-id="bd701-498">Swift</span><span class="sxs-lookup"><span data-stu-id="bd701-498">Swift</span></span>|`swift`|
|<span data-ttu-id="bd701-499">VB</span><span class="sxs-lookup"><span data-stu-id="bd701-499">VB</span></span>|`vb`|
|<span data-ttu-id="bd701-500">XAML</span><span class="sxs-lookup"><span data-stu-id="bd701-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="bd701-501">XML</span><span class="sxs-lookup"><span data-stu-id="bd701-501">XML</span></span>|`xml`|
|<span data-ttu-id="bd701-502">YAML</span><span class="sxs-lookup"><span data-stu-id="bd701-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="bd701-503">Codeerweiterungen</span><span class="sxs-lookup"><span data-stu-id="bd701-503">Code extensions</span></span>

|<span data-ttu-id="bd701-504">Name</span><span class="sxs-lookup"><span data-stu-id="bd701-504">Name</span></span>|<span data-ttu-id="bd701-505">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="bd701-505">Markdown label</span></span>|<span data-ttu-id="bd701-506">Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="bd701-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="bd701-507">C#</span><span class="sxs-lookup"><span data-stu-id="bd701-507">C#</span></span>|<span data-ttu-id="bd701-508">csharp</span><span class="sxs-lookup"><span data-stu-id="bd701-508">csharp</span></span>|<span data-ttu-id="bd701-509">.cs, .csx</span><span class="sxs-lookup"><span data-stu-id="bd701-509">.cs, .csx</span></span>|
|<span data-ttu-id="bd701-510">C++</span><span class="sxs-lookup"><span data-stu-id="bd701-510">C++</span></span>|<span data-ttu-id="bd701-511">cpp</span><span class="sxs-lookup"><span data-stu-id="bd701-511">cpp</span></span>|<span data-ttu-id="bd701-512">.cpp, .h</span><span class="sxs-lookup"><span data-stu-id="bd701-512">.cpp, .h</span></span>|
|<span data-ttu-id="bd701-513">F#</span><span class="sxs-lookup"><span data-stu-id="bd701-513">F#</span></span>|<span data-ttu-id="bd701-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="bd701-514">fsharp</span></span>|<span data-ttu-id="bd701-515">.fs</span><span class="sxs-lookup"><span data-stu-id="bd701-515">.fs</span></span>|
|<span data-ttu-id="bd701-516">Java</span><span class="sxs-lookup"><span data-stu-id="bd701-516">Java</span></span>|<span data-ttu-id="bd701-517">java</span><span class="sxs-lookup"><span data-stu-id="bd701-517">java</span></span>|<span data-ttu-id="bd701-518">.java</span><span class="sxs-lookup"><span data-stu-id="bd701-518">.java</span></span>|
|<span data-ttu-id="bd701-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd701-519">JavaScript</span></span>|<span data-ttu-id="bd701-520">javascript</span><span class="sxs-lookup"><span data-stu-id="bd701-520">javascript</span></span>|<span data-ttu-id="bd701-521">.js</span><span class="sxs-lookup"><span data-stu-id="bd701-521">.js</span></span>|
|<span data-ttu-id="bd701-522">Python</span><span class="sxs-lookup"><span data-stu-id="bd701-522">Python</span></span>|<span data-ttu-id="bd701-523">python</span><span class="sxs-lookup"><span data-stu-id="bd701-523">python</span></span>|<span data-ttu-id="bd701-524">.py</span><span class="sxs-lookup"><span data-stu-id="bd701-524">.py</span></span>|
|<span data-ttu-id="bd701-525">SQL</span><span class="sxs-lookup"><span data-stu-id="bd701-525">SQL</span></span>|<span data-ttu-id="bd701-526">sql</span><span class="sxs-lookup"><span data-stu-id="bd701-526">sql</span></span>|<span data-ttu-id="bd701-527">.sql</span><span class="sxs-lookup"><span data-stu-id="bd701-527">.sql</span></span>|
|<span data-ttu-id="bd701-528">VB</span><span class="sxs-lookup"><span data-stu-id="bd701-528">VB</span></span>|<span data-ttu-id="bd701-529">vb</span><span class="sxs-lookup"><span data-stu-id="bd701-529">vb</span></span>|<span data-ttu-id="bd701-530">.vb</span><span class="sxs-lookup"><span data-stu-id="bd701-530">.vb</span></span>|
|<span data-ttu-id="bd701-531">XAML</span><span class="sxs-lookup"><span data-stu-id="bd701-531">XAML</span></span>|<span data-ttu-id="bd701-532">xaml</span><span class="sxs-lookup"><span data-stu-id="bd701-532">xaml</span></span>|<span data-ttu-id="bd701-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="bd701-533">.xaml</span></span>|
|<span data-ttu-id="bd701-534">XML</span><span class="sxs-lookup"><span data-stu-id="bd701-534">XML</span></span>|<span data-ttu-id="bd701-535">xml</span><span class="sxs-lookup"><span data-stu-id="bd701-535">xml</span></span>|<span data-ttu-id="bd701-536">.xml</span><span class="sxs-lookup"><span data-stu-id="bd701-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="bd701-537">Häufige Fehler und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="bd701-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="bd701-538">Alternativtext</span><span class="sxs-lookup"><span data-stu-id="bd701-538">Alt text</span></span>

<span data-ttu-id="bd701-539">Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert.</span><span class="sxs-lookup"><span data-stu-id="bd701-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="bd701-540">Verwenden Sie beispielsweise anstelle von</span><span class="sxs-lookup"><span data-stu-id="bd701-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="bd701-541">diese Möglichkeit zur Umgehung von Unterstrichen:</span><span class="sxs-lookup"><span data-stu-id="bd701-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="bd701-542">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="bd701-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="bd701-543">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd701-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="bd701-544">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bd701-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="bd701-545">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="bd701-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="bd701-546">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="bd701-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="bd701-547">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="bd701-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="bd701-548">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="bd701-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="bd701-549">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="bd701-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="bd701-550">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="bd701-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="bd701-551">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="bd701-551">Angle brackets</span></span>

<span data-ttu-id="bd701-552">Spitze Klammern werden häufig zum Kennzeichnen eines Platzhalters verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd701-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="bd701-553">Wenn Sie dies im Text nutzen (nicht im Code), müssen Sie die spitzen Klammern codieren.</span><span class="sxs-lookup"><span data-stu-id="bd701-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="bd701-554">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="bd701-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="bd701-555">Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="bd701-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="bd701-556">Markdown-Variante</span><span class="sxs-lookup"><span data-stu-id="bd701-556">Markdown flavor</span></span>

<span data-ttu-id="bd701-557">Das Back-End der Website „docs.microsoft.com“ unterstützt ein kompatibles [CommonMark](https://commonmark.org/)-Markdown, das von der [Markdig](https://github.com/lunet-io/markdig)-Analyse-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="bd701-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="bd701-558">Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="bd701-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="bd701-559">Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bd701-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd701-560">Siehe auch:</span><span class="sxs-lookup"><span data-stu-id="bd701-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="bd701-561">Markdownressourcen</span><span class="sxs-lookup"><span data-stu-id="bd701-561">Markdown resources</span></span>

- <span data-ttu-id="bd701-562">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)</span><span class="sxs-lookup"><span data-stu-id="bd701-562">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="bd701-563">Cheatsheet zur Markdown-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="bd701-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="bd701-564">[Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="bd701-564">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- [<span data-ttu-id="bd701-565">The Markdown Guide (Das Markdown-Handbuch)</span><span class="sxs-lookup"><span data-stu-id="bd701-565">The Markdown Guide</span></span>](https://www.markdownguide.org/)
