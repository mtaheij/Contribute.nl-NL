---
title: ms-date-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236235"
---
# <a name="ms-date-missing"></a>ms-date-missing

## <a name="warning"></a>Waarschuwing

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Bij sommige inhoudsgroepen moet `ms.date` de 'nieuwheid' aangeven, dat wil zeggen wanneer het artikel voor het laatst is beoordeeld op relevantie, nauwkeurigheid, juiste schermafbeeldingen en werkende koppelingen. Deze datum is niet dezelfde als de datum waarop het artikel is *gepubliceerd*. Die datum wordt weergegeven als `ms.date` niet uitdrukkelijk wordt vermeld.

## <a name="resolution"></a>Oplossing

Bevestig dat het artikel up-to-date is en geen gebroken inhoud bevat. Voeg vervolgens een geldige datum toe in de indeling MM/DD/JJJJ:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
