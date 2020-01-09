---
title: GitHub-bijdragewerkstroom voor belangrijke of langdurige wijzigingen
description: In dit artikel wordt beschreven hoe u de werkstroom voor belangrijke bijdragen gebruikt om bijdragen te leveren aan artikelen op docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 997f313e94e4858f37501736c1ec0be2fa8fd552
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188239"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>GitHub-bijdragewerkstroom voor belangrijke of langdurige wijzigingen

> [!IMPORTANT]
> Op alle opslagplaatsen die naar docs.microsoft.com publiceren, is de [Microsoft Open Source-gedragscode](https://opensource.microsoft.com/codeofconduct/) of de [.NET Foundation-gedragscode](https://dotnetfoundation.org/code-of-conduct) van toepassing. Zie [Veelgestelde vragen over de gedragscode](https://opensource.microsoft.com/codeofconduct/faq/) voor meer informatie. Of neem contact op via [opencode@microsoft.com](mailto:opencode@microsoft.com) of [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) als u vragen of opmerkingen hebt.<br>
>
> Kleine correcties of verduidelijkingen voor de documentatie en codevoorbeelden in de openbare opslagplaatsen vallen onder de [gebruiksvoorwaarden van docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Bij nieuwe inhoud of belangrijke wijzigingen wordt een opmerking gegenereerd in de pull-aanvraag, waarin u wordt gevraagd een online Contribution License Agreement (CLA) in te dienen als u geen werknemer van Microsoft bent. U moet het onlineformulier invullen voordat uw pull-aanvraag kan worden samengevoegd.

## <a name="overview"></a>Overzicht

Deze werkstroom is geschikt voor inzenders die belangrijke wijzigingen moeten aanbrengen of die regelmatig bijdragen leveren aan een opslagplaats. Frequente inzenders hebben doorgaans doorlopende (langlopende) wijzigingen die meerdere build-/validatie-/faseringscycli doorlopen of over meerdere dagen worden uitgespreid voor accordering en samenvoeging van de pull-aanvraag.

Voorbeelden van dergelijke bijdragen zijn:

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Bekijk voordat u aan de slag gaat eerst enkele Git-/GitHub-termen en -monikers die in deze werkstroom worden gebruikt. U hoeft deze nu nog niet te begrijpen. U maakt eerst kennis met de termen en kunt dan deze sectie raadplegen als u een definitie wilt controleren.

| Name | Beschrijving |
|-----------|-------------|
|fork|Wordt doorgaans als zelfstandig naamwoord gebruikt bij verwijzing naar een kopie van een GitHub-hoofdopslagplaats. Een fork is in feite gewoon een opslagplaats. Het is echter een bijzondere opslagplaats in de zin dat GitHub een verbinding in stand houdt met de bovenliggende of hoofdopslagplaats. Soms wordt de term gebruikt als werkwoord. In het Nederlands wordt hiervoor het werkwoord splitsen gebruikt, bijvoorbeeld "U moet de opslagplaats eerst splitsen."|
|remote|Een benoemde verbinding naar een externe opslagplaats, bijvoorbeeld de origin of upstream remote. In Git wordt hiernaar verwezen als remote, omdat deze wordt gebruikt om te verwijzen naar een opslagplaats die wordt gehost op een andere computer. In deze werkstroom is een remote altijd een GitHub-opslagplaats.|
|origin|De naam die wordt gegeven aan de verbinding tussen de lokale opslagplaats en de opslagplaats waarvandaan deze is gekloond. In deze werkstroom staat origin voor de verbinding met uw fork. Deze wordt soms gebruikt als moniker voor de oorspronkelijke opslagplaats, bijvoorbeeld in "Vergeet niet uw wijzigingen naar de origin te uploaden."|
|upstream|Net als de origin remote is upstream een benoemde verbinding naar een andere opslagplaats. In deze werkstroom staat upstream voor de verbinding tussen uw lokale opslagplaats en de hoofdopslagplaats, waarvan de fork is gemaakt. Deze wordt soms als moniker gebruikt voor de upstream-opslagplaats, bijvoorbeeld in "Vergeet niet de wijzigingen van de upstream te downloaden."|

## <a name="workflow"></a>Werkstroom

>[!IMPORTANT]
> Voer de stappen uit in de sectie [Instellen](get-started-setup-github.md), indien u dit nog niet hebt gedaan. In deze sectie doorloopt u het instellen van uw GitHub-account, het installeren van Git Bash en een Markdown editor, het maken van een fork en het instellen van een lokale opslagplaats. Als u niet bekend bent met Git- en GitHub-concepten als een opslagplaats of vertakking, leest u eerst [Basisinformatie over Git en GitHub](git-github-fundamentals.md).

In deze werkstroom stromen wijzigingen via een doorlopende cyclus. Vanuit de lokale opslagplaats op uw apparaat stromen de wijzigingen terug naar uw GitHub fork, naar de GitHub-hoofdopslagplaats en weer terug naar uw lokale opslagplaats terwijl u wijzigingen van andere inzenders opneemt.

### <a name="use-github-flow"></a>De GitHub-workflow gebruiken

In [Basisinformatie over Git en GitHub](git-github-fundamentals.md#git) hebt u gelezen dat een Git-opslagplaats een master-vertakking bevat en eventueel vertakkingen met werkversies die nog niet in de master zijn geïntegreerd. Wanneer u een reeks logisch met elkaar verband houdende wijzigingen introduceert, wordt aanbevolen een *werkvertakking* te maken waarmee u uw wijzigingen in de gehele werkstroom kunt beheren. In deze uitleg wordt hiernaar verwezen als een werkvertakking, omdat het een werkruimte is waarin wijzigingen worden herhaald/verfijnd totdat deze in de master-vertakking kunnen worden geïntegreerd.

Als u gerelateerde wijzigingen isoleert in een specifieke vertakking, kunt u deze wijzigingen onafhankelijk beheren en introduceren, waarbij u zich kunt richten op een specifieke uitgavetijd in de publicatiecyclus. Afhankelijk van uw werkzaamheden, kunt u daardoor meerdere werkvertakkingen in uw opslagplaats hebben. Het is niet ongebruikelijk dat mensen tegelijkertijd in meerdere vertakkingen werken, die elk bij een ander project horen.

>[!TIP]
>Het wordt *niet* aanbevolen de wijzigingen rechtstreeks in de mastervertakking door te voeren. Stelt u zich eens voor dat u de mastervertakking gebruikt om enkele wijzigingen door te voeren voor het uitbrengen van een getimede functie. U hebt de wijzigingen voltooid en wacht op het moment waarop u deze kunt uitbrengen. Ondertussen ontvangt u een urgente aanvraag om een fout op te lossen. U voert de wijziging door in een bestand in de mastervertakking en publiceert de wijziging. In dit voorbeeld hebt u per ongeluk niet alleen de fix gepubliceerd, maar *ook* de wijzigingen die u pas op een specifieke datum wilde vrijgeven.

Ga daarom als volgt te werk om in uw lokale opslagplaats een werkvertakking te maken waarin u uw wijzigingen kunt vastleggen. Als u Git Bash hebt ingesteld (zie [Hulpprogramma's installeren om inhoud aan te passen](get-started-setup-tools.md)), kunt u een nieuwe vertakking maken en die vertakking met één opdracht vanuit uw gekloonde opslagplaats 'uitchecken':

````
git checkout -b "branchname"
````

Elke Git-client is anders, dus raadpleeg het Help-systeem van de client van uw keuze. Een overzicht van het proces vindt u in de GitHub-handleiding in de [GitHub-workflow](https://guides.github.com/introduction/flow/).

## <a name="making-your-changes"></a>Wijzigingen aanbrengen

Nu u een kopie ('kloon') van de Microsoft-opslagplaats hebt en een vertakking hebt gemaakt, kunt u met een tekst- of Markdown-editor alle wijzigingen aanbrengen waar de community volgens u baat bij kan hebben. Dit wordt beschreven op de pagina [Hulpprogramma's installeren om inhoud aan te passen](get-started-setup-tools.md).  U kunt uw wijzigingen lokaal opslaan en deze pas naar Microsoft verzenden wanneer u klaar bent.

## <a name="saving-changes-to-your-repository"></a>Wijzigingen in uw opslagplaats opslaan

Voordat u uw wijzigingen naar de auteur verzendt, moet u deze eerst in uw GitHub-opslagplaats opslaan.  En als u de Git Bash-opdrachtregel gebruikt, kan dit in slechts een paar eenvoudige stappen worden uitgevoerd, ook al zijn alle hulpprogramma's verschillend.

Eerst moet u vanuit de opslagplaats alle wijzigingen _faseren_ die moeten worden aangebracht.  Voer hiervoor het volgende uit:

````
git add --all
````

Vervolgens moet u uw opgeslagen wijzigingen doorvoeren in uw lokale opslagplaats.  Voer hiervoor het volgende uit in Git Bash:

````
git commit -m "Short Description of Changes Made"
````

En omdat u deze vertakking op uw lokale computer hebt gemaakt, moet u de fork van uw GitHub.com-account hiervan op de hoogte stellen.  Als u Git Bash gebruikt, kunt u hiervoor het volgende uitvoeren:

````
git push --set-upstream origin <branchname>
````

U bent klaar!  Uw code is nu beschikbaar in uw GitHub-opslagplaats; u kunt nu een pull-aanvraag maken.  

>[!TIP]
> Hoewel uw wijzigingen weliswaar in uw persoonlijke GitHub-account worden weergegeven wanneer u deze pusht, is er geen regel dat u direct een pull-aanvraag moet indienen.  Als u wilt stoppen en op een later tijdstip wilt terugkeren om extra aanpassingen aan te brengen, is dat prima.

Moet u iets herstellen dat u hebt ingediend?  Geen probleem!  Breng uw wijzigingen aan in dezelfde vertakking; daarna kunt u de wijzigingen doorvoeren en opnieuw pushen (u hoeft de upstream-server niet in te stellen op volgende pushes van dezelfde vertakking).

Wilt u nog andere wijzigingen aanbrengen die geen betrekking hebben op deze wijziging?  Ga terug naar de hoofdvertakking om een nieuwe vertakking uit te checken met behulp van Git Bash. Dit is net zo eenvoudig als:

````
git checkout master
git checkout -b "branchname"
````

U bent nu terug in een nieuwe vertakking en u bent al aardig op weg om een belangrijke bijdrager te worden.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Volgende stappen

Dat is alles. U hebt een bijdrage geleverd aan inhoud voor docs.microsoft.com.

- Ga verder naar het artikel [Belangrijke aspecten van het schrijven](how-to-write-use-markdown.md) voor meer informatie over onderwerpen als Markdown en de syntaxis van Markdown-extensies.
