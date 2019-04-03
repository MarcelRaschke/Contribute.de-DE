---
title: ms-date-too-late
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637389"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="3954c-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="3954c-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="3954c-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="3954c-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="3954c-105">Mit dem `ms.date`-Attribut wird „Frische“ signalisiert – d.h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="3954c-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="3954c-106">Darum kann es nicht in der Zukunft liegen!</span><span class="sxs-lookup"><span data-stu-id="3954c-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="3954c-107">Fünf Tage sind für die Herausgabezeit zulässig, wenn der Inhalt etwa zur Qualitätssicherung in Vorbereitung auf ein wichtiges Ereignis eingefroren wird.</span><span class="sxs-lookup"><span data-stu-id="3954c-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="3954c-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="3954c-108">Resolution</span></span>

<span data-ttu-id="3954c-109">Geben Sie ein `ms.date`, das vom aktuellen Datum nicht mehr als fünf Tage abweicht, im Format MM/TT/JJJJ an:</span><span class="sxs-lookup"><span data-stu-id="3954c-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
