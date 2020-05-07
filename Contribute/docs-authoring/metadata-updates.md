---
title: Metadatenaktualisierungen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie Metadaten aus dem Docs Authoring Pack, Visual Studio Code-Erweiterung, aktualisieren.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336633"
---
# <a name="update-metadata"></a><span data-ttu-id="21e6b-103">Aktualisieren von Metadaten</span><span class="sxs-lookup"><span data-stu-id="21e6b-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="21e6b-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="21e6b-104">Summary</span></span>

<span data-ttu-id="21e6b-105">In einer Markdowndatei ( *\*.MD*) gibt es zwei kontextbezogene Menüelemente, die für Metadaten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="21e6b-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="21e6b-106">Wenn Sie mit der rechten Maustaste auf eine beliebige Stelle im Text-Editor klicken, wird etwas wie die folgenden Menüelemente angezeigt:</span><span class="sxs-lookup"><span data-stu-id="21e6b-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Kontextmenü „Metadaten aktualisieren“":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="21e6b-108">Aktualisieren des Metadatenwerts `ms.date`</span><span class="sxs-lookup"><span data-stu-id="21e6b-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="21e6b-109">Wenn Sie die Option **Metadatenwert `ms.date` aktualisieren** auswählen, wird der aktuelle `ms.date`-Wert für die Markdowndateien auf das heutige Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="21e6b-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="21e6b-110">Falls das Dokument kein Metadatenfeld `ms.date` enthält, wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21e6b-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="21e6b-111">Aktualisieren von impliziten Metadatenwerten</span><span class="sxs-lookup"><span data-stu-id="21e6b-111">Update implicit metadata values</span></span>

<span data-ttu-id="21e6b-112">Wenn Sie die Option **Implizite Metadatenwerte aktualisieren** auswählen, werden alle möglichen Metadatenwerte gefunden und ersetzt, die implizit angegeben werden könnten.</span><span class="sxs-lookup"><span data-stu-id="21e6b-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="21e6b-113">Metadatenwerte werden implizit in der Datei *docfx.json* unter dem Knoten `build/fileMetadata` angegeben.</span><span class="sxs-lookup"><span data-stu-id="21e6b-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="21e6b-114">Jedes Schlüssel-Wert-Paar im Knoten `fileMetadata` stellt Metadatenstandardwerte dar.</span><span class="sxs-lookup"><span data-stu-id="21e6b-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="21e6b-115">Beispielsweise könnte eine Markdowndatei im Verzeichnis *top-level/sub-folder*, in dem der Metadatenwert `ms.author` ausgelassen wird, implizit einen Standardwert angeben, der im Knoten `fileMetadata` verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21e6b-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="21e6b-116">In diesem Fall würden alle Markdowndateien implizit den Metadatenwert `ms.author: dapine` übernehmen.</span><span class="sxs-lookup"><span data-stu-id="21e6b-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="21e6b-117">Das Feature wird auf diese impliziten Einstellungen in der Datei *docfx.json* angewendet.</span><span class="sxs-lookup"><span data-stu-id="21e6b-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="21e6b-118">Wenn eine Markdowndatei Metadaten mit Werten enthält, für die explizit etwas anderes als die impliziten Werte festgelegt wird, werden sie überschrieben.</span><span class="sxs-lookup"><span data-stu-id="21e6b-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="21e6b-119">Sehen Sie sich die folgenden Markdowndatei-Metadaten an, bei denen sich diese Markdowndatei in **top-level/sub-folder/includes/example.md** befindet:</span><span class="sxs-lookup"><span data-stu-id="21e6b-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="21e6b-120">Wenn die Option **Implizite Metadatenwerte aktualisieren** für diese Datei ausgeführt wurde, würde der Metadatenwert bei dem vorstehenden angenommenen *docfx.json*-Inhalt auf `ms.author: dapine` aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="21e6b-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="21e6b-121">In Aktion</span><span class="sxs-lookup"><span data-stu-id="21e6b-121">In action</span></span>

<span data-ttu-id="21e6b-122">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="21e6b-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="21e6b-123">[![Demo zum Aktualisieren von Metadaten](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="21e6b-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
