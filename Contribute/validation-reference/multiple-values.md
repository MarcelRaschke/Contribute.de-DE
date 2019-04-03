---
title: multiple-values
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637320"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

Sie haben mehrere Werte für ein Attribut angegeben, für das nur ein Wert zulässig ist.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Attribute, für die nicht mehrere Werte zulässig sind, müssen im einzelwertigen (skalaren) YML-Format angegeben werden.

## <a name="resolution"></a>Lösung

Sie erhalten diesen Vorschlag immer dann, wenn ein mehrwertiges Array für ein einwertiges Attribut verwendet wird, entweder mit mehreren Werten oder einem einzelnen Wert im Array.

YML unterstützt die folgenden Arrayformate für mehrwertige Attribute, z.B. `ms.custom`:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Diese Formate gelten nicht für einwertige Attribute, z.B. `author`.

Wenn Sie mehrere Werte angegeben haben, überprüfen Sie die angegebenen Werte, und ermitteln Sie, welche richtig sind. Entfernen Sie andere Werte, und geben Sie den Einzelwert in der gleichen Zeile wie das Attribut ohne Klammern wie folgt an:

```yml
---
author: meganbradley
---
```

Wenn Sie ein einwertiges Array verwenden, ändern Sie es in das oben genannte skalare Format.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
