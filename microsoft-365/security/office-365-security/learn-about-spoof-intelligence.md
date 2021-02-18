---
title: Configurer la veille contre l’usurpation d’identité
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur la veille contre l’usurpation d’adresse dans Exchange Online Protection (EOP), où vous pouvez autoriser ou bloquer des expéditeurs usurpés spécifiques.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 2a65400d1b48abfc6ac0e4dd38a8245dd7b4f87b
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289686"
---
# <a name="configure-spoof-intelligence-in-eop"></a><span data-ttu-id="7105b-103">Configurer la veille contre l’usurpation d’adresse dans EOP</span><span class="sxs-lookup"><span data-stu-id="7105b-103">Configure spoof intelligence in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="7105b-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7105b-104">**Applies to**</span></span>
- [<span data-ttu-id="7105b-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="7105b-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="7105b-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="7105b-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="7105b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7105b-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="7105b-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, les messages électroniques entrants sont automatiquement protégés contre l’usurpation d’adresse par EOP à partir d’octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="7105b-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, inbound email messages are automatically protected against spoofing by EOP as of October 2018.</span></span> <span data-ttu-id="7105b-109">EOP utilise la veille contre l’usurpation d’adresse dans le cadre de la protection globale de votre organisation contre le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="7105b-109">EOP uses spoof intelligence as part of your organization's overall defense against phishing.</span></span> <span data-ttu-id="7105b-110">Pour plus d’informations, voir [Protection contre l’usurpation d’adresse dans EOP.](anti-spoofing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="7105b-110">For more information, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="7105b-111">Lorsqu’un expéditeur usurpe une adresse de messagerie, il semble qu’il s’agit d’un utilisateur dans l’un des domaines de votre organisation ou d’un utilisateur d’un domaine externe qui envoie du courrier électronique à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7105b-111">When a sender spoofs an email address, they appear to be a user in one of your organization's domains, or a user in an external domain that sends email to your organization.</span></span> <span data-ttu-id="7105b-112">Les personnes malveillantes qui usurpent des expéditeurs pour envoyer du courrier indésirable ou du hameçonnage doivent être bloquées.</span><span class="sxs-lookup"><span data-stu-id="7105b-112">Attackers who spoof senders to send spam or phishing email need to be blocked.</span></span> <span data-ttu-id="7105b-113">Toutefois, il existe des scénarios dans lequel des expéditeurs légitimes usurpent l’adresse.</span><span class="sxs-lookup"><span data-stu-id="7105b-113">But there are scenarios where legitimate senders are spoofing.</span></span> <span data-ttu-id="7105b-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7105b-114">For example:</span></span>

- <span data-ttu-id="7105b-115">Scénarios légitimes pour l’usurpation d’un domaine interne :</span><span class="sxs-lookup"><span data-stu-id="7105b-115">Legitimate scenarios for spoofing internal domains:</span></span>

  - <span data-ttu-id="7105b-116">Les expéditeurs tiers utilisent votre domaine pour envoyer des messages en bloc à vos propres employés pour les sondages de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7105b-116">Third-party senders use your domain to send bulk mail to your own employees for company polls.</span></span>
  - <span data-ttu-id="7105b-117">Une société externe génère et envoie des mises à jour publicitaires ou des mises à jour de produit en votre nom.</span><span class="sxs-lookup"><span data-stu-id="7105b-117">An external company generates and sends advertising or product updates on your behalf.</span></span>
  - <span data-ttu-id="7105b-118">Un assistant doit régulièrement envoyer des courriers électroniques à une autre personne au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7105b-118">An assistant regularly needs to send email for another person within your organization.</span></span>
  - <span data-ttu-id="7105b-119">Une application interne envoie des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="7105b-119">An internal application sends email notifications.</span></span>

- <span data-ttu-id="7105b-120">Scénarios légitimes d’usurpation de domaines externes :</span><span class="sxs-lookup"><span data-stu-id="7105b-120">Legitimate scenarios for spoofing external domains:</span></span>

  - <span data-ttu-id="7105b-121">L’expéditeur figure sur une liste de diffusion (également appelée liste de discussion) et la liste de diffusion relaie le courrier électronique de l’expéditeur d’origine à tous les participants de la liste de diffusion.</span><span class="sxs-lookup"><span data-stu-id="7105b-121">The sender is on a mailing list (also known as a discussion list), and the mailing list relays email from the original sender to all the participants on the mailing list.</span></span>
  - <span data-ttu-id="7105b-122">Une société externe envoie du courrier électronique pour le compte d’une autre société (par exemple, un rapport automatisé ou une société de logiciels en tant que service).</span><span class="sxs-lookup"><span data-stu-id="7105b-122">An external company sends email on behalf of another company (for example, an automated report or a software-as-a-service company).</span></span>

<span data-ttu-id="7105b-123">La veille contre l’usurpation d’adresses, et plus précisément la stratégie de veille contre l’usurpation d’informations par défaut (et uniquement), permet de s’assurer que les messages électroniques usurpés envoyés par des expéditeurs légitimes ne sont pas pris en compte dans les filtres de courrier indésirable EOP ou les systèmes de messagerie externes, tout en protégeant vos utilisateurs contre les attaques de courrier indésirable ou de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="7105b-123">Spoof intelligence, and specifically the default (and only) spoof intelligence policy, helps ensure that the spoofed email sent by legitimate senders doesn't get caught up in EOP spam filters or external email systems, while protecting your users from spam or phishing attacks.</span></span>

<span data-ttu-id="7105b-124">Vous pouvez gérer la veille contre l’usurpation d’adresse dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="7105b-124">You can manage spoof intelligence in the Security & Compliance Center, or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7105b-125">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7105b-125">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7105b-126">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="7105b-126">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="7105b-127">Pour accéder directement à la page **Paramètres anti-courrier indésirable**, utilisez <https://protection.office.com/antispam>.</span><span class="sxs-lookup"><span data-stu-id="7105b-127">To go directly to the **Anti-spam settings** page, use <https://protection.office.com/antispam>.</span></span> <span data-ttu-id="7105b-128">Pour aller directement à la page **anti-hameçonnage,** utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="7105b-128">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="7105b-129">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7105b-129">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="7105b-130">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="7105b-130">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="7105b-131">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="7105b-131">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="7105b-132">Pour modifier la stratégie de veille contre l’usurpation d’informations ou activer  ou  désactiver la veille contre l’usurpation d’informations, vous devez être membre des groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="7105b-132">To modify the spoof intelligence policy or enable or disable spoof intelligence, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="7105b-133">Pour accéder en lecture seule à la stratégie d’intelligence contre  l’usurpation d’informations, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="7105b-133">For read-only access to the spoof intelligence policy, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="7105b-134">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="7105b-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="7105b-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="7105b-135">**Notes**:</span></span>

  - <span data-ttu-id="7105b-136">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7105b-136">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="7105b-137">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7105b-137">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="7105b-138">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7105b-138">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="7105b-139">Pour obtenir nos paramètres recommandés pour la veille contre l’usurpation d’adresse, consultez les paramètres de stratégie [anti-hameçonnage par défaut d’EOP.](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="7105b-139">For our recommended settings for spoof intelligence, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

## <a name="use-the-security--compliance-center-to-manage-spoofed-senders"></a><span data-ttu-id="7105b-140">Utiliser le Centre de sécurité & conformité pour gérer les expéditeurs usurpés</span><span class="sxs-lookup"><span data-stu-id="7105b-140">Use the Security & Compliance Center to manage spoofed senders</span></span>

> [!NOTE]
> <span data-ttu-id="7105b-141">Si vous avez un abonnement Microsoft 365 Entreprise E5 ou que vous avez acheté séparément un module add-on Microsoft Defender pour Office 365, vous pouvez également gérer les expéditeurs qui usurpent votre domaine via [spoof Intelligence insight](walkthrough-spoof-intelligence-insight.md).</span><span class="sxs-lookup"><span data-stu-id="7105b-141">If you have an Microsoft 365 Enterprise E5 subscription or have separately purchased a Microsoft Defender for Office 365 add-on, you can also manage senders who are spoofing your domain through the [Spoof Intelligence insight](walkthrough-spoof-intelligence-insight.md).</span></span>

1. <span data-ttu-id="7105b-142">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="7105b-142">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="7105b-143">Dans la page **Paramètres anti-courrier** indésirable, cliquez sur Développer l’icône pour développer la stratégie de ![ veille contre ](../../media/scc-expand-icon.png) **l’usurpation d’adresse .**</span><span class="sxs-lookup"><span data-stu-id="7105b-143">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand **Spoof intelligence policy**.</span></span>

   ![Sélectionner la stratégie de veille contre l’usurpation d’informations](../../media/anti-spam-settings-spoof-intelligence-policy.png)

3. <span data-ttu-id="7105b-145">Faites l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="7105b-145">Make one of the following selections:</span></span>

   - <span data-ttu-id="7105b-146">**Passer en revue les nouveaux expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="7105b-146">**Review new senders**</span></span>
   - <span data-ttu-id="7105b-147">**Afficher les expéditeurs que j’ai déjà examinés**</span><span class="sxs-lookup"><span data-stu-id="7105b-147">**Show me senders I already reviewed**</span></span>

4. <span data-ttu-id="7105b-148">Dans **l’onglet Décider si ces** expéditeurs sont autorisés à usurper l’adresse de vos utilisateurs qui s’affiche, sélectionnez l’un des onglets suivants :</span><span class="sxs-lookup"><span data-stu-id="7105b-148">In the **Decide if these senders are allowed to spoof your users** flyout that appears, select one of the following tabs:</span></span>

   - <span data-ttu-id="7105b-149">**Vos domaines : expéditeurs** usurpant des utilisateurs dans vos domaines internes.</span><span class="sxs-lookup"><span data-stu-id="7105b-149">**Your Domains**: Senders spoofing users in your internal domains.</span></span>
   - <span data-ttu-id="7105b-150">**Domaines externes : expéditeurs** usurpant des utilisateurs dans des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="7105b-150">**External Domains**: Senders spoofing users in external domains.</span></span>

5. <span data-ttu-id="7105b-151">Cliquez ![ sur Développer ](../../media/scc-expand-icon.png) l’icône dans **la colonne Usurpation d’usurpation d’accès.**</span><span class="sxs-lookup"><span data-stu-id="7105b-151">Click ![Expand icon](../../media/scc-expand-icon.png) in the **Allowed to spoof?** column.</span></span> <span data-ttu-id="7105b-152">Choisissez **Oui** pour autoriser l’expéditeur usurpé  ou non pour marquer le message comme usurpant l’usurpation.</span><span class="sxs-lookup"><span data-stu-id="7105b-152">Choose **Yes** to allow the spoofed sender, or choose **No** to mark the message as spoofed.</span></span> <span data-ttu-id="7105b-153">L’action est contrôlée par la stratégie anti-hameçonnage par défaut ou les stratégies anti-hameçonnage personnalisées (la valeur par défaut est Déplacer le message vers le dossier **Courrier indésirable).**</span><span class="sxs-lookup"><span data-stu-id="7105b-153">The action is controlled by the default anti-phishing policy or custom anti-phishing policies (the default value is **Move message to Junk Email folder**).</span></span> <span data-ttu-id="7105b-154">Pour plus d’informations, voir Paramètres d’usurpation [d’informations dans les stratégies anti-hameçonnage.](set-up-anti-phishing-policies.md#spoof-settings)</span><span class="sxs-lookup"><span data-stu-id="7105b-154">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   ![Screenshot showing the spoofed senders flyout, and whether the sender is allowed to spoof](../../media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)

   <span data-ttu-id="7105b-156">Les colonnes et les valeurs que vous voyez sont expliquées dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="7105b-156">The columns and values that you see are explained in the following list:</span></span>

   - <span data-ttu-id="7105b-157">**Utilisateur usurpé :** compte d’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="7105b-157">**Spoofed user**: The user account that's being spoofed.</span></span> <span data-ttu-id="7105b-158">Il s’agit de l’expéditeur du message dans l’adresse de provenance (également appelée adresse) qui `5322.From` s’affiche dans les clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7105b-158">This is the message sender in the From address (also known as the `5322.From` address) that's shown in email clients.</span></span> <span data-ttu-id="7105b-159">La validité de cette adresse n’est pas vérifiée par SPF.</span><span class="sxs-lookup"><span data-stu-id="7105b-159">The validity of this address is not checked by SPF.</span></span>

     - <span data-ttu-id="7105b-160">Sous **l’onglet** Vos domaines, la valeur contient une seule adresse de messagerie, ou si le serveur de messagerie source usurpe plusieurs comptes d’utilisateur, il en contient **plusieurs.**</span><span class="sxs-lookup"><span data-stu-id="7105b-160">On the **Your Domains** tab, the value contains a single email address, or if the source email server is spoofing multiple user accounts, it contains **More than one**.</span></span>

     - <span data-ttu-id="7105b-161">Sous **l’onglet Domaines externes,** la valeur contient le domaine de l’utilisateur usurpé, et non l’adresse de messagerie complète.</span><span class="sxs-lookup"><span data-stu-id="7105b-161">On the **External Domains** tab, the value contains the domain of the spoofed user, not the full email address.</span></span>

   - <span data-ttu-id="7105b-162">**Infrastructure d’envoi**: domaine trouvé dans une recherche DNS inversée (enregistrement PTR) de l’adresse IP du serveur de messagerie source.</span><span class="sxs-lookup"><span data-stu-id="7105b-162">**Sending Infrastructure**: The domain found in a reverse DNS lookup (PTR record) of the source email server's IP address.</span></span> <span data-ttu-id="7105b-163">Si l’adresse IP source n’a pas d’enregistrement PTR, l’infrastructure d’envoi est identifiée comme \<source IP\> /24 (par exemple, 192.168.100.100/24).</span><span class="sxs-lookup"><span data-stu-id="7105b-163">If the source IP address has no PTR record, then the sending infrastructure is identified as \<source IP\>/24 (for example, 192.168.100.100/24).</span></span>

     <span data-ttu-id="7105b-164">Pour plus d’informations sur les sources de messages et les expéditeurs de messages, voir [une vue d’ensemble des normes de message électronique.](how-office-365-validates-the-from-address.md#an-overview-of-email-message-standards)</span><span class="sxs-lookup"><span data-stu-id="7105b-164">For more information about message sources and message senders, see [An overview of email message standards](how-office-365-validates-the-from-address.md#an-overview-of-email-message-standards).</span></span>

   - <span data-ttu-id="7105b-165">**# des messages**: nombre de messages de l’infrastructure d’envoi à votre organisation qui contiennent l’expéditeur ou les expéditeurs usurpés spécifiés au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="7105b-165">**# of messages**: The number of messages from the sending infrastructure to your organization that contain the specified spoofed sender or senders within the last 30 days.</span></span>

   - <span data-ttu-id="7105b-166">**# des réclamations des utilisateurs**: réclamations déposées par vos utilisateurs contre cet expéditeur au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="7105b-166">**# of user complaints**: Complaints filed by your users against this sender within the last 30 days.</span></span> <span data-ttu-id="7105b-167">Les réclamations se font généralement sous la forme de soumissions de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7105b-167">Complaints are usually in the form of junk submissions to Microsoft.</span></span>

   - <span data-ttu-id="7105b-168">**Résultat de l’authentification**: l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7105b-168">**Authentication result**: One of the following values:</span></span>
      - <span data-ttu-id="7105b-169">**Réussi :** l’expéditeur a réussi les vérifications d’authentification de courrier électronique de l’expéditeur (SPF ou DKIM).</span><span class="sxs-lookup"><span data-stu-id="7105b-169">**Passed**: The sender passed sender email authentication checks (SPF or DKIM).</span></span>
      - <span data-ttu-id="7105b-170">**Échec :** l’expéditeur a échoué aux vérifications d’authentification de l’expéditeur EOP.</span><span class="sxs-lookup"><span data-stu-id="7105b-170">**Failed**: The sender failed EOP sender authentication checks.</span></span>
      - <span data-ttu-id="7105b-171">**Inconnu**: le résultat de ces vérifications est inconnu.</span><span class="sxs-lookup"><span data-stu-id="7105b-171">**Unknown**: The result of these checks isn't known.</span></span>

   - <span data-ttu-id="7105b-172">**Décision définie par**: indique qui a déterminé si l’infrastructure d’envoi est autorisée à usurper l’usurpation de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="7105b-172">**Decision set by**: Shows who determined if the sending infrastructure is allowed to spoof the user:</span></span>
       - <span data-ttu-id="7105b-173">**Stratégie de veille contre l’usurpation** d’informations (automatique)</span><span class="sxs-lookup"><span data-stu-id="7105b-173">**Spoof intelligence policy** (automatic)</span></span>
       - <span data-ttu-id="7105b-174">**Administrateur** (manuel)</span><span class="sxs-lookup"><span data-stu-id="7105b-174">**Admin** (manual)</span></span>

   - <span data-ttu-id="7105b-175">**Dernière vue**: date de la dernière réception d’un message de l’infrastructure d’envoi contenant l’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="7105b-175">**Last seen**: The last date when a message was received from the sending infrastructure that contains the spoofed user.</span></span>

   - <span data-ttu-id="7105b-176">**Autorisé à usurper ? :** les valeurs que vous voyez ici sont :</span><span class="sxs-lookup"><span data-stu-id="7105b-176">**Allowed to spoof?**: The values that you see here are:</span></span>
     - <span data-ttu-id="7105b-177">**Oui**: les messages provenant de la combinaison de l’utilisateur usurpé et de l’infrastructure d’envoi sont autorisés et ne sont pas traités comme des e-mails usurpés.</span><span class="sxs-lookup"><span data-stu-id="7105b-177">**Yes**: Messages from the combination of spoofed user and sending infrastructure are allowed and not treated as spoofed email.</span></span>
     - <span data-ttu-id="7105b-178">**Non**: les messages provenant de la combinaison de l’utilisateur usurpé et de l’infrastructure d’envoi sont marqués comme usurpés.</span><span class="sxs-lookup"><span data-stu-id="7105b-178">**No**: Messages from the combination of spoofed user and sending infrastructure are marked as spoofed.</span></span> <span data-ttu-id="7105b-179">L’action est contrôlée par la stratégie anti-hameçonnage par défaut ou les stratégies anti-hameçonnage personnalisées (la valeur par défaut est Déplacer le message vers le dossier **Courrier indésirable).**</span><span class="sxs-lookup"><span data-stu-id="7105b-179">The action is controlled by the default anti-phishing policy or custom anti-phishing policies (the default value is **Move message to Junk Email folder**).</span></span> <span data-ttu-id="7105b-180">Pour plus d’informations, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="7105b-180">See the next section for more information.</span></span>

     - <span data-ttu-id="7105b-181">**Certains utilisateurs** (onglet Vos domaines uniquement) : une infrastructure d’envoi usurpe plusieurs **utilisateurs,** où certains utilisateurs usurpés sont autorisés et d’autres non.</span><span class="sxs-lookup"><span data-stu-id="7105b-181">**Some users** (**Your Domains** tab only): A sending infrastructure is spoofing multiple users, where some spoofed users are allowed and others are not.</span></span> <span data-ttu-id="7105b-182">Utilisez **l’onglet Détails** pour voir les adresses spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7105b-182">Use the **Detailed** tab to see the specific addresses.</span></span>

6. <span data-ttu-id="7105b-183">En bas de la page, cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="7105b-183">At the bottom of the page, click **Save**.</span></span>

## <a name="use-powershell-to-manage-spoofed-senders"></a><span data-ttu-id="7105b-184">Utiliser PowerShell pour gérer les expéditeurs usurpés</span><span class="sxs-lookup"><span data-stu-id="7105b-184">Use PowerShell to manage spoofed senders</span></span>

<span data-ttu-id="7105b-185">Pour afficher les expéditeurs autorisés et bloqués dans la veille contre l’usurpation d’adresse, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7105b-185">To view allowed and blocked senders in spoof intelligence, use the following syntax:</span></span>

```powershell
Get-PhishFilterPolicy [-AllowedToSpoof <Yes | No | Partial>] [-ConfidenceLevel <Low | High>] [-DecisionBy <Admin | SpoofProtection>] [-Detailed] [-SpoofType <Internal | External>]
```

<span data-ttu-id="7105b-186">Cet exemple renvoie des informations détaillées sur tous les expéditeurs autorisés à usurper des noms d’utilisateurs dans vos domaines.</span><span class="sxs-lookup"><span data-stu-id="7105b-186">This example returns detailed information about all senders that are allowed to spoof users in your domains.</span></span>

```powershell
Get-PhishFilterPolicy -AllowedToSpoof Yes -Detailed -SpoofType Internal
```

<span data-ttu-id="7105b-187">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-PhishFilterPolicy.](https://docs.microsoft.com/powershell/module/exchange/get-phishfilterpolicy)</span><span class="sxs-lookup"><span data-stu-id="7105b-187">For detailed syntax and parameter information, see [Get-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-phishfilterpolicy).</span></span>

<span data-ttu-id="7105b-188">Pour configurer les expéditeurs autorisés et bloqués dans la veille contre l’usurpation d’adresse, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7105b-188">To configure allowed and blocked senders in spoof intelligence, follow these steps:</span></span>

1. <span data-ttu-id="7105b-189">Capturez la liste actuelle des expéditeurs usurpés détectés en écrivant la sortie de l’cmdlet **Get-PhishFilterPolicy** dans un fichier CSV :</span><span class="sxs-lookup"><span data-stu-id="7105b-189">Capture the current list of detected spoofed senders by writing the output of the **Get-PhishFilterPolicy** cmdlet to a CSV file:</span></span>

   ```powershell
   Get-PhishFilterPolicy -Detailed | Export-CSV "C:\My Documents\Spoofed Senders.csv"
   ```

2. <span data-ttu-id="7105b-190">Modifiez le fichier CSV pour ajouter ou modifier les valeurs **SpoofedUser** (adresse e-mail) et **AllowedToSpoof** (Oui ou Non).</span><span class="sxs-lookup"><span data-stu-id="7105b-190">Edit the CSV file to add or modify the **SpoofedUser** (email address) and **AllowedToSpoof** (Yes or No) values.</span></span> <span data-ttu-id="7105b-191">Enregistrez le fichier, lisez-le et stockez le contenu en tant que variable nommée `$UpdateSpoofedSenders` :</span><span class="sxs-lookup"><span data-stu-id="7105b-191">Save the file, read the file, and store the contents as a variable named `$UpdateSpoofedSenders`:</span></span>

   ```powershell
   $UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
   ```

3. <span data-ttu-id="7105b-192">Utilisez la `$UpdateSpoofedSenders` variable pour configurer la stratégie d’intelligence contre l’usurpation d’informations :</span><span class="sxs-lookup"><span data-stu-id="7105b-192">Use the `$UpdateSpoofedSenders` variable to configure the spoof intelligence policy:</span></span>

   ```powershell
   Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
   ```

<span data-ttu-id="7105b-193">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-PhishFilterPolicy.](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy)</span><span class="sxs-lookup"><span data-stu-id="7105b-193">For detailed syntax and parameter information, see [Set-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy).</span></span>

## <a name="use-the-security--compliance-center-to-configure-spoof-intelligence"></a><span data-ttu-id="7105b-194">Utiliser le Centre de sécurité & conformité pour configurer la veille contre l’usurpation d’informations</span><span class="sxs-lookup"><span data-stu-id="7105b-194">Use the Security & Compliance Center to configure spoof intelligence</span></span>

<span data-ttu-id="7105b-195">Les options de configuration pour la veille contre l’usurpation d’informations sont décrites dans les paramètres d’usurpation d’informations dans les [stratégies anti-hameçonnage.](set-up-anti-phishing-policies.md#spoof-settings)</span><span class="sxs-lookup"><span data-stu-id="7105b-195">The configuration options for spoof intelligence are described in [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="7105b-196">Vous pouvez configurer les paramètres de veille contre l’usurpation d’informations dans la stratégie anti-hameçonnage par défaut, ainsi que dans les stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7105b-196">You can configure spoof intelligence settings in the default anti-phishing policy, and also in custom policies.</span></span> <span data-ttu-id="7105b-197">Pour obtenir des instructions basées sur votre abonnement, consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7105b-197">For instructions based on your subscription, see one of the following topics:</span></span>

- <span data-ttu-id="7105b-198">[Configurer des stratégies anti-hameçonnage dans EOP.](configure-anti-phishing-policies-eop.md)</span><span class="sxs-lookup"><span data-stu-id="7105b-198">[Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

- <span data-ttu-id="7105b-199">[Configurer des stratégies anti-hameçonnage dans Microsoft Defender pour Office 365.](configure-atp-anti-phishing-policies.md)</span><span class="sxs-lookup"><span data-stu-id="7105b-199">[Configure anti-phishing policies in Microsoft Defender for Office 365](configure-atp-anti-phishing-policies.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="7105b-200">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="7105b-200">How do you know these procedures worked?</span></span>

<span data-ttu-id="7105b-201">Pour vérifier que vous avez configuré la veille contre l’usurpation d’identité avec des expéditeurs autorisés et non autorisés à usurper l’identité, et que vous avez configuré les paramètres de veille contre l’usurpation d’identité, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7105b-201">To verify that you've configured spoof intelligence with senders who are allowed and not allowed to spoof, and that you've configured the spoof intelligence settings, use any of the following steps:</span></span>

- <span data-ttu-id="7105b-202">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam** \> expand **Spoof intelligence policy** select Show me \> **senders I already reviewed** select the Your \> **Domains** or External **Domains** tab, and verify the **Allowed to spoof?** value for the sender.</span><span class="sxs-lookup"><span data-stu-id="7105b-202">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam** \> expand **Spoof intelligence policy** \> select **Show me senders I already reviewed** \> select the **Your Domains** or **External Domains** tab, and verify the **Allowed to spoof?** value for the sender.</span></span>

- <span data-ttu-id="7105b-203">Dans PowerShell, exécutez les commandes suivantes pour afficher les expéditeurs autorisés et non autorisés à usurper :</span><span class="sxs-lookup"><span data-stu-id="7105b-203">In PowerShell, run the following commands to view the senders who are allowed and not allowed to spoof:</span></span>

  ```powershell
  Get-PhishFilterPolicy -AllowedToSpoof Yes -SpoofType Internal
  Get-PhishFilterPolicy -AllowedToSpoof No -SpoofType Internal
  Get-PhishFilterPolicy -AllowedToSpoof Yes -SpoofType External
  Get-PhishFilterPolicy -AllowedToSpoof No -SpoofType External
  ```

- <span data-ttu-id="7105b-204">Dans PowerShell, exécutez la commande suivante pour exporter la liste de tous les expéditeurs usurpés vers un fichier CSV :</span><span class="sxs-lookup"><span data-stu-id="7105b-204">In PowerShell, run the following command to export the list of all spoofed senders to a CSV file:</span></span>

   ```powershell
   Get-PhishFilterPolicy -Detailed | Export-CSV "C:\My Documents\Spoofed Senders.csv"
   ```

- <span data-ttu-id="7105b-205">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Anti-phishing** or **ATP anti-phishing**, and do either the following steps:  </span><span class="sxs-lookup"><span data-stu-id="7105b-205">In the Security & Compliance Center, go to **Threat management** \> **Policy**  \> **Anti-phishing**  or **ATP anti-phishing**, and do either of the following steps:</span></span>

  - <span data-ttu-id="7105b-206">Sélectionnez une stratégie dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7105b-206">Select a policy from the list.</span></span> <span data-ttu-id="7105b-207">Dans le volant qui s’affiche, vérifiez les valeurs dans la section **Usurpation d’identité.**</span><span class="sxs-lookup"><span data-stu-id="7105b-207">In the flyout that appears, verify the values in the **Spoof** section.</span></span>
  - <span data-ttu-id="7105b-208">Cliquez **sur Stratégie par défaut.**</span><span class="sxs-lookup"><span data-stu-id="7105b-208">Click **Default policy**.</span></span> <span data-ttu-id="7105b-209">Dans le volant qui s’affiche, vérifiez les valeurs dans la section **Usurpation d’identité.**</span><span class="sxs-lookup"><span data-stu-id="7105b-209">In the flyout that appears, verify the values in the **Spoof** section.</span></span>

- <span data-ttu-id="7105b-210">Dans Exchange Online PowerShell, remplacez par Office 365 AntiPhish Default ou le nom d’une stratégie personnalisée, puis exécutez la commande suivante pour vérifier \<Name\> les paramètres :</span><span class="sxs-lookup"><span data-stu-id="7105b-210">In Exchange Online PowerShell, replace \<Name\> with Office365 AntiPhish Default or the name of a custom policy, and run the following command to verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>" | Format-List EnableSpoofIntelligence,EnableUnauthenticatedSender,AuthenticationFailAction
  ```

## <a name="other-ways-to-manage-spoofing-and-phishing"></a><span data-ttu-id="7105b-211">Autres façons de gérer l’usurpation et le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="7105b-211">Other ways to manage spoofing and phishing</span></span>

<span data-ttu-id="7105b-212">Soyez prudent sur l’usurpation d’informations et la protection contre le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="7105b-212">Be diligent about spoofing and phishing protection.</span></span> <span data-ttu-id="7105b-213">Voici quelques méthodes connexes pour vérifier les expéditeurs usurpant votre domaine et les empêcher d’endommager votre organisation :</span><span class="sxs-lookup"><span data-stu-id="7105b-213">Here are related ways to check on senders spoofing your domain and help prevent them from damaging your organization:</span></span>

- <span data-ttu-id="7105b-214">Vérifiez le **rapport de courrier d’usurpation d’adresse .**</span><span class="sxs-lookup"><span data-stu-id="7105b-214">Check the **Spoof Mail Report**.</span></span> <span data-ttu-id="7105b-215">Vous pouvez souvent utiliser ce rapport pour afficher et gérer les expéditeurs usurpés.</span><span class="sxs-lookup"><span data-stu-id="7105b-215">You can use this report often to view and help manage spoofed senders.</span></span> <span data-ttu-id="7105b-216">Pour plus d’informations, [voir le rapport sur les détections d’usurpation d’informations.](view-email-security-reports.md#spoof-detections-report)</span><span class="sxs-lookup"><span data-stu-id="7105b-216">For information, see [Spoof Detections report](view-email-security-reports.md#spoof-detections-report).</span></span>

- <span data-ttu-id="7105b-217">Examinez votre configuration SPF (Sender Policy Framework).</span><span class="sxs-lookup"><span data-stu-id="7105b-217">Review your Sender Policy Framework (SPF) configuration.</span></span> <span data-ttu-id="7105b-218">Pour consulter une brève présentation de SPF et le configurer rapidement, voir [Configurer SPF dans Microsoft 365 pour empêcher l’usurpation d’identité](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="7105b-218">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Microsoft 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="7105b-219">Pour consulter des informations plus approfondies sur l’utilisation de SPF par Office 365, la résolution des problèmes et les déploiements non standard tels que les déploiements hybrides, voir Comment Office 365 utilise SPF (Sender Policy Framework) pour empêcher l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="7105b-219">For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span>

- <span data-ttu-id="7105b-220">Examinez votre configuration DKIM (DomainKeys Identified Mail).</span><span class="sxs-lookup"><span data-stu-id="7105b-220">Review your DomainKeys Identified Mail (DKIM) configuration.</span></span> <span data-ttu-id="7105b-221">Vous devez utiliser DKIM en plus de SPF et DMARC pour empêcher les personnes malveillantes d’envoyer des messages qui semblent provenant de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="7105b-221">You should use DKIM in addition to SPF and DMARC to help prevent attackers from sending messages that look like they are coming from your domain.</span></span> <span data-ttu-id="7105b-222">DKIM vous permet d'ajouter une signature numérique aux messages électroniques dans l'en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="7105b-222">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="7105b-223">Pour plus d’informations, voir Utiliser DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé [dans Office 365.](use-dkim-to-validate-outbound-email.md)</span><span class="sxs-lookup"><span data-stu-id="7105b-223">For information, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

- <span data-ttu-id="7105b-224">Examinez votre configuration DMARC (Domain-based Message Authentication, Reporting, and Conformance).</span><span class="sxs-lookup"><span data-stu-id="7105b-224">Review your Domain-based Message Authentication, Reporting, and Conformance (DMARC) configuration.</span></span> <span data-ttu-id="7105b-225">L’implémentation de DMARC avec SPF et DKIM fournit une protection supplémentaire contre l’usurpation et les courriers de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="7105b-225">Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email.</span></span> <span data-ttu-id="7105b-226">DMARC permet aux systèmes de messagerie de réception de déterminer ce qu’ils doivent faire des messages envoyés à partir de votre domaine qui sont rejetés par les contrôles de SPF ou de DKIM.</span><span class="sxs-lookup"><span data-stu-id="7105b-226">DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span> <span data-ttu-id="7105b-227">Pour plus d’informations, [voir Utiliser DMARC pour valider le courrier électronique dans Office 365.](use-dmarc-to-validate-email.md)</span><span class="sxs-lookup"><span data-stu-id="7105b-227">For information, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>
