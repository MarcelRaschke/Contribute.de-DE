---
title: ms-prod-and-service
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 42e6f063c8b3d97386b2655b49a19a3e103d6b3b
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713198"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="318f8-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="318f8-103">ms-prod-and-service</span></span>

<span data-ttu-id="318f8-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="318f8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="318f8-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="318f8-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="318f8-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="318f8-106">Resolution</span></span>

<span data-ttu-id="318f8-107">Entweder `ms.prod` oder `ms.service` ist erforderlich, und nicht beide können vorhanden sein: `ms.prod` wird für lokale Produkte verwendet; `ms.service` wird für Clouddienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="318f8-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="318f8-108">Bestimmen Sie, was für Ihren Artikel geeignet ist, überprüfen Sie, dass der Wert richtig ist, und entfernen Sie das andere Feld.</span><span class="sxs-lookup"><span data-stu-id="318f8-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="318f8-109">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="318f8-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
