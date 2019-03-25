---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987762"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="b978d-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="b978d-103">ms-author-invalid</span></span>

<span data-ttu-id="b978d-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="b978d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b978d-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="b978d-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="b978d-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b978d-106">Resolution</span></span>

<span data-ttu-id="b978d-107">Controleer of de `ms.author`-waarde een geldig Microsoft-alias is.</span><span class="sxs-lookup"><span data-stu-id="b978d-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="b978d-108">Als de alias een distributielijst is, moet deze ook in de toegestane lijst worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b978d-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="b978d-109">U vindt geldige waarden voor DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b978d-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
