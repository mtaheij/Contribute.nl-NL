---
title: h1-missing
description: Uitleg en oplossing voor Docs-buildprobleem h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247416"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

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
> Deze regel geldt niet voor ingesloten bestanden. Als er H1-resultaten in ingesloten bestanden worden weergegeven, moet u waarschijnlijk uw ingesloten bestanden insluiten in een `includes`-map. De `includes`-map kan zich op een willekeurig niveau in het bestandspad bevinden. Op basis van het pad herkent Docs-build het bestand als een ingesloten bestand en worden H1-validaties niet uitgevoerd.
>
> Een veelvoorkomende oorzaak van ontbrekende H1's is fout gebruik van de ingesloten bestanden: de H1 bevindt zich in het ingesloten bestand, maar niet in het bovenliggende bestand. Dit is niet toegestaan, omdat het gebruik van een H1 in een ingesloten bestand betekent dat er in bovenliggende bestanden dubbele H1's zijn, of dat het ingesloten bestand maar één keer wordt gebruikt. H1's moeten binnen een inhoudsset uniek zijn en ingesloten bestanden moeten alleen worden gebruikt om inhoud te delen tussen meerdere bestanden. Als er `h1-missing`-resultaten worden weergegeven, omdat de H1 zich in een ingesloten bestand bevindt, is de oplossing om de H1 te verplaatsen naar het bovenliggende bestand, evenals alle ingesloten inhoud als het ingesloten bestand maar één keer wordt gebruikt. Raadpleeg het interne Microsoft-artikel [Herbruikbare inhoud in artikelen insluiten](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master) voor meer informatie over ingesloten bestanden in Docs.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
