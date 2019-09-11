---
title: internal-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856215"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Waarschuwing

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

U probeert te koppelen aan een kop in het huidige bestand of een ander bestand dat niet bestaat.

## <a name="resolution"></a>Oplossing

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Controleer de kop waaraan u wilt koppelen en werk de koppeling bij.

Als u een koppeling wilt maken naar een sectie in het huidige artikel, gebruikt u een hash-symbool gevolgd door de woorden van de kop. Verwijder leestekens uit de kop en vervang spaties door streepjes. Een voorbeeld:

```markdown
[Managed Disks](#managed-disks)
```

Als u een koppeling wilt maken met een kop in een ander bestand, gebruikt u een relatieve koppeling naar dat bestand, gevolgd door een hash-symbool en de tekst van de kop. Verwijder leestekens uit de kop en vervang spaties door streepjes. Een voorbeeld:

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
