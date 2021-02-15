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
description: Découvrez comment utiliser des add-ins centralisés pour déployer des modules pour les utilisateurs et les groupes de votre organisation.
ms.openlocfilehash: 5366bd5be80559f23490aeb54f9417a189169e12
ms.sourcegitcommit: 0d709e9ab0d8d56c5fc11a921298f82e40e122c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50114200"
---
# <a name="manage-add-ins-in-the-admin-center"></a><span data-ttu-id="330ee-103">Gérer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="330ee-103">Manage add-ins in the admin center</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="330ee-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="330ee-104">The admin center is changing.</span></span> <span data-ttu-id="330ee-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="330ee-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="330ee-106">Les add-ins Office vous aident à personnaliser vos documents et à simplifier la façon dont vous accédez aux informations sur le web (voir Démarrer à l’aide de [votre application Office).](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)</span><span class="sxs-lookup"><span data-stu-id="330ee-106">Office add-ins help you personalize your documents and streamline the way you access information on the web (see [Start using your Office add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> 

<span data-ttu-id="330ee-107">Une fois qu’un administrateur a déployé des modules pour les utilisateurs d’une organisation, il peut désactiver ou activer les modules, modifier, supprimer et gérer l’accès aux modules.</span><span class="sxs-lookup"><span data-stu-id="330ee-107">After an admin deploys add-ins for users in an organization, the admin can turn add-ins off or on, edit, delete, and manage access to the add-ins.</span></span>

<span data-ttu-id="330ee-108">Pour plus d’informations sur l’installation des modules complémentaires à partir du Centre d’administration, voir Déployer des [modules complémentaires dans le Centre d’administration.](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)</span><span class="sxs-lookup"><span data-stu-id="330ee-108">For more information about installing add-ins from the admin center, see [Deploy add-ins in the admin center](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins).</span></span>
  
## <a name="add-in-states"></a><span data-ttu-id="330ee-109">États de complément</span><span class="sxs-lookup"><span data-stu-id="330ee-109">Add-in states</span></span>

<span data-ttu-id="330ee-110">Un add-in peut être à **l’état On** ou **Off.**</span><span class="sxs-lookup"><span data-stu-id="330ee-110">An add-in can be in either the **On** or **Off** state.</span></span>
  
|<span data-ttu-id="330ee-111">**État**</span><span class="sxs-lookup"><span data-stu-id="330ee-111">**State**</span></span>|<span data-ttu-id="330ee-112">**Comment l'état se produit**</span><span class="sxs-lookup"><span data-stu-id="330ee-112">**How the state occurs**</span></span>|<span data-ttu-id="330ee-113">**Impact**</span><span class="sxs-lookup"><span data-stu-id="330ee-113">**Impact**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="330ee-114">**Active**</span><span class="sxs-lookup"><span data-stu-id="330ee-114">**Active**</span></span>  <br/> |<span data-ttu-id="330ee-115">L’administrateur a chargé le module et l’a affecté à des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="330ee-115">Admin uploaded the add-in and assigned it to users or groups.</span></span>  <br/> |<span data-ttu-id="330ee-116">Les utilisateurs et groupes auxquels le complément est affecté voient celui-ci dans les clients concernés.</span><span class="sxs-lookup"><span data-stu-id="330ee-116">Users and groups assigned to the add-in see it in the relevant clients.</span></span>  <br/> |
|<span data-ttu-id="330ee-117">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="330ee-117">**Turned off**</span></span>  <br/> |<span data-ttu-id="330ee-118">Un administrateur a désactivé le complément.</span><span class="sxs-lookup"><span data-stu-id="330ee-118">Admin turned off the add-in.</span></span>  <br/> |<span data-ttu-id="330ee-119">Les utilisateurs et les groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="330ee-119">Users and groups assigned to the add-in no longer have access to it.</span></span>  <br/> <span data-ttu-id="330ee-120">Si l'état du complément est modifié en Actif, les utilisateurs et groupes ont de nouveau accès à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="330ee-120">If the add-in state is changed to Active, the users and groups will have access to it again.</span></span>  <br/> |
|<span data-ttu-id="330ee-121">**Deleted**</span><span class="sxs-lookup"><span data-stu-id="330ee-121">**Deleted**</span></span>  <br/> |<span data-ttu-id="330ee-122">Un administrateur a supprimé le complément.</span><span class="sxs-lookup"><span data-stu-id="330ee-122">Admin deleted the add-in.</span></span>  <br/> |<span data-ttu-id="330ee-123">Les utilisateurs et groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="330ee-123">Users and groups assigned the add-in no longer have access to it.</span></span>  <br/> |
   
<span data-ttu-id="330ee-124">Envisagez de supprimer un add-in si personne ne l’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="330ee-124">Consider deleting an add-in if no one is using it anymore.</span></span> <span data-ttu-id="330ee-125">Par exemple, la turning off an add-in might make sense if an add-in is used only during specific times of the year.</span><span class="sxs-lookup"><span data-stu-id="330ee-125">For example, turning off an add-in might make sense if an add-in is used only during specific times of the year.</span></span>

## <a name="delete-an-add-in"></a><span data-ttu-id="330ee-126">Suppression d’un complément</span><span class="sxs-lookup"><span data-stu-id="330ee-126">Delete an add-in</span></span>

<span data-ttu-id="330ee-127">Vous pouvez également supprimer un module qui a été déployé.</span><span class="sxs-lookup"><span data-stu-id="330ee-127">You can also delete an add-in that was deployed.</span></span>

1. <span data-ttu-id="330ee-128">Dans le Centre d’administration, allez à la page **Paramètres**  >  **Services & des modules.**</span><span class="sxs-lookup"><span data-stu-id="330ee-128">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="330ee-129">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="330ee-129">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="330ee-130">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="330ee-130">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="330ee-131">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="330ee-131">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="330ee-132">Sélectionnez le add-in déployé.</span><span class="sxs-lookup"><span data-stu-id="330ee-132">Select the deployed add-in.</span></span>

3. <span data-ttu-id="330ee-133">Cliquez sur **Supprimer le add-in.**</span><span class="sxs-lookup"><span data-stu-id="330ee-133">Click on **Delete Add-In**.</span></span> <span data-ttu-id="330ee-134">Supprimez le bouton du complément dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="330ee-134">Remove the Add-in button on the bottom right corner.</span></span>

4. <span data-ttu-id="330ee-135">Validez vos sélections, puis sélectionnez **Supprimer le complément**.</span><span class="sxs-lookup"><span data-stu-id="330ee-135">Validate your selections, and choose **Remove add-in**.</span></span>

## <a name="edit-add-in-access"></a><span data-ttu-id="330ee-136">Modification de l’accès d’un complément</span><span class="sxs-lookup"><span data-stu-id="330ee-136">Edit add-in access</span></span>

<span data-ttu-id="330ee-137">Après le déploiement, les administrateurs peuvent également gérer l’accès des utilisateurs aux add-ins.</span><span class="sxs-lookup"><span data-stu-id="330ee-137">Post deployment, admins can also manage user access to add-ins.</span></span>

1. <span data-ttu-id="330ee-138">Dans le Centre d’administration, allez à la page **Paramètres**  >  **Services & des modules.**</span><span class="sxs-lookup"><span data-stu-id="330ee-138">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="330ee-139">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="330ee-139">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="330ee-140">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="330ee-140">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="330ee-141">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="330ee-141">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="330ee-142">Sélectionnez le add-in déployé.</span><span class="sxs-lookup"><span data-stu-id="330ee-142">Select the deployed add-in.</span></span>

3. <span data-ttu-id="330ee-143">Cliquez sur **Modifier sous** Qui **a accès**.</span><span class="sxs-lookup"><span data-stu-id="330ee-143">Click on **Edit** under **Who has Access**.</span></span>

4. <span data-ttu-id="330ee-144">Enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="330ee-144">Save the changes.</span></span>

## <a name="prevent-add-in-downloads-by-turning-off-the-office-store-across-all-clients-except-outlook"></a><span data-ttu-id="330ee-145">Empêcher les téléchargements de modules de l’Office Store sur tous les clients (à l’exception d’Outlook)</span><span class="sxs-lookup"><span data-stu-id="330ee-145">Prevent add-in downloads by turning off the Office Store across all clients (Except Outlook)</span></span>

> [!NOTE]
> <span data-ttu-id="330ee-146">L’installation du add-in Outlook est gérée par [un processus différent.](https://technet.microsoft.com/library/jj943754%28v=exchg.150%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="330ee-146">Outlook add-in installation is managed by a [different process](https://technet.microsoft.com/library/jj943754%28v=exchg.150%29.aspx).</span></span>

<span data-ttu-id="330ee-147">En tant qu’organisation, vous pouvez empêcher le téléchargement de nouveaux modules office à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="330ee-147">As an organization you may wish to prevent the download of new Office add-ins from the Office Store.</span></span> <span data-ttu-id="330ee-148">Cela peut être utilisé conjointement avec le déploiement centralisé pour vous assurer que seuls les compléments approuvés par l’organisation sont déployés pour les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="330ee-148">This can be used in conjunction with Centralized Deployment to ensure that only organization-approved add-ins are deployed to users within your organization.</span></span>
  
<span data-ttu-id="330ee-149">**Pour désactiver l’acquisition d’un add-in**</span><span class="sxs-lookup"><span data-stu-id="330ee-149">**To turn off add-in acquisition**</span></span>
  
1. <span data-ttu-id="330ee-150">Dans le centre d’administration, cliquez sur la page **Paramètres** \> [Services &amp; Compléments](https://go.microsoft.com/fwlink/p/?linkid=2053743).</span><span class="sxs-lookup"><span data-stu-id="330ee-150">In the admin center, go to the **Settings** \> [Services &amp; add-ins](https://go.microsoft.com/fwlink/p/?linkid=2053743) page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="330ee-151">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="330ee-151">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="330ee-152">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="330ee-152">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="330ee-153">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="330ee-153">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>
    
3. <span data-ttu-id="330ee-154">Sélectionnez **Applications et services appartenant aux utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="330ee-154">Select **User owned apps and services**.</span></span>
    
4. <span data-ttu-id="330ee-155">Désactivez l’option pour permettre aux utilisateurs d’accéder à Office Store.</span><span class="sxs-lookup"><span data-stu-id="330ee-155">Clear the option to let users access the Office store.</span></span>

<span data-ttu-id="330ee-156">Cela empêche tous les utilisateurs d’acquérir les modules suivants dans le Store.</span><span class="sxs-lookup"><span data-stu-id="330ee-156">This will prevent all users from acquiring the following add-ins from the store.</span></span>
  
- <span data-ttu-id="330ee-157">Les add-ins pour Word, Excel et PowerPoint 2016 à partir de :</span><span class="sxs-lookup"><span data-stu-id="330ee-157">Add-ins for Word, Excel, and PowerPoint 2016 from:</span></span>
    
  - <span data-ttu-id="330ee-158">Windows</span><span class="sxs-lookup"><span data-stu-id="330ee-158">Windows</span></span>
    
  - <span data-ttu-id="330ee-159">Mac</span><span class="sxs-lookup"><span data-stu-id="330ee-159">Mac</span></span>
    
  - <span data-ttu-id="330ee-160">Office</span><span class="sxs-lookup"><span data-stu-id="330ee-160">Office</span></span>
    
    
- <span data-ttu-id="330ee-161">Acquisitions à partir **d’AppSource**</span><span class="sxs-lookup"><span data-stu-id="330ee-161">Acquisitions starting within **AppSource**</span></span>
    
- <span data-ttu-id="330ee-162">Les add-ins dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="330ee-162">Add-ins within Microsoft 365</span></span>
    
<span data-ttu-id="330ee-163">Un utilisateur qui tente d’accéder à l’Office Store voit le message suivant : **Désolé, Microsoft 365** a été configuré pour empêcher l’acquisition individuelle de modules de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="330ee-163">A user who tries to access the store will see the following message: **Sorry, Microsoft 365 has been configured to prevent individual acquisition of Office Store add-ins.**</span></span>
  
<span data-ttu-id="330ee-164">La prise en charge de la non-prise en charge de l’Office Store est disponible dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="330ee-164">Support for turning off the Office Store is available in the following versions:</span></span>
  
- <span data-ttu-id="330ee-165">Windows : 16.0.9001 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="330ee-165">Windows: 16.0.9001 - Currently available.</span></span>
    
- <span data-ttu-id="330ee-166">Mac : 16.10.18011401 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="330ee-166">Mac: 16.10.18011401 - Currently available.</span></span>
    
- <span data-ttu-id="330ee-167">iOS : 2.9.18010804 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="330ee-167">iOS: 2.9.18010804 - Currently available.</span></span>
    
- <span data-ttu-id="330ee-168">Le site web - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="330ee-168">The web - Currently available.</span></span>
    
<span data-ttu-id="330ee-169">Cela n’empêche pas un administrateur d’utiliser le déploiement centralisé pour affecter un add-in à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="330ee-169">This does not prevent an administrator from using Centralized Deployment to assign an add-in from the Office Store.</span></span>
  
<span data-ttu-id="330ee-170">Pour empêcher un utilisateur de se signer avec un compte Microsoft, vous pouvez restreindre l’accès pour utiliser uniquement le compte d’organisation.</span><span class="sxs-lookup"><span data-stu-id="330ee-170">To prevent a user from signing in with a Microsoft account, you can restrict logon to use only the organizational account.</span></span> <span data-ttu-id="330ee-171">Pour plus d’informations, [voir Identité, authentification et autorisation dans Office 2016.](https://technet.microsoft.com/library/jj683102%28v=office.16%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="330ee-171">For more information, see [Identity, authentication, and authorization in Office 2016](https://technet.microsoft.com/library/jj683102%28v=office.16%29.aspx).</span></span>  

> [!NOTE]
> <span data-ttu-id="330ee-172">Le fait d’empêcher les utilisateurs d’accéder à l’Office Store les empêchera également de recharger une version test des [add-ins Office.](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)</span><span class="sxs-lookup"><span data-stu-id="330ee-172">Preventing users from accessing the office store will also prevent them from [Sideloading Office Add-ins for testing](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins).</span></span>

## <a name="more-about-the-end-user-experience-with-add-ins"></a><span data-ttu-id="330ee-173">En savoir plus sur l’expérience de l’utilisateur final avec les add-ins</span><span class="sxs-lookup"><span data-stu-id="330ee-173">More about the end user experience with add-ins</span></span>

<span data-ttu-id="330ee-174">Après avoir déployé un application, vos utilisateurs finaux peuvent commencer à l’utiliser dans leurs applications Office (voir Démarrer à l’aide de [votre application Office).](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)</span><span class="sxs-lookup"><span data-stu-id="330ee-174">After you deploy an add-in, your end users can start using it in their Office applications (see [Start using your Office Add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> <span data-ttu-id="330ee-175">Le add-in apparaît sur toutes les plateformes qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="330ee-175">The add-in appears on all platforms that the add-in supports.</span></span>
  
<span data-ttu-id="330ee-p110">Si le complément prend en charge les commandes de complément, celles-ci apparaissent sur le ruban Office. Dans l'exemple suivant, la commande **Search Citation** (Rechercher une citation) apparaît pour le complément **Citations**.</span><span class="sxs-lookup"><span data-stu-id="330ee-p110">If the add-in supports add-in commands, the commands appear on the Office ribbon. In the following example, the command **Search Citation** appears for the **Citations** add-in.</span></span> 

![Ruban Office avec citations de recherche](../../media/553b0c0a-65e9-4746-b3b0-8c1b81715a86.png)
  
<span data-ttu-id="330ee-179">Si le add-in déployé ne prend pas en charge les commandes de add-in ou si vous souhaitez afficher tous les modules, vous pouvez les afficher via Mes **modules.**</span><span class="sxs-lookup"><span data-stu-id="330ee-179">If the deployed add-in doesn't support add-in commands or if you want to view all deployed add-ins, you can view them via **My Add-ins**.</span></span> 
  
### <a name="in-word-2016-excel-2016-or-powerpoint-2016"></a><span data-ttu-id="330ee-180">Dans Word 2016, Excel 2016 ou PowerPoint 2016</span><span class="sxs-lookup"><span data-stu-id="330ee-180">In Word 2016, Excel 2016, or PowerPoint 2016</span></span>

1. <span data-ttu-id="330ee-181">Sélectionnez **\> Insérer mes modules.**</span><span class="sxs-lookup"><span data-stu-id="330ee-181">Select **Insert \> My Add-ins**.</span></span> 
    
2. <span data-ttu-id="330ee-182">Sélectionnez l'onglet **Géré par l'administrateur** dans la fenêtre Compléments Office.</span><span class="sxs-lookup"><span data-stu-id="330ee-182">Select the **Admin Managed** tab in the Office Add-ins window.</span></span> 
    
3. <span data-ttu-id="330ee-183">Double-cliquez sur le complément que vous avez déployé précédemment (dans cet exemple, **Citations** ).</span><span class="sxs-lookup"><span data-stu-id="330ee-183">Double-click the add-in you deployed earlier (in this example, **Citations** ).</span></span> <br/><span data-ttu-id="330ee-184">![Onglet Géré par l’administrateur de la page Des add-ins Office](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span><span class="sxs-lookup"><span data-stu-id="330ee-184">![Admin Managed tab of the Office Add-ins page](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span></span>
  
### <a name="in-outlook"></a><span data-ttu-id="330ee-185">Dans Outlook</span><span class="sxs-lookup"><span data-stu-id="330ee-185">In Outlook</span></span>

1. <span data-ttu-id="330ee-186">Dans le **ruban Accueil,** **sélectionnez Obtenir des modules.**</span><span class="sxs-lookup"><span data-stu-id="330ee-186">On the **Home** ribbon, select **Get Add-ins**.</span></span><br/><span data-ttu-id="330ee-187">![Bouton Store dans Outlook](../../media/getaddinsicon.png)</span><span class="sxs-lookup"><span data-stu-id="330ee-187">![Store button in Outlook](../../media/getaddinsicon.png)</span></span>
  
2. <span data-ttu-id="330ee-188">Sélectionnez **Géré par l’administrateur** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="330ee-188">Select **Admin-managed** in the left nav.</span></span> 

## <a name="learn-more"></a><span data-ttu-id="330ee-189">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="330ee-189">Learn more</span></span>

[<span data-ttu-id="330ee-190">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="330ee-190">Deploy add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)

<span data-ttu-id="330ee-191">Pour en savoir plus sur la création et la génération de compléments, voir [Compléments Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins).</span><span class="sxs-lookup"><span data-stu-id="330ee-191">Learn more about creating and building [Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins).</span></span>
  
<span data-ttu-id="330ee-192">[Utilisez les cmdlets PowerShell de déploiement centralisé pour gérer les add-ins.](https://docs.microsoft.com/office365/enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins)</span><span class="sxs-lookup"><span data-stu-id="330ee-192">[Use Centralized Deployment PowerShell cmdlets to manage add-ins](https://docs.microsoft.com/office365/enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins).</span></span>
  
[<span data-ttu-id="330ee-193">Résolution des problèmes : l’utilisateur ne voit pas les modules</span><span class="sxs-lookup"><span data-stu-id="330ee-193">Troubleshoot: User not seeing add-ins</span></span>](https://docs.microsoft.com/office365/troubleshoot/access-management/user-not-seeing-add-ins)

[<span data-ttu-id="330ee-194">Mineurs et acquisition de add-ins à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="330ee-194">Minors and acquiring add-ins from the Microsoft Store</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/minors-and-acquiring-addins-from-the-store)
