---
title: Afbeeldingscompressie - Docs Authoring Pack
description: Meer informatie over het comprimeren van afbeeldingen met het Docs Authoring Pack, en de Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336653"
---
# <a name="image-compression"></a>Afbeeldingscompressie

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>Overzicht

Alle documentatie wordt geleverd via internet, met uitzondering van PDF-versies van documenten. In het geval van statische inhoud kunt u het aantal bytes dat via de kabel wordt verzonden, het beste minimaliseren. Een manier om dat te doen, is door afbeeldingen in rust te comprimeren.

De Docs Authoring Pack-extensie omvat contextmenuopdrachten voor afbeeldingscompressie. De volgende afbeeldingstypen/-extensies worden ondersteund:

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

De algoritmen voor afbeeldingscompressie zonder kwaliteitsverlies worden gebruikt waar van toepassing.

## <a name="compress-image"></a>Afbeelding comprimeren

Klik in het navigatiedeelvenster **Verkenner** met de rechtermuisknop op een afbeeldingsbestand en selecteer vervolgens de optie **Afbeelding comprimeren**. De afbeelding wordt vervolgens gecomprimeerd.

## <a name="compress-images-in-folder"></a>Afbeeldingen in map comprimeren

Klik in het navigatiedeelvenster **Verkenner** met de rechtermuisknop op een map met de afbeeldingen en selecteer vervolgens de optie **Afbeeldingen in map comprimeren**. Alle afbeeldingen in de map worden gecomprimeerd.

## <a name="considerations"></a>Aandachtspunten

Het formaat van afbeeldingen met een grote resolutie wordt impliciet gewijzigd. De maximale afmetingen zijn gebaseerd op de door het platform aanbevolen maximale breedte van `1,200px`. Het maximum wordt alleen gebruikt wanneer afbeeldingen groter zijn dan wordt aanbevolen. Verder blijft de hoogte-breedteverhouding behouden wanneer het formaat ervan automatisch wordt gewijzigd.

## <a name="preferences"></a>Voorkeuren

De maximale afmetingen kunnen worden geconfigureerd, maar er is een maximumbreedte van `1200` pixels. Als u de maximale afmetingen wilt configureren, selecteert u **Bestand > Voorkeuren > Instellingen** en filtert u op `"Docs Image Extension"`.

:::image type="content" source="media/configure-image-compression.png" alt-text="Afbeeldingscompressie configureren":::

> [!NOTE]
> Met een waarde van `0` in **Maximumbreedte** of **Maximumhoogte** negeert u eenvoudig afwijkingen van de resolutie.

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van afbeelding comprimeren](media/compress-image.gif)](media/compress-image.gif#lightbox)
