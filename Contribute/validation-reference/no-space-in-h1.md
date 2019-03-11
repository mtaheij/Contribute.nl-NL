---
title: no-space-in-h1
description: Uitleg en oplossing voor Docs-buildprobleem no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427504"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Waarschuwing

`A space is required after the hash (#) in H1.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop. Zonder de spatie na de hash, wordt een H1 niet herkend in Docs.

## <a name="resolution"></a>Oplossing

Voeg een spatie toe na de hash in uw H1 om dit probleem op te lossen.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]