---
title: ms-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236501"
---
# <a name="ms-service-missing"></a><span data-ttu-id="64972-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="64972-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="64972-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="64972-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="64972-105">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="64972-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="64972-106">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben, aber wenn Sie `ms.subservice` angeben, müssen Sie auch `ms.service` angeben.</span><span class="sxs-lookup"><span data-stu-id="64972-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="64972-107">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="64972-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="64972-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="64972-108">Resolution</span></span>

<span data-ttu-id="64972-109">Bestätigen Sie, dass der `ms.subservice`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="64972-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="64972-110">Fügen Sie dann den entsprechenden `ms.service`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.subservice` ist.</span><span class="sxs-lookup"><span data-stu-id="64972-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="64972-111">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="64972-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="64972-112">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="64972-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
