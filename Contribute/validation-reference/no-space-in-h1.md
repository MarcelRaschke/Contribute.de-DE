---
title: no-space-in-h1
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – no-space-in-h1
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427501"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Warnung

`A space is required after the hash (#) in H1.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift. Wenn Sie nach einem Hash kein Leerzeichen einfügen, erkennt die Dokumentation eine H1 nicht.

## <a name="resolution"></a>Lösung

Fügen Sie in Ihrer H1 ein Leerzeichen nach dem Hash hinzu, um dieses Problem zu beheben.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]