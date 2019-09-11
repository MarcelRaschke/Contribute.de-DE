---
title: h1-no-space
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856241"
---
# <a name="h1-no-space"></a>h1-no-space

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

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
