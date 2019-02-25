---
title: ms-date-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431459"
---
# <a name="ms-date-missing"></a><span data-ttu-id="5e5e7-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="5e5e7-103">ms-date-missing</span></span>

<span data-ttu-id="5e5e7-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="5e5e7-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5e5e7-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="5e5e7-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="5e5e7-106">Mit diesem Datum wird „Frische“ signalisiert – d.h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="5e5e7-107">Dies ist nicht identisch mit dem Datum, zu dem dieser Artikel zuletzt *veröffentlicht* wurde, das auf der Seite angezeigt wird, wenn `ms.date` nicht explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="5e5e7-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="5e5e7-108">Resolution</span></span>

<span data-ttu-id="5e5e7-109">Bestätigen Sie, dass der Artikel ohne Brüche im Inhalt aktuell ist, und fügen Sie ein gültiges Datum im Format MM/TT/JJJJ hinzu:</span><span class="sxs-lookup"><span data-stu-id="5e5e7-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
