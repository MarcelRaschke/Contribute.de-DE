---
title: insecure-link
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379507"
---
# <a name="insecure-link"></a><span data-ttu-id="ad70c-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="ad70c-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ad70c-104">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="ad70c-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="ad70c-105">Diese Meldung bedeutet, dass Sie entweder einen expliziten Markdownlink mit `http` oder eine Rohdaten-URL wie beispielsweise `www.microsoft.com` verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ad70c-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="ad70c-106">Rohdaten-URLs werden bei der Veröffentlichung in Microsoft-Dokumentation in unsichere Links konvertiert und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad70c-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad70c-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="ad70c-107">Resolution</span></span>

<span data-ttu-id="ad70c-108">Ändern Sie alle URLs auf Microsoft-Websites, um `https` anstelle von `http` zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad70c-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="ad70c-109">Wenn Ihr Link eine Rohdaten-URL ist, ändern Sie diesen in einen expliziten Markdownlink, der mit `https` beginnt.</span><span class="sxs-lookup"><span data-stu-id="ad70c-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="ad70c-110">Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links.</span><span class="sxs-lookup"><span data-stu-id="ad70c-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="ad70c-111">Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad70c-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="ad70c-112">So führen Sie das Skript aus:</span><span class="sxs-lookup"><span data-stu-id="ad70c-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="ad70c-113">Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="ad70c-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="ad70c-114">Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad70c-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="ad70c-115">Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.</span><span class="sxs-lookup"><span data-stu-id="ad70c-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
