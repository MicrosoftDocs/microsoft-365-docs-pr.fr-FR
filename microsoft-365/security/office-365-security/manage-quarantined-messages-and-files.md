---
title: Gérer les fichiers et les messages mis en quarantaine en tant qu’administrateur
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent découvrir comment afficher et gérer les messages mis en quarantaine pour tous les utilisateurs dans Exchange Online Protection (EOP). Les administrateurs des organisations avec Microsoft Defender pour Office 365 peuvent également gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive Entreprise et Microsoft Teams.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: b0515d610b38986c2b5339c1cb967a7b150914a2
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50405817"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-eop"></a><span data-ttu-id="61700-104">Gérer les messages et fichiers mis en quarantaine en tant qu’administrateur dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="61700-104">Manage quarantined messages and files as an admin in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="61700-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="61700-105">**Applies to**</span></span>
- [<span data-ttu-id="61700-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="61700-106">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="61700-107">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="61700-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="61700-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="61700-108">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="61700-109">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="61700-109">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="61700-110">Pour plus d’informations, voir [Messages électroniques mis en quarantaine dans EOP.](quarantine-email-messages.md)</span><span class="sxs-lookup"><span data-stu-id="61700-110">For more information, see [Quarantined email messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="61700-111">Les administrateurs peuvent afficher, libérer et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="61700-111">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="61700-112">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, hameçonnage à haut niveau de confiance ou suite à des règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="61700-112">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="61700-113">Les administrateurs peuvent également signaler des faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61700-113">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="61700-114">Les administrateurs des organisations avec Microsoft Defender pour Office 365 peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive Entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="61700-114">Admins in organizations with Microsoft Defender for Office 365 can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="61700-115">Vous affichez et gérez les messages mis en quarantaine dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="61700-115">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="61700-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="61700-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="61700-117">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="61700-117">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="61700-118">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="61700-118">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="61700-119">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="61700-119">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="61700-120">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="61700-120">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="61700-121">Des autorisations doivent vous être attribuées dans **Exchange Online** avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="61700-121">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="61700-122">Pour prendre des mesures sur les messages mis en quarantaine pour tous les  utilisateurs, vous devez être membre des groupes de rôles Gestion de l’organisation, Administrateur de la sécurité ou Administrateur de la mise en <sup>\*</sup> quarantaine.</span><span class="sxs-lookup"><span data-stu-id="61700-122">To take action on quarantined messages for all users, you need to be a member of the **Organization Management**, **Security Administrator**, or **Quarantine Administrator**<sup>\*</sup> role groups.</span></span>
  - <span data-ttu-id="61700-123">Pour accéder en lecture seule aux messages mis en quarantaine pour  tous  les utilisateurs, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="61700-123">For read-only access to quarantined messages for all users, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="61700-124">Pour plus d'informations, voir [Permissions en échange en ligne](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="61700-124">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="61700-125">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="61700-125">**Notes**:</span></span>

  - <span data-ttu-id="61700-126">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux _utilisateurs_ les autorisations et autorisations requises pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="61700-126">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="61700-127">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="61700-127">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="61700-128">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="61700-128">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>
  - <span data-ttu-id="61700-129"><sup>\*</sup>Les membres du **groupe** de rôles Administrateur  de quarantaine doivent également être membres du groupe de rôles Gestion de l’hygiène dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) pour pouvoir mettre en quarantaine les procédures dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61700-129"><sup>\*</sup> Members of the **Quarantine Administrator** role group also need to be members of the **Hygiene Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) in order to do quarantine procedures in Exchange Online PowerShell.</span></span>

- <span data-ttu-id="61700-130">Les messages mis en quarantaine sont conservés pendant une période par défaut avant d’être automatiquement supprimés :</span><span class="sxs-lookup"><span data-stu-id="61700-130">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>
  - <span data-ttu-id="61700-131">30 jours pour les messages mis en quarantaine par des stratégies anti-courrier indésirable (courrier indésirable, hameçonnage et courrier électronique en masse).</span><span class="sxs-lookup"><span data-stu-id="61700-131">30 days for messages quarantined by anti-spam policies (spam, phishing, and bulk email).</span></span> <span data-ttu-id="61700-132">Il s’agit de la valeur par défaut et de la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="61700-132">This is the default and maximum value.</span></span> <span data-ttu-id="61700-133">Pour configurer (plus bas) cette valeur, voir [Configurer des stratégies anti-courrier indésirable.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="61700-133">To configure (lower) this value, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>
  - <span data-ttu-id="61700-134">15 jours pour les messages contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="61700-134">15 days for messages that contain malware.</span></span>
  - <span data-ttu-id="61700-135">15 jours pour les fichiers mis en quarantaine par pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams dans Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="61700-135">15 days for files quarantined by Safe Attachments for SharePoint, OneDrive, and Microsoft Teams in Defender for Office 365.</span></span>

  <span data-ttu-id="61700-136">Lorsqu’un message arrive à expiration de la quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="61700-136">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="61700-137">Utiliser le Centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-137">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="61700-138">Afficher les e-mails mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-138">View quarantined email</span></span>

1. <span data-ttu-id="61700-139">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="61700-139">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="61700-140">Vérifiez que l’option **Afficher les mis en quarantaine** est définie sur la valeur par défaut de **messagerie**.</span><span class="sxs-lookup"><span data-stu-id="61700-140">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="61700-141">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="61700-141">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="61700-142">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="61700-142">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="61700-143">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="61700-143">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="61700-144">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-144">**Received**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-145">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-145">**Sender**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-146">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-146">**Subject**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-147">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-147">**Quarantine reason**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-148">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-148">**Released?**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-149">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-149">**Policy type**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-150">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="61700-150">**Expires**</span></span>
   - <span data-ttu-id="61700-151">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="61700-151">**Recipient**</span></span>
   - <span data-ttu-id="61700-152">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="61700-152">**Message ID**</span></span>
   - <span data-ttu-id="61700-153">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="61700-153">**Policy name**</span></span>
   - <span data-ttu-id="61700-154">**Taille**</span><span class="sxs-lookup"><span data-stu-id="61700-154">**Size**</span></span>
   - <span data-ttu-id="61700-155">**Direction**</span><span class="sxs-lookup"><span data-stu-id="61700-155">**Direction**</span></span>

   <span data-ttu-id="61700-156">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="61700-156">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="61700-157">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="61700-157">To filter the results, click **Filter**.</span></span> <span data-ttu-id="61700-158">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="61700-158">The available filters are:</span></span>

   - <span data-ttu-id="61700-159">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="61700-159">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>
     - <span data-ttu-id="61700-160">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="61700-160">**Today**</span></span>
     - <span data-ttu-id="61700-161">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="61700-161">**Next 2 days**</span></span>
     - <span data-ttu-id="61700-162">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="61700-162">**Next 7 days**</span></span>
     - <span data-ttu-id="61700-163">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="61700-163">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="61700-164">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="61700-164">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="61700-165">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="61700-165">**Quarantine reason**:</span></span>
     - <span data-ttu-id="61700-166">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="61700-166">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>
     - <span data-ttu-id="61700-167">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="61700-167">**Bulk**</span></span>
     - <span data-ttu-id="61700-168">**Hameçonnage**: le  verdict de filtrage du courrier indésirable était le courrier électronique de hameçonnage ou la protection anti-hameçonnage qui a mis en quarantaine le message [(paramètres](set-up-anti-phishing-policies.md#spoof-settings) d’usurpation d’identité ou protection contre [l’usurpation d’identité).](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="61700-168">**Phish**: The spam filter verdict was **Phishing email** or anti-phishing protection quarantined the message ([spoof settings](set-up-anti-phishing-policies.md#spoof-settings) or [impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)).</span></span>
     - <span data-ttu-id="61700-169">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="61700-169">**Malware**</span></span>
     - <span data-ttu-id="61700-170">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="61700-170">**Spam**</span></span>
     - <span data-ttu-id="61700-171">**Hameçonnage à haut niveau de confiance**</span><span class="sxs-lookup"><span data-stu-id="61700-171">**High Confidence Phish**</span></span>

   - <span data-ttu-id="61700-172">**Type de stratégie** : filtrer les messages par type de stratégie :</span><span class="sxs-lookup"><span data-stu-id="61700-172">**Policy Type**: Filter messages by policy type:</span></span>
     - <span data-ttu-id="61700-173">**Stratégie anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="61700-173">**Anti-malware policy**</span></span>
     - <span data-ttu-id="61700-174">**Stratégie de pièces jointes sécurisées**</span><span class="sxs-lookup"><span data-stu-id="61700-174">**Safe Attachments policy**</span></span>
     - <span data-ttu-id="61700-175">**Stratégie anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="61700-175">**Anti-phish policy**</span></span>
     - <span data-ttu-id="61700-176">**Stratégie de filtrage de contenu hébergé** (stratégie anti-courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="61700-176">**Hosted content filter policy** (anti-spam policy)</span></span>
     - <span data-ttu-id="61700-177">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="61700-177">**Transport rule**</span></span>

   - <span data-ttu-id="61700-178">**Destinataire du message électronique**: tous les utilisateurs ou uniquement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="61700-178">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="61700-179">Les utilisateurs finaux peuvent uniquement gérer les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="61700-179">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="61700-180">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="61700-180">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="61700-181">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="61700-181">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="61700-182">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="61700-182">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="61700-183">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="61700-183">Wildcards aren't supported.</span></span> <span data-ttu-id="61700-184">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-184">You can search by the following values:</span></span>

   - <span data-ttu-id="61700-185">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="61700-185">**Message ID**: The globally unique identifier of the message.</span></span>

     <span data-ttu-id="61700-186">Par exemple, [](message-trace-scc.md) vous avez utilisé le suivi des messages pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="61700-186">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="61700-187">Assurez-vous d’inclure la valeur complète de l’ID du message, qui peut inclure des crochets ( \<\> ).</span><span class="sxs-lookup"><span data-stu-id="61700-187">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="61700-188">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="61700-188">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="61700-189">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="61700-189">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="61700-190">**Nom de la stratégie** : utilisez le nom de stratégie complet indiqué dans le message.</span><span class="sxs-lookup"><span data-stu-id="61700-190">**Policy name**: Use the entire policy name of the message.</span></span> <span data-ttu-id="61700-191">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="61700-191">The search is not case-sensitive.</span></span>

   - <span data-ttu-id="61700-192">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="61700-192">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="61700-193">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="61700-193">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="61700-194">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="61700-194">The search is not case-sensitive.</span></span>

   - <span data-ttu-id="61700-195">**Nom de** la stratégie : nom de la stratégie responsable de la mise en quarantaine du message.</span><span class="sxs-lookup"><span data-stu-id="61700-195">**Policy name**: The name of the policy that was responsible for quarantining the message.</span></span>

   <span data-ttu-id="61700-196">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="61700-196">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="61700-197">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="61700-197">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="61700-198">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-198">View quarantined message details</span></span>

<span data-ttu-id="61700-199">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="61700-199">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="61700-200">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="61700-200">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="61700-201">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="61700-201">**Sender address**</span></span>

- <span data-ttu-id="61700-202">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="61700-202">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="61700-203">**Subject**</span><span class="sxs-lookup"><span data-stu-id="61700-203">**Subject**</span></span>

- <span data-ttu-id="61700-204">**Raison de la** mise en quarantaine : indique si un message a été identifié comme courrier **indésirable,** en **bloc,** **hameçonnage,** correspond à une règle de flux de messagerie ( règle de **transport**), ou a été identifié comme contenant un programme **malveillant**.</span><span class="sxs-lookup"><span data-stu-id="61700-204">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="61700-205">**Nombre de destinataires**</span><span class="sxs-lookup"><span data-stu-id="61700-205">**Recipient count**</span></span>

- <span data-ttu-id="61700-206">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="61700-206">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="61700-207">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="61700-207">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="61700-208">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="61700-208">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="61700-209">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="61700-209">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="61700-210">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-210">Take action on quarantined email</span></span>

<span data-ttu-id="61700-211">Une fois que vous avez sélectionné un message, plusieurs options s’offrent à vous pour ce qu’il faut faire avec les messages dans le volet volant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="61700-211">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="61700-212">**Message de publication**: dans le volet volant qui s’affiche, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-212">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="61700-213">**Signaler les messages à Microsoft pour** analyse : cette option est sélectionnée par défaut et signale le message mis en quarantaine par erreur à Microsoft comme faux positif.</span><span class="sxs-lookup"><span data-stu-id="61700-213">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="61700-214">Si le message a été mis en quarantaine en tant que courrier indésirable, en bloc, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61700-214">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="61700-215">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="61700-215">Depending on their analysis, the service-wide spam filter rules might be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="61700-216">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-216">Choose one of the following options:</span></span>
    - <span data-ttu-id="61700-217">**Envoyer des messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="61700-217">**Release messages to all recipients**</span></span>
    - <span data-ttu-id="61700-218">**Envoyer des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="61700-218">**Release messages to specific recipients**</span></span>
    - <span data-ttu-id="61700-219">**Diffuser des messages à d’autres** personnes : notez que la libération de messages de programmes malveillants à des personnes autres que des destinataires d’origine n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61700-219">**Release messages to other people**: Note that releasing malware messages to people other than original recipients is not supported.</span></span>

  <span data-ttu-id="61700-220">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="61700-220">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="61700-221">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="61700-221">Notes about releasing messages:</span></span>

  - <span data-ttu-id="61700-222">Vous ne pouvez pas envoyer un message au même destinataire plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="61700-222">You can't release a message to the same recipient more than once.</span></span>
  - <span data-ttu-id="61700-223">Seuls les destinataires qui n’ont pas reçu le message apparaissent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="61700-223">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="61700-224">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="61700-224">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="61700-225">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="61700-225">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="61700-226">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="61700-226">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="61700-227">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-227">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="61700-228">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="61700-228">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  - <span data-ttu-id="61700-229">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="61700-229">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="61700-230">**Supprimer de la quarantaine**: une fois que vous avez cliqué sur **Oui** dans l’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="61700-230">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="61700-231">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="61700-231">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="61700-232">**Envoyer un message**: dans le volet volant qui s’affiche, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-232">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="61700-233">**Type d’objet**: **e-mail** (par **défaut), URL** ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="61700-233">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="61700-234">**Format de** soumission : **ID de message** réseau (par défaut, avec la valeur correspondante dans la zone **ID** de message réseau) ou fichier **(accédez** à un fichier .eml ou .msg local).</span><span class="sxs-lookup"><span data-stu-id="61700-234">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="61700-235">Notez que si vous sélectionnez **Fichier,** puis **ID de message** réseau, la valeur initiale a disparu.</span><span class="sxs-lookup"><span data-stu-id="61700-235">Note that if you select **File** and then select **Network Message ID**, the initial value is gone.</span></span>

  - <span data-ttu-id="61700-236">**Destinataires :** tapez au moment du bail un destinataire d’origine du message, ou cliquez sur **Sélectionner** tout pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="61700-236">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="61700-237">Vous pouvez également cliquer sur **Sélectionner tout,** puis supprimer de manière sélective des destinataires individuels.</span><span class="sxs-lookup"><span data-stu-id="61700-237">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="61700-238">**Raison de l’envoi** **: ne doit pas avoir été bloqué** (par défaut) ou doit avoir été **bloqué**.</span><span class="sxs-lookup"><span data-stu-id="61700-238">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="61700-239">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="61700-239">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="61700-240">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="61700-240">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="61700-241">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-241">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="61700-242">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-242">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="61700-243">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="61700-243">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="61700-244">Envisagez le scénario suivant : john@gmail.com envoie un message à faith@contoso.com et john@subsidiary.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="61700-244">Consider the following scenario: john@gmail.com sends a message to faith@contoso.com and john@subsidiary.contoso.com.</span></span> <span data-ttu-id="61700-245">Gmail bifurme ce message en deux copies qui sont toutes deux acheminées vers la quarantaine en tant que hameçonnage dans Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61700-245">Gmail bifurcates this message into two copies that are both routed to quarantine as phishing in Microsoft.</span></span> <span data-ttu-id="61700-246">Un administrateur publie ces deux messages admin@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="61700-246">An admin releases both of these messages to admin@contoso.com.</span></span> <span data-ttu-id="61700-247">Le premier message publié qui atteint la boîte aux lettres d’administration est remis.</span><span class="sxs-lookup"><span data-stu-id="61700-247">The first released message that reaches the admin mailbox is delivered.</span></span> <span data-ttu-id="61700-248">Le deuxième message publié est identifié comme remise en double et est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61700-248">The second released message is identified as duplicate delivery and is skipped.</span></span> <span data-ttu-id="61700-249">Les messages sont identifiés comme doublons s’ils ont le même ID de message et le même temps de réception.</span><span class="sxs-lookup"><span data-stu-id="61700-249">Message are identified as duplicates if they have the same message ID and received time.</span></span>

- <span data-ttu-id="61700-250">**Supprimer des messages**: après avoir cliqué sur **Oui** dans l’avertissement qui s’affiche, les messages sont immédiatement supprimés sans être envoyés aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="61700-250">**Delete messages**:  After you click **Yes** in the warning that appears, the messages are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="61700-251">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="61700-251">When you're finished, click **Close**.</span></span>

## <a name="microsoft-defender-for-office-365-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="61700-252">Microsoft Defender pour Office 365 uniquement : utiliser le Centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-252">Microsoft Defender for Office 365 Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="61700-253">Les procédures pour les fichiers mis en quarantaine dans cette section sont disponibles uniquement pour les abonnés à Microsoft Defender pour Office 365 Plan 1 et Plan 2.</span><span class="sxs-lookup"><span data-stu-id="61700-253">The procedures for quarantined files in this section are available only to Microsoft Defender for Office 365 Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="61700-254">Dans les organisations avec Defender pour Office 365, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive Entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="61700-254">In organizations with Defender for Office 365, admins can manage quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span> <span data-ttu-id="61700-255">Pour activer la protection de ces fichiers, voir Activer les [pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.](turn-on-atp-for-spo-odb-and-teams.md)</span><span class="sxs-lookup"><span data-stu-id="61700-255">To enable protection for these files, see [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="61700-256">Afficher les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-256">View quarantined files</span></span>

1. <span data-ttu-id="61700-257">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="61700-257">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="61700-258">Modifier **l’affichage mis en quarantaine** dans les fichiers de **valeurs.**</span><span class="sxs-lookup"><span data-stu-id="61700-258">Change **View quarantined** to the value **files**.</span></span> <span data-ttu-id="61700-259">Vous pouvez trier un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="61700-259">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="61700-260">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="61700-260">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="61700-261">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="61700-261">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="61700-262">Les colonnes par défaut sont marquées d’un astérisque ( <sup>\*</sup> :</span><span class="sxs-lookup"><span data-stu-id="61700-262">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="61700-263">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-263">**User**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-264">**Emplacement**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-264">**Location**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-265">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-265">**File name**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-266">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-266">**File URL**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-267">**Taille du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-267">**File Size**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-268">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-268">**Expires**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-269">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="61700-269">**Released?**<sup>\*</sup></span></span>
   - <span data-ttu-id="61700-270">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="61700-270">**Detected by**</span></span>
   - <span data-ttu-id="61700-271">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="61700-271">**Modified by time**</span></span>

4. <span data-ttu-id="61700-272">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="61700-272">To filter the results, click **Filter**.</span></span> <span data-ttu-id="61700-273">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="61700-273">The available filters are:</span></span>

   - <span data-ttu-id="61700-274">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="61700-274">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>
     - <span data-ttu-id="61700-275">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="61700-275">**Today**</span></span>
     - <span data-ttu-id="61700-276">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="61700-276">**Next 2 days**</span></span>
     - <span data-ttu-id="61700-277">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="61700-277">**Next 7 days**</span></span>
     - <span data-ttu-id="61700-278">Plage de date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="61700-278">A custom date/time range.</span></span>
   - <span data-ttu-id="61700-279">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="61700-279">**Received time**</span></span>
   - <span data-ttu-id="61700-280">**Raison de la mise** en quarantaine : la seule valeur disponible est **Programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="61700-280">**Quarantine reason**: The only available value is **Malware**.</span></span>
   - <span data-ttu-id="61700-281">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="61700-281">**Policy type**</span></span>

<span data-ttu-id="61700-282">Une fois que vous avez trouvé un fichier spécifique mis en quarantaine, sélectionnez-le pour afficher les détails à son sujet et pour agir dessus (par exemple, afficher, libérer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="61700-282">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="61700-283">Afficher les détails du fichier mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-283">View quarantined file details</span></span>

<span data-ttu-id="61700-284">Lorsque vous sélectionnez un fichier dans la liste, les détails suivants apparaissent dans le volet volant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="61700-284">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="61700-285">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="61700-285">**File Name**</span></span>
- <span data-ttu-id="61700-286">**URL du** fichier : URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="61700-286">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>
- <span data-ttu-id="61700-287">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="61700-287">**Malicious content detected on** The date/time the file was quarantined.</span></span>
- <span data-ttu-id="61700-288">**Expire :** date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="61700-288">**Expires**: The date when the file will be deleted from quarantine.</span></span>
- <span data-ttu-id="61700-289">**Détecté par**: Defender pour Office 365 ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61700-289">**Detected By**: Defender for Office 365 or Microsoft's anti-malware engine.</span></span>
- <span data-ttu-id="61700-290">**Déplacer ?**</span><span class="sxs-lookup"><span data-stu-id="61700-290">**Released?**</span></span>
- <span data-ttu-id="61700-291">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="61700-291">**Malware Name**</span></span>
- <span data-ttu-id="61700-292">**ID de document**: identificateur unique du document.</span><span class="sxs-lookup"><span data-stu-id="61700-292">**Document ID**: A unique identifier for the document.</span></span>
- <span data-ttu-id="61700-293">**Taille du** fichier : en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="61700-293">**File Size**: In kilobytes (KB).</span></span>
- <span data-ttu-id="61700-294">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="61700-294">**Organization** Your organization's unique ID.</span></span>
- <span data-ttu-id="61700-295">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="61700-295">**Last modified**</span></span>
- <span data-ttu-id="61700-296">**Modifié par**: l’utilisateur qui a modifié le fichier en dernier.</span><span class="sxs-lookup"><span data-stu-id="61700-296">**Modified By**: The user who last modified the file.</span></span>
- <span data-ttu-id="61700-297">**Valeur SHA-256 bits (Secure Hash Algorithm)**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou à d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="61700-297">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="61700-298">Prendre des mesures sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-298">Take action on quarantined files</span></span>

<span data-ttu-id="61700-299">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez prendre les mesures suivantes sur le fichier dans le volet volant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="61700-299">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="61700-300">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis,** and then click **Release files**.</span><span class="sxs-lookup"><span data-stu-id="61700-300">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>
- <span data-ttu-id="61700-301">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="61700-301">**Download file**</span></span>
- <span data-ttu-id="61700-302">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="61700-302">**Remove file from quarantine**</span></span>

<span data-ttu-id="61700-303">Si vous ne les relâchez pas ou ne les supprimez pas, ils seront supprimés à l’expiration de la période de rétention de mise en quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="61700-303">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="61700-304">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-304">Actions on multiple quarantined files</span></span>

<span data-ttu-id="61700-305">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet volant **Actions** en bloc s’affiche où vous pouvez prendre les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="61700-305">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="61700-306">**Libérer des fichiers**</span><span class="sxs-lookup"><span data-stu-id="61700-306">**Release files**</span></span>
- <span data-ttu-id="61700-307">**Supprimer des fichiers**: une fois que vous avez cliqué sur **Oui** dans l’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="61700-307">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="61700-308">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour afficher et gérer les messages et fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="61700-308">Use Exchange Online PowerShell or standalone EOP PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="61700-309">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont :</span><span class="sxs-lookup"><span data-stu-id="61700-309">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="61700-310">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="61700-310">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/delete-quarantinemessage)

- [<span data-ttu-id="61700-311">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="61700-311">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/export-quarantinemessage)

- [<span data-ttu-id="61700-312">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="61700-312">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage)

- <span data-ttu-id="61700-313">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/preview-quarantinemessage): notez que cette cmdlet est uniquement pour les messages, et non pour les fichiers de programmes malveillants provenant de pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="61700-313">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span>

- [<span data-ttu-id="61700-314">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="61700-314">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage)
