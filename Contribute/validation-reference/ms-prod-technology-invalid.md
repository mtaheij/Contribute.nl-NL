---
title: ms-prod-and-technology-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236335"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Gebruik `ms.prod` om on-premises producten op te geven. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven. De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn. Uw `ms.prod` is ongeldig of de waarde voor `ms.technology` is geen geldig paar met uw `ms.prod`.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.prod` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.technology`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists). Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
