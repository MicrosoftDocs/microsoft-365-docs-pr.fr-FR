---
title: Hello World pour l’API REST Microsoft 365 Defender
description: Découvrez comment créer une application et utiliser un jeton pour accéder aux API Microsoft 365 Defender
keywords: application, jeton, accès, aad, application, inscription d’application, powershell, script, administrateur général, autorisation, microsoft 365 defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: 66afa27d0fa7a092d3f9e9ed6c3b6abc6020cb8d
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49928377"
---
# <a name="hello-world-for-microsoft-365-defender-rest-api"></a><span data-ttu-id="ea184-104">Hello World pour l’API REST Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea184-104">Hello World for Microsoft 365 Defender REST API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="ea184-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ea184-105">**Applies to:**</span></span>

- <span data-ttu-id="ea184-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea184-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea184-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ea184-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ea184-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="ea184-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="get-incidents-using-a-simple-powershell-script"></a><span data-ttu-id="ea184-109">Obtenir des incidents à l’aide d’un script PowerShell simple</span><span class="sxs-lookup"><span data-stu-id="ea184-109">Get incidents using a simple PowerShell script</span></span>

<span data-ttu-id="ea184-110">La réalisation de ce projet doit prendre entre 5 et 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="ea184-110">It should take 5 to 10 minutes to complete this project.</span></span> <span data-ttu-id="ea184-111">Cette estimation de temps inclut l’inscription de l’application et l’application du code à partir de l’exemple de script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea184-111">This time estimate includes registering the application, and applying the code from the PowerShell sample script.</span></span>

### <a name="register-an-app-in-azure-active-directory"></a><span data-ttu-id="ea184-112">Inscrire une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea184-112">Register an app in Azure Active Directory</span></span>

1. <span data-ttu-id="ea184-113">Connectez-vous [à Azure](https://portal.azure.com) en tant qu’utilisateur avec le **rôle d’administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="ea184-113">Sign in to [Azure](https://portal.azure.com) as a user with the **Global administrator** role.</span></span>

2. <span data-ttu-id="ea184-114">Accédez **à Azure Active Directory** App  >  **registrations** New  >  **registration**.</span><span class="sxs-lookup"><span data-stu-id="ea184-114">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation vers l’inscription de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="ea184-116">Dans le formulaire d’inscription, choisissez un nom pour votre application, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ea184-116">In the registration form, choose a name for your application, then select **Register**.</span></span> <span data-ttu-id="ea184-117">La sélection d’un URI de redirection est facultative.</span><span class="sxs-lookup"><span data-stu-id="ea184-117">Selecting a redirect URI is optional.</span></span> <span data-ttu-id="ea184-118">Vous n’en aurez pas besoin pour compléter cet exemple.</span><span class="sxs-lookup"><span data-stu-id="ea184-118">You won't need one to complete this example.</span></span>

4. <span data-ttu-id="ea184-119">Dans la page de votre application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon organisation utilise >, tapez Protection Microsoft contre les menaces, puis sélectionnez  >    >   Protection **Microsoft contre les menaces.** </span><span class="sxs-lookup"><span data-stu-id="ea184-119">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="ea184-120">Votre application peut désormais accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="ea184-120">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="ea184-121">*Microsoft Threat Protection* est un ancien nom de Microsoft 365 Defender et n’apparaîtra pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="ea184-121">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="ea184-122">Vous devez commencer à écrire son nom dans la zone de texte pour qu’il apparaisse.</span><span class="sxs-lookup"><span data-stu-id="ea184-122">You need to start writing its name in the text box to see it appear.</span></span>
   <span data-ttu-id="ea184-123">![Image de la sélection des autorisations d’API](../../media/apis-in-my-org-tab.PNG)</span><span class="sxs-lookup"><span data-stu-id="ea184-123">![Image of API permission selection](../../media/apis-in-my-org-tab.PNG)</span></span>

   - <span data-ttu-id="ea184-124">Sélectionnez **Application permissions**  >  **Incident.Read.All** et **sélectionnez Ajouter des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="ea184-124">Choose **Application permissions** > **Incident.Read.All** and select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection d’API](../../media/request-api-permissions.PNG)

5. <span data-ttu-id="ea184-126">Sélectionnez **Accorder le consentement de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="ea184-126">Select **Grant admin consent**.</span></span> <span data-ttu-id="ea184-127">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner Accorder le **consentement de l’administrateur** pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="ea184-127">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

    ![Image de l’octroi d’autorisations](../../media/grant-consent.PNG)

6. <span data-ttu-id="ea184-129">Ajoutez un secret à l’application.</span><span class="sxs-lookup"><span data-stu-id="ea184-129">Add a secret to the application.</span></span> <span data-ttu-id="ea184-130">Select **Certificates & secrets,** add a description to the secret, then select **Add**.</span><span class="sxs-lookup"><span data-stu-id="ea184-130">Select **Certificates & secrets**, add a description to the secret, then select **Add**.</span></span>

    > [!TIP]
    > <span data-ttu-id="ea184-131">Après avoir sélectionné **Ajouter,** **sélectionnez copier la valeur de secret générée.**</span><span class="sxs-lookup"><span data-stu-id="ea184-131">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="ea184-132">Vous ne pourrez pas récupérer la valeur secrète après votre départ.</span><span class="sxs-lookup"><span data-stu-id="ea184-132">You won't be able to retrieve the secret value after you leave.</span></span>

    ![Image de la clé de création d’application](../../media/webapp-create-key2.png)

7. <span data-ttu-id="ea184-134">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="ea184-134">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="ea184-135">Ils sont répertoriés sous Vue **d’ensemble** sur la page de votre application.</span><span class="sxs-lookup"><span data-stu-id="ea184-135">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

### <a name="get-a-token-using-the-app-and-use-the-token-to-access-the-api"></a><span data-ttu-id="ea184-137">Obtenir un jeton à l’aide de l’application et utiliser le jeton pour accéder à l’API</span><span class="sxs-lookup"><span data-stu-id="ea184-137">Get a token using the app and use the token to access the API</span></span>

<span data-ttu-id="ea184-138">Pour plus d’informations sur les jetons Azure Active Directory, voir le [didacticiel Azure AD.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="ea184-138">For more information on Azure Active Directory tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea184-139">Bien que l’exemple de cette application de démonstration vous encourage à coller votre valeur secrète à des fins de test, vous ne devez jamais coder en dur des **secrets** dans une application en cours d’exécution en production.</span><span class="sxs-lookup"><span data-stu-id="ea184-139">Although the example in this demo app encourage you to paste in your secret value for testing purposes, you should **never hardcode secrets** into an application running in production.</span></span> <span data-ttu-id="ea184-140">Un tiers peut utiliser votre secret pour accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="ea184-140">A third party could use your secret to access resources.</span></span> <span data-ttu-id="ea184-141">Vous pouvez aider à sécuriser les secrets de votre application à l’aide [d’Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates).</span><span class="sxs-lookup"><span data-stu-id="ea184-141">You can help keep your app's secrets secure by using [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates).</span></span> <span data-ttu-id="ea184-142">Pour obtenir un exemple pratique de la façon dont vous pouvez protéger votre application, voir Gérer les secrets dans vos applications serveur avec [Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span><span class="sxs-lookup"><span data-stu-id="ea184-142">For a practical example of how you can protect your app, see [Manage secrets in your server apps with Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span></span>

1. <span data-ttu-id="ea184-143">Copiez le script ci-dessous et collez-le dans votre éditeur de texte favori.</span><span class="sxs-lookup"><span data-stu-id="ea184-143">Copy the script below and paste it into your favorite text editor.</span></span> <span data-ttu-id="ea184-144">Enregistrer sous **Get-Token.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ea184-144">Save as **Get-Token.ps1**.</span></span> <span data-ttu-id="ea184-145">Vous pouvez également exécuter le code tel quel dans PowerShell ISE, mais vous devez l’enregistrer, car nous devons l’exécuter à nouveau lorsque nous utiliserons le script d’extraction d’incident dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="ea184-145">You can also run the code as-is in PowerShell ISE, but you should save it, because we'll need to run it again when we use the incident-fetching script in the next section.</span></span>

    <span data-ttu-id="ea184-146">Ce script génère un jeton et l’enregistre dans le dossier de travail sous le *nom,Latest-token.txt*.</span><span class="sxs-lookup"><span data-stu-id="ea184-146">This script will generate a token and save it in the working folder under the name, *Latest-token.txt*.</span></span>

    ```PowerShell
    # This script gets the app context token and saves it to a file named "Latest-token.txt" under the current directory.
    # Paste in your tenant ID, client ID and app secret (App key).

    $tenantId = '' # Paste your directory (tenant) ID here
    $clientId = '' # Paste your application (client) ID here
    $appSecret = '' # # Paste your own app secret here to test, then store it in a safe place!

    $resourceAppIdUri = 'https://api.security.microsoft.com'
    $oAuthUri = "https://login.windows.net/$tenantId/oauth2/token"
    $authBody = [Ordered] @{
      resource = $resourceAppIdUri
      client_id = $clientId
      client_secret = $appSecret
      grant_type = 'client_credentials'
    }
    $authResponse = Invoke-RestMethod -Method Post -Uri $oAuthUri -Body $authBody -ErrorAction Stop
    $token = $authResponse.access_token
    Out-File -FilePath "./Latest-token.txt" -InputObject $token
    return $token
    ```

#### <a name="validate-the-token"></a><span data-ttu-id="ea184-147">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="ea184-147">Validate the token</span></span>

1. <span data-ttu-id="ea184-148">Copiez et collez le jeton que vous avez reçu dans [JWT](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="ea184-148">Copy and paste the token you received into [JWT](https://jwt.ms) to decode it.</span></span>
1. <span data-ttu-id="ea184-149">*JWT signifie* *JSON Web Token*.</span><span class="sxs-lookup"><span data-stu-id="ea184-149">*JWT* stands for *JSON Web Token*.</span></span> <span data-ttu-id="ea184-150">Le jeton décodé contient un certain nombre d’éléments ou de revendications au format JSON.</span><span class="sxs-lookup"><span data-stu-id="ea184-150">The decoded token will contain a number of JSON-formatted items or claims.</span></span> <span data-ttu-id="ea184-151">Assurez-vous que la revendication *de rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="ea184-151">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

    <span data-ttu-id="ea184-152">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec ```Incidents.Read.All``` ```Incidents.ReadWrite.All``` , et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="ea184-152">In the following image, you can see a decoded token acquired from an app, with ```Incidents.Read.All```, ```Incidents.ReadWrite.All```, and ```AdvancedHunting.Read.All``` permissions:</span></span>

    ![Image jwt.ms](../../media/api-jwt-ms.png)

### <a name="get-a-list-of-recent-incidents"></a><span data-ttu-id="ea184-154">Obtenir la liste des incidents récents</span><span class="sxs-lookup"><span data-stu-id="ea184-154">Get a list of recent incidents</span></span>

<span data-ttu-id="ea184-155">Le script ci-dessous utilise **Get-Token.ps1** pour accéder à l’API.</span><span class="sxs-lookup"><span data-stu-id="ea184-155">The script below will use **Get-Token.ps1** to access the API.</span></span> <span data-ttu-id="ea184-156">Il récupère ensuite la liste des incidents qui ont été mis à jour pour la dernière fois au cours des dernières 48 heures, puis enregistre la liste en tant que fichier JSON.</span><span class="sxs-lookup"><span data-stu-id="ea184-156">It then retrieves a list of incidents that were last updated within the past 48 hours, and saves the list as a JSON file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea184-157">Enregistrez ce script dans le dossier que vous avez **enregistréGet-Token.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ea184-157">Save this script in the same folder you saved **Get-Token.ps1**.</span></span>

```PowerShell
# This script returns incidents last updated within the past 48 hours.

$token = ./Get-Token.ps1

# Get incidents from the past 48 hours.
# The script may appear to fail if you don't have any incidents in that time frame.
$dateTime = (Get-Date).ToUniversalTime().AddHours(-48).ToString("o")

# This URL contains the type of query and the time filter we created above.
# Note that `$filter` does not refer to a local variable in our script --
# it's actually an OData operator and part of the API's syntax.
$url = "https://api.security.microsoft.com/api/incidents?$filter=lastUpdateTime+ge+$dateTime"

# Set the webrequest headers
$headers = @{
    'Content-Type' = 'application/json'
    'Accept' = 'application/json'
    'Authorization' = "Bearer $token"
}

# Send the request and get the results.
$response = Invoke-WebRequest -Method Get -Uri $url -Headers $headers -ErrorAction Stop

# Extract the incidents from the results.
$incidents =  ($response | ConvertFrom-Json).value | ConvertTo-Json -Depth 99

# Get a string containing the execution time. We concatenate that string to the name 
# of the output file to avoid overwriting the file on consecutive runs of the script.
$dateTimeForFileName = Get-Date -Format o | foreach {$_ -replace ":", "."}

# Save the result as json
$outputJsonPath = "./Latest Incidents $dateTimeForFileName.json"

Out-File -FilePath $outputJsonPath -InputObject $incidents
```

<span data-ttu-id="ea184-158">Vous avez terminé !</span><span class="sxs-lookup"><span data-stu-id="ea184-158">You're all done!</span></span> <span data-ttu-id="ea184-159">Vous avez réussi :</span><span class="sxs-lookup"><span data-stu-id="ea184-159">You've successfully:</span></span>

- <span data-ttu-id="ea184-160">Création et inscription d’une application.</span><span class="sxs-lookup"><span data-stu-id="ea184-160">Created and registered an application.</span></span>
- <span data-ttu-id="ea184-161">Autorisation accordée à cette application pour lire les alertes.</span><span class="sxs-lookup"><span data-stu-id="ea184-161">Granted permission for that application to read alerts.</span></span>
- <span data-ttu-id="ea184-162">Connecté à l’API.</span><span class="sxs-lookup"><span data-stu-id="ea184-162">Connected to the API.</span></span>
- <span data-ttu-id="ea184-163">Utilisé un script PowerShell pour renvoyer les incidents mis à jour au cours des dernières 48 heures.</span><span class="sxs-lookup"><span data-stu-id="ea184-163">Used a PowerShell script to return incidents updated in the past 48 hours.</span></span>

## <a name="related-articles"></a><span data-ttu-id="ea184-164">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ea184-164">Related articles</span></span>

- [<span data-ttu-id="ea184-165">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea184-165">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="ea184-166">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea184-166">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="ea184-167">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="ea184-167">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md)
- [<span data-ttu-id="ea184-168">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="ea184-168">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md)
- [<span data-ttu-id="ea184-169">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea184-169">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md)
- [<span data-ttu-id="ea184-170">Gérer les secrets dans vos applications serveur avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="ea184-170">Manage secrets in your server apps with Azure Key Vault</span></span>](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="ea184-171">Autorisation OAuth 2.0 pour la connexion de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="ea184-171">OAuth 2.0 Authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
