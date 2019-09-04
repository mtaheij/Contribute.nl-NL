---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236535"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Waarschuwing

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Oplossing

Controleer of de `ms.author`-waarde een geldig Microsoft-alias is van de huidige auteur. Als de alias een distributielijst is, moet deze ook in de toegestane lijst worden opgenomen.

U vindt geldige waarden voor DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
