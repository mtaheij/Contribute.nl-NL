---
title: multiple-values
description: Uitleg en oplossing voor Docs-buildprobleem multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637317"
---
# <a name="multiple-values"></a><span data-ttu-id="b5798-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="b5798-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b5798-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="b5798-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="b5798-105">U hebt meer dan één waarde opgegeven voor een kenmerk waarvoor maar één waarde is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="b5798-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="b5798-106">Kenmerken die niet meer dan één waarde mogen hebben, moeten worden opgegeven in de YML-indeling (scalar) met één waarde.</span><span class="sxs-lookup"><span data-stu-id="b5798-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="b5798-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b5798-107">Resolution</span></span>

<span data-ttu-id="b5798-108">U ontvangt deze suggestie telkens wanneer u een matrix met meerdere waarden gebruikt voor een kenmerk met één waarde, of het nu gaat om meerdere waarden of om één waarde in de matrix.</span><span class="sxs-lookup"><span data-stu-id="b5798-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="b5798-109">YML ondersteunt de volgende matrixindelingen voor kenmerken met meerdere waarden, bijvoorbeeld `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="b5798-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="b5798-110">Deze indelingen zijn niet geldig voor kenmerken met één waarde, bijvoorbeeld `author`.</span><span class="sxs-lookup"><span data-stu-id="b5798-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="b5798-111">Als u meerdere waarden hebt opgegeven, beoordeelt u de specifieke waarden en bepaalt u welke correct is.</span><span class="sxs-lookup"><span data-stu-id="b5798-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="b5798-112">Verwijder de overige waarden en geef de enkele waarde op dezelfde regel als het kenmerk op, zonder haakjes. Dit doet u als volgt:</span><span class="sxs-lookup"><span data-stu-id="b5798-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="b5798-113">Als u een matrix met één waarde hebt, wijzigt u deze in de hierboven genoemde scalarindeling.</span><span class="sxs-lookup"><span data-stu-id="b5798-113">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]