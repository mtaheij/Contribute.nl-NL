---
title: Markdown gebruiken voor het schrijven van documenten
description: Dit artikel biedt de basis- en referentie-informatie voor de Markdown-taal die wordt gebruikt voor het schrijven van artikelen op docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111061"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Markdown gebruiken voor het schrijven van documenten

Artikelen op [docs.microsoft.com](https://docs.microsoft.com) worden geschreven in de toegankelijke opmaakcodetaal [Markdown](https://daringfireball.net/projects/markdown/), die eenvoudig te lezen en eenvoudig te leren is. Daarom is het al snel een standaardopmaaktaal geworden. De docs-site maakt gebruik van de [Markdig-variant](#markdown-flavor) van Markdown.


## <a name="markdown-basics"></a>Basisbeginselen van Markdown

### <a name="headings"></a>Koppen

Als u een kop wilt maken, gebruikt u een hash (#), als volgt:

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Headers moeten in ATX-stijl worden gemaakt, dat wil zeggen dat aan het begin van de regel 1 tot 6 hekjes (#) moeten staan om een header aan te duiden overeenkomstig de HTML-headerniveaus H1 tot H6. Hierboven vindt u voorbeelden van headers van het eerste tot vierde niveau.

Uw onderwerp **mag** maar één header van het eerste niveau (H1) bevatten. Deze wordt op de pagina weergegeven als de titel.

Als uw header met een `#` eindigt, moet u aan het eind nog een `#` toevoegen zodat de titel correct wordt weergegeven. Bijvoorbeeld `# Async Programming in F# #`.

Met de headers op het tweede niveau wordt de inhoudsopgave op de pagina gegenereerd die wordt weergegeven in de sectie 'In dit artikel' onder de titel op de pagina.

### <a name="bold-and-italic-text"></a>Vetgedrukte en cursieve tekst

Als u tekst als **vet** wilt opmaken, zet u de tekst tussen dubbele sterretjes:

```md
This text is **bold**.
```

Als u tekst als *cursief* wilt opmaken, zet u de tekst tussen enkele sterretjes:

```md
This text is *italic*.
```

Als u tekst als ***vet en cursief*** wilt opmaken, zet u de tekst tussen driedubbele sterretjes:

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Blokcitaten

Blokcitaten worden gemaakt met het teken `>`:

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Het voorbeeld hierboven wordt als volgt weergegeven:

> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.

### <a name="lists"></a>Lijsten

#### <a name="unordered-list"></a>Ongeordende lijst

Als u een ongeordende lijst of een lijst met opsommingstekens wilt opmaken, kunt u sterretjes of streepjes gebruiken. Zo wordt de volgende Markdown:

```md
- List item 1
- List item 2
- List item 3
```

weergegeven als:

- List item 1
- List item 2
- List item 3

Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen. Zo wordt de volgende Markdown:

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

weergegeven als:

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>Geordende lijst

Als u een geordende lijst/stapsgewijze lijst wilt opmaken, gebruikt u de bijbehorende nummers. Zo wordt de volgende Markdown:

```md
1. First instruction
1. Second instruction
1. Third instruction
```

weergegeven als:

1. First instruction
2. Second instruction
3. Third instruction

Als u een lijst in een andere lijst wilt nesten, laat u de lijstitems van de onderliggende lijst inspringen. Zo wordt de volgende Markdown:

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

weergegeven als:

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

Merk op dat we '1.' gebruiken voor alle vermeldingen. Hierdoor is het eenvoudiger om later verschillen te beoordelen als er in latere updates nieuwe stappen worden toegevoegd of bestaande stappen worden verwijderd.

### <a name="tables"></a>Tables

Tabellen maken geen onderdeel uit van de Markdown-kernspecificatie, maar ze worden ondersteund door GFM. Tabellen kunt u maken met het sluisteken (|) en afbreekstreepjes (-). Met afbreekstreepjes maakt u de kolomkoppen. Met het sluisteken scheidt u de kolommen van elkaar. Voeg voor de tabel een lege regel in, zodat de tabel correct wordt weergegeven.

Zo wordt de volgende Markdown:

```md
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

Ga voor meer informatie over het maken van tabellen naar:

- [Informatie ordenen met tabellen](https://help.github.com/articles/organizing-information-with-tables/) in GitHub.
- De web-app [Markdown-tabelgenerator](https://www.tablesgenerator.com/markdown_tables).
- [Referentiemateriaal voor Markdown van Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).
- [Markdown Extra van Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).
- [HTML-tabellen naar Markdown converteren](https://jmalarcon.github.io/markdowntables/).

### <a name="links"></a>Koppelingen

De Markdown-syntaxis voor een inlinekoppeling bestaat uit het gedeelte `[link text]`, het gedeelte dat wordt gekoppeld, gevolgd door het gedeelte `(file-name.md)`, de URL of de bestandsnaam waarnaar wordt gekoppeld:

 `[link text](file-name.md)`

Ga voor meer informatie over koppelen naar:

- De [Markdown-syntaxishandleiding](https://daringfireball.net/projects/markdown/syntax#link) voor informatie over basisondersteuning voor koppelen van Markdown.
- De sectie [Koppelingen](how-to-write-links.md) van deze handleiding voor meer informatie over de aanvullende syntaxis voor koppelen, zoals ondersteund door Markdig.

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

Met de alias na de eerste drie apostroffen (\`) wordt aangegeven welke syntaxismarkering moet worden gebruikt. Hieronder vindt u een lijst met veelgebruikte programmeertalen in Docs-inhoud en het bijbehorende label:

Deze talen bieden ondersteuning voor beschrijvende namen en de meeste talen hebben een functie voor taalmarkeringen.

|Naam|Markdown-label|
|-----|-------|
|.NET Console|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# in browser|csharp-interactive|
|Console|console|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Kusto-querytaal|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps (decimale punt als scheidingsteken)|powerapps-dot|
|PowerApps (decimale komma als scheidingsteken)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

De naam `csharp-interactive` geeft de taal C# aan en de mogelijkheid om de voorbeelden uit te voeren vanuit de browser. Deze codefragmenten worden gecompileerd en uitgevoerd in een Docker-container, en de resultaten van het uitvoeren van het programma worden weergegeven in het browservenster van de gebruiker.

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

## <a name="docs-custom-markdown-extensions"></a>Aangepaste Docs-extensies voor Markdown

> [!NOTE]
> Met Docs.Microsoft.com wordt een Markdig Parser for Markdown geïmplementeerd, die zeer compatibel is met GFM (GitHub Flavored Markdown). Met Markdig wordt extra functionaliteit toegevoegd via Markdown-extensies. Om die reden zijn voor naslagdoeleinden bepaalde artikelen uit de OPS-ontwerphandleiding opgenomen in deze handleiding. (Zie bijvoorbeeld Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave.)

GFM wordt gebruikt voor de opmaak van docs-artikelen, zoals alinea’s, koppelingen, lijsten en koppen. Voor rijkere opmaak kunnen in artikelen Markdig-functies worden gebruikt, zoals:

- Notitieblokken
- Bestanden opnemen
- Selectors
- Ingebedde video's
- Codefragmenten/voorbeelden

Raadpleeg Extensies voor Markdig en Markdown en Codefragmenten in de inhoudsopgave voor de volledige lijst.

### <a name="note-blocks"></a>Notitieblokken

U kunt kiezen uit vier verschillende notitieblokken om de aandacht op specifieke inhoud te vestigen:

- OPMERKING
- WAARSCHUWING
- TIP
- BELANGRIJK

Notitieblokken dienen met beleid te worden gebruikt, omdat ze als storend kunnen worden ervaren. Hoewel notitieblokken ondersteuning bieden voor codeblokken, afbeeldingen, lijsten en koppelingen, wordt het aanbevolen ze simpel te houden.

Voorbeelden:

```md
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

![laat zien hoe de waarschuwingen in het vorige voorbeeld eruit zien op de gepubliceerde Docs-pagina met verschillende pictogrammen en kleuren](media/alerts-rendering.png)

### <a name="include-files"></a>Bestanden opnemen

Als u herbruikbare tekst- of afbeeldingsbestanden hebt die moeten worden ingesloten in artikelbestanden, kunt u een verwijzing naar het in te sluiten bestand gebruiken via de Markdig-functie voor het insluiten van bestanden. Met deze functie wordt aan OPS de opdracht gegeven het betreffende bestand tijdens het opbouwen in uw artikelbestand in te sluiten, zodat dit onderdeel wordt van het gepubliceerde artikel. Er zijn drie soorten insluitingsverwijzingen beschikbaar waarmee u inhoud opnieuw kunt gebruiken:

- Inline: Een gewoon stuk tekst inline hergebruiken in een andere zin.
- Blok: Een volledig Markdown-bestand als blok hergebruiken, genest in een sectie van een artikel.
- Afbeelding: Op deze manier worden afbeeldingen standaard ingesloten in Docs.

Een inline- of blokinsluitingsbestand is niets meer of minder dan een eenvoudig Markdown-bestand (.md). Deze kunnen elke geldige Markdown bevatten. Alle ingesloten Markdown-bestanden moeten in een [algemene `/includes`-submap](git-github-fundamentals.md#includes-subdirectory) worden geplaatst in de hoofdmap van de opslagplaats. Als het artikel wordt gepubliceerd, wordt het ingesloten bestand vervolgens naadloos geïntegreerd.

Dit zijn de vereisten en overwegingen voor insluitingsbestanden:

- Gebruik een insluitingsbestand wanneer u dezelfde tekst in meerdere artikelen wilt gebruiken.
- Gebruik een blokinsluitingsverwijzing voor aanzienlijke hoeveelheden inhoud: enkele alinea's, een gedeelde procedure of een gedeelde sectie. Gebruik deze niet voor content die minder lang is dan een zin.
- Insluitingsverwijzingen worden niet weergegeven in het GitHub-weergaveoverzicht van uw artikel, omdat ze afhankelijk zijn van Markdig-extensies. Ze worden pas weergegeven na publicatie.
- Zorg ervoor dat de tekst in een insluitingsbestand uit volledige zinnen bestaat die niet afhankelijk zijn van voorafgaande of volgende tekst in het artikel waarin naar het insluitingsbestand wordt verwezen. Als u deze richtlijn negeert, ontstaat niet te vertalen tekst in het artikel waardoor de gelokaliseerde ervaring wordt onderbroken.
- Voeg geen insluitingsverwijzingen in andere insluitingsbestanden in. Dit wordt niet ondersteund.
- Plaats mediabestanden in een mediamap die specifiek is voor de submap met insluitingen, bijvoorbeeld de map `<repo>`/includes/media. In de hoofdmap van de mediamap mogen zich geen afbeeldingen bevinden. Als het insluitingsbestand geen afbeeldingen bevat, hoeft er geen bijbehorende mediamap te worden gemaakt.
- Net als bij gewone artikelen dient u geen media te delen tussen insluitingsbestanden. Gebruik een afzonderlijk bestand met een unieke naam voor elk insluitingsbestand en artikel. Sla het mediabestand op in de mediamap die is gekoppeld aan het insluitingsbestand.
- Zorg ervoor dat een artikel meer inhoud bevat dan alleen een insluitingsbestand.  Insluitingsbestanden dienen als aanvulling op de inhoud in de rest van het artikel.

Voorbeeld:

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Selectors

Gebruik selectors in technische artikelen als u van een artikel meerdere versies maakt voor implementatie in verschillende technologieën of op verschillende platformen. Dit is doorgaans het meest van toepassing voor onze inhoud voor mobiele platformen voor ontwikkelaars. Er zijn momenteel twee verschillende soorten selectors in Markdig, een enkelvoudige selector en een meervoudige selector.

Omdat dezelfde selector Markdown in elk onderwerp in de selectie wordt geplaatst, wordt aanbevolen de selector voor uw onderwerp op te nemen in een insluitingsbestand. Deze kan vervolgens naar dit insluitingsbestand verwijzen in alle artikelen waarin dezelfde selector wordt gebruikt.

Hier volgt een voorbeeld van een selector:

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

U kunt een praktijkvoorbeeld van selectors bekijken in [Azure Docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).

### <a name="code-include-references"></a>Insluitingsverwijzingen van code

Met de Markdown-extensie voor het Docs-codefragment kunt u codevoorbeelden in uw artikelen insluiten en ze weergeven in een taalspecifieke syntaxiskleur. U kunt code van de huidige opslagplaats of een andere opslagplaats insluiten. In de onderstaande instructies vindt u een overzicht van het gebruik van de functie met het [docs.microsoft.com-ontwerppakket](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack). In Visual Studio Code kunt u een voorbeeld van de codefragmenten bekijken door **Preview** te openen. Markeren en interactiviteit zijn niet beschikbaar in de preview-versie.

> [!NOTE]
> De extensie biedt geen ondersteuning voor het integraal opnemen van code-inhoud. Dit moet worden uitgevoerd door middel van de standaard Markdown-conventie, die drie keer moet worden afgevinkt.

#### <a name="code-from-current-repository"></a>Code uit huidige opslagplaats

1. Klik in Visual Studio Code op **Alt + M** of **optie + M** en selecteer Fragment.
2. Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen. Als u lokaal wilt zoeken, selecteert u Volledige lokale zoekopdracht.
3. Voer een zoekterm in om het bestand te zoeken. Wanneer u het bestand hebt gevonden, selecteert u het bestand.
4. Selecteer vervolgens een optie om te bepalen welke regel(s) code er in het fragment moeten worden opgenomen. U kunt kiezen uit de volgende opties: **Id**, **Bereik** en **Geen**.
5. Geef, op basis van uw selectie uit stap 4, indien nodig een waarde op.

Volledig codebestand weergeven:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Deel van een codebestand weergeven door regels op te geven:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Deel van een codebestand weergeven op basis van de naam van een fragment:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>Code uit een andere opslagplaats

1. Klik in Visual Studio Code op **Alt + M** of **optie + M** en selecteer Fragment.
2. Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen. Als u wilt zoeken in meerdere opslagplaatsen, selecteert u Verwijzing naar meerdere opslagplaatsen.
3. U krijgt een selectie van opslagplaatsen die zich in *.openpublishing.publish.config.json* bevinden. Selecteer een opslagplaats.
3. Voer een zoekterm in om het bestand te zoeken. Wanneer u het bestand hebt gevonden, selecteert u het bestand.
4. Selecteer vervolgens een optie om te bepalen welke regel(s) code er in het fragment moeten worden opgenomen. U kunt kiezen uit de volgende opties: **Id**, **Bereik** en **Geen**.
5. Geef, op basis van uw selectie uit stap 5, indien nodig een waarde op.

Uw fragmentverwijzing ziet er als volgt uit:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>Pad naar het codebestand

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Dit voorbeeld komt uit de ASP.NET-docs-opslagplaats, uit het artikelbestand [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Er wordt naar het codebestand verwezen met een relatief pad naar [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in dezelfde opslagplaats.

#### <a name="selected-line-numbers"></a>Bepaalde regelnummers

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

In dit voorbeeld worden alleen regels 2-24 en 26 van het code bestand *StudentController.cs* weergegeven.

U kunt beter fragmenten gebruiken dan regelnummers. We leggen hieronder uit waarom.

#### <a name="named-snippet"></a>Fragment met naam

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Gebruik alleen letters en onderstrepingstekens voor de naam.

In het voorbeeld wordt het gedeelte `snippet_Create` van het codebestand weergegeven. Het codebestand van dit voorbeeld heeft een C#-regio genaamd `snippet_Create`:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Wanneer mogelijk kunt u beter naar een gedeelte met naam verwijzen dan regelnummers op te geven. Verwijzingen naar regelnummers zijn foutgevoelig omdat codebestanden altijd veranderen, waarbij ook de regelnummers kunnen wijzigen.
U ontvangt niet per se een melding van zulke wijzigingen. In uw artikel zullen dan de verkeerde regels worden weergegeven zonder dat u weet dat er iets is veranderd.

#### <a name="highlighting-selected-lines"></a>Bepaalde regels markeren

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

In het voorbeeld zijn regel 2 en 5 gemarkeerd, waarbij wordt geteld vanaf het begin van het weergegeven fragment. (Voor het markeren van regels wordt niet geteld vanaf het begin van het codebestand.) Met andere woorden: regel 3 en 6 van het codebestand zijn gemarkeerd.

#### <a name="interactive-code-snippets"></a>Interactieve codefragmenten

U kunt de interactieve modus inschakelen voor codefragmenten die met verwijzing zijn opgenomen. Hier volgen enkele voorbeelden:

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

Als u deze functie voor een bepaald codeblok wilt inschakelen, gebruikt u het kenmerk `interactive`. De beschikbare kenmerkwaarden zijn:

- `cloudshell-powershell` - Hiermee schakelt u Azure PowerShell Cloud Shell in, zoals in het vorige voorbeeld
- `cloudshell-bash` - Schakelt de Azure Cloud Shell in
- `try-dotnet` - Hiermee schakelt u .NET proberen in
- `try-dotnet-class` - Hiermee schakelt u .NET proberen met klasse-scaffolding in
- `try-dotnet-method` - Hiermee schakelt u .NET proberen met methode-scaffolding in

Er zijn paren van `language` en `interactive` die compatibel zijn. Als `interactive` bijvoorbeeld `try-dotnet` is, moet de taal `csharp` zijn. Op dezelfde manier werkt `cloudshell-powershell` alleen met `powershell` en `cloudshell-bash` als `bash` de taal is.

Voor Azure Cloud Shell en PowerShell Cloud Shell kunnen gebruikers opdrachten uitvoeren voor enkel hun eigen Azure-account.

Met [.NET proberen](https://github.com/dotnet/try) is interactieve uitvoering van .NET-code (C#) in de browser mogelijk. Voor .NET proberen zijn er drie opties voor interactiviteit: `try-dotnet`, `try-dotnet-class` en `try-dotnet-method`. U kunt deze opties gebruiken zonder extra configuratie in het codefragment. De volgende naamruimten zijn momenteel standaard beschikbaar:

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

Met de waarde van het `try-dotnet`-kenmerk kunnen gebruikers C#-code in de browser uitvoeren zonder de code te hoeven inpakken in aangepaste code.

Voorbeeld:

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

Met behulp van de `try-dotnet-class`-waarde wordt klasse-scaffolding toegepast op de code die wordt doorgegeven aan het interactieve onderdeel.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

Voorbeeld:

Codefragment waarop geen klasse-scaffolding is toegepast

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

Codefragment waarop wel klasse-scaffolding is toegepast

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

Met behulp van de `try-dotnet-method`-waarde wordt methode-scaffolding toegepast op de code die wordt doorgegeven aan het interactieve onderdeel.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

Voorbeeld:

Codefragment waarop geen methode-scaffolding is toegepast

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

Codefragment waarop wel methode-scaffolding is toegepast

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>Naslaginformatie over fragmentsyntaxis

U kunt naar codefragmenten die in uw opslagplaats zijn opgeslagen verwijzen door de opgegeven codetaal te gebruiken. De inhoud van het opgegeven codepad wordt uitgebreid en in uw bestand opgenomen.

Er gelden geen beperkingen ten aanzien van de mappenstructuur van codefragmenten. U kunt de codefragmenten beheren als normale broncode.

Syntaxis:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Deze syntaxis is een Markdown-blokextensie. Deze moet op zijn eigen regel worden gebruikt.

- `<language>` (*optioneel*)
  - Taal van het codefragment. Zie de sectie [Ondersteunde talen](#supported-languages) verderop in dit artikel voor meer informatie.

- `<path>`(*verplichte*)
  - Relatief pad naar het bestandssysteem dat het codefragmentbestand aangeeft waarnaar moet worden verwezen.

- `<attribute>`en `<attribute-value>`(*optioneel*)
  - Worden samen gebruikt om op te geven hoe de code uit het bestand moet worden opgehaald:
    - `range`: `1,3-5` Een bereik met regels. Dit voorbeeld bevat regels 1, 3, 4 en 5.
    - `id`: `snippet_Create` De id van het fragment dat moet worden ingevoegd vanuit het codebestand. Deze waarde kan niet naast elkaar bestaan met een bereik.
    - `highlight`: `2-4,6` Het bereik en/of het aantal regels dat moet worden gemarkeerd in het gegenereerde codefragment. De nummering is relatief ten opzichte van het codefragment zelf, niet het geïmporteerde bereik.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` De waarde van de tekenreeks bepaalt welke soorten interactiviteit zijn ingeschakeld.

#### <a name="supported-languages"></a>Ondersteunde talen

|Name|Markdown-label|
|-----|-------|
|.NET Core CLI|`dotnetcli`|
|ASP.NET met C#|`aspx-csharp`|
|ASP.NET met VB|`aspx-vb`|
|Azure CLI|`azurecli`|
|Azure CLI in browser|`azurecli-interactive`|
|Azure PowerShell in browser|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|C# in browser|`csharp-interactive`|
|Console|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Kusto-querytaal|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|Power Query M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>Code-extensies

|Name|Markdown-label|Bestandsextensie|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xmal|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>Gotcha's en probleemoplossing

### <a name="alt-text"></a>Alternatieve tekst

Alternatieve tekst met onderstrepingstekens wordt niet goed weergegeven. In plaats van bijvoorbeeld dit te gebruiken:

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Typt u voor de onderstrepingstekens een escape-teken, zoals hier:

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostroffen en aanhalingstekens

Als u tekst vanuit Word in een Markdown editor kopieert, bevat deze mogelijk gekrulde apostroffen of aanhalingstekens. Deze moeten worden gecodeerd of gewijzigd in rechte apostroffen of aanhalingstekens. Anders ziet de tekst er misschien zo uit wanneer u het bestand gaat publiceren: Itâ€™s

Hieronder vindt u de codering voor de gekrulde versies van deze leestekens:

- Linker dubbel aanhalingsteken (openen): `&#8220;`
- Rechter dubbel aanhalingsteken (sluiten): `&#8221;`
- Rechter enkel aanhalingsteken of apostrof (sluiten): `&#8217;`
- Linker enkel aanhalingsteken (openen) (wordt zelden gebruikt): `&#8216;`

### <a name="angle-brackets"></a>Punthaken

Het is gebruikelijk punthaken te gebruiken om een tijdelijke aanduiding aan te geven. Als u dit in tekst doet (dus niet in code), moet u de punthaken coderen. Anders zal Markdown deze aanzien voor HTML-code.

Voorbeeld: codeer `<script name>` als `&lt;script name&gt;`

## <a name="markdown-flavor"></a>Markdown-variant

De back-end van docs.microsoft.com biedt ondersteuning voor Markdown die compatibel is met [CommonMark](https://commonmark.org/) en is geparseerd via de parseerengine [Markdig](https://github.com/lunet-io/markdig). Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt. Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.

## <a name="see-also"></a>Zie ook:

### <a name="markdown-resources"></a>Markdown-resources

- [Inleiding tot Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Referentiemateriaal voor Docs Markdown](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Basisbeginselen voor GitHubs Markdown](https://help.github.com/articles/markdown-basics/)
- [De Markdown-handleiding](https://www.markdownguide.org/)
