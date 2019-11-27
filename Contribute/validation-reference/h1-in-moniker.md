---
title: h1-in-moniker
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-in-moniker
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528828"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

## <a name="warning"></a>Warnung

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift. Pro Datei kann nur eine H1 vorhanden sein. H1-Elemente sind in Monikerabschnitten nicht erlaubt, da H1-Elemente in Monikern je nach Konfiguration der Versionierung leicht zu doppelten oder fehlenden H1-Elementen führen können.

Möglicherweise erhalten Sie diese Meldung auch, wenn Ihr Monikerabschnitt eine Zeile mit Gleichheitszeichen enthält, die einen doppelten Unterstrich wie folgt macht: `=======`. Dies ist eine alternative Markdownsyntax für eine H1. Es ist auch häufig in Mergekonflikten zu sehen:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Lösung

Entfernen Sie H1-Elemente aus allen Monikerabschnitten, und stellen Sie sicher, dass das H1-Element oben im Artikel für alle Monikerabschnitte geeignet ist, um dieses Problem zu beheben. Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu überspringen (nach H1 darf also nicht H3 folgen).

Wenn es sich bei einer H1 in einem Monikerabschnitt tatsächlich um einen doppelten Unterstrich (`=======`) handelt, entfernen oder ersetzen Sie ihn wie jeweils anwendbar durch eine Hashtagüberschrift wie beispielsweise `##`. Wenn der doppelte Unterstrich Teil eines Mergekonflikts ist, entfernen Sie auch die Anfangs- und Endmarker des Mergekonflikts und den veralteten Text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
