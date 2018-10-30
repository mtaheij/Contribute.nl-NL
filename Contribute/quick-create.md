---
title: 'Snelstart: een geheim instellen en ophalen uit Azure Key Vault | Microsoft Docs'
description: 'Snelstart: een geheim instellen en ophalen uit Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805732"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Snelstart: een geheim instellen en ophalen uit Azure Key Vault

In deze snelstart ziet u hoe u een geheim kunt opslaan in Key Vault en dit geheim vervolgens kunt ophalen met behulp van een web-app. Als u de geheime waarde wilt bekijken, voert u deze uit in Azure. In de snelstart wordt gebruikgemaakt van Node.js en beheerde service-identiteiten (MSI's).

> [!div class="checklist"]
> * Maak een sleutelkluis.
> * Sla een geheim op in de sleutelkluis.
> * Haal een geheim op uit Key Vault.
> * Maak een Azure-webtoepassing.

> * [Schakel beheerde service-identiteiten in](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Verleen de vereiste machtigingen voor de webtoepassing om gegevens in Key Vault te lezen.

Controleer voordat u verdergaat of u bekend bent met de [basisbeginselen](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

> [!NOTE]
> U moet een aantal concepten kennen om te begrijpen waarom de onderstaande zelfstudie de best practice is. Key Vault is een centrale opslagplaats voor het opslaan van geheimen via een programma. Maar hiervoor moeten toepassingen/gebruikers eerst worden geverifieerd bij Key Vault, dat wil zeggen een geheim presenteren. Als u de best practices voor beveiliging wilt volgen, moet dit eerste geheim ook periodiek worden gerouleerd. Maar met [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) krijgen toepassingen die worden uitgevoerd in Azure, een identiteit die automatisch wordt beheerd in Azure. Dit helpt bij het oplossen van het **probleem van het introduceren van geheimen** waar gebruikers/toepassingen best practices kunnen volgen zonder dat het eerste geheim hoeft te worden gerouleerd

## <a name="prerequisites"></a>Vereisten

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* [Visual Studio 2017 versie 15.7.3 of hoger](https://www.microsoft.com/net/download/windows) met de volgende workloads:
  * ASP.NET-ontwikkeling en webontwikkeling
  * Platformoverschrijdende ontwikkeling met .NET Core
* [.NET Core 2.1 SDK of hoger](https://www.microsoft.com/net/download/windows)
::: zone-end
* Git ([download](https://git-scm.com/downloads)).
* Een Azure-abonnement. Als u nog geen Azure-abonnement hebt, maakt u eerst een [gratis account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) aan voordat u begint.
* Versie [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 of later. Deze versie is beschikbaar voor Windows, Mac en Linux.

## <a name="login-to-azure"></a>Aanmelden bij Azure

Als u zich wilt aanmelden bij Azure met behulp van de opdrachtregelinterface, typt u:

```azurecli
az login
```

## <a name="create-resource-group"></a>Resourcegroep maken

Maak een resourcegroep met de opdracht [az group create](/cli/azure/group#az-group-create). Een Azure-resourcegroep is een logische container waarin Azure-resources worden geïmplementeerd en beheerd.

Selecteer de naam van een resourcegroep en vul de tijdelijke aanduiding in.
In het volgende voorbeeld wordt een resourcegroep met de naam *<YourResourceGroupName>* gemaakt op de locatie *eastus*.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

De resourcegroep die u zojuist hebt gemaakt, wordt overal in deze zelfstudie gebruikt.

## <a name="create-an-azure-key-vault"></a>Een Azure-sleutelkluis maken

Vervolgens maakt u een sleutelkluis met behulp van de resourcegroep die u in de vorige stap hebt gemaakt. Hoewel in dit artikel ContosoKeyVault wordt gebruikt als de naam voor de sleutelkluis, moet u een unieke naam gebruiken. Geef de volgende informatie op:

* Naam van de kluis: **selecteer hier de naam van de sleutelkluis**.
* Naam van de resourcegroep: **selecteer hier de naam van de resourcegroep**.
* Locatie: **eastus**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

Op dit moment is uw Azure-account de enige gemachtigde om bewerkingen uit te voeren voor deze nieuwe kluis.

## <a name="add-a-secret-to-key-vault"></a>Een geheim toevoegen aan Key Vault

We gaan een geheim toevoegen om te laten zien hoe dit werkt. U kunt een SQL-verbindingsreeks opslaan of andere gegevens die u veilig wilt bewaren, maar wel beschikbaar wilt stellen voor de toepassing. In deze zelfstudie gebruiken we het geheim **AppSecret** en slaan we de waarde van **MySecret** op in dit geheim.

Typ de onderstaande opdrachten om in Key Vault een geheim te maken met de naam **AppSecret** waarin de waarde van **MySecret** wordt opgeslagen:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Ga als volgt te werk om het geheim weer te geven als tekst zonder opmaak:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Met deze opdracht vraagt u de geheime gegevens op, inclusief de URI. Als u deze stappen hebt uitgevoerd, beschikt u over een URI voor een geheim in een Azure-sleutelkluis. Schrijf deze gegevens op. U hebt deze in een latere stap nodig.

## <a name="clone-the-repo"></a>De opslagplaats klonen

Kloon de opslagplaats zodat u een lokale kopie ervan hebt en de bron kunt bewerken. Voer hiervoor de volgende opdracht uit:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Afhankelijkheden installeren

Hier installeren we de afhankelijkheden. Voer de volgende opdrachten uit:

    cd key-vault-node-quickstart
    npm install

In dit project worden twee knooppuntmodules gebruikt:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>De webtoepassing publiceren in Azure

Hieronder vindt u de paar stappen die moeten worden uitgevoerd om de toepassing in Azure te publiceren.

* In de eerste stap wordt een plan voor een [Azure App Service](https://azure.microsoft.com/services/app-service/) gemaakt. In dit plan kunt u meerdere web-apps opslaan.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Hierna maken we een web-app. Vervang in het volgende voorbeeld <app_name> door een globaal unieke naam (geldige tekens zijn a-z, 0-9 en -). De runtime wordt ingesteld op NODE|6.9. Voer `az webapp list-runtimes` uit als u alle ondersteunde runtimes wilt zien

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Wanneer de web-app is gemaakt, wordt met Azure CLI uitvoer weergegeven die lijkt op het volgende voorbeeld:

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    Blader naar de pas gemaakte web-app. U ziet een werkende web-app. Vervang <app-name> door een unieke app-naam.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Met de bovenstaande opdracht wordt ook een app gemaakt waarvoor Git is ingeschakeld, waarmee u vanuit de lokale Git kunt implementeren in Azure. 
    De lokale Git wordt geconfigureerd met de volgende URL: https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git

* Maak een implementatiegebruiker. Als de vorige opdracht is uitgevoerd, kunt u een externe Azure-instantie toevoegen aan de lokale Git-opslagplaats. Vervang <url> door de URL van de externe Git-instantie die u hebt verkregen bij Git inschakelen voor uw app.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>De oplossing openen en bewerken

Bewerk het bestand program.cs om het voorbeeld uit te voeren met de naam van uw specifieke sleutelkluis:

1. Ga naar de map key-vault-dotnet-core-quickstart.
2. Open het bestand key-vault-dotnet-core-quickstart.sln in Visual Studio 2017.
3. Open het bestand Program.cs en vervang de tijdelijke aanduiding *YourKeyVaultName* door de naam van de sleutelkluis die u eerder hebt gemaakt.

Deze oplossing maakt gebruik van de NuGet-bibliotheken [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) en [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).

## <a name="run-the-app"></a>De app uitvoeren

Selecteer **Fouten opsporen** > **Starten** zonder foutopsporing in het hoofdmenu van Visual Studio 2017. Wanneer de browser wordt weergegeven, gaat u naar de pagina **Over**. U ziet nu de waarde voor **AppGeheim**.

## <a name="publish-the-web-application-to-azure"></a>De webtoepassing publiceren in Azure

Publiceer de app in Azure om deze live als web-app in actie te zien en om te controleren of u de geheime waarde kunt ophalen:

1. Selecteer in Visual Studio het project **key-vault-dotnet-core-quickstart**.
2. Selecteer **Publiceren** > **Start**.
3. Maak een nieuwe **App Service** en selecteer vervolgens **Publiceren**.
4. Wijzig de naam van de app in **keyvaultdotnetcorequickstart**.
5. Selecteer **Maken**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>Beheerde service-identiteiten inschakelen

Azure Key Vault biedt een manier voor het veilig opslaan van referenties en andere sleutels en geheimen, maar uw code moet worden geverifieerd in Azure Key Vault om deze referenties op te halen. Met Managed Service Identity wordt dit eenvoudiger doordat Azure-services zijn voorzien van een automatisch beheerde identiteit in Azure AD (Azure Active Directory). U kunt deze identiteit gebruiken voor verificatie bij alle services die ondersteuning bieden voor Azure AD-verificatie, inclusief Key Vault, zonder dat u referenties in uw code hoeft te hebben.

1. Ga terug naar Azure CLI.
2. Voer de opdracht assign-identity uit om de identiteit voor deze toepassing te maken:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>De opdracht in deze procedure komt overeen met naar de portal gaan en **Managed Service Identity** in de eigenschappen van de webtoepassing instellen op **Aan**.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Machtigingen toewijzen aan de toepassing om geheimen in Key Vault te lezen

Maak een notitie van de uitvoer wanneer u de toepassing publiceert in Azure. Gebruik hierbij de notatie:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Voer deze opdracht uit met de naam van uw sleutelkluis en de waarde **PrincipalId**:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>De Node-app implementeren in Azure en de geheime waarde ophalen

Nu alles is ingesteld, voert u de volgende opdracht uit om de app te implementeren in Azure

```bash
git push azure master
```

Als u hierna naar https://<app_name>.azurewebsites.net bladert, ziet u de geheime waarde.
Controleer of u de naam <YourKeyVaultName> hebt vervangen door de naam van de kluis

::: zone-end

::: zone pivot="dotnet"
Tijdens het uitvoeren van de toepassing ziet u nu de geheime waarde die is opgehaald.
::: zone-end

## <a name="next-steps"></a>Volgende stappen

::: zone pivot="nodejs"
* [Startpagina van Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentatie voor Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK voor Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API-naslaginformatie](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Startpagina van Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentatie voor Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Azure-SDK voor .NET](https://github.com/Azure/azure-sdk-for-net)
* [Azure REST API-naslaginformatie](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
