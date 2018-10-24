---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084470"
---
# <a name="docs-pr-validation-service"></a>Docs PR-validatieservice

De Docs PR-validatieservice is een GitHub-app die validatieregels uitvoert op de bestanden in een PR.

Als de validatieservice is ingeschakeld voor een opslagplaats, ziet u het volgende gedrag:

1. U dient een PR in.
1. In de GitHub-opmerking die de status van uw PR aangeeft, ziet u de status van controles die zijn ingeschakeld voor de opslagplaats. In dit voorbeeld zijn er twee controles ingeschakeld, namelijk "Commit Validation" en "OpenPublishing.Build":

   ![sommige controles zijn mislukt](media/validation-failed.png)

   De build kan mogelijk toch worden doorgevoerd, ook als de validatie voor het doorvoeren niet is geslaagd.

1. Klik op **Details** voor meer informatie.
1. Op de pagina Details ziet u alle validatiecontroles die zijn mislukt, met informatie over wat u moet doen om de fouten op te lossen:

   ![validatiebericht](media/validation-details.png)

Zie de inhoudsopgave aan de linkerkant van dit artikel voor de lijst met validaties die momenteel beschikbaar zijn in de service.