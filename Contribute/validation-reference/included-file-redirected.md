---
title: included-file-redirected
description: Uitleg en oplossing voor Docs-buildprobleem included-file-redirected
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459068"
---
# <a name="included-file-redirected"></a><span data-ttu-id="543d8-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="543d8-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="543d8-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="543d8-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="543d8-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="543d8-105">Resolution</span></span>

<span data-ttu-id="543d8-106">Herstructureer uw inhoud, zodat u geen omgeleid bestand opneemt.</span><span class="sxs-lookup"><span data-stu-id="543d8-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="543d8-107">Maak bijvoorbeeld een nieuw bestand als u de opgenomen verwijzing wilt opnemen of verwijderen en wilt koppelen naar inhoud of deze inline wilt schrijven.</span><span class="sxs-lookup"><span data-stu-id="543d8-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
