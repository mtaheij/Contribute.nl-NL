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
# <a name="formatting-code-samples"></a><span data-ttu-id="7dd84-104">Codevoorbeelden opmaken</span><span class="sxs-lookup"><span data-stu-id="7dd84-104">Formatting code samples</span></span>

<span data-ttu-id="7dd84-105">In de bestaande documentatie is door de tijd heen meerdere stijlen gebruikt. Ook zijn de regels voor het opmaken meerdere keren gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="7dd84-106">We proberen een consistente stijl voor PowerShell-codeblokken en -uitvoer in onze documentatie aan te houden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="7dd84-107">Markdown ondersteunt twee verschillende codestijlen:</span><span class="sxs-lookup"><span data-stu-id="7dd84-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="7dd84-108">Codereeksen (inline) - gemarkeerd met één accent grave (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="7dd84-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="7dd84-109">Wordt inline in een alinea gebruikt in plaats van als een op zichzelf staand codeblok.</span><span class="sxs-lookup"><span data-stu-id="7dd84-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="7dd84-110">Wordt vooral gebruikt rond cmdlet-namen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="7dd84-111">Zie [Syntaxiselementen van opdrachten opmaken](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="7dd84-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="7dd84-112">Codeblokken: een blok van meerdere regels, omringd door tekenreeksen met drievoudige accents graves (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="7dd84-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="7dd84-113">Codeblokken gebruiken</span><span class="sxs-lookup"><span data-stu-id="7dd84-113">Using code blocks</span></span>

<span data-ttu-id="7dd84-114">Markdown biedt de mogelijkheid om inspringing te gebruiken om een codeblok aan te duiden, maar dit patroon kan problematisch zijn en moet worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="7dd84-115">Alle codeblokken moeten zich binnen een afscheiding bevinden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="7dd84-116">Een afscheiding is een codeblok dat wordt omringd door tekenreeksen met drie accents graves (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="7dd84-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="7dd84-117">De markeringen voor de codeafscheiding moeten zich op een eigen regel voor en na het codevoorbeeld bevinden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="7dd84-118">De markering na het begin van het codeblok heeft mogelijk een optioneel taallabel.</span><span class="sxs-lookup"><span data-stu-id="7dd84-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="7dd84-119">In het Open Publishing System (OPS) van Microsoft wordt het taallabel gebruikt om de functie voor markering van de syntaxis te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="7dd84-120">OPS voegt tevens een knop **Kopiëren** toe waarmee u de inhoud van het codeblok naar het klembord kopieert.</span><span class="sxs-lookup"><span data-stu-id="7dd84-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="7dd84-121">Hiermee kunt u de code snel in een script plakken om het codevoorbeeld te testen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="7dd84-122">Niet alle voorbeelden in onze documentatie zijn echter bedoeld om op die manier te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="7dd84-123">Sommige codeblokken vormen mogelijk een eenvoudige illustratie van een PowerShell-concept of een abstracte weergave van syntaxis.</span><span class="sxs-lookup"><span data-stu-id="7dd84-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="7dd84-124">In onze documentatie worden twee typen codeblokken gebruikt:</span><span class="sxs-lookup"><span data-stu-id="7dd84-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="7dd84-125">Illustratieve voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7dd84-125">Illustrative examples</span></span>
2. <span data-ttu-id="7dd84-126">Uitvoerbare voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7dd84-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="7dd84-127">Illustratieve voorbeelden opmaken</span><span class="sxs-lookup"><span data-stu-id="7dd84-127">Formatting illustrative examples</span></span>

<span data-ttu-id="7dd84-128">Illustratieve voorbeelden worden gebruikt om een PowerShell-concept uit te leggen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="7dd84-129">Ze zijn niet bedoeld om naar het klembord te worden gekopieerd en te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="7dd84-130">Ze worden vooral gebruikt voor eenvoudige voorbeelden die gemakkelijk kunnen worden getypt.</span><span class="sxs-lookup"><span data-stu-id="7dd84-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="7dd84-131">Ook worden ze gebruikt voor syntaxisvoorbeelden, waarbij de syntaxis van een opdracht wordt geïllustreerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="7dd84-132">Illustratieve voorbeelden maken gebruikt van een ‘naakte’ afscheiding om het begin en einde van een codeblok te markeren.</span><span class="sxs-lookup"><span data-stu-id="7dd84-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="7dd84-133">Het codeblok kan voorbeelduitvoer bevatten van de opdracht die wordt geïllustreerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="7dd84-134">Syntaxisblok</span><span class="sxs-lookup"><span data-stu-id="7dd84-134">Syntax block</span></span>

<span data-ttu-id="7dd84-135">Dit voorbeeld toont alle mogelijke parameters van de `Get-Command`-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd84-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="7dd84-136">Dit voorbeeld bevat een beschrijving van de `for`-instructie in algemene termen:</span><span class="sxs-lookup"><span data-stu-id="7dd84-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="7dd84-137">Eenvoudig illustratief voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7dd84-137">Simple illustration example</span></span>

<span data-ttu-id="7dd84-138">Dit is een voorbeeld waarin de operators van de PowerShell-vergelijking worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="7dd84-138">Here is an example illustrating PowerShell comparison operators:</span></span>

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

<span data-ttu-id="7dd84-139">Houd er rekening mee dat dit voorbeeld de vereenvoudigde PowerShell-prompt bevat en de resulterende uitvoer weergeeft.</span><span class="sxs-lookup"><span data-stu-id="7dd84-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="7dd84-140">In dit geval is het niet de bedoeling dat de lezer dit voorbeeld kopieert en uitvoert.</span><span class="sxs-lookup"><span data-stu-id="7dd84-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="7dd84-141">Uitvoerbare voorbeelden opmaken</span><span class="sxs-lookup"><span data-stu-id="7dd84-141">Formatting executable examples</span></span>

<span data-ttu-id="7dd84-142">Complexere voorbeelden of voorbeelden die bedoeld zijn om te worden gekopieerd en uitgevoerd, moeten de volgende blokstijlopmaak gebruiken:</span><span class="sxs-lookup"><span data-stu-id="7dd84-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="7dd84-143">De uitvoer die door PowerShell-opdrachten wordt weergegeven, moet zich in een **Uitvoer**-codeblok bevinden om markering van de syntaxis te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="7dd84-144">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="7dd84-144">For example:</span></span>

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

<span data-ttu-id="7dd84-145">Het codelabel **Uitvoer** is geen officiële ‘taal’ die door het systeem voor het markeren van syntaxis wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7dd84-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="7dd84-146">Dit label is echter nuttig omdat in OPS het label ‘Uitvoer’ aan het codevak op de webpagina wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="7dd84-147">En de syntaxis in dit codevak ‘Uitvoer’ is niet gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="7dd84-148">Stijlregels voor code</span><span class="sxs-lookup"><span data-stu-id="7dd84-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="7dd84-149">Voortzetting van regels in codevoorbeelden vermijden</span><span class="sxs-lookup"><span data-stu-id="7dd84-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="7dd84-150">Vermijd tekens voor voortzetting van de regel (`` ` ``) in PowerShell-codevoorbeelden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="7dd84-151">Deze zijn moeilijk te zien en kunnen problemen veroorzaken als er extra spaties aan het einde van de regel staan.</span><span class="sxs-lookup"><span data-stu-id="7dd84-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="7dd84-152">Gebruik PowerShell-splatting om de regellengte in te korten voor cmdlets die veel parameters bevatten.</span><span class="sxs-lookup"><span data-stu-id="7dd84-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="7dd84-153">Profiteer van de mogelijkheden voor natuurlijke regeleinden in PowerShell, zoals na het pijpteken (`|`), accolades en haakjes.</span><span class="sxs-lookup"><span data-stu-id="7dd84-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="7dd84-154">PowerShell-prompts vermijden in voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7dd84-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="7dd84-155">Het gebruik van de prompt-tekenreeks wordt afgeraden en moet worden beperkt tot scenario’s die zijn bedoeld om het gebruik van de opdrachtregel te illustreren.</span><span class="sxs-lookup"><span data-stu-id="7dd84-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="7dd84-156">Prompts zijn vereist voor voorbeelden waarin opdrachten worden weergegeven waarmee de prompt wordt aangepast of als het getoonde pad van belang is voor het scenario dat wordt geïllustreerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="7dd84-157">PowerShell-prompts moeten alleen worden gebruikt in illustratieve voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="7dd84-158">De prompt-tekenreeks moet voor de meeste voorbeelden ‘`PS>`’ zijn.</span><span class="sxs-lookup"><span data-stu-id="7dd84-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="7dd84-159">Deze prompt is onafhankelijk van indicatoren voor specifieke besturingssystemen.</span><span class="sxs-lookup"><span data-stu-id="7dd84-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="7dd84-160">Prompts moeten **NIET** worden gebruikt in uitvoerbare voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="7dd84-161">In het volgende voorbeeld wordt getoond hoe de prompt verandert als de registerprovider wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7dd84-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

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

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="7dd84-162">Geen aliassen gebruiken in voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7dd84-162">Do not use aliases in examples</span></span>

<span data-ttu-id="7dd84-163">Gebruik altijd de volledige naam van cmdlets en parameters, tenzij u het specifiek over de alias hebt.</span><span class="sxs-lookup"><span data-stu-id="7dd84-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="7dd84-164">Cmdlet- en parameternamen moeten de juiste Pascal-Case-spelling bevatten die in de code is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="7dd84-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="7dd84-165">Parameters gebruiken in voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7dd84-165">Using parameters in examples</span></span>

<span data-ttu-id="7dd84-166">Vermijd het gebruik van positionele parameters.</span><span class="sxs-lookup"><span data-stu-id="7dd84-166">Avoid using positional parameters.</span></span> <span data-ttu-id="7dd84-167">Over het algemeen moet u altijd de parameternaam in een voorbeeld insluiten, zelfs als de parameter positioneel is.</span><span class="sxs-lookup"><span data-stu-id="7dd84-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="7dd84-168">Dit verkleint de kans op verwarring in uw voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="7dd84-168">This reduces the chance of confusion in your examples.</span></span>
