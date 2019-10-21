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
# <a name="contributing-to-powershell-documentation"></a>Bijdragen aan PowerShell-documentatie

Bedankt voor uw interesse in de PowerShell-documentatie!

Dit document gaat over de procedure voor het bijdragen aan artikelen en codevoorbeelden die op de PowerShell-documentatiesite worden gehost. Bijdragen kunnen iets eenvoudigs betreffen als correcties van typfouten of iets ingewikkelds als nieuwe artikelen.

De PowerShell-documentatiesite is opgebouwd vanuit meerdere opslagplaatsen die een of meer docsets bevatten:

- [Naslaginformatie voor PowerShell-concepten en -cmdlets][psdocs]
- Voorbeelden van PowerShell-SDK-code - privéopslagplaats met de voorbeelden die in de SDK-artikelen worden gebruikt
- [Naslaginformatie voor PowerShell .NET-SDK](/dotnet/api/?view=pscore-6.2.0): Privéopslagplaats met inhoud die is gegenereerd op basis van een PowerShell-broncode

Problemen voor deze inhoud worden bijgehouden in de [PowerShell-Docs][docsrepo]-opslagplaats.

## <a name="repository-structure"></a>Structuur van de opslagplaats

De PowerShell-Docs-opslagplaats bestaat uit drie docsets die worden gepubliceerd op [Microsoft Docs][psdocs]. De docsets zijn opgenomen in de volgende mappen:

- [/reference/][ref]: Bevat de verwijzing naar de PowerShell-cmdlet voor de cmdlets die in PowerShell zijn inbegrepen. De naslaginformatie is gebundeld in versiemappen (3.0, 4.0, 5.0, 5.1, 6 en 7). Deze docset bevat geen naslaginformatie voor de modules die in Windows of andere producten van Microsoft worden geleverd.
- [/reference/docs-conceptual][conceptual]: Bevat de conceptuele documentatie voor PowerShell. Hieronder vallen installatie-instructies, voorbeeldscripts, uitleg en meer.
- [/developer/][SDK]: Bevat de conceptuele documentatie voor de PowerShell-SDK.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
