---
title: Création de rapports et suivi des messages
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez découvrir les rapports et les outils de dépannage disponibles pour les administrateurs Microsoft Exchange Online Protection des données (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ae55ded9d907754161813c9f7bfa7eeb14c558a8
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52625028"
---
# <a name="reporting-and-message-trace-in-eop"></a><span data-ttu-id="1240e-103">Rapports et suivi des messages dans EOP</span><span class="sxs-lookup"><span data-stu-id="1240e-103">Reporting and message trace in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1240e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1240e-104">**Applies to**</span></span>
- [<span data-ttu-id="1240e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="1240e-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="1240e-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="1240e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="1240e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1240e-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="1240e-108">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, EOP propose de nombreux rapports différents qui peuvent vous aider à déterminer l’état général et l’état de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1240e-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="1240e-109">Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité.</span><span class="sxs-lookup"><span data-stu-id="1240e-109">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span>

## <a name="usage-reports"></a><span data-ttu-id="1240e-110">Rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="1240e-110">Usage reports</span></span>

<span data-ttu-id="1240e-111">**Microsoft 365 groupes :** afficher des informations sur le nombre de groupes Microsoft 365 créés et utilisés.</span><span class="sxs-lookup"><span data-stu-id="1240e-111">**Microsoft 365 groups activity**: View information about the number of Microsoft 365 groups that are created and used.</span></span>

<span data-ttu-id="1240e-112">**Activité de messagerie**: afficher des informations sur le nombre de messages envoyés, reçus et lus dans toute votre organisation, et par des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1240e-112">**Email activity**: View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>

<span data-ttu-id="1240e-113">**Utilisation de l’application de messagerie**: afficher des informations sur les applications de messagerie utilisées.</span><span class="sxs-lookup"><span data-stu-id="1240e-113">**Email app usage**: View information about the email apps that are used.</span></span> <span data-ttu-id="1240e-114">Ceci inclut le nombre total de connexions pour chaque application et les versions de Outlook qui se connectent.</span><span class="sxs-lookup"><span data-stu-id="1240e-114">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>

<span data-ttu-id="1240e-115">**Utilisation des boîtes aux** lettres : afficher les informations sur le stockage utilisé, la consommation de quota, le nombre d’éléments et la dernière activité (activité d’envoi ou de lecture) pour les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1240e-115">**Mailbox usage**: View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="1240e-116">Pour plus d'informations, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="1240e-116">See the following resources for more information:</span></span>

- [<span data-ttu-id="1240e-117">Microsoft 365 Rapports dans le Centre d’administration : Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="1240e-117">Microsoft 365 Reports in the admin center - Microsoft 365 groups</span></span>](../../admin/activity-reports/office-365-groups.md)

- [<span data-ttu-id="1240e-118">Microsoft 365 Rapports dans le Centre d’administration - Activité de messagerie</span><span class="sxs-lookup"><span data-stu-id="1240e-118">Microsoft 365 Reports in the admin center - Email activity</span></span>](../../admin/activity-reports/email-activity.md)

- [<span data-ttu-id="1240e-119">Microsoft 365 Rapports dans le Centre d’administration - Utilisation des applications de messagerie</span><span class="sxs-lookup"><span data-stu-id="1240e-119">Microsoft 365 Reports in the admin center - Email apps usage</span></span>](../../admin/activity-reports/email-apps-usage.md)

- [<span data-ttu-id="1240e-120">Microsoft 365 Rapports dans le Centre d’administration - Utilisation des boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="1240e-120">Microsoft 365 Reports in the admin center - Mailbox usage</span></span>](../../admin/activity-reports/mailbox-usage.md)

## <a name="security--compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="1240e-121">Rapports de conformité & sécurité dans le Centre d’administration Microsoft 365 de sécurité</span><span class="sxs-lookup"><span data-stu-id="1240e-121">Security & compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="1240e-122">Ces rapports améliorés offrent une expérience de rapport interactive pour les administrateurs EOP, qui inclut des informations récapitulatifs et la possibilité d’obtenir plus de détails.</span><span class="sxs-lookup"><span data-stu-id="1240e-122">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>

<span data-ttu-id="1240e-123">**Defender pour Office 365**: afficher des informations sur les liens sécurisés et les pièces jointes sécurisées qui font partie de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="1240e-123">**Defender for Office 365**: View information about Safe Links and Safe Attachments that are part of Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="1240e-124">**EOP**: afficher des informations sur les détections de programmes malveillants, les messages usurpés, les détections de courrier indésirable et le flux de messagerie vers et depuis votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1240e-124">**EOP**: View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>

[<span data-ttu-id="1240e-125">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1240e-125">View reports for Defender for Office 365</span></span>](view-reports-for-mdo.md)

## <a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="1240e-126">Rapports personnalisés à l’aide de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="1240e-126">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="1240e-127">Créez par programme des rapports disponibles dans le Centre d’administration à l’aide de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="1240e-127">Programmatically create reports that are available in the admin center by using Microsoft Graph.</span></span> <span data-ttu-id="1240e-128">Pour plus d’informations, voir [Vue d’ensemble](/graph/overview) de Microsoft Graph et utilisation des rapports [Office 365'utilisation dans Microsoft Graph](/graph/api/resources/report).</span><span class="sxs-lookup"><span data-stu-id="1240e-128">For more information, see [Overview of Microsoft Graph](/graph/overview) and [Working with Office 365 usage reports in Microsoft Graph](/graph/api/resources/report).</span></span>

## <a name="message-trace"></a><span data-ttu-id="1240e-129">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="1240e-129">Message trace</span></span>

<span data-ttu-id="1240e-130">Suit les messages électroniques pendant qu'ils circulent dans EOP.</span><span class="sxs-lookup"><span data-stu-id="1240e-130">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="1240e-131">Vous pouvez déterminer si un message électronique a été reçu, rejeté, différé ou remis par le service.</span><span class="sxs-lookup"><span data-stu-id="1240e-131">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="1240e-132">Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.</span><span class="sxs-lookup"><span data-stu-id="1240e-132">It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="1240e-133">Vous pouvez ainsi répondre efficacement aux questions de vos utilisateurs, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie, tout en réduisant la nécessité de demander de l'aide à l'assistance technique.</span><span class="sxs-lookup"><span data-stu-id="1240e-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>

<span data-ttu-id="1240e-134">Voir [suivi des messages dans le Centre de sécurité & conformité.](message-trace-scc.md)</span><span class="sxs-lookup"><span data-stu-id="1240e-134">See [Message trace in the Security & Compliance Center](message-trace-scc.md).</span></span>

## <a name="audit-logging"></a><span data-ttu-id="1240e-135">Journalisation d'audit</span><span class="sxs-lookup"><span data-stu-id="1240e-135">Audit logging</span></span>

<span data-ttu-id="1240e-136">Effectue le suivi des modifications spécifiques apportées par les administrateurs à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1240e-136">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="1240e-137">Ces rapports peuvent vous aider à résoudre les problèmes de configuration ou à trouver la cause des problèmes de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="1240e-137">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span> <span data-ttu-id="1240e-138">Consultez [les rapports d’audit dans Exchange Online](/exchange/security-and-compliance/exchange-auditing-reports/exchange-auditing-reports).</span><span class="sxs-lookup"><span data-stu-id="1240e-138">See [Auditing reports in Exchange Online](/exchange/security-and-compliance/exchange-auditing-reports/exchange-auditing-reports).</span></span>

## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="1240e-139">Disponibilité et latence des rapports et des données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="1240e-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="1240e-140">Le tableau suivant présente la disponibilité des rapports et des données de suivi des messages EOP, ainsi que leur latence.</span><span class="sxs-lookup"><span data-stu-id="1240e-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>

****

|<span data-ttu-id="1240e-141">Type de rapport</span><span class="sxs-lookup"><span data-stu-id="1240e-141">Report type</span></span>|<span data-ttu-id="1240e-142">Données disponibles pendant (période rétrospective)</span><span class="sxs-lookup"><span data-stu-id="1240e-142">Data available for (look back period)</span></span>|<span data-ttu-id="1240e-143">Latence</span><span class="sxs-lookup"><span data-stu-id="1240e-143">Latency</span></span>|
|---|---|---|
|<span data-ttu-id="1240e-144">Rapports récapitulatifs sur la protection du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="1240e-144">Mail protection summary reports</span></span>|<span data-ttu-id="1240e-145">90 jours</span><span class="sxs-lookup"><span data-stu-id="1240e-145">90 days</span></span>|<span data-ttu-id="1240e-p106">L'agrégation quasi-complète des données des messages dure entre 24 et 48 heures. Des modifications agrégées incrémentielles mineures peuvent se produire jusqu'à 5 jours.</span><span class="sxs-lookup"><span data-stu-id="1240e-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>|
|<span data-ttu-id="1240e-148">Rapports détaillés sur la protection du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="1240e-148">Mail protection detail reports</span></span>|<span data-ttu-id="1240e-149">90 jours</span><span class="sxs-lookup"><span data-stu-id="1240e-149">90 days</span></span>|<span data-ttu-id="1240e-p107">Pour les messages de moins de 7 jours, les données détaillées apparaissent normalement dans les 24 heures, mais leur génération peut durer jusqu'à 48 heures. Il est possible que des modifications incrémentielles mineures soient apportées pendant 5 jours.</span><span class="sxs-lookup"><span data-stu-id="1240e-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span> <p> <span data-ttu-id="1240e-152">Pour les messages remontant à plus de sept jours, la génération des résultats détaillés peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="1240e-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|<span data-ttu-id="1240e-153">Données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="1240e-153">Message trace data</span></span>|<span data-ttu-id="1240e-154">90 jours</span><span class="sxs-lookup"><span data-stu-id="1240e-154">90 days</span></span>|<span data-ttu-id="1240e-155">Lorsque vous effectuez un suivi de messages remontant à moins de 7 jours, ces derniers apparaissent normalement dans les 5 à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="1240e-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span><p> <span data-ttu-id="1240e-156">Lorsque vous effectuez un suivi de messages remontant à plus de 7 jours, la génération des résultats peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="1240e-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|

> [!NOTE]
> <span data-ttu-id="1240e-157">La disponibilité et la latence des données sont les mêmes, qu’elles soient demandées via le Centre d’administration ou PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="1240e-157">Data availability and latency is the same whether requested via the admin center or remote PowerShell.</span></span>