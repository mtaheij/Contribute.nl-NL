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
# <a name="ms-date-too-late"></a>ms-date-too-late

**Binnenkort beschikbaar**

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
