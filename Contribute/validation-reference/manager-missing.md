---
title: manager-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427489"
---
# <a name="manager-missing"></a>manager-missing

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Für einige Inhaltsgruppen ist das Attribut `manager` erforderlich, um den Manager des Autors zu identifizieren.

## <a name="resolution"></a>Lösung

Geben Sie einen gültigen Microsoft-Alias für `manager` an:

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
