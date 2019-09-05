---
title: ms-service-and-subservice-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236511"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="300fd-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="300fd-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="300fd-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="300fd-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="300fd-105">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="300fd-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="300fd-106">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="300fd-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="300fd-107">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="300fd-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="300fd-108">Entweder ist Ihr `ms.service`-Wert ungültig, oder Ihr `ms.subservice`-Wert bildet mit Ihrem `ms.service` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="300fd-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="300fd-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="300fd-109">Resolution</span></span>

<span data-ttu-id="300fd-110">Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="300fd-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="300fd-111">Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="300fd-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="300fd-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="300fd-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="300fd-113">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="300fd-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
