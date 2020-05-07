---
title: Sortierauswahl – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie das Feature „Sortierauswahl“ aus dem Docs Authoring Pack, Visual Studio Code-Erweiterung, verwenden.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336748"
---
# <a name="sort-selection"></a><span data-ttu-id="72d6c-103">Sortierauswahl</span><span class="sxs-lookup"><span data-stu-id="72d6c-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="72d6c-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="72d6c-104">Summary</span></span>

<span data-ttu-id="72d6c-105">Wenn Sie in einer Markdowndatei ( *\*.MD*) Ihre Auswahl getroffen haben, stehen Ihnen jetzt zwei Kontextmenüelemente zum Sortieren zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="72d6c-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="72d6c-106">Klicken Sie mit der rechten Maustaste auf den markierten Text, um das Kontextmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="72d6c-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="72d6c-107">Dann wird etwas wie die folgenden Menüelemente angezeigt:</span><span class="sxs-lookup"><span data-stu-id="72d6c-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Kontextmenü für „Sortierauswahl“":::

> [!TIP]
> <span data-ttu-id="72d6c-109">Die Kontextmenüelemente zum Sortieren sind so lange ausgeblendet, bis der Text-Editor von Visual Studio Code eine gültige Auswahl enthält.</span><span class="sxs-lookup"><span data-stu-id="72d6c-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="72d6c-110">Auswahl aufsteigend sortieren (A bis Z)</span><span class="sxs-lookup"><span data-stu-id="72d6c-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="72d6c-111">Wenn Sie die Option **Auswahl aufsteigend sortieren (A bis Z)** auswählen, wird die gesamte Auswahl aufsteigend, alphabetisch von A bis Z, sortiert.</span><span class="sxs-lookup"><span data-stu-id="72d6c-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="72d6c-112">Auswahl absteigend sortieren (Z bis A)</span><span class="sxs-lookup"><span data-stu-id="72d6c-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="72d6c-113">Wenn Sie die Option **Auswahl absteigend sortieren (Z bis A)** auswählen, wird die gesamte Auswahl absteigend, alphabetisch von Z bis A, sortiert.</span><span class="sxs-lookup"><span data-stu-id="72d6c-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="72d6c-114">Überlegungen</span><span class="sxs-lookup"><span data-stu-id="72d6c-114">Considerations</span></span>

<span data-ttu-id="72d6c-115">Der zugrunde liegende Sortiermechanismus verwendet *natürliche Sprache*.</span><span class="sxs-lookup"><span data-stu-id="72d6c-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="72d6c-116">Dadurch ist er leistungsfähiger und umfassender als die Standardsortierung.</span><span class="sxs-lookup"><span data-stu-id="72d6c-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="72d6c-117">Sehen Sie sich die folgende Tabelle an:</span><span class="sxs-lookup"><span data-stu-id="72d6c-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="72d6c-118">Ohne natürlichsprachliche Sortierung wäre die Reihenfolge für `Column1` 1, 11, 2 usw. gewesen, doch sie „versteht“ stattdessen, dass 11 größer als 2 ist. Dies ergibt die folgende aufsteigende Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="72d6c-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="72d6c-119">In Aktion</span><span class="sxs-lookup"><span data-stu-id="72d6c-119">In action</span></span>

<span data-ttu-id="72d6c-120">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="72d6c-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="72d6c-121">[![Demo zur Sortierauswahl](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="72d6c-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
