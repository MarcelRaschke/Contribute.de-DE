---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481700"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="a721c-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="a721c-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="a721c-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="a721c-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="a721c-105">Lösung</span><span class="sxs-lookup"><span data-stu-id="a721c-105">Resolution</span></span>

<span data-ttu-id="a721c-106">Überprüfen Sie, ob es sich bei dem Wert `ms.author` um den gültigen Microsoft-Alias des aktuellen Autors handelt.</span><span class="sxs-lookup"><span data-stu-id="a721c-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="a721c-107">Es wird empfohlen, dass der festgelegte Autor ein Vollzeitmitarbeiter oder Mitglied einer Teamverteilerliste ist und kein vorübergehender Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a721c-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="a721c-108">Wenn der Alias eine Verteilerliste (Distribution List, DL) ist, muss dieser sich ebenfalls auf der `ms.author`-Zulassungsliste befinden.</span><span class="sxs-lookup"><span data-stu-id="a721c-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="a721c-109">Gültige Werte für `ms.author`-Verteilerlisten finden Sie auf [dieser internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="a721c-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
