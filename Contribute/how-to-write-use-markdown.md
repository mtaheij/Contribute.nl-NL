---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805719"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="0fbea-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="0fbea-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="0fbea-104">Artikelen op [docs.microsoft.com](http://docs.microsoft.com) worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="0fbea-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="0fbea-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="0fbea-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="0fbea-106">Omdat Docs-inhoud wordt opgeslagen in GitHub, kan een hoofdverzameling van Markdown, [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), worden gebruikt. Deze biedt aanvullende functionaliteit voor algemene opmaakbehoeften.</span><span class="sxs-lookup"><span data-stu-id="0fbea-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="0fbea-107">Daarnaast wordt met OPS (Open Publishing Services) Markdig Markdown Parser geïmplementeerd,</span><span class="sxs-lookup"><span data-stu-id="0fbea-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="0fbea-108">Markdig is zeer compatibel met GFM. Hiermee wordt functionaliteit toegevoegd om specifieke functies van Docs in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="0fbea-109">Markdig is een snelle, krachtige, CommonMark-compatibele, extensible Markdown-processor voor .NET.</span><span class="sxs-lookup"><span data-stu-id="0fbea-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="0fbea-110">Betere ondersteuning voor community</span><span class="sxs-lookup"><span data-stu-id="0fbea-110">Better community support</span></span>
* <span data-ttu-id="0fbea-111">Betere ondersteuning voor standaarden</span><span class="sxs-lookup"><span data-stu-id="0fbea-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="0fbea-112">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="0fbea-113">Koppen</span><span class="sxs-lookup"><span data-stu-id="0fbea-113">Headings</span></span>

<span data-ttu-id="0fbea-114">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="0fbea-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="0fbea-115">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="0fbea-115">Bold and italic text</span></span>

<span data-ttu-id="0fbea-116">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="0fbea-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="0fbea-117">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="0fbea-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="0fbea-118">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="0fbea-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="0fbea-119">Lijsten</span><span class="sxs-lookup"><span data-stu-id="0fbea-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="0fbea-120">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="0fbea-120">Unordered list</span></span>

<span data-ttu-id="0fbea-121">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0fbea-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="0fbea-122">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="0fbea-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="0fbea-123">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-123">will be rendered as:</span></span>

- <span data-ttu-id="0fbea-124">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="0fbea-124">List item 1</span></span>
- <span data-ttu-id="0fbea-125">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="0fbea-125">List item 2</span></span>
- <span data-ttu-id="0fbea-126">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="0fbea-126">List item 3</span></span>

<span data-ttu-id="0fbea-127">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0fbea-128">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="0fbea-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="0fbea-129">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-129">will be rendered as:</span></span>

- <span data-ttu-id="0fbea-130">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="0fbea-130">List item 1</span></span>
  - <span data-ttu-id="0fbea-131">Lijstitem A</span><span class="sxs-lookup"><span data-stu-id="0fbea-131">List item A</span></span>
  - <span data-ttu-id="0fbea-132">Lijstitem B</span><span class="sxs-lookup"><span data-stu-id="0fbea-132">List item B</span></span>
- <span data-ttu-id="0fbea-133">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="0fbea-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="0fbea-134">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="0fbea-134">Ordered list</span></span>

<span data-ttu-id="0fbea-135">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="0fbea-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="0fbea-136">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="0fbea-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="0fbea-137">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-137">will be rendered as:</span></span>

1. <span data-ttu-id="0fbea-138">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-138">First instruction</span></span>
2. <span data-ttu-id="0fbea-139">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-139">Second instruction</span></span>
3. <span data-ttu-id="0fbea-140">Derde instructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-140">Third instruction</span></span>

<span data-ttu-id="0fbea-141">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0fbea-142">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="0fbea-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="0fbea-143">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-143">will be rendered as:</span></span>

1. <span data-ttu-id="0fbea-144">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-144">First instruction</span></span>
   1. <span data-ttu-id="0fbea-145">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-145">Sub-instruction</span></span>
   2. <span data-ttu-id="0fbea-146">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-146">Sub-instruction</span></span>
2. <span data-ttu-id="0fbea-147">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="0fbea-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="0fbea-148">Tabellen</span><span class="sxs-lookup"><span data-stu-id="0fbea-148">Tables</span></span>

<span data-ttu-id="0fbea-149">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="0fbea-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="0fbea-150">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="0fbea-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="0fbea-151">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="0fbea-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="0fbea-152">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0fbea-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="0fbea-153">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="0fbea-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="0fbea-154">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-154">will be rendered as:</span></span>

| <span data-ttu-id="0fbea-155">Pret</span><span class="sxs-lookup"><span data-stu-id="0fbea-155">Fun</span></span>                  | <span data-ttu-id="0fbea-156">met</span><span class="sxs-lookup"><span data-stu-id="0fbea-156">With</span></span>                 | <span data-ttu-id="0fbea-157">Tabellen</span><span class="sxs-lookup"><span data-stu-id="0fbea-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="0fbea-158">links uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="0fbea-158">left-aligned column</span></span>  | <span data-ttu-id="0fbea-159">rechts uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="0fbea-159">right-aligned column</span></span> | <span data-ttu-id="0fbea-160">gecentreerde kolom</span><span class="sxs-lookup"><span data-stu-id="0fbea-160">centered column</span></span> |
| <span data-ttu-id="0fbea-161">USD 100</span><span class="sxs-lookup"><span data-stu-id="0fbea-161">$100</span></span>                 | <span data-ttu-id="0fbea-162">USD 100</span><span class="sxs-lookup"><span data-stu-id="0fbea-162">$100</span></span>                 | <span data-ttu-id="0fbea-163">USD 100</span><span class="sxs-lookup"><span data-stu-id="0fbea-163">$100</span></span>            |
| <span data-ttu-id="0fbea-164">USD 10</span><span class="sxs-lookup"><span data-stu-id="0fbea-164">$10</span></span>                  | <span data-ttu-id="0fbea-165">USD 10</span><span class="sxs-lookup"><span data-stu-id="0fbea-165">$10</span></span>                  | <span data-ttu-id="0fbea-166">USD 10</span><span class="sxs-lookup"><span data-stu-id="0fbea-166">$10</span></span>             |
| <span data-ttu-id="0fbea-167">USD 1</span><span class="sxs-lookup"><span data-stu-id="0fbea-167">$1</span></span>                   | <span data-ttu-id="0fbea-168">USD 1</span><span class="sxs-lookup"><span data-stu-id="0fbea-168">$1</span></span>                   | <span data-ttu-id="0fbea-169">USD 1</span><span class="sxs-lookup"><span data-stu-id="0fbea-169">$1</span></span>              |

<span data-ttu-id="0fbea-170">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="0fbea-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="0fbea-171">De [functie voor tabelterugloop](#table-wrapping) van Markdig biedt ondersteuning bij het opmaken van brede tabellen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="0fbea-172">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="0fbea-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="0fbea-173">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="0fbea-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="0fbea-174">[Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="0fbea-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="0fbea-175">[Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="0fbea-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="0fbea-176">[HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="0fbea-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="0fbea-177">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="0fbea-177">Links</span></span>

<span data-ttu-id="0fbea-178">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="0fbea-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="0fbea-179">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="0fbea-179">For more information on linking, see:</span></span>

- <span data-ttu-id="0fbea-180">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="0fbea-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="0fbea-181">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over de aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.</span><span class="sxs-lookup"><span data-stu-id="0fbea-181">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="0fbea-182">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="0fbea-182">Code snippets</span></span>

<span data-ttu-id="0fbea-183">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="0fbea-184">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="0fbea-184">For details, see:</span></span>

- [<span data-ttu-id="0fbea-185">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="0fbea-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="0fbea-186">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="0fbea-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="0fbea-187">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="0fbea-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="0fbea-188">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="0fbea-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="0fbea-189">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0fbea-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="0fbea-190">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="0fbea-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="0fbea-191">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="0fbea-192">Naam</span><span class="sxs-lookup"><span data-stu-id="0fbea-192">Name</span></span>|<span data-ttu-id="0fbea-193">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="0fbea-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="0fbea-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="0fbea-194">.NET Console</span></span>|<span data-ttu-id="0fbea-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="0fbea-195">dotnetcli</span></span>|
|<span data-ttu-id="0fbea-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="0fbea-196">ASP.NET (C#)</span></span>|<span data-ttu-id="0fbea-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="0fbea-197">aspx-csharp</span></span>|
|<span data-ttu-id="0fbea-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="0fbea-198">ASP.NET (VB)</span></span>|<span data-ttu-id="0fbea-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="0fbea-199">aspx-vb</span></span>|
|<span data-ttu-id="0fbea-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="0fbea-200">AzCopy</span></span>|<span data-ttu-id="0fbea-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="0fbea-201">azcopy</span></span>|
|<span data-ttu-id="0fbea-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="0fbea-202">Azure CLI</span></span>|<span data-ttu-id="0fbea-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="0fbea-203">azurecli</span></span>|
|<span data-ttu-id="0fbea-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0fbea-204">Azure PowerShell</span></span>|<span data-ttu-id="0fbea-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="0fbea-205">azurepowershell</span></span>|
|<span data-ttu-id="0fbea-206">C++</span><span class="sxs-lookup"><span data-stu-id="0fbea-206">C++</span></span>|<span data-ttu-id="0fbea-207">cpp</span><span class="sxs-lookup"><span data-stu-id="0fbea-207">cpp</span></span>|
|<span data-ttu-id="0fbea-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="0fbea-208">C++/CX</span></span>|<span data-ttu-id="0fbea-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="0fbea-209">cppcx</span></span>|
|<span data-ttu-id="0fbea-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="0fbea-210">C++/WinRT</span></span>|<span data-ttu-id="0fbea-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="0fbea-211">cppwinrt</span></span>|
|<span data-ttu-id="0fbea-212">C#</span><span class="sxs-lookup"><span data-stu-id="0fbea-212">C#</span></span>|<span data-ttu-id="0fbea-213">csharp</span><span class="sxs-lookup"><span data-stu-id="0fbea-213">csharp</span></span>|
|<span data-ttu-id="0fbea-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="0fbea-214">CSHTML</span></span>|<span data-ttu-id="0fbea-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="0fbea-215">cshtml</span></span>|
|<span data-ttu-id="0fbea-216">DAX</span><span class="sxs-lookup"><span data-stu-id="0fbea-216">DAX</span></span>|<span data-ttu-id="0fbea-217">dax</span><span class="sxs-lookup"><span data-stu-id="0fbea-217">dax</span></span>|
|<span data-ttu-id="0fbea-218">F#</span><span class="sxs-lookup"><span data-stu-id="0fbea-218">F#</span></span>|<span data-ttu-id="0fbea-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="0fbea-219">fsharp</span></span>|
|<span data-ttu-id="0fbea-220">Go</span><span class="sxs-lookup"><span data-stu-id="0fbea-220">Go</span></span>|<span data-ttu-id="0fbea-221">go</span><span class="sxs-lookup"><span data-stu-id="0fbea-221">go</span></span>|
|<span data-ttu-id="0fbea-222">HTML</span><span class="sxs-lookup"><span data-stu-id="0fbea-222">HTML</span></span>|<span data-ttu-id="0fbea-223">html</span><span class="sxs-lookup"><span data-stu-id="0fbea-223">html</span></span>|
|<span data-ttu-id="0fbea-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="0fbea-224">HTTP</span></span>|<span data-ttu-id="0fbea-225">http</span><span class="sxs-lookup"><span data-stu-id="0fbea-225">http</span></span>|
|<span data-ttu-id="0fbea-226">Java</span><span class="sxs-lookup"><span data-stu-id="0fbea-226">Java</span></span>|<span data-ttu-id="0fbea-227">java</span><span class="sxs-lookup"><span data-stu-id="0fbea-227">java</span></span>|
|<span data-ttu-id="0fbea-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0fbea-228">JavaScript</span></span>|<span data-ttu-id="0fbea-229">javascript</span><span class="sxs-lookup"><span data-stu-id="0fbea-229">javascript</span></span>|
|<span data-ttu-id="0fbea-230">JSON</span><span class="sxs-lookup"><span data-stu-id="0fbea-230">JSON</span></span>|<span data-ttu-id="0fbea-231">json</span><span class="sxs-lookup"><span data-stu-id="0fbea-231">json</span></span>|
|<span data-ttu-id="0fbea-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-232">Markdown</span></span>|<span data-ttu-id="0fbea-233">md</span><span class="sxs-lookup"><span data-stu-id="0fbea-233">md</span></span>|
|<span data-ttu-id="0fbea-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="0fbea-234">NodeJS</span></span>|<span data-ttu-id="0fbea-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="0fbea-235">nodejs</span></span>|
|<span data-ttu-id="0fbea-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0fbea-236">Objective-C</span></span>|<span data-ttu-id="0fbea-237">objc</span><span class="sxs-lookup"><span data-stu-id="0fbea-237">objc</span></span>|
|<span data-ttu-id="0fbea-238">OData</span><span class="sxs-lookup"><span data-stu-id="0fbea-238">OData</span></span>|<span data-ttu-id="0fbea-239">odata</span><span class="sxs-lookup"><span data-stu-id="0fbea-239">odata</span></span>|
|<span data-ttu-id="0fbea-240">PHP</span><span class="sxs-lookup"><span data-stu-id="0fbea-240">PHP</span></span>|<span data-ttu-id="0fbea-241">php</span><span class="sxs-lookup"><span data-stu-id="0fbea-241">php</span></span>|
|<span data-ttu-id="0fbea-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="0fbea-242">Power Apps Formula</span></span>|<span data-ttu-id="0fbea-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="0fbea-243">powerappsfl</span></span>|
|<span data-ttu-id="0fbea-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0fbea-244">PowerShell</span></span>|<span data-ttu-id="0fbea-245">powershell</span><span class="sxs-lookup"><span data-stu-id="0fbea-245">powershell</span></span>|
|<span data-ttu-id="0fbea-246">Python</span><span class="sxs-lookup"><span data-stu-id="0fbea-246">Python</span></span>|<span data-ttu-id="0fbea-247">python</span><span class="sxs-lookup"><span data-stu-id="0fbea-247">python</span></span>|
|<span data-ttu-id="0fbea-248">Q#</span><span class="sxs-lookup"><span data-stu-id="0fbea-248">Q#</span></span>|<span data-ttu-id="0fbea-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="0fbea-249">qsharp</span></span>|
|<span data-ttu-id="0fbea-250">R</span><span class="sxs-lookup"><span data-stu-id="0fbea-250">R</span></span>|<span data-ttu-id="0fbea-251">r</span><span class="sxs-lookup"><span data-stu-id="0fbea-251">r</span></span>|
|<span data-ttu-id="0fbea-252">Ruby</span><span class="sxs-lookup"><span data-stu-id="0fbea-252">Ruby</span></span>|<span data-ttu-id="0fbea-253">ruby</span><span class="sxs-lookup"><span data-stu-id="0fbea-253">ruby</span></span>|
|<span data-ttu-id="0fbea-254">SQL</span><span class="sxs-lookup"><span data-stu-id="0fbea-254">SQL</span></span>|<span data-ttu-id="0fbea-255">sql</span><span class="sxs-lookup"><span data-stu-id="0fbea-255">sql</span></span>|
|<span data-ttu-id="0fbea-256">Swift</span><span class="sxs-lookup"><span data-stu-id="0fbea-256">Swift</span></span>|<span data-ttu-id="0fbea-257">swift</span><span class="sxs-lookup"><span data-stu-id="0fbea-257">swift</span></span>|
|<span data-ttu-id="0fbea-258">TypeScript</span><span class="sxs-lookup"><span data-stu-id="0fbea-258">TypeScript</span></span>|<span data-ttu-id="0fbea-259">typescript</span><span class="sxs-lookup"><span data-stu-id="0fbea-259">typescript</span></span>|
|<span data-ttu-id="0fbea-260">VB</span><span class="sxs-lookup"><span data-stu-id="0fbea-260">VB</span></span>|<span data-ttu-id="0fbea-261">vb</span><span class="sxs-lookup"><span data-stu-id="0fbea-261">vb</span></span>|
|<span data-ttu-id="0fbea-262">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="0fbea-262">VSTS CLI</span></span>|<span data-ttu-id="0fbea-263">vstscli</span><span class="sxs-lookup"><span data-stu-id="0fbea-263">vstscli</span></span>|
|<span data-ttu-id="0fbea-264">XAML</span><span class="sxs-lookup"><span data-stu-id="0fbea-264">XAML</span></span>|<span data-ttu-id="0fbea-265">xaml</span><span class="sxs-lookup"><span data-stu-id="0fbea-265">xaml</span></span>|
|<span data-ttu-id="0fbea-266">XML</span><span class="sxs-lookup"><span data-stu-id="0fbea-266">XML</span></span>|<span data-ttu-id="0fbea-267">xml</span><span class="sxs-lookup"><span data-stu-id="0fbea-267">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="0fbea-268">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="0fbea-268">Example: C\#</span></span>

<span data-ttu-id="0fbea-269">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0fbea-269">__Markdown__</span></span>

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

<span data-ttu-id="0fbea-270">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="0fbea-270">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="0fbea-271">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="0fbea-271">Example: SQL</span></span>

<span data-ttu-id="0fbea-272">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0fbea-272">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="0fbea-273">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="0fbea-273">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="0fbea-274">Aangepaste OPS-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-274">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="0fbea-275">Met OPS (Open Publishing Services) wordt Markdig Parser for Markdown geïmplementeerd, dat zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="0fbea-275">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="0fbea-276">Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="0fbea-276">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="0fbea-277">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="0fbea-277">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="0fbea-278">(Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="0fbea-278">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="0fbea-279">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-279">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="0fbea-280">Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="0fbea-280">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="0fbea-281">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="0fbea-281">Note blocks</span></span>
- <span data-ttu-id="0fbea-282">Omvat</span><span class="sxs-lookup"><span data-stu-id="0fbea-282">Includes</span></span>
- <span data-ttu-id="0fbea-283">Selectors</span><span class="sxs-lookup"><span data-stu-id="0fbea-283">Selectors</span></span>
- <span data-ttu-id="0fbea-284">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="0fbea-284">Embedded videos</span></span>
- <span data-ttu-id="0fbea-285">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="0fbea-285">Code snippets/samples</span></span>

<span data-ttu-id="0fbea-286">Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="0fbea-286">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="0fbea-287">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="0fbea-287">Note blocks</span></span>

<span data-ttu-id="0fbea-288">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="0fbea-288">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="0fbea-289">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="0fbea-289">NOTE</span></span>
- <span data-ttu-id="0fbea-290">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="0fbea-290">WARNING</span></span>
- <span data-ttu-id="0fbea-291">TIP</span><span class="sxs-lookup"><span data-stu-id="0fbea-291">TIP</span></span>
- <span data-ttu-id="0fbea-292">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="0fbea-292">IMPORTANT</span></span>

<span data-ttu-id="0fbea-293">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="0fbea-293">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="0fbea-294">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="0fbea-294">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="0fbea-295">Omvat</span><span class="sxs-lookup"><span data-stu-id="0fbea-295">Includes</span></span>

<span data-ttu-id="0fbea-296">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="0fbea-296">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="0fbea-297">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="0fbea-297">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="0fbea-298">Er zijn drie soorten insluitingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="0fbea-298">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="0fbea-299">Inline: een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="0fbea-299">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="0fbea-300">Blok: een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="0fbea-300">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="0fbea-301">Afbeelding: op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="0fbea-301">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="0fbea-302">Een inline- of blokinsluiting is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="0fbea-302">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="0fbea-303">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="0fbea-303">It can contain any valid Markdown.</span></span> <span data-ttu-id="0fbea-304">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="0fbea-304">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="0fbea-305">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="0fbea-305">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="0fbea-306">Dit zijn de vereisten en overwegingen voor insluitingen:</span><span class="sxs-lookup"><span data-stu-id="0fbea-306">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="0fbea-307">Gebruik insluitingen wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0fbea-307">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="0fbea-308">Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="0fbea-308">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="0fbea-309">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="0fbea-309">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="0fbea-310">Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van Markdig-extensies.</span><span class="sxs-lookup"><span data-stu-id="0fbea-310">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="0fbea-311">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="0fbea-311">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="0fbea-312">Zorg ervoor dat de tekst in een insluiting uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-312">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="0fbea-313">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="0fbea-313">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="0fbea-314">Voeg geen insluitingen in andere insluitingen in.</span><span class="sxs-lookup"><span data-stu-id="0fbea-314">Don't embed includes within other includes.</span></span> <span data-ttu-id="0fbea-315">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0fbea-315">They are not supported.</span></span>
- <span data-ttu-id="0fbea-316">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="0fbea-316">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="0fbea-317">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="0fbea-317">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="0fbea-318">Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0fbea-318">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="0fbea-319">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="0fbea-319">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="0fbea-320">Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel.</span><span class="sxs-lookup"><span data-stu-id="0fbea-320">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="0fbea-321">Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.</span><span class="sxs-lookup"><span data-stu-id="0fbea-321">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="0fbea-322">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.</span><span class="sxs-lookup"><span data-stu-id="0fbea-322">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="0fbea-323">Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="0fbea-323">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="0fbea-324">Selectors</span><span class="sxs-lookup"><span data-stu-id="0fbea-324">Selectors</span></span>

<span data-ttu-id="0fbea-325">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of platformen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-325">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="0fbea-326">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="0fbea-326">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="0fbea-327">Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="0fbea-327">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="0fbea-328">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluiting.</span><span class="sxs-lookup"><span data-stu-id="0fbea-328">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="0fbea-329">Deze kan vervolgens naar deze insluiting verwijzen in alle onderwerpen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0fbea-329">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="0fbea-330">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="0fbea-330">Code snippets</span></span>

<span data-ttu-id="0fbea-331">Markdig ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="0fbea-331">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="0fbea-332">Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:</span><span class="sxs-lookup"><span data-stu-id="0fbea-332">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="0fbea-333">Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="0fbea-333">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="0fbea-334">Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-334">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="0fbea-335">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="0fbea-335">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="0fbea-336">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="0fbea-336">Alt text</span></span>

<span data-ttu-id="0fbea-337">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0fbea-337">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="0fbea-338">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="0fbea-338">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="0fbea-339">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="0fbea-339">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="0fbea-340">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="0fbea-340">Apostrophes and quotation marks</span></span>

<span data-ttu-id="0fbea-341">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="0fbea-341">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="0fbea-342">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="0fbea-342">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span>
<span data-ttu-id="0fbea-343">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="0fbea-343">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="0fbea-344">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="0fbea-344">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="0fbea-345">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="0fbea-345">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="0fbea-346">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="0fbea-346">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="0fbea-347">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="0fbea-347">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="0fbea-348">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="0fbea-348">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="0fbea-349">Punthaken</span><span class="sxs-lookup"><span data-stu-id="0fbea-349">Angle brackets</span></span>

<span data-ttu-id="0fbea-350">Het is gebruikelijk punthaken te gebruiken om een tijdelijke aanduiding aan te geven.</span><span class="sxs-lookup"><span data-stu-id="0fbea-350">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="0fbea-351">Als u dit in tekst doet (dus niet in code), moet u de punthaken coderen.</span><span class="sxs-lookup"><span data-stu-id="0fbea-351">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="0fbea-352">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="0fbea-352">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="0fbea-353">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="0fbea-353">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="0fbea-354">Zie ook:</span><span class="sxs-lookup"><span data-stu-id="0fbea-354">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="0fbea-355">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="0fbea-355">Markdown resources</span></span>

- [<span data-ttu-id="0fbea-356">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-356">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="0fbea-357">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-357">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="0fbea-358">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="0fbea-358">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="0fbea-359">De Markdown-handleiding</span><span class="sxs-lookup"><span data-stu-id="0fbea-359">The Markdown Guide</span></span>](https://www.markdownguide.org/)
