---
title: Markdownreferenz für docs.microsoft.com
description: Lernen Sie die in der Microsoft-Dokumentation-Plattform verwendeten Markdownfeatures und -syntax kennen.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624730"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="394a3-103">Docs Markdown-Referenz</span><span class="sxs-lookup"><span data-stu-id="394a3-103">Docs Markdown reference</span></span>

<span data-ttu-id="394a3-104">In diesem Artikel werden die wichtigsten Konzepte zum Schreiben von Markdown für doc.microsoft.com (Docs) in alphabetischer Reihenfolge erläutert.</span><span class="sxs-lookup"><span data-stu-id="394a3-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="394a3-105">[Markdown](https://daringfireball.net/projects/markdown/) ist eine schlanke Markupsprache mit Nur-Text-Formatierungssyntax.</span><span class="sxs-lookup"><span data-stu-id="394a3-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="394a3-106">Docs unterstützt ein kompatibles [CommonMark](https://commonmark.org/)-Markdown, das von der [Markdig](https://github.com/lunet-io/markdig)-Analyse-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="394a3-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="394a3-107">Docs unterstützt auch benutzerdefinierte Markdownerweiterungen, die umfangreicheren Inhalt auf der Docs-Website bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="394a3-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="394a3-108">Sie können Markdown in einem beliebigen Text-Editor schreiben, es wird jedoch empfohlen, [Visual Studio Code](https://code.visualstudio.com/) mit dem [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="394a3-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="394a3-109">Das Docs Authoring Pack bietet Bearbeitungstools und Vorschaufunktionen, mit denen Sie sehen können, wie Ihre Artikel beim Rendern auf Docs aussehen werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="394a3-110">Warnungen (Hinweis, Tipp, Wichtig, Achtung, Warnung)</span><span class="sxs-lookup"><span data-stu-id="394a3-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="394a3-111">Warnungen sind eine Markdownerweiterung zum Erstellen von Blockzitaten, die auf docs.microsoft.com mit Farben und Symbolen gerendert werden, die die Bedeutung des Inhalts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="394a3-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="394a3-112">Die folgenden Warnungstypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="394a3-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="394a3-113">Diese Warnungen sehen auf docs.microsoft.com folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="394a3-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="394a3-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="394a3-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="394a3-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="394a3-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="394a3-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="394a3-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="394a3-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="394a3-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="394a3-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="394a3-119">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="394a3-119">Angle brackets</span></span>

<span data-ttu-id="394a3-120">Wenn Sie in Ihrer Datei spitze Klammern im Text verwenden, z. B. zur Bezeichnung eines Platzhalters, müssen Sie die spitzen Klammern manuell codieren.</span><span class="sxs-lookup"><span data-stu-id="394a3-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="394a3-121">Andernfalls interpretiert Markdown sie als HTML-Tag.</span><span class="sxs-lookup"><span data-stu-id="394a3-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="394a3-122">Codieren Sie `<script name>` z. B. als `&lt;script name&gt;` oder `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="394a3-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="394a3-123">Spitze Klammern müssen in Text, der als Inlinecode oder in Codeblöcken formatiert ist, nicht mit einem Escapezeichen versehen werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="394a3-124">Apostrophe und Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="394a3-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="394a3-125">Wenn Sie aus Word in einen Markdowneditor kopieren, könnte der Text typografische Apostrophe oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="394a3-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="394a3-126">Diese müssen codiert oder in einfache Apostrophe und Anführungszeichen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="394a3-127">Andernfalls wird beim Veröffentlichen der Datei möglicherweise Folgendes ausgegeben: Itâ&euro;&trade;s</span><span class="sxs-lookup"><span data-stu-id="394a3-127">Otherwise, you end up with things like this when the file is published: Itâ&euro;&trade;s</span></span>

<span data-ttu-id="394a3-128">Hier sind die Codierungen für die typografischen Versionen dieser Satzzeichen:</span><span class="sxs-lookup"><span data-stu-id="394a3-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="394a3-129">Linkes (öffnendes) Anführungszeichen: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="394a3-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="394a3-130">Rechtes (schließendes) Anführungszeichen: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="394a3-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="394a3-131">Rechtes (schließendes) einzelnes Anführungszeichen oder Apostroph: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="394a3-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="394a3-132">Linkes (öffnendes) einzelnes Anführungszeichen (selten verwendet): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="394a3-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="394a3-133">Blockzitate</span><span class="sxs-lookup"><span data-stu-id="394a3-133">Blockquotes</span></span>

<span data-ttu-id="394a3-134">Blockzitate werden mit dem `>`-Zeichen generiert:</span><span class="sxs-lookup"><span data-stu-id="394a3-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="394a3-135">Das vorherige Beispiel wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="394a3-136">Dies ist ein Blockzitat.</span><span class="sxs-lookup"><span data-stu-id="394a3-136">This is a blockquote.</span></span> <span data-ttu-id="394a3-137">Es wird normalerweise eingerückt und mit einer anderen Hintergrundfarbe gerendert.</span><span class="sxs-lookup"><span data-stu-id="394a3-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="394a3-138">Fetter und kursiver Text</span><span class="sxs-lookup"><span data-stu-id="394a3-138">Bold and italic text</span></span>

<span data-ttu-id="394a3-139">Um Text **fett** zu formatieren, schließen Sie ihn in vier Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="394a3-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="394a3-140">Um Text *kursiv* zu formatieren, schließen Sie ihn in zwei Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="394a3-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="394a3-141">Um Text ***fett und kursiv*** zu formatieren, schließen Sie ihn in sechs Sternchen ein:</span><span class="sxs-lookup"><span data-stu-id="394a3-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="394a3-142">Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="394a3-142">Code snippets</span></span>

<span data-ttu-id="394a3-143">Docs Markdown unterstützt die Platzierung von Codeausschnitten sowohl inline in einem Satz als auch als separater „umgrenzter“ Block zwischen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="394a3-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="394a3-144">Weitere Informationen finden Sie unter [Hinzufügen von Code zu Dokumenten](code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="394a3-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="394a3-145">Spalten</span><span class="sxs-lookup"><span data-stu-id="394a3-145">Columns</span></span>

<span data-ttu-id="394a3-146">Die Markdownerweiterung **columns** ermöglicht es Dokumentationsautoren, spaltenbasierte Inhaltslayouts hinzuzufügen, die flexibler und leistungsfähiger als einfache Markdowntabellen sind, die sich nur für echte Tabellendaten eignen.</span><span class="sxs-lookup"><span data-stu-id="394a3-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="394a3-147">Sie können bis zu vier Spalten hinzufügen und das optionale Attribut `span` verwenden, um zwei oder mehr Spalten zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="394a3-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="394a3-148">Die Syntax für Spalten sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="394a3-149">Spalten sollten nur einfaches Markdown, einschließlich Bildern, enthalten.</span><span class="sxs-lookup"><span data-stu-id="394a3-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="394a3-150">Überschriften, Tabellen, Registerkarten und andere komplexe Strukturen sollten nicht eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="394a3-151">Eine Zeile darf keinen Inhalt außerhalb der Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="394a3-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="394a3-152">Beispielsweise erstellt das folgende Markdown eine Spalte, die zwei Spaltenbreiten umfasst, sowie eine Standardspalte (ohne `span`):</span><span class="sxs-lookup"><span data-stu-id="394a3-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="394a3-153">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="394a3-154">**Spalte mit doppelter Spaltenbreite und viel Text**</span><span class="sxs-lookup"><span data-stu-id="394a3-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="394a3-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="394a3-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="394a3-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="394a3-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="394a3-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="394a3-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="394a3-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="394a3-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="394a3-159">**Spalte mit einfacher Spaltenbreite und einem Bild**</span><span class="sxs-lookup"><span data-stu-id="394a3-159">**This is a single-span column with an image in it.**</span></span>

      ![Dok.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="394a3-161">Überschriften</span><span class="sxs-lookup"><span data-stu-id="394a3-161">Headings</span></span>

<span data-ttu-id="394a3-162">Microsoft-Dokumentation unterstützt sechs Markdownüberschriftenebenen:</span><span class="sxs-lookup"><span data-stu-id="394a3-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="394a3-163">Zwischen dem letzten `#` und dem Überschriftentext muss ein Leerzeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="394a3-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="394a3-164">Jede Markdowndatei darf lediglich eine H1-Überschrift aufweisen.</span><span class="sxs-lookup"><span data-stu-id="394a3-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="394a3-165">Die H1-Überschrift muss nach dem YML-Metadatenblock der erste Inhalt in der Datei sein.</span><span class="sxs-lookup"><span data-stu-id="394a3-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="394a3-166">H2-Überschriften werden automatisch rechts in einem Navigationsmenü der veröffentlichten Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="394a3-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="394a3-167">Überschriften auf niedrigeren Ebenen werden nicht angezeigt. Verwenden Sie H2s an sinnvollen Stellen, damit Leser gut durch Ihre Artikel navigieren können.</span><span class="sxs-lookup"><span data-stu-id="394a3-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="394a3-168">HTML-Überschriften, wie z. B. `<h1>`, werden nicht empfohlen und führen in einigen Fällen zu Buildwarnungen.</span><span class="sxs-lookup"><span data-stu-id="394a3-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="394a3-169">Über [Lesezeichenlinks](how-to-write-links.md#explicit-anchor-links) können Sie Links zu einzelnen Überschriften einer Datei einfügen.</span><span class="sxs-lookup"><span data-stu-id="394a3-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#explicit-anchor-links).</span></span>

## <a name="html"></a><span data-ttu-id="394a3-170">HTML</span><span class="sxs-lookup"><span data-stu-id="394a3-170">HTML</span></span>

<span data-ttu-id="394a3-171">Markdown unterstützt zwar Inline-HTML, aber HTML wird für die Veröffentlichung auf Docs nicht empfohlen. HTML führt zu Buildfehlern oder -warnungen (einige Werte sind davon ausgenommen).</span><span class="sxs-lookup"><span data-stu-id="394a3-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="394a3-172">Bilder</span><span class="sxs-lookup"><span data-stu-id="394a3-172">Images</span></span>

<span data-ttu-id="394a3-173">Die folgenden Dateitypen werden standardmäßig für Bilder unterstützt:</span><span class="sxs-lookup"><span data-stu-id="394a3-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="394a3-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="394a3-174">.jpg</span></span>
- <span data-ttu-id="394a3-175">.png</span><span class="sxs-lookup"><span data-stu-id="394a3-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="394a3-176">Standarddarstellung von Bildern (standardmäßiges Markdown)</span><span class="sxs-lookup"><span data-stu-id="394a3-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="394a3-177">Die grundlegende Markdownsyntax zum Einbetten eines Bilds sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="394a3-178">`<alt text>` ist eine kurze Beschreibung des Bilds, und `<folder path>` ist ein relativer Pfad zum Bild.</span><span class="sxs-lookup"><span data-stu-id="394a3-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="394a3-179">Für visuell eingeschränkte Menschen ist Alternativtext erforderlich.</span><span class="sxs-lookup"><span data-stu-id="394a3-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="394a3-180">Dieser Text ist zudem nützlich bei einem Seitenladefehler, durch den ein Bild nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="394a3-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="394a3-181">Unterstriche in Alternativtext werden nicht korrekt gerendert, es sei denn, Sie stellen ihnen einen umgekehrten Schrägstrich (`\_`) als Escapezeichen voran.</span><span class="sxs-lookup"><span data-stu-id="394a3-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="394a3-182">Kopieren Sie jedoch keine Dateinamen zur Verwendung als Alternativtext.</span><span class="sxs-lookup"><span data-stu-id="394a3-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="394a3-183">Schreiben Sie beispielsweise nicht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="394a3-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="394a3-184">Schreiben Sie stattdessen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="394a3-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="394a3-185">Standarddarstellung von Bildern (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="394a3-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="394a3-186">Die benutzerdefinierte Docs-Erweiterung `:::image:::`unterstützt Standardbilder, komplexe Bilder und Symbole.</span><span class="sxs-lookup"><span data-stu-id="394a3-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="394a3-187">Bei Standardbildern funktioniert die ältere Markdownsyntax weiterhin, doch wird die neue Erweiterung empfohlen, da sie leistungsfähigere Funktionen unterstützt, wie z. B. das Angeben eines Lokalisierungsbereichs, der sich vom übergeordneten Thema unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="394a3-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="394a3-188">Weitere erweiterte Funktionen, z. B. das Auswählen aus der Shared Image Gallery statt Angabe eines lokalen Bilds, werden in Zukunft verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="394a3-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="394a3-189">Die neue Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="394a3-190">Wenn `type="content"` (Standard), sind sowohl `source` als auch `alt-text` erforderlich.</span><span class="sxs-lookup"><span data-stu-id="394a3-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="394a3-191">Komplexe Bilder mit langen Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="394a3-191">Complex images with long descriptions</span></span>

<span data-ttu-id="394a3-192">Sie können diese Erweiterung auch zum Hinzufügen eines Bilds mit einer langen Beschreibung verwenden, die von Sprachausgaben gelesen, aber nicht visuell auf der veröffentlichten Seite gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="394a3-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="394a3-193">Lange Beschreibungen sind eine Anforderung hinsichtlich der Barrierefreiheit bei komplexen Bildern, z. B. Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="394a3-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="394a3-194">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="394a3-195">Wenn `type="complex"`, sind `source`, `alt-text`, eine lange Beschreibung und das `:::image-end:::`-Tag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="394a3-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="394a3-196">Festlegen des Lokalisierungsbereichs</span><span class="sxs-lookup"><span data-stu-id="394a3-196">Specifying loc-scope</span></span>

<span data-ttu-id="394a3-197">Manchmal unterscheidet sich der Lokalisierungsbereich eines Bilds von dem des Artikels oder Moduls, in dem es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="394a3-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="394a3-198">Dies kann zu einer falschen globalen Darstellung führen, wenn z. B. der Screenshot eines Produkts versehentlich in eine Sprache lokalisiert wird, in der das Produkt nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="394a3-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="394a3-199">Um das zu verhindern, können Sie das optionale Attribut `loc-scope` in Bildern vom Typ `content` und `complex` angeben.</span><span class="sxs-lookup"><span data-stu-id="394a3-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="394a3-200">Symbole</span><span class="sxs-lookup"><span data-stu-id="394a3-200">Icons</span></span>

<span data-ttu-id="394a3-201">Die Bilderweiterung unterstützt Symbole, bei denen es sich um dekorative Bilder handelt und die keinen Alternativtext aufweisen sollten.</span><span class="sxs-lookup"><span data-stu-id="394a3-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="394a3-202">Die Syntax für Symbole sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="394a3-203">Wenn `type="icon"`, sollte nur `source` angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="394a3-204">Einbezogene Markdowndateien</span><span class="sxs-lookup"><span data-stu-id="394a3-204">Included Markdown files</span></span>

<span data-ttu-id="394a3-205">Wenn Markdowndateien in mehreren Artikeln wiederholt werden müssen, können Sie eine Includedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="394a3-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="394a3-206">Die Einbeziehungsfunktion weist Docs an, den Verweis zum Zeitpunkt der Erstellung durch den Inhalt der Includedatei zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="394a3-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="394a3-207">Sie können Einbeziehungen auf folgende Arten verwenden:</span><span class="sxs-lookup"><span data-stu-id="394a3-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="394a3-208">Inline: Verwenden Sie einen häufig verwendeten Textausschnitt inline innerhalb eines Satzes wieder.</span><span class="sxs-lookup"><span data-stu-id="394a3-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="394a3-209">Block: Verwenden Sie eine gesamte Markdowndatei als ein im Abschnitt eines Artikels geschachtelten Block wieder.</span><span class="sxs-lookup"><span data-stu-id="394a3-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="394a3-210">Inline- oder Blockincludedateien sind Markdowndateien (.md).</span><span class="sxs-lookup"><span data-stu-id="394a3-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="394a3-211">Sie können jeglichen gültigen Markdowncode enthalten.</span><span class="sxs-lookup"><span data-stu-id="394a3-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="394a3-212">Includedateien befinden sich normalerweise in einem allgemeinen Unterverzeichnis *includes* im Stammverzeichnis des Repositorys.</span><span class="sxs-lookup"><span data-stu-id="394a3-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="394a3-213">Bei Veröffentlichung des Artikels wird die einbezogene Datei nahtlos integriert.</span><span class="sxs-lookup"><span data-stu-id="394a3-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="394a3-214">Einbeziehungssyntax</span><span class="sxs-lookup"><span data-stu-id="394a3-214">Includes syntax</span></span>

<span data-ttu-id="394a3-215">Blockeinbeziehungen befinden sich in einer eigenen Zeile:</span><span class="sxs-lookup"><span data-stu-id="394a3-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="394a3-216">Inlineeinbeziehungen befinden sich innerhalb einer Zeile:</span><span class="sxs-lookup"><span data-stu-id="394a3-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="394a3-217">Dabei ist `<title>` der Name der Datei, und `<filepath>` ist der relative Pfad zur Datei.</span><span class="sxs-lookup"><span data-stu-id="394a3-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="394a3-218">`INCLUDE` muss groß geschrieben werden, und es muss ein Leerzeichen vor `<title>` vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="394a3-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="394a3-219">Die Anforderungen und Überlegungen zu Includedateien lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="394a3-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="394a3-220">Verwenden Sie Blockeinbeziehungen für umfangreiche Inhaltsmengen, d.h. ein oder zwei Absätze, ein gemeinsames Verfahren oder ein gemeinsamer Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="394a3-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="394a3-221">Verwenden Sie sie nicht für Inhalte, die kleiner sind als ein Satz.</span><span class="sxs-lookup"><span data-stu-id="394a3-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="394a3-222">Einbeziehungen werden in der GitHub-Ansicht Ihres Artikels nicht gerendert, da sie von Docs-Erweiterungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="394a3-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="394a3-223">Sie werden erst nach der Veröffentlichung gerendert.</span><span class="sxs-lookup"><span data-stu-id="394a3-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="394a3-224">Stellen Sie sicher, dass sämtlicher Text in einer Includedatei in vollständigen Sätzen oder Ausdrücken geschrieben ist, die nicht vom vorhergehenden oder nachfolgenden Text in dem Artikel, der auf die Includedatei verweist, abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="394a3-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="394a3-225">Wenn Sie diese Vorgabe ignorieren, wird eine unübersetzbare Zeichenfolge im Artikel erstellt.</span><span class="sxs-lookup"><span data-stu-id="394a3-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="394a3-226">Betten Sie keine Includedateien in andere Includedateien ein.</span><span class="sxs-lookup"><span data-stu-id="394a3-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="394a3-227">Platzieren Sie Mediendateien in einem Medienordner, der für das Includeunterverzeichnis bestimmt ist (z. B. der Ordner `<repo>` */includes/media*).</span><span class="sxs-lookup"><span data-stu-id="394a3-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="394a3-228">Der Stamm des *media*-Verzeichnisses darf keine Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="394a3-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="394a3-229">Wenn das Includeverzeichnis keine Bilder enthält, ist kein entsprechendes *media*-Verzeichnis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="394a3-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="394a3-230">Geben Sie Medien wie reguläre Artikel nicht zur gemeinsamen Nutzung durch Includedateien frei.</span><span class="sxs-lookup"><span data-stu-id="394a3-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="394a3-231">Verwenden Sie eine separate Datei mit einem eindeutigen Namen für jede Einbeziehung und jeden Artikel.</span><span class="sxs-lookup"><span data-stu-id="394a3-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="394a3-232">Speichern Sie die Mediendatei in dem Medienordner, der der Einbeziehung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="394a3-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="394a3-233">Verwenden Sie eine Einbeziehung nicht als ausschließlichen Inhalt eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="394a3-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="394a3-234">Einbeziehungen sind als Ergänzung des übrigen Artikelinhalts gedacht.</span><span class="sxs-lookup"><span data-stu-id="394a3-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="394a3-235">Links</span><span class="sxs-lookup"><span data-stu-id="394a3-235">Links</span></span>

<span data-ttu-id="394a3-236">Weitere Informationen zur Syntax von Links finden Sie unter [Verwenden von Links in der Dokumentation](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="394a3-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="394a3-237">Listen (Nummeriert, Aufzählungszeichen, Checkliste)</span><span class="sxs-lookup"><span data-stu-id="394a3-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="394a3-238">Nummerierte Liste</span><span class="sxs-lookup"><span data-stu-id="394a3-238">Numbered list</span></span>

<span data-ttu-id="394a3-239">Zum Erstellen einer nummerierten Liste können Sie für alle Punkte Einsen verwenden.</span><span class="sxs-lookup"><span data-stu-id="394a3-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="394a3-240">Die Zahlen werden bei der Veröffentlichung in aufsteigender Reihenfolge als sequenzielle Liste gerendert.</span><span class="sxs-lookup"><span data-stu-id="394a3-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="394a3-241">Für eine bessere Lesbarkeit der Quelle können Sie Ihre Listen manuell inkrementieren.</span><span class="sxs-lookup"><span data-stu-id="394a3-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="394a3-242">Verwenden Sie keine Buchstaben für Listen, auch nicht für geschachtelte Listen.</span><span class="sxs-lookup"><span data-stu-id="394a3-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="394a3-243">Diese werden bei der Veröffentlichung auf Docs nicht fehlerfrei gerendert. Geschachtelte nummerierte Listen werden mit Kleinbuchstaben gerendert, wenn sie veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="394a3-244">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="394a3-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="394a3-245">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-245">This renders as follows:</span></span>

1. <span data-ttu-id="394a3-246">This is</span><span class="sxs-lookup"><span data-stu-id="394a3-246">This is</span></span>
1. <span data-ttu-id="394a3-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="394a3-247">a parent numbered list</span></span>
   1. <span data-ttu-id="394a3-248">and this is</span><span class="sxs-lookup"><span data-stu-id="394a3-248">and this is</span></span>
   1. <span data-ttu-id="394a3-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="394a3-249">a nested numbered list</span></span>
1. <span data-ttu-id="394a3-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="394a3-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="394a3-251">Liste mit Aufzählungszeichen</span><span class="sxs-lookup"><span data-stu-id="394a3-251">Bulleted list</span></span>

<span data-ttu-id="394a3-252">Verwenden Sie für eine Liste mit Aufzählungszeichen `-` oder `*` gefolgt von einem Leerzeichen am Anfang jeder Zeile:</span><span class="sxs-lookup"><span data-stu-id="394a3-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="394a3-253">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-253">This renders as follows:</span></span>

- <span data-ttu-id="394a3-254">This is</span><span class="sxs-lookup"><span data-stu-id="394a3-254">This is</span></span>
- <span data-ttu-id="394a3-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="394a3-255">a parent bulleted list</span></span>
  - <span data-ttu-id="394a3-256">and this is</span><span class="sxs-lookup"><span data-stu-id="394a3-256">and this is</span></span>
  - <span data-ttu-id="394a3-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="394a3-257">a nested bulleted list</span></span>
- <span data-ttu-id="394a3-258">All done!</span><span class="sxs-lookup"><span data-stu-id="394a3-258">All done!</span></span>

<span data-ttu-id="394a3-259">Unabhängig davon, welche Syntax Sie verwenden (`-` oder `*`), verwenden Sie diese jeweils konsistent innerhalb eines Artikels.</span><span class="sxs-lookup"><span data-stu-id="394a3-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="394a3-260">Checkliste</span><span class="sxs-lookup"><span data-stu-id="394a3-260">Checklist</span></span>

<span data-ttu-id="394a3-261">Checklisten können auf Docs mit einer benutzerdefinierten Markdownerweiterung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="394a3-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="394a3-262">Dieses Beispiel wird auf Docs folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="394a3-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="394a3-263">List item 1</span></span>
> * <span data-ttu-id="394a3-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="394a3-264">List item 2</span></span>
> * <span data-ttu-id="394a3-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="394a3-265">List item 3</span></span>

<span data-ttu-id="394a3-266">Verwenden Sie Checklisten am Anfang oder Ende eines Artikels, um zusammenzufassen, was der Leser lernen wird bzw. gelernt hat.</span><span class="sxs-lookup"><span data-stu-id="394a3-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="394a3-267">Fügen Sie keine sinnlosen Checklisten in der Mitte des Artikels ein.</span><span class="sxs-lookup"><span data-stu-id="394a3-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="394a3-268">Aktion „Nächste Schritte“</span><span class="sxs-lookup"><span data-stu-id="394a3-268">Next step action</span></span>

<span data-ttu-id="394a3-269">Sie können eine benutzerdefinierte Erweiterung verwenden, um eine Schaltfläche für weitere Schritte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="394a3-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="394a3-270">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="394a3-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="394a3-271">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="394a3-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="394a3-272">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="394a3-273">Informationen zum Hinzufügen von Code zu Artikeln</span><span class="sxs-lookup"><span data-stu-id="394a3-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="394a3-274">Sie können für nächste Schritte jede unterstützte Linkart verwenden, auch einen Markdownlink zu einer anderen Webseite.</span><span class="sxs-lookup"><span data-stu-id="394a3-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="394a3-275">In den meisten Fällen ist der Link für die nächsten Schritte ein relativer Link zu einer anderen Datei im gleichen Docset.</span><span class="sxs-lookup"><span data-stu-id="394a3-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="394a3-276">Nicht lokalisierte Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="394a3-276">Non-localized strings</span></span>

<span data-ttu-id="394a3-277">Sie können die benutzerdefinierte Markdownerweiterung `no-loc` verwenden, um Inhaltszeichenfolgen anzugeben, die beim Lokalisierungsprozess ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="394a3-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="394a3-278">Bei allen angegebenen Zeichenfolgen wird die Groß-/Kleinschreibung beachtet. Das heißt, die Zeichenfolge muss genau übereinstimmen, um bei der Lokalisierung ignoriert zu werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="394a3-279">Verwenden Sie die folgende Syntax, um eine einzelne Zeichenfolge als nicht lokalisierbar zu markieren:</span><span class="sxs-lookup"><span data-stu-id="394a3-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="394a3-280">Im folgenden Beispiel wird nur die einzelne Instanz von `Document` während des Lokalisierungsprozesses ignoriert:</span><span class="sxs-lookup"><span data-stu-id="394a3-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="394a3-281">Verwenden Sie `\`, um Sonderzeichen mit Escapezeichen zu versehen:</span><span class="sxs-lookup"><span data-stu-id="394a3-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="394a3-282">Sie können auch Metadaten im YAML-Header verwenden, um alle Instanzen einer Zeichenfolge innerhalb der aktuellen Markdowndatei als nicht lokalisierbar zu markieren:</span><span class="sxs-lookup"><span data-stu-id="394a3-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="394a3-283">Die „no-loc“-Metadaten werden in der Datei *docfx.json* nicht als globale Metadaten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="394a3-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="394a3-284">Die Lokalisierungspipeline liest die Datei *docfx.json* nicht, sodass die „no-loc“-Metadaten in jeder einzelnen Quelldatei hinzugefügt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="394a3-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="394a3-285">Im folgenden Beispiel werden sowohl in `title` der Metadaten als auch im Markdownheader das Wort `Document` während des Lokalisierungsprozesses ignoriert.</span><span class="sxs-lookup"><span data-stu-id="394a3-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="394a3-286">In `description` der Metadaten und im Markdownhauptinhalt wird das Wort `document` lokalisiert, da es nicht mit dem Großbuchstaben `D` beginnt.</span><span class="sxs-lookup"><span data-stu-id="394a3-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="394a3-287">Selektoren</span><span class="sxs-lookup"><span data-stu-id="394a3-287">Selectors</span></span>

<span data-ttu-id="394a3-288">Selektoren sind Elemente der Benutzeroberfläche, mit denen der Benutzer zwischen mehreren Varianten desselben Artikels wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="394a3-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="394a3-289">Sie werden in einigen Docsets verwendet, um unterschiedlichen Implementierungen bei verschiedenen Technologien oder Plattformen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="394a3-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="394a3-290">Selektoren sind in der Regel besonders für unsere Inhalte für mobile Plattformen geeignet, die sich an Entwickler richten.</span><span class="sxs-lookup"><span data-stu-id="394a3-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="394a3-291">Da derselbe Markdownselektor in jeder Artikeldatei enthalten ist, die diesen Selektor verwendet, wird empfohlen, dass Sie den Selektor Ihres Artikels in einer Includedatei platzieren.</span><span class="sxs-lookup"><span data-stu-id="394a3-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="394a3-292">Dann können Sie auf diese Includedatei in allen Artikeldateien, die denselben Selektor verwenden, verweisen.</span><span class="sxs-lookup"><span data-stu-id="394a3-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="394a3-293">Es gibt zwei Selektortypen: einen einfachen und einen Mehrfachselektor.</span><span class="sxs-lookup"><span data-stu-id="394a3-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="394a3-294">Einfache Auswahl</span><span class="sxs-lookup"><span data-stu-id="394a3-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="394a3-295">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="394a3-304">Mehrfachauswahl</span><span class="sxs-lookup"><span data-stu-id="394a3-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="394a3-305">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Plattform" title2="Back-End"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | JavaScript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | JavaScript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | JavaScript)](how-to-write-links.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-links.md)
> - [(Xamarin Android | JavaScript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="394a3-318">Tiefgestellt und Hochgestellt</span><span class="sxs-lookup"><span data-stu-id="394a3-318">Subscript and superscript</span></span>

<span data-ttu-id="394a3-319">Sie sollten tief- und hochgestelle Zeichen nur verwenden, wenn dies aus Gründen der technischen Genauigkeit erforderlich ist, z. B. beim Schreiben mathematischer Formeln.</span><span class="sxs-lookup"><span data-stu-id="394a3-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="394a3-320">Verwenden Sie diesen Zeichentyp nicht für nicht standardmäßige Stile, wie z. B. Fußnoten.</span><span class="sxs-lookup"><span data-stu-id="394a3-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="394a3-321">Verwenden Sie sowohl für tiefgestellte als auch hochgestellte Zeichen HTML:</span><span class="sxs-lookup"><span data-stu-id="394a3-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="394a3-322">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-322">This renders as follows:</span></span>

<span data-ttu-id="394a3-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="394a3-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="394a3-324">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-324">This renders as follows:</span></span>

<span data-ttu-id="394a3-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="394a3-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="394a3-326">Tables</span><span class="sxs-lookup"><span data-stu-id="394a3-326">Tables</span></span>

<span data-ttu-id="394a3-327">Die einfachste Möglichkeit zum Erstellen einer Tabelle in Markdown ist die Verwendung von senkrechten Strichen und Unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="394a3-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="394a3-328">Fügen Sie unter der ersten Zeile Unterstriche ein, um eine Standardtabelle mit Kopfzeile zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="394a3-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="394a3-329">Dies wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-329">This renders as follows:</span></span>

|<span data-ttu-id="394a3-330">This is</span><span class="sxs-lookup"><span data-stu-id="394a3-330">This is</span></span>   |<span data-ttu-id="394a3-331">a simple</span><span class="sxs-lookup"><span data-stu-id="394a3-331">a simple</span></span>   |<span data-ttu-id="394a3-332">table header</span><span class="sxs-lookup"><span data-stu-id="394a3-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="394a3-333">table</span><span class="sxs-lookup"><span data-stu-id="394a3-333">table</span></span>     |<span data-ttu-id="394a3-334">data</span><span class="sxs-lookup"><span data-stu-id="394a3-334">data</span></span>       |<span data-ttu-id="394a3-335">here</span><span class="sxs-lookup"><span data-stu-id="394a3-335">here</span></span>        |
|<span data-ttu-id="394a3-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="394a3-336">it doesn't</span></span>|<span data-ttu-id="394a3-337">actually</span><span class="sxs-lookup"><span data-stu-id="394a3-337">actually</span></span>   |<span data-ttu-id="394a3-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="394a3-338">have to line up nicely!</span></span>||

<span data-ttu-id="394a3-339">Sie können die Spalten mithilfe von Doppelpunkten ausrichten:</span><span class="sxs-lookup"><span data-stu-id="394a3-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="394a3-340">Dieser Code wird folgendermaßen gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-340">Renders as follows:</span></span>

| <span data-ttu-id="394a3-341">Fun</span><span class="sxs-lookup"><span data-stu-id="394a3-341">Fun</span></span>                  | <span data-ttu-id="394a3-342">With</span><span class="sxs-lookup"><span data-stu-id="394a3-342">With</span></span>                 | <span data-ttu-id="394a3-343">Tables</span><span class="sxs-lookup"><span data-stu-id="394a3-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="394a3-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="394a3-344">left-aligned column</span></span>  | <span data-ttu-id="394a3-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="394a3-345">right-aligned column</span></span> | <span data-ttu-id="394a3-346">centered column</span><span class="sxs-lookup"><span data-stu-id="394a3-346">centered column</span></span> |
| <span data-ttu-id="394a3-347">$100</span><span class="sxs-lookup"><span data-stu-id="394a3-347">$100</span></span>                 | <span data-ttu-id="394a3-348">$100</span><span class="sxs-lookup"><span data-stu-id="394a3-348">$100</span></span>                 | <span data-ttu-id="394a3-349">$100</span><span class="sxs-lookup"><span data-stu-id="394a3-349">$100</span></span>            |
| <span data-ttu-id="394a3-350">$10</span><span class="sxs-lookup"><span data-stu-id="394a3-350">$10</span></span>                  | <span data-ttu-id="394a3-351">$10</span><span class="sxs-lookup"><span data-stu-id="394a3-351">$10</span></span>                  | <span data-ttu-id="394a3-352">$10</span><span class="sxs-lookup"><span data-stu-id="394a3-352">$10</span></span>             |
| <span data-ttu-id="394a3-353">$1</span><span class="sxs-lookup"><span data-stu-id="394a3-353">$1</span></span>                   | <span data-ttu-id="394a3-354">$1</span><span class="sxs-lookup"><span data-stu-id="394a3-354">$1</span></span>                   | <span data-ttu-id="394a3-355">$1</span><span class="sxs-lookup"><span data-stu-id="394a3-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="394a3-356">Mit der Erweiterung „Docs Authoring Pack“ für VS Code können Sie einfache Tabellen unkompliziert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="394a3-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="394a3-357">Sie können auch den [Tables Generator](http://www.tablesgenerator.com/markdown_tables) verwenden.</span><span class="sxs-lookup"><span data-stu-id="394a3-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="394a3-358">Zeilenumbrüche innerhalb von Wörtern in einer Tabellenzelle</span><span class="sxs-lookup"><span data-stu-id="394a3-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="394a3-359">Lange Wörter in einer Markdowntabelle können dazu führen, dass die Tabelle in den rechten Navigationsbereich hineinreicht und nicht mehr lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="394a3-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="394a3-360">Sie können dieses Problem lösen, indem Sie beim Rendern auf Docs zulassen, dass bei Bedarf automatisch Zeilenumbrüche in Wörter eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="394a3-361">Dafür müssen Sie die Tabelle nur mit der benutzerdefinierten Klasse `[!div class="mx-tdBreakAll"]` umschließen.</span><span class="sxs-lookup"><span data-stu-id="394a3-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="394a3-362">Im Folgenden finden Sie ein Markdownbeispiel einer Tabelle mit drei Zeilen, die von einem `div`-Element mit dem Klassennamen `mx-tdBreakAll` umschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="394a3-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="394a3-363">Dieser Code wird wie folgt gerendert:</span><span class="sxs-lookup"><span data-stu-id="394a3-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="394a3-364">Name</span><span class="sxs-lookup"><span data-stu-id="394a3-364">Name</span></span>|<span data-ttu-id="394a3-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="394a3-365">Syntax</span></span>|<span data-ttu-id="394a3-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="394a3-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="394a3-367">Description</span><span class="sxs-lookup"><span data-stu-id="394a3-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="394a3-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="394a3-368">Quiet</span></span>|<span data-ttu-id="394a3-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="394a3-369">/quiet</span></span>|<span data-ttu-id="394a3-370">Yes</span><span class="sxs-lookup"><span data-stu-id="394a3-370">Yes</span></span>|<span data-ttu-id="394a3-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="394a3-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="394a3-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="394a3-372">NoRestart</span></span>|<span data-ttu-id="394a3-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="394a3-373">/norestart</span></span>|<span data-ttu-id="394a3-374">No</span><span class="sxs-lookup"><span data-stu-id="394a3-374">No</span></span>|<span data-ttu-id="394a3-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="394a3-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="394a3-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="394a3-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="394a3-377">Help</span><span class="sxs-lookup"><span data-stu-id="394a3-377">Help</span></span>|<span data-ttu-id="394a3-378">/help</span><span class="sxs-lookup"><span data-stu-id="394a3-378">/help</span></span>|<span data-ttu-id="394a3-379">No</span><span class="sxs-lookup"><span data-stu-id="394a3-379">No</span></span>|<span data-ttu-id="394a3-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="394a3-380">Provides help and quick reference.</span></span> <span data-ttu-id="394a3-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="394a3-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="394a3-382">Zeilenumbrüche innerhalb von Wörtern in Tabellenzellen der zweiten Spalte</span><span class="sxs-lookup"><span data-stu-id="394a3-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="394a3-383">Möglicherweise möchten Sie, dass Zeilenumbrüche innerhalb von Wörtern nur in der zweiten Spalte einer Tabelle automatisch eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="394a3-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="394a3-384">Um Zeilenumbrüche auf die zweite Spalte zu beschränken, wenden Sie die Klasse `mx-tdCol2BreakAll` wie oben gezeigt mithilfe der `div`-Wrappersyntax an.</span><span class="sxs-lookup"><span data-stu-id="394a3-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="394a3-385">Datenmatrixtabellen</span><span class="sxs-lookup"><span data-stu-id="394a3-385">Data matrix tables</span></span>

<span data-ttu-id="394a3-386">Eine Datenmatrixtabelle weist sowohl einen Header als auch eine gewichtete erste Spalte auf, sodass eine Matrix mit einer leeren Zelle in der oberen linken Ecke erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="394a3-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="394a3-387">Die Dokumente enthalten benutzerdefiniertes Markdown für Datenmatrixtabellen:</span><span class="sxs-lookup"><span data-stu-id="394a3-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="394a3-388">In der ersten Spalte muss jeder Eintrag fett formatiert sein (`**bold**`). Andernfalls sind die Tabellen für die Sprachausgabe nicht zugänglich und für Dokumente ungültig.</span><span class="sxs-lookup"><span data-stu-id="394a3-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="394a3-389">HTML-Tabellen</span><span class="sxs-lookup"><span data-stu-id="394a3-389">HTML Tables</span></span>

<span data-ttu-id="394a3-390">HTML-Tabellen werden für docs.microsoft.com nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="394a3-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="394a3-391">Sie können in der Quelle nicht von Menschen gelesen werden, was jedoch ein wichtiges Merkmal von Markdown ist.</span><span class="sxs-lookup"><span data-stu-id="394a3-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
