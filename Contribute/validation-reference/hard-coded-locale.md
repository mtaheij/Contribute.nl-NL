---
title: hard-coded-locale
description: Uitleg en oplossing voor Docs-buildprobleem hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427274"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="62c44-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="62c44-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="62c44-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="62c44-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="62c44-105">Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c44-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="62c44-106">Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie.</span><span class="sxs-lookup"><span data-stu-id="62c44-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="62c44-107">Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="62c44-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="62c44-108">Voor de volgende sites is deze validatie vereist:</span><span class="sxs-lookup"><span data-stu-id="62c44-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="62c44-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="62c44-109">azure.microsoft.com</span></span>
- <span data-ttu-id="62c44-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="62c44-110">docs.microsoft.com</span></span>
- <span data-ttu-id="62c44-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="62c44-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="62c44-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="62c44-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="62c44-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="62c44-113">Resolution</span></span>

<span data-ttu-id="62c44-114">Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c44-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="62c44-115">Zie dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="62c44-115">The following is an example.</span></span>

<span data-ttu-id="62c44-116">Voor:</span><span class="sxs-lookup"><span data-stu-id="62c44-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="62c44-117">Na:</span><span class="sxs-lookup"><span data-stu-id="62c44-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]