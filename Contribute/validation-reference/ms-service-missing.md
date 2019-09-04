---
title: ms-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236493"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>Waarschuwing

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven, maar als u `ms.subservice` opgeeft, moet u ook `ms.service` opgeven. De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.

## <a name="resolution"></a>Oplossing

Controleer of de waarde voor `ms.subservice` die u hebt opgegeven, juist is voor uw artikel. Voeg vervolgens de juiste waarde voor `ms.service` toe die als geldige bovenliggende waarde voor de `ms.subservice` kan worden gebruikt.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists). Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
