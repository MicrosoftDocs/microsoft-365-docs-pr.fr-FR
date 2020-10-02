---
title: Configurer SharePoint Online
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: MET150
localization_priority: Priority
description: Configurer la compréhension de contenu dans Projet Cortex
ms.openlocfilehash: 7fb5998729c9f11902f8fdfaffa62b160928077c
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321348"
---
# <a name="set-up-sharepoint-syntex"></a><span data-ttu-id="cf325-103">Configurer SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="cf325-103">Set up SharePoint Syntex</span></span>

<span data-ttu-id="cf325-104">Les administrateurs peuvent utiliser le Centre d’administration Microsoft 365 pour configurer [Microsoft SharePoint Syntex](document-understanding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cf325-104">Admins can use the Microsoft 365 admin center to set up [Microsoft SharePoint Syntex](document-understanding-overview.md).</span></span> 

<span data-ttu-id="cf325-105">Tenez compte des informations suivantes avant de démarrer :</span><span class="sxs-lookup"><span data-stu-id="cf325-105">Consider the following before you start:</span></span>

- <span data-ttu-id="cf325-106">Pour quels sites SharePoint allez-vous activer le traitement des formulaires ?</span><span class="sxs-lookup"><span data-stu-id="cf325-106">Which SharePoint sites will you enable form processing?</span></span> <span data-ttu-id="cf325-107">Tous les sites, certains sites ou des sites sélectionnés ?</span><span class="sxs-lookup"><span data-stu-id="cf325-107">All of them, some, or select sites?</span></span>
- <span data-ttu-id="cf325-108">Comment allez-vous nommer votre centre de contenu par défaut ?</span><span class="sxs-lookup"><span data-stu-id="cf325-108">What will you name of your default content center?</span></span>

<span data-ttu-id="cf325-109">Vous pouvez modifier vos paramètres après la configuration initiale dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf325-109">You can change your settings after initial setup in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="cf325-110">Le contenu de cet article est destiné à la préversion privée du Projet Cortex.</span><span class="sxs-lookup"><span data-stu-id="cf325-110">The content in this article is for the Project Cortex Private Preview.</span></span> <span data-ttu-id="cf325-111">[En savoir plus sur le Projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="cf325-111">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="cf325-112">Avant la configuration, veillez à planifier la meilleure manière d’installer et de configurer la compréhension de contenu dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="cf325-112">Prior to setup, make sure to plan for the best way to set up and configure content understanding in your environment.</span></span> <span data-ttu-id="cf325-113">Par exemple, vous devez prendre en compte les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="cf325-113">For example, you need to make considerations about the following names of:</span></span>

- <span data-ttu-id="cf325-114">Sites SharePoint pour lesquels vous souhaitez activer le traitement des formulaires : tous les sites, certains sites ou des sites sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cf325-114">The SharePoint sites that you want to enable form processing - all of them, some, or selected sites</span></span>
- <span data-ttu-id="cf325-115">Votre centre de contenu et le nom de l’administrateur de site principal</span><span class="sxs-lookup"><span data-stu-id="cf325-115">Your content center and the name of the primary site admin</span></span>

## <a name="requirements"></a><span data-ttu-id="cf325-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf325-116">Requirements</span></span> 

> [!NOTE]
> <span data-ttu-id="cf325-117">Pour accéder au Centre d’administration Microsoft 365 et configurer la compréhension de contenu, vous devez disposer des autorisations d’administrateur général ou d’administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cf325-117">You must have Global admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up content understanding.</span></span>

<span data-ttu-id="cf325-118">En tant qu’administrateur, vous pouvez également modifier vos paramètres sélectionnés à tout moment après la configuration, ainsi que les paramètres de gestion de la compréhension de contenu dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf325-118">As an admin, you can also make changes to your selected settings anytime after setup, and throughout the content understanding management settings in the Microsoft 365 Admin Center.</span></span>

## <a name="to-set-up-sharepoint-syntex"></a><span data-ttu-id="cf325-119">Pour configurer SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="cf325-119">To set up SharePoint Syntex</span></span>

1. <span data-ttu-id="cf325-120">Dans le Centre d’administration Microsoft 365, sélectionnez **Configuration**, puis affichez la section **Connaissances organisationnelles**.</span><span class="sxs-lookup"><span data-stu-id="cf325-120">In the Microsoft 365 admin center, select **Setup**, and then view the **Organizational knowledge** section.</span></span>

2. <span data-ttu-id="cf325-121">Dans la section **Connaissances organisationnelles**, sélectionnez **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="cf325-121">In the **Organizational knowledge** section, select **Automate content understanding**.</span></span><br/>

    ![Page de configuration des connaissances organisationnelles](../media/content-understanding/admin-org-knowledge-options.png)</br>

3. <span data-ttu-id="cf325-123">À la page **Automatiser la compréhension de contenu** , cliquez sur **Commencer** pour parcourir le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="cf325-123">On the **Automate content understanding** page, click **Get started** to walk through the setup process.</span></span><br/>

    ![Commencer la configuration](../media/content-understanding/admin-content-understanding-get-started.png)</br>

4. <span data-ttu-id="cf325-125">Dans la page Activer le balisage d’image, choisissez d’autoriser ou non le [balisage d’image](image-tagging.md).</span><span class="sxs-lookup"><span data-stu-id="cf325-125">On the Turn on image tagging page, choose if you want to allow [image tagging](image-tagging.md).</span></span>

    ![Capture d’écran des options de balisage d’image](../media/content-understanding/admin-content-understanding-setup-image-tagging.png)</br>

5. <span data-ttu-id="cf325-127">Sur la page **Configurer le traitement des formulaires**, vous pouvez choisir d’autoriser ou non les utilisateurs à créer des modèles de traitement de formulaire dans des bibliothèques de documents SharePoint spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cf325-127">On the **Configure Form Processing** page, you can choose if you want to let users be able to create form processing models in specific SharePoint document libraries.</span></span> <span data-ttu-id="cf325-128">Une option de menu **Créer un modèle de traitement de formulaire** sera disponible dans les rubans des bibliothèques de documents SharePoint où le traitement des formulaires est activé.</span><span class="sxs-lookup"><span data-stu-id="cf325-128">A menu option will be available in the document library ribbon to **Create a form processing model** in SharePoint document libraries in which it is enabled.</span></span>
 
     <span data-ttu-id="cf325-129">Concernant les **bibliothèques SharePoint qui doivent afficher l’option de création d’un modèle de traitement de formulaire**, vous pouvez sélectionner les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="cf325-129">For **Which SharePoint libraries should show option to create a form processing model**, you can select:</span></span></br>
      - <span data-ttu-id="cf325-130">**Toutes les bibliothèques SharePoint** pour rendre cette option disponible dans toutes les bibliothèques SharePoint au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf325-130">**All SharePoint libraries** to make it available to all SharePoint libraries in your organization.</span></span></br>
      - <span data-ttu-id="cf325-131">**Seules les bibliothèques de sites sélectionnés**. Sélectionnez ensuite les sites dans lesquels vous souhaitez rendre cette option disponible ou chargez une liste de 50 sites maximum.</span><span class="sxs-lookup"><span data-stu-id="cf325-131">**Only libraries in selected sites**, and then select the sites in which you want to make it available or upload a list of up to 50 sites.</span></span></br>
      - <span data-ttu-id="cf325-132">**Aucune bibliothèque SharePoint** si cette option ne doit être disponible sur aucun site (vous pouvez modifier ce paramètre après la configuration).</span><span class="sxs-lookup"><span data-stu-id="cf325-132">**No SharePoint libraries** if you don't want to make it available to any sites (you can change this after setup).</span></span>

   ![Configurer le traitement des formulaires](../media/content-understanding/admin-configforms.png)

   > [!Note]
   > <span data-ttu-id="cf325-134">La suppression d’un site une fois inclus n’affecte pas les modèles existants appliqués aux bibliothèques de ce site. Cette action ne vous empêche pas non plus d’appliquer des modèles de compréhension de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cf325-134">Removing a site after it has been included does not affect existing models applied to the libraries in that site or the ability to apply document understanding models to a library.</span></span> 
    
6. <span data-ttu-id="cf325-135">À la page **Créer un centre de contenu**, vous pouvez créer un site de centre de contenu SharePoint. Vos utilisateurs pourront alors créer et gérer des modèles de compréhension de document sur ce même site.</span><span class="sxs-lookup"><span data-stu-id="cf325-135">On the **Create Content Center** page, you can create a SharePoint content center site on which your users can create and manage document understanding models.</span></span> </br>
    <span data-ttu-id="cf325-136">a.</span><span class="sxs-lookup"><span data-stu-id="cf325-136">a.</span></span> <span data-ttu-id="cf325-137">Dans le champ **Nom du site**, tapez le nom souhaité pour votre site de centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="cf325-137">For **Site name**, type the name you want to give your content center site.</span></span></br>
    <span data-ttu-id="cf325-138">b.</span><span class="sxs-lookup"><span data-stu-id="cf325-138">b.</span></span> <span data-ttu-id="cf325-139">Le champ **Adresse du site** affiche l’URL de votre site, en fonction du nom de site choisi.</span><span class="sxs-lookup"><span data-stu-id="cf325-139">The **Site address** will show the URL for your site, based on what you selected for the site name.</span></span> <span data-ttu-id="cf325-140">Si vous souhaitez le modifier, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf325-140">If you want to change it, click **Edit**.</span></span></br>

      ![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</br>

    <span data-ttu-id="cf325-142">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf325-142">Select **Next**.</span></span>

7. <span data-ttu-id="cf325-143">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="cf325-143">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="cf325-144">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="cf325-144">If you are satisfied with your selections, select **Activate**.</span></span>

8. <span data-ttu-id="cf325-145">À la page de confirmation, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cf325-145">On the confirmation page, click **Done**.</span></span>

9. <span data-ttu-id="cf325-146">Le programme vous renverra alors à la page **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="cf325-146">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="cf325-147">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="cf325-147">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="assign-licenses"></a><span data-ttu-id="cf325-148">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="cf325-148">Assign licenses</span></span>

<span data-ttu-id="cf325-149">Après avoir configuré SharePoint Syntex, vous devez attribuer des licences aux futurs utilisateurs des fonctionnalités de SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="cf325-149">Once you have configured SharePoint Syntex, you must assign licenses for the users who will be using any SharePoint Syntex features.</span></span>

<span data-ttu-id="cf325-150">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="cf325-150">To assign licenses:</span></span>

1. <span data-ttu-id="cf325-151">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="cf325-151">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="cf325-152">Sélectionnez les utilisateurs auxquels attribuer une licence, puis cliquez sur **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="cf325-152">Select the users that you want to license, and click **Manage product licenses**.</span></span>

3. <span data-ttu-id="cf325-153">Sélectionnez **Attribuer plus**.</span><span class="sxs-lookup"><span data-stu-id="cf325-153">Select **Assign more**.</span></span>

4. <span data-ttu-id="cf325-154">Sélectionnez **Services de contenu intelligents**.</span><span class="sxs-lookup"><span data-stu-id="cf325-154">Select **Intelligent Content Services**.</span></span> <span data-ttu-id="cf325-155">Sous **Applications**, vérifiez que les deux options **Common Data Service pour les services de contenu intelligents** et **Services de contenu intelligents** sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="cf325-155">Under **Apps**, make sure **Common Data Service for Intelligent Content Services** and **Intelligent Content Services** are both selected.</span></span>

    ![Licences SharePoint Syntex dans le Centre d’administration Microsoft 365.](../media/content-understanding/sharepoint-syntex-licenses.png)

5. <span data-ttu-id="cf325-157">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cf325-157">Click **Save changes**.</span></span>

## <a name="ai-builder-credits"></a><span data-ttu-id="cf325-158">Crédits AI Builder</span><span class="sxs-lookup"><span data-stu-id="cf325-158">AI Builder credits</span></span>

<span data-ttu-id="cf325-159">Si vous possédez 300 licences SharePoint Syntex au sein de votre organisation, vous bénéficierez d’un million de crédits AI Builder.</span><span class="sxs-lookup"><span data-stu-id="cf325-159">If you have 300 or more SharePoint Syntex licenses for SharePoint Syntex in your organization, you will be allocated one million AI Builder credits.</span></span> <span data-ttu-id="cf325-160">Si vous possédez moins de 300 licences, vous devez acheter des crédits AI Builder pour utiliser le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="cf325-160">If you have fewer than 300 licenses, you must purchase AI Builder credits in order to use forms processing.</span></span>

<span data-ttu-id="cf325-161">Vous pouvez estimer la capacité d’AI Builder qui vous convient, grâce à la calculatrice [AI Builder](https://powerapps.microsoft.com/ai-builder-calculator).</span><span class="sxs-lookup"><span data-stu-id="cf325-161">You can estimate the AI Builder capacity that’s right for you with the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator).</span></span>

<span data-ttu-id="cf325-162">Accédez au [centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/resources/capacity) pour vérifier vos crédits et leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="cf325-162">Go to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/resources/capacity) to check your credits and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf325-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf325-163">See also</span></span>

[<span data-ttu-id="cf325-164">Vue d’ensemble du modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="cf325-164">Overview of the form processing model</span></span>](https://docs.microsoft.com/ai-builder/form-processing-model-overview)

[<span data-ttu-id="cf325-165">Étape par étape : créer un modèle de compréhension de document (vidéo)</span><span class="sxs-lookup"><span data-stu-id="cf325-165">Step-by-Step: How to Build a Document Understanding Model (video)</span></span>](https://www.youtube.com/watch?v=DymSHObD-bg)

