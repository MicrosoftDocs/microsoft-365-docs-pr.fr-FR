---
title: Hello World pour l’API REST Microsoft 365 Defender
description: Découvrez comment créer une application et utiliser un jeton pour accéder aux API Microsoft 365 Defender
keywords: application, jeton, Access, AAD, app, inscription de l’application, PowerShell, script, administrateur global, autorisation
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: bd4f7e5485d67cf74477900ae2cc5c77f1a6ee41
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844043"
---
# <a name="hello-world-for-microsoft-365-defender-rest-api"></a><span data-ttu-id="6d00a-104">Hello World pour l’API REST Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6d00a-104">Hello World for Microsoft 365 Defender REST API</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6d00a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6d00a-105">**Applies to:**</span></span>
- <span data-ttu-id="6d00a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6d00a-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="6d00a-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="6d00a-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d00a-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="6d00a-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="get-incidents-using-a-simple-powershell-script"></a><span data-ttu-id="6d00a-109">Obtenir des incidents à l’aide d’un script PowerShell simple</span><span class="sxs-lookup"><span data-stu-id="6d00a-109">Get incidents using a simple PowerShell script</span></span>

### <a name="how-long-it-takes-to-go-through-this-example"></a><span data-ttu-id="6d00a-110">Combien de temps faut-il pour suivre cet exemple ?</span><span class="sxs-lookup"><span data-stu-id="6d00a-110">How long it takes to go through this example?</span></span>
<span data-ttu-id="6d00a-111">Il faut seulement 5 minutes en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="6d00a-111">It only takes 5 minutes done in two steps:</span></span>
- <span data-ttu-id="6d00a-112">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="6d00a-112">Application registration</span></span>
- <span data-ttu-id="6d00a-113">Utiliser des exemples : nécessite uniquement une opération copier/coller d’un court script PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d00a-113">Use examples: only requires copy/paste of a short PowerShell script</span></span>

### <a name="do-i-need-a-permission-to-connect"></a><span data-ttu-id="6d00a-114">Ai-je besoin d’une autorisation pour se connecter ?</span><span class="sxs-lookup"><span data-stu-id="6d00a-114">Do I need a permission to connect?</span></span>
<span data-ttu-id="6d00a-115">Pour l’étape d’inscription de l’application, vous devez disposer d’un rôle d' **administrateur général** dans votre client Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6d00a-115">For the Application registration stage, you must have a **Global administrator** role in your Azure Active Directory (Azure AD) tenant.</span></span>

### <a name="step-1---create-an-app-in-azure-active-directory"></a><span data-ttu-id="6d00a-116">Étape 1 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d00a-116">Step 1 - Create an App in Azure Active Directory</span></span>

1. <span data-ttu-id="6d00a-117">Connectez-vous à [Azure](https://portal.azure.com) avec votre utilisateur d' **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="6d00a-117">Log on to [Azure](https://portal.azure.com) with your **Global administrator** user.</span></span>

2. <span data-ttu-id="6d00a-118">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-118">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="6d00a-120">Dans le formulaire d’inscription, choisissez un nom pour votre application, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-120">In the registration form, choose a name for your application and then select **Register**.</span></span>

4. <span data-ttu-id="6d00a-121">Autorisez votre application à accéder à Microsoft Defender pour le point de terminaison et attribuez-lui l’autorisation **lire tous les incidents** :</span><span class="sxs-lookup"><span data-stu-id="6d00a-121">Allow your Application to access Microsoft Defender for Endpoint and assign it **Read all incidents** permission:</span></span>

   - <span data-ttu-id="6d00a-122">Sur la page de votre application, sélectionnez **autorisations d’API**  >  **Ajouter une**  >  **API mon organisation utilise** > tapez **Microsoft 365 Defender** et sélectionnez sur **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-122">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** > type **Microsoft 365 Defender** and select on **Microsoft 365 Defender**.</span></span>

   >[!NOTE]
   ><span data-ttu-id="6d00a-123">Microsoft 365 Defender n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="6d00a-123">Microsoft 365 Defender does not appear in the original list.</span></span> <span data-ttu-id="6d00a-124">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="6d00a-124">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/apis-in-my-org-tab.PNG)

   - <span data-ttu-id="6d00a-126">Choose **application permissions**  >  **incident. Read. All** > Select on **Add permissions**</span><span class="sxs-lookup"><span data-stu-id="6d00a-126">Choose **Application permissions** > **Incident.Read.All** > Select on **Add permissions**</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions.PNG)

   >[!IMPORTANT]
   ><span data-ttu-id="6d00a-128">Vous devez sélectionner les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="6d00a-128">You need to select the relevant permissions.</span></span> 

     <span data-ttu-id="6d00a-129">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="6d00a-129">For instance,</span></span>

     - <span data-ttu-id="6d00a-130">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="6d00a-130">To determine which permission you need, please look at the **Permissions** section in the API you are interested to call.</span></span>

5. <span data-ttu-id="6d00a-131">Sélectionnez **accorder le consentement** de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="6d00a-131">Select **Grant admin consent**</span></span>

    - >[!NOTE]
      > <span data-ttu-id="6d00a-132">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner sur **accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="6d00a-132">Every time you add permission you must select on **Grant consent** for the new permission to take effect.</span></span>

    ![Image des autorisations accorder](../../media/grant-consent.PNG)

6. <span data-ttu-id="6d00a-134">Ajoutez un secret à l’application.</span><span class="sxs-lookup"><span data-stu-id="6d00a-134">Add a secret to the application.</span></span>

    - <span data-ttu-id="6d00a-135">Sélectionnez **certificats & secrets** , ajoutez une description à la clé secrète et sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-135">Select **Certificates & secrets** , add description to the secret and select **Add**.</span></span>

    >[!IMPORTANT]
    > <span data-ttu-id="6d00a-136">Après avoir sélectionné **Ajouter** , **Copiez la valeur secrète générée**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-136">After selecting **Add** , **copy the generated secret value**.</span></span> <span data-ttu-id="6d00a-137">Vous ne pourrez pas récupérer une fois que vous aurez quitté !</span><span class="sxs-lookup"><span data-stu-id="6d00a-137">You won't be able to retrieve after you leave!</span></span>

    ![Image de la clé créer une application](../../media/webapp-create-key2.png)

7. <span data-ttu-id="6d00a-139">Notez l’ID de votre application et votre ID de client :</span><span class="sxs-lookup"><span data-stu-id="6d00a-139">Write down your application ID and your tenant ID:</span></span>

   - <span data-ttu-id="6d00a-140">Sur la page de votre application, accédez à **vue d’ensemble** et copiez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d00a-140">On your application page, go to **Overview** and copy the following:</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)


<span data-ttu-id="6d00a-142">Terminé!</span><span class="sxs-lookup"><span data-stu-id="6d00a-142">Done!</span></span> <span data-ttu-id="6d00a-143">Vous avez correctement inscrit une application.</span><span class="sxs-lookup"><span data-stu-id="6d00a-143">You have successfully registered an application.</span></span>

### <a name="step-2---get-a-token-using-the-app-and-use-this-token-to-access-the-api"></a><span data-ttu-id="6d00a-144">Étape 2 : obtenir un jeton à l’aide de l’application et utiliser ce jeton pour accéder à l’API.</span><span class="sxs-lookup"><span data-stu-id="6d00a-144">Step 2 - Get a token using the App and use this token to access the API.</span></span>

-   <span data-ttu-id="6d00a-145">Copiez le script ci-dessous dans PowerShell ISE ou dans un éditeur de texte, et enregistrez-le sous le **Get-Token.ps1**</span><span class="sxs-lookup"><span data-stu-id="6d00a-145">Copy the script below to PowerShell ISE or to a text editor, and save it as " **Get-Token.ps1** "</span></span>
-   <span data-ttu-id="6d00a-146">L’exécution de ce script générera un jeton et l’enregistrera dans le dossier de travail sous le nom « **Latest-token.txt** ».</span><span class="sxs-lookup"><span data-stu-id="6d00a-146">Running this script will generate a token and will save it in the working folder under the name " **Latest-token.txt** ".</span></span>

```
# That code gets the App Context Token and save it to a file named "Latest-token.txt" under the current directory
# Paste below your Tenant ID, App ID and App Secret (App key).

$tenantId = '' ### Paste your tenant ID here
$appId = '' ### Paste your Application ID here
$appSecret = '' ### Paste your Application secret here

$resourceAppIdUri = 'https://api.security.microsoft.com'
$oAuthUri = "https://login.windows.net/$TenantId/oauth2/token"
$authBody = [Ordered] @{
    resource = "$resourceAppIdUri"
    client_id = "$appId"
    client_secret = "$appSecret"
    grant_type = 'client_credentials'
}
$authResponse = Invoke-RestMethod -Method Post -Uri $oAuthUri -Body $authBody -ErrorAction Stop
$token = $authResponse.access_token
Out-File -FilePath "./Latest-token.txt" -InputObject $token
return $token
```

-   <span data-ttu-id="6d00a-147">Vérification de la validité :</span><span class="sxs-lookup"><span data-stu-id="6d00a-147">Sanity Check:</span></span><br>
<span data-ttu-id="6d00a-148">Exécutez le script.</span><span class="sxs-lookup"><span data-stu-id="6d00a-148">Run the script.</span></span><br>
<span data-ttu-id="6d00a-149">Dans votre navigateur, accédez à : https://jwt.ms/</span><span class="sxs-lookup"><span data-stu-id="6d00a-149">In your browser go to: https://jwt.ms/</span></span> <br>
<span data-ttu-id="6d00a-150">Copiez le jeton (contenu du fichier Latest-token.txt).</span><span class="sxs-lookup"><span data-stu-id="6d00a-150">Copy the token (the content of the Latest-token.txt file).</span></span><br>
<span data-ttu-id="6d00a-151">Colle dans la zone supérieure.</span><span class="sxs-lookup"><span data-stu-id="6d00a-151">Paste in the top box.</span></span><br>
<span data-ttu-id="6d00a-152">Recherchez la section « rôles ».</span><span class="sxs-lookup"><span data-stu-id="6d00a-152">Look for the "roles" section.</span></span> <span data-ttu-id="6d00a-153">Recherchez le ```Incidents.Read.All``` rôle.</span><span class="sxs-lookup"><span data-stu-id="6d00a-153">Find the ```Incidents.Read.All``` role.</span></span><br>
<span data-ttu-id="6d00a-154">L’exemple ci-dessous provient d’une application qui possède ```Incidents.Read.All``` ```Incidents.ReadWrite.All``` les ```AdvancedHunting.Read.All``` autorisations et.</span><span class="sxs-lookup"><span data-stu-id="6d00a-154">The below example is from an app that has ```Incidents.Read.All```, ```Incidents.ReadWrite.All``` and ```AdvancedHunting.Read.All``` permissions.</span></span>

![Image jwt.ms](../../media/api-jwt-ms.png)

### <a name="lets-get-the-incidents"></a><span data-ttu-id="6d00a-156">Permet d’obtenir les incidents.</span><span class="sxs-lookup"><span data-stu-id="6d00a-156">Lets get the Incidents!</span></span>

-   <span data-ttu-id="6d00a-157">Le script ci-dessous utilisera **Get-Token.ps1** pour accéder à l’API et obtiendra la dernière mise à jour des incidents au cours des 48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="6d00a-157">The script below will use **Get-Token.ps1** to access the API and will get the incidents last updated in past 48 hours.</span></span>
-   <span data-ttu-id="6d00a-158">Enregistrez ce script dans le dossier dans lequel vous avez enregistré le script précédent **Get-Token.ps1**.</span><span class="sxs-lookup"><span data-stu-id="6d00a-158">Save this script in the same folder you saved the previous script **Get-Token.ps1**.</span></span> 
-   <span data-ttu-id="6d00a-159">Le script d’un fichier JSON avec les données dans le même dossier que les scripts.</span><span class="sxs-lookup"><span data-stu-id="6d00a-159">The script a json file with the data in the same folder as the scripts.</span></span>

```
# Returns Incidents last updated in the past 48 hours.

$token = ./Get-Token.ps1       #run the script Get-Token.ps1  - make sure you are running this script from the same folder of Get-Token.ps1

# Get Incidents from the last 48 hours. Make sure you have incidents in that time frame.
$dateTime = (Get-Date).ToUniversalTime().AddHours(-48).ToString("o")

# The URL contains the type of query and the time filter we created above
$url = "https://api.security.microsoft.com/api/incidents?$filter=lastUpdateTime+ge+$dateTime"

# Set the WebRequest headers
$headers = @{ 
    'Content-Type' = 'application/json'
    'Accept' = 'application/json'
    'Authorization' = "Bearer $token"
}

# Send the webrequest and get the results. 
$response = Invoke-WebRequest -Method Get -Uri $url -Headers $headers -ErrorAction Stop

# Extract the incidents from the results. 
$incidents =  ($response | ConvertFrom-Json).value | ConvertTo-Json -Depth 99

# Get string with the execution time. We concatenate that string to the output file to avoid overwrite the file
$dateTimeForFileName = Get-Date -Format o | foreach {$_ -replace ":", "."}    

# Save the result as json
$outputJsonPath = "./Latest Incidents $dateTimeForFileName.json"     

Out-File -FilePath $outputJsonPath -InputObject $incidents 
```

<span data-ttu-id="6d00a-160">Vous avez tous fini !</span><span class="sxs-lookup"><span data-stu-id="6d00a-160">You're all done!</span></span> <span data-ttu-id="6d00a-161">Vous venez d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d00a-161">You have just successfully:</span></span>
-   <span data-ttu-id="6d00a-162">Créé et inscrit et application</span><span class="sxs-lookup"><span data-stu-id="6d00a-162">Created and registered and application</span></span>
-   <span data-ttu-id="6d00a-163">Autorisation accordée à cette application pour lire les alertes</span><span class="sxs-lookup"><span data-stu-id="6d00a-163">Granted permission for that application to read alerts</span></span>
-   <span data-ttu-id="6d00a-164">Connexion de l’API</span><span class="sxs-lookup"><span data-stu-id="6d00a-164">Connected the API</span></span>
-   <span data-ttu-id="6d00a-165">Utilisation d’un script PowerShell pour renvoyer des incidents créés au cours des 48 dernières heures</span><span class="sxs-lookup"><span data-stu-id="6d00a-165">Used a PowerShell script to return incidents created in the past 48 hours</span></span>



## <a name="related-topic"></a><span data-ttu-id="6d00a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d00a-166">Related topic</span></span>
- [<span data-ttu-id="6d00a-167">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6d00a-167">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="6d00a-168">Accéder à Microsoft 365 Defender avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="6d00a-168">Access  Microsoft 365 Defender with application context</span></span>](api-create-app-web.md)
- [<span data-ttu-id="6d00a-169">Accéder à Microsoft 365 Defender avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="6d00a-169">Access  Microsoft 365 Defender with user context</span></span>](api-create-app-user-context.md)
