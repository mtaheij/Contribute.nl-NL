---
title: Updates van metagegevens - Docs-Authoring Pack
description: Meer informatie over het bijwerken van metagegevens met het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336630"
---
# <a name="update-metadata"></a><span data-ttu-id="9e69c-103">Metagegevens bijwerken</span><span class="sxs-lookup"><span data-stu-id="9e69c-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="9e69c-104">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="9e69c-104">Summary</span></span>

<span data-ttu-id="9e69c-105">In een Markdown-bestand ( *\*.md*) zijn er twee contextuele menuopdrachten die specifiek zijn voor metagegevens.</span><span class="sxs-lookup"><span data-stu-id="9e69c-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="9e69c-106">Wanneer u met de rechtermuisknop op een willekeurige plaats in de teksteditor klikt, ziet u iets wat lijkt op de volgende menuopdrachten:</span><span class="sxs-lookup"><span data-stu-id="9e69c-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Contextmenu voor metagegevens bijwerken":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="9e69c-108">Metagegevenswaarde `ms.date` bijwerken</span><span class="sxs-lookup"><span data-stu-id="9e69c-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="9e69c-109">Als u de optie **Metagegevenswaarde `ms.date` bijwerken** selecteert, wordt de huidige waarde `ms.date` voor de Markdown-bestanden ingesteld op de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="9e69c-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="9e69c-110">Als het document geen `ms.date` metagegevensveld heeft, wordt er geen actie ondernomen.</span><span class="sxs-lookup"><span data-stu-id="9e69c-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="9e69c-111">Impliciete metagegevenswaarden bijwerken</span><span class="sxs-lookup"><span data-stu-id="9e69c-111">Update implicit metadata values</span></span>

<span data-ttu-id="9e69c-112">Als u de optie **Impliciete metagegevenswaarden bijwerken** selecteert, worden alle mogelijke metagegevenswaarden gevonden en vervangen die impliciet konden worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="9e69c-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="9e69c-113">Metagegevenswaarden worden impliciet opgegeven in het bestand *docfx.json*, onder het knooppunt `build/fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="9e69c-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="9e69c-114">Elk sleutelwaardepaar in het knooppunt `fileMetadata` staat voor de standaardinstellingen van metagegevens.</span><span class="sxs-lookup"><span data-stu-id="9e69c-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="9e69c-115">Met een Markdown-bestand in de map *top-level/sub-folder* waarmee de metagegevenswaarde `ms.author` wordt weggelaten, kan impliciet een standaardwaarde worden opgeven voor gebruik in het knooppunt `fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="9e69c-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="9e69c-116">In dit geval nemen alle Markdown-bestanden impliciet de metagegevenswaarde `ms.author: dapine` aan.</span><span class="sxs-lookup"><span data-stu-id="9e69c-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="9e69c-117">De functie wordt uitgevoerd op deze impliciete instellingen die te vinden zijn in het bestand *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="9e69c-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="9e69c-118">Als een Markdown-bestand metagegevens bevat met waarden die expliciet zijn ingesteld op iets anders dan de impliciete waarden, worden deze overschreven.</span><span class="sxs-lookup"><span data-stu-id="9e69c-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="9e69c-119">Kijk eens naar de volgende metagegevens van een Markdown-bestand, waarbij dit Markdown-bestand zich bevindt in **top-level/sub-folder/includes/example.md**:</span><span class="sxs-lookup"><span data-stu-id="9e69c-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="9e69c-120">Als de optie **Impliciete metagegevenswaarden bijwerken** op dit bestand werd uitgevoerd, met de veronderstelde *docfx.json*-inhoud van hiervoor, wordt de metagegevenswaarde bijgewerkt naar `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="9e69c-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="9e69c-121">In actie</span><span class="sxs-lookup"><span data-stu-id="9e69c-121">In action</span></span>

<span data-ttu-id="9e69c-122">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="9e69c-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="9e69c-123">[![Voorbeeld van metagegevens bijwerken](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9e69c-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
