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
# <a name="ms-author-missing"></a><span data-ttu-id="5c16d-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="5c16d-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="5c16d-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="5c16d-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="5c16d-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5c16d-105">Resolution</span></span>

<span data-ttu-id="5c16d-106">Voeg de Microsoft-alias van de huidige auteur toe voor `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="5c16d-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="5c16d-107">Let op: dit moet de *huidige* eigenaar van het artikel zijn, niet de oorspronkelijke auteur als het eigenaarsschap is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5c16d-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="5c16d-108">We adviseren dat de aangewezen auteur een voltijds werknemer of teamdistributielijst (DL) is in plaats van een leverancier voor de korte termijn.</span><span class="sxs-lookup"><span data-stu-id="5c16d-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="5c16d-109">Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="5c16d-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="5c16d-110">U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="5c16d-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
