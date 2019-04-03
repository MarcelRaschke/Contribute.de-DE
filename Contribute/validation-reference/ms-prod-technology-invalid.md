---
title: ms-prod-and-technology-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636837"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="20e51-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="20e51-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="20e51-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="20e51-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="20e51-105">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="20e51-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="20e51-106">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="20e51-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="20e51-107">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="20e51-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="20e51-108">Entweder ist Ihr `ms.prod`-Wert ungültig, oder Ihr `ms.technology`-Wert bildet mit Ihrem `ms.prod` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="20e51-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="20e51-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="20e51-109">Resolution</span></span>

<span data-ttu-id="20e51-110">Bestätigen Sie, dass Ihr `ms.prod`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="20e51-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="20e51-111">Wählen Sie dann einen gültigen `ms.technology`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="20e51-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="20e51-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="20e51-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
