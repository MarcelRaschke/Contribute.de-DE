---
title: internal-bookmark-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856218"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Warnung

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

Sie versuchen, in der aktuellen oder einer anderen Datei eine Überschrift zu verknüpfen, die nicht vorhanden ist.

## <a name="resolution"></a>Lösung

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Überprüfen Sie die Überschrift, die Sie verknüpfen möchten, und aktualisieren Sie den Link.

Verwenden Sie ein Hashsymbol gefolgt von der Überschrift, um einen Abschnitt im aktuellen Artikel zu verknüpfen. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche. Dies ist ein Beispiel:

```markdown
[Managed Disks](#managed-disks)
```

Um eine Verknüpfung mit einer Überschrift in einer anderen Datei herzustellen, verwenden Sie einen relativen Link zu dieser Datei gefolgt von einem Hashsymbol und den Wörtern der Überschrift. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche. Dies ist ein Beispiel:

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
