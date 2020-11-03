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
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous découvrirez les rapports et les outils de dépannage disponibles pour les administrateurs de Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 9a8eb8e35ef73eb27604eef4bf701982b1d51710
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48845551"
---
# <a name="reporting-and-message-trace-in-eop"></a><span data-ttu-id="13c40-103">Création de rapports et suivi des messages dans EOP</span><span class="sxs-lookup"><span data-stu-id="13c40-103">Reporting and message trace in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="13c40-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, EOP offre un grand nombre de rapports qui peuvent vous aider à déterminer l’état général et l’intégrité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="13c40-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="13c40-105">Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité.</span><span class="sxs-lookup"><span data-stu-id="13c40-105">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span>

## <a name="usage-reports"></a><span data-ttu-id="13c40-106">Rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="13c40-106">Usage reports</span></span>

<span data-ttu-id="13c40-107">**Activité des groupes microsoft 365** : afficher des informations sur le nombre de groupes Microsoft 365 créés et utilisés.</span><span class="sxs-lookup"><span data-stu-id="13c40-107">**Microsoft 365 groups activity** : View information about the number of Microsoft 365 groups that are created and used.</span></span>

<span data-ttu-id="13c40-108">**Activité de messagerie** : afficher des informations sur le nombre de messages envoyés, reçus et lus dans l’ensemble de votre organisation, ainsi que sur des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="13c40-108">**Email activity** : View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>

<span data-ttu-id="13c40-109">**Utilisation** des applications de messagerie : Affichez des informations sur les applications de messagerie utilisées.</span><span class="sxs-lookup"><span data-stu-id="13c40-109">**Email app usage** : View information about the email apps that are used.</span></span> <span data-ttu-id="13c40-110">Ceci inclut le nombre total de connexions pour chaque application et les versions de Outlook qui se connectent.</span><span class="sxs-lookup"><span data-stu-id="13c40-110">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>

<span data-ttu-id="13c40-111">**Utilisation des boîtes aux lettres** : afficher des informations sur l’espace de stockage utilisé, la consommation de quota, le nombre d’éléments et la dernière activité (activité d’envoi ou de lecture) pour les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="13c40-111">**Mailbox usage** : View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="13c40-112">Pour plus d'informations, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="13c40-112">See the following resources for more information:</span></span>

- [<span data-ttu-id="13c40-113">Rapports Microsoft 365 dans le centre d’administration-groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="13c40-113">Microsoft 365 Reports in the admin center - Microsoft 365 groups</span></span>](https://docs.microsoft.com/microsoft-365/admin/activity-reports/office-365-groups)

- [<span data-ttu-id="13c40-114">Rapports Microsoft 365 dans le centre d’administration-activité de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="13c40-114">Microsoft 365 Reports in the admin center - Email activity</span></span>](https://docs.microsoft.com/microsoft-365/admin/activity-reports/email-activity)

- [<span data-ttu-id="13c40-115">Rapports Microsoft 365 dans le centre d’administration-utilisation des applications de messagerie</span><span class="sxs-lookup"><span data-stu-id="13c40-115">Microsoft 365 Reports in the admin center - Email apps usage</span></span>](https://docs.microsoft.com/microsoft-365/admin/activity-reports/email-apps-usage)

- [<span data-ttu-id="13c40-116">Rapports Microsoft 365 dans le centre d’administration-utilisation des boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="13c40-116">Microsoft 365 Reports in the admin center - Mailbox usage</span></span>](https://docs.microsoft.com/microsoft-365/admin/activity-reports/mailbox-usage)

## <a name="security--compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="13c40-117">Sécurité & des rapports de conformité dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="13c40-117">Security & compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="13c40-118">Ces rapports améliorés fournissent une expérience de création de rapports interactive pour les administrateurs EOP, qui inclut des informations récapitulatives et la possibilité d’approfondir plus en détail.</span><span class="sxs-lookup"><span data-stu-id="13c40-118">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>

<span data-ttu-id="13c40-119">**Defender pour office 365** : Affichez des informations sur les liens fiables et les pièces jointes fiables qui font partie de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="13c40-119">**Defender for Office 365** : View information about Safe Links and Safe Attachments that are part of Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="13c40-120">**EOP** : Affichez des informations sur les détections de programmes malveillants, le courrier falsifié, les détections de courrier indésirable et le flux de messagerie vers et depuis votre organisation.</span><span class="sxs-lookup"><span data-stu-id="13c40-120">**EOP** : View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>

[<span data-ttu-id="13c40-121">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="13c40-121">View reports for Defender for Office 365</span></span>](view-reports-for-atp.md)

## <a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="13c40-122">Rapports personnalisés à l’aide de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="13c40-122">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="13c40-123">Créez par programme des rapports disponibles dans le centre d’administration à l’aide de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="13c40-123">Programmatically create reports that are available in the admin center by using Microsoft Graph.</span></span> <span data-ttu-id="13c40-124">Pour plus d’informations, reportez-vous à la rubrique [vue d’ensemble de Microsoft Graph](https://docs.microsoft.com/graph/overview) et [utilisation des rapports d’utilisation d’Office 365 dans Microsoft Graph](https://docs.microsoft.com/graph/api/resources/report).</span><span class="sxs-lookup"><span data-stu-id="13c40-124">For more information, see [Overview of Microsoft Graph](https://docs.microsoft.com/graph/overview) and [Working with Office 365 usage reports in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/report).</span></span>

## <a name="message-trace"></a><span data-ttu-id="13c40-125">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="13c40-125">Message trace</span></span>

<span data-ttu-id="13c40-126">Suit les messages électroniques pendant qu'ils circulent dans EOP.</span><span class="sxs-lookup"><span data-stu-id="13c40-126">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="13c40-127">Vous pouvez déterminer si un message électronique a été reçu, rejeté, différé ou remis par le service.</span><span class="sxs-lookup"><span data-stu-id="13c40-127">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="13c40-128">Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.</span><span class="sxs-lookup"><span data-stu-id="13c40-128">It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="13c40-129">Vous pouvez ainsi répondre efficacement aux questions de vos utilisateurs, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie, tout en réduisant la nécessité de demander de l'aide à l'assistance technique.</span><span class="sxs-lookup"><span data-stu-id="13c40-129">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>

<span data-ttu-id="13c40-130">Consultez [la rubrique suivi des messages dans le centre de sécurité & conformité](message-trace-scc.md).</span><span class="sxs-lookup"><span data-stu-id="13c40-130">See [Message trace in the Security & Compliance Center](message-trace-scc.md).</span></span>

## <a name="audit-logging"></a><span data-ttu-id="13c40-131">Journalisation d'audit</span><span class="sxs-lookup"><span data-stu-id="13c40-131">Audit logging</span></span>

<span data-ttu-id="13c40-132">Effectue le suivi des modifications spécifiques apportées par les administrateurs à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="13c40-132">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="13c40-133">Ces rapports peuvent vous aider à résoudre les problèmes de configuration ou à trouver la cause des problèmes de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="13c40-133">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span> <span data-ttu-id="13c40-134">Consultez la rubrique [Auditing reports in EOP](auditing-reports-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="13c40-134">See [Auditing reports in EOP](auditing-reports-in-eop.md).</span></span>

## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="13c40-135">Disponibilité et latence des rapports et des données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="13c40-135">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="13c40-136">Le tableau suivant présente la disponibilité des rapports et des données de suivi des messages EOP, ainsi que leur latence.</span><span class="sxs-lookup"><span data-stu-id="13c40-136">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>

****

|<span data-ttu-id="13c40-137">Type de rapport</span><span class="sxs-lookup"><span data-stu-id="13c40-137">Report type</span></span>|<span data-ttu-id="13c40-138">Données disponibles pendant (période rétrospective)</span><span class="sxs-lookup"><span data-stu-id="13c40-138">Data available for (look back period)</span></span>|<span data-ttu-id="13c40-139">Latence</span><span class="sxs-lookup"><span data-stu-id="13c40-139">Latency</span></span>|
|---|---|---|
|<span data-ttu-id="13c40-140">Rapports de synthèse de la protection de la messagerie</span><span class="sxs-lookup"><span data-stu-id="13c40-140">Mail protection summary reports</span></span>|<span data-ttu-id="13c40-141">90 jours</span><span class="sxs-lookup"><span data-stu-id="13c40-141">90 days</span></span>|<span data-ttu-id="13c40-p106">L'agrégation quasi-complète des données des messages dure entre 24 et 48 heures. Des modifications agrégées incrémentielles mineures peuvent se produire jusqu'à 5 jours.</span><span class="sxs-lookup"><span data-stu-id="13c40-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>|
|<span data-ttu-id="13c40-144">Rapports détaillés de la protection de messagerie</span><span class="sxs-lookup"><span data-stu-id="13c40-144">Mail protection detail reports</span></span>|<span data-ttu-id="13c40-145">90 jours</span><span class="sxs-lookup"><span data-stu-id="13c40-145">90 days</span></span>|<span data-ttu-id="13c40-p107">Pour les messages de moins de 7 jours, les données détaillées apparaissent normalement dans les 24 heures, mais leur génération peut durer jusqu'à 48 heures. Il est possible que des modifications incrémentielles mineures soient apportées pendant 5 jours.</span><span class="sxs-lookup"><span data-stu-id="13c40-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span> <br/><br/> <span data-ttu-id="13c40-148">Pour les messages remontant à plus de sept jours, la génération des résultats détaillés peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="13c40-148">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|<span data-ttu-id="13c40-149">Données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="13c40-149">Message trace data</span></span>|<span data-ttu-id="13c40-150">90 jours</span><span class="sxs-lookup"><span data-stu-id="13c40-150">90 days</span></span>|<span data-ttu-id="13c40-151">Lorsque vous effectuez un suivi de messages remontant à moins de 7 jours, ces derniers apparaissent normalement dans les 5 à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="13c40-151">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span><br/><br/> <span data-ttu-id="13c40-152">Lorsque vous effectuez un suivi de messages remontant à plus de 7 jours, la génération des résultats peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="13c40-152">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|

> [!NOTE]
> <span data-ttu-id="13c40-153">La disponibilité et la latence des données sont les mêmes, qu’elles soient demandées via le centre d’administration ou PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="13c40-153">Data availability and latency is the same whether requested via the admin center or remote PowerShell.</span></span>
