---
title: Een pull-aanvraag verzenden
description: Dit artikel beschrijft het proces en best practices voor pull-aanvragen, zodat u zeker weet dat uw bijdrage wordt samengevoegd.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188219"
---
# <a name="best-practices-for-pull-requests"></a>Best practice voor pull-aanvragen

Als u inhoudelijke wijzigingen wilt indienen, dient u een pull-aanvraag in vanuit uw fork. Elke pull-aanvraag moet worden gecontroleerd voordat deze kan worden samengevoegd.

## <a name="target-the-correct-branch"></a>De juiste vertakking kiezen

Alle wijzigingen moeten worden gemaakt in de vertakking `staging`. Wijzigingen mogen nooit zijn gericht op de vertakking `live`. Wijzigingen in de vertakking `staging` kunnen worden samengevoegd in `live` zodat alle wijzigingen die in `live` worden gemaakt, worden overschreven.

Als u een wijziging indient voor documentatie die alleen op een niet-uitgebrachte versie van PowerShell van toepassing is, moet u controleren of er een releasevertakking is voor die versie. Alle wijzigingen die op een specifieke, toekomstige versie van toepassing zijn, moeten worden gericht op de releasevertakking. Releasevertakkingen hebben het volgende naamgevingspatroon: `release-<version>`.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>Zorg ervoor dat de wachtrij voor pull-aanvragen voor iedereen beter werkt

In de wachtrij voor pull-aanvragen hebben we te maken met twee vaststaande feiten:

- Voor controle van pull-aanvragen met een kleine omvang en gerelateerde wijzigingen is minder tijd nodig.
- Voor controle van pull-aanvragen met een grote omvang of niet-gerelateerde wijzigingen is meer tijd nodig.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>Vermijd vertakkingen waarmee grote aantallen bestanden worden bijgewerkt

Scheid kleine updates aan bestaande artikelen van nieuwe artikelen of artikelen die grotendeels zijn herschreven. Behandel deze wijzigingen in aparte werkstromen.

Massale wijzigingen drijven pull-aanvragen met grote aantallen gewijzigde bestanden aan. Beperk uw pull-aanvragen tot maximaal 50 gewijzigde bestanden. Grote pull-aanvragen zijn moeilijk te controleren en gevoeliger voor fouten.

### <a name="renaming-or-deleting-files"></a>Bestanden een andere naam geven of verwijderen

Als u bestanden een andere naam geeft of verwijdert, moet u voorkomen dat deze wijzigingen worden vermengd met toevoegingen of updates van inhoud.
Verwerk deze wijzigingen in een afzonderlijke pull-aanvraag die wordt samengevoegd na de pull-aanvraag voor gerelateerde updates. Werk bijvoorbeeld het omleidbestand bij en controleer of de omleiding werkt voor u een artikel verwijdert.

U moet alle bestanden bijwerken die verwijzen naar het bestand waarvan de naam is gewijzigd. Dit omvat ook alle inhoudsopgavebestanden. U moet ook omleidingsvermeldingen toevoegen in het omleidingshoofdbestand (`.openpublishing.redirection.json`) in de hoofdmap van de opslagplaats.

## <a name="docs-pr-validation-service"></a>Docs PR-validatieservice

De Docs PR-validatieservice is een GitHub-app die validatieregels uitvoert op de bestanden in een PR.

U ziet het volgende gedrag:

1. U dient een PR in.
1. In de GitHub-opmerking die de status van uw PR aangeeft, ziet u de status van controles die zijn ingeschakeld voor de opslagplaats. In dit voorbeeld zijn er twee controles ingeschakeld, namelijk "Commit Validation" en "OpenPublishing.Build":

   ![sommige controles zijn mislukt](media/powershell-pull-requests/validation-failed.png)

   De build kan mogelijk toch worden doorgevoerd, ook als de validatie voor het doorvoeren niet is geslaagd.

1. Klik op **Details** voor meer informatie.
1. Op de pagina Details ziet u alle validatiecontroles die zijn mislukt, met informatie over wat u moet doen om de problemen op te lossen.
1. Als de validatie slaagt, wordt de volgende opmerking toegevoegd aan de pull-aanvraag:

   ![build-validatie](media/powershell-pull-requests/build-validation.png)

Als u een externe bijdrager (dus van buiten Microsoft) bent, hebt u geen toegang tot de gedetailleerde compilatierapporten of preview-koppelingen.

### <a name="build-warnings"></a>Build-waarschuwingen

Normaal gesproken moet u alle build-fouten, -waarschuwingen en -suggesties oplossen. Er zijn echter een aantal waarschuwingen die kunnen worden genegeerd.

De volgende waarschuwingen kunnen niet worden genegeerd:

- > Kan de servicenaam voor `<version>/<modulepath>/About/About.md` niet vinden

- > Metagegevens met een of meer van de volgende namen mogen niet worden ingesteld in de YAML-koptekst, als metagegevens op bestandsniveau in docfx.json of als algemene metagegevens in docfx.json: `locale`. Deze worden door het Docs-platform gegenereerd. De waarden die op deze 3 plaatsen worden ingesteld, worden daarom genegeerd. Verwijder ze uit alle 3 de plaatsen om de waarschuwing op te lossen.
