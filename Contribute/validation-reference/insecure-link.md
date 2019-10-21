---
title: insecure-link
description: Uitleg en oplossing voor Docs-buildprobleem insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379517"
---
# <a name="insecure-link"></a><span data-ttu-id="68ae9-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="68ae9-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="68ae9-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="68ae9-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="68ae9-105">Dit bericht betekent dat u een expliciete Markdown-koppeling met `http` of een onbewerkte URL, zoals `www.microsoft.com`, hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="68ae9-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="68ae9-106">Onbewerkte URL’s worden omgezet in onveilige koppelingen als ze naar Docs worden gepubliceerd en moeten niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="68ae9-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="68ae9-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="68ae9-107">Resolution</span></span>

<span data-ttu-id="68ae9-108">Wijzig alle URL’s naar Microsoft-websites zodat `https` wordt gebruikt in plaats van `http`.</span><span class="sxs-lookup"><span data-stu-id="68ae9-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="68ae9-109">Als uw koppeling een onbewerkte URL is, moet deze worden gewijzigd naar een expliciete Markdown-koppeling die begint met `https`.</span><span class="sxs-lookup"><span data-stu-id="68ae9-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="68ae9-110">De Markdown-extensie voor Docs in VS Code bevat een opschoonscript voor Microsoft-koppelingen.</span><span class="sxs-lookup"><span data-stu-id="68ae9-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="68ae9-111">Met het script controleert u alle koppelingen naar Microsoft-sites in een opslagplaats om te zorgen dat ze beginnen met `https` in plaats van `http` en geen codes voor landinstellingen, zoals `en-us`, bevatten.</span><span class="sxs-lookup"><span data-stu-id="68ae9-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="68ae9-112">Het script uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="68ae9-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="68ae9-113">Installeer de [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-extensie voor VS Code.</span><span class="sxs-lookup"><span data-stu-id="68ae9-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="68ae9-114">Klik op alt + M om het menu Markdown te openen.</span><span class="sxs-lookup"><span data-stu-id="68ae9-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="68ae9-115">Selecteer **Opschonen** en daarna **Microsoft-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="68ae9-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
