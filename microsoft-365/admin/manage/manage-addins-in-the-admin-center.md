---
title: Gérer des compléments dans le centre d’administration
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
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
ms.openlocfilehash: 8503ed7ea2e088a8e17b52e619ee999aa05f497a
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51579289"
---
# <a name="manage-add-ins-in-the-admin-center"></a><span data-ttu-id="27a6a-103">Gérer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="27a6a-103">Manage add-ins in the admin center</span></span>

<span data-ttu-id="27a6a-104">Les add-ins Office vous aident à personnaliser vos documents et à simplifier la façon dont vous accédez aux informations sur le web (voir Démarrer à l’aide de [votre application Office).](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)</span><span class="sxs-lookup"><span data-stu-id="27a6a-104">Office add-ins help you personalize your documents and streamline the way you access information on the web (see [Start using your Office add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> 

<span data-ttu-id="27a6a-105">Une fois qu’un administrateur a déployé des modules pour les utilisateurs d’une organisation, il peut désactiver ou activer les modules, modifier, supprimer et gérer l’accès aux modules.</span><span class="sxs-lookup"><span data-stu-id="27a6a-105">After an admin deploys add-ins for users in an organization, the admin can turn add-ins off or on, edit, delete, and manage access to the add-ins.</span></span>

<span data-ttu-id="27a6a-106">Pour plus d’informations sur l’installation des modules complémentaires à partir du Centre d’administration, voir Déployer des [modules complémentaires dans le Centre d’administration.](./manage-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="27a6a-106">For more information about installing add-ins from the admin center, see [Deploy add-ins in the admin center](./manage-deployment-of-add-ins.md).</span></span>
  
## <a name="add-in-states"></a><span data-ttu-id="27a6a-107">États de complément</span><span class="sxs-lookup"><span data-stu-id="27a6a-107">Add-in states</span></span>

<span data-ttu-id="27a6a-108">Un add-in peut être à **l’état On** ou **Off.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-108">An add-in can be in either the **On** or **Off** state.</span></span>
  
|<span data-ttu-id="27a6a-109">**État**</span><span class="sxs-lookup"><span data-stu-id="27a6a-109">**State**</span></span>|<span data-ttu-id="27a6a-110">**Comment l'état se produit**</span><span class="sxs-lookup"><span data-stu-id="27a6a-110">**How the state occurs**</span></span>|<span data-ttu-id="27a6a-111">**Impact**</span><span class="sxs-lookup"><span data-stu-id="27a6a-111">**Impact**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27a6a-112">**Active**</span><span class="sxs-lookup"><span data-stu-id="27a6a-112">**Active**</span></span>  <br/> |<span data-ttu-id="27a6a-113">L’administrateur a chargé le module et l’a affecté à des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="27a6a-113">Admin uploaded the add-in and assigned it to users or groups.</span></span>  <br/> |<span data-ttu-id="27a6a-114">Les utilisateurs et groupes auxquels le complément est affecté voient celui-ci dans les clients concernés.</span><span class="sxs-lookup"><span data-stu-id="27a6a-114">Users and groups assigned to the add-in see it in the relevant clients.</span></span>  <br/> |
|<span data-ttu-id="27a6a-115">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="27a6a-115">**Turned off**</span></span>  <br/> |<span data-ttu-id="27a6a-116">Un administrateur a désactivé le complément.</span><span class="sxs-lookup"><span data-stu-id="27a6a-116">Admin turned off the add-in.</span></span>  <br/> |<span data-ttu-id="27a6a-117">Les utilisateurs et les groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="27a6a-117">Users and groups assigned to the add-in no longer have access to it.</span></span>  <br/> <span data-ttu-id="27a6a-118">Si l'état du complément est modifié en Actif, les utilisateurs et groupes ont de nouveau accès à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="27a6a-118">If the add-in state is changed to Active, the users and groups will have access to it again.</span></span>  <br/> |
|<span data-ttu-id="27a6a-119">**Deleted**</span><span class="sxs-lookup"><span data-stu-id="27a6a-119">**Deleted**</span></span>  <br/> |<span data-ttu-id="27a6a-120">Un administrateur a supprimé le complément.</span><span class="sxs-lookup"><span data-stu-id="27a6a-120">Admin deleted the add-in.</span></span>  <br/> |<span data-ttu-id="27a6a-121">Les utilisateurs et groupes auxquels le complément est affecté ne peuvent plus accéder à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="27a6a-121">Users and groups assigned the add-in no longer have access to it.</span></span>  <br/> |
   
<span data-ttu-id="27a6a-122">Envisagez de supprimer un add-in si personne ne l’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="27a6a-122">Consider deleting an add-in if no one is using it anymore.</span></span> <span data-ttu-id="27a6a-123">Par exemple, la turning off an add-in might make sense if an add-in is used only during specific times of the year.</span><span class="sxs-lookup"><span data-stu-id="27a6a-123">For example, turning off an add-in might make sense if an add-in is used only during specific times of the year.</span></span>

## <a name="delete-an-add-in"></a><span data-ttu-id="27a6a-124">Suppression d’un complément</span><span class="sxs-lookup"><span data-stu-id="27a6a-124">Delete an add-in</span></span>

<span data-ttu-id="27a6a-125">Vous pouvez également supprimer un module qui a été déployé.</span><span class="sxs-lookup"><span data-stu-id="27a6a-125">You can also delete an add-in that was deployed.</span></span>

1. <span data-ttu-id="27a6a-126">Dans le Centre d’administration, allez sur la page **Paramètres**  >  **Services & des modules.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-126">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="27a6a-127">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="27a6a-127">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="27a6a-128">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-128">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="27a6a-129">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-129">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="27a6a-130">Sélectionnez le add-in déployé.</span><span class="sxs-lookup"><span data-stu-id="27a6a-130">Select the deployed add-in.</span></span>

3. <span data-ttu-id="27a6a-131">Cliquez sur **Supprimer le add-in.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-131">Click on **Delete Add-In**.</span></span> <span data-ttu-id="27a6a-132">Supprimez le bouton du complément dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="27a6a-132">Remove the Add-in button on the bottom right corner.</span></span>

4. <span data-ttu-id="27a6a-133">Validez vos sélections, puis sélectionnez **Supprimer le complément**.</span><span class="sxs-lookup"><span data-stu-id="27a6a-133">Validate your selections, and choose **Remove add-in**.</span></span>

## <a name="edit-add-in-access"></a><span data-ttu-id="27a6a-134">Modification de l’accès d’un complément</span><span class="sxs-lookup"><span data-stu-id="27a6a-134">Edit add-in access</span></span>

<span data-ttu-id="27a6a-135">Après le déploiement, les administrateurs peuvent également gérer l’accès des utilisateurs aux add-ins.</span><span class="sxs-lookup"><span data-stu-id="27a6a-135">Post deployment, admins can also manage user access to add-ins.</span></span>

1. <span data-ttu-id="27a6a-136">Dans le Centre d’administration, allez sur la page **Paramètres**  >  **Services & des modules.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-136">In the admin center, go to the **Settings** > **Services & add-ins** page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="27a6a-137">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="27a6a-137">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="27a6a-138">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-138">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="27a6a-139">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-139">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>

2. <span data-ttu-id="27a6a-140">Sélectionnez le add-in déployé.</span><span class="sxs-lookup"><span data-stu-id="27a6a-140">Select the deployed add-in.</span></span>

3. <span data-ttu-id="27a6a-141">Cliquez sur **Modifier sous** Qui **a accès**.</span><span class="sxs-lookup"><span data-stu-id="27a6a-141">Click on **Edit** under **Who has Access**.</span></span>

4. <span data-ttu-id="27a6a-142">Enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="27a6a-142">Save the changes.</span></span>

## <a name="prevent-add-in-downloads-by-turning-off-the-office-store-across-all-clients-except-outlook"></a><span data-ttu-id="27a6a-143">Empêcher les téléchargements de modules de l’Office Store sur tous les clients (à l’exception d’Outlook)</span><span class="sxs-lookup"><span data-stu-id="27a6a-143">Prevent add-in downloads by turning off the Office Store across all clients (Except Outlook)</span></span>

> [!NOTE]
> <span data-ttu-id="27a6a-144">L’installation du add-in Outlook est gérée par [un processus différent.](/exchange/clients-and-mobile-in-exchange-online/add-ins-for-outlook/specify-who-can-install-and-manage-add-ins)</span><span class="sxs-lookup"><span data-stu-id="27a6a-144">Outlook add-in installation is managed by a [different process](/exchange/clients-and-mobile-in-exchange-online/add-ins-for-outlook/specify-who-can-install-and-manage-add-ins).</span></span>

<span data-ttu-id="27a6a-145">En tant qu’organisation, vous pouvez empêcher le téléchargement de nouveaux modules office à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="27a6a-145">As an organization you may wish to prevent the download of new Office add-ins from the Office Store.</span></span> <span data-ttu-id="27a6a-146">Cela peut être utilisé conjointement avec le déploiement centralisé pour vous assurer que seuls les compléments approuvés par l’organisation sont déployés pour les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="27a6a-146">This can be used in conjunction with Centralized Deployment to ensure that only organization-approved add-ins are deployed to users within your organization.</span></span>
  
<span data-ttu-id="27a6a-147">**Pour désactiver l’acquisition d’un add-in**</span><span class="sxs-lookup"><span data-stu-id="27a6a-147">**To turn off add-in acquisition**</span></span>
  
1. <span data-ttu-id="27a6a-148">Dans le centre d’administration, cliquez sur la page **Paramètres** \> [Services &amp; Compléments](https://go.microsoft.com/fwlink/p/?linkid=2053743).</span><span class="sxs-lookup"><span data-stu-id="27a6a-148">In the admin center, go to the **Settings** \> [Services &amp; add-ins](https://go.microsoft.com/fwlink/p/?linkid=2053743) page.</span></span>

     > [!NOTE]
    > <span data-ttu-id="27a6a-149">Le Centre d’administration est mis à jour vers l’expérience de déploiement avec les applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="27a6a-149">The admin center is getting updated to deployment experience with Integrated Apps .</span></span> <span data-ttu-id="27a6a-150">Si vous ne voyez pas les étapes ci-dessus, consultez la section Déploiement centralisé en allant dans **Applications intégrées**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-150">If you don't see the above steps, go to Centralized Deployment section by going to **Settings** > **Integrated apps**.</span></span> <span data-ttu-id="27a6a-151">En haut de la page **Applications intégrées,** choisissez **Les applications.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-151">On the top of the **Integrated apps** page, choose **Add-ins**.</span></span>
    
3. <span data-ttu-id="27a6a-152">Sélectionnez **Applications et services appartenant aux utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="27a6a-152">Select **User owned apps and services**.</span></span>
    
4. <span data-ttu-id="27a6a-153">Désactivez l’option pour permettre aux utilisateurs d’accéder à Office Store.</span><span class="sxs-lookup"><span data-stu-id="27a6a-153">Clear the option to let users access the Office store.</span></span>

<span data-ttu-id="27a6a-154">Cela empêche tous les utilisateurs d’acquérir les modules suivants dans le Store.</span><span class="sxs-lookup"><span data-stu-id="27a6a-154">This will prevent all users from acquiring the following add-ins from the store.</span></span>
  
- <span data-ttu-id="27a6a-155">Les add-ins pour Word, Excel et PowerPoint 2016 à partir de :</span><span class="sxs-lookup"><span data-stu-id="27a6a-155">Add-ins for Word, Excel, and PowerPoint 2016 from:</span></span>
    
  - <span data-ttu-id="27a6a-156">Windows</span><span class="sxs-lookup"><span data-stu-id="27a6a-156">Windows</span></span>
    
  - <span data-ttu-id="27a6a-157">Mac</span><span class="sxs-lookup"><span data-stu-id="27a6a-157">Mac</span></span>
    
  - <span data-ttu-id="27a6a-158">Office</span><span class="sxs-lookup"><span data-stu-id="27a6a-158">Office</span></span>
    
    
- <span data-ttu-id="27a6a-159">Acquisitions à partir **d’AppSource**</span><span class="sxs-lookup"><span data-stu-id="27a6a-159">Acquisitions starting within **AppSource**</span></span>
    
- <span data-ttu-id="27a6a-160">Add-ins within Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="27a6a-160">Add-ins within Microsoft 365</span></span>
    
<span data-ttu-id="27a6a-161">Un utilisateur qui tente d’accéder à l’Office Store voit le message suivant : **Désolé, Microsoft 365** a été configuré pour empêcher l’acquisition individuelle de modules de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="27a6a-161">A user who tries to access the store will see the following message: **Sorry, Microsoft 365 has been configured to prevent individual acquisition of Office Store add-ins.**</span></span>
  
<span data-ttu-id="27a6a-162">La prise en charge de la non-prise en charge de l’Office Store est disponible dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="27a6a-162">Support for turning off the Office Store is available in the following versions:</span></span>
  
- <span data-ttu-id="27a6a-163">Windows : 16.0.9001 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="27a6a-163">Windows: 16.0.9001 - Currently available.</span></span>
    
- <span data-ttu-id="27a6a-164">Mac : 16.10.18011401 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="27a6a-164">Mac: 16.10.18011401 - Currently available.</span></span>
    
- <span data-ttu-id="27a6a-165">iOS : 2.9.18010804 - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="27a6a-165">iOS: 2.9.18010804 - Currently available.</span></span>
    
- <span data-ttu-id="27a6a-166">Le site web - Actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="27a6a-166">The web - Currently available.</span></span>
    
<span data-ttu-id="27a6a-167">Cela n’empêche pas un administrateur d’utiliser le déploiement centralisé pour affecter un add-in à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="27a6a-167">This does not prevent an administrator from using Centralized Deployment to assign an add-in from the Office Store.</span></span>
  
<span data-ttu-id="27a6a-168">Pour empêcher un utilisateur de se signer avec un compte Microsoft, vous pouvez restreindre l’accès pour utiliser uniquement le compte d’organisation.</span><span class="sxs-lookup"><span data-stu-id="27a6a-168">To prevent a user from signing in with a Microsoft account, you can restrict logon to use only the organizational account.</span></span> <span data-ttu-id="27a6a-169">Pour plus d’informations, [voir Identité, authentification et autorisation dans Office 2016.](/DeployOffice/security/identity-authentication-and-authorization-in-office)</span><span class="sxs-lookup"><span data-stu-id="27a6a-169">For more information, see [Identity, authentication, and authorization in Office 2016](/DeployOffice/security/identity-authentication-and-authorization-in-office).</span></span>  

> [!NOTE]
> <span data-ttu-id="27a6a-170">Le fait d’empêcher les utilisateurs d’accéder à l’Office Store les empêchera également de recharger une version test des [add-ins Office.](/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)</span><span class="sxs-lookup"><span data-stu-id="27a6a-170">Preventing users from accessing the office store will also prevent them from [Sideloading Office Add-ins for testing](/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins).</span></span>

## <a name="more-about-the-end-user-experience-with-add-ins"></a><span data-ttu-id="27a6a-171">En savoir plus sur l’expérience de l’utilisateur final avec les add-ins</span><span class="sxs-lookup"><span data-stu-id="27a6a-171">More about the end user experience with add-ins</span></span>

<span data-ttu-id="27a6a-172">Après avoir déployé un application, vos utilisateurs finaux peuvent commencer à l’utiliser dans leurs applications Office (voir Démarrer à l’aide de [votre application Office).](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)</span><span class="sxs-lookup"><span data-stu-id="27a6a-172">After you deploy an add-in, your end users can start using it in their Office applications (see [Start using your Office Add-in](https://support.microsoft.com/office/82e665c4-6700-4b56-a3f3-ef5441996862)).</span></span> <span data-ttu-id="27a6a-173">Le add-in apparaît sur toutes les plateformes qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="27a6a-173">The add-in appears on all platforms that the add-in supports.</span></span>
  
<span data-ttu-id="27a6a-p109">Si le complément prend en charge les commandes de complément, celles-ci apparaissent sur le ruban Office. Dans l'exemple suivant, la commande **Search Citation** (Rechercher une citation) apparaît pour le complément **Citations**.</span><span class="sxs-lookup"><span data-stu-id="27a6a-p109">If the add-in supports add-in commands, the commands appear on the Office ribbon. In the following example, the command **Search Citation** appears for the **Citations** add-in.</span></span> 

![Ruban Office avec citations de recherche](../../media/553b0c0a-65e9-4746-b3b0-8c1b81715a86.png)
  
<span data-ttu-id="27a6a-177">Si le add-in déployé ne prend pas en charge les commandes de ce dernier ou si vous souhaitez afficher tous les modules, vous pouvez les afficher via Mes **modules.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-177">If the deployed add-in doesn't support add-in commands or if you want to view all deployed add-ins, you can view them via **My Add-ins**.</span></span> 
  
### <a name="in-word-2016-excel-2016-or-powerpoint-2016"></a><span data-ttu-id="27a6a-178">Dans Word 2016, Excel 2016 ou PowerPoint 2016</span><span class="sxs-lookup"><span data-stu-id="27a6a-178">In Word 2016, Excel 2016, or PowerPoint 2016</span></span>

1. <span data-ttu-id="27a6a-179">Sélectionnez **\> Insérer mes modules.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-179">Select **Insert \> My Add-ins**.</span></span> 
    
2. <span data-ttu-id="27a6a-180">Sélectionnez l'onglet **Géré par l'administrateur** dans la fenêtre Compléments Office.</span><span class="sxs-lookup"><span data-stu-id="27a6a-180">Select the **Admin Managed** tab in the Office Add-ins window.</span></span> 
    
3. <span data-ttu-id="27a6a-181">Double-cliquez sur le complément que vous avez déployé précédemment (dans cet exemple, **Citations** ).</span><span class="sxs-lookup"><span data-stu-id="27a6a-181">Double-click the add-in you deployed earlier (in this example, **Citations** ).</span></span> <br/><span data-ttu-id="27a6a-182">![Onglet Géré par l’administrateur de la page Des add-ins Office](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span><span class="sxs-lookup"><span data-stu-id="27a6a-182">![Admin Managed tab of the Office Add-ins page](../../media/fd36ba81-9882-40f0-9fce-74f991aa97d5.png)</span></span>
  
### <a name="in-outlook"></a><span data-ttu-id="27a6a-183">Dans Outlook</span><span class="sxs-lookup"><span data-stu-id="27a6a-183">In Outlook</span></span>

1. <span data-ttu-id="27a6a-184">Dans le **ruban Accueil,** **sélectionnez Obtenir des modules.**</span><span class="sxs-lookup"><span data-stu-id="27a6a-184">On the **Home** ribbon, select **Get Add-ins**.</span></span><br/><span data-ttu-id="27a6a-185">![Bouton Store dans Outlook](../../media/getaddinsicon.png)</span><span class="sxs-lookup"><span data-stu-id="27a6a-185">![Store button in Outlook](../../media/getaddinsicon.png)</span></span>
  
2. <span data-ttu-id="27a6a-186">Sélectionnez **Géré par l’administrateur** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="27a6a-186">Select **Admin-managed** in the left nav.</span></span> 

## <a name="learn-more"></a><span data-ttu-id="27a6a-187">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="27a6a-187">Learn more</span></span>

[<span data-ttu-id="27a6a-188">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="27a6a-188">Deploy add-ins in the admin center</span></span>](./manage-deployment-of-add-ins.md)

<span data-ttu-id="27a6a-189">Pour en savoir plus sur la création et la génération de compléments, voir [Compléments Office](/office/dev/add-ins/overview/office-add-ins).</span><span class="sxs-lookup"><span data-stu-id="27a6a-189">Learn more about creating and building [Office Add-ins](/office/dev/add-ins/overview/office-add-ins).</span></span>
  
<span data-ttu-id="27a6a-190">[Utilisez les cmdlets PowerShell de déploiement centralisé pour gérer les add-ins.](../../enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="27a6a-190">[Use Centralized Deployment PowerShell cmdlets to manage add-ins](../../enterprise/use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins.md).</span></span>
  
[<span data-ttu-id="27a6a-191">Résolution des problèmes : l’utilisateur ne voit pas les modules</span><span class="sxs-lookup"><span data-stu-id="27a6a-191">Troubleshoot: User not seeing add-ins</span></span>](/office365/troubleshoot/access-management/user-not-seeing-add-ins)

[<span data-ttu-id="27a6a-192">Mineurs et acquisition de add-ins à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="27a6a-192">Minors and acquiring add-ins from the Microsoft Store</span></span>](./minors-and-acquiring-addins-from-the-store.md)