---
title: Spezifischer Leitfaden zum Schreiben der Cmdlet-Referenz
description: Dieser Artikel enthält spezifische Regeln zum Formatieren von PowerShell-Codebeispielen. Dies gilt für konzeptionelle Artikel mit Beispielen sowie für die Cmdlet-Referenz.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290286"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="1a5dd-104">Aktualisieren von Referenzartikeln</span><span class="sxs-lookup"><span data-stu-id="1a5dd-104">Updating reference articles</span></span>

<span data-ttu-id="1a5dd-105">Cmdlet-Referenzartikel weisen eine bestimmte Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="1a5dd-106">Diese Struktur wird von [PlatyPS][] definiert.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="1a5dd-107">PlatyPS ist das Tool, das zum Generieren von Cmdlet-Hilfe für PowerShell-Module verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="1a5dd-108">PlatyPS erstellt die grundlegende Markdowndatei für ein Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="1a5dd-109">Nachdem die Markdowndateien bearbeitet wurden, wird PlatyPS zum Erstellen der MAML-Hilfsdateien für das Cmdlet `Get-Help` verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="1a5dd-110">PlatyPS verfügt über ein hartcodiertes Schema für Cmdlet-Referenzen, das im Code enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="1a5dd-111">Im Dokument [platyPS.schema.md][] wird diese Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="1a5dd-112">Verstöße gegen das Schema führen zu Buildfehlern, die behoben werden müssen, bevor Ihr Beitrag akzeptiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="1a5dd-113">Allgemeine Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1a5dd-113">General guidelines</span></span>

- <span data-ttu-id="1a5dd-114">Entfernen Sie keine der Überschriftstrukturen.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="1a5dd-115">PlatyPS erwartet spezifische Überschriften.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="1a5dd-116">Die Header **Input type** (Eingabetyp) und **Output type** (Ausgabetyp) müssen einen Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="1a5dd-117">Wenn das Cmdlet keine Eingaben akzeptiert oder keinen Wert zurückgibt, verwenden Sie den Wert „None“ (Keiner).</span><span class="sxs-lookup"><span data-stu-id="1a5dd-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="1a5dd-118">Umgrenzte Codeblöcke sind nur im Abschnitt [Beispiele](#format-for-examples) zulässig.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="1a5dd-119">Inlinecodespannen können in allen Absätzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="1a5dd-120">Formatieren von „About_“-Dateien</span><span class="sxs-lookup"><span data-stu-id="1a5dd-120">Formatting About_ files</span></span>

<span data-ttu-id="1a5dd-121">`About_*`-Dateien werden nun von [Pandoc][] anstelle von PlatyPS verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="1a5dd-122">`About_*`-Dateien werden für die bestmögliche Kompatibilität mit allen Versionen von PowerShell und den Veröffentlichungstools formatiert.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="1a5dd-123">Nehmen Sie keine Änderungen an der Formatierung von `about_*`-Dateien vor, ohne dies mit einem Entwickler des Repositorys zu klären.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="1a5dd-124">Grundlegende Formatierungsrichtlinien:</span><span class="sxs-lookup"><span data-stu-id="1a5dd-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="1a5dd-125">Beschränken Sie die Zeilen auf 80 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="1a5dd-126">Codeblöcke, Blockzitate und Tabellen werden auf 76 Zeichen beschränkt, da Pandoc bei der Konvertierung Einzüge mit vier Leerzeichen für diese einfügt.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="1a5dd-127">Tabellen müssen in 76 Zeichen passen.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="1a5dd-128">Umschließen Sie Inhalte von Zellen in mehreren Zeilen manuell.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="1a5dd-129">Verwenden Sie öffnende und schließende `|`-Zeichen in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="1a5dd-130">Ein funktionierendes Beispiel finden Sie unter [about_Comparison_Operators][about-example].</span><span class="sxs-lookup"><span data-stu-id="1a5dd-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="1a5dd-131">Bei der Verwendung der Sonderzeichen `\`, `$`, `` ` `` und `<` von Pandoc:</span><span class="sxs-lookup"><span data-stu-id="1a5dd-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="1a5dd-132">In einer Überschrift: müssen diese Zeichen mit einem voranstehenden `\`-Escapezeichen versehen werden.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="1a5dd-133">In einem Absatz: müssen diese Zeichen in Codespannen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="1a5dd-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1a5dd-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="1a5dd-135">Formatierung von Beispielen</span><span class="sxs-lookup"><span data-stu-id="1a5dd-135">Format for examples</span></span>

<span data-ttu-id="1a5dd-136">Im PlatyPS-Schema ist die Überschrift **EXAMPLES** eine H2-Überschrift, und alle Beispiele sind H3-Überschriften.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="1a5dd-137">Das Schema lässt nicht zu, dass Codeblöcke in einem Beispiel durch Absätze getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="1a5dd-138">Das folgende Schema ist gültig:</span><span class="sxs-lookup"><span data-stu-id="1a5dd-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="1a5dd-139">Geben Sie für alle Beispiele eine Zahl und einen kurzen Titel an.</span><span class="sxs-lookup"><span data-stu-id="1a5dd-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="1a5dd-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1a5dd-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org