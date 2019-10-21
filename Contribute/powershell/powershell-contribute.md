---
title: Bijdragen aan opslagplaatsen van Powershell-Docs
description: Dit artikel betreft de opslagplaatsen waaruit de PowerShell-documentatie bestaat.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290168"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="c2443-103">Bijdragen aan PowerShell-documentatie</span><span class="sxs-lookup"><span data-stu-id="c2443-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="c2443-104">Bedankt voor uw interesse in de PowerShell-documentatie!</span><span class="sxs-lookup"><span data-stu-id="c2443-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="c2443-105">Dit document gaat over de procedure voor het bijdragen aan artikelen en codevoorbeelden die op de PowerShell-documentatiesite worden gehost.</span><span class="sxs-lookup"><span data-stu-id="c2443-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="c2443-106">Bijdragen kunnen iets eenvoudigs betreffen als correcties van typfouten of iets ingewikkelds als nieuwe artikelen.</span><span class="sxs-lookup"><span data-stu-id="c2443-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="c2443-107">De PowerShell-documentatiesite is opgebouwd vanuit meerdere opslagplaatsen die een of meer docsets bevatten:</span><span class="sxs-lookup"><span data-stu-id="c2443-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="c2443-108">[Naslaginformatie voor PowerShell-concepten en -cmdlets][psdocs]</span><span class="sxs-lookup"><span data-stu-id="c2443-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="c2443-109">Voorbeelden van PowerShell-SDK-code - privéopslagplaats met de voorbeelden die in de SDK-artikelen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="c2443-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="c2443-110">[Naslaginformatie voor PowerShell .NET-SDK](/dotnet/api/?view=pscore-6.2.0): Privéopslagplaats met inhoud die is gegenereerd op basis van een PowerShell-broncode</span><span class="sxs-lookup"><span data-stu-id="c2443-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="c2443-111">Problemen voor deze inhoud worden bijgehouden in de [PowerShell-Docs][docsrepo]-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="c2443-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="c2443-112">Structuur van de opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c2443-112">Repository Structure</span></span>

<span data-ttu-id="c2443-113">De PowerShell-Docs-opslagplaats bestaat uit drie docsets die worden gepubliceerd op [Microsoft Docs][psdocs]. De docsets zijn opgenomen in de volgende mappen:</span><span class="sxs-lookup"><span data-stu-id="c2443-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="c2443-114">[/reference/][ref]: Bevat de verwijzing naar de PowerShell-cmdlet voor de cmdlets die in PowerShell zijn inbegrepen.</span><span class="sxs-lookup"><span data-stu-id="c2443-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="c2443-115">De naslaginformatie is gebundeld in versiemappen (3.0, 4.0, 5.0, 5.1, 6 en 7).</span><span class="sxs-lookup"><span data-stu-id="c2443-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="c2443-116">Deze docset bevat geen naslaginformatie voor de modules die in Windows of andere producten van Microsoft worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="c2443-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="c2443-117">[/reference/docs-conceptual][conceptual]: Bevat de conceptuele documentatie voor PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2443-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="c2443-118">Hieronder vallen installatie-instructies, voorbeeldscripts, uitleg en meer.</span><span class="sxs-lookup"><span data-stu-id="c2443-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="c2443-119">[/developer/][SDK]: Bevat de conceptuele documentatie voor de PowerShell-SDK.</span><span class="sxs-lookup"><span data-stu-id="c2443-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
