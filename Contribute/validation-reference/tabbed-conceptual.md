# <a name="tabbed-conceptual"></a><span data-ttu-id="2ab9b-101">Tabbed conceptual</span><span class="sxs-lookup"><span data-stu-id="2ab9b-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ab9b-102">De Tabbed conceptual-syntaxis is afgeschaft en er mogen geen nieuwe tabbladen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="2ab9b-103">De in dit artikel beschreven validaties zijn van toepassing op inhoudsets die zijn goedgekeurd voor het gebruik van Tabbed conceptual tot er vervangende functionaliteit beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="2ab9b-104">Tab-syntaxis</span><span class="sxs-lookup"><span data-stu-id="2ab9b-104">Tab syntax</span></span>

<span data-ttu-id="2ab9b-105">De syntaxis voor tabs ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="2ab9b-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="2ab9b-106">Tab met één niveau:</span><span class="sxs-lookup"><span data-stu-id="2ab9b-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="2ab9b-107">Optioneel afhankelijk tab:</span><span class="sxs-lookup"><span data-stu-id="2ab9b-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="2ab9b-108">Voorbeeld van een tabsectie met één niveau met twee tabs en het tabgroepeindteken (---):</span><span class="sxs-lookup"><span data-stu-id="2ab9b-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="2ab9b-109">Tabs kunnen eventueel secundaire tabs of afhankelijkheidstabs bevatten.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="2ab9b-110">Hierdoor worden tabs afhankelijk van de selectie in een andere reeks tabs.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="2ab9b-111">Hier volgt een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="2ab9b-111">Here's an example:</span></span>

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

<span data-ttu-id="2ab9b-112">De volgende validaties gelden voor syntaxis van tabs:</span><span class="sxs-lookup"><span data-stu-id="2ab9b-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="2ab9b-113">De syntaxis van tabs moet juist zijn.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="2ab9b-114">Afhankelijke tabs moeten in een vorige tabgroep zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="2ab9b-115">Er is slechts één niveau van afhankelijkheid toegestaan.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="2ab9b-116">Er zijn minimaal twee tabs toegestaan.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="2ab9b-117">Er zijn niet meer dan vier tabs toegestaan.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="2ab9b-118">Tabs moet in een whitelist zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="2ab9b-119">Tab-id-paren moeten geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="2ab9b-120">Deze kunnen niet meerdere keren dezelfde tab-id bevatten in één tabgroep.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="2ab9b-121">Whitelist voor tabs</span><span class="sxs-lookup"><span data-stu-id="2ab9b-121">Tab whitelist</span></span>

<span data-ttu-id="2ab9b-122">De volgende tabnaam-/tab-id-paren zijn in een whitelist opgenomen.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="2ab9b-123">Afhankelijke tab-id's zijn niet gepaard maar moeten geldig zijn op basis van de kolom Tab-id.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="2ab9b-124">De waarden zijn hoofdlettergevoelig</span><span class="sxs-lookup"><span data-stu-id="2ab9b-124">The values are case-sensitive</span></span>

|<span data-ttu-id="2ab9b-125">Naam van het tab</span><span class="sxs-lookup"><span data-stu-id="2ab9b-125">Tab name</span></span>              |<span data-ttu-id="2ab9b-126">Id van de tab</span><span class="sxs-lookup"><span data-stu-id="2ab9b-126">Tab ID</span></span>            |
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