---
title: hard-coded-locale
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – hard-coded-locale
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427406"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="c6226-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="c6226-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="c6226-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="c6226-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="c6226-105">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c6226-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="c6226-106">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="c6226-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="c6226-107">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c6226-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="c6226-108">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="c6226-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="c6226-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c6226-109">azure.microsoft.com</span></span>
- <span data-ttu-id="c6226-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c6226-110">docs.microsoft.com</span></span>
- <span data-ttu-id="c6226-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c6226-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="c6226-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c6226-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="c6226-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="c6226-113">Resolution</span></span>

<span data-ttu-id="c6226-114">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="c6226-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="c6226-115">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c6226-115">The following is an example.</span></span>

<span data-ttu-id="c6226-116">Vorher:</span><span class="sxs-lookup"><span data-stu-id="c6226-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="c6226-117">Nachher:</span><span class="sxs-lookup"><span data-stu-id="c6226-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]