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
# <a name="updating-reference-articles"></a>Naslagartikelen bijwerken

Artikelen met naslaginformatie voor cmdlets hebben een specifieke structuur. Deze structuur wordt gedefinieerd door [PlatyPS][].
PlatyPS is het hulpprogramma dat we gebruiken om cmdlet-hulp te genereren voor PowerShell-modules. PlatyPS maakt het Markdown-basisbestand voor een cmdlet. Nadat de Markdown-bestanden zijn bewerkt, wordt PlatyPS gebruikt om de MAML-helpbestanden te maken die door de `Get-Help`-cmdlet worden gebruikt.

In PlatyPS is een in code vastgelegd schema voor cmdlet-naslaginformatie. Dit schema is in de code geschreven. In het document [platyPS.schema.md][] is deze structuur beschreven. Schendingen van het schema veroorzaken compilatiefouten die moeten worden opgelost voordat we uw bijdrage kunnen accepteren.

## <a name="general-guidelines"></a>Algemene richtlijnen

- Verwijder geen koptekststructuren. PlatyPS verwacht een specifieke reeks kopteksten.
- De kopteksten **Inputtype**  en **Outputtype**  moeten een type hebben. Gebruik de waarde 'Geen' als de cmdlet geen invoer heeft of een waarde retourneert.
- Afgebakende codeblokken zijn alleen toegestaan in de sectie [Voorbeelden](#format-for-examples).
- In elke alinea kunnen inline codereeksen worden gebruikt.

## <a name="formatting-about_-files"></a>About_-bestanden opmaken

`About_*`-bestanden worden nu verwerkt door [Pandoc][] in plaats van PlatyPS. `About_*`-bestanden zijn ingedeeld voor de beste compatibiliteit tussen alle versies van PowerShell en de hulpprogramma's voor publicatie.
Pas de indeling van `about_*`-bestanden niet aan zonder de persoon die verantwoordelijk is voor onderhoud van de opslagplaats te raadplegen.

Algemene richtlijnen voor het opmaken:

- Beperk regels tot 80 tekens
- Codeblokken, blokcitaten en tabellen zijn beperkt tot 76 tekens, omdat Pandoc deze met vier spaties inspringt tijdens de conversie
- Tabellen moeten binnen 76 tekens passen
  - Laat inhoud van cellen die over meerdere regels valt handmatig teruglopen
  - Gebruik op elke regel `|`-tekens voor openen en sluiten
  - Bekijk een werkend voorbeeld in [about_Comparison_Operators][about-example]
- Wanneer de speciale tekens `\`, `$`, `` ` `` en `<` van Pandoc worden gebruikt
  - Binnen een koptekst - moeten deze tekens worden voorafgegaan door een `\`-voorloopteken
  - Binnen een alinea - moeten deze tekens in codereeksen worden geplaatst. Bijvoorbeeld:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Indeling voor voorbeelden

In het PlatyPS-schema is de koptekst **VOORBEELDEN** een H2-kop en elk voorbeeld een H3-koptekst.

Het schema staat binnen een voorbeeld niet toe dat codeblokken worden gescheiden door alinea’s. Het geldige schema is:

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Geef elk voorbeeld een nummer en voeg een korte titel toe.

Bijvoorbeeld:

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