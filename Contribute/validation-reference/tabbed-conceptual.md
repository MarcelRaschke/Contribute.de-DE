# <a name="tabbed-conceptual"></a><span data-ttu-id="dbf1e-101">Konzeptdarstellungen im Registerkartenformat</span><span class="sxs-lookup"><span data-stu-id="dbf1e-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbf1e-102">Die Syntax für Konzeptdarstellungen im Registerkartenformat ist veraltet. Es sollten also keine neuen Registerkarten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="dbf1e-103">Die in diesem Artikel beschriebenen Überprüfungen gelten für Inhalte, die Konzeptdarstellungen im Registerkartenformat so lange verwenden dürfen, bis die Ersatzfunktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="dbf1e-104">Registerkartensyntax</span><span class="sxs-lookup"><span data-stu-id="dbf1e-104">Tab syntax</span></span>

<span data-ttu-id="dbf1e-105">Die Syntax für Registerkarten sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="dbf1e-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="dbf1e-106">Registerkarte mit einer Ebene:</span><span class="sxs-lookup"><span data-stu-id="dbf1e-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="dbf1e-107">Optional abhängige Registerkarte:</span><span class="sxs-lookup"><span data-stu-id="dbf1e-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="dbf1e-108">Beispiel eines Registerkartenabschnitts mit einer Ebene mit zwei Registerkarten und dem Abschlusszeichen für die Registerkartengruppe (---):</span><span class="sxs-lookup"><span data-stu-id="dbf1e-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="dbf1e-109">Registerkarten können optional sekundäre Registerkarten oder Registerkarten für Abhängigkeiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="dbf1e-110">Dadurch werden Registerkarten von der Auswahl in einer anderen Registerkartenreihe abhängig.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="dbf1e-111">Hier sehen Sie ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dbf1e-111">Here's an example:</span></span>

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

<span data-ttu-id="dbf1e-112">Es gelten die folgenden Überprüfungen für die Registerkartensyntax:</span><span class="sxs-lookup"><span data-stu-id="dbf1e-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="dbf1e-113">Die Registerkartensyntax muss richtig sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="dbf1e-114">Abhängige Registerkarten müssen in einer vorherigen Registerkartengruppe definiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="dbf1e-115">Es ist nur eine Abhängigkeitsebene zulässig.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="dbf1e-116">Es dürfen nicht weniger als zwei Registerkarten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="dbf1e-117">Es dürfen nicht mehr als vier Registerkarten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="dbf1e-118">Registerkarten müssen sich auf der Whitelist befinden.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="dbf1e-119">Registerkarten- bzw. ID-Paare müssen gültig sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="dbf1e-120">In einer Registerkartengruppe darf die gleiche Registerkarten-ID nicht mehrfach vorkommen.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="dbf1e-121">Registerkartenwhitelist</span><span class="sxs-lookup"><span data-stu-id="dbf1e-121">Tab whitelist</span></span>

<span data-ttu-id="dbf1e-122">Die folgenden Registerkartennamen- und Registerkarten-ID-Paare befinden sich auf der Whitelist.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="dbf1e-123">IDs von abhängigen Registerkarten werden nicht gekoppelt, müssen jedoch gemäß der Spalte „Registerkarten-ID“ gültig sein.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="dbf1e-124">Bei den Werten wird Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="dbf1e-124">The values are case-sensitive</span></span>

|<span data-ttu-id="dbf1e-125">Registerkartenname</span><span class="sxs-lookup"><span data-stu-id="dbf1e-125">Tab name</span></span>              |<span data-ttu-id="dbf1e-126">Registerkarten-ID</span><span class="sxs-lookup"><span data-stu-id="dbf1e-126">Tab ID</span></span>            |
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