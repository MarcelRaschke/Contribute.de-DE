---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636791"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="9769b-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="9769b-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9769b-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="9769b-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="9769b-105">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte, `ms.service` für Clouddienste.</span><span class="sxs-lookup"><span data-stu-id="9769b-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="9769b-106">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="9769b-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="9769b-107">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="9769b-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="9769b-108">Sie können nicht `ms.prod` mit `ms.subservice` oder `ms.service` mit `ms.technology` verwenden.</span><span class="sxs-lookup"><span data-stu-id="9769b-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="9769b-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="9769b-109">Resolution</span></span>

<span data-ttu-id="9769b-110">Überprüfen Sie zuerst, ob Sie das richtige übergeordnete Attribut (`ms.prod` oder `ms.service`) für Ihren Artikel ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="9769b-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="9769b-111">Fügen Sie dann das entsprechende untergeordnete Feld mit einem gültigen gepaarten Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="9769b-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="9769b-112">Entfernen Sie ggf. zusätzliche Felder.</span><span class="sxs-lookup"><span data-stu-id="9769b-112">Remove any extra fields.</span></span>

<span data-ttu-id="9769b-113">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="9769b-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
