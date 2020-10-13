---
title: Vues de campagne dans Office 365, plan DAV
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: mcostea
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
description: Découvrez Campaign Views dans Office 365 - Protection avancée contre les menaces.
ms.openlocfilehash: 00af3f241bc1d9fd2cae9ebae0cdec7817679ed2
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48430572"
---
# <a name="campaign-views-in-office-365-atp"></a><span data-ttu-id="18be4-103">Campaign Views dans Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="18be4-103">Campaign Views in Office 365 ATP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="18be4-104">Les vues de campagne sont une fonctionnalité de la protection avancée contre les menaces (ATP) plan 2 (par exemple, Microsoft 365 E5 ou des organisations avec un complément ATP plan 2).</span><span class="sxs-lookup"><span data-stu-id="18be4-104">Campaign Views is a feature in Advanced Threat Protection (ATP) Plan 2 (for example Microsoft 365 E5 or organizations with an ATP Plan 2 add-on).</span></span> <span data-ttu-id="18be4-105">Les vues de campagne dans le centre de sécurité & conformité identifient et catégorisent les attaques par hameçonnage dans le service.</span><span class="sxs-lookup"><span data-stu-id="18be4-105">Campaign Views in the Security & Compliance Center identifies and categorizes phishing attacks in the service.</span></span> <span data-ttu-id="18be4-106">Campaign Views permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="18be4-106">Campaign Views can help you to:</span></span>

- <span data-ttu-id="18be4-107">Examiner et répondre efficacement aux attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="18be4-107">Efficiently investigate and respond to phishing attacks.</span></span>
- <span data-ttu-id="18be4-108">Mieux comprendre l’étendue de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="18be4-108">Better understand the scope of the attack.</span></span>
- <span data-ttu-id="18be4-109">Afficher la valeur pour les décideurs.</span><span class="sxs-lookup"><span data-stu-id="18be4-109">Show value to decision makers.</span></span>

<span data-ttu-id="18be4-110">Campaign Views vous permet de voir la présentation d’une attaque plus rapidement et plus complètement que n’importe quel autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18be4-110">Campaign Views lets you see the big picture of an attack faster and more complete than any human.</span></span>

## <a name="what-is-a-campaign"></a><span data-ttu-id="18be4-111">Qu’est-ce qu’une campagne ?</span><span class="sxs-lookup"><span data-stu-id="18be4-111">What is a campaign?</span></span>

<span data-ttu-id="18be4-112">Une campagne est une attaque par e-mail coordonné contre une ou plusieurs organisations.</span><span class="sxs-lookup"><span data-stu-id="18be4-112">A campaign is a coordinated email attack against one or many organizations.</span></span> <span data-ttu-id="18be4-113">Les attaques par courrier électronique qui volent les informations d’identification et les données d’entreprise sont un secteur important et lucratif.</span><span class="sxs-lookup"><span data-stu-id="18be4-113">Email attacks that steal credentials and company data are a large and lucrative industry.</span></span> <span data-ttu-id="18be4-114">À mesure que les technologies augmentent pour empêcher les attaques, les agresseurs modifient leurs méthodes afin de garantir une réussite continue.</span><span class="sxs-lookup"><span data-stu-id="18be4-114">As technologies increase in an effort to stop attacks, attackers modify their methods in an effort to ensure continued success.</span></span>

<span data-ttu-id="18be4-115">Microsoft exploite les grandes quantités de données anti-hameçonnage, de blocage du courrier indésirable et anti-programme malveillant dans l’ensemble du service afin d’identifier les campagnes.</span><span class="sxs-lookup"><span data-stu-id="18be4-115">Microsoft leverages the vast amounts of anti-phishing, anti-spam, and anti-malware data across the entire service to help identify campaigns.</span></span> <span data-ttu-id="18be4-116">Nous analysons et classifions les informations d’attaque en fonction de plusieurs facteurs.</span><span class="sxs-lookup"><span data-stu-id="18be4-116">We analyze and classify the attack information according to several factors.</span></span> <span data-ttu-id="18be4-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="18be4-117">For example:</span></span>

- <span data-ttu-id="18be4-118">**Source**de l’attaque : les adresses IP source et les domaines de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="18be4-118">**Attack source**: The source IP addresses and sender email domains.</span></span>
- <span data-ttu-id="18be4-119">**Propriétés de message**: le contenu, le style et la tonalité des messages.</span><span class="sxs-lookup"><span data-stu-id="18be4-119">**Message properties**: The content, style, and tone of the messages.</span></span>
- <span data-ttu-id="18be4-120">**Destinataires du message**: relation entre les destinataires.</span><span class="sxs-lookup"><span data-stu-id="18be4-120">**Message recipients**: How recipients are related.</span></span> <span data-ttu-id="18be4-121">Par exemple, les domaines de destinataire, les fonctions de destinataire (administrateurs, cadres, etc.), les types de sociétés (grande, petite, publique, privée, etc.) et les industries.</span><span class="sxs-lookup"><span data-stu-id="18be4-121">For example, recipient domains, recipient job functions (admins, executives, etc.), company types (large, small, public, private, etc.), and industries.</span></span>
- <span data-ttu-id="18be4-122">**Charge utile d’attaque**: liens malveillants, pièces jointes ou autres charges utiles dans les messages.</span><span class="sxs-lookup"><span data-stu-id="18be4-122">**Attack payload**: Malicious links, attachments, or other payloads in the messages.</span></span>

<span data-ttu-id="18be4-123">Une campagne peut être à courte durée de vie ou peut s’étendre sur plusieurs jours, semaines ou mois avec des périodes actives et inactives.</span><span class="sxs-lookup"><span data-stu-id="18be4-123">A campaign might be short-lived, or could span several days, weeks, or months with active and inactive periods.</span></span> <span data-ttu-id="18be4-124">Une campagne peut être lancée par rapport à votre organisation, ou votre organisation peut faire partie d’une campagne plus importante sur plusieurs sociétés.</span><span class="sxs-lookup"><span data-stu-id="18be4-124">A campaign might be launched against your specific organization, or your organization might be part of a larger campaign across multiple companies.</span></span>

## <a name="campaign-views-in-the-security--compliance-center"></a><span data-ttu-id="18be4-125">Vues de campagne dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="18be4-125">Campaign Views in the Security & Compliance Center</span></span>

<span data-ttu-id="18be4-126">Les vues de campagne sont disponibles dans le [Centre de sécurité & conformité](https://protection.office.com) aux **Threat management** \> **campagnes**gestion des menaces ou directement sur le <https://protection.office.com/campaigns> .</span><span class="sxs-lookup"><span data-stu-id="18be4-126">Campaign Views is available in the [Security & Compliance Center](https://protection.office.com) at **Threat management** \> **Campaigns**, or directly at <https://protection.office.com/campaigns>.</span></span>

![Vue d’ensemble des campagnes dans la Centre de sécurité et conformité](../../media/campaigns-overview.png)

<span data-ttu-id="18be4-128">Vous pouvez également accéder aux vues de campagne à partir de :</span><span class="sxs-lookup"><span data-stu-id="18be4-128">You can also get to Campaign Views from:</span></span>

- <span data-ttu-id="18be4-129">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Campagnes marketing**</span><span class="sxs-lookup"><span data-stu-id="18be4-129">**Threat management** \> **Explorer** \> **View** \> **Campaigns**</span></span>

- <span data-ttu-id="18be4-130">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Tous les messages électroniques** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="18be4-130">**Threat management** \> **Explorer** \> **View** \> **All email** \> **Campaign** tab</span></span>

- <span data-ttu-id="18be4-131">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Hameçonnage** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="18be4-131">**Threat management** \> **Explorer** \> **View** \> **Phish** \> **Campaign** tab</span></span>

- <span data-ttu-id="18be4-132">**Gestion** \> des menaces **Explorateur** \> **Affichage** \> **Programmes malveillants** \> Onglet **campagne**</span><span class="sxs-lookup"><span data-stu-id="18be4-132">**Threat management** \> **Explorer** \> **View** \> **Malware** \> **Campaign** tab</span></span>

<span data-ttu-id="18be4-133">Pour accéder aux vues de campagne, vous devez être membre des groupes de rôles gestion de l' **organisation**, administrateur de la **sécurité**ou **lecteur de sécurité** dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="18be4-133">To access Campaign Views, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Reader** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="18be4-134">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="campaigns-overview"></a><span data-ttu-id="18be4-135">Vue d’ensemble des campagnes</span><span class="sxs-lookup"><span data-stu-id="18be4-135">Campaigns overview</span></span>

<span data-ttu-id="18be4-136">La page vue d’ensemble affiche des informations sur toutes les campagnes.</span><span class="sxs-lookup"><span data-stu-id="18be4-136">The overview page shows information about all campaigns.</span></span>

<span data-ttu-id="18be4-137">Sous l’onglet **campagne** par défaut, la zone **type de campagne** affiche un graphique à barres qui indique le nombre de destinataires par jour.</span><span class="sxs-lookup"><span data-stu-id="18be4-137">On the default **Campaign** tab, the **Campaign type** area shows a bar graph that shows the number of recipients per day.</span></span> <span data-ttu-id="18be4-138">Par défaut, le graphique affiche les données de **hameçonnage** et de **programmes malveillants** .</span><span class="sxs-lookup"><span data-stu-id="18be4-138">By default, the graph shows both **Phish** and **Malware** data.</span></span>

> [!TIP]
> <span data-ttu-id="18be4-139">Si vous ne voyez pas de données de campagne, essayez de modifier la plage de dates ou les [filtres](#filters-and-settings).</span><span class="sxs-lookup"><span data-stu-id="18be4-139">If you don't see any campaign data, try changing the date range or [filters](#filters-and-settings).</span></span>

<span data-ttu-id="18be4-140">Le reste de la page vue d’ensemble affiche les informations suivantes dans l’onglet **campagne** :</span><span class="sxs-lookup"><span data-stu-id="18be4-140">The rest of the overview page shows the following information on the **Campaign** tab:</span></span>

- <span data-ttu-id="18be4-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="18be4-141">**Name**</span></span>

- <span data-ttu-id="18be4-142">**Exemple d’objet** : la ligne d’objet de l’un des messages de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-142">**Sample subject**: The subject line of one of the messages in the campaign.</span></span> <span data-ttu-id="18be4-143">Notez que tous les messages de la campagne n’auront pas nécessairement le même objet.</span><span class="sxs-lookup"><span data-stu-id="18be4-143">Note that all messages in the campaign will not necessarily have the same subject.</span></span>

- <span data-ttu-id="18be4-144">**Ciblé**: pourcentage tel que calculé par : (nombre de destinataires de campagne dans votre organisation)/(nombre total de destinataires dans la campagne pour toutes les organisations du service).</span><span class="sxs-lookup"><span data-stu-id="18be4-144">**Targeted**: The percentage as calculated by: (the number of campaign recipients in your organization) / (the total number of recipients in the campaign across all organizations in the service).</span></span> <span data-ttu-id="18be4-145">Cette valeur indique le degré auquel la campagne est dirigée uniquement au sein de votre organisation (valeur la plus élevée) par rapport à d’autres organisations du service (une valeur inférieure).</span><span class="sxs-lookup"><span data-stu-id="18be4-145">This value indicates the degree to which the campaign is directed only at your organization (a higher value) vs. also directed at other organizations in the service (a lower value).</span></span>

- <span data-ttu-id="18be4-146">**Type**: cette valeur est **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="18be4-146">**Type**: This value is either **Phish** or **Malware**.</span></span>

- <span data-ttu-id="18be4-147">**Sous-type**: cette valeur contient davantage de détails sur la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-147">**Subtype**: This value contains more details about the campaign.</span></span> <span data-ttu-id="18be4-148">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="18be4-148">For example:</span></span>

  - <span data-ttu-id="18be4-149">**Hameçonnage**: le cas échéant, la marque qui est en hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-149">**Phish**: Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="18be4-150">Par exemple,,,, `Microsoft` `365` `Unknown` `Outlook` ou `DocuSign` .</span><span class="sxs-lookup"><span data-stu-id="18be4-150">For example, `Microsoft`, `365`, `Unknown`, `Outlook`, or `DocuSign`.</span></span>

  - <span data-ttu-id="18be4-151">**Programme malveillant**: par exemple, `HTML/PHISH` ou `HTML/<MalwareFamilyName>` .</span><span class="sxs-lookup"><span data-stu-id="18be4-151">**Malware**: For example, `HTML/PHISH` or `HTML/<MalwareFamilyName>`.</span></span>

<span data-ttu-id="18be4-152">Le cas échéant, la marque en cours d’hameçonnage par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-152">Where available, the brand that is being phished by this campaign.</span></span> <span data-ttu-id="18be4-153">Lorsque la détection est pilotée par la technologie ATP, le préfixe **ATP** est ajouté à la valeur de sous-type.</span><span class="sxs-lookup"><span data-stu-id="18be4-153">When the detection is driven by ATP technology, the prefix **ATP-** is added to the subtype value.</span></span>

- <span data-ttu-id="18be4-154">**Destinataires** : nombre d’utilisateurs qui ont été ciblés par cette campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-154">**Recipients**: The number of users that were targeted by this campaign.</span></span>

- <span data-ttu-id="18be4-155">**Boîte de réception**: nombre d’utilisateurs ayant reçu des messages de cette campagne dans leur boîte de réception (non remis dans leur dossier courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="18be4-155">**Inboxed**: The number of users that received messages from this campaign in their Inbox (not delivered to their Junk Email folder).</span></span>

- <span data-ttu-id="18be4-156">**Clic**: nombre d’utilisateurs sur lesquels l’utilisateur a cliqué sur l’URL ou pour ouvrir la pièce jointe dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="18be4-156">**Clicked**: The number of users that clicked on the URL or opened the attachment in the phishing message.</span></span>

- <span data-ttu-id="18be4-157">**Cliquez sur taux**: pourcentage tel que calculé par « boîte de réception sur laquelle l'**utilisateur a cliqué**  /  **Inboxed**».</span><span class="sxs-lookup"><span data-stu-id="18be4-157">**Click rate**: The percentage as calculated by "**Clicked** / **Inboxed**".</span></span> <span data-ttu-id="18be4-158">Cette valeur est un indicateur de l’efficacité de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-158">This value is an indicator of the effectiveness of the campaign.</span></span> <span data-ttu-id="18be4-159">En d’autres termes, si les destinataires pouvaient identifier le message en tant qu’hameçonnage, et s’ils ne cliquaient pas sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="18be4-159">In other words, if the recipients were able to identify the message as phishing, and if they didn't click on the payload URL.</span></span>

  <span data-ttu-id="18be4-160">Notez que le **taux de clic** n’est pas utilisé dans les campagnes de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="18be4-160">Note that **Click rate** isn't used in malware campaigns.</span></span>

- <span data-ttu-id="18be4-161">**Consulté**le nombre d’utilisateurs qui l’ont fait par le biais du site Web de charge utile.</span><span class="sxs-lookup"><span data-stu-id="18be4-161">**Visited**: How many users actually made it through to the payload website.</span></span> <span data-ttu-id="18be4-162">S’il y a des valeurs de **clic** , mais que les liens fiables bloquent l’accès au site Web, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="18be4-162">If there are **Clicked** values, but Safe Links blocked access to the website, this value will be zero.</span></span>

<span data-ttu-id="18be4-163">L’onglet origine de la **campagne** affiche les sources de messages sur une carte du monde.</span><span class="sxs-lookup"><span data-stu-id="18be4-163">The **Campaign origin** tab shows the message sources on a map of the world.</span></span>

### <a name="filters-and-settings"></a><span data-ttu-id="18be4-164">Filtres et paramètres</span><span class="sxs-lookup"><span data-stu-id="18be4-164">Filters and settings</span></span>

<span data-ttu-id="18be4-165">En haut de la page vues de la campagne, il existe plusieurs paramètres de filtre et de requête qui vous permettent de trouver et d’isoler des campagnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="18be4-165">At the top of the Campaign Views page, there are several filter and query settings to help you find and isolate specific campaigns.</span></span>

![Filtres de campagne](../../media/campaign-filters-and-settings.png)

<span data-ttu-id="18be4-167">Le filtrage le plus élémentaire que vous pouvez faire est la date/l’heure de début et la date/heure de fin.</span><span class="sxs-lookup"><span data-stu-id="18be4-167">The most basic filtering that you can do is the start date/time and the end date/time.</span></span>

<span data-ttu-id="18be4-168">Pour filtrer davantage l’affichage, vous pouvez effectuer une seule propriété avec plusieurs valeurs de filtrage en cliquant sur le bouton **type de campagne** , en sélectionnant l’option **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="18be4-168">To further filter the view, you can do single property with multiple values filtering by clicking the **Campaign type** button, making your selection, and then clicking **Refresh**.</span></span>

<span data-ttu-id="18be4-169">Les propriétés de la campagne disponibles sont décrites dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="18be4-169">The available campaign properties are described in the following list:</span></span>

- <span data-ttu-id="18be4-170">Basic</span><span class="sxs-lookup"><span data-stu-id="18be4-170">Basic</span></span>

  - <span data-ttu-id="18be4-171">**Type de campagne**: sélectionnez **programme malveillant** ou **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="18be4-171">**Campaign type**: Select **Malware** or **Phish**.</span></span> <span data-ttu-id="18be4-172">L’effacement des sélections a le même résultat que la sélection des deux.</span><span class="sxs-lookup"><span data-stu-id="18be4-172">Clearing the selections has the same result as selecting both.</span></span>
  - <span data-ttu-id="18be4-173">**Nom de la campagne**</span><span class="sxs-lookup"><span data-stu-id="18be4-173">**Campaign name**</span></span>
  - <span data-ttu-id="18be4-174">**Sous-type de campagne**</span><span class="sxs-lookup"><span data-stu-id="18be4-174">**Campaign subtype**</span></span>
  - <span data-ttu-id="18be4-175">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-175">**Sender**</span></span>
  - <span data-ttu-id="18be4-176">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="18be4-176">**Recipients**</span></span>
  - <span data-ttu-id="18be4-177">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-177">**Sender domain**</span></span>
  - <span data-ttu-id="18be4-178">**Subject**</span><span class="sxs-lookup"><span data-stu-id="18be4-178">**Subject**</span></span>
  - <span data-ttu-id="18be4-179">**Nom de fichier des pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="18be4-179">**Attachment filename**</span></span>
  - <span data-ttu-id="18be4-180">**Famille de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="18be4-180">**Malware family**</span></span>
  - <span data-ttu-id="18be4-181">**Action de remise**</span><span class="sxs-lookup"><span data-stu-id="18be4-181">**Delivery action**</span></span>
  - <span data-ttu-id="18be4-182">**Technologie de détection**</span><span class="sxs-lookup"><span data-stu-id="18be4-182">**Detection technology**</span></span>
  - <span data-ttu-id="18be4-183">**Tags**</span><span class="sxs-lookup"><span data-stu-id="18be4-183">**Tags**</span></span>
  - <span data-ttu-id="18be4-184">**Substitutions système**</span><span class="sxs-lookup"><span data-stu-id="18be4-184">**System overrides**</span></span>

- <span data-ttu-id="18be4-185">Avancé</span><span class="sxs-lookup"><span data-stu-id="18be4-185">Advanced</span></span>

  - <span data-ttu-id="18be4-186">**ID de message Internet**: disponible dans le champ d’en-tête **message-ID** de l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="18be4-186">**Internet message ID**: Available in the **Message-ID** header field in the message header.</span></span> <span data-ttu-id="18be4-187">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (Notez les chevrons).</span><span class="sxs-lookup"><span data-stu-id="18be4-187">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
  
  - <span data-ttu-id="18be4-188">**ID de message réseau**: valeur Guid disponible dans le champ d’en-tête **X-MS-Exchange-Organization-Network-message-ID** de l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="18be4-188">**Network message ID**: A GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header field in the message header.</span></span>
  
  - <span data-ttu-id="18be4-189">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-189">**Sender IP**</span></span>
  
  - <span data-ttu-id="18be4-190">**Attachment SHA256**: pour trouver la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes : `certutil.exe -hashfile "<Path>\<Filename>" SHA256` .</span><span class="sxs-lookup"><span data-stu-id="18be4-190">**Attachment SHA256**: To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt: `certutil.exe -hashfile "<Path>\<Filename>" SHA256`.</span></span>
  
  - <span data-ttu-id="18be4-191">**ID de cluster**</span><span class="sxs-lookup"><span data-stu-id="18be4-191">**Cluster ID**</span></span>
  
  - <span data-ttu-id="18be4-192">**ID de stratégie d’alerte**</span><span class="sxs-lookup"><span data-stu-id="18be4-192">**Alert Policy ID**</span></span>

- <span data-ttu-id="18be4-193">URL</span><span class="sxs-lookup"><span data-stu-id="18be4-193">URLs</span></span>

  - <span data-ttu-id="18be4-194">**Domaine d’URL**</span><span class="sxs-lookup"><span data-stu-id="18be4-194">**URL domain**</span></span>
  - <span data-ttu-id="18be4-195">**Domaine et chemin d’accès de l’URL**</span><span class="sxs-lookup"><span data-stu-id="18be4-195">**URL domain and path**</span></span>
  - <span data-ttu-id="18be4-196">**URL**</span><span class="sxs-lookup"><span data-stu-id="18be4-196">**URL**</span></span>
  - <span data-ttu-id="18be4-197">**Chemin d’URL**</span><span class="sxs-lookup"><span data-stu-id="18be4-197">**URL path**</span></span>
  - <span data-ttu-id="18be4-198">**Cliquez sur verdict**</span><span class="sxs-lookup"><span data-stu-id="18be4-198">**Click verdict**</span></span>

<span data-ttu-id="18be4-199">Pour un filtrage plus avancé, incluant le filtrage par plusieurs propriétés, vous pouvez cliquer sur le bouton **filtre avancé** pour créer une requête.</span><span class="sxs-lookup"><span data-stu-id="18be4-199">For more advanced filtering, including filtering by multiple properties, you can click the **Advanced filter** button to build a query.</span></span> <span data-ttu-id="18be4-200">Les mêmes propriétés de campagne sont disponibles, mais avec les améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="18be4-200">The same campaign properties are available, but with the following enhancements:</span></span>

- <span data-ttu-id="18be4-201">Vous pouvez cliquer sur **Ajouter une condition** pour sélectionner plusieurs conditions.</span><span class="sxs-lookup"><span data-stu-id="18be4-201">You can click **Add a condition** to select multiple conditions.</span></span>
- <span data-ttu-id="18be4-202">Vous pouvez choisir l' **And** opérateur and **ou or entre** les conditions.</span><span class="sxs-lookup"><span data-stu-id="18be4-202">You can choose the **And** or **Or** operator between conditions.</span></span>
- <span data-ttu-id="18be4-203">Vous pouvez sélectionner l’élément de **groupe** de conditions au bas de la liste conditions pour créer des conditions composées complexes.</span><span class="sxs-lookup"><span data-stu-id="18be4-203">You can select the **Condition group** item at the bottom of the conditions list to form complex compound conditions.</span></span>

<span data-ttu-id="18be4-204">Lorsque vous avez terminé, cliquez sur le bouton **requête** .</span><span class="sxs-lookup"><span data-stu-id="18be4-204">When you're finished, click the **Query** button.</span></span>

<span data-ttu-id="18be4-205">Une fois que vous avez créé un filtre de base ou avancé, vous pouvez l’enregistrer à l’aide de la **requête enregistrer** la requête ou **enregistrer la requête sous**.</span><span class="sxs-lookup"><span data-stu-id="18be4-205">After you create a basic or advanced filter, you can save it by using **Save query** or **Save query as**.</span></span> <span data-ttu-id="18be4-206">Par la suite, lorsque vous revenez à vues de la campagne, vous pouvez charger un filtre enregistré en cliquant sur paramètres de la **requête enregistrée**.</span><span class="sxs-lookup"><span data-stu-id="18be4-206">Later, when you return to Campaign Views, you can load a saved filter by clicking **Saved query settings**.</span></span>

<span data-ttu-id="18be4-207">Pour exporter le graphique ou la liste des campagnes, cliquez sur **Exporter** , puis sélectionnez **Exporter les données du graphique** ou exporter la liste des **campagnes**.</span><span class="sxs-lookup"><span data-stu-id="18be4-207">To export the graph or the list of campaigns, click **Export** and select **Export chart data** or **Export campaign list**.</span></span>

<span data-ttu-id="18be4-208">Si vous disposez d’un abonnement Microsoft Defender ATP, vous pouvez cliquer sur **WDATP** pour connecter ou déconnecter les informations de campagne avec Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="18be4-208">If you have a Microsoft Defender ATP subscription, you can click **WDATP** to connect or disconnect the campaigns information with Microsoft Defender ATP.</span></span> <span data-ttu-id="18be4-209">Pour plus d’informations, reportez-vous à la rubrique [intégrer Office 365 ATP avec Microsoft Defender ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/integrate-office-365-ti-with-wdatp).</span><span class="sxs-lookup"><span data-stu-id="18be4-209">For more information, see [Integrate Office 365 ATP with Microsoft Defender ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/integrate-office-365-ti-with-wdatp).</span></span>

## <a name="campaign-details"></a><span data-ttu-id="18be4-210">Détails de la campagne</span><span class="sxs-lookup"><span data-stu-id="18be4-210">Campaign details</span></span>

<span data-ttu-id="18be4-211">Lorsque vous cliquez sur le nom d’une campagne, les détails de la campagne s’affichent dans un menu volant.</span><span class="sxs-lookup"><span data-stu-id="18be4-211">When you click on the name of a campaign, the campaign details appear in a flyout.</span></span>

### <a name="campaign-information"></a><span data-ttu-id="18be4-212">Informations sur la campagne</span><span class="sxs-lookup"><span data-stu-id="18be4-212">Campaign information</span></span>

<span data-ttu-id="18be4-213">En haut de la vue Détails de la campagne, les informations de campagne suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="18be4-213">At the top of the campaign details view, the following campaign information is available:</span></span>

- <span data-ttu-id="18be4-214">**ID**: identificateur unique de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-214">**ID**: The unique campaign identifier.</span></span>

- <span data-ttu-id="18be4-215">**Démarré** et **terminé**: date de début et date de fin de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-215">**Started** and **Ended**: The start date and end date of the campaign.</span></span> <span data-ttu-id="18be4-216">Notez que ces dates peuvent s’étendre davantage que vos dates de filtrage sélectionnées sur la page de vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="18be4-216">Note that these dates might extend further than your filter dates that you selected on the overview page.</span></span>

- <span data-ttu-id="18be4-217">**Impact**: cette section contient les données suivantes pour le filtre de plage de dates que vous avez sélectionné (ou que vous sélectionnez dans la chronologie) :</span><span class="sxs-lookup"><span data-stu-id="18be4-217">**Impact**: This section contains the following data for the date range filter you selected (or that you select in the timeline):</span></span>
  
  - <span data-ttu-id="18be4-218">Nombre total de destinataires.</span><span class="sxs-lookup"><span data-stu-id="18be4-218">The total number of recipients.</span></span>
  - <span data-ttu-id="18be4-219">Nombre de messages qui ont reçu la boîte de réception (c’est-à-dire remis dans la boîte de réception, et non dans le dossier courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="18be4-219">The number of messages that were "Inboxed" (that is, delivered to the Inbox, not to the Junk Email folder).</span></span>
  - <span data-ttu-id="18be4-220">Le nombre d’utilisateurs sur lesquels l’utilisateur a cliqué dans le message de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="18be4-220">How many users clicked on the URL payload in the phishing message.</span></span>
  - <span data-ttu-id="18be4-221">Howe nombre d’utilisateurs visitaient l’URL.</span><span class="sxs-lookup"><span data-stu-id="18be4-221">Howe many users visited the URL.</span></span>

- <span data-ttu-id="18be4-222">**Ciblé**: pourcentage tel que calculé par : (nombre de destinataires de campagne dans votre organisation)/(nombre total de destinataires dans la campagne pour toutes les organisations du service).</span><span class="sxs-lookup"><span data-stu-id="18be4-222">**Targeted**: The percentage as calculated by: (the number of campaign recipients in your organization) / (the total number of recipients in the campaign across all organizations in the service).</span></span> <span data-ttu-id="18be4-223">Notez que cette valeur est calculée sur toute la durée de vie de la campagne et ne change pas en fonction des filtres de date.</span><span class="sxs-lookup"><span data-stu-id="18be4-223">Note that this value is calculated over the entire lifetime of the campaign, and doesn't change based on date filters.</span></span>

- <span data-ttu-id="18be4-224">Chronologie interactive de l’activité de campagne : la chronologie affiche l’activité sur toute la durée de vie de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-224">An interactive timeline of campaign activity: The timeline shows activity over the entire lifetime of the campaign.</span></span> <span data-ttu-id="18be4-225">Par défaut, la zone ombrée inclut le filtre de plage de dates que vous avez sélectionné dans la vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="18be4-225">By default, the shaded area includes the date range filter that you selected in the overview.</span></span> <span data-ttu-id="18be4-226">Vous pouvez cliquer et faire glisser pour sélectionner un point de départ et un point de terminaison spécifiques, ce <u>qui modifiera les données affichées dans la zone d' **impact** , et sur le reste de la page, comme décrit dans les sections suivantes</u>.</span><span class="sxs-lookup"><span data-stu-id="18be4-226">You can click and drag to select a specific start point and end point, <u>which will change the data that's displayed in **Impact** area, and on the rest of the page as described in the next sections</u>.</span></span>

<span data-ttu-id="18be4-227">Dans la barre de titre, vous pouvez cliquer sur le bouton Télécharger la campagne en **écriture** ![ pour télécharger ](../../media/download-campaign-write-up-button.png) les détails de la campagne dans un document Word (par défaut, nommé CampaignReport.docx).</span><span class="sxs-lookup"><span data-stu-id="18be4-227">In the title bar, you can click the **Download campaign write-up** button ![Download campaign write-up icon](../../media/download-campaign-write-up-button.png) to download the campaign details to a Word document (by default, named CampaignReport.docx).</span></span> <span data-ttu-id="18be4-228">Notez que le téléchargement contient des détails sur toute la durée de vie de la campagne (pas seulement sur les dates de filtrage sélectionnées).</span><span class="sxs-lookup"><span data-stu-id="18be4-228">Note that the download contains details over the entire lifetime of the campaign (not just the filter dates you selected).</span></span>

![Informations sur la campagne](../../media/campaign-details-campaign-info.png)

### <a name="campaign-flow"></a><span data-ttu-id="18be4-230">Flux de la campagne</span><span class="sxs-lookup"><span data-stu-id="18be4-230">Campaign flow</span></span>

<span data-ttu-id="18be4-231">Au milieu de la vue Détails de la campagne, des informations importantes sur la campagne sont présentées dans la section **flux** , dans un diagramme de flux horizontal (appelé diagramme _Sankey_ ).</span><span class="sxs-lookup"><span data-stu-id="18be4-231">In the middle of the campaign details view, important details about the campaign are presented in the **Flow** section in a horizontal flow diagram (known as a _Sankey_ diagram).</span></span> <span data-ttu-id="18be4-232">Ces détails vous aideront à comprendre les éléments de la campagne et l’impact potentiel au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="18be4-232">These details will help you to understand the elements of the campaign and the potential impact in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="18be4-233">Les informations affichées dans le diagramme de **flux** sont contrôlées par la plage de dates grisée dans la chronologie, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="18be4-233">The information that's displayed in the **Flow** diagram is controlled by the shaded date range in the timeline as described in the previous section.</span></span>

![Détails de la campagne ne contenant pas d’URL d’utilisateur](../../media/campaign-details-no-recipient-actions.png)

<span data-ttu-id="18be4-235">Si vous pointez sur une bande horizontale dans le diagramme, vous pouvez voir le nombre de messages associés (par exemple, les messages d’une adresse IP source particulière, les messages provenant de l’adresse IP source en utilisant le domaine d’expéditeur spécifié, etc.).</span><span class="sxs-lookup"><span data-stu-id="18be4-235">If you hover over a horizontal band in the diagram, you'll see the number of related messages (for example, messages from a particular source IP, messages from the source IP using the specified sender domain, etc.).</span></span>

<span data-ttu-id="18be4-236">Le diagramme contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="18be4-236">The diagram contains the following information:</span></span>

- <span data-ttu-id="18be4-237">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-237">**Sender IPs**</span></span>

- <span data-ttu-id="18be4-238">**Domaines de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-238">**Sender domains**</span></span>

- <span data-ttu-id="18be4-239">Valeurs de **verdict du filtre**: les valeurs de verdict sont liées aux valeurs de filtrage d’hameçonnage et de filtrage du courrier indésirable disponibles, comme décrit dans [les en-têtes de message anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-239">**Filter verdicts**: Verdict values are related to the available phishing and spam filtering verdicts as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="18be4-240">Les valeurs disponibles sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="18be4-240">The available values are described in the following table:</span></span>

  ****

  |<span data-ttu-id="18be4-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="18be4-241">Value</span></span>|<span data-ttu-id="18be4-242">Verdict du filtre de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="18be4-242">Spam filter verdict</span></span>|<span data-ttu-id="18be4-243">Description</span><span class="sxs-lookup"><span data-stu-id="18be4-243">Description</span></span>|
  |---|---|---|
  |<span data-ttu-id="18be4-244">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="18be4-244">**Allowed**</span></span>|`SFV:SKN` <br/><br/> `SFV:SKI`|<span data-ttu-id="18be4-245">Le message a été marqué comme n’étant pas un courrier indésirable et/ou a ignoré le filtrage avant d’être évalué par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-245">The message was marked as not spam and/or skipped filtering before being evaluated by spam filtering.</span></span> <span data-ttu-id="18be4-246">Par exemple, le message a été marqué comme n’étant pas un courrier indésirable par une règle de flux de messagerie (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="18be4-246">For example, the message was marked as not spam by a mail flow rule (also known as a transport rule).</span></span><br/><br/><span data-ttu-id="18be4-247">Le message a ignoré le filtrage du courrier indésirable pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="18be4-247">The message skipped spam filtering for other reasons.</span></span> <span data-ttu-id="18be4-248">Par exemple, l’expéditeur et le destinataire semblent être dans la même organisation.</span><span class="sxs-lookup"><span data-stu-id="18be4-248">For example, the sender and recipient appear to be in the same organization.</span></span>|
  |<span data-ttu-id="18be4-249">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="18be4-249">**Blocked**</span></span>|`SFV:SKS`|<span data-ttu-id="18be4-250">Le message a été marqué comme courrier indésirable avant d’être évalué par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-250">The message was marked as spam before being evaluated by spam filtering.</span></span> <span data-ttu-id="18be4-251">Par exemple, par une règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="18be4-251">For example, by a mail flow rule.</span></span>|
  |<span data-ttu-id="18be4-252">**Détecté**</span><span class="sxs-lookup"><span data-stu-id="18be4-252">**Detected**</span></span>|`SFV:SPM`|<span data-ttu-id="18be4-253">Le message a été marqué comme courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-253">The message was marked as spam by spam filtering.</span></span>|
  |<span data-ttu-id="18be4-254">**Non détecté**</span><span class="sxs-lookup"><span data-stu-id="18be4-254">**Not Detected**</span></span>|`SFV:NSPM`|<span data-ttu-id="18be4-255">Le message a été marqué comme non courrier indésirable par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-255">The message was marked as not spam by spam filtering.</span></span>|
  |<span data-ttu-id="18be4-256">**A**</span><span class="sxs-lookup"><span data-stu-id="18be4-256">**Released**</span></span>|`SFV:SKQ`|<span data-ttu-id="18be4-257">Le message a ignoré le filtrage du courrier indésirable, car il a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="18be4-257">The message skipped spam filtering because it was released from quarantine.</span></span>|
  |<span data-ttu-id="18be4-258">**Autoriser le client**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-258">**Tenant Allow**<sup>\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="18be4-259">Le message a ignoré le filtrage du courrier indésirable en raison des paramètres d’une stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-259">The message skipped spam filtering because of the settings in an anti-spam policy.</span></span> <span data-ttu-id="18be4-260">Par exemple, l’expéditeur se trouve dans la liste des expéditeurs autorisés ou dans la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="18be4-260">For example, the sender was in the allowed sender list or allowed domain list.</span></span>|
  |<span data-ttu-id="18be4-261">**Bloc de locataire**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-261">**Tenant Block**<sup>\*\*</sup></span></span>|`SFV:SKA`|<span data-ttu-id="18be4-262">Le message a été bloqué par le filtrage du courrier indésirable en raison des paramètres d’une stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-262">The message was blocked by spam filtering because of the settings in an anti-spam policy.</span></span> <span data-ttu-id="18be4-263">Par exemple, l’expéditeur se trouve dans la liste des expéditeurs autorisés ou dans la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="18be4-263">For example, the sender was in the allowed sender list or allowed domain list.</span></span>|
  |<span data-ttu-id="18be4-264">**Autorisation de l’utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-264">**User Allow**<sup>\*</sup></span></span>|`SFV:SFE`|<span data-ttu-id="18be4-265">Le message a ignoré le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs approuvés d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18be4-265">The message skipped spam filtering because the sender was in a user's Safe Senders list.</span></span>|
  |<span data-ttu-id="18be4-266">**Bloc utilisateur**<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-266">**User Block**<sup>\*\*</sup></span></span>|`SFV:BLK`|<span data-ttu-id="18be4-267">Le message a été bloqué par le filtrage du courrier indésirable, car l’expéditeur se trouvait dans la liste des expéditeurs bloqués d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18be4-267">The message was blocked by spam filtering because the sender was in a user's Blocked Senders list.</span></span>|
  |<span data-ttu-id="18be4-268">**ZAP**</span><span class="sxs-lookup"><span data-stu-id="18be4-268">**ZAP**</span></span>|<span data-ttu-id="18be4-269">s/o</span><span class="sxs-lookup"><span data-stu-id="18be4-269">n/a</span></span>|<span data-ttu-id="18be4-270">[Vidage automatique des heures zéro (ZAP)](zero-hour-auto-purge.md) déplacement du message remis vers le dossier de courrier indésirable ou la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="18be4-270">[Zero-hour auto purge (ZAP)](zero-hour-auto-purge.md) moved the delivered message to the Junk Email folder or quarantine.</span></span> <span data-ttu-id="18be4-271">Vous configurez l’action dans votre stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18be4-271">You configure the action in your anti-spam policy.</span></span>|
  |

  <span data-ttu-id="18be4-272"><sup>\*</sup> Examinez vos stratégies de blocage du courrier indésirable, car le message autorisé aurait probablement été bloqué par le service.</span><span class="sxs-lookup"><span data-stu-id="18be4-272"><sup>\*</sup> Review your anti-spam policies, because the allowed message would have likely been blocked by the service.</span></span>

  <span data-ttu-id="18be4-273"><sup>\*\*</sup> Examinez vos stratégies de blocage du courrier indésirable, car ces messages doivent être mis en quarantaine et non remis.</span><span class="sxs-lookup"><span data-stu-id="18be4-273"><sup>\*\*</sup> Review your anti-spam policies, because these messages should be quarantined, not delivered.</span></span>

- <span data-ttu-id="18be4-274">**Emplacements de remise**: vous souhaiterez probablement analyser les messages remis aux destinataires (dans la boîte de réception ou le dossier courrier indésirable), même si les utilisateurs ne cliquaient pas sur l’URL de la charge utile dans le message.</span><span class="sxs-lookup"><span data-stu-id="18be4-274">**Delivery locations**: You'll likely want to investigate messages that were delivered to recipients (either to the Inbox or the Junk Email folder), even if users didn't click on the payload URL in the message.</span></span> <span data-ttu-id="18be4-275">Vous pouvez également supprimer les messages mis en quarantaine en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="18be4-275">You can also remove the quarantined messages from quarantine.</span></span> <span data-ttu-id="18be4-276">Pour plus d’informations, consultez la rubrique [messages électroniques mis en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-276">For more information, see [Quarantined email messages in EOP](quarantine-email-messages.md).</span></span>

  - <span data-ttu-id="18be4-277">**Dossier supprimé**</span><span class="sxs-lookup"><span data-stu-id="18be4-277">**Deleted folder**</span></span>
  - <span data-ttu-id="18be4-278">**Raccroché**</span><span class="sxs-lookup"><span data-stu-id="18be4-278">**Dropped**</span></span>
  - <span data-ttu-id="18be4-279">**External**: le destinataire est situé dans votre organisation de messagerie locale dans les environnements hybrides.</span><span class="sxs-lookup"><span data-stu-id="18be4-279">**External**: The recipient is located in your on-premises email organization in hybrid environments.</span></span>
  - <span data-ttu-id="18be4-280">**Échec**</span><span class="sxs-lookup"><span data-stu-id="18be4-280">**Failed**</span></span>
  - <span data-ttu-id="18be4-281">**Renvoyé**</span><span class="sxs-lookup"><span data-stu-id="18be4-281">**Forwarded**</span></span>
  - <span data-ttu-id="18be4-282">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="18be4-282">**Inbox**</span></span>
  - <span data-ttu-id="18be4-283">**Dossier Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="18be4-283">**Junk folder**</span></span>
  - <span data-ttu-id="18be4-284">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="18be4-284">**Quarantine**</span></span>
  - <span data-ttu-id="18be4-285">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="18be4-285">**Unknown**</span></span>

- <span data-ttu-id="18be4-286">**Clics sur l’URL**: ces valeurs sont décrites dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="18be4-286">**URL clicks**: These values are described in the next section.</span></span>

> [!NOTE]
> <span data-ttu-id="18be4-287">Dans toutes les couches contenant plus de 10 éléments, les 10 premiers éléments sont affichés, tandis que les autres sont regroupés dans les **autres**.</span><span class="sxs-lookup"><span data-stu-id="18be4-287">In all layers that contain more than 10 items, the top 10 items are shown, while the rest are bundled together in **Others**.</span></span>

#### <a name="url-clicks"></a><span data-ttu-id="18be4-288">Clics d’URL</span><span class="sxs-lookup"><span data-stu-id="18be4-288">URL clicks</span></span>

<span data-ttu-id="18be4-289">Lorsqu’un message d’hameçonnage est remis dans le dossier boîte de réception ou courrier indésirable d’un destinataire, il y a toujours un risque que l’utilisateur clique sur l’URL de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="18be4-289">When a phishing message is delivered to a recipient's Inbox or Junk Email folder, there's always a chance that the user will click on the payload URL.</span></span> <span data-ttu-id="18be4-290">Le fait de ne pas cliquer sur l’URL est une petite mesure de succès, mais vous devez déterminer pourquoi le message de hameçonnage a été remis à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="18be4-290">Not clicking on the URL is a small measure of success, but you need to determine why the phishing message was even delivered to the mailbox.</span></span>

<span data-ttu-id="18be4-291">Si un utilisateur a cliqué sur l’URL de la charge utile dans le message d’hameçonnage, les actions sont affichées dans la zone de **clics sur l’URL** du diagramme dans la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-291">If a user clicked on the payload URL in the phishing message, the actions are displayed in the **URL clicks** area of the diagram in the campaign details view.</span></span>

- <span data-ttu-id="18be4-292">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="18be4-292">**Allowed**</span></span>

- <span data-ttu-id="18be4-293">**BlockPage**: le destinataire a cliqué sur l’URL de charge utile, mais son accès au site Web malveillant a été bloqué par une stratégie de [liens fiables](atp-safe-links.md) dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="18be4-293">**BlockPage**: The recipient clicked on the payload URL, but their access to the malicious website was blocked by a [Safe Links](atp-safe-links.md) policy in your organization.</span></span>

- <span data-ttu-id="18be4-294">**BlockPageOverride**: le destinataire a cliqué sur l’URL de charge utile dans le message, les liens fiables ont essayé de les arrêter, mais ils ont été autorisés à remplacer le bloc.</span><span class="sxs-lookup"><span data-stu-id="18be4-294">**BlockPageOverride**: The recipient clicked on the payload URL in the message, Safe Links tried to stop them, but they were allowed to override the block.</span></span> <span data-ttu-id="18be4-295">Inspectez vos [stratégies de liens fiables](set-up-atp-safe-links-policies.md) afin de déterminer pourquoi les utilisateurs sont autorisés à remplacer le verdict des liens fiables et à passer au site Web malveillant.</span><span class="sxs-lookup"><span data-stu-id="18be4-295">Inspect your [Safe Links policies](set-up-atp-safe-links-policies.md) to see why users are allowed to override the Safe Links verdict and continue to the malicious website.</span></span>

- <span data-ttu-id="18be4-296">**PendingDetonationPage**: pièces jointes fiables dans Office 365 la protection avancée contre les menaces est en cours d’ouverture et d’étude de l’URL de charge utile dans un environnement d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="18be4-296">**PendingDetonationPage**: Safe Attachments in Office 365 ATP is in the process of opening and investigating the payload URL in a virtual computer environment.</span></span>

- <span data-ttu-id="18be4-297">**PendingDetonationPageOverride**: le destinataire a été autorisé à remplacer le processus de détonation de charge utile et à ouvrir l’URL sans attendre les résultats.</span><span class="sxs-lookup"><span data-stu-id="18be4-297">**PendingDetonationPageOverride**: The recipient was allowed to override the payload detonation process and open the URL without waiting for the results.</span></span>

### <a name="tabs"></a><span data-ttu-id="18be4-298">Onglets</span><span class="sxs-lookup"><span data-stu-id="18be4-298">Tabs</span></span>

<span data-ttu-id="18be4-299">Les onglets de la vue Détails de la campagne vous permettent d’approfondir la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-299">The tabs in the campaign details view allow you to further investigate the campaign.</span></span>

> [!TIP]
> <span data-ttu-id="18be4-300">Les informations affichées dans les onglets sont contrôlées par la plage de dates grisée dans le scénario, comme décrit dans la section [informations sur la campagne](#campaign-information) .</span><span class="sxs-lookup"><span data-stu-id="18be4-300">The information that's displayed on the tabs is controlled by the shaded date range in the timeline as described in [Campaign information](#campaign-information) section.</span></span>

- <span data-ttu-id="18be4-301">**Clics**sur l’URL : si les utilisateurs ne cliquent pas sur l’URL de la charge utile dans le message, cette section est vide.</span><span class="sxs-lookup"><span data-stu-id="18be4-301">**URL clicks**: If users didn't click on the payload URL in the message, this section will be blank.</span></span> <span data-ttu-id="18be4-302">Si un utilisateur a pu cliquer sur l’URL, les valeurs suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="18be4-302">If a user was able to click on the URL, the following values will be populated:</span></span>

  - <span data-ttu-id="18be4-303">**Utilisateur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-303">**User**<sup>\*</sup></span></span>
  - <span data-ttu-id="18be4-304">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-304">**URL**<sup>\*</sup></span></span>
  - <span data-ttu-id="18be4-305">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="18be4-305">**Click time**</span></span>
  - <span data-ttu-id="18be4-306">**Cliquez sur verdict**</span><span class="sxs-lookup"><span data-stu-id="18be4-306">**Click verdict**</span></span>

- <span data-ttu-id="18be4-307">**Adresses IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="18be4-307">**Sender IPs**</span></span>

  - <span data-ttu-id="18be4-308">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-308">**Sender IP**<sup>\*</sup></span></span>
  - <span data-ttu-id="18be4-309">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="18be4-309">**Total count**</span></span>
  - <span data-ttu-id="18be4-310">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="18be4-310">**Inboxed**</span></span>
  - <span data-ttu-id="18be4-311">**Pas de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="18be4-311">**Not Inboxed**</span></span>
  - <span data-ttu-id="18be4-312">**SPF transmis**: l’expéditeur a été authentifié par [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-312">**SPF passed**: The sender was authenticated by the [Sender Policy Framework (SPF)](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="18be4-313">Un expéditeur qui ne passe pas la validation SPF indique un expéditeur non authentifié ou le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="18be4-313">A sender that doesn't pass SPF validation indicates an unauthenticated sender, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="18be4-314">**Expéditeurs**</span><span class="sxs-lookup"><span data-stu-id="18be4-314">**Senders**</span></span>

  - <span data-ttu-id="18be4-315">**Expéditeur**: il s’agit de l’adresse de l’expéditeur réelle dans la commande SMTP Mail from, qui n’est pas nécessairement l’adresse de messagerie de l’expéditeur que les utilisateurs voient dans leurs clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="18be4-315">**Sender**: This is the actual sender address in the SMTP MAIL FROM command, which is not necessarily the From: email address that users see in their email clients.</span></span>
  - <span data-ttu-id="18be4-316">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="18be4-316">**Total count**</span></span>
  - <span data-ttu-id="18be4-317">**Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="18be4-317">**Inboxed**</span></span>
  - <span data-ttu-id="18be4-318">**Pas de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="18be4-318">**Not Inboxed**</span></span>
  - <span data-ttu-id="18be4-319">**DKIM transmis**: l’expéditeur a été authentifié par des [clés de domaine identifiées par des clés de domaine (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-319">**DKIM passed**: The sender was authenticated by [Domain Keys Identified Mail (DKIM)](support-for-validation-of-dkim-signed-messages.md).</span></span> <span data-ttu-id="18be4-320">Un expéditeur qui ne passe pas la validation DKIM indique un expéditeur non authentifié ou le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="18be4-320">A sender that doesn't pass DKIM validation indicates an unauthenticated sender, or the message is spoofing a legitimate sender.</span></span>
  - <span data-ttu-id="18be4-321">**DMARC réussi**: l’expéditeur a été authentifié par [l’authentification de message basée sur un domaine, la création de rapports et la conformité (DMARC)](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="18be4-321">**DMARC passed**: The sender was authenticated by [Domain-based Message Authentication, Reporting, and Conformance (DMARC)](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="18be4-322">Un expéditeur qui ne passe pas la validation DMARC indique un expéditeur non authentifié ou le message usurpe l’identité d’un expéditeur légitime.</span><span class="sxs-lookup"><span data-stu-id="18be4-322">A sender that doesn't pass DMARC validation indicates an unauthenticated sender, or the message is spoofing a legitimate sender.</span></span>

- <span data-ttu-id="18be4-323">**Attachments**</span><span class="sxs-lookup"><span data-stu-id="18be4-323">**Attachments**</span></span>

  - <span data-ttu-id="18be4-324">**Filename**</span><span class="sxs-lookup"><span data-stu-id="18be4-324">**Filename**</span></span>
  - <span data-ttu-id="18be4-325">**SHA256**</span><span class="sxs-lookup"><span data-stu-id="18be4-325">**SHA256**</span></span>
  - <span data-ttu-id="18be4-326">**Famille de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="18be4-326">**Malware family**</span></span>
  - <span data-ttu-id="18be4-327">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="18be4-327">**Total count**</span></span>

- <span data-ttu-id="18be4-328">**URL**</span><span class="sxs-lookup"><span data-stu-id="18be4-328">**URL**</span></span>

  - <span data-ttu-id="18be4-329">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="18be4-329">**URL**<sup>\*</sup></span></span>
  - <span data-ttu-id="18be4-330">**Nombre total**</span><span class="sxs-lookup"><span data-stu-id="18be4-330">**Total Count**</span></span>

<span data-ttu-id="18be4-331"><sup>\*</sup> Le fait de cliquer sur cette valeur ouvre un nouveau menu mobile qui contient plus de détails sur l’élément spécifié (utilisateur, URL, etc.) au-dessus de la vue Détails de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-331"><sup>\*</sup> Clicking on this value opens a new flyout that contains more details about the specified item (user, URL, etc.) on top of the campaign details view.</span></span> <span data-ttu-id="18be4-332">Pour revenir à la vue Détails de la campagne, cliquez sur **Terminé** dans la nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="18be4-332">To return to the campaign details view, click **Done** in the new flyout.</span></span>

### <a name="buttons"></a><span data-ttu-id="18be4-333">Boutons</span><span class="sxs-lookup"><span data-stu-id="18be4-333">Buttons</span></span>

<span data-ttu-id="18be4-334">Les boutons de la vue Détails de la campagne vous permettent d’utiliser le Power Explorer pour approfondir l’examen de la campagne.</span><span class="sxs-lookup"><span data-stu-id="18be4-334">The buttons in the campaign details view allow you to use the power of Threat Explorer to further investigate the campaign.</span></span>

- <span data-ttu-id="18be4-335">**Explorer la campagne**: ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de la valeur **ID de campagne** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="18be4-335">**Explore campaign**: Opens a new Threat Explorer search tab using the **Campaign ID** value as the search filter.</span></span>

- <span data-ttu-id="18be4-336">**Explorer les messages**de la boîte de réception : ouvre un nouvel onglet de recherche de l’Explorateur de menaces à l’aide de l' **ID de campagne** et de l' **emplacement de remise : boîte de réception** comme filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="18be4-336">**Explore Inboxed messages**: Opens a new Threat Explorer search tab using the **Campaign ID** and **Delivery location: Inbox** as the search filter.</span></span>
