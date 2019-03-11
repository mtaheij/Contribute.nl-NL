---
title: internal-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427493"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Current file doesn't contain a bookmark named '{bookmark}'.`

U probeert te koppelen aan een kop in het huidige bestand dat niet bestaat.

## <a name="resolution"></a>Oplossing

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Controleer de kop waaraan u wilt koppelen en werk de koppeling bij.

Als u een koppeling wilt maken naar een sectie in het huidige artikel, gebruikt u een hash-symbool gevolgd door de woorden van de kop. Verwijder leestekens uit de kop en vervang spaties door streepjes. Een voorbeeld:

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
