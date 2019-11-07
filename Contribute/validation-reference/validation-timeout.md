---
title: validation-timeout
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166747"
---
# <a name="validation-timeout"></a><span data-ttu-id="933d4-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="933d4-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="933d4-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="933d4-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="933d4-105">Gelegentlich verhindern vorübergehende Probleme beim Validierungsdienst (z.B. ein fehlerhafter Serverzustand), dass der Dienst bei der Erstellung von Dokumentationsartikeln erfolgreich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="933d4-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="933d4-106">Nach mehreren Versuchen erfolgt ein Timeout für den Aufruf, und die Validierung wird abgebrochen, um Verzögerungen bei der Erstellung und eine Blockierung der Buildpipeline zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="933d4-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="933d4-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="933d4-107">Resolution</span></span>

<span data-ttu-id="933d4-108">Versuchen Sie, Ihren Pull Request zu schließen und nochmals zu öffnen, oder erzwingen Sie einen vollständigen Build über das [Docs-Portal](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="933d4-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="933d4-109">Häufig erledigen sich Dienstprobleme nach dem ersten Wiederholungsversuch von selbst.</span><span class="sxs-lookup"><span data-stu-id="933d4-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="933d4-110">Beachten Sie, dass Sie ein Repositoryadministrator sein müssen, um einen Build über das Docs-Portal zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="933d4-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="933d4-111">Wenn Sie nicht wissen, wer Ihr Repositoryadministrator ist oder Sie die Meldung nach einem erzwungenen Build weiterhin erhalten, erstellen Sie ein Issue über [https://SiteHelp](https://SiteHelp), wenn Sie Microsoft-Mitarbeiter sind, oder erwähnen Sie in Ihrem PR den Autor eines Artikels mithilfe des @-Zeichens, um Unterstützung zu erhalten, wenn Sie ein externer Mitwirkender sind.</span><span class="sxs-lookup"><span data-stu-id="933d4-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="933d4-112">Wenn Sie ein Repositoryadministrator sind, können Sie wie folgt einen vollständigen Build erzwingen:</span><span class="sxs-lookup"><span data-stu-id="933d4-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="933d4-113">Navigieren Sie zum [Docs-Portal](https://ops.microsoft.com/#/), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="933d4-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="933d4-114">Sie finden Ihr Repository, indem Sie es in linken oberen Ecke suchen und dann auswählen.</span><span class="sxs-lookup"><span data-stu-id="933d4-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="933d4-115">:::image type="content" source="media/find-repo.png" alt-text="Repositorysuche über das Suchfeld im Docs-Portal":::</span><span class="sxs-lookup"><span data-stu-id="933d4-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="933d4-116">Klicken Sie auf der Registerkarte **Buildverlauf** auf **+ Manual Publish** (Manuelle Veröffentlichung).</span><span class="sxs-lookup"><span data-stu-id="933d4-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="933d4-117">Wählen Sie den Branch aus, der die Warnung erhält, z. B. „Master“.</span><span class="sxs-lookup"><span data-stu-id="933d4-117">Select the branch that's getting the Warning, such as Master.</span></span>
1. <span data-ttu-id="933d4-118">Behalten Sie für das Ziel die Standardeinstellung **Docs-Website** bei.</span><span class="sxs-lookup"><span data-stu-id="933d4-118">For target, keep the default, **Docs site**.</span></span>
1. <span data-ttu-id="933d4-119">Aktivieren Sie das Kontrollkästchen **Veröffentlichung erzwingen**.</span><span class="sxs-lookup"><span data-stu-id="933d4-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="933d4-120">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="933d4-120">Click **Publish**.</span></span>

   <span data-ttu-id="933d4-121">:::image type="content" source="media/force-build.png" alt-text="Schritte zum Erzwingen eines vollständigen Builds":::</span><span class="sxs-lookup"><span data-stu-id="933d4-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="933d4-122">So wird ein vollständiger Build auf dem Branch erzwungen.</span><span class="sxs-lookup"><span data-stu-id="933d4-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
