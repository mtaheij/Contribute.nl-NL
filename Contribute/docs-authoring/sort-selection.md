---
title: Selectie sorteren - Docs Authoring Pack
description: Meer informatie over het gebruik van de functie Selectie sorteren van het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336745"
---
# <a name="sort-selection"></a>Sorteringen selecteren

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Samenvatting

Wanneer u een selectie hebt gemaakt, worden in een Markdown-bestand ( *\*.md*) twee contextmenuopdrachten voor sorteren weergegeven. Klik met de rechtermuisknop op de geselecteerde tekst om het contextmenu te openen. U ziet iets wat vergelijkbaar is met de volgende menuopdrachten:

:::image type="content" source="media/sort-selection-menu.png" alt-text="Contextmenu Selectie sorteren":::

> [!TIP]
> De contextmenuopdrachten voor sorteren zijn verborgen totdat er een geldige selectie is in de Visual Studio Code-teksteditor.

## <a name="sort-selection-ascending-a-to-z"></a>Selectie oplopend sorteren (A tot Z)

Als u de optie **Selectie oplopend sorteren (A tot Z)** selecteert, wordt de volledige selectie in alfabetische volgorde gesorteerd van A naar Z.

## <a name="sort-selection-descending-z-to-a"></a>Selectie aflopend sorteren (Z tot A)

Als u de optie **Selectie aflopend sorteren (Z tot A)** selecteert, wordt de volledige selectie in alfabetische volgorde gesorteerd van Z naar A.

## <a name="considerations"></a>Aandachtspunten

Het onderliggende sorteermechanisme maakt gebruik van sorteren in *natuurlijke taal*. Hierdoor is het krachtiger en uitgebreider dan het standaard sorteren. Kijk eens naar de volgende tabel:

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

Zonder sorteren in natuurlijke taal zou de volgorde voor `Column1` 1, 11, 2 zijn geweest, maar het mechanisme begrijpt dat 11 groter is dan 2, wat resulteert in de volgende oplopende volgorde:

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

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van Selectie sorteren](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
