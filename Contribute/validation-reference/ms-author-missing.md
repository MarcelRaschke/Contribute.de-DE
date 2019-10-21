---
title: ms-author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246256"
---
# <a name="ms-author-missing"></a><span data-ttu-id="2d3cd-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="2d3cd-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="2d3cd-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="2d3cd-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="2d3cd-105">Lösung</span><span class="sxs-lookup"><span data-stu-id="2d3cd-105">Resolution</span></span>

<span data-ttu-id="2d3cd-106">Fügen Sie den Microsoft-Alias des aktuellen Autors für `ms.author` hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d3cd-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="2d3cd-107">Falls sich der Besitzer geändert hat, muss dies der *aktuelle* Besitzer des Artikels sein und nicht der ursprüngliche Autor.</span><span class="sxs-lookup"><span data-stu-id="2d3cd-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="2d3cd-108">Es wird empfohlen, dass der festgelegte Autor ein Vollzeitmitarbeiter oder Mitglied einer Teamverteilerliste (DL) und kein vorübergehender Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="2d3cd-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="2d3cd-109">Wenn der Alias eine Verteilerliste (Distribution List, DL) ist, muss dieser sich ebenfalls auf der `ms.author`-Zulassungsliste befinden.</span><span class="sxs-lookup"><span data-stu-id="2d3cd-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="2d3cd-110">Gültige Werte für `ms.author`-Verteilerlisten finden Sie auf [dieser internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="2d3cd-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
