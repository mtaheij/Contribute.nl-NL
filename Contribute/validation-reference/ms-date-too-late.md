---
title: ms-date-too-late
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713103"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="cca8e-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="cca8e-103">ms-date-too-late</span></span>

<span data-ttu-id="cca8e-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="cca8e-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="cca8e-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="cca8e-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="cca8e-106">Het kenmerk `ms.date` wordt gebruikt om de 'nieuwheid' aan te geven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen.</span><span class="sxs-lookup"><span data-stu-id="cca8e-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="cca8e-107">Daarom kan de datum niet in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="cca8e-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="cca8e-108">Vijf dagen zijn toegestaan om rekening te kunnen houden met een releasedatum, bijvoorbeeld wanneer de inhoud is bevroren voor QA ter voorbereiding op een groot evenement.</span><span class="sxs-lookup"><span data-stu-id="cca8e-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="cca8e-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="cca8e-109">Resolution</span></span>

<span data-ttu-id="cca8e-110">Geef een `ms.date` niet eerder dan vijf dagen vanaf vandaag op. Gebruik de indeling MM/DD/JJJJ.</span><span class="sxs-lookup"><span data-stu-id="cca8e-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
