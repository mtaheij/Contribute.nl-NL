---
title: Validatie-time-out
description: Uitleg en oplossing voor Docs-buildprobleem validatie-time-out
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592546"
---
# <a name="validation-timeout"></a><span data-ttu-id="bc65c-103">Validatie-time-out</span><span class="sxs-lookup"><span data-stu-id="bc65c-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="bc65c-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="bc65c-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="bc65c-105">Soms kan het door tijdelijke problemen in de validatieservice, zoals een slecht functionerende server, voorkomen dat Docs Build de service op correcte wijze aanroept.</span><span class="sxs-lookup"><span data-stu-id="bc65c-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="bc65c-106">De aanroep registreert na meerdere pogingen een time-out en de validatie wordt geannuleerd om build-vertragingen en een overbelaste build-pipeline te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="bc65c-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="bc65c-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="bc65c-107">Resolution</span></span>

<span data-ttu-id="bc65c-108">Sluit uw pull-aanvraag af en open deze opnieuw of forceer een volledige build via [Docs Portal](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="bc65c-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="bc65c-109">Vaak worden serviceproblemen vanzelf opgelost wanneer de handeling opnieuw wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bc65c-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="bc65c-110">U moet een opslagplaatsbeheerder zijn om een build via Docs Portal te forceren.</span><span class="sxs-lookup"><span data-stu-id="bc65c-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="bc65c-111">Als u niet weet wie u opslagplaatsbeheerder is of als u de melding blijft ontvangen na een geforceerde build, kunt u een probleem melden via [https://SiteHelp](https://SiteHelp) als u een Microsoft-medewerker bent of met een @vermelding van de auteur van een artikel in uw pull-aanvraag om hulp vragen als u een externe inzender bent.</span><span class="sxs-lookup"><span data-stu-id="bc65c-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="bc65c-112">Als u een opslagplaatsbeheerder bent, kunt u als volgt een volledige build forceren:</span><span class="sxs-lookup"><span data-stu-id="bc65c-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="bc65c-113">Ga naar [Docs Portal](https://ops.microsoft.com/#/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="bc65c-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="bc65c-114">Zoek de opslagplaats door in de linkerbovenhoek te zoeken en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="bc65c-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="bc65c-115">:::image type="content" source="media/find-repo.png" alt-text="uw opslagplaats zoeken via het zoekvak van Docs Portal":::</span><span class="sxs-lookup"><span data-stu-id="bc65c-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="bc65c-116">Klik op het tabblad **Buildgeschiedenis** op **+ Handmatig publiceren**.</span><span class="sxs-lookup"><span data-stu-id="bc65c-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="bc65c-117">Selecteer de vertakking die de waarschuwing krijgt, zoals Basis.</span><span class="sxs-lookup"><span data-stu-id="bc65c-117">Select the branch that's getting the Warning, such as master.</span></span>
1. <span data-ttu-id="bc65c-118">Behoud de standaard **Docs-site** voor het doel.</span><span class="sxs-lookup"><span data-stu-id="bc65c-118">For target, keep the default, **Docs Site**.</span></span>
1. <span data-ttu-id="bc65c-119">Schakel het selectievakje **Geforceerd publiceren** in.</span><span class="sxs-lookup"><span data-stu-id="bc65c-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="bc65c-120">Klik op **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="bc65c-120">Click **Publish**.</span></span>

   <span data-ttu-id="bc65c-121">:::image type="content" source="media/force-build.png" alt-text="stappen om een volledige build te forceren":::</span><span class="sxs-lookup"><span data-stu-id="bc65c-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="bc65c-122">Hiermee wordt een volledige build op de vertakking geforceerd.</span><span class="sxs-lookup"><span data-stu-id="bc65c-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
