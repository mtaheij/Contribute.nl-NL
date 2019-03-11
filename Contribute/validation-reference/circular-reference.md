---
title: circular-reference
description: Uitleg en oplossing voor Docs-buildprobleem circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459206"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Fout

`Files '{file name 1}' and '{file name 2}' reference each other.`

Dit kan bijvoorbeeld een ingesloten bestand zijn dat is gekoppeld aan het huidige bestand of een koppeling naar een bestand dat wordt omgeleid naar het huidige bestand.

## <a name="resolution"></a>Oplossing

Controleer de koppelingen in de bestanden en voer de benodigde wijzigingen uit zodat geen enkel bestand is gekoppeld aan zichzelf of zichzelf bevat.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
