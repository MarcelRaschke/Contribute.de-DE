---
title: multiple-values
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 515a8cd76cbd3d9bd117b1d0d59492f4a77bea4c
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236477"
---
# <a name="multiple-values"></a><span data-ttu-id="98474-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="98474-103">multiple-values</span></span>

## <a name="warning"></a><span data-ttu-id="98474-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="98474-104">Warning</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="98474-105">Sie haben mehrere Werte für ein Attribut angegeben, für das nur ein Wert zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="98474-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="98474-106">Attribute, für die nicht mehrere Werte zulässig sind, müssen im einzelwertigen (skalaren) YML-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="98474-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="98474-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="98474-107">Resolution</span></span>

<span data-ttu-id="98474-108">Sie erhalten diesen Vorschlag immer dann, wenn ein mehrwertiges Array für ein einwertiges Attribut verwendet wird, entweder mit mehreren Werten oder einem einzelnen Wert im Array.</span><span class="sxs-lookup"><span data-stu-id="98474-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="98474-109">YML unterstützt die folgenden Arrayformate für mehrwertige Attribute, z.B. `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="98474-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="98474-110">Diese Formate gelten nicht für einwertige Attribute, z.B. `author`.</span><span class="sxs-lookup"><span data-stu-id="98474-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="98474-111">Wenn Sie mehrere Werte angegeben haben, überprüfen Sie die angegebenen Werte, und ermitteln Sie, welche richtig sind.</span><span class="sxs-lookup"><span data-stu-id="98474-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="98474-112">Entfernen Sie andere Werte, und geben Sie den Einzelwert in der gleichen Zeile wie das Attribut ohne Klammern wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="98474-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="98474-113">Wenn Sie ein einwertiges Array verwenden, ändern Sie es in das oben genannte skalare Format.</span><span class="sxs-lookup"><span data-stu-id="98474-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="98474-114">Geltende Attribute</span><span class="sxs-lookup"><span data-stu-id="98474-114">Attributes in scope</span></span>

<span data-ttu-id="98474-115">Die folgenden Attribute müssen einwertig sein:</span><span class="sxs-lookup"><span data-stu-id="98474-115">The following attributes are required to be single-valued:</span></span>

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
