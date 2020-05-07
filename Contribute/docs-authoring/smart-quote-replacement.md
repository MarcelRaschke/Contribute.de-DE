---
title: Automatischer Austausch typografischer Anführungszeichen – Docs Authoring Pack
description: Hier erfahren Sie, wie typografische Anführungszeichen mithilfe des Docs Authoring Packs, Visual Studio Code-Erweiterung, automatisch ausgetauscht werden.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336702"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="0854e-103">Austausch typografischer Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="0854e-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0854e-104">Summary</span></span>

<span data-ttu-id="0854e-105">Inhaltsentwickler sind für die Erstellung einiger der fortschrittlichsten Features moderner Technologie und Intelligenz zuständig, doch unsere Tools bevorzugen heutzutage in Markdown die Verwendung von einfachen (') oder doppelten einfachen Anführungszeichen (").</span><span class="sxs-lookup"><span data-stu-id="0854e-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="0854e-106">Das Gegenteil dazu sind die typografischen Anführungszeichen („“).</span><span class="sxs-lookup"><span data-stu-id="0854e-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="0854e-107">Typografische Anführungszeichen sind in idealen Typografien üblich, werden bei Markdown und gerendertem HTML aber nicht bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="0854e-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="0854e-108">Ein Beispiel: Bei Ihrer Arbeit an einem Microsoft Word-Dokument haben Sie vielleicht Folgendes bemerkt: Wenn Sie die <kbd>UMSCHALTTASTE</kbd> gedrückt halten und ein <kbd>"</kbd> eingeben, ersetzt Word das Zeichen `"` schnell durch ein dem typografischen Anführungszeichen entsprechendes Zeichen `“`.</span><span class="sxs-lookup"><span data-stu-id="0854e-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="0854e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0854e-109">Description</span></span>        | <span data-ttu-id="0854e-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="0854e-110">Unicode</span></span>  | <span data-ttu-id="0854e-111">Typografisches Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-111">Smart Quote</span></span> | <span data-ttu-id="0854e-112">Austausch durch</span><span class="sxs-lookup"><span data-stu-id="0854e-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="0854e-113">Doppeltes linkes Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="0854e-114">Doppeltes rechtes Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="0854e-115">Einfaches linkes Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="0854e-116">Einfaches rechtes Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="0854e-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="0854e-117">Wenn Sie in einer Markdowndatei ( *\*.MD*) Text einfügen oder Inhalte aktualisieren, wertet dieses Feature den Inhalt aktiv aus und tauscht Werte automatisch entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="0854e-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="0854e-118">Das Feature zum Austausch von typografischen Anführungszeichen tauscht auch andere Zeichen aus, z. B. unter anderem: `©, ™, ®, •`, tiefgestellte und hochgestellte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0854e-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="0854e-119">Dies ist hilfreich beim Einfügen von Text aus Word-Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="0854e-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="0854e-120">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0854e-120">Preferences</span></span>

<span data-ttu-id="0854e-121">Dieses Feature ist optional; der Standardwert lautet aber `true`.</span><span class="sxs-lookup"><span data-stu-id="0854e-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="0854e-122">So schalten Sie dieses Feature ein oder aus:</span><span class="sxs-lookup"><span data-stu-id="0854e-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="0854e-123">Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.</span><span class="sxs-lookup"><span data-stu-id="0854e-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="0854e-124">Schalten Sie die Einstellung im Abschnitt **Markdown: Replace Smart Quotes** (Typografische Anführungszeichen austauschen) ein.</span><span class="sxs-lookup"><span data-stu-id="0854e-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="0854e-125">In Aktion</span><span class="sxs-lookup"><span data-stu-id="0854e-125">In action</span></span>

<span data-ttu-id="0854e-126">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="0854e-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="0854e-127">[![Demo zum Austausch typografischer Anführungszeichen](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0854e-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
