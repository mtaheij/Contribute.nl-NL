---
title: deprecated-attribute
description: Uitleg en oplossing voor Docs-buildprobleem deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987785"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Gebruik `ms.service` om cloudservices op te geven. Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven. Gebruik `ms.component` niet. Het is voor deze inhoud verouderd.

## <a name="resolution"></a>Oplossing

Controleer of de waarde van uw `ms.service` juist is voor uw artikel. Kies vervolgens een geldige waarde voor `ms.subservice`.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
