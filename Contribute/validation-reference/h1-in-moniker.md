---
title: h1-in-moniker
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-in-moniker
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246358"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="96609-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="96609-103">h1-in-moniker</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="96609-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="96609-104">Suggestion</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="96609-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="96609-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="96609-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96609-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="96609-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="96609-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="96609-108">Pro Datei kann nur eine H1 vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="96609-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="96609-109">H1-Elemente sind in Monikerabschnitten nicht erlaubt, da H1-Elemente in Monikern je nach Konfiguration der Versionierung leicht zu doppelten oder fehlenden H1-Elementen führen können.</span><span class="sxs-lookup"><span data-stu-id="96609-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="96609-110">Möglicherweise erhalten Sie diese Meldung auch, wenn Ihr Monikerabschnitt eine Zeile mit Gleichheitszeichen enthält, die einen doppelten Unterstrich wie folgt macht: `=======`.</span><span class="sxs-lookup"><span data-stu-id="96609-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="96609-111">Dies ist eine alternative Markdownsyntax für eine H1.</span><span class="sxs-lookup"><span data-stu-id="96609-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="96609-112">Es ist auch häufig in Mergekonflikten zu sehen:</span><span class="sxs-lookup"><span data-stu-id="96609-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="96609-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="96609-113">Resolution</span></span>

<span data-ttu-id="96609-114">Entfernen Sie H1-Elemente aus allen Monikerabschnitten, und stellen Sie sicher, dass das H1-Element oben im Artikel für alle Monikerabschnitte geeignet ist, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="96609-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="96609-115">Beachten Sie, dass es nicht zulässig ist, eine Überschriftenebene zu überspringen (nach H1 darf also nicht H3 folgen).</span><span class="sxs-lookup"><span data-stu-id="96609-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="96609-116">Wenn es sich bei einer H1 in einem Monikerabschnitt tatsächlich um einen doppelten Unterstrich (`=======`) handelt, entfernen oder ersetzen Sie ihn wie jeweils anwendbar durch eine Hashtagüberschrift wie beispielsweise `##`.</span><span class="sxs-lookup"><span data-stu-id="96609-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="96609-117">Wenn der doppelte Unterstrich Teil eines Mergekonflikts ist, entfernen Sie auch die Anfangs- und Endmarker des Mergekonflikts und den veralteten Text.</span><span class="sxs-lookup"><span data-stu-id="96609-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
