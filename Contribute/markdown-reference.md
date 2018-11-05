---
title: Markdownreferenz für OPS und docs.microsoft.com
description: Der OPS-Plattformleitfaden für die Erweiterungen für Markdown und DocFX Flavored Markdown (DFM).
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: e248eafb0247b200313ba198f2545eca947f5627
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805913"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="2c8b8-103">Markdownreferenz für OPS</span><span class="sxs-lookup"><span data-stu-id="2c8b8-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="2c8b8-104">Markdown ist eine schlanke Markupsprache mit Nur-Text-Formatierungssyntax.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="2c8b8-105">OPS unterstützt den CommonMark-Standard für Markdown sowie einige Markdownerweiterungen, die umfangreicheren Inhalt auf docs.microsoft.com bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-105">OPS supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="2c8b8-106">In diesem Artikel werden die wichtigsten Konzepte bezüglich Markdown in OPS für doc.microsoft.com in alphabetischer Reihenfolge erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="2c8b8-107">Sie können Markdown in einem beliebigen Text-Editor schreiben.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="2c8b8-108">Wenn Sie einen Editor verwenden möchten, der das Einfügen von Markdownstandardsyntax und von benutzerdefinierten OPS-Erweiterungen unterstützt, wird [VS Code](https://code.visualstudio.com/) mit installiertem [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="2c8b8-109">OPS wurde in Markdig für alle neuen Repositorys standardisiert. Ältere Repositorys werden zu Markdig migriert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="2c8b8-110">Unter [https://babelmark.github.io/](https://babelmark.github.io/) können Sie das Rendern von Markdown in Markdig und mit anderen Engines testen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="2c8b8-111">Warnungen (Hinweis, Tipp, Wichtig, Achtung, Warnung)</span><span class="sxs-lookup"><span data-stu-id="2c8b8-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="2c8b8-112">Damit werden OPS-spezifische Markdownerweiterungen angewiesen, Blockzitate zu erzeugen, die auf docs.microsoft.com mit anderen Hintergrundfarben und Symbolen gerendert werden, die den Inhalt hervorheben.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-112">Alerts an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="2c8b8-113">Die folgenden Warnungstypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-113">The following alert types are supported:</span></span>

```markdown
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

<span data-ttu-id="2c8b8-114">Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="2c8b8-115">Informationen, die der Benutzer lesen sollte, wenn er den Artikel überfliegt.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="2c8b8-116">Weiterführende Informationen, durch die der Benutzer erfolgreicher arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c8b8-117">Wichtige Informationen, die für die erfolgreiche Arbeit des Benutzers essentiell sind.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="2c8b8-118">Mögliche negative Auswirkungen einer Aktion.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="2c8b8-119">Gefährliche Folgen einer Aktion.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="2c8b8-120">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="2c8b8-120">Code snippets</span></span>

<span data-ttu-id="2c8b8-121">Sie können Codeausschnitte in Ihre Markdowndatei einbetten:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="2c8b8-122">Überschriften</span><span class="sxs-lookup"><span data-stu-id="2c8b8-122">Headings</span></span>

<span data-ttu-id="2c8b8-123">OPS unterstützt sechs Markdownüberschriftenebenen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="2c8b8-124">Zwischen dem letzten `#` und dem Überschriftentext muss ein Leerzeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="2c8b8-125">Jede Markdowndatei darf lediglich eine H1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="2c8b8-126">Die H1 muss nach dem YML-Metadatenblock der erste Inhalt in der Datei sein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="2c8b8-127">H2s werden automatisch rechts in einem Navigationsmenü der veröffentlichten Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="2c8b8-128">Dies gilt nicht für Überschriften auf niedrigeren Ebenen. Verwenden Sie H2s an sinnvollen Stellen, damit Leser gut durch Ihre Artikel navigieren können.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="2c8b8-129">HTML-Überschriften, wie z.B. `<h1>`, werden nicht empfohlen und führen in einigen Fällen zu Buildwarnungen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="2c8b8-130">Über [Lesezeichenlinks](#bookmark-links) können Sie Links zu einzelnen Überschriften einer Datei einfügen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="2c8b8-131">HTML</span><span class="sxs-lookup"><span data-stu-id="2c8b8-131">HTML</span></span>

<span data-ttu-id="2c8b8-132">Markdown unterstützt zwar Inline-HTML, aber HTML wird für die Veröffentlichung über OPS nicht empfohlen. HTML führt zu Buildfehlern oder -warnungen (einige wenige Werte sind davon ausgenommen).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="2c8b8-133">Bilder</span><span class="sxs-lookup"><span data-stu-id="2c8b8-133">Images</span></span>

<span data-ttu-id="2c8b8-134">Verwenden Sie zum Einbetten eines Bilds die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="2c8b8-135">`alt text` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="2c8b8-136">Für visuell eingeschränkte Menschen ist Alternativtext erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="2c8b8-137">Dieser Text ist zudem nützlich bei einem Seitenladefehler, durch den ein Bild nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="2c8b8-138">Bilder sollten in einem `/media`-Ordner in Ihrem Docset gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="2c8b8-139">Die folgenden Dateitypen werden standardmäßig für Bilder unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="2c8b8-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="2c8b8-140">.jpg</span></span>
- <span data-ttu-id="2c8b8-141">.png</span><span class="sxs-lookup"><span data-stu-id="2c8b8-141">.png</span></span>

<span data-ttu-id="2c8b8-142">Sie können die Unterstützung für andere Bildtypen hinzufügen, indem Sie sie als Ressourcen zur Datei „docfx.json“<!--add link to reference when available--> für Ihr Docset hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="2c8b8-143">Links</span><span class="sxs-lookup"><span data-stu-id="2c8b8-143">Links</span></span>

<span data-ttu-id="2c8b8-144">In den meisten Fällen verwendet OPS Standardmarkdownlinks zu anderen Dateien und Seiten.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="2c8b8-145">Die Linktypen werden weiter unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="2c8b8-146">Mit dem Docs Authoring Pack für VS Code können Sie relative Links und Lesezeichenlinks problemlos einfügen, ohne sich um den Pfad Gedanken machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c8b8-147">Beziehen Sie in die Links zu Microsoft-Seiten keine Gebietsschemacodes ein (z.B. „de-de“).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="2c8b8-148">Hartcodierte Gebietsschemacodes verhindern, dass lokalisierter Inhalt gerendert wird. So wird die Benutzung für Leser in anderen Gebietsschemas erschwert und führt zu hohen Lokalisierungskosten.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="2c8b8-149">Wenn Sie eine URL aus dem Browser kopieren, wird der Gebietsschemacode standardmäßig mit kopiert. Deshalb müssen Sie diesen manuell löschen, wenn Sie einen Link erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete in when you create your link.</span></span> <span data-ttu-id="2c8b8-150">Verwenden Sie z.B. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="2c8b8-151">Und nicht:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="2c8b8-152">Relative Links im gleichen Docset</span><span class="sxs-lookup"><span data-stu-id="2c8b8-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="2c8b8-153">Ein relativer Pfad ist ein Pfad zu einer Zieldatei, der in einem relativen Verhältnis zur aktuellen Datei steht.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="2c8b8-154">In OPS können Sie einen relativen Pfad verwenden, um einen Link zu einer anderen Datei im gleichen Docset einzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="2c8b8-155">Die Syntax für einen relativen Pfad sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="2c8b8-156">`../` gibt eine höhere Ebene in der Hierarchie an.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="2c8b8-157">Der relative Pfad wird während des Builds aufgelöst. Auch die Erweiterung „.md“ wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="2c8b8-158">Sie können „../“ verwenden, um einen Link zu einer Datei im übergeordneten Ordner zu erstellen. Diese Datei muss sich allerdings im gleichen Docset befinden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="2c8b8-159">Sie können „../“ nicht zum Erstellen eines Links zu einer Datei in einem anderen Docset verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="2c8b8-160">OPS unterstützt zudem eine Sonderform von relativen Pfaden, die mit „~“ beginnt (z.B. ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="2c8b8-161">Diese Syntax gibt eine Datei an, die abhängig vom Stammordner eines Docsets ist.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="2c8b8-162">Diese Art von Pfad wird ebenfalls während des Erstellungsvorgangs überprüft und aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c8b8-163">Beziehen Sie die Erweiterung mit in den relativen Pfad ein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="2c8b8-164">Der Build prüft das Vorhandensein der Zieldatei dieses relativen Pfads.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="2c8b8-165">Wenn der relative Pfad keine Erweiterung enthält, ist es wahrscheinlich, dass der Build einen fehlerhaften Link meldet.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="2c8b8-166">Verwenden Sie z.B. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="2c8b8-167">Und nicht:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="2c8b8-168">Absolute Links zu anderen Dateien in OPS</span><span class="sxs-lookup"><span data-stu-id="2c8b8-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="2c8b8-169">Beziehen Sie nicht die Erweiterung (.md) ein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="2c8b8-170">Dadurch wird ein Link zur Linux-Übersichtsdatei außerhalb des Docsets mit Azure-Artikeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="2c8b8-171">Links zu externen Websites</span><span class="sxs-lookup"><span data-stu-id="2c8b8-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="2c8b8-172">Ein URL-basierter Link zu einer anderen Webseite (muss „https://“ enthalten).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="2c8b8-173">Lesezeichenlinks</span><span class="sxs-lookup"><span data-stu-id="2c8b8-173">Bookmark links</span></span>

<span data-ttu-id="2c8b8-174">Lesezeichenlinks zu Überschriften in einer anderen Datei im gleichen Repository:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="2c8b8-175">Lesezeichenlink zu einer Überschrift in der aktuellen Datei:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="2c8b8-176">Verwenden Sie eine Raute, und geben Sie dann die Überschrift ohne Interpunktion und mit Bindestrichen statt Leerzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="2c8b8-177">Explizite Ankerlinks</span><span class="sxs-lookup"><span data-stu-id="2c8b8-177">Explicit anchor links</span></span>

<span data-ttu-id="2c8b8-178">Explizite Ankerlinks mit dem HTML-Tag `<a>` **sind nicht erforderlich und werden nicht empfohlen** (Ausnahmen: im Hub und auf der Landing Page).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="2c8b8-179">Verwenden Sie Lesezeichenlinks wie oben beschrieben in allgemeinen Markdowndateien.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="2c8b8-180">Verwenden Sie für den Hub und die Landing Page Anker. Orientieren Sie sich dafür an folgendem Format:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="2c8b8-181">`## <a id="AnchorText"> </a>Header text` oder `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="2c8b8-182">Verwenden Sie die folgende Syntax, um Links zu expliziten Ankern herzustellen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="2c8b8-183">Xref-Links</span><span class="sxs-lookup"><span data-stu-id="2c8b8-183">XREF (cross reference) links</span></span>

<span data-ttu-id="2c8b8-184">Verwenden Sie Xref-Links mit einer eindeutigen ID (UID), um automatisch generierte Links zu API-Referenzen im aktuellen Docset oder in anderen Docsets hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="2c8b8-185">Fügen Sie die Konfiguration `xrefService` in der Datei `docfx.json` hinzu, um auf API-Referenzseiten in anderen Docsets zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-185">To reference API reference pages in other docsets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="2c8b8-186">Die UID entspricht dem vollqualifizierten Klassen- und Membernamen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="2c8b8-187">Wenn Sie ein Sternchen (\*) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="2c8b8-188">Verwenden Sie z.B. `List<T>.BinarySearch*`, um einen Link zur Seite der BinarySearch-Methode statt einen Link zu einer bestimmten Überladung wie `List<T>.BinarySearch(T, IComparer<T>)` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="2c8b8-189">Sie können eine der folgenden Syntaxvarianten auswählen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="2c8b8-190">Automatischer Link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="2c8b8-191">Der optionale Abfrageparameter `displayProperty` erzeugt einen vollqualifizierten Linktext.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="2c8b8-192">Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="2c8b8-193">Markdownlink: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="2c8b8-194">Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="2c8b8-195">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-195">Examples:</span></span>

- <span data-ttu-id="2c8b8-196">`<xref:System.String>` wird als „String“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="2c8b8-197">`<xref:System.String?displayProperty=nameWithType>` wird als „System.String“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="2c8b8-198">`[String class](xref:System.String)` wird als „String class“ gerendert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="2c8b8-199">Im Moment gibt es keine einfache Möglichkeit, die UIDs zu suchen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="2c8b8-200"><!-- ? -->Sie können die UID am besten finden, indem Sie sich die Quelle der API-Seite ansehen, zu der Sie einen Link erstellen möchten, und dann den Wert „ms.assetid“ suchen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="2c8b8-201">Einzelne Überladungswerte werden in der Quelle nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="2c8b8-202">Wir erarbeiten ein besseres System für die Zukunft.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="2c8b8-203">Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert als `%60`, `%23` und `%2A` im HTML-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="2c8b8-204">Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="2c8b8-205">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-205">Examples:</span></span>

- <span data-ttu-id="2c8b8-206">System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="2c8b8-207">System.Exception.\#ctor wird `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="2c8b8-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="2c8b8-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="2c8b8-209">Listen (Nummeriert, Aufzählungszeichen, Checkliste)</span><span class="sxs-lookup"><span data-stu-id="2c8b8-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="2c8b8-210">Nummerierte Liste</span><span class="sxs-lookup"><span data-stu-id="2c8b8-210">Numbered list</span></span>

<span data-ttu-id="2c8b8-211">Für eine nummerierte Liste können Sie für alle Punkte Einsen verwenden. Diese werden bei der Veröffentlichung als aufsteigende Zahlenfolge gerendert.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="2c8b8-212">Für eine bessere Lesbarkeit der Quelle können Sie Ihre Listen inkrementieren.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="2c8b8-213">Verwenden Sie keine Buchstaben für Listen, auch nicht für geschachtelte Listen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="2c8b8-214">Diese werden nicht fehlerfrei gerendert, wenn sie über OPS veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="2c8b8-215">Geschachtelte nummerierte Listen werden mit Kleinbuchstaben gerendert, wenn sie veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="2c8b8-216">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="2c8b8-217">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-217">This renders as follows:</span></span>

1. <span data-ttu-id="2c8b8-218">This is</span><span class="sxs-lookup"><span data-stu-id="2c8b8-218">This is</span></span>
1. <span data-ttu-id="2c8b8-219">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="2c8b8-219">a parent numbered list</span></span>
   1. <span data-ttu-id="2c8b8-220">and this is</span><span class="sxs-lookup"><span data-stu-id="2c8b8-220">and this is</span></span>
   1. <span data-ttu-id="2c8b8-221">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="2c8b8-221">a nested numbered list</span></span>
1. <span data-ttu-id="2c8b8-222">(fin)</span><span class="sxs-lookup"><span data-stu-id="2c8b8-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="2c8b8-223">Liste mit Aufzählungszeichen</span><span class="sxs-lookup"><span data-stu-id="2c8b8-223">Bulleted list</span></span>

<span data-ttu-id="2c8b8-224">Verwenden Sie für eine Liste mit Aufzählungszeichen `-` gefolgt von einem Leerzeichen am Anfang jeder Zeile:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="2c8b8-225">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-225">This renders as follows:</span></span>

- <span data-ttu-id="2c8b8-226">This is</span><span class="sxs-lookup"><span data-stu-id="2c8b8-226">This is</span></span>
- <span data-ttu-id="2c8b8-227">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="2c8b8-227">a parent bulleted list</span></span>
  - <span data-ttu-id="2c8b8-228">and this is</span><span class="sxs-lookup"><span data-stu-id="2c8b8-228">and this is</span></span>
  - <span data-ttu-id="2c8b8-229">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="2c8b8-229">a nested bulleted list</span></span>
- <span data-ttu-id="2c8b8-230">All done!</span><span class="sxs-lookup"><span data-stu-id="2c8b8-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="2c8b8-231">Checkliste</span><span class="sxs-lookup"><span data-stu-id="2c8b8-231">Checklist</span></span>

<span data-ttu-id="2c8b8-232">Checklisten können (nur) auf docs.microsoft.com mit einer benutzerdefinierten Markdownerweiterung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="2c8b8-233">Dieses Beispiel wird auf docs.microsoft.com folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="2c8b8-234">List item 1</span><span class="sxs-lookup"><span data-stu-id="2c8b8-234">List item 1</span></span>
> * <span data-ttu-id="2c8b8-235">List item 2</span><span class="sxs-lookup"><span data-stu-id="2c8b8-235">List item 2</span></span>
> * <span data-ttu-id="2c8b8-236">List item 3</span><span class="sxs-lookup"><span data-stu-id="2c8b8-236">List item 3</span></span>

<span data-ttu-id="2c8b8-237">Verwenden Sie Checklisten am Anfang oder Ende eines Artikels, um zusammenzufassen, was der Leser lernen wird bzw. gelernt hat.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-237">Use checklits at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="2c8b8-238">Fügen Sie keine sinnlosen Checklisten in der Mitte des Artikels ein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="2c8b8-239">Aktion „Nächste Schritte“</span><span class="sxs-lookup"><span data-stu-id="2c8b8-239">Next step action</span></span>

<span data-ttu-id="2c8b8-240">Sie können eine benutzerdefinierte Erweiterung verwenden, um eine Schaltfläche für weitere Schritte hinzuzufügen (nur auf docs.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="2c8b8-241">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="2c8b8-242">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="2c8b8-243">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="2c8b8-244">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="2c8b8-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="2c8b8-245">Sie können für nächste Schritte jede unterstützte Linkart verwenden, auch einen Markdownlink zu einer anderen Webseite.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="2c8b8-246">In den meisten Fällen ist der Link für die nächsten Schritte ein relativer Link zu einer anderen Datei im gleichen Docset.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="2c8b8-247">Definition von Abschnitten</span><span class="sxs-lookup"><span data-stu-id="2c8b8-247">Section definition</span></span>

<span data-ttu-id="2c8b8-248"><!-- more info about this would be helpful! --> Es kann sein, dass Sie die Abschnitte festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="2c8b8-249">Diese Syntax wird in den meisten Fällen für Codetabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="2c8b8-250">Sehen Sie sich folgendes Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="2c8b8-251">Dieser blockquote-Markdowntext wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="2c8b8-252">Selektoren</span><span class="sxs-lookup"><span data-stu-id="2c8b8-252">Selectors</span></span>

<span data-ttu-id="2c8b8-253"><!-- could be more clear! --> Sie können einen Selektor verwenden, wenn Sie für denselben Artikel verschiedene Seiten verlinken möchten.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="2c8b8-254">Dann können die Leser zwischen diesen Seiten wechseln.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8b8-255">Diese Erweiterung funktioniert in docs.microsoft.com und MSDN unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="2c8b8-256">Einfache Auswahl</span><span class="sxs-lookup"><span data-stu-id="2c8b8-256">Single selector</span></span>

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

<span data-ttu-id="2c8b8-257">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="2c8b8-266">Mehrfachauswahl</span><span class="sxs-lookup"><span data-stu-id="2c8b8-266">Multi-selector</span></span>

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

<span data-ttu-id="2c8b8-267">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-267">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
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

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="2c8b8-278">Tables</span><span class="sxs-lookup"><span data-stu-id="2c8b8-278">Tables</span></span>

<span data-ttu-id="2c8b8-279">Die einfachste Möglichkeit zum Erstellen einer Tabelle in Markdown ist die Verwendung von senkrechten Strichen und Unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="2c8b8-280">Fügen Sie unter der ersten Zeile Unterstriche ein, um eine Standardtabelle mit Kopfzeile zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="2c8b8-281">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-281">This renders as follows:</span></span>

|<span data-ttu-id="2c8b8-282">This is</span><span class="sxs-lookup"><span data-stu-id="2c8b8-282">This is</span></span>   |<span data-ttu-id="2c8b8-283">a simple</span><span class="sxs-lookup"><span data-stu-id="2c8b8-283">a simple</span></span>   |<span data-ttu-id="2c8b8-284">table header</span><span class="sxs-lookup"><span data-stu-id="2c8b8-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="2c8b8-285">table</span><span class="sxs-lookup"><span data-stu-id="2c8b8-285">table</span></span>     |<span data-ttu-id="2c8b8-286">data</span><span class="sxs-lookup"><span data-stu-id="2c8b8-286">data</span></span>       |<span data-ttu-id="2c8b8-287">here</span><span class="sxs-lookup"><span data-stu-id="2c8b8-287">here</span></span>        |
|<span data-ttu-id="2c8b8-288">it doesn't</span><span class="sxs-lookup"><span data-stu-id="2c8b8-288">it doesn't</span></span>|<span data-ttu-id="2c8b8-289">actually</span><span class="sxs-lookup"><span data-stu-id="2c8b8-289">actually</span></span>   |<span data-ttu-id="2c8b8-290">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="2c8b8-290">have to line up nicely!</span></span>||

<span data-ttu-id="2c8b8-291">Sie können eine Tabelle auch ohne Kopfzeile erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-291">You can also create a table without a header.</span></span> <span data-ttu-id="2c8b8-292">Mit folgendem Code können Sie z.B. eine Liste mit mehreren Spalten erstellen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="2c8b8-293">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="2c8b8-294">This</span><span class="sxs-lookup"><span data-stu-id="2c8b8-294">This</span></span> | <span data-ttu-id="2c8b8-295">table</span><span class="sxs-lookup"><span data-stu-id="2c8b8-295">table</span></span> |
| <span data-ttu-id="2c8b8-296">has no</span><span class="sxs-lookup"><span data-stu-id="2c8b8-296">has no</span></span> | <span data-ttu-id="2c8b8-297">header</span><span class="sxs-lookup"><span data-stu-id="2c8b8-297">header</span></span> |

<span data-ttu-id="2c8b8-298">Sie können die Spalten mithilfe von Doppelpunkten ausrichten:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="2c8b8-299">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="2c8b8-300">right aligned:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-300">right aligned:</span></span>|
|<span data-ttu-id="2c8b8-301">:left aligned</span><span class="sxs-lookup"><span data-stu-id="2c8b8-301">:left aligned</span></span>     |
|<span data-ttu-id="2c8b8-302">:centered        :</span><span class="sxs-lookup"><span data-stu-id="2c8b8-302">:centered        :</span></span>|

> [!TIP]
> Mit der Erweiterung „Docs Authoring Pack“ für VS Code können Sie einfache Tabellen unkompliziert hinzufügen.
>
> Sie können auch den [Tables Generator](http://www.tablesgenerator.com/markdown_tables) verwenden.

### <a name="mx-tdbreakall"></a><span data-ttu-id="2c8b8-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="2c8b8-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Das funktioniert nur auf docs.microsoft.com.

<span data-ttu-id="2c8b8-307">Wenn Sie eine Tabelle in Markdown erstellen, kann diese in den rechten Navigationsbereich hineinreichen und damit nicht lesbar sein.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="2c8b8-308">Dieses Problem lässt sich lösen, indem Sie bei der Dokumentausgabe zulassen, dass Tabellen bei Bedarf umbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="2c8b8-309">Dafür müssen Sie die Tabelle nur mit der benutzerdefinierten Klasse `[!div class="mx-tdBreakAll"]` umschließen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="2c8b8-310">Im Folgenden finden Sie ein Markdownbeispiel einer Tabelle mit drei Zeilen, die von einem `div`-Element mit dem Klassennamen `mx-tdBreakAll` umschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="2c8b8-311">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="2c8b8-312">Name</span><span class="sxs-lookup"><span data-stu-id="2c8b8-312">Name</span></span>|<span data-ttu-id="2c8b8-313">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c8b8-313">Syntax</span></span>|<span data-ttu-id="2c8b8-314">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="2c8b8-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="2c8b8-315">Description</span><span class="sxs-lookup"><span data-stu-id="2c8b8-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="2c8b8-316">Quiet</span><span class="sxs-lookup"><span data-stu-id="2c8b8-316">Quiet</span></span>|<span data-ttu-id="2c8b8-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="2c8b8-317">/quiet</span></span>|<span data-ttu-id="2c8b8-318">Yes</span><span class="sxs-lookup"><span data-stu-id="2c8b8-318">Yes</span></span>|<span data-ttu-id="2c8b8-319">Führt das Installationsprogramm ohne Benutzeroberfläche und Eingabeaufforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="2c8b8-320">NoRestart</span><span class="sxs-lookup"><span data-stu-id="2c8b8-320">NoRestart</span></span>|<span data-ttu-id="2c8b8-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="2c8b8-321">/norestart</span></span>|<span data-ttu-id="2c8b8-322">No</span><span class="sxs-lookup"><span data-stu-id="2c8b8-322">No</span></span>|<span data-ttu-id="2c8b8-323">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="2c8b8-324">Standardmäßig lässt die Benutzeroberfläche einen Neustart bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="2c8b8-325">Help</span><span class="sxs-lookup"><span data-stu-id="2c8b8-325">Help</span></span>|<span data-ttu-id="2c8b8-326">/help</span><span class="sxs-lookup"><span data-stu-id="2c8b8-326">/help</span></span>|<span data-ttu-id="2c8b8-327">No</span><span class="sxs-lookup"><span data-stu-id="2c8b8-327">No</span></span>|<span data-ttu-id="2c8b8-328">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-328">Provides help and quick reference.</span></span> <span data-ttu-id="2c8b8-329">Zeigt die korrekte Verwendung des Setupbefehls einschließlich einer Liste aller Optionen und Verhalten an.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="2c8b8-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="2c8b8-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c8b8-331">Das funktioniert nur auf docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="2c8b8-332">Von Zeit zu Zeit enthält die zweite Spalte einer Tabelle sehr lange Wörter.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="2c8b8-333">Um sicherzustellen, dass lange Wörter sinnvoll unterteilt werden, können Sie die Klasse `mx-tdCol2BreakAll` wie oben gezeigt mithilfe der `div`-Wrappersyntax anwenden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="2c8b8-334">HTML-Tabellen</span><span class="sxs-lookup"><span data-stu-id="2c8b8-334">HTML Tables</span></span>

<span data-ttu-id="2c8b8-335">HTML-Tabellen werden für docs.microsoft.com nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="2c8b8-336">Sie können in der Quelle nicht von Menschen gelesen werden, was jedoch ein wichtiges Merkmal von Markdown ist.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="2c8b8-337">Videos</span><span class="sxs-lookup"><span data-stu-id="2c8b8-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="2c8b8-338">Einbetten von Videos in eine Markdownseite</span><span class="sxs-lookup"><span data-stu-id="2c8b8-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="2c8b8-339">Momentan unterstützt OPS Videos, die auf einer der folgenden Plattformen veröffentlicht wurden:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="2c8b8-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="2c8b8-340">YouTube</span></span>
- <span data-ttu-id="2c8b8-341">Channel 9</span><span class="sxs-lookup"><span data-stu-id="2c8b8-341">Channel 9</span></span>
- <span data-ttu-id="2c8b8-342">OnePlayer von Microsoft</span><span class="sxs-lookup"><span data-stu-id="2c8b8-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="2c8b8-343">Sie können mit der folgenden Syntax ein Video einbetten, das von OPS gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="2c8b8-344">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="2c8b8-345">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="2c8b8-346">Auf veröffentlichten Seiten wird er wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="2c8b8-347">Die URL für ein CH9-Video muss mit `https` beginnen und mit `/player` enden.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="2c8b8-348">Andernfalls wird nicht nur das Video, sondern die gesamte Seite eingebettet.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="2c8b8-349">Hochladen neuer Videos</span><span class="sxs-lookup"><span data-stu-id="2c8b8-349">Uploading new videos</span></span>

<span data-ttu-id="2c8b8-350">Es wird empfohlen, neue Videos folgendermaßen hochzuladen:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="2c8b8-351">Treten Sie der Gruppe **docs_video_users** auf IDWEB bei.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="2c8b8-352">Navigieren Sie zu https://aka.ms/VideoUploadRequest, und machen Sie Angaben zu Ihrem Video.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="2c8b8-353">Sie müssen Folgendes angeben (diese Informationen werden später nicht öffentlich verfügbar sein):</span><span class="sxs-lookup"><span data-stu-id="2c8b8-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="2c8b8-354">Einen Videotitel.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-354">A title for your video.</span></span>
    1. <span data-ttu-id="2c8b8-355">Eine Liste der Produkte/Dienste, mit denen Ihr Video in Zusammenhang steht.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="2c8b8-356">Die Zielseite oder das Zieldocset (wenn Sie noch keine Seite haben), wo Ihr Video gehostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="2c8b8-357">Einen Link zur MP4-Datei des Videos (wenn Sie nicht wissen, wo Sie die Datei speichern sollen, können Sie sie vorübergehend hier speichern: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="2c8b8-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="2c8b8-358">MP4-Dateien sollten mindestens eine Auflösung von 720p haben.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="2c8b8-359">Eine Beschreibung des Videos.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-359">A description of the video.</span></span>
1. <span data-ttu-id="2c8b8-360">Übermitteln (speichern) Sie die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="2c8b8-361">Das Video wird innerhalb von zwei Werktagen hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="2c8b8-362">Der Link, den Sie zur Einbettung benötigen, wird in der Arbeitsaufgabe platziert. Dann wird die Arbeitsaufgabe *wieder Ihnen zugewiesen*.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="2c8b8-363">Sie können die Arbeitsaufgabe schließen, sobald Sie den Link kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="2c8b8-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="2c8b8-364">Der Videolink kann dann mit der folgenden Syntax in Ihrem Beitrag eingefügt werden:</span><span class="sxs-lookup"><span data-stu-id="2c8b8-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
