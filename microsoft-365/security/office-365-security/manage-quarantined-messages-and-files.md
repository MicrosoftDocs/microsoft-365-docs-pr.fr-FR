---
title: Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365
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
ms.openlocfilehash: fdab820d2ccedaf8e4f51ba71b15d2c807d06dd1
ms.sourcegitcommit: fe4beef350ef9f39b1098755cff46fa2b8e7dc4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2020
ms.locfileid: "42857072"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-office-365"></a><span data-ttu-id="25b4b-104">Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="25b4b-104">Manage quarantined messages and files as an admin in Office 365</span></span>

<span data-ttu-id="25b4b-105">La mise en quarantaine bloque les messages potentiellement dangereux ou indésirables dans les organisations Office 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="25b4b-105">Quarantine holds potentially dangerous or unwanted messages in Office 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="25b4b-106">Pour plus d’informations, consultez la rubrique [mise en quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="25b4b-106">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="25b4b-107">Les administrateurs peuvent afficher, publier et supprimer tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="25b4b-107">Admins can view, release, and delete all types of quarantined messages for all users.</span></span> <span data-ttu-id="25b4b-108">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants, le hameçonnage à haute fiabilité ou à la suite de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="25b4b-108">Only admins can manage messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="25b4b-109">Les administrateurs peuvent également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25b4b-109">Admins can also report false positives to Microsoft.</span></span>

<span data-ttu-id="25b4b-110">Les administrateurs dans les organisations disposant d’Office 365 Advanced Threat Protection (ATP) peuvent également afficher, télécharger et supprimer des fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="25b4b-110">Admins in organizations with Office 365 Advance Threat Protection (ATP) can also view, download, and delete quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="25b4b-111">Vous pouvez afficher et gérer les messages mis en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (les clients Exchange Online PowerShell pour Office 365 ; Exchange Online Protection PowerShell pour les clients EOP autonomes).</span><span class="sxs-lookup"><span data-stu-id="25b4b-111">You view and manage quarantined messages in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Office 365 customers; Exchange Online Protection PowerShell for standalone EOP customers).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="25b4b-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="25b4b-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="25b4b-113">Pour ouvrir le centre de sécurité & conformité d’Office 365, <https://protection.office.com>accédez à.</span><span class="sxs-lookup"><span data-stu-id="25b4b-113">To open the Office 365 Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="25b4b-114">Pour ouvrir la page de mise en quarantaine directement, <https://protection.office.com/quarantine>accédez à.</span><span class="sxs-lookup"><span data-stu-id="25b4b-114">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="25b4b-115">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="25b4b-115">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="25b4b-116">Pour vous connecter à Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="25b4b-116">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="25b4b-117">Vous devez disposer d’autorisations pour pouvoir gérer la mise en quarantaine en tant qu’administrateur. Les autorisations sont contrôlées par le rôle de **mise en quarantaine** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="25b4b-117">You need to be assigned permissions before you can manage the quarantine as an admin. The permissions are controlled by the **Quarantine** role in the Security & Compliance Center.</span></span> <span data-ttu-id="25b4b-118">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l' **organisation** (administrateurs globaux), administrateur de **mise en quarantaine**et administrateur de **sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="25b4b-118">By default, this role is assigned to the **Organization Management** (Global admins), **Quarantine Administrator**, and **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="25b4b-119">Pour plus d’informations, consultez [la rubrique autorisations dans le centre de conformité & Office 365 Security](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="25b4b-119">For more information, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="25b4b-120">Les messages mis en quarantaine sont conservés pendant une période de temps par défaut avant d’être supprimés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="25b4b-120">Quarantined messages are retained for a default period of time before they're automatically deleted:</span></span>

  - <span data-ttu-id="25b4b-121">Messages mis en quarantaine par des stratégies de blocage du courrier indésirable (courrier indésirable, hameçonnage et courrier en masse) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="25b4b-121">Messages quarantined by anti-spam policies (spam, phishing, and bulk email): 30 days.</span></span> <span data-ttu-id="25b4b-122">Il s’agit de la valeur par défaut et la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="25b4b-122">This is the default and maximum value.</span></span> <span data-ttu-id="25b4b-123">Pour configurer cette valeur, consultez la rubrique [configurer des stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="25b4b-123">To configure this value, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

  - <span data-ttu-id="25b4b-124">Messages mis en quarantaine par les règles de flux de messagerie (l’action de la règle **permet de livrer le message à la mise en quarantaine hébergée**) : 30 jours.</span><span class="sxs-lookup"><span data-stu-id="25b4b-124">Messages quarantined by mail flow rules (the rule action is **Deliver the message to the hosted quarantine**): 30 days.</span></span> <span data-ttu-id="25b4b-125">Vous ne pouvez pas modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="25b4b-125">You can't change this value.</span></span>

  - <span data-ttu-id="25b4b-126">Messages contenant des programmes malveillants : 15 jours.</span><span class="sxs-lookup"><span data-stu-id="25b4b-126">Messages that contain malware: 15 days.</span></span>

  <span data-ttu-id="25b4b-127">Lorsqu’un message arrive à expiration en quarantaine, vous ne pouvez pas le récupérer.</span><span class="sxs-lookup"><span data-stu-id="25b4b-127">When a message expires from quarantine, you can't recover it.</span></span>

## <a name="use-the-security--compliance-center-to-manage-quarantined-email-messages"></a><span data-ttu-id="25b4b-128">Utiliser le centre de sécurité & conformité pour gérer les messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-128">Use the Security & Compliance Center to manage quarantined email messages</span></span>

### <a name="view-quarantined-email"></a><span data-ttu-id="25b4b-129">Afficher le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-129">View quarantined email</span></span>

1. <span data-ttu-id="25b4b-130">Dans le centre de sécurité et conformité, accédez à **mise en quarantaine**de la **vérification** \> de la **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="25b4b-130">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="25b4b-131">Vérifiez que l’option **afficher en quarantaine** est définie sur la valeur par défaut **e-mail**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-131">Verify that **View quarantined** is set to the default value **email**.</span></span>

3. <span data-ttu-id="25b4b-132">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="25b4b-132">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="25b4b-133">Cliquez sur **modifier les colonnes** pour afficher un maximum de sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="25b4b-133">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="25b4b-134">Les valeurs par défaut sont indiquées par un astérisque<sup>\*</sup>() :</span><span class="sxs-lookup"><span data-stu-id="25b4b-134">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="25b4b-135">**Ont**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-135">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-136">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-136">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-137">**Objet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-137">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-138">**Raison de la mise en quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-138">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-139">**A?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-139">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-140">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-140">**Policy type**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-141">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-141">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-142">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="25b4b-142">**Recipient**</span></span>

   - <span data-ttu-id="25b4b-143">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="25b4b-143">**Message ID**</span></span>

   - <span data-ttu-id="25b4b-144">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="25b4b-144">**Policy name**</span></span>

   - <span data-ttu-id="25b4b-145">**Size**</span><span class="sxs-lookup"><span data-stu-id="25b4b-145">**Size**</span></span>

   - <span data-ttu-id="25b4b-146">**Direction**</span><span class="sxs-lookup"><span data-stu-id="25b4b-146">**Direction**</span></span>

   <span data-ttu-id="25b4b-147">Lorsque vous avez terminé, cliquez sur **Enregistrer**, ou sur **définir sur par défaut**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-147">When you're finished, click **Save**, or click **Set to default**.</span></span>

4. <span data-ttu-id="25b4b-148">Pour filtrer les résultats, cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-148">To filter the results, click **Filter**.</span></span> <span data-ttu-id="25b4b-149">Les filtres disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="25b4b-149">The available filters are:</span></span>

   - <span data-ttu-id="25b4b-150">**Date d’expiration**: filtre les messages par date de fin de mise en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="25b4b-150">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="25b4b-151">**Sans**</span><span class="sxs-lookup"><span data-stu-id="25b4b-151">**Today**</span></span>

     - <span data-ttu-id="25b4b-152">**2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="25b4b-152">**Next 2 days**</span></span>

     - <span data-ttu-id="25b4b-153">**Les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="25b4b-153">**Next 7 days**</span></span>

     - <span data-ttu-id="25b4b-154">**Personnalisé**: entrez une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-154">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="25b4b-155">**Heure de réception**: entrez une **Date de début** et une date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-155">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="25b4b-156">**Raison**de la mise en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="25b4b-156">**Quarantine reason**:</span></span>

     - <span data-ttu-id="25b4b-157">**Stratégie**: le message correspond aux conditions d’une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="25b4b-157">**Policy**: The message matched the conditions of a mail flow rule (also known as a transport rule).</span></span>

     - <span data-ttu-id="25b4b-158">**Courrier en nombre**</span><span class="sxs-lookup"><span data-stu-id="25b4b-158">**Bulk**</span></span>

     - <span data-ttu-id="25b4b-159">**Jouer**</span><span class="sxs-lookup"><span data-stu-id="25b4b-159">**Phish**</span></span>

     - <span data-ttu-id="25b4b-160">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="25b4b-160">**Malware**</span></span>

     - <span data-ttu-id="25b4b-161">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="25b4b-161">**Spam**</span></span>

     - <span data-ttu-id="25b4b-162">**Hameçonnage à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="25b4b-162">**High Confidence Phish**</span></span>

   - <span data-ttu-id="25b4b-163">**Destinataire du message**: tous les utilisateurs ou seulement les messages qui vous sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="25b4b-163">**Email recipient**: All users or only messages sent to you.</span></span> <span data-ttu-id="25b4b-164">Les utilisateurs finaux peuvent gérer uniquement les messages mis en quarantaine qui leur sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="25b4b-164">End users can only manage quarantined messages sent to them.</span></span>

   <span data-ttu-id="25b4b-165">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-165">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="25b4b-166">Pour masquer le menu volant filtre, cliquez à nouveau sur **filtre** .</span><span class="sxs-lookup"><span data-stu-id="25b4b-166">To hide the filter flyout, click **Filter** again.</span></span>

5. <span data-ttu-id="25b4b-167">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="25b4b-167">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="25b4b-168">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="25b4b-168">Wildcards aren't supported.</span></span> <span data-ttu-id="25b4b-169">Vous pouvez effectuer une recherche à l’aide des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-169">You can search by the following values:</span></span>

   - <span data-ttu-id="25b4b-170">**ID du message**: identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-170">**Message ID**: The globally unique identifier of the message.</span></span>

        <span data-ttu-id="25b4b-171">Par exemple, vous avez utilisé le [suivi des messages](message-trace-scc.md) pour rechercher un message qui a été envoyé à un utilisateur de votre organisation, et vous déterminez que le message a été mis en quarantaine au lieu d’être remis.</span><span class="sxs-lookup"><span data-stu-id="25b4b-171">For example, you used [message trace](message-trace-scc.md) to look for a message that was sent to a user in your organization, and you determine that the message was quarantined instead of delivered.</span></span> <span data-ttu-id="25b4b-172">Veillez à inclure la valeur d’ID de message complète, qui peut inclure des\<\>chevrons ().</span><span class="sxs-lookup"><span data-stu-id="25b4b-172">Be sure to include the full message ID value, which might include angle brackets (\<\>).</span></span> <span data-ttu-id="25b4b-173">Par exemple : `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span><span class="sxs-lookup"><span data-stu-id="25b4b-173">For example: `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`.</span></span>

   - <span data-ttu-id="25b4b-174">**Adresse de messagerie**de l’expéditeur : adresse de messagerie de l’expéditeur unique.</span><span class="sxs-lookup"><span data-stu-id="25b4b-174">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="25b4b-175">**Adresse de messagerie du destinataire**: adresse de messagerie d’un destinataire unique.</span><span class="sxs-lookup"><span data-stu-id="25b4b-175">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="25b4b-176">**Objet**: utilisez tout l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-176">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="25b4b-177">La recherche ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="25b4b-177">The search is not case-sensitive.</span></span>

   <span data-ttu-id="25b4b-178">Une fois que vous avez entré les critères de ![recherche,](../media/scc-quarantine-refresh.png) cliquez sur Actualiser le bouton **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="25b4b-178">After you've entered the search criteria, click ![Refresh button](../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="25b4b-179">Une fois que vous avez trouvé un message en quarantaine spécifique, sélectionnez le message pour en afficher les détails et prendre des mesures (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="25b4b-179">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-message-results"></a><span data-ttu-id="25b4b-180">Exporter les résultats du message</span><span class="sxs-lookup"><span data-stu-id="25b4b-180">Export message results</span></span>

1. <span data-ttu-id="25b4b-181">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-181">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="25b4b-182">Cliquez sur **Oui** dans le message de confirmation qui vous signale que la fenêtre du navigateur doit rester ouverte.</span><span class="sxs-lookup"><span data-stu-id="25b4b-182">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="25b4b-183">Lorsque votre exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="25b4b-183">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-message-details"></a><span data-ttu-id="25b4b-184">Afficher les détails du message en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-184">View quarantined message details</span></span>

<span data-ttu-id="25b4b-185">Lorsque vous sélectionnez un message électronique dans la liste, les détails du message suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="25b4b-185">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="25b4b-186">**ID du message**: identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-186">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="25b4b-187">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="25b4b-187">**Sender address**</span></span>

- <span data-ttu-id="25b4b-188">**Received**: date/heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-188">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="25b4b-189">**Subject**</span><span class="sxs-lookup"><span data-stu-id="25b4b-189">**Subject**</span></span>

- <span data-ttu-id="25b4b-190">**Raison**de la mise en quarantaine : indique si un message a été identifié **Bulk**comme **courrier indésirable**, **hameçon, hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-190">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule (**Transport rule**), or was identified as containing **Malware**.</span></span>

- <span data-ttu-id="25b4b-191">**Recipients**: si le message contient plusieurs destinataires, vous devez cliquer sur **preview message** ou **View message Header** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="25b4b-191">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="25b4b-192">**Expire**: date/heure à laquelle le message sera automatiquement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="25b4b-192">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="25b4b-193">**Diffusé à** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été diffusé.</span><span class="sxs-lookup"><span data-stu-id="25b4b-193">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="25b4b-194">**Pas encore publié à**: toutes les adresses de messagerie (le cas échéant) auxquelles le message n’a pas encore été publié.</span><span class="sxs-lookup"><span data-stu-id="25b4b-194">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="25b4b-195">Effectuer une action sur le courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-195">Take action on quarantined email</span></span>

<span data-ttu-id="25b4b-196">Une fois que vous avez sélectionné un message, vous disposez de plusieurs options pour effectuer les messages dans le volet de la fenêtre de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="25b4b-196">After you select a message, you have several options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="25b4b-197">**Message de publication**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-197">**Release message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="25b4b-198">**Signaler les messages à Microsoft pour analyse**: cette option est sélectionnée par défaut et signale le message en quarantaine à Microsoft comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="25b4b-198">**Report messages to Microsoft for analysis**: This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span> <span data-ttu-id="25b4b-199">Si le message a été mis en quarantaine en tant que courrier indésirable, en masse, hameçonnage ou contenant un programme malveillant, le message est également signalé à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25b4b-199">If the message was quarantined as spam, bulk, phishing, or containing malware, the message is also reported to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="25b4b-200">En fonction de leur analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-200">Depending on their analysis, the service-wide spam filter rules might be be adjusted to allow the message through.</span></span>

  - <span data-ttu-id="25b4b-201">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-201">Choose one of the following options:</span></span>

    - <span data-ttu-id="25b4b-202">**Diffuser les messages à tous les destinataires**</span><span class="sxs-lookup"><span data-stu-id="25b4b-202">**Release messages to all recipients**</span></span>

    - <span data-ttu-id="25b4b-203">**Publier des messages à des destinataires spécifiques**</span><span class="sxs-lookup"><span data-stu-id="25b4b-203">**Release messages to specific recipients**</span></span>

    - <span data-ttu-id="25b4b-204">**Publier des messages vers d’autres personnes**</span><span class="sxs-lookup"><span data-stu-id="25b4b-204">**Release messages to other people**</span></span>

  <span data-ttu-id="25b4b-205">Lorsque vous avez terminé, cliquez sur **publier les messages**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-205">When you're finished, click **Release messages**.</span></span>

  <span data-ttu-id="25b4b-206">Remarques sur la libération des messages :</span><span class="sxs-lookup"><span data-stu-id="25b4b-206">Notes about releasing messages:</span></span>

  - <span data-ttu-id="25b4b-207">Vous ne pouvez pas diffuser un message au même destinataire plus d’une fois.</span><span class="sxs-lookup"><span data-stu-id="25b4b-207">You can't release a message to the same recipient more than once.</span></span>

  - <span data-ttu-id="25b4b-208">Seuls les destinataires qui n’ont pas reçu le message s’affichent dans la liste des destinataires potentiels.</span><span class="sxs-lookup"><span data-stu-id="25b4b-208">Only recipients who haven't received the message will appear in the list of potential recipients.</span></span>

- <span data-ttu-id="25b4b-209">**Afficher l’en-tête**du message : cliquez sur ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="25b4b-209">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="25b4b-210">Pour analyser les champs d’en-tête et les valeurs en profondeur, copiez le texte de l’en-tête du message dans votre presse-papiers, puis choisissez **analyseur d’en-têtes de message Microsoft** pour accéder à l’analyseur de connectivité à distance (cliquez avec le bouton droit et choisissez **ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Office 365 pour effectuer cette tâche).</span><span class="sxs-lookup"><span data-stu-id="25b4b-210">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Office 365 to complete this task).</span></span> <span data-ttu-id="25b4b-211">Collez l’en-tête du message sur la page dans la section analyseur d’en-têtes de message, puis choisissez **analyser les en-têtes**:</span><span class="sxs-lookup"><span data-stu-id="25b4b-211">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="25b4b-212">**Afficher un aperçu du message**: dans le volet flyout qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-212">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="25b4b-213">**Mode Source**: affiche la version HTML du corps du message avec tous les liens désactivés.</span><span class="sxs-lookup"><span data-stu-id="25b4b-213">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="25b4b-214">**Affichage de texte**: affiche le corps du message en texte brut.</span><span class="sxs-lookup"><span data-stu-id="25b4b-214">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="25b4b-215">**Supprimer de la quarantaine**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="25b4b-215">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted without being sent to the original recipients.</span></span>

- <span data-ttu-id="25b4b-216">**Message de téléchargement**: dans le volet flyout qui apparaît, sélectionnez **je comprends les risques du téléchargement de ce message** pour enregistrer une copie locale du message au format. eml.</span><span class="sxs-lookup"><span data-stu-id="25b4b-216">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="25b4b-217">**Envoyer un message**: dans le volet flyout qui apparaît, choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-217">**Submit message**: In the flyout pane that appears, choose the following options:</span></span>

  - <span data-ttu-id="25b4b-218">**Type d’objet**: **e-mail** (par défaut), **URL**ou **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-218">**Object type**: **Email** (default), **URL**, or **Attachment**.</span></span>

  - <span data-ttu-id="25b4b-219">**Format d’envoi**: **ID de message réseau** (par défaut, avec la valeur correspondante dans la zone **ID de message réseau** ) ou **fichier** (accédez à un fichier. eml ou. MSG local).</span><span class="sxs-lookup"><span data-stu-id="25b4b-219">**Submission format**: **Network Message ID** (default, with the corresponding value in the **Network Message ID** box) or **File** (browse to a local .eml or .msg file).</span></span> <span data-ttu-id="25b4b-220">Notez que si vous sélectionnez **fichier** , puis **ID de message réseau**, la valeur initiale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="25b4b-220">Note that if you select **File** and then select **Network Message ID**, the initially value is gone.</span></span>

  - <span data-ttu-id="25b4b-221">**Destinataires**: saisissez au bail d’un destinataire d’origine du message, ou cliquez sur **Sélectionner tout** pour identifier tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="25b4b-221">**Recipients**: Type at lease one original recipient of the message, or click **Select All** to identify all recipients.</span></span> <span data-ttu-id="25b4b-222">Vous pouvez également cliquer sur **Sélectionner tout** , puis supprimer des destinataires de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="25b4b-222">You can also click **Select All** and then selectively remove individual recipients.</span></span>

  - <span data-ttu-id="25b4b-223">**Raison du dépôt**: **ne doit pas avoir été bloqué** (par défaut) ou **doit avoir été bloqué**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-223">**Reason for submission**: **Should not have been blocked** (default) or **Should have been blocked**.</span></span>

  <span data-ttu-id="25b4b-224">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-224">When you're finished, click **Submit**.</span></span>

<span data-ttu-id="25b4b-225">Si vous ne libérez pas ou ne supprimez pas le message, il sera supprimé une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="25b4b-225">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="25b4b-226">Effectuer une action sur plusieurs messages électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-226">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="25b4b-227">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-227">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="25b4b-228">**Messages de publication**: les options sont les mêmes que lorsque vous libérez un seul message, sauf que vous ne pouvez pas sélectionner les **messages de publication à des destinataires spécifiques**; vous pouvez uniquement sélectionner **publier le message à tous les destinataires** ou **publier des messages à d’autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-228">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="25b4b-229">**Supprimer des messages**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, le message est immédiatement supprimé sans être envoyé aux destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="25b4b-229">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="25b4b-230">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-230">When you're finished, click **Close**.</span></span>

## <a name="atp-only-use-the-security--compliance-center-to-manage-quarantined-files"></a><span data-ttu-id="25b4b-231">ATP uniquement : utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-231">ATP Only: Use the Security & Compliance Center to manage quarantined files</span></span>

> [!NOTE]
> <span data-ttu-id="25b4b-232">Les procédures des fichiers mis en quarantaine dans cette section sont uniquement disponibles pour les abonnés plan 1 et plan 2.</span><span class="sxs-lookup"><span data-stu-id="25b4b-232">The procedures for quarantined files in this section are available only to ATP Plan 1 and Plan 2 subscribers.</span></span>

<span data-ttu-id="25b4b-233">Dans les organisations avec ATP, les administrateurs peuvent gérer les fichiers mis en quarantaine dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="25b4b-233">In organizations with ATP, admins can managed quarantined files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

### <a name="view-quarantined-files"></a><span data-ttu-id="25b4b-234">Afficher les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-234">View quarantined files</span></span>

1. <span data-ttu-id="25b4b-235">Dans le centre de sécurité et conformité, accédez à **mise en quarantaine**de la **vérification** \> de la **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="25b4b-235">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="25b4b-236">Modifier la **vue mise en quarantaine** sur les **fichiers**de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="25b4b-236">Change **View quarantined** to the default value **files**.</span></span> <span data-ttu-id="25b4b-237">Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="25b4b-237">You can sort on a field by clicking on an available column header.</span></span>

3. <span data-ttu-id="25b4b-238">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="25b4b-238">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="25b4b-239">Cliquez sur **modifier les colonnes** pour afficher un maximum de sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="25b4b-239">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="25b4b-240">Les colonnes par défaut sont marquées d’un<sup>\*</sup>astérisque () :</span><span class="sxs-lookup"><span data-stu-id="25b4b-240">The default columns are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="25b4b-241">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-241">**User**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-242">**Emplacements**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-242">**Location**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-243">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-243">**File name**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-244">**URL du fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-244">**File URL**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-245">**Taille de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-245">**File Size**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-246">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-246">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-247">**A?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="25b4b-247">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="25b4b-248">**Détectés par**</span><span class="sxs-lookup"><span data-stu-id="25b4b-248">**Detected by**</span></span>

   - <span data-ttu-id="25b4b-249">**Modifié par heure**</span><span class="sxs-lookup"><span data-stu-id="25b4b-249">**Modified by time**</span></span>

4. <span data-ttu-id="25b4b-250">Pour filtrer les résultats, cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-250">To filter the results, click **Filter**.</span></span> <span data-ttu-id="25b4b-251">Les filtres disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="25b4b-251">The available filters are:</span></span>

   - <span data-ttu-id="25b4b-252">**Date d’expiration**: filtre les messages par date de fin de mise en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="25b4b-252">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="25b4b-253">**Sans**</span><span class="sxs-lookup"><span data-stu-id="25b4b-253">**Today**</span></span>

     - <span data-ttu-id="25b4b-254">**2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="25b4b-254">**Next 2 days**</span></span>

     - <span data-ttu-id="25b4b-255">**Les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="25b4b-255">**Next 7 days**</span></span>

     - <span data-ttu-id="25b4b-256">Une plage date/heure personnalisée.</span><span class="sxs-lookup"><span data-stu-id="25b4b-256">A custom date/time range.</span></span>

   - <span data-ttu-id="25b4b-257">**Heure de réception**</span><span class="sxs-lookup"><span data-stu-id="25b4b-257">**Received time**</span></span>

   - <span data-ttu-id="25b4b-258">**Raison**de la mise en quarantaine : la seule valeur disponible est **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-258">**Quarantine reason**: The only available value is **Malware**.</span></span>

<span data-ttu-id="25b4b-259">Une fois que vous avez trouvé un fichier en quarantaine spécifique, sélectionnez le fichier pour en afficher les détails et effectuer une action (par exemple, afficher, publier, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="25b4b-259">After you find a specific quarantined file, select the file to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

#### <a name="export-file-results"></a><span data-ttu-id="25b4b-260">Exporter les résultats des fichiers</span><span class="sxs-lookup"><span data-stu-id="25b4b-260">Export file results</span></span>

1. <span data-ttu-id="25b4b-261">Sélectionnez les fichiers qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-261">Select the files you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="25b4b-262">Cliquez sur **Oui** dans le message de confirmation qui vous signale que la fenêtre du navigateur doit rester ouverte.</span><span class="sxs-lookup"><span data-stu-id="25b4b-262">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="25b4b-263">Lorsque votre exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="25b4b-263">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

#### <a name="view-quarantined-file-details"></a><span data-ttu-id="25b4b-264">Afficher les détails des fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-264">View quarantined file details</span></span>

<span data-ttu-id="25b4b-265">Lorsque vous sélectionnez un fichier dans la liste, les détails de fichier suivants s’affichent dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="25b4b-265">When you select a file in the list, the following file details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="25b4b-266">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="25b4b-266">**File Name**</span></span>

- <span data-ttu-id="25b4b-267">**URL du fichier**: URL qui définit l’emplacement du fichier (par exemple, dans SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="25b4b-267">**File URL**: URL that defines the location of the file (for example, in SharePoint Online).</span></span>

- <span data-ttu-id="25b4b-268">**Contenu malveillant détecté sur** Date/heure de mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="25b4b-268">**Malicious content detected on** The date/time the file was quarantined.</span></span>

- <span data-ttu-id="25b4b-269">**Expire**: date à laquelle le fichier sera supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="25b4b-269">**Expires**: The date when the file will be deleted from quarantine.</span></span>

- <span data-ttu-id="25b4b-270">**Détecté par**: ATP (protection avancée contre les menaces) ou le moteur anti-programme malveillant de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25b4b-270">**Detected By**: ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span>

- <span data-ttu-id="25b4b-271">**A?**</span><span class="sxs-lookup"><span data-stu-id="25b4b-271">**Released?**</span></span>

- <span data-ttu-id="25b4b-272">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="25b4b-272">**Malware Name**</span></span>

- <span data-ttu-id="25b4b-273">**ID de document**: identificateur unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="25b4b-273">**Document ID**: A unique identifier for the document.</span></span>

- <span data-ttu-id="25b4b-274">**Taille du fichier**: en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="25b4b-274">**File Size**: In kilobytes (KB).</span></span>

- <span data-ttu-id="25b4b-275">**Organisation** ID unique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="25b4b-275">**Organization** Your organization's unique ID.</span></span>

- <span data-ttu-id="25b4b-276">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="25b4b-276">**Last modified**</span></span>

- <span data-ttu-id="25b4b-277">**Modifié par**: utilisateur qui a modifié le fichier pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="25b4b-277">**Modified By**: The user who last modified the file.</span></span>

- <span data-ttu-id="25b4b-278">**Valeur 256-bit (SHA-256) de l’algorithme de hachage sécurisé**: vous pouvez utiliser cette valeur de hachage pour identifier le fichier dans d’autres magasins de réputation ou dans d’autres emplacements de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="25b4b-278">**Secure Hash Algorithm 256-bit (SHA-256) value**: You can use this hash value to identify the file in other reputation stores or in other locations in your environment.</span></span>

### <a name="take-action-on-quarantined-files"></a><span data-ttu-id="25b4b-279">Effectuer des actions sur les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-279">Take action on quarantined files</span></span>

<span data-ttu-id="25b4b-280">Lorsque vous sélectionnez un fichier dans la liste, vous pouvez effectuer les actions suivantes sur le fichier dans le volet flyout de **Détails** :</span><span class="sxs-lookup"><span data-stu-id="25b4b-280">When you select a file in the list, you can take the following actions on the file in the **Details** flyout pane:</span></span>

- <span data-ttu-id="25b4b-281">**Fichiers de version**: sélectionnez (par défaut) ou désélectionnez **les fichiers de rapports à Microsoft pour analyse**, puis cliquez sur **libérer les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-281">**Release files**: Select (default) or unselect **Report files to Microsoft for analysis**, and then click **Release files**.</span></span>

- <span data-ttu-id="25b4b-282">**Télécharger un fichier**</span><span class="sxs-lookup"><span data-stu-id="25b4b-282">**Download file**</span></span>

- <span data-ttu-id="25b4b-283">**Supprimer le fichier de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="25b4b-283">**Remove file from quarantine**</span></span>

<span data-ttu-id="25b4b-284">Si vous ne libérez pas ou ne supprimez pas les fichiers, ils seront supprimés une fois la période de rétention de quarantaine par défaut expirée.</span><span class="sxs-lookup"><span data-stu-id="25b4b-284">If you don't release or remove the files, they will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="actions-on-multiple-quarantined-files"></a><span data-ttu-id="25b4b-285">Actions sur plusieurs fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-285">Actions on multiple quarantined files</span></span>

<span data-ttu-id="25b4b-286">Lorsque vous sélectionnez plusieurs fichiers mis en quarantaine dans la liste (jusqu’à 100), le volet flyout **actions en bloc** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-286">When you select multiple quarantined files in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="25b4b-287">**Fichiers de version**</span><span class="sxs-lookup"><span data-stu-id="25b4b-287">**Release files**</span></span>

- <span data-ttu-id="25b4b-288">**Supprimer des fichiers**: après avoir cliqué sur **Oui** dans le message d’avertissement qui s’affiche, les fichiers sont immédiatement supprimés.</span><span class="sxs-lookup"><span data-stu-id="25b4b-288">**Delete files**:  After you click **Yes** in the warning that appears, the files are immediately deleted.</span></span>

<span data-ttu-id="25b4b-289">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="25b4b-289">When you're finished, click **Close**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-exchange-online-protection-powershell-to-view-and-manage-quarantined-messages-and-files"></a><span data-ttu-id="25b4b-290">Utiliser Exchange Online PowerShell ou un environnement Exchange Online Protection PowerShell autonome pour afficher et gérer les messages et fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="25b4b-290">Use Exchange Online PowerShell or standalone Exchange Online Protection PowerShell to view and manage quarantined messages and files</span></span>

<span data-ttu-id="25b4b-291">Les cmdlets que vous utilisez pour afficher et gérer les messages et les fichiers en quarantaine sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b4b-291">The cmdlets you use to view and manages messages and files in quarantine are:</span></span>

- [<span data-ttu-id="25b4b-292">Delete-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="25b4b-292">Delete-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/delete-quarantinemessage)

- [<span data-ttu-id="25b4b-293">Export-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="25b4b-293">Export-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/export-quarantinemessage)

- [<span data-ttu-id="25b4b-294">Get-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="25b4b-294">Get-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage)

- <span data-ttu-id="25b4b-295">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Notez que cette applet de commande concerne uniquement les messages, pas les fichiers de programmes malveillants, pour SharePoint Online, OneDrive entreprise ou Teams.</span><span class="sxs-lookup"><span data-stu-id="25b4b-295">[Preview-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/preview-quarantinemessage): Note that this cmdlet is only for messages, not malware files from ATP for SharePoint Online, OneDrive for Business, or Teams.</span></span>

- [<span data-ttu-id="25b4b-296">Release-QuarantineMessage</span><span class="sxs-lookup"><span data-stu-id="25b4b-296">Release-QuarantineMessage</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage)
