---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288499"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Warnung

`Missing attribute: author. Add the current author's GitHub ID.`

Das `author`-Attribut identifiziert den Autor des Artikels durch die GitHub-ID. 

## <a name="resolution"></a>Lösung

Fügen Sie die GitHub-ID des aktuellen Autors dem YML-Header hinzu:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Falls sich der Besitzer geändert hat, muss dies der *aktuelle* Besitzer des Artikels sein und nicht der ursprüngliche Autor.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
