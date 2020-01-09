---
title: Senden eines Pull Requests
description: In diesem Artikel werden der Pull Request-Prozess und bewährte Methoden beschrieben, um sicherzustellen, dass Ihre Beiträge zusammengeführt werden können.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188226"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="57e71-103">Bewährte Methoden für Pull Requests (PRs)</span><span class="sxs-lookup"><span data-stu-id="57e71-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="57e71-104">Um Inhaltsänderungen zu veröffentlichen, übermitteln Sie einen Pull Request aus Ihrem Fork.</span><span class="sxs-lookup"><span data-stu-id="57e71-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="57e71-105">Jeder Pull Request muss vor dem Zusammenführen geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="57e71-105">Every pull request has to be reviewed before it can be merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="57e71-106">Korrekter Branch als Ziel</span><span class="sxs-lookup"><span data-stu-id="57e71-106">Target the correct branch</span></span>

<span data-ttu-id="57e71-107">Alle Änderungen sollten am Branch `staging` erfolgen.</span><span class="sxs-lookup"><span data-stu-id="57e71-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="57e71-108">Änderungen sollten niemals auf den Branch `live` ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="57e71-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="57e71-109">Änderungen, die im Branch `staging` vorgenommen wurden, werden in `live` zusammengeführt, sodass alle Änderungen an `live` überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="57e71-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="57e71-110">Wenn Sie eine Änderung an der Dokumentation einreichen, die nur für eine nicht veröffentlichte Version von PowerShell gilt, überprüfen Sie, ob es einen Releasebranch für diese Version gibt.</span><span class="sxs-lookup"><span data-stu-id="57e71-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="57e71-111">Alle Änderungen, die für eine bestimmte, zukünftige Version gelten, sollten auf den Releasebranch ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="57e71-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="57e71-112">Releasebranches haben das folgende Namensmuster: `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="57e71-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="57e71-113">Bessere Bearbeitung der Pull Request-Warteschlange im Interesse aller Beteiligten</span><span class="sxs-lookup"><span data-stu-id="57e71-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="57e71-114">Für die PR-Warteschlange gelten zwei grundlegende Wahrheiten:</span><span class="sxs-lookup"><span data-stu-id="57e71-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="57e71-115">Pull Requests mit kleinem Umfang und verwandten Änderungen können schneller geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="57e71-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="57e71-116">Bei Pull Requests mit großem Umfang oder nicht verwandten Änderungen dauert die Prüfung länger.</span><span class="sxs-lookup"><span data-stu-id="57e71-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="57e71-117">Vermeiden von Branchs, die eine große Zahl von Dateien aktualisieren</span><span class="sxs-lookup"><span data-stu-id="57e71-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="57e71-118">Trennen Sie geringfügige Updates vorhandener Artikel von neuen Artikeln oder wesentlichen Überarbeitungen.</span><span class="sxs-lookup"><span data-stu-id="57e71-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="57e71-119">Arbeiten Sie in separaten Arbeitsbranchs an diesen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="57e71-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="57e71-120">Umfangreiche Änderungen haben PRs mit einer großen Anzahl von geänderten Dateien zur Folge.</span><span class="sxs-lookup"><span data-stu-id="57e71-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="57e71-121">Beschränken Sie Ihre PRs auf maximal 50 geänderte Dateien.</span><span class="sxs-lookup"><span data-stu-id="57e71-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="57e71-122">Große PRs sind schwer zu überprüfen und sind anfälliger für Fehler.</span><span class="sxs-lookup"><span data-stu-id="57e71-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="57e71-123">Umbenennen oder Löschen von Dateien</span><span class="sxs-lookup"><span data-stu-id="57e71-123">Renaming or deleting files</span></span>

<span data-ttu-id="57e71-124">Wenn Sie Dateien umbenennen oder löschen, sollten Sie diese Änderungen nicht mit Inhaltsergänzungen oder Updates kombinieren.</span><span class="sxs-lookup"><span data-stu-id="57e71-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="57e71-125">Behandeln Sie die Änderungen in einem separaten PR, der nach dem PR für verwandte Updates gemergt wird.</span><span class="sxs-lookup"><span data-stu-id="57e71-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="57e71-126">Aktualisieren Sie z.B. die Datei der Umleitung, und überprüfen Sie vor dem Löschen eines Artikels, ob die Umleitung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57e71-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="57e71-127">Sie müssen alle Dateien aktualisieren, die mit der umbenannten Datei verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="57e71-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="57e71-128">Dies schließt alle Dateien des Inhaltsverzeichnisses ein.</span><span class="sxs-lookup"><span data-stu-id="57e71-128">This includes any TOC files.</span></span> <span data-ttu-id="57e71-129">Des Weiteren müssen Sie die Umleitungseinträge in der Masterumleitungsdatei (`.openpublishing.redirection.json`) im Stammverzeichnis des Repository hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57e71-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="57e71-130">Docs PR-Überprüfungsdienst</span><span class="sxs-lookup"><span data-stu-id="57e71-130">Docs PR validation service</span></span>

<span data-ttu-id="57e71-131">Der Docs PR-Überprüfungsdienst ist eine GitHub-App, die Gültigkeitsprüfungsregeln für die Dateien in einem PR (Pull Request) ausführt.</span><span class="sxs-lookup"><span data-stu-id="57e71-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="57e71-132">Daraufhin wird folgendes Verhalten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="57e71-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="57e71-133">Sie senden einen PR.</span><span class="sxs-lookup"><span data-stu-id="57e71-133">You submit a PR.</span></span>
1. <span data-ttu-id="57e71-134">Im GitHub-Kommentar, der den Status Ihres PRs anzeigt, wird der Status der für das Repository aktivierten „Überprüfungen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57e71-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="57e71-135">Beachten Sie, dass in diesem Beispiel zwei Überprüfungen aktiviert sind, „Commit Validation“ und „OpenPublishing.Build“:</span><span class="sxs-lookup"><span data-stu-id="57e71-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![Fehler bei einigen Überprüfungen](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="57e71-137">Die „Build“-Überprüfung kann erfolgreich sein, selbst wenn die „Commit Validation“-Überprüfung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="57e71-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="57e71-138">Klicken Sie auf **Details**, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57e71-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="57e71-139">Auf der Seite „Details“ werden alle fehlgeschlagenen Gültigkeitsüberprüfungen mit Information zur Problembehandlung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57e71-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="57e71-140">Wenn die Überprüfung erfolgreich ist, wird dem PR der folgende Kommentar hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="57e71-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![Buildüberprüfung](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="57e71-142">Wenn Sie ein externer (nicht von Microsoft) Mitwirkender sind, haben Sie keinen Zugriff auf die ausführlichen Buildberichte oder Vorschaulinks.</span><span class="sxs-lookup"><span data-stu-id="57e71-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="57e71-143">Buildwarnungen</span><span class="sxs-lookup"><span data-stu-id="57e71-143">Build warnings</span></span>

<span data-ttu-id="57e71-144">Normalerweise sollten Sie alle Buildfehler, Warnungen und Vorschläge beheben.</span><span class="sxs-lookup"><span data-stu-id="57e71-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="57e71-145">Es gibt jedoch einige Warnungen, die ignoriert werden können.</span><span class="sxs-lookup"><span data-stu-id="57e71-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="57e71-146">Die folgenden Warnungen können ignoriert werden:</span><span class="sxs-lookup"><span data-stu-id="57e71-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="57e71-147">Der Dienstname für `<version>/<modulepath>/About/About.md` kann nicht gefunden werden!</span><span class="sxs-lookup"><span data-stu-id="57e71-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="57e71-148">Metadaten mit folgenden Namen dürfen nicht im YAML-Header oder als Metadaten auf Dateiebene in „docfx.JSON“ oder als globale Metadaten in „docfx.JSON“ festgelegt werden: `locale`.</span><span class="sxs-lookup"><span data-stu-id="57e71-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="57e71-149">Diese werden von der Microsoft Dokumentation-Plattform generiert, sodass die Werte, die an diesen drei Stellen festgelegt werden, ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="57e71-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="57e71-150">Entfernen Sie diese bitte von allen drei Stellen, um die Warnung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="57e71-150">Please remove them from all 3 places to resolve the warning.</span></span>
