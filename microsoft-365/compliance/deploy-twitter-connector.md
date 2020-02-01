---
title: Déploiement d’un connecteur pour l’archivage des données Twitter
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
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des données Twitter vers Microsoft 365. Une fois ces données importées dans Microsoft 365, vous pouvez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Twitter de votre organisation.
ms.openlocfilehash: 9951040335a2dcacc90ac4dc7a6f3e5079bf5692
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595279"
---
# <a name="deploy-a-connector-to-archive-twitter-data"></a><span data-ttu-id="4d90f-104">Déploiement d’un connecteur pour l’archivage des données Twitter</span><span class="sxs-lookup"><span data-stu-id="4d90f-104">Deploy a connector to archive Twitter data</span></span>

<span data-ttu-id="4d90f-105">Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir du compte Twitter de votre organisation vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4d90f-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Microsoft 365.</span></span> <span data-ttu-id="4d90f-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Twitter, reportez-vous à la rubrique [configurer un connecteur pour archiver les données Twitter ](archive-twitter-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="4d90f-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Set up a connector to archive Twitter data ](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-create-an-app-in-azure-active-directory"></a><span data-ttu-id="4d90f-107">Étape 1 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4d90f-107">Step 1: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="4d90f-108">Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.</span><span class="sxs-lookup"><span data-stu-id="4d90f-108">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

   ![Se connecter à Azure](media/TCimage01.png)

2. <span data-ttu-id="4d90f-110">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-110">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![Accéder à Azure Active Directory](media/TCimage02.png)

3. <span data-ttu-id="4d90f-112">Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-112">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![Créer une nouvelle inscription d’application](media/TCimage03.png)

4. <span data-ttu-id="4d90f-114">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="4d90f-114">Register the application.</span></span> <span data-ttu-id="4d90f-115">Sous **URI de redirection (facultatif)**, sélectionnez **Web** dans la liste déroulante type d' `https://portal.azure.com` application, puis tapez dans la zone de l’URI.</span><span class="sxs-lookup"><span data-stu-id="4d90f-115">Under **Redirect URI (optional)**, select **Web** in the application type dropdown list and then type `https://portal.azure.com` in the box for the URI.</span></span>

   ![<span data-ttu-id="4d90f-116">Type https://portal.azure.com de l’URI de redirection</span><span class="sxs-lookup"><span data-stu-id="4d90f-116">Type https://portal.azure.com for the redirect URI</span></span> ](media/TCimage04.png)

5. <span data-ttu-id="4d90f-117">Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="4d90f-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="4d90f-118">Vous utilisez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4d90f-118">You use these IDs in later steps.</span></span>

    ![Copier et enregistrer l’ID de l’application et l’ID du répertoire](media/TCimage05.png)

6. <span data-ttu-id="4d90f-120">Accédez à **certificats & secrets de la nouvelle application** , puis sous **secrets client** , cliquez sur **nouvelle clé secrète client**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-120">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![Créer une clé secrète client](media/TCimage06.png)

7. <span data-ttu-id="4d90f-122">Créer une nouvelle clé secrète.</span><span class="sxs-lookup"><span data-stu-id="4d90f-122">Create a new secret.</span></span> <span data-ttu-id="4d90f-123">Dans la zone Description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="4d90f-123">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![Tapez le secret et choisissez la période d’expiration.](media/TCimage08.png)

8. <span data-ttu-id="4d90f-125">Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="4d90f-125">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="4d90f-126">Il s’agit de la clé secrète de l’application AAD que vous utilisez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4d90f-126">This is the AAD application secret that you use in later steps.</span></span>

   ![Copier et enregistrer la clé secrète](media/TCimage09.png)


## <a name="step-2-deploy-the-connector-web-service-from-github-to-your-azure-account"></a><span data-ttu-id="4d90f-128">Étape 2 : déployer le service Web connecteur depuis GitHub vers votre compte Azure</span><span class="sxs-lookup"><span data-stu-id="4d90f-128">Step 2: Deploy the connector web service from GitHub to your Azure account</span></span>

1. <span data-ttu-id="4d90f-129">Accédez à [ce site github](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet) et cliquez sur **déployer vers Azure**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-129">Go to [this GitHub site](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet) and click **Deploy to Azure**.</span></span>

    ![Accéder à la page d’accueil Azure](media/FBCimage11.png)

2. <span data-ttu-id="4d90f-131">Une fois que vous avez cliqué sur **déployer vers Azure**, vous serez redirigé vers un portail Azure avec une page de modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4d90f-131">After you click **Deploy to Azure**, you will be redirected to an Azure portal with a custom template page.</span></span> <span data-ttu-id="4d90f-132">Renseignez les détails de **base** et les **paramètres** , puis cliquez sur **acheter**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-132">Fill in the **Basics** and **Settings** details and then click **Purchase**.</span></span>

   ![Cliquez sur créer une ressource et tapez le compte de stockage.](media/FBCimage12.png)

    - <span data-ttu-id="4d90f-134">**Abonnement :** Sélectionnez votre abonnement Azure pour lequel vous souhaitez déployer le service Web du connecteur Twitter.</span><span class="sxs-lookup"><span data-stu-id="4d90f-134">**Subscription:** Select your Azure subscription that you want to deploy the Twitter connector web service to.</span></span>
    
    - <span data-ttu-id="4d90f-135">**Groupe de ressources :** Sélectionnez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="4d90f-135">**Resource group:** Choose or create a new resource group.</span></span> <span data-ttu-id="4d90f-136">Un groupe de ressources est un conteneur qui contient les ressources associées pour une solution Azure.</span><span class="sxs-lookup"><span data-stu-id="4d90f-136">A resource group is a container that holds related resources for an Azure solution.</span></span>

    - <span data-ttu-id="4d90f-137">**Emplacement :** Choisissez un emplacement.</span><span class="sxs-lookup"><span data-stu-id="4d90f-137">**Location:** Choose a location.</span></span>

    - <span data-ttu-id="4d90f-138">**Nom de l’application Web :** Fournissez un nom unique pour l’application Web de connecteur.</span><span class="sxs-lookup"><span data-stu-id="4d90f-138">**Web App Name:** Provide a unique name for the connector web app.</span></span> <span data-ttu-id="4d90f-139">Le nom doit comporter entre 3 et 18 caractères.</span><span class="sxs-lookup"><span data-stu-id="4d90f-139">Th name must be between 3 and 18 characters in length.</span></span> <span data-ttu-id="4d90f-140">Ce nom est utilisé pour créer l’URL du service d’application Azure ; par exemple, si vous spécifiez le nom de l’application Web **twitterconnector** , l’URL du service d’application Azure sera **twitterconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-140">This name is used to create the Azure app service URL; for example, if you provide the Web app name of **twitterconnector** then the Azure app service URL  will be **twitterconnector.azurewebsites.net**.</span></span>
    
    - <span data-ttu-id="4d90f-141">**tenantId :** ID de client de votre organisation Microsoft 365 que vous avez copié après avoir créé l’application de connecteur Facebook dans Azure Active Directory à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="4d90f-141">**tenantId:** The tenant ID of your Microsoft 365 organization that you copied after creating the Facebook connector app in Azure       Active Directory in Step 1.</span></span>
    
   - <span data-ttu-id="4d90f-142">**APISecretKey :** Vous pouvez taper n’importe quelle valeur comme clé secrète.</span><span class="sxs-lookup"><span data-stu-id="4d90f-142">**APISecretKey:** You can type any value as the secret.</span></span> <span data-ttu-id="4d90f-143">Il est utilisé pour accéder à l’application Web de connecteur à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="4d90f-143">This is used to access the connector web app in Step 5.</span></span>

3. <span data-ttu-id="4d90f-144">Une fois le déploiement réussi, la page ressemblera à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="4d90f-144">After the deployment is successful, the page will look similar to the following screenshot:</span></span>

    ![Cliquez sur stockage, puis sur compte de stockage.](media/FBCimage13.png)

## <a name="step-3-create-the-twitter-app"></a><span data-ttu-id="4d90f-146">Étape 3 : créer l’application Twitter</span><span class="sxs-lookup"><span data-stu-id="4d90f-146">Step 3: Create the Twitter app</span></span>

1. <span data-ttu-id="4d90f-147">Accédez à https://developer.twitter.com, connectez-vous à l’aide des informations d’identification pour le compte de développeur de votre organisation, puis cliquez sur **applications**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-147">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![Accédez à https://developer.twitter.com et connectez-vous](media/TCimage25-5.png)
2. <span data-ttu-id="4d90f-149">Cliquez sur **créer une application**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-149">Click **Create an app**.</span></span>
   
   ![Accéder à la page applications pour créer une application](media/TCimage26.png)

3. <span data-ttu-id="4d90f-151">Sous **Détails**de l’application, ajoutez des informations sur l’application.</span><span class="sxs-lookup"><span data-stu-id="4d90f-151">Under **App details**, add information about the application.</span></span>

   ![Entrer des informations sur l’application](media/TCimage27.png)

4. <span data-ttu-id="4d90f-153">Dans le tableau de bord du développeur Twitter, sélectionnez l’application que vous venez de créer et copiez l’ID d’application affiché et enregistrez-le dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="4d90f-153">On the Twitter developer dashboard, select the app that you just created and copy the App ID that's displayed  and save it to a text file or other storage location.</span></span> <span data-ttu-id="4d90f-154">Ensuite, cliquez sur **Détails**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-154">Then click **Details**.</span></span>
   
   ![Copier et enregistrer l’ID de l’application](media/TCimage28.png)

5. <span data-ttu-id="4d90f-156">Sous l’onglet **clés et jetons** , sous clés de l' **API consommateur** , copiez la clé secrète de l’API et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="4d90f-156">On the **Keys and tokens** tab, under **Consumer API keys** copy the API secret key and save it to a text file or other storage location.</span></span> <span data-ttu-id="4d90f-157">Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="4d90f-157">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>
   
   ![Copier et enregistrer dans la clé secrète de l’API](media/TCimage29.png)

   <span data-ttu-id="4d90f-159">Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="4d90f-159">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="4d90f-160">Cliquez sur l’onglet **autorisations** et configurez les autorisations comme indiqué dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="4d90f-160">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![Configurer des autorisations](media/TCimage30.png)

7. <span data-ttu-id="4d90f-162">Une fois que vous avez enregistré les paramètres d’autorisation, cliquez sur l’onglet Détails de l' **application** , puis cliquez sur **modifier > modifier les détails**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-162">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![Modifier les détails de l’application](media/TCimage31.png)

8. <span data-ttu-id="4d90f-164">Effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d90f-164">Do the following tasks:</span></span>

   - <span data-ttu-id="4d90f-165">Activez la case à cocher pour autoriser l’application de connecteur à se connecter à Twitter.</span><span class="sxs-lookup"><span data-stu-id="4d90f-165">Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   - <span data-ttu-id="4d90f-166">Ajoutez l’URI de redirection OAuth en utilisant le format suivant : \*\* \<connectorserviceuri>/views/twitteroauth\*\*, où la valeur de *connectorserviceuri* est l’URL de service d’application Azure pour votre organisation ; par exemple, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span><span class="sxs-lookup"><span data-stu-id="4d90f-166">Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

    ![Autoriser l’application de connecteur à se connecter à Twitter et ajouter l’URI de redirection OAuth](media/TCimage32.png)

<span data-ttu-id="4d90f-168">L’application de développeur Twitter est maintenant prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="4d90f-168">The Twitter developer app is now ready to use.</span></span>

## <a name="step-4-configure-the-connector-web-app"></a><span data-ttu-id="4d90f-169">Étape 4 : configuration de l’application Web de connecteur</span><span class="sxs-lookup"><span data-stu-id="4d90f-169">Step 4: Configure the connector web app</span></span> 

1. <span data-ttu-id="4d90f-170">Accédez à https://\<AzureAppResourceName>. azurewebsites.net (où **AzureAppResourceName** est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4).</span><span class="sxs-lookup"><span data-stu-id="4d90f-170">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4).</span></span> <span data-ttu-id="4d90f-171">Par exemple, si le nom est **twitterconnector**, accédez à https://twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="4d90f-171">For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="4d90f-172">La page d’accueil de l’application se présente comme la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="4d90f-172">The home page of the app looks like the following screenshot:</span></span>

   ![Accéder à la page des ressources de l’application Azure](media/FBCimage41.png)

2. <span data-ttu-id="4d90f-174">Cliquez sur **configurer** pour afficher une page de connexion.</span><span class="sxs-lookup"><span data-stu-id="4d90f-174">Click **Configure** to display a sign in page.</span></span>

   ![Cliquez sur configurer pour afficher la page de connexion.](media/FBCimage42.png)

3. <span data-ttu-id="4d90f-176">Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="4d90f-176">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="4d90f-177">Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la configuration.</span><span class="sxs-lookup"><span data-stu-id="4d90f-177">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the configuration details page.</span></span>

   ![Se connecter à l’aide de l’ID de client et de la clé secrète d’API](media/TCimage35.png)

4. <span data-ttu-id="4d90f-179">Entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="4d90f-179">Enter the following configuration settings</span></span> 

   - <span data-ttu-id="4d90f-180">**Clé de l’API Twitter :** ID d’application de l’application Twitter que vous avez créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="4d90f-180">**Twitter Api Key:** The app ID for the Twitter application that you created in Step 3.</span></span>
   
   - <span data-ttu-id="4d90f-181">**Clé secrète de l’API Twitter :** Clé secrète de l’API pour l’application Twitter que vous avez créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="4d90f-181">**Twitter Api Secret Key:** The API secret key for the Twitter application that you created in Step 3.</span></span>
   
   - <span data-ttu-id="4d90f-182">**Jeton d’accès Twitter :** Le jeton d’accès que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="4d90f-182">**Twitter Access Token:** The access token that you created in Step 3.</span></span>
   
   - <span data-ttu-id="4d90f-183">**Jeton d’accès Twitter secret :** Code secret de jeton d’accès que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="4d90f-183">**Twitter Access Token Secret:** The access token secret that you created in Step 3.</span></span>
   
   - <span data-ttu-id="4d90f-184">**ID de l’application AAD :** L’ID d’application pour l’application Azure Active Directory que vous avez créée à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="4d90f-184">**AAD Application ID:** The application ID for the Azure Active Directory app that you created in Step 1</span></span>
   
   - <span data-ttu-id="4d90f-185">**Clé secrète de l’application AAD :** Valeur de la clé secrète APISecretKey que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="4d90f-185">**AAD Application Secret:** The value for the APISecretKey secret that you created in Step 1.</span></span>

5. <span data-ttu-id="4d90f-186">Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="4d90f-186">Click **Save** to save the connector settings.</span></span>

## <a name="step-5-set-up-a-twitter-connector-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="4d90f-187">Étape 5 : configurer un connecteur Twitter dans le centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4d90f-187">Step 5: Set up a Twitter connector in the Microsoft 365 compliance center</span></span>

1. <span data-ttu-id="4d90f-188">Accédez à [https://compliance.microsoft.com](https://compliance.microsoft.com) , puis cliquez sur **connecteurs de données** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="4d90f-188">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and then click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="4d90f-189">Dans la page **connecteurs de données (aperçu)** , sous **Twitter**, cliquez sur **affichage**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-189">On the **Data connectors (preview)** page under **Twitter**, click **View**.</span></span>

3. <span data-ttu-id="4d90f-190">Sur la page **Twitter** , cliquez sur **Ajouter un connecteur**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-190">On the **Twitter** page, click **Add connector**.</span></span>

4. <span data-ttu-id="4d90f-191">Sur la page **conditions de service** , cliquez sur **accepter**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-191">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="4d90f-192">Dans la page **Ajouter des informations d’identification pour votre application connecteur** , entrez les informations suivantes, puis cliquez sur **valider la connexion**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-192">On the **Add credentials for your connector app** page, enter the following information and then click **Validate connection**.</span></span>

   ![Entrer les informations d’identification de l’application de connecteur](media/TCimage38.png)

    - <span data-ttu-id="4d90f-194">Dans la zone **nom** , tapez un nom pour le connecteur, tel que le **Gestionnaire d’aide Twitter**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-194">In the **Name** box, type a name for the connector, such as **Twitter help handle**.</span></span>
    
    - <span data-ttu-id="4d90f-195">Dans la zone **URL du connecteur** , tapez ou collez l’URL du service d’application Azure. par exemple `https://twitterconnector.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="4d90f-195">In the **Connector URL** box, type or paste the Azure app service URL; for example `https://twitterconnector.azurewebsites.net`.</span></span>
    
    - <span data-ttu-id="4d90f-196">Dans la zone **mot de passe** , tapez ou collez la valeur du APISecretKey que vous avez créé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="4d90f-196">In the **Password** box, type or paste the value of the APISecretKey that you created in Step 2.</span></span>
    
    - <span data-ttu-id="4d90f-197">Dans la zone ID d’application **Azure** , tapez ou collez la valeur de l’ID d’application Azure (également appelé *ID client*) que vous avez obtenu à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="4d90f-197">In the **Azure App ID** box, type or paste the value of the Azure Application App Id (also called the *client ID*) that you obtained in Step 1.</span></span>

6. <span data-ttu-id="4d90f-198">Une fois la connexion correctement validée, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-198">After the connection is successfully validated, click **Next**.</span></span>

7. <span data-ttu-id="4d90f-199">Sur la page **autoriser Microsoft 365 à importer des données** , tapez ou collez de nouveau le APISecretKey, puis cliquez sur **application Web de connexion**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-199">On the **Authorize Microsoft 365 to import data** page, type or paste the APISecretKey again and then click  **Login web app**.</span></span>

8. <span data-ttu-id="4d90f-200">Cliquez sur **connexion avec Twitter**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-200">Click **Login with Twitter**.</span></span>

9. <span data-ttu-id="4d90f-201">Sur la page de connexion Twitter, connectez-vous à l’aide des informations d’identification du compte Twitter de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4d90f-201">On the Twitter sign in page, sign in using the credentials for your organization’s Twitter account.</span></span>

   ![Se connecter à un compte Twitter](media/TCimage42.png)

   <span data-ttu-id="4d90f-203">Une fois que vous êtes connecté, la page Twitter affiche le message suivant : « travail de connecteur Twitter correctement configuré ».</span><span class="sxs-lookup"><span data-stu-id="4d90f-203">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

10. <span data-ttu-id="4d90f-204">Cliquez sur **Continuer** pour terminer la configuration du connecteur Twitter.</span><span class="sxs-lookup"><span data-stu-id="4d90f-204">Click **Continue** to complete setting up the Twitter connector.</span></span>

11. <span data-ttu-id="4d90f-205">Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer initialement les éléments qui sont un certain âge.</span><span class="sxs-lookup"><span data-stu-id="4d90f-205">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="4d90f-206">Sélectionnez un âge, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-206">Select an age, and then click **Next**.</span></span>

12. <span data-ttu-id="4d90f-207">Dans la page **choisir l’emplacement de stockage** , tapez l’adresse de messagerie de la boîte aux lettres Microsoft 365 dans laquelle les éléments Twitter seront importés, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4d90f-207">On the **Choose storage location** page, type the email address of Microsoft 365 mailbox that the Twitter items will be imported to, and then click **Next**.</span></span>

13. <span data-ttu-id="4d90f-208">Sur l' **autorisation fournir un administrateur**, cliquez sur **accorder le consentement** , puis suivez les étapes.</span><span class="sxs-lookup"><span data-stu-id="4d90f-208">On the **Provide admin consent**, click **Provide consent** and then follow the steps.</span></span> <span data-ttu-id="4d90f-209">Vous devez être un administrateur général pour accorder le consentement du service d’importation Office 365 pour accéder aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4d90f-209">You must be a global admin to provide consent for the Office 365 Import service to access data in your organization.</span></span>

14. <span data-ttu-id="4d90f-210">Cliquez sur **suivant** pour passer en revue les paramètres du connecteur, puis cliquez sur **Terminer** pour terminer l’installation du connecteur.</span><span class="sxs-lookup"><span data-stu-id="4d90f-210">Click **Next** to review the connector settings and then click **Finish** to complete the connector setup.</span></span>

15. <span data-ttu-id="4d90f-211">Dans le centre de conformité, accédez à la page **connecteurs de données** , puis cliquez sur l’onglet **connecteurs** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="4d90f-211">In the compliance center, go to the **Data connectors** page, and click the **Connectors** tab to see the progress of the import process.</span></span>
