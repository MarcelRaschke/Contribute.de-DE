---
title: insecure-link
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587673"
---
# <a name="insecure-link"></a><span data-ttu-id="3df06-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="3df06-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3df06-104">Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="3df06-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="3df06-105">**Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .</span><span class="sxs-lookup"><span data-stu-id="3df06-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="3df06-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="3df06-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="3df06-107">Diese Meldung bedeutet, dass Sie entweder einen expliziten Markdownlink mit `http` oder eine Rohdaten-URL wie beispielsweise `www.microsoft.com` verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="3df06-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="3df06-108">Rohdaten-URLs werden bei der Veröffentlichung in Microsoft-Dokumentation in unsichere Links konvertiert und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3df06-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="3df06-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="3df06-109">Resolution</span></span>

<span data-ttu-id="3df06-110">Ändern Sie alle URLs auf Microsoft-Websites, um `https` anstelle von `http` zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3df06-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="3df06-111">Wenn Ihr Link eine Rohdaten-URL ist, ändern Sie diesen in einen expliziten Markdownlink, der mit `https` beginnt.</span><span class="sxs-lookup"><span data-stu-id="3df06-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="3df06-112">Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links.</span><span class="sxs-lookup"><span data-stu-id="3df06-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="3df06-113">Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten.</span><span class="sxs-lookup"><span data-stu-id="3df06-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="3df06-114">So führen Sie das Skript aus:</span><span class="sxs-lookup"><span data-stu-id="3df06-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="3df06-115">Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="3df06-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="3df06-116">Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3df06-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="3df06-117">Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.</span><span class="sxs-lookup"><span data-stu-id="3df06-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
