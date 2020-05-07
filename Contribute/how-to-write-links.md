---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624745"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="8c49f-103">Verwenden von Links in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8c49f-103">Use links in documentation</span></span>

<span data-ttu-id="8c49f-104">In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="8c49f-105">Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="8c49f-106">Benutzer werden über Links auf Inhalte derselben Seite, auf benachbarten Seiten oder auf externen Websites und URLs verwiesen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="8c49f-107">Das Back-End der Website „docs.microsoft.com“ nutzt Open Publishing Services (OPS). Dadurch wird [CommonMark][]-konformes Markdown unterstützt, das durch die [Markdig][]-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="8c49f-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="8c49f-108">Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)][GFM] kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="8c49f-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="8c49f-109">Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c49f-110">Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).</span><span class="sxs-lookup"><span data-stu-id="8c49f-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="8c49f-111">Linktext</span><span class="sxs-lookup"><span data-stu-id="8c49f-111">Link text</span></span>

<span data-ttu-id="8c49f-112">Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein.</span><span class="sxs-lookup"><span data-stu-id="8c49f-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="8c49f-113">Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c49f-114">Verwenden Sie nicht die Formulierung „Hier klicken“.</span><span class="sxs-lookup"><span data-stu-id="8c49f-114">Do not use "click here."</span></span> <span data-ttu-id="8c49f-115">Diese ist im Hinblick auf die Suchmaschinenoptimierung suboptimal und beschreibt das Linkziel nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="8c49f-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="8c49f-116">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="8c49f-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="8c49f-117">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="8c49f-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="8c49f-118">Links in einem Artikel zum anderen Artikel</span><span class="sxs-lookup"><span data-stu-id="8c49f-118">Links from one article to another</span></span>

<span data-ttu-id="8c49f-119">Das Veröffentlichungssystem unterstützt zwei Arten von Hyperlinks: **URLs** und **Dateilinks**.</span><span class="sxs-lookup"><span data-stu-id="8c49f-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="8c49f-120">Bei einem URL-Link kann es sich um einen URL-Pfad handeln, der relativ zum Stammverzeichnis von docs.microsoft.com ist, oder um eine absolute URL, die die vollständige URL-Syntax enthält (z. B. `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span><span class="sxs-lookup"><span data-stu-id="8c49f-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="8c49f-121">Verwenden Sie URL-Links, wenn Sie Inhalt außerhalb des aktuellen _Docsets_ oder zwischen automatisch generierten Referenz- und Konzeptartikeln innerhalb des Docsets verlinken.</span><span class="sxs-lookup"><span data-stu-id="8c49f-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="8c49f-122">Die einfachste Möglichkeit zum Erstellen eines relativen Links besteht darin, die URL aus Ihrem Browser zu kopieren und dann `https://docs.microsoft.com/en-us` aus dem Wert zu entfernen, den Sie in den Markdowncode einfügen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="8c49f-123">URLs für Microsoft-Eigenschaften sollten keine Gebietsschemas enthalten. Entfernen Sie also beispielsweise „/de-de“ aus der URL.</span><span class="sxs-lookup"><span data-stu-id="8c49f-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="8c49f-124">Ein Dateilink wird verwendet, um einen Artikel mit einem anderen innerhalb des Docsets zu verlinken.</span><span class="sxs-lookup"><span data-stu-id="8c49f-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="8c49f-125">Für alle Dateipfade müssen Schrägstriche (`/`) anstelle von umgekehrten Schrägstrichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="8c49f-126">Einem Artikel wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8c49f-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="8c49f-127">Ein Artikel verweist auf einen Artikel im übergeordneten Verzeichnis des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="8c49f-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="8c49f-128">Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="8c49f-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="8c49f-129">Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des übergeordneten Verzeichnisses des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="8c49f-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="8c49f-130">In keinem der oben stehenden Beispiele wird `~/` als Teil des Links verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c49f-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="8c49f-131">Wenn Sie auf einen absoluten Pfad verweisen möchten, der im Stammverzeichnis des Repositorys beginnt, beginnen Sie den Link mit `/`.</span><span class="sxs-lookup"><span data-stu-id="8c49f-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="8c49f-132">Wenn Sie ein `~/` einfügen, wird dadurch beim Navigieren in den Quellrepositorys auf GitHub ein ungültiger Link erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="8c49f-133">Wenn der Pfad mit `/` beginnt, kann der Link ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="8c49f-134">Linkstruktur auf docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="8c49f-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="8c49f-135">Auf docs.microsoft.com veröffentlichte Inhalte weisen folgende URL-Struktur auf:</span><span class="sxs-lookup"><span data-stu-id="8c49f-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="8c49f-136">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="8c49f-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="8c49f-137">`<locale>`: gibt die Sprache des Artikels an (Beispiel: de-de oder en-us)</span><span class="sxs-lookup"><span data-stu-id="8c49f-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="8c49f-138">`<product-service>`: gibt den Namen des Produkts oder Diensts an (Beispiel: powershell, dotnet oder azure)</span><span class="sxs-lookup"><span data-stu-id="8c49f-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="8c49f-139">`[<feature-service>]` (optional): gibt den Featurenamen oder Subdienst des Produkts an (Beispiel: csharp oder load-balancer)</span><span class="sxs-lookup"><span data-stu-id="8c49f-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="8c49f-140">`[<subfolder>]` (optional): der Name eines Unterordners innerhalb eines Features</span><span class="sxs-lookup"><span data-stu-id="8c49f-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="8c49f-141">`<topic>`: der Name der Artikeldatei für das Thema (Beispiel: load-balancer-overview oder overview)</span><span class="sxs-lookup"><span data-stu-id="8c49f-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="8c49f-142">`[?view=\<view-name>]` (optional): der Ansichtsname, der von der Versionsauswahl für Inhalt mit mehreren verfügbaren Versionen verwendet wird (Beispiel: azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="8c49f-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="8c49f-143">Artikel im selben _Docset_ besitzen meistens das gleiche `<product-service>`-URL-Fragment.</span><span class="sxs-lookup"><span data-stu-id="8c49f-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="8c49f-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8c49f-144">For example:</span></span>
> - <span data-ttu-id="8c49f-145">Gleiches Docset</span><span class="sxs-lookup"><span data-stu-id="8c49f-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="8c49f-146">Anderes Docset</span><span class="sxs-lookup"><span data-stu-id="8c49f-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="8c49f-147">Lesezeichenlinks</span><span class="sxs-lookup"><span data-stu-id="8c49f-147">Bookmark links</span></span>

<span data-ttu-id="8c49f-148">Verwenden Sie ein Hashsymbol gefolgt von der Überschrift in Kleinbuchstaben, um einen Lesezeichenlink zu einer Überschrift in der *aktuellen* Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="8c49f-149">Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche:</span><span class="sxs-lookup"><span data-stu-id="8c49f-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="8c49f-150">Wenn Sie eine Lesezeichenüberschrift in einem anderen Artikel verlinken möchten, verwenden Sie einen datei- oder websitebezogenen Link und ein Hashsymbol gefolgt von der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="8c49f-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="8c49f-151">Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche:</span><span class="sxs-lookup"><span data-stu-id="8c49f-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="8c49f-152">Sie können auch den Lesezeichenlink aus der URL kopieren.</span><span class="sxs-lookup"><span data-stu-id="8c49f-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="8c49f-153">Zeigen Sie mit der Maus auf die Kopfzeile von docs.microsoft.com, um zur URL zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="8c49f-154">Das Linksymbol sollte angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8c49f-154">You should see a link icon appear:</span></span>

![Linksymbol in Artikelüberschrift](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="8c49f-156">Klicken Sie auf das Linksymbol, und kopieren Sie dann den Ankertext des Lesezeichens aus der URL (d. h. den Teil nach dem Hash).</span><span class="sxs-lookup"><span data-stu-id="8c49f-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="8c49f-157">Die Docs-Erweiterung bietet auch Tools zum Erstellen von Links.</span><span class="sxs-lookup"><span data-stu-id="8c49f-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="8c49f-158">Explizite Ankerlinks</span><span class="sxs-lookup"><span data-stu-id="8c49f-158">Explicit anchor links</span></span>

<span data-ttu-id="8c49f-159">Es ist nicht erforderlich und wird nicht empfohlen, explizite Ankerlinks mit dem HTML-Tag `<a>` hinzufügen (Ausnahmen: im Hub und auf der Landing Page).</span><span class="sxs-lookup"><span data-stu-id="8c49f-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="8c49f-160">Verwenden Sie stattdessen wie unter [Lesezeichenlinks](#bookmark-links) beschrieben die automatisch generierten Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="8c49f-161">Deklarieren Sie folgendermaßen Anker für den Hub und die Landing Page:</span><span class="sxs-lookup"><span data-stu-id="8c49f-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="8c49f-162">oder</span><span class="sxs-lookup"><span data-stu-id="8c49f-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="8c49f-163">So können Sie einen Link zum Anker erstellen:</span><span class="sxs-lookup"><span data-stu-id="8c49f-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="8c49f-164">Ankertext muss immer aus Kleinbuchstaben bestehen und darf keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c49f-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="8c49f-165">XRef-Links (Querverweise)</span><span class="sxs-lookup"><span data-stu-id="8c49f-165">XRef (cross reference) links</span></span>

<span data-ttu-id="8c49f-166">Es wird empfohlen, XRef-Links zum Verlinken mit APIs zu verwenden, da diese zur Buildzeit überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="8c49f-167">Verwenden Sie XRef-Links mit der eindeutigen ID ([UID](#determine-the-uid)) des Typs oder Members, um automatisch generierte Links zu API-Referenzen im aktuellen Docset oder in anderen Docsets hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="8c49f-168">Sie können die [Docs-Markdownerweiterung für Visual Studio Code][docsextension] (im Docs Authoring Pack enthalten) verwenden, um .NET-XRef-Links einzufügen, die im [.NET-API-Browser][] angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="8c49f-169">Überprüfen Sie, ob die API, die Sie verlinken möchten, sich auf [docs.microsoft.com][docs] befindet, indem Sie ihren Namen ganz oder teilweise in den [.NET-API-Browser][] oder das [UWP][] eingeben.</span><span class="sxs-lookup"><span data-stu-id="8c49f-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="8c49f-170">Wenn keine Ergebnisse angezeigt werden, ist sie noch nicht auf docs.microsoft.com vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="8c49f-171">Sie können eine der folgenden Syntaxvarianten auswählen:</span><span class="sxs-lookup"><span data-stu-id="8c49f-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="8c49f-172">Automatische Links:</span><span class="sxs-lookup"><span data-stu-id="8c49f-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="8c49f-173">Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.</span><span class="sxs-lookup"><span data-stu-id="8c49f-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="8c49f-174">Der optionale Abfrageparameter `displayProperty=nameWithType` erzeugt einen vollqualifizierten Linktext, der **namespace.typ** für Typen und **typ.member** für Typmember (inklusive Enumerationstypenmember) lautet.</span><span class="sxs-lookup"><span data-stu-id="8c49f-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="8c49f-175">Markdownlinks:</span><span class="sxs-lookup"><span data-stu-id="8c49f-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="8c49f-176">Verwenden Sie Markdownlinks für XRef, wenn Sie den angezeigten Linktext anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c49f-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="8c49f-177">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="8c49f-177">Examples:</span></span>

- <span data-ttu-id="8c49f-178">**\<xref:System.String>** wird als <xref:System.String> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="8c49f-179">**\<xref:System.String?displayProperty=nameWithType>** wird als <xref:System.String?displayProperty=nameWithType> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="8c49f-180">**\[String-Klasse](xref:System.String)** wird als [String-Klasse](xref:System.String) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="8c49f-181">Der Abfrageparameter `displayProperty=fullName` funktioniert genau wie `displayProperty=nameWithType` für Klassen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="8c49f-182">Der Linktext wird also zu **namespace.klassenname**.</span><span class="sxs-lookup"><span data-stu-id="8c49f-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="8c49f-183">Für Member wird der Linktext jedoch als **namespace.klassenname.membername** angezeigt. Das ist möglicherweise nicht erwünscht.</span><span class="sxs-lookup"><span data-stu-id="8c49f-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="8c49f-184">Bei UIDs wird die Groß-/Kleinschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-184">UIDs are case sensitive.</span></span> <span data-ttu-id="8c49f-185">Beispielsweise wird `<xref:System.Object>` ordnungsgemäß aufgelöst, `<xref:system.object>` jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="8c49f-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="8c49f-186">XRef-Buildwarnungen und inkrementelle Builds</span><span class="sxs-lookup"><span data-stu-id="8c49f-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="8c49f-187">Bei einem inkrementellen Build werden nur Dateien erstellt, die geändert wurden oder von einer Änderung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="8c49f-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="8c49f-188">Wenn eine Buildwarnung zu einem ungültigen XRef-Link angezeigt wird, der Link aber eigentlich gültig ist, kann das daran liegen, dass es sich um einen inkrementellen Build handelt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="8c49f-189">Die Datei, die die Warnung verursacht hat, wurde nicht geändert und deshalb nicht erstellt, sodass frühere Warnungen wiederholt angezeigt wurden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="8c49f-190">Die Warnung wird nicht mehr angezeigt, wenn die Datei geändert wird oder Sie einen vollständigen Build initiieren (über ops.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="8c49f-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="8c49f-191">Das ist ein Nachteil von inkrementellen Builds, da DocFX keine Datenupdates im XRef-Dienst erkennt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="8c49f-192">Ermitteln der UID</span><span class="sxs-lookup"><span data-stu-id="8c49f-192">Determine the UID</span></span>

<span data-ttu-id="8c49f-193">Die UID entspricht in der Regel dem vollqualifizierten Klassen- oder Membernamen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="8c49f-194">Es gibt mindestens zwei Möglichkeiten, die UID zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="8c49f-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="8c49f-195">Rechtsklicken Sie auf die Seite [Dokumentation][docs] eines Typs oder Members, klicken Sie dann auf **Quelltext anzeigen**, und kopieren Sie den **content**-Wert von **ms.assetid**:</span><span class="sxs-lookup"><span data-stu-id="8c49f-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid im Quelltext der Webseite](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="8c49f-197">Nutzen Sie die [automatische Vervollständigung][], indem Sie den Typnamen ganz oder teilweise an die URL anfügen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="8c49f-198">Wenn Sie beispielsweise `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in die Adressleiste Ihres Browsers eingeben, werden alle Typen und Methoden angezeigt, die **Writeline** im Namen enthalten, sowie die jeweilige UID.</span><span class="sxs-lookup"><span data-stu-id="8c49f-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="8c49f-199">Überprüfen der UID</span><span class="sxs-lookup"><span data-stu-id="8c49f-199">Verify the UID</span></span>

<span data-ttu-id="8c49f-200">Sie können testen, ob die UID korrekt ist, indem Sie **System.String** in der folgenden URL durch Ihre UID ersetzen und diese dann in die Adressleiste eines Browsers einfügen:</span><span class="sxs-lookup"><span data-stu-id="8c49f-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="8c49f-201">Bei der UID in der URL wird die Groß-/Kleinschreibung beachtet. Vermeiden Sie zudem Leerzeichen zwischen den Parametertypen, wenn Sie eine Methodenüberladungs-UID überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="8c49f-202">Wenn die Ausgabe der folgenden ähnelt, ist die UID korrekt:</span><span class="sxs-lookup"><span data-stu-id="8c49f-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="8c49f-203">Wenn auf der Seite nur `[]` angezeigt wird, ist die UID nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="8c49f-204">Prozentcodierung von URLs</span><span class="sxs-lookup"><span data-stu-id="8c49f-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="8c49f-205">Sonderzeichen in der UID müssen folgendermaßen HTML-codiert werden:</span><span class="sxs-lookup"><span data-stu-id="8c49f-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="8c49f-206">Zeichen</span><span class="sxs-lookup"><span data-stu-id="8c49f-206">Character</span></span> | <span data-ttu-id="8c49f-207">HTML-Codierung</span><span class="sxs-lookup"><span data-stu-id="8c49f-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="8c49f-208">%60</span><span class="sxs-lookup"><span data-stu-id="8c49f-208">%60</span></span>           |
| `#`       | <span data-ttu-id="8c49f-209">%23</span><span class="sxs-lookup"><span data-stu-id="8c49f-209">%23</span></span>           |
| `*`       | <span data-ttu-id="8c49f-210">%2A</span><span class="sxs-lookup"><span data-stu-id="8c49f-210">%2A</span></span>           |

<span data-ttu-id="8c49f-211">Hier finden Sie eine vollständige Liste der [Prozentcodierungen](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="8c49f-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="8c49f-212">Codierungsbeispiele:</span><span class="sxs-lookup"><span data-stu-id="8c49f-212">Encoding examples:</span></span>

- <span data-ttu-id="8c49f-213">`System.Threading.Tasks.Task``1` wird als `System.Threading.Tasks.Task%601` codiert (Vergleich: [Abschnitt zu generischen Typen](#generic-types)).</span><span class="sxs-lookup"><span data-stu-id="8c49f-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="8c49f-214">`System.Exception.#ctor` wird als `System.Exception.%23ctor` codiert.</span><span class="sxs-lookup"><span data-stu-id="8c49f-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="8c49f-215">`System.Object.Equals*` wird als `System.Object.Equals%2A` codiert.</span><span class="sxs-lookup"><span data-stu-id="8c49f-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="8c49f-216">Generische Typen</span><span class="sxs-lookup"><span data-stu-id="8c49f-216">Generic types</span></span>

<span data-ttu-id="8c49f-217">Bei generischen Typen handelt es sich um Typen wie `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="8c49f-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="8c49f-218">Wenn Sie einen solchen Typ im [.NET-API-Browser](https://docs.microsoft.com/dotnet/api/) suchen, stellen Sie bei der URL fest, dass `<T>` im Format `-1` dargestellt wird und somit eigentlich für **\`1** steht:</span><span class="sxs-lookup"><span data-stu-id="8c49f-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="8c49f-219">Für eine Verlinkung mit einem generischen Typ wie **List\<T>** müssen Sie das Backtickzeichen **\`** wie im folgenden Beispiel dargestellt als **%60** codieren:</span><span class="sxs-lookup"><span data-stu-id="8c49f-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="8c49f-220">Methoden</span><span class="sxs-lookup"><span data-stu-id="8c49f-220">Methods</span></span>

<span data-ttu-id="8c49f-221">Für die Verlinkung mit einer Methode können Sie entweder einen Link zur allgemeinen Methodenseite erstellen, indem Sie ein Sternchen (`*`) an den Methodennamen anfügen, oder zu einer bestimmten Überladung.</span><span class="sxs-lookup"><span data-stu-id="8c49f-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="8c49f-222">Verwenden Sie die allgemeine Seite beispielsweise, wenn Sie einen Link zur `<xref:System.Object.Equals%2A?displayProperty=nameWithType>`-Methode ohne bestimmte Parametertypen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c49f-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="8c49f-223">Das Sternchen wird als `%2A` codiert.</span><span class="sxs-lookup"><span data-stu-id="8c49f-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="8c49f-224">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8c49f-224">For example:</span></span>

<span data-ttu-id="8c49f-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` verlinkt zu <xref:System.Object.Equals%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="8c49f-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="8c49f-226">Für eine Verlinkung zu einer bestimmten Überladung müssen Sie nach dem Methodennamen Klammern einfügen und dort die vollständigen Namen der einzelnen Parameter eingeben.</span><span class="sxs-lookup"><span data-stu-id="8c49f-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="8c49f-227">Fügen Sie kein Leerzeichen zwischen den Typnamen ein, da der Link andernfalls nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8c49f-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="8c49f-228">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8c49f-228">For example:</span></span>

<span data-ttu-id="8c49f-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` verlinkt zu <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="8c49f-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="8c49f-230">Links von Includes</span><span class="sxs-lookup"><span data-stu-id="8c49f-230">Links from includes</span></span>

<span data-ttu-id="8c49f-231">Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="8c49f-232">Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="8c49f-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="8c49f-233">Mit dem Erweiterung [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) für Visual Studio Code können Sie relative Links und Lesezeichenlinks korrekt einfügen, ohne sich um den Pfad Gedanken machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="8c49f-234">Links in Selektoren</span><span class="sxs-lookup"><span data-stu-id="8c49f-234">Links in selectors</span></span>

<span data-ttu-id="8c49f-235">Ein Selektor ist eine Komponente zum Navigieren, die in einem Dokumentationsartikel als Dropdownliste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c49f-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="8c49f-236">Wenn ein Leser einen Wert in der Dropdownliste auswählt, wird der ausgewählte Artikel im Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8c49f-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="8c49f-237">In der Regel enthält die Selektorliste Links zu Artikeln, die in engem Zusammenhang stehen, z.B. der gleiche Inhalt in mehreren Programmiersprachen oder eine zusammenhängende Reihe von Artikeln.</span><span class="sxs-lookup"><span data-stu-id="8c49f-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="8c49f-238">Wenn Sie in einer Includedatei eingebettete Selektoren verwenden, verwenden Sie folgende Linkstruktur:</span><span class="sxs-lookup"><span data-stu-id="8c49f-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="8c49f-239">Verweislinks</span><span class="sxs-lookup"><span data-stu-id="8c49f-239">Reference-style links</span></span>

<span data-ttu-id="8c49f-240">Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="8c49f-241">Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können.</span><span class="sxs-lookup"><span data-stu-id="8c49f-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="8c49f-242">Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:</span><span class="sxs-lookup"><span data-stu-id="8c49f-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="8c49f-243">Inlinetext:</span><span class="sxs-lookup"><span data-stu-id="8c49f-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="8c49f-244">Linkverweise am Ende des Artikels:</span><span class="sxs-lookup"><span data-stu-id="8c49f-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="8c49f-245">Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="8c49f-246">Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8c49f-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="8c49f-247">Link zu Seiten außerhalb der technischen Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8c49f-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="8c49f-248">Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="8c49f-249">Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:</span><span class="sxs-lookup"><span data-stu-id="8c49f-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="8c49f-250">Links zu Websites von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="8c49f-250">Links to third-party sites</span></span>

<span data-ttu-id="8c49f-251">Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="8c49f-252">Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="8c49f-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="8c49f-253">**Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="8c49f-254">Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google.</span><span class="sxs-lookup"><span data-stu-id="8c49f-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="8c49f-255">Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.</span><span class="sxs-lookup"><span data-stu-id="8c49f-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="8c49f-256">**Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="8c49f-257">Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="8c49f-258">**Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8c49f-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="8c49f-259">**Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8c49f-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="8c49f-260">Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c49f-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="8c49f-261">Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“</span><span class="sxs-lookup"><span data-stu-id="8c49f-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="8c49f-262">**Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="8c49f-263">Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="8c49f-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="8c49f-264">**Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder microsoft.com-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.</span><span class="sxs-lookup"><span data-stu-id="8c49f-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET-API-Browser]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[UWP]: https://docs.microsoft.com/uwp/api
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Automatische Vervollständigung]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
