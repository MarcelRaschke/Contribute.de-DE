---
title: Vorlage und Spickzettel für .NET-Artikel
description: In diesem Artikel ist eine praktische Vorlage enthalten, die Sie zum Erstellen neuer Artikel für die Repositorys der .NET-Dokumentation verwenden können.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 15288ccb1831e994fd078f47788ad4c2f502775c
ms.sourcegitcommit: 92d06515af1d9d0e5abf632fc3b6425c487174d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90837210"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="56e05-103">Metadaten und Markdownvorlage für .NET-Dokumentationen</span><span class="sxs-lookup"><span data-stu-id="56e05-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="56e05-104">Diese dotnet/docs-Vorlage enthält Beispiele für die Markdownsyntax sowie Anweisungen zum Einstellen der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="56e05-104">This dotnet/docs template contains examples of Markdown syntax and guidance on setting the metadata.</span></span>

<span data-ttu-id="56e05-105">Beim Erstellen einer Markdowndatei sollten Sie die enthaltene Vorlage in eine neue Datei kopieren, die Metadaten wie unten gezeigt ausfüllen und den Titel des Artikels in der obigen H1-Überschrift festlegen.</span><span class="sxs-lookup"><span data-stu-id="56e05-105">When creating a Markdown file, copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="56e05-106">Metadaten</span><span class="sxs-lookup"><span data-stu-id="56e05-106">Metadata</span></span>

<span data-ttu-id="56e05-107">Der erforderliche Metadatenblock befindet sich im folgenden Metadatenblockbeispiel:</span><span class="sxs-lookup"><span data-stu-id="56e05-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="56e05-108">Sie **müssen** zwischen dem Doppelpunkt („:“) und dem Wert eines Metadatenelements ein Leerzeichen setzen.</span><span class="sxs-lookup"><span data-stu-id="56e05-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="56e05-109">Doppelpunkte in einem Wert (z.B. in einem Titel) unterbrechen den Metadatenparser.</span><span class="sxs-lookup"><span data-stu-id="56e05-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="56e05-110">In diesem Fall müssen Sie doppelte Anführungszeichen um den Titel setzen (z.B. `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="56e05-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="56e05-111">**title**: Wird in den Ergebnissen von Suchmaschinen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56e05-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="56e05-112">Der Titel sollte nicht mit dem Titel in Ihrer H1-Überschrift übereinstimmen und darf maximal 60 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="56e05-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="56e05-113">**description**: Zusammenfassung des Artikelinhalts.</span><span class="sxs-lookup"><span data-stu-id="56e05-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="56e05-114">Für gewöhnlich wird diese Beschreibung in den Suchergebnissen angezeigt, jedoch wird sie nicht für die Suchrangfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="56e05-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="56e05-115">Einschließlich der Leerzeichen sollte die Länge der Beschreibung zwischen 115 und 145 Zeichen liegen.</span><span class="sxs-lookup"><span data-stu-id="56e05-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="56e05-116">**author**: Das Feld „author“ (Autor) sollte den **GitHub-Benutzernamen** des Autors enthalten.</span><span class="sxs-lookup"><span data-stu-id="56e05-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="56e05-117">**ms.date**: Das Datum des letzten wichtigen Updates.</span><span class="sxs-lookup"><span data-stu-id="56e05-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="56e05-118">Aktualisieren Sie dieses Datum bei vorhandenen Artikeln, wenn Sie einen gesamten Artikel prüfen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="56e05-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="56e05-119">Kleine Fehlerbehebungen, z.B. Tippfehler oder ähnliches, rechtfertigen ein Update nicht.</span><span class="sxs-lookup"><span data-stu-id="56e05-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="56e05-120">An jeden Artikel werden weitere Metadaten angefügt, allerdings werden die meisten Metadatenwerte in der Regel auf der Ordnerebene angewendet. Dies wird in der Datei **docfx.json** angegeben.</span><span class="sxs-lookup"><span data-stu-id="56e05-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="56e05-121">Grundlegendes Markdown, GFM und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="56e05-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="56e05-122">Die Grundlagen von Markdown, GFM (GitHub Flavored Markdown) und OPS-spezifischen Erweiterungen können Sie anhand des Artikels [Markdownreferenz](../markdown-reference.md) erlernen.</span><span class="sxs-lookup"><span data-stu-id="56e05-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS-specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="56e05-123">Markdown nutzt Sonderzeichen wie \*, \` und \# für die Formatierung.</span><span class="sxs-lookup"><span data-stu-id="56e05-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="56e05-124">Wenn Sie eines dieser Zeichen in Ihren Inhalt einfügen möchten, müssen Sie eine der folgenden Vorgehensweisen anwenden:</span><span class="sxs-lookup"><span data-stu-id="56e05-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="56e05-125">Versehen Sie das Sonderzeichen mit einem umgekehrten Schrägstrich als Escapezeichen (z. B. `\*` für \*).</span><span class="sxs-lookup"><span data-stu-id="56e05-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*).</span></span>
- <span data-ttu-id="56e05-126">Verwenden Sie den [HTML-Code](http://www.ascii.cl/htmlcodes.htm) für das Zeichen (z.B. `&#42;` für &#42;).</span><span class="sxs-lookup"><span data-stu-id="56e05-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="56e05-127">Dateinamen</span><span class="sxs-lookup"><span data-stu-id="56e05-127">File names</span></span>

<span data-ttu-id="56e05-128">Dateinamen unterliegen folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="56e05-128">File names use the following rules:</span></span>

* <span data-ttu-id="56e05-129">Nur Kleinbuchstaben, Zahlen und Bindestriche sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="56e05-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="56e05-130">Leer- oder Satzzeichen sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="56e05-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="56e05-131">Worte und Zahlen im Dateinamen werden durch Bindestriche getrennt.</span><span class="sxs-lookup"><span data-stu-id="56e05-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="56e05-132">Verwenden Sie Verben, die den Zweck angeben, z.B. develop, buy, build, troubleshoot.</span><span class="sxs-lookup"><span data-stu-id="56e05-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="56e05-133">Auf „-ing“ endenden Worte dürfen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56e05-133">No -ing words.</span></span>
* <span data-ttu-id="56e05-134">Kurze Worte wie a, and, the, in, or usw. sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="56e05-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="56e05-135">Das Markdownformat und die Erweiterung „.md“ sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56e05-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="56e05-136">Verwenden Sie angemessene, kurze Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="56e05-136">Keep file names reasonably short.</span></span> <span data-ttu-id="56e05-137">Sie sind Teil der URL für Ihre Artikel.</span><span class="sxs-lookup"><span data-stu-id="56e05-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="56e05-138">Überschriften</span><span class="sxs-lookup"><span data-stu-id="56e05-138">Headings</span></span>

<span data-ttu-id="56e05-139">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="56e05-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="56e05-140">Schreiben Sie das erste Wort einer Überschrift immer groß.</span><span class="sxs-lookup"><span data-stu-id="56e05-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="56e05-141">Textformatierung</span><span class="sxs-lookup"><span data-stu-id="56e05-141">Text styling</span></span>

<span data-ttu-id="56e05-142">*Kursiv*</span><span class="sxs-lookup"><span data-stu-id="56e05-142">*Italics*</span></span>\
<span data-ttu-id="56e05-143">Für Dateien, Ordner, Pfade (für lange Elemente, die in Ihre eigene Zeile getrennt werden) und neue Begriffe</span><span class="sxs-lookup"><span data-stu-id="56e05-143">Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="56e05-144">**Fett**</span><span class="sxs-lookup"><span data-stu-id="56e05-144">**Bold**</span></span>\
<span data-ttu-id="56e05-145">Für Benutzeroberflächenelemente</span><span class="sxs-lookup"><span data-stu-id="56e05-145">Use for UI elements.</span></span>

`Code`\
<span data-ttu-id="56e05-146">Für Inlinecode, Schlüsselwörter der Sprache, NuGet-Paketnamen, Befehlszeilenbefehle, Datenbanktabellen- und Spaltennamen sowie URLs, die nicht klickbar sein sollen</span><span class="sxs-lookup"><span data-stu-id="56e05-146">Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="56e05-147">Links</span><span class="sxs-lookup"><span data-stu-id="56e05-147">Links</span></span>

<span data-ttu-id="56e05-148">Informationen zu Ankern, internen Links, Links zu anderen Dokumenten, Codeeinfügungen und externen Links finden Sie im allgemeinen Artikel zu [Links](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="56e05-148">See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="56e05-149">Das Team für die .NET-Dokumentation wendet folgende Konventionen an:</span><span class="sxs-lookup"><span data-stu-id="56e05-149">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="56e05-150">In den meisten Fällen werden relative Links verwendet. Von der Verwendung von `~/` wird in Links abgeraten, weil relative Links zur Quelle auf GitHub führen.</span><span class="sxs-lookup"><span data-stu-id="56e05-150">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="56e05-151">Allerdings wird das Zeichen `~/` für Links zu Dateien in abhängigen Repositorys verwendet, um den Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56e05-151">However, whenever we link to a file in a dependent repo, we use the `~/` character to provide the path.</span></span> <span data-ttu-id="56e05-152">Da die Dateien im abhängigen Repository sich auf GitHub an einem anderen Speicherort befinden, werden die Links mit relativen Links, unabhängig davon, wie sie geschrieben sind, nicht richtig aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="56e05-152">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="56e05-153">Die C#-Sprachspezifikation und die Visual Basic-Sprachspezifikation sind in den .NET-Dokumentationen enthalten, indem die Quelle der Sprach-Repositorys eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="56e05-153">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="56e05-154">Die Markdownquellen werden in den Repositorys [csharplang](https://github.com/dotnet/csharplang) und [vblang](https://github.com/dotnet/vblang) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="56e05-154">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="56e05-155">Links zu den Sprachspezifikationen müssen zu den Quellverzeichnissen zeigen, in denen diese Spezifikationen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="56e05-155">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="56e05-156">Für C# ist das Verzeichnis **~/_csharplang/spec**, und für Visual Basic ist das Verzeichnis **~/_vblang/spec**. Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="56e05-156">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="56e05-157">Links zu APIs</span><span class="sxs-lookup"><span data-stu-id="56e05-157">Links to APIs</span></span>

<span data-ttu-id="56e05-158">Das Buildsystem verfügt über einige Erweiterungen, mit denen Sie Links zu .NET-APIs erstellen können, ohne externe Links verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="56e05-158">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="56e05-159">Verwenden Sie eine der folgenden Syntaxvarianten:</span><span class="sxs-lookup"><span data-stu-id="56e05-159">You use one of the following syntax:</span></span>

1. <span data-ttu-id="56e05-160">Automatische Verknüpfung: `<xref:UID>` oder `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="56e05-160">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="56e05-161">Der `displayProperty`-Abfrageparameter erzeugt einen vollqualifizierten Linktext.</span><span class="sxs-lookup"><span data-stu-id="56e05-161">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="56e05-162">Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.</span><span class="sxs-lookup"><span data-stu-id="56e05-162">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="56e05-163">Markdownlink: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="56e05-163">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="56e05-164">Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="56e05-164">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="56e05-165">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="56e05-165">Examples:</span></span>

- <span data-ttu-id="56e05-166">`<xref:System.String>` wird als [Zeichenfolge](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="56e05-166">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="56e05-167">`<xref:System.String?displayProperty=nameWithType>` wird als [System.String](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="56e05-167">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="56e05-168">`[String class](xref:System.String)` wird als [Zeichenfolgenklasse](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="56e05-168">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="56e05-169">Weitere Informationen zur Verwendung dieser Notation finden Sie unter [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Verwenden des Querverweises).</span><span class="sxs-lookup"><span data-stu-id="56e05-169">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="56e05-170">Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert jeweils als `%60`, `%23` und `%2A` im HTML-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="56e05-170">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="56e05-171">Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56e05-171">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="56e05-172">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="56e05-172">Examples:</span></span>

- <span data-ttu-id="56e05-173">System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="56e05-173">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="56e05-174">System.Exception.\#ctor wird `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="56e05-174">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="56e05-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="56e05-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="56e05-176">Die UIDs von Typen, eine Liste von überladenen Membern oder einen bestimmten überladenen Member finden Sie über `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="56e05-176">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="56e05-177">Die Abfragezeichenfolge `?text=*\<type-member-name>*` gibt den Typ oder Member an, dessen UIDs Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="56e05-177">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="56e05-178">`https://xref.docs.microsoft.com/autocomplete?text=string.format` ruft beispielsweise die Überladungen [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) ab.</span><span class="sxs-lookup"><span data-stu-id="56e05-178">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="56e05-179">Das Tool sucht in der UID nach dem angegebenen Abfrageparameter `text`.</span><span class="sxs-lookup"><span data-stu-id="56e05-179">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="56e05-180">Zum Beispiel können Sie nach Membernamen (ToString), partiellen Membernamen (ToStri), Typen und Membernamen (Double.ToString) und mehr suchen.</span><span class="sxs-lookup"><span data-stu-id="56e05-180">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="56e05-181">Wenn Sie \* (oder `%2A`) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API.</span><span class="sxs-lookup"><span data-stu-id="56e05-181">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="56e05-182">Dies können Sie z. B. verwenden, wenn Sie eine Verknüpfung mit der Seite [List\<T>.BinarySearch-Methode](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) auf generische Weise als Alternative zu einer bestimmten Überladung wie [List\<T>.BinarySearch (T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="56e05-182">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="56e05-183">Sie können auch \* verwenden, um einen Link zu einer Memberseite zu erstellen, wenn der Member nicht überladen ist. Damit ersparen Sie sich das Einfügen der Parameterliste in die UID.</span><span class="sxs-lookup"><span data-stu-id="56e05-183">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="56e05-184">Sie müssen den vollqualifizierten Namen des Typs jedes Parameters der Methode einfügen, um einen Link zu einer spezifischen Methodenüberladung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56e05-184">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="56e05-185">Beispielsweise \<xref:System.DateTime.ToString>-Links an die parameterlose [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString)-Methode, während \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> mit der Methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="56e05-185">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="56e05-186">Verwenden Sie zum Verknüpfen eines generischen Typs (z. B. [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)) das Zeichen \` (`%60`) gefolgt von der Anzahl generischer Typparameter.</span><span class="sxs-lookup"><span data-stu-id="56e05-186">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="56e05-187">Zum Beispiel verknüpft `<xref:System.Nullable%601>` den Typ [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), und `<xref:System.Func%602>` verknüpft den Delegaten [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="56e05-187">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="56e05-188">Code</span><span class="sxs-lookup"><span data-stu-id="56e05-188">Code</span></span>

<span data-ttu-id="56e05-189">Die beste Methode zum Einfügen von Code besteht darin, Ausschnitte aus einem funktionstüchtigen Beispiel einzufügen.</span><span class="sxs-lookup"><span data-stu-id="56e05-189">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="56e05-190">Erstellen Sie Ihr Beispiel anhand der Anweisungen im Artikel [Contributing to .NET (Mitwirken an .NET)](dotnet-contribute.md#contribute-to-samples).</span><span class="sxs-lookup"><span data-stu-id="56e05-190">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contribute-to-samples) article.</span></span> <span data-ttu-id="56e05-191">Durch Einfügen von Ausschnitten aus vollständigen Programmen wird sichergestellt, dass der gesamte Code das CI-System (Continuous Integration) durchläuft.</span><span class="sxs-lookup"><span data-stu-id="56e05-191">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="56e05-192">Wenn Sie jedoch etwas veranschaulichen müssen, das zu Fehlern zur Kompilier- oder Laufzeit führt, können Sie Inlinecodeblöcke verwenden.</span><span class="sxs-lookup"><span data-stu-id="56e05-192">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

<span data-ttu-id="56e05-193">Informationen zur Markdownsyntax zum Anzeigen von Code in Dokumenten finden Sie unter [Gewusst wie: Einbinden von Code in Dokumenten](../code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="56e05-193">For information about the Markdown syntax for showing code in docs, see [How to include code in docs](../code-in-docs.md).</span></span>

## <a name="images"></a><span data-ttu-id="56e05-194">Bilder</span><span class="sxs-lookup"><span data-stu-id="56e05-194">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="56e05-195">Statisches Bild oder animiertes GIF</span><span class="sxs-lookup"><span data-stu-id="56e05-195">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="56e05-196">Verknüpftes Bild</span><span class="sxs-lookup"><span data-stu-id="56e05-196">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="56e05-197">Videos</span><span class="sxs-lookup"><span data-stu-id="56e05-197">Videos</span></span>

<span data-ttu-id="56e05-198">Derzeit können Sie mithilfe der folgenden Syntax sowohl Channel 9- als auch YouTube-Videos einbetten:</span><span class="sxs-lookup"><span data-stu-id="56e05-198">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="56e05-199">Channel 9</span><span class="sxs-lookup"><span data-stu-id="56e05-199">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="56e05-200">Wählen Sie die Registerkarte **Embed** (Einbetten) unter dem Video aus, und kopieren Sie die URL aus dem `<iframe>`-Element, um die richtige URL des Videos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="56e05-200">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="56e05-201">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="56e05-201">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="56e05-202">YouTube</span><span class="sxs-lookup"><span data-stu-id="56e05-202">YouTube</span></span>

<span data-ttu-id="56e05-203">Klicken Sie mit der rechten Maustaste auf das Video, und wählen Sie **Einbettungscode kopieren** aus `<iframe>`, um die richtige URL des Videos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="56e05-203">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="56e05-204">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="56e05-204">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="56e05-205">Erweiterungen für docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="56e05-205">docs.microsoft extensions</span></span>

<span data-ttu-id="56e05-206">Einige zusätzliche Erweiterungen für GitHub Flavored Markdown werden von docs.microsoft bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="56e05-206">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="56e05-207">Listen mit Häkchen</span><span class="sxs-lookup"><span data-stu-id="56e05-207">Checked lists</span></span>

<span data-ttu-id="56e05-208">Für Listen ist eine benutzerdefinierte Formatvorlage verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56e05-208">A custom style is available for lists.</span></span> <span data-ttu-id="56e05-209">Sie können Listen mit grünen Häkchen ausgeben.</span><span class="sxs-lookup"><span data-stu-id="56e05-209">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="56e05-210">Dies wird wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="56e05-210">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="56e05-211">Erstellen einer .NET Core-App</span><span class="sxs-lookup"><span data-stu-id="56e05-211">How to create a .NET Core app</span></span>
> * <span data-ttu-id="56e05-212">Hinzufügen eines Verweises zum Microsoft.XmlSerializer.Generator-Paket</span><span class="sxs-lookup"><span data-stu-id="56e05-212">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="56e05-213">Bearbeiten Ihrer MyApp.csproj-Datei zum Hinzufügen von Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="56e05-213">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="56e05-214">Hinzufügen von „XmlSerializer“ und einer Klasse</span><span class="sxs-lookup"><span data-stu-id="56e05-214">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="56e05-215">Erstellen und Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="56e05-215">How to build and run the application</span></span>

<span data-ttu-id="56e05-216">Ein Beispiel der Liste mit Häkchen finden Sie in dieser [.NET Core-Dokumentation](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="56e05-216">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="56e05-217">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="56e05-217">Buttons</span></span>

<span data-ttu-id="56e05-218">Schaltflächenlinks:</span><span class="sxs-lookup"><span data-stu-id="56e05-218">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="56e05-219">Dies wird wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="56e05-219">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="56e05-220">Schaltflächenlinks</span><span class="sxs-lookup"><span data-stu-id="56e05-220">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="56e05-221">Ein Beispiel solcher Schaltflächen finden Sie in dieser [Visual Studio-Dokumentation](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="56e05-221">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="56e05-222">Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="56e05-222">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="56e05-223">Ein Beispiel für exemplarische Vorgehensweisen finden Sie in diesem [C#-Leitfaden](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="56e05-223">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
