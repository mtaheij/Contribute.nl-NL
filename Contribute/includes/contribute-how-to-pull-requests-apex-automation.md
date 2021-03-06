---
ms.openlocfilehash: b64e8dd4c62ca05b6e04ef404ebf98a618d0171e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "66391263"
---
Door middel van automatisering van opmerkingen kunnen gebruikers op leesniveau (gebruikers die geen schrijfmachtigingen in een opslagplaats hebben) een actie op schrijfniveau uitvoeren door het desbetreffende label aan een pull-aanvraag (PR) toe te wijzen. Als u in een opslagplaats werkt waar automatisering van opmerkingen is geïmplementeerd, gebruikt u de hashtag-opmerkingen in de volgende tabel om labels toe te wijzen of te wijzigen, of een pull-aanvraag te sluiten. Microsoft-medewerkers krijgen ook via e-mail een melding over het controleren en goedkeuren van openbare opslagplaats-PR's als er wijzigingen worden voorgesteld voor artikelen waarvan u de auteur bent.

| Hashtag-opmerking | Gevolg | Beschikbaarheid in opslagplaats |
| --- | --- | --- |
| `#sign-off` |Als de auteur van een artikel de opmerking `#sign-off` in de opmerkingenstream typt, wordt het label **ready-to-merge** toegewezen. Met dit label weten de revisoren in de opslagplaats wanneer een pull-aanvraag klaar is om te worden gecontroleerd of samengevoegd. <br/><br/> Als een bijdrager die *niet* als auteur vermeld staat, zich bij een openbare repopull-aanvraag wil afmelden met de opmerking `#sign-off`, wordt er een bericht voor de pull-aanvraag geschreven waarin staat aangegeven dat alleen de auteur het label kan toewijzen. |Openbare en persoonlijk |
| `#hold-off` |Een auteur kan `#hold-off` in een PR-opmerking typen om het label **ready-to-merge** te verwijderen voor het geval zij of hij van gedachten verandert of een fout heeft gemaakt. In de persoonlijke opslagplaats wordt hierdoor het label **do-not-merge** toegewezen. |Openbare en persoonlijk |
| `#please-close` |Een auteur kan `#please-close` in de opmerkingenstream typen om de pull-aanvraag te sluiten als zij of hij besluit de wijzigingen niet te willen samenvoegen. |Openbaar |
