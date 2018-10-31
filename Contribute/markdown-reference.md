---
title: Markdown-naslaginformatie voor OPS en docs.microsoft.com
description: De OPS-platformhandleiding voor Markdown- en DocFX Flavored Markdown-extensies (DFM).
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: e248eafb0247b200313ba198f2545eca947f5627
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805888"
---
# <a name="markdown-reference-for-ops"></a>Markdown-naslaginformatie voor OPS

Markdown is een lichtgewicht opmaakcodetaal met een syntaxis voor het opmaken van platte tekst. OPS ondersteunt de CommonMark-standaard voor Markdown, plus enkele aangepaste Markdown-extensies die zijn ontworpen om rijkere inhoud op docs.microsoft.com te bieden. Dit artikel bevat alfabetische naslaginformatie voor het gebruik van Markdown in OPS voor docs.microsoft.com.

U kunt voor het opstellen van Markdown elke teksteditor gebruiken. Voor elke editor die het invoegen van zowel standaard-Markdown-syntaxis als aangepaste OPS-extensies mogelijk maakt, wordt [VS Code](https://code.visualstudio.com/) met een geïnstalleerd [Docs-ontwerppakket](https://aka.ms/DocsAuthoringPack) aangeraden.

OPS is gestandaardiseerd in Markdig voor alle nieuwe opslagplaatsen, en oudere opslagplaatsen worden gemigreerd naar Markdig. U kunt het weergeven van Markdown in Markdig versus andere engines testen op [https://babelmark.github.io/](https://babelmark.github.io/).

## <a name="alerts-note-tip-important-caution-warning"></a>Waarschuwingen (Opmerking, Tip, Belangrijk, Let op, Waarschuwing)

Geeft een waarschuwing voor een OPS-specifieke Markdown-extensie om blokcitaten te maken die op docs.microsoft.com worden weergegeven met kleuren en pictogrammen die het belang van de inhoud aanduiden. De volgende typen waarschuwingen worden ondersteund:

```markdown
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

Deze waarschuwingen zien er op docs.microsoft.com als volgt uit:

> [!NOTE]
> Informatie die de gebruiker ook bij globaal scannen moet zien.

> [!TIP]
> Optionele informatie waarmee een gebruiker meer succes zal hebben.

> [!IMPORTANT]
> Informatie die essentieel voor de gebruiker is om succes te hebben.

> [!CAUTION]
> Mogelijke negatieve gevolgen van een actie.

> [!WARNING]
> Bepaalde gevaarlijke gevolgen van een actie.

## <a name="code-snippets"></a>Codefragmenten

U kunt codefragmenten in uw Markdown-bestanden insluiten:

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Koppen

OPS ondersteunt zes niveaus Markdown-koppen:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Tussen de laatste `#` en de koptekst moet een spatie staan.
- Elk Markdown-bestand moet precies één H1 hebben.
- De H1 moet de eerste inhoud in het bestand zijn na het YML-blok met metagegevens.
- H2's verschijnen automatisch in het navigatiemenu aan de rechterkant van het gepubliceerde bestand. Dit geldt niet voor koppen op een lager niveau. Gebruik H2's dus strategisch om lezers te helpen door uw inhoud te navigeren.
- HMTL-koppen, zoals `<h1>`, worden niet aanbevolen en leiden in sommige gevallen tot compileerwaarschuwingen.
- U kunt de afzonderlijke koppen in een bestand koppelen via [bladwijzers](#bookmark-links).

## <a name="html"></a>HTML

Hoewel Markdown ondersteuning biedt voor inline-HTML, wordt HTML niet aanbevolen voor het publiceren via OPS. Bovendien leidt dit, behalve bij een beperkte lijst met waarden, tot compileerfouten of -waarschuwingen. <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a>Afbeeldingen

De syntaxis voor het insluiten van een afbeelding is:

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Hierbij is `alt text` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding. Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig. Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.

Afbeeldingen moeten worden opgeslagen in een `/media`-map in uw docset. De volgende bestandstypen worden standaard voor afbeeldingen ondersteund:

- .jpg
- .png

U kunt ook ondersteuning voor andere typen afbeeldingen toevoegen door deze toe te voegen als resources aan het docfx.json-bestand<!--add link to reference when available--> voor uw docset.

## <a name="links"></a>Koppelingen

In de meeste gevallen gebruikt OPS standaard-Markdown-koppelingen naar andere bestanden en pagina's. De typen koppelingen worden in de onderstaande subsecties beschreven.

> [!TIP]
> Het Docs-ontwerppakket voor VS Code kan helpen relatieve koppelingen en bladwijzers correct in te voegen zonder dat u zich met paden bezig hoeft te houden.

> [!IMPORTANT]
> Neem geen codes voor landinstellingen, zoals nl-nl, in uw koppelingen naar Microsoft-sites op. Landinstellingscodes die in code zijn vastgelegd verhinderen dat gelokaliseerde inhoud wordt weergegeven. Dit leidt tot een slechte klantervaring voor gebruikers in andere regio's en brengt aanzienlijke lokalisatiekosten met zich mee. Wanneer u een URL uit een browser kopieert, wordt de landinstellingscode standaard opgenomen, zodat u deze handmatig moet verwijderen wanneer u een koppeling maakt. Gebruik bijvoorbeeld:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Niet:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Relatieve koppelingen naar bestanden in dezelfde docset

Een relatief pad is het pad naar het doelbestand ten opzichte van het huidige bestand. U kunt in OPS een relatief pad gebruiken om een koppeling naar ander bestand in dezelfde docset te maken. De syntaxis voor een relatief pad ziet er als volgt uit:

```markdown
[link text](../../folder/filename.md)
```

Hierbij duidt `../` één niveau hoger in de hiërarchie aan.

- Het relatieve pad wordt tijdens het compileren omgezet, met inbegrip van het verwijderen van de MD-extensie.
- U kunt ../ gebruiken om het bestand te koppelen aan een bestand in de bovenliggende map, maar dat bestand moet dan wel in dezelfde docset aanwezig zijn. U kunt ../ niet gebruiken om een bestand te koppelen aan een bestand in een andere docset-map.
- OPS ondersteunt ook een speciale vorm van een relatief pad. Deze vorm begint met het teken ~ (bijvoorbeeld ~/foo/bar.md). Met deze syntaxis wordt een bestand ten opzichte van de hoofdmap van een docset aangegeven. Ook dit type pad wordt tijdens de build gevalideerd en omgezet.

> [!IMPORTANT]
> Neem de bestandsextensie in het relatieve pad op. Bij het compileren wordt het bestaan van het doelbestand van dat relatieve pad gevalideerd. Als het relatieve pad geen bestandsextensie bevat, wordt bij het compileren waarschijnlijk een waarschuwing of verbroken koppeling gerapporteerd. Gebruik bijvoorbeeld:
>
> `[link text](../../folder/filename.md)`
>
> Niet:
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a>Absolute koppelingen naar andere bestanden in OPS

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Neem de bestandsextensie (.md) niet op. Deze koppelt naar het Linux-overzichtsbestand van buiten de Azure-docset 'articles'.

### <a name="links-to-external-sites"></a>Koppelingen naar externe sites

```markdown
[Microsoft](https://www.microsoft.com)
```

Op URL gebaseerde koppeling naar een andere webpagina (moet https:// bevatten).

### <a name="bookmark-links"></a>Bladwijzerkoppelingen

Bladwijzerkoppeling naar een kop in een ander bestand in dezelfde opslagplaats:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Bladwijzerkoppeling naar een kop in het huidige bestand:

```markdown
[Managed Disks](#managed-disks)
```

Gebruik een hash-code gevolgd door de woorden van de kop zonder leestekens en met streepjes als vervanging voor spaties.

### <a name="explicit-anchor-links"></a>Expliciete ankerkoppelingen

Expliciete ankerkoppelingen die de `<a>`-HTML-tag gebruiken worden **niet vereist of aanbevolen** behalve in hub- en landingspagina's. Gebruik in algemene Markdown-bestanden bladwijzers zoals hierboven wordt beschreven. Gebruik als volgt ankers voor hub- en landingspagina's:

`## <a id="AnchorText"> </a>Header text` of `## <a name="AnchorText"> </a>Header text`

Gebruik de volgende syntaxis om een koppeling naar expliciete ankers te maken:

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>XREF-koppelingen (kruisverwijzing)

Als u in de huidige docset of andere docsets een koppeling wilt maken naar automatisch gegenereerde pagina's met API-naslaginformatie, gebruikt u XREF-koppelingen met de unieke id (UID).

> [!NOTE]
> Als u wilt verwijzen naar pagina's met API-naslaginformatie in andere docsets, moet u `xrefService`-configuratie in het `docfx.json`-bestand toevoegen.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

De UID is gelijk aan de volledig gekwalificeerde naam van de klasse en het lid. Als u een * toevoegt na de UID, vertegenwoordigt de koppeling een overbelastingspagina en niet een specifieke API. Gebruik bijvoorbeeld `List<T>.BinarySearch*` om een koppeling naar de pagina BinarySearch Method te maken in plaats van te koppelen naar een specifieke overbelasting zoals `List<T>.BinarySearch(T, IComparer<T>)`.

Voor de syntaxis hebt u de volgende mogelijkheden:

- Automatisch koppelen: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  De optionele queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst. Standaard toont de koppelingstekst alleen de naam van het lid of het type.

- Markdown-koppeling: `[link text](xref:UID)`
  
  Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.

Voorbeelden:

- `<xref:System.String>` wordt weergegeven als String.
- `<xref:System.String?displayProperty=nameWithType>` wordt weergegeven als System.String.
- `[String class](xref:System.String)` wordt weergeven als String class.

Momenteel is er geen eenvoudige manier om de UID's te zoeken. <!-- ? -->De beste manier om de UID voor een API te zoeken, is om de bron van de API-pagina waaraan u wilt koppelen te bekijken en de waarde ms.assetid te zoeken. Afzonderlijke overbelastingswaarden worden in de bron niet weergegeven. We werken aan een beter systeem voor de toekomst.

Wanneer de UID de speciale tekens \`, \# of \* bevat, moet de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML worden gecodeerd. U ziet soms haakjes in de code, maar dat is geen vereiste.

Voorbeelden:

- System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`
- System.Exception. \#ctor wordt `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Lijsten (Genummerd, Met opsommingstekens, Controlelijst)

### <a name="numbered-list"></a>Genummerde lijst

Als u een genummerde lijst wilt maken, kunt u alle 1's gebruiken. Deze worden bij het publiceren weergegeven als een sequentiële lijst. Voor betere leesbaarheid van de bron kunt u uw lijsten verhogen.

Gebruik geen letters in lijsten, ook niet in geneste lijsten. Deze worden bij het publiceren via OPS niet goed weergegeven. Geneste lijsten die gebruikmaken van nummers, worden bij het publiceren weergegeven als kleine letters. Bijvoorbeeld:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Dit wordt weergegeven als:

1. Dit is
1. een bovenliggende lijst met nummers
   1. en dit is
   1. een geneste lijst met nummers
1. (einde)

### <a name="bulleted-list"></a>Lijst met opsommingstekens

Als u een lijst met opsommingstekens wilt maken, gebruikt u `-` gevolgd door een spatie aan het begin van elke regel:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Dit wordt weergegeven als:

- Dit is
- een bovenliggende lijst met opsommingstekens
  - en dit is
  - een geneste lijst met opsommingstekens
- Klaar!

### <a name="checklist"></a>Controlelijst

Controlelijsten zijn beschikbaar voor gebruik op (alleen) docs.microsoft.com via een aangepaste Markdown-extensie:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Dit voorbeeld wordt op docs.microsoft.com weergegeven als:

> [!div class="checklist"]
> * Lijstitem 1
> * Lijstitem 2
> * Lijstitem 3

Gebruik controlelijsten aan het begin of eind van een artikel om inhoud voor 'Wat gaat u leren' of 'Wat hebt u geleerd' samen te vatten. Voeg geen willekeurige controlelijsten ergens anders in een artikel toe.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Actie volgende stap

U kunt een aangepaste extensie gebruiken om een knop voor de actie van de volgende stap toe te voegen aan pagina's op (alleen) docs.microsoft.com.

De syntaxis ziet er als volgt uit:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Bijvoorbeeld:

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Dit wordt weergegeven als:

> [!div class="nextstepaction"]
> [Informatie over de basisstijl](style-quick-start.md)

U kunt elke ondersteunde koppeling in een volgende stapactie gebruiken, met inbegrip van een Markdown-koppeling naar een andere webpagina. In de meeste gevallen is de koppeling voor de volgende actie een relatieve koppeling naar een ander bestand in dezelfde docset.

## <a name="section-definition"></a>Sectiedefinitie

<!-- more info about this would be helpful! --> U moet mogelijk een sectie definiëren. Deze syntaxis wordt voornamelijk gebruikt voor codetabellen.
Zie het volgende voorbeeld:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

De eraan voorafgaande blockquote-Markdown-tekst wordt weergegeven als:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Selectors

<!-- could be more clear! --> U kunt een selector gebruiken wanneer u verschillende pagina's voor hetzelfde artikel met elkaar wilt verbinden. Lezers kunnen dan schakelen tussen die pagina's.

> [!NOTE]
> Deze extensie werkt anders tussen docs.microsoft.com en MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Single selector

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... wordt als volgt weergegeven:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Multi-selector

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... wordt als volgt weergegeven:

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a>Tabellen

De eenvoudigste manier om een tabel in Markdown te maken is gebruik te maken van pipes en regels. Als u een standaardtabel met een kop wilt maken, laat u de eerste regel volgen door een stippellijn:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Dit wordt weergegeven als:

|Dit is   |een eenvoudige   |tabelkop|
|----------|-----------|------------|
|tabel     |gegevens       |hier        |
|deze hoeft niet|precies   |te zijn uitgelijnd.||

U kunt ook een tabel zonder kop maken. Ga bijvoorbeeld als volgt te werk om een lijst met meerdere kolommen te maken:

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

Dit wordt als volgt weergegeven:

|   |   |
| - | - |
| Deze | tabel |
| heeft geen | kop |

U kunt de kolommen uitlijnen met behulp van dubbele punten:

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Wordt weergegeven als:

|                  |
|------------------|
|    rechts uitgelijnd:|
|:links uitgelijnd     |
|:gecentreerd        :|

> [!TIP]
> U kunt met Docs Authoring Extension voor VS Code gemakkelijk basis-Markdown-tabellen toevoegen.
>
> U kunt ook een [onlinegenerator voor tabellen](http://www.tablesgenerator.com/markdown_tables) gebruiken.

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Dit werkt alleen op de site docs.microsoft.com.

Als u een tabel in Markdown maakt, kan de tabel worden uitgebreid naar het navigatievenster rechts, waardoor de tabel onleesbaar wordt. Dat is op te lossen door bij het renderen van Docs de tabel op te splitsen wanneer dat nodig is. U laat eenvoudig de tabel teruglopen met de aangepaste klasse `[!div class="mx-tdBreakAll"]`.

Hier ziet u een Markdown-voorbeeld van een tabel met drie rijen die teruglopen door gebruik te maken van een `div` met de klassenaam `mx-tdBreakAll`.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Deze wordt als volgt weergegeven:

> [!div class="mx-tdBreakAll"]
> |Naam|Syntaxis|Verplicht voor installatie op de achtergrond?|Beschrijving|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Ja|Het installatieprogramma wordt uitgevoerd zonder dat de UI of prompts worden weergegeven.|
> |NoRestart|/norestart|Nee|Onderdrukt elke poging tot herstarten. De UI geeft standaard een prompt vóór de herstart.|
> |Help|/help|Nee|Biedt hulp- en naslaginformatie. Geeft het juiste gebruik van de setup-opdracht weer, samen met een overzicht van alle opties en alle gedrag.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Dit werkt alleen op de site docs.microsoft.com.

Er kunnen soms hele lange woorden in de tweede kolom van een tabel staan. Om ervoor te zorgen dat lange woorden netjes worden gesplitst, kunt u de klasse `mx-tdCol2BreakAll` toepassen met behulp van de `div`-wrapper-syntaxis zoals eerder besproken.

### <a name="html-tables"></a>HTML-tabellen

HTML-tabellen worden niet aanbevolen voor docs.microsoft.com. Ze kunnen niet door mensen worden gelezen in de bron. Dit is wel een basisprincipe van Markdown.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Video's

### <a name="embedding-videos-into-a-markdown-page"></a>Video's insluiten op een Markdown-pagina

Momenteel biedt OPS ondersteuning voor video's die zijn gepubliceerd op een van de volgende drie locaties:

- YouTube
- Channel 9
- Het eigen One Player-systeem van Microsoft

U kunt een video insluiten met de volgende syntaxis zodat OPS de video kan renderen.

```markdown
> [!VIDEO <embedded_video_link>]
```

Voorbeeld:

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... wordt weergegeven als:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

En deze wordt als volgt weergegeven op gepubliceerde pagina's:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> De URL van de CH9-video moet beginnen met `https` en eindigen met `/player`. Anders wordt de hele pagina en niet alleen de video ingesloten.

### <a name="uploading-new-videos"></a>Nieuwe video's uploaden

Alle nieuwe video's moeten worden geüpload met het volgende proces:

1. Neem deel aan de groep **docs_video_users** op IDWEB.
1. Ga naar https://aka.ms/VideoUploadRequest en vul de gegevens voor uw video in. Het volgende is nodig (geen van deze items is zichtbaar voor het publiek):
    1. Een titel voor uw video.
    1. Een lijst met producten/services waarop uw video betrekking heeft.
    1. De doelpagina of (als u de pagina nog niet hebt) de docset waarop uw video wordt gehost.
    1. Een koppeling naar het MP4-bestand voor uw video (als u geen locatie hebt waar het bestand kan worden geplaatst, kunt u het tijdelijk hier plaatsen:   `\\scratch2\scratch\apex`). MP4-bestanden moeten 720p of hoger zijn.
    1. Een beschrijving van de video.
1. Verzend dat item (sla het op).
1. De video wordt binnen twee werkdagen geüpload. De koppeling die u voor het insluiten nodig hebt, wordt in het werkitem geplaatst en deze wordt *terug naar u* omgezet.
1. Nadat u de videokoppeling hebt vastgelegd, sluit u het werkitem.
1. De videokoppeling kan vervolgens aan uw bericht worden toegevoegd met deze syntaxis:

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
