---
title: Création de rapports et suivi des messages dans Exchange Online Protection
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous découvrirez les rapports et les outils de dépannage disponibles pour les administrateurs de Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 44b4223b4310a2de1d90f99f8a7af23cc6054f94
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034379"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="33ab6-103">Création de rapports et suivi des messages dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="33ab6-103">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="33ab6-104">Microsoft Exchange Online Protection (EOP) offre un grand nombre de rapports qui peuvent vous aider à déterminer l'état général de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="33ab6-104">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="33ab6-105">Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité.</span><span class="sxs-lookup"><span data-stu-id="33ab6-105">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span>

## <a name="usage-reports"></a><span data-ttu-id="33ab6-106">Rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="33ab6-106">Usage reports</span></span>

<span data-ttu-id="33ab6-107">**Activité des groupes microsoft 365**: afficher des informations sur le nombre de groupes Microsoft 365 créés et utilisés.</span><span class="sxs-lookup"><span data-stu-id="33ab6-107">**Microsoft 365 groups activity**: View information about the number of Microsoft 365 groups that are created and used.</span></span>

<span data-ttu-id="33ab6-108">**Activité de messagerie**: afficher des informations sur le nombre de messages envoyés, reçus et lus dans l’ensemble de votre organisation, ainsi que sur des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="33ab6-108">**Email activity**: View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>

<span data-ttu-id="33ab6-109">**Utilisation**des applications de messagerie : Affichez des informations sur les applications de messagerie utilisées.</span><span class="sxs-lookup"><span data-stu-id="33ab6-109">**Email app usage**: View information about the email apps that are used.</span></span> <span data-ttu-id="33ab6-110">Ceci inclut le nombre total de connexions pour chaque application et les versions de Outlook qui se connectent.</span><span class="sxs-lookup"><span data-stu-id="33ab6-110">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>

<span data-ttu-id="33ab6-111">**Utilisation des boîtes aux lettres**: afficher des informations sur l’espace de stockage utilisé, la consommation de quota, le nombre d’éléments et la dernière activité (activité d’envoi ou de lecture) pour les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="33ab6-111">**Mailbox usage**: View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="33ab6-112">Pour plus d'informations, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="33ab6-112">See the following resources for more information:</span></span>

- [<span data-ttu-id="33ab6-113">Rapports Microsoft 365 dans le centre d’administration-groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="33ab6-113">Microsoft 365 Reports in the admin center - Microsoft 365 groups</span></span>](https://docs.microsoft.com/office365/admin/activity-reports/office-365-groups)

- [<span data-ttu-id="33ab6-114">Rapports Microsoft 365 dans le centre d’administration-activité de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="33ab6-114">Microsoft 365 Reports in the Admin Center - Email activity</span></span>](https://docs.microsoft.com/office365/admin/activity-reports/email-activity)

- [<span data-ttu-id="33ab6-115">Rapports Microsoft 365 dans le centre d’administration-utilisation des applications de messagerie</span><span class="sxs-lookup"><span data-stu-id="33ab6-115">Microsoft 365 Reports in the Admin Center - Email apps usage</span></span>](https://docs.microsoft.com/office365/admin/activity-reports/email-apps-usage)

- [<span data-ttu-id="33ab6-116">Rapports Microsoft 365 dans le centre d’administration-utilisation des boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="33ab6-116">Microsoft 365 Reports in the Admin Center - Mailbox usage</span></span>](https://docs.microsoft.com/office365/admin/activity-reports/mailbox-usage)

## <a name="security--compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="33ab6-117">Sécurité & des rapports de conformité dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="33ab6-117">Security & compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="33ab6-118">Ces rapports améliorés fournissent une expérience de création de rapports interactive pour les administrateurs EOP, qui inclut des informations récapitulatives et la possibilité d’approfondir plus en détail.</span><span class="sxs-lookup"><span data-stu-id="33ab6-118">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>

<span data-ttu-id="33ab6-119">**Protection avancée contre les menaces (ATP)**: Affichez des informations sur les liens fiables et les pièces jointes fiables qui font partie de l’ATP.</span><span class="sxs-lookup"><span data-stu-id="33ab6-119">**Advanced Threat Protection (ATP)**: View information about safe links and safe attachments that are part of ATP.</span></span>

<span data-ttu-id="33ab6-120">**EOP**: Affichez des informations sur les détections de programmes malveillants, le courrier falsifié, les détections de courrier indésirable et le flux de messagerie vers et depuis votre organisation.</span><span class="sxs-lookup"><span data-stu-id="33ab6-120">**EOP**: View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>

[<span data-ttu-id="33ab6-121">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="33ab6-121">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

## <a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="33ab6-122">Rapports personnalisés à l’aide de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="33ab6-122">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="33ab6-123">Créez par programme des rapports qui sont disponibles dans le centre d’administration Microsoft 365 à l’aide de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="33ab6-123">Programmatically create reports that are available in the Microsoft 365 admin center by using Microsoft Graph.</span></span> <span data-ttu-id="33ab6-124">Voir les sous-rubriques relatives [à l’utilisation des rapports d’utilisation Office 365 dans Microsoft Graph](https://docs.microsoft.com/graph/api/resources/report).</span><span class="sxs-lookup"><span data-stu-id="33ab6-124">See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/report).</span></span>

## <a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="33ab6-125">Rapports personnalisés à l’aide de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="33ab6-125">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="33ab6-126">Créer des rapports par programme.</span><span class="sxs-lookup"><span data-stu-id="33ab6-126">Programmatically create reports.</span></span> <span data-ttu-id="33ab6-127">Voir [vue d’ensemble de Microsoft Graph](https://docs.microsoft.com/graph/overview).</span><span class="sxs-lookup"><span data-stu-id="33ab6-127">See [Overview of Microsoft Graph](https://docs.microsoft.com/graph/overview).</span></span>

## <a name="message-trace"></a><span data-ttu-id="33ab6-128">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="33ab6-128">Message trace</span></span>

<span data-ttu-id="33ab6-129">Suit les messages électroniques pendant qu'ils circulent dans EOP.</span><span class="sxs-lookup"><span data-stu-id="33ab6-129">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="33ab6-130">Vous pouvez déterminer si un message électronique a été reçu, rejeté, différé ou remis par le service.</span><span class="sxs-lookup"><span data-stu-id="33ab6-130">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="33ab6-131">Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.</span><span class="sxs-lookup"><span data-stu-id="33ab6-131">It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="33ab6-132">Vous pouvez ainsi répondre efficacement aux questions de vos utilisateurs, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie, tout en réduisant la nécessité de demander de l'aide à l'assistance technique.</span><span class="sxs-lookup"><span data-stu-id="33ab6-132">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>

<span data-ttu-id="33ab6-133">Voir [suivi d’un message électronique](https://docs.microsoft.com/exchange/monitoring/trace-an-email-message/trace-an-email-message)</span><span class="sxs-lookup"><span data-stu-id="33ab6-133">See [Trace an email message](https://docs.microsoft.com/exchange/monitoring/trace-an-email-message/trace-an-email-message)</span></span>

## <a name="audit-logging"></a><span data-ttu-id="33ab6-134">Journalisation d'audit</span><span class="sxs-lookup"><span data-stu-id="33ab6-134">Audit logging</span></span>

<span data-ttu-id="33ab6-135">Effectue le suivi des modifications spécifiques apportées par les administrateurs à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="33ab6-135">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="33ab6-136">Ces rapports peuvent vous aider à résoudre les problèmes de configuration ou à trouver la cause des problèmes de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="33ab6-136">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span> <span data-ttu-id="33ab6-137">Consultez la rubrique [Auditing reports in EOP](auditing-reports-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="33ab6-137">See [Auditing reports in EOP](auditing-reports-in-eop.md).</span></span>

## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="33ab6-138">Disponibilité et latence des rapports et des données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="33ab6-138">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="33ab6-139">Le tableau suivant présente la disponibilité des rapports et des données de suivi des messages EOP, ainsi que leur latence.</span><span class="sxs-lookup"><span data-stu-id="33ab6-139">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="33ab6-140">**Type de rapport**</span><span class="sxs-lookup"><span data-stu-id="33ab6-140">**Report type**</span></span>|<span data-ttu-id="33ab6-141">**Données disponibles pendant (période rétrospective)**</span><span class="sxs-lookup"><span data-stu-id="33ab6-141">**Data available for (look back period)**</span></span>|<span data-ttu-id="33ab6-142">**Latence**</span><span class="sxs-lookup"><span data-stu-id="33ab6-142">**Latency**</span></span>|
|<span data-ttu-id="33ab6-143">Rapports de synthèse de la protection de la messagerie</span><span class="sxs-lookup"><span data-stu-id="33ab6-143">Mail protection summary reports</span></span>|<span data-ttu-id="33ab6-144">90 jours</span><span class="sxs-lookup"><span data-stu-id="33ab6-144">90 days</span></span>|<span data-ttu-id="33ab6-p107">L'agrégation quasi-complète des données des messages dure entre 24 et 48 heures. Des modifications agrégées incrémentielles mineures peuvent se produire jusqu'à 5 jours.</span><span class="sxs-lookup"><span data-stu-id="33ab6-p107">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>|
|<span data-ttu-id="33ab6-147">Rapports détaillés de la protection de messagerie</span><span class="sxs-lookup"><span data-stu-id="33ab6-147">Mail protection detail reports</span></span>|<span data-ttu-id="33ab6-148">90 jours</span><span class="sxs-lookup"><span data-stu-id="33ab6-148">90 days</span></span>|<span data-ttu-id="33ab6-p108">Pour les messages de moins de 7 jours, les données détaillées apparaissent normalement dans les 24 heures, mais leur génération peut durer jusqu'à 48 heures. Il est possible que des modifications incrémentielles mineures soient apportées pendant 5 jours.</span><span class="sxs-lookup"><span data-stu-id="33ab6-p108">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span> <br/><br/> <span data-ttu-id="33ab6-151">Pour les messages remontant à plus de sept jours, la génération des résultats détaillés peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="33ab6-151">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|<span data-ttu-id="33ab6-152">Données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="33ab6-152">Message trace data</span></span>|<span data-ttu-id="33ab6-153">90 jours</span><span class="sxs-lookup"><span data-stu-id="33ab6-153">90 days</span></span>|<span data-ttu-id="33ab6-154">Lorsque vous effectuez un suivi de messages remontant à moins de 7 jours, ces derniers apparaissent normalement dans les 5 à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="33ab6-154">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span><br/><br/> <span data-ttu-id="33ab6-155">Lorsque vous effectuez un suivi de messages remontant à plus de 7 jours, la génération des résultats peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="33ab6-155">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|

> [!NOTE]
> <span data-ttu-id="33ab6-156">La disponibilité et la latence des données sont les mêmes, qu’elles soient demandées via le centre d’administration Microsoft 365 ou PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="33ab6-156">Data availability and latency is the same whether requested via the Microsoft 365 admin center or remote PowerShell.</span></span>
