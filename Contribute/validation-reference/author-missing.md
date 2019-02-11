---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713037"
---
# <a name="author-missing"></a><span data-ttu-id="7f12d-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="7f12d-103">author-missing</span></span>

<span data-ttu-id="7f12d-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="7f12d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="7f12d-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="7f12d-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="7f12d-106">Das `author`-Attribut identifiziert den Autor des Artikels durch die GitHub-ID.</span><span class="sxs-lookup"><span data-stu-id="7f12d-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="7f12d-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="7f12d-107">Resolution</span></span>

<span data-ttu-id="7f12d-108">Fügen Sie die GitHub-ID des Autors dem YML-Header hinzu:</span><span class="sxs-lookup"><span data-stu-id="7f12d-108">Add the author's GitHub ID to the YML header:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]