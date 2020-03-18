---
title: Voltooiing van dev lang - Docs Authoring Pack
description: Meer informatie over hoe dev lang-voltooiing inzenders helpt in het Docs Authoring Pack, Visual Studio Code extensie.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336791"
---
# <a name="dev-lang-completion"></a>Voltooiing van dev lang

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Overzicht

Inzenders hebben hulp nodig bij het bepalen van de geldige taal-id's (dev langs) die in een Markdown-bestand driedubbele apostroffen (code-afbakeningopeningen) kunnen volgen. Helaas bestaat er geen validatie tijdens build time van dev-lang. Het resultaat is een ongelijksoortige weergave van één taal binnen dezelfde conceptuele docset.

Kijk bijvoorbeeld eens naar C#. Inzenders hebben `c#`, `C#`, `cs`, `csharp` en andere gebruikt als dev lang-weergaven van de taal. Welke van de voorgaande weergaven is correct?

De functie *Voltooiing van dev lang* neemt de verwarring weg door een lijst met bekende dev langs weer te geven. Bij het selecteren van een dev lang-naam uit IntelliSense:

* De code-afbakening wordt gesloten.
* Het caret-teken bevindt zich in de code-afbakening.

## <a name="preferences"></a>Voorkeuren

Het is niet mogelijk om deze functie uit te schakelen. De volgende instellingen zijn beschikbaar:

* [Veelgebruikte dev langs weergeven](#display-commonly-used-dev-langs)
* [Alle bekende dev langs weergeven](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>Veelgebruikte dev langs weergeven

Er wordt slechts een subset van de geldige dev langs gebruikt in één docset. De gebruikerservaring verbeteren:

1. Open in Visual Studio Code de docset naar de hoofdmap.
1. Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.
1. Klik op de koppeling **Bewerken in settings.json** in de sectie **Markdown: Docset-talen**.
1. Voeg de volgende eigenschap `markdown.docsetLanguages` toe aan het bestand *settings.json*:

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Plaats het caret-teken in de lege matrix van de eigenschap en activeer IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>). Er wordt een lijst met namen van bekende dev langs weergegeven.
1. Voeg dev lang-namen toe aan de matrix totdat u tevreden bent met de lijst. In de volgende lijst worden bijvoorbeeld vier dev lang-namen weergegeven aan de gebruiker na het typen van driedubbele apostrof:

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. Sla de wijzigingen op in het bestand *settings.json*.

> [!WARNING]
> Een lege `markdown.docsetLanguages`-matrix zorgt ervoor dat alle bekende dev langs worden weergegeven.

### <a name="display-all-known-dev-langs"></a>Alle bekende dev langs weergeven

Standaard worden alle bekende dev lang-namen weergegeven in IntelliSense. Deze instelling overschrijft de eigenschap `markdown.docsetLanguages` die wordt beschreven in [Veelgebruikte dev-langs weergeven](#display-commonly-used-dev-langs).

U kunt deze instelling als volgt wijzigen:

1. Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.
1. De instelling in- en uitschakelen in de sectie **Markdown: Alle beschikbare talen**.

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie:

[![Voltooiing van dev lang](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
