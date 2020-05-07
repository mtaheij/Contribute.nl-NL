---
title: Markdown-tabellen opnieuw opmaken - Docs Authoring Pack
description: Meer informatie over het gebruik van de verschillende opmaakfuncties voor Markdown-tabellen van het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336768"
---
# <a name="reformat-markdown-tables"></a>Markdown-tabellen opnieuw opmaken

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Samenvatting

Als u in een Markdown-bestand ( *\*.md*) een volledige tabel selecteert, worden twee contextmenuopdrachten voor tabelopmaak beschikbaar. Klik met de rechtermuisknop op de geselecteerde Markdown-tabel om het contextmenu te openen. U ziet iets wat vergelijkbaar is met de volgende menuopdrachten:

:::image type="content" source="media/reformat-table-menu.png" alt-text="Contextmenu tabel opnieuw opmaken":::

> [!TIP]
> Deze functie werkt **niet** met meerdere tabelselecties, maar is bedoeld voor één Markdown-tabel. U moet de hele tabel selecteren, inclusief koppen voor gewenste resultaten.

## <a name="consolidate-selected-table"></a>Geselecteerde tabel consolideren

Als u de optie **Geselecteerde tabel consolideren** selecteert, worden de tabelkoppen en inhoud samengevouwen met slechts één spatie aan beide zijden van elke waarde.

## <a name="evenly-distribute-selected-table"></a>Geselecteerde tabel gelijkmatig verdelen

Als u de optie **Geselecteerde tabel gelijkmatig verdelen** selecteert, wordt de langste waarde in elke kolom berekend en worden alle andere waarden gelijkmatig verdeeld.

## <a name="considerations"></a>Aandachtspunten

De functie heeft geen invloed op de weergave van de tabel, maar helpt wel om de leesbaarheid van de tabel te verbeteren, waardoor deze beter onderhoudbaar wordt. Met de functie voor het opnieuw opmaken van tabellen handhaaft u de uitlijning van kolommen.

Kijk eens naar de volgende tabel:

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

Nadat deze 'gelijkmatig gedistribueerd' is:

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

Nadat deze 'geconsolideerd' is:

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van tabel opnieuw opmaken](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
