---
title: ms-prod-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987696"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="fc284-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="fc284-103">ms-prod-missing</span></span>

<span data-ttu-id="fc284-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="fc284-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="fc284-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="fc284-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="fc284-106">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="fc284-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="fc284-107">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben, aber wenn Sie `ms.technology` angeben, müssen Sie auch `ms.prod` angeben.</span><span class="sxs-lookup"><span data-stu-id="fc284-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="fc284-108">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="fc284-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="fc284-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="fc284-109">Resolution</span></span>

<span data-ttu-id="fc284-110">Bestätigen Sie, dass der `ms.technology`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="fc284-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="fc284-111">Fügen Sie dann den entsprechenden `ms.prod`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.technology` ist.</span><span class="sxs-lookup"><span data-stu-id="fc284-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="fc284-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="fc284-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
