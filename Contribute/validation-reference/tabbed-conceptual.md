---
ms.date: 03/29/2019
title: Tabbed conceptual
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841292"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="b0bbc-102">Tabbed conceptual</span><span class="sxs-lookup"><span data-stu-id="b0bbc-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0bbc-103">De Tabbed conceptual-syntaxis is afgeschaft en er mogen geen nieuwe tabbladen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="b0bbc-104">De in dit artikel beschreven validaties zijn van toepassing op inhoudsets die zijn goedgekeurd voor het gebruik van Tabbed conceptual tot er vervangende functionaliteit beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="b0bbc-105">Tab-syntaxis</span><span class="sxs-lookup"><span data-stu-id="b0bbc-105">Tab syntax</span></span>

<span data-ttu-id="b0bbc-106">De syntaxis voor tabs ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="b0bbc-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="b0bbc-107">Tab met één niveau:</span><span class="sxs-lookup"><span data-stu-id="b0bbc-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="b0bbc-108">Optioneel afhankelijk tab:</span><span class="sxs-lookup"><span data-stu-id="b0bbc-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="b0bbc-109">Voorbeeld van een tabsectie met één niveau met twee tabs en het tabgroepeindteken (---):</span><span class="sxs-lookup"><span data-stu-id="b0bbc-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="b0bbc-110">Tabs kunnen eventueel secundaire tabs of afhankelijkheidstabs bevatten.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="b0bbc-111">Hierdoor worden tabs afhankelijk van de selectie in een andere reeks tabs.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="b0bbc-112">Hier volgt een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="b0bbc-112">Here's an example:</span></span>

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

<span data-ttu-id="b0bbc-113">De volgende validaties gelden voor syntaxis van tabs:</span><span class="sxs-lookup"><span data-stu-id="b0bbc-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="b0bbc-114">De syntaxis van tabs moet juist zijn.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="b0bbc-115">Afhankelijke tabs moeten in een vorige tabgroep zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="b0bbc-116">Er is slechts één niveau van afhankelijkheid toegestaan.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="b0bbc-117">Er zijn minimaal twee tabs toegestaan.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="b0bbc-118">Er zijn niet meer dan vier tabs toegestaan.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="b0bbc-119">Tabbladen moeten worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-119">Tabs must be approved.</span></span>
- <span data-ttu-id="b0bbc-120">Tab-id-paren moeten geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="b0bbc-121">Deze kunnen niet meerdere keren dezelfde tab-id bevatten in één tabgroep.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="b0bbc-122">Goedgekeurde tabbladen</span><span class="sxs-lookup"><span data-stu-id="b0bbc-122">Approved tabs</span></span>

<span data-ttu-id="b0bbc-123">De volgende tabnaam-/tab-id-paren zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="b0bbc-124">Afhankelijke tab-id's zijn niet gepaard maar moeten geldig zijn op basis van de kolom Tab-id.</span><span class="sxs-lookup"><span data-stu-id="b0bbc-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="b0bbc-125">De waarden zijn hoofdlettergevoelig</span><span class="sxs-lookup"><span data-stu-id="b0bbc-125">The values are case-sensitive</span></span>

|<span data-ttu-id="b0bbc-126">Naam van het tab</span><span class="sxs-lookup"><span data-stu-id="b0bbc-126">Tab name</span></span>              |<span data-ttu-id="b0bbc-127">Id van de tab</span><span class="sxs-lookup"><span data-stu-id="b0bbc-127">Tab ID</span></span>            |
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