---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Koppelingen voor specifieke landinstellingen
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841243"
---
# <a name="locale-specific-links"></a><span data-ttu-id="a35ef-102">Koppelingen voor specifieke landinstellingen</span><span class="sxs-lookup"><span data-stu-id="a35ef-102">Locale-specific links</span></span>

<span data-ttu-id="a35ef-103">Landinstellingscodes, zoals `en-us`, mogen niet worden opgenomen in koppelingen naar bepaalde sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a35ef-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="a35ef-104">Als u een landinstellingscode opneemt in een koppeling in Engelse inhoud, wordt deze ook opgenomen in gelokaliseerde koppelingen. Gebruikers zullen dat ervaren als een slechte lokalisatie.</span><span class="sxs-lookup"><span data-stu-id="a35ef-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="a35ef-105">Als een koppeling in inhoud die in het Duits is gelokaliseerd `en-us` bevat, worden Duitse klanten omgeleid naar het Engelse artikel, ook al is er een Duitse versie beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="a35ef-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="a35ef-106">Verwijder landinstellingscodes uit koppelingen naar sites van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a35ef-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="a35ef-107">Zie dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="a35ef-107">The following is an example.</span></span>

<span data-ttu-id="a35ef-108">Voor:</span><span class="sxs-lookup"><span data-stu-id="a35ef-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="a35ef-109">Na:</span><span class="sxs-lookup"><span data-stu-id="a35ef-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="a35ef-110">Voor de volgende sites is deze validatie vereist:</span><span class="sxs-lookup"><span data-stu-id="a35ef-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="a35ef-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a35ef-111">azure.microsoft.com</span></span>
- <span data-ttu-id="a35ef-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a35ef-112">docs.microsoft.com</span></span>
- <span data-ttu-id="a35ef-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a35ef-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="a35ef-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a35ef-114">technet.microsoft.com</span></span>