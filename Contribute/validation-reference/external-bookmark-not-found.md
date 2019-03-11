---
title: external-bookmark-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427460"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="6c32b-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="6c32b-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="6c32b-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="6c32b-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="6c32b-105">Sie versuchen, eine Überschrift in einer anderen Datei zu verknüpfen, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6c32b-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="6c32b-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="6c32b-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="6c32b-107">Überprüfen Sie die Datei, die Sie verknüpfen, und aktualisieren Sie den Lesezeichenlink, damit dieser auf einen gültigen Abschnitt in der Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="6c32b-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="6c32b-108">Wenn Sie eine Abschnittsüberschrift in einem anderen Artikel verknüpfen möchten, verwenden Sie einen datei- oder websitebezogenen Link und ein Hashsymbol gefolgt von der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="6c32b-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="6c32b-109">Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="6c32b-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="6c32b-110">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6c32b-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
