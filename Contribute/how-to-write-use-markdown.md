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
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="25c48-103">Verwenden von Markdown für das Schreiben von Dokumentationsartikeln</span><span class="sxs-lookup"><span data-stu-id="25c48-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="25c48-104">Docs.Microsoft.Com-Artikel sind in einer leichten Markupsprache namens [Markdown](https://daringfireball.net/projects/markdown/) geschrieben, die sowohl einfach zu lesen als auch zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="25c48-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="25c48-105">Darum ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="25c48-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="25c48-106">Da Dokumentationsinhalte in GitHub gespeichert werden, können sie ein als Superset von Markdown bezeichnetes [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) verwenden, das zusätzliche Funktionalität für gängige Formatierungsanforderungen bietet.</span><span class="sxs-lookup"><span data-stu-id="25c48-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="25c48-107">Außerdem implementiert Open Publishing Services (OPS) „Markdig Markdown Parser“.</span><span class="sxs-lookup"><span data-stu-id="25c48-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="25c48-108">Markdig weist eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) auf und verfügt über Möglichkeiten zur Aktivierung von dokumentationsspezifischen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="25c48-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="25c48-109">Markdig ist ein schneller, leistungsstarker und mit CommonMark kompatibler erweiterbarer Markdown-Prozessor für .NET.</span><span class="sxs-lookup"><span data-stu-id="25c48-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="25c48-110">Bessere Unterstützung durch die Community</span><span class="sxs-lookup"><span data-stu-id="25c48-110">Better community support</span></span>
* <span data-ttu-id="25c48-111">Bessere Unterstützung für Standards</span><span class="sxs-lookup"><span data-stu-id="25c48-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="25c48-112">Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="25c48-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="25c48-113">Überschriften</span><span class="sxs-lookup"><span data-stu-id="25c48-113">Headings</span></span>

<span data-ttu-id="25c48-114">Um eine Überschrift zu erstellen, verwenden Sie ein Rautenzeichen (#) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25c48-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="25c48-115">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="25c48-115">Bold and italic text</span></span>

<span data-ttu-id="25c48-116">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="25c48-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="25c48-117">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="25c48-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="25c48-118">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="25c48-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="25c48-119">Listen</span><span class="sxs-lookup"><span data-stu-id="25c48-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="25c48-120">Ungeordnete Liste</span><span class="sxs-lookup"><span data-stu-id="25c48-120">Unordered list</span></span>

<span data-ttu-id="25c48-121">Um eine ungeordnete Liste/Liste mit Aufzählungszeichen zu formatieren, können Sie entweder Sternchen oder Gedankenstriche verwenden.</span><span class="sxs-lookup"><span data-stu-id="25c48-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="25c48-122">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="25c48-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="25c48-123">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="25c48-123">will be rendered as:</span></span>

- <span data-ttu-id="25c48-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="25c48-124">List item 1</span></span>
- <span data-ttu-id="25c48-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="25c48-125">List item 2</span></span>
- <span data-ttu-id="25c48-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="25c48-126">List item 3</span></span>

<span data-ttu-id="25c48-127">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="25c48-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="25c48-128">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="25c48-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="25c48-129">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="25c48-129">will be rendered as:</span></span>

- <span data-ttu-id="25c48-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="25c48-130">List item 1</span></span>
  - <span data-ttu-id="25c48-131">List item A</span><span class="sxs-lookup"><span data-stu-id="25c48-131">List item A</span></span>
  - <span data-ttu-id="25c48-132">List item B</span><span class="sxs-lookup"><span data-stu-id="25c48-132">List item B</span></span>
- <span data-ttu-id="25c48-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="25c48-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="25c48-134">Geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="25c48-134">Ordered list</span></span>

<span data-ttu-id="25c48-135">Um eine geordnete/schrittweise Liste zu formatieren, verwenden Sie entsprechende Zahlen.</span><span class="sxs-lookup"><span data-stu-id="25c48-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="25c48-136">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="25c48-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="25c48-137">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="25c48-137">will be rendered as:</span></span>

1. <span data-ttu-id="25c48-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-138">First instruction</span></span>
2. <span data-ttu-id="25c48-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-139">Second instruction</span></span>
3. <span data-ttu-id="25c48-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-140">Third instruction</span></span>

<span data-ttu-id="25c48-141">Um eine Liste in einer anderen zu verschachteln, rücken Sie die untergeordneten Listenelemente ein.</span><span class="sxs-lookup"><span data-stu-id="25c48-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="25c48-142">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="25c48-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="25c48-143">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="25c48-143">will be rendered as:</span></span>

1. <span data-ttu-id="25c48-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-144">First instruction</span></span>
    1. <span data-ttu-id="25c48-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-145">Sub-instruction</span></span>
    2. <span data-ttu-id="25c48-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-146">Sub-instruction</span></span>
2. <span data-ttu-id="25c48-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="25c48-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="25c48-148">Tables</span><span class="sxs-lookup"><span data-stu-id="25c48-148">Tables</span></span>

<span data-ttu-id="25c48-149">Tabellen sind nicht Teil der Markdownkernspezifikation, werden jedoch von GFM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25c48-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="25c48-150">Sie können Tabellen mit dem senkrechten Strich (|) und dem Bindestrich (-) erstellen.</span><span class="sxs-lookup"><span data-stu-id="25c48-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="25c48-151">Mit Bindestrichen werden die Überschriften der Spalten erstellt, mit senkrechten Strichen die Spalten voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="25c48-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="25c48-152">Beziehen Sie zum korrekten Rendern eine leere Zeile vor Ihrer Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="25c48-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="25c48-153">Beispielsweise wird das folgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="25c48-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="25c48-154">so gerendert:</span><span class="sxs-lookup"><span data-stu-id="25c48-154">will be rendered as:</span></span>

| <span data-ttu-id="25c48-155">Fun</span><span class="sxs-lookup"><span data-stu-id="25c48-155">Fun</span></span>                  | <span data-ttu-id="25c48-156">With</span><span class="sxs-lookup"><span data-stu-id="25c48-156">With</span></span>                 | <span data-ttu-id="25c48-157">Tables</span><span class="sxs-lookup"><span data-stu-id="25c48-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="25c48-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="25c48-158">left-aligned column</span></span>  | <span data-ttu-id="25c48-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="25c48-159">right-aligned column</span></span> | <span data-ttu-id="25c48-160">centered column</span><span class="sxs-lookup"><span data-stu-id="25c48-160">centered column</span></span> |
| <span data-ttu-id="25c48-161">$100</span><span class="sxs-lookup"><span data-stu-id="25c48-161">$100</span></span>                 | <span data-ttu-id="25c48-162">$100</span><span class="sxs-lookup"><span data-stu-id="25c48-162">$100</span></span>                 | <span data-ttu-id="25c48-163">$100</span><span class="sxs-lookup"><span data-stu-id="25c48-163">$100</span></span>            |
| <span data-ttu-id="25c48-164">$10</span><span class="sxs-lookup"><span data-stu-id="25c48-164">$10</span></span>                  | <span data-ttu-id="25c48-165">$10</span><span class="sxs-lookup"><span data-stu-id="25c48-165">$10</span></span>                  | <span data-ttu-id="25c48-166">$10</span><span class="sxs-lookup"><span data-stu-id="25c48-166">$10</span></span>             |
| <span data-ttu-id="25c48-167">$1</span><span class="sxs-lookup"><span data-stu-id="25c48-167">$1</span></span>                   | <span data-ttu-id="25c48-168">$1</span><span class="sxs-lookup"><span data-stu-id="25c48-168">$1</span></span>                   | <span data-ttu-id="25c48-169">$1</span><span class="sxs-lookup"><span data-stu-id="25c48-169">$1</span></span>              |

<span data-ttu-id="25c48-170">Weitere Informationen zum Erstellen von Tabellen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="25c48-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="25c48-171">Abschnitt zur Markdig-[Tabellenumbruchfunktion](#table-wrapping), die bei der Formatierung breiter Tabellen hilfreich sein kann</span><span class="sxs-lookup"><span data-stu-id="25c48-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="25c48-172">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organisieren von Daten mit Tabellen) von GitHub</span><span class="sxs-lookup"><span data-stu-id="25c48-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="25c48-173">Die [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)-Web-App (Markdowntabellengenerator)</span><span class="sxs-lookup"><span data-stu-id="25c48-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="25c48-174">Markdown Cheatsheet von Adam Pritchard</span><span class="sxs-lookup"><span data-stu-id="25c48-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="25c48-175">Markdown Extra von Michel Fortin</span><span class="sxs-lookup"><span data-stu-id="25c48-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="25c48-176">Convert HTML tables to Markdown (Konvertieren von HTML-Tabellen in Markdown)</span><span class="sxs-lookup"><span data-stu-id="25c48-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="25c48-177">Links</span><span class="sxs-lookup"><span data-stu-id="25c48-177">Links</span></span>

<span data-ttu-id="25c48-178">Die Markdownsyntax für einen Inlinelink besteht aus dem `[link text]`-Anteil, d.h. dem Text, der mit einem Hyperlink versehen wird, gefolgt vom `(file-name.md)`-Anteil, der aus der URL oder dem Dateinamen besteht, zu dem die Verknüpfung hergestellt wird:</span><span class="sxs-lookup"><span data-stu-id="25c48-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="25c48-179">Weitere Informationen zur Verknüpfung finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="25c48-179">For more information on linking, see:</span></span>

- <span data-ttu-id="25c48-180">Das Handbuch [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) enthält nähere Informationen zur grundlegenden Unterstützung von Verknüpfungen durch Markdown.</span><span class="sxs-lookup"><span data-stu-id="25c48-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="25c48-181">Der Abschnitt [Links](how-to-write-links.md) dieses Handbuchs enthält nähere Informationen zur zusätzlichen von Markdig bereitgestellten Verknüpfungssyntax.</span><span class="sxs-lookup"><span data-stu-id="25c48-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="25c48-182">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="25c48-182">Code snippets</span></span>

<span data-ttu-id="25c48-183">Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „eingezäunter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="25c48-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="25c48-184">Nähere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="25c48-184">For details, see:</span></span>

- <span data-ttu-id="25c48-185">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#precode) (Abschnitt zur nativen Unterstützung für Codeblöcke)</span><span class="sxs-lookup"><span data-stu-id="25c48-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="25c48-186">[Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Erstellen und Hervorheben von Codeblöcken)</span><span class="sxs-lookup"><span data-stu-id="25c48-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="25c48-187">Mit umzäunten Codeblöcken können Sie mühelos die Hervorhebung von Syntax für Ihre Codeausschnitte aktivieren.</span><span class="sxs-lookup"><span data-stu-id="25c48-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="25c48-188">Das allgemeine Format für umzäunte Codeblöcke ist:</span><span class="sxs-lookup"><span data-stu-id="25c48-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="25c48-189">Der Alias nach den anfänglichen drei „\`“-Zeichen definiert die zu verwendende Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="25c48-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="25c48-190">Die folgende Liste enthält in Dokumentationsinhalten gebräuchliche Programmiersprachen und die zugehörigen Kennzeichnungen:</span><span class="sxs-lookup"><span data-stu-id="25c48-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="25c48-191">Diese Sprachen verfügen über Unterstützung für den Anzeigenamen und die meisten über Sprachhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="25c48-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="25c48-192">Name</span><span class="sxs-lookup"><span data-stu-id="25c48-192">Name</span></span>|<span data-ttu-id="25c48-193">Markdownbezeichnung</span><span class="sxs-lookup"><span data-stu-id="25c48-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="25c48-194">.NET-Konsole</span><span class="sxs-lookup"><span data-stu-id="25c48-194">.NET Console</span></span>|<span data-ttu-id="25c48-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="25c48-195">dotnetcli</span></span>|
|<span data-ttu-id="25c48-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="25c48-196">ASP.NET (C#)</span></span>|<span data-ttu-id="25c48-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="25c48-197">aspx-csharp</span></span>|
|<span data-ttu-id="25c48-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="25c48-198">ASP.NET (VB)</span></span>|<span data-ttu-id="25c48-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="25c48-199">aspx-vb</span></span>|
|<span data-ttu-id="25c48-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="25c48-200">AzCopy</span></span>|<span data-ttu-id="25c48-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="25c48-201">azcopy</span></span>|
|<span data-ttu-id="25c48-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="25c48-202">Azure CLI</span></span>|<span data-ttu-id="25c48-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="25c48-203">azurecli</span></span>|
|<span data-ttu-id="25c48-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="25c48-204">Azure PowerShell</span></span>|<span data-ttu-id="25c48-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="25c48-205">azurepowershell</span></span>|
|<span data-ttu-id="25c48-206">C++</span><span class="sxs-lookup"><span data-stu-id="25c48-206">C++</span></span>|<span data-ttu-id="25c48-207">cpp</span><span class="sxs-lookup"><span data-stu-id="25c48-207">cpp</span></span>|
|<span data-ttu-id="25c48-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="25c48-208">C++/CX</span></span>|<span data-ttu-id="25c48-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="25c48-209">cppcx</span></span>|
|<span data-ttu-id="25c48-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="25c48-210">C++/WinRT</span></span>|<span data-ttu-id="25c48-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="25c48-211">cppwinrt</span></span>|
|<span data-ttu-id="25c48-212">C#</span><span class="sxs-lookup"><span data-stu-id="25c48-212">C#</span></span>|<span data-ttu-id="25c48-213">csharp</span><span class="sxs-lookup"><span data-stu-id="25c48-213">csharp</span></span>|
|<span data-ttu-id="25c48-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="25c48-214">CSHTML</span></span>|<span data-ttu-id="25c48-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="25c48-215">cshtml</span></span>|
|<span data-ttu-id="25c48-216">DAX</span><span class="sxs-lookup"><span data-stu-id="25c48-216">DAX</span></span>|<span data-ttu-id="25c48-217">dax</span><span class="sxs-lookup"><span data-stu-id="25c48-217">dax</span></span>|
|<span data-ttu-id="25c48-218">F#</span><span class="sxs-lookup"><span data-stu-id="25c48-218">F#</span></span>|<span data-ttu-id="25c48-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="25c48-219">fsharp</span></span>|
|<span data-ttu-id="25c48-220">Go</span><span class="sxs-lookup"><span data-stu-id="25c48-220">Go</span></span>|<span data-ttu-id="25c48-221">go</span><span class="sxs-lookup"><span data-stu-id="25c48-221">go</span></span>|
|<span data-ttu-id="25c48-222">HTML</span><span class="sxs-lookup"><span data-stu-id="25c48-222">HTML</span></span>|<span data-ttu-id="25c48-223">html</span><span class="sxs-lookup"><span data-stu-id="25c48-223">html</span></span>|
|<span data-ttu-id="25c48-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="25c48-224">HTTP</span></span>|<span data-ttu-id="25c48-225">http</span><span class="sxs-lookup"><span data-stu-id="25c48-225">http</span></span>|
|<span data-ttu-id="25c48-226">Java</span><span class="sxs-lookup"><span data-stu-id="25c48-226">Java</span></span>|<span data-ttu-id="25c48-227">java</span><span class="sxs-lookup"><span data-stu-id="25c48-227">java</span></span>|
|<span data-ttu-id="25c48-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="25c48-228">JavaScript</span></span>|<span data-ttu-id="25c48-229">javascript</span><span class="sxs-lookup"><span data-stu-id="25c48-229">javascript</span></span>|
|<span data-ttu-id="25c48-230">JSON</span><span class="sxs-lookup"><span data-stu-id="25c48-230">JSON</span></span>|<span data-ttu-id="25c48-231">json</span><span class="sxs-lookup"><span data-stu-id="25c48-231">json</span></span>|
|<span data-ttu-id="25c48-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="25c48-232">Markdown</span></span>|<span data-ttu-id="25c48-233">md</span><span class="sxs-lookup"><span data-stu-id="25c48-233">md</span></span>|
|<span data-ttu-id="25c48-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="25c48-234">NodeJS</span></span>|<span data-ttu-id="25c48-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="25c48-235">nodejs</span></span>|
|<span data-ttu-id="25c48-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="25c48-236">Objective-C</span></span>|<span data-ttu-id="25c48-237">objc</span><span class="sxs-lookup"><span data-stu-id="25c48-237">objc</span></span>|
|<span data-ttu-id="25c48-238">OData</span><span class="sxs-lookup"><span data-stu-id="25c48-238">OData</span></span>|<span data-ttu-id="25c48-239">odata</span><span class="sxs-lookup"><span data-stu-id="25c48-239">odata</span></span>|
|<span data-ttu-id="25c48-240">PHP</span><span class="sxs-lookup"><span data-stu-id="25c48-240">PHP</span></span>|<span data-ttu-id="25c48-241">php</span><span class="sxs-lookup"><span data-stu-id="25c48-241">php</span></span>|
|<span data-ttu-id="25c48-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="25c48-242">Power Apps Formula</span></span>|<span data-ttu-id="25c48-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="25c48-243">powerappsfl</span></span>|
|<span data-ttu-id="25c48-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="25c48-244">PowerShell</span></span>|<span data-ttu-id="25c48-245">powershell</span><span class="sxs-lookup"><span data-stu-id="25c48-245">powershell</span></span>|
|<span data-ttu-id="25c48-246">Python</span><span class="sxs-lookup"><span data-stu-id="25c48-246">Python</span></span>|<span data-ttu-id="25c48-247">python</span><span class="sxs-lookup"><span data-stu-id="25c48-247">python</span></span>|
|<span data-ttu-id="25c48-248">Q#</span><span class="sxs-lookup"><span data-stu-id="25c48-248">Q#</span></span>|<span data-ttu-id="25c48-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="25c48-249">qsharp</span></span>|
|<span data-ttu-id="25c48-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="25c48-250">Ruby</span></span>|<span data-ttu-id="25c48-251">ruby</span><span class="sxs-lookup"><span data-stu-id="25c48-251">ruby</span></span>|
|<span data-ttu-id="25c48-252">SQL</span><span class="sxs-lookup"><span data-stu-id="25c48-252">SQL</span></span>|<span data-ttu-id="25c48-253">sql</span><span class="sxs-lookup"><span data-stu-id="25c48-253">sql</span></span>|
|<span data-ttu-id="25c48-254">Swift</span><span class="sxs-lookup"><span data-stu-id="25c48-254">Swift</span></span>|<span data-ttu-id="25c48-255">swift</span><span class="sxs-lookup"><span data-stu-id="25c48-255">swift</span></span>|
|<span data-ttu-id="25c48-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="25c48-256">TypeScript</span></span>|<span data-ttu-id="25c48-257">typescript</span><span class="sxs-lookup"><span data-stu-id="25c48-257">typescript</span></span>|
|<span data-ttu-id="25c48-258">VB</span><span class="sxs-lookup"><span data-stu-id="25c48-258">VB</span></span>|<span data-ttu-id="25c48-259">vb</span><span class="sxs-lookup"><span data-stu-id="25c48-259">vb</span></span>|
|<span data-ttu-id="25c48-260">VSTS-CLI</span><span class="sxs-lookup"><span data-stu-id="25c48-260">VSTS CLI</span></span>|<span data-ttu-id="25c48-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="25c48-261">vstscli</span></span>|
|<span data-ttu-id="25c48-262">XAML</span><span class="sxs-lookup"><span data-stu-id="25c48-262">XAML</span></span>|<span data-ttu-id="25c48-263">xaml</span><span class="sxs-lookup"><span data-stu-id="25c48-263">xaml</span></span>|
|<span data-ttu-id="25c48-264">XML</span><span class="sxs-lookup"><span data-stu-id="25c48-264">XML</span></span>|<span data-ttu-id="25c48-265">xml</span><span class="sxs-lookup"><span data-stu-id="25c48-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="25c48-266">Beispiel: C\#</span><span class="sxs-lookup"><span data-stu-id="25c48-266">Example: C\#</span></span>

<span data-ttu-id="25c48-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="25c48-267">__Markdown__</span></span>

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

<span data-ttu-id="25c48-268">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="25c48-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="25c48-269">Beispiel: SQL</span><span class="sxs-lookup"><span data-stu-id="25c48-269">Example: SQL</span></span>

<span data-ttu-id="25c48-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="25c48-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="25c48-271">__Darstellung__</span><span class="sxs-lookup"><span data-stu-id="25c48-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="25c48-272">OPS: benutzerdefinierte Markdownerweiterungen</span><span class="sxs-lookup"><span data-stu-id="25c48-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="25c48-273">In Open Publishing Services (OPS) ist der Markdig-Parser für Markdown implementiert, der eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) aufweist.</span><span class="sxs-lookup"><span data-stu-id="25c48-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="25c48-274">Markdig fügt Funktionen über Markuperweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="25c48-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="25c48-275">Daher sind einige ausgewählte Artikel aus dem vollständigen OPS-Erstellungshandbuch als Referenz in diesem Handbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="25c48-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="25c48-276">(Sehen Sie sich beispielsweise „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis an.)</span><span class="sxs-lookup"><span data-stu-id="25c48-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="25c48-277">GFM wird in Dokumentationsartikeln für die meisten Formatierungsaufgaben wie Absätze, Links, Listen und Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="25c48-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="25c48-278">Zur weitergehenden Formatierung von Artikeln können folgende Markdig-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="25c48-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="25c48-279">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="25c48-279">Note blocks</span></span>
- <span data-ttu-id="25c48-280">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="25c48-280">Includes</span></span>
- <span data-ttu-id="25c48-281">Selektoren</span><span class="sxs-lookup"><span data-stu-id="25c48-281">Selectors</span></span>
- <span data-ttu-id="25c48-282">Eingebettete Videos</span><span class="sxs-lookup"><span data-stu-id="25c48-282">Embedded videos</span></span>
- <span data-ttu-id="25c48-283">Codeausschnitte/-beispiele</span><span class="sxs-lookup"><span data-stu-id="25c48-283">Code snippets/samples</span></span>

<span data-ttu-id="25c48-284">Die vollständige Liste finden Sie unter „Markdig- und Markdown-Erweiterungen“ und „Codeausschnitte“ im Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="25c48-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="25c48-285">Notizzettel</span><span class="sxs-lookup"><span data-stu-id="25c48-285">Note blocks</span></span>

<span data-ttu-id="25c48-286">Sie können aus vier Notizzetteltypen auswählen, um die Aufmerksamkeit auf bestimmten Inhalt zu richten:</span><span class="sxs-lookup"><span data-stu-id="25c48-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="25c48-287">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="25c48-287">NOTE</span></span>
- <span data-ttu-id="25c48-288">WARNUNG</span><span class="sxs-lookup"><span data-stu-id="25c48-288">WARNING</span></span>
- <span data-ttu-id="25c48-289">TIPP</span><span class="sxs-lookup"><span data-stu-id="25c48-289">TIP</span></span>
- <span data-ttu-id="25c48-290">WICHTIG</span><span class="sxs-lookup"><span data-stu-id="25c48-290">IMPORTANT</span></span>

<span data-ttu-id="25c48-291">Generell sollten Notizzettel sparsam verwendet werden, da sie eine empfindliche Unterbrechung darstellen können.</span><span class="sxs-lookup"><span data-stu-id="25c48-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="25c48-292">Sie unterstützen zwar Codeblöcke, Bilder, Listen und Links, halten Sie sie aber trotzdem möglichst unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="25c48-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="25c48-293">Einbeziehungen</span><span class="sxs-lookup"><span data-stu-id="25c48-293">Includes</span></span>

<span data-ttu-id="25c48-294">Wenn wiederverwendbarer Text oder Bilddateien in Artikeldateien einbezogen werden müssen, können Sie über die Markdig-Dateieinbeziehungsfunktion einen Verweis auf die Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="25c48-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="25c48-295">Diese Funktion weist OPS an, die jeweilige Datei zur Erstellungszeit in Ihre Artikeldatei einzubeziehen, sodass sie ein Teil des veröffentlichten Artikels ist.</span><span class="sxs-lookup"><span data-stu-id="25c48-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="25c48-296">Um das Wiederverwenden von Inhalt zu erleichtern, können Sie drei Einbeziehungstypen verwenden:</span><span class="sxs-lookup"><span data-stu-id="25c48-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="25c48-297">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines anderen Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="25c48-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="25c48-298">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="25c48-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="25c48-299">Bilder: So wird die Standardeinbeziehung von Bildern in Dokumente implementiert.</span><span class="sxs-lookup"><span data-stu-id="25c48-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="25c48-300">Inline- oder Blockeinbeziehungen sind einfache Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="25c48-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="25c48-301">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="25c48-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="25c48-302">Alle Markdownincludedateien sollten im Stamm des Repositorys in einem [gemeinsamen `/includes`-Unterverzeichnis](git-github-fundamentals.md#includes-subdirectory) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="25c48-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="25c48-303">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="25c48-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="25c48-304">Die Anforderungen und Überlegungen zu Einbeziehungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25c48-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="25c48-305">Verwenden Sie stets dann Einbeziehungen, wenn der gleiche Text in verschiedenen Artikeln enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="25c48-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="25c48-306">Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="25c48-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="25c48-307">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="25c48-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="25c48-308">Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Markdig-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="25c48-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="25c48-309">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="25c48-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="25c48-310">Stellen Sie sicher, dass sämtlicher Text in einer Einbeziehung in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Einbeziehung verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="25c48-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="25c48-311">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt und damit die Lokalisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="25c48-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="25c48-312">Betten Sie keine Einbeziehungen in andere Einbeziehungen ein.</span><span class="sxs-lookup"><span data-stu-id="25c48-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="25c48-313">Sie werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25c48-313">They are not supported.</span></span>
- <span data-ttu-id="25c48-314">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z.B. der Ordner `<repo>`/includes/media).</span><span class="sxs-lookup"><span data-stu-id="25c48-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="25c48-315">Der Stamm des Medienverzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="25c48-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="25c48-316">Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes Medienverzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25c48-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="25c48-317">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="25c48-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="25c48-318">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="25c48-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="25c48-319">Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="25c48-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="25c48-320">Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="25c48-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="25c48-321">Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="25c48-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="25c48-322">Selektoren</span><span class="sxs-lookup"><span data-stu-id="25c48-322">Selectors</span></span>

<span data-ttu-id="25c48-323">Verwenden Sie Selektoren in technischen Artikeln, wenn Sie mehrere Varianten des gleichen Artikels erstellen, um Implementierungsunterschiede einzelner Technologien bzw. Plattformen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="25c48-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="25c48-324">Dies gilt in der Regel am meisten für unsere Inhalte für mobile Plattformen, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="25c48-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="25c48-325">Es gibt derzeit zwei unterschiedliche Selektortypen in Markdig: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="25c48-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="25c48-326">Da derselbe Markdownselektor in jedem Artikel der Auswahl erwähnt wird, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Einbeziehung platzieren.</span><span class="sxs-lookup"><span data-stu-id="25c48-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="25c48-327">Dann können Sie auf diese Einbeziehung in allen Artikeln, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="25c48-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="25c48-328">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="25c48-328">Code snippets</span></span>

<span data-ttu-id="25c48-329">Markdig unterstützt über die Codeausschnitterweiterung die erweiterte Einbeziehung von Code in einen Artikel.</span><span class="sxs-lookup"><span data-stu-id="25c48-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="25c48-330">DFM bietet erweitertes Rendern, das auf GFM-Funktionen wie Programmieren der Sprachauswahl und farbiger Syntaxmarkierung sowie netten Funktionen wie den folgenden basiert:</span><span class="sxs-lookup"><span data-stu-id="25c48-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="25c48-331">Einbeziehung zentralisierter Codebeispiele bzw. -ausschnitte aus einem externen Repository</span><span class="sxs-lookup"><span data-stu-id="25c48-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="25c48-332">Benutzeroberfläche mit Registerkarten zur Anzeige mehrerer Versionen von Codebeispielen in verschiedenen Sprachen</span><span class="sxs-lookup"><span data-stu-id="25c48-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="25c48-333">Häufige Fehler und Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="25c48-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="25c48-334">Alternativtext</span><span class="sxs-lookup"><span data-stu-id="25c48-334">Alt text</span></span>

<span data-ttu-id="25c48-335">Alternativtext, der Unterstriche enthält, wird nicht korrekt gerendert.</span><span class="sxs-lookup"><span data-stu-id="25c48-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="25c48-336">Verwenden Sie beispielsweise anstelle von</span><span class="sxs-lookup"><span data-stu-id="25c48-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="25c48-337">diese Möglichkeit zur Umgehung von Unterstrichen:</span><span class="sxs-lookup"><span data-stu-id="25c48-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="25c48-338">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="25c48-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="25c48-339">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="25c48-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="25c48-340">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="25c48-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="25c48-341">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="25c48-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="25c48-342">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="25c48-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="25c48-343">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="25c48-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="25c48-344">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="25c48-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="25c48-345">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="25c48-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="25c48-346">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="25c48-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="25c48-347">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="25c48-347">Angle brackets</span></span>

<span data-ttu-id="25c48-348">Wenn Sie in Ihrer Datei geschweifte Klammern im Text (nicht Code) verwenden, z.B. zur Bezeichnung eines Platzhalters, müssen Sie die geschweiften Klammern manuell codieren.</span><span class="sxs-lookup"><span data-stu-id="25c48-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="25c48-349">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="25c48-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="25c48-350">Codieren Sie `<script name>` z.B. als `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="25c48-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="25c48-351">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25c48-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="25c48-352">Markdownressourcen</span><span class="sxs-lookup"><span data-stu-id="25c48-352">Markdown resources</span></span>

- <span data-ttu-id="25c48-353">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Einführung)</span><span class="sxs-lookup"><span data-stu-id="25c48-353">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="25c48-354">Cheatsheet zur Markdown-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="25c48-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="25c48-355">[Getting started with writing and formatting on GitHub](https://help.github.com/articles/markdown-basics/) (Erste Schritte: Schreiben und Formatieren auf GitHub) Grundlegendes zu Markdown</span><span class="sxs-lookup"><span data-stu-id="25c48-355">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
