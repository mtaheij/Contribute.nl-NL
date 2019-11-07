---
title: hard-coded-locale
description: Uitleg en oplossing voor Docs-buildprobleem hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166826"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="64850-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="64850-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64850-104">De regel is aanvankelijk ingeschakeld als 'Suggestie', zodat de inhoudteams tijd hebben om de impact te meten en een plan kunnen ontwikkelen om hun opslagplaatsen op te schonen.</span><span class="sxs-lookup"><span data-stu-id="64850-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="64850-105">**Deze wordt verhoogd naar een waarschuwing op 20-12-2019**.</span><span class="sxs-lookup"><span data-stu-id="64850-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="64850-106">Suggestie</span><span class="sxs-lookup"><span data-stu-id="64850-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="64850-107">Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64850-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="64850-108">Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie.</span><span class="sxs-lookup"><span data-stu-id="64850-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="64850-109">Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="64850-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="64850-110">Voor de volgende sites is deze validatie vereist:</span><span class="sxs-lookup"><span data-stu-id="64850-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="64850-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="64850-111">azure.microsoft.com</span></span>
- <span data-ttu-id="64850-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="64850-112">docs.microsoft.com</span></span>
- <span data-ttu-id="64850-113">msdn.microsoft.com (met uitzondering van social.msdn.com, waarvoor de landinstelling is vereist om ervoor te zorgen dat het juiste forum is gekoppeld)</span><span class="sxs-lookup"><span data-stu-id="64850-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="64850-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="64850-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="64850-115">Oplossing</span><span class="sxs-lookup"><span data-stu-id="64850-115">Resolution</span></span>

<span data-ttu-id="64850-116">Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64850-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="64850-117">Zie dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="64850-117">The following is an example.</span></span>

<span data-ttu-id="64850-118">Voor:</span><span class="sxs-lookup"><span data-stu-id="64850-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="64850-119">Na:</span><span class="sxs-lookup"><span data-stu-id="64850-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="64850-120">De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen.</span><span class="sxs-lookup"><span data-stu-id="64850-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="64850-121">Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten.</span><span class="sxs-lookup"><span data-stu-id="64850-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="64850-122">Het script uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="64850-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="64850-123">Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.</span><span class="sxs-lookup"><span data-stu-id="64850-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="64850-124">Klik op alt + M om het menu Markdown te openen.</span><span class="sxs-lookup"><span data-stu-id="64850-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="64850-125">Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="64850-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
