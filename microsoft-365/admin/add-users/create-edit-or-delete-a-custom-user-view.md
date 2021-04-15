---
title: Créer, modifier ou supprimer une vue utilisateur personnalisée
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
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 4fe7f6ac-be8e-4b57-9e13-24ff889a4b28
description: Apprenez à utiliser des filtres pour créer, modifier ou supprimer un affichage utilisateur personnalisé dans Microsoft 365.
ms.openlocfilehash: 4bd4ea351612c2ae5175cd27fa7a689d671a8b62
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51759929"
---
# <a name="create-edit-or-delete-a-custom-user-view"></a><span data-ttu-id="393a3-103">Créer, modifier ou supprimer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="393a3-103">Create, edit, or delete a custom user view</span></span>

<span data-ttu-id="393a3-104">Si vous êtes un administrateur global ou de gestion des utilisateurs d'un abonnement Microsoft 365 pour les entreprises, vous pouvez créer des affichages utilisateur personnalisés pour afficher un sous-ensemble spécifique d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="393a3-104">If you're a global or user management admin of a Microsoft 365 for business subscription,  you can create custom user views to view a specific subset of users.</span></span> <span data-ttu-id="393a3-105">Ces affichages s'ajoutent à l'ensemble standard d'affichages.</span><span class="sxs-lookup"><span data-stu-id="393a3-105">These views are in addition to the standard set of views.</span></span> <span data-ttu-id="393a3-106">Vous pouvez créer, modifier ou supprimer des affichages utilisateur personnalisés, et les affichages personnalisés que vous créez sont disponibles pour tous les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="393a3-106">You can create, edit, or delete custom user views, and the custom views you create are available to all admins.</span></span>
  
## <a name="custom-user-views-in-the-admin-center"></a><span data-ttu-id="393a3-107">Affichages utilisateur personnalisés dans le Centre d'administration</span><span class="sxs-lookup"><span data-stu-id="393a3-107">Custom user views in the admin center</span></span>

<span data-ttu-id="393a3-108">Lorsque vous créez, modifiez ou supprimez un affichage  utilisateur personnalisé, les modifications s'afficheront dans la liste De filtres que tous les administrateurs de votre entreprise voient lorsqu'ils vont sur la **page** Utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="393a3-108">When you create, edit, or delete a custom user view, the changes will be shown in the **Filter** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="393a3-109">Vous pouvez créer jusqu'à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="393a3-109">You can create up to 50 custom views.</span></span> 

> [!TIP]
>  <span data-ttu-id="393a3-110">Les affichages utilisateur standard sont affichés par défaut dans **la** liste de listes listes des filtres.</span><span class="sxs-lookup"><span data-stu-id="393a3-110">Standard user views are displayed by default in the **Filters** drop-down list.</span></span> <span data-ttu-id="393a3-111">Les filtres standard incluent tous les utilisateurs, les utilisateurs sous **licence,** les utilisateurs invités, les utilisateurs autorisés à se connecter, les **utilisateurs bloqués,** les utilisateurs sans **licence,** les utilisateurs avec erreur, les **administrateurs** de facturation, les **administrateurs** globaux, les administrateurs du **helpdesk,** les **administrateurs** de service et les administrateurs de gestion des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="393a3-111">The standard filters include **All users**, **Licensed users**, **Guest users**,  **Sign-in allowed**, **Sign-in blocked**, **Unlicensed users**, **Users with errors**, **Billing admins**, **Global admins**, **Helpdesk admins**, **Service admins**, and **User management admins**.</span></span> <span data-ttu-id="393a3-112">Vous ne pouvez pas modifier ou supprimer des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="393a3-112">You can't edit or delete standard views.</span></span> 

<span data-ttu-id="393a3-113">Quelques éléments à noter concernant les affichages standard :</span><span class="sxs-lookup"><span data-stu-id="393a3-113">A few things to note about standard views:</span></span> 

- <span data-ttu-id="393a3-114">Certains affichages standard affichent une liste non triée s'il y a plus de 2 000 utilisateurs dans la liste.</span><span class="sxs-lookup"><span data-stu-id="393a3-114">Some standard views display an unsorted list if there are more than 2,000 users in the list.</span></span> <span data-ttu-id="393a3-115">Pour localiser des utilisateurs spécifiques dans cette liste, utilisez la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="393a3-115">To locate specific users in this list, use the search box.</span></span> 
- <span data-ttu-id="393a3-116">Si vous n'avez pas acheté Microsoft 365 auprès de Microsoft, les administrateurs de facturation n'apparaissent pas dans la liste des **affichages** standard.</span><span class="sxs-lookup"><span data-stu-id="393a3-116">If you didn't purchase Microsoft 365 from Microsoft, **Billing admins** don't appear in the standard views list.</span></span> <span data-ttu-id="393a3-117">Pour plus d'informations, consultez la rubrique [Affectation de rôles d'administrateur](assign-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="393a3-117">For more information, see [Assigning admin roles](assign-admin-roles.md).</span></span> 
  
## <a name="choose-the-filters-for-your-custom-user-view"></a><span data-ttu-id="393a3-118">Choisir les filtres pour votre affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="393a3-118">Choose the filters for your custom user view</span></span>

<span data-ttu-id="393a3-119">Vous pouvez créer et modifier vos affichages personnalisés dans le **volet** Filtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="393a3-119">You can create and edit your custom views in the **Custom filter** pane.</span></span> <span data-ttu-id="393a3-120">Si vous sélectionnez plusieurs options de filtre, vous obtenez des résultats qui contiennent des utilisateurs qui correspondent à tous les critères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="393a3-120">If you select multiple filter options, you get results that contain users who match all the selected criteria.</span></span> <span data-ttu-id="393a3-121">L'exemple suivant vous montre comment créer un affichage personnalisé nommé « Utilisateurs canadien » qui affiche tous les utilisateurs d'un domaine spécifique qui sont au Canada.</span><span class="sxs-lookup"><span data-stu-id="393a3-121">The following example shows you how to create a custom view named "Canadian users" that shows all users on a specific domain who are in Canada.</span></span> 

  
 <span data-ttu-id="393a3-122">**A - Domaine** Si vous avez plusieurs domaines pour votre organisation, vous pouvez choisir parmi une liste de domaines disponibles.</span><span class="sxs-lookup"><span data-stu-id="393a3-122">**A - Domain** If you have multiple domains for your organization, you can choose from a drop-down list of domains that are available.</span></span> 
  
 <span data-ttu-id="393a3-123">**B - État de la signature** Choisissez les utilisateurs autorisés ou bloqués.</span><span class="sxs-lookup"><span data-stu-id="393a3-123">**B - Sign-in status** Choose users that are allowed or blocked.</span></span> 
  
 <span data-ttu-id="393a3-124">**C - Emplacement** Choisissez un emplacement dans une liste de pays.</span><span class="sxs-lookup"><span data-stu-id="393a3-124">**C - Location** Choose a location from a drop-down list of countries.</span></span> 
  
 <span data-ttu-id="393a3-125">**D - Licence de produit attribuée** Choisissez dans une liste des licences disponibles au niveau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="393a3-125">**D - Assigned product license** Choose from a drop-down list of licenses that are available at your organization.</span></span> <span data-ttu-id="393a3-126">Utilisez ce filtre pour afficher les utilisateurs qui ont la licence que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="393a3-126">Use this filter to show users who have the license you selected assigned to them.</span></span> <span data-ttu-id="393a3-127">Les utilisateurs peuvent également avoir des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="393a3-127">Users may also have additional licenses.</span></span> 
  
<span data-ttu-id="393a3-128">Vous pouvez également filtrer en fonction des détails de profil utilisateur supplémentaires utilisés dans votre organisation, tels que le service, la ville, l'État ou la province, le pays ou la région, ou la fonction.</span><span class="sxs-lookup"><span data-stu-id="393a3-128">You can also filter by additional user profile details used in your organization such as department, city, state or province, country or region, or job title.</span></span>
  
 <span data-ttu-id="393a3-129">**Autres conditions :**</span><span class="sxs-lookup"><span data-stu-id="393a3-129">**Other conditions:**</span></span>
  
- <span data-ttu-id="393a3-130">**Utilisateurs synchronisés uniquement** Activez cette case pour afficher tous les utilisateurs qui ont été synchronisés avec Active Directory local, que les utilisateurs soient activés ou non.</span><span class="sxs-lookup"><span data-stu-id="393a3-130">**Synchronized users only** Select this box to show all users who have been synced with the local Active Directory, regardless of whether the users have been activated or not.</span></span> 
    
- <span data-ttu-id="393a3-131">**Utilisateurs avec erreurs** Sélectionnez cette zone pour afficher les utilisateurs qui peuvent avoir des erreurs d'approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="393a3-131">**Users with errors** Select this box to show users who may have provisioning errors.</span></span> 
    
- <span data-ttu-id="393a3-132">**Utilisateurs sans permis** Sélectionnez cette case pour rechercher tous les utilisateurs qui n'ont pas reçu de licence.</span><span class="sxs-lookup"><span data-stu-id="393a3-132">**Unlicensed users** Select this box to find all the users who haven't been assigned a license.</span></span> <span data-ttu-id="393a3-133">Les résultats de cette vue peuvent également inclure les utilisateurs qui ont une boîte aux lettres Exchange mais n'ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="393a3-133">The results for this view can also include users who have an Exchange mailbox but don't have a license.</span></span> <span data-ttu-id="393a3-134">Pour suivre ces utilisateurs spécifiquement, utilisez le filtre Utilisateurs sans permis avec des boîtes aux lettres **ou des archives Exchange.**</span><span class="sxs-lookup"><span data-stu-id="393a3-134">To track those users specifically, use the filter **Unlicensed users with Exchange mailboxes or archives**.</span></span> <span data-ttu-id="393a3-135">Les résultats de cette vue peuvent également inclure les utilisateurs qui ont une archive Exchange, mais n'ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="393a3-135">The results for this view can also include users who have an Exchange archive, but don't have a license.</span></span>
    
- <span data-ttu-id="393a3-136">**Utilisateurs sans permis avec des boîtes aux lettres ou des archives Exchange** Sélectionnez cette case pour afficher les comptes d'utilisateur qui ont été créés dans Exchange Online et qui ont une boîte aux lettres Exchange, mais qui n'ont pas été affectés à une licence Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="393a3-136">**Unlicensed users with Exchange mailboxes or archives** Select this box to show user accounts that were created in Exchange Online and have an Exchange mailbox, but weren't assigned an Microsoft 365 license.</span></span> <span data-ttu-id="393a3-137">Les résultats de ce filtre incluent les utilisateurs qui ont ou qui ont été affectés à une archive Exchange.</span><span class="sxs-lookup"><span data-stu-id="393a3-137">The results of this filter include users who have or who were assigned an Exchange archive.</span></span> 

> [!NOTE]
> <span data-ttu-id="393a3-138">Le **filtre Utilisateurs sans** permis avec boîtes aux lettres Exchange fonctionne dans les cas ci-après :</span><span class="sxs-lookup"><span data-stu-id="393a3-138">The **Unlicensed users with Exchange mailboxes** filter works when:</span></span>
1. <span data-ttu-id="393a3-139">La boîte aux lettres  a été récemment convertie en utilisateur et **n'a** pas de licence.</span><span class="sxs-lookup"><span data-stu-id="393a3-139">The mailbox has been recently converted from **shared** to **user** and it has no license.</span></span>
2. <span data-ttu-id="393a3-140">La boîte aux lettres a été récemment migrée vers Microsoft 365, mais une licence n'a pas été attribuée.</span><span class="sxs-lookup"><span data-stu-id="393a3-140">The mailbox has been recently migrated to Microsoft 365 but a license has not been assigned.</span></span>
3. <span data-ttu-id="393a3-141">La boîte aux lettres a été créée à l'aide de PowerShell et une licence n'a pas été attribuée.</span><span class="sxs-lookup"><span data-stu-id="393a3-141">The mailbox has been created using PowerShell, and a license has not been assigned.</span></span>
4. <span data-ttu-id="393a3-142">Une nouvelle boîte aux lettres qui a été créée en local avec une cmdlet New-RemoteMailbox est mise en service pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="393a3-142">A new mailbox that has been created on-premise with a New-RemoteMailbox cmdlet is provisioned for the user.</span></span>
    
> [!TIP]
> <span data-ttu-id="393a3-143">Si vous créez un affichage personnalisé qui renvoie plus de 2 000 utilisateurs, la liste d'utilisateurs résultante n'est pas triée.</span><span class="sxs-lookup"><span data-stu-id="393a3-143">If you create a custom view that returns more than 2,000 users, the resulting user list isn't sorted.</span></span> <span data-ttu-id="393a3-144">Dans ce cas, utilisez la zone de recherche pour rechercher des utilisateurs ou modifiez votre affichage personnalisé pour affiner votre recherche.</span><span class="sxs-lookup"><span data-stu-id="393a3-144">In this case, use the search box to find users or edit your custom view to refine your search.</span></span> 
  
## <a name="create-a-custom-user-view"></a><span data-ttu-id="393a3-145">Créer un affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="393a3-145">Create a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="393a3-146">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-146">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.</span></span>
    
2. <span data-ttu-id="393a3-147">Dans la page **Utilisateurs** actifs, sélectionnez **Filtres** et **Nouveau filtre.**</span><span class="sxs-lookup"><span data-stu-id="393a3-147">On the **Active users** page, select **Filters** and select **New filter**.</span></span>
  
3. <span data-ttu-id="393a3-148">Dans la page **Filtre personnalisé,** entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="393a3-148">On the **Custom filter** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="393a3-149">Votre affichage personnalisé est désormais inclus dans la liste de listes de filtres.</span><span class="sxs-lookup"><span data-stu-id="393a3-149">Your custom view is now included in the drop-down list of filters.</span></span>
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="393a3-150">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-150">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a>.</span></span>  

2. <span data-ttu-id="393a3-151">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages** et **Ajouter un affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="393a3-151">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="393a3-152">Dans la page **Affichage** personnalisé, entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="393a3-152">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="393a3-153">Votre affichage personnalisé est désormais inclus dans la liste de listes de filtres.</span><span class="sxs-lookup"><span data-stu-id="393a3-153">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end


::: moniker range="o365-21vianet"

1. <span data-ttu-id="393a3-154">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-154">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a>.</span></span> 

2. <span data-ttu-id="393a3-155">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages** et **Ajouter un affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="393a3-155">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="393a3-156">Dans la page **Affichage** personnalisé, entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="393a3-156">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="393a3-157">Votre affichage personnalisé est désormais inclus dans la liste de listes de filtres.</span><span class="sxs-lookup"><span data-stu-id="393a3-157">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end
    

## <a name="edit-or-delete-a-custom-user-view"></a><span data-ttu-id="393a3-158">Modifier ou supprimer un affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="393a3-158">Edit or delete a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="393a3-159">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-159">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.</span></span>
    
2. <span data-ttu-id="393a3-160">Dans la page **Utilisateurs** actifs, **sélectionnez Filtrer,** sélectionnez le filtre à modifier, puis sélectionnez **Modifier le filtre.**</span><span class="sxs-lookup"><span data-stu-id="393a3-160">On the **Active users** page, select **Filter**, select the filter you want to change, and then select **Edit filter**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="393a3-161">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="393a3-161">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="393a3-162">Dans la page **Filtre personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="393a3-162">On the **Custom filter** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="393a3-163">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="393a3-163">Or, to delete the filter, at the bottom of the page select **Delete**.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="393a3-164">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-164">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a>.</span></span>  

2. <span data-ttu-id="393a3-165">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages,** sélectionnez le filtre à modifier, puis **sélectionnez Modifier cet affichage.**</span><span class="sxs-lookup"><span data-stu-id="393a3-165">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="393a3-166">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="393a3-166">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="393a3-167">Dans la page **Affichage personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="393a3-167">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="393a3-168">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer l'affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="393a3-168">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="393a3-169">Dans le Centre d'administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="393a3-169">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a>.</span></span> 

2. <span data-ttu-id="393a3-170">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages,** sélectionnez le filtre à modifier, puis **sélectionnez Modifier cet affichage.**</span><span class="sxs-lookup"><span data-stu-id="393a3-170">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="393a3-171">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="393a3-171">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="393a3-172">Dans la page **Affichage personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="393a3-172">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="393a3-173">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer l'affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="393a3-173">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end


     