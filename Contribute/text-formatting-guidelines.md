---
title: Richtlijnen voor het opmaken van tekst
description: Kom meer te weten over wanneer u de tekststijlen Vet, Cursief, Code en andere stijlen gebruikt in artikelen die worden gepubliceerd op docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336505"
---
# <a name="text-formatting-guidelines"></a>Richtlijnen voor het opmaken van tekst

Als de stijlen Vet, Cursief en Code consistent en correct worden gebruikt voor tekstelementen, verbetert dit de leesbaarheid en ontstaan er geen interpretatiefouten.

## <a name="bold"></a>Vet

Gebruik vet voor elementen in de gebruikersinterface, zoals menuopties, namen van dialoogvensters en namen van invoervelden.

### <a name="examples"></a>Voorbeelden

* **Dit**: Klik in **Solution Explorer** met de rechtermuisknop op het projectknooppunt en selecteer vervolgens **Toevoegen > Nieuw item**.
* **Niet dit**: Klik in Solution Explorer met de rechtermuisknop op het projectknooppunt en selecteer vervolgens Toevoegen > Nieuw item.
* **Niet dit**: Klik in *Solution Explorer* met de rechtermuisknop op het projectknooppunt en selecteer vervolgens *Toevoegen > Nieuw item*.

## <a name="italics"></a>Cursief

Gebruik cursief voor:

* Nieuwe termen die u introduceert in combinatie met een definitie of uitleg.
* Bestandsnamen, mapnamen, paden.
* Gebruikersinvoer.

### <a name="examples"></a>Voorbeelden

* **Dit**: In App Service worden apps uitgevoerd op basis van een *App Service-plan*. Een App Service-plan omvat een reeks rekenresources waarop web-apps kunnen worden uitgevoerd.
* **Niet dit**: In App Service worden apps uitgevoerd op basis van een 'App Service-plan'. Een App Service-plan omvat een reeks rekenresources waarop web-apps kunnen worden uitgevoerd.
* **Dit**: Vervang de code in *HttpTriggerCSharp.cs* door de volgende code.
* **Niet dit**: Vervang de code in `HttpTriggerCSharp.cs` door de volgende code.
* **Dit**: Voer *ContosoUniversity* in voor de **Naam**en selecteer vervolgens **Toevoegen**.
* **Niet dit**: Voer 'ContosoUniversity' in voor de **Naam** en selecteer vervolgens **Toevoegen**.

## <a name="code-style"></a>De stijl Code

Gebruik codestijl voor:

* Code-elementen, zoals methodenamen, eigenschapsnamen en taaltrefwoorden.
* SQL-opdrachten
* NuGet-pakketnamen
* Opdrachtregelopdrachten
* Databasetabel- en kolomnamen
* Resourcenamen die niet moeten worden gelokaliseerd (zoals namen van virtuele machines)
* URL's waarop niet kan worden geklikt

**Waarom?** In oudere stijlgidsen staat dat vet moet worden gebruikt voor veel van deze tekstelementen. De meeste artikelen worden echter gelokaliseerd en door de codestijl weet de vertaler dat dat deel van de tekst niet moet worden vertaald.

Codestijl kan *inline* (tussen \`) of *afgebakende* codeblokken (tussen \`\`\`) zijn die meerdere regels omvatten. Langere codefragmenten en paden moeten in speciale codeblokken worden geplaatst.

### <a name="examples-using-inline-styles"></a>Voorbeelden met inlinestijlen

* **Dit**: In Entity Framework worden eigenschappen met de naam `Id` of `ClassnameID` automatisch als primaire sleutel gezien.
* **Niet dit**: In Entity Framework worden eigenschappen met de naam *Id* of *ClassnameID* automatisch als primaire sleutel gezien.
* **Dit**: Het pakket `Microsoft.EntityFrameworkCore` biedt runtimeondersteuning voor EF Core.
* **Niet dit**: Het pakket *Microsoft.EntityFrameworkCore* biedt runtimeondersteuning voor EF Core.

### <a name="examples-of-fenced-code-blocks"></a>Voorbeelden van speciale codeblokken

* **Dit**: Er worden geen opdrachten verzonden naar de database als er instructies worden gegeven waarmee alleen een `IQueryable` wordt gewijzigd, zoals bij de volgende code:

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **Niet dit**: Er worden geen opdrachten verzonden naar de database als er instructies worden gebruikt waarmee alleen een **IQueryable** wordt gewijzigd, zoals bij **var students = context.Students.Where(s=> s.LastName == "Daviolo")** .

* **Dit**: Voer het volgende in om het script `Get-ServiceLog.ps1` uit te voeren in de map `C:\Scripts`:

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **Niet dit**: Voer het volgende in om het script **Get-ServiceLog.ps1** uit te voeren in de map **C:\Scripts**: "C:\Scripts\Get-ServiceLog.ps1."

* **Alle** afgebakende codeblokken moeten een goedgekeurde taalcode hebben. Zie [Code opnemen in documenten](./code-in-docs.md#supported-languages) voor een lijst met ondersteunde taalcodes.

## <a name="headings-and-link-text"></a>Koppen en tekst van koppelingen

Gebruik geen inlinestijl zoals cursief, vet of code voor koppen of hyperlinktekst.

**Waarom?**

Mensen herkennen tekst met de reguliere koppelingsopmaak als koppelingen waar ze op kunnen klikken. Als u een koppeling bijvoorbeeld de stijl Code geeft, is het mogelijk niet meer duidelijk dat de tekst een koppeling is. Koppen hebben hun eigen stijl en het ziet er rommelig uit om daar ook andere stijlen in te gebruiken.

### <a name="examples"></a>Voorbeelden

* **Dit**: Het bestand *function.json* wordt gegenereerd door het NuGet-pakket [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).
* **Niet dit**: Het bestand *function.json* wordt gegenereerd door het NuGet-pakket [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).

* **Dit**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **Niet dit**:

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>Toetsen en toetsenbordsneltoetsen

Volg deze conventies om te verwijzen naar toetsen of toetsencombinaties:

* Schrijf de eerste letter van de toetsnamen in hoofdletters.
* Gebruik geen inlinestijl zoals cursief, vet of code.
* Gebruik + om toetsen te koppelen die tegelijkertijd worden ingedrukt.

### <a name="examples"></a>Voorbeelden

* **Dit**: Selecteer Alt+Ctrl+S.
* **Niet dit**: Druk op  **Alt+Ctrl+S**.
* **Niet dit**: Druk op `ALT+CTRL+S`.

Zie [Interacties beschrijven met gebruikersinterface](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472) voor meer informatie.

## <a name="exceptions"></a>Uitzonderingen

Er zijn altijd uitzonderingen op de stijlrichtlijnen. Wanneer ze de leesbaarheid schaden, doet u iets anders. Een HTML-tabel met voornamelijk code-elementen ziet er mogelijk te rommelig uit als overal de stijl Code wordt gebruikt. U kunt in deze context vetgedrukte stijlen kiezen.

Als u een alternatieve tekststijl kiest waar normaal gesproken code is vereist, controleert u of de tekst in gelokaliseerde versies van het artikel kan worden vertaald. Code is de enige stijl waarbij vertaling automatisch wordt verhinderd. Zie [Niet-gelokaliseerde tekenreeksen](markdown-reference.md#non-localized-strings) als u lokalisatie wilt voorkomen zonder codestijl te gebruiken.
