---
title: Markdownreferenz für docs.microsoft.com
description: Lernen Sie die in der Microsoft-Dokumentation-Plattform verwendeten Markdownfeatures und -syntax kennen.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592562"
---
# <a name="markdown-reference"></a><span data-ttu-id="eca1c-103">Markdownreferenz</span><span class="sxs-lookup"><span data-stu-id="eca1c-103">Markdown Reference</span></span>

<span data-ttu-id="eca1c-104">Markdown ist eine schlanke Markupsprache mit Nur-Text-Formatierungssyntax.</span><span class="sxs-lookup"><span data-stu-id="eca1c-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="eca1c-105">Die Dokumentationsplattform unterstützt den CommonMark-Standard für Markdown sowie einige Markdownerweiterungen, die umfangreicheren Inhalt auf docs.microsoft.com bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="eca1c-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="eca1c-106">In diesem Artikel werden die wichtigsten Konzepte bezüglich Markdown für doc.microsoft.com in alphabetischer Reihenfolge erläutert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="eca1c-107">Sie können Markdown in einem beliebigen Text-Editor schreiben.</span><span class="sxs-lookup"><span data-stu-id="eca1c-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="eca1c-108">Wenn Sie einen Editor verwenden möchten, der das Einfügen von Markdownstandardsyntax und von benutzerdefinierten Dokumentationserweiterungen unterstützt, wird [VS Code](https://code.visualstudio.com/) mit installiertem [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) empfohlen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="eca1c-109">Microsoft-Dokumentation nutzt die Markdown-Engine von Markdig.</span><span class="sxs-lookup"><span data-stu-id="eca1c-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="eca1c-110">Unter [https://babelmark.github.io/](https://babelmark.github.io/) können Sie das Rendern von Markdown in Markdig und mit anderen Engines testen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="eca1c-111">Warnungen (Hinweis, Tipp, Wichtig, Achtung, Warnung)</span><span class="sxs-lookup"><span data-stu-id="eca1c-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="eca1c-112">Damit wird eine Markdownerweiterungen für Microsoft-Dokumentation angewiesen, Blockzitate zu erzeugen, die auf docs.microsoft.com mit anderen Hintergrundfarben und Symbolen gerendert werden, die den Inhalt hervorheben.</span><span class="sxs-lookup"><span data-stu-id="eca1c-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="eca1c-113">Die folgenden Warnungstypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eca1c-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="eca1c-114">Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="eca1c-114">These alerts look like this on docs.microsoft.com:</span></span>

![Hier wird dargestellt, wie Warnungen im vorherigen Beispiel auf der veröffentlichten Dokumentationsseite mit unterschiedlichen Symbolen und Farben aussieht.](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="eca1c-116">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="eca1c-116">Code snippets</span></span>

<span data-ttu-id="eca1c-117">Sie können Codeausschnitte in Ihre Markdowndatei einbetten:</span><span class="sxs-lookup"><span data-stu-id="eca1c-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="eca1c-118">Überschriften</span><span class="sxs-lookup"><span data-stu-id="eca1c-118">Headings</span></span>

<span data-ttu-id="eca1c-119">Microsoft-Dokumentation unterstützt sechs Markdownüberschriftenebenen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="eca1c-120">Zwischen dem letzten `#` und dem Überschriftentext muss ein Leerzeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="eca1c-121">Jede Markdowndatei darf lediglich eine H1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="eca1c-122">Die H1 muss nach dem YML-Metadatenblock der erste Inhalt in der Datei sein.</span><span class="sxs-lookup"><span data-stu-id="eca1c-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="eca1c-123">H2s werden automatisch rechts in einem Navigationsmenü der veröffentlichten Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eca1c-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="eca1c-124">Dies gilt nicht für Überschriften auf niedrigeren Ebenen. Verwenden Sie H2s an sinnvollen Stellen, damit Leser gut durch Ihre Artikel navigieren können.</span><span class="sxs-lookup"><span data-stu-id="eca1c-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="eca1c-125">HTML-Überschriften, wie z.B. `<h1>`, werden nicht empfohlen und führen in einigen Fällen zu Buildwarnungen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-125">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="eca1c-126">Über [Lesezeichenlinks](#bookmark-links) können Sie Links zu einzelnen Überschriften einer Datei einfügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="eca1c-127">HTML</span><span class="sxs-lookup"><span data-stu-id="eca1c-127">HTML</span></span>

<span data-ttu-id="eca1c-128">Markdown unterstützt zwar Inline-HTML, aber HTML wird für die Veröffentlichung auf Microsoft-Dokumentation nicht empfohlen. HTML führt zu Buildfehlern oder -warnungen (einige Werte sind davon ausgenommen).</span><span class="sxs-lookup"><span data-stu-id="eca1c-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="eca1c-129">Bilder</span><span class="sxs-lookup"><span data-stu-id="eca1c-129">Images</span></span>

<span data-ttu-id="eca1c-130">Verwenden Sie zum Einbetten eines Bilds die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="eca1c-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="eca1c-131">`alt text` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild.</span><span class="sxs-lookup"><span data-stu-id="eca1c-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="eca1c-132">Für visuell eingeschränkte Menschen ist Alternativtext erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca1c-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="eca1c-133">Dieser Text ist zudem nützlich bei einem Seitenladefehler, durch den ein Bild nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="eca1c-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="eca1c-134">Bilder sollten in einem `/media`-Ordner in Ihrem Docset gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="eca1c-135">Die folgenden Dateitypen werden standardmäßig für Bilder unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eca1c-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="eca1c-136">.jpg</span><span class="sxs-lookup"><span data-stu-id="eca1c-136">.jpg</span></span>
- <span data-ttu-id="eca1c-137">.png</span><span class="sxs-lookup"><span data-stu-id="eca1c-137">.png</span></span>

<span data-ttu-id="eca1c-138">Andere Bildtypen werden unterstützt, wenn Sie diese als Ressourcen zur „docfx.json“-Datei</span><span class="sxs-lookup"><span data-stu-id="eca1c-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="eca1c-139">für Ihr Docset hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="eca1c-140">Links</span><span class="sxs-lookup"><span data-stu-id="eca1c-140">Links</span></span>

<span data-ttu-id="eca1c-141">In den meisten Fällen verwendet Microsoft-Dokumentation Standardmarkdownlinks zu anderen Dateien und Seiten.</span><span class="sxs-lookup"><span data-stu-id="eca1c-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="eca1c-142">Die Linktypen werden weiter unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="eca1c-143">Mit dem Docs Authoring Pack für VS Code können Sie relative Links und Lesezeichenlinks problemlos einfügen, ohne sich um den Pfad Gedanken machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca1c-144">Beziehen Sie in die Links zu Microsoft-Seiten keine Gebietsschemacodes ein (z.B. „de-de“).</span><span class="sxs-lookup"><span data-stu-id="eca1c-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="eca1c-145">Hartcodierte Gebietsschemacodes verhindern, dass lokalisierter Inhalt gerendert wird. So wird die Benutzung für Leser in anderen Gebietsschemas erschwert und führt zu hohen Lokalisierungskosten.</span><span class="sxs-lookup"><span data-stu-id="eca1c-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="eca1c-146">Wenn Sie eine URL aus dem Browser kopieren, wird der Gebietsschemacode standardmäßig mit kopiert. Deshalb müssen Sie diesen manuell löschen, wenn Sie einen Link erstellen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="eca1c-147">Verwenden Sie z.B. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eca1c-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="eca1c-148">Und nicht:</span><span class="sxs-lookup"><span data-stu-id="eca1c-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="eca1c-149">Relative Links im gleichen Docset</span><span class="sxs-lookup"><span data-stu-id="eca1c-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="eca1c-150">Ein relativer Pfad ist ein Pfad zu einer Zieldatei, der in einem relativen Verhältnis zur aktuellen Datei steht.</span><span class="sxs-lookup"><span data-stu-id="eca1c-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="eca1c-151">Auf Microsoft-Dokumentation können Sie einen relativen Pfad verwenden, um einen Link zu einer anderen Datei im gleichen Docset einzufügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="eca1c-152">Die Syntax für einen relativen Pfad sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="eca1c-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="eca1c-153">`../` gibt eine höhere Ebene in der Hierarchie an.</span><span class="sxs-lookup"><span data-stu-id="eca1c-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="eca1c-154">Der relative Pfad wird während des Builds aufgelöst. Auch die Erweiterung „.md“ wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="eca1c-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="eca1c-155">Sie können „../“ verwenden, um einen Link zu einer Datei im übergeordneten Ordner zu erstellen. Diese Datei muss sich allerdings im gleichen Docset befinden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="eca1c-156">Sie können „../“ nicht zum Erstellen eines Links zu einer Datei in einem anderen Docset verwenden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="eca1c-157">Microsoft-Dokumentation unterstützt zudem eine Sonderform von relativen Pfaden, die mit „~“ beginnt (z.B. ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="eca1c-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="eca1c-158">Diese Syntax gibt eine Datei an, die abhängig vom Stammordner eines Docsets ist.</span><span class="sxs-lookup"><span data-stu-id="eca1c-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="eca1c-159">Diese Art von Pfad wird ebenfalls während des Erstellungsvorgangs überprüft und aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="eca1c-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca1c-160">Beziehen Sie die Erweiterung mit in den relativen Pfad ein.</span><span class="sxs-lookup"><span data-stu-id="eca1c-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="eca1c-161">Der Build prüft das Vorhandensein der Zieldatei dieses relativen Pfads.</span><span class="sxs-lookup"><span data-stu-id="eca1c-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="eca1c-162">Wenn der relative Pfad keine Erweiterung enthält, ist es wahrscheinlich, dass der Build einen fehlerhaften Link meldet.</span><span class="sxs-lookup"><span data-stu-id="eca1c-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="eca1c-163">Verwenden Sie z.B. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eca1c-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="eca1c-164">Und nicht:</span><span class="sxs-lookup"><span data-stu-id="eca1c-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="eca1c-165">Links relativ zur Website zu anderen Dateien auf Microsoft-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="eca1c-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="eca1c-166">Beziehen Sie nicht die Erweiterung (.md) ein.</span><span class="sxs-lookup"><span data-stu-id="eca1c-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="eca1c-167">Dadurch wird ein Link zur Linux-Übersichtsdatei außerhalb des Docsets mit Azure-Artikeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="eca1c-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="eca1c-168">Links zu externen Websites</span><span class="sxs-lookup"><span data-stu-id="eca1c-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="eca1c-169">Ein URL-basierter Link zu einer anderen Webseite (muss „https://“ enthalten).</span><span class="sxs-lookup"><span data-stu-id="eca1c-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="eca1c-170">Lesezeichenlinks</span><span class="sxs-lookup"><span data-stu-id="eca1c-170">Bookmark links</span></span>

<span data-ttu-id="eca1c-171">Lesezeichenlink zu Überschriften in einer anderen Datei im gleichen Repository.</span><span class="sxs-lookup"><span data-stu-id="eca1c-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="eca1c-172">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eca1c-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="eca1c-173">Lesezeichenlink zu einer Überschrift in der aktuellen Datei:</span><span class="sxs-lookup"><span data-stu-id="eca1c-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="eca1c-174">Verwenden Sie ein Rautenzeichen (`#`) gefolgt von der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="eca1c-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="eca1c-175">So ändern Sie den Text der Überschrift in Linktext:</span><span class="sxs-lookup"><span data-stu-id="eca1c-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="eca1c-176">Verwenden Sie nur Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="eca1c-176">Use all lowercase characters</span></span>
- <span data-ttu-id="eca1c-177">Entfernen Sie alle Satzzeichen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-177">Remove punctuation</span></span>
- <span data-ttu-id="eca1c-178">Ersetzen Sie Leerzeichen durch Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="eca1c-178">Replace spaces with dashes</span></span>

<span data-ttu-id="eca1c-179">Wenn die Überschrift beispielsweise „2.2 Security concerns“ lautet, entspricht der Linktext des Lesezeichens „#22-security-concerns“.</span><span class="sxs-lookup"><span data-stu-id="eca1c-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="eca1c-180">Explizite Ankerlinks</span><span class="sxs-lookup"><span data-stu-id="eca1c-180">Explicit anchor links</span></span>

<span data-ttu-id="eca1c-181">Explizite Ankerlinks mit dem HTML-Tag `<a>` **sind nicht erforderlich und werden nicht empfohlen** (Ausnahmen: im Hub und auf der Landing Page).</span><span class="sxs-lookup"><span data-stu-id="eca1c-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="eca1c-182">Verwenden Sie Lesezeichenlinks wie oben beschrieben in allgemeinen Markdowndateien.</span><span class="sxs-lookup"><span data-stu-id="eca1c-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="eca1c-183">Verwenden Sie für den Hub und die Landing Page Anker. Orientieren Sie sich dafür an folgendem Format:</span><span class="sxs-lookup"><span data-stu-id="eca1c-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="eca1c-184">`## <a id="AnchorText"> </a>Header text` oder `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="eca1c-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="eca1c-185">Verwenden Sie die folgende Syntax, um Links zu expliziten Ankern herzustellen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="eca1c-186">Xref-Links</span><span class="sxs-lookup"><span data-stu-id="eca1c-186">XREF (cross reference) links</span></span>

<span data-ttu-id="eca1c-187">Verwenden Sie Xref-Links mit einer eindeutigen ID (UID), um automatisch generierte Links zu API-Referenzen im aktuellen Docset oder in anderen Docsets hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="eca1c-188">Fügen Sie die Konfiguration `xrefService` in der Datei `docfx.json` hinzu, um auf API-Referenzseiten in anderen Docsets zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="eca1c-189">Die UID entspricht dem vollqualifizierten Klassen- und Membernamen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="eca1c-190">Wenn Sie ein Sternchen (\*) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API.</span><span class="sxs-lookup"><span data-stu-id="eca1c-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="eca1c-191">Verwenden Sie z.B. `List<T>.BinarySearch*`, um einen Link zur Seite der BinarySearch-Methode statt einen Link zu einer bestimmten Überladung wie `List<T>.BinarySearch(T, IComparer<T>)` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="eca1c-192">Sie können eine der folgenden Syntaxvarianten auswählen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="eca1c-193">Automatischer Link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="eca1c-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="eca1c-194">Der optionale Abfrageparameter `displayProperty` erzeugt einen vollqualifizierten Linktext.</span><span class="sxs-lookup"><span data-stu-id="eca1c-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="eca1c-195">Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.</span><span class="sxs-lookup"><span data-stu-id="eca1c-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="eca1c-196">Markdownlink: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="eca1c-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="eca1c-197">Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="eca1c-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="eca1c-198">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="eca1c-198">Examples:</span></span>

- <span data-ttu-id="eca1c-199">`<xref:System.String>` wird als „String“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="eca1c-200">`<xref:System.String?displayProperty=nameWithType>` wird als „System.String“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="eca1c-201">`[String class](xref:System.String)` wird als „String class“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="eca1c-202">Im Moment gibt es keine einfache Möglichkeit, die UIDs zu suchen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="eca1c-203">Die beste Möglichkeit, die UID für eine API zu suchen, ist die Anzeige der Quelle für die API-Seite, zu der Sie eine Verknüpfung herstellen möchten, und den Wert „ms.assetid“ zu suchen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="eca1c-204">Einzelne Überladungswerte werden in der Quelle nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eca1c-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="eca1c-205">Wir erarbeiten ein besseres System für die Zukunft.</span><span class="sxs-lookup"><span data-stu-id="eca1c-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="eca1c-206">Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert als `%60`, `%23` und `%2A` im HTML-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="eca1c-207">Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca1c-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="eca1c-208">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="eca1c-208">Examples:</span></span>

- <span data-ttu-id="eca1c-209">System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="eca1c-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="eca1c-210">System.Exception.\#ctor wird `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="eca1c-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="eca1c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="eca1c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="eca1c-212">Listen (Nummeriert, Aufzählungszeichen, Checkliste)</span><span class="sxs-lookup"><span data-stu-id="eca1c-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="eca1c-213">Nummerierte Liste</span><span class="sxs-lookup"><span data-stu-id="eca1c-213">Numbered list</span></span>

<span data-ttu-id="eca1c-214">Für eine nummerierte Liste können Sie für alle Punkte Einsen verwenden. Diese werden bei der Veröffentlichung als aufsteigende Zahlenfolge gerendert.</span><span class="sxs-lookup"><span data-stu-id="eca1c-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="eca1c-215">Für eine bessere Lesbarkeit der Quelle können Sie Ihre Listen inkrementieren.</span><span class="sxs-lookup"><span data-stu-id="eca1c-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="eca1c-216">Verwenden Sie keine Buchstaben für Listen, auch nicht für geschachtelte Listen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="eca1c-217">Diese werden nicht fehlerfrei gerendert, wenn sie auf der Seite von Microsoft-Dokumentation veröffentlicht werden. Geschachtelte nummerierte Listen werden mit Kleinbuchstaben gerendert, wenn sie veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="eca1c-218">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eca1c-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="eca1c-219">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-219">This renders as follows:</span></span>

1. <span data-ttu-id="eca1c-220">This is</span><span class="sxs-lookup"><span data-stu-id="eca1c-220">This is</span></span>
1. <span data-ttu-id="eca1c-221">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="eca1c-221">a parent numbered list</span></span>
   1. <span data-ttu-id="eca1c-222">and this is</span><span class="sxs-lookup"><span data-stu-id="eca1c-222">and this is</span></span>
   1. <span data-ttu-id="eca1c-223">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="eca1c-223">a nested numbered list</span></span>
1. <span data-ttu-id="eca1c-224">(fin)</span><span class="sxs-lookup"><span data-stu-id="eca1c-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="eca1c-225">Liste mit Aufzählungszeichen</span><span class="sxs-lookup"><span data-stu-id="eca1c-225">Bulleted list</span></span>

<span data-ttu-id="eca1c-226">Verwenden Sie für eine Liste mit Aufzählungszeichen `-` gefolgt von einem Leerzeichen am Anfang jeder Zeile:</span><span class="sxs-lookup"><span data-stu-id="eca1c-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="eca1c-227">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-227">This renders as follows:</span></span>

- <span data-ttu-id="eca1c-228">This is</span><span class="sxs-lookup"><span data-stu-id="eca1c-228">This is</span></span>
- <span data-ttu-id="eca1c-229">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="eca1c-229">a parent bulleted list</span></span>
  - <span data-ttu-id="eca1c-230">and this is</span><span class="sxs-lookup"><span data-stu-id="eca1c-230">and this is</span></span>
  - <span data-ttu-id="eca1c-231">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="eca1c-231">a nested bulleted list</span></span>
- <span data-ttu-id="eca1c-232">All done!</span><span class="sxs-lookup"><span data-stu-id="eca1c-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="eca1c-233">Checkliste</span><span class="sxs-lookup"><span data-stu-id="eca1c-233">Checklist</span></span>

<span data-ttu-id="eca1c-234">Checklisten können (nur) auf docs.microsoft.com mit einer benutzerdefinierten Markdownerweiterung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="eca1c-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="eca1c-235">Dieses Beispiel wird auf docs.microsoft.com folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="eca1c-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="eca1c-236">List item 1</span></span>
> * <span data-ttu-id="eca1c-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="eca1c-237">List item 2</span></span>
> * <span data-ttu-id="eca1c-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="eca1c-238">List item 3</span></span>

<span data-ttu-id="eca1c-239">Verwenden Sie Checklisten am Anfang oder Ende eines Artikels, um zusammenzufassen, was der Leser lernen wird bzw. gelernt hat.</span><span class="sxs-lookup"><span data-stu-id="eca1c-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="eca1c-240">Fügen Sie keine sinnlosen Checklisten in der Mitte des Artikels ein.</span><span class="sxs-lookup"><span data-stu-id="eca1c-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="eca1c-241">Aktion „Nächste Schritte“</span><span class="sxs-lookup"><span data-stu-id="eca1c-241">Next step action</span></span>

<span data-ttu-id="eca1c-242">Sie können eine benutzerdefinierte Erweiterung verwenden, um eine Schaltfläche für weitere Schritte hinzuzufügen (nur auf docs.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="eca1c-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="eca1c-243">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="eca1c-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="eca1c-244">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eca1c-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="eca1c-245">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="eca1c-246">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="eca1c-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="eca1c-247">Sie können für nächste Schritte jede unterstützte Linkart verwenden, auch einen Markdownlink zu einer anderen Webseite.</span><span class="sxs-lookup"><span data-stu-id="eca1c-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="eca1c-248">In den meisten Fällen ist der Link für die nächsten Schritte ein relativer Link zu einer anderen Datei im gleichen Docset.</span><span class="sxs-lookup"><span data-stu-id="eca1c-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="eca1c-249">Definition von Abschnitten</span><span class="sxs-lookup"><span data-stu-id="eca1c-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="eca1c-250">Gelegentlich müssen Sie Abschnitte definieren.</span><span class="sxs-lookup"><span data-stu-id="eca1c-250">You might need to define a section.</span></span> <span data-ttu-id="eca1c-251">Diese Syntax wird in den meisten Fällen für Codetabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="eca1c-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="eca1c-252">Sehen Sie sich folgendes Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="eca1c-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="eca1c-253">Dieser blockquote-Markdowntext wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="eca1c-254">Selektoren</span><span class="sxs-lookup"><span data-stu-id="eca1c-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="eca1c-255">Sie können einen Selektor verwenden, wenn Sie für denselben Artikel verschiedene Seiten verbinden möchten.</span><span class="sxs-lookup"><span data-stu-id="eca1c-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="eca1c-256">Dann können die Leser zwischen diesen Seiten wechseln.</span><span class="sxs-lookup"><span data-stu-id="eca1c-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="eca1c-257">Diese Erweiterung funktioniert in docs.microsoft.com und MSDN unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="eca1c-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="eca1c-258">Einfache Auswahl</span><span class="sxs-lookup"><span data-stu-id="eca1c-258">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="eca1c-259">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="eca1c-268">Mehrfachauswahl</span><span class="sxs-lookup"><span data-stu-id="eca1c-268">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="eca1c-269">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-269">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Plattform" title2="Back-End"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | JavaScript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | JavaScript)](how-to-write-workflows-major.md)

## <a name="tables"></a><span data-ttu-id="eca1c-282">Tables</span><span class="sxs-lookup"><span data-stu-id="eca1c-282">Tables</span></span>

<span data-ttu-id="eca1c-283">Die einfachste Möglichkeit zum Erstellen einer Tabelle in Markdown ist die Verwendung von senkrechten Strichen und Unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="eca1c-284">Fügen Sie unter der ersten Zeile Unterstriche ein, um eine Standardtabelle mit Kopfzeile zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="eca1c-285">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-285">This renders as follows:</span></span>

|<span data-ttu-id="eca1c-286">This is</span><span class="sxs-lookup"><span data-stu-id="eca1c-286">This is</span></span>   |<span data-ttu-id="eca1c-287">a simple</span><span class="sxs-lookup"><span data-stu-id="eca1c-287">a simple</span></span>   |<span data-ttu-id="eca1c-288">table header</span><span class="sxs-lookup"><span data-stu-id="eca1c-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="eca1c-289">table</span><span class="sxs-lookup"><span data-stu-id="eca1c-289">table</span></span>     |<span data-ttu-id="eca1c-290">data</span><span class="sxs-lookup"><span data-stu-id="eca1c-290">data</span></span>       |<span data-ttu-id="eca1c-291">here</span><span class="sxs-lookup"><span data-stu-id="eca1c-291">here</span></span>        |
|<span data-ttu-id="eca1c-292">it doesn't</span><span class="sxs-lookup"><span data-stu-id="eca1c-292">it doesn't</span></span>|<span data-ttu-id="eca1c-293">actually</span><span class="sxs-lookup"><span data-stu-id="eca1c-293">actually</span></span>   |<span data-ttu-id="eca1c-294">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="eca1c-294">have to line up nicely!</span></span>||

<span data-ttu-id="eca1c-295">Sie können eine Tabelle auch ohne Kopfzeile erstellen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-295">You can also create a table without a header.</span></span> <span data-ttu-id="eca1c-296">Mit folgendem Code können Sie z.B. eine Liste mit mehreren Spalten erstellen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="eca1c-297">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="eca1c-298">This</span><span class="sxs-lookup"><span data-stu-id="eca1c-298">This</span></span> | <span data-ttu-id="eca1c-299">table</span><span class="sxs-lookup"><span data-stu-id="eca1c-299">table</span></span> |
| <span data-ttu-id="eca1c-300">has no</span><span class="sxs-lookup"><span data-stu-id="eca1c-300">has no</span></span> | <span data-ttu-id="eca1c-301">header</span><span class="sxs-lookup"><span data-stu-id="eca1c-301">header</span></span> |

<span data-ttu-id="eca1c-302">Sie können die Spalten mithilfe von Doppelpunkten ausrichten:</span><span class="sxs-lookup"><span data-stu-id="eca1c-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="eca1c-303">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="eca1c-304">right aligned:</span><span class="sxs-lookup"><span data-stu-id="eca1c-304">right aligned:</span></span>|
|<span data-ttu-id="eca1c-305">:left aligned</span><span class="sxs-lookup"><span data-stu-id="eca1c-305">:left aligned</span></span>     |
|<span data-ttu-id="eca1c-306">:centered        :</span><span class="sxs-lookup"><span data-stu-id="eca1c-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="eca1c-307">Mit der Erweiterung „Docs Authoring Pack“ für VS Code können Sie einfache Tabellen unkompliziert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="eca1c-308">Sie können auch den [Tables Generator](http://www.tablesgenerator.com/markdown_tables) verwenden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="eca1c-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="eca1c-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca1c-310">Das funktioniert nur auf docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca1c-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="eca1c-311">Wenn Sie eine Tabelle in Markdown erstellen, kann diese in den rechten Navigationsbereich hineinreichen und damit nicht lesbar sein.</span><span class="sxs-lookup"><span data-stu-id="eca1c-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="eca1c-312">Dieses Problem lässt sich lösen, indem Sie bei der Dokumentausgabe zulassen, dass Tabellen bei Bedarf umbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="eca1c-313">Dafür müssen Sie die Tabelle nur mit der benutzerdefinierten Klasse `[!div class="mx-tdBreakAll"]` umschließen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="eca1c-314">Im Folgenden finden Sie ein Markdownbeispiel einer Tabelle mit drei Zeilen, die von einem `div`-Element mit dem Klassennamen `mx-tdBreakAll` umschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="eca1c-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="eca1c-315">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="eca1c-316">Name</span><span class="sxs-lookup"><span data-stu-id="eca1c-316">Name</span></span>|<span data-ttu-id="eca1c-317">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca1c-317">Syntax</span></span>|<span data-ttu-id="eca1c-318">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="eca1c-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="eca1c-319">Description</span><span class="sxs-lookup"><span data-stu-id="eca1c-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="eca1c-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="eca1c-320">Quiet</span></span>|<span data-ttu-id="eca1c-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="eca1c-321">/quiet</span></span>|<span data-ttu-id="eca1c-322">Yes</span><span class="sxs-lookup"><span data-stu-id="eca1c-322">Yes</span></span>|<span data-ttu-id="eca1c-323">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="eca1c-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="eca1c-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="eca1c-324">NoRestart</span></span>|<span data-ttu-id="eca1c-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="eca1c-325">/norestart</span></span>|<span data-ttu-id="eca1c-326">No</span><span class="sxs-lookup"><span data-stu-id="eca1c-326">No</span></span>|<span data-ttu-id="eca1c-327">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="eca1c-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="eca1c-328">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="eca1c-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="eca1c-329">Help</span><span class="sxs-lookup"><span data-stu-id="eca1c-329">Help</span></span>|<span data-ttu-id="eca1c-330">/help</span><span class="sxs-lookup"><span data-stu-id="eca1c-330">/help</span></span>|<span data-ttu-id="eca1c-331">No</span><span class="sxs-lookup"><span data-stu-id="eca1c-331">No</span></span>|<span data-ttu-id="eca1c-332">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="eca1c-332">Provides help and quick reference.</span></span> <span data-ttu-id="eca1c-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="eca1c-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="eca1c-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="eca1c-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca1c-335">Das funktioniert nur auf docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca1c-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="eca1c-336">Von Zeit zu Zeit enthält die zweite Spalte einer Tabelle sehr lange Wörter.</span><span class="sxs-lookup"><span data-stu-id="eca1c-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="eca1c-337">Um sicherzustellen, dass lange Wörter sinnvoll unterteilt werden, können Sie die Klasse `mx-tdCol2BreakAll` wie oben gezeigt mithilfe der `div`-Wrappersyntax anwenden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="eca1c-338">HTML-Tabellen</span><span class="sxs-lookup"><span data-stu-id="eca1c-338">HTML Tables</span></span>

<span data-ttu-id="eca1c-339">HTML-Tabellen werden für docs.microsoft.com nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="eca1c-340">Sie können in der Quelle nicht von Menschen gelesen werden, was jedoch ein wichtiges Merkmal von Markdown ist.</span><span class="sxs-lookup"><span data-stu-id="eca1c-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="eca1c-341">Videos</span><span class="sxs-lookup"><span data-stu-id="eca1c-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="eca1c-342">Einbetten von Videos in eine Markdownseite</span><span class="sxs-lookup"><span data-stu-id="eca1c-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="eca1c-343">Momentan unterstützt Microsoft-Dokumentation Videos, die auf einer der folgenden Plattformen veröffentlicht wurden:</span><span class="sxs-lookup"><span data-stu-id="eca1c-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="eca1c-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="eca1c-344">YouTube</span></span>
- <span data-ttu-id="eca1c-345">Channel 9</span><span class="sxs-lookup"><span data-stu-id="eca1c-345">Channel 9</span></span>
- <span data-ttu-id="eca1c-346">OnePlayer von Microsoft</span><span class="sxs-lookup"><span data-stu-id="eca1c-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="eca1c-347">Sie können mit der folgenden Syntax ein Video einbetten, das von Microsoft-Dokumentation gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="eca1c-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="eca1c-348">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eca1c-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="eca1c-349">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="eca1c-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="eca1c-350">Auf veröffentlichten Seiten wird er wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="eca1c-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="eca1c-351">Die URL für ein CH9-Video muss mit `https` beginnen und mit `/player` enden.</span><span class="sxs-lookup"><span data-stu-id="eca1c-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="eca1c-352">Andernfalls wird nicht nur das Video, sondern die gesamte Seite eingebettet.</span><span class="sxs-lookup"><span data-stu-id="eca1c-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="eca1c-353">Hochladen neuer Videos</span><span class="sxs-lookup"><span data-stu-id="eca1c-353">Uploading new videos</span></span>

<span data-ttu-id="eca1c-354">Es wird empfohlen, neue Videos folgendermaßen hochzuladen:</span><span class="sxs-lookup"><span data-stu-id="eca1c-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="eca1c-355">Treten Sie der Gruppe **docs_video_users** auf IDWEB bei.</span><span class="sxs-lookup"><span data-stu-id="eca1c-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="eca1c-356">Navigieren Sie zu https://aka.ms/VideoUploadRequest, und machen Sie Angaben zu Ihrem Video.</span><span class="sxs-lookup"><span data-stu-id="eca1c-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="eca1c-357">Sie müssen Folgendes angeben (diese Informationen werden später nicht öffentlich verfügbar sein):</span><span class="sxs-lookup"><span data-stu-id="eca1c-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="eca1c-358">Einen Videotitel.</span><span class="sxs-lookup"><span data-stu-id="eca1c-358">A title for your video.</span></span>
    1. <span data-ttu-id="eca1c-359">Eine Liste der Produkte/Dienste, mit denen Ihr Video in Zusammenhang steht.</span><span class="sxs-lookup"><span data-stu-id="eca1c-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="eca1c-360">Die Zielseite oder das Zieldocset (wenn Sie noch keine Seite haben), wo Ihr Video gehostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eca1c-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="eca1c-361">Einen Link zur MP4-Datei des Videos (wenn Sie nicht wissen, wo Sie die Datei speichern sollen, können Sie sie vorübergehend hier speichern: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="eca1c-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="eca1c-362">MP4-Dateien sollten mindestens eine Auflösung von 720p haben.</span><span class="sxs-lookup"><span data-stu-id="eca1c-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="eca1c-363">Eine Beschreibung des Videos.</span><span class="sxs-lookup"><span data-stu-id="eca1c-363">A description of the video.</span></span>
1. <span data-ttu-id="eca1c-364">Übermitteln (speichern) Sie die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="eca1c-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="eca1c-365">Das Video wird innerhalb von zwei Werktagen hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="eca1c-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="eca1c-366">Der Link, den Sie zur Einbettung benötigen, wird im Arbeitselement platziert. Dann wird das Arbeitselement *wieder Ihnen zugewiesen*.</span><span class="sxs-lookup"><span data-stu-id="eca1c-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="eca1c-367">Sie können das Arbeitselement schließen, sobald Sie den Link kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="eca1c-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="eca1c-368">Der Videolink kann dann mit der folgenden Syntax in Ihrem Beitrag eingefügt werden:</span><span class="sxs-lookup"><span data-stu-id="eca1c-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
