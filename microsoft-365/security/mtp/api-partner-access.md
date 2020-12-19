---
title: Accès partenaire via les API Microsoft 365 Defender
description: Découvrez comment créer une application pour accéder par programme à Microsoft 365 Defender au nom de vos utilisateurs.
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
ms.openlocfilehash: 5de113c8f8419b3af2a287bd7ba7e41dc06b4121
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719439"
---
# <a name="create-an-app-with-partner-access-to-microsoft-365-defender-apis"></a><span data-ttu-id="cf6bc-104">Créer une application avec un accès partenaire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-104">Create an app with partner access to Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="cf6bc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cf6bc-105">**Applies to:**</span></span>

- <span data-ttu-id="cf6bc-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf6bc-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cf6bc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="cf6bc-109">Cette page explique comment créer une application Azure Active Directory qui a un accès par programme à Microsoft 365 Defender, pour le compte des utilisateurs sur plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-109">This page describes how to create an Azure Active Directory app that has programmatic access to Microsoft 365 Defender, on behalf of users across multiple tenants.</span></span> <span data-ttu-id="cf6bc-110">Les applications mutualisées sont utiles pour le traitement de groupes d’utilisateurs de grande taille.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-110">Multi-tenant apps are useful for serving large groups of users.</span></span>

<span data-ttu-id="cf6bc-111">Si vous avez besoin d’un accès par programme à Microsoft 365 Defender au nom d’un utilisateur unique, consultez la rubrique [créer une application pour accéder aux API microsoft 365 Defender au nom d’un utilisateur](api-create-app-user-context.md).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-111">If you need programmatic access to Microsoft 365 Defender on behalf of a single user, see [Create an app to access Microsoft 365 Defender APIs on behalf of a user](api-create-app-user-context.md).</span></span> <span data-ttu-id="cf6bc-112">Si vous avez besoin d’un accès sans définition explicite de l’utilisateur (par exemple, si vous écrivez une application ou un démon d’arrière-plan), consultez la rubrique [créer une application pour accéder à Microsoft 365 Defender sans utilisateur](api-create-app-web.md).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-112">If you need access without a user explicitly defined (for example, if you're writing a background app or daemon), see [Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md).</span></span> <span data-ttu-id="cf6bc-113">Si vous n’êtes pas certain du type d’accès dont vous avez besoin, consultez la rubrique [prise en main](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-113">If you're not sure which kind of access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="cf6bc-114">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-114">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="cf6bc-115">Ces API vous aident à automatiser les flux de travail et à utiliser les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-115">Those APIs help you automate workflows and make use of Microsoft 365 Defender's capabilities.</span></span> <span data-ttu-id="cf6bc-116">Cet accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-116">This API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="cf6bc-117">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-117">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="cf6bc-118">En règle générale, vous devez effectuer les étapes suivantes pour utiliser ces API :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-118">In general, you'll need to take the following steps to use these APIs:</span></span>

- <span data-ttu-id="cf6bc-119">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-119">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="cf6bc-120">Obtenir un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-120">Get an access token using this application.</span></span>
- <span data-ttu-id="cf6bc-121">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-121">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="cf6bc-122">Étant donné que cette application est multi-locataire, vous aurez également besoin d’un [consentement administratif](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) de chaque client au nom de ses utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-122">Since this app is multi-tenant, you'll also need [admin consent](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) from each tenant on behalf of its users.</span></span>

<span data-ttu-id="cf6bc-123">Cet article explique comment :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-123">This article explains how to:</span></span>

- <span data-ttu-id="cf6bc-124">Créer une **application Azure ad mutualisée**</span><span class="sxs-lookup"><span data-stu-id="cf6bc-124">Create a **multi-tenant** Azure AD application</span></span>
- <span data-ttu-id="cf6bc-125">Obtenez un consentement autorisé de votre administrateur d’utilisateur pour votre application pour accéder à Microsoft 365 Defender dont les ressources ont besoin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-125">Get authorized consent from your user administrator for your application to access the Microsoft 365 Defender that resources it needs.</span></span>
- <span data-ttu-id="cf6bc-126">Obtenir un jeton d’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-126">Get an access token to Microsoft 365 Defender</span></span>
- <span data-ttu-id="cf6bc-127">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="cf6bc-127">Validate the token</span></span>

<span data-ttu-id="cf6bc-128">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-128">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="cf6bc-129">Ces API vous aideront à automatiser les flux de travail et innoveront en fonction des fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-129">Those APIs will help you automate work flows and innovate based on Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="cf6bc-130">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-130">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="cf6bc-131">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-131">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="cf6bc-132">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-132">In general, you’ll need to take the following steps to use the APIs:</span></span>

- <span data-ttu-id="cf6bc-133">Créez une **application Azure ad mutualisée** .</span><span class="sxs-lookup"><span data-stu-id="cf6bc-133">Create a **multi-tenant** Azure AD application.</span></span>
- <span data-ttu-id="cf6bc-134">Obtenir l’autorisation de l’administrateur de votre application pour accéder aux ressources Microsoft 365 Defender dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-134">Get authorized (consent) by your user administrator for your application to access Microsoft 365 Defender resources it needs.</span></span>
- <span data-ttu-id="cf6bc-135">Obtenir un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-135">Get an access token using this application.</span></span>
- <span data-ttu-id="cf6bc-136">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-136">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="cf6bc-137">Les étapes suivantes vous guident dans la création d’une application Azure AD mutualisée, l’obtention d’un jeton d’accès à Microsoft 365 Defender et la validation du jeton.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-137">The following steps with guide you how to create a multi-tenant Azure AD application, get an access token to Microsoft 365 Defender and validate the token.</span></span>

## <a name="create-the-multi-tenant-app"></a><span data-ttu-id="cf6bc-138">Créer l’application mutualisée</span><span class="sxs-lookup"><span data-stu-id="cf6bc-138">Create the multi-tenant app</span></span>

1. <span data-ttu-id="cf6bc-139">Connectez-vous à [Azure](https://portal.azure.com) en tant qu’utilisateur doté du rôle d' **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="cf6bc-139">Sign in to [Azure](https://portal.azure.com) as a user with the **Global Administrator** role.</span></span>

2. <span data-ttu-id="cf6bc-140">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-140">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="cf6bc-142">Dans le formulaire d’inscription :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-142">In the registration form:</span></span>

   - <span data-ttu-id="cf6bc-143">Choisissez un nom pour votre application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-143">Choose a name for your application.</span></span>
   - <span data-ttu-id="cf6bc-144">Dans **types de comptes pris en charge**, sélectionnez **comptes dans n’importe quel annuaire d’organisation (tout annuaire Azure AD)-client**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-144">From **Supported account types**, select **Accounts in any organizational directory (Any Azure AD directory) - Multitenant**.</span></span>
   - <span data-ttu-id="cf6bc-145">Renseignez la section **URI de redirection** .</span><span class="sxs-lookup"><span data-stu-id="cf6bc-145">Fill out the **Redirect URI** section.</span></span> <span data-ttu-id="cf6bc-146">Sélectionnez type **Web** et donnez à l’URI de redirection la forme **https://portal.azure.com** .</span><span class="sxs-lookup"><span data-stu-id="cf6bc-146">Select type **Web** and give the redirect URI as **https://portal.azure.com**.</span></span>

   <span data-ttu-id="cf6bc-147">Une fois que vous avez fini de remplir le formulaire, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-147">After you're done filling out the form, select **Register**.</span></span>

   ![Image du formulaire inscrire un formulaire d’application](../..//media/atp-api-new-app-partner.png)

4. <span data-ttu-id="cf6bc-149">Sur la page de votre application, sélectionnez **autorisations d’API**  >  **Ajouter une**  >  **API mon organisation utilise** des >, tapez **Microsoft Threat Protection**, puis sélectionnez **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-149">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="cf6bc-150">Votre application peut maintenant accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-150">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="cf6bc-151">*Microsoft Threat Protection* est un ancien nom pour Microsoft 365 Defender et n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-151">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="cf6bc-152">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-152">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de la sélection des autorisations de l’API](../../media/apis-in-my-org-tab.PNG)

5. <span data-ttu-id="cf6bc-154">Sélectionnez **autorisations d’application**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-154">Select **Application permissions**.</span></span> <span data-ttu-id="cf6bc-155">Choisissez les autorisations appropriées pour votre scénario (par exemple, **incident. Read. All**), puis sélectionnez **Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-155">Choose the relevant permissions for your scenario (for example, **Incident.Read.All**), and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions.PNG)

    > [!NOTE]
    > <span data-ttu-id="cf6bc-157">Vous devez sélectionner les autorisations appropriées pour votre scénario.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-157">You need to select the relevant permissions for your scenario.</span></span> <span data-ttu-id="cf6bc-158">*Read All incidents* n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-158">*Read all incidents* is just an example.</span></span> <span data-ttu-id="cf6bc-159">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-159">To determine which permission you need, please look at the **Permissions** section in the API you want to call.</span></span>
    >
    > <span data-ttu-id="cf6bc-160">Par exemple, pour [exécuter des requêtes avancées](api-advanced-hunting.md), sélectionnez l’autorisation « exécuter des requêtes avancées »; pour [isoler un appareil](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), sélectionnez l’autorisation « isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="cf6bc-160">For instance, to [run advanced queries](api-advanced-hunting.md), select the 'Run advanced queries' permission; to [isolate a device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), select the 'Isolate machine' permission.</span></span>

6. <span data-ttu-id="cf6bc-161">Sélectionnez **accorder le consentement** de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-161">Select **Grant admin consent**.</span></span> <span data-ttu-id="cf6bc-162">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner **accorder le consentement** de l’administrateur pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-162">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

    ![Image des autorisations accorder](../../media/grant-consent.PNG)

7. <span data-ttu-id="cf6bc-164">Pour ajouter une clé secrète à l’application, sélectionnez **certificats & secrets**, ajoutez une description à la clé secrète, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-164">To add a secret to the application, select **Certificates & secrets**, add a description to the secret, then select **Add**.</span></span>

    > [!TIP]
    > <span data-ttu-id="cf6bc-165">Une fois que vous avez sélectionné **Ajouter**, sélectionnez **copier la valeur secrète générée**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-165">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="cf6bc-166">Vous ne pourrez pas récupérer la valeur secrète une fois que vous aurez quitté.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-166">You won't be able to retrieve the secret value after you leave.</span></span>

    ![Image de la clé créer une application](../../media/webapp-create-key2.png)

8. <span data-ttu-id="cf6bc-168">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-168">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="cf6bc-169">Elles sont indiquées sous **vue d’ensemble** sur votre application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-169">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

9. <span data-ttu-id="cf6bc-171">Ajoutez l’application au client de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-171">Add the application to your user's tenant.</span></span>

   <span data-ttu-id="cf6bc-172">Étant donné que votre application interagit avec Microsoft 365 Defender au nom de vos utilisateurs, elle doit être approuvée pour chaque client sur lequel vous envisagez de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-172">Since your application interacts with Microsoft 365 Defender on behalf of your users, it needs be approved for every tenant on which you intend to use it.</span></span>

   <span data-ttu-id="cf6bc-173">Un **administrateur général** du client de votre utilisateur doit afficher le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-173">A **Global Administrator** from your user's tenant needs to view the consent link and approve your application.</span></span>

   <span data-ttu-id="cf6bc-174">Le lien de consentement est de la forme :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-174">Consent link is of the form:</span></span>

   ```HTTP
   https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=00000000-0000-0000-0000-000000000000&response_type=code&sso_reload=true
   ```

   <span data-ttu-id="cf6bc-175">Les chiffres `00000000-0000-0000-0000-000000000000` doivent être remplacés par l’ID de votre application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-175">The digits `00000000-0000-0000-0000-000000000000` should be replaced with your Application ID.</span></span>

   <span data-ttu-id="cf6bc-176">Après avoir cliqué sur le lien de consentement, connectez-vous à l’aide de l’administrateur général du client de l’utilisateur et accordez l’application.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-176">After clicking on the consent link, sign in with the Global Administrator of the user's tenant and consent the application.</span></span>

   ![Image de consentement](../../media/app-consent-partner.png)

   <span data-ttu-id="cf6bc-178">Vous devrez également demander à votre utilisateur son ID de client.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-178">You'll also need to ask your user for their tenant ID.</span></span> <span data-ttu-id="cf6bc-179">L’ID de locataire est l’un des identificateurs utilisés pour acquérir des jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-179">The tenant ID is one of the identifiers used to acquire access tokens.</span></span>

- <span data-ttu-id="cf6bc-180">**Terminé!**</span><span class="sxs-lookup"><span data-stu-id="cf6bc-180">**Done!**</span></span> <span data-ttu-id="cf6bc-181">Vous avez correctement inscrit une application !</span><span class="sxs-lookup"><span data-stu-id="cf6bc-181">You've successfully registered an application!</span></span>
- <span data-ttu-id="cf6bc-182">Voir des exemples ci-dessous pour l’acquisition et la validation de jetons.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-182">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="cf6bc-183">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="cf6bc-183">Get an access token</span></span>

<span data-ttu-id="cf6bc-184">Pour plus d’informations sur les jetons Azure AD, consultez le [didacticiel Azure ad](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-184">For more information on Azure AD tokens, see the [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf6bc-185">Bien que les exemples de cette section vous encouragent à coller des valeurs secrètes à des fins de test, vous ne devez **jamais coder les secrets** dans une application exécutée en production.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-185">Although the examples in this section encourage you to paste in secret values for testing purposes, you should **never hardcode secrets** into an application running in production.</span></span> <span data-ttu-id="cf6bc-186">Un tiers peut utiliser votre clé secrète pour accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-186">A third party could use your secret to access resources.</span></span> <span data-ttu-id="cf6bc-187">Vous pouvez protéger les secrets de votre application en utilisant [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-187">You can help keep your app's secrets secure by using [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/about-keys-secrets-certificates).</span></span> <span data-ttu-id="cf6bc-188">Pour obtenir un exemple pratique de la façon dont vous pouvez protéger votre application, voir [Manage secrets in your Server Apps with Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-188">For a practical example of how you can protect your app, see [Manage secrets in your server apps with Azure Key Vault](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/).</span></span>

> [!TIP]
> <span data-ttu-id="cf6bc-189">Dans les exemples suivants, utilisez l’ID de client d’un utilisateur pour tester le fonctionnement du script.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-189">In the following examples, use a user's tenant ID to test that the script is working.</span></span>

### <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="cf6bc-190">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="cf6bc-190">Get an access token using PowerShell</span></span>

```PowerShell
# This code gets the application context token and saves it to a file named "Latest-token.txt" under the current directory.

$tenantId = '' # Paste your directory (tenant) ID here
$clientId = '' # Paste your application (client) ID here
$appSecret = '' # Paste your own app secret here to test, then store it in a safe place!

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

### <a name="get-an-access-token-using-c"></a><span data-ttu-id="cf6bc-191">Obtenir un jeton d’accès à l’aide de C\#</span><span class="sxs-lookup"><span data-stu-id="cf6bc-191">Get an access token using C\#</span></span>

> [!NOTE]
> <span data-ttu-id="cf6bc-192">Le code suivant a été testé avec NuGet Microsoft. IdentityModel. clients. ActiveDirectory 3.19.8.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-192">The following code was tested with Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span></span>

1. <span data-ttu-id="cf6bc-193">Créez une nouvelle application console.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-193">Create a new console application.</span></span>
1. <span data-ttu-id="cf6bc-194">Installez NuGet [Microsoft. IdentityModel. clients. ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-194">Install NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span></span>
1. <span data-ttu-id="cf6bc-195">Ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-195">Add the following line:</span></span>

    ```C#
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

1. <span data-ttu-id="cf6bc-196">Copiez et collez le code suivant dans votre application (n’oubliez pas de mettre à jour les trois variables : `tenantId` , `clientId` , `appSecret` ) :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-196">Copy and paste the following code into your app (don't forget to update the three variables: `tenantId`, `clientId`, `appSecret`):</span></span>

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

### <a name="get-an-access-token-using-python"></a><span data-ttu-id="cf6bc-197">Obtenir un jeton d’accès à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="cf6bc-197">Get an access token using Python</span></span>

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

### <a name="get-an-access-token-using-curl"></a><span data-ttu-id="cf6bc-198">Obtenir un jeton d’accès à l’aide de la boucle</span><span class="sxs-lookup"><span data-stu-id="cf6bc-198">Get an access token using curl</span></span>

> [!NOTE]
> <span data-ttu-id="cf6bc-199">La fonction bouclé est préinstallée sur Windows 10, versions 1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-199">Curl is pre-installed on Windows 10, versions 1803 and later.</span></span> <span data-ttu-id="cf6bc-200">Pour les autres versions de Windows, téléchargez et installez l’outil directement à partir du [site Web officiel](https://curl.haxx.se/windows/).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-200">For other versions of Windows, download and install the tool directly from the [official curl website](https://curl.haxx.se/windows/).</span></span>

1. <span data-ttu-id="cf6bc-201">Ouvrez une invite de commandes et définissez CLIENT_ID à votre ID d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-201">Open a command prompt, and set CLIENT_ID to your Azure application ID.</span></span>
1. <span data-ttu-id="cf6bc-202">Définissez CLIENT_SECRET à la clé secrète de votre application Azure.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-202">Set CLIENT_SECRET to your Azure application secret.</span></span>
1. <span data-ttu-id="cf6bc-203">Définissez TENANT_ID sur l’ID de client Azure de l’utilisateur qui souhaite utiliser votre application pour accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-203">Set TENANT_ID to the Azure tenant ID of the user that wants to use your app to access Microsoft 365 Defender.</span></span>
1. <span data-ttu-id="cf6bc-204">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-204">Run the following command:</span></span>

```bash
curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://securitycenter.onmicrosoft.com/windowsatpservice/.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
```

<span data-ttu-id="cf6bc-205">Une réponse réussie se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-205">A successful response will look like this:</span></span>

```bash
{"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
```

## <a name="validate-the-token"></a><span data-ttu-id="cf6bc-206">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="cf6bc-206">Validate the token</span></span>

1. <span data-ttu-id="cf6bc-207">Copiez et collez le jeton dans le site Web du [validateur de jeton Web JSON, JWT,](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-207">Copy and paste the token into the [JSON web token validator website, JWT,](https://jwt.ms) to decode it.</span></span>
1. <span data-ttu-id="cf6bc-208">Assurez-vous que la revendication de *rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-208">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

<span data-ttu-id="cf6bc-209">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec ```Incidents.Read.All``` , ```Incidents.ReadWrite.All``` et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="cf6bc-209">In the following image, you can see a decoded token acquired from an app, with ```Incidents.Read.All```, ```Incidents.ReadWrite.All```, and ```AdvancedHunting.Read.All``` permissions:</span></span>

![Image de la validation du jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-the-microsoft-365-defender-api"></a><span data-ttu-id="cf6bc-211">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-211">Use the token to access the Microsoft 365 Defender API</span></span>

1. <span data-ttu-id="cf6bc-212">Choisissez l’API que vous souhaitez utiliser (incidents ou chasse avancée).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-212">Choose the API you want to use (incidents, or advanced hunting).</span></span> <span data-ttu-id="cf6bc-213">Pour plus d’informations, consultez la rubrique [API Microsoft 365 Defender prises en charge](api-supported.md).</span><span class="sxs-lookup"><span data-stu-id="cf6bc-213">For more information, see [Supported Microsoft 365 Defender APIs](api-supported.md).</span></span>
2. <span data-ttu-id="cf6bc-214">Dans la requête HTTP que vous allez envoyer, définissez l’en-tête d’autorisation sur `"Bearer" <token>` , le *porteur* étant le modèle d’autorisation et le *jeton* comme jeton validé.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-214">In the http request you're about to send, set the authorization header to `"Bearer" <token>`, *Bearer* being the authorization scheme, and *token* being your validated token.</span></span>
3. <span data-ttu-id="cf6bc-215">Le jeton expire dans une heure.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-215">The token will expire within one hour.</span></span> <span data-ttu-id="cf6bc-216">Vous pouvez envoyer plusieurs demandes pendant ce temps avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-216">You can send more than one request during this time  with the same token.</span></span>

<span data-ttu-id="cf6bc-217">L’exemple suivant montre comment envoyer une demande pour obtenir une liste d’incidents **à l’aide de C#**.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-217">The following example shows how to send a request to get a list of incidents **using C#**.</span></span>

```C#
   var httpClient = new HttpClient();
   var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

   request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

   var response = httpClient.SendAsync(request).GetAwaiter().GetResult();
```

## <a name="related-articles"></a><span data-ttu-id="cf6bc-218">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="cf6bc-218">Related articles</span></span>

- [<span data-ttu-id="cf6bc-219">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-219">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="cf6bc-220">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf6bc-220">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="cf6bc-221">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="cf6bc-221">Create a 'Hello world' application</span></span>](api-hello-world.md)
- [<span data-ttu-id="cf6bc-222">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf6bc-222">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md)
- [<span data-ttu-id="cf6bc-223">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf6bc-223">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md)
- [<span data-ttu-id="cf6bc-224">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="cf6bc-224">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="cf6bc-225">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cf6bc-225">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="cf6bc-226">Gérer les secrets dans vos applications serveur avec le coffre de clés Azure</span><span class="sxs-lookup"><span data-stu-id="cf6bc-226">Manage secrets in your server apps with Azure Key Vault</span></span>](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="cf6bc-227">Autorisation 2,0 OAuth pour l’authentification de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="cf6bc-227">OAuth 2.0 authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
