---
title: h1-in-moniker
description: Uitleg en oplossing voor Docs-buildprobleem h1-in-moniker.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246355"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop. U kunt slechts één H1 hebben in elk bestand. H1 is niet toegestaan in moniker-secties omdat H1-in-moniker-exemplaren eenvoudig kunnen leiden tot dubbele of ontbrekende H1-exemplaren, afhankelijk van de manier waarop versiebeheer is geconfigureerd.

U ziet dit bericht mogelijk ook als een moniker-sectie een regel met isgelijktekens bevat die een dubbele onderstreping vormen, zoals dit: `=======`. Dit is een alternatieve Markdown-syntaxis voor een H1. Het komt ook vaak voor bij samenvoegingsconflicten:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door alle H1-exemplaren uit alle moniker-secties te verwijderen en te zorgen dat de H1 bovenaan het artikel gepast is voor alle moniker-secties. Het overslaan van kopniveaus, zoals H1 laten volgen door H3, is niet toegestaan.

Als een H1 in een moniker-sectie eigenlijk een dubbele onderstreping is (`=======`), moet u deze, waar van toepassing, verwijderen of vervangen door een hashtag-kop, zoals `##`. Als de dubbele onderstreping het gevolg van een samenvoegingsconflict is, moet u ook de begin- en eindmarkeringen van het samenvoegingsconflict en de verouderde tekst verwijderen.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
