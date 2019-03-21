---
title: ms-prod-and-technology-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987581"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="e080d-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="e080d-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="e080d-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="e080d-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="e080d-105">Warnung</span><span class="sxs-lookup"><span data-stu-id="e080d-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="e080d-106">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="e080d-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="e080d-107">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="e080d-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="e080d-108">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="e080d-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="e080d-109">Entweder ist Ihr `ms.prod`-Wert ungültig, oder Ihr `ms.technology`-Wert bildet mit Ihrem `ms.prod` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="e080d-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="e080d-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="e080d-110">Resolution</span></span>

<span data-ttu-id="e080d-111">Bestätigen Sie, dass Ihr `ms.prod`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="e080d-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="e080d-112">Wählen Sie dann einen gültigen `ms.technology`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e080d-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="e080d-113">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e080d-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
