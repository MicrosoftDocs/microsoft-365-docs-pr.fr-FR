---
title: Affichages de campagne dans la protection avancée contre les menaces
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
ms.openlocfilehash: b7078188d8e01f27e6941c3f61f4ef20a004606c
ms.sourcegitcommit: 6a1a8aa024fd685d04da97bfcbc8eadacc488534
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46653232"
---
# <a name="campaign-views-in-atp"></a><span data-ttu-id="4276b-103">Affichages de campagne dans la protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="4276b-103">Campaign Views in ATP</span></span>

<span data-ttu-id="4276b-104">Les vues de campagne sont une fonctionnalité de la protection avancée contre les menaces (ATP) dans le centre de sécurité & conformité qui identifie et catégorise les attaques par hameçonnage dans le service.</span><span class="sxs-lookup"><span data-stu-id="4276b-104">Campaign Views is a feature in Advanced Threat Protection (ATP) in the Security & Compliance Center that identifies and categorizes phishing attacks in the service.</span></span> <span data-ttu-id="4276b-105">Campaign Views permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4276b-105">Campaign Views can help you to:</span></span>

- <span data-ttu-id="4276b-106">Examiner et répondre efficacement aux attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4276b-106">Efficiently investigate and respond to phishing attacks.</span></span>

- <span data-ttu-id="4276b-107">Mieux comprendre l’étendue de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="4276b-107">Better understand the scope of the attack.</span></span>

- <span data-ttu-id="4276b-108">Afficher la valeur pour les décideurs.</span><span class="sxs-lookup"><span data-stu-id="4276b-108">Show value to decision makers.</span></span>

<span data-ttu-id="4276b-109">Campaign Views vous permet de voir la présentation d’une attaque plus rapidement et plus complètement que n’importe quel autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4276b-109">Campaign Views lets you see the big picture of an attack faster and more complete than any human.</span></span>

## <a name="what-is-a-campaign"></a><span data-ttu-id="4276b-110">Qu’est-ce qu’une campagne ?</span><span class="sxs-lookup"><span data-stu-id="4276b-110">What is a campaign?</span></span>

<span data-ttu-id="4276b-111">Une campagne est une attaque par e-mail coordonné contre une ou plusieurs organisations.</span><span class="sxs-lookup"><span data-stu-id="4276b-111">A campaign is a coordinated email attack against one or many organizations.</span></span> <span data-ttu-id="4276b-112">Les attaques par courrier électronique qui volent les informations d’identification et les données d’entreprise sont un secteur important et lucratif.</span><span class="sxs-lookup"><span data-stu-id="4276b-112">Email attacks that steal credentials and company data are a big and lucrative industry.</span></span> <span data-ttu-id="4276b-113">À mesure que les technologies augmentent pour empêcher les attaques, les agresseurs modifient leurs méthodes afin de garantir une réussite continue.</span><span class="sxs-lookup"><span data-stu-id="4276b-113">As technologies increase in an effort to stop attacks, attackers modify their methods in an effort to ensure continued success.</span></span>

<span data-ttu-id="4276b-114">Microsoft exploite les grandes quantités de données anti-hameçonnage, de blocage du courrier indésirable et anti-programme malveillant dans l’ensemble du service afin d’identifier les campagnes.</span><span class="sxs-lookup"><span data-stu-id="4276b-114">Microsoft leverages the vast amounts of anti-phishing, anti-spam, and anti-malware data across the entire service to help identify campaigns.</span></span> <span data-ttu-id="4276b-115">Nous analysons et classifions les informations d’attaque en fonction de plusieurs facteurs.</span><span class="sxs-lookup"><span data-stu-id="4276b-115">We analyze and classify the attack information according to several factors.</span></span> <span data-ttu-id="4276b-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4276b-116">For example:</span></span>

- <span data-ttu-id="4276b-117">**Source**de l’attaque : les adresses IP source et les domaines de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4276b-117">**Attack source**: The source IP addresses and sender email domains.</span></span>

- <span data-ttu-id="4276b-118">**Propriétés des messages d’attaque**: le contenu, le style et la tonalité des messages.</span><span class="sxs-lookup"><span data-stu-id="4276b-118">**Attack message properties**: The content, style, and tone of the messages.</span></span>

- <span data-ttu-id="4276b-119">**Destinataires d’attaques** : domaines de destinataires, fonctions de tâche de destinataire (administrateurs, cadres, etc.), types d’entreprise (grand, petit, public, privé, etc.) et industries.</span><span class="sxs-lookup"><span data-stu-id="4276b-119">**Attack recipients**: Recipient domains, recipient job functions (admins, executives, etc.), company types (large, small, public, private, etc.), and industries.</span></span>

- <span data-ttu-id="4276b-120">**Charge utile d’attaque**: liens malveillants, pièces jointes ou autres charges utiles dans les messages.</span><span class="sxs-lookup"><span data-stu-id="4276b-120">**Attack payload**: Malicious links, attachments, or other payloads in the messages.</span></span>

<span data-ttu-id="4276b-121">Une campagne peut être à courte durée de vie ou peut s’étendre sur plusieurs jours, semaines ou mois avec des périodes actives et inactives.</span><span class="sxs-lookup"><span data-stu-id="4276b-121">A campaign might be short-lived, or could span several days, weeks, or months with active and inactive periods.</span></span> <span data-ttu-id="4276b-122">Une campagne peut être lancée par rapport à votre organisation, ou votre organisation peut faire partie d’une campagne plus importante sur plusieurs sociétés.</span><span class="sxs-lookup"><span data-stu-id="4276b-122">A campaign might be launched against your specific organization, or your organization might be part of a larger campaign across multiple companies.</span></span>

## <a name="campaign-views-the-security--compliance-center"></a><span data-ttu-id="4276b-123">Vue de campagne du centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="4276b-123">Campaign Views the Security & Compliance Center</span></span>

<span data-ttu-id="4276b-124">Les vues de campagne sont disponibles dans le [Centre de sécurité & conformité](https://protection.office.com) aux **Threat management** \> **campagnes**gestion des menaces ou directement sur le <https://protection.office.com/campaigns> .</span><span class="sxs-lookup"><span data-stu-id="4276b-124">Campaign Views is available in the [Security & Compliance Center](https://protection.office.com) at **Threat management** \> **Campaigns**, or directly at <https://protection.office.com/campaigns>.</span></span>

![Vue d’ensemble des campagnes dans la Centre de sécurité et conformité](../../media/campaigns-overview.png)

<span data-ttu-id="4276b-126">Vous pouvez également accéder aux vues de campagne à partir de :</span><span class="sxs-lookup"><span data-stu-id="4276b-126">You can also get to Campaign Views from:</span></span>

- <span data-ttu-id="4276b-127">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Campagnes marketing**</span><span class="sxs-lookup"><span data-stu-id="4276b-127">**Threat management** \> **Explorer** \> **View** \> **Campaigns**</span></span>

- <span data-ttu-id="4276b-128">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Tous les messages électroniques** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="4276b-128">**Threat management** \> **Explorer** \> **View** \> **All email** \> **Campaign** tab</span></span>

- <span data-ttu-id="4276b-129">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Hameçonnage** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="4276b-129">**Threat management** \> **Explorer** \> **View** \> **Phish** \> **Campaign** tab</span></span>

- <span data-ttu-id="4276b-130">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Programmes malveillants** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="4276b-130">**Threat management** \> **Explorer** \> **View** \> **Malware** \> **Campaign** tab</span></span>

<span data-ttu-id="4276b-131">Pour accéder aux vues de campagne, vous devez être membre des groupes de rôles gestion de l' **organisation**, administrateur de la **sécurité**ou **lecteur de sécurité** dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="4276b-131">To access Campaign Views, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Reader** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="4276b-132">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-132">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="campaigns-overview"></a><span data-ttu-id="4276b-133">Vue d’ensemble des campagnes</span><span class="sxs-lookup"><span data-stu-id="4276b-133">Campaigns overview</span></span>

<span data-ttu-id="4276b-134">La page vue d’ensemble affiche des informations sur toutes les campagnes.</span><span class="sxs-lookup"><span data-stu-id="4276b-134">The overview page shows information about all campaigns.</span></span>

<span data-ttu-id="4276b-135">Sous l’onglet **campagne** par défaut, la zone **type de campagne** affiche un graphique à barres qui indique le nombre de destinataires par jour.</span><span class="sxs-lookup"><span data-stu-id="4276b-135">On the default **Campaign** tab, the **Campaign type** area shows a bar graph that shows the number of recipients per day.</span></span> <span data-ttu-id="4276b-136">Par défaut, le graphique affiche les données de **hameçonnage** et de **programmes malveillants** .</span><span class="sxs-lookup"><span data-stu-id="4276b-136">By default, the graph shows both **Phish** and **Malware** data.</span></span>

> [!TIP]
> <span data-ttu-id="4276b-137">Si vous ne voyez pas de données de campagne, essayez de modifier la plage de dates ou les [filtres](#filters-and-settings).</span><span class="sxs-lookup"><span data-stu-id="4276b-137">If you don't see any campaign data, try changing the date range or [filters](#filters-and-settings).</span></span>

<span data-ttu-id="4276b-138">Le reste de la page vue d’ensemble affiche les informations suivantes dans l’onglet **campagne** :</span><span class="sxs-lookup"><span data-stu-id="4276b-138">The rest of the overview page shows the following information on the **Campaign** tab:</span></span>

- <span data-ttu-id="4276b-139">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4276b-139">**Name**</span></span>

- <span data-ttu-id="4276b-140">**Exemple d’objet** : la ligne d’objet de l’un des messages de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-140">**Sample subject**: The subject line of one of the messages in the campaign.</span></span> <span data-ttu-id="4276b-141">Notez que tous les messages de la campagne n’auront pas nécessairement le même objet.</span><span class="sxs-lookup"><span data-stu-id="4276b-141">Note that all messages in the campaign will not necessarily have the same subject.</span></span>

- <span data-ttu-id="4276b-142">**Ciblé**: pourcentage tel que calculé par : (nombre de destinataires de campagne dans votre organisation)/(nombre total de destinataires dans la campagne pour toutes les organisations du service).</span><span class="sxs-lookup"><span data-stu-id="4276b-142">**Targeted**: The percentage as calculated by: (the number of campaign recipients in your organization) / (the total number of recipients in the campaign across all organizations in the service).</span></span> <span data-ttu-id="4276b-143">Cette valeur indique le degré auquel la campagne est spécifiquement dirigée au sein de votre organisation (valeur la plus élevée) par rapport aux autres organisations du service (une valeur inférieure).</span><span class="sxs-lookup"><span data-stu-id="4276b-143">This value indicates the degree to which the campaign is specifically directed at your organization (a higher value) vs. directed at other organizations in the service (a lower value).</span></span>

- <span data-ttu-id="4276b-144">**Type**: cette valeur est **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="4276b-144">**Type**: This value is either **Phish** or **Malware**.</span></span>

- <span data-ttu-id="4276b-145">**Sous-type**: cette valeur contient davantage de détails sur la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-145">**Subtype**: This value contains more details about the campaign.</span></span> <span data-ttu-id="4276b-146">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4276b-146">For example:</span></span>

  - <span data-ttu-id="4276b-147">**Hameçonnage**: le cas échéant, la marque qui est en hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-147">**Phish**: Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="4276b-148">Par exemple,,,, `Microsoft` `365` `Unknown` `Outlook` ou `DocuSign` .</span><span class="sxs-lookup"><span data-stu-id="4276b-148">For example, `Microsoft`, `365`, `Unknown`, `Outlook`, or `DocuSign`.</span></span>

  - <span data-ttu-id="4276b-149">**Programme malveillant**: par exemple, `HTML/PHISH` ou `HTML/<MalwareFamilyName>` .</span><span class="sxs-lookup"><span data-stu-id="4276b-149">**Malware**: For example, `HTML/PHISH` or `HTML/<MalwareFamilyName>`.</span></span>

<span data-ttu-id="4276b-150">Le cas échéant, la marque en cours d’hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-150">Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="4276b-151">Lorsque la détection est pilotée par la technologie ATP, le préfixe **ATP** est ajouté à la valeur de sous-type.</span><span class="sxs-lookup"><span data-stu-id="4276b-151">When the detection is driven by ATP technology, the prefix **ATP-** is added to the subtype value.</span></span>

- <span data-ttu-id="4276b-152">**Destinataires** : nombre d’utilisateurs qui ont été ciblés par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-152">**Recipients**: The number of users that were targeted by this campaign.</span></span>

- <span data-ttu-id="4276b-153">**Boîte de réception**: nombre d’utilisateurs ayant reçu des messages de cette campagne dans leur boîte de réception (non remis dans leur dossier courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="4276b-153">**Inboxed**: The number of users that received messages from this campaign in their Inbox (not delivered to their Junk Email folder).</span></span>

- <span data-ttu-id="4276b-154">**Clic**: nombre d’utilisateurs sur lesquels l’utilisateur a cliqué sur l’URL ou pour ouvrir la pièce jointe dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4276b-154">**Clicked**: The number of users that clicked on the URL or opened the attachment in the phishing message.</span></span>

- <span data-ttu-id="4276b-155">**Cliquez sur taux**: pourcentage tel que calculé par « boîte de réception sur laquelle l'**utilisateur a cliqué**  /  **Inboxed**».</span><span class="sxs-lookup"><span data-stu-id="4276b-155">**Click rate**: The percentage as calculated by "**Clicked** / **Inboxed**".</span></span> <span data-ttu-id="4276b-156">Cette valeur est un indicateur de l’efficacité de la campagne et indique si les destinataires ont pu identifier le message en tant qu’hameçonnage et éviter de cliquer sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="4276b-156">This value is an indicator of the effectiveness of the campaign, and whether the recipients were able to identify the message as phishing and avoid clicking on the payload URL.</span></span>

  <span data-ttu-id="4276b-157">Notez que cette valeur n’est pas utilisée dans les campagnes de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4276b-157">Note that this value isn't used in malware campaigns.</span></span>

- <span data-ttu-id="4276b-158">**Consulté**le nombre d’utilisateurs qui l’ont fait par le biais du site Web de charge utile.</span><span class="sxs-lookup"><span data-stu-id="4276b-158">**Visited**: How many users actually made it through to the payload website.</span></span> <span data-ttu-id="4276b-159">S’il y a des valeurs de **clic** , mais que les liens fiables bloquent l’accès au site Web, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4276b-159">If there are **Clicked** values, but Safe Links blocked access to the website, this value will be zero.</span></span>

<span data-ttu-id="4276b-160">L’onglet origine de la **campagne** affiche les sources de messages sur une carte du monde.</span><span class="sxs-lookup"><span data-stu-id="4276b-160">The **Campaign origin** tab shows the message sources on a map of the world.</span></span>

### <a name="filters-and-settings"></a><span data-ttu-id="4276b-161">Filtres et paramètres</span><span class="sxs-lookup"><span data-stu-id="4276b-161">Filters and settings</span></span>

<span data-ttu-id="4276b-162">En haut de la page vues de la campagne, il existe plusieurs paramètres de filtre et de requête qui vous permettent de trouver et d’isoler des campagnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4276b-162">At the top of the Campaign Views page, there are several filter and query settings to help you find and isolate specific campaigns.</span></span>

![Filtres de campagne](../../media/campaign-filters-and-settings.png)

<span data-ttu-id="4276b-164">Le filtrage le plus élémentaire que vous pouvez faire est la date/l’heure de début et la date/heure de fin.</span><span class="sxs-lookup"><span data-stu-id="4276b-164">The most basic filtering that you can do is the start date/time and the end date/time.</span></span>

<span data-ttu-id="4276b-165">Pour filtrer davantage l’affichage, vous pouvez effectuer une seule propriété avec plusieurs valeurs de filtrage en cliquant sur le bouton **type de campagne** , en sélectionnant l’option **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="4276b-165">To further filter the view, you can do single property with multiple values filtering by clicking the **Campaign type** button, making your selection, and then clicking **Refresh**.</span></span>

<span data-ttu-id="4276b-166">Les propriétés de la campagne disponibles sont décrites dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="4276b-166">The available campaign properties are described in the following list:</span></span>

- <span data-ttu-id="4276b-167">De base</span><span class="sxs-lookup"><span data-stu-id="4276b-167">Basic</span></span>

  - <span data-ttu-id="4276b-168">**Type de campagne**: sélectionnez **programme malveillant** ou **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="4276b-168">**Campaign type**: Select **Malware** or **Phish**.</span></span> <span data-ttu-id="4276b-169">L’effacement des sélections a le même résultat que la sélection des deux.</span><span class="sxs-lookup"><span data-stu-id="4276b-169">Clearing the selections has the same result as selecting both.</span></span>
  - <span data-ttu-id="4276b-170">**Nom de la campagne**</span><span class="sxs-lookup"><span data-stu-id="4276b-170">**Campaign name**</span></span>
  - <span data-ttu-id="4276b-171">**Sous-type de campagne**</span><span class="sxs-lookup"><span data-stu-id="4276b-171">**Campaign subtype**</span></span>
  - <span data-ttu-id="4276b-172">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-172">**Sender**</span></span>
  - <span data-ttu-id="4276b-173">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="4276b-173">**Recipients**</span></span>
  - <span data-ttu-id="4276b-174">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-174">**Sender domain**</span></span>
  - <span data-ttu-id="4276b-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="4276b-175">**Subject**</span></span>
  - <span data-ttu-id="4276b-176">**Nom de fichier des pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="4276b-176">**Attachment filename**</span></span>
  - <span data-ttu-id="4276b-177">**Famille de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="4276b-177">**Malware family**</span></span>
  - <span data-ttu-id="4276b-178">**Action de remise**</span><span class="sxs-lookup"><span data-stu-id="4276b-178">**Delivery action**</span></span>
  - <span data-ttu-id="4276b-179">**Technologie de détection**</span><span class="sxs-lookup"><span data-stu-id="4276b-179">**Detection technology**</span></span>
  - <span data-ttu-id="4276b-180">**Tags**</span><span class="sxs-lookup"><span data-stu-id="4276b-180">**Tags**</span></span>
  - <span data-ttu-id="4276b-181">**Substitutions système**</span><span class="sxs-lookup"><span data-stu-id="4276b-181">**System overrides**</span></span>

- <span data-ttu-id="4276b-182">Avancé</span><span class="sxs-lookup"><span data-stu-id="4276b-182">Advanced</span></span>

  - <span data-ttu-id="4276b-183">**ID de message Internet**: disponible dans le champ d’en-tête **message-ID** de l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="4276b-183">**Internet message ID**: Available in the **Message-ID** header field in the message header.</span></span> <span data-ttu-id="4276b-184">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (Notez les chevrons).</span><span class="sxs-lookup"><span data-stu-id="4276b-184">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
  
  - <span data-ttu-id="4276b-185">**ID de message réseau**: valeur Guid disponible dans le champ d’en-tête **X-MS-Exchange-Organization-Network-message-ID** de l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="4276b-185">**Network message ID**: A GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header field in the message header.</span></span>
  
  - <span data-ttu-id="4276b-186">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-186">**Sender IP**</span></span>
  
  - <span data-ttu-id="4276b-187">**Attachment SHA256**: pour trouver la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes : `certutil.exe -hashfile "<Path>\<Filename>" SHA256` .</span><span class="sxs-lookup"><span data-stu-id="4276b-187">**Attachment SHA256**: To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt: `certutil.exe -hashfile "<Path>\<Filename>" SHA256`.</span></span>
  
  - <span data-ttu-id="4276b-188">**ID de cluster**</span><span class="sxs-lookup"><span data-stu-id="4276b-188">**Cluster ID**</span></span>
  
  - <span data-ttu-id="4276b-189">**ID de stratégie d’alerte**</span><span class="sxs-lookup"><span data-stu-id="4276b-189">**Alert Policy ID**</span></span>

- <span data-ttu-id="4276b-190">URL</span><span class="sxs-lookup"><span data-stu-id="4276b-190">URLs</span></span>

  - <span data-ttu-id="4276b-191">**Domaine d’URL**</span><span class="sxs-lookup"><span data-stu-id="4276b-191">**URL domain**</span></span>
  - <span data-ttu-id="4276b-192">**Domaine et chemin d’accès de l’URL**</span><span class="sxs-lookup"><span data-stu-id="4276b-192">**URL domain and path**</span></span>
  - <span data-ttu-id="4276b-193">**URL**</span><span class="sxs-lookup"><span data-stu-id="4276b-193">**URL**</span></span>
  - <span data-ttu-id="4276b-194">**Chemin d’URL**</span><span class="sxs-lookup"><span data-stu-id="4276b-194">**URL path**</span></span>
  - <span data-ttu-id="4276b-195">**Cliquez sur verdict**</span><span class="sxs-lookup"><span data-stu-id="4276b-195">**Click verdict**</span></span>

<span data-ttu-id="4276b-196">Pour un filtrage plus avancé, incluant le filtrage par plusieurs propriétés, vous pouvez cliquer sur le bouton **filtre avancé** pour créer une requête.</span><span class="sxs-lookup"><span data-stu-id="4276b-196">For more advanced filtering, including filtering by multiple properties, you can click the **Advanced filter** button to build a query.</span></span> <span data-ttu-id="4276b-197">Les mêmes propriétés de campagne sont disponibles, mais avec les améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4276b-197">The same campaign properties are available, but with the following enhancements:</span></span>

- <span data-ttu-id="4276b-198">Vous pouvez cliquer sur **Ajouter une condition** pour sélectionner plusieurs conditions.</span><span class="sxs-lookup"><span data-stu-id="4276b-198">You can click **Add a condition** to select multiple conditions.</span></span>
- <span data-ttu-id="4276b-199">Vous pouvez choisir l' **And** opérateur and **ou or entre** les conditions.</span><span class="sxs-lookup"><span data-stu-id="4276b-199">You can choose the **And** or **Or** operator between conditions.</span></span>
- <span data-ttu-id="4276b-200">Vous pouvez sélectionner l’élément de **groupe** de conditions au bas de la liste conditions pour créer des conditions composées complexes.</span><span class="sxs-lookup"><span data-stu-id="4276b-200">You can select the **Condition group** item at the bottom of the conditions list to form complex compound conditions.</span></span>

<span data-ttu-id="4276b-201">Lorsque vous avez terminé, cliquez sur le bouton **requête** .</span><span class="sxs-lookup"><span data-stu-id="4276b-201">When you're finished, click the **Query** button.</span></span>

<span data-ttu-id="4276b-202">Une fois que vous avez créé un filtre de base ou avancé, vous pouvez l’enregistrer à l’aide de la **requête enregistrer** la requête ou **enregistrer la requête sous**.</span><span class="sxs-lookup"><span data-stu-id="4276b-202">After you create a basic or advanced filter, you can save it by using **Save query** or **Save query as**.</span></span> <span data-ttu-id="4276b-203">Par la suite, lorsque vous revenez à vues de la campagne, vous pouvez charger un filtre enregistré en cliquant sur paramètres de la **requête enregistrée**.</span><span class="sxs-lookup"><span data-stu-id="4276b-203">Later, when you return to Campaign Views, you can load a saved filter by clicking **Saved query settings**.</span></span>

<span data-ttu-id="4276b-204">Pour exporter le graphique ou la liste des campagnes, cliquez sur **Exporter** , puis sélectionnez **Exporter les données du graphique** ou exporter la liste des **campagnes**.</span><span class="sxs-lookup"><span data-stu-id="4276b-204">To export the graph or the list of campaigns, click **Export** and select **Export chart data** or **Export campaign list**.</span></span>

<span data-ttu-id="4276b-205">Si vous disposez d’un abonnement Microsoft Defender ATP, vous pouvez cliquer sur **WDATP** pour connecter ou déconnecter les informations de campagne avec Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="4276b-205">If you have a Microsoft Defender ATP subscription, you can click **WDATP** to connect or disconnect the campaigns information with Microsoft Defender ATP.</span></span> <span data-ttu-id="4276b-206">Pour plus d’informations, reportez-vous à la rubrique [intégrer Office 365 ATP avec Microsoft Defender ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/integrate-office-365-ti-with-wdatp).</span><span class="sxs-lookup"><span data-stu-id="4276b-206">For more information, see [Integrate Office 365 ATP with Microsoft Defender ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/integrate-office-365-ti-with-wdatp).</span></span>

## <a name="campaign-details"></a><span data-ttu-id="4276b-207">Détails de la campagne</span><span class="sxs-lookup"><span data-stu-id="4276b-207">Campaign details</span></span>

<span data-ttu-id="4276b-208">Lorsque vous cliquez sur le nom d’une campagne, les détails de la campagne s’affichent dans un menu volant.</span><span class="sxs-lookup"><span data-stu-id="4276b-208">When you click on the name of a campaign, the campaign details appear in a flyout.</span></span>

### <a name="campaign-information"></a><span data-ttu-id="4276b-209">Informations sur la campagne</span><span class="sxs-lookup"><span data-stu-id="4276b-209">Campaign information</span></span>

<span data-ttu-id="4276b-210">En haut de la vue Détails de la campagne, les informations de campagne suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="4276b-210">At the top of the campaign details view, the following campaign information is available:</span></span>

- <span data-ttu-id="4276b-211">**ID**: identificateur unique de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-211">**ID**: The unique campaign identifier.</span></span>

- <span data-ttu-id="4276b-212">**Démarré** et **terminé**: date de début et date de fin de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-212">**Started** and **Ended**: The start date and end date of the campaign.</span></span> <span data-ttu-id="4276b-213">Notez que ces dates peuvent s’étendre davantage que vos dates de filtrage sélectionnées sur la page de vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="4276b-213">Note that these dates might extend further than your filter dates that you selected on the overview page.</span></span>

- <span data-ttu-id="4276b-214">**Impact**: cette section contient les données suivantes pour le filtre de plage de dates que vous avez sélectionné (ou que vous sélectionnez dans la chronologie) :</span><span class="sxs-lookup"><span data-stu-id="4276b-214">**Impact**: This section contains the following data for the date range filter you selected (or that you select in the timeline):</span></span>
  
  - <span data-ttu-id="4276b-215">Nombre total de destinataires.</span><span class="sxs-lookup"><span data-stu-id="4276b-215">The total number of recipients.</span></span>
  - <span data-ttu-id="4276b-216">Nombre de messages qui ont reçu la boîte de réception (c’est-à-dire remis dans la boîte de réception, et non dans le dossier courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="4276b-216">The number of messages that were "Inboxed" (that is, delivered to the Inbox, not to the Junk Email folder).</span></span>
  - <span data-ttu-id="4276b-217">Le nombre d’utilisateurs sur lesquels l’utilisateur a cliqué dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4276b-217">How many users clicked on the URL payload in the phishing message.</span></span>
  - <span data-ttu-id="4276b-218">Howe nombre d’utilisateurs visitaient l’URL.</span><span class="sxs-lookup"><span data-stu-id="4276b-218">Howe many users visited the URL.</span></span>

- <span data-ttu-id="4276b-219">**Ciblé**: pourcentage tel que calculé par : (nombre de destinataires de campagne dans votre organisation)/(nombre total de destinataires dans la campagne pour toutes les organisations du service).</span><span class="sxs-lookup"><span data-stu-id="4276b-219">**Targeted**: The percentage as calculated by: (the number of campaign recipients in your organization) / (the total number of recipients in the campaign across all organizations in the service).</span></span> <span data-ttu-id="4276b-220">Notez que cette valeur est calculée sur toute la durée de vie de la campagne et ne modifie pas les dates de filtrage.</span><span class="sxs-lookup"><span data-stu-id="4276b-220">Note that this value is calculated over the entire lifetime of the campaign, and doesn't change the filter dates.</span></span>

- <span data-ttu-id="4276b-221">Chronologie interactive de l’activité de campagne : la chronologie affiche l’activité sur toute la durée de vie de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-221">An interactive timeline of campaign activity: The timeline shows activity over the entire lifetime of the campaign.</span></span> <span data-ttu-id="4276b-222">Par défaut, la zone ombrée inclut le filtre de plage de dates que vous avez sélectionné dans la vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="4276b-222">By default, the shaded area includes the date range filter that you selected in the overview.</span></span> <span data-ttu-id="4276b-223">Vous pouvez cliquer et faire glisser pour sélectionner un point de départ et un point de terminaison spécifiques, ce <u>qui modifiera les données affichées dans la zone d' **impact** , et sur le reste de la page, comme décrit dans les sections suivantes</u>.</span><span class="sxs-lookup"><span data-stu-id="4276b-223">You can click and drag to select a specific start point and end point, <u>which will change the data that's displayed in **Impact** area, and on the rest of the page as described in the next sections</u>.</span></span>

<span data-ttu-id="4276b-224">Dans la barre de titre, vous pouvez cliquer sur le bouton Télécharger la campagne en **écriture** ![ pour télécharger ](../../media/download-campaign-write-up-button.png) les détails de la campagne dans un document Word (par défaut, nommé CampaignReport.docx).</span><span class="sxs-lookup"><span data-stu-id="4276b-224">In the title bar, you can click the **Download campaign write-up** button ![Download campaign write-up icon](../../media/download-campaign-write-up-button.png) to download the campaign details to a Word document (by default, named CampaignReport.docx).</span></span> <span data-ttu-id="4276b-225">Notez que ce document contient des détails sur toute la durée de vie de la campagne (pas seulement sur les dates de filtrage sélectionnées).</span><span class="sxs-lookup"><span data-stu-id="4276b-225">Note that this document contains details over the entire lifetime of the campaign (not just the filter dates you selected).</span></span>

![Informations sur la campagne](../../media/campaign-details-campaign-info.png)

### <a name="campaign-flow"></a><span data-ttu-id="4276b-227">Flux de la campagne</span><span class="sxs-lookup"><span data-stu-id="4276b-227">Campaign flow</span></span>

<span data-ttu-id="4276b-228">Au milieu de la vue Détails de la campagne, des informations importantes sur la campagne sont présentées dans la section **flux** , dans un diagramme de flux horizontal (appelé diagramme _Sankey_ ).</span><span class="sxs-lookup"><span data-stu-id="4276b-228">In the middle of the campaign details view, important details about the campaign are presented in the **Flow** section in a horizontal flow diagram (known as a _Sankey_ diagram).</span></span> <span data-ttu-id="4276b-229">Ces détails vous aideront à comprendre les éléments de la campagne et l’impact potentiel au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4276b-229">These details will help you to understand the elements of the campaign and the potential impact in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="4276b-230">Les informations affichées dans le diagramme de **flux** sont contrôlées par la plage de dates grisée dans la chronologie, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="4276b-230">The information that's displayed in the **Flow** diagram is controlled by the shaded date range in the timeline as described in the previous section.</span></span>

![Détails de la campagne ne contenant pas d’URL d’utilisateur](../../media/campaign-details-no-recipient-actions.png)

<span data-ttu-id="4276b-232">Si vous pointez sur une bande horizontale dans le diagramme, vous pouvez voir le nombre de messages associés (par exemple, les messages d’une adresse IP source particulière, les messages provenant de l’adresse IP source en utilisant le domaine d’expéditeur spécifié, etc.).</span><span class="sxs-lookup"><span data-stu-id="4276b-232">If you hover over a horizontal band in the diagram, you'll see the number of related messages (for example, messages from a particular source IP, messages from the source IP using the specified sender domain, etc.).</span></span>

<span data-ttu-id="4276b-233">Le diagramme contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4276b-233">The diagram contains the following information:</span></span>

- <span data-ttu-id="4276b-234">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-234">**Sender IPs**</span></span>

- <span data-ttu-id="4276b-235">**Domaines de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-235">**Sender domains**</span></span>

- <span data-ttu-id="4276b-236">Valeurs de **verdict du filtre**: ces valeurs sont liées aux verdicts de hameçonnage et de filtrage du courrier indésirable disponibles, comme décrit dans [les en-têtes de message anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-236">**Filter verdicts**: These values are related to the available phishing and spam filtering verdicts as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="4276b-237">Les valeurs disponibles sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="4276b-237">The available values are described in the following table:</span></span>

  ****

  |<span data-ttu-id="4276b-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="4276b-238">Value</span></span>|<span data-ttu-id="4276b-239">Verdict du filtre de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4276b-239">Spam filter verdict</span></span>|<span data-ttu-id="4276b-240">Description</span><span class="sxs-lookup"><span data-stu-id="4276b-240">Description</span></span>|
  |---|---|---|
  |<span data-ttu-id="4276b-241">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="4276b-241">**Allowed**</span></span>|`SFV:SKN` <br/><br/> `SFV:SKI`|<span data-ttu-id="4276b-242">Le message a été marqué comme n’étant pas un courrier indésirable et/ou a ignoré le filtrage avant d’être évalué par le filtrage du courrier indésirable (par exemple, par une règle de flux de messagerie, également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="4276b-242">The message was marked as not spam and/or skipped filtering before being evaluated by spam filtering (for example, by a mail flow rule, also known as a transport rule).</span></span><br/><br/><span data-ttu-id="4276b-243">Le message a ignoré le filtrage du courrier indésirable pour d’autres raisons (par exemple, l’expéditeur et le destinataire semblent être dans la même organisation).</span><span class="sxs-lookup"><span data-stu-id="4276b-243">The message skipped spam filtering for other reasons (for example, the sender and recipient appear to be in the same organization).</span></span>|
  |<span data-ttu-id="4276b-244">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="4276b-244">**Blocked**</span></span>|`SFV:SKS`|<span data-ttu-id="4276b-245">Le message a été marqué comme courrier indésirable avant d’être évalué par le filtrage du courrier indésirable (par exemple, par une règle de flux de messagerie).</span><span class="sxs-lookup"><span data-stu-id="4276b-245">The message was marked as spam before being evaluated by spam filtering (for example, by a mail flow rule).</span></span>|
  |<span data-ttu-id="4276b-246">**Détecté**</span><span class="sxs-lookup"><span data-stu-id="4276b-246">**Detected**</span></span>|`SFV:SPM`|<span data-ttu-id="4276b-247">Le message a été marqué comme courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4276b-247">The message was marked as spam by spam filtering.</span></span>|
  |<span data-ttu-id="4276b-248">**Non détecté**</span><span class="sxs-lookup"><span data-stu-id="4276b-248">**Not Detected**</span></span>|`SFV:NSPM`|<span data-ttu-id="4276b-249">Le message a été marqué comme non courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4276b-249">The message was marked as not spam by spam filtering.</span></span>|
  |<span data-ttu-id="4276b-250">**A**</span><span class="sxs-lookup"><span data-stu-id="4276b-250">**Released**</span></span>|`SFV:SKQ`|<span data-ttu-id="4276b-251">Le message a ignoré le filtrage du courrier indésirable, car il a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="4276b-251">The message skipped spam filtering because it was released from quarantine.</span></span>|
  |<span data-ttu-id="4276b-252">**Autoriser le client**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-252">**Tenant Allow**<sup>\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="4276b-253">Le message a ignoré le filtrage du courrier indésirable en raison des paramètres de stratégie de blocage du courrier indésirable (par exemple, l’expéditeur se trouvait dans la liste des expéditeurs autorisés ou le domaine autorisé).</span><span class="sxs-lookup"><span data-stu-id="4276b-253">The message skipped spam filtering due to anti-spam policy settings (for example, the sender was in the allowed sender list or allowed domain list).</span></span>|
  |<span data-ttu-id="4276b-254">**Bloc de locataire**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-254">**Tenant Block**<sup>\*\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="4276b-255">Le message a été bloqué par le filtrage du courrier indésirable en raison des paramètres de stratégie de blocage du courrier indésirable (par exemple, l’expéditeur se trouvait dans la liste des expéditeurs autorisés ou le domaine autorisé).</span><span class="sxs-lookup"><span data-stu-id="4276b-255">The message was blocked by spam filtering due to anti-spam policy settings (for example, the sender was in the allowed sender list or allowed domain list).</span></span>|
  |<span data-ttu-id="4276b-256">**Autorisation de l’utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-256">**User Allow**<sup>\*</sup></span></span>|`SFV:SFE`|<span data-ttu-id="4276b-257">Le message a ignoré le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs approuvés d’un utilisateur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="4276b-257">The message skipped spam filtering because the sender was in a user's Safe Senders list in Outlook.</span></span>|
  |<span data-ttu-id="4276b-258">**Bloc utilisateur**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-258">**User Block**<sup>\*\*</sup></span></span>|`SFV:BLK`|<span data-ttu-id="4276b-259">Le message a été bloqué par le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs bloqués d’un utilisateur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="4276b-259">The message was blocked by spam filtering because the sender was in a user's Blocked Senders list in Outlook.</span></span>|
  |<span data-ttu-id="4276b-260">**ZAP**</span><span class="sxs-lookup"><span data-stu-id="4276b-260">**ZAP**</span></span>|<span data-ttu-id="4276b-261">s/o</span><span class="sxs-lookup"><span data-stu-id="4276b-261">n/a</span></span>|<span data-ttu-id="4276b-262">La [purge automatique à zéro heure (ZAP)](zero-hour-auto-purge.md) a effectué une action sur le message remis en fonction de vos paramètres de stratégie anti-courrier indésirable (déplacés vers le dossier courrier indésirable ou mis en quarantaine).</span><span class="sxs-lookup"><span data-stu-id="4276b-262">[Zero-hour auto purge (ZAP)](zero-hour-auto-purge.md) took action on the delivered message according to your anti-spam policy settings (moved to the Junk Email folder or Quarantined).</span></span>|
  |

  <span data-ttu-id="4276b-263"><sup>\*</sup> Examinez vos stratégies de blocage du courrier indésirable, car le message autorisé aurait probablement été bloqué par le service.</span><span class="sxs-lookup"><span data-stu-id="4276b-263"><sup>\*</sup> Review your anti-spam policies, because the allowed message would have likely been blocked by the service.</span></span>

  <span data-ttu-id="4276b-264"><sup>\*\*</sup> Examinez vos stratégies de blocage du courrier indésirable, car ces messages doivent être mis en quarantaine et non remis.</span><span class="sxs-lookup"><span data-stu-id="4276b-264"><sup>\*\*</sup> Review your anti-spam policies, because these messages should be quarantined, not delivered.</span></span>

- <span data-ttu-id="4276b-265">**Emplacements de remise**: vous souhaiterez peut-être examiner les messages qui ont été remis aux destinataires (soit dans la boîte de réception, soit dans le dossier courrier indésirable), même si les utilisateurs n'ont pas cliqué sur l'URL de la charge utile dans le message.</span><span class="sxs-lookup"><span data-stu-id="4276b-265">**Delivery locations**: You'll likely want to investigate messages that were actually delivered to recipients (either to the Inbox or the Junk Email folder), even if users didn't click on the payload URL in the message.</span></span> <span data-ttu-id="4276b-266">Vous pouvez également supprimer les messages mis en quarantaine en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="4276b-266">You can also remove the quarantined messages from quarantine.</span></span> <span data-ttu-id="4276b-267">Pour plus d’informations, consultez la rubrique [messages électroniques mis en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-267">For more information, see [Quarantined email messages in EOP](quarantine-email-messages.md).</span></span>

  - <span data-ttu-id="4276b-268">**Dossier supprimé**</span><span class="sxs-lookup"><span data-stu-id="4276b-268">**Deleted folder**</span></span>
  - <span data-ttu-id="4276b-269">**Raccroché**</span><span class="sxs-lookup"><span data-stu-id="4276b-269">**Dropped**</span></span>
  - <span data-ttu-id="4276b-270">**External**: le destinataire est situé dans votre organisation de messagerie locale dans les environnements hybrides.</span><span class="sxs-lookup"><span data-stu-id="4276b-270">**External**: The recipient is located in your on-premises email organization in hybrid environments.</span></span>
  - <span data-ttu-id="4276b-271">**Échec**</span><span class="sxs-lookup"><span data-stu-id="4276b-271">**Failed**</span></span>
  - <span data-ttu-id="4276b-272">**Renvoyé**</span><span class="sxs-lookup"><span data-stu-id="4276b-272">**Forwarded**</span></span>
  - <span data-ttu-id="4276b-273">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="4276b-273">**Inbox**</span></span>
  - <span data-ttu-id="4276b-274">**Dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4276b-274">**Junk folder**</span></span>
  - <span data-ttu-id="4276b-275">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="4276b-275">**Quarantine**</span></span>
  - <span data-ttu-id="4276b-276">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="4276b-276">**Unknown**</span></span>

- <span data-ttu-id="4276b-277">**Clics sur l’URL**: ces éléments sont décrits dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="4276b-277">**URL clicks**: These are described in the next section.</span></span>

> [!NOTE]
> <span data-ttu-id="4276b-278">Dans toutes les couches contenant plus de 10 éléments, les 10 premiers éléments sont affichés, tandis que les autres sont regroupés dans les **autres**.</span><span class="sxs-lookup"><span data-stu-id="4276b-278">In all layers that contain more than 10 items, the top 10 items are shown, while the rest are bundled together in **Others**.</span></span>

#### <a name="url-clicks"></a><span data-ttu-id="4276b-279">Clics d’URL</span><span class="sxs-lookup"><span data-stu-id="4276b-279">URL clicks</span></span>

<span data-ttu-id="4276b-280">Lorsqu’un message d’hameçonnage est remis à un destinataire (dans la boîte de réception ou dans le dossier courrier indésirable), il y a toujours un risque que l’utilisateur clique sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="4276b-280">When a phishing message is delivered to a recipient (to the Inbox or the Junk Email folder), there's always a chance that the user will click on the payload URL.</span></span> <span data-ttu-id="4276b-281">Le fait de ne pas cliquer sur l’URL dans un message remis est une petite mesure de succès, mais vous devez déterminer pourquoi le message de hameçonnage a été remis à sa boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4276b-281">Not clicking on the URL in a delivered message is a small measure of success, but you need to determine why the phishing message was delivered to their mailbox in the first place.</span></span>

<span data-ttu-id="4276b-282">Si un utilisateur a cliqué sur l’URL de la charge utile dans le message d’hameçonnage, les actions sont affichées dans la zone de **clics sur l’URL** du diagramme dans la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-282">If a user clicked on the payload URL in the phishing message, the actions are displayed in the **URL clicks** area of the diagram in the campaign details view.</span></span>

- <span data-ttu-id="4276b-283">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="4276b-283">**Allowed**</span></span>

- <span data-ttu-id="4276b-284">**BlockPage**: le destinataire a cliqué sur l’URL de charge utile, mais son accès au site Web malveillant a été bloqué par les stratégies de [liens fiables ATP](atp-safe-links.md) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4276b-284">**BlockPage**: The recipient clicked on the payload URL, but their access to the malicious website was blocked by the [ATP Safe Links](atp-safe-links.md) policies in your organization.</span></span>

- <span data-ttu-id="4276b-285">**BlockPageOverride**: le destinataire a cliqué sur l’URL de charge utile dans le message, les liens fiables ATP ont essayé de les arrêter, mais ils ont été autorisés à remplacer le bloc.</span><span class="sxs-lookup"><span data-stu-id="4276b-285">**BlockPageOverride**: The recipient clicked on the payload URL in the message, ATP Safe Links tried to stop them, but they were allowed to override the block.</span></span> <span data-ttu-id="4276b-286">Vous devez examiner vos [stratégies de liens fiables](set-up-atp-safe-links-policies.md) pour savoir pourquoi les utilisateurs sont autorisés à remplacer le verdict des liens fiables et continuer à accéder au site Web malveillant.</span><span class="sxs-lookup"><span data-stu-id="4276b-286">You need to investigate your [Safe Links policies](set-up-atp-safe-links-policies.md) to see why users are allowed to override the Safe Links verdict and continue to the malicious website.</span></span>

- <span data-ttu-id="4276b-287">**PendingDetonationPage**: les pièces jointes de protection avancée contre les menaces sont en cours d’ouverture de l’URL de charge utile dans un environnement d’ordinateur virtuel et de l’affichage de ce qui se passe.</span><span class="sxs-lookup"><span data-stu-id="4276b-287">**PendingDetonationPage**: ATP Safe Attachments is in the process of opening the payload URL in a virtual computer environment, and seeing what happens.</span></span>

- <span data-ttu-id="4276b-288">**PendingDetonationPageOverride**: le destinataire a été autorisé à remplacer le processus de détonation de charge utile et à ouvrir l’URL sans attendre les résultats.</span><span class="sxs-lookup"><span data-stu-id="4276b-288">**PendingDetonationPageOverride**: The recipient was allowed to override the payload detonation process and open the URL without waiting for the results.</span></span>

### <a name="tabs"></a><span data-ttu-id="4276b-289">Onglets</span><span class="sxs-lookup"><span data-stu-id="4276b-289">Tabs</span></span>

<span data-ttu-id="4276b-290">Les onglets de la vue Détails de la campagne vous permettent d’approfondir la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-290">The tabs in the campaign details view allow you to further investigate the campaign.</span></span>

> [!TIP]
> <span data-ttu-id="4276b-291">Les informations affichées dans les onglets sont contrôlées par la plage de dates grisée dans le scénario, comme décrit dans la section [informations sur la campagne](#campaign-information) .</span><span class="sxs-lookup"><span data-stu-id="4276b-291">The information that's displayed on the tabs is controlled by the shaded date range in the timeline as described in [Campaign information](#campaign-information) section.</span></span>

- <span data-ttu-id="4276b-292">**Clics**sur l’URL : si les utilisateurs ne cliquent pas sur l’URL de la charge utile dans le message d’hameçonnage, cette section est vide.</span><span class="sxs-lookup"><span data-stu-id="4276b-292">**URL clicks**: If users didn't click on the payload URL in the phishing message, this section will be blank.</span></span> <span data-ttu-id="4276b-293">Si un utilisateur a pu cliquer sur l’URL, les valeurs suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="4276b-293">If a user was able to click on the URL, the following values will be populated:</span></span>

  - <span data-ttu-id="4276b-294">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-294">**User**<sup>\*</sup></span></span>
  - <span data-ttu-id="4276b-295">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-295">**URL**<sup>\*</sup></span></span>
  - <span data-ttu-id="4276b-296">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="4276b-296">**Click time**</span></span>
  - <span data-ttu-id="4276b-297">**Cliquez sur verdict**</span><span class="sxs-lookup"><span data-stu-id="4276b-297">**Click verdict**</span></span>

- <span data-ttu-id="4276b-298">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4276b-298">**Sender IPs**</span></span>

  - <span data-ttu-id="4276b-299">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-299">**Sender IP**<sup>\*</sup></span></span>
  - <span data-ttu-id="4276b-300">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="4276b-300">**Total count**</span></span>
  - <span data-ttu-id="4276b-301">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="4276b-301">**Inboxed**</span></span>
  - <span data-ttu-id="4276b-302">**Pas de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="4276b-302">**Not Inboxed**</span></span>
  - <span data-ttu-id="4276b-303">**SPF transmis**: l’expéditeur a été authentifié par [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-303">**SPF passed**: The sender was authenticated by the [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="4276b-304">Un expéditeur qui ne passe pas la validation SPF indique que l’expéditeur n’est pas authentifié, ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="4276b-304">A sender that does not pass SPF validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="4276b-305">**Expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="4276b-305">**Senders**</span></span>

  - <span data-ttu-id="4276b-306">**Expéditeur**: il s’agit de l’adresse de l’expéditeur réelle dans la commande SMTP Mail from, qui n’est pas nécessairement l’adresse de messagerie de l’expéditeur que les utilisateurs voient dans leurs clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4276b-306">**Sender**: This is the actual sender address in the SMTP MAIL FROM command, which is not necessarily the From: email address that users see in their email clients.</span></span>
  - <span data-ttu-id="4276b-307">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="4276b-307">**Total count**</span></span>
  - <span data-ttu-id="4276b-308">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="4276b-308">**Inboxed**</span></span>
  - <span data-ttu-id="4276b-309">**Pas de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="4276b-309">**Not Inboxed**</span></span>
  - <span data-ttu-id="4276b-310">**DKIM transmis**: l’expéditeur a été authentifié par des [clés de domaine identifiées par des clés de domaine (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-310">**DKIM passed**: The sender was authenticated by [Domain Keys Identified Mail (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span></span> <span data-ttu-id="4276b-311">Un expéditeur qui ne passe pas la validation DKIM indique que l’expéditeur n’est pas authentifié, ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="4276b-311">A sender that does not pass DKIM validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>
  - <span data-ttu-id="4276b-312">**DMARC réussi**: l’expéditeur a été authentifié par [l’authentification de message basée sur un domaine, la création de rapports et la conformité (DMARC)](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="4276b-312">**DMARC passed**: The sender was authenticated by [Domain-based Message Authentication, Reporting, and Conformance (DMARC)](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="4276b-313">Un expéditeur qui ne réussit pas la validation DMARC indique que l’expéditeur n’est pas authentifié ou que le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="4276b-313">A sender that does not pass DMARC validation indicates the sender isn't authenticated, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="4276b-314">**Attachments**</span><span class="sxs-lookup"><span data-stu-id="4276b-314">**Attachments**</span></span>

  - <span data-ttu-id="4276b-315">**Filename**</span><span class="sxs-lookup"><span data-stu-id="4276b-315">**Filename**</span></span>
  - <span data-ttu-id="4276b-316">**SHA256**</span><span class="sxs-lookup"><span data-stu-id="4276b-316">**SHA256**</span></span>
  - <span data-ttu-id="4276b-317">**Famille de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="4276b-317">**Malware family**</span></span>
  - <span data-ttu-id="4276b-318">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="4276b-318">**Total count**</span></span>

- <span data-ttu-id="4276b-319">**URL**</span><span class="sxs-lookup"><span data-stu-id="4276b-319">**URL**</span></span>

  - <span data-ttu-id="4276b-320">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4276b-320">**URL**<sup>\*</sup></span></span>
  - <span data-ttu-id="4276b-321">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="4276b-321">**Total Count**</span></span>

<span data-ttu-id="4276b-322"><sup>\*</sup> Le fait de cliquer sur cette valeur ouvre un nouveau menu mobile qui contient plus de détails sur l’élément spécifié (utilisateur, URL, etc.) au-dessus de la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-322"><sup>\*</sup> Clicking on this value opens a new flyout that contains more details about the specified item (user, URL, etc.) on top of the campaign details view.</span></span> <span data-ttu-id="4276b-323">Pour revenir à la vue Détails de la campagne, cliquez sur **Terminé** dans la nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="4276b-323">To return to the campaign details view, click **Done** in the new flyout.</span></span>

### <a name="buttons"></a><span data-ttu-id="4276b-324">Boutons</span><span class="sxs-lookup"><span data-stu-id="4276b-324">Buttons</span></span>

<span data-ttu-id="4276b-325">Les boutons de la vue Détails de la campagne vous permettent d’utiliser le Power Explorer pour approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="4276b-325">The buttons in the campaign details view allow you to use the power of Threat Explorer to further investigate the campaign.</span></span>

- <span data-ttu-id="4276b-326">**Explorer la campagne**: ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de la valeur **ID de campagne** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="4276b-326">**Explore campaign**: Opens a new Threat Explorer search tab using the **Campaign ID** value as the search filter.</span></span>

- <span data-ttu-id="4276b-327">**Explorer les messages**de la boîte de réception : ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de l' **ID de campagne** et de l' **emplacement de remise : boîte de réception** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="4276b-327">**Explore Inboxed messages**: Opens a new Threat Explorer search tab using the **Campaign ID** and **Delivery location: Inbox** as the search filter.</span></span>
