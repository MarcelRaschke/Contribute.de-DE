---
title: ms-prod-and-service
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236348"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="af011-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="af011-103">ms-prod-and-service</span></span>

## <a name="warning"></a><span data-ttu-id="af011-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="af011-104">Warning</span></span>
<span data-ttu-id="af011-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span><span class="sxs-lookup"><span data-stu-id="af011-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span></span>

## <a name="resolution"></a><span data-ttu-id="af011-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="af011-106">Resolution</span></span>

<span data-ttu-id="af011-107">Entweder `ms.prod` oder `ms.service` ist erforderlich, und nicht beide können vorhanden sein: `ms.prod` wird für lokale Produkte verwendet; `ms.service` wird für Clouddienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="af011-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="af011-108">Bestimmen Sie, was für Ihren Artikel geeignet ist, überprüfen Sie, dass der Wert richtig ist, und entfernen Sie das andere Feld.</span><span class="sxs-lookup"><span data-stu-id="af011-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="af011-109">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="af011-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="af011-110">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="af011-110">To request new values, follow [this process](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
