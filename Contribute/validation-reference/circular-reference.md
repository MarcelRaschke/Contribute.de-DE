---
title: circular-reference
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459209"
---
# <a name="circular-reference"></a><span data-ttu-id="76859-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="76859-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="76859-104">Fehler</span><span class="sxs-lookup"><span data-stu-id="76859-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="76859-105">Dabei könnte es sich beispielsweise um eine eingeschlossene Datei handeln, die auf die aktuelle Datei oder einen Link zu einer Datei verweist, die auf die aktuelle Datei umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="76859-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="76859-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="76859-106">Resolution</span></span>

<span data-ttu-id="76859-107">Überprüfen Sie die Links in den Dateien, und nehmen Sie entsprechende Änderungen vor, damit keine Datei mit sich selbst verknüpft ist oder sich selbst einschließt.</span><span class="sxs-lookup"><span data-stu-id="76859-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
