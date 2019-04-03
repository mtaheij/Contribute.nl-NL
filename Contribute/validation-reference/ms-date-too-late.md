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
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Het kenmerk `ms.date` wordt gebruikt om de 'nieuwheid' aan te geven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen. Daarom kan de datum niet in de toekomst liggen. Vijf dagen zijn toegestaan om rekening te kunnen houden met een releasedatum, bijvoorbeeld wanneer de inhoud is bevroren voor QA ter voorbereiding op een groot evenement.

## <a name="resolution"></a>Oplossing

Geef een `ms.date` niet eerder dan vijf dagen vanaf vandaag op. Gebruik de indeling MM/DD/JJJJ:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
