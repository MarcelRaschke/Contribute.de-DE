---
title: internal-bookmark-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427496"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="622dd-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="622dd-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="622dd-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="622dd-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="622dd-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="622dd-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="622dd-106">Sie versuchen, in der aktuellen Datei eine Überschrift zu verknüpfen, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="622dd-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="622dd-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="622dd-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="622dd-108">Überprüfen Sie die Überschrift, die Sie verknüpfen möchten, und aktualisieren Sie den Link.</span><span class="sxs-lookup"><span data-stu-id="622dd-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="622dd-109">Verwenden Sie ein Hashsymbol gefolgt von der Überschrift, um einen Abschnitt im aktuellen Artikel zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="622dd-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="622dd-110">Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="622dd-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="622dd-111">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="622dd-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
