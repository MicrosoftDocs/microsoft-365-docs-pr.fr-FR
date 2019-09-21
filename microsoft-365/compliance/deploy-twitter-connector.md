---
title: Déploiement d’un connecteur pour l’archivage des données Twitter dans Office 365
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
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des données Twitter vers Office 365. Une fois ces données importées dans Office 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Twitter de votre organisation.
ms.openlocfilehash: c3c5af0fc42057d9fc2e8b8e67423398d6ed0ddf
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37070274"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a><span data-ttu-id="1a57f-104">Déploiement d’un connecteur pour l’archivage des données Twitter dans Office 365</span><span class="sxs-lookup"><span data-stu-id="1a57f-104">Deploy a connector to archive Twitter data in Office 365</span></span>

<span data-ttu-id="1a57f-105">Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir du compte Twitter de votre organisation vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="1a57f-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Office 365.</span></span> <span data-ttu-id="1a57f-106">Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Twitter, reportez-vous à la rubrique [utiliser un exemple de connecteur pour archiver des données Twitter dans Office 365 (version d’évaluation)](archive-twitter-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="1a57f-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Use a sample connector to archive Twitter data in Office 365 (Preview)](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="1a57f-107">Étape 1 : Télécharger le package</span><span class="sxs-lookup"><span data-stu-id="1a57f-107">Step 1: Download the package</span></span>

<span data-ttu-id="1a57f-108">Téléchargez le package prédéfini à partir de la section Release dans le référentiel GitHub à l' [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)adresse.</span><span class="sxs-lookup"><span data-stu-id="1a57f-108">Download the prebuilt package from the Release section in the GitHub repository at [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span></span> <span data-ttu-id="1a57f-109">Sous la dernière version, téléchargez le fichier zip nommé **SampleConnector. zip**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="1a57f-110">Vous téléchargez ce fichier zip vers Azure à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="1a57f-110">You upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="1a57f-111">Étape 2 : créer une application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a57f-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="1a57f-112">Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.</span><span class="sxs-lookup"><span data-stu-id="1a57f-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

   ![](media/TCimage01.png)

2. <span data-ttu-id="1a57f-113">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-113">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![](media/TCimage02.png)

3. <span data-ttu-id="1a57f-114">Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-114">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![](media/TCimage03.png)

4. <span data-ttu-id="1a57f-115">Inscrivez l’application.</span><span class="sxs-lookup"><span data-stu-id="1a57f-115">Register the application.</span></span> <span data-ttu-id="1a57f-116">Sous **URI de redirection (facultatif)**, sélectionnez Web dans la liste déroulante type d' <https://portal.azure.com> application, puis tapez dans la zone de l’URI.</span><span class="sxs-lookup"><span data-stu-id="1a57f-116">Under **Redirect URI (optional)**, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/TCimage04.png)

5. <span data-ttu-id="1a57f-117">Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr.</span><span class="sxs-lookup"><span data-stu-id="1a57f-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="1a57f-118">Vous utilisez ces ID dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1a57f-118">You use these IDs in later steps.</span></span>

    ![](media/TCimage05.png)

6. <span data-ttu-id="1a57f-119">Accédez à **certificats & secrets de la nouvelle application** , puis sous **secrets client** , cliquez sur **nouvelle clé secrète client**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-119">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![](media/TCimage06.png)

7. <span data-ttu-id="1a57f-120">Créer une nouvelle clé secrète.</span><span class="sxs-lookup"><span data-stu-id="1a57f-120">Create a new secret.</span></span> <span data-ttu-id="1a57f-121">Dans la zone Description, tapez le secret, puis choisissez une période d’expiration.</span><span class="sxs-lookup"><span data-stu-id="1a57f-121">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![](media/TCimage08.png)

8. <span data-ttu-id="1a57f-122">Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-122">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="1a57f-123">Il s’agit de la clé secrète de l’application AAD que vous utilisez dans les étapes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1a57f-123">This is the AAD application secret that you use in later steps.</span></span>

   ![](media/TCimage09.png)

9. <span data-ttu-id="1a57f-124">Accédez au **manifeste** et copiez le identifierUris (également appelé URI de l’application AAD) en surbrillance dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="1a57f-124">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="1a57f-125">Copiez l’URI de l’application AAD dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-125">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="1a57f-126">Vous l’utilisez à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="1a57f-126">You use it in Step 6.</span></span>

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="1a57f-127">Étape 3 : créer un compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="1a57f-127">Step 3: Create an Azure storage account</span></span>

1.  <span data-ttu-id="1a57f-128">Accédez à la page d’accueil Azure de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a57f-128">Go to the Azure home page for your organization.</span></span>

    ![](media/TCimage11.png)

2. <span data-ttu-id="1a57f-129">Cliquez sur **créer une ressource** et tapez le **compte de stockage** dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="1a57f-129">Click **Create a resource** and they type **storage account** in the search box.</span></span>

   ![](media/TCimage12.png)

3. <span data-ttu-id="1a57f-130">Cliquez sur **stockage**, puis sur **compte de stockage**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-130">Click **Storage**, and then click **Storage account**.</span></span>

   ![](media/TCimage13.png)

4. <span data-ttu-id="1a57f-131">Sur la page **créer un compte de stockage** , dans la zone abonnement, sélectionnez **paiement en cours** ou **version d’évaluation gratuite** en fonction du type d’abonnement Azure dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="1a57f-131">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> 

   ![](media/TCimage14.png)

5. <span data-ttu-id="1a57f-132">Sélectionnez ou créez un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="1a57f-132">Select or create a resource group.</span></span>

   ![](media/TCimage15.png)

6. <span data-ttu-id="1a57f-133">Tapez un nom pour le compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-133">Type a name for the storage account.</span></span>

   ![](media/TCimage16.png)

7. <span data-ttu-id="1a57f-134">Passez en revue, puis cliquez sur **créer** pour créer le compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-134">Review and then click **Create** to create the storage account.</span></span>

   ![](media/TCimage17.png)

8. <span data-ttu-id="1a57f-135">Après quelques instants, cliquez sur **Actualiser** , puis sur **accéder à la ressource** pour accéder au compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-135">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

   ![](media/TCimage18.png)

9. <span data-ttu-id="1a57f-136">Cliquez sur **touches d’accès** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="1a57f-136">Click **Access keys** in the left navigation pane.</span></span>

   ![](media/TCimage19.png)

10. <span data-ttu-id="1a57f-137">Copiez une **chaîne de connexion** et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-137">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="1a57f-138">Vous pouvez l’utiliser lors de la création d’une ressource d’application Web à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="1a57f-138">You use this when creating a web app resource in Step 4.</span></span>

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="1a57f-139">Étape 4 : créer une nouvelle ressource d’application Web dans Azure</span><span class="sxs-lookup"><span data-stu-id="1a57f-139">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="1a57f-140">Sur la page d' **Accueil** du portail Azure, cliquez sur **créer une \> ressource \> tout le Web App**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-140">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="1a57f-141">Dans la page **application Web** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-141">On the **Web app** page, click **Create**.</span></span>

   ![](media/TCimage21.png)

2. <span data-ttu-id="1a57f-142">Renseignez les détails (comme indiqué ci-dessous), puis créez l’application Web.</span><span class="sxs-lookup"><span data-stu-id="1a57f-142">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="1a57f-143">Le nom que vous entrez dans la zone nom de l' **application** est utilisé pour créer l’URL du service d’application Azure ; par exemple, twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="1a57f-143">The name that you enter in the **App name** box is used to create the Azure app service URL; for example, twitterconnector.azurewebsites.net.</span></span>

   ![](media/TCimage22.png)

3. <span data-ttu-id="1a57f-144">Accédez à la ressource d’application Web nouvellement créée, puis cliquez sur paramètres de l' **application** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="1a57f-144">Go to the newly created web app resource and click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="1a57f-145">Sous **paramètres**de l’application, cliquez sur **Ajouter un nouveau paramètre** , puis ajoutez les trois paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1a57f-145">Under **Application settings**, click **Add new setting** and add the following three settings.</span></span> <span data-ttu-id="1a57f-146">Utilisez les valeurs (que vous avez copiées dans le fichier texte à partir des étapes précédentes) :</span><span class="sxs-lookup"><span data-stu-id="1a57f-146">Use the values (that you copied to the text file from the previous steps):</span></span> 

    <span data-ttu-id="1a57f-147">– \* \* APISecretKey — vous pouvez taper n’importe quelle valeur en tant que clé secrète.</span><span class="sxs-lookup"><span data-stu-id="1a57f-147">– \*\*APISecretKey — You can type any value as the secret.</span></span> <span data-ttu-id="1a57f-148">Il est utilisé pour accéder à l’application Web de connecteur à l’étape 7.</span><span class="sxs-lookup"><span data-stu-id="1a57f-148">This is used to access the connector web app in Step 7.</span></span>

    <span data-ttu-id="1a57f-149">– **StorageAccountConnectionString** – URI de chaîne de connexion que vous avez copiée après avoir créé le compte de stockage Azure à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1a57f-149">– **StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    <span data-ttu-id="1a57f-150">– **tenantId** – ID de client de votre organisation Office 365 que vous avez copié après avoir créé l’application connecteur Twitter dans Azure Active Directory à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1a57f-150">– **tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Twitter connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/TCimage23.png)

4. <span data-ttu-id="1a57f-151">Sous **paramètres généraux**, cliquez sur **en** regard de l’est **toujours activé**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-151">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="1a57f-152">Cliquez sur **Enregistrer** en haut de la page pour enregistrer les paramètres de l’application.</span><span class="sxs-lookup"><span data-stu-id="1a57f-152">Click **Save** at the top of the page to save the application settings.</span></span>

   ![](media/TCimage24.png)

5. <span data-ttu-id="1a57f-153">La dernière étape consiste à télécharger le code source de l’application du connecteur vers Azure que vous avez téléchargé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="1a57f-153">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="1a57f-154">Dans un navigateur Web, accédez à https://<AzureAppResourceName>. SCM.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="1a57f-154">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="1a57f-155">Par exemple, si le nom de votre ressource d’application Azure (que vous avez nommée à l’étape 2 de cette section) est **twitterconnector**, vous accédez https://twitterconnector.scm.azurewebsites.net/ZipDeployUià.</span><span class="sxs-lookup"><span data-stu-id="1a57f-155">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **twitterconnector**, then you would go to https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span></span>

6. <span data-ttu-id="1a57f-156">Faites glisser et déposez le SampleConnector. zip (que vous avez téléchargé à l’étape 1) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="1a57f-156">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="1a57f-157">Une fois les fichiers téléchargés et le déploiement réussi, la capture d’écran suivante se présente :</span><span class="sxs-lookup"><span data-stu-id="1a57f-157">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot:</span></span>

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a><span data-ttu-id="1a57f-158">Étape 5 : créer l’application Twitter</span><span class="sxs-lookup"><span data-stu-id="1a57f-158">Step 5: Create the Twitter app</span></span>

1. <span data-ttu-id="1a57f-159">Accédez à https://developer.twitter.com, connectez-vous à l’aide des informations d’identification pour le compte de développeur de votre organisation, puis cliquez sur **applications**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-159">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![TCimage25-5. png](media/TCimage25-5.png)
2. <span data-ttu-id="1a57f-161">Cliquez sur **créer une application**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-161">Click **Create an app**.</span></span>
   
   ![](media/TCimage26.png)

3. <span data-ttu-id="1a57f-162">Sous **Détails**de l’application, ajoutez des informations sur l’application.</span><span class="sxs-lookup"><span data-stu-id="1a57f-162">Under **App details**, add information about the application.</span></span>

   ![](media/TCimage27.png)

4. <span data-ttu-id="1a57f-163">Dans le tableau de bord du développeur Twitter, sélectionnez l’application que vous venez de créer et copiez l’ID d’application affiché et enregistrez-le dans un fichier texte ou dans un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-163">On the Twitter developer dashboard, select the app that you just created and copy the App ID that's displayed  and save it to a text file or other storage location.</span></span> <span data-ttu-id="1a57f-164">Ensuite, cliquez sur **Détails**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-164">Then click **Details**.</span></span>
   
   ![](media/TCimage28.png)

5. <span data-ttu-id="1a57f-165">Sous l’onglet **clés et jetons** , sous clés de l' **API consommateur** , copiez la clé secrète de l’API et enregistrez-la dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-165">On the **Keys and tokens** tab, under **Consumer API keys** copy the API secret key and save it to a text file or other storage location.</span></span> <span data-ttu-id="1a57f-166">Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-166">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>
   
   ![](media/TCimage29.png)

   <span data-ttu-id="1a57f-167">Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="1a57f-167">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="1a57f-168">Cliquez sur l’onglet **autorisations** et configurez les autorisations comme indiqué dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="1a57f-168">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![](media/TCimage30.png)

7. <span data-ttu-id="1a57f-169">Une fois que vous avez enregistré les paramètres d’autorisation, cliquez sur l’onglet Détails de l' **application** , puis cliquez sur **modifier > modifier les détails**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-169">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![](media/TCimage31.png)

8. <span data-ttu-id="1a57f-170">Effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a57f-170">Do the following tasks:</span></span>

   <span data-ttu-id="1a57f-171">: Activez cette case à cocher pour autoriser l’application de connecteur à se connecter à Twitter.</span><span class="sxs-lookup"><span data-stu-id="1a57f-171">– Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   <span data-ttu-id="1a57f-172">: Ajoutez l’URI de redirection OAuth en utilisant le format suivant : \*\* \<connectorserviceuri>/views/twitteroauth\*\*, où la valeur de *connectorserviceuri* est l’URL de service d’application Azure pour votre organisation ; par exemple, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span><span class="sxs-lookup"><span data-stu-id="1a57f-172">– Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

   ![](media/TCimage32.png)

<span data-ttu-id="1a57f-173">L’application de développeur Twitter est maintenant prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1a57f-173">The Twitter developer app is now ready to use.</span></span>

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="1a57f-174">Étape 6 : configuration de l’application Web de connecteur</span><span class="sxs-lookup"><span data-stu-id="1a57f-174">Step 6: Configure the connector web app</span></span> 

1. <span data-ttu-id="1a57f-175">Accédez à https://\<AzureAppResourceName>. azurewebsites.net (où **AzureAppResourceName** est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4).</span><span class="sxs-lookup"><span data-stu-id="1a57f-175">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4).</span></span> <span data-ttu-id="1a57f-176">Par exemple, si le nom est **twitterconnector**, accédez à https://twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="1a57f-176">For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="1a57f-177">La page d’accueil de l’application se présente comme la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="1a57f-177">The home page of the app looks like the following screenshot:</span></span>

   ![](media/FBCimage41.png)

2. <span data-ttu-id="1a57f-178">Cliquez sur **configurer** pour afficher une page de connexion.</span><span class="sxs-lookup"><span data-stu-id="1a57f-178">Click **Configure** to display a sign in page.</span></span>

   ![](media/FBCimage42.png)

3. <span data-ttu-id="1a57f-179">Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="1a57f-179">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="1a57f-180">Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la **configuration** .</span><span class="sxs-lookup"><span data-stu-id="1a57f-180">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

   ![](media/TCimage35.png)

4. <span data-ttu-id="1a57f-181">Sous **Détails**de la configuration, entrez les paramètres de configuration suivants</span><span class="sxs-lookup"><span data-stu-id="1a57f-181">Under **Configuration Details**, enter the following configuration settings</span></span> 

   <span data-ttu-id="1a57f-182">– **Clé de l’API Twitter** – ID de l’application Twitter que vous avez créée à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="1a57f-182">– **Twitter Api Key** – The app ID for the Twitter application that you created in Step 5.</span></span>
   <span data-ttu-id="1a57f-183">– **Clé secrète de l’API Twitter** : clé secrète de l’API pour l’application Twitter que vous avez créée à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="1a57f-183">– **Twitter Api Secret Key** – The API secret key for the Twitter application that you created in Step 5.</span></span>
   <span data-ttu-id="1a57f-184">– **Jeton d’accès Twitter** – le jeton d’accès que vous avez créé à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="1a57f-184">– **Twitter Access Token** – The access token that you created in Step 5.</span></span>
   <span data-ttu-id="1a57f-185">– **Jeton d’accès Twitter-secret** de jeton d’accès que vous avez créé à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="1a57f-185">– **Twitter Access Token Secret** – The access token secret that you created in Step 5.</span></span>
   <span data-ttu-id="1a57f-186">– **ID de l’application AAD** – ID de l’application Azure Active Directory que vous avez créée à l’étape 2 – **clé secrète de l’application AAD** – valeur de la clé secrète APISecretKey que vous avez créée à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="1a57f-186">– **AAD Application ID** – The application ID for the Azure Active Directory app that you created in Step 2 – **AAD Application Secret** – The value for the APISecretKey secret that you created in Step 4.</span></span>
   <span data-ttu-id="1a57f-187">– **URI de l’application AAD** – URI de l’application AAD obtenue à l’étape 2 ; par exemple, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span><span class="sxs-lookup"><span data-stu-id="1a57f-187">– **AAD Application Uri** – The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   <span data-ttu-id="1a57f-188">– **Clé d’instrumentation Insights** de l’application : laissez cette zone vide.</span><span class="sxs-lookup"><span data-stu-id="1a57f-188">– **App Insights Instrumentation Key** – Leave this box blank.</span></span>

5. <span data-ttu-id="1a57f-189">Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.</span><span class="sxs-lookup"><span data-stu-id="1a57f-189">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a><span data-ttu-id="1a57f-190">Étape 7 : configurer un connecteur personnalisé dans le centre de sécurité et de conformité</span><span class="sxs-lookup"><span data-stu-id="1a57f-190">Step 7: Set up a custom connector in the security and compliance center</span></span>

1.  <span data-ttu-id="1a57f-191">Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données \> importer des données**tierces.</span><span class="sxs-lookup"><span data-stu-id="1a57f-191">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

    ![](media/TCimage36.png)

2. <span data-ttu-id="1a57f-192">Cliquez sur **Ajouter un connecteur** , puis sur **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-192">Click **Add a connector** and then click **Twitter**.</span></span>

   ![](media/TCimage37.png)

3. <span data-ttu-id="1a57f-193">Dans la page **Ajouter une application connecteur** , entrez les informations suivantes, puis cliquez sur **valider le connecteur**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-193">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    <span data-ttu-id="1a57f-194">– Dans la première zone, tapez un nom pour le connecteur, tel que **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-194">– In the first box, type a name for the connector, such as **Twitter**.</span></span>
    <span data-ttu-id="1a57f-195">– Dans la deuxième zone, tapez ou collez la valeur du APISecretKey que vous avez ajouté à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="1a57f-195">– In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    <span data-ttu-id="1a57f-196">– Dans la troisième zone, tapez ou collez l’URL du service d’application Azure ; par exemple, **https://twitterconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-196">– In the third box, type or paste the Azure app service URL; for example, **https://twitterconnector.azurewebsites.net**.</span></span>

   <span data-ttu-id="1a57f-197">Une fois le connecteur validé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-197">After the connector is successfully validated, click **Next**.</span></span>

   ![](media/TCimage38.png)

4. <span data-ttu-id="1a57f-198">Cliquez sur **connexion avec application connecteur**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-198">Click **Login with Connector App**.</span></span>

   ![](media/TCimage39.png)

5. <span data-ttu-id="1a57f-199">Tapez ou collez à nouveau le APISecretKey, puis cliquez sur **connexion au service connecteur**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-199">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/TCimage40.png)


6. <span data-ttu-id="1a57f-200">Cliquez sur **continuer avec Twitter**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-200">Click **Continue with Twitter**.</span></span>

7. <span data-ttu-id="1a57f-201">Sur la page de connexion Twitter, connectez-vous à l’aide des informations d’identification du compte pour le compte Twitter de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a57f-201">On the Twitter sign in page, sign in using the credentials for the account for your organization’s Twitter account.</span></span>

   ![](media/TCimage42.png)

   <span data-ttu-id="1a57f-202">Une fois que vous êtes connecté, la page Twitter affiche le message suivant : « travail de connecteur Twitter correctement configuré ».</span><span class="sxs-lookup"><span data-stu-id="1a57f-202">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

8. <span data-ttu-id="1a57f-203">Cliquez sur **Terminer** pour terminer la configuration du connecteur Twitter.</span><span class="sxs-lookup"><span data-stu-id="1a57f-203">Click **Finish** to complete setting up the Twitter connector.</span></span>

9. <span data-ttu-id="1a57f-204">Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer (et archiver) les éléments qui sont un certain âge.</span><span class="sxs-lookup"><span data-stu-id="1a57f-204">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="1a57f-205">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1a57f-205">Click **Next**.</span></span>

   ![](media/TCimage44.png)

10. <span data-ttu-id="1a57f-206">Sur la page **définir le compte de stockage** , tapez l’adresse de messagerie d’une boîte aux lettres Office 365 dans laquelle les éléments Twitter seront importés.</span><span class="sxs-lookup"><span data-stu-id="1a57f-206">On the **Set Storage Account** page, type the email address of an Office 365 mailbox that the Twitter items will be imported to.</span></span>

    ![](media/TCimage45.png)

11. <span data-ttu-id="1a57f-207">Vérifiez vos paramètres, puis cliquez sur **Terminer** pour terminer l’installation du connecteur dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="1a57f-207">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. <span data-ttu-id="1a57f-208">Accédez à la page données tierces d' **archivage** pour voir la progression du processus d’importation.</span><span class="sxs-lookup"><span data-stu-id="1a57f-208">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/TCimage48.png)
