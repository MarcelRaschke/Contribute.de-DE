---
title: h1-not-first
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528906"
---
# <a name="h1-not-first"></a><span data-ttu-id="d8626-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="d8626-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="d8626-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="d8626-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="d8626-105">Nur der YAML-Metadatenheader darf vor der H1-Überschrift in einer Markdowndatei stehen.</span><span class="sxs-lookup"><span data-stu-id="d8626-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="d8626-106">Wenn Sie einen Hinweis oder ein Bild zum Anfang des Artikels hinzufügen möchten, muss dieses nach der H1-Überschrift stehen.</span><span class="sxs-lookup"><span data-stu-id="d8626-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="d8626-107">Folgendes ist nicht zulässig:</span><span class="sxs-lookup"><span data-stu-id="d8626-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="d8626-108">Gehen Sie stattdessen folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="d8626-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="d8626-109">Das Problem wird außerdem häufig durch [Bytereihenfolge-Marken (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) vor dem YAML-Header verursacht.</span><span class="sxs-lookup"><span data-stu-id="d8626-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="d8626-110">Diese werden manchmal durch Codierungsprobleme ausgelöst, wenn Inhalte an Repositorys committet werden.</span><span class="sxs-lookup"><span data-stu-id="d8626-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="d8626-111">Dadurch entsteht ein fehlerhaftes Rendering auf GitHub, deshalb sollten diese entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d8626-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="d8626-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="d8626-112">Resolution</span></span>

<span data-ttu-id="d8626-113">Entfernen Sie sämtliche Inhalte außer dem YAML-Metadatenheader vor der H1-Überschrift.</span><span class="sxs-lookup"><span data-stu-id="d8626-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
