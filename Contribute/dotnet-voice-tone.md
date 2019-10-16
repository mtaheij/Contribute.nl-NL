---
title: Vorm- en toonrichtlijnen voor .NET-documentatiebijdragen
description: Leer wat onze vorm- en toonrichtlijnen zijn aan de hand van voorbeelden van onze stijl in vergelijking met voorbeelden die niet aan onze richtlijnen voldoen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 4108019ac50d703c6dd509eca7a6394cc1c9dc18
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288477"
---
# <a name="voice-and-tone-guidelines"></a>Vorm- en toonrichtlijnen

Allerlei soorten mensen, onder wie IT-professionals en -ontwikkelaars, lezen uw documenten om .NET te leren kennen en te gebruiken bij hun dagelijkse werkzaamheden. Uw doel is om geweldige documentatie te maken die lezers helpen bij hun reis. Onze richtlijnen helpen daarbij. Onze stijlgids bevat de volgende aanbevelingen:

U kunt voorbeelden van elk ervan bekijken bij het lezen van deze stijlgids. We hebben deze gids volgens onze eigen richtlijnen geschreven om een voorbeeld te geven dat u kunt volgen bij het schrijven van documentatie voor . NET. We geven ook tegenvoorbeelden, zodat u kunt zien hoe artikelen eruitzien als u onze richtlijnen niet volgt.

## <a name="use-a-conversational-tone"></a>Schrijf in spreektaal

### <a name="appropriate-style"></a>Gewenste stijl

We zien graag spreektaal in onze documentatie. Als u een van onze zelfstudies of een uitleg leest, moet u het gevoel krijgen dat u in gesprek bent met de auteur. De ervaring moet informeel, gemoedelijk en informatief voor u zijn. U moet als lezer het gevoel krijgen dat u luistert naar de auteur die de concepten aan u uitlegt.

### <a name="inappropriate-style"></a>Ongewenste stijl

Er is een contrast waarneembaar tussen spreektaal en de stijl die men doorgaans aantreft in academische behandelingen van technische onderwerpen. Deze laatste resources zijn zeer nuttig, maar zijn geschreven in een stijl die behoorlijk afwijkt van de stijl in onze documentatie. Bij het lezen van een academische verhandeling treft men een zeer andere toon en schrijfstijl aan. Men krijgt het gevoel een droog verslag over een zeer saai onderwerp te lezen.  

De eerste alinea hierboven is geschreven in spreektaal, zoals we aanbevelen. De tweede is geschreven in academische stijl. U merkt direct het verschil. 

## <a name="write-in-second-person"></a>Schrijf in de tweede persoon

### <a name="appropriate-style"></a>Gewenste stijl

Schrijf uw artikelen alsof u rechtstreeks tegen de lezer praat. Zorg dat u de tweede persoon vaak gebruikt (zoals ik net in deze twee zinnen heb gedaan). Dit betekent niet dat u altijd het woord 'u' moet gebruiken. Richt u wel rechtstreeks tot de lezer. Doe dat door de gebiedende wijs te gebruiken. Vertel wat u de lezer wilt leren.

### <a name="inappropriate-style"></a>Ongewenste stijl

Een auteur kan er ook voor kiezen om in de derde persoon te schrijven. De auteur moet dan een voornaamwoord of zelfstandig naamwoord vinden om naar de lezer te verwijzen. Voor de lezer is een stijl in de derde persoon minder boeiend en aantrekkelijk om te lezen.

De eerste alinea is geschreven in onze aanbevolen stijl. De tweede is in de derde persoon geschreven. Schrijf in de tweede persoon. Dat vindt u vast veel gemakkelijker om te lezen.

## <a name="use-active-voice"></a>Gebruik de actieve vorm

Schrijf uw artikelen in de actieve vorm. De actieve vorm betekent dat het onderwerp van de zin de handeling (het werkwoord) van de zin uitvoert. Het tegenovergestelde is de passieve vorm, waarbij de zin zo is opgesteld dat het onderwerp van de zin de handeling ondergaat. Vergelijk deze twee voorbeelden:

>De programmeur heeft de code met behulp van de compiler omgezet in een uitvoerbaar bestand.

>De code is door de programmeur met behulp van de compiler omgezet in een uitvoerbaar bestand.

De eerste zin maakt gebruik van de actieve vorm. De tweede zin is geschreven in de passieve vorm. (En deze twee zinnen zelf zijn ook weer voorbeelden van beide stijlen.)

We raden de actieve vorm aan omdat die beter leesbaar is. De passieve vorm kan lastiger te lezen zijn.

## <a name="target-a-fifth-grade-reading-level"></a>Richt u op het leesniveau van groep zeven

We geven deze laatste richtlijn omdat het Engels voor veel van onze lezers niet de moedertaal is. U bereikt een internationaal publiek met uw artikelen. Houd er rekening mee dat uw lezers niet dezelfde Engelse woordenschat hebben als u.

U schrijft echter wel voor technische professionals. U mag aannemen dat uw lezers programmeerkennis hebben en de specifieke programmeertermen kennen. Objectgeoriënteerd programmeren, klasse, object, functie en methode zijn vertrouwde termen. Maar niet iedereen die uw artikelen leest, heeft informatica gestudeerd. Daarom is het goed om termen als 'idempotent' uit te leggen als u die gebruikt:

>De methode `Close()` is idempotent. Dit betekent dat u deze methode meerdere keren kunt aanroepen, waarbij het effect hetzelfde is als wanneer u deze methode één keer aanroept.

## <a name="avoid-future-tense"></a>Vermijd de toekomende tijd

In bepaalde niet-Engelse talen is het begrip toekomende tijd anders dan in het Engels. Als u de toekomende tijd gebruikt, worden uw documenten misschien moeilijker leesbaar. Uit het gebruik van de toekomende tijd volgt ook de vraag wanneer dat precies is. Als u dus zegt 'U zult ervan profiteren als u PowerShell leert' is de voor de hand liggende vraag voor de lezer wanneer hij of zij er dan van gaat profiteren. Gebruik daarom in plaats daarvan: 'U profiteert ervan als u PowerShell leert'.

## <a name="what-is-it---so-what"></a>Leg het nut van concepten uit

Definieer een concept als u het bij de lezer introduceert en leg alleen dan uit waarom het nuttig is. Pas als de lezer begrijpt wat iets is, kan hij of zij de voordelen (of wat dan ook) ervan begrijpen.
