---
title: Validatie-time-out
description: Uitleg en oplossing voor Docs-buildprobleem validatie-time-out
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033292"
---
# <a name="validation-timeout"></a><span data-ttu-id="3dd73-103">Validatie-time-out</span><span class="sxs-lookup"><span data-stu-id="3dd73-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="3dd73-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="3dd73-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="3dd73-105">Soms kan het door tijdelijke problemen in de validatieservice, zoals een slecht functionerende server, voorkomen dat Docs Build de service op correcte wijze aanroept.</span><span class="sxs-lookup"><span data-stu-id="3dd73-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="3dd73-106">De aanroep registreert na meerdere pogingen een time-out en de validatie wordt geannuleerd om build-vertragingen en een overbelaste build-pipeline te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="3dd73-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="3dd73-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3dd73-107">Resolution</span></span>

<span data-ttu-id="3dd73-108">Probeer uw pull-aanvraag te sluiten en opnieuw te openen of een handmatige build-actie via Docs-portal uit te voeren (alleen mogelijk voor opslagplaatsbeheerders).</span><span class="sxs-lookup"><span data-stu-id="3dd73-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="3dd73-109">Vaak worden serviceproblemen vanzelf opgelost wanneer de handeling opnieuw wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3dd73-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="3dd73-110">Als u hulp nodig hebt van een beheerder of de melding blijft ontvangen, kunt u een probleem melden via [https://SiteHelp](https://SiteHelp) als u een Microsoft-medewerker bent of met een @vermelding van de auteur van een artikel in uw pull-aanvraag om hulp vragen als u een externe inzender bent.</span><span class="sxs-lookup"><span data-stu-id="3dd73-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
