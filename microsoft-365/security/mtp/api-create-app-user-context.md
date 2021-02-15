---
title: Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur
description: Découvrez comment accéder aux API Microsoft 365 Defender au nom d’un utilisateur.
keywords: access, de la part de l’utilisateur, de l’api, de l’application, de l’utilisateur, du jeton d’accès, du jeton,
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
ms.openlocfilehash: d443334a00b5247525a2cdba98a11cfe0f515193
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49928461"
---
# <a name="create-an-app-to-access-microsoft-365-defender-apis-on-behalf-of-a-user"></a><span data-ttu-id="bd944-104">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="bd944-104">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="bd944-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bd944-105">**Applies to:**</span></span>

- <span data-ttu-id="bd944-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd944-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bd944-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bd944-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="bd944-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="bd944-109">Cette page explique comment créer une application pour obtenir un accès par programme à Microsoft 365 Defender pour le compte d’un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd944-109">This page describes how to create an application to get programmatic access to Microsoft 365 Defender on behalf of a single user.</span></span>

<span data-ttu-id="bd944-110">Si vous avez besoin d’un accès par programmation à Microsoft 365 Defender sans utilisateur défini (par exemple, si vous écrivez une application en arrière-plan ou un daemon), voir Créer une application pour accéder à [Microsoft 365 Defender](api-create-app-web.md)sans utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd944-110">If you need programmatic access to Microsoft 365 Defender without a defined user (for example, if you're writing a background app or daemon), see [Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md).</span></span> <span data-ttu-id="bd944-111">Si vous devez fournir l’accès à plusieurs clients, par exemple, si vous fournissez des services à une grande organisation ou à un groupe de clients, voir Créer une application avec un accès partenaire aux API [Microsoft 365 Defender.](api-partner-access.md) If you’re not sure which kind of access you need, see [Get started](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="bd944-111">If you need to provide access for multiple tenants—for example, if you're serving a large organization or a group of customers—see [Create an app with partner access to Microsoft 365 Defender APIs](api-partner-access.md).If you're not sure which kind of access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="bd944-112">Microsoft 365 Defender expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="bd944-112">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="bd944-113">Ces API vous aident à automatiser les flux de travail et à utiliser les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="bd944-113">Those APIs help you automate workflows and make use of Microsoft 365 Defender's capabilities.</span></span> <span data-ttu-id="bd944-114">Cet accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="bd944-114">This API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="bd944-115">Pour plus d’informations, voir flux de code [d’autorisation OAuth 2.0.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="bd944-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="bd944-116">En règle générale, vous devez suivre les étapes suivantes pour utiliser ces API :</span><span class="sxs-lookup"><span data-stu-id="bd944-116">In general, you'll need to take the following steps to use these APIs:</span></span>

- <span data-ttu-id="bd944-117">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="bd944-117">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="bd944-118">Obtenez un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="bd944-118">Get an access token using this application.</span></span>
- <span data-ttu-id="bd944-119">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="bd944-119">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="bd944-120">Cet article explique comment :</span><span class="sxs-lookup"><span data-stu-id="bd944-120">This article explains how to:</span></span>

- <span data-ttu-id="bd944-121">Créer une application Azure AD</span><span class="sxs-lookup"><span data-stu-id="bd944-121">Create an Azure AD application</span></span>
- <span data-ttu-id="bd944-122">Obtenir un jeton d’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-122">Get an access token to Microsoft 365 Defender</span></span>
- <span data-ttu-id="bd944-123">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="bd944-123">Validate the token</span></span>

> [!NOTE]
> <span data-ttu-id="bd944-124">Lorsque vous accédez à l’API Microsoft 365 Defender pour le compte d’un utilisateur, vous avez besoin des autorisations d’application et des autorisations utilisateur correctes.</span><span class="sxs-lookup"><span data-stu-id="bd944-124">When accessing Microsoft 365 Defender API on behalf of a user, you will need the correct application permissions and user permissions.</span></span>

> [!TIP]
> <span data-ttu-id="bd944-125">Si vous avez l’autorisation d’effectuer une action dans le portail, vous avez l’autorisation d’effectuer l’action dans l’API.</span><span class="sxs-lookup"><span data-stu-id="bd944-125">If you have the permission to perform an action in the portal, you have the permission to perform the action in the API.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="bd944-126">Créer une application</span><span class="sxs-lookup"><span data-stu-id="bd944-126">Create an app</span></span>

1. <span data-ttu-id="bd944-127">Connectez-vous [à Azure](https://portal.azure.com) en tant qu’utilisateur avec le **rôle Administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="bd944-127">Sign in to [Azure](https://portal.azure.com) as a user with the **Global Administrator** role.</span></span>

2. <span data-ttu-id="bd944-128">Accédez **à Azure Active Directory** App  >  **registrations** New  >  **registration**.</span><span class="sxs-lookup"><span data-stu-id="bd944-128">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation vers l’inscription de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="bd944-130">Dans le formulaire, choisissez un nom pour votre application et entrez les informations suivantes pour l’URI de redirection, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bd944-130">In the form, choose a name for your application and enter the following information for the redirect URI, then select **Register**.</span></span>

   ![Image de la fenêtre Créer une application](../../media/nativeapp-create2.PNG)

   - <span data-ttu-id="bd944-132">**Type d’application :** Client public</span><span class="sxs-lookup"><span data-stu-id="bd944-132">**Application type:** Public client</span></span>
   - <span data-ttu-id="bd944-133">**URI de redirection :**https://portal.azure.com</span><span class="sxs-lookup"><span data-stu-id="bd944-133">**Redirect URI:** https://portal.azure.com</span></span>

4. <span data-ttu-id="bd944-134">Dans la page de votre application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon organisation utilise >, tapez Protection Microsoft contre les menaces, puis sélectionnez  >    >   Protection **Microsoft contre les menaces.** </span><span class="sxs-lookup"><span data-stu-id="bd944-134">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="bd944-135">Votre application peut désormais accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="bd944-135">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="bd944-136">*Microsoft Threat Protection* est un ancien nom de Microsoft 365 Defender et n’apparaîtra pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="bd944-136">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="bd944-137">Vous devez commencer à écrire son nom dans la zone de texte pour qu’il apparaisse.</span><span class="sxs-lookup"><span data-stu-id="bd944-137">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de la sélection des autorisations d’API](../../media/apis-in-my-org-tab.PNG)

   - <span data-ttu-id="bd944-139">Choisissez **Autorisations déléguées.**</span><span class="sxs-lookup"><span data-stu-id="bd944-139">Choose **Delegated permissions**.</span></span> <span data-ttu-id="bd944-140">Choisissez les autorisations pertinentes pour votre scénario (par exemple **Incident.Read),** puis **sélectionnez Ajouter des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="bd944-140">Choose the relevant permissions for your scenario (for example **Incident.Read**), and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection d’API](../../media/request-api-permissions-delegated.PNG)

    > [!NOTE]
    > <span data-ttu-id="bd944-142">Vous devez sélectionner les autorisations pertinentes pour votre scénario.</span><span class="sxs-lookup"><span data-stu-id="bd944-142">You need to select the relevant permissions for your scenario.</span></span> <span data-ttu-id="bd944-143">*Lire tous les incidents* n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="bd944-143">*Read all incidents* is just an example.</span></span> <span data-ttu-id="bd944-144">Pour déterminer l’autorisation qui vous est nécessaire, consultez la section **Autorisations** de l’API que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="bd944-144">To determine which permission you need, please look at the **Permissions** section in the API you want to call.</span></span>
    >
    > <span data-ttu-id="bd944-145">Par exemple, pour [exécuter des requêtes avancées,](api-advanced-hunting.md)sélectionnez l’autorisation « Exécuter des requêtes avancées » ; pour [isoler un appareil,](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine)sélectionnez l’autorisation « Isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="bd944-145">For instance, to [run advanced queries](api-advanced-hunting.md), select the 'Run advanced queries' permission; to [isolate a device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), select the 'Isolate machine' permission.</span></span>

5. <span data-ttu-id="bd944-146">Sélectionnez **Accorder le consentement de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="bd944-146">Select **Grant admin consent**.</span></span> <span data-ttu-id="bd944-147">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner Accorder le **consentement de l’administrateur** pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="bd944-147">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

   ![Image de l’octroi d’autorisations](../../media/grant-consent-delegated.PNG)

6. <span data-ttu-id="bd944-149">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="bd944-149">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="bd944-150">Ils sont répertoriés sous Vue **d’ensemble** sur la page de votre application.</span><span class="sxs-lookup"><span data-stu-id="bd944-150">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

## <a name="get-an-access-token"></a><span data-ttu-id="bd944-152">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="bd944-152">Get an access token</span></span>

<span data-ttu-id="bd944-153">Pour plus d’informations sur les jetons Azure Active Directory, voir le [didacticiel Azure AD.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="bd944-153">For more information on Azure Active Directory tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

### <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="bd944-154">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd944-154">Get an access token using PowerShell</span></span>

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

## <a name="validate-the-token"></a><span data-ttu-id="bd944-155">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="bd944-155">Validate the token</span></span>

1. <span data-ttu-id="bd944-156">Copiez et collez le jeton dans [JWT](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="bd944-156">Copy and paste the token into [JWT](https://jwt.ms) to decode it.</span></span>
1. <span data-ttu-id="bd944-157">Assurez-vous que la revendication *de rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="bd944-157">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

<span data-ttu-id="bd944-158">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec ```Incidents.Read.All``` ```Incidents.ReadWrite.All``` , et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="bd944-158">In the following image, you can see a decoded token acquired from an app, with ```Incidents.Read.All```, ```Incidents.ReadWrite.All```, and ```AdvancedHunting.Read.All``` permissions:</span></span>

![Image de validation de jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-the-microsoft-365-defender-api"></a><span data-ttu-id="bd944-160">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-160">Use the token to access the Microsoft 365 Defender API</span></span>

1. <span data-ttu-id="bd944-161">Choisissez l’API que vous souhaitez utiliser (incidents ou recherche avancée).</span><span class="sxs-lookup"><span data-stu-id="bd944-161">Choose the API you want to use (incidents, or advanced hunting).</span></span> <span data-ttu-id="bd944-162">Pour plus d’informations, voir [API Microsoft 365 Defender pris en charge.](api-supported.md)</span><span class="sxs-lookup"><span data-stu-id="bd944-162">For more information, see [Supported Microsoft 365 Defender APIs](api-supported.md).</span></span>
2. <span data-ttu-id="bd944-163">Dans la requête http que vous êtes sur le point d’envoyer, définissez l’en-tête d’autorisation sur , le porteur étant le schéma d’autorisation et le jeton comme jeton `"Bearer" <token>` validé.  </span><span class="sxs-lookup"><span data-stu-id="bd944-163">In the http request you're about to send, set the authorization header to `"Bearer" <token>`, *Bearer* being the authorization scheme, and *token* being your validated token.</span></span>
3. <span data-ttu-id="bd944-164">Le jeton expire dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="bd944-164">The token will expire within one hour.</span></span> <span data-ttu-id="bd944-165">Vous pouvez envoyer plusieurs demandes pendant cette période avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="bd944-165">You can send more than one request during this time  with the same token.</span></span>

<span data-ttu-id="bd944-166">L’exemple suivant montre comment envoyer une demande pour obtenir une liste d’incidents à **l’aide de C#**.</span><span class="sxs-lookup"><span data-stu-id="bd944-166">The following example shows how to send a request to get a list of incidents **using C#**.</span></span>

```C#
    var httpClient = new HttpClient();
    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();
```

## <a name="related-articles"></a><span data-ttu-id="bd944-167">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="bd944-167">Related articles</span></span>

- [<span data-ttu-id="bd944-168">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-168">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="bd944-169">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-169">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="bd944-170">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="bd944-170">Create a 'Hello world' app</span></span>](api-hello-world.md)
- [<span data-ttu-id="bd944-171">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="bd944-171">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md)
- [<span data-ttu-id="bd944-172">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd944-172">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md)
- [<span data-ttu-id="bd944-173">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="bd944-173">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="bd944-174">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bd944-174">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="bd944-175">Autorisation OAuth 2.0 pour la connexion de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="bd944-175">OAuth 2.0 authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
