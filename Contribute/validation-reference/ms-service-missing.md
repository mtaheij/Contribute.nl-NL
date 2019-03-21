---
title: ms-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987716"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven, maar als u `ms.subservice` opgeeft, moet u ook `ms.service` opgeven. De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.

## <a name="resolution"></a>Oplossing

Controleer of de waarde voor `ms.subservice` die u hebt opgegeven, juist is voor uw artikel. Voeg vervolgens de juiste waarde voor `ms.service` toe die als geldige bovenliggende waarde voor de `ms.subservice` kan worden gebruikt.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
