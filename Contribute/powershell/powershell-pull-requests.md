---
title: Een pull-aanvraag verzenden
description: Dit artikel beschrijft het proces en best practices voor pull-aanvragen, zodat u zeker weet dat uw bijdrage wordt samengevoegd.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290076"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="f442d-103">Best practice voor pull-aanvragen</span><span class="sxs-lookup"><span data-stu-id="f442d-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="f442d-104">Als u inhoudelijke wijzigingen wilt indienen, dient u een pull-aanvraag in vanuit uw fork.</span><span class="sxs-lookup"><span data-stu-id="f442d-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="f442d-105">Elke pull-aanvraag moet worden gecontroleerd voordat deze kan worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="f442d-105">Every pull request has to be reviewed before it can merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="f442d-106">De juiste vertakking kiezen</span><span class="sxs-lookup"><span data-stu-id="f442d-106">Target the correct branch</span></span>

<span data-ttu-id="f442d-107">Alle wijzigingen moeten worden gemaakt in de vertakking `staging`.</span><span class="sxs-lookup"><span data-stu-id="f442d-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="f442d-108">Wijzigingen mogen nooit zijn gericht op de vertakking `live`.</span><span class="sxs-lookup"><span data-stu-id="f442d-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="f442d-109">Wijzigingen in de vertakking `staging` kunnen worden samengevoegd in `live` zodat alle wijzigingen die in `live` worden gemaakt, worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="f442d-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="f442d-110">Als u een wijziging indient voor documentatie die alleen op een niet-uitgebrachte versie van PowerShell van toepassing is, moet u controleren of er een releasevertakking is voor die versie.</span><span class="sxs-lookup"><span data-stu-id="f442d-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="f442d-111">Alle wijzigingen die op een specifieke, toekomstige versie van toepassing zijn, moeten worden gericht op de releasevertakking.</span><span class="sxs-lookup"><span data-stu-id="f442d-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="f442d-112">Releasevertakkingen hebben het volgende naamgevingspatroon: `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="f442d-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="f442d-113">Zorg ervoor dat de wachtrij voor pull-aanvragen voor iedereen beter werkt</span><span class="sxs-lookup"><span data-stu-id="f442d-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="f442d-114">In de wachtrij voor pull-aanvragen hebben we te maken met twee vaststaande feiten:</span><span class="sxs-lookup"><span data-stu-id="f442d-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="f442d-115">Voor controle van pull-aanvragen met een kleine omvang en gerelateerde wijzigingen is minder tijd nodig.</span><span class="sxs-lookup"><span data-stu-id="f442d-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="f442d-116">Voor controle van pull-aanvragen met een grote omvang of niet-gerelateerde wijzigingen is meer tijd nodig.</span><span class="sxs-lookup"><span data-stu-id="f442d-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="f442d-117">Vermijd vertakkingen waarmee grote aantallen bestanden worden bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="f442d-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="f442d-118">Scheid kleine updates aan bestaande artikelen van nieuwe artikelen of artikelen die grotendeels zijn herschreven.</span><span class="sxs-lookup"><span data-stu-id="f442d-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="f442d-119">Behandel deze wijzigingen in aparte werkstromen.</span><span class="sxs-lookup"><span data-stu-id="f442d-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="f442d-120">Massale wijzigingen drijven pull-aanvragen met grote aantallen gewijzigde bestanden aan.</span><span class="sxs-lookup"><span data-stu-id="f442d-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="f442d-121">Beperk uw pull-aanvragen tot maximaal 50 gewijzigde bestanden.</span><span class="sxs-lookup"><span data-stu-id="f442d-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="f442d-122">Grote pull-aanvragen zijn moeilijk te controleren en gevoeliger voor fouten.</span><span class="sxs-lookup"><span data-stu-id="f442d-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="f442d-123">Bestanden een andere naam geven of verwijderen</span><span class="sxs-lookup"><span data-stu-id="f442d-123">Renaming or deleting files</span></span>

<span data-ttu-id="f442d-124">Als u bestanden een andere naam geeft of verwijdert, moet u voorkomen dat deze wijzigingen worden vermengd met toevoegingen of updates van inhoud.</span><span class="sxs-lookup"><span data-stu-id="f442d-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="f442d-125">Verwerk deze wijzigingen in een afzonderlijke pull-aanvraag die wordt samengevoegd na de pull-aanvraag voor gerelateerde updates.</span><span class="sxs-lookup"><span data-stu-id="f442d-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="f442d-126">Werk bijvoorbeeld het omleidbestand bij en controleer of de omleiding werkt voor u een artikel verwijdert.</span><span class="sxs-lookup"><span data-stu-id="f442d-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="f442d-127">U moet alle bestanden bijwerken die verwijzen naar het bestand waarvan de naam is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f442d-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="f442d-128">Dit omvat ook alle inhoudsopgavebestanden.</span><span class="sxs-lookup"><span data-stu-id="f442d-128">This includes any TOC files.</span></span> <span data-ttu-id="f442d-129">U moet ook omleidingsvermeldingen toevoegen in het omleidingshoofdbestand (`.openpublishing.redirection.json`) in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="f442d-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="f442d-130">Docs PR-validatieservice</span><span class="sxs-lookup"><span data-stu-id="f442d-130">Docs PR validation service</span></span>

<span data-ttu-id="f442d-131">De Docs PR-validatieservice is een GitHub-app die validatieregels uitvoert op de bestanden in een PR.</span><span class="sxs-lookup"><span data-stu-id="f442d-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="f442d-132">U ziet het volgende gedrag:</span><span class="sxs-lookup"><span data-stu-id="f442d-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="f442d-133">U dient een PR in.</span><span class="sxs-lookup"><span data-stu-id="f442d-133">You submit a PR.</span></span>
1. <span data-ttu-id="f442d-134">In de GitHub-opmerking die de status van uw PR aangeeft, ziet u de status van controles die zijn ingeschakeld voor de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="f442d-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="f442d-135">In dit voorbeeld zijn er twee controles ingeschakeld, namelijk "Commit Validation" en "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="f442d-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![sommige controles zijn mislukt](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="f442d-137">De build kan mogelijk toch worden doorgevoerd, ook als de validatie voor het doorvoeren niet is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="f442d-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="f442d-138">Klik op **Details** voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f442d-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="f442d-139">Op de pagina Details ziet u alle validatiecontroles die zijn mislukt, met informatie over wat u moet doen om de problemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="f442d-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="f442d-140">Als de validatie slaagt, wordt de volgende opmerking toegevoegd aan de pull-aanvraag:</span><span class="sxs-lookup"><span data-stu-id="f442d-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![build-validatie](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="f442d-142">Als u een externe bijdrager (dus van buiten Microsoft) bent, hebt u geen toegang tot de gedetailleerde compilatierapporten of preview-koppelingen.</span><span class="sxs-lookup"><span data-stu-id="f442d-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="f442d-143">Build-waarschuwingen</span><span class="sxs-lookup"><span data-stu-id="f442d-143">Build warnings</span></span>

<span data-ttu-id="f442d-144">Normaal gesproken moet u alle build-fouten, -waarschuwingen en -suggesties oplossen.</span><span class="sxs-lookup"><span data-stu-id="f442d-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="f442d-145">Er zijn echter een aantal waarschuwingen die kunnen worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="f442d-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="f442d-146">De volgende waarschuwingen kunnen niet worden genegeerd:</span><span class="sxs-lookup"><span data-stu-id="f442d-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="f442d-147">Kan de servicenaam voor `<version>/<modulepath>/About/About.md` niet vinden</span><span class="sxs-lookup"><span data-stu-id="f442d-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="f442d-148">Metagegevens met een of meer van de volgende namen mogen niet worden ingesteld in de YAML-koptekst, als metagegevens op bestandsniveau in docfx.json of als algemene metagegevens in docfx.json: `locale`.</span><span class="sxs-lookup"><span data-stu-id="f442d-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="f442d-149">Deze worden door het Docs-platform gegenereerd. De waarden die op deze 3 plaatsen worden ingesteld, worden daarom genegeerd.</span><span class="sxs-lookup"><span data-stu-id="f442d-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="f442d-150">Verwijder ze uit alle 3 de plaatsen om de waarschuwing op te lossen.</span><span class="sxs-lookup"><span data-stu-id="f442d-150">Please remove them from all 3 places to resolve the warning.</span></span>
