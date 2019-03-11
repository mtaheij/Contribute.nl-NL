---
title: circular-reference
description: Uitleg en oplossing voor Docs-buildprobleem circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459206"
---
# <a name="circular-reference"></a><span data-ttu-id="c0f67-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="c0f67-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="c0f67-104">Fout</span><span class="sxs-lookup"><span data-stu-id="c0f67-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="c0f67-105">Dit kan bijvoorbeeld een ingesloten bestand zijn dat is gekoppeld aan het huidige bestand of een koppeling naar een bestand dat wordt omgeleid naar het huidige bestand.</span><span class="sxs-lookup"><span data-stu-id="c0f67-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="c0f67-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c0f67-106">Resolution</span></span>

<span data-ttu-id="c0f67-107">Controleer de koppelingen in de bestanden en voer de benodigde wijzigingen uit zodat geen enkel bestand is gekoppeld aan zichzelf of zichzelf bevat.</span><span class="sxs-lookup"><span data-stu-id="c0f67-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
