---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653549"
---
# <a name="locale-specific-links"></a><span data-ttu-id="f1811-101">Gebietsschemaspezifische Links</span><span class="sxs-lookup"><span data-stu-id="f1811-101">Locale-specific links</span></span>

<span data-ttu-id="f1811-102">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f1811-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="f1811-103">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="f1811-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="f1811-104">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1811-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="f1811-105">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="f1811-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="f1811-106">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f1811-106">The following is an example.</span></span>

<span data-ttu-id="f1811-107">Vorher:</span><span class="sxs-lookup"><span data-stu-id="f1811-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="f1811-108">Nachher:</span><span class="sxs-lookup"><span data-stu-id="f1811-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="f1811-109">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="f1811-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="f1811-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f1811-110">azure.microsoft.com</span></span>
- <span data-ttu-id="f1811-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f1811-111">docs.microsoft.com</span></span>
- <span data-ttu-id="f1811-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f1811-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="f1811-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f1811-113">technet.microsoft.com</span></span>