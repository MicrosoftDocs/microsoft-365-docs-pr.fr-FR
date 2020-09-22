---
title: Créer une application pour accéder à la protection contre les menaces Microsoft sans utilisateur
description: Découvrez comment créer une application pour accéder à la protection contre les menaces Microsoft sans utilisateur
keywords: application, Access, API, Create
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
ms.openlocfilehash: 57ba0eb77ccb855cc0c0224b5321f11809e21ae8
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201418"
---
# <a name="create-an-app-to-access-microsoft-threat-protection-without-a-user"></a><span data-ttu-id="c5d1d-104">Créer une application pour accéder à la protection contre les menaces Microsoft sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="c5d1d-104">Create an app to access Microsoft Threat Protection without a user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c5d1d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c5d1d-105">**Applies to:**</span></span>
- <span data-ttu-id="c5d1d-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c5d1d-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="c5d1d-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c5d1d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="c5d1d-109">Cette page explique comment créer une application pour accéder par programme à la protection de Microsoft contre les menaces sans utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-109">This page describes how to create an application to get programmatic access to Microsoft Threat Protection without a user.</span></span> <span data-ttu-id="c5d1d-110">Si vous avez besoin d’un accès par programme à Microsoft Threat Protection au nom d’un utilisateur, reportez-vous à la rubrique [Get Access with User Context](api-create-app-user-context.md).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-110">If you need programmatic access to Microsoft Threat Protection on behalf of a user, see [Get access with user context](api-create-app-user-context.md).</span></span> <span data-ttu-id="c5d1d-111">Si vous n’êtes pas certain de l’accès dont vous avez besoin, consultez la rubrique [prise en main](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-111">If you are not sure which access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="c5d1d-112">La protection contre les menaces Microsoft expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-112">Microsoft Threat Protection exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="c5d1d-113">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-113">Those APIs will help you automate work flows and innovate based on Microsoft Threat Protection capabilities.</span></span> <span data-ttu-id="c5d1d-114">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-114">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="c5d1d-115">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="c5d1d-116">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-116">In general, you'll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="c5d1d-117">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-117">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="c5d1d-118">Obtenir un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-118">Get an access token using this application.</span></span>
- <span data-ttu-id="c5d1d-119">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-119">Use the token to access Microsoft Threat Protection API.</span></span>

<span data-ttu-id="c5d1d-120">Cet article explique comment créer une application Azure AD, obtenir un jeton d’accès à Microsoft Threat Protection et valider le jeton.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-120">This article explains how to create an Azure AD application, get an access token to Microsoft Threat Protection, and validate the token.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="c5d1d-121">Créer une application</span><span class="sxs-lookup"><span data-stu-id="c5d1d-121">Create an app</span></span>

1. <span data-ttu-id="c5d1d-122">Connectez-vous à [Azure](https://portal.azure.com) avec un utilisateur disposant du rôle d' **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="c5d1d-122">Log on to [Azure](https://portal.azure.com) with a user that has the **Global Administrator** role.</span></span>

2. <span data-ttu-id="c5d1d-123">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-123">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="c5d1d-125">Dans le formulaire d’inscription, choisissez un nom pour votre application, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-125">In the registration form, choose a name for your application, and then select **Register**.</span></span>

4. <span data-ttu-id="c5d1d-126">Pour permettre à votre application d’accéder à la protection contre les menaces Microsoft et de lui attribuer des autorisations, dans la page de votre application, sélectionnez autorisations de l' **API**  >  **Ajouter**une  >  **API mon organisation utilise** des >, tapez **protection Microsoft contre les menaces**, puis sélectionnez **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-126">To enable your app to access Microsoft Threat Protection and assign it permissions, on your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and then select **Microsoft Threat Protection**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c5d1d-127">La protection contre les menaces Microsoft ne s’affiche pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-127">Microsoft Threat Protection does not appear in the original list.</span></span> <span data-ttu-id="c5d1d-128">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-128">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/apis-in-my-org-tab.PNG)

   - <span data-ttu-id="c5d1d-130">Sélectionnez **autorisations d’Application** > choisissez les autorisations appropriées pour votre scénario, par exemple, **incident. Read. All**, puis sélectionnez **Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-130">Select **Application permissions** > Choose the relevant permissions for your scenario, e.g. **Incident.Read.All**, and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions.PNG)

    >[!NOTE]
    ><span data-ttu-id="c5d1d-132">Vous devez sélectionner les autorisations appropriées pour votre scénario, **« lire tous les incidents »** est un exemple.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-132">You need to select the relevant permissions for your scenario, **'Read all incidents'** is just an example.</span></span> <span data-ttu-id="c5d1d-133">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-133">To determine which permission you need, please look at the **Permissions** section in the API you are interested to call.</span></span>

5. <span data-ttu-id="c5d1d-134">Sélectionnez **accorder le consentement**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-134">Select **Grant consent**.</span></span>

     > [!NOTE]
     > <span data-ttu-id="c5d1d-135">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner **accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-135">Every time you add a permission, you must select **Grant consent** for the new permission to take effect.</span></span>

    ![Image des autorisations accorder](../../media/grant-consent.PNG)

6. <span data-ttu-id="c5d1d-137">Pour ajouter une clé secrète à l’application, sélectionnez **certificats & secrets**, ajoutez une description à la clé secrète, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-137">To add a secret to the application, select **Certificates & secrets**, add a description to the secret, and then select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c5d1d-138">Une fois que vous avez sélectionné **Ajouter**, sélectionnez **copier la valeur secrète générée**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-138">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="c5d1d-139">Vous ne pourrez pas récupérer cette valeur une fois que vous aurez quitté.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-139">You won't be able to retrieve this value after you leave.</span></span>

    ![Image de la clé créer une application](../../media/webapp-create-key2.png)

7. <span data-ttu-id="c5d1d-141">Notez l’ID de votre application et votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-141">Write down your application ID and your tenant ID.</span></span> <span data-ttu-id="c5d1d-142">Sur la page de votre application, accédez à **vue d’ensemble** et copiez ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-142">On your application page, go to **Overview** and copy the following.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

8. <span data-ttu-id="c5d1d-144">**Pour les partenaires de protection contre les menaces Microsoft uniquement**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-144">**For Microsoft Threat Protection Partners only**.</span></span> <span data-ttu-id="c5d1d-145">[Suivez les instructions ci-dessous](https://docs.microsoft.com/microsoft-365/security/mtp/api-partner-access).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-145">[Follow the instructions here](https://docs.microsoft.com/microsoft-365/security/mtp/api-partner-access).</span></span> <span data-ttu-id="c5d1d-146">Configurez votre application de sorte qu’elle soit multi-locataire (disponible dans tous les clients après consentement).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-146">Set your app to be multi-tenanted (available in all tenants after consent).</span></span> <span data-ttu-id="c5d1d-147">Cette condition est **requise** pour les applications tierces (par exemple, si vous créez une application conçue pour s’exécuter dans le client de plusieurs clients).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-147">This is **required** for third-party apps (for example, if you create an app that is intended to run in multiple customers' tenant).</span></span> <span data-ttu-id="c5d1d-148">Cette opération n’est **pas nécessaire** si vous créez un service que vous souhaitez exécuter uniquement dans votre client (par exemple, si vous créez une application pour votre propre utilisation qui interagira uniquement avec vos propres données).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-148">This is **not required** if you create a service that you want to run in your tenant only (for example, if you create an application for your own usage that will only interact with your own data).</span></span> <span data-ttu-id="c5d1d-149">Pour configurer votre application pour qu’elle soit mutualisée :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-149">To set your app to be multi-tenanted:</span></span>

    - <span data-ttu-id="c5d1d-150">Accédez à **authentification**et ajoutez https://portal.azure.com en tant qu' **URI de redirection**.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-150">Go to **Authentication**, and add https://portal.azure.com as the **Redirect URI**.</span></span>

    - <span data-ttu-id="c5d1d-151">En bas de la page, sous **types de comptes pris en charge**, sélectionnez les **comptes dans n’importe quel consentement d’application d’annuaire d’organisation** pour votre application mutualisée.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-151">On the bottom of the page, under **Supported account types**, select the **Accounts in any organizational directory** application consent for your multi-tenant app.</span></span>

    <span data-ttu-id="c5d1d-152">Vous avez besoin que votre application soit approuvée dans chaque client où vous avez l’intention de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-152">You need your application to be approved in each tenant where you intend to use it.</span></span> <span data-ttu-id="c5d1d-153">Cela est dû au fait que votre application interagit avec Microsoft Threat Protection au nom de votre client.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-153">This is because your application interacts Microsoft Threat Protection on behalf of your customer.</span></span>

    <span data-ttu-id="c5d1d-154">Vous (ou votre client si vous rédigez une application tierce) devez sélectionner le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-154">You (or your customer if you are writing a third-party app) need to select the consent link and approve your app.</span></span> <span data-ttu-id="c5d1d-155">L’autorisation doit être faite avec un utilisateur disposant de privilèges d’administrateur dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-155">The consent should be done with a user who has administrative privileges in Active Directory.</span></span>

    <span data-ttu-id="c5d1d-156">Le lien de consentement est formé comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-156">The consent link is formed as follows:</span></span> 

    ```
    https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=00000000-0000-0000-0000-000000000000&response_type=code&sso_reload=true
    ```

    <span data-ttu-id="c5d1d-157">Où 00000000-0000-0000-0000-000000000000 est remplacé par votre ID d’application.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-157">Where 00000000-0000-0000-0000-000000000000 is replaced with your application ID.</span></span>


<span data-ttu-id="c5d1d-158">**Terminé!**</span><span class="sxs-lookup"><span data-stu-id="c5d1d-158">**Done!**</span></span> <span data-ttu-id="c5d1d-159">Vous avez correctement inscrit une application !</span><span class="sxs-lookup"><span data-stu-id="c5d1d-159">You have successfully registered an application!</span></span> <span data-ttu-id="c5d1d-160">Voir des exemples ci-dessous pour l’acquisition et la validation de jetons.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-160">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="c5d1d-161">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="c5d1d-161">Get an access token</span></span>

<span data-ttu-id="c5d1d-162">Pour plus d’informations sur les jetons Azure AD, consultez le [didacticiel Azure ad](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-162">For more details on Azure AD tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

### <a name="use-powershell"></a><span data-ttu-id="c5d1d-163">Utiliser PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5d1d-163">Use PowerShell</span></span>

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

### <a name="use-c"></a><span data-ttu-id="c5d1d-164">Utiliser C# :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-164">Use C#:</span></span>

<span data-ttu-id="c5d1d-165">Le code suivant a été testé avec NuGet Microsoft. IdentityModel. clients. ActiveDirectory 3.19.8.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-165">The following code was tested with Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span></span>

1. <span data-ttu-id="c5d1d-166">Créez une nouvelle application console.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-166">Create a new console application.</span></span>
1. <span data-ttu-id="c5d1d-167">Installez NuGet [Microsoft. IdentityModel. clients. ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-167">Install Nuget [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span></span>
1. <span data-ttu-id="c5d1d-168">Ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-168">Add the following:</span></span>

    ```
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

1. <span data-ttu-id="c5d1d-169">Copiez et collez le code suivant dans votre application (n’oubliez pas de mettre à jour les trois variables : ```tenantId, appId, appSecret``` ) :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-169">Copy and paste the following code in your app (don't forget to update the three variables: ```tenantId, appId, appSecret```):</span></span>

    ```
    string tenantId = "00000000-0000-0000-0000-000000000000"; // Paste your own tenant ID here
    string appId = "11111111-1111-1111-1111-111111111111"; // Paste your own app ID here
    string appSecret = "22222222-2222-2222-2222-222222222222"; // Paste your own app secret here for a test, and then store it in a safe place! 

    const string authority = "https://login.windows.net";
    const string wdatpResourceId = "https://api.security.microsoft.com";

    AuthenticationContext auth = new AuthenticationContext($"{authority}/{tenantId}/");
    ClientCredential clientCredential = new ClientCredential(appId, appSecret);
    AuthenticationResult authenticationResult = auth.AcquireTokenAsync(wdatpResourceId, clientCredential).GetAwaiter().GetResult();
    string token = authenticationResult.AccessToken;
    ```


### <a name="use-python"></a><span data-ttu-id="c5d1d-170">Utiliser python</span><span class="sxs-lookup"><span data-stu-id="c5d1d-170">Use Python</span></span> 

```
import json
import urllib.request
import urllib.parse

tenantId = '00000000-0000-0000-0000-000000000000' # Paste your own tenant ID here
appId = '11111111-1111-1111-1111-111111111111' # Paste your own app ID here
appSecret = '22222222-2222-2222-2222-222222222222' # Paste your own app secret here

url = "https://login.windows.net/%s/oauth2/token" % (tenantId)

resourceAppIdUri = 'https://api.securitycenter.windows.com'

body = {
    'resource' : resourceAppIdUri,
    'client_id' : appId,
    'client_secret' : appSecret,
    'grant_type' : 'client_credentials'
}

data = urllib.parse.urlencode(body).encode("utf-8")

req = urllib.request.Request(url, data)
response = urllib.request.urlopen(req)
jsonResponse = json.loads(response.read())
aadToken = jsonResponse["access_token"]
```
### <a name="use-curl"></a><span data-ttu-id="c5d1d-171">Utilisation de la boucle</span><span class="sxs-lookup"><span data-stu-id="c5d1d-171">Use Curl</span></span>

> [!NOTE]
> <span data-ttu-id="c5d1d-172">La procédure suivante part du principe que la boucle pour Windows est déjà installée sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-172">The following procedure assumes that Curl for Windows is already installed on your computer.</span></span>

1. <span data-ttu-id="c5d1d-173">Ouvrez une invite de commandes et définissez CLIENT_ID à votre ID d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-173">Open a command prompt, and set CLIENT_ID to your Azure application ID.</span></span>
1. <span data-ttu-id="c5d1d-174">Définissez CLIENT_SECRET à la clé secrète de votre application Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-174">Set CLIENT_SECRET to your Azure application secret.</span></span>
1. <span data-ttu-id="c5d1d-175">Définissez TENANT_ID sur l’ID de client Azure du client qui souhaite utiliser votre application pour accéder à la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-175">Set TENANT_ID to the Azure tenant ID of the customer that wants to use your app to access Microsoft Threat Protection.</span></span>
1. <span data-ttu-id="c5d1d-176">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-176">Run the following command:</span></span>

```
curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://securitycenter.onmicrosoft.com/windowsatpservice/.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
```

<span data-ttu-id="c5d1d-177">Vous obtiendrez une réponse sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-177">You will get an answer in the following form:</span></span>

```
{"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
```

## <a name="validate-the-token"></a><span data-ttu-id="c5d1d-178">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="c5d1d-178">Validate the token</span></span>

<span data-ttu-id="c5d1d-179">Assurez-vous que vous avez obtenu le bon jeton :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-179">Ensure that you got the correct token:</span></span>

1. <span data-ttu-id="c5d1d-180">Copiez et collez le jeton que vous avez reçu à l’étape précédente dans [JWT](https://jwt.ms) afin de le décoder.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-180">Copy and paste the token you got in the previous step into [JWT](https://jwt.ms) in order to decode it.</span></span>
1. <span data-ttu-id="c5d1d-181">Vérifiez que vous obtenez une revendication « Roles » avec les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-181">Validate that you get a 'roles' claim with the desired permissions</span></span>
1. <span data-ttu-id="c5d1d-182">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application avec ```Incidents.Read.All``` , ```Incidents.ReadWrite.All``` et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="c5d1d-182">In the following image, you can see a decoded token acquired from an app with ```Incidents.Read.All```, ```Incidents.ReadWrite.All``` and ```AdvancedHunting.Read.All``` permissions:</span></span>

![Image de la validation du jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-microsoft-threat-protection-api"></a><span data-ttu-id="c5d1d-184">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c5d1d-184">Use the token to access Microsoft Threat Protection API</span></span>

1. <span data-ttu-id="c5d1d-185">Choisissez l’API que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-185">Choose the API you want to use.</span></span> <span data-ttu-id="c5d1d-186">Pour plus d’informations, consultez la rubrique [API de protection contre les menaces Microsoft prises en charge](api-supported.md).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-186">For more information, see [Supported Microsoft Threat Protection APIs](api-supported.md).</span></span>

2. <span data-ttu-id="c5d1d-187">Définissez l’en-tête Authorization dans la requête HTTP que vous envoyez à « porteur {Token} » (porteur est le modèle d’autorisation).</span><span class="sxs-lookup"><span data-stu-id="c5d1d-187">Set the authorization header in the http request you send to "Bearer {token}" (Bearer is the authorization scheme).</span></span>

3. <span data-ttu-id="c5d1d-188">Le délai d’expiration du jeton est d’une heure.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-188">The expiration time of the token is one hour.</span></span> <span data-ttu-id="c5d1d-189">Vous pouvez envoyer plusieurs demandes avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-189">You can send more then one request with the same token.</span></span>

<span data-ttu-id="c5d1d-190">Voici un exemple d’envoi d’une demande pour obtenir une liste d’incidents **à l’aide de C#**:</span><span class="sxs-lookup"><span data-stu-id="c5d1d-190">The following is an example of sending a request to get a list of incidents **using C#**:</span></span> 

```
    var httpClient = new HttpClient();

    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();

    // Do something useful with the response
```

## <a name="related-topics"></a><span data-ttu-id="c5d1d-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d1d-191">Related topics</span></span>
- [<span data-ttu-id="c5d1d-192">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c5d1d-192">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
- [<span data-ttu-id="c5d1d-193">Accéder à la protection contre les menaces Microsoft avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="c5d1d-193">Access  Microsoft Threat Protection with application context</span></span>](api-create-app-web.md)
- [<span data-ttu-id="c5d1d-194">Accéder à la protection contre les menaces Microsoft avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="c5d1d-194">Access  Microsoft Threat Protection with user context</span></span>](api-create-app-user-context.md)
