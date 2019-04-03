---
title: ms-prod-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636765"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Gebruik `ms.prod` om on-premises producten op te geven. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven, maar als u `ms.technology` opgeeft, moet u ook `ms.prod` opgeven. De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.

## <a name="resolution"></a>Oplossing

Controleer of de waarde voor `ms.technology` die u hebt opgegeven, juist is voor uw artikel. Voeg vervolgens de juiste waarde voor `ms.prod` toe die als geldige bovenliggende waarde voor de `ms.technology` kan worden gebruikt.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
