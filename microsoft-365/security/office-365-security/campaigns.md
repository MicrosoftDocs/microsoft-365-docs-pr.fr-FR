---
title: Affichages des campagnes dans Office 365 - Protection avancée contre les menaces
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 40eab14dff8d0c51a35bfbc7a04365a5a025e207
ms.sourcegitcommit: 08a4ee7765f3eba42f0c037c5c564c581e45df3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2020
ms.locfileid: "42637327"
---
# <a name="campaign-views-in-office-365-atp"></a><span data-ttu-id="c86c6-103">Campaign Views dans Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c86c6-103">Campaign Views in Office 365 ATP</span></span>

<span data-ttu-id="c86c6-104">Campaign Views est une fonctionnalité de la protection avancée contre les menaces (ATP) dans le Centre de sécurité et de conformité Office 365 qui identifie et catégorise les attaques par hameçonnage dans le service.</span><span class="sxs-lookup"><span data-stu-id="c86c6-104">Campaign Views is a feature in Advanced Threat Protection (ATP) in the Office 365 Security & Compliance Center that identifies and categorizes phishing attacks in the service.</span></span> <span data-ttu-id="c86c6-105">Campaign Views permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c86c6-105">Campaign Views can help you to:</span></span>

- <span data-ttu-id="c86c6-106">Examiner et répondre efficacement aux attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c86c6-106">Efficiently investigate and respond to phishing attacks.</span></span>

- <span data-ttu-id="c86c6-107">Mieux comprendre l’étendue de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="c86c6-107">Better understand the scope of the attack.</span></span>

- <span data-ttu-id="c86c6-108">Afficher la valeur pour les décideurs.</span><span class="sxs-lookup"><span data-stu-id="c86c6-108">Show value to decision makers.</span></span>

<span data-ttu-id="c86c6-109">Campaign Views vous permet de voir la présentation d’une attaque plus rapidement et plus complètement que n’importe quel autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c86c6-109">Campaign Views lets you see the big picture of an attack faster and more complete than any human.</span></span>

## <a name="what-is-a-campaign"></a><span data-ttu-id="c86c6-110">Qu’est-ce qu’une campagne ?</span><span class="sxs-lookup"><span data-stu-id="c86c6-110">What is a campaign?</span></span>

<span data-ttu-id="c86c6-111">Une campagne est une attaque par e-mail coordonné contre une ou plusieurs organisations.</span><span class="sxs-lookup"><span data-stu-id="c86c6-111">A campaign is a coordinated email attack against one or many organizations.</span></span> <span data-ttu-id="c86c6-112">Les attaques par courrier électronique qui volent les informations d’identification et les données d’entreprise sont un secteur important et lucratif.</span><span class="sxs-lookup"><span data-stu-id="c86c6-112">Email attacks that steal credentials and company data are a big and lucrative industry.</span></span> <span data-ttu-id="c86c6-113">À mesure que les technologies augmentent pour empêcher les attaques, les agresseurs modifient leurs méthodes afin de garantir une réussite continue.</span><span class="sxs-lookup"><span data-stu-id="c86c6-113">As technologies increase in an effort to stop attacks, attackers modify their methods in an effort to ensure continued success.</span></span>

<span data-ttu-id="c86c6-114">Microsoft exploite les grandes quantités de données anti-hameçonnage, anti-courrier indésirable et anti-programme malveillant dans l’ensemble du service Office 365 pour vous aider à identifier les campagnes.</span><span class="sxs-lookup"><span data-stu-id="c86c6-114">Microsoft leverages the vast amounts of anti-phishing, anti-spam, and anti-malware data across the entire Office 365 service to help identify campaigns.</span></span> <span data-ttu-id="c86c6-115">Nous analysons et classifions les informations d’attaque en fonction de plusieurs facteurs.</span><span class="sxs-lookup"><span data-stu-id="c86c6-115">We analyze and classify the attack information according to several factors.</span></span> <span data-ttu-id="c86c6-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c86c6-116">For example:</span></span>

- <span data-ttu-id="c86c6-117">**Sources d’attaque** : adresses IP sources et domaines de l’e-mail de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c86c6-117">**Attack source**: Source IP addresses and sender email domains.</span></span>

- <span data-ttu-id="c86c6-118">**Propriétés du message d’attaque** : le contenu, le style et le ton des messages d’attaques.</span><span class="sxs-lookup"><span data-stu-id="c86c6-118">**Attack message properties**: The content, style, and tone of the attack messages.</span></span>

- <span data-ttu-id="c86c6-119">**Destinataires d’attaques** : domaines de destinataires, fonctions de tâche de destinataire (administrateurs, cadres, etc.), types d’entreprise (grand, petit, public, privé, etc.) et industries.</span><span class="sxs-lookup"><span data-stu-id="c86c6-119">**Attack recipients**: Recipient domains, recipient job functions (admins, executives, etc.), company types (large, small, public, private, etc.), and industries.</span></span>

- <span data-ttu-id="c86c6-120">**Charge utile d’attaque**: liens malveillants, pièces jointes ou autres charges utiles dans les messages d’attaque.</span><span class="sxs-lookup"><span data-stu-id="c86c6-120">**Attack payload**: Malicious links, attachments, or other payloads in the attack messages.</span></span>

<span data-ttu-id="c86c6-121">Une campagne peut être à courte durée de vie ou peut s’étendre sur plusieurs jours, semaines ou mois avec des périodes actives et inactives.</span><span class="sxs-lookup"><span data-stu-id="c86c6-121">A campaign might be short-lived, or could span several days, weeks, or months with active and inactive periods.</span></span> <span data-ttu-id="c86c6-122">Une campagne peut être lancée par rapport à votre organisation, ou votre organisation peut faire partie d’une campagne plus importante sur plusieurs sociétés.</span><span class="sxs-lookup"><span data-stu-id="c86c6-122">A campaign might be launched against your specific organization, or your organization might be part of a larger campaign across multiple companies.</span></span>

## <a name="campaign-views-the-office-365-security--compliance-center"></a><span data-ttu-id="c86c6-123">Campaign Views dans le Centre de sécurité et conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="c86c6-123">Campaign Views the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="c86c6-124">Les vues de campagne sont disponibles dans le [Centre de sécurité & conformité](https://protection.office.com) aux **campagnes**de **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="c86c6-124">Campaign Views is available in the [Security & Compliance Center](https://protection.office.com) at **Threat management** \> **Campaigns**.</span></span>

![Vue d’ensemble des campagnes dans la Centre de sécurité et conformité](../../media/campaigns-overview.png)

<span data-ttu-id="c86c6-126">Vous pouvez également accéder à la vue campagnes à partir de :</span><span class="sxs-lookup"><span data-stu-id="c86c6-126">You can also get to Campaigns View from:</span></span>

- <span data-ttu-id="c86c6-127">**Threat management** \> **Explorer** \> **View** Affichage \> des **campagnes marketing** dans l’Explorateur de gestion des menaces</span><span class="sxs-lookup"><span data-stu-id="c86c6-127">**Threat management** \> **Explorer** \> **View** \> **Campaigns**</span></span>

- <span data-ttu-id="c86c6-128">**Threat management** \> **Explorer** Explorateur \> de gestion des menaces **Afficher** \> **toutes les** \> **campagnes** de messagerie</span><span class="sxs-lookup"><span data-stu-id="c86c6-128">**Threat management** \> **Explorer** \> **View** \> **All email** \> **Campaign**</span></span>

> [!TIP]
> <span data-ttu-id="c86c6-129">Si aucune donnée de campagne n’apparaît, essayez de modifier la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="c86c6-129">If you don't see any campaign data, try changing the date range.</span></span>

<span data-ttu-id="c86c6-130">La page vue d’ensemble présente les informations suivantes sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="c86c6-130">The overview page shows the following information about the campaign:</span></span>

- <span data-ttu-id="c86c6-131">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c86c6-131">**Name**</span></span>

- <span data-ttu-id="c86c6-132">**Exemple d’objet** : la ligne d’objet de l’un des messages de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-132">**Sample subject**: The subject line of one of the messages in the campaign.</span></span> <span data-ttu-id="c86c6-133">Notez que tous les messages de la campagne n’auront pas nécessairement le même objet.</span><span class="sxs-lookup"><span data-stu-id="c86c6-133">Note that all messages in the campaign will not necessarily have the same subject.</span></span>

- <span data-ttu-id="c86c6-134">**Type**: actuellement, cette valeur est toujours **hameçon**.</span><span class="sxs-lookup"><span data-stu-id="c86c6-134">**Type**: Currently, this value is always **Phish**.</span></span>

- <span data-ttu-id="c86c6-135">**Sous-type** : s’il est disponible, il s’agit de la marque faisant l’objet d’un hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-135">**Subtype**: Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="c86c6-136">Lorsque la détection est pilotée par la technologie ATP, le préfixe **ATP** est ajouté à la valeur de sous-type.</span><span class="sxs-lookup"><span data-stu-id="c86c6-136">When the detection is driven by ATP technology, the prefix **ATP-** is added to the subtype value.</span></span>

- <span data-ttu-id="c86c6-137">**Destinataires** : nombre d’utilisateurs qui ont été ciblés par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-137">**Recipients**: The number of users that were targeted by this campaign.</span></span>

- <span data-ttu-id="c86c6-138">**Boîte de réception**: nombre d’utilisateurs ayant reçu des messages de cette campagne dans leur boîte de réception (non remis au courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="c86c6-138">**Inboxed**: The number of users that received messages from this campaign in their Inbox (not delivered to Junk).</span></span>

- <span data-ttu-id="c86c6-139">**Clic**: nombre d’utilisateurs sur lesquels l’utilisateur a cliqué sur l’URL dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c86c6-139">**Clicked**: The number of users that clicked on the URL in the phishing message.</span></span>

- <span data-ttu-id="c86c6-140">**Cliquez sur taux**: pourcentage tel que calculé par «**boîte de réception**sur laquelle l'**utilisateur a cliqué** / ».</span><span class="sxs-lookup"><span data-stu-id="c86c6-140">**Click Rate**: The percentage as calculated by "**Clicked** / **Inboxed**".</span></span> <span data-ttu-id="c86c6-141">Cette valeur est un indicateur de l’efficacité de la campagne et indique si les destinataires ont pu identifier le message en tant qu’hameçonnage et éviter de cliquer sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="c86c6-141">This value is an indicator of the effectiveness of the campaign, and whether the recipients were able to identify the message as phishing and avoid clicking on the payload URL.</span></span>

- <span data-ttu-id="c86c6-142">**Consulté**le nombre d’utilisateurs qui l’ont fait par le biais du site Web de charge utile.</span><span class="sxs-lookup"><span data-stu-id="c86c6-142">**Visited**: How many users actually made it through to the payload website.</span></span> <span data-ttu-id="c86c6-143">S’il y a des valeurs de **clic** , mais que les liens fiables bloquent l’accès au site Web, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c86c6-143">If there are **Clicked** values, but Safe Links blocked access to the website, this value will be zero.</span></span>

<span data-ttu-id="c86c6-144">Lorsque vous cliquez sur le nom d’une campagne, les détails de la campagne s’affichent dans une fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="c86c6-144">When you click on the name of a campaign, the campaign details appears in a flyout.</span></span>

## <a name="campaign-details"></a><span data-ttu-id="c86c6-145">Détails de la campagne</span><span class="sxs-lookup"><span data-stu-id="c86c6-145">Campaign details</span></span>

<span data-ttu-id="c86c6-146">Dans la vue Détails de la campagne, de nombreuses informations sont disponibles sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="c86c6-146">In the campaign details view, a lot of information is available about the campaign:</span></span>

- <span data-ttu-id="c86c6-147">Informations sur la campagne :</span><span class="sxs-lookup"><span data-stu-id="c86c6-147">Campaign information:</span></span>

  - <span data-ttu-id="c86c6-148">**ID**: identificateur unique de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-148">**ID**: The unique campaign identifier.</span></span>

  - <span data-ttu-id="c86c6-149">**Commencé** et **terminé** : le filtre de la plage de dates que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c86c6-149">**Started** and **Ended**: the date range filter you selected.</span></span>

  - <span data-ttu-id="c86c6-150">**Impact**: les données suivantes pour le filtre de plage de dates que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="c86c6-150">**Impact**: The following data for the date range filter you selected:</span></span>
  
    - <span data-ttu-id="c86c6-151">Nombre total de destinataires.</span><span class="sxs-lookup"><span data-stu-id="c86c6-151">The total number of recipients.</span></span>

    - <span data-ttu-id="c86c6-152">Nombre de messages qui ont reçu la boîte de réception (c’est-à-dire remis dans la boîte de réception, et non du courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="c86c6-152">The number of messages that were "Inboxed" (that is, delivered to the Inbox, not to Junk).</span></span>

    - <span data-ttu-id="c86c6-153">Le nombre d’utilisateurs sur lesquels l’utilisateur a cliqué dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c86c6-153">How many users clicked on the URL payload in the phishing message.</span></span>

    - <span data-ttu-id="c86c6-154">Howe nombre d’utilisateurs visitaient l’URL.</span><span class="sxs-lookup"><span data-stu-id="c86c6-154">Howe many users visited the URL.</span></span>

  - <span data-ttu-id="c86c6-155">Chronologie de l’activité de la campagne : lorsque la campagne a commencé et se termine et que le volume de messages s’affiche au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="c86c6-155">A timeline of campaign activity: When the campaign started and ended, and the volume of messages over time.</span></span>

### <a name="campaign-flow"></a><span data-ttu-id="c86c6-156">Flux de la campagne</span><span class="sxs-lookup"><span data-stu-id="c86c6-156">Campaign flow</span></span>

<span data-ttu-id="c86c6-157">Des informations importantes sur la campagne sont présentées dans un diagramme de flux horizontal (appelé diagramme de _Sankey_) dans la section **Flux**.</span><span class="sxs-lookup"><span data-stu-id="c86c6-157">Important details about the campaign are presented in a horizontal flow diagram (known as a _Sankey_ diagram) in the **Flow** section.</span></span> <span data-ttu-id="c86c6-158">Ces détails vous aideront à comprendre les éléments de la campagne et l’impact potentiel au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c86c6-158">These details will help you to understand the elements of the campaign and the potential impact in your organization.</span></span>

![Détails de la campagne ne contenant pas d’URL d’utilisateur](../../media/campaign-details-no-recipient-actions.png)

<span data-ttu-id="c86c6-160">Si vous pointez sur une bande horizontale dans le diagramme, vous pouvez voir le nombre de messages associés (par exemple, les messages d’une adresse IP source particulière, les messages provenant de l’adresse IP source en utilisant le domaine d’expéditeur spécifié, etc.).</span><span class="sxs-lookup"><span data-stu-id="c86c6-160">If you hover over a horizontal band in the diagram, you'll see the number of related messages (for example, messages from a particular source IP, messages from the source IP using the specified sender domain, etc.).</span></span>

<span data-ttu-id="c86c6-161">Le diagramme contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c86c6-161">The diagram contains the following information:</span></span>

- <span data-ttu-id="c86c6-162">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c86c6-162">**Sender IPs**</span></span>

- <span data-ttu-id="c86c6-163">**Domaines de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c86c6-163">**Sender domains**</span></span>

- <span data-ttu-id="c86c6-164">**Filtrer les verdicts**: les valeurs indiquées ici sont liées aux verdicts de hameçonnage et de filtrage du courrier indésirable disponibles, comme décrit dans [les en-têtes de message anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="c86c6-164">**Filter verdicts**: The values here are related to the available phishing and spam filtering verdicts as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="c86c6-165">Les valeurs disponibles sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c86c6-165">The available values are described in the following table:</span></span>

  |<span data-ttu-id="c86c6-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="c86c6-166">Value</span></span>|<span data-ttu-id="c86c6-167">Verdict du filtre de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c86c6-167">Spam filter verdict</span></span>|<span data-ttu-id="c86c6-168">Description</span><span class="sxs-lookup"><span data-stu-id="c86c6-168">Description</span></span>|
  |:-----|:-----|:-----|
  | <span data-ttu-id="c86c6-169">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="c86c6-169">**Allowed**</span></span>|`SFV:SKN` <br/><br/> `SFV:SKI`|<span data-ttu-id="c86c6-170">Le message a été marqué comme n’étant pas un courrier indésirable et/ou a ignoré le filtrage avant d’être évalué par le filtrage du courrier indésirable (par exemple, par une règle de flux de messagerie, également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="c86c6-170">The message was marked as not spam and/or skipped filtering before being evaluated by spam filtering (for example, by a mail flow rule, also known as a transport rule).</span></span><br/><br/><span data-ttu-id="c86c6-171">Le message a ignoré le filtrage du courrier indésirable pour d’autres raisons (par exemple, l’expéditeur et le destinataire semblent être dans la même organisation).</span><span class="sxs-lookup"><span data-stu-id="c86c6-171">The message skipped spam filtering for other reasons (for example, the sender and recipient appear to be in the same organization).</span></span>|
  |<span data-ttu-id="c86c6-172">**Blocked**</span><span class="sxs-lookup"><span data-stu-id="c86c6-172">**Blocked**</span></span>|`SFV:SKS`|<span data-ttu-id="c86c6-173">Le message a été marqué comme courrier indésirable avant d’être évalué par le filtrage du courrier indésirable (par exemple, par une règle de flux de messagerie).</span><span class="sxs-lookup"><span data-stu-id="c86c6-173">The message was marked as spam before being evaluated by spam filtering (for example, by a mail flow rule).</span></span>|
  |<span data-ttu-id="c86c6-174">**Détecté**</span><span class="sxs-lookup"><span data-stu-id="c86c6-174">**Detected**</span></span>|`SFV:SPM`|<span data-ttu-id="c86c6-175">Le message a été marqué comme courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c86c6-175">The message was marked as spam by spam filtering.</span></span>|
  |<span data-ttu-id="c86c6-176">**Non détecté**</span><span class="sxs-lookup"><span data-stu-id="c86c6-176">**Not Detected**</span></span>|`SFV:NSPM`|<span data-ttu-id="c86c6-177">Le message a été marqué comme non courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c86c6-177">The message was marked as not spam by spam filtering.</span></span>|
  |<span data-ttu-id="c86c6-178">**A**</span><span class="sxs-lookup"><span data-stu-id="c86c6-178">**Released**</span></span>|`SFV:SKQ`|<span data-ttu-id="c86c6-179">Le message a ignoré le filtrage du courrier indésirable, car il a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c86c6-179">The message skipped spam filtering because it was released from quarantine.</span></span>|
  |<span data-ttu-id="c86c6-180">**Autoriser le client**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-180">**Tenant Allow**<sup>\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="c86c6-181">Le message a ignoré le filtrage du courrier indésirable en raison des paramètres de stratégie de blocage du courrier indésirable (par exemple, l’expéditeur se trouvait dans la liste des expéditeurs autorisés ou le domaine autorisé).</span><span class="sxs-lookup"><span data-stu-id="c86c6-181">The message skipped spam filtering due to anti-spam policy settings (for example, the sender was in the allowed sender list or allowed domain list).</span></span>|
  |<span data-ttu-id="c86c6-182">**Bloc de locataire**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-182">**Tenant Block**<sup>\*\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="c86c6-183">Le message a été bloqué par le filtrage du courrier indésirable en raison des paramètres de stratégie de blocage du courrier indésirable (par exemple, l’expéditeur se trouvait dans la liste des expéditeurs autorisés ou le domaine autorisé).</span><span class="sxs-lookup"><span data-stu-id="c86c6-183">The message was blocked by spam filtering due to anti-spam policy settings (for example, the sender was in the allowed sender list or allowed domain list).</span></span>|
  |<span data-ttu-id="c86c6-184">**Autorisation de l’utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-184">**User Allow**<sup>\*</sup></span></span>|`SFV:SFE`|<span data-ttu-id="c86c6-185">Le message a ignoré le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs approuvés d’un utilisateur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="c86c6-185">The message skipped spam filtering because the sender was in a user's Safe Senders list in Outlook.</span></span>|
  |<span data-ttu-id="c86c6-186">**Bloc utilisateur**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-186">**User Block**<sup>\*\*</sup></span></span>|`SFV:BLK`|<span data-ttu-id="c86c6-187">Le message a été bloqué par le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs bloqués d’un utilisateur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="c86c6-187">The message was blocked by spam filtering because the sender was in a user's Blocked Senders list in Outlook.</span></span>|
  |<span data-ttu-id="c86c6-188">**ZAP**</span><span class="sxs-lookup"><span data-stu-id="c86c6-188">**ZAP**</span></span>|<span data-ttu-id="c86c6-189">s/o</span><span class="sxs-lookup"><span data-stu-id="c86c6-189">n/a</span></span>|<span data-ttu-id="c86c6-190">La [purge automatique à zéro heure (ZAP)](zero-hour-auto-purge.md) a effectué une action sur le message remis en fonction de vos paramètres de stratégie anti-courrier indésirable (déplacés vers le dossier courrier indésirable ou mis en quarantaine).</span><span class="sxs-lookup"><span data-stu-id="c86c6-190">[Zero-hour auto purge (ZAP)](zero-hour-auto-purge.md) took action on the delivered message according to your anti-spam policy settings (moved to the Junk Email folder or Quarantined).</span></span>|

  <span data-ttu-id="c86c6-191"><sup>\*</sup>Examinez vos stratégies de blocage du courrier indésirable, car le message autorisé aurait probablement été bloqué par le service.</span><span class="sxs-lookup"><span data-stu-id="c86c6-191"><sup>\*</sup> Review your anti-spam policies, because the allowed message would have likely been blocked by the service.</span></span>

  <span data-ttu-id="c86c6-192"><sup>\*\*</sup>Examinez vos stratégies de blocage du courrier indésirable, car ces messages doivent être mis en quarantaine et non remis.</span><span class="sxs-lookup"><span data-stu-id="c86c6-192"><sup>\*\*</sup> Review your anti-spam policies, because these messages should be quarantined, not delivered.</span></span>

- <span data-ttu-id="c86c6-193">**Emplacements de remise**: vous souhaiterez peut-être examiner les messages qui ont été remis aux destinataires (soit dans la boîte de réception, soit dans le dossier courrier indésirable), même si les utilisateurs n'ont pas cliqué sur l'URL de la charge utile dans le message.</span><span class="sxs-lookup"><span data-stu-id="c86c6-193">**Delivery locations**: You'll likely want to investigate messages that were actually delivered to recipients (either to the Inbox or the Junk Email folder), even if users didn't click on the payload URL in the message.</span></span> <span data-ttu-id="c86c6-194">Vous pouvez également supprimer les messages mis en quarantaine en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c86c6-194">You can also remove the quarantined messages from quarantine.</span></span> <span data-ttu-id="c86c6-195">Pour plus d’informations, consultez la rubrique [mise en quarantaine des messages électroniques dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c86c6-195">For more information, see [Quarantine email messages in Office 365](quarantine-email-messages.md).</span></span>

  - <span data-ttu-id="c86c6-196">**Dossier supprimé**</span><span class="sxs-lookup"><span data-stu-id="c86c6-196">**Deleted folder**</span></span>

  - <span data-ttu-id="c86c6-197">**Raccroché**</span><span class="sxs-lookup"><span data-stu-id="c86c6-197">**Dropped**</span></span>

  - <span data-ttu-id="c86c6-198">**External**: le destinataire est situé dans votre organisation de messagerie locale.</span><span class="sxs-lookup"><span data-stu-id="c86c6-198">**External**: The recipient is located in your on-premises email organization.</span></span>

  - <span data-ttu-id="c86c6-199">**Échec**</span><span class="sxs-lookup"><span data-stu-id="c86c6-199">**Failed**</span></span>

  - <span data-ttu-id="c86c6-200">**Renvoyé**</span><span class="sxs-lookup"><span data-stu-id="c86c6-200">**Forwarded**</span></span>

  - <span data-ttu-id="c86c6-201">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="c86c6-201">**Inbox**</span></span>

  - <span data-ttu-id="c86c6-202">**Dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="c86c6-202">**Junk folder**</span></span>

  - <span data-ttu-id="c86c6-203">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="c86c6-203">**Quarantine**</span></span>

  - <span data-ttu-id="c86c6-204">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="c86c6-204">**Unknown**</span></span>

> [!NOTE]
> <span data-ttu-id="c86c6-205">Dans toutes les couches contenant plus de 10 éléments, les 10 premiers éléments sont affichés, tandis que les autres sont regroupés dans les **autres**.</span><span class="sxs-lookup"><span data-stu-id="c86c6-205">In all layers that contain more than 10 items, the top 10 items are shown, while the rest are bundled together in **Others**.</span></span>

#### <a name="url-clicks"></a><span data-ttu-id="c86c6-206">Clics d’URL</span><span class="sxs-lookup"><span data-stu-id="c86c6-206">URL clicks</span></span>

<span data-ttu-id="c86c6-207">Lorsqu’un message d’hameçonnage est remis à un destinataire (dans la boîte de réception ou dans le dossier courrier indésirable), il y a toujours un risque que l’utilisateur clique sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="c86c6-207">When a phishing message is delivered to a recipient (to the Inbox or the Junk Email folder), there's always a chance that the user will click on the payload URL.</span></span> <span data-ttu-id="c86c6-208">Le fait de ne pas cliquer sur l’URL dans un message remis est une petite mesure de succès, mais vous devez déterminer pourquoi le message de hameçonnage a été remis à sa boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c86c6-208">Not clicking on the URL in a delivered message is a small measure of success, but you need to determine why the phishing message was delivered to their mailbox in the first place.</span></span>

<span data-ttu-id="c86c6-209">Si un utilisateur a cliqué sur l’URL de la charge utile dans le message d’hameçonnage, les actions sont affichées dans la zone de **clics sur l’URL** du diagramme dans la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-209">If a user clicked on the payload URL in the phishing message, the actions are displayed in the **URL clicks** area of the diagram in the campaign details view.</span></span>

- <span data-ttu-id="c86c6-210">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="c86c6-210">**Allowed**</span></span>

- <span data-ttu-id="c86c6-211">**BlockPage**: le destinataire a cliqué sur l’URL de charge utile, mais son accès au site Web malveillant a été bloqué par les stratégies de [liens fiables ATP](atp-safe-links.md) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c86c6-211">**BlockPage**: The recipient clicked on the payload URL, but their access to the malicious website was blocked by the [ATP Safe Links](atp-safe-links.md) policies in your organization.</span></span>

- <span data-ttu-id="c86c6-212">**BlockPageOverride**: le destinataire a cliqué sur l’URL de charge utile dans le message, les liens fiables ATP ont essayé de les arrêter, mais ils ont été autorisés à remplacer le bloc.</span><span class="sxs-lookup"><span data-stu-id="c86c6-212">**BlockPageOverride**: The recipient clicked on the payload URL in the message, ATP Safe Links tried to stop them, but they were allowed to override the block.</span></span> <span data-ttu-id="c86c6-213">Vous devez examiner vos [stratégies de liens fiables](set-up-atp-safe-links-policies.md) pour savoir pourquoi les utilisateurs sont autorisés à remplacer le verdict des liens fiables et continuer à accéder au site Web malveillant.</span><span class="sxs-lookup"><span data-stu-id="c86c6-213">You need to investigate your [Safe Links policies](set-up-atp-safe-links-policies.md) to see why users are allowed to override the Safe Links verdict and continue to the malicious website.</span></span>

- <span data-ttu-id="c86c6-214">**PendingDetonationPage**: les pièces jointes de protection avancée contre les menaces sont en cours d’ouverture de l’URL de charge utile dans un environnement d’ordinateur virtuel et de l’affichage de ce qui se passe.</span><span class="sxs-lookup"><span data-stu-id="c86c6-214">**PendingDetonationPage**: ATP Safe Attachments is in the process of opening the payload URL in a virtual computer environment, and seeing what happens.</span></span>

- <span data-ttu-id="c86c6-215">**PendingDetonationPageOverride**: le destinataire a été autorisé à remplacer le processus de détonation de charge utile et à ouvrir l’URL sans attendre les résultats.</span><span class="sxs-lookup"><span data-stu-id="c86c6-215">**PendingDetonationPageOverride**: The recipient was allowed to override the payload detonation process and open the URL without waiting for the results.</span></span>

### <a name="tabs"></a><span data-ttu-id="c86c6-216">Onglets</span><span class="sxs-lookup"><span data-stu-id="c86c6-216">Tabs</span></span>

<span data-ttu-id="c86c6-217">La vue Détails de la campagne comporte plusieurs onglets qui vous permettent d’approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-217">There are several tabs in the campaign details view that allow you to further investigate the campaign.</span></span>

- <span data-ttu-id="c86c6-218">**Clics**sur l’URL : si les utilisateurs ne cliquent pas sur l’URL de la charge utile dans le message d’hameçonnage, cette section est vide.</span><span class="sxs-lookup"><span data-stu-id="c86c6-218">**URL Clicks**: If users didn't click on the payload URL in the phishing message, this section will be blank.</span></span> <span data-ttu-id="c86c6-219">Si un utilisateur a pu cliquer sur l’URL, les valeurs suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="c86c6-219">If a user was able to click on the URL, the following values will be populated:</span></span>

  - <span data-ttu-id="c86c6-220">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-220">**User**<sup>\*</sup></span></span>

  - <span data-ttu-id="c86c6-221">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-221">**URL**<sup>\*</sup></span></span>

  - <span data-ttu-id="c86c6-222">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="c86c6-222">**Click Time**</span></span>

  - <span data-ttu-id="c86c6-223">**Cliquez sur Action**</span><span class="sxs-lookup"><span data-stu-id="c86c6-223">**Click Action**</span></span>

- <span data-ttu-id="c86c6-224">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c86c6-224">**Sender IPs**</span></span>

  - <span data-ttu-id="c86c6-225">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-225">**Sender IP**<sup>\*</sup></span></span>

  - <span data-ttu-id="c86c6-226">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="c86c6-226">**Total Count**</span></span>

  - <span data-ttu-id="c86c6-227">**Nombre de la boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="c86c6-227">**Inboxed Count**</span></span>

  - <span data-ttu-id="c86c6-228">**Nombre de bloqués**</span><span class="sxs-lookup"><span data-stu-id="c86c6-228">**Blocked Count**</span></span>

  - <span data-ttu-id="c86c6-229">**SPF transmis**: l’expéditeur a été authentifié par [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="c86c6-229">**SPF Passed**: The sender was authenticated by the [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="c86c6-230">Un expéditeur qui ne passe pas la validation SPF indique que l’expéditeur n’est pas authentifié, ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="c86c6-230">A sender that does not pass SPF validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="c86c6-231">**Expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="c86c6-231">**Senders**</span></span>

  - <span data-ttu-id="c86c6-232">**Expéditeur**: il s’agit de l’adresse de l’expéditeur réelle dans la commande SMTP Mail from, qui n’est pas nécessairement l’adresse de messagerie de l’expéditeur que les utilisateurs voient dans leurs clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c86c6-232">**Sender**: This is the actual sender address in the SMTP MAIL FROM command, which is not necessarily the From: email address that users see in their email clients.</span></span>

  - <span data-ttu-id="c86c6-233">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="c86c6-233">**Total Count**</span></span>

  - <span data-ttu-id="c86c6-234">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="c86c6-234">**Inboxed**</span></span>

  - <span data-ttu-id="c86c6-235">**Pas de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="c86c6-235">**Not Inboxed**</span></span>

  - <span data-ttu-id="c86c6-236">**DKIM transmis**: l’expéditeur a été authentifié par des [clés de domaine identifiées par des clés de domaine (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c86c6-236">**DKIM Passed**: The sender was authenticated by [Domain Keys Identified Mail (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span></span> <span data-ttu-id="c86c6-237">Un expéditeur qui ne passe pas la validation DKIM indique que l’expéditeur n’est pas authentifié, ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="c86c6-237">A sender that does not pass DKIM validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>

  - <span data-ttu-id="c86c6-238">**DMARC réussi**: l’expéditeur a été authentifié par [l’authentification de message basée sur un domaine, la création de rapports et la conformité (DMARC)](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="c86c6-238">**DMARC Passed**: The sender was authenticated by [Domain-based Message Authentication, Reporting, and Conformance (DMARC)](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="c86c6-239">Un expéditeur qui ne réussit pas la validation DMARC indique que l’expéditeur n’est pas authentifié ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="c86c6-239">A sender that does not pass DMARC validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="c86c6-240">**Charge utile**</span><span class="sxs-lookup"><span data-stu-id="c86c6-240">**Payloads**</span></span>

  - <span data-ttu-id="c86c6-241">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c86c6-241">**URL**<sup>\*</sup></span></span>

  - <span data-ttu-id="c86c6-242">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="c86c6-242">**Total Count**</span></span>

<span data-ttu-id="c86c6-243"><sup>\*</sup> Le fait de cliquer sur cette valeur ouvre un nouveau menu mobile qui contient plus de détails sur l’élément spécifié (utilisateur, URL, etc.) au-dessus de la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-243"><sup>\*</sup> Clicking on this value opens a new flyout that contains more details about the specified item (user, URL, etc.) on top of the campaign details view.</span></span> <span data-ttu-id="c86c6-244">Pour revenir à la vue Détails de la campagne, cliquez sur **Terminé** dans la nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="c86c6-244">To return to the campaign details view, click **Done** in the new flyout.</span></span>

### <a name="buttons"></a><span data-ttu-id="c86c6-245">Boutons</span><span class="sxs-lookup"><span data-stu-id="c86c6-245">Buttons</span></span>

<span data-ttu-id="c86c6-246">Les boutons de la vue Détails de la campagne vous permettent d’utiliser le Power Explorer pour approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c86c6-246">The buttons in the campaign details view allow you to use the power of Threat Explorer to further investigate the campaign.</span></span>

- <span data-ttu-id="c86c6-247">**Explorer la campagne**: ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de la valeur **ID de campagne** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="c86c6-247">**Explore campaign**: Opens a new Threat Explorer search tab using the **Campaign ID** value as the search filter.</span></span>

- <span data-ttu-id="c86c6-248">**Explorer les messages**de la boîte de réception : ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de l' **ID de campagne** et de l' **emplacement de remise : boîte de réception** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="c86c6-248">**Explore Inboxed messages**: Opens a new Threat Explorer search tab using the **Campaign ID** and **Delivery location: Inbox** as the search filter.</span></span>
