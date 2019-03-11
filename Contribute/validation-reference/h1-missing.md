---
title: h1-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459117"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Warnung

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
> Diese Regel gilt nicht für eingeschlossene Dateien. Wenn bei eingeschlossenen Dateien H1-Warnungen ausgelöst werden, müssen Sie die eingeschlossenen Dateien wahrscheinlich in einen `includes`-Ordner verschieben. Der `includes`-Ordner kann sich im Dateipfad auf einer beliebigen Ebene befinden. Je nach Pfad wird die Datei bei der Erstellung der Dokumentation als eingeschlossene Datei erkannt, und die H1-Überprüfung wird nicht ausgeführt.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]