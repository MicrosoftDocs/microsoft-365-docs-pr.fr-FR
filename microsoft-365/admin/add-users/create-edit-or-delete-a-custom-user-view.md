---
title: Créer, modifier ou supprimer une vue utilisateur personnalisée dans Office 365
f1.keywords:
- NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 4fe7f6ac-be8e-4b57-9e13-24ff889a4b28
description: Apprenez à utiliser des filtres pour créer, modifier ou supprimer des affichages utilisateur personnalisés dans Office 365.
ms.openlocfilehash: ba03d3da3e8bfdc4f2a661d1dc59845a8a22609f
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239392"
---
# <a name="create-edit-or-delete-a-custom-user-view-in-office-365"></a><span data-ttu-id="beeaa-103">Créer, modifier ou supprimer une vue utilisateur personnalisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="beeaa-103">Create, edit, or delete a custom user view in Office 365</span></span>

<span data-ttu-id="beeaa-104">Si vous êtes un administrateur général ou un administrateur de gestion des utilisateurs d’Office 365, vous pouvez créer des affichages utilisateur personnalisés pour afficher un sous-ensemble spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="beeaa-104">If you're a global or user management admin of Office 365, you can create custom user views to view a specific subset of users.</span></span> <span data-ttu-id="beeaa-105">Ces affichages s’ajoutent à l’ensemble standard de vues fournies avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="beeaa-105">These views are in addition to the standard set of views that come with Office 365.</span></span> <span data-ttu-id="beeaa-106">Vous pouvez créer, modifier ou supprimer des affichages utilisateur personnalisés, et les vues personnalisées que vous créez sont disponibles pour tous les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="beeaa-106">You can create, edit, or delete custom user views, and the custom views you create are available to all admins.</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="beeaa-107">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="beeaa-107">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

::: moniker-end
  
## <a name="custom-user-views-in-the-admin-center"></a><span data-ttu-id="beeaa-108">Vues utilisateur personnalisées dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="beeaa-108">Custom user views in the admin center</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="beeaa-109">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications s’affichent dans la liste de **filtres** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="beeaa-109">When you create, edit, or delete a custom user view, the changes will be shown in the **Filter** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="beeaa-110">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="beeaa-110">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="beeaa-111">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications apparaissent dans la liste des **affichages** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="beeaa-111">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="beeaa-112">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="beeaa-112">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="beeaa-113">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications apparaissent dans la liste des **affichages** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="beeaa-113">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="beeaa-114">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="beeaa-114">You can create up to 50 custom views.</span></span> 

::: moniker-end

> [!TIP]
>  <span data-ttu-id="beeaa-115">Les affichages standard des utilisateurs sont affichés par défaut dans la liste déroulante **filtres** .</span><span class="sxs-lookup"><span data-stu-id="beeaa-115">Standard user views are displayed by default in the **Filters** drop-down list.</span></span> <span data-ttu-id="beeaa-116">Les filtres standard incluent **tous les utilisateurs**, **les utilisateurs sous licence**, **les utilisateurs invités**, la **connexion autorisée**, les **utilisateurs**qui ne disposent **pas de**licence, les **utilisateurs avec des erreurs, les administrateurs de** **facturation**, les administrateurs **globaux**, les administrateurs de service d' **assistance**, les administrateurs de **service**et les administrateurs de **gestion des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-116">The standard filters include **All users**, **Licensed users**, **Guest users**,  **Sign-in allowed**, **Sign-in blocked**, **Unlicensed users**, **Users with errors**, **Billing admins**, **Global admins**, **Helpdesk admins**, **Service admins**, and **User management admins**.</span></span> <span data-ttu-id="beeaa-117">Vous ne pouvez pas modifier ou supprimer des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="beeaa-117">You can't edit or delete standard views.</span></span> 

<span data-ttu-id="beeaa-118">Voici quelques points à noter concernant les vues standard :</span><span class="sxs-lookup"><span data-stu-id="beeaa-118">A few things to note about standard views:</span></span> 

- <span data-ttu-id="beeaa-119">Certains affichages standard affichent une liste non triée s’il y a plus de 2 000 utilisateurs dans la liste.</span><span class="sxs-lookup"><span data-stu-id="beeaa-119">Some standard views display an unsorted list if there are more than 2,000 users in the list.</span></span> <span data-ttu-id="beeaa-120">Pour rechercher des utilisateurs spécifiques dans cette liste, utilisez la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="beeaa-120">To locate specific users in this list, use the search box.</span></span> 
- <span data-ttu-id="beeaa-121">Si vous n’avez pas acheté Office 365 auprès de Microsoft, les **administrateurs de facturation** n’apparaissent pas dans la liste des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="beeaa-121">If you didn't purchase Office 365 from Microsoft, **Billing admins** don't appear in the standard views list.</span></span> <span data-ttu-id="beeaa-122">Pour plus d'informations, consultez la rubrique [Affectation de rôles d'administrateur](assign-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="beeaa-122">For more information, see [Assigning admin roles](assign-admin-roles.md).</span></span> 
  
## <a name="choose-the-filters-for-your-custom-user-view"></a><span data-ttu-id="beeaa-123">Choisir les filtres pour votre vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="beeaa-123">Choose the filters for your custom user view</span></span>

<span data-ttu-id="beeaa-124">Vous pouvez créer et modifier vos affichages personnalisés dans le volet **filtre personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="beeaa-124">You can create and edit your custom views in the **Custom filter** pane.</span></span> <span data-ttu-id="beeaa-125">Si vous sélectionnez plusieurs options de filtre, vous obtenez des résultats qui contiennent les utilisateurs qui répondent à tous les critères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="beeaa-125">If you select multiple filter options, you get results that contain users who match all the selected criteria.</span></span> <span data-ttu-id="beeaa-126">L’exemple suivant montre comment créer une vue personnalisée nommée « Users canadien » qui affiche tous les utilisateurs d’un domaine spécifique au Canada.</span><span class="sxs-lookup"><span data-stu-id="beeaa-126">The following example shows you how to create a custom view named "Canadian users" that shows all users on a specific domain who are in Canada.</span></span> 

  
 <span data-ttu-id="beeaa-127">**A-domaine** Si votre organisation dispose de plusieurs domaines, vous pouvez choisir dans une liste déroulante des domaines disponibles.</span><span class="sxs-lookup"><span data-stu-id="beeaa-127">**A - Domain** If you have multiple domains for your organization, you can choose from a drop-down list of domains that are available.</span></span> 
  
 <span data-ttu-id="beeaa-128">**B-état de connexion** Choisissez les utilisateurs autorisés ou bloqués.</span><span class="sxs-lookup"><span data-stu-id="beeaa-128">**B - Sign-in status** Choose users that are allowed or blocked.</span></span> 
  
 <span data-ttu-id="beeaa-129">**Emplacement C** Choisissez un emplacement dans une liste déroulante de pays.</span><span class="sxs-lookup"><span data-stu-id="beeaa-129">**C - Location** Choose a location from a drop-down list of countries.</span></span> 
  
 <span data-ttu-id="beeaa-130">**D-licence de produit attribuée** Faites votre choix dans la liste déroulante des licences disponibles dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="beeaa-130">**D - Assigned product license** Choose from a drop-down list of licenses that are available at your organization.</span></span> <span data-ttu-id="beeaa-131">Utilisez ce filtre pour montrer aux utilisateurs qui disposent de la licence que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="beeaa-131">Use this filter to show users who have the license you selected assigned to them.</span></span> <span data-ttu-id="beeaa-132">Les utilisateurs peuvent également avoir des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="beeaa-132">Users may also have additional licenses.</span></span> 
  
<span data-ttu-id="beeaa-133">Vous pouvez également filtrer par des détails de profil utilisateur supplémentaires utilisés dans votre organisation, tels que service, ville, État ou province, pays ou région, ou fonction.</span><span class="sxs-lookup"><span data-stu-id="beeaa-133">You can also filter by additional user profile details used in your organization such as department, city, state or province, country or region, or job title.</span></span>
  
 <span data-ttu-id="beeaa-134">**Autres conditions :**</span><span class="sxs-lookup"><span data-stu-id="beeaa-134">**Other conditions:**</span></span>
  
- <span data-ttu-id="beeaa-135">**Utilisateurs synchronisés uniquement** Activez cette case à cocher pour afficher tous les utilisateurs qui ont été synchronisés avec l’annuaire Active Directory local, que les utilisateurs aient été activés ou non.</span><span class="sxs-lookup"><span data-stu-id="beeaa-135">**Synchronized users only** Select this box to show all users who have been synced with the local Active Directory, regardless of whether the users have been activated or not.</span></span> 
    
- <span data-ttu-id="beeaa-136">**Utilisateurs avec des erreurs** Activez cette case à cocher pour afficher les utilisateurs qui peuvent avoir des erreurs de mise en service.</span><span class="sxs-lookup"><span data-stu-id="beeaa-136">**Users with errors** Select this box to show users who may have provisioning errors.</span></span> 
    
- <span data-ttu-id="beeaa-137">**Utilisateurs sans licence** Activez cette case à cocher pour rechercher tous les utilisateurs qui n’ont pas reçu de licence.</span><span class="sxs-lookup"><span data-stu-id="beeaa-137">**Unlicensed users** Select this box to find all the users who haven't been assigned a license.</span></span> <span data-ttu-id="beeaa-138">Les résultats de cette vue peuvent également inclure des utilisateurs qui disposent d’une boîte aux lettres Exchange mais qui n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="beeaa-138">The results for this view can also include users who have an Exchange mailbox but don't have a license.</span></span> <span data-ttu-id="beeaa-139">Pour effectuer le suivi de ces utilisateurs en particulier, utilisez le filtre **utilisateurs sans licence avec des boîtes aux lettres ou des archives Exchange**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-139">To track those users specifically, use the filter **Unlicensed users with Exchange mailboxes or archives**.</span></span> <span data-ttu-id="beeaa-140">Les résultats de cette vue peuvent également inclure des utilisateurs qui disposent d’une archive Exchange, mais qui n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="beeaa-140">The results for this view can also include users who have an Exchange archive, but don't have a license.</span></span>
    
- <span data-ttu-id="beeaa-141">**Utilisateurs sans licence avec des boîtes aux lettres ou des archives Exchange** Activez cette case à cocher pour afficher les comptes d’utilisateur qui ont été créés dans Exchange Online et qui disposent d’une boîte aux lettres Exchange, mais auxquels aucune licence Office 365 n’a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="beeaa-141">**Unlicensed users with Exchange mailboxes or archives** Select this box to show user accounts that were created in Exchange Online and have an Exchange mailbox, but weren't assigned an Office 365 license.</span></span> <span data-ttu-id="beeaa-142">Les résultats de ce filtre incluent les utilisateurs qui disposent ou non d’une archive Exchange.</span><span class="sxs-lookup"><span data-stu-id="beeaa-142">The results of this filter include users who have or who were assigned an Exchange archive.</span></span> 
    
> [!TIP]
> <span data-ttu-id="beeaa-143">Si vous créez un affichage personnalisé qui renvoie plus de 2 000 utilisateurs, la liste d’utilisateurs obtenue n’est pas triée.</span><span class="sxs-lookup"><span data-stu-id="beeaa-143">If you create a custom view that returns more than 2,000 users, the resulting user list isn't sorted.</span></span> <span data-ttu-id="beeaa-144">Dans ce cas, utilisez la zone de recherche pour rechercher des utilisateurs ou modifier votre vue personnalisée pour affiner votre recherche.</span><span class="sxs-lookup"><span data-stu-id="beeaa-144">In this case, use the search box to find users or edit your custom view to refine your search.</span></span> 
  
## <a name="create-a-custom-user-view"></a><span data-ttu-id="beeaa-145">Créer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="beeaa-145">Create a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="beeaa-146">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-146">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="beeaa-147">Sur la page **utilisateurs actifs** , sélectionnez **filtres** , puis **nouveau filtre**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-147">On the **Active users** page, select **Filters** and select **New filter**.</span></span>
  
3. <span data-ttu-id="beeaa-148">Sur la page **filtre personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-148">On the **Custom filter** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="beeaa-149">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="beeaa-149">Your custom view is now included in the drop-down list of filters.</span></span>
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="beeaa-150">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-150">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="beeaa-151">Sur la page **utilisateurs actifs** , sélectionnez **affichages** et sélectionnez **Ajouter un affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-151">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="beeaa-152">Sur la page **affichage personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-152">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="beeaa-153">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="beeaa-153">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end


::: moniker range="o365-21vianet"

1. <span data-ttu-id="beeaa-154">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-154">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="beeaa-155">Sur la page **utilisateurs actifs** , sélectionnez **affichages** et sélectionnez **Ajouter un affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-155">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="beeaa-156">Sur la page **affichage personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-156">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="beeaa-157">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="beeaa-157">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end
    

## <a name="edit-or-delete-a-custom-user-view"></a><span data-ttu-id="beeaa-158">Modifier ou supprimer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="beeaa-158">Edit or delete a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="beeaa-159">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-159">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="beeaa-160">Sur la page **utilisateurs actifs** , sélectionnez **filtre**, sélectionnez le filtre à modifier, puis sélectionnez **modifier le filtre**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-160">On the **Active users** page, select **Filter**, select the filter you want to change, and then select **Edit filter**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="beeaa-161">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="beeaa-161">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="beeaa-162">Sur la page **filtre personnalisé** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-162">On the **Custom filter** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="beeaa-163">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-163">Or, to delete the filter, at the bottom of the page select **Delete**.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="beeaa-164">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-164">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="beeaa-165">Sur la page **utilisateurs actifs** , sélectionnez **affichages**, sélectionnez le filtre à modifier, puis cliquez sur **modifier cet affichage**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-165">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="beeaa-166">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="beeaa-166">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="beeaa-167">Sur la page **vue personnalisée** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-167">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="beeaa-168">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **Supprimer l’affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-168">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="beeaa-169">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="beeaa-169">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="beeaa-170">Sur la page **utilisateurs actifs** , sélectionnez **affichages**, sélectionnez le filtre à modifier, puis cliquez sur **modifier cet affichage**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-170">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="beeaa-171">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="beeaa-171">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="beeaa-172">Sur la page **vue personnalisée** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-172">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="beeaa-173">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **Supprimer l’affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="beeaa-173">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end


     

