---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848580"
---
# <a name="author-missing"></a><span data-ttu-id="8a60d-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="8a60d-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="8a60d-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="8a60d-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="8a60d-105">Das `author`-Attribut identifiziert den Autor des Artikels durch die GitHub-ID.</span><span class="sxs-lookup"><span data-stu-id="8a60d-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="8a60d-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="8a60d-106">Resolution</span></span>

<span data-ttu-id="8a60d-107">Fügen Sie die GitHub-ID des aktuellen Autors dem YML-Header hinzu:</span><span class="sxs-lookup"><span data-stu-id="8a60d-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="8a60d-108">Falls sich der Besitzer geändert hat, muss dies der *aktuelle* Besitzer des Artikels sein und nicht der ursprüngliche Autor.</span><span class="sxs-lookup"><span data-stu-id="8a60d-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
