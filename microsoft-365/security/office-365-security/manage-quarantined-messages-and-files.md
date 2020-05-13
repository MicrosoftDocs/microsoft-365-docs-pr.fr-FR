---
title: Gérer les fichiers et les messages mis en quarantaine en tant qu’administrateur
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
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à afficher et à gérer les messages mis en quarantaine pour tous les utilisateurs dans Exchange Online Protection (EOP). Les administrateurs dans les organisations avec Office 365 Advanced Threat Protection (Office 365 ATP) peuvent également gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.
ms.openlocfilehash: 0f0dd7ee14aeb4558674a6e2240e022df3c489fc
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44209006"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-eop"></a><span data-ttu-id="a3692-104">Gérer les messages et les fichiers mis en quarantaine en tant qu’administrateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="a3692-104">Manage quarantined messages and files as an admin in EOP</span></span>

<span data-ttu-id="a3692-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, la mise en quarantaine bloque les messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="a3692-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="a3692-106">Pour plus d’informations, consultez la rubrique [messages électroniques mis en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a3692-106">For more information, see [Quarantined email messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="a3692-107">Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3692-107">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="a3692-108">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="a3692-108">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="a3692-109">Les administrateurs peuvent également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3692-109">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="a3692-110">Les administrateurs dans les organisations disposant d’Office 365 Advanced Threat Protection (Office 365 ATP) peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3692-110">Admins in organizations with Office 365 Advance Threat Protection (Office 365 ATP) can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="a3692-111">Vous pouvez afficher et gérer les messages mis en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="a3692-111">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a3692-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a3692-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a3692-113">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="a3692-113">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="a3692-114">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="a3692-114">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="a3692-115">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="a3692-115">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="a3692-116">Pour vous connecter à Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="a3692-116">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="a3692-117">Vous devez disposer d’autorisations pour pouvoir gérer la mise en quarantaine en tant qu’administrateur. Les autorisations sont contrôlées par le rôle de **mise en quarantaine** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="a3692-117">You need to be assigned permissions before you can manage the quarantine as an admin. The permissions are controlled by the **Quarantine** role in the Security & Compliance Center.</span></span> <span data-ttu-id="a3692-118">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l' **organisation** (administrateurs globaux), administrateur de **mise en quarantaine**et administrateur de **sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="a3692-118">By default, this role is assigned to the **Organization Management** (Global admins), **Quarantine Administrator**, and **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="a3692-119">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a3692-119">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="a3692-120">Les messages mis en quarantaine sont conservés pendant une période de temps par défaut avant d’être supprimés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="a3692-120">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>

  - <span data-ttu-id="a3692-121">Messages mis en quarantaine par des stratégies de blocage du courrier indésirable (courrier indésirable, hameçonnage et courrier en masse) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a3692-121">Messages quarantined by anti-spam policies (spam, phishing, and bulk email): 30 days.</span></span> <span data-ttu-id="a3692-122">Il s’agit de la valeur par défaut et la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="a3692-122">This is the default and maximum value.</span></span> <span data-ttu-id="a3692-123">Pour configurer cette valeur, reportez-vous à la rubrique [configurer des stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a3692-123">To configure this value, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

  - <span data-ttu-id="a3692-124">Messages contenant des programmes malveillants : 15 jours.</span><span class="sxs-lookup"><span data-stu-id="a3692-124">Messages that contain malware: 15 days.</span></span>

  <span data-ttu-id="a3692-125">Lorsqu’un message arrive à expiration en quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="a3692-125">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="a3692-126">Utiliser le centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-126">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="a3692-127">Afficher le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-127">View quarantined email</span></span>

1. <span data-ttu-id="a3692-128">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="a3692-128">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="a3692-129">Vérifiez que l’option **afficher en quarantaine** est définie sur la valeur par défaut **e-mail**.</span><span class="sxs-lookup"><span data-stu-id="a3692-129">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="a3692-130">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="a3692-130">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="a3692-131">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="a3692-131">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="a3692-132">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="a3692-132">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="a3692-133">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-133">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-134">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-134">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-135">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-135">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-136">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-136">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-137">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-137">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-138">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-138">**Policy type**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-139">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="a3692-139">**Recipient**</span></span>

   - <span data-ttu-id="a3692-140">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="a3692-140">**Message ID**</span></span>

   - <span data-ttu-id="a3692-141">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="a3692-141">**Policy name**</span></span>

   - <span data-ttu-id="a3692-142">**Taille**</span><span class="sxs-lookup"><span data-stu-id="a3692-142">**Size**</span></span>

   - <span data-ttu-id="a3692-143">**Direction**</span><span class="sxs-lookup"><span data-stu-id="a3692-143">**Direction**</span></span>

   <span data-ttu-id="a3692-144">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="a3692-144">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="a3692-145">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-145">To filter the results, click **Filter**.</span></span> <span data-ttu-id="a3692-146">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="a3692-146">The available filters are:</span></span>

   - <span data-ttu-id="a3692-147">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a3692-147">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="a3692-148">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="a3692-148">**Today**</span></span>

     - <span data-ttu-id="a3692-149">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a3692-149">**Next 2 days**</span></span>

     - <span data-ttu-id="a3692-150">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a3692-150">**Next 7 days**</span></span>

     - <span data-ttu-id="a3692-151">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a3692-151">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a3692-152">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a3692-152">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a3692-153">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="a3692-153">**Quarantine reason**:</span></span>

     - <span data-ttu-id="a3692-154">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="a3692-154">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>

     - <span data-ttu-id="a3692-155">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="a3692-155">**Bulk**</span></span>

     - <span data-ttu-id="a3692-156">**Jouer**</span><span class="sxs-lookup"><span data-stu-id="a3692-156">**Phish**</span></span>

     - <span data-ttu-id="a3692-157">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="a3692-157">**Malware**</span></span>

     - <span data-ttu-id="a3692-158">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a3692-158">**Spam**</span></span>

     - <span data-ttu-id="a3692-159">**Hameçonnage à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="a3692-159">**High Confidence Phish**</span></span>

   - <span data-ttu-id="a3692-160">**Destinataire du message**: tous les utilisateurs ou seulement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="a3692-160">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="a3692-161">Les utilisateurs finaux peuvent gérer uniquement les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="a3692-161">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="a3692-162">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-162">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="a3692-163">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-163">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="a3692-164">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a3692-164">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="a3692-165">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3692-165">Wildcards aren't supported.</span></span> <span data-ttu-id="a3692-166">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-166">You can search by the following values:</span></span>

   - <span data-ttu-id="a3692-167">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="a3692-167">**Message ID**: The globally unique identifier of the message.</span></span>

     <span data-ttu-id="a3692-168">Par exemple, vous avez utilisé le [suivi des messages](message-trace-scc.md) pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="a3692-168">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="a3692-169">Veillez à inclure la valeur d’ID de message complète, qui peut inclure des chevrons ( \< \> ).</span><span class="sxs-lookup"><span data-stu-id="a3692-169">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="a3692-170">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="a3692-170">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="a3692-171">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a3692-171">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="a3692-172">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="a3692-172">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="a3692-173">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="a3692-173">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="a3692-174">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="a3692-174">The search is not case-sensitive.</span></span>

   <span data-ttu-id="a3692-175">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="a3692-175">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="a3692-176">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="a3692-176">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-message-results"></a><span data-ttu-id="a3692-177">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="a3692-177">Export message results</span></span>

1. <span data-ttu-id="a3692-178">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="a3692-178">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="a3692-179">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="a3692-179">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="a3692-180">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a3692-180">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="a3692-181">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-181">View quarantined message details</span></span>

<span data-ttu-id="a3692-182">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a3692-182">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a3692-183">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="a3692-183">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="a3692-184">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a3692-184">**Sender address**</span></span>

- <span data-ttu-id="a3692-185">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="a3692-185">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="a3692-186">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a3692-186">**Subject**</span></span>

- <span data-ttu-id="a3692-187">**Raison**de la mise en quarantaine : indique si un message a été identifié **Bulk**comme **courrier indésirable**, **hameçon, hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="a3692-187">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="a3692-188">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="a3692-188">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="a3692-189">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a3692-189">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="a3692-190">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a3692-190">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="a3692-191">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a3692-191">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="a3692-192">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-192">Take action on quarantined email</span></span>

<span data-ttu-id="a3692-193">Une fois que vous avez sélectionné un message, vous disposez de plusieurs options pour effectuer les messages dans le volet de la fenêtre de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a3692-193">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a3692-194">**Message de publication**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-194">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="a3692-195">**Signaler les messages à Microsoft pour analyse**: cette option est sélectionnée par défaut et signale le message en quarantaine à Microsoft comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="a3692-195">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="a3692-196">Si le message a été mis en quarantaine en tant que courrier indésirable, en masse, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3692-196">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="a3692-197">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="a3692-197">Depending on their analysis, the service-wide spam filter rules might be be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="a3692-198">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-198">Choose one of the following options:</span></span>

    - <span data-ttu-id="a3692-199">**Diffuser les messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="a3692-199">**Release messages to all recipients**</span></span>

    - <span data-ttu-id="a3692-200">**Publier des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="a3692-200">**Release messages to specific recipients**</span></span>

    - <span data-ttu-id="a3692-201">**Publier des messages vers d’autres personnes**</span><span class="sxs-lookup"><span data-stu-id="a3692-201">**Release messages to other people**</span></span>

  <span data-ttu-id="a3692-202">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="a3692-202">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="a3692-203">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="a3692-203">Notes about releasing messages:</span></span>

  - <span data-ttu-id="a3692-204">Vous ne pouvez pas diffuser un message au même destinataire plus d’une fois.</span><span class="sxs-lookup"><span data-stu-id="a3692-204">You can't release a message to the same recipient more than once.</span></span>

  - <span data-ttu-id="a3692-205">Seuls les destinataires qui n’ont pas reçu le message s’affichent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="a3692-205">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="a3692-206">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="a3692-206">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="a3692-207">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="a3692-207">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="a3692-208">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="a3692-208">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="a3692-209">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-209">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="a3692-210">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="a3692-210">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="a3692-211">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="a3692-211">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="a3692-212">**Supprimer de la quarantaine**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3692-212">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="a3692-213">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="a3692-213">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="a3692-214">**Envoyer un message**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-214">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="a3692-215">**Type d’objet**: **e-mail** (par défaut), **URL**ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="a3692-215">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="a3692-216">**Format d’envoi**: **ID de message réseau** (par défaut, avec la valeur correspondante dans la zone **ID de message réseau** ) ou **fichier** (accédez à un fichier. eml ou. MSG local).</span><span class="sxs-lookup"><span data-stu-id="a3692-216">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="a3692-217">Notez que si vous sélectionnez **fichier** , puis **ID de message réseau**, la valeur initiale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="a3692-217">Note that if you select **File** and then select **Network Message ID**, the initially value is gone.</span></span>

  - <span data-ttu-id="a3692-218">**Destinataires**: saisissez au bail d’un destinataire d’origine du message, ou cliquez sur **Sélectionner tout** pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="a3692-218">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="a3692-219">Vous pouvez également cliquer sur **Sélectionner tout** , puis supprimer des destinataires de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="a3692-219">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="a3692-220">**Raison du dépôt**: **ne doit pas avoir été bloqué** (par défaut) ou **doit avoir été bloqué**.</span><span class="sxs-lookup"><span data-stu-id="a3692-220">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="a3692-221">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-221">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="a3692-222">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3692-222">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="a3692-223">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-223">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="a3692-224">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-224">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="a3692-225">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="a3692-225">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="a3692-226">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a3692-226">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="a3692-227">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-227">When you're finished, click **Close**.</span></span>

## <a name="atp-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="a3692-228">ATP uniquement : utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-228">ATP Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="a3692-229">Les procédures des fichiers mis en quarantaine dans cette section sont uniquement disponibles pour les abonnés plan 1 et plan 2.</span><span class="sxs-lookup"><span data-stu-id="a3692-229">The procedures for quarantined files in this section are available only to ATP Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="a3692-230">Dans les organisations avec ATP, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3692-230">In organizations with ATP, admins can managed quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="a3692-231">Afficher les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-231">View quarantined files</span></span>

1. <span data-ttu-id="a3692-232">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="a3692-232">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="a3692-233">Modifier la **vue mise en quarantaine** sur les **fichiers**de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3692-233">Change **View quarantined** to the default value **files**.</span></span> <span data-ttu-id="a3692-234">Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="a3692-234">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="a3692-235">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="a3692-235">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="a3692-236">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="a3692-236">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="a3692-237">Les colonnes par défaut sont marquées d’un astérisque ( <sup>\*</sup> ) :</span><span class="sxs-lookup"><span data-stu-id="a3692-237">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="a3692-238">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-238">**User**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-239">**Emplacements**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-239">**Location**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-240">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-240">**File name**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-241">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-241">**File URL**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-242">**Taille de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-242">**File Size**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-243">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-243">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-244">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a3692-244">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="a3692-245">**Détectés par**</span><span class="sxs-lookup"><span data-stu-id="a3692-245">**Detected by**</span></span>

   - <span data-ttu-id="a3692-246">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="a3692-246">**Modified by time**</span></span>

4. <span data-ttu-id="a3692-247">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a3692-247">To filter the results, click **Filter**.</span></span> <span data-ttu-id="a3692-248">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="a3692-248">The available filters are:</span></span>

   - <span data-ttu-id="a3692-249">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a3692-249">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="a3692-250">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="a3692-250">**Today**</span></span>

     - <span data-ttu-id="a3692-251">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a3692-251">**Next 2 days**</span></span>

     - <span data-ttu-id="a3692-252">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a3692-252">**Next 7 days**</span></span>

     - <span data-ttu-id="a3692-253">Une plage date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a3692-253">A custom date/time range.</span></span>

   - <span data-ttu-id="a3692-254">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="a3692-254">**Received time**</span></span>

   - <span data-ttu-id="a3692-255">**Raison**de la mise en quarantaine : la seule valeur disponible est **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="a3692-255">**Quarantine reason**: The only available value is **Malware**.</span></span>

<span data-ttu-id="a3692-256">Une fois que vous avez trouvé un fichier en quarantaine spécifique, sélectionnez le fichier pour en afficher les détails et effectuer une action (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="a3692-256">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-file-results"></a><span data-ttu-id="a3692-257">Exporter les résultats des fichiers</span><span class="sxs-lookup"><span data-stu-id="a3692-257">Export file results</span></span>

1. <span data-ttu-id="a3692-258">Sélectionnez les fichiers qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="a3692-258">Select the files you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="a3692-259">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="a3692-259">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="a3692-260">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a3692-260">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="a3692-261">Afficher les détails des fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-261">View quarantined file details</span></span>

<span data-ttu-id="a3692-262">Lorsque vous sélectionnez un fichier dans la liste, les détails de fichier suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a3692-262">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a3692-263">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="a3692-263">**File Name**</span></span>

- <span data-ttu-id="a3692-264">**URL du fichier**: URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="a3692-264">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>

- <span data-ttu-id="a3692-265">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="a3692-265">**Malicious content detected on** The date/time the file was quarantined.</span></span>

- <span data-ttu-id="a3692-266">**Expire**: date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a3692-266">**Expires**: The date when the file will be deleted from quarantine.</span></span>

- <span data-ttu-id="a3692-267">**Détecté par**: ATP (protection avancée contre les menaces) ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3692-267">**Detected By**: ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span>

- <span data-ttu-id="a3692-268">**Déplacer ?**</span><span class="sxs-lookup"><span data-stu-id="a3692-268">**Released?**</span></span>

- <span data-ttu-id="a3692-269">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="a3692-269">**Malware Name**</span></span>

- <span data-ttu-id="a3692-270">**ID de document**: identificateur unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="a3692-270">**Document ID**: A unique identifier for the document.</span></span>

- <span data-ttu-id="a3692-271">**Taille du fichier**: en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="a3692-271">**File Size**: In kilobytes (KB).</span></span>

- <span data-ttu-id="a3692-272">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3692-272">**Organization** Your organization's unique ID.</span></span>

- <span data-ttu-id="a3692-273">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="a3692-273">**Last modified**</span></span>

- <span data-ttu-id="a3692-274">**Modifié par**: utilisateur qui a modifié le fichier pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="a3692-274">**Modified By**: The user who last modified the file.</span></span>

- <span data-ttu-id="a3692-275">**Valeur 256-bit (SHA-256) de l’algorithme de hachage sécurisé**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou dans d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a3692-275">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="a3692-276">Effectuer des actions sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-276">Take action on quarantined files</span></span>

<span data-ttu-id="a3692-277">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez effectuer les actions suivantes sur le fichier dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a3692-277">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a3692-278">**Fichiers de version**: sélectionnez (par défaut) ou désélectionnez **les fichiers de rapports à Microsoft pour analyse**, puis cliquez sur **libérer les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="a3692-278">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>

- <span data-ttu-id="a3692-279">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="a3692-279">**Download file**</span></span>

- <span data-ttu-id="a3692-280">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="a3692-280">**Remove file from quarantine**</span></span>

<span data-ttu-id="a3692-281">Si vous ne libérez pas ou ne supprimez pas les fichiers, ils seront supprimés une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="a3692-281">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="a3692-282">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-282">Actions on multiple quarantined files</span></span>

<span data-ttu-id="a3692-283">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-283">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="a3692-284">**Fichiers de version**</span><span class="sxs-lookup"><span data-stu-id="a3692-284">**Release files**</span></span>

- <span data-ttu-id="a3692-285">**Supprimer des fichiers**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="a3692-285">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

1. <span data-ttu-id="a3692-286">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a3692-286">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

## <a name="use-exchange-online-powershell-or-standalone-exchange-online-protection-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="a3692-287">Utiliser Exchange Online PowerShell ou un environnement Exchange Online Protection PowerShell autonome pour afficher et gérer les messages et fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a3692-287">Use Exchange Online PowerShell or standalone Exchange Online Protection PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="a3692-288">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3692-288">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="a3692-289">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="a3692-289">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/delete-quarantinemessage)

- [<span data-ttu-id="a3692-290">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="a3692-290">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/export-quarantinemessage)

- [<span data-ttu-id="a3692-291">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="a3692-291">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage)

- <span data-ttu-id="a3692-292">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Notez que cette applet de commande concerne uniquement les messages, pas les fichiers de programmes malveillants, pour SharePoint Online, OneDrive entreprise ou Teams.</span><span class="sxs-lookup"><span data-stu-id="a3692-292">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from ATP for SharePoint Online, OneDrive for Business, or Teams.</span></span>

- [<span data-ttu-id="a3692-293">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="a3692-293">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage)
