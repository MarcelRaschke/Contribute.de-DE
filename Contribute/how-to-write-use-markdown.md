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
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="d4061-103">Verwenden von Markdown für das Schreiben von Dokumentationsartikeln</span><span class="sxs-lookup"><span data-stu-id="d4061-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="d4061-104">Docs.Microsoft.Com-Artikel sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="d4061-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="d4061-105">Darum ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="d4061-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="d4061-106">Da Dokumentationsinhalte in GitHub gespeichert werden, können sie ein als Superset von Markdown bezeichnetes [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) verwenden, das zusätzliche Funktionalität für gängige Formatierungsanforderungen bietet.</span><span class="sxs-lookup"><span data-stu-id="d4061-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="d4061-107">Außerdem implementiert Open Publishing Services (OPS) „DocFX Flavored Markdown (DFM)“.</span><span class="sxs-lookup"><span data-stu-id="d4061-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="d4061-108">DFM weist eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) auf und verfügt über Möglichkeiten zur Aktivierung von dokumentationsspezifischen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d4061-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="d4061-109">Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="d4061-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="d4061-110">Überschriften</span><span class="sxs-lookup"><span data-stu-id="d4061-110">Headings</span></span>

<span data-ttu-id="d4061-111">Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4061-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="d4061-112">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="d4061-112">Bold and italic text</span></span>

<span data-ttu-id="d4061-113">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="d4061-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="d4061-114">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="d4061-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="d4061-115">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="d4061-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="d4061-116">Listen</span><span class="sxs-lookup"><span data-stu-id="d4061-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="d4061-117">Ungeordnete Liste</span><span class="sxs-lookup"><span data-stu-id="d4061-117">Unordered list</span></span>

<span data-ttu-id="d4061-118">Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4061-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="d4061-119">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="d4061-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="d4061-120">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="d4061-120">will be rendered as:</span></span>

- <span data-ttu-id="d4061-121">List item 1</span><span class="sxs-lookup"><span data-stu-id="d4061-121">List item 1</span></span>
- <span data-ttu-id="d4061-122">List item 2</span><span class="sxs-lookup"><span data-stu-id="d4061-122">List item 2</span></span>
- <span data-ttu-id="d4061-123">List item 3</span><span class="sxs-lookup"><span data-stu-id="d4061-123">List item 3</span></span>

<span data-ttu-id="d4061-124">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="d4061-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d4061-125">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="d4061-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="d4061-126">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="d4061-126">will be rendered as:</span></span>

- <span data-ttu-id="d4061-127">List item 1</span><span class="sxs-lookup"><span data-stu-id="d4061-127">List item 1</span></span>
  - <span data-ttu-id="d4061-128">List item A</span><span class="sxs-lookup"><span data-stu-id="d4061-128">List item A</span></span>
  - <span data-ttu-id="d4061-129">List item B</span><span class="sxs-lookup"><span data-stu-id="d4061-129">List item B</span></span>
- <span data-ttu-id="d4061-130">List item 2</span><span class="sxs-lookup"><span data-stu-id="d4061-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="d4061-131">Geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="d4061-131">Ordered list</span></span>

<span data-ttu-id="d4061-132">Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen.</span><span class="sxs-lookup"><span data-stu-id="d4061-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="d4061-133">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="d4061-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="d4061-134">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="d4061-134">will be rendered as:</span></span>

1. <span data-ttu-id="d4061-135">First instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-135">First instruction</span></span>
2. <span data-ttu-id="d4061-136">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-136">Second instruction</span></span>
3. <span data-ttu-id="d4061-137">Third instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-137">Third instruction</span></span>

<span data-ttu-id="d4061-138">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="d4061-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d4061-139">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="d4061-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="d4061-140">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="d4061-140">will be rendered as:</span></span>

1. <span data-ttu-id="d4061-141">First instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-141">First instruction</span></span>
    1. <span data-ttu-id="d4061-142">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-142">Sub-instruction</span></span>
    2. <span data-ttu-id="d4061-143">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-143">Sub-instruction</span></span>
2. <span data-ttu-id="d4061-144">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d4061-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="d4061-145">Tables</span><span class="sxs-lookup"><span data-stu-id="d4061-145">Tables</span></span>

<span data-ttu-id="d4061-146">Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4061-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="d4061-147">Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4061-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="d4061-148">Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="d4061-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="d4061-149">Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="d4061-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="d4061-150">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="d4061-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d4061-151">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="d4061-151">will be rendered as:</span></span>

| <span data-ttu-id="d4061-152">Fun</span><span class="sxs-lookup"><span data-stu-id="d4061-152">Fun</span></span>                  | <span data-ttu-id="d4061-153">With</span><span class="sxs-lookup"><span data-stu-id="d4061-153">With</span></span>                 | <span data-ttu-id="d4061-154">Tables</span><span class="sxs-lookup"><span data-stu-id="d4061-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d4061-155">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d4061-155">left-aligned column</span></span>  | <span data-ttu-id="d4061-156">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d4061-156">right-aligned column</span></span> | <span data-ttu-id="d4061-157">centered column</span><span class="sxs-lookup"><span data-stu-id="d4061-157">centered column</span></span> |
| <span data-ttu-id="d4061-158">$100</span><span class="sxs-lookup"><span data-stu-id="d4061-158">$100</span></span>                 | <span data-ttu-id="d4061-159">$100</span><span class="sxs-lookup"><span data-stu-id="d4061-159">$100</span></span>                 | <span data-ttu-id="d4061-160">$100</span><span class="sxs-lookup"><span data-stu-id="d4061-160">$100</span></span>            |
| <span data-ttu-id="d4061-161">$10</span><span class="sxs-lookup"><span data-stu-id="d4061-161">$10</span></span>                  | <span data-ttu-id="d4061-162">$10</span><span class="sxs-lookup"><span data-stu-id="d4061-162">$10</span></span>                  | <span data-ttu-id="d4061-163">$10</span><span class="sxs-lookup"><span data-stu-id="d4061-163">$10</span></span>             |
| <span data-ttu-id="d4061-164">$1</span><span class="sxs-lookup"><span data-stu-id="d4061-164">$1</span></span>                   | <span data-ttu-id="d4061-165">$1</span><span class="sxs-lookup"><span data-stu-id="d4061-165">$1</span></span>                   | <span data-ttu-id="d4061-166">$1</span><span class="sxs-lookup"><span data-stu-id="d4061-166">$1</span></span>              |

<span data-ttu-id="d4061-167">Weitere Informationen zum Erstellen von Tabellen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d4061-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="d4061-168">Abschnitt zur DFM-[Tabellenumbruchfunktion](#table-wrapping), die bei der Formatierung breiter Tabellen hilfreich sein kann</span><span class="sxs-lookup"><span data-stu-id="d4061-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="d4061-169">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organisieren von Daten mit Tabellen) von GitHub</span><span class="sxs-lookup"><span data-stu-id="d4061-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="d4061-170">Die [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)-Web-App (Markdowntabellengenerator)</span><span class="sxs-lookup"><span data-stu-id="d4061-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="d4061-171">Markdown Cheatsheet von Adam Pritchard</span><span class="sxs-lookup"><span data-stu-id="d4061-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="d4061-172">Markdown Extra von Michel Fortin</span><span class="sxs-lookup"><span data-stu-id="d4061-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="d4061-173">Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)</span><span class="sxs-lookup"><span data-stu-id="d4061-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="d4061-174">Links</span><span class="sxs-lookup"><span data-stu-id="d4061-174">Links</span></span>

<span data-ttu-id="d4061-175">Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:</span><span class="sxs-lookup"><span data-stu-id="d4061-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="d4061-176">Weitere Informationen zur Verknüpfung finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="d4061-176">For more information on linking, see:</span></span>

- <span data-ttu-id="d4061-177">Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.</span><span class="sxs-lookup"><span data-stu-id="d4061-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="d4061-178">Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält nähere Informationen zur zusätzlichen von DFM bereitgestellten Verknüpfungssyntax.</span><span class="sxs-lookup"><span data-stu-id="d4061-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="d4061-179">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="d4061-179">Code snippets</span></span>

<span data-ttu-id="d4061-180">Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="d4061-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d4061-181">Nähere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d4061-181">For details, see:</span></span>

- <span data-ttu-id="d4061-182">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)</span><span class="sxs-lookup"><span data-stu-id="d4061-182">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="d4061-183">[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)</span><span class="sxs-lookup"><span data-stu-id="d4061-183">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="d4061-184">Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d4061-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="d4061-185">Das allgemeine Format für umzäunte Codeblöcke ist:</span><span class="sxs-lookup"><span data-stu-id="d4061-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="d4061-186">Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="d4061-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="d4061-187">Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:</span><span class="sxs-lookup"><span data-stu-id="d4061-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="d4061-188">Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="d4061-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="d4061-189">Name</span><span class="sxs-lookup"><span data-stu-id="d4061-189">Name</span></span>|<span data-ttu-id="d4061-190">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="d4061-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="d4061-191">.NET-Konsole</span><span class="sxs-lookup"><span data-stu-id="d4061-191">.NET Console</span></span>|<span data-ttu-id="d4061-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="d4061-192">dotnetcli</span></span>|
|<span data-ttu-id="d4061-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="d4061-193">ASP.NET (C#)</span></span>|<span data-ttu-id="d4061-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="d4061-194">aspx-csharp</span></span>|
|<span data-ttu-id="d4061-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="d4061-195">ASP.NET (VB)</span></span>|<span data-ttu-id="d4061-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="d4061-196">aspx-vb</span></span>|
|<span data-ttu-id="d4061-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="d4061-197">AzCopy</span></span>|<span data-ttu-id="d4061-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="d4061-198">azcopy</span></span>|
|<span data-ttu-id="d4061-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d4061-199">Azure CLI</span></span>|<span data-ttu-id="d4061-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="d4061-200">azurecli</span></span>|
|<span data-ttu-id="d4061-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4061-201">Azure PowerShell</span></span>|<span data-ttu-id="d4061-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="d4061-202">azurepowershell</span></span>|
|<span data-ttu-id="d4061-203">C++</span><span class="sxs-lookup"><span data-stu-id="d4061-203">C++</span></span>|<span data-ttu-id="d4061-204">cpp</span><span class="sxs-lookup"><span data-stu-id="d4061-204">cpp</span></span>|
|<span data-ttu-id="d4061-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="d4061-205">C++/CX</span></span>|<span data-ttu-id="d4061-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="d4061-206">cppcx</span></span>|
|<span data-ttu-id="d4061-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="d4061-207">C++/WinRT</span></span>|<span data-ttu-id="d4061-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="d4061-208">cppwinrt</span></span>|
|<span data-ttu-id="d4061-209">C#</span><span class="sxs-lookup"><span data-stu-id="d4061-209">C#</span></span>|<span data-ttu-id="d4061-210">csharp</span><span class="sxs-lookup"><span data-stu-id="d4061-210">csharp</span></span>|
|<span data-ttu-id="d4061-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="d4061-211">CSHTML</span></span>|<span data-ttu-id="d4061-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="d4061-212">cshtml</span></span>|
|<span data-ttu-id="d4061-213">DAX</span><span class="sxs-lookup"><span data-stu-id="d4061-213">DAX</span></span>|<span data-ttu-id="d4061-214">dax</span><span class="sxs-lookup"><span data-stu-id="d4061-214">dax</span></span>|
|<span data-ttu-id="d4061-215">F#</span><span class="sxs-lookup"><span data-stu-id="d4061-215">F#</span></span>|<span data-ttu-id="d4061-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="d4061-216">fsharp</span></span>|
|<span data-ttu-id="d4061-217">Go</span><span class="sxs-lookup"><span data-stu-id="d4061-217">Go</span></span>|<span data-ttu-id="d4061-218">go</span><span class="sxs-lookup"><span data-stu-id="d4061-218">go</span></span>|
|<span data-ttu-id="d4061-219">HTML</span><span class="sxs-lookup"><span data-stu-id="d4061-219">HTML</span></span>|<span data-ttu-id="d4061-220">html</span><span class="sxs-lookup"><span data-stu-id="d4061-220">html</span></span>|
|<span data-ttu-id="d4061-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="d4061-221">HTTP</span></span>|<span data-ttu-id="d4061-222">http</span><span class="sxs-lookup"><span data-stu-id="d4061-222">http</span></span>|
|<span data-ttu-id="d4061-223">Java</span><span class="sxs-lookup"><span data-stu-id="d4061-223">Java</span></span>|<span data-ttu-id="d4061-224">java</span><span class="sxs-lookup"><span data-stu-id="d4061-224">java</span></span>|
|<span data-ttu-id="d4061-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d4061-225">JavaScript</span></span>|<span data-ttu-id="d4061-226">javascript</span><span class="sxs-lookup"><span data-stu-id="d4061-226">javascript</span></span>|
|<span data-ttu-id="d4061-227">JSON</span><span class="sxs-lookup"><span data-stu-id="d4061-227">JSON</span></span>|<span data-ttu-id="d4061-228">json</span><span class="sxs-lookup"><span data-stu-id="d4061-228">json</span></span>|
|<span data-ttu-id="d4061-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="d4061-229">Markdown</span></span>|<span data-ttu-id="d4061-230">md</span><span class="sxs-lookup"><span data-stu-id="d4061-230">md</span></span>|
|<span data-ttu-id="d4061-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="d4061-231">NodeJS</span></span>|<span data-ttu-id="d4061-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="d4061-232">nodejs</span></span>|
|<span data-ttu-id="d4061-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d4061-233">Objective-C</span></span>|<span data-ttu-id="d4061-234">objc</span><span class="sxs-lookup"><span data-stu-id="d4061-234">objc</span></span>|
|<span data-ttu-id="d4061-235">OData</span><span class="sxs-lookup"><span data-stu-id="d4061-235">OData</span></span>|<span data-ttu-id="d4061-236">odata</span><span class="sxs-lookup"><span data-stu-id="d4061-236">odata</span></span>|
|<span data-ttu-id="d4061-237">PHP</span><span class="sxs-lookup"><span data-stu-id="d4061-237">PHP</span></span>|<span data-ttu-id="d4061-238">php</span><span class="sxs-lookup"><span data-stu-id="d4061-238">php</span></span>|
|<span data-ttu-id="d4061-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="d4061-239">Power Apps Formula</span></span>|<span data-ttu-id="d4061-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="d4061-240">powerappsfl</span></span>|
|<span data-ttu-id="d4061-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4061-241">PowerShell</span></span>|<span data-ttu-id="d4061-242">powershell</span><span class="sxs-lookup"><span data-stu-id="d4061-242">powershell</span></span>|
|<span data-ttu-id="d4061-243">Python</span><span class="sxs-lookup"><span data-stu-id="d4061-243">Python</span></span>|<span data-ttu-id="d4061-244">python</span><span class="sxs-lookup"><span data-stu-id="d4061-244">python</span></span>|
|<span data-ttu-id="d4061-245">Q#</span><span class="sxs-lookup"><span data-stu-id="d4061-245">Q#</span></span>|<span data-ttu-id="d4061-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="d4061-246">qsharp</span></span>|
|<span data-ttu-id="d4061-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="d4061-247">Ruby</span></span>|<span data-ttu-id="d4061-248">ruby</span><span class="sxs-lookup"><span data-stu-id="d4061-248">ruby</span></span>|
|<span data-ttu-id="d4061-249">SQL</span><span class="sxs-lookup"><span data-stu-id="d4061-249">SQL</span></span>|<span data-ttu-id="d4061-250">sql</span><span class="sxs-lookup"><span data-stu-id="d4061-250">sql</span></span>|
|<span data-ttu-id="d4061-251">Swift</span><span class="sxs-lookup"><span data-stu-id="d4061-251">Swift</span></span>|<span data-ttu-id="d4061-252">swift</span><span class="sxs-lookup"><span data-stu-id="d4061-252">swift</span></span>|
|<span data-ttu-id="d4061-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="d4061-253">TypeScript</span></span>|<span data-ttu-id="d4061-254">typescript</span><span class="sxs-lookup"><span data-stu-id="d4061-254">typescript</span></span>|
|<span data-ttu-id="d4061-255">VB</span><span class="sxs-lookup"><span data-stu-id="d4061-255">VB</span></span>|<span data-ttu-id="d4061-256">vb</span><span class="sxs-lookup"><span data-stu-id="d4061-256">vb</span></span>|
|<span data-ttu-id="d4061-257">VSTS-CLI</span><span class="sxs-lookup"><span data-stu-id="d4061-257">VSTS CLI</span></span>|<span data-ttu-id="d4061-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="d4061-258">vstscli</span></span>|
|<span data-ttu-id="d4061-259">XAML</span><span class="sxs-lookup"><span data-stu-id="d4061-259">XAML</span></span>|<span data-ttu-id="d4061-260">xaml</span><span class="sxs-lookup"><span data-stu-id="d4061-260">xaml</span></span>|
|<span data-ttu-id="d4061-261">XML</span><span class="sxs-lookup"><span data-stu-id="d4061-261">XML</span></span>|<span data-ttu-id="d4061-262">xml</span><span class="sxs-lookup"><span data-stu-id="d4061-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="d4061-263">Beispiel: C\#</span><span class="sxs-lookup"><span data-stu-id="d4061-263">Example: C\#</span></span>

<span data-ttu-id="d4061-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d4061-264">__Markdown__</span></span>

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

<span data-ttu-id="d4061-265">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="d4061-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="d4061-266">Beispiel: SQL</span><span class="sxs-lookup"><span data-stu-id="d4061-266">Example: SQL</span></span>

<span data-ttu-id="d4061-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d4061-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="d4061-268">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="d4061-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="d4061-269">OPS: benutzerdefinierte Markdownerweiterungen</span><span class="sxs-lookup"><span data-stu-id="d4061-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="d4061-270">In Open Publishing Services (OPS) ist die DFM-Erweiterung (DocFX Flavored Markdown) implementiert, die eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist.</span><span class="sxs-lookup"><span data-stu-id="d4061-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="d4061-271">DFM fügt Funktionen über Markuperweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d4061-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="d4061-272">Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4061-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="d4061-273">(Sehen Sie sich beispielsweise „DFM- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)</span><span class="sxs-lookup"><span data-stu-id="d4061-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="d4061-274">GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4061-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="d4061-275">Zur weitergehenden Formatierung von Artikeln können folgende DFM-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="d4061-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="d4061-276">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="d4061-276">Note blocks</span></span>
- <span data-ttu-id="d4061-277">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="d4061-277">Includes</span></span>
- <span data-ttu-id="d4061-278">Selektoren</span><span class="sxs-lookup"><span data-stu-id="d4061-278">Selectors</span></span>
- <span data-ttu-id="d4061-279">Eingebettete Videos</span><span class="sxs-lookup"><span data-stu-id="d4061-279">Embedded videos</span></span>
- <span data-ttu-id="d4061-280">Codeausschnitte/-beispiele</span><span class="sxs-lookup"><span data-stu-id="d4061-280">Code snippets/samples</span></span>

<span data-ttu-id="d4061-281">Die vollständige Liste finden Sie unter „DFM- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d4061-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="d4061-282">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="d4061-282">Note blocks</span></span>

<span data-ttu-id="d4061-283">Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:</span><span class="sxs-lookup"><span data-stu-id="d4061-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="d4061-284">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="d4061-284">NOTE</span></span>
- <span data-ttu-id="d4061-285">WARNUNG</span><span class="sxs-lookup"><span data-stu-id="d4061-285">WARNING</span></span>
- <span data-ttu-id="d4061-286">TIPP</span><span class="sxs-lookup"><span data-stu-id="d4061-286">TIP</span></span>
- <span data-ttu-id="d4061-287">WICHTIG</span><span class="sxs-lookup"><span data-stu-id="d4061-287">IMPORTANT</span></span>

<span data-ttu-id="d4061-288">Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können.</span><span class="sxs-lookup"><span data-stu-id="d4061-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="d4061-289">Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="d4061-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="d4061-290">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="d4061-290">Includes</span></span>

<span data-ttu-id="d4061-291">Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die DFM-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4061-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="d4061-292">Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist.</span><span class="sxs-lookup"><span data-stu-id="d4061-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="d4061-293">Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Einbeziehungstypen verwenden:</span><span class="sxs-lookup"><span data-stu-id="d4061-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="d4061-294">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="d4061-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="d4061-295">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="d4061-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="d4061-296">Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.</span><span class="sxs-lookup"><span data-stu-id="d4061-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="d4061-297">Inline- oder Blockeinbeziehungen sind einfache Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="d4061-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="d4061-298">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4061-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="d4061-299">Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d4061-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="d4061-300">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="d4061-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="d4061-301">Die Anforderungen und Überlegungen zu Einbeziehungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4061-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="d4061-302">Verwenden Sie stets dann Einbeziehungen, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="d4061-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="d4061-303">Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="d4061-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d4061-304">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="d4061-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d4061-305">Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von DFM-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d4061-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="d4061-306">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="d4061-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d4061-307">Stellen Sie sicher, dass sämtlicher Text in einer Einbeziehung in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Einbeziehung verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d4061-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="d4061-308">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="d4061-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="d4061-309">Betten Sie keine Einbeziehungen in andere Einbeziehungen ein.</span><span class="sxs-lookup"><span data-stu-id="d4061-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="d4061-310">Sie werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4061-310">They are not supported.</span></span>
- <span data-ttu-id="d4061-311">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media).</span><span class="sxs-lookup"><span data-stu-id="d4061-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="d4061-312">Der Stamm des Medienverzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4061-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="d4061-313">Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4061-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="d4061-314">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="d4061-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d4061-315">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="d4061-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="d4061-316">Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4061-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="d4061-317">Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="d4061-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="d4061-318">Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="d4061-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="d4061-319">Selektoren</span><span class="sxs-lookup"><span data-stu-id="d4061-319">Selectors</span></span>

<span data-ttu-id="d4061-320">Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="d4061-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d4061-321">Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="d4061-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="d4061-322">Es gibt derzeit zwei unterschiedliche Selektortypen in DFM: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="d4061-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="d4061-323">Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Einbeziehung platzieren.</span><span class="sxs-lookup"><span data-stu-id="d4061-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="d4061-324">Dann können Sie auf diese Einbeziehung in allen Artikeln, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="d4061-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="d4061-325">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="d4061-325">Code snippets</span></span>

<span data-ttu-id="d4061-326">DFM unterstützt über seine Codeausschnitterweiterung die erweiterte Einbeziehung von Code in einen Artikel.</span><span class="sxs-lookup"><span data-stu-id="d4061-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="d4061-327">DFM bietet erweitertes Rendern, das auf GFM-Funktionen wie Programmieren der Sprachauswahl und farbiger Syntaxmarkierung sowie netten Funktionen wie den folgenden basiert:</span><span class="sxs-lookup"><span data-stu-id="d4061-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="d4061-328">Einbeziehung zentralisierter Codebeispiele bzw. -ausschnitte aus einem externen Repository</span><span class="sxs-lookup"><span data-stu-id="d4061-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="d4061-329">Benutzeroberfläche mit Registerkarten zur Anzeige mehrerer Versionen von Codebeispielen in verschiedenen Sprachen</span><span class="sxs-lookup"><span data-stu-id="d4061-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="d4061-330">Häufige Fehler und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="d4061-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="d4061-331">Alternativtext</span><span class="sxs-lookup"><span data-stu-id="d4061-331">Alt text</span></span>

<span data-ttu-id="d4061-332">Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert.</span><span class="sxs-lookup"><span data-stu-id="d4061-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="d4061-333">Verwenden Sie beispielsweise anstelle von</span><span class="sxs-lookup"><span data-stu-id="d4061-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d4061-334">diese Möglichkeit zur Umgehung von Unterstrichen:</span><span class="sxs-lookup"><span data-stu-id="d4061-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d4061-335">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="d4061-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d4061-336">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4061-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d4061-337">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4061-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d4061-338">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="d4061-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d4061-339">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="d4061-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d4061-340">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="d4061-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d4061-341">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="d4061-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d4061-342">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="d4061-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d4061-343">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="d4061-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d4061-344">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="d4061-344">Angle brackets</span></span>

<span data-ttu-id="d4061-345">Wenn Sie in Ihrer Datei geschweifte Klammern im Text (nicht Code) verwenden, z.B. zur Bezeichnung eines Platzhalters, müssen Sie die geschweiften Klammern manuell codieren.</span><span class="sxs-lookup"><span data-stu-id="d4061-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="d4061-346">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="d4061-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d4061-347">Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="d4061-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="d4061-348">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4061-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="d4061-349">Markdownressourcen</span><span class="sxs-lookup"><span data-stu-id="d4061-349">Markdown resources</span></span>

- <span data-ttu-id="d4061-350">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)</span><span class="sxs-lookup"><span data-stu-id="d4061-350">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="d4061-351">Cheatsheet zur Markdown-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d4061-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="d4061-352">[Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="d4061-352">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
