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
description: Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs. Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (règles de transport).
ms.openlocfilehash: 1ae64b71d29f9e2d973f5a73cc19790fe0736913
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43635353"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator"></a><span data-ttu-id="6d8f8-104">Gérer les fichiers et les messages mis en quarantaine en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="6d8f8-104">Manage quarantined messages and files as an administrator</span></span>

<span data-ttu-id="6d8f8-105">La mise en quarantaine bloque les messages potentiellement dangereux ou indésirables dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-105">Quarantine holds potentially dangerous or unwanted messages in Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="6d8f8-106">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-106">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="6d8f8-107">Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-107">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="6d8f8-108">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-108">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="6d8f8-109">Les administrateurs peuvent également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-109">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="6d8f8-110">Les administrateurs dans les organisations disposant d’Office 365 Advanced Threat Protection (ATP) peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-110">Admins in organizations with Office 365 Advance Threat Protection (ATP) can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="6d8f8-111">Vous pouvez afficher et gérer les messages mis en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les clients Microsoft 365 ; Exchange Online Protection PowerShell pour les clients EOP autonomes).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-111">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 customers; Exchange Online Protection PowerShell for standalone EOP customers).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6d8f8-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6d8f8-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6d8f8-113">Pour ouvrir le centre de sécurité & conformité, accédez <https://protection.office.com>à.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-113">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="6d8f8-114">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-114">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="6d8f8-115">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-115">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="6d8f8-116">Pour vous connecter à Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-116">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="6d8f8-117">Vous devez disposer d’autorisations pour pouvoir gérer la mise en quarantaine en tant qu’administrateur. Les autorisations sont contrôlées par le rôle de **mise en quarantaine** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-117">You need to be assigned permissions before you can manage the quarantine as an admin. The permissions are controlled by the **Quarantine** role in the Security & Compliance Center.</span></span> <span data-ttu-id="6d8f8-118">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l' **organisation** (administrateurs globaux), administrateur de **mise en quarantaine**et administrateur de **sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-118">By default, this role is assigned to the **Organization Management** (Global admins), **Quarantine Administrator**, and **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="6d8f8-119">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-119">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="6d8f8-120">Les messages mis en quarantaine sont conservés pendant une période de temps par défaut avant d’être supprimés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-120">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>

  - <span data-ttu-id="6d8f8-121">Messages mis en quarantaine par des stratégies de blocage du courrier indésirable (courrier indésirable, hameçonnage et courrier en masse) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-121">Messages quarantined by anti-spam policies (spam, phishing, and bulk email): 30 days.</span></span> <span data-ttu-id="6d8f8-122">Il s’agit de la valeur par défaut et la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-122">This is the default and maximum value.</span></span> <span data-ttu-id="6d8f8-123">Pour configurer cette valeur, reportez-vous à la rubrique [configurer des stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-123">To configure this value, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="6d8f8-124">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-124">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

  - <span data-ttu-id="6d8f8-125">Messages contenant des programmes malveillants : 15 jours.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-125">Messages that contain malware: 15 days.</span></span>

  <span data-ttu-id="6d8f8-126">Lorsqu’un message arrive à expiration en quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-126">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="6d8f8-127">Utiliser le centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-127">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="6d8f8-128">Afficher le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-128">View quarantined email</span></span>

1. <span data-ttu-id="6d8f8-129">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-129">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="6d8f8-130">Vérifiez que l’option **afficher en quarantaine** est définie sur la valeur par défaut **e-mail**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-130">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="6d8f8-131">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-131">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="6d8f8-132">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-132">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="6d8f8-133">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-133">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="6d8f8-134">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-134">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-135">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-135">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-136">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-136">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-137">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-137">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-138">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-138">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-139">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-139">**Policy type**<sup>\*</sup></span></span>

1. <span data-ttu-id="6d8f8-140">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-140">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

   - <span data-ttu-id="6d8f8-141">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-141">**Recipient**</span></span>

   - <span data-ttu-id="6d8f8-142">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-142">**Message ID**</span></span>

   - <span data-ttu-id="6d8f8-143">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-143">**Policy name**</span></span>

   - <span data-ttu-id="6d8f8-144">**Taille**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-144">**Size**</span></span>

   - <span data-ttu-id="6d8f8-145">**Direction**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-145">**Direction**</span></span>

   <span data-ttu-id="6d8f8-146">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-146">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="6d8f8-147">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-147">To filter the results, click **Filter**.</span></span> <span data-ttu-id="6d8f8-148">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-148">The available filters are:</span></span>

   - <span data-ttu-id="6d8f8-149">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-149">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="6d8f8-150">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-150">**Today**</span></span>

     - <span data-ttu-id="6d8f8-151">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-151">**Next 2 days**</span></span>

     - <span data-ttu-id="6d8f8-152">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-152">**Next 7 days**</span></span>

     - <span data-ttu-id="6d8f8-153">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-153">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="6d8f8-154">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-154">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="6d8f8-155">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-155">**Quarantine reason**:</span></span>

     - <span data-ttu-id="6d8f8-156">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-156">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>

     - <span data-ttu-id="6d8f8-157">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-157">**Bulk**</span></span>

     - <span data-ttu-id="6d8f8-158">**Jouer**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-158">**Phish**</span></span>

     - <span data-ttu-id="6d8f8-159">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-159">**Malware**</span></span>

     - <span data-ttu-id="6d8f8-160">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-160">**Spam**</span></span>

     - <span data-ttu-id="6d8f8-161">**Hameçonnage à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-161">**High Confidence Phish**</span></span>

   - <span data-ttu-id="6d8f8-162">**Destinataire du message**: tous les utilisateurs ou seulement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-162">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="6d8f8-163">Les utilisateurs finaux peuvent gérer uniquement les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-163">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="6d8f8-164">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-164">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="6d8f8-165">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-165">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="6d8f8-166">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-166">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="6d8f8-167">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-167">Wildcards aren't supported.</span></span> <span data-ttu-id="6d8f8-168">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-168">You can search by the following values:</span></span>

   - <span data-ttu-id="6d8f8-169">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-169">**Message ID**: The globally unique identifier of the message.</span></span>

        <span data-ttu-id="6d8f8-170">Par exemple, vous avez utilisé le [suivi des messages](message-trace-scc.md) pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-170">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="6d8f8-171">Veillez à inclure la valeur d’ID de message complète, qui peut inclure des\<\>chevrons ().</span><span class="sxs-lookup"><span data-stu-id="6d8f8-171">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="6d8f8-172">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-172">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="6d8f8-173">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-173">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="6d8f8-174">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-174">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="6d8f8-175">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-175">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="6d8f8-176">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-176">The search is not case-sensitive.</span></span>

   <span data-ttu-id="6d8f8-177">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-177">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="6d8f8-178">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-178">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-message-results"></a><span data-ttu-id="6d8f8-179">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="6d8f8-179">Export message results</span></span>

1. <span data-ttu-id="6d8f8-180">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-180">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="6d8f8-181">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-181">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="6d8f8-182">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-182">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="6d8f8-183">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-183">View quarantined message details</span></span>

<span data-ttu-id="6d8f8-184">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-184">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="6d8f8-185">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-185">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="6d8f8-186">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-186">**Sender address**</span></span>

- <span data-ttu-id="6d8f8-187">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-187">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="6d8f8-188">**Subject**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-188">**Subject**</span></span>

- <span data-ttu-id="6d8f8-189">**Raison**de la mise en quarantaine : indique si un message a été identifié **Bulk**comme **courrier indésirable**, **hameçon, hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-189">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="6d8f8-190">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-190">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="6d8f8-191">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-191">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="6d8f8-192">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-192">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="6d8f8-193">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-193">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="6d8f8-194">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-194">Take action on quarantined email</span></span>

<span data-ttu-id="6d8f8-195">Une fois que vous avez sélectionné un message, vous disposez de plusieurs options pour effectuer les messages dans le volet de la fenêtre de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-195">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="6d8f8-196">**Message de publication**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-196">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="6d8f8-197">**Signaler les messages à Microsoft pour analyse**: cette option est sélectionnée par défaut et signale le message en quarantaine à Microsoft comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-197">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="6d8f8-198">Si le message a été mis en quarantaine en tant que courrier indésirable, en masse, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-198">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="6d8f8-199">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-199">Depending on their analysis, the service-wide spam filter rules might be be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="6d8f8-200">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-200">Choose one of the following options:</span></span>

    - <span data-ttu-id="6d8f8-201">**Diffuser les messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-201">**Release messages to all recipients**</span></span>

    - <span data-ttu-id="6d8f8-202">**Publier des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-202">**Release messages to specific recipients**</span></span>

    - <span data-ttu-id="6d8f8-203">**Publier des messages vers d’autres personnes**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-203">**Release messages to other people**</span></span>

  <span data-ttu-id="6d8f8-204">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-204">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="6d8f8-205">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-205">Notes about releasing messages:</span></span>

  - <span data-ttu-id="6d8f8-206">Vous ne pouvez pas diffuser un message au même destinataire plus d’une fois.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-206">You can't release a message to the same recipient more than once.</span></span>

  - <span data-ttu-id="6d8f8-207">Seuls les destinataires qui n’ont pas reçu le message s’affichent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-207">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="6d8f8-208">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-208">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="6d8f8-209">Pour analyser les champs d’en-tête et les valeurs en profondeur, copiez le texte de l’en-tête du message dans votre presse-papiers, puis choisissez **analyseur d’en-têtes de message Microsoft** pour accéder à l’analyseur de connectivité à distance (cliquez avec le bouton droit et choisissez **ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 pour effectuer cette tâche).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-209">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="6d8f8-210">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-210">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="6d8f8-211">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-211">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="6d8f8-212">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-212">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="6d8f8-213">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-213">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="6d8f8-214">**Supprimer de la quarantaine**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-214">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="6d8f8-215">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-215">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="6d8f8-216">**Envoyer un message**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-216">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="6d8f8-217">**Type d’objet**: **e-mail** (par défaut), **URL**ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-217">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="6d8f8-218">**Format d’envoi**: **ID de message réseau** (par défaut, avec la valeur correspondante dans la zone **ID de message réseau** ) ou **fichier** (accédez à un fichier. eml ou. MSG local).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-218">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="6d8f8-219">Notez que si vous sélectionnez **fichier** , puis **ID de message réseau**, la valeur initiale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-219">Note that if you select **File** and then select **Network Message ID**, the initially value is gone.</span></span>

  - <span data-ttu-id="6d8f8-220">**Destinataires**: saisissez au bail d’un destinataire d’origine du message, ou cliquez sur **Sélectionner tout** pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-220">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="6d8f8-221">Vous pouvez également cliquer sur **Sélectionner tout** , puis supprimer des destinataires de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-221">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="6d8f8-222">**Raison du dépôt**: **ne doit pas avoir été bloqué** (par défaut) ou **doit avoir été bloqué**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-222">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="6d8f8-223">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-223">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="6d8f8-224">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-224">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="6d8f8-225">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-225">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="6d8f8-226">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-226">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="6d8f8-227">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-227">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="6d8f8-228">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-228">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="6d8f8-229">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-229">When you're finished, click **Close**.</span></span>

## <a name="atp-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="6d8f8-230">ATP uniquement : utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-230">ATP Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="6d8f8-231">Les procédures des fichiers mis en quarantaine dans cette section sont uniquement disponibles pour les abonnés plan 1 et plan 2.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-231">The procedures for quarantined files in this section are available only to ATP Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="6d8f8-232">Dans les organisations avec ATP, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-232">In organizations with ATP, admins can managed quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="6d8f8-233">Afficher les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-233">View quarantined files</span></span>

1. <span data-ttu-id="6d8f8-234">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-234">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="6d8f8-235">Modifier la **vue mise en quarantaine** sur les **fichiers**de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-235">Change **View quarantined** to the default value **files**.</span></span> <span data-ttu-id="6d8f8-236">Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-236">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="6d8f8-237">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-237">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="6d8f8-238">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-238">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="6d8f8-239">Les colonnes par défaut sont marquées d’un<sup>\*</sup>astérisque () :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-239">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="6d8f8-240">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-240">**User**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-241">**Emplacements**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-241">**Location**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-242">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-242">**File name**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-243">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-243">**File URL**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-244">**Taille de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-244">**File Size**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-245">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-245">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-246">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="6d8f8-246">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="6d8f8-247">**Détectés par**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-247">**Detected by**</span></span>

   - <span data-ttu-id="6d8f8-248">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-248">**Modified by time**</span></span>

4. <span data-ttu-id="6d8f8-249">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-249">To filter the results, click **Filter**.</span></span> <span data-ttu-id="6d8f8-250">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-250">The available filters are:</span></span>

   - <span data-ttu-id="6d8f8-251">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-251">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="6d8f8-252">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-252">**Today**</span></span>

     - <span data-ttu-id="6d8f8-253">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-253">**Next 2 days**</span></span>

     - <span data-ttu-id="6d8f8-254">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-254">**Next 7 days**</span></span>

     - <span data-ttu-id="6d8f8-255">Une plage date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-255">A custom date/time range.</span></span>

   - <span data-ttu-id="6d8f8-256">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-256">**Received time**</span></span>

   - <span data-ttu-id="6d8f8-257">**Raison**de la mise en quarantaine : la seule valeur disponible est **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-257">**Quarantine reason**: The only available value is **Malware**.</span></span>

<span data-ttu-id="6d8f8-258">Une fois que vous avez trouvé un fichier en quarantaine spécifique, sélectionnez le fichier pour en afficher les détails et effectuer une action (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-258">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-file-results"></a><span data-ttu-id="6d8f8-259">Exporter les résultats des fichiers</span><span class="sxs-lookup"><span data-stu-id="6d8f8-259">Export file results</span></span>

1. <span data-ttu-id="6d8f8-260">Sélectionnez les fichiers qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-260">Select the files you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="6d8f8-261">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-261">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="6d8f8-262">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-262">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="6d8f8-263">Afficher les détails des fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-263">View quarantined file details</span></span>

<span data-ttu-id="6d8f8-264">Lorsque vous sélectionnez un fichier dans la liste, les détails de fichier suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-264">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="6d8f8-265">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-265">**File Name**</span></span>

- <span data-ttu-id="6d8f8-266">**URL du fichier**: URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-266">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>

- <span data-ttu-id="6d8f8-267">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-267">**Malicious content detected on** The date/time the file was quarantined.</span></span>

- <span data-ttu-id="6d8f8-268">**Expire**: date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-268">**Expires**: The date when the file will be deleted from quarantine.</span></span>

- <span data-ttu-id="6d8f8-269">**Détecté par**: ATP (protection avancée contre les menaces) ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-269">**Detected By**: ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span>

- <span data-ttu-id="6d8f8-270">**Déplacer ?**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-270">**Released?**</span></span>

- <span data-ttu-id="6d8f8-271">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-271">**Malware Name**</span></span>

- <span data-ttu-id="6d8f8-272">**ID de document**: identificateur unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-272">**Document ID**: A unique identifier for the document.</span></span>

- <span data-ttu-id="6d8f8-273">**Taille du fichier**: en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-273">**File Size**: In kilobytes (KB).</span></span>

- <span data-ttu-id="6d8f8-274">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-274">**Organization** Your organization's unique ID.</span></span>

- <span data-ttu-id="6d8f8-275">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-275">**Last modified**</span></span>

- <span data-ttu-id="6d8f8-276">**Modifié par**: utilisateur qui a modifié le fichier pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-276">**Modified By**: The user who last modified the file.</span></span>

- <span data-ttu-id="6d8f8-277">**Valeur 256-bit (SHA-256) de l’algorithme de hachage sécurisé**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou dans d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-277">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="6d8f8-278">Effectuer des actions sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-278">Take action on quarantined files</span></span>

<span data-ttu-id="6d8f8-279">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez effectuer les actions suivantes sur le fichier dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-279">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="6d8f8-280">**Fichiers de version**: sélectionnez (par défaut) ou désélectionnez **les fichiers de rapports à Microsoft pour analyse**, puis cliquez sur **libérer les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-280">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>

- <span data-ttu-id="6d8f8-281">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-281">**Download file**</span></span>

- <span data-ttu-id="6d8f8-282">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-282">**Remove file from quarantine**</span></span>

<span data-ttu-id="6d8f8-283">Si vous ne libérez pas ou ne supprimez pas les fichiers, ils seront supprimés une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-283">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="6d8f8-284">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-284">Actions on multiple quarantined files</span></span>

<span data-ttu-id="6d8f8-285">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-285">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="6d8f8-286">**Fichiers de version**</span><span class="sxs-lookup"><span data-stu-id="6d8f8-286">**Release files**</span></span>

- <span data-ttu-id="6d8f8-287">**Supprimer des fichiers**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-287">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

1. <span data-ttu-id="6d8f8-288">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général (ou des rôles de centre de sécurité & conformité appropriés) dans votre organisation, connectez-vous et [accédez au centre de sécurité & conformité](../../compliance/go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f8-288">Using a work or school account that has global administrator privileges (or appropriate Security & Compliance Center roles) in your organization, sign in and [go to the Security & Compliance Center](../../compliance/go-to-the-securitycompliance-center.md).</span></span>

## <a name="use-exchange-online-powershell-or-standalone-exchange-online-protection-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="6d8f8-289">Utiliser Exchange Online PowerShell ou un environnement Exchange Online Protection PowerShell autonome pour afficher et gérer les messages et fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6d8f8-289">Use Exchange Online PowerShell or standalone Exchange Online Protection PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="6d8f8-290">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d8f8-290">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="6d8f8-291">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="6d8f8-291">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/delete-quarantinemessage)

- [<span data-ttu-id="6d8f8-292">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="6d8f8-292">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/export-quarantinemessage)

- [<span data-ttu-id="6d8f8-293">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="6d8f8-293">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage)

- <span data-ttu-id="6d8f8-294">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Notez que cette applet de commande concerne uniquement les messages, pas les fichiers de programmes malveillants, pour SharePoint Online, OneDrive entreprise ou Teams.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-294">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from ATP for SharePoint Online, OneDrive for Business, or Teams.</span></span>

- [<span data-ttu-id="6d8f8-295">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="6d8f8-295">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage)
