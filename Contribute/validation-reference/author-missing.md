---
title: author-missing
description: Uitleg en oplossing voor Docs-buildprobleem author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236296"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Waarschuwing

`Missing attribute: author. Add the current author's GitHub ID.`

Het kenmerk `author` identificeert de auteur van het artikel op GitHub-id. 

## <a name="resolution"></a>Oplossing

Voeg de GitHub-id van de huidige auteur toe aan de YML-header:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Let op: dit moet de *huidige* eigenaar van het artikel zijn, niet de oorspronkelijke auteur als het eigenaarsschap is gewijzigd.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
