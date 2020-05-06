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
description: Dans cet article, vous allez découvrir comment les administrateurs peuvent gérer les messages et les fichiers mis en quarantaine pour les utilisateurs dans Office 365.
ms.openlocfilehash: e69887b54b3e892775c16fa3e306da3b17ab7db3
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036172"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator"></a><span data-ttu-id="d2411-103">Gérer les fichiers et les messages mis en quarantaine en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="d2411-103">Manage quarantined messages and files as an administrator</span></span>

<span data-ttu-id="d2411-104">La quarantaine contient des messages potentiellement dangereux ou indésirables dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d2411-104">Quarantine holds potentially dangerous or unwanted messages in Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="d2411-105">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-105">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="d2411-106">Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d2411-106">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="d2411-107">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="d2411-107">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="d2411-108">Les administrateurs peuvent également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2411-108">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="d2411-109">Les administrateurs dans les organisations disposant d’Office 365 Advanced Threat Protection (ATP) peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d2411-109">Admins in organizations with Office 365 Advance Threat Protection (ATP) can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="d2411-110">Vous pouvez afficher et gérer les messages mis en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les clients Microsoft 365 ; Exchange Online Protection PowerShell pour les clients EOP autonomes).</span><span class="sxs-lookup"><span data-stu-id="d2411-110">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 customers; Exchange Online Protection PowerShell for standalone EOP customers).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d2411-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d2411-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d2411-112">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="d2411-112">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="d2411-113">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="d2411-113">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="d2411-114">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="d2411-114">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="d2411-115">Pour vous connecter à Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="d2411-115">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="d2411-116">Vous devez disposer d’autorisations pour pouvoir gérer la mise en quarantaine en tant qu’administrateur. Les autorisations sont contrôlées par le rôle de **mise en quarantaine** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="d2411-116">You need to be assigned permissions before you can manage the quarantine as an admin. The permissions are controlled by the **Quarantine** role in the Security & Compliance Center.</span></span> <span data-ttu-id="d2411-117">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l' **organisation** (administrateurs globaux), administrateur de **mise en quarantaine**et administrateur de **sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="d2411-117">By default, this role is assigned to the **Organization Management** (Global admins), **Quarantine Administrator**, and **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="d2411-118">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-118">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="d2411-119">Les messages mis en quarantaine sont conservés pendant une période de temps par défaut avant d’être supprimés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="d2411-119">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>

  - <span data-ttu-id="d2411-120">Messages mis en quarantaine par des stratégies de blocage du courrier indésirable (courrier indésirable, hameçonnage et courrier en masse) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="d2411-120">Messages quarantined by anti-spam policies (spam, phishing, and bulk email): 30 days.</span></span> <span data-ttu-id="d2411-121">Il s’agit de la valeur par défaut et la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="d2411-121">This is the default and maximum value.</span></span> <span data-ttu-id="d2411-122">Pour configurer cette valeur, reportez-vous à la rubrique [configurer des stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-122">To configure this value, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="d2411-123">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-123">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

  - <span data-ttu-id="d2411-124">Messages contenant des programmes malveillants : 15 jours.</span><span class="sxs-lookup"><span data-stu-id="d2411-124">Messages that contain malware: 15 days.</span></span>

  <span data-ttu-id="d2411-125">Lorsqu’un message arrive à expiration en quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="d2411-125">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="d2411-126">Utiliser le centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-126">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="d2411-127">Afficher le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-127">View quarantined email</span></span>

1. <span data-ttu-id="d2411-128">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="d2411-128">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="d2411-129">Vérifiez que l’option **afficher en quarantaine** est définie sur la valeur par défaut **e-mail**.</span><span class="sxs-lookup"><span data-stu-id="d2411-129">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="d2411-130">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="d2411-130">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="d2411-131">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="d2411-131">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="d2411-132">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="d2411-132">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="d2411-133">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-133">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-134">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-134">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-135">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-135">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-136">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-136">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-137">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-137">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-138">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-138">**Policy type**<sup>\*</sup></span></span>

1. <span data-ttu-id="d2411-139">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-139">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

   - <span data-ttu-id="d2411-140">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="d2411-140">**Recipient**</span></span>

   - <span data-ttu-id="d2411-141">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="d2411-141">**Message ID**</span></span>

   - <span data-ttu-id="d2411-142">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="d2411-142">**Policy name**</span></span>

   - <span data-ttu-id="d2411-143">**Taille**</span><span class="sxs-lookup"><span data-stu-id="d2411-143">**Size**</span></span>

   - <span data-ttu-id="d2411-144">**Direction**</span><span class="sxs-lookup"><span data-stu-id="d2411-144">**Direction**</span></span>

   <span data-ttu-id="d2411-145">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="d2411-145">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="d2411-146">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-146">To filter the results, click **Filter**.</span></span> <span data-ttu-id="d2411-147">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="d2411-147">The available filters are:</span></span>

   - <span data-ttu-id="d2411-148">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="d2411-148">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="d2411-149">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="d2411-149">**Today**</span></span>

     - <span data-ttu-id="d2411-150">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="d2411-150">**Next 2 days**</span></span>

     - <span data-ttu-id="d2411-151">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="d2411-151">**Next 7 days**</span></span>

     - <span data-ttu-id="d2411-152">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="d2411-152">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="d2411-153">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="d2411-153">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="d2411-154">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="d2411-154">**Quarantine reason**:</span></span>

     - <span data-ttu-id="d2411-155">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="d2411-155">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>

     - <span data-ttu-id="d2411-156">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="d2411-156">**Bulk**</span></span>

     - <span data-ttu-id="d2411-157">**Jouer**</span><span class="sxs-lookup"><span data-stu-id="d2411-157">**Phish**</span></span>

     - <span data-ttu-id="d2411-158">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="d2411-158">**Malware**</span></span>

     - <span data-ttu-id="d2411-159">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="d2411-159">**Spam**</span></span>

     - <span data-ttu-id="d2411-160">**Hameçonnage à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="d2411-160">**High Confidence Phish**</span></span>

   - <span data-ttu-id="d2411-161">**Destinataire du message**: tous les utilisateurs ou seulement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="d2411-161">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="d2411-162">Les utilisateurs finaux peuvent gérer uniquement les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="d2411-162">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="d2411-163">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-163">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="d2411-164">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-164">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="d2411-165">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d2411-165">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="d2411-166">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d2411-166">Wildcards aren't supported.</span></span> <span data-ttu-id="d2411-167">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-167">You can search by the following values:</span></span>

   - <span data-ttu-id="d2411-168">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="d2411-168">**Message ID**: The globally unique identifier of the message.</span></span>

        <span data-ttu-id="d2411-169">Par exemple, vous avez utilisé le [suivi des messages](message-trace-scc.md) pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="d2411-169">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="d2411-170">Veillez à inclure la valeur d’ID de message complète, qui peut inclure des\<\>chevrons ().</span><span class="sxs-lookup"><span data-stu-id="d2411-170">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="d2411-171">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="d2411-171">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="d2411-172">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d2411-172">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="d2411-173">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="d2411-173">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="d2411-174">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="d2411-174">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="d2411-175">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="d2411-175">The search is not case-sensitive.</span></span>

   <span data-ttu-id="d2411-176">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="d2411-176">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="d2411-177">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="d2411-177">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-message-results"></a><span data-ttu-id="d2411-178">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="d2411-178">Export message results</span></span>

1. <span data-ttu-id="d2411-179">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="d2411-179">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="d2411-180">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="d2411-180">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="d2411-181">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="d2411-181">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="d2411-182">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-182">View quarantined message details</span></span>

<span data-ttu-id="d2411-183">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="d2411-183">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="d2411-184">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="d2411-184">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="d2411-185">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="d2411-185">**Sender address**</span></span>

- <span data-ttu-id="d2411-186">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="d2411-186">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="d2411-187">**Subject**</span><span class="sxs-lookup"><span data-stu-id="d2411-187">**Subject**</span></span>

- <span data-ttu-id="d2411-188">**Raison**de la mise en quarantaine : indique si un message a été identifié **Bulk**comme **courrier indésirable**, **hameçon, hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="d2411-188">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="d2411-189">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="d2411-189">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="d2411-190">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d2411-190">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="d2411-191">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="d2411-191">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="d2411-192">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="d2411-192">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="d2411-193">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-193">Take action on quarantined email</span></span>

<span data-ttu-id="d2411-194">Une fois que vous avez sélectionné un message, vous disposez de plusieurs options pour effectuer les messages dans le volet de la fenêtre de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="d2411-194">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="d2411-195">**Message de publication**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-195">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="d2411-196">**Signaler les messages à Microsoft pour analyse**: cette option est sélectionnée par défaut et signale le message en quarantaine à Microsoft comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="d2411-196">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="d2411-197">Si le message a été mis en quarantaine en tant que courrier indésirable, en masse, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2411-197">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="d2411-198">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="d2411-198">Depending on their analysis, the service-wide spam filter rules might be be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="d2411-199">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-199">Choose one of the following options:</span></span>

    - <span data-ttu-id="d2411-200">**Diffuser les messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="d2411-200">**Release messages to all recipients**</span></span>

    - <span data-ttu-id="d2411-201">**Publier des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="d2411-201">**Release messages to specific recipients**</span></span>

    - <span data-ttu-id="d2411-202">**Publier des messages vers d’autres personnes**</span><span class="sxs-lookup"><span data-stu-id="d2411-202">**Release messages to other people**</span></span>

  <span data-ttu-id="d2411-203">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="d2411-203">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="d2411-204">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="d2411-204">Notes about releasing messages:</span></span>

  - <span data-ttu-id="d2411-205">Vous ne pouvez pas diffuser un message au même destinataire plus d’une fois.</span><span class="sxs-lookup"><span data-stu-id="d2411-205">You can't release a message to the same recipient more than once.</span></span>

  - <span data-ttu-id="d2411-206">Seuls les destinataires qui n’ont pas reçu le message s’affichent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="d2411-206">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="d2411-207">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="d2411-207">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="d2411-208">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="d2411-208">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="d2411-209">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="d2411-209">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="d2411-210">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-210">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="d2411-211">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="d2411-211">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="d2411-212">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="d2411-212">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="d2411-213">**Supprimer de la quarantaine**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="d2411-213">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="d2411-214">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="d2411-214">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="d2411-215">**Envoyer un message**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-215">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="d2411-216">**Type d’objet**: **e-mail** (par défaut), **URL**ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="d2411-216">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="d2411-217">**Format d’envoi**: **ID de message réseau** (par défaut, avec la valeur correspondante dans la zone **ID de message réseau** ) ou **fichier** (accédez à un fichier. eml ou. MSG local).</span><span class="sxs-lookup"><span data-stu-id="d2411-217">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="d2411-218">Notez que si vous sélectionnez **fichier** , puis **ID de message réseau**, la valeur initiale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="d2411-218">Note that if you select **File** and then select **Network Message ID**, the initially value is gone.</span></span>

  - <span data-ttu-id="d2411-219">**Destinataires**: saisissez au bail d’un destinataire d’origine du message, ou cliquez sur **Sélectionner tout** pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="d2411-219">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="d2411-220">Vous pouvez également cliquer sur **Sélectionner tout** , puis supprimer des destinataires de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="d2411-220">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="d2411-221">**Raison du dépôt**: **ne doit pas avoir été bloqué** (par défaut) ou **doit avoir été bloqué**.</span><span class="sxs-lookup"><span data-stu-id="d2411-221">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="d2411-222">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-222">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="d2411-223">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2411-223">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="d2411-224">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-224">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="d2411-225">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-225">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="d2411-226">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="d2411-226">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="d2411-227">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d2411-227">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="d2411-228">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-228">When you're finished, click **Close**.</span></span>

## <a name="atp-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="d2411-229">ATP uniquement : utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-229">ATP Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="d2411-230">Les procédures des fichiers mis en quarantaine dans cette section sont uniquement disponibles pour les abonnés plan 1 et plan 2.</span><span class="sxs-lookup"><span data-stu-id="d2411-230">The procedures for quarantined files in this section are available only to ATP Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="d2411-231">Dans les organisations avec ATP, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d2411-231">In organizations with ATP, admins can managed quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="d2411-232">Afficher les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-232">View quarantined files</span></span>

1. <span data-ttu-id="d2411-233">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="d2411-233">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="d2411-234">Modifier la **vue mise en quarantaine** sur les **fichiers**de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2411-234">Change **View quarantined** to the default value **files**.</span></span> <span data-ttu-id="d2411-235">Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="d2411-235">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="d2411-236">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="d2411-236">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="d2411-237">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="d2411-237">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="d2411-238">Les colonnes par défaut sont marquées d’un<sup>\*</sup>astérisque () :</span><span class="sxs-lookup"><span data-stu-id="d2411-238">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="d2411-239">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-239">**User**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-240">**Emplacements**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-240">**Location**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-241">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-241">**File name**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-242">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-242">**File URL**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-243">**Taille de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-243">**File Size**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-244">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-244">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-245">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d2411-245">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="d2411-246">**Détectés par**</span><span class="sxs-lookup"><span data-stu-id="d2411-246">**Detected by**</span></span>

   - <span data-ttu-id="d2411-247">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="d2411-247">**Modified by time**</span></span>

4. <span data-ttu-id="d2411-248">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="d2411-248">To filter the results, click **Filter**.</span></span> <span data-ttu-id="d2411-249">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="d2411-249">The available filters are:</span></span>

   - <span data-ttu-id="d2411-250">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="d2411-250">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="d2411-251">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="d2411-251">**Today**</span></span>

     - <span data-ttu-id="d2411-252">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="d2411-252">**Next 2 days**</span></span>

     - <span data-ttu-id="d2411-253">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="d2411-253">**Next 7 days**</span></span>

     - <span data-ttu-id="d2411-254">Une plage date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d2411-254">A custom date/time range.</span></span>

   - <span data-ttu-id="d2411-255">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="d2411-255">**Received time**</span></span>

   - <span data-ttu-id="d2411-256">**Raison**de la mise en quarantaine : la seule valeur disponible est **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="d2411-256">**Quarantine reason**: The only available value is **Malware**.</span></span>

<span data-ttu-id="d2411-257">Une fois que vous avez trouvé un fichier en quarantaine spécifique, sélectionnez le fichier pour en afficher les détails et effectuer une action (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="d2411-257">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-file-results"></a><span data-ttu-id="d2411-258">Exporter les résultats des fichiers</span><span class="sxs-lookup"><span data-stu-id="d2411-258">Export file results</span></span>

1. <span data-ttu-id="d2411-259">Sélectionnez les fichiers qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="d2411-259">Select the files you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="d2411-260">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="d2411-260">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="d2411-261">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="d2411-261">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="d2411-262">Afficher les détails des fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-262">View quarantined file details</span></span>

<span data-ttu-id="d2411-263">Lorsque vous sélectionnez un fichier dans la liste, les détails de fichier suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="d2411-263">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="d2411-264">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="d2411-264">**File Name**</span></span>

- <span data-ttu-id="d2411-265">**URL du fichier**: URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="d2411-265">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>

- <span data-ttu-id="d2411-266">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="d2411-266">**Malicious content detected on** The date/time the file was quarantined.</span></span>

- <span data-ttu-id="d2411-267">**Expire**: date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d2411-267">**Expires**: The date when the file will be deleted from quarantine.</span></span>

- <span data-ttu-id="d2411-268">**Détecté par**: ATP (protection avancée contre les menaces) ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2411-268">**Detected By**: ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span>

- <span data-ttu-id="d2411-269">**Déplacer ?**</span><span class="sxs-lookup"><span data-stu-id="d2411-269">**Released?**</span></span>

- <span data-ttu-id="d2411-270">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="d2411-270">**Malware Name**</span></span>

- <span data-ttu-id="d2411-271">**ID de document**: identificateur unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="d2411-271">**Document ID**: A unique identifier for the document.</span></span>

- <span data-ttu-id="d2411-272">**Taille du fichier**: en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="d2411-272">**File Size**: In kilobytes (KB).</span></span>

- <span data-ttu-id="d2411-273">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d2411-273">**Organization** Your organization's unique ID.</span></span>

- <span data-ttu-id="d2411-274">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="d2411-274">**Last modified**</span></span>

- <span data-ttu-id="d2411-275">**Modifié par**: utilisateur qui a modifié le fichier pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="d2411-275">**Modified By**: The user who last modified the file.</span></span>

- <span data-ttu-id="d2411-276">**Valeur 256-bit (SHA-256) de l’algorithme de hachage sécurisé**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou dans d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="d2411-276">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="d2411-277">Effectuer des actions sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-277">Take action on quarantined files</span></span>

<span data-ttu-id="d2411-278">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez effectuer les actions suivantes sur le fichier dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="d2411-278">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="d2411-279">**Fichiers de version**: sélectionnez (par défaut) ou désélectionnez **les fichiers de rapports à Microsoft pour analyse**, puis cliquez sur **libérer les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="d2411-279">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>

- <span data-ttu-id="d2411-280">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="d2411-280">**Download file**</span></span>

- <span data-ttu-id="d2411-281">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="d2411-281">**Remove file from quarantine**</span></span>

<span data-ttu-id="d2411-282">Si vous ne libérez pas ou ne supprimez pas les fichiers, ils seront supprimés une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="d2411-282">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="d2411-283">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-283">Actions on multiple quarantined files</span></span>

<span data-ttu-id="d2411-284">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-284">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="d2411-285">**Fichiers de version**</span><span class="sxs-lookup"><span data-stu-id="d2411-285">**Release files**</span></span>

- <span data-ttu-id="d2411-286">**Supprimer des fichiers**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="d2411-286">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

1. <span data-ttu-id="d2411-287">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d2411-287">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

## <a name="use-exchange-online-powershell-or-standalone-exchange-online-protection-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="d2411-288">Utiliser Exchange Online PowerShell ou un environnement Exchange Online Protection PowerShell autonome pour afficher et gérer les messages et fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2411-288">Use Exchange Online PowerShell or standalone Exchange Online Protection PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="d2411-289">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2411-289">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="d2411-290">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="d2411-290">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/delete-quarantinemessage)

- [<span data-ttu-id="d2411-291">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="d2411-291">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/export-quarantinemessage)

- [<span data-ttu-id="d2411-292">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="d2411-292">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage)

- <span data-ttu-id="d2411-293">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Notez que cette applet de commande concerne uniquement les messages, pas les fichiers de programmes malveillants, pour SharePoint Online, OneDrive entreprise ou Teams.</span><span class="sxs-lookup"><span data-stu-id="d2411-293">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from ATP for SharePoint Online, OneDrive for Business, or Teams.</span></span>

- [<span data-ttu-id="d2411-294">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="d2411-294">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage)
