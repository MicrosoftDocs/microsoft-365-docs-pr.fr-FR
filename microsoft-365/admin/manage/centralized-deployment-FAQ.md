---
title: Forum aux questions sur le déploiement centralisé
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
description: Passez en revue les réponses aux questions fréquemment posées sur le déploiement centralisé à partir du centre d’administration Microsoft 365.
ms.openlocfilehash: b1b5ccbb5373bf5d536208efdfe487bc0c872f25
ms.sourcegitcommit: 222fc3f8841de82b1b558f47db8a79aa5054d0ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "45102883"
---
# <a name="centralized-deployment-faq"></a><span data-ttu-id="2a390-103">Forum aux questions sur le déploiement centralisé</span><span class="sxs-lookup"><span data-stu-id="2a390-103">Centralized Deployment FAQ</span></span>

<span data-ttu-id="2a390-104">Le déploiement centralisé est la méthode recommandée pour un administrateur Office 365 pour déployer des compléments Office (Word, Excel, PowerPoint et Outlook) pour les utilisateurs et les groupes au sein d’une organisation, à condition que l’organisation remplisse toutes les conditions d’utilisation du déploiement centralisé comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2a390-104">Centralized Deployment is the recommended way for an Office 365 admin to deploy Office add-ins (Word, Excel, PowerPoint, and Outlook) to users and groups within an organization, provided the organization meets all requirements for using Centralized Deployment as outlined in this article.</span></span>   
  
## <a name="how-do-i-know-if-my-organization-is-set-up-for-centralized-deployment"></a><span data-ttu-id="2a390-105">Comment savoir si mon organisation est configurée pour un déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="2a390-105">How do I know if my organization is set up for Centralized Deployment?</span></span>  

<span data-ttu-id="2a390-106">Le déploiement centralisé des compléments nécessite que les utilisateurs utilisent les applications Microsoft 365 pour Enterprise (et sont connectés à Office à l’aide de leurs informations d’identification de connexion de l’organisation) et disposent de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2a390-106">Centralized deployment of add-ins requires that users are using Microsoft 365 Apps for enterprise (and are signed into Office using their organizational log-in credentials) and have Exchange Online mailboxes.</span></span> <span data-ttu-id="2a390-107">Le répertoire de votre abonnement doit être dans Azure Active Directory ou être fédéré.</span><span class="sxs-lookup"><span data-stu-id="2a390-107">Your subscription directory must either be in, or federated to, Azure Active Directory.</span></span>  
 
<span data-ttu-id="2a390-108">Le déploiement centralisé est uniquement pris en charge pour les boîtes aux lettres en ligne.</span><span class="sxs-lookup"><span data-stu-id="2a390-108">Centralized Deployment is only supported for online mailboxes.</span></span> <span data-ttu-id="2a390-109">Il ne prend pas en charge le déploiement vers des boîtes aux lettres Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="2a390-109">It does not support deployment to on-premises Exchange mailboxes.</span></span>

<span data-ttu-id="2a390-110">Vous pouvez utiliser le [Vérificateur de compatibilité du déploiement centralisé](centralized-deployment-of-add-ins.md#centralized-deployment-compatibility-checker)   pour déterminer si votre abonnement est éligible.</span><span class="sxs-lookup"><span data-stu-id="2a390-110">You can use the [Centralized Deployment Compatibility Checker](centralized-deployment-of-add-ins.md#centralized-deployment-compatibility-checker) to determine if your subscription is eligible.</span></span> 
  
## <a name="how-do-you-target-add-in-user-assignments-with-centralized-deployment"></a><span data-ttu-id="2a390-111">Comment ciblez-vous les affectations d’utilisateurs de compléments avec un déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="2a390-111">How do you target add-in user assignments with Centralized Deployment?</span></span>  

<span data-ttu-id="2a390-112">Le déploiement centralisé prend en charge les affectations à des utilisateurs individuels, des groupes et tout le monde dans le client.</span><span class="sxs-lookup"><span data-stu-id="2a390-112">Centralized Deployment supports assignments to individual users, groups, and everyone in the tenant.</span></span> <span data-ttu-id="2a390-113">Le déploiement centralisé peut être utilisé pour les utilisateurs dans les groupes de niveau supérieur ou les groupes sans groupes parents, mais pas pour les utilisateurs dans les groupes ou groupes imbriqués ayant des groupes parents.</span><span class="sxs-lookup"><span data-stu-id="2a390-113">Centralized Deployment can be used for users in top-level groups or groups without parent groups, but not for users in nested groups or groups that have parent groups.</span></span> <span data-ttu-id="2a390-114">Le déploiement centralisé fait également partie de la plupart des groupes Azure Active Directory, y compris les groupes Office 365, les listes de distribution et les groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2a390-114">Centralized Deployment is also part of most Azure Active Directory groups, including Office 365 Groups, distribution lists, and security groups.</span></span>  

<span data-ttu-id="2a390-115">Il est préférable d’utiliser des affectations de groupes au lieu de l’affectation individuelle des utilisateurs pour faciliter la gestion.</span><span class="sxs-lookup"><span data-stu-id="2a390-115">It is better to use groups assignments instead of individual user assignment for easier management.</span></span>
 
<span data-ttu-id="2a390-116">Pour plus d’informations, consultez la rubrique [attributions d’utilisateurs et de groupes](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide#user-and-group-assignments).</span><span class="sxs-lookup"><span data-stu-id="2a390-116">For more details, see [User and Group assignments](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide#user-and-group-assignments).</span></span>  
   
## <a name="how-long-does-it-take-for-add-ins-to-show-up-for-all-users"></a><span data-ttu-id="2a390-117">Combien de temps faut-il pour que les compléments s’affichent pour tous les utilisateurs ?</span><span class="sxs-lookup"><span data-stu-id="2a390-117">How long does it take for add-ins to show up for all users?</span></span>  

<span data-ttu-id="2a390-118">Un complément peut prendre jusqu’à 24 heures pour s’afficher pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2a390-118">It can take up to 24 hours for an add-in to show up for all users.</span></span> <span data-ttu-id="2a390-119">La mise à jour des compléments peut prendre le même temps, passer de l’activation ou de la désactivation, ou des suppressions de compléments.</span><span class="sxs-lookup"><span data-stu-id="2a390-119">It can take the same amount of time for add-in updates, changes from turn on or turn off, or add-in removals.</span></span> 
  
## <a name="as-an-administrator-how-do-i-manage-the-user-access-to-add-ins-for-my-organization"></a><span data-ttu-id="2a390-120">En tant qu’administrateur, comment puis-je gérer l’accès des utilisateurs aux compléments pour mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="2a390-120">As an administrator, how do I manage the user access to add-ins for my organization?</span></span>

<span data-ttu-id="2a390-121">Pour faciliter le déploiement des compléments pour les utilisateurs, les groupes ou l’ensemble de votre organisation, nous recommandons aux administrateurs d’utiliser un déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="2a390-121">For easy deployment of add-ins to users, groups, or to your entire organization, we recommend administrators use Centralized Deployment.</span></span>

<span data-ttu-id="2a390-122">Pour plus d’informations sur la gestion de l’accès des utilisateurs, voir :</span><span class="sxs-lookup"><span data-stu-id="2a390-122">For more information about managing user access, see:</span></span>
 - [<span data-ttu-id="2a390-123">Empêcher les téléchargements de compléments en désactivant l’Office Store sur tous les clients (sauf Outlook)</span><span class="sxs-lookup"><span data-stu-id="2a390-123">Prevent add-in downloads by turning off the Office Store across all clients (Except Outlook)</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#prevent-add-in-downloads-by-turning-off-the-office-store-across-all-clients-except-outlook)
 - [<span data-ttu-id="2a390-124">Désignation des administrateurs et utilisateurs qui peuvent installer et gérer des compléments pour Outlook</span><span class="sxs-lookup"><span data-stu-id="2a390-124">Specify the administrators and users who can install and manage add-ins for Outlook</span></span>](https://docs.microsoft.com/Exchange/specify-who-can-install-and-manage-add-ins-2013-help)

## <a name="will-centralized-deployment-provide-admins-the-flexibility-to-choose-the-deployment-method-for-outlook-add-ins"></a><span data-ttu-id="2a390-125">Le déploiement centralisé offrira-t-il la souplesse nécessaire pour choisir la méthode de déploiement des compléments Outlook ?</span><span class="sxs-lookup"><span data-stu-id="2a390-125">Will Centralized Deployment provide admins the flexibility to choose the deployment method for Outlook add-ins?</span></span>  

<span data-ttu-id="2a390-126">Oui.</span><span class="sxs-lookup"><span data-stu-id="2a390-126">Yes.</span></span> <span data-ttu-id="2a390-127">Le déploiement centralisé offre aux administrateurs la souplesse nécessaire pour choisir l’une des trois méthodes de déploiement pour les compléments Outlook lors du déploiement de compléments :</span><span class="sxs-lookup"><span data-stu-id="2a390-127">Centralized Deployment provides admins the flexibility to choose one of three deployment methods for Outlook add-ins during add-in deployment:</span></span>

<span data-ttu-id="2a390-128">**Fixed (valeur par défaut)**   Le complément est déployé automatiquement sur les utilisateurs affectés, et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="2a390-128">**Fixed (Default)**  The add-in is deployed automatically to the assigned users, and they cannot remove it.</span></span>  
 
<span data-ttu-id="2a390-129">**Disponible** Les utilisateurs peuvent installer le complément dans Outlook en choisissant **accueil > obtenir d’autres compléments > gérés**par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2a390-129">**Available** Users can install the add-in in Outlook by choosing **Home > Get More add-ins > Admin-managed**.</span></span>
 
<span data-ttu-id="2a390-130">**Facultatif** Le complément est déployé automatiquement sur les utilisateurs attribués, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="2a390-130">**Optional** The add-in is deployed automatically to the assigned users, but they can choose to remove it.</span></span>  
    
## <a name="can-admins-update-line-of-business-lob-add-ins"></a><span data-ttu-id="2a390-131">Les administrateurs peuvent-ils mettre à jour des compléments métier (LOB) ?</span><span class="sxs-lookup"><span data-stu-id="2a390-131">Can admins update Line-of-Business (LOB) add-ins?</span></span>  

<span data-ttu-id="2a390-132">Oui.</span><span class="sxs-lookup"><span data-stu-id="2a390-132">Yes.</span></span> <span data-ttu-id="2a390-133">Les administrateurs peuvent télécharger un nouveau fichier manifeste afin de prendre en charge les modifications de métadonnées pour les compléments métier déployés par l’administrateur. Le complément est mis à jour lors du prochain démarrage des applications Office.</span><span class="sxs-lookup"><span data-stu-id="2a390-133">Admins can upload a new manifest file to support metadata changes for admin-deployed LOB add-ins. The add-in updates the next time the Office applications starts.</span></span> <span data-ttu-id="2a390-134">L'application web peut changer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="2a390-134">The web application can change at any time.</span></span>  
 
<span data-ttu-id="2a390-135">Pour plus d’informations, reportez-vous à la rubrique [line-of-Business Add-in](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#more-about-office-add-ins-security).</span><span class="sxs-lookup"><span data-stu-id="2a390-135">For more information, see [line-of-business add-in](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#more-about-office-add-ins-security).</span></span>  

## <a name="can-admins-turn-off-add-ins"></a><span data-ttu-id="2a390-136">Les administrateurs peuvent-ils désactiver les compléments ?</span><span class="sxs-lookup"><span data-stu-id="2a390-136">Can admins turn off add-ins?</span></span>  

<span data-ttu-id="2a390-137">Oui.</span><span class="sxs-lookup"><span data-stu-id="2a390-137">Yes.</span></span> <span data-ttu-id="2a390-138">Les administrateurs peuvent activer ou désactiver les compléments qu’ils déploient pour tous les utilisateurs à partir du centre d’administration Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a390-138">Admins can turn on or off the add-ins they deploy for all users from the Microsoft admin center.</span></span>

<span data-ttu-id="2a390-139">Pour plus d’informations, consultez la rubrique [États des compléments](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#add-in-states).</span><span class="sxs-lookup"><span data-stu-id="2a390-139">For more information, see [Add-in states](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#add-in-states).</span></span>  

##  <a name="can-admins-delete-or-remove-add-ins"></a><span data-ttu-id="2a390-140">Les administrateurs peuvent-ils supprimer ou supprimer des compléments ?</span><span class="sxs-lookup"><span data-stu-id="2a390-140">Can admins delete or remove add-ins?</span></span>

<span data-ttu-id="2a390-141">Oui.</span><span class="sxs-lookup"><span data-stu-id="2a390-141">Yes.</span></span> <span data-ttu-id="2a390-142">Les administrateurs peuvent supprimer des compléments qu’ils ont déployés pour tous les utilisateurs à partir du centre d’administration Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a390-142">Admins can delete add-ins they deployed for all users from the Microsoft admin center.</span></span>

<span data-ttu-id="2a390-143">Pour plus d’informations, consultez la rubrique [Delete an Add-in](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#delete-an-add-in).</span><span class="sxs-lookup"><span data-stu-id="2a390-143">For more information, see [Delete an add-in](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center#delete-an-add-in).</span></span> 
  
## <a name="can-admins-deploy-paid-add-ins-from-the-office-store-using-centralized-deployment"></a><span data-ttu-id="2a390-144">Les administrateurs peuvent-ils déployer des compléments payants à partir de l’Office Store à l’aide d’un déploiement centralisé ?</span><span class="sxs-lookup"><span data-stu-id="2a390-144">Can admins deploy paid add-ins from the Office Store using Centralized Deployment?</span></span> 

<span data-ttu-id="2a390-145">Non.</span><span class="sxs-lookup"><span data-stu-id="2a390-145">No.</span></span> <span data-ttu-id="2a390-146">Vous ne pouvez pas déployer des compléments payants à partir de l’Office Store à l’aide du déploiement centralisé pour le moment.</span><span class="sxs-lookup"><span data-stu-id="2a390-146">You can't deploy paid add-ins from the Office Store using Centralized Deployment at this time.</span></span>  
 
<span data-ttu-id="2a390-147">Nous vous suggérons de contacter le développeur ISV pour le complément payant afin de demander un fichier manifeste ou une URL.</span><span class="sxs-lookup"><span data-stu-id="2a390-147">We suggest reaching out to the ISV Developer for the paid add-in to request a manifest file or a URL.</span></span> <span data-ttu-id="2a390-148">L’administrateur client peut ensuite déployer le complément en tant que complément métier à l’aide du déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="2a390-148">The tenant admin can then deploy the add-in as a LOB add-in using Centralized Deployment.</span></span>
    
## <a name="which-admin-role-do-i-need-to-manage-add-ins-for-my-organization"></a><span data-ttu-id="2a390-149">Quel rôle d’administrateur dois-je utiliser pour gérer les compléments pour mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="2a390-149">Which admin role do I need to manage add-ins for my organization?</span></span>  

<span data-ttu-id="2a390-150">Vous devez disposer du rôle d’administrateur global pour gérer les compléments. Si vous êtes la personne qui a acheté votre abonnement Microsoft 365 pour les entreprises, vous êtes l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2a390-150">You must have the Global admin role to manage add-ins. If you're the person who purchased your Microsoft 365 for business subscription, you are the Global admin.</span></span> 
 
<span data-ttu-id="2a390-151">Votre abonnement est fourni avec un ensemble de rôles d’administrateur que vous pouvez attribuer à d’autres utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2a390-151">Your subscription comes with a set of admin roles that you can assign to other users in your organization.</span></span> <span data-ttu-id="2a390-152">Chaque rôle d’administrateur est mappé à des fonctions professionnelles courantes et donne aux membres de votre organisation des autorisations pour effectuer des tâches spécifiques dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a390-152">Each admin role maps to common business functions and gives people in your organization permissions to perform specific tasks in the Microsoft 365 admin center.</span></span>  
 
<span data-ttu-id="2a390-153">Pour plus d’informations, consultez la rubrique [assigner des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="2a390-153">For more information, see [Assign admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span></span>  
