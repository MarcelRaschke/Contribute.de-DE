---
title: ms-prod-or-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 93351fa343603a0b9d60e4b3e3ae41ce90d9912e
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236277"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="c1ccf-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="c1ccf-103">ms-prod-or-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="c1ccf-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="c1ccf-104">Warning</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="c1ccf-105">Lösung</span><span class="sxs-lookup"><span data-stu-id="c1ccf-105">Resolution</span></span>

<span data-ttu-id="c1ccf-106">Entweder `ms.prod` oder `ms.service` ist erforderlich, und nicht beide können vorhanden sein: `ms.prod` wird für lokale Produkte verwendet; `ms.service` wird für Clouddienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1ccf-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="c1ccf-107">Bestimmen Sie, was für Ihren Artikel geeignet ist, überprüfen Sie, dass der Wert richtig ist, und entfernen Sie das andere Feld.</span><span class="sxs-lookup"><span data-stu-id="c1ccf-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="c1ccf-108">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="c1ccf-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="c1ccf-109">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c1ccf-109">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
