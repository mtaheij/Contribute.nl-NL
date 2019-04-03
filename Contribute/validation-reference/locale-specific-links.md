---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653546"
---
# <a name="locale-specific-links"></a><span data-ttu-id="a78d3-101">Koppelingen voor specifieke landinstellingen</span><span class="sxs-lookup"><span data-stu-id="a78d3-101">Locale-specific links</span></span>

<span data-ttu-id="a78d3-102">Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a78d3-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="a78d3-103">Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie.</span><span class="sxs-lookup"><span data-stu-id="a78d3-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="a78d3-104">Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="a78d3-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="a78d3-105">Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a78d3-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="a78d3-106">Zie dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="a78d3-106">The following is an example.</span></span>

<span data-ttu-id="a78d3-107">Voor:</span><span class="sxs-lookup"><span data-stu-id="a78d3-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="a78d3-108">Na:</span><span class="sxs-lookup"><span data-stu-id="a78d3-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="a78d3-109">Voor de volgende sites is deze validatie vereist:</span><span class="sxs-lookup"><span data-stu-id="a78d3-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="a78d3-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a78d3-110">azure.microsoft.com</span></span>
- <span data-ttu-id="a78d3-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a78d3-111">docs.microsoft.com</span></span>
- <span data-ttu-id="a78d3-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a78d3-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="a78d3-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a78d3-113">technet.microsoft.com</span></span>