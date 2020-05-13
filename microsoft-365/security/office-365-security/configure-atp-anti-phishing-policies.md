---
title: Configurer des stratégies anti-hameçonnage ATP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage avancées disponibles dans les organisations avec Office 365 Advanced Threat Protection (Office 365 ATP).
ms.openlocfilehash: efecd830db7ed10210605e31aa0ded2599de1b72
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44208886"
---
# <a name="configure-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-103">Configurer des stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-103">Configure ATP anti-phishing policies</span></span>

<span data-ttu-id="2c18e-104">Les stratégies anti-hameçonnage ATP font partie de la [protection avancée contre les menaces d’Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-104">ATP anti-phishing policies are part of [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="2c18e-105">Les stratégies anti-hameçonnage ATP peuvent vous aider à protéger votre organisation contre les attaques de hameçonnage malveillant basées sur l’emprunt d’identité et d’autres types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-105">ATP anti-phishing policies can help protect your organization from malicious impersonation-based phishing attacks and other types of phishing attacks.</span></span> <span data-ttu-id="2c18e-106">Pour plus d’informations sur les différences entre les stratégies de détection d’hameçonnage dans les stratégies anti-hameçonnage Exchange Online Protection (EOP) et ATP, reportez-vous à la rubrique [protection anti-hameçonnage](anti-phishing-protection.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-106">For more information about the differences between anti-phishing policies in Exchange Online Protection (EOP) and ATP anti-phishing policies, see [Anti-phishing protection](anti-phishing-protection.md).</span></span>

<span data-ttu-id="2c18e-107">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut de l’ATP.</span><span class="sxs-lookup"><span data-stu-id="2c18e-107">Admins can view, edit, and configure (but not delete) the default ATP anti-phishing policy.</span></span> <span data-ttu-id="2c18e-108">Pour une granularité accrue, vous pouvez également créer des stratégies anti-hameçonnage personnalisées ATP qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2c18e-108">For greater granularity, you can also create custom ATP anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="2c18e-109">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2c18e-109">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="2c18e-110">Vous pouvez configurer des stratégies anti-hameçonnage ATP dans le centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c18e-110">You can configure ATP anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span>

<span data-ttu-id="2c18e-111">Pour plus d’informations sur la configuration des stratégies de blocage plus limitées disponibles dans les organisations Exchange Online Protection (autrement dit, les organisations Microsoft 365 sans Office 365 ATP), voir [configure anti-phishing Policies in EOP](configure-anti-phishing-policies-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-111">For information about configuring the more limited in anti-phishing policies that are available in Exchange Online Protection organizations (that is, Microsoft 365 organizations without Office 365 ATP), see [Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

## <a name="atp-anti-phishing-policies-in-the-security--compliance-center-vs-exchange-online-powershell"></a><span data-ttu-id="2c18e-112">Stratégies anti-hameçonnage ATP dans le centre de sécurité & Compliance Center vs Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c18e-112">ATP anti-phishing policies in the Security & Compliance Center vs Exchange Online PowerShell</span></span>

<span data-ttu-id="2c18e-113">Les éléments de base d’une stratégie anti-hameçonnage ATP sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2c18e-113">The basic elements of an ATP anti-phishing policy are:</span></span>

- <span data-ttu-id="2c18e-114">**Stratégie anti-hameçonnage**: spécifie les protections de hameçonnage à activer ou à désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="2c18e-114">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>

- <span data-ttu-id="2c18e-115">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-115">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="2c18e-116">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies anti-hameçonnage ATP dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="2c18e-116">The difference between these two elements isn't obvious when you manage ATP anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="2c18e-117">Lorsque vous créez une stratégie anti-hameçonnage ATP dans le centre de sécurité & conformité, vous créez en réalité une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en même temps pour les deux.</span><span class="sxs-lookup"><span data-stu-id="2c18e-117">When you create an ATP anti-phishing policy in the Security & Compliance Center, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

- <span data-ttu-id="2c18e-118">Lorsque vous modifiez une stratégie anti-hameçonnage ATP dans le centre de sécurité & conformité, les paramètres liés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-118">When you modify an ATP anti-phishing policy in the Security & Compliance Center, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="2c18e-119">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-119">All other settings modify the associated anti-phish policy.</span></span>

- <span data-ttu-id="2c18e-120">Lorsque vous supprimez une stratégie anti-hameçonnage ATP du centre de sécurité & conformité, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2c18e-120">When you remove an ATP anti-phishing policy from the Security & Compliance Center, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="2c18e-121">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est apparente.</span><span class="sxs-lookup"><span data-stu-id="2c18e-121">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="2c18e-122">Vous pouvez gérer les stratégies anti-hameçonnage à l’aide des cmdlets \*\* \* -antiphishpolicy permet\*\* et gérer les règles anti-hameçonnage à l’aide des cmdlets \*\* \* -antiphishrule permet\*\* .</span><span class="sxs-lookup"><span data-stu-id="2c18e-122">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="2c18e-123">Dans PowerShell, vous devez d’abord créer la stratégie anti-hameçonnage, puis créer la règle anti-hameçonnage qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="2c18e-123">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>

- <span data-ttu-id="2c18e-124">Dans PowerShell, vous modifiez les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage séparément.</span><span class="sxs-lookup"><span data-stu-id="2c18e-124">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>

- <span data-ttu-id="2c18e-125">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="2c18e-125">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

### <a name="default-atp-anti-phishing-policy"></a><span data-ttu-id="2c18e-126">Stratégie anti-hameçonnage par défaut ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-126">Default ATP anti-phishing policy</span></span>

<span data-ttu-id="2c18e-127">Chaque organisation ATP est dotée d’une stratégie anti-hameçonnage intégrée à la protection avancée contre les hameçons Office 365 avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-127">Every ATP organization has a built-in ATP anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="2c18e-128">La stratégie anti-hameçonnage nommée Office antiphishing par défaut est appliquée à tous les destinataires de l’organisation, même s’il n’y a aucune règle anti-hameçonnage (filtres de destinataires) associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-128">The anti-phish policy named Office365 AntiPhish Default is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>

- <span data-ttu-id="2c18e-129">La stratégie appelée Office antiphishing par défaut a une valeur de priorité personnalisée la **plus faible** que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="2c18e-129">The policy named Office365 AntiPhish Default has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="2c18e-130">Toutes les stratégies personnalisées que vous créez ont toujours une priorité plus élevée que la stratégie nommée Office antiphishing par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-130">Any custom policies that you create always have a higher priority than the policy named Office365 AntiPhish Default.</span></span>

- <span data-ttu-id="2c18e-131">La stratégie nommée Office antiphishing par défaut est la stratégie par défaut (la propriété **IsDefault** a la valeur `True` ) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-131">The policy named Office365 AntiPhish Default is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="2c18e-132">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées ATP avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2c18e-132">To increase the effectiveness of anti-phishing protection, you can create custom ATP anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="2c18e-133">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2c18e-133">What do you need to know before you begin?</span></span>

- <span data-ttu-id="2c18e-134">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="2c18e-134">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="2c18e-135">Pour accéder directement à la page **anti-hameçonnage ATP** , utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="2c18e-135">To go directly to the **ATP anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="2c18e-136">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="2c18e-136">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="2c18e-137">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="2c18e-137">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="2c18e-138">Pour ajouter, modifier et supprimer des stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-138">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="2c18e-139">Pour un accès en lecture seule aux stratégies de détection d’hameçonnage, vous devez être membre du groupe de rôles **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-139">For read-only access to anti-phishing policies, you need to be a member of the **Security Reader** role group.</span></span> <span data-ttu-id="2c18e-140">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-140">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="2c18e-141">Pour connaître les paramètres recommandés pour les stratégies anti-hameçonnage ATP, consultez la rubrique paramètres de la [stratégie anti-hameçonnage Office ATP](recommended-settings-for-eop-and-office365-atp.md#office-atp-anti-phishing-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="2c18e-141">For our recommended settings for ATP anti-phishing policies, see [Office ATP anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#office-atp-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="2c18e-142">Autoriser jusqu’à 30 minutes pour l’application d’une stratégie nouvelle ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2c18e-142">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="2c18e-143">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, consultez la rubrique [Order and Precedence of e-mail protection](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-143">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-144">Utiliser le centre de sécurité & conformité pour créer des stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-144">Use the Security & Compliance Center to create ATP anti-phishing policies</span></span>

<span data-ttu-id="2c18e-145">La création d’une stratégie anti-hameçonnage personnalisée ATP dans le centre de sécurité & Compliance Center crée simultanément la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="2c18e-145">Creating a custom ATP anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="2c18e-146">Lorsque vous créez une stratégie anti-hameçonnage ATP, vous pouvez uniquement spécifier le nom de la stratégie, sa description et le filtre de destinataire qui identifie la personne à laquelle la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="2c18e-146">When you create an ATP anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="2c18e-147">Après avoir créé la stratégie, vous pouvez modifier la stratégie pour modifier ou consulter les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-147">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="2c18e-148">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-148">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-149">Sur la page **anti-hameçonnage** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-149">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="2c18e-150">L’Assistant **créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="2c18e-150">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="2c18e-151">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c18e-151">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="2c18e-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="2c18e-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="2c18e-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="2c18e-155">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-155">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="2c18e-156">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="2c18e-156">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="2c18e-157">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<destinataire1\>_ ou _\<destinataire2\>_).</span><span class="sxs-lookup"><span data-stu-id="2c18e-157">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="2c18e-158">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<destinataire1\>_ et _\<membre du groupe 1\>_).</span><span class="sxs-lookup"><span data-stu-id="2c18e-158">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="2c18e-159">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-159">Click **Add a condition**.</span></span> <span data-ttu-id="2c18e-160">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-160">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="2c18e-161">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2c18e-161">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="2c18e-162">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2c18e-162">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="2c18e-163">**Le domaine du destinataire est**: spécifie des destinataires dans un ou plusieurs domaines acceptés configurés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2c18e-163">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in the organization.</span></span>

   <span data-ttu-id="2c18e-164">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="2c18e-164">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="2c18e-165">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2c18e-165">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="2c18e-166">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-166">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="2c18e-167">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="2c18e-167">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="2c18e-168">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-168">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="2c18e-169">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="2c18e-169">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="2c18e-170">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-170">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="2c18e-171">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-171">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="2c18e-172">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="2c18e-172">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="2c18e-173">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-173">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="2c18e-174">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="2c18e-174">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="2c18e-175">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="2c18e-175">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="2c18e-176">Lorsque vous avez terminé, cliquez sur **créer cette stratégie**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-176">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="2c18e-177">Cliquez sur **OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-177">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="2c18e-178">Après avoir créé la stratégie anti-hameçonnage ATP avec ces paramètres généraux de stratégie, suivez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-178">After you create the ATP anti-phishing policy with these general policy settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-179">Utiliser le centre de sécurité & conformité pour modifier les stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-179">Use the Security & Compliance Center to modify ATP anti-phishing policies</span></span>

<span data-ttu-id="2c18e-180">Utilisez les procédures suivantes pour modifier les stratégies anti-hameçonnage ATP : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2c18e-180">Use the following procedures to modify ATP anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="2c18e-181">Si vous ne l’avez pas encore fait, ouvrez le centre de sécurité & conformité, **Threat management** puis accédez à \> **Policy** \> **protection contre les menaces pour le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-181">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-182">Sélectionnez la stratégie anti-hameçonnage personnalisée ATP à modifier.</span><span class="sxs-lookup"><span data-stu-id="2c18e-182">Select the custom ATP anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="2c18e-183">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2c18e-183">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="2c18e-184">Le menu de **modification de votre \< nom \> de stratégie** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-184">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="2c18e-185">Si vous cliquez sur **modifier** dans une section, vous pouvez accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="2c18e-185">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="2c18e-186">Les étapes suivantes sont présentées dans l’ordre dans lequel les sections apparaissent, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="2c18e-186">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="2c18e-187">Une fois que vous avez cliqué sur **modifier** dans une section, les paramètres disponibles sont présentés dans un format d’Assistant, mais vous pouvez sauter les pages dans n’importe quel ordre, et vous pouvez cliquer sur **Enregistrer** sur n’importe quelle page (ou sur **Annuler** ou **Fermer** l' ![ icône ](../../media/scc-remove-icon.png) pour revenir à la page \*\*modifier le \< nom \> \*\* de la stratégie (vous n’avez pas besoin d’accéder à la dernière page de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="2c18e-187">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="2c18e-188">**Paramètre de stratégie**: cliquez sur **modifier** pour modifier les mêmes paramètres que ceux qui étaient disponibles lorsque vous avez [créé la stratégie](#use-the-security--compliance-center-to-create-atp-anti-phishing-policies) dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="2c18e-188">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-atp-anti-phishing-policies) in the previous section:</span></span>

   - <span data-ttu-id="2c18e-189">**Name**</span><span class="sxs-lookup"><span data-stu-id="2c18e-189">**Name**</span></span>
   - <span data-ttu-id="2c18e-190">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c18e-190">**Description**</span></span>
   - <span data-ttu-id="2c18e-191">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="2c18e-191">**Applied to**</span></span>
   - <span data-ttu-id="2c18e-192">**Vérifier vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="2c18e-192">**Review your settings**</span></span>

   <span data-ttu-id="2c18e-193">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="2c18e-193">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="2c18e-194">**Emprunt d’identité**: cliquez sur **modifier** pour modifier les expéditeurs et les domaines protégés protégés dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-194">**Impersonation**: Click **Edit** to modify the protected senders and protected domains in the policy.</span></span> <span data-ttu-id="2c18e-195">Ces paramètres sont une condition pour la stratégie qui identifie les expéditeurs usurpés à rechercher (individuellement ou par domaine) dans l’adresse de provenance des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="2c18e-195">These settings are a condition for the policy that identifies spoofed senders to look for (individually or by domain) in the From address of inbound messages.</span></span> <span data-ttu-id="2c18e-196">Pour plus d’informations, consultez la rubrique [emprunt d’identité dans les stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies).</span><span class="sxs-lookup"><span data-stu-id="2c18e-196">For more information, see [Impersonation settings in ATP anti-phishing policies](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies).</span></span>

   - <span data-ttu-id="2c18e-197">**Ajouter des utilisateurs à protéger**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-197">**Add users to protect**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-198">Pour l’activer, faites glisser le bouton bascule sur **activé**, puis cliquez sur le bouton **Ajouter un utilisateur** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-198">To turn it on, slide the toggle to **On**, and then click the **Add user** button that appears.</span></span>

     <span data-ttu-id="2c18e-199">Dans la fenêtre mobile **Ajouter un utilisateur** qui s’affiche, configurez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-199">In the **Add user** flyout that appears, configure the following values:</span></span>

     - <span data-ttu-id="2c18e-200">**Adresse de messagerie**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-200">**Email address**:</span></span>

        - <span data-ttu-id="2c18e-201">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2c18e-201">Click in the box and scroll through the list of users to select.</span></span>
        - <span data-ttu-id="2c18e-202">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-202">Click in the box and start typing to filter the list and select a user.</span></span>
        - <span data-ttu-id="2c18e-203">Pour supprimer une entrée, cliquez sur **supprimer** ![ l’icône Supprimer ](../../media/scc-remove-icon.png) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-203">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="2c18e-204">**Name**: cette valeur est renseignée en fonction de l’adresse de messagerie que vous avez sélectionnée, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="2c18e-204">**Name**: This value is populated based on the email address you selected, but you can change it.</span></span>

     <span data-ttu-id="2c18e-205">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="2c18e-205">When you're finished, click **Save** on any page.</span></span>

    <span data-ttu-id="2c18e-206">Pour modifier une entrée existante, sélectionnez-la dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2c18e-206">To edit an existing entry, select the protected user in the list.</span></span>

   - <span data-ttu-id="2c18e-207">**Ajouter des domaines à protéger**: configurez l’un des paramètres suivants ou les deux :</span><span class="sxs-lookup"><span data-stu-id="2c18e-207">**Add domains to protect**: Configure one or both of the following settings:</span></span>

     - <span data-ttu-id="2c18e-208">**Inclure automatiquement les domaines dont je suis propriétaire**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-208">**Automatically include the domains I own**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-209">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-209">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="2c18e-210">**Inclure les domaines personnalisés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-210">**Include custom domains**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-211">Pour l’activer, faites glisser le bouton bascule sur **activé**, puis dans la zone **Ajouter des domaines** , entrez le nom de domaine (par exemple, contoso.com), appuyez sur entrée et répétez l’opération si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2c18e-211">To turn it on, slide the toggle to **On**, and in the **Add domains** box, enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="2c18e-212">**Actions**: cliquez sur **modifier**</span><span class="sxs-lookup"><span data-stu-id="2c18e-212">**Actions**: Click **Edit**</span></span>

     - <span data-ttu-id="2c18e-213">**Si un message électronique est envoyé par un utilisateur représenté**: configurez l’une des actions suivantes pour les messages dans lesquels l’expéditeur usurpé est l’un des utilisateurs protégés que vous avez spécifié dans **Ajouter des utilisateurs à protéger**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-213">**If email is sent by an impersonated user**: Configure one of the following actions for messages where the spoofed sender is one of the protected users you specified in **Add users to protect**:</span></span>

       - <span data-ttu-id="2c18e-214">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="2c18e-214">**Don't apply any action**</span></span>
       - <span data-ttu-id="2c18e-215">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="2c18e-215">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="2c18e-216">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="2c18e-216">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="2c18e-217">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="2c18e-217">**Quarantine the message**</span></span>
       - <span data-ttu-id="2c18e-218">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="2c18e-218">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="2c18e-219">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="2c18e-219">**Delete the message before it's delivered**</span></span>

     - <span data-ttu-id="2c18e-220">**Si le courrier électronique est envoyé par un domaine emprunté**: configurez l’une des actions suivantes pour les messages dans lesquels l’expéditeur usurpé se trouve dans l’un des domaines protégés que vous avez spécifiés dans **Ajouter des domaines à protéger**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-220">**If email is sent by an impersonated domain**: Configure one of the following actions for messages where the spoofed sender is in one of the protected domains you specified in **Add domains to protect**:</span></span>

     - <span data-ttu-id="2c18e-221">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="2c18e-221">**Don't apply any action**</span></span>
     - <span data-ttu-id="2c18e-222">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="2c18e-222">**Redirect message to other email addresses**</span></span>
     - <span data-ttu-id="2c18e-223">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="2c18e-223">**Move message to Junk Email folder**</span></span>
     - <span data-ttu-id="2c18e-224">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="2c18e-224">**Quarantine the message**</span></span>
     - <span data-ttu-id="2c18e-225">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="2c18e-225">**Deliver the message and add other addresses to the Bcc line**</span></span>
     - <span data-ttu-id="2c18e-226">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="2c18e-226">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="2c18e-227">Cliquez sur **conseils de sécurité pour l’emprunt d’identité** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c18e-227">Click **turn on impersonation safety tips** and configure any of the following settings:</span></span>

     - <span data-ttu-id="2c18e-228">**Afficher l’astuce pour les utilisateurs empruntés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-228">**Show tip for impersonated users**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-229">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-229">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="2c18e-230">**Afficher le Conseil pour les domaines empruntés**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-230">**Show tip for impersonated domains**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-231">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-231">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="2c18e-232">**Afficher le Conseil pour les caractères inhabituels**: la valeur par défaut est **off**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-232">**Show tip for unusual characters**: The default value is **Off**.</span></span> <span data-ttu-id="2c18e-233">Pour l’activer, faites glisser le bouton bascule sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-233">To turn it on, slide the toggle to **On**.</span></span>

     <span data-ttu-id="2c18e-234">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-234">When you're finished, click **Save**.</span></span>

   - <span data-ttu-id="2c18e-235">**Intelligence des boîtes aux lettres**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-235">**Mailbox intelligence**:</span></span>

     - <span data-ttu-id="2c18e-236">**Activer l’intelligence des boîtes aux lettres ?**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-236">**Enable mailbox intelligence?**: The default value is **On**.</span></span> <span data-ttu-id="2c18e-237">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-237">To turn it off, slide the toggle to **Off**.</span></span>

     - <span data-ttu-id="2c18e-238">**Activer la protection contre l’usurpation d’identité basée sur les boîtes aux lettres ?**: ce paramètre est disponible uniquement si **activer l’intelligence des boîtes aux lettres** est **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-238">**Enable mailbox intelligence based impersonation protection?**: This setting is only available if **Enable mailbox intelligence?** is **On**.</span></span>

       <span data-ttu-id="2c18e-239">Dans **si un message électronique est envoyé par un utilisateur emprunté**, vous pouvez spécifier l’une des actions suivantes à effectuer sur les messages qui échouent à la boîte aux lettres (les mêmes actions que celles disponibles pour les utilisateurs protégés et les domaines protégés) :</span><span class="sxs-lookup"><span data-stu-id="2c18e-239">In **If email is sent by an impersonated user**, you can specify one of the following actions to take on messages that fail mailbox intelligence (the same actions that are available for protected users and protected domains):</span></span>

       - <span data-ttu-id="2c18e-240">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="2c18e-240">**Don't apply any action**</span></span>
       - <span data-ttu-id="2c18e-241">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="2c18e-241">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="2c18e-242">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="2c18e-242">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="2c18e-243">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="2c18e-243">**Quarantine the message**</span></span>
       - <span data-ttu-id="2c18e-244">**Remise du message et ajout d’autres adresses à la ligne CCI**</span><span class="sxs-lookup"><span data-stu-id="2c18e-244">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="2c18e-245">**Supprimer le message avant qu’il ne soit remis**</span><span class="sxs-lookup"><span data-stu-id="2c18e-245">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="2c18e-246">**Ajouter des expéditeurs et des domaines approuvés**: spécifiez les exceptions pour la stratégie :</span><span class="sxs-lookup"><span data-stu-id="2c18e-246">**Add trusted senders and domains**: Specify exceptions for the policy:</span></span>

     - <span data-ttu-id="2c18e-247">**Expéditeurs approuvés**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-247">**Trusted senders**:</span></span>

       - <span data-ttu-id="2c18e-248">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2c18e-248">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="2c18e-249">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-249">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="2c18e-250">Pour supprimer une entrée, cliquez sur **supprimer** ![ l’icône Supprimer ](../../media/scc-remove-icon.png) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c18e-250">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="2c18e-251">**Domaines approuvés**: saisissez le nom de domaine (par exemple, contoso.com), appuyez sur entrée et répétez l’opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2c18e-251">**Trusted domains**: Enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="2c18e-252">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="2c18e-252">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="2c18e-253">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-253">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="2c18e-254">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="2c18e-254">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="2c18e-255">**Utilisateurs protégés**</span><span class="sxs-lookup"><span data-stu-id="2c18e-255">**Protected users**</span></span>
       - <span data-ttu-id="2c18e-256">**Domaines protégés** \> **Inclure les domaines dont je suis propriétaire**</span><span class="sxs-lookup"><span data-stu-id="2c18e-256">**Protected domains** \> **Include domains I own**</span></span>
       - <span data-ttu-id="2c18e-257">**Domaines protégés** \> **Domaines protégés** (domaines personnalisés)</span><span class="sxs-lookup"><span data-stu-id="2c18e-257">**Protected domains** \> **Protected domains** (custom domains)</span></span>
       - <span data-ttu-id="2c18e-258">**Veille des boîtes aux lettres**</span><span class="sxs-lookup"><span data-stu-id="2c18e-258">**Mailbox intelligence**</span></span>

   <span data-ttu-id="2c18e-259">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="2c18e-259">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="2c18e-260">**Spoof**: cliquez sur **modifier** pour activer ou désactiver l’Assistant usurpation d’identité, activez ou désactivez l’identification de l’expéditeur non authentifié dans Outlook, puis configurez l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués.</span><span class="sxs-lookup"><span data-stu-id="2c18e-260">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="2c18e-261">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="2c18e-261">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="2c18e-262">Notez que ces mêmes paramètres sont également disponibles dans les stratégies de détection d’hameçonnage dans EOP.</span><span class="sxs-lookup"><span data-stu-id="2c18e-262">Note that these same settings are also available in anti-phishing policies in EOP.</span></span>

   - <span data-ttu-id="2c18e-263">**Usurpation des paramètres de filtrage**: la valeur par défaut est **activée**, et nous vous recommandons de la laisser activée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-263">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="2c18e-264">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-264">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="2c18e-265">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in EOP](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="2c18e-265">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="2c18e-266">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’identité si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="2c18e-266">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="2c18e-267">Pour obtenir des instructions, voir [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="2c18e-267">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="2c18e-268">**Activer la fonctionnalité d’expéditeur non authentifié**: la valeur par défaut est **activé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-268">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="2c18e-269">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-269">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="2c18e-270">**Actions**: spécifiez l’action à effectuer sur les messages qui échouent à l’aide d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="2c18e-270">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="2c18e-271">**Si un message électronique est envoyé par un utilisateur qui n’est pas autorisé à usurper votre domaine**:</span><span class="sxs-lookup"><span data-stu-id="2c18e-271">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="2c18e-272">**Déplacer le message vers les dossiers de courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="2c18e-272">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="2c18e-273">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="2c18e-273">**Quarantine the message**</span></span>

   - <span data-ttu-id="2c18e-274">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="2c18e-274">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="2c18e-275">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-275">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="2c18e-276">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="2c18e-276">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="2c18e-277">**Activer la protection contre l’usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="2c18e-277">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="2c18e-278">**Activer la fonctionnalité d’expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="2c18e-278">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="2c18e-279">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="2c18e-279">When you're finished, click **Save** on any page.</span></span>

7. <span data-ttu-id="2c18e-280">**Paramètres avancés**: cliquez sur **modifier** pour configurer les seuils avancés de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-280">**Advanced settings**: Click **Edit** to configure the advanced phishing thresholds.</span></span> <span data-ttu-id="2c18e-281">Pour plus d’informations, consultez la rubrique [seuils d’hameçonnage avancés dans les stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-atp-anti-phishing-policies).</span><span class="sxs-lookup"><span data-stu-id="2c18e-281">For more information, see [Advanced phishing thresholds in ATP anti-phishing policies](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-atp-anti-phishing-policies).</span></span>

   - <span data-ttu-id="2c18e-282">**Seuils de hameçonnage avancés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-282">**Advanced phishing thresholds**: Select one of the following values:</span></span>

   - <span data-ttu-id="2c18e-283">**1-standard** (il s’agit de la valeur par défaut.)</span><span class="sxs-lookup"><span data-stu-id="2c18e-283">**1 - Standard** (This is the default value.)</span></span>
   - <span data-ttu-id="2c18e-284">**2-agressif**</span><span class="sxs-lookup"><span data-stu-id="2c18e-284">**2 - Aggressive**</span></span>
   - <span data-ttu-id="2c18e-285">**3-plus agressif**</span><span class="sxs-lookup"><span data-stu-id="2c18e-285">**3 - More aggressive**</span></span>
   - <span data-ttu-id="2c18e-286">**4-le plus agressif**</span><span class="sxs-lookup"><span data-stu-id="2c18e-286">**4 - Most aggressive**</span></span>

   - <span data-ttu-id="2c18e-287">**Vérifiez vos paramètres**: cliquez sur **modifier** pour revenir à la page **seuils avancés de hameçonnage** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-287">**Review your settings**: Click **Edit** to jump back to the **Advanced phishing thresholds** page.</span></span>

   <span data-ttu-id="2c18e-288">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="2c18e-288">When you're finished, click **Save** on either page.</span></span>

8. <span data-ttu-id="2c18e-289">Sur la page **modifier votre \< nom \> de stratégie** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-289">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-atp-anti-phishing-policy"></a><span data-ttu-id="2c18e-290">Utiliser le centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-290">Use the Security & Compliance Center to modify the default ATP anti-phishing policy</span></span>

<span data-ttu-id="2c18e-291">La stratégie anti-hameçonnage par défaut ATP est nommée Office antiphishing par défaut et n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="2c18e-291">The default ATP anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="2c18e-292">Pour modifier la stratégie anti-hameçonnage par défaut ATP, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2c18e-292">To modify the default ATP anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="2c18e-293">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-293">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-294">Sur la page **anti-hameçonnage** , cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-294">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="2c18e-295">La page **modifier votre stratégie d’anti-hameçonnage Office 365 par défaut** apparaît.</span><span class="sxs-lookup"><span data-stu-id="2c18e-295">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="2c18e-296">Les sections suivantes sont disponibles, qui contiennent les paramètres identiques lorsque vous [modifiez une stratégie personnalisée](#use-the-security--compliance-center-to-modify-atp-anti-phishing-policies):</span><span class="sxs-lookup"><span data-stu-id="2c18e-296">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-atp-anti-phishing-policies):</span></span>

   - <span data-ttu-id="2c18e-297">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="2c18e-297">**Impersonation**</span></span>
   - <span data-ttu-id="2c18e-298">**Tromp**</span><span class="sxs-lookup"><span data-stu-id="2c18e-298">**Spoof**</span></span>
   - <span data-ttu-id="2c18e-299">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="2c18e-299">**Advanced settings**</span></span>

   <span data-ttu-id="2c18e-300">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="2c18e-300">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="2c18e-301">Vous pouvez voir la section paramètres de **stratégie** et les valeurs, mais il n’existe aucun lien de **modification** , afin que vous ne puissiez pas modifier les paramètres (nom de stratégie, description et personnes auxquelles la stratégie s’applique (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="2c18e-301">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="2c18e-302">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-302">You can't delete the default policy.</span></span>
   - <span data-ttu-id="2c18e-303">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="2c18e-303">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="2c18e-304">Sur la page **modifier votre stratégie par défaut pour les antiphishing Office 365** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-304">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-305">Activer ou désactiver des stratégies anti-hameçonnage personnalisées ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-305">Enable or disable custom ATP anti-phishing policies</span></span>

1. <span data-ttu-id="2c18e-306">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-306">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-307">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="2c18e-307">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="2c18e-308">Faites glisser le bouton bascule sur **désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-308">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="2c18e-309">Faites glisser le bouton bascule sur **activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2c18e-309">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="2c18e-310">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-310">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-311">Définir la priorité des stratégies anti-hameçonnage personnalisées ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-311">Set the priority of custom ATP anti-phishing policies</span></span>

<span data-ttu-id="2c18e-312">Par défaut, les stratégies anti-hameçonnage ATP ont une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="2c18e-312">By default, ATP anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="2c18e-313">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="2c18e-313">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="2c18e-314">Deux stratégies ne peuvent pas avoir la même priorité.</span><span class="sxs-lookup"><span data-stu-id="2c18e-314">No two policies can have the same priority.</span></span>

<span data-ttu-id="2c18e-315">Les stratégies anti-hameçonnage personnalisé ATP sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="2c18e-315">Custom ATP anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="2c18e-316">La stratégie anti-hameçonnage par défaut nommée Office antiphishing par défaut a une valeur de priorité personnalisée la **plus faible**et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="2c18e-316">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="2c18e-317">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie anti-hameçonnage ATP une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-317">**Note**: In the Security & Compliance Center, you can only change the priority of the ATP anti-phishing policy after you create it.</span></span> <span data-ttu-id="2c18e-318">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle anti-hameçonnage (qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="2c18e-318">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="2c18e-319">Pour modifier la priorité d’une stratégie, cliquez sur **augmenter la priorité** ou sur **diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de **priorité** dans le centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="2c18e-319">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="2c18e-320">La modification de la priorité d’une stratégie n’a de sens que si vous disposez de plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="2c18e-320">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="2c18e-321">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-321">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-322">Sélectionnez la stratégie que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="2c18e-322">Select the policy that you want to modify.</span></span> <span data-ttu-id="2c18e-323">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2c18e-323">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="2c18e-324">Le menu de **modification de votre \< nom \> de stratégie** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-324">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="2c18e-325">La stratégie anti-hameçonnage personnalisée ATP avec la valeur **Priority** de priorité **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="2c18e-325">The custom ATP anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="2c18e-326">La stratégie anti-hameçonnage personnalisée ATP avec la valeur de **priorité** la plus faible (par exemple, **3**) a uniquement le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="2c18e-326">The custom ATP anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="2c18e-327">Si vous avez au moins trois stratégies anti-hameçonnage personnalisées, les stratégies de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-327">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="2c18e-328">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-328">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="2c18e-329">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-329">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-330">Utiliser le centre de sécurité & conformité pour afficher les stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-330">Use the Security & Compliance Center to view ATP anti-phishing policies</span></span>

1. <span data-ttu-id="2c18e-331">Dans le centre de sécurité & conformité, puis accédez **Threat management** à \> **Policy** \> **protection contre les**menaces pour le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-331">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-332">Effectuez l'une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-332">Do one of the following steps:</span></span>

   - <span data-ttu-id="2c18e-333">Sélectionnez une stratégie anti-hameçonnage personnalisée ATP que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="2c18e-333">Select a custom ATP anti-phishing policy that you want to view.</span></span> <span data-ttu-id="2c18e-334">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2c18e-334">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="2c18e-335">Cliquez sur **stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-335">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="2c18e-336">Le menu contextuel **modifier votre \< \> nom de stratégie** s’affiche, dans lequel vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="2c18e-336">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-337">Utiliser le centre de sécurité & conformité pour supprimer les stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-337">Use the Security & Compliance Center to remove ATP anti-phishing policies</span></span>

1. <span data-ttu-id="2c18e-338">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-338">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="2c18e-339">Sélectionnez la stratégie que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2c18e-339">Select the policy that you want to remove.</span></span> <span data-ttu-id="2c18e-340">Si elle est déjà sélectionnée, désactivez-la et sélectionnez-la à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2c18e-340">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="2c18e-341">Dans la fenêtre mobile **modifier \< le \> nom de la stratégie** qui s’affiche, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-341">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="2c18e-342">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c18e-342">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-atp-anti-phishing-policies"></a><span data-ttu-id="2c18e-343">Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="2c18e-343">Use Exchange Online PowerShell to configure ATP anti-phishing policies</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="2c18e-344">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-344">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="2c18e-345">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-345">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="2c18e-346">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-346">Create the anti-phish policy.</span></span>

2. <span data-ttu-id="2c18e-347">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="2c18e-347">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="2c18e-348">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="2c18e-348">**Notes**:</span></span>

- <span data-ttu-id="2c18e-349">Vous pouvez créer une nouvelle règle anti-hameçonnage et lui affecter une stratégie anti-hameçonnage existante non associée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-349">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="2c18e-350">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-350">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="2c18e-351">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage de PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="2c18e-351">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="2c18e-352">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="2c18e-352">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>

  - <span data-ttu-id="2c18e-353">Définir la priorité de la stratégie lors de la création ( _ \< numéro \> _de_priorité_ ) sur la cmdlet **New-antiphishrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="2c18e-353">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="2c18e-354">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’avez pas affecté la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-354">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="2c18e-355">Étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-355">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="2c18e-356">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-356">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="2c18e-357">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c18e-357">This example creates anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="2c18e-358">La stratégie est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="2c18e-358">The policy is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>
- <span data-ttu-id="2c18e-359">Description : stratégie de service de recherche.</span><span class="sxs-lookup"><span data-stu-id="2c18e-359">The description is: Research department policy.</span></span>
- <span data-ttu-id="2c18e-360">Active la protection des domaines de l’Organisation pour tous les domaines acceptés et la protection des domaines ciblés pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="2c18e-360">Enables organization domains protection for all accepted domains, and targeted domains protection for fabrikam.com.</span></span>
- <span data-ttu-id="2c18e-361">Spécifie Mai Fujito (mfujito@fabrikam.com) en tant qu’utilisateur pour empêcher l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="2c18e-361">Specifies Mai Fujito (mfujito@fabrikam.com) as the user to protect from impersonation.</span></span>
- <span data-ttu-id="2c18e-362">Active la boîte aux lettres décisionnelle.</span><span class="sxs-lookup"><span data-stu-id="2c18e-362">Enables mailbox intelligence.</span></span>
- <span data-ttu-id="2c18e-363">Active la protection contre les boîtes aux lettres et spécifie l’action de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="2c18e-363">Enables mailbox intelligence protection, and specifies the quarantine action.</span></span>
- <span data-ttu-id="2c18e-364">Active les conseils de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2c18e-364">Enables safety tips.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -EnableOrganizationDomainsProtection $true -EnableTargetedDomainsProtection $true -TargetedDomainsToProtect fabrikam.com -TargetedDomainProtectionAction Quarantine -EnableTargetedUserProtection $true -TargetedUsersToProtect "Mai Fujito;mfujito@fabrikam.com" -TargetedUserProtectionAction Quarantine -EnableMailboxIntelligence $true -EnableMailboxIntelligenceProtection $true -MailboxIntelligenceProtectionAction Quarantine -EnableSimilarUsersSafetyTips $true -EnableSimilarDomainsSafetyTips $true -EnableUnusualCharactersSafetyTips $true
```

<span data-ttu-id="2c18e-365">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="2c18e-365">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="2c18e-366">Étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-366">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="2c18e-367">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-367">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="2c18e-368">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-368">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="2c18e-369">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="2c18e-369">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="2c18e-370">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="2c18e-370">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="2c18e-371">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-371">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="2c18e-372">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="2c18e-372">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="2c18e-373">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-373">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="2c18e-374">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-374">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="2c18e-375">Cet exemple renvoie la liste récapitulative de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2c18e-375">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="2c18e-376">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="2c18e-376">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="2c18e-377">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="2c18e-377">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="2c18e-378">Utiliser PowerShell pour afficher les règles de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-378">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="2c18e-379">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-379">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="2c18e-380">Cet exemple renvoie la liste récapitulative de toutes les règles anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2c18e-380">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="2c18e-381">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-381">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="2c18e-382">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="2c18e-382">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="2c18e-383">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="2c18e-383">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="2c18e-384">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-384">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="2c18e-385">À l’exception des éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell comme lors de la création de la stratégie, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2c18e-385">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) section earlier in this topic.</span></span>

- <span data-ttu-id="2c18e-386">Le commutateur _MakeDefault_ qui désactive la stratégie spécifiée dans la stratégie par défaut (appliquée à tout le monde, toujours à la priorité la **plus basse** et vous ne pouvez pas le supprimer) n’est disponible que lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c18e-386">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="2c18e-387">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (l’applet de commande **Set-antiphishpolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="2c18e-387">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="2c18e-388">Lorsque vous renommez une stratégie anti-hameçonnage dans le centre de sécurité & conformité, vous renommez uniquement la _règle_anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="2c18e-388">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="2c18e-389">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-389">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="2c18e-390">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="2c18e-390">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="2c18e-391">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-391">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="2c18e-392">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-392">The only setting that isn't available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="2c18e-393">Pour activer ou désactiver les règles anti-hameçonnage existantes, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="2c18e-393">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="2c18e-394">Dans le cas contraire, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c18e-394">Otherwise, no additional settings are available when you modify an anti-phish rule in PowerShell.</span></span> <span data-ttu-id="2c18e-395">Les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) , plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2c18e-395">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this topic.</span></span>

<span data-ttu-id="2c18e-396">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-396">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="2c18e-397">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="2c18e-397">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="2c18e-398">Utiliser PowerShell pour activer ou désactiver les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-398">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="2c18e-399">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive la totalité de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="2c18e-399">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="2c18e-400">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="2c18e-400">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="2c18e-401">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-401">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="2c18e-402">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="2c18e-402">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="2c18e-403">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="2c18e-403">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="2c18e-404">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/enable-AntiPhishrule) et [Disable-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/disable-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="2c18e-404">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/enable-AntiPhishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/disable-AntiPhishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="2c18e-405">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-405">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="2c18e-406">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="2c18e-406">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="2c18e-407">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="2c18e-407">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="2c18e-408">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="2c18e-408">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="2c18e-409">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="2c18e-409">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="2c18e-410">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="2c18e-410">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="2c18e-411">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-411">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="2c18e-p144">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="2c18e-p144">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="2c18e-414">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="2c18e-414">**Notes**:</span></span>

- <span data-ttu-id="2c18e-415">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-antiphishrule permet** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-415">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="2c18e-416">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante, elle a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-416">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="2c18e-417">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-417">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="2c18e-418">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-418">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="2c18e-419">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-419">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="2c18e-420">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="2c18e-420">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="2c18e-421">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="2c18e-421">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="2c18e-422">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2c18e-422">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="2c18e-423">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="2c18e-423">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="2c18e-424">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c18e-424">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="2c18e-425">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="2c18e-425">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="2c18e-426">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-antiphishrule permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="2c18e-426">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="2c18e-427">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="2c18e-427">How do you know these procedures worked?</span></span>

<span data-ttu-id="2c18e-428">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage ATP, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-428">To verify that you've successfully configured ATP anti-phishing policies, do any of the following steps:</span></span>

- <span data-ttu-id="2c18e-429">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** pour \> **Policy** \> **le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="2c18e-429">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span> <span data-ttu-id="2c18e-430">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="2c18e-430">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="2c18e-431">Pour afficher plus de détails, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c18e-431">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="2c18e-432">Sélectionnez la stratégie dans la liste, puis affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="2c18e-432">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="2c18e-433">Cliquez sur **stratégie par défaut** et affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="2c18e-433">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="2c18e-434">Dans Exchange Online PowerShell, remplacez \< name \> par le nom de la stratégie ou de la règle, puis exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="2c18e-434">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, and run the following command and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
