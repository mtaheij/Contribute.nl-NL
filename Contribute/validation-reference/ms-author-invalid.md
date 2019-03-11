---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427505"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="eb33e-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="eb33e-103">ms-author-invalid</span></span>

<span data-ttu-id="eb33e-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="eb33e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="eb33e-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="eb33e-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="eb33e-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="eb33e-106">Resolution</span></span>

<span data-ttu-id="eb33e-107">Controleer of de `ms.author`-waarde een geldig Microsoft-alias is.</span><span class="sxs-lookup"><span data-stu-id="eb33e-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="eb33e-108">Als de alias een distributielijst is, moet deze ook in de whitelist worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="eb33e-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="eb33e-109">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="eb33e-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
