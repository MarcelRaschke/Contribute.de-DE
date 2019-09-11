---
title: h1-empty
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-empty
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 691d72a3aee9204ba3fe55a398e954c7719f3680
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848555"
---
# <a name="h1-empty"></a><span data-ttu-id="37c01-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="37c01-103">h1-empty</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="37c01-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="37c01-104">Suggestion</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="37c01-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="37c01-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="37c01-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37c01-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="37c01-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="37c01-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="37c01-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="37c01-108">Resolution</span></span>

<span data-ttu-id="37c01-109">Stellen Sie sicher, dass Ihre H1 Inhalt und nicht nur einen Hash enthält, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="37c01-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="37c01-110">Falsch:</span><span class="sxs-lookup"><span data-stu-id="37c01-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="37c01-111">Richtig:</span><span class="sxs-lookup"><span data-stu-id="37c01-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]