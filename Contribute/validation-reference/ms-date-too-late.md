---
title: ms-date-too-late
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713106"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Bald verfügbar!**

## <a name="warning"></a>Warnung

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Mit dem `ms.date`-Attribut wird „Frische“ signalisiert – d.h., wann der Artikel zuletzt auf Relevanz, Genauigkeit, richtige Screenshots und funktionierende Links überprüft wurde. Darum kann es nicht in der Zukunft liegen! Fünf Tage sind für die Herausgabezeit zulässig, wenn der Inhalt etwa zur Qualitätssicherung in Vorbereitung auf ein wichtiges Ereignis eingefroren wird.

## <a name="resolution"></a>Lösung

Geben Sie ein `ms.date`, das vom aktuellen Datum nicht mehr als fünf Tage abweicht, im Format MM/TT/JJJJ an.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
