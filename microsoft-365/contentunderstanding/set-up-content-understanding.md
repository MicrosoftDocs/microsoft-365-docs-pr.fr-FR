---
title: Configurer SharePoint Online
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
ms.openlocfilehash: 2f9fd4e035152a127f9f1c254f4c489a6ca4c976
ms.sourcegitcommit: f000358c01a8006e5749a86b256300ee3a73174c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2021
ms.locfileid: "51994700"
---
# <a name="set-up-sharepoint-syntex"></a><span data-ttu-id="f08c2-103">Configurer SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f08c2-103">Set up SharePoint Syntex</span></span>

<span data-ttu-id="f08c2-104">Les administrateurs peuvent utiliser le Centre d’administration Microsoft 365 pour configurer [Microsoft SharePoint Syntex](index.md).</span><span class="sxs-lookup"><span data-stu-id="f08c2-104">Admins can use the Microsoft 365 admin center to set up [Microsoft SharePoint Syntex](index.md).</span></span> 

<span data-ttu-id="f08c2-105">Tenez compte des informations suivantes avant de démarrer :</span><span class="sxs-lookup"><span data-stu-id="f08c2-105">Consider the following before you start:</span></span>

- <span data-ttu-id="f08c2-106">Dans quels sites SharePoint allez-vous activer le traitement des formulaires ?</span><span class="sxs-lookup"><span data-stu-id="f08c2-106">In which SharePoint sites will you enable form processing?</span></span> <span data-ttu-id="f08c2-107">Tous les sites, certains sites ou des sites sélectionnés ?</span><span class="sxs-lookup"><span data-stu-id="f08c2-107">All of them, some, or select sites?</span></span>
- <span data-ttu-id="f08c2-108">Comment allez-vous nommer votre centre de contenu par défaut ?</span><span class="sxs-lookup"><span data-stu-id="f08c2-108">What will you name your default content center?</span></span>

<span data-ttu-id="f08c2-109">Vous pouvez modifier vos paramètres après la configuration initiale dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f08c2-109">You can change your settings after initial setup in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="f08c2-110">Avant la configuration, veillez à planifier la meilleure manière d’installer et de configurer la compréhension de contenu dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="f08c2-110">Prior to setup, make sure to plan for the best way to set up and configure content understanding in your environment.</span></span> <span data-ttu-id="f08c2-111">Par exemple, vous devez prendre les décisions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f08c2-111">For example, you need to make the following decisions:</span></span>

- <span data-ttu-id="f08c2-112">Sites SharePoint dans lesquels vous souhaitez activer le traitement des formulaires : tous les sites, certains sites ou des sites sélectionnés</span><span class="sxs-lookup"><span data-stu-id="f08c2-112">The SharePoint sites in which you want to enable form processing - all of them, some, or selected sites</span></span>
- <span data-ttu-id="f08c2-113">Le nom et les administrateurs de votre centre de contenu </span><span class="sxs-lookup"><span data-stu-id="f08c2-113">The name and admins for your content center</span></span>

## <a name="requirements"></a><span data-ttu-id="f08c2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f08c2-114">Requirements</span></span> 

> [!NOTE]
> <span data-ttu-id="f08c2-115">Pour accéder au centre d’administration Microsoft 365 et configurer SharePoint Syntex, vous devez disposer des autorisations d’administrateur général ou d’administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f08c2-115">You must have Global admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up SharePoint Syntex.</span></span>

<span data-ttu-id="f08c2-116">En tant qu’administrateur, vous pouvez également modifier vos paramètres sélectionnés à tout moment après la configuration, ainsi que les paramètres de gestion de la compréhension de contenu dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f08c2-116">As an admin, you can also make changes to your selected settings anytime after setup, and throughout the content understanding management settings in the Microsoft 365 Admin Center.</span></span>

### <a name="licensing"></a><span data-ttu-id="f08c2-117">Gestion des licences</span><span class="sxs-lookup"><span data-stu-id="f08c2-117">Licensing</span></span>

<span data-ttu-id="f08c2-118">Pour utiliser SharePoint Syntex, votre organisation doit avoir un abonnement à SharePoint Syntex, et chaque utilisateur doit avoir les licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="f08c2-118">To use SharePoint Syntex, your organization must have a subscription to SharePoint Syntex, and each user must have the following licenses assigned:</span></span>

- <span data-ttu-id="f08c2-119">SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="f08c2-119">SharePoint Syntex</span></span>
- <span data-ttu-id="f08c2-120">SharePoint Syntex : Type DPO</span><span class="sxs-lookup"><span data-stu-id="f08c2-120">SharePoint Syntex - SPO type</span></span>
- <span data-ttu-id="f08c2-121">Service de données courant pour SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="f08c2-121">Common Data Service for SharePoint Syntex</span></span>

<span data-ttu-id="f08c2-122">Si vous annulez votre abonnement SharePoint Syntex à une date ultérieure (ou si votre version d’évaluation expire), les utilisateurs ne pourront plus créer ou exécuter des modèles de présentation ou de traitement de formulaires, et le modèle du centre de contenu ne sera plus disponible.</span><span class="sxs-lookup"><span data-stu-id="f08c2-122">If you cancel your SharePoint Syntex subscription at a future date (or your trial expires), users will no longer be able to create or run document understanding or form processing models, and the content center template will no longer be available.</span></span> <span data-ttu-id="f08c2-123">En outre, les rapports des magasins à terme, l'importation de la taxonomie SKOS et la poussée des types de contenu ne seront plus disponibles.</span><span class="sxs-lookup"><span data-stu-id="f08c2-123">Additionally, term store reports, SKOS taxonomy import, and Content type push will no longer be available.</span></span> <span data-ttu-id="f08c2-124">Aucun contenu n’est supprimé et les autorisations de site ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="f08c2-124">No content will be deleted and site permissions will not be changed.</span></span>

### <a name="ai-builder-credits"></a><span data-ttu-id="f08c2-125">Crédits AI Builder</span><span class="sxs-lookup"><span data-stu-id="f08c2-125">AI Builder credits</span></span>

<span data-ttu-id="f08c2-126">Si vous possédez 300 licences SharePoint Syntex au sein de votre organisation, vous bénéficierez d’un million de crédits AI Builder.</span><span class="sxs-lookup"><span data-stu-id="f08c2-126">If you have 300 or more SharePoint Syntex licenses for SharePoint Syntex in your organization, you will be allocated one million AI Builder credits.</span></span> <span data-ttu-id="f08c2-127">Si vous possédez moins de 300 licences, vous devez acheter des crédits AI Builder pour utiliser le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="f08c2-127">If you have fewer than 300 licenses, you must purchase AI Builder credits in order to use forms processing.</span></span>

<span data-ttu-id="f08c2-128">Vous pouvez estimer la capacité d’AI Builder qui vous convient, grâce à la calculatrice [AI Builder](https://powerapps.microsoft.com/ai-builder-calculator).</span><span class="sxs-lookup"><span data-stu-id="f08c2-128">You can estimate the AI Builder capacity that’s right for you with the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator).</span></span>

<span data-ttu-id="f08c2-129">Si vous planifiez d’utiliser un environnement Power Platform personnalisé, vous devez [attribuer des crédit à cet environnement](/power-platform/admin/capacity-add-on).</span><span class="sxs-lookup"><span data-stu-id="f08c2-129">If you plan to use a custom Power Platform environment, you must [allocate credits to that environment](/power-platform/admin/capacity-add-on).</span></span>

<span data-ttu-id="f08c2-130">Accédez au [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/resources/capacity) pour vérifier vos crédits et leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="f08c2-130">Go to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/resources/capacity) to check your credits and usage.</span></span>

## <a name="to-set-up-sharepoint-syntex"></a><span data-ttu-id="f08c2-131">Pour configurer SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="f08c2-131">To set up SharePoint Syntex</span></span>

1. <span data-ttu-id="f08c2-132">Dans le Centre d’administration Microsoft 365, sélectionnez **Configuration**, puis affichez la section **Fichiers et contenu**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-132">In the Microsoft 365 admin center, select **Setup**, and then view the **Files and content** section.</span></span>

2. <span data-ttu-id="f08c2-133">Dans la section **Fichiers et contenu**, sélectionnez **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-133">In the **Files and content** section, select **Automate content understanding**.</span></span><br/>

3. <span data-ttu-id="f08c2-134">À la page **Automatiser la compréhension de contenu** , cliquez sur **Commencer** pour parcourir le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="f08c2-134">On the **Automate content understanding** page, click **Get started** to walk through the setup process.</span></span><br/>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f08c2-135">![Commencer la configuration](../media/content-understanding/admin-content-understanding-get-started.png)</span><span class="sxs-lookup"><span data-stu-id="f08c2-135">![Begin setup](../media/content-understanding/admin-content-understanding-get-started.png)</span></span></br>

4. <span data-ttu-id="f08c2-136">Sur la page **Configurer le traitement des formulaires**, vous pouvez choisir d’autoriser ou non les utilisateurs à créer des modèles de traitement de formulaire dans des bibliothèques de documents SharePoint spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f08c2-136">On the **Configure Form Processing** page, you can choose if you want to let users be able to create form processing models in specific SharePoint document libraries.</span></span> <span data-ttu-id="f08c2-137">Une option de menu **Créer un modèle de traitement de formulaire** sera disponible dans les rubans des bibliothèques de documents SharePoint où le traitement des formulaires est activé.</span><span class="sxs-lookup"><span data-stu-id="f08c2-137">A menu option will be available in the document library ribbon to **Create a form processing model** in SharePoint document libraries in which it is enabled.</span></span>
 
     <span data-ttu-id="f08c2-138">Concernant les **bibliothèques SharePoint qui doivent afficher l’option de création d’un modèle de traitement de formulaire**, vous pouvez sélectionner les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f08c2-138">For **Which SharePoint libraries should show option to create a form processing model**, you can select:</span></span></br>
      - <span data-ttu-id="f08c2-139">**Les bibliothèques dans les sites SharePoint** pour rendre cette option disponible dans toutes les bibliothèques SharePoint au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f08c2-139">**Libraries in all SharePoint sites** to make it available to all SharePoint libraries in your organization.</span></span></br>
      - <span data-ttu-id="f08c2-140">**Ls bibliothèques dans les sites SharePoint sélectionnés**. Sélectionnez ensuite les sites dans lesquels vous souhaitez rendre cette option disponible ou chargez une liste de 50 sites maximum.</span><span class="sxs-lookup"><span data-stu-id="f08c2-140">**Libraries in selected SharePoint sites**, and then select the sites in which you want to make it available or upload a list of up to 50 sites.</span></span></br>
      - <span data-ttu-id="f08c2-141">**Aucune bibliothèque SharePoint** si cette option ne doit être disponible sur aucun site (vous pouvez modifier ce paramètre après la configuration).</span><span class="sxs-lookup"><span data-stu-id="f08c2-141">**No SharePoint libraries** if you don't want to make it available to any sites (you can change this after setup).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f08c2-142">![Configurer les options du site de traitement des formulaires](../media/content-understanding/admin-configforms.png)</span><span class="sxs-lookup"><span data-stu-id="f08c2-142">![Configure form processing site options](../media/content-understanding/admin-configforms.png)</span></span>

   > [!Note]
   > <span data-ttu-id="f08c2-143">La suppression d’un site une fois inclus n’affecte pas les modèles existants appliqués aux bibliothèques de ce site. Cette action ne vous empêche pas non plus d’appliquer des modèles de compréhension de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f08c2-143">Removing a site after it has been included does not affect existing models applied to the libraries in that site or the ability to apply document understanding models to a library.</span></span> 
    
    <span data-ttu-id="f08c2-144">Si vous avez plusieurs environnements Power Platform configurés, vous pouvez choisir celui à utiliser avec le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="f08c2-144">If you have multiple Power Platform environments configured, you can choose which one you want to use with for form processing.</span></span> <span data-ttu-id="f08c2-145">(Cette option ne s’affiche pas si vous n’avez qu’un seul environnement.)</span><span class="sxs-lookup"><span data-stu-id="f08c2-145">(This option will not appear if you only have one environment.)</span></span>

    ![Configurer les options Power Platform de traitement des formulaires](../media/content-understanding/setup-power-platform-env.png)

    <span data-ttu-id="f08c2-147">Pour l’**environnement Power Platform**, vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="f08c2-147">For **Power Platform environment**, you can select:</span></span>
    - <span data-ttu-id="f08c2-148">**Utilisez l’environnement par défaut** pour utiliser votre environnement Power Platform par défaut.</span><span class="sxs-lookup"><span data-stu-id="f08c2-148">**Use the default environment** to use your default Power Platform environment.</span></span>
    - <span data-ttu-id="f08c2-149">**Utilisez un environnement personnalisé** pour utiliser un environnement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f08c2-149">**Use a custom environment** to use a custom environment.</span></span> <span data-ttu-id="f08c2-150">Sélectionnez l’environnement que vous souhaitez utiliser dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f08c2-150">Choose the environment that you want to use from the list.</span></span> <span data-ttu-id="f08c2-151">Vous devez installer l’application *Générateur d’IA pour Project Cortex* dans cet environnement et y attribuer des crédits du Générateur d’IA avant de pouvoir créer des modèles de traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="f08c2-151">You must install the *AI Builder for Project Cortex* app in this environment and allocate AI Builder credits to it before you can create form processing models.</span></span>

    <span data-ttu-id="f08c2-152">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-152">Click **Next**.</span></span>

5. <span data-ttu-id="f08c2-153">À la page **Créer un centre de contenu**, vous pouvez créer un site de centre de contenu SharePoint. Vos utilisateurs pourront alors créer et gérer des modèles de compréhension de document sur ce même site.</span><span class="sxs-lookup"><span data-stu-id="f08c2-153">On the **Create Content Center** page, you can create a SharePoint content center site on which your users can create and manage document understanding models.</span></span>

    1. <span data-ttu-id="f08c2-154">Dans le champ **Nom du site**, tapez le nom souhaité pour votre site de centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="f08c2-154">For **Site name**, type the name you want to give your content center site.</span></span>
    
    1. <span data-ttu-id="f08c2-155">Le champ **Adresse du site** affiche l’URL de votre site, en fonction du nom de site choisi.</span><span class="sxs-lookup"><span data-stu-id="f08c2-155">The **Site address** will show the URL for your site, based on what you selected for the site name.</span></span> <span data-ttu-id="f08c2-156">Si vous souhaitez le modifier, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-156">If you want to change it, click **Edit**.</span></span>

       > [!div class="mx-imgBorder"]
       > <span data-ttu-id="f08c2-157">![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</span><span class="sxs-lookup"><span data-stu-id="f08c2-157">![Create content center](../media/content-understanding/admin-cu-create-cc.png)</span></span></br>

       <span data-ttu-id="f08c2-158">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-158">Select **Next**.</span></span>

6. <span data-ttu-id="f08c2-159">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="f08c2-159">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="f08c2-160">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-160">If you are satisfied with your selections, select **Activate**.</span></span>

7. <span data-ttu-id="f08c2-161">À la page de confirmation, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-161">On the confirmation page, click **Done**.</span></span>

8. <span data-ttu-id="f08c2-162">Le programme vous renverra alors à la page **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-162">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="f08c2-163">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="f08c2-163">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="assign-licenses"></a><span data-ttu-id="f08c2-164">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="f08c2-164">Assign licenses</span></span>

<span data-ttu-id="f08c2-165">Après avoir configuré SharePoint Syntex, vous devez attribuer des licences aux futurs utilisateurs des fonctionnalités de SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="f08c2-165">Once you have configured SharePoint Syntex, you must assign licenses for the users who will be using any SharePoint Syntex features.</span></span>

<span data-ttu-id="f08c2-166">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="f08c2-166">To assign licenses:</span></span>

1. <span data-ttu-id="f08c2-167">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-167">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="f08c2-168">Sélectionnez les utilisateurs auxquels attribuer une licence, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-168">Select the users that you want to license, and choose **Manage product licenses**.</span></span>

3. <span data-ttu-id="f08c2-169">Sélectionnez **Applications** dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="f08c2-169">Choose **Apps** from the drop-down menu.</span></span>

4. <span data-ttu-id="f08c2-170">Sélectionnez **Afficher les applications pour SharePoint Syntex**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-170">Select **Show apps for  SharePoint Syntex**.</span></span> <span data-ttu-id="f08c2-171">Sous **Applications**, assurez-vous que **service de données commun pour SharePoint Syntex**, **SharePoint Syntex** et **SharePoint Syntex-SPO type** sont tous sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f08c2-171">Under **Apps**, make sure **Common Data Service for SharePoint Syntex**, **SharePoint Syntex**, and **SharePoint Syntex - SPO type** are all selected.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f08c2-172">![Licences SharePoint Syntex dans le Centre d’administration Microsoft 365.](../media/content-understanding/sharepoint-syntex-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="f08c2-172">![SharePoint Syntex licenses in the Microsoft 365 admin center](../media/content-understanding/sharepoint-syntex-licenses.png)</span></span>

5. <span data-ttu-id="f08c2-173">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="f08c2-173">Click **Save changes**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f08c2-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f08c2-174">See also</span></span>

[<span data-ttu-id="f08c2-175">Vue d’ensemble du modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="f08c2-175">Overview of the form processing model</span></span>](/ai-builder/form-processing-model-overview)

[<span data-ttu-id="f08c2-176">Étape par étape : créer un modèle de compréhension de document (vidéo)</span><span class="sxs-lookup"><span data-stu-id="f08c2-176">Step-by-Step: How to Build a Document Understanding Model (video)</span></span>](https://www.youtube.com/watch?v=DymSHObD-bg)

[<span data-ttu-id="f08c2-177">Créer et gérer des environnements dans le Centre d'administration Power Platform</span><span class="sxs-lookup"><span data-stu-id="f08c2-177">Create and manage environments in the Power Platform admin center</span></span>](/power-platform/admin/create-environment)
