---
title: Gérer des compléments dans le centre d’administration
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
description: Découvrez comment utiliser des compléments centralisés pour déployer des compléments pour les utilisateurs et les groupes de votre organisation.
ms.openlocfilehash: 6339858871834637c0b8fdd1b16c17b534026de9
ms.sourcegitcommit: e5ac81132cc5fd248350627a3cc7b3c640f53b6e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48207885"
---
# <a name="manage-add-ins-in-the-admin-center"></a><span data-ttu-id="f2469-103">Gérer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="f2469-103">Manage add-ins in the admin center</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="f2469-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="f2469-104">The admin center is changing.</span></span> <span data-ttu-id="f2469-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="f2469-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="f2469-106">Les compléments Office vous permettent de personnaliser vos documents et de rationaliser le mode d’accès aux informations sur le Web (voir [commencer à utiliser votre complément Office](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span><span class="sxs-lookup"><span data-stu-id="f2469-106">Office add-ins help you personalize your documents and streamline the way you access information on the web (see [Start using your Office add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> 

<span data-ttu-id="f2469-107">Une fois qu’un administrateur déploie des compléments pour les utilisateurs d’une organisation, l’administrateur peut désactiver ou activer les compléments, modifier, supprimer et gérer l’accès aux compléments.</span><span class="sxs-lookup"><span data-stu-id="f2469-107">After an admin deploys add-ins for users in an organization, the admin can turn add-ins off or on, edit, delete, and manage access to the add-ins.</span></span>

<span data-ttu-id="f2469-108">Pour plus d’informations sur l’installation des compléments à partir du centre d’administration, consultez [la rubrique deploy Add-ins in the Admin Center](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="f2469-108">For more information about installing add-ins from the admin center, see [Deploy add-ins in the admin center](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins).</span></span>
  
## <a name="add-in-states"></a><span data-ttu-id="f2469-109">États de complément</span><span class="sxs-lookup"><span data-stu-id="f2469-109">Add-in states</span></span>

<span data-ttu-id="f2469-110">Un complément peut avoir l’état **activé** ou **désactivé** .</span><span class="sxs-lookup"><span data-stu-id="f2469-110">An add-in can be in either the **On** or **Off** state.</span></span>
  
|<span data-ttu-id="f2469-111">**État**</span><span class="sxs-lookup"><span data-stu-id="f2469-111">**State**</span></span>|<span data-ttu-id="f2469-112">**Comment l'état se produit**</span><span class="sxs-lookup"><span data-stu-id="f2469-112">**How the state occurs**</span></span>|<span data-ttu-id="f2469-113">**Impact**</span><span class="sxs-lookup"><span data-stu-id="f2469-113">**Impact**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2469-114">**Active**</span><span class="sxs-lookup"><span data-stu-id="f2469-114">**Active**</span></span>  <br/> |<span data-ttu-id="f2469-115">Un administrateur a chargé le complément et l’a affecté à des utilisateurs ou à des groupes.</span><span class="sxs-lookup"><span data-stu-id="f2469-115">Admin uploaded the add-in and assigned it to users or groups.</span></span>  <br/> |<span data-ttu-id="f2469-116">Les utilisateurs et groupes auxquels le complément est affecté voient celui-ci dans les clients concernés.</span><span class="sxs-lookup"><span data-stu-id="f2469-116">Users and groups assigned to the add-in see it in the relevant clients.</span></span>  <br/> |
|<span data-ttu-id="f2469-117">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="f2469-117">**Turned off**</span></span>  <br/> |<span data-ttu-id="f2469-118">Un administrateur a désactivé le complément.</span><span class="sxs-lookup"><span data-stu-id="f2469-118">Admin turned off the add-in.</span></span>  <br/> |<span data-ttu-id="f2469-119">Les utilisateurs et les groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f2469-119">Users and groups assigned to the add-in no longer have access to it.</span></span>  <br/> <span data-ttu-id="f2469-120">Si l'état du complément est modifié en Actif, les utilisateurs et groupes ont de nouveau accès à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f2469-120">If the add-in state is changed to Active, the users and groups will have access to it again.</span></span>  <br/> |
|<span data-ttu-id="f2469-121">**Deleted**</span><span class="sxs-lookup"><span data-stu-id="f2469-121">**Deleted**</span></span>  <br/> |<span data-ttu-id="f2469-122">Un administrateur a supprimé le complément.</span><span class="sxs-lookup"><span data-stu-id="f2469-122">Admin deleted the add-in.</span></span>  <br/> |<span data-ttu-id="f2469-123">Les utilisateurs et groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f2469-123">Users and groups assigned the add-in no longer have access to it.</span></span>  <br/> |
   
<span data-ttu-id="f2469-124">Envisagez de supprimer un complément s’il n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="f2469-124">Consider deleting an add-in if no one is using it anymore.</span></span> <span data-ttu-id="f2469-125">Par exemple, la désactivation d’un complément peut être utile si un complément est utilisé uniquement à des moments spécifiques de l’année.</span><span class="sxs-lookup"><span data-stu-id="f2469-125">For example, turning off an add-in might make sense if an add-in is used only during specific times of the year.</span></span>

## <a name="delete-an-add-in"></a><span data-ttu-id="f2469-126">Suppression d’un complément</span><span class="sxs-lookup"><span data-stu-id="f2469-126">Delete an add-in</span></span>

<span data-ttu-id="f2469-127">Vous pouvez également supprimer un complément qui a été déployé.</span><span class="sxs-lookup"><span data-stu-id="f2469-127">You can also delete an add-in that was deployed.</span></span>

1. <span data-ttu-id="f2469-128">Dans le centre d’administration, accédez à la page **paramètres**de  >  **& des compléments** .</span><span class="sxs-lookup"><span data-stu-id="f2469-128">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="f2469-129">Le centre d’administration est mis à jour vers l’expérience de déploiement avec des applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="f2469-129">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="f2469-130">Si vous ne voyez pas les étapes ci-dessus, accédez à la section déploiement centralisé en accédant à **paramètres**  >  **intégrés**dans les applications.</span><span class="sxs-lookup"><span data-stu-id="f2469-130">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="f2469-131">En haut de la page **applications intégrées** , choisissez **compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-131">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="f2469-132">Sélectionnez le complément déployé.</span><span class="sxs-lookup"><span data-stu-id="f2469-132">Select the deployed add-in.</span></span>

3. <span data-ttu-id="f2469-133">Cliquez sur **supprimer le complément**.</span><span class="sxs-lookup"><span data-stu-id="f2469-133">Click on **Delete Add-In**.</span></span> <span data-ttu-id="f2469-134">Supprimez le bouton du complément dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="f2469-134">Remove the Add-in button on the bottom right corner.</span></span>

4. <span data-ttu-id="f2469-135">Validez vos sélections, puis sélectionnez **Supprimer le complément**.</span><span class="sxs-lookup"><span data-stu-id="f2469-135">Validate your selections, and choose **Remove add-in**.</span></span>

## <a name="edit-add-in-access"></a><span data-ttu-id="f2469-136">Modification de l’accès d’un complément</span><span class="sxs-lookup"><span data-stu-id="f2469-136">Edit add-in access</span></span>

<span data-ttu-id="f2469-137">Post-déploiement, les administrateurs peuvent également gérer l’accès des utilisateurs aux compléments.</span><span class="sxs-lookup"><span data-stu-id="f2469-137">Post deployment, admins can also manage user access to add-ins.</span></span>

1. <span data-ttu-id="f2469-138">Dans le centre d’administration, accédez à la page **paramètres**de  >  **& des compléments** .</span><span class="sxs-lookup"><span data-stu-id="f2469-138">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="f2469-139">Le centre d’administration est mis à jour vers l’expérience de déploiement avec des applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="f2469-139">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="f2469-140">Si vous ne voyez pas les étapes ci-dessus, accédez à la section déploiement centralisé en accédant à **paramètres**  >  **intégrés**dans les applications.</span><span class="sxs-lookup"><span data-stu-id="f2469-140">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="f2469-141">En haut de la page **applications intégrées** , choisissez **compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-141">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="f2469-142">Sélectionnez le complément déployé.</span><span class="sxs-lookup"><span data-stu-id="f2469-142">Select the deployed add-in.</span></span>

3. <span data-ttu-id="f2469-143">Cliquez sur **modifier** sous la rubrique **qui a accès**.</span><span class="sxs-lookup"><span data-stu-id="f2469-143">Click on **Edit** under **Who has Access**.</span></span>

4. <span data-ttu-id="f2469-144">Enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="f2469-144">Save the changes.</span></span>

## <a name="prevent-add-in-downloads-by-turning-off-the-office-store-across-all-clients-except-outlook"></a><span data-ttu-id="f2469-145">Empêcher les téléchargements de compléments en désactivant l’Office Store sur tous les clients (sauf Outlook)</span><span class="sxs-lookup"><span data-stu-id="f2469-145">Prevent add-in downloads by turning off the Office Store across all clients (Except Outlook)</span></span>

> [!NOTE]
> <span data-ttu-id="f2469-146">L’installation d’un complément Outlook est gérée par un [autre processus](https://technet.microsoft.com/library/jj943754%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2469-146">Outlook add-in installation is managed by a [different process](https://technet.microsoft.com/library/jj943754%28v=exchg.150%29.aspx).</span></span>

<span data-ttu-id="f2469-147">En tant qu’organisation, vous souhaiterez peut-être empêcher le téléchargement de nouveaux compléments Office à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="f2469-147">As an organization you may wish to prevent the download of new Office add-ins from the Office Store.</span></span> <span data-ttu-id="f2469-148">Il peut être utilisé conjointement avec un déploiement centralisé afin de s’assurer que seuls les compléments approuvés par l’organisation sont déployés pour les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f2469-148">This can be used in conjunction with Centralized Deployment to ensure that only organization-approved add-ins are deployed to users within your organization.</span></span>
  
<span data-ttu-id="f2469-149">**Pour désactiver l’acquisition du complément**</span><span class="sxs-lookup"><span data-stu-id="f2469-149">**To turn off add-in acquisition**</span></span>
  
1. <span data-ttu-id="f2469-150">Dans le centre d’administration, cliquez sur la page **Paramètres** \> [Services &amp; Compléments](https://go.microsoft.com/fwlink/p/?linkid=2053743).</span><span class="sxs-lookup"><span data-stu-id="f2469-150">In the admin center, go to the **Settings** \> [Services &amp; add-ins](https://go.microsoft.com/fwlink/p/?linkid=2053743) page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="f2469-151">Le centre d’administration est mis à jour vers l’expérience de déploiement avec des applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="f2469-151">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="f2469-152">Si vous ne voyez pas les étapes ci-dessus, accédez à la section déploiement centralisé en accédant à **paramètres**  >  **intégrés**dans les applications.</span><span class="sxs-lookup"><span data-stu-id="f2469-152">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="f2469-153">En haut de la page **applications intégrées** , choisissez **compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-153">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>
    
3. <span data-ttu-id="f2469-154">Sélectionnez **Applications et services appartenant aux utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f2469-154">Select **User owned apps and services**.</span></span>
    
4. <span data-ttu-id="f2469-155">Désactivez l’option pour permettre aux utilisateurs d’accéder à Office Store.</span><span class="sxs-lookup"><span data-stu-id="f2469-155">Clear the option to let users access the Office store.</span></span>

<span data-ttu-id="f2469-156">Cela empêchera tous les utilisateurs d’acquérir les compléments suivants à partir de la Banque.</span><span class="sxs-lookup"><span data-stu-id="f2469-156">This will prevent all users from acquiring the following add-ins from the store.</span></span>
  
- <span data-ttu-id="f2469-157">Compléments pour Word, Excel et PowerPoint 2016 à partir de :</span><span class="sxs-lookup"><span data-stu-id="f2469-157">Add-ins for Word, Excel, and PowerPoint 2016 from:</span></span>
    
  - <span data-ttu-id="f2469-158">Windows</span><span class="sxs-lookup"><span data-stu-id="f2469-158">Windows</span></span>
    
  - <span data-ttu-id="f2469-159">Mac</span><span class="sxs-lookup"><span data-stu-id="f2469-159">Mac</span></span>
    
  - <span data-ttu-id="f2469-160">Office</span><span class="sxs-lookup"><span data-stu-id="f2469-160">Office</span></span>
    
    
- <span data-ttu-id="f2469-161">Acquisitions à partir de **AppSource**</span><span class="sxs-lookup"><span data-stu-id="f2469-161">Acquisitions starting within **AppSource**</span></span>
    
- <span data-ttu-id="f2469-162">Compléments dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f2469-162">Add-ins within Microsoft 365</span></span>
    
<span data-ttu-id="f2469-163">Un utilisateur qui tente d’accéder au magasin verra apparaître le message suivant : « **Désolé, Microsoft 365 a été configuré pour empêcher l’acquisition individuelle de compléments de l’Office Store.**</span><span class="sxs-lookup"><span data-stu-id="f2469-163">A user who tries to access the store will see the following message: **Sorry, Microsoft 365 has been configured to prevent individual acquisition of Office Store add-ins.**</span></span>
  
<span data-ttu-id="f2469-164">La prise en charge de la désactivation de l’Office Store est disponible dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f2469-164">Support for turning off the Office Store is available in the following versions:</span></span>
  
- <span data-ttu-id="f2469-165">Windows : 16.0.9001 actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="f2469-165">Windows: 16.0.9001 - Currently available.</span></span>
    
- <span data-ttu-id="f2469-166">Mac : 16.10.18011401-actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="f2469-166">Mac: 16.10.18011401 - Currently available.</span></span>
    
- <span data-ttu-id="f2469-167">iOS : 2.9.18010804-actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="f2469-167">iOS: 2.9.18010804 - Currently available.</span></span>
    
- <span data-ttu-id="f2469-168">Le Web est actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="f2469-168">The web - Currently available.</span></span>
    
<span data-ttu-id="f2469-169">Cela n’empêche pas un administrateur d’utiliser un déploiement centralisé pour affecter un complément à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="f2469-169">This does not prevent an administrator from using Centralized Deployment to assign an add-in from the Office Store.</span></span>
  
<span data-ttu-id="f2469-170">Pour empêcher un utilisateur de se connecter à l’aide d’un compte Microsoft, vous pouvez limiter l’ouverture de session pour utiliser uniquement le compte d’organisation.</span><span class="sxs-lookup"><span data-stu-id="f2469-170">To prevent a user from signing in with a Microsoft account, you can restrict logon to use only the organizational account.</span></span> <span data-ttu-id="f2469-171">Pour plus d’informations, voir [identité, authentification et autorisation dans Office 2016](https://technet.microsoft.com/library/jj683102%28v=office.16%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2469-171">For more information, see [Identity, authentication, and authorization in Office 2016](https://technet.microsoft.com/library/jj683102%28v=office.16%29.aspx).</span></span>  

## <a name="more-about-the-end-user-experience-with-add-ins"></a><span data-ttu-id="f2469-172">En savoir plus sur l’expérience de l’utilisateur final avec les compléments</span><span class="sxs-lookup"><span data-stu-id="f2469-172">More about the end user experience with add-ins</span></span>

<span data-ttu-id="f2469-173">Une fois que vous avez déployé un complément, vos utilisateurs finaux peuvent commencer à l’utiliser dans leurs applications Office (voir [commencer à utiliser votre complément Office](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span><span class="sxs-lookup"><span data-stu-id="f2469-173">After you deploy an add-in, your end users can start using it in their Office applications (see [Start using your Office Add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> <span data-ttu-id="f2469-174">Le complément apparaît sur toutes les plateformes prises en charge par le complément.</span><span class="sxs-lookup"><span data-stu-id="f2469-174">The add-in appears on all platforms that the add-in supports.</span></span>
  
<span data-ttu-id="f2469-p110">Si le complément prend en charge les commandes de complément, celles-ci apparaissent sur le ruban Office. Dans l'exemple suivant, la commande **Search Citation** (Rechercher une citation) apparaît pour le complément **Citations**.</span><span class="sxs-lookup"><span data-stu-id="f2469-p110">If the add-in supports add-in commands, the commands appear on the Office ribbon. In the following example, the command **Search Citation** appears for the **Citations** add-in.</span></span> 

![Ruban Office avec des citations de recherche](../../media/553b0c0a-65e9-4746-b3b0-8c1b81715a86.png)
  
<span data-ttu-id="f2469-178">Si le complément déployé ne prend pas en charge les commandes de complément ou si vous souhaitez afficher tous les compléments déployés, vous pouvez les consulter via **mes compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-178">If the deployed add-in doesn't support add-in commands or if you want to view all deployed add-ins, you can view them via **My Add-ins**.</span></span> 
  
### <a name="in-word-2016-excel-2016-or-powerpoint-2016"></a><span data-ttu-id="f2469-179">Dans Word 2016, Excel 2016 ou PowerPoint 2016</span><span class="sxs-lookup"><span data-stu-id="f2469-179">In Word 2016, Excel 2016, or PowerPoint 2016</span></span>

1. <span data-ttu-id="f2469-180">Sélectionnez **insérer \> mes compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-180">Select **Insert \> My Add-ins**.</span></span> 
    
2. <span data-ttu-id="f2469-181">Sélectionnez l'onglet **Géré par l'administrateur** dans la fenêtre Compléments Office.</span><span class="sxs-lookup"><span data-stu-id="f2469-181">Select the **Admin Managed** tab in the Office Add-ins window.</span></span> 
    
3. <span data-ttu-id="f2469-182">Double-cliquez sur le complément que vous avez déployé précédemment (dans cet exemple, **Citations** ).</span><span class="sxs-lookup"><span data-stu-id="f2469-182">Double-click the add-in you deployed earlier (in this example, **Citations** ).</span></span> <br/><span data-ttu-id="f2469-183">![Onglet géré par l’administrateur de la page compléments Office](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span><span class="sxs-lookup"><span data-stu-id="f2469-183">![Admin Managed tab of the Office Add-ins page](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span></span>
  
### <a name="in-outlook"></a><span data-ttu-id="f2469-184">Dans Outlook</span><span class="sxs-lookup"><span data-stu-id="f2469-184">In Outlook</span></span>

1. <span data-ttu-id="f2469-185">Sur le ruban **Accueil** , sélectionnez **obtenir des compléments**.</span><span class="sxs-lookup"><span data-stu-id="f2469-185">On the **Home** ribbon, select **Get Add-ins**.</span></span><br/><span data-ttu-id="f2469-186">![Bouton Store dans Outlook](../../media/getaddinsicon.png)</span><span class="sxs-lookup"><span data-stu-id="f2469-186">![Store button in Outlook](../../media/getaddinsicon.png)</span></span>
  
2. <span data-ttu-id="f2469-187">Sélectionnez **Géré par l’administrateur** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="f2469-187">Select **Admin-managed** in the left nav.</span></span> 

## <a name="learn-more"></a><span data-ttu-id="f2469-188">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="f2469-188">Learn more</span></span>

[<span data-ttu-id="f2469-189">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="f2469-189">Deploy add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)

<span data-ttu-id="f2469-190">Pour en savoir plus sur la création et la génération de compléments, voir [Compléments Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins).</span><span class="sxs-lookup"><span data-stu-id="f2469-190">Learn more about creating and building [Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins).</span></span>
  
<span data-ttu-id="f2469-191">[Utilisez les cmdlets PowerShell de déploiement centralisé pour gérer les compléments](https://docs.microsoft.com/office365/enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins).</span><span class="sxs-lookup"><span data-stu-id="f2469-191">[Use Centralized Deployment PowerShell cmdlets to manage add-ins](https://docs.microsoft.com/office365/enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins).</span></span>
  
[<span data-ttu-id="f2469-192">Résolution des problèmes : l’utilisateur ne voit pas les compléments</span><span class="sxs-lookup"><span data-stu-id="f2469-192">Troubleshoot: User not seeing add-ins</span></span>](https://docs.microsoft.com/office365/troubleshoot/access-management/user-not-seeing-add-ins)

[<span data-ttu-id="f2469-193">Mineurs et acquisition de compléments à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f2469-193">Minors and acquiring add-ins from the Microsoft Store</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/minors-and-acquiring-addins-from-the-store)