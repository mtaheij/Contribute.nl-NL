---
title: Bijdrageproces voor Powershell-documentopslagplaatsen
description: In dit artikel vindt u een korte inleiding voor bijdragen aan de opslagplaatsen voor PowerShell-documenten. U krijgt informatie over de gebruikte opslagplaatsen, het proces voor het rangschikken van inhoud en de beleidsregels voor het beheren van codevoorbeelden en andere assets.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290191"
---
# <a name="process-for-contributing-to-powershell-docs"></a>Proces voor bijdragen aan PowerShell-documenten

We stellen bijdragen vanuit de community aan documenten zeer op prijs. De volgende lijst bevat een aantal richtlijnen waarmee u rekening moet houden wanneer u een bijdrage levert aan de PowerShell-documentatie:

- **NIET DOEN**: verras ons niet met grote pull-aanvragen. In plaats daarvan kunt u beter een actie-item aanmaken, zodat we in gesprek kunnen gaan over de richting die we op moeten gaan voordat u hier erg veel tijd in gaat steken.
- **DOEN**: volg deze instructies en de stijlgidsen voor [code](powershell-style-code.md) en [naslaginformatie](powershell-style-reference.md).
- **DOEN**: gebruik het [sjabloonbestand](powershell-style-basic-markdown.md) als beginpunt van uw werk.
- **DOEN**: maak een aparte vertakking van uw fork voordat u aan de artikelen gaat werken.
- **DOEN**: volg de [GitHub Flow-workflow](../how-to-write-workflows-major.md).
- **DOEN**: plaats regelmatig blogs en tweets (of wat u maar wilt) over uw bijdragen.

Door deze richtlijnen te volgen, hebben we allemaal een betere ervaring.

## <a name="make-a-contribution-to-powershell-docs"></a>Een bijdrage leveren aan PowerShell-documenten

U kunt kiezen uit bestaande [actie-items](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).
Afhankelijk van uw interesse en mate van betrokkenheid vallen de inspanningen in de volgende categorieën:

- **Kleine wijzigingen**. Voor kleine wijzigingen leest u de instructies voor bewerkingen in GitHub op de [startpagina](../index.md#quick-edits-to-existing-documents) van de handleiding van de bijdrager. De wijzigingen zijn onder andere:

  - Typfouten en spelfouten oplossen
  - Grammatica of indeling verbeteren
  - Kleine technische of feitelijke bewerkingen

- **Onderhoud**. Deze categorie bevat redelijk eenvoudige bijdragen, zoals het herstellen van gebroken of onjuiste koppelingen, het toevoegen van ontbrekende codevoorbeelden of het oplossen van problemen met beperkte inhoud. In enkele gevallen gaat het bij deze actie-items om een groot aantal bestanden. In dat geval moet u ons, voor u begint, laten weten waaraan u wilt werken. Voeg een opmerking toe aan het actie-item om ons te melden dat u hieraan werkt.

- **Updates van de inhoud**. Gezien de grote omvang van de documentenset kan inhoud eenvoudig verouderd raken, waardoor revisie is vereist. Daarnaast kunnen, om tal van redenen, twee of zelfs drie exemplaren van hetzelfde inhoudsitem bestaan. Wanneer u inhoud bijwerkt, moet u ervoor zorgen dat afzonderlijke onderwerpen actueel zijn of inhoud in een functiegebied reviseren, om dubbele items te vermijden en ervoor te zorgen dat alle unieke inhoud in de kleinere documentenset wordt bewaard.

- **Nieuwe inhoud schrijven**. Als u uw eigen onderwerp wilt schrijven, vindt u bij deze actie-items een aantal onderwerpen die we graag aan onze documentenset willen toevoegen. Wel willen we graag dat u ons informeert voordat u aan een onderwerp gaat werken. Als u een onderwerp wilt gaan schrijven dat niet in de lijst staat, kunt u een actie-item openen.

Zodra u een taak hebt gekozen om aan te werken, volgt u de instructies om [aan de slag](../get-started-setup-github.md) te gaan om een GitHub-account te maken en uw omgeving in te stellen.

### <a name="making-large-changes"></a>Grote wijzigingen aanbrengen

**Stap 1:** Als u nieuwe inhoud wilt gaan schrijven of bestaande inhoud grondig wilt reviseren, opent u een actie-item waarin u beschrijft wat u wilt doen.

**Stap 2:** Splits de `MicrosoftDocs/PowerShell-Docs`-opslagplaats en maak een werkvertakking voor uw wijzigingen.

**Stap 3:** Breng de wijzigingen aan in deze nieuwe vertakking.

Gebruik de sjabloon in de [stijlgids](powershell-style-basic-markdown.md) als uw uitgangspunt als dit een nieuw onderwerp is. Dit bestand bevat de schrijfrichtlijnen en uitleg over de metagegevens die voor elk artikel zijn vereist.

Navigeer naar de map die overeenkomt met de locatie in de inhoudsopgave die u in stap 1 voor uw artikel hebt bepaald.
Die map bevat de Markdown-bestanden voor alle artikelen in dat hoofdstuk. Maak indien nodig een nieuwe map waarin u de bestanden voor uw inhoud plaatst. Het hoofdartikel voor dat hoofdstuk heet *index.md*.
Voor afbeeldingen en andere statische resources maakt u de submap **media** in de map waarin uw artikel staat, als deze submap nog niet is gemaakt. Maak in de map **media** een submap met de naam van het artikel (met uitzondering van het indexbestand).

Volg de juiste Markdown-syntaxis. Lees de [stijlgids](powershell-style-basic-markdown.md) voor gedetailleerde instructies en voorbeelden.

**Voorbeeldstructuur**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**Stap 4:** Dien een pull-aanvraag (PR) in van uw vertakking naar de *fasering*-vertakking.

Normaal gesproken gaat een PR over één actie-item per keer. Met de aanvraag kunnen een of meerdere bestanden worden aangepast. Als u oplossingen van meerdere problemen in verschillende bestanden wilt aanpakken, kunt u beter afzonderlijke pull-aanvragen gebruiken.

Als u met uw pull-aanvraag een bestaand probleem oplost, voegt u het trefwoord `Fixes #Issue_Number` toe aan het Commit-bericht of de beschrijving van de pull-aanvraag. Op die manier wordt het actie-item automatisch afgesloten zodra de pull-aanvraag is samengevoegd. Zie [Actie-items afsluiten via Commit-berichten](https://help.github.com/articles/closing-issues-via-commit-messages/) voor meer informatie.

Het PowerShell-team beoordeelt uw pull-aanvraag en laat u weten of er andere wijzigingen nodig zijn voor de goedkeuring.

**Stap 5:** Voer eventuele benodigde updates aan uw vertakking door die u met het team hebt besproken.

Nadat de pull-aanvraag is goedgekeurd, voegen de onderhouders uw pull-aanvraag samen in de *fasering*-vertakking. We pushen periodiek alle commits van de *fasering*-vertakking naar de *live*-vertakking. Zodra uw bijdrage live is, kunt u deze zien op de [PowerShell-Docs-site](https://docs.microsoft.com/PowerShell/). Meestal publiceren we twee tot drie keer per werkweek.

## <a name="contributor-license-agreement"></a>Licentieovereenkomst voor bijdragers

U moet de [Contribution License Agreement (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) ondertekenen voordat uw pull-aanvraag wordt samengevoegd. Dit is een eenmalige vereiste wanneer u een bijdrage levert aan onze documentatie.

U hoeft de overeenkomst niet van tevoren te ondertekenen. U kunt uw pull-aanvraag klonen, vertakken en verzenden zoals u gewend bent.
Wanneer uw pull-aanvraag wordt gemaakt, wordt deze door een CLA-bot geclassificeerd. Als het een kleine wijziging betreft (u corrigeert bijvoorbeeld een typfout), dan krijgt de pull-aanvraag het label `cla-not-required`. Anders wordt de aanvraag als `cla-required` geclassificeerd. Zodra u de CLA hebt ondertekend, krijgen de huidige en alle toekomstige pull-aanvragen het label `cla-signed`.
