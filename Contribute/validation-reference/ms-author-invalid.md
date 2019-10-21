---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246290"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Oplossing

Werk de `ms.author`-waarde bij met een geldige Microsoft-alias van de huidige auteur. We adviseren dat de aangewezen auteur een voltijds werknemer of teamdistributielijst (DL) is in plaats van een leverancier voor de korte termijn. Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.

U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
