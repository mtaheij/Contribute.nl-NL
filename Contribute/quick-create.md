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
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308819"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="41383-103">Snelstart: een geheim instellen en ophalen uit Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="41383-104">In deze snelstart ziet u hoe u een geheim kunt opslaan in Key Vault en dit geheim vervolgens kunt ophalen met behulp van een web-app.</span><span class="sxs-lookup"><span data-stu-id="41383-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="41383-105">Als u de geheime waarde wilt bekijken, voert u deze uit in Azure.</span><span class="sxs-lookup"><span data-stu-id="41383-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="41383-106">In de snelstart wordt gebruikgemaakt van Node.js en beheerde service-identiteiten (MSI's)</span><span class="sxs-lookup"><span data-stu-id="41383-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="41383-107">Maak een sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="41383-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="41383-108">Sla een geheim op in Key Vault.</span><span class="sxs-lookup"><span data-stu-id="41383-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="41383-109">Haal een geheim op uit Key Vault.</span><span class="sxs-lookup"><span data-stu-id="41383-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="41383-110">Maak een Azure-webtoepassing.
</span><span class="sxs-lookup"><span data-stu-id="41383-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="41383-111">[Schakel beheerde service-identiteiten in](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="41383-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="41383-112">Verleen de vereiste machtigingen voor de webtoepassing om gegevens in Key Vault te lezen.</span><span class="sxs-lookup"><span data-stu-id="41383-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="41383-113">Controleer voordat u verdergaat of u bekend bent met de [basisbeginselen](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="41383-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="41383-114">U moet een aantal concepten kennen om te begrijpen waarom de onderstaande zelfstudie de best practice is.</span><span class="sxs-lookup"><span data-stu-id="41383-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="41383-115">Key Vault is een centrale opslagplaats voor het opslaan van geheimen via een programma.</span><span class="sxs-lookup"><span data-stu-id="41383-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="41383-116">Maar hiervoor moeten toepassingen/gebruikers eerst worden geverifieerd bij Key Vault, dat wil zeggen een geheim presenteren.</span><span class="sxs-lookup"><span data-stu-id="41383-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="41383-117">Als u de best practices voor beveiliging wilt volgen, moet dit eerste geheim ook periodiek worden gerouleerd.</span><span class="sxs-lookup"><span data-stu-id="41383-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="41383-118">Maar met [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) krijgen toepassingen die worden uitgevoerd in Azure, een identiteit die automatisch wordt beheerd in Azure.</span><span class="sxs-lookup"><span data-stu-id="41383-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="41383-119">Dit helpt bij het oplossen van het **probleem van het introduceren van geheimen** waar gebruikers/toepassingen best practices kunnen volgen zonder dat het eerste geheim hoeft te worden gerouleerd</span><span class="sxs-lookup"><span data-stu-id="41383-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="41383-120">Vereisten</span><span class="sxs-lookup"><span data-stu-id="41383-120">Prerequisites</span></span>

<span data-ttu-id="41383-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="41383-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="41383-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="41383-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="41383-123">[Visual Studio 2017 versie 15.7.3 of hoger](https://www.microsoft.com/net/download/windows) met de volgende workloads:</span><span class="sxs-lookup"><span data-stu-id="41383-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="41383-124">ASP.NET-ontwikkeling en webontwikkeling</span><span class="sxs-lookup"><span data-stu-id="41383-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="41383-125">Platformoverschrijdende ontwikkeling met .NET Core</span><span class="sxs-lookup"><span data-stu-id="41383-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="41383-126">[.NET Core 2.1 SDK of later](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="41383-127">Git ([download](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="41383-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="41383-128">Een Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="41383-128">An Azure subscription.</span></span> <span data-ttu-id="41383-129">Als u nog geen Azure-abonnement hebt, maakt u eerst een [gratis account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) aan voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="41383-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="41383-130">Versie [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 of later.</span><span class="sxs-lookup"><span data-stu-id="41383-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="41383-131">Deze versie is beschikbaar voor Windows, Mac en Linux.</span><span class="sxs-lookup"><span data-stu-id="41383-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="41383-132">Aanmelden bij Azure</span><span class="sxs-lookup"><span data-stu-id="41383-132">Login to Azure</span></span>

<span data-ttu-id="41383-133">Als u zich wilt aanmelden bij Azure met behulp van de opdrachtregelinterface, typt u:</span><span class="sxs-lookup"><span data-stu-id="41383-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="41383-134">Resourcegroep maken</span><span class="sxs-lookup"><span data-stu-id="41383-134">Create resource group</span></span>

<span data-ttu-id="41383-135">Maak een resourcegroep met de opdracht [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="41383-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="41383-136">Een Azure-resourcegroep is een logische container waarin Azure-resources worden geïmplementeerd en beheerd.</span><span class="sxs-lookup"><span data-stu-id="41383-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="41383-137">Selecteer de naam van een resourcegroep en vul de tijdelijke aanduiding in.</span><span class="sxs-lookup"><span data-stu-id="41383-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="41383-138">In het volgende voorbeeld wordt een resourcegroep met de naam *<YourResourceGroupName>* gemaakt op de locatie *eastus*.</span><span class="sxs-lookup"><span data-stu-id="41383-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="41383-139">De resourcegroep die u zojuist hebt gemaakt, wordt overal in deze zelfstudie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41383-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="41383-140">Een Azure-sleutelkluis maken</span><span class="sxs-lookup"><span data-stu-id="41383-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="41383-141">Vervolgens maakt u een sleutelkluis met behulp van de resourcegroep die u in de vorige stap hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="41383-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="41383-142">Hoewel in dit artikel ContosoKeyVault wordt gebruikt als de naam voor de sleutelkluis, moet u een unieke naam gebruiken.</span><span class="sxs-lookup"><span data-stu-id="41383-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="41383-143">Geef de volgende informatie op:</span><span class="sxs-lookup"><span data-stu-id="41383-143">Provide the following information:</span></span>

* <span data-ttu-id="41383-144">Naam van de kluis: **selecteer hier de naam van de sleutelkluis**.</span><span class="sxs-lookup"><span data-stu-id="41383-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="41383-145">Naam van de resourcegroep: **selecteer hier de naam van de resourcegroep**.</span><span class="sxs-lookup"><span data-stu-id="41383-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="41383-146">Locatie: **eastus**.</span><span class="sxs-lookup"><span data-stu-id="41383-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="41383-147">Op dit moment is uw Azure-account de enige gemachtigde om bewerkingen uit te voeren voor deze nieuwe kluis.</span><span class="sxs-lookup"><span data-stu-id="41383-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="41383-148">Een geheim toevoegen aan Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-148">Add a secret to key vault</span></span>

<span data-ttu-id="41383-149">We gaan een geheim toevoegen om te laten zien hoe dit werkt.</span><span class="sxs-lookup"><span data-stu-id="41383-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="41383-150">U kunt een SQL-verbindingsreeks opslaan of andere gegevens die u veilig wilt bewaren, maar wel beschikbaar wilt stellen voor de toepassing.</span><span class="sxs-lookup"><span data-stu-id="41383-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="41383-151">In deze zelfstudie gebruiken we het geheim **AppSecret** en slaan we de waarde van **MySecret** op in dit geheim.</span><span class="sxs-lookup"><span data-stu-id="41383-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="41383-152">Typ de onderstaande opdrachten om in Key Vault een geheim te maken met de naam **AppSecret** waarin de waarde van **MySecret** wordt opgeslagen:</span><span class="sxs-lookup"><span data-stu-id="41383-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="41383-153">Ga als volgt te werk om het geheim weer te geven als tekst zonder opmaak:</span><span class="sxs-lookup"><span data-stu-id="41383-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="41383-154">Met deze opdracht vraagt u de geheime gegevens op, inclusief de URI.</span><span class="sxs-lookup"><span data-stu-id="41383-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="41383-155">Als u deze stappen hebt uitgevoerd, beschikt u over een URI voor een geheim in een Azure-sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="41383-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="41383-156">Schrijf deze gegevens op.</span><span class="sxs-lookup"><span data-stu-id="41383-156">Write this information down.</span></span> <span data-ttu-id="41383-157">U hebt deze in een latere stap nodig.</span><span class="sxs-lookup"><span data-stu-id="41383-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="41383-158">De opslagplaats klonen</span><span class="sxs-lookup"><span data-stu-id="41383-158">Clone the Repo</span></span>

<span data-ttu-id="41383-159">Kloon de opslagplaats zodat u een lokale kopie ervan hebt en de bron kunt bewerken. Voer hiervoor de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="41383-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="41383-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="41383-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="41383-161">Afhankelijkheden installeren</span><span class="sxs-lookup"><span data-stu-id="41383-161">Install dependencies</span></span>

<span data-ttu-id="41383-162">Hier installeren we de afhankelijkheden.</span><span class="sxs-lookup"><span data-stu-id="41383-162">Here we install the dependencies.</span></span> <span data-ttu-id="41383-163">Voer de volgende opdrachten uit: cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="41383-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="41383-164">In dit project worden twee knooppuntmodules gebruikt:</span><span class="sxs-lookup"><span data-stu-id="41383-164">This project used 2 node modules:</span></span>

* [<span data-ttu-id="41383-165">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="41383-165">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="41383-166">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="41383-166">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="41383-167">De webtoepassing publiceren in Azure</span><span class="sxs-lookup"><span data-stu-id="41383-167">Publish the web application to Azure</span></span>

<span data-ttu-id="41383-168">Hieronder vindt u de paar stappen die moeten worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="41383-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="41383-169">In de eerste stap wordt een plan voor een [Azure App Service](https://azure.microsoft.com/services/app-service/) gemaakt.</span><span class="sxs-lookup"><span data-stu-id="41383-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="41383-170">In dit plan kunt u meerdere web-apps opslaan.</span><span class="sxs-lookup"><span data-stu-id="41383-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="41383-171">Hierna maken we een web-app.</span><span class="sxs-lookup"><span data-stu-id="41383-171">Next we create a web app.</span></span> <span data-ttu-id="41383-172">Vervang in het volgende voorbeeld <app_name> door een globaal unieke naam (geldige tekens zijn a-z, 0-9 en -).</span><span class="sxs-lookup"><span data-stu-id="41383-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="41383-173">De runtime wordt ingesteld op NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="41383-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="41383-174">Voer az webapp list-runtimes uit om alle ondersteunde runtimes te bekijken</span><span class="sxs-lookup"><span data-stu-id="41383-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="41383-175">Wanneer de web-app is gemaakt, wordt met Azure CLI uitvoer weergegeven die lijkt op het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="41383-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="41383-176">Blader naar de pas gemaakte web-app. U ziet een werkende web-app.</span><span class="sxs-lookup"><span data-stu-id="41383-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="41383-177">Vervang <app-name> door een unieke app-naam.</span><span class="sxs-lookup"><span data-stu-id="41383-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="41383-178">Met de bovenstaande opdracht wordt ook een app gemaakt waarvoor Git is ingeschakeld, waarmee u vanuit de lokale Git kunt implementeren in Azure.</span><span class="sxs-lookup"><span data-stu-id="41383-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="41383-179">De lokale Git wordt geconfigureerd met de volgende URL: https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git</span><span class="sxs-lookup"><span data-stu-id="41383-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="41383-180">Maak een implementatiegebruiker. Als de vorige opdracht is uitgevoerd, kunt u een externe Azure-instantie toevoegen aan de lokale Git-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="41383-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="41383-181">Vervang <url> door de URL van de externe Git-instantie die u hebt verkregen bij Git inschakelen voor uw app.</span><span class="sxs-lookup"><span data-stu-id="41383-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="41383-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-182">::: zone-end</span></span>

<span data-ttu-id="41383-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="41383-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="41383-184">De oplossing openen en bewerken</span><span class="sxs-lookup"><span data-stu-id="41383-184">Open and edit the solution</span></span>

<span data-ttu-id="41383-185">Bewerk het bestand program.cs om het voorbeeld uit te voeren met de naam van uw specifieke sleutelkluis:</span><span class="sxs-lookup"><span data-stu-id="41383-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="41383-186">Ga naar de map key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="41383-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="41383-187">Open het bestand key-vault-dotnet-core-quickstart.sln in Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="41383-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="41383-188">Open het bestand Program.cs en vervang de tijdelijke aanduiding *YourKeyVaultName* door de naam van de sleutelkluis die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="41383-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="41383-189">Deze oplossing maakt gebruik van de NuGet-bibliotheken [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) en [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="41383-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="41383-190">De app uitvoeren</span><span class="sxs-lookup"><span data-stu-id="41383-190">Run the app</span></span>

<span data-ttu-id="41383-191">Selecteer **Fouten opsporen** > **Starten** zonder foutopsporing in het hoofdmenu van Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="41383-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="41383-192">Wanneer de browser wordt weergegeven, gaat u naar de pagina **Over**.</span><span class="sxs-lookup"><span data-stu-id="41383-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="41383-193">U ziet nu de waarde voor **AppGeheim**.</span><span class="sxs-lookup"><span data-stu-id="41383-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="41383-194">De webtoepassing publiceren in Azure</span><span class="sxs-lookup"><span data-stu-id="41383-194">Publish the web application to Azure</span></span>

<span data-ttu-id="41383-195">Publiceer de app in Azure om deze live als web-app in actie te zien en om te controleren of u de geheime waarde kunt ophalen:</span><span class="sxs-lookup"><span data-stu-id="41383-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="41383-196">Selecteer in Visual Studio het project **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="41383-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="41383-197">Selecteer **Publiceren** > **Start**.</span><span class="sxs-lookup"><span data-stu-id="41383-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="41383-198">Maak een nieuwe **App Service** en selecteer vervolgens **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="41383-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="41383-199">Wijzig de naam van de app in **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="41383-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="41383-200">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="41383-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="41383-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="41383-202">Beheerde service-identiteiten inschakelen</span><span class="sxs-lookup"><span data-stu-id="41383-202">Enable managed service identities</span></span>

<span data-ttu-id="41383-203">Azure Key Vault biedt een manier voor het veilig opslaan van referenties en andere sleutels en geheimen, maar uw code moet worden geverifieerd in Azure Key Vault om deze referenties op te halen.</span><span class="sxs-lookup"><span data-stu-id="41383-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="41383-204">Met Managed Service Identity wordt dit eenvoudiger doordat Azure-services zijn voorzien van een automatisch beheerde identiteit in Azure AD (Azure Active Directory).</span><span class="sxs-lookup"><span data-stu-id="41383-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="41383-205">U kunt deze identiteit gebruiken voor verificatie bij alle services die ondersteuning bieden voor Azure AD-verificatie, inclusief Key Vault, zonder dat u referenties in uw code hoeft te hebben.</span><span class="sxs-lookup"><span data-stu-id="41383-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="41383-206">Ga terug naar Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="41383-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="41383-207">Voer de opdracht assign-identity uit om de identiteit voor deze toepassing te maken:</span><span class="sxs-lookup"><span data-stu-id="41383-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="41383-208">De opdracht in deze procedure komt overeen met naar de portal gaan en **Managed Service Identity** in de eigenschappen van de webtoepassing instellen op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="41383-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="41383-209">Machtigingen toewijzen aan de toepassing om geheimen in Key Vault te lezen</span><span class="sxs-lookup"><span data-stu-id="41383-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="41383-210">Maak een notitie van de uitvoer wanneer u de toepassing publiceert in Azure.</span><span class="sxs-lookup"><span data-stu-id="41383-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="41383-211">Gebruik hierbij de notatie:</span><span class="sxs-lookup"><span data-stu-id="41383-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="41383-212">Voer deze opdracht uit met de naam van uw sleutelkluis en de waarde **PrincipalId**:</span><span class="sxs-lookup"><span data-stu-id="41383-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="41383-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="41383-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="41383-214">De Node-app implementeren in Azure en de geheime waarde ophalen</span><span class="sxs-lookup"><span data-stu-id="41383-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="41383-215">Nu alles is ingesteld,</span><span class="sxs-lookup"><span data-stu-id="41383-215">Now that everything is set.</span></span> <span data-ttu-id="41383-216">voert u de volgende opdracht uit om de app te implementeren in Azure</span><span class="sxs-lookup"><span data-stu-id="41383-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="41383-217">Als u hierna naar https://<app_name>.azurewebsites.net bladert, ziet u de geheime waarde.</span><span class="sxs-lookup"><span data-stu-id="41383-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="41383-218">Controleer of u de naam <YourKeyVaultName> hebt vervangen door de naam van de kluis</span><span class="sxs-lookup"><span data-stu-id="41383-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="41383-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-219">::: zone-end</span></span>

<span data-ttu-id="41383-220">::: zone pivot="dotnet" Tijdens het uitvoeren van de toepassing ziet u nu de geheime waarde die is opgehaald.</span><span class="sxs-lookup"><span data-stu-id="41383-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="41383-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="41383-222">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="41383-222">Next steps</span></span>

<span data-ttu-id="41383-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="41383-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="41383-224">Startpagina van Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="41383-225">Documentatie voor Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="41383-226">Azure SDK voor Node</span><span class="sxs-lookup"><span data-stu-id="41383-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="41383-227">[Azure REST API-verwijzing](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="41383-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="41383-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="41383-229">Startpagina van Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="41383-230">Documentatie voor Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="41383-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="41383-231">Azure-SDK voor .NET</span><span class="sxs-lookup"><span data-stu-id="41383-231">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="41383-232">[Azure REST API-naslaginformatie](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="41383-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
