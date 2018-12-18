---
title: Markdown-naslaginformatie voor docs.microsoft.com
description: De Docs platformhandleiding voor Markdown.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 1023f3036e5c1facd0bcd4c31069e6faf3c95483
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245867"
---
# <a name="markdown-reference"></a><span data-ttu-id="d7db5-103">Markdown-naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="d7db5-103">Markdown Reference</span></span>

<span data-ttu-id="d7db5-104">Markdown is een lichtgewicht opmaakcodetaal met een syntaxis voor het opmaken van platte tekst.</span><span class="sxs-lookup"><span data-stu-id="d7db5-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="d7db5-105">Het Docs-platform ondersteunt de CommonMark-standaard voor Markdown, plus enkele aangepaste Markdown-extensies die zijn ontworpen om rijkere inhoud op docs.microsoft.com te bieden.</span><span class="sxs-lookup"><span data-stu-id="d7db5-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="d7db5-106">Dit artikel bevat alfabetische naslaginformatie voor het gebruik van Markdown voor docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d7db5-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="d7db5-107">U kunt voor het opstellen van Markdown elke teksteditor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="d7db5-108">Voor elke editor die het invoegen van zowel standaard-Markdown-syntaxis als aangepaste Docs-extensies mogelijk maakt, wordt [VS Code](https://code.visualstudio.com/) met een geïnstalleerd [Docs-ontwerppakket](https://aka.ms/DocsAuthoringPack) aangeraden.</span><span class="sxs-lookup"><span data-stu-id="d7db5-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="d7db5-109">Docs maakt gebruik van de Markdown-engine in Markdig.</span><span class="sxs-lookup"><span data-stu-id="d7db5-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="d7db5-110">U kunt het weergeven van Markdown in Markdig versus andere engines testen op [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="d7db5-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="d7db5-111">Waarschuwingen (Opmerking, Tip, Belangrijk, Let op, Waarschuwing)</span><span class="sxs-lookup"><span data-stu-id="d7db5-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="d7db5-112">Geeft een waarschuwing voor een Docs Markdown-extensie om blokcitaten te maken die op docs.microsoft.com worden weergegeven met kleuren en pictogrammen die het belang van de inhoud aanduiden.</span><span class="sxs-lookup"><span data-stu-id="d7db5-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="d7db5-113">De volgende typen waarschuwingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="d7db5-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="d7db5-114">Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="d7db5-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="d7db5-115">Informatie die de gebruiker ook bij globaal scannen moet zien.</span><span class="sxs-lookup"><span data-stu-id="d7db5-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="d7db5-116">Optionele informatie waarmee een gebruiker meer succes zal hebben.</span><span class="sxs-lookup"><span data-stu-id="d7db5-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7db5-117">Informatie die essentieel voor de gebruiker is om succes te hebben.</span><span class="sxs-lookup"><span data-stu-id="d7db5-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="d7db5-118">Mogelijke negatieve gevolgen van een actie.</span><span class="sxs-lookup"><span data-stu-id="d7db5-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="d7db5-119">Bepaalde gevaarlijke gevolgen van een actie.</span><span class="sxs-lookup"><span data-stu-id="d7db5-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="d7db5-120">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="d7db5-120">Code snippets</span></span>

<span data-ttu-id="d7db5-121">U kunt codefragmenten in uw Markdown-bestanden insluiten:</span><span class="sxs-lookup"><span data-stu-id="d7db5-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="d7db5-122">Koppen</span><span class="sxs-lookup"><span data-stu-id="d7db5-122">Headings</span></span>

<span data-ttu-id="d7db5-123">Docs ondersteunt zes niveaus Markdown-koppen:</span><span class="sxs-lookup"><span data-stu-id="d7db5-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="d7db5-124">Tussen de laatste `#` en de koptekst moet een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="d7db5-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="d7db5-125">Elk Markdown-bestand moet precies één H1 hebben.</span><span class="sxs-lookup"><span data-stu-id="d7db5-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="d7db5-126">De H1 moet de eerste inhoud in het bestand zijn na het YML-blok met metagegevens.</span><span class="sxs-lookup"><span data-stu-id="d7db5-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="d7db5-127">H2's verschijnen automatisch in het navigatiemenu aan de rechterkant van het gepubliceerde bestand.</span><span class="sxs-lookup"><span data-stu-id="d7db5-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="d7db5-128">Dit geldt niet voor koppen op een lager niveau. Gebruik H2's dus strategisch om lezers te helpen door uw inhoud te navigeren.</span><span class="sxs-lookup"><span data-stu-id="d7db5-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="d7db5-129">HMTL-koppen, zoals `<h1>`, worden niet aanbevolen en leiden in sommige gevallen tot compileerwaarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="d7db5-130">U kunt de afzonderlijke koppen in een bestand koppelen via [bladwijzers](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="d7db5-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="d7db5-131">HTML</span><span class="sxs-lookup"><span data-stu-id="d7db5-131">HTML</span></span>

<span data-ttu-id="d7db5-132">Hoewel Markdown ondersteuning biedt voor inline-HTML, wordt HTML niet aanbevolen voor het publiceren naar Docs. Bovendien leidt dit, behalve bij een beperkte lijst met waarden, tot compileerfouten of -waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="d7db5-133">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="d7db5-133">Images</span></span>

<span data-ttu-id="d7db5-134">De syntaxis voor het insluiten van een afbeelding is:</span><span class="sxs-lookup"><span data-stu-id="d7db5-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="d7db5-135">Hierbij is `alt text` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="d7db5-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="d7db5-136">Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig.</span><span class="sxs-lookup"><span data-stu-id="d7db5-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="d7db5-137">Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.</span><span class="sxs-lookup"><span data-stu-id="d7db5-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="d7db5-138">Afbeeldingen moeten worden opgeslagen in een `/media`-map in uw docset.</span><span class="sxs-lookup"><span data-stu-id="d7db5-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="d7db5-139">De volgende bestandstypen worden standaard voor afbeeldingen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="d7db5-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="d7db5-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="d7db5-140">.jpg</span></span>
- <span data-ttu-id="d7db5-141">.png</span><span class="sxs-lookup"><span data-stu-id="d7db5-141">.png</span></span>

<span data-ttu-id="d7db5-142">U kunt ook ondersteuning voor andere typen afbeeldingen toevoegen door deze toe te voegen als resources aan het docfx.json-bestand<!--add link to reference when available--> voor uw docset.</span><span class="sxs-lookup"><span data-stu-id="d7db5-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="d7db5-143">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="d7db5-143">Links</span></span>

<span data-ttu-id="d7db5-144">In de meeste gevallen gebruikt Docs standaard-Markdown-koppelingen naar andere bestanden en pagina's.</span><span class="sxs-lookup"><span data-stu-id="d7db5-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="d7db5-145">De typen koppelingen worden in de onderstaande subsecties beschreven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="d7db5-146">Het Docs-ontwerppakket voor VS Code kan helpen relatieve koppelingen en bladwijzers correct in te voegen zonder dat u zich met paden bezig hoeft te houden.</span><span class="sxs-lookup"><span data-stu-id="d7db5-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7db5-147">Neem geen codes voor landinstellingen, zoals nl-nl, in uw koppelingen naar Microsoft-sites op.</span><span class="sxs-lookup"><span data-stu-id="d7db5-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="d7db5-148">Landinstellingscodes die in code zijn vastgelegd verhinderen dat gelokaliseerde inhoud wordt weergegeven. Dit leidt tot een slechte klantervaring voor gebruikers in andere regio's en brengt aanzienlijke lokalisatiekosten met zich mee.</span><span class="sxs-lookup"><span data-stu-id="d7db5-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="d7db5-149">Wanneer u een URL uit een browser kopieert, wordt de landinstellingscode standaard opgenomen. U moet deze handmatig dus verwijderen wanneer u een koppeling maakt.</span><span class="sxs-lookup"><span data-stu-id="d7db5-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="d7db5-150">Gebruik bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="d7db5-151">Niet:</span><span class="sxs-lookup"><span data-stu-id="d7db5-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="d7db5-152">Relatieve koppelingen naar bestanden in dezelfde docset</span><span class="sxs-lookup"><span data-stu-id="d7db5-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="d7db5-153">Een relatief pad is het pad naar het doelbestand ten opzichte van het huidige bestand.</span><span class="sxs-lookup"><span data-stu-id="d7db5-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="d7db5-154">U kunt in Docs een relatief pad gebruiken om een koppeling naar ander bestand in dezelfde docset te maken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="d7db5-155">De syntaxis voor een relatief pad ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="d7db5-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="d7db5-156">Hierbij duidt `../` één niveau hoger in de hiërarchie aan.</span><span class="sxs-lookup"><span data-stu-id="d7db5-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="d7db5-157">Het relatieve pad wordt tijdens het compileren omgezet, met inbegrip van het verwijderen van de MD-extensie.</span><span class="sxs-lookup"><span data-stu-id="d7db5-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="d7db5-158">U kunt ../ gebruiken om het bestand te koppelen aan een bestand in de bovenliggende map, maar dat bestand moet dan wel in dezelfde docset aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="d7db5-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="d7db5-159">U kunt ../ niet gebruiken om een bestand te koppelen aan een bestand in een andere docset-map.</span><span class="sxs-lookup"><span data-stu-id="d7db5-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="d7db5-160">Docs ondersteunt ook een speciale vorm van een relatief pad. Deze vorm begint met het teken ~ (bijvoorbeeld ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="d7db5-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="d7db5-161">Met deze syntaxis wordt een bestand ten opzichte van de hoofdmap van een docset aangegeven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="d7db5-162">Ook dit type pad wordt tijdens de build gevalideerd en omgezet.</span><span class="sxs-lookup"><span data-stu-id="d7db5-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7db5-163">Neem de bestandsextensie in het relatieve pad op.</span><span class="sxs-lookup"><span data-stu-id="d7db5-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="d7db5-164">Bij het compileren wordt het bestaan van het doelbestand van dat relatieve pad gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="d7db5-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="d7db5-165">Als het relatieve pad geen bestandsextensie bevat, wordt bij het compileren waarschijnlijk een waarschuwing of verbroken koppeling gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="d7db5-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="d7db5-166">Gebruik bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="d7db5-167">Niet:</span><span class="sxs-lookup"><span data-stu-id="d7db5-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="d7db5-168">Sitegerelateerde koppelingen naar andere bestanden in Docs</span><span class="sxs-lookup"><span data-stu-id="d7db5-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="d7db5-169">Neem de bestandsextensie (.md) niet op.</span><span class="sxs-lookup"><span data-stu-id="d7db5-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="d7db5-170">Deze koppelt naar het Linux-overzichtsbestand van buiten de Azure-docset 'articles'.</span><span class="sxs-lookup"><span data-stu-id="d7db5-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="d7db5-171">Koppelingen naar externe sites</span><span class="sxs-lookup"><span data-stu-id="d7db5-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="d7db5-172">Op URL gebaseerde koppeling naar een andere webpagina (moet https:// bevatten).</span><span class="sxs-lookup"><span data-stu-id="d7db5-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="d7db5-173">Bladwijzerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="d7db5-173">Bookmark links</span></span>

<span data-ttu-id="d7db5-174">Bladwijzerkoppeling naar een kop in een ander bestand in dezelfde opslagplaats:</span><span class="sxs-lookup"><span data-stu-id="d7db5-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="d7db5-175">Bladwijzerkoppeling naar een kop in het huidige bestand:</span><span class="sxs-lookup"><span data-stu-id="d7db5-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="d7db5-176">Gebruik een hash-code gevolgd door de woorden van de kop zonder leestekens en met streepjes als vervanging voor spaties.</span><span class="sxs-lookup"><span data-stu-id="d7db5-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="d7db5-177">Expliciete ankerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="d7db5-177">Explicit anchor links</span></span>

<span data-ttu-id="d7db5-178">Expliciete ankerkoppelingen die de `<a>`-HTML-tag gebruiken worden **niet vereist of aanbevolen** behalve in hub- en landingspagina's.</span><span class="sxs-lookup"><span data-stu-id="d7db5-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="d7db5-179">Gebruik in algemene Markdown-bestanden bladwijzers zoals hierboven wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="d7db5-180">Gebruik als volgt ankers voor hub- en landingspagina's:</span><span class="sxs-lookup"><span data-stu-id="d7db5-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="d7db5-181">`## <a id="AnchorText"> </a>Header text` of `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="d7db5-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="d7db5-182">Gebruik de volgende syntaxis om een koppeling naar expliciete ankers te maken:</span><span class="sxs-lookup"><span data-stu-id="d7db5-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="d7db5-183">XREF-koppelingen (kruisverwijzing)</span><span class="sxs-lookup"><span data-stu-id="d7db5-183">XREF (cross reference) links</span></span>

<span data-ttu-id="d7db5-184">Als u in de huidige docset of andere docsets een koppeling wilt maken naar automatisch gegenereerde pagina's met API-naslaginformatie, gebruikt u XREF-koppelingen met de unieke id (UID).</span><span class="sxs-lookup"><span data-stu-id="d7db5-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="d7db5-185">Als u wilt verwijzen naar pagina's met API-naslaginformatie in andere docsets, moet u `xrefService`-configuratie in het `docfx.json`-bestand toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="d7db5-186">De UID is gelijk aan de volledig gekwalificeerde naam van de klasse en het lid.</span><span class="sxs-lookup"><span data-stu-id="d7db5-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="d7db5-187">Als u een \* toevoegt na de UID, vertegenwoordigt de koppeling een overbelastingspagina en niet een specifieke API.</span><span class="sxs-lookup"><span data-stu-id="d7db5-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="d7db5-188">Gebruik bijvoorbeeld `List<T>.BinarySearch*` om een koppeling naar de pagina BinarySearch Method te maken in plaats van te koppelen naar een specifieke overbelasting zoals `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="d7db5-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="d7db5-189">Voor de syntaxis hebt u de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="d7db5-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="d7db5-190">Automatisch koppelen: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="d7db5-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="d7db5-191">De optionele queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst.</span><span class="sxs-lookup"><span data-stu-id="d7db5-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="d7db5-192">Standaard toont de koppelingstekst alleen de naam van het lid of het type.</span><span class="sxs-lookup"><span data-stu-id="d7db5-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="d7db5-193">Markdown-koppeling: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="d7db5-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="d7db5-194">Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="d7db5-195">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="d7db5-195">Examples:</span></span>

- <span data-ttu-id="d7db5-196">`<xref:System.String>` wordt weergegeven als String.</span><span class="sxs-lookup"><span data-stu-id="d7db5-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="d7db5-197">`<xref:System.String?displayProperty=nameWithType>` wordt weergegeven als System.String.</span><span class="sxs-lookup"><span data-stu-id="d7db5-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="d7db5-198">`[String class](xref:System.String)` wordt weergeven als String class.</span><span class="sxs-lookup"><span data-stu-id="d7db5-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="d7db5-199">Momenteel is er geen eenvoudige manier om de UID's te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="d7db5-200"><!-- ? -->De beste manier om de UID voor een API te zoeken, is om de bron van de API-pagina waaraan u wilt koppelen te bekijken en de waarde ms.assetid te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="d7db5-201">Afzonderlijke overbelastingswaarden worden in de bron niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="d7db5-202">We werken aan een beter systeem voor de toekomst.</span><span class="sxs-lookup"><span data-stu-id="d7db5-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="d7db5-203">Wanneer de UID de speciale tekens \`, \# of \* bevat, moet de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML worden gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="d7db5-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="d7db5-204">U ziet soms haakjes in de code, maar dat is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="d7db5-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="d7db5-205">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="d7db5-205">Examples:</span></span>

- <span data-ttu-id="d7db5-206">System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="d7db5-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="d7db5-207">System.Exception. \#ctor wordt `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="d7db5-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="d7db5-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="d7db5-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="d7db5-209">Lijsten (Genummerd, Met opsommingstekens, Controlelijst)</span><span class="sxs-lookup"><span data-stu-id="d7db5-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="d7db5-210">Genummerde lijst</span><span class="sxs-lookup"><span data-stu-id="d7db5-210">Numbered list</span></span>

<span data-ttu-id="d7db5-211">Als u een genummerde lijst wilt maken, kunt u alle 1's gebruiken. Deze worden bij het publiceren weergegeven als een sequentiële lijst.</span><span class="sxs-lookup"><span data-stu-id="d7db5-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="d7db5-212">Voor betere leesbaarheid van de bron kunt u uw lijsten verhogen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="d7db5-213">Gebruik geen letters in lijsten, ook niet in geneste lijsten.</span><span class="sxs-lookup"><span data-stu-id="d7db5-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="d7db5-214">Deze worden bij het publiceren naar Docs niet goed weergegeven. Geneste lijsten die gebruikmaken van nummers, worden bij het publiceren weergegeven als kleine letters.</span><span class="sxs-lookup"><span data-stu-id="d7db5-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="d7db5-215">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="d7db5-216">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-216">This renders as follows:</span></span>

1. <span data-ttu-id="d7db5-217">Dit is</span><span class="sxs-lookup"><span data-stu-id="d7db5-217">This is</span></span>
1. <span data-ttu-id="d7db5-218">een bovenliggende lijst met nummers</span><span class="sxs-lookup"><span data-stu-id="d7db5-218">a parent numbered list</span></span>
   1. <span data-ttu-id="d7db5-219">en dit is</span><span class="sxs-lookup"><span data-stu-id="d7db5-219">and this is</span></span>
   1. <span data-ttu-id="d7db5-220">een geneste lijst met nummers</span><span class="sxs-lookup"><span data-stu-id="d7db5-220">a nested numbered list</span></span>
1. <span data-ttu-id="d7db5-221">(einde)</span><span class="sxs-lookup"><span data-stu-id="d7db5-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="d7db5-222">Lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="d7db5-222">Bulleted list</span></span>

<span data-ttu-id="d7db5-223">Als u een lijst met opsommingstekens wilt maken, gebruikt u `-` gevolgd door een spatie aan het begin van elke regel:</span><span class="sxs-lookup"><span data-stu-id="d7db5-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="d7db5-224">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-224">This renders as follows:</span></span>

- <span data-ttu-id="d7db5-225">Dit is</span><span class="sxs-lookup"><span data-stu-id="d7db5-225">This is</span></span>
- <span data-ttu-id="d7db5-226">een bovenliggende lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="d7db5-226">a parent bulleted list</span></span>
  - <span data-ttu-id="d7db5-227">en dit is</span><span class="sxs-lookup"><span data-stu-id="d7db5-227">and this is</span></span>
  - <span data-ttu-id="d7db5-228">een geneste lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="d7db5-228">a nested bulleted list</span></span>
- <span data-ttu-id="d7db5-229">Klaar!</span><span class="sxs-lookup"><span data-stu-id="d7db5-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="d7db5-230">Controlelijst</span><span class="sxs-lookup"><span data-stu-id="d7db5-230">Checklist</span></span>

<span data-ttu-id="d7db5-231">Controlelijsten zijn beschikbaar voor gebruik op (alleen) docs.microsoft.com via een aangepaste Markdown-extensie:</span><span class="sxs-lookup"><span data-stu-id="d7db5-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="d7db5-232">Dit voorbeeld wordt op docs.microsoft.com weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d7db5-233">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="d7db5-233">List item 1</span></span>
> * <span data-ttu-id="d7db5-234">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="d7db5-234">List item 2</span></span>
> * <span data-ttu-id="d7db5-235">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="d7db5-235">List item 3</span></span>

<span data-ttu-id="d7db5-236">Gebruik controlelijsten aan het begin of eind van een artikel om inhoud voor 'Wat gaat u leren' of 'Wat hebt u geleerd' samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="d7db5-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="d7db5-237">Voeg geen willekeurige controlelijsten ergens anders in een artikel toe.</span><span class="sxs-lookup"><span data-stu-id="d7db5-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="d7db5-238">Actie volgende stap</span><span class="sxs-lookup"><span data-stu-id="d7db5-238">Next step action</span></span>

<span data-ttu-id="d7db5-239">U kunt een aangepaste extensie gebruiken om een knop voor de actie van de volgende stap toe te voegen aan pagina's op (alleen) docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d7db5-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="d7db5-240">De syntaxis ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="d7db5-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="d7db5-241">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="d7db5-242">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d7db5-243">Informatie over de basisstijl</span><span class="sxs-lookup"><span data-stu-id="d7db5-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="d7db5-244">U kunt elke ondersteunde koppeling in een volgende stapactie gebruiken, met inbegrip van een Markdown-koppeling naar een andere webpagina.</span><span class="sxs-lookup"><span data-stu-id="d7db5-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="d7db5-245">In de meeste gevallen is de koppeling voor de volgende actie een relatieve koppeling naar een ander bestand in dezelfde docset.</span><span class="sxs-lookup"><span data-stu-id="d7db5-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="d7db5-246">Sectiedefinitie</span><span class="sxs-lookup"><span data-stu-id="d7db5-246">Section definition</span></span>

<span data-ttu-id="d7db5-247"><!-- more info about this would be helpful! --> U moet mogelijk een sectie definiëren.</span><span class="sxs-lookup"><span data-stu-id="d7db5-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="d7db5-248">Deze syntaxis wordt voornamelijk gebruikt voor codetabellen.</span><span class="sxs-lookup"><span data-stu-id="d7db5-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="d7db5-249">Zie het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="d7db5-250">De eraan voorafgaande blockquote-Markdown-tekst wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="d7db5-251">Selectors</span><span class="sxs-lookup"><span data-stu-id="d7db5-251">Selectors</span></span>

<span data-ttu-id="d7db5-252"><!-- could be more clear! --> U kunt een selector gebruiken wanneer u verschillende pagina's voor hetzelfde artikel met elkaar wilt verbinden.</span><span class="sxs-lookup"><span data-stu-id="d7db5-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="d7db5-253">Lezers kunnen dan schakelen tussen die pagina's.</span><span class="sxs-lookup"><span data-stu-id="d7db5-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d7db5-254">Deze extensie werkt anders tussen docs.microsoft.com en MSDN.</span><span class="sxs-lookup"><span data-stu-id="d7db5-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="d7db5-255">Single selector</span><span class="sxs-lookup"><span data-stu-id="d7db5-255">Single selector</span></span>

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

<span data-ttu-id="d7db5-256">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d7db5-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="d7db5-265">Multi-selector</span><span class="sxs-lookup"><span data-stu-id="d7db5-265">Multi-selector</span></span>

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

<span data-ttu-id="d7db5-266">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d7db5-266">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="d7db5-277">Tabellen</span><span class="sxs-lookup"><span data-stu-id="d7db5-277">Tables</span></span>

<span data-ttu-id="d7db5-278">De eenvoudigste manier om een tabel in Markdown te maken is gebruik te maken van pipes en regels.</span><span class="sxs-lookup"><span data-stu-id="d7db5-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="d7db5-279">Als u een standaardtabel met een kop wilt maken, laat u de eerste regel volgen door een stippellijn:</span><span class="sxs-lookup"><span data-stu-id="d7db5-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="d7db5-280">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-280">This renders as follows:</span></span>

|<span data-ttu-id="d7db5-281">Dit is</span><span class="sxs-lookup"><span data-stu-id="d7db5-281">This is</span></span>   |<span data-ttu-id="d7db5-282">een eenvoudige</span><span class="sxs-lookup"><span data-stu-id="d7db5-282">a simple</span></span>   |<span data-ttu-id="d7db5-283">tabelkop</span><span class="sxs-lookup"><span data-stu-id="d7db5-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="d7db5-284">tabel</span><span class="sxs-lookup"><span data-stu-id="d7db5-284">table</span></span>     |<span data-ttu-id="d7db5-285">gegevens</span><span class="sxs-lookup"><span data-stu-id="d7db5-285">data</span></span>       |<span data-ttu-id="d7db5-286">hier</span><span class="sxs-lookup"><span data-stu-id="d7db5-286">here</span></span>        |
|<span data-ttu-id="d7db5-287">deze hoeft niet</span><span class="sxs-lookup"><span data-stu-id="d7db5-287">it doesn't</span></span>|<span data-ttu-id="d7db5-288">precies</span><span class="sxs-lookup"><span data-stu-id="d7db5-288">actually</span></span>   |<span data-ttu-id="d7db5-289">te zijn uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="d7db5-289">have to line up nicely!</span></span>||

<span data-ttu-id="d7db5-290">U kunt ook een tabel zonder kop maken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-290">You can also create a table without a header.</span></span> <span data-ttu-id="d7db5-291">Ga bijvoorbeeld als volgt te werk om een lijst met meerdere kolommen te maken:</span><span class="sxs-lookup"><span data-stu-id="d7db5-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="d7db5-292">Dit wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d7db5-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="d7db5-293">Deze</span><span class="sxs-lookup"><span data-stu-id="d7db5-293">This</span></span> | <span data-ttu-id="d7db5-294">tabel</span><span class="sxs-lookup"><span data-stu-id="d7db5-294">table</span></span> |
| <span data-ttu-id="d7db5-295">heeft geen</span><span class="sxs-lookup"><span data-stu-id="d7db5-295">has no</span></span> | <span data-ttu-id="d7db5-296">kop</span><span class="sxs-lookup"><span data-stu-id="d7db5-296">header</span></span> |

<span data-ttu-id="d7db5-297">U kunt de kolommen uitlijnen met behulp van dubbele punten:</span><span class="sxs-lookup"><span data-stu-id="d7db5-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="d7db5-298">Wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="d7db5-299">rechts uitgelijnd:</span><span class="sxs-lookup"><span data-stu-id="d7db5-299">right aligned:</span></span>|
|<span data-ttu-id="d7db5-300">:links uitgelijnd</span><span class="sxs-lookup"><span data-stu-id="d7db5-300">:left aligned</span></span>     |
|<span data-ttu-id="d7db5-301">:gecentreerd        :</span><span class="sxs-lookup"><span data-stu-id="d7db5-301">:centered        :</span></span>|

> [!TIP]
> U kunt met Docs Authoring Extension voor VS Code gemakkelijk basis-Markdown-tabellen toevoegen.
>
> U kunt ook een [onlinegenerator voor tabellen](http://www.tablesgenerator.com/markdown_tables) gebruiken.

### <a name="mx-tdbreakall"></a><span data-ttu-id="d7db5-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="d7db5-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Dit werkt alleen op de site docs.microsoft.com.

<span data-ttu-id="d7db5-306">Als u een tabel in Markdown maakt, kan de tabel worden uitgebreid naar het navigatievenster rechts, waardoor de tabel onleesbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="d7db5-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="d7db5-307">Dat is op te lossen door bij het renderen van Docs de tabel op te splitsen wanneer dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="d7db5-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="d7db5-308">U laat eenvoudig de tabel teruglopen met de aangepaste klasse `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="d7db5-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="d7db5-309">Hier ziet u een Markdown-voorbeeld van een tabel met drie rijen die teruglopen door gebruik te maken van een `div` met de klassenaam `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="d7db5-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="d7db5-310">Deze wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d7db5-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="d7db5-311">Naam</span><span class="sxs-lookup"><span data-stu-id="d7db5-311">Name</span></span>|<span data-ttu-id="d7db5-312">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d7db5-312">Syntax</span></span>|<span data-ttu-id="d7db5-313">Verplicht voor installatie op de achtergrond?</span><span class="sxs-lookup"><span data-stu-id="d7db5-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="d7db5-314">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d7db5-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="d7db5-315">Quiet</span><span class="sxs-lookup"><span data-stu-id="d7db5-315">Quiet</span></span>|<span data-ttu-id="d7db5-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="d7db5-316">/quiet</span></span>|<span data-ttu-id="d7db5-317">Ja</span><span class="sxs-lookup"><span data-stu-id="d7db5-317">Yes</span></span>|<span data-ttu-id="d7db5-318">Het installatieprogramma wordt uitgevoerd zonder dat de UI of prompts worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="d7db5-319">NoRestart</span><span class="sxs-lookup"><span data-stu-id="d7db5-319">NoRestart</span></span>|<span data-ttu-id="d7db5-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="d7db5-320">/norestart</span></span>|<span data-ttu-id="d7db5-321">Nee</span><span class="sxs-lookup"><span data-stu-id="d7db5-321">No</span></span>|<span data-ttu-id="d7db5-322">Onderdrukt elke poging tot herstarten.</span><span class="sxs-lookup"><span data-stu-id="d7db5-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="d7db5-323">De UI geeft standaard een prompt vóór de herstart.</span><span class="sxs-lookup"><span data-stu-id="d7db5-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="d7db5-324">Help</span><span class="sxs-lookup"><span data-stu-id="d7db5-324">Help</span></span>|<span data-ttu-id="d7db5-325">/help</span><span class="sxs-lookup"><span data-stu-id="d7db5-325">/help</span></span>|<span data-ttu-id="d7db5-326">Nee</span><span class="sxs-lookup"><span data-stu-id="d7db5-326">No</span></span>|<span data-ttu-id="d7db5-327">Biedt hulp- en naslaginformatie.</span><span class="sxs-lookup"><span data-stu-id="d7db5-327">Provides help and quick reference.</span></span> <span data-ttu-id="d7db5-328">Geeft het juiste gebruik van de setup-opdracht weer, samen met een overzicht van alle opties en alle gedrag.</span><span class="sxs-lookup"><span data-stu-id="d7db5-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="d7db5-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="d7db5-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7db5-330">Dit werkt alleen op de site docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d7db5-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="d7db5-331">Er kunnen soms hele lange woorden in de tweede kolom van een tabel staan.</span><span class="sxs-lookup"><span data-stu-id="d7db5-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="d7db5-332">Om ervoor te zorgen dat lange woorden netjes worden gesplitst, kunt u de klasse `mx-tdCol2BreakAll` toepassen met behulp van de `div`-wrapper-syntaxis zoals eerder besproken.</span><span class="sxs-lookup"><span data-stu-id="d7db5-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="d7db5-333">HTML-tabellen</span><span class="sxs-lookup"><span data-stu-id="d7db5-333">HTML Tables</span></span>

<span data-ttu-id="d7db5-334">HTML-tabellen worden niet aanbevolen voor docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d7db5-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="d7db5-335">Ze kunnen niet door mensen worden gelezen in de bron. Dit is wel een basisprincipe van Markdown.</span><span class="sxs-lookup"><span data-stu-id="d7db5-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="d7db5-336">Video's</span><span class="sxs-lookup"><span data-stu-id="d7db5-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="d7db5-337">Video's insluiten op een Markdown-pagina</span><span class="sxs-lookup"><span data-stu-id="d7db5-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="d7db5-338">Momenteel biedt Docs ondersteuning voor video's die zijn gepubliceerd op een van de volgende drie locaties:</span><span class="sxs-lookup"><span data-stu-id="d7db5-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="d7db5-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="d7db5-339">YouTube</span></span>
- <span data-ttu-id="d7db5-340">Channel 9</span><span class="sxs-lookup"><span data-stu-id="d7db5-340">Channel 9</span></span>
- <span data-ttu-id="d7db5-341">Het eigen One Player-systeem van Microsoft</span><span class="sxs-lookup"><span data-stu-id="d7db5-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="d7db5-342">U kunt een video insluiten met de volgende syntaxis zodat Docs de video kan weergeven.</span><span class="sxs-lookup"><span data-stu-id="d7db5-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="d7db5-343">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d7db5-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="d7db5-344">... wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="d7db5-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="d7db5-345">En deze wordt als volgt weergegeven op gepubliceerde pagina's:</span><span class="sxs-lookup"><span data-stu-id="d7db5-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="d7db5-346">De URL van de CH9-video moet beginnen met `https` en eindigen met `/player`.</span><span class="sxs-lookup"><span data-stu-id="d7db5-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="d7db5-347">Anders wordt de hele pagina en niet alleen de video ingesloten.</span><span class="sxs-lookup"><span data-stu-id="d7db5-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="d7db5-348">Nieuwe video's uploaden</span><span class="sxs-lookup"><span data-stu-id="d7db5-348">Uploading new videos</span></span>

<span data-ttu-id="d7db5-349">Alle nieuwe video's moeten worden geüpload met het volgende proces:</span><span class="sxs-lookup"><span data-stu-id="d7db5-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="d7db5-350">Neem deel aan de groep **docs_video_users** op IDWEB.</span><span class="sxs-lookup"><span data-stu-id="d7db5-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="d7db5-351">Ga naar https://aka.ms/VideoUploadRequest en vul de gegevens voor uw video in.</span><span class="sxs-lookup"><span data-stu-id="d7db5-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="d7db5-352">Het volgende is nodig (geen van deze items is zichtbaar voor het publiek):</span><span class="sxs-lookup"><span data-stu-id="d7db5-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="d7db5-353">Een titel voor uw video.</span><span class="sxs-lookup"><span data-stu-id="d7db5-353">A title for your video.</span></span>
    1. <span data-ttu-id="d7db5-354">Een lijst met producten/services waarop uw video betrekking heeft.</span><span class="sxs-lookup"><span data-stu-id="d7db5-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="d7db5-355">De doelpagina of (als u de pagina nog niet hebt) de docset waarop uw video wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="d7db5-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="d7db5-356">Een koppeling naar het MP4-bestand voor uw video (als u geen locatie hebt waar het bestand kan worden geplaatst, kunt u het tijdelijk hier plaatsen:   `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="d7db5-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="d7db5-357">MP4-bestanden moeten 720p of hoger zijn.</span><span class="sxs-lookup"><span data-stu-id="d7db5-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="d7db5-358">Een beschrijving van de video.</span><span class="sxs-lookup"><span data-stu-id="d7db5-358">A description of the video.</span></span>
1. <span data-ttu-id="d7db5-359">Verzend dat item (sla het op).</span><span class="sxs-lookup"><span data-stu-id="d7db5-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="d7db5-360">De video wordt binnen twee werkdagen geüpload.</span><span class="sxs-lookup"><span data-stu-id="d7db5-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="d7db5-361">De koppeling die u voor het insluiten nodig hebt, wordt in het werkitem geplaatst en deze wordt *terug naar u* omgezet.</span><span class="sxs-lookup"><span data-stu-id="d7db5-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="d7db5-362">Nadat u de videokoppeling hebt vastgelegd, sluit u het werkitem.</span><span class="sxs-lookup"><span data-stu-id="d7db5-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="d7db5-363">De videokoppeling kan vervolgens aan uw bericht worden toegevoegd met deze syntaxis:</span><span class="sxs-lookup"><span data-stu-id="d7db5-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
