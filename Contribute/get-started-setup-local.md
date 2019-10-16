---
title: Git-opslagplaats lokaal instellen
description: Dit artikel biedt ondersteuning bij het maken van uw lokale Git-opslagplaats om bij te dragen aan documentatie. Ook het splits- en kloonproces wordt hier beschreven.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: e73c60c439285f901c5c83e538f8971d795bd6c4
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288607"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>Een lokale Git-opslagplaats voor documentatie instellen

In dit artikel worden de stappen beschreven om een Git-opslagplaats op uw lokale machine in te stellen, met het doel bij te dragen aan de documentatie van Microsoft. Inzenders kunnen een lokaal gekloonde opslagplaats gebruiken om nieuwe artikelen toe te voegen, omvangrijke wijzigingen aan te brengen in bestaande artikelen of illustraties aan te passen.

Voor u kunt bijdragen, moet u de volgende eenmalige installatiestappen uitvoeren:
> [!div class="checklist"]
> * De juiste opslagplaats bepalen
> * Een fork instellen van de opslagplaats naar uw GitHub-account
> * Een lokale map voor de gekloonde bestanden kiezen
> * De opslagplaats op uw lokale machine klonen
> * De externe upstreamwaarde configureren

> [!IMPORTANT]
> Als u slechts kleine wijzigingen aan een artikel aanbrengt, hoeft u de stappen in dit artikel *niet* te voltooien. U kunt meteen doorgaan naar de [werkstroom voor snelle wijzigingen](index.md#quick-edits-to-existing-documents).
>

## <a name="overview"></a>Overzicht

Als u wilt bijdragen aan de documentatiesite van Microsoft, kunt u lokaal Markdown-bestanden maken en bewerken door de bijbehorende documentatieopslagplaats te klonen. Microsoft vereist dat u een fork maakt tussen de juiste opslagplaats en uw eigen GitHub-account, zodat u beschikt over lees-/schrijfmachtigingen om de voorgestelde wijzigingen op te slaan. Vervolgens gebruikt u pull-aanvragen om uw wijzigingen door te voeren in de centraal gedeelde alleen-lezenopslagplaats.

![GitHub-driehoek](./media/git-and-github-initial-setup.png)

Als u nog niet eerder met GitHub hebt gewerkt, bekijkt u de volgende video voor een conceptueel overzicht van het splits- en kloonproces:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>De opslagplaats bepalen

De documentatie die op [docs.microsoft.com](https://docs.microsoft.com) wordt gehost, bevindt zich in diverse opslagplaatsen op [github.com](https://www.github.com).

1. Als u niet zeker weet welke opslagplaats u moet gebruiken, zoekt u in uw webbrowser naar het betreffende artikel op [docs.microsoft.com](https://docs.microsoft.com). Selecteer de koppeling **Edit** (potloodpictogram) in de rechterbovenhoek van het artikel.

   ![Klik op Edit om de opslagplaats en de bestandslocatie te bepalen.](media/index/edit-article.png)

2. De koppeling brengt u naar de github.com-locatie van het bijbehorende Markdown-bestand in de juiste opslagplaats. Bekijk de URL om de naam van de opslagplaats te bepalen.

   ![Bekijk de URL om de locatie van de opslagplaats te bepalen.](media/public-repo.png)

   Deze populaire opslagplaatsen zijn bijvoorbeeld beschikbaar voor openbare bijdragen:
   - Documentatie over Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - Documentatie over SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Documentatie over Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - Documentatie over .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Documentatie over Azure .NET SDK[https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   - Documentatie over ConfigMGR[https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)

## <a name="fork-the-repository"></a>De opslagplaats splitsen
Maak met behulp van de juiste opslagplaats een fork van de opslagplaats naar uw eigen GitHub-account via de GitHub-website.

Een persoonlijke fork is vereist omdat alle hoofdopslagplaatsen voor documentatie alleen-lezentoegang bieden. Als u een wijziging wilt aanbrengen, moet u via uw fork een [pull-aanvraag](git-github-fundamentals.md#pull-requests) indienen bij de hoofdopslagplaats. Voor het vereenvoudigen van dit proces moet u van de opslagplaats eerst een kopie voor uzelf maken waarin u schrijftoegang hebt. Hiervoor is een *fork* van GitHub geschikt.

1. Ga naar de GitHub-pagina van de hoofdopslagplaats en klik op de knop **Fork** rechtsboven.

   ![Voorbeeld van een GitHub-profiel](./media/contribute-get-started-setup-local/fork.png)

2. Wanneer u hierom wordt gevraagd, selecteert u de tegel voor uw GitHub-account als de doellocatie waar de fork moet worden gemaakt. Hiermee wordt binnen uw GitHub-account een kopie gemaakt van de opslagplaats, ook wel een fork genoemd.

## <a name="choose-a-local-folder"></a>Lokale map kiezen
Maak een lokale map waarin u de lokale kopie van de opslagplaats wilt opslaan. Sommige opslagplaatsen kunnen erg groot zijn; bijvoorbeeld tot wel 5 GB voor Azure-documenten. Kies een locatie met beschikbare schijfruimte.

1. Kies een mapnaam die u gemakkelijk kunt onthouden en invoeren. Kies bijvoorbeeld een hoofdmap `C:\docs\` of maak een map in de map `~/Documents/docs/` van uw gebruikersprofiel

   > [!IMPORTANT]
   > Kies geen pad naar een lokale map dat al deel uitmaakt van een maplocatie voor een andere Git-opslagplaats. U kunt wel de gekloonde Git-mappen naast elkaar opslaan, maar als u Git-mappen in elkaar nest, ontstaan fouten tijdens het bijhouden van bestanden.

2. Git Bash openen

   ![Git Bash openen](./media/contribute-get-started-setup-local/gitbash-start.png)

   De standaardlocatie waarin Git Bash start, is doorgaans de thuismap (~) of `/c/users/<Windows-user-account>/` in het Windows-besturingssysteem.

   Voer bij de $-prompt `pwd` in om de huidige map te bepalen. 

3. Wijzig de map (cd) in de map die u hebt gemaakt voor het lokaal hosten van de opslagplaats. Let op: Git Bash gebruikt voor mappaden de Linux-conventie waarbij schuine strepen naar rechts wijzen in plaats van naar links.

   Bijvoorbeeld `cd /c/docs/ ` of `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>Een lokale kloon maken

Bereid met behulp van Git Bash het uitvoeren van de opdracht **clone** voor om een kopie van een opslagplaats (uw fork) naar de huidige map op uw apparaat te kopiëren. 

### <a name="authenticate-by-using-git-credential-manager"></a>Verifiëren met behulp van Git Credential Manager
Als u de recentste versie van Git voor Windows hebt geïnstalleerd en de standaardinstallatie hebt geaccepteerd, is Git Credential Manager standaard ingeschakeld. Git Credential Manager maakt verificatie veel eenvoudiger, omdat u uw persoonlijke toegangstoken niet hoeft in te trekken wanneer u geverifieerde verbindingen en remotes met GitHub opnieuw tot stand brengt.

1. Voer de opdracht **clone** uit door de naam van de opslagplaats op te geven. Door de kloonactie wordt de geforkte opslagplaats naar uw lokale computer gedownload (gekloond). 

    > [!Tip]
    > U kunt de GitHub-URL van uw fork voor de kloonopdracht ophalen met de knop **Klonen of downloaden** in de gebruikersinterface van GitHub:
    >
    > ![Klonen of downloaden](./media/contribute-get-started-setup-local/clone-or-download.png)

    Zorg ervoor dat u tijdens het klonen het pad naar *uw fork* opgeeft, en niet naar de hoofdopslagplaats waarvandaan u de fork hebt gemaakt. Als u dit niet doet, kunt u geen wijzigingen bijdragen. Naar uw fork wordt verwezen met uw persoonlijke GitHub-gebruikersaccount, zoals `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Uw kloonopdracht ziet er dan bijvoorbeeld als volgt uit:

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. Voer uw GitHub-referenties in wanneer dit wordt gevraagd.

    ![Aanmelding bij GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. Voer uw tweeledige verificatiecode in wanneer dit wordt gevraagd.

    ![Tweeledige verificatie bij GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Uw referenties worden opgeslagen en gebruikt voor het verifiëren van toekomstige GitHub-aanvragen. U hoeft deze verificatie slechts één keer per computer uit te voeren. 

4. De kloonopdracht voert een kopie van de bestanden van de opslagplaats uit en downloadt deze van uw fork naar een nieuwe map op de lokale schijf. In de huidige map wordt een nieuwe map gemaakt. Dit kan, afhankelijk van de grootte van de opslagplaats, enkele minuten duren. U kunt de map verkennen om de structuur ervan te zien zodra deze bewerking is voltooid.

## <a name="configure-remote-upstream"></a>Externe upstream configureren
Nadat u de opslagplaats hebt gekloond, stelt u externe alleen-lezenverbinding in met de hoofdopslagplaats. Deze heeft de naam **upstream**. U gebruikt de upstream-URL om uw lokale opslagplaats gesynchroniseerd te houden met de recentste wijzigingen van anderen. De opdracht **git remote** wordt gebruikt om de configuratiewaarde in te stellen. Gebruik de opdracht **fetch** om de vertakkingsinformatie op te halen van de upstreamopslagplaats.

1. Als u **Git Credential Manager** gebruikt, gebruikt u de volgende opdrachten. Vervang de tijdelijke aanduidingen \<repo\> en \<organisation\>.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Bekijk de geconfigureerde waarden en bevestig dat de URL's juist zijn. Controleer of de **origin**-URL's naar uw persoonlijke fork verwijzen. Controleer of de **upstream**-URL's naar de hoofdopslagplaats verwijzen, zoals MicrosoftDocs of Azure. 
   ```bash
   git remote -v 
   ```

   Er wordt een voorbeeld van externe uitvoer weergegeven. Een fictief Git-account met de naam MyGitAccount wordt geconfigureerd met een persoonlijk toegangstoken voor toegang tot de repo Azure-documenten:
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Als u een fout hebt gemaakt, kunt u de externe waarde verwijderen. Als u de upstreamwaarde wilt verwijderen, voert u de opdracht `git remote remove upstream` uit.

## <a name="next-steps"></a>Volgende stappen
- Ga naar de pagina [GitHub-bijdragewerkstroom](how-to-write-workflows-major.md) voor meer informatie over het toevoegen en bijwerken van inhoud.
