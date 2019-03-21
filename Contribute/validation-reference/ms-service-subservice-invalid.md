---
title: ms-service-and-subservice-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987633"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Binnenkort beschikbaar**

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven. De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn. Uw `ms.service` is ongeldig of de waarde voor `ms.subservice` is geen geldig paar met uw `ms.service`.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.service` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.subservice`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
