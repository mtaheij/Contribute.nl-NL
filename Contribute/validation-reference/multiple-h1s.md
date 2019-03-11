---
title: multiple-h1
description: Uitleg en oplossing voor Docs-buildprobleem multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427525"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>Waarschuwing

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop. U kunt slechts één H1 hebben in elk bestand.

## <a name="resolution"></a>Oplossing

Om dit probleem op te lossen, wijzigt u het kopniveau van H1s in H2 (`##`) of deelt u uw bestand anders in. Het overslaan van kopniveaus, zoals H1 laten volgen door H3, is niet toegestaan.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]