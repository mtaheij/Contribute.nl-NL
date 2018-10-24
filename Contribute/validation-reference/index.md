---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084470"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="8ac8b-101">Docs PR-validatieservice</span><span class="sxs-lookup"><span data-stu-id="8ac8b-101">Docs PR validation service</span></span>

<span data-ttu-id="8ac8b-102">De Docs PR-validatieservice is een GitHub-app die validatieregels uitvoert op de bestanden in een PR.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="8ac8b-103">Als de validatieservice is ingeschakeld voor een opslagplaats, ziet u het volgende gedrag:</span><span class="sxs-lookup"><span data-stu-id="8ac8b-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="8ac8b-104">U dient een PR in.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-104">You submit a PR.</span></span>
1. <span data-ttu-id="8ac8b-105">In de GitHub-opmerking die de status van uw PR aangeeft, ziet u de status van controles die zijn ingeschakeld voor de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="8ac8b-106">In dit voorbeeld zijn er twee controles ingeschakeld, namelijk "Commit Validation" en "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="8ac8b-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![sommige controles zijn mislukt](media/validation-failed.png)

   <span data-ttu-id="8ac8b-108">De build kan mogelijk toch worden doorgevoerd, ook als de validatie voor het doorvoeren niet is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="8ac8b-109">Klik op **Details** voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="8ac8b-110">Op de pagina Details ziet u alle validatiecontroles die zijn mislukt, met informatie over wat u moet doen om de fouten op te lossen:</span><span class="sxs-lookup"><span data-stu-id="8ac8b-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![validatiebericht](media/validation-details.png)

<span data-ttu-id="8ac8b-112">Zie de inhoudsopgave aan de linkerkant van dit artikel voor de lijst met validaties die momenteel beschikbaar zijn in de service.</span><span class="sxs-lookup"><span data-stu-id="8ac8b-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>