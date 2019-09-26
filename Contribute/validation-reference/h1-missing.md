---
title: h1-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247410"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 bezieht sich auf die erste Überschrift in einer Markdowndatei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt. Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.

## <a name="resolution"></a>Lösung

Fügen Sie eine H1 als ersten Inhalt nach dem YML-Metadatenblock in Ihrer Datei hinzu, um dieses Problem zu beheben:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Diese Regel gilt nicht für eingeschlossene Dateien. Wenn für eingeschlossene Dateien H1-Ergebnisse ausgelöst werden, müssen Sie die eingeschlossenen Dateien wahrscheinlich in einen `includes`-Ordner verschieben. Der `includes`-Ordner kann sich im Dateipfad auf einer beliebigen Ebene befinden. Je nach Pfad wird die Datei bei der Erstellung der Dokumentation als eingeschlossene Datei erkannt, und die H1-Überprüfung wird nicht ausgeführt.
>
> Eine häufige Ursache für fehlende H1-Elemente in übergeordneten Dateien ist eine falsche Verwendung der eingeschlossenen Dateien: die H1 befindet sich in der eingeschlossenen Datei, nicht in der übergeordneten Datei. Dies ist unzulässig, weil die Verwendung einer H1 in einer eingeschlossenen Datei entweder bedeutet, dass doppelte H1s in übergeordneten Dateien vorhanden sind oder die eingeschlossene Datei nur einmalig verwendet wird. H1-Elemente müssen innerhalb eines Inhaltssatzes eindeutig sein, und eingeschlossene Dateien sollten nur verwendet werden, um Inhalte in mehreren Dateien gemeinsam zu verwenden. Wenn Sie `h1-missing`-Ergebnisse erhalten, weil die H1 in einer eingeschlossenen Datei enthalten ist, muss als Lösung die H1 in die übergeordnete Datei verschoben werden – und der gesamte eingeschlossene Inhalt, wenn die eingeschlossene Datei nur einmalig verwendet wird. Weitere Informationen zu eingeschlossenen Dateien in der Dokumentation finden Sie im Microsoft-internen Artikel [Einschließen wiederverwendbarer Inhalte in Artikeln](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
