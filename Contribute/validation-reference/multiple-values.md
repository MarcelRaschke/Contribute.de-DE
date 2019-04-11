---
title: multiple-values
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899657"
---
# <a name="multiple-values"></a><span data-ttu-id="f644a-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="f644a-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f644a-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f644a-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="f644a-105">Sie haben mehrere Werte für ein Attribut angegeben, für das nur ein Wert zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f644a-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="f644a-106">Attribute, für die nicht mehrere Werte zulässig sind, müssen im einzelwertigen (skalaren) YML-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f644a-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="f644a-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="f644a-107">Resolution</span></span>

<span data-ttu-id="f644a-108">Sie erhalten diesen Vorschlag immer dann, wenn ein mehrwertiges Array für ein einwertiges Attribut verwendet wird, entweder mit mehreren Werten oder einem einzelnen Wert im Array.</span><span class="sxs-lookup"><span data-stu-id="f644a-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="f644a-109">YML unterstützt die folgenden Arrayformate für mehrwertige Attribute, z.B. `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="f644a-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="f644a-110">Diese Formate gelten nicht für einwertige Attribute, z.B. `author`.</span><span class="sxs-lookup"><span data-stu-id="f644a-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="f644a-111">Wenn Sie mehrere Werte angegeben haben, überprüfen Sie die angegebenen Werte, und ermitteln Sie, welche richtig sind.</span><span class="sxs-lookup"><span data-stu-id="f644a-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="f644a-112">Entfernen Sie andere Werte, und geben Sie den Einzelwert in der gleichen Zeile wie das Attribut ohne Klammern wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="f644a-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="f644a-113">Wenn Sie ein einwertiges Array verwenden, ändern Sie es in das oben genannte skalare Format.</span><span class="sxs-lookup"><span data-stu-id="f644a-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="f644a-114">Geltende Attribute</span><span class="sxs-lookup"><span data-stu-id="f644a-114">Attributes in scope</span></span>

<span data-ttu-id="f644a-115">Die folgenden Attribute müssen einwertig sein:</span><span class="sxs-lookup"><span data-stu-id="f644a-115">The following attributes are required to be single-valued:</span></span>

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
