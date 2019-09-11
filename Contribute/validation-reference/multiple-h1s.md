---
title: multiple-h1
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-h1
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848606"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift. Pro Datei kann nur eine H1 vorhanden sein.

## <a name="resolution"></a>Lösung

Ändern Sie nachfolgende H1-Überschriften in H2-Überschriften (`##`), oder strukturieren Sie Ihre Datei um, um das Problem zu beheben. Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu übersprungen (nach H1 darf also nicht H3 folgen).

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]