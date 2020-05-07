---
title: Sjabloon en cheatsheet voor .NET-artikelen
description: Dit artikel bevat een handige sjabloon waarmee u nieuwe artikelen kunt maken voor opslagplaatsen voor .NET-documenten
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: a520112cd77f4c4807e7719c2c4dbd43a762f062
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "80759542"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>Sjabloon voor metagegevens en Markdown voor .NET-documenten

Deze dotnet/docs-sjabloon bevat voorbeelden van Markdown-syntaxis, maar ook aanwijzingen voor het instellen van metagegevens.

Wanneer u een Markdown-bestand maakt, dient u de opgenomen sjabloon naar een nieuw bestand te kopiëren, de metagegevens in te vullen zoals hierna is aangegeven en de kop H1 boven de titel van het artikel te zetten.

## <a name="metadata"></a>Metagegevens

Het vereiste blok met metagegevens bevindt zich in het volgende voorbeeldblok met metagegevens:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Tussen de dubbele punt (:) en de waarde van een metagegevenselement **moet** een spatie staan.
- Dubbele punten in een waarde (zoals een titel) verbreken de metagegevensparser. Omring in dit geval de titel met dubbele aanhalingstekens (bijvoorbeeld `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **titel**: Deze wordt in zoekprogrammaresultaten weergegeven. De titel mag niet identiek zijn aan de titel in uw kop H1 en moet maximaal 60 tekens bevatten.
- **beschrijving**: Hierin wordt de inhoud van het artikel samengevat. Deze wordt meestal in de pagina met zoekresultaten weergegeven, maar wordt niet gebruikt voor de rangschikking van de zoekresultaten. De lengte dient 115 tot 145 tekens te bedragen, inclusief spaties.
- **auteur**: Het veld Auteur moet de **GitHub-gebruikersnaam** van de auteur bevatten.
- **ms.date**: De datum van de laatste belangrijke update. Werk deze bij voor bestaande artikelen als u het gehele artikel hebt bekeken en bijgewerkt. Kleine aanpassingen, zoals typfouten e.d., rechtvaardigen geen update.

Er zijn andere metagegevens aan elk artikel toegevoegd, maar wij passen gewoonlijk de meeste metagegevenswaarden toe op mapniveau, zoals is opgegeven in **docfx.json**.

## <a name="basic-markdown-gfm-and-special-characters"></a>Elementaire Markdown, GFM en speciale tekens

U kunt de basisbeginselen van Markdown, GitHub Flavored Markdown (GFM) en OPS-specifieke extensies leren in het artikel [Markdown-naslaginformatie](../markdown-reference.md).

Markdown maakt gebruik van speciale tekens, zoals \*, \` en \# voor opmaak. Als u een van deze tekens in uw inhoud wilt opnemen, moet u een van de volgende stappen ondernemen:

- Plaats een backslash vóór een speciaal teken om deze als escape-teken te gebruiken (bijvoorbeeld `\*` vóór een \*)
- Gebruik de [HTML-entiteitscode](http://www.ascii.cl/htmlcodes.htm) voor het teken (bijvoorbeeld `&#42;` vóór een &#42;).

## <a name="file-names"></a>Bestandsnamen

Voor bestandsnamen zijn de volgende regels van toepassing:

* Deze bevatten alleen kleine letters, cijfers en afbreekstreepjes.
* Deze bevatten geen spaties of leestekens. Deze maken gebruik van afbreekstreepjes als scheidingsteken tussen woorden en getallen in de bestandsnaam.
* Gebruik specifieke actieve werkwoorden, zoals ontwikkelen, kopen, maken, problemen oplossen. Geen onvoltooid tegenwoordige tijd.
* Geen kleine woorden: gebruik niet 'een', 'en', 'de', 'in', 'of', 'enz.'
* De indeling moet Markdown zijn en de bestandsextensie .md.
* Houd de bestandsnamen redelijk kort. Deze maken deel uit van de URL voor uw artikelen.

## <a name="headings"></a>Koppen

Gebruik zinnen met hoofdletters. Begin het eerste woord van een koptekst altijd met een hoofdletter.

## <a name="text-styling"></a>Tekststijl

*Cursief* Gebruik deze stijl voor bestanden, mappen, paden (voor lange items, op hun eigen regel gesplitst), nieuwe termen.

**Vet** Gebruik deze stijl voor elementen in de gebruikersinterface.

`Code` U kunt deze gebruiken voor inline-code, sleutelwoorden voor de taal, NuGet-pakketnamen, opdrachten in opdrachtregels, databasetabel- en kolomnamen en URL's waarvan u niet wilt dat erop geklikt kan worden.

## <a name="links"></a>Koppelingen

Raadpleeg het algemene artikel over [Koppelingen](../how-to-write-links.md) voor informatie over ankers, interne koppelingen, koppelingen naar andere documenten, insluiting van code en externe koppelingen.

Het .NET-documententeam maakt gebruik van de volgende conventies:

- In de meeste gevallen gebruiken we de relatieve koppelingen en ontmoedigen het gebruik van `~/` in koppelingen, omdat relatieve koppelingen worden opgehaald in de bron op GitHub. Steeds wanneer wij echter een koppeling maken naar een bestand in een afhankelijke opslagplaats, gebruiken wij het `~/`-teken om het pad op te geven. Aangezien de bestanden in de afhankelijke opslagplaats zich op een andere locatie bevinden in GitHub, worden de koppelingen niet correct opgehaald met relatieve koppelingen, ongeacht de wijze waarop deze zijn geschreven.
- De specificaties voor de computertaal C# en taal de Visual Basic zijn in de .NET-documenten opgenomen door de bron in te voegen vanuit de taalopslagplaatsen. De Markdown-bronnen worden beheerd in de opslagplaatsen [csharplang](https://github.com/dotnet/csharplang) en [vblang](https://github.com/dotnet/vblang).

Koppelingen naar specificaties moeten verwijzen naar de bronmappen waarin die specificaties zijn opgenomen. Voor C# is dit **~/_csharplang/spec** en voor Visual Basic is dit **~/_vblang/spec**, zoals in het volgende voorbeeld:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>Koppelingen naar API's

Het build-systeem bevat enkele extensies waarmee we koppelingen kunnen maken met .NET-API's zonder externe koppelingen te hoeven gebruiken. U gebruikt een van de volgende typen syntaxis:

1. Automatisch koppelen: `<xref:UID>` of `<xref:UID?displayProperty=nameWithType>`

   De queryparameter `displayProperty` produceert een volledig gekwalificeerde koppelingstekst. Standaard toont de koppelingstekst alleen de naam van het lid of het type.

2. Markdown-koppeling: `[link text](xref:UID)`

   Gebruik deze als u de weergegeven koppelingstekst wilt aanpassen.

Voorbeelden:

- `<xref:System.String>` weergeven als [String](https://docs.microsoft.com/dotnet/api/system.string)
- `<xref:System.String?displayProperty=nameWithType>` weergeven als [System.String](https://docs.microsoft.com/dotnet/api/system.string)
- `[String class](xref:System.String)` weergeven als [String class](https://docs.microsoft.com/dotnet/api/system.string)

Bekijk [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Kruisverwijzing gebruiken) voor meer informatie over het gebruik van deze notatie.

Bepaalde UID's bevatten de speciale tekens \`, \# of \*,waardoor de waarde van de UID respectievelijk als `%60`, `%23` en `%2A` met HTML moet worden gecodeerd. U ziet soms haakjes in de code, maar dat is geen vereiste.

Voorbeelden:

- System.Threading.Tasks.Task\`1 wordt `System.Threading.Tasks.Task%601`
- System.Exception. \#ctor wordt `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wordt `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

U kunt de UID's opzoeken van typen, evenals een lijst van overbelaste leden of een bepaald overbelast lid vanuit `https://xref.docs.microsoft.com/autocomplete`. Via de querytekenreeks `?text=*\<type-member-name>*` wordt het type of lid geïdentificeerd waarvan of van wie de UID's zijn die u wilt zien. Met `https://xref.docs.microsoft.com/autocomplete?text=string.format` worden bijvoorbeeld de overbelastingen ten aanzien van [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) opgehaald. Met het hulpprogramma zoekt u naar de opgegeven queryparameter `text` ergens in de UID. U kunt bijvoorbeeld zoeken naar de naam van het lid (ToString), een gedeelte daarvan (ToStri), de naam van het type en lid (Double.ToString) enz.

Als u een \* (of `%2A`) toevoegt na de UID, geeft de koppeling de overbelastingspagina aan en niet een specifieke API. U kunt dat bijvoorbeeld gebruiken wanneer u op een generieke manier wilt koppelen aan de pagina [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) in plaats van specifieke overbelasting zoals [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_). U kunt tevens met \* een koppeling maken met een lidpagina wanneer het lid niet overbelast is; zo hoeft u geen parameterlijst in de UID op te nemen.

Als u een koppeling wilt maken met een overbelasting van een specifieke methode, moet u de volledig gekwalificeerde typenaam van alle parameters van de methode opnemen. Zo bevat \<xref:System.DateTime.ToString> een koppeling naar de parameterloze methode [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) terwijl \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> een koppeling bevat naar de methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).

Als u een koppeling wilt maken naar een algemeen type, zoals [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), moet u het teken \` (`%60`) gebruiken, gevolgd door het aantal algemene parametertypen. Zo bevat `<xref:System.Nullable%601>` een koppeling met het type [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), terwijl `<xref:System.Func%602>` een koppeling bevat met de gemachtigde [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).

## <a name="code"></a>Code

De beste manier om code in te voegen is fragmenten van een werkend voorbeeld in te voegen. Maak uw voorbeeld op basis van de instructies in het artikel [Bijdragen aan .NET](dotnet-contribute.md#contributing-to-samples). De basisregels voor het invoegen van code bevinden zich in de algemene richtlijnen voor [code](../code-in-docs.md).

U kunt de code invoegen met behulp van de volgende syntaxis:

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (*optioneel*, maar *wel aanbevolen*)
  * Taal van het codefragment waarnaar wordt verwezen.

* `<name>`( *optioneel*)
  * Naam van het codefragment. Deze heeft geen invloed op het HTML-resultaat, maar u kunt deze gebruiken om de leesbaarheid van uw Markdown-bron te verbeteren.

* `<pathToFile>`(*verplichte*)
  * Relatief pad naar het bestandssysteem dat het codefragmentbestand aangeeft waarnaar moet worden verwezen. Dit kan ingewikkeld worden vanwege de verschillende opslagplaatsen waaruit de .NET-documentenset bestaat. De .NET-voorbeelden bevinden zich in de dotnet/voorbeelden-opslagplaats. Alle paden van fragmenten zouden beginnen met `~/samples`, waarbij de rest van het pad het pad naar de bron is vanuit de hoofdmap van die opslagplaats.

* `<queryoption>`( *optioneel*)
  * Deze worden gebruikt om op te geven hoe de code uit het bestand moet worden opgehaald:
    * `#`: `#{tagname}` (naam van de tag) *of* `#L{startlinenumber}-L{endlinenumber}` (regelbereik).
    Wij ontmoedigen het gebruik van regelnummers, omdat deze zeer foutgevoelig zijn. Het gebruik van een tagnaam geniet de voorkeur voor de verwijzing naar codefragmenten. Gebruik zinvolle tagnamen. (Veel codefragmenten zijn vanuit een eerder platform gemigreerd en de tags hebben namen zoals `Snippet1`, `Snippet2` enzovoort. Die praktijk is veel moeilijker aan te houden.)
    * `range`: `?range=1,3-5` Een bereik met regels. Dit voorbeeld bevat regels 1, 3, 4 en 5.

Wij raden aan om voor zover mogelijk de optie van tagnamen te gebruiken. De tagnaam is de naam van een regio of een commentaar bij code in de in de broncode aanwezige notatie `Snippettagname`. In het volgende voorbeeld is te zien hoe u kunt verwijzen naar de tagnaam `BasicThrow`:

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

Het relatieve pad naar de bron in de opslagplaats **dotnet/voorbeelden** volgt het pad `~/samples`.

En u kunt zien hoe de tags van de fragmenten in [dit bronbestand](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) zijn gestructureerd. Zie de [DocFX-richtlijnen](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file) voor details over weergave van tagnamen in bronbestanden van codefragmenten per taal.

In het volgende voorbeeld is de code te zien die in alle drie .NET-talen is ingevoegd:

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

Wanneer u fragmenten uit volledige programma's invoegt, zorgt dit ervoor dat alle code via ons CI-systeem (Continue integratie) gaat. Als u echter iets moet weergeven wat voor compilatietijd- of runtimefouten zorgt, kunt u codeblokken in regels gebruiken.

## <a name="images"></a>Afbeeldingen

### <a name="static-image-or-animated-gif"></a>Statische afbeelding of GIF-animatie

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Gekoppelde afbeelding

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Video's

Momenteel kunt u zowel Channel 9- als YouTube-video's insluiten met de volgende syntaxis:

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

Selecteer het tabblad **Insluiten** onder het videoframe en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen. Bijvoorbeeld:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Klik met de rechtermuisknop op de video, selecteer **Insluitcode kopiëren** en kopieer de URL vanuit het `<iframe>`-element om de juiste URL van de video te krijgen.

```markdown
> [!VIDEO <youtube_video_link>]
```

Bijvoorbeeld:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>Extensies docs.microsoft

docs.microsoft biedt GitHub Flavored Markdown enkele extra extensies.

### <a name="checked-lists"></a>Gecontroleerde lijsten

Er is een aangepaste stijl beschikbaar voor lijsten. U kunt lijsten met groene vinkjes renderen.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Dit wordt weergegeven als:

> [!div class="checklist"]
> * Een .NET Core-app maken
> * Een verwijzing toevoegen aan het pakket Microsoft.XmlSerializer.Generator
> * MyApp.csproj zo bewerken dat u afhankelijkheden kunt toevoegen
> * Een klasse en een XmlSerializer toevoegen
> * De toepassing bouwen en uitvoeren

U kunt in de [.NET Core-documenten](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator) een voorbeeld zien van gecontroleerde lijsten in actie.

### <a name="buttons"></a>Knoppen

Knopkoppelingen:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Dit wordt weergegeven als:

> [!div class="button"]
> [knopkoppelingen](dotnet-contribute.md)

U kunt in de [Visual Studio-documenten](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio) een voorbeeld zien van knoppen in actie.

### <a name="step-by-steps"></a>Stappenplannen

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

U kunt in de [C#-handleiding](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure) een voorbeeld zien van stappenplannen in actie.
