---
title: Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez découvrir comment afficher et gérer les messages mis en quarantaine dans le Centre de sécurité et de conformité dans Microsoft 365.
ms.openlocfilehash: ff6cb3dbf9a0a2010bf792115c53265689873090
ms.sourcegitcommit: 614666afb104fc97acb4a2ee5577ef63c0de153a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2020
ms.locfileid: "44173379"
---
# <a name="find-and-release-quarantined-messages-as-a-user"></a><span data-ttu-id="a5013-103">Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5013-103">Find and release quarantined messages as a user</span></span>

<span data-ttu-id="a5013-104">La quarantaine contient des messages potentiellement dangereux ou indésirables dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a5013-104">Quarantine holds potentially dangerous or unwanted messages in Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="a5013-105">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a5013-105">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="a5013-106">En tant qu'utilisateur, vous pouvez afficher, déplacer et supprimer les messages mis en quarantaine car considérés comme du courrier indésirable ou des e-mails de masse, si vous en êtes le destinataire.</span><span class="sxs-lookup"><span data-stu-id="a5013-106">As a user, you can view, release, and delete quarantined messages where you are a recipient, and the message was quarantined as spam or bulk email.</span></span> <span data-ttu-id="a5013-107">Depuis le 2020 avril, vous pouvez afficher ou supprimer les messages hameçonnage mis en quarantaine (pas d'hameçonnage de haute confiance) auxquels vous êtes destinataire.</span><span class="sxs-lookup"><span data-stu-id="a5013-107">As of April 2020, you can view or delete quarantined phishing (not high confidence phishing) messages where you are a recipient.</span></span> <span data-ttu-id="a5013-108">Vous pouvez afficher et gérer vos messages mis en quarantaine dans le centre de sécurité et de conformité ou (si un administrateur a utilisé cette configuration) dans les [notifications de courrier indésirable de l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a5013-108">You view and manage your quarantined messages in the Security & Compliance Center or (if an admin has set this up) in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a5013-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a5013-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a5013-110">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="a5013-110">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="a5013-111">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="a5013-111">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="a5013-112">Les administrateurs peuvent configurer la durée pendant laquelle les messages sont conservés dans la quarantaine avant d’être définitivement supprimés (stratégies anti-courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="a5013-112">Admins can configure how long messages are kept in quarantine before they're permanently deleted (anti-spam policies).</span></span> <span data-ttu-id="a5013-113">Les messages dont la mise en quarantaine est arrivée à expiration ne peuvent pas être récupérés.</span><span class="sxs-lookup"><span data-stu-id="a5013-113">Messages that have expired from quarantine are unrecoverable.</span></span> <span data-ttu-id="a5013-114">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a5013-114">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="a5013-115">Les administrateurs peuvent également [activer les notifications de courrier indésirable pour l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5013-115">Admins can also [enable end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) in anti-spam policies.</span></span> <span data-ttu-id="a5013-116">Les utilisateurs peuvent débloquer les messages mis en quarantaine pour cause de courrier indésirable, directement à partir de ces notifications, mais ils ne peuvent pas débloquer les messages mis en quarantaine pour hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a5013-116">Users can release spam quarantined messages but not phish quarantined messages directly from these notifications.</span></span> <span data-ttu-id="a5013-117">Si vous souhaitez en savoir plus, consultez l’article [Notifications de courrier indésirable pour l’utilisateur final dans Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a5013-117">For more information, see [End-user spam notifications in Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

- <span data-ttu-id="a5013-118">Les messages mis en quarantaine car considérés comme de l’hameçonnage, des programmes malveillants ou par règles de flux de messagerie (également appelés règles de transport) ne sont disponibles que pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="a5013-118">Messages that were quarantined for high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="a5013-119">Les messages de hameçonnage peuvent être examinés par les utilisateurs, mais publiés uniquement par les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="a5013-119">Phish messages can be reviewed by users but only released by admins.</span></span> <span data-ttu-id="a5013-120">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="a5013-120">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="a5013-121">Vous ne pouvez déplacer un message et le signaler comme faux positif (légitime) qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a5013-121">You can only release a message and report it as a false positive (not junk) once.</span></span>

## <a name="view-your-quarantined-messages"></a><span data-ttu-id="a5013-122">Afficher les messages en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a5013-122">View your quarantined messages</span></span>

1. <span data-ttu-id="a5013-123">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="a5013-123">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="a5013-124">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="a5013-124">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="a5013-125">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="a5013-125">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="a5013-126">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="a5013-126">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="a5013-127">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-127">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-128">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-128">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-129">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-129">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-130">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-130">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-131">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-131">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-132">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-132">**Policy type**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-133">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a5013-133">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="a5013-134">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="a5013-134">**Recipient**</span></span>

   - <span data-ttu-id="a5013-135">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="a5013-135">**Message ID**</span></span>

   - <span data-ttu-id="a5013-136">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="a5013-136">**Policy name**</span></span>

   - <span data-ttu-id="a5013-137">**Taille**</span><span class="sxs-lookup"><span data-stu-id="a5013-137">**Size**</span></span>

   - <span data-ttu-id="a5013-138">**Direction**</span><span class="sxs-lookup"><span data-stu-id="a5013-138">**Direction**</span></span>

   <span data-ttu-id="a5013-139">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="a5013-139">When you're finished, click **Save**, or click **Set to default**.</span></span>

3. <span data-ttu-id="a5013-140">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a5013-140">To filter the results, click **Filter**.</span></span> <span data-ttu-id="a5013-141">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="a5013-141">The available filters are:</span></span>

   - <span data-ttu-id="a5013-142">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a5013-142">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="a5013-143">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="a5013-143">**Today**</span></span>

     - <span data-ttu-id="a5013-144">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a5013-144">**Next 2 days**</span></span>

     - <span data-ttu-id="a5013-145">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a5013-145">**Next 7 days**</span></span>

     - <span data-ttu-id="a5013-146">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a5013-146">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a5013-147">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a5013-147">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a5013-148">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="a5013-148">**Quarantine reason**:</span></span>

     - <span data-ttu-id="a5013-149">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="a5013-149">**Bulk**</span></span>

     - <span data-ttu-id="a5013-150">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a5013-150">**Spam**</span></span>

     - <span data-ttu-id="a5013-151">**Hameçonnage** (à partir d’avril 2020)</span><span class="sxs-lookup"><span data-stu-id="a5013-151">**Phish** (As of April, 2020)</span></span>

   <span data-ttu-id="a5013-152">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="a5013-152">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="a5013-153">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a5013-153">To hide the filter flyout, click **Filter** again.</span></span>

4. <span data-ttu-id="a5013-154">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a5013-154">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="a5013-155">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a5013-155">Wildcards aren't supported.</span></span> <span data-ttu-id="a5013-156">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5013-156">You can search by the following values:</span></span>

   - <span data-ttu-id="a5013-157">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="a5013-157">**Message ID**: The globally unique identifier of the message.</span></span> <span data-ttu-id="a5013-158">Si vous sélectionnez un message dans la liste, la valeur **ID du message** apparaît dans le volet déroulant **Détails** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5013-158">If you select a message in the list, the **Message ID** value appears in the **Details** flyout pane that appears.</span></span> <span data-ttu-id="a5013-159">Les administrateurs peuvent utiliser le [suivi des messages](message-trace-scc.md) pour rechercher les messages et les valeurs d’ID de message correspondantes.</span><span class="sxs-lookup"><span data-stu-id="a5013-159">Admins can use [message trace](message-trace-scc.md) to find messages and their corresponding Message ID values.</span></span>

   - <span data-ttu-id="a5013-160">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a5013-160">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="a5013-161">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="a5013-161">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="a5013-162">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="a5013-162">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="a5013-163">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="a5013-163">The search is not case-sensitive.</span></span>

   <span data-ttu-id="a5013-164">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="a5013-164">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="a5013-165">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="a5013-165">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

### <a name="export-message-results"></a><span data-ttu-id="a5013-166">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="a5013-166">Export message results</span></span>

1. <span data-ttu-id="a5013-167">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="a5013-167">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="a5013-168">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="a5013-168">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="a5013-169">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a5013-169">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

### <a name="view-quarantined-message-details"></a><span data-ttu-id="a5013-170">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a5013-170">View quarantined message details</span></span>

<span data-ttu-id="a5013-171">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a5013-171">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a5013-172">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="a5013-172">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="a5013-173">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a5013-173">**Sender address**</span></span>

- <span data-ttu-id="a5013-174">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="a5013-174">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="a5013-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a5013-175">**Subject**</span></span>

- <span data-ttu-id="a5013-176">**Raison de la mise en quarantaine** : indique si un message a été identifié comme **Courrier indésirable**, **E-mail de masse** ou (à partir d’avril 2020) **Hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="a5013-176">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk** or (as of April, 2020) **Phish**.</span></span>

- <span data-ttu-id="a5013-177">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="a5013-177">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="a5013-178">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a5013-178">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="a5013-179">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a5013-179">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="a5013-180">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a5013-180">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="a5013-181">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a5013-181">Take action on quarantined email</span></span>

<span data-ttu-id="a5013-182">Après avoir sélectionné un message, vous pouvez effectuer les actions suivantes dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a5013-182">After you select a message, you have options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a5013-183">**Déplacer le message** : dans le volet déroulant qui s’affiche, indiquez si vous souhaitez **Signaler les messages à Microsoft pour analyse**.</span><span class="sxs-lookup"><span data-stu-id="a5013-183">**Release message**: In the flyout pane that appears, choose whether to **Report messages to Microsoft for analysis**.</span></span> <span data-ttu-id="a5013-184">Cette option est sélectionnée par défaut et signale à Microsoft le message mis en quarantaine par erreur comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="a5013-184">This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span>

  <span data-ttu-id="a5013-185">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="a5013-185">When you're finished, click **Release messages**.</span></span>

- <span data-ttu-id="a5013-186">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="a5013-186">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="a5013-187">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="a5013-187">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="a5013-188">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="a5013-188">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="a5013-189">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5013-189">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="a5013-190">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="a5013-190">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="a5013-191">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="a5013-191">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="a5013-192">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="a5013-192">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="a5013-193">**Supprimer de la quarantaine** : Le message est supprimé dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5013-193">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted.</span></span>

<span data-ttu-id="a5013-194">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a5013-194">When you're finished, click **Close**.</span></span>

<span data-ttu-id="a5013-195">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5013-195">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="a5013-196">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a5013-196">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="a5013-197">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5013-197">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="a5013-198">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="a5013-198">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="a5013-199">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5013-199">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="a5013-200">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a5013-200">When you're finished, click **Close**.</span></span>
