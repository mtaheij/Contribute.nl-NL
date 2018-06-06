---
title: Git-opslagplaats lokaal instellen
description: Dit artikel biedt ondersteuning bij het maken van uw lokale Git-opslagplaats om bij te dragen aan documentatie. Ook het splits- en kloonproces wordt hier beschreven.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: f702d0d29ee7dc9c69cb26b79bf6283d91b6b6bc
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469757"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="31666-103">Een lokale Git-opslagplaats voor documentatie instellen</span><span class="sxs-lookup"><span data-stu-id="31666-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="31666-104">In dit artikel worden de stappen beschreven om een Git-opslagplaats op uw lokale machine in te stellen, met het doel bij te dragen aan de documentatie van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31666-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="31666-105">Inzenders kunnen een lokaal gekloonde opslagplaats gebruiken om nieuwe artikelen toe te voegen, omvangrijke wijzigingen aan te brengen in bestaande artikelen of illustraties aan te passen.</span><span class="sxs-lookup"><span data-stu-id="31666-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="31666-106">Voor u kunt bijdragen, moet u de volgende eenmalige installatiestappen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="31666-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="31666-107">De juiste opslagplaats bepalen</span><span class="sxs-lookup"><span data-stu-id="31666-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="31666-108">Een fork instellen van de opslagplaats naar uw GitHub-account</span><span class="sxs-lookup"><span data-stu-id="31666-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="31666-109">Een lokale map voor de gekloonde bestanden kiezen</span><span class="sxs-lookup"><span data-stu-id="31666-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="31666-110">De opslagplaats op uw lokale machine klonen</span><span class="sxs-lookup"><span data-stu-id="31666-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="31666-111">De externe upstreamwaarde configureren</span><span class="sxs-lookup"><span data-stu-id="31666-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31666-112">Als u slechts kleine wijzigingen aan een artikel aanbrengt, hoeft u de stappen in dit artikel *niet* te voltooien.</span><span class="sxs-lookup"><span data-stu-id="31666-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="31666-113">U kunt meteen doorgaan naar de [werkstroom voor snelle wijzigingen](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="31666-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="31666-114">Overzicht</span><span class="sxs-lookup"><span data-stu-id="31666-114">Overview</span></span>

<span data-ttu-id="31666-115">Als u wilt bijdragen aan de documentatiesite van Microsoft, kunt u lokaal Markdown-bestanden maken en bewerken door de bijbehorende documentatieopslagplaats te klonen.</span><span class="sxs-lookup"><span data-stu-id="31666-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="31666-116">Microsoft vereist dat u een fork maakt tussen de juiste opslagplaats en uw eigen GitHub-account, zodat u beschikt over lees-/schrijfmachtigingen om de voorgestelde wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="31666-116">Microsoft requires you to fork the appropriate repository into your own github account, so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="31666-117">Vervolgens gebruikt u pull-aanvragen om uw wijzigingen door te voeren in de centraal gedeelde alleen-lezenopslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub-driehoek](./media/git-and-github-initial-setup.png)

<span data-ttu-id="31666-119">Als u nog niet eerder met GitHub hebt gewerkt, bekijkt u de volgende video voor een conceptueel overzicht van het splits- en kloonproces:</span><span class="sxs-lookup"><span data-stu-id="31666-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="31666-120">De opslagplaats bepalen</span><span class="sxs-lookup"><span data-stu-id="31666-120">Determine the repository</span></span>

<span data-ttu-id="31666-121">De documentatie die op [docs.microsoft.com](https://docs.microsoft.com) wordt gehost, bevindt zich in diverse opslagplaatsen op [github.com](https://www.github.com).</span><span class="sxs-lookup"><span data-stu-id="31666-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="31666-122">Als u niet zeker weet welke opslagplaats u moet gebruiken, zoekt u in uw webbrowser naar het betreffende artikel op docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="31666-122">If you are unsure of which repository to use, then visit the article on docs.microsoft.com using your web browser.</span></span> <span data-ttu-id="31666-123">Selecteer de koppeling **Edit** (potloodpictogram) in de rechterbovenhoek van het artikel.</span><span class="sxs-lookup"><span data-stu-id="31666-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Klik op Edit om de opslagplaats en de bestandslocatie te bepalen.](media/index/edit-article.png)

2. <span data-ttu-id="31666-125">De koppeling brengt u naar de github.com-locatie van het bijbehorende Markdown-bestand in de juiste opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="31666-126">Bekijk de URL om de naam van de opslagplaats te bepalen.</span><span class="sxs-lookup"><span data-stu-id="31666-126">Note the URL to view the repository name.</span></span>

   ![Bekijk de URL om de locatie van de opslagplaats te bepalen.](media/public-repo.png)

   <span data-ttu-id="31666-128">Deze populaire opslagplaatsen zijn bijvoorbeeld beschikbaar voor openbare bijdragen:</span><span class="sxs-lookup"><span data-stu-id="31666-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="31666-129">Documentatie over Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="31666-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="31666-130">Documentatie over SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="31666-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="31666-131">Documentatie over Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="31666-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="31666-132">Documentatie over .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="31666-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="31666-133">Documentatie over Azure .NET SDK[https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="31666-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="31666-134">De opslagplaats splitsen</span><span class="sxs-lookup"><span data-stu-id="31666-134">Fork the repository</span></span>
<span data-ttu-id="31666-135">Maak met behulp van de juiste opslagplaats een fork van de opslagplaats naar uw eigen GitHub-account via de GitHub-website.</span><span class="sxs-lookup"><span data-stu-id="31666-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="31666-136">U hebt een persoonlijke fork nodig omdat alle hoofdopslagplaatsen voor documenten alleen-lezentoegang bieden. Dit houdt in dat u niet rechtstreeks wijzigingen kunt aanbrengen in de inhoud van de opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="31666-136">A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories.</span></span> <span data-ttu-id="31666-137">Als u een wijziging wilt aanbrengen, moet u via uw fork een [pull-aanvraag](git-github-fundamentals.md#pull-requests) indienen bij de hoofdopslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="31666-138">Voor het vereenvoudigen van dit proces moet u van de opslagplaats eerst een kopie voor uzelf maken waarin u schrijftoegang hebt.</span><span class="sxs-lookup"><span data-stu-id="31666-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="31666-139">Hiervoor is een *fork* van GitHub geschikt.</span><span class="sxs-lookup"><span data-stu-id="31666-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="31666-140">Ga naar de GitHub-pagina van de hoofdopslagplaats en klik op de knop **Fork** rechtsboven.</span><span class="sxs-lookup"><span data-stu-id="31666-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Voorbeeld van een GitHub-profiel](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="31666-142">Wanneer u hierom wordt gevraagd, selecteert u de tegel voor uw GitHub-account als de doellocatie waar de fork moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31666-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="31666-143">Hiermee wordt binnen uw GitHub-account een kopie gemaakt van de opslagplaats, ook wel een fork genoemd.</span><span class="sxs-lookup"><span data-stu-id="31666-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="31666-144">Lokale map kiezen</span><span class="sxs-lookup"><span data-stu-id="31666-144">Choose a local folder</span></span>
<span data-ttu-id="31666-145">Maak een lokale map waarin u de lokale kopie van de opslagplaats wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="31666-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="31666-146">Sommige opslagplaatsen kunnen erg groot zijn; bijvoorbeeld tot wel 5 GB voor Azure-documenten.</span><span class="sxs-lookup"><span data-stu-id="31666-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="31666-147">Kies een locatie met beschikbare schijfruimte.</span><span class="sxs-lookup"><span data-stu-id="31666-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="31666-148">Kies een mapnaam die u gemakkelijk kunt onthouden en invoeren.</span><span class="sxs-lookup"><span data-stu-id="31666-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="31666-149">Kies bijvoorbeeld een hoofdmap `C:\docs\` of maak een map in de map `~/Documents/docs/` van uw gebruikersprofiel</span><span class="sxs-lookup"><span data-stu-id="31666-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="31666-150">Kies geen pad naar een lokale map dat al deel uitmaakt van een maplocatie voor een andere Git-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="31666-151">U kunt wel de gekloonde Git-mappen naast elkaar opslaan, maar als u Git-mappen in elkaar nest, ontstaan fouten tijdens het bijhouden van bestanden.</span><span class="sxs-lookup"><span data-stu-id="31666-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="31666-152">Git Bash openen</span><span class="sxs-lookup"><span data-stu-id="31666-152">Launch Git Bash</span></span>

   ![Git Bash openen](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="31666-154">De standaardlocatie waarin Git Bash start, is doorgaans de thuismap (~) of `/c/users/<Windows-user-account>/` in het Windows-besturingssysteem.</span><span class="sxs-lookup"><span data-stu-id="31666-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="31666-155">Voer bij de $-prompt `pwd` in om de huidige map te bepalen.</span><span class="sxs-lookup"><span data-stu-id="31666-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="31666-156">Wijzig de map (cd) in de map die u hebt gemaakt voor het lokaal hosten van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="31666-157">Let op: Git Bash gebruikt voor mappaden de Linux-conventie waarbij schuine strepen naar rechts wijzen in plaats van naar links.</span><span class="sxs-lookup"><span data-stu-id="31666-157">Note that Git Bash uses Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="31666-158">Bijvoorbeeld `cd /c/docs/ ` of `cd ~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="31666-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="31666-159">Een lokale kloon maken</span><span class="sxs-lookup"><span data-stu-id="31666-159">Create a local clone</span></span>

<span data-ttu-id="31666-160">Bereid met behulp van Git Bash het uitvoeren van de opdracht **clone** voor om een kopie van een opslagplaats (uw fork) naar de huidige map op uw apparaat te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="31666-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="31666-161">Verifiëren met behulp van Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="31666-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="31666-162">Als u de recentste versie van Git voor Windows hebt geïnstalleerd en de standaardinstallatie hebt geaccepteerd, is Git Credential Manager standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="31666-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="31666-163">Git Credential Manager maakt verificatie veel eenvoudiger, omdat u uw persoonlijke toegangstoken niet hoeft in te trekken wanneer u geverifieerde verbindingen en remotes met GitHub opnieuw tot stand brengt.</span><span class="sxs-lookup"><span data-stu-id="31666-163">Git Credential Manager makes authentication much easier, because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="31666-164">Voer de opdracht **clone** uit door de naam van de opslagplaats op te geven.</span><span class="sxs-lookup"><span data-stu-id="31666-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="31666-165">Door de kloonactie wordt de geforkte opslagplaats naar uw lokale computer gedownload (gekloond).</span><span class="sxs-lookup"><span data-stu-id="31666-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="31666-166">U kunt de GitHub-URL van uw fork voor de kloonopdracht ophalen met de knop **Klonen of downloaden** in de gebruikersinterface van GitHub:</span><span class="sxs-lookup"><span data-stu-id="31666-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Klonen of downloaden](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="31666-168">Zorg ervoor dat u tijdens het klonen het pad naar *uw fork* opgeeft, en niet naar de hoofdopslagplaats waarvandaan u de fork hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31666-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="31666-169">Als u dit niet doet, kunt u geen wijzigingen bijdragen.</span><span class="sxs-lookup"><span data-stu-id="31666-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="31666-170">Naar uw fork wordt verwezen met uw persoonlijke GitHub-gebruikersaccount, zoals `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="31666-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="31666-171">Uw kloonopdracht ziet er dan bijvoorbeeld als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="31666-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="31666-172">Voer uw GitHub-referenties in wanneer dit wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="31666-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![Aanmelding bij GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="31666-174">Voer uw tweeledige verificatiecode in wanneer dit wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="31666-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![Tweeledige verificatie bij GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="31666-176">Uw referenties worden opgeslagen en gebruikt voor het verifiëren van toekomstige GitHub-aanvragen.</span><span class="sxs-lookup"><span data-stu-id="31666-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="31666-177">U hoeft deze verificatie slechts één keer per computer uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="31666-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="31666-178">De kloonopdracht voert een kopie van de bestanden van de opslagplaats uit en downloadt deze van uw fork naar een nieuwe map op de lokale schijf.</span><span class="sxs-lookup"><span data-stu-id="31666-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="31666-179">In de huidige map wordt een nieuwe map gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31666-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="31666-180">Dit kan, afhankelijk van de grootte van de opslagplaats, enkele minuten duren.</span><span class="sxs-lookup"><span data-stu-id="31666-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="31666-181">U kunt de map verkennen om de structuur ervan te zien zodra deze bewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="31666-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="31666-182">Externe upstream configureren</span><span class="sxs-lookup"><span data-stu-id="31666-182">Configure remote upstream</span></span>
<span data-ttu-id="31666-183">Nadat u de opslagplaats hebt gekloond, stelt u externe alleen-lezenverbinding in met de hoofdopslagplaats. Deze heeft de naam **upstream**.</span><span class="sxs-lookup"><span data-stu-id="31666-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="31666-184">U gebruikt de upstream-URL om uw lokale opslagplaats gesynchroniseerd te houden met de recentste wijzigingen van anderen.</span><span class="sxs-lookup"><span data-stu-id="31666-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="31666-185">De opdracht **git remote** wordt gebruikt om de configuratiewaarde in te stellen.</span><span class="sxs-lookup"><span data-stu-id="31666-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="31666-186">Gebruik de opdracht **fetch** om de vertakkingsinformatie op te halen van de upstreamopslagplaats.</span><span class="sxs-lookup"><span data-stu-id="31666-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="31666-187">Als u **Git Credential Manager** gebruikt, gebruikt u de volgende opdrachten.</span><span class="sxs-lookup"><span data-stu-id="31666-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="31666-188">Vervang de tijdelijke aanduidingen \<repo\> en \<organisation\>.</span><span class="sxs-lookup"><span data-stu-id="31666-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="31666-189">Bekijk de geconfigureerde waarden en bevestig dat de URL's juist zijn.</span><span class="sxs-lookup"><span data-stu-id="31666-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="31666-190">Controleer of de **origin**-URL's naar uw persoonlijke fork verwijzen.</span><span class="sxs-lookup"><span data-stu-id="31666-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="31666-191">Controleer of de **upstream**-URL's naar de hoofdopslagplaats verwijzen, zoals MicrosoftDocs of Azure.</span><span class="sxs-lookup"><span data-stu-id="31666-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="31666-192">Er wordt een voorbeeld van externe uitvoer weergegeven.</span><span class="sxs-lookup"><span data-stu-id="31666-192">Example remote output is shown.</span></span> <span data-ttu-id="31666-193">Een fictief Git-account met de naam MyGitAccount wordt geconfigureerd met een persoonlijk toegangstoken voor toegang tot de repo Azure-documenten:</span><span class="sxs-lookup"><span data-stu-id="31666-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="31666-194">Als u een fout hebt gemaakt, kunt u de externe waarde verwijderen.</span><span class="sxs-lookup"><span data-stu-id="31666-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="31666-195">Als u de upstreamwaarde wilt verwijderen, voert u de opdracht `git remote remove upstream` uit.</span><span class="sxs-lookup"><span data-stu-id="31666-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="31666-196">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="31666-196">Next steps</span></span>
- <span data-ttu-id="31666-197">Ga naar de pagina [GitHub-bijdragewerkstroom](how-to-write-workflows-major.md) voor meer informatie over het toevoegen en bijwerken van inhoud.</span><span class="sxs-lookup"><span data-stu-id="31666-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>