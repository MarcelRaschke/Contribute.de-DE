---
title: ms-service-and-subservice-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637297"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="e6a72-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="e6a72-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e6a72-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="e6a72-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="e6a72-105">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="e6a72-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="e6a72-106">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="e6a72-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="e6a72-107">Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="e6a72-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="e6a72-108">Entweder ist Ihr `ms.service`-Wert ungültig, oder Ihr `ms.subservice`-Wert bildet mit Ihrem `ms.service` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="e6a72-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="e6a72-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="e6a72-109">Resolution</span></span>

<span data-ttu-id="e6a72-110">Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="e6a72-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="e6a72-111">Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e6a72-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="e6a72-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e6a72-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
