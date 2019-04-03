---
title: deprecated-attribute
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636883"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="80b5b-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="80b5b-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="80b5b-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="80b5b-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="80b5b-105">Geben Sie mit `ms.service` Clouddienste an.</span><span class="sxs-lookup"><span data-stu-id="80b5b-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="80b5b-106">Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben.</span><span class="sxs-lookup"><span data-stu-id="80b5b-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="80b5b-107">Verwenden Sie `ms.component` nicht; es ist für diesen Inhalt veraltet.</span><span class="sxs-lookup"><span data-stu-id="80b5b-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="80b5b-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="80b5b-108">Resolution</span></span>

<span data-ttu-id="80b5b-109">Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist.</span><span class="sxs-lookup"><span data-stu-id="80b5b-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="80b5b-110">Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="80b5b-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="80b5b-111">Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="80b5b-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
