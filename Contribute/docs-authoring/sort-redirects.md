---
title: Omleidingen sorteren - Docs Authoring Pack
description: Meer informatie over het sorteren van omleidingen met het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336676"
---
# <a name="sort-redirects"></a>Omleidingen sorteren

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Overzicht

Met de ontwikkeling van een docs.microsoft.com-docset worden sommige Markdown-bestanden uiteindelijk verwijderd. Wanneer een Markdown-bestand wordt verwijderd, moeten we een omleiding bieden, zodat alle verwijzingen naar het verwijderde artikel op de juiste wijze worden omgezet via de omleiding. Omleidingen zijn te vinden in het bestand *.openpublishing.redirection.json*.

1. Open het Opdrachtpalet en druk op <kbd>F1</kbd> (of op <kbd>⇧ ⌘ P</kbd> in macOS)
1. Type: **Docs: Masteromleidingsbestand sorteren**
1. Selecteer de opdracht om deze uit te voeren
1. Bekijk wijzigingen in het bestand *.openpublishing.redirection.json*

## <a name="considerations"></a>Aandachtspunten

Het concept van ketenvorming volgt uit de manier waarop het bestand *.openpublishing.redirection.json* oorspronkelijk is ontworpen. Bestanden die als een omleiding worden toegevoegd, raken na verloop van tijd verouderd. Dit gebeurt wanneer bestand A wordt verwijderd en een omleiding naar bestand B nodig heeft, waarna het bestand B wordt verwijderd en vervolgens wordt omgeleid naar bestand C. In het ideale geval verwijzen beide vermeldingen naar C, zodat A omleidt naar C en B hetzelfde blijft. Dit is een kleine prestatieverbetering en er wordt actief gewerkt aan de functie.

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van omleidingen sorteren](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
