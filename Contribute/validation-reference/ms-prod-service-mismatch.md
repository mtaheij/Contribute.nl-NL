---
title: ms-prod-service-mismatch
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987610"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Binnenkort beschikbaar**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Gebruik `ms.prod` om on-premises producten op te geven, `ms.service` voor cloudservices. Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven. Geef `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven. U kunt `ms.prod` niet gebruiken met `ms.subservice` of `ms.service` niet met `ms.technology`.

## <a name="resolution"></a>Oplossing

Controleer eerst of u de juiste bovenliggende waarde (`ms.prod` of `ms.service`) voor uw artikel hebt geselecteerd. Voeg vervolgens het juiste onderliggende veld toe met een geldige gepaarde waarde. Verwijder eventuele extra velden.

U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
