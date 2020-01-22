---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111061"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="33a11-103">Markdown gebruiken voor het schrijven van documenten</span><span class="sxs-lookup"><span data-stu-id="33a11-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="33a11-104">Artikelen op [docs.microsoft.com](https://docs.microsoft.com) worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is.</span><span class="sxs-lookup"><span data-stu-id="33a11-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="33a11-105">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="33a11-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="33a11-106">De docs-site maakt gebruik van de [Markdig-variant](#markdown-flavor) van Markdown.</span><span class="sxs-lookup"><span data-stu-id="33a11-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="33a11-107">Basisbeginselen van Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="33a11-108">Koppen</span><span class="sxs-lookup"><span data-stu-id="33a11-108">Headings</span></span>

<span data-ttu-id="33a11-109">Als u een kop wilt maken, gebruikt u een hash (#), als volgt:</span><span class="sxs-lookup"><span data-stu-id="33a11-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="33a11-110">Headers moeten in ATX-stijl worden gemaakt, dat wil zeggen dat aan het begin van de regel 1 tot 6 hekjes (#) moeten staan om een header aan te duiden overeenkomstig de HTML-headerniveaus H1 tot H6.</span><span class="sxs-lookup"><span data-stu-id="33a11-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="33a11-111">Hierboven vindt u voorbeelden van headers van het eerste tot vierde niveau.</span><span class="sxs-lookup"><span data-stu-id="33a11-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="33a11-112">Uw onderwerp **mag** maar één header van het eerste niveau (H1) bevatten. Deze wordt op de pagina weergegeven als de titel.</span><span class="sxs-lookup"><span data-stu-id="33a11-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="33a11-113">Als uw header met een `#` eindigt, moet u aan het eind nog een `#` toevoegen zodat de titel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33a11-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="33a11-114">Bijvoorbeeld `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="33a11-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="33a11-115">Met de headers op het tweede niveau wordt de inhoudsopgave op de pagina gegenereerd die wordt weergegeven in de sectie 'In dit artikel' onder de titel op de pagina.</span><span class="sxs-lookup"><span data-stu-id="33a11-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="33a11-116">Vetgedrukte en cursieve tekst</span><span class="sxs-lookup"><span data-stu-id="33a11-116">Bold and italic text</span></span>

<span data-ttu-id="33a11-117">Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="33a11-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="33a11-118">Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="33a11-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="33a11-119">Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:</span><span class="sxs-lookup"><span data-stu-id="33a11-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="33a11-120">Blokcitaten</span><span class="sxs-lookup"><span data-stu-id="33a11-120">Blockquotes</span></span>

<span data-ttu-id="33a11-121">Blokcitaten worden gemaakt met het teken `>`:</span><span class="sxs-lookup"><span data-stu-id="33a11-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="33a11-122">Het voorbeeld hierboven wordt als volgt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="33a11-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="33a11-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="33a11-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="33a11-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="33a11-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="33a11-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="33a11-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="33a11-126">Lijsten</span><span class="sxs-lookup"><span data-stu-id="33a11-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="33a11-127">Ongeordende lijst</span><span class="sxs-lookup"><span data-stu-id="33a11-127">Unordered list</span></span>

<span data-ttu-id="33a11-128">Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33a11-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="33a11-129">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="33a11-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="33a11-130">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="33a11-130">will be rendered as:</span></span>

- <span data-ttu-id="33a11-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="33a11-131">List item 1</span></span>
- <span data-ttu-id="33a11-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="33a11-132">List item 2</span></span>
- <span data-ttu-id="33a11-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="33a11-133">List item 3</span></span>

<span data-ttu-id="33a11-134">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="33a11-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="33a11-135">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="33a11-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="33a11-136">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="33a11-136">will be rendered as:</span></span>

- <span data-ttu-id="33a11-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="33a11-137">List item 1</span></span>
  - <span data-ttu-id="33a11-138">List item A</span><span class="sxs-lookup"><span data-stu-id="33a11-138">List item A</span></span>
  - <span data-ttu-id="33a11-139">List item B</span><span class="sxs-lookup"><span data-stu-id="33a11-139">List item B</span></span>
- <span data-ttu-id="33a11-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="33a11-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="33a11-141">Geordende lijst</span><span class="sxs-lookup"><span data-stu-id="33a11-141">Ordered list</span></span>

<span data-ttu-id="33a11-142">Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers.</span><span class="sxs-lookup"><span data-stu-id="33a11-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="33a11-143">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="33a11-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="33a11-144">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="33a11-144">will be rendered as:</span></span>

1. <span data-ttu-id="33a11-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-145">First instruction</span></span>
2. <span data-ttu-id="33a11-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-146">Second instruction</span></span>
3. <span data-ttu-id="33a11-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-147">Third instruction</span></span>

<span data-ttu-id="33a11-148">Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen.</span><span class="sxs-lookup"><span data-stu-id="33a11-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="33a11-149">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="33a11-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="33a11-150">weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="33a11-150">will be rendered as:</span></span>

1. <span data-ttu-id="33a11-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-151">First instruction</span></span>
   1. <span data-ttu-id="33a11-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-152">Sub-instruction</span></span>
   2. <span data-ttu-id="33a11-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-153">Sub-instruction</span></span>
2. <span data-ttu-id="33a11-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="33a11-154">Second instruction</span></span>

<span data-ttu-id="33a11-155">Merk op dat we '1.' gebruiken</span><span class="sxs-lookup"><span data-stu-id="33a11-155">Note that we use '1.'</span></span> <span data-ttu-id="33a11-156">voor alle vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="33a11-156">for all entries.</span></span> <span data-ttu-id="33a11-157">Hierdoor is het eenvoudiger om later verschillen te beoordelen als er in latere updates nieuwe stappen worden toegevoegd of bestaande stappen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="33a11-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="33a11-158">Tables</span><span class="sxs-lookup"><span data-stu-id="33a11-158">Tables</span></span>

<span data-ttu-id="33a11-159">Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM.</span><span class="sxs-lookup"><span data-stu-id="33a11-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="33a11-160">Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-).</span><span class="sxs-lookup"><span data-stu-id="33a11-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="33a11-161">Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar.</span><span class="sxs-lookup"><span data-stu-id="33a11-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="33a11-162">Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33a11-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="33a11-163">Zo wordt de volgende Markdown:</span><span class="sxs-lookup"><span data-stu-id="33a11-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="33a11-164">Wordt weergegeven als:</span><span class="sxs-lookup"><span data-stu-id="33a11-164">Will be rendered as:</span></span>

| <span data-ttu-id="33a11-165">Fun</span><span class="sxs-lookup"><span data-stu-id="33a11-165">Fun</span></span>                  | <span data-ttu-id="33a11-166">With</span><span class="sxs-lookup"><span data-stu-id="33a11-166">With</span></span>                 | <span data-ttu-id="33a11-167">Tables</span><span class="sxs-lookup"><span data-stu-id="33a11-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="33a11-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="33a11-168">left-aligned column</span></span>  | <span data-ttu-id="33a11-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="33a11-169">right-aligned column</span></span> | <span data-ttu-id="33a11-170">centered column</span><span class="sxs-lookup"><span data-stu-id="33a11-170">centered column</span></span> |
| <span data-ttu-id="33a11-171">$100</span><span class="sxs-lookup"><span data-stu-id="33a11-171">$100</span></span>                 | <span data-ttu-id="33a11-172">$100</span><span class="sxs-lookup"><span data-stu-id="33a11-172">$100</span></span>                 | <span data-ttu-id="33a11-173">$100</span><span class="sxs-lookup"><span data-stu-id="33a11-173">$100</span></span>            |
| <span data-ttu-id="33a11-174">$10</span><span class="sxs-lookup"><span data-stu-id="33a11-174">$10</span></span>                  | <span data-ttu-id="33a11-175">$10</span><span class="sxs-lookup"><span data-stu-id="33a11-175">$10</span></span>                  | <span data-ttu-id="33a11-176">$10</span><span class="sxs-lookup"><span data-stu-id="33a11-176">$10</span></span>             |
| <span data-ttu-id="33a11-177">$1</span><span class="sxs-lookup"><span data-stu-id="33a11-177">$1</span></span>                   | <span data-ttu-id="33a11-178">$1</span><span class="sxs-lookup"><span data-stu-id="33a11-178">$1</span></span>                   | <span data-ttu-id="33a11-179">$1</span><span class="sxs-lookup"><span data-stu-id="33a11-179">$1</span></span>              |

<span data-ttu-id="33a11-180">Ga voor meer informatie over het maken van tabellen naar:</span><span class="sxs-lookup"><span data-stu-id="33a11-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="33a11-181">[Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="33a11-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="33a11-182">De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="33a11-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="33a11-183">[Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="33a11-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="33a11-184">[Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="33a11-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="33a11-185">[HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="33a11-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="33a11-186">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="33a11-186">Links</span></span>

<span data-ttu-id="33a11-187">De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="33a11-188">Ga voor meer informatie over koppelen naar:</span><span class="sxs-lookup"><span data-stu-id="33a11-188">For more information on linking, see:</span></span>

- <span data-ttu-id="33a11-189">De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.</span><span class="sxs-lookup"><span data-stu-id="33a11-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="33a11-190">De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over de aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.</span><span class="sxs-lookup"><span data-stu-id="33a11-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="33a11-191">Codefragmenten</span><span class="sxs-lookup"><span data-stu-id="33a11-191">Code snippets</span></span>

<span data-ttu-id="33a11-192">Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen.</span><span class="sxs-lookup"><span data-stu-id="33a11-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="33a11-193">Zie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="33a11-193">For details, see:</span></span>

- [<span data-ttu-id="33a11-194">Eigen systeemondersteuning van Markdown voor codeblokken</span><span class="sxs-lookup"><span data-stu-id="33a11-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="33a11-195">GFM-ondersteuning voor codeomheining en syntaxismarkering</span><span class="sxs-lookup"><span data-stu-id="33a11-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="33a11-196">Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="33a11-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="33a11-197">De algemene opmaak voor omheinde codeblokken is:</span><span class="sxs-lookup"><span data-stu-id="33a11-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="33a11-198">Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="33a11-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="33a11-199">Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:</span><span class="sxs-lookup"><span data-stu-id="33a11-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="33a11-200">Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.</span><span class="sxs-lookup"><span data-stu-id="33a11-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="33a11-201">Naam</span><span class="sxs-lookup"><span data-stu-id="33a11-201">Name</span></span>|<span data-ttu-id="33a11-202">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="33a11-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="33a11-203">.NET Console</span><span class="sxs-lookup"><span data-stu-id="33a11-203">.NET Console</span></span>|<span data-ttu-id="33a11-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="33a11-204">dotnetcli</span></span>|
|<span data-ttu-id="33a11-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="33a11-205">ASP.NET (C#)</span></span>|<span data-ttu-id="33a11-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="33a11-206">aspx-csharp</span></span>|
|<span data-ttu-id="33a11-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="33a11-207">ASP.NET (VB)</span></span>|<span data-ttu-id="33a11-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="33a11-208">aspx-vb</span></span>|
|<span data-ttu-id="33a11-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="33a11-209">AzCopy</span></span>|<span data-ttu-id="33a11-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="33a11-210">azcopy</span></span>|
|<span data-ttu-id="33a11-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="33a11-211">Azure CLI</span></span>|<span data-ttu-id="33a11-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="33a11-212">azurecli</span></span>|
|<span data-ttu-id="33a11-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33a11-213">Azure PowerShell</span></span>|<span data-ttu-id="33a11-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="33a11-214">azurepowershell</span></span>|
|<span data-ttu-id="33a11-215">Bash</span><span class="sxs-lookup"><span data-stu-id="33a11-215">Bash</span></span>|<span data-ttu-id="33a11-216">bash</span><span class="sxs-lookup"><span data-stu-id="33a11-216">bash</span></span>|
|<span data-ttu-id="33a11-217">C++</span><span class="sxs-lookup"><span data-stu-id="33a11-217">C++</span></span>|<span data-ttu-id="33a11-218">cpp</span><span class="sxs-lookup"><span data-stu-id="33a11-218">cpp</span></span>|
|<span data-ttu-id="33a11-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="33a11-219">C++/CX</span></span>|<span data-ttu-id="33a11-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="33a11-220">cppcx</span></span>|
|<span data-ttu-id="33a11-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="33a11-221">C++/WinRT</span></span>|<span data-ttu-id="33a11-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="33a11-222">cppwinrt</span></span>|
|<span data-ttu-id="33a11-223">C#</span><span class="sxs-lookup"><span data-stu-id="33a11-223">C#</span></span>|<span data-ttu-id="33a11-224">csharp</span><span class="sxs-lookup"><span data-stu-id="33a11-224">csharp</span></span>|
|<span data-ttu-id="33a11-225">C# in browser</span><span class="sxs-lookup"><span data-stu-id="33a11-225">C# in browser</span></span>|<span data-ttu-id="33a11-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="33a11-226">csharp-interactive</span></span>|
|<span data-ttu-id="33a11-227">Console</span><span class="sxs-lookup"><span data-stu-id="33a11-227">Console</span></span>|<span data-ttu-id="33a11-228">console</span><span class="sxs-lookup"><span data-stu-id="33a11-228">console</span></span>|
|<span data-ttu-id="33a11-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="33a11-229">CSHTML</span></span>|<span data-ttu-id="33a11-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="33a11-230">cshtml</span></span>|
|<span data-ttu-id="33a11-231">DAX</span><span class="sxs-lookup"><span data-stu-id="33a11-231">DAX</span></span>|<span data-ttu-id="33a11-232">dax</span><span class="sxs-lookup"><span data-stu-id="33a11-232">dax</span></span>|
|<span data-ttu-id="33a11-233">Docker</span><span class="sxs-lookup"><span data-stu-id="33a11-233">Docker</span></span>|<span data-ttu-id="33a11-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="33a11-234">dockerfile</span></span>|
|<span data-ttu-id="33a11-235">F#</span><span class="sxs-lookup"><span data-stu-id="33a11-235">F#</span></span>|<span data-ttu-id="33a11-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="33a11-236">fsharp</span></span>|
|<span data-ttu-id="33a11-237">Go</span><span class="sxs-lookup"><span data-stu-id="33a11-237">Go</span></span>|<span data-ttu-id="33a11-238">go</span><span class="sxs-lookup"><span data-stu-id="33a11-238">go</span></span>|
|<span data-ttu-id="33a11-239">HTML</span><span class="sxs-lookup"><span data-stu-id="33a11-239">HTML</span></span>|<span data-ttu-id="33a11-240">html</span><span class="sxs-lookup"><span data-stu-id="33a11-240">html</span></span>|
|<span data-ttu-id="33a11-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="33a11-241">HTTP</span></span>|<span data-ttu-id="33a11-242">http</span><span class="sxs-lookup"><span data-stu-id="33a11-242">http</span></span>|
|<span data-ttu-id="33a11-243">Java</span><span class="sxs-lookup"><span data-stu-id="33a11-243">Java</span></span>|<span data-ttu-id="33a11-244">java</span><span class="sxs-lookup"><span data-stu-id="33a11-244">java</span></span>|
|<span data-ttu-id="33a11-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="33a11-245">JavaScript</span></span>|<span data-ttu-id="33a11-246">javascript</span><span class="sxs-lookup"><span data-stu-id="33a11-246">javascript</span></span>|
|<span data-ttu-id="33a11-247">JSON</span><span class="sxs-lookup"><span data-stu-id="33a11-247">JSON</span></span>|<span data-ttu-id="33a11-248">json</span><span class="sxs-lookup"><span data-stu-id="33a11-248">json</span></span>|
|<span data-ttu-id="33a11-249">Kusto-querytaal</span><span class="sxs-lookup"><span data-stu-id="33a11-249">Kusto Query Language</span></span>|<span data-ttu-id="33a11-250">kusto</span><span class="sxs-lookup"><span data-stu-id="33a11-250">kusto</span></span>|
|<span data-ttu-id="33a11-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-251">Markdown</span></span>|<span data-ttu-id="33a11-252">md</span><span class="sxs-lookup"><span data-stu-id="33a11-252">md</span></span>|
|<span data-ttu-id="33a11-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="33a11-253">Objective-C</span></span>|<span data-ttu-id="33a11-254">objc</span><span class="sxs-lookup"><span data-stu-id="33a11-254">objc</span></span>|
|<span data-ttu-id="33a11-255">OData</span><span class="sxs-lookup"><span data-stu-id="33a11-255">OData</span></span>|<span data-ttu-id="33a11-256">odata</span><span class="sxs-lookup"><span data-stu-id="33a11-256">odata</span></span>|
|<span data-ttu-id="33a11-257">PHP</span><span class="sxs-lookup"><span data-stu-id="33a11-257">PHP</span></span>|<span data-ttu-id="33a11-258">php</span><span class="sxs-lookup"><span data-stu-id="33a11-258">php</span></span>|
|<span data-ttu-id="33a11-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="33a11-259">protobuf</span></span>|<span data-ttu-id="33a11-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="33a11-260">protobuf</span></span>|
|<span data-ttu-id="33a11-261">PowerApps (decimale punt als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="33a11-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="33a11-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="33a11-262">powerapps-dot</span></span>|
|<span data-ttu-id="33a11-263">PowerApps (decimale komma als scheidingsteken)</span><span class="sxs-lookup"><span data-stu-id="33a11-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="33a11-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="33a11-264">powerapps-comma</span></span>|
|<span data-ttu-id="33a11-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="33a11-265">PowerShell</span></span>|<span data-ttu-id="33a11-266">powershell</span><span class="sxs-lookup"><span data-stu-id="33a11-266">powershell</span></span>|
|<span data-ttu-id="33a11-267">Python</span><span class="sxs-lookup"><span data-stu-id="33a11-267">Python</span></span>|<span data-ttu-id="33a11-268">python</span><span class="sxs-lookup"><span data-stu-id="33a11-268">python</span></span>|
|<span data-ttu-id="33a11-269">Q#</span><span class="sxs-lookup"><span data-stu-id="33a11-269">Q#</span></span>|<span data-ttu-id="33a11-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="33a11-270">qsharp</span></span>|
|<span data-ttu-id="33a11-271">R</span><span class="sxs-lookup"><span data-stu-id="33a11-271">R</span></span>|<span data-ttu-id="33a11-272">r</span><span class="sxs-lookup"><span data-stu-id="33a11-272">r</span></span>|
|<span data-ttu-id="33a11-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="33a11-273">Ruby</span></span>|<span data-ttu-id="33a11-274">ruby</span><span class="sxs-lookup"><span data-stu-id="33a11-274">ruby</span></span>|
|<span data-ttu-id="33a11-275">SQL</span><span class="sxs-lookup"><span data-stu-id="33a11-275">SQL</span></span>|<span data-ttu-id="33a11-276">sql</span><span class="sxs-lookup"><span data-stu-id="33a11-276">sql</span></span>|
|<span data-ttu-id="33a11-277">Swift</span><span class="sxs-lookup"><span data-stu-id="33a11-277">Swift</span></span>|<span data-ttu-id="33a11-278">swift</span><span class="sxs-lookup"><span data-stu-id="33a11-278">swift</span></span>|
|<span data-ttu-id="33a11-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="33a11-279">TypeScript</span></span>|<span data-ttu-id="33a11-280">typescript</span><span class="sxs-lookup"><span data-stu-id="33a11-280">typescript</span></span>|
|<span data-ttu-id="33a11-281">VB</span><span class="sxs-lookup"><span data-stu-id="33a11-281">VB</span></span>|<span data-ttu-id="33a11-282">vb</span><span class="sxs-lookup"><span data-stu-id="33a11-282">vb</span></span>|
|<span data-ttu-id="33a11-283">XAML</span><span class="sxs-lookup"><span data-stu-id="33a11-283">XAML</span></span>|<span data-ttu-id="33a11-284">xaml</span><span class="sxs-lookup"><span data-stu-id="33a11-284">xaml</span></span>|
|<span data-ttu-id="33a11-285">XML</span><span class="sxs-lookup"><span data-stu-id="33a11-285">XML</span></span>|<span data-ttu-id="33a11-286">xml</span><span class="sxs-lookup"><span data-stu-id="33a11-286">xml</span></span>|

<span data-ttu-id="33a11-287">De naam `csharp-interactive` geeft de taal C# aan en de mogelijkheid om de voorbeelden uit te voeren vanuit de browser.</span><span class="sxs-lookup"><span data-stu-id="33a11-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="33a11-288">Deze codefragmenten worden gecompileerd en uitgevoerd in een Docker-container, en de resultaten van het uitvoeren van het programma worden weergegeven in het browservenster van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="33a11-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="33a11-289">Voorbeeld: C\#</span><span class="sxs-lookup"><span data-stu-id="33a11-289">Example: C\#</span></span>

<span data-ttu-id="33a11-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="33a11-290">__Markdown__</span></span>

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

<span data-ttu-id="33a11-291">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="33a11-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="33a11-292">Voorbeeld: SQL</span><span class="sxs-lookup"><span data-stu-id="33a11-292">Example: SQL</span></span>

<span data-ttu-id="33a11-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="33a11-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="33a11-294">__Weergave__</span><span class="sxs-lookup"><span data-stu-id="33a11-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="33a11-295">Aangepaste Docs-extensies voor Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="33a11-296">Met Docs.Microsoft.com wordt een Markdig Parser for Markdown geïmplementeerd, die zeer compatibel is met GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="33a11-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="33a11-297">Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="33a11-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="33a11-298">Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding.</span><span class="sxs-lookup"><span data-stu-id="33a11-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="33a11-299">(Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)</span><span class="sxs-lookup"><span data-stu-id="33a11-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="33a11-300">GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen.</span><span class="sxs-lookup"><span data-stu-id="33a11-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="33a11-301">Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:</span><span class="sxs-lookup"><span data-stu-id="33a11-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="33a11-302">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="33a11-302">Note blocks</span></span>
- <span data-ttu-id="33a11-303">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="33a11-303">Include files</span></span>
- <span data-ttu-id="33a11-304">Selectors</span><span class="sxs-lookup"><span data-stu-id="33a11-304">Selectors</span></span>
- <span data-ttu-id="33a11-305">Ingebedde video's</span><span class="sxs-lookup"><span data-stu-id="33a11-305">Embedded videos</span></span>
- <span data-ttu-id="33a11-306">Codefragmenten/voorbeelden</span><span class="sxs-lookup"><span data-stu-id="33a11-306">Code snippets/samples</span></span>

<span data-ttu-id="33a11-307">Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.</span><span class="sxs-lookup"><span data-stu-id="33a11-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="33a11-308">Notitieblokken</span><span class="sxs-lookup"><span data-stu-id="33a11-308">Note blocks</span></span>

<span data-ttu-id="33a11-309">U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:</span><span class="sxs-lookup"><span data-stu-id="33a11-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="33a11-310">OPMERKING</span><span class="sxs-lookup"><span data-stu-id="33a11-310">NOTE</span></span>
- <span data-ttu-id="33a11-311">WAARSCHUWING</span><span class="sxs-lookup"><span data-stu-id="33a11-311">WARNING</span></span>
- <span data-ttu-id="33a11-312">TIP</span><span class="sxs-lookup"><span data-stu-id="33a11-312">TIP</span></span>
- <span data-ttu-id="33a11-313">BELANGRIJK</span><span class="sxs-lookup"><span data-stu-id="33a11-313">IMPORTANT</span></span>

<span data-ttu-id="33a11-314">Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren.</span><span class="sxs-lookup"><span data-stu-id="33a11-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="33a11-315">Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.</span><span class="sxs-lookup"><span data-stu-id="33a11-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="33a11-316">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="33a11-316">Examples:</span></span>

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

<span data-ttu-id="33a11-317">Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="33a11-317">These alerts look like this on docs.microsoft.com:</span></span>

![laat zien hoe de waarschuwingen in het vorige voorbeeld eruit zien op de gepubliceerde Docs-pagina met verschillende pictogrammen en kleuren](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="33a11-319">Bestanden opnemen</span><span class="sxs-lookup"><span data-stu-id="33a11-319">Include files</span></span>

<span data-ttu-id="33a11-320">Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden.</span><span class="sxs-lookup"><span data-stu-id="33a11-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="33a11-321">Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="33a11-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="33a11-322">Er zijn drie soorten insluitingsverwijzingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="33a11-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="33a11-323">Inline: Een gewoon stuk tekst inline hergebruiken in een andere zin.</span><span class="sxs-lookup"><span data-stu-id="33a11-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="33a11-324">Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="33a11-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="33a11-325">Afbeelding: Op deze manier worden afbeeldingen standaard ingesloten in Docs.</span><span class="sxs-lookup"><span data-stu-id="33a11-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="33a11-326">Een inline- of blokinsluitingsbestand is niets meer of minder dan een eenvoudig Markdown-bestand (.md).</span><span class="sxs-lookup"><span data-stu-id="33a11-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="33a11-327">Deze kunnen elke geldige Markdown bevatten.</span><span class="sxs-lookup"><span data-stu-id="33a11-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="33a11-328">Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="33a11-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="33a11-329">Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="33a11-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="33a11-330">Dit zijn de vereisten en overwegingen voor insluitingsbestanden:</span><span class="sxs-lookup"><span data-stu-id="33a11-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="33a11-331">Gebruik een insluitingsbestand wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33a11-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="33a11-332">Gebruik een blokinsluitingsverwijzing voor aanzienlijke hoeveelheden inhoud: enkele alinea's, een gedeelde procedure of een gedeelde sectie.</span><span class="sxs-lookup"><span data-stu-id="33a11-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="33a11-333">Gebruik deze niet voor content die minder lang is dan een zin.</span><span class="sxs-lookup"><span data-stu-id="33a11-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="33a11-334">Insluitingsverwijzingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikel, omdat ze afhankelijk zijn van Markdig-extensies.</span><span class="sxs-lookup"><span data-stu-id="33a11-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="33a11-335">Ze worden pas weergegeven na publicatie.</span><span class="sxs-lookup"><span data-stu-id="33a11-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="33a11-336">Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar het insluitingsbestand wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="33a11-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="33a11-337">Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.</span><span class="sxs-lookup"><span data-stu-id="33a11-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="33a11-338">Voeg geen insluitingsverwijzingen in andere insluitingsbestanden in.</span><span class="sxs-lookup"><span data-stu-id="33a11-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="33a11-339">Dit wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="33a11-339">They are not supported.</span></span>
- <span data-ttu-id="33a11-340">Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="33a11-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="33a11-341">In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="33a11-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="33a11-342">Als het insluitingsbestand geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="33a11-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="33a11-343">Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="33a11-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="33a11-344">Gebruik een afzonderlijk bestand met een unieke naam voor elk insluitingsbestand en artikel.</span><span class="sxs-lookup"><span data-stu-id="33a11-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="33a11-345">Sla het mediabestand op in de mediamap die is gekoppeld aan het insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="33a11-346">Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="33a11-347">Insluitingsbestanden dienen als aanvulling op de inhoud in de rest van het artikel.</span><span class="sxs-lookup"><span data-stu-id="33a11-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="33a11-348">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="33a11-349">Selectors</span><span class="sxs-lookup"><span data-stu-id="33a11-349">Selectors</span></span>

<span data-ttu-id="33a11-350">Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of op verschillende platformen.</span><span class="sxs-lookup"><span data-stu-id="33a11-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="33a11-351">Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="33a11-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="33a11-352">Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.</span><span class="sxs-lookup"><span data-stu-id="33a11-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="33a11-353">Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="33a11-354">Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelen waarin dezelfde selector wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="33a11-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="33a11-355">Hier volgt een voorbeeld van een selector:</span><span class="sxs-lookup"><span data-stu-id="33a11-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="33a11-356">U kunt een praktijkvoorbeeld van selectors bekijken in [Azure Docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="33a11-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="33a11-357">Insluitingsverwijzingen van code</span><span class="sxs-lookup"><span data-stu-id="33a11-357">Code include references</span></span>

<span data-ttu-id="33a11-358">Met de Markdown-extensie voor het Docs-codefragment kunt u codevoorbeelden in uw artikelen insluiten en ze weergeven in een taalspecifieke syntaxiskleur.</span><span class="sxs-lookup"><span data-stu-id="33a11-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="33a11-359">U kunt code van de huidige opslagplaats of een andere opslagplaats insluiten.</span><span class="sxs-lookup"><span data-stu-id="33a11-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="33a11-360">In de onderstaande instructies vindt u een overzicht van het gebruik van de functie met het [docs.microsoft.com-ontwerppakket](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="33a11-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="33a11-361">In Visual Studio Code kunt u een voorbeeld van de codefragmenten bekijken door **Preview** te openen.</span><span class="sxs-lookup"><span data-stu-id="33a11-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="33a11-362">Markeren en interactiviteit zijn niet beschikbaar in de preview-versie.</span><span class="sxs-lookup"><span data-stu-id="33a11-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="33a11-363">De extensie biedt geen ondersteuning voor het integraal opnemen van code-inhoud. Dit moet worden uitgevoerd door middel van de standaard Markdown-conventie, die drie keer moet worden afgevinkt.</span><span class="sxs-lookup"><span data-stu-id="33a11-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="33a11-364">Code uit huidige opslagplaats</span><span class="sxs-lookup"><span data-stu-id="33a11-364">Code from current repository</span></span>

1. <span data-ttu-id="33a11-365">Klik in Visual Studio Code op **Alt + M** of **optie + M** en selecteer Fragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="33a11-366">Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="33a11-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="33a11-367">Als u lokaal wilt zoeken, selecteert u Volledige lokale zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="33a11-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="33a11-368">Voer een zoekterm in om het bestand te zoeken.</span><span class="sxs-lookup"><span data-stu-id="33a11-368">Enter a search term to find the file.</span></span> <span data-ttu-id="33a11-369">Wanneer u het bestand hebt gevonden, selecteert u het bestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="33a11-370">Selecteer vervolgens een optie om te bepalen welke regel(s) code er in het fragment moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="33a11-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="33a11-371">U kunt kiezen uit de volgende opties: **Id**, **Bereik** en **Geen**.</span><span class="sxs-lookup"><span data-stu-id="33a11-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="33a11-372">Geef, op basis van uw selectie uit stap 4, indien nodig een waarde op.</span><span class="sxs-lookup"><span data-stu-id="33a11-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="33a11-373">Volledig codebestand weergeven:</span><span class="sxs-lookup"><span data-stu-id="33a11-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="33a11-374">Deel van een codebestand weergeven door regels op te geven:</span><span class="sxs-lookup"><span data-stu-id="33a11-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="33a11-375">Deel van een codebestand weergeven op basis van de naam van een fragment:</span><span class="sxs-lookup"><span data-stu-id="33a11-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="33a11-376">Code uit een andere opslagplaats</span><span class="sxs-lookup"><span data-stu-id="33a11-376">Code from another repository</span></span>

1. <span data-ttu-id="33a11-377">Klik in Visual Studio Code op **Alt + M** of **optie + M** en selecteer Fragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="33a11-378">Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="33a11-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="33a11-379">Als u wilt zoeken in meerdere opslagplaatsen, selecteert u Verwijzing naar meerdere opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="33a11-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="33a11-380">U krijgt een selectie van opslagplaatsen die zich in *.openpublishing.publish.config.json* bevinden.</span><span class="sxs-lookup"><span data-stu-id="33a11-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="33a11-381">Selecteer een opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="33a11-381">Select a repository.</span></span>
3. <span data-ttu-id="33a11-382">Voer een zoekterm in om het bestand te zoeken.</span><span class="sxs-lookup"><span data-stu-id="33a11-382">Enter a search term to find the file.</span></span> <span data-ttu-id="33a11-383">Wanneer u het bestand hebt gevonden, selecteert u het bestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="33a11-384">Selecteer vervolgens een optie om te bepalen welke regel(s) code er in het fragment moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="33a11-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="33a11-385">U kunt kiezen uit de volgende opties: **Id**, **Bereik** en **Geen**.</span><span class="sxs-lookup"><span data-stu-id="33a11-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="33a11-386">Geef, op basis van uw selectie uit stap 5, indien nodig een waarde op.</span><span class="sxs-lookup"><span data-stu-id="33a11-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="33a11-387">Uw fragmentverwijzing ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="33a11-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="33a11-388">Pad naar het codebestand</span><span class="sxs-lookup"><span data-stu-id="33a11-388">Path to code file</span></span>

<span data-ttu-id="33a11-389">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="33a11-390">Dit voorbeeld komt uit de ASP.NET-docs-opslagplaats, uit het artikelbestand [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md).</span><span class="sxs-lookup"><span data-stu-id="33a11-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="33a11-391">Er wordt naar het codebestand verwezen met een relatief pad naar [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in dezelfde opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="33a11-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="33a11-392">Bepaalde regelnummers</span><span class="sxs-lookup"><span data-stu-id="33a11-392">Selected line numbers</span></span>

<span data-ttu-id="33a11-393">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="33a11-394">In dit voorbeeld worden alleen regels 2-24 en 26 van het code bestand *StudentController.cs* weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33a11-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="33a11-395">U kunt beter fragmenten gebruiken dan regelnummers. We leggen hieronder uit waarom.</span><span class="sxs-lookup"><span data-stu-id="33a11-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="33a11-396">Fragment met naam</span><span class="sxs-lookup"><span data-stu-id="33a11-396">Named snippet</span></span>

<span data-ttu-id="33a11-397">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="33a11-398">Gebruik alleen letters en onderstrepingstekens voor de naam.</span><span class="sxs-lookup"><span data-stu-id="33a11-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="33a11-399">In het voorbeeld wordt het gedeelte `snippet_Create` van het codebestand weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33a11-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="33a11-400">Het codebestand van dit voorbeeld heeft een C#-regio genaamd `snippet_Create`:</span><span class="sxs-lookup"><span data-stu-id="33a11-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="33a11-401">Wanneer mogelijk kunt u beter naar een gedeelte met naam verwijzen dan regelnummers op te geven.</span><span class="sxs-lookup"><span data-stu-id="33a11-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="33a11-402">Verwijzingen naar regelnummers zijn foutgevoelig omdat codebestanden altijd veranderen, waarbij ook de regelnummers kunnen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="33a11-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="33a11-403">U ontvangt niet per se een melding van zulke wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="33a11-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="33a11-404">In uw artikel zullen dan de verkeerde regels worden weergegeven zonder dat u weet dat er iets is veranderd.</span><span class="sxs-lookup"><span data-stu-id="33a11-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="33a11-405">Bepaalde regels markeren</span><span class="sxs-lookup"><span data-stu-id="33a11-405">Highlighting selected lines</span></span>

<span data-ttu-id="33a11-406">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="33a11-407">In het voorbeeld zijn regel 2 en 5 gemarkeerd, waarbij wordt geteld vanaf het begin van het weergegeven fragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="33a11-408">(Voor het markeren van regels wordt niet geteld vanaf het begin van het codebestand.) Met andere woorden: regel 3 en 6 van het codebestand zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="33a11-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="33a11-409">Interactieve codefragmenten</span><span class="sxs-lookup"><span data-stu-id="33a11-409">Interactive code snippets</span></span>

<span data-ttu-id="33a11-410">U kunt de interactieve modus inschakelen voor codefragmenten die met verwijzing zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="33a11-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="33a11-411">Hier volgen enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="33a11-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="33a11-412">Als u deze functie voor een bepaald codeblok wilt inschakelen, gebruikt u het kenmerk `interactive`.</span><span class="sxs-lookup"><span data-stu-id="33a11-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="33a11-413">De beschikbare kenmerkwaarden zijn:</span><span class="sxs-lookup"><span data-stu-id="33a11-413">The available attribute values are:</span></span>

- <span data-ttu-id="33a11-414">`cloudshell-powershell` - Hiermee schakelt u Azure PowerShell Cloud Shell in, zoals in het vorige voorbeeld</span><span class="sxs-lookup"><span data-stu-id="33a11-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="33a11-415">`cloudshell-bash` - Schakelt de Azure Cloud Shell in</span><span class="sxs-lookup"><span data-stu-id="33a11-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="33a11-416">`try-dotnet` - Hiermee schakelt u .NET proberen in</span><span class="sxs-lookup"><span data-stu-id="33a11-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="33a11-417">`try-dotnet-class` - Hiermee schakelt u .NET proberen met klasse-scaffolding in</span><span class="sxs-lookup"><span data-stu-id="33a11-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="33a11-418">`try-dotnet-method` - Hiermee schakelt u .NET proberen met methode-scaffolding in</span><span class="sxs-lookup"><span data-stu-id="33a11-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="33a11-419">Er zijn paren van `language` en `interactive` die compatibel zijn.</span><span class="sxs-lookup"><span data-stu-id="33a11-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="33a11-420">Als `interactive` bijvoorbeeld `try-dotnet` is, moet de taal `csharp` zijn.</span><span class="sxs-lookup"><span data-stu-id="33a11-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="33a11-421">Op dezelfde manier werkt `cloudshell-powershell` alleen met `powershell` en `cloudshell-bash` als `bash` de taal is.</span><span class="sxs-lookup"><span data-stu-id="33a11-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="33a11-422">Voor Azure Cloud Shell en PowerShell Cloud Shell kunnen gebruikers opdrachten uitvoeren voor enkel hun eigen Azure-account.</span><span class="sxs-lookup"><span data-stu-id="33a11-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="33a11-423">Met [.NET proberen](https://github.com/dotnet/try) is interactieve uitvoering van .NET-code (C#) in de browser mogelijk.</span><span class="sxs-lookup"><span data-stu-id="33a11-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="33a11-424">Voor .NET proberen zijn er drie opties voor interactiviteit: `try-dotnet`, `try-dotnet-class` en `try-dotnet-method`.</span><span class="sxs-lookup"><span data-stu-id="33a11-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="33a11-425">U kunt deze opties gebruiken zonder extra configuratie in het codefragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="33a11-426">De volgende naamruimten zijn momenteel standaard beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="33a11-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="33a11-427">System</span><span class="sxs-lookup"><span data-stu-id="33a11-427">System</span></span>
- <span data-ttu-id="33a11-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="33a11-428">System.Linq</span></span>
- <span data-ttu-id="33a11-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="33a11-429">System.Collections.Generic</span></span>
- <span data-ttu-id="33a11-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="33a11-430">System.Text</span></span>
- <span data-ttu-id="33a11-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="33a11-431">System.Globalization</span></span>
- <span data-ttu-id="33a11-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="33a11-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="33a11-433">Met de waarde van het `try-dotnet`-kenmerk kunnen gebruikers C#-code in de browser uitvoeren zonder de code te hoeven inpakken in aangepaste code.</span><span class="sxs-lookup"><span data-stu-id="33a11-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="33a11-434">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="33a11-435">Met behulp van de `try-dotnet-class`-waarde wordt klasse-scaffolding toegepast op de code die wordt doorgegeven aan het interactieve onderdeel.</span><span class="sxs-lookup"><span data-stu-id="33a11-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="33a11-436">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-436">Example:</span></span>

<span data-ttu-id="33a11-437">Codefragment waarop geen klasse-scaffolding is toegepast</span><span class="sxs-lookup"><span data-stu-id="33a11-437">Code Snippet without Class Scaffolding Applied</span></span>

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="33a11-438">Codefragment waarop wel klasse-scaffolding is toegepast</span><span class="sxs-lookup"><span data-stu-id="33a11-438">Code Snippet with Class Scaffolding Applied</span></span>

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="33a11-439">Met behulp van de `try-dotnet-method`-waarde wordt methode-scaffolding toegepast op de code die wordt doorgegeven aan het interactieve onderdeel.</span><span class="sxs-lookup"><span data-stu-id="33a11-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="33a11-440">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="33a11-440">Example:</span></span>

<span data-ttu-id="33a11-441">Codefragment waarop geen methode-scaffolding is toegepast</span><span class="sxs-lookup"><span data-stu-id="33a11-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="33a11-442">Codefragment waarop wel methode-scaffolding is toegepast</span><span class="sxs-lookup"><span data-stu-id="33a11-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="33a11-443">Naslaginformatie over fragmentsyntaxis</span><span class="sxs-lookup"><span data-stu-id="33a11-443">Snippet syntax reference</span></span>

<span data-ttu-id="33a11-444">U kunt naar codefragmenten die in uw opslagplaats zijn opgeslagen verwijzen door de opgegeven codetaal te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33a11-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="33a11-445">De inhoud van het opgegeven codepad wordt uitgebreid en in uw bestand opgenomen.</span><span class="sxs-lookup"><span data-stu-id="33a11-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="33a11-446">Er gelden geen beperkingen ten aanzien van de mappenstructuur van codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="33a11-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="33a11-447">U kunt de codefragmenten beheren als normale broncode.</span><span class="sxs-lookup"><span data-stu-id="33a11-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="33a11-448">Syntaxis:</span><span class="sxs-lookup"><span data-stu-id="33a11-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="33a11-449">Deze syntaxis is een Markdown-blokextensie.</span><span class="sxs-lookup"><span data-stu-id="33a11-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="33a11-450">Deze moet op zijn eigen regel worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="33a11-450">It must be used on its own line.</span></span>

- <span data-ttu-id="33a11-451">`<language>` (*optioneel*)</span><span class="sxs-lookup"><span data-stu-id="33a11-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="33a11-452">Taal van het codefragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-452">Language of the code snippet.</span></span> <span data-ttu-id="33a11-453">Zie de sectie [Ondersteunde talen](#supported-languages) verderop in dit artikel voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="33a11-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="33a11-454">`<path>`(*verplichte*)</span><span class="sxs-lookup"><span data-stu-id="33a11-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="33a11-455">Relatief pad naar het bestandssysteem dat het codefragmentbestand aangeeft waarnaar moet worden verwezen.</span><span class="sxs-lookup"><span data-stu-id="33a11-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="33a11-456">`<attribute>`en `<attribute-value>`(*optioneel*)</span><span class="sxs-lookup"><span data-stu-id="33a11-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="33a11-457">Worden samen gebruikt om op te geven hoe de code uit het bestand moet worden opgehaald:</span><span class="sxs-lookup"><span data-stu-id="33a11-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="33a11-458">`range`: `1,3-5` Een bereik met regels.</span><span class="sxs-lookup"><span data-stu-id="33a11-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="33a11-459">Dit voorbeeld bevat regels 1, 3, 4 en 5.</span><span class="sxs-lookup"><span data-stu-id="33a11-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="33a11-460">`id`: `snippet_Create` De id van het fragment dat moet worden ingevoegd vanuit het codebestand.</span><span class="sxs-lookup"><span data-stu-id="33a11-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="33a11-461">Deze waarde kan niet naast elkaar bestaan met een bereik.</span><span class="sxs-lookup"><span data-stu-id="33a11-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="33a11-462">`highlight`: `2-4,6` Het bereik en/of het aantal regels dat moet worden gemarkeerd in het gegenereerde codefragment.</span><span class="sxs-lookup"><span data-stu-id="33a11-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="33a11-463">De nummering is relatief ten opzichte van het codefragment zelf, niet het geïmporteerde bereik.</span><span class="sxs-lookup"><span data-stu-id="33a11-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="33a11-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` De waarde van de tekenreeks bepaalt welke soorten interactiviteit zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="33a11-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="33a11-465">Ondersteunde talen</span><span class="sxs-lookup"><span data-stu-id="33a11-465">Supported languages</span></span>

|<span data-ttu-id="33a11-466">Name</span><span class="sxs-lookup"><span data-stu-id="33a11-466">Name</span></span>|<span data-ttu-id="33a11-467">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="33a11-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="33a11-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="33a11-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="33a11-469">ASP.NET met C#</span><span class="sxs-lookup"><span data-stu-id="33a11-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="33a11-470">ASP.NET met VB</span><span class="sxs-lookup"><span data-stu-id="33a11-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="33a11-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="33a11-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="33a11-472">Azure CLI in browser</span><span class="sxs-lookup"><span data-stu-id="33a11-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="33a11-473">Azure PowerShell in browser</span><span class="sxs-lookup"><span data-stu-id="33a11-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="33a11-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="33a11-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="33a11-475">Bash</span><span class="sxs-lookup"><span data-stu-id="33a11-475">Bash</span></span>|`bash`|
|<span data-ttu-id="33a11-476">C++</span><span class="sxs-lookup"><span data-stu-id="33a11-476">C++</span></span>|`cpp`|
|<span data-ttu-id="33a11-477">C#</span><span class="sxs-lookup"><span data-stu-id="33a11-477">C#</span></span>|`csharp`|
|<span data-ttu-id="33a11-478">C# in browser</span><span class="sxs-lookup"><span data-stu-id="33a11-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="33a11-479">Console</span><span class="sxs-lookup"><span data-stu-id="33a11-479">Console</span></span>|`console`|
|<span data-ttu-id="33a11-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="33a11-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="33a11-481">DAX</span><span class="sxs-lookup"><span data-stu-id="33a11-481">DAX</span></span>|`dax`|
|<span data-ttu-id="33a11-482">Docker</span><span class="sxs-lookup"><span data-stu-id="33a11-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="33a11-483">F#</span><span class="sxs-lookup"><span data-stu-id="33a11-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="33a11-484">HTML</span><span class="sxs-lookup"><span data-stu-id="33a11-484">HTML</span></span>|`html`|
|<span data-ttu-id="33a11-485">Java</span><span class="sxs-lookup"><span data-stu-id="33a11-485">Java</span></span>|`java`|
|<span data-ttu-id="33a11-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="33a11-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="33a11-487">JSON</span><span class="sxs-lookup"><span data-stu-id="33a11-487">JSON</span></span>|`json`|
|<span data-ttu-id="33a11-488">Kusto-querytaal</span><span class="sxs-lookup"><span data-stu-id="33a11-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="33a11-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-489">Markdown</span></span>|`md`|
|<span data-ttu-id="33a11-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="33a11-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="33a11-491">PHP</span><span class="sxs-lookup"><span data-stu-id="33a11-491">PHP</span></span>|`php`|
|<span data-ttu-id="33a11-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="33a11-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="33a11-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="33a11-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="33a11-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="33a11-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="33a11-495">Python</span><span class="sxs-lookup"><span data-stu-id="33a11-495">Python</span></span>|`python`|
|<span data-ttu-id="33a11-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="33a11-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="33a11-497">SQL</span><span class="sxs-lookup"><span data-stu-id="33a11-497">SQL</span></span>|`sql`|
|<span data-ttu-id="33a11-498">Swift</span><span class="sxs-lookup"><span data-stu-id="33a11-498">Swift</span></span>|`swift`|
|<span data-ttu-id="33a11-499">VB</span><span class="sxs-lookup"><span data-stu-id="33a11-499">VB</span></span>|`vb`|
|<span data-ttu-id="33a11-500">XAML</span><span class="sxs-lookup"><span data-stu-id="33a11-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="33a11-501">XML</span><span class="sxs-lookup"><span data-stu-id="33a11-501">XML</span></span>|`xml`|
|<span data-ttu-id="33a11-502">YAML</span><span class="sxs-lookup"><span data-stu-id="33a11-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="33a11-503">Code-extensies</span><span class="sxs-lookup"><span data-stu-id="33a11-503">Code extensions</span></span>

|<span data-ttu-id="33a11-504">Name</span><span class="sxs-lookup"><span data-stu-id="33a11-504">Name</span></span>|<span data-ttu-id="33a11-505">Markdown-label</span><span class="sxs-lookup"><span data-stu-id="33a11-505">Markdown label</span></span>|<span data-ttu-id="33a11-506">Bestandsextensie</span><span class="sxs-lookup"><span data-stu-id="33a11-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="33a11-507">C#</span><span class="sxs-lookup"><span data-stu-id="33a11-507">C#</span></span>|<span data-ttu-id="33a11-508">csharp</span><span class="sxs-lookup"><span data-stu-id="33a11-508">csharp</span></span>|<span data-ttu-id="33a11-509">.cs, .csx</span><span class="sxs-lookup"><span data-stu-id="33a11-509">.cs, .csx</span></span>|
|<span data-ttu-id="33a11-510">C++</span><span class="sxs-lookup"><span data-stu-id="33a11-510">C++</span></span>|<span data-ttu-id="33a11-511">cpp</span><span class="sxs-lookup"><span data-stu-id="33a11-511">cpp</span></span>|<span data-ttu-id="33a11-512">.cpp, .h</span><span class="sxs-lookup"><span data-stu-id="33a11-512">.cpp, .h</span></span>|
|<span data-ttu-id="33a11-513">F#</span><span class="sxs-lookup"><span data-stu-id="33a11-513">F#</span></span>|<span data-ttu-id="33a11-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="33a11-514">fsharp</span></span>|<span data-ttu-id="33a11-515">.fs</span><span class="sxs-lookup"><span data-stu-id="33a11-515">.fs</span></span>|
|<span data-ttu-id="33a11-516">Java</span><span class="sxs-lookup"><span data-stu-id="33a11-516">Java</span></span>|<span data-ttu-id="33a11-517">java</span><span class="sxs-lookup"><span data-stu-id="33a11-517">java</span></span>|<span data-ttu-id="33a11-518">.java</span><span class="sxs-lookup"><span data-stu-id="33a11-518">.java</span></span>|
|<span data-ttu-id="33a11-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="33a11-519">JavaScript</span></span>|<span data-ttu-id="33a11-520">javascript</span><span class="sxs-lookup"><span data-stu-id="33a11-520">javascript</span></span>|<span data-ttu-id="33a11-521">.js</span><span class="sxs-lookup"><span data-stu-id="33a11-521">.js</span></span>|
|<span data-ttu-id="33a11-522">Python</span><span class="sxs-lookup"><span data-stu-id="33a11-522">Python</span></span>|<span data-ttu-id="33a11-523">python</span><span class="sxs-lookup"><span data-stu-id="33a11-523">python</span></span>|<span data-ttu-id="33a11-524">.py</span><span class="sxs-lookup"><span data-stu-id="33a11-524">.py</span></span>|
|<span data-ttu-id="33a11-525">SQL</span><span class="sxs-lookup"><span data-stu-id="33a11-525">SQL</span></span>|<span data-ttu-id="33a11-526">sql</span><span class="sxs-lookup"><span data-stu-id="33a11-526">sql</span></span>|<span data-ttu-id="33a11-527">.sql</span><span class="sxs-lookup"><span data-stu-id="33a11-527">.sql</span></span>|
|<span data-ttu-id="33a11-528">VB</span><span class="sxs-lookup"><span data-stu-id="33a11-528">VB</span></span>|<span data-ttu-id="33a11-529">vb</span><span class="sxs-lookup"><span data-stu-id="33a11-529">vb</span></span>|<span data-ttu-id="33a11-530">.vb</span><span class="sxs-lookup"><span data-stu-id="33a11-530">.vb</span></span>|
|<span data-ttu-id="33a11-531">XAML</span><span class="sxs-lookup"><span data-stu-id="33a11-531">XAML</span></span>|<span data-ttu-id="33a11-532">xaml</span><span class="sxs-lookup"><span data-stu-id="33a11-532">xaml</span></span>|<span data-ttu-id="33a11-533">.xmal</span><span class="sxs-lookup"><span data-stu-id="33a11-533">.xaml</span></span>|
|<span data-ttu-id="33a11-534">XML</span><span class="sxs-lookup"><span data-stu-id="33a11-534">XML</span></span>|<span data-ttu-id="33a11-535">xml</span><span class="sxs-lookup"><span data-stu-id="33a11-535">xml</span></span>|<span data-ttu-id="33a11-536">.xml</span><span class="sxs-lookup"><span data-stu-id="33a11-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="33a11-537">Gotcha's en probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33a11-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="33a11-538">Alternatieve tekst</span><span class="sxs-lookup"><span data-stu-id="33a11-538">Alt text</span></span>

<span data-ttu-id="33a11-539">Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33a11-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="33a11-540">In plaats van bijvoorbeeld dit te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="33a11-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="33a11-541">Typt u voor de onderstrepingstekens een escape-teken, zoals hier:</span><span class="sxs-lookup"><span data-stu-id="33a11-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="33a11-542">Apostroffen en aanhalingstekens</span><span class="sxs-lookup"><span data-stu-id="33a11-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="33a11-543">Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="33a11-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="33a11-544">Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens.</span><span class="sxs-lookup"><span data-stu-id="33a11-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="33a11-545">Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="33a11-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="33a11-546">Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:</span><span class="sxs-lookup"><span data-stu-id="33a11-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="33a11-547">Linker dubbel aanhalingsteken (openen): `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="33a11-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="33a11-548">Rechter dubbel aanhalingsteken (sluiten): `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="33a11-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="33a11-549">Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="33a11-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="33a11-550">Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="33a11-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="33a11-551">Punthaken</span><span class="sxs-lookup"><span data-stu-id="33a11-551">Angle brackets</span></span>

<span data-ttu-id="33a11-552">Het is gebruikelijk punthaken te gebruiken om een tijdelijke aanduiding aan te geven.</span><span class="sxs-lookup"><span data-stu-id="33a11-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="33a11-553">Als u dit in tekst doet (dus niet in code), moet u de punthaken coderen.</span><span class="sxs-lookup"><span data-stu-id="33a11-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="33a11-554">Anders zal Markdown deze aanzien voor HTML-code.</span><span class="sxs-lookup"><span data-stu-id="33a11-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="33a11-555">Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="33a11-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="33a11-556">Markdown-variant</span><span class="sxs-lookup"><span data-stu-id="33a11-556">Markdown flavor</span></span>

<span data-ttu-id="33a11-557">De back-end van docs.microsoft.com biedt ondersteuning voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parseerengine [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="33a11-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="33a11-558">Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="33a11-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="33a11-559">Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="33a11-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="33a11-560">Zie ook:</span><span class="sxs-lookup"><span data-stu-id="33a11-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="33a11-561">Markdown-resources</span><span class="sxs-lookup"><span data-stu-id="33a11-561">Markdown resources</span></span>

- [<span data-ttu-id="33a11-562">Inleiding tot Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-562">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="33a11-563">Referentiemateriaal voor Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="33a11-564">Basisbeginselen voor GitHubs Markdown</span><span class="sxs-lookup"><span data-stu-id="33a11-564">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="33a11-565">De Markdown-handleiding</span><span class="sxs-lookup"><span data-stu-id="33a11-565">The Markdown Guide</span></span>](https://www.markdownguide.org/)
