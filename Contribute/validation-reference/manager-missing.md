---
title: manager-missing
description: Uitleg en oplossing voor Docs-buildprobleem manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427492"
---
# <a name="manager-missing"></a>manager-missing

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Voor sommige inhoudsgroepen is het kenmerk `manager` vereist voor het identificeren van de beheerder van de auteur.

## <a name="resolution"></a>Oplossing

Voeg een geldige Microsoft-alias toe voor `manager`:

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
