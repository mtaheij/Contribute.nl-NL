---
title: Sjabloon en cheatsheet voor .NET-artikelen
description: Dit artikel bevat een handige sjabloon waarmee u nieuwe artikelen kunt maken voor opslagplaatsen voor .NET-documenten
ms.date: 11/07/2018
ms.openlocfilehash: 15f64ec86c475e2da2f6539c8f388d076389c4e0
ms.sourcegitcommit: 68d81b61ffa60aba16acfed023760449e16de91b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2018
ms.locfileid: "52299655"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="72216-103">Sjabloon voor metagegevens en Markdown voor .NET-documenten</span><span class="sxs-lookup"><span data-stu-id="72216-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="72216-104">Deze dotnet/docs-sjabloon bevat voorbeelden van Markdown-syntaxis, maar ook aanwijzingen voor het instellen van metagegevens.</span><span class="sxs-lookup"><span data-stu-id="72216-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="72216-105">Wanneer u een Markdown-bestand maakt, dient u de opgenomen sjabloon naar een nieuw bestand te kopiëren, de metagegevens in te vullen zoals hierna is aangegeven en de kop H1 boven de titel van het artikel te zetten.</span><span class="sxs-lookup"><span data-stu-id="72216-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="72216-106">Metagegevens</span><span class="sxs-lookup"><span data-stu-id="72216-106">Metadata</span></span>

<span data-ttu-id="72216-107">Het vereiste blok met metagegevens bevindt zich in het volgende voorbeeldblok met metagegevens:</span><span class="sxs-lookup"><span data-stu-id="72216-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="72216-108">Tussen de dubbele punt (:) en de waarde van een metagegevenselement **moet** een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="72216-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="72216-109">Dubbele punten in een waarde (zoals een titel) verbreken de metagegevensparser.</span><span class="sxs-lookup"><span data-stu-id="72216-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="72216-110">Omring in dit geval de titel met dubbele aanhalingstekens (bijvoorbeeld `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="72216-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="72216-111">**titel**: deze wordt in zoekprogrammaresultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="72216-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="72216-112">De titel mag niet identiek zijn aan de titel in uw kop H1 en moet maximaal 60 tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="72216-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="72216-113">**beschrijving**: hierin vat u de inhoud van het artikel samen.</span><span class="sxs-lookup"><span data-stu-id="72216-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="72216-114">Deze wordt meestal in de pagina met zoekresultaten weergegeven, maar wordt niet gebruikt voor de rangschikking van de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="72216-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="72216-115">De lengte dient 115 tot 145 tekens te bedragen, inclusief spaties.</span><span class="sxs-lookup"><span data-stu-id="72216-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="72216-116">**auteur**: het veld Auteur moet de **GitHub-gebruikersnaam** van de auteur bevatten.</span><span class="sxs-lookup"><span data-stu-id="72216-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="72216-117">**ms.date**: de datum van de laatste belangrijke update.</span><span class="sxs-lookup"><span data-stu-id="72216-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="72216-118">Werk deze bij voor bestaande artikelen als u het gehele artikel hebt bekeken en bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="72216-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="72216-119">Kleine aanpassingen, zoals typfouten e.d., rechtvaardigen geen update.</span><span class="sxs-lookup"><span data-stu-id="72216-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="72216-120">Er zijn andere metagegevens aan elk artikel toegevoegd, maar wij passen gewoonlijk de meeste metagegevenswaarden toe op mapniveau, zoals is opgegeven in **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="72216-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="72216-121">Elementaire Markdown, GFM en speciale tekens</span><span class="sxs-lookup"><span data-stu-id="72216-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="72216-122">U kunt de basisbeginselen van Markdown, GitHub Flavored Markdown (GFM) en OPS-specifieke extensies leren in de algemene artikelen over [Markdown](how-to-write-use-markdown.md) en [naslaginformatie over Markdown](markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="72216-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="72216-123">Markdown maakt gebruik van speciale tekens, zoals \*, \` en \# voor opmaak.</span><span class="sxs-lookup"><span data-stu-id="72216-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="72216-124">Als u een van deze tekens in uw inhoud wilt opnemen, moet u een van de volgende stappen ondernemen:</span><span class="sxs-lookup"><span data-stu-id="72216-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="72216-125">Plaats een backslash vóór een speciaal teken om deze als escape-teken te gebruiken (bijvoorbeeld `\*` vóór een \*)</span><span class="sxs-lookup"><span data-stu-id="72216-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="72216-126">Gebruik de [HTML-entiteitscode](http://www.ascii.cl/htmlcodes.htm) voor het teken (bijvoorbeeld `&#42;` vóór een &#42;).</span><span class="sxs-lookup"><span data-stu-id="72216-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="72216-127">Bestandsnamen</span><span class="sxs-lookup"><span data-stu-id="72216-127">File names</span></span>

<span data-ttu-id="72216-128">Voor bestandsnamen zijn de volgende regels van toepassing:</span><span class="sxs-lookup"><span data-stu-id="72216-128">File names use the following rules:</span></span>

* <span data-ttu-id="72216-129">Deze bevatten alleen kleine letters, cijfers en afbreekstreepjes.</span><span class="sxs-lookup"><span data-stu-id="72216-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="72216-130">Deze bevatten geen spaties of leestekens.</span><span class="sxs-lookup"><span data-stu-id="72216-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="72216-131">Deze maken gebruik van afbreekstreepjes als scheidingsteken tussen woorden en getallen in de bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="72216-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="72216-132">Gebruik specifieke actieve werkwoorden, zoals ontwikkelen, kopen, maken, problemen oplossen.</span><span class="sxs-lookup"><span data-stu-id="72216-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="72216-133">Geen onvoltooid tegenwoordige tijd.</span><span class="sxs-lookup"><span data-stu-id="72216-133">No -ing words.</span></span>
* <span data-ttu-id="72216-134">Geen kleine woorden: gebruik niet 'een', 'en', 'de', 'in', 'of', 'enz.'</span><span class="sxs-lookup"><span data-stu-id="72216-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="72216-135">De indeling moet Markdown zijn en de bestandsextensie .md.</span><span class="sxs-lookup"><span data-stu-id="72216-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="72216-136">Houd de bestandsnamen redelijk kort.</span><span class="sxs-lookup"><span data-stu-id="72216-136">Keep file names reasonably short.</span></span> <span data-ttu-id="72216-137">Deze maken deel uit van de URL voor uw artikelen.</span><span class="sxs-lookup"><span data-stu-id="72216-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="72216-138">Koppen</span><span class="sxs-lookup"><span data-stu-id="72216-138">Headings</span></span>

<span data-ttu-id="72216-139">Gebruik zinnen met hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="72216-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="72216-140">Begin het eerste woord van een koptekst altijd met een hoofdletter.</span><span class="sxs-lookup"><span data-stu-id="72216-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="72216-141">Tekststijl</span><span class="sxs-lookup"><span data-stu-id="72216-141">Text styling</span></span>

<span data-ttu-id="72216-142">*Cursief* Gebruik deze stijl voor bestanden, mappen, paden (voor lange items, op hun eigen regel gesplitst), nieuwe termen.</span><span class="sxs-lookup"><span data-stu-id="72216-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="72216-143">**Vet** Gebruik deze stijl voor elementen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="72216-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="72216-144">`Code` U kunt deze gebruiken voor inline-code, sleutelwoorden voor de taal, NuGet-pakketnamen, opdrachten in opdrachtregels, databasetabel- en kolomnamen en URL's waarvan u niet wilt dat erop geklikt kan worden.</span><span class="sxs-lookup"><span data-stu-id="72216-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="72216-145">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="72216-145">Links</span></span>

<span data-ttu-id="72216-146">Raadpleeg het algemene artikel over [Koppelingen](how-to-write-links.md) voor informatie over ankers, interne koppelingen, koppelingen naar andere documenten, insluiting van code en externe koppelingen.</span><span class="sxs-lookup"><span data-stu-id="72216-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="72216-147">Het .NET-documententeam maakt gebruik van de volgende conventies:</span><span class="sxs-lookup"><span data-stu-id="72216-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="72216-148">In de meeste gevallen gebruiken we de relatieve koppelingen en ontmoedigen het gebruik van `~/` in koppelingen, omdat relatieve koppelingen worden opgehaald in de bron op GitHub.</span><span class="sxs-lookup"><span data-stu-id="72216-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="72216-149">Steeds wanneer wij echter een koppeling maken naar een bestand in een afhankelijke opslagplaats, gebruiken wij het `~/`-teken om het pad op te geven.</span><span class="sxs-lookup"><span data-stu-id="72216-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="72216-150">Aangezien de bestanden in de afhankelijke opslagplaats zich op een andere locatie bevinden in GitHub, worden de koppelingen niet correct opgehaald met relatieve koppelingen, ongeacht de wijze waarop deze zijn geschreven.</span><span class="sxs-lookup"><span data-stu-id="72216-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="72216-151">De specificaties voor de computertaal C# en taal de Visual Basic zijn in de .NET-documenten opgenomen door de bron in te voegen vanuit de taalopslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="72216-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="72216-152">De Markdown-bronnen worden beheerd in de opslagplaatsen [csharplang](https://github.com/dotnet/csharplang) en [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="72216-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="72216-153">Koppelingen naar specificaties moeten verwijzen naar de bronmappen waarin die specificaties zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="72216-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="72216-154">Voor C# is dit **~/_csharplang/spec** en voor Visual Basic is dit **~/_vblang/spec**, zoals in het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="72216-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="72216-155">Koppelingen naar API's</span><span class="sxs-lookup"><span data-stu-id="72216-155">Links to APIs</span></span>

<span data-ttu-id="72216-156">Het build-systeem bevat enkele extensies waarmee we koppelingen kunnen maken met .NET-API's zonder externe koppelingen te hoeven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="72216-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="72216-157">U gebruikt een van de volgende typen syntaxis:</span><span class="sxs-lookup"><span data-stu-id="72216-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="72216-158">Automatisch koppelen: `<xref:UID>` of `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="72216-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="72216-159">De queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst.</span><span class="sxs-lookup"><span data-stu-id="72216-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="72216-160">Standaard toont de koppelingstekst alleen de naam van het lid of het type.</span><span class="sxs-lookup"><span data-stu-id="72216-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="72216-161">Markdown-koppeling: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="72216-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="72216-162">Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="72216-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="72216-163">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="72216-163">Examples:</span></span>

- <span data-ttu-id="72216-164">`<xref:System.String>` weergeven als [String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="72216-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="72216-165">`<xref:System.String?displayProperty=nameWithType>` weergeven als [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="72216-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="72216-166">`[String class](xref:System.String)` weergeven als [String class](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="72216-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="72216-167">Bekijk [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Kruisverwijzing gebruiken) voor meer informatie over het gebruik van deze notatie.</span><span class="sxs-lookup"><span data-stu-id="72216-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="72216-168">Bepaalde UID's bevatten de speciale tekens \`, \# of \*,waardoor de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML moet worden gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="72216-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="72216-169">U ziet soms haakjes in de code, maar dat is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="72216-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="72216-170">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="72216-170">Examples:</span></span>

- <span data-ttu-id="72216-171">System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="72216-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="72216-172">System.Exception. \#ctor wordt `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="72216-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="72216-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="72216-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="72216-174">U kunt de UID's opzoeken van typen, evenals een lijst van overbelaste leden of een bepaald overbelast lid vanuit `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="72216-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="72216-175">Via de querytekenreeks `?text=*\<type-member-name>*` wordt het type of lid geïdentificeerd waarvan of van wie de UID's zijn die u wilt zien.</span><span class="sxs-lookup"><span data-stu-id="72216-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="72216-176">Met `https://xref.docs.microsoft.com/autocomplete?text=string.format` worden bijvoorbeeld de overbelastingen ten aanzien van [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) opgehaald.</span><span class="sxs-lookup"><span data-stu-id="72216-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="72216-177">Met het hulpprogramma zoekt u naar de opgegeven queryparameter `text` ergens in de UID.</span><span class="sxs-lookup"><span data-stu-id="72216-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="72216-178">U kunt bijvoorbeeld zoeken naar de naam van het lid (ToString), een gedeelte daarvan (ToStri), de naam van het type en lid (Double.ToString) enz.</span><span class="sxs-lookup"><span data-stu-id="72216-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="72216-179">Als u een \* (of `%2A`) toevoegt na de UID, geeft de koppeling de overbelastingspagina aan en niet een specifieke API.</span><span class="sxs-lookup"><span data-stu-id="72216-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="72216-180">U kunt dat bijvoorbeeld gebruiken wanneer u op een generieke manier wilt koppelen aan de pagina [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) in plaats van specifieke overbelasting zoals [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="72216-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="72216-181">U kunt tevens met \* een koppeling maken met een lidpagina wanneer het lid niet overbelast is; zo hoeft u geen parameterlijst in de UID op te nemen.</span><span class="sxs-lookup"><span data-stu-id="72216-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="72216-182">Als u een koppeling wilt maken met een overbelasting van een specifieke methode, moet u de volledig gekwalificeerde typenaam van alle parameters van de methode opnemen.</span><span class="sxs-lookup"><span data-stu-id="72216-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="72216-183">Zo bevat \<xref:System.DateTime.ToString> een koppeling naar de parameterloze methode [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) terwijl \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> een koppeling bevat naar de methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="72216-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="72216-184">Als u een koppeling wilt maken naar een algemeen type, zoals [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), moet u het teken \` (`%60`) gebruiken, gevolgd door het aantal algemene parametertypen.</span><span class="sxs-lookup"><span data-stu-id="72216-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="72216-185">Zo bevat `<xref:System.Nullable%601>` een koppeling met het type [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), terwijl `<xref:System.Func%602>` een koppeling bevat met de gemachtigde [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="72216-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="72216-186">Code</span><span class="sxs-lookup"><span data-stu-id="72216-186">Code</span></span>

<span data-ttu-id="72216-187">De beste manier om code in te voegen is fragmenten van een werkend voorbeeld in te voegen.</span><span class="sxs-lookup"><span data-stu-id="72216-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="72216-188">Maak uw voorbeeld op basis van de instructies in het artikel [Bijdragen aan .NET](dotnet-contribute-process.md#contributing-to-samples).</span><span class="sxs-lookup"><span data-stu-id="72216-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="72216-189">De basisregels voor het invoegen van code bevinden zich in de algemene richtlijnen voor [code](how-to-write-use-markdown.md#code-includes).</span><span class="sxs-lookup"><span data-stu-id="72216-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-includes).</span></span>

<span data-ttu-id="72216-190">U kunt de code invoegen met behulp van de volgende syntaxis:</span><span class="sxs-lookup"><span data-stu-id="72216-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="72216-191">`-<language>` (*optioneel*, maar *wel aanbevolen*)</span><span class="sxs-lookup"><span data-stu-id="72216-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="72216-192">Taal van het codefragment waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="72216-192">Language of the code snippet being referenced.</span></span> <span data-ttu-id="72216-193">Zie [Ondersteunde talen](#supported-languages) voor een lijst met ondersteunde waarden.</span><span class="sxs-lookup"><span data-stu-id="72216-193">For a list of supported values, see [Supported languages](#supported-languages).</span></span>

* <span data-ttu-id="72216-194">`<name>`( *optioneel*)</span><span class="sxs-lookup"><span data-stu-id="72216-194">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="72216-195">Naam van het codefragment.</span><span class="sxs-lookup"><span data-stu-id="72216-195">Name for the code snippet.</span></span> <span data-ttu-id="72216-196">Deze heeft geen invloed op het HTML-resultaat, maar u kunt deze gebruiken om de leesbaarheid van uw Markdown-bron te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="72216-196">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="72216-197">`<pathToFile>`(*verplichte*)</span><span class="sxs-lookup"><span data-stu-id="72216-197">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="72216-198">Relatief pad naar het bestandssysteem dat het codefragmentbestand aangeeft waarnaar moet worden verwezen.</span><span class="sxs-lookup"><span data-stu-id="72216-198">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="72216-199">Dit kan ingewikkeld worden vanwege de verschillende opslagplaatsen waaruit de .NET-documentenset bestaat.</span><span class="sxs-lookup"><span data-stu-id="72216-199">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="72216-200">De .NET-voorbeelden bevinden zich in de dotnet/voorbeelden-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="72216-200">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="72216-201">Alle paden van fragmenten zouden beginnen met `~/samples`, waarbij de rest van het pad het pad naar de bron is vanuit de hoofdmap van die opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="72216-201">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="72216-202">`<queryoption>`( *optioneel*)</span><span class="sxs-lookup"><span data-stu-id="72216-202">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="72216-203">Deze worden gebruikt om op te geven hoe de code uit het bestand moet worden opgehaald:</span><span class="sxs-lookup"><span data-stu-id="72216-203">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="72216-204">`#`:  `#{tagname}` (naam van de tag) *of* `#L{startlinenumber}-L{endlinenumber}` (regelbereik).</span><span class="sxs-lookup"><span data-stu-id="72216-204">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="72216-205">Wij ontmoedigen het gebruik van regelnummers, omdat deze zeer foutgevoelig zijn.</span><span class="sxs-lookup"><span data-stu-id="72216-205">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="72216-206">Het gebruik van een tagnaam geniet de voorkeur voor de verwijzing naar codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="72216-206">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="72216-207">Gebruik zinvolle tagnamen.</span><span class="sxs-lookup"><span data-stu-id="72216-207">Use meaningful tag names.</span></span> <span data-ttu-id="72216-208">(Veel codefragmenten zijn vanuit een eerder platform gemigreerd en de tags hebben namen zoals `Snippet1`, `Snippet2` enzovoort. Die praktijk is veel moeilijker aan te houden.)</span><span class="sxs-lookup"><span data-stu-id="72216-208">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="72216-209">`range`: `?range=1,3-5` Een bereik met regels.</span><span class="sxs-lookup"><span data-stu-id="72216-209">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="72216-210">Dit voorbeeld bevat regels 1, 3, 4 en 5.</span><span class="sxs-lookup"><span data-stu-id="72216-210">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="72216-211">Wij raden aan om voor zover mogelijk de optie van tagnamen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="72216-211">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="72216-212">De tagnaam is de naam van een regio of een commentaar bij code in de in de broncode aanwezige notatie `Snippettagname`.</span><span class="sxs-lookup"><span data-stu-id="72216-212">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="72216-213">In het volgende voorbeeld is te zien hoe u kunt verwijzen naar de tagnaam `BasicThrow`:</span><span class="sxs-lookup"><span data-stu-id="72216-213">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="72216-214">Het relatieve pad naar de bron in de opslagplaats **dotnet/voorbeelden** volgt het pad `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="72216-214">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="72216-215">En u kunt zien hoe de tags van de fragmenten in [dit bronbestand](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) zijn gestructureerd.</span><span class="sxs-lookup"><span data-stu-id="72216-215">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="72216-216">Zie de [DocFX-richtlijnen](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file) voor details over weergave van tagnamen in bronbestanden van codefragmenten per taal.</span><span class="sxs-lookup"><span data-stu-id="72216-216">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="72216-217">In het volgende voorbeeld is de code te zien die in alle drie .NET-talen is ingevoegd:</span><span class="sxs-lookup"><span data-stu-id="72216-217">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="72216-218">Wanneer u fragmenten uit volledige programma's invoegt, zorgt dit ervoor dat alle code via ons CI-systeem (Continue integratie) gaat.</span><span class="sxs-lookup"><span data-stu-id="72216-218">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="72216-219">Als u echter iets moet weergeven wat voor compilatietijd- of runtimefouten zorgt, kunt u codeblokken in regels gebruiken.</span><span class="sxs-lookup"><span data-stu-id="72216-219">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="72216-220">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="72216-220">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="72216-221">Statische afbeelding of GIF-animatie</span><span class="sxs-lookup"><span data-stu-id="72216-221">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="72216-222">Gekoppelde afbeelding</span><span class="sxs-lookup"><span data-stu-id="72216-222">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="72216-223">Video's</span><span class="sxs-lookup"><span data-stu-id="72216-223">Videos</span></span>

<span data-ttu-id="72216-224">Momenteel kunt u zowel Channel 9- als YouTube-video's insluiten met de volgende syntaxis:</span><span class="sxs-lookup"><span data-stu-id="72216-224">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="72216-225">Channel 9</span><span class="sxs-lookup"><span data-stu-id="72216-225">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="72216-226">Selecteer het tabblad **Insluiten** onder het videoframe en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen.</span><span class="sxs-lookup"><span data-stu-id="72216-226">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="72216-227">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="72216-227">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="72216-228">YouTube</span><span class="sxs-lookup"><span data-stu-id="72216-228">YouTube</span></span>

<span data-ttu-id="72216-229">Klik met de rechtermuisknop op de video, selecteer **Insluitcode kopiëren** en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen.</span><span class="sxs-lookup"><span data-stu-id="72216-229">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="72216-230">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="72216-230">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="72216-231">Extensies docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="72216-231">docs.microsoft extensions</span></span>

<span data-ttu-id="72216-232">docs.microsoft biedt GitHub Flavored Markdown enkele extra extensies.</span><span class="sxs-lookup"><span data-stu-id="72216-232">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="72216-233">Gecontroleerde lijsten</span><span class="sxs-lookup"><span data-stu-id="72216-233">Checked lists</span></span>

<span data-ttu-id="72216-234">Er is een aangepaste stijl beschikbaar voor lijsten.</span><span class="sxs-lookup"><span data-stu-id="72216-234">A custom style is available for lists.</span></span> <span data-ttu-id="72216-235">U kunt lijsten met groene vinkjes renderen.</span><span class="sxs-lookup"><span data-stu-id="72216-235">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="72216-236">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="72216-236">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="72216-237">Een .NET Core-app maken</span><span class="sxs-lookup"><span data-stu-id="72216-237">How to create a .NET Core app</span></span>
> * <span data-ttu-id="72216-238">Een verwijzing toevoegen aan het pakket Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="72216-238">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="72216-239">MyApp.csproj zo bewerken dat u afhankelijkheden kunt toevoegen</span><span class="sxs-lookup"><span data-stu-id="72216-239">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="72216-240">Een klasse en een XmlSerializer toevoegen</span><span class="sxs-lookup"><span data-stu-id="72216-240">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="72216-241">De toepassing bouwen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="72216-241">How to build and run the application</span></span>

<span data-ttu-id="72216-242">U kunt in de [.NET Core-documenten](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator) een voorbeeld zien van gecontroleerde lijsten in actie.</span><span class="sxs-lookup"><span data-stu-id="72216-242">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="72216-243">Knoppen</span><span class="sxs-lookup"><span data-stu-id="72216-243">Buttons</span></span>

<span data-ttu-id="72216-244">Knopkoppelingen:</span><span class="sxs-lookup"><span data-stu-id="72216-244">Button links:</span></span>

```markdown
> [!div class="button"]
[button links](dotnet-contribute.md)
```

<span data-ttu-id="72216-245">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="72216-245">This renders as:</span></span>

> [!div class="button"]
[<span data-ttu-id="72216-246">knopkoppelingen</span><span class="sxs-lookup"><span data-stu-id="72216-246">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="72216-247">U kunt in de [Visual Studio-documenten](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio) een voorbeeld zien van knoppen in actie.</span><span class="sxs-lookup"><span data-stu-id="72216-247">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="72216-248">Stappenplannen</span><span class="sxs-lookup"><span data-stu-id="72216-248">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
[Pre](../docs/csharp/expression-trees-interpreting.md)
[Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="72216-249">U kunt in de [C#-handleiding](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure) een voorbeeld zien van stappenplannen in actie.</span><span class="sxs-lookup"><span data-stu-id="72216-249">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
