---
title: Choisir le domaine à utiliser lors de la création de groupes Microsoft 365
ms.reviewer: arvaradh
f1.keywords: NOCSH
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
description: 'Découvrez comment choisir le domaine à utiliser lors de la création de groupes Microsoft 365 en configurant des stratégies d’adresse de messagerie à l’aide de PowerShell. '
ms.openlocfilehash: 1bc8a160ffc368bc4c66a5ac17ffcb203dc678f5
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43630622"
---
# <a name="choose-the-domain-to-use-when-creating-microsoft-365-groups"></a><span data-ttu-id="a5c0f-103">Choisir le domaine à utiliser lors de la création de groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a5c0f-103">Choose the domain to use when creating Microsoft 365 groups</span></span>

 <span data-ttu-id="a5c0f-104">Certaines organisations utilisent des domaines de messagerie distincts pour segmenter différentes parties de leurs activités.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-104">Some organizations use separate email domains to segment different parts of their businesses.</span></span> <span data-ttu-id="a5c0f-105">Vous pouvez spécifier le domaine à utiliser lorsque vos utilisateurs créent des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-105">You can specify which domain should be used when your users create Microsoft 365 groups.</span></span>
  
<span data-ttu-id="a5c0f-106">Si votre organisation a besoin que les utilisateurs créent leurs groupes dans des domaines autres que le domaine accepté par défaut de votre entreprise, vous pouvez autoriser cela en configurant des stratégies d’adresse de messagerie (EAPs) à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-106">If your organization needs users to create their groups in domains other than the default accepted domain of your business, you can allow this by configuring email address policies (EAPs) using PowerShell.</span></span>
  
<span data-ttu-id="a5c0f-107">Avant de pouvoir exécuter les applets de commande PowerShell, téléchargez et installez un module qui vous permettra de communiquer avec votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-107">Before you can run the PowerShell cmdlets, download and install a module that will let you talk to your organization.</span></span> <span data-ttu-id="a5c0f-108">Consultez [connexion à Exchange Online à l’aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=785881).</span><span class="sxs-lookup"><span data-stu-id="a5c0f-108">Check out [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=785881).</span></span>
  
## <a name="example-scenarios"></a><span data-ttu-id="a5c0f-109">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="a5c0f-109">Example scenarios</span></span>

<span data-ttu-id="a5c0f-110">Supposons que le domaine principal de votre entreprise est Contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-110">Let's say your business's main domain is Contoso.com.</span></span> <span data-ttu-id="a5c0f-111">Mais le domaine accepté par défaut de votre organisation est service.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-111">But your organization's default accepted domain is service.contoso.com.</span></span> <span data-ttu-id="a5c0f-112">Cela signifie que les groupes seront créés dans service.contoso.com (par exemple, jimsteam@service.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a5c0f-112">This means groups will be created in service.contoso.com (for example, jimsteam@service.contoso.com).</span></span>
  
<span data-ttu-id="a5c0f-113">Imaginons que vous avez également des sous-domaines configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-113">Let's say you also have sub-domains configured in your organization.</span></span> <span data-ttu-id="a5c0f-114">Vous souhaitez créer des groupes dans ces domaines également :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-114">You want groups to be created in these domains, too:</span></span>
  
- <span data-ttu-id="a5c0f-115">students.contoso.com pour les étudiants</span><span class="sxs-lookup"><span data-stu-id="a5c0f-115">students.contoso.com for students</span></span>
    
- <span data-ttu-id="a5c0f-116">faculty.contoso.com pour les membres du corps enseignant</span><span class="sxs-lookup"><span data-stu-id="a5c0f-116">faculty.contoso.com for faculty members</span></span>
    
<span data-ttu-id="a5c0f-117">Les deux scénarios suivants expliquent comment effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-117">The following two scenarios explain how you would accomplish this.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a5c0f-118">Lorsque vous avez plusieurs EAPs, elles sont évaluées dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-118">When you have mulitple EAPs, they are evaluated in the order of priority.</span></span> <span data-ttu-id="a5c0f-119">La valeur 1 correspond à la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-119">A value of 1 means the highest priority.</span></span> <span data-ttu-id="a5c0f-120">Une fois qu’un EAP répond, aucune autre EAP n’est évaluée et les adresses qui sont marquées sur le groupe sont telles que le protocole EAP correspondant.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-120">Once an EAP matches, no further EAP is evaluated and addresses that gets stamped on the group are as per the matched EAP.</span></span> <span data-ttu-id="a5c0f-121">> si aucune EAPs ne correspond aux critères spécifiés, le groupe est mis en service dans le domaine accepté par défaut de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-121">> If no EAPs match the specified criteria, then the group gets provisioned in the organization's default accepted domain.</span></span> <span data-ttu-id="a5c0f-122">Consultez la [gestion des domaines acceptés dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=785428) pour plus d’informations sur l’ajout d’un domaine accepté.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-122">Check out [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=785428) for details on how to add an accepted domain.</span></span> 
  
### <a name="scenario-1"></a><span data-ttu-id="a5c0f-123">Scénario 1</span><span class="sxs-lookup"><span data-stu-id="a5c0f-123">Scenario 1</span></span>

<span data-ttu-id="a5c0f-124">L’exemple suivant montre comment mettre en service tous les groupes Microsoft 365 de votre organisation dans le domaine groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-124">The following example shows you how to provision all Microsoft 365 groups in your organization in the groups.contoso.com domain.</span></span>
  
```
New-EmailAddressPolicy -Name Groups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@groups.contoso.com" -Priority 1
```

### <a name="scenario-2"></a><span data-ttu-id="a5c0f-125">Scénario 2</span><span class="sxs-lookup"><span data-stu-id="a5c0f-125">Scenario 2</span></span>

<span data-ttu-id="a5c0f-126">Supposons que vous souhaitez contrôler les sous-domaines dans lesquels les groupes Microsoft 365 sont créés.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-126">Let's say you want to control what sub-domains Microsoft 365 groups are created in.</span></span> <span data-ttu-id="a5c0f-127">Vous souhaitez :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-127">You want:</span></span>
  
- <span data-ttu-id="a5c0f-128">Groupes créés par les étudiants (utilisateurs dont le **service** est défini sur les **étudiants**) dans le domaine students.groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-128">Groups created by students (users which have **Department** set to **Students**) in the students.groups.contoso.com domain.</span></span> <span data-ttu-id="a5c0f-129">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-129">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name StudentsGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Students'} -Priority 1
  ```

- <span data-ttu-id="a5c0f-130">Groupes créés par les membres de l’Université (les utilisateurs dont le **service** est défini sur **Université ou adresse e-mail contiennent Faculty.contoso.com)**) dans le domaine Faculty.groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-130">Groups created by faculty members (users which have **Department** set to **Faculty or email address contains faculty.contoso.com)**) in the faculty.groups.contoso.com domain.</span></span> <span data-ttu-id="a5c0f-131">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-131">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name FacultyGroups -IncludeUnifiedGroupRecipients -EnabledEmailAddressTemplates "SMTP:@faculty.groups.contoso.com","smtp:@groups.contoso.com" -ManagedByFilter {Department -eq 'Faculty' -or EmailAddresses -like "*faculty.contoso.com*"} -Priority 2
  ```

- <span data-ttu-id="a5c0f-132">Tous les autres utilisateurs du domaine groups.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-132">All other users in the groups.contoso.com domain.</span></span> <span data-ttu-id="a5c0f-133">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-133">Use this command:</span></span>
    
  ```
  New-EmailAddressPolicy -Name OtherGroups -IncludeUnifiedGroupRecipients -EnabledPrimarySMTPAddressTemplate "SMTP:@groups.contoso.com" -Priority 3
  ```

## <a name="change-email-address-policies"></a><span data-ttu-id="a5c0f-134">Modifier les stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="a5c0f-134">Change email address policies</span></span>

<span data-ttu-id="a5c0f-135">Pour modifier les modèles de priorité ou d’adresse de messagerie d’un protocole EAP existant, utilisez la cmdlet Set-EmailAddressPolicy.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-135">To change the priority or email address templates for an existing EAP, use the Set-EmailAddressPolicy cmdlet.</span></span>
  
```
Set-EmailAddressPolicy -Name StudentsGroups -EnabledEmailAddressTemplates "SMTP:@students.groups.contoso.com","smtp:@groups.contoso.com", "smtp:@students.contoso.com" ManagedByFilter {Department -eq 'Students'} -Priority 2

```

<span data-ttu-id="a5c0f-136">La modification d’un protocole EAP n’a pas d’impact sur les groupes qui ont déjà été configurés.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-136">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="delete-email-address-policies"></a><span data-ttu-id="a5c0f-137">Supprimer des stratégies d’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="a5c0f-137">Delete email address policies</span></span>

<span data-ttu-id="a5c0f-138">Pour supprimer un protocole EAP, utilisez la cmdlet Remove-EmailAddressPolicy.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-138">To delete an EAP, use the Remove-EmailAddressPolicy cmdlet.</span></span>
  
```
Remove-EmailAddressPolicy -Identity StudentsGroups
```

<span data-ttu-id="a5c0f-139">La modification d’un protocole EAP n’a pas d’impact sur les groupes qui ont déjà été configurés.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-139">Changing an EAP has no impact on the groups that have already been provisioned.</span></span>
  
## <a name="hybrid-requirements"></a><span data-ttu-id="a5c0f-140">Exigences hybrides</span><span class="sxs-lookup"><span data-stu-id="a5c0f-140">Hybrid requirements</span></span>

<span data-ttu-id="a5c0f-141">Si votre organisation est configurée dans un scénario hybride, consultez [configurer les groupes microsoft 365 avec l’environnement Exchange hybride local](https://go.microsoft.com/fwlink/p/?LinkId=785430) pour vous assurer que votre organisation remplit les conditions requises pour la création de groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-141">If your organization is configured in a hybrid scenario, check out [Configure Microsoft 365 groups with on-premises Exchange hybrid](https://go.microsoft.com/fwlink/p/?LinkId=785430) to make sure your organization meets the requirements for creating Microsoft 365 groups.</span></span> 
  
## <a name="additional-info-about-using-email-address-policies-groups"></a><span data-ttu-id="a5c0f-142">Informations supplémentaires sur l’utilisation des groupes de stratégies d’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-142">Additional info about using email address policies groups:</span></span>

<span data-ttu-id="a5c0f-143">Voici quelques éléments à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="a5c0f-143">There are a few more things to know:</span></span>
  
- <span data-ttu-id="a5c0f-144">La manière dont les groupes rapides sont créés dépend du nombre de EAPs configurés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-144">How fast groups are created depends on the number of EAPs configured in your organization.</span></span>
    
- <span data-ttu-id="a5c0f-145">Les administrateurs et les utilisateurs peuvent également modifier les domaines lorsqu’ils créent des groupes.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-145">Admins and users can also modify domains when they create groups.</span></span>
    
- <span data-ttu-id="a5c0f-146">Le groupe d’utilisateurs est déterminé à l’aide des requêtes standard (propriétés de l’utilisateur) qui sont déjà disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-146">Group of users is determined using the standard queries (User properties) that are already available.</span></span> <span data-ttu-id="a5c0f-147">Consultez [les propriétés filtrables pour le paramètre-RecipientFilter pour les](https://go.microsoft.com/fwlink/p/?LinkId=785918) propriétés filtrables prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-147">Check out [Filterable properties for the -RecipientFilter parameter](https://go.microsoft.com/fwlink/p/?LinkId=785918) for supported filterable properties.</span></span> 
    
- <span data-ttu-id="a5c0f-148">Si vous ne configurez aucun EAPs pour les groupes, le domaine accepté par défaut est sélectionné pour la création de groupe.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-148">If you don't configure any EAPs for groups, then the default accepted domain is selected for group creation.</span></span>
    
- <span data-ttu-id="a5c0f-149">Si vous supprimez un domaine accepté, vous devez d’abord mettre à jour le EAPs, sinon la mise en service de groupe sera affectée.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-149">If you remove an accepted domain, you should update the EAPs first, otherwise, group provisioning will be impacted.</span></span>
    
- <span data-ttu-id="a5c0f-150">Une limite maximale de 100 stratégies d’adresse de messagerie peut être configurée pour une organisation.</span><span class="sxs-lookup"><span data-stu-id="a5c0f-150">A maximum limit of 100 email address policies can be configured for an organization.</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="a5c0f-151">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a5c0f-151">Related articles</span></span>

[<span data-ttu-id="a5c0f-152">Créer un groupe Microsoft 365 dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="a5c0f-152">Create an Microsoft 365 group in the admin center</span></span>](create-groups.md)
