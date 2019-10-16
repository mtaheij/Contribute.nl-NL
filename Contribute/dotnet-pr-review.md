---
title: Beoordelingsproces pull-aanvraag bij .NET-docs
description: Bij .NET-docs is de webhook voor samenvoegingen van pull-aanvragen niet ingeschakeld. In dit artikel wordt het proces voor pull-aanvragen beschreven voor deze opslagplaatsen
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/04/2019
ms.openlocfilehash: 80877a93dc410454c939bcd5be5588861682ed11
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288531"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>Beoordelingsproces voor pull-aanvragen voor de opslagplaatsen van .NET-docs

In veel opslagplaatsen zijn webhooks voor samenvoegingen van pull-aanvragen, die automatisch kleine pull-aanvragen samenvoegen, niet ingeschakeld. In dit artikel wordt het controleproces voor pull-aanvragen beschreven voor deze opslagplaatsen. Het controleproces voor pull-aanvragen is ontworpen voor deze doeleinden:

1. Het publiceren van inhoud van hoge kwaliteit afkomstig van onze teams, productteamleden en communityleden.
1. Het tijdig geven van consistente feedback aan auteurs waarop zij actie kunnen ondernemen.
1. Het op gang brengen van een gesprek tussen auteurs en reviewers.

De processen blijven zich ontwikkelen naarmate teams worden vernieuwd en het platform wordt uitgebreid.

## <a name="reviewers"></a>Reviewers

Een van de leden van het inhoudsteam beoordeelt elke pull-aanvraag. Leden van het inhoudsteam kunnen een beoordeling aanvragen van de leden van het specifieke productteam om de technische nauwkeurigheid te verifiëren. Het inhoudsteam gebruikt de functie Code Ownership van GitHub om automatisch beoordelingen aan te vragen van leden van het inhoudsteam. Als onderdeel van dit proces kan een reviewer andere teamleden taggen om interne pull-aanvragen te beoordelen. Teamleden zien aangevraagde beoordelingen van teamleden en communityleden in dezelfde wachtrij.

Communityleden kunnen ook pull-aanvragen beoordelen en feedback geven. Pull-aanvragen moeten echter altijd door minstens één lid van het kerninhoudsteam worden goedgekeurd voordat ze worden samengevoegd.

## <a name="review-process"></a>Beoordelingsproces

Beoordelingen volgen een van de drie paden op basis van de pull-aanvraag:

- **Kleine pull-aanvragen**: bij kleine pull-aanvragen gaat het om één bugfix, zoals een schrijffout, een verbroken koppeling, kleine codewijzigingen of soortgelijke wijzigingen.
- **Grote bijdragen**: grote bijdragen zijn belangrijke bewerkingen van een bestaand artikel, nieuwe artikelen, of bewerkingen van een aantal artikelen.
- **Wordt aan gewerkt**: auteurs kunnen een beoordeling aanvragen voor een artikel waar nog aan wordt gewerkt door een pull-aanvraag te openen met het label [WIP] in de titel. Het label WIP is een afkorting van 'Work in Progress' (wordt aan gewerkt). 

De verwerking via bot voor de Licentieovereenkomst voor bijdragers (CLA) is een goede richtlijn voor het verschil tussen kleine en grote bijdragen. Pull-aanvragen waarvoor de CLA niet hoeft te worden ondertekend, zijn meestal klein. Pull-aanvragen waarvoor de CLA wel moet worden ondertekend, zijn meestal groot.

### <a name="small-prs"></a>Kleine pull-aanvragen

De wijzigingen in kleine pull-aanvragen worden beoordeeld op nauwkeurigheid en gecontroleerd met behulp van de build op de beoordelingssite. Omdat deze pull-aanvragen klein zijn, wordt er geen beoordeling van het hele artikel geactiveerd. 

Reviewers kunnen andere kleine wijzigingen opmerken die een artikel beter leesbaar maken. Als deze wijzigingen eveneens klein zijn, kunnen ze worden voorgesteld als opmerkingen bij de beoordeling. Als de voorgestelde wijzigingen een grotere beoordeling zouden activeren, is het beter om een probleem te melden en ze later aan te pakken. 

### <a name="larger-changes"></a>Grotere wijzigingen

Grotere pull-aanvragen worden grondiger beoordeeld. Er wordt gecontroleerd of:

- De pull-aanvraag voorbeeldcode bevat, in de bron en als downloadbaar ZIP-bestand.
- Voorbeeldcode correct kan worden gecompileerd en uitgevoerd.
- Het artikel duidelijk de doelen beschrijft voor de lezer en of deze doelen worden bereikt.
- Het artikel voldoet aan de [stijl- en grammaticarichtlijnen](dotnet-style-guide.md) en volgt onze [principes voor toonzetting en woordgebruik](dotnet-voice-tone.md).
- Alle koppelingen juist zijn omgezet.

Leden van het inhoudsteam beoordelen de pull-aanvraag en verzenden de beoordeling met opmerkingen. Als alleen kleine wijzigingen zijn aangevraagd, kunnen teamleden de pull-aanvraag met de feedback goedkeuren. De auteur kan vervolgens de feedback verwerken en de pull-aanvraag samenvoegen. Voor de meeste beoordelingen worden wijzigingen aangevraagd en wanneer deze wijzigingen zijn aangebracht, gaat de reviewer opnieuw beoordelen.

Als voor de bewerkingen een technische beoordeling is vereist, vraagt de reviewer van het inhoudsteam een beoordeling aan bij het juiste lid van het productteam.

### <a name="review-wip-pull-requests"></a>Pull-aanvragen voor WIP beoordelen

Nieuwe auteurs willen mogelijk graag al vroeg in het proces feedback ontvangen. Ze kunnen een pull-aanvraag openen door het label [WIP] toe te voegen aan de titel. In een opmerking kunnen ze een vroege beoordeling aanvragen.

Deze vroege beoordelingen zijn niet zo grondig als een volledige beoordeling van een pull-aanvraag. Het inhoudsteam plaatst opmerkingen, maar keurt niets goed en vraagt geen wijzigingen aan met behulp van de beoordelingsfunctie van GitHub. Deze vroege beoordelingen zijn gericht op de structuur van het artikel: de grote lijnen, de algemene inhoud en de voorbeelden. Deze beoordelingen omvatten geen grondige controle van de grammatica en juiste koppelingen.

## <a name="respond-to-reviews"></a>Reageren op beoordelingen

De auteur werkt de pull-aanvraag bij als antwoord op de opmerkingen, waarbij elke verwerkte opmerking wordt gemarkeerd met de reactie +1 om aan te geven dat deze is verwerkt. Als de auteur het niet eens is met een opmerking, of de opmerking op een andere manier verwerkt, voegt hij of zij een opmerking toe waarin dit wordt uitgelegd.

De auteur @-mentions de oorspronkelijke reviewer in een opmerking om een nieuwe beoordeling aan te vragen. 

## <a name="response-time-expectations"></a>Verwachtingen met betrekking tot reactietijden

Leden van het inhoudsteam beoordelen nieuwe pull-aanvragen meestal binnen twee werkdagen. Als de beoordeling langer duurt, voegt een van de teamleden een opmerking toe dat de pull-aanvraag is gezien en wanneer deze waarschijnlijk wordt beoordeeld.

Zodra een beoordeling is verzonden, moeten auteurs proberen om in minder dan een week te reageren op de opmerkingen. Vrijwilligers kunnen mogelijk niet altijd aan deze verwachtingen voldoen vanwege andere verplichtingen. In dergelijke gevallen vragen teamleden de communityauteur om de pull-aanvraag bij te werken. Als dit niet kan, werkt het teamlid de pull-aanvraag bij en voegt deze samen.
