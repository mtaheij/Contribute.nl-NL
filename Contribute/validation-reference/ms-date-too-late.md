---
title: ms-date-too-late
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431479"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="d3f68-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="d3f68-103">ms-date-too-late</span></span>

<span data-ttu-id="d3f68-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="d3f68-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="d3f68-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="d3f68-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="d3f68-106">Het kenmerk `ms.date` wordt gebruikt om de 'nieuwheid' aan te geven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen.</span><span class="sxs-lookup"><span data-stu-id="d3f68-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="d3f68-107">Daarom kan de datum niet in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="d3f68-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="d3f68-108">Vijf dagen zijn toegestaan om rekening te kunnen houden met een releasedatum, bijvoorbeeld wanneer de inhoud is bevroren voor QA ter voorbereiding op een groot evenement.</span><span class="sxs-lookup"><span data-stu-id="d3f68-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="d3f68-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d3f68-109">Resolution</span></span>

<span data-ttu-id="d3f68-110">Geef een `ms.date` niet eerder dan vijf dagen vanaf vandaag op. Gebruik de indeling MM/DD/JJJJ:</span><span class="sxs-lookup"><span data-stu-id="d3f68-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
