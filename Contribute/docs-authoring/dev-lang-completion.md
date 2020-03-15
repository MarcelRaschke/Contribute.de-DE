---
title: Vervollständigung von Entwicklungssprachen – Docs Authoring Pack
description: Hier erfahren Sie, wie die Vervollständigung von Entwicklungssprachen Mitwirkende im Docs Authoring Pack, Visual Studio Code-Erweiterung, unterstützt.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336794"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="94980-103">Vervollständigung von Entwicklungssprachen</span><span class="sxs-lookup"><span data-stu-id="94980-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="94980-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="94980-104">Summary</span></span>

<span data-ttu-id="94980-105">Mitwirkende benötigen Unterstützung bei der Ermittlung der gültigen Sprach-IDs (Entwicklungssprachen), die in einer Markdowndatei auf Dreifach-Graviszeichen (Codefenceöffnungen) folgen können.</span><span class="sxs-lookup"><span data-stu-id="94980-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="94980-106">Leider gibt es keine Überprüfung von Entwicklungssprachen zur Buildzeit.</span><span class="sxs-lookup"><span data-stu-id="94980-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="94980-107">Das Ergebnis deshalb: unterschiedliche Darstellungen einer einzelnen Sprache innerhalb desselben konzeptionellen Dokumentationssatzes (Docset).</span><span class="sxs-lookup"><span data-stu-id="94980-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="94980-108">Sehen Sie sich C# als Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="94980-108">Consider C# as an example.</span></span> <span data-ttu-id="94980-109">Mitwirkende haben unter anderem `c#`, `C#`, `cs`, `csharp` als Entwicklungssprachendarstellungen der Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="94980-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="94980-110">Welche der vorstehenden Darstellungen ist richtig?</span><span class="sxs-lookup"><span data-stu-id="94980-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="94980-111">Das Feature zur *Vervollständigung von Entwicklungssprachen* beseitigt die Möglichkeit einer Verwechslung durch die Anzeige einer Liste von bekannten Entwicklungssprachen.</span><span class="sxs-lookup"><span data-stu-id="94980-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="94980-112">Nachdem Sie den Namen einer Entwicklungssprache aus IntelliSense ausgewählt haben, geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94980-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="94980-113">Der Codefence wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="94980-113">The code fence is closed.</span></span>
* <span data-ttu-id="94980-114">Der Textcursor wird im Codefence positioniert.</span><span class="sxs-lookup"><span data-stu-id="94980-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="94980-115">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="94980-115">Preferences</span></span>

<span data-ttu-id="94980-116">Dieses Feature kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="94980-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="94980-117">Die folgenden Einstellungen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="94980-117">The following settings are available:</span></span>

* [<span data-ttu-id="94980-118">Häufig verwendete Entwicklungssprachen anzeigen</span><span class="sxs-lookup"><span data-stu-id="94980-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="94980-119">Alle bekannten Entwicklungssprachen anzeigen</span><span class="sxs-lookup"><span data-stu-id="94980-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="94980-120">Häufig verwendete Entwicklungssprachen anzeigen</span><span class="sxs-lookup"><span data-stu-id="94980-120">Display commonly used dev langs</span></span>

<span data-ttu-id="94980-121">In einem einzelnen Dokumentationssatz (Docset) wird nur eine Teilmenge der gültigen Entwicklungssprachen verwendet.</span><span class="sxs-lookup"><span data-stu-id="94980-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="94980-122">So verbessern Sie die Benutzerleistung:</span><span class="sxs-lookup"><span data-stu-id="94980-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="94980-123">Öffnen Sie in Visual Studio Code den Dokumentationssatz im Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="94980-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="94980-124">Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.</span><span class="sxs-lookup"><span data-stu-id="94980-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="94980-125">Klicken Sie auf den Link **In „settings.json“ bearbeiten**  im Abschnitt **Markdown: Docset-Sprachen**.</span><span class="sxs-lookup"><span data-stu-id="94980-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="94980-126">Fügen Sie die folgende `markdown.docsetLanguages`-Eigenschaft zur Datei *settings.json* hinzu:</span><span class="sxs-lookup"><span data-stu-id="94980-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="94980-127">Positionieren Sie den Textcursor im leeren Array der Eigenschaft, und aktivieren Sie IntelliSense (über <kbd>STRG</kbd> + <kbd>LEERTASTE</kbd>).</span><span class="sxs-lookup"><span data-stu-id="94980-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="94980-128">Daraufhin wird eine Liste bekannter Namen von Entwicklungssprachen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94980-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="94980-129">Fügen Sie so viele Namen zum Array hinzu, bis Ihnen die Liste zusagt.</span><span class="sxs-lookup"><span data-stu-id="94980-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="94980-130">Beispielsweise zeigt die folgende Liste dem Benutzer nach der Eingabe von Dreifach-Graviszeichen vier Namen von Entwicklungssprachen an:</span><span class="sxs-lookup"><span data-stu-id="94980-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="94980-131">Speichern Sie Ihre Änderungen an der Datei *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="94980-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="94980-132">Ein leeres `markdown.docsetLanguages`-Array bewirkt, dass alle bekannten Entwicklungssprachen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="94980-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="94980-133">Alle bekannten Entwicklungssprachen anzeigen</span><span class="sxs-lookup"><span data-stu-id="94980-133">Display all known dev langs</span></span>

<span data-ttu-id="94980-134">Standardmäßig werden in IntelliSense alle bekannten Namen von Entwicklungssprachen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94980-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="94980-135">Diese Einstellung überschreibt die in [Häufig verwendete Entwicklungssprachen](#display-commonly-used-dev-langs) beschriebene Eigenschaft `markdown.docsetLanguages`.</span><span class="sxs-lookup"><span data-stu-id="94980-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="94980-136">So ändern Sie diese Einstellung:</span><span class="sxs-lookup"><span data-stu-id="94980-136">To change this setting:</span></span>

1. <span data-ttu-id="94980-137">Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.</span><span class="sxs-lookup"><span data-stu-id="94980-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="94980-138">Schalten Sie die Einstellung im Abschnitt **Markdown: Alle verfügbaren Sprachen** um.</span><span class="sxs-lookup"><span data-stu-id="94980-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="94980-139">In Aktion</span><span class="sxs-lookup"><span data-stu-id="94980-139">In action</span></span>

<span data-ttu-id="94980-140">Nachstehend sehen Sie eine kurze Demo dieses Features:</span><span class="sxs-lookup"><span data-stu-id="94980-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="94980-141">[![Vervollständigung von Entwicklungssprachen](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="94980-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
