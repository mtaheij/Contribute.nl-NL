---
title: ms-date-too-late
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637386"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="c1679-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="c1679-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="c1679-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="c1679-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="c1679-105">Het kenmerk `ms.date` wordt gebruikt om de 'nieuwheid' aan te geven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen.</span><span class="sxs-lookup"><span data-stu-id="c1679-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="c1679-106">Daarom kan de datum niet in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="c1679-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="c1679-107">Vijf dagen zijn toegestaan om rekening te kunnen houden met een releasedatum, bijvoorbeeld wanneer de inhoud is bevroren voor QA ter voorbereiding op een groot evenement.</span><span class="sxs-lookup"><span data-stu-id="c1679-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="c1679-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c1679-108">Resolution</span></span>

<span data-ttu-id="c1679-109">Geef een `ms.date` niet eerder dan vijf dagen vanaf vandaag op. Gebruik de indeling MM/DD/JJJJ:</span><span class="sxs-lookup"><span data-stu-id="c1679-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
