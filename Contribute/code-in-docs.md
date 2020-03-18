---
title: Code opnemen in docs-artikelen
description: Leer hoe u code-elementen en -fragmenten kunt opnemen in artikelen die zijn gepubliceerd op docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336473"
---
# <a name="how-to-include-code-in-docs"></a>Code opnemen in docs-artikelen

Er zijn verschillende manieren om code op te nemen in een artikel dat is gepubliceerd op docs.microsoft.com:

* Afzonderlijke elementen (woorden) binnen een regel.

  Hier volgt een voorbeeld van `code`-stijl.

  Gebruik code-indeling als u verwijst naar benoemde parameters en variabelen in een nabijgelegen codeblok in uw tekst. Code-indeling kan ook worden gebruikt voor eigenschappen, methoden, klassen en taaltrefwoorden. Zie [Code-elementen](#code-elements) verderop in dit artikel voor meer informatie.

* Codeblokken in het Markdown-bestand van het artikel.

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Gebruik codeblokken in regels wanneer het niet praktisch is om code weer te geven door verwijzing naar een codebestand. Zie [Codeblokken](#inline-code-blocks) verderop in dit artikel voor meer informatie.

* Codeblokken met verwijzing naar een codebestand in de lokale opslagplaats.

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Zie [Verwijzingen naar codefragmenten in de opslagplaats](#in-repo-snippet-references) verderop in dit artikel voor meer informatie.

* Codeblokken met verwijzing naar een codebestand in een andere opslagplaats.

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Zie [Verwijzingen naar codefragmenten buiten de opslagplaats](#out-of-repo-snippet-references) verderop in dit artikel voor meer informatie.
  
* Codeblokken waarmee de gebruiker code kan uitvoeren in de browser.

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Zie [Interactieve codefragmenten](#interactive-code-snippets) verderop in dit artikel voor meer informatie.

We leggen de Markdown uit voor elk van deze manieren op code op te nemen. Daarnaast biedt het artikel ook enkele [algemene richtlijnen voor alle codeblokken](#code-blocks).

## <a name="code-elements"></a>Code-elementen

Een code-element is een trefwoord, naam van een klasse, naam van een eigenschap, enzovoort in een programmeertaal. Het is niet altijd duidelijk wat kan worden aangeduid als 'code'. NuGet-pakketnamen moeten bijvoorbeeld worden behandeld als code. Als u twijfelt, raadpleegt u deze [richtlijnen voor het opmaken van tekst](text-formatting-guidelines.md).

### <a name="inline-code-style"></a>Codestijl in regels

Als u een code-element wilt opnemen in de tekst van een artikel, plaatst u het tussen accents graves (\`) om codestijl aan te duiden.
Voor codestijl in regels mag geen gebruik worden gemaakt van tekenreeksen met drievoudige accent graves.

|Markdown |Weergave |
|---------|---------|
|In Entity Framework worden eigenschappen met de naam \`Id\` of \`ClassnameID\` automatisch als primaire sleutel gezien.|In Entity Framework worden eigenschappen met de naam `Id` of `ClassnameID` automatisch als primaire sleutel gezien.|

Wanneer een artikel is gelokaliseerd (vertaald in andere talen), wordt tekst met codeopmaak onvertaald gelaten. Zie [Niet-gelokaliseerde tekenreeksen](markdown-reference.md#non-localized-strings) als u lokalisatie wilt voorkomen zonder codestijl te gebruiken.

### <a name="bold-style"></a>Vet

Sommige oudere stijlrichtlijnen vereisen dat u inlinecode vetgedrukt maakt. Vette tekst is een optie wanneer codestijl te opvallend is en ten koste gaat van de leesbaarheid. Een Markdown-tabel met voornamelijk code-elementen ziet er mogelijk te rommelig uit als overal de codestijl wordt gebruikt. Als u ervoor kiest om de stijl vet te gebruiken, gebruikt u [syntaxis voor niet-gelokaliseerde tekenreeksen](markdown-reference.md#non-localized-strings) zodat de code niet wordt gelokaliseerd.

### <a name="links"></a>Koppelingen

Een koppeling naar de referentiedocumentatie is mogelijk handiger dan de indeling van de code in sommige contexten. Als u een koppeling gebruikt, past u geen code-indeling toe op de tekst van de koppeling. Wanneer u codeopmaak gebruikt voor een koppeling, is het mogelijk niet meer duidelijk dat de tekst een koppeling is.

Als u een koppeling gebruikt en later in dezelfde context naar hetzelfde element verwijst, gebruikt u code-indeling voor de volgende exemplaren in plaats van koppelingen.

### <a name="placeholders"></a>Tijdelijke aanduidingen

Als u wilt dat de gebruiker een sectie met de weergegeven code vervangt door de eigen waarden, gebruikt u de tekst voor tijdelijke aanduidingen die is gemarkeerd met punthaken of accolades. Bijvoorbeeld: `az group delete -n <ResourceGroupName>`. Leg uit dat de haken of accolades moeten worden verwijderd bij het vervangen van echte waarden.

## <a name="code-blocks"></a>Codeblokken

De syntaxis voor het opnemen van code in een document is afhankelijk van waar de code zich bevindt:

* [In het Markdown-bestand van het artikel](#inline-code-blocks)
* [In een codebestand in dezelfde opslagplaats](#in-repo-snippet-references)
* [In een codebestand in een andere opslagplaats](#out-of-repo-snippet-references)

Hieronder volgen richtlijnen die van toepassing zijn op alle drie de soorten codeblokken:

* [Automatiseer codevalidatie.](#code-validation)
* [Markeer belangrijke coderegels.](#highlighting)
* [Vermijd horizontale schuifbalken.](#horizontal-scroll-bars)

### <a name="screenshots"></a>Schermopnamen

Alle methoden die in de voorgaande sectie worden vermeld, resulteren in bruikbare codeblokken:

* U kunt deze kopiëren en plakken.
* Ze worden geïndexeerd door zoekmachines.
* Ze zijn toegankelijk voor schermlezers.

Dit zijn slechts enkele redenen waarom IDE-schermopnamen niet worden aanbevolen als methode voor het opnemen van code in een artikel. Gebruik IDE-schermopnamen alleen voor code als u iets over de IDE zelf weergeeft, zoals IntelliSense. Gebruik geen schermopnamen om alleen kleuren en markering weer te geven.

### <a name="code-validation"></a>Codevalidatie

Sommige opslagplaatsen bevatten geïmplementeerde processen die automatisch alle voorbeeldcode compileren om deze te controleren op fouten. Dit is het geval in de .NET-opslagplaats. Voor meer informatie leest u [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) (Bijdragen) in de .NET-opslagplaats.

Als u codeblokken uit een andere opslagplaats gebruikt, werkt u met de eigenaren aan een onderhoudsstrategie voor de code, zodat de opgenomen code niet wordt onderbroken of verouderd raakt als nieuwe versies van de bibliotheken die de code gebruikt, worden verzonden.

### <a name="highlighting"></a>Markeren

Fragmenten bevatten doorgaans meer code dan nodig is om context te verschaffen. U kunt de leesbaarheid verbeteren door de belangrijkste regels code uit het fragment te markeren, zoals in dit voorbeeld:

![Voorbeeld van gemarkeerde code](media/code-in-docs/highlighted-code.png)

U kunt geen code markeren wanneer u de code opneemt in het Markdown-bestand van het artikel. Markering werkt alleen voor codefragmenten die zijn opgenomen door verwijzing naar een codebestand.

### <a name="horizontal-scroll-bars"></a>Horizontale schuifbalken

Splits lange regels om horizontale schuifbalken te vermijden. Door schuifbalken bij codeblokken is de code lastiger te lezen. Dit geldt vooral voor langere codeblokken, waarbij het wellicht niet mogelijk is om de schuifbalk en de regel code die u wilt lezen, tegelijkertijd te bekijken.

Splits coderegels van meer dan 85 tekens om horizontale schuifbalken in codeblokken te minimaliseren. De aanwezigheid of het ontbreken van een schuifbalk is echter niet het enige criterium voor de leesbaarheid. Als het onderbreken van een regel vóór 85 tekens de leesbaarheid of het kopiëren en plakken nadelig beïnvloedt, kunt u meer dan 85 tekens gebruiken.

## <a name="inline-code-blocks"></a>Codeblokken in regels

Gebruik codeblokken in regels alleen wanneer het niet praktisch is om code weer te geven door verwijzing naar een codebestand. Code in regels is doorgaans moeilijker om te testen en bij te houden dan een codebestand dat deel uitmaakt van een volledig project.  Bovendien kan code in regels de context weglaten aan de hand waarvan een ontwikkelaar de code kan begrijpen en gebruiken. Deze overwegingen zijn met name van toepassing op programmeertalen. Codeblokken in regels kunnen ook worden gebruikt voor uitvoer en invoer (zoals JSON), querytalen (zoals SQL) en scripttalen (zoals Power shell).
  
U kunt op twee manieren aangeven dat een tekstgedeelte in een artikel een codeblok is: door *aan beide kanten* drie accents graves (\`\`\`) te plaatsen of door inspringing van het codeblok. De eerste optie heeft de voorkeur, omdat u hiermee de taal kunt opgeven. Vermijd het gebruik van inspringing. Dit kan eenvoudig verkeerd worden geïnterpreteerd en het is moeilijk voor een andere schrijver om te begrijpen wat u bedoelde als hij uw artikel moet wijzigen.

Taalindicatoren worden direct na de eerste drie accents graves geplaatst, zoals in het volgende voorbeeld:

Markdown:

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

Weergave:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Voor meer informatie over de waarden die u kunt opgeven als taalindicatoren gaat u naar [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases) (Taalnamen en -aliassen).

Als u een taal- of omgevingswoord gebruikt na de drie accents graves (\`\`\`) dat niet wordt ondersteund, wordt dat woord weergegeven in de titelbalk van de codesectie op de weergegeven pagina. Gebruik waar mogelijk een taal- of omgevingsindicator in de codeblokken in regels.

> [!NOTE]
> Als u code kopieert en plakt vanuit een Word-document, moet u ervoor zorgen dat de code geen gekrulde aanhalingstekens bevat die niet geldig zijn in code (bijvoorbeeld `“` en `’`). Als dit het geval is, kunt u de aanhalingstekens omzetten in normale aanhalingstekens (`'` en `"`). U kunt ook gebruikmaken van het Docs Authoring Pack, [de functie voor het vervangen van gekrulde aanhalingstekens](docs-authoring/smart-quote-replacement.md).

## <a name="in-repo-snippet-references"></a>Verwijzingen naar codefragmenten in de opslagplaats

De beste manier om codefragmenten voor programmeertalen op te nemen in artikelen is met een verwijzing naar een codebestand. Hierdoor kunt u regels met code markeren en wordt de bredere context van het fragment beschikbaar op GitHub, zodat ontwikkelaars dit kunnen gebruiken. U kunt code toevoegen met behulp van de handmatige drievoudige puntnotatie (:\:\:) of in Visual Studio Code met behulp van het [docs.microsoft.com-ontwerppakket](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Klik in Visual Studio Code op <kbd>Alt + M</kbd> of <kbd>optie + M</kbd> en selecteer Fragment.
2. Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen. Als u lokaal wilt zoeken, selecteert u Volledige zoekopdracht.
3. Voer een zoekterm in om het bestand te zoeken. Wanneer u het bestand hebt gevonden, selecteert u het.
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

Deel van een codebestand weergeven door de naam van een fragment op te geven:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

In de volgende gedeelten worden deze voorbeelden uitgelegd:

* [Een relatief pad naar het codebestand gebruiken](#path-to-code-file)
* [Alleen bepaalde regelnummers opnemen](#selected-line-numbers)
* [Verwijzen naar een fragment met naam](#named-snippet)
* [Bepaalde regels markeren](#highlighting-selected-lines)

Zie [Naslaginformatie over fragmentsyntaxis](#snippet-syntax-reference) verderop in dit artikel voor meer informatie.

### <a name="path-to-code-file"></a>Pad naar het codebestand

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Dit voorbeeld komt uit de ASP.NET-docs-opslagplaats, uit het artikelbestand [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Er wordt naar het codebestand verwezen met een relatief pad naar [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in dezelfde opslagplaats.

### <a name="selected-line-numbers"></a>Bepaalde regelnummers

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

In dit voorbeeld worden alleen regels 2-24 en 26 van het codebestand *StudentController.cs* weergegeven.

U kunt beter fragmenten met een naam gebruiken dan regelnummers. We leggen hieronder uit waarom.

### <a name="named-snippet"></a>Fragment met naam

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Gebruik alleen letters en onderstrepingstekens voor de naam.

In het voorbeeld wordt het gedeelte `snippet_Create` van het codebestand weergegeven. Het codebestand voor dit voorbeeld bevat fragmenttags in opmerkingen in de C#-code:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Wanneer mogelijk kunt u beter naar een gedeelte met naam verwijzen dan regelnummers op te geven. Verwijzingen naar regelnummers zijn foutgevoelig omdat codebestanden altijd veranderen, waarbij ook de regelnummers kunnen wijzigen.
U ontvangt niet per se een melding van zulke wijzigingen. In uw artikel zullen dan de verkeerde regels worden weergegeven zonder dat u weet dat er iets is veranderd.

### <a name="highlighting-selected-lines"></a>Bepaalde regels markeren

Voorbeeld:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

In het voorbeeld zijn regel 2 en 5 gemarkeerd, waarbij wordt geteld vanaf het begin van het weergegeven fragment. Voor het markeren van regels wordt niet geteld vanaf het begin van het codebestand. Met andere woorden: regel 3 en 6 van het codebestand zijn gemarkeerd.

## <a name="out-of-repo-snippet-references"></a>Verwijzingen naar codefragmenten buiten de opslagplaats

Als het codebestand waarnaar u wilt verwijzen zich in een andere opslagplaats bevindt, moet u de codeopslagplaats instellen als een *afhankelijke opslagplaats*. In dat geval geeft u er een naam voor op. De naam fungeert vervolgens als mapnaam voor codeverwijzingen.

Neem het volgende voorbeeld: de docs-opslagplaats is *Azure/azure-docs* en de codeopslagplaats is *Azure/azure-functions-durable-extension*.

In de hoofdmap van *azure-docs* voegt u het volgende gedeelte toe in *.openpublishing.publish.config.json*:

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

Als u nu verwijst naar *samples-durable-functions* alsof deze een map is in *azure-docs*, verwijst u eigenlijk naar de hoofdmap in de opslagplaats *azure-functions-durable-extension*.

U kunt code toevoegen met behulp van de handmatige drievoudige puntnotatie (:\:\:) of in Visual Studio Code met behulp van het [docs.microsoft.com-ontwerppakket](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Klik in Visual Studio Code op <kbd>Alt + M</kbd> of <kbd>optie + M</kbd> en selecteer Fragment.
2. Wanneer het fragment is geselecteerd, wordt u gevraagd om een Volledige zoekopdracht, een Zoekopdracht met bereik of een Verwijzing naar meerdere opslagplaatsen. Als u wilt zoeken in meerdere opslagplaatsen, selecteert u Verwijzing naar meerdere opslagplaatsen.
3. U krijgt een selectie van opslagplaatsen die zich in *.openpublishing.publish.config.json* bevinden. Selecteer een opslagplaats.
4. Voer een zoekterm in om het bestand te zoeken. Wanneer u het bestand hebt gevonden, selecteert u het.
5. Selecteer vervolgens een optie om te bepalen welke regel(s) code er in het fragment moeten worden opgenomen. U kunt kiezen uit de volgende opties: **Id**, **Bereik** en **Geen**.
6. Geef op basis van uw selectie uit stap 5 een waarde op.

Uw fragmentverwijzing ziet er als volgt uit:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

In de opslagplaats *azure-functions-durable-extension* bevindt dat codebestand zich in de map *samples/csx/shared*. Zoals [eerder](#highlighting-selected-lines) opgemerkt staan regelnummers voor markeringen relatief aan het begin van het fragment in plaats van aan het begin van het bestand.

> [!NOTE]
> De naam die u toewijst aan de afhankelijke opslagplaats is relatief ten opzichte van de hoofdmap van de opslagplaats, maar de tilde (~) verwijst naar de hoofdmap van de docset. De hoofdmap van de docset wordt bepaald door `build_source_folder` in *.openpublishing.publish.config.json*. Het pad naar het fragment in het vorige voorbeeld werkt in de azure-docs repo omdat `build_source_folder` naar de repohoofdmap (`.`) verwijst. Als `build_source_folder` `articles` was, zou het pad beginnen met `~/../samples-durable-functions` in plaats van `~/samples-durable-functions`.

## <a name="interactive-code-snippets"></a>Interactieve codefragmenten

### <a name="inline-interactive-code-blocks"></a>Interactieve codeblokken in regels

U kunt codefragmenten uitvoerbaar maken in het browservenster voor de volgende talen:

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Wanneer de interactieve modus is ingeschakeld, bevatten de weergegeven codevakken de knop **Proberen** of **Uitvoeren**. Bijvoorbeeld:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

wordt weergegeven als:

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Als u deze functie voor een bepaald codeblok wilt inschakelen, gebruikt u een speciale taal-id. De beschikbare opties zijn:

* `azurepowershell-interactive` - Hiermee schakelt u Azure PowerShell Cloud Shell in, zoals in het vorige voorbeeld
* `azurecli-interactive` - Schakelt de Azure Cloud Shell in
* `csharp-interactive`-Schakelt de C# REPL in

Voor Azure Cloud Shell en PowerShell Cloud Shell kunnen gebruikers opdrachten uitvoeren voor enkel hun eigen Azure-account.

### <a name="code-snippets-included-by-reference"></a>Codefragmenten die met verwijzing zijn opgenomen

U kunt de interactieve modus inschakelen voor codefragmenten die met verwijzing zijn opgenomen. Hier volgen enkele voorbeelden:

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Als u deze functie voor een bepaald codeblok wilt inschakelen, gebruikt u het kenmerk `interactive`. De beschikbare kenmerkwaarden zijn:

* `cloudshell-powershell` - Hiermee schakelt u Azure PowerShell Cloud Shell in, zoals in het vorige voorbeeld
* `cloudshell-bash` - Schakelt de Azure Cloud Shell in
* `try-dotnet` - Hiermee schakelt u .NET proberen in
* `try-dotnet-class` - Hiermee schakelt u .NET proberen met klasse-scaffolding in
* `try-dotnet-method` - Hiermee schakelt u .NET proberen met methode-scaffolding in

Voor Azure Cloud Shell en PowerShell Cloud Shell kunnen gebruikers alleen opdrachten uitvoeren voor hun eigen Azure-account.

## <a name="snippet-syntax-reference"></a>Naslaginformatie over fragmentsyntaxis

Syntaxis:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Deze syntaxis is een Markdown-blokextensie. Deze moet op zijn eigen regel worden gebruikt.

* `<language>` (*optioneel*)
  * Taal van het codefragment. Zie de sectie [Ondersteunde talen](#supported-languages) verderop in dit artikel voor meer informatie.

* `<path>`(*verplichte*)
  * Relatief pad naar het bestandssysteem dat het codefragmentbestand aangeeft waarnaar moet worden verwezen.

* `<attribute>`en `<attribute-value>`(*optioneel*)
  * Worden samen gebruikt om op te geven hoe de code uit het bestand moet worden opgehaald en hoe deze moet worden weergegeven:
    * `range`: `1,3-5` Een bereik met regels. Dit voorbeeld bevat regels 1, 3, 4 en 5.
    * `id`: `snippet_Create` De id van het fragment dat moet worden ingevoegd vanuit het codebestand. Deze waarde kan niet naast elkaar bestaan met een bereik.
    * `highlight`: `2-4,6` Het bereik en/of het aantal regels dat moet worden gemarkeerd in het gegenereerde codefragment. De nummering is relatief ten opzichte van de weergegeven regels (zoals opgegeven met een bereik of id), niet voor het bestand.
    * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` De waarde van de tekenreeks bepaalt welke soorten interactiviteit zijn ingeschakeld.
    * Zie de [DocFX-richtlijnen](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file) voor details over weergave van tagnamen in bronbestanden van codefragmenten per taal.

## <a name="supported-languages"></a>Ondersteunde talen

Het [Docs Authoring Pack ](how-to-write-docs-auth-pack.md) bevat een functie voor het voltooien van instructies en validatie van de beschikbare taal-id's voor omheinde codeblokken.

### <a name="fenced-code-blocks"></a>Omheinde codeblokken

| Name                           | Geldige aliassen                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Toegangslogboeken                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| ARM assembler                  | `armasm`, `arm`                                                                |
| AVR assembler                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| DNS Zone file                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (Device Tree)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handgrepen                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| Managed Object Format          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Plaintext no highlight         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Eigenschappen                     | `properties`                                                                   |
| Protocol Buffers               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python profiler results        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM spec files                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Shell                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Structured Text                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> Het Docs Authoring Pack, [de functie Dev Lang Completion](docs-authoring/dev-lang-completion.md) gebruikt de eerste geldige alias als er meerdere aliassen beschikbaar zijn.

## <a name="next-steps"></a>Volgende stappen

Zie [Richtlijnen voor het opmaken van tekst](text-formatting-guidelines.md)voor meer informatie over de tekstopmaak voor andere inhoudstypen dan code.
