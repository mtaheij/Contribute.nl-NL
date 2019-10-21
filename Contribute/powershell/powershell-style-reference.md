---
title: Specifieke richtlijnen voor het schrijven van cmdlet-naslaginformatie
description: Dit artikel bevat specifieke regels voor het opmaken van PowerShell-codevoorbeelden. Dit is van toepassing op conceptuele artikelen met voorbeelden en op cmdlet-verwijzingen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290283"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="c007e-104">Naslagartikelen bijwerken</span><span class="sxs-lookup"><span data-stu-id="c007e-104">Updating reference articles</span></span>

<span data-ttu-id="c007e-105">Artikelen met naslaginformatie voor cmdlets hebben een specifieke structuur.</span><span class="sxs-lookup"><span data-stu-id="c007e-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="c007e-106">Deze structuur wordt gedefinieerd door [PlatyPS][].</span><span class="sxs-lookup"><span data-stu-id="c007e-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="c007e-107">PlatyPS is het hulpprogramma dat we gebruiken om cmdlet-hulp te genereren voor PowerShell-modules.</span><span class="sxs-lookup"><span data-stu-id="c007e-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="c007e-108">PlatyPS maakt het Markdown-basisbestand voor een cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c007e-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="c007e-109">Nadat de Markdown-bestanden zijn bewerkt, wordt PlatyPS gebruikt om de MAML-helpbestanden te maken die door de `Get-Help`-cmdlet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c007e-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="c007e-110">In PlatyPS is een in code vastgelegd schema voor cmdlet-naslaginformatie. Dit schema is in de code geschreven.</span><span class="sxs-lookup"><span data-stu-id="c007e-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="c007e-111">In het document [platyPS.schema.md][] is deze structuur beschreven.</span><span class="sxs-lookup"><span data-stu-id="c007e-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="c007e-112">Schendingen van het schema veroorzaken compilatiefouten die moeten worden opgelost voordat we uw bijdrage kunnen accepteren.</span><span class="sxs-lookup"><span data-stu-id="c007e-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="c007e-113">Algemene richtlijnen</span><span class="sxs-lookup"><span data-stu-id="c007e-113">General guidelines</span></span>

- <span data-ttu-id="c007e-114">Verwijder geen koptekststructuren.</span><span class="sxs-lookup"><span data-stu-id="c007e-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="c007e-115">PlatyPS verwacht een specifieke reeks kopteksten.</span><span class="sxs-lookup"><span data-stu-id="c007e-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="c007e-116">De kopteksten **Inputtype**  en **Outputtype**  moeten een type hebben.</span><span class="sxs-lookup"><span data-stu-id="c007e-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="c007e-117">Gebruik de waarde 'Geen' als de cmdlet geen invoer heeft of een waarde retourneert.</span><span class="sxs-lookup"><span data-stu-id="c007e-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="c007e-118">Afgebakende codeblokken zijn alleen toegestaan in de sectie [Voorbeelden](#format-for-examples).</span><span class="sxs-lookup"><span data-stu-id="c007e-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="c007e-119">In elke alinea kunnen inline codereeksen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c007e-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="c007e-120">About_-bestanden opmaken</span><span class="sxs-lookup"><span data-stu-id="c007e-120">Formatting About_ files</span></span>

<span data-ttu-id="c007e-121">`About_*`-bestanden worden nu verwerkt door [Pandoc][] in plaats van PlatyPS.</span><span class="sxs-lookup"><span data-stu-id="c007e-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="c007e-122">`About_*`-bestanden zijn ingedeeld voor de beste compatibiliteit tussen alle versies van PowerShell en de hulpprogramma's voor publicatie.</span><span class="sxs-lookup"><span data-stu-id="c007e-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="c007e-123">Pas de indeling van `about_*`-bestanden niet aan zonder de persoon die verantwoordelijk is voor onderhoud van de opslagplaats te raadplegen.</span><span class="sxs-lookup"><span data-stu-id="c007e-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="c007e-124">Algemene richtlijnen voor het opmaken:</span><span class="sxs-lookup"><span data-stu-id="c007e-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="c007e-125">Beperk regels tot 80 tekens</span><span class="sxs-lookup"><span data-stu-id="c007e-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="c007e-126">Codeblokken, blokcitaten en tabellen zijn beperkt tot 76 tekens, omdat Pandoc deze met vier spaties inspringt tijdens de conversie</span><span class="sxs-lookup"><span data-stu-id="c007e-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="c007e-127">Tabellen moeten binnen 76 tekens passen</span><span class="sxs-lookup"><span data-stu-id="c007e-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="c007e-128">Laat inhoud van cellen die over meerdere regels valt handmatig teruglopen</span><span class="sxs-lookup"><span data-stu-id="c007e-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="c007e-129">Gebruik op elke regel `|`-tekens voor openen en sluiten</span><span class="sxs-lookup"><span data-stu-id="c007e-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="c007e-130">Bekijk een werkend voorbeeld in [about_Comparison_Operators][about-example]</span><span class="sxs-lookup"><span data-stu-id="c007e-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="c007e-131">Wanneer de speciale tekens `\`, `$`, `` ` `` en `<` van Pandoc worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="c007e-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="c007e-132">Binnen een koptekst - moeten deze tekens worden voorafgegaan door een `\`-voorloopteken</span><span class="sxs-lookup"><span data-stu-id="c007e-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="c007e-133">Binnen een alinea - moeten deze tekens in codereeksen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="c007e-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="c007e-134">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="c007e-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="c007e-135">Indeling voor voorbeelden</span><span class="sxs-lookup"><span data-stu-id="c007e-135">Format for examples</span></span>

<span data-ttu-id="c007e-136">In het PlatyPS-schema is de koptekst **VOORBEELDEN** een H2-kop en elk voorbeeld een H3-koptekst.</span><span class="sxs-lookup"><span data-stu-id="c007e-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="c007e-137">Het schema staat binnen een voorbeeld niet toe dat codeblokken worden gescheiden door alinea’s.</span><span class="sxs-lookup"><span data-stu-id="c007e-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="c007e-138">Het geldige schema is:</span><span class="sxs-lookup"><span data-stu-id="c007e-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="c007e-139">Geef elk voorbeeld een nummer en voeg een korte titel toe.</span><span class="sxs-lookup"><span data-stu-id="c007e-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="c007e-140">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="c007e-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org