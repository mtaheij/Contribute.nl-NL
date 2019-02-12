---
title: ms-component-deprecated
description: Uitleg en oplossing voor Docs-buildprobleem ms-component-deprecated
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713149"
---
# <a name="ms-component-deprecated"></a>ms-component-deprecated

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven. Gebruik `ms.component` niet. Het is voor deze inhoud verouderd.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.service` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.subservice`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
