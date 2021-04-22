---
title: Hello World pour l'API Microsoft Defender pour point de terminaison
ms.reviewer: ''
description: Créez un appel d'API pratique de type « Hello World » à l'API Microsoft Defender for Endpoint.
keywords: api, api pris en charge, recherche avancée, requête
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f4571607181fc96d87934ff60801643f5969e7e9
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51929250"
---
# <a name="microsoft-defender-for-endpoint-api---hello-world"></a><span data-ttu-id="ff8ce-104">API Microsoft Defender pour point de terminaison - Hello World</span><span class="sxs-lookup"><span data-stu-id="ff8ce-104">Microsoft Defender for Endpoint API - Hello World</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ff8ce-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ff8ce-105">**Applies to:**</span></span> 
- [<span data-ttu-id="ff8ce-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ff8ce-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)


- <span data-ttu-id="ff8ce-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ff8ce-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ff8ce-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="get-alerts-using-a-simple-powershell-script"></a><span data-ttu-id="ff8ce-109">Obtenir des alertes à l'aide d'un script PowerShell simple</span><span class="sxs-lookup"><span data-stu-id="ff8ce-109">Get Alerts using a simple PowerShell script</span></span>

### <a name="how-long-it-takes-to-go-through-this-example"></a><span data-ttu-id="ff8ce-110">Combien de temps faut-il pour passer par cet exemple ?</span><span class="sxs-lookup"><span data-stu-id="ff8ce-110">How long it takes to go through this example?</span></span>
<span data-ttu-id="ff8ce-111">Cela ne prend que 5 minutes en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-111">It only takes 5 minutes done in two steps:</span></span>
- <span data-ttu-id="ff8ce-112">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="ff8ce-112">Application registration</span></span>
- <span data-ttu-id="ff8ce-113">Exemples : nécessite uniquement une copie/coller d'un court script PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff8ce-113">Use examples: only requires copy/paste of a short PowerShell script</span></span>

### <a name="do-i-need-a-permission-to-connect"></a><span data-ttu-id="ff8ce-114">Ai-je besoin d'une autorisation pour me connecter ?</span><span class="sxs-lookup"><span data-stu-id="ff8ce-114">Do I need a permission to connect?</span></span>
<span data-ttu-id="ff8ce-115">Pour l'étape d'inscription de l'application, vous devez avoir un rôle d'administrateur **général** dans votre client Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="ff8ce-115">For the Application registration stage, you must have a **Global administrator** role in your Azure Active Directory (Azure AD) tenant.</span></span>

### <a name="step-1---create-an-app-in-azure-active-directory"></a><span data-ttu-id="ff8ce-116">Étape 1 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ff8ce-116">Step 1 - Create an App in Azure Active Directory</span></span>

1. <span data-ttu-id="ff8ce-117">Connectez-vous [à Azure](https://portal.azure.com) avec votre **utilisateur administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-117">Log on to [Azure](https://portal.azure.com) with your **Global administrator** user.</span></span>

2. <span data-ttu-id="ff8ce-118">Accédez **à Azure Active Directory** App  >  **registrations** New  >  **registration**.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-118">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de Microsoft Azure et navigation vers l'inscription de l'application](images/atp-azure-new-app2.png)

3. <span data-ttu-id="ff8ce-120">Dans le formulaire d'inscription, choisissez un nom pour votre application, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="ff8ce-120">In the registration form, choose a name for your application and then click **Register**.</span></span>

4. <span data-ttu-id="ff8ce-121">Autorisez votre application à accéder à Defender pour endpoint et attribuez-lui **l'autorisation** « Lire toutes les alertes » :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-121">Allow your Application to access Defender for Endpoint and assign it **'Read all alerts'** permission:</span></span>

   - <span data-ttu-id="ff8ce-122">Dans la page de votre application, cliquez sur **Autorisations d'API** Ajouter des API d'autorisation que mon  >    >   organisation > **tapez WindowsDefenderATP** et cliquez sur **WindowsDefenderATP**.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-122">On your application page, click **API Permissions** > **Add permission** > **APIs my organization uses** > type **WindowsDefenderATP** and click on **WindowsDefenderATP**.</span></span>

   - <span data-ttu-id="ff8ce-123">**Remarque**: WindowsDefenderATP n'apparaît pas dans la liste d'origine.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-123">**Note**: WindowsDefenderATP does not appear in the original list.</span></span> <span data-ttu-id="ff8ce-124">Vous devez commencer à écrire son nom dans la zone de texte pour qu'il apparaisse.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-124">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de l'accès à l'API et de la sélection de l'API1](images/add-permission.png)

   - <span data-ttu-id="ff8ce-126">Choose **Application permissions**  >  **Alert.Read.All** > Click on **Add permissions**</span><span class="sxs-lookup"><span data-stu-id="ff8ce-126">Choose **Application permissions** > **Alert.Read.All** > Click on **Add permissions**</span></span>

   ![Image de l'accès à l'API et sélection de l'API2](images/application-permissions.png)

   <span data-ttu-id="ff8ce-128">**Remarque importante**: vous devez sélectionner les autorisations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-128">**Important note**: You need to select the relevant permissions.</span></span> <span data-ttu-id="ff8ce-129">« Lire toutes les alertes » n'est qu'un exemple !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-129">'Read All Alerts' is only an example!</span></span>

     <span data-ttu-id="ff8ce-130">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="ff8ce-130">For instance,</span></span>

     - <span data-ttu-id="ff8ce-131">Pour [exécuter des requêtes avancées,](run-advanced-query-api.md)sélectionnez l'autorisation « Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="ff8ce-131">To [run advanced queries](run-advanced-query-api.md), select 'Run advanced queries' permission</span></span>
     - <span data-ttu-id="ff8ce-132">Pour [isoler un ordinateur, sélectionnez](isolate-machine.md)l'autorisation « Isoler l'ordinateur »</span><span class="sxs-lookup"><span data-stu-id="ff8ce-132">To [isolate a machine](isolate-machine.md), select 'Isolate machine' permission</span></span>
     - <span data-ttu-id="ff8ce-133">Pour déterminer l'autorisation qui vous est nécessaire, consultez la section **Autorisations** de l'API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-133">To determine which permission you need, please look at the **Permissions** section in the API you are interested to call.</span></span>

5. <span data-ttu-id="ff8ce-134">Cliquez sur **Accorder le consentement**</span><span class="sxs-lookup"><span data-stu-id="ff8ce-134">Click **Grant consent**</span></span>

    - <span data-ttu-id="ff8ce-135">**Remarque**: chaque fois que vous ajoutez une autorisation, vous devez cliquer sur **Accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-135">**Note**: Every time you add permission you must click on **Grant consent** for the new permission to take effect.</span></span>

    ![Image de l'octroi d'autorisations](images/grant-consent.png)

6. <span data-ttu-id="ff8ce-137">Ajoutez un secret à l'application.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-137">Add a secret to the application.</span></span>

    - <span data-ttu-id="ff8ce-138">Cliquez **sur Certificats & secrets,** ajoutez une description à la secret, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-138">Click **Certificates & secrets**, add description to the secret and click **Add**.</span></span>

    <span data-ttu-id="ff8ce-139">**Important**: après avoir cliqué sur Ajouter, **copiez la valeur de secret générée.**</span><span class="sxs-lookup"><span data-stu-id="ff8ce-139">**Important**: After click Add, **copy the generated secret value**.</span></span> <span data-ttu-id="ff8ce-140">Vous ne pourrez plus récupérer une fois que vous êtes parti !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-140">You won't be able to retrieve after you leave!</span></span>

    ![Image de la clé de création d'application](images/webapp-create-key2.png)

7. <span data-ttu-id="ff8ce-142">Notez votre ID d'application et votre ID de client :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-142">Write down your application ID and your tenant ID:</span></span>

   - <span data-ttu-id="ff8ce-143">Dans la page de votre application, allez à **Vue d'ensemble** et copiez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-143">On your application page, go to **Overview** and copy the following:</span></span>

   ![Image de l'ID d'application créé](images/app-and-tenant-ids.png)


<span data-ttu-id="ff8ce-145">Terminé !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-145">Done!</span></span> <span data-ttu-id="ff8ce-146">Vous avez réussi à inscrire une application !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-146">You have successfully registered an application!</span></span>

### <a name="step-2---get-a-token-using-the-app-and-use-this-token-to-access-the-api"></a><span data-ttu-id="ff8ce-147">Étape 2 : obtenir un jeton à l'aide de l'application et utiliser ce jeton pour accéder à l'API.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-147">Step 2 - Get a token using the App and use this token to access the API.</span></span>

-   <span data-ttu-id="ff8ce-148">Copiez le script ci-dessous sur PowerShell ISE ou dans un éditeur de texte, puis enregistrez-le sous «**Get-Token.ps1**»</span><span class="sxs-lookup"><span data-stu-id="ff8ce-148">Copy the script below to PowerShell ISE or to a text editor, and save it as "**Get-Token.ps1**"</span></span>
-   <span data-ttu-id="ff8ce-149">L'exécution de ce script génère un jeton et l'enregistre dans le dossier de travail sous le nom **«Latest-token.txt**».</span><span class="sxs-lookup"><span data-stu-id="ff8ce-149">Running this script will generate a token and will save it in the working folder under the name "**Latest-token.txt**".</span></span>

```
# That code gets the App Context Token and save it to a file named "Latest-token.txt" under the current directory
# Paste below your Tenant ID, App ID and App Secret (App key).

$tenantId = '' ### Paste your tenant ID here
$appId = '' ### Paste your Application ID here
$appSecret = '' ### Paste your Application secret here

$resourceAppIdUri = 'https://api.securitycenter.microsoft.com'
$oAuthUri = "https://login.microsoftonline.com/$TenantId/oauth2/token"
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

-   <span data-ttu-id="ff8ce-150">Vérification de la sanité :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-150">Sanity Check:</span></span><br>
<span data-ttu-id="ff8ce-151">Exécutez le script.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-151">Run the script.</span></span><br>
<span data-ttu-id="ff8ce-152">Dans votre navigateur, allez à : https://jwt.ms/</span><span class="sxs-lookup"><span data-stu-id="ff8ce-152">In your browser go to: https://jwt.ms/</span></span> <br>
<span data-ttu-id="ff8ce-153">Copiez le jeton (le contenu du Latest-token.txt fichier).</span><span class="sxs-lookup"><span data-stu-id="ff8ce-153">Copy the token (the content of the Latest-token.txt file).</span></span><br>
<span data-ttu-id="ff8ce-154">Coller dans la zone supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-154">Paste in the top box.</span></span><br>
<span data-ttu-id="ff8ce-155">Recherchez la section « rôles ».</span><span class="sxs-lookup"><span data-stu-id="ff8ce-155">Look for the "roles" section.</span></span> <span data-ttu-id="ff8ce-156">Recherchez le rôle Alert.Read.All.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-156">Find the Alert.Read.All role.</span></span>

![Image jwt.ms](images/api-jwt-ms.png)

### <a name="lets-get-the-alerts"></a><span data-ttu-id="ff8ce-158">Permet d'obtenir les alertes !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-158">Lets get the Alerts!</span></span>

-   <span data-ttu-id="ff8ce-159">Le script ci-dessous utilise **Get-Token.ps1** pour accéder à l'API et reçoit les dernières alertes de 48 heures.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-159">The script below will use **Get-Token.ps1** to access the API and will get the past 48 hours Alerts.</span></span>
-   <span data-ttu-id="ff8ce-160">Enregistrez ce script dans le dossier que vous avez enregistré le script **précédentGet-Token.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-160">Save this script in the same folder you saved the previous script **Get-Token.ps1**.</span></span> 
-   <span data-ttu-id="ff8ce-161">Le script crée deux fichiers (json et csv) avec les données dans le même dossier que les scripts.</span><span class="sxs-lookup"><span data-stu-id="ff8ce-161">The script creates two files (json and csv) with the data in the same folder as the scripts.</span></span>

```
# Returns Alerts created in the past 48 hours.

$token = ./Get-Token.ps1       #run the script Get-Token.ps1  - make sure you are running this script from the same folder of Get-Token.ps1

# Get Alert from the last 48 hours. Make sure you have alerts in that time frame.
$dateTime = (Get-Date).ToUniversalTime().AddHours(-48).ToString("o")       

# The URL contains the type of query and the time filter we create above
# Read more about other query options and filters at   Https://TBD- add the documentation link
$url = "https://api.securitycenter.microsoft.com/api/alerts?`$filter=alertCreationTime ge $dateTime"

# Set the WebRequest headers
$headers = @{ 
    'Content-Type' = 'application/json'
    Accept = 'application/json'
    Authorization = "Bearer $token" 
}

# Send the webrequest and get the results. 
$response = Invoke-WebRequest -Method Get -Uri $url -Headers $headers -ErrorAction Stop

# Extract the alerts from the results. 
$alerts =  ($response | ConvertFrom-Json).value | ConvertTo-Json

# Get string with the execution time. We concatenate that string to the output file to avoid overwrite the file
$dateTimeForFileName = Get-Date -Format o | foreach {$_ -replace ":", "."}    

# Save the result as json and as csv
$outputJsonPath = "./Latest Alerts $dateTimeForFileName.json"     
$outputCsvPath = "./Latest Alerts $dateTimeForFileName.csv"

Out-File -FilePath $outputJsonPath -InputObject $alerts
($alerts | ConvertFrom-Json) | Export-CSV $outputCsvPath -NoTypeInformation 
```

<span data-ttu-id="ff8ce-162">Vous avez terminé !</span><span class="sxs-lookup"><span data-stu-id="ff8ce-162">You’re all done!</span></span> <span data-ttu-id="ff8ce-163">Vous avez réussi :</span><span class="sxs-lookup"><span data-stu-id="ff8ce-163">You have just successfully:</span></span>
-   <span data-ttu-id="ff8ce-164">Créé, inscrit et application</span><span class="sxs-lookup"><span data-stu-id="ff8ce-164">Created and registered and application</span></span>
-   <span data-ttu-id="ff8ce-165">Autorisation accordée à cette application pour lire les alertes</span><span class="sxs-lookup"><span data-stu-id="ff8ce-165">Granted permission for that application to read alerts</span></span>
-   <span data-ttu-id="ff8ce-166">Connecté à l'API</span><span class="sxs-lookup"><span data-stu-id="ff8ce-166">Connected the API</span></span>
-   <span data-ttu-id="ff8ce-167">Utilisation d'un script PowerShell pour renvoyer les alertes créées au cours des dernières 48 heures</span><span class="sxs-lookup"><span data-stu-id="ff8ce-167">Used a PowerShell script to return alerts created in the past 48 hours</span></span>



## <a name="related-topic"></a><span data-ttu-id="ff8ce-168">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="ff8ce-168">Related topic</span></span>
- [<span data-ttu-id="ff8ce-169">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ff8ce-169">Microsoft Defender for Endpoint APIs</span></span>](exposed-apis-list.md)
- [<span data-ttu-id="ff8ce-170">Accéder à Microsoft Defender pour le point de terminaison avec le contexte de l'application</span><span class="sxs-lookup"><span data-stu-id="ff8ce-170">Access Microsoft Defender for Endpoint with application context</span></span>](exposed-apis-create-app-webapp.md)
- [<span data-ttu-id="ff8ce-171">Accéder à Microsoft Defender pour le point de terminaison avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="ff8ce-171">Access Microsoft Defender for Endpoint with user context</span></span>](exposed-apis-create-app-nativeapp.md)
