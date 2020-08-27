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
ms.openlocfilehash: 3b83bcd3c60dbd779d727a79f6689fdf0004d340
ms.sourcegitcommit: 195172dd836e8a793e8e0c2db3323b7391bc51ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2020
ms.locfileid: "47255756"
---
# <a name="configure-anti-phishing-policies-in-eop"></a><span data-ttu-id="d04ad-103">Configurer des stratégies anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="d04ad-103">Configure anti-phishing policies in EOP</span></span>

<span data-ttu-id="d04ad-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, il existe une stratégie anti-hameçonnage par défaut qui contient un nombre limité de fonctionnalités anti-usurpation d’identité activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there's a default anti-phishing policy that contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="d04ad-105">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="d04ad-105">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="d04ad-106">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-106">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="d04ad-107">Pour une granularité accrue, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d04ad-107">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="d04ad-108">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d04ad-108">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="d04ad-109">Les organisations disposant d’une boîte aux lettres Exchange Online peuvent configurer des stratégies anti-hameçonnage dans le centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d04ad-109">Organizations with Exchange Online mailboxes can configure anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span> <span data-ttu-id="d04ad-110">Les organisations EOP autonomes peuvent utiliser uniquement le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="d04ad-110">Standalone EOP organizations can only use the Security & Compliance Center.</span></span>

<span data-ttu-id="d04ad-111">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées disponibles dans Office 365 Advanced Threat Protection (Office 365 ATP), voir [configure ATP anti-phishing Policies](configure-atp-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-111">For information about creating and modifying the more advanced ATP anti-phishing policies that are available in Office 365 Advanced Threat Protection (Office 365 ATP), see [Configure ATP anti-phishing policies](configure-atp-anti-phishing-policies.md).</span></span>

<span data-ttu-id="d04ad-112">Les éléments de base d’une stratégie anti-hameçonnage sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d04ad-112">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="d04ad-113">**Stratégie anti-hameçonnage**: spécifie les protections de hameçonnage à activer ou à désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="d04ad-113">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="d04ad-114">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-114">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="d04ad-115">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de détection d’hameçonnage dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="d04ad-115">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="d04ad-116">Lorsque vous créez une stratégie anti-hameçonnage, vous créez en réalité une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="d04ad-116">When you create an anti-phishing policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="d04ad-117">Lorsque vous modifiez une stratégie anti-hameçonnage, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-117">When you modify an anti-phishing policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="d04ad-118">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-118">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="d04ad-119">Lorsque vous supprimez une stratégie anti-hameçonnage, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="d04ad-119">When you remove an anti-phishing policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="d04ad-120">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="d04ad-120">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="d04ad-121">Pour plus d’informations, consultez la section [utiliser Exchange Online PowerShell pour configurer les stratégies anti-hameçonnage](#use-exchange-online-powershell-to-configure-anti-phishing-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d04ad-121">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies](#use-exchange-online-powershell-to-configure-anti-phishing-policies) section later in this article.</span></span>

<span data-ttu-id="d04ad-122">Chaque organisation dispose d’une stratégie anti-hameçonnage intégrée nommée Office antiphishing par défaut, qui comporte les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-122">Every organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="d04ad-123">La stratégie est appliquée à tous les destinataires de l’organisation, même s’il n’y a aucune règle anti-hameçonnage (filtres de destinataire) associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-123">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="d04ad-124">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="d04ad-124">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="d04ad-125">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-125">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="d04ad-126">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-126">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="d04ad-127">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d04ad-127">To increase the effectiveness of anti-phishing protection, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d04ad-128">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d04ad-128">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d04ad-129">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="d04ad-129">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="d04ad-130">Pour accéder directement à la page **anti-hameçonnage** , utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="d04ad-130">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="d04ad-131">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="d04ad-131">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

  <span data-ttu-id="d04ad-132">Vous ne pouvez pas gérer les stratégies de détection d’hameçonnage dans une version autonome d’EOP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d04ad-132">You can't manage anti-phishing policies in standalone EOP PowerShell.</span></span>

- <span data-ttu-id="d04ad-133">Avant de pouvoir effectuer les procédures décrites dans cet article, vous devez disposer des autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-133">You need to be assigned permissions before you can do the procedures in this article:</span></span>

  - <span data-ttu-id="d04ad-134">Pour ajouter, modifier et supprimer des stratégies de détection d’hameçonnage, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="d04ad-134">To add, modify, and delete anti-phishing policies, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="d04ad-135">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-135">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="d04ad-136">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="d04ad-136">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="d04ad-137">Pour un accès en lecture seule aux stratégies de détection d’hameçonnage, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="d04ad-137">For read-only access to anti-phishing policies, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="d04ad-138">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-138">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="d04ad-139">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="d04ad-139">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="d04ad-140">Pour créer et modifier des stratégies de détection d’hameçonnage dans un EOP autonome, vous devez effectuer une opération qui nécessite l' _hydratation_ de votre client.</span><span class="sxs-lookup"><span data-stu-id="d04ad-140">To create and modify anti-phishing policies in standalone EOP, you need to do something that requires _hydration_ for your tenant.</span></span> <span data-ttu-id="d04ad-141">Par exemple, dans le centre d’administration Exchange, vous pouvez accéder à l’onglet **autorisations** , sélectionner un groupe de rôles existant, cliquer sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) , puis supprimer un rôle (ce que vous devrez finalement rajouter).</span><span class="sxs-lookup"><span data-stu-id="d04ad-141">For example, in the Exchange admin center (EAC), you can go to the **Permissions** tab, select an existing role group, click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and remove a role (which you'll ultimately add back).</span></span> <span data-ttu-id="d04ad-142">Si votre locataire n’a jamais été hydraté, vous obtenez une boîte de dialogue intitulée **mettre à jour les paramètres d’organisation** avec une barre de progression qui doit se terminer avec succès.</span><span class="sxs-lookup"><span data-stu-id="d04ad-142">If your tenant has never been hydrated, you get a dialog named **Update Organization Settings** with a progress bar that should complete successfully.</span></span> <span data-ttu-id="d04ad-143">Pour plus d’informations sur la mise en attente, reportez-vous à la cmdlet [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) (qui n’est pas disponible dans la version autonome d’EOP PowerShell ou dans le centre de conformité & Security).</span><span class="sxs-lookup"><span data-stu-id="d04ad-143">For more information about hydration, see the [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) cmdlet (which isn't available in standalone EOP PowerShell or in the Security & Compliance Center).</span></span>

- <span data-ttu-id="d04ad-144">Pour connaître les paramètres recommandés pour les stratégies de détection d’hameçonnage, consultez les paramètres de la [stratégie anti-hameçonnage par défaut EOP](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="d04ad-144">For our recommended settings for anti-phishing policies, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="d04ad-145">Autorisez jusqu’à 30 minutes pour l’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d04ad-145">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="d04ad-146">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, consultez la rubrique [Order and Precedence of e-mail protection](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-146">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-anti-phishing-policies"></a><span data-ttu-id="d04ad-147">Utiliser le centre de sécurité & conformité pour créer des stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-147">Use the Security & Compliance Center to create anti-phishing policies</span></span>

<span data-ttu-id="d04ad-148">La création d’une stratégie anti-hameçonnage personnalisée dans le centre de sécurité & conformité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="d04ad-148">Creating a custom anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="d04ad-149">Lorsque vous créez une stratégie anti-hameçonnage, vous pouvez uniquement spécifier le nom de la stratégie, sa description et le filtre de destinataire qui identifie la personne à laquelle la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="d04ad-149">When you create an anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="d04ad-150">Après avoir créé la stratégie, vous pouvez modifier la stratégie pour modifier ou consulter les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-150">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="d04ad-151">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection anti-hameçonnage**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d04ad-151">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-152">Sur la page **anti-hameçonnage** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-152">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="d04ad-153">L’Assistant **créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="d04ad-153">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="d04ad-154">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d04ad-154">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="d04ad-155">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-155">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="d04ad-156">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-156">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="d04ad-157">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-157">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="d04ad-158">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-158">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="d04ad-159">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="d04ad-159">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="d04ad-160">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="d04ad-160">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="d04ad-161">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="d04ad-161">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="d04ad-162">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-162">Click **Add a condition**.</span></span> <span data-ttu-id="d04ad-163">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="d04ad-163">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="d04ad-164">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d04ad-164">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="d04ad-165">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d04ad-165">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="d04ad-166">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d04ad-166">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="d04ad-167">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="d04ad-167">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="d04ad-168">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="d04ad-168">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="d04ad-169">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="d04ad-169">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="d04ad-170">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="d04ad-170">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="d04ad-171">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="d04ad-171">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="d04ad-172">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="d04ad-172">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="d04ad-173">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-173">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="d04ad-174">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-174">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="d04ad-175">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="d04ad-175">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="d04ad-176">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-176">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="d04ad-177">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="d04ad-177">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="d04ad-178">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="d04ad-178">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="d04ad-179">Lorsque vous avez terminé, cliquez sur **créer cette stratégie**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-179">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="d04ad-180">Cliquez sur **OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d04ad-180">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="d04ad-181">Après avoir créé la stratégie anti-hameçonnage avec ces paramètres généraux de stratégie, suivez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-181">After you create the anti-phishing policy with these general policy settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-anti-phishing-policies"></a><span data-ttu-id="d04ad-182">Utiliser le centre de sécurité & conformité pour modifier des stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-182">Use the Security & Compliance Center to modify anti-phishing policies</span></span>

<span data-ttu-id="d04ad-183">Utilisez les procédures suivantes pour modifier les stratégies de détection d’hameçonnage : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d04ad-183">Use the following procedures to modify anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="d04ad-184">Si vous ne l’avez pas encore fait, ouvrez le centre de sécurité & conformité, puis **accédez à** \> **Policy** \> **protection contre le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-184">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-185">Sélectionnez la stratégie anti-hameçonnage personnalisée que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="d04ad-185">Select the custom anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="d04ad-186">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d04ad-186">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="d04ad-187">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="d04ad-187">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="d04ad-188">Si vous cliquez sur **modifier** dans une section, vous pouvez accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="d04ad-188">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="d04ad-189">Les étapes suivantes sont présentées dans l’ordre dans lequel les sections apparaissent, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="d04ad-189">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="d04ad-190">Une fois que vous avez cliqué sur **modifier** dans une section, les paramètres disponibles sont présentés dans un format d’Assistant, mais vous pouvez sauter les pages dans n’importe quel ordre, et vous pouvez cliquer sur **Enregistrer** sur n’importe quelle page (ou sur **Annuler** ou **Fermer** l' ![ icône ](../../media/scc-remove-icon.png) pour revenir à la page \*\*modifier votre stratégie \<name\> \*\* (vous n’avez pas besoin de consulter la dernière page de l’Assistant pour enregistrer ou quitter</span><span class="sxs-lookup"><span data-stu-id="d04ad-190">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="d04ad-191">**Paramètre de stratégie**: cliquez sur **modifier** pour modifier les mêmes paramètres que ceux qui étaient disponibles lorsque vous avez [créé la stratégie](#use-the-security--compliance-center-to-create-anti-phishing-policies) dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="d04ad-191">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-anti-phishing-policies) in the previous section:</span></span>

   - <span data-ttu-id="d04ad-192">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d04ad-192">**Name**</span></span>
   - <span data-ttu-id="d04ad-193">**Description**</span><span class="sxs-lookup"><span data-stu-id="d04ad-193">**Description**</span></span>
   - <span data-ttu-id="d04ad-194">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="d04ad-194">**Applied to**</span></span>
   - <span data-ttu-id="d04ad-195">**Vérifiez vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="d04ad-195">**Review your settings**</span></span>

   <span data-ttu-id="d04ad-196">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="d04ad-196">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="d04ad-197">**Spoof**: cliquez sur **modifier** pour activer ou désactiver l’Assistant usurpation d’identité, activez ou désactivez l’identification de l’expéditeur non authentifié dans Outlook, puis configurez l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués.</span><span class="sxs-lookup"><span data-stu-id="d04ad-197">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="d04ad-198">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="d04ad-198">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="d04ad-199">Notez que ces mêmes paramètres sont également disponibles dans les stratégies anti-hameçonnage ATP.</span><span class="sxs-lookup"><span data-stu-id="d04ad-199">Note that these same settings are also available in ATP anti-phishing policies.</span></span>

   - <span data-ttu-id="d04ad-200">**Usurpation des paramètres de filtrage**: la valeur par défaut est **activée**, et nous vous recommandons de la laisser activée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-200">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="d04ad-201">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-201">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="d04ad-202">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in EOP](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-202">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="d04ad-203">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’identité si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="d04ad-203">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="d04ad-204">Pour obtenir des instructions, voir [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="d04ad-204">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="d04ad-205">**Activer la fonctionnalité d’expéditeur non authentifié**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-205">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="d04ad-206">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-206">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="d04ad-207">**Actions**: spécifiez l’action à effectuer sur les messages qui échouent à l’aide d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="d04ad-207">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="d04ad-208">**Si un message électronique est envoyé par un utilisateur qui n’est pas autorisé à usurper votre domaine**:</span><span class="sxs-lookup"><span data-stu-id="d04ad-208">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="d04ad-209">**Déplacer le message vers les dossiers de courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="d04ad-209">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="d04ad-210">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="d04ad-210">**Quarantine the message**</span></span>

   - <span data-ttu-id="d04ad-211">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="d04ad-211">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="d04ad-212">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-212">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="d04ad-213">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="d04ad-213">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="d04ad-214">**Activer la protection contre l’usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="d04ad-214">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="d04ad-215">**Activer la fonctionnalité d’expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="d04ad-215">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="d04ad-216">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="d04ad-216">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="d04ad-217">Sur la page \*\*modifier votre stratégie \<Name\> \*\* , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-217">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy"></a><span data-ttu-id="d04ad-218">Utiliser le centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="d04ad-218">Use the Security & Compliance Center to modify the default anti-phishing policy</span></span>

<span data-ttu-id="d04ad-219">La stratégie anti-hameçonnage par défaut est nommée Office antiphishing par défaut et n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="d04ad-219">The default anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="d04ad-220">Pour modifier la stratégie anti-hameçonnage par défaut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d04ad-220">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="d04ad-221">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection anti-hameçonnage**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d04ad-221">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-222">Sur la page **anti-hameçonnage** , cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-222">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="d04ad-223">La page **modifier votre stratégie d’anti-hameçonnage Office 365 par défaut** apparaît.</span><span class="sxs-lookup"><span data-stu-id="d04ad-223">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="d04ad-224">Les sections suivantes sont disponibles, qui contiennent les paramètres identiques lorsque vous [modifiez une stratégie personnalisée](#use-the-security--compliance-center-to-modify-anti-phishing-policies).</span><span class="sxs-lookup"><span data-stu-id="d04ad-224">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-anti-phishing-policies).</span></span>

   - <span data-ttu-id="d04ad-225">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="d04ad-225">**Impersonation**</span></span>
   - <span data-ttu-id="d04ad-226">**Tromp**</span><span class="sxs-lookup"><span data-stu-id="d04ad-226">**Spoof**</span></span>
   - <span data-ttu-id="d04ad-227">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="d04ad-227">**Advanced settings**</span></span>

   <span data-ttu-id="d04ad-228">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="d04ad-228">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="d04ad-229">Vous pouvez voir la section paramètres de **stratégie** et les valeurs, mais il n’existe aucun lien de **modification** , afin que vous ne puissiez pas modifier les paramètres (nom de stratégie, description et personnes auxquelles la stratégie s’applique (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="d04ad-229">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="d04ad-230">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-230">You can't delete the default policy.</span></span>
   - <span data-ttu-id="d04ad-231">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="d04ad-231">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="d04ad-232">Sur la page **modifier votre stratégie par défaut pour les antiphishing Office 365** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-232">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies"></a><span data-ttu-id="d04ad-233">Activer ou désactiver les stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="d04ad-233">Enable or disable custom anti-phishing policies</span></span>

1. <span data-ttu-id="d04ad-234">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection anti-hameçonnage**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d04ad-234">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-235">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="d04ad-235">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="d04ad-236">Faites glisser le bouton bascule sur **désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-236">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="d04ad-237">Faites glisser le bouton bascule sur **activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d04ad-237">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="d04ad-238">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-238">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies"></a><span data-ttu-id="d04ad-239">Définir la priorité des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="d04ad-239">Set the priority of custom anti-phishing policies</span></span>

<span data-ttu-id="d04ad-240">Par défaut, les stratégies de détection d’hameçonnage reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="d04ad-240">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="d04ad-241">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="d04ad-241">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="d04ad-242">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-242">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="d04ad-243">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="d04ad-243">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="d04ad-244">Les stratégies anti-hameçonnage personnalisées sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="d04ad-244">Custom anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="d04ad-245">La stratégie anti-hameçonnage par défaut nommée Office antiphishing par défaut a une valeur de priorité personnalisée la **plus faible**et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="d04ad-245">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="d04ad-246">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie anti-hameçonnage une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-246">**Note**: In the Security & Compliance Center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="d04ad-247">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle anti-hameçonnage (qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="d04ad-247">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="d04ad-248">Pour modifier la priorité d’une stratégie, cliquez sur **augmenter la priorité** ou sur **diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de **priorité** dans le centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="d04ad-248">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="d04ad-249">La modification de la priorité d’une stratégie n’a de sens que si vous disposez de plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="d04ad-249">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="d04ad-250">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-250">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-251">Sélectionnez la stratégie que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="d04ad-251">Select the policy that you want to modify.</span></span> <span data-ttu-id="d04ad-252">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d04ad-252">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="d04ad-253">Le menu volant **modifier \<name\> votre stratégie** apparaît.</span><span class="sxs-lookup"><span data-stu-id="d04ad-253">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="d04ad-254">La stratégie anti-hameçonnage personnalisée avec la valeur **Priority** de priorité **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="d04ad-254">The custom anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="d04ad-255">La stratégie anti-hameçonnage personnalisée avec la valeur de **priorité** la plus faible (par exemple, **3**) a uniquement le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="d04ad-255">The custom anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="d04ad-256">Si vous avez au moins trois stratégies anti-hameçonnage personnalisées, les stratégies de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="d04ad-256">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="d04ad-257">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="d04ad-257">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="d04ad-258">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-258">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-anti-phishing-policies"></a><span data-ttu-id="d04ad-259">Utiliser le centre de sécurité & conformité pour afficher les stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-259">Use the Security & Compliance Center to view anti-phishing policies</span></span>

1. <span data-ttu-id="d04ad-260">Dans le centre de sécurité & conformité, puis accédez **à** \> **Policy** \> **protection contre le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-260">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-261">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-261">Do one of the following steps:</span></span>

   - <span data-ttu-id="d04ad-262">Sélectionnez une stratégie anti-hameçonnage personnalisée que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="d04ad-262">Select a custom anti-phishing policy that you want to view.</span></span> <span data-ttu-id="d04ad-263">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d04ad-263">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="d04ad-264">Cliquez sur **stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-264">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="d04ad-265">Le menu volant **modifier \<name\> votre stratégie** apparaît, dans lequel vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d04ad-265">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-anti-phishing-policies"></a><span data-ttu-id="d04ad-266">Utiliser le centre de sécurité & conformité pour supprimer les stratégies de protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-266">Use the Security & Compliance Center to remove anti-phishing policies</span></span>

1. <span data-ttu-id="d04ad-267">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection anti-hameçonnage**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d04ad-267">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="d04ad-268">Sélectionnez la stratégie que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="d04ad-268">Select the policy that you want to remove.</span></span> <span data-ttu-id="d04ad-269">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d04ad-269">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="d04ad-270">Dans le menu volant **modifier \<name\> votre stratégie** qui s’affiche, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d04ad-270">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="d04ad-271">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d04ad-271">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies"></a><span data-ttu-id="d04ad-272">Utiliser Exchange Online PowerShell pour configurer les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-272">Use Exchange Online PowerShell to configure anti-phishing policies</span></span>

<span data-ttu-id="d04ad-273">Comme décrit précédemment, une stratégie anti-hameçonnage se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-273">As previously described, an anti-phishing policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="d04ad-274">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est apparente.</span><span class="sxs-lookup"><span data-stu-id="d04ad-274">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="d04ad-275">Vous pouvez gérer les stratégies anti-hameçonnage à l’aide des cmdlets \*\* \* -antiphishpolicy permet\*\* et gérer les règles anti-hameçonnage à l’aide des cmdlets \*\* \* -antiphishrule permet\*\* .</span><span class="sxs-lookup"><span data-stu-id="d04ad-275">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="d04ad-276">Dans PowerShell, vous devez d’abord créer la stratégie anti-hameçonnage, puis créer la règle anti-hameçonnage qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="d04ad-276">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="d04ad-277">Dans PowerShell, vous modifiez les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage séparément.</span><span class="sxs-lookup"><span data-stu-id="d04ad-277">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="d04ad-278">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="d04ad-278">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

> [!NOTE]
> <span data-ttu-id="d04ad-279">Les procédures PowerShell suivantes ne sont pas disponibles dans les organisations EOP autonomes utilisant Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d04ad-279">The following PowerShell procedures aren't available in standalone EOP organizations using Exchange Online Protection PowerShell.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="d04ad-280">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-280">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="d04ad-281">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-281">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="d04ad-282">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-282">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="d04ad-283">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="d04ad-283">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="d04ad-284">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="d04ad-284">**Notes**:</span></span>

- <span data-ttu-id="d04ad-285">Vous pouvez créer une nouvelle règle anti-hameçonnage et lui affecter une stratégie anti-hameçonnage existante non associée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-285">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="d04ad-286">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-286">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="d04ad-287">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage de PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="d04ad-287">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="d04ad-288">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="d04ad-288">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="d04ad-289">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="d04ad-289">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="d04ad-290">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’avez pas affecté la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-290">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="d04ad-291">Étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-291">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="d04ad-292">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-292">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-EnableAntiSpoofEnforcement <$true | $false>] [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableUnauthenticatedSender <$true | $false>]
```

<span data-ttu-id="d04ad-293">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d04ad-293">This example creates an anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="d04ad-294">Description : stratégie de service de recherche.</span><span class="sxs-lookup"><span data-stu-id="d04ad-294">The description is: Research department policy.</span></span>
- <span data-ttu-id="d04ad-295">Remplace l’action par défaut pour l’usurpation en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d04ad-295">Changes the default action for spoofing to Quarantine.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="d04ad-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="d04ad-296">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="d04ad-297">Étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-297">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="d04ad-298">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-298">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="d04ad-299">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-299">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="d04ad-300">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="d04ad-300">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="d04ad-301">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="d04ad-301">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="d04ad-302">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-302">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="d04ad-303">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="d04ad-303">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="d04ad-304">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-304">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="d04ad-305">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-305">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="d04ad-306">Cet exemple renvoie la liste récapitulative de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d04ad-306">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="d04ad-307">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="d04ad-307">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="d04ad-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="d04ad-308">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="d04ad-309">Utiliser PowerShell pour afficher les règles de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-309">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="d04ad-310">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-310">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="d04ad-311">Cet exemple renvoie la liste récapitulative de toutes les règles anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d04ad-311">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="d04ad-312">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-312">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="d04ad-313">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="d04ad-313">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="d04ad-314">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="d04ad-314">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="d04ad-315">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-315">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="d04ad-316">À l’exception des éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell comme lors de la création d’une stratégie, comme décrit dans l' [étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d04ad-316">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create a policy as described in [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) earlier in this article.</span></span>

- <span data-ttu-id="d04ad-317">Le commutateur _MakeDefault_ qui désactive la stratégie spécifiée dans la stratégie par défaut (appliquée à tout le monde, toujours à la priorité la **plus basse** et vous ne pouvez pas le supprimer) n’est disponible que lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d04ad-317">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="d04ad-318">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (l’applet de commande **Set-antiphishpolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="d04ad-318">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="d04ad-319">Lorsque vous renommez une stratégie anti-hameçonnage dans le centre de sécurité & conformité, vous renommez uniquement la _règle_anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d04ad-319">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="d04ad-320">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-320">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="d04ad-321">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="d04ad-321">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="d04ad-322">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-322">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="d04ad-323">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-323">The only setting that's not available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="d04ad-324">Pour activer ou désactiver les règles anti-hameçonnage existantes, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="d04ad-324">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="d04ad-325">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) , plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d04ad-325">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="d04ad-326">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-326">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="d04ad-327">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="d04ad-327">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="d04ad-328">Utiliser PowerShell pour activer ou désactiver les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-328">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="d04ad-329">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive la totalité de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="d04ad-329">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="d04ad-330">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="d04ad-330">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="d04ad-331">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-331">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="d04ad-332">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="d04ad-332">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="d04ad-333">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="d04ad-333">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="d04ad-334">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) et [Disable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="d04ad-334">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="d04ad-335">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-335">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="d04ad-336">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="d04ad-336">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="d04ad-337">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="d04ad-337">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="d04ad-338">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="d04ad-338">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="d04ad-339">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="d04ad-339">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="d04ad-340">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="d04ad-340">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="d04ad-341">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-341">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="d04ad-p136">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="d04ad-p136">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="d04ad-344">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="d04ad-344">**Notes**:</span></span>

- <span data-ttu-id="d04ad-345">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="d04ad-345">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="d04ad-346">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante, elle a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="d04ad-346">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="d04ad-347">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-347">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="d04ad-348">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-348">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="d04ad-349">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-349">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="d04ad-350">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="d04ad-350">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="d04ad-351">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="d04ad-351">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="d04ad-352">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d04ad-352">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="d04ad-353">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="d04ad-353">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="d04ad-354">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d04ad-354">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="d04ad-355">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="d04ad-355">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="d04ad-356">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="d04ad-356">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="d04ad-357">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="d04ad-357">How do you know these procedures worked?</span></span>

<span data-ttu-id="d04ad-358">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage ATP, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-358">To verify that you've successfully configured ATP anti-phishing policies, do any of the following steps:</span></span>

- <span data-ttu-id="d04ad-359">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection anti-hameçonnage**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d04ad-359">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span> <span data-ttu-id="d04ad-360">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="d04ad-360">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="d04ad-361">Pour afficher plus de détails, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d04ad-361">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="d04ad-362">Sélectionnez la stratégie dans la liste, puis affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="d04ad-362">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="d04ad-363">Cliquez sur **stratégie par défaut** et affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="d04ad-363">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="d04ad-364">Dans Exchange Online PowerShell, remplacez \<Name\> par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="d04ad-364">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
