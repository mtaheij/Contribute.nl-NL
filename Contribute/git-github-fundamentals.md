---
title: Essentiële informatie over Git en GitHub voor documentatie
description: In dit artikel vindt u een overzicht van Git- en GitHub-opslagplaatsen en wordt uitgelegd hoe inhoud wordt geordend en welke naamconventies voor docs.microsoft.com worden gebruikt.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 5f7f90b69953e23833906202c739d2168b139d7e
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2018
---
# <a name="git-and-github-essentials-for-docs"></a>Essentiële informatie over Git en GitHub voor Docs

## <a name="overview"></a>Overzicht

Als inzender van Docs-inhoud werkt u met meerdere hulpmiddelen en processen. Hiermee kunt u gelijktijdig met andere inzenders aan hetzelfde project te werken, mogelijk aan precies dezelfde inhoud of zelfs op hetzelfde moment. Dit wordt allemaal mogelijk gemaakt door Git- en GitHub-software.

Git is een open source-versiebeheersysteem. Hiermee is dit soort samenwerking aan een project mogelijk door middel van *gedistribueerd versiebeheer* van bestanden in *opslagplaatsen*. Git maakt het in feite mogelijk dat stromen werkzaamheden van meerdere inzenders in een tijdsbestek voor een bepaalde opslagplaats worden geïntegreerd.

GitHub is een hostingwebservice voor Git-opslagplaatsen, zoals de opslagplaatsen die worden gebruikt om inhoud van [docs.microsoft.com](https://docs.microsoft.com) op te slaan. GitHub host voor projecten de hoofdopslagplaats waaruit inzenders kopieën voor hun eigen werk kunnen maken.

## <a name="git"></a>Git

Als u vertrouwd bent met gecentraliseerde versiebeheersystemen (zoals Team Foundation Server, SharePoint of Visual SourceSafe), zult u merken dat Git een unieke bijdragewerkstroom en terminologie voor de ondersteuning van het gedistribueerde model heeft. Zo worden bijvoorbeeld bestanden niet vergrendeld wat normaal wel het geval is bij uit- en incheckbewerkingen. Bij Git wordt op een veel gedetailleerder niveau naar wijzigingen gekeken, waarbij bestanden byte voor byte met elkaar worden vergeleken.

Ook wordt bij Git een gelaagde structuur gebruikt om inhoud voor een project op te slaan en te beheren:

- *Opslagplaats*: dit is de hoogste opslageenheid en wordt ook wel een *repository of repo*  genoemd. Een opslagplaats bevat een of meer vertakkingen.
- *Vertakking*: een opslageenheid met de bestanden en mappen die gezamenlijk de inhoudsset van een project vormen. Vertakkingen zorgen voor de scheiding van werkstromen (meestal versies genoemd). Bijdragen worden altijd gemaakt voor en toegewezen aan een specifieke vertakking. Alle opslagplaatsen bevatten een standaardvertakking (meestal de hoofdvertakking genoemd) en een of meer vertakkingen die bedoeld zijn om later te worden samengevoegd met de hoofdvertakking. De hoofdvertakking fungeert als de huidige versie en 'de enige vertrouwde bron' voor het project. Alle andere vertakkingen in de opslagplaats worden hiervan afgeleid.

Inzenders werken met Git om opslagplaatsen op zowel lokaal als op GitHub-niveau te updaten en bewerken:

- Lokaal via hulpmiddelen zoals de Git Bash-console waarmee Git-opdrachten voor het beheer van lokale opslagplaatsen en de communicatie met GitHub-opslagplaatsen kunnen worden gegeven.
- Via [www.github.com](https://www.github.com), waarmee Git wordt geïntegreerd om bijdragen in de hoofdopslagplaats samen te voegen

## <a name="github"></a>GitHub

> [!NOTE]
> Hoewel de Docs-richtlijnen zijn gebaseerd op het gebruik GitHub, gebruiken sommige teams Visual Studio Team Services om Git-opslagplaatsen te hosten. De Visual Studio Team Explorer-client biedt een gebruikersinterface voor interactie met Team Services-opslagplaatsen. Deze interface kunt u gebruiken om Git-opdrachten via een opdrachtregel in te voeren.
> </br>
> Ook zijn veel van de volgende richtlijnen ontwikkeld als aanbevolen procedures op basis van jaren ervaring in het hosten van Azure-service-inhoud in GitHub. Deze zijn mogelijk vereist in bepaalde Docs-opslagplaatsen.

Alle werkstromen beginnen en eindigen op GitHub-niveau waar de hoofdopslagplaats voor een bepaald Docs-project is opgeslagen. De exemplaren die inzenders voor hun eigen gebruik maken, worden op meerdere computers gedistribueerd. Deze exemplaren worden uiteindelijk weer overgebracht naar de belangrijkste GitHub-opslagplaats van het project.

### <a name="directory-organization"></a>Organisatie van mappen

Zoals eerder genoemd, dient de standaardvertakking ('hoofdvertakking') als de huidige versie van de inhoud voor het project. De inhoud van de hoofdvertakking (en vertakkingen die op basis van de hoofdvertakking zijn gemaakt) wordt globaal afgestemd op de organisatie van de artikelen op de bijbehorende Docs-pagina's. Submappen worden gebruikt om soortgelijke inhoud (zoals services), media-inhoud (zoals afbeeldingsbestanden) en include-bestanden voor hergebruik van inhoud te scheiden.

De hoofdmap `articles` bevindt zich meestal direct onder de hoofdmap van de opslagplaats. De map articles bevat een reeks submappen. Artikelen in de submappen zijn opgemaakt als Markdown-bestanden met de extensie *.md*. Sommige opslagplaatsen die ondersteuning bieden voor meerdere services, maken gebruik van een generieke submap `/articles`, bijvoorbeeld de opslagplaats [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs). Andere gebruiken misschien een servicespecifieke naam, zoals de opslagplaats [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs), die `/IntuneDocs` gebruikt.

Direct in deze hoofdmap vindt u algemene artikelen die betrekking hebben op de algehele service of het algehele product. De hoofdmap bevat meestal ook enkele submappen die horen bij de functies/services of bij algemene scenario's. Zo staan de Azure-artikelen over virtuele machines in de submap `/virtual-machines`, de Intune-artikelen uit de sectie Begrijpen en verkennen in de submap `/understand-explore`, enzovoort.

### <a name="media-subdirectory"></a>Submap voor media

Elke artikelmap bevat een submap `/media` voor de overeenkomstige mediabestanden. Mediabestanden bevatten afbeeldingen die worden gebruikt voor artikelen die verwijzingen naar afbeeldingen bevatten.

### <a name="includes-subdirectory"></a>Map met include-bestanden

Wanneer er herbruikbare inhoud is die wordt gedeeld door twee of meer artikelen, wordt deze inhoud opgeslagen in een submap `/includes` buiten de hoofdmap `articles`. In een Markdown-bestand waarvoor het include-bestand wordt gebruikt, wordt een overeenkomende Markdown-extensie include geplaatst op de locatie waar de verwijzing naar het include-bestand moet worden gebruikt.

Zie [Markdown gebruiken: Includes](how-to-write-use-markdown.md#includes) voor aanvullende richtlijnen.

### <a name="markdown-file-template"></a>Sjabloon voor Markdown-bestanden

Voor het gemak bevat de hoofdmap van elke opslagplaats meestal een sjabloon voor Markdown-bestanden met de naam `template.md`. U kunt deze sjabloon gebruiken als basis voor een nieuw artikel dat u wilt verzenden naar de opslagplaats. Het bestand bevat:

- Een **koptekst met metagegevens** boven aan het bestand, afgebakend door twee regels met drie afbreekstreepjes, en verschillende labels die worden gebruikt voor het bijhouden van informatie met betrekking tot het artikel. De metagegevens van het artikel maken bepaalde functies mogelijk, zoals toekenning aan auteur, toekenning aan inzender, breadcrumbs, artikelbeschrijvingen en zoekmachineoptimalisatie. Ook worden de metagegevens gebruikt voor rapportageprocessen waarmee Microsoft de prestaties van de inhoud kan evalueren. De metagegevens zijn dus belangrijk.
- Een sectie met **metagegevens** met de beschrijving van de verschillende labels en waarden voor de metagegevens. Als u niet zeker weet welke waarden u moet gebruiken in de sectie voor metagegevens, kunt u de sectie leeg laten of de waarden markeren als commentaar door er een hashtag (#) voor te plaatsen. De waarden worden dan beoordeeld/voltooid door de revisor van de pull-aanvraag voor de opslagplaats.
- Verschillende **voorbeelden van het gebruik van Markdown** voor het indelen van de elementen van een artikel.
- Algemene **instructies voor het gebruik van Markdown-extensies** die u kunt gebruiken voor diverse waarschuwingstypen.
- Voorbeelden van het **insluiten van video's** met behulp van een iframe.
- Algemene **instructies voor het gebruik van extensies van docs.microsoft.com** die u kunt gebruiken voor speciale besturingselementen, zoals knoppen en selectors.

## <a name="pull-requests"></a>Pull-aanvragen

Een *pull-aanvraag* biedt een handige manier voor een inzender om een set wijzigingen voor te stellen die op de standaardvertakking moet worden toegepast. De wijzigingen (ook wel *doorvoeracties* genoemd) worden opgeslagen in de vertakking van de inzender, zodat GitHub eerst de impact van het *samenvoegen* van deze wijzigingen met de standaardvertakking kan verwerken. Een pull-aanvraag dient ook als mechanisme om de inzender feedback te verschaffen van een build-/validatieproces, de revisor van de pull-aanvraag, om mogelijke problemen op te lossen of vragen te beantwoorden voordat de wijzigingen met de hoofdvertakking worden samengevoegd.

Er zijn twee manieren om bij te dragen via een pull-aanvraag, afhankelijk van de grootte van de wijzigingen die u wilt voorstellen. Dit wordt later in de secties [GitHub-werkstroom](how-to-write-workflows-major.md) van deze gids gedetailleerd besproken.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
