---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Markdown gebruiken voor het schrijven van documenten

Artikelen op docs.microsoft.com worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is. Daarom is het al snel een standaardopmaaktaal geworden.

Omdat Docs-inhoud wordt opgeslagen in GitHub, kan een hoofdverzameling van Markdown, [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), worden gebruikt. Deze biedt aanvullende functionaliteit voor algemene opmaakbehoeften. Daarnaast wordt met OPS (Open Publishing Services) DFM (DocFX Flavored Markdown) geïmplementeerd, dat zeer compatibel is met GitHub Flavored Markdown (GFM). Hiermee wordt aanvullende functionaliteit toegevoegd om voor Docs specifieke functies in te schakelen.

## <a name="markdown-basics"></a>Basisbeginselen van Markdown

### <a name="headings"></a>Koppen

Als u een kop wilt maken, gebruikt u een hash (#), als volgt:

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>Vetgedrukte en cursieve tekst

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
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>Lijsten

#### <a name="unordered-list"></a>Ongeordende lijst

Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken. Zo wordt de volgende Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

weergegeven als:

- Lijstitem 1
- Lijstitem 2
- Lijstitem 3

Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen. Zo wordt de volgende Markdown:

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

weergegeven als:

- Lijstitem 1
  - Lijstitem A
  - Lijstitem B
- Lijstitem 2

#### <a name="ordered-list"></a>Geordende lijst

Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers. Zo wordt de volgende Markdown:

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

weergegeven als:

1. Eerste instructie
2. Tweede instructie
3. Derde instructie

Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen. Zo wordt de volgende Markdown:

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

weergegeven als:

1. Eerste instructie
    1. Subinstructie
    2. Subinstructie
2. Tweede instructie

### <a name="tables"></a>Tabellen

Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM. Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-). Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar. Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.

Zo wordt de volgende Markdown:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

weergegeven als:

| Pret                  | met                 | Tabellen          |
| :------------------- | -------------------: |:---------------:|
| links uitgelijnde kolom  | rechts uitgelijnde kolom | gecentreerde kolom |
| USD 100                 | USD 100                 | USD 100            |
| USD 10                  | USD 10                  | USD 10             |
| USD 1                   | USD 1                   | USD 1              |

Ga voor meer informatie over het maken van tabellen naar:

- De [functie voor tabelterugloop](#table-wrapping) van DFM biedt ondersteuning bij het opmaken van brede tabellen
- [Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub
- De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables)
- [Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table)
- [HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>Koppelingen

De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:

 `[link text](file-name.md)`

Ga voor meer informatie over koppelen naar:

- De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.
- De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over aanvullende syntaxis voor koppelen, zoals ondersteund door DFM.

### <a name="code-snippets"></a>Codefragmenten

Markdown ondersteunt het plaatsen van codefragmenten inline in een zin, maar ook als een afzonderlijk, 'omheind' blok tussen zinnen. Zie voor meer informatie:

- [Eigen systeemondersteuning van Markdown voor codeblokken](https://daringfireball.net/projects/markdown/syntax#precode)
- [GFM-ondersteuning voor codeomheining en syntaxismarkering](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Met omheinde codeblokken kunt u eenvoudig syntaxis markeren voor uw codefragmenten. De algemene opmaak voor omheinde codeblokken is:

    ```alias
    ...
    your code goes in here
    ...
    ```

Met de alias na de eerste drie apostroffen (`) wordt aangegeven welke syntaxismarkering moet worden gebruikt. Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:

Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.

|Naam|Markdown-label|
|-----|-------|
|.NET Console|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>Voorbeeld: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Weergave__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Voorbeeld: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Weergave__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>Aangepaste OPS-extensies voor Markdown

> [!NOTE]
> Met OPS (Open Publishing Services) wordt DFM (DocFX Flavored Markdown) geïmplementeerd, dat zeer compatibel is met GFM (GitHub Flavored Markdown). Met DFM wordt extra functionaliteit toegevoegd via Markdown-extensies. Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding. (Zie bijvoorbeeld Extensies voor DFM en Markdown en Codefragmenten in de inhoudsopgave.)

GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen. Voor rijkere opmaak kunnen in artikelen DFM-functies worden gebruikt, zoals:

- Notitieblokken
- Omvat
- Selectors
- Ingebedde video's
- Codefragmenten/voorbeelden

Raadpleeg Extensies voor DFM en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.

### <a name="note-blocks"></a>Notitieblokken

U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:

- OPMERKING
- WAARSCHUWING
- TIP
- BELANGRIJK

Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren. Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.

### <a name="includes"></a>Omvat

Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de DFM-functie voor het insluiten van bestanden. Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel. Er zijn drie soorten insluitingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:

- Inline: een gewoon stuk tekst inline hergebruiken in een andere zin.
- Blok: een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.
- Afbeelding: op deze manier worden afbeeldingen standaard ingesloten in Docs.

Een inline- of blokinsluiting is niets meer of minder dan een eenvoudig Markdown-bestand (.md). Deze kunnen elke geldige Markdown bevatten. Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats. Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.

Dit zijn de vereisten en overwegingen voor insluitingen:

- Gebruik insluitingen wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.
- Gebruik blokinsluitingen voor aanzienlijke hoeveelheden inhoud: enkele alinea’s, een gedeelde procedure of een gedeelde sectie. Gebruik deze niet voor content die minder lang is dan een zin.
- Insluitingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikelen, omdat ze afhankelijk zijn van DFM-extensies. Ze worden pas weergegeven na publicatie.
- Zorg ervoor dat de tekst in een insluiting uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar de insluiting wordt verwezen. Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.
- Voeg geen insluitingen in andere insluitingen in. Dit wordt niet ondersteund.
- Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media. In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden. Als de insluiting geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.
- Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden. Gebruik een afzonderlijk bestand met een unieke naam voor elke insluiting en elk artikel. Sla het mediabestand op in de mediamap die is gekoppeld aan de insluiting.
- Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluiting.  Insluitingen dienen als aanvulling op de inhoud in de rest van het artikel.

### <a name="selectors"></a>Selectors

Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of platformen. Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars. Er zijn momenteel twee verschillende soorten selectors in DFM, een enkelvoudige selector en een meervoudige selector.

Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluiting. Deze kan vervolgens naar deze insluiting verwijzen in alle onderwerpen waarin dezelfde selector wordt gebruikt.

### <a name="code-snippets"></a>Codefragmenten

DFM ondersteunt geavanceerde insluiting van code in een artikel, via de extensie voor codefragmenten. Dit biedt een geavanceerde weergave die gebruikmaakt van GFM-functies, zoals keuze van programmeertaal en syntaxiskleuren, plus leuke functies als:

- Insluiting van gecentraliseerde codevoorbeelden/-fragmenten uit een externe opslagplaats.
- Gebruikersinterface met tabbladen voor weergave van meerdere versies van codevoorbeelden in verschillende talen.

## <a name="gotchas-and-troubleshooting"></a>Gotcha's en probleemoplossing

### <a name="alt-text"></a>Alternatieve tekst

Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven. In plaats van bijvoorbeeld dit te gebruiken:

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Typt u voor de onderstrepingstekens een escape-teken, zoals hier:

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostroffen en aanhalingstekens

Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens. Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens. Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s

Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:

- Linker dubbel aanhalingsteken (openen): `&#8220;`
- Rechter dubbel aanhalingsteken (sluiten): `&#8221;`
- Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`
- Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`

### <a name="angle-brackets"></a>Punthaken

Als u in lopende tekst (geen code) punthaken gebruikt, bijvoorbeeld om een tijdelijke aanduiding aan te geven, moet u de punthaken handmatig coderen. Anders zal Markdown deze aanzien voor HTML-code.

Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`

## <a name="see-also"></a>Zie ook

### <a name="markdown-resources"></a>Markdown-resources

- [Inleiding tot Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Referentiemateriaal voor Docs Markdown](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Basisbeginselen voor GitHubs Markdown](https://help.github.com/articles/markdown-basics/)
