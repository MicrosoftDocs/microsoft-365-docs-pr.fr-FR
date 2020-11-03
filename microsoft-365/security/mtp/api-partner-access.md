---
title: Accès partenaire via les API Microsoft 365 Defender
description: Découvrez comment créer une application AAD pour accéder par programme à Microsoft 365 Defender au nom de vos clients
keywords: partenaire, Access, API, multi-locataire, consentement, jeton d’accès, application
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
ms.openlocfilehash: eb40d5d2d82f57be225515ad0aa566038397bbbd
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844983"
---
# <a name="partner-access-through-microsoft-365-defender-apis"></a><span data-ttu-id="9fc69-104">Accès partenaire via les API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9fc69-104">Partner access through Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="9fc69-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9fc69-105">**Applies to:**</span></span>
- <span data-ttu-id="9fc69-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9fc69-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="9fc69-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="9fc69-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9fc69-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="9fc69-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


<span data-ttu-id="9fc69-109">Cette page explique comment créer une application AAD pour accéder par programme à Microsoft 365 Defender au nom de vos clients.</span><span class="sxs-lookup"><span data-stu-id="9fc69-109">This page describes how to create an AAD application to get programmatic access to Microsoft 365 Defender on behalf of your customers.</span></span>

<span data-ttu-id="9fc69-110">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="9fc69-110">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="9fc69-111">Ces API vous aideront à automatiser les flux de travail et innoveront en fonction des fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="9fc69-111">Those APIs will help you automate work flows and innovate based on Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="9fc69-112">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="9fc69-112">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="9fc69-113">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="9fc69-113">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="9fc69-114">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="9fc69-114">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="9fc69-115">Créez une **application AAD mutualisée** .</span><span class="sxs-lookup"><span data-stu-id="9fc69-115">Create a **multi-tenant** AAD application.</span></span>
- <span data-ttu-id="9fc69-116">Obtenir l’autorisation de l’administrateur de votre client pour accéder aux ressources Microsoft 365 Defender dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="9fc69-116">Get authorized (consent) by your customer administrator for your application to access Microsoft 365 Defender resources it needs.</span></span>
- <span data-ttu-id="9fc69-117">Obtenir un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="9fc69-117">Get an access token using this application.</span></span>
- <span data-ttu-id="9fc69-118">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="9fc69-118">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="9fc69-119">Les étapes suivantes vous expliquent comment créer une application AAD, obtenir un jeton d’accès à Microsoft 365 Defender et valider le jeton.</span><span class="sxs-lookup"><span data-stu-id="9fc69-119">The following steps with guide you how to create an AAD application, get an access token to Microsoft 365 Defender and validate the token.</span></span>

## <a name="create-the-multi-tenant-app"></a><span data-ttu-id="9fc69-120">Créer l’application mutualisée</span><span class="sxs-lookup"><span data-stu-id="9fc69-120">Create the multi-tenant app</span></span>

1. <span data-ttu-id="9fc69-121">Ouvrez une session sur votre [client Azure](https://portal.azure.com) avec un utilisateur qui dispose du rôle d' **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="9fc69-121">Log on to your [Azure tenant](https://portal.azure.com) with user that has **Global Administrator** role.</span></span>

2. <span data-ttu-id="9fc69-122">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="9fc69-122">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="9fc69-124">Dans le formulaire d’inscription :</span><span class="sxs-lookup"><span data-stu-id="9fc69-124">In the registration form:</span></span>

    - <span data-ttu-id="9fc69-125">Choisissez un nom pour votre application.</span><span class="sxs-lookup"><span data-stu-id="9fc69-125">Choose a name for your application.</span></span>

    - <span data-ttu-id="9fc69-126">Types de comptes pris en charge-comptes dans n’importe quel annuaire d’organisation.</span><span class="sxs-lookup"><span data-stu-id="9fc69-126">Supported account types - accounts in any organizational directory.</span></span>

    - <span data-ttu-id="9fc69-127">URI de redirection-type : Web, URI : https://portal.azure.com</span><span class="sxs-lookup"><span data-stu-id="9fc69-127">Redirect URI - type: Web, URI: https://portal.azure.com</span></span>

    ![Image de l’inscription de l’application partenaire Microsoft Azure](../../media/atp-api-new-app-partner.png)


4. <span data-ttu-id="9fc69-129">Autorisez votre application à accéder à Microsoft 365 Defender et attribuez-lui le jeu d’autorisations minimal requis pour terminer l’intégration.</span><span class="sxs-lookup"><span data-stu-id="9fc69-129">Allow your Application to access Microsoft 365 Defender and assign it with the minimal set of permissions required to complete the integration.</span></span>

   - <span data-ttu-id="9fc69-130">Sur la page de votre application, cliquez sur autorisations de l' **API**  >  **Ajouter** une  >  **API que mon organisation utilise** > tapez **Microsoft 365 Defender** et cliquez sur **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="9fc69-130">On your application page, click **API Permissions** > **Add permission** > **APIs my organization uses** > type **Microsoft 365 Defender** and click on **Microsoft 365 Defender**.</span></span>

   >[!NOTE]
   ><span data-ttu-id="9fc69-131">Microsoft 365 Defender n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="9fc69-131">Microsoft 365 Defender does not appear in the original list.</span></span> <span data-ttu-id="9fc69-132">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="9fc69-132">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/apis-in-my-org-tab.PNG)
   
   ### <a name="request-api-permissions"></a><span data-ttu-id="9fc69-134">Demander des autorisations d’API</span><span class="sxs-lookup"><span data-stu-id="9fc69-134">Request API permissions</span></span>

   <span data-ttu-id="9fc69-135">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="9fc69-135">To determine which permission you need, please look at the **Permissions** section in the API you are interested to call.</span></span> 

   <span data-ttu-id="9fc69-136">Dans l’exemple suivant, nous allons utiliser l’autorisation **« lire tous les incidents »** :</span><span class="sxs-lookup"><span data-stu-id="9fc69-136">In the following example we will use **'Read all incidents'** permission:</span></span>

   <span data-ttu-id="9fc69-137">Choose **application permissions**  >  **incidents. Read. All** > cliquez sur **Ajouter des autorisations**</span><span class="sxs-lookup"><span data-stu-id="9fc69-137">Choose **Application permissions** > **Incidents.Read.All** > Click on **Add permissions**</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions.PNG)


5. <span data-ttu-id="9fc69-139">Cliquez sur **accorder le consentement**</span><span class="sxs-lookup"><span data-stu-id="9fc69-139">Click **Grant consent**</span></span>

    >[!NOTE]
    ><span data-ttu-id="9fc69-140">Chaque fois que vous ajoutez une autorisation, vous devez cliquer sur **accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="9fc69-140">Every time you add permission you must click on **Grant consent** for the new permission to take effect.</span></span>

    ![Image des autorisations accorder](../../media/grant-consent.PNG)

6. <span data-ttu-id="9fc69-142">Ajoutez un secret à l’application.</span><span class="sxs-lookup"><span data-stu-id="9fc69-142">Add a secret to the application.</span></span>

    - <span data-ttu-id="9fc69-143">Cliquez sur **certificats & secrets** , ajoutez une description à la clé secrète, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9fc69-143">Click **Certificates & secrets** , add description to the secret and click **Add**.</span></span>

    >[!IMPORTANT]
    > <span data-ttu-id="9fc69-144">Après avoir sélectionné **Ajouter** , **Copiez la valeur secrète générée**.</span><span class="sxs-lookup"><span data-stu-id="9fc69-144">After selecting **Add** , **copy the generated secret value**.</span></span> <span data-ttu-id="9fc69-145">Vous ne pourrez pas récupérer une fois que vous aurez quitté !</span><span class="sxs-lookup"><span data-stu-id="9fc69-145">You won't be able to retrieve after you leave!</span></span>

    ![Image de la clé créer une application](../../media/webapp-create-key2.png)

7. <span data-ttu-id="9fc69-147">Notez l’ID de votre application :</span><span class="sxs-lookup"><span data-stu-id="9fc69-147">Write down your application ID:</span></span>

   - <span data-ttu-id="9fc69-148">Sur la page de votre application, accédez à **vue d’ensemble** et copiez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9fc69-148">On your application page, go to **Overview** and copy the following:</span></span>

   ![Image de l’ID d’application créé](../../media/app-id.png)

8. <span data-ttu-id="9fc69-150">Ajoutez l’application au client de votre client.</span><span class="sxs-lookup"><span data-stu-id="9fc69-150">Add the application to your customer's tenant.</span></span>

    <span data-ttu-id="9fc69-151">Vous avez besoin que votre application soit approuvée dans chaque locataire client sur lequel vous envisagez de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9fc69-151">You need your application to be approved in each customer tenant where you intend to use it.</span></span> <span data-ttu-id="9fc69-152">Cela est dû au fait que votre application interagit avec l’application Microsoft 365 Defender au nom de votre client.</span><span class="sxs-lookup"><span data-stu-id="9fc69-152">This is because your application interacts with Microsoft 365 Defender application on behalf of your customer.</span></span>

    <span data-ttu-id="9fc69-153">Un utilisateur disposant d’un **administrateur général** du client de votre client doit cliquer sur le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="9fc69-153">A user with **Global Administrator** from your customer's tenant need to click the consent link and approve your application.</span></span>

    <span data-ttu-id="9fc69-154">Le lien de consentement est de la forme :</span><span class="sxs-lookup"><span data-stu-id="9fc69-154">Consent link is of the form:</span></span>

    ```
    https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=00000000-0000-0000-0000-000000000000&response_type=code&sso_reload=true
    ```

    <span data-ttu-id="9fc69-155">Où 00000000-0000-0000-0000-000000000000 doit être remplacé par l’ID de votre application</span><span class="sxs-lookup"><span data-stu-id="9fc69-155">Where 00000000-0000-0000-0000-000000000000 should be replaced with your Application ID</span></span>

    <span data-ttu-id="9fc69-156">Après avoir cliqué sur le lien de consentement, connectez-vous avec l’administrateur général du client du client et acceptez l’application.</span><span class="sxs-lookup"><span data-stu-id="9fc69-156">After clicking on the consent link, login with the Global Administrator of the customer's tenant and consent the application.</span></span>

    ![Image de consentement](../../media/app-consent-partner.png)

    <span data-ttu-id="9fc69-158">De plus, vous devrez demander à votre client son ID de client et l’enregistrer pour une utilisation ultérieure lors de l’acquisition du jeton.</span><span class="sxs-lookup"><span data-stu-id="9fc69-158">In addition, you will need to ask your customer for their tenant ID and save it for future use when acquiring the token.</span></span>

- <span data-ttu-id="9fc69-159">**Terminé!**</span><span class="sxs-lookup"><span data-stu-id="9fc69-159">**Done!**</span></span> <span data-ttu-id="9fc69-160">Vous avez correctement inscrit une application !</span><span class="sxs-lookup"><span data-stu-id="9fc69-160">You have successfully registered an application!</span></span> 
- <span data-ttu-id="9fc69-161">Voir des exemples ci-dessous pour l’acquisition et la validation de jetons.</span><span class="sxs-lookup"><span data-stu-id="9fc69-161">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token-examples"></a><span data-ttu-id="9fc69-162">Obtenir des exemples de jeton d’accès :</span><span class="sxs-lookup"><span data-stu-id="9fc69-162">Get an access token examples:</span></span>

>[!NOTE]
> <span data-ttu-id="9fc69-163">Pour obtenir un jeton d’accès au nom de votre client, utilisez l’ID de client du client sur les acquisitions de jetons suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fc69-163">To get access token on behalf of your customer, use the customer's tenant ID on the following token acquisitions.</span></span>

<br><span data-ttu-id="9fc69-164">Pour plus d’informations sur le jeton AAD, reportez-vous au [didacticiel AAD](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds) .</span><span class="sxs-lookup"><span data-stu-id="9fc69-164">For more details on AAD token, refer to [AAD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span></span>

### <a name="using-powershell"></a><span data-ttu-id="9fc69-165">Utiliser PowerShell</span><span class="sxs-lookup"><span data-stu-id="9fc69-165">Using PowerShell</span></span>

```
# That code gets the App Context Token and save it to a file named "Latest-token.txt" under the current directory
# Paste below your Tenant ID, App ID and App Secret (App key).

$tenantId = '' ### Paste your tenant ID here
$appId = '' ### Paste your Application ID here
$appSecret = '' ### Paste your Application key here

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

### <a name="using-c"></a><span data-ttu-id="9fc69-166">À l’aide de C# :</span><span class="sxs-lookup"><span data-stu-id="9fc69-166">Using C#:</span></span>

><span data-ttu-id="9fc69-167">Le code ci-dessous a été testé avec NuGet Microsoft. IdentityModel. clients. ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9fc69-167">The below code was tested with Nuget Microsoft.IdentityModel.Clients.ActiveDirectory</span></span>

- <span data-ttu-id="9fc69-168">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="9fc69-168">Create a new Console Application</span></span>
- <span data-ttu-id="9fc69-169">Installer NuGet [Microsoft. IdentityModel. clients. ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/)</span><span class="sxs-lookup"><span data-stu-id="9fc69-169">Install Nuget [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/)</span></span>
- <span data-ttu-id="9fc69-170">Ajoutez le suivant à l’aide de</span><span class="sxs-lookup"><span data-stu-id="9fc69-170">Add the below using</span></span>

    ```
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

- <span data-ttu-id="9fc69-171">Copiez/collez le code ci-dessous dans votre application (n’oubliez pas de mettre à jour les 3 variables : ```tenantId, appId, appSecret``` )</span><span class="sxs-lookup"><span data-stu-id="9fc69-171">Copy/Paste the below code in your application (do not forget to update the 3 variables: ```tenantId, appId, appSecret```)</span></span>

    ```
    string tenantId = "00000000-0000-0000-0000-000000000000"; // Paste your own tenant ID here
    string appId = "11111111-1111-1111-1111-111111111111"; // Paste your own app ID here
    string appSecret = "22222222-2222-2222-2222-222222222222"; // Paste your own app secret here for a test, and then store it in a safe place! 

    const string authority = "https://login.windows.net";
    const string mtpResourceId = "https://api.security.microsoft.com";

    AuthenticationContext auth = new AuthenticationContext($"{authority}/{tenantId}/");
    ClientCredential clientCredential = new ClientCredential(appId, appSecret);
    AuthenticationResult authenticationResult = auth.AcquireTokenAsync(mtpResourceId, clientCredential).GetAwaiter().GetResult();
    string token = authenticationResult.AccessToken;
    ```



### <a name="using-curl"></a><span data-ttu-id="9fc69-172">Utilisation de la boucle</span><span class="sxs-lookup"><span data-stu-id="9fc69-172">Using Curl</span></span>

> [!NOTE]
> <span data-ttu-id="9fc69-173">La procédure ci-dessous est censée boucler pour Windows est déjà installée sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9fc69-173">The below procedure supposed Curl for Windows is already installed on your computer</span></span>

- <span data-ttu-id="9fc69-174">Ouvrir une fenêtre de commande</span><span class="sxs-lookup"><span data-stu-id="9fc69-174">Open a command window</span></span>
- <span data-ttu-id="9fc69-175">Définir CLIENT_ID à votre ID d’application Azure</span><span class="sxs-lookup"><span data-stu-id="9fc69-175">Set CLIENT_ID to your Azure application ID</span></span>
- <span data-ttu-id="9fc69-176">Définir CLIENT_SECRET à votre code secret d’application Azure</span><span class="sxs-lookup"><span data-stu-id="9fc69-176">Set CLIENT_SECRET to your Azure application secret</span></span>
- <span data-ttu-id="9fc69-177">Définissez TENANT_ID sur l’ID de client Azure du client qui souhaite utiliser votre application pour accéder à l’application Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9fc69-177">Set TENANT_ID to the Azure tenant ID of the customer that wants to use your application to access Microsoft 365 Defender application</span></span>
- <span data-ttu-id="9fc69-178">Exécutez la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9fc69-178">Run the below command:</span></span>

```
curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://api.security.microsoft.com.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
```

<span data-ttu-id="9fc69-179">Vous obtiendrez une réponse du formulaire :</span><span class="sxs-lookup"><span data-stu-id="9fc69-179">You will get an answer of the form:</span></span>

```
{"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
```

## <a name="validate-the-token"></a><span data-ttu-id="9fc69-180">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="9fc69-180">Validate the token</span></span>

<span data-ttu-id="9fc69-181">Vérification de la santé pour vérifier que vous avez bien reçu un jeton correct :</span><span class="sxs-lookup"><span data-stu-id="9fc69-181">Sanity check to make sure you got a correct token:</span></span>

- <span data-ttu-id="9fc69-182">Copier/coller dans [JWT](https://jwt.ms) le jeton que vous obtenez à l’étape précédente afin de le décoder</span><span class="sxs-lookup"><span data-stu-id="9fc69-182">Copy/paste into [JWT](https://jwt.ms) the token you get in the previous step in order to decode it</span></span>
- <span data-ttu-id="9fc69-183">Vérifier que vous obtenez une revendication « Roles » avec les autorisations souhaitées</span><span class="sxs-lookup"><span data-stu-id="9fc69-183">Validate you get a 'roles' claim with the desired permissions</span></span>
- <span data-ttu-id="9fc69-184">Dans la capture d’écran ci-dessous, vous pouvez voir un jeton décodé acquis auprès d’une application avec plusieurs autorisations pour Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="9fc69-184">In the screenshot below, you can see a decoded token acquired from an Application with multiple permissions to Microsoft 365 Defender:</span></span>
- <span data-ttu-id="9fc69-185">La revendication « TID » est l’ID de client auquel appartient le jeton.</span><span class="sxs-lookup"><span data-stu-id="9fc69-185">The "tid" claim is the tenant ID the token belongs to.</span></span>

![Image de la validation du jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-microsoft-365-defender-api"></a><span data-ttu-id="9fc69-187">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9fc69-187">Use the token to access Microsoft 365 Defender API</span></span>

- <span data-ttu-id="9fc69-188">Sélectionnez l’API que vous souhaitez utiliser, pour plus d’informations, consultez la rubrique [Microsoft 365 Defender API pris en charge](api-supported.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc69-188">Choose the API you want to use, for more information, see [Supported Microsoft 365 Defender APIs](api-supported.md)</span></span>
- <span data-ttu-id="9fc69-189">Définissez l’en-tête Authorization dans la requête HTTP que vous envoyez à « porteur {Token} » (porteur est le modèle d’autorisation)</span><span class="sxs-lookup"><span data-stu-id="9fc69-189">Set the Authorization header in the Http request you send to "Bearer {token}" (Bearer is the Authorization scheme)</span></span>
- <span data-ttu-id="9fc69-190">Le délai d’expiration du jeton est de 1 heure (vous pouvez envoyer plusieurs demandes avec le même jeton)</span><span class="sxs-lookup"><span data-stu-id="9fc69-190">The Expiration time of the token is 1 hour (you can send more then one request with the same token)</span></span>

- <span data-ttu-id="9fc69-191">Exemple d’envoi d’une demande pour obtenir une liste d’incidents **à l’aide de C#**</span><span class="sxs-lookup"><span data-stu-id="9fc69-191">Example of sending a request to get a list of incidents **using C#**</span></span> 
    ```
    var httpClient = new HttpClient();

    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();

    // Do something useful with the response
    ```

## <a name="related-topics"></a><span data-ttu-id="9fc69-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fc69-192">Related topics</span></span> 

- [<span data-ttu-id="9fc69-193">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9fc69-193">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="9fc69-194">Accéder à Microsoft 365 Defender avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="9fc69-194">Access  Microsoft 365 Defender with application context</span></span>](api-create-app-web.md)
- [<span data-ttu-id="9fc69-195">Accéder à Microsoft 365 Defender avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="9fc69-195">Access  Microsoft 365 Defender with user context</span></span>](api-create-app-user-context.md)
