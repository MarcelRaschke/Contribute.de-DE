---
title: Sortieren von Umleitungen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie Umleitungen mit dem Docs Authoring Pack, Visual Studio Code-Erweiterung, sortieren.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336679"
---
# <a name="sort-redirects"></a><span data-ttu-id="f762d-103">Sortieren von Umleitungen</span><span class="sxs-lookup"><span data-stu-id="f762d-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="f762d-104">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f762d-104">Summary</span></span>

<span data-ttu-id="f762d-105">Bei der Entwicklung eines docs.Microsoft.com-Dokumentationssatzes (Docset) werden einige Markdowndateien letztlich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f762d-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="f762d-106">Wenn eine Markdowndatei gelöscht wurde, müssen wir eine Umleitung bereitstellen, damit jeder Verweis auf den gelöschten Artikel über die Umleitung ordnungsgemäß aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f762d-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="f762d-107">Umleitungen werden in der Datei *.openpublishing.redirection.json* angegeben.</span><span class="sxs-lookup"><span data-stu-id="f762d-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="f762d-108">Öffnen Sie die Befehlspalette, und drücken Sie <kbd>F1</kbd> (oder unter macOS <kbd>⇧⌘P</kbd>).</span><span class="sxs-lookup"><span data-stu-id="f762d-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="f762d-109">Geben Sie ein: **Docs: Masterumleitungsdatei sortieren**</span><span class="sxs-lookup"><span data-stu-id="f762d-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="f762d-110">Wählen Sie den Befehl zur Ausführung aus.</span><span class="sxs-lookup"><span data-stu-id="f762d-110">Select the command to execute it</span></span>
1. <span data-ttu-id="f762d-111">Beachten Sie Änderungen an der Datei *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="f762d-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="f762d-112">Überlegungen</span><span class="sxs-lookup"><span data-stu-id="f762d-112">Considerations</span></span>

<span data-ttu-id="f762d-113">Das Konzept von „Daisy Chaining“ besteht darin, wie die Datei *.openpublishing.redirection.json* ursprünglich entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="f762d-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="f762d-114">Im Laufe der Zeit veralten letztlich Dateien, die als Umleitung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f762d-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="f762d-115">Dies geschieht, wenn Datei A gelöscht wird und eine Umleitung zu Datei B erforderlich ist, später Datei B gelöscht wird und dann zu Datei C umgeleitet wird. Im Idealfall würden beide Einträge auf C verweisen, sodass A zu C umgeleitet wird und B unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="f762d-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="f762d-116">Dies ist ein geringfügiger Leistungsgewinn, und das Feature wird derzeit aktiv bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="f762d-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="f762d-117">In Aktion</span><span class="sxs-lookup"><span data-stu-id="f762d-117">In action</span></span>

<span data-ttu-id="f762d-118">Nachstehend sehen Sie eine kurze Demo dieses Features.</span><span class="sxs-lookup"><span data-stu-id="f762d-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="f762d-119">[![Demo zum Sortieren von Umleitungen](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f762d-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
