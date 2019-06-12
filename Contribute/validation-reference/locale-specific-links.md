---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Gebietsschemaspezifische Links
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841248"
---
# <a name="locale-specific-links"></a><span data-ttu-id="531e3-102">Gebietsschemaspezifische Links</span><span class="sxs-lookup"><span data-stu-id="531e3-102">Locale-specific links</span></span>

<span data-ttu-id="531e3-103">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="531e3-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="531e3-104">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="531e3-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="531e3-105">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="531e3-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="531e3-106">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="531e3-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="531e3-107">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="531e3-107">The following is an example.</span></span>

<span data-ttu-id="531e3-108">Vorher:</span><span class="sxs-lookup"><span data-stu-id="531e3-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="531e3-109">Nachher:</span><span class="sxs-lookup"><span data-stu-id="531e3-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="531e3-110">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="531e3-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="531e3-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="531e3-111">azure.microsoft.com</span></span>
- <span data-ttu-id="531e3-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="531e3-112">docs.microsoft.com</span></span>
- <span data-ttu-id="531e3-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="531e3-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="531e3-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="531e3-114">technet.microsoft.com</span></span>