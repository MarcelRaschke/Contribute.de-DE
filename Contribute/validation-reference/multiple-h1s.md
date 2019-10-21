---
title: multiple-h1
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – multiple-h1
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246275"
---
# <a name="multiple-h1"></a><span data-ttu-id="2ba19-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="2ba19-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2ba19-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="2ba19-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="2ba19-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="2ba19-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="2ba19-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ba19-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="2ba19-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="2ba19-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="2ba19-108">Pro Datei kann nur eine H1 vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2ba19-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="2ba19-109">Möglicherweise erhalten Sie diese Meldung auch, wenn Ihr Artikel eine Zeile mit Gleichheitszeichen enthält, die einen doppelten Unterstrich wie folgt macht: `=======`.</span><span class="sxs-lookup"><span data-stu-id="2ba19-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="2ba19-110">Dies ist eine alternative Markdownsyntax für eine H1.</span><span class="sxs-lookup"><span data-stu-id="2ba19-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="2ba19-111">Es ist auch häufig in Mergekonflikten zu sehen:</span><span class="sxs-lookup"><span data-stu-id="2ba19-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="2ba19-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="2ba19-112">Resolution</span></span>

<span data-ttu-id="2ba19-113">Ändern Sie nachfolgende H1-Überschriften in H2-Überschriften (`##`), oder strukturieren Sie Ihre Datei um, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2ba19-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="2ba19-114">Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu überspringen (nach H1 darf also nicht H3 folgen).</span><span class="sxs-lookup"><span data-stu-id="2ba19-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="2ba19-115">Wenn es sich bei einer zusätzlichen H1 tatsächlich um einen doppelten Unterstrich (`=======`) handelt, entfernen, oder ersetzen Sie ihn wie jeweils anwendbar durch eine Hashtagüberschrift wie beispielsweise `##`.</span><span class="sxs-lookup"><span data-stu-id="2ba19-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="2ba19-116">Wenn der doppelte Unterstrich Teil eines Mergekonflikts ist, entfernen Sie auch die Anfangs- und Endmarker des Mergekonflikts und den veralteten Text.</span><span class="sxs-lookup"><span data-stu-id="2ba19-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
