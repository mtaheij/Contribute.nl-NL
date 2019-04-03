---
title: ms-prod-service-mismatch
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636788"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

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
