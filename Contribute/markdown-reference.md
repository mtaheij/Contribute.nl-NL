---
title: Markdown-naslaginformatie voor docs.microsoft.com
description: Maak kennis met de Markdown-functies en -syntaxis die worden gebruikt op het Microsoft Docs-platform.
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 14cc9f0912149eb342c97d0dd7d2776bd54c84e7
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331953"
---
# <a name="docs-markdown-reference"></a>Docs Markdown-naslaginformatie

Dit artikel bevat alfabetische naslaginformatie voor het schrijven van Markdown voor docs.microsoft.com (Docs).

[Markdown](https://daringfireball.net/projects/markdown/) is een lichtgewicht opmaakcodetaal met een syntaxis voor platte tekst. Docs biedt ondersteuning voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parserengine [Markdig](https://github.com/lunet-io/markdig). Docs biedt ook ondersteuning voor aangepaste Markdown-extensies die uitgebreide inhoud op de Docs-site bieden.

U kunt u elke teksteditor gebruiken voor het schrijven van Markdown, maar u kunt het beste [Visual Studio Code](https://code.visualstudio.com/) met het [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) gebruiken. Het Docs Authoring Pack bevat bewerkingsprogramma's en preview-functionaliteit waarmee u kunt zien hoe uw artikelen eruitzien zoals ze worden weergegeven op Docs.

## <a name="alerts-note-tip-important-caution-warning"></a>Waarschuwingen (Opmerking, Tip, Belangrijk, Let op, Waarschuwing)

Dit zijn waarschuwingen voor een Markdown-extensie om blokcitaten te maken die op docs.microsoft.com worden weergegeven met kleuren en pictogrammen die het belang van de inhoud aanduiden. De volgende typen waarschuwingen worden ondersteund:

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
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>Punthaken

Als u in lopende tekst punthaken gebruikt, bijvoorbeeld om een tijdelijke aanduiding aan te geven, moet u de punthaken handmatig coderen. Anders zal Markdown deze aanzien voor HTML-code.

Voorbeeld: codeer `<script name>` als `&lt;script name&gt;` of `\<script name>`.

Punthaken hoeven niet te worden voorafgegaan in tekst die is opgemaakt als code in regels of in codeblokken.

## <a name="apostrophes-and-quotation-marks"></a>Apostroffen en aanhalingstekens

Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens. Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens. Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s

Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:

- Linker dubbel aanhalingsteken (openen): `&#8220;`
- Rechter dubbel aanhalingsteken (sluiten): `&#8221;`
- Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`
- Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`

## <a name="blockquotes"></a>Blokcitaten

Blokcitaten worden gemaakt met het teken `>`:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

Het voorbeeld hierboven wordt als volgt weergegeven:

> Dit is een blokcitaat. Deze wordt doorgaans ingesprongen weergegeven met een andere achtergrondkleur.

## <a name="bold-and-italic-text"></a>Vetgedrukte en cursieve tekst

Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:

```markdown
This text is **bold**.
```

Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:

```markdown
This text is *italic*.
```

Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Codefragmenten

Docs Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen. Zie [Code toevoegen aan docs](code-in-docs.md)voor meer informatie.

## <a name="columns"></a>Kolommen

Met de Markdown-extensie **kolommen** kunnen Docs-schrijvers op kolommen gebaseerde inhoudsindelingen toevoegen die flexibelere en krachtiger zijn dan normale Markdown-tabellen, die alleen geschikt zijn voor echte tabellaire gegevens. U kunt maximaal vier kolommen toevoegen en het optionele kenmerk `span` gebruiken om twee of meer kolommen samen te voegen.

De syntaxis voor kolommen ziet er als volgt uit:

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

Kolommen mogen alleen elementaire Markdown inclusief afbeeldingen bevatten. Kopteksten, tabellen, tabs en andere complexe structuren mogen niet worden gebruikt. Een rij kan geen inhoud buiten een kolom bevatten.

Met de volgende Markdown maakt u bijvoorbeeld één kolom die bestaat uit twee kolombreedten en één standaardkolom (geen `span`):

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

Dit wordt weergegeven als:

:::row:::
   :::column span="2":::
      **Dit is een kolom met twee kolombreedten met veel tekst.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **Dit is een kolom met één kolombreedte met een afbeelding.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>Koppen

Docs ondersteunt zes niveaus Markdown-koppen:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Tussen de laatste `#` en de koptekst moet een spatie staan.
- Elk Markdown-bestand moet precies één H1-koptekst hebben.
- De H1-koptekst moet de eerste inhoud in het bestand zijn na het YML-blok met metagegevens.
- H2-kopteksten verschijnen automatisch in het navigatiemenu aan de rechterkant van het gepubliceerde bestand. Dit geldt niet voor koppen op een lager niveau. Gebruik H2's dus strategisch om lezers te helpen door uw inhoud te navigeren.
- HMTL-koppen, zoals `<h1>`, worden niet aanbevolen en leiden in sommige gevallen tot opbouwwaarschuwingen.
- U kunt de afzonderlijke koppen in een bestand koppelen via [bladwijzerkoppelingen](how-to-write-links.md#links-to-anchors).

## <a name="html"></a>HTML

Hoewel Markdown ondersteuning biedt voor inline-HTML, wordt HTML niet aanbevolen voor het publiceren naar Docs. Bovendien leidt dit, behalve bij een beperkte lijst met waarden, tot compileerfouten of -waarschuwingen. 

## <a name="images"></a>Afbeeldingen

De volgende bestandstypen worden standaard voor afbeeldingen ondersteund:

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>Standaard conceptuele afbeeldingen (standaard Markdown)

De basis Markdown-syntaxis om een afbeelding in te sluiten is:

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Hierbij is `<alt text>` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding. Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig. Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.

Onderstrepingstekens in alternatieve tekst worden niet correct weergegeven, tenzij u ze markeert als bijzondere tekens door ze met een backslash (`\_`) toe te voegen als voorvoegsel. Kopieer echter geen bestandsnamen om te gebruiken als alternatieve tekst. Dus in plaats van dit:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Schrijft u dit:

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Standaard conceptuele afbeeldingen (Docs Markdown)

De aangepaste Docs-extensie `:::image:::` ondersteunt standaardafbeeldingen, complexe afbeeldingen en pictogrammen.

De oudere Markdown-syntaxis kan nog worden gebruikt voor standaardafbeeldingen, maar u kunt beter gebruikmaken van de nieuwe extensie, omdat deze krachtigere functionaliteit ondersteunt, zoals het opgeven van een lokalisatiebereik dat afwijkt van het bovenliggende onderwerp. Deze geavanceerde functionaliteit wordt in de toekomst verder uitgebreid, zoals het selecteren van de gedeelde afbeeldingengalerie in plaats van het opgeven van een lokale afbeelding. De nieuwe syntaxis ziet er als volgt uit:

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

Als `type="content"` (standaard), zijn zowel `source` als `alt-text` vereist.

### <a name="complex-images-with-long-descriptions"></a>Complexe afbeeldingen met lange beschrijvingen

U kunt deze extensie ook gebruiken om een afbeelding toe te voegen met een lange beschrijving die wordt gelezen door schermlezers, maar niet visueel wordt weergegeven op de gepubliceerde pagina. Lange beschrijvingen zijn een toegangsvereiste voor complexe afbeeldingen, zoals grafieken. De syntaxis ziet er als volgt uit:

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

Als `type="complex"`, `source`, `alt-text`, zijn een lange beschrijving en de tag `:::image-end:::` vereist.

### <a name="specifying-loc-scope"></a>Lokalisatiebereik opgeven

Soms wijkt het lokalisatiebereik voor een afbeelding af van het bereik van een artikel of de module waarin de afbeelding is opgenomen. Dit kan leiden tot onjuistheden, bijvoorbeeld als een schermopname van een product per ongeluk wordt gelokaliseerd in een taal waarin het product niet beschikbaar is. Om dit te voorkomen, kunt u het optionele kenmerk `loc-scope` opgeven in afbeeldingen van het type `content` en `complex`.

### <a name="icons"></a>Pictogrammen

De afbeeldingsextensie biedt ondersteuning voor pictogrammen. Dit zijn decoratieve afbeeldingen die geen alternatieve tekst mogen bevatten. De syntaxis voor pictogrammen ziet er als volgt uit:

```Markdown
:::image type="icon" source="<folderPath>":::
```

Als `type="icon"`, moet alleen `source` worden opgegeven.

## <a name="included-markdown-files"></a>Ingesloten Markdown-bestanden

Wanneer de Markdown-bestanden moeten worden herhaald in meerdere artikelen, kunt u een Include-bestand gebruiken. Met de functie Includes kunnen Docs de verwijzing tijdens het bouwen vervangen door de inhoud van het Include-bestand. U kunt Include-bestanden op de volgende manieren gebruiken:

- Inline: Een gewoon stuk tekst inline hergebruiken in een zin.
- Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.

Een inline- of blokinsluitingsbestand is niets meer of minder dan een Markdown-bestand (.md). Deze kunnen elke geldige Markdown bevatten. Include-bestanden bevinden zich doorgaans in een submap *includes* in de hoofdmap van de opslagplaats. Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.

### <a name="includes-syntax"></a>Ingesloten syntaxis

Een blokinsluiting wordt op een eigen regel weergegeven:

```markdown
[!INCLUDE [<title>](<filepath>)]
```

Inline-insluitingen bevinden zich in een regel:

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

waarbij `<title>` de naam van het bestand is en `<filepath>` het relatieve pad naar het bestand is. `INCLUDE` moet met een hoofdletter beginnen en er moet een spatie voor de `<title>` staan.

Dit zijn de vereisten en overwegingen voor insluitingsbestanden:

- Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie. Gebruik deze niet voor content die minder lang is dan een zin.
- Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van Docs-extensies. Ze worden pas weergegeven na publicatie.
- Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen. Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel.
- Voeg geen insluitingsbestanden in andere insluitingsbestanden in.
- Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>` */includes/media*. In de hoofdmap van de *mediamap* mogen zich geen afbeeldingen bevinden. Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende *mediamap* te worden gemaakt.
- Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden. Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel. Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.
- Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.  Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.

## <a name="links"></a>Koppelingen

Zie [Koppelingen in documentatie gebruiken](how-to-write-links.md) voor meer informatie over de syntaxis voor koppelingen.

## <a name="lists-numbered-bulleted-checklist"></a>Lijsten (Genummerd, Met opsommingstekens, Controlelijst)

### <a name="numbered-list"></a>Genummerde lijst

U kunt alle 1's gebruiken om een genummerde lijst te maken. De nummers worden bij het publiceren weergegeven als een sequentiële lijst in oplopende volgorde. Voor betere leesbaarheid van de bron kunt u uw lijsten handmatig verhogen.

Gebruik geen letters in lijsten, ook niet in geneste lijsten. Deze worden bij het publiceren naar Docs niet goed weergegeven. Geneste lijsten die gebruikmaken van nummers, worden bij het publiceren weergegeven als kleine letters. Bijvoorbeeld:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Dit wordt weergegeven als:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>Lijst met opsommingstekens

Als u een lijst met opsommingstekens wilt maken, gebruikt u `-` of `*` gevolgd door een spatie aan het begin van elke regel:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Dit wordt weergegeven als:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

Welke syntaxis u ook gebruikt, `-` of `*`, gebruik deze consistent binnen een artikel.

### <a name="checklist"></a>Controlelijst

Controlelijsten zijn beschikbaar voor gebruik op Docs via een aangepaste Markdown-extensie:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Dit voorbeeld wordt op Docs weergegeven als:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Gebruik controlelijsten aan het begin of eind van een artikel om inhoud voor 'Wat gaat u leren' of 'Wat hebt u geleerd' samen te vatten. Voeg geen willekeurige controlelijsten ergens anders in een artikel toe.

## <a name="next-step-action"></a>Actie volgende stap

U kunt een aangepaste extensie gebruiken om een knop voor de actie van de volgende stap toe te voegen aan Docs-pagina's.

De syntaxis ziet er als volgt uit:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Bijvoorbeeld:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Dit wordt weergegeven als:

> [!div class="nextstepaction"]
> [Meer informatie over het toevoegen van code aan artikelen](code-in-docs.md)

U kunt elke ondersteunde koppeling in een volgende stapactie gebruiken, met inbegrip van een Markdown-koppeling naar een andere webpagina. In de meeste gevallen is de koppeling voor de volgende actie een relatieve koppeling naar een ander bestand in dezelfde docset.

## <a name="non-localized-strings"></a>Niet-gelokaliseerde tekenreeksen

U kunt de aangepaste Markdown-extensie `no-loc` gebruiken om tekenreeksen te identificeren van inhoud die tijdens het lokalisatieproces moeten worden genegeerd.

Alle aangeroepen tekenreeksen zijn hoofdlettergevoelig. Dat wil zeggen dat de tekenreeks exact moet overeenkomen om te worden genegeerd.

Als u een afzonderlijke tekenreeks als niet-lokaliseerbaar wilt markeren, gebruikt u de volgende syntaxis:

```markdown
:::no-loc text="String":::
```

In het volgende voorbeeld wordt slechts één exemplaar van `Document` genegeerd tijdens het lokalisatieproces:

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> Gebruik `\` om speciale tekens te escapen:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

U kunt ook metagegevens in de YAML-header gebruiken om alle exemplaren van een tekenreeks binnen het huidige Markdown-bestand te markeren als niet-lokaliseerbaar:

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> De metagegevens voor niet-lokaliseerbaar worden niet ondersteund als globale metagegevens in het bestand *docfx.json*. De gelokaliseerde pijplijn leest het bestand *docfx.json* niet. Daarom moeten de metagegevens voor niet-lokaliseerbaar aan elk afzonderlijk bronbestand worden toegevoegd.

In het volgende voorbeeld wordt zowel in de metagegevens `title` als in de Markdown-header het woord `Document` tijdens het lokalisatieproces genegeerd.

In de metagegevens `description` en de belangrijkste inhoud van Markdown wordt het woord `document` gelokaliseerd, omdat het niet begint met een hoofdletter `D`.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>Selectors

Selectors zijn UI-elementen waarmee de gebruiker tussen meerdere varianten van hetzelfde artikel kan schakelen. Ze worden gebruikt in sommige docsets om verschillen in de implementatie van technologieën of platformen aan te pakken. Selectors zijn doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars.

Omdat dezelfde selector Markdown in elk artikelbestand in de selector wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand. Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelbestanden waarin dezelfde selector wordt gebruikt.

Er zijn twee soorten selectors, een enkelvoudige selector en een meervoudige selector.

### <a name="single-selector"></a>Single selector

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

... wordt als volgt weergegeven:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Multi-selector

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

... wordt als volgt weergegeven:

> [!div class="op_multi_selector" title1="Platform" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>Subscript en superscript

Gebruik alleen subscript of superscript als dat nodig is voor de technische nauwkeurigheid, zoals bij het schrijven van wiskundige formules. Gebruik deze niet voor niet-standaardstijlen, zoals voetnoten.

Gebruik HTML voor zowel subscript als superscript:

```html
Hello <sub>This is subscript!</sub>
```

Dit wordt weergegeven als:

Hallo <sub>Dit is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Dit wordt weergegeven als:

Tot ziens <sup>Dit is superscript!</sup>

## <a name="tables"></a>Tables

De eenvoudigste manier om een tabel in Markdown te maken is gebruik te maken van pipes en regels. Als u een standaardtabel met een kop wilt maken, laat u de eerste regel volgen door een stippellijn:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Dit wordt weergegeven als:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

U kunt de kolommen uitlijnen met behulp van dubbele punten:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Wordt weergegeven als:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> U kunt met Docs Authoring Extension voor VS Code gemakkelijk basis-Markdown-tabellen toevoegen.
>
> U kunt ook een [onlinegenerator voor tabellen](http://www.tablesgenerator.com/markdown_tables) gebruiken.

### <a name="line-breaks-within-words-in-any-table-cell"></a>Regeleinden in woorden in een tabelcel

Als u lange woorden in een Markdown-tabel gebruikt, kan de tabel worden uitgebreid naar het navigatievenster rechts, waardoor de tabel onleesbaar wordt. U kunt dit oplossen door toe te staan dat in de Docs-weergave automatisch regeleinden in woorden worden ingevoegd wanneer dit nodig is. U laat eenvoudig de tabel teruglopen met de aangepaste klasse `[!div class="mx-tdBreakAll"]`.

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
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Regeleinden in woorden in tabelcellen in de tweede kolom

Mogelijk wilt u dat regeleinden in woorden alleen automatisch in de tweede kolom van een tabel worden ingevoegd. Als u de regeleinden wilt beperken tot de tweede kolom, past u de klasse `mx-tdCol2BreakAll` toe met behulp van de `div`-wrappersyntaxis, zoals eerder besproken.

### <a name="html-tables"></a>HTML-tabellen

HTML-tabellen worden niet aanbevolen voor docs.microsoft.com. Ze kunnen niet door mensen worden gelezen in de bron. Dit is wel een basisprincipe van Markdown.
