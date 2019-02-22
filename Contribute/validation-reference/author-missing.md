---
title: author-missing
description: Uitleg en oplossing voor Docs-buildprobleem author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431525"
---
# <a name="author-missing"></a><span data-ttu-id="d8066-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="d8066-103">author-missing</span></span>

<span data-ttu-id="d8066-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="d8066-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d8066-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="d8066-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="d8066-106">Het kenmerk `author` identificeert de auteur van het artikel op GitHub-id.</span><span class="sxs-lookup"><span data-stu-id="d8066-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="d8066-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d8066-107">Resolution</span></span>

<span data-ttu-id="d8066-108">Voeg de GitHub-id van de auteur toe aan de YML-header:</span><span class="sxs-lookup"><span data-stu-id="d8066-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]