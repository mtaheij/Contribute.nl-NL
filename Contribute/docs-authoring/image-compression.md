---
title: Afbeeldingscompressie - Docs Authoring Pack
description: Meer informatie over het comprimeren van afbeeldingen met het Docs Authoring Pack, en de Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336653"
---
# <a name="image-compression"></a><span data-ttu-id="48026-103">Afbeeldingscompressie</span><span class="sxs-lookup"><span data-stu-id="48026-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="48026-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="48026-104">Summary</span></span>

<span data-ttu-id="48026-105">Alle documentatie wordt geleverd via internet, met uitzondering van PDF-versies van documenten. In het geval van statische inhoud kunt u het aantal bytes dat via de kabel wordt verzonden, het beste minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="48026-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="48026-106">Een manier om dat te doen, is door afbeeldingen in rust te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="48026-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="48026-107">De Docs Authoring Pack-extensie omvat contextmenuopdrachten voor afbeeldingscompressie.</span><span class="sxs-lookup"><span data-stu-id="48026-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="48026-108">De volgende afbeeldingstypen/-extensies worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="48026-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="48026-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="48026-109">*\*.png*</span></span>
* <span data-ttu-id="48026-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="48026-110">*\*.jpg*</span></span>
* <span data-ttu-id="48026-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="48026-111">*\*.jpeg*</span></span>
* <span data-ttu-id="48026-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="48026-112">*\*.gif*</span></span>
* <span data-ttu-id="48026-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="48026-113">*\*.svg*</span></span>
* <span data-ttu-id="48026-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="48026-114">*\*.webp*</span></span>

<span data-ttu-id="48026-115">De algoritmen voor afbeeldingscompressie zonder kwaliteitsverlies worden gebruikt waar van toepassing.</span><span class="sxs-lookup"><span data-stu-id="48026-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="48026-116">Afbeelding comprimeren</span><span class="sxs-lookup"><span data-stu-id="48026-116">Compress image</span></span>

<span data-ttu-id="48026-117">Klik in het navigatiedeelvenster **Verkenner** met de rechtermuisknop op een afbeeldingsbestand en selecteer vervolgens de optie **Afbeelding comprimeren**.</span><span class="sxs-lookup"><span data-stu-id="48026-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="48026-118">De afbeelding wordt vervolgens gecomprimeerd.</span><span class="sxs-lookup"><span data-stu-id="48026-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="48026-119">Afbeeldingen in map comprimeren</span><span class="sxs-lookup"><span data-stu-id="48026-119">Compress images in folder</span></span>

<span data-ttu-id="48026-120">Klik in het navigatiedeelvenster **Verkenner** met de rechtermuisknop op een map met de afbeeldingen en selecteer vervolgens de optie **Afbeeldingen in map comprimeren**.</span><span class="sxs-lookup"><span data-stu-id="48026-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="48026-121">Alle afbeeldingen in de map worden gecomprimeerd.</span><span class="sxs-lookup"><span data-stu-id="48026-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="48026-122">Aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="48026-122">Considerations</span></span>

<span data-ttu-id="48026-123">Het formaat van afbeeldingen met een grote resolutie wordt impliciet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="48026-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="48026-124">De maximale afmetingen zijn gebaseerd op de door het platform aanbevolen maximale breedte van `1,200px`.</span><span class="sxs-lookup"><span data-stu-id="48026-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="48026-125">Het maximum wordt alleen gebruikt wanneer afbeeldingen groter zijn dan wordt aanbevolen. Verder blijft de hoogte-breedteverhouding behouden wanneer het formaat ervan automatisch wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="48026-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="48026-126">Voorkeuren</span><span class="sxs-lookup"><span data-stu-id="48026-126">Preferences</span></span>

<span data-ttu-id="48026-127">De maximale afmetingen kunnen worden geconfigureerd, maar er is een maximumbreedte van `1200` pixels.</span><span class="sxs-lookup"><span data-stu-id="48026-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="48026-128">Als u de maximale afmetingen wilt configureren, selecteert u **Bestand > Voorkeuren > Instellingen** en filtert u op `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="48026-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Afbeeldingscompressie configureren":::

> [!NOTE]
> <span data-ttu-id="48026-130">Met een waarde van `0` in **Maximumbreedte** of **Maximumhoogte** negeert u eenvoudig afwijkingen van de resolutie.</span><span class="sxs-lookup"><span data-stu-id="48026-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="48026-131">In actie</span><span class="sxs-lookup"><span data-stu-id="48026-131">In action</span></span>

<span data-ttu-id="48026-132">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="48026-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="48026-133">[![Voorbeeld van afbeelding comprimeren](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="48026-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
