---
title: h1-no-space
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528958"
---
# <a name="h1-no-space"></a><span data-ttu-id="2bb33-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="2bb33-103">h1-no-space</span></span>

## <a name="warning"></a><span data-ttu-id="2bb33-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="2bb33-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="2bb33-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="2bb33-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="2bb33-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2bb33-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="2bb33-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="2bb33-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="2bb33-108">Wenn Sie nach einem Hash kein Leerzeichen einfügen, erkennt die Dokumentation eine H1 nicht.</span><span class="sxs-lookup"><span data-stu-id="2bb33-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="2bb33-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="2bb33-109">Resolution</span></span>

<span data-ttu-id="2bb33-110">Fügen Sie in Ihrer H1 ein Leerzeichen nach dem Hash hinzu, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2bb33-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
