---
title: yaml-header-invalid
description: Uitleg en oplossing voor Docs-buildprobleem yaml-header-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459022"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Waarschuwing

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Dit betekent meestal dat een metagegevenswaarde zonder aanhalingstekens in een YAML-header een dubbele punt of een andere speciaal teken bevat. Het kan ook betekenen dat er een spatie ontbreekt na de dubbele punt in een sleutel-waardepaar.

## <a name="resolution"></a>Oplossing

Controleer uw YAML-header. Zoek naar de volgende fouten.

Dubbele punt in een waarde zonder aanhalingstekens:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Wijzigen in:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Geen spatie na een dubbele punt in een sleutel-waardepaar:

```yml
---
title:I omitted a space.
---
```

Wijzigen in:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
