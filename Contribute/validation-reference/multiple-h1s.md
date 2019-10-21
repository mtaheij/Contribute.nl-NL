---
title: multiple-h1
description: Uitleg en oplossing voor Docs-buildprobleem multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246277"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype. U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop. U kunt slechts één H1 hebben in elk bestand.

U ziet dit bericht mogelijk ook als uw artikel een regel met isgelijktekens bevat die een dubbele onderstreping vormen, zoals dit: `=======`. Dit is een alternatieve Markdown-syntaxis voor een H1. Het komt ook vaak voor bij samenvoegingsconflicten:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

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

Als een extra H1 eigenlijk een dubbele onderstreping is (`=======`), moet u deze, waar van toepassing, verwijderen of vervangen door een hashtag-kop, zoals `##`. Als de dubbele onderstreping het gevolg van een samenvoegingsconflict is, moet u ook de begin- en eindmarkeringen van het samenvoegingsconflict en de verouderde tekst verwijderen.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
