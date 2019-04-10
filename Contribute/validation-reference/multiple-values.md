---
title: multiple-values
description: Uitleg en oplossing voor Docs-buildprobleem multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899654"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

U hebt meer dan één waarde opgegeven voor een kenmerk waarvoor maar één waarde is toegestaan.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Kenmerken die niet meer dan één waarde mogen hebben, moeten worden opgegeven in de YML-indeling (scalar) met één waarde.

## <a name="resolution"></a>Oplossing

U ontvangt deze suggestie telkens wanneer u een matrix met meerdere waarden gebruikt voor een kenmerk met één waarde, of het nu gaat om meerdere waarden of om één waarde in de matrix.

YML ondersteunt de volgende matrixindelingen voor kenmerken met meerdere waarden, bijvoorbeeld `ms.custom`:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Deze indelingen zijn niet geldig voor kenmerken met één waarde, bijvoorbeeld `author`.

Als u meerdere waarden hebt opgegeven, beoordeelt u de specifieke waarden en bepaalt u welke correct is. Verwijder de overige waarden en geef de enkele waarde op dezelfde regel als het kenmerk op, zonder haakjes. Dit doet u als volgt:

```yml
---
author: meganbradley
---
```

Als u een matrix met één waarde hebt, wijzigt u deze in de hierboven genoemde scalarindeling.

## <a name="attributes-in-scope"></a>Kenmerken in het bereik

De volgende kenmerken moeten één waarde hebben:

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
