---
title: Validatie-time-out
description: Uitleg en oplossing voor Docs-buildprobleem validatie-time-out
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033292"
---
# <a name="validation-timeout"></a>Validatie-time-out

## <a name="warning"></a>Waarschuwing

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

Soms kan het door tijdelijke problemen in de validatieservice, zoals een slecht functionerende server, voorkomen dat Docs Build de service op correcte wijze aanroept. De aanroep registreert na meerdere pogingen een time-out en de validatie wordt geannuleerd om build-vertragingen en een overbelaste build-pipeline te voorkomen.

## <a name="resolution"></a>Oplossing

Probeer uw pull-aanvraag te sluiten en opnieuw te openen of een handmatige build-actie via Docs-portal uit te voeren (alleen mogelijk voor opslagplaatsbeheerders). Vaak worden serviceproblemen vanzelf opgelost wanneer de handeling opnieuw wordt uitgevoerd. Als u hulp nodig hebt van een beheerder of de melding blijft ontvangen, kunt u een probleem melden via [https://SiteHelp](https://SiteHelp) als u een Microsoft-medewerker bent of met een @vermelding van de auteur van een artikel in uw pull-aanvraag om hulp vragen als u een externe inzender bent.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
