---
title: insecure-link
description: Uitleg en oplossing voor Docs-buildprobleem insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587683"
---
# <a name="insecure-link"></a><span data-ttu-id="7db3f-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="7db3f-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7db3f-104">De regel is aanvankelijk ingeschakeld als 'Suggestie', zodat de inhoudteams tijd hebben om de impact te meten en een plan kunnen ontwikkelen om hun opslagplaatsen op te schonen.</span><span class="sxs-lookup"><span data-stu-id="7db3f-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="7db3f-105">**Deze wordt verhoogd naar een waarschuwing op 20-12-2019**.</span><span class="sxs-lookup"><span data-stu-id="7db3f-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="7db3f-106">Suggestie</span><span class="sxs-lookup"><span data-stu-id="7db3f-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="7db3f-107">Dit bericht betekent dat u een expliciete Markdown-koppeling met `http` of een onbewerkte URL, zoals `www.microsoft.com`, hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7db3f-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="7db3f-108">Onbewerkte URL’s worden omgezet in onveilige koppelingen als ze naar Docs worden gepubliceerd en moeten niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7db3f-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="7db3f-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7db3f-109">Resolution</span></span>

<span data-ttu-id="7db3f-110">Wijzig alle URL’s naar Microsoft-websites zodat `https` wordt gebruikt in plaats van `http`.</span><span class="sxs-lookup"><span data-stu-id="7db3f-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="7db3f-111">Als uw koppeling een onbewerkte URL is, moet deze worden gewijzigd naar een expliciete Markdown-koppeling die begint met `https`.</span><span class="sxs-lookup"><span data-stu-id="7db3f-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="7db3f-112">De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen.</span><span class="sxs-lookup"><span data-stu-id="7db3f-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="7db3f-113">Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten.</span><span class="sxs-lookup"><span data-stu-id="7db3f-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="7db3f-114">Het script uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="7db3f-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="7db3f-115">Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.</span><span class="sxs-lookup"><span data-stu-id="7db3f-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="7db3f-116">Klik op alt + M om het menu Markdown te openen.</span><span class="sxs-lookup"><span data-stu-id="7db3f-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="7db3f-117">Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="7db3f-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
