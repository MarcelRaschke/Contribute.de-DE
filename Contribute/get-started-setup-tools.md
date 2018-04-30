---
title: Installieren von Tools für die Inhaltsentwicklung
description: In diesem Artikel werden das Herunterladen und Installieren der Clienttools erläutert, die Sie für Git und das Bearbeiten von Markdowndateien benötigen.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="76067-103">Installieren von Tools für die Inhaltsentwicklung</span><span class="sxs-lookup"><span data-stu-id="76067-103">Install content authoring tools</span></span>

<span data-ttu-id="76067-104">Dieser Artikel beschreibt die Schritte, die erforderlich sind, um Git-Clienttools und Visual Studio Code interaktiv zu installieren.</span><span class="sxs-lookup"><span data-stu-id="76067-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="76067-105">Installieren von [Git für Windows](https://git-scm.com/download/win)</span><span class="sxs-lookup"><span data-stu-id="76067-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="76067-106">Installieren von [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="76067-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="76067-107">Wenn Sie nur geringfügige Änderungen an einem Artikel vornehmen, müssen Sie die in diesem Artikel erläuterten Schritte *nicht* durchführen und können direkt mit dem Workflow für [schnelle Änderungen](index.md#quick-edits-to-existing-documents) fortfahren.</span><span class="sxs-lookup"><span data-stu-id="76067-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="76067-108">Wichtige Mitwirkende sollten diese Schritte ausführen, da ihnen dadurch die Verwendung des [Workflows für größere Änderungen oder Änderungen mit langer Ausführungszeit](how-to-write-workflows-major.md) ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="76067-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="76067-109">Auch wenn Sie über Schreibberechtigungen im Hauptrepository verfügen, *wird ausdrücklich empfohlen, das Repository zu forken und zu klonen (dies wird in diesem Leitfaden vorausgesetzt)*, damit Sie über die Schreib- bzw. Leseberechtigungen verfügen, um vorgeschlagene Änderungen in Ihrem Fork zu speichern.</span><span class="sxs-lookup"><span data-stu-id="76067-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="76067-110">Installieren der Git-Clienttools unter Windows</span><span class="sxs-lookup"><span data-stu-id="76067-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="76067-111">Installieren Sie die aktuelle Version der [Git-Clienttools von Software Freedom](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="76067-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="76067-112">Die Installation umfasst das Versionskontrollsystem von Git sowie Git Bash, die Befehlszeilen-App, die Sie zur Interaktion mit Ihrem lokalen Git-Repository verwenden.</span><span class="sxs-lookup"><span data-stu-id="76067-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="76067-113">Wenn Sie eine grafische Benutzeroberfläche (Graphical User Interface, GUI) gegenüber einer Befehlszeilenschnittstelle (Command-Line Interface, CLI) vorziehen, finden Sie einige gängige Optionen auf der [Seite zu GUI Clients von Software Freedom Conservancy](https://git-scm.com/downloads/guis), unter [GitHub Desktop auf GitHub](https://desktop.github.com/) oder [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).</span><span class="sxs-lookup"><span data-stu-id="76067-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="76067-114">Befolgen Sie die Anweisungen für die Installation und Konfiguration für Ihren Client.</span><span class="sxs-lookup"><span data-stu-id="76067-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="76067-115">Im nächsten Artikel geht es um das [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="76067-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="76067-116">Hier finden Sie weitere Git-Ressourcen (in englischer Sprache): [Git-Terminologie](https://help.github.com/articles/github-glossary) | [Git-Grundlagen](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Lernressourcen für Git und GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="76067-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="76067-117">Grundlegendes zu Markdown-Editoren</span><span class="sxs-lookup"><span data-stu-id="76067-117">Understand Markdown editors</span></span>

<span data-ttu-id="76067-118">Markdown ist eine leichte Markupsprache, die sowohl einfach zu lesen als auch zu lernen ist.</span><span class="sxs-lookup"><span data-stu-id="76067-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="76067-119">Aus diesem Grund ist sie schnell zu einem Branchenstandard geworden.</span><span class="sxs-lookup"><span data-stu-id="76067-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="76067-120">Um Artikel in Markdown zu schreiben, sollten Sie zuerst einen Markdown-Editor herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="76067-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="76067-121">[Visual Studio Code](https://code.visualstudio.com/) ist das bei Microsoft bevorzugte Tool zum Bearbeiten von Markdown.</span><span class="sxs-lookup"><span data-stu-id="76067-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="76067-122">[Atom](https://atom.io) ist ein weiteres beliebtes Tool für die Markdownbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="76067-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="76067-123">Markdowntext wird in Dateien mit der Erweiterung „MD“ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76067-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="76067-124">Nähere Informationen zum Schreiben mit Markdown, inklusive der Grundlagen von Markdown und der von benutzerdefinierten OPS-Markdownerweiterungen unterstützten Features werden später im Artikel [Verwenden von Markdown](how-to-write-use-markdown.md) behandelt.</span><span class="sxs-lookup"><span data-stu-id="76067-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="76067-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="76067-125">Visual Studio Code</span></span>

<span data-ttu-id="76067-126">[Visual Studio Code](https://code.visualstudio.com/), auch als VS Code bezeichnet, ist ein schlanker Editor, der unter Windows, Linux und Mac verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="76067-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="76067-127">Er umfasst die Git-Integration sowie Unterstützung für Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="76067-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="76067-128">Laden Sie [VS Code](https://code.visualstudio.com/) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="76067-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="76067-129">Die VS Code-Startseite sollte Ihr Betriebssystem erkennen.</span><span class="sxs-lookup"><span data-stu-id="76067-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="76067-130">Windows</span><span class="sxs-lookup"><span data-stu-id="76067-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="76067-131">Mac</span><span class="sxs-lookup"><span data-stu-id="76067-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="76067-132">Linux</span><span class="sxs-lookup"><span data-stu-id="76067-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="76067-133">Um VS Code zu starten und den aktuellen Ordner zu öffnen, führen Sie den Befehl `code .` an der Befehlszeile oder in der Bash-Shell aus.</span><span class="sxs-lookup"><span data-stu-id="76067-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="76067-134">Wenn der aktuelle Ordner zu einem lokalen Git-Repository gehört, wird die GitHub-Integration automatisch in Visual Studio Code angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76067-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="76067-135">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="76067-135">Next steps</span></span>

<span data-ttu-id="76067-136">Jetzt sind Sie bereit zum [Einrichten eines lokalen Git-Repositorys](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="76067-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
