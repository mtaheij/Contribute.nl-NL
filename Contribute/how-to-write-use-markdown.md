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
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="88f3d-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="88f3d-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="88f3d-104">Artikelen op docs.microsoft.com worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="88f3d-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="88f3d-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="88f3d-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="88f3d-106">Omdat Docs-inhoud wordt opgeslagen in GitHub, kan een hoofdverzameling van Markdown, [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), worden gebruikt. Deze biedt aanvullende functionaliteit voor algemene opmaakbehoeften.</span><span class="sxs-lookup"><span data-stu-id="88f3d-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="88f3d-107">Daarnaast wordt met OPS (Open Publishing Services) DFM (DocFX Flavored Markdown) geïmplementeerd,</span><span class="sxs-lookup"><span data-stu-id="88f3d-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="88f3d-108">dat zeer compatibel is met GitHub Flavored Markdown (GFM). Hiermee wordt aanvullende functionaliteit toegevoegd om voor Docs specifieke functies in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="88f3d-109">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="88f3d-110">Koppen</span><span class="sxs-lookup"><span data-stu-id="88f3d-110">Headings</span></span>

<span data-ttu-id="88f3d-111">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="88f3d-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="88f3d-112">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="88f3d-112">Bold and italic text</span></span>

<span data-ttu-id="88f3d-113">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="88f3d-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="88f3d-114">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="88f3d-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="88f3d-115">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="88f3d-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="88f3d-116">Lijsten</span><span class="sxs-lookup"><span data-stu-id="88f3d-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="88f3d-117">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="88f3d-117">Unordered list</span></span>

<span data-ttu-id="88f3d-118">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="88f3d-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="88f3d-119">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="88f3d-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="88f3d-120">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-120">will be rendered as:</span></span>

- <span data-ttu-id="88f3d-121">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-121">List item 1</span></span>
- <span data-ttu-id="88f3d-122">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="88f3d-122">List item 2</span></span>
- <span data-ttu-id="88f3d-123">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="88f3d-123">List item 3</span></span>

<span data-ttu-id="88f3d-124">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="88f3d-125">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="88f3d-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="88f3d-126">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-126">will be rendered as:</span></span>

- <span data-ttu-id="88f3d-127">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-127">List item 1</span></span>
  - <span data-ttu-id="88f3d-128">Lijstitem A</span><span class="sxs-lookup"><span data-stu-id="88f3d-128">List item A</span></span>
  - <span data-ttu-id="88f3d-129">Lijstitem B</span><span class="sxs-lookup"><span data-stu-id="88f3d-129">List item B</span></span>
- <span data-ttu-id="88f3d-130">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="88f3d-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="88f3d-131">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="88f3d-131">Ordered list</span></span>

<span data-ttu-id="88f3d-132">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="88f3d-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="88f3d-133">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="88f3d-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="88f3d-134">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-134">will be rendered as:</span></span>

1. <span data-ttu-id="88f3d-135">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-135">First instruction</span></span>
2. <span data-ttu-id="88f3d-136">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-136">Second instruction</span></span>
3. <span data-ttu-id="88f3d-137">Derde instructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-137">Third instruction</span></span>

<span data-ttu-id="88f3d-138">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="88f3d-139">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="88f3d-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="88f3d-140">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-140">will be rendered as:</span></span>

1. <span data-ttu-id="88f3d-141">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-141">First instruction</span></span>
    1. <span data-ttu-id="88f3d-142">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-142">Sub-instruction</span></span>
    2. <span data-ttu-id="88f3d-143">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-143">Sub-instruction</span></span>
2. <span data-ttu-id="88f3d-144">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="88f3d-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="88f3d-145">Tabellen</span><span class="sxs-lookup"><span data-stu-id="88f3d-145">Tables</span></span>

<span data-ttu-id="88f3d-146">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="88f3d-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="88f3d-147">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="88f3d-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="88f3d-148">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="88f3d-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="88f3d-149">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="88f3d-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="88f3d-150">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="88f3d-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="88f3d-151">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-151">will be rendered as:</span></span>

| <span data-ttu-id="88f3d-152">Pret</span><span class="sxs-lookup"><span data-stu-id="88f3d-152">Fun</span></span>                  | <span data-ttu-id="88f3d-153">met</span><span class="sxs-lookup"><span data-stu-id="88f3d-153">With</span></span>                 | <span data-ttu-id="88f3d-154">Tabellen</span><span class="sxs-lookup"><span data-stu-id="88f3d-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="88f3d-155">links uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="88f3d-155">left-aligned column</span></span>  | <span data-ttu-id="88f3d-156">rechts uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="88f3d-156">right-aligned column</span></span> | <span data-ttu-id="88f3d-157">gecentreerde kolom</span><span class="sxs-lookup"><span data-stu-id="88f3d-157">centered column</span></span> |
| <span data-ttu-id="88f3d-158">USD 100</span><span class="sxs-lookup"><span data-stu-id="88f3d-158">$100</span></span>                 | <span data-ttu-id="88f3d-159">USD 100</span><span class="sxs-lookup"><span data-stu-id="88f3d-159">$100</span></span>                 | <span data-ttu-id="88f3d-160">USD 100</span><span class="sxs-lookup"><span data-stu-id="88f3d-160">$100</span></span>            |
| <span data-ttu-id="88f3d-161">USD 10</span><span class="sxs-lookup"><span data-stu-id="88f3d-161">$10</span></span>                  | <span data-ttu-id="88f3d-162">USD 10</span><span class="sxs-lookup"><span data-stu-id="88f3d-162">$10</span></span>                  | <span data-ttu-id="88f3d-163">USD 10</span><span class="sxs-lookup"><span data-stu-id="88f3d-163">$10</span></span>             |
| <span data-ttu-id="88f3d-164">USD 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-164">$1</span></span>                   | <span data-ttu-id="88f3d-165">USD 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-165">$1</span></span>                   | <span data-ttu-id="88f3d-166">USD 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-166">$1</span></span>              |

<span data-ttu-id="88f3d-167">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="88f3d-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="88f3d-168">De [functie voor tabelterugloop](#table-wrapping) van DFM biedt ondersteuning bij het opmaken van brede tabellen</span><span class="sxs-lookup"><span data-stu-id="88f3d-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="88f3d-169">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub</span><span class="sxs-lookup"><span data-stu-id="88f3d-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="88f3d-170">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="88f3d-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="88f3d-171">Referentiemateriaal voor Markdown van Adam Pritchard</span><span class="sxs-lookup"><span data-stu-id="88f3d-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="88f3d-172">Markdown Extra van Michel Fortin</span><span class="sxs-lookup"><span data-stu-id="88f3d-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="88f3d-173">HTML-tabellen naar Markdown converteren</span><span class="sxs-lookup"><span data-stu-id="88f3d-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="88f3d-174">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="88f3d-174">Links</span></span>

<span data-ttu-id="88f3d-175">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="88f3d-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="88f3d-176">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="88f3d-176">For more information on linking, see:</span></span>

- <span data-ttu-id="88f3d-177">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="88f3d-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="88f3d-178">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over aanvullende syntaxis voor koppelen, zoals ondersteund door DFM.</span><span class="sxs-lookup"><span data-stu-id="88f3d-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="88f3d-179">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="88f3d-179">Code snippets</span></span>

<span data-ttu-id="88f3d-180">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="88f3d-181">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="88f3d-181">For details, see:</span></span>

- [<span data-ttu-id="88f3d-182">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="88f3d-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="88f3d-183">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="88f3d-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="88f3d-184">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="88f3d-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="88f3d-185">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="88f3d-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="88f3d-186">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88f3d-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="88f3d-187">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="88f3d-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="88f3d-188">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="88f3d-189">Naam</span><span class="sxs-lookup"><span data-stu-id="88f3d-189">Name</span></span>|<span data-ttu-id="88f3d-190">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="88f3d-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="88f3d-191">.NET Console</span><span class="sxs-lookup"><span data-stu-id="88f3d-191">.NET Console</span></span>|<span data-ttu-id="88f3d-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="88f3d-192">dotnetcli</span></span>|
|<span data-ttu-id="88f3d-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="88f3d-193">ASP.NET (C#)</span></span>|<span data-ttu-id="88f3d-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="88f3d-194">aspx-csharp</span></span>|
|<span data-ttu-id="88f3d-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="88f3d-195">ASP.NET (VB)</span></span>|<span data-ttu-id="88f3d-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="88f3d-196">aspx-vb</span></span>|
|<span data-ttu-id="88f3d-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="88f3d-197">AzCopy</span></span>|<span data-ttu-id="88f3d-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="88f3d-198">azcopy</span></span>|
|<span data-ttu-id="88f3d-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="88f3d-199">Azure CLI</span></span>|<span data-ttu-id="88f3d-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="88f3d-200">azurecli</span></span>|
|<span data-ttu-id="88f3d-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="88f3d-201">Azure PowerShell</span></span>|<span data-ttu-id="88f3d-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="88f3d-202">azurepowershell</span></span>|
|<span data-ttu-id="88f3d-203">C++</span><span class="sxs-lookup"><span data-stu-id="88f3d-203">C++</span></span>|<span data-ttu-id="88f3d-204">cpp</span><span class="sxs-lookup"><span data-stu-id="88f3d-204">cpp</span></span>|
|<span data-ttu-id="88f3d-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="88f3d-205">C++/CX</span></span>|<span data-ttu-id="88f3d-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="88f3d-206">cppcx</span></span>|
|<span data-ttu-id="88f3d-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="88f3d-207">C++/WinRT</span></span>|<span data-ttu-id="88f3d-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="88f3d-208">cppwinrt</span></span>|
|<span data-ttu-id="88f3d-209">C#</span><span class="sxs-lookup"><span data-stu-id="88f3d-209">C#</span></span>|<span data-ttu-id="88f3d-210">csharp</span><span class="sxs-lookup"><span data-stu-id="88f3d-210">csharp</span></span>|
|<span data-ttu-id="88f3d-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="88f3d-211">CSHTML</span></span>|<span data-ttu-id="88f3d-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="88f3d-212">cshtml</span></span>|
|<span data-ttu-id="88f3d-213">DAX</span><span class="sxs-lookup"><span data-stu-id="88f3d-213">DAX</span></span>|<span data-ttu-id="88f3d-214">dax</span><span class="sxs-lookup"><span data-stu-id="88f3d-214">dax</span></span>|
|<span data-ttu-id="88f3d-215">F#</span><span class="sxs-lookup"><span data-stu-id="88f3d-215">F#</span></span>|<span data-ttu-id="88f3d-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="88f3d-216">fsharp</span></span>|
|<span data-ttu-id="88f3d-217">Go</span><span class="sxs-lookup"><span data-stu-id="88f3d-217">Go</span></span>|<span data-ttu-id="88f3d-218">go</span><span class="sxs-lookup"><span data-stu-id="88f3d-218">go</span></span>|
|<span data-ttu-id="88f3d-219">HTML</span><span class="sxs-lookup"><span data-stu-id="88f3d-219">HTML</span></span>|<span data-ttu-id="88f3d-220">html</span><span class="sxs-lookup"><span data-stu-id="88f3d-220">html</span></span>|
|<span data-ttu-id="88f3d-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="88f3d-221">HTTP</span></span>|<span data-ttu-id="88f3d-222">http</span><span class="sxs-lookup"><span data-stu-id="88f3d-222">http</span></span>|
|<span data-ttu-id="88f3d-223">Java</span><span class="sxs-lookup"><span data-stu-id="88f3d-223">Java</span></span>|<span data-ttu-id="88f3d-224">java</span><span class="sxs-lookup"><span data-stu-id="88f3d-224">java</span></span>|
|<span data-ttu-id="88f3d-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="88f3d-225">JavaScript</span></span>|<span data-ttu-id="88f3d-226">javascript</span><span class="sxs-lookup"><span data-stu-id="88f3d-226">javascript</span></span>|
|<span data-ttu-id="88f3d-227">JSON</span><span class="sxs-lookup"><span data-stu-id="88f3d-227">JSON</span></span>|<span data-ttu-id="88f3d-228">json</span><span class="sxs-lookup"><span data-stu-id="88f3d-228">json</span></span>|
|<span data-ttu-id="88f3d-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-229">Markdown</span></span>|<span data-ttu-id="88f3d-230">md</span><span class="sxs-lookup"><span data-stu-id="88f3d-230">md</span></span>|
|<span data-ttu-id="88f3d-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="88f3d-231">NodeJS</span></span>|<span data-ttu-id="88f3d-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="88f3d-232">nodejs</span></span>|
|<span data-ttu-id="88f3d-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="88f3d-233">Objective-C</span></span>|<span data-ttu-id="88f3d-234">objc</span><span class="sxs-lookup"><span data-stu-id="88f3d-234">objc</span></span>|
|<span data-ttu-id="88f3d-235">OData</span><span class="sxs-lookup"><span data-stu-id="88f3d-235">OData</span></span>|<span data-ttu-id="88f3d-236">odata</span><span class="sxs-lookup"><span data-stu-id="88f3d-236">odata</span></span>|
|<span data-ttu-id="88f3d-237">PHP</span><span class="sxs-lookup"><span data-stu-id="88f3d-237">PHP</span></span>|<span data-ttu-id="88f3d-238">php</span><span class="sxs-lookup"><span data-stu-id="88f3d-238">php</span></span>|
|<span data-ttu-id="88f3d-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="88f3d-239">Power Apps Formula</span></span>|<span data-ttu-id="88f3d-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="88f3d-240">powerappsfl</span></span>|
|<span data-ttu-id="88f3d-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="88f3d-241">PowerShell</span></span>|<span data-ttu-id="88f3d-242">powershell</span><span class="sxs-lookup"><span data-stu-id="88f3d-242">powershell</span></span>|
|<span data-ttu-id="88f3d-243">Python</span><span class="sxs-lookup"><span data-stu-id="88f3d-243">Python</span></span>|<span data-ttu-id="88f3d-244">python</span><span class="sxs-lookup"><span data-stu-id="88f3d-244">python</span></span>|
|<span data-ttu-id="88f3d-245">Q#</span><span class="sxs-lookup"><span data-stu-id="88f3d-245">Q#</span></span>|<span data-ttu-id="88f3d-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="88f3d-246">qsharp</span></span>|
|<span data-ttu-id="88f3d-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="88f3d-247">Ruby</span></span>|<span data-ttu-id="88f3d-248">ruby</span><span class="sxs-lookup"><span data-stu-id="88f3d-248">ruby</span></span>|
|<span data-ttu-id="88f3d-249">SQL</span><span class="sxs-lookup"><span data-stu-id="88f3d-249">SQL</span></span>|<span data-ttu-id="88f3d-250">sql</span><span class="sxs-lookup"><span data-stu-id="88f3d-250">sql</span></span>|
|<span data-ttu-id="88f3d-251">Swift</span><span class="sxs-lookup"><span data-stu-id="88f3d-251">Swift</span></span>|<span data-ttu-id="88f3d-252">swift</span><span class="sxs-lookup"><span data-stu-id="88f3d-252">swift</span></span>|
|<span data-ttu-id="88f3d-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="88f3d-253">TypeScript</span></span>|<span data-ttu-id="88f3d-254">typescript</span><span class="sxs-lookup"><span data-stu-id="88f3d-254">typescript</span></span>|
|<span data-ttu-id="88f3d-255">VB</span><span class="sxs-lookup"><span data-stu-id="88f3d-255">VB</span></span>|<span data-ttu-id="88f3d-256">vb</span><span class="sxs-lookup"><span data-stu-id="88f3d-256">vb</span></span>|
|<span data-ttu-id="88f3d-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="88f3d-257">VSTS CLI</span></span>|<span data-ttu-id="88f3d-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="88f3d-258">vstscli</span></span>|
|<span data-ttu-id="88f3d-259">XAML</span><span class="sxs-lookup"><span data-stu-id="88f3d-259">XAML</span></span>|<span data-ttu-id="88f3d-260">xaml</span><span class="sxs-lookup"><span data-stu-id="88f3d-260">xaml</span></span>|
|<span data-ttu-id="88f3d-261">XML</span><span class="sxs-lookup"><span data-stu-id="88f3d-261">XML</span></span>|<span data-ttu-id="88f3d-262">xml</span><span class="sxs-lookup"><span data-stu-id="88f3d-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="88f3d-263">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="88f3d-263">Example: C\#</span></span>

<span data-ttu-id="88f3d-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="88f3d-264">__Markdown__</span></span>

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

<span data-ttu-id="88f3d-265">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="88f3d-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="88f3d-266">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="88f3d-266">Example: SQL</span></span>

<span data-ttu-id="88f3d-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="88f3d-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="88f3d-268">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="88f3d-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="88f3d-269">Aangepaste OPS-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="88f3d-270">Met OPS (Open Publishing Services) wordt DFM (DocFX Flavored Markdown) geïmplementeerd, dat zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="88f3d-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="88f3d-271">Met DFM wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="88f3d-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="88f3d-272">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="88f3d-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="88f3d-273">(Zie bijvoorbeeld Extensies voor DFM en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="88f3d-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="88f3d-274">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="88f3d-275">Voor rijkere opmaak kunnen in artikelen DFM-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="88f3d-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="88f3d-276">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="88f3d-276">Note blocks</span></span>
- <span data-ttu-id="88f3d-277">Omvat</span><span class="sxs-lookup"><span data-stu-id="88f3d-277">Includes</span></span>
- <span data-ttu-id="88f3d-278">Selectors</span><span class="sxs-lookup"><span data-stu-id="88f3d-278">Selectors</span></span>
- <span data-ttu-id="88f3d-279">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="88f3d-279">Embedded videos</span></span>
- <span data-ttu-id="88f3d-280">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="88f3d-280">Code snippets/samples</span></span>

<span data-ttu-id="88f3d-281">Raadpleeg Extensies voor DFM en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="88f3d-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="88f3d-282">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="88f3d-282">Note blocks</span></span>

<span data-ttu-id="88f3d-283">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="88f3d-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="88f3d-284">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="88f3d-284">NOTE</span></span>
- <span data-ttu-id="88f3d-285">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="88f3d-285">WARNING</span></span>
- <span data-ttu-id="88f3d-286">TIP</span><span class="sxs-lookup"><span data-stu-id="88f3d-286">TIP</span></span>
- <span data-ttu-id="88f3d-287">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="88f3d-287">IMPORTANT</span></span>

<span data-ttu-id="88f3d-288">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="88f3d-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="88f3d-289">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="88f3d-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="88f3d-290">Omvat</span><span class="sxs-lookup"><span data-stu-id="88f3d-290">Includes</span></span>

<span data-ttu-id="88f3d-291">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de DFM-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="88f3d-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="88f3d-292">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="88f3d-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="88f3d-293">Er zijn drie soorten insluitingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="88f3d-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="88f3d-294">Inline: een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="88f3d-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="88f3d-295">Blok: een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="88f3d-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="88f3d-296">Afbeelding: op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="88f3d-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="88f3d-297">Een inline- of blokinsluiting is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="88f3d-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="88f3d-298">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="88f3d-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="88f3d-299">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="88f3d-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="88f3d-300">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="88f3d-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="88f3d-301">Dit zijn de vereisten en overwegingen voor insluitingen:</span><span class="sxs-lookup"><span data-stu-id="88f3d-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="88f3d-302">Gebruik insluitingen wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="88f3d-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="88f3d-303">Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="88f3d-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="88f3d-304">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="88f3d-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="88f3d-305">Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van DFM-extensies.</span><span class="sxs-lookup"><span data-stu-id="88f3d-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="88f3d-306">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="88f3d-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="88f3d-307">Zorg ervoor dat de tekst in een insluiting uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="88f3d-308">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="88f3d-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="88f3d-309">Voeg geen insluitingen in andere insluitingen in.</span><span class="sxs-lookup"><span data-stu-id="88f3d-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="88f3d-310">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="88f3d-310">They are not supported.</span></span>
- <span data-ttu-id="88f3d-311">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="88f3d-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="88f3d-312">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="88f3d-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="88f3d-313">Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88f3d-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="88f3d-314">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="88f3d-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="88f3d-315">Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel.</span><span class="sxs-lookup"><span data-stu-id="88f3d-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="88f3d-316">Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.</span><span class="sxs-lookup"><span data-stu-id="88f3d-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="88f3d-317">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.</span><span class="sxs-lookup"><span data-stu-id="88f3d-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="88f3d-318">Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="88f3d-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="88f3d-319">Selectors</span><span class="sxs-lookup"><span data-stu-id="88f3d-319">Selectors</span></span>

<span data-ttu-id="88f3d-320">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of platformen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="88f3d-321">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="88f3d-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="88f3d-322">Er zijn momenteel twee verschillende soorten selectors in DFM, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="88f3d-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="88f3d-323">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluiting.</span><span class="sxs-lookup"><span data-stu-id="88f3d-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="88f3d-324">Deze kan vervolgens naar deze insluiting verwijzen in alle onderwerpen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88f3d-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="88f3d-325">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="88f3d-325">Code snippets</span></span>

<span data-ttu-id="88f3d-326">DFM ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="88f3d-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="88f3d-327">Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:</span><span class="sxs-lookup"><span data-stu-id="88f3d-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="88f3d-328">Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="88f3d-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="88f3d-329">Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="88f3d-330">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="88f3d-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="88f3d-331">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="88f3d-331">Alt text</span></span>

<span data-ttu-id="88f3d-332">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="88f3d-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="88f3d-333">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="88f3d-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="88f3d-334">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="88f3d-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="88f3d-335">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="88f3d-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="88f3d-336">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="88f3d-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="88f3d-337">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="88f3d-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="88f3d-338">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="88f3d-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="88f3d-339">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="88f3d-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="88f3d-340">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="88f3d-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="88f3d-341">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="88f3d-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="88f3d-342">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="88f3d-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="88f3d-343">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="88f3d-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="88f3d-344">Punthaken</span><span class="sxs-lookup"><span data-stu-id="88f3d-344">Angle brackets</span></span>

<span data-ttu-id="88f3d-345">Als u in lopende tekst (geen code) punthaken gebruikt, bijvoorbeeld om een tijdelijke aanduiding aan te geven, moet u de punthaken handmatig coderen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="88f3d-346">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="88f3d-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="88f3d-347">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="88f3d-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="88f3d-348">Zie ook</span><span class="sxs-lookup"><span data-stu-id="88f3d-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="88f3d-349">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="88f3d-349">Markdown resources</span></span>

- [<span data-ttu-id="88f3d-350">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-350">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="88f3d-351">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="88f3d-352">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="88f3d-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
