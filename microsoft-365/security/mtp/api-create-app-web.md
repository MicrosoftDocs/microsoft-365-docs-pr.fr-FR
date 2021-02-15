---
title: Créer une application pour accéder à Microsoft 365 Defender sans utilisateur
description: Découvrez comment créer une application pour accéder à Microsoft 365 Defender sans utilisateur.
keywords: application, accès, api, créer
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
ms.openlocfilehash: f438189b4ba9fb66124650782b3de2ee34dfee64
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49928437"
---
# <a name="create-an-app-to-access-microsoft-365-defender-without-a-user"></a><span data-ttu-id="4f6ef-104">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f6ef-104">Create an app to access Microsoft 365 Defender without a user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="4f6ef-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-105">**Applies to:**</span></span>

- <span data-ttu-id="4f6ef-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f6ef-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f6ef-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="4f6ef-109">Cette page décrit comment créer une application pour obtenir un accès par programme à Microsoft 365 Defender sans utilisateur défini, par exemple, si vous créez un daemon ou un service en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-109">This page describes how to create an application to get programmatic access to Microsoft 365 Defender without a defined user—for example, if you're creating a daemon or background service.</span></span>

<span data-ttu-id="4f6ef-110">Si vous avez besoin d’un accès par programmation à Microsoft 365 Defender pour le compte d’un ou de plusieurs utilisateurs, voir Créer une application pour accéder aux API [Microsoft 365 Defender](api-create-app-user-context.md) au nom d’un utilisateur et Créer une application avec un accès partenaire aux API [Microsoft 365 Defender.](api-partner-access.md)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-110">If you need programmatic access to Microsoft 365 Defender on behalf of one or more users, see [Create an app to access Microsoft 365 Defender APIs on behalf of a user](api-create-app-user-context.md) and [Create an app with partner access to Microsoft 365 Defender APIs](api-partner-access.md).</span></span> <span data-ttu-id="4f6ef-111">If you’re not sure which kind of access you need, see [Get started](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="4f6ef-111">If you're not sure which kind of access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="4f6ef-112">Microsoft 365 Defender expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-112">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="4f6ef-113">Ces API vous aident à automatiser les flux de travail et à utiliser les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-113">Those APIs help you automate workflows and make use of Microsoft 365 Defender's capabilities.</span></span> <span data-ttu-id="4f6ef-114">Cet accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-114">This API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="4f6ef-115">Pour plus d’informations, voir flux de code [d’autorisation OAuth 2.0.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="4f6ef-116">En règle générale, vous devez suivre les étapes suivantes pour utiliser ces API :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-116">In general, you'll need to take the following steps to use these APIs:</span></span>

- <span data-ttu-id="4f6ef-117">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4f6ef-117">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="4f6ef-118">Obtenez un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-118">Get an access token using this application.</span></span>
- <span data-ttu-id="4f6ef-119">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-119">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="4f6ef-120">Cet article explique comment :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-120">This article explains how to:</span></span>

- <span data-ttu-id="4f6ef-121">Créer une application Azure AD</span><span class="sxs-lookup"><span data-stu-id="4f6ef-121">Create an Azure AD application</span></span>
- <span data-ttu-id="4f6ef-122">Obtenir un jeton d’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-122">Get an access token to Microsoft 365 Defender</span></span>
- <span data-ttu-id="4f6ef-123">Validez le jeton.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-123">Validate the token.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="4f6ef-124">Créer une application</span><span class="sxs-lookup"><span data-stu-id="4f6ef-124">Create an app</span></span>

1. <span data-ttu-id="4f6ef-125">Connectez-vous [à Azure](https://portal.azure.com) en tant qu’utilisateur avec le **rôle Administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-125">Sign in to [Azure](https://portal.azure.com) as a user with the **Global Administrator** role.</span></span>

2. <span data-ttu-id="4f6ef-126">Accédez **à Azure Active Directory** App  >  **registrations** New  >  **registration**.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-126">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation vers l’inscription de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="4f6ef-128">Dans le formulaire, choisissez un nom pour votre application, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-128">In the form, choose a name for your application, then select **Register**.</span></span>

4. <span data-ttu-id="4f6ef-129">Dans la page de votre application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon organisation utilise >, tapez Protection Microsoft contre les menaces, puis sélectionnez  >    >   Protection **Microsoft contre les menaces.** </span><span class="sxs-lookup"><span data-stu-id="4f6ef-129">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="4f6ef-130">Votre application peut désormais accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-130">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="4f6ef-131">*Microsoft Threat Protection* est un ancien nom de Microsoft 365 Defender et n’apparaîtra pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-131">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="4f6ef-132">Vous devez commencer à écrire son nom dans la zone de texte pour qu’il apparaisse.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-132">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de la sélection des autorisations d’API](../../media/apis-in-my-org-tab.PNG)

5. <span data-ttu-id="4f6ef-134">Sélectionnez **les autorisations d’application.**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-134">Select **Application permissions**.</span></span> <span data-ttu-id="4f6ef-135">Choisissez les autorisations pertinentes pour votre scénario (par exemple, **Incident.Read.All),** puis **sélectionnez Ajouter des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-135">Choose the relevant permissions for your scenario (for example, **Incident.Read.All**), and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection d’API](../../media/request-api-permissions.PNG)

    > [!NOTE]
    > <span data-ttu-id="4f6ef-137">Vous devez sélectionner les autorisations pertinentes pour votre scénario.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-137">You need to select the relevant permissions for your scenario.</span></span> <span data-ttu-id="4f6ef-138">*Lire tous les incidents* n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-138">*Read all incidents* is just an example.</span></span> <span data-ttu-id="4f6ef-139">Pour déterminer l’autorisation qui vous est nécessaire, consultez la section **Autorisations** de l’API que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-139">To determine which permission you need, please look at the **Permissions** section in the API you want to call.</span></span>
    >
    > <span data-ttu-id="4f6ef-140">Par exemple, pour [exécuter des requêtes avancées,](api-advanced-hunting.md)sélectionnez l’autorisation « Exécuter des requêtes avancées » ; pour [isoler un appareil,](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine)sélectionnez l’autorisation « Isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="4f6ef-140">For instance, to [run advanced queries](api-advanced-hunting.md), select the 'Run advanced queries' permission; to [isolate a device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), select the 'Isolate machine' permission.</span></span>

6. <span data-ttu-id="4f6ef-141">Sélectionnez **Accorder le consentement de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-141">Select **Grant admin consent**.</span></span> <span data-ttu-id="4f6ef-142">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner Accorder le **consentement de l’administrateur** pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-142">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

    ![Image de l’octroi d’autorisations](../../media/grant-consent.PNG)

7. <span data-ttu-id="4f6ef-144">Pour ajouter une secret à l’application, sélectionnez **Certificats & secrets,** ajoutez une description à la secret, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-144">To add a secret to the application, select **Certificates & secrets**, add a description to the secret, then select **Add**.</span></span>

    > [!TIP]
    > <span data-ttu-id="4f6ef-145">Après avoir sélectionné **Ajouter,** **sélectionnez copier la valeur de secret générée.**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-145">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="4f6ef-146">Vous ne pourrez pas récupérer la valeur secrète après votre départ.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-146">You won't be able to retrieve the secret value after you leave.</span></span>

    ![Image de la clé de création d’application](../../media/webapp-create-key2.png)

8. <span data-ttu-id="4f6ef-148">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-148">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="4f6ef-149">Ils sont répertoriés sous Vue **d’ensemble** sur la page de votre application.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-149">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

9. <span data-ttu-id="4f6ef-151">Pour les partenaires **Microsoft 365 Defender** uniquement : suivez ces [instructions](https://docs.microsoft.com/microsoft-365/security/mtp/api-partner-access) pour l’accès des partenaires via les API Microsoft 365 Defender, définissez votre application comme multi-clients, afin qu’elle puisse être disponible dans tous les clients une fois que vous avez reçu le consentement de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-151">**For Microsoft 365 Defender Partners only**: [Follow these instructions](https://docs.microsoft.com/microsoft-365/security/mtp/api-partner-access) for partner access through the Microsoft 365 Defender APIs, set your app to be multi-tenant, so it can be available in all tenants once you receive admin consent.</span></span> <span data-ttu-id="4f6ef-152">L’accès  des partenaires est requis pour les applications tierces, par exemple, si vous créez une application destinée à s’exécuter dans les clients de plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-152">Partner access is **required** for third-party apps—for example, if you create an app that is intended to run in multiple customers' tenants.</span></span> <span data-ttu-id="4f6ef-153">Il **n’est** pas nécessaire si vous créez un service que vous souhaitez exécuter uniquement dans votre client, par exemple une application pour votre propre utilisation qui interagit uniquement avec vos propres données.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-153">It is **not required** if you create a service that you want to run in your tenant only, such as an application for your own usage that will only interact with your own data.</span></span> <span data-ttu-id="4f6ef-154">Pour définir votre application comme multi-locataire :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-154">To set your app to be multi-tenant:</span></span>

    - <span data-ttu-id="4f6ef-155">Go to **Authentication**, and add https://portal.azure.com as the Redirect **URI**.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-155">Go to **Authentication**, and add https://portal.azure.com as the **Redirect URI**.</span></span>

    - <span data-ttu-id="4f6ef-156">En bas de la page, sous **Types** de comptes pris en charge, sélectionnez les comptes dans n’importe quel consentement d’application  d’annuaire d’organisation pour votre application multi-locataire.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-156">On the bottom of the page, under **Supported account types**, select the **Accounts in any organizational directory** application consent for your multi-tenant app.</span></span>

    <span data-ttu-id="4f6ef-157">Étant donné que votre application interagit avec Microsoft 365 Defender pour le compte de vos utilisateurs, elle doit être approuvée pour chaque client sur lequel vous avez l’intention de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-157">Since your application interacts with Microsoft 365 Defender on behalf of your users, it needs be approved for every tenant on which you intend to use it.</span></span>

    <span data-ttu-id="4f6ef-158">L’administrateur général Active Directory pour chaque client doit sélectionner le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-158">The Active Directory global admin for each tenant needs to select the consent link and approve your app.</span></span>

    <span data-ttu-id="4f6ef-159">Le lien de consentement a la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-159">The consent link has the following structure:</span></span>

    ```http
    https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=<00000000-0000-0000-0000-000000000000>&response_type=code&sso_reload=true
    ```

    <span data-ttu-id="4f6ef-160">Les chiffres `00000000-0000-0000-0000-000000000000` doivent être remplacés par votre ID d’application.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-160">The digits `00000000-0000-0000-0000-000000000000` should be replaced with your Application ID.</span></span>  

<span data-ttu-id="4f6ef-161">**Terminé !**</span><span class="sxs-lookup"><span data-stu-id="4f6ef-161">**Done!**</span></span> <span data-ttu-id="4f6ef-162">Vous avez réussi à inscrire une application !</span><span class="sxs-lookup"><span data-stu-id="4f6ef-162">You've successfully registered an application!</span></span> <span data-ttu-id="4f6ef-163">Voir les exemples ci-dessous pour l’acquisition et la validation des jetons.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-163">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="4f6ef-164">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="4f6ef-164">Get an access token</span></span>

<span data-ttu-id="4f6ef-165">Pour plus d’informations sur les jetons Azure Active Directory, voir le [didacticiel Azure AD.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-165">For more information on Azure Active Directory tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f6ef-166">Bien que les exemples de cette section vous encouragent à coller des valeurs secrètes à des fins de test, vous ne devez jamais coder en dur des **secrets** dans une application en cours d’exécution en production.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-166">Although the examples in this section encourage you to paste in secret values for testing purposes, you should **never hardcode secrets** into an application running in production.</span></span> <span data-ttu-id="4f6ef-167">Un tiers peut utiliser votre secret pour accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-167">A third party could use your secret to access resources.</span></span> <span data-ttu-id="4f6ef-168">Vous pouvez aider à sécuriser les secrets de votre application à l’aide [d’Azure Key Vault.](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-168">You can help keep your app's secrets secure by using [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates).</span></span> <span data-ttu-id="4f6ef-169">Pour obtenir un exemple pratique de la façon dont vous pouvez protéger votre application, voir Gérer les secrets dans vos applications serveur avec [Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span><span class="sxs-lookup"><span data-stu-id="4f6ef-169">For a practical example of how you can protect your app, see [Manage secrets in your server apps with Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span></span>

### <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="4f6ef-170">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f6ef-170">Get an access token using PowerShell</span></span>

```PowerShell
# This code gets the application context token and saves it to a file named "Latest-token.txt" under the current directory.

$tenantId = '' # Paste your directory (tenant) ID here
$clientId = '' # Paste your application (client) ID here
$appSecret = '' # Paste your own app secret here to test, then store it in a safe place, such as the Azure Key Vault!

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

### <a name="get-an-access-token-using-c"></a><span data-ttu-id="4f6ef-171">Obtenir un jeton d’accès à l’aide de C\#</span><span class="sxs-lookup"><span data-stu-id="4f6ef-171">Get an access token using C\#</span></span>

> [!NOTE]
> <span data-ttu-id="4f6ef-172">Le code suivant a été testé avec Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-172">The following code was tested with Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span></span>

1. <span data-ttu-id="4f6ef-173">Créez une application console.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-173">Create a new console application.</span></span>

1. <span data-ttu-id="4f6ef-174">Installez NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span><span class="sxs-lookup"><span data-stu-id="4f6ef-174">Install NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span></span>

1. <span data-ttu-id="4f6ef-175">Ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-175">Add the following line:</span></span>

    ```C#
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

1. <span data-ttu-id="4f6ef-176">Copiez et collez le code suivant dans votre application (n’oubliez pas de mettre à jour les trois variables `tenantId` : , , ) `clientId` `appSecret` :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-176">Copy and paste the following code into your app (don't forget to update the three variables: `tenantId`, `clientId`, `appSecret`):</span></span>

    ```C#
    string tenantId = ""; // Paste your directory (tenant) ID here
    string clientId = ""; // Paste your application (client) ID here
    string appSecret = ""; // Paste your own app secret here to test, then store it in a safe place, such as the Azure Key Vault!

    const string authority = "https://login.windows.net";
    const string wdatpResourceId = "https://api.security.microsoft.com";

    AuthenticationContext auth = new AuthenticationContext($"{authority}/{tenantId}/");
    ClientCredential clientCredential = new ClientCredential(clientId, appSecret);
    AuthenticationResult authenticationResult = auth.AcquireTokenAsync(wdatpResourceId, clientCredential).GetAwaiter().GetResult();
    string token = authenticationResult.AccessToken;
    ```

### <a name="get-an-access-token-using-python"></a><span data-ttu-id="4f6ef-177">Obtenir un jeton d’accès à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="4f6ef-177">Get an access token using Python</span></span>

```Python
import json
import urllib.request
import urllib.parse

tenantId = '' # Paste your directory (tenant) ID here
clientId = '' # Paste your application (client) ID here
appSecret = '' # Paste your own app secret here to test, then store it in a safe place, such as the Azure Key Vault!

url = "https://login.windows.net/%s/oauth2/token" % (tenantId)

resourceAppIdUri = 'https://api.securitycenter.windows.com'

body = {
    'resource' : resourceAppIdUri,
    'client_id' : clientId,
    'client_secret' : appSecret,
    'grant_type' : 'client_credentials'
}

data = urllib.parse.urlencode(body).encode("utf-8")

req = urllib.request.Request(url, data)
response = urllib.request.urlopen(req)
jsonResponse = json.loads(response.read())
aadToken = jsonResponse["access_token"]
```

### <a name="get-an-access-token-using-curl"></a><span data-ttu-id="4f6ef-178">Obtenir un jeton d’accès à l’aide de l’outil</span><span class="sxs-lookup"><span data-stu-id="4f6ef-178">Get an access token using curl</span></span>

> [!NOTE]
> <span data-ttu-id="4f6ef-179">Il est préinstallé sur Windows 10, versions 1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-179">Curl is pre-installed on Windows 10, versions 1803 and later.</span></span> <span data-ttu-id="4f6ef-180">Pour les autres versions de Windows, téléchargez et installez l’outil directement à partir du site [web officiel de lancement.](https://curl.haxx.se/windows/)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-180">For other versions of Windows, download and install the tool directly from the [official curl website](https://curl.haxx.se/windows/).</span></span>

1. <span data-ttu-id="4f6ef-181">Ouvrez une invite de commandes et définissez CLIENT_ID sur votre ID d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-181">Open a command prompt, and set CLIENT_ID to your Azure application ID.</span></span>

1. <span data-ttu-id="4f6ef-182">Définissez CLIENT_SECRET sur votre secret d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-182">Set CLIENT_SECRET to your Azure application secret.</span></span>

1. <span data-ttu-id="4f6ef-183">Définissez TENANT_ID sur l’ID de locataire Azure du client qui souhaite utiliser votre application pour accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-183">Set TENANT_ID to the Azure tenant ID of the customer that wants to use your app to access Microsoft 365 Defender.</span></span>

1. <span data-ttu-id="4f6ef-184">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-184">Run the following command:</span></span>

   ```bash
   curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://securitycenter.onmicrosoft.com/windowsatpservice/.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
   ```

   <span data-ttu-id="4f6ef-185">Une réponse réussie ressemblera à ceci :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-185">A successful response will look like this:</span></span>

   ```bash
   {"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
   ```

## <a name="validate-the-token"></a><span data-ttu-id="4f6ef-186">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="4f6ef-186">Validate the token</span></span>

1. <span data-ttu-id="4f6ef-187">Copiez et collez le jeton dans le site web de validation de jeton [web JSON, JWT,](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-187">Copy and paste the token into the [JSON web token validator website, JWT,](https://jwt.ms) to decode it.</span></span>

1. <span data-ttu-id="4f6ef-188">Assurez-vous que la revendication *de rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-188">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

   <span data-ttu-id="4f6ef-189">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec `Incidents.Read.All` `Incidents.ReadWrite.All` , et des `AdvancedHunting.Read.All` autorisations :</span><span class="sxs-lookup"><span data-stu-id="4f6ef-189">In the following image, you can see a decoded token acquired from an app, with `Incidents.Read.All`, `Incidents.ReadWrite.All`, and `AdvancedHunting.Read.All` permissions:</span></span>

   ![Image de validation de jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-the-microsoft-365-defender-api"></a><span data-ttu-id="4f6ef-191">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-191">Use the token to access the Microsoft 365 Defender API</span></span>

1. <span data-ttu-id="4f6ef-192">Choisissez l’API que vous souhaitez utiliser (incidents ou recherche avancée).</span><span class="sxs-lookup"><span data-stu-id="4f6ef-192">Choose the API you want to use (incidents, or advanced hunting).</span></span> <span data-ttu-id="4f6ef-193">Pour plus d’informations, voir [API Microsoft 365 Defender pris en charge.](api-supported.md)</span><span class="sxs-lookup"><span data-stu-id="4f6ef-193">For more information, see [Supported Microsoft 365 Defender APIs](api-supported.md).</span></span>

2. <span data-ttu-id="4f6ef-194">Dans la demande http que vous êtes sur le point d’envoyer, définissez l’en-tête d’autorisation sur `"Bearer" <token>` , *bearer* étant le schéma d’autorisation et le jeton en cours de validation. </span><span class="sxs-lookup"><span data-stu-id="4f6ef-194">In the http request you are about to send, set the authorization header to `"Bearer" <token>`, *Bearer* being the authorization scheme, and *token* being your validated token.</span></span>

3. <span data-ttu-id="4f6ef-195">Le jeton expire dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-195">The token will expire within one hour.</span></span> <span data-ttu-id="4f6ef-196">Vous pouvez envoyer plusieurs demandes pendant cette période avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-196">You can send more than one request during this time with the same token.</span></span>

<span data-ttu-id="4f6ef-197">L’exemple suivant montre comment envoyer une demande pour obtenir une liste d’incidents à **l’aide de C#**.</span><span class="sxs-lookup"><span data-stu-id="4f6ef-197">The following example shows how to send a request to get a list of incidents **using C#**.</span></span>

```C#
    var httpClient = new HttpClient();
    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();
```

## <a name="related-articles"></a><span data-ttu-id="4f6ef-198">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4f6ef-198">Related articles</span></span>

- [<span data-ttu-id="4f6ef-199">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-199">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="4f6ef-200">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-200">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="4f6ef-201">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="4f6ef-201">Create a 'Hello world' application</span></span>](api-hello-world.md)
- [<span data-ttu-id="4f6ef-202">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f6ef-202">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md)
- [<span data-ttu-id="4f6ef-203">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f6ef-203">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md)
- [<span data-ttu-id="4f6ef-204">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="4f6ef-204">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="4f6ef-205">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4f6ef-205">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="4f6ef-206">Gérer les secrets dans vos applications serveur avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4f6ef-206">Manage secrets in your server apps with Azure Key Vault</span></span>](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="4f6ef-207">Autorisation OAuth 2.0 pour la connexion de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="4f6ef-207">OAuth 2.0 authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
