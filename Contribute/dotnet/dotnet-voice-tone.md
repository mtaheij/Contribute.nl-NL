---
title: Vorm- en toonrichtlijnen voor .NET-documentatiebijdragen
description: Leer wat onze vorm- en toonrichtlijnen zijn aan de hand van voorbeelden van onze stijl in vergelijking met voorbeelden die niet aan onze richtlijnen voldoen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 6f74eb9107612edfff76831fa4dea4f90e73d050
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559212"
---
# <a name="voice-and-tone-guidelines"></a>Vorm- en toonrichtlijnen

Allerlei mensen, onder wie IT-professionals en -ontwikkelaars, lezen de .NET-documenten om .NET te leren en te gebruiken bij hun dagelijkse werkzaamheden. Uw doel is om geweldige documentatie te maken die lezers helpen bij hun reis. Onze richtlijnen helpen daarbij. Onze stijlgids bevat de volgende aanbevelingen:

## <a name="use-a-conversational-tone"></a>Schrijf in spreektaal

De volgende paragraaf is geschreven in gespreksstijl. De paragraaf erna is in een academischere stijl geschreven.

### <a name="appropriate-style"></a>Gewenste stijl

We zien graag spreektaal in onze documentatie. Als u een van onze zelfstudies of een uitleg leest, moet u het gevoel krijgen dat u in gesprek bent met de auteur. De ervaring moet informeel, gemoedelijk en informatief voor u zijn. U moet als lezer het gevoel krijgen dat u luistert naar de auteur die de concepten aan u uitlegt.

### <a name="inappropriate-style"></a>Ongewenste stijl

Er is een contrast waarneembaar tussen spreektaal en de stijl die men doorgaans aantreft in academische behandelingen van technische onderwerpen. Deze laatste resources zijn zeer nuttig, maar zijn geschreven in een stijl die behoorlijk afwijkt van de stijl in onze documentatie. Bij het lezen van een academische verhandeling treft men een zeer andere toon en schrijfstijl aan. Men krijgt het gevoel een droog verslag over een zeer saai onderwerp te lezen.  

## <a name="write-in-second-person"></a>Schrijf in de tweede persoon

De volgende paragraaf gebruikt de tweede persoon. Die daarna gebruikt de derde persoon. Schrijf in de tweede persoon.

### <a name="appropriate-style"></a>Gewenste stijl

Schrijf uw artikelen alsof u rechtstreeks tegen de lezer praat. Gebruik vaak de tweede persoon (zoals ik net in deze twee zinnen heb gedaan). Dit betekent niet dat u altijd het woord 'u' moet gebruiken. Richt u wel rechtstreeks tot de lezer. Doe dat door de gebiedende wijs te gebruiken. Vertel wat u de lezer wilt leren.

### <a name="inappropriate-style"></a>Ongewenste stijl

Een auteur kan er ook voor kiezen om in de derde persoon te schrijven. De auteur moet dan een voornaamwoord of zelfstandig naamwoord vinden om naar de lezer te verwijzen. Voor de lezer is een stijl in de derde persoon minder boeiend en aantrekkelijk om te lezen.

## <a name="use-active-voice"></a>Gebruik de actieve vorm

Schrijf uw artikelen in de actieve vorm. De actieve vorm betekent dat het onderwerp van de zin de handeling (het werkwoord) van de zin uitvoert. Het tegenovergestelde is de passieve vorm, waarbij de zin zo is opgesteld dat het onderwerp van de zin de handeling ondergaat. Vergelijk deze twee voorbeelden:

>De programmeur heeft de code met behulp van de compiler omgezet in een uitvoerbaar bestand.

>De code is door de programmeur met behulp van de compiler omgezet in een uitvoerbaar bestand.

De eerste zin maakt gebruik van de actieve vorm. De tweede zin is geschreven in de passieve vorm. (En deze twee zinnen zelf zijn ook weer voorbeelden van beide stijlen.)

We raden de actieve vorm aan omdat die beter leesbaar is. De passieve vorm kan lastiger te lezen zijn.

## <a name="write-for-readers-who-may-have-a-limited-vocabulary"></a>Schrijf voor lezers die mogelijk een beperkte woordenschat hebben

U bereikt een internationaal publiek met uw artikelen. Veel van uw lezers zijn geen Engelstalige sprekers en hebben mogelijk niet de Engelse woordenschat die u wel hebt.

U schrijft echter wel voor technische professionals. U mag aannemen dat uw lezers programmeerkennis hebben en de specifieke programmeertermen kennen. Objectgeoriënteerd programmeren, klasse, object, functie en methode zijn vertrouwde termen. Maar niet iedereen die uw artikelen leest, heeft informatica gestudeerd. Daarom is het goed om termen als 'idempotent' uit te leggen als u die gebruikt, bijvoorbeeld:

> De methode `Close()` is idempotent. Dit betekent dat u deze methode meerdere keren kunt aanroepen, waarbij het effect hetzelfde is als wanneer u deze methode één keer aanroept.

## <a name="avoid-future-tense"></a>Vermijd de toekomende tijd

In bepaalde niet-Engelse talen is het begrip toekomende tijd anders dan in het Engels. Als u de toekomende tijd gebruikt, worden uw documenten misschien moeilijker leesbaar. Uit het gebruik van de toekomende tijd volgt ook de vraag wanneer dat precies is. Als u dus zegt 'U zult ervan profiteren als u PowerShell leert' is de voor de hand liggende vraag voor de lezer wanneer hij of zij er dan van gaat profiteren. Gebruik daarom in plaats daarvan: 'U profiteert ervan als u PowerShell leert'.

## <a name="what-is-it---so-what"></a>Leg het nut van concepten uit

Definieer een concept als u het bij de lezer introduceert en leg alleen dan uit waarom het nuttig is. Pas als de lezer begrijpt wat iets is, kan hij of zij de voordelen (of wat dan ook) ervan begrijpen.
