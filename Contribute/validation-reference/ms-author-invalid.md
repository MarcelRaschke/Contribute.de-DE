---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246307"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="0628b-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="0628b-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="0628b-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="0628b-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="0628b-105">Lösung</span><span class="sxs-lookup"><span data-stu-id="0628b-105">Resolution</span></span>

<span data-ttu-id="0628b-106">Ändern Sie den `ms.author`-Wert in den gültigen Microsoft-Alias des aktuellen Autors.</span><span class="sxs-lookup"><span data-stu-id="0628b-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="0628b-107">Es wird empfohlen, dass der festgelegte Autor ein Vollzeitmitarbeiter oder Mitglied einer Teamverteilerliste (DL) und kein vorübergehender Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="0628b-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="0628b-108">Wenn der Alias eine Verteilerliste (Distribution List, DL) ist, muss dieser sich ebenfalls auf der `ms.author`-Zulassungsliste befinden.</span><span class="sxs-lookup"><span data-stu-id="0628b-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="0628b-109">Gültige Werte für `ms.author`-Verteilerlisten finden Sie auf [dieser internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0628b-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
