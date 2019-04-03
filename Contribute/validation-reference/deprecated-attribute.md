---
title: deprecated-attribute
description: Uitleg en oplossing voor Docs-buildprobleem deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636880"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="ef1c9-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="ef1c9-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ef1c9-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="ef1c9-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="ef1c9-105">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="ef1c9-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="ef1c9-106">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="ef1c9-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="ef1c9-107">Gebruik `ms.component` niet. Het is voor deze inhoud verouderd.</span><span class="sxs-lookup"><span data-stu-id="ef1c9-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="ef1c9-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ef1c9-108">Resolution</span></span>

<span data-ttu-id="ef1c9-109">Controleer of de waarde van uw `ms.service` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="ef1c9-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="ef1c9-110">Kies vervolgens een geldige waarde voor `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="ef1c9-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="ef1c9-111">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="ef1c9-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
