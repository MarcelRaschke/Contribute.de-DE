---
title: ms-prod-and-technology-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236344"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="af080-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="af080-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="af080-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="af080-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="af080-105">Verwenden Sie `ms.prod` zur Angabe lokaler Produkte.</span><span class="sxs-lookup"><span data-stu-id="af080-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="af080-106">Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben.</span><span class="sxs-lookup"><span data-stu-id="af080-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="af080-107">Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.</span><span class="sxs-lookup"><span data-stu-id="af080-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="af080-108">Entweder ist Ihr `ms.prod`-Wert ungültig, oder Ihr `ms.technology`-Wert bildet mit Ihrem `ms.prod` kein gültiges Paar.</span><span class="sxs-lookup"><span data-stu-id="af080-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="af080-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="af080-109">Resolution</span></span>

<span data-ttu-id="af080-110">Bestätigen Sie, dass Ihr `ms.prod`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="af080-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="af080-111">Wählen Sie dann einen gültigen `ms.technology`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="af080-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="af080-112">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="af080-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="af080-113">[Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="af080-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
