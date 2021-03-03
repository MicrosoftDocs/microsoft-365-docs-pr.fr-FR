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
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage disponibles dans les organisations Exchange Online Protection (EOP) avec ou sans boîtes aux lettres Exchange Online.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 612c7153f89a404cac736a9a46e8ca5f69e46f65
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50406219"
---
# <a name="configure-anti-phishing-policies-in-eop"></a><span data-ttu-id="0e336-103">Configurer des stratégies anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="0e336-103">Configure anti-phishing policies in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="0e336-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0e336-104">**Applies to**</span></span>
- [<span data-ttu-id="0e336-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0e336-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="0e336-106">Dans les organisations Microsoft 365 avec boîtes aux lettres dans Exchange Online ou les organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, il existe une stratégie anti-hameçonnage par défaut qui contient un nombre limité de fonctionnalités de protection contre l’usurpation d’adresses qui sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-106">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there's a default anti-phishing policy that contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="0e336-107">Pour plus d’informations, voir Paramètres d’usurpation [d’informations dans les stratégies anti-hameçonnage.](set-up-anti-phishing-policies.md#spoof-settings)</span><span class="sxs-lookup"><span data-stu-id="0e336-107">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="0e336-108">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-108">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="0e336-109">Pour plus de granularité, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0e336-109">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="0e336-110">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0e336-110">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="0e336-111">Les organisations ayant des boîtes aux lettres Exchange Online peuvent configurer des stratégies anti-hameçonnage dans le Centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e336-111">Organizations with Exchange Online mailboxes can configure anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span> <span data-ttu-id="0e336-112">Les organisations EOP autonomes peuvent uniquement utiliser le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="0e336-112">Standalone EOP organizations can only use the Security & Compliance Center.</span></span>

<span data-ttu-id="0e336-113">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées dans Microsoft Defender pour Office 365 qui sont disponibles dans Defender pour Office 365, voir Configurer des stratégies anti-hameçonnage dans Microsoft Defender pour [Office 365.](configure-atp-anti-phishing-policies.md)</span><span class="sxs-lookup"><span data-stu-id="0e336-113">For information about creating and modifying the more advanced anti-phishing policies in Microsoft Defender for Office 365 that are available in Defender for Office 365, see [Configure anti-phishing policies in Microsoft Defender for Office 365](configure-atp-anti-phishing-policies.md).</span></span>

<span data-ttu-id="0e336-114">Les éléments de base d’une stratégie anti-hameçonnage sont :</span><span class="sxs-lookup"><span data-stu-id="0e336-114">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="0e336-115">**La stratégie anti-hameçonnage :** spécifie les protections de hameçonnage à activer ou désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="0e336-115">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="0e336-116">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-116">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="0e336-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies anti-hameçonnage dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="0e336-117">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="0e336-118">Lorsque vous créez une stratégie anti-hameçonnage, vous créez en fait une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="0e336-118">When you create an anti-phishing policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="0e336-119">Lorsque vous modifiez une stratégie anti-hameçonnage, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-119">When you modify an anti-phishing policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="0e336-120">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="0e336-120">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="0e336-121">Lorsque vous supprimez une stratégie anti-hameçonnage, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="0e336-121">When you remove an anti-phishing policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="0e336-122">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="0e336-122">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="0e336-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell pour configurer des stratégies [anti-hameçonnage](#use-exchange-online-powershell-to-configure-anti-phishing-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0e336-123">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies](#use-exchange-online-powershell-to-configure-anti-phishing-policies) section later in this article.</span></span>

<span data-ttu-id="0e336-124">Chaque organisation dispose d’une stratégie anti-hameçonnage intégrée nommée Office365 AntiPhish Default qui possède les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="0e336-124">Every organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="0e336-125">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle anti-hameçonnage (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-125">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="0e336-126">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="0e336-126">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="0e336-127">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="0e336-127">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="0e336-128">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-128">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="0e336-129">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts qui sont appliqués à des utilisateurs ou des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0e336-129">To increase the effectiveness of anti-phishing protection, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0e336-130">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0e336-130">What do you need to know before you begin?</span></span>

- <span data-ttu-id="0e336-131">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="0e336-131">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="0e336-132">Pour aller directement à la page **anti-hameçonnage,** utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="0e336-132">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="0e336-133">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0e336-133">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

  <span data-ttu-id="0e336-134">Vous ne pouvez pas gérer les stratégies anti-hameçonnage dans EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="0e336-134">You can't manage anti-phishing policies in standalone EOP PowerShell.</span></span>

- <span data-ttu-id="0e336-135">Des autorisations doivent vous être attribuées dans **Exchange Online** avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="0e336-135">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="0e336-136">Pour ajouter, modifier et supprimer des stratégies anti-hameçonnage,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="0e336-136">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="0e336-137">Pour accéder en lecture seule aux stratégies anti-hameçonnage,  vous  devez être membre des groupes de rôles Lecteur global ou Lecteur de <sup>\*</sup> sécurité.</span><span class="sxs-lookup"><span data-stu-id="0e336-137">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups<sup>\*</sup>.</span></span>

  <span data-ttu-id="0e336-138">Pour plus d'informations, voir [Permissions en échange en ligne](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="0e336-138">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="0e336-139">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="0e336-139">**Notes**:</span></span>

  - <span data-ttu-id="0e336-140">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux _utilisateurs_ les autorisations et autorisations requises pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0e336-140">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="0e336-141">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0e336-141">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="0e336-142">Le **groupe de rôles** Gestion de l’organisation en affichage seul dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la <sup>\*</sup> fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0e336-142">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>
  - <span data-ttu-id="0e336-143"><sup>\*</sup> Dans le Centre de sécurité & conformité, l’accès en lecture seule permet aux utilisateurs d’afficher les paramètres des stratégies anti-hameçonnage personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0e336-143"><sup>\*</sup> In the Security & Compliance Center, read-only access allows users to view the settings of custom anti-phishing policies.</span></span> <span data-ttu-id="0e336-144">Les utilisateurs en lecture seule ne peuvent pas voir les paramètres dans la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-144">Read-only users can't see the settings in the default anti-phishing policy.</span></span>

- <span data-ttu-id="0e336-145">Pour créer et modifier des stratégies anti-hameçonnage dans EOP autonome, vous devez faire une opération nécessitant une _hydration_ pour votre client.</span><span class="sxs-lookup"><span data-stu-id="0e336-145">To create and modify anti-phishing policies in standalone EOP, you need to do something that requires _hydration_ for your tenant.</span></span> <span data-ttu-id="0e336-146">Par exemple, dans le Centre d’administration Exchange (EAC), vous pouvez passer à  l’onglet **Autorisations,** sélectionner un groupe de rôles existant, cliquer sur Modifier l’icône Modifier et supprimer un rôle (que vous ajouterez finalement ![ ](../../media/ITPro-EAC-EditIcon.png) à nouveau).</span><span class="sxs-lookup"><span data-stu-id="0e336-146">For example, in the Exchange admin center (EAC), you can go to the **Permissions** tab, select an existing role group, click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and remove a role (which you'll ultimately add back).</span></span> <span data-ttu-id="0e336-147">Si votre client n’a jamais été retenté, vous obtenez une boîte de dialogue nommée Mettre à jour les **paramètres** de l’organisation avec une barre de progression qui doit se terminer correctement.</span><span class="sxs-lookup"><span data-stu-id="0e336-147">If your tenant has never been hydrated, you get a dialog named **Update Organization Settings** with a progress bar that should complete successfully.</span></span> <span data-ttu-id="0e336-148">Pour plus d’informations sur l’hydration, voir la cmdlet [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) (qui n’est pas disponible dans EOP PowerShell autonome ou dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="0e336-148">For more information about hydration, see the [Enable-OrganizationCustomization](https://docs.microsoft.com/powershell/module/exchange/enable-organizationcustomization) cmdlet (which isn't available in standalone EOP PowerShell or in the Security & Compliance Center).</span></span>

- <span data-ttu-id="0e336-149">Pour obtenir nos paramètres recommandés pour les stratégies anti-hameçonnage, consultez les paramètres de stratégie [anti-hameçonnage par défaut d’EOP.](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="0e336-149">For our recommended settings for anti-phishing policies, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="0e336-150">Autorisez jusqu’à 30 minutes d’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0e336-150">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="0e336-151">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, voir Ordre et priorité de la [protection du courrier électronique.](how-policies-and-protections-are-combined.md)</span><span class="sxs-lookup"><span data-stu-id="0e336-151">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-anti-phishing-policies"></a><span data-ttu-id="0e336-152">Utiliser le Centre de sécurité & conformité pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-152">Use the Security & Compliance Center to create anti-phishing policies</span></span>

<span data-ttu-id="0e336-153">La création d’une stratégie anti-hameçonnage personnalisée dans le Centre de sécurité & conformité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="0e336-153">Creating a custom anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="0e336-154">Lorsque vous créez une stratégie anti-hameçonnage, vous ne pouvez spécifier que le nom de la stratégie, la description et le filtre de destinataires qui identifient à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-154">When you create an anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="0e336-155">Après avoir créé la stratégie, vous pouvez la modifier pour modifier ou passer en revue les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-155">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="0e336-156">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-156">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-157">Dans la page **Anti-hameçonnage,** cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="0e336-157">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="0e336-158">**L’Assistant Créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0e336-158">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="0e336-159">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e336-159">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="0e336-160">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-160">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="0e336-161">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-161">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="0e336-162">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0e336-162">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="0e336-163">Dans la page **Appliqué à** qui s’affiche, identifiez les destinataires internes à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-163">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="0e336-164">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="0e336-164">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="0e336-165">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="0e336-165">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="0e336-166">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="0e336-166">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="0e336-167">Cliquez **sur Ajouter une condition.**</span><span class="sxs-lookup"><span data-stu-id="0e336-167">Click **Add a condition**.</span></span> <span data-ttu-id="0e336-168">Dans ladown qui s’affiche, sélectionnez une condition sous **Applied si**:</span><span class="sxs-lookup"><span data-stu-id="0e336-168">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="0e336-169">**Le destinataire est**: Spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0e336-169">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="0e336-170">**Le destinataire est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0e336-170">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="0e336-171">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0e336-171">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="0e336-172">Une fois que vous avez sélectionné la condition, une zone « Tout » apparaît dans la zone « **Tout le** monde ».</span><span class="sxs-lookup"><span data-stu-id="0e336-172">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="0e336-173">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="0e336-173">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="0e336-174">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="0e336-174">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="0e336-175">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="0e336-175">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="0e336-176">Pour supprimer des entrées individuelles, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="0e336-176">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="0e336-177">Pour supprimer la condition entière, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la condition.</span><span class="sxs-lookup"><span data-stu-id="0e336-177">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="0e336-178">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous Appliqué **si**.</span><span class="sxs-lookup"><span data-stu-id="0e336-178">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="0e336-179">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous Sauf **si**.</span><span class="sxs-lookup"><span data-stu-id="0e336-179">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="0e336-180">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="0e336-180">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="0e336-181">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0e336-181">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="0e336-182">Dans la page **Examiner vos paramètres** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="0e336-182">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="0e336-183">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="0e336-183">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="0e336-184">Lorsque vous avez terminé, cliquez sur **Créer cette stratégie.**</span><span class="sxs-lookup"><span data-stu-id="0e336-184">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="0e336-185">Cliquez **sur OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0e336-185">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="0e336-186">Après avoir créé la stratégie anti-hameçonnage avec ces paramètres de stratégie générale, utilisez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-186">After you create the anti-phishing policy with these general policy settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-anti-phishing-policies"></a><span data-ttu-id="0e336-187">Utiliser le Centre de sécurité & conformité pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-187">Use the Security & Compliance Center to modify anti-phishing policies</span></span>

<span data-ttu-id="0e336-188">Utilisez les procédures suivantes pour modifier les stratégies anti-hameçonnage : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0e336-188">Use the following procedures to modify anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="0e336-189">Si vous n’y êtes pas déjà, ouvrez le Centre  de sécurité & conformité et allez à l’anti-hameçonnage de la stratégie de gestion \>  \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="0e336-189">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-190">Sélectionnez la stratégie anti-hameçonnage personnalisée à modifier.</span><span class="sxs-lookup"><span data-stu-id="0e336-190">Select the custom anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="0e336-191">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0e336-191">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="0e336-192">Le **volant \<name\> Modifier votre** stratégie s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0e336-192">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="0e336-193">Cliquer sur **Modifier** dans n’importe quelle section vous permet d’accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="0e336-193">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="0e336-194">Les étapes suivantes sont présentées dans l’ordre d’apparition des sections, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="0e336-194">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="0e336-195">Une fois  que vous avez cliqué sur Modifier dans une section, les paramètres disponibles sont présentés dans un  format  d’Assistant, mais vous pouvez passer dans les pages dans n’importe quel ordre et vous pouvez cliquer sur Enregistrer sur n’importe quelle page (ou  ![ ](../../media/scc-remove-icon.png) **\<name\>** sur l’icône Annuler ou Fermer pour revenir à la page Modifier votre stratégie (vous n’êtes pas obligé de visiter la dernière page de l’Assistant pour enregistrer ou quitter).</span><span class="sxs-lookup"><span data-stu-id="0e336-195">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="0e336-196">**Paramètre de stratégie**: cliquez **sur Modifier** pour modifier les paramètres qui étaient disponibles lorsque vous [avez](#use-the-security--compliance-center-to-create-anti-phishing-policies) créé la stratégie dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="0e336-196">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-anti-phishing-policies) in the previous section:</span></span>

   - <span data-ttu-id="0e336-197">**Name**</span><span class="sxs-lookup"><span data-stu-id="0e336-197">**Name**</span></span>
   - <span data-ttu-id="0e336-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e336-198">**Description**</span></span>
   - <span data-ttu-id="0e336-199">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="0e336-199">**Applied to**</span></span>
   - <span data-ttu-id="0e336-200">**Passer en revue vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="0e336-200">**Review your settings**</span></span>

   <span data-ttu-id="0e336-201">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="0e336-201">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="0e336-202">Usurpation d’identité : cliquez sur Modifier pour activer ou désactiver la veille contre l’usurpation d’identité, activer ou désactiver l’identification des expéditeurs non authentifiés dans Outlook et configurer l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués. </span><span class="sxs-lookup"><span data-stu-id="0e336-202">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="0e336-203">Pour plus d’informations, voir Paramètres d’usurpation [d’informations dans les stratégies anti-hameçonnage.](set-up-anti-phishing-policies.md#spoof-settings)</span><span class="sxs-lookup"><span data-stu-id="0e336-203">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="0e336-204">Notez que ces mêmes paramètres sont également disponibles dans les stratégies anti-hameçonnage dans Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="0e336-204">Note that these same settings are also available in anti-phishing policies in Defender for Office 365.</span></span>

   - <span data-ttu-id="0e336-205">**Paramètres de filtre** d’usurpation d’usurpation : la valeur par défaut est **Sur** et nous vous recommandons de la laisser.</span><span class="sxs-lookup"><span data-stu-id="0e336-205">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="0e336-206">Pour le désactiver, faites glisser le curseur sur **Désactiver.**</span><span class="sxs-lookup"><span data-stu-id="0e336-206">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="0e336-207">Pour plus d’informations, voir [Configurer la veille contre l’usurpation d’adresse dans EOP.](learn-about-spoof-intelligence.md)</span><span class="sxs-lookup"><span data-stu-id="0e336-207">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="0e336-208">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’usurpation si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez plutôt le filtrage amélioré pour les connecteurs.</span><span class="sxs-lookup"><span data-stu-id="0e336-208">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="0e336-209">Pour obtenir des instructions, voir [Filtrage amélioré pour les connecteurs dans Exchange Online.](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors)</span><span class="sxs-lookup"><span data-stu-id="0e336-209">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="0e336-210">**Activer la fonctionnalité Expéditeur** non authentifié : la valeur par défaut est **Activé.**</span><span class="sxs-lookup"><span data-stu-id="0e336-210">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="0e336-211">Pour le désactiver, faites glisser le curseur sur **Désactiver.**</span><span class="sxs-lookup"><span data-stu-id="0e336-211">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="0e336-212">**Actions**: spécifiez l’action à prendre sur les messages qui échouent à la veille contre l’usurpation d’informations :</span><span class="sxs-lookup"><span data-stu-id="0e336-212">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="0e336-213">**Si un e-mail est envoyé par une personne qui n’est** pas autorisée à usurper votre domaine :</span><span class="sxs-lookup"><span data-stu-id="0e336-213">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="0e336-214">**Déplacer le message vers les dossiers Courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="0e336-214">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="0e336-215">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="0e336-215">**Quarantine the message**</span></span>

   - <span data-ttu-id="0e336-216">**Consultez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="0e336-216">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="0e336-217">Vous pouvez cliquer **sur Modifier** dans chaque section pour revenir à la page concernée.</span><span class="sxs-lookup"><span data-stu-id="0e336-217">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="0e336-218">Vous pouvez basculer les paramètres  suivants **directement** sur cette page :</span><span class="sxs-lookup"><span data-stu-id="0e336-218">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="0e336-219">**Activer la protection contre l’usurpation d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="0e336-219">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="0e336-220">**Activer la fonctionnalité Expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="0e336-220">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="0e336-221">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="0e336-221">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="0e336-222">De retour sur la page **Modifier votre \<Name\> stratégie,** consultez vos paramètres, puis cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="0e336-222">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy"></a><span data-ttu-id="0e336-223">Utiliser le Centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="0e336-223">Use the Security & Compliance Center to modify the default anti-phishing policy</span></span>

<span data-ttu-id="0e336-224">La stratégie anti-hameçonnage par défaut est nommée Office365 AntiPhish Default et elle n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="0e336-224">The default anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="0e336-225">Pour modifier la stratégie anti-hameçonnage par défaut, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-225">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="0e336-226">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-226">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-227">Dans la page **Anti-hameçonnage,** cliquez sur **Stratégie par défaut.**</span><span class="sxs-lookup"><span data-stu-id="0e336-227">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="0e336-228">La page **Modifier votre stratégie Office 365 par** défaut s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0e336-228">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="0e336-229">Les sections suivantes sont disponibles, qui contiennent des paramètres identiques lorsque vous [modifiez une stratégie personnalisée.](#use-the-security--compliance-center-to-modify-anti-phishing-policies)</span><span class="sxs-lookup"><span data-stu-id="0e336-229">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-anti-phishing-policies).</span></span>

   - <span data-ttu-id="0e336-230">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="0e336-230">**Impersonation**</span></span>
   - <span data-ttu-id="0e336-231">**Usurpation d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="0e336-231">**Spoof**</span></span>
   - <span data-ttu-id="0e336-232">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="0e336-232">**Advanced settings**</span></span>

   <span data-ttu-id="0e336-233">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="0e336-233">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="0e336-234">Vous pouvez voir la **section** paramètres de  stratégie et les valeurs, mais il n’existe aucun lien Modifier, donc vous ne pouvez pas modifier les paramètres (nom de stratégie, description et à qui s’applique la stratégie (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="0e336-234">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="0e336-235">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-235">You can't delete the default policy.</span></span>
   - <span data-ttu-id="0e336-236">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="0e336-236">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="0e336-237">Dans la page **Modifier votre stratégie Par défaut, consultez** vos paramètres, puis cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="0e336-237">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies"></a><span data-ttu-id="0e336-238">Activer ou désactiver des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="0e336-238">Enable or disable custom anti-phishing policies</span></span>

1. <span data-ttu-id="0e336-239">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-239">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-240">Notez la valeur dans la **colonne État** :</span><span class="sxs-lookup"><span data-stu-id="0e336-240">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="0e336-241">Faites glisser le basculement vers **Désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-241">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="0e336-242">Faites glisser le curseur sur **Activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e336-242">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="0e336-243">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-243">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies"></a><span data-ttu-id="0e336-244">Définir la priorité des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="0e336-244">Set the priority of custom anti-phishing policies</span></span>

<span data-ttu-id="0e336-245">Par défaut, les stratégies anti-hameçonnage se voir donner une priorité basée sur l’ordre de leur création (les nouvelles stratégies sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="0e336-245">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="0e336-246">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="0e336-246">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="0e336-247">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="0e336-247">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="0e336-248">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="0e336-248">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="0e336-249">Les stratégies anti-hameçonnage personnalisées sont affichées dans l’ordre  de traitement (la première stratégie a la valeur Priorité 0).</span><span class="sxs-lookup"><span data-stu-id="0e336-249">Custom anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="0e336-250">La stratégie anti-hameçonnage par défaut nommée Office365 AntiPhish Default a la valeur de priorité personnalisée **La** plus faible et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="0e336-250">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="0e336-251">**Remarque**: dans le Centre de sécurité & conformité, vous ne pouvez modifier la priorité de la stratégie anti-hameçonnage qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="0e336-251">**Note**: In the Security & Compliance Center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="0e336-252">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle anti-hameçonnage (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="0e336-252">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="0e336-253">Pour modifier la priorité d’une stratégie, cliquez sur Augmenter la priorité ou Diminuer la  priorité dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de priorité dans le Centre de sécurité & conformité).  </span><span class="sxs-lookup"><span data-stu-id="0e336-253">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="0e336-254">La modification de la priorité d’une stratégie n’a de sens que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="0e336-254">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="0e336-255">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-255">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-256">Sélectionnez la stratégie à modifier.</span><span class="sxs-lookup"><span data-stu-id="0e336-256">Select the policy that you want to modify.</span></span> <span data-ttu-id="0e336-257">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0e336-257">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="0e336-258">Le **volant \<name\> Modifier votre** stratégie s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0e336-258">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="0e336-259">La stratégie anti-hameçonnage  personnalisée dont la valeur de priorité **est 0** ne dispose que **du** bouton Diminuer la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="0e336-259">The custom anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="0e336-260">La stratégie anti-hameçonnage personnalisée  dont la valeur de priorité est la plus faible (par exemple, **3**) ne dispose que du bouton **Augmenter** la priorité.</span><span class="sxs-lookup"><span data-stu-id="0e336-260">The custom anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="0e336-261">Si vous disposez de trois stratégies anti-hameçonnage personnalisées ou plus, les  stratégies entre les valeurs de priorité les plus élevées et les plus faibles disposent à la fois des boutons Augmenter la priorité et Diminuer la priorité. </span><span class="sxs-lookup"><span data-stu-id="0e336-261">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="0e336-262">Cliquez **sur Augmenter la priorité** ou Diminuer la **priorité** pour modifier la **valeur** Priorité.</span><span class="sxs-lookup"><span data-stu-id="0e336-262">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="0e336-263">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0e336-263">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-anti-phishing-policies"></a><span data-ttu-id="0e336-264">Utiliser le Centre de sécurité & conformité pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-264">Use the Security & Compliance Center to view anti-phishing policies</span></span>

1. <span data-ttu-id="0e336-265">Dans le Centre de sécurité & conformité, puis allez à  l’anti-hameçonnage de la stratégie de gestion \>  \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="0e336-265">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-266">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-266">Do one of the following steps:</span></span>

   - <span data-ttu-id="0e336-267">Sélectionnez une stratégie anti-hameçonnage personnalisée à afficher.</span><span class="sxs-lookup"><span data-stu-id="0e336-267">Select a custom anti-phishing policy that you want to view.</span></span> <span data-ttu-id="0e336-268">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0e336-268">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="0e336-269">Cliquez **sur Stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-269">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="0e336-270">Le **volant \<name\> Modifier votre stratégie** s’affiche, où vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0e336-270">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-anti-phishing-policies"></a><span data-ttu-id="0e336-271">Utiliser le Centre de sécurité & conformité pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-271">Use the Security & Compliance Center to remove anti-phishing policies</span></span>

1. <span data-ttu-id="0e336-272">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-272">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="0e336-273">Sélectionnez la stratégie à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0e336-273">Select the policy that you want to remove.</span></span> <span data-ttu-id="0e336-274">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0e336-274">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="0e336-275">Dans le **volant \<name\> Modifier votre stratégie** qui s’affiche, cliquez sur Supprimer la **stratégie,** puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0e336-275">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="0e336-276">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e336-276">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies"></a><span data-ttu-id="0e336-277">Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-277">Use Exchange Online PowerShell to configure anti-phishing policies</span></span>

<span data-ttu-id="0e336-278">Comme décrit précédemment, une stratégie anti-hameçonnage se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-278">As previously described, an anti-phishing policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="0e336-279">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est évidente.</span><span class="sxs-lookup"><span data-stu-id="0e336-279">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="0e336-280">Vous gérez les stratégies anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishPolicy** et vous gérez les règles anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="0e336-280">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="0e336-281">Dans PowerShell, vous créez d’abord la stratégie anti-hameçonnage, puis vous créez la règle anti-hameçonnage qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="0e336-281">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="0e336-282">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-282">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="0e336-283">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="0e336-283">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

> [!NOTE]
> <span data-ttu-id="0e336-284">Les procédures PowerShell suivantes ne sont pas disponibles dans les organisations EOP autonomes utilisant Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e336-284">The following PowerShell procedures aren't available in standalone EOP organizations using Exchange Online Protection PowerShell.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="0e336-285">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-285">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="0e336-286">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="0e336-286">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="0e336-287">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-287">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="0e336-288">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="0e336-288">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="0e336-289">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="0e336-289">**Notes**:</span></span>

- <span data-ttu-id="0e336-290">Vous pouvez créer une règle anti-hameçonnage et lui attribuer une stratégie anti-hameçonnage existante et non dissociée.</span><span class="sxs-lookup"><span data-stu-id="0e336-290">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="0e336-291">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-291">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="0e336-292">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage dans PowerShell qui ne sont pas disponibles dans le Centre de sécurité & conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="0e336-292">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="0e336-293">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="0e336-293">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="0e336-294">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="0e336-294">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="0e336-295">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le Centre de sécurité & conformité tant que vous n’avez pas attribué la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0e336-295">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="0e336-296">Étape 1 : Utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-296">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="0e336-297">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-297">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-EnableSpoofIntelligence <$true | $false>] [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableUnauthenticatedSender <$true | $false>]
```

<span data-ttu-id="0e336-298">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e336-298">This example creates an anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="0e336-299">La description est la suivante : stratégie du service de recherche.</span><span class="sxs-lookup"><span data-stu-id="0e336-299">The description is: Research department policy.</span></span>
- <span data-ttu-id="0e336-300">Modifie l’action par défaut pour l’usurpation en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0e336-300">Changes the default action for spoofing to Quarantine.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="0e336-301">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="0e336-301">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="0e336-302">Étape 2 : Utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-302">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="0e336-303">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-303">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="0e336-304">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-304">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="0e336-305">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="0e336-305">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="0e336-306">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="0e336-306">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="0e336-307">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e336-307">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="0e336-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="0e336-308">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="0e336-309">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-309">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="0e336-310">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-310">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="0e336-311">Cet exemple renvoie une liste récapitulatif de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0e336-311">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="0e336-312">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="0e336-312">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="0e336-313">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="0e336-313">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="0e336-314">Utiliser PowerShell pour afficher les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-314">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="0e336-315">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-315">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="0e336-316">Cet exemple renvoie une liste récapitulatif de toutes les règles anti-hameçonnage ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0e336-316">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="0e336-317">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-317">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="0e336-318">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="0e336-318">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="0e336-319">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="0e336-319">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="0e336-320">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-320">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="0e336-321">Outre les éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell que lorsque vous créez une stratégie comme décrit à l’étape 1 : Utiliser PowerShell pour créer une stratégie [anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0e336-321">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create a policy as described in [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) earlier in this article.</span></span>

- <span data-ttu-id="0e336-322">Le _commutateur MakeDefault_ qui transforme la stratégie spécifiée en  stratégie par défaut (appliquée à tout le monde, toujours la plus faible priorité et que vous ne pouvez pas supprimer) est disponible uniquement lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e336-322">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="0e336-323">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (la cmdlet **Set-AntiPhishPolicy** n’a pas de _paramètre Name)._</span><span class="sxs-lookup"><span data-stu-id="0e336-323">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="0e336-324">Lorsque vous renommez une stratégie anti-hameçonnage dans le Centre de sécurité & conformité, vous renommez uniquement la règle _anti-hameçonnage._</span><span class="sxs-lookup"><span data-stu-id="0e336-324">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="0e336-325">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-325">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="0e336-326">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="0e336-326">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="0e336-327">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-327">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="0e336-328">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e336-328">The only setting that's not available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="0e336-329">Pour activer ou désactiver des règles anti-hameçonnage existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="0e336-329">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="0e336-330">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser PowerShell pour créer une section de règle [anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0e336-330">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="0e336-331">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-331">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="0e336-332">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="0e336-332">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="0e336-333">Utiliser PowerShell pour activer ou désactiver des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-333">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="0e336-334">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive l’ensemble de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="0e336-334">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="0e336-335">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="0e336-335">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="0e336-336">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-336">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="0e336-337">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0e336-337">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="0e336-338">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="0e336-338">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="0e336-339">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) et [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="0e336-339">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="0e336-340">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-340">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="0e336-341">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="0e336-341">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="0e336-342">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="0e336-342">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="0e336-343">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="0e336-343">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="0e336-344">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="0e336-344">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="0e336-345">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="0e336-345">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="0e336-346">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-346">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="0e336-p138">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="0e336-p138">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="0e336-349">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="0e336-349">**Notes**:</span></span>

- <span data-ttu-id="0e336-350">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="0e336-350">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="0e336-351">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante et elle a toujours la valeur de priorité nonmodifiable La plus **faible**.</span><span class="sxs-lookup"><span data-stu-id="0e336-351">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="0e336-352">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-352">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="0e336-353">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="0e336-353">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="0e336-354">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-354">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="0e336-355">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0e336-355">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="0e336-356">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="0e336-356">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="0e336-357">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="0e336-357">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="0e336-358">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="0e336-358">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="0e336-359">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0e336-359">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="0e336-360">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0e336-360">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="0e336-361">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="0e336-361">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="0e336-362">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="0e336-362">How do you know these procedures worked?</span></span>

<span data-ttu-id="0e336-363">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, faites l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-363">To verify that you've successfully configured anti-phishing policies in Microsoft Defender for Office 365, do any of the following steps:</span></span>

- <span data-ttu-id="0e336-364">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="0e336-364">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span> <span data-ttu-id="0e336-365">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="0e336-365">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="0e336-366">Pour afficher plus de détails, vous pouvez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e336-366">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="0e336-367">Sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="0e336-367">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="0e336-368">Cliquez **sur Stratégie par** défaut et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="0e336-368">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="0e336-369">Dans Exchange Online PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante \<Name\> et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="0e336-369">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
