---
title: Comprendre les abonnements et les licences dans Microsoft 365 pour les entreprises
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
search.appverid:
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 7ac93507-0e38-4398-8bfe-9c1d123cb387
description: 'Découvrez les abonnements et les licences dans Microsoft 365 pour les entreprises et les personnes qui peuvent attribuer des licences et ce qui se passe quand vous attribuez une licence à quelqu’un. '
ms.custom:
- okr_SMB
- AdminSurgePortfolio
ms.openlocfilehash: f83b2069bd1b4c86e2198252a54ed2e8e5c55a04
ms.sourcegitcommit: bd5a08785b5ec320b04b02f8776e28bce5fb448f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "44844679"
---
# <a name="understand-subscriptions-and-licenses-in-microsoft-365-for-business"></a><span data-ttu-id="4040c-103">Comprendre les abonnements et les licences dans Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="4040c-103">Understand subscriptions and licenses in Microsoft 365 for business</span></span>

<span data-ttu-id="4040c-104">Cet article explique la relation entre les abonnements et les licences, et fournit des informations supplémentaires sur les [personnes autorisées à attribuer des licences](#find-out-who-can-assign-licenses), la [compréhension de ce qui se produit lorsque vous attribuez une licence à un utilisateur](#understand-what-happens-when-you-assign-a-license-to-someone), et [sur le nombre d’appareils pouvant installer Office sur](#how-many-devices-can-people-install-office-on).</span><span class="sxs-lookup"><span data-stu-id="4040c-104">This article explains the relationship between subscriptions and licenses, and provides additional information about [who can assign licenses](#find-out-who-can-assign-licenses), [understanding what happens when you assign a license to someone](#understand-what-happens-when-you-assign-a-license-to-someone), and [how many devices can people install Office on](#how-many-devices-can-people-install-office-on).</span></span> <span data-ttu-id="4040c-105">Elle inclut également des liens vers des [licences de présentation des licences pour les boîtes aux lettres non utilisateur](#understand-licenses-for-non-user-mailboxes)et [des articles sur la gestion des licences](#articles-about-managing-licenses).</span><span class="sxs-lookup"><span data-stu-id="4040c-105">It also includes links to [understanding licenses for non-user mailboxes](#understand-licenses-for-non-user-mailboxes), and [Articles about managing licenses](#articles-about-managing-licenses).</span></span>
  
<span data-ttu-id="4040c-106">Lorsque vous achetez un abonnement à Microsoft 365 pour les entreprises, vous vous inscrivez à un ensemble d’applications et de services que vous payez mensuellement ou annuellement.</span><span class="sxs-lookup"><span data-stu-id="4040c-106">When you buy a subscription to Microsoft 365 for business, you sign up for a set of applications and services that you pay for on a either a monthly or an annual basis.</span></span> <span data-ttu-id="4040c-107">Les applications et les services que vous recevez dans le cadre de votre abonnement dépendent du produit que vous avez acheté, tel que Microsoft 365 Apps for Business ou Microsoft 365 Business standard.</span><span class="sxs-lookup"><span data-stu-id="4040c-107">The applications and services that you receive as part of your subscription depend on which product you purchased, such as Microsoft 365 Apps for business or Microsoft 365 Business Standard.</span></span> <span data-ttu-id="4040c-108">Vous pouvez consulter les informations fournies avec chaque produit sur la [page acheter Microsoft 365](https://products.office.com/compare-all-microsoft-office-products?&activetab=tab:primaryr1).</span><span class="sxs-lookup"><span data-stu-id="4040c-108">You can review what comes with each product on the [Buy Microsoft 365 page](https://products.office.com/compare-all-microsoft-office-products?&activetab=tab:primaryr1).</span></span> 

<span data-ttu-id="4040c-109">Vous pouvez consulter différentes options de licence disponibles dans [Microsoft 365 pour les petites et moyennes entreprises](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/licensing-microsoft-365-in-smb)</span><span class="sxs-lookup"><span data-stu-id="4040c-109">You can review different Licensing options available in [Microsoft 365 for small and medium-sized businesses](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/licensing-microsoft-365-in-smb)</span></span>

<span data-ttu-id="4040c-110">Lorsque vous achetez un abonnement, vous spécifiez le nombre de licences dont vous avez besoin, en fonction du nombre de personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4040c-110">When you buy a subscription, you specify the number of licenses that you need, based on how many people you have in your organization.</span></span> <span data-ttu-id="4040c-111">Une fois l'achat terminé, vous créez des comptes pour les utilisateurs, puis attribuez une licence à chacun.</span><span class="sxs-lookup"><span data-stu-id="4040c-111">After your purchase is complete, you create accounts for people, and then assign a license to each person.</span></span> <span data-ttu-id="4040c-112">À mesure que les besoins de votre organisation évoluent, vous pouvez acheter des licences supplémentaires pour accueillir de nouvelles personnes ou réattribuer des licences à d’autres utilisateurs lorsqu’un utilisateur quitte votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4040c-112">As your organizational needs change, you can buy more licenses to accommodate new people, or reassign licenses to other users when someone leaves your organization.</span></span> 

<span data-ttu-id="4040c-113">Si vous disposez de plusieurs abonnements, vous pouvez attribuer des licences à différentes personnes pour chaque abonnement.</span><span class="sxs-lookup"><span data-stu-id="4040c-113">If you have more than one subscription, you can assign licenses to different people for each subscription.</span></span> <span data-ttu-id="4040c-114">Par exemple, tous vos utilisateurs peuvent être affectés à tous les services et applications Microsoft 365 dans le cadre d’un abonnement Microsoft 365 Business standard, tandis qu’un sous-ensemble d’utilisateurs peut également être affecté à Visio online via un abonnement Visio distinct.</span><span class="sxs-lookup"><span data-stu-id="4040c-114">For example, all of your users could be assigned to all Microsoft 365 applications and services as part of an Microsoft 365 Business Standard subscription, while a subset of users could also be assigned to Visio Online through a separate Visio subscription.</span></span> 

  
## <a name="find-out-who-can-assign-licenses"></a><span data-ttu-id="4040c-115">Identifier qui peut attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="4040c-115">Find out who can assign licenses</span></span>

<span data-ttu-id="4040c-116">Different types of admins can work with licenses in different ways, depending on their roles.</span><span class="sxs-lookup"><span data-stu-id="4040c-116">Different types of admins can work with licenses in different ways, depending on their roles.</span></span> <span data-ttu-id="4040c-117">The following table lists the most common options.</span><span class="sxs-lookup"><span data-stu-id="4040c-117">The following table lists the most common options.</span></span> <span data-ttu-id="4040c-118">For a complete list of admin roles and privileges, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4040c-118">For a complete list of admin roles and privileges, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  
|<span data-ttu-id="4040c-119">**Rôle d'administrateur**</span><span class="sxs-lookup"><span data-stu-id="4040c-119">**Admin role**</span></span>|<span data-ttu-id="4040c-120">**Attribuer une licence**</span><span class="sxs-lookup"><span data-stu-id="4040c-120">**Assign a license**</span></span>|<span data-ttu-id="4040c-121">**Supprimer une licence**</span><span class="sxs-lookup"><span data-stu-id="4040c-121">**Remove a license**</span></span>|<span data-ttu-id="4040c-122">**Acheter des licences supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="4040c-122">**Purchase more licenses**</span></span>|<span data-ttu-id="4040c-123">**Supprimer un compte**</span><span class="sxs-lookup"><span data-stu-id="4040c-123">**Delete an account**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4040c-124">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="4040c-124">Global admin</span></span>  <br/> |<span data-ttu-id="4040c-125">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-125">Yes</span></span>  <br/> |<span data-ttu-id="4040c-126">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-126">Yes</span></span>  <br/> |<span data-ttu-id="4040c-127">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-127">Yes</span></span>  <br/> |<span data-ttu-id="4040c-128">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-128">Yes</span></span>  <br/> |
|<span data-ttu-id="4040c-129">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="4040c-129">Billing admin</span></span>  <br/> |<span data-ttu-id="4040c-130">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-130">No</span></span>  <br/> |<span data-ttu-id="4040c-131">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-131">No</span></span>  <br/> |<span data-ttu-id="4040c-132">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-132">Yes</span></span>  <br/> |<span data-ttu-id="4040c-133">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-133">No</span></span>  <br/> |
|<span data-ttu-id="4040c-134">Administrateur de gestion des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4040c-134">User management admin</span></span>  <br/> |<span data-ttu-id="4040c-135">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-135">Yes</span></span>  <br/> |<span data-ttu-id="4040c-136">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-136">Yes</span></span>  <br/> |<span data-ttu-id="4040c-137">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-137">No</span></span>  <br/> |<span data-ttu-id="4040c-138">Oui</span><span class="sxs-lookup"><span data-stu-id="4040c-138">Yes</span></span>  <br/> |
|<span data-ttu-id="4040c-139">Administrateur de service</span><span class="sxs-lookup"><span data-stu-id="4040c-139">Service admin</span></span>  <br/> |<span data-ttu-id="4040c-140">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-140">No</span></span>  <br/> |<span data-ttu-id="4040c-141">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-141">No</span></span>  <br/> |<span data-ttu-id="4040c-142">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-142">No</span></span>  <br/> |<span data-ttu-id="4040c-143">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-143">No</span></span>  <br/> |
|<span data-ttu-id="4040c-144">Administrateur de mots de passe</span><span class="sxs-lookup"><span data-stu-id="4040c-144">Password admin</span></span>  <br/> |<span data-ttu-id="4040c-145">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-145">No</span></span>  <br/> |<span data-ttu-id="4040c-146">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-146">No</span></span>  <br/> |<span data-ttu-id="4040c-147">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-147">No</span></span>  <br/> |<span data-ttu-id="4040c-148">Non</span><span class="sxs-lookup"><span data-stu-id="4040c-148">No</span></span>  <br/> |
   
## <a name="understand-what-happens-when-you-assign-a-license-to-someone"></a><span data-ttu-id="4040c-149">Que se passe-t-il lorsque vous attribuez une licence à quelqu'un ?</span><span class="sxs-lookup"><span data-stu-id="4040c-149">Understand what happens when you assign a license to someone</span></span>

<span data-ttu-id="4040c-150">Le tableau suivant indique ce qui se produit automatiquement lorsque vous attribuez une licence à quelqu'un :</span><span class="sxs-lookup"><span data-stu-id="4040c-150">The following table lists what automatically happens when you assign a license to someone:</span></span>
  
|<span data-ttu-id="4040c-151">**Si l'abonnement inclut ce service**</span><span class="sxs-lookup"><span data-stu-id="4040c-151">**If the subscription has this service**</span></span>|<span data-ttu-id="4040c-152">**Cet événement se produit automatiquement**</span><span class="sxs-lookup"><span data-stu-id="4040c-152">**This automatically happens**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4040c-153">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4040c-153">Exchange Online</span></span>  <br/> |<span data-ttu-id="4040c-154">Une boîte aux lettres est créée pour cette personne.</span><span class="sxs-lookup"><span data-stu-id="4040c-154">A mailbox is created for that person.</span></span>  <br/> <span data-ttu-id="4040c-155">Pour plus d’informations sur le contrat SLA pour cette tâche, voir [«Configuration... messages dans le centre d’administration Microsoft 365](https://support.microsoft.com/help/2635238/setting-up-messages-in-the-office-365-admin-center).</span><span class="sxs-lookup"><span data-stu-id="4040c-155">To learn about the SLA for this task to be completed, see ["Setting up..." messages in the Microsoft 365 admin center](https://support.microsoft.com/help/2635238/setting-up-messages-in-the-office-365-admin-center).</span></span> |
|<span data-ttu-id="4040c-156">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4040c-156">SharePoint Online</span></span>  <br/> |<span data-ttu-id="4040c-157">Les autorisations de modification du site d'équipe SharePoint Online par défaut sont attribuées à cette personne.</span><span class="sxs-lookup"><span data-stu-id="4040c-157">Edit permissions to the default SharePoint Online team site are assigned to that person.</span></span>  <br/> |
|<span data-ttu-id="4040c-158">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="4040c-158">Skype for Business Online</span></span>  <br/> |<span data-ttu-id="4040c-159">La personne aura accès aux fonctionnalités associées à la licence.</span><span class="sxs-lookup"><span data-stu-id="4040c-159">The person will have access to the features associated with the license.</span></span>  <br/> |
|<span data-ttu-id="4040c-160">Applications Microsoft 365 pour les grandes entreprises</span><span class="sxs-lookup"><span data-stu-id="4040c-160">Microsoft 365 Apps for enterprise</span></span>  <br/> |<span data-ttu-id="4040c-161">La personne pourra télécharger Microsoft Office sur un maximum de 5 Mac ou PC, 5 tablettes et 5 smartphones.</span><span class="sxs-lookup"><span data-stu-id="4040c-161">The person will be able to download Microsoft Office on up to 5 Macs or PCs, 5 tablets, and 5 smartphones.</span></span>  <br/> |
   
## <a name="how-many-devices-can-people-install-office-on"></a><span data-ttu-id="4040c-162">Sur combien d'appareils les utilisateurs peuvent-ils installer Office ?</span><span class="sxs-lookup"><span data-stu-id="4040c-162">How many devices can people install Office on?</span></span>

<span data-ttu-id="4040c-163">Si votre abonnement comprend un des produits suivants, chaque personne peut installer Office sur un maximum de 5 PC ou Mac, 5 tablettes et 5 téléphones.</span><span class="sxs-lookup"><span data-stu-id="4040c-163">If your subscription includes any of the following products, each person can install Office on up to 5 PCs or Mac, 5 tablets, and 5 phones.</span></span>
  
- <span data-ttu-id="4040c-164">Microsoft 365 Apps for business</span><span class="sxs-lookup"><span data-stu-id="4040c-164">Microsoft 365 Apps for business</span></span>
    
- <span data-ttu-id="4040c-165">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="4040c-165">Microsoft 365 Business Standard</span></span>
    
- <span data-ttu-id="4040c-166">Microsoft 365 Apps for enterprise</span><span class="sxs-lookup"><span data-stu-id="4040c-166">Microsoft 365 Apps for enterprise</span></span>
    
- <span data-ttu-id="4040c-167">Office 365 Entreprise E3</span><span class="sxs-lookup"><span data-stu-id="4040c-167">Office 365 Enterprise E3</span></span>
    
- <span data-ttu-id="4040c-168">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="4040c-168">Office 365 Enterprise E5</span></span>
    
## <a name="understand-licenses-for-non-user-mailboxes"></a><span data-ttu-id="4040c-169">Comprendre les licences pour les boîtes aux lettres non-utilisateur</span><span class="sxs-lookup"><span data-stu-id="4040c-169">Understand licenses for non-user mailboxes</span></span>

<span data-ttu-id="4040c-170">You don't need to assign licenses to resource mailboxes, room mailboxes, and shared mailboxes, except when they are over their storage quota of 50 gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="4040c-170">You don't need to assign licenses to resource mailboxes, room mailboxes, and shared mailboxes, except when they are over their storage quota of 50 gigabytes (GB).</span></span> <span data-ttu-id="4040c-171">For more about non-user mailboxes, see the following articles:</span><span class="sxs-lookup"><span data-stu-id="4040c-171">For more about non-user mailboxes, see the following articles:</span></span>
  
- [<span data-ttu-id="4040c-172">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="4040c-172">Create a shared mailbox</span></span>](../../admin/email/create-a-shared-mailbox.md)
    
- <span data-ttu-id="4040c-173">[Boîtes aux lettres partagées dans Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=847433) pour tous les autres plans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4040c-173">[Shared Mailboxes in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=847433) for all other Microsoft 365 plans.</span></span> 
    
- [<span data-ttu-id="4040c-174">Créer et gérer des boîtes aux lettres de salle</span><span class="sxs-lookup"><span data-stu-id="4040c-174">Create and Manage Room Mailboxes</span></span>](https://go.microsoft.com/fwlink/p/?linkid=847434)
    
- <span data-ttu-id="4040c-175">[Gérer des boîtes aux lettres de ressource](https://go.microsoft.com/fwlink/p/?linkid=847435).</span><span class="sxs-lookup"><span data-stu-id="4040c-175">[Manage Equipment Mailboxes](https://go.microsoft.com/fwlink/p/?linkid=847435)</span></span>
    
## <a name="articles-about-managing-licenses"></a><span data-ttu-id="4040c-176">Articles sur la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="4040c-176">Articles about managing licenses</span></span>

- [<span data-ttu-id="4040c-177">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4040c-177">Assign licenses to users</span></span>](../../admin/manage/assign-licenses-to-users.md)
    
- [<span data-ttu-id="4040c-178">Retirer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4040c-178">Remove licenses from users</span></span>](../../admin/manage/remove-licenses-from-users.md)
    
- [<span data-ttu-id="4040c-179">Acheter des licences pour votre abonnement</span><span class="sxs-lookup"><span data-stu-id="4040c-179">Buy licenses for your subscription</span></span>](buy-licenses.md)
    
- [<span data-ttu-id="4040c-180">Acheter un autre abonnement</span><span class="sxs-lookup"><span data-stu-id="4040c-180">Buy another subscription</span></span>](../buy-another-subscription.md)
    
- [<span data-ttu-id="4040c-181">Acheter ou modifier un composant additionnel</span><span class="sxs-lookup"><span data-stu-id="4040c-181">Buy or edit an add-on</span></span>](../buy-or-edit-an-add-on.md)
    
- [<span data-ttu-id="4040c-182">Supprimer des licences de votre abonnement</span><span class="sxs-lookup"><span data-stu-id="4040c-182">Remove licenses from your subscription</span></span>](remove-licenses-from-subscription.md)
    
- [<span data-ttu-id="4040c-183">Résoudre les conflits de licence</span><span class="sxs-lookup"><span data-stu-id="4040c-183">Resolve license conflicts</span></span>](../../admin/manage/resolve-license-conflicts.md)
    
- [<span data-ttu-id="4040c-184">Gérer les licences utilisateur Yammer</span><span class="sxs-lookup"><span data-stu-id="4040c-184">Manage Yammer user licenses</span></span>](https://docs.microsoft.com/yammer/manage-yammer-users/manage-yammer-licenses-in-office-365)
