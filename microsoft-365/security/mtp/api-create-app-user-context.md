---
title: Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur
description: Découvrez comment accéder aux API Microsoft 365 Defender au nom d’un utilisateur.
keywords: accès, de la part de l’utilisateur, de l’API, de l’application, de l’utilisateur, du jeton d’accès, du jeton
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
ms.openlocfilehash: f1c0caea9ff7810f79026c789241a4f250ec5303
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719415"
---
# <a name="create-an-app-to-access-microsoft-365-defender-apis-on-behalf-of-a-user"></a><span data-ttu-id="37020-104">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="37020-104">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="37020-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="37020-105">**Applies to:**</span></span>

- <span data-ttu-id="37020-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37020-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="37020-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37020-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="37020-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="37020-109">Cette page explique comment créer une application pour accéder par programme à Microsoft 365 Defender au nom d’un utilisateur unique.</span><span class="sxs-lookup"><span data-stu-id="37020-109">This page describes how to create an application to get programmatic access to Microsoft 365 Defender on behalf of a single user.</span></span>

<span data-ttu-id="37020-110">Si vous avez besoin d’un accès par programme à Microsoft 365 Defender sans utilisateur défini (par exemple, si vous écrivez une application ou un démon en arrière-plan), consultez la rubrique [créer une application pour accéder à Microsoft 365 Defender sans utilisateur](api-create-app-web.md).</span><span class="sxs-lookup"><span data-stu-id="37020-110">If you need programmatic access to Microsoft 365 Defender without a defined user (for example, if you're writing a background app or daemon), see [Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md).</span></span> <span data-ttu-id="37020-111">Si vous devez fournir un accès à plusieurs clients (par exemple, si vous utilisez une grande organisation ou un groupe de clients), voir [créer une application avec un accès partenaire aux API Microsoft 365 Defender](api-partner-access.md). Si vous n’êtes pas certain du type d’accès dont vous avez besoin, consultez la rubrique [prise en main](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="37020-111">If you need to provide access for multiple tenants—for example, if you're serving a large organization or a group of customers—see [Create an app with partner access to Microsoft 365 Defender APIs](api-partner-access.md).If you're not sure which kind of access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="37020-112">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="37020-112">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="37020-113">Ces API vous aident à automatiser les flux de travail et à utiliser les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="37020-113">Those APIs help you automate workflows and make use of Microsoft 365 Defender's capabilities.</span></span> <span data-ttu-id="37020-114">Cet accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="37020-114">This API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="37020-115">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="37020-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="37020-116">En règle générale, vous devez effectuer les étapes suivantes pour utiliser ces API :</span><span class="sxs-lookup"><span data-stu-id="37020-116">In general, you'll need to take the following steps to use these APIs:</span></span>

- <span data-ttu-id="37020-117">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="37020-117">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="37020-118">Obtenir un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="37020-118">Get an access token using this application.</span></span>
- <span data-ttu-id="37020-119">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="37020-119">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="37020-120">Cet article explique comment :</span><span class="sxs-lookup"><span data-stu-id="37020-120">This article explains how to:</span></span>

- <span data-ttu-id="37020-121">Créer une application Azure AD</span><span class="sxs-lookup"><span data-stu-id="37020-121">Create an Azure AD application</span></span>
- <span data-ttu-id="37020-122">Obtenir un jeton d’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-122">Get an access token to Microsoft 365 Defender</span></span>
- <span data-ttu-id="37020-123">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="37020-123">Validate the token</span></span>

> [!NOTE]
> <span data-ttu-id="37020-124">Lors de l’accès à l’API Microsoft 365 Defender au nom d’un utilisateur, vous devez disposer des autorisations d’application et des autorisations utilisateur correctes.</span><span class="sxs-lookup"><span data-stu-id="37020-124">When accessing Microsoft 365 Defender API on behalf of a user, you will need the correct application permissions and user permissions.</span></span>

> [!TIP]
> <span data-ttu-id="37020-125">Si vous disposez de l’autorisation pour effectuer une action dans le portail, vous disposez de l’autorisation pour effectuer l’action dans l’API.</span><span class="sxs-lookup"><span data-stu-id="37020-125">If you have the permission to perform an action in the portal, you have the permission to perform the action in the API.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="37020-126">Créer une application</span><span class="sxs-lookup"><span data-stu-id="37020-126">Create an app</span></span>

1. <span data-ttu-id="37020-127">Connectez-vous à [Azure](https://portal.azure.com) en tant qu’utilisateur doté du rôle d' **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="37020-127">Sign in to [Azure](https://portal.azure.com) as a user with the **Global Administrator** role.</span></span>

2. <span data-ttu-id="37020-128">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="37020-128">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="37020-130">Dans le formulaire, choisissez un nom pour votre application et entrez les informations suivantes pour l’URI de redirection, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="37020-130">In the form, choose a name for your application and enter the following information for the redirect URI, then select **Register**.</span></span>

   ![Image de la fenêtre créer une application](../../media/nativeapp-create2.PNG)

   - <span data-ttu-id="37020-132">**Type d’application :** Client public</span><span class="sxs-lookup"><span data-stu-id="37020-132">**Application type:** Public client</span></span>
   - <span data-ttu-id="37020-133">**URI de redirection :**https://portal.azure.com</span><span class="sxs-lookup"><span data-stu-id="37020-133">**Redirect URI:** https://portal.azure.com</span></span>

4. <span data-ttu-id="37020-134">Sur la page de votre application, sélectionnez **autorisations d’API**  >  **Ajouter une**  >  **API mon organisation utilise** des >, tapez **Microsoft Threat Protection**, puis sélectionnez **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="37020-134">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="37020-135">Votre application peut maintenant accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="37020-135">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="37020-136">*Microsoft Threat Protection* est un ancien nom pour Microsoft 365 Defender et n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="37020-136">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="37020-137">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="37020-137">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de la sélection des autorisations de l’API](../../media/apis-in-my-org-tab.PNG)

   - <span data-ttu-id="37020-139">Sélectionnez **autorisations déléguées**.</span><span class="sxs-lookup"><span data-stu-id="37020-139">Choose **Delegated permissions**.</span></span> <span data-ttu-id="37020-140">Choisissez les autorisations appropriées pour votre scénario (par exemple, **incident. Read**), puis sélectionnez **Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="37020-140">Choose the relevant permissions for your scenario (for example **Incident.Read**), and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions-delegated.PNG)

    > [!NOTE]
    > <span data-ttu-id="37020-142">Vous devez sélectionner les autorisations appropriées pour votre scénario.</span><span class="sxs-lookup"><span data-stu-id="37020-142">You need to select the relevant permissions for your scenario.</span></span> <span data-ttu-id="37020-143">*Read All incidents* n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="37020-143">*Read all incidents* is just an example.</span></span> <span data-ttu-id="37020-144">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="37020-144">To determine which permission you need, please look at the **Permissions** section in the API you want to call.</span></span>
    >
    > <span data-ttu-id="37020-145">Par exemple, pour [exécuter des requêtes avancées](api-advanced-hunting.md), sélectionnez l’autorisation « exécuter des requêtes avancées »; pour [isoler un appareil](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), sélectionnez l’autorisation « isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="37020-145">For instance, to [run advanced queries](api-advanced-hunting.md), select the 'Run advanced queries' permission; to [isolate a device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), select the 'Isolate machine' permission.</span></span>

5. <span data-ttu-id="37020-146">Sélectionnez **accorder le consentement** de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="37020-146">Select **Grant admin consent**.</span></span> <span data-ttu-id="37020-147">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner **accorder le consentement** de l’administrateur pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="37020-147">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

   ![Image des autorisations accorder](../../media/grant-consent-delegated.PNG)

6. <span data-ttu-id="37020-149">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="37020-149">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="37020-150">Elles sont indiquées sous **vue d’ensemble** sur votre application.</span><span class="sxs-lookup"><span data-stu-id="37020-150">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

## <a name="get-an-access-token"></a><span data-ttu-id="37020-152">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="37020-152">Get an access token</span></span>

<span data-ttu-id="37020-153">Pour plus d’informations sur les jetons Azure Active Directory, consultez le [didacticiel Azure ad](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span><span class="sxs-lookup"><span data-stu-id="37020-153">For more information on Azure Active Directory tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

### <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="37020-154">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="37020-154">Get an access token using PowerShell</span></span>

```PowerShell
if(!(Get-Package adal.ps)) { Install-Package -Name adal.ps } # Install the ADAL.PS package in case it's not already present

$tenantId = '' # Paste your directory (tenant) ID here.
$clientId = '' # Paste your application (client) ID here.
$redirectUri = '' # Paste your app's redirection URI

$authority = "https://login.windows.net/$tenantId"
$resourceUrl = 'https://api.security.microsoft.com'

$response = Get-ADALToken -Resource $resourceUrl -ClientId $cleintId -RedirectUri $redirectUri -Authority $authority -PromptBehavior:Always
$response.AccessToken | clip

$response.AccessToken
```

## <a name="validate-the-token"></a><span data-ttu-id="37020-155">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="37020-155">Validate the token</span></span>

1. <span data-ttu-id="37020-156">Copiez et collez le jeton dans [JWT](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="37020-156">Copy and paste the token into [JWT](https://jwt.ms) to decode it.</span></span>
1. <span data-ttu-id="37020-157">Assurez-vous que la revendication de *rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="37020-157">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

<span data-ttu-id="37020-158">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec ```Incidents.Read.All``` , ```Incidents.ReadWrite.All``` et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="37020-158">In the following image, you can see a decoded token acquired from an app, with ```Incidents.Read.All```, ```Incidents.ReadWrite.All```, and ```AdvancedHunting.Read.All``` permissions:</span></span>

![Image de la validation du jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-the-microsoft-365-defender-api"></a><span data-ttu-id="37020-160">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-160">Use the token to access the Microsoft 365 Defender API</span></span>

1. <span data-ttu-id="37020-161">Choisissez l’API que vous souhaitez utiliser (incidents ou chasse avancée).</span><span class="sxs-lookup"><span data-stu-id="37020-161">Choose the API you want to use (incidents, or advanced hunting).</span></span> <span data-ttu-id="37020-162">Pour plus d’informations, consultez la rubrique [API Microsoft 365 Defender prises en charge](api-supported.md).</span><span class="sxs-lookup"><span data-stu-id="37020-162">For more information, see [Supported Microsoft 365 Defender APIs](api-supported.md).</span></span>
2. <span data-ttu-id="37020-163">Dans la requête HTTP que vous allez envoyer, définissez l’en-tête d’autorisation sur `"Bearer" <token>` , le *porteur* étant le modèle d’autorisation et le *jeton* comme jeton validé.</span><span class="sxs-lookup"><span data-stu-id="37020-163">In the http request you're about to send, set the authorization header to `"Bearer" <token>`, *Bearer* being the authorization scheme, and *token* being your validated token.</span></span>
3. <span data-ttu-id="37020-164">Le jeton expire dans une heure.</span><span class="sxs-lookup"><span data-stu-id="37020-164">The token will expire within one hour.</span></span> <span data-ttu-id="37020-165">Vous pouvez envoyer plusieurs demandes pendant ce temps avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="37020-165">You can send more than one request during this time  with the same token.</span></span>

<span data-ttu-id="37020-166">L’exemple suivant montre comment envoyer une demande pour obtenir une liste d’incidents **à l’aide de C#**.</span><span class="sxs-lookup"><span data-stu-id="37020-166">The following example shows how to send a request to get a list of incidents **using C#**.</span></span>

```C#
    var httpClient = new HttpClient();
    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();
```

## <a name="related-articles"></a><span data-ttu-id="37020-167">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="37020-167">Related articles</span></span>

- [<span data-ttu-id="37020-168">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-168">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="37020-169">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-169">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="37020-170">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="37020-170">Create a 'Hello world' app</span></span>](api-hello-world.md)
- [<span data-ttu-id="37020-171">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="37020-171">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md)
- [<span data-ttu-id="37020-172">Créer une application avec un accès partenaire mutualisée aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37020-172">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md)
- [<span data-ttu-id="37020-173">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="37020-173">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="37020-174">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="37020-174">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="37020-175">Autorisation 2,0 OAuth pour l’authentification de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="37020-175">OAuth 2.0 authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
