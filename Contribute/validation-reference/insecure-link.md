---
title: insecure-link
description: Uitleg en oplossing voor Docs-buildprobleem insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528853"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> De regel is aanvankelijk ingeschakeld als 'Suggestie', zodat de inhoudteams tijd hebben om de impact te meten en een plan kunnen ontwikkelen om hun opslagplaatsen op te schonen. **Deze wordt verhoogd naar een waarschuwing op 20-12-2019**.

## <a name="suggestion"></a>Suggestie

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Dit bericht betekent dat u een expliciete Markdown-koppeling met `http` of een onbewerkte URL, zoals `www.microsoft.com`, hebt gebruikt. Onbewerkte URL’s worden omgezet in onveilige koppelingen als ze naar Docs worden gepubliceerd en moeten niet worden gebruikt.

## <a name="resolution"></a>Oplossing

Wijzig alle URL’s naar Microsoft-websites zodat `https` wordt gebruikt in plaats van `http`.

Als uw koppeling een onbewerkte URL is, wijzigt u deze in een expliciete Markdown-koppeling die begint met `https`, zoals:

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen. Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten. Het script uitvoeren:
>
> 1. Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.
> 1. Klik op alt + M om het menu Markdown te openen.
> 1. Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.

In sommige gevallen moet u mogelijk webadressen noteren, zoals volledige domeinnamen, die niet bedoeld zijn als klikbare koppelingen. Deze moeten worden opgemaakt als inlinecode, zoals:

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
