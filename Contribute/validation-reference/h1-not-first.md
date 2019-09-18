---
title: h1-not-first
description: Uitleg en oplossing voor Docs-buildprobleem h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895457"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Markdown content is not allowed before H1.`

Alleen de header van de YAML-metagegevens kan vóór de H1 komen in een Markdown-bestand. Als u bijvoorbeeld boven aan het artikel een notitie of een afbeelding wilt toevoegen, moet deze na H1 komen. Het volgende is niet toegestaan:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Doe dit in plaats daarvan:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Een andere veelvoorkomende oorzaak van dit probleem is [byte order marks (BOM's)](http://www.websina.com/bugzero/kb/unicode-bom.html) vóór de YAML-header. Deze worden soms geïntroduceerd door coderingsproblemen bij het doorvoeren van inhoud naar opslagplaatsen. Ze veroorzaken een ongeldige rendering in GitHub en moeten worden verwijderd.

## <a name="resolution"></a>Oplossing

Verwijder andere inhoud dan de header van de YAML-metagegevens voor de H1.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
