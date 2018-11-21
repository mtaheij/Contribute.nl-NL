---
title: Markdown-naslaginformatie voor OPS en docs.microsoft.com
description: De OPS-platformhandleiding voor Markdown- en DocFX Flavored Markdown-extensies (DFM).
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 64921bacf48e638221048db4b24e1a941f1d2777
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609540"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="de209-103">Markdown-naslaginformatie voor OPS</span><span class="sxs-lookup"><span data-stu-id="de209-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="de209-104">Markdown is een lichtgewicht opmaakcodetaal met een syntaxis voor het opmaken van platte tekst.</span><span class="sxs-lookup"><span data-stu-id="de209-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="de209-105">Open Publishing Services (OPS) ondersteunt de CommonMark-standaard voor Markdown, plus enkele aangepaste Markdown-extensies die zijn ontworpen om rijkere inhoud op docs.microsoft.com te bieden.</span><span class="sxs-lookup"><span data-stu-id="de209-105">Open Publishing Services (OPS) supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="de209-106">Dit artikel bevat alfabetische naslaginformatie voor het gebruik van Markdown in OPS voor docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="de209-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="de209-107">U kunt voor het opstellen van Markdown elke teksteditor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="de209-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="de209-108">Voor elke editor die het invoegen van zowel standaard-Markdown-syntaxis als aangepaste OPS-extensies mogelijk maakt, wordt [VS Code](https://code.visualstudio.com/) met een geïnstalleerd [Docs-ontwerppakket](https://aka.ms/DocsAuthoringPack) aangeraden.</span><span class="sxs-lookup"><span data-stu-id="de209-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="de209-109">OPS is gestandaardiseerd in Markdig voor alle nieuwe opslagplaatsen, en oudere opslagplaatsen worden gemigreerd naar Markdig.</span><span class="sxs-lookup"><span data-stu-id="de209-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="de209-110">U kunt het weergeven van Markdown in Markdig versus andere engines testen op [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="de209-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="de209-111">Waarschuwingen (Opmerking, Tip, Belangrijk, Let op, Waarschuwing)</span><span class="sxs-lookup"><span data-stu-id="de209-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="de209-112">Alerts is een OPS-specifieke Markdown-extensie om blokcitaten te maken die op docs.microsoft.com worden weergegeven met kleuren en pictogrammen die het belang van de inhoud aanduiden.</span><span class="sxs-lookup"><span data-stu-id="de209-112">Alerts is an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="de209-113">De volgende typen waarschuwingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="de209-113">The following alert types are supported:</span></span>

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="de209-114">Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="de209-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="de209-115">Informatie die de gebruiker ook bij globaal scannen moet zien.</span><span class="sxs-lookup"><span data-stu-id="de209-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="de209-116">Optionele informatie waarmee een gebruiker meer succes zal hebben.</span><span class="sxs-lookup"><span data-stu-id="de209-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de209-117">Informatie die essentieel voor de gebruiker is om succes te hebben.</span><span class="sxs-lookup"><span data-stu-id="de209-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="de209-118">Mogelijke negatieve gevolgen van een actie.</span><span class="sxs-lookup"><span data-stu-id="de209-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="de209-119">Bepaalde gevaarlijke gevolgen van een actie.</span><span class="sxs-lookup"><span data-stu-id="de209-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="de209-120">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="de209-120">Code snippets</span></span>

<span data-ttu-id="de209-121">U kunt codefragmenten in uw Markdown-bestanden insluiten:</span><span class="sxs-lookup"><span data-stu-id="de209-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="de209-122">Koppen</span><span class="sxs-lookup"><span data-stu-id="de209-122">Headings</span></span>

<span data-ttu-id="de209-123">OPS ondersteunt zes niveaus Markdown-koppen:</span><span class="sxs-lookup"><span data-stu-id="de209-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="de209-124">Tussen de laatste `#` en de koptekst moet een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="de209-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="de209-125">Elk Markdown-bestand moet precies één H1 hebben.</span><span class="sxs-lookup"><span data-stu-id="de209-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="de209-126">De H1 moet de eerste inhoud in het bestand zijn na het YML-blok met metagegevens.</span><span class="sxs-lookup"><span data-stu-id="de209-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="de209-127">H2's verschijnen automatisch in het navigatiemenu aan de rechterkant van het gepubliceerde bestand.</span><span class="sxs-lookup"><span data-stu-id="de209-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="de209-128">Dit geldt niet voor koppen op een lager niveau. Gebruik H2's dus strategisch om lezers te helpen door uw inhoud te navigeren.</span><span class="sxs-lookup"><span data-stu-id="de209-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="de209-129">HMTL-koppen, zoals `<h1>`, worden niet aanbevolen en leiden in sommige gevallen tot compileerwaarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="de209-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="de209-130">U kunt de afzonderlijke koppen in een bestand koppelen via [bladwijzers](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="de209-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="de209-131">HTML</span><span class="sxs-lookup"><span data-stu-id="de209-131">HTML</span></span>

<span data-ttu-id="de209-132">Hoewel Markdown ondersteuning biedt voor inline-HTML, wordt HTML niet aanbevolen voor het publiceren via OPS. Bovendien leidt dit, behalve bij een beperkte lijst met waarden, tot compileerfouten of -waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="de209-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="de209-133">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="de209-133">Images</span></span>

<span data-ttu-id="de209-134">De syntaxis voor het insluiten van een afbeelding is:</span><span class="sxs-lookup"><span data-stu-id="de209-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="de209-135">Hierbij is `alt text` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="de209-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="de209-136">Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig.</span><span class="sxs-lookup"><span data-stu-id="de209-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="de209-137">Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.</span><span class="sxs-lookup"><span data-stu-id="de209-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="de209-138">Afbeeldingen moeten worden opgeslagen in een `/media`-map in uw docset.</span><span class="sxs-lookup"><span data-stu-id="de209-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="de209-139">De volgende bestandstypen worden standaard voor afbeeldingen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="de209-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="de209-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="de209-140">.jpg</span></span>
- <span data-ttu-id="de209-141">.png</span><span class="sxs-lookup"><span data-stu-id="de209-141">.png</span></span>

<span data-ttu-id="de209-142">U kunt ook ondersteuning voor andere typen afbeeldingen toevoegen door deze toe te voegen als resources aan het docfx.json-bestand<!--add link to reference when available--> voor uw docset.</span><span class="sxs-lookup"><span data-stu-id="de209-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="de209-143">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="de209-143">Links</span></span>

<span data-ttu-id="de209-144">In de meeste gevallen gebruikt OPS standaard-Markdown-koppelingen naar andere bestanden en pagina's.</span><span class="sxs-lookup"><span data-stu-id="de209-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="de209-145">De typen koppelingen worden in de onderstaande subsecties beschreven.</span><span class="sxs-lookup"><span data-stu-id="de209-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="de209-146">Het Docs-ontwerppakket voor VS Code kan helpen relatieve koppelingen en bladwijzers correct in te voegen zonder dat u zich met paden bezig hoeft te houden.</span><span class="sxs-lookup"><span data-stu-id="de209-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de209-147">Neem geen codes voor landinstellingen, zoals nl-nl, in uw koppelingen naar Microsoft-sites op.</span><span class="sxs-lookup"><span data-stu-id="de209-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="de209-148">Landinstellingscodes die in code zijn vastgelegd verhinderen dat gelokaliseerde inhoud wordt weergegeven. Dit leidt tot een slechte klantervaring voor gebruikers in andere regio's en brengt aanzienlijke lokalisatiekosten met zich mee.</span><span class="sxs-lookup"><span data-stu-id="de209-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="de209-149">Wanneer u een URL uit een browser kopieert, wordt de landinstellingscode standaard opgenomen. U moet deze handmatig dus verwijderen wanneer u een koppeling maakt.</span><span class="sxs-lookup"><span data-stu-id="de209-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="de209-150">Gebruik bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="de209-151">Niet:</span><span class="sxs-lookup"><span data-stu-id="de209-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="de209-152">Relatieve koppelingen naar bestanden in dezelfde docset</span><span class="sxs-lookup"><span data-stu-id="de209-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="de209-153">Een relatief pad is het pad naar het doelbestand ten opzichte van het huidige bestand.</span><span class="sxs-lookup"><span data-stu-id="de209-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="de209-154">U kunt in OPS een relatief pad gebruiken om een koppeling naar ander bestand in dezelfde docset te maken.</span><span class="sxs-lookup"><span data-stu-id="de209-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="de209-155">De syntaxis voor een relatief pad ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="de209-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="de209-156">Hierbij duidt `../` één niveau hoger in de hiërarchie aan.</span><span class="sxs-lookup"><span data-stu-id="de209-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="de209-157">Het relatieve pad wordt tijdens het compileren omgezet, met inbegrip van het verwijderen van de MD-extensie.</span><span class="sxs-lookup"><span data-stu-id="de209-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="de209-158">U kunt ../ gebruiken om het bestand te koppelen aan een bestand in de bovenliggende map, maar dat bestand moet dan wel in dezelfde docset aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="de209-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="de209-159">U kunt ../ niet gebruiken om een bestand te koppelen aan een bestand in een andere docset-map.</span><span class="sxs-lookup"><span data-stu-id="de209-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="de209-160">OPS ondersteunt ook een speciale vorm van een relatief pad. Deze vorm begint met het teken ~ (bijvoorbeeld ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="de209-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="de209-161">Met deze syntaxis wordt een bestand ten opzichte van de hoofdmap van een docset aangegeven.</span><span class="sxs-lookup"><span data-stu-id="de209-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="de209-162">Ook dit type pad wordt tijdens de build gevalideerd en omgezet.</span><span class="sxs-lookup"><span data-stu-id="de209-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de209-163">Neem de bestandsextensie in het relatieve pad op.</span><span class="sxs-lookup"><span data-stu-id="de209-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="de209-164">Bij het compileren wordt het bestaan van het doelbestand van dat relatieve pad gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="de209-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="de209-165">Als het relatieve pad geen bestandsextensie bevat, wordt bij het compileren waarschijnlijk een waarschuwing of verbroken koppeling gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="de209-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="de209-166">Gebruik bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="de209-167">Niet:</span><span class="sxs-lookup"><span data-stu-id="de209-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="de209-168">Absolute koppelingen naar andere bestanden in OPS</span><span class="sxs-lookup"><span data-stu-id="de209-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="de209-169">Neem de bestandsextensie (.md) niet op.</span><span class="sxs-lookup"><span data-stu-id="de209-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="de209-170">Deze koppelt naar het Linux-overzichtsbestand van buiten de Azure-docset 'articles'.</span><span class="sxs-lookup"><span data-stu-id="de209-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="de209-171">Koppelingen naar externe sites</span><span class="sxs-lookup"><span data-stu-id="de209-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="de209-172">Op URL gebaseerde koppeling naar een andere webpagina (moet https:// bevatten).</span><span class="sxs-lookup"><span data-stu-id="de209-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="de209-173">Bladwijzerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="de209-173">Bookmark links</span></span>

<span data-ttu-id="de209-174">Bladwijzerkoppeling naar een kop in een ander bestand in dezelfde opslagplaats:</span><span class="sxs-lookup"><span data-stu-id="de209-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="de209-175">Bladwijzerkoppeling naar een kop in het huidige bestand:</span><span class="sxs-lookup"><span data-stu-id="de209-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="de209-176">Gebruik een hash-code gevolgd door de woorden van de kop zonder leestekens en met streepjes als vervanging voor spaties.</span><span class="sxs-lookup"><span data-stu-id="de209-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="de209-177">Expliciete ankerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="de209-177">Explicit anchor links</span></span>

<span data-ttu-id="de209-178">Expliciete ankerkoppelingen die de `<a>`-HTML-tag gebruiken worden **niet vereist of aanbevolen** behalve in hub- en landingspagina's.</span><span class="sxs-lookup"><span data-stu-id="de209-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="de209-179">Gebruik in algemene Markdown-bestanden bladwijzers zoals hierboven wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="de209-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="de209-180">Gebruik als volgt ankers voor hub- en landingspagina's:</span><span class="sxs-lookup"><span data-stu-id="de209-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="de209-181">`## <a id="AnchorText"> </a>Header text` of `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="de209-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="de209-182">Gebruik de volgende syntaxis om een koppeling naar expliciete ankers te maken:</span><span class="sxs-lookup"><span data-stu-id="de209-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="de209-183">XREF-koppelingen (kruisverwijzing)</span><span class="sxs-lookup"><span data-stu-id="de209-183">XREF (cross reference) links</span></span>

<span data-ttu-id="de209-184">Als u in de huidige docset of andere docsets een koppeling wilt maken naar automatisch gegenereerde pagina's met API-naslaginformatie, gebruikt u XREF-koppelingen met de unieke id (UID).</span><span class="sxs-lookup"><span data-stu-id="de209-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="de209-185">Als u wilt verwijzen naar pagina's met API-naslaginformatie in andere docsets, moet u `xrefService`-configuratie in het `docfx.json`-bestand toevoegen.</span><span class="sxs-lookup"><span data-stu-id="de209-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="de209-186">De UID is gelijk aan de volledig gekwalificeerde naam van de klasse en het lid.</span><span class="sxs-lookup"><span data-stu-id="de209-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="de209-187">Als u een \* toevoegt na de UID, vertegenwoordigt de koppeling een overbelastingspagina en niet een specifieke API.</span><span class="sxs-lookup"><span data-stu-id="de209-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="de209-188">Gebruik bijvoorbeeld `List<T>.BinarySearch*` om een koppeling naar de pagina BinarySearch Method te maken in plaats van te koppelen naar een specifieke overbelasting zoals `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="de209-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="de209-189">Voor de syntaxis hebt u de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="de209-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="de209-190">Automatisch koppelen: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="de209-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="de209-191">De optionele queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst.</span><span class="sxs-lookup"><span data-stu-id="de209-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="de209-192">Standaard toont de koppelingstekst alleen de naam van het lid of het type.</span><span class="sxs-lookup"><span data-stu-id="de209-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="de209-193">Markdown-koppeling: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="de209-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="de209-194">Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="de209-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="de209-195">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="de209-195">Examples:</span></span>

- <span data-ttu-id="de209-196">`<xref:System.String>` wordt weergegeven als String.</span><span class="sxs-lookup"><span data-stu-id="de209-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="de209-197">`<xref:System.String?displayProperty=nameWithType>` wordt weergegeven als System.String.</span><span class="sxs-lookup"><span data-stu-id="de209-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="de209-198">`[String class](xref:System.String)` wordt weergeven als String class.</span><span class="sxs-lookup"><span data-stu-id="de209-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="de209-199">Momenteel is er geen eenvoudige manier om de UID's te zoeken.</span><span class="sxs-lookup"><span data-stu-id="de209-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="de209-200"><!-- ? -->De beste manier om de UID voor een API te zoeken, is om de bron van de API-pagina waaraan u wilt koppelen te bekijken en de waarde ms.assetid te zoeken.</span><span class="sxs-lookup"><span data-stu-id="de209-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="de209-201">Afzonderlijke overbelastingswaarden worden in de bron niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de209-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="de209-202">We werken aan een beter systeem voor de toekomst.</span><span class="sxs-lookup"><span data-stu-id="de209-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="de209-203">Wanneer de UID de speciale tekens \`, \# of \* bevat, moet de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML worden gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="de209-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="de209-204">U ziet soms haakjes in de code, maar dat is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="de209-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="de209-205">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="de209-205">Examples:</span></span>

- <span data-ttu-id="de209-206">System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="de209-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="de209-207">System.Exception. \#ctor wordt `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="de209-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="de209-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="de209-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="de209-209">Lijsten (Genummerd, Met opsommingstekens, Controlelijst)</span><span class="sxs-lookup"><span data-stu-id="de209-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="de209-210">Genummerde lijst</span><span class="sxs-lookup"><span data-stu-id="de209-210">Numbered list</span></span>

<span data-ttu-id="de209-211">Als u een genummerde lijst wilt maken, kunt u alle 1's gebruiken. Deze worden bij het publiceren weergegeven als een sequentiële lijst.</span><span class="sxs-lookup"><span data-stu-id="de209-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="de209-212">Voor betere leesbaarheid van de bron kunt u uw lijsten verhogen.</span><span class="sxs-lookup"><span data-stu-id="de209-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="de209-213">Gebruik geen letters in lijsten, ook niet in geneste lijsten.</span><span class="sxs-lookup"><span data-stu-id="de209-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="de209-214">Deze worden bij het publiceren via OPS niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de209-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="de209-215">Geneste lijsten die gebruikmaken van nummers, worden bij het publiceren weergegeven als kleine letters.</span><span class="sxs-lookup"><span data-stu-id="de209-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="de209-216">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="de209-217">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-217">This renders as follows:</span></span>

1. <span data-ttu-id="de209-218">Dit is</span><span class="sxs-lookup"><span data-stu-id="de209-218">This is</span></span>
1. <span data-ttu-id="de209-219">een bovenliggende lijst met nummers</span><span class="sxs-lookup"><span data-stu-id="de209-219">a parent numbered list</span></span>
   1. <span data-ttu-id="de209-220">en dit is</span><span class="sxs-lookup"><span data-stu-id="de209-220">and this is</span></span>
   1. <span data-ttu-id="de209-221">een geneste lijst met nummers</span><span class="sxs-lookup"><span data-stu-id="de209-221">a nested numbered list</span></span>
1. <span data-ttu-id="de209-222">(einde)</span><span class="sxs-lookup"><span data-stu-id="de209-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="de209-223">Lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="de209-223">Bulleted list</span></span>

<span data-ttu-id="de209-224">Als u een lijst met opsommingstekens wilt maken, gebruikt u `-` gevolgd door een spatie aan het begin van elke regel:</span><span class="sxs-lookup"><span data-stu-id="de209-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="de209-225">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-225">This renders as follows:</span></span>

- <span data-ttu-id="de209-226">Dit is</span><span class="sxs-lookup"><span data-stu-id="de209-226">This is</span></span>
- <span data-ttu-id="de209-227">een bovenliggende lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="de209-227">a parent bulleted list</span></span>
  - <span data-ttu-id="de209-228">en dit is</span><span class="sxs-lookup"><span data-stu-id="de209-228">and this is</span></span>
  - <span data-ttu-id="de209-229">een geneste lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="de209-229">a nested bulleted list</span></span>
- <span data-ttu-id="de209-230">Klaar!</span><span class="sxs-lookup"><span data-stu-id="de209-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="de209-231">Controlelijst</span><span class="sxs-lookup"><span data-stu-id="de209-231">Checklist</span></span>

<span data-ttu-id="de209-232">Controlelijsten zijn beschikbaar voor gebruik op (alleen) docs.microsoft.com via een aangepaste Markdown-extensie:</span><span class="sxs-lookup"><span data-stu-id="de209-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="de209-233">Dit voorbeeld wordt op docs.microsoft.com weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="de209-234">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="de209-234">List item 1</span></span>
> * <span data-ttu-id="de209-235">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="de209-235">List item 2</span></span>
> * <span data-ttu-id="de209-236">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="de209-236">List item 3</span></span>

<span data-ttu-id="de209-237">Gebruik controlelijsten aan het begin of eind van een artikel om inhoud voor 'Wat gaat u leren' of 'Wat hebt u geleerd' samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="de209-237">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="de209-238">Voeg geen willekeurige controlelijsten ergens anders in een artikel toe.</span><span class="sxs-lookup"><span data-stu-id="de209-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="de209-239">Actie volgende stap</span><span class="sxs-lookup"><span data-stu-id="de209-239">Next step action</span></span>

<span data-ttu-id="de209-240">U kunt een aangepaste extensie gebruiken om een knop voor de actie van de volgende stap toe te voegen aan pagina's op (alleen) docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="de209-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="de209-241">De syntaxis ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="de209-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="de209-242">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="de209-243">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="de209-244">Informatie over de basisstijl</span><span class="sxs-lookup"><span data-stu-id="de209-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="de209-245">U kunt elke ondersteunde koppeling in een volgende stapactie gebruiken, met inbegrip van een Markdown-koppeling naar een andere webpagina.</span><span class="sxs-lookup"><span data-stu-id="de209-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="de209-246">In de meeste gevallen is de koppeling voor de volgende actie een relatieve koppeling naar een ander bestand in dezelfde docset.</span><span class="sxs-lookup"><span data-stu-id="de209-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="de209-247">Sectiedefinitie</span><span class="sxs-lookup"><span data-stu-id="de209-247">Section definition</span></span>

<span data-ttu-id="de209-248"><!-- more info about this would be helpful! --> U moet mogelijk een sectie definiëren.</span><span class="sxs-lookup"><span data-stu-id="de209-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="de209-249">Deze syntaxis wordt voornamelijk gebruikt voor codetabellen.</span><span class="sxs-lookup"><span data-stu-id="de209-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="de209-250">Zie het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="de209-251">De eraan voorafgaande blockquote-Markdown-tekst wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="de209-252">Selectors</span><span class="sxs-lookup"><span data-stu-id="de209-252">Selectors</span></span>

<span data-ttu-id="de209-253"><!-- could be more clear! --> U kunt een selector gebruiken wanneer u verschillende pagina's voor hetzelfde artikel met elkaar wilt verbinden.</span><span class="sxs-lookup"><span data-stu-id="de209-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="de209-254">Lezers kunnen dan schakelen tussen die pagina's.</span><span class="sxs-lookup"><span data-stu-id="de209-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="de209-255">Deze extensie werkt anders tussen docs.microsoft.com en MSDN.</span><span class="sxs-lookup"><span data-stu-id="de209-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="de209-256">Single selector</span><span class="sxs-lookup"><span data-stu-id="de209-256">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="de209-257">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="de209-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="de209-266">Multi-selector</span><span class="sxs-lookup"><span data-stu-id="de209-266">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="de209-267">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="de209-267">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="de209-278">Tabellen</span><span class="sxs-lookup"><span data-stu-id="de209-278">Tables</span></span>

<span data-ttu-id="de209-279">De eenvoudigste manier om een tabel in Markdown te maken is gebruik te maken van pipes en regels.</span><span class="sxs-lookup"><span data-stu-id="de209-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="de209-280">Als u een standaardtabel met een kop wilt maken, laat u de eerste regel volgen door een stippellijn:</span><span class="sxs-lookup"><span data-stu-id="de209-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="de209-281">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-281">This renders as follows:</span></span>

|<span data-ttu-id="de209-282">Dit is</span><span class="sxs-lookup"><span data-stu-id="de209-282">This is</span></span>   |<span data-ttu-id="de209-283">een eenvoudige</span><span class="sxs-lookup"><span data-stu-id="de209-283">a simple</span></span>   |<span data-ttu-id="de209-284">tabelkop</span><span class="sxs-lookup"><span data-stu-id="de209-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="de209-285">tabel</span><span class="sxs-lookup"><span data-stu-id="de209-285">table</span></span>     |<span data-ttu-id="de209-286">gegevens</span><span class="sxs-lookup"><span data-stu-id="de209-286">data</span></span>       |<span data-ttu-id="de209-287">hier</span><span class="sxs-lookup"><span data-stu-id="de209-287">here</span></span>        |
|<span data-ttu-id="de209-288">deze hoeft niet</span><span class="sxs-lookup"><span data-stu-id="de209-288">it doesn't</span></span>|<span data-ttu-id="de209-289">precies</span><span class="sxs-lookup"><span data-stu-id="de209-289">actually</span></span>   |<span data-ttu-id="de209-290">te zijn uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="de209-290">have to line up nicely!</span></span>||

<span data-ttu-id="de209-291">U kunt ook een tabel zonder kop maken.</span><span class="sxs-lookup"><span data-stu-id="de209-291">You can also create a table without a header.</span></span> <span data-ttu-id="de209-292">Ga bijvoorbeeld als volgt te werk om een lijst met meerdere kolommen te maken:</span><span class="sxs-lookup"><span data-stu-id="de209-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="de209-293">Dit wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="de209-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="de209-294">Deze</span><span class="sxs-lookup"><span data-stu-id="de209-294">This</span></span> | <span data-ttu-id="de209-295">tabel</span><span class="sxs-lookup"><span data-stu-id="de209-295">table</span></span> |
| <span data-ttu-id="de209-296">heeft geen</span><span class="sxs-lookup"><span data-stu-id="de209-296">has no</span></span> | <span data-ttu-id="de209-297">kop</span><span class="sxs-lookup"><span data-stu-id="de209-297">header</span></span> |

<span data-ttu-id="de209-298">U kunt de kolommen uitlijnen met behulp van dubbele punten:</span><span class="sxs-lookup"><span data-stu-id="de209-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="de209-299">Wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="de209-300">rechts uitgelijnd:</span><span class="sxs-lookup"><span data-stu-id="de209-300">right aligned:</span></span>|
|<span data-ttu-id="de209-301">:links uitgelijnd</span><span class="sxs-lookup"><span data-stu-id="de209-301">:left aligned</span></span>     |
|<span data-ttu-id="de209-302">:gecentreerd        :</span><span class="sxs-lookup"><span data-stu-id="de209-302">:centered        :</span></span>|

> [!TIP]
> U kunt met Docs Authoring Extension voor VS Code gemakkelijk basis-Markdown-tabellen toevoegen.
>
> U kunt ook een [onlinegenerator voor tabellen](http://www.tablesgenerator.com/markdown_tables) gebruiken.

### <a name="mx-tdbreakall"></a><span data-ttu-id="de209-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="de209-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Dit werkt alleen op de site docs.microsoft.com.

<span data-ttu-id="de209-307">Als u een tabel in Markdown maakt, kan de tabel worden uitgebreid naar het navigatievenster rechts, waardoor de tabel onleesbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="de209-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="de209-308">Dat is op te lossen door bij het renderen van Docs de tabel op te splitsen wanneer dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="de209-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="de209-309">U laat eenvoudig de tabel teruglopen met de aangepaste klasse `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="de209-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="de209-310">Hier ziet u een Markdown-voorbeeld van een tabel met drie rijen die teruglopen door gebruik te maken van een `div` met de klassenaam `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="de209-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="de209-311">Deze wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="de209-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="de209-312">Naam</span><span class="sxs-lookup"><span data-stu-id="de209-312">Name</span></span>|<span data-ttu-id="de209-313">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="de209-313">Syntax</span></span>|<span data-ttu-id="de209-314">Verplicht voor installatie op de achtergrond?</span><span class="sxs-lookup"><span data-stu-id="de209-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="de209-315">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="de209-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="de209-316">Quiet</span><span class="sxs-lookup"><span data-stu-id="de209-316">Quiet</span></span>|<span data-ttu-id="de209-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="de209-317">/quiet</span></span>|<span data-ttu-id="de209-318">Ja</span><span class="sxs-lookup"><span data-stu-id="de209-318">Yes</span></span>|<span data-ttu-id="de209-319">Het installatieprogramma wordt uitgevoerd zonder dat de UI of prompts worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de209-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="de209-320">NoRestart</span><span class="sxs-lookup"><span data-stu-id="de209-320">NoRestart</span></span>|<span data-ttu-id="de209-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="de209-321">/norestart</span></span>|<span data-ttu-id="de209-322">Nee</span><span class="sxs-lookup"><span data-stu-id="de209-322">No</span></span>|<span data-ttu-id="de209-323">Onderdrukt elke poging tot herstarten.</span><span class="sxs-lookup"><span data-stu-id="de209-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="de209-324">De UI geeft standaard een prompt vóór de herstart.</span><span class="sxs-lookup"><span data-stu-id="de209-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="de209-325">Help</span><span class="sxs-lookup"><span data-stu-id="de209-325">Help</span></span>|<span data-ttu-id="de209-326">/help</span><span class="sxs-lookup"><span data-stu-id="de209-326">/help</span></span>|<span data-ttu-id="de209-327">Nee</span><span class="sxs-lookup"><span data-stu-id="de209-327">No</span></span>|<span data-ttu-id="de209-328">Biedt hulp- en naslaginformatie.</span><span class="sxs-lookup"><span data-stu-id="de209-328">Provides help and quick reference.</span></span> <span data-ttu-id="de209-329">Geeft het juiste gebruik van de setup-opdracht weer, samen met een overzicht van alle opties en alle gedrag.</span><span class="sxs-lookup"><span data-stu-id="de209-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="de209-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="de209-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de209-331">Dit werkt alleen op de site docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="de209-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="de209-332">Er kunnen soms hele lange woorden in de tweede kolom van een tabel staan.</span><span class="sxs-lookup"><span data-stu-id="de209-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="de209-333">Om ervoor te zorgen dat lange woorden netjes worden gesplitst, kunt u de klasse `mx-tdCol2BreakAll` toepassen met behulp van de `div`-wrapper-syntaxis zoals eerder besproken.</span><span class="sxs-lookup"><span data-stu-id="de209-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="de209-334">HTML-tabellen</span><span class="sxs-lookup"><span data-stu-id="de209-334">HTML Tables</span></span>

<span data-ttu-id="de209-335">HTML-tabellen worden niet aanbevolen voor docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="de209-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="de209-336">Ze kunnen niet door mensen worden gelezen in de bron. Dit is wel een basisprincipe van Markdown.</span><span class="sxs-lookup"><span data-stu-id="de209-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="de209-337">Video's</span><span class="sxs-lookup"><span data-stu-id="de209-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="de209-338">Video's insluiten op een Markdown-pagina</span><span class="sxs-lookup"><span data-stu-id="de209-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="de209-339">Momenteel biedt OPS ondersteuning voor video's die zijn gepubliceerd op een van de volgende drie locaties:</span><span class="sxs-lookup"><span data-stu-id="de209-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="de209-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="de209-340">YouTube</span></span>
- <span data-ttu-id="de209-341">Channel 9</span><span class="sxs-lookup"><span data-stu-id="de209-341">Channel 9</span></span>
- <span data-ttu-id="de209-342">Het eigen One Player-systeem van Microsoft</span><span class="sxs-lookup"><span data-stu-id="de209-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="de209-343">U kunt een video insluiten met de volgende syntaxis zodat OPS de video kan renderen.</span><span class="sxs-lookup"><span data-stu-id="de209-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="de209-344">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="de209-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="de209-345">... wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="de209-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="de209-346">En deze wordt als volgt weergegeven op gepubliceerde pagina's:</span><span class="sxs-lookup"><span data-stu-id="de209-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="de209-347">De URL van de CH9-video moet beginnen met `https` en eindigen met `/player`.</span><span class="sxs-lookup"><span data-stu-id="de209-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="de209-348">Anders wordt de hele pagina en niet alleen de video ingesloten.</span><span class="sxs-lookup"><span data-stu-id="de209-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="de209-349">Nieuwe video's uploaden</span><span class="sxs-lookup"><span data-stu-id="de209-349">Uploading new videos</span></span>

<span data-ttu-id="de209-350">Alle nieuwe video's moeten worden geüpload met het volgende proces:</span><span class="sxs-lookup"><span data-stu-id="de209-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="de209-351">Neem deel aan de groep **docs_video_users** op IDWEB.</span><span class="sxs-lookup"><span data-stu-id="de209-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="de209-352">Ga naar https://aka.ms/VideoUploadRequest en vul de gegevens voor uw video in.</span><span class="sxs-lookup"><span data-stu-id="de209-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="de209-353">Het volgende is nodig (geen van deze items is zichtbaar voor het publiek):</span><span class="sxs-lookup"><span data-stu-id="de209-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="de209-354">Een titel voor uw video.</span><span class="sxs-lookup"><span data-stu-id="de209-354">A title for your video.</span></span>
    1. <span data-ttu-id="de209-355">Een lijst met producten/services waarop uw video betrekking heeft.</span><span class="sxs-lookup"><span data-stu-id="de209-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="de209-356">De doelpagina of (als u de pagina nog niet hebt) de docset waarop uw video wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="de209-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="de209-357">Een koppeling naar het MP4-bestand voor uw video (als u geen locatie hebt waar het bestand kan worden geplaatst, kunt u het tijdelijk hier plaatsen:   `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="de209-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="de209-358">MP4-bestanden moeten 720p of hoger zijn.</span><span class="sxs-lookup"><span data-stu-id="de209-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="de209-359">Een beschrijving van de video.</span><span class="sxs-lookup"><span data-stu-id="de209-359">A description of the video.</span></span>
1. <span data-ttu-id="de209-360">Verzend dat item (sla het op).</span><span class="sxs-lookup"><span data-stu-id="de209-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="de209-361">De video wordt binnen twee werkdagen geüpload.</span><span class="sxs-lookup"><span data-stu-id="de209-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="de209-362">De koppeling die u voor het insluiten nodig hebt, wordt in het werkitem geplaatst en deze wordt *terug naar u* omgezet.</span><span class="sxs-lookup"><span data-stu-id="de209-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="de209-363">Nadat u de videokoppeling hebt vastgelegd, sluit u het werkitem.</span><span class="sxs-lookup"><span data-stu-id="de209-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="de209-364">De videokoppeling kan vervolgens aan uw bericht worden toegevoegd met deze syntaxis:</span><span class="sxs-lookup"><span data-stu-id="de209-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
