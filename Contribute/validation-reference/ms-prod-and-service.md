---
title: ms-prod-and-service
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987673"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="ac81a-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="ac81a-103">ms-prod-and-service</span></span>

<span data-ttu-id="ac81a-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="ac81a-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ac81a-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="ac81a-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="ac81a-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="ac81a-106">Resolution</span></span>

<span data-ttu-id="ac81a-107">Entweder `ms.prod` oder `ms.service` ist erforderlich, und nicht beide können vorhanden sein: `ms.prod` wird für lokale Produkte verwendet; `ms.service` wird für Clouddienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac81a-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="ac81a-108">Bestimmen Sie, was für Ihren Artikel geeignet ist, überprüfen Sie, dass der Wert richtig ist, und entfernen Sie das andere Feld.</span><span class="sxs-lookup"><span data-stu-id="ac81a-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="ac81a-109">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="ac81a-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
