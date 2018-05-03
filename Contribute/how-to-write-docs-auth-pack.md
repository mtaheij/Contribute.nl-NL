---
title: Docs-ontwerppakket voor VS Code
description: Extensiepakket van VS Code voor het schrijven van Markdown voor docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.article: contributor-guide
ms.prod: n.a
ms.service: n.a
ms.technology: n.a
ms.openlocfilehash: 5c857deb07e28e1f6744c895a291bf78a6acf1df
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs-ontwerppakket voor VS Code

Het Docs-ontwerppakket is een verzameling extensies voor VS Code die u kunt gebruiken bij het schrijven van Markdown voor docs.microsoft.com. Het pakket is [verkrijgbaar via de VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) en bevat de volgende extensies:

- **DocFX:** biedt een specifieke Markdown-preview voor docs.microsoft.com. Zie [DocFX](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX) voor meer informatie.
- **markdownlint:** een populaire Markdown-linter van David Anson zodat u zeker weet dat u voor uw Markdown de best practices gebruikt. Zie [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) voor meer informatie.
- **Docs Markdown:** biedt hulp bij het schrijven van Markdown voor inhoud van docs.microsoft.com in het Open Publishing System (OPS), inclusief fundamentele Markdown-ondersteuning en ondersteuning voor aangepaste Markdown-syntaxis in OPS. De rest van dit onderwerp gaat over de Docs Markdown-extensie.

## <a name="prerequisites-and-assumptions"></a>Vereisten en aannames

Voor het nauwkeurig invoegen van relatieve koppelingen, afbeeldingen en andere ingesloten inhoud met de Docs Markdown-extensie moet uw VS Code-werkruimte op de hoofdmap van uw gekloonde OPS-opslagplaats zijn gericht.

Sommige syntaxissen die door de extensie worden ondersteund, zoals waarschuwingen en codefragmenten, bestaan uit aangepaste Markdown voor OPS en worden niet goed weergegeven, tenzij u deze via OPS publiceert.

## <a name="how-to-use-the-docs-markdown-extension"></a>De Docs Markdown-extensie gebruiken

Typ `ALT+M` voor toegang tot het menu van Docs Markdown. U kunt klikken of de pijltjes omhoog/omlaag gebruiken om de gewenste functie te selecteren, of begin te typen om te filteren. Kies vervolgens `ENTER` wanneer de gewenste functie in het menu wordt gemarkeerd. De volgende functies zijn beschikbaar:

|Functie     |Opdracht             |Beschrijving           |
|-------------|--------------------|----------------------|
|Vet         |`formatBold`        |Hiermee wordt tekst **vetgedrukt** weergegeven.|
|Cursief       |`formatItalic`      |Hiermee wordt tekst *cursief* weergegeven.|
|Code         |`formatCode`        |Als er één regel of minder is geselecteerd, wordt tekst als `inline code` weergegeven.<br><br>Als er meerdere regels zijn geselecteerd, worden deze als afgeschermd codeblok opgemaakt. U hebt nu de mogelijkheid om een programmeertaal te selecteren die door OPS wordt ondersteund.|
|Waarschuwing        |`insertAlert`       |Hiermee voegt u een notitie of de aanduiding Belangrijk, Waarschuwing of Tip toe.<br><br>Selecteer Waarschuwing in het menu en selecteer het waarschuwingstype. Als u al eerder tekst hebt geselecteerd, wordt deze omringd door de geselecteerde waarschuwingssyntaxis. Is er geen tekst geselecteerd, dan wordt een nieuwe waarschuwing toegevoegd met tijdelijke tekst.|
|Genummerde lijst|`insertNumberedList` |Hiermee voegt u een nieuwe genummerde lijst in.<br><br> Als er meerdere regels zijn geselecteerd, wordt elke regel als lijstitem weergegeven. Houd er rekening mee dat genummerde lijsten worden in Markdown met alleen enen (1) worden weergegeven, maar met opeenvolgende nummers of (voor geneste lijsten) letters worden weergegeven op docs.microsoft.com. Als u een geneste genummerde lijst wilt maken, drukt u in de bovenliggende lijst op de Tab-toets.|
|Lijst met opsommingstekens|`insertBulletedList` |Hiermee voegt u een nieuwe lijst met opsommingstekens in.|
|Tabel        |`insertTable`        |Hiermee voegt u een Markdown-tabelstructuur in.<br><br>Nadat u de tabelopdracht hebt geselecteerd, geeft u het aantal kolommen en rijen op in de notatie kolommen:rijen, zoals 3:4. Het maximum aantal kolommen dat u via deze extensie kunt opgeven is 5. Dit is het aanbevolen maximum om de tabel nog goed leesbaar te houden.|
|Koppeling         |`selectLinkType`      |Hiermee voegt u een koppeling in. Wanneer u deze opdracht selecteert, wordt het volgende submenu weergegeven.<br><br>`External`: Koppeling naar een webpagina via URI. Moet http of https bevatten.<br>`Internal`: Hiermee voegt u een relatieve koppeling naar een ander bestand in dezelfde opslagplaats in. Nadat u deze optie hebt gekozen, voert u tekst in het opdrachtvenster in om bestanden op naam te filteren. Kies daarna het gewenste bestand. <br>`Bookmark in this file`: kies een van de titels in het huidige bestand uit de lijst om een bladwijzer met de juiste indeling in te voegen.<br>`Bookmark in another file`: filter eerst op bestandsnaam en selecteer dan het bestand waarnaar u wilt koppelen. Kies vervolgens de juiste titel in het geselecteerde bestand.|
|Afbeelding        |`insertImage`     |Typ alternatieve tekst (vereist voor toegankelijkheid) en selecteer deze tekst. Roep vervolgens deze opdracht aan om de lijst met ondersteunde afbeeldingsbestanden in de opslagplaats te filteren en selecteer het gewenste bestand. Als u geen alternatieve tekst hebt geselecteerd wanneer u deze opdracht aanroept, wordt u gevraagd dit in te voeren voordat u een afbeeldingsbestand kunt selecteren.|
|Opnemen      |`insertInclude`   |Vind een bestand om in het huidige bestand in te sluiten.|
|Codefragment      |`insertSnippet`   |Vind een codefragment in de opslagplaats om in het huidige bestand in te sluiten.|
|Video        |`insertVideo`     |Voeg een ingesloten video toe.|
|Preview      |`previewTopic`    |Bekijk met behulp van de extensie DocFX een preview van het actieve onderwerp in een naastgelegen venster.  Als de extensie DocFX niet is geïnstalleerd, of wel is geïnstalleerd maar is uitgeschakeld, wordt het onderwerp niet weergegeven.


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

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>De verouderde werkbalk Gauntlet weergeven

Voormalige gebruikers van de extensiecode Gauntlet zullen hebben gemerkt dat de schrijfwerkbalk niet langer onder aan het VS Code-venster wordt weergegeven wanneer de extensie Docs Markdown wordt geïnstalleerd. De reden hiervoor is dat de werkbalk veel ruimte op de VS Code-statusbalk innam en niet voldeed aan de best practices voor extensie-UX. We hebben de werkbalk daarom afgeschaft in de nieuwe extensie. U kunt er echter wel voor kiezen om de werkbalk weer te geven. Werk hiervoor uw VS Code-bestand settings.json als volgt bij:

1. Ga in VS Code naar File (Bestand) -> Preferences (Voorkeuren) -> Settings (Instellingen) (`CTRL+Comma`).
1. Selecteer User Settings (Gebruikersinstellingen) om de instellingen voor alle VS Code-werkruimten te wijzigen of selecteer Workspace Settings (Instellingen werkruimte) om alleen de instellingen voor de huidige werkruimte te wijzigen.
1. Zoek in het deelvenster Default Settings (Standaardinstellingen) naar Docs Authoring Extension Configuration (Configuratie Docs-schrijfextensie) en selecteer het potloodpictogram naast de gewenste instelling. Daarna wordt u gevraagd om `true` of `false` te selecteren. Zodra u uw keuze hebt gemaakt, voegt VS Code automatisch de waarde aan het bestand settings.json toe. U wordt gevraagd het venster opnieuw te laden zodat de wijzigingen worden doorgevoerd.

## <a name="known-issues"></a>Bekende problemen

- [DocFX Preview] MacOS en Linux: DocFX Preview opent de preview niet op de juiste manier (met de preview worden de standaardinstellingen voor Markdown-previews van VS Code voor deze platformen hersteld).
- [DocFX Preview] Alle platformen: sommige syntaxissen, zoals xref-koppelingen (kruisverwijzingen) naar API's, worden niet goed weergegeven in de preview. In sommige gevallen ontstaan hierdoor lege plekken in de inhoud.
- [Externe bladwijzers] Linux: de lijst met bestanden wordt weergegeven, maar er worden geen selecteerbare titels weergegeven.
- [Includes] Linux: de lijst met bestanden wordt weergegeven, maar er wordt geen koppeling toegevoegd nadat de selectie is gemaakt.