---
title: ms-service-and-subservice-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987637"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="1869a-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="1869a-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="1869a-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="1869a-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="1869a-105">Warnung</span><span class="sxs-lookup"><span data-stu-id="1869a-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="1869a-106">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="1869a-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="1869a-107">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="1869a-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="1869a-108">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="1869a-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="1869a-109">Entweder ist Ihr `ms.service`-Wert ungültig, oder Ihr `ms.subservice`-Wert bildet mit Ihrem `ms.service` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="1869a-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="1869a-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="1869a-110">Resolution</span></span>

<span data-ttu-id="1869a-111">Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="1869a-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="1869a-112">Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1869a-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="1869a-113">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="1869a-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
