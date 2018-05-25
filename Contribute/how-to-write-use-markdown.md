---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/23/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="3dc37-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="3dc37-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="3dc37-104">Artikelen op docs.microsoft.com worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="3dc37-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="3dc37-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="3dc37-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="3dc37-106">Omdat Docs-inhoud wordt opgeslagen in GitHub, kan een hoofdverzameling van Markdown, [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), worden gebruikt. Deze biedt aanvullende functionaliteit voor algemene opmaakbehoeften.</span><span class="sxs-lookup"><span data-stu-id="3dc37-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="3dc37-107">Daarnaast wordt met OPS (Open Publishing Services) Markdig Markdown Parser geïmplementeerd,</span><span class="sxs-lookup"><span data-stu-id="3dc37-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="3dc37-108">Markdig is zeer compatibel met GitHub Flavored Markdown (GFM). Hiermee wordt aanvullende functionaliteit toegevoegd om voor Docs specifieke functies in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="3dc37-109">Markdig is een snelle, krachtige, CommonMark-compatibele, extensible Markdown-processor voor .NET.</span><span class="sxs-lookup"><span data-stu-id="3dc37-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="3dc37-110">Betere ondersteuning voor community</span><span class="sxs-lookup"><span data-stu-id="3dc37-110">Better community support</span></span>
* <span data-ttu-id="3dc37-111">Betere ondersteuning voor standaarden</span><span class="sxs-lookup"><span data-stu-id="3dc37-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="3dc37-112">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="3dc37-113">Koppen</span><span class="sxs-lookup"><span data-stu-id="3dc37-113">Headings</span></span>

<span data-ttu-id="3dc37-114">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="3dc37-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="3dc37-115">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="3dc37-115">Bold and italic text</span></span>

<span data-ttu-id="3dc37-116">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="3dc37-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="3dc37-117">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="3dc37-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="3dc37-118">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="3dc37-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="3dc37-119">Lijsten</span><span class="sxs-lookup"><span data-stu-id="3dc37-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="3dc37-120">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="3dc37-120">Unordered list</span></span>

<span data-ttu-id="3dc37-121">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3dc37-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="3dc37-122">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="3dc37-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="3dc37-123">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-123">will be rendered as:</span></span>

- <span data-ttu-id="3dc37-124">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="3dc37-124">List item 1</span></span>
- <span data-ttu-id="3dc37-125">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="3dc37-125">List item 2</span></span>
- <span data-ttu-id="3dc37-126">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="3dc37-126">List item 3</span></span>

<span data-ttu-id="3dc37-127">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3dc37-128">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="3dc37-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="3dc37-129">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-129">will be rendered as:</span></span>

- <span data-ttu-id="3dc37-130">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="3dc37-130">List item 1</span></span>
  - <span data-ttu-id="3dc37-131">Lijstitem A</span><span class="sxs-lookup"><span data-stu-id="3dc37-131">List item A</span></span>
  - <span data-ttu-id="3dc37-132">Lijstitem B</span><span class="sxs-lookup"><span data-stu-id="3dc37-132">List item B</span></span>
- <span data-ttu-id="3dc37-133">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="3dc37-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="3dc37-134">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="3dc37-134">Ordered list</span></span>

<span data-ttu-id="3dc37-135">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="3dc37-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="3dc37-136">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="3dc37-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="3dc37-137">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-137">will be rendered as:</span></span>

1. <span data-ttu-id="3dc37-138">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-138">First instruction</span></span>
2. <span data-ttu-id="3dc37-139">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-139">Second instruction</span></span>
3. <span data-ttu-id="3dc37-140">Derde instructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-140">Third instruction</span></span>

<span data-ttu-id="3dc37-141">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3dc37-142">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="3dc37-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="3dc37-143">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-143">will be rendered as:</span></span>

1. <span data-ttu-id="3dc37-144">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-144">First instruction</span></span>
    1. <span data-ttu-id="3dc37-145">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-145">Sub-instruction</span></span>
    2. <span data-ttu-id="3dc37-146">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-146">Sub-instruction</span></span>
2. <span data-ttu-id="3dc37-147">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="3dc37-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="3dc37-148">Tabellen</span><span class="sxs-lookup"><span data-stu-id="3dc37-148">Tables</span></span>

<span data-ttu-id="3dc37-149">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="3dc37-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="3dc37-150">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="3dc37-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="3dc37-151">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="3dc37-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="3dc37-152">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3dc37-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="3dc37-153">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="3dc37-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="3dc37-154">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-154">will be rendered as:</span></span>

| <span data-ttu-id="3dc37-155">Pret</span><span class="sxs-lookup"><span data-stu-id="3dc37-155">Fun</span></span>                  | <span data-ttu-id="3dc37-156">met</span><span class="sxs-lookup"><span data-stu-id="3dc37-156">With</span></span>                 | <span data-ttu-id="3dc37-157">Tabellen</span><span class="sxs-lookup"><span data-stu-id="3dc37-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="3dc37-158">links uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="3dc37-158">left-aligned column</span></span>  | <span data-ttu-id="3dc37-159">rechts uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="3dc37-159">right-aligned column</span></span> | <span data-ttu-id="3dc37-160">gecentreerde kolom</span><span class="sxs-lookup"><span data-stu-id="3dc37-160">centered column</span></span> |
| <span data-ttu-id="3dc37-161">USD 100</span><span class="sxs-lookup"><span data-stu-id="3dc37-161">$100</span></span>                 | <span data-ttu-id="3dc37-162">USD 100</span><span class="sxs-lookup"><span data-stu-id="3dc37-162">$100</span></span>                 | <span data-ttu-id="3dc37-163">USD 100</span><span class="sxs-lookup"><span data-stu-id="3dc37-163">$100</span></span>            |
| <span data-ttu-id="3dc37-164">USD 10</span><span class="sxs-lookup"><span data-stu-id="3dc37-164">$10</span></span>                  | <span data-ttu-id="3dc37-165">USD 10</span><span class="sxs-lookup"><span data-stu-id="3dc37-165">$10</span></span>                  | <span data-ttu-id="3dc37-166">USD 10</span><span class="sxs-lookup"><span data-stu-id="3dc37-166">$10</span></span>             |
| <span data-ttu-id="3dc37-167">USD 1</span><span class="sxs-lookup"><span data-stu-id="3dc37-167">$1</span></span>                   | <span data-ttu-id="3dc37-168">USD 1</span><span class="sxs-lookup"><span data-stu-id="3dc37-168">$1</span></span>                   | <span data-ttu-id="3dc37-169">USD 1</span><span class="sxs-lookup"><span data-stu-id="3dc37-169">$1</span></span>              |

<span data-ttu-id="3dc37-170">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="3dc37-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="3dc37-171">De [functie voor tabelterugloop](#table-wrapping) van Markdig biedt ondersteuning bij het opmaken van brede tabellen</span><span class="sxs-lookup"><span data-stu-id="3dc37-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="3dc37-172">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub</span><span class="sxs-lookup"><span data-stu-id="3dc37-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="3dc37-173">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="3dc37-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="3dc37-174">Referentiemateriaal voor Markdown van Adam Pritchard</span><span class="sxs-lookup"><span data-stu-id="3dc37-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="3dc37-175">Markdown Extra van Michel Fortin</span><span class="sxs-lookup"><span data-stu-id="3dc37-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="3dc37-176">HTML-tabellen naar Markdown converteren</span><span class="sxs-lookup"><span data-stu-id="3dc37-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="3dc37-177">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="3dc37-177">Links</span></span>

<span data-ttu-id="3dc37-178">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="3dc37-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="3dc37-179">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="3dc37-179">For more information on linking, see:</span></span>

- <span data-ttu-id="3dc37-180">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="3dc37-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="3dc37-181">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.</span><span class="sxs-lookup"><span data-stu-id="3dc37-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="3dc37-182">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="3dc37-182">Code snippets</span></span>

<span data-ttu-id="3dc37-183">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="3dc37-184">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="3dc37-184">For details, see:</span></span>

- [<span data-ttu-id="3dc37-185">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="3dc37-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="3dc37-186">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="3dc37-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="3dc37-187">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="3dc37-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="3dc37-188">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="3dc37-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="3dc37-189">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3dc37-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="3dc37-190">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="3dc37-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="3dc37-191">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="3dc37-192">Naam</span><span class="sxs-lookup"><span data-stu-id="3dc37-192">Name</span></span>|<span data-ttu-id="3dc37-193">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="3dc37-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="3dc37-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="3dc37-194">.NET Console</span></span>|<span data-ttu-id="3dc37-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="3dc37-195">dotnetcli</span></span>|
|<span data-ttu-id="3dc37-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="3dc37-196">ASP.NET (C#)</span></span>|<span data-ttu-id="3dc37-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="3dc37-197">aspx-csharp</span></span>|
|<span data-ttu-id="3dc37-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="3dc37-198">ASP.NET (VB)</span></span>|<span data-ttu-id="3dc37-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="3dc37-199">aspx-vb</span></span>|
|<span data-ttu-id="3dc37-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="3dc37-200">AzCopy</span></span>|<span data-ttu-id="3dc37-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="3dc37-201">azcopy</span></span>|
|<span data-ttu-id="3dc37-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="3dc37-202">Azure CLI</span></span>|<span data-ttu-id="3dc37-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="3dc37-203">azurecli</span></span>|
|<span data-ttu-id="3dc37-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3dc37-204">Azure PowerShell</span></span>|<span data-ttu-id="3dc37-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="3dc37-205">azurepowershell</span></span>|
|<span data-ttu-id="3dc37-206">C++</span><span class="sxs-lookup"><span data-stu-id="3dc37-206">C++</span></span>|<span data-ttu-id="3dc37-207">cpp</span><span class="sxs-lookup"><span data-stu-id="3dc37-207">cpp</span></span>|
|<span data-ttu-id="3dc37-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="3dc37-208">C++/CX</span></span>|<span data-ttu-id="3dc37-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="3dc37-209">cppcx</span></span>|
|<span data-ttu-id="3dc37-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3dc37-210">C++/WinRT</span></span>|<span data-ttu-id="3dc37-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="3dc37-211">cppwinrt</span></span>|
|<span data-ttu-id="3dc37-212">C#</span><span class="sxs-lookup"><span data-stu-id="3dc37-212">C#</span></span>|<span data-ttu-id="3dc37-213">csharp</span><span class="sxs-lookup"><span data-stu-id="3dc37-213">csharp</span></span>|
|<span data-ttu-id="3dc37-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="3dc37-214">CSHTML</span></span>|<span data-ttu-id="3dc37-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="3dc37-215">cshtml</span></span>|
|<span data-ttu-id="3dc37-216">DAX</span><span class="sxs-lookup"><span data-stu-id="3dc37-216">DAX</span></span>|<span data-ttu-id="3dc37-217">dax</span><span class="sxs-lookup"><span data-stu-id="3dc37-217">dax</span></span>|
|<span data-ttu-id="3dc37-218">F#</span><span class="sxs-lookup"><span data-stu-id="3dc37-218">F#</span></span>|<span data-ttu-id="3dc37-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="3dc37-219">fsharp</span></span>|
|<span data-ttu-id="3dc37-220">Go</span><span class="sxs-lookup"><span data-stu-id="3dc37-220">Go</span></span>|<span data-ttu-id="3dc37-221">go</span><span class="sxs-lookup"><span data-stu-id="3dc37-221">go</span></span>|
|<span data-ttu-id="3dc37-222">HTML</span><span class="sxs-lookup"><span data-stu-id="3dc37-222">HTML</span></span>|<span data-ttu-id="3dc37-223">html</span><span class="sxs-lookup"><span data-stu-id="3dc37-223">html</span></span>|
|<span data-ttu-id="3dc37-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="3dc37-224">HTTP</span></span>|<span data-ttu-id="3dc37-225">http</span><span class="sxs-lookup"><span data-stu-id="3dc37-225">http</span></span>|
|<span data-ttu-id="3dc37-226">Java</span><span class="sxs-lookup"><span data-stu-id="3dc37-226">Java</span></span>|<span data-ttu-id="3dc37-227">java</span><span class="sxs-lookup"><span data-stu-id="3dc37-227">java</span></span>|
|<span data-ttu-id="3dc37-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="3dc37-228">JavaScript</span></span>|<span data-ttu-id="3dc37-229">javascript</span><span class="sxs-lookup"><span data-stu-id="3dc37-229">javascript</span></span>|
|<span data-ttu-id="3dc37-230">JSON</span><span class="sxs-lookup"><span data-stu-id="3dc37-230">JSON</span></span>|<span data-ttu-id="3dc37-231">json</span><span class="sxs-lookup"><span data-stu-id="3dc37-231">json</span></span>|
|<span data-ttu-id="3dc37-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-232">Markdown</span></span>|<span data-ttu-id="3dc37-233">md</span><span class="sxs-lookup"><span data-stu-id="3dc37-233">md</span></span>|
|<span data-ttu-id="3dc37-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="3dc37-234">NodeJS</span></span>|<span data-ttu-id="3dc37-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="3dc37-235">nodejs</span></span>|
|<span data-ttu-id="3dc37-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="3dc37-236">Objective-C</span></span>|<span data-ttu-id="3dc37-237">objc</span><span class="sxs-lookup"><span data-stu-id="3dc37-237">objc</span></span>|
|<span data-ttu-id="3dc37-238">OData</span><span class="sxs-lookup"><span data-stu-id="3dc37-238">OData</span></span>|<span data-ttu-id="3dc37-239">odata</span><span class="sxs-lookup"><span data-stu-id="3dc37-239">odata</span></span>|
|<span data-ttu-id="3dc37-240">PHP</span><span class="sxs-lookup"><span data-stu-id="3dc37-240">PHP</span></span>|<span data-ttu-id="3dc37-241">php</span><span class="sxs-lookup"><span data-stu-id="3dc37-241">php</span></span>|
|<span data-ttu-id="3dc37-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="3dc37-242">Power Apps Formula</span></span>|<span data-ttu-id="3dc37-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="3dc37-243">powerappsfl</span></span>|
|<span data-ttu-id="3dc37-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3dc37-244">PowerShell</span></span>|<span data-ttu-id="3dc37-245">powershell</span><span class="sxs-lookup"><span data-stu-id="3dc37-245">powershell</span></span>|
|<span data-ttu-id="3dc37-246">Python</span><span class="sxs-lookup"><span data-stu-id="3dc37-246">Python</span></span>|<span data-ttu-id="3dc37-247">python</span><span class="sxs-lookup"><span data-stu-id="3dc37-247">python</span></span>|
|<span data-ttu-id="3dc37-248">Q#</span><span class="sxs-lookup"><span data-stu-id="3dc37-248">Q#</span></span>|<span data-ttu-id="3dc37-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="3dc37-249">qsharp</span></span>|
|<span data-ttu-id="3dc37-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="3dc37-250">Ruby</span></span>|<span data-ttu-id="3dc37-251">ruby</span><span class="sxs-lookup"><span data-stu-id="3dc37-251">ruby</span></span>|
|<span data-ttu-id="3dc37-252">SQL</span><span class="sxs-lookup"><span data-stu-id="3dc37-252">SQL</span></span>|<span data-ttu-id="3dc37-253">sql</span><span class="sxs-lookup"><span data-stu-id="3dc37-253">sql</span></span>|
|<span data-ttu-id="3dc37-254">Swift</span><span class="sxs-lookup"><span data-stu-id="3dc37-254">Swift</span></span>|<span data-ttu-id="3dc37-255">swift</span><span class="sxs-lookup"><span data-stu-id="3dc37-255">swift</span></span>|
|<span data-ttu-id="3dc37-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="3dc37-256">TypeScript</span></span>|<span data-ttu-id="3dc37-257">typescript</span><span class="sxs-lookup"><span data-stu-id="3dc37-257">typescript</span></span>|
|<span data-ttu-id="3dc37-258">VB</span><span class="sxs-lookup"><span data-stu-id="3dc37-258">VB</span></span>|<span data-ttu-id="3dc37-259">vb</span><span class="sxs-lookup"><span data-stu-id="3dc37-259">vb</span></span>|
|<span data-ttu-id="3dc37-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="3dc37-260">VSTS CLI</span></span>|<span data-ttu-id="3dc37-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="3dc37-261">vstscli</span></span>|
|<span data-ttu-id="3dc37-262">XAML</span><span class="sxs-lookup"><span data-stu-id="3dc37-262">XAML</span></span>|<span data-ttu-id="3dc37-263">xaml</span><span class="sxs-lookup"><span data-stu-id="3dc37-263">xaml</span></span>|
|<span data-ttu-id="3dc37-264">XML</span><span class="sxs-lookup"><span data-stu-id="3dc37-264">XML</span></span>|<span data-ttu-id="3dc37-265">xml</span><span class="sxs-lookup"><span data-stu-id="3dc37-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="3dc37-266">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="3dc37-266">Example: C\#</span></span>

<span data-ttu-id="3dc37-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3dc37-267">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="3dc37-268">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="3dc37-268">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="3dc37-269">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="3dc37-269">Example: SQL</span></span>

<span data-ttu-id="3dc37-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3dc37-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="3dc37-271">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="3dc37-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="3dc37-272">Aangepaste OPS-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="3dc37-273">Met OPS (Open Publishing Services) wordt Markdig Parser for Markdown geïmplementeerd, dat zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="3dc37-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="3dc37-274">Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="3dc37-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="3dc37-275">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="3dc37-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="3dc37-276">(Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="3dc37-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="3dc37-277">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="3dc37-278">Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="3dc37-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="3dc37-279">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="3dc37-279">Note blocks</span></span>
- <span data-ttu-id="3dc37-280">Omvat</span><span class="sxs-lookup"><span data-stu-id="3dc37-280">Includes</span></span>
- <span data-ttu-id="3dc37-281">Selectors</span><span class="sxs-lookup"><span data-stu-id="3dc37-281">Selectors</span></span>
- <span data-ttu-id="3dc37-282">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="3dc37-282">Embedded videos</span></span>
- <span data-ttu-id="3dc37-283">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="3dc37-283">Code snippets/samples</span></span>

<span data-ttu-id="3dc37-284">Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="3dc37-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="3dc37-285">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="3dc37-285">Note blocks</span></span>

<span data-ttu-id="3dc37-286">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="3dc37-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="3dc37-287">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="3dc37-287">NOTE</span></span>
- <span data-ttu-id="3dc37-288">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="3dc37-288">WARNING</span></span>
- <span data-ttu-id="3dc37-289">TIP</span><span class="sxs-lookup"><span data-stu-id="3dc37-289">TIP</span></span>
- <span data-ttu-id="3dc37-290">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="3dc37-290">IMPORTANT</span></span>

<span data-ttu-id="3dc37-291">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="3dc37-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="3dc37-292">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="3dc37-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="3dc37-293">Omvat</span><span class="sxs-lookup"><span data-stu-id="3dc37-293">Includes</span></span>

<span data-ttu-id="3dc37-294">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="3dc37-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="3dc37-295">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="3dc37-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="3dc37-296">Er zijn drie soorten insluitingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="3dc37-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="3dc37-297">Inline: een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="3dc37-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="3dc37-298">Blok: een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="3dc37-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="3dc37-299">Afbeelding: op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="3dc37-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="3dc37-300">Een inline- of blokinsluiting is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="3dc37-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="3dc37-301">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="3dc37-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="3dc37-302">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3dc37-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="3dc37-303">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="3dc37-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="3dc37-304">Dit zijn de vereisten en overwegingen voor insluitingen:</span><span class="sxs-lookup"><span data-stu-id="3dc37-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="3dc37-305">Gebruik insluitingen wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3dc37-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="3dc37-306">Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="3dc37-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="3dc37-307">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="3dc37-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="3dc37-308">Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van Markdig-extensies.</span><span class="sxs-lookup"><span data-stu-id="3dc37-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="3dc37-309">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="3dc37-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="3dc37-310">Zorg ervoor dat de tekst in een insluiting uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="3dc37-311">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="3dc37-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="3dc37-312">Voeg geen insluitingen in andere insluitingen in.</span><span class="sxs-lookup"><span data-stu-id="3dc37-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="3dc37-313">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="3dc37-313">They are not supported.</span></span>
- <span data-ttu-id="3dc37-314">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="3dc37-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="3dc37-315">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="3dc37-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="3dc37-316">Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3dc37-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="3dc37-317">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="3dc37-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="3dc37-318">Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel.</span><span class="sxs-lookup"><span data-stu-id="3dc37-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="3dc37-319">Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.</span><span class="sxs-lookup"><span data-stu-id="3dc37-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="3dc37-320">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.</span><span class="sxs-lookup"><span data-stu-id="3dc37-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="3dc37-321">Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="3dc37-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="3dc37-322">Selectors</span><span class="sxs-lookup"><span data-stu-id="3dc37-322">Selectors</span></span>

<span data-ttu-id="3dc37-323">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of platformen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="3dc37-324">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="3dc37-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="3dc37-325">Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="3dc37-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="3dc37-326">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluiting.</span><span class="sxs-lookup"><span data-stu-id="3dc37-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="3dc37-327">Deze kan vervolgens naar deze insluiting verwijzen in alle onderwerpen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3dc37-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="3dc37-328">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="3dc37-328">Code snippets</span></span>

<span data-ttu-id="3dc37-329">Markdig ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="3dc37-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="3dc37-330">Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:</span><span class="sxs-lookup"><span data-stu-id="3dc37-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="3dc37-331">Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3dc37-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="3dc37-332">Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="3dc37-333">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="3dc37-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="3dc37-334">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="3dc37-334">Alt text</span></span>

<span data-ttu-id="3dc37-335">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3dc37-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="3dc37-336">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="3dc37-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="3dc37-337">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="3dc37-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="3dc37-338">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="3dc37-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="3dc37-339">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="3dc37-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="3dc37-340">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="3dc37-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="3dc37-341">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="3dc37-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="3dc37-342">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="3dc37-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="3dc37-343">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="3dc37-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="3dc37-344">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="3dc37-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="3dc37-345">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="3dc37-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="3dc37-346">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="3dc37-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="3dc37-347">Punthaken</span><span class="sxs-lookup"><span data-stu-id="3dc37-347">Angle brackets</span></span>

<span data-ttu-id="3dc37-348">Als u in lopende tekst (geen code) punthaken gebruikt, bijvoorbeeld om een tijdelijke aanduiding aan te geven, moet u de punthaken handmatig coderen.</span><span class="sxs-lookup"><span data-stu-id="3dc37-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="3dc37-349">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="3dc37-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="3dc37-350">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="3dc37-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="3dc37-351">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3dc37-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="3dc37-352">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="3dc37-352">Markdown resources</span></span>

- [<span data-ttu-id="3dc37-353">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="3dc37-354">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="3dc37-355">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="3dc37-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
