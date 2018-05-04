---
title: Koppelingen in documentatie gebruiken
description: Dit artikel biedt ondersteuning voor het maken van koppelingen naar inhoud in docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="2820e-103">Koppelingen in documentatie gebruiken</span><span class="sxs-lookup"><span data-stu-id="2820e-103">Using links in documentation</span></span>
<span data-ttu-id="2820e-104">In dit artikel wordt beschreven hoe u hyperlinks gebruikt van pagina's die op docs.microsoft.com worden gehost. Koppelingen kunnen eenvoudig in Markdown worden toegevoegd, met een aantal afwijkende conventies.</span><span class="sxs-lookup"><span data-stu-id="2820e-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com. Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="2820e-105">Koppelingen verwijzen gebruikers naar inhoud op dezelfde pagina, naar omliggende pagina's of naar externe websites en URL's.</span><span class="sxs-lookup"><span data-stu-id="2820e-105">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="2820e-106">De docs.microsoft.com site-back-end gebruikt Open Publishing Services (OPS); deze implementeren DocFX Flavored Markdown (DFM).</span><span class="sxs-lookup"><span data-stu-id="2820e-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="2820e-107">DFM is uiterst compatibel met GitHub Flavored Markdown (GFM) en voegt extra functies toe aan de hand van Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="2820e-107">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2820e-108">Alle koppelingen moeten zijn beveiligd (`https` vs. `http`) wanneer het doel dit ondersteunt (dit zou voor de grote meerderheid moeten gelden).</span><span class="sxs-lookup"><span data-stu-id="2820e-108">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="2820e-109">Tekst van koppeling</span><span class="sxs-lookup"><span data-stu-id="2820e-109">Link text</span></span>

<span data-ttu-id="2820e-110">De woorden die u gebruikt in de tekst van de koppeling moeten duidelijk de bestemming van de koppeling aangeven.</span><span class="sxs-lookup"><span data-stu-id="2820e-110">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="2820e-111">Gebruik dus normale beschrijvende tekst of de titel van de pagina die u wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="2820e-111">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2820e-112">Gebruik niet 'klik hier'.</span><span class="sxs-lookup"><span data-stu-id="2820e-112">Do not use "click here."</span></span> <span data-ttu-id="2820e-113">Het is nadelig voor de SEO en geeft geen goede beschrijving van het doelobject.</span><span class="sxs-lookup"><span data-stu-id="2820e-113">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="2820e-114">**Goed:**</span><span class="sxs-lookup"><span data-stu-id="2820e-114">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="2820e-115">**Fout:**</span><span class="sxs-lookup"><span data-stu-id="2820e-115">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="2820e-116">Koppelingen van het ene artikel naar het andere</span><span class="sxs-lookup"><span data-stu-id="2820e-116">Links from one article to another</span></span>

<span data-ttu-id="2820e-117">Als u een inlinekoppeling wilt maken van een technisch Docs-artikel naar een ander technisch Docs-artikel in dezelfde docset, gebruikt u de volgende syntaxis voor de koppeling:</span><span class="sxs-lookup"><span data-stu-id="2820e-117">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="2820e-118">Een artikel in een map wordt gekoppeld aan een ander artikel in dezelfde map:</span><span class="sxs-lookup"><span data-stu-id="2820e-118">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="2820e-119">Een artikel in een submap wordt gekoppeld aan een artikel in de hoofdmap:</span><span class="sxs-lookup"><span data-stu-id="2820e-119">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="2820e-120">Een artikel in de hoofdmap wordt gekoppeld aan een artikel in een submap:</span><span class="sxs-lookup"><span data-stu-id="2820e-120">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="2820e-121">Een artikel in een submap wordt gekoppeld aan een artikel in een andere submap:</span><span class="sxs-lookup"><span data-stu-id="2820e-121">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="2820e-122">Een artikel dat naar meerder docsets koppelt (zelfs in dezelfde opslagplaats): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="2820e-122">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="2820e-123">Koppelingen naar ankers</span><span class="sxs-lookup"><span data-stu-id="2820e-123">Links to anchors</span></span>

<span data-ttu-id="2820e-124">U hoeft geen ankers te maken.</span><span class="sxs-lookup"><span data-stu-id="2820e-124">You do not have to create anchors.</span></span> <span data-ttu-id="2820e-125">Deze worden automatisch gegenereerd tijdens de publicatie van alle H2-koppen.</span><span class="sxs-lookup"><span data-stu-id="2820e-125">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="2820e-126">U hoeft alleen maar koppelingen naar de H2-secties te maken.</span><span class="sxs-lookup"><span data-stu-id="2820e-126">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="2820e-127">U maakt als volgt een koppeling naar een kop in hetzelfde artikel:</span><span class="sxs-lookup"><span data-stu-id="2820e-127">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="2820e-128">U maakt als volgt een koppeling naar een anker in een ander artikel in dezelfde submap:</span><span class="sxs-lookup"><span data-stu-id="2820e-128">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="2820e-129">U maakt als volgt een koppeling naar een anker in een andere servicesubmap:</span><span class="sxs-lookup"><span data-stu-id="2820e-129">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="2820e-130">Koppelingen in Include-bestanden</span><span class="sxs-lookup"><span data-stu-id="2820e-130">Links from includes</span></span>

<span data-ttu-id="2820e-131">Omdat Include-bestanden deel uitmaken van een andere map moet u een langer relatief pad gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2820e-131">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="2820e-132">Gebruik de volgende notatie om vanuit een Include-bestand een koppeling naar een artikel te maken:</span><span class="sxs-lookup"><span data-stu-id="2820e-132">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="2820e-133">Koppelingen in selectors</span><span class="sxs-lookup"><span data-stu-id="2820e-133">Links in selectors</span></span>

<span data-ttu-id="2820e-134">Als u met selectors werkt die zijn opgenomen in een Include-bestand, zoals het Azure-documentatieteam doet, gebruikt u de volgende koppelingsstructuur:</span><span class="sxs-lookup"><span data-stu-id="2820e-134">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="2820e-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="2820e-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="2820e-136">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="2820e-136">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="2820e-137">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="2820e-137">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="2820e-138">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="2820e-138">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="2820e-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="2820e-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="2820e-140">Koppelingen met verwijzingen</span><span class="sxs-lookup"><span data-stu-id="2820e-140">Reference-style links</span></span>

<span data-ttu-id="2820e-141">U kunt koppelingen met verwijzingen gebruiken zodat uw broninhoud gemakkelijker te lezen is.</span><span class="sxs-lookup"><span data-stu-id="2820e-141">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="2820e-142">Bij koppelingen met verwijzingen wordt de syntaxis voor de inlinekoppeling vervangen door een eenvoudige syntaxis en kunnen de lange URL's naar het einde van het artikel worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="2820e-142">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="2820e-143">Hier volgt het voorbeeld van [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="2820e-143">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="2820e-144">Inlinetekst:</span><span class="sxs-lookup"><span data-stu-id="2820e-144">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="2820e-145">Koppelingsverwijzingen aan het einde van het artikel:</span><span class="sxs-lookup"><span data-stu-id="2820e-145">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="2820e-146">Zorg ervoor dat u een spatie typt tussen de dubbele punt en de koppeling.</span><span class="sxs-lookup"><span data-stu-id="2820e-146">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="2820e-147">Als u de spatie vergeet bij het maken van een koppeling naar andere technische artikelen, werkt de koppeling niet meer in het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="2820e-147">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="2820e-148">Een koppeling maken naar pagina's die geen deel uitmaken van de technische documentatie</span><span class="sxs-lookup"><span data-stu-id="2820e-148">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="2820e-149">Als u een koppeling wilt maken naar een pagina in een ander Microsoft-domein (zoals de pagina met prijzen, de SLA-pagina of naar iets dat geen documentatieartikel is), gebruikt u een absolute URL, maar laat u de landcode achterwege.</span><span class="sxs-lookup"><span data-stu-id="2820e-149">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="2820e-150">Het doel hier is dat de koppelingen werken in GitHub en op de weergegeven site:</span><span class="sxs-lookup"><span data-stu-id="2820e-150">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="2820e-151">Een koppeling maken naar sites van derden</span><span class="sxs-lookup"><span data-stu-id="2820e-151">Links to third-party sites</span></span>

<span data-ttu-id="2820e-152">Het beste kunt u gebruikers zo weinig mogelijk doorsturen naar andere sites.</span><span class="sxs-lookup"><span data-stu-id="2820e-152">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="2820e-153">Soms is het echter nodig. Houd in die gevallen rekening met de volgende informatie wanneer u een koppeling maakt naar sites van derden:</span><span class="sxs-lookup"><span data-stu-id="2820e-153">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="2820e-154">**Aansprakelijkheid:** maak een koppeling naar de inhoud van derden als u informatie van deze derde partij wilt delen.</span><span class="sxs-lookup"><span data-stu-id="2820e-154">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="2820e-155">Het is bijvoorbeeld niet de taak van Microsoft om mensen te vertellen hoe ze Android-ontwikkeltools moeten gebruiken. Dat is namelijk de taak van Google.</span><span class="sxs-lookup"><span data-stu-id="2820e-155">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="2820e-156">We kunnen eventueel wel uitleggen hoe Android-ontwikkeltools moeten worden gebruikt *met* Azure, maar het is aan Google om te vertellen hoe hun eigen tools moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2820e-156">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="2820e-157">**Aftekening door PM**: geef aan dat Microsoft verplicht moet aftekenen op inhoud van derden.</span><span class="sxs-lookup"><span data-stu-id="2820e-157">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="2820e-158">Door een koppeling te maken, zeggen we iets over ons vertrouwen in die inhoud en onze verplichtingen als mensen de instructies volgen</span><span class="sxs-lookup"><span data-stu-id="2820e-158">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="2820e-159">**Controle naar de actualiteit van de inhoud:** controleer of de inhoud van de derde partij nog steeds actueel, juist en relevant is en dat de koppeling niet is gewijzigd</span><span class="sxs-lookup"><span data-stu-id="2820e-159">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="2820e-160">**Offsite:** zorg ervoor dat gebruikers er zich van bewust zijn dat ze naar een andere site gaan.</span><span class="sxs-lookup"><span data-stu-id="2820e-160">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="2820e-161">Als dat niet blijkt uit de context, maakt u dat met een aparte zin duidelijk. Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="2820e-161">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="2820e-162">"Tot de vereisten behoren ook de Android-ontwikkeltools die u kunt downloaden op de Android Studio-site".</span><span class="sxs-lookup"><span data-stu-id="2820e-162">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="2820e-163">**Volgende stappen:** het is prima om een koppeling te maken naar, bijvoorbeeld, een MVP-blog in de sectie Volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="2820e-163">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="2820e-164">Maar nogmaals, wijs de gebruikers erop dat ze de site verlaten.</span><span class="sxs-lookup"><span data-stu-id="2820e-164">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="2820e-165">**Juridisch:** we kunnen een beroep doen op de juridisch bindende bepalingen die worden beschreven in de sectie **Koppelingen naar de sites van derden** van de **Gebruiksvoorwaarden**. Deze voorwaarden kunt u openen door op een pagina van ms.com naar de voettekst te gaan.</span><span class="sxs-lookup"><span data-stu-id="2820e-165">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="2820e-166">Een koppeling maken naar MSDN of TechNet</span><span class="sxs-lookup"><span data-stu-id="2820e-166">Links to MSDN or TechNet</span></span>

<span data-ttu-id="2820e-167">Wanneer u een koppeling wilt maken naar MSDN of TechNet, gebruikt u de volledige koppeling naar het onderwerp en verwijdert u de landcode voor de taal uit de koppeling.</span><span class="sxs-lookup"><span data-stu-id="2820e-167">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="2820e-168">Koppeling naar Azure PowerShell-referentiemateriaal</span><span class="sxs-lookup"><span data-stu-id="2820e-168">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="2820e-169">Het Azure PowerShell-referentiemateriaal heeft sinds november 2016 een aantal wijzigingen ondergaan.</span><span class="sxs-lookup"><span data-stu-id="2820e-169">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="2820e-170">Gebruik de volgende richtlijnen om een koppeling naar deze inhoud te maken vanuit andere artikelen op docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="2820e-170">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="2820e-171">Structuur van de URL:</span><span class="sxs-lookup"><span data-stu-id="2820e-171">Structure of the URL:</span></span>

* <span data-ttu-id="2820e-172">Voor cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2820e-172">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="2820e-173">Voor conceptonderwerpen:</span><span class="sxs-lookup"><span data-stu-id="2820e-173">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="2820e-174">De sectie met de &lt;monikernaam&gt; is optioneel.</span><span class="sxs-lookup"><span data-stu-id="2820e-174">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="2820e-175">Als deze sectie wordt weggelaten, wordt u doorgestuurd naar de nieuwste versie van de inhoud.</span><span class="sxs-lookup"><span data-stu-id="2820e-175">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="2820e-176">De &lt;service-name&gt; is een van de voorbeelden die in de volgende basis-URL's wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="2820e-176">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="2820e-177">Azure PowerShell-inhoud (AzureRM): https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="2820e-177">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="2820e-178">Azure PowerShell-inhoud (ASM): https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="2820e-178">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="2820e-179">Azure Active Directory PowerShell-inhoud (AzureAD): https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="2820e-179">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="2820e-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="2820e-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="2820e-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="2820e-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="2820e-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="2820e-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="2820e-183">Wanneer u deze URL's gebruikt, wordt u omgeleid naar de nieuwste versie van de inhoud.</span><span class="sxs-lookup"><span data-stu-id="2820e-183">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="2820e-184">Op die manier hoeft u geen versiemoniker op te geven.</span><span class="sxs-lookup"><span data-stu-id="2820e-184">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="2820e-185">U voorkomt zo ook dat koppelingen naar conceptinhoud moeten worden bijgewerkt wanneer de versie verandert.</span><span class="sxs-lookup"><span data-stu-id="2820e-185">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="2820e-186">Als u een goede koppeling wilt maken, gaat u in uw browser naar de pagina waarnaar u wilt koppelen en kopieert u de URL.</span><span class="sxs-lookup"><span data-stu-id="2820e-186">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="2820e-187">Verwijder vervolgens 'https://docs.microsoft.com' en de gegevens van de landinstelling.</span><span class="sxs-lookup"><span data-stu-id="2820e-187">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="2820e-188">Wanneer u een koppeling vanuit een inhoudsopgave maakt, moet u de volledige URL zonder de landcode gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2820e-188">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="2820e-189">Voorbeeld van Markdown:</span><span class="sxs-lookup"><span data-stu-id="2820e-189">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
