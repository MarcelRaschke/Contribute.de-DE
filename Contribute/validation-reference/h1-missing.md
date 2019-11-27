---
title: h1-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528864"
---
# <a name="h1-missing"></a><span data-ttu-id="e4608-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="e4608-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e4608-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="e4608-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="e4608-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="e4608-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="e4608-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4608-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="e4608-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="e4608-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4608-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="e4608-108">Resolution</span></span>

<span data-ttu-id="e4608-109">Fügen Sie eine H1 als ersten Inhalt nach dem YML-Metadatenblock in Ihrer Datei hinzu, um dieses Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="e4608-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="e4608-110">Diese Regel gilt nicht für eingeschlossene Dateien.</span><span class="sxs-lookup"><span data-stu-id="e4608-110">This rule does not apply to included files.</span></span> <span data-ttu-id="e4608-111">Wenn für eingeschlossene Dateien H1-Ergebnisse ausgelöst werden, müssen Sie die eingeschlossenen Dateien wahrscheinlich in einen `includes`-Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="e4608-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="e4608-112">Der `includes`-Ordner kann sich im Dateipfad auf einer beliebigen Ebene befinden.</span><span class="sxs-lookup"><span data-stu-id="e4608-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="e4608-113">Je nach Pfad wird die Datei bei der Erstellung der Dokumentation als eingeschlossene Datei erkannt, und die H1-Überprüfung wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4608-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="e4608-114">Eine häufige Ursache für fehlende H1-Elemente in übergeordneten Dateien ist eine falsche Verwendung der eingeschlossenen Dateien: die H1 befindet sich in der eingeschlossenen Datei, nicht in der übergeordneten Datei.</span><span class="sxs-lookup"><span data-stu-id="e4608-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="e4608-115">Dies ist unzulässig, weil die Verwendung einer H1 in einer eingeschlossenen Datei entweder bedeutet, dass doppelte H1s in übergeordneten Dateien vorhanden sind oder die eingeschlossene Datei nur einmalig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4608-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="e4608-116">H1-Elemente müssen innerhalb eines Inhaltssatzes eindeutig sein, und eingeschlossene Dateien sollten nur verwendet werden, um Inhalte in mehreren Dateien gemeinsam zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4608-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="e4608-117">Wenn Sie `h1-missing`-Ergebnisse erhalten, weil die H1 in einer eingeschlossenen Datei enthalten ist, muss als Lösung die H1 in die übergeordnete Datei verschoben werden – und der gesamte eingeschlossene Inhalt, wenn die eingeschlossene Datei nur einmalig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4608-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="e4608-118">Weitere Informationen zu eingeschlossenen Dateien in der Dokumentation finden Sie im Microsoft-internen Artikel [Einschließen wiederverwendbarer Inhalte in Artikeln](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span><span class="sxs-lookup"><span data-stu-id="e4608-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
