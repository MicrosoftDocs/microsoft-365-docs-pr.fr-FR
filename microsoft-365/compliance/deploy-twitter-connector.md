---
title: Déployer un connecteur pour archiver des données Twitter
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
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des données Twitter dans Microsoft 365. Une fois ces données importées dans Microsoft 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Twitter de votre organisation.
ms.openlocfilehash: 0dd996802964b2a2fc58d26e23af57193c89ee8c
ms.sourcegitcommit: 6fc6aaa2b7610e148f41018abd229e3c55b2f3d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49619910"
---
# <a name="deploy-a-connector-to-archive-twitter-data"></a><span data-ttu-id="eb127-104">Déployer un connecteur pour archiver des données Twitter</span><span class="sxs-lookup"><span data-stu-id="eb127-104">Deploy a connector to archive Twitter data</span></span>

<span data-ttu-id="eb127-105">Cet article contient le processus pas à pas pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir du compte Twitter de votre organisation vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="eb127-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Microsoft 365.</span></span> <span data-ttu-id="eb127-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Twitter, voir Configurer un connecteur pour archiver les [données Twitter. ](archive-twitter-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="eb127-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Set up a connector to archive Twitter data ](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-create-an-app-in-azure-active-directory"></a><span data-ttu-id="eb127-107">Étape 1 : Créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb127-107">Step 1: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="eb127-108">Go to <https://portal.azure.com> and sign in using the credentials of a global admin account.</span><span class="sxs-lookup"><span data-stu-id="eb127-108">Go to <https://portal.azure.com> and sign in using the credentials of a global admin account.</span></span>

   ![Connectez-vous à Azure](../media/TCimage01.png)

2. <span data-ttu-id="eb127-110">Dans le volet de navigation gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eb127-110">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![Go to Azure Active Directory](../media/TCimage02.png)

3. <span data-ttu-id="eb127-112">Dans le volet de navigation de gauche, cliquez sur **Inscriptions d’applications (prévisualisation),** puis sur **Nouvelle inscription.**</span><span class="sxs-lookup"><span data-stu-id="eb127-112">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![Créer une inscription d’application](../media/TCimage03.png)

4. <span data-ttu-id="eb127-114">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="eb127-114">Register the application.</span></span> <span data-ttu-id="eb127-115">Sous **URI de redirection (facultatif),** sélectionnez **Web** dans la liste rouge type d’application, puis tapez dans la zone de `https://portal.azure.com` l’URI.</span><span class="sxs-lookup"><span data-stu-id="eb127-115">Under **Redirect URI (optional)**, select **Web** in the application type dropdown list and then type `https://portal.azure.com` in the box for the URI.</span></span>

   ![<span data-ttu-id="eb127-116">Type https://portal.azure.com de l’URI de redirection</span><span class="sxs-lookup"><span data-stu-id="eb127-116">Type https://portal.azure.com for the redirect URI</span></span> ](../media/TCimage04.png)

5. <span data-ttu-id="eb127-117">Copiez **l’ID d’application (client)** et l’ID d’annuaire **(client)** et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="eb127-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="eb127-118">Vous utiliserez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb127-118">You use these IDs in later steps.</span></span>

    ![Copier et enregistrer l’ID d’application et l’ID d’annuaire](../media/TCimage05.png)

6. <span data-ttu-id="eb127-120">Go to **Certificates & secrets for the new app** and under Client **secrets** click New **client secret**.</span><span class="sxs-lookup"><span data-stu-id="eb127-120">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![Créer une nouvelle secret client](../media/TCimage06.png)

7. <span data-ttu-id="eb127-122">Créez une nouvelle secret.</span><span class="sxs-lookup"><span data-stu-id="eb127-122">Create a new secret.</span></span> <span data-ttu-id="eb127-123">Dans la zone de description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="eb127-123">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![Tapez la secret et choisissez la période d’expiration](../media/TCimage08.png)

8. <span data-ttu-id="eb127-125">Copiez la valeur de la secret et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="eb127-125">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="eb127-126">Il s’agit de la question secrète de l’application AAD que vous utiliserez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb127-126">This is the AAD application secret that you use in later steps.</span></span>

   ![Copier et enregistrer la secret](../media/TCimage09.png)


## <a name="step-2-deploy-the-connector-web-service-from-github-to-your-azure-account"></a><span data-ttu-id="eb127-128">Étape 2 : Déployer le service web connecteur à partir de GitHub votre compte Azure</span><span class="sxs-lookup"><span data-stu-id="eb127-128">Step 2: Deploy the connector web service from GitHub to your Azure account</span></span>

1. <span data-ttu-id="eb127-129">Go to [this GitHub site](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet) and click Deploy to **Azure**.</span><span class="sxs-lookup"><span data-stu-id="eb127-129">Go to [this GitHub site](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet) and click **Deploy to Azure**.</span></span>

    ![Go to the Azure home page](../media/FBCimage11.png)

2. <span data-ttu-id="eb127-131">Une fois que vous avez **cliqué sur Déployer** vers Azure, vous êtes redirigé vers un portail Azure avec une page de modèle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="eb127-131">After you click **Deploy to Azure**, you will be redirected to an Azure portal with a custom template page.</span></span> <span data-ttu-id="eb127-132">Remplissez les **informations de base** et **Paramètres,** puis cliquez sur **Acheter.**</span><span class="sxs-lookup"><span data-stu-id="eb127-132">Fill in the **Basics** and **Settings** details and then click **Purchase**.</span></span>

   ![Cliquez sur Créer un compte de stockage de ressources et de types](../media/FBCimage12.png)

    - <span data-ttu-id="eb127-134">**Abonnement :** Sélectionnez votre abonnement Azure sur qui vous souhaitez déployer le service web de connecteur Twitter.</span><span class="sxs-lookup"><span data-stu-id="eb127-134">**Subscription:** Select your Azure subscription that you want to deploy the Twitter connector web service to.</span></span>
    
    - <span data-ttu-id="eb127-135">**Groupe de ressources :** Choisissez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="eb127-135">**Resource group:** Choose or create a new resource group.</span></span> <span data-ttu-id="eb127-136">Un groupe de ressources est un conteneur qui contient des ressources associées pour une solution Azure.</span><span class="sxs-lookup"><span data-stu-id="eb127-136">A resource group is a container that holds related resources for an Azure solution.</span></span>

    - <span data-ttu-id="eb127-137">**Emplacement :** Choisissez un emplacement.</span><span class="sxs-lookup"><span data-stu-id="eb127-137">**Location:** Choose a location.</span></span>

    - <span data-ttu-id="eb127-138">**Nom de l’application web :** Fournissez un nom unique pour l’application web du connecteur.</span><span class="sxs-lookup"><span data-stu-id="eb127-138">**Web App Name:** Provide a unique name for the connector web app.</span></span> <span data-ttu-id="eb127-139">La longueur du nom doit être de 3 à 18 caractères.</span><span class="sxs-lookup"><span data-stu-id="eb127-139">Th name must be between 3 and 18 characters in length.</span></span> <span data-ttu-id="eb127-140">Ce nom est utilisé pour créer l’URL du service d’application Azure ; par exemple, si vous fournissez le nom de l’application Web **twitterconnector,** l’URL du service d’application Azure **sera twitterconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="eb127-140">This name is used to create the Azure app service URL; for example, if you provide the Web app name of **twitterconnector** then the Azure app service URL  will be **twitterconnector.azurewebsites.net**.</span></span>
    
    - <span data-ttu-id="eb127-141">**tenantId :** ID client de votre organisation Microsoft 365 que vous avez copié après avoir créé l’application connecteur Facebook dans Azure Active Directory à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="eb127-141">**tenantId:** The tenant ID of your Microsoft 365 organization that you copied after creating the Facebook connector app in Azure       Active Directory in Step 1.</span></span>
    
   - <span data-ttu-id="eb127-142">**APISecretKey :** Vous pouvez taper n’importe quelle valeur comme secret.</span><span class="sxs-lookup"><span data-stu-id="eb127-142">**APISecretKey:** You can type any value as the secret.</span></span> <span data-ttu-id="eb127-143">Il permet d’accéder à l’application web de connecteur à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="eb127-143">This is used to access the connector web app in Step 5.</span></span>

3. <span data-ttu-id="eb127-144">Une fois le déploiement réussi, la page ressemble à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="eb127-144">After the deployment is successful, the page will look similar to the following screenshot:</span></span>

    ![Cliquez Stockage puis cliquez sur Stockage compte](../media/FBCimage13.png)

## <a name="step-3-create-the-twitter-app"></a><span data-ttu-id="eb127-146">Étape 3 : Créer l’application Twitter</span><span class="sxs-lookup"><span data-stu-id="eb127-146">Step 3: Create the Twitter app</span></span>

1. <span data-ttu-id="eb127-147">Go to https://developer.twitter.com , log in using the credentials for the developer account for your organization, and then click **Apps**.</span><span class="sxs-lookup"><span data-stu-id="eb127-147">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![Go to https://developer.twitter.com and log in](../media/TCimage25-5.png)
2. <span data-ttu-id="eb127-149">Cliquez **sur Créer une application.**</span><span class="sxs-lookup"><span data-stu-id="eb127-149">Click **Create an app**.</span></span>
   
   ![Go to Apps page to create an app](../media/TCimage26.png)

3. <span data-ttu-id="eb127-151">Sous **Détails de l’application,** ajoutez des informations sur l’application.</span><span class="sxs-lookup"><span data-stu-id="eb127-151">Under **App details**, add information about the application.</span></span>

   ![Entrer des informations sur l’application](../media/TCimage27.png)

4. <span data-ttu-id="eb127-153">Dans le tableau de bord du développeur Twitter, sélectionnez l’application que vous avez créée, puis cliquez sur **Détails.**</span><span class="sxs-lookup"><span data-stu-id="eb127-153">On the Twitter developer dashboard, select the app that you just created and then click **Details**.</span></span>
   
   ![Copier et enregistrer l’ID d’application](../media/TCimage28.png)

5. <span data-ttu-id="eb127-155">Sous **l’onglet** Clés et jetons, sous Clés **d’API** consommateur, copiez la clé d’API et la clé secrète API et enregistrez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="eb127-155">On the **Keys and tokens** tab, under **Consumer API keys** copy both the API Key and the API secret key and save them to a text file or other storage location.</span></span> <span data-ttu-id="eb127-156">Cliquez ensuite **sur Créer** pour générer un jeton d’accès et une secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="eb127-156">Then click **Create** to generate an access token and access token secret and copy these to a text file or other storage location.</span></span>
   
   ![Copier et enregistrer dans la clé secrète API](../media/TCimage29.png)

   <span data-ttu-id="eb127-158">Cliquez ensuite **sur Créer** pour générer un jeton d’accès et une secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="eb127-158">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="eb127-159">Cliquez sur **l’onglet Autorisations** et configurez les autorisations comme illustré dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="eb127-159">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![Configuration des autorisations](../media/TCimage30.png)

7. <span data-ttu-id="eb127-161">Après avoir enregistrer les paramètres d’autorisation, cliquez sur l’onglet **Détails** de l’application, puis cliquez sur **Modifier > modifier les détails.**</span><span class="sxs-lookup"><span data-stu-id="eb127-161">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![Modifier les détails de l’application](../media/TCimage31.png)

8. <span data-ttu-id="eb127-163">Effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb127-163">Do the following tasks:</span></span>

   - <span data-ttu-id="eb127-164">Cochez la case pour autoriser l’application connecteur à se connecter à Twitter.</span><span class="sxs-lookup"><span data-stu-id="eb127-164">Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   - <span data-ttu-id="eb127-165">Ajoutez l’URI de redirection OAuth au format suivant : **\<connectorserviceuri> /Views/TwitterOAuth**, où la valeur de *connectorserviceuri* est l’URL du service d’application Azure pour votre organisation ; par exemple, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth .</span><span class="sxs-lookup"><span data-stu-id="eb127-165">Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

    ![Autoriser l’application connecteur à se connecter à Twitter et ajouter un URI de redirection OAuth](../media/TCimage32.png)

<span data-ttu-id="eb127-167">L’application de développement Twitter est maintenant prête à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="eb127-167">The Twitter developer app is now ready to use.</span></span>

## <a name="step-4-configure-the-connector-web-app"></a><span data-ttu-id="eb127-168">Étape 4 : Configurer l’application web du connecteur</span><span class="sxs-lookup"><span data-stu-id="eb127-168">Step 4: Configure the connector web app</span></span> 

1. <span data-ttu-id="eb127-169">Go to https:// \<AzureAppResourceName> .azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4).</span><span class="sxs-lookup"><span data-stu-id="eb127-169">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4).</span></span> <span data-ttu-id="eb127-170">Par exemple, si le nom est **twitterconnector**, allez à https://twitterconnector.azurewebsites.net .</span><span class="sxs-lookup"><span data-stu-id="eb127-170">For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="eb127-171">La page d’accueil de l’application ressemble à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="eb127-171">The home page of the app looks like the following screenshot:</span></span>

   ![Go to Azure app resource page](../media/FBCimage41.png)

2. <span data-ttu-id="eb127-173">Cliquez **sur Configurer pour** afficher une page de signature.</span><span class="sxs-lookup"><span data-stu-id="eb127-173">Click **Configure** to display a sign in page.</span></span>

   ![Cliquez sur Configurer pour afficher la page de signature](../media/FBCimage42.png)

3. <span data-ttu-id="eb127-175">Dans la zone ID de locataire, tapez ou collez votre ID de client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="eb127-175">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="eb127-176">Dans la zone de mot de passe, tapez ou collez la clé APISecretKey (obtenue à l’étape 2), puis cliquez sur Définir la configuration **Paramètres** pour afficher la page de détails de configuration.</span><span class="sxs-lookup"><span data-stu-id="eb127-176">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the configuration details page.</span></span>

   ![Se connectez à l’aide de l’ID client et de la clé secrète API](../media/TCimage35.png)

4. <span data-ttu-id="eb127-178">Entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="eb127-178">Enter the following configuration settings</span></span> 

   - <span data-ttu-id="eb127-179">**Clé d’api Twitter :** Clé d’API pour l’application Twitter que vous avez créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="eb127-179">**Twitter Api Key:** The API key for the Twitter application that you created in Step 3.</span></span>
   
   - <span data-ttu-id="eb127-180">**Clé secrète de l’api Twitter :** Clé secrète API pour l’application Twitter que vous avez créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="eb127-180">**Twitter Api Secret Key:** The API secret key for the Twitter application that you created in Step 3.</span></span>
   
   - <span data-ttu-id="eb127-181">**Jeton d’accès Twitter :** Jeton d’accès que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="eb127-181">**Twitter Access Token:** The access token that you created in Step 3.</span></span>
   
   - <span data-ttu-id="eb127-182">**Secret du jeton d’accès Twitter :** Secret de jeton d’accès que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="eb127-182">**Twitter Access Token Secret:** The access token secret that you created in Step 3.</span></span>
   
   - <span data-ttu-id="eb127-183">**ID d’application AAD :** ID de l’application Azure Active Directory que vous avez créée à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="eb127-183">**AAD Application ID:** The application ID for the Azure Active Directory app that you created in Step 1</span></span>
   
   - <span data-ttu-id="eb127-184">**Secret d’application AAD :** Valeur de la clé secrète APISecretKey que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="eb127-184">**AAD Application Secret:** The value for the APISecretKey secret that you created in Step 1.</span></span>

5. <span data-ttu-id="eb127-185">Cliquez **sur Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="eb127-185">Click **Save** to save the connector settings.</span></span>

## <a name="step-5-set-up-a-twitter-connector-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="eb127-186">Étape 5 : Configurer un connecteur Twitter dans le centre Microsoft 365 conformité</span><span class="sxs-lookup"><span data-stu-id="eb127-186">Step 5: Set up a Twitter connector in the Microsoft 365 compliance center</span></span>

1. <span data-ttu-id="eb127-187">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click Data **connectors** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="eb127-187">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="eb127-188">Dans la page **Connecteurs de données** sous **Twitter,** cliquez sur **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="eb127-188">On the **Data connectors** page under **Twitter**, click **View**.</span></span>

3. <span data-ttu-id="eb127-189">Dans la page **Twitter,** cliquez sur **Ajouter un connecteur.**</span><span class="sxs-lookup"><span data-stu-id="eb127-189">On the **Twitter** page, click **Add connector**.</span></span>

4. <span data-ttu-id="eb127-190">Dans la page **Conditions d’utilisation,** cliquez sur **Accepter.**</span><span class="sxs-lookup"><span data-stu-id="eb127-190">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="eb127-191">Dans la page **Ajouter des informations d’identification pour votre** application de connecteur, entrez les informations suivantes, puis cliquez sur Valider la **connexion.**</span><span class="sxs-lookup"><span data-stu-id="eb127-191">On the **Add credentials for your connector app** page, enter the following information and then click **Validate connection**.</span></span>

   ![Entrer les informations d’identification de l’application connecteur](../media/TCimage38.png)

    - <span data-ttu-id="eb127-193">Dans la **zone** Nom, tapez un nom pour le connecteur, tel que le handle **d’aide de Twitter.**</span><span class="sxs-lookup"><span data-stu-id="eb127-193">In the **Name** box, type a name for the connector, such as **Twitter help handle**.</span></span>
    
    - <span data-ttu-id="eb127-194">Dans la zone **URL du connecteur,** tapez ou collez l’URL du service d’application Azure . par `https://twitterconnector.azurewebsites.net` exemple.</span><span class="sxs-lookup"><span data-stu-id="eb127-194">In the **Connector URL** box, type or paste the Azure app service URL; for example `https://twitterconnector.azurewebsites.net`.</span></span>
    
    - <span data-ttu-id="eb127-195">Dans la **zone Mot** de passe, tapez ou collez la valeur de l’APISecretKey que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="eb127-195">In the **Password** box, type or paste the value of the APISecretKey that you created in Step 2.</span></span>
    
    - <span data-ttu-id="eb127-196">Dans la **zone ID** d’application Azure, tapez ou collez la valeur de l’ID d’application Azure (également appelé *ID client)* que vous avez obtenue à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="eb127-196">In the **Azure App ID** box, type or paste the value of the Azure Application App Id (also called the *client ID*) that you obtained in Step 1.</span></span>

6. <span data-ttu-id="eb127-197">Une fois la connexion validée, cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="eb127-197">After the connection is successfully validated, click **Next**.</span></span>

7. <span data-ttu-id="eb127-198">Dans la page **Autoriser Microsoft 365** importer des données, tapez ou collez de nouveau l’APISecretKey, puis cliquez sur Login **web app**.</span><span class="sxs-lookup"><span data-stu-id="eb127-198">On the **Authorize Microsoft 365 to import data** page, type or paste the APISecretKey again and then click  **Login web app**.</span></span>

8. <span data-ttu-id="eb127-199">Cliquez **sur Se connecter avec Twitter.**</span><span class="sxs-lookup"><span data-stu-id="eb127-199">Click **Login with Twitter**.</span></span>

9. <span data-ttu-id="eb127-200">Sur la page de connexion à Twitter, connectez-vous à l’aide des informations d’identification du compte Twitter de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="eb127-200">On the Twitter sign in page, sign in using the credentials for your organization's Twitter account.</span></span>

   ![Se connectez à un compte Twitter](../media/TCimage42.png)

   <span data-ttu-id="eb127-202">Une fois que vous êtes connecté, la page Twitter affiche le message suivant, « Le travail connecteur Twitter a été correctement installé ».</span><span class="sxs-lookup"><span data-stu-id="eb127-202">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

10. <span data-ttu-id="eb127-203">Cliquez **sur Continuer** pour terminer la configuration du connecteur Twitter.</span><span class="sxs-lookup"><span data-stu-id="eb127-203">Click **Continue** to complete setting up the Twitter connector.</span></span>

11. <span data-ttu-id="eb127-204">Dans la page **Définir les filtres,** vous pouvez appliquer un filtre pour importer initialement des éléments d’un certain âge.</span><span class="sxs-lookup"><span data-stu-id="eb127-204">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="eb127-205">Sélectionnez un âge, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eb127-205">Select an age, and then click **Next**.</span></span>

12. <span data-ttu-id="eb127-206">Dans la page **Choisir** l’emplacement de stockage, tapez l’adresse de messagerie Microsoft 365 boîte aux lettres dans Microsoft 365 vers qui les éléments Twitter seront importés, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eb127-206">On the **Choose storage location** page, type the email address of Microsoft 365 mailbox that the Twitter items will be imported to, and then click **Next**.</span></span>

13. <span data-ttu-id="eb127-207">Cliquez **sur Suivant** pour passer en revue les paramètres du connecteur, puis cliquez sur **Terminer** pour terminer la configuration du connecteur.</span><span class="sxs-lookup"><span data-stu-id="eb127-207">Click **Next** to review the connector settings and then click **Finish** to complete the connector setup.</span></span>

14. <span data-ttu-id="eb127-208">Dans le centre de conformité, allez à la page **Connecteurs** de données, puis cliquez sur l’onglet **Connecteurs** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="eb127-208">In the compliance center, go to the **Data connectors** page, and click the **Connectors** tab to see the progress of the import process.</span></span>
