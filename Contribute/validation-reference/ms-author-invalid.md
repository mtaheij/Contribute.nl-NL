---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481706"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Oplossing

Controleer of de `ms.author`-waarde een geldig Microsoft-alias is van de huidige auteur. De aangewezen auteur kan het beste een voltijdse werknemer zijn of teamdistributielijst (DL), in plaats van een leverancier voor de korte termijn. Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.

U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
