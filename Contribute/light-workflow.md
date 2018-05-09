---
title: GitHub-Beitragsworkflow für geringfügige oder selten vorkommende Änderungen
description: In diesem Artikel erfahren Sie, wie Sie den Beitragsworkflow für geringfügige Änderungen bei der Mitwirkung an docs.microsoft.com-Artikeln verwenden.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a><span data-ttu-id="8786a-103">GitHub-Beitragsworkflow für geringfügige oder selten vorkommende Änderungen</span><span class="sxs-lookup"><span data-stu-id="8786a-103">GitHub contribution workflow for minor or infrequent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8786a-104">Für alle Repositorys, die in „docs.microsoft.com“ veröffentlichen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache).</span><span class="sxs-lookup"><span data-stu-id="8786a-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="8786a-105">Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/).</span><span class="sxs-lookup"><span data-stu-id="8786a-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="8786a-106">Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).</span><span class="sxs-lookup"><span data-stu-id="8786a-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="8786a-107">Kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys werden durch die [docs.microsoft.com - Nutzungsbestimmungen](https://docs.microsoft.com/legal/termsofuse) abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="8786a-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="8786a-108">Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind.</span><span class="sxs-lookup"><span data-stu-id="8786a-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="8786a-109">Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request annehmen können.</span><span class="sxs-lookup"><span data-stu-id="8786a-109">We need you to complete the online form before we can accept your pull request.</span></span>

## <a name="overview"></a><span data-ttu-id="8786a-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8786a-110">Overview</span></span>

<span data-ttu-id="8786a-111">Dieser Workflow eignet sich dazu, geringfügige oder selten vorkommende Änderungen mithilfe des webbasierten Markdown-Editors von GitHub vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8786a-111">This workflow is suitable for making minor or infrequent changes, by using GitHub's web-based Markdown editor.</span></span> <span data-ttu-id="8786a-112">Ihre Bearbeitungsmöglichkeiten im GitHub-Editor sind eingeschränkt, da die Benutzeroberfläche nicht alle Git-Vorgänge und Erstellungsszenarios unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8786a-112">The GitHub editor is limited in terms of what you can do, because the UI does not support all Git operations and authoring scenarios.</span></span> <span data-ttu-id="8786a-113">Wenn Sie umfangreichere Beiträge erstellen müssen oder Unterstützung zu fortgeschrittenen Git-Features benötigen (z.B. Branchingverwaltung, fortgeschrittene Zusammenführungs-Konfliktlösung), beachten Sie bitte die Informationen zum [Beitragsworkflow für größere oder langfristige Änderungen](full-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="8786a-113">If you need to make large contributions, or you need support for advanced Git features (such as branch management or advanced merge conflict resolution), refer to the [major or long-running changes workflow](full-workflow.md).</span></span>

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a><span data-ttu-id="8786a-114">Prozedur für die Verwendung des GitHub-Editors zum Vorschlagen Ihrer Änderungen</span><span class="sxs-lookup"><span data-stu-id="8786a-114">Procedure for using the GitHub editor to propose your changes</span></span>

1. <span data-ttu-id="8786a-115">Durchsuchen Sie das GitHub-Repository und die Markdowndatei des Artikels.</span><span class="sxs-lookup"><span data-stu-id="8786a-115">Browse to the article's corresponding GitHub repository and Markdown file.</span></span> <span data-ttu-id="8786a-116">Dazu können Sie eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="8786a-116">You can use either of the following methods:</span></span>

   - <span data-ttu-id="8786a-117">Suchen Sie den Artikel, indem Sie die Markdowndateien im zugehörigen GitHub-Repository durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="8786a-117">Find the article by browsing through the Markdown files in the related GitHub repository.</span></span>
   - <span data-ttu-id="8786a-118">Navigieren Sie unter [https://docs.microsoft.com/](https://docs.microsoft.com/) zum Artikel, und klicken Sie dann rechts oben auf der Seite auf den Link **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8786a-118">Go to the article on [docs.microsoft.com](https://docs.microsoft.com/) and select the **Edit** link in the upper-right corner of the page.</span></span>

     ![Ort des Links „Bearbeiten“](./media/light-workflow/contributetogit.png)

2. <span data-ttu-id="8786a-120">Wählen Sie das Bleistiftsymbol für **Diese Datei bearbeiten** oben rechts aus, um in den Bearbeitungsmodus zu wechseln:</span><span class="sxs-lookup"><span data-stu-id="8786a-120">Select the **Edit this file** pencil icon to go into edit mode:</span></span>

    ![Ort des Bleistiftsymbols](./media/light-workflow/editicon.png)

3. <span data-ttu-id="8786a-122">Nehmen Sie Änderungen vor, indem Sie Markdown auf der Registerkarte **Edit file** (Datei bearbeiten) verwenden, und zeigen Sie eine Vorschau Ihrer Änderungen auf der Registerkarte **Preview changes** (Vorschau der Änderungen) an. Die Verwendung des Editors ist recht einfach. Sollten Sie trotzdem Hilfe benötigen, nutzen Sie folgende Handbücher:</span><span class="sxs-lookup"><span data-stu-id="8786a-122">Make changes by using Markdown on the **Edit file** tab, and preview your changes on the **Preview changes** tab. Using the editor is fairly straightforward, but if you need assistance, see the following guides:</span></span>

   - [<span data-ttu-id="8786a-123">Verwendung von Markdown</span><span class="sxs-lookup"><span data-stu-id="8786a-123">How to use Markdown</span></span>](how-to-write-use-markdown.md)
   - [<span data-ttu-id="8786a-124">Erstellen von Dateien auf GitHub</span><span class="sxs-lookup"><span data-stu-id="8786a-124">Creating files on GitHub</span></span>](https://github.com/blog/1327-creating-files-on-github)
   - [<span data-ttu-id="8786a-125">Hochladen von Dateien in Ihre Repositorys</span><span class="sxs-lookup"><span data-stu-id="8786a-125">Upload files to your repositories</span></span>](https://github.com/blog/2105-upload-files-to-your-repositories)

4. <span data-ttu-id="8786a-126">Scrollen Sie zum unteren Rand der Seite, wo Sie eine der folgenden Optionen sehen:</span><span class="sxs-lookup"><span data-stu-id="8786a-126">Scroll to the bottom of the page, where you see one of the following:</span></span>

   - <span data-ttu-id="8786a-127">**Propose file change** (Dateiänderung vorschlagen): Wird angezeigt, wenn Sie schreibgeschützten Zugriff auf das Repository haben, wie in [Editing files in another user's repository (Bearbeiten von Dateien im Repository eines anderen Benutzers)](https://help.github.com/articles/editing-files-in-another-user-s-repository/) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8786a-127">**Propose file change**: Appears when you have read-only access to the repository, such as [editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/).</span></span> <span data-ttu-id="8786a-128">In diesem Fall erstellt GitHub einen „Patch“-Branch in Ihrem Fork des Repositorys (und automatisch einen Fork, sofern nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="8786a-128">In this case, GitHub will create a "patch" branch in your fork of the repository (and automatically create a fork if it doesn't exist).</span></span> <span data-ttu-id="8786a-129">Nachdem Sie auf **Propose file change** (Dateiänderung vorschlagen) geklickt haben, wird die Seite **Comparing changes** (Änderungen vergleichen) angezeigt, damit Sie Ihre Änderungen überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="8786a-129">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="8786a-130">Klicken Sie dann auf die Schaltfläche **Create pull request** (Pull Request erstellen), um Ihre Änderungen an die Pull Request-Warteschlange zu übermitteln, und fahren Sie mit dem [nächsten Abschnitt](#pull-request-processing) fort.</span><span class="sxs-lookup"><span data-stu-id="8786a-130">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

   - <span data-ttu-id="8786a-131">**Commit changes** (Änderungen übernehmen): Wird angezeigt, wenn Sie über Schreibberechtigungen in einem Repository verfügen, wie in [Editing files in your own repository (Bearbeiten von Dateien in Ihrem eigenen Repository)](https://help.github.com/articles/editing-files-in-your-repository/) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8786a-131">**Commit changes**: Appears when you have write permissions to a repository, such as [editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/).</span></span> <span data-ttu-id="8786a-132">In diesem Fall bietet GitHub Ihnen zwei Optionen zum Speichern Ihrer Änderungen an:</span><span class="sxs-lookup"><span data-stu-id="8786a-132">In this case, GitHub gives you two options for saving your changes:</span></span>

     - <span data-ttu-id="8786a-133">**Commit directly to the `<branch-name>` branch** (Direkt an den Branche <Name des Branchs> übergeben), wobei `<branch-name>` der Name des Branchs ist, in dem Sie sich befanden, als Sie auf die Schaltfläche zur **Bearbeitung** geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="8786a-133">**Commit directly to the `<branch-name>` branch**, where `<branch-name>` is the name of the branch that you were on when you selected the **Edit** button.</span></span> <span data-ttu-id="8786a-134">Hiermit werden Ihre Änderungen anstelle der Verwendung eines Pull Requests direkt auf den Branch angewandt.</span><span class="sxs-lookup"><span data-stu-id="8786a-134">This applies your changes directly to the branch instead of using a pull request.</span></span> <span data-ttu-id="8786a-135">Jetzt sind Sie fertig!</span><span class="sxs-lookup"><span data-stu-id="8786a-135">At this point, you're finished!</span></span>

     - <span data-ttu-id="8786a-136">**Erstellen Sie einen neuen Branch für diesen Commit und starten Sie einen Pull Request**. Dabei wird eine Eingabeaufforderung mit einem Standardnamen zum Erstellen eines neuen Branchs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8786a-136">**Create a new branch for this commit and start a pull request**, which prompts you with a default name to create a new branch.</span></span> <span data-ttu-id="8786a-137">Nachdem Sie auf **Propose file change** (Dateiänderung vorschlagen) geklickt haben, wird die Seite **Comparing changes** (Änderungen vergleichen) angezeigt, damit Sie Ihre Änderungen überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="8786a-137">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="8786a-138">Klicken Sie dann auf die Schaltfläche **Create pull request** (Pull Request erstellen), um Ihre Änderungen an die Pull Request-Warteschlange zu übermitteln, und fahren Sie mit dem [nächsten Abschnitt](#pull-request-processing) fort.</span><span class="sxs-lookup"><span data-stu-id="8786a-138">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="8786a-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8786a-139">Next steps</span></span>

- <span data-ttu-id="8786a-140">Fahren Sie mit den Artikeln zu Schreibgrundlagen fort, um mehr über Themen wie Markdown, Markdownerweiterungssyntax usw. zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="8786a-140">Continue to the "Writing essentials" articles to learn more about Markdown, Markdown extensions syntax, and more.</span></span>