---
title: Choisir le domaine à utiliser lors de la création de groupes Office 365
ms.reviewer: arvaradh
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
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
ms.assetid: 7cf5655d-e523-4bc3-a93b-3ccebf44a01a
description: 'Découvrez comment choisir le domaine à utiliser lors de la création de groupes Office 365 en configurant des stratégies d’adresse de messagerie à l’aide de PowerShell. '
ms.openlocfilehash: 55fc99cd201e66166e7da164777cfba2f763609c
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239236"
---
# <a name="choose-the-domain-to-use-when-creating-office-365-groups"></a><span data-ttu-id="a26e2-103">Choisir le domaine à utiliser lors de la création de groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="a26e2-103">Choose the domain to use when creating Office 365 Groups</span></span>

 <span data-ttu-id="a26e2-p101">Certaines organisations utilisent des domaines de messagerie distincts pour segmenter différentes parties de leurs activités. Vous pouvez spécifier le domaine à utiliser par vos utilisateurs pour créer des groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="a26e2-p101">Some organizations use separate email domains to segment different parts of their businesses. You can specify which domain should be used when your users create Office 365 groups.</span></span>
  
<span data-ttu-id="a26e2-106">Si votre organisation a besoin que les utilisateurs créent leurs groupes dans des domaines autres que le domaine accepté par défaut de votre entreprise, vous pouvez autoriser cela en configurant des stratégies d’adresse de messagerie (EAPs) à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a26e2-106">If your organization needs users to create their groups in domains other than the default accepted domain of your business, you can allow this by configuring email address policies (EAPs) using PowerShell.</span></span>
  
<span data-ttu-id="a26e2-107">Avant de pouvoir exécuter les applets de commande PowerShell, téléchargez et installez un module qui vous permettra de communiquer avec votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="a26e2-107">Before you can run the PowerShell cmdlets, download and install a module that will let you talk to your Office 365 organization.</span></span> <span data-ttu-id="a26e2-108">Consultez [connexion à Exchange Online à l’aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=785881).</span><span class="sxs-lookup"><span data-stu-id="a26e2-108">Check out [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=785881).</span></span>
  
## <a name="example-scenarios"></a><span data-ttu-id="a26e2-109">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="a26e2-109">Example scenarios</span></span>

<span data-ttu-id="a26e2-110">Supposons que le domaine principal de votre entreprise est Contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-110">Let's say your business's main domain is Contoso.com.</span></span> <span data-ttu-id="a26e2-111">Mais le domaine accepté par défaut de votre organisation est service.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-111">But your organization's default accepted domain is service.contoso.com.</span></span> <span data-ttu-id="a26e2-112">Cela signifie que les groupes seront créés dans service.contoso.com (par exemple, jimsteam@service.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a26e2-112">This means groups will be created in service.contoso.com (for example, jimsteam@service.contoso.com).</span></span>
  
<span data-ttu-id="a26e2-113">Imaginons que vous avez également des sous-domaines configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a26e2-113">Let's say you also have sub-domains configured in your organization.</span></span> <span data-ttu-id="a26e2-114">Vous souhaitez créer des groupes dans ces domaines également :</span><span class="sxs-lookup"><span data-stu-id="a26e2-114">You want groups to be created in these domains, too:</span></span>
  
- <span data-ttu-id="a26e2-115">students.contoso.com pour les étudiants</span><span class="sxs-lookup"><span data-stu-id="a26e2-115">students.contoso.com for students</span></span>
    
- <span data-ttu-id="a26e2-116">faculty.contoso.com pour les membres du corps enseignant</span><span class="sxs-lookup"><span data-stu-id="a26e2-116">faculty.contoso.com for faculty members</span></span>
    
<span data-ttu-id="a26e2-117">Les deux scénarios suivants expliquent comment effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a26e2-117">The following two scenarios explain how you would accomplish this.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a26e2-118">Lorsque vous avez plusieurs EAPs, elles sont évaluées dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="a26e2-118">When you have mulitple EAPs, they are evaluated in the order of priority.</span></span> <span data-ttu-id="a26e2-119">La valeur 1 correspond à la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="a26e2-119">A value of 1 means the highest priority.</span></span> <span data-ttu-id="a26e2-120">Une fois qu’un EAP répond, aucune autre EAP n’est évaluée et les adresses qui sont marquées sur le groupe sont telles que le protocole EAP correspondant.</span><span class="sxs-lookup"><span data-stu-id="a26e2-120">Once an EAP matches, no further EAP is evaluated and addresses that gets stamped on the group are as per the matched EAP.</span></span> <span data-ttu-id="a26e2-121">> si aucune EAPs ne correspond aux critères spécifiés, le groupe est mis en service dans le domaine accepté par défaut de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="a26e2-121">> If no EAPs match the specified criteria, then the group gets provisioned in the organization's default accepted domain.</span></span> <span data-ttu-id="a26e2-122">Consultez la [gestion des domaines acceptés dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=785428) pour plus d’informations sur l’ajout d’un domaine accepté.</span><span class="sxs-lookup"><span data-stu-id="a26e2-122">Check out [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=785428) for details on how to add an accepted domain.</span></span> 
  
### <a name="scenario-1"></a><span data-ttu-id="a26e2-123">Scénario 1</span><span class="sxs-lookup"><span data-stu-id="a26e2-123">Scenario 1</span></span>

<span data-ttu-id="a26e2-124">L’exemple suivant montre comment mettre en service tous les groupes Office 365 de votre organisation dans le domaine groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-124">The following example shows you how to provision all Office 365 groups in your organization in the groups.contoso.com domain.</span></span>
  
```
New-EmailAddressPolicy -Name Groups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@groups.contoso.com" -Priority 1
```

### <a name="scenario-2"></a><span data-ttu-id="a26e2-125">Scénario 2</span><span class="sxs-lookup"><span data-stu-id="a26e2-125">Scenario 2</span></span>

<span data-ttu-id="a26e2-126">Supposons que vous souhaitez contrôler les sous-domaines dans lesquels les groupes Office 365 sont créés.</span><span class="sxs-lookup"><span data-stu-id="a26e2-126">Let's say you want to control what sub-domains Office 365 groups are created in.</span></span> <span data-ttu-id="a26e2-127">Vous souhaitez :</span><span class="sxs-lookup"><span data-stu-id="a26e2-127">You want:</span></span>
  
- <span data-ttu-id="a26e2-128">Groupes créés par les étudiants (utilisateurs dont le **service** est défini sur les **étudiants**) dans le domaine students.groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-128">Groups created by students (users which have **Department** set to **Students**) in the students.groups.contoso.com domain.</span></span> <span data-ttu-id="a26e2-129">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a26e2-129">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name StudentsGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Students'} -Priority 1
  ```

- <span data-ttu-id="a26e2-130">Groupes créés par les membres de l’Université (les utilisateurs dont le **service** est défini sur **Université ou adresse e-mail contiennent Faculty.contoso.com)**) dans le domaine Faculty.groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-130">Groups created by faculty members (users which have **Department** set to **Faculty or email address contains faculty.contoso.com)**) in the faculty.groups.contoso.com domain.</span></span> <span data-ttu-id="a26e2-131">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a26e2-131">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name FacultyGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@faculty.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Faculty' -or EmailAddresses -like "*faculty.contoso.com*"} -Priority 2
  ```

- <span data-ttu-id="a26e2-132">Tous les autres utilisateurs du domaine groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a26e2-132">All other users in the groups.contoso.com domain.</span></span> <span data-ttu-id="a26e2-133">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a26e2-133">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name OtherGroups -IncludeUnifiedGroupRecipients -EnabledPrimarySMTPAddressTemplate "SMTP:@groups.contoso.com" -Priority 3
  ```

## <a name="change-email-address-policies"></a><span data-ttu-id="a26e2-134">Modifier les stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="a26e2-134">Change email address policies</span></span>

<span data-ttu-id="a26e2-135">Pour modifier les modèles de priorité ou d’adresse de messagerie d’un protocole EAP existant, utilisez la cmdlet Set-EmailAddressPolicy.</span><span class="sxs-lookup"><span data-stu-id="a26e2-135">To change the priority or email address templates for an existing EAP, use the Set-EmailAddressPolicy cmdlet.</span></span>
  
```
Set-EmailAddressPolicy -Name StudentsGroups -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com", "smtp:@students.contoso.com" ManagedByFilter {Department -eq 'Students'} -Priority 2

```

<span data-ttu-id="a26e2-136">La modification d’un protocole EAP n’a pas d’impact sur les groupes qui ont déjà été configurés.</span><span class="sxs-lookup"><span data-stu-id="a26e2-136">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="delete-email-address-policies"></a><span data-ttu-id="a26e2-137">Supprimer des stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="a26e2-137">Delete email address policies</span></span>

<span data-ttu-id="a26e2-138">Pour supprimer un protocole EAP, utilisez la cmdlet Remove-EmailAddressPolicy.</span><span class="sxs-lookup"><span data-stu-id="a26e2-138">To delete an EAP, use the Remove-EmailAddressPolicy cmdlet.</span></span>
  
```
Remove-EmailAddressPolicy -Identity StudentsGroups
```

<span data-ttu-id="a26e2-139">La modification d’un protocole EAP n’a pas d’impact sur les groupes qui ont déjà été configurés.</span><span class="sxs-lookup"><span data-stu-id="a26e2-139">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="hybrid-requirements"></a><span data-ttu-id="a26e2-140">Exigences hybrides</span><span class="sxs-lookup"><span data-stu-id="a26e2-140">Hybrid requirements</span></span>

<span data-ttu-id="a26e2-141">Si votre organisation est configurée dans un scénario hybride, consultez [configurer les groupes office 365 avec l’environnement Exchange hybride local](https://go.microsoft.com/fwlink/p/?LinkId=785430) pour vous assurer que votre organisation remplit les conditions requises pour la création de groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="a26e2-141">If your organization is configured in a hybrid scenario, check out [Configure Office 365 Groups with on-premises Exchange hybrid](https://go.microsoft.com/fwlink/p/?LinkId=785430) to make sure your organization meets the requirements for creating Office 365 groups.</span></span> 
  
## <a name="additional-info-about-using-email-address-policies-groups"></a><span data-ttu-id="a26e2-142">Informations supplémentaires sur l’utilisation des groupes de stratégies d’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="a26e2-142">Additional info about using email address policies groups:</span></span>

<span data-ttu-id="a26e2-143">Voici quelques éléments à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="a26e2-143">There are a few more things to know:</span></span>
  
- <span data-ttu-id="a26e2-144">La manière dont les groupes rapides sont créés dépend du nombre de EAPs configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a26e2-144">How fast groups are created depends on the number of EAPs configured in your organization.</span></span>
    
- <span data-ttu-id="a26e2-145">Les administrateurs et les utilisateurs peuvent également modifier les domaines lorsqu’ils créent des groupes.</span><span class="sxs-lookup"><span data-stu-id="a26e2-145">Admins and users can also modify domains when they create groups.</span></span>
    
- <span data-ttu-id="a26e2-146">Le groupe d’utilisateurs est déterminé à l’aide des requêtes standard (propriétés de l’utilisateur) qui sont déjà disponibles.</span><span class="sxs-lookup"><span data-stu-id="a26e2-146">Group of users is determined using the standard queries (User properties) that are already available.</span></span> <span data-ttu-id="a26e2-147">Consultez [les propriétés filtrables pour le paramètre-RecipientFilter pour les](https://go.microsoft.com/fwlink/p/?LinkId=785918) pProperties filtrables pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a26e2-147">Check out [Filterable properties for the -RecipientFilter parameter](https://go.microsoft.com/fwlink/p/?LinkId=785918) for supported filterable pproperties.</span></span> 
    
- <span data-ttu-id="a26e2-148">Si vous ne configurez aucun EAPs pour les groupes, le domaine accepté par défaut est sélectionné pour la création de groupe.</span><span class="sxs-lookup"><span data-stu-id="a26e2-148">If you don't configure any EAPs for groups, then the default accepted domain is selected for group creation.</span></span>
    
- <span data-ttu-id="a26e2-149">Si vous supprimez un domaine accepté, vous devez d’abord mettre à jour le EAPs, sinon la mise en service de groupe sera affectée.</span><span class="sxs-lookup"><span data-stu-id="a26e2-149">If you remove an accepted domain, you should update the EAPs first, otherwise, group provisioning will be impacted.</span></span>
    
- <span data-ttu-id="a26e2-150">Une limite maximale de 100 stratégies d’adresse de messagerie peut être configurée pour une organisation.</span><span class="sxs-lookup"><span data-stu-id="a26e2-150">A maximum limit of 100 email address policies can be configured for an organization.</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="a26e2-151">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a26e2-151">Related articles</span></span>

[<span data-ttu-id="a26e2-152">Créer un groupe Office 365 dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="a26e2-152">Create an Office 365 group in the admin center</span></span>](create-groups.md)
