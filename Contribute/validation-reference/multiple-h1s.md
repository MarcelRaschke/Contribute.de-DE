---
title: multiple-h1
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-h1
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848606"
---
# <a name="multiple-h1"></a><span data-ttu-id="8c0dd-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="8c0dd-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8c0dd-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="8c0dd-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="8c0dd-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="8c0dd-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="8c0dd-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c0dd-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="8c0dd-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="8c0dd-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="8c0dd-108">Pro Datei kann nur eine H1 vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8c0dd-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c0dd-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="8c0dd-109">Resolution</span></span>

<span data-ttu-id="8c0dd-110">Ändern Sie nachfolgende H1-Überschriften in H2-Überschriften (`##`), oder strukturieren Sie Ihre Datei um, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="8c0dd-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="8c0dd-111">Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu übersprungen (nach H1 darf also nicht H3 folgen).</span><span class="sxs-lookup"><span data-stu-id="8c0dd-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]