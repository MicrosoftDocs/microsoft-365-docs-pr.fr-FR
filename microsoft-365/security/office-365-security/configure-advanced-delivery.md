---
title: Configurer la remise de simulations de hameçonnage tiers aux utilisateurs et de messages non filtrés dans des boîtes aux lettres SecOps
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
ms.collection:
- M365-security-compliance
ms.custom: ''
description: Les administrateurs peuvent apprendre à utiliser la stratégie de remise avancée dans Exchange Online Protection (EOP) pour identifier les messages qui ne doivent pas être filtrés dans des scénarios pris en charge spécifiques (simulations d’hameçonnage tiers et messages remis à des boîtes aux lettres d’opérations de sécurité (SecOps).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 053f88da96983b03ad03e75c11a4fa692ac6a850
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53256866"
---
# <a name="configure-the-delivery-of-third-party-phishing-simulations-to-users-and-unfiltered-messages-to-secops-mailboxes"></a><span data-ttu-id="812c7-103">Configurer la remise de simulations de hameçonnage tiers aux utilisateurs et de messages non filtrés dans des boîtes aux lettres SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-103">Configure the delivery of third-party phishing simulations to users and unfiltered messages to SecOps mailboxes</span></span>

<span data-ttu-id="812c7-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="812c7-104">**Applies to**</span></span>
- [<span data-ttu-id="812c7-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="812c7-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="812c7-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="812c7-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="812c7-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="812c7-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="812c7-108">La fonctionnalité décrite dans cet article est en prévisualisation, n’est pas disponible pour tout le monde et peut faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="812c7-108">The feature that's described in this article is in Preview, isn't available to everyone, and is subject to change.</span></span>

<span data-ttu-id="812c7-109">Pour sécuriser votre organisation par [défaut,](secure-by-default.md)Exchange Online Protection (EOP) n’autorise pas les listes sécurisées ou le contournement de filtrage pour les messages identifiés comme programmes malveillants ou hameçonnage à haut niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="812c7-109">To keep your organization [secure by default](secure-by-default.md), Exchange Online Protection (EOP) does not allow safe lists or filtering bypass for messages that are identified as malware or high confidence phishing.</span></span> <span data-ttu-id="812c7-110">Toutefois, il existe des scénarios spécifiques qui nécessitent la remise de messages non filtrés.</span><span class="sxs-lookup"><span data-stu-id="812c7-110">But, there are specific scenarios that require the delivery of unfiltered messages.</span></span> <span data-ttu-id="812c7-111">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="812c7-111">For example:</span></span>

- <span data-ttu-id="812c7-112">**Simulations de hameçonnage tierces**: les attaques simulées peuvent vous aider à identifier les utilisateurs vulnérables avant qu’une attaque réelle n’impacte votre organisation.</span><span class="sxs-lookup"><span data-stu-id="812c7-112">**Third-party phishing simulations**: Simulated attacks can help you identify vulnerable users before a real attack impacts your organization.</span></span>
- <span data-ttu-id="812c7-113">Boîtes aux lettres d’opérations de sécurité **(SecOps)**: boîtes aux lettres dédiées utilisées par les équipes de sécurité pour collecter et analyser les messages non filtrés (bonnes et mauvaises).</span><span class="sxs-lookup"><span data-stu-id="812c7-113">**Security operations (SecOps) mailboxes**: Dedicated mailboxes that are used by security teams to collect and analyze unfiltered messages (both good and bad).</span></span>

<span data-ttu-id="812c7-114">Vous utilisez la _stratégie de remise_ avancée dans Microsoft 365 pour empêcher le filtrage de ces messages dans ces _scénarios spécifiques._ <sup>\*</sup> La stratégie de remise avancée garantit que les messages dans ces scénarios atteignent les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="812c7-114">You use the _advanced delivery policy_ in Microsoft 365 to prevent these messages _in these specific scenarios_ from being filtered.<sup>\*</sup> The advanced delivery policy ensures that messages in these scenarios achieve the following results:</span></span>

- <span data-ttu-id="812c7-115">Les filtres dans EOP et Microsoft Defender Office 365 aucune action sur ces messages.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="812c7-115">Filters in EOP and Microsoft Defender for Office 365 take no action on these messages.<sup>\*</sup></span></span>
- <span data-ttu-id="812c7-116">[La purge zéro heure (ZAP) pour](zero-hour-auto-purge.md) le courrier indésirable et le hameçonnage n’a aucune action sur ces messages.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="812c7-116">[Zero-hour Purge (ZAP)](zero-hour-auto-purge.md) for spam and phishing take no action on these messages.<sup>\*</sup></span></span>
- <span data-ttu-id="812c7-117">[Les alertes système par](alerts.md) défaut ne sont pas déclenchées pour ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="812c7-117">[Default system alerts](alerts.md) aren't triggered for these scenarios.</span></span>
- <span data-ttu-id="812c7-118">[Air and clustering in Defender for Office 365](office-365-air.md) ignores these messages.</span><span class="sxs-lookup"><span data-stu-id="812c7-118">[AIR and clustering in Defender for Office 365](office-365-air.md) ignores these messages.</span></span>
- <span data-ttu-id="812c7-119">Plus spécifiquement pour les simulations de hameçonnage tierces :</span><span class="sxs-lookup"><span data-stu-id="812c7-119">Specifically for third-party phishing simulations:</span></span>
  - <span data-ttu-id="812c7-120">[Les soumissions d’administrateur](admin-submission.md) génèrent une réponse automatique qui dit que le message fait partie d’une campagne de simulation de hameçonnage et qu’il ne constitue pas une menace réelle.</span><span class="sxs-lookup"><span data-stu-id="812c7-120">[Admin submissions](admin-submission.md) generates an automatic response saying that the message is part of a phishing simulation campaign and isn't a real threat.</span></span> <span data-ttu-id="812c7-121">Les alertes et air ne sont pas déclenchés.</span><span class="sxs-lookup"><span data-stu-id="812c7-121">Alerts and AIR will not be triggered.</span></span>
  - <span data-ttu-id="812c7-122">[Coffre dans Defender pour Office 365](safe-links.md) ne bloque pas ou ne désaxique pas les URL spécifiquement identifiées dans ces messages.</span><span class="sxs-lookup"><span data-stu-id="812c7-122">[Safe Links in Defender for Office 365](safe-links.md) doesn't block or detonate the specifically identified URLs in these messages.</span></span>
  - <span data-ttu-id="812c7-123">[Coffre pièces jointes dans Defender pour Office 365](safe-attachments.md) les pièces jointes de ces messages ne sont pas détonation.</span><span class="sxs-lookup"><span data-stu-id="812c7-123">[Safe Attachments in Defender for Office 365](safe-attachments.md) doesn't detonate attachments in these messages.</span></span>

<span data-ttu-id="812c7-124"><sup>\*</sup> Vous ne pouvez pas contourner le filtrage des programmes malveillants ou zap pour les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="812c7-124"><sup>\*</sup> You can't bypass malware filtering or ZAP for malware.</span></span>

<span data-ttu-id="812c7-125">Les messages identifiés par la stratégie de remise avancée ne sont pas des menaces de sécurité. Les messages sont donc marqués comme étant des remplacements système.</span><span class="sxs-lookup"><span data-stu-id="812c7-125">Messages that are identified by the advanced delivery policy aren't security threats, so the messages are marked as system overrides.</span></span> <span data-ttu-id="812c7-126">Les administrateurs peuvent filtrer et analyser ces substitutions système dans les expériences suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-126">Admins can filter and analyze these system overrides in the following experiences:</span></span>

- [<span data-ttu-id="812c7-127">Détections de l’Explorateur de menaces/En temps réel dans Defender Office 365 plan 2</span><span class="sxs-lookup"><span data-stu-id="812c7-127">Threat Explorer/Real-time detections in Defender for Office 365 plan 2</span></span>](threat-explorer.md)
- <span data-ttu-id="812c7-128">Page [Entité de messagerie dans l’Explorateur de menaces/Détections en temps réel](mdo-email-entity-page.md)</span><span class="sxs-lookup"><span data-stu-id="812c7-128">The [Email entity Page in Threat Explorer/Real-time detections](mdo-email-entity-page.md)</span></span>
- <span data-ttu-id="812c7-129">Rapport [d’état de la protection contre les menaces](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="812c7-129">The [Threat protection status report](view-email-security-reports.md#threat-protection-status-report)</span></span>
- [<span data-ttu-id="812c7-130">Recherche avancée dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="812c7-130">Advanced hunting in Microsoft Defender for Endpoint</span></span>](../defender-endpoint/advanced-hunting-overview.md)
- [<span data-ttu-id="812c7-131">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="812c7-131">Campaign Views</span></span>](campaigns.md)

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="812c7-132">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="812c7-132">What do you need to know before you begin?</span></span>

- <span data-ttu-id="812c7-133">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="812c7-133">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="812c7-134">Pour aller directement à la page **de remise avancée,** ouvrez <https://security.microsoft.com/advanceddelivery> .</span><span class="sxs-lookup"><span data-stu-id="812c7-134">To go directly to the **Advanced delivery** page, open <https://security.microsoft.com/advanceddelivery>.</span></span>

- <span data-ttu-id="812c7-135">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="812c7-135">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="812c7-136">Des autorisations doivent vous être attribuées avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="812c7-136">You need to be assigned permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="812c7-137">Pour créer, modifier ou supprimer des paramètres configurés dans la stratégie  de remise avancée, vous devez être membre du  groupe de rôles Administrateur de la sécurité dans le portail **Microsoft 365 Defender** et membre du groupe de rôles Gestion de l’organisation **dans Exchange Online**.</span><span class="sxs-lookup"><span data-stu-id="812c7-137">To create, modify, or remove configured settings in the advanced delivery policy, you need to be a member of the **Security Administrator** role group in the **Microsoft 365 Defender portal** and a member of the **Organization Management** role group in **Exchange Online**.</span></span>
  - <span data-ttu-id="812c7-138">Pour un accès en lecture seule à la stratégie de  remise  avancée, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="812c7-138">For read-only access to the advanced delivery policy, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="812c7-139">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender et](permissions-microsoft-365-security-center.md) [autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="812c7-139">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md) and [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  > <span data-ttu-id="812c7-140">L’ajout d’utilisateurs au rôle Azure Active Directory leur donne les autorisations  requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="812c7-140">Adding users to the corresponding Azure Active Directory role gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="812c7-141">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="812c7-141">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-configure-secops-mailboxes-in-the-advanced-delivery-policy"></a><span data-ttu-id="812c7-142">Utiliser le portail Microsoft 365 Defender pour configurer les boîtes aux lettres SecOps dans la stratégie de remise avancée</span><span class="sxs-lookup"><span data-stu-id="812c7-142">Use the Microsoft 365 Defender portal to configure SecOps mailboxes in the advanced delivery policy</span></span>

1. <span data-ttu-id="812c7-143">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Rules** section \> **Advanced delivery**.</span><span class="sxs-lookup"><span data-stu-id="812c7-143">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Rules** section \> **Advanced delivery**.</span></span>

2. <span data-ttu-id="812c7-144">Dans la page **Remise** avancée, vérifiez que l’onglet Boîte aux lettres **SecOps** est sélectionné, puis faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-144">On the **Advanced delivery** page, verify that the **SecOps mailbox** tab is selected, and then do one of the following steps:</span></span>
   - <span data-ttu-id="812c7-145">Cliquez sur ![ Modifier ](../../media/m365-cc-sc-edit-icon.png) **l’icône Modifier.**</span><span class="sxs-lookup"><span data-stu-id="812c7-145">Click ![Edit icon](../../media/m365-cc-sc-edit-icon.png) **Edit**.</span></span>
   - <span data-ttu-id="812c7-146">S’il n’existe aucune simulation de hameçonnage configurée, cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="812c7-146">If there are no configured phishing simulations, click **Add**.</span></span>

3. <span data-ttu-id="812c7-147">Dans le volant modifier les boîtes aux lettres **SecOps** qui s’ouvre, entrez une boîte aux lettres Exchange Online existante que vous souhaitez désigner comme boîte aux lettres SecOps en suivant l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-147">On the **Edit SecOps mailboxes** flyout that opens, enter an existing Exchange Online mailbox that you want to designate as SecOps mailbox by doing one of the following steps:</span></span>
   - <span data-ttu-id="812c7-148">Cliquez dans la zone, laissez la liste des boîtes aux lettres résoudre, puis sélectionnez la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="812c7-148">Click in the box, let the list of mailboxes resolve, and then select the mailbox.</span></span>
   - <span data-ttu-id="812c7-149">Cliquez dans la zone commencer à taper un identificateur pour la boîte aux lettres (nom, nom complet, alias, adresse e-mail, nom de compte, etc.), puis sélectionnez la boîte aux lettres (nom complet) dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="812c7-149">Click in the box start typing an identifier for the mailbox (name, display name, alias, email address, account name, etc.), and select the mailbox (display name) from the results.</span></span>

     <span data-ttu-id="812c7-150">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="812c7-150">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="812c7-151">Les groupes de distribution ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="812c7-151">Distribution groups are not allowed.</span></span>

     <span data-ttu-id="812c7-152">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="812c7-152">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="812c7-154">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="812c7-154">next to the value.</span></span>

4. <span data-ttu-id="812c7-155">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="812c7-155">When you're finished, click **Save**.</span></span>

<span data-ttu-id="812c7-156">Les entrées de boîte aux lettres SecOps que vous avez configurées sont affichées sous l’onglet Boîte aux lettres **SecOps.** Pour apporter des modifications, cliquez ![ sur Modifier ](../../media/m365-cc-sc-edit-icon.png) **l’icône Modifier** sous l’onglet.</span><span class="sxs-lookup"><span data-stu-id="812c7-156">The SecOps mailbox entries that you configured are displayed on the **SecOps mailbox** tab. To make changes, click ![Edit icon](../../media/m365-cc-sc-edit-icon.png) **Edit** on the tab.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-configure-third-party-phishing-simulations-in-the-advanced-delivery-policy"></a><span data-ttu-id="812c7-157">Utiliser le portail Microsoft 365 Defender pour configurer des simulations de hameçonnage tiers dans la stratégie de remise avancée</span><span class="sxs-lookup"><span data-stu-id="812c7-157">Use the Microsoft 365 Defender portal to configure third-party phishing simulations in the advanced delivery policy</span></span>

1. <span data-ttu-id="812c7-158">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Rules** section \> **Advanced delivery**.</span><span class="sxs-lookup"><span data-stu-id="812c7-158">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Rules** section \> **Advanced delivery**.</span></span>

2. <span data-ttu-id="812c7-159">Dans la page **Remise avancée,** sélectionnez l’onglet **Simulation** de hameçonnage, puis faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-159">On the **Advanced delivery** page, select the **Phishing simulation** tab, and then do one of the following steps:</span></span>
   - <span data-ttu-id="812c7-160">Cliquez sur ![ Modifier ](../../media/m365-cc-sc-edit-icon.png) **l’icône Modifier.**</span><span class="sxs-lookup"><span data-stu-id="812c7-160">Click ![Edit icon](../../media/m365-cc-sc-edit-icon.png) **Edit**.</span></span>
   - <span data-ttu-id="812c7-161">S’il n’existe aucune simulation de hameçonnage configurée, cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="812c7-161">If there are no configured phishing simulations, click **Add**.</span></span>

3. <span data-ttu-id="812c7-162">Dans le **flyout de simulation** de hameçonnage tiers qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="812c7-162">On the **Edit third-party phishing simulation** flyout that opens, configure the following settings:</span></span>

   - <span data-ttu-id="812c7-163">**Domaine** d’envoi : développez ce paramètre et entrez au moins un domaine d’adresse de messagerie (par exemple, contoso.com) en cliquant dans la zone, en entrant une valeur, puis en appuyant sur Entrée ou en sélectionnant la valeur affichée sous la zone.</span><span class="sxs-lookup"><span data-stu-id="812c7-163">**Sending domain**: Expand this setting and enter at least one email address domain (for example, contoso.com) by clicking in the box, entering a value, and then pressing Enter or selecting the value that's displayed below the box.</span></span> <span data-ttu-id="812c7-164">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="812c7-164">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="812c7-165">Vous pouvez ajouter jusqu’à 10 entrées.</span><span class="sxs-lookup"><span data-stu-id="812c7-165">You can add up to 10 entries.</span></span>
   - <span data-ttu-id="812c7-166">**Adresse IP** d’envoi : développez ce paramètre et entrez au moins une adresse IPv4 valide en cliquant dans la zone, en entrant une valeur, puis en appuyant sur Entrée ou en sélectionnant la valeur affichée sous la zone.</span><span class="sxs-lookup"><span data-stu-id="812c7-166">**Sending IP**: Expand this setting and enter at least one valid IPv4 address is required by clicking in the box, entering a value, and then pressing Enter or selecting the value that's displayed below the box.</span></span> <span data-ttu-id="812c7-167">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="812c7-167">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="812c7-168">Vous pouvez ajouter jusqu’à 10 entrées.</span><span class="sxs-lookup"><span data-stu-id="812c7-168">You can add up to 10 entries.</span></span> <span data-ttu-id="812c7-169">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-169">Valid values are:</span></span>
     - <span data-ttu-id="812c7-170">Adresse IP unique : par exemple, 192.168.1.1.</span><span class="sxs-lookup"><span data-stu-id="812c7-170">Single IP: For example, 192.168.1.1.</span></span>
     - <span data-ttu-id="812c7-171">Plage d’adresses IP : par exemple, 192.168.0.1-192.168.0.254.</span><span class="sxs-lookup"><span data-stu-id="812c7-171">IP range: For example, 192.168.0.1-192.168.0.254.</span></span>
     - <span data-ttu-id="812c7-172">ADRESSE IP CIDR : par exemple, 192.168.0.1/25.</span><span class="sxs-lookup"><span data-stu-id="812c7-172">CIDR IP: For example, 192.168.0.1/25.</span></span>
   - <span data-ttu-id="812c7-173">URL de simulation pour autoriser : développez ce paramètre et entrez éventuellement des URL spécifiques qui font partie de votre campagne de simulation de hameçonnage qui ne doivent pas être bloquées ou désaxées en cliquant dans la zone, en entrant une valeur, puis en appuyant sur Entrée ou en sélectionnant la valeur affichée sous la zone.</span><span class="sxs-lookup"><span data-stu-id="812c7-173">**Simulation URLs to allow**: Expand this setting and optionally enter specific URLs that are part of your phishing simulation campaign that should not be blocked or detonated by clicking in the box, entering a value, and then pressing Enter or selecting the value that's displayed below the box.</span></span> <span data-ttu-id="812c7-174">Vous pouvez ajouter jusqu’à 10 entrées.</span><span class="sxs-lookup"><span data-stu-id="812c7-174">You can add up to 10 entries.</span></span>

   <span data-ttu-id="812c7-175">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="812c7-175">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="812c7-177">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="812c7-177">next to the value.</span></span>

4. <span data-ttu-id="812c7-178">Lorsque vous avez terminé, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-178">When you're finished, do one of the following steps:</span></span>
   - <span data-ttu-id="812c7-179">**Première fois**: cliquez **sur Ajouter,** puis sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="812c7-179">**First time**: Click **Add**, and then click **Close**.</span></span>
   - <span data-ttu-id="812c7-180">**Modifier une version existante**: cliquez sur **Enregistrer,** puis sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="812c7-180">**Edit existing**: Click **Save** and then click **Close**.</span></span>

<span data-ttu-id="812c7-181">Les entrées de simulation de hameçonnage tierces que vous avez configurées sont affichées sous l’onglet **Simulation de hameçonnage.** Pour apporter des modifications, cliquez ![ sur Modifier ](../../media/m365-cc-sc-edit-icon.png) **l’icône Modifier** sous l’onglet.</span><span class="sxs-lookup"><span data-stu-id="812c7-181">The third-party phishing simulation entries that you configured are displayed on the **Phishing simulation** tab. To make changes, click ![Edit icon](../../media/m365-cc-sc-edit-icon.png) **Edit** on the tab.</span></span>

## <a name="additional-scenarios-that-require-filtering-bypass"></a><span data-ttu-id="812c7-182">Scénarios supplémentaires nécessitant le contournement du filtrage</span><span class="sxs-lookup"><span data-stu-id="812c7-182">Additional scenarios that require filtering bypass</span></span>

<span data-ttu-id="812c7-183">Outre les deux scénarios que la stratégie de remise avancée peut vous aider, il existe d’autres scénarios qui peuvent nécessiter que vous contourniez le filtrage :</span><span class="sxs-lookup"><span data-stu-id="812c7-183">In addition to the two scenarios that the advanced delivery policy can help you with, there are other scenarios that might require you bypass filtering:</span></span>

- <span data-ttu-id="812c7-184">**Filtres tiers**: si l’enregistrement MX de votre domaine ne pointe pas vers Office 365 (les messages sont d’abord acheminés [ailleurs),](secure-by-default.md) la sécurité par défaut *n’est* *pas disponible.*</span><span class="sxs-lookup"><span data-stu-id="812c7-184">**Third-party filters**: If your domain's MX record *doesn't* point to Office 365 (messages are routed somewhere else first), [secure by default](secure-by-default.md) *is not available*.</span></span> <span data-ttu-id="812c7-185">Si vous souhaitez ajouter une protection, vous devez activer le filtrage amélioré pour les connecteurs (également appelé ignorer la *liste).*</span><span class="sxs-lookup"><span data-stu-id="812c7-185">If you'd like to add protection, you'll need to enable Enhanced Filtering for Connectors (also known as *skip listing*).</span></span> <span data-ttu-id="812c7-186">Pour plus d’informations, voir [Gérer le flux de messagerie](/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud)à l’aide d’un service cloud tiers Exchange Online .</span><span class="sxs-lookup"><span data-stu-id="812c7-186">For more information, see [Manage mail flow using a third-party cloud service with Exchange Online](/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud).</span></span> <span data-ttu-id="812c7-187">Si vous ne souhaitez pas que le filtrage amélioré pour les connecteurs soit utilisé, utilisez des règles de flux de messagerie (également appelées règles de transport) pour contourner le filtrage Microsoft pour les messages qui ont déjà été évalués par un filtrage tiers.</span><span class="sxs-lookup"><span data-stu-id="812c7-187">If you don't want Enhanced Filtering for Connectors,use mail flow rules (also known as transport rules) to bypass Microsoft filtering for messages that have already been evaluated by third-party filtering.</span></span> <span data-ttu-id="812c7-188">Pour plus d’informations, voir [Utiliser des règles de flux de messagerie pour définir le SCL dans les messages.](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-set-scl.md)</span><span class="sxs-lookup"><span data-stu-id="812c7-188">For more information, see [Use mail flow rules to set the SCL in messages](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-set-scl.md).</span></span>

- <span data-ttu-id="812c7-189">**Faux positifs** en cours d’examen : vous souhaitez peut-être autoriser temporairement certains messages en cours d’analyse par Microsoft via des [envois](admin-submission.md) d’administrateur à signaler les messages de bonne qualité connus qui sont marqués à tort comme incorrects pour Microsoft (faux positifs).</span><span class="sxs-lookup"><span data-stu-id="812c7-189">**False positives under review**: You might want to temporarily allow certain messages that are still being analyzed by Microsoft via [admin submissions](admin-submission.md) to report known good messages that are incorrectly being marked as bad to Microsoft (false positives).</span></span> <span data-ttu-id="812c7-190">Comme pour toutes les substitutions, il est **_vivement_** recommandé que ces allocations soient temporaires.</span><span class="sxs-lookup"><span data-stu-id="812c7-190">As with all overrides, we **_highly recommended_** that these allowances are temporary.</span></span>

## <a name="exchange-online-powershell-procedures-for-secops-mailboxes-in-the-advanced-delivery-policy"></a><span data-ttu-id="812c7-191">Exchange Online Procédures PowerShell pour les boîtes aux lettres SecOps dans la stratégie de remise avancée</span><span class="sxs-lookup"><span data-stu-id="812c7-191">Exchange Online PowerShell procedures for SecOps mailboxes in the advanced delivery policy</span></span>

<span data-ttu-id="812c7-192">Dans Exchange Online PowerShell, les éléments de base des boîtes aux lettres SecOps dans la stratégie de remise avancée sont :</span><span class="sxs-lookup"><span data-stu-id="812c7-192">In Exchange Online PowerShell, the basic elements of SecOps mailboxes in the advanced delivery policy are:</span></span>

- <span data-ttu-id="812c7-193">Stratégie de remplacement **SecOps**: contrôlée par les cmdlets **\* -SecOpsOverridePolicy.**</span><span class="sxs-lookup"><span data-stu-id="812c7-193">**The SecOps override policy**: Controlled by the **\*-SecOpsOverridePolicy** cmdlets.</span></span>
- <span data-ttu-id="812c7-194">**Règle de remplacement SecOps**: contrôlée par les cmdlets **\* -SecOpsOverrideRule.**</span><span class="sxs-lookup"><span data-stu-id="812c7-194">**The SecOps override rule**: Controlled by the **\*-SecOpsOverrideRule** cmdlets.</span></span>

<span data-ttu-id="812c7-195">Ce comportement a les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="812c7-195">This behavior has the following results:</span></span>

- <span data-ttu-id="812c7-196">Vous créez d’abord la stratégie, puis la règle qui identifie la stratégie à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="812c7-196">You create the policy first, then you create the rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="812c7-197">Lorsque vous supprimez une stratégie de PowerShell, la règle correspondante est également supprimée.</span><span class="sxs-lookup"><span data-stu-id="812c7-197">When you remove a policy from PowerShell, the corresponding rule is also removed.</span></span>
- <span data-ttu-id="812c7-198">Lorsque vous supprimez une règle de PowerShell, la stratégie correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="812c7-198">When you remove a rule from PowerShell, the corresponding policy is not removed.</span></span> <span data-ttu-id="812c7-199">Vous devez supprimer manuellement la stratégie correspondante.</span><span class="sxs-lookup"><span data-stu-id="812c7-199">You need to remove the corresponding policy manually.</span></span>

### <a name="use-powershell-to-configure-secops-mailboxes"></a><span data-ttu-id="812c7-200">Utiliser PowerShell pour configurer des boîtes aux lettres SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-200">Use PowerShell to configure SecOps mailboxes</span></span>

<span data-ttu-id="812c7-201">La configuration d’une boîte aux lettres SecOps dans la stratégie de remise avancée dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="812c7-201">Configuring a SecOps mailbox in the advanced delivery policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="812c7-202">Créez la stratégie de remplacement SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-202">Create the SecOps override policy.</span></span>
2. <span data-ttu-id="812c7-203">Créez la règle de remplacement SecOps qui spécifie la stratégie à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="812c7-203">Create the SecOps override rule that specifies the policy that the rule applies to.</span></span>

#### <a name="step-1-use-powershell-to-create-the-secops-override-policy"></a><span data-ttu-id="812c7-204">Étape 1 : Utiliser PowerShell pour créer la stratégie de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-204">Step 1: Use PowerShell to create the SecOps override policy</span></span>

<span data-ttu-id="812c7-205">Pour créer la stratégie de remplacement SecOps, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-205">To create the SecOps override policy, use the following syntax:</span></span>

```powershell
New-SecOpsOverridePolicy -Name SecOpsOverridePolicy -SentTo <EmailAddress1>,<EmailAddress2>,...<EmailAddressN>
```

<span data-ttu-id="812c7-206">**Remarque**: quelle que soit la valeur de nom que vous spécifiez, le nom de la stratégie sera SecOpsOverridePolicy. Vous pouvez donc également utiliser cette valeur.</span><span class="sxs-lookup"><span data-stu-id="812c7-206">**Note**: Regardless of the Name value you specify, the policy name will be SecOpsOverridePolicy, so you might as well use that value.</span></span>

<span data-ttu-id="812c7-207">Cet exemple crée la stratégie de boîte aux lettres SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-207">This example creates the SecOps mailbox policy.</span></span>

```powershell
New-SecOpsOverridePolicy -Name SecOpsOverridePolicy -SentTo secops@contoso.com
```

<span data-ttu-id="812c7-208">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SecOpsOverridePolicy](/powershell/module/exchange/new-secopsoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-208">For detailed syntax and parameter information, see [New-SecOpsOverridePolicy](/powershell/module/exchange/new-secopsoverridepolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-the-secops-override-rule"></a><span data-ttu-id="812c7-209">Étape 2 : Utiliser PowerShell pour créer la règle de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-209">Step 2: Use PowerShell to create the SecOps override rule</span></span>

<span data-ttu-id="812c7-210">Cet exemple crée la règle de boîte aux lettres SecOps avec les paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="812c7-210">This example creates the SecOps mailbox rule with the specified settings.</span></span>

```powershell
New-SecOpsOverrideRule -Name SecOpsOverrideRule -Policy SecOpsOverridePolicy
```

<span data-ttu-id="812c7-211">**Remarque**: \*\*Quelle que soit la valeur de nom que vous spécifiez, le nom de la règle sera SecOpsOverrideRule, où est une valeur \<GUID\> GUID unique \<GUID\> (par exemple, 6fed4b63-3563-495d-a481-b24a311f8329).</span><span class="sxs-lookup"><span data-stu-id="812c7-211">**Note**: \*\*Regardless of the Name value you specify, the rule name will be SecOpsOverrideRule\<GUID\> where \<GUID\> is a unique GUID value (for example, 6fed4b63-3563-495d-a481-b24a311f8329).</span></span>

<span data-ttu-id="812c7-212">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SecOpsOverrideRule](/powershell/module/exchange/new-secopsoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-212">For detailed syntax and parameter information, see [New-SecOpsOverrideRule](/powershell/module/exchange/new-secopsoverriderule).</span></span>

### <a name="use-powershell-to-view-the-secops-override-policy"></a><span data-ttu-id="812c7-213">Utiliser PowerShell pour afficher la stratégie de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-213">Use PowerShell to view the SecOps override policy</span></span>

<span data-ttu-id="812c7-214">Cet exemple renvoie des informations détaillées sur la seule stratégie de boîte aux lettres SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-214">This example returns detailed information about the one and only SecOps mailbox policy.</span></span>

```powershell
Get-SecOpsOverridePolicy
```

<span data-ttu-id="812c7-215">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SecOpsOverridePolicy](/powershell/module/exchange/get-secopsoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-215">For detailed syntax and parameter information, see [Get-SecOpsOverridePolicy](/powershell/module/exchange/get-secopsoverridepolicy).</span></span>

### <a name="use-powershell-to-view-secops-override-rules"></a><span data-ttu-id="812c7-216">Utiliser PowerShell pour afficher les règles de remplacement secOps</span><span class="sxs-lookup"><span data-stu-id="812c7-216">Use PowerShell to view SecOps override rules</span></span>

<span data-ttu-id="812c7-217">Cet exemple renvoie des informations détaillées sur les règles de remplacement SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-217">This example returns detailed information about SecOps override rules.</span></span>

```powershell
Get-SecOpsOverrideRule
```

<span data-ttu-id="812c7-218">Bien que la commande précédente ne retourne qu’une seule règle, toutes les règles en attente de suppression peuvent également être incluses dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="812c7-218">Although the previous command should return only one rule, any rules that are pending deletion might also be included in the results.</span></span>

<span data-ttu-id="812c7-219">Cet exemple identifie la règle valide (une) et toutes les règles non valides.</span><span class="sxs-lookup"><span data-stu-id="812c7-219">This example identifies the valid rule (one) and any invalid rules.</span></span>

```powershell
Get-SecOpsOverrideRule | Format-Table Name,Mode
```

<span data-ttu-id="812c7-220">Après avoir identifié les règles non valides, vous pouvez les supprimer à l’aide de l’cmdlet **Remove-SecOpsOverrideRule,** comme décrit plus loin [dans cet article.](#use-powershell-to-remove-secops-override-rules)</span><span class="sxs-lookup"><span data-stu-id="812c7-220">After you identify the invalid rules, you can remove them by using the **Remove-SecOpsOverrideRule** cmdlet as described [later in this article](#use-powershell-to-remove-secops-override-rules).</span></span>

<span data-ttu-id="812c7-221">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SecOpsOverrideRule](/powershell/module/exchange/get-secopsoverriderule)</span><span class="sxs-lookup"><span data-stu-id="812c7-221">For detailed syntax and parameter information, see [Get-SecOpsOverrideRule](/powershell/module/exchange/get-secopsoverriderule)</span></span>

### <a name="use-powershell-to-modify-the-secops-override-policy"></a><span data-ttu-id="812c7-222">Utiliser PowerShell pour modifier la stratégie de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-222">Use PowerShell to modify the SecOps override policy</span></span>

<span data-ttu-id="812c7-223">Pour modifier la stratégie de remplacement SecOps, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-223">To modify the SecOps override policy, use the following syntax:</span></span>

```powershell
Set-SecOpsOverridePolicy -Identity SecOpsOverridePolicy [-AddSentTo <EmailAddress1>,<EmailAddress2>,...<EmailAddressN>] [-RemoveSentTo <EmailAddress1>,<EmailAddress2>,...<EmailAddressN>]
```

<span data-ttu-id="812c7-224">Cet exemple ajoute secops2@contoso.com la stratégie de remplacement SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-224">This example adds secops2@contoso.com to the SecOps override policy.</span></span>

```powershell
Set-SecOpsOverridePolicy -Identity SecOpsOverridePolicy -AddSentTo secops2@contoso.com
```

<span data-ttu-id="812c7-225">**Remarque**: s’il existe une règle de remplacement SecOps associée valide, les adresses de messagerie de la règle sont également mises à jour.</span><span class="sxs-lookup"><span data-stu-id="812c7-225">**Note**: If an associated, valid SecOps override rule exists, the email addresses in the rule will also be updated.</span></span>

<span data-ttu-id="812c7-226">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SecOpsOverridePolicy](/powershell/module/exchange/set-secopsoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-226">For detailed syntax and parameter information, see [Set-SecOpsOverridePolicy](/powershell/module/exchange/set-secopsoverridepolicy).</span></span>

### <a name="use-powershell-to-modify-a-secops-override-rule"></a><span data-ttu-id="812c7-227">Utiliser PowerShell pour modifier une règle de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-227">Use PowerShell to modify a SecOps override rule</span></span>

<span data-ttu-id="812c7-228">La cmdlet **Set-SecOpsOverrideRule** ne modifie pas les adresses de messagerie dans la règle de remplacement SecOps.</span><span class="sxs-lookup"><span data-stu-id="812c7-228">The **Set-SecOpsOverrideRule** cmdlet does not modify the email addresses in the SecOps override rule.</span></span> <span data-ttu-id="812c7-229">Pour modifier les adresses de messagerie dans la règle de remplacement SecOps, utilisez l’cmdlet **Set-SecOpsOverridePolicy.**</span><span class="sxs-lookup"><span data-stu-id="812c7-229">To modify the email addresses in the SecOps override rule, use the **Set-SecOpsOverridePolicy** cmdlet.</span></span>

<span data-ttu-id="812c7-230">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SecOpsOverrideRule](/powershell/module/exchange/set-secopsoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-230">For detailed syntax and parameter information, see [Set-SecOpsOverrideRule](/powershell/module/exchange/set-secopsoverriderule).</span></span>

### <a name="use-powershell-to-remove-the-secops-override-policy"></a><span data-ttu-id="812c7-231">Utiliser PowerShell pour supprimer la stratégie de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-231">Use PowerShell to remove the SecOps override policy</span></span>

<span data-ttu-id="812c7-232">Cet exemple supprime la stratégie de boîte aux lettres SecOps et la règle correspondante.</span><span class="sxs-lookup"><span data-stu-id="812c7-232">This example removes the SecOps Mailbox policy and the corresponding rule.</span></span>

```powershell
Remove-SecOpsOverridePolicy -Identity SecOpsOverridePolicy
```

<span data-ttu-id="812c7-233">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SecOpsOverridePolicy](/powershell/module/exchange/remove-secopsoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-233">For detailed syntax and parameter information, see [Remove-SecOpsOverridePolicy](/powershell/module/exchange/remove-secopsoverridepolicy).</span></span>

### <a name="use-powershell-to-remove-secops-override-rules"></a><span data-ttu-id="812c7-234">Utiliser PowerShell pour supprimer des règles de remplacement SecOps</span><span class="sxs-lookup"><span data-stu-id="812c7-234">Use PowerShell to remove SecOps override rules</span></span>

<span data-ttu-id="812c7-235">Pour supprimer une règle de remplacement SecOps, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-235">To remove a SecOps override rule, use the following syntax:</span></span>

```powershell
Remove-SecOpsOverrideRule -Identity <RuleIdentity>
```

<span data-ttu-id="812c7-236">Cet exemple supprime la règle de remplacement SecOps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="812c7-236">This example removes the specified SecOps override rule.</span></span>

```powershell
Remove-SecOpsOverrideRule -Identity SecOpsOverrideRule6fed4b63-3563-495d-a481-b24a311f8329
```

<span data-ttu-id="812c7-237">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SecOpsOverrideRule](/powershell/module/exchange/remove-secopsoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-237">For detailed syntax and parameter information, see [Remove-SecOpsOverrideRule](/powershell/module/exchange/remove-secopsoverriderule).</span></span>

## <a name="exchange-online-powershell-procedures-for-third-party-phishing-simulations-in-the-advanced-delivery-policy"></a><span data-ttu-id="812c7-238">Exchange Online Procédures PowerShell pour les simulations de hameçonnage tiers dans la stratégie de remise avancée</span><span class="sxs-lookup"><span data-stu-id="812c7-238">Exchange Online PowerShell procedures for third-party phishing simulations in the advanced delivery policy</span></span>

<span data-ttu-id="812c7-239">Dans Exchange Online PowerShell, les éléments de base des simulations de hameçonnage tiers dans la stratégie de remise avancée sont les éléments ci-après :</span><span class="sxs-lookup"><span data-stu-id="812c7-239">In Exchange Online PowerShell, the basic elements of third-party phishing simulations in the advanced delivery policy are:</span></span>

- <span data-ttu-id="812c7-240">**Stratégie de remplacement de simulation de** hameçonnage : contrôlée par les cmdlets **\* -PhishSimOverridePolicy.**</span><span class="sxs-lookup"><span data-stu-id="812c7-240">**The phishing simulation override policy**: Controlled by the **\*-PhishSimOverridePolicy** cmdlets.</span></span>
- <span data-ttu-id="812c7-241">**Règle de remplacement de simulation d’hameçonnage**: contrôlée par les cmdlets **\* -PhishSimOverrideRule.**</span><span class="sxs-lookup"><span data-stu-id="812c7-241">**The phishing simulation override rule**: Controlled by the **\*-PhishSimOverrideRule** cmdlets.</span></span>

<span data-ttu-id="812c7-242">Ce comportement a les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="812c7-242">This behavior has the following results:</span></span>

- <span data-ttu-id="812c7-243">Vous créez d’abord la stratégie, puis la règle qui identifie la stratégie à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="812c7-243">You create the policy first, then you create the rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="812c7-244">Vous modifiez séparément les paramètres de la stratégie et de la règle.</span><span class="sxs-lookup"><span data-stu-id="812c7-244">You modify the settings in the policy and the rule separately.</span></span>
- <span data-ttu-id="812c7-245">Lorsque vous supprimez une stratégie de PowerShell, la règle correspondante est également supprimée.</span><span class="sxs-lookup"><span data-stu-id="812c7-245">When you remove a policy from PowerShell, the corresponding rule is also removed.</span></span>
- <span data-ttu-id="812c7-246">Lorsque vous supprimez une règle de PowerShell, la stratégie correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="812c7-246">When you remove a rule from PowerShell, the corresponding policy is not removed.</span></span> <span data-ttu-id="812c7-247">Vous devez supprimer manuellement la stratégie correspondante.</span><span class="sxs-lookup"><span data-stu-id="812c7-247">You need to remove the corresponding policy manually.</span></span>

### <a name="use-powershell-to-configure-third-party-phishing-simulations"></a><span data-ttu-id="812c7-248">Utiliser PowerShell pour configurer des simulations de hameçonnage tierces</span><span class="sxs-lookup"><span data-stu-id="812c7-248">Use PowerShell to configure third-party phishing simulations</span></span>

<span data-ttu-id="812c7-249">La configuration d’une simulation de hameçonnage tierce dans la stratégie de remise avancée dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="812c7-249">Configuring a third-party phishing simulation in the advanced delivery policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="812c7-250">Créez la stratégie de remplacement de simulation d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="812c7-250">Create the phishing simulation override policy.</span></span>
2. <span data-ttu-id="812c7-251">Créez la règle de remplacement de simulation de hameçonnage qui spécifie la stratégie à appliquer à la règle.</span><span class="sxs-lookup"><span data-stu-id="812c7-251">Create the phishing simulation override rule that specifies the policy that the rule applies to.</span></span>

#### <a name="step-1-use-powershell-to-create-the-phishing-simulation-override-policy"></a><span data-ttu-id="812c7-252">Étape 1 : Utiliser PowerShell pour créer la stratégie de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-252">Step 1: Use PowerShell to create the phishing simulation override policy</span></span>

<span data-ttu-id="812c7-253">Cet exemple crée la stratégie de remplacement de simulation de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="812c7-253">This example creates the phishing simulation override policy.</span></span>

```powershell
New-PhishSimOverridePolicy -Name PhishSimOverridePolicy
```

<span data-ttu-id="812c7-254">**Remarque**: quelle que soit la valeur de nom que vous spécifiez, le nom de la stratégie sera PhishSimOverridePolicy. Vous pouvez donc également utiliser cette valeur.</span><span class="sxs-lookup"><span data-stu-id="812c7-254">**Note**: Regardless of the Name value you specify, the policy name will be PhishSimOverridePolicy, so you might as well use that value.</span></span>

<span data-ttu-id="812c7-255">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-PhishSimOverridePolicy](/powershell/module/exchange/new-phishsimoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-255">For detailed syntax and parameter information, see [New-PhishSimOverridePolicy](/powershell/module/exchange/new-phishsimoverridepolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-the-phishing-simulation-override-rule"></a><span data-ttu-id="812c7-256">Étape 2 : Utiliser PowerShell pour créer la règle de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-256">Step 2: Use PowerShell to create the phishing simulation override rule</span></span>

<span data-ttu-id="812c7-257">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-257">Use the following syntax:</span></span>

```powershell
New-PhishSimOverrideRule -Name PhishSimOverrideRule -Policy PhishSimOverridePolicy -SenderDomainIs <Domain1>,<Domain2>,...<DomainN> -SenderIpRanges <IPAddressEntry1>,<IPAddressEntry2>,...<IPAddressEntryN>
```

<span data-ttu-id="812c7-258">Quelle que soit la valeur name que vous spécifiez, le nom de la règle sera PhishSimOverrideRule, où est une valeur \<GUID\> \<GUID\> GUID unique (par exemple, a0eae53e-d755-4a42-9320-b9c6b55c5011).</span><span class="sxs-lookup"><span data-stu-id="812c7-258">Regardless of the Name value you specify, the rule name will be PhishSimOverrideRule\<GUID\> where \<GUID\> is a unique GUID value (for example, a0eae53e-d755-4a42-9320-b9c6b55c5011).</span></span>

<span data-ttu-id="812c7-259">Une entrée d’adresse IP valide est l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="812c7-259">A valid IP address entry is one of the following values:</span></span>

- <span data-ttu-id="812c7-260">Adresse IP unique : par exemple, 192.168.1.1.</span><span class="sxs-lookup"><span data-stu-id="812c7-260">Single IP: For example, 192.168.1.1.</span></span>
- <span data-ttu-id="812c7-261">Plage d’adresses IP : par exemple, 192.168.0.1-192.168.0.254.</span><span class="sxs-lookup"><span data-stu-id="812c7-261">IP range: For example, 192.168.0.1-192.168.0.254.</span></span>
- <span data-ttu-id="812c7-262">ADRESSE IP CIDR : par exemple, 192.168.0.1/25.</span><span class="sxs-lookup"><span data-stu-id="812c7-262">CIDR IP: For example, 192.168.0.1/25.</span></span>

<span data-ttu-id="812c7-263">Cet exemple crée la règle de remplacement de simulation de hameçonnage avec les paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="812c7-263">This example creates the phishing simulation override rule with the specified settings.</span></span>

```powershell
New-PhishSimOverrideRule -Name PhishSimOverrideRule -Policy PhishSimOverridePolicy -SenderDomainIs fabrikam.com,wingtiptoys.com -SenderIpRanges 192.168.1.55
```

<span data-ttu-id="812c7-264">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-PhishSimOverrideRule](/powershell/module/exchange/new-phishsimoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-264">For detailed syntax and parameter information, see [New-PhishSimOverrideRule](/powershell/module/exchange/new-phishsimoverriderule).</span></span>

### <a name="use-powershell-to-view-the-phishing-simulation-override-policy"></a><span data-ttu-id="812c7-265">Utiliser PowerShell pour afficher la stratégie de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-265">Use PowerShell to view the phishing simulation override policy</span></span>

<span data-ttu-id="812c7-266">Cet exemple renvoie des informations détaillées sur la seule stratégie de remplacement de simulation de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="812c7-266">This example returns detailed information about the one and only phishing simulation override policy.</span></span>

```powershell
Get-PhishSimOverridePolicy
```

<span data-ttu-id="812c7-267">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-PhishSimOverridePolicy](/powershell/module/exchange/get-phishsimoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-267">For detailed syntax and parameter information, see [Get-PhishSimOverridePolicy](/powershell/module/exchange/get-phishsimoverridepolicy).</span></span>

### <a name="use-powershell-to-view-phishing-simulation-override-rules"></a><span data-ttu-id="812c7-268">Utiliser PowerShell pour afficher les règles de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-268">Use PowerShell to view phishing simulation override rules</span></span>

<span data-ttu-id="812c7-269">Cet exemple renvoie des informations détaillées sur les règles de remplacement de simulation de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="812c7-269">This example returns detailed information about phishing simulation override rules.</span></span>

```powershell
Get-PhishSimOverrideRule
```

<span data-ttu-id="812c7-270">Bien que la commande précédente ne retourne qu’une seule règle, toutes les règles en attente de suppression peuvent également être incluses dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="812c7-270">Although the previous command should return only one rule, any rules that are pending deletion might also be included in the results.</span></span>

<span data-ttu-id="812c7-271">Cet exemple identifie la règle valide (une) et toutes les règles non valides.</span><span class="sxs-lookup"><span data-stu-id="812c7-271">This example identifies the valid rule (one) and any invalid rules.</span></span>

```powershell
Get-PhishSimOverrideRule | Format-Table Name,Mode
```

<span data-ttu-id="812c7-272">Après avoir identifié les règles non valides, vous pouvez les supprimer à l’aide de la cmdlet **Remove-PhisSimOverrideRule,** comme décrit plus loin [dans cet article.](#use-powershell-to-remove-phishing-simulation-override-rules)</span><span class="sxs-lookup"><span data-stu-id="812c7-272">After you identify the invalid rules, you can remove them by using the **Remove-PhisSimOverrideRule** cmdlet as described [later in this article](#use-powershell-to-remove-phishing-simulation-override-rules).</span></span>

<span data-ttu-id="812c7-273">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-PhishSimOverrideRule](/powershell/module/exchange/get-phishsimoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-273">For detailed syntax and parameter information, see [Get-PhishSimOverrideRule](/powershell/module/exchange/get-phishsimoverriderule).</span></span>

### <a name="use-powershell-to-modify-the-phishing-simulation-override-policy"></a><span data-ttu-id="812c7-274">Utiliser PowerShell pour modifier la stratégie de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-274">Use PowerShell to modify the phishing simulation override policy</span></span>

<span data-ttu-id="812c7-275">Pour modifier la stratégie de remplacement de simulation de hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-275">To modify the phishing simulation override policy, use the following syntax:</span></span>

```powershell
Set-PhishSimOverridePolicy -Identity PhishSimOverridePolicy [-Comment "<DescriptiveText>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="812c7-276">Cet exemple désactive la stratégie de remplacement de simulation de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="812c7-276">This example disables the phishing simulation override policy.</span></span>

```powershell
Set-PhishSimOverridePolicy -Identity PhishSimOverridePolicy -Enabled $false
```

<span data-ttu-id="812c7-277">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-PhishSimOverridePolicy](/powershell/module/exchange/set-phishsimoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-277">For detailed syntax and parameter information, see [Set-PhishSimOverridePolicy](/powershell/module/exchange/set-phishsimoverridepolicy).</span></span>

### <a name="use-powershell-to-modify-a-phishing-simulation-override-rule"></a><span data-ttu-id="812c7-278">Utiliser PowerShell pour modifier une règle de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-278">Use PowerShell to modify a phishing simulation override rule</span></span>

<span data-ttu-id="812c7-279">Pour modifier la règle de remplacement de simulation de hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-279">To modify the phishing simulation override rule, use the following syntax:</span></span>

```powershell
Set-PhishSimOverrideRule -Identity PhishSimOverrideRulea0eae53e-d755-4a42-9320-b9c6b55c5011 [-Comment "<DescriptiveText>"] [-AddSenderDomainIs <DomainEntry1>,<DomainEntry2>,...<DomainEntryN>] [-RemoveSenderDomainIs <DomainEntry1>,<DomainEntry2>,...<DomainEntryN>] [-AddSenderIpRanges <IPAddressEntry1>,<IPAddressEntry2>,...<IPAddressEntryN>] [-RemoveSenderIpRanges <IPAddressEntry1>,<IPAddressEntry2>,...<IPAddressEntryN>]
```

<span data-ttu-id="812c7-280">Cet exemple modifie la règle de remplacement de simulation de hameçonnage spécifiée avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="812c7-280">This example modifies the specified phishing simulation override rule with the following settings:</span></span>

- <span data-ttu-id="812c7-281">Ajoutez l’entrée de domaine blueyonderairlines.com.</span><span class="sxs-lookup"><span data-stu-id="812c7-281">Add the domain entry blueyonderairlines.com.</span></span>
- <span data-ttu-id="812c7-282">Supprimez l’entrée d’adresse IP 192.168.1.55.</span><span class="sxs-lookup"><span data-stu-id="812c7-282">Remove the IP address entry 192.168.1.55.</span></span>

<span data-ttu-id="812c7-283">Notez que ces modifications n’affectent pas les entrées existantes.</span><span class="sxs-lookup"><span data-stu-id="812c7-283">Note that these changes don't affect existing entries.</span></span>

```powershell
Set-PhishSimOverrideRule -Identity PhishSimOverrideRulea0eae53e-d755-4a42-9320-b9c6b55c5011 -AddSenderDomainIs blueyonderairlines.com -RemoveSenderIpRanges 192.168.1.55
```

<span data-ttu-id="812c7-284">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-PhishSimOverrideRule](/powershell/module/exchange/set-phishsimoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-284">For detailed syntax and parameter information, see [Set-PhishSimOverrideRule](/powershell/module/exchange/set-phishsimoverriderule).</span></span>

### <a name="use-powershell-to-remove-a-phishing-simulation-override-policy"></a><span data-ttu-id="812c7-285">Utiliser PowerShell pour supprimer une stratégie de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-285">Use PowerShell to remove a phishing simulation override policy</span></span>

<span data-ttu-id="812c7-286">Cet exemple supprime la stratégie de remplacement de simulation de hameçonnage et la règle correspondante.</span><span class="sxs-lookup"><span data-stu-id="812c7-286">This example removes the phishing simulation override policy and the corresponding rule.</span></span>

```powershell
Remove-PhishSimOverridePolicy -Identity PhishSimOverridePolicy
```

<span data-ttu-id="812c7-287">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-PhishSimOverridePolicy](/powershell/module/exchange/remove-phishsimoverridepolicy).</span><span class="sxs-lookup"><span data-stu-id="812c7-287">For detailed syntax and parameter information, see [Remove-PhishSimOverridePolicy](/powershell/module/exchange/remove-phishsimoverridepolicy).</span></span>

### <a name="use-powershell-to-remove-phishing-simulation-override-rules"></a><span data-ttu-id="812c7-288">Utiliser PowerShell pour supprimer les règles de remplacement de simulation de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="812c7-288">Use PowerShell to remove phishing simulation override rules</span></span>

<span data-ttu-id="812c7-289">Pour supprimer une règle de remplacement de simulation de hameçonnage, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="812c7-289">To remove a phishing simulation override rule, use the following syntax:</span></span>

```powershell
Remove-PhishSimOverrideRule -Identity <RuleIdentity>
```

<span data-ttu-id="812c7-290">Cet exemple supprime la règle de remplacement de simulation de hameçonnage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="812c7-290">This example removes the specified phishing simulation override rule.</span></span>

```powershell
Remove-PhishSimOverrideRule -Identity PhishSimOverrideRulea0eae53e-d755-4a42-9320-b9c6b55c5011
```

<span data-ttu-id="812c7-291">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-PhishSimOverrideRule](/powershell/module/exchange/remove-phishsimoverriderule).</span><span class="sxs-lookup"><span data-stu-id="812c7-291">For detailed syntax and parameter information, see [Remove-PhishSimOverrideRule](/powershell/module/exchange/remove-phishsimoverriderule).</span></span>
