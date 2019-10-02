---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481706"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="8ea6c-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="8ea6c-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8ea6c-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="8ea6c-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="8ea6c-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8ea6c-105">Resolution</span></span>

<span data-ttu-id="8ea6c-106">Controleer of de `ms.author`-waarde een geldig Microsoft-alias is van de huidige auteur.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="8ea6c-107">De aangewezen auteur kan het beste een voltijdse werknemer zijn of teamdistributielijst (DL), in plaats van een leverancier voor de korte termijn.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="8ea6c-108">Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="8ea6c-109">U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8ea6c-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
