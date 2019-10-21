---
title: insecure-link
description: Uitleg en oplossing voor Docs-buildprobleem insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379517"
---
# <a name="insecure-link"></a>insecure-link

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestie

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Dit bericht betekent dat u een expliciete Markdown-koppeling met `http` of een onbewerkte URL, zoals `www.microsoft.com`, hebt gebruikt. Onbewerkte URL’s worden omgezet in onveilige koppelingen als ze naar Docs worden gepubliceerd en moeten niet worden gebruikt.

## <a name="resolution"></a>Oplossing

Wijzig alle URL’s naar Microsoft-websites zodat `https` wordt gebruikt in plaats van `http`.

Als uw koppeling een onbewerkte URL is, moet deze worden gewijzigd naar een expliciete Markdown-koppeling die begint met `https`.

> [!TIP]
> De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen. Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten. Het script uitvoeren:
>
> 1. Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.
> 1. Klik op alt + M om het menu Markdown te openen.
> 1. Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
