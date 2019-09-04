---
title: author-missing
description: Uitleg en oplossing voor Docs-buildprobleem author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236296"
---
# <a name="author-missing"></a><span data-ttu-id="7d96a-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="7d96a-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="7d96a-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="7d96a-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="7d96a-105">Het kenmerk `author` identificeert de auteur van het artikel op GitHub-id.</span><span class="sxs-lookup"><span data-stu-id="7d96a-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="7d96a-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7d96a-106">Resolution</span></span>

<span data-ttu-id="7d96a-107">Voeg de GitHub-id van de huidige auteur toe aan de YML-header:</span><span class="sxs-lookup"><span data-stu-id="7d96a-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="7d96a-108">Let op: dit moet de *huidige* eigenaar van het artikel zijn, niet de oorspronkelijke auteur als het eigenaarsschap is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="7d96a-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
