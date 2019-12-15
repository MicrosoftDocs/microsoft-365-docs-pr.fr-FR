---
title: Affichages des campagnes dans Office 365 - Protection avancée contre les menaces
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: mcostea
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez Campaign Views dans Office 365 - Protection avancée contre les menaces.
ms.openlocfilehash: 2d43b73a613ad6399a151a6bda39f236c7c913e8
ms.sourcegitcommit: b65c80051e53d9be223f4769f4d42a39f5a07735
ms.translationtype: MT + HT Review
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "39962759"
---
# <a name="campaign-views-in-office-365-atp"></a><span data-ttu-id="83598-103">Campaign Views dans Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="83598-103">Campaign Views in Office 365 ATP</span></span>

> [!NOTE]
> <span data-ttu-id="83598-104">Les fonctionnalités décrites dans cette rubrique sont actuellement en préversion et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="83598-104">The features described in this article are currently in preview and subject to change.</span></span>

<span data-ttu-id="83598-105">Campaign Views est une fonctionnalité de la protection avancée contre les menaces (ATP) dans le Centre de sécurité et de conformité Office 365 qui identifie et catégorise les attaques par hameçonnage dans le service.</span><span class="sxs-lookup"><span data-stu-id="83598-105">Campaign Views is a feature in Advanced Threat Protection (ATP) in the Office 365 Security & Compliance Center that identifies and categorizes phishing attacks in the service.</span></span> <span data-ttu-id="83598-106">Campaign Views permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="83598-106">Campaign Views can help you to:</span></span>

- <span data-ttu-id="83598-107">Examiner et répondre efficacement aux attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="83598-107">Efficiently investigate and respond to phishing attacks.</span></span>

- <span data-ttu-id="83598-108">Mieux comprendre l’étendue de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="83598-108">Better understand the scope of the attack.</span></span>

- <span data-ttu-id="83598-109">Afficher la valeur pour les décideurs.</span><span class="sxs-lookup"><span data-stu-id="83598-109">Show value to decision makers.</span></span>

<span data-ttu-id="83598-110">Campaign Views vous permet de voir la présentation d’une attaque plus rapidement et plus complètement que n’importe quel autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83598-110">Campaign Views lets you see the big picture of an attack faster and more complete than any human.</span></span>

## <a name="what-is-a-campaign"></a><span data-ttu-id="83598-111">Qu’est-ce qu’une campagne ?</span><span class="sxs-lookup"><span data-stu-id="83598-111">What is a ToolTip?</span></span>

<span data-ttu-id="83598-112">Une campagne est une attaque par e-mail coordonné contre une ou plusieurs organisations.</span><span class="sxs-lookup"><span data-stu-id="83598-112">A campaign is a coordinated email attack against one or many organizations.</span></span> <span data-ttu-id="83598-113">Aujourd’hui, les attaques par e-mail qui volent les informations d’identification et les données de l’entreprise sont une activité importante et lucrative.</span><span class="sxs-lookup"><span data-stu-id="83598-113">Today, email attacks that steal credentials and company data are a big and lucrative business.</span></span> <span data-ttu-id="83598-114">Au fur et à mesure de l’augmentation des attaques, les intrus sont suffisamment sophistiqués pour modifier leurs méthodes pour garantir la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="83598-114">As technologies increase in an effort to stop attacks, attackers are sophisticated enough to modify their methods in an effort to ensure continued success.</span></span>

<span data-ttu-id="83598-115">Microsoft exploite les nombreuses fonctionnalités de protection contre le hameçonnage, l’anti-courrier indésirable et les programmes malveillants sur l’ensemble du service Office 365 dans le monde entier pour identifier les campagnes.</span><span class="sxs-lookup"><span data-stu-id="83598-115">Microsoft leverages the vast amounts of anti-phishing, anti-spam, and anti-malware data and experience across the entire Office 365 service world-wide to identify campaigns.</span></span> <span data-ttu-id="83598-116">Les informations de l’attaque sont analysées et classées en fonction de plusieurs facteurs.</span><span class="sxs-lookup"><span data-stu-id="83598-116">The attack information is analyzed and classified according to several factors.</span></span> <span data-ttu-id="83598-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="83598-117">For example:</span></span>

- <span data-ttu-id="83598-118">**Sources d’attaque** : adresses IP sources et domaines de l’e-mail de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="83598-118">**Attack source**: Source IP addresses and sender email domains.</span></span>

- <span data-ttu-id="83598-119">**Propriétés du message d’attaque** : le contenu, le style et le ton des messages d’attaques.</span><span class="sxs-lookup"><span data-stu-id="83598-119">**Attack message properties**: The content, style, and tone of the attack messages.</span></span>

- <span data-ttu-id="83598-120">**Destinataires d’attaques** : domaines de destinataires, fonctions de tâche de destinataire (administrateurs, cadres, etc.), types d’entreprise (grand, petit, public, privé, etc.) et industries.</span><span class="sxs-lookup"><span data-stu-id="83598-120">**Attack recipients**: Recipient domains, recipient job functions (admins, executives, etc.), company types (large, small, public, private, etc.), and industries.</span></span>

- <span data-ttu-id="83598-121">**Charge utile d’attaques** : liens malveillants, pièces jointes ou autres charges utiles.</span><span class="sxs-lookup"><span data-stu-id="83598-121">**Attack payload**: Malicious links, attachments, or other payloads.</span></span>

## <a name="campaign-views-the-office-365-security--compliance-center"></a><span data-ttu-id="83598-122">Campaign Views dans le Centre de sécurité et conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="83598-122">Permissions in the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="83598-123">Campaign Views est disponible dans le [Centre de sécurité et conformité](https://docs.microsoft.com/microsoft-365/compliance/go-to-the-securitycompliance-center) aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="83598-123">Campaign Views is available in the [Security & Compliance Center](https://docs.microsoft.com/microsoft-365/compliance/go-to-the-securitycompliance-center) at the following locations:</span></span>

- <span data-ttu-id="83598-124">**Gestion des menaces** \> **Explorer** \> **Affichage** \> **Hameçonnage** \> **Top campagne (Aperçu)**</span><span class="sxs-lookup"><span data-stu-id="83598-124">**Threat management** \> **Explorer** \> **View** \> **Phish** \> **Top campaign (Preview)**</span></span>

- <span data-ttu-id="83598-125">**Gestion des menaces** \> **Explorer** \> **Affichage** \> **Tous les e-mails** \> **Top campagne (Aperçu)**</span><span class="sxs-lookup"><span data-stu-id="83598-125">**Threat management** \> **Explorer** \> **View** \> **All email** \> **Top campaign (Preview)**</span></span>

![Vue d’ensemble des campagnes dans la Centre de sécurité et conformité](../media/campaigns-overview.png)

> [!TIP]
> <span data-ttu-id="83598-127">Pour l’instant, le seul filtrage disponible est la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="83598-127">Currently, the only filtering that's available is the date range.</span></span> <span data-ttu-id="83598-128">Si aucune donnée de campagne n’apparaît, essayez de modifier la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="83598-128">If you don't see any campaign data, try changing the date range.</span></span>

<span data-ttu-id="83598-129">La page vue d’ensemble présente les informations suivantes sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="83598-129">The overview page shows the following information about the campaign:</span></span>

- <span data-ttu-id="83598-130">**Nom**</span><span class="sxs-lookup"><span data-stu-id="83598-130">**Name**</span></span>

- <span data-ttu-id="83598-131">**Exemple d’objet** : la ligne d’objet de l’un des messages de la campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-131">**Sample subject**: The subject line of one of the messages in the campaign.</span></span> <span data-ttu-id="83598-132">Notez que _toutes_ les messages de la campagne ne comportent pas nécessairement cette même ligne d’objet.</span><span class="sxs-lookup"><span data-stu-id="83598-132">Note that _all_ the messages in the campaign will not necessarily have this same subject line.</span></span>

- <span data-ttu-id="83598-133">**Type** : pour l’instant, cette valeur sera toujours **Hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="83598-133">**Type**: Currently, this value will always be **Phish**.</span></span>

- <span data-ttu-id="83598-134">**Sous-type** : s’il est disponible, il s’agit de la marque faisant l’objet d’un hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-134">**Subtype**: Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="83598-135">Lorsque la détection est contrôlée par la technologie ATP, le préfixe **ATP-** est ajouté à la valeur de sous-type.</span><span class="sxs-lookup"><span data-stu-id="83598-135">When the detection is driven by ATP technology, the prefix **ATP-** is added to the subtype value.</span></span>

- <span data-ttu-id="83598-136">**Destinataires** : nombre d’utilisateurs qui ont été ciblés par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-136">**Recipients**: The number of users that were targeted by this campaign.</span></span>

- <span data-ttu-id="83598-137">**Remis**: nombre d’utilisateurs qui ont reçu des messages de cette campagne dans leur boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="83598-137">**Delivered**: The number of users that received messages from this campaign into their Inbox.</span></span>

- <span data-ttu-id="83598-138">**ID** : identificateur unique de la campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-138">**ID**: A unique identifier for the campaign.</span></span>

<span data-ttu-id="83598-139">Lorsque vous cliquez sur le nom d’une campagne, les détails de la campagne s’affichent dans une fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="83598-139">When you click on the name of a campaign, the campaign details appears in a flyout.</span></span>

## <a name="campaign-details"></a><span data-ttu-id="83598-140">Détails de la campagne</span><span class="sxs-lookup"><span data-stu-id="83598-140">Campaign details</span></span>

<span data-ttu-id="83598-141">Dans la vue Détails de la campagne, de nombreuses informations sont disponibles sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="83598-141">In the campaign details view, a lot of information is available about the campaign:</span></span>

- <span data-ttu-id="83598-142">Informations sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="83598-142">Campaign information:</span></span>

  - <span data-ttu-id="83598-143">**ID** : il s’agit de l’identificateur unique de la campagne dans l’écran vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="83598-143">**ID**: The same unique identifier of the campaign from the overview screen.</span></span>

  - <span data-ttu-id="83598-144">**Commencé** et **terminé** : le filtre de la plage de dates que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83598-144">**Started** and **Ended**: the date range filter you selected.</span></span>

  - <span data-ttu-id="83598-145">**Impact** : nombre de messages envoyés dans la plage de dates que vous avez sélectionnée, nombre de boîtes aux lettres dans la boîte de réception (autrement dit, remis à la boîte de réception) et nombre d’utilisateurs sur la charge utile d’URL dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="83598-145">**Impact**: the number of messages sent in the date range you selected, how many were "inboxed" (that is, delivered to the Inbox), and how many users clicked on the URL payload in the phishing message.</span></span>

  - <span data-ttu-id="83598-146">Chronologie de l’activité de la campagne : lorsque la campagne a commencé et se termine et que le volume de messages s’affiche au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="83598-146">A timeline of campaign activity: When the campaign started and ended, and the volume of messages over time.</span></span>

### <a name="campaign-flow"></a><span data-ttu-id="83598-147">Flux de la campagne</span><span class="sxs-lookup"><span data-stu-id="83598-147">Campaign flow</span></span>

<span data-ttu-id="83598-148">Des informations importantes sur la campagne sont présentées dans un diagramme de flux horizontal (appelé diagramme de _Sankey_) dans la section **Flux**.</span><span class="sxs-lookup"><span data-stu-id="83598-148">Important details about the campaign are presented in a horizontal flow diagram (known as a _Sankey_ diagram) in the **Flow** section.</span></span> <span data-ttu-id="83598-149">Ces détails vous aideront à comprendre les éléments de la campagne et l’impact potentiel au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="83598-149">These details will help you to understand the elements of the campaign and the potential impact in your organization.</span></span>

![Détails de la campagne ne contenant pas d’URL d’utilisateur](../media/campaign-details-no-recipient-actions.png)

<span data-ttu-id="83598-151">Si vous pointez sur une bande horizontale dans le diagramme, vous pouvez voir le nombre de messages associés (par exemple, les messages d’une adresse IP source particulière, les messages provenant de l’adresse IP source en utilisant le domaine d’expéditeur spécifié, etc.).</span><span class="sxs-lookup"><span data-stu-id="83598-151">If you hover over a horizontal band in the diagram, you'll see the number of related messages (for example, messages from a particular source IP, messages from the source IP using the specified sender domain, etc.).</span></span>

<span data-ttu-id="83598-152">Le diagramme contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="83598-152">The entry contains the following information:</span></span>

- <span data-ttu-id="83598-153">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="83598-153">**Sender IPs**</span></span>

- <span data-ttu-id="83598-154">**Domaines de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="83598-154">**Sender domains**</span></span>

- <span data-ttu-id="83598-155">**Filtrer les verdicts**: les valeurs ici sont liées aux verdicts de filtre anti-hameçonnage et anti-courrier indésirable disponibles, comme décrit dans [En-têtes des messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="83598-155">**Filter verdicts**: The values here are related to the available anti-phishing and anti-spam filter verdicts as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="83598-156">Voici les valeurs **Client autorisent**, ce qui signifie qu’un paramètre configuré dans l’organisation permettait l’envoi d’un message qui aurait été autrement bloqué par le service (par exemple, un domaine dans la liste des expéditeurs autorisés).</span><span class="sxs-lookup"><span data-stu-id="83598-156">Of great interest here are the values **Tenant Allow**, which means a configured setting in the organization allowed a message through that would have been otherwise blocked by the service (for example, a domain in the Allowed Senders list).</span></span>

  - <span data-ttu-id="83598-157">**Blocage de locataire** : cette valeur indique qu’un paramètre de votre organisation (par exemple, une entrée de domaine dans la [liste d’expéditeurs bloqués](create-block-sender-lists-in-office-365.md)) a détecté le message et déterminé l’emplacement où il a été remis.</span><span class="sxs-lookup"><span data-stu-id="83598-157">**Tenant Block**: This value indicates that a setting in your organization (for example, a domain entry in the [Blocked Senders list](create-block-sender-lists-in-office-365.md)) both detected the message and determined where it was delivered.</span></span> <span data-ttu-id="83598-158">Pour les messages qui n’ont pas été mis en quarantaine, consultez vos paramètres d’expéditeurs bloqués pour déterminer la raison pour laquelle le message a été remis.</span><span class="sxs-lookup"><span data-stu-id="83598-158">For messages that weren't quarantined, review your blocked senders settings to determine why the message was delivered.</span></span>

  - <span data-ttu-id="83598-159">**Détecté**</span><span class="sxs-lookup"><span data-stu-id="83598-159">**Detected app**</span></span>

  - <span data-ttu-id="83598-160">**Autoriser le locataire**</span><span class="sxs-lookup"><span data-stu-id="83598-160">**Tenant Allow**</span></span>

- <span data-ttu-id="83598-161">**Emplacements de remise**: vous souhaiterez peut-être examiner les messages qui ont été remis aux destinataires (soit dans la boîte de réception, soit dans le dossier courrier indésirable), même si les utilisateurs n'ont pas cliqué sur l'URL de la charge utile dans le message.</span><span class="sxs-lookup"><span data-stu-id="83598-161">**Delivery locations**: You'll likely want to investigate messages that were actually delivered to recipients (either to the Inbox or the Junk Email folder), even if users didn't click on the payload URL in the message.</span></span> <span data-ttu-id="83598-162">Vous pouvez également supprimer les messages mis en quarantaine de [Messages mis en quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="83598-162">You can also remove the quarantined messages from [Quarantine email messages in Office 365](quarantine-email-messages.md).</span></span>

  - <span data-ttu-id="83598-163">**Dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="83598-163">**The Junk E-Mail folder.**</span></span>

  - <span data-ttu-id="83598-164">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="83598-164">**Quarantine**</span></span>

  - <span data-ttu-id="83598-165">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="83598-165">**Inbox**</span></span>

#### <a name="url-clicks"></a><span data-ttu-id="83598-166">Clics d’URL</span><span class="sxs-lookup"><span data-stu-id="83598-166">URL clicks</span></span>

<span data-ttu-id="83598-167">Il y a toujours la possibilité que les messages remis à la boîte de réception ou au dossier courrier indésirable du destinataire soient traités par l’utilisateur (autrement dit, l’utilisateur peut cliquer sur l’URL malveillante dans le message).</span><span class="sxs-lookup"><span data-stu-id="83598-167">There's always the chance that messages delivered to the recipient's Inbox or Junk Email folder can be acted upon by the user (that is, user will click on the malicious URL in the message).</span></span> <span data-ttu-id="83598-168">Si ce n’est pas le cas, il s’agit d’une mesure de réussite minime, même si vous avez certainement besoin de déterminer pourquoi le message nuisible a été remis à sa boîte aux lettres en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="83598-168">If they haven't, that's a small measure of success, although you certainly need to determine why the harmful message was delivered to their mailbox in the first place.</span></span>

<span data-ttu-id="83598-169">Si un utilisateur clique sur l’URL malveillante, les actions s’affichent dans la zone **Clics d’URL** du diagramme.</span><span class="sxs-lookup"><span data-stu-id="83598-169">If a user has clicked on the malicious URL, the actions are displayed in the **URL clicks** area of the diagram.</span></span>

![Détails de la campagne contenant d’URL d’utilisateur](../media/campaign-details-with-recipient-actions.png)

- <span data-ttu-id="83598-171">**Blocage de liens fiables** : cette valeur indique que le destinataire a cliqué sur l’URL de la charge utile dans le message, mais qu’il a été bloqué par les stratégies de[Liens fiables ATP](atp-safe-links.md) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="83598-171">**Safe Links Block**: This value indicates the recipient clicked on the payload URL in the message, but it was blocked by the [ATP Safe Links](atp-safe-links.md) policies in your organization.</span></span>

- <span data-ttu-id="83598-172">**Annulation du blocage des liens fiables**: cette valeur indique également que le destinataire a cliqué sur l’URL de charge utile dans le message. les liens fiables ATP ont tenté de les arrêter, mais ils ont été autorisés à remplacer le blocage.</span><span class="sxs-lookup"><span data-stu-id="83598-172">**Safe Links Block Override**: This value also indicates the recipient clicked on the payload URL in the message, ATP Safe Links tried to stop them, but they were allowed to override the block.</span></span> <span data-ttu-id="83598-173">Vous devez examiner vos [Stratégies de liens fiables](set-up-atp-safe-links-policies.md) pour déterminer la raison pour laquelle les utilisateurs sont autorisés à remplacer les liens de verdict des liens fiables et à cliquer sur URL malveillantes.</span><span class="sxs-lookup"><span data-stu-id="83598-173">You need to investigate your [Safe Links policies](set-up-atp-safe-links-policies.md) to see why users are allowed to override the Safe Links verdict and click on malicious URLs.</span></span>

### <a name="tabs"></a><span data-ttu-id="83598-174">Onglets</span><span class="sxs-lookup"><span data-stu-id="83598-174">Tabs</span></span>

<span data-ttu-id="83598-175">La vue Détails de la campagne comporte plusieurs onglets qui vous permettent d’approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-175">There are several tabs in the campaign details view that allow you to further investigate the campaign.</span></span>

- <span data-ttu-id="83598-176">**Clics d’URL** : si l’URL de la charge utile dans le message d’hameçonnage n’a pas été activé, cette section reste vide.</span><span class="sxs-lookup"><span data-stu-id="83598-176">**URL Clicks**: If the payload URL in the phishing message wasn't clicked, this section will be blank.</span></span> <span data-ttu-id="83598-177">Si un utilisateur a pu cliquer sur l’URL, vous pouvez</span><span class="sxs-lookup"><span data-stu-id="83598-177">If a user was able to click on the URL, you</span></span>

  - <span data-ttu-id="83598-178">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="83598-178">User</span></span>

  - <span data-ttu-id="83598-179">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="83598-179">URL</span></span>

  - <span data-ttu-id="83598-180">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="83598-180">**Click Time**</span></span>

  - <span data-ttu-id="83598-181">**Cliquez sur Action**</span><span class="sxs-lookup"><span data-stu-id="83598-181">Click **Action**.</span></span>

- <span data-ttu-id="83598-182">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="83598-182">**Sender IPs**</span></span>

  - <span data-ttu-id="83598-183">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="83598-183">**Sender IP**<sup>\*</sup></span></span>

  - <span data-ttu-id="83598-184">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="83598-184">**Total Count**</span></span>

  - <span data-ttu-id="83598-185">**Nombre de la boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="83598-185">**Inboxed Count**</span></span>

  - <span data-ttu-id="83598-186">**Nombre de bloqués**</span><span class="sxs-lookup"><span data-stu-id="83598-186">**Blocked Count**</span></span>

  - <span data-ttu-id="83598-187">**SPF réussi**</span><span class="sxs-lookup"><span data-stu-id="83598-187">**SPF Passed**</span></span>

- <span data-ttu-id="83598-188">**Expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="83598-188">**Senders**</span></span>

  - <span data-ttu-id="83598-189">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="83598-189">**Sender**</span></span>

  - <span data-ttu-id="83598-190">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="83598-190">**Total Count**</span></span>

  - <span data-ttu-id="83598-191">**Nombre de la boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="83598-191">**Inboxed Count**</span></span>

  - <span data-ttu-id="83598-192">**Nombre de bloqués**</span><span class="sxs-lookup"><span data-stu-id="83598-192">**Blocked Count**</span></span>

  - <span data-ttu-id="83598-193">**DKIM réussi**</span><span class="sxs-lookup"><span data-stu-id="83598-193">**DKIM Passed**</span></span>

  - <span data-ttu-id="83598-194">**DMARC réussi**</span><span class="sxs-lookup"><span data-stu-id="83598-194">**DMARC Passed**</span></span>

- <span data-ttu-id="83598-195">**Charge utile**</span><span class="sxs-lookup"><span data-stu-id="83598-195">**Payloads**</span></span>

  - <span data-ttu-id="83598-196">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="83598-196">URL</span></span>

  - <span data-ttu-id="83598-197">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="83598-197">**Total Count**</span></span>

<span data-ttu-id="83598-198"><sup>\*</sup> Le fait de cliquer sur cette valeur ouvre un nouveau menu mobile qui contient plus de détails sur l’élément spécifié (utilisateur, URL, etc.) au-dessus de la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-198"><sup>\*</sup> Clicking on this value opens a new flyout that contains more details about the specified item (user, URL, etc.) on top of the campaign details view.</span></span> <span data-ttu-id="83598-199">Pour revenir à la vue Détails de la campagne, cliquez sur **Terminé** dans la nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="83598-199">To return to the campaign details view, click **Done** in the new flyout.</span></span>

### <a name="buttons"></a><span data-ttu-id="83598-200">Boutons</span><span class="sxs-lookup"><span data-stu-id="83598-200">Buttons</span></span>

<span data-ttu-id="83598-201">Les boutons de la vue Détails de la campagne vous permettent d’utiliser le Power Explorer pour approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="83598-201">The buttons in the campaign details view allow you to use the power of Threat Explorer to further investigate the campaign.</span></span>

- <span data-ttu-id="83598-202">**Explorer la campagne**: ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de la valeur **ID de campagne** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="83598-202">**Explore campaign**: Opens a new Threat Explorer search tab using the **Campaign ID** value as the search filter.</span></span>

- <span data-ttu-id="83598-203">**Explorer les messages de la boîte de réception**: ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de la **ID de campagne** et de **emplacement de remise : boîte de réception** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="83598-203">**Explore Inbox messages**: Opens a new Threat Explorer search tab using the **Campaign ID** and **Delivery location: Inbox** as the search filter.</span></span>
