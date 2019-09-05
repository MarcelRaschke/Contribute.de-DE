---
title: ms-prod-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236322"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="d7610-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="d7610-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="d7610-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="d7610-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="d7610-105">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="d7610-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="d7610-106">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben, aber wenn Sie `ms.technology` angeben, müssen Sie auch `ms.prod` angeben.</span><span class="sxs-lookup"><span data-stu-id="d7610-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="d7610-107">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="d7610-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="d7610-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="d7610-108">Resolution</span></span>

<span data-ttu-id="d7610-109">Bestätigen Sie, dass der `ms.technology`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="d7610-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="d7610-110">Fügen Sie dann den entsprechenden `ms.prod`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.technology` ist.</span><span class="sxs-lookup"><span data-stu-id="d7610-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="d7610-111">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="d7610-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="d7610-112">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="d7610-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
