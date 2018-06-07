---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469530"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="e4241-103">Verwenden von Links in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e4241-103">Using links in documentation</span></span>
<span data-ttu-id="e4241-104">In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="e4241-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="e4241-105">Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e4241-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="e4241-106">Benutzer werden über Links auf Inhalte derselben Seite, von benachbarten Seiten oder von externen Websites und URLs verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e4241-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="e4241-107">Das Back-End der docs.microsoft.com-Website verwendet Open Publishing Services (OPS), worin DocFX Flavored Markdown (DFM) implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e4241-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="e4241-108">DFM weist eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) auf und verfügt durch Markdownerweiterungen über zusätzliche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e4241-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4241-109">Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).</span><span class="sxs-lookup"><span data-stu-id="e4241-109">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="e4241-110">Linktext</span><span class="sxs-lookup"><span data-stu-id="e4241-110">Link text</span></span>

<span data-ttu-id="e4241-111">Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein.</span><span class="sxs-lookup"><span data-stu-id="e4241-111">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="e4241-112">Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="e4241-112">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4241-113">Verwenden Sie nicht die Formulierung „Hier klicken“.</span><span class="sxs-lookup"><span data-stu-id="e4241-113">Do not use "click here."</span></span> <span data-ttu-id="e4241-114">Diese ist im Hinblick auf die SEO suboptimal und beschreibt das Linkziel nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="e4241-114">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="e4241-115">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="e4241-115">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="e4241-116">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="e4241-116">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="e4241-117">Links in einem Artikel zum anderen Artikel</span><span class="sxs-lookup"><span data-stu-id="e4241-117">Links from one article to another</span></span>

<span data-ttu-id="e4241-118">Verwenden Sie zum Erstellen eines Inlinelinks in einem technischen Dokumentationsartikel zu einem anderen technischen Dokumentationsartikel innerhalb desselben Dokumentationssatzes die folgende Linksyntax:</span><span class="sxs-lookup"><span data-stu-id="e4241-118">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="e4241-119">Einem Artikel in einem Verzeichnis wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e4241-119">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="e4241-120">Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel im Stammverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e4241-120">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="e4241-121">Einem Artikel im Stammverzeichnis wird ein Link in einem Artikel in einem Unterverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e4241-121">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="e4241-122">Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel in einem anderen Unterverzeichnis hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e4241-122">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="e4241-123">Einem Artikel wird ein Link zwischen verschiedenen Dokumentationssätzen hinzugefügt (auch wenn sie zum selben Repository gehören): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="e4241-123">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="e4241-124">Links zu Verankerungen</span><span class="sxs-lookup"><span data-stu-id="e4241-124">Links to anchors</span></span>

<span data-ttu-id="e4241-125">Sie müssen keine Anker erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4241-125">You do not have to create anchors.</span></span> <span data-ttu-id="e4241-126">Sie werden automatisch bei der Veröffentlichung aller H2-Überschriften generiert.</span><span class="sxs-lookup"><span data-stu-id="e4241-126">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="e4241-127">Sie müssen lediglich Links zu den H2-Abschnitten erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4241-127">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="e4241-128">So erstellen Sie einen Link zu einer Überschrift im selben Artikel</span><span class="sxs-lookup"><span data-stu-id="e4241-128">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="e4241-129">So erstellen Sie einen Link zu einer Verankerung in einem anderen Artikel desselben Unterverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="e4241-129">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="e4241-130">So erstellen Sie einen Link zu einer Verankerung in einem anderen Dienstunterverzeichnis</span><span class="sxs-lookup"><span data-stu-id="e4241-130">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="e4241-131">Links von Includes</span><span class="sxs-lookup"><span data-stu-id="e4241-131">Links from includes</span></span>

<span data-ttu-id="e4241-132">Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4241-132">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="e4241-133">Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="e4241-133">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="e4241-134">Links in Selektoren</span><span class="sxs-lookup"><span data-stu-id="e4241-134">Links in selectors</span></span>

<span data-ttu-id="e4241-135">Wenn Sie in einer include-Datei eingebettete Selektoren verwenden, wie es beim Azure-Dokumentationsteam der Fall ist, verwenden Sie folgende Linkstruktur:</span><span class="sxs-lookup"><span data-stu-id="e4241-135">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="e4241-136">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="e4241-136">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="e4241-137">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="e4241-137">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="e4241-138">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="e4241-138">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="e4241-139">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="e4241-139">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="e4241-140">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="e4241-140">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="e4241-141">Verweislinks</span><span class="sxs-lookup"><span data-stu-id="e4241-141">Reference-style links</span></span>

<span data-ttu-id="e4241-142">Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4241-142">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="e4241-143">Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können.</span><span class="sxs-lookup"><span data-stu-id="e4241-143">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="e4241-144">Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:</span><span class="sxs-lookup"><span data-stu-id="e4241-144">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="e4241-145">Inlinetext:</span><span class="sxs-lookup"><span data-stu-id="e4241-145">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="e4241-146">Linkverweise am Ende des Artikels:</span><span class="sxs-lookup"><span data-stu-id="e4241-146">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="e4241-147">Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen.</span><span class="sxs-lookup"><span data-stu-id="e4241-147">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="e4241-148">Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="e4241-148">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="e4241-149">Link zu Seiten außerhalb der technischen Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e4241-149">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="e4241-150">Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen.</span><span class="sxs-lookup"><span data-stu-id="e4241-150">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="e4241-151">Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:</span><span class="sxs-lookup"><span data-stu-id="e4241-151">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="e4241-152">Links zu Websites von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="e4241-152">Links to third-party sites</span></span>

<span data-ttu-id="e4241-153">Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="e4241-153">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="e4241-154">Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="e4241-154">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="e4241-155">**Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen.</span><span class="sxs-lookup"><span data-stu-id="e4241-155">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="e4241-156">Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google.</span><span class="sxs-lookup"><span data-stu-id="e4241-156">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="e4241-157">Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.</span><span class="sxs-lookup"><span data-stu-id="e4241-157">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="e4241-158">**Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e4241-158">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="e4241-159">Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="e4241-159">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="e4241-160">**Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e4241-160">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="e4241-161">**Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="e4241-161">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="e4241-162">Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4241-162">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="e4241-163">Zum Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“</span><span class="sxs-lookup"><span data-stu-id="e4241-163">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="e4241-164">**Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4241-164">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="e4241-165">Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="e4241-165">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="e4241-166">**Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder „ms.com“-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.</span><span class="sxs-lookup"><span data-stu-id="e4241-166">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="e4241-167">Links zu MSDN oder TechNet</span><span class="sxs-lookup"><span data-stu-id="e4241-167">Links to MSDN or TechNet</span></span>

<span data-ttu-id="e4241-168">Wenn Sie Links zu Websites von MSDN oder TechNet hinzufügen müssen, verwenden Sie den vollständigen Link zum Thema, und entfernen Sie das Sprachgebietsschema „en-us“ im Link.</span><span class="sxs-lookup"><span data-stu-id="e4241-168">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="e4241-169">Link zu weiterführenden Azure PowerShell-Inhalten</span><span class="sxs-lookup"><span data-stu-id="e4241-169">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="e4241-170">Seit November 2016 wurden verschiedene Änderungen an weiterführenden Azure PowerShell-Inhalten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="e4241-170">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="e4241-171">Beachten Sie beim Erstellen von Links zu diesen Inhalten aus anderen Artikeln auf der Website „docs.microsoft.com“ die folgenden Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="e4241-171">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="e4241-172">Struktur der URL:</span><span class="sxs-lookup"><span data-stu-id="e4241-172">Structure of the URL:</span></span>

* <span data-ttu-id="e4241-173">Für Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e4241-173">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="e4241-174">Für konzeptionelle Themen:</span><span class="sxs-lookup"><span data-stu-id="e4241-174">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="e4241-175">Der Teil &lt;moniker-name&gt; ist optional.</span><span class="sxs-lookup"><span data-stu-id="e4241-175">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="e4241-176">Wenn dieser ausgelassen wird, werden Sie zur aktuellen Version des Inhalts weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4241-176">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="e4241-177">Der Teil &lt;service-name&gt; ist eines der Beispiele, das in den folgenden Basis-URLs gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="e4241-177">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="e4241-178">Inhalt von Azure PowerShell (AzureRM): https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="e4241-178">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="e4241-179">Inhalt von Azure PowerShell (ASM): https://docs.microsoft.com/powershell/azure/ _servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="e4241-179">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="e4241-180">Inhalt von Azure Active Directory-PowerShell (Azure AD): https://docs.microsoft.com/powershell/azure/ _active-directory_</span><span class="sxs-lookup"><span data-stu-id="e4241-180">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="e4241-181">Azure Service Fabric-PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="e4241-181">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="e4241-182">Azure Information Protection-PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="e4241-182">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="e4241-183">Azure PowerShell für Aufträge für die elastische Datenbank: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="e4241-183">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="e4241-184">Wenn Sie diese URLs verwenden, werden Sie zur aktuellen Version des Inhalts umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4241-184">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="e4241-185">Auf diese Weise müssen Sie keinen Versionsmoniker angeben.</span><span class="sxs-lookup"><span data-stu-id="e4241-185">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="e4241-186">Sie müssen bei Versionsänderungen auch keine Links zu konzeptionellen Inhalten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4241-186">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="e4241-187">Um den richtigen Link zu erstellen, suchen Sie nach der Seite, für die Sie einen Link in Ihren Browser einfügen möchten, und kopieren Sie die URL.</span><span class="sxs-lookup"><span data-stu-id="e4241-187">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="e4241-188">Entfernen Sie dann „https://docs.microsoft.com“ und die Gebietsschemainformationen.</span><span class="sxs-lookup"><span data-stu-id="e4241-188">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="e4241-189">Wenn Sie einen Link aus einem Inhaltsverzeichnis hinzufügen, müssen Sie die vollständige URL ohne Gebietsschemaangabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4241-189">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="e4241-190">Beispiel für Markdown:</span><span class="sxs-lookup"><span data-stu-id="e4241-190">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
