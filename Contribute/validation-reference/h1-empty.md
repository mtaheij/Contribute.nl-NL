---
title: h1-empty
description: Uitleg en oplossing voor Docs-buildprobleem h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528793"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Waarschuwing

`H1 is required. Add content to your top-level heading.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door ervoor te zorgen dat uw H1 inhoud bevat en niet alleen een hash.

Slecht:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Goed:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
