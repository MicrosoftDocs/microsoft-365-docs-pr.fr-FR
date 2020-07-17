---
title: Déployer des compléments dans le centre d’administration
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 737e8c86-be63-44d7-bf02-492fa7cd9c3f
description: Découvrez comment déployer des compléments pour les utilisateurs et les groupes de votre organisation à l’aide du déploiement centralisé dans le centre d’administration.
ms.openlocfilehash: 4e9a3a4b7182bfd452c63abd03836623dc77260c
ms.sourcegitcommit: f7566dd6010744c72684efdc37f4471672330b61
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "45138243"
---
# <a name="deploy-add-ins-in-the-admin-center"></a><span data-ttu-id="4ccf4-103">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4ccf4-103">Deploy add-ins in the admin center</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="4ccf4-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-104">The admin center is changing.</span></span> <span data-ttu-id="4ccf4-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="4ccf4-106">[] Les compléments Office vous aident à personnaliser vos documents et à accéder plus simplement aux informations sur le web (voir [Commencer à utiliser votre complément Office](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-106">Office add-ins help you personalize your documents and streamline the way you access information on the web (see [Start using your Office Add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> <span data-ttu-id="4ccf4-107">En tant qu’administrateur, vous pouvez déployer des compléments Office pour les utilisateurs de votre organisation à l’aide de la fonctionnalité de déploiement centralisé dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-107">As an admin, you can deploy Office add-ins for the users in your organization by using the Centralized Deployment feature in the Microsoft 365 admin center.</span></span> <span data-ttu-id="4ccf4-108">Le déploiement centralisé est la méthode recommandée et la plus riche en fonctionnalités permettant à la plupart des administrateurs de déployer des compléments pour les utilisateurs et les groupes au sein d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-108">Centralized Deployment is the recommended and most feature-rich way for most admins to deploy add-ins to users and groups within an organization.</span></span> 

<span data-ttu-id="4ccf4-109">Pour plus d’informations sur la façon de déterminer si votre organisation peut prendre en charge le déploiement centralisé, reportez-vous à la rubrique [déterminer si un déploiement centralisé de compléments fonctionne pour votre organisation](centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-109">For more information on how to determine if your organization can support Centralized Deployment, see [Determine if Centralized Deployment of add-ins works for your organization](centralized-deployment-of-add-ins.md).</span></span>

<span data-ttu-id="4ccf4-110">Pour en savoir plus sur la gestion des compléments après le déploiement, consultez [la rubrique gestion des compléments dans le centre d’administration](manage-addins-in-the-admin-center.md) .</span><span class="sxs-lookup"><span data-stu-id="4ccf4-110">To learn more about managing add-ins after deployment, see [Manage add-ins in the admin center](manage-addins-in-the-admin-center.md)</span></span>
  
> [!NOTE]
>  <span data-ttu-id="4ccf4-111">Pour Word, Excel et PowerPoint utilisent un [catalogue d’applications SharePoint](https://dev.office.com/docs/add-ins/publish/publish-task-pane-and-content-add-ins-to-an-add-in-catalog) pour déployer des compléments pour les utilisateurs dans un environnement local sans connexion à Microsoft 365 et/ou prise en charge des compléments SharePoint requis.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-111">For Word, Excel and PowerPoint use a [SharePoint App Catalog](https://dev.office.com/docs/add-ins/publish/publish-task-pane-and-content-add-ins-to-an-add-in-catalog) to deploy add-ins to users in an on-premises environment with no connection to Microsoft 365 and/or support for SharePoint add-ins required.</span></span> <span data-ttu-id="4ccf4-112">Pour Outlook, utilisez le panneau de configuration Exchange pour déployer dans un environnement local sans connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-112">For Outlook use Exchange control panel to deploy in an on-premises environment without a connection to Microsoft 365.</span></span>
  
## <a name="recommended-approach-for-deploying-office-add-ins"></a><span data-ttu-id="4ccf4-113">Approche recommandée pour le déploiement de compléments Office</span><span class="sxs-lookup"><span data-stu-id="4ccf4-113">Recommended approach for deploying Office add-ins</span></span>

<span data-ttu-id="4ccf4-114">Pour déployer des compléments à l’aide d’une approche progressive, nous vous recommandons d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ccf4-114">To roll out add-ins by using a phased approach, we recommend the following:</span></span>
  
1. <span data-ttu-id="4ccf4-115">Déployez le complément vers un petit groupe de parties intéressées et de membres du service informatique.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-115">Roll out the add-in to a small set of business stakeholders and members of the IT department.</span></span> <span data-ttu-id="4ccf4-116">Si le déploiement réussit, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-116">If the deployment is successful, move to step 2.</span></span>
    
2. <span data-ttu-id="4ccf4-117">Déployez le complément à d’autres personnes au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-117">Roll out the add-in to more individuals within the business.</span></span> <span data-ttu-id="4ccf4-118">Une fois encore, évaluez les résultats et, si elle réussit, poursuivez le déploiement complet.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-118">Again, evaluate the results and, if successful, continue with full deployment.</span></span>
    
3. <span data-ttu-id="4ccf4-119">Effectuer un déploiement complet pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-119">Perform a full rollout to all users.</span></span>
    
<span data-ttu-id="4ccf4-120">En fonction de la taille de l’audience cible, vous pouvez ajouter ou supprimer des étapes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-120">Depending on the size of the target audience, you can add or remove roll-out steps.</span></span>
  
## <a name="deploy-an-office-add-in-using-the-admin-center"></a><span data-ttu-id="4ccf4-121">Déploiement d’un complément Office à l’aide du centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4ccf4-121">Deploy an Office add-in using the admin center</span></span>

<span data-ttu-id="4ccf4-122">Avant de commencer, consultez [la rubrique déterminer si un déploiement centralisé de compléments fonctionne pour votre organisation](centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-122">Before you begin, see [Determine if Centralized Deployment of add-ins works for your organization](centralized-deployment-of-add-ins.md).</span></span>
  
1. <span data-ttu-id="4ccf4-123">Dans le centre d’administration, accédez à **Settings** la \> page **compléments** de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-123">In the admin center, go to the **Settings** \> **Add-ins** page.</span></span>
    
2. <span data-ttu-id="4ccf4-124">Sélectionnez **déployer un complément** en haut de la page, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-124">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>
    
3. <span data-ttu-id="4ccf4-125">Sélectionnez une option et suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-125">Select an option and follow the instructions.</span></span>
  
4. <span data-ttu-id="4ccf4-126">Si vous avez sélectionné l’option d’ajout d’un complément à partir de l’Office Store, effectuez votre sélection de complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-126">If you selected the option to add an add-in from the Office Store, make your add-in selection.</span></span> </br>

    <span data-ttu-id="4ccf4-127">Vous pouvez afficher les compléments disponibles par catégories : **suggestions pour vous**, **évaluation**ou **nom**.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-127">You can view available add-ins by categories: **Suggested for you**, **Rating**, or **Name**.</span></span> <span data-ttu-id="4ccf4-128">Seuls les compléments gratuits sont disponibles dans l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-128">Only free add-ins are available from the Office Store.</span></span> <span data-ttu-id="4ccf4-129">Les compléments payants ne sont pas pris en charge pour le moment.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-129">Paid add-ins aren't supported currently.</span></span> <span data-ttu-id="4ccf4-130">Une fois que vous avez sélectionné un complément, acceptez les conditions requises pour continuer.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-130">After you select an add-in, accept the terms and conditions to proceed.</span></span> <br/> 

    > [!NOTE] 
    > <span data-ttu-id="4ccf4-131">Avec l’option Office Store, les mises à jour et les améliorations sont apportées automatiquement aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-131">With the Office Store option, updates and enhancements are automatically to users.</span></span>

5. <span data-ttu-id="4ccf4-132">Sur la page suivante, sélectionnez **Tout le monde**, **Utilisateurs/groupes spécifiques**ou **Moi uniquement** pour spécifier les personnes vers lesquelles le complément est déployé.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-132">On the next page, select **Everyone**, **Specific users/groups**, or **Just me** to specify who the add-in is deployed to.</span></span> <span data-ttu-id="4ccf4-133">Utilisez la zone de recherche pour rechercher des utilisateurs ou des groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-133">Use the Search box to find specific users or groups.</span></span> <br/>

    > [!NOTE] 
    > <span data-ttu-id="4ccf4-134">Pour en savoir plus sur les autres États qui s’appliquent à un complément, consultez la rubrique [États des compléments](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center.md).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-134">To learn about other states that apply to an add-in, see [Add-in states](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center.md).</span></span>
  
6. <span data-ttu-id="4ccf4-135">Sélectionnez **Déployer**.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-135">Select **Deploy**.</span></span>
  
7. <span data-ttu-id="4ccf4-136">Une coche verte apparaît lorsque le complément est déployé.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-136">A green tick appears when the add-in is deployed.</span></span> <span data-ttu-id="4ccf4-137">Suivez les instructions sur la page pour tester le complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-137">Follow the on-page instructions to test the add-in.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4ccf4-138">Il se peut que les utilisateurs doivent relancer Office pour afficher l’icône du complément sur le ruban de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-138">Users might need to relaunch Office to view the add-in icon on the app ribbon.</span></span> <span data-ttu-id="4ccf4-139">Les compléments Outlook peuvent prendre jusqu’à 24 heures pour apparaître sur les rubans des applications.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-139">Outlook add-ins can take up to 24 hours to appear on app ribbons.</span></span>
    
8. <span data-ttu-id="4ccf4-140">Lorsque vous avez terminé, sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-140">When finished, select **Next**.</span></span> <span data-ttu-id="4ccf4-141">Si vous avez déjà déployé, vous pouvez sélectionner Modifier les utilisateurs **qui ont accès au complément** pour le déployer sur un plus grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-141">If you've deployed to just yourself, you can select **Change who has access to add-in** to deploy to more users.</span></span>

    <span data-ttu-id="4ccf4-142">Si vous avez déployé le complément auprès d’autres membres de votre organisation, suivez les instructions pour annoncer le déploiement du complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-142">If you've deployed the add-in to other members of your organization, follow the instructions to announce the deployment of the add-in.</span></span> <br/>
  
    <span data-ttu-id="4ccf4-143">Il est recommandé d’informer les utilisateurs et les groupes que le complément déployé est disponible.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-143">It's good practice to inform users and groups that the deployed add-in is available.</span></span> <span data-ttu-id="4ccf4-144">Envisagez d’envoyer un courrier électronique qui décrit quand et comment utiliser le complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-144">Consider sending an email that describes when and how to use the add-in.</span></span> <span data-ttu-id="4ccf4-145">Inclure ou créer un lien vers du contenu d’aide ou des FAQ susceptibles d’aider les utilisateurs s’ils ont des problèmes avec le complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-145">Include or link to Help content or FAQs that might help users if they have problems with the add-in.</span></span>
  
### <a name="considerations-when-assigning-an-add-in-to-users-and-groups"></a><span data-ttu-id="4ccf4-146">Points à considérer lors de l'affectation d'un complément à des utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="4ccf4-146">Considerations when assigning an add-in to users and groups</span></span>

<span data-ttu-id="4ccf4-147">Les administrateurs peuvent affecter un complément à tout le monde ou à des utilisateurs et groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-147">Admins can assign an add-in to everyone or to specific users and groups.</span></span> <span data-ttu-id="4ccf4-148">Chaque option a des conséquences spécifiques :</span><span class="sxs-lookup"><span data-stu-id="4ccf4-148">Each option has implications:</span></span>
  
- <span data-ttu-id="4ccf4-149">**Tout le monde** Cette option affecte le complément à tous les utilisateurs de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-149">**Everyone** This option assigns the add-in to every user in the organization.</span></span> <span data-ttu-id="4ccf4-150">Utilisez-la avec parcimonie et uniquement pour les compléments qui sont réellement universels pour l'ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-150">Use this option sparingly and only for add-ins that are truly universal to your organization.</span></span> 
    
- <span data-ttu-id="4ccf4-151">**Les utilisateurs** Si vous affectez un complément à un utilisateur individuel, puis que vous déployez le complément sur un nouvel utilisateur, vous devez d’abord ajouter le nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-151">**Users** If you assign an add-in to an individual user, and then deploy the add-in to a new user, you must first add the new user.</span></span>
    
- <span data-ttu-id="4ccf4-152">**Groupes** Si vous affectez un complément à un groupe, le complément est automatiquement affecté aux utilisateurs qui sont ajoutés au groupe.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-152">**Groups** If you assign an add-in to a group, users who are added to the group are automatically assigned the add-in.</span></span> <span data-ttu-id="4ccf4-153">Lorsqu’un utilisateur est supprimé d’un groupe, il perd l’accès au complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-153">When a user is removed from a group, the user loses access to the add-in.</span></span> <span data-ttu-id="4ccf4-154">Dans les deux cas, aucune action supplémentaire n’est requise de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-154">In either case, no additional action is required from the admin.</span></span> 

- <span data-ttu-id="4ccf4-155">**Moi-même** Si vous affectez un complément à vous-même, le complément est affecté uniquement à votre compte, ce qui est idéal pour tester le complément.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-155">**Just me** If you assign an add-in to just yourself, the add-in is assigned to only your account, which is ideal for testing the add-in.</span></span>
    
<span data-ttu-id="4ccf4-156">L’option appropriée pour votre organisation dépend de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-156">The right option for your organization depends on your configuration.</span></span> <span data-ttu-id="4ccf4-157">Toutefois, nous vous recommandons d’utiliser des groupes.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-157">However, we recommend making assignments by using groups.</span></span> <span data-ttu-id="4ccf4-158">En tant qu’administrateur, vous pouvez trouver plus facile de gérer les compléments à l’aide de groupes et de contrôler l’appartenance à ces groupes plutôt que d’affecter des utilisateurs individuels à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-158">As an admin, you might find it easier to manage add-ins by using groups and controlling the membership of those groups rather than assigning individual users each time.</span></span> <span data-ttu-id="4ccf4-159">Dans certains cas, vous souhaiterez peut-être limiter l’accès à un petit ensemble d’utilisateurs en effectuant des affectations à des utilisateurs spécifiques en affectant manuellement les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-159">In some situations, you might want to restrict access to a small set of users by making assignments to specific users by assigning users manually.</span></span>
  
## <a name="more-about-office-add-ins-security"></a><span data-ttu-id="4ccf4-160">En savoir plus sur la sécurité des compléments Office</span><span class="sxs-lookup"><span data-stu-id="4ccf4-160">More about Office add-ins security</span></span>

<span data-ttu-id="4ccf4-p116">Les compléments Office combinent un fichier manifeste XML qui inclut certaines métadonnées sur le complément, mais surtout qui pointe vers une application web contenant tout le code et la logique. Les fonctionnalités des compléments peuvent varier. Par exemple, les compléments peuvent :</span><span class="sxs-lookup"><span data-stu-id="4ccf4-p116">Office add-ins combine an XML manifest file that contains some metadata about the add-in, but most importantly points to a web application which contains all the code and logic. Add-ins can range in their capabilities. For example, add-ins can:</span></span>
  
- <span data-ttu-id="4ccf4-164">afficher des données.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-164">Display data.</span></span>
    
- <span data-ttu-id="4ccf4-165">lire le document d'un utilisateur pour fournir des services contextuels.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-165">Read a user's document to provide contextual services.</span></span>
    
- <span data-ttu-id="4ccf4-166">lire et écrire des données vers le document d'un utilisateur et à partir de celui-ci pour fournir une valeur à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-166">Read and write data to and from a user's document to provide value to that user.</span></span>
    
<span data-ttu-id="4ccf4-167">Pour plus d'informations sur les types et fonctionnalités des compléments Office, voir [Vue d'ensemble de la plateforme des compléments Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins), notamment la section « Anatomie d'un complément Office ».</span><span class="sxs-lookup"><span data-stu-id="4ccf4-167">For more information about the types and capabilities of Office add-ins, see [Office Add-ins platform overview](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins), especially the section "Anatomy of an Office Add-in."</span></span>
  
<span data-ttu-id="4ccf4-p117">Pour interagir avec le document de l'utilisateur, le complément doit déclarer les autorisations dont il a besoin dans le fichier manifeste. Un modèle d'autorisations d'accès d'une API JavaScript à cinq niveaux fournit la base de la confidentialité et de la sécurité pour les utilisateurs des compléments du volet Office. La plupart des compléments de l'Office Store sont au niveau ReadWriteDocument. Presque tous les compléments prennent en charge le niveau ReadDocument au minimum. Pour plus d'informations sur les niveaux d'autorisation, voir [Demande d'autorisations pour l'utilisation d'API dans les compléments de contenu et du volet Office](https://docs.microsoft.com/office/dev/add-ins/develop/requesting-permissions-for-api-use-in-content-and-task-pane-add-ins).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-p117">To interact with the user's document, the add-in needs to declare what permission it needs in the manifest. A five-level JavaScript API access-permissions model provides the basis for privacy and security for users of task pane add-ins. The majority of the add-ins in the Office Store are level ReadWriteDocument with almost all add-ins supporting at least the ReadDocument level. For more information about the permission levels, see [Requesting permissions for API use in content and task pane add-ins](https://docs.microsoft.com/office/dev/add-ins/develop/requesting-permissions-for-api-use-in-content-and-task-pane-add-ins).</span></span>
  
<span data-ttu-id="4ccf4-p118">Lors de la mise à jour d'un manifeste, les modifications standard sont apportées à l'icône et au texte d'un complément. Les commandes de complément changent parfois, contrairement aux autorisations du complément. L'application web dans laquelle le code et la logique du complément sont exécutés peut changer à tout moment, ce qui est la nature même des applications web.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-p118">When updating a manifest, the typical changes are to an add-in's icon and text. Occasionally, add-in commands change. However, the permissions of the add-in do not change. The web application where all the code and logic for the add-in runs can change at any time, which is the nature of web applications.</span></span>
  
<span data-ttu-id="4ccf4-175">Les mises à jour des compléments se produisent comme suit :</span><span class="sxs-lookup"><span data-stu-id="4ccf4-175">Updates for add-ins happen as follows:</span></span>
  
- <span data-ttu-id="4ccf4-p119">**Complément métier :** dans ce cas, lorsqu'un administrateur a chargé explicitement un manifeste, le complément nécessite que l'administrateur charge un nouveau fichier manifeste pour prendre en charge la modification des métadonnées. Le complément est mis à jour au démarrage suivant des applications Office concernées. L'application web peut changer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-p119">**Line-of-business add-in:** In this case, where an admin explicitly uploaded a manifest, the add-in requires that the admin upload a new manifest file to support metadata changes. The next time the relevant Office applications start, the add-in will update. The web application can change at any time.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4ccf4-179">L’administrateur n’a pas besoin de supprimer un complément LOB pour effectuer une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-179">Admin does not need to remove a LOB Add-in for doing an update.</span></span>   <span data-ttu-id="4ccf4-180">Dans la section compléments, l’administrateur peut simplement cliquer sur le complément LOB et cliquer sur le **bouton mettre à jour** dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-180">In the Add-ins section, Admin can simply click on the LOB Add-in and choose the **Update Button** in the bottom right corner.</span></span> <span data-ttu-id="4ccf4-181">La mise à jour ne fonctionnera que si la version du nouveau complément est supérieure à celle du complément existant.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-181">Update will work only if the version of the new add-in is greater than that of the existing add-in.</span></span>   
    
- <span data-ttu-id="4ccf4-p121">**Complément de l'Office Store :** lorsqu'un administrateur a sélectionné un complément à partir de l'Office Store, si un complément est mis à jour dans l'Office Store, le complément sera mis à jour plus tard dans le déploiement centralisé. Le complément est mis à jour au démarrage suivant des applications Office concernées. L'application web peut changer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-p121">**Office Store add-in:** When an admin selected an add-in from the Office Store, if an add-in updates in the Office Store, the add-in will update later in Centralized Deployment. The next time the relevant Office applications start, the add-in will update. The web application can change at any time.</span></span> 
  
## <a name="learn-more"></a><span data-ttu-id="4ccf4-185">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="4ccf4-185">Learn more</span></span>

[<span data-ttu-id="4ccf4-186">Gérer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4ccf4-186">Manage add-ins in the admin center</span></span>](manage-addins-in-the-admin-center.md)

<span data-ttu-id="4ccf4-187">[Création de compléments Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins-fundamentals).</span><span class="sxs-lookup"><span data-stu-id="4ccf4-187">[Building Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins-fundamentals).</span></span>

[<span data-ttu-id="4ccf4-188">Mineurs et acquisition de compléments à partir du magasin</span><span class="sxs-lookup"><span data-stu-id="4ccf4-188">Minors and acquiring add-ins from the store</span></span>](minors-and-acquiring-addins-from-the-store.md)
  
[<span data-ttu-id="4ccf4-189">Utiliser les cmdlets PowerShell de déploiement centralisé pour gérer les compléments</span><span class="sxs-lookup"><span data-stu-id="4ccf4-189">Use Centralized Deployment PowerShell cmdlets to manage add-ins</span></span>](https://docs.microsoft.com/office365/enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins)
  
[<span data-ttu-id="4ccf4-190">Résolution des problèmes : l’utilisateur ne voit pas les compléments</span><span class="sxs-lookup"><span data-stu-id="4ccf4-190">Troubleshoot: User not seeing add-ins</span></span>](https://docs.microsoft.com/office365/troubleshoot/access-management/user-not-seeing-add-ins)
