---
title: Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Consumer/IW
ms.topic: how-to
localization_priority: Priority
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les utilisateurs peuvent découvrir comment afficher et gérer les messages mis en quarantaine dans Exchange Online Protection (EOP) qui auraient dû leur être remis.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 961912427f9c343f8235f0ed8e990431669ff9e5
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063382"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-eop"></a><span data-ttu-id="a6e56-103">Rechercher et publier des messages mis en quarantaine en tant qu’utilisateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="a6e56-103">Find and release quarantined messages as a user in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a6e56-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a6e56-104">**Applies to**</span></span>
- [<span data-ttu-id="a6e56-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="a6e56-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="a6e56-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="a6e56-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="a6e56-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a6e56-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="a6e56-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="a6e56-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="a6e56-109">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a6e56-109">For more information, see [Quarantine in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="a6e56-110">En tant qu'utilisateur, vous pouvez afficher, déplacer et supprimer les messages mis en quarantaine car considérés comme du courrier indésirable ou des e-mails de masse, si vous en êtes le destinataire.</span><span class="sxs-lookup"><span data-stu-id="a6e56-110">As a user, you can view, release, and delete quarantined messages where you are a recipient, and the message was quarantined as spam or bulk email.</span></span> <span data-ttu-id="a6e56-111">Depuis le 2020 avril, vous pouvez afficher ou supprimer les messages hameçonnage mis en quarantaine (pas d'hameçonnage de haute confiance) auxquels vous êtes destinataire.</span><span class="sxs-lookup"><span data-stu-id="a6e56-111">As of April 2020, you can view or delete quarantined phishing (not high confidence phishing) messages where you are a recipient.</span></span> <span data-ttu-id="a6e56-112">Vous pouvez afficher et gérer vos messages mis en quarantaine dans le centre de sécurité et de conformité ou (si un administrateur a utilisé cette configuration) dans les [notifications de courrier indésirable de l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a6e56-112">You view and manage your quarantined messages in the Security & Compliance Center or (if an admin has set this up) in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a6e56-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a6e56-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a6e56-114">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="a6e56-114">To open the Security & Compliance Center, go to <https://protection.office.com>.</span></span> <span data-ttu-id="a6e56-115">Pour ouvrir la page de quarantaine directement, accédez à <https://protection.office.com/quarantine>.</span><span class="sxs-lookup"><span data-stu-id="a6e56-115">To open the Quarantine page directly, go to <https://protection.office.com/quarantine>.</span></span>

- <span data-ttu-id="a6e56-116">Les administrateurs peuvent configurer la durée pendant laquelle les messages sont conservés dans la quarantaine avant d’être définitivement supprimés (stratégies anti-courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="a6e56-116">Admins can configure how long messages are kept in quarantine before they're permanently deleted (anti-spam policies).</span></span> <span data-ttu-id="a6e56-117">Les messages dont la mise en quarantaine est arrivée à expiration ne peuvent pas être récupérés.</span><span class="sxs-lookup"><span data-stu-id="a6e56-117">Messages that have expired from quarantine are unrecoverable.</span></span> <span data-ttu-id="a6e56-118">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a6e56-118">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="a6e56-119">Les administrateurs peuvent également [activer les notifications de courrier indésirable pour l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6e56-119">Admins can also [enable end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications) in anti-spam policies.</span></span> <span data-ttu-id="a6e56-120">Les utilisateurs peuvent débloquer les messages mis en quarantaine pour cause de courrier indésirable, directement depuis ces notifications.</span><span class="sxs-lookup"><span data-stu-id="a6e56-120">Users can release quarantined spam messages directly from these notifications.</span></span> <span data-ttu-id="a6e56-121">Les utilisateurs peuvent examiner les messages mis en quarantaine pour hameçonnage (pas les messages d’hameçonnage haute confiance) directement depuis ces notifications.</span><span class="sxs-lookup"><span data-stu-id="a6e56-121">Users can review quarantined phishing messages (not high confidence phishing messages) directly from these notifications.</span></span> <span data-ttu-id="a6e56-122">Si vous souhaitez en savoir plus, veuillez consulter l’article [Notifications de courrier indésirable pour l’utilisateur final dans EOP](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a6e56-122">For more information, see [End-user spam notifications in EOP](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

- <span data-ttu-id="a6e56-123">Les messages mis en quarantaine car considérés comme de l’hameçonnage, des programmes malveillants ou par règles de flux de messagerie (également appelés règles de transport) ne sont disponibles que pour les administrateurs. Ils sont en revanche invisibles pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a6e56-123">Messages that were quarantined for high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins, and aren't visible to users.</span></span> <span data-ttu-id="a6e56-124">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="a6e56-124">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="a6e56-125">Vous ne pouvez déplacer un message et le signaler comme faux positif (légitime) qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a6e56-125">You can only release a message and report it as a false positive (not junk) once.</span></span>

## <a name="view-your-quarantined-messages"></a><span data-ttu-id="a6e56-126">Afficher les messages en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6e56-126">View your quarantined messages</span></span>

1. <span data-ttu-id="a6e56-127">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-127">In the Security and Compliance Center, go to **Threat Management** \> **Review** \> **Quarantine**.</span></span>

2. <span data-ttu-id="a6e56-128">Vous pouvez trier les résultats en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="a6e56-128">You can sort the results by clicking on an available column header.</span></span> <span data-ttu-id="a6e56-129">Cliquez sur **Modifier les colonnes** pour afficher jusqu’à sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="a6e56-129">Click **Modify columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="a6e56-130">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="a6e56-130">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

   - <span data-ttu-id="a6e56-131">**Reçu**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-131">**Received**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-132">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-132">**Sender**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-133">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-133">**Subject**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-134">**Raison de la quarantaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-134">**Quarantine reason**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-135">**Déplacer ?**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-135">**Released?**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-136">**Type de stratégie**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-136">**Policy type**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-137">**Expire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a6e56-137">**Expires**<sup>\*</sup></span></span>
   - <span data-ttu-id="a6e56-138">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="a6e56-138">**Recipient**</span></span>
   - <span data-ttu-id="a6e56-139">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="a6e56-139">**Message ID**</span></span>
   - <span data-ttu-id="a6e56-140">**Nom de la stratégie**</span><span class="sxs-lookup"><span data-stu-id="a6e56-140">**Policy name**</span></span>
   - <span data-ttu-id="a6e56-141">**Taille**</span><span class="sxs-lookup"><span data-stu-id="a6e56-141">**Size**</span></span>
   - <span data-ttu-id="a6e56-142">**Direction**</span><span class="sxs-lookup"><span data-stu-id="a6e56-142">**Direction**</span></span>

   <span data-ttu-id="a6e56-143">Lorsque vous avez terminé, cliquez sur **Enregistrer** ou sur **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-143">When you're finished, click **Save**, or click **Set to default**.</span></span>

3. <span data-ttu-id="a6e56-144">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-144">To filter the results, click **Filter**.</span></span> <span data-ttu-id="a6e56-145">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="a6e56-145">The available filters are:</span></span>

   - <span data-ttu-id="a6e56-146">**Date d’expiration** : filtrer les messages par date d'expiration de la quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a6e56-146">**Expires time**: Filter messages by when they will expire from quarantine:</span></span>
     - <span data-ttu-id="a6e56-147">**Aujourd’hui**</span><span class="sxs-lookup"><span data-stu-id="a6e56-147">**Today**</span></span>
     - <span data-ttu-id="a6e56-148">**Dans les 2 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a6e56-148">**Next 2 days**</span></span>
     - <span data-ttu-id="a6e56-149">**Dans les 7 prochains jours**</span><span class="sxs-lookup"><span data-stu-id="a6e56-149">**Next 7 days**</span></span>
     - <span data-ttu-id="a6e56-150">**Personnaliser**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-150">**Custom**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a6e56-151">**Heure de réception**: Entrer une **Date de début** et une **Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-151">**Received time**: Enter a **Start date** and **End date**.</span></span>

   - <span data-ttu-id="a6e56-152">**Raison de la mise en quarantaine :**</span><span class="sxs-lookup"><span data-stu-id="a6e56-152">**Quarantine reason**:</span></span>
     - <span data-ttu-id="a6e56-153">**E-mail de masse**</span><span class="sxs-lookup"><span data-stu-id="a6e56-153">**Bulk**</span></span>
     - <span data-ttu-id="a6e56-154">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6e56-154">**Spam**</span></span>
     - <span data-ttu-id="a6e56-155">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a6e56-155">**Phish**</span></span>

   - <span data-ttu-id="a6e56-156">**Type de stratégie** : filtrer les messages par type de stratégie :</span><span class="sxs-lookup"><span data-stu-id="a6e56-156">**Policy Type**: Filter messages by policy type:</span></span>
     - <span data-ttu-id="a6e56-157">**Stratégie anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a6e56-157">**Anti-phish policy**</span></span>
     - <span data-ttu-id="a6e56-158">**Stratégie de filtrage de contenu hébergé** (stratégie anti-courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="a6e56-158">**Hosted content filter policy** (anti-spam policy)</span></span>

   <span data-ttu-id="a6e56-159">Pour effacer le filtre, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-159">To clear the filter, click **Clear**.</span></span> <span data-ttu-id="a6e56-160">Pour masquer le menu déroulant de filtrage, cliquez de nouveau sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-160">To hide the filter flyout, click **Filter** again.</span></span>

4. <span data-ttu-id="a6e56-161">Utilisez **Trier les résultats par** (le bouton **ID de message** par défaut) et une valeur correspondante pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a6e56-161">Use **Sort results by** (the **Message ID** button by default) and a corresponding value to find specific messages.</span></span> <span data-ttu-id="a6e56-162">Les caractères génériques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a6e56-162">Wildcards aren't supported.</span></span> <span data-ttu-id="a6e56-163">Vous pouvez effectuer une recherche sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6e56-163">You can search by the following values:</span></span>

   - <span data-ttu-id="a6e56-164">**ID du message** : l’identificateur global unique du message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-164">**Message ID**: The globally unique identifier of the message.</span></span> <span data-ttu-id="a6e56-165">Si vous sélectionnez un message dans la liste, la valeur **ID du message** apparaît dans le volet déroulant **Détails** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a6e56-165">If you select a message in the list, the **Message ID** value appears in the **Details** flyout pane that appears.</span></span> <span data-ttu-id="a6e56-166">Les administrateurs peuvent utiliser le [suivi des messages](message-trace-scc.md) pour rechercher les messages et les valeurs d’ID de message correspondantes.</span><span class="sxs-lookup"><span data-stu-id="a6e56-166">Admins can use [message trace](message-trace-scc.md) to find messages and their corresponding Message ID values.</span></span>

   - <span data-ttu-id="a6e56-167">**Adresse e-mail de l'expéditeur** : adresse e-mail d'un seul expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a6e56-167">**Sender email address**: A single sender's email address.</span></span>

   - <span data-ttu-id="a6e56-168">**Nom de la stratégie** : utilisez le nom de stratégie complet indiqué dans le message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-168">**Policy name**: Use the entire policy name of the message.</span></span> <span data-ttu-id="a6e56-169">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="a6e56-169">The search is not case-sensitive.</span></span>

   - <span data-ttu-id="a6e56-170">**Adresse e-mail du destinataire** : adresse e-mail d'un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="a6e56-170">**Recipient email address**: A single recipient's email address.</span></span>

   - <span data-ttu-id="a6e56-171">**Sujet** : utiliser l'intégralité du sujet du message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-171">**Subject**: Use the entire subject of the message.</span></span> <span data-ttu-id="a6e56-172">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="a6e56-172">The search is not case-sensitive.</span></span>

   <span data-ttu-id="a6e56-173">Après avoir entrer les critères de recherche, cliquez sur le ![Bouton actualiser](../../media/scc-quarantine-refresh.png) **Actualiser** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="a6e56-173">After you've entered the search criteria, click ![Refresh button](../../media/scc-quarantine-refresh.png) **Refresh** to filter the results.</span></span>

<span data-ttu-id="a6e56-174">Une fois le message spécifique mis en quarantaine trouvé, sélectionnez-le pour afficher des détails à son sujet et pour prendre des mesures (par exemple, afficher, déplacer, télécharger ou supprimer le message).</span><span class="sxs-lookup"><span data-stu-id="a6e56-174">After you find a specific quarantined message, select the message to view details about it, and to take action on it (for example, view, release, download, or delete the message).</span></span>

### <a name="export-message-results"></a><span data-ttu-id="a6e56-175">Exporter les résultats de message</span><span class="sxs-lookup"><span data-stu-id="a6e56-175">Export message results</span></span>

1. <span data-ttu-id="a6e56-176">Sélectionnez les messages qui vous intéressent, puis cliquez sur **Exporter les résultats**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-176">Select the messages you're interested in, and click **Export results**.</span></span>

2. <span data-ttu-id="a6e56-177">Cliquez sur **Oui** dans le message de confirmation qui vous avertit que la fenêtre du navigateur reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="a6e56-177">Click **Yes** in the confirmation message that warns you to keep the browser window open.</span></span>

3. <span data-ttu-id="a6e56-178">Lorsque l’exportation est prête, vous pouvez nommer et choisir l’emplacement de téléchargement du fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a6e56-178">When your export is ready, you can name and choose the download location for the .csv file.</span></span>

### <a name="view-quarantined-message-details"></a><span data-ttu-id="a6e56-179">Afficher les détails des messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6e56-179">View quarantined message details</span></span>

<span data-ttu-id="a6e56-180">Lorsque vous sélectionnez un message électronique dans la liste, les détails de message suivants s’affichent dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a6e56-180">When you select an email message in the list, the following message details appear in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a6e56-181">**ID du message** : l’identificateur global unique pour le message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-181">**Message ID**: The globally unique identifier for the message.</span></span>

- <span data-ttu-id="a6e56-182">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a6e56-182">**Sender address**</span></span>

- <span data-ttu-id="a6e56-183">**Reçu** : Date et heure de réception du message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-183">**Received**: The date/time when the message was received.</span></span>

- <span data-ttu-id="a6e56-184">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a6e56-184">**Subject**</span></span>

- <span data-ttu-id="a6e56-185">**Raison de mise en quarantaine** : indique si un message a été identifié comme **courrier indésirable**, **courrier en nombre** ou **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-185">**Quarantine reason**: Shows if a message has been identified as **Spam**, **Bulk** or **Phish**.</span></span>

- <span data-ttu-id="a6e56-186">**Destinataires** : si le message contient plusieurs destinataires, vous devez cliquer sur **Prévisualiser le message** ou **Afficher l’en-tête du message** pour afficher la liste complète des destinataires.</span><span class="sxs-lookup"><span data-stu-id="a6e56-186">**Recipients**: If the message contains multiple recipients, you need to click **Preview message** or **View message header** to see the complete list of recipients.</span></span>

- <span data-ttu-id="a6e56-187">**Expires** : Date et heure auxquelles le message sera automatiquement et définitivement supprimé de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a6e56-187">**Expires**: The date/time when the message will be automatically and permanently deleted from quarantine.</span></span>

- <span data-ttu-id="a6e56-188">**Déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a6e56-188">**Released to**: All email addresses (if any) to which the message has been released.</span></span>

- <span data-ttu-id="a6e56-189">**Pas encore déplacé pour** : toutes les adresses e-mail (le cas échéant) auxquelles le message n'a pas encore été envoyé.</span><span class="sxs-lookup"><span data-stu-id="a6e56-189">**Not yet released to**: All email addresses (if any) to which the message has not yet been released.</span></span>

### <a name="take-action-on-quarantined-email"></a><span data-ttu-id="a6e56-190">Effectuer une action sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6e56-190">Take action on quarantined email</span></span>

<span data-ttu-id="a6e56-191">Après avoir sélectionné un message, vous pouvez effectuer les actions suivantes dans le volet déroulant **Détails** :</span><span class="sxs-lookup"><span data-stu-id="a6e56-191">After you select a message, you have options for what to do with the messages in the **Details** flyout pane:</span></span>

- <span data-ttu-id="a6e56-192">**Déplacer le message** : dans le volet déroulant qui s’affiche, indiquez si vous souhaitez **Signaler les messages à Microsoft pour analyse**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-192">**Release message**: In the flyout pane that appears, choose whether to **Report messages to Microsoft for analysis**.</span></span> <span data-ttu-id="a6e56-193">Cette option est sélectionnée par défaut et signale à Microsoft le message mis en quarantaine par erreur comme un faux positif.</span><span class="sxs-lookup"><span data-stu-id="a6e56-193">This is selected by default, and reports the erroneously quarantined message to Microsoft as a false positive.</span></span>

  <span data-ttu-id="a6e56-194">Lorsque vous avez terminé, cliquez sur **Déplacer les messages**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-194">When you're finished, click **Release messages**.</span></span>

- <span data-ttu-id="a6e56-195">**Afficher l’en-tête du message** : Sélectionnez ce lien pour afficher le texte d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="a6e56-195">**View message header**: Choose this link to see the message header text.</span></span> <span data-ttu-id="a6e56-196">Pour analyser en profondeur les champs d'en-tête et les valeurs, copiez le texte d’en-tête du message dans le presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft** pour accéder à l’analyseur de connectivité à distance (Faites un clic droit et sélectionnez **Ouvrir dans un nouvel onglet** si vous ne souhaitez pas laisser Microsoft 365 accomplir cette tâche).</span><span class="sxs-lookup"><span data-stu-id="a6e56-196">To analyze the header fields and values in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Microsoft 365 to complete this task).</span></span> <span data-ttu-id="a6e56-197">Collez l’en-tête du message dans la section analyseur d’en-tête de message de la page, puis sélectionnez **Analyser les en-têtes** :</span><span class="sxs-lookup"><span data-stu-id="a6e56-197">Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**:</span></span>

- <span data-ttu-id="a6e56-198">**Prévisualiser le message** : dans le volet déroulant qui apparaît, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6e56-198">**Preview message**: In the flyout pane that appears, choose one of the following options:</span></span>
  - <span data-ttu-id="a6e56-199">**Mode Source** : affiche la version HTML du corps du message, dans laquelle tous les liens sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="a6e56-199">**Source view**: Shows the HTML version of the message body with all links disabled.</span></span>
  - <span data-ttu-id="a6e56-200">**Mode texte** : affiche le corps du message au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="a6e56-200">**Text view**: Shows the message body in plain text.</span></span>

- <span data-ttu-id="a6e56-201">**Supprimer de la quarantaine** : Le message est supprimé dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a6e56-201">**Remove from quarantine**: After you click **Yes** in the warning that appears, the message is immediately deleted.</span></span>

<span data-ttu-id="a6e56-202">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-202">When you're finished, click **Close**.</span></span>

<span data-ttu-id="a6e56-203">Si vous ne déplacez pas ou ne supprimez pas le message, il sera supprimé après l'expiration de la période de conservation de quarantaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="a6e56-203">If you don't release or remove the message, it will be deleted after the default quarantine retention period expires.</span></span>

#### <a name="take-action-on-multiple-quarantined-email-messages"></a><span data-ttu-id="a6e56-204">Effectuer une action sur plusieurs courriers électroniques mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6e56-204">Take action on multiple quarantined email messages</span></span>

<span data-ttu-id="a6e56-205">Lorsque vous sélectionnez plusieurs messages mis en quarantaine dans la liste (jusqu’à 100), le volet déroulant **Actions groupées** s’affiche et vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6e56-205">When you select multiple quarantined messages in the list (up to 100), the **Bulk actions** flyout pane appears where you can take the following actions:</span></span>

- <span data-ttu-id="a6e56-206">**Déplacer les messages** : Les options sont les mêmes que lorsque vous déplacez un seul message, sauf que vous ne pouvez pas sélectionner **Déplacer les messages pour des destinataires spécifiques**. Vous pouvez seulement sélectionner **Déplacer le message pour tous les destinataires** ou **Déplacer les messages pour d'autres personnes**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-206">**Release messages**: The options are the same as when you release a single message, except you can't select **Release messages to specific recipients**; you can only select **Release message to all recipients** or **Release messages to other people**.</span></span>

- <span data-ttu-id="a6e56-207">**Supprimer des messages** : le message est immédiatement supprimé sans être envoyé aux destinataires d’origine dès que vous cliquez sur **Oui** dans le message d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a6e56-207">**Delete messages**:  After you click **Yes** in the warning that appears, the message are immediately deleted without being sent to the original recipients.</span></span>

<span data-ttu-id="a6e56-208">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a6e56-208">When you're finished, click **Close**.</span></span>