---
title: xref-not-found
description: Uitleg en oplossing voor Docs-buildprobleem xref-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427515"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>Waarschuwing

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

De UID waaraan u hebt gekoppeld, bestaat niet of is niet beschikbaar voor uw opslagplaats.

## <a name="resolution"></a>Oplossing

Controleer of de UID correct is en dat de Xref-service correct is geconfigureerd op uw opslagplaats, zoals beschreven in de interne documentatie van Microsoft over de [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
