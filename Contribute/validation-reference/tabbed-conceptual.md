# <a name="tabbed-conceptual"></a>Konzeptdarstellungen im Registerkartenformat

> [!IMPORTANT]
> Die Syntax für Konzeptdarstellungen im Registerkartenformat ist veraltet. Es sollten also keine neuen Registerkarten hinzugefügt werden. Die in diesem Artikel beschriebenen Überprüfungen gelten für Inhalte, die Konzeptdarstellungen im Registerkartenformat so lange verwenden dürfen, bis die Ersatzfunktion verfügbar ist.

## <a name="tab-syntax"></a>Registerkartensyntax

Die Syntax für Registerkarten sieht wie folgt aus:

Registerkarte mit einer Ebene:

`# [Tab Display Name](#tab/tab-id)`

Optional abhängige Registerkarte:

`# [Tab Display Name](#tab/tab-id/tab-condition)`

Beispiel eines Registerkartenabschnitts mit einer Ebene mit zwei Registerkarten und dem Abschlusszeichen für die Registerkartengruppe (---):

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

Registerkarten können optional sekundäre Registerkarten oder Registerkarten für Abhängigkeiten enthalten. Dadurch werden Registerkarten von der Auswahl in einer anderen Registerkartenreihe abhängig. Hier sehen Sie ein Beispiel:

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

Es gelten die folgenden Überprüfungen für die Registerkartensyntax:

- Die Registerkartensyntax muss richtig sein.
- Abhängige Registerkarten müssen in einer vorherigen Registerkartengruppe definiert worden sein.
- Es ist nur eine Abhängigkeitsebene zulässig.
- Es dürfen nicht weniger als zwei Registerkarten vorhanden sein.
- Es dürfen nicht mehr als vier Registerkarten vorhanden sein.
- Registerkarten müssen sich auf der Whitelist befinden.
- Registerkarten- bzw. ID-Paare müssen gültig sein.
- In einer Registerkartengruppe darf die gleiche Registerkarten-ID nicht mehrfach vorkommen.

## <a name="tab-whitelist"></a>Registerkartenwhitelist

Die folgenden Registerkartennamen- und Registerkarten-ID-Paare befinden sich auf der Whitelist. IDs von abhängigen Registerkarten werden nicht gekoppelt, müssen jedoch gemäß der Spalte „Registerkarten-ID“ gültig sein. Bei den Werten wird Groß- und Kleinschreibung unterschieden.

|Registerkartenname              |Registerkarten-ID            |
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