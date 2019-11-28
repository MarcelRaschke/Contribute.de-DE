---
title: insecure-link
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528846"
---
# <a name="insecure-link"></a><span data-ttu-id="d8300-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="d8300-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8300-104">Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="d8300-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="d8300-105">**Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .</span><span class="sxs-lookup"><span data-stu-id="d8300-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="d8300-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="d8300-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="d8300-107">Diese Meldung bedeutet, dass Sie entweder einen expliziten Markdownlink mit `http` oder eine Rohdaten-URL wie beispielsweise `www.microsoft.com` verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="d8300-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="d8300-108">Rohdaten-URLs werden bei der Veröffentlichung in Microsoft-Dokumentation in unsichere Links konvertiert und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8300-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="d8300-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="d8300-109">Resolution</span></span>

<span data-ttu-id="d8300-110">Ändern Sie alle URLs auf Microsoft-Websites, um `https` anstelle von `http` zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8300-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="d8300-111">Wenn Ihr Link eine Rohdaten-URL ist, ändern Sie diesen wie im folgenden Beispiel in einen expliziten Markdownlink, der mit `https` beginnt:</span><span class="sxs-lookup"><span data-stu-id="d8300-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`, such as:</span></span>

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> <span data-ttu-id="d8300-112">Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links.</span><span class="sxs-lookup"><span data-stu-id="d8300-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="d8300-113">Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8300-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="d8300-114">So führen Sie das Skript aus:</span><span class="sxs-lookup"><span data-stu-id="d8300-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="d8300-115">Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="d8300-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="d8300-116">Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8300-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="d8300-117">Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.</span><span class="sxs-lookup"><span data-stu-id="d8300-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<span data-ttu-id="d8300-118">In einigen Fällen müssen Sie möglicherweise Webadressen dokumentieren, z. B. vollqualifizierte Domänennamen, die keine klickbaren Links sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d8300-118">In some cases, you might need to document web addresses, such as fully-qualified domain names, that aren't meant to be clickable links.</span></span> <span data-ttu-id="d8300-119">Diese sollten wie im folgenden Beispiel als Inlinecode formatiert werden:</span><span class="sxs-lookup"><span data-stu-id="d8300-119">These should be styled as inline code, such as:</span></span>

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
