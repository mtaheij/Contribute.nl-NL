---
title: h1-empty
description: Uitleg en oplossing voor Docs-buildprobleem h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427275"
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