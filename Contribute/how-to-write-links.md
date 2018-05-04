---
title: Koppelingen in documentatie gebruiken
description: Dit artikel biedt ondersteuning voor het maken van koppelingen naar inhoud in docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a>Koppelingen in documentatie gebruiken
In dit artikel wordt beschreven hoe u hyperlinks gebruikt van pagina's die op docs.microsoft.com worden gehost. Koppelingen kunnen eenvoudig in Markdown worden toegevoegd, met een aantal afwijkende conventies. Koppelingen verwijzen gebruikers naar inhoud op dezelfde pagina, naar omliggende pagina's of naar externe websites en URL's.

De docs.microsoft.com site-back-end gebruikt Open Publishing Services (OPS); deze implementeren DocFX Flavored Markdown (DFM). DFM is uiterst compatibel met GitHub Flavored Markdown (GFM) en voegt extra functies toe aan de hand van Markdown-extensies.

> [!IMPORTANT]
> Alle koppelingen moeten zijn beveiligd (`https` vs. `http`) wanneer het doel dit ondersteunt (dit zou voor de grote meerderheid moeten gelden).

## <a name="link-text"></a>Tekst van koppeling

De woorden die u gebruikt in de tekst van de koppeling moeten duidelijk de bestemming van de koppeling aangeven. Gebruik dus normale beschrijvende tekst of de titel van de pagina die u wilt koppelen.

> [!IMPORTANT]
> Gebruik niet 'klik hier'. Het is nadelig voor de SEO en geeft geen goede beschrijving van het doelobject.

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

- Een artikel dat naar meerder docsets koppelt (zelfs in dezelfde opslagplaats): `[link text](./directory/article-name)`
  
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

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Koppelingen in selectors

Als u met selectors werkt die zijn opgenomen in een Include-bestand, zoals het Azure-documentatieteam doet, gebruikt u de volgende koppelingsstructuur:

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Text1 | Example1 )](../articles/folder/article-name1.md)
    - [(Text1 | Example2 )](../articles/folder/article-name2.md)
    - [(Text2 | Example3 )](../articles/folder/article-name3.md)
    - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Koppelingen met verwijzingen

U kunt koppelingen met verwijzingen gebruiken zodat uw broninhoud gemakkelijker te lezen is. Bij koppelingen met verwijzingen wordt de syntaxis voor de inlinekoppeling vervangen door een eenvoudige syntaxis en kunnen de lange URL's naar het einde van het artikel worden verplaatst. Hier volgt het voorbeeld van [Daring Fireball](https://daringfireball.net/projects/markdown/):

Inlinetekst:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Koppelingsverwijzingen aan het einde van het artikel:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Zorg ervoor dat u een spatie typt tussen de dubbele punt en de koppeling. Als u de spatie vergeet bij het maken van een koppeling naar andere technische artikelen, werkt de koppeling niet meer in het gepubliceerde artikel.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Een koppeling maken naar pagina's die geen deel uitmaken van de technische documentatie

Als u een koppeling wilt maken naar een pagina in een ander Microsoft-domein (zoals de pagina met prijzen, de SLA-pagina of naar iets dat geen documentatieartikel is), gebruikt u een absolute URL, maar laat u de landcode achterwege. Het doel hier is dat de koppelingen werken in GitHub en op de weergegeven site:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Een koppeling maken naar sites van derden

Het beste kunt u gebruikers zo weinig mogelijk doorsturen naar andere sites. Soms is het echter nodig. Houd in die gevallen rekening met de volgende informatie wanneer u een koppeling maakt naar sites van derden:

- **Aansprakelijkheid:** maak een koppeling naar de inhoud van derden als u informatie van deze derde partij wilt delen. Het is bijvoorbeeld niet de taak van Microsoft om mensen te vertellen hoe ze Android-ontwikkeltools moeten gebruiken. Dat is namelijk de taak van Google. We kunnen eventueel wel uitleggen hoe Android-ontwikkeltools moeten worden gebruikt *met* Azure, maar het is aan Google om te vertellen hoe hun eigen tools moeten worden gebruikt.
- **Aftekening door PM**: geef aan dat Microsoft verplicht moet aftekenen op inhoud van derden. Door een koppeling te maken, zeggen we iets over ons vertrouwen in die inhoud en onze verplichtingen als mensen de instructies volgen
- **Controle naar de actualiteit van de inhoud:** controleer of de inhoud van de derde partij nog steeds actueel, juist en relevant is en dat de koppeling niet is gewijzigd
- **Offsite:** zorg ervoor dat gebruikers er zich van bewust zijn dat ze naar een andere site gaan. Als dat niet blijkt uit de context, maakt u dat met een aparte zin duidelijk. Bijvoorbeeld: "Tot de vereisten behoren ook de Android-ontwikkeltools die u kunt downloaden op de Android Studio-site".
- **Volgende stappen:** het is prima om een koppeling te maken naar, bijvoorbeeld, een MVP-blog in de sectie Volgende stappen. Maar nogmaals, wijs de gebruikers erop dat ze de site verlaten.
- **Juridisch:** we kunnen een beroep doen op de juridisch bindende bepalingen die worden beschreven in de sectie **Koppelingen naar de sites van derden** van de **Gebruiksvoorwaarden**. Deze voorwaarden kunt u openen door op een pagina van ms.com naar de voettekst te gaan.

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

De sectie met de &lt;monikernaam&gt; is optioneel. Als deze sectie wordt weggelaten, wordt u doorgestuurd naar de nieuwste versie van de inhoud. De &lt;service-name&gt; is een van de voorbeelden die in de volgende basis-URL's wordt weergegeven:

- Azure PowerShell-inhoud (AzureRM): https://docs.microsoft.com/powershell/azure/
- Azure PowerShell-inhoud (ASM): https://docs.microsoft.com/powershell/azure/_servicemanagement_
- Azure Active Directory PowerShell-inhoud (AzureAD): https://docs.microsoft.com/powershell/azure/_active-directory_
- Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_
- Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_
- Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_

Wanneer u deze URL's gebruikt, wordt u omgeleid naar de nieuwste versie van de inhoud. Op die manier hoeft u geen versiemoniker op te geven. U voorkomt zo ook dat koppelingen naar conceptinhoud moeten worden bijgewerkt wanneer de versie verandert.

Als u een goede koppeling wilt maken, gaat u in uw browser naar de pagina waarnaar u wilt koppelen en kopieert u de URL.
Verwijder vervolgens 'https://docs.microsoft.com' en de gegevens van de landinstelling.

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
