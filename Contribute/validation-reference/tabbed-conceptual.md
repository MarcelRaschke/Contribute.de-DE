---
ms.date: 03/29/2019
title: Konzeptdarstellungen im Registerkartenformat
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841300"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="12efe-102">Konzeptdarstellungen im Registerkartenformat</span><span class="sxs-lookup"><span data-stu-id="12efe-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12efe-103">Die Syntax für Konzeptdarstellungen im Registerkartenformat ist veraltet. Es sollten also keine neuen Registerkarten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="12efe-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="12efe-104">Die in diesem Artikel beschriebenen Überprüfungen gelten für Inhalte, die Konzeptdarstellungen im Registerkartenformat so lange verwenden dürfen, bis die Ersatzfunktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12efe-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="12efe-105">Registerkartensyntax</span><span class="sxs-lookup"><span data-stu-id="12efe-105">Tab syntax</span></span>

<span data-ttu-id="12efe-106">Die Syntax für Registerkarten sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="12efe-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="12efe-107">Registerkarte mit einer Ebene:</span><span class="sxs-lookup"><span data-stu-id="12efe-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="12efe-108">Optional abhängige Registerkarte:</span><span class="sxs-lookup"><span data-stu-id="12efe-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="12efe-109">Beispiel eines Registerkartenabschnitts mit einer Ebene mit zwei Registerkarten und dem Abschlusszeichen für die Registerkartengruppe (---):</span><span class="sxs-lookup"><span data-stu-id="12efe-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="12efe-110">Registerkarten können optional sekundäre Registerkarten oder Registerkarten für Abhängigkeiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="12efe-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="12efe-111">Dadurch werden Registerkarten von der Auswahl in einer anderen Registerkartenreihe abhängig.</span><span class="sxs-lookup"><span data-stu-id="12efe-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="12efe-112">Hier sehen Sie ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="12efe-112">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="12efe-113">Es gelten die folgenden Überprüfungen für die Registerkartensyntax:</span><span class="sxs-lookup"><span data-stu-id="12efe-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="12efe-114">Die Registerkartensyntax muss richtig sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="12efe-115">Abhängige Registerkarten müssen in einer vorherigen Registerkartengruppe definiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="12efe-116">Es ist nur eine Abhängigkeitsebene zulässig.</span><span class="sxs-lookup"><span data-stu-id="12efe-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="12efe-117">Es dürfen nicht weniger als zwei Registerkarten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="12efe-118">Es dürfen nicht mehr als vier Registerkarten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="12efe-119">Registerkarten müssen genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="12efe-119">Tabs must be approved.</span></span>
- <span data-ttu-id="12efe-120">Registerkarten- bzw. ID-Paare müssen gültig sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="12efe-121">In einer Registerkartengruppe darf die gleiche Registerkarten-ID nicht mehrfach vorkommen.</span><span class="sxs-lookup"><span data-stu-id="12efe-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="12efe-122">Genehmigte Registerkarten</span><span class="sxs-lookup"><span data-stu-id="12efe-122">Approved tabs</span></span>

<span data-ttu-id="12efe-123">Die folgenden Paare aus Registerkartenname und Registerkarten-ID wurden genehmigt.</span><span class="sxs-lookup"><span data-stu-id="12efe-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="12efe-124">IDs von abhängigen Registerkarten werden nicht gekoppelt, müssen jedoch gemäß der Spalte „Registerkarten-ID“ gültig sein.</span><span class="sxs-lookup"><span data-stu-id="12efe-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="12efe-125">Bei den Werten wird Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="12efe-125">The values are case-sensitive</span></span>

|<span data-ttu-id="12efe-126">Registerkartenname</span><span class="sxs-lookup"><span data-stu-id="12efe-126">Tab name</span></span>              |<span data-ttu-id="12efe-127">Registerkarten-ID</span><span class="sxs-lookup"><span data-stu-id="12efe-127">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |