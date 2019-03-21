---
title: ms-prod-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987693"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Gebruik `ms.prod` om on-premises producten op te geven. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven, maar als u `ms.technology` opgeeft, moet u ook `ms.prod` opgeven. De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.

## <a name="resolution"></a>Oplossing

Controleer of de waarde voor `ms.technology` die u hebt opgegeven, juist is voor uw artikel. Voeg vervolgens de juiste waarde voor `ms.prod` toe die als geldige bovenliggende waarde voor de `ms.technology` kan worden gebruikt.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
