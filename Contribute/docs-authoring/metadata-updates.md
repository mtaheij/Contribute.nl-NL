---
title: Updates van metagegevens - Docs-Authoring Pack
description: Meer informatie over het bijwerken van metagegevens met het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336630"
---
# <a name="update-metadata"></a>Metagegevens bijwerken

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Overzicht

In een Markdown-bestand ( *\*.md*) zijn er twee contextuele menuopdrachten die specifiek zijn voor metagegevens. Wanneer u met de rechtermuisknop op een willekeurige plaats in de teksteditor klikt, ziet u iets wat lijkt op de volgende menuopdrachten:

:::image type="content" source="media/update-metadata-menu.png" alt-text="Contextmenu voor metagegevens bijwerken":::

## <a name="update-msdate-metadata-value"></a>Metagegevenswaarde `ms.date` bijwerken

Als u de optie **Metagegevenswaarde `ms.date` bijwerken** selecteert, wordt de huidige waarde `ms.date` voor de Markdown-bestanden ingesteld op de datum van vandaag. Als het document geen `ms.date` metagegevensveld heeft, wordt er geen actie ondernomen.

## <a name="update-implicit-metadata-values"></a>Impliciete metagegevenswaarden bijwerken

Als u de optie **Impliciete metagegevenswaarden bijwerken** selecteert, worden alle mogelijke metagegevenswaarden gevonden en vervangen die impliciet konden worden opgegeven. Metagegevenswaarden worden impliciet opgegeven in het bestand *docfx.json*, onder het knooppunt `build/fileMetadata`. Elk sleutelwaardepaar in het knooppunt `fileMetadata` staat voor de standaardinstellingen van metagegevens. Met een Markdown-bestand in de map *top-level/sub-folder* waarmee de metagegevenswaarde `ms.author` wordt weggelaten, kan impliciet een standaardwaarde worden opgeven voor gebruik in het knooppunt `fileMetadata`.

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

In dit geval nemen alle Markdown-bestanden impliciet de metagegevenswaarde `ms.author: dapine` aan. De functie wordt uitgevoerd op deze impliciete instellingen die te vinden zijn in het bestand *docfx.json*. Als een Markdown-bestand metagegevens bevat met waarden die expliciet zijn ingesteld op iets anders dan de impliciete waarden, worden deze overschreven.

Kijk eens naar de volgende metagegevens van een Markdown-bestand, waarbij dit Markdown-bestand zich bevindt in **top-level/sub-folder/includes/example.md**:

```markdown
---
ms.author: someone-else
---

# Content
```

Als de optie **Impliciete metagegevenswaarden bijwerken** op dit bestand werd uitgevoerd, met de veronderstelde *docfx.json*-inhoud van hiervoor, wordt de metagegevenswaarde bijgewerkt naar `ms.author: dapine`.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>In actie

Hieronder volgt een korte demonstratie van deze functie.

[![Voorbeeld van metagegevens bijwerken](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
