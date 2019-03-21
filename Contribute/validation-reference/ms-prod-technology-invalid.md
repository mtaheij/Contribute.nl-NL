---
title: ms-prod-and-technology-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987578"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Binnenkort beschikbaar**

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Gebruik `ms.prod` om on-premises producten op te geven. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven. De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn. Uw `ms.prod` is ongeldig of de waarde voor `ms.technology` is geen geldig paar met uw `ms.prod`.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.prod` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.technology`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
