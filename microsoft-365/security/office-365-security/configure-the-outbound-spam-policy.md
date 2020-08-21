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
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à afficher, créer, modifier et supprimer des stratégies de courrier indésirable sortant dans Exchange Online Protection (EOP).
ms.openlocfilehash: 530c1af9b7802be6073f19331ce7f6a20bdb2668
ms.sourcegitcommit: 260bbb93bbda62db9e88c021ccccfa75ac39a32e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "46845977"
---
# <a name="configure-outbound-spam-filtering-in-eop"></a><span data-ttu-id="47a73-103">Configurer le filtrage du courrier indésirable sortant dans EOP</span><span class="sxs-lookup"><span data-stu-id="47a73-103">Configure outbound spam filtering in EOP</span></span>

<span data-ttu-id="47a73-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, les messages électroniques sortants envoyés via EOP sont automatiquement vérifiés pour le courrier indésirable et l’envoi inhabituel.</span><span class="sxs-lookup"><span data-stu-id="47a73-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, outbound email messages that are sent through EOP are automatically checked for spam and unusual sending activity.</span></span>

<span data-ttu-id="47a73-105">Le courrier indésirable sortant d’un utilisateur de votre organisation indique généralement un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="47a73-105">Outbound spam from a user in your organization typically indicates a compromised account.</span></span> <span data-ttu-id="47a73-106">Les messages sortants suspects sont marqués comme courrier indésirable (quel que soit le seuil de probabilité de courrier indésirable ou SCL) et sont acheminés via le [pool de remise à haut risque](high-risk-delivery-pool-for-outbound-messages.md) afin de protéger la réputation du service (c’est-à-dire maintenir les serveurs de messagerie source Microsoft 365 hors des listes d’adresses IP bloquées).</span><span class="sxs-lookup"><span data-stu-id="47a73-106">Suspicious outbound messages are marked as spam (regardless of the spam confidence level or SCL) and are routed through the [high-risk delivery pool](high-risk-delivery-pool-for-outbound-messages.md) to help protect the reputation of the service (that is, keep Microsoft 365 source email servers off of IP block lists).</span></span> <span data-ttu-id="47a73-107">Les administrateurs sont automatiquement informés de l’activité e-mail sortante suspecte et des utilisateurs bloqués via des [stratégies d’alerte](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="47a73-107">Admins are automatically notified of suspicious outbound email activity and blocked users via [alert policies](../../compliance/alert-policies.md).</span></span>

<span data-ttu-id="47a73-108">EOP utilise des stratégies de courrier indésirable sortant dans le cadre de la protection globale de votre organisation contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="47a73-108">EOP uses outbound spam policies as part of your organization's overall defense against spam.</span></span> <span data-ttu-id="47a73-109">Pour plus d’informations, voir [Protection contre le courrier indésirable](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="47a73-109">For more information, see [Anti-spam protection](anti-spam-protection.md).</span></span>

<span data-ttu-id="47a73-110">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-110">Admins can view, edit, and configure (but not delete) the default outbound spam policy.</span></span> <span data-ttu-id="47a73-111">Pour une granularité accrue, vous pouvez également créer des stratégies de courrier indésirable sortant personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="47a73-111">For greater granularity, you can also create custom outbound spam policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="47a73-112">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="47a73-112">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="47a73-113">Vous pouvez configurer des stratégies de courrier indésirable sortant dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome EOP pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="47a73-113">You can configure outbound spam policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

<span data-ttu-id="47a73-114">Les éléments de base d’une stratégie de courrier indésirable sortant dans EOP sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-114">The basic elements of an outbound spam policy in EOP are:</span></span>

- <span data-ttu-id="47a73-115">**Stratégie de filtrage du courrier indésirable sortant**: spécifie les actions pour le filtrage du courrier indésirable sortant et les options de notification.</span><span class="sxs-lookup"><span data-stu-id="47a73-115">**The outbound spam filter policy**: Specifies the actions for outbound spam filtering verdicts and the notification options.</span></span>
- <span data-ttu-id="47a73-116">**Règle de filtrage du courrier indésirable sortant**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-116">**The outbound spam filter rule**: Specifies the priority and recipient filters (who the policy applies to) for a outbound spam filter policy.</span></span>

<span data-ttu-id="47a73-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de courrier indésirable sortant dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="47a73-117">The difference between these two elements isn't obvious when you manage outbound spam polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="47a73-118">Lorsque vous créez une stratégie, vous créez en réalité une règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="47a73-118">When you create a policy, you're actually creating a outbound spam filter rule and the associated outbound spam filter policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="47a73-119">Lorsque vous modifiez une stratégie, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-119">When you modify a policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the outbound spam filter rule.</span></span> <span data-ttu-id="47a73-120">Tous les autres paramètres modifient la stratégie de filtrage du courrier indésirable sortant associée.</span><span class="sxs-lookup"><span data-stu-id="47a73-120">All other settings modify the associated outbound spam filter policy.</span></span>
- <span data-ttu-id="47a73-121">Lorsque vous supprimez une stratégie, la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="47a73-121">When you remove a policy, the outbound spam filter rule and the associated outbound spam filter policy are removed.</span></span>

<span data-ttu-id="47a73-122">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="47a73-122">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="47a73-123">Pour plus d’informations, reportez-vous à la section [utiliser Exchange Online PowerShell or standalone EOP PowerShell pour configurer des stratégies de courrier indésirable sortant](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="47a73-123">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure outbound spam policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies) section later in this topic.</span></span>

<span data-ttu-id="47a73-124">Chaque organisation dispose d’une stratégie de courrier indésirable sortante intégrée nommée par défaut qui possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="47a73-124">Every organization has a built-in outbound spam policy named Default that has these properties:</span></span>

- <span data-ttu-id="47a73-125">La stratégie est appliquée à tous les destinataires de l’organisation, même si aucune règle de filtrage du courrier indésirable sortant (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-125">The policy is applied to all recipients in the organization, even though there's no outbound spam filter rule (recipient filters) associated with the policy.</span></span>
- <span data-ttu-id="47a73-126">La stratégie a la valeur de priorité personnalisée la **plus petite**, que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="47a73-126">The policy has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="47a73-127">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée que la stratégie nommée Par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-127">Any custom policies that you create always have a higher priority than the policy named Default.</span></span>
- <span data-ttu-id="47a73-128">La stratégie est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-128">The policy is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="47a73-129">Pour accroître l’efficacité du filtrage du courrier indésirable sortant, vous pouvez créer des stratégies de courrier indésirable sortant personnalisées avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="47a73-129">To increase the effectiveness of outbound spam filtering, you can create custom outbound spam policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="47a73-130">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="47a73-130">What do you need to know before you begin?</span></span>

- <span data-ttu-id="47a73-131">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="47a73-131">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="47a73-132">Pour accéder directement à la page **Paramètres anti-courrier indésirable**, utilisez <https://protection.office.com/antispam>.</span><span class="sxs-lookup"><span data-stu-id="47a73-132">To go directly to the **Anti-spam settings** page, use <https://protection.office.com/antispam>.</span></span>

- <span data-ttu-id="47a73-133">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="47a73-133">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="47a73-134">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="47a73-134">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="47a73-135">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="47a73-135">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="47a73-136">Pour ajouter, modifier et supprimer des stratégies de courrier indésirable sortant, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-136">To add, modify, and delete outbound spam policies, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="47a73-137">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="47a73-137">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="47a73-138">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="47a73-138">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="47a73-139">Pour un accès en lecture seule aux stratégies de courrier indésirable sortant, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-139">For read-only access to outbound spam policies, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="47a73-140">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="47a73-140">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="47a73-141">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="47a73-141">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="47a73-142">Pour connaître les paramètres recommandés pour les stratégies de courrier indésirable sortant, voir [EOP Outbound Outbound Filter Policy Settings](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="47a73-142">For our recommended settings for outbound spam policies, see [EOP outbound spam filter policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings).</span></span>

- <span data-ttu-id="47a73-143">Les [stratégies d’alerte](../../compliance/alert-policies.md) par défaut nommées limite d’envoi de **courrier électronique sont dépassées**, des **modèles de courrier électronique suspects détectés**et l’utilisateur ne peut pas envoyer **de courriers** électroniques aux membres du groupe **TenantAdmins** (**administrateurs globaux**) à propos de l’activité de courrier électronique sortant inhabituel et des utilisateurs bloqués en raison du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-143">The default [alert policies](../../compliance/alert-policies.md) named **Email sending limit exceeded**, **Suspicious email sending patterns detected**, and **User restricted from sending email** already send email notifications to members of the **TenantAdmins** (**Global admins**) group about unusual outbound email activity and blocked users due to outbound spam.</span></span> <span data-ttu-id="47a73-144">Pour plus d’informations, consultez [la rubrique vérifier les paramètres d’alerte pour les utilisateurs restreints](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span><span class="sxs-lookup"><span data-stu-id="47a73-144">For more information, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span> <span data-ttu-id="47a73-145">Nous vous recommandons d’utiliser ces stratégies d’alerte à la place des options de notification dans les stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-145">We recommend that you use these alert policies instead of the the notification options in outbound spam policies.</span></span>

## <a name="use-the-security--compliance-center-to-create-outbound-spam-policies"></a><span data-ttu-id="47a73-146">Utiliser le centre de sécurité & conformité pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-146">Use the Security & Compliance Center to create outbound spam policies</span></span>

<span data-ttu-id="47a73-147">La création d’une stratégie de courrier indésirable sortant personnalisé dans le centre de sécurité & conformité crée la règle de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="47a73-147">Creating a custom outbound spam policy in the Security & Compliance Center creates the spam filter rule and the associated spam filter policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="47a73-148">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-148">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-149">Dans la page **paramètres du blocage du courrier indésirable** , cliquez sur **créer une stratégie sortante**.</span><span class="sxs-lookup"><span data-stu-id="47a73-149">On the **Anti-spam settings** page, click **Create an outbound policy**.</span></span>

3. <span data-ttu-id="47a73-150">Dans la **stratégie de filtrage du courrier indésirable sortant** qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-150">In the **Outbound spam filter policy** fly out that opens, configure the following settings:</span></span>

   - <span data-ttu-id="47a73-151">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-151">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="47a73-152">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-152">**Description**: Enter an optional description for the policy.</span></span>

4. <span data-ttu-id="47a73-153">Module Développez la section **notifications** pour configurer des utilisateurs supplémentaires qui doivent recevoir des copies et des notifications de messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="47a73-153">(Optional) Expand the **Notifications** section to configure additional users who should receive copies and notifications of suspicious outbound email messages:</span></span>

   - <span data-ttu-id="47a73-154">**Envoyer une copie des messages électroniques sortants suspects à des personnes spécifiques**: ce paramètre ajoute les utilisateurs spécifiés en tant que destinataires CCI aux messages sortants suspects.</span><span class="sxs-lookup"><span data-stu-id="47a73-154">**Send a copy of suspicious outbound email messages to specific people**: This setting adds the specified users as Bcc recipients to the suspicious outbound messages.</span></span>

     > [!NOTE]
     > <span data-ttu-id="47a73-155">Ce paramètre ne fonctionne que dans le cadre de la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-155">This setting only works in the default outbound spam policy.</span></span> <span data-ttu-id="47a73-156">Il ne fonctionne pas dans les stratégies de courrier indésirable sortant personnalisées que vous créez.</span><span class="sxs-lookup"><span data-stu-id="47a73-156">It doesn't work in custom outbound spam policies that you create.</span></span>

     <span data-ttu-id="47a73-157">Pour activer ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="47a73-157">To enable this setting:</span></span>

     1. <span data-ttu-id="47a73-158">Activez la case à cocher pour activer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="47a73-158">Select the check box to enable the setting.</span></span>

     1. <span data-ttu-id="47a73-159">Cliquez sur **Ajouter des personnes**.</span><span class="sxs-lookup"><span data-stu-id="47a73-159">Click **Add people**.</span></span> <span data-ttu-id="47a73-160">Dans la fenêtre mobile **Ajouter ou supprimer des destinataires** qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="47a73-160">In the **Add or remove recipients** flyout that appears:</span></span>

     1. <span data-ttu-id="47a73-161">Entrez l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="47a73-161">Enter the sender's email address.</span></span> <span data-ttu-id="47a73-162">Vous pouvez spécifier plusieurs adresses de messagerie séparées par des points-virgules (;) ou un destinataire par ligne.</span><span class="sxs-lookup"><span data-stu-id="47a73-162">You can specify multiple email addresses separated by semicolons (;) or one recipient per line.</span></span>

     1. <span data-ttu-id="47a73-163">Clic </span><span class="sxs-lookup"><span data-stu-id="47a73-163">Click</span></span> ![Icône Ajouter](../../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) <span data-ttu-id="47a73-165">pour ajouter les destinataires.</span><span class="sxs-lookup"><span data-stu-id="47a73-165">to add the recipients.</span></span>

        <span data-ttu-id="47a73-166">Répétez ces étapes autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="47a73-166">Repeat these steps as many times as necessary.</span></span>

        <span data-ttu-id="47a73-167">Les destinataires que vous avez ajoutés apparaissent dans la section **liste des destinataires** du menu volant.</span><span class="sxs-lookup"><span data-stu-id="47a73-167">The recipients you added appear in the **Recipient list** section on the flyout.</span></span> <span data-ttu-id="47a73-168">Pour supprimer un destinataire, cliquez sur le ![ bouton supprimer ](../../media/scc-remove-icon.png) .</span><span class="sxs-lookup"><span data-stu-id="47a73-168">To delete a recipient, click ![Remove button](../../media/scc-remove-icon.png).</span></span>

     1. <span data-ttu-id="47a73-169">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="47a73-169">When you're finished, click **Save**.</span></span>

        <span data-ttu-id="47a73-170">Pour désactiver ce paramètre, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="47a73-170">To disable this setting, clear the check box.</span></span>

   - <span data-ttu-id="47a73-171">**Informer des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant**:</span><span class="sxs-lookup"><span data-stu-id="47a73-171">**Notify specific people if a sender is blocked due to sending outbound spam**:</span></span>

     > [!IMPORTANT]
     >
     > - <span data-ttu-id="47a73-172">Ce paramètre est en cours d’arrêt des stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-172">This setting is in the process of being deprecated from outbound spam policies.</span></span>
     >
     > - <span data-ttu-id="47a73-173">La [stratégie d’alerte](../../compliance/alert-policies.md) par défaut nommée **User Restricted from sending email** envoie déjà des notifications par courrier électronique aux membres du groupe **TenantAdmins** (**administrateurs globaux**) lorsque les utilisateurs sont bloqués en raison du dépassement des limites de la section **limites des destinataires** .</span><span class="sxs-lookup"><span data-stu-id="47a73-173">The default [alert policy](../../compliance/alert-policies.md) named **User restricted from sending email** already sends email notifications to members of the **TenantAdmins** (**Global admins**) group when users are blocked due to exceeding the limits in the **Recipient Limits** section.</span></span> <span data-ttu-id="47a73-174">**Nous vous recommandons vivement d’utiliser la stratégie d’alerte au lieu de ce paramètre dans la stratégie anti-courrier indésirable sortant pour avertir les administrateurs et les autres utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="47a73-174">**We strongly recommend that you use the alert policy rather than this setting in the outbound spam policy to notify admins and other users**.</span></span> <span data-ttu-id="47a73-175">Pour obtenir des instructions, consultez [la rubrique vérifier les paramètres d’alerte pour les utilisateurs restreints](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span><span class="sxs-lookup"><span data-stu-id="47a73-175">For instructions, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span>

5. <span data-ttu-id="47a73-176">Module Développez la section **limites des destinataires** pour configurer les limites et les actions pour les messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="47a73-176">(Optional) Expand the **Recipient Limits** section to configure the limits and actions for suspicious outbound email messages:</span></span>

   > [!NOTE]
   > <span data-ttu-id="47a73-177">Ces paramètres ne s’appliquent qu’aux boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="47a73-177">These settings are only applicable to cloud-based mailboxes.</span></span>

   - <span data-ttu-id="47a73-178">**Nombre maximal de destinataires par utilisateur**</span><span class="sxs-lookup"><span data-stu-id="47a73-178">**Maximum number of recipients per user**</span></span>

     <span data-ttu-id="47a73-179">Une valeur valide est comprise entre 0 et 10000.</span><span class="sxs-lookup"><span data-stu-id="47a73-179">A valid value is 0 to 10000.</span></span> <span data-ttu-id="47a73-180">La valeur par défaut est 0, ce qui signifie que les valeurs par défaut du service sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="47a73-180">The default value is 0, which means the service defaults are used.</span></span> <span data-ttu-id="47a73-181">Pour plus d’informations, consultez la rubrique [limites d’envoi](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1).</span><span class="sxs-lookup"><span data-stu-id="47a73-181">For more information, see [Sending limits](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1).</span></span>

     - <span data-ttu-id="47a73-182">**Limite horaire externe**: nombre maximal de destinataires externes par heure.</span><span class="sxs-lookup"><span data-stu-id="47a73-182">**External hourly limit**: The maximum number of external recipients per hour.</span></span>

     - <span data-ttu-id="47a73-183">**Limite horaire interne**: nombre maximal de destinataires internes par heure.</span><span class="sxs-lookup"><span data-stu-id="47a73-183">**Internal hourly limit**: The maximum number of internal recipients per hour.</span></span>

     - <span data-ttu-id="47a73-184">**Limite journalière**: nombre total maximal de destinataires par jour.</span><span class="sxs-lookup"><span data-stu-id="47a73-184">**Daily limit**: The maximum total number of recipients per day.</span></span>

   - <span data-ttu-id="47a73-185">**Action lorsqu’un utilisateur dépasse les limites ci-dessus**: configurez l’action à effectuer lorsque l’une des **limites de destinataires** est dépassée.</span><span class="sxs-lookup"><span data-stu-id="47a73-185">**Action when a user exceeds the limits above**: Configure the action to take when any one of the **Recipient Limits** are exceeded.</span></span> <span data-ttu-id="47a73-186">Pour toutes les actions, les destinataires spécifiés dans l’utilisateur ne peuvent pas **Envoyer de stratégie d’alerte par courrier électronique** (et dans le paramètre à présent, **avertir les personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant** dans la stratégie de courrier indésirable sortant reçoit des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="47a73-186">For all actions, the recipients specified in the **User restricted from sending email** alert policy (and in the now redundant **Notify specific people if a sender is blocked due to sending outbound spam** setting in the outbound spam policy receive email notifications.</span></span>

     - <span data-ttu-id="47a73-187">**Empêcher l’utilisateur d’envoyer des messages jusqu’au jour suivant**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-187">**Restrict the user from sending mail till the following day**: This is the default value.</span></span> <span data-ttu-id="47a73-188">Les notifications par courrier électronique sont envoyées et l’utilisateur ne peut plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="47a73-188">Email notifications are sent, and the user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="47a73-189">L’administrateur n’a aucun moyen de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="47a73-189">There is no way for the admin to override this block.</span></span>

       - <span data-ttu-id="47a73-190">L’activité alerte nommée **utilisateur restreint de l’envoi de courrier électronique** avertit les administrateurs (par e-mail et sur la page **afficher les alertes** ).</span><span class="sxs-lookup"><span data-stu-id="47a73-190">The activity alert named **User restricted from sending email** notifies admins (via email and on the **View alerts** page).</span></span>

       - <span data-ttu-id="47a73-191">Tous les destinataires spécifiés dans le paramètre **informer des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant** dans la stratégie sont également avertis.</span><span class="sxs-lookup"><span data-stu-id="47a73-191">Any recipients specified in the **Notify specific people if a sender is blocked due to sending outbound spam** setting in the policy are also notified.</span></span>

       - <span data-ttu-id="47a73-192">L’utilisateur ne peut plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="47a73-192">The user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="47a73-193">L’administrateur n’a aucun moyen de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="47a73-193">There is no way for the admin to override this block.</span></span>

     - <span data-ttu-id="47a73-194">**Empêcher l’utilisateur d’envoyer des courriers**électroniques : les notifications par courrier électronique sont envoyées, l’utilisateur est ajouté au portail \*\*[utilisateurs restreints] <https://sip.protection.office.com/restrictedusers> \*\* dans le centre de sécurité & conformité et l’utilisateur ne peut pas envoyer de courrier électronique tant qu’il n’a pas été supprimé du portail **utilisateurs restreints** par un administrateur. Une fois qu’un administrateur a supprimé l’utilisateur de la liste, l’utilisateur n’est plus relimité pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="47a73-194">**Restrict the user from sending mail**: Email notifications are sent, the user is added to the **[Restricted Users]<https://sip.protection.office.com/restrictedusers>** portal in the Security & Compliance Center, and the user can't send email until they're removed from the **Restricted Users** portal by an admin. After an admin removes the user from the list, the user won't be restricted again for that day.</span></span> <span data-ttu-id="47a73-195">Pour obtenir des instructions, consultez [la rubrique Suppression d’un utilisateur du portail utilisateurs restreints après l’envoi du courrier indésirable](removing-user-from-restricted-users-portal-after-spam.md).</span><span class="sxs-lookup"><span data-stu-id="47a73-195">For instructions, see [Removing a user from the Restricted Users portal after sending spam email](removing-user-from-restricted-users-portal-after-spam.md).</span></span>

     - <span data-ttu-id="47a73-196">**Aucune action, alerte uniquement**: les notifications par courrier électronique sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="47a73-196">**No action, alert only**: Email notifications are sent.</span></span>

6. <span data-ttu-id="47a73-197">Module Développez la section **transfert automatique** pour contrôler le transfert automatique des messages par les utilisateurs vers des expéditeurs externes.</span><span class="sxs-lookup"><span data-stu-id="47a73-197">(Optional) Expand **Automatic forwarding** section to control automatic email forwarding by users to external senders.</span></span> <span data-ttu-id="47a73-198">Pour plus d’informations sur le transfert automatique, voir [configurer le transfert du courrier](https://docs.microsoft.com/microsoft-365/admin/email/configure-email-forwarding).</span><span class="sxs-lookup"><span data-stu-id="47a73-198">For more information about automatic forwarding, see [Configure email forwarding](https://docs.microsoft.com/microsoft-365/admin/email/configure-email-forwarding).</span></span>

   > [!NOTE]
   >
   > - <span data-ttu-id="47a73-199">Avant le 2020 septembre, ces paramètres sont disponibles mais ne sont pas appliqués.</span><span class="sxs-lookup"><span data-stu-id="47a73-199">Before September 2020, these settings are available but not enforced.</span></span>
   >
   > - <span data-ttu-id="47a73-200">Ces paramètres s’appliquent uniquement aux boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="47a73-200">These settings apply only to cloud-based mailboxes.</span></span>
   >
   > - <span data-ttu-id="47a73-201">Le transfert automatique vers les destinataires internes n’est pas affecté par ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="47a73-201">Automatic forwarding to internal recipients is not affected by these setting.</span></span>

   <span data-ttu-id="47a73-202">Les valeurs disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="47a73-202">The available values are:</span></span>

   - <span data-ttu-id="47a73-203">**Automatique-contrôlé par le système**: autorise le filtrage du courrier indésirable sortant à contrôler le transfert automatique du courrier électronique externe.</span><span class="sxs-lookup"><span data-stu-id="47a73-203">**Automatic - System-controlled**: Allows outbound spam filtering to control automatic external email forwarding.</span></span> <span data-ttu-id="47a73-204">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-204">This is the default value.</span></span>

   - <span data-ttu-id="47a73-205">**Activé**: le transfert automatique du courrier électronique externe n’est pas désactivé par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-205">**On**: Automatic external email forwarding is not disabled by the policy.</span></span>

   - <span data-ttu-id="47a73-206">**Off**: tous les transferts de messages externes automatiques sont désactivés par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-206">**Off**: All automatic external email forwarding is disabled by the policy.</span></span>

7. <span data-ttu-id="47a73-207">Exige Développez la section **appliqué à** pour identifier les expéditeurs internes auxquels la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="47a73-207">(Required) Expand the **Applied to** section to identify the internal senders that the policy applies to.</span></span>

    <span data-ttu-id="47a73-208">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="47a73-208">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="47a73-209">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<sender1\>_ ou _\<sender2\>_).</span><span class="sxs-lookup"><span data-stu-id="47a73-209">Multiple values of the same condition or exception use OR logic (for example, _\<sender1\>_ or _\<sender2\>_).</span></span> <span data-ttu-id="47a73-210">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<sender1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="47a73-210">Different conditions or exceptions use AND logic (for example, _\<sender1\>_ and _\<member of group 1\>_).</span></span>

    <span data-ttu-id="47a73-211">Il est plus facile de cliquer sur**Ajouter une condition** trois fois pour afficher toutes les conditions disponibles.</span><span class="sxs-lookup"><span data-stu-id="47a73-211">It's easiest to click **Add a condition** three times to see all of the available conditions.</span></span> <span data-ttu-id="47a73-212">Vous pouvez cliquer sur le ![bouton Supprimer](../../media/scc-remove-icon.png) pour supprimer les conditions que vous ne voulez pas configurer.</span><span class="sxs-lookup"><span data-stu-id="47a73-212">You can click ![Remove button](../../media/scc-remove-icon.png) to remove conditions that you don't want to configure.</span></span>

    - <span data-ttu-id="47a73-213">**Le domaine de l’expéditeur est**: spécifie les expéditeurs dans un ou plusieurs domaines acceptés configurés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="47a73-213">**The sender domain is**: Specifies senders in one or more of the configured accepted domains in the organization.</span></span> <span data-ttu-id="47a73-214">Cliquez dans la zone **Ajouter un indicateur** pour afficher et sélectionner un domaine.</span><span class="sxs-lookup"><span data-stu-id="47a73-214">Click in the **Add a tag** box to see and select a domain.</span></span> <span data-ttu-id="47a73-215">Cliquez de nouveau sur la zone **Ajouter un indicateur** pour sélectionner d’autres domaines si plusieurs domaines sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="47a73-215">Click again the **Add a tag** box to select additional domains if more than one domain is available.</span></span>

    - <span data-ttu-id="47a73-216">L' **expéditeur est**: spécifie un ou plusieurs utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="47a73-216">**Sender is**: Specifies one or more users in your organization.</span></span> <span data-ttu-id="47a73-217">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="47a73-217">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="47a73-218">Cliquez de nouveau sur la zone **Ajouter une balise** pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="47a73-218">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="47a73-219">L' **expéditeur est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="47a73-219">**Sender is a member of**: Specifies one or more groups in your organization.</span></span> <span data-ttu-id="47a73-220">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="47a73-220">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="47a73-221">Cliquez de nouveau sur la zone **Ajouter une balise** pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="47a73-221">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="47a73-222">**Sauf si**: pour ajouter des exceptions à la règle, cliquez sur **Ajouter une condition** trois fois pour afficher toutes les exceptions disponibles.</span><span class="sxs-lookup"><span data-stu-id="47a73-222">**Except if**: To add exceptions for the rule, click **Add a condition** three times to see all of the available exceptions.</span></span> <span data-ttu-id="47a73-223">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="47a73-223">The settings and behavior are exactly like the conditions.</span></span>

8. <span data-ttu-id="47a73-224">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="47a73-224">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-view-outbound-spam-policies"></a><span data-ttu-id="47a73-225">Utiliser le centre de sécurité & conformité pour afficher les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-225">Use the Security & Compliance Center to view outbound spam policies</span></span>

1. <span data-ttu-id="47a73-226">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-226">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-227">Sur la page **paramètres de blocage du courrier indésirable** , cliquez sur ![ développer ](../../media/scc-expand-icon.png) une icône pour développer une stratégie de courrier indésirable sortant :</span><span class="sxs-lookup"><span data-stu-id="47a73-227">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="47a73-228">Stratégie par défaut nommée **stratégie de filtrage du courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="47a73-228">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="47a73-229">Une stratégie personnalisée que vous avez créée où la valeur dans la colonne **type** est **personnalisée stratégie anti-courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="47a73-229">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="47a73-230">Les paramètres de stratégie sont affichés dans les détails de stratégie développés qui s’affichent, ou vous pouvez cliquer sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="47a73-230">The policy settings are displayed in the expanded policy details that appear, or you can click **Edit policy**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-outbound-spam-policies"></a><span data-ttu-id="47a73-231">Utiliser le centre de sécurité & conformité pour modifier les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-231">Use the Security & Compliance Center to modify outbound spam policies</span></span>

1. <span data-ttu-id="47a73-232">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-232">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-233">Sur la page **paramètres de blocage du courrier indésirable** , cliquez sur ![ développer ](../../media/scc-expand-icon.png) une icône pour développer une stratégie de courrier indésirable sortant :</span><span class="sxs-lookup"><span data-stu-id="47a73-233">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="47a73-234">Stratégie par défaut nommée **stratégie de filtrage du courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="47a73-234">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="47a73-235">Une stratégie personnalisée que vous avez créée où la valeur dans la colonne **type** est **personnalisée stratégie anti-courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="47a73-235">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="47a73-236">Cliquez sur **Modifier une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="47a73-236">Click **Edit policy**.</span></span>

<span data-ttu-id="47a73-237">Pour les stratégies de courrier indésirable sortant personnalisé, les paramètres disponibles dans le menu volant qui s’affiche sont identiques à ceux décrits dans la section [utiliser le centre de sécurité & conformité pour créer des stratégies de courrier indésirable sortant](#use-the-security--compliance-center-to-create-outbound-spam-policies) .</span><span class="sxs-lookup"><span data-stu-id="47a73-237">For custom outbound spam policies, the available settings in the flyout that appears are identical to those described in the [Use the Security & Compliance Center to create outbound spam policies](#use-the-security--compliance-center-to-create-outbound-spam-policies) section.</span></span>

<span data-ttu-id="47a73-238">Pour la stratégie de courrier indésirable sortant par défaut nommée **stratégie de filtrage du courrier indésirable sortant**, la section **appliqué à** n’est pas disponible (la stratégie s’applique à tout le monde) et vous ne pouvez pas renommer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="47a73-238">For the default outbound spam policy named **Outbound spam filter policy**, the **Applied to** section isn't available (the policy applies to everyone), and you can't rename the policy.</span></span>

<span data-ttu-id="47a73-239">Pour activer ou désactiver une stratégie, définir l’ordre de priorité de la stratégie ou configurer les notifications de mise en quarantaine de l’utilisateur final, voir les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="47a73-239">To enable or disable a policy, set the policy priority order, or configure the end-user quarantine notifications, see the following sections.</span></span>

### <a name="enable-or-disable-outbound-spam-policies"></a><span data-ttu-id="47a73-240">Activer ou désactiver les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-240">Enable or disable outbound spam policies</span></span>

1. <span data-ttu-id="47a73-241">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-241">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-242">Dans la page **paramètres de blocage du courrier indésirable** , cliquez sur ![ développer ](../../media/scc-expand-icon.png) une icône pour développer une stratégie personnalisée que vous avez créée (la valeur dans la colonne **type** est **stratégie courrier indésirable sortant personnalisé**).</span><span class="sxs-lookup"><span data-stu-id="47a73-242">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand a custom policy that you created (the value in the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="47a73-243">Dans les détails de la stratégie développée qui s’affichent, notez la valeur dans la colonne**Activé**.</span><span class="sxs-lookup"><span data-stu-id="47a73-243">In the expanded policy details that appear, notice the value in the **On** column.</span></span>

   <span data-ttu-id="47a73-244">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="47a73-244">Move the toggle to the left to disable the policy:</span></span> ![Désactiver](../../media/scc-toggle-off.png)

   <span data-ttu-id="47a73-246">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="47a73-246">Move the toggle to the right to enable the policy:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)

<span data-ttu-id="47a73-248">Vous ne pouvez pas désactiver la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-248">You can't disable the default outbound spam policy.</span></span>

### <a name="set-the-priority-of-custom-outbound-spam-policies"></a><span data-ttu-id="47a73-249">Définir la priorité des stratégies de courrier indésirable sortant personnalisé</span><span class="sxs-lookup"><span data-stu-id="47a73-249">Set the priority of custom outbound spam policies</span></span>

<span data-ttu-id="47a73-250">Par défaut, les stratégies de courrier indésirable sortant reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="47a73-250">By default, outbound spam policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="47a73-251">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="47a73-251">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="47a73-252">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="47a73-252">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="47a73-253">Les stratégies de courrier indésirable sortant personnalisé sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="47a73-253">Custom outbound spam policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="47a73-254">La stratégie de courrier indésirable sortant par défaut nommée **stratégie de filtrage du courrier indésirable sortant** a la valeur Priority la **plus faible**et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="47a73-254">The default outbound spam policy named **Outbound spam filter policy** has the priority value **Lowest**, and you can't change it.</span></span>

<span data-ttu-id="47a73-255">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="47a73-255">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="47a73-256">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-256">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-257">Dans la page **paramètres de blocage du courrier indésirable** , recherchez les stratégies pour lesquelles la valeur dans la colonne **type** est **Custom courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="47a73-257">On the **Anti-spam settings** page, find the policies where the value in the **Type** column is **Custom outbound spam policy**.</span></span> <span data-ttu-id="47a73-258">Notez les valeurs de la colonne**Priorité** :</span><span class="sxs-lookup"><span data-stu-id="47a73-258">Notice the values in the **Priority** column:</span></span>

   - <span data-ttu-id="47a73-259">La stratégie de courrier indésirable sortant personnalisé avec la priorité la plus élevée a la valeur ![ flèche vers le bas ](../../media/ITPro-EAC-DownArrowIcon.png) **0**.</span><span class="sxs-lookup"><span data-stu-id="47a73-259">The custom outbound spam policy with the highest priority has the value ![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **0**.</span></span>

   - <span data-ttu-id="47a73-260">La stratégie de courrier indésirable sortant personnalisé avec la priorité la plus faible est dotée de l' ![ icône de flèche haut ](../../media/ITPro-EAC-UpArrowIcon.png) **n** (par exemple, ![ icône flèche haut ](../../media/ITPro-EAC-UpArrowIcon.png) **3**).</span><span class="sxs-lookup"><span data-stu-id="47a73-260">The custom outbound spam policy with the lowest priority has the value ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **3**).</span></span>

   - <span data-ttu-id="47a73-261">Si vous avez au moins trois stratégies de courrier indésirable sortant personnalisées, les stratégies comprises entre la priorité la plus élevée et la priorité la plus faible ont une icône flèche ![ ](../../media/ITPro-EAC-UpArrowIcon.png)![ vers le bas de l’icône ](../../media/ITPro-EAC-DownArrowIcon.png) **n** (par exemple, icône flèche ![ ](../../media/ITPro-EAC-UpArrowIcon.png)![ vers le bas, icône ](../../media/ITPro-EAC-DownArrowIcon.png) **2**).</span><span class="sxs-lookup"><span data-stu-id="47a73-261">If you have three or more custom outbound spam policies, the policies between the highest and lowest priority have values ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **2**).</span></span>

3. <span data-ttu-id="47a73-262">Clic </span><span class="sxs-lookup"><span data-stu-id="47a73-262">Click</span></span> ![Icône de flèche vers le haut](../../media/ITPro-EAC-UpArrowIcon.png) <span data-ttu-id="47a73-264">ou</span><span class="sxs-lookup"><span data-stu-id="47a73-264">or</span></span> ![Icône de flèche vers le bas](../../media/ITPro-EAC-DownArrowIcon.png) <span data-ttu-id="47a73-266">pour déplacer la stratégie de courrier indésirable sortant personnalisé vers le haut ou vers le bas dans la liste priorité.</span><span class="sxs-lookup"><span data-stu-id="47a73-266">to move the custom outbound spam policy up or down in the priority list.</span></span>

## <a name="use-the-security--compliance-center-to-remove-outbound-spam-policies"></a><span data-ttu-id="47a73-267">Utiliser le centre de sécurité & conformité pour supprimer les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-267">Use the Security & Compliance Center to remove outbound spam policies</span></span>

1. <span data-ttu-id="47a73-268">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="47a73-268">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="47a73-269">Dans la page **paramètres de blocage du courrier indésirable** , cliquez sur ![ développer ](../../media/scc-expand-icon.png) pour développer la stratégie personnalisée à supprimer (la colonne **type** est **personnalisée courrier indésirable sortant**).</span><span class="sxs-lookup"><span data-stu-id="47a73-269">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand the custom policy that you want to delete (the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="47a73-270">Dans les détails de la stratégie développée qui s’affichent, cliquez sur **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="47a73-270">In the expanded policy details that appear, click **Delete policy**.</span></span>

4. <span data-ttu-id="47a73-271">Cliquez sur **Oui** lorsque la boîte de dialogue d’avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="47a73-271">Click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="47a73-272">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-272">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-outbound-spam-policies"></a><span data-ttu-id="47a73-273">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-273">Use Exchange Online PowerShell or standalone EOP PowerShell to configure outbound spam policies</span></span>

<span data-ttu-id="47a73-274">Comme décrit précédemment, une stratégie de courrier indésirable sortant est constituée d’une stratégie de filtrage du courrier indésirable sortant et d’une règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-274">As previously described, an outbound spam policy consists of an outbound spam filter policy and an outbound spam filter rule.</span></span>

<span data-ttu-id="47a73-275">Dans Exchange Online PowerShell ou le PowerShell autonome EOP, la différence entre les stratégies de filtrage du courrier indésirable sortant et les règles de filtrage du courrier indésirable sortant est apparente.</span><span class="sxs-lookup"><span data-stu-id="47a73-275">In Exchange Online PowerShell or standalone EOP PowerShell, the difference between outbound spam filter policies and outbound spam filter rules is apparent.</span></span> <span data-ttu-id="47a73-276">Vous gérez les stratégies de filtrage du courrier indésirable sortant à l’aide des cmdlets \*\* \* -HostedOutboundSpamFilterPolicy\*\* et vous gérez les règles de filtrage du courrier indésirable sortant à l’aide des cmdlets \*\* \* -HostedOutboundSpamFilterRule\*\* .</span><span class="sxs-lookup"><span data-stu-id="47a73-276">You manage outbound spam filter policies by using the **\*-HostedOutboundSpamFilterPolicy** cmdlets, and you manage outbound spam filter rules by using the **\*-HostedOutboundSpamFilterRule** cmdlets.</span></span>

- <span data-ttu-id="47a73-277">Dans PowerShell, vous devez d’abord créer la stratégie de filtrage du courrier indésirable sortant, puis créer la règle de filtrage du courrier indésirable sortant qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="47a73-277">In PowerShell, you create the outbound spam filter policy first, then you create the outbound spam filter rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="47a73-278">Dans PowerShell, vous pouvez modifier séparément les paramètres de la stratégie de filtrage du courrier indésirable sortant et de la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-278">In PowerShell, you modify the settings in the outbound spam filter policy and the outbound spam filter rule separately.</span></span>
- <span data-ttu-id="47a73-279">Lorsque vous supprimez une stratégie de filtrage du courrier indésirable sortant de PowerShell, la règle de filtrage du courrier indésirable sortant correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="47a73-279">When you remove a outbound spam filter policy from PowerShell, the corresponding outbound spam filter rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-outbound-spam-policies"></a><span data-ttu-id="47a73-280">Utiliser PowerShell pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-280">Use PowerShell to create outbound spam policies</span></span>

<span data-ttu-id="47a73-281">La création d’une stratégie de courrier indésirable sortant dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="47a73-281">Creating an outbound spam policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="47a73-282">Créez la stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-282">Create the outbound spam filter policy.</span></span>
2. <span data-ttu-id="47a73-283">Créez la règle de filtrage du courrier indésirable sortant qui spécifie la stratégie de filtrage du courrier indésirable sortant à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="47a73-283">Create the outbound spam filter rule that specifies the outbound spam filter policy that the rule applies to.</span></span>

 <span data-ttu-id="47a73-284">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="47a73-284">**Notes**:</span></span>

- <span data-ttu-id="47a73-285">Vous pouvez créer une règle de filtrage du courrier indésirable sortant et lui affecter une stratégie de filtrage du courrier indésirable sortant existante non associée.</span><span class="sxs-lookup"><span data-stu-id="47a73-285">You can create a new outbound spam filter rule and assign an existing, unassociated outbound spam filter policy to it.</span></span> <span data-ttu-id="47a73-286">Une règle de filtrage du courrier indésirable sortant ne peut pas être associée à plusieurs stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-286">An outbound spam filter rule can't be associated with more than one outbound spam filter policy.</span></span>

- <span data-ttu-id="47a73-287">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de filtrage du courrier indésirable sortant dans PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="47a73-287">You can configure the following settings on new outbound spam filter policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="47a73-288">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-HostedOutboundSpamFilterRule** ).</span><span class="sxs-lookup"><span data-stu-id="47a73-288">Create the new policy as disabled (_Enabled_ `$false` on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>
  - <span data-ttu-id="47a73-289">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-HostedOutboundSpamFilterRule** ).</span><span class="sxs-lookup"><span data-stu-id="47a73-289">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>

- <span data-ttu-id="47a73-290">Une nouvelle stratégie de filtrage du courrier indésirable sortant que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’affectez pas la stratégie à une règle de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="47a73-290">A new outbound spam filter policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a spam filter rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-outbound-spam-filter-policy"></a><span data-ttu-id="47a73-291">Étape 1 : utiliser PowerShell pour créer une stratégie de filtrage des courriers indésirables sortants</span><span class="sxs-lookup"><span data-stu-id="47a73-291">Step 1: Use PowerShell to create an outbound spam filter policy</span></span>

<span data-ttu-id="47a73-292">Pour créer une stratégie de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-292">To create an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="47a73-293">Cet exemple crée une stratégie de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-293">This example creates a new outbound spam filter policy named Contoso Executives with the following settings:</span></span>

- <span data-ttu-id="47a73-294">Les limites de taux de destinataires sont limitées aux valeurs plus petites que celles par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a73-294">The recipient rate limits are restricted to smaller values that the defaults.</span></span> <span data-ttu-id="47a73-295">Pour plus d’informations, consultez la rubrique [limites d’envoi dans les options Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span><span class="sxs-lookup"><span data-stu-id="47a73-295">For more information, see [Sending limits across Microsoft 365 options](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span></span>

- <span data-ttu-id="47a73-296">Une fois que l’une des limites est atteinte, l’utilisateur ne peut pas envoyer de messages.</span><span class="sxs-lookup"><span data-stu-id="47a73-296">After one of the limits is reached, the user is prevented from sending messages.</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "Contoso Executives" -RecipientLimitExternalPerHour 400 -RecipientLimitInternalPerHour 800 -RecipientLimitPerDay 800 -ActionWhenThresholdReached BlockUser
```

<span data-ttu-id="47a73-297">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="47a73-297">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-outbound-spam-filter-rule"></a><span data-ttu-id="47a73-298">Étape 2 : utiliser PowerShell pour créer une règle de filtrage des courriers indésirables sortants</span><span class="sxs-lookup"><span data-stu-id="47a73-298">Step 2: Use PowerShell to create an outbound spam filter rule</span></span>

<span data-ttu-id="47a73-299">Pour créer une règle de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-299">To create an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "<RuleName>" -HostedOutboundSpamFilterPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="47a73-300">Cet exemple crée une règle de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="47a73-300">This example creates a new outbound spam filter rule named Contoso Executives with these settings:</span></span>

- <span data-ttu-id="47a73-301">La stratégie de filtrage du courrier indésirable sortant nommé Contoso Executives est associée à la règle.</span><span class="sxs-lookup"><span data-stu-id="47a73-301">The outbound spam filter policy named Contoso Executives is associated with the rule.</span></span>

- <span data-ttu-id="47a73-302">La règle s’applique aux membres du groupe nommé Groupe Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="47a73-302">The rule applies to members of the group named Contoso Executives Group.</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "Contoso Executives" -HostedOutboundSpamFilterPolicy "Contoso Executives" -SentToMemberOf "Contoso Executives Group"
```

<span data-ttu-id="47a73-303">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="47a73-303">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/new-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-policies"></a><span data-ttu-id="47a73-304">Utiliser PowerShell pour afficher les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-304">Use PowerShell to view outbound spam filter policies</span></span>

<span data-ttu-id="47a73-305">Pour renvoyer une liste récapitulative de toutes les stratégies de filtrage du courrier indésirable sortant, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-305">To return a summary list of all outbound spam filter policies, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy
```

<span data-ttu-id="47a73-306">Pour renvoyer des informations détaillées sur une stratégie de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-306">To return detailed information about a specific outbound spam filter policy, use the this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="47a73-307">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie de filtrage du courrier indésirable sortant nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="47a73-307">This example returns all the property values for the outbound spam filter policy named Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "Executives" | Format-List
```

<span data-ttu-id="47a73-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="47a73-308">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-rules"></a><span data-ttu-id="47a73-309">Utiliser PowerShell pour afficher les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-309">Use PowerShell to view outbound spam filter rules</span></span>

<span data-ttu-id="47a73-310">Pour afficher les règles de filtrage de courrier indésirable sortant existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-310">To view existing outbound spam filter rules, use the following syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule [-Identity "<RuleIdentity>] [-State <Enabled | Disabled]
```

<span data-ttu-id="47a73-311">Pour renvoyer une liste récapitulative de toutes les règles de filtrage du courrier indésirable sortant, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-311">To return a summary list of all outbound spam filter rules, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule
```

<span data-ttu-id="47a73-312">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="47a73-312">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -State Disabled
```

```PowerShell
Get-HostedOutboundSpamFilterRule -State Enabled
```

<span data-ttu-id="47a73-313">Pour renvoyer des informations détaillées sur une règle de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-313">To return detailed information about a specific outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "<RuleName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="47a73-314">Cet exemple renvoie toutes les valeurs de propriété pour la règle de filtrage du courrier indésirable sortant nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="47a73-314">This example returns all the property values for the outbound spam filter rule named Contoso Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="47a73-315">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="47a73-315">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/get-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-policies"></a><span data-ttu-id="47a73-316">Utiliser PowerShell pour modifier les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-316">Use PowerShell to modify outbound spam filter policies</span></span>

<span data-ttu-id="47a73-317">Les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie de filtrage des programmes malveillants dans PowerShell comme lors de la création de la stratégie, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie de filtrage du courrier indésirable sortant](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="47a73-317">The same settings are available when you modify a malware filter policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an outbound spam filter policy](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) section earlier in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="47a73-318">Vous ne pouvez pas renommer une stratégie de filtrage du courrier indésirable sortant (la cmdlet **Set-HostedOutboundSpamFilterPolicy** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="47a73-318">You can't rename an outbound spam filter policy (the **Set-HostedOutboundSpamFilterPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="47a73-319">Lorsque vous renommez une stratégie de courrier indésirable sortant dans le centre de sécurité & conformité, vous renommez uniquement la _règle_de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="47a73-319">When you rename an outbound spam policy in the Security & Compliance Center, you're only renaming the outbound spam filter _rule_.</span></span>

<span data-ttu-id="47a73-320">Pour modifier une stratégie de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-320">To modify an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="47a73-321">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="47a73-321">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-rules"></a><span data-ttu-id="47a73-322">Utiliser PowerShell pour modifier les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-322">Use PowerShell to modify outbound spam filter rules</span></span>

<span data-ttu-id="47a73-323">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="47a73-323">The only setting that isn't available when you modify an outbound spam filter rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="47a73-324">Pour activer ou désactiver les règles de filtrage de courrier indésirable sortant existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="47a73-324">To enable or disable existing outbound spam filter rules, see the next section.</span></span>

<span data-ttu-id="47a73-325">Dans le cas contraire, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47a73-325">Otherwise, no additional settings are available when you modify an outbound spam filter rule in PowerShell.</span></span> <span data-ttu-id="47a73-326">Les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle de filtrage du courrier indésirable sortant](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="47a73-326">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an outbound spam filter rule](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) section earlier in this topic.</span></span>

<span data-ttu-id="47a73-327">Pour modifier une règle de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-327">To modify an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="47a73-328">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="47a73-328">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/set-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-outbound-spam-filter-rules"></a><span data-ttu-id="47a73-329">Utiliser PowerShell pour activer ou désactiver les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-329">Use PowerShell to enable or disable outbound spam filter rules</span></span>

<span data-ttu-id="47a73-330">L’activation ou la désactivation d’une règle de filtrage du courrier indésirable sortant dans PowerShell active ou désactive la totalité de la stratégie anti-courrier indésirable sortant (la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant affecté).</span><span class="sxs-lookup"><span data-stu-id="47a73-330">Enabling or disabling an outbound spam filter rule in PowerShell enables or disables the whole outbound spam policy (the outbound spam filter rule and the assigned outbound spam filter policy).</span></span> <span data-ttu-id="47a73-331">Vous ne pouvez pas activer ou désactiver la stratégie de courrier indésirable sortant par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="47a73-331">You can't enable or disable the default outbound spam policy (it's always always applied to all recipients).</span></span>

<span data-ttu-id="47a73-332">Pour activer ou désactiver une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-332">To enable or disable an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-HostedOutboundSpamFilterRule | Disable-HostedOutboundSpamFilterRule> -Identity "<RuleName>"
```

<span data-ttu-id="47a73-333">Cet exemple désactive la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="47a73-333">This example disables the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Disable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="47a73-334">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="47a73-334">This example enables same rule.</span></span>

```PowerShell
Enable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="47a73-335">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/enable-hostedoutboundspamfilterrule) et [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/disable-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="47a73-335">For detailed syntax and parameter information, see [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/enable-hostedoutboundspamfilterrule) and [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/disable-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-outbound-spam-filter-rules"></a><span data-ttu-id="47a73-336">Utiliser PowerShell pour définir la priorité des règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-336">Use PowerShell to set the priority of outbound spam filter rules</span></span>

<span data-ttu-id="47a73-337">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="47a73-337">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="47a73-338">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="47a73-338">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="47a73-339">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="47a73-339">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="47a73-340">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="47a73-340">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="47a73-341">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="47a73-341">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="47a73-342">Pour définir la priorité d’une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-342">To set the priority of an outbound spam filter rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="47a73-p139">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="47a73-p139">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "Marketing Department" -Priority 2
```

> [!NOTE]
>
> - <span data-ttu-id="47a73-345">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-HostedOutboundSpamFilterRule** .</span><span class="sxs-lookup"><span data-stu-id="47a73-345">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-HostedOutboundSpamFilterRule** cmdlet instead.</span></span>
>
> - <span data-ttu-id="47a73-346">La stratégie de filtrage du courrier indésirable par défaut sortante n’a pas de règle de filtrage du courrier indésirable correspondante et a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="47a73-346">The outbound default spam filter policy doesn't have a corresponding spam filter rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-policies"></a><span data-ttu-id="47a73-347">Utiliser PowerShell pour supprimer les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-347">Use PowerShell to remove outbound spam filter policies</span></span>

<span data-ttu-id="47a73-348">Lorsque vous utilisez PowerShell pour supprimer une stratégie de filtrage du courrier indésirable sortant, la règle de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="47a73-348">When you use PowerShell to remove an outbound spam filter policy, the corresponding outbound spam filter rule isn't removed.</span></span>

<span data-ttu-id="47a73-349">Pour supprimer une stratégie de filtrage des courriers indésirables sortants dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-349">To remove an outbound spam filter policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="47a73-350">Cet exemple supprime la stratégie de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="47a73-350">This example removes the outbound spam filter policy named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "Marketing Department"
```

<span data-ttu-id="47a73-351">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="47a73-351">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-rules"></a><span data-ttu-id="47a73-352">Utiliser PowerShell pour supprimer les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="47a73-352">Use PowerShell to remove outbound spam filter rules</span></span>

<span data-ttu-id="47a73-353">Lorsque vous utilisez PowerShell pour supprimer une règle de filtrage du courrier indésirable sortant, la stratégie de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="47a73-353">When you use PowerShell to remove an outbound spam filter rule, the corresponding outbound spam filter policy isn't removed.</span></span>

<span data-ttu-id="47a73-354">Pour supprimer une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="47a73-354">To remove an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "<PolicyName>"
```

<span data-ttu-id="47a73-355">Cet exemple supprime la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="47a73-355">This example removes the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="47a73-356">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="47a73-356">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/remove-hostedoutboundspamfilterrule).</span></span>

## <a name="for-more-information"></a><span data-ttu-id="47a73-357">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="47a73-357">For more information</span></span>

[<span data-ttu-id="47a73-358">Retirer les utilisateurs bloqués du portail des utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="47a73-358">Remove blocked users from the Restricted Users portal</span></span>](removing-user-from-restricted-users-portal-after-spam.md)

[<span data-ttu-id="47a73-359">Pool de remise à haut risque pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="47a73-359">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="47a73-360">Forum Aux Questions sur la protection anti-courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="47a73-360">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)

[<span data-ttu-id="47a73-361">Rapport des messages transférés automatiquement</span><span class="sxs-lookup"><span data-stu-id="47a73-361">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)
