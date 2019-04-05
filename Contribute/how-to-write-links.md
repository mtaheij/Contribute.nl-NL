---
title: Koppelingen in documentatie gebruiken
description: Dit artikel biedt ondersteuning voor het maken van koppelingen naar inhoud in docs.microsoft.com.
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 464c6b2ae8976252828d73390f9cbeea67f4e3ce
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637547"
---
# <a name="using-links-in-documentation"></a>Koppelingen in documentatie gebruiken
In dit artikel wordt beschreven hoe u hyperlinks gebruikt van pagina's die op docs.microsoft.com worden gehost. Koppelingen kunnen eenvoudig in Markdown worden toegevoegd, met een aantal afwijkende conventies. Koppelingen verwijzen gebruikers naar inhoud op dezelfde pagina, naar omliggende pagina's of naar externe websites en URL's.

De back-end van docs.microsoft.com gebruikt Open Publishing Services (OPS), dat ondersteuning biedt voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parseerengine [Markdig](https://github.com/lunet-io/markdig). Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt. Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.

> [!IMPORTANT]
> Alle koppelingen moeten zijn beveiligd (`https` vs. `http`) wanneer het doel dit ondersteunt (dit zou voor de grote meerderheid moeten gelden).

## <a name="link-text"></a>Tekst van koppeling

De woorden die u gebruikt in de tekst van de koppeling moeten duidelijk de bestemming van de koppeling aangeven. Gebruik dus normale beschrijvende tekst of de titel van de pagina die u wilt koppelen.

> [!IMPORTANT]
> Gebruik niet 'klik hier'. Het is nadelig voor de zoekmachineoptimalisatie en geeft geen goede beschrijving van het doelobject.

**Goed:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Fout:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Koppelingen van het ene artikel naar het andere

Als u een inlinekoppeling wilt maken van een technisch Docs-artikel naar een ander technisch Docs-artikel in dezelfde docset, gebruikt u de volgende syntaxis voor de koppeling:

- Een artikel in een map wordt gekoppeld aan een ander artikel in dezelfde map:

  `[link text](article-name.md)`

- Een artikel in een submap wordt gekoppeld aan een artikel in de hoofdmap:

  `[link text](../article-name.md)`

- Een artikel in de hoofdmap wordt gekoppeld aan een artikel in een submap:

  `[link text](./directory/article-name.md)`

- Een artikel in een submap wordt gekoppeld aan een artikel in een andere submap:

  `[link text](../directory/article-name.md)`

- Een artikel dat naar meerder docsets koppelt (zelfs in dezelfde opslagplaats):  `[link text](./directory/article-name)`

> [!IMPORTANT]
> Geen van de bovenstaande voorbeelden gebruikt de `~/` als onderdeel van de koppeling. Als u een koppeling maakt naar een pad in de hoofdmap van de opslagplaats, begint u met de `/`. Als u de `~/` opneemt, worden de koppelingen ongeldig als er wordt verwezen naar bronopslagplaatsen in GitHub. Als u het pad begint met `/`, wordt het correct omgezet.

## <a name="links-to-anchors"></a>Koppelingen naar ankers

U hoeft geen ankers te maken. Deze worden automatisch gegenereerd tijdens de publicatie van alle H2-koppen. U hoeft alleen maar koppelingen naar de H2-secties te maken.

- U maakt als volgt een koppeling naar een kop in hetzelfde artikel:

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- U maakt als volgt een koppeling naar een anker in een ander artikel in dezelfde submap:

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- U maakt als volgt een koppeling naar een anker in een andere servicesubmap:

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Koppelingen in Include-bestanden

Omdat Include-bestanden deel uitmaken van een andere map moet u een langer relatief pad gebruiken. Gebruik de volgende notatie om vanuit een Include-bestand een koppeling naar een artikel te maken:

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a>Koppelingen in selectors

Een selector is een navigatieonderdeel dat als vervolgkeuzelijst in een docs-artikel wordt weergegeven. Als de lezer een waarde in de vervolgkeuzelijst selecteert, wordt het geselecteerde artikel geopend in de browser. De selectorlijst bevat gewoonlijk koppelingen naar nauw verwante artikelen, bijvoorbeeld over hetzelfde onderwerp in meerdere programmeertalen, of naar een reeks nauw verwante artikelen. 

Als u met selectors werkt die zijn opgenomen in een Include-bestand, gebruikt u de volgende koppelingsstructuur:

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a>Koppelingen met verwijzingen

U kunt koppelingen met verwijzingen gebruiken zodat uw broninhoud gemakkelijker te lezen is. Bij koppelingen met verwijzingen wordt de syntaxis voor de inlinekoppeling vervangen door een eenvoudige syntaxis en kunnen de lange URL's naar het einde van het artikel worden verplaatst. Hier volgt het voorbeeld van [Daring Fireball](https://daringfireball.net/projects/markdown/):

Inlinetekst:

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Koppelingsverwijzingen aan het einde van het artikel:

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
Zorg ervoor dat u een spatie typt tussen de dubbele punt en de koppeling. Als u de spatie vergeet bij het maken van een koppeling naar andere technische artikelen, werkt de koppeling niet meer in het gepubliceerde artikel.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Een koppeling maken naar pagina's die geen deel uitmaken van de technische documentatie

Als u een koppeling wilt maken naar een pagina in een ander Microsoft-domein (zoals de pagina met prijzen, de SLA-pagina of naar iets dat geen documentatieartikel is), gebruikt u een absolute URL, maar laat u de landcode achterwege. Het doel hier is dat de koppelingen werken in GitHub en op de weergegeven site:

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a>Een koppeling maken naar sites van derden

Het beste kunt u gebruikers zo weinig mogelijk doorsturen naar andere sites. Soms is het echter nodig. Houd in die gevallen rekening met de volgende informatie wanneer u een koppeling maakt naar sites van derden:

- **Verantwoordelijkheden**: Maak een koppeling naar de inhoud van een derde partij als u informatie van deze partij wilt delen. Het is bijvoorbeeld niet de taak van Microsoft om mensen te vertellen hoe ze Android-ontwikkeltools moeten gebruiken. Dat is namelijk de taak van Google. We kunnen eventueel wel uitleggen hoe Android-ontwikkeltools moeten worden gebruikt *met* Azure, maar het is aan Google om te vertellen hoe hun eigen tools moeten worden gebruikt.
- **Aftekening door PM**: Geef aan dat Microsoft moet aftekenen op inhoud van derden. Door een koppeling te maken, zeggen we iets over ons vertrouwen in die inhoud en onze verplichtingen als mensen de instructies volgen
- **Controle van de nieuwheid**: Controleer of de inhoud van de derde partij nog steeds actueel, correct en relevant is en dat de koppeling niet is gewijzigd.
- **Offsite**: Zorg ervoor dat gebruikers er zich van bewust zijn dat ze naar een andere site gaan. Als dat niet blijkt uit de context, maakt u dat met een aparte zin duidelijk. Bijvoorbeeld: Bijvoorbeeld: "Tot de vereisten behoren ook de Android-ontwikkeltools die u kunt downloaden op de Android Studio-site."
- **Volgende stappen**: Het is prima om een koppeling te maken naar, bijvoorbeeld, een MVP-blog in de sectie Volgende stappen. Maar nogmaals, wijs de gebruikers erop dat ze de site verlaten.
- **Juridisch**: We kunnen een beroep doen op de juridisch bindende bepalingen in de sectie **Koppelingen naar de sites van derden** van de **Gebruiksvoorwaarden** onderaan elke pagina op ms.com.

## <a name="links-to-msdn-or-technet"></a>Een koppeling maken naar MSDN of TechNet

Wanneer u een koppeling wilt maken naar MSDN of TechNet, gebruikt u de volledige koppeling naar het onderwerp en verwijdert u de landcode voor de taal uit de koppeling.

## <a name="links-to-azure-powershell-reference-content"></a>Koppeling naar Azure PowerShell-referentiemateriaal

Het Azure PowerShell-referentiemateriaal heeft sinds november 2016 een aantal wijzigingen ondergaan. Gebruik de volgende richtlijnen om een koppeling naar deze inhoud te maken vanuit andere artikelen op docs.microsoft.com.

Structuur van de URL:

* Voor cmdlets:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Voor conceptonderwerpen:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

De sectie `<moniker-name>` is optioneel. Als deze sectie wordt weggelaten, wordt u doorgestuurd naar de nieuwste versie van de inhoud. De sectie `<service-name>` is een van de voorbeelden die in de volgende basis-URL's worden weergegeven:

- Azure PowerShell-inhoud (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Azure PowerShell-inhoud (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Azure Active Directory PowerShell-inhoud (AzureAD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

Wanneer u deze URL's gebruikt, wordt u omgeleid naar de nieuwste versie van de inhoud. Op die manier hoeft u geen versiemoniker op te geven. U voorkomt zo ook dat koppelingen naar conceptinhoud moeten worden bijgewerkt wanneer de versie verandert.

Als u een goede koppeling wilt maken, gaat u in uw browser naar de pagina waarnaar u wilt koppelen en kopieert u de URL.
Verwijder vervolgens `https://docs.microsoft.com` en de landinstellingsgegevens.

Wanneer u een koppeling vanuit een inhoudsopgave maakt, moet u de volledige URL zonder de landcode gebruiken.

Voorbeeld van Markdown:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
