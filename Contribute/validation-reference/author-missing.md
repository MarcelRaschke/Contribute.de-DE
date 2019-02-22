---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431528"
---
# <a name="author-missing"></a><span data-ttu-id="0b29b-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="0b29b-103">author-missing</span></span>

<span data-ttu-id="0b29b-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="0b29b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0b29b-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="0b29b-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="0b29b-106">Das `author`-Attribut identifiziert den Autor des Artikels durch die GitHub-ID.</span><span class="sxs-lookup"><span data-stu-id="0b29b-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="0b29b-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b29b-107">Resolution</span></span>

<span data-ttu-id="0b29b-108">Fügen Sie die GitHub-ID des Autors dem YML-Header hinzu:</span><span class="sxs-lookup"><span data-stu-id="0b29b-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]