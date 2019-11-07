---
title: Validatie-time-out
description: Uitleg en oplossing voor Docs-buildprobleem validatie-time-out
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592546"
---
# <a name="validation-timeout"></a>Validatie-time-out

## <a name="warning"></a>Waarschuwing

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

Soms kan het door tijdelijke problemen in de validatieservice, zoals een slecht functionerende server, voorkomen dat Docs Build de service op correcte wijze aanroept. De aanroep registreert na meerdere pogingen een time-out en de validatie wordt geannuleerd om build-vertragingen en een overbelaste build-pipeline te voorkomen.

## <a name="resolution"></a>Oplossing

Sluit uw pull-aanvraag af en open deze opnieuw of forceer een volledige build via [Docs Portal](https://ops.microsoft.com/#/). Vaak worden serviceproblemen vanzelf opgelost wanneer de handeling opnieuw wordt uitgevoerd.

U moet een opslagplaatsbeheerder zijn om een build via Docs Portal te forceren. Als u niet weet wie u opslagplaatsbeheerder is of als u de melding blijft ontvangen na een geforceerde build, kunt u een probleem melden via [https://SiteHelp](https://SiteHelp) als u een Microsoft-medewerker bent of met een @vermelding van de auteur van een artikel in uw pull-aanvraag om hulp vragen als u een externe inzender bent.

Als u een opslagplaatsbeheerder bent, kunt u als volgt een volledige build forceren:

1. Ga naar [Docs Portal](https://ops.microsoft.com/#/) en meld u aan.
1. Zoek de opslagplaats door in de linkerbovenhoek te zoeken en selecteer deze.

   :::image type="content" source="media/find-repo.png" alt-text="uw opslagplaats zoeken via het zoekvak van Docs Portal":::
1. Klik op het tabblad **Buildgeschiedenis** op **+ Handmatig publiceren**.
1. Selecteer de vertakking die de waarschuwing krijgt, zoals Basis.
1. Behoud de standaard **Docs-site** voor het doel.
1. Schakel het selectievakje **Geforceerd publiceren** in.
1. Klik op **Publiceren**.

   :::image type="content" source="media/force-build.png" alt-text="stappen om een volledige build te forceren":::

Hiermee wordt een volledige build op de vertakking geforceerd.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
