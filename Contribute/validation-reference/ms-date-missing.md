---
title: ms-date-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431456"
---
# <a name="ms-date-missing"></a><span data-ttu-id="d43c3-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="d43c3-103">ms-date-missing</span></span>

<span data-ttu-id="d43c3-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="d43c3-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d43c3-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="d43c3-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="d43c3-106">Deze datum wordt gebruikt om de 'nieuwheid' aan te geven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen.</span><span class="sxs-lookup"><span data-stu-id="d43c3-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="d43c3-107">Deze datum is niet dezelfde als de datum waarop het artikel is *gepubliceerd*. Die datum wordt weergegeven als `ms.date` niet uitdrukkelijk wordt vermeld.</span><span class="sxs-lookup"><span data-stu-id="d43c3-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="d43c3-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d43c3-108">Resolution</span></span>

<span data-ttu-id="d43c3-109">Bevestig dat het artikel up-to-date is en geen gebroken inhoud bevat. Voeg vervolgens een geldige datum toe in de indeling MM/DD/JJJJ:</span><span class="sxs-lookup"><span data-stu-id="d43c3-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
