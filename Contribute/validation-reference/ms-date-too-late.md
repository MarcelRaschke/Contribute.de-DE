---
title: ms-date-too-late
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431482"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Bald verfügbar!**

## <a name="warning"></a>Warnung

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Mit dem `ms.date`-Attribut wird „Frische“ signalisiert – d.h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde. Darum kann es nicht in der Zukunft liegen! Fünf Tage sind für die Herausgabezeit zulässig, wenn der Inhalt etwa zur Qualitätssicherung in Vorbereitung auf ein wichtiges Ereignis eingefroren wird.

## <a name="resolution"></a>Lösung

Geben Sie ein `ms.date`, das vom aktuellen Datum nicht mehr als fünf Tage abweicht, im Format MM/TT/JJJJ an:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
