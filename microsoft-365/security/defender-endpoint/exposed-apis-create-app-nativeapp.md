---
title: Utiliser les API Microsoft Defender pour les points de terminaison
ms.reviewer: ''
description: Découvrez comment concevoir une application Windows pour obtenir un accès par programmation à Microsoft Defender pour Endpoint sans utilisateur.
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
ms.openlocfilehash: 8f23a0b269986f4caa199ad3744c563fcc6ff6b2
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769100"
---
# <a name="use-microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="efe94-104">Utiliser les API Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="efe94-104">Use Microsoft Defender for Endpoint APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="efe94-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="efe94-105">**Applies to:**</span></span>
- [<span data-ttu-id="efe94-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="efe94-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="efe94-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="efe94-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="efe94-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="efe94-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="efe94-109">Cette page explique comment créer une application pour obtenir l’accès par programme à Defender for Endpoint pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="efe94-109">This page describes how to create an application to get programmatic access to Defender for Endpoint on behalf of a user.</span></span>

<span data-ttu-id="efe94-110">Si vous avez besoin d’un accès par programmation à Microsoft Defender pour endpoint sans utilisateur, reportez-vous à Access Microsoft Defender pour Endpoint avec le [contexte de l’application.](exposed-apis-create-app-webapp.md)</span><span class="sxs-lookup"><span data-stu-id="efe94-110">If you need programmatic access Microsoft Defender for Endpoint without a user, refer to [Access Microsoft Defender for Endpoint with application context](exposed-apis-create-app-webapp.md).</span></span>

<span data-ttu-id="efe94-111">Si vous n’êtes pas sûr de l’accès dont vous avez besoin, lisez la [page Introduction.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="efe94-111">If you are not sure which access you need, read the [Introduction page](apis-intro.md).</span></span>

<span data-ttu-id="efe94-112">Microsoft Defender pour point de terminaison expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="efe94-112">Microsoft Defender for Endpoint exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="efe94-113">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="efe94-113">Those APIs will enable you to automate work flows and innovate based on Microsoft Defender for Endpoint capabilities.</span></span> <span data-ttu-id="efe94-114">L’accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="efe94-114">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="efe94-115">Pour plus d’informations, [voir code d’autorisation OAuth 2.0 Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="efe94-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="efe94-116">En règle générale, vous devez suivre les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="efe94-116">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="efe94-117">Créer une application AAD</span><span class="sxs-lookup"><span data-stu-id="efe94-117">Create an AAD application</span></span>
- <span data-ttu-id="efe94-118">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="efe94-118">Get an access token using this application</span></span>
- <span data-ttu-id="efe94-119">Utiliser le jeton pour accéder à l’API Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="efe94-119">Use the token to access Defender for Endpoint API</span></span>

<span data-ttu-id="efe94-120">Cette page explique comment créer une application AAD, obtenir un jeton d’accès à Microsoft Defender pour le point de terminaison et valider le jeton.</span><span class="sxs-lookup"><span data-stu-id="efe94-120">This page explains how to create an AAD application, get an access token to Microsoft Defender for Endpoint and validate the token.</span></span>

>[!NOTE]
> <span data-ttu-id="efe94-121">Lorsque vous accédez à l’API Microsoft Defender pour endpoint pour le compte d’un utilisateur, vous avez besoin de l’autorisation d’application et de l’autorisation utilisateur correctes.</span><span class="sxs-lookup"><span data-stu-id="efe94-121">When accessing Microsoft Defender for Endpoint API on behalf of a user, you will need the correct Application permission and user permission.</span></span>
> <span data-ttu-id="efe94-122">Si vous n’êtes pas familiarisé avec les autorisations utilisateur sur Microsoft Defender pour le point de terminaison, voir Gérer l’accès au portail à l’aide du contrôle [d’accès basé sur les rôles.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="efe94-122">If you are not familiar with user permissions on Microsoft Defender for Endpoint, see [Manage portal access using role-based access control](rbac.md).</span></span>

>[!TIP]
> <span data-ttu-id="efe94-123">Si vous avez l’autorisation d’effectuer une action dans le portail, vous avez l’autorisation d’effectuer l’action dans l’API.</span><span class="sxs-lookup"><span data-stu-id="efe94-123">If you have the permission to perform an action in the portal, you have the permission to perform the action in the API.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="efe94-124">Créer une application</span><span class="sxs-lookup"><span data-stu-id="efe94-124">Create an app</span></span>

1. <span data-ttu-id="efe94-125">Connectez-vous [à Azure](https://portal.azure.com) avec un compte d’utilisateur ayant le **rôle Administrateur** général.</span><span class="sxs-lookup"><span data-stu-id="efe94-125">Log on to [Azure](https://portal.azure.com) with a user account that has the **Global Administrator** role.</span></span>

2. <span data-ttu-id="efe94-126">Accédez à **Azure Active Directory**  >  **Inscription de l’application Nouvelle**  >  **inscription.**</span><span class="sxs-lookup"><span data-stu-id="efe94-126">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de la Microsoft Azure et de la navigation vers l’inscription de l’application](images/atp-azure-new-app2.png)

3. <span data-ttu-id="efe94-128">Lorsque la page **Inscrire une application** s’affiche, saisissez les informations d’inscription de votre application :</span><span class="sxs-lookup"><span data-stu-id="efe94-128">When the **Register an application** page appears, enter your application's registration information:</span></span>

   - <span data-ttu-id="efe94-129">**Nom** : saisissez un nom d’application cohérent qui s’affichera pour les utilisateurs de l’application.</span><span class="sxs-lookup"><span data-stu-id="efe94-129">**Name** - Enter a meaningful application name that will be displayed to users of the app.</span></span>
   - <span data-ttu-id="efe94-130">**Types de compte pris en charge** : sélectionnez les comptes à prendre en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="efe94-130">**Supported account types** - Select which accounts you would like your application to support.</span></span>

       | <span data-ttu-id="efe94-131">Types de comptes pris en charge</span><span class="sxs-lookup"><span data-stu-id="efe94-131">Supported account types</span></span> | <span data-ttu-id="efe94-132">Description</span><span class="sxs-lookup"><span data-stu-id="efe94-132">Description</span></span> |
       |-------------------------|-------------|
       | <span data-ttu-id="efe94-133">**Comptes dans cet annuaire organisationnel uniquement**</span><span class="sxs-lookup"><span data-stu-id="efe94-133">**Accounts in this organizational directory only**</span></span> | <span data-ttu-id="efe94-134">Sélectionnez cette option si vous générez une application métier.</span><span class="sxs-lookup"><span data-stu-id="efe94-134">Select this option if you're building a line-of-business (LOB) application.</span></span> <span data-ttu-id="efe94-135">Cette option n’est pas disponible si vous n’inscrivez pas l’application dans un annuaire.</span><span class="sxs-lookup"><span data-stu-id="efe94-135">This option is not available if you're not registering the application in a directory.</span></span><br><br><span data-ttu-id="efe94-136">Cette option s’applique à un compte Azure AD à locataire unique seulement.</span><span class="sxs-lookup"><span data-stu-id="efe94-136">This option maps to Azure AD only single-tenant.</span></span><br><br><span data-ttu-id="efe94-137">Il s’agit de l’option par défaut, sauf si vous inscrivez l’application hors d’un annuaire.</span><span class="sxs-lookup"><span data-stu-id="efe94-137">This is the default option unless you're registering the app outside of a directory.</span></span> <span data-ttu-id="efe94-138">Dans les cas où l’application est inscrite hors d’un annuaire, l’option par défaut est comptes mutualisés Azure AD et comptes Microsoft personnels.</span><span class="sxs-lookup"><span data-stu-id="efe94-138">In cases where the app is registered outside of a directory, the default is Azure AD multi-tenant and personal Microsoft accounts.</span></span> |
       | <span data-ttu-id="efe94-139">**Comptes dans un annuaire organisationnel**</span><span class="sxs-lookup"><span data-stu-id="efe94-139">**Accounts in any organizational directory**</span></span> | <span data-ttu-id="efe94-140">Sélectionnez cette option si vous souhaitez cibler tous les clients professionnels et éducatifs.</span><span class="sxs-lookup"><span data-stu-id="efe94-140">Select this option if you would like to target all business and educational customers.</span></span><br><br><span data-ttu-id="efe94-141">Cette option s’applique à un compte Azure AD multi-locataire seulement.</span><span class="sxs-lookup"><span data-stu-id="efe94-141">This option maps to an Azure AD only multi-tenant.</span></span><br><br><span data-ttu-id="efe94-142">Si vous avez inscrit l’application comme compte Azure AD à locataire unique seulement, vous pouvez le mettre à jour vers un compte Azure AD multi-locataire et inversement via le panneau **Authentification**.</span><span class="sxs-lookup"><span data-stu-id="efe94-142">If you registered the app as Azure AD only single-tenant, you can update it to be Azure AD multi-tenant and back to single-tenant through the **Authentication** blade.</span></span> |
       | <span data-ttu-id="efe94-143">**Comptes dans un annuaire organisationnel et comptes personnels Microsoft**</span><span class="sxs-lookup"><span data-stu-id="efe94-143">**Accounts in any organizational directory and personal Microsoft accounts**</span></span> | <span data-ttu-id="efe94-144">Sélectionnez cette option pour cibler l’ensemble le plus large de clients.</span><span class="sxs-lookup"><span data-stu-id="efe94-144">Select this option to target the widest set of customers.</span></span><br><br><span data-ttu-id="efe94-145">Cette option s’applique à des comptes Microsoft personnels et Azure AD multi-locataires.</span><span class="sxs-lookup"><span data-stu-id="efe94-145">This option maps to Azure AD multi-tenant and personal Microsoft accounts.</span></span><br><br><span data-ttu-id="efe94-146">Si vous avez inscrit l’application comme comptes Microsoft personnels et Azure AD multi-locataires, vous ne pouvez pas modifier cela dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="efe94-146">If you registered the app as Azure AD multi-tenant and personal Microsoft accounts, you cannot change this in the UI.</span></span> <span data-ttu-id="efe94-147">Vous devez utiliser l’éditeur de manifeste de l’application pour modifier les types de compte pris en charge.</span><span class="sxs-lookup"><span data-stu-id="efe94-147">Instead, you must use the application manifest editor to change the supported account types.</span></span> |

   - <span data-ttu-id="efe94-148">**URI de redirection (facultatif)**  : sélectionnez le type d’application que vous créez, **Web** ou **Client public (mobile et bureau)**, puis entrez l’URI de redirection (ou URL de réponse).</span><span class="sxs-lookup"><span data-stu-id="efe94-148">**Redirect URI (optional)** - Select the type of app you're building, **Web** or **Public client (mobile & desktop)**, and then enter the redirect URI (or reply URL) for your application.</span></span>
       - <span data-ttu-id="efe94-149">Pour les applications web, indiquez l’URL de base de votre application.</span><span class="sxs-lookup"><span data-stu-id="efe94-149">For web applications, provide the base URL of your app.</span></span> <span data-ttu-id="efe94-150">Par exemple, `http://localhost:31544` peut être l’URL d’une application web en cours d’exécution sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="efe94-150">For example, `http://localhost:31544` might be the URL for a web app running on your local machine.</span></span> <span data-ttu-id="efe94-151">Les utilisateurs peuvent utiliser cette URL pour se connecter à une application web cliente.</span><span class="sxs-lookup"><span data-stu-id="efe94-151">Users would use this URL to sign in to a web client application.</span></span>
       - <span data-ttu-id="efe94-152">Pour les applications de client public, indiquez l’URI utilisé par Azure AD pour renvoyer les réponses de jeton.</span><span class="sxs-lookup"><span data-stu-id="efe94-152">For public client applications, provide the URI used by Azure AD to return token responses.</span></span> <span data-ttu-id="efe94-153">Entrez une valeur spécifique de votre application, par exemple, `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="efe94-153">Enter a value specific to your application, such as `myapp://auth`.</span></span>

     <span data-ttu-id="efe94-154">Pour accéder à des exemples spécifiques aux applications web ou natives, consultez les [Guides de démarrage rapides](/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="efe94-154">To see specific examples for web applications or native applications, check out our [quickstarts](/azure/active-directory/develop/#quickstarts).</span></span>

     <span data-ttu-id="efe94-155">Lorsque vous avez terminé, sélectionnez **Inscrire**.</span><span class="sxs-lookup"><span data-stu-id="efe94-155">When finished, select **Register**.</span></span>

4. <span data-ttu-id="efe94-156">Autorisez votre application à accéder à Microsoft Defender pour le point de terminaison et attribuez-lui l’autorisation « Lire les alertes » :</span><span class="sxs-lookup"><span data-stu-id="efe94-156">Allow your Application to access Microsoft Defender for Endpoint and assign it 'Read alerts' permission:</span></span>

    - <span data-ttu-id="efe94-157">Dans la page de votre application, sélectionnez **Autorisations API** Ajouter des API d’autorisation que mon  >    >   organisation > **tapez WindowsDefenderATP** et sélectionnez **sur WindowsDefenderATP**.</span><span class="sxs-lookup"><span data-stu-id="efe94-157">On your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** > type **WindowsDefenderATP** and select on **WindowsDefenderATP**.</span></span>

    - <span data-ttu-id="efe94-158">**Remarque**: *WindowsDefenderATP* n’apparaît pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="efe94-158">**Note**: *WindowsDefenderATP* does not appear in the original list.</span></span> <span data-ttu-id="efe94-159">Commencez à écrire son nom dans la zone de texte pour l’voir apparaître.</span><span class="sxs-lookup"><span data-stu-id="efe94-159">Start writing its name in the text box to see it appear.</span></span>

      ![ajouter une autorisation](images/add-permission.png)

    - <span data-ttu-id="efe94-161">Choose **Delegated permissions**  >  **Alert.Read** > select **Add permissions**</span><span class="sxs-lookup"><span data-stu-id="efe94-161">Choose **Delegated permissions** > **Alert.Read** > select **Add permissions**</span></span>

      ![autorisations d’application](images/application-permissions-public-client.png)

    - <span data-ttu-id="efe94-163">**Remarque importante**: sélectionnez les autorisations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="efe94-163">**Important note**: Select the relevant permissions.</span></span> <span data-ttu-id="efe94-164">Les alertes de lecture ne sont qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="efe94-164">Read alerts is only an example.</span></span>

      <span data-ttu-id="efe94-165">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="efe94-165">For instance,</span></span>

      - <span data-ttu-id="efe94-166">Pour [exécuter des requêtes avancées,](run-advanced-query-api.md)sélectionnez l’autorisation « Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="efe94-166">To [run advanced queries](run-advanced-query-api.md), select 'Run advanced queries' permission</span></span>
      - <span data-ttu-id="efe94-167">Pour [isoler un appareil, sélectionnez](isolate-machine.md)l’autorisation « Isoler l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="efe94-167">To [isolate a device](isolate-machine.md), select 'Isolate machine' permission</span></span>
      - <span data-ttu-id="efe94-168">Pour déterminer l’autorisation qui vous est nécessaire, consultez la section **Autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="efe94-168">To determine which permission you need, view the **Permissions** section in the API you are interested to call.</span></span>

    - <span data-ttu-id="efe94-169">Sélectionner **Accorder le consentement**</span><span class="sxs-lookup"><span data-stu-id="efe94-169">Select **Grant consent**</span></span>

      <span data-ttu-id="efe94-170">**Remarque**: chaque fois que vous ajoutez une autorisation, vous devez sélectionner accordez **l’autorisation** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="efe94-170">**Note**: Every time you add permission you must select on **Grant consent** for the new permission to take effect.</span></span>

      ![Image de l’octroi d’autorisations](images/grant-consent.png)

6. <span data-ttu-id="efe94-172">Notez votre ID d’application et votre ID de client :</span><span class="sxs-lookup"><span data-stu-id="efe94-172">Write down your application ID and your tenant ID:</span></span>

   - <span data-ttu-id="efe94-173">Dans la page de votre application, allez à **Vue d’ensemble** et copiez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="efe94-173">On your application page, go to **Overview** and copy the following information:</span></span>

   ![Image de l’ID d’application créé](images/app-and-tenant-ids.png)


## <a name="get-an-access-token"></a><span data-ttu-id="efe94-175">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="efe94-175">Get an access token</span></span>

<span data-ttu-id="efe94-176">Pour plus d’informations sur les jetons AAD, voir [le didacticiel Azure AD](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span><span class="sxs-lookup"><span data-stu-id="efe94-176">For more information on AAD tokens, see [Azure AD tutorial](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)</span></span>

### <a name="using-c"></a><span data-ttu-id="efe94-177">Utilisation de C #</span><span class="sxs-lookup"><span data-stu-id="efe94-177">Using C#</span></span>

- <span data-ttu-id="efe94-178">Copiez/collez la classe ci-dessous dans votre application.</span><span class="sxs-lookup"><span data-stu-id="efe94-178">Copy/Paste the below class in your application.</span></span>
- <span data-ttu-id="efe94-179">Utilisez **la méthode AcquireUserTokenAsync** avec votre ID d’application, ID de client, nom d’utilisateur et mot de passe pour acquérir un jeton.</span><span class="sxs-lookup"><span data-stu-id="efe94-179">Use **AcquireUserTokenAsync** method with your application ID, tenant ID, user name, and password to acquire a token.</span></span>

    ```csharp
    namespace WindowsDefenderATP
    {
        using System.Net.Http;
        using System.Text;
        using System.Threading.Tasks;
        using Newtonsoft.Json.Linq;

        public static class WindowsDefenderATPUtils
        {
            private const string Authority = "https://login.microsoftonline.com";

            private const string WdatpResourceId = "https://api.securitycenter.microsoft.com";

            public static async Task<string> AcquireUserTokenAsync(string username, string password, string appId, string tenantId)
            {
                using (var httpClient = new HttpClient())
                {
                    var urlEncodedBody = $"resource={WdatpResourceId}&client_id={appId}&grant_type=password&username={username}&password={password}";

                    var stringContent = new StringContent(urlEncodedBody, Encoding.UTF8, "application/x-www-form-urlencoded");

                    using (var response = await httpClient.PostAsync($"{Authority}/{tenantId}/oauth2/token", stringContent).ConfigureAwait(false))
                    {
                        response.EnsureSuccessStatusCode();

                        var json = await response.Content.ReadAsStringAsync().ConfigureAwait(false);

                        var jObject = JObject.Parse(json);

                        return jObject["access_token"].Value<string>();
                    }
                }
            }
        }
    }
    ```

## <a name="validate-the-token"></a><span data-ttu-id="efe94-180">Valider le jeton</span><span class="sxs-lookup"><span data-stu-id="efe94-180">Validate the token</span></span>

<span data-ttu-id="efe94-181">Vérifiez que vous avez reçu un jeton correct :</span><span class="sxs-lookup"><span data-stu-id="efe94-181">Verify to make sure you got a correct token:</span></span>
- <span data-ttu-id="efe94-182">Copier/coller dans [JWT](https://jwt.ms) le jeton obtenu à l’étape précédente afin de le décoder</span><span class="sxs-lookup"><span data-stu-id="efe94-182">Copy/paste into [JWT](https://jwt.ms) the token you got in the previous step in order to decode it</span></span>
- <span data-ttu-id="efe94-183">Valider que vous obtenez une revendication « scp » avec les autorisations d’application souhaitées</span><span class="sxs-lookup"><span data-stu-id="efe94-183">Validate you get a 'scp' claim with the desired app permissions</span></span>
- <span data-ttu-id="efe94-184">Dans la capture d’écran ci-dessous, vous pouvez voir un jeton décodé acquis à partir de l’application dans le didacticiel :</span><span class="sxs-lookup"><span data-stu-id="efe94-184">In the screenshot below you can see a decoded token acquired from the app in the tutorial:</span></span>

![Image de validation de jeton](images/nativeapp-decoded-token.png)

## <a name="use-the-token-to-access-microsoft-defender-for-endpoint-api"></a><span data-ttu-id="efe94-186">Utiliser le jeton pour accéder à l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="efe94-186">Use the token to access Microsoft Defender for Endpoint API</span></span>

- <span data-ttu-id="efe94-187">Choisissez l’API que vous souhaitez utiliser : API [Microsoft Defender pour point de terminaison prise en charge](exposed-apis-list.md)</span><span class="sxs-lookup"><span data-stu-id="efe94-187">Choose the API you want to use - [Supported Microsoft Defender for Endpoint APIs](exposed-apis-list.md)</span></span>
- <span data-ttu-id="efe94-188">Définissez l’en-tête Authorization dans la requête HTTP que vous envoyez à « Bearer {token} » (le porteur est le schéma d’autorisation)</span><span class="sxs-lookup"><span data-stu-id="efe94-188">Set the Authorization header in the HTTP request you send to "Bearer {token}" (Bearer is the Authorization scheme)</span></span>
- <span data-ttu-id="efe94-189">Le délai d’expiration du jeton est de 1 heure (vous pouvez envoyer plusieurs demandes avec le même jeton)</span><span class="sxs-lookup"><span data-stu-id="efe94-189">The Expiration time of the token is 1 hour (you can send more than one request with the same token)</span></span>

- <span data-ttu-id="efe94-190">Exemple d’envoi d’une demande pour obtenir une liste d’alertes à **l’aide C#**</span><span class="sxs-lookup"><span data-stu-id="efe94-190">Example of sending a request to get a list of alerts **using C#**</span></span> 

    ```csharp
    var httpClient = new HttpClient();

    var request = new HttpRequestMessage(HttpMethod.Get, "https://api.securitycenter.microsoft.com/api/alerts");

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", token);

    var response = httpClient.SendAsync(request).GetAwaiter().GetResult();

    // Do something useful with the response
    ```

## <a name="see-also"></a><span data-ttu-id="efe94-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efe94-191">See also</span></span>
- [<span data-ttu-id="efe94-192">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="efe94-192">Microsoft Defender for Endpoint APIs</span></span>](exposed-apis-list.md)
- [<span data-ttu-id="efe94-193">Accéder à Microsoft Defender pour le point de terminaison avec le contexte de l’application</span><span class="sxs-lookup"><span data-stu-id="efe94-193">Access Microsoft Defender for Endpoint with application context</span></span>](exposed-apis-create-app-webapp.md)
