---
title: Specifieke richtlijnen voor het schrijven van scriptvoorbeelden
description: Dit artikel bevat specifieke regels voor het opmaken van PowerShell-codevoorbeelden. Dit is van toepassing op conceptuele artikelen met voorbeelden en op cmdlet-verwijzingen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290260"
---
# <a name="formatting-code-samples"></a>Codevoorbeelden opmaken

In de bestaande documentatie is door de tijd heen meerdere stijlen gebruikt. Ook zijn de regels voor het opmaken meerdere keren gewijzigd. We proberen een consistente stijl voor PowerShell-codeblokken en -uitvoer in onze documentatie aan te houden.

Markdown ondersteunt twee verschillende codestijlen:

- Codereeksen (inline) - gemarkeerd met één accent grave (`` ` ``). Wordt inline in een alinea gebruikt in plaats van als een op zichzelf staand codeblok. Wordt vooral gebruikt rond cmdlet-namen. Zie [Syntaxiselementen van opdrachten opmaken](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Codeblokken: een blok van meerdere regels, omringd door tekenreeksen met drievoudige accents graves (`` ``` ``).

## <a name="using-code-blocks"></a>Codeblokken gebruiken

Markdown biedt de mogelijkheid om inspringing te gebruiken om een codeblok aan te duiden, maar dit patroon kan problematisch zijn en moet worden vermeden. Alle codeblokken moeten zich binnen een afscheiding bevinden. Een afscheiding is een codeblok dat wordt omringd door tekenreeksen met drie accents graves (`` ``` ``). De markeringen voor de codeafscheiding moeten zich op een eigen regel voor en na het codevoorbeeld bevinden. De markering na het begin van het codeblok heeft mogelijk een optioneel taallabel. In het Open Publishing System (OPS) van Microsoft wordt het taallabel gebruikt om de functie voor markering van de syntaxis te ondersteunen.

OPS voegt tevens een knop **Kopiëren** toe waarmee u de inhoud van het codeblok naar het klembord kopieert. Hiermee kunt u de code snel in een script plakken om het codevoorbeeld te testen. Niet alle voorbeelden in onze documentatie zijn echter bedoeld om op die manier te worden uitgevoerd. Sommige codeblokken vormen mogelijk een eenvoudige illustratie van een PowerShell-concept of een abstracte weergave van syntaxis.

In onze documentatie worden twee typen codeblokken gebruikt:

1. Illustratieve voorbeelden
2. Uitvoerbare voorbeelden

## <a name="formatting-illustrative-examples"></a>Illustratieve voorbeelden opmaken

Illustratieve voorbeelden worden gebruikt om een PowerShell-concept uit te leggen. Ze zijn niet bedoeld om naar het klembord te worden gekopieerd en te worden uitgevoerd. Ze worden vooral gebruikt voor eenvoudige voorbeelden die gemakkelijk kunnen worden getypt.
Ook worden ze gebruikt voor syntaxisvoorbeelden, waarbij de syntaxis van een opdracht wordt geïllustreerd.

Illustratieve voorbeelden maken gebruikt van een ‘naakte’ afscheiding om het begin en einde van een codeblok te markeren. Het codeblok kan voorbeelduitvoer bevatten van de opdracht die wordt geïllustreerd.

### <a name="syntax-block"></a>Syntaxisblok

Dit voorbeeld toont alle mogelijke parameters van de `Get-Command`-cmdlet.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

Dit voorbeeld bevat een beschrijving van de `for`-instructie in algemene termen:

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Eenvoudig illustratief voorbeeld

Dit is een voorbeeld waarin de operators van de PowerShell-vergelijking worden weergegeven:

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

Houd er rekening mee dat dit voorbeeld de vereenvoudigde PowerShell-prompt bevat en de resulterende uitvoer weergeeft. In dit geval is het niet de bedoeling dat de lezer dit voorbeeld kopieert en uitvoert.

## <a name="formatting-executable-examples"></a>Uitvoerbare voorbeelden opmaken

Complexere voorbeelden of voorbeelden die bedoeld zijn om te worden gekopieerd en uitgevoerd, moeten de volgende blokstijlopmaak gebruiken:

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

De uitvoer die door PowerShell-opdrachten wordt weergegeven, moet zich in een **Uitvoer**-codeblok bevinden om markering van de syntaxis te voorkomen. Bijvoorbeeld:

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

Het codelabel **Uitvoer** is geen officiële ‘taal’ die door het systeem voor het markeren van syntaxis wordt ondersteund.
Dit label is echter nuttig omdat in OPS het label ‘Uitvoer’ aan het codevak op de webpagina wordt toegevoegd.
En de syntaxis in dit codevak ‘Uitvoer’ is niet gemarkeerd.

## <a name="coding-style-rules"></a>Stijlregels voor code

### <a name="avoid-line-continuation-in-code-samples"></a>Voortzetting van regels in codevoorbeelden vermijden

Vermijd tekens voor voortzetting van de regel (`` ` ``) in PowerShell-codevoorbeelden. Deze zijn moeilijk te zien en kunnen problemen veroorzaken als er extra spaties aan het einde van de regel staan.

- Gebruik PowerShell-splatting om de regellengte in te korten voor cmdlets die veel parameters bevatten.
- Profiteer van de mogelijkheden voor natuurlijke regeleinden in PowerShell, zoals na het pijpteken (`|`), accolades en haakjes.

### <a name="avoid-using-powershell-prompts-in-examples"></a>PowerShell-prompts vermijden in voorbeelden

Het gebruik van de prompt-tekenreeks wordt afgeraden en moet worden beperkt tot scenario’s die zijn bedoeld om het gebruik van de opdrachtregel te illustreren. Prompts zijn vereist voor voorbeelden waarin opdrachten worden weergegeven waarmee de prompt wordt aangepast of als het getoonde pad van belang is voor het scenario dat wordt geïllustreerd.

- PowerShell-prompts moeten alleen worden gebruikt in illustratieve voorbeelden. De prompt-tekenreeks moet voor de meeste voorbeelden ‘`PS>`’ zijn. Deze prompt is onafhankelijk van indicatoren voor specifieke besturingssystemen.
- Prompts moeten **NIET** worden gebruikt in uitvoerbare voorbeelden.

In het volgende voorbeeld wordt getoond hoe de prompt verandert als de registerprovider wordt gebruikt.

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a>Geen aliassen gebruiken in voorbeelden

Gebruik altijd de volledige naam van cmdlets en parameters, tenzij u het specifiek over de alias hebt. Cmdlet- en parameternamen moeten de juiste Pascal-Case-spelling bevatten die in de code is gedefinieerd.

### <a name="using-parameters-in-examples"></a>Parameters gebruiken in voorbeelden

Vermijd het gebruik van positionele parameters. Over het algemeen moet u altijd de parameternaam in een voorbeeld insluiten, zelfs als de parameter positioneel is. Dit verkleint de kans op verwarring in uw voorbeelden.
