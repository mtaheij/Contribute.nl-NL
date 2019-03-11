---
title: h1-missing
description: Uitleg en oplossing voor Docs-buildprobleem h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459114"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Waarschuwing

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.

## <a name="resolution"></a>Oplossing

Om dit probleem op te lossen, voegt u een H1 toe als de eerste inhoud na het blok met YML-metagegevens in uw bestand:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Deze regel geldt niet voor ingesloten bestanden. Als er H1-waarschuwingen op ingesloten bestanden worden weergegeven, moet u waarschijnlijk uw ingesloten bestanden insluiten in een `includes`-map. De `includes`-map kan zich op een willekeurig niveau in het bestandspad bevinden. Op basis van het pad herkent Docs-build het bestand als een ingesloten bestand en worden H1-validaties niet uitgevoerd.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]