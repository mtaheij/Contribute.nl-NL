---
title: hard-coded-locale
description: Uitleg en oplossing voor Docs-buildprobleem hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0fbc7634e00202fdfdf607b9504744a6d9846792
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590872"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> De regel is aanvankelijk ingeschakeld als 'Suggestie', zodat de inhoudteams tijd hebben om de impact te meten en een plan kunnen ontwikkelen om hun opslagplaatsen op te schonen. **Deze wordt verhoogd naar een waarschuwing op 20-12-2019**.

## <a name="suggestion"></a>Suggestie

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft. Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie. Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.

Voor de volgende sites is deze validatie vereist:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>Oplossing

Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft. Zie dit voorbeeld.

Voor:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Na:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen. Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten. Het script uitvoeren:
>
> 1. Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.
> 1. Klik op alt + M om het menu Markdown te openen.
> 1. Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
