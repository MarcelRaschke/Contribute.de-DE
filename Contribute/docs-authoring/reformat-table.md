---
title: Neuformatieren von Markdowntabellen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie die verschiedenen Formatierungsfeatures für Markdowntabellen aus dem Docs Authoring Pack, Visual Studio Code-Erweiterung, verwenden.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336771"
---
# <a name="reformat-markdown-tables"></a>Neuformatieren von Markdowntabellen

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

Wenn Sie in einer Markdowndatei ( *\*.MD*) eine komplette Tabelle auswählen, stehen Ihnen zwei Kontextmenüelemente für Tabellenformatierung zur Verfügung. Klicken Sie mit der rechten Maustaste auf die ausgewählte Markdowntabelle, um das Kontextmenü zu öffnen. Dann wird etwas wie die folgenden Menüelemente angezeigt:

:::image type="content" source="media/reformat-table-menu.png" alt-text="Kontextmenü „Tabelle neu formatieren“":::

> [!TIP]
> Dieses Feature funktioniert **nicht** bei der Auswahl von mehreren Tabellen, sondern ist für eine einzelne Markdowntabelle vorgesehen. Sie müssen die gesamte Tabelle auswählen, einschließlich der Überschriften für die gewünschten Ergebnisse.

## <a name="consolidate-selected-table"></a>Ausgewählte Tabelle konsolidieren

Wenn Sie die Option **Ausgewählte Tabelle konsolidieren** auswählen, werden die Tabellenüberschriften und Inhalte so reduziert, dass auf jeder Seite der einzelnen Werte nur ein Leerzeichen steht.

## <a name="evenly-distribute-selected-table"></a>Ausgewählte Tabelle gleichmäßig verteilen

Wenn Sie die Option **Ausgewählte Tabelle gleichmäßig verteilen** auswählen, wird der längste Wert in jeder Spalte berechnet, und alle anderen Werte werden gleichmäßig entsprechend über den Bereich verteilt.

## <a name="considerations"></a>Überlegungen

Das Feature wirkt sich nicht auf das Rendering der Tabelle aus, wird aber dabei helfen, die Lesbarkeit der Tabelle – und dadurch deren Verwaltbarkeit – zu verbessern. Bei dem Feature zur Neuformatierung von Tabellen bleibt die Spaltenausrichtung erhalten.

Sehen Sie sich die folgende Tabelle an:

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

Nach dem Vorgang „gleichmäßig verteilt“:

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

Nach dem Vorgang „konsolidiert“:

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

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zum Neuformatieren von Tabellen](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
