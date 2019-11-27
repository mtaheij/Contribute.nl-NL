---
title: h1-not-first
description: Uitleg en oplossing voor Docs-buildprobleem h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528915"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>Waarschuwing

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
