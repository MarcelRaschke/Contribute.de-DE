---
title: hard-coded-locale
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – hard-coded-locale
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166834"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="dd67f-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="dd67f-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd67f-104">Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="dd67f-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="dd67f-105">**Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .</span><span class="sxs-lookup"><span data-stu-id="dd67f-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="dd67f-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="dd67f-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="dd67f-107">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="dd67f-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="dd67f-108">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="dd67f-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="dd67f-109">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dd67f-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="dd67f-110">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="dd67f-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="dd67f-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="dd67f-111">azure.microsoft.com</span></span>
- <span data-ttu-id="dd67f-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="dd67f-112">docs.microsoft.com</span></span>
- <span data-ttu-id="dd67f-113">msdn.microsoft.com (ausgenommen social.msdn.com, wofür das Gebietsschema nötig ist, um sicherzustellen, dass das richtige Forum verknüpft ist)</span><span class="sxs-lookup"><span data-stu-id="dd67f-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="dd67f-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="dd67f-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="dd67f-115">Lösung</span><span class="sxs-lookup"><span data-stu-id="dd67f-115">Resolution</span></span>

<span data-ttu-id="dd67f-116">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="dd67f-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="dd67f-117">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dd67f-117">The following is an example.</span></span>

<span data-ttu-id="dd67f-118">Vorher:</span><span class="sxs-lookup"><span data-stu-id="dd67f-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="dd67f-119">Nachher:</span><span class="sxs-lookup"><span data-stu-id="dd67f-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="dd67f-120">Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links.</span><span class="sxs-lookup"><span data-stu-id="dd67f-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="dd67f-121">Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd67f-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="dd67f-122">So führen Sie das Skript aus:</span><span class="sxs-lookup"><span data-stu-id="dd67f-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="dd67f-123">Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="dd67f-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="dd67f-124">Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd67f-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="dd67f-125">Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.</span><span class="sxs-lookup"><span data-stu-id="dd67f-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
