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
description: Découvrez comment utiliser des filtres pour créer, modifier ou supprimer un affichage utilisateur personnalisé dans Microsoft 365.
ms.openlocfilehash: 598a167b9845f763ddab57d3c5ba36e431aa751c
ms.sourcegitcommit: a3ec91423c352cd5fbf79b46ccd9c169455a03ba
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2020
ms.locfileid: "44664573"
---
# <a name="create-edit-or-delete-a-custom-user-view"></a><span data-ttu-id="9bced-103">Créer, modifier ou supprimer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="9bced-103">Create, edit, or delete a custom user view</span></span>

<span data-ttu-id="9bced-104">Si vous êtes un administrateur global ou de gestion des utilisateurs d’un abonnement Microsoft 365 pour les entreprises, vous pouvez créer des affichages utilisateur personnalisés pour afficher un sous-ensemble spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bced-104">If you're a global or user management admin of a Microsoft 365 for business subscription,  you can create custom user views to view a specific subset of users.</span></span> <span data-ttu-id="9bced-105">Ces affichages s’ajoutent à l’ensemble standard d’affichages.</span><span class="sxs-lookup"><span data-stu-id="9bced-105">These views are in addition to the standard set of views.</span></span> <span data-ttu-id="9bced-106">Vous pouvez créer, modifier ou supprimer des affichages utilisateur personnalisés, et les affichages personnalisés que vous créez sont disponibles pour tous les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="9bced-106">You can create, edit, or delete custom user views, and the custom views you create are available to all admins.</span></span>
  
## <a name="custom-user-views-in-the-admin-center"></a><span data-ttu-id="9bced-107">Affichages utilisateur personnalisés dans le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="9bced-107">Custom user views in the admin center</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="9bced-108">Lorsque vous créez, modifiez ou supprimez un affichage  utilisateur personnalisé, les modifications s’afficheront dans la liste De filtres que tous les administrateurs de votre entreprise voient lorsqu’ils vont sur la **page** Utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bced-108">When you create, edit, or delete a custom user view, the changes will be shown in the **Filter** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="9bced-109">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-109">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="9bced-110">Lorsque vous créez, modifiez ou supprimez un affichage  utilisateur personnalisé, les modifications s’afficheront dans la liste Affichages que tous les administrateurs de votre entreprise voient lorsqu’ils vont sur la **page** Utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bced-110">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="9bced-111">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-111">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="9bced-112">Lorsque vous créez, modifiez ou supprimez un affichage  utilisateur personnalisé, les modifications s’afficheront dans la liste Affichages que tous les administrateurs de votre entreprise voient lorsqu’ils vont sur la **page** Utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bced-112">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="9bced-113">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-113">You can create up to 50 custom views.</span></span> 

::: moniker-end

> [!TIP]
>  <span data-ttu-id="9bced-114">Les affichages utilisateur standard sont affichés par défaut dans **la** liste de listes listes des filtres.</span><span class="sxs-lookup"><span data-stu-id="9bced-114">Standard user views are displayed by default in the **Filters** drop-down list.</span></span> <span data-ttu-id="9bced-115">Les filtres standard incluent tous les utilisateurs, les utilisateurs sous **licence,** les utilisateurs invités, les utilisateurs autorisés à se connecter, les **utilisateurs bloqués,** les utilisateurs sans **licence,** les utilisateurs avec erreur, les **administrateurs** de facturation, les **administrateurs** globaux, les administrateurs du **helpdesk,** les **administrateurs** de service et les administrateurs de gestion des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="9bced-115">The standard filters include **All users**, **Licensed users**, **Guest users**,  **Sign-in allowed**, **Sign-in blocked**, **Unlicensed users**, **Users with errors**, **Billing admins**, **Global admins**, **Helpdesk admins**, **Service admins**, and **User management admins**.</span></span> <span data-ttu-id="9bced-116">Vous ne pouvez pas modifier ou supprimer des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="9bced-116">You can't edit or delete standard views.</span></span> 

<span data-ttu-id="9bced-117">Quelques éléments à noter concernant les affichages standard :</span><span class="sxs-lookup"><span data-stu-id="9bced-117">A few things to note about standard views:</span></span> 

- <span data-ttu-id="9bced-118">Certains affichages standard affichent une liste non triée s’il y a plus de 2 000 utilisateurs dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9bced-118">Some standard views display an unsorted list if there are more than 2,000 users in the list.</span></span> <span data-ttu-id="9bced-119">Pour localiser des utilisateurs spécifiques dans cette liste, utilisez la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="9bced-119">To locate specific users in this list, use the search box.</span></span> 
- <span data-ttu-id="9bced-120">Si vous n’avez pas acheté Microsoft 365 auprès de Microsoft, les administrateurs de facturation n’apparaissent pas dans la liste des **affichages** standard.</span><span class="sxs-lookup"><span data-stu-id="9bced-120">If you didn't purchase Microsoft 365 from Microsoft, **Billing admins** don't appear in the standard views list.</span></span> <span data-ttu-id="9bced-121">Pour plus d'informations, consultez la rubrique [Affectation de rôles d'administrateur](assign-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9bced-121">For more information, see [Assigning admin roles](assign-admin-roles.md).</span></span> 
  
## <a name="choose-the-filters-for-your-custom-user-view"></a><span data-ttu-id="9bced-122">Choisir les filtres pour votre affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="9bced-122">Choose the filters for your custom user view</span></span>

<span data-ttu-id="9bced-123">Vous pouvez créer et modifier vos affichages personnalisés dans le **volet** Filtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9bced-123">You can create and edit your custom views in the **Custom filter** pane.</span></span> <span data-ttu-id="9bced-124">Si vous sélectionnez plusieurs options de filtre, vous obtenez des résultats qui contiennent des utilisateurs qui correspondent à tous les critères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9bced-124">If you select multiple filter options, you get results that contain users who match all the selected criteria.</span></span> <span data-ttu-id="9bced-125">L’exemple suivant vous montre comment créer un affichage personnalisé nommé « Utilisateurs canadien » qui affiche tous les utilisateurs d’un domaine spécifique qui sont au Canada.</span><span class="sxs-lookup"><span data-stu-id="9bced-125">The following example shows you how to create a custom view named "Canadian users" that shows all users on a specific domain who are in Canada.</span></span> 

  
 <span data-ttu-id="9bced-126">**A - Domaine** Si vous avez plusieurs domaines pour votre organisation, vous pouvez choisir parmi une liste de domaines disponibles.</span><span class="sxs-lookup"><span data-stu-id="9bced-126">**A - Domain** If you have multiple domains for your organization, you can choose from a drop-down list of domains that are available.</span></span> 
  
 <span data-ttu-id="9bced-127">**B - État de la signature** Choisissez les utilisateurs autorisés ou bloqués.</span><span class="sxs-lookup"><span data-stu-id="9bced-127">**B - Sign-in status** Choose users that are allowed or blocked.</span></span> 
  
 <span data-ttu-id="9bced-128">**C - Emplacement** Choisissez un emplacement dans une liste de pays.</span><span class="sxs-lookup"><span data-stu-id="9bced-128">**C - Location** Choose a location from a drop-down list of countries.</span></span> 
  
 <span data-ttu-id="9bced-129">**D - Licence de produit attribuée** Choisissez dans une liste des licences disponibles au niveau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9bced-129">**D - Assigned product license** Choose from a drop-down list of licenses that are available at your organization.</span></span> <span data-ttu-id="9bced-130">Utilisez ce filtre pour afficher les utilisateurs qui ont la licence que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9bced-130">Use this filter to show users who have the license you selected assigned to them.</span></span> <span data-ttu-id="9bced-131">Les utilisateurs peuvent également avoir des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9bced-131">Users may also have additional licenses.</span></span> 
  
<span data-ttu-id="9bced-132">Vous pouvez également filtrer en fonction des détails de profil utilisateur supplémentaires utilisés dans votre organisation, tels que le service, la ville, l’État ou la province, le pays ou la région, ou la fonction.</span><span class="sxs-lookup"><span data-stu-id="9bced-132">You can also filter by additional user profile details used in your organization such as department, city, state or province, country or region, or job title.</span></span>
  
 <span data-ttu-id="9bced-133">**Autres conditions :**</span><span class="sxs-lookup"><span data-stu-id="9bced-133">**Other conditions:**</span></span>
  
- <span data-ttu-id="9bced-134">**Utilisateurs synchronisés uniquement** Activez cette case pour afficher tous les utilisateurs qui ont été synchronisés avec Active Directory local, que les utilisateurs soient activés ou non.</span><span class="sxs-lookup"><span data-stu-id="9bced-134">**Synchronized users only** Select this box to show all users who have been synced with the local Active Directory, regardless of whether the users have been activated or not.</span></span> 
    
- <span data-ttu-id="9bced-135">**Utilisateurs avec erreurs** Sélectionnez cette case pour afficher les utilisateurs qui peuvent avoir des erreurs d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="9bced-135">**Users with errors** Select this box to show users who may have provisioning errors.</span></span> 
    
- <span data-ttu-id="9bced-136">**Utilisateurs sans permis** Sélectionnez cette case pour rechercher tous les utilisateurs qui n’ont pas reçu de licence.</span><span class="sxs-lookup"><span data-stu-id="9bced-136">**Unlicensed users** Select this box to find all the users who haven't been assigned a license.</span></span> <span data-ttu-id="9bced-137">Les résultats de cette vue peuvent également inclure les utilisateurs qui ont une boîte aux lettres Exchange mais n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="9bced-137">The results for this view can also include users who have an Exchange mailbox but don't have a license.</span></span> <span data-ttu-id="9bced-138">Pour suivre ces utilisateurs spécifiquement, utilisez le filtre Utilisateurs sans permis avec des boîtes aux lettres **ou des archives Exchange.**</span><span class="sxs-lookup"><span data-stu-id="9bced-138">To track those users specifically, use the filter **Unlicensed users with Exchange mailboxes or archives**.</span></span> <span data-ttu-id="9bced-139">Les résultats de cette vue peuvent également inclure les utilisateurs qui ont une archive Exchange, mais n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="9bced-139">The results for this view can also include users who have an Exchange archive, but don't have a license.</span></span>
    
- <span data-ttu-id="9bced-140">**Utilisateurs sans permis avec des boîtes aux lettres ou des archives Exchange** Sélectionnez cette case pour afficher les comptes d’utilisateur qui ont été créés dans Exchange Online et qui ont une boîte aux lettres Exchange, mais qui n’ont pas obtenu de licence Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9bced-140">**Unlicensed users with Exchange mailboxes or archives** Select this box to show user accounts that were created in Exchange Online and have an Exchange mailbox, but weren't assigned an Microsoft 365 license.</span></span> <span data-ttu-id="9bced-141">Les résultats de ce filtre incluent les utilisateurs qui ont ou qui ont été affectés à une archive Exchange.</span><span class="sxs-lookup"><span data-stu-id="9bced-141">The results of this filter include users who have or who were assigned an Exchange archive.</span></span> 

> [!NOTE]
> <span data-ttu-id="9bced-142">Le **filtre Utilisateurs sans** permis avec boîtes aux lettres Exchange fonctionne dans les cas ci-après :</span><span class="sxs-lookup"><span data-stu-id="9bced-142">The **Unlicensed users with Exchange mailboxes** filter works when:</span></span>
1. <span data-ttu-id="9bced-143">La boîte aux lettres  a été récemment convertie en utilisateur et **n’a** pas de licence.</span><span class="sxs-lookup"><span data-stu-id="9bced-143">The mailbox has been recently converted from **shared** to **user** and it has no license.</span></span>
2. <span data-ttu-id="9bced-144">La boîte aux lettres a été récemment migrée vers Microsoft 365, mais une licence n’a pas été attribuée.</span><span class="sxs-lookup"><span data-stu-id="9bced-144">The mailbox has been recently migrated to Microsoft 365 but a license has not been assigned.</span></span>
3. <span data-ttu-id="9bced-145">La boîte aux lettres a été créée à l’aide de PowerShell et une licence n’a pas été attribuée.</span><span class="sxs-lookup"><span data-stu-id="9bced-145">The mailbox has been created using PowerShell, and a license has not been assigned.</span></span>
4. <span data-ttu-id="9bced-146">Une nouvelle boîte aux lettres qui a été créée en local avec une cmdlet New-RemoteMailbox est mise en service pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9bced-146">A new mailbox that has been created on-premise with a New-RemoteMailbox cmdlet is provisioned for the user.</span></span>
    
> [!TIP]
> <span data-ttu-id="9bced-147">Si vous créez un affichage personnalisé qui renvoie plus de 2 000 utilisateurs, la liste d’utilisateurs résultante n’est pas triée.</span><span class="sxs-lookup"><span data-stu-id="9bced-147">If you create a custom view that returns more than 2,000 users, the resulting user list isn't sorted.</span></span> <span data-ttu-id="9bced-148">Dans ce cas, utilisez la zone de recherche pour rechercher des utilisateurs ou modifiez votre affichage personnalisé pour affiner votre recherche.</span><span class="sxs-lookup"><span data-stu-id="9bced-148">In this case, use the search box to find users or edit your custom view to refine your search.</span></span> 
  
## <a name="create-a-custom-user-view"></a><span data-ttu-id="9bced-149">Créer un affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="9bced-149">Create a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="9bced-150">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-150">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.</span></span>
    
2. <span data-ttu-id="9bced-151">Dans la page **Utilisateurs** actifs, sélectionnez **Filtres** et **Nouveau filtre.**</span><span class="sxs-lookup"><span data-stu-id="9bced-151">On the **Active users** page, select **Filters** and select **New filter**.</span></span>
  
3. <span data-ttu-id="9bced-152">Dans la page **Filtre personnalisé,** entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9bced-152">On the **Custom filter** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="9bced-153">Votre affichage personnalisé est désormais inclus dans la liste liste de filtres.</span><span class="sxs-lookup"><span data-stu-id="9bced-153">Your custom view is now included in the drop-down list of filters.</span></span>
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="9bced-154">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-154">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a>.</span></span>  

2. <span data-ttu-id="9bced-155">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages** et **Ajouter un affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="9bced-155">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="9bced-156">Dans la page **Affichage personnalisé,** entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9bced-156">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="9bced-157">Votre affichage personnalisé est désormais inclus dans la liste liste de filtres.</span><span class="sxs-lookup"><span data-stu-id="9bced-157">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end


::: moniker range="o365-21vianet"

1. <span data-ttu-id="9bced-158">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-158">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a>.</span></span> 

2. <span data-ttu-id="9bced-159">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages** et **Ajouter un affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="9bced-159">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="9bced-160">Dans la page **Affichage personnalisé,** entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9bced-160">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="9bced-161">Votre affichage personnalisé est désormais inclus dans la liste liste de filtres.</span><span class="sxs-lookup"><span data-stu-id="9bced-161">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end
    

## <a name="edit-or-delete-a-custom-user-view"></a><span data-ttu-id="9bced-162">Modifier ou supprimer un affichage utilisateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="9bced-162">Edit or delete a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="9bced-163">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-163">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.</span></span>
    
2. <span data-ttu-id="9bced-164">Dans la page **Utilisateurs** actifs, **sélectionnez Filtrer,** sélectionnez le filtre à modifier, puis sélectionnez **Modifier le filtre.**</span><span class="sxs-lookup"><span data-stu-id="9bced-164">On the **Active users** page, select **Filter**, select the filter you want to change, and then select **Edit filter**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="9bced-165">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-165">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="9bced-166">Dans la page **Filtre personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="9bced-166">On the **Custom filter** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="9bced-167">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9bced-167">Or, to delete the filter, at the bottom of the page select **Delete**.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="9bced-168">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-168">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a>.</span></span>  

2. <span data-ttu-id="9bced-169">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages,** sélectionnez le filtre à modifier, puis **sélectionnez Modifier cet affichage.**</span><span class="sxs-lookup"><span data-stu-id="9bced-169">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="9bced-170">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-170">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="9bced-171">Dans la page **Affichage personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="9bced-171">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="9bced-172">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer l’affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="9bced-172">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="9bced-173">Dans le Centre d’administration, allez à **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">actifs.</a></span><span class="sxs-lookup"><span data-stu-id="9bced-173">In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a>.</span></span> 

2. <span data-ttu-id="9bced-174">Dans la page **Utilisateurs** actifs, sélectionnez **Affichages,** sélectionnez le filtre à modifier, puis **sélectionnez Modifier cet affichage.**</span><span class="sxs-lookup"><span data-stu-id="9bced-174">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="9bced-175">Vous pouvez modifier uniquement les affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9bced-175">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="9bced-176">Dans la page **Affichage personnalisé,** modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="9bced-176">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="9bced-177">Ou, pour supprimer le filtre, en bas de la page, sélectionnez **Supprimer l’affichage personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="9bced-177">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end


     