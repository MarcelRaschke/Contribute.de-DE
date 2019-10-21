---
title: Spezifischer Leitfaden zum Schreiben von Skriptbeispielen
description: Dieser Artikel enthält spezifische Regeln zum Formatieren von PowerShell-Codebeispielen. Dies gilt für konzeptionelle Artikel mit Beispielen sowie für die Cmdlet-Referenz.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290263"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="3e47b-104">Formatieren der Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="3e47b-104">Formatting code samples</span></span>

<span data-ttu-id="3e47b-105">Die vorhandene Dokumentation hat im Laufe der Zeit mehrere Stile verwendet, und die Formatierungsregeln wurden mehrmals geändert.</span><span class="sxs-lookup"><span data-stu-id="3e47b-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="3e47b-106">In der Dokumentation wird möglichst ein konsistenter Stil für PowerShell-Codeblöcke und Ausgaben eingehalten.</span><span class="sxs-lookup"><span data-stu-id="3e47b-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="3e47b-107">Markdown unterstützt zwei verschiedene Codestile:</span><span class="sxs-lookup"><span data-stu-id="3e47b-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="3e47b-108">Codespannen (inline) – gekennzeichnet durch einen einfachen Backtick (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="3e47b-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="3e47b-109">Verwendete Einrückung in einem Paragraphen anstelle eines eigenständigen Blocks.</span><span class="sxs-lookup"><span data-stu-id="3e47b-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="3e47b-110">Diese Codestile werden am häufigsten bei Cmdlet-Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e47b-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="3e47b-111">Weitere Informationen finden Sie unter [Formatieren der Befehle für Syntaxelementes](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="3e47b-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="3e47b-112">Codeblöcke – ein mehrzeiliger Block umgeben von dreifachen Backticks(`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="3e47b-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="3e47b-113">Verwenden der Codeblöcke</span><span class="sxs-lookup"><span data-stu-id="3e47b-113">Using code blocks</span></span>

<span data-ttu-id="3e47b-114">Markdown ermöglicht dem Einzug einen Codeblock zu kennzeichnen, aber dieses Muster kann problematisch sein und sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="3e47b-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="3e47b-115">Alle Codeblöcke sollten in einem Codefence enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3e47b-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="3e47b-116">Ein Codefence ist ein Block aus Codes, der von dreifachen Backticks(`` ``` ``) umgeben ist.</span><span class="sxs-lookup"><span data-stu-id="3e47b-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="3e47b-117">Die Codefencemarker müssen vor und nach dem Codebeispiel in einer eigenen Zeile stehen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="3e47b-118">Der Marker am Anfang des Codeblocks kann eine optionale Sprachbezeichnung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="3e47b-119">Das Open Publishing System (OPS) von Microsoft verwendet die Sprachbezeichnung, um die Funktion der Syntaxhervorhebung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="3e47b-120">OPS fügt auch eine **Kopieren** -Schaltfläche hinzu, mit der der Inhalt des Codeblocks in die Zwischenablage kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e47b-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="3e47b-121">Dies ermöglicht es Ihnen, den Code schnell in ein Skript einzufügen, um das Codebeispiel zu testen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="3e47b-122">Es ist jedoch nicht möglich, alle Beispiele in der Dokumentation auf diese Weise auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="3e47b-123">Einige Codeblöcke können eine einfache Abbildung eines PowerShell-Konzepts oder eine abstrakte Darstellung der Syntax darstellen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="3e47b-124">In der Dokumentation werden zwei Arten von Codeblöcken verwendet:</span><span class="sxs-lookup"><span data-stu-id="3e47b-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="3e47b-125">Anschauliche Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e47b-125">Illustrative examples</span></span>
2. <span data-ttu-id="3e47b-126">Ausführbare Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e47b-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="3e47b-127">Formatieren anschaulicher Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e47b-127">Formatting illustrative examples</span></span>

<span data-ttu-id="3e47b-128">Anschauliche Beispiele werden zur Erklärung eines PowerShell-Konzepts verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e47b-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="3e47b-129">Diese Beispiele sollten zur Ausführung nicht in die Zwischenablage kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e47b-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="3e47b-130">Diese werden am häufigsten für einfache Beispiele verwendet, die einfach zu schreiben sind.</span><span class="sxs-lookup"><span data-stu-id="3e47b-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="3e47b-131">Darüber hinaus werden diese auch für Syntaxbeispiele verwendet, in denen die Syntax eines Befehls veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="3e47b-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="3e47b-132">Anschauliche Beispiele verwenden einen „reinen“ Codefence, um den Anfang und das Ende eines Codeblocks zu markieren.</span><span class="sxs-lookup"><span data-stu-id="3e47b-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="3e47b-133">Der Codeblock kann eine Beispielausgabe des dargestellten Befehls enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e47b-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="3e47b-134">Syntaxblock</span><span class="sxs-lookup"><span data-stu-id="3e47b-134">Syntax block</span></span>

<span data-ttu-id="3e47b-135">In diesem Beispiel werden alle möglichen Parameter des `Get-Command`-Cmdlets veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3e47b-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="3e47b-136">In diesem Beispiel wird die `for`-Anweisung in allgemeinen Begriffen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3e47b-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="3e47b-137">Ein einfaches Beispiel zur Veranschaulichung</span><span class="sxs-lookup"><span data-stu-id="3e47b-137">Simple illustration example</span></span>

<span data-ttu-id="3e47b-138">Im Folgenden Beispiel werden PowerShell-Vergleichsoperatoren dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3e47b-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="3e47b-139">Beachten Sie, dass in diesem Beispiel die vereinfachte PowerShell-Eingabeaufforderung und die resultierende Ausgabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3e47b-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="3e47b-140">In diesem Fall ist es nicht beabsichtigt, dieses Beispiel zu kopieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="3e47b-141">Formatieren ausführbarer Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e47b-141">Formatting executable examples</span></span>

<span data-ttu-id="3e47b-142">Bei komplexeren Beispielen oder Beispielen, die für das Kopieren und Ausführen hilfreich sind, sollte das folgende Markup im Blockstil verwenden:</span><span class="sxs-lookup"><span data-stu-id="3e47b-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="3e47b-143">Die von PowerShell-Befehlen angezeigte Ausgabe sollte in einen **Ausgabe**-Codeblock eingeschlossen werden, um die Syntaxhervorhebung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3e47b-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="3e47b-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3e47b-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="3e47b-145">Die **Ausgabe** -Codebezeichnung ist keine offizielle „Sprache“, die vom System für die Syntaxhervorhebung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3e47b-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="3e47b-146">Diese Bezeichnung ist jedoch nützlich, da OPS dem Codefeld auf der Website die Bezeichnung „Ausgabe“ hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3e47b-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="3e47b-147">Dieses Codefeld „Ausgabe“ hat keine Syntaxhervorhebung.</span><span class="sxs-lookup"><span data-stu-id="3e47b-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="3e47b-148">Codierungsstilregeln</span><span class="sxs-lookup"><span data-stu-id="3e47b-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="3e47b-149">Vermeiden von Zeilenfortsetzungen in Codebeispielen</span><span class="sxs-lookup"><span data-stu-id="3e47b-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="3e47b-150">Vermeiden Sie Zeilenfortsetzungszeichen (`` ` ``) in PowerShell-Codebeispielen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="3e47b-151">Diese sind schwer zu erkennen und können Probleme verursachen, wenn am Ende der Zeile zusätzliche Leerzeichen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3e47b-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="3e47b-152">Verwenden Sie PowerShell-Verteilung, um die Zeilenlänge für Cmdlets mit vielen Parametern zu verringern.</span><span class="sxs-lookup"><span data-stu-id="3e47b-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="3e47b-153">Profitieren Sie von den Vorteilen der natürlichen Zeilenumbruchsmöglichkeiten von PowerShell, wie z. B. nach Pipezeichen (`|`), öffnenden geschweiften Klammern, Klammern und eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="3e47b-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="3e47b-154">Vermeiden Sie die Verwendung von PowerShell-Eingabeaufforderungen in Beispielen</span><span class="sxs-lookup"><span data-stu-id="3e47b-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="3e47b-155">Von der Verwendung der Eingabeaufforderungszeichenfolge wird abgeraten und sollte auf Szenarios beschränkt sein, die die Verwendung der Befehlszeile veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="3e47b-156">Eingabeaufforderungen sind für Beispiele erforderlich, die Befehle veranschaulichen, welche die Eingabeaufforderung ändern, oder wenn der angezeigte Pfad für das dargestellte Szenario maßgeblich ist.</span><span class="sxs-lookup"><span data-stu-id="3e47b-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="3e47b-157">PowerShell-Eingabeaufforderungen sollten nur in anschaulichen Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e47b-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="3e47b-158">In den meisten dieser Beispiele sollte die Eingabeaufforderungszeichenfolge „`PS>`“ lauten.</span><span class="sxs-lookup"><span data-stu-id="3e47b-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="3e47b-159">Diese Eingabeaufforderung ist unabhängig von betriebssystemspezifischen Indikatoren.</span><span class="sxs-lookup"><span data-stu-id="3e47b-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="3e47b-160">Eingabeaufforderungen sollten **NICHT** in ausführbaren Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e47b-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="3e47b-161">Im folgenden Beispiel wird veranschaulicht, wie die Eingabeaufforderung geändert wird, wenn der Registrierungsanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e47b-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="3e47b-162">Verwenden Sie in den Beispielen keine Alias.</span><span class="sxs-lookup"><span data-stu-id="3e47b-162">Do not use aliases in examples</span></span>

<span data-ttu-id="3e47b-163">Sie sollten immer den vollständigen Namen aller Cmdlets und Parameter verwenden, es sei denn, Sie meinen ausdrücklich Alias.</span><span class="sxs-lookup"><span data-stu-id="3e47b-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="3e47b-164">Cmdlet-und Parameternamen müssen die richtige Pascal-Schreibweise verwenden, die im Code definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e47b-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="3e47b-165">Verwenden der Parameter in Beispielen</span><span class="sxs-lookup"><span data-stu-id="3e47b-165">Using parameters in examples</span></span>

<span data-ttu-id="3e47b-166">Vermeiden Sie Positionsparameter.</span><span class="sxs-lookup"><span data-stu-id="3e47b-166">Avoid using positional parameters.</span></span> <span data-ttu-id="3e47b-167">Im Allgemeinen sollten Sie immer den Parameternamen in einem Beispiel einschließen, auch wenn es sich um einen positionellen Parameter handelt.</span><span class="sxs-lookup"><span data-stu-id="3e47b-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="3e47b-168">Dadurch kommt es zu weniger Verwirrung in Ihren Beispielen.</span><span class="sxs-lookup"><span data-stu-id="3e47b-168">This reduces the chance of confusion in your examples.</span></span>
