---
title: h1-in-moniker
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-in-moniker
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246358"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

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
