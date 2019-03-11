---
title: yaml-header-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – yaml-header-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459025"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Warnung

`Invalid YAML header: Improper use of a colon in a metadata entry.`

In der Regel bedeutet dieser Fehler, dass ein Metadatenwert ohne Anführungszeichen in einem YAML-Header einen Doppelpunkt oder ein anderes Sonderzeichen enthält. Alternativ kann ein Leerzeichen nach dem Doppelpunkt in einem Name/Wert-Paar fehlen.

## <a name="resolution"></a>Lösung

Überprüfen Sie Ihren YAML-Header. Suchen Sie die folgenden Fehlern.

Doppelpunkt in einem Wert ohne Anführungszeichen:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Änderung:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Kein Leerzeichen nach einem Doppelpunkt in einem Name/Wert-Paar:

```yml
---
title:I omitted a space.
---
```

Änderung:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
