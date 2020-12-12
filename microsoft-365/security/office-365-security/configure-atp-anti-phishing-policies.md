---
title: Configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage avancées disponibles dans les organisations avec Microsoft Defender pour Office 365.
ms.openlocfilehash: 295600098aee151ec088e48345bf69181ba3afb8
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49658893"
---
# <a name="configure-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-103">Configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-103">Configure anti-phishing policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="babd1-104">Les stratégies anti-hameçonnage de [Microsoft Defender pour Office 365](office-365-atp.md) peuvent vous aider à protéger votre organisation contre les attaques d’hameçonnage malveillant basées sur l’emprunt d’identité et d’autres types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-104">Anti-phishing policies in [Microsoft Defender for Office 365](office-365-atp.md) can help protect your organization from malicious impersonation-based phishing attacks and other types of phishing attacks.</span></span> <span data-ttu-id="babd1-105">Pour plus d’informations sur les différences entre les stratégies de détection d’hameçonnage dans Exchange Online Protection (EOP) et les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, consultez la rubrique [anti-phishing protection](anti-phishing-protection.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-105">For more information about the differences between anti-phishing policies in Exchange Online Protection (EOP) and anti-phishing policies in Microsoft Defender for Office 365, see [Anti-phishing protection](anti-phishing-protection.md).</span></span>

<span data-ttu-id="babd1-106">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-106">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="babd1-107">Pour une granularité accrue, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="babd1-107">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="babd1-108">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="babd1-108">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="babd1-109">Vous pouvez configurer des stratégies anti-hameçonnage dans le centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="babd1-109">You can configure anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span>

<span data-ttu-id="babd1-110">Pour plus d’informations sur la configuration des stratégies de blocage plus limitées disponibles dans les organisations Exchange Online Protection (autrement dit, les organisations sans Microsoft Defender pour Office 365), voir [configure anti-phishing Policies in EOP](configure-anti-phishing-policies-eop.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-110">For information about configuring the more limited in anti-phishing policies that are available in Exchange Online Protection organizations (that is, organizations without Microsoft Defender for Office 365), see [Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

<span data-ttu-id="babd1-111">Les éléments de base d’une stratégie anti-hameçonnage sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="babd1-111">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="babd1-112">**Stratégie anti-hameçonnage**: spécifie les protections de hameçonnage à activer ou à désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="babd1-112">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="babd1-113">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-113">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="babd1-114">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de détection d’hameçonnage dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="babd1-114">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="babd1-115">Lorsque vous créez une stratégie, vous créez en réalité une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="babd1-115">When you create a policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="babd1-116">Lorsque vous modifiez une stratégie, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-116">When you modify a policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="babd1-117">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="babd1-117">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="babd1-118">Lorsque vous supprimez une stratégie, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="babd1-118">When you remove a policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="babd1-119">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="babd1-119">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="babd1-120">Pour plus d’informations, voir la section [utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365](#use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="babd1-120">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies in Microsoft Defender for Office 365](#use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365) section later in this article.</span></span>

<span data-ttu-id="babd1-121">Chaque organisation Microsoft Defender pour Office 365 dispose d’une stratégie anti-hameçonnage intégrée nommée Office antiphishing par défaut, qui comporte les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-121">Every Microsoft Defender for Office 365 organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="babd1-122">La stratégie est appliquée à tous les destinataires de l’organisation, même s’il n’y a aucune règle anti-hameçonnage (filtres de destinataire) associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-122">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="babd1-123">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="babd1-123">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="babd1-124">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="babd1-124">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="babd1-125">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-125">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="babd1-126">Pour accroître l’efficacité de la protection anti-hameçonnage dans Microsoft Defender pour Office 365, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="babd1-126">To increase the effectiveness of anti-phishing protection in Microsoft Defender for Office 365, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="babd1-127">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="babd1-127">What do you need to know before you begin?</span></span>

- <span data-ttu-id="babd1-128">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="babd1-128">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="babd1-129">Pour accéder directement à la page **anti-hameçonnage ATP** , utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="babd1-129">To go directly to the **ATP anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="babd1-130">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="babd1-130">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="babd1-131">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="babd1-131">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="babd1-132">Pour ajouter, modifier et supprimer des stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="babd1-132">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="babd1-133">Pour un accès en lecture seule aux stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur** de sécurité <sup>\*</sup> .</span><span class="sxs-lookup"><span data-stu-id="babd1-133">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups<sup>\*</sup>.</span></span>

  <span data-ttu-id="babd1-134">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="babd1-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="babd1-135">**Notes**:</span></span>

  - <span data-ttu-id="babd1-136">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="babd1-136">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="babd1-137">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="babd1-137">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="babd1-138">Le groupe de rôles gestion de l' **Organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) offre également un accès en lecture seule à la fonctionnalité <sup>\*</sup> .</span><span class="sxs-lookup"><span data-stu-id="babd1-138">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>
  - <span data-ttu-id="babd1-139"><sup>\*</sup> Dans le centre de sécurité & conformité, l’accès en lecture seule permet aux utilisateurs d’afficher les paramètres des stratégies anti-hameçonnage personnalisées.</span><span class="sxs-lookup"><span data-stu-id="babd1-139"><sup>\*</sup> In the Security & Compliance Center, read-only access allows users to view the settings of custom anti-phishing policies.</span></span> <span data-ttu-id="babd1-140">Les utilisateurs en lecture seule ne peuvent pas voir les paramètres dans la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-140">Read-only users can't see the settings in the default anti-phishing policy.</span></span>

- <span data-ttu-id="babd1-141">Pour connaître les paramètres recommandés pour les stratégies de détection d’hameçonnage dans Microsoft Defender pour Office 365, reportez-vous à la rubrique [anti-phishing Policy in Defender for office 365 Settings](recommended-settings-for-eop-and-office365-atp.md#anti-phishing-policy-settings-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="babd1-141">For our recommended settings for anti-phishing policies in Microsoft Defender for Office 365, see [Anti-phishing policy in Defender for Office 365 settings](recommended-settings-for-eop-and-office365-atp.md#anti-phishing-policy-settings-in-microsoft-defender-for-office-365).</span></span>

- <span data-ttu-id="babd1-142">Autoriser jusqu’à 30 minutes pour l’application d’une stratégie nouvelle ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="babd1-142">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="babd1-143">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, consultez la rubrique [Order and Precedence of e-mail protection](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-143">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-144">Utiliser le centre de sécurité & conformité pour créer des stratégies de détection d’hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-144">Use the Security & Compliance Center to create anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="babd1-145">La création d’une stratégie anti-hameçonnage personnalisée dans le centre de sécurité & conformité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="babd1-145">Creating a custom anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="babd1-146">Lorsque vous créez une stratégie anti-hameçonnage, vous pouvez uniquement spécifier le nom de la stratégie, sa description et le filtre de destinataire qui identifie la personne à laquelle la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="babd1-146">When you create an anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="babd1-147">Après avoir créé la stratégie, vous pouvez modifier la stratégie pour modifier ou consulter les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-147">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="babd1-148">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-148">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-149">Sur la page **anti-hameçonnage** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="babd1-149">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="babd1-150">L’Assistant **créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="babd1-150">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="babd1-151">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="babd1-151">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="babd1-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="babd1-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="babd1-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="babd1-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="babd1-155">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-155">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="babd1-156">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="babd1-156">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="babd1-157">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="babd1-157">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="babd1-158">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="babd1-158">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="babd1-159">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="babd1-159">Click **Add a condition**.</span></span> <span data-ttu-id="babd1-160">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="babd1-160">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="babd1-161">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="babd1-161">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="babd1-162">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="babd1-162">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="babd1-163">**Le domaine du destinataire est**: spécifie des destinataires dans un ou plusieurs domaines acceptés configurés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="babd1-163">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in the organization.</span></span>

   <span data-ttu-id="babd1-164">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="babd1-164">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="babd1-165">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="babd1-165">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="babd1-166">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="babd1-166">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="babd1-167">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="babd1-167">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="babd1-168">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="babd1-168">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="babd1-169">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="babd1-169">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="babd1-170">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="babd1-170">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="babd1-171">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="babd1-171">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="babd1-172">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="babd1-172">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="babd1-173">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="babd1-173">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="babd1-174">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="babd1-174">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="babd1-175">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="babd1-175">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="babd1-176">Lorsque vous avez terminé, cliquez sur **créer cette stratégie**.</span><span class="sxs-lookup"><span data-stu-id="babd1-176">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="babd1-177">Cliquez sur **OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="babd1-177">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="babd1-178">Après avoir créé la stratégie anti-hameçonnage avec ces paramètres généraux, suivez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-178">After you create the anti-phishing policy with these general settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-179">Utiliser le centre de sécurité & conformité pour modifier les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-179">Use the Security & Compliance Center to modify anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="babd1-180">Utilisez les procédures suivantes pour modifier les stratégies de détection d’hameçonnage : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="babd1-180">Use the following procedures to modify anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="babd1-181">Si vous ne l’avez pas encore fait, ouvrez le centre de sécurité & conformité,  puis accédez à \>  \> **protection contre les menaces pour le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-181">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-182">Sélectionnez la stratégie anti-hameçonnage personnalisée que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="babd1-182">Select the custom anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="babd1-183">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="babd1-183">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="babd1-184">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="babd1-184">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="babd1-185">Si vous cliquez sur **modifier** dans une section, vous pouvez accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="babd1-185">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="babd1-186">Les étapes suivantes sont présentées dans l’ordre dans lequel les sections apparaissent, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="babd1-186">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="babd1-187">Une fois que vous avez cliqué sur **modifier** dans une section, les paramètres disponibles sont présentés dans un format d’Assistant, mais vous pouvez sauter les pages dans n’importe quel ordre, et vous pouvez cliquer sur **Enregistrer** sur n’importe quelle page (ou sur **Annuler** ou **Fermer** l' ![ icône ](../../media/scc-remove-icon.png) pour revenir à la page **modifier votre stratégie \<name\>** (vous n’avez pas besoin de consulter la dernière page de l’Assistant pour enregistrer ou quitter</span><span class="sxs-lookup"><span data-stu-id="babd1-187">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="babd1-188">**Paramètre de stratégie**: cliquez sur **modifier** pour modifier les mêmes paramètres que ceux qui étaient disponibles lorsque vous avez [créé la stratégie](#use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365) dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="babd1-188">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365) in the previous section:</span></span>

   - <span data-ttu-id="babd1-189">**Name**</span><span class="sxs-lookup"><span data-stu-id="babd1-189">**Name**</span></span>
   - <span data-ttu-id="babd1-190">**Description**</span><span class="sxs-lookup"><span data-stu-id="babd1-190">**Description**</span></span>
   - <span data-ttu-id="babd1-191">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="babd1-191">**Applied to**</span></span>
   - <span data-ttu-id="babd1-192">**Vérifier vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="babd1-192">**Review your settings**</span></span>

   <span data-ttu-id="babd1-193">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="babd1-193">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="babd1-194">**Emprunt d’identité**: cliquez sur **modifier** pour modifier les expéditeurs et les domaines protégés protégés dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-194">**Impersonation**: Click **Edit** to modify the protected senders and protected domains in the policy.</span></span> <span data-ttu-id="babd1-195">Ces paramètres sont une condition pour la stratégie qui identifie les expéditeurs usurpés à rechercher (individuellement ou par domaine) dans l’adresse de provenance des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="babd1-195">These settings are a condition for the policy that identifies spoofed senders to look for (individually or by domain) in the From address of inbound messages.</span></span> <span data-ttu-id="babd1-196">Pour plus d’informations, reportez-vous à la rubrique [emprunt d’identité des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="babd1-196">For more information, see [Impersonation settings in anti-phishing policies in Microsoft Defender for Office 365](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span>

   - <span data-ttu-id="babd1-197">**Ajouter des utilisateurs à protéger**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-197">**Add users to protect**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-198">Pour l’activer, faites glisser le bouton bascule sur **activé**, puis cliquez sur le bouton **Ajouter un utilisateur** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="babd1-198">To turn it on, slide the toggle to **On**, and then click the **Add user** button that appears.</span></span>

     <span data-ttu-id="babd1-199">Dans la fenêtre mobile **Ajouter un utilisateur** qui s’affiche, configurez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-199">In the **Add user** flyout that appears, configure the following values:</span></span>

     - <span data-ttu-id="babd1-200">**Adresse de messagerie**:</span><span class="sxs-lookup"><span data-stu-id="babd1-200">**Email address**:</span></span>

       - <span data-ttu-id="babd1-201">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="babd1-201">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="babd1-202">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="babd1-202">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="babd1-203">Pour supprimer une entrée, cliquez sur **supprimer** ![ l’icône Supprimer ](../../media/scc-remove-icon.png) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="babd1-203">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="babd1-204">**Name**: cette valeur est renseignée en fonction de l’adresse de messagerie que vous avez sélectionnée, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="babd1-204">**Name**: This value is populated based on the email address you selected, but you can change it.</span></span>

     <span data-ttu-id="babd1-205">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="babd1-205">When you're finished, click **Save** on any page.</span></span>

     <span data-ttu-id="babd1-206">Pour modifier une entrée existante, sélectionnez-la dans la liste.</span><span class="sxs-lookup"><span data-stu-id="babd1-206">To edit an existing entry, select the protected user in the list.</span></span>

     > [!NOTE]
     >
     > - <span data-ttu-id="babd1-207">Dans chaque stratégie anti-hameçonnage, vous pouvez spécifier un maximum de 60 utilisateurs protégés (adresses e-mail de l’expéditeur).</span><span class="sxs-lookup"><span data-stu-id="babd1-207">In each anti-phishing policy, you can specify a maximum of 60 protected users (sender email addresses).</span></span> <span data-ttu-id="babd1-208">Vous ne pouvez pas spécifier le même utilisateur protégé dans plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="babd1-208">You can't specify the same protected user in multiple policies.</span></span>
     >
     > - <span data-ttu-id="babd1-209">La protection contre l’usurpation d’identité d’utilisateur ne fonctionne pas si l’expéditeur et le destinataire ont déjà communiqué par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="babd1-209">User impersonation protection does not work if the sender and recipient have previously communicated via email.</span></span> <span data-ttu-id="babd1-210">Si l’expéditeur et le destinataire n’ont jamais communiqué par courrier électronique, le message est identifié en tant que tentative d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="babd1-210">If the sender and recipient have never communicated via email, the message will be identified as an impersonation attempt.</span></span>

   - <span data-ttu-id="babd1-211">**Ajouter des domaines à protéger**: configurez l’un des paramètres suivants ou les deux :</span><span class="sxs-lookup"><span data-stu-id="babd1-211">**Add domains to protect**: Configure one or both of the following settings:</span></span>

     - <span data-ttu-id="babd1-212">**Inclure automatiquement les domaines dont je suis propriétaire**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-212">**Automatically include the domains I own**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-213">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-213">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="babd1-214">**Inclure les domaines personnalisés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-214">**Include custom domains**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-215">Pour l’activer, faites glisser le bouton bascule sur **activé**, puis dans la zone **Ajouter des domaines** , entrez le nom de domaine (par exemple, contoso.com), appuyez sur entrée et répétez l’opération si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="babd1-215">To turn it on, slide the toggle to **On**, and in the **Add domains** box, enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

     > [!NOTE]
     > <span data-ttu-id="babd1-216">Vous pouvez avoir un maximum de 50 domaines dans toutes les stratégies de détection d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-216">You can have a maximum of 50 domains in all anti-phishing policies.</span></span>

   - <span data-ttu-id="babd1-217">**Actions**: cliquez sur **modifier**</span><span class="sxs-lookup"><span data-stu-id="babd1-217">**Actions**: Click **Edit**</span></span>

     - <span data-ttu-id="babd1-218">**Si un message électronique est envoyé par un utilisateur représenté**: configurez l’une des actions suivantes pour les messages dans lesquels l’expéditeur usurpé est l’un des utilisateurs protégés que vous avez spécifié dans **Ajouter des utilisateurs à protéger**:</span><span class="sxs-lookup"><span data-stu-id="babd1-218">**If email is sent by an impersonated user**: Configure one of the following actions for messages where the spoofed sender is one of the protected users you specified in **Add users to protect**:</span></span>

       - <span data-ttu-id="babd1-219">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="babd1-219">**Don't apply any action**</span></span>
       - <span data-ttu-id="babd1-220">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="babd1-220">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="babd1-221">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="babd1-221">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="babd1-222">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="babd1-222">**Quarantine the message**</span></span>
       - <span data-ttu-id="babd1-223">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="babd1-223">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="babd1-224">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="babd1-224">**Delete the message before it's delivered**</span></span>

     - <span data-ttu-id="babd1-225">**Si le courrier électronique est envoyé par un domaine emprunté**: configurez l’une des actions suivantes pour les messages dans lesquels l’expéditeur usurpé se trouve dans l’un des domaines protégés que vous avez spécifiés dans **Ajouter des domaines à protéger**:</span><span class="sxs-lookup"><span data-stu-id="babd1-225">**If email is sent by an impersonated domain**: Configure one of the following actions for messages where the spoofed sender is in one of the protected domains you specified in **Add domains to protect**:</span></span>

       - <span data-ttu-id="babd1-226">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="babd1-226">**Don't apply any action**</span></span>
       - <span data-ttu-id="babd1-227">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="babd1-227">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="babd1-228">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="babd1-228">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="babd1-229">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="babd1-229">**Quarantine the message**</span></span>
       - <span data-ttu-id="babd1-230">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="babd1-230">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="babd1-231">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="babd1-231">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="babd1-232">Cliquez sur **conseils de sécurité pour l’emprunt d’identité** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="babd1-232">Click **turn on impersonation safety tips** and configure any of the following settings:</span></span>

     - <span data-ttu-id="babd1-233">**Afficher l’astuce pour les utilisateurs empruntés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-233">**Show tip for impersonated users**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-234">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-234">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="babd1-235">**Afficher le Conseil pour les domaines empruntés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-235">**Show tip for impersonated domains**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-236">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-236">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="babd1-237">**Afficher le Conseil pour les caractères inhabituels**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="babd1-237">**Show tip for unusual characters**: The default value is **Off**.</span></span> <span data-ttu-id="babd1-238">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-238">To turn it on, slide the toggle to **On**.</span></span>

     <span data-ttu-id="babd1-239">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="babd1-239">When you're finished, click **Save**.</span></span>

   - <span data-ttu-id="babd1-240">**Intelligence des boîtes aux lettres**:</span><span class="sxs-lookup"><span data-stu-id="babd1-240">**Mailbox intelligence**:</span></span>

     - <span data-ttu-id="babd1-241">**Activer l’intelligence des boîtes aux lettres ?**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-241">**Enable mailbox intelligence?**: The default value is **On**.</span></span> <span data-ttu-id="babd1-242">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-242">To turn it off, slide the toggle to **Off**.</span></span>

     - <span data-ttu-id="babd1-243">**Activer la protection contre l’usurpation d’identité basée sur les boîtes aux lettres ?**: ce paramètre est disponible uniquement si **activer l’intelligence des boîtes aux lettres** est **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-243">**Enable mailbox intelligence based impersonation protection?**: This setting is only available if **Enable mailbox intelligence?** is **On**.</span></span>

       <span data-ttu-id="babd1-244">Dans **si un message électronique est envoyé par un utilisateur emprunté**, vous pouvez spécifier l’une des actions suivantes à effectuer sur les messages qui échouent à la boîte aux lettres (les mêmes actions que celles disponibles pour les utilisateurs protégés et les domaines protégés) :</span><span class="sxs-lookup"><span data-stu-id="babd1-244">In **If email is sent by an impersonated user**, you can specify one of the following actions to take on messages that fail mailbox intelligence (the same actions that are available for protected users and protected domains):</span></span>

       - <span data-ttu-id="babd1-245">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="babd1-245">**Don't apply any action**</span></span>
       - <span data-ttu-id="babd1-246">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="babd1-246">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="babd1-247">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="babd1-247">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="babd1-248">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="babd1-248">**Quarantine the message**</span></span>
       - <span data-ttu-id="babd1-249">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="babd1-249">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="babd1-250">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="babd1-250">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="babd1-251">**Ajouter des expéditeurs et des domaines approuvés**: spécifiez les exceptions pour la stratégie :</span><span class="sxs-lookup"><span data-stu-id="babd1-251">**Add trusted senders and domains**: Specify exceptions for the policy:</span></span>

     - <span data-ttu-id="babd1-252">**Expéditeurs approuvés**:</span><span class="sxs-lookup"><span data-stu-id="babd1-252">**Trusted senders**:</span></span>

       - <span data-ttu-id="babd1-253">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="babd1-253">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="babd1-254">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="babd1-254">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="babd1-255">Pour supprimer une entrée, cliquez sur **supprimer** ![ l’icône Supprimer ](../../media/scc-remove-icon.png) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="babd1-255">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="babd1-256">**Domaines approuvés**: saisissez le nom de domaine (par exemple, contoso.com), appuyez sur entrée et répétez l’opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="babd1-256">**Trusted domains**: Enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="babd1-257">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="babd1-257">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="babd1-258">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="babd1-258">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="babd1-259">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="babd1-259">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="babd1-260">**Utilisateurs protégés**</span><span class="sxs-lookup"><span data-stu-id="babd1-260">**Protected users**</span></span>
       - <span data-ttu-id="babd1-261">**Domaines protégés** \> **Inclure les domaines dont je suis propriétaire**</span><span class="sxs-lookup"><span data-stu-id="babd1-261">**Protected domains** \> **Include domains I own**</span></span>
       - <span data-ttu-id="babd1-262">**Domaines protégés** \> **Domaines protégés** (domaines personnalisés)</span><span class="sxs-lookup"><span data-stu-id="babd1-262">**Protected domains** \> **Protected domains** (custom domains)</span></span>
       - <span data-ttu-id="babd1-263">**Veille des boîtes aux lettres**</span><span class="sxs-lookup"><span data-stu-id="babd1-263">**Mailbox intelligence**</span></span>

   <span data-ttu-id="babd1-264">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="babd1-264">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="babd1-265">**Spoof**: cliquez sur **modifier** pour activer ou désactiver l’Assistant usurpation d’identité, activez ou désactivez l’identification de l’expéditeur non authentifié dans Outlook, puis configurez l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués.</span><span class="sxs-lookup"><span data-stu-id="babd1-265">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="babd1-266">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="babd1-266">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="babd1-267">Notez que ces mêmes paramètres sont également disponibles dans les stratégies de détection d’hameçonnage dans EOP.</span><span class="sxs-lookup"><span data-stu-id="babd1-267">Note that these same settings are also available in anti-phishing policies in EOP.</span></span>

   - <span data-ttu-id="babd1-268">**Usurpation des paramètres de filtrage**: la valeur par défaut est **activée**, et nous vous recommandons de la laisser activée.</span><span class="sxs-lookup"><span data-stu-id="babd1-268">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="babd1-269">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-269">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="babd1-270">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in EOP](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-270">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="babd1-271">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’identité si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="babd1-271">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="babd1-272">Pour obtenir des instructions, voir [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="babd1-272">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="babd1-273">**Activer la fonctionnalité d’expéditeur non authentifié**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-273">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="babd1-274">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="babd1-274">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="babd1-275">**Actions**: spécifiez l’action à effectuer sur les messages qui échouent à l’aide d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="babd1-275">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="babd1-276">**Si un message électronique est envoyé par un utilisateur qui n’est pas autorisé à usurper votre domaine**:</span><span class="sxs-lookup"><span data-stu-id="babd1-276">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="babd1-277">**Déplacer le message vers les dossiers de courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="babd1-277">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="babd1-278">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="babd1-278">**Quarantine the message**</span></span>

   - <span data-ttu-id="babd1-279">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="babd1-279">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="babd1-280">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="babd1-280">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="babd1-281">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="babd1-281">You can toggle the following settings **On** or **Off** directly on this page:</span></span>
       - <span data-ttu-id="babd1-282">**Activer la protection contre l’usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="babd1-282">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="babd1-283">**Activer la fonctionnalité d’expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="babd1-283">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="babd1-284">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="babd1-284">When you're finished, click **Save** on any page.</span></span>

7. <span data-ttu-id="babd1-285">**Paramètres avancés**: cliquez sur **modifier** pour configurer les seuils avancés de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-285">**Advanced settings**: Click **Edit** to configure the advanced phishing thresholds.</span></span> <span data-ttu-id="babd1-286">Pour plus d’informations, reportez-vous à [seuils d’hameçonnage avancés dans la rubrique anti-hameçonnage Policies in Microsoft Defender for Office 365](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="babd1-286">For more information, see [Advanced phishing thresholds in anti-phishing policies in Microsoft Defender for Office 365](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span>

   - <span data-ttu-id="babd1-287">**Seuils de hameçonnage avancés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-287">**Advanced phishing thresholds**: Select one of the following values:</span></span>

   - <span data-ttu-id="babd1-288">**1-standard** (il s’agit de la valeur par défaut.)</span><span class="sxs-lookup"><span data-stu-id="babd1-288">**1 - Standard** (This is the default value.)</span></span>
   - <span data-ttu-id="babd1-289">**2-agressif**</span><span class="sxs-lookup"><span data-stu-id="babd1-289">**2 - Aggressive**</span></span>
   - <span data-ttu-id="babd1-290">**3-plus agressif**</span><span class="sxs-lookup"><span data-stu-id="babd1-290">**3 - More aggressive**</span></span>
   - <span data-ttu-id="babd1-291">**4-le plus agressif**</span><span class="sxs-lookup"><span data-stu-id="babd1-291">**4 - Most aggressive**</span></span>

   - <span data-ttu-id="babd1-292">**Vérifiez vos paramètres**: cliquez sur **modifier** pour revenir à la page **seuils avancés de hameçonnage** .</span><span class="sxs-lookup"><span data-stu-id="babd1-292">**Review your settings**: Click **Edit** to jump back to the **Advanced phishing thresholds** page.</span></span>

   <span data-ttu-id="babd1-293">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="babd1-293">When you're finished, click **Save** on either page.</span></span>

8. <span data-ttu-id="babd1-294">Sur la page **modifier votre stratégie \<Name\>** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="babd1-294">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-295">Utiliser le centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-295">Use the Security & Compliance Center to modify the default anti-phishing policy in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="babd1-296">La stratégie anti-hameçonnage par défaut dans Microsoft Defender pour Office 365 est appelée Office antiphishing par défaut et n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="babd1-296">The default anti-phishing policy in Microsoft Defender for Office 365 is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="babd1-297">Pour modifier la stratégie anti-hameçonnage par défaut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="babd1-297">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="babd1-298">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-298">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-299">Sur la page **anti-hameçonnage** , cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="babd1-299">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="babd1-300">La page **modifier votre stratégie d’anti-hameçonnage Office 365 par défaut** apparaît.</span><span class="sxs-lookup"><span data-stu-id="babd1-300">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="babd1-301">Les sections suivantes sont disponibles, qui contiennent les paramètres identiques lorsque vous [modifiez une stratégie personnalisée](#use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365):</span><span class="sxs-lookup"><span data-stu-id="babd1-301">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365):</span></span>

   - <span data-ttu-id="babd1-302">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="babd1-302">**Impersonation**</span></span>
   - <span data-ttu-id="babd1-303">**Tromp**</span><span class="sxs-lookup"><span data-stu-id="babd1-303">**Spoof**</span></span>
   - <span data-ttu-id="babd1-304">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="babd1-304">**Advanced settings**</span></span>

   <span data-ttu-id="babd1-305">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="babd1-305">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="babd1-306">Vous pouvez voir la section paramètres de **stratégie** et les valeurs, mais il n’existe aucun lien de **modification** , afin que vous ne puissiez pas modifier les paramètres (nom de stratégie, description et personnes auxquelles la stratégie s’applique (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="babd1-306">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="babd1-307">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-307">You can't delete the default policy.</span></span>
   - <span data-ttu-id="babd1-308">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="babd1-308">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="babd1-309">Sur la page **modifier votre stratégie par défaut pour les antiphishing Office 365** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="babd1-309">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-310">Activer ou désactiver les stratégies anti-hameçonnage personnalisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-310">Enable or disable custom anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="babd1-311">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-311">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-312">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="babd1-312">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="babd1-313">Faites glisser le bouton bascule sur **désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-313">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="babd1-314">Faites glisser le bouton bascule sur **activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="babd1-314">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="babd1-315">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-315">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-316">Définir la priorité des stratégies anti-hameçonnage personnalisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-316">Set the priority of custom anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="babd1-317">Par défaut, les stratégies de détection d’hameçonnage reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="babd1-317">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="babd1-318">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="babd1-318">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="babd1-319">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="babd1-319">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="babd1-320">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="babd1-320">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="babd1-321">Les stratégies anti-hameçonnage personnalisées sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="babd1-321">Custom anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="babd1-322">La stratégie anti-hameçonnage par défaut nommée Office antiphishing par défaut a une valeur de priorité personnalisée la **plus faible** et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="babd1-322">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="babd1-323">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie anti-hameçonnage une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="babd1-323">**Note**: In the Security & Compliance Center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="babd1-324">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle anti-hameçonnage (qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="babd1-324">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="babd1-325">Pour modifier la priorité d’une stratégie, cliquez sur **augmenter la priorité** ou sur **diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de **priorité** dans le centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="babd1-325">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="babd1-326">La modification de la priorité d’une stratégie n’a de sens que si vous disposez de plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="babd1-326">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="babd1-327">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-327">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-328">Sélectionnez la stratégie que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="babd1-328">Select the policy that you want to modify.</span></span> <span data-ttu-id="babd1-329">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="babd1-329">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="babd1-330">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="babd1-330">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="babd1-331">La stratégie anti-hameçonnage personnalisée avec la valeur  de priorité **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="babd1-331">The custom anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="babd1-332">La stratégie anti-hameçonnage personnalisée avec la valeur de **priorité** la plus faible (par exemple, **3**) a uniquement le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="babd1-332">The custom anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="babd1-333">Si vous avez au moins trois stratégies anti-hameçonnage personnalisées, les stratégies de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="babd1-333">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="babd1-334">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="babd1-334">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="babd1-335">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="babd1-335">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-336">Utiliser le centre de sécurité & conformité pour afficher les stratégies de détection d’hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-336">Use the Security & Compliance Center to view anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="babd1-337">Dans le centre de sécurité & conformité, puis accédez  à \>  \> **protection contre les** menaces pour le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-337">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-338">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-338">Do one of the following steps:</span></span>

   - <span data-ttu-id="babd1-339">Sélectionnez une stratégie anti-hameçonnage personnalisée que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="babd1-339">Select a custom anti-phishing policy that you want to view.</span></span> <span data-ttu-id="babd1-340">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="babd1-340">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="babd1-341">Cliquez sur **stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-341">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="babd1-342">Le menu volant **modifier \<name\> votre stratégie** apparaît, dans lequel vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="babd1-342">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-343">Utiliser le centre de sécurité & conformité pour supprimer les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-343">Use the Security & Compliance Center to remove anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="babd1-344">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-344">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="babd1-345">Sélectionnez la stratégie que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="babd1-345">Select the policy that you want to remove.</span></span> <span data-ttu-id="babd1-346">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="babd1-346">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="babd1-347">Dans le menu volant **modifier \<name\> votre stratégie** qui s’affiche, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="babd1-347">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="babd1-348">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="babd1-348">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="babd1-349">Utiliser Exchange Online PowerShell pour configurer les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="babd1-349">Use Exchange Online PowerShell to configure anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="babd1-350">Comme décrit précédemment, une stratégie de blocage du courrier indésirable se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-350">As previously described, an anti-spam policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="babd1-351">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est apparente.</span><span class="sxs-lookup"><span data-stu-id="babd1-351">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="babd1-352">Vous pouvez gérer les stratégies anti-hameçonnage à l’aide des cmdlets **\* -antiphishpolicy permet** et gérer les règles anti-hameçonnage à l’aide des cmdlets **\* -antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="babd1-352">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="babd1-353">Dans PowerShell, vous devez d’abord créer la stratégie anti-hameçonnage, puis créer la règle anti-hameçonnage qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="babd1-353">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="babd1-354">Dans PowerShell, vous modifiez les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage séparément.</span><span class="sxs-lookup"><span data-stu-id="babd1-354">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="babd1-355">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="babd1-355">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="babd1-356">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-356">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="babd1-357">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="babd1-357">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="babd1-358">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-358">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="babd1-359">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="babd1-359">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="babd1-360">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="babd1-360">**Notes**:</span></span>

- <span data-ttu-id="babd1-361">Vous pouvez créer une nouvelle règle anti-hameçonnage et lui affecter une stratégie anti-hameçonnage existante non associée.</span><span class="sxs-lookup"><span data-stu-id="babd1-361">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="babd1-362">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-362">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="babd1-363">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage de PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="babd1-363">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="babd1-364">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="babd1-364">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="babd1-365">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="babd1-365">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="babd1-366">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’avez pas affecté la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-366">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="babd1-367">Étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-367">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="babd1-368">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-368">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="babd1-369">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="babd1-369">This example creates anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="babd1-370">La stratégie est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="babd1-370">The policy is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>
- <span data-ttu-id="babd1-371">Description : stratégie de service de recherche.</span><span class="sxs-lookup"><span data-stu-id="babd1-371">The description is: Research department policy.</span></span>
- <span data-ttu-id="babd1-372">Active la protection des domaines de l’Organisation pour tous les domaines acceptés et la protection des domaines ciblés pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="babd1-372">Enables organization domains protection for all accepted domains, and targeted domains protection for fabrikam.com.</span></span>
- <span data-ttu-id="babd1-373">Spécifie Mai Fujito (mfujito@fabrikam.com) en tant qu’utilisateur pour empêcher l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="babd1-373">Specifies Mai Fujito (mfujito@fabrikam.com) as the user to protect from impersonation.</span></span>
- <span data-ttu-id="babd1-374">Active la boîte aux lettres décisionnelle.</span><span class="sxs-lookup"><span data-stu-id="babd1-374">Enables mailbox intelligence.</span></span>
- <span data-ttu-id="babd1-375">Active la protection contre les boîtes aux lettres et spécifie l’action de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="babd1-375">Enables mailbox intelligence protection, and specifies the quarantine action.</span></span>
- <span data-ttu-id="babd1-376">Active les conseils de sécurité.</span><span class="sxs-lookup"><span data-stu-id="babd1-376">Enables safety tips.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -EnableOrganizationDomainsProtection $true -EnableTargetedDomainsProtection $true -TargetedDomainsToProtect fabrikam.com -TargetedDomainProtectionAction Quarantine -EnableTargetedUserProtection $true -TargetedUsersToProtect "Mai Fujito;mfujito@fabrikam.com" -TargetedUserProtectionAction Quarantine -EnableMailboxIntelligence $true -EnableMailboxIntelligenceProtection $true -MailboxIntelligenceProtectionAction Quarantine -EnableSimilarUsersSafetyTips $true -EnableSimilarDomainsSafetyTips $true -EnableUnusualCharactersSafetyTips $true
```

<span data-ttu-id="babd1-377">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="babd1-377">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="babd1-378">Étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-378">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="babd1-379">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-379">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="babd1-380">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-380">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="babd1-381">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="babd1-381">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="babd1-382">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="babd1-382">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="babd1-383">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="babd1-383">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="babd1-384">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="babd1-384">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="babd1-385">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-385">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="babd1-386">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-386">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="babd1-387">Cet exemple renvoie la liste récapitulative de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="babd1-387">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="babd1-388">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="babd1-388">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="babd1-389">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="babd1-389">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="babd1-390">Utiliser PowerShell pour afficher les règles de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-390">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="babd1-391">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-391">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="babd1-392">Cet exemple renvoie la liste récapitulative de toutes les règles anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="babd1-392">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="babd1-393">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-393">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="babd1-394">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="babd1-394">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="babd1-395">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="babd1-395">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="babd1-396">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-396">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="babd1-397">À l’exception des éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell comme lors de la création de la stratégie, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="babd1-397">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) section earlier in this article.</span></span>

- <span data-ttu-id="babd1-398">Le commutateur _MakeDefault_ qui désactive la stratégie spécifiée dans la stratégie par défaut (appliquée à tout le monde, toujours à la priorité la **plus basse** et vous ne pouvez pas le supprimer) n’est disponible que lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="babd1-398">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="babd1-399">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (l’applet de commande **Set-antiphishpolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="babd1-399">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="babd1-400">Lorsque vous renommez une stratégie anti-hameçonnage dans le centre de sécurité & conformité, vous renommez uniquement la _règle_ anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="babd1-400">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="babd1-401">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-401">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="babd1-402">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="babd1-402">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="babd1-403">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-403">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="babd1-404">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="babd1-404">The only setting that isn't available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="babd1-405">Pour activer ou désactiver les règles anti-hameçonnage existantes, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="babd1-405">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="babd1-406">Dans le cas contraire, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="babd1-406">Otherwise, no additional settings are available when you modify an anti-phish rule in PowerShell.</span></span> <span data-ttu-id="babd1-407">Les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) , plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="babd1-407">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="babd1-408">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-408">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="babd1-409">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="babd1-409">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="babd1-410">Utiliser PowerShell pour activer ou désactiver les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-410">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="babd1-411">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive la totalité de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="babd1-411">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="babd1-412">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="babd1-412">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="babd1-413">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-413">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="babd1-414">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="babd1-414">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="babd1-415">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="babd1-415">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="babd1-416">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) et [Disable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="babd1-416">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="babd1-417">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-417">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="babd1-418">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="babd1-418">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="babd1-419">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="babd1-419">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="babd1-420">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="babd1-420">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="babd1-421">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="babd1-421">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="babd1-422">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="babd1-422">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="babd1-423">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-423">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="babd1-p148">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="babd1-p148">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="babd1-426">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="babd1-426">**Notes**:</span></span>

- <span data-ttu-id="babd1-427">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="babd1-427">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="babd1-428">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante, elle a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="babd1-428">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="babd1-429">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-429">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="babd1-430">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="babd1-430">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="babd1-431">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-431">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="babd1-432">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="babd1-432">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="babd1-433">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="babd1-433">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="babd1-434">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="babd1-434">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="babd1-435">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="babd1-435">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="babd1-436">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="babd1-436">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="babd1-437">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="babd1-437">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="babd1-438">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="babd1-438">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="babd1-439">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="babd1-439">How do you know these procedures worked?</span></span>

<span data-ttu-id="babd1-440">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-440">To verify that you've successfully configured anti-phishing policies in Microsoft Defender for Office 365, do any of the following steps:</span></span>

- <span data-ttu-id="babd1-441">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="babd1-441">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span> <span data-ttu-id="babd1-442">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="babd1-442">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="babd1-443">Pour afficher plus de détails, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd1-443">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="babd1-444">Sélectionnez la stratégie dans la liste, puis affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="babd1-444">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="babd1-445">Cliquez sur **stratégie par défaut** et affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="babd1-445">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="babd1-446">Dans Exchange Online PowerShell, remplacez \<Name\> par le nom de la stratégie ou de la règle, puis exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="babd1-446">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, and run the following command and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
