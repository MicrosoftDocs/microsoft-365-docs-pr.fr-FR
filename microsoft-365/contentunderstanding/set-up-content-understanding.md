---
title: 'Configurer la présentation du contenu (aperçu) '
description: Comment configurer le projet cortex.
author: efrene
ms.author: efrene
manager: pamgreen
ms.date: 08/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: fca80e45dfa45ee5da9521854c6eebfbd87d8859
ms.sourcegitcommit: 91c82a79962387205c4dd4dd8d61322b79fed55f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2020
ms.locfileid: "46539904"
---
# <a name="set-up-content-understanding-preview"></a><span data-ttu-id="24308-103">Configurer la présentation du contenu (aperçu)</span><span class="sxs-lookup"><span data-stu-id="24308-103">Set up content understanding (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="24308-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="24308-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="24308-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="24308-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="24308-106">Les administrateurs peuvent utiliser le centre d’administration Microsoft 365 pour configurer et configurer la compréhension du contenu.</span><span class="sxs-lookup"><span data-stu-id="24308-106">Admins can use the Microsoft 365 admin center to set up and configure content understanding.</span></span> 

<span data-ttu-id="24308-107">Avant de procéder à l’installation, veillez à planifier la meilleure façon de configurer et de configurer la compréhension du contenu dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="24308-107">Prior to setup, make sure to plan for the best way to set up and configure content understanding in your environment.</span></span> <span data-ttu-id="24308-108">Par exemple, vous devez prendre en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="24308-108">For example, you will need to make considerations about the following:</span></span>
- <span data-ttu-id="24308-109">Quels sites SharePoint allez-vous activer le traitement de formulaires ?</span><span class="sxs-lookup"><span data-stu-id="24308-109">Which SharePoint sites will you enable form processing?</span></span> <span data-ttu-id="24308-110">Tous les sites, certains d’entre eux ou certains sites sélectionnés ?</span><span class="sxs-lookup"><span data-stu-id="24308-110">All of them, some, or select sites?</span></span>
- <span data-ttu-id="24308-111">Nom de votre centre de contenu, et qui est l’administrateur de site principal ?</span><span class="sxs-lookup"><span data-stu-id="24308-111">Name of your content center, and who is the primary site admin?</span></span>

<span data-ttu-id="24308-112">Un administrateur peut également modifier les paramètres sélectionnés à tout moment après l’installation par le biais des paramètres de présentation du contenu du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24308-112">An admin can also make changes to your selected settings anytime after setup through the content understanding management settings in the Microsoft 365 admin center.</span></span>


## <a name="requirements"></a><span data-ttu-id="24308-113">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="24308-113">Requirements</span></span> 
<span data-ttu-id="24308-114">Vous devez disposer d’autorisations d’administrateur général ou d’administrateur SharePoint pour pouvoir accéder au centre d’administration Microsoft 365 et configurer le mémorandum d’accord sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="24308-114">You must have Global Admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up content understanding.</span></span>


## <a name="to-set-up-content-understanding"></a><span data-ttu-id="24308-115">Pour configurer la présentation du contenu</span><span class="sxs-lookup"><span data-stu-id="24308-115">To set up content understanding</span></span>

1. <span data-ttu-id="24308-116">Dans le centre d’administration 365 de Microsoft, sélectionnez **configuration**, puis affichez la section connaissances de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="24308-116">In the Microsoft 365 admin center, select **Setup**, and then view the **Organizational knowledge** section.</span></span>
2. <span data-ttu-id="24308-117">Dans la section connaissances de l' **organisation** , sélectionnez **automatiser la compréhension du contenu**.</span><span class="sxs-lookup"><span data-stu-id="24308-117">In the **Organizational knowledge** section, select **Automate content understanding**.</span></span><br/>

    ![Page de configuration des connaissances organisationnelles](../media/content-understanding/admin-org-knowledge-options.png)</br>

3. <span data-ttu-id="24308-119">Sur la page **automatiser le contenu** , cliquez sur **prise en main** pour vous guider tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="24308-119">On the **Automate content understanding** page, click **Get started** to walk you through the setup process.</span></span><br/>

    ![Début de l’installation](../media/content-understanding/admin-content-understanding-get-started.png)</br>


4. <span data-ttu-id="24308-121">Sur la page **configurer le traitement du formulaire** , vous pouvez choisir d’autoriser les utilisateurs à utiliser le générateur ai pour créer des modèles de traitement de formulaires dans des bibliothèques de documents SharePoint spécifiques.</span><span class="sxs-lookup"><span data-stu-id="24308-121">On the **Configure Form Processing** page, you can choose if you want to let users be able to use AI Builder to create form processing models in specific SharePoint document libraries.</span></span> <span data-ttu-id="24308-122">Une option de menu est disponible dans le ruban bibliothèque de documents pour **créer un modèle de traitement de formulaire** dans les bibliothèques de documents SharePoint dans lesquelles il est activé.</span><span class="sxs-lookup"><span data-stu-id="24308-122">A menu option will be available in the document library ribbon to **Create a form processing model** in SharePoint document libraries in which it is enabled.</span></span>
 
     <span data-ttu-id="24308-123">Pour **que les bibliothèques SharePoint affichent l’option permettant de créer un modèle de traitement de formulaire**, vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="24308-123">For **Which SharePoint libraries should show option to create a form processing model**, you can select:</span></span></br>
    - <span data-ttu-id="24308-124">**Toutes les bibliothèques SharePoint** pour les mettre à la disposition de toutes les bibliothèques SharePoint dans votre client.</span><span class="sxs-lookup"><span data-stu-id="24308-124">**All SharePoint libraries** to make it available to all SharePoint libraries in your tenant.</span></span></br>
    - <span data-ttu-id="24308-125">**Uniquement les bibliothèques de sites sélectionnés**, puis sélectionnez les sites dans lesquels vous souhaitez les mettre à disposition.</span><span class="sxs-lookup"><span data-stu-id="24308-125">**Only libraries in selected sites**, and then select the sites in which you want to make it available.</span></span></br>
    - <span data-ttu-id="24308-126">**Aucune bibliothèque SharePoint** si vous ne souhaitez pas le mettre à la disposition de tous les sites (vous pouvez modifier ce paramètre après l’installation).</span><span class="sxs-lookup"><span data-stu-id="24308-126">**No SharePoint libraries** if you currently don't want to make it available to any sites (you can change this after setup).</span></span>
</br>

   <span data-ttu-id="24308-127">![Configurer le traitement de formulaires](../media/content-understanding/admin-configforms.png)
</span><span class="sxs-lookup"><span data-stu-id="24308-127">![Configure form processing](../media/content-understanding/admin-configforms.png)
</span></span></br>

   > [!Note]
   > <span data-ttu-id="24308-128">L’activation de ce paramètre sur une bibliothèque de documents SharePoint n’affecte pas les modèles existants appliqués à la bibliothèque ou la possibilité d’appliquer des modèles de présentation de document à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="24308-128">Enabling this setting on a SharePoint document library does not affect existing models applied to the library or the ability to apply document understanding models to a library.</span></span> 

    
5. <span data-ttu-id="24308-129">Sur la page **créer un centre de contenu** , vous pouvez créer un site Centre de contenu SharePoint sur lequel vos utilisateurs peuvent créer et gérer des modèles de présentation de documents.</span><span class="sxs-lookup"><span data-stu-id="24308-129">On the **Create Content Center** page, you can create a SharePoint content center site on which your users can create and manage document understanding models.</span></span> </br>
    <span data-ttu-id="24308-130">a.</span><span class="sxs-lookup"><span data-stu-id="24308-130">a.</span></span> <span data-ttu-id="24308-131">Pour **nom du site**, tapez le nom que vous souhaitez donner à votre site Centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="24308-131">For **Site name**, type the name you want to give your content center site.</span></span></br>
    <span data-ttu-id="24308-132">b.</span><span class="sxs-lookup"><span data-stu-id="24308-132">b.</span></span> <span data-ttu-id="24308-133">L' **adresse du site** indique l’URL de votre site, en fonction de ce que vous avez sélectionné pour le nom du site.</span><span class="sxs-lookup"><span data-stu-id="24308-133">The **Site address** will show the URL for your site, based on what you selected for the site name.</span></span></br>

    > [!Note] 
    > <span data-ttu-id="24308-134">Bien que vous puissiez sélectionner n’importe quelle langue prise en charge, Notez que les modèles de présentation du contenu ne peuvent être créés que pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="24308-134">While you can select any supported language, note that content understanding models can only be created for English.</span></span></br>

      ![Créer un centre de contenu](../media/content-understanding/admin-cu-create-cc.png)</br>


    <span data-ttu-id="24308-136">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="24308-136">Select **Next**.</span></span>
6. <span data-ttu-id="24308-137">Sur la page **Terminer et vérifier** , vous pouvez examiner le paramètre que vous avez sélectionné et choisir d’effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="24308-137">On the **Finish and review** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="24308-138">Si vos sélections vous conviennent, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="24308-138">If you are satisfied with your selections, select **Activate**.</span></span>



7. <span data-ttu-id="24308-139">La page **content Understanding activation** s’affiche, confirmant que le système a ajouté vos préférences de traitement de formulaire et créé le site du centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="24308-139">The **Content understanding activated** page will display, confirming that the system has added your form processing preferences and creating the Content Center site.</span></span> <span data-ttu-id="24308-140">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="24308-140">Select **Done**.</span></span>

8. <span data-ttu-id="24308-141">Vous serez redirigé vers la page **automatiser le contenu** .</span><span class="sxs-lookup"><span data-stu-id="24308-141">You'll be returned to your **Automate content understanding** page.</span></span> <span data-ttu-id="24308-142">À partir de cette page, vous pouvez sélectionner **gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="24308-142">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

## <a name="see-also"></a><span data-ttu-id="24308-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24308-143">See also</span></span>



  






