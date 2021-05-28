---
title: Configurer SharePoint Online
ms.author: mikeplum
author: MikePlumleyMSFT
ms.reviewer: ssquires
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.collection:
- enabler-strategic
- m365initiative-syntex
search.appverid: MET150
localization_priority: Priority
description: Configurer la compréhension de contenu dans Projet Cortex
ms.openlocfilehash: 7589003505aafb480872b14a09c383cfbe0dff40
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683548"
---
# <a name="set-up-sharepoint-syntex"></a><span data-ttu-id="01e12-103">Configurer SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="01e12-103">Set up SharePoint Syntex</span></span>

<span data-ttu-id="01e12-104">Les administrateurs peuvent utiliser le Centre d’administration Microsoft 365 pour configurer [Microsoft SharePoint Syntex](index.md).</span><span class="sxs-lookup"><span data-stu-id="01e12-104">Admins can use the Microsoft 365 admin center to set up [Microsoft SharePoint Syntex](index.md).</span></span> 

<span data-ttu-id="01e12-105">Tenez compte des informations suivantes avant de démarrer :</span><span class="sxs-lookup"><span data-stu-id="01e12-105">Consider the following before you start:</span></span>

- <span data-ttu-id="01e12-106">Dans quels sites SharePoint allez-vous activer le traitement des formulaires ?</span><span class="sxs-lookup"><span data-stu-id="01e12-106">In which SharePoint sites will you enable form processing?</span></span> <span data-ttu-id="01e12-107">Tous les sites, certains sites ou des sites sélectionnés ?</span><span class="sxs-lookup"><span data-stu-id="01e12-107">All of them, some, or select sites?</span></span>
- <span data-ttu-id="01e12-108">Comment allez-vous nommer votre centre de contenu par défaut ?</span><span class="sxs-lookup"><span data-stu-id="01e12-108">What will you name your default content center?</span></span>

<span data-ttu-id="01e12-109">Vous pouvez modifier vos paramètres après la configuration initiale dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="01e12-109">You can change your settings after initial setup in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="01e12-p102">Avant la configuration, veillez à planifier la meilleure manière d’installer et de configurer la compréhension de contenu dans votre environnement. Par exemple, vous devez prendre les décisions suivantes :</span><span class="sxs-lookup"><span data-stu-id="01e12-p102">Prior to setup, make sure to plan for the best way to set up and configure content understanding in your environment. For example, you need to make the following decisions:</span></span>

- <span data-ttu-id="01e12-112">Sites SharePoint dans lesquels vous souhaitez activer le traitement des formulaires : tous les sites, certains sites ou des sites sélectionnés</span><span class="sxs-lookup"><span data-stu-id="01e12-112">The SharePoint sites in which you want to enable form processing - all of them, some, or selected sites</span></span>
- <span data-ttu-id="01e12-113">Le nom et les administrateurs de votre centre de contenu </span><span class="sxs-lookup"><span data-stu-id="01e12-113">The name and admins for your content center</span></span>

## <a name="requirements"></a><span data-ttu-id="01e12-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01e12-114">Requirements</span></span> 

> [!NOTE]
> <span data-ttu-id="01e12-115">Pour accéder au centre d’administration Microsoft 365 et configurer SharePoint Syntex, vous devez disposer des autorisations d’administrateur général ou d’administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="01e12-115">You must have Global admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up SharePoint Syntex.</span></span>

<span data-ttu-id="01e12-116">En tant qu’administrateur, vous pouvez également modifier vos paramètres sélectionnés à tout moment après la configuration, ainsi que les paramètres de gestion de la compréhension de contenu dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="01e12-116">As an admin, you can also make changes to your selected settings anytime after setup, and throughout the content understanding management settings in the Microsoft 365 Admin Center.</span></span>

<span data-ttu-id="01e12-117">Si vous envisagez d’utiliser un environnement Platform Power personnalisé, vous devez [installer l’application *Générateur d’IA pour Project Cortex* dans cet environnement](/power-platform/admin/manage-apps#install-an-app-in-the-environment-view) et y [attribuer des crédits du Générateur d’IA](/power-platform/admin/capacity-add-on) avant de pouvoir créer des modèles de traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="01e12-117">If you plan to use a custom Power Platform environment, you must [install the *AI Builder for Project Cortex* app in this environment](/power-platform/admin/manage-apps#install-an-app-in-the-environment-view) and [allocate AI Builder credits](/power-platform/admin/capacity-add-on) to it before you can create form processing models.</span></span>

### <a name="licensing"></a><span data-ttu-id="01e12-118">Gestion des licences</span><span class="sxs-lookup"><span data-stu-id="01e12-118">Licensing</span></span>

<span data-ttu-id="01e12-119">Pour utiliser SharePoint Syntex, votre organisation doit avoir un abonnement à SharePoint Syntex, et chaque utilisateur doit avoir les licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="01e12-119">To use SharePoint Syntex, your organization must have a subscription to SharePoint Syntex, and each user must have the following licenses assigned:</span></span>

- <span data-ttu-id="01e12-120">SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="01e12-120">SharePoint Syntex</span></span>
- <span data-ttu-id="01e12-121">SharePoint Syntex : Type DPO</span><span class="sxs-lookup"><span data-stu-id="01e12-121">SharePoint Syntex - SPO type</span></span>
- <span data-ttu-id="01e12-122">Service de données courant pour SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="01e12-122">Common Data Service for SharePoint Syntex</span></span>

<span data-ttu-id="01e12-123">Si vous annulez votre abonnement SharePoint Syntex à une date ultérieure (ou si votre version d’évaluation expire), les utilisateurs ne pourront plus créer ou exécuter des modèles de présentation ou de traitement de formulaires, et le modèle du centre de contenu ne sera plus disponible.</span><span class="sxs-lookup"><span data-stu-id="01e12-123">If you cancel your SharePoint Syntex subscription at a future date (or your trial expires), users will no longer be able to create or run document understanding or form processing models, and the content center template will no longer be available.</span></span> <span data-ttu-id="01e12-124">En outre, les rapports des magasins à terme, l'importation de la taxonomie SKOS et la poussée des types de contenu ne seront plus disponibles.</span><span class="sxs-lookup"><span data-stu-id="01e12-124">Additionally, term store reports, SKOS taxonomy import, and Content type push will no longer be available.</span></span> <span data-ttu-id="01e12-125">Aucun contenu n’est supprimé et les autorisations de site ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="01e12-125">No content will be deleted and site permissions will not be changed.</span></span>

### <a name="ai-builder-credits"></a><span data-ttu-id="01e12-126">Crédits AI Builder</span><span class="sxs-lookup"><span data-stu-id="01e12-126">AI Builder credits</span></span>

<span data-ttu-id="01e12-127">Si vous possédez 300 licences SharePoint Syntex au sein de votre organisation, vous bénéficierez d’un million de crédits AI Builder.</span><span class="sxs-lookup"><span data-stu-id="01e12-127">If you have 300 or more SharePoint Syntex licenses for SharePoint Syntex in your organization, you will be allocated one million AI Builder credits.</span></span> <span data-ttu-id="01e12-128">Si vous possédez moins de 300 licences, vous devez acheter des crédits AI Builder pour utiliser le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="01e12-128">If you have fewer than 300 licenses, you must purchase AI Builder credits in order to use forms processing.</span></span>

<span data-ttu-id="01e12-129">Vous pouvez estimer la capacité d’AI Builder qui vous convient, grâce à la calculatrice [AI Builder](https://powerapps.microsoft.com/ai-builder-calculator).</span><span class="sxs-lookup"><span data-stu-id="01e12-129">You can estimate the AI Builder capacity that’s right for you with the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator).</span></span>

<span data-ttu-id="01e12-130">Si vous planifiez d’utiliser un environnement Power Platform personnalisé, vous devez [attribuer des crédit à cet environnement](/power-platform/admin/capacity-add-on).</span><span class="sxs-lookup"><span data-stu-id="01e12-130">If you plan to use a custom Power Platform environment, you must [allocate credits to that environment](/power-platform/admin/capacity-add-on).</span></span>

<span data-ttu-id="01e12-131">Accédez au [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/resources/capacity) pour vérifier vos crédits et leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="01e12-131">Go to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/resources/capacity) to check your credits and usage.</span></span>

## <a name="to-set-up-sharepoint-syntex"></a><span data-ttu-id="01e12-132">Pour configurer SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="01e12-132">To set up SharePoint Syntex</span></span>

1. <span data-ttu-id="01e12-133">Dans le Centre d’administration Microsoft 365, sélectionnez **Configuration**, puis affichez la section **Fichiers et contenu**.</span><span class="sxs-lookup"><span data-stu-id="01e12-133">In the Microsoft 365 admin center, select **Setup**, and then view the **Files and content** section.</span></span>

2. <span data-ttu-id="01e12-134">Dans la section **Fichiers et contenu**, sélectionnez **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="01e12-134">In the **Files and content** section, select **Automate content understanding**.</span></span> <span data-ttu-id="01e12-135">Notez que la disponibilité de votre crédit AI Builder actuel s’affiche dans la section **D’un coup d’œil**.</span><span class="sxs-lookup"><span data-stu-id="01e12-135">Note that your current AI Builder credit availability is shown in the **At a glance** section.</span></span><br/>

3. <span data-ttu-id="01e12-136">À la page **Automatiser la compréhension de contenu** , cliquez sur **Commencer** pour parcourir le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="01e12-136">On the **Automate content understanding** page, click **Get started** to walk through the setup process.</span></span> <br/>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="01e12-137">![Commencer la configuration](../media/content-understanding/admin-content-understanding-get-started.png)</span><span class="sxs-lookup"><span data-stu-id="01e12-137">![Begin setup](../media/content-understanding/admin-content-understanding-get-started.png)</span></span></br>

4. <span data-ttu-id="01e12-138">Sur la page **Configurer le traitement des formulaires**, vous pouvez choisir d’autoriser ou non les utilisateurs à créer des modèles de traitement de formulaire dans des bibliothèques de documents SharePoint spécifiques.</span><span class="sxs-lookup"><span data-stu-id="01e12-138">On the **Configure Form Processing** page, you can choose if you want to let users be able to create form processing models in specific SharePoint document libraries.</span></span> <span data-ttu-id="01e12-139">Une option de menu **Créer un modèle de traitement de formulaire** sera disponible dans les rubans des bibliothèques de documents SharePoint où le traitement des formulaires est activé.</span><span class="sxs-lookup"><span data-stu-id="01e12-139">A menu option will be available in the document library ribbon to **Create a form processing model** in SharePoint document libraries in which it is enabled.</span></span>
 
     <span data-ttu-id="01e12-140">Concernant les **bibliothèques SharePoint qui doivent afficher l’option de création d’un modèle de traitement de formulaire**, vous pouvez sélectionner les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="01e12-140">For **Which SharePoint libraries should show option to create a form processing model**, you can select:</span></span></br>
      - <span data-ttu-id="01e12-141">**Les bibliothèques dans les sites SharePoint** pour rendre cette option disponible dans toutes les bibliothèques SharePoint au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01e12-141">**Libraries in all SharePoint sites** to make it available to all SharePoint libraries in your organization.</span></span></br>
      - <span data-ttu-id="01e12-142">**Ls bibliothèques dans les sites SharePoint sélectionnés**. Sélectionnez ensuite les sites dans lesquels vous souhaitez rendre cette option disponible ou chargez une liste de 50 sites maximum.</span><span class="sxs-lookup"><span data-stu-id="01e12-142">**Libraries in selected SharePoint sites**, and then select the sites in which you want to make it available or upload a list of up to 50 sites.</span></span></br>
      - <span data-ttu-id="01e12-143">**Aucune bibliothèque SharePoint** si cette option ne doit être disponible sur aucun site (vous pouvez modifier ce paramètre après la configuration).</span><span class="sxs-lookup"><span data-stu-id="01e12-143">**No SharePoint libraries** if you don't want to make it available to any sites (you can change this after setup).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="01e12-144">![Configurer les options du site de traitement des formulaires](../media/content-understanding/admin-configforms.png)</span><span class="sxs-lookup"><span data-stu-id="01e12-144">![Configure form processing site options](../media/content-understanding/admin-configforms.png)</span></span>

   > [!Note]
   > <span data-ttu-id="01e12-145">La suppression d’un site une fois inclus n’affecte pas les modèles existants appliqués aux bibliothèques de ce site. Cette action ne vous empêche pas non plus d’appliquer des modèles de compréhension de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="01e12-145">Removing a site after it has been included does not affect existing models applied to the libraries in that site or the ability to apply document understanding models to a library.</span></span> 
    
    <span data-ttu-id="01e12-146">Si vous avez plusieurs environnements Power Platform configurés, vous pouvez choisir celui à utiliser avec le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="01e12-146">If you have multiple Power Platform environments configured, you can choose which one you want to use with for form processing.</span></span> <span data-ttu-id="01e12-147">(Cette option ne s’affiche pas si vous n’avez qu’un seul environnement.)</span><span class="sxs-lookup"><span data-stu-id="01e12-147">(This option will not appear if you only have one environment.)</span></span>

    ![Configurer les options Power Platform de traitement des formulaires](../media/content-understanding/setup-power-platform-env.png)

    <span data-ttu-id="01e12-149">Pour l’**environnement Power Platform**, vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="01e12-149">For **Power Platform environment**, you can select:</span></span>
    - <span data-ttu-id="01e12-150">**Utilisez l’environnement par défaut** pour utiliser votre environnement Power Platform par défaut.</span><span class="sxs-lookup"><span data-stu-id="01e12-150">**Use the default environment** to use your default Power Platform environment.</span></span>
    - <span data-ttu-id="01e12-151">**Utilisez un environnement personnalisé** pour utiliser un environnement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="01e12-151">**Use a custom environment** to use a custom environment.</span></span> <span data-ttu-id="01e12-152">Sélectionnez l’environnement que vous souhaitez utiliser dans la liste.</span><span class="sxs-lookup"><span data-stu-id="01e12-152">Choose the environment that you want to use from the list.</span></span> <span data-ttu-id="01e12-153">([Voir la configuration requise pour un environnement personnalisé](/microsoft-365/contentunderstanding/set-up-content-understanding#requirements)).</span><span class="sxs-lookup"><span data-stu-id="01e12-153">([See the requirements for a custom environment](/microsoft-365/contentunderstanding/set-up-content-understanding#requirements)).</span></span>

    <span data-ttu-id="01e12-154">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="01e12-154">Click **Next**.</span></span>

5. <span data-ttu-id="01e12-155">À la page **Créer un centre de contenu**, vous pouvez créer un site de centre de contenu SharePoint. Vos utilisateurs pourront alors créer et gérer des modèles de compréhension de document sur ce même site.</span><span class="sxs-lookup"><span data-stu-id="01e12-155">On the **Create Content Center** page, you can create a SharePoint content center site on which your users can create and manage document understanding models.</span></span>

    1. <span data-ttu-id="01e12-156">Dans le champ **Nom du site**, tapez le nom souhaité pour votre site de centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="01e12-156">For **Site name**, type the name you want to give your content center site.</span></span>
    
    1. <span data-ttu-id="01e12-157">Le champ **Adresse du site** affiche l’URL de votre site, en fonction du nom de site choisi.</span><span class="sxs-lookup"><span data-stu-id="01e12-157">The **Site address** will show the URL for your site, based on what you selected for the site name.</span></span> <span data-ttu-id="01e12-158">Si vous souhaitez le modifier, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="01e12-158">If you want to change it, click **Edit**.</span></span>

       > [!div class="mx-imgBorder"]
       > <span data-ttu-id="01e12-159">![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</span><span class="sxs-lookup"><span data-stu-id="01e12-159">![Create content center](../media/content-understanding/admin-cu-create-cc.png)</span></span></br>

       <span data-ttu-id="01e12-160">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="01e12-160">Select **Next**.</span></span>

6. <span data-ttu-id="01e12-161">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="01e12-161">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="01e12-162">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="01e12-162">If you are satisfied with your selections, select **Activate**.</span></span>

7. <span data-ttu-id="01e12-163">À la page de confirmation, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="01e12-163">On the confirmation page, click **Done**.</span></span>

8. <span data-ttu-id="01e12-164">Le programme vous renverra alors à la page **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="01e12-164">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="01e12-165">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="01e12-165">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="assign-licenses"></a><span data-ttu-id="01e12-166">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="01e12-166">Assign licenses</span></span>

<span data-ttu-id="01e12-167">Après avoir configuré SharePoint Syntex, vous devez attribuer des licences aux futurs utilisateurs des fonctionnalités de SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="01e12-167">Once you have configured SharePoint Syntex, you must assign licenses for the users who will be using any SharePoint Syntex features.</span></span>

<span data-ttu-id="01e12-168">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="01e12-168">To assign licenses:</span></span>

1. <span data-ttu-id="01e12-169">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="01e12-169">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="01e12-170">Sélectionnez les utilisateurs auxquels attribuer une licence, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="01e12-170">Select the users that you want to license, and choose **Manage product licenses**.</span></span>

3. <span data-ttu-id="01e12-171">Sélectionnez **Applications** dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="01e12-171">Choose **Apps** from the drop-down menu.</span></span>

4. <span data-ttu-id="01e12-172">Sélectionnez **Afficher les applications pour SharePoint Syntex**.</span><span class="sxs-lookup"><span data-stu-id="01e12-172">Select **Show apps for  SharePoint Syntex**.</span></span> <span data-ttu-id="01e12-173">Sous **Applications**, assurez-vous que **service de données commun pour SharePoint Syntex**, **SharePoint Syntex** et **SharePoint Syntex-SPO type** sont tous sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="01e12-173">Under **Apps**, make sure **Common Data Service for SharePoint Syntex**, **SharePoint Syntex**, and **SharePoint Syntex - SPO type** are all selected.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="01e12-174">![Licences SharePoint Syntex dans le Centre d’administration Microsoft 365.](../media/content-understanding/sharepoint-syntex-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="01e12-174">![SharePoint Syntex licenses in the Microsoft 365 admin center](../media/content-understanding/sharepoint-syntex-licenses.png)</span></span>

5. <span data-ttu-id="01e12-175">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="01e12-175">Click **Save changes**.</span></span>

## <a name="see-also"></a><span data-ttu-id="01e12-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01e12-176">See also</span></span>

[<span data-ttu-id="01e12-177">Vue d’ensemble du modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="01e12-177">Overview of the form processing model</span></span>](/ai-builder/form-processing-model-overview)

[<span data-ttu-id="01e12-178">Étape par étape : créer un modèle de compréhension de document (vidéo)</span><span class="sxs-lookup"><span data-stu-id="01e12-178">Step-by-Step: How to Build a Document Understanding Model (video)</span></span>](https://www.youtube.com/watch?v=DymSHObD-bg)

[<span data-ttu-id="01e12-179">Créer et gérer des environnements dans le Centre d'administration Power Platform</span><span class="sxs-lookup"><span data-stu-id="01e12-179">Create and manage environments in the Power Platform admin center</span></span>](/power-platform/admin/create-environment)
