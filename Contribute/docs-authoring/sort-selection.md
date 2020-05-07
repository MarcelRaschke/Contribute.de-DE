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
# <a name="sort-selection"></a>Sortierauswahl

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

Wenn Sie in einer Markdowndatei ( *\*.MD*) Ihre Auswahl getroffen haben, stehen Ihnen jetzt zwei Kontextmenüelemente zum Sortieren zur Verfügung. Klicken Sie mit der rechten Maustaste auf den markierten Text, um das Kontextmenü zu öffnen. Dann wird etwas wie die folgenden Menüelemente angezeigt:

:::image type="content" source="media/sort-selection-menu.png" alt-text="Kontextmenü für „Sortierauswahl“":::

> [!TIP]
> Die Kontextmenüelemente zum Sortieren sind so lange ausgeblendet, bis der Text-Editor von Visual Studio Code eine gültige Auswahl enthält.

## <a name="sort-selection-ascending-a-to-z"></a>Auswahl aufsteigend sortieren (A bis Z)

Wenn Sie die Option **Auswahl aufsteigend sortieren (A bis Z)** auswählen, wird die gesamte Auswahl aufsteigend, alphabetisch von A bis Z, sortiert.

## <a name="sort-selection-descending-z-to-a"></a>Auswahl absteigend sortieren (Z bis A)

Wenn Sie die Option **Auswahl absteigend sortieren (Z bis A)** auswählen, wird die gesamte Auswahl absteigend, alphabetisch von Z bis A, sortiert.

## <a name="considerations"></a>Überlegungen

Der zugrunde liegende Sortiermechanismus verwendet *natürliche Sprache*. Dadurch ist er leistungsfähiger und umfassender als die Standardsortierung. Sehen Sie sich die folgende Tabelle an:

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

Ohne natürlichsprachliche Sortierung wäre die Reihenfolge für `Column1` 1, 11, 2 usw. gewesen, doch sie „versteht“ stattdessen, dass 11 größer als 2 ist. Dies ergibt die folgende aufsteigende Reihenfolge:

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

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zur Sortierauswahl](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
