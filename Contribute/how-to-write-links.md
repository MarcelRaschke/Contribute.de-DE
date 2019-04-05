---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 464c6b2ae8976252828d73390f9cbeea67f4e3ce
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637550"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="293a2-103">Verwenden von Links in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="293a2-103">Using links in documentation</span></span>
<span data-ttu-id="293a2-104">In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="293a2-105">Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="293a2-106">Benutzer werden über Links auf Inhalte derselben Seite, von benachbarten Seiten oder von externen Websites und URLs verwiesen.</span><span class="sxs-lookup"><span data-stu-id="293a2-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="293a2-107">Das Back-End der Website „docs.microsoft.com“ nutzt Open Publishing Services (OPS). Dadurch wird [CommonMark](https://commonmark.org/)-konformes Markdown unterstützt, das durch die [Markdig](https://github.com/lunet-io/markdig)-Engine analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="293a2-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="293a2-108">Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="293a2-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="293a2-109">Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="293a2-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="293a2-110">Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).</span><span class="sxs-lookup"><span data-stu-id="293a2-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="293a2-111">Linktext</span><span class="sxs-lookup"><span data-stu-id="293a2-111">Link text</span></span>

<span data-ttu-id="293a2-112">Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein.</span><span class="sxs-lookup"><span data-stu-id="293a2-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="293a2-113">Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="293a2-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="293a2-114">Verwenden Sie nicht die Formulierung „Hier klicken“.</span><span class="sxs-lookup"><span data-stu-id="293a2-114">Do not use "click here."</span></span> <span data-ttu-id="293a2-115">Diese ist im Hinblick auf die Suchmaschinenoptimierung suboptimal und beschreibt das Linkziel nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="293a2-115">It's bad for search engine optimization, and doesn't adequately describe the target.</span></span>

<span data-ttu-id="293a2-116">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="293a2-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="293a2-117">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="293a2-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="293a2-118">Links in einem Artikel zum anderen Artikel</span><span class="sxs-lookup"><span data-stu-id="293a2-118">Links from one article to another</span></span>

<span data-ttu-id="293a2-119">Verwenden Sie zum Erstellen eines Inlinelinks in einem technischen Dokumentationsartikel zu einem anderen technischen Dokumentationsartikel innerhalb desselben Dokumentationssatzes die folgende Linksyntax:</span><span class="sxs-lookup"><span data-stu-id="293a2-119">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="293a2-120">Einem Artikel in einem Verzeichnis wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="293a2-120">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="293a2-121">Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel im Stammverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="293a2-121">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="293a2-122">Einem Artikel im Stammverzeichnis wird ein Link in einem Artikel in einem Unterverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="293a2-122">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="293a2-123">Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel in einem anderen Unterverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="293a2-123">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="293a2-124">Einem Artikel wird ein Link zwischen verschiedenen Dokumentationssätzen hinzugefügt (auch wenn sie zum selben Repository gehören):  `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="293a2-124">An article linking across docsets (even if in the same repository):  `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="293a2-125">In keinem der oben stehenden Beispiele wird `~/` als Teil des Links verwendet.</span><span class="sxs-lookup"><span data-stu-id="293a2-125">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="293a2-126">Wenn Sie einen Link zu einem Pfad hinzufügen, der sich am Stamm des Repositorys befindet, beginnen Sie mit `/`.</span><span class="sxs-lookup"><span data-stu-id="293a2-126">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="293a2-127">Wenn Sie ein `~/` einfügen, wird dadurch beim Navigieren in den Quellrepositorys auf GitHub ein ungültiger Link erstellt.</span><span class="sxs-lookup"><span data-stu-id="293a2-127">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="293a2-128">Wenn der Pfad mit `/` beginnt, kann der Link ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-128">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="293a2-129">Links zu Verankerungen</span><span class="sxs-lookup"><span data-stu-id="293a2-129">Links to anchors</span></span>

<span data-ttu-id="293a2-130">Sie müssen keine Anker erstellen.</span><span class="sxs-lookup"><span data-stu-id="293a2-130">You do not have to create anchors.</span></span> <span data-ttu-id="293a2-131">Sie werden automatisch bei der Veröffentlichung aller H2-Überschriften generiert.</span><span class="sxs-lookup"><span data-stu-id="293a2-131">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="293a2-132">Sie müssen lediglich Links zu den H2-Abschnitten erstellen.</span><span class="sxs-lookup"><span data-stu-id="293a2-132">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="293a2-133">So erstellen Sie einen Link zu einer Überschrift im selben Artikel</span><span class="sxs-lookup"><span data-stu-id="293a2-133">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="293a2-134">So erstellen Sie einen Link zu einer Verankerung in einem anderen Artikel desselben Unterverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="293a2-134">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="293a2-135">So erstellen Sie einen Link zu einer Verankerung in einem anderen Dienstunterverzeichnis</span><span class="sxs-lookup"><span data-stu-id="293a2-135">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="293a2-136">Links von Includes</span><span class="sxs-lookup"><span data-stu-id="293a2-136">Links from includes</span></span>

<span data-ttu-id="293a2-137">Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden.</span><span class="sxs-lookup"><span data-stu-id="293a2-137">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="293a2-138">Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="293a2-138">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="293a2-139">Links in Selektoren</span><span class="sxs-lookup"><span data-stu-id="293a2-139">Links in selectors</span></span>

<span data-ttu-id="293a2-140">Ein Selektor ist eine Komponente zum Navigieren, die in einem Dokumentationsartikel als Dropdownliste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="293a2-140">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="293a2-141">Wenn ein Leser einen Wert in der Dropdownliste auswählt, wird der ausgewählte Artikel im Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="293a2-141">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="293a2-142">In der Regel enthält die Selektorliste Links zu Artikeln, die in engem Zusammenhang stehen, z.B. der gleiche Inhalt in mehreren Programmiersprachen oder eine zusammenhängende Reihe von Artikeln.</span><span class="sxs-lookup"><span data-stu-id="293a2-142">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="293a2-143">Wenn Sie in einer Includedatei eingebettete Selektoren verwenden, verwenden Sie folgende Linkstruktur:</span><span class="sxs-lookup"><span data-stu-id="293a2-143">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="293a2-144">Verweislinks</span><span class="sxs-lookup"><span data-stu-id="293a2-144">Reference-style links</span></span>

<span data-ttu-id="293a2-145">Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden.</span><span class="sxs-lookup"><span data-stu-id="293a2-145">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="293a2-146">Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können.</span><span class="sxs-lookup"><span data-stu-id="293a2-146">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="293a2-147">Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:</span><span class="sxs-lookup"><span data-stu-id="293a2-147">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="293a2-148">Inlinetext:</span><span class="sxs-lookup"><span data-stu-id="293a2-148">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="293a2-149">Linkverweise am Ende des Artikels:</span><span class="sxs-lookup"><span data-stu-id="293a2-149">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="293a2-150">Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen.</span><span class="sxs-lookup"><span data-stu-id="293a2-150">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="293a2-151">Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="293a2-151">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="293a2-152">Link zu Seiten außerhalb der technischen Dokumentation</span><span class="sxs-lookup"><span data-stu-id="293a2-152">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="293a2-153">Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen.</span><span class="sxs-lookup"><span data-stu-id="293a2-153">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="293a2-154">Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:</span><span class="sxs-lookup"><span data-stu-id="293a2-154">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="293a2-155">Links zu Websites von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="293a2-155">Links to third-party sites</span></span>

<span data-ttu-id="293a2-156">Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-156">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="293a2-157">Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="293a2-157">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="293a2-158">**Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen.</span><span class="sxs-lookup"><span data-stu-id="293a2-158">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="293a2-159">Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google.</span><span class="sxs-lookup"><span data-stu-id="293a2-159">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="293a2-160">Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.</span><span class="sxs-lookup"><span data-stu-id="293a2-160">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="293a2-161">**Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-161">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="293a2-162">Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="293a2-162">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="293a2-163">**Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="293a2-163">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="293a2-164">**Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="293a2-164">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="293a2-165">Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="293a2-165">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="293a2-166">Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“</span><span class="sxs-lookup"><span data-stu-id="293a2-166">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="293a2-167">**Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="293a2-167">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="293a2-168">Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="293a2-168">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="293a2-169">**Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder „ms.com“-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.</span><span class="sxs-lookup"><span data-stu-id="293a2-169">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="293a2-170">Links zu MSDN oder TechNet</span><span class="sxs-lookup"><span data-stu-id="293a2-170">Links to MSDN or TechNet</span></span>

<span data-ttu-id="293a2-171">Wenn Sie Links zu Websites von MSDN oder TechNet hinzufügen müssen, verwenden Sie den vollständigen Link zum Thema, und entfernen Sie das Sprachgebietsschema „en-us“ im Link.</span><span class="sxs-lookup"><span data-stu-id="293a2-171">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="293a2-172">Link zu weiterführenden Azure PowerShell-Inhalten</span><span class="sxs-lookup"><span data-stu-id="293a2-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="293a2-173">Seit November 2016 wurden verschiedene Änderungen an weiterführenden Azure PowerShell-Inhalten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="293a2-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="293a2-174">Beachten Sie beim Erstellen von Links zu diesen Inhalten aus anderen Artikeln auf der Website „docs.microsoft.com“ die folgenden Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="293a2-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="293a2-175">Struktur der URL:</span><span class="sxs-lookup"><span data-stu-id="293a2-175">Structure of the URL:</span></span>

* <span data-ttu-id="293a2-176">Für Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="293a2-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="293a2-177">Für konzeptionelle Themen:</span><span class="sxs-lookup"><span data-stu-id="293a2-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="293a2-178">Der Teil `<moniker-name>` ist optional.</span><span class="sxs-lookup"><span data-stu-id="293a2-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="293a2-179">Wenn dieser ausgelassen wird, werden Sie zur aktuellen Version des Inhalts weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="293a2-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="293a2-180">Der Teil `<service-name>` ist eines der Beispiele, das in den folgenden Basis-URLs gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="293a2-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="293a2-181">Inhalt von Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="293a2-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="293a2-182">Inhalt von Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="293a2-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="293a2-183">Inhalt von Azure Active Directory PowerShell (Azure AD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="293a2-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="293a2-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="293a2-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="293a2-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="293a2-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="293a2-186">Azure PowerShell für Aufträge für die elastische Datenbank: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="293a2-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="293a2-187">Wenn Sie diese URLs verwenden, werden Sie zur aktuellen Version des Inhalts umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="293a2-187">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="293a2-188">Auf diese Weise müssen Sie keinen Versionsmoniker angeben.</span><span class="sxs-lookup"><span data-stu-id="293a2-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="293a2-189">Sie müssen bei Versionsänderungen auch keine Links zu konzeptionellen Inhalten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="293a2-189">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="293a2-190">Um den richtigen Link zu erstellen, suchen Sie nach der Seite, für die Sie einen Link in Ihren Browser einfügen möchten, und kopieren Sie die URL.</span><span class="sxs-lookup"><span data-stu-id="293a2-190">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="293a2-191">Entfernen Sie dann `https://docs.microsoft.com` und die Gebietsschemainformationen.</span><span class="sxs-lookup"><span data-stu-id="293a2-191">Then, remove  `https://docs.microsoft.com` and the locale info.</span></span>

<span data-ttu-id="293a2-192">Wenn Sie einen Link aus einem Inhaltsverzeichnis hinzufügen, müssen Sie die vollständige URL ohne Gebietsschemaangabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="293a2-192">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="293a2-193">Beispiel für Markdown:</span><span class="sxs-lookup"><span data-stu-id="293a2-193">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
