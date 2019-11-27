---
title: h1-no-space
description: Uitleg en oplossing voor Docs-buildprobleem h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528956"
---
# <a name="h1-no-space"></a>h1-no-space

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
