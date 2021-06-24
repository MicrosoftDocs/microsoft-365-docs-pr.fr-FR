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
ms.openlocfilehash: e56e1b5d91b74d2ffcf9cccc897962b915c6e83c
ms.sourcegitcommit: ebb1c3b4d94058a58344317beb9475c8a2eae9a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53108066"
---
# <a name="configure-anti-phishing-policies-in-eop"></a><span data-ttu-id="46e30-103">Configurer des stratégies anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="46e30-103">Configure anti-phishing policies in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="46e30-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="46e30-104">**Applies to**</span></span>
- [<span data-ttu-id="46e30-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="46e30-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="46e30-106">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, il existe une stratégie anti-hameçonnage par défaut qui contient un nombre limité de fonctionnalités de protection contre l’usurpation d’adresses qui sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="46e30-106">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there's a default anti-phishing policy that contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="46e30-107">Si vous souhaitez en savoir plus, consultez l’article [Paramètres d’usurpation dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="46e30-107">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="46e30-108">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="46e30-108">Admins can view, edit, and configure (but not delete) the default anti-phishing policy.</span></span> <span data-ttu-id="46e30-109">Pour plus de granularité, vous pouvez également créer des stratégies anti-hameçonnage personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="46e30-109">For greater granularity, you can also create custom anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="46e30-110">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="46e30-110">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="46e30-111">Les organisations Exchange Online boîtes aux lettres peuvent configurer des stratégies anti-hameçonnage dans le portail Microsoft 365 Defender ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46e30-111">Organizations with Exchange Online mailboxes can configure anti-phishing policies in the Microsoft 365 Defender portal or in Exchange Online PowerShell.</span></span> <span data-ttu-id="46e30-112">Les organisations EOP autonomes peuvent uniquement utiliser le portail Microsoft 365 Defender client.</span><span class="sxs-lookup"><span data-stu-id="46e30-112">Standalone EOP organizations can only use the Microsoft 365 Defender portal.</span></span>

<span data-ttu-id="46e30-113">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées disponibles dans Microsoft Defender pour Office 365, voir Configurer des stratégies [anti-hameçonnage](configure-mdo-anti-phishing-policies.md)dans Microsoft Defender pour Office 365 .</span><span class="sxs-lookup"><span data-stu-id="46e30-113">For information about creating and modifying the more advanced anti-phishing policies that are available in Microsoft Defender for Office 365, see [Configure anti-phishing policies in Microsoft Defender for Office 365](configure-mdo-anti-phishing-policies.md).</span></span>

<span data-ttu-id="46e30-114">Les éléments de base d’une stratégie anti-hameçonnage sont :</span><span class="sxs-lookup"><span data-stu-id="46e30-114">The basic elements of an anti-phishing policy are:</span></span>

- <span data-ttu-id="46e30-115">**La stratégie anti-hameçonnage :** spécifie les protections de hameçonnage à activer ou désactiver, ainsi que les actions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="46e30-115">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>
- <span data-ttu-id="46e30-116">**La règle anti-hameçonnage**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique) pour une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-116">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="46e30-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies anti-hameçonnage dans Microsoft 365 Defender portail :</span><span class="sxs-lookup"><span data-stu-id="46e30-117">The difference between these two elements isn't obvious when you manage anti-phishing policies in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="46e30-118">Lorsque vous créez une stratégie anti-hameçonnage, vous créez en fait une règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="46e30-118">When you create an anti-phishing policy, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="46e30-119">Lorsque vous modifiez une stratégie anti-hameçonnage, les paramètres liés au nom, à la priorité, activés ou désactivés, et aux filtres de destinataire modifient la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-119">When you modify an anti-phishing policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="46e30-120">Tous les autres paramètres modifient la stratégie anti-hameçonnage associée.</span><span class="sxs-lookup"><span data-stu-id="46e30-120">All other settings modify the associated anti-phish policy.</span></span>
- <span data-ttu-id="46e30-121">Lorsque vous supprimez une stratégie anti-hameçonnage, la règle anti-hameçonnage et la stratégie anti-hameçonnage associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="46e30-121">When you remove an anti-phishing policy, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="46e30-122">Dans Exchange Online PowerShell, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="46e30-122">In Exchange Online PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="46e30-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell pour configurer des stratégies [anti-hameçonnage](#use-exchange-online-powershell-to-configure-anti-phishing-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="46e30-123">For more information, see the [Use Exchange Online PowerShell to configure anti-phishing policies](#use-exchange-online-powershell-to-configure-anti-phishing-policies) section later in this article.</span></span>

<span data-ttu-id="46e30-124">Chaque organisation dispose d’une stratégie anti-hameçonnage intégrée nommée Office365 AntiPhish Default qui possède les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="46e30-124">Every organization has a built-in anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="46e30-125">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle anti-hameçonnage (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-125">The policy is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="46e30-126">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="46e30-126">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="46e30-127">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="46e30-127">Any custom policies that you create always have a higher priority.</span></span>
- <span data-ttu-id="46e30-128">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="46e30-128">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="46e30-129">Pour accroître l’efficacité de la protection anti-hameçonnage, vous pouvez créer des stratégies anti-hameçonnage personnalisées avec des paramètres plus stricts qui sont appliqués à des utilisateurs ou des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="46e30-129">To increase the effectiveness of anti-phishing protection, you can create custom anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="46e30-130">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="46e30-130">What do you need to know before you begin?</span></span>

- <span data-ttu-id="46e30-131">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="46e30-131">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="46e30-132">Pour aller directement à la page **anti-hameçonnage,** utilisez <https://security.microsoft.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="46e30-132">To go directly to the **Anti-phishing** page, use <https://security.microsoft.com/antiphishing>.</span></span>

- <span data-ttu-id="46e30-133">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="46e30-133">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

  <span data-ttu-id="46e30-134">Vous ne pouvez pas gérer les stratégies anti-hameçonnage dans EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="46e30-134">You can't manage anti-phishing policies in standalone EOP PowerShell.</span></span>

- <span data-ttu-id="46e30-135">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="46e30-135">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="46e30-136">Pour ajouter, modifier et supprimer des stratégies anti-hameçonnage,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="46e30-136">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="46e30-137">Pour accéder en lecture seule aux stratégies anti-hameçonnage,  vous  devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="46e30-137">For read-only access to anti-phishing policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="46e30-138">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="46e30-138">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="46e30-139">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="46e30-139">**Notes**:</span></span>

  - <span data-ttu-id="46e30-140">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="46e30-140">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="46e30-141">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="46e30-141">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="46e30-142">Le **groupe de rôles** Gestion de l’organisation en affichage seul [dans Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la <sup>\*</sup> fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="46e30-142">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature<sup>\*</sup>.</span></span>

- <span data-ttu-id="46e30-143">Pour obtenir nos paramètres recommandés pour les stratégies anti-hameçonnage, consultez les paramètres de stratégie [anti-hameçonnage EOP.](recommended-settings-for-eop-and-office365.md#eop-anti-phishing-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="46e30-143">For our recommended settings for anti-phishing policies, see [EOP anti-phishing policy settings](recommended-settings-for-eop-and-office365.md#eop-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="46e30-144">Autorisez jusqu’à 30 minutes d’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="46e30-144">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="46e30-145">Pour plus d’informations sur l’endroit où les stratégies anti-hameçonnage sont appliquées dans le pipeline de filtrage, voir Ordre et priorité de la [protection du courrier électronique.](how-policies-and-protections-are-combined.md)</span><span class="sxs-lookup"><span data-stu-id="46e30-145">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-anti-phishing-policies"></a><span data-ttu-id="46e30-146">Utiliser le portail Microsoft 365 Defender pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-146">Use the Microsoft 365 Defender portal to create anti-phishing policies</span></span>

<span data-ttu-id="46e30-147">La création d’une stratégie anti-hameçonnage personnalisée dans le portail Microsoft 365 Defender crée la règle anti-hameçonnage et la stratégie anti-hameçonnage associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="46e30-147">Creating a custom anti-phishing policy in the Microsoft 365 Defender portal creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="46e30-148">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-148">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-149">Dans la page **Anti-hameçonnage,** cliquez sur ![ Créer une icône ](../../media/m365-cc-sc-create-icon.png) **Créer.**</span><span class="sxs-lookup"><span data-stu-id="46e30-149">On the **Anti-phishing** page, click ![Create icon](../../media/m365-cc-sc-create-icon.png) **Create**.</span></span>

3. <span data-ttu-id="46e30-150">L’assistant d'application de stratégies s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="46e30-150">The policy wizard opens.</span></span> <span data-ttu-id="46e30-151">Dans la page **Nom de la** stratégie, configurez les paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="46e30-151">On the **Policy name** page, configure these settings:</span></span>
   - <span data-ttu-id="46e30-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>
   - <span data-ttu-id="46e30-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="46e30-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46e30-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="46e30-155">Dans la page **Utilisateurs, groupes et domaines** qui s’affiche, identifiez les destinataires internes auxquels la stratégie s’applique (conditions de destinataire) :</span><span class="sxs-lookup"><span data-stu-id="46e30-155">On the **Users, groups, and domains** page that appears, identify the internal recipients that the policy applies to (recipient conditions):</span></span>
   - <span data-ttu-id="46e30-156">**Utilisateurs** : boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="46e30-156">**Users**: The specified mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="46e30-157">**Groupes** : groupes de distribution, groupes de sécurité à extension messagerie ou groupes Microsoft 365 spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="46e30-157">**Groups**: The specified distribution groups, mail-enabled security groups, or Microsoft 365 Groups in your organization.</span></span>
   - <span data-ttu-id="46e30-158">**Domaines** : tous les destinataires des [domaines acceptés](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="46e30-158">**Domains**: All recipients in the specified [accepted domains](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) in your organization.</span></span>

   <span data-ttu-id="46e30-159">Cliquez dans la zone appropriée, commencez à taper une valeur et sélectionnez la valeur souhaitée dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="46e30-159">Click in the appropriate box, start typing a value, and select the value that you want from the results.</span></span> <span data-ttu-id="46e30-160">Répétez cette opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="46e30-160">Repeat this process as many times as necessary.</span></span> <span data-ttu-id="46e30-161">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="46e30-161">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="46e30-163">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="46e30-163">next to the value.</span></span>

   <span data-ttu-id="46e30-164">Pour les utilisateurs ou les groupes, vous pouvez utiliser la plupart des identificateurs (nom, nom d’affichage, alias, adresse e-mail, nom de compte, etc.), mais le nom d'affichage correspondant apparaît dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="46e30-164">For users or groups, you can use most identifiers (name, display name, alias, email address, account name, etc.), but the corresponding display name is shown in the results.</span></span> <span data-ttu-id="46e30-165">Pour les utilisateurs, entrez un astérisque (\*) seul pour afficher toutes les valeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="46e30-165">For users, enter an asterisk (\*) by itself to see all available values.</span></span>

   <span data-ttu-id="46e30-166">Plusieurs valeurs dans la même condition utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="46e30-166">Multiple values in the same condition use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="46e30-167">Des conditions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="46e30-167">Different conditions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   - <span data-ttu-id="46e30-168">**Exclure ces utilisateurs, groupes et domaines** : pour ajouter des exceptions pour les destinataires internes auxquels la stratégie s’applique (exceptions pour les destinataires), sélectionnez cette option et configurez les exceptions.</span><span class="sxs-lookup"><span data-stu-id="46e30-168">**Exclude these users, groups, and domains**: To add exceptions for the internal recipients that the policy applies to (recpient exceptions), select this option and configure the exceptions.</span></span> <span data-ttu-id="46e30-169">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="46e30-169">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="46e30-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46e30-170">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="46e30-171">Dans la page **de protection** & seuil de  hameçonnage qui s’affiche, utilisez la case à cocher Activer la veille contre l’usurpation d’informations pour activer ou désactiver l’usurpation d’informations.</span><span class="sxs-lookup"><span data-stu-id="46e30-171">On the **Phishing threshold & protection** page that appears, use the **Enable spoof intelligence** check box to turn spoof intelligence on or off.</span></span> <span data-ttu-id="46e30-172">La valeur par défaut est sur (sélectionné) et nous vous recommandons de la laisser.</span><span class="sxs-lookup"><span data-stu-id="46e30-172">The default value is on (selected), and we recommend that you leave it on.</span></span> <span data-ttu-id="46e30-173">Vous configurez l’action à prendre sur les messages usurpés bloqués sur la page suivante.</span><span class="sxs-lookup"><span data-stu-id="46e30-173">You configure the action to take on blocked spoofed messages on the next page.</span></span>

   <span data-ttu-id="46e30-174">Pour désactiver la veille contre l’usurpation d’informations, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="46e30-174">To turn off spoof intelligence, clear the check box.</span></span>

   > [!NOTE]
   > <span data-ttu-id="46e30-175">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’Microsoft 365 ; vous activez plutôt le filtrage amélioré pour les connecteurs.</span><span class="sxs-lookup"><span data-stu-id="46e30-175">You don't need to turn off anti-spoofing protection if your MX record doesn't point to Microsoft 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="46e30-176">Pour obtenir des instructions, voir [Filtrage amélioré pour les connecteurs dans Exchange Online](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="46e30-176">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   <span data-ttu-id="46e30-177">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46e30-177">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="46e30-178">Dans la page **Action** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="46e30-178">On the **Actions** page that appears, configure the following settings:</span></span>
   - <span data-ttu-id="46e30-179">**Si le message est détecté comme** usurpant l’usurpation : ce paramètre est disponible uniquement si vous avez sélectionné Activer la veille contre l’usurpation d’informations sur la page précédente. </span><span class="sxs-lookup"><span data-stu-id="46e30-179">**If message is detected as spoof**: This setting is available only if you selected **Enable spoof intelligence** on the previous page.</span></span> <span data-ttu-id="46e30-180">Sélectionnez l’une des actions suivantes dans la liste bas pour les messages provenant d’expéditeurs usurpés bloqués :</span><span class="sxs-lookup"><span data-stu-id="46e30-180">Select one of the following actions in the drop down list for messages from blocked spoofed senders:</span></span>
     - <span data-ttu-id="46e30-181">**Déplacer le message vers les dossiers Courrier indésirable des destinataires**</span><span class="sxs-lookup"><span data-stu-id="46e30-181">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="46e30-182">**Mettre le message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="46e30-182">**Quarantine the message**</span></span>

   - <span data-ttu-id="46e30-183">**Conseils de sécurité & indicateurs :**</span><span class="sxs-lookup"><span data-stu-id="46e30-183">**Safety tips & indicators**:</span></span>
     - <span data-ttu-id="46e30-184">**Afficher le premier contact conseil de sécurité**: pour plus d’informations, voir First contact [conseil de sécurité](set-up-anti-phishing-policies.md#first-contact-safety-tip).</span><span class="sxs-lookup"><span data-stu-id="46e30-184">**Show first contact safety tip**: For more information, see [First contact safety tip](set-up-anti-phishing-policies.md#first-contact-safety-tip).</span></span>
     - <span data-ttu-id="46e30-185">Afficher **(?)** pour les expéditeurs non authentifiés pour usurpation d’identité : ajoute un point d’interrogation à la photo de l’expéditeur dans la zone De de Outlook si le message ne passe pas les vérifications SPF ou DKIM et si le message ne passe pas <sup>\*</sup>  l’authentification DMARC ou [composite](email-validation-and-authentication.md#composite-authentication).</span><span class="sxs-lookup"><span data-stu-id="46e30-185">**Show (?) for unauthenticated senders for spoof**<sup>\*</sup>: Adds a question mark to the sender's photo in the From box in Outlook if the message does not pass SPF or DKIM checks **and** the message does not pass DMARC or [composite authentication](email-validation-and-authentication.md#composite-authentication).</span></span>
     - <span data-ttu-id="46e30-186">**Afficher la balise « via**» : ajoute une balise via (chris@contoso.com via fabrikam.com) à l’adresse De si elle est différente du domaine dans la signature DKIM ou <sup>\*</sup> l’adresse **MAIL FROM.**</span><span class="sxs-lookup"><span data-stu-id="46e30-186">**Show "via" tag**<sup>\*</sup>: Adds a via tag (chris@contoso.com via fabrikam.com) to the From address if it's different from the domain in the DKIM signature or the **MAIL FROM** address.</span></span>

     <span data-ttu-id="46e30-187">Pour activer un paramètre, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="46e30-187">To turn on a setting, select the check box.</span></span> <span data-ttu-id="46e30-188">Pour la désactiver, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="46e30-188">To turn it off, clear the check box.</span></span>

     <span data-ttu-id="46e30-189"><sup>\*</sup> Ce paramètre est disponible uniquement si vous avez sélectionné Activer la veille contre l’usurpation **d’informations** sur la page précédente.</span><span class="sxs-lookup"><span data-stu-id="46e30-189"><sup>\*</sup> This setting is available only if you selected **Enable spoof intelligence** on the previous page.</span></span> <span data-ttu-id="46e30-190">Pour plus d’informations, [voir Expéditeur non authentifié.](set-up-anti-phishing-policies.md#unauthenticated-sender)</span><span class="sxs-lookup"><span data-stu-id="46e30-190">For more information, see [Unauthenticated sender](set-up-anti-phishing-policies.md#unauthenticated-sender).</span></span>

   <span data-ttu-id="46e30-191">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46e30-191">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="46e30-192">Dans la page **Révision** qui s’affiche, passez en revue vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="46e30-192">On the **Review** page that appears, review your settings.</span></span> <span data-ttu-id="46e30-193">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="46e30-193">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="46e30-194">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="46e30-194">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="46e30-195">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="46e30-195">When you're finished, click **Submit**.</span></span>

8. <span data-ttu-id="46e30-196">Dans la page de confirmation qui s’affiche, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="46e30-196">On the confirmation page that appears, click **Done**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-anti-phishing-policies"></a><span data-ttu-id="46e30-197">Utiliser le portail Microsoft 365 Defender pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-197">Use the Microsoft 365 Defender portal to view anti-phishing policies</span></span>

1. <span data-ttu-id="46e30-198">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-198">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-199">Dans la page **Anti-hameçonnage,** les propriétés suivantes sont affichées dans la liste des stratégies :</span><span class="sxs-lookup"><span data-stu-id="46e30-199">On the **Anti-phishing** page, the following properties are displayed in the list of policies:</span></span>

   - <span data-ttu-id="46e30-200">**Name**</span><span class="sxs-lookup"><span data-stu-id="46e30-200">**Name**</span></span>
   - <span data-ttu-id="46e30-201">**État**</span><span class="sxs-lookup"><span data-stu-id="46e30-201">**Status**</span></span>
   - <span data-ttu-id="46e30-202">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="46e30-202">**Priority**</span></span>
   - <span data-ttu-id="46e30-203">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="46e30-203">**Last modified**</span></span>

3. <span data-ttu-id="46e30-204">Lorsque vous sélectionnez une stratégie en cliquant sur le nom, les paramètres de stratégie s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="46e30-204">When you select a policy by clicking on the name, the policy settings are displayed in a flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-anti-phishing-policies"></a><span data-ttu-id="46e30-205">Utiliser le portail Microsoft 365 Defender pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-205">Use the Microsoft 365 Defender portal to modify anti-phishing policies</span></span>

1. <span data-ttu-id="46e30-206">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-206">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-207">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="46e30-207">On the **Anti-phishing** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="46e30-208">Dans le menu volant des détails de stratégie qui s’affiche, sélectionnez **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="46e30-208">In the policy details flyout that appears, select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="46e30-209">Pour plus d’informations sur les paramètres, consultez la section Utiliser le portail Microsoft 365 Defender pour créer des stratégies [anti-hameçonnage](#use-the-microsoft-365-defender-portal-to-create-anti-phishing-policies) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="46e30-209">For more information about the settings, see the [Use the Microsoft 365 Defender portal to create anti-phishing policies](#use-the-microsoft-365-defender-portal-to-create-anti-phishing-policies) section earlier in this article.</span></span>  

   <span data-ttu-id="46e30-210">Pour la stratégie anti-hameçonnage par défaut, la section **Utilisateurs,** groupes et domaines n’est pas disponible (la stratégie s’applique à tout le monde) et vous ne pouvez pas renommer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-210">For the default anti-phishing policy, the **Users, groups, and domains** section isn't available (the policy applies to everyone), and you can't rename the policy.</span></span>

<span data-ttu-id="46e30-211">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="46e30-211">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-custom-anti-phishing-policies"></a><span data-ttu-id="46e30-212">Activer ou désactiver des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="46e30-212">Enable or disable custom anti-phishing policies</span></span>

<span data-ttu-id="46e30-213">Vous ne pouvez pas désactiver la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="46e30-213">You can't disable the default anti-phishing policy.</span></span>

1. <span data-ttu-id="46e30-214">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-214">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-215">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="46e30-215">On the **Anti-phishing** page, select a custom policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="46e30-216">En haut du menu volant des détails de stratégie qui s’affiche, vous verrez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="46e30-216">At the top of the policy details flyout that appears, you'll see one of the following values:</span></span>
   - <span data-ttu-id="46e30-217">**Stratégie désactivée** : pour activer la stratégie, cliquez sur ![Icône Activer](../../media/m365-cc-sc-turn-on-off-icon.png) **Activer**.</span><span class="sxs-lookup"><span data-stu-id="46e30-217">**Policy off**: To turn on the policy, click ![Turn on icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn on** .</span></span>
   - <span data-ttu-id="46e30-218">**Stratégie activée** : pour activer la stratégie, cliquez sur ![Icône Désactiver](../../media/m365-cc-sc-turn-on-off-icon.png) **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="46e30-218">**Policy on**: To turn off the policy, click ![Turn off icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn off**.</span></span>

4. <span data-ttu-id="46e30-219">Dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Activer** ou **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="46e30-219">In the confirmation dialog that appears, click **Turn on** or **Turn off**.</span></span>

5. <span data-ttu-id="46e30-220">Cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-220">Click **Close** in the policy details flyout.</span></span>

<span data-ttu-id="46e30-221">De retour sur la page principale de la stratégie, la valeur **État** de la stratégie sera **Activée** ou **Désactivée**.</span><span class="sxs-lookup"><span data-stu-id="46e30-221">Back on the main policy page, the **Status** value of the policy will be **On** or **Off**.</span></span>

### <a name="set-the-priority-of-custom-anti-phishing-policies"></a><span data-ttu-id="46e30-222">Définir la priorité des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="46e30-222">Set the priority of custom anti-phishing policies</span></span>

<span data-ttu-id="46e30-223">Par défaut, les stratégies anti-hameçonnage se voir donner une priorité basée sur l’ordre de leur création (les nouvelles stratégies sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="46e30-223">By default, anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="46e30-224">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="46e30-224">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="46e30-225">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="46e30-225">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="46e30-226">Pour modifier la priorité d’une stratégie, cliquez sur **Augmenter la priorité** ou **Diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro **Priorité** dans le Portail Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="46e30-226">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Microsoft 365 Defender portal).</span></span> <span data-ttu-id="46e30-227">La modification de la priorité d’une stratégie n’a de sens que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="46e30-227">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

 <span data-ttu-id="46e30-228">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="46e30-228">**Notes**:</span></span>

- <span data-ttu-id="46e30-229">Dans le portail Microsoft 365 Defender, vous ne pouvez modifier la priorité de la stratégie anti-hameçonnage qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="46e30-229">In the Microsoft 365 Defender portal, you can only change the priority of the anti-phishing policy after you create it.</span></span> <span data-ttu-id="46e30-230">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle anti-hameçonnage (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="46e30-230">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>
- <span data-ttu-id="46e30-231">Les stratégies anti-hameçonnage sont traitées dans l’ordre d’affichage (la première stratégie a la valeur Priority 0). </span><span class="sxs-lookup"><span data-stu-id="46e30-231">Anti-phishing policies are processed in the order that they're displayed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="46e30-232">La stratégie anti-hameçonnage par défaut a la valeur de priorité **La** plus faible et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="46e30-232">The default anti-phishing policy has the priority value **Lowest**, and you can't change it.</span></span>

1. <span data-ttu-id="46e30-233">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-233">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-234">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="46e30-234">On the **Anti-phishing** page, select a custom policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="46e30-235">En haut du menu volant détails de la stratégie qui s’affiche, vous verrez **Augmenter la priorité** ou **Diminuer la priorité** en fonction de la valeur de priorité actuelle et du nombre de stratégies personnalisées :</span><span class="sxs-lookup"><span data-stu-id="46e30-235">At the top of the policy details flyout that appears, you'll see **Increase priority** or **Decrease priority** based on the current priority value and the number of custom policies:</span></span>
   - <span data-ttu-id="46e30-236">La stratégie dont la valeur **de** priorité **est 0** ne dispose que de l’option Diminuer **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="46e30-236">The policy with the **Priority** value **0** has only the **Decrease priority** option available.</span></span>
   - <span data-ttu-id="46e30-237">La stratégie dont la valeur **de** priorité est la plus faible (par exemple, **3**) n’a que l’option Augmenter **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="46e30-237">The policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** option available.</span></span>
   - <span data-ttu-id="46e30-238">Si vous avez au moins trois stratégies, les stratégies  entre les valeurs de priorité les plus élevées et les plus faibles ont les options Augmenter la priorité et Diminuer **la** priorité disponibles.</span><span class="sxs-lookup"><span data-stu-id="46e30-238">If you have three or more policies, the policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** options available.</span></span>

   <span data-ttu-id="46e30-239">Cliquez sur l’![Icône Augmenter la priorité](../../media/m365-cc-sc-increase-icon.png) **Augmenter la priorité** ou ![Icône Diminuer la priorité](../../media/m365-cc-sc-decrease-icon.png) **Diminuer la priorité** pour modifier la valeur **Priorité**.</span><span class="sxs-lookup"><span data-stu-id="46e30-239">Click ![Increase priority icon](../../media/m365-cc-sc-increase-icon.png) **Increase priority** or ![Decrease priority icon](../../media/m365-cc-sc-decrease-icon.png) **Decrease priority** to change the **Priority** value.</span></span>

4. <span data-ttu-id="46e30-240">Lorsque vous avez terminé, cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="46e30-240">When you're finished, click **Close** in the policy details flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-custom-anti-phishing-policies"></a><span data-ttu-id="46e30-241">Utiliser le portail Microsoft 365 Defender pour supprimer des stratégies anti-hameçonnage personnalisées</span><span class="sxs-lookup"><span data-stu-id="46e30-241">Use the Microsoft 365 Defender portal to remove custom anti-phishing policies</span></span>

<span data-ttu-id="46e30-242">Lorsque vous utilisez le portail Microsoft 365 Defender pour supprimer une stratégie anti-hameçonnage personnalisée, la règle anti-hameçonnage et la stratégie anti-hameçonnage correspondante sont toutes deux supprimées.</span><span class="sxs-lookup"><span data-stu-id="46e30-242">When you use the Microsoft 365 Defender portal to remove a custom anti-phishing policy, the anti-phish rule and the corresponding anti-phish policy are both deleted.</span></span> <span data-ttu-id="46e30-243">Vous ne pouvez pas supprimer la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="46e30-243">You can't remove the default anti-phishing policy.</span></span>

1. <span data-ttu-id="46e30-244">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-244">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="46e30-245">Dans la page **Anti-hameçonnage,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="46e30-245">On the **Anti-phishing** page, select a custom policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="46e30-246">En haut du menu volant Détails de la stratégie qui s’affiche, cliquez sur l’![Icône Autres actions](../../media/m365-cc-sc-more-actions-icon.png) **Autres actions** \> ![Icône Supprimer la stratégie](../../media/m365-cc-sc-delete-icon.png) **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="46e30-246">At the top of the policy details flyout that appears, click ![More actions icon](../../media/m365-cc-sc-more-actions-icon.png) **More actions** \> ![Delete policy icon](../../media/m365-cc-sc-delete-icon.png) **Delete policy**.</span></span>

4. <span data-ttu-id="46e30-247">Dans la boîte de dialogue de confirmation qui s'affiche, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="46e30-247">In the confirmation dialog that appears, click **Yes**.</span></span>

## <a name="use-exchange-online-powershell-to-configure-anti-phishing-policies"></a><span data-ttu-id="46e30-248">Utiliser Exchange Online PowerShell pour configurer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-248">Use Exchange Online PowerShell to configure anti-phishing policies</span></span>

<span data-ttu-id="46e30-249">Comme décrit précédemment, une stratégie anti-hameçonnage se compose d’une stratégie anti-hameçonnage et d’une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-249">As previously described, an anti-phishing policy consists of an anti-phish policy and an anti-phish rule.</span></span>

<span data-ttu-id="46e30-250">Dans Exchange Online PowerShell, la différence entre les stratégies anti-hameçonnage et les règles anti-hameçonnage est évidente.</span><span class="sxs-lookup"><span data-stu-id="46e30-250">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="46e30-251">Vous gérez les stratégies anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishPolicy** et vous gérez les règles anti-hameçonnage à l’aide des cmdlets **\* -AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="46e30-251">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="46e30-252">Dans PowerShell, vous créez d’abord la stratégie anti-hameçonnage, puis vous créez la règle anti-hameçonnage qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="46e30-252">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="46e30-253">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie anti-hameçonnage et de la règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-253">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>
- <span data-ttu-id="46e30-254">Lorsque vous supprimez une stratégie anti-hameçonnage de PowerShell, la règle anti-hameçonnage correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="46e30-254">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

> [!NOTE]
> <span data-ttu-id="46e30-255">Les procédures PowerShell suivantes ne sont pas disponibles dans les organisations EOP autonomes utilisant Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46e30-255">The following PowerShell procedures aren't available in standalone EOP organizations using Exchange Online Protection PowerShell.</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="46e30-256">Utiliser PowerShell pour créer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-256">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="46e30-257">La création d’une stratégie anti-hameçonnage dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="46e30-257">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="46e30-258">Créez la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-258">Create the anti-phish policy.</span></span>
2. <span data-ttu-id="46e30-259">Créez la règle anti-hameçonnage qui spécifie la stratégie anti-hameçonnage à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="46e30-259">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="46e30-260">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="46e30-260">**Notes**:</span></span>

- <span data-ttu-id="46e30-261">Vous pouvez créer une règle anti-hameçonnage et lui attribuer une stratégie anti-hameçonnage existante et non dissociée.</span><span class="sxs-lookup"><span data-stu-id="46e30-261">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="46e30-262">Une règle anti-hameçonnage ne peut pas être associée à plusieurs stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-262">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="46e30-263">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies anti-hameçonnage dans PowerShell qui ne sont pas disponibles dans le portail Microsoft 365 Defender tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="46e30-263">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Microsoft 365 Defender portal until after you create the policy:</span></span>

  - <span data-ttu-id="46e30-264">Créez la stratégie comme désactivée (_activée_ sur la `$false` cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="46e30-264">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>
  - <span data-ttu-id="46e30-265">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-AntiPhishRule).**</span><span class="sxs-lookup"><span data-stu-id="46e30-265">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="46e30-266">Une nouvelle stratégie anti-hameçonnage que vous créez dans PowerShell n’est pas visible dans le portail Microsoft 365 Defender tant que vous n’avez pas attribué la stratégie à une règle anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="46e30-266">A new anti-phish policy that you create in PowerShell isn't visible in the Microsoft 365 Defender portal until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="46e30-267">Étape 1 : Utiliser PowerShell pour créer une stratégie anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-267">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="46e30-268">Pour créer une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-268">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-EnableSpoofIntelligence <$true | $false>] [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableUnauthenticatedSender <$true | $false>] [-EnableViaTag <$true | $false>]
```

<span data-ttu-id="46e30-269">Cet exemple crée une stratégie anti-hameçonnage nommée Research Quarantine avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="46e30-269">This example creates an anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="46e30-270">La description est la suivante : stratégie du service de recherche.</span><span class="sxs-lookup"><span data-stu-id="46e30-270">The description is: Research department policy.</span></span>
- <span data-ttu-id="46e30-271">Modifie l’action par défaut pour l’usurpation en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="46e30-271">Changes the default action for spoofing to Quarantine.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Research department policy" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="46e30-272">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishPolicy](/powershell/module/exchange/New-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="46e30-272">For detailed syntax and parameter information, see [New-AntiPhishPolicy](/powershell/module/exchange/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="46e30-273">Étape 2 : Utiliser PowerShell pour créer une règle anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-273">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="46e30-274">Pour créer une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-274">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="46e30-275">Cet exemple crée une règle anti-hameçonnage nommée Research Department avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="46e30-275">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="46e30-276">La règle est associée à la stratégie anti-hameçonnage nommée Research Quarantine.</span><span class="sxs-lookup"><span data-stu-id="46e30-276">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="46e30-277">La règle s’applique aux membres du groupe nommé Research Department.</span><span class="sxs-lookup"><span data-stu-id="46e30-277">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="46e30-278">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="46e30-278">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="46e30-279">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-AntiPhishRule](/powershell/module/exchange/New-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="46e30-279">For detailed syntax and parameter information, see [New-AntiPhishRule](/powershell/module/exchange/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="46e30-280">Utiliser PowerShell pour afficher les stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-280">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="46e30-281">Pour afficher les stratégies anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-281">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="46e30-282">Cet exemple renvoie une liste récapitulatif de toutes les stratégies anti-hameçonnage, ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="46e30-282">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="46e30-283">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie anti-hameçonnage nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="46e30-283">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="46e30-284">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishPolicy](/powershell/module/exchange/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="46e30-284">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](/powershell/module/exchange/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="46e30-285">Utiliser PowerShell pour afficher les règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-285">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="46e30-286">Pour afficher les règles anti-hameçonnage existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-286">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="46e30-287">Cet exemple renvoie une liste récapitulatif de toutes les règles anti-hameçonnage ainsi que les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="46e30-287">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="46e30-288">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="46e30-288">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="46e30-289">Cet exemple renvoie toutes les valeurs de propriété pour la règle anti-hameçonnage nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="46e30-289">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="46e30-290">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-AntiPhishRule](/powershell/module/exchange/Get-AntiPhishrule).</span><span class="sxs-lookup"><span data-stu-id="46e30-290">For detailed syntax and parameter information, see [Get-AntiPhishRule](/powershell/module/exchange/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="46e30-291">Utiliser PowerShell pour modifier des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-291">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="46e30-292">Outre les éléments suivants, les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell que lorsque vous créez une stratégie comme décrit à l’étape 1 : Utiliser PowerShell pour créer une stratégie [anti-hameçonnage](#step-1-use-powershell-to-create-an-anti-phish-policy) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="46e30-292">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create a policy as described in [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) earlier in this article.</span></span>

- <span data-ttu-id="46e30-293">Le _commutateur MakeDefault_ qui transforme la stratégie spécifiée en  stratégie par défaut (appliquée à tout le monde, toujours la priorité la plus faible et que vous ne pouvez pas supprimer) est disponible uniquement lorsque vous modifiez une stratégie anti-hameçonnage dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46e30-293">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>
- <span data-ttu-id="46e30-294">Vous ne pouvez pas renommer une stratégie anti-hameçonnage (la cmdlet **Set-AntiPhishPolicy** n’a pas de _paramètre Name)._</span><span class="sxs-lookup"><span data-stu-id="46e30-294">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="46e30-295">Lorsque vous renommez une stratégie anti-hameçonnage dans le portail Microsoft 365 Defender, vous renommez uniquement la règle _anti-hameçonnage._</span><span class="sxs-lookup"><span data-stu-id="46e30-295">When you rename an anti-phishing policy in the Microsoft 365 Defender portal, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="46e30-296">Pour modifier une stratégie anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-296">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="46e30-297">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishPolicy](/powershell/module/exchange/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="46e30-297">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](/powershell/module/exchange/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="46e30-298">Utiliser PowerShell pour modifier des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-298">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="46e30-299">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle anti-hameçonnage dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="46e30-299">The only setting that's not available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="46e30-300">Pour activer ou désactiver des règles anti-hameçonnage existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="46e30-300">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="46e30-301">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser PowerShell pour créer une section de règle [anti-hameçonnage](#step-2-use-powershell-to-create-an-anti-phish-rule) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="46e30-301">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this article.</span></span>

<span data-ttu-id="46e30-302">Pour modifier une règle anti-hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-302">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="46e30-303">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AntiPhishRule](/powershell/module/exchange/set-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="46e30-303">For detailed syntax and parameter information, see [Set-AntiPhishRule](/powershell/module/exchange/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="46e30-304">Utiliser PowerShell pour activer ou désactiver des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-304">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="46e30-305">L’activation ou la désactivation d’une règle anti-hameçonnage dans PowerShell active ou désactive l’ensemble de la stratégie anti-hameçonnage (la règle anti-hameçonnage et la stratégie anti-hameçonnage affectée).</span><span class="sxs-lookup"><span data-stu-id="46e30-305">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="46e30-306">Vous ne pouvez pas activer ou désactiver la stratégie anti-hameçonnage par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="46e30-306">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="46e30-307">Pour activer ou désactiver une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-307">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="46e30-308">Cet exemple désactive la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="46e30-308">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="46e30-309">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="46e30-309">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="46e30-310">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-AntiPhishRule](/powershell/module/exchange/enable-antiphishrule) et [Disable-AntiPhishRule](/powershell/module/exchange/disable-antiphishrule).</span><span class="sxs-lookup"><span data-stu-id="46e30-310">For detailed syntax and parameter information, see [Enable-AntiPhishRule](/powershell/module/exchange/enable-antiphishrule) and [Disable-AntiPhishRule](/powershell/module/exchange/disable-antiphishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="46e30-311">Utiliser PowerShell pour définir la priorité des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-311">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="46e30-p131">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle. La valeur la plus basse que vous pouvez définir dépend du nombre de règles. Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4. Tout changement de priorité d'une règle existante peut avoir un effet en cascade sur les autres règles. Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="46e30-p131">The highest priority value you can set on a rule is 0. The lowest value you can set depends on the number of rules. For example, if you have five rules, you can use the priority values 0 through 4. Changing the priority of an existing rule can have a cascading effect on other rules. For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="46e30-317">Pour définir la priorité d’une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-317">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="46e30-p132">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="46e30-p132">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="46e30-320">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="46e30-320">**Notes**:</span></span>

- <span data-ttu-id="46e30-321">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-AntiPhishRule.**</span><span class="sxs-lookup"><span data-stu-id="46e30-321">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>
- <span data-ttu-id="46e30-322">La stratégie anti-hameçonnage par défaut n’a pas de règle anti-hameçonnage correspondante et elle a toujours la valeur de priorité nonmodifiable La plus **faible**.</span><span class="sxs-lookup"><span data-stu-id="46e30-322">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="46e30-323">Utiliser PowerShell pour supprimer des stratégies anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-323">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="46e30-324">Lorsque vous utilisez PowerShell pour supprimer une stratégie anti-hameçonnage, la règle anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="46e30-324">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="46e30-325">Pour supprimer une stratégie anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-325">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="46e30-326">Cet exemple supprime la stratégie anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="46e30-326">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="46e30-327">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishPolicy](/powershell/module/exchange/Remove-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="46e30-327">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](/powershell/module/exchange/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="46e30-328">Utiliser PowerShell pour supprimer des règles anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="46e30-328">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="46e30-329">Lorsque vous utilisez PowerShell pour supprimer une règle anti-hameçonnage, la stratégie anti-hameçonnage correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="46e30-329">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="46e30-330">Pour supprimer une règle anti-hameçonnage dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="46e30-330">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="46e30-331">Cet exemple supprime la règle anti-hameçonnage nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="46e30-331">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="46e30-332">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-AntiPhishRule](/powershell/module/exchange/Remove-AntiPhishRule).</span><span class="sxs-lookup"><span data-stu-id="46e30-332">For detailed syntax and parameter information, see [Remove-AntiPhishRule](/powershell/module/exchange/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="46e30-333">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="46e30-333">How do you know these procedures worked?</span></span>

<span data-ttu-id="46e30-334">Pour vérifier que vous avez bien configuré les stratégies anti-hameçonnage dans EOP, faites l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="46e30-334">To verify that you've successfully configured anti-phishing policies in EOP, do any of the following steps:</span></span>

- <span data-ttu-id="46e30-335">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="46e30-335">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Anti-phishing**.</span></span> <span data-ttu-id="46e30-336">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="46e30-336">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="46e30-337">Pour afficher plus de détails, sélectionnez la stratégie dans la liste en cliquant sur le nom et en visualnant les détails dans le volant qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="46e30-337">To view more details, select the policy from the list by clicking on the name and viewing the details in the flyout that appears.</span></span>

- <span data-ttu-id="46e30-338">Dans Exchange Online PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante \<Name\> et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="46e30-338">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```
