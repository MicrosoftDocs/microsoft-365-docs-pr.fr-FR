---
title: Configurer des stratégies anti-hameçonnage dans EOP
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
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage disponibles dans les organisations Exchange Online Protection (EOP) avec ou sans boîte aux lettres Exchange Online.
ms.openlocfilehash: 03c1ce8e940491607fe04988d41c927f92479d96
ms.sourcegitcommit: 222fb7fe2b26dde3d8591b61cc02113d6135012c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49760331"
---
# <a name="configure-anti-phishing-policies-in-eop"></a><span data-ttu-id="b8a36-103">Configurer des stratégies anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="b8a36-103">Configure anti-phishing policies in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="b8a36-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, il existe une stratégie anti-hameçonnage par défaut qui contient un nombre limité de fonctionnalités anti-usurpation d’identité activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there's a default anti-phishing policy that contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="b8a36-105">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="b8a36-105">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="b8a36-106">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-106">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="b8a36-107">Pour une granularité accrue, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b8a36-107">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="b8a36-108">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-108">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="b8a36-109">Les organisations disposant d’une boîte aux lettres Exchange Online peuvent configurer des stratégies anti-hameçonnage dans le centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8a36-109">Organizations with Exchange Online mailboxes can configure anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span> <span data-ttu-id="b8a36-110">Les organisations EOP autonomes peuvent utiliser uniquement le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b8a36-110">Standalone EOP organizations can only use the Security & Compliance Center.</span></span>

<span data-ttu-id="b8a36-111">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées dans Microsoft Defender pour Office 365 qui sont disponibles dans Defender for Office 365, consultez la rubrique [configure anti-phishing Policies in Microsoft Defender for office 365](configure-atp-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b8a36-111">For information about creating and modifying the more advanced anti-phishing policies in Microsoft Defender for Office 365 that are available in Defender for Office 365, see [Configure anti-phishing policies in Microsoft Defender for Office 365](configure-atp-anti-phishing-policies.md).</span></span>

<span data-ttu-id="b8a36-112">Les éléments de base d’une stratégie anti-hameçonnage sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b8a36-112">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="b8a36-113">**Stratégie anti-hameçonnage**: spécifie les protections de hameçonnage à activer ou à désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="b8a36-113">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="b8a36-114">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-114">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="b8a36-115">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de détection d’hameçonnage dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="b8a36-115">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="b8a36-116">Lorsque vous créez une stratégie anti-hameçonnage, vous créez en réalité une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="b8a36-116">When you create an anti-phishing policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="b8a36-117">Lorsque vous modifiez une stratégie anti-hameçonnage, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-117">When you modify an anti-phishing policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="b8a36-118">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-118">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="b8a36-119">Lorsque vous supprimez une stratégie anti-hameçonnage, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-119">When you remove an anti-phishing policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="b8a36-120">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="b8a36-120">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="b8a36-121">Pour plus d’informations, consultez la section [utiliser Exchange Online PowerShell pour configurer les stratégies anti-hameçonnage](#use-exchange-online-powershell-to-configure-anti-phishing-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b8a36-121">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies](#use-exchange-online-powershell-to-configure-anti-phishing-policies) section later in this article.</span></span>

<span data-ttu-id="b8a36-122">Chaque organisation dispose d’une stratégie anti-hameçonnage intégrée nommée Office antiphishing par défaut, qui comporte les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-122">Every organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="b8a36-123">La stratégie est appliquée à tous les destinataires de l’organisation, même s’il n’y a aucune règle anti-hameçonnage (filtres de destinataire) associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-123">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="b8a36-124">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="b8a36-124">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="b8a36-125">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-125">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="b8a36-126">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-126">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="b8a36-127">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b8a36-127">To increase the effectiveness of anti-phishing protection, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b8a36-128">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b8a36-128">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b8a36-129">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="b8a36-129">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="b8a36-130">Pour accéder directement à la page **anti-hameçonnage** , utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="b8a36-130">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="b8a36-131">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="b8a36-131">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

  <span data-ttu-id="b8a36-132">Vous ne pouvez pas gérer les stratégies de détection d’hameçonnage dans une version autonome d’EOP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8a36-132">You can't manage anti-phishing policies in standalone EOP PowerShell.</span></span>

- <span data-ttu-id="b8a36-133">Des autorisations doivent vous avoir été attribuées dans le Centre de sécurité et de conformité pour que vous puissiez effectuer les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b8a36-133">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="b8a36-134">Pour ajouter, modifier et supprimer des stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-134">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="b8a36-135">Pour un accès en lecture seule aux stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur** de sécurité <sup>\*</sup> .</span><span class="sxs-lookup"><span data-stu-id="b8a36-135">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups<sup>\*</sup>.</span></span>

  <span data-ttu-id="b8a36-136">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b8a36-136">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="b8a36-137">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="b8a36-137">**Notes**:</span></span>

  - <span data-ttu-id="b8a36-138">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b8a36-138">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="b8a36-139">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="b8a36-139">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="b8a36-140">Le groupe de rôles gestion de l' **Organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) offre également un accès en lecture seule à la fonctionnalité <sup>\*</sup> .</span><span class="sxs-lookup"><span data-stu-id="b8a36-140">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>
  - <span data-ttu-id="b8a36-141"><sup>\*</sup> Dans le centre de sécurité & conformité, l’accès en lecture seule permet aux utilisateurs d’afficher les paramètres des stratégies anti-hameçonnage personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-141"><sup>\*</sup> In the Security & Compliance Center, read-only access allows users to view the settings of custom anti-phishing policies.</span></span> <span data-ttu-id="b8a36-142">Les utilisateurs en lecture seule ne peuvent pas voir les paramètres dans la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-142">Read-only users can't see the settings in the default anti-phishing policy.</span></span>

- <span data-ttu-id="b8a36-143">Pour créer et modifier des stratégies de détection d’hameçonnage dans un EOP autonome, vous devez effectuer une opération qui nécessite l' _hydratation_ de votre client.</span><span class="sxs-lookup"><span data-stu-id="b8a36-143">To create and modify anti-phishing policies in standalone EOP, you need to do something that requires _hydration_ for your tenant.</span></span> <span data-ttu-id="b8a36-144">Par exemple, dans le centre d’administration Exchange, vous pouvez accéder à l’onglet **autorisations** , sélectionner un groupe de rôles existant, cliquer sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) , puis supprimer un rôle (ce que vous devrez finalement rajouter).</span><span class="sxs-lookup"><span data-stu-id="b8a36-144">For example, in the Exchange admin center (EAC), you can go to the **Permissions** tab, select an existing role group, click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and remove a role (which you'll ultimately add back).</span></span> <span data-ttu-id="b8a36-145">Si votre locataire n’a jamais été hydraté, vous obtenez une boîte de dialogue intitulée **mettre à jour les paramètres d’organisation** avec une barre de progression qui doit se terminer avec succès.</span><span class="sxs-lookup"><span data-stu-id="b8a36-145">If your tenant has never been hydrated, you get a dialog named **Update Organization Settings** with a progress bar that should complete successfully.</span></span> <span data-ttu-id="b8a36-146">Pour plus d’informations sur la mise en attente, reportez-vous à la cmdlet [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) (qui n’est pas disponible dans la version autonome d’EOP PowerShell ou dans le centre de conformité & Security).</span><span class="sxs-lookup"><span data-stu-id="b8a36-146">For more information about hydration, see the [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) cmdlet (which isn't available in standalone EOP PowerShell or in the Security & Compliance Center).</span></span>

- <span data-ttu-id="b8a36-147">Pour connaître les paramètres recommandés pour les stratégies de détection d’hameçonnage, consultez les paramètres de la [stratégie anti-hameçonnage par défaut EOP](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="b8a36-147">For our recommended settings for anti-phishing policies, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="b8a36-148">Autorisez jusqu’à 30 minutes pour l’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b8a36-148">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="b8a36-149">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, consultez la rubrique [Order and Precedence of e-mail protection](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="b8a36-149">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-anti-phishing-policies"></a><span data-ttu-id="b8a36-150">Utiliser le centre de sécurité & conformité pour créer des stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-150">Use the Security & Compliance Center to create anti-phishing policies</span></span>

<span data-ttu-id="b8a36-151">La création d’une stratégie anti-hameçonnage personnalisée dans le centre de sécurité & conformité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="b8a36-151">Creating a custom anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="b8a36-152">Lorsque vous créez une stratégie anti-hameçonnage, vous pouvez uniquement spécifier le nom de la stratégie, sa description et le filtre de destinataire qui identifie la personne à laquelle la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="b8a36-152">When you create an anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="b8a36-153">Après avoir créé la stratégie, vous pouvez modifier la stratégie pour modifier ou consulter les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-153">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="b8a36-154">Dans le centre de sécurité & conformité, accédez  à \>  \> **protection anti-hameçonnage** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b8a36-154">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-155">Sur la page **anti-hameçonnage** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-155">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="b8a36-156">L’Assistant **créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b8a36-156">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="b8a36-157">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8a36-157">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="b8a36-158">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-158">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="b8a36-159">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-159">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="b8a36-160">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-160">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="b8a36-161">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-161">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="b8a36-162">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="b8a36-162">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="b8a36-163">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="b8a36-163">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="b8a36-164">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="b8a36-164">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="b8a36-165">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-165">Click **Add a condition**.</span></span> <span data-ttu-id="b8a36-166">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="b8a36-166">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="b8a36-167">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b8a36-167">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="b8a36-168">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b8a36-168">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="b8a36-169">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b8a36-169">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="b8a36-170">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="b8a36-170">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="b8a36-171">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="b8a36-171">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="b8a36-172">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="b8a36-172">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="b8a36-173">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="b8a36-173">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="b8a36-174">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="b8a36-174">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="b8a36-175">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="b8a36-175">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="b8a36-176">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-176">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="b8a36-177">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-177">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="b8a36-178">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="b8a36-178">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="b8a36-179">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-179">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="b8a36-180">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="b8a36-180">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="b8a36-181">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="b8a36-181">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="b8a36-182">Lorsque vous avez terminé, cliquez sur **créer cette stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-182">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="b8a36-183">Cliquez sur **OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b8a36-183">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="b8a36-184">Après avoir créé la stratégie anti-hameçonnage avec ces paramètres généraux de stratégie, suivez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-184">After you create the anti-phishing policy with these general policy settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-anti-phishing-policies"></a><span data-ttu-id="b8a36-185">Utiliser le centre de sécurité & conformité pour modifier des stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-185">Use the Security & Compliance Center to modify anti-phishing policies</span></span>

<span data-ttu-id="b8a36-186">Utilisez les procédures suivantes pour modifier les stratégies de détection d’hameçonnage : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-186">Use the following procedures to modify anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="b8a36-187">Si vous ne l’avez pas encore fait, ouvrez le centre de sécurité & conformité, puis **accédez à** \>  \> **protection contre le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-187">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-188">Sélectionnez la stratégie anti-hameçonnage personnalisée que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="b8a36-188">Select the custom anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="b8a36-189">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b8a36-189">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="b8a36-190">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="b8a36-190">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="b8a36-191">Si vous cliquez sur **modifier** dans une section, vous pouvez accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="b8a36-191">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="b8a36-192">Les étapes suivantes sont présentées dans l’ordre dans lequel les sections apparaissent, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="b8a36-192">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="b8a36-193">Une fois que vous avez cliqué sur **modifier** dans une section, les paramètres disponibles sont présentés dans un format d’Assistant, mais vous pouvez sauter les pages dans n’importe quel ordre, et vous pouvez cliquer sur **Enregistrer** sur n’importe quelle page (ou sur **Annuler** ou **Fermer** l' ![ icône ](../../media/scc-remove-icon.png) pour revenir à la page **modifier votre stratégie \<name\>** (vous n’avez pas besoin de consulter la dernière page de l’Assistant pour enregistrer ou quitter</span><span class="sxs-lookup"><span data-stu-id="b8a36-193">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="b8a36-194">**Paramètre de stratégie**: cliquez sur **modifier** pour modifier les mêmes paramètres que ceux qui étaient disponibles lorsque vous avez [créé la stratégie](#use-the-security--compliance-center-to-create-anti-phishing-policies) dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="b8a36-194">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-anti-phishing-policies) in the previous section:</span></span>

   - <span data-ttu-id="b8a36-195">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8a36-195">**Name**</span></span>
   - <span data-ttu-id="b8a36-196">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8a36-196">**Description**</span></span>
   - <span data-ttu-id="b8a36-197">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="b8a36-197">**Applied to**</span></span>
   - <span data-ttu-id="b8a36-198">**Vérifier vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="b8a36-198">**Review your settings**</span></span>

   <span data-ttu-id="b8a36-199">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="b8a36-199">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="b8a36-200">**Spoof**: cliquez sur **modifier** pour activer ou désactiver l’Assistant usurpation d’identité, activez ou désactivez l’identification de l’expéditeur non authentifié dans Outlook, puis configurez l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués.</span><span class="sxs-lookup"><span data-stu-id="b8a36-200">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="b8a36-201">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="b8a36-201">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="b8a36-202">Notez que ces mêmes paramètres sont également disponibles dans les stratégies de détection d’hameçonnage dans Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="b8a36-202">Note that these same settings are also available in anti-phishing policies in Defender for Office 365.</span></span>

   - <span data-ttu-id="b8a36-203">**Usurpation des paramètres de filtrage**: la valeur par défaut est **activée**, et nous vous recommandons de la laisser activée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-203">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="b8a36-204">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-204">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="b8a36-205">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in EOP](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="b8a36-205">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="b8a36-206">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’identité si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="b8a36-206">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="b8a36-207">Pour obtenir des instructions, voir [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="b8a36-207">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="b8a36-208">**Activer la fonctionnalité d’expéditeur non authentifié**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-208">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="b8a36-209">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-209">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="b8a36-210">**Actions**: spécifiez l’action à effectuer sur les messages qui échouent à l’aide d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="b8a36-210">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="b8a36-211">**Si un message électronique est envoyé par un utilisateur qui n’est pas autorisé à usurper votre domaine**:</span><span class="sxs-lookup"><span data-stu-id="b8a36-211">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="b8a36-212">**Déplacer le message vers les dossiers de courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="b8a36-212">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="b8a36-213">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="b8a36-213">**Quarantine the message**</span></span>

   - <span data-ttu-id="b8a36-214">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="b8a36-214">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="b8a36-215">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-215">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="b8a36-216">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="b8a36-216">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="b8a36-217">**Activer la protection contre l’usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="b8a36-217">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="b8a36-218">**Activer la fonctionnalité d’expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="b8a36-218">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="b8a36-219">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="b8a36-219">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="b8a36-220">Sur la page **modifier votre stratégie \<Name\>** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-220">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy"></a><span data-ttu-id="b8a36-221">Utiliser le centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="b8a36-221">Use the Security & Compliance Center to modify the default anti-phishing policy</span></span>

<span data-ttu-id="b8a36-222">La stratégie anti-hameçonnage par défaut est nommée Office antiphishing par défaut et n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="b8a36-222">The default anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="b8a36-223">Pour modifier la stratégie anti-hameçonnage par défaut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b8a36-223">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="b8a36-224">Dans le centre de sécurité & conformité, accédez  à \>  \> **protection anti-hameçonnage** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b8a36-224">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-225">Sur la page **anti-hameçonnage** , cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-225">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="b8a36-226">La page **modifier votre stratégie d’anti-hameçonnage Office 365 par défaut** apparaît.</span><span class="sxs-lookup"><span data-stu-id="b8a36-226">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="b8a36-227">Les sections suivantes sont disponibles, qui contiennent les paramètres identiques lorsque vous [modifiez une stratégie personnalisée](#use-the-security--compliance-center-to-modify-anti-phishing-policies).</span><span class="sxs-lookup"><span data-stu-id="b8a36-227">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-anti-phishing-policies).</span></span>

   - <span data-ttu-id="b8a36-228">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="b8a36-228">**Impersonation**</span></span>
   - <span data-ttu-id="b8a36-229">**Tromp**</span><span class="sxs-lookup"><span data-stu-id="b8a36-229">**Spoof**</span></span>
   - <span data-ttu-id="b8a36-230">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="b8a36-230">**Advanced settings**</span></span>

   <span data-ttu-id="b8a36-231">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="b8a36-231">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="b8a36-232">Vous pouvez voir la section paramètres de **stratégie** et les valeurs, mais il n’existe aucun lien de **modification** , afin que vous ne puissiez pas modifier les paramètres (nom de stratégie, description et personnes auxquelles la stratégie s’applique (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="b8a36-232">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="b8a36-233">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-233">You can't delete the default policy.</span></span>
   - <span data-ttu-id="b8a36-234">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="b8a36-234">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="b8a36-235">Sur la page **modifier votre stratégie par défaut pour les antiphishing Office 365** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-235">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies"></a><span data-ttu-id="b8a36-236">Activer ou désactiver les stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="b8a36-236">Enable or disable custom anti-phishing policies</span></span>

1. <span data-ttu-id="b8a36-237">Dans le centre de sécurité & conformité, accédez  à \>  \> **protection anti-hameçonnage** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b8a36-237">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-238">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="b8a36-238">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="b8a36-239">Faites glisser le bouton bascule sur **désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-239">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="b8a36-240">Faites glisser le bouton bascule sur **activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b8a36-240">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="b8a36-241">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-241">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies"></a><span data-ttu-id="b8a36-242">Définir la priorité des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="b8a36-242">Set the priority of custom anti-phishing policies</span></span>

<span data-ttu-id="b8a36-243">Par défaut, les stratégies de détection d’hameçonnage reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="b8a36-243">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="b8a36-244">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="b8a36-244">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="b8a36-245">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-245">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="b8a36-246">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="b8a36-246">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="b8a36-247">Les stratégies anti-hameçonnage personnalisées sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="b8a36-247">Custom anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="b8a36-248">La stratégie anti-hameçonnage par défaut nommée Office antiphishing par défaut a une valeur de priorité personnalisée la **plus faible** et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="b8a36-248">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="b8a36-249">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie anti-hameçonnage une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-249">**Note**: In the Security & Compliance Center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="b8a36-250">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle anti-hameçonnage (qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="b8a36-250">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="b8a36-251">Pour modifier la priorité d’une stratégie, cliquez sur **augmenter la priorité** ou sur **diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de **priorité** dans le centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="b8a36-251">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="b8a36-252">La modification de la priorité d’une stratégie n’a de sens que si vous disposez de plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="b8a36-252">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="b8a36-253">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \>  \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-253">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-254">Sélectionnez la stratégie que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="b8a36-254">Select the policy that you want to modify.</span></span> <span data-ttu-id="b8a36-255">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b8a36-255">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="b8a36-256">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="b8a36-256">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="b8a36-257">La stratégie anti-hameçonnage personnalisée avec la valeur  de priorité **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="b8a36-257">The custom anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="b8a36-258">La stratégie anti-hameçonnage personnalisée avec la valeur de **priorité** la plus faible (par exemple, **3**) a uniquement le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="b8a36-258">The custom anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="b8a36-259">Si vous avez au moins trois stratégies anti-hameçonnage personnalisées, les stratégies de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-259">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="b8a36-260">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-260">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="b8a36-261">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-261">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-anti-phishing-policies"></a><span data-ttu-id="b8a36-262">Utiliser le centre de sécurité & conformité pour afficher les stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-262">Use the Security & Compliance Center to view anti-phishing policies</span></span>

1. <span data-ttu-id="b8a36-263">Dans le centre de sécurité & conformité, puis accédez **à** \>  \> **protection contre le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-263">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-264">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-264">Do one of the following steps:</span></span>

   - <span data-ttu-id="b8a36-265">Sélectionnez une stratégie anti-hameçonnage personnalisée que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="b8a36-265">Select a custom anti-phishing policy that you want to view.</span></span> <span data-ttu-id="b8a36-266">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b8a36-266">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="b8a36-267">Cliquez sur **stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-267">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="b8a36-268">Le menu volant **modifier \<name\> votre stratégie** apparaît, dans lequel vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b8a36-268">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-anti-phishing-policies"></a><span data-ttu-id="b8a36-269">Utiliser le centre de sécurité & conformité pour supprimer les stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-269">Use the Security & Compliance Center to remove anti-phishing policies</span></span>

1. <span data-ttu-id="b8a36-270">Dans le centre de sécurité & conformité, accédez  à \>  \> **protection anti-hameçonnage** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b8a36-270">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="b8a36-271">Sélectionnez la stratégie que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="b8a36-271">Select the policy that you want to remove.</span></span> <span data-ttu-id="b8a36-272">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b8a36-272">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="b8a36-273">Dans le menu volant **modifier \<name\> votre stratégie** qui s’affiche, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b8a36-273">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="b8a36-274">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a36-274">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies"></a><span data-ttu-id="b8a36-275">Utiliser Exchange Online PowerShell pour configurer les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-275">Use Exchange Online PowerShell to configure anti-phishing policies</span></span>

<span data-ttu-id="b8a36-276">Comme décrit précédemment, une stratégie anti-hameçonnage se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-276">As previously described, an anti-phishing policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="b8a36-277">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est apparente.</span><span class="sxs-lookup"><span data-stu-id="b8a36-277">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="b8a36-278">Vous pouvez gérer les stratégies anti-hameçonnage à l’aide des cmdlets **\* -antiphishpolicy permet** et gérer les règles anti-hameçonnage à l’aide des cmdlets **\* -antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-278">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="b8a36-279">Dans PowerShell, vous devez d’abord créer la stratégie anti-hameçonnage, puis créer la règle anti-hameçonnage qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="b8a36-279">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="b8a36-280">Dans PowerShell, vous modifiez les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage séparément.</span><span class="sxs-lookup"><span data-stu-id="b8a36-280">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="b8a36-281">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="b8a36-281">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

> [!NOTE]
> <span data-ttu-id="b8a36-282">Les procédures PowerShell suivantes ne sont pas disponibles dans les organisations EOP autonomes utilisant Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8a36-282">The following PowerShell procedures aren't available in standalone EOP organizations using Exchange Online Protection PowerShell.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="b8a36-283">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-283">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="b8a36-284">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-284">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="b8a36-285">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-285">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="b8a36-286">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="b8a36-286">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="b8a36-287">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="b8a36-287">**Notes**:</span></span>

- <span data-ttu-id="b8a36-288">Vous pouvez créer une nouvelle règle anti-hameçonnage et lui affecter une stratégie anti-hameçonnage existante non associée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-288">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="b8a36-289">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-289">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="b8a36-290">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage de PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="b8a36-290">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="b8a36-291">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="b8a36-291">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="b8a36-292">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="b8a36-292">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="b8a36-293">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’avez pas affecté la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-293">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="b8a36-294">Étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-294">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="b8a36-295">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-295">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-EnableSpoofIntelligence <$true | $false>] [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableUnauthenticatedSender <$true | $false>]
```

<span data-ttu-id="b8a36-296">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8a36-296">This example creates an anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="b8a36-297">Description : stratégie de service de recherche.</span><span class="sxs-lookup"><span data-stu-id="b8a36-297">The description is: Research department policy.</span></span>
- <span data-ttu-id="b8a36-298">Remplace l’action par défaut pour l’usurpation en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b8a36-298">Changes the default action for spoofing to Quarantine.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="b8a36-299">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="b8a36-299">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="b8a36-300">Étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-300">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="b8a36-301">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-301">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="b8a36-302">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-302">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="b8a36-303">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="b8a36-303">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="b8a36-304">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="b8a36-304">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="b8a36-305">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-305">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="b8a36-306">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="b8a36-306">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="b8a36-307">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-307">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="b8a36-308">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-308">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="b8a36-309">Cet exemple renvoie la liste récapitulative de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-309">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="b8a36-310">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="b8a36-310">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="b8a36-311">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="b8a36-311">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="b8a36-312">Utiliser PowerShell pour afficher les règles de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-312">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="b8a36-313">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-313">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="b8a36-314">Cet exemple renvoie la liste récapitulative de toutes les règles anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b8a36-314">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="b8a36-315">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-315">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="b8a36-316">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="b8a36-316">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="b8a36-317">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="b8a36-317">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="b8a36-318">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-318">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="b8a36-319">À l’exception des éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell comme lors de la création d’une stratégie, comme décrit dans l' [étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b8a36-319">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create a policy as described in [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) earlier in this article.</span></span>

- <span data-ttu-id="b8a36-320">Le commutateur _MakeDefault_ qui désactive la stratégie spécifiée dans la stratégie par défaut (appliquée à tout le monde, toujours à la priorité la **plus basse** et vous ne pouvez pas le supprimer) n’est disponible que lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8a36-320">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="b8a36-321">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (l’applet de commande **Set-antiphishpolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="b8a36-321">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="b8a36-322">Lorsque vous renommez une stratégie anti-hameçonnage dans le centre de sécurité & conformité, vous renommez uniquement la _règle_ anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b8a36-322">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="b8a36-323">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-323">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="b8a36-324">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="b8a36-324">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="b8a36-325">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-325">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="b8a36-326">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-326">The only setting that's not available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="b8a36-327">Pour activer ou désactiver les règles anti-hameçonnage existantes, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="b8a36-327">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="b8a36-328">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) , plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b8a36-328">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="b8a36-329">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-329">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="b8a36-330">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="b8a36-330">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="b8a36-331">Utiliser PowerShell pour activer ou désactiver les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-331">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="b8a36-332">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive la totalité de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="b8a36-332">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="b8a36-333">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="b8a36-333">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="b8a36-334">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-334">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="b8a36-335">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="b8a36-335">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="b8a36-336">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="b8a36-336">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="b8a36-337">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) et [Disable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="b8a36-337">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="b8a36-338">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-338">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="b8a36-339">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="b8a36-339">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="b8a36-340">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="b8a36-340">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="b8a36-341">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="b8a36-341">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="b8a36-342">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="b8a36-342">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="b8a36-343">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="b8a36-343">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="b8a36-344">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-344">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="b8a36-p138">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="b8a36-p138">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="b8a36-347">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="b8a36-347">**Notes**:</span></span>

- <span data-ttu-id="b8a36-348">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-348">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="b8a36-349">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante, elle a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="b8a36-349">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="b8a36-350">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-350">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="b8a36-351">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-351">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="b8a36-352">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-352">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="b8a36-353">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="b8a36-353">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="b8a36-354">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="b8a36-354">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="b8a36-355">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b8a36-355">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="b8a36-356">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="b8a36-356">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="b8a36-357">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b8a36-357">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="b8a36-358">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="b8a36-358">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="b8a36-359">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="b8a36-359">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="b8a36-360">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="b8a36-360">How do you know these procedures worked?</span></span>

<span data-ttu-id="b8a36-361">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-361">To verify that you've successfully configured anti-phishing policies in Microsoft Defender for Office 365, do any of the following steps:</span></span>

- <span data-ttu-id="b8a36-362">Dans le centre de sécurité & conformité, accédez  à \>  \> **protection anti-hameçonnage** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b8a36-362">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span> <span data-ttu-id="b8a36-363">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="b8a36-363">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="b8a36-364">Pour afficher plus de détails, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a36-364">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="b8a36-365">Sélectionnez la stratégie dans la liste, puis affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="b8a36-365">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="b8a36-366">Cliquez sur **stratégie par défaut** et affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="b8a36-366">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="b8a36-367">Dans Exchange Online PowerShell, remplacez \<Name\> par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="b8a36-367">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
