---
title: Sjabloon en cheatsheet voor .NET-artikelen
description: Dit artikel bevat een handige sjabloon waarmee u nieuwe artikelen kunt maken voor opslagplaatsen voor .NET-documenten
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 15288ccb1831e994fd078f47788ad4c2f502775c
ms.sourcegitcommit: 92d06515af1d9d0e5abf632fc3b6425c487174d5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90837207"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="07365-103">Sjabloon voor metagegevens en Markdown voor .NET-documenten</span><span class="sxs-lookup"><span data-stu-id="07365-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="07365-104">Deze dotnet/docs-sjabloon bevat voorbeelden van Markdown-syntaxis en aanwijzingen voor het instellen van metagegevens.</span><span class="sxs-lookup"><span data-stu-id="07365-104">This dotnet/docs template contains examples of Markdown syntax and guidance on setting the metadata.</span></span>

<span data-ttu-id="07365-105">Wanneer u een Markdown-bestand maakt, moet u de opgenomen sjabloon naar een nieuw bestand kopiëren, de metagegevens invullen zoals hierna is aangegeven en de kop H1 boven de titel van het artikel zetten.</span><span class="sxs-lookup"><span data-stu-id="07365-105">When creating a Markdown file, copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="07365-106">Metagegevens</span><span class="sxs-lookup"><span data-stu-id="07365-106">Metadata</span></span>

<span data-ttu-id="07365-107">Het vereiste blok met metagegevens bevindt zich in het volgende voorbeeldblok met metagegevens:</span><span class="sxs-lookup"><span data-stu-id="07365-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="07365-108">Tussen de dubbele punt (:) en de waarde van een metagegevenselement **moet** een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="07365-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="07365-109">Dubbele punten in een waarde (zoals een titel) verbreken de metagegevensparser.</span><span class="sxs-lookup"><span data-stu-id="07365-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="07365-110">Omring in dit geval de titel met dubbele aanhalingstekens (bijvoorbeeld `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="07365-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="07365-111">**titel**: Deze wordt in zoekprogrammaresultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="07365-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="07365-112">De titel mag niet identiek zijn aan de titel in uw kop H1 en moet maximaal 60 tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="07365-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="07365-113">**beschrijving**: Hierin wordt de inhoud van het artikel samengevat.</span><span class="sxs-lookup"><span data-stu-id="07365-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="07365-114">Deze wordt meestal in de pagina met zoekresultaten weergegeven, maar wordt niet gebruikt voor de rangschikking van de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="07365-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="07365-115">De lengte dient 115 tot 145 tekens te bedragen, inclusief spaties.</span><span class="sxs-lookup"><span data-stu-id="07365-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="07365-116">**auteur**: Het veld Auteur moet de **GitHub-gebruikersnaam** van de auteur bevatten.</span><span class="sxs-lookup"><span data-stu-id="07365-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="07365-117">**ms.date**: De datum van de laatste belangrijke update.</span><span class="sxs-lookup"><span data-stu-id="07365-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="07365-118">Werk deze bij voor bestaande artikelen als u het gehele artikel hebt bekeken en bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="07365-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="07365-119">Kleine aanpassingen, zoals typfouten e.d., rechtvaardigen geen update.</span><span class="sxs-lookup"><span data-stu-id="07365-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="07365-120">Er zijn andere metagegevens aan elk artikel toegevoegd, maar wij passen gewoonlijk de meeste metagegevenswaarden toe op mapniveau, zoals is opgegeven in **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="07365-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="07365-121">Elementaire Markdown, GFM en speciale tekens</span><span class="sxs-lookup"><span data-stu-id="07365-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="07365-122">U kunt de basisbeginselen van Markdown, GitHub Flavored Markdown (GFM) en OPS-specifieke extensies leren in het artikel [Markdown-naslaginformatie](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="07365-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS-specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="07365-123">Markdown maakt gebruik van speciale tekens, zoals \*, \` en \# voor opmaak.</span><span class="sxs-lookup"><span data-stu-id="07365-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="07365-124">Als u een van deze tekens in uw inhoud wilt opnemen, moet u een van de volgende stappen ondernemen:</span><span class="sxs-lookup"><span data-stu-id="07365-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="07365-125">Plaats een backslash vóór een speciaal teken om deze als escape-teken te gebruiken (bijvoorbeeld `\*` voor een \*).</span><span class="sxs-lookup"><span data-stu-id="07365-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*).</span></span>
- <span data-ttu-id="07365-126">Gebruik de [HTML-entiteitscode](http://www.ascii.cl/htmlcodes.htm) voor het teken (bijvoorbeeld `&#42;` vóór een &#42;).</span><span class="sxs-lookup"><span data-stu-id="07365-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="07365-127">Bestandsnamen</span><span class="sxs-lookup"><span data-stu-id="07365-127">File names</span></span>

<span data-ttu-id="07365-128">Voor bestandsnamen zijn de volgende regels van toepassing:</span><span class="sxs-lookup"><span data-stu-id="07365-128">File names use the following rules:</span></span>

* <span data-ttu-id="07365-129">Deze bevatten alleen kleine letters, cijfers en afbreekstreepjes.</span><span class="sxs-lookup"><span data-stu-id="07365-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="07365-130">Deze bevatten geen spaties of leestekens.</span><span class="sxs-lookup"><span data-stu-id="07365-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="07365-131">Deze maken gebruik van afbreekstreepjes als scheidingsteken tussen woorden en getallen in de bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="07365-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="07365-132">Gebruik specifieke actieve werkwoorden, zoals ontwikkelen, kopen, maken, problemen oplossen.</span><span class="sxs-lookup"><span data-stu-id="07365-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="07365-133">Geen onvoltooid tegenwoordige tijd.</span><span class="sxs-lookup"><span data-stu-id="07365-133">No -ing words.</span></span>
* <span data-ttu-id="07365-134">Geen kleine woorden: gebruik niet 'een', 'en', 'de', 'in', 'of', 'enz.'</span><span class="sxs-lookup"><span data-stu-id="07365-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="07365-135">De indeling moet Markdown zijn en de bestandsextensie .md.</span><span class="sxs-lookup"><span data-stu-id="07365-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="07365-136">Houd de bestandsnamen redelijk kort.</span><span class="sxs-lookup"><span data-stu-id="07365-136">Keep file names reasonably short.</span></span> <span data-ttu-id="07365-137">Deze maken deel uit van de URL voor uw artikelen.</span><span class="sxs-lookup"><span data-stu-id="07365-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="07365-138">Koppen</span><span class="sxs-lookup"><span data-stu-id="07365-138">Headings</span></span>

<span data-ttu-id="07365-139">Gebruik zinnen met hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="07365-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="07365-140">Begin het eerste woord van een koptekst altijd met een hoofdletter.</span><span class="sxs-lookup"><span data-stu-id="07365-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="07365-141">Tekststijl</span><span class="sxs-lookup"><span data-stu-id="07365-141">Text styling</span></span>

<span data-ttu-id="07365-142">*Cursief*</span><span class="sxs-lookup"><span data-stu-id="07365-142">*Italics*</span></span>\
<span data-ttu-id="07365-143">Gebruik deze stijl voor bestanden, mappen, paden (voor lange items, op hun eigen regel gesplitst), nieuwe termen.</span><span class="sxs-lookup"><span data-stu-id="07365-143">Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="07365-144">**Vet**</span><span class="sxs-lookup"><span data-stu-id="07365-144">**Bold**</span></span>\
<span data-ttu-id="07365-145">Gebruik deze stijl voor elementen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="07365-145">Use for UI elements.</span></span>

`Code`\
<span data-ttu-id="07365-146">U kunt deze stijl gebruiken voor inline-code, sleutelwoorden voor de taal, NuGet-pakketnamen, opdrachten in opdrachtregels, databasetabel- en kolomnamen en URL's waarvan u niet wilt dat erop kan worden geklikt.</span><span class="sxs-lookup"><span data-stu-id="07365-146">Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="07365-147">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="07365-147">Links</span></span>

<span data-ttu-id="07365-148">Raadpleeg het algemene artikel over [Koppelingen](../how-to-write-links.md) voor informatie over ankers, interne koppelingen, koppelingen naar andere documenten, insluiting van code en externe koppelingen.</span><span class="sxs-lookup"><span data-stu-id="07365-148">See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="07365-149">Het .NET-documententeam maakt gebruik van de volgende conventies:</span><span class="sxs-lookup"><span data-stu-id="07365-149">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="07365-150">In de meeste gevallen gebruiken we de relatieve koppelingen en ontmoedigen het gebruik van `~/` in koppelingen, omdat relatieve koppelingen worden opgehaald in de bron op GitHub.</span><span class="sxs-lookup"><span data-stu-id="07365-150">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="07365-151">Wanneer we echter een koppeling maken naar een bestand in een afhankelijke opslagplaats, gebruiken we het `~/`-teken om het pad op te geven.</span><span class="sxs-lookup"><span data-stu-id="07365-151">However, whenever we link to a file in a dependent repo, we use the `~/` character to provide the path.</span></span> <span data-ttu-id="07365-152">Aangezien de bestanden in de afhankelijke opslagplaats zich op een andere locatie bevinden in GitHub, worden de koppelingen niet correct opgehaald met relatieve koppelingen, ongeacht de wijze waarop deze zijn geschreven.</span><span class="sxs-lookup"><span data-stu-id="07365-152">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="07365-153">De specificaties voor de computertaal C# en taal de Visual Basic zijn in de .NET-documenten opgenomen door de bron in te voegen vanuit de taalopslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="07365-153">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="07365-154">De Markdown-bronnen worden beheerd in de opslagplaatsen [csharplang](https://github.com/dotnet/csharplang) en [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="07365-154">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="07365-155">Koppelingen naar specificaties moeten verwijzen naar de bronmappen waarin die specificaties zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="07365-155">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="07365-156">Voor C# is dit **~/_csharplang/spec** en voor Visual Basic is dit **~/_vblang/spec**, zoals in het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="07365-156">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="07365-157">Koppelingen naar API's</span><span class="sxs-lookup"><span data-stu-id="07365-157">Links to APIs</span></span>

<span data-ttu-id="07365-158">Het build-systeem bevat enkele extensies waarmee we koppelingen kunnen maken met .NET-API's zonder externe koppelingen te hoeven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="07365-158">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="07365-159">U gebruikt een van de volgende typen syntaxis:</span><span class="sxs-lookup"><span data-stu-id="07365-159">You use one of the following syntax:</span></span>

1. <span data-ttu-id="07365-160">Automatisch koppelen: `<xref:UID>` of `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="07365-160">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="07365-161">De queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst.</span><span class="sxs-lookup"><span data-stu-id="07365-161">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="07365-162">Standaard toont de koppelingstekst alleen de naam van het lid of het type.</span><span class="sxs-lookup"><span data-stu-id="07365-162">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="07365-163">Markdown-koppeling: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="07365-163">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="07365-164">Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="07365-164">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="07365-165">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="07365-165">Examples:</span></span>

- <span data-ttu-id="07365-166">`<xref:System.String>` weergeven als [String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="07365-166">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="07365-167">`<xref:System.String?displayProperty=nameWithType>` weergeven als [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="07365-167">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="07365-168">`[String class](xref:System.String)` weergeven als [String class](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="07365-168">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="07365-169">Bekijk [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Kruisverwijzing gebruiken) voor meer informatie over het gebruik van deze notatie.</span><span class="sxs-lookup"><span data-stu-id="07365-169">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="07365-170">Bepaalde UID's bevatten de speciale tekens \`, \# of \*,waardoor de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML moet worden gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="07365-170">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="07365-171">U ziet soms haakjes in de code, maar dat is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="07365-171">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="07365-172">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="07365-172">Examples:</span></span>

- <span data-ttu-id="07365-173">System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="07365-173">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="07365-174">System.Exception. \#ctor wordt `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="07365-174">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="07365-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="07365-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="07365-176">U kunt de UID's opzoeken van typen, evenals een lijst van overbelaste leden of een bepaald overbelast lid vanuit `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="07365-176">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="07365-177">Via de querytekenreeks `?text=*\<type-member-name>*` wordt het type of lid geïdentificeerd waarvan of van wie de UID's zijn die u wilt zien.</span><span class="sxs-lookup"><span data-stu-id="07365-177">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="07365-178">Met `https://xref.docs.microsoft.com/autocomplete?text=string.format` worden bijvoorbeeld de overbelastingen ten aanzien van [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) opgehaald.</span><span class="sxs-lookup"><span data-stu-id="07365-178">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="07365-179">Met het hulpprogramma zoekt u naar de opgegeven queryparameter `text` ergens in de UID.</span><span class="sxs-lookup"><span data-stu-id="07365-179">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="07365-180">U kunt bijvoorbeeld zoeken naar de naam van het lid (ToString), een gedeelte daarvan (ToStri), de naam van het type en lid (Double.ToString) enz.</span><span class="sxs-lookup"><span data-stu-id="07365-180">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="07365-181">Als u een \* (of `%2A`) toevoegt na de UID, geeft de koppeling de overbelastingspagina aan en niet een specifieke API.</span><span class="sxs-lookup"><span data-stu-id="07365-181">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="07365-182">U kunt dat bijvoorbeeld gebruiken wanneer u op een generieke manier wilt koppelen aan de pagina [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) in plaats van specifieke overbelasting zoals [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="07365-182">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="07365-183">U kunt tevens met \* een koppeling maken met een lidpagina wanneer het lid niet overbelast is; zo hoeft u geen parameterlijst in de UID op te nemen.</span><span class="sxs-lookup"><span data-stu-id="07365-183">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="07365-184">Als u een koppeling wilt maken met een overbelasting van een specifieke methode, moet u de volledig gekwalificeerde typenaam van alle parameters van de methode opnemen.</span><span class="sxs-lookup"><span data-stu-id="07365-184">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="07365-185">Zo wordt \<xref:System.DateTime.ToString> gekoppeld aan de parameterloze methode [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), terwijl \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> wordt gekoppeld aan de methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="07365-185">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="07365-186">Als u een koppeling wilt maken naar een algemeen type, zoals [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), moet u het teken \` (`%60`) gebruiken, gevolgd door het aantal algemene parametertypen.</span><span class="sxs-lookup"><span data-stu-id="07365-186">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="07365-187">Zo bevat `<xref:System.Nullable%601>` een koppeling met het type [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), terwijl `<xref:System.Func%602>` een koppeling bevat met de gemachtigde [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="07365-187">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="07365-188">Code</span><span class="sxs-lookup"><span data-stu-id="07365-188">Code</span></span>

<span data-ttu-id="07365-189">De beste manier om code in te voegen is fragmenten van een werkend voorbeeld in te voegen.</span><span class="sxs-lookup"><span data-stu-id="07365-189">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="07365-190">Maak uw voorbeeld op basis van de instructies in het artikel [Bijdragen aan .NET](dotnet-contribute.md#contribute-to-samples).</span><span class="sxs-lookup"><span data-stu-id="07365-190">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contribute-to-samples) article.</span></span> <span data-ttu-id="07365-191">Wanneer u fragmenten uit volledige programma's invoegt, zorgt dit ervoor dat alle code via ons CI-systeem (Continue integratie) gaat.</span><span class="sxs-lookup"><span data-stu-id="07365-191">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="07365-192">Als u echter iets moet weergeven wat voor compilatietijd- of runtimefouten zorgt, kunt u codeblokken in regels gebruiken.</span><span class="sxs-lookup"><span data-stu-id="07365-192">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

<span data-ttu-id="07365-193">Voor meer informatie over de Markdown-syntaxis om code in docs weer te geven, raadpleegt u [Code in opnemen in docs-artikelen](../code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="07365-193">For information about the Markdown syntax for showing code in docs, see [How to include code in docs](../code-in-docs.md).</span></span>

## <a name="images"></a><span data-ttu-id="07365-194">Afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="07365-194">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="07365-195">Statische afbeelding of GIF-animatie</span><span class="sxs-lookup"><span data-stu-id="07365-195">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="07365-196">Gekoppelde afbeelding</span><span class="sxs-lookup"><span data-stu-id="07365-196">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="07365-197">Video's</span><span class="sxs-lookup"><span data-stu-id="07365-197">Videos</span></span>

<span data-ttu-id="07365-198">Momenteel kunt u zowel Channel 9- als YouTube-video's insluiten met de volgende syntaxis:</span><span class="sxs-lookup"><span data-stu-id="07365-198">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="07365-199">Channel 9</span><span class="sxs-lookup"><span data-stu-id="07365-199">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="07365-200">Selecteer het tabblad **Insluiten** onder het videoframe en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen.</span><span class="sxs-lookup"><span data-stu-id="07365-200">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="07365-201">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="07365-201">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="07365-202">YouTube</span><span class="sxs-lookup"><span data-stu-id="07365-202">YouTube</span></span>

<span data-ttu-id="07365-203">Klik met de rechtermuisknop op de video, selecteer **Insluitcode kopiëren** en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen.</span><span class="sxs-lookup"><span data-stu-id="07365-203">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="07365-204">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="07365-204">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="07365-205">Extensies docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="07365-205">docs.microsoft extensions</span></span>

<span data-ttu-id="07365-206">docs.microsoft biedt GitHub Flavored Markdown enkele extra extensies.</span><span class="sxs-lookup"><span data-stu-id="07365-206">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="07365-207">Gecontroleerde lijsten</span><span class="sxs-lookup"><span data-stu-id="07365-207">Checked lists</span></span>

<span data-ttu-id="07365-208">Er is een aangepaste stijl beschikbaar voor lijsten.</span><span class="sxs-lookup"><span data-stu-id="07365-208">A custom style is available for lists.</span></span> <span data-ttu-id="07365-209">U kunt lijsten met groene vinkjes renderen.</span><span class="sxs-lookup"><span data-stu-id="07365-209">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="07365-210">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="07365-210">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="07365-211">Een .NET Core-app maken</span><span class="sxs-lookup"><span data-stu-id="07365-211">How to create a .NET Core app</span></span>
> * <span data-ttu-id="07365-212">Een verwijzing toevoegen aan het pakket Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="07365-212">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="07365-213">MyApp.csproj zo bewerken dat u afhankelijkheden kunt toevoegen</span><span class="sxs-lookup"><span data-stu-id="07365-213">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="07365-214">Een klasse en een XmlSerializer toevoegen</span><span class="sxs-lookup"><span data-stu-id="07365-214">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="07365-215">De toepassing bouwen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="07365-215">How to build and run the application</span></span>

<span data-ttu-id="07365-216">U kunt in de [.NET Core-documenten](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator) een voorbeeld zien van gecontroleerde lijsten in actie.</span><span class="sxs-lookup"><span data-stu-id="07365-216">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="07365-217">Knoppen</span><span class="sxs-lookup"><span data-stu-id="07365-217">Buttons</span></span>

<span data-ttu-id="07365-218">Knopkoppelingen:</span><span class="sxs-lookup"><span data-stu-id="07365-218">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="07365-219">Dit wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="07365-219">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="07365-220">knopkoppelingen</span><span class="sxs-lookup"><span data-stu-id="07365-220">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="07365-221">U kunt in de [Visual Studio-documenten](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio) een voorbeeld zien van knoppen in actie.</span><span class="sxs-lookup"><span data-stu-id="07365-221">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="07365-222">Stappenplannen</span><span class="sxs-lookup"><span data-stu-id="07365-222">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="07365-223">U kunt in de [C#-handleiding](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure) een voorbeeld zien van stappenplannen in actie.</span><span class="sxs-lookup"><span data-stu-id="07365-223">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
