---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713175"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="6cc2e-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="6cc2e-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="6cc2e-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="6cc2e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6cc2e-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="6cc2e-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="6cc2e-106">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte, `ms.service` für Clouddienste.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="6cc2e-107">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="6cc2e-108">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="6cc2e-109">Sie können nicht `ms.prod` mit `ms.subservice` oder `ms.service` mit `ms.technology` verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="6cc2e-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="6cc2e-110">Resolution</span></span>

<span data-ttu-id="6cc2e-111">Überprüfen Sie zuerst, ob Sie das richtige übergeordnete Attribut (`ms.prod` oder `ms.service`) für Ihren Artikel ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="6cc2e-112">Fügen Sie dann das entsprechende untergeordnete Feld mit einem gültigen gepaarten Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="6cc2e-113">Entfernen Sie ggf. zusätzliche Felder.</span><span class="sxs-lookup"><span data-stu-id="6cc2e-113">Remove any extra fields.</span></span>

<span data-ttu-id="6cc2e-114">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="6cc2e-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
