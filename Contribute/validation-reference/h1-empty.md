---
title: h1-empty
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-empty
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427411"
---
# <a name="h1-empty"></a><span data-ttu-id="cf82e-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="cf82e-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="cf82e-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="cf82e-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="cf82e-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="cf82e-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="cf82e-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf82e-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="cf82e-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="cf82e-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="cf82e-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="cf82e-108">Resolution</span></span>

<span data-ttu-id="cf82e-109">Stellen Sie sicher, dass Ihre H1 Inhalt und nicht nur einen Hash enthält, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="cf82e-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="cf82e-110">Falsch:</span><span class="sxs-lookup"><span data-stu-id="cf82e-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="cf82e-111">Richtig:</span><span class="sxs-lookup"><span data-stu-id="cf82e-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]