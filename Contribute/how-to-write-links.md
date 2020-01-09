---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 970f80b4e6ce795e0e2f15192d31680d7de6d35b
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188342"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="935cc-103">Verwenden von Links in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="935cc-103">Use links in documentation</span></span>

<span data-ttu-id="935cc-104">In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="935cc-105">Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="935cc-106">Benutzer werden über Links auf Inhalte derselben Seite, auf benachbarten Seiten oder auf externen Websites und URLs verwiesen.</span><span class="sxs-lookup"><span data-stu-id="935cc-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="935cc-107">Das Back-End der Website „docs.microsoft.com“ nutzt Open Publishing Services (OPS). Dadurch wird [CommonMark](https://commonmark.org/)-konformes Markdown unterstützt, das durch die [Markdig](https://github.com/lunet-io/markdig)-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="935cc-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark](https://commonmark.org/)-compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="935cc-108">Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="935cc-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="935cc-109">Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="935cc-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="935cc-110">Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).</span><span class="sxs-lookup"><span data-stu-id="935cc-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="935cc-111">Linktext</span><span class="sxs-lookup"><span data-stu-id="935cc-111">Link text</span></span>

<span data-ttu-id="935cc-112">Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein.</span><span class="sxs-lookup"><span data-stu-id="935cc-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="935cc-113">Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="935cc-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="935cc-114">Verwenden Sie nicht die Formulierung „Hier klicken“.</span><span class="sxs-lookup"><span data-stu-id="935cc-114">Do not use "click here."</span></span> <span data-ttu-id="935cc-115">Diese ist im Hinblick auf die Suchmaschinenoptimierung suboptimal und beschreibt das Linkziel nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="935cc-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="935cc-116">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="935cc-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="935cc-117">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="935cc-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="935cc-118">Links in einem Artikel zum anderen Artikel</span><span class="sxs-lookup"><span data-stu-id="935cc-118">Links from one article to another</span></span>

<span data-ttu-id="935cc-119">Verwenden Sie zum Erstellen eines Inlinelinks in einem technischen Dokumentationsartikel zu einem anderen technischen Dokumentationsartikel innerhalb desselben *Dokumentationssatzes* die folgende Linksyntax:</span><span class="sxs-lookup"><span data-stu-id="935cc-119">To create an inline link from a Docs technical article to another Docs technical article within the same *docset*, use the following link syntax:</span></span>

- <span data-ttu-id="935cc-120">Einem Artikel wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="935cc-120">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="935cc-121">Ein Artikel verweist auf einen Artikel im übergeordneten Verzeichnis des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="935cc-121">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="935cc-122">Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="935cc-122">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="935cc-123">Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des übergeordneten Verzeichnisses des aktuellen Verzeichnisses:</span><span class="sxs-lookup"><span data-stu-id="935cc-123">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="935cc-124">In keinem der oben stehenden Beispiele wird `~/` als Teil des Links verwendet.</span><span class="sxs-lookup"><span data-stu-id="935cc-124">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="935cc-125">Wenn Sie auf einen absoluten Pfad verweisen möchten, der im Stammverzeichnis des Repositorys beginnt, beginnen Sie den Link mit `/`.</span><span class="sxs-lookup"><span data-stu-id="935cc-125">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="935cc-126">Wenn Sie ein `~/` einfügen, wird dadurch beim Navigieren in den Quellrepositorys auf GitHub ein ungültiger Link erstellt.</span><span class="sxs-lookup"><span data-stu-id="935cc-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="935cc-127">Wenn der Pfad mit `/` beginnt, kann der Link ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-127">Starting the path with `/` resolves correctly.</span></span>

<span data-ttu-id="935cc-128">Wenn Sie auf einen Artikel in einem anderen Dokumentationssatz verweisen möchten, verwenden Sie die folgende Syntax (auch wenn sich die Dateien im selben Repository befinden sollten):</span><span class="sxs-lookup"><span data-stu-id="935cc-128">To link to an article in a different docset, even if the file is in the same repository, use the following syntax:</span></span>

`[link text](/docset-root/directory/article-name)`
   
<span data-ttu-id="935cc-129">Wenn beispielsweise ein Artikel, dessen Stamm-URL `https://docs.microsoft.com/dotnet` lautet, auf einen Artikel verweist, dessen Stamm-URL `https://docs.microsoft.com/visualstudio` ist, sähe der Link so aus: `[link text](/visualstudio/directory/article-name)`.</span><span class="sxs-lookup"><span data-stu-id="935cc-129">For example, if an article whose root URL is `https://docs.microsoft.com/dotnet` links to an article whose root URL is `https://docs.microsoft.com/visualstudio`, the link would look like `[link text](/visualstudio/directory/article-name)`.</span></span>

> [!TIP]
> <span data-ttu-id="935cc-130">Artikel im selben *Dokumentationssatz* besitzen das gleiche URL-Fragment nach „docs.microsoft.com“.</span><span class="sxs-lookup"><span data-stu-id="935cc-130">Articles in the same *docset* have the same URL fragment after "docs.microsoft.com".</span></span> <span data-ttu-id="935cc-131">`https://docs.microsoft.com/dotnet/core/get-started` und `https://docs.microsoft.com/dotnet/framework/install` befinden sich z. B. im selben Dokumentationssatz, aber `https://docs.microsoft.com/dotnet/core/get-started` und `https://docs.microsoft.com/visualstudio/whats-new` befinden sich in verschiedenen Dokumentationssätzen.</span><span class="sxs-lookup"><span data-stu-id="935cc-131">For example, `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/dotnet/framework/install` are in the same docset, and `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/visualstudio/whats-new` are in different docsets.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="935cc-132">Links zu Verankerungen</span><span class="sxs-lookup"><span data-stu-id="935cc-132">Links to anchors</span></span>

<span data-ttu-id="935cc-133">Sie müssen keine Anker erstellen.</span><span class="sxs-lookup"><span data-stu-id="935cc-133">You do not have to create anchors.</span></span> <span data-ttu-id="935cc-134">Sie werden automatisch bei der Veröffentlichung aller H2-Überschriften generiert.</span><span class="sxs-lookup"><span data-stu-id="935cc-134">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="935cc-135">Sie müssen lediglich Links zu den H2-Abschnitten erstellen.</span><span class="sxs-lookup"><span data-stu-id="935cc-135">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="935cc-136">So erstellen Sie einen Link zu einer Überschrift im selben Artikel</span><span class="sxs-lookup"><span data-stu-id="935cc-136">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="935cc-137">So erstellen Sie einen Link zu einer Verankerung in einem anderen Artikel:</span><span class="sxs-lookup"><span data-stu-id="935cc-137">To link to an anchor in another article:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="935cc-138">Links von Includes</span><span class="sxs-lookup"><span data-stu-id="935cc-138">Links from includes</span></span>

<span data-ttu-id="935cc-139">Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden.</span><span class="sxs-lookup"><span data-stu-id="935cc-139">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="935cc-140">Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="935cc-140">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="935cc-141">Links in Selektoren</span><span class="sxs-lookup"><span data-stu-id="935cc-141">Links in selectors</span></span>

<span data-ttu-id="935cc-142">Ein Selektor ist eine Komponente zum Navigieren, die in einem Dokumentationsartikel als Dropdownliste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="935cc-142">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="935cc-143">Wenn ein Leser einen Wert in der Dropdownliste auswählt, wird der ausgewählte Artikel im Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="935cc-143">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="935cc-144">In der Regel enthält die Selektorliste Links zu Artikeln, die in engem Zusammenhang stehen, z.B. der gleiche Inhalt in mehreren Programmiersprachen oder eine zusammenhängende Reihe von Artikeln.</span><span class="sxs-lookup"><span data-stu-id="935cc-144">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="935cc-145">Wenn Sie in einer Includedatei eingebettete Selektoren verwenden, verwenden Sie folgende Linkstruktur:</span><span class="sxs-lookup"><span data-stu-id="935cc-145">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="935cc-146">Verweislinks</span><span class="sxs-lookup"><span data-stu-id="935cc-146">Reference-style links</span></span>

<span data-ttu-id="935cc-147">Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden.</span><span class="sxs-lookup"><span data-stu-id="935cc-147">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="935cc-148">Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können.</span><span class="sxs-lookup"><span data-stu-id="935cc-148">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="935cc-149">Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:</span><span class="sxs-lookup"><span data-stu-id="935cc-149">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="935cc-150">Inlinetext:</span><span class="sxs-lookup"><span data-stu-id="935cc-150">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="935cc-151">Linkverweise am Ende des Artikels:</span><span class="sxs-lookup"><span data-stu-id="935cc-151">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="935cc-152">Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen.</span><span class="sxs-lookup"><span data-stu-id="935cc-152">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="935cc-153">Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="935cc-153">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="935cc-154">Link zu Seiten außerhalb der technischen Dokumentation</span><span class="sxs-lookup"><span data-stu-id="935cc-154">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="935cc-155">Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen.</span><span class="sxs-lookup"><span data-stu-id="935cc-155">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="935cc-156">Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:</span><span class="sxs-lookup"><span data-stu-id="935cc-156">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="935cc-157">Links zu Websites von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="935cc-157">Links to third-party sites</span></span>

<span data-ttu-id="935cc-158">Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-158">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="935cc-159">Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="935cc-159">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="935cc-160">**Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen.</span><span class="sxs-lookup"><span data-stu-id="935cc-160">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="935cc-161">Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google.</span><span class="sxs-lookup"><span data-stu-id="935cc-161">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="935cc-162">Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.</span><span class="sxs-lookup"><span data-stu-id="935cc-162">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="935cc-163">**Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-163">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="935cc-164">Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="935cc-164">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="935cc-165">**Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="935cc-165">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="935cc-166">**Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="935cc-166">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="935cc-167">Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="935cc-167">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="935cc-168">Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“</span><span class="sxs-lookup"><span data-stu-id="935cc-168">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="935cc-169">**Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="935cc-169">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="935cc-170">Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="935cc-170">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="935cc-171">**Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder „ms.com“-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.</span><span class="sxs-lookup"><span data-stu-id="935cc-171">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="935cc-172">Link zu weiterführenden Azure PowerShell-Inhalten</span><span class="sxs-lookup"><span data-stu-id="935cc-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="935cc-173">Seit November 2016 wurden verschiedene Änderungen an weiterführenden Azure PowerShell-Inhalten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="935cc-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="935cc-174">Beachten Sie beim Erstellen von Links zu diesen Inhalten aus anderen Artikeln auf der Website „docs.microsoft.com“ die folgenden Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="935cc-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="935cc-175">Struktur der URL:</span><span class="sxs-lookup"><span data-stu-id="935cc-175">Structure of the URL:</span></span>

* <span data-ttu-id="935cc-176">Für Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="935cc-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="935cc-177">Für konzeptionelle Themen:</span><span class="sxs-lookup"><span data-stu-id="935cc-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="935cc-178">Der Teil `<moniker-name>` ist optional.</span><span class="sxs-lookup"><span data-stu-id="935cc-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="935cc-179">Wenn dieser ausgelassen wird, werden Sie zur aktuellen Version des Inhalts weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="935cc-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="935cc-180">Der Teil `<service-name>` ist eines der Beispiele, das in den folgenden Basis-URLs gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="935cc-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="935cc-181">Inhalt von Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="935cc-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="935cc-182">Inhalt von Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="935cc-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="935cc-183">Inhalt von Azure Active Directory PowerShell (Azure AD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="935cc-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="935cc-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="935cc-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="935cc-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="935cc-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="935cc-186">Azure PowerShell für Aufträge für die elastische Datenbank: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="935cc-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="935cc-187">Wenn Sie diese URLs verwenden, werden Sie zur aktuellen Version des Inhalts umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="935cc-187">When you use these URLs, you'll be redirected to the latest version of the content.</span></span> <span data-ttu-id="935cc-188">Auf diese Weise müssen Sie keinen Versionsmoniker angeben.</span><span class="sxs-lookup"><span data-stu-id="935cc-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="935cc-189">Sie müssen bei Versionsänderungen auch keine Links zu konzeptionellen Inhalten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="935cc-189">And, you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="935cc-190">Um den richtigen Link zu erstellen, suchen Sie nach der Seite, für die Sie einen Link in Ihren Browser einfügen möchten, kopieren Sie die URL, und entfernen Sie den Gebietsschemacode, z. B. **en-us**.</span><span class="sxs-lookup"><span data-stu-id="935cc-190">To create the correct link, find the page that you want to link to in your browser, copy the URL, and then remove the locale code, for example, **en-us**.</span></span>

<span data-ttu-id="935cc-191">Beispiel für Markdown:</span><span class="sxs-lookup"><span data-stu-id="935cc-191">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](https://docs.microsoft.com/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](https://docs.microsoft.com/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-azurerm-ps)
```
