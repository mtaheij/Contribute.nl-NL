---
title: author-missing
description: Uitleg en oplossing voor Docs-buildprobleem author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288517"
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
