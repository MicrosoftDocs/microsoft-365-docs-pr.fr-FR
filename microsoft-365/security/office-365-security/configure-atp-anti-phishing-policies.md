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
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage avancées disponibles dans les organisations avec Microsoft Defender pour Office 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d75455df972e9db0ef1cf4bbeba9f3b78b11002b
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50406197"
---
# <a name="configure-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-103">Configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-103">Configure anti-phishing policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8e182-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8e182-104">**Applies to**</span></span>
- [<span data-ttu-id="8e182-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="8e182-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="8e182-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e182-106">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="8e182-107">Les stratégies anti-hameçonnage dans Microsoft Defender pour [Office 365](office-365-atp.md) peuvent aider à protéger votre organisation contre les attaques par hameçonnage basées sur l’emprunt d’identité malveillant et d’autres types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-107">Anti-phishing policies in [Microsoft Defender for Office 365](office-365-atp.md) can help protect your organization from malicious impersonation-based phishing attacks and other types of phishing attacks.</span></span> <span data-ttu-id="8e182-108">Pour plus d’informations sur les différences entre les stratégies anti-hameçonnage dans Exchange Online Protection (EOP) et les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, voir [Protection anti-hameçonnage.](anti-phishing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="8e182-108">For more information about the differences between anti-phishing policies in Exchange Online Protection (EOP) and anti-phishing policies in Microsoft Defender for Office 365, see [Anti-phishing protection](anti-phishing-protection.md).</span></span>

<span data-ttu-id="8e182-109">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-109">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="8e182-110">Pour plus de granularité, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e182-110">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="8e182-111">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8e182-111">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="8e182-112">Vous pouvez configurer des stratégies anti-hameçonnage dans le Centre de sécurité & conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e182-112">You can configure anti-phishing policies in the Security & Compliance Center or in Exchange Online PowerShell.</span></span>

<span data-ttu-id="8e182-113">Pour plus d’informations sur la configuration des stratégies anti-hameçonnage les plus limitées disponibles dans les organisations Exchange Online Protection (c’est-à-dire, les organisations sans Microsoft Defender pour Office 365), voir Configurer des stratégies anti-hameçonnage dans [EOP.](configure-anti-phishing-policies-eop.md)</span><span class="sxs-lookup"><span data-stu-id="8e182-113">For information about configuring the more limited in anti-phishing policies that are available in Exchange Online Protection organizations (that is, organizations without Microsoft Defender for Office 365), see [Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

<span data-ttu-id="8e182-114">Les éléments de base d’une stratégie anti-hameçonnage sont :</span><span class="sxs-lookup"><span data-stu-id="8e182-114">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="8e182-115">**La stratégie anti-hameçonnage :** spécifie les protections de hameçonnage à activer ou désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="8e182-115">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="8e182-116">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-116">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="8e182-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies anti-hameçonnage dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="8e182-117">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="8e182-118">Lorsque vous créez une stratégie, vous créez en fait une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="8e182-118">When you create a policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="8e182-119">Lorsque vous modifiez une stratégie, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-119">When you modify a policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="8e182-120">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="8e182-120">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="8e182-121">Lorsque vous supprimez une stratégie, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="8e182-121">When you remove a policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="8e182-122">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="8e182-122">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="8e182-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage dans Microsoft Defender pour [Office 365](#use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8e182-123">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies in Microsoft Defender for Office 365](#use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365) section later in this article.</span></span>

<span data-ttu-id="8e182-124">Chaque organisation Microsoft Defender pour Office 365 possède une stratégie anti-hameçonnage intégrée nommée Office365 AntiPhish Default qui possède les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="8e182-124">Every Microsoft Defender for Office 365 organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="8e182-125">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle anti-hameçonnage (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-125">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="8e182-126">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="8e182-126">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="8e182-127">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8e182-127">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="8e182-128">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-128">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="8e182-129">Pour accroître l’efficacité de la protection anti-hameçonnage dans Microsoft Defender pour Office 365, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts qui sont appliqués à des utilisateurs ou des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8e182-129">To increase the effectiveness of anti-phishing protection in Microsoft Defender for Office 365, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8e182-130">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8e182-130">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8e182-131">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="8e182-131">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="8e182-132">Pour aller directement à la page **anti-hameçonnage ATP,** utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="8e182-132">To go directly to the **ATP anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="8e182-133">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="8e182-133">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="8e182-134">Des autorisations doivent vous être attribuées dans **Exchange Online** avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="8e182-134">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="8e182-135">Pour ajouter, modifier et supprimer des stratégies anti-hameçonnage,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="8e182-135">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="8e182-136">Pour accéder en lecture seule aux stratégies anti-hameçonnage,  vous  devez être membre des groupes de rôles Lecteur global ou Lecteur de <sup>\*</sup> sécurité.</span><span class="sxs-lookup"><span data-stu-id="8e182-136">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups<sup>\*</sup>.</span></span>

  <span data-ttu-id="8e182-137">Pour plus d'informations, voir [Permissions en échange en ligne](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="8e182-137">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="8e182-138">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="8e182-138">**Notes**:</span></span>

  - <span data-ttu-id="8e182-139">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux _utilisateurs_ les autorisations et autorisations requises pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8e182-139">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="8e182-140">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="8e182-140">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="8e182-141">Le **groupe de rôles** Gestion de l’organisation en affichage seul dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la <sup>\*</sup> fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8e182-141">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>
  - <span data-ttu-id="8e182-142"><sup>\*</sup> Dans le Centre de sécurité & conformité, l’accès en lecture seule permet aux utilisateurs d’afficher les paramètres des stratégies anti-hameçonnage personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8e182-142"><sup>\*</sup> In the Security & Compliance Center, read-only access allows users to view the settings of custom anti-phishing policies.</span></span> <span data-ttu-id="8e182-143">Les utilisateurs en lecture seule ne peuvent pas voir les paramètres dans la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-143">Read-only users can't see the settings in the default anti-phishing policy.</span></span>

- <span data-ttu-id="8e182-144">Pour obtenir les paramètres recommandés pour les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, consultez stratégie anti-hameçonnage dans Les paramètres de Defender pour [Office 365.](recommended-settings-for-eop-and-office365-atp.md#anti-phishing-policy-settings-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="8e182-144">For our recommended settings for anti-phishing policies in Microsoft Defender for Office 365, see [Anti-phishing policy in Defender for Office 365 settings](recommended-settings-for-eop-and-office365-atp.md#anti-phishing-policy-settings-in-microsoft-defender-for-office-365).</span></span>

- <span data-ttu-id="8e182-145">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="8e182-145">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="8e182-146">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, voir Ordre et priorité de la [protection du courrier électronique.](how-policies-and-protections-are-combined.md)</span><span class="sxs-lookup"><span data-stu-id="8e182-146">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-147">Utiliser le Centre de sécurité & conformité pour créer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-147">Use the Security & Compliance Center to create anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8e182-148">La création d’une stratégie anti-hameçonnage personnalisée dans le Centre de sécurité & conformité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="8e182-148">Creating a custom anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="8e182-149">Lorsque vous créez une stratégie anti-hameçonnage, vous ne pouvez spécifier que le nom, la description et le filtre de destinataires qui identifient à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-149">When you create an anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="8e182-150">Après avoir créé la stratégie, vous pouvez la modifier pour modifier ou passer en revue les paramètres anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-150">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="8e182-151">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-151">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-152">Dans la page **Anti-hameçonnage,** cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-152">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="8e182-153">**L’Assistant Créer une stratégie anti-hameçonnage** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8e182-153">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="8e182-154">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e182-154">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="8e182-155">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-155">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="8e182-156">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-156">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="8e182-157">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8e182-157">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="8e182-158">Dans la page **Appliqué à** qui s’affiche, identifiez les destinataires internes à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-158">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="8e182-159">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="8e182-159">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="8e182-160">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="8e182-160">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="8e182-161">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="8e182-161">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="8e182-162">Cliquez **sur Ajouter une condition.**</span><span class="sxs-lookup"><span data-stu-id="8e182-162">Click **Add a condition**.</span></span> <span data-ttu-id="8e182-163">Dans ladown qui s’affiche, sélectionnez une condition sous **Applied si**:</span><span class="sxs-lookup"><span data-stu-id="8e182-163">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="8e182-164">**Le destinataire est**: Spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e182-164">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="8e182-165">**Le destinataire est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e182-165">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="8e182-166">**Le domaine du destinataire** est : Spécifie les destinataires dans un ou plusieurs des domaines acceptés configurés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8e182-166">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in the organization.</span></span>

   <span data-ttu-id="8e182-167">Une fois que vous avez sélectionné la condition, une zone « Tout » apparaît dans la zone « **Tout le** monde ».</span><span class="sxs-lookup"><span data-stu-id="8e182-167">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="8e182-168">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e182-168">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="8e182-169">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="8e182-169">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="8e182-170">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="8e182-170">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="8e182-171">Pour supprimer des entrées individuelles, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="8e182-171">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="8e182-172">Pour supprimer la condition entière, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la condition.</span><span class="sxs-lookup"><span data-stu-id="8e182-172">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="8e182-173">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous Appliqué **si**.</span><span class="sxs-lookup"><span data-stu-id="8e182-173">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="8e182-174">Pour ajouter des exceptions, cliquez **sur Ajouter une condition** et sélectionnez une exception sous Sauf **si**.</span><span class="sxs-lookup"><span data-stu-id="8e182-174">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="8e182-175">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="8e182-175">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="8e182-176">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8e182-176">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="8e182-177">Dans la page **Examiner vos paramètres** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="8e182-177">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="8e182-178">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="8e182-178">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="8e182-179">Lorsque vous avez terminé, cliquez sur **Créer cette stratégie.**</span><span class="sxs-lookup"><span data-stu-id="8e182-179">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="8e182-180">Cliquez **sur OK** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-180">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="8e182-181">Après avoir créé la stratégie anti-hameçonnage avec ces paramètres généraux, utilisez les instructions de la section suivante pour configurer les paramètres de protection dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-181">After you create the anti-phishing policy with these general settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-182">Utiliser le Centre de sécurité & conformité pour modifier les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-182">Use the Security & Compliance Center to modify anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8e182-183">Utilisez les procédures suivantes pour modifier les stratégies anti-hameçonnage : une nouvelle stratégie que vous avez créée ou des stratégies existantes que vous avez déjà personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8e182-183">Use the following procedures to modify anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="8e182-184">Si vous n’y êtes pas déjà, ouvrez le  Centre de sécurité & conformité et allez à l’anti-hameçonnage ATP de la stratégie de gestion \>  \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="8e182-184">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-185">Sélectionnez la stratégie anti-hameçonnage personnalisée à modifier.</span><span class="sxs-lookup"><span data-stu-id="8e182-185">Select the custom anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="8e182-186">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8e182-186">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="8e182-187">Le **volant \<name\> Modifier votre** stratégie s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-187">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="8e182-188">Cliquer sur **Modifier** dans une section vous permet d’accéder aux paramètres de cette section.</span><span class="sxs-lookup"><span data-stu-id="8e182-188">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="8e182-189">Les étapes suivantes sont présentées dans l’ordre d’apparition des sections, mais elles ne sont pas séquentielles (vous pouvez sélectionner et modifier les sections dans n’importe quel ordre).</span><span class="sxs-lookup"><span data-stu-id="8e182-189">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="8e182-190">Une fois  que vous avez cliqué sur Modifier dans une section, les paramètres disponibles sont présentés dans un  format  d’Assistant, mais vous pouvez passer dans les pages dans n’importe quel ordre et vous pouvez cliquer sur Enregistrer sur n’importe quelle page (ou  ![ ](../../media/scc-remove-icon.png) **\<name\>** sur l’icône Annuler ou Fermer pour revenir à la page Modifier votre stratégie (vous n’êtes pas obligé de visiter la dernière page de l’Assistant pour enregistrer ou quitter).</span><span class="sxs-lookup"><span data-stu-id="8e182-190">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="8e182-191">**Paramètre de stratégie**: cliquez **sur Modifier** pour modifier les paramètres qui étaient disponibles lorsque vous [avez](#use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365) créé la stratégie dans la section précédente :</span><span class="sxs-lookup"><span data-stu-id="8e182-191">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-anti-phishing-policies-in-microsoft-defender-for-office-365) in the previous section:</span></span>

   - <span data-ttu-id="8e182-192">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e182-192">**Name**</span></span>
   - <span data-ttu-id="8e182-193">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e182-193">**Description**</span></span>
   - <span data-ttu-id="8e182-194">**Appliqué à**</span><span class="sxs-lookup"><span data-stu-id="8e182-194">**Applied to**</span></span>
   - <span data-ttu-id="8e182-195">**Passer en revue vos paramètres**</span><span class="sxs-lookup"><span data-stu-id="8e182-195">**Review your settings**</span></span>

   <span data-ttu-id="8e182-196">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="8e182-196">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="8e182-197">**Emprunt d’identité**: cliquez **sur Modifier** pour modifier les expéditeurs protégés et les domaines protégés dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-197">**Impersonation**: Click **Edit** to modify the protected senders and protected domains in the policy.</span></span> <span data-ttu-id="8e182-198">Ces paramètres sont une condition de la stratégie qui identifie les expéditeurs usurpés à rechercher (individuellement ou par domaine) dans l’adresse De des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="8e182-198">These settings are a condition for the policy that identifies spoofed senders to look for (individually or by domain) in the From address of inbound messages.</span></span> <span data-ttu-id="8e182-199">Pour plus d’informations, voir Paramètres d’emprunt d’identité dans les [stratégies anti-hameçonnage dans Microsoft Defender pour Office 365.](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="8e182-199">For more information, see [Impersonation settings in anti-phishing policies in Microsoft Defender for Office 365](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span>

   - <span data-ttu-id="8e182-200">**Ajouter des utilisateurs à protéger**: la valeur par défaut est **Off**.</span><span class="sxs-lookup"><span data-stu-id="8e182-200">**Add users to protect**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-201">Pour l’activer, faites glisser le bouton bascule sur **Activer,** puis cliquez sur le bouton **Ajouter** un utilisateur qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-201">To turn it on, slide the toggle to **On**, and then click the **Add user** button that appears.</span></span>

     <span data-ttu-id="8e182-202">Dans le **volant Ajouter un** utilisateur qui s’affiche, configurez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-202">In the **Add user** flyout that appears, configure the following values:</span></span>

     - <span data-ttu-id="8e182-203">**Adresse de messagerie**:</span><span class="sxs-lookup"><span data-stu-id="8e182-203">**Email address**:</span></span>

       - <span data-ttu-id="8e182-204">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e182-204">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="8e182-205">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionner un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e182-205">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="8e182-206">Pour supprimer une entrée, cliquez **sur Supprimer** ![ ](../../media/scc-remove-icon.png) l’icône sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e182-206">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="8e182-207">**Nom**: cette valeur est remplie en fonction de l’adresse de messagerie que vous avez sélectionnée, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="8e182-207">**Name**: This value is populated based on the email address you selected, but you can change it.</span></span>

     <span data-ttu-id="8e182-208">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="8e182-208">When you're finished, click **Save** on any page.</span></span>

     <span data-ttu-id="8e182-209">Pour modifier une entrée existante, sélectionnez l’utilisateur protégé dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8e182-209">To edit an existing entry, select the protected user in the list.</span></span>

     > [!NOTE]
     >
     > - <span data-ttu-id="8e182-210">Dans chaque stratégie anti-hameçonnage, vous pouvez spécifier un maximum de 60 utilisateurs protégés (adresses e-mail de l’expéditeur).</span><span class="sxs-lookup"><span data-stu-id="8e182-210">In each anti-phishing policy, you can specify a maximum of 60 protected users (sender email addresses).</span></span> <span data-ttu-id="8e182-211">Vous ne pouvez pas spécifier le même utilisateur protégé dans plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="8e182-211">You can't specify the same protected user in multiple policies.</span></span>
     >
     > - <span data-ttu-id="8e182-212">La protection contre l’emprunt d’identité d’utilisateur ne fonctionne pas si l’expéditeur et le destinataire ont précédemment communiqué par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8e182-212">User impersonation protection does not work if the sender and recipient have previously communicated via email.</span></span> <span data-ttu-id="8e182-213">Si l’expéditeur et le destinataire n’ont jamais communiqué par courrier électronique, le message est identifié comme une tentative d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="8e182-213">If the sender and recipient have never communicated via email, the message will be identified as an impersonation attempt.</span></span>

   - <span data-ttu-id="8e182-214">**Ajouter des domaines à protéger**: configurez l’un des paramètres suivants ou les deux :</span><span class="sxs-lookup"><span data-stu-id="8e182-214">**Add domains to protect**: Configure one or both of the following settings:</span></span>

     - <span data-ttu-id="8e182-215">**Incluez automatiquement les domaines dont je suis propriétaire**: la valeur par défaut est **Off**.</span><span class="sxs-lookup"><span data-stu-id="8e182-215">**Automatically include the domains I own**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-216">Pour l’activer, faites glisser le curseur sur **Activer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-216">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="8e182-217">**Inclure des domaines personnalisés**: la valeur par défaut est **Off**.</span><span class="sxs-lookup"><span data-stu-id="8e182-217">**Include custom domains**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-218">Pour l’activer, faites glisser le basculement  sur **Activer** et, dans la zone Ajouter des domaines, entrez le nom de domaine (par exemple, contoso.com), appuyez sur Entrée et répétez l’étape si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8e182-218">To turn it on, slide the toggle to **On**, and in the **Add domains** box, enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

     > [!NOTE]
     > <span data-ttu-id="8e182-219">Vous pouvez avoir un maximum de 50 domaines dans toutes les stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-219">You can have a maximum of 50 domains in all anti-phishing policies.</span></span>

   - <span data-ttu-id="8e182-220">**Actions**: cliquez sur **Modifier**</span><span class="sxs-lookup"><span data-stu-id="8e182-220">**Actions**: Click **Edit**</span></span>

     - <span data-ttu-id="8e182-221">Si des messages électroniques sont envoyés par un utilisateur dont l’identité est usurpée : configurez l’une des actions suivantes pour les messages dont l’expéditeur usurpé est l’un des utilisateurs protégés que vous avez spécifiés dans Ajouter des utilisateurs à **protéger**:</span><span class="sxs-lookup"><span data-stu-id="8e182-221">**If email is sent by an impersonated user**: Configure one of the following actions for messages where the spoofed sender is one of the protected users you specified in **Add users to protect**:</span></span>

       - <span data-ttu-id="8e182-222">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="8e182-222">**Don't apply any action**</span></span>
       - <span data-ttu-id="8e182-223">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="8e182-223">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="8e182-224">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e182-224">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="8e182-225">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="8e182-225">**Quarantine the message**</span></span>
       - <span data-ttu-id="8e182-226">**Remettre le message et ajouter d’autres adresses à la ligne Bcc**</span><span class="sxs-lookup"><span data-stu-id="8e182-226">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="8e182-227">**Supprimer le message avant sa livraison**</span><span class="sxs-lookup"><span data-stu-id="8e182-227">**Delete the message before it's delivered**</span></span>

     - <span data-ttu-id="8e182-228">Si le courrier électronique est envoyé par un domaine dont l’identité est usurpée : configurez l’une des actions **suivantes** pour les messages dont l’expéditeur usurpé se trouve dans l’un des domaines protégés que vous avez spécifiés dans Ajouter des domaines à protéger :</span><span class="sxs-lookup"><span data-stu-id="8e182-228">**If email is sent by an impersonated domain**: Configure one of the following actions for messages where the spoofed sender is in one of the protected domains you specified in **Add domains to protect**:</span></span>

       - <span data-ttu-id="8e182-229">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="8e182-229">**Don't apply any action**</span></span>
       - <span data-ttu-id="8e182-230">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="8e182-230">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="8e182-231">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e182-231">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="8e182-232">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="8e182-232">**Quarantine the message**</span></span>
       - <span data-ttu-id="8e182-233">**Remettre le message et ajouter d’autres adresses à la ligne Bcc**</span><span class="sxs-lookup"><span data-stu-id="8e182-233">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="8e182-234">**Supprimer le message avant sa livraison**</span><span class="sxs-lookup"><span data-stu-id="8e182-234">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="8e182-235">Cliquez **sur Activer les conseils de sécurité d’emprunt** d’identité et configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e182-235">Click **turn on impersonation safety tips** and configure any of the following settings:</span></span>

     - <span data-ttu-id="8e182-236">**Afficher le conseil pour les utilisateurs dont** l’identité est usurpée : la valeur par défaut est **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="8e182-236">**Show tip for impersonated users**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-237">Pour l’activer, faites glisser le curseur sur **Activer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-237">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="8e182-238">**Afficher le conseil pour les domaines dont l’identité est emprunt** d’identité : la valeur par défaut est **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="8e182-238">**Show tip for impersonated domains**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-239">Pour l’activer, faites glisser le curseur sur **Activer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-239">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="8e182-240">**Afficher la conseil pour les caractères inhabituels**: la valeur par défaut est **Off**.</span><span class="sxs-lookup"><span data-stu-id="8e182-240">**Show tip for unusual characters**: The default value is **Off**.</span></span> <span data-ttu-id="8e182-241">Pour l’activer, faites glisser le curseur sur **Activer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-241">To turn it on, slide the toggle to **On**.</span></span>

     <span data-ttu-id="8e182-242">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8e182-242">When you're finished, click **Save**.</span></span>

   - <span data-ttu-id="8e182-243">**Intelligence des boîtes aux lettres**:</span><span class="sxs-lookup"><span data-stu-id="8e182-243">**Mailbox intelligence**:</span></span>

     - <span data-ttu-id="8e182-244">**Activer l’intelligence de boîte** aux lettres ? : la valeur par défaut est **Activé**.</span><span class="sxs-lookup"><span data-stu-id="8e182-244">**Enable mailbox intelligence?**: The default value is **On**.</span></span> <span data-ttu-id="8e182-245">Pour le désactiver, faites glisser le curseur sur **Désactiver.**</span><span class="sxs-lookup"><span data-stu-id="8e182-245">To turn it off, slide the toggle to **Off**.</span></span>

     - <span data-ttu-id="8e182-246">**Activer la protection contre l’emprunt** d’identité basée sur l’intelligence des boîtes aux **lettres**? : ce paramètre est disponible uniquement si l’intelligence de boîte **aux** lettres est activée .</span><span class="sxs-lookup"><span data-stu-id="8e182-246">**Enable mailbox intelligence based impersonation protection?**: This setting is only available if **Enable mailbox intelligence?** is **On**.</span></span>

       <span data-ttu-id="8e182-247">Dans Si le courrier électronique est envoyé par un utilisateur dont l’identité est usurpée, vous pouvez spécifier l’une des actions suivantes à prendre sur les messages qui échouent à la veille de boîte aux lettres (les mêmes actions disponibles pour les utilisateurs protégés et les domaines protégés) :</span><span class="sxs-lookup"><span data-stu-id="8e182-247">In **If email is sent by an impersonated user**, you can specify one of the following actions to take on messages that fail mailbox intelligence (the same actions that are available for protected users and protected domains):</span></span>

       - <span data-ttu-id="8e182-248">**Ne pas appliquer d’action**</span><span class="sxs-lookup"><span data-stu-id="8e182-248">**Don't apply any action**</span></span>
       - <span data-ttu-id="8e182-249">**Rediriger le message vers d’autres adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="8e182-249">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="8e182-250">**Déplacer le message dans le dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e182-250">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="8e182-251">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="8e182-251">**Quarantine the message**</span></span>
       - <span data-ttu-id="8e182-252">**Remettre le message et ajouter d’autres adresses à la ligne Bcc**</span><span class="sxs-lookup"><span data-stu-id="8e182-252">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="8e182-253">**Supprimer le message avant sa livraison**</span><span class="sxs-lookup"><span data-stu-id="8e182-253">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="8e182-254">**Ajouter des expéditeurs et des domaines de confiance**: spécifiez des exceptions pour la stratégie :</span><span class="sxs-lookup"><span data-stu-id="8e182-254">**Add trusted senders and domains**: Specify exceptions for the policy:</span></span>

     - <span data-ttu-id="8e182-255">**Expéditeurs fiables**:</span><span class="sxs-lookup"><span data-stu-id="8e182-255">**Trusted senders**:</span></span>

       - <span data-ttu-id="8e182-256">Cliquez dans la zone et faites défiler la liste des utilisateurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e182-256">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="8e182-257">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionner un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e182-257">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="8e182-258">Pour supprimer une entrée, cliquez **sur Supprimer** ![ ](../../media/scc-remove-icon.png) l’icône sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e182-258">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="8e182-259">**Domaines de confiance**: entrez le nom de domaine (par exemple, contoso.com), appuyez sur Entrée et répétez les étapes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8e182-259">**Trusted domains**: Enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="8e182-260">**Consultez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="8e182-260">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="8e182-261">Vous pouvez cliquer **sur Modifier** dans chaque section pour revenir à la page concernée.</span><span class="sxs-lookup"><span data-stu-id="8e182-261">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="8e182-262">Vous pouvez basculer les paramètres  suivants **directement** sur cette page :</span><span class="sxs-lookup"><span data-stu-id="8e182-262">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="8e182-263">**Utilisateurs protégés**</span><span class="sxs-lookup"><span data-stu-id="8e182-263">**Protected users**</span></span>
       - <span data-ttu-id="8e182-264">**Domaines protégés** \> **Inclure les domaines que je possède**</span><span class="sxs-lookup"><span data-stu-id="8e182-264">**Protected domains** \> **Include domains I own**</span></span>
       - <span data-ttu-id="8e182-265">**Domaines protégés** \> **Domaines protégés** (domaines personnalisés)</span><span class="sxs-lookup"><span data-stu-id="8e182-265">**Protected domains** \> **Protected domains** (custom domains)</span></span>
       - <span data-ttu-id="8e182-266">**Veille des boîtes aux lettres**</span><span class="sxs-lookup"><span data-stu-id="8e182-266">**Mailbox intelligence**</span></span>

   <span data-ttu-id="8e182-267">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="8e182-267">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="8e182-268">Usurpation d’identité : cliquez sur Modifier pour activer ou désactiver la veille contre l’usurpation d’identité, activer ou désactiver l’identification des expéditeurs non authentifiés dans Outlook et configurer l’action à appliquer aux messages provenant d’expéditeurs usurpés bloqués. </span><span class="sxs-lookup"><span data-stu-id="8e182-268">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="8e182-269">Pour plus d’informations, voir Paramètres d’usurpation [d’informations dans les stratégies anti-hameçonnage.](set-up-anti-phishing-policies.md#spoof-settings)</span><span class="sxs-lookup"><span data-stu-id="8e182-269">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="8e182-270">Notez que ces mêmes paramètres sont également disponibles dans les stratégies anti-hameçonnage dans EOP.</span><span class="sxs-lookup"><span data-stu-id="8e182-270">Note that these same settings are also available in anti-phishing policies in EOP.</span></span>

   - <span data-ttu-id="8e182-271">**Paramètres de filtre** d’usurpation d’usurpation : la valeur par défaut est **Sur** et nous vous recommandons de la laisser.</span><span class="sxs-lookup"><span data-stu-id="8e182-271">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="8e182-272">Pour le désactiver, faites glisser le curseur sur **Désactiver.**</span><span class="sxs-lookup"><span data-stu-id="8e182-272">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="8e182-273">Pour plus d’informations, voir [Configurer la veille contre l’usurpation d’adresse dans EOP.](learn-about-spoof-intelligence.md)</span><span class="sxs-lookup"><span data-stu-id="8e182-273">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="8e182-274">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’usurpation si votre enregistrement MX ne pointe pas vers Microsoft 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="8e182-274">You don't need to disable anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="8e182-275">Pour obtenir des instructions, voir [Filtrage amélioré pour les connecteurs dans Exchange Online.](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors)</span><span class="sxs-lookup"><span data-stu-id="8e182-275">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="8e182-276">**Activer la fonctionnalité Expéditeur** non authentifié : la valeur par défaut est **Activé.**</span><span class="sxs-lookup"><span data-stu-id="8e182-276">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="8e182-277">Pour le désactiver, faites glisser le curseur sur **Désactiver.**</span><span class="sxs-lookup"><span data-stu-id="8e182-277">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="8e182-278">**Actions**: spécifiez l’action à prendre sur les messages qui échouent à la veille contre l’usurpation d’informations :</span><span class="sxs-lookup"><span data-stu-id="8e182-278">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="8e182-279">**Si un e-mail est envoyé par une personne qui n’est** pas autorisée à usurper votre domaine :</span><span class="sxs-lookup"><span data-stu-id="8e182-279">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="8e182-280">**Déplacer le message vers les dossiers Courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="8e182-280">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="8e182-281">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="8e182-281">**Quarantine the message**</span></span>

   - <span data-ttu-id="8e182-282">**Consultez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="8e182-282">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="8e182-283">Vous pouvez cliquer **sur Modifier** dans chaque section pour revenir à la page concernée.</span><span class="sxs-lookup"><span data-stu-id="8e182-283">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="8e182-284">Vous pouvez basculer les paramètres  suivants **directement** sur cette page :</span><span class="sxs-lookup"><span data-stu-id="8e182-284">You can toggle the following settings **On** or **Off** directly on this page:</span></span>
       - <span data-ttu-id="8e182-285">**Activer la protection contre l’usurpation d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="8e182-285">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="8e182-286">**Activer la fonctionnalité Expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="8e182-286">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="8e182-287">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="8e182-287">When you're finished, click **Save** on any page.</span></span>

7. <span data-ttu-id="8e182-288">**Paramètres avancés :** cliquez **sur Modifier** pour configurer les seuils de hameçonnage avancés.</span><span class="sxs-lookup"><span data-stu-id="8e182-288">**Advanced settings**: Click **Edit** to configure the advanced phishing thresholds.</span></span> <span data-ttu-id="8e182-289">Pour plus d’informations, voir Seuils d’hameçonnage avancés dans les [stratégies anti-hameçonnage dans Microsoft Defender pour Office 365.](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="8e182-289">For more information, see [Advanced phishing thresholds in anti-phishing policies in Microsoft Defender for Office 365](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span>

   - <span data-ttu-id="8e182-290">**Seuils de hameçonnage avancés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-290">**Advanced phishing thresholds**: Select one of the following values:</span></span>

   - <span data-ttu-id="8e182-291">**1 - Standard** (il s’agit de la valeur par défaut.)</span><span class="sxs-lookup"><span data-stu-id="8e182-291">**1 - Standard** (This is the default value.)</span></span>
   - <span data-ttu-id="8e182-292">**2 - Agressif**</span><span class="sxs-lookup"><span data-stu-id="8e182-292">**2 - Aggressive**</span></span>
   - <span data-ttu-id="8e182-293">**3 - Plus agressif**</span><span class="sxs-lookup"><span data-stu-id="8e182-293">**3 - More aggressive**</span></span>
   - <span data-ttu-id="8e182-294">**4 - Plus agressif**</span><span class="sxs-lookup"><span data-stu-id="8e182-294">**4 - Most aggressive**</span></span>

   - <span data-ttu-id="8e182-295">**Consultez vos paramètres**: cliquez sur **Modifier** pour revenir à la page **Seuils d’hameçonnage** avancés.</span><span class="sxs-lookup"><span data-stu-id="8e182-295">**Review your settings**: Click **Edit** to jump back to the **Advanced phishing thresholds** page.</span></span>

   <span data-ttu-id="8e182-296">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur l’une ou l’autre page.</span><span class="sxs-lookup"><span data-stu-id="8e182-296">When you're finished, click **Save** on either page.</span></span>

8. <span data-ttu-id="8e182-297">De retour sur la page **Modifier votre \<Name\> stratégie,** consultez vos paramètres, puis cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-297">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-298">Utiliser le Centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-298">Use the Security & Compliance Center to modify the default anti-phishing policy in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8e182-299">La stratégie anti-hameçonnage par défaut dans Microsoft Defender pour Office 365 est nommée Par défaut anti-hameçonnage Office365 et elle n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="8e182-299">The default anti-phishing policy in Microsoft Defender for Office 365 is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="8e182-300">Pour modifier la stratégie anti-hameçonnage par défaut, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-300">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="8e182-301">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-301">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-302">Dans la page **Anti-hameçonnage,** cliquez sur **Stratégie par défaut.**</span><span class="sxs-lookup"><span data-stu-id="8e182-302">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="8e182-303">La page **Modifier votre stratégie Office 365 AntiPhish Default** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-303">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="8e182-304">Les sections suivantes sont disponibles, qui contiennent des paramètres identiques lorsque vous [modifiez une stratégie personnalisée](#use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365):</span><span class="sxs-lookup"><span data-stu-id="8e182-304">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-anti-phishing-policies-in-microsoft-defender-for-office-365):</span></span>

   - <span data-ttu-id="8e182-305">**Emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="8e182-305">**Impersonation**</span></span>
   - <span data-ttu-id="8e182-306">**Usurpation d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="8e182-306">**Spoof**</span></span>
   - <span data-ttu-id="8e182-307">**Paramètres avancés**</span><span class="sxs-lookup"><span data-stu-id="8e182-307">**Advanced settings**</span></span>

   <span data-ttu-id="8e182-308">Les paramètres suivants ne sont pas disponibles lorsque vous modifiez la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="8e182-308">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="8e182-309">Vous pouvez voir la **section** paramètres de  stratégie et les valeurs, mais il n’existe aucun lien Modifier, donc vous ne pouvez pas modifier les paramètres (nom de stratégie, description et à qui s’applique la stratégie (elle s’applique à tous les destinataires)).</span><span class="sxs-lookup"><span data-stu-id="8e182-309">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="8e182-310">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-310">You can't delete the default policy.</span></span>
   - <span data-ttu-id="8e182-311">Vous ne pouvez pas modifier la priorité de la stratégie par défaut (elle est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="8e182-311">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="8e182-312">Dans la page **Modifier votre stratégie Par défaut, consultez** vos paramètres, puis cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="8e182-312">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-313">Activer ou désactiver des stratégies anti-hameçonnage personnalisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-313">Enable or disable custom anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="8e182-314">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-314">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-315">Notez la valeur dans la **colonne État** :</span><span class="sxs-lookup"><span data-stu-id="8e182-315">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="8e182-316">Faites glisser le curseur sur **Désactivé** pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-316">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="8e182-317">Faites glisser le curseur sur **Activé** pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8e182-317">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="8e182-318">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-318">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-319">Définir la priorité des stratégies anti-hameçonnage personnalisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-319">Set the priority of custom anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8e182-320">Par défaut, les stratégies anti-hameçonnage se voir donner une priorité basée sur l’ordre de leur création (les nouvelles stratégies sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="8e182-320">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="8e182-321">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="8e182-321">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="8e182-322">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="8e182-322">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="8e182-323">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="8e182-323">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="8e182-324">Les stratégies anti-hameçonnage personnalisées sont affichées dans l’ordre  de traitement (la première stratégie a la valeur Priorité 0).</span><span class="sxs-lookup"><span data-stu-id="8e182-324">Custom anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="8e182-325">La stratégie anti-hameçonnage par défaut nommée Office365 AntiPhish Default a la valeur de priorité personnalisée **La** plus faible et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="8e182-325">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="8e182-326">**Remarque**: dans le Centre de sécurité & conformité, vous ne pouvez modifier la priorité de la stratégie anti-hameçonnage qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="8e182-326">**Note**: In the Security & Compliance Center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="8e182-327">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle anti-hameçonnage (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="8e182-327">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="8e182-328">Pour modifier la priorité d’une stratégie, cliquez sur Augmenter la priorité ou Diminuer la  priorité dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro de priorité dans le Centre de sécurité & conformité).  </span><span class="sxs-lookup"><span data-stu-id="8e182-328">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="8e182-329">La modification de la priorité d’une stratégie n’est logique que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="8e182-329">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="8e182-330">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-330">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-331">Sélectionnez la stratégie à modifier.</span><span class="sxs-lookup"><span data-stu-id="8e182-331">Select the policy that you want to modify.</span></span> <span data-ttu-id="8e182-332">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8e182-332">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="8e182-333">Le **volant \<name\> Modifier votre** stratégie s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-333">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="8e182-334">La stratégie anti-hameçonnage  personnalisée dont la valeur de priorité **est 0** ne dispose que **du** bouton Diminuer la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="8e182-334">The custom anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="8e182-335">La stratégie anti-hameçonnage personnalisée  dont la valeur de priorité est la plus faible (par exemple, **3**) ne dispose que du bouton **Augmenter** la priorité.</span><span class="sxs-lookup"><span data-stu-id="8e182-335">The custom anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="8e182-336">Si vous disposez de trois stratégies anti-hameçonnage personnalisées ou plus, les  stratégies entre les valeurs de priorité les plus élevées et les plus faibles disposent à la fois des boutons Augmenter la priorité et Diminuer la priorité. </span><span class="sxs-lookup"><span data-stu-id="8e182-336">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="8e182-337">Cliquez **sur Augmenter la priorité** ou Diminuer la **priorité** pour modifier la **valeur** Priorité.</span><span class="sxs-lookup"><span data-stu-id="8e182-337">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="8e182-338">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8e182-338">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-339">Utiliser le Centre de sécurité & conformité pour afficher les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-339">Use the Security & Compliance Center to view anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="8e182-340">Dans le Centre de sécurité & conformité, puis allez à  l’anti-hameçonnage ATP de la stratégie de gestion \>  \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="8e182-340">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-341">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-341">Do one of the following steps:</span></span>

   - <span data-ttu-id="8e182-342">Sélectionnez une stratégie anti-hameçonnage personnalisée à afficher.</span><span class="sxs-lookup"><span data-stu-id="8e182-342">Select a custom anti-phishing policy that you want to view.</span></span> <span data-ttu-id="8e182-343">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8e182-343">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="8e182-344">Cliquez **sur Stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-344">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="8e182-345">Le **volant \<name\> Modifier votre stratégie** s’affiche, où vous pouvez afficher les paramètres et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8e182-345">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-346">Utiliser le Centre de sécurité & conformité pour supprimer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-346">Use the Security & Compliance Center to remove anti-phishing policies in Microsoft Defender for Office 365</span></span>

1. <span data-ttu-id="8e182-347">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-347">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8e182-348">Sélectionnez la stratégie à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8e182-348">Select the policy that you want to remove.</span></span> <span data-ttu-id="8e182-349">S’il est déjà sélectionné, désélectionnez-le et sélectionnez-le à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8e182-349">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="8e182-350">Dans le **volant \<name\> Modifier votre stratégie** qui s’affiche, cliquez sur Supprimer la **stratégie,** puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e182-350">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="8e182-351">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e182-351">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8e182-352">Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e182-352">Use Exchange Online PowerShell to configure anti-phishing policies in Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8e182-353">Comme décrit précédemment, une stratégie anti-courrier indésirable se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-353">As previously described, an anti-spam policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="8e182-354">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est évidente.</span><span class="sxs-lookup"><span data-stu-id="8e182-354">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="8e182-355">Vous gérez les stratégies anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishPolicy** et vous gérez les règles anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="8e182-355">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="8e182-356">Dans PowerShell, vous créez d’abord la stratégie anti-hameçonnage, puis vous créez la règle anti-hameçonnage qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="8e182-356">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="8e182-357">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-357">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="8e182-358">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="8e182-358">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="8e182-359">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-359">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="8e182-360">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="8e182-360">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="8e182-361">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-361">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="8e182-362">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="8e182-362">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="8e182-363">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="8e182-363">**Notes**:</span></span>

- <span data-ttu-id="8e182-364">Vous pouvez créer une règle anti-hameçonnage et lui attribuer une stratégie anti-hameçonnage existante et non dissociée.</span><span class="sxs-lookup"><span data-stu-id="8e182-364">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="8e182-365">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-365">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="8e182-366">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage dans PowerShell qui ne sont pas disponibles dans le Centre de sécurité & conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="8e182-366">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="8e182-367">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="8e182-367">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="8e182-368">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="8e182-368">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="8e182-369">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le Centre de sécurité & conformité tant que vous n’avez pas attribué la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e182-369">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="8e182-370">Étape 1 : Utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-370">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="8e182-371">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-371">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="8e182-372">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e182-372">This example creates anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="8e182-373">La stratégie est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="8e182-373">The policy is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>
- <span data-ttu-id="8e182-374">La description est la suivante : stratégie du service de recherche.</span><span class="sxs-lookup"><span data-stu-id="8e182-374">The description is: Research department policy.</span></span>
- <span data-ttu-id="8e182-375">Active la protection des domaines d’organisation pour tous les domaines acceptés et la protection des domaines ciblés pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="8e182-375">Enables organization domains protection for all accepted domains, and targeted domains protection for fabrikam.com.</span></span>
- <span data-ttu-id="8e182-376">Spécifie Mai Fujito (mfujito@fabrikam.com) en tant qu’utilisateur pour empêcher l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="8e182-376">Specifies Mai Fujito (mfujito@fabrikam.com) as the user to protect from impersonation.</span></span>
- <span data-ttu-id="8e182-377">Active la boîte aux lettres décisionnelle.</span><span class="sxs-lookup"><span data-stu-id="8e182-377">Enables mailbox intelligence.</span></span>
- <span data-ttu-id="8e182-378">Active la protection de l’intelligence des boîtes aux lettres et spécifie l’action de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="8e182-378">Enables mailbox intelligence protection, and specifies the quarantine action.</span></span>
- <span data-ttu-id="8e182-379">Active les conseils de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8e182-379">Enables safety tips.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -EnableOrganizationDomainsProtection $true -EnableTargetedDomainsProtection $true -TargetedDomainsToProtect fabrikam.com -TargetedDomainProtectionAction Quarantine -EnableTargetedUserProtection $true -TargetedUsersToProtect "Mai Fujito;mfujito@fabrikam.com" -TargetedUserProtectionAction Quarantine -EnableMailboxIntelligence $true -EnableMailboxIntelligenceProtection $true -MailboxIntelligenceProtectionAction Quarantine -EnableSimilarUsersSafetyTips $true -EnableSimilarDomainsSafetyTips $true -EnableUnusualCharactersSafetyTips $true
```

<span data-ttu-id="8e182-380">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="8e182-380">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="8e182-381">Étape 2 : Utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-381">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="8e182-382">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-382">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="8e182-383">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-383">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="8e182-384">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="8e182-384">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="8e182-385">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="8e182-385">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="8e182-386">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8e182-386">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="8e182-387">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="8e182-387">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="8e182-388">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-388">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="8e182-389">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-389">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="8e182-390">Cet exemple renvoie une liste récapitulatif de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8e182-390">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="8e182-391">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="8e182-391">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="8e182-392">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="8e182-392">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="8e182-393">Utiliser PowerShell pour afficher les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-393">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="8e182-394">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-394">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="8e182-395">Cet exemple renvoie une liste récapitulatif de toutes les règles anti-hameçonnage ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8e182-395">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="8e182-396">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-396">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="8e182-397">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="8e182-397">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="8e182-398">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="8e182-398">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="8e182-399">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-399">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="8e182-400">Outre les éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell que lorsque vous créez la stratégie comme décrit à l’étape 1 : Utiliser PowerShell pour créer une section de stratégie [anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8e182-400">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) section earlier in this article.</span></span>

- <span data-ttu-id="8e182-401">Le _commutateur MakeDefault_ qui transforme la stratégie spécifiée en  stratégie par défaut (appliquée à tout le monde, toujours la priorité la plus faible et que vous ne pouvez pas supprimer) est disponible uniquement lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e182-401">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="8e182-402">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (la cmdlet **Set-AntiPhishPolicy** n’a pas de _paramètre Name)._</span><span class="sxs-lookup"><span data-stu-id="8e182-402">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="8e182-403">Lorsque vous renommez une stratégie anti-hameçonnage dans le Centre de sécurité & conformité, vous renommez uniquement la règle _anti-hameçonnage._</span><span class="sxs-lookup"><span data-stu-id="8e182-403">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="8e182-404">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-404">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="8e182-405">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="8e182-405">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="8e182-406">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-406">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="8e182-407">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="8e182-407">The only setting that isn't available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="8e182-408">Pour activer ou désactiver des règles anti-hameçonnage existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="8e182-408">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="8e182-409">Sinon, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e182-409">Otherwise, no additional settings are available when you modify an anti-phish rule in PowerShell.</span></span> <span data-ttu-id="8e182-410">Les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser PowerShell pour créer une section de règle [anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8e182-410">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="8e182-411">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-411">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="8e182-412">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="8e182-412">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="8e182-413">Utiliser PowerShell pour activer ou désactiver des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-413">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="8e182-414">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive l’ensemble de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="8e182-414">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="8e182-415">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="8e182-415">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="8e182-416">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-416">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="8e182-417">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="8e182-417">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="8e182-418">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="8e182-418">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="8e182-419">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) et [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="8e182-419">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="8e182-420">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-420">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="8e182-421">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="8e182-421">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="8e182-422">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="8e182-422">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="8e182-423">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="8e182-423">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="8e182-424">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="8e182-424">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="8e182-425">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="8e182-425">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="8e182-426">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-426">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="8e182-p148">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="8e182-p148">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="8e182-429">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="8e182-429">**Notes**:</span></span>

- <span data-ttu-id="8e182-430">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="8e182-430">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="8e182-431">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante et elle a toujours la valeur de priorité nonmodifiable La plus **faible**.</span><span class="sxs-lookup"><span data-stu-id="8e182-431">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="8e182-432">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-432">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="8e182-433">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="8e182-433">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="8e182-434">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-434">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="8e182-435">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="8e182-435">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="8e182-436">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="8e182-436">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="8e182-437">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8e182-437">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="8e182-438">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="8e182-438">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="8e182-439">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8e182-439">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="8e182-440">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="8e182-440">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="8e182-441">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="8e182-441">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="8e182-442">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="8e182-442">How do you know these procedures worked?</span></span>

<span data-ttu-id="8e182-443">Pour vérifier que vous avez correctement configuré les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, faites l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-443">To verify that you've successfully configured anti-phishing policies in Microsoft Defender for Office 365, do any of the following steps:</span></span>

- <span data-ttu-id="8e182-444">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8e182-444">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span> <span data-ttu-id="8e182-445">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="8e182-445">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="8e182-446">Pour afficher plus de détails, vous pouvez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e182-446">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="8e182-447">Sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="8e182-447">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="8e182-448">Cliquez **sur Stratégie par** défaut et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="8e182-448">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="8e182-449">Dans Exchange Online PowerShell, remplacez par le nom de la stratégie ou de la règle, puis exécutez la commande suivante \<Name\> et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="8e182-449">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, and run the following command and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
