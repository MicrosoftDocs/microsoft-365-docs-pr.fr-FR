---
title: Déployer un connecteur pour archiver les données des pages Facebook Business
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des pages Facebook Business Microsoft 365. Une fois ces données importées dans Microsoft 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Facebook de votre organisation.
ms.openlocfilehash: b771c50eb5c2eb5f99269f1f399d27043ebee6bb
ms.sourcegitcommit: 6fc6aaa2b7610e148f41018abd229e3c55b2f3d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49619950"
---
# <a name="deploy-a-connector-to-archive-facebook-business-pages-data"></a><span data-ttu-id="3d83d-104">Déployer un connecteur pour archiver les données des pages Facebook Business</span><span class="sxs-lookup"><span data-stu-id="3d83d-104">Deploy a connector to archive Facebook Business pages data</span></span>

<span data-ttu-id="3d83d-105">Cet article contient le processus pas à pas pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir de pages Facebook Business vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d83d-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from Facebook Business pages to Microsoft 365.</span></span> <span data-ttu-id="3d83d-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Facebook, voir Configurer un connecteur pour archiver les [données Facebook.](archive-facebook-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="3d83d-106">For a high-level overview of this process and a list of prerequisites required to deploy a Facebook connector, see [Set up a connector to archive Facebook data](archive-facebook-data-with-sample-connector.md).</span></span>

## <a name="step-1-create-an-app-in-azure-active-directory"></a><span data-ttu-id="3d83d-107">Étape 1 : Créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3d83d-107">Step 1: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="3d83d-108">Go to <https://portal.azure.com> and sign in using the credentials of a global admin account.</span><span class="sxs-lookup"><span data-stu-id="3d83d-108">Go to <https://portal.azure.com> and sign in using the credentials of a global admin account.</span></span>

    ![Créer une application dans AAD](../media/FBCimage1.png)

2. <span data-ttu-id="3d83d-110">Dans le volet de navigation gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-110">In the left navigation pane, click **Azure Active Directory**.</span></span>

    ![Cliquez sur Azure Active Directory](../media/FBCimage2.png)

3. <span data-ttu-id="3d83d-112">Dans le volet de navigation de gauche, cliquez sur **Inscriptions d’applications (prévisualisation),** puis sur **Nouvelle inscription.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-112">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

    ![Cliquez sur **Inscriptions d’applications (prévisualisation)**, puis sur **Nouvelle inscription**](../media/FBCimage3.png)

4. <span data-ttu-id="3d83d-114">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="3d83d-114">Register the application.</span></span> <span data-ttu-id="3d83d-115">Sous URI de redirection, sélectionnez Web dans la liste de listes de listes listes des types d’application, puis tapez dans la zone de <https://portal.azure.com> l’URI.</span><span class="sxs-lookup"><span data-stu-id="3d83d-115">Under Redirect URI, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![Inscription de l’application](../media/FBCimage4.png)

5. <span data-ttu-id="3d83d-117">Copiez **l’ID d’application (client)** et l’ID d’annuaire **(client)** et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="3d83d-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="3d83d-118">Vous utiliserez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d83d-118">You use these IDs in later steps.</span></span>

   ![Copiez l’ID d’application et l’ID d’annuaire et enregistrez-les](../media/FBCimage5.png)

6. <span data-ttu-id="3d83d-120">Go to **Certificates & secrets for the new app.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-120">Go to **Certificates & secrets for the new app.**</span></span>

   ![Go to Certificates & secrets for the new app](../media/FBCimage6.png)

7. <span data-ttu-id="3d83d-122">Cliquez **sur Nouvelle secret client**</span><span class="sxs-lookup"><span data-stu-id="3d83d-122">Click **New client secret**</span></span>

   ![Cliquez sur Nouvelle secret client](../media/FBCimage7.png)

8. <span data-ttu-id="3d83d-124">Créez une nouvelle secret.</span><span class="sxs-lookup"><span data-stu-id="3d83d-124">Create a new secret.</span></span> <span data-ttu-id="3d83d-125">Dans la zone de description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="3d83d-125">In the description box, type the secret and then choose an expiration period.</span></span>

    ![Tapez la secret, puis choisissez une période d’expiration](../media/FBCimage8.png)

9. <span data-ttu-id="3d83d-127">Copiez la valeur de la secret et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="3d83d-127">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="3d83d-128">Il s’agit de la question secrète de l’application AAD que vous utiliserez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d83d-128">This is the AAD application secret that you use in later steps.</span></span>

   ![Copier la valeur de la secret et l’enregistrer](../media/FBCimage9.png)

## <a name="step-2-deploy-the-connector-web-service-from-github-to-your-azure-account"></a><span data-ttu-id="3d83d-130">Étape 2 : Déployer le service web connecteur à partir de GitHub votre compte Azure</span><span class="sxs-lookup"><span data-stu-id="3d83d-130">Step 2: Deploy the connector web service from GitHub to your Azure account</span></span>

1. <span data-ttu-id="3d83d-131">Go to [this GitHub site](https://github.com/microsoft/m365-sample-connector-csharp-aspnet) and click Deploy to **Azure**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-131">Go to [this GitHub site](https://github.com/microsoft/m365-sample-connector-csharp-aspnet) and click **Deploy to Azure**.</span></span>

    ![Cliquez sur Déployer sur Azure](../media/FBCGithubApp.png)

2. <span data-ttu-id="3d83d-133">Une fois que vous avez **cliqué sur Déployer** vers Azure, vous êtes redirigé vers un portail Azure avec une page de modèle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3d83d-133">After you click **Deploy to Azure**, you will be redirected to an Azure portal with a custom template page.</span></span> <span data-ttu-id="3d83d-134">Remplissez les **informations de base** et **Paramètres,** puis cliquez sur **Acheter.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-134">Fill in the **Basics** and **Settings** details and then click **Purchase**.</span></span>

   - <span data-ttu-id="3d83d-135">**Abonnement :** Sélectionnez votre abonnement Azure sur qui vous souhaitez déployer le service web connecteur de pages Facebook Business.</span><span class="sxs-lookup"><span data-stu-id="3d83d-135">**Subscription:** Select your Azure subscription that you want to deploy the Facebook Business pages connector web service to.</span></span>

   - <span data-ttu-id="3d83d-136">**Groupe de ressources :** Choisissez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="3d83d-136">**Resource group:** Choose or create a new resource group.</span></span> <span data-ttu-id="3d83d-137">Un groupe de ressources est un conteneur qui contient des ressources associées pour une solution Azure.</span><span class="sxs-lookup"><span data-stu-id="3d83d-137">A resource group is a container that holds related resources for an Azure solution.</span></span>

   - <span data-ttu-id="3d83d-138">**Emplacement :** Choisissez un emplacement.</span><span class="sxs-lookup"><span data-stu-id="3d83d-138">**Location:** Choose a location.</span></span>

   - <span data-ttu-id="3d83d-139">**Nom de l’application web :** Fournissez un nom unique pour l’application web du connecteur.</span><span class="sxs-lookup"><span data-stu-id="3d83d-139">**Web App Name:** Provide a unique name for the connector web app.</span></span> <span data-ttu-id="3d83d-140">La longueur du nom doit être de 3 à 18 caractères.</span><span class="sxs-lookup"><span data-stu-id="3d83d-140">Th name must be between 3 and 18 characters in length.</span></span> <span data-ttu-id="3d83d-141">Ce nom est utilisé pour créer l’URL du service d’application Azure ; par exemple, si vous fournissez le nom de l’application Web **fbconnector,** l’URL du service d’application Azure **sera fbconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-141">This name is used to create the Azure app service URL; for example, if you provide the Web app name of **fbconnector** then the Azure app service URL  will be **fbconnector.azurewebsites.net**.</span></span>

   - <span data-ttu-id="3d83d-142">**tenantId :** ID client de votre organisation Microsoft 365 que vous avez copiée après la création de l’application connecteur Facebook à l Azure Active Directory l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="3d83d-142">**tenantId:** The tenant ID of your Microsoft 365 organization that you copied after creating the Facebook connector app in Azure Active Directory in Step 1.</span></span>

   - <span data-ttu-id="3d83d-143">**APISecretKey :** Vous pouvez taper n’importe quelle valeur comme secret.</span><span class="sxs-lookup"><span data-stu-id="3d83d-143">**APISecretKey:** You can type any value as the secret.</span></span> <span data-ttu-id="3d83d-144">Il permet d’accéder à l’application web de connecteur à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="3d83d-144">This is used to access the connector web app in Step 5.</span></span>

     ![Cliquez sur Créer un compte de stockage de ressources et de types](../media/FBCimage12.png)

3. <span data-ttu-id="3d83d-146">Une fois le déploiement réussi, la page ressemble à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="3d83d-146">After the deployment is successful, the page will look similar to the following screenshot:</span></span>

   ![Cliquez Stockage puis cliquez sur Stockage compte](../media/FBCimage13.png)

## <a name="step-3-register-the-facebook-app"></a><span data-ttu-id="3d83d-148">Étape 3 : Inscrire l’application Facebook</span><span class="sxs-lookup"><span data-stu-id="3d83d-148">Step 3: Register the Facebook app</span></span>

1. <span data-ttu-id="3d83d-149">Go to <https://developers.facebook.com> , log in using the credentials for the account for your organization’s Facebook Business pages, and then click Add New **App**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-149">Go to <https://developers.facebook.com>, log in using the credentials for the account for your organization's Facebook Business pages, and then click **Add New App**.</span></span>

   ![Ajouter une nouvelle page d’application pour les entreprises Facebook](../media/FBCimage25.png)

2. <span data-ttu-id="3d83d-151">Créez un ID d’application.</span><span class="sxs-lookup"><span data-stu-id="3d83d-151">Create a new app ID.</span></span>

   ![Créer un ID d’application](../media/FBCimage26.png)

3. <span data-ttu-id="3d83d-153">Dans le volet de navigation de gauche, **cliquez** sur Ajouter des produits, puis cliquez sur **Configurer** dans la vignette de **connexion Facebook.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-153">In the left navigation pane, click **Add Products** and then click **Set Up** in the **Facebook Login** tile.</span></span>

   ![Cliquez sur Ajouter des produits](../media/FBCimage27.png)

4. <span data-ttu-id="3d83d-155">Dans la page Intégrer la connexion Facebook, cliquez sur **Web.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-155">On the Integrate Facebook Login page, click **Web**.</span></span>

   ![Cliquez sur Le Web sur la page d’intégration de la connexion Facebook](../media/FBCimage28.png)

5. <span data-ttu-id="3d83d-157">Ajouter l’URL du service d’application Azure ; par `https://fbconnector.azurewebsites.net` exemple.</span><span class="sxs-lookup"><span data-stu-id="3d83d-157">Add the Azure app service URL; for example `https://fbconnector.azurewebsites.net`.</span></span>

   ![Ajouter l’URL du service d’application Azure](../media/FBCimage29.png)

6. <span data-ttu-id="3d83d-159">Complétez la section Démarrage rapide de la configuration de la connexion à Facebook.</span><span class="sxs-lookup"><span data-stu-id="3d83d-159">Complete the QuickStart section of the Facebook Login setup.</span></span>

   ![Terminer la section Démarrage rapide](../media/FBCimage30.png)

7. <span data-ttu-id="3d83d-161">Dans le volet de navigation de gauche sous **Connexion Facebook,** cliquez sur **Paramètres** et ajoutez l’URI de redirection OAuth dans la zone URI de redirection **OAuth** valide.</span><span class="sxs-lookup"><span data-stu-id="3d83d-161">In the left navigation pane under **Facebook Login**, click **Settings**, and add the OAuth redirect URI in the **Valid OAuth Redirect URIs** box.</span></span> <span data-ttu-id="3d83d-162">Utilisez le format **\<connectorserviceuri> /Views/FacebookOAuth**, où la valeur de connectorserviceuri est l’URL du service d’application Azure pour votre organisation ; par exemple, `https://fbconnector.azurewebsites.net` .</span><span class="sxs-lookup"><span data-stu-id="3d83d-162">Use the format **\<connectorserviceuri>/Views/FacebookOAuth**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example, `https://fbconnector.azurewebsites.net`.</span></span>

   ![Ajouter l’URI de redirection OAuth à la zone URI de redirection OAuth valide](../media/FBCimage31.png)

8. <span data-ttu-id="3d83d-164">Dans le volet de navigation de gauche, cliquez sur **Ajouter des** produits, puis sur **Webhooks.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-164">In the left navigation pane, click **Add Products** and then click **Webhooks.**</span></span> <span data-ttu-id="3d83d-165">Dans le menu déroulant **Page,** cliquez sur **Page.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-165">In the **Page** pull-down menu, click **Page**.</span></span>

   ![Cliquez sur Ajouter des produits, puis sur \*\*Webhooks](../media/FBCimage32.png)

9. <span data-ttu-id="3d83d-167">Ajoutez l’URL de rappel webhooks et ajoutez un jeton de vérification.</span><span class="sxs-lookup"><span data-stu-id="3d83d-167">Add Webhooks Callback URL and add a verify token.</span></span> <span data-ttu-id="3d83d-168">Le format de l’URL de rappel, utilisez le format **<connectorserviceuri> /api/FbPageWebhook**, où la valeur de connectorserviceuri est l’URL du service d’application Azure pour votre organisation ; par exemple `https://fbconnector.azurewebsites.net` .</span><span class="sxs-lookup"><span data-stu-id="3d83d-168">The format of the callback URL, use the format **<connectorserviceuri>/api/FbPageWebhook**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example `https://fbconnector.azurewebsites.net`.</span></span>

   <span data-ttu-id="3d83d-169">Le jeton de vérification doit être similaire à un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="3d83d-169">The verify token should similar to a strong password.</span></span> <span data-ttu-id="3d83d-170">Copiez le jeton de vérification dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="3d83d-170">Copy the verify token to a text file or other storage location.</span></span>

   ![Ajouter le jeton de vérification](../media/FBCimage33.png)

10. <span data-ttu-id="3d83d-172">Testez et abonnez-vous au point de terminaison pour le flux.</span><span class="sxs-lookup"><span data-stu-id="3d83d-172">Test and subscribe to the endpoint for feed.</span></span>

    ![Tester et s’abonner au point de terminaison](../media/FBCimage34.png)

11. <span data-ttu-id="3d83d-174">Ajoutez une URL de confidentialité, une icône d’application et une utilisation professionnelle.</span><span class="sxs-lookup"><span data-stu-id="3d83d-174">Add a privacy URL, app icon, and business use.</span></span> <span data-ttu-id="3d83d-175">Copiez également l’ID d’application et la secret de l’application dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="3d83d-175">Also, copy the app ID and app secret to a text file or other storage location.</span></span>

    ![Ajouter une URL de confidentialité, une icône d’application et une utilisation professionnelle](../media/FBCimage35.png)

12. <span data-ttu-id="3d83d-177">Rendez l’application publique.</span><span class="sxs-lookup"><span data-stu-id="3d83d-177">Make the app public.</span></span>

    ![Rendre l’application publique](../media/FBCimage36.png)

13. <span data-ttu-id="3d83d-179">Ajoutez un utilisateur au rôle d’administrateur ou de testeur.</span><span class="sxs-lookup"><span data-stu-id="3d83d-179">Add user to the admin or tester role.</span></span>

    ![Ajouter un utilisateur au rôle d’administrateur ou de testeur](../media/FBCimage37.png)

14. <span data-ttu-id="3d83d-181">Ajoutez **l’autorisation d’accès au contenu public de** la page.</span><span class="sxs-lookup"><span data-stu-id="3d83d-181">Add the **Page Public Content Access** permission.</span></span>

    ![dd l’autorisation d’accès au contenu public de page](../media/FBCimage38.png)

15. <span data-ttu-id="3d83d-183">Ajouter l’autorisation Gérer les pages.</span><span class="sxs-lookup"><span data-stu-id="3d83d-183">Add Manage Pages permission.</span></span>

    ![Ajouter l’autorisation Gérer les pages](../media/FBCimage39.png)

16. <span data-ttu-id="3d83d-185">Faites passer l’application en revue par Facebook.</span><span class="sxs-lookup"><span data-stu-id="3d83d-185">Get the application reviewed by Facebook.</span></span>

    ![Faire passer l’application en revue par Facebook](../media/FBCimage40.png)

## <a name="step-4-configure-the-connector-web-app"></a><span data-ttu-id="3d83d-187">Étape 4 : Configurer l’application web de connecteur</span><span class="sxs-lookup"><span data-stu-id="3d83d-187">Step 4: Configure the connector web app</span></span>

1. <span data-ttu-id="3d83d-188">Go to `https://<AzureAppResourceName>.azurewebsites.net` (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4).</span><span class="sxs-lookup"><span data-stu-id="3d83d-188">Go to `https://<AzureAppResourceName>.azurewebsites.net` (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4).</span></span> <span data-ttu-id="3d83d-189">Par exemple, si le nom est **fbconnector**, allez à `https://fbconnector.azurewebsites.net` .</span><span class="sxs-lookup"><span data-stu-id="3d83d-189">For example, if the name is **fbconnector**, go to `https://fbconnector.azurewebsites.net`.</span></span> <span data-ttu-id="3d83d-190">La page d’accueil de l’application ressemblera à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="3d83d-190">The home page of the app will look like the following screenshot:</span></span>

   ![Go to you connector web app](../media/FBCimage41.png)

2. <span data-ttu-id="3d83d-192">Cliquez **sur Configurer pour** afficher une page de signature.</span><span class="sxs-lookup"><span data-stu-id="3d83d-192">Click **Configure** to display a sign in page.</span></span>

   ![Cliquez sur Configurer pour afficher une page de signature](../media/FBCimage42.png)

3. <span data-ttu-id="3d83d-194">Dans la zone ID de locataire, tapez ou collez votre ID de client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="3d83d-194">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="3d83d-195">Dans la zone de mot de passe, tapez ou collez la clé APISecretKey (obtenue à l’étape 2), puis cliquez sur Définir la configuration **Paramètres** pour afficher la page de détails de configuration.</span><span class="sxs-lookup"><span data-stu-id="3d83d-195">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the configuration details page.</span></span>

    ![Connectez-vous à l’aide de votre ID de client et de votre mot de passe, puis allez à la page des détails de configuration](../media/FBCimage43.png)

4. <span data-ttu-id="3d83d-197">Entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="3d83d-197">Enter the following configuration settings</span></span>

   - <span data-ttu-id="3d83d-198">**ID d’application Facebook :** ID d’application pour l’application Facebook obtenue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3d83d-198">**Facebook application ID:** The app ID for the Facebook application that you obtained in Step 3.</span></span>

   - <span data-ttu-id="3d83d-199">**Secret d’application Facebook :** Secret d’application pour l’application Facebook que vous avez obtenu à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3d83d-199">**Facebook application secret:** The app secret for the Facebook application that you obtained in Step 3.</span></span>

   - <span data-ttu-id="3d83d-200">**Les webhooks Facebook vérifient le jeton :** Jeton de vérification que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3d83d-200">**Facebook webhooks verify token:** The verify token that you created in Step 3.</span></span>

   - <span data-ttu-id="3d83d-201">**ID d’application AAD :** ID de l’application Azure Active Directory que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="3d83d-201">**AAD application ID:** The application ID for the Azure Active Directory app that you created in Step 1.</span></span>

   - <span data-ttu-id="3d83d-202">**Secret d’application AAD :** Valeur de la clé secrète APISecretKey que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="3d83d-202">**AAD application secret:** The value for the APISecretKey secret that you created in Step 1.</span></span>

5. <span data-ttu-id="3d83d-203">Cliquez **sur Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="3d83d-203">Click **Save** to save the connector settings.</span></span>

## <a name="step-5-set-up-a-facebook-connector-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="3d83d-204">Étape 5 : Configurer un connecteur Facebook dans le centre Microsoft 365 conformité</span><span class="sxs-lookup"><span data-stu-id="3d83d-204">Step 5: Set up a Facebook connector in the Microsoft 365 compliance center</span></span>

1. <span data-ttu-id="3d83d-205">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click Data **connectors** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="3d83d-205">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="3d83d-206">Dans la page **Connecteurs de données** sous **les pages Facebook Entreprise,** cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-206">On the **Data connectors** page under **Facebook Business pages**, click **View**.</span></span>

3. <span data-ttu-id="3d83d-207">Dans la **page Des pages d’entreprise Facebook,** cliquez **sur Ajouter un connecteur.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-207">On the **Facebook business pages** page, click **Add connector**.</span></span>

4. <span data-ttu-id="3d83d-208">Dans la page **Conditions d’utilisation,** cliquez sur **Accepter.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-208">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="3d83d-209">Dans la page **Ajouter des informations d’identification pour votre** application de connecteur, entrez les informations suivantes, puis cliquez sur Valider la **connexion.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-209">On the **Add credentials for your connector app** page, enter the following information and then click **Validate connection**.</span></span>

   ![Entrer les informations d’identification de l’application connecteur](../media/TCimage38.png)

   - <span data-ttu-id="3d83d-211">Dans la **zone** Nom, tapez un nom pour le connecteur, tel que la **page d’actualités facebook.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-211">In the **Name** box, type a name for the connector, such as **Facebook news page**.</span></span>

   - <span data-ttu-id="3d83d-212">Dans la **zone URL de** connexion, tapez ou collez l’URL du service d’application Azure ; par `https://fbconnector.azurewebsites.net` exemple.</span><span class="sxs-lookup"><span data-stu-id="3d83d-212">In the **Connection URL** box, type or paste the Azure app service URL; for example `https://fbconnector.azurewebsites.net`.</span></span>

   - <span data-ttu-id="3d83d-213">Dans la **zone Mot** de passe, tapez ou collez la valeur de l’APISecretKey que vous avez ajoutée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="3d83d-213">In the **Password** box, type or paste the value of the APISecretKey that you added in Step 2.</span></span>

   - <span data-ttu-id="3d83d-214">Dans la **zone ID** d’application Azure, tapez ou collez la valeur de l’ID d’application (client) également appelé ID d’application AAD que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="3d83d-214">In the **Azure App ID** box, type or paste the value of the Application (client) ID also called as AAD Application ID that you created in Step 1.</span></span>

6. <span data-ttu-id="3d83d-215">Une fois la connexion validée, cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-215">After the connection is successfully validated, click **Next**.</span></span>

7. <span data-ttu-id="3d83d-216">Dans la page **Autoriser Microsoft 365** importer des données, tapez ou collez de nouveau l’APISecretKey, puis cliquez sur Login **web app**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-216">On the **Authorize Microsoft 365 to import data** page, type or paste the APISecretKey again and then click **Login web app**.</span></span>

8. <span data-ttu-id="3d83d-217">Dans la page **Configurer l’application connecteur Facebook,** cliquez sur Se connecter avec **Facebook** et connectez-vous à l’aide des informations d’identification du compte pour les pages Facebook Business de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3d83d-217">On the **Configure Facebook connector app** page, click **Login with Facebook** and log in using the credentials for the account for your organization's Facebook Business pages.</span></span> <span data-ttu-id="3d83d-218">Assurez-vous que le compte Facebook à qui vous vous êtes connecté se voit attribuer le rôle d’administrateur pour les pages Facebook Business de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3d83d-218">Make sure the Facebook account that you logged in to is assigned the admin role for your organization's Facebook Business pages.</span></span>

   ![Connectez-vous avec Facebook](../media/FBCimage50.png)

9. <span data-ttu-id="3d83d-220">Une liste des pages d’entreprise gérées par le compte Facebook à qui vous vous êtes connecté s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3d83d-220">A list of the business pages managed by the Facebook account that you logged in to is displayed.</span></span> <span data-ttu-id="3d83d-221">Sélectionnez la page à archiver, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="3d83d-221">Select the page to archive and then click **Next**.</span></span>

   ![Sélectionnez la page d’entreprise de l’organisation que vous souhaitez archiver](../media/FBCimage52.png)

10. <span data-ttu-id="3d83d-223">Cliquez **sur Continuer** pour quitter la configuration de l’application de service connecteur.</span><span class="sxs-lookup"><span data-stu-id="3d83d-223">Click **Continue** to exit the setup of the connector service app.</span></span>

11. <span data-ttu-id="3d83d-224">Dans la page **Définir les filtres,** vous pouvez appliquer un filtre pour importer initialement des éléments d’un certain âge.</span><span class="sxs-lookup"><span data-stu-id="3d83d-224">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="3d83d-225">Sélectionnez un âge, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-225">Select an age, and then click **Next**.</span></span>

12. <span data-ttu-id="3d83d-226">Dans la page **Choisir** l’emplacement de stockage, tapez l’adresse de messagerie Microsoft 365 boîte aux lettres dans Microsoft 365 vers qui les éléments Facebook seront importés, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3d83d-226">On the **Choose storage location** page, type the email address of Microsoft 365 mailbox that the Facebook items will be imported to, and then click **Next**.</span></span>

13. <span data-ttu-id="3d83d-227">Cliquez **sur Suivant** pour passer en revue les paramètres du connecteur, puis cliquez sur **Terminer** pour terminer la configuration du connecteur.</span><span class="sxs-lookup"><span data-stu-id="3d83d-227">Click **Next** to review the connector settings and then click **Finish** to complete the connector setup.</span></span>

14. <span data-ttu-id="3d83d-228">Dans le centre de conformité, allez à la page **Connecteurs** de données, puis cliquez sur l’onglet **Connecteurs** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="3d83d-228">In the compliance center, go to the **Data connectors** page, and click the **Connectors** tab to see the progress of the import process.</span></span>
