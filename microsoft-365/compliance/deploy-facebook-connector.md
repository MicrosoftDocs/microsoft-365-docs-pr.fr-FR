---
title: Déployer un connecteur pour archiver des données Facebook dans Office 365
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
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des pages Facebook dans Office 365. Une fois ces données importées dans Office 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Facebook de votre organisation.
ms.openlocfilehash: 1f5b0f241616cc95e79e80d054a8782f97c5887b
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37070909"
---
# <a name="deploy-a-connector-to-archive-facebook-data-in-office-365"></a><span data-ttu-id="ca06b-104">Déployer un connecteur pour archiver des données Facebook dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ca06b-104">Deploy a connector to archive Facebook data in Office 365</span></span>

<span data-ttu-id="ca06b-105">Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir de pages d’entreprise Facebook vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="ca06b-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from Facebook Business pages to Office 365.</span></span> <span data-ttu-id="ca06b-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Facebook, voir [utiliser un exemple de connecteur pour archiver des données Facebook dans Office 365 (version d’évaluation)](archive-facebook-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="ca06b-106">For a high-level overview of this process and a list of prerequisites required to deploy a Facebook connector, see [Use a sample connector to archive Facebook data in Office 365 (Preview)](archive-facebook-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="ca06b-107">Étape 1 : Télécharger le package</span><span class="sxs-lookup"><span data-stu-id="ca06b-107">Step 1: Download the package</span></span>

<span data-ttu-id="ca06b-108">Téléchargez le package prédéfini à partir de la section Release dans le référentiel GitHub à l' <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>adresse.</span><span class="sxs-lookup"><span data-stu-id="ca06b-108">Download the prebuilt package from the Release section in the GitHub repository at <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>.</span></span> <span data-ttu-id="ca06b-109">Sous la dernière version, téléchargez le fichier zip nommé **SampleConnector. zip**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="ca06b-110">Vous téléchargez ce fichier zip vers Azure à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="ca06b-110">You upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="ca06b-111">Étape 2 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ca06b-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="ca06b-112">Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.</span><span class="sxs-lookup"><span data-stu-id="ca06b-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

    ![Créer une application dans AAD](media/FBCimage1.png)

2. <span data-ttu-id="ca06b-114">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-114">In the left navigation pane, click **Azure Active Directory**.</span></span>

    ![](media/FBCimage2.png)

3. <span data-ttu-id="ca06b-115">Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-115">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

    ![](media/FBCimage3.png)

4. <span data-ttu-id="ca06b-116">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="ca06b-116">Register the application.</span></span> <span data-ttu-id="ca06b-117">Sous URI de redirection, sélectionnez Web dans la liste déroulante type d' <https://portal.azure.com> application, puis tapez dans la zone de l’URI.</span><span class="sxs-lookup"><span data-stu-id="ca06b-117">Under Redirect URI, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/FBCimage4.png)

5. <span data-ttu-id="ca06b-118">Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="ca06b-118">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="ca06b-119">Vous utilisez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca06b-119">You use these IDs in later steps.</span></span>

   ![](media/FBCimage5.png)

6. <span data-ttu-id="ca06b-120">Accédez à **certificats & secrets de la nouvelle application.**</span><span class="sxs-lookup"><span data-stu-id="ca06b-120">Go to **Certificates & secrets for the new app.**</span></span>

   ![](media/FBCimage6.png)

7. <span data-ttu-id="ca06b-121">Cliquez sur **nouvelle clé secrète client**</span><span class="sxs-lookup"><span data-stu-id="ca06b-121">Click **New client secret**</span></span>

   ![](media/FBCimage7.png)

8. <span data-ttu-id="ca06b-122">Créer une nouvelle clé secrète.</span><span class="sxs-lookup"><span data-stu-id="ca06b-122">Create a new secret.</span></span> <span data-ttu-id="ca06b-123">Dans la zone Description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="ca06b-123">In the description box, type the secret and then choose an expiration period.</span></span> 

    ![](media/FBCimage8.png)

9. <span data-ttu-id="ca06b-124">Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-124">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="ca06b-125">Il s’agit de la clé secrète de l’application AAD que vous utilisez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca06b-125">This is the AAD application secret that you use in later steps.</span></span>

   ![](media/FBCimage9.png)

10. <span data-ttu-id="ca06b-126">Accédez au **manifeste** et copiez le identifierUris (également appelé URI de l’application AAD) en surbrillance dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="ca06b-126">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="ca06b-127">Copiez l’URI de l’application AAD dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-127">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="ca06b-128">Vous l’utilisez à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="ca06b-128">You use it in Step 6.</span></span>

   ![](media/FBCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="ca06b-129">Étape 3 : créer un compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="ca06b-129">Step 3: Create an Azure storage account</span></span>

1. <span data-ttu-id="ca06b-130">Accédez à la page d’accueil Azure de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ca06b-130">Go to the Azure home page for your organization.</span></span>

    ![](media/FBCimage11.png)

2. <span data-ttu-id="ca06b-131">Cliquez sur **créer une ressource** et tapez le **compte de stockage** dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="ca06b-131">Click **Create a resource** and they type **storage account** in the search box.</span></span>

    ![](media/FBCimage12.png)

3. <span data-ttu-id="ca06b-132">Cliquez sur **stockage**, puis sur **compte de stockage**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-132">Click **Storage**, and then click **Storage account**.</span></span>

    ![](media/FBCimage13.png)

4. <span data-ttu-id="ca06b-133">Sur la page **créer un compte de stockage** , dans la zone abonnement, sélectionnez **paiement en cours** ou **version d’évaluation gratuite** en fonction du type d’abonnement Azure dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="ca06b-133">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> <span data-ttu-id="ca06b-134">Ensuite, sélectionnez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="ca06b-134">Then select or create a resource group.</span></span>

    ![](media/FBCimage14.png)

5. <span data-ttu-id="ca06b-135">Tapez un nom pour le compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-135">Type a name for the storage account.</span></span>

    ![](media/FBCimage15.png)

6. <span data-ttu-id="ca06b-136">Passez en revue, puis cliquez sur **créer** pour créer le compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-136">Review and then click **Create** to create the storage account.</span></span>

    ![](media/FBCimage16.png)

7. <span data-ttu-id="ca06b-137">Après quelques instants, cliquez sur **Actualiser** , puis sur **accéder à la ressource** pour accéder au compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-137">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

    ![](media/FBCimage17.png)

8. <span data-ttu-id="ca06b-138">Cliquez sur **touches d’accès** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="ca06b-138">Click **Access keys** in the left navigation pane.</span></span>

    ![](media/FBCimage18.png)

9. <span data-ttu-id="ca06b-139">Copiez une **chaîne de connexion** et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-139">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="ca06b-140">Vous l’utilisez lors de la création d’une ressource d’application Web.</span><span class="sxs-lookup"><span data-stu-id="ca06b-140">You use this when creating a web app resource.</span></span>

    ![](media/FBCimage19.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="ca06b-141">Étape 4 : créer une nouvelle ressource d’application Web dans Azure</span><span class="sxs-lookup"><span data-stu-id="ca06b-141">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="ca06b-142">Sur la page d' **Accueil** du portail Azure, cliquez sur **créer une \> ressource \> tout le Web App**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-142">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="ca06b-143">Dans la page **application Web** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-143">On the **Web app** page, click **Create**.</span></span> 

   ![](media/FBCimage20.png)

2. <span data-ttu-id="ca06b-144">Renseignez les détails (comme indiqué ci-dessous), puis créez l’application Web.</span><span class="sxs-lookup"><span data-stu-id="ca06b-144">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="ca06b-145">Notez que le nom que vous entrez dans la zone nom de l' **application** est utilisé pour créer l’URL du service d’application Azure ; par exemple, fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca06b-145">Note that the name that you enter in the **App name** box is used to create the Azure app service URL; for example, fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage21.png)

3. <span data-ttu-id="ca06b-146">Accédez à la ressource d’application Web nouvellement créée, cliquez sur paramètres de l' **application** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="ca06b-146">Go to the newly created web app resource, click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="ca06b-147">Sous paramètres de l’application, cliquez sur Ajouter un nouveau paramètre et ajoutez les trois paramètres suivants : utilisez les valeurs (que vous avez copiées dans le fichier texte à partir des étapes précédentes) :</span><span class="sxs-lookup"><span data-stu-id="ca06b-147">Under Application settings, click Add new setting and add the following three settings: Use the values (that you copied to the text file from the previous steps):</span></span> 

    <span data-ttu-id="ca06b-148">– **APISecretKey** – vous pouvez taper n’importe quelle valeur comme clé secrète.</span><span class="sxs-lookup"><span data-stu-id="ca06b-148">– **APISecretKey** – You can type any value as the secret.</span></span> <span data-ttu-id="ca06b-149">Il est utilisé pour accéder à l’application Web de connecteur à l’étape 7.</span><span class="sxs-lookup"><span data-stu-id="ca06b-149">This is used to access the connector web app in Step 7.</span></span>

    <span data-ttu-id="ca06b-150">– \* \* StorageAccountConnectionString : URI de chaîne de connexion que vous avez copiée après avoir créé le compte de stockage Azure à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="ca06b-150">– \*\*StorageAccountConnectionString — The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    <span data-ttu-id="ca06b-151">– **tenantId** – ID de client de votre organisation Office 365 que vous avez copié après avoir créé l’application de connecteur Facebook dans Azure Active Directory à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="ca06b-151">– **tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Facebook connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/FBCimage22.png)

4. <span data-ttu-id="ca06b-152">Sous **paramètres généraux**, cliquez sur **en** regard de l’est **toujours activé**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-152">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="ca06b-153">Cliquez sur **Enregistrer** en haut de la page pour enregistrer les paramètres de l’application.</span><span class="sxs-lookup"><span data-stu-id="ca06b-153">Click **Save** at the top of the page to save application settings.</span></span>

   ![](media/FBCimage23.png)

5. <span data-ttu-id="ca06b-154">La dernière étape consiste à télécharger le code source de l’application du connecteur vers Azure que vous avez téléchargé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ca06b-154">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="ca06b-155">Dans un navigateur Web, accédez à https://<AzureAppResourceName>. SCM.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="ca06b-155">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="ca06b-156">Par exemple, si le nom de votre ressource d’application Azure (que vous avez nommée à l’étape 2 de cette section) est **fbconnector**, vous accédez https://fbconnector.scm.azurewebsites.net/ZipDeployUià.</span><span class="sxs-lookup"><span data-stu-id="ca06b-156">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **fbconnector**, then you would go to https://fbconnector.scm.azurewebsites.net/ZipDeployUi.</span></span> 

6. <span data-ttu-id="ca06b-157">Faites glisser et déposez le SampleConnector. zip (que vous avez téléchargé à l’étape 1) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="ca06b-157">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="ca06b-158">Une fois les fichiers téléchargés et le déploiement réussi, la capture d’écran suivante se présente :</span><span class="sxs-lookup"><span data-stu-id="ca06b-158">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot:</span></span>

   ![](media/FBCimage24.png)

## <a name="step-5-register-the-facebook-app"></a><span data-ttu-id="ca06b-159">Étape 5 : inscrire l’application Facebook</span><span class="sxs-lookup"><span data-stu-id="ca06b-159">Step 5: Register the Facebook app</span></span>

1. <span data-ttu-id="ca06b-160">Accédez à <https://developers.facebook.com>, connectez-vous à l’aide des informations d’identification du compte pour les pages d’entreprise Facebook de votre organisation, puis cliquez sur **Ajouter une nouvelle application**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-160">Go to <https://developers.facebook.com>, log in using the credentials for the account for your organization’s Facebook Business pages, and then click **Add New App**.</span></span>

   ![](media/FBCimage25.png)

2. <span data-ttu-id="ca06b-161">Créer un ID d’application.</span><span class="sxs-lookup"><span data-stu-id="ca06b-161">Create a new app ID.</span></span>

   ![](media/FBCimage26.png)

3. <span data-ttu-id="ca06b-162">Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis cliquez sur **configurer** dans la vignette de **connexion Facebook** .</span><span class="sxs-lookup"><span data-stu-id="ca06b-162">In the left navigation pane, click **Add Products** and then click **Set Up** in the **Facebook Login** tile.</span></span>

   ![](media/FBCimage27.png)

4. <span data-ttu-id="ca06b-163">Sur la page intégration de la connexion Facebook, cliquez sur **Web**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-163">On the Integrate Facebook Login page, click **Web**.</span></span>

   ![](media/FBCimage28.png)

5. <span data-ttu-id="ca06b-164">Ajoutez l’URL du service d’application Azure ; par exemple https://fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca06b-164">Add the Azure app service URL; for example https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage29.png)

6. <span data-ttu-id="ca06b-165">Complétez la section démarrage rapide de la configuration de connexion Facebook.</span><span class="sxs-lookup"><span data-stu-id="ca06b-165">Complete the QuickStart section of the Facebook Login setup.</span></span>

   ![](media/FBCimage30.png)

7. <span data-ttu-id="ca06b-166">Dans le volet de navigation de gauche sous **connexion Facebook**, cliquez sur **paramètres**, puis ajoutez l’URI de redirection OAuth dans la zone **URI de redirection OAuth valide** .</span><span class="sxs-lookup"><span data-stu-id="ca06b-166">In the left navigation pane under **Facebook Login**, click **Settings**, and add the OAuth redirect URI in the **Valid OAuth Redirect URIs** box.</span></span> <span data-ttu-id="ca06b-167">Utilisez le format \*\* \<connectorserviceuri>/views/facebookoauth\*\*, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation ; par exemple, https://fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca06b-167">Use the format **\<connectorserviceuri>/Views/FacebookOAuth**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example, https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage31.png)

8. <span data-ttu-id="ca06b-168">Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis sur **webhooks.**</span><span class="sxs-lookup"><span data-stu-id="ca06b-168">In the left navigation pane, click **Add Products** and then click **Webhooks.**</span></span> <span data-ttu-id="ca06b-169">Dans le menu déroulant **page** , cliquez sur **page**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-169">In the **Page** pull-down menu, click **Page**.</span></span> 

   ![](media/FBCimage32.png)

9. <span data-ttu-id="ca06b-170">Ajoutez l’URL de rappel des webhooks et ajoutez un jeton de vérification.</span><span class="sxs-lookup"><span data-stu-id="ca06b-170">Add Webhooks Callback URL and add a verify token.</span></span> <span data-ttu-id="ca06b-171">Le format de l’URL de rappel, utilisez le format \*\* <connectorserviceuri>/API/FbPageWebhook\*\*, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation ; par exemple https://fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca06b-171">The format of the callback URL, use the format **<connectorserviceuri>/api/FbPageWebhook**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example https://fbconnector.azurewebsites.net.</span></span> 

    <span data-ttu-id="ca06b-172">Le jeton Verify doit ressembler à un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="ca06b-172">The verify token should similar to a strong password.</span></span> <span data-ttu-id="ca06b-173">Copiez le jeton de vérification dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-173">Copy the verify token to a text file or other storage location.</span></span>

     ![](media/FBCimage33.png)

10. <span data-ttu-id="ca06b-174">Testez et abonnez-vous au point de terminaison pour le flux.</span><span class="sxs-lookup"><span data-stu-id="ca06b-174">Test and subscribe to the endpoint for feed.</span></span>

    ![](media/FBCimage34.png)

11. <span data-ttu-id="ca06b-175">Ajoutez une URL de confidentialité, une icône d’application et une utilisation professionnelle.</span><span class="sxs-lookup"><span data-stu-id="ca06b-175">Add a privacy URL, app icon, and business use.</span></span> <span data-ttu-id="ca06b-176">Copiez également l’ID de l’application et la clé secrète de l’application dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="ca06b-176">Also, copy the app ID and app secret to a text file or other storage location.</span></span>

    ![](media/FBCimage35.png)

12. <span data-ttu-id="ca06b-177">Rendez l’application publique.</span><span class="sxs-lookup"><span data-stu-id="ca06b-177">Make the app public.</span></span>

    ![](media/FBCimage36.png)

13. <span data-ttu-id="ca06b-178">Ajouter un utilisateur au rôle administrateur ou testeur.</span><span class="sxs-lookup"><span data-stu-id="ca06b-178">Add user to the admin or tester role.</span></span>

    ![](media/FBCimage37.png)

14. <span data-ttu-id="ca06b-179">Ajoutez l’autorisation d' **accès au contenu public** de la page.</span><span class="sxs-lookup"><span data-stu-id="ca06b-179">Add the **Page Public Content Access** permission.</span></span>

    ![](media/FBCimage38.png)

15. <span data-ttu-id="ca06b-180">Ajouter l’autorisation gérer les pages.</span><span class="sxs-lookup"><span data-stu-id="ca06b-180">Add Manage Pages permission.</span></span>

    ![](media/FBCimage39.png)

16. <span data-ttu-id="ca06b-181">Obtenir l’application examinée par Facebook.</span><span class="sxs-lookup"><span data-stu-id="ca06b-181">Get the application reviewed by Facebook.</span></span>

    ![](media/FBCimage40.png)

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="ca06b-182">Étape 6 : configuration de l’application Web de connecteur</span><span class="sxs-lookup"><span data-stu-id="ca06b-182">Step 6: Configure the connector web app</span></span>

1. <span data-ttu-id="ca06b-183">Accédez à https://\<AzureAppResourceName>. azurewebsites.net (où AzureAppResourceName est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4) par exemple, si le nom est **fbconnector**, accédez à https://fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca06b-183">Go to https://\<AzureAppResourceName>.azurewebsites.net (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4) For example, if the name is **fbconnector**, go to https://fbconnector.azurewebsites.net.</span></span> <span data-ttu-id="ca06b-184">La page d’accueil de l’application se présente comme la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="ca06b-184">The home page of the app will look like the following screenshot:</span></span>


   ![](media/FBCimage41.png)

2. <span data-ttu-id="ca06b-185">Cliquez sur **configurer** pour afficher une page de connexion.</span><span class="sxs-lookup"><span data-stu-id="ca06b-185">Click **Configure** to display a sign in page.</span></span>
 
   ![](media/FBCimage42.png)

3. <span data-ttu-id="ca06b-186">Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="ca06b-186">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="ca06b-187">Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la **configuration** .</span><span class="sxs-lookup"><span data-stu-id="ca06b-187">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

    ![](media/FBCimage43.png)


4. <span data-ttu-id="ca06b-188">Sous **Détails**de la configuration, entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="ca06b-188">Under **Configuration Details**, enter the following configuration settings</span></span> 

   <span data-ttu-id="ca06b-189">– **ID d’application Facebook** – ID d’application pour l’application Facebook que vous avez obtenue à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ca06b-189">– **Facebook application ID** – The app ID for the Facebook application that you obtained in Step 5.</span></span>
   <span data-ttu-id="ca06b-190">– **Clé d’application Facebook** : clé secrète de l’application Facebook que vous avez obtenue à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ca06b-190">– **Facebook application secret** – The app secret for the Facebook application that you obtained in Step 5.</span></span>
   <span data-ttu-id="ca06b-191">– **Facebook webhooks Verify** : le jeton de vérification que vous avez créé à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ca06b-191">– **Facebook webhooks verify token** – The verify token that you created in Step 5.</span></span>
   <span data-ttu-id="ca06b-192">– **ID d’application AAD** – ID d’application pour l’application Azure Active Directory que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="ca06b-192">– **AAD application ID** – The application ID for the Azure Active Directory app that you created in Step 2.</span></span>
   <span data-ttu-id="ca06b-193">– **Clé secrète de l’application AAD** – valeur de la clé secrète APISecretKey que vous avez créée à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="ca06b-193">– **AAD application secret** – The value for the APISecretKey secret that you created in Step 4.</span></span>
   <span data-ttu-id="ca06b-194">– **URI de l’application AAD** – URI de l’application AAD obtenue à l’étape 2 ; par exemple, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span><span class="sxs-lookup"><span data-stu-id="ca06b-194">– **AAD application Uri** – The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   <span data-ttu-id="ca06b-195">– **Clé d’instrumentation Insights** de l’application : laissez cette zone vide.</span><span class="sxs-lookup"><span data-stu-id="ca06b-195">– **App insights instrumentation key** – Leave this box blank.</span></span>

5. <span data-ttu-id="ca06b-196">Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="ca06b-196">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a><span data-ttu-id="ca06b-197">Étape 7 : configurer un connecteur personnalisé dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="ca06b-197">Step 7: Set up a custom connector in the Security & Compliance Center</span></span>

1. <span data-ttu-id="ca06b-198">Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données \> importer des données**tierces.</span><span class="sxs-lookup"><span data-stu-id="ca06b-198">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

   ![](media/FBCimage44.png)

2.  <span data-ttu-id="ca06b-199">Cliquez sur **Ajouter un connecteur** , puis sur **pages Facebook**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-199">Click **Add a connector** and then click **Facebook pages**.</span></span>

    ![](media/FBCimage46.png)

3.  <span data-ttu-id="ca06b-200">Dans la page **Ajouter une application connecteur** , entrez les informations suivantes, puis cliquez sur **valider le connecteur**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-200">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    <span data-ttu-id="ca06b-201">– Dans la première zone, tapez un nom pour le connecteur, tel que **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-201">– In the first box, type a name for the connector, such as **Facebook**.</span></span>
    <span data-ttu-id="ca06b-202">– Dans la deuxième zone, tapez ou collez la valeur du APISecretKey que vous avez ajouté à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="ca06b-202">– In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    <span data-ttu-id="ca06b-203">– Dans la troisième zone, tapez ou collez l’URL du service d’application Azure ; par exemple **https://fbconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-203">– In the third box, type or paste the Azure app service URL; for example **https://fbconnector.azurewebsites.net**.</span></span>
 
    <span data-ttu-id="ca06b-204">Une fois le connecteur validé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-204">After the connector is successfully validated, click **Next**.</span></span>
    
    ![](media/FBCimage47.png)

4.  <span data-ttu-id="ca06b-205">Cliquez sur **connexion avec application connecteur**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-205">Click **Login with Connector App**.</span></span>

    ![](media/FBCimage45.png)

5. <span data-ttu-id="ca06b-206">Tapez ou collez à nouveau le APISecretKey, puis cliquez sur **connexion au service connecteur**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-206">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/FBCimage48.png)


6. <span data-ttu-id="ca06b-207">Cliquez sur **connexion avec Facebook.**</span><span class="sxs-lookup"><span data-stu-id="ca06b-207">Click **Login with Facebook.**</span></span>

   ![](media/FBCimage49.png)

7. <span data-ttu-id="ca06b-208">Sur la page **se connecter à Facebook** , connectez-vous à l’aide des informations d’identification du compte pour les pages de l’entreprise Facebook de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ca06b-208">On the **Log in to Facebook** page, log in using the credentials for the account for your organization’s Facebook Business pages.</span></span> <span data-ttu-id="ca06b-209">Assurez-vous que le compte Facebook auquel vous êtes connecté se voit attribuer le rôle d’administrateur pour les pages d’entreprise Facebook de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ca06b-209">Make sure the Facebook account that you logged in to is assigned the admin role for your organization’s Facebook Business pages</span></span>

   ![](media/FBCimage50.png)

8. <span data-ttu-id="ca06b-210">Cliquez sur **Sélectionner les pages** pour choisir les pages professionnelles de votre organisation que vous souhaitez archiver dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="ca06b-210">Click **Select Pages** to choose your organization’s business pages that you want to archive in Office 365.</span></span>

   ![](media/FBCimage51.png)

9. <span data-ttu-id="ca06b-211">Une liste des pages d’entreprise gérées par le compte Facebook auquel vous vous êtes connecté s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ca06b-211">A list of the Business pages managed by the Facebook account that you logged in to is displayed.</span></span> <span data-ttu-id="ca06b-212">Sélectionnez la page à archiver, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-212">Select the page to archive and then click **Save**.</span></span>

    ![](media/FBCimage52.png)

10. <span data-ttu-id="ca06b-213">Cliquez sur **préparer** pour quitter le programme d’installation de l’application de service connecteur.</span><span class="sxs-lookup"><span data-stu-id="ca06b-213">Click **prepare** to exit the setup of the connector service app.</span></span>

    ![](media/FBCimage53.png)

11. <span data-ttu-id="ca06b-214">Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer (et archiver) les éléments qui sont un certain âge.</span><span class="sxs-lookup"><span data-stu-id="ca06b-214">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="ca06b-215">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ca06b-215">Click **Next**.</span></span>

    ![](media/FBCimage54.png)

12. <span data-ttu-id="ca06b-216">Sur la page **définir le compte de stockage** , sélectionnez la boîte aux lettres Office 365 dans laquelle les éléments des pages Facebook de l’entreprise que vous avez sélectionnées seront importés.</span><span class="sxs-lookup"><span data-stu-id="ca06b-216">On the **Set Storage Account** page, select the Office 365 mailbox that the items from the Facebook Business pages that you previously selected will be imported to.</span></span>

    ![](media/FBCimage55.png)

13. <span data-ttu-id="ca06b-217">Vérifiez vos paramètres, puis cliquez sur **Terminer** pour terminer l’installation du connecteur dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="ca06b-217">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/FBCimage56.png)

14. <span data-ttu-id="ca06b-218">Accédez à la page données tierces d' **archivage** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="ca06b-218">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/FBCimage58.png)
