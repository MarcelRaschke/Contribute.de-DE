---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084528"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="676ed-101">Docs PR-Überprüfungsdienst</span><span class="sxs-lookup"><span data-stu-id="676ed-101">Docs PR validation service</span></span>

<span data-ttu-id="676ed-102">Der Docs PR-Überprüfungsdienst ist eine GitHub-App, die Gültigkeitsprüfungsregeln für die Dateien in einem PR (Pull Request) ausführt.</span><span class="sxs-lookup"><span data-stu-id="676ed-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="676ed-103">Wenn der Überprüfungsdienst für ein Repository aktiviert ist, werden Sie das folgende Verhalten beobachten:</span><span class="sxs-lookup"><span data-stu-id="676ed-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="676ed-104">Sie senden einen PR.</span><span class="sxs-lookup"><span data-stu-id="676ed-104">You submit a PR.</span></span>
1. <span data-ttu-id="676ed-105">Im GitHub-Kommentar, der den Status Ihres PRs anzeigt, wird der Status der für das Repository aktivierten „Überprüfungen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="676ed-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="676ed-106">Beachten Sie, dass in diesem Beispiel zwei Überprüfungen aktiviert sind, „Commit Validation“ und „OpenPublishing.Build“:</span><span class="sxs-lookup"><span data-stu-id="676ed-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![Fehler bei einigen Überprüfungen](media/validation-failed.png)

   <span data-ttu-id="676ed-108">Die „Build“-Überprüfung kann erfolgreich sein, selbst wenn die „Commit Validation“-Überprüfung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="676ed-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="676ed-109">Klicken Sie auf **Details**, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="676ed-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="676ed-110">Auf der Details-Seite werden alle fehlgeschlagenen Gültigkeitsüberprüfungen mit Information zur Problembehandlung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="676ed-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![Validierungsmeldung](media/validation-details.png)

<span data-ttu-id="676ed-112">Die Liste der derzeit im Dienst verfügbaren Gültigkeiten finden Sie links im Inhaltsverzeichnis dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="676ed-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>