---
title: Configurer l’intelligence usurpée
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur l’usurpation d’identité dans Exchange Online Protection (EOP), où vous pouvez autoriser ou bloquer des expéditeurs usurpés spécifiques.
ms.openlocfilehash: e1c282076d054c338a02a50412ec376406f5ce98
ms.sourcegitcommit: df6cc8c2eb2a65c7668f2953b0f7ec783a596d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/13/2020
ms.locfileid: "44726747"
---
# <a name="configure-spoof-intelligence-in-eop"></a><span data-ttu-id="cb5ea-103">Configurer l’intelligence des usurpations d’identité dans EOP</span><span class="sxs-lookup"><span data-stu-id="cb5ea-103">Configure spoof intelligence in EOP</span></span>

<span data-ttu-id="cb5ea-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, les messages électroniques entrants sont automatiquement protégés contre l’usurpation par EOP au 1er octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, inbound email messages are automatically protected against spoofing by EOP as of October 2018.</span></span> <span data-ttu-id="cb5ea-105">EOP utilise l’intelligence d’usurpation d’identité dans le cadre de la protection globale de votre organisation contre le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-105">EOP uses spoof intelligence as part of your organization's overall defense against phishing.</span></span> <span data-ttu-id="cb5ea-106">Pour plus d’informations, consultez la rubrique [protection contre l’usurpation d’adresses dans EOP](anti-spoofing-protection.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-106">For more information, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="cb5ea-107">Lorsqu’un expéditeur usurpe une adresse de messagerie, il semble être un utilisateur de l’un des domaines de votre organisation ou un utilisateur dans un domaine externe qui envoie des messages à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-107">When a sender spoofs an email address, they appear to be a user in one of your organization's domains, or a user in an external domain that sends email to your organization.</span></span> <span data-ttu-id="cb5ea-108">Les agresseurs qui usurpent des expéditeurs pour envoyer du courrier indésirable ou des tentatives de hameçonnage doivent être bloqués.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-108">Attackers who spoof senders to send spam or phishing email need to be blocked.</span></span> <span data-ttu-id="cb5ea-109">Toutefois, il existe des scénarios dans lesquels les expéditeurs légitimes sont usurpés.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-109">But there are scenarios where legitimate senders are spoofing.</span></span> <span data-ttu-id="cb5ea-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-110">For example:</span></span>

- <span data-ttu-id="cb5ea-111">Scénarios légitimes pour l’usurpation des domaines internes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-111">Legitimate scenarios for spoofing internal domains:</span></span>

  - <span data-ttu-id="cb5ea-112">Les expéditeurs tiers utilisent votre domaine pour envoyer du courrier en nombre à vos employés pour les sondages de sociétés.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-112">Third-party senders use your domain to send bulk mail to your own employees for company polls.</span></span>

  - <span data-ttu-id="cb5ea-113">Une société externe génère et envoie des mises à jour de la publicité ou des produits en votre nom.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-113">An external company generates and sends advertising or product updates on your behalf.</span></span>

  - <span data-ttu-id="cb5ea-114">Un assistant doit régulièrement envoyer un message électronique à une autre personne au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-114">An assistant regularly needs to send email for another person within your organization.</span></span>

  - <span data-ttu-id="cb5ea-115">Une application interne envoie des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-115">An internal application sends email notifications.</span></span>

- <span data-ttu-id="cb5ea-116">Scénarios légitimes pour l’usurpation de domaines externes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-116">Legitimate scenarios for spoofing external domains:</span></span>

  - <span data-ttu-id="cb5ea-117">L’expéditeur figure sur une liste de publipostage (également appelée liste de discussion) et la liste de distribution relaie le courrier de l’expéditeur d’origine vers tous les participants de la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-117">The sender is on a mailing list (also known as a discussion list), and the mailing list relays email from the original sender to all the participants on the mailing list.</span></span>

  - <span data-ttu-id="cb5ea-118">Une société externe envoie un courrier électronique au nom d’une autre société (par exemple, un rapport automatisé ou une société de service de logiciel).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-118">An external company sends email on behalf of another company (for example, an automated report or a software-as-a-service company).</span></span>

<span data-ttu-id="cb5ea-119">L’intelligence d’usurpation d’identité, et en particulier la stratégie d’intelligence d’usurpation par défaut (et uniquement), permet de s’assurer que le courrier électronique usurpé envoyé par des expéditeurs légitimes ne se trouve pas dans les filtres de courrier indésirable EOP ou les systèmes de messagerie externes, tout en protégeant vos utilisateurs contre le courrier indésirable ou le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="cb5ea-119">Spoof intelligence, and specifically the default (and only) spoof intelligence policy, helps ensure that the spoofed email sent by legitimate senders doesn't get caught up in EOP spam filters or external email systems, while protecting your users from spam or phishing attacks.</span></span>

<span data-ttu-id="cb5ea-120">Vous pouvez gérer l’aide à la décision dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-120">You can manage spoof intelligence in the Security & Compliance Center, or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cb5ea-121">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cb5ea-121">What do you need to know before you begin?</span></span>

- <span data-ttu-id="cb5ea-122">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-122">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="cb5ea-123">Pour accéder directement à la page **Paramètres anti-courrier indésirable**, utilisez <https://protection.office.com/antispam>.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-123">To go directly to the **Anti-spam settings** page, use <https://protection.office.com/antispam>.</span></span> <span data-ttu-id="cb5ea-124">Pour accéder directement à la page **anti-hameçonnage** , utilisez <https://protection.office.com/antiphishing> .</span><span class="sxs-lookup"><span data-stu-id="cb5ea-124">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="cb5ea-125">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-125">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="cb5ea-126">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-126">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="cb5ea-127">Avant de pouvoir effectuer les procédures décrites dans cette rubrique, vous devez disposer des autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-127">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="cb5ea-128">Pour modifier la stratégie d’intelligence de falsification ou activer ou désactiver l’aide à l’usurpation d’identité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-128">To modify the spoof intelligence policy or enable or disable spoof intelligence, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="cb5ea-129">**Gestion** de l’organisation ou **administrateur de sécurité** dans le [Centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-129">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="cb5ea-130">Gestion de l' **organisation** ou gestion de l' **hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-130">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="cb5ea-131">Pour un accès en lecture seule à la stratégie d’aide à la décision, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-131">For read-only access to the spoof intelligence policy, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="cb5ea-132">**Lecteur de sécurité** dans le [centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-132">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="cb5ea-133">**Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-133">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="cb5ea-134">Pour connaître les paramètres recommandés pour l’intelligence d’usurpation, voir paramètres de la [stratégie anti-hameçonnage par défaut EOP](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-134">For our recommended settings for spoof intelligence, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

## <a name="use-the-security--compliance-center-to-manage-spoofed-senders"></a><span data-ttu-id="cb5ea-135">Utiliser le centre de sécurité & conformité pour gérer les expéditeurs usurpés</span><span class="sxs-lookup"><span data-stu-id="cb5ea-135">Use the Security & Compliance Center to manage spoofed senders</span></span>

> [!NOTE]
> <span data-ttu-id="cb5ea-136">Si vous disposez d’un abonnement Microsoft 365 entreprise E5 ou si vous avez acheté séparément un complément Office 365 Advanced Threat Protection (Office 365 ATP), vous pouvez également gérer les expéditeurs qui usurpent votre domaine via la fonctionnalité d’aide à la [décision](walkthrough-spoof-intelligence-insight.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-136">If you have an Microsoft 365 Enterprise E5 subscription or have separately purchased an Office 365 Advanced Threat Protection (Office 365 ATP) add-on, you can also manage senders who are spoofing your domain through the [Spoof Intelligence insight](walkthrough-spoof-intelligence-insight.md).</span></span>

1. <span data-ttu-id="cb5ea-137">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Stratégie** \> **Anti-courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-137">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam**.</span></span>

2. <span data-ttu-id="cb5ea-138">Dans la page **paramètres de blocage du courrier indésirable** , cliquez sur ![ développer ](../../media/scc-expand-icon.png) pour développer stratégie d’aide à la **décision**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-138">On the **Anti-spam settings** page, click ![Expand icon](../../media/scc-expand-icon.png) to expand **Spoof intelligence policy**.</span></span>

   ![Sélectionner la stratégie d’intelligence d’usurpation d’identité](../../media/anti-spam-settings-spoof-intelligence-policy.png)

3. <span data-ttu-id="cb5ea-140">Effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-140">Make one of the following selections:</span></span>

   - <span data-ttu-id="cb5ea-141">**Vérifier les nouveaux expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="cb5ea-141">**Review new senders**</span></span>
   - <span data-ttu-id="cb5ea-142">**Afficher les expéditeurs que j’ai déjà consultés**</span><span class="sxs-lookup"><span data-stu-id="cb5ea-142">**Show me senders I already reviewed**</span></span>

4. <span data-ttu-id="cb5ea-143">Dans la fenêtre **décider si ces expéditeurs sont autorisés à usurper votre** sélection, sélectionnez l’un des onglets suivants :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-143">In the **Decide if these senders are allowed to spoof your users** flyout that appears, select one of the following tabs:</span></span>

   - <span data-ttu-id="cb5ea-144">**Vos domaines**: les expéditeurs usurpant l’identité des utilisateurs dans vos domaines internes.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-144">**Your Domains**: Senders spoofing users in your internal domains.</span></span>
   - <span data-ttu-id="cb5ea-145">**Domaines externes**: les expéditeurs usurpant l’identité des utilisateurs dans les domaines externes.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-145">**External Domains**: Senders spoofing users in external domains.</span></span>

5. <span data-ttu-id="cb5ea-146">Cliquez sur ![ développer une icône ](../../media/scc-expand-icon.png) dans la colonne **autorisé à usurper** .</span><span class="sxs-lookup"><span data-stu-id="cb5ea-146">Click ![Expand icon](../../media/scc-expand-icon.png) in the **Allowed to spoof?** column.</span></span> <span data-ttu-id="cb5ea-147">Choisissez **Oui** pour autoriser l’expéditeur usurpé ou **non** pour marquer le message comme falsifié.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-147">Choose **Yes** to allow the spoofed sender, or choose **No** to mark the message as spoofed.</span></span> <span data-ttu-id="cb5ea-148">L’action est contrôlée par la stratégie anti-hameçonnage par défaut ou par des stratégies anti-hameçonnage personnalisées ATP (la valeur par défaut est **déplacer le message vers le dossier courrier indésirable**).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-148">The action is controlled by the default anti-phishing policy or custom ATP anti-phishing policies (the default value is **Move message to Junk Email folder**).</span></span> <span data-ttu-id="cb5ea-149">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-149">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   ![Capture d’écran montrant le menu volant des expéditeurs falsifiés et indique si l’expéditeur est autorisé à usurper](../../media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)

   <span data-ttu-id="cb5ea-151">Les colonnes et les valeurs que vous voyez sont expliquées dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-151">The columns and values that you see are explained in the following list:</span></span>

   - <span data-ttu-id="cb5ea-152">**Utilisateur usurpé**: le compte d’utilisateur qui est usurpé.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-152">**Spoofed user**: The user account that's being spoofed.</span></span> <span data-ttu-id="cb5ea-153">Il s’agit de l’expéditeur du message dans l’adresse de provenance (également appelée `5322.From` adresse) qui apparaît dans les clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-153">This is the message sender in the From address (also known as the `5322.From` address) that's shown in email clients.</span></span> <span data-ttu-id="cb5ea-154">La validité de cette adresse n’est pas vérifiée par SPF.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-154">The validity of this address is not checked by SPF.</span></span>

     - <span data-ttu-id="cb5ea-155">Dans l’onglet **vos domaines** , la valeur contient une adresse de messagerie unique, ou si le serveur de messagerie source usurpe plusieurs comptes d’utilisateur, il en contient **plusieurs**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-155">On the **Your Domains** tab, the value contains a single email address, or if the source email server is spoofing multiple user accounts, it contains **More than one**.</span></span>

     - <span data-ttu-id="cb5ea-156">Sous l’onglet **domaines externes** , la valeur contient le domaine de l’utilisateur usurpé, et non l’adresse de messagerie complète.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-156">On the **External Domains** tab, the value contains the domain of the spoofed user, not the full email address.</span></span>

   - <span data-ttu-id="cb5ea-157">**Infrastructure d’envoi**: domaine trouvé dans une recherche DNS inversée (enregistrement PTR) de l’adresse IP du serveur de messagerie source ou adresse IP si la source n’a pas d’enregistrement PTR.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-157">**Sending Infrastructure**: The domain found in a reverse DNS lookup (PTR record) of the source email server's IP address, or the IP address if the source has no PTR record.</span></span>

     <span data-ttu-id="cb5ea-158">Pour plus d’informations sur les sources de messages et les expéditeurs de messages, voir [une vue d’ensemble des normes des messages électroniques](how-office-365-validates-the-from-address.md#an-overview-of-email-message-standards).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-158">For more information about message sources and message senders, see [An overview of email message standards](how-office-365-validates-the-from-address.md#an-overview-of-email-message-standards).</span></span>

   - <span data-ttu-id="cb5ea-159">**Nbre de messages**: nombre de messages provenant de l’infrastructure d’envoi à votre organisation qui contiennent l’expéditeur ou les expéditeurs usurpés au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-159">**# of messages**: The number of messages from the sending infrastructure to your organization that contain the specified spoofed sender or senders within the last 30 days.</span></span>

   - <span data-ttu-id="cb5ea-160">**nombre de plaintes de l’utilisateur**: plaintes déposées par vos utilisateurs par rapport à cet expéditeur au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-160">**# of user complaints**: Complaints filed by your users against this sender within the last 30 days.</span></span> <span data-ttu-id="cb5ea-161">Les plaintes se présentent généralement sous la forme d’envois de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-161">Complaints are usually in the form of junk submissions to Microsoft.</span></span>

   - <span data-ttu-id="cb5ea-162">**Résultat de l’authentification**: l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-162">**Authentication result**: One of the following values:</span></span>

      - <span data-ttu-id="cb5ea-163">**Réussite**: l’expéditeur a passé des vérifications d’authentification de courrier électronique de l’expéditeur (SPF ou DKIM).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-163">**Passed**: The sender passed sender email authentication checks (SPF or DKIM).</span></span>
      - <span data-ttu-id="cb5ea-164">**Échec**: l’expéditeur a échoué aux vérifications d’authentification de l’expéditeur EOP.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-164">**Failed**: The sender failed EOP sender authentication checks.</span></span>
      - <span data-ttu-id="cb5ea-165">**Inconnu**: le résultat de ces vérifications n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-165">**Unknown**: The result of these checks isn't known.</span></span>

   - <span data-ttu-id="cb5ea-166">**Décision définie par**: indique qui a déterminé si l’infrastructure d’envoi est autorisée à usurper l’identité de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-166">**Decision set by**: Shows who determined if the sending infrastructure is allowed to spoof the user:</span></span>

       - <span data-ttu-id="cb5ea-167">**Stratégie d’intelligence infalsifiable** (automatique)</span><span class="sxs-lookup"><span data-stu-id="cb5ea-167">**Spoof intelligence policy** (automatic)</span></span>
       - <span data-ttu-id="cb5ea-168">**Administrateur** (manuel)</span><span class="sxs-lookup"><span data-stu-id="cb5ea-168">**Admin** (manual)</span></span>

   - <span data-ttu-id="cb5ea-169">**Dernière**détection : dernière date à laquelle un message a été reçu de l’infrastructure d’envoi qui contient l’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-169">**Last seen**: The last date when a message was received from the sending infrastructure that contains the spoofed user.</span></span>

   - <span data-ttu-id="cb5ea-170">**Autorisé à usurper ?**: les valeurs que vous voyez ici sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-170">**Allowed to spoof?**: The values that you see here are:</span></span>

     - <span data-ttu-id="cb5ea-171">**Oui**: les messages provenant de la combinaison d’une infrastructure utilisateur et d’une infrastructure d’envoi usurpés sont autorisés et ne sont pas traités comme des messages falsifiés.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-171">**Yes**: Messages from the combination of spoofed user and sending infrastructure are allowed and not treated as spoofed email.</span></span>

     - <span data-ttu-id="cb5ea-172">**Non**: les messages provenant de la combinaison d’une infrastructure d’utilisateur et d’expéditeur usurpée sont marqués comme falsifiés.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-172">**No**: Messages from the combination of spoofed user and sending infrastructure are marked as spoofed.</span></span> <span data-ttu-id="cb5ea-173">L’action est contrôlée par la stratégie anti-hameçonnage par défaut ou par des stratégies anti-hameçonnage personnalisées ATP (la valeur par défaut est **déplacer le message vers le dossier courrier indésirable**).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-173">The action is controlled by the default anti-phishing policy or custom ATP anti-phishing policies (the default value is **Move message to Junk Email folder**).</span></span> <span data-ttu-id="cb5ea-174">Pour plus d’informations, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-174">See the next section for more information.</span></span>

     - <span data-ttu-id="cb5ea-175">**Certains utilisateurs** (**votre onglet domaines** uniquement) : une infrastructure d’envoi usurpe l’identité de plusieurs utilisateurs, où certains utilisateurs usurpés sont autorisés et d’autres non.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-175">**Some users** (**Your Domains** tab only): A sending infrastructure is spoofing multiple users, where some spoofed users are allowed and others are not.</span></span> <span data-ttu-id="cb5ea-176">Utilisez l’onglet **détaillé** pour afficher les adresses spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-176">Use the **Detailed** tab to see the specific addresses.</span></span>

6. <span data-ttu-id="cb5ea-177">Au bas de la page, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-177">At the bottom of the page, click **Save**.</span></span>

## <a name="use-powershell-to-manage-spoofed-senders"></a><span data-ttu-id="cb5ea-178">Utiliser PowerShell pour gérer les expéditeurs usurpés</span><span class="sxs-lookup"><span data-stu-id="cb5ea-178">Use PowerShell to manage spoofed senders</span></span>

<span data-ttu-id="cb5ea-179">Pour afficher les expéditeurs autorisés et bloqués dans l’intelligence des usurpations d’identité, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-179">To view allowed and blocked senders in spoof intelligence, use the following syntax:</span></span>

```powershell
Get-PhishFilterPolicy [-AllowedToSpoof <Yes | No | Partial>] [-ConfidenceLevel <Low | High>] [-DecisionBy <Admin | SpoofProtection>] [-Detailed] [-SpoofType <Internal | External>]
```

<span data-ttu-id="cb5ea-180">Cet exemple renvoie des informations détaillées sur tous les expéditeurs autorisés à usurper des utilisateurs dans vos domaines.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-180">This example returns detailed information about all senders that are allowed to spoof users in your domains.</span></span>

```powershell
Get-PhishFilterPolicy -AllowedToSpoof Yes -Detailed -SpoofType Internal
```

<span data-ttu-id="cb5ea-181">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-phishfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-181">For detailed syntax and parameter information, see [Get-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-phishfilterpolicy).</span></span>

<span data-ttu-id="cb5ea-182">Pour configurer les expéditeurs autorisés et bloqués dans l’intelligence des usurpations d’identité, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-182">To configure allowed and blocked senders in spoof intelligence, follow these steps:</span></span>

1. <span data-ttu-id="cb5ea-183">Capturez la liste actuelle des expéditeurs usurpés détectés en écrivant la sortie de la cmdlet **Get-PhishFilterPolicy** dans un fichier CSV :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-183">Capture the current list of detected spoofed senders by writing the output of the **Get-PhishFilterPolicy** cmdlet to a CSV file:</span></span>

   ```powershell
   Get-PhishFilterPolicy -Detailed | Export-CSV "C:\My Documents\Spoofed Senders.csv"
   ```

2. <span data-ttu-id="cb5ea-184">Modifiez le fichier CSV pour ajouter ou modifier les valeurs **SpoofedUser** (adresse de messagerie) et **AllowedToSpoof** (oui ou non).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-184">Edit the CSV file to add or modify the **SpoofedUser** (email address) and **AllowedToSpoof** (Yes or No) values.</span></span> <span data-ttu-id="cb5ea-185">Enregistrez le fichier, lisez le fichier, puis stockez le contenu en tant que variable nommée `$UpdateSpoofedSenders` :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-185">Save the file, read the file, and store the contents as a variable named `$UpdateSpoofedSenders`:</span></span>

   ```powershell
   $UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
   ```

3. <span data-ttu-id="cb5ea-186">Utilisez la `$UpdateSpoofedSenders` variable pour configurer la stratégie d’intelligence d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-186">Use the `$UpdateSpoofedSenders` variable to configure the spoof intelligence policy:</span></span>

   ```powershell
   Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
   ```

<span data-ttu-id="cb5ea-187">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-187">For detailed syntax and parameter information, see [Set-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy).</span></span>

## <a name="use-the-security--compliance-center-to-configure-spoof-intelligence"></a><span data-ttu-id="cb5ea-188">Utiliser le centre de sécurité & conformité pour configurer l’aide à l’usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="cb5ea-188">Use the Security & Compliance Center to configure spoof intelligence</span></span>

<span data-ttu-id="cb5ea-189">Les options de configuration de l’intelligence d’usurpation sont décrites dans la rubrique [usurpation Settings in anti-phishing Policies](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-189">The configuration options for spoof intelligence are described in [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="cb5ea-190">Vous pouvez configurer les paramètres d’aide à la décision d’usurpation d’identité dans la stratégie anti-hameçonnage par défaut, ainsi que dans les stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-190">You can configure spoof intelligence settings in the default anti-phishing policy, and also in custom policies.</span></span> <span data-ttu-id="cb5ea-191">Pour obtenir des instructions sur la base de votre abonnement, consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-191">For instructions based on your subscription, see one of the following topics:</span></span>

- <span data-ttu-id="cb5ea-192">[Configurez les stratégies anti-hameçonnage dans EOP](configure-anti-phishing-policies-eop.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-192">[Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

- <span data-ttu-id="cb5ea-193">[Configurez les stratégies anti-hameçonnage ATP dans Microsoft 365](configure-atp-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-193">[Configure ATP anti-phishing policies in Microsoft 365](configure-atp-anti-phishing-policies.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="cb5ea-194">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="cb5ea-194">How do you know these procedures worked?</span></span>

<span data-ttu-id="cb5ea-195">Pour vérifier que vous avez configuré l’intelligence des usurpations d’identité avec des expéditeurs autorisés et non autorisés à usurper, et que vous avez configuré les paramètres d’aide à la décision, suivez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-195">To verify that you've configured spoof intelligence with senders who are allowed and not allowed to spoof, and that you've configured the spoof intelligence settings, use any of the following steps:</span></span>

- <span data-ttu-id="cb5ea-196">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **protection contre les menaces-courrier indésirable** \> développer la **stratégie d’intelligence frauduleux** \> : sélectionner Afficher les **expéditeurs que j’ai déjà consultés** \> Sélectionnez l’onglet **domaines** ou **domaines externes** , et vérifier la valeur **autorisé à usurper ?** pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-196">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-spam** \> expand **Spoof intelligence policy** \> select **Show me senders I already reviewed** \> select the **Your Domains** or **External Domains** tab, and verify the **Allowed to spoof?** value for the sender.</span></span>

- <span data-ttu-id="cb5ea-197">Dans PowerShell, exécutez les commandes suivantes pour afficher les expéditeurs autorisés et non autorisés à usurper les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-197">In PowerShell, run the following commands to view the senders who are allowed and not allowed to spoof:</span></span>

  ```powershell
  Get-PhishFilterPolicy -AllowedToSpoof Yes -SpoofType Internal
  Get-PhishFilterPolicy -AllowedToSpoof No -SpoofType Internal
  Get-PhishFilterPolicy -AllowedToSpoof Yes -SpoofType External
  Get-PhishFilterPolicy -AllowedToSpoof No -SpoofType External
  ```

- <span data-ttu-id="cb5ea-198">Dans PowerShell, exécutez la commande suivante pour exporter la liste de tous les expéditeurs usurpés vers un fichier CSV :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-198">In PowerShell, run the following command to export the list of all spoofed senders to a CSV file:</span></span>

   ```powershell
   Get-PhishFilterPolicy -Detailed | Export-CSV "C:\My Documents\Spoofed Senders.csv"
   ```

- <span data-ttu-id="cb5ea-199">Dans le centre de sécurité & conformité, accédez à anti-hameçonnage de la stratégie de **gestion des menaces** \> **Policy** \> **Anti-phishing** et effectuez l’une des opérations suivantes : **ATP anti-phishing**  </span><span class="sxs-lookup"><span data-stu-id="cb5ea-199">In the Security & Compliance Center, go to **Threat management** \> **Policy**  \> **Anti-phishing**  or **ATP anti-phishing**, and do either of the following steps:</span></span>

  - <span data-ttu-id="cb5ea-200">Sélectionnez une stratégie dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-200">Select a policy from the list.</span></span> <span data-ttu-id="cb5ea-201">Dans le menu volant qui s’affiche, vérifiez les valeurs de la section **usurpation** .</span><span class="sxs-lookup"><span data-stu-id="cb5ea-201">In the flyout that appears, verify the values in the **Spoof** section.</span></span>
  - <span data-ttu-id="cb5ea-202">Cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-202">Click **Default policy**.</span></span> <span data-ttu-id="cb5ea-203">Dans le menu volant qui s’affiche, vérifiez les valeurs de la section **usurpation** .</span><span class="sxs-lookup"><span data-stu-id="cb5ea-203">In the flyout that appears, verify the values in the **Spoof** section.</span></span>

- <span data-ttu-id="cb5ea-204">Dans Exchange Online PowerShell, remplacez par \<Name\> la valeur par défaut Office 365 antiphishing ou par le nom d’une stratégie personnalisée, puis exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-204">In Exchange Online PowerShell, replace \<Name\> with Office365 AntiPhish Default or the name of a custom policy, and run the following command to verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>" | Format-List EnableAntiSpoofEnforcement,EnableUnauthenticatedSender,AuthenticationFailAction
  ```

## <a name="other-ways-to-manage-spoofing-and-phishing"></a><span data-ttu-id="cb5ea-205">Autres façons de gérer l’usurpation d’identité et le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="cb5ea-205">Other ways to manage spoofing and phishing</span></span>

<span data-ttu-id="cb5ea-206">Soyez très à la protection contre l’usurpation d’identité et la protection antiphishing.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-206">Be diligent about spoofing and phishing protection.</span></span> <span data-ttu-id="cb5ea-207">Voici des méthodes relatives pour vérifier les expéditeurs qui usurpent votre domaine et les empêcher d’endommager votre organisation :</span><span class="sxs-lookup"><span data-stu-id="cb5ea-207">Here are related ways to check on senders spoofing your domain and help prevent them from damaging your organization:</span></span>

- <span data-ttu-id="cb5ea-208">Vérifiez le **rapport de courrier infalsifiable**.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-208">Check the **Spoof Mail Report**.</span></span> <span data-ttu-id="cb5ea-209">Vous pouvez utiliser ce rapport fréquemment pour afficher et gérer les expéditeurs usurpés.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-209">You can use this report often to view and help manage spoofed senders.</span></span> <span data-ttu-id="cb5ea-210">Pour plus d’informations, reportez-vous à la rubrique [Subdetections Report](view-email-security-reports.md#spoof-detections-report).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-210">For information, see [Spoof Detections report](view-email-security-reports.md#spoof-detections-report).</span></span>

- <span data-ttu-id="cb5ea-211">Passez en revue votre configuration SPF (Sender Policy Framework).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-211">Review your Sender Policy Framework (SPF) configuration.</span></span> <span data-ttu-id="cb5ea-212">Pour consulter une brève présentation de SPF et le configurer rapidement, voir [Configurer SPF dans Microsoft 365 pour empêcher l’usurpation d’identité](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-212">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Microsoft 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="cb5ea-213">Pour consulter des informations plus approfondies sur l’utilisation de SPF par Office 365, la résolution des problèmes et les déploiements non standard tels que les déploiements hybrides, voir Comment Office 365 utilise SPF (Sender Policy Framework) pour empêcher l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-213">For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span>

- <span data-ttu-id="cb5ea-214">Passez en revue votre configuration DKIM (DomainKeys Identified Identified Mail).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-214">Review your DomainKeys Identified Mail (DKIM) configuration.</span></span> <span data-ttu-id="cb5ea-215">Vous devez utiliser DKIM en plus de SPF et de DMARC pour empêcher les agresseurs d’envoyer des messages qui semblent provenir de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-215">You should use DKIM in addition to SPF and DMARC to help prevent attackers from sending messages that look like they are coming from your domain.</span></span> <span data-ttu-id="cb5ea-216">DKIM vous permet d'ajouter une signature numérique aux messages électroniques dans l'en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-216">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="cb5ea-217">Pour plus d’informations, consultez [la rubrique use DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-217">For information, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

- <span data-ttu-id="cb5ea-218">Passez en revue votre configuration d’authentification de message basée sur un domaine, de création de rapports et de conformité (DMARC).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-218">Review your Domain-based Message Authentication, Reporting, and Conformance (DMARC) configuration.</span></span> <span data-ttu-id="cb5ea-219">L’implémentation de DMARC avec SPF et DKIM fournit une protection supplémentaire contre l’usurpation et les courriers de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-219">Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email.</span></span> <span data-ttu-id="cb5ea-220">DMARC permet aux systèmes de messagerie de réception de déterminer ce qu’ils doivent faire des messages envoyés à partir de votre domaine qui sont rejetés par les contrôles de SPF ou de DKIM.</span><span class="sxs-lookup"><span data-stu-id="cb5ea-220">DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span> <span data-ttu-id="cb5ea-221">Pour plus d’informations, consultez la rubrique [utiliser DMARC pour valider le courrier électronique dans Office 365](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ea-221">For information, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>
