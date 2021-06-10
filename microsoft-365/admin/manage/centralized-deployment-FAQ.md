---
title: Forum aux questions sur le déploiement centralisé
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
description: Examinez les réponses aux questions fréquentes sur le déploiement centralisé à partir Microsoft 365'administration centrale.
ms.openlocfilehash: 60d7a91da738803976b6823009450124d7b57814
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51579301"
---
# <a name="centralized-deployment-faq"></a><span data-ttu-id="c6e48-103">Forum aux questions sur le déploiement centralisé</span><span class="sxs-lookup"><span data-stu-id="c6e48-103">Centralized Deployment FAQ</span></span>

<span data-ttu-id="c6e48-104">Le déploiement centralisé est la façon recommandée pour un administrateur Office 365 de déployer des modules de Office (Word, Excel, PowerPoint et Outlook) pour les utilisateurs et les groupes au sein d’une organisation, à condition que l’organisation réponde à toutes les exigences d’utilisation du déploiement centralisé, comme indiqué dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c6e48-104">Centralized Deployment is the recommended way for an Office 365 admin to deploy Office add-ins (Word, Excel, PowerPoint, and Outlook) to users and groups within an organization, provided the organization meets all requirements for using Centralized Deployment as outlined in this article.</span></span>   
  
## <a name="how-do-i-know-if-my-organization-is-set-up-for-centralized-deployment"></a><span data-ttu-id="c6e48-105">Comment savoir si mon organisation est définie pour un déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-105">How do I know if my organization is set up for Centralized Deployment?</span></span>  

<span data-ttu-id="c6e48-106">Le déploiement centralisé des add-ins nécessite que les utilisateurs utilisent Applications Microsoft 365 pour les grandes entreprises (et soient connectés à Office à l’aide de leurs informations d’identification de connexion organisationnelle) et qu’ils Exchange Online boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c6e48-106">Centralized deployment of add-ins requires that users are using Microsoft 365 Apps for enterprise (and are signed into Office using their organizational log-in credentials) and have Exchange Online mailboxes.</span></span> <span data-ttu-id="c6e48-107">Votre annuaire d’abonnements doit être dans un répertoire ou fédéré Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6e48-107">Your subscription directory must either be in, or federated to, Azure Active Directory.</span></span>  
 
<span data-ttu-id="c6e48-108">Le déploiement centralisé est uniquement pris en charge pour les boîtes aux lettres en ligne.</span><span class="sxs-lookup"><span data-stu-id="c6e48-108">Centralized Deployment is only supported for online mailboxes.</span></span> <span data-ttu-id="c6e48-109">Il ne prend pas en charge le déploiement vers des boîtes aux lettres Exchange sur site.</span><span class="sxs-lookup"><span data-stu-id="c6e48-109">It does not support deployment to on-premises Exchange mailboxes.</span></span>

<span data-ttu-id="c6e48-110">Vous pouvez utiliser le contrôle [de compatibilité du](centralized-deployment-of-add-ins.md#centralized-deployment-compatibility-checker)déploiement centralisé pour déterminer si votre abonnement est   éligible.</span><span class="sxs-lookup"><span data-stu-id="c6e48-110">You can use the [Centralized Deployment Compatibility Checker](centralized-deployment-of-add-ins.md#centralized-deployment-compatibility-checker) to determine if your subscription is eligible.</span></span> 
  
## <a name="how-do-you-target-add-in-user-assignments-with-centralized-deployment"></a><span data-ttu-id="c6e48-111">Comment cibler les affectations d’utilisateurs de add-in avec le déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-111">How do you target add-in user assignments with Centralized Deployment?</span></span>  

<span data-ttu-id="c6e48-112">Le déploiement centralisé prend en charge les affectations à des utilisateurs individuels, des groupes et à tous les utilisateurs du client.</span><span class="sxs-lookup"><span data-stu-id="c6e48-112">Centralized Deployment supports assignments to individual users, groups, and everyone in the tenant.</span></span> <span data-ttu-id="c6e48-113">Le déploiement centralisé peut être utilisé pour les utilisateurs de groupes de niveau supérieur ou de groupes sans groupes parents, mais pas pour les utilisateurs de groupes imbrmbrés ou de groupes qui ont des groupes parents.</span><span class="sxs-lookup"><span data-stu-id="c6e48-113">Centralized Deployment can be used for users in top-level groups or groups without parent groups, but not for users in nested groups or groups that have parent groups.</span></span> <span data-ttu-id="c6e48-114">Le déploiement centralisé fait également partie de la plupart des groupes Azure Active Directory, notamment les groupes Office 365, les listes de distribution et les groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c6e48-114">Centralized Deployment is also part of most Azure Active Directory groups, including Office 365 Groups, distribution lists, and security groups.</span></span>  

<span data-ttu-id="c6e48-115">Il est préférable d’utiliser des affectations de groupes plutôt que des affectations individuelles d’utilisateurs pour faciliter la gestion.</span><span class="sxs-lookup"><span data-stu-id="c6e48-115">It is better to use groups assignments instead of individual user assignment for easier management.</span></span>
 
<span data-ttu-id="c6e48-116">Pour plus d’informations, voir [Affectations d’utilisateurs et de groupes.](./centralized-deployment-of-add-ins.md?view=o365-worldwide#user-and-group-assignments)</span><span class="sxs-lookup"><span data-stu-id="c6e48-116">For more details, see [User and Group assignments](./centralized-deployment-of-add-ins.md?view=o365-worldwide#user-and-group-assignments).</span></span>  
   
## <a name="how-long-does-it-take-for-add-ins-to-show-up-for-all-users"></a><span data-ttu-id="c6e48-117">Combien de temps faut-il pour que les modules s’afficheront pour tous les utilisateurs ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-117">How long does it take for add-ins to show up for all users?</span></span>  

<span data-ttu-id="c6e48-118">L’exposition d’un add-in pour tous les utilisateurs peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="c6e48-118">It can take up to 24 hours for an add-in to show up for all users.</span></span> <span data-ttu-id="c6e48-119">Les mises à jour de modules, les modifications apportées à l’aide de l’activer ou de la désactiver, ou les suppressions de ces derniers peuvent prendre autant de temps.</span><span class="sxs-lookup"><span data-stu-id="c6e48-119">It can take the same amount of time for add-in updates, changes from turn on or turn off, or add-in removals.</span></span> 
  
## <a name="as-an-administrator-how-do-i-manage-the-user-access-to-add-ins-for-my-organization"></a><span data-ttu-id="c6e48-120">En tant qu’administrateur, comment puis-je gérer l’accès des utilisateurs aux add-ins pour mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-120">As an administrator, how do I manage the user access to add-ins for my organization?</span></span>

<span data-ttu-id="c6e48-121">Pour faciliter le déploiement des modules pour les utilisateurs, les groupes ou l’ensemble de votre organisation, nous recommandons aux administrateurs d’utiliser le déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="c6e48-121">For easy deployment of add-ins to users, groups, or to your entire organization, we recommend administrators use Centralized Deployment.</span></span>

<span data-ttu-id="c6e48-122">Pour plus d’informations sur la gestion de l’accès des utilisateurs, voir :</span><span class="sxs-lookup"><span data-stu-id="c6e48-122">For more information about managing user access, see:</span></span>
 - [<span data-ttu-id="c6e48-123">Empêcher les téléchargements de Office sur tous les clients (sauf Outlook)</span><span class="sxs-lookup"><span data-stu-id="c6e48-123">Prevent add-in downloads by turning off the Office Store across all clients (Except Outlook)</span></span>](./manage-addins-in-the-admin-center.md#prevent-add-in-downloads-by-turning-off-the-office-store-across-all-clients-except-outlook)
 - [<span data-ttu-id="c6e48-124">Désignation des administrateurs et utilisateurs qui peuvent installer et gérer des compléments pour Outlook</span><span class="sxs-lookup"><span data-stu-id="c6e48-124">Specify the administrators and users who can install and manage add-ins for Outlook</span></span>](/Exchange/specify-who-can-install-and-manage-add-ins-2013-help)

## <a name="will-centralized-deployment-provide-admins-the-flexibility-to-choose-the-deployment-method-for-outlook-add-ins"></a><span data-ttu-id="c6e48-125">Le déploiement centralisé offre-t-il aux administrateurs la possibilité de choisir la méthode de déploiement pour Outlook des modules ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-125">Will Centralized Deployment provide admins the flexibility to choose the deployment method for Outlook add-ins?</span></span>  

<span data-ttu-id="c6e48-126">Oui.</span><span class="sxs-lookup"><span data-stu-id="c6e48-126">Yes.</span></span> <span data-ttu-id="c6e48-127">Le déploiement centralisé offre aux administrateurs la possibilité de choisir l’une des trois méthodes de déploiement pour les Outlook lors du déploiement de ces derniers :</span><span class="sxs-lookup"><span data-stu-id="c6e48-127">Centralized Deployment provides admins the flexibility to choose one of three deployment methods for Outlook add-ins during add-in deployment:</span></span>

<span data-ttu-id="c6e48-128">**Fixe (valeur par défaut)**   Le add-in est déployé automatiquement pour les utilisateurs affectés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="c6e48-128">**Fixed (Default)**  The add-in is deployed automatically to the assigned users, and they cannot remove it.</span></span>  
 
<span data-ttu-id="c6e48-129">**Disponible** Les utilisateurs peuvent installer le Outlook en choisissant Home **> Get More add-ins > admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="c6e48-129">**Available** Users can install the add-in in Outlook by choosing **Home > Get More add-ins > Admin-managed**.</span></span>
 
<span data-ttu-id="c6e48-130">**Facultatif** Le add-in est déployé automatiquement pour les utilisateurs affectés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="c6e48-130">**Optional** The add-in is deployed automatically to the assigned users, but they can choose to remove it.</span></span>  
    
## <a name="can-admins-update-line-of-business-lob-add-ins"></a><span data-ttu-id="c6e48-131">Les administrateurs peuvent-ils mettre à jour des add-ins métier ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-131">Can admins update Line-of-Business (LOB) add-ins?</span></span>  

<span data-ttu-id="c6e48-132">Oui.</span><span class="sxs-lookup"><span data-stu-id="c6e48-132">Yes.</span></span> <span data-ttu-id="c6e48-133">Les administrateurs peuvent télécharger un nouveau fichier manifeste pour prendre en charge les modifications apportées aux métadonnées pour les add-ins LOB déployés par l’administrateur. Le add-in est mis à jour lors du prochain démarrage Office applications.</span><span class="sxs-lookup"><span data-stu-id="c6e48-133">Admins can upload a new manifest file to support metadata changes for admin-deployed LOB add-ins. The add-in updates the next time the Office applications starts.</span></span> <span data-ttu-id="c6e48-134">L'application web peut changer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c6e48-134">The web application can change at any time.</span></span>  
 
<span data-ttu-id="c6e48-135">Pour plus d’informations, voir le [add-in métier.](./manage-addins-in-the-admin-center.md)</span><span class="sxs-lookup"><span data-stu-id="c6e48-135">For more information, see [line-of-business add-in](./manage-addins-in-the-admin-center.md).</span></span>  

## <a name="can-admins-turn-off-add-ins"></a><span data-ttu-id="c6e48-136">Les administrateurs peuvent-ils désactiver les modules ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-136">Can admins turn off add-ins?</span></span>  

<span data-ttu-id="c6e48-137">Oui.</span><span class="sxs-lookup"><span data-stu-id="c6e48-137">Yes.</span></span> <span data-ttu-id="c6e48-138">Les administrateurs peuvent activer ou désactiver les modules qu’ils déploient pour tous les utilisateurs à partir du Centre d’administration Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6e48-138">Admins can turn on or off the add-ins they deploy for all users from the Microsoft admin center.</span></span>

<span data-ttu-id="c6e48-139">Pour plus d’informations, voir [États des modules complémentaires.](./manage-addins-in-the-admin-center.md#add-in-states)</span><span class="sxs-lookup"><span data-stu-id="c6e48-139">For more information, see [Add-in states](./manage-addins-in-the-admin-center.md#add-in-states).</span></span>  

##  <a name="can-admins-delete-or-remove-add-ins"></a><span data-ttu-id="c6e48-140">Les administrateurs peuvent-ils supprimer ou supprimer des modules ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-140">Can admins delete or remove add-ins?</span></span>

<span data-ttu-id="c6e48-141">Oui.</span><span class="sxs-lookup"><span data-stu-id="c6e48-141">Yes.</span></span> <span data-ttu-id="c6e48-142">Les administrateurs peuvent supprimer des modules qu’ils ont déployés pour tous les utilisateurs à partir du Centre d’administration Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6e48-142">Admins can delete add-ins they deployed for all users from the Microsoft admin center.</span></span>

<span data-ttu-id="c6e48-143">Pour plus d’informations, [voir Supprimer un module complémentaire.](./manage-addins-in-the-admin-center.md#delete-an-add-in)</span><span class="sxs-lookup"><span data-stu-id="c6e48-143">For more information, see [Delete an add-in](./manage-addins-in-the-admin-center.md#delete-an-add-in).</span></span> 
  
## <a name="can-admins-deploy-paid-add-ins-from-the-office-store-using-centralized-deployment"></a><span data-ttu-id="c6e48-144">Les administrateurs peuvent-ils déployer des add-ins payants à partir du Office Store à l’aide d’un déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-144">Can admins deploy paid add-ins from the Office Store using Centralized Deployment?</span></span> 

<span data-ttu-id="c6e48-145">Non.</span><span class="sxs-lookup"><span data-stu-id="c6e48-145">No.</span></span> <span data-ttu-id="c6e48-146">Pour l’instant, vous ne pouvez pas déployer de Office payants à partir du Office Store à l’aide du déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="c6e48-146">You can't deploy paid add-ins from the Office Store using Centralized Deployment at this time.</span></span>  
 
<span data-ttu-id="c6e48-147">Nous vous suggérons d’atteindre le développeur de logiciels indépendants pour que le add-in payant demande un fichier manifeste ou une URL.</span><span class="sxs-lookup"><span data-stu-id="c6e48-147">We suggest reaching out to the ISV Developer for the paid add-in to request a manifest file or a URL.</span></span> <span data-ttu-id="c6e48-148">L’administrateur client peut ensuite déployer le add-in en tant que add-in cœur de rôle à l’aide du déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="c6e48-148">The tenant admin can then deploy the add-in as a LOB add-in using Centralized Deployment.</span></span>
    
## <a name="which-admin-role-do-i-need-to-manage-add-ins-for-my-organization"></a><span data-ttu-id="c6e48-149">Quel rôle d’administrateur ai-je besoin pour gérer les add-ins pour mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="c6e48-149">Which admin role do I need to manage add-ins for my organization?</span></span>  

<span data-ttu-id="c6e48-150">L’administrateur général est le rôle recommandé avec un accès complet au cycle de vie de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="c6e48-150">Global Admin is the recommended role with complete access to add-in management lifecycle.</span></span> <span data-ttu-id="c6e48-151">Les autres rôles d’administrateur ont un accès limité au cycle de vie du déploiement des applications.</span><span class="sxs-lookup"><span data-stu-id="c6e48-151">Other Admin roles have a limited access to add-in deployment lifecycle.</span></span> <span data-ttu-id="c6e48-152">Si vous êtes la personne qui a acheté votre abonnement Microsoft 365 entreprise, vous êtes l’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="c6e48-152">If you're the person who purchased your Microsoft 365 for business subscription, you are the Global admin.</span></span> 
 
<span data-ttu-id="c6e48-153">Votre abonnement est livré avec un ensemble de rôles d’administrateur que vous pouvez attribuer à d’autres utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c6e48-153">Your subscription comes with a set of admin roles that you can assign to other users in your organization.</span></span> <span data-ttu-id="c6e48-154">Chaque rôle d’administrateur est map pour les fonctions d’entreprise courantes et donne aux membres de votre organisation des autorisations pour effectuer des tâches spécifiques dans Microsoft 365 centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="c6e48-154">Each admin role maps to common business functions and gives people in your organization permissions to perform specific tasks in the Microsoft 365 admin center.</span></span>  
 
<span data-ttu-id="c6e48-155">Pour plus d’informations, voir [Attribuer des rôles d’administrateur.](../add-users/assign-admin-roles.md?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="c6e48-155">For more information, see [Assign admin roles](../add-users/assign-admin-roles.md?view=o365-worldwide).</span></span> 