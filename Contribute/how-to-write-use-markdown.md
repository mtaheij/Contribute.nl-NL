---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: ffc44f07929890ef17b3878ba389dfeea82691a6
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592465"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="b3dba-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="b3dba-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="b3dba-104">Artikelen op [docs.microsoft.com](https://docs.microsoft.com) worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="b3dba-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="b3dba-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="b3dba-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="b3dba-106">De docs-site maakt gebruik van de [Markdig-variant](#markdown-flavor) van Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3dba-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="b3dba-107">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="b3dba-108">Koppen</span><span class="sxs-lookup"><span data-stu-id="b3dba-108">Headings</span></span>

<span data-ttu-id="b3dba-109">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="b3dba-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="b3dba-110">Headers moeten in ATX-stijl worden gemaakt, dat wil zeggen dat aan het begin van de regel 1 tot 6 hekjes (#) moeten staan om een header aan te duiden overeenkomstig de HTML-headerniveaus H1 tot H6.</span><span class="sxs-lookup"><span data-stu-id="b3dba-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="b3dba-111">Hierboven vindt u voorbeelden van headers van het eerste tot vierde niveau.</span><span class="sxs-lookup"><span data-stu-id="b3dba-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="b3dba-112">Uw onderwerp **mag** maar één header van het eerste niveau (H1) bevatten. Deze wordt op de pagina weergegeven als de titel.</span><span class="sxs-lookup"><span data-stu-id="b3dba-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="b3dba-113">Als uw header met een `#` eindigt, moet u aan het eind nog een `#` toevoegen zodat de titel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b3dba-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="b3dba-114">Bijvoorbeeld `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="b3dba-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="b3dba-115">Met de headers op het tweede niveau wordt de inhoudsopgave op de pagina gegenereerd die wordt weergegeven in de sectie 'In dit artikel' onder de titel op de pagina.</span><span class="sxs-lookup"><span data-stu-id="b3dba-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="b3dba-116">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="b3dba-116">Bold and italic text</span></span>

<span data-ttu-id="b3dba-117">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="b3dba-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="b3dba-118">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="b3dba-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="b3dba-119">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="b3dba-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="b3dba-120">Blokcitaten</span><span class="sxs-lookup"><span data-stu-id="b3dba-120">Blockquotes</span></span>

<span data-ttu-id="b3dba-121">Blokcitaten worden gemaakt met het teken `>`:</span><span class="sxs-lookup"><span data-stu-id="b3dba-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="b3dba-122">Het voorbeeld hierboven wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b3dba-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="b3dba-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="b3dba-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="b3dba-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="b3dba-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="b3dba-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="b3dba-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="b3dba-126">Lijsten</span><span class="sxs-lookup"><span data-stu-id="b3dba-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="b3dba-127">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="b3dba-127">Unordered list</span></span>

<span data-ttu-id="b3dba-128">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b3dba-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="b3dba-129">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3dba-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="b3dba-130">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-130">will be rendered as:</span></span>

- <span data-ttu-id="b3dba-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="b3dba-131">List item 1</span></span>
- <span data-ttu-id="b3dba-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="b3dba-132">List item 2</span></span>
- <span data-ttu-id="b3dba-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="b3dba-133">List item 3</span></span>

<span data-ttu-id="b3dba-134">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b3dba-135">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3dba-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="b3dba-136">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-136">will be rendered as:</span></span>

- <span data-ttu-id="b3dba-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="b3dba-137">List item 1</span></span>
  - <span data-ttu-id="b3dba-138">List item A</span><span class="sxs-lookup"><span data-stu-id="b3dba-138">List item A</span></span>
  - <span data-ttu-id="b3dba-139">List item B</span><span class="sxs-lookup"><span data-stu-id="b3dba-139">List item B</span></span>
- <span data-ttu-id="b3dba-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="b3dba-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="b3dba-141">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="b3dba-141">Ordered list</span></span>

<span data-ttu-id="b3dba-142">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="b3dba-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="b3dba-143">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3dba-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="b3dba-144">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-144">will be rendered as:</span></span>

1. <span data-ttu-id="b3dba-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-145">First instruction</span></span>
2. <span data-ttu-id="b3dba-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-146">Second instruction</span></span>
3. <span data-ttu-id="b3dba-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-147">Third instruction</span></span>

<span data-ttu-id="b3dba-148">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b3dba-149">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3dba-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="b3dba-150">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-150">will be rendered as:</span></span>

1. <span data-ttu-id="b3dba-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-151">First instruction</span></span>
   1. <span data-ttu-id="b3dba-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-152">Sub-instruction</span></span>
   2. <span data-ttu-id="b3dba-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-153">Sub-instruction</span></span>
2. <span data-ttu-id="b3dba-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b3dba-154">Second instruction</span></span>

<span data-ttu-id="b3dba-155">Merk op dat we '1.' gebruiken</span><span class="sxs-lookup"><span data-stu-id="b3dba-155">Note that we use '1.'</span></span> <span data-ttu-id="b3dba-156">voor alle vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-156">for all entries.</span></span> <span data-ttu-id="b3dba-157">Hierdoor is het eenvoudiger om later verschillen te beoordelen als er in latere updates nieuwe stappen worden toegevoegd of bestaande stappen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="b3dba-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="b3dba-158">Tabellen</span><span class="sxs-lookup"><span data-stu-id="b3dba-158">Tables</span></span>

<span data-ttu-id="b3dba-159">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="b3dba-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="b3dba-160">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="b3dba-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="b3dba-161">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="b3dba-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="b3dba-162">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b3dba-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="b3dba-163">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3dba-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="b3dba-164">Wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-164">Will be rendered as:</span></span>

| <span data-ttu-id="b3dba-165">Fun</span><span class="sxs-lookup"><span data-stu-id="b3dba-165">Fun</span></span>                  | <span data-ttu-id="b3dba-166">With</span><span class="sxs-lookup"><span data-stu-id="b3dba-166">With</span></span>                 | <span data-ttu-id="b3dba-167">Tables</span><span class="sxs-lookup"><span data-stu-id="b3dba-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="b3dba-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="b3dba-168">left-aligned column</span></span>  | <span data-ttu-id="b3dba-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="b3dba-169">right-aligned column</span></span> | <span data-ttu-id="b3dba-170">centered column</span><span class="sxs-lookup"><span data-stu-id="b3dba-170">centered column</span></span> |
| <span data-ttu-id="b3dba-171">$100</span><span class="sxs-lookup"><span data-stu-id="b3dba-171">$100</span></span>                 | <span data-ttu-id="b3dba-172">$100</span><span class="sxs-lookup"><span data-stu-id="b3dba-172">$100</span></span>                 | <span data-ttu-id="b3dba-173">$100</span><span class="sxs-lookup"><span data-stu-id="b3dba-173">$100</span></span>            |
| <span data-ttu-id="b3dba-174">$10</span><span class="sxs-lookup"><span data-stu-id="b3dba-174">$10</span></span>                  | <span data-ttu-id="b3dba-175">$10</span><span class="sxs-lookup"><span data-stu-id="b3dba-175">$10</span></span>                  | <span data-ttu-id="b3dba-176">$10</span><span class="sxs-lookup"><span data-stu-id="b3dba-176">$10</span></span>             |
| <span data-ttu-id="b3dba-177">$1</span><span class="sxs-lookup"><span data-stu-id="b3dba-177">$1</span></span>                   | <span data-ttu-id="b3dba-178">$1</span><span class="sxs-lookup"><span data-stu-id="b3dba-178">$1</span></span>                   | <span data-ttu-id="b3dba-179">$1</span><span class="sxs-lookup"><span data-stu-id="b3dba-179">$1</span></span>              |

<span data-ttu-id="b3dba-180">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="b3dba-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="b3dba-181">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="b3dba-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="b3dba-182">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="b3dba-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="b3dba-183">[Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="b3dba-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="b3dba-184">[Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="b3dba-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="b3dba-185">[HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="b3dba-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="b3dba-186">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="b3dba-186">Links</span></span>

<span data-ttu-id="b3dba-187">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="b3dba-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="b3dba-188">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="b3dba-188">For more information on linking, see:</span></span>

- <span data-ttu-id="b3dba-189">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3dba-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="b3dba-190">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over de aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.</span><span class="sxs-lookup"><span data-stu-id="b3dba-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="b3dba-191">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="b3dba-191">Code snippets</span></span>

<span data-ttu-id="b3dba-192">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="b3dba-193">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="b3dba-193">For details, see:</span></span>

- [<span data-ttu-id="b3dba-194">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="b3dba-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="b3dba-195">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="b3dba-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="b3dba-196">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="b3dba-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="b3dba-197">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="b3dba-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="b3dba-198">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3dba-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="b3dba-199">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="b3dba-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="b3dba-200">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="b3dba-201">Naam</span><span class="sxs-lookup"><span data-stu-id="b3dba-201">Name</span></span>|<span data-ttu-id="b3dba-202">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="b3dba-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="b3dba-203">.NET Console</span><span class="sxs-lookup"><span data-stu-id="b3dba-203">.NET Console</span></span>|<span data-ttu-id="b3dba-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="b3dba-204">dotnetcli</span></span>|
|<span data-ttu-id="b3dba-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="b3dba-205">ASP.NET (C#)</span></span>|<span data-ttu-id="b3dba-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="b3dba-206">aspx-csharp</span></span>|
|<span data-ttu-id="b3dba-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="b3dba-207">ASP.NET (VB)</span></span>|<span data-ttu-id="b3dba-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="b3dba-208">aspx-vb</span></span>|
|<span data-ttu-id="b3dba-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="b3dba-209">AzCopy</span></span>|<span data-ttu-id="b3dba-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="b3dba-210">azcopy</span></span>|
|<span data-ttu-id="b3dba-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b3dba-211">Azure CLI</span></span>|<span data-ttu-id="b3dba-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="b3dba-212">azurecli</span></span>|
|<span data-ttu-id="b3dba-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3dba-213">Azure PowerShell</span></span>|<span data-ttu-id="b3dba-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="b3dba-214">azurepowershell</span></span>|
|<span data-ttu-id="b3dba-215">Bash</span><span class="sxs-lookup"><span data-stu-id="b3dba-215">Bash</span></span>|<span data-ttu-id="b3dba-216">bash</span><span class="sxs-lookup"><span data-stu-id="b3dba-216">bash</span></span>|
|<span data-ttu-id="b3dba-217">C++</span><span class="sxs-lookup"><span data-stu-id="b3dba-217">C++</span></span>|<span data-ttu-id="b3dba-218">cpp</span><span class="sxs-lookup"><span data-stu-id="b3dba-218">cpp</span></span>|
|<span data-ttu-id="b3dba-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="b3dba-219">C++/CX</span></span>|<span data-ttu-id="b3dba-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="b3dba-220">cppcx</span></span>|
|<span data-ttu-id="b3dba-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="b3dba-221">C++/WinRT</span></span>|<span data-ttu-id="b3dba-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="b3dba-222">cppwinrt</span></span>|
|<span data-ttu-id="b3dba-223">C#</span><span class="sxs-lookup"><span data-stu-id="b3dba-223">C#</span></span>|<span data-ttu-id="b3dba-224">csharp</span><span class="sxs-lookup"><span data-stu-id="b3dba-224">csharp</span></span>|
|<span data-ttu-id="b3dba-225">C# in browser</span><span class="sxs-lookup"><span data-stu-id="b3dba-225">C# in browser</span></span>|<span data-ttu-id="b3dba-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="b3dba-226">csharp-interactive</span></span>|
|<span data-ttu-id="b3dba-227">Console</span><span class="sxs-lookup"><span data-stu-id="b3dba-227">Console</span></span>|<span data-ttu-id="b3dba-228">console</span><span class="sxs-lookup"><span data-stu-id="b3dba-228">console</span></span>|
|<span data-ttu-id="b3dba-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="b3dba-229">CSHTML</span></span>|<span data-ttu-id="b3dba-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="b3dba-230">cshtml</span></span>|
|<span data-ttu-id="b3dba-231">DAX</span><span class="sxs-lookup"><span data-stu-id="b3dba-231">DAX</span></span>|<span data-ttu-id="b3dba-232">dax</span><span class="sxs-lookup"><span data-stu-id="b3dba-232">dax</span></span>|
|<span data-ttu-id="b3dba-233">Docker</span><span class="sxs-lookup"><span data-stu-id="b3dba-233">Docker</span></span>|<span data-ttu-id="b3dba-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="b3dba-234">dockerfile</span></span>|
|<span data-ttu-id="b3dba-235">F#</span><span class="sxs-lookup"><span data-stu-id="b3dba-235">F#</span></span>|<span data-ttu-id="b3dba-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="b3dba-236">fsharp</span></span>|
|<span data-ttu-id="b3dba-237">Go</span><span class="sxs-lookup"><span data-stu-id="b3dba-237">Go</span></span>|<span data-ttu-id="b3dba-238">go</span><span class="sxs-lookup"><span data-stu-id="b3dba-238">go</span></span>|
|<span data-ttu-id="b3dba-239">HTML</span><span class="sxs-lookup"><span data-stu-id="b3dba-239">HTML</span></span>|<span data-ttu-id="b3dba-240">html</span><span class="sxs-lookup"><span data-stu-id="b3dba-240">html</span></span>|
|<span data-ttu-id="b3dba-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="b3dba-241">HTTP</span></span>|<span data-ttu-id="b3dba-242">http</span><span class="sxs-lookup"><span data-stu-id="b3dba-242">http</span></span>|
|<span data-ttu-id="b3dba-243">Java</span><span class="sxs-lookup"><span data-stu-id="b3dba-243">Java</span></span>|<span data-ttu-id="b3dba-244">java</span><span class="sxs-lookup"><span data-stu-id="b3dba-244">java</span></span>|
|<span data-ttu-id="b3dba-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b3dba-245">JavaScript</span></span>|<span data-ttu-id="b3dba-246">javascript</span><span class="sxs-lookup"><span data-stu-id="b3dba-246">javascript</span></span>|
|<span data-ttu-id="b3dba-247">JSON</span><span class="sxs-lookup"><span data-stu-id="b3dba-247">JSON</span></span>|<span data-ttu-id="b3dba-248">json</span><span class="sxs-lookup"><span data-stu-id="b3dba-248">json</span></span>|
|<span data-ttu-id="b3dba-249">Kusto-querytaal</span><span class="sxs-lookup"><span data-stu-id="b3dba-249">Kusto Query Language</span></span>|<span data-ttu-id="b3dba-250">kusto</span><span class="sxs-lookup"><span data-stu-id="b3dba-250">kusto</span></span>|
|<span data-ttu-id="b3dba-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-251">Markdown</span></span>|<span data-ttu-id="b3dba-252">md</span><span class="sxs-lookup"><span data-stu-id="b3dba-252">md</span></span>|
|<span data-ttu-id="b3dba-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b3dba-253">Objective-C</span></span>|<span data-ttu-id="b3dba-254">objc</span><span class="sxs-lookup"><span data-stu-id="b3dba-254">objc</span></span>|
|<span data-ttu-id="b3dba-255">OData</span><span class="sxs-lookup"><span data-stu-id="b3dba-255">OData</span></span>|<span data-ttu-id="b3dba-256">odata</span><span class="sxs-lookup"><span data-stu-id="b3dba-256">odata</span></span>|
|<span data-ttu-id="b3dba-257">PHP</span><span class="sxs-lookup"><span data-stu-id="b3dba-257">PHP</span></span>|<span data-ttu-id="b3dba-258">php</span><span class="sxs-lookup"><span data-stu-id="b3dba-258">php</span></span>|
|<span data-ttu-id="b3dba-259">PowerApps (decimale punt als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="b3dba-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="b3dba-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="b3dba-260">powerapps-dot</span></span>|
|<span data-ttu-id="b3dba-261">PowerApps (decimale komma als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="b3dba-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="b3dba-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="b3dba-262">powerapps-comma</span></span>|
|<span data-ttu-id="b3dba-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3dba-263">PowerShell</span></span>|<span data-ttu-id="b3dba-264">powershell</span><span class="sxs-lookup"><span data-stu-id="b3dba-264">powershell</span></span>|
|<span data-ttu-id="b3dba-265">Python</span><span class="sxs-lookup"><span data-stu-id="b3dba-265">Python</span></span>|<span data-ttu-id="b3dba-266">python</span><span class="sxs-lookup"><span data-stu-id="b3dba-266">python</span></span>|
|<span data-ttu-id="b3dba-267">Q#</span><span class="sxs-lookup"><span data-stu-id="b3dba-267">Q#</span></span>|<span data-ttu-id="b3dba-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="b3dba-268">qsharp</span></span>|
|<span data-ttu-id="b3dba-269">R</span><span class="sxs-lookup"><span data-stu-id="b3dba-269">R</span></span>|<span data-ttu-id="b3dba-270">r</span><span class="sxs-lookup"><span data-stu-id="b3dba-270">r</span></span>|
|<span data-ttu-id="b3dba-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="b3dba-271">Ruby</span></span>|<span data-ttu-id="b3dba-272">ruby</span><span class="sxs-lookup"><span data-stu-id="b3dba-272">ruby</span></span>|
|<span data-ttu-id="b3dba-273">SQL</span><span class="sxs-lookup"><span data-stu-id="b3dba-273">SQL</span></span>|<span data-ttu-id="b3dba-274">sql</span><span class="sxs-lookup"><span data-stu-id="b3dba-274">sql</span></span>|
|<span data-ttu-id="b3dba-275">Swift</span><span class="sxs-lookup"><span data-stu-id="b3dba-275">Swift</span></span>|<span data-ttu-id="b3dba-276">swift</span><span class="sxs-lookup"><span data-stu-id="b3dba-276">swift</span></span>|
|<span data-ttu-id="b3dba-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="b3dba-277">TypeScript</span></span>|<span data-ttu-id="b3dba-278">typescript</span><span class="sxs-lookup"><span data-stu-id="b3dba-278">typescript</span></span>|
|<span data-ttu-id="b3dba-279">VB</span><span class="sxs-lookup"><span data-stu-id="b3dba-279">VB</span></span>|<span data-ttu-id="b3dba-280">vb</span><span class="sxs-lookup"><span data-stu-id="b3dba-280">vb</span></span>|
|<span data-ttu-id="b3dba-281">XAML</span><span class="sxs-lookup"><span data-stu-id="b3dba-281">XAML</span></span>|<span data-ttu-id="b3dba-282">xaml</span><span class="sxs-lookup"><span data-stu-id="b3dba-282">xaml</span></span>|
|<span data-ttu-id="b3dba-283">XML</span><span class="sxs-lookup"><span data-stu-id="b3dba-283">XML</span></span>|<span data-ttu-id="b3dba-284">xml</span><span class="sxs-lookup"><span data-stu-id="b3dba-284">xml</span></span>|

<span data-ttu-id="b3dba-285">De naam `csharp-interactive` geeft de taal C# aan en de mogelijkheid om de voorbeelden uit te voeren vanuit de browser.</span><span class="sxs-lookup"><span data-stu-id="b3dba-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="b3dba-286">Deze codefragmenten worden gecompileerd en uitgevoerd in een Docker-container, en de resultaten van het uitvoeren van het programma worden weergegeven in het browservenster van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b3dba-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="b3dba-287">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="b3dba-287">Example: C\#</span></span>

<span data-ttu-id="b3dba-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b3dba-288">__Markdown__</span></span>

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

<span data-ttu-id="b3dba-289">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="b3dba-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="b3dba-290">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="b3dba-290">Example: SQL</span></span>

<span data-ttu-id="b3dba-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b3dba-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="b3dba-292">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="b3dba-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="b3dba-293">Aangepaste Docs-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-293">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="b3dba-294">Met Docs.Microsoft.com wordt een Markdig Parser for Markdown geïmplementeerd, die zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="b3dba-294">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="b3dba-295">Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="b3dba-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="b3dba-296">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="b3dba-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="b3dba-297">(Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="b3dba-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="b3dba-298">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="b3dba-299">Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="b3dba-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="b3dba-300">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="b3dba-300">Note blocks</span></span>
- <span data-ttu-id="b3dba-301">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="b3dba-301">Include files</span></span>
- <span data-ttu-id="b3dba-302">Selectors</span><span class="sxs-lookup"><span data-stu-id="b3dba-302">Selectors</span></span>
- <span data-ttu-id="b3dba-303">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="b3dba-303">Embedded videos</span></span>
- <span data-ttu-id="b3dba-304">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="b3dba-304">Code snippets/samples</span></span>

<span data-ttu-id="b3dba-305">Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="b3dba-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="b3dba-306">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="b3dba-306">Note blocks</span></span>

<span data-ttu-id="b3dba-307">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="b3dba-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="b3dba-308">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="b3dba-308">NOTE</span></span>
- <span data-ttu-id="b3dba-309">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="b3dba-309">WARNING</span></span>
- <span data-ttu-id="b3dba-310">TIP</span><span class="sxs-lookup"><span data-stu-id="b3dba-310">TIP</span></span>
- <span data-ttu-id="b3dba-311">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="b3dba-311">IMPORTANT</span></span>

<span data-ttu-id="b3dba-312">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="b3dba-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="b3dba-313">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="b3dba-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="b3dba-314">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="b3dba-314">Examples:</span></span>

```md
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

<span data-ttu-id="b3dba-315">Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="b3dba-315">These alerts look like this on docs.microsoft.com:</span></span>

![laat zien hoe de waarschuwingen in het vorige voorbeeld eruit zien op de gepubliceerde Docs-pagina met verschillende pictogrammen en kleuren](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="b3dba-317">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="b3dba-317">Include files</span></span>

<span data-ttu-id="b3dba-318">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="b3dba-318">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="b3dba-319">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="b3dba-319">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="b3dba-320">Er zijn drie soorten insluitingsverwijzingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="b3dba-320">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="b3dba-321">Inline: Een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="b3dba-321">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="b3dba-322">Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="b3dba-322">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="b3dba-323">Afbeelding: Op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="b3dba-323">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="b3dba-324">Een inline- of blokinsluitingsbestand is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="b3dba-324">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="b3dba-325">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="b3dba-325">It can contain any valid Markdown.</span></span> <span data-ttu-id="b3dba-326">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="b3dba-326">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="b3dba-327">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="b3dba-327">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="b3dba-328">Dit zijn de vereisten en overwegingen voor insluitingsbestanden:</span><span class="sxs-lookup"><span data-stu-id="b3dba-328">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="b3dba-329">Gebruik een insluitingsbestand wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b3dba-329">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="b3dba-330">Gebruik een blokinsluitingsverwijzing voor aanzienlijke hoeveelheden inhoud: enkele alinea's, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="b3dba-330">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="b3dba-331">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="b3dba-331">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="b3dba-332">Insluitingsverwijzingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikel, omdat ze afhankelijk zijn van Markdig-extensies.</span><span class="sxs-lookup"><span data-stu-id="b3dba-332">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="b3dba-333">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="b3dba-333">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="b3dba-334">Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar het insluitingsbestand wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-334">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="b3dba-335">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="b3dba-335">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="b3dba-336">Voeg geen insluitingsverwijzingen in andere insluitingsbestanden in.</span><span class="sxs-lookup"><span data-stu-id="b3dba-336">Don't embed include references within other include files.</span></span> <span data-ttu-id="b3dba-337">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="b3dba-337">They are not supported.</span></span>
- <span data-ttu-id="b3dba-338">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="b3dba-338">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="b3dba-339">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="b3dba-339">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="b3dba-340">Als het insluitingsbestand geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b3dba-340">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="b3dba-341">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="b3dba-341">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="b3dba-342">Gebruik een afzonderlijk bestand met een unieke naam voor elk insluitingsbestand en artikel.</span><span class="sxs-lookup"><span data-stu-id="b3dba-342">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="b3dba-343">Sla het mediabestand op in de mediamap die is gekoppeld aan het insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="b3dba-343">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="b3dba-344">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="b3dba-344">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="b3dba-345">Insluitingsbestanden dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="b3dba-345">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="b3dba-346">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="b3dba-346">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="b3dba-347">Selectors</span><span class="sxs-lookup"><span data-stu-id="b3dba-347">Selectors</span></span>

<span data-ttu-id="b3dba-348">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of op verschillende platformen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-348">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="b3dba-349">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="b3dba-349">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="b3dba-350">Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="b3dba-350">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="b3dba-351">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="b3dba-351">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="b3dba-352">Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3dba-352">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="b3dba-353">Hier volgt een voorbeeld van een selector:</span><span class="sxs-lookup"><span data-stu-id="b3dba-353">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="b3dba-354">U kunt een praktijkvoorbeeld van selectors bekijken in [Azure Docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="b3dba-354">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="b3dba-355">Insluitingsverwijzingen van code</span><span class="sxs-lookup"><span data-stu-id="b3dba-355">Code include references</span></span>

<span data-ttu-id="b3dba-356">Markdig ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="b3dba-356">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="b3dba-357">Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:</span><span class="sxs-lookup"><span data-stu-id="b3dba-357">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="b3dba-358">Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="b3dba-358">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="b3dba-359">Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-359">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="b3dba-360">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b3dba-360">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="b3dba-361">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="b3dba-361">Alt text</span></span>

<span data-ttu-id="b3dba-362">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b3dba-362">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="b3dba-363">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="b3dba-363">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="b3dba-364">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="b3dba-364">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="b3dba-365">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="b3dba-365">Apostrophes and quotation marks</span></span>

<span data-ttu-id="b3dba-366">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="b3dba-366">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="b3dba-367">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="b3dba-367">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="b3dba-368">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="b3dba-368">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="b3dba-369">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="b3dba-369">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="b3dba-370">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="b3dba-370">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="b3dba-371">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="b3dba-371">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="b3dba-372">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="b3dba-372">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="b3dba-373">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="b3dba-373">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="b3dba-374">Punthaken</span><span class="sxs-lookup"><span data-stu-id="b3dba-374">Angle brackets</span></span>

<span data-ttu-id="b3dba-375">Het is gebruikelijk punthaken te gebruiken om een tijdelijke aanduiding aan te geven.</span><span class="sxs-lookup"><span data-stu-id="b3dba-375">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="b3dba-376">Als u dit in tekst doet (dus niet in code), moet u de punthaken coderen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-376">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="b3dba-377">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="b3dba-377">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="b3dba-378">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="b3dba-378">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="b3dba-379">Markdown-variant</span><span class="sxs-lookup"><span data-stu-id="b3dba-379">Markdown flavor</span></span>

<span data-ttu-id="b3dba-380">De back-end van docs.microsoft.com biedt ondersteuning voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parseerengine [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="b3dba-380">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="b3dba-381">Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="b3dba-381">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="b3dba-382">Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="b3dba-382">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3dba-383">Zie ook:</span><span class="sxs-lookup"><span data-stu-id="b3dba-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="b3dba-384">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="b3dba-384">Markdown resources</span></span>

- [<span data-ttu-id="b3dba-385">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="b3dba-386">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="b3dba-387">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="b3dba-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="b3dba-388">De Markdown-handleiding</span><span class="sxs-lookup"><span data-stu-id="b3dba-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
