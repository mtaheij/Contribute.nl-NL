---
title: Markdown-naslaginformatie voor docs.microsoft.com
description: Maak kennis met de Markdown-functies en -syntaxis die worden gebruikt op het Microsoft Docs-platform.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624735"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="fb485-103">Docs Markdown-naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="fb485-103">Docs Markdown reference</span></span>

<span data-ttu-id="fb485-104">Dit artikel bevat alfabetische naslaginformatie voor het schrijven van Markdown voor docs.microsoft.com (Docs).</span><span class="sxs-lookup"><span data-stu-id="fb485-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="fb485-105">[Markdown](https://daringfireball.net/projects/markdown/) is een lichtgewicht opmaakcodetaal met een syntaxis voor platte tekst.</span><span class="sxs-lookup"><span data-stu-id="fb485-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="fb485-106">Docs biedt ondersteuning voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parserengine [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="fb485-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="fb485-107">Docs biedt ook ondersteuning voor aangepaste Markdown-extensies die uitgebreide inhoud op de Docs-site bieden.</span><span class="sxs-lookup"><span data-stu-id="fb485-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="fb485-108">U kunt u elke teksteditor gebruiken voor het schrijven van Markdown, maar u kunt het beste [Visual Studio Code](https://code.visualstudio.com/) met het [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb485-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="fb485-109">Het Docs Authoring Pack bevat bewerkingsprogramma's en preview-functionaliteit waarmee u kunt zien hoe uw artikelen eruitzien zoals ze worden weergegeven op Docs.</span><span class="sxs-lookup"><span data-stu-id="fb485-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="fb485-110">Waarschuwingen (Opmerking, Tip, Belangrijk, Let op, Waarschuwing)</span><span class="sxs-lookup"><span data-stu-id="fb485-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="fb485-111">Dit zijn waarschuwingen voor een Markdown-extensie om blokcitaten te maken die op docs.microsoft.com worden weergegeven met kleuren en pictogrammen die het belang van de inhoud aanduiden.</span><span class="sxs-lookup"><span data-stu-id="fb485-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="fb485-112">De volgende typen waarschuwingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="fb485-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="fb485-113">Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="fb485-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="fb485-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="fb485-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="fb485-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb485-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="fb485-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="fb485-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="fb485-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="fb485-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="fb485-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="fb485-119">Punthaken</span><span class="sxs-lookup"><span data-stu-id="fb485-119">Angle brackets</span></span>

<span data-ttu-id="fb485-120">Als u in lopende tekst punthaken gebruikt, bijvoorbeeld om een tijdelijke aanduiding aan te geven, moet u de punthaken handmatig coderen.</span><span class="sxs-lookup"><span data-stu-id="fb485-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="fb485-121">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="fb485-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="fb485-122">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;` of `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="fb485-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="fb485-123">Punthaken hoeven niet te worden voorafgegaan in tekst die is opgemaakt als code in regels of in codeblokken.</span><span class="sxs-lookup"><span data-stu-id="fb485-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="fb485-124">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="fb485-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="fb485-125">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="fb485-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="fb485-126">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="fb485-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="fb485-127">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ&euro;&trade;s</span><span class="sxs-lookup"><span data-stu-id="fb485-127">Otherwise, you end up with things like this when the file is published: Itâ&euro;&trade;s</span></span>

<span data-ttu-id="fb485-128">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="fb485-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="fb485-129">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="fb485-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="fb485-130">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="fb485-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="fb485-131">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="fb485-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="fb485-132">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="fb485-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="fb485-133">Blokcitaten</span><span class="sxs-lookup"><span data-stu-id="fb485-133">Blockquotes</span></span>

<span data-ttu-id="fb485-134">Blokcitaten worden gemaakt met het teken `>`:</span><span class="sxs-lookup"><span data-stu-id="fb485-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="fb485-135">Het voorbeeld hierboven wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="fb485-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="fb485-136">Dit is een blokcitaat.</span><span class="sxs-lookup"><span data-stu-id="fb485-136">This is a blockquote.</span></span> <span data-ttu-id="fb485-137">Deze wordt doorgaans ingesprongen weergegeven met een andere achtergrondkleur.</span><span class="sxs-lookup"><span data-stu-id="fb485-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="fb485-138">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="fb485-138">Bold and italic text</span></span>

<span data-ttu-id="fb485-139">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="fb485-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="fb485-140">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="fb485-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="fb485-141">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="fb485-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="fb485-142">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="fb485-142">Code snippets</span></span>

<span data-ttu-id="fb485-143">Docs Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="fb485-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="fb485-144">Zie [Code toevoegen aan docs](code-in-docs.md)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fb485-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="fb485-145">Kolommen</span><span class="sxs-lookup"><span data-stu-id="fb485-145">Columns</span></span>

<span data-ttu-id="fb485-146">Met de Markdown-extensie **kolommen** kunnen Docs-schrijvers op kolommen gebaseerde inhoudsindelingen toevoegen die flexibelere en krachtiger zijn dan normale Markdown-tabellen, die alleen geschikt zijn voor echte tabellaire gegevens.</span><span class="sxs-lookup"><span data-stu-id="fb485-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="fb485-147">U kunt maximaal vier kolommen toevoegen en het optionele kenmerk `span` gebruiken om twee of meer kolommen samen te voegen.</span><span class="sxs-lookup"><span data-stu-id="fb485-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="fb485-148">De syntaxis voor kolommen ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="fb485-149">Kolommen mogen alleen elementaire Markdown inclusief afbeeldingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="fb485-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="fb485-150">Kopteksten, tabellen, tabs en andere complexe structuren mogen niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fb485-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="fb485-151">Een rij kan geen inhoud buiten een kolom bevatten.</span><span class="sxs-lookup"><span data-stu-id="fb485-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="fb485-152">Met de volgende Markdown maakt u bijvoorbeeld één kolom die bestaat uit twee kolombreedten en één standaardkolom (geen `span`):</span><span class="sxs-lookup"><span data-stu-id="fb485-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="fb485-153">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="fb485-154">**Dit is een kolom met twee kolombreedten met veel tekst.**</span><span class="sxs-lookup"><span data-stu-id="fb485-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="fb485-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="fb485-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="fb485-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="fb485-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="fb485-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="fb485-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="fb485-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="fb485-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="fb485-159">**Dit is een kolom met één kolombreedte met een afbeelding.**</span><span class="sxs-lookup"><span data-stu-id="fb485-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="fb485-161">Koppen</span><span class="sxs-lookup"><span data-stu-id="fb485-161">Headings</span></span>

<span data-ttu-id="fb485-162">Docs ondersteunt zes niveaus Markdown-koppen:</span><span class="sxs-lookup"><span data-stu-id="fb485-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="fb485-163">Tussen de laatste `#` en de koptekst moet een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="fb485-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="fb485-164">Elk Markdown-bestand moet precies één H1-koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="fb485-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="fb485-165">De H1-koptekst moet de eerste inhoud in het bestand zijn na het YML-blok met metagegevens.</span><span class="sxs-lookup"><span data-stu-id="fb485-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="fb485-166">H2-kopteksten verschijnen automatisch in het navigatiemenu aan de rechterkant van het gepubliceerde bestand.</span><span class="sxs-lookup"><span data-stu-id="fb485-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="fb485-167">Dit geldt niet voor koppen op een lager niveau. Gebruik H2's dus strategisch om lezers te helpen door uw inhoud te navigeren.</span><span class="sxs-lookup"><span data-stu-id="fb485-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="fb485-168">HMTL-koppen, zoals `<h1>`, worden niet aanbevolen en leiden in sommige gevallen tot opbouwwaarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="fb485-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="fb485-169">U kunt de afzonderlijke koppen in een bestand koppelen via [bladwijzerkoppelingen](how-to-write-links.md#explicit-anchor-links).</span><span class="sxs-lookup"><span data-stu-id="fb485-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#explicit-anchor-links).</span></span>

## <a name="html"></a><span data-ttu-id="fb485-170">HTML</span><span class="sxs-lookup"><span data-stu-id="fb485-170">HTML</span></span>

<span data-ttu-id="fb485-171">Hoewel Markdown ondersteuning biedt voor inline-HTML, wordt HTML niet aanbevolen voor het publiceren naar Docs. Bovendien leidt dit, behalve bij een beperkte lijst met waarden, tot compileerfouten of -waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="fb485-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="fb485-172">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="fb485-172">Images</span></span>

<span data-ttu-id="fb485-173">De volgende bestandstypen worden standaard voor afbeeldingen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="fb485-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="fb485-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="fb485-174">.jpg</span></span>
- <span data-ttu-id="fb485-175">.png</span><span class="sxs-lookup"><span data-stu-id="fb485-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="fb485-176">Standaard conceptuele afbeeldingen (standaard Markdown)</span><span class="sxs-lookup"><span data-stu-id="fb485-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="fb485-177">De basis Markdown-syntaxis om een afbeelding in te sluiten is:</span><span class="sxs-lookup"><span data-stu-id="fb485-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="fb485-178">Hierbij is `<alt text>` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="fb485-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="fb485-179">Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig.</span><span class="sxs-lookup"><span data-stu-id="fb485-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="fb485-180">Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.</span><span class="sxs-lookup"><span data-stu-id="fb485-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="fb485-181">Onderstrepingstekens in alternatieve tekst worden niet correct weergegeven, tenzij u ze markeert als bijzondere tekens door ze met een backslash (`\_`) toe te voegen als voorvoegsel.</span><span class="sxs-lookup"><span data-stu-id="fb485-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="fb485-182">Kopieer echter geen bestandsnamen om te gebruiken als alternatieve tekst.</span><span class="sxs-lookup"><span data-stu-id="fb485-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="fb485-183">Dus in plaats van dit:</span><span class="sxs-lookup"><span data-stu-id="fb485-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="fb485-184">Schrijft u dit:</span><span class="sxs-lookup"><span data-stu-id="fb485-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="fb485-185">Standaard conceptuele afbeeldingen (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="fb485-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="fb485-186">De aangepaste Docs-extensie `:::image:::` ondersteunt standaardafbeeldingen, complexe afbeeldingen en pictogrammen.</span><span class="sxs-lookup"><span data-stu-id="fb485-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="fb485-187">De oudere Markdown-syntaxis kan nog worden gebruikt voor standaardafbeeldingen, maar u kunt beter gebruikmaken van de nieuwe extensie, omdat deze krachtigere functionaliteit ondersteunt, zoals het opgeven van een lokalisatiebereik dat afwijkt van het bovenliggende onderwerp.</span><span class="sxs-lookup"><span data-stu-id="fb485-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="fb485-188">Deze geavanceerde functionaliteit wordt in de toekomst verder uitgebreid, zoals het selecteren van de gedeelde afbeeldingengalerie in plaats van het opgeven van een lokale afbeelding.</span><span class="sxs-lookup"><span data-stu-id="fb485-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="fb485-189">De nieuwe syntaxis ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="fb485-190">Als `type="content"` (standaard), zijn zowel `source` als `alt-text` vereist.</span><span class="sxs-lookup"><span data-stu-id="fb485-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="fb485-191">Complexe afbeeldingen met lange beschrijvingen</span><span class="sxs-lookup"><span data-stu-id="fb485-191">Complex images with long descriptions</span></span>

<span data-ttu-id="fb485-192">U kunt deze extensie ook gebruiken om een afbeelding toe te voegen met een lange beschrijving die wordt gelezen door schermlezers, maar niet visueel wordt weergegeven op de gepubliceerde pagina.</span><span class="sxs-lookup"><span data-stu-id="fb485-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="fb485-193">Lange beschrijvingen zijn een toegangsvereiste voor complexe afbeeldingen, zoals grafieken.</span><span class="sxs-lookup"><span data-stu-id="fb485-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="fb485-194">De syntaxis ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="fb485-195">Als `type="complex"`, `source`, `alt-text`, zijn een lange beschrijving en de tag `:::image-end:::` vereist.</span><span class="sxs-lookup"><span data-stu-id="fb485-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="fb485-196">Lokalisatiebereik opgeven</span><span class="sxs-lookup"><span data-stu-id="fb485-196">Specifying loc-scope</span></span>

<span data-ttu-id="fb485-197">Soms wijkt het lokalisatiebereik voor een afbeelding af van het bereik van een artikel of de module waarin de afbeelding is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="fb485-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="fb485-198">Dit kan leiden tot onjuistheden, bijvoorbeeld als een schermopname van een product per ongeluk wordt gelokaliseerd in een taal waarin het product niet beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="fb485-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="fb485-199">Om dit te voorkomen, kunt u het optionele kenmerk `loc-scope` opgeven in afbeeldingen van het type `content` en `complex`.</span><span class="sxs-lookup"><span data-stu-id="fb485-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="fb485-200">Pictogrammen</span><span class="sxs-lookup"><span data-stu-id="fb485-200">Icons</span></span>

<span data-ttu-id="fb485-201">De afbeeldingsextensie biedt ondersteuning voor pictogrammen. Dit zijn decoratieve afbeeldingen die geen alternatieve tekst mogen bevatten.</span><span class="sxs-lookup"><span data-stu-id="fb485-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="fb485-202">De syntaxis voor pictogrammen ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="fb485-203">Als `type="icon"`, moet alleen `source` worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="fb485-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="fb485-204">Ingesloten Markdown-bestanden</span><span class="sxs-lookup"><span data-stu-id="fb485-204">Included Markdown files</span></span>

<span data-ttu-id="fb485-205">Wanneer de Markdown-bestanden moeten worden herhaald in meerdere artikelen, kunt u een Include-bestand gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb485-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="fb485-206">Met de functie Includes kunnen Docs de verwijzing tijdens het bouwen vervangen door de inhoud van het Include-bestand.</span><span class="sxs-lookup"><span data-stu-id="fb485-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="fb485-207">U kunt Include-bestanden op de volgende manieren gebruiken:</span><span class="sxs-lookup"><span data-stu-id="fb485-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="fb485-208">Inline: Een gewoon stuk tekst inline hergebruiken in een zin.</span><span class="sxs-lookup"><span data-stu-id="fb485-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="fb485-209">Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="fb485-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="fb485-210">Een inline- of blokinsluitingsbestand is niets meer of minder dan een Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="fb485-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="fb485-211">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="fb485-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="fb485-212">Include-bestanden bevinden zich doorgaans in een submap *includes* in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="fb485-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="fb485-213">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="fb485-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="fb485-214">Ingesloten syntaxis</span><span class="sxs-lookup"><span data-stu-id="fb485-214">Includes syntax</span></span>

<span data-ttu-id="fb485-215">Een blokinsluiting wordt op een eigen regel weergegeven:</span><span class="sxs-lookup"><span data-stu-id="fb485-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="fb485-216">Inline-insluitingen bevinden zich in een regel:</span><span class="sxs-lookup"><span data-stu-id="fb485-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="fb485-217">waarbij `<title>` de naam van het bestand is en `<filepath>` het relatieve pad naar het bestand is.</span><span class="sxs-lookup"><span data-stu-id="fb485-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="fb485-218">`INCLUDE` moet met een hoofdletter beginnen en er moet een spatie voor de `<title>` staan.</span><span class="sxs-lookup"><span data-stu-id="fb485-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="fb485-219">Dit zijn de vereisten en overwegingen voor insluitingsbestanden:</span><span class="sxs-lookup"><span data-stu-id="fb485-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="fb485-220">Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="fb485-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="fb485-221">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="fb485-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="fb485-222">Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van Docs-extensies.</span><span class="sxs-lookup"><span data-stu-id="fb485-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="fb485-223">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="fb485-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="fb485-224">Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="fb485-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="fb485-225">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel.</span><span class="sxs-lookup"><span data-stu-id="fb485-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="fb485-226">Voeg geen insluitingsbestanden in andere insluitingsbestanden in.</span><span class="sxs-lookup"><span data-stu-id="fb485-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="fb485-227">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>` */includes/media*.</span><span class="sxs-lookup"><span data-stu-id="fb485-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="fb485-228">In de hoofdmap van de *mediamap* mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="fb485-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="fb485-229">Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende *mediamap* te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fb485-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="fb485-230">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="fb485-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="fb485-231">Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel.</span><span class="sxs-lookup"><span data-stu-id="fb485-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="fb485-232">Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.</span><span class="sxs-lookup"><span data-stu-id="fb485-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="fb485-233">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.</span><span class="sxs-lookup"><span data-stu-id="fb485-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="fb485-234">Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="fb485-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="fb485-235">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="fb485-235">Links</span></span>

<span data-ttu-id="fb485-236">Zie [Koppelingen in documentatie gebruiken](how-to-write-links.md) voor meer informatie over de syntaxis voor koppelingen.</span><span class="sxs-lookup"><span data-stu-id="fb485-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="fb485-237">Lijsten (Genummerd, Met opsommingstekens, Controlelijst)</span><span class="sxs-lookup"><span data-stu-id="fb485-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="fb485-238">Genummerde lijst</span><span class="sxs-lookup"><span data-stu-id="fb485-238">Numbered list</span></span>

<span data-ttu-id="fb485-239">U kunt alle 1's gebruiken om een genummerde lijst te maken.</span><span class="sxs-lookup"><span data-stu-id="fb485-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="fb485-240">De nummers worden bij het publiceren weergegeven als een sequentiële lijst in oplopende volgorde.</span><span class="sxs-lookup"><span data-stu-id="fb485-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="fb485-241">Voor betere leesbaarheid van de bron kunt u uw lijsten handmatig verhogen.</span><span class="sxs-lookup"><span data-stu-id="fb485-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="fb485-242">Gebruik geen letters in lijsten, ook niet in geneste lijsten.</span><span class="sxs-lookup"><span data-stu-id="fb485-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="fb485-243">Deze worden bij het publiceren naar Docs niet goed weergegeven. Geneste lijsten die gebruikmaken van nummers, worden bij het publiceren weergegeven als kleine letters.</span><span class="sxs-lookup"><span data-stu-id="fb485-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="fb485-244">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="fb485-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="fb485-245">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-245">This renders as follows:</span></span>

1. <span data-ttu-id="fb485-246">This is</span><span class="sxs-lookup"><span data-stu-id="fb485-246">This is</span></span>
1. <span data-ttu-id="fb485-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="fb485-247">a parent numbered list</span></span>
   1. <span data-ttu-id="fb485-248">and this is</span><span class="sxs-lookup"><span data-stu-id="fb485-248">and this is</span></span>
   1. <span data-ttu-id="fb485-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="fb485-249">a nested numbered list</span></span>
1. <span data-ttu-id="fb485-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="fb485-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="fb485-251">Lijst met opsommingstekens</span><span class="sxs-lookup"><span data-stu-id="fb485-251">Bulleted list</span></span>

<span data-ttu-id="fb485-252">Als u een lijst met opsommingstekens wilt maken, gebruikt u `-` of `*` gevolgd door een spatie aan het begin van elke regel:</span><span class="sxs-lookup"><span data-stu-id="fb485-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="fb485-253">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-253">This renders as follows:</span></span>

- <span data-ttu-id="fb485-254">This is</span><span class="sxs-lookup"><span data-stu-id="fb485-254">This is</span></span>
- <span data-ttu-id="fb485-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="fb485-255">a parent bulleted list</span></span>
  - <span data-ttu-id="fb485-256">and this is</span><span class="sxs-lookup"><span data-stu-id="fb485-256">and this is</span></span>
  - <span data-ttu-id="fb485-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="fb485-257">a nested bulleted list</span></span>
- <span data-ttu-id="fb485-258">All done!</span><span class="sxs-lookup"><span data-stu-id="fb485-258">All done!</span></span>

<span data-ttu-id="fb485-259">Welke syntaxis u ook gebruikt, `-` of `*`, gebruik deze consistent binnen een artikel.</span><span class="sxs-lookup"><span data-stu-id="fb485-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="fb485-260">Controlelijst</span><span class="sxs-lookup"><span data-stu-id="fb485-260">Checklist</span></span>

<span data-ttu-id="fb485-261">Controlelijsten zijn beschikbaar voor gebruik op Docs via een aangepaste Markdown-extensie:</span><span class="sxs-lookup"><span data-stu-id="fb485-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="fb485-262">Dit voorbeeld wordt op Docs weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="fb485-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="fb485-263">List item 1</span></span>
> * <span data-ttu-id="fb485-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="fb485-264">List item 2</span></span>
> * <span data-ttu-id="fb485-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="fb485-265">List item 3</span></span>

<span data-ttu-id="fb485-266">Gebruik controlelijsten aan het begin of eind van een artikel om inhoud voor 'Wat gaat u leren' of 'Wat hebt u geleerd' samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="fb485-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="fb485-267">Voeg geen willekeurige controlelijsten ergens anders in een artikel toe.</span><span class="sxs-lookup"><span data-stu-id="fb485-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="fb485-268">Actie volgende stap</span><span class="sxs-lookup"><span data-stu-id="fb485-268">Next step action</span></span>

<span data-ttu-id="fb485-269">U kunt een aangepaste extensie gebruiken om een knop voor de actie van de volgende stap toe te voegen aan Docs-pagina's.</span><span class="sxs-lookup"><span data-stu-id="fb485-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="fb485-270">De syntaxis ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="fb485-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="fb485-271">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="fb485-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="fb485-272">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="fb485-273">Meer informatie over het toevoegen van code aan artikelen</span><span class="sxs-lookup"><span data-stu-id="fb485-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="fb485-274">U kunt elke ondersteunde koppeling in een volgende stapactie gebruiken, met inbegrip van een Markdown-koppeling naar een andere webpagina.</span><span class="sxs-lookup"><span data-stu-id="fb485-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="fb485-275">In de meeste gevallen is de koppeling voor de volgende actie een relatieve koppeling naar een ander bestand in dezelfde docset.</span><span class="sxs-lookup"><span data-stu-id="fb485-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="fb485-276">Niet-gelokaliseerde tekenreeksen</span><span class="sxs-lookup"><span data-stu-id="fb485-276">Non-localized strings</span></span>

<span data-ttu-id="fb485-277">U kunt de aangepaste Markdown-extensie `no-loc` gebruiken om tekenreeksen te identificeren van inhoud die tijdens het lokalisatieproces moeten worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="fb485-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="fb485-278">Alle aangeroepen tekenreeksen zijn hoofdlettergevoelig. Dat wil zeggen dat de tekenreeks exact moet overeenkomen om te worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="fb485-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="fb485-279">Als u een afzonderlijke tekenreeks als niet-lokaliseerbaar wilt markeren, gebruikt u de volgende syntaxis:</span><span class="sxs-lookup"><span data-stu-id="fb485-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="fb485-280">In het volgende voorbeeld wordt slechts één exemplaar van `Document` genegeerd tijdens het lokalisatieproces:</span><span class="sxs-lookup"><span data-stu-id="fb485-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="fb485-281">Gebruik `\` om speciale tekens te escapen:</span><span class="sxs-lookup"><span data-stu-id="fb485-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="fb485-282">U kunt ook metagegevens in de YAML-header gebruiken om alle exemplaren van een tekenreeks binnen het huidige Markdown-bestand te markeren als niet-lokaliseerbaar:</span><span class="sxs-lookup"><span data-stu-id="fb485-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="fb485-283">De metagegevens voor niet-lokaliseerbaar worden niet ondersteund als globale metagegevens in het bestand *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="fb485-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="fb485-284">De gelokaliseerde pijplijn leest het bestand *docfx.json* niet. Daarom moeten de metagegevens voor niet-lokaliseerbaar aan elk afzonderlijk bronbestand worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fb485-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="fb485-285">In het volgende voorbeeld wordt zowel in de metagegevens `title` als in de Markdown-header het woord `Document` tijdens het lokalisatieproces genegeerd.</span><span class="sxs-lookup"><span data-stu-id="fb485-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="fb485-286">In de metagegevens `description` en de belangrijkste inhoud van Markdown wordt het woord `document` gelokaliseerd, omdat het niet begint met een hoofdletter `D`.</span><span class="sxs-lookup"><span data-stu-id="fb485-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="fb485-287">Selectors</span><span class="sxs-lookup"><span data-stu-id="fb485-287">Selectors</span></span>

<span data-ttu-id="fb485-288">Selectors zijn UI-elementen waarmee de gebruiker tussen meerdere varianten van hetzelfde artikel kan schakelen.</span><span class="sxs-lookup"><span data-stu-id="fb485-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="fb485-289">Ze worden gebruikt in sommige docsets om verschillen in de implementatie van technologieën of platformen aan te pakken.</span><span class="sxs-lookup"><span data-stu-id="fb485-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="fb485-290">Selectors zijn doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="fb485-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="fb485-291">Omdat dezelfde selector Markdown in elk artikelbestand in de selector wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="fb485-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="fb485-292">Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelbestanden waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fb485-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="fb485-293">Er zijn twee soorten selectors, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="fb485-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="fb485-294">Single selector</span><span class="sxs-lookup"><span data-stu-id="fb485-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="fb485-295">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="fb485-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="fb485-304">Multi-selector</span><span class="sxs-lookup"><span data-stu-id="fb485-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="fb485-305">... wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="fb485-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="fb485-318">Subscript en superscript</span><span class="sxs-lookup"><span data-stu-id="fb485-318">Subscript and superscript</span></span>

<span data-ttu-id="fb485-319">Gebruik alleen subscript of superscript als dat nodig is voor de technische nauwkeurigheid, zoals bij het schrijven van wiskundige formules.</span><span class="sxs-lookup"><span data-stu-id="fb485-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="fb485-320">Gebruik deze niet voor niet-standaardstijlen, zoals voetnoten.</span><span class="sxs-lookup"><span data-stu-id="fb485-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="fb485-321">Gebruik HTML voor zowel subscript als superscript:</span><span class="sxs-lookup"><span data-stu-id="fb485-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="fb485-322">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-322">This renders as follows:</span></span>

<span data-ttu-id="fb485-323">Hallo <sub>Dit is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="fb485-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="fb485-324">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-324">This renders as follows:</span></span>

<span data-ttu-id="fb485-325">Tot ziens <sup>Dit is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="fb485-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="fb485-326">Tables</span><span class="sxs-lookup"><span data-stu-id="fb485-326">Tables</span></span>

<span data-ttu-id="fb485-327">De eenvoudigste manier om een tabel in Markdown te maken is gebruik te maken van pipes en regels.</span><span class="sxs-lookup"><span data-stu-id="fb485-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="fb485-328">Als u een standaardtabel met een kop wilt maken, laat u de eerste regel volgen door een stippellijn:</span><span class="sxs-lookup"><span data-stu-id="fb485-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="fb485-329">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-329">This renders as follows:</span></span>

|<span data-ttu-id="fb485-330">This is</span><span class="sxs-lookup"><span data-stu-id="fb485-330">This is</span></span>   |<span data-ttu-id="fb485-331">a simple</span><span class="sxs-lookup"><span data-stu-id="fb485-331">a simple</span></span>   |<span data-ttu-id="fb485-332">table header</span><span class="sxs-lookup"><span data-stu-id="fb485-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="fb485-333">table</span><span class="sxs-lookup"><span data-stu-id="fb485-333">table</span></span>     |<span data-ttu-id="fb485-334">data</span><span class="sxs-lookup"><span data-stu-id="fb485-334">data</span></span>       |<span data-ttu-id="fb485-335">here</span><span class="sxs-lookup"><span data-stu-id="fb485-335">here</span></span>        |
|<span data-ttu-id="fb485-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="fb485-336">it doesn't</span></span>|<span data-ttu-id="fb485-337">actually</span><span class="sxs-lookup"><span data-stu-id="fb485-337">actually</span></span>   |<span data-ttu-id="fb485-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="fb485-338">have to line up nicely!</span></span>||

<span data-ttu-id="fb485-339">U kunt de kolommen uitlijnen met behulp van dubbele punten:</span><span class="sxs-lookup"><span data-stu-id="fb485-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="fb485-340">Wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="fb485-340">Renders as follows:</span></span>

| <span data-ttu-id="fb485-341">Fun</span><span class="sxs-lookup"><span data-stu-id="fb485-341">Fun</span></span>                  | <span data-ttu-id="fb485-342">With</span><span class="sxs-lookup"><span data-stu-id="fb485-342">With</span></span>                 | <span data-ttu-id="fb485-343">Tables</span><span class="sxs-lookup"><span data-stu-id="fb485-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="fb485-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="fb485-344">left-aligned column</span></span>  | <span data-ttu-id="fb485-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="fb485-345">right-aligned column</span></span> | <span data-ttu-id="fb485-346">centered column</span><span class="sxs-lookup"><span data-stu-id="fb485-346">centered column</span></span> |
| <span data-ttu-id="fb485-347">$100</span><span class="sxs-lookup"><span data-stu-id="fb485-347">$100</span></span>                 | <span data-ttu-id="fb485-348">$100</span><span class="sxs-lookup"><span data-stu-id="fb485-348">$100</span></span>                 | <span data-ttu-id="fb485-349">$100</span><span class="sxs-lookup"><span data-stu-id="fb485-349">$100</span></span>            |
| <span data-ttu-id="fb485-350">$10</span><span class="sxs-lookup"><span data-stu-id="fb485-350">$10</span></span>                  | <span data-ttu-id="fb485-351">$10</span><span class="sxs-lookup"><span data-stu-id="fb485-351">$10</span></span>                  | <span data-ttu-id="fb485-352">$10</span><span class="sxs-lookup"><span data-stu-id="fb485-352">$10</span></span>             |
| <span data-ttu-id="fb485-353">$1</span><span class="sxs-lookup"><span data-stu-id="fb485-353">$1</span></span>                   | <span data-ttu-id="fb485-354">$1</span><span class="sxs-lookup"><span data-stu-id="fb485-354">$1</span></span>                   | <span data-ttu-id="fb485-355">$1</span><span class="sxs-lookup"><span data-stu-id="fb485-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="fb485-356">U kunt met Docs Authoring Extension voor VS Code gemakkelijk basis-Markdown-tabellen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fb485-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="fb485-357">U kunt ook een [onlinegenerator voor tabellen](http://www.tablesgenerator.com/markdown_tables) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb485-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="fb485-358">Regeleinden in woorden in een tabelcel</span><span class="sxs-lookup"><span data-stu-id="fb485-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="fb485-359">Als u lange woorden in een Markdown-tabel gebruikt, kan de tabel worden uitgebreid naar het navigatievenster rechts, waardoor de tabel onleesbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="fb485-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="fb485-360">U kunt dit oplossen door toe te staan dat in de Docs-weergave automatisch regeleinden in woorden worden ingevoegd wanneer dit nodig is.</span><span class="sxs-lookup"><span data-stu-id="fb485-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="fb485-361">U laat eenvoudig de tabel teruglopen met de aangepaste klasse `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="fb485-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="fb485-362">Hier ziet u een Markdown-voorbeeld van een tabel met drie rijen die teruglopen door gebruik te maken van een `div` met de klassenaam `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="fb485-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="fb485-363">Deze wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="fb485-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="fb485-364">Name</span><span class="sxs-lookup"><span data-stu-id="fb485-364">Name</span></span>|<span data-ttu-id="fb485-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb485-365">Syntax</span></span>|<span data-ttu-id="fb485-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="fb485-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="fb485-367">Description</span><span class="sxs-lookup"><span data-stu-id="fb485-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="fb485-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="fb485-368">Quiet</span></span>|<span data-ttu-id="fb485-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="fb485-369">/quiet</span></span>|<span data-ttu-id="fb485-370">Yes</span><span class="sxs-lookup"><span data-stu-id="fb485-370">Yes</span></span>|<span data-ttu-id="fb485-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="fb485-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="fb485-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="fb485-372">NoRestart</span></span>|<span data-ttu-id="fb485-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="fb485-373">/norestart</span></span>|<span data-ttu-id="fb485-374">No</span><span class="sxs-lookup"><span data-stu-id="fb485-374">No</span></span>|<span data-ttu-id="fb485-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="fb485-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="fb485-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="fb485-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="fb485-377">Help</span><span class="sxs-lookup"><span data-stu-id="fb485-377">Help</span></span>|<span data-ttu-id="fb485-378">/help</span><span class="sxs-lookup"><span data-stu-id="fb485-378">/help</span></span>|<span data-ttu-id="fb485-379">No</span><span class="sxs-lookup"><span data-stu-id="fb485-379">No</span></span>|<span data-ttu-id="fb485-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="fb485-380">Provides help and quick reference.</span></span> <span data-ttu-id="fb485-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="fb485-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="fb485-382">Regeleinden in woorden in tabelcellen in de tweede kolom</span><span class="sxs-lookup"><span data-stu-id="fb485-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="fb485-383">Mogelijk wilt u dat regeleinden in woorden alleen automatisch in de tweede kolom van een tabel worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="fb485-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="fb485-384">Als u de regeleinden wilt beperken tot de tweede kolom, past u de klasse `mx-tdCol2BreakAll` toe met behulp van de `div`-wrappersyntaxis, zoals eerder besproken.</span><span class="sxs-lookup"><span data-stu-id="fb485-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="fb485-385">Gegevensmatrixtabellen</span><span class="sxs-lookup"><span data-stu-id="fb485-385">Data matrix tables</span></span>

<span data-ttu-id="fb485-386">Een gegevensmatrixtabel bevat zowel een header als een gewogen eerste kolom, waardoor linksboven een matrix met een lege cel wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fb485-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="fb485-387">Docs heeft aangepaste Markdown voor gegevensmatrixtabellen:</span><span class="sxs-lookup"><span data-stu-id="fb485-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="fb485-388">Elke vermelding in de eerste kolom moet dik worden gedrukt (`**bold**`), anders zijn de tabellen niet toegankelijk voor schermlezers of geldig voor Docs.</span><span class="sxs-lookup"><span data-stu-id="fb485-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="fb485-389">HTML-tabellen</span><span class="sxs-lookup"><span data-stu-id="fb485-389">HTML Tables</span></span>

<span data-ttu-id="fb485-390">HTML-tabellen worden niet aanbevolen voor docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="fb485-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="fb485-391">Ze kunnen niet door mensen worden gelezen in de bron. Dit is wel een basisprincipe van Markdown.</span><span class="sxs-lookup"><span data-stu-id="fb485-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
