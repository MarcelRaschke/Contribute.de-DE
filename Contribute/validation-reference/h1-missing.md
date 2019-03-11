---
title: h1-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459117"
---
# <a name="h1-missing"></a><span data-ttu-id="94b6e-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="94b6e-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="94b6e-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="94b6e-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="94b6e-105">H1 bezieht sich auf die erste Überschrift in einer Markdowndatei.</span><span class="sxs-lookup"><span data-stu-id="94b6e-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="94b6e-106">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94b6e-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="94b6e-107">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (#) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="94b6e-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="94b6e-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="94b6e-108">Resolution</span></span>

<span data-ttu-id="94b6e-109">Fügen Sie eine H1 als ersten Inhalt nach dem YML-Metadatenblock in Ihrer Datei hinzu, um dieses Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="94b6e-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="94b6e-110">Diese Regel gilt nicht für eingeschlossene Dateien.</span><span class="sxs-lookup"><span data-stu-id="94b6e-110">This rule does not apply to included files.</span></span> <span data-ttu-id="94b6e-111">Wenn bei eingeschlossenen Dateien H1-Warnungen ausgelöst werden, müssen Sie die eingeschlossenen Dateien wahrscheinlich in einen `includes`-Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="94b6e-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="94b6e-112">Der `includes`-Ordner kann sich im Dateipfad auf einer beliebigen Ebene befinden.</span><span class="sxs-lookup"><span data-stu-id="94b6e-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="94b6e-113">Je nach Pfad wird die Datei bei der Erstellung der Dokumentation als eingeschlossene Datei erkannt, und die H1-Überprüfung wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94b6e-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]