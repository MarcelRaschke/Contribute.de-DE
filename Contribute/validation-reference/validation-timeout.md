---
title: validation-timeout
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024208"
---
# <a name="validation-timeout"></a><span data-ttu-id="4bb35-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="4bb35-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="4bb35-104">Warnung</span><span class="sxs-lookup"><span data-stu-id="4bb35-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="4bb35-105">Gelegentlich verhindern vorübergehende Probleme beim Validierungsdienst (z.B. ein fehlerhafter Serverzustand), dass der Dienst bei der Erstellung von Dokumentationsartikeln erfolgreich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4bb35-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="4bb35-106">Nach drei Versuchen erfolgt ein Timeout für den Aufruf, und die Validierung wird abgebrochen, um Verzögerungen bei der Erstellung und eine Blockierung der Buildpipeline zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4bb35-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="4bb35-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="4bb35-107">Resolution</span></span>

<span data-ttu-id="4bb35-108">Schließen Sie den PR, und öffnen Sie ihn erneut, oder führen Sie einen manuellen Buildvorgang aus (nur für Repositoryadministratoren).</span><span class="sxs-lookup"><span data-stu-id="4bb35-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="4bb35-109">Häufig erledigen sich Dienstprobleme nach dem ersten Wiederholungsversuch von selbst.</span><span class="sxs-lookup"><span data-stu-id="4bb35-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="4bb35-110">Wenn Sie die Meldung weiterhin erhalten, erstellen Sie ein Issue über [https://SiteHelp](https://SiteHelp), wenn Sie Microsoft-Mitarbeiter sind, oder erwähnen Sie in Ihrem PR den Autor eines Artikels mithilfe des @-Zeichens, um Unterstützung zu erhalten, wenn Sie ein externer Mitwirkender sind.</span><span class="sxs-lookup"><span data-stu-id="4bb35-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
