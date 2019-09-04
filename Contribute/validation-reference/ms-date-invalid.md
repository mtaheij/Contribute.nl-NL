---
title: ms-date-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2f34a0e510d7d006c598ae163217a117a72f1de2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236147"
---
# <a name="ms-date-invalid"></a>ms-date-invalid

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a>Oplossing

Bevestig dat het artikel up-to-date is en geen gebroken inhoud bevat. Voeg vervolgens een geldige datum toe in de indeling MM/DD/JJJJ:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
