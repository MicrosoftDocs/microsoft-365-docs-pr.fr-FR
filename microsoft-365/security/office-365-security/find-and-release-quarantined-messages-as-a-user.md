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
ms.openlocfilehash: 177f60f1fccc764d74ec0374249a62c602cb84aa
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036511"
---
# <a name="find-and-release-quarantined-messages-as-a-user"></a><span data-ttu-id="c3cbe-103">Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur</span><span class="sxs-lookup"><span data-stu-id="c3cbe-103">Find and release quarantined messages as a user</span></span>

<span data-ttu-id="c3cbe-104">La quarantaine contient des messages potentiellement dangereux ou indésirables dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-104">Quarantine holds potentially dangerous or unwanted messages in Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="c3cbe-105">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-105">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="c3cbe-106">En tant qu'utilisateur, vous pouvez afficher, déplacer et supprimer les messages mis en quarantaine car considérés comme du courrier indésirable, des e-mails de masse, ou (à partir d’avril 2020) de l’hameçonnage, si vous en êtes le destinataire.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-106">As a user, you can view, release, and delete quarantined messages where you are a recipient, and the message was quarantined as spam, bulk email, or (as of April, 2020) phishing.</span></span> <span data-ttu-id="c3cbe-107">Vous pouvez afficher et gérer vos messages mis en quarantaine dans le centre de sécurité et de conformité ou (si un administrateur a utilisé cette configuration) dans les [notifications de courrier indésirable de l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-107">You view and manage your quarantined messages in the Security & Compliance Center or (if an admin has set this up) in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c3cbe-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c3cbe-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c3cbe-109">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-109">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="c3cbe-110">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-110">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="c3cbe-111">Les administrateurs peuvent configurer la durée pendant laquelle les messages sont conservés dans la quarantaine avant d’être définitivement supprimés (stratégies anti-courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-111">Admins can configure how long messages are kept in quarantine before they're permanently deleted (anti-spam policies).</span></span> <span data-ttu-id="c3cbe-112">Les messages dont la mise en quarantaine est arrivée à expiration ne peuvent pas être récupérés.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-112">Messages that have expired from quarantine are unrecoverable.</span></span> <span data-ttu-id="c3cbe-113">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-113">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="c3cbe-114">Les administrateurs peuvent également [activer les notifications de courrier indésirable pour l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-114">Admins can also [enable end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) in anti-spam policies.</span></span> <span data-ttu-id="c3cbe-115">Les utilisateurs peuvent débloquer les messages mis en quarantaine pour cause de courrier indésirable, directement à partir de ces notifications, mais ils ne peuvent pas débloquer les messages mis en quarantaine pour hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-115">Users can release spam quarantined messages but not phish quarantined messages directly from these notifications.</span></span> <span data-ttu-id="c3cbe-116">Si vous souhaitez en savoir plus, consultez l’article [Notifications de courrier indésirable pour l’utilisateur final dans Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-116">For more information, see [End-user spam notifications in Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

- <span data-ttu-id="c3cbe-117">Les messages mis en quarantaine car considérés comme de l’hameçonnage, des programmes malveillants ou par règles de flux de messagerie (également appelés règles de transport) ne sont disponibles que pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-117">Messages that were quarantined for high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="c3cbe-118">Les messages de hameçonnage peuvent être examinés par les utilisateurs, mais publiés uniquement par les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-118">Phish messages can be reviewed by users but only released by admins.</span></span> <span data-ttu-id="c3cbe-119">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-119">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="c3cbe-120">Vous ne pouvez déplacer un message et le signaler comme faux positif (légitime) qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-120">You can only release a message and report it as a false positive (not junk) once.</span></span>

## <a name="view-your-quarantined-messages"></a><span data-ttu-id="c3cbe-121">Afficher les messages en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c3cbe-121">View your quarantined messages</span></span>

1. <span data-ttu-id="c3cbe-122">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-122">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="c3cbe-123">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-123">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="c3cbe-124">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-124">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="c3cbe-125">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-125">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="c3cbe-126">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-126">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-127">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-127">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-128">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-128">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-129">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-129">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-130">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-130">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-131">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-131">**Policy type**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-132">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c3cbe-132">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="c3cbe-133">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-133">**Recipient**</span></span>

   - <span data-ttu-id="c3cbe-134">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-134">**Message ID**</span></span>

   - <span data-ttu-id="c3cbe-135">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-135">**Policy name**</span></span>

   - <span data-ttu-id="c3cbe-136">**Taille**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-136">**Size**</span></span>

   - <span data-ttu-id="c3cbe-137">**Direction**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-137">**Direction**</span></span>

   <span data-ttu-id="c3cbe-138">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-138">When you're finished, click **Save**, or click **Set to default**.</span></span>

3. <span data-ttu-id="c3cbe-139">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-139">To filter the results, click **Filter**.</span></span> <span data-ttu-id="c3cbe-140">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-140">The available filters are:</span></span>

   - <span data-ttu-id="c3cbe-141">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-141">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="c3cbe-142">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-142">**Today**</span></span>

     - <span data-ttu-id="c3cbe-143">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-143">**Next 2 days**</span></span>

     - <span data-ttu-id="c3cbe-144">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-144">**Next 7 days**</span></span>

     - <span data-ttu-id="c3cbe-145">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-145">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="c3cbe-146">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-146">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="c3cbe-147">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-147">**Quarantine reason**:</span></span>

     - <span data-ttu-id="c3cbe-148">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-148">**Bulk**</span></span>

     - <span data-ttu-id="c3cbe-149">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-149">**Spam**</span></span>

     - <span data-ttu-id="c3cbe-150">**Hameçonnage** (à partir d’avril 2020)</span><span class="sxs-lookup"><span data-stu-id="c3cbe-150">**Phish** (As of April, 2020)</span></span>

   <span data-ttu-id="c3cbe-151">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-151">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="c3cbe-152">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-152">To hide the filter flyout, click **Filter** again.</span></span>

4. <span data-ttu-id="c3cbe-153">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-153">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="c3cbe-154">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-154">Wildcards aren't supported.</span></span> <span data-ttu-id="c3cbe-155">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-155">You can search by the following values:</span></span>

   - <span data-ttu-id="c3cbe-156">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-156">**Message ID**: The globally unique identifier of the message.</span></span> <span data-ttu-id="c3cbe-157">Si vous sélectionnez un message dans la liste, la valeur **ID du message** apparaît dans le volet déroulant **Détails** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-157">If you select a message in the list, the **Message ID** value appears in the **Details** flyout pane that appears.</span></span> <span data-ttu-id="c3cbe-158">Les administrateurs peuvent utiliser le [suivi des messages](message-trace-scc.md) pour rechercher les messages et les valeurs d’ID de message correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-158">Admins can use [message trace](message-trace-scc.md) to find messages and their corresponding Message ID values.</span></span>

   - <span data-ttu-id="c3cbe-159">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-159">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="c3cbe-160">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-160">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="c3cbe-161">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-161">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="c3cbe-162">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-162">The search is not case-sensitive.</span></span>

   <span data-ttu-id="c3cbe-163">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-163">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="c3cbe-164">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-164">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

### <a name="export-message-results"></a><span data-ttu-id="c3cbe-165">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="c3cbe-165">Export message results</span></span>

1. <span data-ttu-id="c3cbe-166">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-166">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="c3cbe-167">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-167">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="c3cbe-168">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-168">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

### <a name="view-quarantined-message-details"></a><span data-ttu-id="c3cbe-169">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c3cbe-169">View quarantined message details</span></span>

<span data-ttu-id="c3cbe-170">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-170">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="c3cbe-171">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-171">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="c3cbe-172">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-172">**Sender address**</span></span>

- <span data-ttu-id="c3cbe-173">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-173">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="c3cbe-174">**Subject**</span><span class="sxs-lookup"><span data-stu-id="c3cbe-174">**Subject**</span></span>

- <span data-ttu-id="c3cbe-175">**Raison de la mise en quarantaine** : indique si un message a été identifié comme **Courrier indésirable**, **E-mail de masse** ou (à partir d’avril 2020) **Hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-175">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk** or (as of April, 2020) **Phish**.</span></span>

- <span data-ttu-id="c3cbe-176">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-176">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="c3cbe-177">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-177">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="c3cbe-178">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-178">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="c3cbe-179">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-179">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="c3cbe-180">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c3cbe-180">Take action on quarantined email</span></span>

<span data-ttu-id="c3cbe-181">Après avoir sélectionné un message, vous pouvez effectuer les actions suivantes dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-181">After you select a message, you have options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="c3cbe-182">**Déplacer le message** : dans le volet déroulant qui s’affiche, indiquez si vous souhaitez **Signaler les messages à Microsoft pour analyse**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-182">**Release message**: In the flyout pane that appears, choose whether to **Report messages to Microsoft for analysis**.</span></span> <span data-ttu-id="c3cbe-183">Cette option est sélectionnée par défaut et signale à Microsoft le message mis en quarantaine par erreur comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-183">This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span>

  <span data-ttu-id="c3cbe-184">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-184">When you're finished, click **Release messages**.</span></span>

- <span data-ttu-id="c3cbe-185">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-185">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="c3cbe-186">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="c3cbe-186">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="c3cbe-187">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-187">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="c3cbe-188">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-188">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="c3cbe-189">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-189">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="c3cbe-190">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-190">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="c3cbe-191">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-191">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="c3cbe-192">**Supprimer de la quarantaine** : Le message est supprimé dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-192">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted.</span></span>

<span data-ttu-id="c3cbe-193">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-193">When you're finished, click **Close**.</span></span>

<span data-ttu-id="c3cbe-194">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-194">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="c3cbe-195">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c3cbe-195">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="c3cbe-196">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3cbe-196">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="c3cbe-197">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-197">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="c3cbe-198">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-198">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="c3cbe-199">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c3cbe-199">When you're finished, click **Close**.</span></span>
