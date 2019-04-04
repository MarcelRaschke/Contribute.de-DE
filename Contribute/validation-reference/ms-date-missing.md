---
title: ms-date-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637274"
---
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Für manche Inhaltsgruppen ist es erforderlich, dass das `ms.date`-Attribut „Aktualität“ signalisiert – d. h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde. Dies ist nicht identisch mit dem Datum, zu dem dieser Artikel zuletzt *veröffentlicht* wurde, das auf der Seite angezeigt wird, wenn `ms.date` nicht explizit angegeben wird.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass der Artikel ohne Brüche im Inhalt aktuell ist, und fügen Sie ein gültiges Datum im Format MM/TT/JJJJ hinzu:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
