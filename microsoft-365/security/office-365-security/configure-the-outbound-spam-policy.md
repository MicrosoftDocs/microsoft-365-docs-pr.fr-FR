---
title: Configurer le filtrage du courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à afficher, créer, modifier et supprimer des stratégies de courrier indésirable sortant dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6b7ba1e398466c448de37060db340c1d20cb1504
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50165762"
---
# <a name="configure-outbound-spam-filtering-in-eop"></a><span data-ttu-id="9acb8-103">Configurer le filtrage du courrier indésirable sortant dans EOP</span><span class="sxs-lookup"><span data-stu-id="9acb8-103">Configure outbound spam filtering in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="9acb8-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9acb8-104">**Applies to**</span></span>
- [<span data-ttu-id="9acb8-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="9acb8-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="9acb8-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="9acb8-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="9acb8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9acb8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="9acb8-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîte aux lettres Exchange Online, les messages électroniques sortants envoyés via EOP sont automatiquement vérifiés pour le courrier indésirable et l’activité d’envoi inhabituelle.</span><span class="sxs-lookup"><span data-stu-id="9acb8-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, outbound email messages that are sent through EOP are automatically checked for spam and unusual sending activity.</span></span>

<span data-ttu-id="9acb8-109">Le courrier indésirable sortant provenant d’un utilisateur de votre organisation indique généralement un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="9acb8-109">Outbound spam from a user in your organization typically indicates a compromised account.</span></span> <span data-ttu-id="9acb8-110">Les messages sortants suspects sont marqués comme courrier indésirable (quel que soit le niveau de confiance du courrier indésirable ou SCL) et sont acheminés via le pool de remise à risque élevé pour protéger la réputation du service [(c’est-à-dire,](high-risk-delivery-pool-for-outbound-messages.md) empêcher les serveurs de messagerie source Microsoft 365 des listes d’adresses IP bloqués).</span><span class="sxs-lookup"><span data-stu-id="9acb8-110">Suspicious outbound messages are marked as spam (regardless of the spam confidence level or SCL) and are routed through the [high-risk delivery pool](high-risk-delivery-pool-for-outbound-messages.md) to help protect the reputation of the service (that is, keep Microsoft 365 source email servers off of IP block lists).</span></span> <span data-ttu-id="9acb8-111">Les administrateurs sont automatiquement avertis de l’activité de courrier sortant suspecte et des utilisateurs bloqués via les stratégies [d’alerte.](../../compliance/alert-policies.md)</span><span class="sxs-lookup"><span data-stu-id="9acb8-111">Admins are automatically notified of suspicious outbound email activity and blocked users via [alert policies](../../compliance/alert-policies.md).</span></span>

<span data-ttu-id="9acb8-112">EOP utilise des stratégies de courrier indésirable sortant dans le cadre de la protection globale de votre organisation contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9acb8-112">EOP uses outbound spam policies as part of your organization's overall defense against spam.</span></span> <span data-ttu-id="9acb8-113">Pour plus d’informations, voir [Protection contre le courrier indésirable](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="9acb8-113">For more information, see [Anti-spam protection](anti-spam-protection.md).</span></span>

<span data-ttu-id="9acb8-114">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-114">Admins can view, edit, and configure (but not delete) the default outbound spam policy.</span></span> <span data-ttu-id="9acb8-115">Pour plus de granularité, vous pouvez également créer des stratégies de courrier indésirable sortant personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9acb8-115">For greater granularity, you can also create custom outbound spam policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="9acb8-116">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9acb8-116">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="9acb8-117">Vous pouvez configurer des stratégies de courrier indésirable sortant dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="9acb8-117">You can configure outbound spam policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

<span data-ttu-id="9acb8-118">Les éléments de base d’une stratégie de courrier indésirable sortant dans EOP sont :</span><span class="sxs-lookup"><span data-stu-id="9acb8-118">The basic elements of an outbound spam policy in EOP are:</span></span>

- <span data-ttu-id="9acb8-119">**La stratégie de filtrage du** courrier indésirable sortant : spécifie les actions pour les verdicts de filtrage du courrier indésirable sortant et les options de notification.</span><span class="sxs-lookup"><span data-stu-id="9acb8-119">**The outbound spam filter policy**: Specifies the actions for outbound spam filtering verdicts and the notification options.</span></span>
- <span data-ttu-id="9acb8-120">**La règle de filtrage du** courrier indésirable sortant : spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique) pour une stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-120">**The outbound spam filter rule**: Specifies the priority and recipient filters (who the policy applies to) for a outbound spam filter policy.</span></span>

<span data-ttu-id="9acb8-121">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez les polices de courrier indésirable sortant dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="9acb8-121">The difference between these two elements isn't obvious when you manage outbound spam polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="9acb8-122">Lorsque vous créez une stratégie, vous créez en fait une règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="9acb8-122">When you create a policy, you're actually creating a outbound spam filter rule and the associated outbound spam filter policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="9acb8-123">Lorsque vous modifiez une stratégie, les paramètres liés au nom, à la priorité, activé ou désactivé et aux filtres de destinataire modifient la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-123">When you modify a policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the outbound spam filter rule.</span></span> <span data-ttu-id="9acb8-124">Tous les autres paramètres modifient la stratégie de filtrage du courrier indésirable sortant associée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-124">All other settings modify the associated outbound spam filter policy.</span></span>
- <span data-ttu-id="9acb8-125">Lorsque vous supprimez une stratégie, la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="9acb8-125">When you remove a policy, the outbound spam filter rule and the associated outbound spam filter policy are removed.</span></span>

<span data-ttu-id="9acb8-126">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="9acb8-126">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="9acb8-127">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou [EOP PowerShell](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies) autonome pour configurer les stratégies de courrier indésirable sortant plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9acb8-127">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure outbound spam policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies) section later in this article.</span></span>

<span data-ttu-id="9acb8-128">Chaque organisation dispose d’une stratégie de courrier indésirable sortant intégrée nommée Default qui possède les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="9acb8-128">Every organization has a built-in outbound spam policy named Default that has these properties:</span></span>

- <span data-ttu-id="9acb8-129">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle de filtrage du courrier indésirable sortant (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-129">The policy is applied to all recipients in the organization, even though there's no outbound spam filter rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="9acb8-130">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="9acb8-130">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="9acb8-131">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée que la stratégie nommée Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-131">Any custom policies that you create always have a higher priority than the policy named Default.</span></span>
- <span data-ttu-id="9acb8-132">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-132">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="9acb8-133">Pour accroître l’efficacité du filtrage du courrier indésirable sortant, vous pouvez créer des stratégies de courrier indésirable sortant personnalisées avec des paramètres plus stricts qui sont appliqués à des utilisateurs ou des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9acb8-133">To increase the effectiveness of outbound spam filtering, you can create custom outbound spam policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9acb8-134">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9acb8-134">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9acb8-135">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="9acb8-135">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="9acb8-136">Pour accéder directement à la page **Paramètres anti-courrier indésirable**, utilisez <https://protection.office.com/antispam>.</span><span class="sxs-lookup"><span data-stu-id="9acb8-136">To go directly to the **Anti-spam settings** page, use <https://protection.office.com/antispam>.</span></span>

- <span data-ttu-id="9acb8-137">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="9acb8-137">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="9acb8-138">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9acb8-138">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9acb8-139">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="9acb8-139">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="9acb8-140">Pour ajouter, modifier et supprimer des stratégies de courrier  indésirable sortant, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="9acb8-140">To add, modify, and delete outbound spam policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="9acb8-141">Pour accéder en lecture seule aux stratégies de courrier  indésirable sortant, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="9acb8-141">For read-only access to outbound spam policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="9acb8-142">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9acb8-142">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="9acb8-143">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="9acb8-143">**Notes**:</span></span>

  - <span data-ttu-id="9acb8-144">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9acb8-144">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="9acb8-145">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="9acb8-145">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="9acb8-146">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9acb8-146">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="9acb8-147">Pour obtenir nos paramètres recommandés pour les stratégies de courrier indésirable sortant, consultez les paramètres de stratégie de filtrage du courrier indésirable sortant [EOP.](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="9acb8-147">For our recommended settings for outbound spam policies, see [EOP outbound spam filter policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings).</span></span>

- <span data-ttu-id="9acb8-148">Les [](../../compliance/alert-policies.md) stratégies d’alerte par défaut nommées Limite d’envoi de courrier électronique ont été **dépassées,** des modèles d’envoi de courrier suspects ont été détectés et l’utilisateur ne peut pas envoyer de courrier électronique envoie déjà des notifications par courrier électronique aux membres du groupe  **TenantAdmins** (Administrateurs globaux) concernant l’activité inhabituelle de courrier sortant et les **utilisateurs** bloqués en raison du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-148">The default [alert policies](../../compliance/alert-policies.md) named **Email sending limit exceeded**, **Suspicious email sending patterns detected**, and **User restricted from sending email** already send email notifications to members of the **TenantAdmins** (**Global admins**) group about unusual outbound email activity and blocked users due to outbound spam.</span></span> <span data-ttu-id="9acb8-149">Pour plus d’informations, [voir Vérifier les paramètres d’alerte pour les utilisateurs restreints.](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users)</span><span class="sxs-lookup"><span data-stu-id="9acb8-149">For more information, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span> <span data-ttu-id="9acb8-150">Nous vous recommandons d’utiliser ces stratégies d’alerte au lieu des options de notification dans les stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-150">We recommend that you use these alert policies instead of the the notification options in outbound spam policies.</span></span>

## <a name="use-the-security--compliance-center-to-create-outbound-spam-policies"></a><span data-ttu-id="9acb8-151">Utiliser le Centre de sécurité & conformité pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-151">Use the Security & Compliance Center to create outbound spam policies</span></span>

<span data-ttu-id="9acb8-152">La création d’une stratégie personnalisée de courrier indésirable sortant dans le Centre de sécurité & conformité crée la règle de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="9acb8-152">Creating a custom outbound spam policy in the Security & Compliance Center creates the spam filter rule and the associated spam filter policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="9acb8-153">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-153">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-154">Dans la page **Paramètres anti-courrier** indésirable, cliquez **sur Créer une stratégie sortante.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-154">On the **Anti-spam settings** page, click **Create an outbound policy**.</span></span>

3. <span data-ttu-id="9acb8-155">Dans la **stratégie de filtrage du** courrier indésirable sortant qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9acb8-155">In the **Outbound spam filter policy** fly out that opens, configure the following settings:</span></span>

   - <span data-ttu-id="9acb8-156">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-156">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="9acb8-157">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-157">**Description**: Enter an optional description for the policy.</span></span>

4. <span data-ttu-id="9acb8-158">(Facultatif) Développez la section **Notifications** pour configurer des utilisateurs supplémentaires devant recevoir des copies et des notifications de messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="9acb8-158">(Optional) Expand the **Notifications** section to configure additional users who should receive copies and notifications of suspicious outbound email messages:</span></span>

   - <span data-ttu-id="9acb8-159">**Envoyer une copie des messages** électroniques sortants suspects à des personnes spécifiques : ce paramètre ajoute les utilisateurs spécifiés en tant que destinataires Bcc aux messages sortants suspects.</span><span class="sxs-lookup"><span data-stu-id="9acb8-159">**Send a copy of suspicious outbound email messages to specific people**: This setting adds the specified users as Bcc recipients to the suspicious outbound messages.</span></span>

     > [!NOTE]
     > <span data-ttu-id="9acb8-160">Ce paramètre fonctionne uniquement dans la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-160">This setting only works in the default outbound spam policy.</span></span> <span data-ttu-id="9acb8-161">Elle ne fonctionne pas dans les stratégies de courrier indésirable sortant personnalisées que vous créez.</span><span class="sxs-lookup"><span data-stu-id="9acb8-161">It doesn't work in custom outbound spam policies that you create.</span></span>

     <span data-ttu-id="9acb8-162">Pour activer ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="9acb8-162">To enable this setting:</span></span>

     1. <span data-ttu-id="9acb8-163">Activez la case à cocher pour activer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="9acb8-163">Select the check box to enable the setting.</span></span>

     1. <span data-ttu-id="9acb8-164">Cliquez **sur Ajouter des personnes.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-164">Click **Add people**.</span></span> <span data-ttu-id="9acb8-165">Dans le **volant Ajouter ou supprimer des destinataires** qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="9acb8-165">In the **Add or remove recipients** flyout that appears:</span></span>

     1. <span data-ttu-id="9acb8-166">Entrez l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="9acb8-166">Enter the sender's email address.</span></span> <span data-ttu-id="9acb8-167">Vous pouvez spécifier plusieurs adresses e-mail séparées par des points-virgules (;) ou un destinataire par ligne.</span><span class="sxs-lookup"><span data-stu-id="9acb8-167">You can specify multiple email addresses separated by semicolons (;) or one recipient per line.</span></span>

     1. <span data-ttu-id="9acb8-168">Clic </span><span class="sxs-lookup"><span data-stu-id="9acb8-168">Click</span></span> ![Icône Ajouter](../../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) <span data-ttu-id="9acb8-170">pour ajouter les destinataires.</span><span class="sxs-lookup"><span data-stu-id="9acb8-170">to add the recipients.</span></span>

        <span data-ttu-id="9acb8-171">Répétez ces étapes autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9acb8-171">Repeat these steps as many times as necessary.</span></span>

        <span data-ttu-id="9acb8-172">Les destinataires que vous avez ajoutés apparaissent dans la section **Liste des** destinataires du volet volant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-172">The recipients you added appear in the **Recipient list** section on the flyout.</span></span> <span data-ttu-id="9acb8-173">Pour supprimer un destinataire, cliquez sur ![ Supprimer le bouton ](../../media/scc-remove-icon.png) .</span><span class="sxs-lookup"><span data-stu-id="9acb8-173">To delete a recipient, click ![Remove button](../../media/scc-remove-icon.png).</span></span>

     1. <span data-ttu-id="9acb8-174">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-174">When you're finished, click **Save**.</span></span>

        <span data-ttu-id="9acb8-175">Pour désactiver ce paramètre, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="9acb8-175">To disable this setting, clear the check box.</span></span>

   - <span data-ttu-id="9acb8-176">**Informez des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant**:</span><span class="sxs-lookup"><span data-stu-id="9acb8-176">**Notify specific people if a sender is blocked due to sending outbound spam**:</span></span>

     > [!IMPORTANT]
     >
     > - <span data-ttu-id="9acb8-177">Ce paramètre est en train d’être supprimé des stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-177">This setting is in the process of being deprecated from outbound spam policies.</span></span>
     >
     > - <span data-ttu-id="9acb8-178">La [](../../compliance/alert-policies.md) stratégie d’alerte par défaut nommée User **restricted from sending email** already sends email notifications to members of the **TenantAdmins** (**Global admins**) group when users are blocked due to exceeding the limits in the **Recipient Limits** section.</span><span class="sxs-lookup"><span data-stu-id="9acb8-178">The default [alert policy](../../compliance/alert-policies.md) named **User restricted from sending email** already sends email notifications to members of the **TenantAdmins** (**Global admins**) group when users are blocked due to exceeding the limits in the **Recipient Limits** section.</span></span> <span data-ttu-id="9acb8-179">**Nous vous recommandons vivement d’utiliser** la stratégie d’alerte plutôt que ce paramètre dans la stratégie de courrier indésirable sortant pour avertir les administrateurs et les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9acb8-179">**We strongly recommend that you use the alert policy rather than this setting in the outbound spam policy to notify admins and other users**.</span></span> <span data-ttu-id="9acb8-180">Pour obtenir des instructions, [voir Vérifier les paramètres d’alerte pour les utilisateurs restreints.](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users)</span><span class="sxs-lookup"><span data-stu-id="9acb8-180">For instructions, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span>

5. <span data-ttu-id="9acb8-181">(Facultatif) Développez la section **Limites des destinataires** pour configurer les limites et les actions pour les messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="9acb8-181">(Optional) Expand the **Recipient Limits** section to configure the limits and actions for suspicious outbound email messages:</span></span>

   > [!NOTE]
   > <span data-ttu-id="9acb8-182">Ces paramètres s’appliquent uniquement aux boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="9acb8-182">These settings are only applicable to cloud-based mailboxes.</span></span>

   - <span data-ttu-id="9acb8-183">**Nombre maximal de destinataires par utilisateur**</span><span class="sxs-lookup"><span data-stu-id="9acb8-183">**Maximum number of recipients per user**</span></span>

     <span data-ttu-id="9acb8-184">Une valeur valide est de 0 à 10 000.</span><span class="sxs-lookup"><span data-stu-id="9acb8-184">A valid value is 0 to 10000.</span></span> <span data-ttu-id="9acb8-185">La valeur par défaut est 0, ce qui signifie que les valeurs par défaut du service sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="9acb8-185">The default value is 0, which means the service defaults are used.</span></span> <span data-ttu-id="9acb8-186">Pour plus d’informations, voir [Limites d’envoi.](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1)</span><span class="sxs-lookup"><span data-stu-id="9acb8-186">For more information, see [Sending limits](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1).</span></span>

     - <span data-ttu-id="9acb8-187">**Limite horaire externe :** nombre maximal de destinataires externes par heure.</span><span class="sxs-lookup"><span data-stu-id="9acb8-187">**External hourly limit**: The maximum number of external recipients per hour.</span></span>

     - <span data-ttu-id="9acb8-188">**Limite horaire interne :** nombre maximal de destinataires internes par heure.</span><span class="sxs-lookup"><span data-stu-id="9acb8-188">**Internal hourly limit**: The maximum number of internal recipients per hour.</span></span>

     - <span data-ttu-id="9acb8-189">**Limite quotidienne**: nombre total maximal de destinataires par jour.</span><span class="sxs-lookup"><span data-stu-id="9acb8-189">**Daily limit**: The maximum total number of recipients per day.</span></span>

   - <span data-ttu-id="9acb8-190">**Action lorsqu’un utilisateur dépasse les limites** ci-dessus : configurez l’action à prendre lorsqu’une des **limites de destinataires** est dépassée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-190">**Action when a user exceeds the limits above**: Configure the action to take when any one of the **Recipient Limits** are exceeded.</span></span> <span data-ttu-id="9acb8-191">Pour toutes les actions, les  destinataires spécifiés dans l’utilisateur ne  peuvent pas envoyer de stratégie d’alerte de courrier électronique (et, désormais, redondants Notifier des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant dans la stratégie de courrier indésirable sortant reçoivent des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="9acb8-191">For all actions, the recipients specified in the **User restricted from sending email** alert policy (and in the now redundant **Notify specific people if a sender is blocked due to sending outbound spam** setting in the outbound spam policy receive email notifications.</span></span>

     - <span data-ttu-id="9acb8-192">**Empêchez l’utilisateur d’envoyer des messages jusqu’au jour suivant**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-192">**Restrict the user from sending mail till the following day**: This is the default value.</span></span> <span data-ttu-id="9acb8-193">Des notifications par courrier électronique sont envoyées et l’utilisateur ne pourra plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="9acb8-193">Email notifications are sent, and the user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="9acb8-194">Il n’existe aucun moyen pour l’administrateur de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="9acb8-194">There is no way for the admin to override this block.</span></span>

       - <span data-ttu-id="9acb8-195">L’alerte d’activité nommée **Utilisateur limité à l’envoi** de courriers électroniques avertit les administrateurs (par courrier électronique et sur la page Afficher **les alertes).**</span><span class="sxs-lookup"><span data-stu-id="9acb8-195">The activity alert named **User restricted from sending email** notifies admins (via email and on the **View alerts** page).</span></span>

       - <span data-ttu-id="9acb8-196">Tous les destinataires spécifiés dans la stratégie **Notifier** des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant dans la stratégie sont également avertis.</span><span class="sxs-lookup"><span data-stu-id="9acb8-196">Any recipients specified in the **Notify specific people if a sender is blocked due to sending outbound spam** setting in the policy are also notified.</span></span>

       - <span data-ttu-id="9acb8-197">L’utilisateur ne pourra plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="9acb8-197">The user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="9acb8-198">Il n’existe aucun moyen pour l’administrateur de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="9acb8-198">There is no way for the admin to override this block.</span></span>

     - <span data-ttu-id="9acb8-199">Empêcher l’utilisateur d’envoyer des messages électroniques : des notifications par courrier électronique sont envoyées, l’utilisateur est ajouté au portail [Utilisateurs  **restreints] <https://sip.protection.office.com/restrictedusers>** dans le Centre de sécurité & conformité et l’utilisateur ne peut pas envoyer de courrier tant qu’il n’a pas été supprimé du portail Utilisateurs restreints par un administrateur. Une fois qu’un administrateur a supprimé l’utilisateur de la liste, il ne sera plus restreint pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="9acb8-199">**Restrict the user from sending mail**: Email notifications are sent, the user is added to the **[Restricted Users]<https://sip.protection.office.com/restrictedusers>** portal in the Security & Compliance Center, and the user can't send email until they're removed from the **Restricted Users** portal by an admin. After an admin removes the user from the list, the user won't be restricted again for that day.</span></span> <span data-ttu-id="9acb8-200">Pour obtenir des instructions, consultez La suppression d’un utilisateur du portail Utilisateurs restreints [après l’envoi de courrier indésirable.](removing-user-from-restricted-users-portal-after-spam.md)</span><span class="sxs-lookup"><span data-stu-id="9acb8-200">For instructions, see [Removing a user from the Restricted Users portal after sending spam email](removing-user-from-restricted-users-portal-after-spam.md).</span></span>

     - <span data-ttu-id="9acb8-201">**Aucune action, alerte uniquement :** les notifications par courrier électronique sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="9acb8-201">**No action, alert only**: Email notifications are sent.</span></span>

6. <span data-ttu-id="9acb8-202">(Facultatif) Développez la section **De forwarding automatique** pour contrôler le forwarding automatique des messages électroniques par les utilisateurs vers des expéditeurs externes.</span><span class="sxs-lookup"><span data-stu-id="9acb8-202">(Optional) Expand **Automatic forwarding** section to control automatic email forwarding by users to external senders.</span></span> <span data-ttu-id="9acb8-203">Pour plus d’informations, voir [Control automatic external email forwarding in Microsoft 365](external-email-forwarding.md).</span><span class="sxs-lookup"><span data-stu-id="9acb8-203">For more information, see [Control automatic external email forwarding in Microsoft 365](external-email-forwarding.md).</span></span>

   > [!NOTE]
   >
   > - <span data-ttu-id="9acb8-204">Avant septembre 2020, ces paramètres sont disponibles mais ne sont pas appliqués.</span><span class="sxs-lookup"><span data-stu-id="9acb8-204">Before September 2020, these settings are available but not enforced.</span></span>
   >
   > - <span data-ttu-id="9acb8-205">Ces paramètres s’appliquent uniquement aux boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="9acb8-205">These settings apply only to cloud-based mailboxes.</span></span>
   >
   > - <span data-ttu-id="9acb8-206">Lorsque le forwarding automatique est désactivé, le destinataire reçoit une note de non-remise (également appelée NDR ou bounce message) si des expéditeurs externes envoient des courriers électroniques à une boîte aux lettres sur place.</span><span class="sxs-lookup"><span data-stu-id="9acb8-206">When automatic forwarding is disabled, the recipient will receive a non-delivery report (also known as an NDR or bounce message) if external senders send email to a mailbox that has forwarding in place.</span></span> <span data-ttu-id="9acb8-207">Si le message est envoyé  par un expéditeur interne et que la méthode de forwarding est le [forwarding](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) de boîte aux lettres (également appelé « _forwarding SMTP_», l’expéditeur interne reçoit la NDR.</span><span class="sxs-lookup"><span data-stu-id="9acb8-207">If the message is sent by an internal sender **and** the forwarding method is [mailbox forwarding](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) (also known as _SMTP forwarding_), the internal sender will get the NDR.</span></span> <span data-ttu-id="9acb8-208">L’expéditeur interne ne reçoit pas de rapport de non-rapport si le forwarding s’est produit en raison d’une règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9acb8-208">The internal sender does not get an NDR if the forwarding occurred due to an inbox rule.</span></span>

   <span data-ttu-id="9acb8-209">Les valeurs disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="9acb8-209">The available values are:</span></span>

   - <span data-ttu-id="9acb8-210">**Automatique - Contrôlé par le système**: permet au filtrage du courrier indésirable sortant de contrôler le transport automatique du courrier externe.</span><span class="sxs-lookup"><span data-stu-id="9acb8-210">**Automatic - System-controlled**: Allows outbound spam filtering to control automatic external email forwarding.</span></span> <span data-ttu-id="9acb8-211">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-211">This is the default value.</span></span>
   - <span data-ttu-id="9acb8-212">**On**: le forwarding automatique du courrier externe n’est pas désactivé par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-212">**On**: Automatic external email forwarding is not disabled by the policy.</span></span>
   - <span data-ttu-id="9acb8-213">**Désactivé**: tous les envois automatiques de courrier externe sont désactivés par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-213">**Off**: All automatic external email forwarding is disabled by the policy.</span></span>

7. <span data-ttu-id="9acb8-214">(Obligatoire) Développez la section **Appliqué à** pour identifier les expéditeurs internes à qui la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="9acb8-214">(Required) Expand the **Applied to** section to identify the internal senders that the policy applies to.</span></span>

    <span data-ttu-id="9acb8-215">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="9acb8-215">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="9acb8-216">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<sender1\>_ ou _\<sender2\>_).</span><span class="sxs-lookup"><span data-stu-id="9acb8-216">Multiple values of the same condition or exception use OR logic (for example, _\<sender1\>_ or _\<sender2\>_).</span></span> <span data-ttu-id="9acb8-217">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<sender1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="9acb8-217">Different conditions or exceptions use AND logic (for example, _\<sender1\>_ and _\<member of group 1\>_).</span></span>

    <span data-ttu-id="9acb8-218">Il est plus facile de cliquer sur **Ajouter une condition** trois fois pour afficher toutes les conditions disponibles.</span><span class="sxs-lookup"><span data-stu-id="9acb8-218">It's easiest to click **Add a condition** three times to see all of the available conditions.</span></span> <span data-ttu-id="9acb8-219">Vous pouvez cliquer sur le ![bouton Supprimer](../../media/scc-remove-icon.png) pour supprimer les conditions que vous ne voulez pas configurer.</span><span class="sxs-lookup"><span data-stu-id="9acb8-219">You can click ![Remove button](../../media/scc-remove-icon.png) to remove conditions that you don't want to configure.</span></span>

    - <span data-ttu-id="9acb8-220">**Le domaine de l’expéditeur** est : Spécifie les expéditeurs dans un ou plusieurs des domaines acceptés configurés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="9acb8-220">**The sender domain is**: Specifies senders in one or more of the configured accepted domains in the organization.</span></span> <span data-ttu-id="9acb8-221">Cliquez dans la zone **Ajouter un indicateur** pour afficher et sélectionner un domaine.</span><span class="sxs-lookup"><span data-stu-id="9acb8-221">Click in the **Add a tag** box to see and select a domain.</span></span> <span data-ttu-id="9acb8-222">Cliquez de nouveau sur la zone **Ajouter un indicateur** pour sélectionner d’autres domaines si plusieurs domaines sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="9acb8-222">Click again the **Add a tag** box to select additional domains if more than one domain is available.</span></span>

    - <span data-ttu-id="9acb8-223">**L’expéditeur est**: spécifie un ou plusieurs utilisateurs dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9acb8-223">**Sender is**: Specifies one or more users in your organization.</span></span> <span data-ttu-id="9acb8-224">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="9acb8-224">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="9acb8-225">Cliquez à nouveau **sur la zone Ajouter une** balise pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9acb8-225">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="9acb8-226">**L’expéditeur est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9acb8-226">**Sender is a member of**: Specifies one or more groups in your organization.</span></span> <span data-ttu-id="9acb8-227">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="9acb8-227">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="9acb8-228">Cliquez à nouveau **sur la zone Ajouter une** balise pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9acb8-228">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="9acb8-229">**Sauf si**: pour ajouter des exceptions à la règle, cliquez sur **Ajouter une condition** trois fois pour afficher toutes les exceptions disponibles.</span><span class="sxs-lookup"><span data-stu-id="9acb8-229">**Except if**: To add exceptions for the rule, click **Add a condition** three times to see all of the available exceptions.</span></span> <span data-ttu-id="9acb8-230">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="9acb8-230">The settings and behavior are exactly like the conditions.</span></span>

8. <span data-ttu-id="9acb8-231">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-231">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-view-outbound-spam-policies"></a><span data-ttu-id="9acb8-232">Utiliser le Centre de sécurité & conformité pour afficher les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-232">Use the Security & Compliance Center to view outbound spam policies</span></span>

1. <span data-ttu-id="9acb8-233">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-233">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-234">Dans la page **Paramètres anti-courrier** indésirable, cliquez sur Développer l’icône ![ pour développer une stratégie de courrier indésirable sortant ](../../media/scc-expand-icon.png) :</span><span class="sxs-lookup"><span data-stu-id="9acb8-234">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="9acb8-235">Stratégie par défaut nommée **Stratégie de filtrage du courrier indésirable sortant.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-235">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="9acb8-236">Une stratégie personnalisée que vous avez créée lorsque la valeur dans la colonne **Type** est **Stratégie personnalisée de courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-236">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="9acb8-237">Les paramètres de stratégie s’affichent dans les détails de stratégie étendus qui s’affichent, ou vous pouvez cliquer sur **Modifier la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-237">The policy settings are displayed in the expanded policy details that appear, or you can click **Edit policy**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-outbound-spam-policies"></a><span data-ttu-id="9acb8-238">Utiliser le Centre de sécurité & conformité pour modifier les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-238">Use the Security & Compliance Center to modify outbound spam policies</span></span>

1. <span data-ttu-id="9acb8-239">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-239">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-240">Dans la page **Paramètres anti-courrier** indésirable, cliquez sur Développer l’icône ![ pour développer une stratégie de courrier indésirable sortant ](../../media/scc-expand-icon.png) :</span><span class="sxs-lookup"><span data-stu-id="9acb8-240">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="9acb8-241">Stratégie par défaut nommée **Stratégie de filtrage du courrier indésirable sortant.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-241">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="9acb8-242">Une stratégie personnalisée que vous avez créée lorsque la valeur dans la colonne **Type** est **Stratégie personnalisée de courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-242">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="9acb8-243">Cliquez sur **Modifier une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-243">Click **Edit policy**.</span></span>

<span data-ttu-id="9acb8-244">Pour les stratégies de courrier indésirable sortant personnalisées, les paramètres disponibles dans le volant qui s’affiche sont identiques à ceux décrits dans la section Utiliser le Centre de sécurité [&](#use-the-security--compliance-center-to-create-outbound-spam-policies) conformité pour créer des stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-244">For custom outbound spam policies, the available settings in the flyout that appears are identical to those described in the [Use the Security & Compliance Center to create outbound spam policies](#use-the-security--compliance-center-to-create-outbound-spam-policies) section.</span></span>

<span data-ttu-id="9acb8-245">Pour la stratégie de courrier indésirable sortant par défaut nommée Stratégie de filtrage du courrier indésirable **sortant,** la **section** Appliqué à n’est pas disponible (la stratégie s’applique à tout le monde) et vous ne pouvez pas renommer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9acb8-245">For the default outbound spam policy named **Outbound spam filter policy**, the **Applied to** section isn't available (the policy applies to everyone), and you can't rename the policy.</span></span>

<span data-ttu-id="9acb8-246">Pour activer ou désactiver une stratégie, définir l’ordre de priorité de la stratégie ou configurer les notifications de mise en quarantaine de l’utilisateur final, voir les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9acb8-246">To enable or disable a policy, set the policy priority order, or configure the end-user quarantine notifications, see the following sections.</span></span>

### <a name="enable-or-disable-outbound-spam-policies"></a><span data-ttu-id="9acb8-247">Activer ou désactiver les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-247">Enable or disable outbound spam policies</span></span>

1. <span data-ttu-id="9acb8-248">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-248">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-249">Dans la page **Paramètres anti-courrier** indésirable, cliquez sur Développer l’icône pour développer une stratégie personnalisée que vous avez créée (la valeur dans la colonne Type est Stratégie personnalisée de courrier indésirable ![ ](../../media/scc-expand-icon.png) **sortant).** </span><span class="sxs-lookup"><span data-stu-id="9acb8-249">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand a custom policy that you created (the value in the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="9acb8-250">Dans les détails de la stratégie développée qui s’affichent, notez la valeur dans la colonne **Activé**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-250">In the expanded policy details that appear, notice the value in the **On** column.</span></span>

   <span data-ttu-id="9acb8-251">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="9acb8-251">Move the toggle to the left to disable the policy:</span></span> ![Désactiver](../../media/scc-toggle-off.png)

   <span data-ttu-id="9acb8-253">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="9acb8-253">Move the toggle to the right to enable the policy:</span></span> ![Activer](../../media/scc-toggle-on.png)

<span data-ttu-id="9acb8-255">Vous ne pouvez pas désactiver la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-255">You can't disable the default outbound spam policy.</span></span>

### <a name="set-the-priority-of-custom-outbound-spam-policies"></a><span data-ttu-id="9acb8-256">Définir la priorité des stratégies de courrier indésirable sortant personnalisées</span><span class="sxs-lookup"><span data-stu-id="9acb8-256">Set the priority of custom outbound spam policies</span></span>

<span data-ttu-id="9acb8-257">Par défaut, les stratégies de courrier indésirable sortant se voient donner une priorité basée sur l’ordre de leur création (les stratégies plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="9acb8-257">By default, outbound spam policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="9acb8-258">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="9acb8-258">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="9acb8-259">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-259">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="9acb8-260">Les stratégies de courrier indésirable sortant personnalisées sont affichées dans  l’ordre de traitement (la première stratégie a la valeur Priorité 0).</span><span class="sxs-lookup"><span data-stu-id="9acb8-260">Custom outbound spam policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="9acb8-261">La stratégie de courrier indésirable sortant par défaut nommée **Stratégie** de filtrage du courrier indésirable sortant a la valeur de priorité **La** plus faible et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="9acb8-261">The default outbound spam policy named **Outbound spam filter policy** has the priority value **Lowest**, and you can't change it.</span></span>

<span data-ttu-id="9acb8-262">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="9acb8-262">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="9acb8-263">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-263">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-264">Dans la page **Paramètres anti-courrier** indésirable, recherchez les stratégies dont la valeur dans la colonne **Type** est Stratégie personnalisée de courrier **indésirable sortant.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-264">On the **Anti-spam settings** page, find the policies where the value in the **Type** column is **Custom outbound spam policy**.</span></span> <span data-ttu-id="9acb8-265">Notez les valeurs de la colonne **Priorité** :</span><span class="sxs-lookup"><span data-stu-id="9acb8-265">Notice the values in the **Priority** column:</span></span>

   - <span data-ttu-id="9acb8-266">La stratégie personnalisée de courrier indésirable sortant avec la priorité la plus élevée a la valeur Flèche vers le ![ ](../../media/ITPro-EAC-DownArrowIcon.png) **bas 0**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-266">The custom outbound spam policy with the highest priority has the value ![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **0**.</span></span>

   - <span data-ttu-id="9acb8-267">La stratégie personnalisée de courrier indésirable sortant avec la priorité la plus faible a la valeur n flèche vers le haut (par exemple, icône flèche vers le ![ ](../../media/ITPro-EAC-UpArrowIcon.png)  ![ haut ](../../media/ITPro-EAC-UpArrowIcon.png) **3**).</span><span class="sxs-lookup"><span data-stu-id="9acb8-267">The custom outbound spam policy with the lowest priority has the value ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **3**).</span></span>

   - <span data-ttu-id="9acb8-268">Si vous avez trois stratégies de courrier indésirable sortant personnalisées ou plus, les stratégies entre la priorité la plus élevée et la plus basse ont des valeurs icône flèche vers le haut vers le bas icône flèche vers le bas ![ ](../../media/ITPro-EAC-UpArrowIcon.png)![ ](../../media/ITPro-EAC-DownArrowIcon.png) **n** (par exemple, icône flèche vers le haut vers le bas icône ![ ](../../media/ITPro-EAC-UpArrowIcon.png)![ ](../../media/ITPro-EAC-DownArrowIcon.png) **2**).</span><span class="sxs-lookup"><span data-stu-id="9acb8-268">If you have three or more custom outbound spam policies, the policies between the highest and lowest priority have values ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **2**).</span></span>

3. <span data-ttu-id="9acb8-269">Clic </span><span class="sxs-lookup"><span data-stu-id="9acb8-269">Click</span></span> ![Icône de flèche vers le haut](../../media/ITPro-EAC-UpArrowIcon.png) <span data-ttu-id="9acb8-271">ou</span><span class="sxs-lookup"><span data-stu-id="9acb8-271">or</span></span> ![Icône de flèche vers le bas](../../media/ITPro-EAC-DownArrowIcon.png) <span data-ttu-id="9acb8-273">pour déplacer la stratégie de courrier indésirable sortant personnalisée vers le haut ou vers le bas dans la liste de priorités.</span><span class="sxs-lookup"><span data-stu-id="9acb8-273">to move the custom outbound spam policy up or down in the priority list.</span></span>

## <a name="use-the-security--compliance-center-to-remove-outbound-spam-policies"></a><span data-ttu-id="9acb8-274">Utiliser le Centre de sécurité & conformité pour supprimer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-274">Use the Security & Compliance Center to remove outbound spam policies</span></span>

1. <span data-ttu-id="9acb8-275">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-275">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="9acb8-276">Dans la page **Paramètres anti-courrier** indésirable, cliquez sur Développer l’icône pour développer la stratégie personnalisée à supprimer (la colonne Type est stratégie personnalisée de courrier ![ ](../../media/scc-expand-icon.png) indésirable **sortant).** </span><span class="sxs-lookup"><span data-stu-id="9acb8-276">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand the custom policy that you want to delete (the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="9acb8-277">Dans les détails de la stratégie développée qui s’affichent, cliquez sur **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-277">In the expanded policy details that appear, click **Delete policy**.</span></span>

4. <span data-ttu-id="9acb8-278">Cliquez sur **Oui** lorsque la boîte de dialogue d’avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9acb8-278">Click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="9acb8-279">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-279">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies"></a><span data-ttu-id="9acb8-280">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-280">Use Exchange Online PowerShell or standalone EOP PowerShell to configure outbound spam policies</span></span>

<span data-ttu-id="9acb8-281">Comme décrit précédemment, une stratégie de courrier indésirable sortant se compose d’une stratégie de filtrage du courrier indésirable sortant et d’une règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-281">As previously described, an outbound spam policy consists of an outbound spam filter policy and an outbound spam filter rule.</span></span>

<span data-ttu-id="9acb8-282">Dans Exchange Online PowerShell ou EOP PowerShell autonome, la différence entre les stratégies de filtrage du courrier indésirable sortant et les règles de filtrage du courrier indésirable sortant est évidente.</span><span class="sxs-lookup"><span data-stu-id="9acb8-282">In Exchange Online PowerShell or standalone EOP PowerShell, the difference between outbound spam filter policies and outbound spam filter rules is apparent.</span></span> <span data-ttu-id="9acb8-283">Vous gérez les stratégies de filtrage du courrier indésirable sortant à l’aide des cmdlets **\* -HostedOutboundSpamFilterPolicy** et vous gérez les règles de filtrage du courrier indésirable sortant à l’aide des cmdlets **\* -HostedOutboundSpamFilterRule.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-283">You manage outbound spam filter policies by using the **\*-HostedOutboundSpamFilterPolicy** cmdlets, and you manage outbound spam filter rules by using the **\*-HostedOutboundSpamFilterRule** cmdlets.</span></span>

- <span data-ttu-id="9acb8-284">Dans PowerShell, vous créez d’abord la stratégie de filtrage du courrier indésirable sortant, puis vous créez la règle de filtrage du courrier indésirable sortant qui identifie la stratégie à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="9acb8-284">In PowerShell, you create the outbound spam filter policy first, then you create the outbound spam filter rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="9acb8-285">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de filtrage du courrier indésirable sortant et de la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-285">In PowerShell, you modify the settings in the outbound spam filter policy and the outbound spam filter rule separately.</span></span>
- <span data-ttu-id="9acb8-286">Lorsque vous supprimez une stratégie de filtrage du courrier indésirable sortant de PowerShell, la règle de filtrage du courrier indésirable sortant correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="9acb8-286">When you remove a outbound spam filter policy from PowerShell, the corresponding outbound spam filter rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-outbound-spam-policies"></a><span data-ttu-id="9acb8-287">Utiliser PowerShell pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-287">Use PowerShell to create outbound spam policies</span></span>

<span data-ttu-id="9acb8-288">La création d’une stratégie de courrier indésirable sortant dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="9acb8-288">Creating an outbound spam policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="9acb8-289">Créez la stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-289">Create the outbound spam filter policy.</span></span>
2. <span data-ttu-id="9acb8-290">Créez la règle de filtrage du courrier indésirable sortant qui spécifie la stratégie de filtrage du courrier indésirable sortant à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="9acb8-290">Create the outbound spam filter rule that specifies the outbound spam filter policy that the rule applies to.</span></span>

 <span data-ttu-id="9acb8-291">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="9acb8-291">**Notes**:</span></span>

- <span data-ttu-id="9acb8-292">Vous pouvez créer une règle de filtrage du courrier indésirable sortant et lui attribuer une stratégie de filtrage du courrier indésirable sortant existante, non dissociée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-292">You can create a new outbound spam filter rule and assign an existing, unassociated outbound spam filter policy to it.</span></span> <span data-ttu-id="9acb8-293">Une règle de filtrage du courrier indésirable sortant ne peut pas être associée à plusieurs stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="9acb8-293">An outbound spam filter rule can't be associated with more than one outbound spam filter policy.</span></span>

- <span data-ttu-id="9acb8-294">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de filtrage du courrier indésirable sortant dans PowerShell qui ne sont pas disponibles dans le Centre de sécurité & conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="9acb8-294">You can configure the following settings on new outbound spam filter policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="9acb8-295">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-HostedOutboundSpamFilterRule).**</span><span class="sxs-lookup"><span data-stu-id="9acb8-295">Create the new policy as disabled (_Enabled_ `$false` on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>
  - <span data-ttu-id="9acb8-296">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-HostedOutboundSpamFilterRule).**</span><span class="sxs-lookup"><span data-stu-id="9acb8-296">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>

- <span data-ttu-id="9acb8-297">Une nouvelle stratégie de filtrage du courrier indésirable sortant que vous créez dans PowerShell n’est pas visible dans le Centre de sécurité & conformité tant que vous n’avez pas attribué la stratégie à une règle de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9acb8-297">A new outbound spam filter policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a spam filter rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-outbound-spam-filter-policy"></a><span data-ttu-id="9acb8-298">Étape 1 : Utiliser PowerShell pour créer une stratégie de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-298">Step 1: Use PowerShell to create an outbound spam filter policy</span></span>

<span data-ttu-id="9acb8-299">Pour créer une stratégie de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-299">To create an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="9acb8-300">Cet exemple crée une stratégie de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9acb8-300">This example creates a new outbound spam filter policy named Contoso Executives with the following settings:</span></span>

- <span data-ttu-id="9acb8-301">Les limites de taux de destinataires sont limitées aux valeurs plus petites que les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="9acb8-301">The recipient rate limits are restricted to smaller values that the defaults.</span></span> <span data-ttu-id="9acb8-302">Pour plus d’informations, voir [Limites d’envoi dans les options Microsoft 365.](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options)</span><span class="sxs-lookup"><span data-stu-id="9acb8-302">For more information, see [Sending limits across Microsoft 365 options](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span></span>

- <span data-ttu-id="9acb8-303">Une fois l’une des limites atteinte, l’utilisateur ne peut plus envoyer de messages.</span><span class="sxs-lookup"><span data-stu-id="9acb8-303">After one of the limits is reached, the user is prevented from sending messages.</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "Contoso Executives" -RecipientLimitExternalPerHour 400 -RecipientLimitInternalPerHour 800 -RecipientLimitPerDay 800 -ActionWhenThresholdReached BlockUser
```

<span data-ttu-id="9acb8-304">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="9acb8-304">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-outbound-spam-filter-rule"></a><span data-ttu-id="9acb8-305">Étape 2 : Utiliser PowerShell pour créer une règle de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-305">Step 2: Use PowerShell to create an outbound spam filter rule</span></span>

<span data-ttu-id="9acb8-306">Pour créer une règle de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-306">To create an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "<RuleName>" -HostedOutboundSpamFilterPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="9acb8-307">Cet exemple crée une règle de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="9acb8-307">This example creates a new outbound spam filter rule named Contoso Executives with these settings:</span></span>

- <span data-ttu-id="9acb8-308">La stratégie de filtrage du courrier indésirable sortant nommée Cadres Contoso est associée à la règle.</span><span class="sxs-lookup"><span data-stu-id="9acb8-308">The outbound spam filter policy named Contoso Executives is associated with the rule.</span></span>

- <span data-ttu-id="9acb8-309">La règle s’applique aux membres du groupe nommé Groupe Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="9acb8-309">The rule applies to members of the group named Contoso Executives Group.</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "Contoso Executives" -HostedOutboundSpamFilterPolicy "Contoso Executives" -SentToMemberOf "Contoso Executives Group"
```

<span data-ttu-id="9acb8-310">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="9acb8-310">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-policies"></a><span data-ttu-id="9acb8-311">Utiliser PowerShell pour afficher les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-311">Use PowerShell to view outbound spam filter policies</span></span>

<span data-ttu-id="9acb8-312">Pour renvoyer une liste récapitulatif de toutes les stratégies de filtrage du courrier indésirable sortant, exécutez la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9acb8-312">To return a summary list of all outbound spam filter policies, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy
```

<span data-ttu-id="9acb8-313">Pour renvoyer des informations détaillées sur une stratégie de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-313">To return detailed information about a specific outbound spam filter policy, use the this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="9acb8-314">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie de filtrage du courrier indésirable sortant nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="9acb8-314">This example returns all the property values for the outbound spam filter policy named Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "Executives" | Format-List
```

<span data-ttu-id="9acb8-315">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="9acb8-315">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-rules"></a><span data-ttu-id="9acb8-316">Utiliser PowerShell pour afficher les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-316">Use PowerShell to view outbound spam filter rules</span></span>

<span data-ttu-id="9acb8-317">Pour afficher les règles de filtrage du courrier indésirable sortant existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-317">To view existing outbound spam filter rules, use the following syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled>]
```

<span data-ttu-id="9acb8-318">Pour renvoyer une liste récapitulatif de toutes les règles de filtrage du courrier indésirable sortant, exécutez la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9acb8-318">To return a summary list of all outbound spam filter rules, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule
```

<span data-ttu-id="9acb8-319">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9acb8-319">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -State Disabled
```

```PowerShell
Get-HostedOutboundSpamFilterRule -State Enabled
```

<span data-ttu-id="9acb8-320">Pour retourner des informations détaillées sur une règle de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-320">To return detailed information about a specific outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "<RuleName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="9acb8-321">Cet exemple renvoie toutes les valeurs de propriété pour la règle de filtrage du courrier indésirable sortant nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="9acb8-321">This example returns all the property values for the outbound spam filter rule named Contoso Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="9acb8-322">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="9acb8-322">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-policies"></a><span data-ttu-id="9acb8-323">Utiliser PowerShell pour modifier les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-323">Use PowerShell to modify outbound spam filter policies</span></span>

<span data-ttu-id="9acb8-324">Les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie de filtrage des programmes malveillants dans PowerShell que lorsque vous créez la stratégie comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) pour créer une section de stratégie de filtrage du courrier indésirable sortant plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9acb8-324">The same settings are available when you modify a malware filter policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an outbound spam filter policy](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) section earlier in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9acb8-325">Vous ne pouvez pas renommer une stratégie de filtrage du courrier indésirable sortant (la cmdlet **Set-HostedOutboundSpamFilterPolicy** n’a pas de _paramètre Name)._</span><span class="sxs-lookup"><span data-stu-id="9acb8-325">You can't rename an outbound spam filter policy (the **Set-HostedOutboundSpamFilterPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="9acb8-326">Lorsque vous renommez une stratégie de courrier indésirable sortant dans le Centre de sécurité & conformité, vous renommez uniquement la règle de filtrage du courrier _indésirable sortant._</span><span class="sxs-lookup"><span data-stu-id="9acb8-326">When you rename an outbound spam policy in the Security & Compliance Center, you're only renaming the outbound spam filter _rule_.</span></span>

<span data-ttu-id="9acb8-327">Pour modifier une stratégie de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-327">To modify an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="9acb8-328">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="9acb8-328">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-rules"></a><span data-ttu-id="9acb8-329">Utiliser PowerShell pour modifier les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-329">Use PowerShell to modify outbound spam filter rules</span></span>

<span data-ttu-id="9acb8-330">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-330">The only setting that isn't available when you modify an outbound spam filter rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="9acb8-331">Pour activer ou désactiver les règles de filtrage du courrier indésirable sortant existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="9acb8-331">To enable or disable existing outbound spam filter rules, see the next section.</span></span>

<span data-ttu-id="9acb8-332">Sinon, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9acb8-332">Otherwise, no additional settings are available when you modify an outbound spam filter rule in PowerShell.</span></span> <span data-ttu-id="9acb8-333">Les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) pour créer une section de règle de filtrage du courrier indésirable sortant plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9acb8-333">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an outbound spam filter rule](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) section earlier in this article.</span></span>

<span data-ttu-id="9acb8-334">Pour modifier une règle de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-334">To modify an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="9acb8-335">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="9acb8-335">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-outbound-spam-filter-rules"></a><span data-ttu-id="9acb8-336">Utiliser PowerShell pour activer ou désactiver les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-336">Use PowerShell to enable or disable outbound spam filter rules</span></span>

<span data-ttu-id="9acb8-337">L’activation ou la désactivation d’une règle de filtrage du courrier indésirable sortant dans PowerShell active ou désactive l’ensemble de la stratégie de courrier indésirable sortant (la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant affectée).</span><span class="sxs-lookup"><span data-stu-id="9acb8-337">Enabling or disabling an outbound spam filter rule in PowerShell enables or disables the whole outbound spam policy (the outbound spam filter rule and the assigned outbound spam filter policy).</span></span> <span data-ttu-id="9acb8-338">Vous ne pouvez pas activer ou désactiver la stratégie de courrier indésirable sortant par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="9acb8-338">You can't enable or disable the default outbound spam policy (it's always always applied to all recipients).</span></span>

<span data-ttu-id="9acb8-339">Pour activer ou désactiver une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-339">To enable or disable an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-HostedOutboundSpamFilterRule | Disable-HostedOutboundSpamFilterRule> -Identity "<RuleName>"
```

<span data-ttu-id="9acb8-340">Cet exemple désactive la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="9acb8-340">This example disables the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Disable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="9acb8-341">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="9acb8-341">This example enables same rule.</span></span>

```PowerShell
Enable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="9acb8-342">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/enable-hostedoutboundspamfilterrule) et [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/disable-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="9acb8-342">For detailed syntax and parameter information, see [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/enable-hostedoutboundspamfilterrule) and [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/disable-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-outbound-spam-filter-rules"></a><span data-ttu-id="9acb8-343">Utiliser PowerShell pour définir la priorité des règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-343">Use PowerShell to set the priority of outbound spam filter rules</span></span>

<span data-ttu-id="9acb8-344">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="9acb8-344">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="9acb8-345">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="9acb8-345">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="9acb8-346">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="9acb8-346">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="9acb8-347">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="9acb8-347">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="9acb8-348">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="9acb8-348">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="9acb8-349">Pour définir la priorité d’une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-349">To set the priority of an outbound spam filter rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="9acb8-p141">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="9acb8-p141">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "Marketing Department" -Priority 2
```

> [!NOTE]
>
> - <span data-ttu-id="9acb8-352">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-HostedOutboundSpamFilterRule.**</span><span class="sxs-lookup"><span data-stu-id="9acb8-352">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-HostedOutboundSpamFilterRule** cmdlet instead.</span></span>
>
> - <span data-ttu-id="9acb8-353">La stratégie de filtrage du courrier indésirable par défaut sortante n’a pas de règle de filtrage de courrier indésirable correspondante et elle a toujours la valeur de priorité nonmodifiable La plus **faible**.</span><span class="sxs-lookup"><span data-stu-id="9acb8-353">The outbound default spam filter policy doesn't have a corresponding spam filter rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-policies"></a><span data-ttu-id="9acb8-354">Utiliser PowerShell pour supprimer des stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-354">Use PowerShell to remove outbound spam filter policies</span></span>

<span data-ttu-id="9acb8-355">Lorsque vous utilisez PowerShell pour supprimer une stratégie de filtrage du courrier indésirable sortant, la règle de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-355">When you use PowerShell to remove an outbound spam filter policy, the corresponding outbound spam filter rule isn't removed.</span></span>

<span data-ttu-id="9acb8-356">Pour supprimer une stratégie de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-356">To remove an outbound spam filter policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="9acb8-357">Cet exemple supprime la stratégie de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="9acb8-357">This example removes the outbound spam filter policy named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "Marketing Department"
```

<span data-ttu-id="9acb8-358">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="9acb8-358">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-rules"></a><span data-ttu-id="9acb8-359">Utiliser PowerShell pour supprimer des règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="9acb8-359">Use PowerShell to remove outbound spam filter rules</span></span>

<span data-ttu-id="9acb8-360">Lorsque vous utilisez PowerShell pour supprimer une règle de filtrage du courrier indésirable sortant, la stratégie de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="9acb8-360">When you use PowerShell to remove an outbound spam filter rule, the corresponding outbound spam filter policy isn't removed.</span></span>

<span data-ttu-id="9acb8-361">Pour supprimer une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9acb8-361">To remove an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "<PolicyName>"
```

<span data-ttu-id="9acb8-362">Cet exemple supprime la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="9acb8-362">This example removes the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="9acb8-363">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="9acb8-363">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterrule).</span></span>

## <a name="for-more-information"></a><span data-ttu-id="9acb8-364">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="9acb8-364">For more information</span></span>

[<span data-ttu-id="9acb8-365">Supprimer les utilisateurs bloqués du portail des utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="9acb8-365">Remove blocked users from the Restricted Users portal</span></span>](removing-user-from-restricted-users-portal-after-spam.md)

[<span data-ttu-id="9acb8-366">Pool de remise à haut risque pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="9acb8-366">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="9acb8-367">Forum Aux Questions sur la protection anti-courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="9acb8-367">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)

[<span data-ttu-id="9acb8-368">Rapport des messages transférés automatiquement</span><span class="sxs-lookup"><span data-stu-id="9acb8-368">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)
