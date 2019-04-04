---
title: ms-date-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637271"
---
# <a name="ms-date-missing"></a><span data-ttu-id="a3956-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="a3956-103">ms-date-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a3956-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="a3956-104">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="a3956-105">Bij sommige inhoudsgroepen moet `ms.date` de 'nieuwheid' aangeven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen.</span><span class="sxs-lookup"><span data-stu-id="a3956-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a3956-106">Deze datum is niet dezelfde als de datum waarop het artikel is *gepubliceerd*. Die datum wordt weergegeven als `ms.date` niet uitdrukkelijk wordt vermeld.</span><span class="sxs-lookup"><span data-stu-id="a3956-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="a3956-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a3956-107">Resolution</span></span>

<span data-ttu-id="a3956-108">Bevestig dat het artikel up-to-date is en geen gebroken inhoud bevat. Voeg vervolgens een geldige datum toe in de indeling MM/DD/JJJJ:</span><span class="sxs-lookup"><span data-stu-id="a3956-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
