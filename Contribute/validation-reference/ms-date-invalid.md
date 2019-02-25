---
title: ms-date-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: e960bc2d8e9013e480f2bb391cdfa0c1da043b8b
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431505"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="99319-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="99319-103">ms-date-invalid</span></span>

<span data-ttu-id="99319-104">**Bald verfügbar!**</span><span class="sxs-lookup"><span data-stu-id="99319-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="99319-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="99319-105">Suggestion</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="99319-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="99319-106">Resolution</span></span>

<span data-ttu-id="99319-107">Bestätigen Sie, dass der Artikel ohne Brüche im Inhalt aktuell ist, und fügen Sie ein gültiges Datum im Format MM/TT/JJJJ hinzu:</span><span class="sxs-lookup"><span data-stu-id="99319-107">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
