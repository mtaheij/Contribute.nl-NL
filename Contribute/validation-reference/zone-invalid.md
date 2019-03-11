---
title: zone-invalid
description: Uitleg en oplossing voor Docs-buildprobleem zone-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/4/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0f654d553dcb48cadfc305b91e4f809e3fa69fc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57461713"
---
# <a name="zone-invalid"></a><span data-ttu-id="2c74a-103">zone-invalid</span><span class="sxs-lookup"><span data-stu-id="2c74a-103">zone-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="2c74a-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="2c74a-104">Warning</span></span>

`Invalid zone: No "::: zone-end" found. Blocks should be explicitly closed.`

## <a name="resolution"></a><span data-ttu-id="2c74a-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="2c74a-105">Resolution</span></span>

<span data-ttu-id="2c74a-106">Voeg `::: zone-end` toe aan het einde van de zone.</span><span class="sxs-lookup"><span data-stu-id="2c74a-106">Add `::: zone-end` at the end of your zone.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
