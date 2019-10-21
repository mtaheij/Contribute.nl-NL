---
title: hard-coded-locale
description: Uitleg en oplossing voor Docs-buildprobleem hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310325"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="9f353-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="9f353-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="9f353-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="9f353-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="9f353-105">Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9f353-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="9f353-106">Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie.</span><span class="sxs-lookup"><span data-stu-id="9f353-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="9f353-107">Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9f353-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="9f353-108">Voor de volgende sites is deze validatie vereist:</span><span class="sxs-lookup"><span data-stu-id="9f353-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="9f353-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9f353-109">azure.microsoft.com</span></span>
- <span data-ttu-id="9f353-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9f353-110">docs.microsoft.com</span></span>
- <span data-ttu-id="9f353-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9f353-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="9f353-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9f353-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="9f353-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="9f353-113">Resolution</span></span>

<span data-ttu-id="9f353-114">Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9f353-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="9f353-115">Zie dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="9f353-115">The following is an example.</span></span>

<span data-ttu-id="9f353-116">Voor:</span><span class="sxs-lookup"><span data-stu-id="9f353-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="9f353-117">Na:</span><span class="sxs-lookup"><span data-stu-id="9f353-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="9f353-118">De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen.</span><span class="sxs-lookup"><span data-stu-id="9f353-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="9f353-119">Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten.</span><span class="sxs-lookup"><span data-stu-id="9f353-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="9f353-120">Het script uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="9f353-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="9f353-121">Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.</span><span class="sxs-lookup"><span data-stu-id="9f353-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="9f353-122">Klik op alt + M om het menu Markdown te openen.</span><span class="sxs-lookup"><span data-stu-id="9f353-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="9f353-123">Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="9f353-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]