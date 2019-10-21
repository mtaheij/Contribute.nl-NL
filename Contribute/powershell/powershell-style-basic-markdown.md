---
title: Sjabloon en spiekbrief voor PowerShell-artikelen
description: Dit artikel bevat een handige sjabloon waarmee u nieuwe artikelen kunt maken voor PowerShell-documenten
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290352"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="73979-103">Markdown-stijlgids voor PowerShell-Docs</span><span class="sxs-lookup"><span data-stu-id="73979-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="73979-104">Dit artikel bevat wat specifieke stijlrichtlijnen voor de PowerShell-Docs-inhoud.</span><span class="sxs-lookup"><span data-stu-id="73979-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="73979-105">Raadpleeg de [stijlgids van Microsoft](https://docs.microsoft.com/style-guide/welcome/) voor hulp bij andere schrijfstijlen.</span><span class="sxs-lookup"><span data-stu-id="73979-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="73979-106">Metagegevens</span><span class="sxs-lookup"><span data-stu-id="73979-106">Metadata</span></span>

<span data-ttu-id="73979-107">Deze sjabloon bevat voorbeelden van Markdown-syntaxis, maar ook aanwijzingen voor het instellen van metagegevens.</span><span class="sxs-lookup"><span data-stu-id="73979-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="73979-108">Wanneer u een Markdown-bestand maakt, dient u de opgenomen sjabloon naar een nieuw bestand te kopiëren, de metagegevens in te vullen zoals hierna is aangegeven en de kop H1 boven de titel van het artikel te zetten.</span><span class="sxs-lookup"><span data-stu-id="73979-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="73979-109">Het vereiste blok met metagegevens bevindt zich in het volgende voorbeeldblok met metagegevens:</span><span class="sxs-lookup"><span data-stu-id="73979-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="73979-110">Tussen de dubbele punt (:) en de waarde van een metagegevenselement **moet** een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="73979-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="73979-111">Dubbele punten in een waarde (zoals een titel) verbreken de metagegevensparser.</span><span class="sxs-lookup"><span data-stu-id="73979-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="73979-112">Omring in dit geval de titel met dubbele aanhalingstekens (bijvoorbeeld `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="73979-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="73979-113">**auteur**: Het veld Auteur moet de **GitHub-gebruikersnaam** van de auteur bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="73979-114">**beschrijving**: Hierin wordt de inhoud van het artikel samengevat.</span><span class="sxs-lookup"><span data-stu-id="73979-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="73979-115">Deze wordt meestal in de pagina met zoekresultaten weergegeven, maar wordt niet gebruikt voor de rangschikking van de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="73979-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="73979-116">De lengte dient 115 tot 145 tekens te bedragen, inclusief spaties.</span><span class="sxs-lookup"><span data-stu-id="73979-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="73979-117">**ms.date**: De datum van de laatste belangrijke update.</span><span class="sxs-lookup"><span data-stu-id="73979-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="73979-118">Werk deze bij voor bestaande artikelen als u het gehele artikel hebt bekeken en bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="73979-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="73979-119">Kleine aanpassingen, zoals typfouten, rechtvaardigen geen update.</span><span class="sxs-lookup"><span data-stu-id="73979-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="73979-120">**titel**: Deze wordt in zoekprogrammaresultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73979-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="73979-121">De titel mag niet identiek zijn aan de titel in uw H1-kop en moet maximaal 60 tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="73979-122">Er zijn andere metagegevens aan elk artikel toegevoegd, maar wij passen gewoonlijk de meeste metagegevenswaarden toe op mapniveau, zoals is opgegeven in **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="73979-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="73979-123">Productterminologie</span><span class="sxs-lookup"><span data-stu-id="73979-123">Product Terminology</span></span>

<span data-ttu-id="73979-124">Er zijn verschillende varianten van PowerShell.</span><span class="sxs-lookup"><span data-stu-id="73979-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="73979-125">Deze tabel bevat een definitie van verschillende termen die worden gebruikt om PowerShell te bespreken.</span><span class="sxs-lookup"><span data-stu-id="73979-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="73979-126">**PowerShell**: Dit is de standaard.</span><span class="sxs-lookup"><span data-stu-id="73979-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="73979-127">PowerShell is het product dat wij aanbieden.</span><span class="sxs-lookup"><span data-stu-id="73979-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="73979-128">De term PowerShell kan worden gebruikt om welke editie van het product dan ook te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="73979-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="73979-129">**PowerShell Core**: PowerShell op basis van .NET Core Common Language Runtime (CoreCLR) voor alle ondersteunde platforms.</span><span class="sxs-lookup"><span data-stu-id="73979-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="73979-130">**Windows PowerShell**: PowerShell op basis van .NET Framework Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="73979-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="73979-131">Windows PowerShell is alleen beschikbaar op Windows. Hiervoor is de volledige CLR van het .NET Framework vereist.</span><span class="sxs-lookup"><span data-stu-id="73979-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="73979-132">Over het algemeen kunnen verwijzingen naar ‘Windows PowerShell’ in documentatie worden vervangen door ‘PowerShell’.</span><span class="sxs-lookup"><span data-stu-id="73979-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="73979-133">‘Windows PowerShell’ moet **niet** worden gewijzigd als specifieke technologie voor Windows wordt besproken.</span><span class="sxs-lookup"><span data-stu-id="73979-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="73979-134">Elementaire Markdown, GFM en speciale tekens</span><span class="sxs-lookup"><span data-stu-id="73979-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="73979-135">U kunt de basisbeginselen van Markdown, GitHub Flavored Markdown (GFM) en OPS-specifieke extensies leren in de algemene artikelen over [Markdown](../how-to-write-use-markdown.md) en [naslaginformatie over Markdown](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="73979-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](../how-to-write-use-markdown.md) and [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="73979-136">Markdown maakt gebruik van speciale tekens, zoals \*, \` en \# voor opmaak.</span><span class="sxs-lookup"><span data-stu-id="73979-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="73979-137">Als u een van deze tekens in uw inhoud wilt opnemen, moet u een van de volgende stappen ondernemen:</span><span class="sxs-lookup"><span data-stu-id="73979-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="73979-138">Plaats een backslash vóór een speciaal teken om deze als escape-teken te gebruiken (bijvoorbeeld `\*` vóór een \*)</span><span class="sxs-lookup"><span data-stu-id="73979-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="73979-139">Gebruik de [HTML-entiteitscode](http://www.ascii.cl/htmlcodes.htm) voor het teken (bijvoorbeeld `&#42;` vóór een &#42;).</span><span class="sxs-lookup"><span data-stu-id="73979-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="73979-140">Markdown-bestanden moeten onbewerkte ASCII-tekst of UTF-8-codering bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="73979-141">Vermijd echter het gebruik van UTF-8-tekens met meerdere bytes.</span><span class="sxs-lookup"><span data-stu-id="73979-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="73979-142">Gebruik in plaats daarvan een HTML-entiteit.</span><span class="sxs-lookup"><span data-stu-id="73979-142">Instead use an HTML entity.</span></span> <span data-ttu-id="73979-143">Gebruik voor de auteursrechtsymbolen bijvoorbeeld `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="73979-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="73979-144">Deze wordt weergegeven als &copy;.</span><span class="sxs-lookup"><span data-stu-id="73979-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="73979-145">Hyperlinks</span><span class="sxs-lookup"><span data-stu-id="73979-145">Hyperlinks</span></span>

- <span data-ttu-id="73979-146">Vermijd het gebruik van pure URL’s.</span><span class="sxs-lookup"><span data-stu-id="73979-146">Avoid using bare URLs.</span></span> <span data-ttu-id="73979-147">Voor koppelingen moet Markdown-syntaxis `[friendlyname](url-or-path)` worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="73979-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="73979-148">Koppelingen moeten een beschrijvende naam hebben, meestal de titel van het onderwerp waarnaar wordt verwezen</span><span class="sxs-lookup"><span data-stu-id="73979-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="73979-149">Alle items in de sectie Verwante koppelingen onderaan moeten een hyperlink bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="73979-150">Gebruik relatieve koppelingen als u verwijst naar andere inhoud die wordt gehost op **docs.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="73979-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="73979-151">Gebruik geen accents graves, vetgedrukte tekst of andere opmaak binnen de haakjes van een hyperlink.</span><span class="sxs-lookup"><span data-stu-id="73979-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="73979-152">Raadpleeg [Koppelingen in documentatie gebruiken](../how-to-write-links.md) voor uitgebreide informatie over het gebruik van koppelingen.</span><span class="sxs-lookup"><span data-stu-id="73979-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="73979-153">Bestandsnamen</span><span class="sxs-lookup"><span data-stu-id="73979-153">Filenames</span></span>

<span data-ttu-id="73979-154">Voor bestandsnamen zijn de volgende regels van toepassing:</span><span class="sxs-lookup"><span data-stu-id="73979-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="73979-155">Bevatten alleen letters, cijfers en afbreekstreepjes.</span><span class="sxs-lookup"><span data-stu-id="73979-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="73979-156">Deze bevatten geen spaties of leestekens.</span><span class="sxs-lookup"><span data-stu-id="73979-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="73979-157">Deze maken gebruik van afbreekstreepjes als scheidingsteken tussen woorden en getallen in de bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="73979-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="73979-158">Gebruik specifieke actieve werkwoorden, zoals ontwikkelen, kopen, maken, problemen oplossen.</span><span class="sxs-lookup"><span data-stu-id="73979-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="73979-159">Geen onvoltooid tegenwoordige tijd.</span><span class="sxs-lookup"><span data-stu-id="73979-159">No -ing words.</span></span>
- <span data-ttu-id="73979-160">Geen kleine woorden: gebruik niet 'een', 'en', 'de', 'in', 'of', 'enz.'</span><span class="sxs-lookup"><span data-stu-id="73979-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="73979-161">De indeling moet Markdown zijn en de bestandsextensie .md.</span><span class="sxs-lookup"><span data-stu-id="73979-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="73979-162">Houd de bestandsnamen redelijk kort.</span><span class="sxs-lookup"><span data-stu-id="73979-162">Keep file names reasonably short.</span></span> <span data-ttu-id="73979-163">Deze maken deel uit van de URL voor uw artikelen.</span><span class="sxs-lookup"><span data-stu-id="73979-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="73979-164">Witregels, spaties en tabs</span><span class="sxs-lookup"><span data-stu-id="73979-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="73979-165">Verwijder dubbele witregels.</span><span class="sxs-lookup"><span data-stu-id="73979-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="73979-166">Meerdere witregels worden in HTML als één witregel weergeven. Meerdere witregels gebruiken heeft dus geen zin.</span><span class="sxs-lookup"><span data-stu-id="73979-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="73979-167">Witregels geven ook het einde van een blok aan in Markdown.</span><span class="sxs-lookup"><span data-stu-id="73979-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="73979-168">Er moet één witregel tussen verschillende typen Markdown-blokken zijn (zoals tussen een alinea en een lijst of koptekst).</span><span class="sxs-lookup"><span data-stu-id="73979-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="73979-169">Spatiegebruik is erg belangrijk in Markdown.</span><span class="sxs-lookup"><span data-stu-id="73979-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="73979-170">Gebruik altijd spaties in plaats van harde tabs.</span><span class="sxs-lookup"><span data-stu-id="73979-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="73979-171">Verwijder extra spaties aan het einde van regels.</span><span class="sxs-lookup"><span data-stu-id="73979-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="73979-172">Titels en koppen</span><span class="sxs-lookup"><span data-stu-id="73979-172">Titles and headings</span></span>

<span data-ttu-id="73979-173">Gebruik alleen [ATX-kopteksten][atx] (kopteksten in #-stijl in plaats van `=`- of `-`-stijl).</span><span class="sxs-lookup"><span data-stu-id="73979-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="73979-174">Gebruik alleen zinnen - alleen eigennamen en de eerste letter van een titel of koptekst moet een hoofdletter krijgen</span><span class="sxs-lookup"><span data-stu-id="73979-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="73979-175">Er moet één spatie zijn tussen de `#` en de eerste letter van de koptekst</span><span class="sxs-lookup"><span data-stu-id="73979-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="73979-176">Kopteksten moeten worden omgeven door één lege regel</span><span class="sxs-lookup"><span data-stu-id="73979-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="73979-177">Slechts één H1 per document</span><span class="sxs-lookup"><span data-stu-id="73979-177">Only one H1 per document</span></span>
- <span data-ttu-id="73979-178">Koptekstniveaus moeten met één worden verhoogd - sla geen niveaus over</span><span class="sxs-lookup"><span data-stu-id="73979-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="73979-179">Gebruik geen accents graves, vetgedrukte tekst of andere opmaak in kopteksten</span><span class="sxs-lookup"><span data-stu-id="73979-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="73979-180">Voor het schema dat door [PlatyPS][platyPS] wordt afgedwongen voor cmdlet-verwijzingen zijn specifieke H2- en H3-koppen vereist.</span><span class="sxs-lookup"><span data-stu-id="73979-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="73979-181">Het toevoegen of verwijderen van kopteksten kan problemen opleveren in de build.</span><span class="sxs-lookup"><span data-stu-id="73979-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="73979-182">Raadpleeg de [stijlgids voor cmdlet-verwijzingen](powershell-style-reference.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="73979-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="73979-183">Beperk de lengte van regels tot 100 tekens</span><span class="sxs-lookup"><span data-stu-id="73979-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="73979-184">Dit vereenvoudigt de opdrachtregeluitvoer voor verschillen en geschiedenis.</span><span class="sxs-lookup"><span data-stu-id="73979-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="73979-185">Deze regel is niet van toepassing op een groot deel van de bestaande inhoud in PowerShell-Docs, maar zal in de loop van de tijd worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73979-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="73979-186">Lever gerust een bijdrage. Met de [reflow-uitbreiding][reflow] in Visual Studio Code (VSCode) kunt u alinea's eenvoudig opnieuw opmaken overeenkomstig deze beperking.</span><span class="sxs-lookup"><span data-stu-id="73979-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="73979-187">Lijsten</span><span class="sxs-lookup"><span data-stu-id="73979-187">Lists</span></span>

<span data-ttu-id="73979-188">Als uw lijst meerdere zinnen of alinea’s bevat, kunt u overwegen een koptekst op subniveau te gebruiken in plaats van een lijst.</span><span class="sxs-lookup"><span data-stu-id="73979-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="73979-189">Lijsten moeten worden omgeven door één lege regel.</span><span class="sxs-lookup"><span data-stu-id="73979-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="73979-190">Niet-geordende lijsten</span><span class="sxs-lookup"><span data-stu-id="73979-190">Unordered lists</span></span>

<span data-ttu-id="73979-191">Beëindig lijstitems niet met een punt, tenzij ze meerdere zinnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="73979-192">Gebruik het afbreekstreepje (`-`) als opsommingsteken voor een lijstitem.</span><span class="sxs-lookup"><span data-stu-id="73979-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="73979-193">Dit voorkomt verwarring met vette of cursieve markeringen, waarbij het sterretje [`*`] wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73979-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="73979-194">Voeg een regel toe en lijn de inspringing uit met het eerste teken achter het opsommingsteken om een alinea of andere elementen onder een opsomming op te nemen.</span><span class="sxs-lookup"><span data-stu-id="73979-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="73979-195">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="73979-196">Dit is een lijst met subelementen onder een opsommingsteken.</span><span class="sxs-lookup"><span data-stu-id="73979-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="73979-197">Item van eerste opsomming</span><span class="sxs-lookup"><span data-stu-id="73979-197">First bullet item</span></span>

  <span data-ttu-id="73979-198">Zin met uitleg voor de eerste opsomming.</span><span class="sxs-lookup"><span data-stu-id="73979-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="73979-199">Item van subopsommingsteken</span><span class="sxs-lookup"><span data-stu-id="73979-199">Sub-bullet item</span></span>

    <span data-ttu-id="73979-200">Zin met uitleg voor de subopsomming.</span><span class="sxs-lookup"><span data-stu-id="73979-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="73979-201">Item van tweede opsomming</span><span class="sxs-lookup"><span data-stu-id="73979-201">Second bullet item</span></span>
- <span data-ttu-id="73979-202">Item van derde opsomming</span><span class="sxs-lookup"><span data-stu-id="73979-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="73979-203">Geordende lijsten</span><span class="sxs-lookup"><span data-stu-id="73979-203">Ordered lists</span></span>

<span data-ttu-id="73979-204">Lijn de inspringing uit met het eerste teken achter het itemnummer om een alinea of andere elementen onder een genummerd item op te nemen.</span><span class="sxs-lookup"><span data-stu-id="73979-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="73979-205">om deze uitvoer te krijgen:</span><span class="sxs-lookup"><span data-stu-id="73979-205">to get this output:</span></span>

> 1. <span data-ttu-id="73979-206">Plaats bij het eerste element een spatie achter de 1.</span><span class="sxs-lookup"><span data-stu-id="73979-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="73979-207">Lange zinnen moeten passend worden gemaakt op de volgende regel en worden uitgelijnd met het eerste teken na de markering van de genummerde lijst.</span><span class="sxs-lookup"><span data-stu-id="73979-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="73979-208">U kunt een tweede element (zoals dit) opnemen door een nieuwe regel na de eerste in te voegen en de inspringing uit te lijnen.</span><span class="sxs-lookup"><span data-stu-id="73979-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="73979-209">De inspringing van het tweede element moet worden uitgelijnd met het eerste teken na de markering van de genummerde lijst.</span><span class="sxs-lookup"><span data-stu-id="73979-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="73979-210">Voor items met één cijfer, zoals dit, springt u in naar kolom 4.</span><span class="sxs-lookup"><span data-stu-id="73979-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="73979-211">Voor items met dubbele cijfers, zoals nummer 10, springt u in naar kolom 5.</span><span class="sxs-lookup"><span data-stu-id="73979-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="73979-212">Het volgende genummerde item begint hier.</span><span class="sxs-lookup"><span data-stu-id="73979-212">The next numbered item starts here.</span></span>

<span data-ttu-id="73979-213">Alle items in de genummerde lijst moeten het nummer `1.` gebruiken in plaats van een interval voor elk item.</span><span class="sxs-lookup"><span data-stu-id="73979-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="73979-214">Bij het weergeven van de Markdown wordt de waarde automatisch verhoogd.</span><span class="sxs-lookup"><span data-stu-id="73979-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="73979-215">Hierdoor kunnen items gemakkelijker in een andere volgorde worden geplaatst en wordt de inspringing van onderliggende inhoud gestandaardiseerd.</span><span class="sxs-lookup"><span data-stu-id="73979-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="73979-216">Syntaxiselementen van opdrachten opmaken</span><span class="sxs-lookup"><span data-stu-id="73979-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="73979-217">Namen van PowerShell-cmdlets hebben [Pascal-hoofdletters][pascal-case].</span><span class="sxs-lookup"><span data-stu-id="73979-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="73979-218">Werkwoorden zijn van zelfstandige naamwoorden gescheiden door middel van een koppelteken.</span><span class="sxs-lookup"><span data-stu-id="73979-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="73979-219">Gebruik altijd de volledige Pascal Case-naam voor cmdlets en parameters.</span><span class="sxs-lookup"><span data-stu-id="73979-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="73979-220">Vermijd het gebruik van aliassen tenzij u specifiek over een alias spreekt.</span><span class="sxs-lookup"><span data-stu-id="73979-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="73979-221">Binnen een alinea moeten taaltrefwoorden, cmdlet-namen en verwijzingen naar variabelen tussen accents graves (`` ` ``) worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="73979-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="73979-222">Namen van eigenschappen, parameters en klassen moeten **vet** zijn.</span><span class="sxs-lookup"><span data-stu-id="73979-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="73979-223">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="73979-224">Wanneer naar een parameter wordt verwezen aan de hand van de naam, moet de naam **vet** zijn.</span><span class="sxs-lookup"><span data-stu-id="73979-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="73979-225">Wanneer het gebruik van een parameter met een afbreekstreepje als voorvoegsel wordt gedemonstreerd, moet de parameter tussen accents graves worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="73979-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="73979-226">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="73979-227">Wanneer naar externe opdrachten (EXE-bestanden, scripts, enzovoort) wordt verwezen, moet de naam van de opdracht vet zijn, alleen kleine letters bevatten (of hoofdletters als deze aan het begin van een zin staat) en de juiste bestandsextensie bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="73979-228">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="73979-229">Wanneer een voorbeeld van het gebruik van een externe opdracht wordt gebruikt, moet het voorbeeld tussen accents graves zijn geplaatst.</span><span class="sxs-lookup"><span data-stu-id="73979-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="73979-230">Als er een naamconflict met een alias is, moet u de bestandsextensie in het voorbeeld van de opdracht opnemen.</span><span class="sxs-lookup"><span data-stu-id="73979-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="73979-231">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="73979-232">Als u een conceptueel artikel (in tegenstelling tot referentie-inhoud) schrijft, moet de eerste instantie van een cmdlet-naam een hyperlink naar de cmdlet-documentatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="73979-233">Gebruik geen accents graves, vetgedrukte tekst of andere opmaak binnen de haakjes van een hyperlink.</span><span class="sxs-lookup"><span data-stu-id="73979-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="73979-234">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="73979-235">Raadpleeg het gedeelte [Hyperlinks](#hyperlinks) in de stijlgids voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="73979-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="73979-236">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="73979-236">Images</span></span>

<span data-ttu-id="73979-237">De syntaxis voor het insluiten van een afbeelding is:</span><span class="sxs-lookup"><span data-stu-id="73979-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="73979-238">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="73979-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="73979-239">Hierbij is `alt text` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="73979-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="73979-240">Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig.</span><span class="sxs-lookup"><span data-stu-id="73979-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="73979-241">Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.</span><span class="sxs-lookup"><span data-stu-id="73979-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="73979-242">Afbeeldingen moeten worden opgeslagen in een `media/<article-name>`-map in de map die uw artikel bevat.</span><span class="sxs-lookup"><span data-stu-id="73979-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="73979-243">Afbeeldingen moeten niet worden gedeeld tussen artikelen.</span><span class="sxs-lookup"><span data-stu-id="73979-243">Images should not be shared between articles.</span></span> <span data-ttu-id="73979-244">Maak onder de map `media` een map die overeenkomt met de bestandsnaam van uw artikel.</span><span class="sxs-lookup"><span data-stu-id="73979-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="73979-245">Kopieer de afbeeldingen voor dat artikel naar de nieuwe map.</span><span class="sxs-lookup"><span data-stu-id="73979-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="73979-246">Als een afbeelding door meerdere artikelen wordt gebruikt, moet elke afbeeldingsmap een kopie van het afbeeldingsbestand bevatten.</span><span class="sxs-lookup"><span data-stu-id="73979-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="73979-247">Dit voorkomt dat een wijziging voor een afbeelding in het ene artikel gevolgen heeft voor het andere artikelen.</span><span class="sxs-lookup"><span data-stu-id="73979-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="73979-248">In sommige gevallen wilt u mogelijk afbeeldingen, zoals logo’s en pictogrammen, delen in meerdere artikelen.</span><span class="sxs-lookup"><span data-stu-id="73979-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="73979-249">Deze afbeeldingen worden in de map `/media/shared` in de hoofdmap van de opslagplaats opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="73979-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="73979-250">De volgende soorten afbeeldingsbestanden worden ondersteund: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span><span class="sxs-lookup"><span data-stu-id="73979-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
