---
title: Créer une application pour accéder à Microsoft Defender pour le point de terminaison sans utilisateur
ms.reviewer: ''
description: Découvrez comment concevoir une application web pour obtenir un accès par programmation à Microsoft Defender pour endpoint sans utilisateur.
keywords: api, api de graphique, api pris en charge, acteur, alertes, appareil, utilisateur, domaine, ip, fichier, recherche avancée, requête
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 2d78b7ea31c45220735a8579d728f9c0f7bda181
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842109"
---
# <a name="create-an-app-to-access-microsoft-defender-for-endpoint-without-a-user"></a><span data-ttu-id="d4222-104">Créer une application pour accéder à Microsoft Defender pour le point de terminaison sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4222-104">Create an app to access Microsoft Defender for Endpoint without a user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="d4222-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="d4222-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="d4222-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d4222-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d4222-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d4222-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="d4222-108">Cette page explique comment créer une application pour obtenir l’accès par programme à Defender for Endpoint sans utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4222-108">This page describes how to create an application to get programmatic access to Defender for Endpoint without a user.</span></span> <span data-ttu-id="d4222-109">Si vous avez besoin d’un accès par programme à Defender for Endpoint pour le compte d’un utilisateur, voir [Obtenir l’accès avec le contexte utilisateur.](exposed-apis-create-app-nativeapp.md)</span><span class="sxs-lookup"><span data-stu-id="d4222-109">If you need programmatic access to Defender for Endpoint on behalf of a user, see [Get access with user context](exposed-apis-create-app-nativeapp.md).</span></span> <span data-ttu-id="d4222-110">Si vous n’êtes pas sûr de l’accès dont vous avez besoin, [consultez La mise en place.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="d4222-110">If you are not sure which access you need, see [Get started](apis-intro.md).</span></span>

<span data-ttu-id="d4222-111">Microsoft Defender pour point de terminaison expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="d4222-111">Microsoft Defender for Endpoint exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="d4222-112">Ces API vous aideront à automatiser les flux de travail et à innover en fonction des fonctionnalités de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d4222-112">Those APIs will help you automate work flows and innovate based on Defender for Endpoint capabilities.</span></span> <span data-ttu-id="d4222-113">L’accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="d4222-113">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="d4222-114">Pour plus d’informations, [voir code d’autorisation OAuth 2.0 Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="d4222-114">For more information, see [OAuth 2.0 Authorization Code Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="d4222-115">En règle générale, vous devez suivre les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="d4222-115">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="d4222-116">Créez une Azure Active Directory application (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d4222-116">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="d4222-117">Obtenez un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="d4222-117">Get an access token using this application.</span></span>
- <span data-ttu-id="d4222-118">Utilisez le jeton pour accéder à l’API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d4222-118">Use the token to access Defender for Endpoint API.</span></span>

<span data-ttu-id="d4222-119">Cet article explique comment créer une application Azure AD, obtenir un jeton d’accès à Microsoft Defender pour le point de terminaison et valider le jeton.</span><span class="sxs-lookup"><span data-stu-id="d4222-119">This article explains how to create an Azure AD application, get an access token to Microsoft Defender for Endpoint, and validate the token.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="d4222-120">Créer une application</span><span class="sxs-lookup"><span data-stu-id="d4222-120">Create an app</span></span>

1. <span data-ttu-id="d4222-121">Connectez-vous [à Azure](https://portal.azure.com) avec un utilisateur qui a le **rôle Administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="d4222-121">Log on to [Azure](https://portal.azure.com) with a user that has the **Global Administrator** role.</span></span>

2. <span data-ttu-id="d4222-122">Accédez à **Azure Active Directory**  >  **Inscription de l’application Nouvelle**  >  **inscription.**</span><span class="sxs-lookup"><span data-stu-id="d4222-122">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de la Microsoft Azure et de la navigation vers l’inscription de l’application](images/atp-azure-new-app2.png)

3. <span data-ttu-id="d4222-124">Dans le formulaire d’inscription, choisissez un nom pour votre application, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d4222-124">In the registration form, choose a name for your application, and then select **Register**.</span></span>

4. <span data-ttu-id="d4222-125">Pour permettre à votre application d’accéder à Defender pour le point de terminaison et de lui attribuer l’autorisation « Lire toutes les **alertes** ». Sur votre page d’application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon organisation utilise  >    >   >, tapez **WindowsDefenderATP,** puis sélectionnez **WindowsDefenderATP**.</span><span class="sxs-lookup"><span data-stu-id="d4222-125">To enable your app to access Defender for Endpoint and assign it **'Read all alerts'** permission, on your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **WindowsDefenderATP**, and then select **WindowsDefenderATP**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d4222-126">*WindowsDefenderATP* n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="d4222-126">*WindowsDefenderATP* does not appear in the original list.</span></span> <span data-ttu-id="d4222-127">Commencez à écrire son nom dans la zone de texte pour le voir apparaître.</span><span class="sxs-lookup"><span data-stu-id="d4222-127">Start writing its name in the text box to see it appear.</span></span>

   ![ajouter une autorisation](images/add-permission.png)

   - <span data-ttu-id="d4222-129">Sélectionnez **Autorisations**  >  **d’application Alert.Read.All,** puis **sélectionnez Ajouter des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="d4222-129">Select **Application permissions** > **Alert.Read.All**, and then select **Add permissions**.</span></span>

   ![autorisation d’application](images/application-permissions.png)

     <span data-ttu-id="d4222-131">Vous devez sélectionner les autorisations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="d4222-131">You need to select the relevant permissions.</span></span> <span data-ttu-id="d4222-132">« Lire toutes les alertes » n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="d4222-132">'Read All Alerts' is only an example.</span></span> <span data-ttu-id="d4222-133">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d4222-133">For instance:</span></span>

     - <span data-ttu-id="d4222-134">Pour [exécuter des requêtes avancées,](run-advanced-query-api.md)sélectionnez l’autorisation « Exécuter des requêtes avancées ».</span><span class="sxs-lookup"><span data-stu-id="d4222-134">To [run advanced queries](run-advanced-query-api.md), select the 'Run advanced queries' permission.</span></span>
     - <span data-ttu-id="d4222-135">Pour [isoler un appareil,](isolate-machine.md)sélectionnez l’autorisation « Isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="d4222-135">To [isolate a device](isolate-machine.md), select the 'Isolate machine' permission.</span></span>
     - <span data-ttu-id="d4222-136">Pour déterminer l’autorisation qui vous est nécessaire, regardez la section **Autorisations** de l’API que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="d4222-136">To determine which permission you need, look at the **Permissions** section in the API you are interested to call.</span></span>

5. <span data-ttu-id="d4222-137">Sélectionnez **Accorder le consentement.**</span><span class="sxs-lookup"><span data-stu-id="d4222-137">Select **Grant consent**.</span></span>

     > [!NOTE]
     > <span data-ttu-id="d4222-138">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner **Accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="d4222-138">Every time you add a permission, you must select **Grant consent** for the new permission to take effect.</span></span>

    ![Accorder des autorisations](images/grant-consent.png)

6. <span data-ttu-id="d4222-140">Pour ajouter une secret à l’application, sélectionnez **Certificats & secrets,** ajoutez une description à la secret, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d4222-140">To add a secret to the application, select **Certificates & secrets**, add a description to the secret, and then select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4222-141">Après avoir sélectionné **Ajouter,** **sélectionnez copier la valeur de secret générée.**</span><span class="sxs-lookup"><span data-stu-id="d4222-141">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="d4222-142">Vous ne pourrez pas récupérer cette valeur après votre départ.</span><span class="sxs-lookup"><span data-stu-id="d4222-142">You won't be able to retrieve this value after you leave.</span></span>

    ![Image de la clé de création d’application](images/webapp-create-key2.png)

7. <span data-ttu-id="d4222-144">Notez votre ID d’application et votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="d4222-144">Write down your application ID and your tenant ID.</span></span> <span data-ttu-id="d4222-145">Dans la page de votre application, allez à **Vue d’ensemble** et copiez ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="d4222-145">On your application page, go to **Overview** and copy the following.</span></span>

   ![Image de l’ID d’application créé](images/app-and-tenant-ids.png)

8. <span data-ttu-id="d4222-147">**Pour Microsoft Defender pour les partenaires de point de terminaison uniquement.**</span><span class="sxs-lookup"><span data-stu-id="d4222-147">**For Microsoft Defender for Endpoint Partners only**.</span></span> <span data-ttu-id="d4222-148">Définissez votre application pour qu’elle soit multi-locataire (disponible dans tous les locataires après consentement).</span><span class="sxs-lookup"><span data-stu-id="d4222-148">Set your app to be multi-tenanted (available in all tenants after consent).</span></span> <span data-ttu-id="d4222-149">Cette étape **est requise** pour les applications tierces (par exemple, si vous créez une application destinée à s’exécuter dans le client de plusieurs clients).</span><span class="sxs-lookup"><span data-stu-id="d4222-149">This is **required** for third-party apps (for example, if you create an app that is intended to run in multiple customers' tenant).</span></span> <span data-ttu-id="d4222-150">Cela **n’est** pas obligatoire si vous créez un service que vous souhaitez exécuter uniquement dans votre client (par exemple, si vous créez une application pour votre propre utilisation qui interagit uniquement avec vos propres données).</span><span class="sxs-lookup"><span data-stu-id="d4222-150">This is **not required** if you create a service that you want to run in your tenant only (for example, if you create an application for your own usage that will only interact with your own data).</span></span> <span data-ttu-id="d4222-151">Pour définir votre application pour qu’elle soit multi-locataire :</span><span class="sxs-lookup"><span data-stu-id="d4222-151">To set your app to be multi-tenanted:</span></span>

    - <span data-ttu-id="d4222-152">Go to **Authentication**, and add `https://portal.azure.com` as the Redirect **URI**.</span><span class="sxs-lookup"><span data-stu-id="d4222-152">Go to **Authentication**, and add `https://portal.azure.com` as the **Redirect URI**.</span></span>

    - <span data-ttu-id="d4222-153">En bas de la page, sous **Types** de comptes pris en charge, sélectionnez les comptes dans n’importe quel consentement d’application  d’annuaire d’organisation pour votre application multi-locataire.</span><span class="sxs-lookup"><span data-stu-id="d4222-153">On the bottom of the page, under **Supported account types**, select the **Accounts in any organizational directory** application consent for your multi-tenant app.</span></span>

    <span data-ttu-id="d4222-154">Votre application doit être approuvée dans chaque client où vous avez l’intention de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="d4222-154">You need your application to be approved in each tenant where you intend to use it.</span></span> <span data-ttu-id="d4222-155">En effet, votre application interagit avec Defender for Endpoint pour le compte de votre client.</span><span class="sxs-lookup"><span data-stu-id="d4222-155">This is because your application interacts Defender for Endpoint on behalf of your customer.</span></span>

    <span data-ttu-id="d4222-156">Vous (ou votre client si vous écrivez une application tierce) devez sélectionner le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="d4222-156">You (or your customer if you are writing a third-party app) need to select the consent link and approve your app.</span></span> <span data-ttu-id="d4222-157">Le consentement doit être effectué avec un utilisateur qui dispose de privilèges d’administration dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4222-157">The consent should be done with a user who has administrative privileges in Active Directory.</span></span>

    <span data-ttu-id="d4222-158">Le lien de consentement est constitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4222-158">The consent link is formed as follows:</span></span> 

    ```
    https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=00000000-0000-0000-0000-000000000000&response_type=code&sso_reload=true
    ```

    <span data-ttu-id="d4222-159">Où 00000000-0000-0000-0000-00000000000000 est remplacé par votre ID d’application.</span><span class="sxs-lookup"><span data-stu-id="d4222-159">Where 00000000-0000-0000-0000-000000000000 is replaced with your application ID.</span></span>


<span data-ttu-id="d4222-160">**Terminé !**</span><span class="sxs-lookup"><span data-stu-id="d4222-160">**Done!**</span></span> <span data-ttu-id="d4222-161">Vous avez réussi à inscrire une application !</span><span class="sxs-lookup"><span data-stu-id="d4222-161">You have successfully registered an application!</span></span> <span data-ttu-id="d4222-162">Voir les exemples ci-dessous pour l’acquisition et la validation des jetons.</span><span class="sxs-lookup"><span data-stu-id="d4222-162">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="d4222-163">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="d4222-163">Get an access token</span></span>

<span data-ttu-id="d4222-164">Pour plus d’informations sur les jetons Azure AD, voir le [didacticiel Azure AD.](/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="d4222-164">For more information on Azure AD tokens, see the [Azure AD tutorial](/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

### <a name="use-powershell"></a><span data-ttu-id="d4222-165">Utiliser PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4222-165">Use PowerShell</span></span>

```powershell
# This script acquires the App Context Token and stores it in the variable $token for later use in the script.
# Paste your Tenant ID, App ID, and App Secret (App key) into the indicated quotes below.

$tenantId = '' ### Paste your tenant ID here
$appId = '' ### Paste your Application ID here
$appSecret = '' ### Paste your Application key here

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
```

### <a name="use-c"></a><span data-ttu-id="d4222-166">Utilisez C# :</span><span class="sxs-lookup"><span data-stu-id="d4222-166">Use C#:</span></span>

<span data-ttu-id="d4222-167">Le code suivant a été testé avec NuGet Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span><span class="sxs-lookup"><span data-stu-id="d4222-167">The following code was tested with NuGet Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span></span>

1. <span data-ttu-id="d4222-168">Créez une application console.</span><span class="sxs-lookup"><span data-stu-id="d4222-168">Create a new console application.</span></span>
1. <span data-ttu-id="d4222-169">Installez NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span><span class="sxs-lookup"><span data-stu-id="d4222-169">Install NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span></span>
1. <span data-ttu-id="d4222-170">Ajoutez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4222-170">Add the following:</span></span>

    ```
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

1. <span data-ttu-id="d4222-171">Copiez et collez le code suivant dans votre application (n’oubliez pas de mettre à jour les trois variables ```tenantId, appId, appSecret``` :</span><span class="sxs-lookup"><span data-stu-id="d4222-171">Copy and paste the following code in your app (don't forget to update the three variables: ```tenantId, appId, appSecret```):</span></span>

    ```
    string tenantId = "00000000-0000-0000-0000-000000000000"; // Paste your own tenant ID here
    string appId = "11111111-1111-1111-1111-111111111111"; // Paste your own app ID here
    string appSecret = "22222222-2222-2222-2222-222222222222"; // Paste your own app secret here for a test, and then store it in a safe place! 

    const string authority = "https://login.microsoftonline.com";
    const string wdatpResourceId = "https://api.securitycenter.microsoft.com";

    AuthenticationContext auth = new AuthenticationContext($"{authority}/{tenantId}/");
    ClientCredential clientCredential = new ClientCredential(appId, appSecret);
    AuthenticationResult authenticationResult = auth.AcquireTokenAsync(wdatpResourceId, clientCredential).GetAwaiter().GetResult();
    string token = authenticationResult.AccessToken;
    ```


### <a name="use-python"></a><span data-ttu-id="d4222-172">Utiliser Python</span><span class="sxs-lookup"><span data-stu-id="d4222-172">Use Python</span></span>

<span data-ttu-id="d4222-173">Voir [Obtenir un jeton à l’aide de Python.](run-advanced-query-sample-python.md#get-token)</span><span class="sxs-lookup"><span data-stu-id="d4222-173">See [Get token using Python](run-advanced-query-sample-python.md#get-token).</span></span>

### <a name="use-curl"></a><span data-ttu-id="d4222-174">Utiliser l’erreur</span><span class="sxs-lookup"><span data-stu-id="d4222-174">Use Curl</span></span>

> [!NOTE]
> <span data-ttu-id="d4222-175">La procédure suivante part du principe que La Windows est déjà installée sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d4222-175">The following procedure assumes that Curl for Windows is already installed on your computer.</span></span>

1. <span data-ttu-id="d4222-176">Ouvrez une invite de commandes et définissez CLIENT_ID sur votre ID d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="d4222-176">Open a command prompt, and set CLIENT_ID to your Azure application ID.</span></span>
1. <span data-ttu-id="d4222-177">Définissez CLIENT_SECRET sur votre secret d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="d4222-177">Set CLIENT_SECRET to your Azure application secret.</span></span>
1. <span data-ttu-id="d4222-178">Définissez TENANT_ID sur l’ID de client Azure du client qui souhaite utiliser votre application pour accéder à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d4222-178">Set TENANT_ID to the Azure tenant ID of the customer that wants to use your app to access Defender for Endpoint.</span></span>
1. <span data-ttu-id="d4222-179">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d4222-179">Run the following command:</span></span>

```
curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://securitycenter.onmicrosoft.com/windowsatpservice/.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
```

<span data-ttu-id="d4222-180">Vous recevez une réponse sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="d4222-180">You will get an answer in the following form:</span></span>

```
{"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
```

## <a name="validate-the-token"></a><span data-ttu-id="d4222-181">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="d4222-181">Validate the token</span></span>

<span data-ttu-id="d4222-182">Assurez-vous que vous avez reçu le jeton correct :</span><span class="sxs-lookup"><span data-stu-id="d4222-182">Ensure that you got the correct token:</span></span>

1. <span data-ttu-id="d4222-183">Copiez et collez le jeton obtenu à l’étape précédente dans [JWT](https://jwt.ms) afin de le décoder.</span><span class="sxs-lookup"><span data-stu-id="d4222-183">Copy and paste the token you got in the previous step into [JWT](https://jwt.ms) in order to decode it.</span></span>
1. <span data-ttu-id="d4222-184">Vérifier que vous obtenez une revendication « rôles » avec les autorisations souhaitées</span><span class="sxs-lookup"><span data-stu-id="d4222-184">Validate that you get a 'roles' claim with the desired permissions</span></span>
1. <span data-ttu-id="d4222-185">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application avec des autorisations pour tous les rôles de Microsoft Defender pour endpoint :</span><span class="sxs-lookup"><span data-stu-id="d4222-185">In the following image, you can see a decoded token acquired from an app with permissions to all of  Microsoft Defender for Endpoint's roles:</span></span>

![Image de validation de jeton](images/webapp-decoded-token.png)

## <a name="use-the-token-to-access-microsoft-defender-for-endpoint-api"></a><span data-ttu-id="d4222-187">Utiliser le jeton pour accéder à l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d4222-187">Use the token to access Microsoft Defender for Endpoint API</span></span>

1. <span data-ttu-id="d4222-188">Choisissez l’API que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="d4222-188">Choose the API you want to use.</span></span> <span data-ttu-id="d4222-189">Pour plus d’informations, [voir Supported Defender pour les API de point de terminaison.](exposed-apis-list.md)</span><span class="sxs-lookup"><span data-stu-id="d4222-189">For more information, see [Supported Defender for Endpoint APIs](exposed-apis-list.md).</span></span>
1. <span data-ttu-id="d4222-190">Définissez l’en-tête d’autorisation dans la demande http que vous envoyez à « Bearer {token} » (le porteur est le schéma d’autorisation).</span><span class="sxs-lookup"><span data-stu-id="d4222-190">Set the authorization header in the http request you send to "Bearer {token}" (Bearer is the authorization scheme).</span></span>
1. <span data-ttu-id="d4222-191">Le délai d’expiration du jeton est d’une heure.</span><span class="sxs-lookup"><span data-stu-id="d4222-191">The expiration time of the token is one hour.</span></span> <span data-ttu-id="d4222-192">Vous pouvez envoyer plusieurs demandes avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="d4222-192">You can send more than one request with the same token.</span></span>

<span data-ttu-id="d4222-193">Voici un exemple d’envoi d’une demande pour obtenir une liste d’alertes à l’aide **C#**:</span><span class="sxs-lookup"><span data-stu-id="d4222-193">The following is an example of sending a request to get a list of alerts **using C#**:</span></span> 
```
    var httpClient = new HttpClient();

    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.securitycenter.microsoft.com/api/alerts");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();

    // Do something useful with the response
```

## <a name="see-also"></a><span data-ttu-id="d4222-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4222-194">See also</span></span>
- <span data-ttu-id="d4222-195">[API prises en charge Microsoft Defender pour point de terminaison](exposed-apis-list.md).</span><span class="sxs-lookup"><span data-stu-id="d4222-195">[Supported Microsoft Defender for Endpoint APIs](exposed-apis-list.md)</span></span>
- [<span data-ttu-id="d4222-196">Accéder à Microsoft Defender pour le point de terminaison au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4222-196">Access Microsoft Defender for Endpoint on behalf of a user</span></span>](exposed-apis-create-app-nativeapp.md)
