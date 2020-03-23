---
title: Rechercher et débloquer les messages en quarantaine en tant qu’utilisateur dans Office 365
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
description: En tant qu'utilisateur Office 365, vous pouvez afficher, déplacer et supprimer les messages mis en quarantaine (les messages dont vous êtes le destinataire et qui sont en quarantaine car considérés comme du courrier indésirable ou comme des e-mails de masse). Vous pouvez afficher et gérer vos messages mis en quarantaine dans le Centre de sécurité et de conformité.
ms.openlocfilehash: 04f04cfddb123bf176f3c71568789c77d225a601
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42893669"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a><span data-ttu-id="8ea77-104">Rechercher et déplacer les messages en quarantaine en tant qu’utilisateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8ea77-104">Find and release quarantined messages as a user in Office 365</span></span>

<span data-ttu-id="8ea77-105">La quarantaine contient des messages potentiellement dangereux ou indésirables dans les organisations Office 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8ea77-105">Quarantine holds potentially dangerous or unwanted messages in Office 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="8ea77-106">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8ea77-106">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="8ea77-107">En tant qu'utilisateur, vous pouvez afficher, déplacer et supprimer les messages mis en quarantaine car considérés comme du courrier indésirable, des e-mails de masse, ou (à partir d’avril 2020) de l’hameçonnage, si vous en êtes le destinataire.</span><span class="sxs-lookup"><span data-stu-id="8ea77-107">As a user, you can view, release, and delete quarantined messages where you are a recipient, and the message was quarantined as spam, bulk email, or (as of April, 2020) phishing.</span></span> <span data-ttu-id="8ea77-108">Vous pouvez également signaler les faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8ea77-108">You can also report false positives to Microsoft.</span></span>

<span data-ttu-id="8ea77-109">Vous pouvez afficher et gérer vos messages mis en quarantaine dans le Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="8ea77-109">You view and manage your quarantined messages in the Security & Compliance Center.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8ea77-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8ea77-110">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8ea77-111">Pour ouvrir le Centre de sécurité et conformité Office 365, accédez à <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="8ea77-111">To open the Office 365 Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="8ea77-112">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="8ea77-112">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="8ea77-113">Les administrateurs peuvent configurer la durée pendant laquelle les messages sont conservés dans la quarantaine avant d’être définitivement supprimés (stratégies anti-courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="8ea77-113">Admins can configure how long messages are kept in quarantine before they're permanently deleted (anti-spam policies).</span></span> <span data-ttu-id="8ea77-114">Les messages dont la mise en quarantaine est arrivée à expiration ne peuvent pas être récupérés.</span><span class="sxs-lookup"><span data-stu-id="8ea77-114">Messages that have expired from quarantine are unrecoverable.</span></span> <span data-ttu-id="8ea77-115">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8ea77-115">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="8ea77-116">Les administrateurs peuvent également [activer les notifications de courrier indésirable pour l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="8ea77-116">Admins can also [enable end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) in anti-spam policies.</span></span> <span data-ttu-id="8ea77-117">Depuis octobre 2019, vous ne pouvez plus déplacer les messages mis en quarantaine directement à partir de ces notifications.</span><span class="sxs-lookup"><span data-stu-id="8ea77-117">As of October 2019, you can no longer release quarantined messages directly from these notifications.</span></span> <span data-ttu-id="8ea77-118">Vous pouvez cliquer sur **Examiner** dans la notification, ce qui vous permet d’accéder à la quarantaine dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="8ea77-118">You can click **Review** in the notification, which will take you to Quarantine in the Security & Compliance Center.</span></span> <span data-ttu-id="8ea77-119">Pour plus d’informations sur ces notifications, voir [Notifications de courrier indésirable à l’utilisateur final dans Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8ea77-119">For more information about the notifications, see [End-user spam notifications in Office 365](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

- <span data-ttu-id="8ea77-120">Les messages mis en quarantaine car considérés comme de l’hameçonnage, des programmes malveillants ou par règles de flux de messagerie (également appelés règles de transport) ne sont disponibles que pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8ea77-120">Messages that were quarantined for high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="8ea77-121">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="8ea77-121">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="8ea77-122">Vous ne pouvez déplacer un message et le signaler comme faux positif (légitime) qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="8ea77-122">You can only release a message and report it as a false positive (not junk) once.</span></span>

## <a name="view-your-quarantined-messages"></a><span data-ttu-id="8ea77-123">Afficher les messages en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8ea77-123">View your quarantined messages</span></span>

1. <span data-ttu-id="8ea77-124">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-124">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="8ea77-125">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="8ea77-125">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="8ea77-126">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="8ea77-126">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="8ea77-127">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="8ea77-127">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="8ea77-128">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-128">**Received**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-129">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-129">**Sender**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-130">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-130">**Subject**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-131">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-131">**Quarantine reason**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-132">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-132">**Released?**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-133">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-133">**Policy type**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-134">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8ea77-134">**Expires**<sup>\*</sup></span></span>

   - <span data-ttu-id="8ea77-135">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="8ea77-135">**Recipient**</span></span>

   - <span data-ttu-id="8ea77-136">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="8ea77-136">**Message ID**</span></span>

   - <span data-ttu-id="8ea77-137">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="8ea77-137">**Policy name**</span></span>

   - <span data-ttu-id="8ea77-138">**Taille**</span><span class="sxs-lookup"><span data-stu-id="8ea77-138">**Size**</span></span>

   - <span data-ttu-id="8ea77-139">**Direction**</span><span class="sxs-lookup"><span data-stu-id="8ea77-139">**Direction**</span></span>

   <span data-ttu-id="8ea77-140">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-140">When you're finished, click **Save**, or click **Set to default**.</span></span>

3. <span data-ttu-id="8ea77-141">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-141">To filter the results, click **Filter**.</span></span> <span data-ttu-id="8ea77-142">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="8ea77-142">The available filters are:</span></span>

   - <span data-ttu-id="8ea77-143">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="8ea77-143">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>

     - <span data-ttu-id="8ea77-144">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="8ea77-144">**Today**</span></span>

     - <span data-ttu-id="8ea77-145">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="8ea77-145">**Next 2 days**</span></span>

     - <span data-ttu-id="8ea77-146">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="8ea77-146">**Next 7 days**</span></span>

     - <span data-ttu-id="8ea77-147">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-147">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="8ea77-148">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-148">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="8ea77-149">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="8ea77-149">**Quarantine reason**:</span></span>

     - <span data-ttu-id="8ea77-150">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="8ea77-150">**Bulk**</span></span>

     - <span data-ttu-id="8ea77-151">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8ea77-151">**Spam**</span></span>

     - <span data-ttu-id="8ea77-152">**Hameçonnage** (à partir d’avril 2020)</span><span class="sxs-lookup"><span data-stu-id="8ea77-152">**Phish** (As of April, 2020)</span></span>

   <span data-ttu-id="8ea77-153">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-153">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="8ea77-154">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-154">To hide the filter flyout, click **Filter** again.</span></span>

4. <span data-ttu-id="8ea77-155">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8ea77-155">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="8ea77-156">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8ea77-156">Wildcards aren't supported.</span></span> <span data-ttu-id="8ea77-157">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ea77-157">You can search by the following values:</span></span>

   - <span data-ttu-id="8ea77-158">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="8ea77-158">**Message ID**: The globally unique identifier of the message.</span></span> <span data-ttu-id="8ea77-159">Si vous sélectionnez un message dans la liste, la valeur **ID du message** apparaît dans le volet déroulant **Détails** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8ea77-159">If you select a message in the list, the **Message ID** value appears in the **Details** flyout pane that appears.</span></span> <span data-ttu-id="8ea77-160">Les administrateurs peuvent utiliser le [suivi des messages](message-trace-scc.md) pour rechercher les messages et les valeurs d’ID de message correspondantes.</span><span class="sxs-lookup"><span data-stu-id="8ea77-160">Admins can use [message trace](message-trace-scc.md) to find messages and their corresponding Message ID values.</span></span>

   - <span data-ttu-id="8ea77-161">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8ea77-161">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="8ea77-162">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="8ea77-162">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="8ea77-163">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="8ea77-163">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="8ea77-164">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="8ea77-164">The search is not case-sensitive.</span></span>

   <span data-ttu-id="8ea77-165">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="8ea77-165">After you've entered the search criteria, click ![Refresh button](../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="8ea77-166">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="8ea77-166">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

### <a name="export-message-results"></a><span data-ttu-id="8ea77-167">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="8ea77-167">Export message results</span></span>

1. <span data-ttu-id="8ea77-168">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-168">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="8ea77-169">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="8ea77-169">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="8ea77-170">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="8ea77-170">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

### <a name="view-quarantined-message-details"></a><span data-ttu-id="8ea77-171">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8ea77-171">View quarantined message details</span></span>

<span data-ttu-id="8ea77-172">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="8ea77-172">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="8ea77-173">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="8ea77-173">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="8ea77-174">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8ea77-174">**Sender address**</span></span>

- <span data-ttu-id="8ea77-175">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="8ea77-175">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="8ea77-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8ea77-176">**Subject**</span></span>

- <span data-ttu-id="8ea77-177">**Raison de la mise en quarantaine** : indique si un message a été identifié comme **Courrier indésirable**, **E-mail de masse** ou (à partir d’avril 2020) **Hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-177">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk** or (as of April, 2020) **Phish**.</span></span>

- <span data-ttu-id="8ea77-178">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="8ea77-178">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="8ea77-179">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="8ea77-179">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="8ea77-180">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="8ea77-180">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="8ea77-181">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="8ea77-181">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="8ea77-182">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8ea77-182">Take action on quarantined email</span></span>

<span data-ttu-id="8ea77-183">Après avoir sélectionné un message, vous pouvez effectuer les actions suivantes dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="8ea77-183">After you select a message, you have options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="8ea77-184">**Déplacer le message** : dans le volet déroulant qui s’affiche, indiquez si vous souhaitez **Signaler les messages à Microsoft pour analyse**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-184">**Release message**: In the flyout pane that appears, choose whether to **Report messages to Microsoft for analysis**.</span></span> <span data-ttu-id="8ea77-185">Cette option est sélectionnée par défaut et signale à Microsoft le message mis en quarantaine par erreur comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="8ea77-185">This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span>

  <span data-ttu-id="8ea77-186">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-186">When you're finished, click **Release messages**.</span></span>

- <span data-ttu-id="8ea77-187">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="8ea77-187">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="8ea77-188">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Office 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="8ea77-188">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Office 365 to complete this task).</span></span> <span data-ttu-id="8ea77-189">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="8ea77-189">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="8ea77-190">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ea77-190">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>

  - <span data-ttu-id="8ea77-191">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="8ea77-191">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  
  - <span data-ttu-id="8ea77-192">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="8ea77-192">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="8ea77-193">**Télécharger le message** : dans le volet déroulant qui s’affiche, sélectionnez **Je comprends les risques liés au téléchargement de ce message** pour enregistrer une copie locale du message au format .eml.</span><span class="sxs-lookup"><span data-stu-id="8ea77-193">**Download message**: In the flyout pane that appears, select **I understand the risks from downloading this message** to save a local copy of the message in .eml format.</span></span>

- <span data-ttu-id="8ea77-194">**Supprimer de la quarantaine** : Le message est supprimé dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8ea77-194">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted.</span></span>

<span data-ttu-id="8ea77-195">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-195">When you're finished, click **Close**.</span></span>

<span data-ttu-id="8ea77-196">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="8ea77-196">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="8ea77-197">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8ea77-197">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="8ea77-198">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ea77-198">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="8ea77-199">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-199">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="8ea77-200">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8ea77-200">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="8ea77-201">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8ea77-201">When you're finished, click **Close**.</span></span>
