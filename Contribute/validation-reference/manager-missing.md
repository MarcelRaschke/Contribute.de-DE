---
title: manager-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637251"
---
# <a name="manager-missing"></a><span data-ttu-id="ac5bc-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="ac5bc-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ac5bc-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="ac5bc-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="ac5bc-105">Für einige Inhaltsgruppen ist das Attribut `manager` erforderlich, um den Manager des Autors zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ac5bc-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac5bc-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="ac5bc-106">Resolution</span></span>

<span data-ttu-id="ac5bc-107">Geben Sie einen gültigen Microsoft-Alias für `manager` an:</span><span class="sxs-lookup"><span data-stu-id="ac5bc-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
