---
title: hard-coded-locale
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – hard-coded-locale
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310327"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="d3010-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="d3010-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="d3010-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="d3010-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="d3010-105">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="d3010-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="d3010-106">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="d3010-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="d3010-107">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d3010-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="d3010-108">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="d3010-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="d3010-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3010-109">azure.microsoft.com</span></span>
- <span data-ttu-id="d3010-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3010-110">docs.microsoft.com</span></span>
- <span data-ttu-id="d3010-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3010-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="d3010-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3010-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="d3010-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="d3010-113">Resolution</span></span>

<span data-ttu-id="d3010-114">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="d3010-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="d3010-115">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d3010-115">The following is an example.</span></span>

<span data-ttu-id="d3010-116">Vorher:</span><span class="sxs-lookup"><span data-stu-id="d3010-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="d3010-117">Nachher:</span><span class="sxs-lookup"><span data-stu-id="d3010-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="d3010-118">Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links.</span><span class="sxs-lookup"><span data-stu-id="d3010-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="d3010-119">Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3010-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="d3010-120">So führen Sie das Skript aus:</span><span class="sxs-lookup"><span data-stu-id="d3010-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="d3010-121">Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="d3010-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="d3010-122">Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d3010-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="d3010-123">Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.</span><span class="sxs-lookup"><span data-stu-id="d3010-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]