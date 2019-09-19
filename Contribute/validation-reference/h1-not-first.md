---
title: h1-not-first
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895460"
---
# <a name="h1-not-first"></a><span data-ttu-id="76a49-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="76a49-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="76a49-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="76a49-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="76a49-105">Nur der YAML-Metadatenheader darf vor der H1-Überschrift in einer Markdowndatei stehen.</span><span class="sxs-lookup"><span data-stu-id="76a49-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="76a49-106">Wenn Sie einen Hinweis oder ein Bild zum Anfang des Artikels hinzufügen möchten, muss dieses nach der H1-Überschrift stehen.</span><span class="sxs-lookup"><span data-stu-id="76a49-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="76a49-107">Folgendes ist nicht zulässig:</span><span class="sxs-lookup"><span data-stu-id="76a49-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="76a49-108">Gehen Sie stattdessen folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="76a49-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="76a49-109">Das Problem wird außerdem häufig durch [Bytereihenfolge-Marken (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) vor dem YAML-Header verursacht.</span><span class="sxs-lookup"><span data-stu-id="76a49-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="76a49-110">Diese werden manchmal durch Codierungsprobleme ausgelöst, wenn Inhalte an Repositorys committet werden.</span><span class="sxs-lookup"><span data-stu-id="76a49-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="76a49-111">Dadurch entsteht ein fehlerhaftes Rendering auf GitHub, deshalb sollten diese entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="76a49-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="76a49-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="76a49-112">Resolution</span></span>

<span data-ttu-id="76a49-113">Entfernen Sie sämtliche Inhalte außer dem YAML-Metadatenheader vor der H1-Überschrift.</span><span class="sxs-lookup"><span data-stu-id="76a49-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
