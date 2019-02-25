---
title: deprecated-attribute
description: Uitleg en oplossing voor Docs-buildprobleem deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322674"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="3c6d8-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="3c6d8-103">deprecated-attribute</span></span>

<span data-ttu-id="3c6d8-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="3c6d8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3c6d8-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="3c6d8-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="3c6d8-106">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="3c6d8-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="3c6d8-107">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="3c6d8-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="3c6d8-108">Gebruik `ms.component` niet. Het is voor deze inhoud verouderd.</span><span class="sxs-lookup"><span data-stu-id="3c6d8-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c6d8-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3c6d8-109">Resolution</span></span>

<span data-ttu-id="3c6d8-110">Controleer of de waarde van uw `ms.service` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="3c6d8-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="3c6d8-111">Kies vervolgens een geldige waarde voor `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="3c6d8-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="3c6d8-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="3c6d8-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
