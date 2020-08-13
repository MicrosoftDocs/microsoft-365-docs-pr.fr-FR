---
title: Table EmailPostDeliveryEvents dans le schéma de chasse avancé
description: En savoir plus sur les actions postérieures à la livraison effectuées sur les courriers électroniques Microsoft 365 dans le tableau EmailPostDeliveryEvents du schéma de chasse avancé
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, EmailPostDeliveryEvents, ID de message réseau, expéditeur, destinataire, ID pièce jointe, nom de la pièce jointe, nombre d’URL
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 0384f3ba07b42c8e783994dfa1db75cf2d6ca80b
ms.sourcegitcommit: 51097b18d94da20aa727ebfbeb6ec84c263b25c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46648862"
---
# <a name="emailpostdeliveryevents"></a><span data-ttu-id="6a930-104">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="6a930-104">EmailPostDeliveryEvents</span></span>

<span data-ttu-id="6a930-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6a930-105">**Applies to:**</span></span>
- <span data-ttu-id="6a930-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="6a930-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="6a930-107">Le `EmailPostDeliveryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les actions postérieures à la livraison effectuées sur les messages électroniques traités par Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6a930-107">The `EmailPostDeliveryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about post-delivery actions taken on email messages processed by Microsoft 365.</span></span> <span data-ttu-id="6a930-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="6a930-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="6a930-109">Pour obtenir plus d’informations sur les messages électroniques individuels, vous pouvez également utiliser les [`EmailEvents`](advanced-hunting-emailevents-table.md) [`EmailAttachmentInfo`](advanced-hunting-emailattachmentinfo-table.md) tables, et [`EmailUrlInfo`](advanced-hunting-emailurlinfo-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6a930-109">To get more information about individual email messages, you can also use the [`EmailEvents`](advanced-hunting-emailevents-table.md), [`EmailAttachmentInfo`](advanced-hunting-emailattachmentinfo-table.md), and the [`EmailUrlInfo`](advanced-hunting-emailurlinfo-table.md) tables.</span></span> <span data-ttu-id="6a930-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6a930-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="6a930-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="6a930-111">Column name</span></span> | <span data-ttu-id="6a930-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a930-112">Data type</span></span> | <span data-ttu-id="6a930-113">Description</span><span class="sxs-lookup"><span data-stu-id="6a930-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="6a930-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="6a930-114">datetime</span></span> | <span data-ttu-id="6a930-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="6a930-115">Date and time when the event was recorded</span></span> |
| `EventId` | <span data-ttu-id="6a930-116">string</span><span class="sxs-lookup"><span data-stu-id="6a930-116">string</span></span> | <span data-ttu-id="6a930-117">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="6a930-117">Unique identifier for the event</span></span> |
| `NetworkMessageId` | <span data-ttu-id="6a930-118">string</span><span class="sxs-lookup"><span data-stu-id="6a930-118">string</span></span> | <span data-ttu-id="6a930-119">Identificateur unique pour le courrier électronique, généré par Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6a930-119">Unique identifier for the email, generated by Microsoft 365</span></span> |
| `InternetMessageId` | <span data-ttu-id="6a930-120">chaîne</span><span class="sxs-lookup"><span data-stu-id="6a930-120">string</span></span> | <span data-ttu-id="6a930-121">Identificateur public de l’e-mail défini par le système de courrier d’envoi</span><span class="sxs-lookup"><span data-stu-id="6a930-121">Public-facing identifier for the email that is set by the sending email system</span></span> |
| `Action` | <span data-ttu-id="6a930-122">chaîne</span><span class="sxs-lookup"><span data-stu-id="6a930-122">string</span></span> | <span data-ttu-id="6a930-123">Action effectuée sur l’entité</span><span class="sxs-lookup"><span data-stu-id="6a930-123">Action taken on the entity</span></span> |
| `ActionType` | <span data-ttu-id="6a930-124">string</span><span class="sxs-lookup"><span data-stu-id="6a930-124">string</span></span> | <span data-ttu-id="6a930-125">Type d’activité qui a déclenché l’événement : correction manuelle, hameçonnage ZAP, programme malveillant ZAP</span><span class="sxs-lookup"><span data-stu-id="6a930-125">Type of activity that triggered the event: Manual remediation, Phish ZAP, Malware ZAP</span></span> |
| `ActionTrigger` | <span data-ttu-id="6a930-126">string</span><span class="sxs-lookup"><span data-stu-id="6a930-126">string</span></span> | <span data-ttu-id="6a930-127">Indique si une action a été déclenchée par un administrateur (manuellement ou par l’approbation d’une action automatisée en attente) ou par un mécanisme spécial, tel qu’un ZAP ou une remise dynamique.</span><span class="sxs-lookup"><span data-stu-id="6a930-127">Indicates whether an action was triggered by an administrator (manually or through approval of a pending automated action), or by some special mechanism, such as a ZAP or Dynamic Delivery</span></span> |
| `ActionResult` | <span data-ttu-id="6a930-128">string</span><span class="sxs-lookup"><span data-stu-id="6a930-128">string</span></span> | <span data-ttu-id="6a930-129">Résultat de l’action</span><span class="sxs-lookup"><span data-stu-id="6a930-129">Result of the action</span></span> |
| `RecipientEmailAddress` | <span data-ttu-id="6a930-130">string</span><span class="sxs-lookup"><span data-stu-id="6a930-130">string</span></span> | <span data-ttu-id="6a930-131">Adresse e-mail du destinataire ou adresse e-mail du destinataire après extension de la liste de distribution</span><span class="sxs-lookup"><span data-stu-id="6a930-131">Email address of the recipient, or email address of the recipient after distribution list expansion</span></span> |
| `DeliveryLocation` | <span data-ttu-id="6a930-132">chaîne</span><span class="sxs-lookup"><span data-stu-id="6a930-132">string</span></span> | <span data-ttu-id="6a930-133">Emplacement de remise du courrier électronique : boîte de réception/dossier, local/externe, courrier indésirable, quarantaine, échec, supprimé, éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="6a930-133">Location where the email was delivered: Inbox/Folder, On-premises/External, Junk, Quarantine, Failed, Dropped, Deleted items</span></span> |

## <a name="supported-event-types"></a><span data-ttu-id="6a930-134">Types d’événements pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a930-134">Supported event types</span></span>
<span data-ttu-id="6a930-135">Cette table capture les événements avec les `ActionType` valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a930-135">This table captures events with the following `ActionType` values:</span></span>

- <span data-ttu-id="6a930-136">**Correction manuelle** : un administrateur a effectué manuellement une action sur un message électronique une fois qu’il a été remis à la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a930-136">**Manual remediation** – An administrator manually took action on an email message after it was delivered to the user mailbox.</span></span> <span data-ttu-id="6a930-137">Cela inclut les actions effectuées manuellement via l' [Explorateur de menaces](../office-365-security/threat-explorer.md) ou les approbations d' [actions d’enquête et de réponse (air) automatisées](mtp-autoir-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6a930-137">This includes actions taken manually through [Threat Explorer](../office-365-security/threat-explorer.md) or approvals of [automated investigation and response (AIR) actions](mtp-autoir-actions.md).</span></span>
- <span data-ttu-id="6a930-138">**Hameçonnage zap** – [purge automatique avec zéro heure (ZAP)](../office-365-security/zero-hour-auto-purge.md) a effectué une action sur un e-mail de hameçonnage après la remise.</span><span class="sxs-lookup"><span data-stu-id="6a930-138">**Phish ZAP** – [Zero-hour auto purge (ZAP)](../office-365-security/zero-hour-auto-purge.md) took action on a phishing email after delivery.</span></span>
- <span data-ttu-id="6a930-139">**Programme malveillant zap** – la purge automatique à zéro heure (ZAP) a effectué une action sur un message électronique contenant un programme malveillant après la remise.</span><span class="sxs-lookup"><span data-stu-id="6a930-139">**Malware ZAP** – Zero-hour auto purge (ZAP) took action on an email message found containing malware after delivery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a930-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a930-140">Related topics</span></span>
- [<span data-ttu-id="6a930-141">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="6a930-141">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="6a930-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="6a930-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="6a930-143">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="6a930-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="6a930-144">Recherche sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="6a930-144">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="6a930-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="6a930-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="6a930-146">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="6a930-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)