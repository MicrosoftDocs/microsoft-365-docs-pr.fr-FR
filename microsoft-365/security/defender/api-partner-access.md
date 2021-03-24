---
title: Accès des partenaires via les API Microsoft 365 Defender
description: Découvrez comment créer une application pour obtenir un accès par programme à Microsoft 365 Defender pour le compte de vos utilisateurs.
keywords: partenaire, accès, api, client multiple, consentement, jeton d’accès, application
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 46876fef8a0279ee350d57fdc85aeced82696656
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062038"
---
# <a name="create-an-app-with-partner-access-to-microsoft-365-defender-apis"></a><span data-ttu-id="6f248-104">Créer une application avec un accès partenaire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-104">Create an app with partner access to Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="6f248-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6f248-105">**Applies to:**</span></span>

- <span data-ttu-id="6f248-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f248-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="6f248-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f248-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="6f248-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="6f248-109">Cette page explique comment créer une application Azure Active Directory qui dispose d’un accès par programmation à Microsoft 365 Defender, pour le compte d’utilisateurs sur plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="6f248-109">This page describes how to create an Azure Active Directory app that has programmatic access to Microsoft 365 Defender, on behalf of users across multiple tenants.</span></span> <span data-ttu-id="6f248-110">Les applications multi-clients sont utiles pour servir de grands groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6f248-110">Multi-tenant apps are useful for serving large groups of users.</span></span>

<span data-ttu-id="6f248-111">Si vous avez besoin d’un accès par programme à Microsoft 365 Defender pour le compte d’un seul utilisateur, voir Créer une application pour accéder aux API [Microsoft 365 Defender](api-create-app-user-context.md)au nom d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f248-111">If you need programmatic access to Microsoft 365 Defender on behalf of a single user, see [Create an app to access Microsoft 365 Defender APIs on behalf of a user](api-create-app-user-context.md).</span></span> <span data-ttu-id="6f248-112">Si vous avez besoin d’un accès sans utilisateur explicitement défini (par exemple, si vous écrivez une application en arrière-plan ou un daemon), voir Créer une application pour accéder à [Microsoft 365 Defender](api-create-app-web.md)sans utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f248-112">If you need access without a user explicitly defined (for example, if you're writing a background app or daemon), see [Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md).</span></span> <span data-ttu-id="6f248-113">If you’re not sure which kind of access you need, see [Get started](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="6f248-113">If you're not sure which kind of access you need, see [Get started](api-access.md).</span></span>

<span data-ttu-id="6f248-114">Microsoft 365 Defender expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="6f248-114">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="6f248-115">Ces API vous aident à automatiser les flux de travail et à utiliser les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-115">Those APIs help you automate workflows and make use of Microsoft 365 Defender's capabilities.</span></span> <span data-ttu-id="6f248-116">Cet accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="6f248-116">This API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="6f248-117">Pour plus d’informations, voir flux de code [d’autorisation OAuth 2.0.](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="6f248-117">For more information, see [OAuth 2.0 Authorization Code Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="6f248-118">En règle générale, vous devez suivre les étapes suivantes pour utiliser ces API :</span><span class="sxs-lookup"><span data-stu-id="6f248-118">In general, you'll need to take the following steps to use these APIs:</span></span>

- <span data-ttu-id="6f248-119">Créez une application Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6f248-119">Create an Azure Active Directory (Azure AD) application.</span></span>
- <span data-ttu-id="6f248-120">Obtenez un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="6f248-120">Get an access token using this application.</span></span>
- <span data-ttu-id="6f248-121">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-121">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="6f248-122">Étant donné que cette application est multi-locataire, vous aurez également besoin du consentement de l’administrateur de chaque client pour le compte de ses utilisateurs. [](/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant)</span><span class="sxs-lookup"><span data-stu-id="6f248-122">Since this app is multi-tenant, you'll also need [admin consent](/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) from each tenant on behalf of its users.</span></span>

<span data-ttu-id="6f248-123">Cet article explique comment :</span><span class="sxs-lookup"><span data-stu-id="6f248-123">This article explains how to:</span></span>

- <span data-ttu-id="6f248-124">Créer une application Azure AD **multi-client**</span><span class="sxs-lookup"><span data-stu-id="6f248-124">Create a **multi-tenant** Azure AD application</span></span>
- <span data-ttu-id="6f248-125">Obtenez l’autorisation de votre administrateur utilisateur pour que votre application accède à Microsoft 365 Defender avec les ressources dont elle a besoin.</span><span class="sxs-lookup"><span data-stu-id="6f248-125">Get authorized consent from your user administrator for your application to access the Microsoft 365 Defender that resources it needs.</span></span>
- <span data-ttu-id="6f248-126">Obtenir un jeton d’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-126">Get an access token to Microsoft 365 Defender</span></span>
- <span data-ttu-id="6f248-127">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="6f248-127">Validate the token</span></span>

<span data-ttu-id="6f248-128">Microsoft 365 Defender expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="6f248-128">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="6f248-129">Ces API vous aideront à automatiser les flux de travail et à faire preuve d’innovation en fonction des fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-129">Those APIs will help you automate work flows and innovate based on Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="6f248-130">L’accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="6f248-130">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="6f248-131">Pour plus d’informations, voir flux de code [d’autorisation OAuth 2.0.](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="6f248-131">For more information, see [OAuth 2.0 Authorization Code Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="6f248-132">En règle générale, vous devez suivre les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="6f248-132">In general, you’ll need to take the following steps to use the APIs:</span></span>

- <span data-ttu-id="6f248-133">Créez une application Azure AD à **plusieurs** locataires.</span><span class="sxs-lookup"><span data-stu-id="6f248-133">Create a **multi-tenant** Azure AD application.</span></span>
- <span data-ttu-id="6f248-134">Obtenez l’autorisation (consentement) de votre administrateur utilisateur pour que votre application accède aux ressources Microsoft 365 Defender dont elle a besoin.</span><span class="sxs-lookup"><span data-stu-id="6f248-134">Get authorized (consent) by your user administrator for your application to access Microsoft 365 Defender resources it needs.</span></span>
- <span data-ttu-id="6f248-135">Obtenez un jeton d’accès à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="6f248-135">Get an access token using this application.</span></span>
- <span data-ttu-id="6f248-136">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-136">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="6f248-137">Les étapes suivantes vous guident dans la création d’une application Azure AD à plusieurs clients, l’utilisation d’un jeton d’accès à Microsoft 365 Defender et la validation du jeton.</span><span class="sxs-lookup"><span data-stu-id="6f248-137">The following steps with guide you how to create a multi-tenant Azure AD application, get an access token to Microsoft 365 Defender and validate the token.</span></span>

## <a name="create-the-multi-tenant-app"></a><span data-ttu-id="6f248-138">Créer l’application multi-client</span><span class="sxs-lookup"><span data-stu-id="6f248-138">Create the multi-tenant app</span></span>

1. <span data-ttu-id="6f248-139">Connectez-vous [à Azure](https://portal.azure.com) en tant qu’utilisateur avec le **rôle Administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="6f248-139">Sign in to [Azure](https://portal.azure.com) as a user with the **Global Administrator** role.</span></span>

2. <span data-ttu-id="6f248-140">Accédez **à Azure Active Directory** App  >  **registrations** New  >  **registration**.</span><span class="sxs-lookup"><span data-stu-id="6f248-140">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span>

   ![Image de Microsoft Azure et navigation vers l’inscription de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="6f248-142">Dans le formulaire d’inscription :</span><span class="sxs-lookup"><span data-stu-id="6f248-142">In the registration form:</span></span>

   - <span data-ttu-id="6f248-143">Choisissez un nom pour votre application.</span><span class="sxs-lookup"><span data-stu-id="6f248-143">Choose a name for your application.</span></span>
   - <span data-ttu-id="6f248-144">À **partir des types de** comptes pris en charge, sélectionnez Comptes dans n’importe quel annuaire d’organisation (n’importe quel annuaire Azure **AD) - Multi-client**.</span><span class="sxs-lookup"><span data-stu-id="6f248-144">From **Supported account types**, select **Accounts in any organizational directory (Any Azure AD directory) - Multitenant**.</span></span>
   - <span data-ttu-id="6f248-145">Remplissez la section **URI de** redirection.</span><span class="sxs-lookup"><span data-stu-id="6f248-145">Fill out the **Redirect URI** section.</span></span> <span data-ttu-id="6f248-146">Sélectionnez type **Web** et donnez l’URI de redirection en **https://portal.azure.com** tant que .</span><span class="sxs-lookup"><span data-stu-id="6f248-146">Select type **Web** and give the redirect URI as **https://portal.azure.com**.</span></span>

   <span data-ttu-id="6f248-147">Une fois que vous avez terminé de remplir le formulaire, sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="6f248-147">After you're done filling out the form, select **Register**.</span></span>

   ![Image du formulaire Inscrire une application](../..//media/atp-api-new-app-partner.png)

4. <span data-ttu-id="6f248-149">Dans la page de votre application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon organisation utilise >, tapez Protection Microsoft contre les menaces, puis sélectionnez  >    >   Protection **Microsoft contre les menaces.** </span><span class="sxs-lookup"><span data-stu-id="6f248-149">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and select **Microsoft Threat Protection**.</span></span> <span data-ttu-id="6f248-150">Votre application peut désormais accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-150">Your app can now access Microsoft 365 Defender.</span></span>

   > [!TIP]
   > <span data-ttu-id="6f248-151">*Microsoft Threat Protection* est un ancien nom de Microsoft 365 Defender et n’apparaîtra pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="6f248-151">*Microsoft Threat Protection* is a former name for Microsoft 365 Defender, and will not appear in the original list.</span></span> <span data-ttu-id="6f248-152">Vous devez commencer à écrire son nom dans la zone de texte pour qu’il apparaisse.</span><span class="sxs-lookup"><span data-stu-id="6f248-152">You need to start writing its name in the text box to see it appear.</span></span>

   ![Image de la sélection des autorisations d’API](../../media/apis-in-my-org-tab.PNG)

5. <span data-ttu-id="6f248-154">Sélectionnez **les autorisations d’application.**</span><span class="sxs-lookup"><span data-stu-id="6f248-154">Select **Application permissions**.</span></span> <span data-ttu-id="6f248-155">Choisissez les autorisations pertinentes pour votre scénario (par exemple, **Incident.Read.All),** puis **sélectionnez Ajouter des autorisations.**</span><span class="sxs-lookup"><span data-stu-id="6f248-155">Choose the relevant permissions for your scenario (for example, **Incident.Read.All**), and then select **Add permissions**.</span></span>

   ![Image de l’accès à l’API et de la sélection d’API](../../media/request-api-permissions.PNG)

    > [!NOTE]
    > <span data-ttu-id="6f248-157">Vous devez sélectionner les autorisations pertinentes pour votre scénario.</span><span class="sxs-lookup"><span data-stu-id="6f248-157">You need to select the relevant permissions for your scenario.</span></span> <span data-ttu-id="6f248-158">*Lire tous les incidents* n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="6f248-158">*Read all incidents* is just an example.</span></span> <span data-ttu-id="6f248-159">Pour déterminer l’autorisation qui vous est nécessaire, consultez la section **Autorisations** de l’API que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="6f248-159">To determine which permission you need, please look at the **Permissions** section in the API you want to call.</span></span>
    >
    > <span data-ttu-id="6f248-160">Par exemple, pour [exécuter des requêtes avancées,](api-advanced-hunting.md)sélectionnez l’autorisation « Exécuter des requêtes avancées » ; pour [isoler un appareil,](/windows/security/threat-protection/microsoft-defender-atp/isolate-machine)sélectionnez l’autorisation « Isoler l’ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="6f248-160">For instance, to [run advanced queries](api-advanced-hunting.md), select the 'Run advanced queries' permission; to [isolate a device](/windows/security/threat-protection/microsoft-defender-atp/isolate-machine), select the 'Isolate machine' permission.</span></span>

6. <span data-ttu-id="6f248-161">Sélectionnez **Accorder le consentement de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="6f248-161">Select **Grant admin consent**.</span></span> <span data-ttu-id="6f248-162">Chaque fois que vous ajoutez une autorisation, vous devez sélectionner Accorder le **consentement de l’administrateur** pour qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="6f248-162">Every time you add a permission, you must select **Grant admin consent** for it to take effect.</span></span>

    ![Image de l’octroi d’autorisations](../../media/grant-consent.PNG)

7. <span data-ttu-id="6f248-164">Pour ajouter une secret à l’application, sélectionnez **Certificats & secrets,** ajoutez une description à la secret, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6f248-164">To add a secret to the application, select **Certificates & secrets**, add a description to the secret, then select **Add**.</span></span>

    > [!TIP]
    > <span data-ttu-id="6f248-165">Après avoir sélectionné **Ajouter,** **sélectionnez copier la valeur de secret générée.**</span><span class="sxs-lookup"><span data-stu-id="6f248-165">After you select **Add**, select **copy the generated secret value**.</span></span> <span data-ttu-id="6f248-166">Vous ne pourrez pas récupérer la valeur secrète après votre départ.</span><span class="sxs-lookup"><span data-stu-id="6f248-166">You won't be able to retrieve the secret value after you leave.</span></span>

    ![Image de la clé de création d’application](../../media/webapp-create-key2.png)

8. <span data-ttu-id="6f248-168">Enregistrez votre ID d’application et votre ID de client dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="6f248-168">Record your application ID and your tenant ID somewhere safe.</span></span> <span data-ttu-id="6f248-169">Ils sont répertoriés sous Vue **d’ensemble** sur la page de votre application.</span><span class="sxs-lookup"><span data-stu-id="6f248-169">They're listed under **Overview** on your application page.</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)

9. <span data-ttu-id="6f248-171">Ajoutez l’application au client de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f248-171">Add the application to your user's tenant.</span></span>

   <span data-ttu-id="6f248-172">Étant donné que votre application interagit avec Microsoft 365 Defender pour le compte de vos utilisateurs, elle doit être approuvée pour chaque client sur lequel vous avez l’intention de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="6f248-172">Since your application interacts with Microsoft 365 Defender on behalf of your users, it needs be approved for every tenant on which you intend to use it.</span></span>

   <span data-ttu-id="6f248-173">Un **administrateur général du** client de votre utilisateur doit afficher le lien de consentement et approuver votre application.</span><span class="sxs-lookup"><span data-stu-id="6f248-173">A **Global Administrator** from your user's tenant needs to view the consent link and approve your application.</span></span>

   <span data-ttu-id="6f248-174">Le lien de consentement est de la forme :</span><span class="sxs-lookup"><span data-stu-id="6f248-174">Consent link is of the form:</span></span>

   ```HTTP
   https://login.microsoftonline.com/common/oauth2/authorize?prompt=consent&client_id=00000000-0000-0000-0000-000000000000&response_type=code&sso_reload=true
   ```

   <span data-ttu-id="6f248-175">Les chiffres `00000000-0000-0000-0000-000000000000` doivent être remplacés par votre ID d’application.</span><span class="sxs-lookup"><span data-stu-id="6f248-175">The digits `00000000-0000-0000-0000-000000000000` should be replaced with your Application ID.</span></span>

   <span data-ttu-id="6f248-176">Après avoir cliqué sur le lien de consentement, connectez-vous avec l’administrateur général du client de l’utilisateur et consentez à l’application.</span><span class="sxs-lookup"><span data-stu-id="6f248-176">After clicking on the consent link, sign in with the Global Administrator of the user's tenant and consent the application.</span></span>

   ![Image de consentement](../../media/app-consent-partner.png)

   <span data-ttu-id="6f248-178">Vous devez également demander à votre utilisateur son ID de client.</span><span class="sxs-lookup"><span data-stu-id="6f248-178">You'll also need to ask your user for their tenant ID.</span></span> <span data-ttu-id="6f248-179">L’ID de client est l’un des identificateurs utilisés pour acquérir des jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="6f248-179">The tenant ID is one of the identifiers used to acquire access tokens.</span></span>

- <span data-ttu-id="6f248-180">**Terminé !**</span><span class="sxs-lookup"><span data-stu-id="6f248-180">**Done!**</span></span> <span data-ttu-id="6f248-181">Vous avez réussi à inscrire une application !</span><span class="sxs-lookup"><span data-stu-id="6f248-181">You've successfully registered an application!</span></span>
- <span data-ttu-id="6f248-182">Voir les exemples ci-dessous pour l’acquisition et la validation des jetons.</span><span class="sxs-lookup"><span data-stu-id="6f248-182">See examples below for token acquisition and validation.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="6f248-183">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="6f248-183">Get an access token</span></span>

<span data-ttu-id="6f248-184">Pour plus d’informations sur les jetons Azure AD, voir le [didacticiel Azure AD.](/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="6f248-184">For more information on Azure AD tokens, see the [Azure AD tutorial](/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f248-185">Bien que les exemples de cette section vous encouragent à coller des valeurs secrètes à des fins de test, vous ne devez jamais coder en dur des **secrets** dans une application en cours d’exécution en production.</span><span class="sxs-lookup"><span data-stu-id="6f248-185">Although the examples in this section encourage you to paste in secret values for testing purposes, you should **never hardcode secrets** into an application running in production.</span></span> <span data-ttu-id="6f248-186">Un tiers peut utiliser votre secret pour accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="6f248-186">A third party could use your secret to access resources.</span></span> <span data-ttu-id="6f248-187">Vous pouvez aider à sécuriser les secrets de votre application à l’aide [d’Azure Key Vault](/azure/key-vault/general/about-keys-secrets-certificates).</span><span class="sxs-lookup"><span data-stu-id="6f248-187">You can help keep your app's secrets secure by using [Azure Key Vault](/azure/key-vault/general/about-keys-secrets-certificates).</span></span> <span data-ttu-id="6f248-188">Pour obtenir un exemple pratique de la façon dont vous pouvez protéger votre application, voir Gérer les secrets dans vos applications serveur avec [Azure Key Vault](/learn/modules/manage-secrets-with-azure-key-vault/).</span><span class="sxs-lookup"><span data-stu-id="6f248-188">For a practical example of how you can protect your app, see [Manage secrets in your server apps with Azure Key Vault](/learn/modules/manage-secrets-with-azure-key-vault/).</span></span>

> [!TIP]
> <span data-ttu-id="6f248-189">Dans les exemples suivants, utilisez l’ID de locataire d’un utilisateur pour tester le fonctionnement du script.</span><span class="sxs-lookup"><span data-stu-id="6f248-189">In the following examples, use a user's tenant ID to test that the script is working.</span></span>

### <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="6f248-190">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f248-190">Get an access token using PowerShell</span></span>

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

### <a name="get-an-access-token-using-c"></a><span data-ttu-id="6f248-191">Obtenir un jeton d’accès à l’aide de C\#</span><span class="sxs-lookup"><span data-stu-id="6f248-191">Get an access token using C\#</span></span>

> [!NOTE]
> <span data-ttu-id="6f248-192">Le code suivant a été testé avec Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span><span class="sxs-lookup"><span data-stu-id="6f248-192">The following code was tested with Nuget Microsoft.IdentityModel.Clients.ActiveDirectory 3.19.8.</span></span>

1. <span data-ttu-id="6f248-193">Créez une application console.</span><span class="sxs-lookup"><span data-stu-id="6f248-193">Create a new console application.</span></span>
1. <span data-ttu-id="6f248-194">Installez NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span><span class="sxs-lookup"><span data-stu-id="6f248-194">Install NuGet [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).</span></span>
1. <span data-ttu-id="6f248-195">Ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="6f248-195">Add the following line:</span></span>

    ```C#
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    ```

1. <span data-ttu-id="6f248-196">Copiez et collez le code suivant dans votre application (n’oubliez pas de mettre à jour les trois variables `tenantId` : , , ) `clientId` `appSecret` :</span><span class="sxs-lookup"><span data-stu-id="6f248-196">Copy and paste the following code into your app (don't forget to update the three variables: `tenantId`, `clientId`, `appSecret`):</span></span>

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

### <a name="get-an-access-token-using-python"></a><span data-ttu-id="6f248-197">Obtenir un jeton d’accès à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="6f248-197">Get an access token using Python</span></span>

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

### <a name="get-an-access-token-using-curl"></a><span data-ttu-id="6f248-198">Obtenir un jeton d’accès à l’aide de l’outil</span><span class="sxs-lookup"><span data-stu-id="6f248-198">Get an access token using curl</span></span>

> [!NOTE]
> <span data-ttu-id="6f248-199">Il est préinstallé sur Windows 10, versions 1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6f248-199">Curl is pre-installed on Windows 10, versions 1803 and later.</span></span> <span data-ttu-id="6f248-200">Pour les autres versions de Windows, téléchargez et installez l’outil directement à partir du site [web officiel de lancement.](https://curl.haxx.se/windows/)</span><span class="sxs-lookup"><span data-stu-id="6f248-200">For other versions of Windows, download and install the tool directly from the [official curl website](https://curl.haxx.se/windows/).</span></span>

1. <span data-ttu-id="6f248-201">Ouvrez une invite de commandes et définissez CLIENT_ID sur votre ID d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="6f248-201">Open a command prompt, and set CLIENT_ID to your Azure application ID.</span></span>
1. <span data-ttu-id="6f248-202">Définissez CLIENT_SECRET sur votre secret d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="6f248-202">Set CLIENT_SECRET to your Azure application secret.</span></span>
1. <span data-ttu-id="6f248-203">Définissez TENANT_ID sur l’ID de locataire Azure de l’utilisateur qui souhaite utiliser votre application pour accéder à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6f248-203">Set TENANT_ID to the Azure tenant ID of the user that wants to use your app to access Microsoft 365 Defender.</span></span>
1. <span data-ttu-id="6f248-204">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6f248-204">Run the following command:</span></span>

```bash
curl -i -X POST -H "Content-Type:application/x-www-form-urlencoded" -d "grant_type=client_credentials" -d "client_id=%CLIENT_ID%" -d "scope=https://securitycenter.onmicrosoft.com/windowsatpservice/.default" -d "client_secret=%CLIENT_SECRET%" "https://login.microsoftonline.com/%TENANT_ID%/oauth2/v2.0/token" -k
```

<span data-ttu-id="6f248-205">Une réponse réussie ressemblera à ceci :</span><span class="sxs-lookup"><span data-stu-id="6f248-205">A successful response will look like this:</span></span>

```bash
{"token_type":"Bearer","expires_in":3599,"ext_expires_in":0,"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIn <truncated> aWReH7P0s0tjTBX8wGWqJUdDA"}
```

## <a name="validate-the-token"></a><span data-ttu-id="6f248-206">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="6f248-206">Validate the token</span></span>

1. <span data-ttu-id="6f248-207">Copiez et collez le jeton dans le site web de validation de jeton [web JSON, JWT,](https://jwt.ms) pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="6f248-207">Copy and paste the token into the [JSON web token validator website, JWT,](https://jwt.ms) to decode it.</span></span>
1. <span data-ttu-id="6f248-208">Assurez-vous que la revendication *de rôles* dans le jeton décodé contient les autorisations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="6f248-208">Make sure that the *roles* claim within the decoded token contains the desired permissions.</span></span>

<span data-ttu-id="6f248-209">Dans l’image suivante, vous pouvez voir un jeton décodé acquis à partir d’une application, avec ```Incidents.Read.All``` ```Incidents.ReadWrite.All``` , et des ```AdvancedHunting.Read.All``` autorisations :</span><span class="sxs-lookup"><span data-stu-id="6f248-209">In the following image, you can see a decoded token acquired from an app, with ```Incidents.Read.All```, ```Incidents.ReadWrite.All```, and ```AdvancedHunting.Read.All``` permissions:</span></span>

![Image de validation de jeton](../../media/webapp-decoded-token.png)

## <a name="use-the-token-to-access-the-microsoft-365-defender-api"></a><span data-ttu-id="6f248-211">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-211">Use the token to access the Microsoft 365 Defender API</span></span>

1. <span data-ttu-id="6f248-212">Choisissez l’API que vous souhaitez utiliser (incidents ou recherche avancée).</span><span class="sxs-lookup"><span data-stu-id="6f248-212">Choose the API you want to use (incidents, or advanced hunting).</span></span> <span data-ttu-id="6f248-213">Pour plus d’informations, voir [API Microsoft 365 Defender pris en charge.](api-supported.md)</span><span class="sxs-lookup"><span data-stu-id="6f248-213">For more information, see [Supported Microsoft 365 Defender APIs](api-supported.md).</span></span>
2. <span data-ttu-id="6f248-214">Dans la requête http que vous êtes sur le point d’envoyer, définissez l’en-tête d’autorisation sur , le porteur étant le schéma d’autorisation et le jeton comme jeton `"Bearer" <token>` validé.  </span><span class="sxs-lookup"><span data-stu-id="6f248-214">In the http request you're about to send, set the authorization header to `"Bearer" <token>`, *Bearer* being the authorization scheme, and *token* being your validated token.</span></span>
3. <span data-ttu-id="6f248-215">Le jeton expire dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="6f248-215">The token will expire within one hour.</span></span> <span data-ttu-id="6f248-216">Vous pouvez envoyer plusieurs demandes pendant cette période avec le même jeton.</span><span class="sxs-lookup"><span data-stu-id="6f248-216">You can send more than one request during this time  with the same token.</span></span>

<span data-ttu-id="6f248-217">L’exemple suivant montre comment envoyer une demande pour obtenir une liste d’incidents à l’aide **de C#**.</span><span class="sxs-lookup"><span data-stu-id="6f248-217">The following example shows how to send a request to get a list of incidents **using C#**.</span></span>

```C#
   var httpClient = new HttpClient();
   var request = new HttpRequestMessage(HttpMethod.Get, "https://api.security.microsoft.com/api/incidents");

   request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

   var response = httpClient.SendAsync(request).GetAwaiter().GetResult();
```

## <a name="related-articles"></a><span data-ttu-id="6f248-218">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6f248-218">Related articles</span></span>

- [<span data-ttu-id="6f248-219">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-219">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="6f248-220">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f248-220">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="6f248-221">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="6f248-221">Create a 'Hello world' application</span></span>](api-hello-world.md)
- [<span data-ttu-id="6f248-222">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="6f248-222">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md)
- [<span data-ttu-id="6f248-223">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="6f248-223">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md)
- [<span data-ttu-id="6f248-224">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="6f248-224">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="6f248-225">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6f248-225">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="6f248-226">Gérer les secrets dans vos applications serveur avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="6f248-226">Manage secrets in your server apps with Azure Key Vault</span></span>](/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="6f248-227">Autorisation OAuth 2.0 pour la connexion de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="6f248-227">OAuth 2.0 authorization for user sign in and API access</span></span>](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)