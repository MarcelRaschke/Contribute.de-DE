---
title: multiple-h1s
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-h1s
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528944"
---
# <a name="multiple-h1s"></a>multiple-h1s

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift. Pro Datei kann nur eine H1 vorhanden sein.

Möglicherweise erhalten Sie diese Meldung auch, wenn Ihr Artikel eine Zeile mit Gleichheitszeichen enthält, die einen doppelten Unterstrich wie folgt macht: `=======`. Dies ist eine alternative Markdownsyntax für eine H1. Es ist auch häufig in Mergekonflikten zu sehen:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Lösung

Ändern Sie nachfolgende H1-Überschriften in H2-Überschriften (`##`), oder strukturieren Sie Ihre Datei um, um das Problem zu beheben. Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu überspringen (nach H1 darf also nicht H3 folgen).

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

Wenn es sich bei einer zusätzlichen H1 tatsächlich um einen doppelten Unterstrich (`=======`) handelt, entfernen, oder ersetzen Sie ihn wie jeweils anwendbar durch eine Hashtagüberschrift wie beispielsweise `##`. Wenn der doppelte Unterstrich Teil eines Mergekonflikts ist, entfernen Sie auch die Anfangs- und Endmarker des Mergekonflikts und den veralteten Text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
