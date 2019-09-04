---
title: ms-date-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236260"
---
# <a name="ms-date-missing"></a><span data-ttu-id="9a53f-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="9a53f-103">ms-date-missing</span></span>

## <a name="warning"></a><span data-ttu-id="9a53f-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="9a53f-104">Warning</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="9a53f-105">Für manche Inhaltsgruppen ist es erforderlich, dass das `ms.date`-Attribut „Aktualität“ signalisiert – d. h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="9a53f-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="9a53f-106">Dies ist nicht identisch mit dem Datum, zu dem dieser Artikel zuletzt *veröffentlicht* wurde, das auf der Seite angezeigt wird, wenn `ms.date` nicht explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a53f-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="9a53f-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="9a53f-107">Resolution</span></span>

<span data-ttu-id="9a53f-108">Bestätigen Sie, dass der Artikel ohne Brüche im Inhalt aktuell ist, und fügen Sie ein gültiges Datum im Format MM/TT/JJJJ hinzu:</span><span class="sxs-lookup"><span data-stu-id="9a53f-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
