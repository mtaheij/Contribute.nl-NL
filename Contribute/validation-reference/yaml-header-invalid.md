---
title: yaml-header-invalid
description: Uitleg en oplossing voor Docs-buildprobleem yaml-header-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459022"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="905ff-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="905ff-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="905ff-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="905ff-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="905ff-105">Dit betekent meestal dat een metagegevenswaarde zonder aanhalingstekens in een YAML-header een dubbele punt of een andere speciaal teken bevat.</span><span class="sxs-lookup"><span data-stu-id="905ff-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="905ff-106">Het kan ook betekenen dat er een spatie ontbreekt na de dubbele punt in een sleutel-waardepaar.</span><span class="sxs-lookup"><span data-stu-id="905ff-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="905ff-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="905ff-107">Resolution</span></span>

<span data-ttu-id="905ff-108">Controleer uw YAML-header.</span><span class="sxs-lookup"><span data-stu-id="905ff-108">Review your YAML header.</span></span> <span data-ttu-id="905ff-109">Zoek naar de volgende fouten.</span><span class="sxs-lookup"><span data-stu-id="905ff-109">Look for the following mistakes.</span></span>

<span data-ttu-id="905ff-110">Dubbele punt in een waarde zonder aanhalingstekens:</span><span class="sxs-lookup"><span data-stu-id="905ff-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="905ff-111">Wijzigen in:</span><span class="sxs-lookup"><span data-stu-id="905ff-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="905ff-112">Geen spatie na een dubbele punt in een sleutel-waardepaar:</span><span class="sxs-lookup"><span data-stu-id="905ff-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="905ff-113">Wijzigen in:</span><span class="sxs-lookup"><span data-stu-id="905ff-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
