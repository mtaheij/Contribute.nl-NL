---
title: Markdown-koppen
description: Beschrijft de vereisten voor Markdown-koppen.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084452"
---
# <a name="markdown-headings"></a><span data-ttu-id="57ea5-103">Markdown-koppen</span><span class="sxs-lookup"><span data-stu-id="57ea5-103">Markdown headings</span></span>

<span data-ttu-id="57ea5-104">De volgende validatievereisten zijn van toepassing op koppen in OPS Markdown-bestanden.</span><span class="sxs-lookup"><span data-stu-id="57ea5-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="57ea5-105">H1</span><span class="sxs-lookup"><span data-stu-id="57ea5-105">H1</span></span>

<span data-ttu-id="57ea5-106">`H1` verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="57ea5-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="57ea5-107">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="57ea5-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="57ea5-108">U maakt een H1 door een regel te beginnen met één hash (`#`), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="57ea5-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="57ea5-109">Dit is bijvoorbeeld de H1 van dit artikel:</span><span class="sxs-lookup"><span data-stu-id="57ea5-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="57ea5-110">De volgende regels zijn van toepassing op H1-koppen:</span><span class="sxs-lookup"><span data-stu-id="57ea5-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="57ea5-111">Het bestand moet een H1 bevatten.</span><span class="sxs-lookup"><span data-stu-id="57ea5-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="57ea5-112">Er kan slechts één H1 zijn.</span><span class="sxs-lookup"><span data-stu-id="57ea5-112">There can only be one H1.</span></span>
- <span data-ttu-id="57ea5-113">De H1 mag niet leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="57ea5-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="57ea5-114">Tussen de `#` en de inhoud van de H1 moet een spatie staan.</span><span class="sxs-lookup"><span data-stu-id="57ea5-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="57ea5-115">Een H1 zonder spatie wordt niet als een kop weergegeven op de gepubliceerde pagina.</span><span class="sxs-lookup"><span data-stu-id="57ea5-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="57ea5-116">De H1 moet de eerste inhoud in het bestand zijn na de YML-kop met metagegevens.</span><span class="sxs-lookup"><span data-stu-id="57ea5-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="57ea5-117">Inhoud, zoals tekst of afbeeldingen, tussen het einde van de YML-kop en de H1 is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="57ea5-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="57ea5-118">Het HTML-element voor koppen op het eerste niveau, `<h1>`, mag niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="57ea5-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="57ea5-119">Gebruik de Markdown-syntaxis (`# `).</span><span class="sxs-lookup"><span data-stu-id="57ea5-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="57ea5-120">De H1 mag niet langer dan 100 tekens zijn.</span><span class="sxs-lookup"><span data-stu-id="57ea5-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="57ea5-121">Dit is een stijlrichtlijn.</span><span class="sxs-lookup"><span data-stu-id="57ea5-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="57ea5-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="57ea5-122">H2 - H6</span></span>

<span data-ttu-id="57ea5-123">H2 (`## `) tot en met H6 (`###### `) zijn toegestaan in OPS.</span><span class="sxs-lookup"><span data-stu-id="57ea5-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="57ea5-124">Gebruik de Markdown-koppen, niet de HTML (`<h2>` - `<h6>`), om koppen te maken.</span><span class="sxs-lookup"><span data-stu-id="57ea5-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
