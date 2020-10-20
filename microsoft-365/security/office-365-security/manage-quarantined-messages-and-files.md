---
title: Gérer les fichiers et les messages mis en quarantaine en tant qu’administrateur
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
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
description: Les administrateurs peuvent apprendre à afficher et à gérer les messages mis en quarantaine pour tous les utilisateurs dans Exchange Online Protection (EOP). Les administrateurs dans les organisations avec Office 365 Advanced Threat Protection (Office 365 ATP) peuvent également gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.
ms.openlocfilehash: 5e1115157ef7d67bc7a3f626eb61d01ecc0986cb
ms.sourcegitcommit: 153f413402f93b79be421741f3b9fed318d6d270
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48600540"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-eop"></a><span data-ttu-id="77a22-104">Gérer les messages et fichiers mis en quarantaine en tant qu’administrateur dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="77a22-104">Manage quarantined messages and files as an admin in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="77a22-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="77a22-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="77a22-106">Pour plus d’informations, consultez la rubrique [messages électroniques mis en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="77a22-106">For more information, see [Quarantined email messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="77a22-107">Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="77a22-107">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="77a22-108">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="77a22-108">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="77a22-109">Les administrateurs peuvent également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77a22-109">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="77a22-110">Les administrateurs dans les organisations disposant d’Office 365 Advanced Threat Protection (Office 365 ATP) peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="77a22-110">Admins in organizations with Office 365 Advance Threat Protection (Office 365 ATP) can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="77a22-111">Vous pouvez afficher et gérer les messages mis en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="77a22-111">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="77a22-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="77a22-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="77a22-113">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="77a22-113">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="77a22-114">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="77a22-114">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="77a22-115">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="77a22-115">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="77a22-116">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="77a22-116">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="77a22-117">Vous devez disposer d’autorisations pour pouvoir gérer la mise en quarantaine en tant qu’administrateur. Les autorisations sont contrôlées par le rôle de **mise en quarantaine** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="77a22-117">You need to be assigned permissions before you can manage the quarantine as an admin. The permissions are controlled by the **Quarantine** role in the Security & Compliance Center.</span></span> <span data-ttu-id="77a22-118">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l' **organisation** (administrateurs globaux), administrateur de **mise en quarantaine**et administrateur de **sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="77a22-118">By default, this role is assigned to the **Organization Management** (Global admins), **Quarantine Administrator**, and **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="77a22-119">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="77a22-119">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="77a22-120">Les messages mis en quarantaine sont conservés pendant une période de temps par défaut avant d’être supprimés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="77a22-120">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>

  - <span data-ttu-id="77a22-121">Messages mis en quarantaine par des stratégies de blocage du courrier indésirable (courrier indésirable, hameçonnage et courrier en masse) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="77a22-121">Messages quarantined by anti-spam policies (spam, phishing, and bulk email): 30 days.</span></span> <span data-ttu-id="77a22-122">Il s’agit de la valeur par défaut et la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="77a22-122">This is the default and maximum value.</span></span> <span data-ttu-id="77a22-123">Pour configurer cette valeur, reportez-vous à la rubrique [configurer des stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="77a22-123">To configure this value, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

  - <span data-ttu-id="77a22-124">Messages contenant des programmes malveillants : 15 jours.</span><span class="sxs-lookup"><span data-stu-id="77a22-124">Messages that contain malware: 15 days.</span></span>

  <span data-ttu-id="77a22-125">Lorsqu’un message arrive à expiration en quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="77a22-125">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="77a22-126">Utiliser le centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-126">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="77a22-127">Afficher le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-127">View quarantined email</span></span>

1. <span data-ttu-id="77a22-128">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="77a22-128">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="77a22-129">Vérifiez que l’option **Afficher les mis en quarantaine** est définie sur la valeur par défaut de **messagerie**.</span><span class="sxs-lookup"><span data-stu-id="77a22-129">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="77a22-130">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="77a22-130">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="77a22-131">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="77a22-131">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="77a22-132">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="77a22-132">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="77a22-133">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-133">**Received**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-134">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-134">**Sender**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-135">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-135">**Subject**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-136">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-136">**Quarantine reason**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-137">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-137">**Released?**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-138">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-138">**Policy type**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-139">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="77a22-139">**Recipient**</span></span>
   - <span data-ttu-id="77a22-140">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="77a22-140">**Message ID**</span></span>
   - <span data-ttu-id="77a22-141">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="77a22-141">**Policy name**</span></span>
   - <span data-ttu-id="77a22-142">**Taille**</span><span class="sxs-lookup"><span data-stu-id="77a22-142">**Size**</span></span>
   - <span data-ttu-id="77a22-143">**Direction**</span><span class="sxs-lookup"><span data-stu-id="77a22-143">**Direction**</span></span>

   <span data-ttu-id="77a22-144">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="77a22-144">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="77a22-145">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-145">To filter the results, click **Filter**.</span></span> <span data-ttu-id="77a22-146">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="77a22-146">The available filters are:</span></span>

   - <span data-ttu-id="77a22-147">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="77a22-147">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>
     - <span data-ttu-id="77a22-148">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="77a22-148">**Today**</span></span>
     - <span data-ttu-id="77a22-149">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="77a22-149">**Next 2 days**</span></span>
     - <span data-ttu-id="77a22-150">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="77a22-150">**Next 7 days**</span></span>
     - <span data-ttu-id="77a22-151">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="77a22-151">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="77a22-152">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="77a22-152">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="77a22-153">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="77a22-153">**Quarantine reason**:</span></span>
     - <span data-ttu-id="77a22-154">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="77a22-154">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>
     - <span data-ttu-id="77a22-155">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="77a22-155">**Bulk**</span></span>
     - <span data-ttu-id="77a22-156">**Hameçonnage**: le verdict de filtrage du courrier indésirable était le message de **hameçonnage** ou la protection anti-hameçonnage a mis en quarantaine le message ([paramètres d’usurpation](set-up-anti-phishing-policies.md#spoof-settings) ou [protection contre](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies)l’usurpation d’identité).</span><span class="sxs-lookup"><span data-stu-id="77a22-156">**Phish**: The spam filter verdict was **Phishing email** or anti-phishing protection quarantined the message ([spoof settings](set-up-anti-phishing-policies.md#spoof-settings) or [impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies)).</span></span>
     - <span data-ttu-id="77a22-157">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="77a22-157">**Malware**</span></span>
     - <span data-ttu-id="77a22-158">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="77a22-158">**Spam**</span></span>
     - <span data-ttu-id="77a22-159">**Hameçonnage à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="77a22-159">**High Confidence Phish**</span></span>
     
   - <span data-ttu-id="77a22-160">**Type de stratégie**: filtrer les messages par type de stratégie :</span><span class="sxs-lookup"><span data-stu-id="77a22-160">**Policy Type**: Filter messages by policy type:</span></span>
     - <span data-ttu-id="77a22-161">**Stratégie anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="77a22-161">**Anti-malware policy**</span></span>
     - <span data-ttu-id="77a22-162">**Stratégie de pièces jointes fiables**</span><span class="sxs-lookup"><span data-stu-id="77a22-162">**Safe Attachments policy**</span></span>
     - <span data-ttu-id="77a22-163">**Stratégie anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="77a22-163">**Anti-phish policy**</span></span>
     - <span data-ttu-id="77a22-164">**Stratégie de filtrage de contenu hébergé**</span><span class="sxs-lookup"><span data-stu-id="77a22-164">**Hosted content filter policy**</span></span>
     - <span data-ttu-id="77a22-165">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="77a22-165">**Transport rule**</span></span>

   - <span data-ttu-id="77a22-166">**Destinataire du message**: tous les utilisateurs ou seulement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="77a22-166">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="77a22-167">Les utilisateurs finaux peuvent gérer uniquement les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="77a22-167">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="77a22-168">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-168">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="77a22-169">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-169">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="77a22-170">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="77a22-170">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="77a22-171">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="77a22-171">Wildcards aren't supported.</span></span> <span data-ttu-id="77a22-172">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-172">You can search by the following values:</span></span>

   - <span data-ttu-id="77a22-173">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="77a22-173">**Message ID**: The globally unique identifier of the message.</span></span>

     <span data-ttu-id="77a22-174">Par exemple, vous avez utilisé le [suivi des messages](message-trace-scc.md) pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="77a22-174">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="77a22-175">Veillez à inclure la valeur d’ID de message complète, qui peut inclure des chevrons ( \<\> ).</span><span class="sxs-lookup"><span data-stu-id="77a22-175">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="77a22-176">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="77a22-176">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="77a22-177">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="77a22-177">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="77a22-178">**Nom**de la stratégie : utilisez le nom de la stratégie complète du message.</span><span class="sxs-lookup"><span data-stu-id="77a22-178">**Policy name**: Use the entire policy name of the message.</span></span> <span data-ttu-id="77a22-179">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="77a22-179">The search is not case-sensitive.</span></span>

   - <span data-ttu-id="77a22-180">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="77a22-180">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="77a22-181">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="77a22-181">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="77a22-182">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="77a22-182">The search is not case-sensitive.</span></span>

   <span data-ttu-id="77a22-183">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="77a22-183">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="77a22-184">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="77a22-184">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-message-results"></a><span data-ttu-id="77a22-185">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="77a22-185">Export message results</span></span>

1. <span data-ttu-id="77a22-186">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="77a22-186">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="77a22-187">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="77a22-187">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="77a22-188">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="77a22-188">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="77a22-189">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-189">View quarantined message details</span></span>

<span data-ttu-id="77a22-190">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="77a22-190">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="77a22-191">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="77a22-191">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="77a22-192">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="77a22-192">**Sender address**</span></span>

- <span data-ttu-id="77a22-193">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="77a22-193">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="77a22-194">**Subject**</span><span class="sxs-lookup"><span data-stu-id="77a22-194">**Subject**</span></span>

- <span data-ttu-id="77a22-195">**Raison**de la mise en quarantaine : indique si un message a été identifié **Bulk**comme **courrier indésirable**, **hameçon, hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="77a22-195">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="77a22-196">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="77a22-196">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="77a22-197">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="77a22-197">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="77a22-198">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="77a22-198">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="77a22-199">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="77a22-199">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="77a22-200">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-200">Take action on quarantined email</span></span>

<span data-ttu-id="77a22-201">Une fois que vous avez sélectionné un message, vous disposez de plusieurs options pour effectuer les messages dans le volet de la fenêtre de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="77a22-201">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="77a22-202">**Message de publication**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-202">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="77a22-203">**Signaler les messages à Microsoft pour analyse**: cette option est sélectionnée par défaut et signale le message en quarantaine à Microsoft comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="77a22-203">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="77a22-204">Si le message a été mis en quarantaine en tant que courrier indésirable, en masse, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77a22-204">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="77a22-205">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="77a22-205">Depending on their analysis, the service-wide spam filter rules might be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="77a22-206">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-206">Choose one of the following options:</span></span>
    - <span data-ttu-id="77a22-207">**Diffuser les messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="77a22-207">**Release messages to all recipients**</span></span>
    - <span data-ttu-id="77a22-208">**Publier des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="77a22-208">**Release messages to specific recipients**</span></span>
    - <span data-ttu-id="77a22-209">**Publier des messages vers d’autres personnes**</span><span class="sxs-lookup"><span data-stu-id="77a22-209">**Release messages to other people**</span></span>

  <span data-ttu-id="77a22-210">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="77a22-210">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="77a22-211">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="77a22-211">Notes about releasing messages:</span></span>

  - <span data-ttu-id="77a22-212">Vous ne pouvez pas diffuser un message au même destinataire plus d’une fois.</span><span class="sxs-lookup"><span data-stu-id="77a22-212">You can't release a message to the same recipient more than once.</span></span>

  - <span data-ttu-id="77a22-213">Seuls les destinataires qui n’ont pas reçu le message s’affichent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="77a22-213">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="77a22-214">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="77a22-214">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="77a22-215">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="77a22-215">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="77a22-216">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="77a22-216">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="77a22-217">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-217">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="77a22-218">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="77a22-218">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  - <span data-ttu-id="77a22-219">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="77a22-219">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="77a22-220">**Supprimer de la quarantaine**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="77a22-220">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="77a22-221">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="77a22-221">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="77a22-222">**Envoyer un message**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-222">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="77a22-223">**Type d’objet**: **e-mail** (par défaut), **URL**ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="77a22-223">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="77a22-224">**Format d’envoi**: **ID de message réseau** (par défaut, avec la valeur correspondante dans la zone **ID de message réseau** ) ou **fichier** (accédez à un fichier. eml ou. MSG local).</span><span class="sxs-lookup"><span data-stu-id="77a22-224">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="77a22-225">Notez que si vous sélectionnez **fichier** , puis **ID de message réseau**, la valeur initiale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="77a22-225">Note that if you select **File** and then select **Network Message ID**, the initially value is gone.</span></span>

  - <span data-ttu-id="77a22-226">**Destinataires**: saisissez au bail d’un destinataire d’origine du message, ou cliquez sur **Sélectionner tout** pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="77a22-226">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="77a22-227">Vous pouvez également cliquer sur **Sélectionner tout** , puis supprimer des destinataires de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="77a22-227">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="77a22-228">**Raison du dépôt**: **ne doit pas avoir été bloqué** (par défaut) ou **doit avoir été bloqué**.</span><span class="sxs-lookup"><span data-stu-id="77a22-228">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="77a22-229">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-229">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="77a22-230">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="77a22-230">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="77a22-231">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-231">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="77a22-232">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-232">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="77a22-233">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="77a22-233">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="77a22-234">Prenons le scénario suivant : john@gmail.com envoie un message à faith@contoso.com et john@subsidiary.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="77a22-234">Consider the following scenario: john@gmail.com sends a message to faith@contoso.com and john@subsidiary.contoso.com.</span></span> <span data-ttu-id="77a22-235">Gmail bifurcation ce message en deux exemplaires qui sont tous deux routés en quarantaine en tant que hameçonnage dans Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77a22-235">Gmail bifurcates this message into two copies that are both routed to quarantine as phishing in Microsoft.</span></span> <span data-ttu-id="77a22-236">Un administrateur publie ces deux messages dans admin@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="77a22-236">An admin releases both of these messages to admin@contoso.com.</span></span> <span data-ttu-id="77a22-237">Le premier message publié qui atteint la boîte aux lettres d’administration est remis.</span><span class="sxs-lookup"><span data-stu-id="77a22-237">The first released message that reaches the admin mailbox is delivered.</span></span> <span data-ttu-id="77a22-238">Le deuxième message publié est identifié comme remise en double et est ignoré.</span><span class="sxs-lookup"><span data-stu-id="77a22-238">The second released message is identified as duplicate delivery and is skipped.</span></span> <span data-ttu-id="77a22-239">Les messages sont identifiés comme étant des doublons s’ils ont le même ID de message et le même horaire de réception.</span><span class="sxs-lookup"><span data-stu-id="77a22-239">Message are identified as duplicates if they have the same message ID and received time.</span></span>

- <span data-ttu-id="77a22-240">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="77a22-240">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="77a22-241">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-241">When you're finished, click **Close**.</span></span>

## <a name="atp-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="77a22-242">ATP uniquement : utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-242">ATP Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="77a22-243">Les procédures des fichiers mis en quarantaine dans cette section sont uniquement disponibles pour les abonnés plan 1 et plan 2.</span><span class="sxs-lookup"><span data-stu-id="77a22-243">The procedures for quarantined files in this section are available only to ATP Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="77a22-244">Dans les organisations avec ATP, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="77a22-244">In organizations with ATP, admins can manage quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="77a22-245">Afficher les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-245">View quarantined files</span></span>

1. <span data-ttu-id="77a22-246">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="77a22-246">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="77a22-247">Modifier la **vue mise en quarantaine** sur les **fichiers**de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="77a22-247">Change **View quarantined** to the default value **files**.</span></span> <span data-ttu-id="77a22-248">Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="77a22-248">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="77a22-249">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="77a22-249">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="77a22-250">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="77a22-250">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="77a22-251">Les colonnes par défaut sont marquées d’un astérisque ( <sup>\*</sup> ) :</span><span class="sxs-lookup"><span data-stu-id="77a22-251">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="77a22-252">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-252">**User**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-253">**Emplacements**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-253">**Location**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-254">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-254">**File name**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-255">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-255">**File URL**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-256">**Taille de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-256">**File Size**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-257">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-257">**Expires**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-258">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="77a22-258">**Released?**<sup>\*</sup></span></span>
   - <span data-ttu-id="77a22-259">**Détectés par**</span><span class="sxs-lookup"><span data-stu-id="77a22-259">**Detected by**</span></span>
   - <span data-ttu-id="77a22-260">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="77a22-260">**Modified by time**</span></span>

4. <span data-ttu-id="77a22-261">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="77a22-261">To filter the results, click **Filter**.</span></span> <span data-ttu-id="77a22-262">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="77a22-262">The available filters are:</span></span>

   - <span data-ttu-id="77a22-263">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="77a22-263">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>
     - <span data-ttu-id="77a22-264">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="77a22-264">**Today**</span></span>
     - <span data-ttu-id="77a22-265">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="77a22-265">**Next 2 days**</span></span>
     - <span data-ttu-id="77a22-266">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="77a22-266">**Next 7 days**</span></span>
     - <span data-ttu-id="77a22-267">Une plage date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="77a22-267">A custom date/time range.</span></span>
   - <span data-ttu-id="77a22-268">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="77a22-268">**Received time**</span></span>
   - <span data-ttu-id="77a22-269">**Raison**de la mise en quarantaine : la seule valeur disponible est **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="77a22-269">**Quarantine reason**: The only available value is **Malware**.</span></span>

<span data-ttu-id="77a22-270">Une fois que vous avez trouvé un fichier en quarantaine spécifique, sélectionnez le fichier pour en afficher les détails et effectuer une action (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="77a22-270">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-file-results"></a><span data-ttu-id="77a22-271">Exporter les résultats des fichiers</span><span class="sxs-lookup"><span data-stu-id="77a22-271">Export file results</span></span>

1. <span data-ttu-id="77a22-272">Sélectionnez les fichiers qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="77a22-272">Select the files you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="77a22-273">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="77a22-273">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="77a22-274">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="77a22-274">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="77a22-275">Afficher les détails des fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-275">View quarantined file details</span></span>

<span data-ttu-id="77a22-276">Lorsque vous sélectionnez un fichier dans la liste, les détails de fichier suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="77a22-276">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="77a22-277">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="77a22-277">**File Name**</span></span>
- <span data-ttu-id="77a22-278">**URL du fichier**: URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="77a22-278">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>
- <span data-ttu-id="77a22-279">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="77a22-279">**Malicious content detected on** The date/time the file was quarantined.</span></span>
- <span data-ttu-id="77a22-280">**Expire**: date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="77a22-280">**Expires**: The date when the file will be deleted from quarantine.</span></span>
- <span data-ttu-id="77a22-281">**Détecté par**: ATP (protection avancée contre les menaces) ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77a22-281">**Detected By**: ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span>
- <span data-ttu-id="77a22-282">**Déplacer ?**</span><span class="sxs-lookup"><span data-stu-id="77a22-282">**Released?**</span></span>
- <span data-ttu-id="77a22-283">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="77a22-283">**Malware Name**</span></span>
- <span data-ttu-id="77a22-284">**ID de document**: identificateur unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="77a22-284">**Document ID**: A unique identifier for the document.</span></span>
- <span data-ttu-id="77a22-285">**Taille du fichier**: en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="77a22-285">**File Size**: In kilobytes (KB).</span></span>
- <span data-ttu-id="77a22-286">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="77a22-286">**Organization** Your organization's unique ID.</span></span>
- <span data-ttu-id="77a22-287">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="77a22-287">**Last modified**</span></span>
- <span data-ttu-id="77a22-288">**Modifié par**: utilisateur qui a modifié le fichier pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="77a22-288">**Modified By**: The user who last modified the file.</span></span>
- <span data-ttu-id="77a22-289">**Valeur 256-bit (SHA-256) de l’algorithme de hachage sécurisé**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou dans d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="77a22-289">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="77a22-290">Effectuer des actions sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-290">Take action on quarantined files</span></span>

<span data-ttu-id="77a22-291">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez effectuer les actions suivantes sur le fichier dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="77a22-291">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="77a22-292">**Fichiers de version**: sélectionnez (par défaut) ou désélectionnez **les fichiers de rapports à Microsoft pour analyse**, puis cliquez sur **libérer les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="77a22-292">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>
- <span data-ttu-id="77a22-293">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="77a22-293">**Download file**</span></span>
- <span data-ttu-id="77a22-294">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="77a22-294">**Remove file from quarantine**</span></span>

<span data-ttu-id="77a22-295">Si vous ne libérez pas ou ne supprimez pas les fichiers, ils seront supprimés une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="77a22-295">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="77a22-296">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-296">Actions on multiple quarantined files</span></span>

<span data-ttu-id="77a22-297">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-297">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="77a22-298">**Fichiers de version**</span><span class="sxs-lookup"><span data-stu-id="77a22-298">**Release files**</span></span>
- <span data-ttu-id="77a22-299">**Supprimer des fichiers**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="77a22-299">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

1. <span data-ttu-id="77a22-300">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="77a22-300">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="77a22-301">Utiliser Exchange Online PowerShell ou l’environnement de ligne de commande Exchange EOP PowerShell autonome pour afficher et gérer les messages et les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="77a22-301">Use Exchange Online PowerShell or standalone EOP PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="77a22-302">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a22-302">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="77a22-303">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="77a22-303">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/delete-quarantinemessage)

- [<span data-ttu-id="77a22-304">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="77a22-304">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/export-quarantinemessage)

- [<span data-ttu-id="77a22-305">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="77a22-305">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage)

- <span data-ttu-id="77a22-306">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/preview-quarantinemessage): Notez que cette applet de commande concerne uniquement les messages, pas les fichiers de programmes malveillants, pour SharePoint Online, OneDrive entreprise ou Teams.</span><span class="sxs-lookup"><span data-stu-id="77a22-306">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from ATP for SharePoint Online, OneDrive for Business, or Teams.</span></span>

- [<span data-ttu-id="77a22-307">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="77a22-307">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage)
