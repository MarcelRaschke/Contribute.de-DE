---
title: Markdown-Überschriften
description: Beschreibt Anforderungen für Markdown-Überschriften
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084488"
---
# <a name="markdown-headings"></a><span data-ttu-id="d6e07-103">Markdown-Überschriften</span><span class="sxs-lookup"><span data-stu-id="d6e07-103">Markdown headings</span></span>

<span data-ttu-id="d6e07-104">Die folgenden Validierungsanforderungen gelten für Überschriften in OPS-Markdown-Dateien.</span><span class="sxs-lookup"><span data-stu-id="d6e07-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="d6e07-105">H1</span><span class="sxs-lookup"><span data-stu-id="d6e07-105">H1</span></span>

<span data-ttu-id="d6e07-106">`H1` bezieht sich auf die erste Überschrift in einer Markdown-Datei.</span><span class="sxs-lookup"><span data-stu-id="d6e07-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="d6e07-107">Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="d6e07-108">Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (`#`) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift.</span><span class="sxs-lookup"><span data-stu-id="d6e07-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="d6e07-109">Die H1 dieses Artikels sieht beispielsweise wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d6e07-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="d6e07-110">Für H1-Überschriften gelten folgende Regeln:</span><span class="sxs-lookup"><span data-stu-id="d6e07-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="d6e07-111">Eine H1 muss in der Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d6e07-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="d6e07-112">Eine H1 darf nur einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-112">There can only be one H1.</span></span>
- <span data-ttu-id="d6e07-113">Die H1 muss Inhalt aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="d6e07-114">Zwischen dem `#` und dem Inhalt der H1 muss ein Leerzeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="d6e07-115">Eine H1 ohne Leerzeichen rendert auf der veröffentlichten Seite nicht als Überschrift.</span><span class="sxs-lookup"><span data-stu-id="d6e07-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="d6e07-116">Die H1 muss nach dem YML-Metadatenheader der erste Inhalt in der Datei sein.</span><span class="sxs-lookup"><span data-stu-id="d6e07-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="d6e07-117">Zwischen dem Ende des YML-Headers und der H1 sind keine Inhalte wie Text oder Bilder zulässig.</span><span class="sxs-lookup"><span data-stu-id="d6e07-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="d6e07-118">Das HTML-Element für Überschriften der obersten Ebene, `<h1>`, sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6e07-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="d6e07-119">Verwenden Sie die Markdown-Syntax (`# `).</span><span class="sxs-lookup"><span data-stu-id="d6e07-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="d6e07-120">Die H1 darf nicht mehr als 100 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6e07-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="d6e07-121">Dies ist eine Stilrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d6e07-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="d6e07-122">H2 – H6</span><span class="sxs-lookup"><span data-stu-id="d6e07-122">H2 - H6</span></span>

<span data-ttu-id="d6e07-123">H2 (`## `) durch H6 (`###### `) sind in OPS zulässig.</span><span class="sxs-lookup"><span data-stu-id="d6e07-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="d6e07-124">Verwenden Sie zum Erstellen von Überschriften die Markdown-Header, nicht die HTML-Header (`<h2>` - `<h6>`).</span><span class="sxs-lookup"><span data-stu-id="d6e07-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
