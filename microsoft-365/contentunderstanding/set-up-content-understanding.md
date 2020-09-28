---
title: Configurer SharePoint Syntex
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Configurer la compréhension du contenu dans le projet cortex
ms.openlocfilehash: f0a26f0044e578928730cf4930f1524e86dff9f3
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48294869"
---
# <a name="set-up-sharepoint-syntex"></a><span data-ttu-id="c6663-103">Configurer SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="c6663-103">Set up SharePoint Syntex</span></span>

<span data-ttu-id="c6663-104">Les administrateurs peuvent utiliser le centre d’administration Microsoft 365 pour installer et Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="c6663-104">Admins can use the Microsoft 365 admin center to set up and Microsoft SharePoint Syntex.</span></span> 

<span data-ttu-id="c6663-105">Tenez compte des points suivants avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="c6663-105">Consider the following before you start:</span></span>

- <span data-ttu-id="c6663-106">Quels sites SharePoint allez-vous activer le traitement de formulaires ?</span><span class="sxs-lookup"><span data-stu-id="c6663-106">Which SharePoint sites will you enable form processing?</span></span> <span data-ttu-id="c6663-107">Tous les sites, certains d’entre eux ou certains sites sélectionnés ?</span><span class="sxs-lookup"><span data-stu-id="c6663-107">All of them, some, or select sites?</span></span>
- <span data-ttu-id="c6663-108">Quels seront les noms de votre centre de contenu et celui de l’administrateur principal du site ?</span><span class="sxs-lookup"><span data-stu-id="c6663-108">What will you name of your content center, and who is the primary site admin?</span></span>

<span data-ttu-id="c6663-109">Vous pouvez modifier vos paramètres après l’installation initiale dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6663-109">You can change your settings after initial setup in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="c6663-110">Le contenu de cet article est destiné à la préversion privée du projet cortex.</span><span class="sxs-lookup"><span data-stu-id="c6663-110">The content in this article is for the Project Cortex Private Preview.</span></span> <span data-ttu-id="c6663-111">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="c6663-111">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="c6663-112">Avant de procéder à l’installation, veillez à planifier la meilleure façon de configurer et de configurer la compréhension du contenu dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="c6663-112">Prior to setup, make sure to plan for the best way to set up and configure content understanding in your environment.</span></span> <span data-ttu-id="c6663-113">Par exemple, vous devez prendre en compte les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="c6663-113">For example, you need to make considerations about the following names of:</span></span>

- <span data-ttu-id="c6663-114">Les sites SharePoint pour lesquels vous souhaitez activer le traitement de formulaire-tous les sites, certains ou certains sites sélectionnés</span><span class="sxs-lookup"><span data-stu-id="c6663-114">The SharePoint sites that you want to enable form processing - all of them, some, or selected sites</span></span>
- <span data-ttu-id="c6663-115">Votre centre de contenu et le nom de l’administrateur de site principal</span><span class="sxs-lookup"><span data-stu-id="c6663-115">Your content center and the name of the primary site admin</span></span>

## <a name="requirements"></a><span data-ttu-id="c6663-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6663-116">Requirements</span></span> 

> [!NOTE]
> <span data-ttu-id="c6663-117">Vous devez disposer d’autorisations d’administrateur général ou d’administrateur SharePoint pour pouvoir accéder au centre d’administration Microsoft 365 et configurer le mémorandum d’accord sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="c6663-117">You must have Global admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up content understanding.</span></span>

<span data-ttu-id="c6663-118">En tant qu’administrateur, vous pouvez également modifier les paramètres sélectionnés à tout moment après l’installation, et tout au long du processus de présentation du contenu dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6663-118">As an admin, you can also make changes to your selected settings anytime after setup, and throughout the content understanding management settings in the Microsoft 365 Admin Center.</span></span>

## <a name="to-set-up-sharepoint-syntex"></a><span data-ttu-id="c6663-119">Pour configurer SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="c6663-119">To set up SharePoint Syntex</span></span>

1. <span data-ttu-id="c6663-120">Dans le centre d’administration 365 de Microsoft, sélectionnez **configuration**, puis affichez la section connaissances de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="c6663-120">In the Microsoft 365 admin center, select **Setup**, and then view the **Organizational knowledge** section.</span></span>

2. <span data-ttu-id="c6663-121">Dans la section connaissances de l' **organisation** , sélectionnez **automatiser la compréhension du contenu**.</span><span class="sxs-lookup"><span data-stu-id="c6663-121">In the **Organizational knowledge** section, select **Automate content understanding**.</span></span><br/>

    ![Page de configuration des connaissances organisationnelles](../media/content-understanding/admin-org-knowledge-options.png)</br>

3. <span data-ttu-id="c6663-123">Sur la page **automatiser SharePoint Syntex** , cliquez sur **commencer** pour passer en revue le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="c6663-123">On the **Automate SharePoint Syntex** page, click **Get started** to walk through the setup process.</span></span><br/>

    ![Début de l’installation](../media/content-understanding/admin-content-understanding-get-started.png)</br>

4. <span data-ttu-id="c6663-125">Sur la page activation du marquage de l’image, choisissez si vous souhaitez autoriser l' [étiquetage des images](image-tagging.md).</span><span class="sxs-lookup"><span data-stu-id="c6663-125">On the Turn on image tagging page, choose if you want to allow [image tagging](image-tagging.md).</span></span>

    ![Capture d’écran des options de marquage d’image](../media/content-understanding/admin-content-understanding-setup-image-tagging.png)</br>

5. <span data-ttu-id="c6663-127">Sur la page **configurer le traitement du formulaire** , vous pouvez choisir d’autoriser les utilisateurs à utiliser le générateur ai pour créer des modèles de traitement de formulaires dans des bibliothèques de documents SharePoint spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c6663-127">On the **Configure Form Processing** page, you can choose if you want to let users be able to use AI Builder to create form processing models in specific SharePoint document libraries.</span></span> <span data-ttu-id="c6663-128">Une option de menu est disponible dans le ruban bibliothèque de documents pour **créer un modèle de traitement de formulaire** dans les bibliothèques de documents SharePoint dans lesquelles il est activé.</span><span class="sxs-lookup"><span data-stu-id="c6663-128">A menu option will be available in the document library ribbon to **Create a form processing model** in SharePoint document libraries in which it is enabled.</span></span>
 
     <span data-ttu-id="c6663-129">Pour **que les bibliothèques SharePoint affichent l’option permettant de créer un modèle de traitement de formulaire**, vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="c6663-129">For **Which SharePoint libraries should show option to create a form processing model**, you can select:</span></span></br>
      - <span data-ttu-id="c6663-130">**Toutes les bibliothèques SharePoint** pour les mettre à la disposition de toutes les bibliothèques SharePoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c6663-130">**All SharePoint libraries** to make it available to all SharePoint libraries in your organization.</span></span></br>
      - <span data-ttu-id="c6663-131">**Uniquement les bibliothèques de sites sélectionnés**, puis sélectionnez les sites dans lesquels vous souhaitez les mettre à disposition.</span><span class="sxs-lookup"><span data-stu-id="c6663-131">**Only libraries in selected sites**, and then select the sites in which you want to make it available.</span></span></br>

   ![Configurer le traitement de formulaires](../media/content-understanding/admin-configforms.png)

   > [!Note]
   > <span data-ttu-id="c6663-133">L’activation de ce paramètre sur une bibliothèque de documents SharePoint n’affecte pas les modèles existants appliqués à la bibliothèque ou la possibilité d’appliquer des modèles de présentation de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c6663-133">Enabling this setting on a SharePoint document library does not affect existing models applied to the library or the ability to apply document understanding models to a library.</span></span> 
    
6. <span data-ttu-id="c6663-134">Sur la page **créer un centre de contenu** , vous pouvez créer un site Centre de contenu SharePoint sur lequel vos utilisateurs peuvent créer et gérer des modèles de présentation de documents.</span><span class="sxs-lookup"><span data-stu-id="c6663-134">On the **Create Content Center** page, you can create a SharePoint content center site on which your users can create and manage document understanding models.</span></span> </br>
    <span data-ttu-id="c6663-135">a.</span><span class="sxs-lookup"><span data-stu-id="c6663-135">a.</span></span> <span data-ttu-id="c6663-136">Pour **nom du site**, tapez le nom que vous souhaitez donner à votre site Centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="c6663-136">For **Site name**, type the name you want to give your content center site.</span></span></br>
    <span data-ttu-id="c6663-137">b.</span><span class="sxs-lookup"><span data-stu-id="c6663-137">b.</span></span> <span data-ttu-id="c6663-138">L' **adresse du site** indique l’URL de votre site, en fonction de ce que vous avez sélectionné pour le nom du site.</span><span class="sxs-lookup"><span data-stu-id="c6663-138">The **Site address** will show the URL for your site, based on what you selected for the site name.</span></span> <span data-ttu-id="c6663-139">Si vous souhaitez le modifier, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="c6663-139">If you want to change it, click **Edit**.</span></span></br>

      ![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</br>

    <span data-ttu-id="c6663-141">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6663-141">Select **Next**.</span></span>

7. <span data-ttu-id="c6663-142">Sur la page **révision et fin** , vous pouvez examiner le paramètre que vous avez sélectionné et choisir d’effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="c6663-142">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="c6663-143">Si vos sélections vous conviennent, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="c6663-143">If you are satisfied with your selections, select **Activate**.</span></span>

8. <span data-ttu-id="c6663-144">Sur la page confirmation, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c6663-144">On the confirmation page, click **Done**.</span></span>

9. <span data-ttu-id="c6663-145">Vous serez redirigé vers la page **automatiser le contenu** .</span><span class="sxs-lookup"><span data-stu-id="c6663-145">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="c6663-146">À partir de cette page, vous pouvez sélectionner **gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c6663-146">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="assign-licenses"></a><span data-ttu-id="c6663-147">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="c6663-147">Assign licenses</span></span>

<span data-ttu-id="c6663-148">Une fois que vous avez configuré SharePoint Syntex, vous devez attribuer des licences aux utilisateurs qui utiliseront les fonctionnalités de traitement de formulaire et de présentation des documents.</span><span class="sxs-lookup"><span data-stu-id="c6663-148">Once you have configured SharePoint Syntex, you must assign licenses for the users who will be using form processing and document understanding features.</span></span>

<span data-ttu-id="c6663-149">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="c6663-149">To assign licenses:</span></span>

1. <span data-ttu-id="c6663-150">Dans le centre d’administration 365 de Microsoft, sous **utilisateurs**, cliquez sur **utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="c6663-150">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="c6663-151">Sélectionnez les utilisateurs auxquels vous souhaitez accorder une licence, puis cliquez sur **gérer les licences des produits**.</span><span class="sxs-lookup"><span data-stu-id="c6663-151">Select the users that you want to license, and click **Manage product licenses**.</span></span>

3. <span data-ttu-id="c6663-152">Sélectionnez **attribuer plus**.</span><span class="sxs-lookup"><span data-stu-id="c6663-152">Select **Assign more**.</span></span>

4. <span data-ttu-id="c6663-153">Sélectionnez **services de contenu intelligents**.</span><span class="sxs-lookup"><span data-stu-id="c6663-153">Select **Intelligent Content Services**.</span></span> <span data-ttu-id="c6663-154">Sous **applications**, assurez-vous que **Common Data Service for intelligent content services** and **intelligent content services** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c6663-154">Under **Apps**, make sure **Common Data Service for Intelligent Content Services** and **Intelligent Content Services** are both selected.</span></span>

    ![Licences Syntex SharePoint dans le centre d’administration Microsoft 365](../media/content-understanding/sharepoint-syntex-licenses.png)

5. <span data-ttu-id="c6663-156">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="c6663-156">Click **Save changes**.</span></span>

## <a name="ai-builder-credits"></a><span data-ttu-id="c6663-157">Crédits du générateur AI</span><span class="sxs-lookup"><span data-stu-id="c6663-157">AI Builder credits</span></span>

<span data-ttu-id="c6663-158">Si vous disposez de 300 ou plus de licences Syntex SharePoint pour SharePoint Syntex dans votre organisation, vous serez affectées aux crédits du générateur de 1 million AI.</span><span class="sxs-lookup"><span data-stu-id="c6663-158">If you have 300 or more SharePoint Syntex licenses for SharePoint Syntex in your organization, you will be allocated one million AI Builder credits.</span></span> <span data-ttu-id="c6663-159">Si vous avez moins de 300 licences, vous devez acheter les crédits du générateur AI pour pouvoir utiliser le traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="c6663-159">If you have fewer than 300 licenses, you must purchase AI Builder credits in order to use forms processing.</span></span>

<span data-ttu-id="c6663-160">Vous pouvez estimer la capacité du générateur AI qui vous convient à l’aide de la [calculatrice du générateur ai](https://powerapps.microsoft.com/ai-builder-calculator).</span><span class="sxs-lookup"><span data-stu-id="c6663-160">You can estimate the AI Builder capacity that’s right for you with the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator).</span></span>

1. <span data-ttu-id="c6663-161">Accédez au [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/resources/capacity) pour vérifier vos crédits et l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c6663-161">Go to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/resources/capacity) to check your credits and usage.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6663-162">L’activation de ce paramètre sur une bibliothèque de documents SharePoint n’affecte pas les modèles existants appliqués à la bibliothèque ou la possibilité d’appliquer des modèles de présentation de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c6663-162">Enable this setting on a SharePoint document library does not affect existing models applied to the library or the ability to apply document understanding models to a library.</span></span> 
    
2. <span data-ttu-id="c6663-163">À partir de la page **créer un centre de contenu** , vous pouvez créer un site Centre de contenu SharePoint pour lequel les utilisateurs peuvent créer et gérer des modèles de présentation de documents.</span><span class="sxs-lookup"><span data-stu-id="c6663-163">From the **Create Content Center** page, you can create a SharePoint content center site for which users can create and manage document understanding models.</span></span> </br>
    <span data-ttu-id="c6663-164">a.</span><span class="sxs-lookup"><span data-stu-id="c6663-164">a.</span></span> <span data-ttu-id="c6663-165">Dans **nom du site**, tapez le nom que vous souhaitez pour le site du centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="c6663-165">For **Site name**, type the name you want for the content center site.</span></span></br>
    <span data-ttu-id="c6663-166">b.</span><span class="sxs-lookup"><span data-stu-id="c6663-166">b.</span></span> <span data-ttu-id="c6663-167">L' **adresse du site** indique l’URL de votre site, en fonction du nom du site.</span><span class="sxs-lookup"><span data-stu-id="c6663-167">The **Site address** shows the URL for your site, based on the site name.</span></span></br>

    > [!NOTE] 
    > <span data-ttu-id="c6663-168">Vous pouvez sélectionner n’importe quelle langue prise en charge, mais vous ne pouvez créer des modèles de présentation de contenu qu’en anglais.</span><span class="sxs-lookup"><span data-stu-id="c6663-168">While you can select any supported language, content understanding models can only be created for English.</span></span></br>

      ![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</br>

3. <span data-ttu-id="c6663-170">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6663-170">Select **Next**.</span></span>

4. <span data-ttu-id="c6663-171">Sur la page **Terminer et vérifier** , vérifiez le paramètre que vous avez sélectionné et choisissez d’effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="c6663-171">On the **Finish and review** page, look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="c6663-172">Si vos sélections vous conviennent, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="c6663-172">If you are satisfied with your selections, select **Activate**.</span></span>

5. <span data-ttu-id="c6663-173">La page **content Understanding Activated** s’affiche, confirmant que le système a ajouté vos préférences de traitement de formulaire et créé le site du centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="c6663-173">The **Content understanding activated** page displays, confirming the system added your form processing preferences and created the Content Center site.</span></span> <span data-ttu-id="c6663-174">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="c6663-174">Select **Done**.</span></span>

6. <span data-ttu-id="c6663-175">Vous serez redirigé vers la page **automatiser le contenu** .</span><span class="sxs-lookup"><span data-stu-id="c6663-175">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="c6663-176">À partir de cette page, vous pouvez sélectionner **gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c6663-176">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="see-also"></a><span data-ttu-id="c6663-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6663-177">See also</span></span>

[<span data-ttu-id="c6663-178">Vue d’ensemble du modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="c6663-178">Overview of the form processing model</span></span>](https://docs.microsoft.com/ai-builder/form-processing-model-overview)

[<span data-ttu-id="c6663-179">Procédure pas à pas : comment créer un modèle de présentation des documents (vidéo)</span><span class="sxs-lookup"><span data-stu-id="c6663-179">Step-by-Step: How to Build a Document Understanding Model (video)</span></span>](https://www.youtube.com/watch?v=DymSHObD-bg)

