---
title: ms-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713083"
---
# <a name="ms-service-missing"></a><span data-ttu-id="1abf4-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="1abf4-103">ms-service-missing</span></span>

<span data-ttu-id="1abf4-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="1abf4-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="1abf4-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="1abf4-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="1abf4-106">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="1abf4-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="1abf4-107">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben, aber wenn Sie `ms.subservice` angeben, müssen Sie auch `ms.service` angeben.</span><span class="sxs-lookup"><span data-stu-id="1abf4-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="1abf4-108">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="1abf4-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="1abf4-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="1abf4-109">Resolution</span></span>

<span data-ttu-id="1abf4-110">Bestätigen Sie, dass der `ms.subservice`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="1abf4-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="1abf4-111">Fügen Sie dann den entsprechenden `ms.service`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.subservice` ist.</span><span class="sxs-lookup"><span data-stu-id="1abf4-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="1abf4-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="1abf4-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
