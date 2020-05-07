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
# <a name="image-compression"></a><span data-ttu-id="23f19-103">Bildkomprimierung</span><span class="sxs-lookup"><span data-stu-id="23f19-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="23f19-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="23f19-104">Summary</span></span>

<span data-ttu-id="23f19-105">Die gesamte Dokumentation wird über das Internet bereitgestellt, mit Ausnahme der PDF-Versionen von Dokumenten. Bei der Verarbeitung statischer Inhalte empfiehlt es sich, die Anzahl der über das Netzwerk gesendeten Bytes zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="23f19-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="23f19-106">Eine Möglichkeit besteht darin, ruhende Bilder zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="23f19-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="23f19-107">Die Docs Authoring Pack-Erweiterung enthält Kontextmenüelemente für die Bildkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="23f19-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="23f19-108">Die folgenden Bildtypen/Erweiterungen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="23f19-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="23f19-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="23f19-109">*\*.png*</span></span>
* <span data-ttu-id="23f19-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="23f19-110">*\*.jpg*</span></span>
* <span data-ttu-id="23f19-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="23f19-111">*\*.jpeg*</span></span>
* <span data-ttu-id="23f19-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="23f19-112">*\*.gif*</span></span>
* <span data-ttu-id="23f19-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="23f19-113">*\*.svg*</span></span>
* <span data-ttu-id="23f19-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="23f19-114">*\*.webp*</span></span>

<span data-ttu-id="23f19-115">Gegebenenfalls werden verlustfreie Bildkomprimierungsalgorithmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="23f19-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="23f19-116">Bild komprimieren</span><span class="sxs-lookup"><span data-stu-id="23f19-116">Compress image</span></span>

<span data-ttu-id="23f19-117">Klicken Sie im Navigationsbereich des **Explorers** mit der rechten Maustaste auf eine Bilddatei, und wählen Sie die Option **Bild komprimieren** aus.</span><span class="sxs-lookup"><span data-stu-id="23f19-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="23f19-118">Dann wird das Bild komprimiert.</span><span class="sxs-lookup"><span data-stu-id="23f19-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="23f19-119">Bilder im Ordner komprimieren</span><span class="sxs-lookup"><span data-stu-id="23f19-119">Compress images in folder</span></span>

<span data-ttu-id="23f19-120">Klicken Sie im Navigationsbereich des **Explorers** mit der rechten Maustaste auf einen Ordner mit Bildern, und wählen Sie die Option **Bilder im Ordner komprimieren** aus.</span><span class="sxs-lookup"><span data-stu-id="23f19-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="23f19-121">Alle Bilder im Ordner werden komprimiert.</span><span class="sxs-lookup"><span data-stu-id="23f19-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="23f19-122">Überlegungen</span><span class="sxs-lookup"><span data-stu-id="23f19-122">Considerations</span></span>

<span data-ttu-id="23f19-123">Bei Bildern mit hoher Auflösung wird die Größe implizit geändert.</span><span class="sxs-lookup"><span data-stu-id="23f19-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="23f19-124">Die maximalen Abmessungen basieren auf der von der Plattform vorgeschlagenen maximalen Breite von `1,200px`.</span><span class="sxs-lookup"><span data-stu-id="23f19-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="23f19-125">Der maximale Wert wird nur verwendet, wenn Bilder größer als empfohlen sind, und sie behalten bei einer automatischen Größenänderung das Seitenverhältnis bei.</span><span class="sxs-lookup"><span data-stu-id="23f19-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="23f19-126">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="23f19-126">Preferences</span></span>

<span data-ttu-id="23f19-127">Die maximalen Abmessungen sind konfigurierbar, aber es gibt eine maximale Standardbreite von `1200` Pixel.</span><span class="sxs-lookup"><span data-stu-id="23f19-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="23f19-128">Wählen Sie zum Konfigurieren der maximalen Abmessungen **Datei -> Einstellungen -> Einstellungen** aus, und filtern Sie nach `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="23f19-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Konfigurieren der Bildkomprimierung":::

> [!NOTE]
> <span data-ttu-id="23f19-130">Beim Wert `0` in **Maximale Breite** oder **Maximale Höhe** werden Auflösungsabweichungen einfach ignoriert.</span><span class="sxs-lookup"><span data-stu-id="23f19-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="23f19-131">In Aktion</span><span class="sxs-lookup"><span data-stu-id="23f19-131">In action</span></span>

<span data-ttu-id="23f19-132">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="23f19-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="23f19-133">[![Demo zum Komprimieren von Bildern](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="23f19-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
