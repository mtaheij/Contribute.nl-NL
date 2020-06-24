---
title: Koppelingen in documentatie gebruiken
description: Dit artikel biedt ondersteuning voor het maken van koppelingen naar inhoud in docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: 94ba4cefd9aff70b38502aa397a3761127c8089f
ms.sourcegitcommit: 9852045bac75fd5d90c0ffc88d2a17dd45ba015f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/19/2020
ms.locfileid: "85107109"
---
# <a name="use-links-in-documentation"></a>Koppelingen in documentatie gebruiken

In dit artikel wordt beschreven hoe u hyperlinks gebruikt van pagina's die op docs.microsoft.com worden gehost. Koppelingen kunnen eenvoudig in Markdown worden toegevoegd, met een aantal afwijkende conventies. Koppelingen verwijzen gebruikers naar inhoud op dezelfde pagina, op omliggende pagina's of op externe websites en URL's.

De back-end van docs.microsoft.com gebruikt Open Publishing Services (OPS), dat ondersteuning biedt voor Markdown die compatibel is met [CommonMark][] en is geparseerd via de parseerengine [Markdig][]. Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)][GFM], aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt. Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.

> [!IMPORTANT]
> Alle koppelingen moeten zijn beveiligd (`https` vs. `http`) wanneer het doel dit ondersteunt (dit zou voor de grote meerderheid moeten gelden).

## <a name="link-text"></a>Tekst van koppeling

De woorden die u gebruikt in de tekst van de koppeling moeten duidelijk de bestemming van de koppeling aangeven. Gebruik dus normale beschrijvende tekst of de titel van de pagina die u wilt koppelen.

> [!IMPORTANT]
> Gebruik niet 'klik hier'. Het is nadelig voor de zoekmachineoptimalisatie en geeft geen goede beschrijving van het doelobject.

**Goed:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**Fout:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Koppelingen van het ene artikel naar het andere

Er zijn twee typen hyperlinks die worden ondersteund door het publicatie systeem: **URL's** en **bestandskoppelingen**.

Een URL-koppeling kan een URL-pad zijn dat relatief is ten opzichte van de hoofdmap van docs.microsoft.com of een absolute URL die de volledige URL-syntaxis bevat (bijvoorbeeld `https://github.com/MicrosoftDocs/PowerShell-Docs`).

- Gebruik URL-koppelingen wanneer u een koppeling maakt naar inhoud buiten de huidige _docset_ of tussen automatisch gegenereerde naslaginformatie en conceptuele artikelen in de docset.
- De eenvoudigste manier om een relatieve koppeling te maken, is door de URL te kopiëren uit uw browser en vervolgens `https://docs.microsoft.com/en-us` te verwijderen uit de waarde die u in Markdown hebt geplakt.
   - Neem geen landinstellingen op in URL's voor Microsoft-eigenschappen (u kunt bijvoorbeeld '/en-us' uit de URL verwijderen).

Een bestandskoppeling wordt gebruikt om een koppeling te maken van het ene naar het andere artikel binnen de docset.

- Alle bestandspaden gebruiken tekens die gebruikmaken van slash- (`/`) in plaats van backslash-tekens.
- Een artikel wordt gekoppeld aan een ander artikel in dezelfde map:

  `[link text](article-name.md)`

- Een artikel wordt gekoppeld aan een artikel in de bovenliggende map van de huidige map:

  `[link text](../article-name.md)`

- Een artikel wordt gekoppeld aan een artikel in een submap van de huidige map:

  `[link text](directory/article-name.md)`

- Een artikel wordt gekoppeld aan een artikel in een submap van de bovenliggende map van de huidige map:

  `[link text](../directory/article-name.md)`

> [!NOTE]
> Geen van de eerder genoemde voorbeelden gebruikt de `~/` als onderdeel van de koppeling. Als u een koppeling wilt maken naar een absoluut pad dat bij de hoofdmap van de opslagplaats begint, begint u de koppeling met `/`. Als u de `~/` opneemt, worden de koppelingen ongeldig als er wordt verwezen naar bronopslagplaatsen in GitHub. Als u het pad begint met `/`, wordt het correct omgezet.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>Structuur van koppelingen op docs.microsoft.com

Inhoud die is gepubliceerd op docs.microsoft.com heeft de volgende URL-structuur:

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

Voorbeelden:

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` -geeft de taal van het artikel weer (bijvoorbeeld: en-us of de-de)
- `<product-service>` -de naam van het product of de service (bijvoorbeeld: powershell, dotnet, of azure)
- `[<feature-service>]` -(optioneel) de naam van de functie of subservice van het product (bijvoorbeeld: csharp of load balancer)
- `[<subfolder>]` -(optioneel) de naam van een submap binnen een functie
- `<topic>` -de naam van het artikelbestand voor het onderwerp (bijvoorbeeld: load balancer-overzicht of overzicht)
- `[?view=\<view-name>]` -(optioneel) de weergavenaam die wordt gebruikt door de versieselector voor inhoud met meerdere beschikbare versies (bijvoorbeeld: azps-3.5.0)

> [!TIP]
> Artikelen in dezelfde _docset_ bevatten in de meeste gevallen hetzelfde URL-fragment `<product-service>`. Bijvoorbeeld:
> - Dezelfde docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - Verschillende docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>Bladwijzerkoppelingen

Als u een bladwijzerkoppeling wilt maken naar een kop in het *huidige* bestand, gebruikt u een hash-symbool gevolgd door de kop in kleine letters. Verwijder leestekens uit de kop en vervang spaties door streepjes:

```markdown
[Managed Disks](#managed-disks)
```

Als u wilt koppelen naar een bladwijzerkop in een ander artikel, gebruikt u de koppeling ten opzichte van het bestand of de site plus een hash-symbool, gevolgd door de woorden van de kop. Verwijder leestekens uit de kop en vervang spaties door streepjes:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

U kunt ook de bladwijzerkoppeling uit de URL kopiëren. Als u de URL wilt vinden, beweegt u de muisaanwijzer over de kopregel op docs.microsoft.com. Er wordt nu een koppelingspictogram weergegeven:

![Koppelingspictogram in artikelkop](media/how-to-write-links/bookmark-link.png)

Klik op het koppelingspictogram en kopieer vervolgens de ankertekst van de bladwijzer uit de URL (dat wil zeggen, het deel na de hash).

> [!NOTE]
> De Docs-extensie bevat ook hulpprogramma's om koppelingen te maken.

### <a name="explicit-anchor-links"></a>Expliciete ankerkoppelingen

De toevoeging van expliciete ankerkoppelingen via de HTML-tag `<a>` is niet vereist of aanbevolen, behalve in hub- en landingspagina's. Gebruik in plaats daarvan de automatisch gegenereerde bladwijzers zoals beschreven in [bladwijzerkoppelingen](#bookmark-links). Geef als volgt ankers op voor hub- en landingspagina's:

```markdown
## <a id="anchortext" />Header text
```

of

```markdown
## <a name="anchortext" />Header text
```

En geef het volgende op om een koppeling naar het anker te maken:

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> Ankertekst moet altijd uit kleine letters bestaan en mag geen spaties bevatten.

## <a name="xref-cross-reference-links"></a>XRef-koppelingen (kruisverwijzing)

XRef-koppelingen zijn de aanbevolen manier om een koppeling naar API's te maken, omdat ze tijdens het bouwen worden gevalideerd. Als u in de huidige docset of andere docsets een koppeling wilt maken naar automatisch gegenereerde pagina's met API-naslaginformatie, gebruikt u XRef-koppelingen met de unieke id ([UID](#determine-the-uid)) van het type of lid.

> [!TIP]
> U kunt de [Docs Markdown-extensie voor VS Code][docsextension] (onderdeel van het Docs Authoring Pack) gebruiken om .NET XRref-koppelingen in te voegen die worden weergegeven in de [.NET API-browser][].

Controleer of de API waarnaar u een koppeling wilt maken zich op [docs.microsoft.com][docs] bevindt, door alle of een deel van de volledige naam in het zoekvak van de [.NET API-browser][] of [Windows UWP][] te typen. Als er geen resultaten worden weergegeven, is het type nog niet aanwezig op docs.microsoft.com.

Voor de syntaxis hebt u de volgende mogelijkheden:

- Automatische koppelingen:

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   Standaard toont de koppelingstekst alleen de naam van het lid of het type. De optionele queryparameter `displayProperty=nameWithType` genereert een volledig gekwalificeerde koppelingstekst, dat wil zeggen, **naamruimte.type** voor typen en **type.lid** voor typeleden, inclusief opsommingstypeleden.

- Koppelingen in de Markdown-stijl:

   ```markdown
   [link text](xref:UID)
   ```

   Gebruik koppelingen in de Markdown-stijl voor XRef als u de tekst van de koppeling wilt aanpassen die wordt weergegeven.

Voorbeelden:

- **\<xref:System.String>** wordt weergegeven als <xref:System.String>

- **\<xref:System.String?displayProperty=nameWithType>** wordt weergegeven als <xref:System.String?displayProperty=nameWithType>

- **\[String class](xref:System.String)** weergegeven als [String class](xref:System.String).

De queryparameter `displayProperty=fullName` werkt op dezelfde manier als `displayProperty=nameWithType` voor klassen. Dat wil zeggen dat de koppelingstekst **naamruimte.klassenaam** wordt. De koppelingstekst wordt voor leden echter weergegeven als **naamruimte.klassenaam.lidnaam**, wat mogelijk niet gewenst is.

> [!NOTE]
> UID's zijn hoofdlettergevoelig. `<xref:System.Object>` wordt bijvoorbeeld correct omgezet, maar `<xref:system.object>` niet.

### <a name="xref-build-warnings-and-incremental-builds"></a>Waarschuwingen voor XRef-builds en incrementele builds

In een incrementele build worden alleen bestanden gecompileerd die zijn gewijzigd of waarvoor een wijziging is aangebracht. Als er een build-waarschuwing over een ongeldige XRef-koppeling wordt weergegeven, maar de koppeling wel geldig is, kan dit zijn omdat de build incrementeel is. Het bestand dat de waarschuwing veroorzaakt, is niet gewijzigd, dus is deze niet gecompileerd en worden eerdere waarschuwingen opnieuw afgespeeld. De waarschuwing verdwijnt wanneer het bestand wordt gewijzigd of als u een volledige build activeert (u kunt een volledige build starten op ops.microsoft.com). Dit is een nadeel van incrementele builds, omdat DocFX geen gegevensupdate kan detecteren in de XRef-service.

### <a name="determine-the-uid"></a>De UID bepalen

De UID is doorgaans gelijk de volledig gekwalificeerde klasse- of lidnaam. Er zijn ten minste twee manieren om de UID te bepalen:

- Klik met de rechtermuisknop op de pagina [Docs][docs] voor een type of lid, selecteer **Bron weergeven** en kopieer vervolgens de waarde voor **Inhoud** voor **ms.assetid**:

  ![ms.assetid in de bron voor webpagina](media/how-to-write-links/ms-assetid.png)

- Gebruik de [site voor automatisch aanvullen][] door een deel van of de volledige naam van het type aan de URL toe te voegen. Als u bijvoorbeeld `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in de adresbalk van uw browser invoert, worden alle typen en methoden weergegeven die **WriteLine** in hun naam bevatten, samen met de bijbehorende UID.

#### <a name="verify-the-uid"></a>De UID verifiëren

Als u wilt testen of u de juiste UID hebt, vervangt u **System.String** in de volgende URL door uw UID en plakt u deze in de adresbalk van een browser:

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> De UID in de URL is hoofdlettergevoelig, en als u een UID voor een overbelasting van een methode controleert, moet u geen spaties tussen de parametertypen opnemen.

Als u een van de volgende items ziet, hebt u de juiste UID:

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

Als alleen `[]` op de pagina worden weergegeven, hebt u de verkeerde UID.

### <a name="percent-encoding-of-urls"></a>Percentagecodering van URL's

Speciale tekens in de UID moeten de volgende HTML-codering hebben:

| Teken | HTML-codering |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

Bekijk een volledige lijst met [percentagecodes](https://en.wikipedia.org/wiki/Percent-encoding).

Voorbeelden van codering:

- ``System.Threading.Tasks.Task`1`` wordt als `System.Threading.Tasks.Task%601` gecodeerd (zie sectie [ over algemene typen](#generic-types))

- `System.Exception.#ctor` wordt gecodeerd als `System.Exception.%23ctor`

- `System.Object.Equals*` wordt gecodeerd als `System.Object.Equals%2A`

### <a name="generic-types"></a>Algemene typen

Algemene typen zijn typen als `System.Collections.Generic.List<T>`. Als u naar dit type bladert in de [.NET API-browser](https://docs.microsoft.com/dotnet/api/) en de bijbehorende URL bekijkt, ziet u dat `<T>` als `-1` is geschreven in de URL, die in werkelijkheid staat voor **'1**:

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

Als u een koppeling wilt maken naar een algemeen type zoals **List\<T>** , codeert u het accent grave-teken **\`** als **%60**, zoals wordt weergegeven in het volgende voorbeeld:

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>Methoden

Als u een koppeling wilt maken naar een methode, kunt u een koppeling maken naar de algemene methodenpagina door een sterretje (`*`) toe te voegen aan de naam van de methode of aan een specifieke overbelasting. Gebruik bijvoorbeeld de algemene pagina wanneer u een koppeling wilt maken naar de methode `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` zonder specifieke parametertypen. Het sterretje wordt gecodeerd als `%2A`. Bijvoorbeeld:

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` vormt een koppeling naar <xref:System.Object.Equals%2A?displayProperty=nameWithType>

Als u een koppeling wilt maken naar een specifieke overbelasting, voegt u haakjes achter de naam van de methode toe en voegt u de volledige typenaam van elke parameter toe. Plaats geen spatie tussen de typenamen, anders werkt de koppeling niet. Bijvoorbeeld:

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` maakt een koppeling naar <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>

## <a name="links-from-includes"></a>Koppelingen vanuit Include-bestanden

Omdat Include-bestanden deel uitmaken van een andere map moet u een langer relatief pad gebruiken. Gebruik de volgende notatie om vanuit een Include-bestand een koppeling naar een artikel te maken:

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> Met de [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)-extensie voor Visual Studio Code kunt u relatieve koppelingen en bladwijzers correct invoegen zonder dat u zich met paden bezig hoeft te houden.

## <a name="links-in-selectors"></a>Koppelingen in selectors

Een selector is een navigatieonderdeel dat als vervolgkeuzelijst in een docs-artikel wordt weergegeven. Als de lezer een waarde in de vervolgkeuzelijst selecteert, wordt het geselecteerde artikel geopend in de browser. De selectorlijst bevat gewoonlijk koppelingen naar nauw verwante artikelen, bijvoorbeeld over hetzelfde onderwerp in meerdere programmeertalen, of naar een reeks nauw verwante artikelen.

Als u met selectors werkt die zijn opgenomen in een Include-bestand, gebruikt u de volgende koppelingsstructuur:

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
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
- **Controle van de nieuwheid**: Controleer of de inhoud van de derde partij nog steeds actueel, correct en relevant is en of de koppeling niet is gewijzigd.
- **Offsite**: Zorg ervoor dat gebruikers er zich van bewust zijn dat ze naar een andere site gaan. Als dat niet blijkt uit de context, maakt u dat met een aparte zin duidelijk. Bijvoorbeeld: Bijvoorbeeld: "Tot de vereisten behoren ook de Android-ontwikkelhulpprogramma's, die u kunt downloaden op de Android Studio-site."
- **Volgende stappen**: Het is prima om een koppeling te maken naar, bijvoorbeeld, een MVP-blog in de sectie Volgende stappen. Maar nogmaals, wijs de gebruikers erop dat ze de site verlaten.
- **Juridisch**: We kunnen een beroep doen op de juridisch bindende bepalingen onder **Koppelingen naar de sites van derden** in de voettekst **Gebruiksvoorwaarden** op elke microsoft.com-pagina.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API-browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[site voor automatisch aanvullen]: https://xref.docs.microsoft.com/autocomplete?text=
