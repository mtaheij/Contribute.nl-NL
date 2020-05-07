---
title: Docs-ontwerppakket voor Visual Studio Code
description: In dit artikel wordt het extensiepakket van Visual Studio Code beschreven waarmee u Markdown voor docs.microsoft.com kunt ontwerpen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336407"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs-ontwerppakket voor VS Code

Het Docs-ontwerppakket is een verzameling extensies voor VS Code die u kunt gebruiken bij het schrijven van Markdown voor docs.microsoft.com. Het pakket is [verkrijgbaar via de VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) en bevat de volgende extensies:

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Biedt hulp bij het schrijven van Markdown voor inhoud op docs.microsoft.com (Docs), inclusief fundamentele Markdown-ondersteuning en ondersteuning voor aangepaste Markdown-syntaxis in Docs, zoals waarschuwingen, codefragmenten en niet-lokaliseerbare tekst. Bevat nu ook enkele basisondersteuning voor het aanpassen van YAML, zoals het invoegen van vermeldingen in de inhoudsopgave.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): een populaire Markdown-linter van David Anson zodat u zeker weet dat uw Markdown geldig is.
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): een spellingcontrole van Street Side Software die volledig offline is.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): gebruikt de CSS op docs.microsoft.com voor een nauwkeuriger Markdown-voorbeeld, inclusief aangepaste Markdown.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): hiermee kunnen gebruikers Learn-modules maken en inhoud uit het Markdown-raamwerk toepassen op nieuwe bestanden.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): biedt Docs YAML-schemavalidatie en automatisch aanvullen.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): biedt afbeeldingscompressie en wijzigen van het formaat van mappen en afzonderlijke bestanden om auteurs van docs.microsoft.com te helpen.

## <a name="prerequisites-and-assumptions"></a>Vereisten en aannames

Voor het invoegen van relatieve koppelingen, afbeeldingen en andere ingesloten inhoud met de Docs Markdown-extensie moet de VS Code-werkruimte zijn ingesteld op de hoofdmap van de gekloonde OPS-opslagplaats (Open Publishing System). Als u bijvoorbeeld de Docs-opslagplaats hebt gekloond naar `C:\git\SomeDocsRepo\`, opent u die map of een submap in VS code: via het menu **Bestand** > **map openen** of `code C:\git\SomeDocsRepo\` via de opdrachtregel.

Sommige syntaxissen die door de extensie worden ondersteund, zoals waarschuwingen en codefragmenten, bestaan uit aangepaste Markdown voor OPS. Aangepaste Markdown wordt niet goed weergegeven, tenzij u deze via OPS publiceert.

## <a name="how-to-use-the-docs-markdown-extension"></a>De Docs Markdown-extensie gebruiken

Druk op <kbd>ALT+M</kbd> voor toegang tot het menu **Docs Markdown**. U kunt klikken of de pijl-omhoog en pijl-omlaag gebruiken om de gewenste opdracht te selecteren. U kunt ook typen om te beginnen met filteren en vervolgens op <kbd>ENTER</kbd> drukken wanneer de gewenste functie in het menu is gemarkeerd.

Raadpleeg het [Leesmij-bestand voor Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) voor een bijgewerkte lijst met opdrachten.

## <a name="how-to-generate-a-master-redirect-file"></a>Een hoofdbestand voor de omleiding genereren

De Docs Markdown-extensie bevat een script voor het genereren of bijwerken van een hoofdbestand voor de omleiding voor een opslagplaats op basis van de `redirect_url`-metagegevens in afzonderlijke bestanden. Met dit script wordt elk Markdown-bestand in de opslagplaats voor `redirect_url` gecontroleerd, worden de metagegevens van de omleiding toegevoegd aan het omleidingshoofdbestand ( *.openpublishing.redirection.json*) voor de opslagplaats en worden de omgeleide bestanden verplaatst naar een map buiten de opslagplaats. Het script uitvoeren:

1. Druk op <kbd>F1</kbd> om het opdrachtenpalet van VS Code te openen.
2. Typ 'Docs: Genereren..'
3. Selecteer de opdracht `Docs: Generate master redirection file`.
4. Wanneer het script is voltooid, worden de resultaten van de omleiding weergegeven in het uitvoerdeelvenster van VS Code en worden de verwijderde Markdown-bestanden toegevoegd aan de map Docs Authoring\redirects onder uw standaardpad.
5. Bekijk de resultaten. Als de resultaten naar verwachting zijn, verzendt u een pull-aanvraag om de opslagplaats bij te werken.

## <a name="how-to-assign-keyboard-shortcuts"></a>Sneltoetsen toewijzen

1. Druk op <kbd>CTRL+K</kbd> en vervolgens op <kbd>Ctrl+S</kbd> om de lijst met **sneltoetsen** te openen.
1. Zoek de opdracht, zoals `formatBold`, waarvoor u een aangepaste toetsencombinatie wilt maken.
1. Klik op het plusteken dat naast de naam van de opdracht verschijnt wanneer u met de cursor over de regel beweegt.
1. Zodra een nieuw invoervak zichtbaar is, typt u de sneltoets die u aan die specifieke opdracht wilt koppelen. Druk bijvoorbeeld op <kbd>Ctrl+B</kbd> om de gebruikelijke sneltoets voor vetgedrukte tekst te gebruiken.
1. Het kan handig zijn om een `when`-component in uw toetsencombinatie in te voegen, zodat deze alleen voor Markdown beschikbaar is en niet voor andere bestanden. Open hiervoor *keybindings.json* en voeg de volgende regel in onder de opdrachtnaam (vergeet geen komma tussen regels toe te voegen):

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Uw voltooide aangepaste toetsencombinatie zou er uit moeten zien zoals in deze *keybindings.json*:

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > Plaats uw toetscombinaties in dit bestand om de standaardcombinaties te overschrijven

1. Sla *keybindings.json* op.

Zie [VS Code-documenten](https://code.visualstudio.com/docs/getstarted/keybindings) voor meer informatie over toetscombinaties.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>De verouderde werkbalk Gauntlet weergeven

Voormalige gebruikers van de extensiecode Gauntlet zullen hebben gemerkt dat de schrijfwerkbalk niet langer onder aan het VS Code-venster wordt weergegeven wanneer de extensie Docs Markdown wordt geïnstalleerd. De reden hiervoor is dat de werkbalk veel ruimte op de VS Code-statusbalk innam en niet voldeed aan de best practices voor extensie-UX. We hebben de werkbalk daarom afgeschaft in de nieuwe extensie. U kunt er echter wel voor kiezen om de werkbalk weer te geven. Werk hiervoor uw VS Code-bestand settings.json als volgt bij:

1. Ga in VS Code naar **Bestand** > **Voorkeuren** > **Instellingen** of druk op <kbd>Ctrl+,</kbd>.
1. Selecteer **Gebruikersinstellingen** om de instellingen voor alle VS Code-werkruimten te wijzigen, of selecteer **Instellingen voor werkruimte** om alleen de instellingen voor de huidige werkruimte te wijzigen.
1. Selecteer **Extensies** > **Configuratie van Docs Markdown-extensies** en schakel vervolgens het selectievakje **Verouderde werkbalk in de onderste statusbalk weergeven** in.

   ![Instellingen voor verouderde werkbalk weergeven in VS Code](docs-authoring/media/show-gauntlet-bar.png)

Wanneer u de selectie hebt gemaakt, wordt het *settings.json*-bestand door VS Code bijgewerkt. Vervolgens wordt u gevraagd het venster opnieuw te laden zodat de wijzigingen van kracht worden.

Nieuwe opdrachten die worden toegevoegd aan de extensie, zijn niet beschikbaar op de werkbalk.

## <a name="how-to-use-docs-templates"></a>Het gebruik van Docs-sjablonen

Met de Docs Article Templates-extensie kunnen schrijvers die VS Code gebruiken, een Markdown-sjabloon ophalen uit een gecentraliseerde opslag en deze toepassen op een bestand. Sjablonen helpen ervoor te zorgen dat de vereiste metagegevens worden opgenomen in artikelen, dat inhoudsnormen worden opgevolgd, enzovoort. Sjablonen worden beheerd als Markdown-bestanden in een openbare GitHub-opslagplaats.

### <a name="to-apply-a-template-in-vs-code"></a>Een sjabloon toepassen in VS Code

1. Controleer of de Docs Article Templates-extensie is geïnstalleerd en is ingeschakeld.
1. Als de Docs Markdown-extensie niet is geïnstalleerd, drukt u op <kbd>F1</kbd> om het opdrachtenpalet te openen, begint u 'sjabloon' te typen om te filteren en klikt u vervolgens op `Docs: Template`. Als Docs Markdown wel is geïnstalleerd, kunt u het opdrachtenpalet gebruiken of op <kbd>Alt+M</kbd> drukken om het menu Docs Markdown QuickPick weer te geven. Selecteer vervolgens `Template` in de lijst.
1. Selecteer de gewenste sjabloon in de lijst die wordt weergegeven.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Uw GitHub-id en/of Microsoft-alias toevoegen aan de VS Code-instellingen

De Templates-extensie biedt ondersteuning voor drie velden met dynamische metagegevens: author, ms.author en ms.date. Dit betekent dat, wanneer de maker van een sjabloon deze velden gebruikt in de metagegevenskoptekst van een Markdown-sjabloon, ze als volgt automatisch worden ingevuld in uw bestand wanneer u de sjabloon toepast:

| Metagegevensveld | Waarde |
|--|--|
| `author` | Uw GitHub-alias, indien opgegeven in het bestand met VS Code-instellingen. |
| `ms.author` | Uw Microsoft-alias, indien opgegeven in het bestand met VS Code-instellingen. Als u geen werknemer van Microsoft bent, laat u dit veld niet-gespecificeerd. |
| `ms.date` | De huidige datum in de ondersteunde Docs-notatie, `MM/DD/YYYY`. De datum wordt niet automatisch bijgewerkt als u het bestand vervolgens wijzigt. U moet de datum handmatig bijwerken. Dit veld geeft aan wanneer het artikel voor het laatst is vernieuwd. |

### <a name="to-set-author-andor-msauthor"></a>Auteur en/of ms.author instellen

1. Ga in VS Code naar **Bestand** > **Voorkeuren** > **Instellingen** of druk op <kbd>Ctrl+,</kbd>.
1. Selecteer **Gebruikersinstellingen** om de instellingen voor alle VS Code-werkruimten te wijzigen, of selecteer **Instellingen voor werkruimte** om alleen de instellingen voor de huidige werkruimte te wijzigen.
1. Ga in het deelvenster Standaardinstellingen aan de linkerkant naar **Configuratie van Docs Article Templates-extensie**. Klik op het penpictogram naast de gewenste instelling, en klik vervolgens in Instellingen op Vervangen.
1. Het Deelvenster **Gebruikersinstellingen** wordt geopend in een naastgelegen venster met onderaan een nieuwe vermelding.
1. Voeg de GitHub-id of Microsoft-e-mailalias toe en sla het bestand op.
1. Mogelijk moet u VS Code sluiten en opnieuw starten om de wijzigingen door te voeren.
1. Wanneer u nu een sjabloon toepast die gebruikmaakt van dynamische velden, worden de GitHub-id en/of Microsoft-alias automatisch ingevuld in de koptekst van de metagegevens.

### <a name="to-make-a-new-template-available-in-vs-code"></a>Een nieuwe sjabloon beschikbaar maken in VS Code

1. Ontwerp uw sjabloon als een Markdown-bestand.
1. Verzend een pull-aanvraag naar de map Sjablonen van de opslagplaats [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates).

Het docs.microsoft.com-team zal uw sjabloon bekijken en de PR samenvoegen als deze voldoet aan de stijlrichtlijnen van docs.microsoft.com. Na het samenvoegen is de sjabloon beschikbaar voor alle gebruikers van de Docs Article Templates-extensie.

## <a name="demo-several-features"></a>Demo van verschillende functies

Hier volgt een korte video waarin de volgende functies van het Docs Authoring Pack worden getoond:

* **YAML-bestanden**
  * Ondersteuning voor 'Docs: Koppeling naar een bestand in de opslagplaats'
* **Markdown-bestanden**
  * Contextmenuoptie om de metagegevenswaarde ms.date bij te werken
  * Ondersteuning voor het automatisch voltooien van code voor de taal-id's binnen een afscheiding
  * Waarschuwingen voor niet-herkende taal-id's binnen een afscheiding/ondersteuning voor automatische correctie
  * Selectie oplopend sorteren (A tot Z)
  * Selectie aflopend sorteren (Z tot A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>Verwachtingen met betrekking tot bijdragen

De Docs Authoring Pack-extensie is een opensource-extensie en is beschikbaar voor bijdragen aan iedereen met een GitHub-account. Er is een speciaal intern Microsoft-team opgesteld dat actief aan dit project werkt. Dit team controleert problemen en pull-aanvragen. De Service Level Agreement (SLA) en verwachtingen voor het ophalen van een pull-aanvraag worden momenteel binnen een week beoordeeld. Door het automatiseren van taken willen we deze tijd verder verkorten.

## <a name="next-steps"></a>Volgende stappen

Bekijk de verschillende functies die beschikbaar zijn in de Docs Authoring Pack, Visual Studio Code-extensie.

* [Voltooiing van Dev Lang](docs-authoring/dev-lang-completion.md)
* [Afbeeldingscompressie](docs-authoring/image-compression.md)
* [Updates van metagegevens](docs-authoring/metadata-updates.md)
* [Tabel opnieuw opmaken](docs-authoring/reformat-table.md)
* [Slimme aanhalingstekens vervangen](docs-authoring/smart-quote-replacement.md)
* [Sorteringen omleiden](docs-authoring/sort-redirects.md)
* [Sorteringen selecteren](docs-authoring/sort-selection.md)
