---
title: external-bookmark-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427460"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Warnung

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Sie versuchen, eine Überschrift in einer anderen Datei zu verknüpfen, die nicht vorhanden ist.

## <a name="resolution"></a>Lösung

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Überprüfen Sie die Datei, die Sie verknüpfen, und aktualisieren Sie den Lesezeichenlink, damit dieser auf einen gültigen Abschnitt in der Datei verweist.

Wenn Sie eine Abschnittsüberschrift in einem anderen Artikel verknüpfen möchten, verwenden Sie einen datei- oder websitebezogenen Link und ein Hashsymbol gefolgt von der Überschrift. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche. Dies ist ein Beispiel:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
