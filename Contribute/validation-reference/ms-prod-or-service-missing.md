---
title: ms-prod-or-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987558"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="b53a3-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="b53a3-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="b53a3-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="b53a3-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b53a3-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="b53a3-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="b53a3-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="b53a3-106">Resolution</span></span>

<span data-ttu-id="b53a3-107">Entweder `ms.prod` oder `ms.service` ist erforderlich, und nicht beide können vorhanden sein: `ms.prod` wird für lokale Produkte verwendet; `ms.service` wird für Clouddienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="b53a3-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="b53a3-108">Bestimmen Sie, was für Ihren Artikel geeignet ist, überprüfen Sie, dass der Wert richtig ist, und entfernen Sie das andere Feld.</span><span class="sxs-lookup"><span data-stu-id="b53a3-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="b53a3-109">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b53a3-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]