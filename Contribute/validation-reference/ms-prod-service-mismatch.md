---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987613"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="5acc9-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="5acc9-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="5acc9-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="5acc9-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5acc9-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="5acc9-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="5acc9-106">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte, `ms.service` für Clouddienste.</span><span class="sxs-lookup"><span data-stu-id="5acc9-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="5acc9-107">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="5acc9-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="5acc9-108">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="5acc9-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="5acc9-109">Sie können nicht `ms.prod` mit `ms.subservice` oder `ms.service` mit `ms.technology` verwenden.</span><span class="sxs-lookup"><span data-stu-id="5acc9-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="5acc9-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="5acc9-110">Resolution</span></span>

<span data-ttu-id="5acc9-111">Überprüfen Sie zuerst, ob Sie das richtige übergeordnete Attribut (`ms.prod` oder `ms.service`) für Ihren Artikel ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="5acc9-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="5acc9-112">Fügen Sie dann das entsprechende untergeordnete Feld mit einem gültigen gepaarten Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="5acc9-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="5acc9-113">Entfernen Sie ggf. zusätzliche Felder.</span><span class="sxs-lookup"><span data-stu-id="5acc9-113">Remove any extra fields.</span></span>

<span data-ttu-id="5acc9-114">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="5acc9-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
