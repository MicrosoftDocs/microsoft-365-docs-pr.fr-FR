---
title: Déploiement d’un connecteur pour l’archivage des données de pages d’entreprise Facebook
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
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des pages Facebook dans Microsoft 365. Une fois ces données importées dans Microsoft 365, vous pouvez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Facebook de votre organisation.
ms.openlocfilehash: 48747dade98701303c4ca6a8c00192ec7faff34a
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2020
ms.locfileid: "42635022"
---
# <a name="deploy-a-connector-to-archive-facebook-business-pages-data"></a><span data-ttu-id="d79cb-104">Déploiement d’un connecteur pour l’archivage des données de pages d’entreprise Facebook</span><span class="sxs-lookup"><span data-stu-id="d79cb-104">Deploy a connector to archive Facebook Business pages data</span></span>

<span data-ttu-id="d79cb-105">Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Microsoft 365 pour importer des données à partir de pages d’entreprise Facebook vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d79cb-105">This article contains the step-by-step process to deploy a connector that uses the Microsoft 365 Import service to import data from Facebook Business pages to Microsoft 365.</span></span> <span data-ttu-id="d79cb-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Facebook, reportez-vous à la rubrique [configurer un connecteur pour archiver les données Facebook](archive-facebook-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="d79cb-106">For a high-level overview of this process and a list of prerequisites required to deploy a Facebook connector, see [Set up a connector to archive Facebook data](archive-facebook-data-with-sample-connector.md).</span></span> 

## <a name="step-1-create-an-app-in-azure-active-directory"></a><span data-ttu-id="d79cb-107">Étape 1 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d79cb-107">Step 1: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="d79cb-108">Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.</span><span class="sxs-lookup"><span data-stu-id="d79cb-108">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

    ![Créer une application dans AAD](../media/FBCimage1.png)

2. <span data-ttu-id="d79cb-110">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-110">In the left navigation pane, click **Azure Active Directory**.</span></span>

    ![Cliquez sur Azure Active Directory](../media/FBCimage2.png)

3. <span data-ttu-id="d79cb-112">Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-112">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

    ![Cliquez sur \* \* inscriptions des applications (aperçu) \* \*, puis cliquez sur \* \* nouvelle inscription \* \*](../media/FBCimage3.png)

4. <span data-ttu-id="d79cb-114">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="d79cb-114">Register the application.</span></span> <span data-ttu-id="d79cb-115">Sous URI de redirection, sélectionnez Web dans la liste déroulante type d' <https://portal.azure.com> application, puis tapez dans la zone de l’URI.</span><span class="sxs-lookup"><span data-stu-id="d79cb-115">Under Redirect URI, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![Inscription de l’application](../media/FBCimage4.png)

5. <span data-ttu-id="d79cb-117">Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="d79cb-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="d79cb-118">Vous utilisez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d79cb-118">You use these IDs in later steps.</span></span>

   ![Copiez l’ID de l’application et l’ID du répertoire et enregistrez-les.](../media/FBCimage5.png)

6. <span data-ttu-id="d79cb-120">Accédez à **certificats & secrets de la nouvelle application.**</span><span class="sxs-lookup"><span data-stu-id="d79cb-120">Go to **Certificates & secrets for the new app.**</span></span>

   ![Accéder aux certificats & secrets de la nouvelle application](../media/FBCimage6.png)

7. <span data-ttu-id="d79cb-122">Cliquez sur **nouvelle clé secrète client**</span><span class="sxs-lookup"><span data-stu-id="d79cb-122">Click **New client secret**</span></span>

   ![Cliquez sur nouvelle clé secrète client](../media/FBCimage7.png)

8. <span data-ttu-id="d79cb-124">Créer une nouvelle clé secrète.</span><span class="sxs-lookup"><span data-stu-id="d79cb-124">Create a new secret.</span></span> <span data-ttu-id="d79cb-125">Dans la zone Description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="d79cb-125">In the description box, type the secret and then choose an expiration period.</span></span> 

    ![Tapez le secret, puis choisissez une période d’expiration.](../media/FBCimage8.png)

9. <span data-ttu-id="d79cb-127">Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="d79cb-127">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="d79cb-128">Il s’agit de la clé secrète de l’application AAD que vous utilisez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d79cb-128">This is the AAD application secret that you use in later steps.</span></span>

   ![Copiez la valeur de la clé secrète et enregistrez-la.](../media/FBCimage9.png)


## <a name="step-2-deploy-the-connector-web-service-from-github-to-your-azure-account"></a><span data-ttu-id="d79cb-130">Étape 2 : déployer le service Web connecteur depuis GitHub vers votre compte Azure</span><span class="sxs-lookup"><span data-stu-id="d79cb-130">Step 2: Deploy the connector web service from GitHub to your Azure account</span></span>

1. <span data-ttu-id="d79cb-131">Accédez à [ce site github](https://github.com/microsoft/m365-sample-connector-csharp-aspnet) et cliquez sur **déployer vers Azure**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-131">Go to [this GitHub site](https://github.com/microsoft/m365-sample-connector-csharp-aspnet) and click **Deploy to Azure**.</span></span>

    ![Cliquez sur déployer vers Azure](../media/FBCGithubApp.png)

2. <span data-ttu-id="d79cb-133">Une fois que vous avez cliqué sur **déployer vers Azure**, vous serez redirigé vers un portail Azure avec une page de modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d79cb-133">After you click **Deploy to Azure**, you will be redirected to an Azure portal with a custom template page.</span></span> <span data-ttu-id="d79cb-134">Renseignez les détails de **base** et les **paramètres** , puis cliquez sur **acheter**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-134">Fill in the **Basics** and **Settings** details and then click **Purchase**.</span></span>

    - <span data-ttu-id="d79cb-135">**Abonnement :** Sélectionnez votre abonnement Azure pour lequel vous souhaitez déployer le service Web du connecteur de pages d’entreprise Facebook.</span><span class="sxs-lookup"><span data-stu-id="d79cb-135">**Subscription:** Select your Azure subscription that you want to deploy the Facebook Business pages connector web service to.</span></span>
    
    - <span data-ttu-id="d79cb-136">**Groupe de ressources :** Sélectionnez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="d79cb-136">**Resource group:** Choose or create a new resource group.</span></span> <span data-ttu-id="d79cb-137">Un groupe de ressources est un conteneur qui contient les ressources associées pour une solution Azure.</span><span class="sxs-lookup"><span data-stu-id="d79cb-137">A resource group is a container that holds related resources for an Azure solution.</span></span>

    - <span data-ttu-id="d79cb-138">**Emplacement :** Choisissez un emplacement.</span><span class="sxs-lookup"><span data-stu-id="d79cb-138">**Location:** Choose a location.</span></span>

    - <span data-ttu-id="d79cb-139">**Nom de l’application Web :** Fournissez un nom unique pour l’application Web de connecteur.</span><span class="sxs-lookup"><span data-stu-id="d79cb-139">**Web App Name:** Provide a unique name for the connector web app.</span></span> <span data-ttu-id="d79cb-140">Le nom doit comporter entre 3 et 18 caractères.</span><span class="sxs-lookup"><span data-stu-id="d79cb-140">Th name must be between 3 and 18 characters in length.</span></span> <span data-ttu-id="d79cb-141">Ce nom est utilisé pour créer l’URL du service d’application Azure ; par exemple, si vous spécifiez le nom de l’application Web **fbconnector** , l’URL du service d’application Azure sera **fbconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-141">This name is used to create the Azure app service URL; for example, if you provide the Web app name of **fbconnector** then the Azure app service URL  will be **fbconnector.azurewebsites.net**.</span></span>
    
    - <span data-ttu-id="d79cb-142">**tenantId :** ID de client de votre organisation Microsoft 365 que vous avez copié après avoir créé l’application de connecteur Facebook dans Azure Active Directory à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d79cb-142">**tenantId:** The tenant ID of your Microsoft 365 organization that you copied after creating the Facebook connector app in Azure Active Directory in Step 1.</span></span>
    
   - <span data-ttu-id="d79cb-143">**APISecretKey :** Vous pouvez taper n’importe quelle valeur comme clé secrète.</span><span class="sxs-lookup"><span data-stu-id="d79cb-143">**APISecretKey:** You can type any value as the secret.</span></span> <span data-ttu-id="d79cb-144">Il est utilisé pour accéder à l’application Web de connecteur à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="d79cb-144">This is used to access the connector web app in Step 5.</span></span>
   
     ![Cliquez sur créer une ressource et tapez le compte de stockage.](../media/FBCimage12.png)

3. <span data-ttu-id="d79cb-146">Une fois le déploiement réussi, la page ressemblera à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="d79cb-146">After the deployment is successful, the page will look similar to the following screenshot:</span></span>

     ![Cliquez sur stockage, puis sur compte de stockage.](../media/FBCimage13.png)

## <a name="step-3-register-the-facebook-app"></a><span data-ttu-id="d79cb-148">Étape 3 : inscrire l’application Facebook</span><span class="sxs-lookup"><span data-stu-id="d79cb-148">Step 3: Register the Facebook app</span></span>

1. <span data-ttu-id="d79cb-149">Accédez à <https://developers.facebook.com>, connectez-vous à l’aide des informations d’identification du compte pour les pages d’entreprise Facebook de votre organisation, puis cliquez sur **Ajouter une nouvelle application**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-149">Go to <https://developers.facebook.com>, log in using the credentials for the account for your organization’s Facebook Business pages, and then click **Add New App**.</span></span>

   ![Ajouter une nouvelle application pour la page d’entreprise Facebook](../media/FBCimage25.png)

2. <span data-ttu-id="d79cb-151">Créer un ID d’application.</span><span class="sxs-lookup"><span data-stu-id="d79cb-151">Create a new app ID.</span></span>

   ![Créer un ID d’application](../media/FBCimage26.png)

3. <span data-ttu-id="d79cb-153">Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis cliquez sur **configurer** dans la vignette de **connexion Facebook** .</span><span class="sxs-lookup"><span data-stu-id="d79cb-153">In the left navigation pane, click **Add Products** and then click **Set Up** in the **Facebook Login** tile.</span></span>

   ![Cliquez sur Ajouter des produits](../media/FBCimage27.png)

4. <span data-ttu-id="d79cb-155">Sur la page intégration de la connexion Facebook, cliquez sur **Web**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-155">On the Integrate Facebook Login page, click **Web**.</span></span>

   ![Cliquez sur Web dans la page intégration de la connexion Facebook](../media/FBCimage28.png)

5. <span data-ttu-id="d79cb-157">Ajoutez l’URL du service d’application Azure ; par exemple `https://fbconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="d79cb-157">Add the Azure app service URL; for example `https://fbconnector.azurewebsites.net`.</span></span>

   ![Ajouter l’URL du service d’application Azure](../media/FBCimage29.png)

6. <span data-ttu-id="d79cb-159">Complétez la section démarrage rapide de la configuration de connexion Facebook.</span><span class="sxs-lookup"><span data-stu-id="d79cb-159">Complete the QuickStart section of the Facebook Login setup.</span></span>

   ![Fin de la section démarrage rapide](../media/FBCimage30.png)

7. <span data-ttu-id="d79cb-161">Dans le volet de navigation de gauche sous **connexion Facebook**, cliquez sur **paramètres**, puis ajoutez l’URI de redirection OAuth dans la zone **URI de redirection OAuth valide** .</span><span class="sxs-lookup"><span data-stu-id="d79cb-161">In the left navigation pane under **Facebook Login**, click **Settings**, and add the OAuth redirect URI in the **Valid OAuth Redirect URIs** box.</span></span> <span data-ttu-id="d79cb-162">Utilisez le format \*\* \<connectorserviceuri>/views/facebookoauth\*\*, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation ; par exemple, `https://fbconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="d79cb-162">Use the format **\<connectorserviceuri>/Views/FacebookOAuth**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example, `https://fbconnector.azurewebsites.net`.</span></span>

   ![Ajouter l’URI de redirection OAuth à la zone URI de redirection OAuth valide](../media/FBCimage31.png)

8. <span data-ttu-id="d79cb-164">Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis sur **webhooks.**</span><span class="sxs-lookup"><span data-stu-id="d79cb-164">In the left navigation pane, click **Add Products** and then click **Webhooks.**</span></span> <span data-ttu-id="d79cb-165">Dans le menu déroulant **page** , cliquez sur **page**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-165">In the **Page** pull-down menu, click **Page**.</span></span> 

   ![Cliquez sur Ajouter des produits, puis cliquez sur \* \* webhooks](../media/FBCimage32.png)

9. <span data-ttu-id="d79cb-167">Ajoutez l’URL de rappel des webhooks et ajoutez un jeton de vérification.</span><span class="sxs-lookup"><span data-stu-id="d79cb-167">Add Webhooks Callback URL and add a verify token.</span></span> <span data-ttu-id="d79cb-168">Le format de l’URL de rappel, utilisez le format \*\* <connectorserviceuri>/API/FbPageWebhook\*\*, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation ; par exemple `https://fbconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="d79cb-168">The format of the callback URL, use the format **<connectorserviceuri>/api/FbPageWebhook**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example `https://fbconnector.azurewebsites.net`.</span></span> 

    <span data-ttu-id="d79cb-169">Le jeton Verify doit ressembler à un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="d79cb-169">The verify token should similar to a strong password.</span></span> <span data-ttu-id="d79cb-170">Copiez le jeton de vérification dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="d79cb-170">Copy the verify token to a text file or other storage location.</span></span>

        ![Add the verify token](../media/FBCimage33.png)

10. <span data-ttu-id="d79cb-171">Testez et abonnez-vous au point de terminaison pour le flux.</span><span class="sxs-lookup"><span data-stu-id="d79cb-171">Test and subscribe to the endpoint for feed.</span></span>

    ![Tester et s’abonner au point de terminaison](../media/FBCimage34.png)

11. <span data-ttu-id="d79cb-173">Ajoutez une URL de confidentialité, une icône d’application et une utilisation professionnelle.</span><span class="sxs-lookup"><span data-stu-id="d79cb-173">Add a privacy URL, app icon, and business use.</span></span> <span data-ttu-id="d79cb-174">Copiez également l’ID de l’application et la clé secrète de l’application dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="d79cb-174">Also, copy the app ID and app secret to a text file or other storage location.</span></span>

    ![Ajouter une URL de confidentialité, une icône d’application et une utilisation professionnelle](../media/FBCimage35.png)

12. <span data-ttu-id="d79cb-176">Rendez l’application publique.</span><span class="sxs-lookup"><span data-stu-id="d79cb-176">Make the app public.</span></span>

    ![Rendez l’application publique](../media/FBCimage36.png)

13. <span data-ttu-id="d79cb-178">Ajouter un utilisateur au rôle administrateur ou testeur.</span><span class="sxs-lookup"><span data-stu-id="d79cb-178">Add user to the admin or tester role.</span></span>

    ![Ajouter un utilisateur au rôle administrateur ou testeur](../media/FBCimage37.png)

14. <span data-ttu-id="d79cb-180">Ajoutez l’autorisation d' **accès au contenu public** de la page.</span><span class="sxs-lookup"><span data-stu-id="d79cb-180">Add the **Page Public Content Access** permission.</span></span>

    ![DD autorisation d’accès au contenu public de la page](../media/FBCimage38.png)

15. <span data-ttu-id="d79cb-182">Ajouter l’autorisation gérer les pages.</span><span class="sxs-lookup"><span data-stu-id="d79cb-182">Add Manage Pages permission.</span></span>

    ![Autorisation ajouter des pages](../media/FBCimage39.png)

16. <span data-ttu-id="d79cb-184">Obtenir l’application examinée par Facebook.</span><span class="sxs-lookup"><span data-stu-id="d79cb-184">Get the application reviewed by Facebook.</span></span>

    ![Obtenir l’application examinée par Facebook](../media/FBCimage40.png)

## <a name="step-4-configure-the-connector-web-app"></a><span data-ttu-id="d79cb-186">Étape 4 : configuration de l’application Web de connecteur</span><span class="sxs-lookup"><span data-stu-id="d79cb-186">Step 4: Configure the connector web app</span></span>

1. <span data-ttu-id="d79cb-187">Accédez à https://\<AzureAppResourceName>. azurewebsites.net (où AzureAppResourceName est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4) par exemple, si le nom est **fbconnector**, accédez à `https://fbconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="d79cb-187">Go to https://\<AzureAppResourceName>.azurewebsites.net (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4) For example, if the name is **fbconnector**, go to `https://fbconnector.azurewebsites.net`.</span></span> <span data-ttu-id="d79cb-188">La page d’accueil de l’application se présente comme la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="d79cb-188">The home page of the app will look like the following screenshot:</span></span>

   ![Accéder à l’application Web de votre connecteur](../media/FBCimage41.png)

2. <span data-ttu-id="d79cb-190">Cliquez sur **configurer** pour afficher une page de connexion.</span><span class="sxs-lookup"><span data-stu-id="d79cb-190">Click **Configure** to display a sign in page.</span></span>
 
   ![Cliquez sur configurer pour afficher une page de connexion.](../media/FBCimage42.png)

3. <span data-ttu-id="d79cb-192">Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="d79cb-192">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="d79cb-193">Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la configuration.</span><span class="sxs-lookup"><span data-stu-id="d79cb-193">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the configuration details page.</span></span>

    ![Connectez-vous à l’aide de votre ID de client et de votre mot de passe, puis accédez à la page Détails de configuration](../media/FBCimage43.png)

4. <span data-ttu-id="d79cb-195">Entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="d79cb-195">Enter the following configuration settings</span></span> 

   - <span data-ttu-id="d79cb-196">**ID d’application Facebook :** ID de l’application Facebook que vous avez obtenue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d79cb-196">**Facebook application ID:** The app ID for the Facebook application that you obtained in Step 3.</span></span>
   
   - <span data-ttu-id="d79cb-197">**Clé secrète de l’application Facebook :** La clé secrète de l’application Facebook que vous avez obtenue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d79cb-197">**Facebook application secret:** The app secret for the Facebook application that you obtained in Step 3.</span></span>
   
   - <span data-ttu-id="d79cb-198">**Jeton de vérification des webhooks Facebook :** Le jeton de vérification que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d79cb-198">**Facebook webhooks verify token:** The verify token that you created in Step 3.</span></span>
   
   - <span data-ttu-id="d79cb-199">**ID de l’application AAD :** L’ID d’application pour l’application Azure Active Directory que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d79cb-199">**AAD application ID:** The application ID for the Azure Active Directory app that you created in Step 1.</span></span>
   
   - <span data-ttu-id="d79cb-200">**Clé secrète de l’application AAD :** Valeur de la clé secrète APISecretKey que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d79cb-200">**AAD application secret:** The value for the APISecretKey secret that you created in Step 1.</span></span>

5. <span data-ttu-id="d79cb-201">Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="d79cb-201">Click **Save** to save the connector settings.</span></span>

## <a name="step-5-set-up-a-facebook-connector-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="d79cb-202">Étape 5 : configurer un connecteur Facebook dans le centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d79cb-202">Step 5: Set up a Facebook connector in the Microsoft 365 compliance center</span></span>

1. <span data-ttu-id="d79cb-203">Accédez à [https://compliance.microsoft.com](https://compliance.microsoft.com) , puis cliquez sur **connecteurs de données** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="d79cb-203">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="d79cb-204">Dans la page **connecteurs de données (aperçu)** , sous **pages professionnelles Facebook**, cliquez sur **affichage**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-204">On the **Data connectors (preview)** page under **Facebook Business pages**, click **View**.</span></span>

3. <span data-ttu-id="d79cb-205">Sur la page des **pages d’entreprise Facebook** , cliquez sur **Ajouter un connecteur**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-205">On the **Facebook business pages** page, click **Add connector**.</span></span>

4. <span data-ttu-id="d79cb-206">Sur la page **conditions de service** , cliquez sur **accepter**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-206">On the **Terms of service** page, click **Accept**.</span></span>

5.  <span data-ttu-id="d79cb-207">Dans la page **Ajouter des informations d’identification pour votre application connecteur** , entrez les informations suivantes, puis cliquez sur **valider la connexion**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-207">On the **Add credentials for your connector app** page, enter the following information and then click **Validate connection**.</span></span>

    ![Entrer les informations d’identification de l’application de connecteur](../media/TCimage38.png)

    - <span data-ttu-id="d79cb-209">Dans la zone **nom** , tapez un nom pour le connecteur, par exemple **page Facebook News**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-209">In the **Name** box, type a name for the connector, such as **Facebook news page**.</span></span>
    
    - <span data-ttu-id="d79cb-210">Dans la zone **URL de connexion** , tapez ou collez l’URL du service d’application Azure. par exemple `https://fbconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="d79cb-210">In the **Connection URL** box, type or paste the Azure app service URL; for example `https://fbconnector.azurewebsites.net`.</span></span>
    
    - <span data-ttu-id="d79cb-211">Dans la zone **mot de passe** , tapez ou collez la valeur du APISecretKey que vous avez ajouté à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="d79cb-211">In the **Password** box, type or paste the value of the APISecretKey that you added in Step 2.</span></span>
    
    - <span data-ttu-id="d79cb-212">Dans la zone ID d’application **Azure** , tapez ou collez la valeur de l’ID d’application (client) également appelé ID d’application AAD que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d79cb-212">In the **Azure App ID** box, type or paste the value of the Application (client) ID also called as AAD Application ID that you created in Step 1.</span></span>
 
6. <span data-ttu-id="d79cb-213">Une fois la connexion correctement validée, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-213">After the connection is successfully validated, click **Next**.</span></span>

7. <span data-ttu-id="d79cb-214">Sur la page **autoriser Microsoft 365 à importer des données** , tapez ou collez de nouveau le APISecretKey, puis cliquez sur **application Web de connexion**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-214">On the **Authorize Microsoft 365 to import data** page, type or paste the APISecretKey again and then click **Login web app**.</span></span>

8. <span data-ttu-id="d79cb-215">Sur la page **configurer l’application Facebook Connector** , cliquez sur **connexion avec Facebook** et connectez-vous à l’aide des informations d’identification du compte pour les pages d’entreprise Facebook de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d79cb-215">On the **Configure Facebook connector app** page, click **Login with Facebook** and log in using the credentials for the account for your organization's Facebook Business pages.</span></span> <span data-ttu-id="d79cb-216">Assurez-vous que le compte Facebook auquel vous vous êtes connecté se voit attribuer le rôle d’administrateur pour les pages d’entreprise Facebook de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d79cb-216">Make sure the Facebook account that you logged in to is assigned the admin role for your organization's Facebook Business pages.</span></span>

   ![Se connecter avec Facebook](../media/FBCimage50.png)

9. <span data-ttu-id="d79cb-218">Une liste des pages d’entreprise gérées par le compte Facebook auquel vous vous êtes connecté s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d79cb-218">A list of the business pages managed by the Facebook account that you logged in to is displayed.</span></span> <span data-ttu-id="d79cb-219">Sélectionnez la page à archiver, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-219">Select the page to archive and then click **Next**.</span></span>

    ![Sélectionnez la page d’entreprise que vous souhaitez archiver](../media/FBCimage52.png)

10. <span data-ttu-id="d79cb-221">Cliquez sur **Continuer** pour quitter le programme d’installation de l’application de service connecteur.</span><span class="sxs-lookup"><span data-stu-id="d79cb-221">Click **Continue** to exit the setup of the connector service app.</span></span>

11. <span data-ttu-id="d79cb-222">Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer initialement les éléments qui sont un certain âge.</span><span class="sxs-lookup"><span data-stu-id="d79cb-222">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="d79cb-223">Sélectionnez un âge, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-223">Select an age, and then click **Next**.</span></span>

12. <span data-ttu-id="d79cb-224">Dans la page **choisir l’emplacement de stockage** , tapez l’adresse de messagerie de la boîte aux lettres Microsoft 365 dans laquelle les éléments Facebook seront importés, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d79cb-224">On the **Choose storage location** page, type the email address of Microsoft 365 mailbox that the Facebook items will be imported to, and then click **Next**.</span></span>

13. <span data-ttu-id="d79cb-225">Sur l' **autorisation fournir un administrateur**, cliquez sur **accorder le consentement** , puis suivez les étapes.</span><span class="sxs-lookup"><span data-stu-id="d79cb-225">On the **Provide admin consent**, click **Provide consent** and then follow the steps.</span></span> <span data-ttu-id="d79cb-226">Vous devez être un administrateur général pour accorder le consentement du service d’importation Office 365 pour accéder aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d79cb-226">You must be a global admin to provide consent for the Office 365 Import service to access data in your organization.</span></span>

14. <span data-ttu-id="d79cb-227">Cliquez sur **suivant** pour passer en revue les paramètres du connecteur, puis cliquez sur **Terminer** pour terminer l’installation du connecteur.</span><span class="sxs-lookup"><span data-stu-id="d79cb-227">Click **Next** to review the connector settings and then click **Finish** to complete the connector setup.</span></span>

15. <span data-ttu-id="d79cb-228">Dans le centre de conformité, accédez à la page **connecteurs de données** , puis cliquez sur l’onglet **connecteurs** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="d79cb-228">In the compliance center, go to the **Data connectors** page, and click the **Connectors** tab to see the progress of the import process.</span></span>
