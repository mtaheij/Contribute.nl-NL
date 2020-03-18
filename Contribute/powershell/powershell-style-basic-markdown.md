---
title: Sjabloon en spiekbrief voor PowerShell-artikelen
description: Dit artikel bevat een handige sjabloon waarmee u nieuwe artikelen kunt maken voor PowerShell-documenten
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331924"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>Markdown-stijlgids voor PowerShell-Docs

Dit artikel bevat wat specifieke stijlrichtlijnen voor de PowerShell-Docs-inhoud.

Raadpleeg de [stijlgids van Microsoft](https://docs.microsoft.com/style-guide/welcome/) voor hulp bij andere schrijfstijlen.

## <a name="metadata"></a>Metagegevens

Deze sjabloon bevat voorbeelden van Markdown-syntaxis, maar ook aanwijzingen voor het instellen van metagegevens.
Wanneer u een Markdown-bestand maakt, dient u de opgenomen sjabloon naar een nieuw bestand te kopiëren, de metagegevens in te vullen zoals hierna is aangegeven en de kop H1 boven de titel van het artikel te zetten.

Het vereiste blok met metagegevens bevindt zich in het volgende voorbeeldblok met metagegevens:

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Tussen de dubbele punt (:) en de waarde van een metagegevenselement **moet** een spatie staan.
- Dubbele punten in een waarde (zoals een titel) verbreken de metagegevensparser. Omring in dit geval de titel met dubbele aanhalingstekens (bijvoorbeeld `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **auteur**: Het veld Auteur moet de **GitHub-gebruikersnaam** van de auteur bevatten.
- **beschrijving**: Hierin wordt de inhoud van het artikel samengevat. Deze wordt meestal in de pagina met zoekresultaten weergegeven, maar wordt niet gebruikt voor de rangschikking van de zoekresultaten. De lengte dient 115 tot 145 tekens te bedragen, inclusief spaties.
- **ms.date**: De datum van de laatste belangrijke update. Werk deze bij voor bestaande artikelen als u het gehele artikel hebt bekeken en bijgewerkt. Kleine aanpassingen, zoals typfouten, rechtvaardigen geen update.
- **titel**: Deze wordt in zoekprogrammaresultaten weergegeven. De titel mag niet identiek zijn aan de titel in uw H1-kop en moet maximaal 60 tekens bevatten.

Er zijn andere metagegevens aan elk artikel toegevoegd, maar wij passen gewoonlijk de meeste metagegevenswaarden toe op mapniveau, zoals is opgegeven in **docfx.json**.

## <a name="product-terminology"></a>Productterminologie

Er zijn verschillende varianten van PowerShell. Deze tabel bevat een definitie van verschillende termen die worden gebruikt om PowerShell te bespreken.

- **PowerShell**: Dit is de standaard. PowerShell is het product dat wij aanbieden. De term PowerShell kan worden gebruikt om welke editie van het product dan ook te beschrijven.
- **PowerShell Core**: PowerShell op basis van .NET Core Common Language Runtime (CoreCLR) voor alle ondersteunde platforms.
- **Windows PowerShell**: PowerShell op basis van .NET Framework Common Language Runtime (CLR). Windows PowerShell is alleen beschikbaar op Windows. Hiervoor is de volledige CLR van het .NET Framework vereist.

Over het algemeen kunnen verwijzingen naar ‘Windows PowerShell’ in documentatie worden vervangen door ‘PowerShell’.
‘Windows PowerShell’ moet **niet** worden gewijzigd als specifieke technologie voor Windows wordt besproken.

## <a name="basic-markdown-gfm-and-special-characters"></a>Elementaire Markdown, GFM en speciale tekens

U kunt de basisbeginselen van Markdown, GitHub Flavored Markdown (GFM) en OPS-specifieke extensies leren in het artikel [Markdown-naslaginformatie](../markdown-reference.md).

Markdown maakt gebruik van speciale tekens, zoals \*, \` en \# voor opmaak. Als u een van deze tekens in uw inhoud wilt opnemen, moet u een van de volgende stappen ondernemen:

- Plaats een backslash vóór een speciaal teken om deze als escape-teken te gebruiken (bijvoorbeeld `\*` vóór een \*)
- Gebruik de [HTML-entiteitscode](http://www.ascii.cl/htmlcodes.htm) voor het teken (bijvoorbeeld `&#42;` vóór een &#42;).
- Markdown-bestanden moeten onbewerkte ASCII-tekst of UTF-8-codering bevatten. Vermijd echter het gebruik van UTF-8-tekens met meerdere bytes. Gebruik in plaats daarvan een HTML-entiteit. Gebruik voor de auteursrechtsymbolen bijvoorbeeld `&copy;`.
  Deze wordt weergegeven als &copy;.

## <a name="hyperlinks"></a>Hyperlinks

- Vermijd het gebruik van pure URL’s. Voor koppelingen moet Markdown-syntaxis `[friendlyname](url-or-path)` worden gebruikt
- Koppelingen moeten een beschrijvende naam hebben, meestal de titel van het onderwerp waarnaar wordt verwezen
- Alle items in de sectie Verwante koppelingen onderaan moeten een hyperlink bevatten.
- Gebruik relatieve koppelingen als u verwijst naar andere inhoud die wordt gehost op **docs.microsoft.com**.
- Gebruik geen accents graves, vetgedrukte tekst of andere opmaak binnen de haakjes van een hyperlink.

Raadpleeg [Koppelingen in documentatie gebruiken](../how-to-write-links.md) voor uitgebreide informatie over het gebruik van koppelingen.

## <a name="filenames"></a>Bestandsnamen

Voor bestandsnamen zijn de volgende regels van toepassing:

- Bevatten alleen letters, cijfers en afbreekstreepjes.
- Deze bevatten geen spaties of leestekens. Deze maken gebruik van afbreekstreepjes als scheidingsteken tussen woorden en getallen in de bestandsnaam.
- Gebruik specifieke actieve werkwoorden, zoals ontwikkelen, kopen, maken, problemen oplossen. Geen onvoltooid tegenwoordige tijd.
- Geen kleine woorden: gebruik niet 'een', 'en', 'de', 'in', 'of', 'enz.'
- De indeling moet Markdown zijn en de bestandsextensie .md.
- Houd de bestandsnamen redelijk kort. Deze maken deel uit van de URL voor uw artikelen.

## <a name="blank-lines-spaces-and-tabs"></a>Witregels, spaties en tabs

Verwijder dubbele witregels. Meerdere witregels worden in HTML als één witregel weergeven. Meerdere witregels gebruiken heeft dus geen zin.

Witregels geven ook het einde van een blok aan in Markdown. Er moet één witregel tussen verschillende typen Markdown-blokken zijn (zoals tussen een alinea en een lijst of koptekst).

> [!NOTE]
> Spatiegebruik is erg belangrijk in Markdown. Gebruik altijd spaties in plaats van harde tabs. Verwijder extra spaties aan het einde van regels.

## <a name="titles-and-headings"></a>Titels en koppen

Gebruik alleen [ATX-kopteksten][atx] (kopteksten in #-stijl in plaats van `=`- of `-`-stijl).

- Gebruik alleen zinnen - alleen eigennamen en de eerste letter van een titel of koptekst moet een hoofdletter krijgen
- Er moet één spatie zijn tussen de `#` en de eerste letter van de koptekst
- Kopteksten moeten worden omgeven door één lege regel
- Slechts één H1 per document
- Koptekstniveaus moeten met één worden verhoogd - sla geen niveaus over
- Gebruik geen accents graves, vetgedrukte tekst of andere opmaak in kopteksten

> [!CAUTION]
> Voor het schema dat door [PlatyPS][platyPS] wordt afgedwongen voor cmdlet-verwijzingen zijn specifieke H2- en H3-koppen vereist. Het toevoegen of verwijderen van kopteksten kan problemen opleveren in de build. Raadpleeg de [stijlgids voor cmdlet-verwijzingen](powershell-style-reference.md) voor meer informatie.

## <a name="limit-line-length-to-100-characters"></a>Beperk de lengte van regels tot 100 tekens

Dit vereenvoudigt de opdrachtregeluitvoer voor verschillen en geschiedenis.

Deze regel is niet van toepassing op een groot deel van de bestaande inhoud in PowerShell-Docs, maar zal in de loop van de tijd worden gebruikt. Lever gerust een bijdrage. Met de [reflow-uitbreiding][reflow] in Visual Studio Code (VSCode) kunt u alinea's eenvoudig opnieuw opmaken overeenkomstig deze beperking.

## <a name="lists"></a>Lijsten

Als uw lijst meerdere zinnen of alinea’s bevat, kunt u overwegen een koptekst op subniveau te gebruiken in plaats van een lijst.

Lijsten moeten worden omgeven door één lege regel.

### <a name="unordered-lists"></a>Niet-geordende lijsten

Beëindig lijstitems niet met een punt, tenzij ze meerdere zinnen bevatten. Gebruik het afbreekstreepje (`-`) als opsommingsteken voor een lijstitem. Dit voorkomt verwarring met vette of cursieve markeringen, waarbij het sterretje [`*`] wordt gebruikt. Voeg een regel toe en lijn de inspringing uit met het eerste teken achter het opsommingsteken om een alinea of andere elementen onder een opsomming op te nemen.

Bijvoorbeeld:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

Dit is een lijst met subelementen onder een opsommingsteken.

- Item van eerste opsomming

  Zin met uitleg voor de eerste opsomming.

  - Item van subopsommingsteken

    Zin met uitleg voor de subopsomming.

- Item van tweede opsomming
- Item van derde opsomming

### <a name="ordered-lists"></a>Geordende lijsten

Lijn de inspringing uit met het eerste teken achter het itemnummer om een alinea of andere elementen onder een genummerd item op te nemen.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

om deze uitvoer te krijgen:

> 1. Plaats bij het eerste element een spatie achter de 1. Lange zinnen moeten passend worden gemaakt op de volgende regel en worden uitgelijnd met het eerste teken na de markering van de genummerde lijst.
>
>    U kunt een tweede element (zoals dit) opnemen door een nieuwe regel na de eerste in te voegen en de inspringing uit te lijnen. De inspringing van het tweede element moet worden uitgelijnd met het eerste teken na de markering van de genummerde lijst. Voor items met één cijfer, zoals dit, springt u in naar kolom 4. Voor items met dubbele cijfers, zoals nummer 10, springt u in naar kolom 5.
>
> 1. Het volgende genummerde item begint hier.

Alle items in de genummerde lijst moeten het nummer `1.` gebruiken in plaats van een interval voor elk item.
Bij het weergeven van de Markdown wordt de waarde automatisch verhoogd. Hierdoor kunnen items gemakkelijker in een andere volgorde worden geplaatst en wordt de inspringing van onderliggende inhoud gestandaardiseerd.

## <a name="formatting-command-syntax-elements"></a>Syntaxiselementen van opdrachten opmaken

- Namen van PowerShell-cmdlets hebben [Pascal-hoofdletters][pascal-case]. Werkwoorden zijn van zelfstandige naamwoorden gescheiden door middel van een koppelteken. Gebruik altijd de volledige Pascal Case-naam voor cmdlets en parameters. Vermijd het gebruik van aliassen tenzij u specifiek over een alias spreekt.

- Binnen een alinea moeten taaltrefwoorden, cmdlet-namen en verwijzingen naar variabelen tussen accents graves (`` ` ``) worden geplaatst. Namen van eigenschappen, parameters en klassen moeten **vet** zijn.

  Bijvoorbeeld:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- Wanneer naar een parameter wordt verwezen aan de hand van de naam, moet de naam **vet** zijn. Wanneer het gebruik van een parameter met een afbreekstreepje als voorvoegsel wordt gedemonstreerd, moet de parameter tussen accents graves worden geplaatst. Bijvoorbeeld:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- Wanneer naar externe opdrachten (EXE-bestanden, scripts, enzovoort) wordt verwezen, moet de naam van de opdracht vet zijn, alleen kleine letters bevatten (of hoofdletters als deze aan het begin van een zin staat) en de juiste bestandsextensie bevatten. Bijvoorbeeld:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- Wanneer een voorbeeld van het gebruik van een externe opdracht wordt gebruikt, moet het voorbeeld tussen accents graves zijn geplaatst.
  Als er een naamconflict met een alias is, moet u de bestandsextensie in het voorbeeld van de opdracht opnemen. Bijvoorbeeld:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- Als u een conceptueel artikel (in tegenstelling tot referentie-inhoud) schrijft, moet de eerste instantie van een cmdlet-naam een hyperlink naar de cmdlet-documentatie bevatten. Gebruik geen accents graves, vetgedrukte tekst of andere opmaak binnen de haakjes van een hyperlink.

  Bijvoorbeeld:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  Raadpleeg het gedeelte [Hyperlinks](#hyperlinks) in de stijlgids voor meer informatie.

## <a name="images"></a>Afbeeldingen

De syntaxis voor het insluiten van een afbeelding is:

```Syntax
![[alt text]](<folderPath>)
```

Voorbeeld:

```markdown
![Introduction](./media/overview/Introduction.png)
```

Hierbij is `alt text` een korte beschrijving van de afbeelding en `<folder path>` een relatief pad naar de afbeelding. Voor schermlezers voor visueel gehandicapten is alternatieve tekst nodig. Dit is ook handig wanneer de afbeelding niet kan worden weergegeven door een sitebug.

Afbeeldingen moeten worden opgeslagen in een `media/<article-name>`-map in de map die uw artikel bevat. Afbeeldingen moeten niet worden gedeeld tussen artikelen. Maak onder de map `media` een map die overeenkomt met de bestandsnaam van uw artikel. Kopieer de afbeeldingen voor dat artikel naar de nieuwe map. Als een afbeelding door meerdere artikelen wordt gebruikt, moet elke afbeeldingsmap een kopie van het afbeeldingsbestand bevatten. Dit voorkomt dat een wijziging voor een afbeelding in het ene artikel gevolgen heeft voor het andere artikelen.

In sommige gevallen wilt u mogelijk afbeeldingen, zoals logo’s en pictogrammen, delen in meerdere artikelen. Deze afbeeldingen worden in de map `/media/shared` in de hoofdmap van de opslagplaats opgeslagen.

De volgende soorten afbeeldingsbestanden worden ondersteund: *.png", *.gif", *.jpeg", *.jpg", *.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
