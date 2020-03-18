---
title: Markdown-tabellen opnieuw opmaken - Docs Authoring Pack
description: Meer informatie over het gebruik van de verschillende opmaakfuncties voor Markdown-tabellen van het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336768"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="8fe2a-103">Markdown-tabellen opnieuw opmaken</span><span class="sxs-lookup"><span data-stu-id="8fe2a-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="8fe2a-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8fe2a-104">Summary</span></span>

<span data-ttu-id="8fe2a-105">Als u in een Markdown-bestand ( *\*.md*) een volledige tabel selecteert, worden twee contextmenuopdrachten voor tabelopmaak beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="8fe2a-106">Klik met de rechtermuisknop op de geselecteerde Markdown-tabel om het contextmenu te openen.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="8fe2a-107">U ziet iets wat vergelijkbaar is met de volgende menuopdrachten:</span><span class="sxs-lookup"><span data-stu-id="8fe2a-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Contextmenu tabel opnieuw opmaken":::

> [!TIP]
> <span data-ttu-id="8fe2a-109">Deze functie werkt **niet** met meerdere tabelselecties, maar is bedoeld voor één Markdown-tabel.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="8fe2a-110">U moet de hele tabel selecteren, inclusief koppen voor gewenste resultaten.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="8fe2a-111">Geselecteerde tabel consolideren</span><span class="sxs-lookup"><span data-stu-id="8fe2a-111">Consolidate selected table</span></span>

<span data-ttu-id="8fe2a-112">Als u de optie **Geselecteerde tabel consolideren** selecteert, worden de tabelkoppen en inhoud samengevouwen met slechts één spatie aan beide zijden van elke waarde.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="8fe2a-113">Geselecteerde tabel gelijkmatig verdelen</span><span class="sxs-lookup"><span data-stu-id="8fe2a-113">Evenly distribute selected table</span></span>

<span data-ttu-id="8fe2a-114">Als u de optie **Geselecteerde tabel gelijkmatig verdelen** selecteert, wordt de langste waarde in elke kolom berekend en worden alle andere waarden gelijkmatig verdeeld.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="8fe2a-115">Aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="8fe2a-115">Considerations</span></span>

<span data-ttu-id="8fe2a-116">De functie heeft geen invloed op de weergave van de tabel, maar helpt wel om de leesbaarheid van de tabel te verbeteren, waardoor deze beter onderhoudbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="8fe2a-117">Met de functie voor het opnieuw opmaken van tabellen handhaaft u de uitlijning van kolommen.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="8fe2a-118">Kijk eens naar de volgende tabel:</span><span class="sxs-lookup"><span data-stu-id="8fe2a-118">Consider the following table:</span></span>

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

<span data-ttu-id="8fe2a-119">Nadat deze 'gelijkmatig gedistribueerd' is:</span><span class="sxs-lookup"><span data-stu-id="8fe2a-119">After being "evenly distributed":</span></span>

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

<span data-ttu-id="8fe2a-120">Nadat deze 'geconsolideerd' is:</span><span class="sxs-lookup"><span data-stu-id="8fe2a-120">After being "consolidated":</span></span>

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

## <a name="in-action"></a><span data-ttu-id="8fe2a-121">In actie</span><span class="sxs-lookup"><span data-stu-id="8fe2a-121">In action</span></span>

<span data-ttu-id="8fe2a-122">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="8fe2a-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="8fe2a-123">[![Voorbeeld van tabel opnieuw opmaken](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8fe2a-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
