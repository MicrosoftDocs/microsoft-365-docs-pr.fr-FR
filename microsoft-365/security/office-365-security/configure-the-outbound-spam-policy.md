---
title: Configurer le filtrage du courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l’envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires.
ms.openlocfilehash: 699de94a300ac8625e92d2c467edd461d72c7d2f
ms.sourcegitcommit: a955324e33097bbd2fc4ad7f2b8d1f3d87bc8580
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43608173"
---
# <a name="configure-outbound-spam-filtering-in-office-365"></a><span data-ttu-id="4dece-103">Configurer le filtrage du courrier indésirable sortant dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4dece-103">Configure outbound spam filtering in Office 365</span></span>

<span data-ttu-id="4dece-104">Si vous êtes un client Office 365 avec des boîtes aux lettres dans Exchange Online ou un client Exchange Online Protection (EOP) autonome sans boîte aux lettres Exchange Online, les messages électroniques sortants envoyés via EOP sont automatiquement vérifiés pour le courrier indésirable et les activités d’envoi inhabituelles.</span><span class="sxs-lookup"><span data-stu-id="4dece-104">If you're an Office 365 customer with mailboxes in Exchange Online or a standalone Exchange Online Protection (EOP) customer without Exchange Online mailboxes, outbound email messages that are sent through EOP are automatically checked for spam and unusual sending activity.</span></span>

<span data-ttu-id="4dece-105">Le courrier indésirable sortant d’un utilisateur de votre organisation indique généralement un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="4dece-105">Outbound spam from a user in your organization typically indicates a compromised account.</span></span> <span data-ttu-id="4dece-106">Les messages sortants suspects sont marqués comme courrier indésirable (quel que soit le seuil de probabilité de courrier indésirable ou la valeur SCL) et sont acheminés via le [pool de remise à haut risque](high-risk-delivery-pool-for-outbound-messages.md) afin de protéger la réputation du service (c’est-à-dire conserver les serveurs de messagerie sources Office 365 hors des listes d’adresses IP bloquées).</span><span class="sxs-lookup"><span data-stu-id="4dece-106">Suspicious outbound messages are marked as spam (regardless of the spam confidence level or SCL) and are routed through the [high-risk delivery pool](high-risk-delivery-pool-for-outbound-messages.md) to help protect the reputation of the service (that is, keep Office 365 source email servers off of IP block lists).</span></span> <span data-ttu-id="4dece-107">Les administrateurs sont automatiquement informés de l’activité e-mail sortante suspecte et des utilisateurs bloqués via des [stratégies d’alerte](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="4dece-107">Admins are automatically notified of suspicious outbound email activity and blocked users via [alert policies](../../compliance/alert-policies.md).</span></span>

<span data-ttu-id="4dece-108">EOP utilise des stratégies de courrier indésirable sortant dans le cadre de la protection globale de votre organisation contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4dece-108">EOP uses outbound spam policies as part of your organization's overall defense against spam.</span></span> <span data-ttu-id="4dece-109">Pour plus d’informations, voir [Protection contre le courrier indésirable dans Office 365](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="4dece-109">For more information, see [Anti-spam protection in Office 365](anti-spam-protection.md).</span></span>

<span data-ttu-id="4dece-110">Les administrateurs peuvent afficher, modifier et configurer (mais pas supprimer) la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-110">Admins can view, edit, and configure (but not delete) the default outbound spam policy.</span></span> <span data-ttu-id="4dece-111">Pour une granularité accrue, vous pouvez également créer des stratégies de courrier indésirable sortant personnalisées qui s’appliquent à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4dece-111">For greater granularity, you can also create custom outbound spam policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="4dece-112">Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez cependant modifier la priorité (l'ordre d'exécution) de vos stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4dece-112">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="4dece-113">Vous pouvez configurer des stratégies de courrier indésirable sortant dans le centre de sécurité & de sécurité Office 365 ou dans PowerShell (les clients Exchange Online PowerShell pour Office 365 ; Exchange Online Protection PowerShell pour les clients EOP autonomes).</span><span class="sxs-lookup"><span data-stu-id="4dece-113">You can configure outbound spam policies in the Office 365 Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Office 365 customers; Exchange Online Protection PowerShell for standalone EOP customers).</span></span>

## <a name="outbound-spam-policies-in-the-office-365-security--compliance-center-vs-exchange-online-powershell-or-exchange-online-protection-powershell"></a><span data-ttu-id="4dece-114">Stratégies de courrier indésirable sortant dans le centre de sécurité & Office 365 Security Center vs Exchange Online PowerShell ou Exchange Online Protection PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dece-114">Outbound spam policies in the Office 365 Security & Compliance Center vs Exchange Online PowerShell or Exchange Online Protection PowerShell</span></span>

<span data-ttu-id="4dece-115">Les éléments de base d’une stratégie de courrier indésirable sortant dans EOP sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4dece-115">The basic elements of an outbound spam policy in EOP are:</span></span>

- <span data-ttu-id="4dece-116">**Stratégie de filtrage du courrier indésirable sortant**: spécifie les actions pour le filtrage du courrier indésirable sortant et les options de notification.</span><span class="sxs-lookup"><span data-stu-id="4dece-116">**The outbound spam filter policy**: Specifies the actions for outbound spam filtering verdicts and the notification options.</span></span>

- <span data-ttu-id="4dece-117">**Règle de filtrage du courrier indésirable sortant**: spécifie la priorité et les filtres de destinataire (auxquels s’applique la stratégie) pour une stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-117">**The outbound spam filter rule**: Specifies the priority and recipient filters (who the policy applies to) for a outbound spam filter policy.</span></span>

<span data-ttu-id="4dece-118">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de courrier indésirable sortant dans le centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="4dece-118">The difference between these two elements isn't obvious when you manage outbound spam policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="4dece-119">Lorsque vous créez une stratégie de courrier indésirable sortant dans le centre de sécurité & conformité, vous créez en réalité une règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="4dece-119">When you create an outbound spam policy in the Security & Compliance Center, you're actually creating a outbound spam filter rule and the associated outbound spam filter policy at the same time using the same name for both.</span></span>

- <span data-ttu-id="4dece-120">Lorsque vous modifiez une stratégie de courrier indésirable sortant dans le centre de sécurité & conformité, les paramètres relatifs aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-120">When you modify an outbound spam policy in the Security & Compliance Center, settings related to the name, priority, enabled or disabled, and recipient filters modify the outbound spam filter rule.</span></span> <span data-ttu-id="4dece-121">Tous les autres paramètres modifient la stratégie de filtrage du courrier indésirable sortant associée.</span><span class="sxs-lookup"><span data-stu-id="4dece-121">All other settings modify the associated outbound spam filter policy.</span></span>

- <span data-ttu-id="4dece-122">Lorsque vous supprimez une stratégie de courrier indésirable sortant du centre de sécurité & conformité, la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="4dece-122">When you remove an outbound spam policy from the Security & Compliance Center, the outbound spam filter rule and the associated outbound spam filter policy are removed.</span></span>

<span data-ttu-id="4dece-123">Dans Exchange Online PowerShell ou une version autonome d’Exchange Online Protection PowerShell, la différence entre les stratégies de filtrage du courrier indésirable sortant et les règles de filtrage du courrier indésirable sortant est apparente.</span><span class="sxs-lookup"><span data-stu-id="4dece-123">In Exchange Online PowerShell or standalone Exchange Online Protection PowerShell, the difference between outbound spam filter policies and outbound spam filter rules is apparent.</span></span> <span data-ttu-id="4dece-124">Vous gérez les stratégies de filtrage du \*\* \*\*\* courrier indésirable sortant à l’aide des cmdlets-HostedContentFilterPolicy et vous gérez les règles de \*\* \*\*\* filtrage du courrier indésirable sortant à l’aide des cmdlets-hostedcontentfilterrule permet.</span><span class="sxs-lookup"><span data-stu-id="4dece-124">You manage outbound spam filter policies by using the **\*-HostedContentFilterPolicy** cmdlets, and you manage outbound spam filter rules by using the **\*-HostedContentFilterRule** cmdlets.</span></span>

- <span data-ttu-id="4dece-125">Dans PowerShell, vous devez d’abord créer la stratégie de filtrage du courrier indésirable sortant, puis créer la règle de filtrage du courrier indésirable sortant qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="4dece-125">In PowerShell, you create the outbound spam filter policy first, then you create the outbound spam filter rule that identifies the policy that the rule applies to.</span></span>

- <span data-ttu-id="4dece-126">Dans PowerShell, vous pouvez modifier séparément les paramètres de la stratégie de filtrage du courrier indésirable sortant et de la règle de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-126">In PowerShell, you modify the settings in the outbound spam filter policy and the outbound spam filter rule separately.</span></span>

- <span data-ttu-id="4dece-127">Lorsque vous supprimez une stratégie de filtrage du courrier indésirable sortant de PowerShell, la règle de filtrage du courrier indésirable sortant correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="4dece-127">When you remove a outbound spam filter policy from PowerShell, the corresponding outbound spam filter rule isn't automatically removed, and vice versa.</span></span>

### <a name="default-outbound-spam-policy"></a><span data-ttu-id="4dece-128">Stratégie anti-courrier indésirable sortant par défaut</span><span class="sxs-lookup"><span data-stu-id="4dece-128">Default outbound spam policy</span></span>

<span data-ttu-id="4dece-129">Chaque organisation dispose d’une stratégie de courrier indésirable sortante intégrée nommée par défaut qui possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dece-129">Every organization has a built-in outbound spam policy named Default that has these properties:</span></span>

- <span data-ttu-id="4dece-130">La stratégie de filtrage du courrier indésirable sortant nommée par défaut est appliquée à tous les destinataires de l’organisation, même si aucune règle de filtrage du courrier indésirable sortant (filtres de destinataires) n’est associée à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4dece-130">The outbound spam filter policy named Default is applied to all recipients in the organization, even though there's no outbound spam filter rule (recipient filters) associated with the policy.</span></span>

- <span data-ttu-id="4dece-131">La stratégie nommée Par défaut possède la valeur de priorité personnalisée **Plus faible** que vous ne pouvez pas modifier (la stratégie est toujours appliquée en dernier).</span><span class="sxs-lookup"><span data-stu-id="4dece-131">The policy named Default has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="4dece-132">Les stratégies personnalisées que vous créez ont toujours une priorité plus élevée que la stratégie nommée Par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-132">Any custom policies that you create always have a higher priority than the policy named Default.</span></span>

- <span data-ttu-id="4dece-133">La stratégie nommée Par défaut est la stratégie par défaut (la propriété **IsDefault** possède la valeur`True`) et vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-133">The policy named Default is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="4dece-134">Pour accroître l’efficacité du filtrage du courrier indésirable sortant, vous pouvez créer des stratégies de courrier indésirable sortant personnalisées avec des paramètres plus stricts appliqués à des utilisateurs ou à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4dece-134">To increase the effectiveness of outbound spam filtering, you can create custom outbound spam policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4dece-135">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4dece-135">What do you need to know before you begin?</span></span>

- <span data-ttu-id="4dece-136">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="4dece-136">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="4dece-137">Pour accéder directement à la page **Paramètres anti-courrier indésirable**, utilisez <https://protection.office.com/antispam>.</span><span class="sxs-lookup"><span data-stu-id="4dece-137">To go directly to the **Anti-spam settings** page, use <https://protection.office.com/antispam>.</span></span>

- <span data-ttu-id="4dece-138">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="4dece-138">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="4dece-139">Pour vous connecter à un service Exchange Online Protection autonome, voir [Se connecter à PowerShell d’Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="4dece-139">To connect to standalone Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="4dece-140">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="4dece-140">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="4dece-141">Pour ajouter, modifier et supprimer des stratégies de courrier indésirable sortant, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="4dece-141">To add, modify, and delete outbound spam policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="4dece-142">Pour un accès en lecture seule aux stratégies de courrier indésirable sortant, vous devez être membre du groupe de rôles **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="4dece-142">For read-only access to outbound spam policies, you need to be a member of the **Security Reader** role group.</span></span> <span data-ttu-id="4dece-143">Pour plus d’informations sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4dece-143">For more information about role groups in the Security & Compliance Center, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="4dece-144">Pour connaître les paramètres recommandés pour les stratégies de courrier indésirable sortant, voir [EOP Outbound Outbound Filter Policy Settings](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="4dece-144">For our recommended settings for outbound spam policies, see [EOP outbound spam filter policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-outbound-spam-policy-settings).</span></span>

- <span data-ttu-id="4dece-145">Les [stratégies d’alerte](../../compliance/alert-policies.md) par défaut nommées limite d’envoi de **courrier électronique sont dépassées**, des **modèles de courrier électronique suspects détectés**et l’utilisateur ne peut pas envoyer **de courriers** électroniques aux membres du groupe **TenantAdmins** (**administrateurs globaux**) à propos de l’activité de courrier électronique sortant inhabituel et des utilisateurs bloqués en raison du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-145">The default [alert policies](../../compliance/alert-policies.md) named **Email sending limit exceeded**, **Suspicious email sending patterns detected**, and **User restricted from sending email** already send email notifications to members of the **TenantAdmins** (**Global admins**) group about unusual outbound email activity and blocked users due to outbound spam.</span></span> <span data-ttu-id="4dece-146">Pour plus d’informations, consultez [la rubrique vérifier les paramètres d’alerte pour les utilisateurs restreints](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span><span class="sxs-lookup"><span data-stu-id="4dece-146">For more information, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span> <span data-ttu-id="4dece-147">Nous vous recommandons d’utiliser ces stratégies d’alerte à la place des options de notification dans les stratégies de courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-147">We recommend that you use these alert policies instead of the the notification options in outbound spam policies.</span></span>

## <a name="use-the-security--compliance-center-to-create-outbound-spam-policies"></a><span data-ttu-id="4dece-148">Utiliser le centre de sécurité & conformité pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-148">Use the Security & Compliance Center to create outbound spam policies</span></span>

<span data-ttu-id="4dece-149">La création d’une stratégie de courrier indésirable sortant personnalisé dans le centre de sécurité & conformité crée la règle de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="4dece-149">Creating a custom outbound spam policy in the Security & Compliance Center creates the spam filter rule and the associated spam filter policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="4dece-150">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-150">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-151">Dans la page **paramètres du blocage du courrier indésirable** , cliquez sur **créer une stratégie sortante**.</span><span class="sxs-lookup"><span data-stu-id="4dece-151">On the **Anti-spam settings** page, click **Create an outbound policy**.</span></span>

3. <span data-ttu-id="4dece-152">Dans la **stratégie de filtrage du courrier indésirable sortant** qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4dece-152">In the **Outbound spam filter policy** fly out that opens, configure the following settings:</span></span>

   - <span data-ttu-id="4dece-153">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4dece-153">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="4dece-154">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4dece-154">**Description**: Enter an optional description for the policy.</span></span>

4. <span data-ttu-id="4dece-155">Module Développez la section **notifications** pour configurer des utilisateurs supplémentaires qui doivent recevoir des copies et des notifications de messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="4dece-155">(Optional) Expand the **Notifications** section to configure additional users who should receive copies and notifications of suspicious outbound email messages:</span></span>

   - <span data-ttu-id="4dece-156">**Envoyer une copie des messages électroniques sortants suspects à des personnes spécifiques**: ce paramètre ajoute les utilisateurs spécifiés en tant que destinataires CCI aux messages sortants suspects.</span><span class="sxs-lookup"><span data-stu-id="4dece-156">**Send a copy of suspicious outbound email messages to specific people**: This setting adds the specified users as Bcc recipients to the suspicious outbound messages.</span></span> <span data-ttu-id="4dece-157">Pour activer ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="4dece-157">To enable this setting:</span></span>

     <span data-ttu-id="4dece-158">a.</span><span class="sxs-lookup"><span data-stu-id="4dece-158">a.</span></span> <span data-ttu-id="4dece-159">Activez la case à cocher pour activer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="4dece-159">Select the check box to enable the setting.</span></span>

     <span data-ttu-id="4dece-160">b.</span><span class="sxs-lookup"><span data-stu-id="4dece-160">b.</span></span> <span data-ttu-id="4dece-161">Cliquez sur **Ajouter des personnes**.</span><span class="sxs-lookup"><span data-stu-id="4dece-161">Click **Add people**.</span></span> <span data-ttu-id="4dece-162">Dans la fenêtre mobile **Ajouter ou supprimer des destinataires** qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="4dece-162">In the **Add or remove recipients** flyout that appears:</span></span>

     <span data-ttu-id="4dece-163">c.</span><span class="sxs-lookup"><span data-stu-id="4dece-163">c.</span></span> <span data-ttu-id="4dece-164">Entrez l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4dece-164">Enter the sender's email address.</span></span> <span data-ttu-id="4dece-165">Vous pouvez spécifier plusieurs adresses de messagerie séparées par des points-virgules (;) ou un destinataire par ligne.</span><span class="sxs-lookup"><span data-stu-id="4dece-165">You can specify multiple email addresses separated by semicolons (;) or one recipient per line.</span></span>

     <span data-ttu-id="4dece-166">d.</span><span class="sxs-lookup"><span data-stu-id="4dece-166">d.</span></span> <span data-ttu-id="4dece-167">Clic </span><span class="sxs-lookup"><span data-stu-id="4dece-167">Click</span></span> ![Icône Ajouter](../../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) <span data-ttu-id="4dece-169">pour ajouter les destinataires.</span><span class="sxs-lookup"><span data-stu-id="4dece-169">to add the recipients.</span></span>

        <span data-ttu-id="4dece-170">Répétez ces étapes autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4dece-170">Repeat these steps as many times as necessary.</span></span>

        <span data-ttu-id="4dece-171">Les destinataires que vous avez ajoutés apparaissent dans la section **liste des destinataires** du menu volant.</span><span class="sxs-lookup"><span data-stu-id="4dece-171">The recipients you added appear in the **Recipient list** section on the flyout.</span></span> <span data-ttu-id="4dece-172">Pour supprimer un destinataire, cliquez ![sur le](../../media/scc-remove-icon.png)bouton supprimer.</span><span class="sxs-lookup"><span data-stu-id="4dece-172">To delete a recipient, click ![Remove button](../../media/scc-remove-icon.png).</span></span>

     <span data-ttu-id="4dece-173">e.</span><span class="sxs-lookup"><span data-stu-id="4dece-173">e.</span></span> <span data-ttu-id="4dece-174">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4dece-174">When you're finished, click **Save**.</span></span>

     <span data-ttu-id="4dece-175">Pour désactiver ce paramètre, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="4dece-175">To disable this setting, clear the check box.</span></span>

   - <span data-ttu-id="4dece-176">**Informer des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant**:</span><span class="sxs-lookup"><span data-stu-id="4dece-176">**Notify specific people if a sender is blocked due to sending outbound spam**:</span></span>

     > [!NOTE]
     > <span data-ttu-id="4dece-177">La [stratégie d’alerte](../../compliance/alert-policies.md) par défaut nommée **User Restricted from sending email** envoie déjà des notifications par courrier électronique aux membres du groupe **TenantAdmins** (**administrateurs globaux**) lorsque les utilisateurs sont bloqués en raison du dépassement des limites de la section **limites des destinataires** .</span><span class="sxs-lookup"><span data-stu-id="4dece-177">The default [alert policy](../../compliance/alert-policies.md) named **User restricted from sending email** already sends email notifications to members of the **TenantAdmins** (**Global admins**) group when users are blocked due to exceeding the limits in the **Recipient Limits** section.</span></span> <span data-ttu-id="4dece-178">Nous vous recommandons d’utiliser la stratégie d’alerte au lieu de ce paramètre dans la stratégie anti-courrier indésirable sortant pour avertir les administrateurs et les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4dece-178">We recommend that you use the alert policy rather than this setting in the outbound spam policy to notify admins and other users.</span></span> <span data-ttu-id="4dece-179">Pour obtenir des instructions, consultez [la rubrique vérifier les paramètres d’alerte pour les utilisateurs restreints](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span><span class="sxs-lookup"><span data-stu-id="4dece-179">For instructions, see [Verify the alert settings for restricted users](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users).</span></span>

     <span data-ttu-id="4dece-180">Pour activer ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="4dece-180">To enable this setting:</span></span>

     <span data-ttu-id="4dece-181">a.</span><span class="sxs-lookup"><span data-stu-id="4dece-181">a.</span></span> <span data-ttu-id="4dece-182">Activez la case à cocher pour activer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="4dece-182">Select the check box to enable the setting.</span></span>

     <span data-ttu-id="4dece-183">b.</span><span class="sxs-lookup"><span data-stu-id="4dece-183">b.</span></span> <span data-ttu-id="4dece-184">Cliquez sur **Ajouter des personnes**.</span><span class="sxs-lookup"><span data-stu-id="4dece-184">Click **Add people**.</span></span> <span data-ttu-id="4dece-185">Dans la fenêtre mobile **Ajouter ou supprimer des destinataires** qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="4dece-185">In the **Add or remove recipients** flyout that appears:</span></span>

     <span data-ttu-id="4dece-186">c.</span><span class="sxs-lookup"><span data-stu-id="4dece-186">c.</span></span> <span data-ttu-id="4dece-187">Entrez l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4dece-187">Enter the sender's email address.</span></span> <span data-ttu-id="4dece-188">Vous pouvez spécifier plusieurs adresses de messagerie séparées par des points-virgules (;) ou un destinataire par ligne.</span><span class="sxs-lookup"><span data-stu-id="4dece-188">You can specify multiple email addresses separated by semicolons (;) or one recipient per line.</span></span>

     <span data-ttu-id="4dece-189">d.</span><span class="sxs-lookup"><span data-stu-id="4dece-189">d.</span></span> <span data-ttu-id="4dece-190">Clic </span><span class="sxs-lookup"><span data-stu-id="4dece-190">Click</span></span> ![Icône Ajouter](../../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) <span data-ttu-id="4dece-192">pour ajouter les destinataires.</span><span class="sxs-lookup"><span data-stu-id="4dece-192">to add the recipients.</span></span>

        <span data-ttu-id="4dece-193">Répétez ces étapes autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4dece-193">Repeat these steps as many times as necessary.</span></span>

        <span data-ttu-id="4dece-194">Les destinataires que vous avez ajoutés apparaissent dans la section **liste des destinataires** du menu volant.</span><span class="sxs-lookup"><span data-stu-id="4dece-194">The recipients you added appear in the **Recipient list** section on the flyout.</span></span> <span data-ttu-id="4dece-195">Pour supprimer un destinataire, cliquez ![sur le](../../media/scc-remove-icon.png)bouton supprimer.</span><span class="sxs-lookup"><span data-stu-id="4dece-195">To delete a recipient, click ![Remove button](../../media/scc-remove-icon.png).</span></span>

     <span data-ttu-id="4dece-196">e.</span><span class="sxs-lookup"><span data-stu-id="4dece-196">e.</span></span> <span data-ttu-id="4dece-197">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4dece-197">When you're finished, click **Save**.</span></span>

     <span data-ttu-id="4dece-198">Pour désactiver ce paramètre, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="4dece-198">To disable this setting, clear the check box.</span></span>

5. <span data-ttu-id="4dece-199">Module Développez la section **limites des destinataires** pour configurer les limites et les actions pour les messages électroniques sortants suspects :</span><span class="sxs-lookup"><span data-stu-id="4dece-199">(Optional) Expand the **Recipient Limits** section to configure the limits and actions for suspicious outbound email messages:</span></span>

   > [!NOTE]
   > <span data-ttu-id="4dece-200">Ces paramètres ne s’appliquent qu’aux boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="4dece-200">These settings are only applicable to cloud-based mailboxes.</span></span>
     
   - <span data-ttu-id="4dece-201">**Nombre maximal de destinataires par utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4dece-201">**Maximum number of recipients per user**</span></span>

     <span data-ttu-id="4dece-202">Une valeur valide est comprise entre 0 et 10000.</span><span class="sxs-lookup"><span data-stu-id="4dece-202">A valid value is 0 to 10000.</span></span> <span data-ttu-id="4dece-203">La valeur par défaut est 0, ce qui signifie que les valeurs par défaut du service sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="4dece-203">The default value is 0, which means the service defaults are used.</span></span> <span data-ttu-id="4dece-204">Pour plus d’informations, consultez la rubrique [limites d’envoi dans les options Office 365](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span><span class="sxs-lookup"><span data-stu-id="4dece-204">For more information, see [Sending limits across Office 365 options](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span></span>

     - <span data-ttu-id="4dece-205">**Limite horaire externe**: nombre maximal de destinataires externes par heure.</span><span class="sxs-lookup"><span data-stu-id="4dece-205">**External hourly limit**: The maximum number of external recipients per hour.</span></span>

     - <span data-ttu-id="4dece-206">**Limite horaire interne**: nombre maximal de destinataires internes par heure.</span><span class="sxs-lookup"><span data-stu-id="4dece-206">**Internal hourly limit**: The maximum number of internal recipients per hour.</span></span>

     - <span data-ttu-id="4dece-207">**Limite journalière**: nombre total maximal de destinataires par jour.</span><span class="sxs-lookup"><span data-stu-id="4dece-207">**Daily limit**: The maximum total number of recipients per day.</span></span>

   - <span data-ttu-id="4dece-208">**Action lorsqu’un utilisateur dépasse les limites ci-dessus**: configurez l’action à effectuer lorsque l’une des **limites de destinataires** est dépassée.</span><span class="sxs-lookup"><span data-stu-id="4dece-208">**Action when a user exceeds the limits above**: Configure the action to take when any one of the **Recipient Limits** are exceeded.</span></span> <span data-ttu-id="4dece-209">Pour toutes les actions, les destinataires spécifiés dans l’utilisateur ne peuvent pas **Envoyer de stratégie d’alerte par courrier électronique** (et dans le paramètre à présent, **avertir les personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant** dans la stratégie de courrier indésirable sortant reçoit des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="4dece-209">For all actions, the recipients specified in the **User restricted from sending email** alert policy (and in the now redundant **Notify specific people if a sender is blocked due to sending outbound spam** setting in the outbound spam policy receive email notifications.</span></span>

     - <span data-ttu-id="4dece-210">**Empêcher l’utilisateur d’envoyer des messages jusqu’au jour suivant**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-210">**Restrict the user from sending mail till the following day**: This is the default value.</span></span> <span data-ttu-id="4dece-211">Les notifications par courrier électronique sont envoyées et l’utilisateur ne peut plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="4dece-211">Email notifications are sent, and the user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="4dece-212">L’administrateur n’a aucun moyen de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="4dece-212">There is no way for the admin to override this block.</span></span>

       - <span data-ttu-id="4dece-213">L’activité alerte nommée **utilisateur restreint de l’envoi de courrier électronique** avertit les administrateurs (par e-mail et sur la page **afficher les alertes** ).</span><span class="sxs-lookup"><span data-stu-id="4dece-213">The activity alert named **User restricted from sending email** notifies admins (via email and on the **View alerts** page).</span></span>

       - <span data-ttu-id="4dece-214">Tous les destinataires spécifiés dans le paramètre **informer des personnes spécifiques si un expéditeur est bloqué en raison de l’envoi de courrier indésirable sortant** dans la stratégie sont également avertis.</span><span class="sxs-lookup"><span data-stu-id="4dece-214">Any recipients specified in the **Notify specific people if a sender is blocked due to sending outbound spam** setting in the policy are also notified.</span></span>

       - <span data-ttu-id="4dece-215">L’utilisateur ne peut plus envoyer de messages avant le jour suivant, en fonction de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="4dece-215">The user will be unable to send any more messages until the following day, based on UTC time.</span></span> <span data-ttu-id="4dece-216">L’administrateur n’a aucun moyen de remplacer ce bloc.</span><span class="sxs-lookup"><span data-stu-id="4dece-216">There is no way for the admin to override this block.</span></span>

     - <span data-ttu-id="4dece-217">**Empêcher l’utilisateur d’envoyer des courriers**électroniques : les notifications par courrier électronique sont envoyées, l’utilisateur est ajouté au portail \*\*[utilisateurs restreints]<https://sip.protection.office.com/restrictedusers> \*\* dans le centre de sécurité & conformité et l’utilisateur ne peut pas envoyer de courrier électronique tant qu’il n’a pas été supprimé du portail **utilisateurs restreints** par un administrateur. Une fois qu’un administrateur a supprimé l’utilisateur de la liste, l’utilisateur n’est plus relimité pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="4dece-217">**Restrict the user from sending mail**: Email notifications are sent, the user is added to the **[Restricted Users]<https://sip.protection.office.com/restrictedusers>** portal in the Security & Compliance Center, and the user can't send email until they're removed from the **Restricted Users** portal by an admin. After an admin removes the user from the list, the user won't be restricted again for that day.</span></span> <span data-ttu-id="4dece-218">Pour obtenir des instructions, consultez [la rubrique Suppression d’un utilisateur du portail utilisateurs restreints après l’envoi du courrier indésirable](removing-user-from-restricted-users-portal-after-spam.md).</span><span class="sxs-lookup"><span data-stu-id="4dece-218">For instructions, see [Removing a user from the Restricted Users portal after sending spam email](removing-user-from-restricted-users-portal-after-spam.md).</span></span>

     - <span data-ttu-id="4dece-219">**Aucune action, alerte uniquement**: les notifications par courrier électronique sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="4dece-219">**No action, alert only**: Email notifications are sent.</span></span>

6. <span data-ttu-id="4dece-220">Exige Développez la section **appliqué à** pour identifier les expéditeurs internes auxquels la stratégie s’applique.</span><span class="sxs-lookup"><span data-stu-id="4dece-220">(Required) Expand the **Applied to** section to identify the internal senders that the policy applies to.</span></span>

    <span data-ttu-id="4dece-221">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="4dece-221">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="4dece-222">Plusieurs valeurs de la même condition ou de l’utilisation ou de la logique d’exception (par exemple, _ \<sender1\> _ ou _ \<sender2\>_).</span><span class="sxs-lookup"><span data-stu-id="4dece-222">Multiple values of the same condition or exception use OR logic (for example, _\<sender1\>_ or _\<sender2\>_).</span></span> <span data-ttu-id="4dece-223">Différentes conditions ou exceptions utilisent et logique (par exemple, _ \<sender1\> _ et _ \<membre du groupe 1\>_).</span><span class="sxs-lookup"><span data-stu-id="4dece-223">Different conditions or exceptions use AND logic (for example, _\<sender1\>_ and _\<member of group 1\>_).</span></span>

    <span data-ttu-id="4dece-224">Il est plus facile de cliquer sur**Ajouter une condition** trois fois pour afficher toutes les conditions disponibles.</span><span class="sxs-lookup"><span data-stu-id="4dece-224">It's easiest to click **Add a condition** three times to see all of the available conditions.</span></span> <span data-ttu-id="4dece-225">Vous pouvez cliquer sur le ![bouton Supprimer](../../media/scc-remove-icon.png) pour supprimer les conditions que vous ne voulez pas configurer.</span><span class="sxs-lookup"><span data-stu-id="4dece-225">You can click ![Remove button](../../media/scc-remove-icon.png) to remove conditions that you don't want to configure.</span></span>

    - <span data-ttu-id="4dece-226">**Le domaine de l’expéditeur est**: spécifie les expéditeurs dans un ou plusieurs des domaines acceptés configurés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="4dece-226">**The sender domain is**: Specifies senders in one or more of the configured accepted domains in Office 365.</span></span> <span data-ttu-id="4dece-227">Cliquez dans la zone **Ajouter un indicateur** pour afficher et sélectionner un domaine.</span><span class="sxs-lookup"><span data-stu-id="4dece-227">Click in the **Add a tag** box to see and select a domain.</span></span> <span data-ttu-id="4dece-228">Cliquez de nouveau sur la zone **Ajouter un indicateur** pour sélectionner d’autres domaines si plusieurs domaines sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4dece-228">Click again the **Add a tag** box to select additional domains if more than one domain is available.</span></span>

    - <span data-ttu-id="4dece-229">L' **expéditeur est**: spécifie un ou plusieurs utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4dece-229">**Sender is**: Specifies one or more users in your organization.</span></span> <span data-ttu-id="4dece-230">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="4dece-230">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="4dece-231">Cliquez de nouveau sur la zone **Ajouter une balise** pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4dece-231">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="4dece-232">L' **expéditeur est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4dece-232">**Sender is a member of**: Specifies one or more groups in your organization.</span></span> <span data-ttu-id="4dece-233">Cliquez sur **Ajouter un indicateur** et commencez à taper pour filtrer la liste.</span><span class="sxs-lookup"><span data-stu-id="4dece-233">Click in the **Add a tag** and start typing to filter the list.</span></span> <span data-ttu-id="4dece-234">Cliquez de nouveau sur la zone **Ajouter une balise** pour sélectionner des expéditeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4dece-234">Click again the **Add a tag** box to select additional senders.</span></span>

    - <span data-ttu-id="4dece-235">**Sauf si**: pour ajouter des exceptions à la règle, cliquez sur **Ajouter une condition** trois fois pour afficher toutes les exceptions disponibles.</span><span class="sxs-lookup"><span data-stu-id="4dece-235">**Except if**: To add exceptions for the rule, click **Add a condition** three times to see all of the available exceptions.</span></span> <span data-ttu-id="4dece-236">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="4dece-236">The settings and behavior are exactly like the conditions.</span></span>

7. <span data-ttu-id="4dece-237">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4dece-237">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-view-outbound-spam-policies"></a><span data-ttu-id="4dece-238">Utiliser le centre de sécurité & conformité pour afficher les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-238">Use the Security & Compliance Center to view outbound spam policies</span></span>

1. <span data-ttu-id="4dece-239">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-239">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-240">Sur la page **paramètres de blocage du courrier indésirable** , cliquez sur ![développer une icône](../../media/scc-expand-icon.png) pour développer une stratégie de courrier indésirable sortant :</span><span class="sxs-lookup"><span data-stu-id="4dece-240">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="4dece-241">Stratégie par défaut nommée **stratégie de filtrage du courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="4dece-241">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="4dece-242">Une stratégie personnalisée que vous avez créée où la valeur dans la colonne **type** est **personnalisée stratégie anti-courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="4dece-242">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="4dece-243">Les paramètres de stratégie sont affichés dans les détails de stratégie développés qui s’affichent, ou vous pouvez cliquer sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4dece-243">The policy settings are displayed in the expanded policy details that appear, or you can click **Edit policy**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-outbound-spam-policies"></a><span data-ttu-id="4dece-244">Utiliser le centre de sécurité & conformité pour modifier les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-244">Use the Security & Compliance Center to modify outbound spam policies</span></span>

1. <span data-ttu-id="4dece-245">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-245">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-246">Sur la page **paramètres de blocage du courrier indésirable** , cliquez sur ![développer une icône](../../media/scc-expand-icon.png) pour développer une stratégie de courrier indésirable sortant :</span><span class="sxs-lookup"><span data-stu-id="4dece-246">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand an outbound spam policy:</span></span>

   - <span data-ttu-id="4dece-247">Stratégie par défaut nommée **stratégie de filtrage du courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="4dece-247">The default policy named **Outbound spam filter policy**.</span></span>

   - <span data-ttu-id="4dece-248">Une stratégie personnalisée que vous avez créée où la valeur dans la colonne **type** est **personnalisée stratégie anti-courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="4dece-248">A custom policy that you created where the value in the **Type** column is **Custom outbound spam policy**.</span></span>

3. <span data-ttu-id="4dece-249">Cliquez sur **Modifier une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4dece-249">Click **Edit policy**.</span></span>

<span data-ttu-id="4dece-250">Pour les stratégies de courrier indésirable sortant personnalisé, les paramètres disponibles dans le menu volant qui s’affiche sont identiques à ceux décrits dans la section [utiliser le centre de sécurité & conformité pour créer des stratégies de courrier indésirable sortant](#use-the-security--compliance-center-to-create-outbound-spam-policies) .</span><span class="sxs-lookup"><span data-stu-id="4dece-250">For custom outbound spam policies, the available settings in the flyout that appears are identical to those described in the [Use the Security & Compliance Center to create outbound spam policies](#use-the-security--compliance-center-to-create-outbound-spam-policies) section.</span></span>

<span data-ttu-id="4dece-251">Pour la stratégie de courrier indésirable sortant par défaut nommée **stratégie de filtrage du courrier indésirable sortant**, la section **appliqué à** n’est pas disponible (la stratégie s’applique à tout le monde) et vous ne pouvez pas renommer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4dece-251">For the default outbound spam policy named **Outbound spam filter policy**, the **Applied to** section isn't available (the policy applies to everyone), and you can't rename the policy.</span></span>

<span data-ttu-id="4dece-252">Pour activer ou désactiver une stratégie, définir l’ordre de priorité de la stratégie ou configurer les notifications de mise en quarantaine de l’utilisateur final, voir les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4dece-252">To enable or disable a policy, set the policy priority order, or configure the end-user quarantine notifications, see the following sections.</span></span>

### <a name="enable-or-disable-outbound-spam-policies"></a><span data-ttu-id="4dece-253">Activer ou désactiver les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-253">Enable or disable outbound spam policies</span></span>

1. <span data-ttu-id="4dece-254">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-254">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-255">Dans la page **paramètres de blocage du courrier indésirable** , cliquez sur ![développer une icône](../../media/scc-expand-icon.png) pour développer une stratégie personnalisée que vous avez créée (la valeur dans la colonne **type** est **stratégie courrier indésirable sortant personnalisé**).</span><span class="sxs-lookup"><span data-stu-id="4dece-255">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand a custom policy that you created (the value in the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="4dece-256">Dans les détails de la stratégie développée qui s’affichent, notez la valeur dans la colonne**Activé**.</span><span class="sxs-lookup"><span data-stu-id="4dece-256">In the expanded policy details that appear, notice the value in the **On** column.</span></span>

   <span data-ttu-id="4dece-257">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="4dece-257">Move the toggle to the left to disable the policy:</span></span> ![Désactiver](../../media/scc-toggle-off.png)

   <span data-ttu-id="4dece-259">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="4dece-259">Move the toggle to the right to enable the policy:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)

<span data-ttu-id="4dece-261">Vous ne pouvez pas désactiver la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-261">You can't disable the default outbound spam policy.</span></span>

### <a name="set-the-priority-of-custom-outbound-spam-policies"></a><span data-ttu-id="4dece-262">Définir la priorité des stratégies de courrier indésirable sortant personnalisé</span><span class="sxs-lookup"><span data-stu-id="4dece-262">Set the priority of custom outbound spam policies</span></span>

<span data-ttu-id="4dece-263">Par défaut, les stratégies de courrier indésirable sortant reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="4dece-263">By default, outbound spam policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="4dece-264">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="4dece-264">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="4dece-265">Deux stratégies ne peuvent pas avoir la même priorité.</span><span class="sxs-lookup"><span data-stu-id="4dece-265">No two policies can have the same priority.</span></span>

<span data-ttu-id="4dece-266">Les stratégies de courrier indésirable sortant personnalisé sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="4dece-266">Custom outbound spam policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="4dece-267">La stratégie de courrier indésirable sortant par défaut nommée **stratégie de filtrage du courrier indésirable sortant** a la valeur Priority la **plus faible**et vous ne pouvez pas la modifier.</span><span class="sxs-lookup"><span data-stu-id="4dece-267">The default outbound spam policy named **Outbound spam filter policy** has the priority value **Lowest**, and you can't change it.</span></span>

<span data-ttu-id="4dece-268">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="4dece-268">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="4dece-269">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-269">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-270">Dans la page **paramètres de blocage du courrier indésirable** , recherchez les stratégies pour lesquelles la valeur dans la colonne **type** est **Custom courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="4dece-270">On the **Anti-spam settings** page, find the policies where the value in the **Type** column is **Custom outbound spam policy**.</span></span> <span data-ttu-id="4dece-271">Notez les valeurs de la colonne**Priorité** :</span><span class="sxs-lookup"><span data-stu-id="4dece-271">Notice the values in the **Priority** column:</span></span>

   - <span data-ttu-id="4dece-272">La stratégie de courrier indésirable sortant personnalisé avec la priorité la ![plus élevée a](../../media/ITPro-EAC-DownArrowIcon.png) la valeur flèche vers le bas **0**.</span><span class="sxs-lookup"><span data-stu-id="4dece-272">The custom outbound spam policy with the highest priority has the value ![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **0**.</span></span>

   - <span data-ttu-id="4dece-273">La stratégie de courrier indésirable sortant personnalisé avec la priorité la ![plus faible est](../../media/ITPro-EAC-UpArrowIcon.png) dotée de l’icône ![de flèche haut](../../media/ITPro-EAC-UpArrowIcon.png) **n** (par exemple, icône flèche haut **3**).</span><span class="sxs-lookup"><span data-stu-id="4dece-273">The custom outbound spam policy with the lowest priority has the value ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png) **3**).</span></span>

   - <span data-ttu-id="4dece-274">Si vous avez au moins trois stratégies de courrier indésirable sortant personnalisées, les stratégies comprises entre ![la priorité la](../../media/ITPro-EAC-UpArrowIcon.png)![plus élevée et](../../media/ITPro-EAC-DownArrowIcon.png) la priorité la plus faible ont une icône](../../media/ITPro-EAC-UpArrowIcon.png)![flèche vers le](../../media/ITPro-EAC-DownArrowIcon.png) bas de l’icône **n** (par exemple, icône flèche vers le bas, ![icône **2**).</span><span class="sxs-lookup"><span data-stu-id="4dece-274">If you have three or more custom outbound spam policies, the policies between the highest and lowest priority have values ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **n** (for example, ![Up Arrow icon](../../media/ITPro-EAC-UpArrowIcon.png)![Down Arrow icon](../../media/ITPro-EAC-DownArrowIcon.png) **2**).</span></span>

3. <span data-ttu-id="4dece-275">Clic </span><span class="sxs-lookup"><span data-stu-id="4dece-275">Click</span></span> ![Icône de flèche vers le haut](../../media/ITPro-EAC-UpArrowIcon.png) <span data-ttu-id="4dece-277">ou</span><span class="sxs-lookup"><span data-stu-id="4dece-277">or</span></span> ![Icône de flèche vers le bas](../../media/ITPro-EAC-DownArrowIcon.png) <span data-ttu-id="4dece-279">pour déplacer la stratégie de courrier indésirable sortant personnalisé vers le haut ou vers le bas dans la liste priorité.</span><span class="sxs-lookup"><span data-stu-id="4dece-279">to move the custom outbound spam policy up or down in the priority list.</span></span>

## <a name="use-the-security--compliance-center-to-remove-outbound-spam-policies"></a><span data-ttu-id="4dece-280">Utiliser le centre de sécurité & conformité pour supprimer les stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-280">Use the Security & Compliance Center to remove outbound spam policies</span></span>

1. <span data-ttu-id="4dece-281">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4dece-281">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="4dece-282">Dans la page **paramètres de blocage du courrier indésirable** , cliquez sur ![développer](../../media/scc-expand-icon.png) pour développer la stratégie personnalisée à supprimer (la colonne **type** est **personnalisée courrier indésirable sortant**).</span><span class="sxs-lookup"><span data-stu-id="4dece-282">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand the custom policy that you want to delete (the **Type** column is **Custom outbound spam policy**).</span></span>

3. <span data-ttu-id="4dece-283">Dans les détails de la stratégie développée qui s’affichent, cliquez sur **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4dece-283">In the expanded policy details that appear, click **Delete policy**.</span></span>

4. <span data-ttu-id="4dece-284">Cliquez sur **Oui** lorsque la boîte de dialogue d’avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4dece-284">Click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="4dece-285">Vous ne pouvez pas supprimer la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-285">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-outbound-spam-policies"></a><span data-ttu-id="4dece-286">Utiliser Exchange Online PowerShell ou Exchange Online Protection PowerShell pour configurer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-286">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure outbound spam policies</span></span>

### <a name="use-powershell-to-create-outbound-spam-policies"></a><span data-ttu-id="4dece-287">Utiliser PowerShell pour créer des stratégies de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-287">Use PowerShell to create outbound spam policies</span></span>

<span data-ttu-id="4dece-288">La création d’une stratégie de courrier indésirable sortant dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="4dece-288">Creating an outbound spam policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="4dece-289">Créez la stratégie de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-289">Create the outbound spam filter policy.</span></span>

2. <span data-ttu-id="4dece-290">Créez la règle de filtrage du courrier indésirable sortant qui spécifie la stratégie de filtrage du courrier indésirable sortant à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="4dece-290">Create the outbound spam filter rule that specifies the outbound spam filter policy that the rule applies to.</span></span>

 <span data-ttu-id="4dece-291">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4dece-291">**Notes**:</span></span>

- <span data-ttu-id="4dece-292">Vous pouvez créer une règle de filtrage du courrier indésirable sortant et lui affecter une stratégie de filtrage du courrier indésirable sortant existante non associée.</span><span class="sxs-lookup"><span data-stu-id="4dece-292">You can create a new outbound spam filter rule and assign an existing, unassociated outbound spam filter policy to it.</span></span> <span data-ttu-id="4dece-293">Une règle de filtrage du courrier indésirable sortant ne peut pas être associée à plusieurs stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-293">An outbound spam filter rule can't be associated with more than one outbound spam filter policy.</span></span>

- <span data-ttu-id="4dece-294">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de filtrage du courrier indésirable sortant dans PowerShell qui ne sont pas disponibles dans le centre de sécurité & de sécurité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="4dece-294">You can configure the following settings on new outbound spam filter policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="4dece-295">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-HostedOutboundSpamFilterRule** ).</span><span class="sxs-lookup"><span data-stu-id="4dece-295">Create the new policy as disabled (_Enabled_ `$false` on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>

  - <span data-ttu-id="4dece-296">Définir la priorité de la stratégie lors de la création ( _ \<numéro\>_ de_priorité_ ) sur la cmdlet **New-HostedOutboundSpamFilterRule** ).</span><span class="sxs-lookup"><span data-stu-id="4dece-296">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-HostedOutboundSpamFilterRule** cmdlet).</span></span>

- <span data-ttu-id="4dece-297">Une nouvelle stratégie de filtrage du courrier indésirable sortant que vous créez dans PowerShell n’est pas visible dans le centre de sécurité & de conformité tant que vous n’affectez pas la stratégie à une règle de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4dece-297">A new outbound spam filter policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a spam filter rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-outbound-spam-filter-policy"></a><span data-ttu-id="4dece-298">Étape 1 : utiliser PowerShell pour créer une stratégie de filtrage des courriers indésirables sortants</span><span class="sxs-lookup"><span data-stu-id="4dece-298">Step 1: Use PowerShell to create an outbound spam filter policy</span></span>

<span data-ttu-id="4dece-299">Pour créer une stratégie de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-299">To create an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="4dece-300">Cet exemple crée une stratégie de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4dece-300">This example creates a new outbound spam filter policy named Contoso Executives with the following settings:</span></span>

- <span data-ttu-id="4dece-301">Les limites de taux de destinataires sont limitées aux valeurs plus petites que celles par défaut.</span><span class="sxs-lookup"><span data-stu-id="4dece-301">The recipient rate limits are restricted to smaller values that the defaults.</span></span> <span data-ttu-id="4dece-302">Pour plus d’informations, consultez la rubrique [limites d’envoi dans les options Office 365](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span><span class="sxs-lookup"><span data-stu-id="4dece-302">For more information, see [Sending limits across Office 365 options](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options).</span></span>

- <span data-ttu-id="4dece-303">Une fois que l’une des limites est atteinte, l’utilisateur ne peut pas envoyer de messages.</span><span class="sxs-lookup"><span data-stu-id="4dece-303">After one of the limits is reached, the user is prevented from sending messages.</span></span>

```PowerShell
New-HostedOutboundSpamFilterPolicy -Name "Contoso Executives" -RecipientLimitExternalPerHour 400 -RecipientLimitInternalPerHour 800 -RecipientLimitPerDay 800 -ActionWhenThresholdReached BlockUser
```

<span data-ttu-id="4dece-304">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/new-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="4dece-304">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/new-hostedoutboundspamfilterpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-outbound-spam-filter-rule"></a><span data-ttu-id="4dece-305">Étape 2 : utiliser PowerShell pour créer une règle de filtrage des courriers indésirables sortants</span><span class="sxs-lookup"><span data-stu-id="4dece-305">Step 2: Use PowerShell to create an outbound spam filter rule</span></span>

<span data-ttu-id="4dece-306">Pour créer une règle de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-306">To create an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "<RuleName>" -HostedOutboundSpamFilterPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="4dece-307">Cet exemple crée une règle de filtrage du courrier indésirable sortant nommée Contoso Executives avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4dece-307">This example creates a new outbound spam filter rule named Contoso Executives with these settings:</span></span>

- <span data-ttu-id="4dece-308">La stratégie de filtrage du courrier indésirable sortant nommé Contoso Executives est associée à la règle.</span><span class="sxs-lookup"><span data-stu-id="4dece-308">The outbound spam filter policy named Contoso Executives is associated with the rule.</span></span>

- <span data-ttu-id="4dece-309">La règle s’applique aux membres du groupe nommé Groupe Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="4dece-309">The rule applies to members of the group named Contoso Executives Group.</span></span>

```PowerShell
New-HostedOutboundSpamFilterRule -Name "Contoso Executives" -HostedOutboundSpamFilterPolicy "Contoso Executives" -SentToMemberOf "Contoso Executives Group"
```

<span data-ttu-id="4dece-310">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/new-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="4dece-310">For detailed syntax and parameter information, see [New-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/new-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-policies"></a><span data-ttu-id="4dece-311">Utiliser PowerShell pour afficher les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-311">Use PowerShell to view outbound spam filter policies</span></span>

<span data-ttu-id="4dece-312">Pour renvoyer une liste récapitulative de toutes les stratégies de filtrage du courrier indésirable sortant, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-312">To return a summary list of all outbound spam filter policies, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy
```

<span data-ttu-id="4dece-313">Pour renvoyer des informations détaillées sur une stratégie de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-313">To return detailed information about a specific outbound spam filter policy, use the this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="4dece-314">Cet exemple renvoie toutes les valeurs de propriété pour la stratégie de filtrage du courrier indésirable sortant nommée Executives.</span><span class="sxs-lookup"><span data-stu-id="4dece-314">This example returns all the property values for the outbound spam filter policy named Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterPolicy -Identity "Executives" | Format-List
```

<span data-ttu-id="4dece-315">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="4dece-315">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-view-outbound-spam-filter-rules"></a><span data-ttu-id="4dece-316">Utiliser PowerShell pour afficher les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-316">Use PowerShell to view outbound spam filter rules</span></span>

<span data-ttu-id="4dece-317">Pour afficher les règles de filtrage de courrier indésirable sortant existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-317">To view existing outbound spam filter rules, use the following syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule [-Identity "<RuleIdentity>] [-State <Enabled | Disabled]
```

<span data-ttu-id="4dece-318">Pour renvoyer une liste récapitulative de toutes les règles de filtrage du courrier indésirable sortant, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-318">To return a summary list of all outbound spam filter rules, run this command:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule
```

<span data-ttu-id="4dece-319">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dece-319">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -State Disabled
```

```PowerShell
Get-HostedOutboundSpamFilterRule -State Enabled
```

<span data-ttu-id="4dece-320">Pour renvoyer des informations détaillées sur une règle de filtrage du courrier indésirable sortant spécifique, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-320">To return detailed information about a specific outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "<RuleName>" | Format-List [<Specific properties to view>]
```

<span data-ttu-id="4dece-321">Cet exemple renvoie toutes les valeurs de propriété pour la règle de filtrage du courrier indésirable sortant nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="4dece-321">This example returns all the property values for the outbound spam filter rule named Contoso Executives.</span></span>

```PowerShell
Get-HostedOutboundSpamFilterRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="4dece-322">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="4dece-322">For detailed syntax and parameter information, see [Get-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-policies"></a><span data-ttu-id="4dece-323">Utiliser PowerShell pour modifier les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-323">Use PowerShell to modify outbound spam filter policies</span></span>

<span data-ttu-id="4dece-324">Les mêmes paramètres sont disponibles lorsque vous modifiez une stratégie de filtrage des programmes malveillants dans PowerShell comme lors de la création de la stratégie, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie de filtrage du courrier indésirable sortant](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4dece-324">The same settings are available when you modify a malware filter policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an outbound spam filter policy](#step-1-use-powershell-to-create-an-outbound-spam-filter-policy) section earlier in this topic.</span></span>

<span data-ttu-id="4dece-325">**Remarque**: vous ne pouvez pas renommer une stratégie de filtrage du courrier indésirable sortant (la cmdlet **Set-HostedOutboundSpamFilterPolicy** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="4dece-325">**Note**: You can't rename an outbound spam filter policy (the **Set-HostedOutboundSpamFilterPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="4dece-326">Lorsque vous renommez une stratégie de courrier indésirable sortant dans le centre de sécurité & conformité, vous renommez uniquement la _règle_de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="4dece-326">When you rename an outbound spam policy in the Security & Compliance Center, you're only renaming the outbound spam filter _rule_.</span></span>

<span data-ttu-id="4dece-327">Pour modifier une stratégie de filtrage des courriers indésirables sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-327">To modify an outbound spam filter policy, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="4dece-328">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="4dece-328">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-modify-outbound-spam-filter-rules"></a><span data-ttu-id="4dece-329">Utiliser PowerShell pour modifier les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-329">Use PowerShell to modify outbound spam filter rules</span></span>

<span data-ttu-id="4dece-330">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="4dece-330">The only setting that isn't available when you modify an outbound spam filter rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="4dece-331">Pour activer ou désactiver les règles de filtrage de courrier indésirable sortant existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="4dece-331">To enable or disable existing outbound spam filter rules, see the next section.</span></span>

<span data-ttu-id="4dece-332">Dans le cas contraire, aucun paramètre supplémentaire n’est disponible lorsque vous modifiez une règle de filtrage du courrier indésirable sortant dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4dece-332">Otherwise, no additional settings are available when you modify an outbound spam filter rule in PowerShell.</span></span> <span data-ttu-id="4dece-333">Les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle de filtrage du courrier indésirable sortant](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4dece-333">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an outbound spam filter rule](#step-2-use-powershell-to-create-an-outbound-spam-filter-rule) section earlier in this topic.</span></span>

<span data-ttu-id="4dece-334">Pour modifier une règle de filtrage du courrier indésirable sortant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-334">To modify an outbound spam filter rule, use this syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="4dece-335">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="4dece-335">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-outbound-spam-filter-rules"></a><span data-ttu-id="4dece-336">Utiliser PowerShell pour activer ou désactiver les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-336">Use PowerShell to enable or disable outbound spam filter rules</span></span>

<span data-ttu-id="4dece-337">L’activation ou la désactivation d’une règle de filtrage du courrier indésirable sortant dans PowerShell active ou désactive la totalité de la stratégie anti-courrier indésirable sortant (la règle de filtrage du courrier indésirable sortant et la stratégie de filtrage du courrier indésirable sortant affecté).</span><span class="sxs-lookup"><span data-stu-id="4dece-337">Enabling or disabling an outbound spam filter rule in PowerShell enables or disables the whole outbound spam policy (the outbound spam filter rule and the assigned outbound spam filter policy).</span></span> <span data-ttu-id="4dece-338">Vous ne pouvez pas activer ou désactiver la stratégie de courrier indésirable sortant par défaut (elle est toujours appliquée à tous les destinataires).</span><span class="sxs-lookup"><span data-stu-id="4dece-338">You can't enable or disable the default outbound spam policy (it's always always applied to all recipients).</span></span>

<span data-ttu-id="4dece-339">Pour activer ou désactiver une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-339">To enable or disable an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-HostedOutboundSpamFilterRule | Disable-HostedOutboundSpamFilterRule> -Identity "<RuleName>"
```

<span data-ttu-id="4dece-340">Cet exemple désactive la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4dece-340">This example disables the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Disable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="4dece-341">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="4dece-341">This example enables same rule.</span></span>

```PowerShell
Enable-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="4dece-342">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/enable-hostedoutboundspamfilterrule) et [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/disable-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="4dece-342">For detailed syntax and parameter information, see [Enable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/enable-hostedoutboundspamfilterrule) and [Disable-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/disable-hostedoutboundspamfilterrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-outbound-spam-filter-rules"></a><span data-ttu-id="4dece-343">Utiliser PowerShell pour définir la priorité des règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-343">Use PowerShell to set the priority of outbound spam filter rules</span></span>

<span data-ttu-id="4dece-344">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="4dece-344">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="4dece-345">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="4dece-345">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="4dece-346">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="4dece-346">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="4dece-347">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="4dece-347">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="4dece-348">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="4dece-348">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="4dece-349">Pour définir la priorité d’une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-349">To set the priority of an outbound spam filter rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="4dece-p146">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="4dece-p146">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-HostedOutboundSpamFilterRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="4dece-352">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="4dece-352">**Notes**:</span></span>

- <span data-ttu-id="4dece-353">Pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-HostedOutboundSpamFilterRule** .</span><span class="sxs-lookup"><span data-stu-id="4dece-353">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-HostedOutboundSpamFilterRule** cmdlet instead.</span></span>

- <span data-ttu-id="4dece-354">La stratégie de filtrage du courrier indésirable par défaut sortante n’a pas de règle de filtrage du courrier indésirable correspondante et a toujours la valeur de priorité non modifiable la **plus faible**.</span><span class="sxs-lookup"><span data-stu-id="4dece-354">The outbound default spam filter policy doesn't have a corresponding spam filter rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-policies"></a><span data-ttu-id="4dece-355">Utiliser PowerShell pour supprimer les stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-355">Use PowerShell to remove outbound spam filter policies</span></span>

<span data-ttu-id="4dece-356">Lorsque vous utilisez PowerShell pour supprimer une stratégie de filtrage du courrier indésirable sortant, la règle de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="4dece-356">When you use PowerShell to remove an outbound spam filter policy, the corresponding outbound spam filter rule isn't removed.</span></span>

<span data-ttu-id="4dece-357">Pour supprimer une stratégie de filtrage des courriers indésirables sortants dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-357">To remove an outbound spam filter policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="4dece-358">Cet exemple supprime la stratégie de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4dece-358">This example removes the outbound spam filter policy named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterPolicy -Identity "Marketing Department"
```

<span data-ttu-id="4dece-359">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/remove-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="4dece-359">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/remove-hostedoutboundspamfilterpolicy).</span></span>

### <a name="use-powershell-to-remove-outbound-spam-filter-rules"></a><span data-ttu-id="4dece-360">Utiliser PowerShell pour supprimer les règles de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="4dece-360">Use PowerShell to remove outbound spam filter rules</span></span>

<span data-ttu-id="4dece-361">Lorsque vous utilisez PowerShell pour supprimer une règle de filtrage du courrier indésirable sortant, la stratégie de filtrage du courrier indésirable sortant correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="4dece-361">When you use PowerShell to remove an outbound spam filter rule, the corresponding outbound spam filter policy isn't removed.</span></span>

<span data-ttu-id="4dece-362">Pour supprimer une règle de filtrage du courrier indésirable sortant dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4dece-362">To remove an outbound spam filter rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "<PolicyName>"
```

<span data-ttu-id="4dece-363">Cet exemple supprime la règle de filtrage du courrier indésirable sortant nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="4dece-363">This example removes the outbound spam filter rule named Marketing Department.</span></span>

```PowerShell
Remove-HostedOutboundSpamFilterRule -Identity "Marketing Department"
```

<span data-ttu-id="4dece-364">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/remove-hostedoutboundspamfilterrule).</span><span class="sxs-lookup"><span data-stu-id="4dece-364">For detailed syntax and parameter information, see [Remove-HostedOutboundSpamFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/remove-hostedoutboundspamfilterrule).</span></span>

## <a name="for-more-information"></a><span data-ttu-id="4dece-365">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="4dece-365">For more information</span></span>

[<span data-ttu-id="4dece-366">Retirer les utilisateurs bloqués du portail Utilisateurs restreints dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4dece-366">Remove blocked users from the Restricted Users portal in Office 365</span></span>](removing-user-from-restricted-users-portal-after-spam.md)

[<span data-ttu-id="4dece-367">Pool de remise à haut risque pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="4dece-367">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="4dece-368">Forum Aux Questions sur la protection anti-courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4dece-368">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
