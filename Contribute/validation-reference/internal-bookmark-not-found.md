---
title: internal-bookmark-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427496"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Current file doesn't contain a bookmark named '{bookmark}'.`

Sie versuchen, in der aktuellen Datei eine Überschrift zu verknüpfen, die nicht vorhanden ist.

## <a name="resolution"></a>Lösung

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Überprüfen Sie die Überschrift, die Sie verknüpfen möchten, und aktualisieren Sie den Link.

Verwenden Sie ein Hashsymbol gefolgt von der Überschrift, um einen Abschnitt im aktuellen Artikel zu verknüpfen. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche. Dies ist ein Beispiel:

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
