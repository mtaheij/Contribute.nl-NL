---
title: ms-author-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246259"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>Waarschuwing

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>Oplossing

Voeg de Microsoft-alias van de huidige auteur toe voor `ms.author`. Let op: dit moet de *huidige* eigenaar van het artikel zijn, niet de oorspronkelijke auteur als het eigenaarsschap is gewijzigd. We adviseren dat de aangewezen auteur een voltijds werknemer of teamdistributielijst (DL) is in plaats van een leverancier voor de korte termijn. 

Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.

U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
