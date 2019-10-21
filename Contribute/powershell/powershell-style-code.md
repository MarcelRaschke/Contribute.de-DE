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
# <a name="formatting-code-samples"></a>Formatieren der Codebeispiele

Die vorhandene Dokumentation hat im Laufe der Zeit mehrere Stile verwendet, und die Formatierungsregeln wurden mehrmals geändert. In der Dokumentation wird möglichst ein konsistenter Stil für PowerShell-Codeblöcke und Ausgaben eingehalten.

Markdown unterstützt zwei verschiedene Codestile:

- Codespannen (inline) – gekennzeichnet durch einen einfachen Backtick (`` ` ``). Verwendete Einrückung in einem Paragraphen anstelle eines eigenständigen Blocks. Diese Codestile werden am häufigsten bei Cmdlet-Namen verwendet. Weitere Informationen finden Sie unter [Formatieren der Befehle für Syntaxelementes](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Codeblöcke – ein mehrzeiliger Block umgeben von dreifachen Backticks(`` ``` ``).

## <a name="using-code-blocks"></a>Verwenden der Codeblöcke

Markdown ermöglicht dem Einzug einen Codeblock zu kennzeichnen, aber dieses Muster kann problematisch sein und sollte vermieden werden. Alle Codeblöcke sollten in einem Codefence enthalten sein. Ein Codefence ist ein Block aus Codes, der von dreifachen Backticks(`` ``` ``) umgeben ist. Die Codefencemarker müssen vor und nach dem Codebeispiel in einer eigenen Zeile stehen. Der Marker am Anfang des Codeblocks kann eine optionale Sprachbezeichnung aufweisen. Das Open Publishing System (OPS) von Microsoft verwendet die Sprachbezeichnung, um die Funktion der Syntaxhervorhebung zu unterstützen.

OPS fügt auch eine **Kopieren** -Schaltfläche hinzu, mit der der Inhalt des Codeblocks in die Zwischenablage kopiert wird. Dies ermöglicht es Ihnen, den Code schnell in ein Skript einzufügen, um das Codebeispiel zu testen. Es ist jedoch nicht möglich, alle Beispiele in der Dokumentation auf diese Weise auszuführen. Einige Codeblöcke können eine einfache Abbildung eines PowerShell-Konzepts oder eine abstrakte Darstellung der Syntax darstellen.

In der Dokumentation werden zwei Arten von Codeblöcken verwendet:

1. Anschauliche Beispiele
2. Ausführbare Beispiele

## <a name="formatting-illustrative-examples"></a>Formatieren anschaulicher Beispiele

Anschauliche Beispiele werden zur Erklärung eines PowerShell-Konzepts verwendet. Diese Beispiele sollten zur Ausführung nicht in die Zwischenablage kopiert werden. Diese werden am häufigsten für einfache Beispiele verwendet, die einfach zu schreiben sind.
Darüber hinaus werden diese auch für Syntaxbeispiele verwendet, in denen die Syntax eines Befehls veranschaulicht wird.

Anschauliche Beispiele verwenden einen „reinen“ Codefence, um den Anfang und das Ende eines Codeblocks zu markieren. Der Codeblock kann eine Beispielausgabe des dargestellten Befehls enthalten.

### <a name="syntax-block"></a>Syntaxblock

In diesem Beispiel werden alle möglichen Parameter des `Get-Command`-Cmdlets veranschaulicht.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

In diesem Beispiel wird die `for`-Anweisung in allgemeinen Begriffen beschrieben:

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Ein einfaches Beispiel zur Veranschaulichung

Im Folgenden Beispiel werden PowerShell-Vergleichsoperatoren dargestellt:

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

Beachten Sie, dass in diesem Beispiel die vereinfachte PowerShell-Eingabeaufforderung und die resultierende Ausgabe angezeigt wird. In diesem Fall ist es nicht beabsichtigt, dieses Beispiel zu kopieren und auszuführen.

## <a name="formatting-executable-examples"></a>Formatieren ausführbarer Beispiele

Bei komplexeren Beispielen oder Beispielen, die für das Kopieren und Ausführen hilfreich sind, sollte das folgende Markup im Blockstil verwenden:

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

Die von PowerShell-Befehlen angezeigte Ausgabe sollte in einen **Ausgabe**-Codeblock eingeschlossen werden, um die Syntaxhervorhebung zu verhindern. Beispiel:

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

Die **Ausgabe** -Codebezeichnung ist keine offizielle „Sprache“, die vom System für die Syntaxhervorhebung unterstützt wird.
Diese Bezeichnung ist jedoch nützlich, da OPS dem Codefeld auf der Website die Bezeichnung „Ausgabe“ hinzufügt.
Dieses Codefeld „Ausgabe“ hat keine Syntaxhervorhebung.

## <a name="coding-style-rules"></a>Codierungsstilregeln

### <a name="avoid-line-continuation-in-code-samples"></a>Vermeiden von Zeilenfortsetzungen in Codebeispielen

Vermeiden Sie Zeilenfortsetzungszeichen (`` ` ``) in PowerShell-Codebeispielen. Diese sind schwer zu erkennen und können Probleme verursachen, wenn am Ende der Zeile zusätzliche Leerzeichen vorhanden sind.

- Verwenden Sie PowerShell-Verteilung, um die Zeilenlänge für Cmdlets mit vielen Parametern zu verringern.
- Profitieren Sie von den Vorteilen der natürlichen Zeilenumbruchsmöglichkeiten von PowerShell, wie z. B. nach Pipezeichen (`|`), öffnenden geschweiften Klammern, Klammern und eckigen Klammern.

### <a name="avoid-using-powershell-prompts-in-examples"></a>Vermeiden Sie die Verwendung von PowerShell-Eingabeaufforderungen in Beispielen

Von der Verwendung der Eingabeaufforderungszeichenfolge wird abgeraten und sollte auf Szenarios beschränkt sein, die die Verwendung der Befehlszeile veranschaulichen. Eingabeaufforderungen sind für Beispiele erforderlich, die Befehle veranschaulichen, welche die Eingabeaufforderung ändern, oder wenn der angezeigte Pfad für das dargestellte Szenario maßgeblich ist.

- PowerShell-Eingabeaufforderungen sollten nur in anschaulichen Beispielen verwendet werden. In den meisten dieser Beispiele sollte die Eingabeaufforderungszeichenfolge „`PS>`“ lauten. Diese Eingabeaufforderung ist unabhängig von betriebssystemspezifischen Indikatoren.
- Eingabeaufforderungen sollten **NICHT** in ausführbaren Beispielen verwendet werden.

Im folgenden Beispiel wird veranschaulicht, wie die Eingabeaufforderung geändert wird, wenn der Registrierungsanbieter verwendet wird.

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

### <a name="do-not-use-aliases-in-examples"></a>Verwenden Sie in den Beispielen keine Alias.

Sie sollten immer den vollständigen Namen aller Cmdlets und Parameter verwenden, es sei denn, Sie meinen ausdrücklich Alias. Cmdlet-und Parameternamen müssen die richtige Pascal-Schreibweise verwenden, die im Code definiert ist.

### <a name="using-parameters-in-examples"></a>Verwenden der Parameter in Beispielen

Vermeiden Sie Positionsparameter. Im Allgemeinen sollten Sie immer den Parameternamen in einem Beispiel einschließen, auch wenn es sich um einen positionellen Parameter handelt. Dadurch kommt es zu weniger Verwirrung in Ihren Beispielen.
