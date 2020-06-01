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
description: Apprenez à utiliser des filtres pour créer, modifier ou supprimer des affichages utilisateur personnalisés dans Microsoft 365.
ms.openlocfilehash: 265aa1a7c22475710a12a93c2bfee0b7749f438b
ms.sourcegitcommit: a005395165db8896f4109674443b5e5e9209861d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2020
ms.locfileid: "44431640"
---
# <a name="create-edit-or-delete-a-custom-user-view-in-office-365"></a><span data-ttu-id="4cf5a-103">Créer, modifier ou supprimer une vue utilisateur personnalisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4cf5a-103">Create, edit, or delete a custom user view in Office 365</span></span>

<span data-ttu-id="4cf5a-104">Si vous êtes un administrateur général ou un administrateur de gestion des utilisateurs d’Office 365, vous pouvez créer des affichages utilisateur personnalisés pour afficher un sous-ensemble spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-104">If you're a global or user management admin of Office 365, you can create custom user views to view a specific subset of users.</span></span> <span data-ttu-id="4cf5a-105">Ces affichages s’ajoutent à l’ensemble standard de vues fournies avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-105">These views are in addition to the standard set of views that come with Office 365.</span></span> <span data-ttu-id="4cf5a-106">Vous pouvez créer, modifier ou supprimer des affichages utilisateur personnalisés, et les vues personnalisées que vous créez sont disponibles pour tous les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-106">You can create, edit, or delete custom user views, and the custom views you create are available to all admins.</span></span>
  
## <a name="custom-user-views-in-the-admin-center"></a><span data-ttu-id="4cf5a-107">Vues utilisateur personnalisées dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4cf5a-107">Custom user views in the admin center</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="4cf5a-108">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications s’affichent dans la liste de **filtres** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="4cf5a-108">When you create, edit, or delete a custom user view, the changes will be shown in the **Filter** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="4cf5a-109">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-109">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="4cf5a-110">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications apparaissent dans la liste des **affichages** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="4cf5a-110">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="4cf5a-111">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-111">You can create up to 50 custom views.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="4cf5a-112">Lorsque vous créez, modifiez ou supprimez une vue utilisateur personnalisée, les modifications apparaissent dans la liste des **affichages** que tous les administrateurs de votre société voient quand ils accèdent à la page **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="4cf5a-112">When you create, edit, or delete a custom user view, the changes will be shown in the **Views** list that all admins in your company see when they go to the **Users** page.</span></span> <span data-ttu-id="4cf5a-113">Vous pouvez créer jusqu’à 50 affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-113">You can create up to 50 custom views.</span></span> 

::: moniker-end

> [!TIP]
>  <span data-ttu-id="4cf5a-114">Les affichages standard des utilisateurs sont affichés par défaut dans la liste déroulante **filtres** .</span><span class="sxs-lookup"><span data-stu-id="4cf5a-114">Standard user views are displayed by default in the **Filters** drop-down list.</span></span> <span data-ttu-id="4cf5a-115">Les filtres standard incluent **tous les utilisateurs**, **les utilisateurs sous licence**, **les utilisateurs invités**, la **connexion autorisée**, les **utilisateurs**qui ne disposent **pas de**licence, les **utilisateurs avec des erreurs, les administrateurs de** **facturation**, les administrateurs **globaux**, les administrateurs de service d' **assistance**, les administrateurs de **service**et les administrateurs de **gestion des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-115">The standard filters include **All users**, **Licensed users**, **Guest users**,  **Sign-in allowed**, **Sign-in blocked**, **Unlicensed users**, **Users with errors**, **Billing admins**, **Global admins**, **Helpdesk admins**, **Service admins**, and **User management admins**.</span></span> <span data-ttu-id="4cf5a-116">Vous ne pouvez pas modifier ou supprimer des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-116">You can't edit or delete standard views.</span></span> 

<span data-ttu-id="4cf5a-117">Voici quelques points à noter concernant les vues standard :</span><span class="sxs-lookup"><span data-stu-id="4cf5a-117">A few things to note about standard views:</span></span> 

- <span data-ttu-id="4cf5a-118">Certains affichages standard affichent une liste non triée s’il y a plus de 2 000 utilisateurs dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-118">Some standard views display an unsorted list if there are more than 2,000 users in the list.</span></span> <span data-ttu-id="4cf5a-119">Pour rechercher des utilisateurs spécifiques dans cette liste, utilisez la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-119">To locate specific users in this list, use the search box.</span></span> 
- <span data-ttu-id="4cf5a-120">Si vous n’avez pas acheté Microsoft 365 auprès de Microsoft, les **administrateurs de facturation** n’apparaissent pas dans la liste des affichages standard.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-120">If you didn't purchase Microsoft 365 from Microsoft, **Billing admins** don't appear in the standard views list.</span></span> <span data-ttu-id="4cf5a-121">Pour plus d'informations, consultez la rubrique [Affectation de rôles d'administrateur](assign-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4cf5a-121">For more information, see [Assigning admin roles](assign-admin-roles.md).</span></span> 
  
## <a name="choose-the-filters-for-your-custom-user-view"></a><span data-ttu-id="4cf5a-122">Choisir les filtres pour votre vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="4cf5a-122">Choose the filters for your custom user view</span></span>

<span data-ttu-id="4cf5a-123">Vous pouvez créer et modifier vos affichages personnalisés dans le volet **filtre personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="4cf5a-123">You can create and edit your custom views in the **Custom filter** pane.</span></span> <span data-ttu-id="4cf5a-124">Si vous sélectionnez plusieurs options de filtre, vous obtenez des résultats qui contiennent les utilisateurs qui répondent à tous les critères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-124">If you select multiple filter options, you get results that contain users who match all the selected criteria.</span></span> <span data-ttu-id="4cf5a-125">L’exemple suivant montre comment créer une vue personnalisée nommée « Users canadien » qui affiche tous les utilisateurs d’un domaine spécifique au Canada.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-125">The following example shows you how to create a custom view named "Canadian users" that shows all users on a specific domain who are in Canada.</span></span> 

  
 <span data-ttu-id="4cf5a-126">**A-domaine** Si votre organisation dispose de plusieurs domaines, vous pouvez choisir dans une liste déroulante des domaines disponibles.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-126">**A - Domain** If you have multiple domains for your organization, you can choose from a drop-down list of domains that are available.</span></span> 
  
 <span data-ttu-id="4cf5a-127">**B-état de connexion** Choisissez les utilisateurs autorisés ou bloqués.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-127">**B - Sign-in status** Choose users that are allowed or blocked.</span></span> 
  
 <span data-ttu-id="4cf5a-128">**Emplacement C** Choisissez un emplacement dans une liste déroulante de pays.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-128">**C - Location** Choose a location from a drop-down list of countries.</span></span> 
  
 <span data-ttu-id="4cf5a-129">**D-licence de produit attribuée** Faites votre choix dans la liste déroulante des licences disponibles dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-129">**D - Assigned product license** Choose from a drop-down list of licenses that are available at your organization.</span></span> <span data-ttu-id="4cf5a-130">Utilisez ce filtre pour montrer aux utilisateurs qui disposent de la licence que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-130">Use this filter to show users who have the license you selected assigned to them.</span></span> <span data-ttu-id="4cf5a-131">Les utilisateurs peuvent également avoir des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-131">Users may also have additional licenses.</span></span> 
  
<span data-ttu-id="4cf5a-132">Vous pouvez également filtrer par des détails de profil utilisateur supplémentaires utilisés dans votre organisation, tels que service, ville, État ou province, pays ou région, ou fonction.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-132">You can also filter by additional user profile details used in your organization such as department, city, state or province, country or region, or job title.</span></span>
  
 <span data-ttu-id="4cf5a-133">**Autres conditions :**</span><span class="sxs-lookup"><span data-stu-id="4cf5a-133">**Other conditions:**</span></span>
  
- <span data-ttu-id="4cf5a-134">**Utilisateurs synchronisés uniquement** Activez cette case à cocher pour afficher tous les utilisateurs qui ont été synchronisés avec l’annuaire Active Directory local, que les utilisateurs aient été activés ou non.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-134">**Synchronized users only** Select this box to show all users who have been synced with the local Active Directory, regardless of whether the users have been activated or not.</span></span> 
    
- <span data-ttu-id="4cf5a-135">**Utilisateurs avec des erreurs** Activez cette case à cocher pour afficher les utilisateurs qui peuvent avoir des erreurs de mise en service.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-135">**Users with errors** Select this box to show users who may have provisioning errors.</span></span> 
    
- <span data-ttu-id="4cf5a-136">**Utilisateurs sans licence** Activez cette case à cocher pour rechercher tous les utilisateurs qui n’ont pas reçu de licence.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-136">**Unlicensed users** Select this box to find all the users who haven't been assigned a license.</span></span> <span data-ttu-id="4cf5a-137">Les résultats de cette vue peuvent également inclure des utilisateurs qui disposent d’une boîte aux lettres Exchange mais qui n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-137">The results for this view can also include users who have an Exchange mailbox but don't have a license.</span></span> <span data-ttu-id="4cf5a-138">Pour effectuer le suivi de ces utilisateurs en particulier, utilisez le filtre **utilisateurs sans licence avec des boîtes aux lettres ou des archives Exchange**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-138">To track those users specifically, use the filter **Unlicensed users with Exchange mailboxes or archives**.</span></span> <span data-ttu-id="4cf5a-139">Les résultats de cette vue peuvent également inclure des utilisateurs qui disposent d’une archive Exchange, mais qui n’ont pas de licence.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-139">The results for this view can also include users who have an Exchange archive, but don't have a license.</span></span>
    
- <span data-ttu-id="4cf5a-140">**Utilisateurs sans licence avec des boîtes aux lettres ou des archives Exchange** Activez cette case à cocher pour afficher les comptes d’utilisateur qui ont été créés dans Exchange Online et qui disposent d’une boîte aux lettres Exchange, mais auxquels aucune licence Microsoft 365 n’a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-140">**Unlicensed users with Exchange mailboxes or archives** Select this box to show user accounts that were created in Exchange Online and have an Exchange mailbox, but weren't assigned an Microsoft 365 license.</span></span> <span data-ttu-id="4cf5a-141">Les résultats de ce filtre incluent les utilisateurs qui disposent ou non d’une archive Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-141">The results of this filter include users who have or who were assigned an Exchange archive.</span></span> 

> [!NOTE]
> <span data-ttu-id="4cf5a-142">Le filtre **utilisateurs sans licence avec boîtes aux lettres Exchange fonctionne dans** les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="4cf5a-142">The **Unlicensed users with Exchange mailboxes** filter works when:</span></span>
1. <span data-ttu-id="4cf5a-143">La boîte aux lettres a été récemment convertie de **partagé** à **utilisateur** et n’a pas de licence.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-143">The mailbox has been recently converted from **shared** to **user** and it has no license.</span></span>
2. <span data-ttu-id="4cf5a-144">La boîte aux lettres a été récemment migrée vers Microsoft 365, mais aucune licence n’a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-144">The mailbox has been recently migrated to Microsoft 365 but a license has not been assigned.</span></span>
3. <span data-ttu-id="4cf5a-145">La boîte aux lettres a été créée à l’aide de PowerShell et aucune licence n’a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-145">The mailbox has been created using PowerShell, and a license has not been assigned.</span></span>
4. <span data-ttu-id="4cf5a-146">Une nouvelle boîte aux lettres créée sur site avec une cmdlet New-RemoteMailbox est configurée pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-146">A new mailbox that has been created on-premise with a New-RemoteMailbox cmdlet is provisioned for the user.</span></span>
    
> [!TIP]
> <span data-ttu-id="4cf5a-147">Si vous créez un affichage personnalisé qui renvoie plus de 2 000 utilisateurs, la liste d’utilisateurs obtenue n’est pas triée.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-147">If you create a custom view that returns more than 2,000 users, the resulting user list isn't sorted.</span></span> <span data-ttu-id="4cf5a-148">Dans ce cas, utilisez la zone de recherche pour rechercher des utilisateurs ou modifier votre vue personnalisée pour affiner votre recherche.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-148">In this case, use the search box to find users or edit your custom view to refine your search.</span></span> 
  
## <a name="create-a-custom-user-view"></a><span data-ttu-id="4cf5a-149">Créer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="4cf5a-149">Create a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4cf5a-150">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-150">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="4cf5a-151">Sur la page **utilisateurs actifs** , sélectionnez **filtres** , puis **nouveau filtre**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-151">On the **Active users** page, select **Filters** and select **New filter**.</span></span>
  
3. <span data-ttu-id="4cf5a-152">Sur la page **filtre personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-152">On the **Custom filter** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="4cf5a-153">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-153">Your custom view is now included in the drop-down list of filters.</span></span>
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4cf5a-154">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-154">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="4cf5a-155">Sur la page **utilisateurs actifs** , sélectionnez **affichages** et sélectionnez **Ajouter un affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-155">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="4cf5a-156">Sur la page **affichage personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-156">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="4cf5a-157">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-157">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end


::: moniker range="o365-21vianet"

1. <span data-ttu-id="4cf5a-158">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-158">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="4cf5a-159">Sur la page **utilisateurs actifs** , sélectionnez **affichages** et sélectionnez **Ajouter un affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-159">On the **Active users** page, select **Views** and select **Add custom view**.</span></span>
  
3. <span data-ttu-id="4cf5a-160">Sur la page **affichage personnalisé** , entrez le nom de votre filtre, choisissez les conditions de votre filtre personnalisé, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-160">On the **Custom view** page, enter the name for your filter, choose the conditions for your custom filter, and then select **Add**.</span></span> <span data-ttu-id="4cf5a-161">Votre vue personnalisée est désormais incluse dans la liste déroulante des filtres.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-161">Your custom view is now included in the drop-down list of filters.</span></span>

::: moniker-end
    

## <a name="edit-or-delete-a-custom-user-view"></a><span data-ttu-id="4cf5a-162">Modifier ou supprimer une vue utilisateur personnalisée</span><span class="sxs-lookup"><span data-stu-id="4cf5a-162">Edit or delete a custom user view</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4cf5a-163">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-163">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="4cf5a-164">Sur la page **utilisateurs actifs** , sélectionnez **filtre**, sélectionnez le filtre à modifier, puis sélectionnez **modifier le filtre**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-164">On the **Active users** page, select **Filter**, select the filter you want to change, and then select **Edit filter**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="4cf5a-165">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-165">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="4cf5a-166">Sur la page **filtre personnalisé** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-166">On the **Custom filter** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="4cf5a-167">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-167">Or, to delete the filter, at the bottom of the page select **Delete**.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4cf5a-168">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-168">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="4cf5a-169">Sur la page **utilisateurs actifs** , sélectionnez **affichages**, sélectionnez le filtre à modifier, puis cliquez sur **modifier cet affichage**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-169">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="4cf5a-170">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-170">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="4cf5a-171">Sur la page **vue personnalisée** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-171">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="4cf5a-172">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **Supprimer l’affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-172">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4cf5a-173">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-173">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="4cf5a-174">Sur la page **utilisateurs actifs** , sélectionnez **affichages**, sélectionnez le filtre à modifier, puis cliquez sur **modifier cet affichage**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-174">On the **Active users** page, select **Views**, select the filter you want to change, and then select **Edit this view**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="4cf5a-175">Vous pouvez modifier uniquement les vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-175">You can edit only custom views.</span></span> 
  
3. <span data-ttu-id="4cf5a-176">Sur la page **vue personnalisée** , modifiez les informations selon vos besoins, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-176">On the **Custom view** page, edit the information as needed, and then select **Save**.</span></span> <span data-ttu-id="4cf5a-177">Sinon, pour supprimer le filtre, dans la partie inférieure de la page, sélectionnez **Supprimer l’affichage personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="4cf5a-177">Or, to delete the filter, at the bottom of the page select **Delete custom view**.</span></span> 

::: moniker-end


     