---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236541"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="4216d-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="4216d-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="4216d-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="4216d-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="4216d-105">Lösung</span><span class="sxs-lookup"><span data-stu-id="4216d-105">Resolution</span></span>

<span data-ttu-id="4216d-106">Überprüfen Sie, ob es sich bei dem Wert `ms.author` um den gültigen Microsoft-Alias des aktuellen Autors handelt.</span><span class="sxs-lookup"><span data-stu-id="4216d-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="4216d-107">Wenn der Alias eine Verteilerliste ist, muss dieser sich ebenfalls auf der Zulassungsliste befinden.</span><span class="sxs-lookup"><span data-stu-id="4216d-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="4216d-108">Gültige Werte für Verteilerlisten finden Sie auf dieser [internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="4216d-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
