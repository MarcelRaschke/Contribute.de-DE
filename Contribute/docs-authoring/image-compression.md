---
title: Bildkomprimierung – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie Bilder im Docs Authoring Pack, Visual Studio Code-Erweiterung, komprimieren.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336656"
---
# <a name="image-compression"></a>Bildkomprimierung

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>Zusammenfassung

Die gesamte Dokumentation wird über das Internet bereitgestellt, mit Ausnahme der PDF-Versionen von Dokumenten. Bei der Verarbeitung statischer Inhalte empfiehlt es sich, die Anzahl der über das Netzwerk gesendeten Bytes zu minimieren. Eine Möglichkeit besteht darin, ruhende Bilder zu komprimieren.

Die Docs Authoring Pack-Erweiterung enthält Kontextmenüelemente für die Bildkomprimierung. Die folgenden Bildtypen/Erweiterungen werden unterstützt:

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

Gegebenenfalls werden verlustfreie Bildkomprimierungsalgorithmen verwendet.

## <a name="compress-image"></a>Bild komprimieren

Klicken Sie im Navigationsbereich des **Explorers** mit der rechten Maustaste auf eine Bilddatei, und wählen Sie die Option **Bild komprimieren** aus. Dann wird das Bild komprimiert.

## <a name="compress-images-in-folder"></a>Bilder im Ordner komprimieren

Klicken Sie im Navigationsbereich des **Explorers** mit der rechten Maustaste auf einen Ordner mit Bildern, und wählen Sie die Option **Bilder im Ordner komprimieren** aus. Alle Bilder im Ordner werden komprimiert.

## <a name="considerations"></a>Überlegungen

Bei Bildern mit hoher Auflösung wird die Größe implizit geändert. Die maximalen Abmessungen basieren auf der von der Plattform vorgeschlagenen maximalen Breite von `1,200px`. Der maximale Wert wird nur verwendet, wenn Bilder größer als empfohlen sind, und sie behalten bei einer automatischen Größenänderung das Seitenverhältnis bei.

## <a name="preferences"></a>Einstellungen

Die maximalen Abmessungen sind konfigurierbar, aber es gibt eine maximale Standardbreite von `1200` Pixel. Wählen Sie zum Konfigurieren der maximalen Abmessungen **Datei -> Einstellungen -> Einstellungen** aus, und filtern Sie nach `"Docs Image Extension"`.

:::image type="content" source="media/configure-image-compression.png" alt-text="Konfigurieren der Bildkomprimierung":::

> [!NOTE]
> Beim Wert `0` in **Maximale Breite** oder **Maximale Höhe** werden Auflösungsabweichungen einfach ignoriert.

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zum Komprimieren von Bildern](media/compress-image.gif)](media/compress-image.gif#lightbox)
