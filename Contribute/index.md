---
title: 'Gids voor inzenders van Microsoft Docs: overzicht'
description: In de handleiding wordt beschreven hoe u kunt bijdragen aan de Microsoft-documentatiesite docs.microsoft.com.
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
---

# <a name="microsoft-docs-contributor-guide-overview"></a>Gids voor inzenders van Microsoft Docs: overzicht

Welkom bij de stijlgids voor [docs.microsoft.com](https://docs.microsoft.com) (ook bekend als Docs).

Meerdere Microsoft-documentatiesets zijn open source en worden gehost op GitHub. Sommige documentatiesets zijn nog niet volledig open source, maar hebben een openbare opslagplaats waarvoor u pull-aanvragen kunt maken. Zo kan de communicatie tussen productengineers, de inhoudsteams en onze klanten worden gestroomlijnd en verbeterd. In het openbaar werken biedt verschillende voordelen:

- Met openbare planning in opensourceopslagplaatsen kan feedback worden verkregen over welke documenten het meest nodig zijn.
- Met openbare controles in opensourceopslagplaatsen kan de inhoud die het nuttigst is, in de eerste versie worden gepubliceerd.
- Met openbare updates in opensourceopslagplaatsen is het eenvoudiger om de inhoud doorlopend te verbeteren.

De gebruikerservaring op [docs.microsoft.com](https://docs.microsoft.com) is rechtstreeks geïntegreerd met werkstromen van [GitHub](https://github.com) om dit nog eenvoudiger te maken. U kunt beginnen door [het document te bewerken dat u bekijkt](#quick-edits-to-existing-documents). Of u kunt helpen door [nieuwe onderwerpen te beoordelen](#review-open-prs) of [kwaliteitsproblemen te melden](#create-quality-issues).

> [!IMPORTANT]
> Op alle opslagplaatsen die naar docs.microsoft.com publiceren, is de [Microsoft Open Source-gedragscode](https://opensource.microsoft.com/codeofconduct/) of de [.NET Foundation-gedragscode](https://dotnetfoundation.org/code-of-conduct) van toepassing. Zie [Veelgestelde vragen over de gedragscode](https://opensource.microsoft.com/codeofconduct/faq/) voor meer informatie. Of neem contact op via [opencode@microsoft.com](mailto:opencode@microsoft.com) of [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) als u vragen of opmerkingen hebt.<br>
>
> Kleine correcties of verduidelijkingen voor de documentatie en codevoorbeelden in de openbare opslagplaatsen vallen onder de [gebruiksvoorwaarden van docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Bij nieuwe inhoud of belangrijke wijzigingen wordt een opmerking gegenereerd in de pull-aanvraag, waarin u wordt gevraagd om online een gebruiksrechtovereenkomst voor bijdrage (CLA) in te dienen als u geen werknemer van Microsoft bent. U moet het onlineformulier invullen voordat we uw pull-aanvraag kunnen beoordelen of accepteren.

## <a name="quick-edits-to-existing-documents"></a>Snelle bewerkingen van bestaande documenten

Met snelle bewerkingen wordt het proces voor het rapporteren en herstellen van kleine fouten en weglatingen in documenten gestroomlijnd. Ondanks alle moeite kunnen toch kleine grammatica- en spelfouten in uw gepubliceerde documenten opduiken. U kunt fouten rapporteren door een probleemmelding te maken. Als deze optie beschikbaar is, kunt u problemen echter ook melden via een pull-aanvraag. Dat is sneller en eenvoudiger.

1. Op sommige documentatiepagina's kunt u rechtstreeks in de browser inhoud bewerken. Als dat het geval is, wordt de knop **Bewerken** weergegeven. Zie het voorbeeld hieronder. Wanneer u op de knop **Bewerken** (of de gelokaliseerde equivalent hiervan) klikt, gaat u naar het bronbestand op GitHub. Als u de knop **Bewerken** (potloodpictogram) niet ziet, betekent dit dat de documentatiepagina niet kan worden gewijzigd.

   ![Locatie van de link Bewerken](./media/index/edit-article.png)

2. Klik vervolgens op het potloodpictogram om het artikel te bewerken zoals hieronder wordt weergegeven. Als het potloodpictogram grijs wordt weergegeven, moet u bij uw GitHub-account aanmelden of een nieuw account maken. 

   ![Locatie van het potloodpictogram](./media/index/edit-icon.png)


3. Breng uw wijzigingen aan in de webeditor. Klik op **Voorbeeld van wijzigingen** om de opmaak van uw wijziging te controleren.

4. Zodra u uw wijzigingen hebt aangebracht, scrolt u naar de onderkant van de pagina. Voer een titel en een beschrijving in voor uw wijzigingen en klik op **Bestandswijziging voorstellen**, zoals aangegeven in de volgende afbeelding:

   ![Bestandswijziging voorstellen](./media/index/submit-pull-request.png)

5. Nu u de wijziging hebt voorgesteld, moet u de eigenaars van de opslagplaats vragen om de wijzigingen naar hun opslagplaats te halen. Dit gebeurt met een zogenaamde pull-aanvraag. Wanneer u in de afbeelding hierboven op **Bestandswijziging voorstellen** klikt, wordt u naar een nieuwe pagina geleid die er ongeveer uitziet als de volgende afbeelding:

   ![pull-aanvraag maken](media/index/create-pull-request.png)

   Klik op **Pull-aanvraag maken**, voer een titel (en optioneel een beschrijving) in voor de pull-aanvraag. Klik vervolgens opnieuw op **Pull-aanvraag maken**.

6. Dat is alles. Uw PR wordt door leden van het inhoudsteam gecontroleerd en samengevoegd. Als u grotere wijzigingen hebt aangebracht, krijgt u misschien feedback waarin u wordt gevraagd om wijzigingen aan te brengen.

De gebruikersinterface voor GitHub-bewerkingen reageert op uw machtigingen voor de opslagplaats. De voorgaande afbeeldingen gelden voor inzenders die geen schrijfmachtigingen hebben voor de doelopslagplaats. In GitHub wordt automatisch een fork van de doelopslagplaats gemaakt in uw account. Als u schrijfrechten hebt voor de doelopslagplaats, wordt in GitHub een nieuwe vertakking in de doelopslagplaats gemaakt. De naam van de vertakking heeft de indeling **\<GitHubId\>-patch-n**, waarbij uw GitHub-id en een numerieke id worden gebruikt voor de vertakking van de patch.

De pull-aanvragen worden gebruikt voor alle wijzigingen en dus ook voor inzenders die over schrijfrechten beschikken. Bij de meeste opslagplaatsen is de `master`-vertakking beschermd, zodat updates als pull-aanvragen moeten worden verzonden.

Voor kleinere of incidentele wijzigingen kunt u het beste de bewerkingservaring binnen browsers gebruiken. Als u grote bijdrage levert of geavanceerde Git-functies gebruikt (zoals vertakkingsbeheer of geavanceerde oplossingen voor samenvoegingsconflicten), moet u de [opslagplaats splitsen en lokaal werken](how-to-write-workflows-major.md).

> [!NOTE]
> Als deze functie is ingeschakeld, kunt u een artikel in **elke taal** bewerken. Afhankelijk van het soort bewerking gebeurt dan het volgende:
> 1. elke taalkundige wijziging die is doorgevoerd, helpt ook bij het verbeteren van onze Machine Translation-engine
> 2. elke bewerking waardoor de inhoud van een artikel significant wordt gewijzigd, wordt intern verwerkt om een wijziging in hetzelfde artikel in het Engels te verzenden. Op deze manier wordt de wijziging, indien goedgekeurd, in alle talen gelokaliseerd.
> Uw voorgestelde wijzigingen beïnvloeden artikelen dus niet alleen positief in uw eigen taal, maar in alle beschikbare talen.

## <a name="review-open-prs"></a>Openstaande PR's controleren

U kunt nieuwe onderwerpen lezen voordat deze zijn gepubliceerd door de momenteel openstaande PR's te controleren. Bij controles wordt het proces van de [GitHub-workflow](https://guides.github.com/introduction/flow/) gevolgd. U kunt voorgestelde updates of nieuwe artikelen in openbare opslagplaatsen bekijken. Controleer deze en voeg uw opmerkingen toe. Ga naar onze opslagplaatsen voor documentatie en bekijk de openstaande pull-aanvragen voor gebieden die interessant zijn voor u. Feedback uit de community over voorgestelde updates is nuttig voor de gehele community.

## <a name="create-quality-issues"></a>Kwaliteitsproblemen maken

Onze documentatie wordt doorlopend aangevuld en verbeterd. Dankzij goede probleemmeldingen kunnen we onze inspanningen richten op de hoogste prioriteiten van de community. Hoe gedetailleerder deze zijn, des te nuttiger is de probleemmelding. Vertel ons naar welke informatie u op zoek was. Vertel ons welke zoektermen u hebt gebruikt. Vertel ons, als u niet aan de slag kunt, hoe u wilt beginnen met het verkennen van onbekende technologie.

Veel van de documentatiepagina's van Microsoft bevatten onderaan een gedeelte **Feedback**. Hier kunt u op klikken om **productfeedback** of **inhoudsfeedback** te geven met betrekking tot problemen in het artikel.

Probleemmeldingen zijn het startpunt om te bespreken wat er nodig is. Het inhoudsteam reageert op deze probleemmeldingen met ideeën over wat we kunnen toevoegen, en vraagt om uw mening. Wanneer we een concept maken, vragen we u om [de PR te beoordelen](#review-open-prs).

## <a name="get-more-involved"></a>Meer betrokken raken

Er zijn onderwerpen beschikbaar die u kunt gebruiken om productief bij te dragen aan Microsoft Docs. In deze onderwerpen wordt uitgelegd hoe u werkt met GitHub-opslagplaatsen, Markdown-hulpprogramma's en de extensies die worden gebruikt voor het Microsoft Docs-platform.
