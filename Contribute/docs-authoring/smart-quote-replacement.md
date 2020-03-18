---
title: Slimme aanhalingstekens automatisch vervangen - Docs Authoring Pack
description: Meer informatie over hoe u slimme aanhalingstekens automatisch vervangt met het Docs Authoring Pack, en de Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336699"
---
# <a name="smart-quote-replacement"></a>Slimme aanhalingstekens vervangen

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Overzicht

Ontwikkelaars van inhoud hebben een aantal van de meest geavanceerde functies van moderne technologieën en intelligence ontwikkeld, maar onze tools geven nog steeds de voorkeur aan 'domme aanhalingstekens' in Markdown. De antoniem is natuurlijk 'slimme aanhalingstekens'. Slimme aanhalingstekens zijn gebruikelijk met ideale typografieën, maar hebben niet de voorkeur met Markdown en gerenderde HTML.

Wanneer u bijvoorbeeld werkt aan Microsoft Word-documenten, hebt u wellicht wel gezien dat wanneer u de <kbd>Shift</kbd>-toets ingedrukt houdt en een <kbd>"</kbd> typt, het teken `"` snel wordt vervangen door een slim aanhalingsteken `“`.

| Description        | Unicode  | Slim aanhalingsteken | Vervanging |
|--------------------|----------|-------------|-------------|
| Dubbel aanhalingsteken links  | `\u201c` | `“`         | `"`         |
| Dubbel aanhalingsteken rechts | `\u201d` | `”`         | `"`         |
| Enkel aanhalingsteken links  | `\u2018` | `‘`         | `'`         |
| Enkel aanhalingsteken rechts | `\u2019` | `’`         | `'`         |

Wanneer u in een Markdown-bestand ( *\*.md*) tekst plakt of wanneer u inhoud bijwerkt: met deze functie wordt de inhoud actief geëvalueerd en worden waarden automatisch dienovereenkomstig vervangen.

> [!NOTE]
> Met de functie voor het vervangen van een slim aanhalingsteken worden ook andere tekens vervangen, zoals, maar niet beperkt tot; (`©, ™, ®, •`, subscript- en superscripttekens). Dit is handig wanneer u tekst uit Word-documenten plakt.

## <a name="preferences"></a>Voorkeuren

Deze functie is optioneel, maar wordt standaard ingesteld op `true`. Deze functie in- of uitschakelen:

1. Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.
1. De instelling in- en uitschakelen in de sectie **Markdown: Sectie Slimme aanhalingstekens vervangen**.

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van slimme aanhalingstekens vervangen](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
