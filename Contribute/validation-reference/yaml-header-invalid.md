---
title: yaml-header-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – yaml-header-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459025"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="1fabd-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="1fabd-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="1fabd-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="1fabd-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="1fabd-105">In der Regel bedeutet dieser Fehler, dass ein Metadatenwert ohne Anführungszeichen in einem YAML-Header einen Doppelpunkt oder ein anderes Sonderzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="1fabd-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="1fabd-106">Alternativ kann ein Leerzeichen nach dem Doppelpunkt in einem Name/Wert-Paar fehlen.</span><span class="sxs-lookup"><span data-stu-id="1fabd-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="1fabd-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="1fabd-107">Resolution</span></span>

<span data-ttu-id="1fabd-108">Überprüfen Sie Ihren YAML-Header.</span><span class="sxs-lookup"><span data-stu-id="1fabd-108">Review your YAML header.</span></span> <span data-ttu-id="1fabd-109">Suchen Sie die folgenden Fehlern.</span><span class="sxs-lookup"><span data-stu-id="1fabd-109">Look for the following mistakes.</span></span>

<span data-ttu-id="1fabd-110">Doppelpunkt in einem Wert ohne Anführungszeichen:</span><span class="sxs-lookup"><span data-stu-id="1fabd-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="1fabd-111">Änderung:</span><span class="sxs-lookup"><span data-stu-id="1fabd-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="1fabd-112">Kein Leerzeichen nach einem Doppelpunkt in einem Name/Wert-Paar:</span><span class="sxs-lookup"><span data-stu-id="1fabd-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="1fabd-113">Änderung:</span><span class="sxs-lookup"><span data-stu-id="1fabd-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
