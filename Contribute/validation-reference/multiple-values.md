---
title: multiple-values
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465114"
---
# <a name="multiple-values"></a><span data-ttu-id="d6094-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="d6094-103">multiple-values</span></span>

<span data-ttu-id="d6094-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="d6094-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d6094-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="d6094-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="d6094-106">Sie haben mehrere Werte für ein Attribut angegeben, für das nur ein Wert zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d6094-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="d6094-107">Attribute, für die nicht mehrere Werte zulässig sind, müssen im einzelwertigen (skalaren) YML-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6094-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="d6094-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="d6094-108">Resolution</span></span>

<span data-ttu-id="d6094-109">Sie erhalten diesen Vorschlag immer dann, wenn ein mehrwertiges Array für ein einwertiges Attribut verwendet wird, entweder mit mehreren Werten oder einem einzelnen Wert im Array.</span><span class="sxs-lookup"><span data-stu-id="d6094-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="d6094-110">YML unterstützt die folgenden Arrayformate für mehrwertige Attribute, z.B. `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="d6094-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="d6094-111">Diese Formate gelten nicht für einwertige Attribute, z.B. `author`.</span><span class="sxs-lookup"><span data-stu-id="d6094-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="d6094-112">Wenn Sie mehrere Werte angegeben haben, überprüfen Sie die angegebenen Werte, und ermitteln Sie, welche richtig sind.</span><span class="sxs-lookup"><span data-stu-id="d6094-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="d6094-113">Entfernen Sie andere Werte, und geben Sie den Einzelwert in der gleichen Zeile wie das Attribut ohne Klammern wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="d6094-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="d6094-114">Wenn Sie ein einwertiges Array verwenden, ändern Sie es in das oben genannte skalare Format.</span><span class="sxs-lookup"><span data-stu-id="d6094-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
