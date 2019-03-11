---
title: external-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427457"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Waarschuwing

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

U probeert te koppelen aan een kop in een ander bestand dat niet bestaat.

## <a name="resolution"></a>Oplossing

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Controleer het bestand waaraan u wilt koppelen en werk uw bladwijzerkoppeling bij om te verwijzen naar een geldige sectie in het bestand.

Als u wilt koppelen naar een sectiekop in een ander artikel, gebruikt u de koppeling ten opzichte van het bestand of de site plus een hash-symbool gevolgd door de woorden van de kop. Verwijder leestekens uit de kop en vervang spaties door streepjes. Een voorbeeld:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
