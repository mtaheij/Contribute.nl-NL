---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653546"
---
# <a name="locale-specific-links"></a>Koppelingen voor specifieke landinstellingen

Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft. Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie. Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.

Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft. Zie dit voorbeeld.

Voor:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Na:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

Voor de volgende sites is deze validatie vereist:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com