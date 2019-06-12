---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Koppelingen voor specifieke landinstellingen
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841243"
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