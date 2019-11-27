---
title: h1-empty
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-empty
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528812"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Warnung

`H1 is required. Add content to your top-level heading.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.

## <a name="resolution"></a>Lösung

Stellen Sie sicher, dass Ihre H1 Inhalt und nicht nur einen Hash enthält, um das Problem zu beheben.

Falsch:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Richtig:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
