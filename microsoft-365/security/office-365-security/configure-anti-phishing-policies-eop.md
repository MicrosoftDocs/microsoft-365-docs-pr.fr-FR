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
description: Les administrateurs peuvent apprendre à créer, modifier et supprimer les stratégies anti-hameçonnage disponibles dans les organisations Exchange Online Protection (EOP) avec ou sans boîtes aux lettres Exchange Online utilisateur.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: c329edc517476cfb184bfa4b70c2f2c9542b6e33
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789062"
---
# <a name="configure-anti-phishing-policies-in-eop"></a><span data-ttu-id="4cc40-103">Configurer des stratégies anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="4cc40-103">Configure anti-phishing policies in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="4cc40-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="4cc40-104">**Applies to**</span></span>
- [<span data-ttu-id="4cc40-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="4cc40-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="4cc40-106">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, il existe une stratégie anti-hameçonnage par défaut qui contient un nombre limité de fonctionnalités anti-usurpation activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc40-106">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there's a default anti-phishing policy that contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="4cc40-107">Si vous souhaitez en savoir plus, consultez l’article [Paramètres d’usurpation dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="4cc40-107">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="4cc40-108">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc40-108">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="4cc40-109">Pour plus de granularité, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cc40-109">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="4cc40-110">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4cc40-110">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="4cc40-111">Les organisations Exchange Online boîtes aux lettres peuvent configurer des stratégies anti-hameçonnage dans le centre de sécurité Microsoft 365 ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cc40-111">Organizations with Exchange Online mailboxes can configure anti-phishing policies in the Microsoft 365 security center or in Exchange Online PowerShell.</span></span> <span data-ttu-id="4cc40-112">Les organisations EOP autonomes peuvent uniquement utiliser le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-112">Standalone EOP organizations can only use the security center.</span></span>

<span data-ttu-id="4cc40-113">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées disponibles dans Microsoft Defender pour Office 365, voir Configurer des stratégies [anti-hameçonnage](configure-atp-anti-phishing-policies.md)dans Microsoft Defender pour Office 365 .</span><span class="sxs-lookup"><span data-stu-id="4cc40-113">For information about creating and modifying the more advanced anti-phishing policies that are available in Microsoft Defender for Office 365, see [Configure anti-phishing policies in Microsoft Defender for Office 365](configure-atp-anti-phishing-policies.md).</span></span>

<span data-ttu-id="4cc40-114">Les éléments de base d’une stratégie anti-hameçonnage sont :</span><span class="sxs-lookup"><span data-stu-id="4cc40-114">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="4cc40-115">**La stratégie anti-hameçonnage :** spécifie les protections de hameçonnage à activer ou désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="4cc40-115">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="4cc40-116">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-116">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="4cc40-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies anti-hameçonnage dans le centre de sécurité :</span><span class="sxs-lookup"><span data-stu-id="4cc40-117">The difference between these two elements isn't obvious when you manage anti-phishing policies in the security center:</span></span>

- <span data-ttu-id="4cc40-118">Lorsque vous créez une stratégie anti-hameçonnage, vous créez en fait une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="4cc40-118">When you create an anti-phishing policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="4cc40-119">Lorsque vous modifiez une stratégie anti-hameçonnage, les paramètres liés au nom, à la priorité, activés ou désactivés, et aux filtres de destinataire modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-119">When you modify an anti-phishing policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="4cc40-120">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-120">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="4cc40-121">Lorsque vous supprimez une stratégie anti-hameçonnage, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="4cc40-121">When you remove an anti-phishing policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="4cc40-122">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="4cc40-122">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="4cc40-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell pour configurer des stratégies [anti-hameçonnage](#use-exchange-online-powershell-to-configure-anti-phishing-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4cc40-123">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies](#use-exchange-online-powershell-to-configure-anti-phishing-policies) section later in this article.</span></span>

<span data-ttu-id="4cc40-124">Chaque organisation dispose d’une stratégie anti-hameçonnage intégrée nommée Office365 AntiPhish Default qui possède les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="4cc40-124">Every organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="4cc40-125">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle anti-hameçonnage (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-125">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="4cc40-126">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="4cc40-126">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="4cc40-127">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-127">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="4cc40-128">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc40-128">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="4cc40-129">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts qui sont appliqués à des utilisateurs ou des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4cc40-129">To increase the effectiveness of anti-phishing protection, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4cc40-130">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4cc40-130">What do you need to know before you begin?</span></span>

- <span data-ttu-id="4cc40-131">Vous ouvrez le centre de sécurité à <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="4cc40-131">You open the security center at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="4cc40-132">Pour aller directement à la page **anti-hameçonnage,** utilisez <https://security.microsoft.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="4cc40-132">To go directly to the **Anti-phishing** page, use <https://security.microsoft.com/antiphishing>.</span></span>

- <span data-ttu-id="4cc40-133">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="4cc40-133">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

  <span data-ttu-id="4cc40-134">Vous ne pouvez pas gérer les stratégies anti-hameçonnage dans EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="4cc40-134">You can't manage anti-phishing policies in standalone EOP PowerShell.</span></span>

- <span data-ttu-id="4cc40-135">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="4cc40-135">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="4cc40-136">Pour ajouter, modifier et supprimer des stratégies anti-hameçonnage,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-136">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="4cc40-137">Pour accéder en lecture seule aux stratégies anti-hameçonnage,  vous  devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-137">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="4cc40-138">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="4cc40-138">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="4cc40-139">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4cc40-139">**Notes**:</span></span>

  - <span data-ttu-id="4cc40-140">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4cc40-140">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="4cc40-141">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4cc40-141">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="4cc40-142">Le **groupe de rôles** Gestion de l’organisation en affichage seul [dans Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la <sup>\*</sup> fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-142">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>

- <span data-ttu-id="4cc40-143">Pour obtenir les paramètres recommandés pour les stratégies anti-hameçonnage, consultez les paramètres de stratégie [anti-hameçonnage par défaut eOP.](recommended-settings-for-eop-and-office365.md#eop-default-anti-phishing-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="4cc40-143">For our recommended settings for anti-phishing policies, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365.md#eop-default-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="4cc40-144">Autorisez jusqu’à 30 minutes d’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4cc40-144">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="4cc40-145">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, voir Ordre et priorité de la [protection du courrier électronique.](how-policies-and-protections-are-combined.md)</span><span class="sxs-lookup"><span data-stu-id="4cc40-145">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security-center-to-create-anti-phishing-policies"></a><span data-ttu-id="4cc40-146">Utiliser le centre de sécurité pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-146">Use the security center to create anti-phishing policies</span></span>

<span data-ttu-id="4cc40-147">La création d’une stratégie anti-hameçonnage personnalisée dans le centre de sécurité crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="4cc40-147">Creating a custom anti-phishing policy in the security center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="4cc40-148">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-148">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-149">Dans la page **Anti-hameçonnage,** cliquez sur ![ Créer une icône ](../../media/m365-cc-sc-create-icon.png) **Créer.**</span><span class="sxs-lookup"><span data-stu-id="4cc40-149">On the **Anti-phishing** page, click ![Create icon](../../media/m365-cc-sc-create-icon.png) **Create**.</span></span>

3. <span data-ttu-id="4cc40-150">L’assistant d'application de stratégies s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="4cc40-150">The policy wizard opens.</span></span> <span data-ttu-id="4cc40-151">Dans la page **Nom de la** stratégie, configurez les paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="4cc40-151">On the **Policy name** page, configure these settings:</span></span>
   - <span data-ttu-id="4cc40-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>
   - <span data-ttu-id="4cc40-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="4cc40-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="4cc40-155">Dans la page **Utilisateurs, groupes et domaines** qui s’affiche, identifiez les destinataires internes auxquels la stratégie s’applique (conditions de destinataire) :</span><span class="sxs-lookup"><span data-stu-id="4cc40-155">On the **Users, groups, and domains** page that appears, identify the internal recipients that the policy applies to (recipient conditions):</span></span>
   - <span data-ttu-id="4cc40-156">**Utilisateurs** : boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cc40-156">**Users**: The specified mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="4cc40-157">**Groupes** : groupes de distribution, groupes de sécurité à extension messagerie ou groupes Microsoft 365 spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cc40-157">**Groups**: The specified distribution groups, mail-enabled security groups, or Microsoft 365 Groups in your organization.</span></span>
   - <span data-ttu-id="4cc40-158">**Domaines** : tous les destinataires des [domaines acceptés](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cc40-158">**Domains**: All recipients in the specified [accepted domains](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) in your organization.</span></span>

   <span data-ttu-id="4cc40-159">Cliquez dans la zone appropriée, commencez à taper une valeur et sélectionnez la valeur souhaitée dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="4cc40-159">Click in the appropriate box, start typing a value, and select the value that you want from the results.</span></span> <span data-ttu-id="4cc40-160">Répétez cette opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4cc40-160">Repeat this process as many times as necessary.</span></span> <span data-ttu-id="4cc40-161">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="4cc40-161">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="4cc40-163">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="4cc40-163">next to the value.</span></span>

   <span data-ttu-id="4cc40-164">Pour les utilisateurs ou les groupes, vous pouvez utiliser la plupart des identificateurs (nom, nom d’affichage, alias, adresse e-mail, nom de compte, etc.), mais le nom d'affichage correspondant apparaît dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="4cc40-164">For users or groups, you can use most identifiers (name, display name, alias, email address, account name, etc.), but the corresponding display name is shown in the results.</span></span> <span data-ttu-id="4cc40-165">Pour les utilisateurs, entrez un astérisque (\*) seul pour afficher toutes les valeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="4cc40-165">For users, enter an asterisk (\*) by itself to see all available values.</span></span>

   <span data-ttu-id="4cc40-166">Plusieurs valeurs dans la même condition utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="4cc40-166">Multiple values in the same condition use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="4cc40-167">Des conditions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="4cc40-167">Different conditions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   - <span data-ttu-id="4cc40-168">**Exclure ces utilisateurs, groupes et domaines** : pour ajouter des exceptions pour les destinataires internes auxquels la stratégie s’applique (exceptions pour les destinataires), sélectionnez cette option et configurez les exceptions.</span><span class="sxs-lookup"><span data-stu-id="4cc40-168">**Exclude these users, groups, and domains**: To add exceptions for the internal recipients that the policy applies to (recpient exceptions), select this option and configure the exceptions.</span></span> <span data-ttu-id="4cc40-169">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="4cc40-169">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="4cc40-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-170">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="4cc40-171">Dans la page **de protection** & seuil de  hameçonnage qui s’affiche, utilisez la case à cocher Activer la veille contre l’usurpation d’informations pour activer ou désactiver l’usurpation d’informations.</span><span class="sxs-lookup"><span data-stu-id="4cc40-171">On the **Phishing threshold & protection** page that appears, use the **Enable spoof intelligence** check box to turn spoof intelligence on or off.</span></span> <span data-ttu-id="4cc40-172">La valeur par défaut est sur (sélectionné) et nous vous recommandons de la laisser.</span><span class="sxs-lookup"><span data-stu-id="4cc40-172">The default value is on (selected), and we recommend that you leave it on.</span></span> <span data-ttu-id="4cc40-173">Vous configurez l’action à prendre sur les messages usurpés bloqués sur la page suivante.</span><span class="sxs-lookup"><span data-stu-id="4cc40-173">You configure the action to take on blocked spoofed messages on the next page.</span></span>

   <span data-ttu-id="4cc40-174">Pour désactiver la veille contre l’usurpation d’informations, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="4cc40-174">To turn off spoof intelligence, clear the check box.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4cc40-175">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’Microsoft 365 ; vous activez plutôt le filtrage amélioré pour les connecteurs.</span><span class="sxs-lookup"><span data-stu-id="4cc40-175">You don't need to turn off anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="4cc40-176">Pour obtenir des instructions, voir [Filtrage amélioré pour les connecteurs dans Exchange Online](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="4cc40-176">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   <span data-ttu-id="4cc40-177">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-177">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="4cc40-178">Dans la page **Action** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4cc40-178">On the **Actions** page that appears, configure the following settings:</span></span>
   - <span data-ttu-id="4cc40-179">**Si le message est détecté comme** usurpant l’usurpation : ce paramètre est disponible uniquement si vous avez sélectionné Activer la veille contre l’usurpation d’informations sur la page précédente. </span><span class="sxs-lookup"><span data-stu-id="4cc40-179">**If message is detected as spoof**: This setting is available only if you selected **Enable spoof intelligence** on the previous page.</span></span> <span data-ttu-id="4cc40-180">Sélectionnez l’une des actions suivantes dans la liste bas pour les messages provenant d’expéditeurs usurpés bloqués :</span><span class="sxs-lookup"><span data-stu-id="4cc40-180">Select one of the following actions in the drop down list for messages from blocked spoofed senders:</span></span>
     - <span data-ttu-id="4cc40-181">**Déplacer le message vers les dossiers Courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="4cc40-181">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="4cc40-182">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="4cc40-182">**Quarantine the message**</span></span>

   - <span data-ttu-id="4cc40-183">**Conseils de & des indicateurs**: ce paramètre est  disponible uniquement si vous avez sélectionné Activer la veille contre l’usurpation d’informations sur la page précédente :</span><span class="sxs-lookup"><span data-stu-id="4cc40-183">**Safety tips & indicators**: This setting is available only if you selected **Enable spoof intelligence** on the previous page:</span></span>
     - <span data-ttu-id="4cc40-184">Afficher **(?)** pour les expéditeurs non authentifiés pour l’usurpation d’identité : ajoute un point d’interrogation à la photo  de l’expéditeur dans la zone De dans Outlook si le message ne passe pas les vérifications SPF ou DKIM et si le message ne passe pas l’authentification DMARC ou [composite](email-validation-and-authentication.md#composite-authentication).</span><span class="sxs-lookup"><span data-stu-id="4cc40-184">**Show (?) for unauthenticated senders for spoof**: Adds a question mark to the sender's photo in the From box in Outlook if the message does not pass SPF or DKIM checks **and** the message does not pass DMARC or [composite authentication](email-validation-and-authentication.md#composite-authentication).</span></span>
     - <span data-ttu-id="4cc40-185">**Afficher la balise « via**» : ajoute une balise via (chris@contoso.com via fabrikam.com) à l’adresse De si elle est différente du domaine dans la signature DKIM ou l’adresse MAIL **FROM.**</span><span class="sxs-lookup"><span data-stu-id="4cc40-185">**Show "via" tag**: Adds a via tag (chris@contoso.com via fabrikam.com) to the From address if it's different from the domain in the DKIM signature or the **MAIL FROM** address.</span></span>

       > [!NOTE]
       > <span data-ttu-id="4cc40-186">Actuellement, le paramètre **afficher la balise « via »** n’est pas disponible dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="4cc40-186">Currently, the **Show "via" tag** setting is not available in all organizations.</span></span> <span data-ttu-id="4cc40-187">Si vous n’avez pas le paramètre Afficher la  balise « **via** », le point d’interrogation et la balise via sont tous deux contrôlés par l’afficheur **(?)** pour les expéditeurs non authentifiés pour le paramètre d’usurpation d’adresse dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4cc40-187">If you don't have the **Show "via" tag** setting, the the question mark **and** the via tag are both controlled by the **Show (?) for unauthenticated senders for spoof** setting in your organization.</span></span>

     <span data-ttu-id="4cc40-188">Pour activer un paramètre, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="4cc40-188">To turn on a setting, select the check box.</span></span> <span data-ttu-id="4cc40-189">Pour la désactiver, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="4cc40-189">To turn it off, clear the check box.</span></span>

   <span data-ttu-id="4cc40-190">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-190">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="4cc40-191">Dans la page **Révision** qui s’affiche, passez en revue vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="4cc40-191">On the **Review** page that appears, review your settings.</span></span> <span data-ttu-id="4cc40-192">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="4cc40-192">You can select **Edit** in each section to modify the settings within the section.</span></span>

   <span data-ttu-id="4cc40-193">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="4cc40-193">When you're finished, click **Submit**.</span></span>

8. <span data-ttu-id="4cc40-194">Dans la page de confirmation qui s’affiche, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-194">On the confirmation page that appears, click **Done**.</span></span>

## <a name="use-the-security-center-to-view-anti-phishing-policies"></a><span data-ttu-id="4cc40-195">Utiliser le centre de sécurité pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-195">Use the security center to view anti-phishing policies</span></span>

1. <span data-ttu-id="4cc40-196">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-196">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-197">Dans la page **Anti-hameçonnage,** les propriétés suivantes sont affichées dans la liste des stratégies anti-hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="4cc40-197">On the **Anti-phishing** page, the following properties are displayed in the list of anti-phishing policies:</span></span>

   - <span data-ttu-id="4cc40-198">**Name**</span><span class="sxs-lookup"><span data-stu-id="4cc40-198">**Name**</span></span>
   - <span data-ttu-id="4cc40-199">**État**</span><span class="sxs-lookup"><span data-stu-id="4cc40-199">**Status**</span></span>
   - <span data-ttu-id="4cc40-200">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4cc40-200">**Priority**</span></span>
   - <span data-ttu-id="4cc40-201">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="4cc40-201">**Last modified**</span></span>

3. <span data-ttu-id="4cc40-202">Lorsque vous sélectionnez une stratégie en cliquant sur le nom, les paramètres de stratégie s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="4cc40-202">When you select a policy by clicking on the name, the policy settings are displayed in a flyout.</span></span>

## <a name="use-the-security-center-to-modify-anti-phishing-policies"></a><span data-ttu-id="4cc40-203">Utiliser le centre de sécurité pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-203">Use the security center to modify anti-phishing policies</span></span>

1. <span data-ttu-id="4cc40-204">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-204">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-205">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="4cc40-205">On the **Anti-phishing** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="4cc40-206">Dans le menu volant des détails de stratégie qui s’affiche, sélectionnez **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="4cc40-206">In the policy details flyout that appears, select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="4cc40-207">Pour plus d’informations sur les paramètres, voir la section Utiliser le centre de sécurité pour créer des stratégies [anti-hameçonnage](#use-the-security-center-to-create-anti-phishing-policies) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4cc40-207">For more information about the settings, see the [Use the security center to create anti-phishing policies](#use-the-security-center-to-create-anti-phishing-policies) section earlier in this article.</span></span>  

   <span data-ttu-id="4cc40-208">Pour la stratégie anti-hameçonnage par défaut, la section **Utilisateurs,** groupes et domaines n’est pas disponible (la stratégie s’applique à tout le monde) et vous ne pouvez pas renommer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-208">For the default anti-phishing policy, the **Users, groups, and domains** section isn't available (the policy applies to everyone), and you can't rename the policy.</span></span>

<span data-ttu-id="4cc40-209">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4cc40-209">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies"></a><span data-ttu-id="4cc40-210">Activer ou désactiver des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="4cc40-210">Enable or disable custom anti-phishing policies</span></span>

<span data-ttu-id="4cc40-211">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc40-211">You can't disable the default anti-phishing policy.</span></span>

1. <span data-ttu-id="4cc40-212">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-212">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-213">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="4cc40-213">On the **Anti-phishing** page, select a custom policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="4cc40-214">En haut du menu volant des détails de stratégie qui s’affiche, vous verrez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cc40-214">At the top of the policy details flyout that appears, you'll see one of the following values:</span></span>
   - <span data-ttu-id="4cc40-215">**Stratégie désactivée** : pour activer la stratégie, cliquez sur ![Icône Activer](../../media/m365-cc-sc-turn-on-off-icon.png) **Activer**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-215">**Policy off**: To turn on the policy, click ![Turn on icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn on** .</span></span>
   - <span data-ttu-id="4cc40-216">**Stratégie activée** : pour activer la stratégie, cliquez sur ![Icône Désactiver](../../media/m365-cc-sc-turn-on-off-icon.png) **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-216">**Policy on**: To turn off the policy, click ![Turn off icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn off**.</span></span>

4. <span data-ttu-id="4cc40-217">Dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Activer** ou **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-217">In the confirmation dialog that appears, click **Turn on** or **Turn off**.</span></span>

5. <span data-ttu-id="4cc40-218">Cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-218">Click **Close** in the policy details flyout.</span></span>

<span data-ttu-id="4cc40-219">De retour sur la page principale de la stratégie, la valeur **État** de la stratégie sera **Activée** ou **Désactivée**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-219">Back on the main policy page, the **Status** value of the policy will be **On** or **Off**.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies"></a><span data-ttu-id="4cc40-220">Définir la priorité des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="4cc40-220">Set the priority of custom anti-phishing policies</span></span>

<span data-ttu-id="4cc40-221">Par défaut, les stratégies anti-hameçonnage se voir donner une priorité basée sur l’ordre de leur création (les nouvelles stratégies sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="4cc40-221">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="4cc40-222">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="4cc40-222">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="4cc40-223">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-223">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="4cc40-224">Pour modifier la priorité d’une stratégie, cliquez sur **Augmenter la priorité** ou **Diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro **Priorité** dans le centre de sécurité).politique</span><span class="sxs-lookup"><span data-stu-id="4cc40-224">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the security center).</span></span> <span data-ttu-id="4cc40-225">La modification de la priorité d’une stratégie n’a de sens que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="4cc40-225">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

 <span data-ttu-id="4cc40-226">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4cc40-226">**Notes**:</span></span>

- <span data-ttu-id="4cc40-227">Dans le centre de sécurité, vous ne pouvez modifier la priorité de la stratégie anti-hameçonnage qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="4cc40-227">In the security center, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="4cc40-228">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle anti-hameçonnage (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="4cc40-228">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>
- <span data-ttu-id="4cc40-229">Les stratégies anti-hameçonnage sont traitées dans l’ordre d’affichage (la première stratégie a la valeur Priority 0). </span><span class="sxs-lookup"><span data-stu-id="4cc40-229">Anti-phishing policies are processed in the order that they're displayed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="4cc40-230">La stratégie anti-hameçonnage par défaut a la valeur de priorité **La** plus faible et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="4cc40-230">The default anti-phishing policy has the priority value **Lowest**, and you can't change it.</span></span>

1. <span data-ttu-id="4cc40-231">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-231">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-232">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="4cc40-232">On the **Anti-phishing** page, select a custom policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="4cc40-233">En haut du menu volant détails de la stratégie qui s’affiche, vous verrez **Augmenter la priorité** ou **Diminuer la priorité** en fonction de la valeur de priorité actuelle et du nombre de stratégies personnalisées :</span><span class="sxs-lookup"><span data-stu-id="4cc40-233">At the top of the policy details flyout that appears, you'll see **Increase priority** or **Decrease priority** based on the current priority value and the number of custom policies:</span></span>
   - <span data-ttu-id="4cc40-234">La stratégie anti-hameçonnage  dont la valeur de priorité **est 0** ne dispose que de l’option Diminuer **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="4cc40-234">The anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** option available.</span></span>
   - <span data-ttu-id="4cc40-235">La stratégie anti-hameçonnage  dont la valeur de priorité est la plus faible (par exemple, **3**) ne dispose que de l’option Augmenter **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="4cc40-235">The anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** option available.</span></span>
   - <span data-ttu-id="4cc40-236">Si vous disposez de trois stratégies anti-hameçonnage ou plus,  les **stratégies** entre les valeurs de priorité les plus élevées et les plus faibles disposent à la fois des options Augmenter la priorité et Diminuer la priorité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-236">If you have three or more anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** options available.</span></span>

   <span data-ttu-id="4cc40-237">Cliquez sur l’![Icône Augmenter la priorité](../../media/m365-cc-sc-increase-icon.png) **Augmenter la priorité** ou ![Icône Diminuer la priorité](../../media/m365-cc-sc-decrease-icon.png) **Diminuer la priorité** pour modifier la valeur **Priorité**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-237">Click ![Increase priority icon](../../media/m365-cc-sc-increase-icon.png) **Increase priority** or ![Decrease priority icon](../../media/m365-cc-sc-decrease-icon.png) **Decrease priority** to change the **Priority** value.</span></span>

4. <span data-ttu-id="4cc40-238">Lorsque vous avez terminé, cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-238">When you're finished, click **Close** in the policy details flyout.</span></span>

## <a name="use-the-security-center-to-remove-custom-anti-phishing-policies"></a><span data-ttu-id="4cc40-239">Utiliser le centre de sécurité pour supprimer des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="4cc40-239">Use the security center to remove custom anti-phishing policies</span></span>

<span data-ttu-id="4cc40-240">Lorsque vous utilisez le centre de sécurité pour supprimer une stratégie anti-hameçonnage personnalisée, la règle anti-hameçonnage et la stratégie anti-hameçonnage correspondante sont toutes deux supprimées.</span><span class="sxs-lookup"><span data-stu-id="4cc40-240">When you use the security center to remove a custom anti-phishing policy, the anti-phish rule and the corresponding anti-phish policy are both deleted.</span></span> <span data-ttu-id="4cc40-241">Vous ne pouvez pas supprimer la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc40-241">You can't remove the default anti-phishing policy.</span></span>

1. <span data-ttu-id="4cc40-242">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-242">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="4cc40-243">Sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4cc40-243">Select a custom policy from the list by clicking on the name of the policy.</span></span> <span data-ttu-id="4cc40-244">En haut du menu volant Détails de la stratégie qui s’affiche, cliquez sur l’![Icône Autres actions](../../media/m365-cc-sc-more-actions-icon.png) **Autres actions** \> ![Icône Supprimer la stratégie](../../media/m365-cc-sc-delete-icon.png) **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-244">At the top of the policy details flyout that appears, click ![More actions icon](../../media/m365-cc-sc-more-actions-icon.png) **More actions** \> ![Delete policy icon](../../media/m365-cc-sc-delete-icon.png) **Delete policy**.</span></span>

3. <span data-ttu-id="4cc40-245">Dans la boîte de dialogue de confirmation qui s'affiche, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-245">In the confirmation dialog that appears, click **Yes**.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies"></a><span data-ttu-id="4cc40-246">Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-246">Use Exchange Online PowerShell to configure anti-phishing policies</span></span>

<span data-ttu-id="4cc40-247">Comme décrit précédemment, une stratégie anti-hameçonnage se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-247">As previously described, an anti-phishing policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="4cc40-248">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est évidente.</span><span class="sxs-lookup"><span data-stu-id="4cc40-248">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="4cc40-249">Vous gérez les stratégies anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishPolicy** et vous gérez les règles anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="4cc40-249">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="4cc40-250">Dans PowerShell, vous créez d’abord la stratégie anti-hameçonnage, puis vous créez la règle anti-hameçonnage qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="4cc40-250">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="4cc40-251">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-251">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="4cc40-252">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="4cc40-252">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

> [!NOTE]
> <span data-ttu-id="4cc40-253">Les procédures PowerShell suivantes ne sont pas disponibles dans les organisations EOP autonomes utilisant Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cc40-253">The following PowerShell procedures aren't available in standalone EOP organizations using Exchange Online Protection PowerShell.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="4cc40-254">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-254">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="4cc40-255">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="4cc40-255">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="4cc40-256">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-256">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="4cc40-257">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="4cc40-257">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="4cc40-258">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4cc40-258">**Notes**:</span></span>

- <span data-ttu-id="4cc40-259">Vous pouvez créer une règle anti-hameçonnage et lui attribuer une stratégie anti-hameçonnage existante et non dissociée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-259">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="4cc40-260">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-260">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="4cc40-261">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage dans PowerShell qui ne sont pas disponibles dans le centre de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="4cc40-261">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the security center until after you create the policy:</span></span>

  - <span data-ttu-id="4cc40-262">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="4cc40-262">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="4cc40-263">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="4cc40-263">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="4cc40-264">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le centre de sécurité tant que vous n’avez pas attribué la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cc40-264">A new anti-phish policy that you create in PowerShell isn't visible in the security center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="4cc40-265">Étape 1 : Utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-265">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="4cc40-266">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-266">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-EnableSpoofIntelligence <$true | $false>] [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableUnauthenticatedSender <$true | $false>] [-EnableViaTag <$true | $false>]
```

<span data-ttu-id="4cc40-267">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4cc40-267">This example creates an anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="4cc40-268">La description est la suivante : stratégie du service de recherche.</span><span class="sxs-lookup"><span data-stu-id="4cc40-268">The description is: Research department policy.</span></span>
- <span data-ttu-id="4cc40-269">Modifie l’action par défaut pour l’usurpation en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="4cc40-269">Changes the default action for spoofing to Quarantine.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="4cc40-270">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishPolicy](/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="4cc40-270">For detailed syntax and parameter information, see [New-AntiPhishPolicy](/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="4cc40-271">Étape 2 : Utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-271">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="4cc40-272">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-272">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="4cc40-273">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cc40-273">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="4cc40-274">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="4cc40-274">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="4cc40-275">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="4cc40-275">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="4cc40-276">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-276">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="4cc40-277">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishRule](/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="4cc40-277">For detailed syntax and parameter information, see [New-AntiPhishRule](/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="4cc40-278">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-278">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="4cc40-279">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-279">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="4cc40-280">Cet exemple renvoie une liste récapitulatif de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="4cc40-280">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="4cc40-281">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="4cc40-281">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="4cc40-282">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishPolicy](/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="4cc40-282">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="4cc40-283">Utiliser PowerShell pour afficher les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-283">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="4cc40-284">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-284">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="4cc40-285">Cet exemple renvoie une liste récapitulatif de toutes les règles anti-hameçonnage ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="4cc40-285">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="4cc40-286">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cc40-286">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="4cc40-287">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="4cc40-287">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="4cc40-288">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishRule](/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="4cc40-288">For detailed syntax and parameter information, see [Get-AntiPhishRule](/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="4cc40-289">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-289">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="4cc40-290">Outre les éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell que lorsque vous créez une stratégie comme décrit à l’étape 1 : Utiliser PowerShell pour créer une stratégie [anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4cc40-290">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create a policy as described in [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) earlier in this article.</span></span>

- <span data-ttu-id="4cc40-291">Le _commutateur MakeDefault_ qui transforme la stratégie spécifiée en  stratégie par défaut (appliquée à tout le monde, toujours la priorité la plus faible et que vous ne pouvez pas supprimer) est disponible uniquement lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cc40-291">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>
- <span data-ttu-id="4cc40-292">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (la cmdlet **Set-AntiPhishPolicy** n’a pas de _paramètre Name)._</span><span class="sxs-lookup"><span data-stu-id="4cc40-292">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="4cc40-293">Lorsque vous renommez une stratégie anti-hameçonnage dans le centre de sécurité, vous renommez uniquement la règle _anti-hameçonnage._</span><span class="sxs-lookup"><span data-stu-id="4cc40-293">When you rename an anti-phishing policy in the security center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="4cc40-294">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-294">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="4cc40-295">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishPolicy](/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="4cc40-295">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="4cc40-296">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-296">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="4cc40-297">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-297">The only setting that's not available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="4cc40-298">Pour activer ou désactiver des règles anti-hameçonnage existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="4cc40-298">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="4cc40-299">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser PowerShell pour créer une section de règle [anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4cc40-299">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="4cc40-300">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-300">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="4cc40-301">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishRule](/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="4cc40-301">For detailed syntax and parameter information, see [Set-AntiPhishRule](/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="4cc40-302">Utiliser PowerShell pour activer ou désactiver des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-302">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="4cc40-303">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive l’ensemble de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="4cc40-303">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="4cc40-304">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="4cc40-304">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="4cc40-305">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-305">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="4cc40-306">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4cc40-306">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="4cc40-307">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="4cc40-307">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="4cc40-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-AntiPhishRule](/powershell/module/exchange/enable-antiphishrule) et [Disable-AntiPhishRule](/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="4cc40-308">For detailed syntax and parameter information, see [Enable-AntiPhishRule](/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="4cc40-309">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-309">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="4cc40-p132">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle. La valeur la plus basse que vous pouvez définir dépend du nombre de règles. Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4. Tout changement de priorité d'une règle existante peut avoir un effet en cascade sur les autres règles. Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="4cc40-p132">The highest priority value you can set on a rule is 0. The lowest value you can set depends on the number of rules. For example, if you have five rules, you can use the priority values 0 through 4. Changing the priority of an existing rule can have a cascading effect on other rules. For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="4cc40-315">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-315">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="4cc40-p133">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="4cc40-p133">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="4cc40-318">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4cc40-318">**Notes**:</span></span>

- <span data-ttu-id="4cc40-319">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="4cc40-319">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>
- <span data-ttu-id="4cc40-320">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante et a toujours la valeur de priorité nonmodifiable La plus **faible**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-320">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="4cc40-321">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-321">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="4cc40-322">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-322">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="4cc40-323">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-323">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="4cc40-324">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4cc40-324">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="4cc40-325">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishPolicy](/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="4cc40-325">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="4cc40-326">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4cc40-326">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="4cc40-327">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="4cc40-327">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="4cc40-328">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc40-328">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="4cc40-329">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4cc40-329">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="4cc40-330">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishRule](/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="4cc40-330">For detailed syntax and parameter information, see [Remove-AntiPhishRule](/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="4cc40-331">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="4cc40-331">How do you know these procedures worked?</span></span>

<span data-ttu-id="4cc40-332">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage dans EOP, faites l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cc40-332">To verify that you've successfully configured anti-phishing policies in EOP, do any of the following steps:</span></span>

- <span data-ttu-id="4cc40-333">Dans le centre de sécurité, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="4cc40-333">In the security center, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Anti-phishing**.</span></span> <span data-ttu-id="4cc40-334">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="4cc40-334">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="4cc40-335">Pour afficher plus de détails, sélectionnez la stratégie dans la liste en cliquant sur le nom et en visualnant les détails dans le volant qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4cc40-335">To view more details, select the policy from the list by clicking on the name and viewing the details in the flyout that appears.</span></span>

- <span data-ttu-id="4cc40-336">Dans Exchange Online PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante \<Name\> et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="4cc40-336">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
