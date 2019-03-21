---
title: ms-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987719"
---
# <a name="ms-service-missing"></a><span data-ttu-id="062ed-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="062ed-103">ms-service-missing</span></span>

<span data-ttu-id="062ed-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="062ed-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="062ed-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="062ed-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="062ed-106">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="062ed-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="062ed-107">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben, aber wenn Sie `ms.subservice` angeben, müssen Sie auch `ms.service` angeben.</span><span class="sxs-lookup"><span data-stu-id="062ed-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="062ed-108">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="062ed-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="062ed-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="062ed-109">Resolution</span></span>

<span data-ttu-id="062ed-110">Bestätigen Sie, dass der `ms.subservice`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="062ed-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="062ed-111">Fügen Sie dann den entsprechenden `ms.service`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.subservice` ist.</span><span class="sxs-lookup"><span data-stu-id="062ed-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="062ed-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="062ed-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
