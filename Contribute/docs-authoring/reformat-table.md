---
title: Neuformatieren von Markdowntabellen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie die verschiedenen Formatierungsfeatures für Markdowntabellen aus dem Docs Authoring Pack, Visual Studio Code-Erweiterung, verwenden.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336771"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="a6b18-103">Neuformatieren von Markdowntabellen</span><span class="sxs-lookup"><span data-stu-id="a6b18-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="a6b18-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a6b18-104">Summary</span></span>

<span data-ttu-id="a6b18-105">Wenn Sie in einer Markdowndatei ( *\*.MD*) eine komplette Tabelle auswählen, stehen Ihnen zwei Kontextmenüelemente für Tabellenformatierung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a6b18-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="a6b18-106">Klicken Sie mit der rechten Maustaste auf die ausgewählte Markdowntabelle, um das Kontextmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a6b18-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="a6b18-107">Dann wird etwas wie die folgenden Menüelemente angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a6b18-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Kontextmenü „Tabelle neu formatieren“":::

> [!TIP]
> <span data-ttu-id="a6b18-109">Dieses Feature funktioniert **nicht** bei der Auswahl von mehreren Tabellen, sondern ist für eine einzelne Markdowntabelle vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a6b18-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="a6b18-110">Sie müssen die gesamte Tabelle auswählen, einschließlich der Überschriften für die gewünschten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="a6b18-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="a6b18-111">Ausgewählte Tabelle konsolidieren</span><span class="sxs-lookup"><span data-stu-id="a6b18-111">Consolidate selected table</span></span>

<span data-ttu-id="a6b18-112">Wenn Sie die Option **Ausgewählte Tabelle konsolidieren** auswählen, werden die Tabellenüberschriften und Inhalte so reduziert, dass auf jeder Seite der einzelnen Werte nur ein Leerzeichen steht.</span><span class="sxs-lookup"><span data-stu-id="a6b18-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="a6b18-113">Ausgewählte Tabelle gleichmäßig verteilen</span><span class="sxs-lookup"><span data-stu-id="a6b18-113">Evenly distribute selected table</span></span>

<span data-ttu-id="a6b18-114">Wenn Sie die Option **Ausgewählte Tabelle gleichmäßig verteilen** auswählen, wird der längste Wert in jeder Spalte berechnet, und alle anderen Werte werden gleichmäßig entsprechend über den Bereich verteilt.</span><span class="sxs-lookup"><span data-stu-id="a6b18-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="a6b18-115">Überlegungen</span><span class="sxs-lookup"><span data-stu-id="a6b18-115">Considerations</span></span>

<span data-ttu-id="a6b18-116">Das Feature wirkt sich nicht auf das Rendering der Tabelle aus, wird aber dabei helfen, die Lesbarkeit der Tabelle – und dadurch deren Verwaltbarkeit – zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a6b18-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="a6b18-117">Bei dem Feature zur Neuformatierung von Tabellen bleibt die Spaltenausrichtung erhalten.</span><span class="sxs-lookup"><span data-stu-id="a6b18-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="a6b18-118">Sehen Sie sich die folgende Tabelle an:</span><span class="sxs-lookup"><span data-stu-id="a6b18-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="a6b18-119">Nach dem Vorgang „gleichmäßig verteilt“:</span><span class="sxs-lookup"><span data-stu-id="a6b18-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="a6b18-120">Nach dem Vorgang „konsolidiert“:</span><span class="sxs-lookup"><span data-stu-id="a6b18-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="a6b18-121">In Aktion</span><span class="sxs-lookup"><span data-stu-id="a6b18-121">In action</span></span>

<span data-ttu-id="a6b18-122">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="a6b18-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="a6b18-123">[![Demo zum Neuformatieren von Tabellen](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a6b18-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
