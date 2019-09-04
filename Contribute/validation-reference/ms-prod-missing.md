---
title: ms-prod-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236295"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

## <a name="warning"></a>Waarschuwing

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Gebruik `ms.prod` om on-premises producten op te geven. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven, maar als u `ms.technology` opgeeft, moet u ook `ms.prod` opgeven. De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.

## <a name="resolution"></a>Oplossing

Controleer of de waarde voor `ms.technology` die u hebt opgegeven, juist is voor uw artikel. Voeg vervolgens de juiste waarde voor `ms.prod` toe die als geldige bovenliggende waarde voor de `ms.technology` kan worden gebruikt.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists). Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
