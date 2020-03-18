---
title: Selectie sorteren - Docs Authoring Pack
description: Meer informatie over het gebruik van de functie Selectie sorteren van het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336745"
---
# <a name="sort-selection"></a><span data-ttu-id="39287-103">Selectie sorteren</span><span class="sxs-lookup"><span data-stu-id="39287-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="39287-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="39287-104">Summary</span></span>

<span data-ttu-id="39287-105">Wanneer u een selectie hebt gemaakt, worden in een Markdown-bestand ( *\*.md*) twee contextmenuopdrachten voor sorteren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="39287-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="39287-106">Klik met de rechtermuisknop op de geselecteerde tekst om het contextmenu te openen.</span><span class="sxs-lookup"><span data-stu-id="39287-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="39287-107">U ziet iets wat vergelijkbaar is met de volgende menuopdrachten:</span><span class="sxs-lookup"><span data-stu-id="39287-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Contextmenu Selectie sorteren":::

> [!TIP]
> <span data-ttu-id="39287-109">De contextmenuopdrachten voor sorteren zijn verborgen totdat er een geldige selectie is in de Visual Studio Code-teksteditor.</span><span class="sxs-lookup"><span data-stu-id="39287-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="39287-110">Selectie oplopend sorteren (A tot Z)</span><span class="sxs-lookup"><span data-stu-id="39287-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="39287-111">Als u de optie **Selectie oplopend sorteren (A tot Z)** selecteert, wordt de volledige selectie in alfabetische volgorde gesorteerd van A naar Z.</span><span class="sxs-lookup"><span data-stu-id="39287-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="39287-112">Selectie aflopend sorteren (Z tot A)</span><span class="sxs-lookup"><span data-stu-id="39287-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="39287-113">Als u de optie **Selectie aflopend sorteren (Z tot A)** selecteert, wordt de volledige selectie in alfabetische volgorde gesorteerd van Z naar A.</span><span class="sxs-lookup"><span data-stu-id="39287-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="39287-114">Aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="39287-114">Considerations</span></span>

<span data-ttu-id="39287-115">Het onderliggende sorteermechanisme maakt gebruik van sorteren in *natuurlijke taal*.</span><span class="sxs-lookup"><span data-stu-id="39287-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="39287-116">Hierdoor is het krachtiger en uitgebreider dan het standaard sorteren.</span><span class="sxs-lookup"><span data-stu-id="39287-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="39287-117">Kijk eens naar de volgende tabel:</span><span class="sxs-lookup"><span data-stu-id="39287-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="39287-118">Zonder sorteren in natuurlijke taal zou de volgorde voor `Column1` 1, 11, 2 zijn geweest, maar het mechanisme begrijpt dat 11 groter is dan 2, wat resulteert in de volgende oplopende volgorde:</span><span class="sxs-lookup"><span data-stu-id="39287-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="39287-119">In actie</span><span class="sxs-lookup"><span data-stu-id="39287-119">In action</span></span>

<span data-ttu-id="39287-120">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="39287-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="39287-121">[![Voorbeeld van Selectie sorteren](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="39287-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
