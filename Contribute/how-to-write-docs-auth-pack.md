---
title: Docs-ontwerppakket voor Visual Studio Code
description: In dit artikel wordt het extensiepakket van Visual Studio Code beschreven waarmee u Markdown voor docs.microsoft.com kunt ontwerpen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 1552ecc3e17e52439a7faa72973813099ce4d253
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188303"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs-ontwerppakket voor VS Code

Het Docs-ontwerppakket is een verzameling extensies voor Visual Studio Code die u kunt gebruiken bij het schrijven van Markdown voor docs.microsoft.com. Het pakket is [verkrijgbaar via de VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) en bevat de volgende extensies:

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): een populaire Markdown-linter van David Anson zodat u zeker weet dat u voor uw Markdown de best practices gebruikt.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): een spellingcontrole van Street Side Software die volledig offline is.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): gebruikt de CSS op docs.microsoft.com voor een nauwkeuriger Markdown-voorbeeld, inclusief aangepaste Markdown.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): biedt hulp bij het schrijven van Markdown voor inhoud op docs.microsoft.com in het OPS (Open Publishing System), inclusief fundamentele Markdown-ondersteuning en ondersteuning voor aangepaste Markdown-syntaxis in OPS. De rest van dit onderwerp gaat over de Docs Markdown-extensie.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): hiermee kunnen gebruikers inhoud uit het Markdown-raamwerk toepassen op nieuwe bestanden.

## <a name="prerequisites-and-assumptions"></a>Vereisten en aannames

Voor het nauwkeurig invoegen van relatieve koppelingen, afbeeldingen en andere ingesloten inhoud met de Docs Markdown-extensie moet de VS Code-werkruimte zijn ingesteld op de hoofdmap van de gekloonde OPS-opslagplaats (Open Publishing System).

Sommige syntaxissen die door de extensie worden ondersteund, zoals waarschuwingen en codefragmenten, bestaan uit aangepaste Markdown voor OPS en worden niet goed weergegeven, tenzij u deze via OPS publiceert.

## <a name="how-to-use-the-docs-markdown-extension"></a>De Docs Markdown-extensie gebruiken

Druk op `ALT+M` voor toegang tot het menu van Docs Markdown. U kunt klikken of de pijltjes omhoog/omlaag gebruiken om de gewenste functie te selecteren, of begin te typen om te filteren. Kies vervolgens `ENTER` wanneer de gewenste functie in het menu wordt gemarkeerd. De volgende functies zijn beschikbaar:

|Functie     |Description           |
|-------------|----------------------|
|Preview      |Bekijk met behulp van Docs Preview-extensie een voorbeeld van het actieve onderwerp in een naastgelegen venster. Deze optie is alleen beschikbaar als Docs Preview is geïnstalleerd.|
|Vet         |Hiermee wordt tekst **vetgedrukt** weergegeven.|
|Cursief       |Hiermee wordt tekst *cursief* weergegeven.|
|Code         |Als er één regel of minder is geselecteerd, wordt tekst als `inline code` weergegeven.<br><br>Als er meerdere regels zijn geselecteerd, worden deze als afgeschermd codeblok opgemaakt. U hebt nu de mogelijkheid om een programmeertaal te selecteren die door OPS wordt ondersteund.|
|Waarschuwing        |Hiermee voegt u een notitie of de aanduiding Belangrijk, Waarschuwing of Tip toe.<br><br>Selecteer Waarschuwing in het menu en selecteer het waarschuwingstype. Als u al eerder tekst hebt geselecteerd, wordt deze omringd door de geselecteerde waarschuwingssyntaxis. Is er geen tekst geselecteerd, dan wordt een nieuwe waarschuwing toegevoegd met tijdelijke tekst.|
|Genummerde lijst|Hiermee voegt u een nieuwe genummerde lijst in.<br><br> Als er meerdere regels zijn geselecteerd, wordt elke regel als lijstitem weergegeven. Houd er rekening mee dat genummerde lijsten worden in Markdown met alleen enen (1) worden weergegeven, maar met opeenvolgende nummers of (voor geneste lijsten) letters worden weergegeven op docs.microsoft.com. Als u een geneste genummerde lijst wilt maken, drukt u in de bovenliggende lijst op de Tab-toets.|
|Lijst met opsommingstekens|Hiermee voegt u een nieuwe lijst met opsommingstekens in.|
|Tabel        |Hiermee voegt u een Markdown-tabelstructuur in.<br><br>Nadat u de tabelopdracht hebt geselecteerd, geeft u het aantal kolommen en rijen op in de notatie kolommen:rijen, zoals 3:4. Het maximum aantal kolommen dat u via deze extensie kunt opgeven is 5. Dit is het aanbevolen maximum om de tabel nog goed leesbaar te houden.|
|Koppeling naar een bestand in de opslagplaats|Hiermee voegt u een relatieve koppeling naar een ander bestand in de huidige opslagplaats in. Nadat u deze optie hebt gekozen, voert u tekst in het opdrachtvenster in om bestanden op naam te filteren. Kies daarna het gewenste bestand. Als u eerder tekst hebt geselecteerd, wordt dit de koppelingstekst. Anders wordt de H1 van het doelbestand gebruikt als de koppelingstekst.|
|Koppeling naar een webpagina    |Hiermee voegt u een koppeling naar een webpagina in. Nadat u deze optie hebt geselecteerd, plakt of typt u de URI in het opdrachtvenster. `https://` is vereist. Als u eerder tekst hebt geselecteerd, wordt dit de koppelingstekst. Anders wordt de URI gebruikt als de koppelingstekst.|
|Koppeling naar koptekst     |Voegt een koppeling naar een bladwijzer in het huidige bestand of een ander bestand in de opslagplaats in.<br>`Bookmark in this file`: kies een van de titels in het huidige bestand uit de lijst om een bladwijzer met de juiste indeling in te voegen.<br>`Bookmark in another file`: filter eerst op bestandsnaam en selecteer dan het bestand waarnaar u wilt koppelen. Kies vervolgens de juiste titel in het geselecteerde bestand.|
|Afbeelding        |Typ alternatieve tekst (vereist voor toegankelijkheid) en selecteer deze tekst. Roep vervolgens deze opdracht aan om de lijst met ondersteunde afbeeldingsbestanden in de opslagplaats te filteren en selecteer het gewenste bestand. Als u geen alternatieve tekst hebt geselecteerd wanneer u deze opdracht aanroept, wordt u gevraagd dit in te voeren voordat u een afbeeldingsbestand kunt selecteren.|
|Opnemen      |Vind een bestand om in het huidige bestand in te sluiten.|
|Codefragment      |Vind een codefragment in de opslagplaats om in het huidige bestand in te sluiten.|
|Video        |Voeg een ingesloten video toe.|
|Sjabloon     |Maak een nieuw bestand en pas een Markdown-sjabloon toe. Zie [Sjablonen](#how-to-use-docs-templates) hieronder voor meer informatie.|

## <a name="how-to-assign-keyboard-shortcuts"></a>Sneltoetsen toewijzen

1. Typ `CTRL+K` en vervolgens `CTRL+S` om de lijst met sneltoetsen te openen.
1. Zoek de opdracht, zoals `formatBold`, waarvoor u een aangepaste toetsencombinaties wilt maken.
1. Klik op het plusteken dat naast de naam van de opdracht verschijnt wanneer u met de cursor over de regel beweegt.
1. Zodra een nieuw invoervak zichtbaar is, typt u de sneltoets die u aan die specifieke opdracht wilt koppelen. Typ bijvoorbeeld `ctrl+b` om de gebruikelijke sneltoets voor vetgedrukte tekst te gebruiken.
1. Het kan handig zijn om een `when`-clausule in uw toetsencombinaties in te voegen, zodat deze alleen voor Markdown beschikbaar is en niet voor andere bestanden. Open hiervoor *keybindings.json* en voeg de volgende regel in onder de opdrachtnaam (vergeet geen komma tussen regels toe te voegen):
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Uw voltooide aangepaste toetsencombinaties zou er uit moeten zien zoals in deze keybindings.json:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Sla keybindings.json op.

Zie [Toetsencombinaties](https://code.visualstudio.com/docs/getstarted/keybindings) in de VS Code-documenten voor meer informatie.

## <a name="how-to-show-the-legacy-toolbar"></a>De verouderde werkbalk weergeven

Gebruikers van de voorlopige versie van de extensie zullen merken dat de schrijfwerkbalk niet meer onder aan het VS Code-venster wordt weergegeven wanneer de Docs Markdown-extensie is geïnstalleerd. De reden hiervoor is dat de werkbalk veel ruimte op de VS Code-statusbalk innam en niet voldeed aan de best practices voor extensie-UX. We hebben de werkbalk daarom afgeschaft in de nieuwe extensie. U kunt er echter wel voor kiezen om de werkbalk weer te geven. Werk hiervoor uw VS Code-bestand settings.json als volgt bij:

1. Ga in VS Code naar File (Bestand) -> Preferences (Voorkeuren) -> Settings (Instellingen) (`CTRL+Comma`).
1. Selecteer User Settings (Gebruikersinstellingen) om de instellingen voor alle VS Code-werkruimten te wijzigen of selecteer Workspace Settings (Instellingen werkruimte) om alleen de instellingen voor de huidige werkruimte te wijzigen.
1. Zoek in het deelvenster Default Settings (Standaardinstellingen) naar Docs Authoring Extension Configuration (Configuratie Docs-schrijfextensie) en selecteer het potloodpictogram naast de gewenste instelling. Daarna wordt u gevraagd om `true` of `false` te selecteren. Zodra u uw keuze hebt gemaakt, voegt VS Code automatisch de waarde aan het bestand settings.json toe. U wordt gevraagd het venster opnieuw te laden zodat de wijzigingen worden doorgevoerd.

## <a name="how-to-use-docs-templates"></a>Het gebruik van Docs-sjablonen

Met de Docs Article Templates-extensie kunnen schrijvers die VS Code gebruiken, een Markdown-sjabloon ophalen uit een gecentraliseerde opslag en deze toepassen op een bestand. Sjablonen helpen ervoor te zorgen dat de vereiste metagegevens worden opgenomen in artikelen, dat inhoudsnormen worden opgevolgd, enzovoort. Sjablonen worden beheerd als Markdown-bestanden in een openbare GitHub-opslagplaats.

### <a name="to-apply-a-template-in-vs-code"></a>Een sjabloon toepassen in VS Code

1. Als de Docs Markdown-extensie niet is geïnstalleerd, drukt u op F1 om het opdrachtenpalet te openen, begint u ‘sjabloon’ te typen om te filteren, en klikt u vervolgens op `Docs: Template`. Als Docs Markdown wel is geïnstalleerd, kunt u het opdrachtenpalet gebruiken of op `Alt+M` klikken om het menu Docs Markdown QuickPick weer te geven. Selecteer vervolgens `Template` in de lijst.
1. Selecteer de gewenste sjabloon in de lijst die wordt weergegeven.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Uw GitHub-id en/of Microsoft-alias toevoegen aan de VS Code-instellingen

De Templates-extensie biedt ondersteuning voor drie velden met dynamische metagegevens: author, ms.author en ms.date. Dit betekent dat, wanneer de maker van een sjabloon deze velden gebruikt in de metagegevenskoptekst van een Markdown-sjabloon, ze als volgt automatisch worden ingevuld in uw bestand wanneer u de sjabloon toepast:

|Metagegevens  |Waarde|
|----------|---------------|
|author    |Uw GitHub-id, indien opgegeven in het bestand met VS Code-instellingen.|
|ms.author |Uw Microsoft-alias, indien opgegeven in het bestand met VS Code-instellingen. Als u geen werknemer van Microsoft bent, laat u dit veld niet-gespecificeerd.|
|ms.date   |De huidige datum in de ondersteunde Docs-notatie, MM/DD/YYYY. De datum wordt niet automatisch bijgewerkt als u het bestand vervolgens wijzigt. U moet de waarde ms.date handmatig bijwerken om de meest recente datum van de publicatie op de docs.microsoft.com-site aan te geven.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>Ga als volgt te werk om author (GitHub-id) en/of ms.author (Microsoft-alias) in te stellen

1. Ga in VS Code naar File (Bestand) -> Preferences (Voorkeuren) -> Settings (Instellingen) (`CTRL+Comma`).
1. Selecteer User Settings (Gebruikersinstellingen) om de instellingen voor alle VS Code-werkruimten te wijzigen, of selecteer Workspace Settings (Instellingen voor werkruimte) om alleen de instellingen voor de huidige werkruimte te wijzigen.
1. Ga in het deelvenster Default Settings (Standaardinstellingen) aan de linkerkant naar Docs Article Templates Extension Configuration (Configuratie van Docs Article Templates-extensie). Klik op het penpictogram naast de gewenste instelling, en klik vervolgens in Settings (Instellingen) op Replace (Vervangen).
1. Het Deelvenster User Setting (Gebruikersinstellingen) wordt geopend in een naastgelegen venster met onderaan een nieuwe vermelding.
1. Voeg de GitHub-id of Microsoft-e-mailalias toe en sla het bestand op.
1. Mogelijk moet u VS Code sluiten en opnieuw starten om de wijzigingen door te voeren.
1. Wanneer u nu een sjabloon toepast die gebruikmaakt van dynamische velden, worden de GitHub-id en/of Microsoft-alias automatisch ingevuld in de koptekst van de metagegevens.
