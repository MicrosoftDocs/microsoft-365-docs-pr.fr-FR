---
title: Table EmailPostDeliveryEvents dans le schéma de recherche avancé
description: En savoir plus sur les actions de post-remise prises sur les e-mails Microsoft 365 dans la table EmailPostDeliveryEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, EmailPostDeliveryEvents, network message id, sender, recipient, attachment id, attachment id, attachment name, malware verdict, phishing verdict, attachment count, link count, url count
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 8940d1dd370f804f8539bf4e753b1112d3c8d3bf
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51198196"
---
# <a name="emailpostdeliveryevents"></a><span data-ttu-id="c42cb-104">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="c42cb-104">EmailPostDeliveryEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c42cb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c42cb-105">**Applies to:**</span></span>
- <span data-ttu-id="c42cb-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c42cb-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="c42cb-107">Le tableau du schéma de recherche avancée contient des informations sur les actions de post-remise prises sur les messages électroniques traitées `EmailPostDeliveryEvents` par Microsoft [](advanced-hunting-overview.md) 365.</span><span class="sxs-lookup"><span data-stu-id="c42cb-107">The `EmailPostDeliveryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about post-delivery actions taken on email messages processed by Microsoft 365.</span></span> <span data-ttu-id="c42cb-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="c42cb-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="c42cb-109">Pour plus d’informations sur les types d’événements (valeurs) pris en charge par une table, utilisez la référence de schéma intégrée disponible `ActionType` dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c42cb-109">For detailed information about the events types (`ActionType` values) supported by a table, use the built-in schema reference available in the security center.</span></span>

<span data-ttu-id="c42cb-110">Pour obtenir plus d’informations sur les messages électroniques individuels, vous pouvez également utiliser les tableaux , et les [`EmailEvents`](advanced-hunting-emailevents-table.md) [`EmailAttachmentInfo`](advanced-hunting-emailattachmentinfo-table.md) [`EmailUrlInfo`](advanced-hunting-emailurlinfo-table.md) tableaux.</span><span class="sxs-lookup"><span data-stu-id="c42cb-110">To get more information about individual email messages, you can also use the [`EmailEvents`](advanced-hunting-emailevents-table.md), [`EmailAttachmentInfo`](advanced-hunting-emailattachmentinfo-table.md), and the [`EmailUrlInfo`](advanced-hunting-emailurlinfo-table.md) tables.</span></span> <span data-ttu-id="c42cb-111">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c42cb-111">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="c42cb-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c42cb-112">Column name</span></span> | <span data-ttu-id="c42cb-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="c42cb-113">Data type</span></span> | <span data-ttu-id="c42cb-114">Description</span><span class="sxs-lookup"><span data-stu-id="c42cb-114">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="c42cb-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c42cb-115">datetime</span></span> | <span data-ttu-id="c42cb-116">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="c42cb-116">Date and time when the event was recorded</span></span> |
| `NetworkMessageId` | <span data-ttu-id="c42cb-117">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-117">string</span></span> | <span data-ttu-id="c42cb-118">Identificateur unique de l’e-mail, généré par Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c42cb-118">Unique identifier for the email, generated by Microsoft 365</span></span> |
| `InternetMessageId` | <span data-ttu-id="c42cb-119">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-119">string</span></span> | <span data-ttu-id="c42cb-120">Identificateur public de l’e-mail défini par le système de courrier d’envoi</span><span class="sxs-lookup"><span data-stu-id="c42cb-120">Public-facing identifier for the email that is set by the sending email system</span></span> |
| `Action` | <span data-ttu-id="c42cb-121">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-121">string</span></span> | <span data-ttu-id="c42cb-122">Action entreprise sur l’entité</span><span class="sxs-lookup"><span data-stu-id="c42cb-122">Action taken on the entity</span></span> |
| `ActionType` | <span data-ttu-id="c42cb-123">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-123">string</span></span> | <span data-ttu-id="c42cb-124">Type d’activité qui a déclenché l’événement : correction manuelle, HAMEÇON ZAP, PROGRAMME MALVEILLANT ZAP</span><span class="sxs-lookup"><span data-stu-id="c42cb-124">Type of activity that triggered the event: Manual remediation, Phish ZAP, Malware ZAP</span></span> |
| `ActionTrigger` | <span data-ttu-id="c42cb-125">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-125">string</span></span> | <span data-ttu-id="c42cb-126">Indique si une action a été déclenchée par un administrateur (manuellement ou par le biais de l’approbation d’une action automatisée en attente) ou par un mécanisme spécial, tel qu’une ZAP ou une remise dynamique</span><span class="sxs-lookup"><span data-stu-id="c42cb-126">Indicates whether an action was triggered by an administrator (manually or through approval of a pending automated action), or by some special mechanism, such as a ZAP or Dynamic Delivery</span></span> |
| `ActionResult` | <span data-ttu-id="c42cb-127">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-127">string</span></span> | <span data-ttu-id="c42cb-128">Résultat de l’action</span><span class="sxs-lookup"><span data-stu-id="c42cb-128">Result of the action</span></span> |
| `RecipientEmailAddress` | <span data-ttu-id="c42cb-129">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-129">string</span></span> | <span data-ttu-id="c42cb-130">Adresse e-mail du destinataire ou adresse e-mail du destinataire après extension de la liste de distribution</span><span class="sxs-lookup"><span data-stu-id="c42cb-130">Email address of the recipient, or email address of the recipient after distribution list expansion</span></span> |
| `DeliveryLocation` | <span data-ttu-id="c42cb-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="c42cb-131">string</span></span> | <span data-ttu-id="c42cb-132">Emplacement de remise du courrier électronique : boîte de réception/dossier, local/externe, courrier indésirable, quarantaine, échec, supprimé, éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="c42cb-132">Location where the email was delivered: Inbox/Folder, On-premises/External, Junk, Quarantine, Failed, Dropped, Deleted items</span></span> |
| `ReportId` | <span data-ttu-id="c42cb-133">long</span><span class="sxs-lookup"><span data-stu-id="c42cb-133">long</span></span> | <span data-ttu-id="c42cb-134">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="c42cb-134">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="c42cb-135">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp.</span><span class="sxs-lookup"><span data-stu-id="c42cb-135">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns.</span></span> |

## <a name="supported-event-types"></a><span data-ttu-id="c42cb-136">Types d’événements pris en charge</span><span class="sxs-lookup"><span data-stu-id="c42cb-136">Supported event types</span></span>
<span data-ttu-id="c42cb-137">Ce tableau capture les événements avec les valeurs `ActionType` suivantes :</span><span class="sxs-lookup"><span data-stu-id="c42cb-137">This table captures events with the following `ActionType` values:</span></span>

- <span data-ttu-id="c42cb-138">**Correction manuelle** : un administrateur a manuellement pris des mesures sur un message électronique après sa remise à la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c42cb-138">**Manual remediation** – An administrator manually took action on an email message after it was delivered to the user mailbox.</span></span> <span data-ttu-id="c42cb-139">Cela inclut les actions entreprises manuellement via [l’Explorateur](../office-365-security/threat-explorer.md) de menaces ou les approbations d’actions d’investigation et de [réponse automatisées (AIR).](m365d-autoir-actions.md)</span><span class="sxs-lookup"><span data-stu-id="c42cb-139">This includes actions taken manually through [Threat Explorer](../office-365-security/threat-explorer.md) or approvals of [automated investigation and response (AIR) actions](m365d-autoir-actions.md).</span></span>
- <span data-ttu-id="c42cb-140">**ZAP d’hameçonnage** : la purge automatique d’heure zéro [(ZAP)](../office-365-security/zero-hour-auto-purge.md) a pris des mesures sur un e-mail de hameçonnage après la remise.</span><span class="sxs-lookup"><span data-stu-id="c42cb-140">**Phish ZAP** – [Zero-hour auto purge (ZAP)](../office-365-security/zero-hour-auto-purge.md) took action on a phishing email after delivery.</span></span>
- <span data-ttu-id="c42cb-141">**ZAP anti-programme** malveillant : la purge automatique d’heure zéro (ZAP) a pris des mesures sur un message électronique détecté contenant un programme malveillant après la remise.</span><span class="sxs-lookup"><span data-stu-id="c42cb-141">**Malware ZAP** – Zero-hour auto purge (ZAP) took action on an email message found containing malware after delivery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c42cb-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c42cb-142">Related topics</span></span>
- [<span data-ttu-id="c42cb-143">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c42cb-143">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c42cb-144">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c42cb-144">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c42cb-145">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="c42cb-145">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="c42cb-146">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="c42cb-146">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="c42cb-147">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c42cb-147">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="c42cb-148">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="c42cb-148">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
