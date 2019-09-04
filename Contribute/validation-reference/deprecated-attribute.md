---
title: deprecated-attribute
description: Uitleg en oplossing voor Docs-buildprobleem deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236242"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

## <a name="warning"></a>Waarschuwing

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven. Gebruik `ms.component` niet. Het is voor deze inhoud verouderd.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.service` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.subservice`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
