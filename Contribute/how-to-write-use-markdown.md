---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615830"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="f0e40-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="f0e40-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="f0e40-104">Artikelen op [docs.microsoft.com](http://docs.microsoft.com) worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="f0e40-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="f0e40-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="f0e40-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="f0e40-106">Omdat Docs-inhoud wordt opgeslagen in GitHub, kan een hoofdverzameling van Markdown, [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), worden gebruikt. Deze biedt aanvullende functionaliteit voor algemene opmaakbehoeften.</span><span class="sxs-lookup"><span data-stu-id="f0e40-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="f0e40-107">Daarnaast wordt met OPS (Open Publishing Services) Markdig Markdown Parser geïmplementeerd,</span><span class="sxs-lookup"><span data-stu-id="f0e40-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="f0e40-108">Markdig is zeer compatibel met GFM. Hiermee wordt functionaliteit toegevoegd om specifieke functies van Docs in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="f0e40-109">Markdig is een snelle, krachtige, CommonMark-compatibele, extensible Markdown-processor voor .NET.</span><span class="sxs-lookup"><span data-stu-id="f0e40-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="f0e40-110">Betere ondersteuning voor community</span><span class="sxs-lookup"><span data-stu-id="f0e40-110">Better community support</span></span>
* <span data-ttu-id="f0e40-111">Betere ondersteuning voor standaarden</span><span class="sxs-lookup"><span data-stu-id="f0e40-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="f0e40-112">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="f0e40-113">Koppen</span><span class="sxs-lookup"><span data-stu-id="f0e40-113">Headings</span></span>

<span data-ttu-id="f0e40-114">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="f0e40-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="f0e40-115">Headers moeten in ATX-stijl worden gemaakt, dat wil zeggen dat aan het begin van de regel 1 tot 6 hekjes (#) moeten staan om een header aan te duiden overeenkomstig de HTML-headerniveaus H1 tot H6.</span><span class="sxs-lookup"><span data-stu-id="f0e40-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="f0e40-116">Hierboven vindt u voorbeelden van headers van het eerste tot vierde niveau.</span><span class="sxs-lookup"><span data-stu-id="f0e40-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="f0e40-117">Uw onderwerp **mag** maar één header van het eerste niveau (H1) bevatten. Deze wordt op de pagina weergegeven als de titel.</span><span class="sxs-lookup"><span data-stu-id="f0e40-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="f0e40-118">Als uw header met een `#` eindigt, moet u aan het eind nog een `#` toevoegen zodat de titel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f0e40-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="f0e40-119">Bijvoorbeeld `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="f0e40-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="f0e40-120">Met de headers op het tweede niveau wordt de inhoudsopgave op de pagina gegenereerd die wordt weergegeven in de sectie 'In dit artikel' onder de titel op de pagina.</span><span class="sxs-lookup"><span data-stu-id="f0e40-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="f0e40-121">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="f0e40-121">Bold and italic text</span></span>

<span data-ttu-id="f0e40-122">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="f0e40-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="f0e40-123">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="f0e40-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="f0e40-124">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="f0e40-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="f0e40-125">Blokcitaten</span><span class="sxs-lookup"><span data-stu-id="f0e40-125">Blockquotes</span></span>

<span data-ttu-id="f0e40-126">Blokcitaten worden gemaakt met het teken `>`:</span><span class="sxs-lookup"><span data-stu-id="f0e40-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="f0e40-127">Het voorbeeld hierboven wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="f0e40-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="f0e40-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="f0e40-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="f0e40-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="f0e40-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="f0e40-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="f0e40-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="f0e40-131">Lijsten</span><span class="sxs-lookup"><span data-stu-id="f0e40-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="f0e40-132">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="f0e40-132">Unordered list</span></span>

<span data-ttu-id="f0e40-133">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f0e40-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="f0e40-134">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0e40-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="f0e40-135">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-135">will be rendered as:</span></span>

- <span data-ttu-id="f0e40-136">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="f0e40-136">List item 1</span></span>
- <span data-ttu-id="f0e40-137">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="f0e40-137">List item 2</span></span>
- <span data-ttu-id="f0e40-138">Lijstitem 3</span><span class="sxs-lookup"><span data-stu-id="f0e40-138">List item 3</span></span>

<span data-ttu-id="f0e40-139">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f0e40-140">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0e40-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="f0e40-141">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-141">will be rendered as:</span></span>

- <span data-ttu-id="f0e40-142">Lijstitem 1</span><span class="sxs-lookup"><span data-stu-id="f0e40-142">List item 1</span></span>
  - <span data-ttu-id="f0e40-143">Lijstitem A</span><span class="sxs-lookup"><span data-stu-id="f0e40-143">List item A</span></span>
  - <span data-ttu-id="f0e40-144">Lijstitem B</span><span class="sxs-lookup"><span data-stu-id="f0e40-144">List item B</span></span>
- <span data-ttu-id="f0e40-145">Lijstitem 2</span><span class="sxs-lookup"><span data-stu-id="f0e40-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="f0e40-146">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="f0e40-146">Ordered list</span></span>

<span data-ttu-id="f0e40-147">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="f0e40-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="f0e40-148">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0e40-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="f0e40-149">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-149">will be rendered as:</span></span>

1. <span data-ttu-id="f0e40-150">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-150">First instruction</span></span>
2. <span data-ttu-id="f0e40-151">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-151">Second instruction</span></span>
3. <span data-ttu-id="f0e40-152">Derde instructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-152">Third instruction</span></span>

<span data-ttu-id="f0e40-153">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f0e40-154">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0e40-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="f0e40-155">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-155">will be rendered as:</span></span>

1. <span data-ttu-id="f0e40-156">Eerste instructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-156">First instruction</span></span>
   1. <span data-ttu-id="f0e40-157">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-157">Sub-instruction</span></span>
   2. <span data-ttu-id="f0e40-158">Subinstructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-158">Sub-instruction</span></span>
2. <span data-ttu-id="f0e40-159">Tweede instructie</span><span class="sxs-lookup"><span data-stu-id="f0e40-159">Second instruction</span></span>

<span data-ttu-id="f0e40-160">Merk op dat we '1.' gebruiken</span><span class="sxs-lookup"><span data-stu-id="f0e40-160">Note that we use '1.'</span></span> <span data-ttu-id="f0e40-161">voor alle vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-161">for all entries.</span></span> <span data-ttu-id="f0e40-162">Hierdoor is het eenvoudiger om later verschillen te beoordelen als er in latere updates nieuwe stappen worden toegevoegd of bestaande stappen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f0e40-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="f0e40-163">Tabellen</span><span class="sxs-lookup"><span data-stu-id="f0e40-163">Tables</span></span>

<span data-ttu-id="f0e40-164">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="f0e40-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="f0e40-165">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="f0e40-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="f0e40-166">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="f0e40-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="f0e40-167">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f0e40-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="f0e40-168">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0e40-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="f0e40-169">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-169">will be rendered as:</span></span>

| <span data-ttu-id="f0e40-170">Pret</span><span class="sxs-lookup"><span data-stu-id="f0e40-170">Fun</span></span>                  | <span data-ttu-id="f0e40-171">met</span><span class="sxs-lookup"><span data-stu-id="f0e40-171">With</span></span>                 | <span data-ttu-id="f0e40-172">Tabellen</span><span class="sxs-lookup"><span data-stu-id="f0e40-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="f0e40-173">links uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="f0e40-173">left-aligned column</span></span>  | <span data-ttu-id="f0e40-174">rechts uitgelijnde kolom</span><span class="sxs-lookup"><span data-stu-id="f0e40-174">right-aligned column</span></span> | <span data-ttu-id="f0e40-175">gecentreerde kolom</span><span class="sxs-lookup"><span data-stu-id="f0e40-175">centered column</span></span> |
| <span data-ttu-id="f0e40-176">USD 100</span><span class="sxs-lookup"><span data-stu-id="f0e40-176">$100</span></span>                 | <span data-ttu-id="f0e40-177">USD 100</span><span class="sxs-lookup"><span data-stu-id="f0e40-177">$100</span></span>                 | <span data-ttu-id="f0e40-178">USD 100</span><span class="sxs-lookup"><span data-stu-id="f0e40-178">$100</span></span>            |
| <span data-ttu-id="f0e40-179">USD 10</span><span class="sxs-lookup"><span data-stu-id="f0e40-179">$10</span></span>                  | <span data-ttu-id="f0e40-180">USD 10</span><span class="sxs-lookup"><span data-stu-id="f0e40-180">$10</span></span>                  | <span data-ttu-id="f0e40-181">USD 10</span><span class="sxs-lookup"><span data-stu-id="f0e40-181">$10</span></span>             |
| <span data-ttu-id="f0e40-182">USD 1</span><span class="sxs-lookup"><span data-stu-id="f0e40-182">$1</span></span>                   | <span data-ttu-id="f0e40-183">USD 1</span><span class="sxs-lookup"><span data-stu-id="f0e40-183">$1</span></span>                   | <span data-ttu-id="f0e40-184">USD 1</span><span class="sxs-lookup"><span data-stu-id="f0e40-184">$1</span></span>              |

<span data-ttu-id="f0e40-185">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="f0e40-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="f0e40-186">De [functie voor tabelterugloop](#table-wrapping) van Markdig biedt ondersteuning bij het opmaken van brede tabellen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="f0e40-187">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="f0e40-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="f0e40-188">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="f0e40-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="f0e40-189">[Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="f0e40-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="f0e40-190">[Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="f0e40-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="f0e40-191">[HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="f0e40-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="f0e40-192">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="f0e40-192">Links</span></span>

<span data-ttu-id="f0e40-193">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="f0e40-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="f0e40-194">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="f0e40-194">For more information on linking, see:</span></span>

- <span data-ttu-id="f0e40-195">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="f0e40-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="f0e40-196">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over de aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.</span><span class="sxs-lookup"><span data-stu-id="f0e40-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="f0e40-197">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="f0e40-197">Code snippets</span></span>

<span data-ttu-id="f0e40-198">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="f0e40-199">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="f0e40-199">For details, see:</span></span>

- [<span data-ttu-id="f0e40-200">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="f0e40-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="f0e40-201">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="f0e40-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="f0e40-202">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="f0e40-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="f0e40-203">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="f0e40-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="f0e40-204">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f0e40-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="f0e40-205">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="f0e40-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="f0e40-206">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="f0e40-207">Naam</span><span class="sxs-lookup"><span data-stu-id="f0e40-207">Name</span></span>|<span data-ttu-id="f0e40-208">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="f0e40-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="f0e40-209">.NET Console</span><span class="sxs-lookup"><span data-stu-id="f0e40-209">.NET Console</span></span>|<span data-ttu-id="f0e40-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="f0e40-210">dotnetcli</span></span>|
|<span data-ttu-id="f0e40-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="f0e40-211">ASP.NET (C#)</span></span>|<span data-ttu-id="f0e40-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="f0e40-212">aspx-csharp</span></span>|
|<span data-ttu-id="f0e40-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="f0e40-213">ASP.NET (VB)</span></span>|<span data-ttu-id="f0e40-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="f0e40-214">aspx-vb</span></span>|
|<span data-ttu-id="f0e40-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f0e40-215">AzCopy</span></span>|<span data-ttu-id="f0e40-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="f0e40-216">azcopy</span></span>|
|<span data-ttu-id="f0e40-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f0e40-217">Azure CLI</span></span>|<span data-ttu-id="f0e40-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="f0e40-218">azurecli</span></span>|
|<span data-ttu-id="f0e40-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0e40-219">Azure PowerShell</span></span>|<span data-ttu-id="f0e40-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="f0e40-220">azurepowershell</span></span>|
|<span data-ttu-id="f0e40-221">C++</span><span class="sxs-lookup"><span data-stu-id="f0e40-221">C++</span></span>|<span data-ttu-id="f0e40-222">cpp</span><span class="sxs-lookup"><span data-stu-id="f0e40-222">cpp</span></span>|
|<span data-ttu-id="f0e40-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="f0e40-223">C++/CX</span></span>|<span data-ttu-id="f0e40-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="f0e40-224">cppcx</span></span>|
|<span data-ttu-id="f0e40-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="f0e40-225">C++/WinRT</span></span>|<span data-ttu-id="f0e40-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="f0e40-226">cppwinrt</span></span>|
|<span data-ttu-id="f0e40-227">C#</span><span class="sxs-lookup"><span data-stu-id="f0e40-227">C#</span></span>|<span data-ttu-id="f0e40-228">csharp</span><span class="sxs-lookup"><span data-stu-id="f0e40-228">csharp</span></span>|
|<span data-ttu-id="f0e40-229">C# in browser</span><span class="sxs-lookup"><span data-stu-id="f0e40-229">C# in browser</span></span>|<span data-ttu-id="f0e40-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="f0e40-230">csharp-interactive</span></span>|
|<span data-ttu-id="f0e40-231">Console</span><span class="sxs-lookup"><span data-stu-id="f0e40-231">Console</span></span>|<span data-ttu-id="f0e40-232">console</span><span class="sxs-lookup"><span data-stu-id="f0e40-232">console</span></span>|
|<span data-ttu-id="f0e40-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="f0e40-233">CSHTML</span></span>|<span data-ttu-id="f0e40-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="f0e40-234">cshtml</span></span>|
|<span data-ttu-id="f0e40-235">DAX</span><span class="sxs-lookup"><span data-stu-id="f0e40-235">DAX</span></span>|<span data-ttu-id="f0e40-236">dax</span><span class="sxs-lookup"><span data-stu-id="f0e40-236">dax</span></span>|
|<span data-ttu-id="f0e40-237">F#</span><span class="sxs-lookup"><span data-stu-id="f0e40-237">F#</span></span>|<span data-ttu-id="f0e40-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="f0e40-238">fsharp</span></span>|
|<span data-ttu-id="f0e40-239">Go</span><span class="sxs-lookup"><span data-stu-id="f0e40-239">Go</span></span>|<span data-ttu-id="f0e40-240">go</span><span class="sxs-lookup"><span data-stu-id="f0e40-240">go</span></span>|
|<span data-ttu-id="f0e40-241">HTML</span><span class="sxs-lookup"><span data-stu-id="f0e40-241">HTML</span></span>|<span data-ttu-id="f0e40-242">html</span><span class="sxs-lookup"><span data-stu-id="f0e40-242">html</span></span>|
|<span data-ttu-id="f0e40-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0e40-243">HTTP</span></span>|<span data-ttu-id="f0e40-244">http</span><span class="sxs-lookup"><span data-stu-id="f0e40-244">http</span></span>|
|<span data-ttu-id="f0e40-245">Java</span><span class="sxs-lookup"><span data-stu-id="f0e40-245">Java</span></span>|<span data-ttu-id="f0e40-246">java</span><span class="sxs-lookup"><span data-stu-id="f0e40-246">java</span></span>|
|<span data-ttu-id="f0e40-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f0e40-247">JavaScript</span></span>|<span data-ttu-id="f0e40-248">javascript</span><span class="sxs-lookup"><span data-stu-id="f0e40-248">javascript</span></span>|
|<span data-ttu-id="f0e40-249">JSON</span><span class="sxs-lookup"><span data-stu-id="f0e40-249">JSON</span></span>|<span data-ttu-id="f0e40-250">json</span><span class="sxs-lookup"><span data-stu-id="f0e40-250">json</span></span>|
|<span data-ttu-id="f0e40-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-251">Markdown</span></span>|<span data-ttu-id="f0e40-252">md</span><span class="sxs-lookup"><span data-stu-id="f0e40-252">md</span></span>|
|<span data-ttu-id="f0e40-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="f0e40-253">NodeJS</span></span>|<span data-ttu-id="f0e40-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="f0e40-254">nodejs</span></span>|
|<span data-ttu-id="f0e40-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f0e40-255">Objective-C</span></span>|<span data-ttu-id="f0e40-256">objc</span><span class="sxs-lookup"><span data-stu-id="f0e40-256">objc</span></span>|
|<span data-ttu-id="f0e40-257">OData</span><span class="sxs-lookup"><span data-stu-id="f0e40-257">OData</span></span>|<span data-ttu-id="f0e40-258">odata</span><span class="sxs-lookup"><span data-stu-id="f0e40-258">odata</span></span>|
|<span data-ttu-id="f0e40-259">PHP</span><span class="sxs-lookup"><span data-stu-id="f0e40-259">PHP</span></span>|<span data-ttu-id="f0e40-260">php</span><span class="sxs-lookup"><span data-stu-id="f0e40-260">php</span></span>|
|<span data-ttu-id="f0e40-261">PowerApps (decimale punt als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="f0e40-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="f0e40-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="f0e40-262">powerapps-dot</span></span>|
|<span data-ttu-id="f0e40-263">PowerApps (decimale komma als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="f0e40-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="f0e40-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="f0e40-264">powerapps-comma</span></span>|
|<span data-ttu-id="f0e40-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0e40-265">PowerShell</span></span>|<span data-ttu-id="f0e40-266">powershell</span><span class="sxs-lookup"><span data-stu-id="f0e40-266">powershell</span></span>|
|<span data-ttu-id="f0e40-267">Python</span><span class="sxs-lookup"><span data-stu-id="f0e40-267">Python</span></span>|<span data-ttu-id="f0e40-268">python</span><span class="sxs-lookup"><span data-stu-id="f0e40-268">python</span></span>|
|<span data-ttu-id="f0e40-269">Q#</span><span class="sxs-lookup"><span data-stu-id="f0e40-269">Q#</span></span>|<span data-ttu-id="f0e40-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="f0e40-270">qsharp</span></span>|
|<span data-ttu-id="f0e40-271">R</span><span class="sxs-lookup"><span data-stu-id="f0e40-271">R</span></span>|<span data-ttu-id="f0e40-272">r</span><span class="sxs-lookup"><span data-stu-id="f0e40-272">r</span></span>|
|<span data-ttu-id="f0e40-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="f0e40-273">Ruby</span></span>|<span data-ttu-id="f0e40-274">ruby</span><span class="sxs-lookup"><span data-stu-id="f0e40-274">ruby</span></span>|
|<span data-ttu-id="f0e40-275">SQL</span><span class="sxs-lookup"><span data-stu-id="f0e40-275">SQL</span></span>|<span data-ttu-id="f0e40-276">sql</span><span class="sxs-lookup"><span data-stu-id="f0e40-276">sql</span></span>|
|<span data-ttu-id="f0e40-277">Swift</span><span class="sxs-lookup"><span data-stu-id="f0e40-277">Swift</span></span>|<span data-ttu-id="f0e40-278">swift</span><span class="sxs-lookup"><span data-stu-id="f0e40-278">swift</span></span>|
|<span data-ttu-id="f0e40-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="f0e40-279">TypeScript</span></span>|<span data-ttu-id="f0e40-280">typescript</span><span class="sxs-lookup"><span data-stu-id="f0e40-280">typescript</span></span>|
|<span data-ttu-id="f0e40-281">VB</span><span class="sxs-lookup"><span data-stu-id="f0e40-281">VB</span></span>|<span data-ttu-id="f0e40-282">vb</span><span class="sxs-lookup"><span data-stu-id="f0e40-282">vb</span></span>|
|<span data-ttu-id="f0e40-283">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="f0e40-283">VSTS CLI</span></span>|<span data-ttu-id="f0e40-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="f0e40-284">vstscli</span></span>|
|<span data-ttu-id="f0e40-285">XAML</span><span class="sxs-lookup"><span data-stu-id="f0e40-285">XAML</span></span>|<span data-ttu-id="f0e40-286">xaml</span><span class="sxs-lookup"><span data-stu-id="f0e40-286">xaml</span></span>|
|<span data-ttu-id="f0e40-287">XML</span><span class="sxs-lookup"><span data-stu-id="f0e40-287">XML</span></span>|<span data-ttu-id="f0e40-288">xml</span><span class="sxs-lookup"><span data-stu-id="f0e40-288">xml</span></span>|

<span data-ttu-id="f0e40-289">De naam `csharp-interactive` geeft de taal C# aan en de mogelijkheid om de voorbeelden uit te voeren vanuit de browser.</span><span class="sxs-lookup"><span data-stu-id="f0e40-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="f0e40-290">Deze codefragmenten worden gecompileerd en uitgevoerd in een Docker-container, en de resultaten van het uitvoeren van het programma worden weergegeven in het browservenster van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="f0e40-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="f0e40-291">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="f0e40-291">Example: C\#</span></span>

<span data-ttu-id="f0e40-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f0e40-292">__Markdown__</span></span>

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

<span data-ttu-id="f0e40-293">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="f0e40-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="f0e40-294">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="f0e40-294">Example: SQL</span></span>

<span data-ttu-id="f0e40-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f0e40-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="f0e40-296">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="f0e40-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="f0e40-297">Aangepaste OPS-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="f0e40-298">Met OPS (Open Publishing Services) wordt Markdig Parser for Markdown geïmplementeerd, dat zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="f0e40-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="f0e40-299">Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="f0e40-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="f0e40-300">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="f0e40-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="f0e40-301">(Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="f0e40-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="f0e40-302">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="f0e40-303">Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="f0e40-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="f0e40-304">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="f0e40-304">Note blocks</span></span>
- <span data-ttu-id="f0e40-305">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="f0e40-305">Include files</span></span>
- <span data-ttu-id="f0e40-306">Selectors</span><span class="sxs-lookup"><span data-stu-id="f0e40-306">Selectors</span></span>
- <span data-ttu-id="f0e40-307">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="f0e40-307">Embedded videos</span></span>
- <span data-ttu-id="f0e40-308">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="f0e40-308">Code snippets/samples</span></span>

<span data-ttu-id="f0e40-309">Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="f0e40-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="f0e40-310">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="f0e40-310">Note blocks</span></span>

<span data-ttu-id="f0e40-311">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="f0e40-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="f0e40-312">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="f0e40-312">NOTE</span></span>
- <span data-ttu-id="f0e40-313">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="f0e40-313">WARNING</span></span>
- <span data-ttu-id="f0e40-314">TIP</span><span class="sxs-lookup"><span data-stu-id="f0e40-314">TIP</span></span>
- <span data-ttu-id="f0e40-315">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="f0e40-315">IMPORTANT</span></span>

<span data-ttu-id="f0e40-316">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="f0e40-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="f0e40-317">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="f0e40-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="f0e40-318">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="f0e40-318">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="f0e40-319">Deze worden als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="f0e40-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="f0e40-320">Dit is een OPMERKING</span><span class="sxs-lookup"><span data-stu-id="f0e40-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="f0e40-321">Dit is een WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="f0e40-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="f0e40-322">Dit is een TIP</span><span class="sxs-lookup"><span data-stu-id="f0e40-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0e40-323">Dit is BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="f0e40-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="f0e40-324">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="f0e40-324">Include files</span></span>

<span data-ttu-id="f0e40-325">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="f0e40-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="f0e40-326">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="f0e40-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="f0e40-327">Er zijn drie soorten insluitingsverwijzingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="f0e40-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="f0e40-328">Inline: Een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="f0e40-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="f0e40-329">Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="f0e40-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="f0e40-330">Afbeelding: Op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="f0e40-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="f0e40-331">Een inline- of blokinsluitingsbestand is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="f0e40-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="f0e40-332">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="f0e40-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="f0e40-333">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="f0e40-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="f0e40-334">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="f0e40-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="f0e40-335">Dit zijn de vereisten en overwegingen voor insluitingsbestanden:</span><span class="sxs-lookup"><span data-stu-id="f0e40-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="f0e40-336">Gebruik een insluitingsbestand wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f0e40-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="f0e40-337">Gebruik een blokinsluitingsverwijzing voor aanzienlijke hoeveelheden inhoud: enkele alinea's, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="f0e40-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="f0e40-338">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="f0e40-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="f0e40-339">Insluitingsverwijzingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikel, omdat ze afhankelijk zijn van Markdig-extensies.</span><span class="sxs-lookup"><span data-stu-id="f0e40-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="f0e40-340">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="f0e40-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="f0e40-341">Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar het insluitingsbestand wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="f0e40-342">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="f0e40-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="f0e40-343">Voeg geen insluitingsverwijzingen in andere insluitingsbestanden in.</span><span class="sxs-lookup"><span data-stu-id="f0e40-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="f0e40-344">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f0e40-344">They are not supported.</span></span>
- <span data-ttu-id="f0e40-345">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="f0e40-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="f0e40-346">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="f0e40-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="f0e40-347">Als het insluitingsbestand geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f0e40-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="f0e40-348">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="f0e40-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="f0e40-349">Gebruik een afzonderlijk bestand met een unieke naam voor elk insluitingsbestand en artikel.</span><span class="sxs-lookup"><span data-stu-id="f0e40-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="f0e40-350">Sla het mediabestand op in de mediamap die is gekoppeld aan het insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="f0e40-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="f0e40-351">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="f0e40-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="f0e40-352">Insluitingsbestanden dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="f0e40-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="f0e40-353">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="f0e40-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="f0e40-354">Selectors</span><span class="sxs-lookup"><span data-stu-id="f0e40-354">Selectors</span></span>

<span data-ttu-id="f0e40-355">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of op verschillende platformen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="f0e40-356">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="f0e40-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="f0e40-357">Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="f0e40-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="f0e40-358">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="f0e40-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="f0e40-359">Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f0e40-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="f0e40-360">Hier volgt een voorbeeld van een selector:</span><span class="sxs-lookup"><span data-stu-id="f0e40-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="f0e40-361">U kunt een praktijkvoorbeeld van selectors bekijken in [Azure Docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="f0e40-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="f0e40-362">Insluitingsverwijzingen van code</span><span class="sxs-lookup"><span data-stu-id="f0e40-362">Code include references</span></span>

<span data-ttu-id="f0e40-363">Markdig ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="f0e40-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="f0e40-364">Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:</span><span class="sxs-lookup"><span data-stu-id="f0e40-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="f0e40-365">Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="f0e40-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="f0e40-366">Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="f0e40-367">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f0e40-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="f0e40-368">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="f0e40-368">Alt text</span></span>

<span data-ttu-id="f0e40-369">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f0e40-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="f0e40-370">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="f0e40-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="f0e40-371">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="f0e40-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="f0e40-372">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="f0e40-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="f0e40-373">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="f0e40-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="f0e40-374">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="f0e40-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="f0e40-375">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="f0e40-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="f0e40-376">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="f0e40-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="f0e40-377">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="f0e40-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="f0e40-378">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="f0e40-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="f0e40-379">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="f0e40-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="f0e40-380">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="f0e40-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="f0e40-381">Punthaken</span><span class="sxs-lookup"><span data-stu-id="f0e40-381">Angle brackets</span></span>

<span data-ttu-id="f0e40-382">Het is gebruikelijk punthaken te gebruiken om een tijdelijke aanduiding aan te geven.</span><span class="sxs-lookup"><span data-stu-id="f0e40-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="f0e40-383">Als u dit in tekst doet (dus niet in code), moet u de punthaken coderen.</span><span class="sxs-lookup"><span data-stu-id="f0e40-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="f0e40-384">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="f0e40-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="f0e40-385">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="f0e40-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="f0e40-386">Zie ook:</span><span class="sxs-lookup"><span data-stu-id="f0e40-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="f0e40-387">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="f0e40-387">Markdown resources</span></span>

- [<span data-ttu-id="f0e40-388">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="f0e40-389">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="f0e40-390">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="f0e40-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="f0e40-391">De Markdown-handleiding</span><span class="sxs-lookup"><span data-stu-id="f0e40-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
