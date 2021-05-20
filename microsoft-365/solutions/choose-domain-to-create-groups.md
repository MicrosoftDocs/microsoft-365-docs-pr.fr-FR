---
title: Choisir le domaine à utiliser lors de la création de Microsoft 365 groupes
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- m365solution-collabgovernance
search.appverid:
- MET150
ms.assetid: 7cf5655d-e523-4bc3-a93b-3ccebf44a01a
recommendations: false
description: Apprenez à choisir le domaine à utiliser lors de la création de groupes Microsoft 365 en configurant des stratégies d’adresse de messagerie à l’aide de PowerShell.
ms.openlocfilehash: 4d620c3344f83f56afd05c00d78615331dd413ed
ms.sourcegitcommit: 9541d5e6720a06327dc785e3ad7e8fb11246fd72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "52583147"
---
# <a name="choose-the-domain-to-use-when-creating-microsoft-365-groups"></a><span data-ttu-id="8cc7d-103">Choisir le domaine à utiliser lors de la création de Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="8cc7d-103">Choose the domain to use when creating Microsoft 365 groups</span></span>

<span data-ttu-id="8cc7d-104">Certaines organisations utilisent des domaines de messagerie distincts pour segmenter différentes parties de leurs activités.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-104">Some organizations use separate email domains to segment different parts of their businesses.</span></span> <span data-ttu-id="8cc7d-105">Vous pouvez spécifier le domaine à utiliser lorsque vos utilisateurs créent Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-105">You can specify which domain should be used when your users create Microsoft 365 groups.</span></span>
  
<span data-ttu-id="8cc7d-106">Si votre organisation a besoin que les utilisateurs créent leurs groupes dans des domaines autres que le domaine accepté par défaut de votre entreprise, vous pouvez l’autoriser en configurant des stratégies d’adresse de messagerie (EAP) à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-106">If your organization needs users to create their groups in domains other than the default accepted domain of your business, you can allow this by configuring email address policies (EAPs) using PowerShell.</span></span>

<span data-ttu-id="8cc7d-107">Avant de pouvoir exécuter les cmdlets PowerShell, téléchargez et installez un module qui vous permettra de parler à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-107">Before you can run the PowerShell cmdlets, download and install a module that will let you talk to your organization.</span></span> <span data-ttu-id="8cc7d-108">Consultez les [Connecter à Exchange Online à l’aide de PowerShell à distance.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="8cc7d-108">Check out [Connect to Exchange Online using remote PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="8cc7d-109">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="8cc7d-109">Example scenarios</span></span>

<span data-ttu-id="8cc7d-110">Supposons que le domaine principal de votre entreprise soit Contoso.com.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-110">Let's say your business's main domain is Contoso.com.</span></span> <span data-ttu-id="8cc7d-111">Toutefois, le domaine accepté par défaut de votre organisation est service.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-111">But your organization's default accepted domain is service.contoso.com.</span></span> <span data-ttu-id="8cc7d-112">Cela signifie que les groupes seront créés dans service.contoso.com (par exemple, jimsteam@service.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8cc7d-112">This means groups will be created in service.contoso.com (for example, jimsteam@service.contoso.com).</span></span>
  
<span data-ttu-id="8cc7d-113">Supposons que des sous-domaines sont également configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-113">Let's say you also have sub-domains configured in your organization.</span></span> <span data-ttu-id="8cc7d-114">Vous souhaitez également créer des groupes dans ces domaines :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-114">You want groups to be created in these domains, too:</span></span>
  
- <span data-ttu-id="8cc7d-115">students.contoso.com pour les étudiants</span><span class="sxs-lookup"><span data-stu-id="8cc7d-115">students.contoso.com for students</span></span>
    
- <span data-ttu-id="8cc7d-116">faculty.contoso.com pour les membres du corps enseignant</span><span class="sxs-lookup"><span data-stu-id="8cc7d-116">faculty.contoso.com for faculty members</span></span>
    
<span data-ttu-id="8cc7d-117">Les deux scénarios suivants expliquent comment effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-117">The following two scenarios explain how you would accomplish this.</span></span>

> [!NOTE]
> <span data-ttu-id="8cc7d-118">Lorsque vous avez des projets DPE, ils sont évalués dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-118">When you have mulitple EAPs, they are evaluated in the order of priority.</span></span> <span data-ttu-id="8cc7d-119">Une valeur de 1 signifie la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-119">A value of 1 means the highest priority.</span></span> <span data-ttu-id="8cc7d-120">Une fois qu’un EAP correspond, aucun autre EAP n’est évalué et les adresses qui sont marqués sur le groupe sont conformes à l’EAP.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-120">Once an EAP matches, no further EAP is evaluated and addresses that gets stamped on the group are as per the matched EAP.</span></span> <span data-ttu-id="8cc7d-121">> si aucun eaps ne correspond aux critères spécifiés, le groupe est provisioné dans le domaine accepté par défaut de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-121">> If no EAPs match the specified criteria, then the group gets provisioned in the organization's default accepted domain.</span></span> <span data-ttu-id="8cc7d-122">Consultez [Gérer les domaines acceptés](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) dans Exchange Online pour plus d’informations sur l’ajout d’un domaine accepté.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-122">Check out [Manage accepted domains in Exchange Online](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) for details on how to add an accepted domain.</span></span>
  
### <a name="scenario-1"></a><span data-ttu-id="8cc7d-123">Scénario 1</span><span class="sxs-lookup"><span data-stu-id="8cc7d-123">Scenario 1</span></span>

<span data-ttu-id="8cc7d-124">L’exemple suivant vous montre comment mettre en service Microsoft 365 groupes de votre organisation dans groups.contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-124">The following example shows you how to provision all Microsoft 365 groups in your organization in the groups.contoso.com domain.</span></span>
  
```
New-EmailAddressPolicy -Name Groups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@groups.contoso.com" -Priority 1
```

### <a name="scenario-2"></a><span data-ttu-id="8cc7d-125">Scénario 2</span><span class="sxs-lookup"><span data-stu-id="8cc7d-125">Scenario 2</span></span>

<span data-ttu-id="8cc7d-126">Supposons que vous vouliez contrôler dans quels sous-domaines Microsoft 365 groupes sont créés.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-126">Let's say you want to control what sub-domains Microsoft 365 groups are created in.</span></span> <span data-ttu-id="8cc7d-127">Vous souhaitez :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-127">You want:</span></span>
  
- <span data-ttu-id="8cc7d-128">Groupes créés par des étudiants (utilisateurs dont le service **est** réservé aux **étudiants)** dans students.groups.contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-128">Groups created by students (users which have **Department** set to **Students**) in the students.groups.contoso.com domain.</span></span> <span data-ttu-id="8cc7d-129">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-129">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name StudentsGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Students'} -Priority 1
  ```

- <span data-ttu-id="8cc7d-130">Groupes créés par des membres  du corps enseignant (les utilisateurs dont le service est définie sur Enseignant ou l’adresse **e-mail** contient faculty.contoso.com) ) dans le faculty.groups.contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-130">Groups created by faculty members (users which have **Department** set to **Faculty or email address contains faculty.contoso.com)**) in the faculty.groups.contoso.com domain.</span></span> <span data-ttu-id="8cc7d-131">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-131">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name FacultyGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@faculty.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Faculty' -or EmailAddresses -like "*faculty.contoso.com*"} -Priority 2
  ```

- <span data-ttu-id="8cc7d-132">Les groupes créés par d’autres personnes sont créés dans groups.contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-132">Groups created by anyone else are created in the groups.contoso.com domain.</span></span> <span data-ttu-id="8cc7d-133">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-133">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name OtherGroups -IncludeUnifiedGroupRecipients -EnabledPrimarySMTPAddressTemplate "SMTP:@groups.contoso.com" -Priority 3
  ```

## <a name="change-email-address-policies"></a><span data-ttu-id="8cc7d-134">Modifier les stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="8cc7d-134">Change email address policies</span></span>

<span data-ttu-id="8cc7d-135">Pour modifier les modèles de priorité ou d’adresse de messagerie d’un EAP existant, utilisez la cmdlet Set-EmailAddressPolicy de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-135">To change the priority or email address templates for an existing EAP, use the Set-EmailAddressPolicy cmdlet.</span></span>
  
```
Set-EmailAddressPolicy -Name StudentsGroups -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com", "smtp:@students.contoso.com" ManagedByFilter {Department -eq 'Students'} -Priority 2

```

<span data-ttu-id="8cc7d-136">La modification d’un EAP n’a aucun impact sur les groupes qui ont déjà été mis en service.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-136">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="delete-email-address-policies"></a><span data-ttu-id="8cc7d-137">Supprimer des stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="8cc7d-137">Delete email address policies</span></span>

<span data-ttu-id="8cc7d-138">Pour supprimer un EAP, utilisez l'Remove-EmailAddressPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-138">To delete an EAP, use the Remove-EmailAddressPolicy cmdlet.</span></span>
  
```
Remove-EmailAddressPolicy -Identity StudentsGroups
```

<span data-ttu-id="8cc7d-139">La modification d’un EAP n’a aucun impact sur les groupes qui ont déjà été mis en service.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-139">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="hybrid-requirements"></a><span data-ttu-id="8cc7d-140">Exigences hybrides</span><span class="sxs-lookup"><span data-stu-id="8cc7d-140">Hybrid requirements</span></span>

<span data-ttu-id="8cc7d-141">Si votre organisation est configurée dans un scénario hybride, consultez Configurer des groupes [Microsoft 365](/exchange/hybrid-deployment/set-up-microsoft-365-groups) avec Exchange hybride local pour vous assurer que votre organisation répond aux exigences de création de groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-141">If your organization is configured in a hybrid scenario, check out [Configure Microsoft 365 groups with on-premises Exchange hybrid](/exchange/hybrid-deployment/set-up-microsoft-365-groups) to make sure your organization meets the requirements for creating Microsoft 365 groups.</span></span> 
  
## <a name="additional-info-about-using-email-address-policies-groups"></a><span data-ttu-id="8cc7d-142">Informations supplémentaires sur l’utilisation de groupes de stratégies d’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-142">Additional info about using email address policies groups:</span></span>

<span data-ttu-id="8cc7d-143">Il y a d’autres choses à savoir :</span><span class="sxs-lookup"><span data-stu-id="8cc7d-143">There are a few more things to know:</span></span>
  
- <span data-ttu-id="8cc7d-144">La rapidité de création des groupes dépend du nombre de P EAP configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-144">How fast groups are created depends on the number of EAPs configured in your organization.</span></span>
    
- <span data-ttu-id="8cc7d-145">Les administrateurs et les utilisateurs peuvent également modifier des domaines lorsqu’ils créent des groupes.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-145">Admins and users can also modify domains when they create groups.</span></span>
    
- <span data-ttu-id="8cc7d-146">Le groupe d’utilisateurs est déterminé à l’aide des requêtes standard (propriétés utilisateur) qui sont déjà disponibles.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-146">Group of users is determined using the standard queries (User properties) that are already available.</span></span> <span data-ttu-id="8cc7d-147">Consultez [propriétés filtrables pour le paramètre -RecipientFilter](/powershell/exchange/recipientfilter-properties) pour les propriétés filtrables pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-147">Check out [Filterable properties for the -RecipientFilter parameter](/powershell/exchange/recipientfilter-properties) for supported filterable properties.</span></span> 
    
- <span data-ttu-id="8cc7d-148">Si vous ne configurez pas de PNE pour les groupes, le domaine accepté par défaut est sélectionné pour la création de groupes.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-148">If you don't configure any EAPs for groups, then the default accepted domain is selected for group creation.</span></span>
    
- <span data-ttu-id="8cc7d-149">Si vous supprimez un domaine accepté, vous devez d’abord mettre à jour les PED, sinon la mise en service de groupe sera impactée.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-149">If you remove an accepted domain, you should update the EAPs first, otherwise, group provisioning will be impacted.</span></span>
    
- <span data-ttu-id="8cc7d-150">Une limite maximale de 100 stratégies d’adresse de messagerie peut être configurée pour une organisation.</span><span class="sxs-lookup"><span data-stu-id="8cc7d-150">A maximum limit of 100 email address policies can be configured for an organization.</span></span>
    
## <a name="related-content"></a><span data-ttu-id="8cc7d-151">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="8cc7d-151">Related content</span></span>

<span data-ttu-id="8cc7d-152">[Planification pas à pas de la gouvernance de](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step) la collaboration (article)</span><span class="sxs-lookup"><span data-stu-id="8cc7d-152">[Collaboration governance planning step-by-step](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step) (article)</span></span>

<span data-ttu-id="8cc7d-153">[Créer votre plan de gouvernance de collaboration](collaboration-governance-first.md) (article)</span><span class="sxs-lookup"><span data-stu-id="8cc7d-153">[Create your collaboration governance plan](collaboration-governance-first.md) (article)</span></span>

<span data-ttu-id="8cc7d-154">[Créer un groupe Microsoft 365 dans le Centre d’administration](../admin/create-groups/create-groups.md) (article)</span><span class="sxs-lookup"><span data-stu-id="8cc7d-154">[Create an Microsoft 365 group in the admin center](../admin/create-groups/create-groups.md) (article)</span></span>