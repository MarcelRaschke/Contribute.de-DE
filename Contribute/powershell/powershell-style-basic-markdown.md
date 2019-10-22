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
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="ddb46-103">Markdown-Styleguide für PowerShell-Dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ddb46-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="ddb46-104">Dieser Artikel enthält stilistische Anweisungen für PowerShell-Dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="ddb46-105">Andere Leitfäden zum Schreibstil finden Sie im [Microsoft-Styleguide](https://docs.microsoft.com/style-guide/welcome/).</span><span class="sxs-lookup"><span data-stu-id="ddb46-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="ddb46-106">Metadaten</span><span class="sxs-lookup"><span data-stu-id="ddb46-106">Metadata</span></span>

<span data-ttu-id="ddb46-107">Diese Vorlage enthält Beispiele für die Markdownsyntax sowie Anweisungen zum Einstellen der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="ddb46-108">Beim Erstellen einer Markdowndatei sollten Sie die enthaltene Vorlage in eine neue Datei kopieren, die Metadaten wie unten gezeigt ausfüllen und den Titel des Artikels in der obigen H1-Überschrift festlegen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="ddb46-109">Der erforderliche Metadatenblock befindet sich im folgenden Metadatenblockbeispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="ddb46-110">Sie **müssen** zwischen dem Doppelpunkt („:“) und dem Wert eines Metadatenelements ein Leerzeichen setzen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="ddb46-111">Doppelpunkte in einem Wert (z.B. in einem Titel) unterbrechen den Metadatenparser.</span><span class="sxs-lookup"><span data-stu-id="ddb46-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="ddb46-112">In diesem Fall müssen Sie doppelte Anführungszeichen um den Titel setzen (z.B. `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="ddb46-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="ddb46-113">**author**: Das Feld „author“ (Autor) sollte den **GitHub-Benutzernamen** des Autors enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="ddb46-114">**description**: Zusammenfassung des Artikelinhalts.</span><span class="sxs-lookup"><span data-stu-id="ddb46-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="ddb46-115">Für gewöhnlich wird diese Beschreibung in den Suchergebnissen angezeigt, jedoch wird sie nicht für die Suchrangfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddb46-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="ddb46-116">Einschließlich der Leerzeichen sollte die Länge der Beschreibung zwischen 115 und 145 Zeichen liegen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="ddb46-117">**ms.date**: Das Datum des letzten wichtigen Updates.</span><span class="sxs-lookup"><span data-stu-id="ddb46-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="ddb46-118">Aktualisieren Sie dieses Datum bei vorhandenen Artikeln, wenn Sie einen gesamten Artikel prüfen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ddb46-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="ddb46-119">Kleine Fehlerbehebungen, z. B. Tippfehler oder ähnliches, rechtfertigen ein Update nicht.</span><span class="sxs-lookup"><span data-stu-id="ddb46-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="ddb46-120">**title**: Wird in den Ergebnissen von Suchmaschinen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="ddb46-121">Der Titel sollte nicht mit dem Titel in Ihrer H1-Überschrift übereinstimmen und darf maximal 60 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="ddb46-122">An jeden Artikel werden weitere Metadaten angefügt, allerdings werden die meisten Metadatenwerte in der Regel auf der Ordnerebene angewendet. Dies wird in der Datei **docfx.json** angegeben.</span><span class="sxs-lookup"><span data-stu-id="ddb46-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="ddb46-123">Produktterminologie</span><span class="sxs-lookup"><span data-stu-id="ddb46-123">Product Terminology</span></span>

<span data-ttu-id="ddb46-124">Es gibt verschiedene Varianten von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddb46-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="ddb46-125">In der folgenden Tabelle werden einige verschiedene Begriffe definiert, die bei der Erörterung von PowerShell verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="ddb46-126">**PowerShell:** Dies ist die Standardversion.</span><span class="sxs-lookup"><span data-stu-id="ddb46-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="ddb46-127">PowerShell ist das von Microsoft veröffentlichte Produkt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="ddb46-128">Der Begriff PowerShell kann verwendet werden, um eine beliebige Edition des Produkts zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ddb46-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="ddb46-129">**PowerShell Core:** Dies ist PowerShell basierend auf der .NET CoreCLR (Common Language Runtime) für unterstützte Plattformen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="ddb46-130">**Windows PowerShell:** Dies ist PowerShell basierend auf der .NET Framework-CLR.</span><span class="sxs-lookup"><span data-stu-id="ddb46-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="ddb46-131">Windows PowerShell wird nur für Windows bereitgestellt und umfasst die vollständige .NET Framework-CLR.</span><span class="sxs-lookup"><span data-stu-id="ddb46-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="ddb46-132">„Windows PowerShell“ kann im Allgemeinen in „PowerShell“ geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="ddb46-133">„Windows PowerShell“ sollte **nicht** geändert werden, wenn Windows-spezifische Technologien behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="ddb46-134">Grundlegendes Markdown, GFM und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="ddb46-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="ddb46-135">Die Grundlagen von Markdown, GFM (GitHub Flavored Markdown) und OPS-spezifischen Erweiterungen können Sie anhand des allgemeinen Artikels zu [Markdown](../how-to-write-use-markdown.md) und der [Markdownreferenz](../markdown-reference.md) erlernen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](../how-to-write-use-markdown.md) and [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="ddb46-136">Markdown nutzt Sonderzeichen wie \*, \` und \# für die Formatierung.</span><span class="sxs-lookup"><span data-stu-id="ddb46-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="ddb46-137">Wenn Sie eines dieser Zeichen in Ihren Inhalt einfügen möchten, müssen Sie eine der folgenden Vorgehensweisen anwenden:</span><span class="sxs-lookup"><span data-stu-id="ddb46-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="ddb46-138">Versehen Sie das Sonderzeichen mit einem umgekehrten Schrägstrich als Escapezeichen (z.B. `\*` für \*).</span><span class="sxs-lookup"><span data-stu-id="ddb46-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="ddb46-139">Verwenden Sie den [HTML-Code](http://www.ascii.cl/htmlcodes.htm) für das Zeichen (z.B. `&#42;` für &#42;).</span><span class="sxs-lookup"><span data-stu-id="ddb46-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="ddb46-140">Markdowndateien sollten nur ASCII-Text oder die UTF-8-Codierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="ddb46-141">Vermeiden Sie jedoch die Verwendung von UTF-8-Zeichen mit mehreren Bytes.</span><span class="sxs-lookup"><span data-stu-id="ddb46-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="ddb46-142">Verwenden Sie stattdessen eine HTML-Entität.</span><span class="sxs-lookup"><span data-stu-id="ddb46-142">Instead use an HTML entity.</span></span> <span data-ttu-id="ddb46-143">Verwenden Sie beispielsweise für Copyrightsymbole `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="ddb46-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="ddb46-144">Es wird als „&copy;“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="ddb46-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="ddb46-145">Links</span><span class="sxs-lookup"><span data-stu-id="ddb46-145">Hyperlinks</span></span>

- <span data-ttu-id="ddb46-146">Vermeiden Sie die Verwendung bloßer URLs.</span><span class="sxs-lookup"><span data-stu-id="ddb46-146">Avoid using bare URLs.</span></span> <span data-ttu-id="ddb46-147">Verwenden Sie für Links die Markdownsyntax `[friendlyname](url-or-path)`.</span><span class="sxs-lookup"><span data-stu-id="ddb46-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="ddb46-148">Links sollten einen Anzeigenamen haben. In den meisten Fällen eignet sich der Titel des Artikels.</span><span class="sxs-lookup"><span data-stu-id="ddb46-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="ddb46-149">Alle Elemente im Abschnitt „Verwandte Links“ ganz unten sollten Links sein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="ddb46-150">Verwenden Sie relative Links, wenn Sie Links zu anderen Inhalten auf **docs.microsoft.com** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="ddb46-151">Verwenden Sie innerhalb der Klammern eines Links keine Backticks, keinen Fettdruck und kein anderes Markup.</span><span class="sxs-lookup"><span data-stu-id="ddb46-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="ddb46-152">Ausführlichere Informationen zu Links finden Sie unter [Verwenden von Links in der Dokumentation](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="ddb46-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="ddb46-153">Dateinamen</span><span class="sxs-lookup"><span data-stu-id="ddb46-153">Filenames</span></span>

<span data-ttu-id="ddb46-154">Dateinamen unterliegen folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="ddb46-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="ddb46-155">Sie dürfen nur Buchstaben, Zahlen und Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="ddb46-156">Leer- oder Satzzeichen sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="ddb46-157">Worte und Zahlen im Dateinamen werden durch Bindestriche getrennt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="ddb46-158">Verwenden Sie Verben, die den Zweck angeben, z.B. develop, buy, build, troubleshoot.</span><span class="sxs-lookup"><span data-stu-id="ddb46-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="ddb46-159">Auf „-ing“ endenden Worte dürfen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-159">No -ing words.</span></span>
- <span data-ttu-id="ddb46-160">Kurze Worte wie a, and, the, in, or usw. sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="ddb46-161">Das Markdownformat und die Erweiterung „.md“ sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ddb46-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="ddb46-162">Verwenden Sie angemessene, kurze Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-162">Keep file names reasonably short.</span></span> <span data-ttu-id="ddb46-163">Sie sind Teil der URL für Ihre Artikel.</span><span class="sxs-lookup"><span data-stu-id="ddb46-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="ddb46-164">Leerzeilen, Leerzeichen und Tabstopps</span><span class="sxs-lookup"><span data-stu-id="ddb46-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="ddb46-165">Entfernen Sie doppelte Leerzeilen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="ddb46-166">Mehrere Leerzeilen werden in HTML als eine Leerzeile dargestellt, mehrere Leerzeilen haben also keinen Zweck.</span><span class="sxs-lookup"><span data-stu-id="ddb46-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="ddb46-167">Leerzeilen geben außerdem das Ende eines Blocks in Markdown an.</span><span class="sxs-lookup"><span data-stu-id="ddb46-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="ddb46-168">Es sollte eine einzelne Leerzeile zwischen Markdownblöcken mit verschiedenen Typen geben (z. B. zwischen einem Paragraphen und einer Liste oder Überschrift).</span><span class="sxs-lookup"><span data-stu-id="ddb46-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="ddb46-169">Abstände sind in Markdown wichtig.</span><span class="sxs-lookup"><span data-stu-id="ddb46-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="ddb46-170">Verwenden Sie immer Leerzeichen anstelle von harten Tabstopps.</span><span class="sxs-lookup"><span data-stu-id="ddb46-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="ddb46-171">Entfernen Sie zusätzliche Leerzeichen am Ende von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="ddb46-172">Titel und Überschriften</span><span class="sxs-lookup"><span data-stu-id="ddb46-172">Titles and headings</span></span>

<span data-ttu-id="ddb46-173">Verwenden Sie nur [ATX-Überschriften][atx] (#-Format, anstatt `=`- oder `-`-Überschriften).</span><span class="sxs-lookup"><span data-stu-id="ddb46-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="ddb46-174">Befolgen Sie die Rechtschreibregeln gemäß Duden (empfohlene Schreibweise).</span><span class="sxs-lookup"><span data-stu-id="ddb46-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="ddb46-175">Zwischen `#` und dem ersten Buchstaben der Überschrift muss ein einzelnes Leerzeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="ddb46-176">Überschriften sollten von einzelnen Leerzeilen umgeben sein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="ddb46-177">Für jedes Dokument ist nur eine H1-Überschrift zulässig.</span><span class="sxs-lookup"><span data-stu-id="ddb46-177">Only one H1 per document</span></span>
- <span data-ttu-id="ddb46-178">Überschriftstufen sollten immer um eine Stufe erhöht werden. Überspringen Sie keine Stufen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="ddb46-179">Verwenden Sie keine Backticks, keinen Fettdruck und kein anderes Markup in Überschriften.</span><span class="sxs-lookup"><span data-stu-id="ddb46-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="ddb46-180">Das von [PlatyPS][platyPS] erzwungene Schema für die Cmdlet-Referenz erfordert spezifische H2- und H3-Überschriften.</span><span class="sxs-lookup"><span data-stu-id="ddb46-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="ddb46-181">Das Hinzufügen oder Entfernen von Überschriften kann den Build unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="ddb46-182">Weitere Informationen finden Sie im [Styleguide für die Cmdlet-Referenz](powershell-style-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ddb46-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="ddb46-183">Schränken Sie die Zeilenlänge auf 100 Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="ddb46-184">Dadurch wird die Befehlszeilenausgabe für Unterschiede und Verläufe vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ddb46-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="ddb46-185">Für den Großteil der vorhandenen Inhalte der PowerShell-Dokumentationen war diese Regel noch nicht in Kraft, sie wird jedoch im Laufe der Zeit implementiert.</span><span class="sxs-lookup"><span data-stu-id="ddb46-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="ddb46-186">Sie können uns dabei gerne unterstützen. Die [Reflow-Erweiterung][reflow] für Visual Studio Code (VS Code) vereinfacht das erneute Formatieren von Paragraphen gemäß dieser Regel.</span><span class="sxs-lookup"><span data-stu-id="ddb46-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="ddb46-187">Listen</span><span class="sxs-lookup"><span data-stu-id="ddb46-187">Lists</span></span>

<span data-ttu-id="ddb46-188">Wenn Ihre Liste mehrere Sätze oder Paragraphen enthält, sollten Sie Unterüberschriften anstelle einer Liste in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="ddb46-189">Listen sollten von einzelnen Leerzeilen umgeben sein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="ddb46-190">Unsortierte Listen</span><span class="sxs-lookup"><span data-stu-id="ddb46-190">Unordered lists</span></span>

<span data-ttu-id="ddb46-191">Beenden Sie Listenelemente nicht mit einem Punkt, es sei denn, sie enthalten mehrere Sätze.</span><span class="sxs-lookup"><span data-stu-id="ddb46-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="ddb46-192">Verwenden Sie das Bindestrichzeichen (`-`) für Aufzählungen von Listenelementen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="ddb46-193">Dadurch wird Verwirrung mit Markup für Fett und Kursiv vermieden, die das Sternchenzeichen [`*`] verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="ddb46-194">Fügen Sie einen Zeilenumbruch ein, und passen Sie den Einzug an das erste Zeichen der Aufzählung an, um einen Paragraphen oder andere Elemente unter ein Aufzählungselement einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="ddb46-195">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="ddb46-196">Dies ist eine Liste, die untergeordnete Elemente unter einem Aufzählungselement enthält.</span><span class="sxs-lookup"><span data-stu-id="ddb46-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="ddb46-197">Erstes Aufzählungselement</span><span class="sxs-lookup"><span data-stu-id="ddb46-197">First bullet item</span></span>

  <span data-ttu-id="ddb46-198">Satz zur Erläuterung des ersten Elements.</span><span class="sxs-lookup"><span data-stu-id="ddb46-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="ddb46-199">Untergeordnetes Aufzählungselement</span><span class="sxs-lookup"><span data-stu-id="ddb46-199">Sub-bullet item</span></span>

    <span data-ttu-id="ddb46-200">Satz zur Erläuterung des untergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="ddb46-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="ddb46-201">Zweites Aufzählungselement</span><span class="sxs-lookup"><span data-stu-id="ddb46-201">Second bullet item</span></span>
- <span data-ttu-id="ddb46-202">Drittes Aufzählungselement</span><span class="sxs-lookup"><span data-stu-id="ddb46-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="ddb46-203">Sortierte Listen</span><span class="sxs-lookup"><span data-stu-id="ddb46-203">Ordered lists</span></span>

<span data-ttu-id="ddb46-204">Passen Sie den Einzug an das erste Zeichen nach der Elementnummer an, um einen Paragraphen oder andere Elemente unter einem nummerierten Element einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

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

<span data-ttu-id="ddb46-205">So erhalten Sie diese Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="ddb46-205">to get this output:</span></span>

> 1. <span data-ttu-id="ddb46-206">Fügen Sie für das erste Element ein einzelnes Leerzeichen nach der „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="ddb46-207">Lange Sätze sollten einen Zeilenumbruch enthalten und müssen am ersten Zeichen nach dem Marker für die nummerierte Liste ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="ddb46-208">Fügen Sie einen Zeilenumbruch nach dem ersten Element ein, und passen Sie die Einzüge an, um ein zweites Element (wie dieses hier) einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="ddb46-209">Der Einzug des zweiten Elements muss am ersten Zeichen nach dem Marker für die nummerierte Liste ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="ddb46-210">Für einstellige Ziffernelemente, wie dieses, fügen Sie einen Einzug bis Spalte 4 ein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="ddb46-211">Für zweistellige Ziffernelemente, z. B. ein Element mit der Nummer 10, fügen Sie einen Einzug bis Spalte 5 ein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="ddb46-212">Das nächste nummerierte Element beginnt hier.</span><span class="sxs-lookup"><span data-stu-id="ddb46-212">The next numbered item starts here.</span></span>

<span data-ttu-id="ddb46-213">Alle Elemente in einer nummerierten Liste sollten die Zahl `1.` enthalten, anstatt die Zahl für jedes Element zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="ddb46-214">Das Markdownrendering erhöht den Wert automatisch.</span><span class="sxs-lookup"><span data-stu-id="ddb46-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="ddb46-215">Dadurch wird das Neuanordnen von Elementen einfacher und der Einzug von untergeordneten Inhalten wird standardisiert.</span><span class="sxs-lookup"><span data-stu-id="ddb46-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="ddb46-216">Formatieren von Befehlssyntaxelementen</span><span class="sxs-lookup"><span data-stu-id="ddb46-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="ddb46-217">Namen von PowerShell-Cmdlets werden mit der [Pascal-Schreibweise][pascal-case] geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ddb46-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="ddb46-218">Verben werden mithilfe eines Bindestrichs von Substantiven getrennt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="ddb46-219">Verwenden Sie immer den vollständigen Namen in der Pascal-Schreibweise für Cmdlets und Parameter.</span><span class="sxs-lookup"><span data-stu-id="ddb46-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="ddb46-220">Vermeiden Sie die Verwendung von Aliasen, es sei denn, Sie schreiben spezifisch über Aliase.</span><span class="sxs-lookup"><span data-stu-id="ddb46-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="ddb46-221">Schlüsselwörter der Sprache, Cmdlet-Namen und Variablenverweise sollten in Paragraphen von Backtickzeichen (`` ` ``) umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="ddb46-222">Eigenschaft, Parameter und Klassennamen sollten **Fett** sein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="ddb46-223">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="ddb46-224">Wenn Sie einen Parameter bei Namen nennen, sollte der Name **fett** geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="ddb46-225">Wenn Sie die Verwendung eines Parameters mithilfe eines Bindestrichs als Präfix darstellen, sollte der Parameter von Backticks umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="ddb46-226">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="ddb46-227">Wenn Sie über externe Befehle (EXE-Dateien, Skripts usw.) schreiben, sollte der Befehlsname fett und in Kleinbuchstaben (oder am Anfang eines Satzes groß) geschrieben werden sowie die entsprechende Dateierweiterung enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="ddb46-228">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="ddb46-229">Wenn Sie die Verwendung eines externen Befehls veranschaulichen, sollte das Beispiel von Backticks umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="ddb46-230">Wenn ein Namenskonflikt mit einem Alias vorliegt, müssen Sie die Dateierweiterung in das Befehlsbeispiel einfügen.</span><span class="sxs-lookup"><span data-stu-id="ddb46-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="ddb46-231">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="ddb46-232">Wenn Sie einen Konzeptartikel schreiben (im Gegensatz zu Referenzinhalten), sollte das erste Vorkommnis eines Cmdlet-Namens ein Link zur Dokumentation des Cmdlets sein.</span><span class="sxs-lookup"><span data-stu-id="ddb46-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="ddb46-233">Verwenden Sie innerhalb der Klammern eines Links keine Backticks, keinen Fettdruck und kein anderes Markup.</span><span class="sxs-lookup"><span data-stu-id="ddb46-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="ddb46-234">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="ddb46-235">Weitere Informationen finden Sie im Abschnitt [Links](#hyperlinks) des Styleguides.</span><span class="sxs-lookup"><span data-stu-id="ddb46-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="ddb46-236">Bilder</span><span class="sxs-lookup"><span data-stu-id="ddb46-236">Images</span></span>

<span data-ttu-id="ddb46-237">Verwenden Sie zum Einbetten eines Bilds die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="ddb46-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="ddb46-238">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ddb46-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="ddb46-239">`alt text` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild.</span><span class="sxs-lookup"><span data-stu-id="ddb46-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="ddb46-240">Für visuell eingeschränkte Menschen ist Alternativtext erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ddb46-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="ddb46-241">Dies ist außerdem nützlich, wenn auf der Website ein Fehler auftritt, durch den das Bild nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ddb46-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="ddb46-242">Bilder sollten in einem `media/<article-name>`-Ordner innerhalb des Ordners gespeichert werden, der Ihren Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="ddb46-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="ddb46-243">Ein Bild sollte nicht in mehreren Artikeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-243">Images should not be shared between articles.</span></span> <span data-ttu-id="ddb46-244">Erstellen Sie einen Ordner, der mit dem Dateinamen Ihres Artikels im `media`-Ordner übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="ddb46-245">Kopieren Sie die Bilder für diesen Artikel in diesen neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="ddb46-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="ddb46-246">Wenn ein Bild in mehreren Artikeln verwendet wird, muss jeder Bildordner eine Kopie dieser Bilddatei enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb46-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="ddb46-247">Durch diese Vorgehensweise wird verhindert, dass eine Änderung an einem Bild in einem Artikel sich auf einen anderen Artikel auswirkt.</span><span class="sxs-lookup"><span data-stu-id="ddb46-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="ddb46-248">In manchen Fällen möchten Sie Bilder, z. B. Logos und Symbole, in mehreren Artikeln verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddb46-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="ddb46-249">Diese Bilder werden im `/media/shared`-Ordner im Stammverzeichnis des Repositorys gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ddb46-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="ddb46-250">Die folgenden Bilddateitypen werden unterstützt: „*.png“, „*.gif“, „*.jpeg“, „*.jpg“, „\*.svg“.</span><span class="sxs-lookup"><span data-stu-id="ddb46-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
