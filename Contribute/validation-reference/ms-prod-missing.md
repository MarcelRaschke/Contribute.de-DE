---
title: ms-prod-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713221"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="0b8d0-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="0b8d0-103">ms-prod-missing</span></span>

<span data-ttu-id="0b8d0-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="0b8d0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0b8d0-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="0b8d0-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="0b8d0-106">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="0b8d0-107">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben, aber wenn Sie `ms.technology` angeben, müssen Sie auch `ms.prod` angeben.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="0b8d0-108">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="0b8d0-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b8d0-109">Resolution</span></span>

<span data-ttu-id="0b8d0-110">Bestätigen Sie, dass der `ms.technology`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="0b8d0-111">Fügen Sie dann den entsprechenden `ms.prod`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.technology` ist.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="0b8d0-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="0b8d0-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
