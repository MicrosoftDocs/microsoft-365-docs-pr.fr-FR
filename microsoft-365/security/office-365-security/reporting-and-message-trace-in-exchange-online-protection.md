---
title: Création de rapports et suivi des messages dans Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 12/18/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft Exchange Online Protection (EOP) offre un grand nombre de rapports qui peuvent vous aider à déterminer l'état général de votre organisation. Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité. Le tableau suivant décrit les rapports et les outils de dépannage disponibles pour les administrateurs EOP.
ms.openlocfilehash: 39ac70c401cb4a630b95fab89fe3a145495c29eb
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078407"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="0c21e-105">Création de rapports et suivi des messages dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0c21e-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="0c21e-106">Microsoft Exchange Online Protection (EOP) offre un grand nombre de rapports qui peuvent vous aider à déterminer l'état général de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c21e-106">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="0c21e-107">Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité.</span><span class="sxs-lookup"><span data-stu-id="0c21e-107">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span>

## <a name="usage-reports"></a><span data-ttu-id="0c21e-108">Rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="0c21e-108">Usage reports</span></span>

<span data-ttu-id="0c21e-109">**Activité des groupes office 365**: afficher des informations sur le nombre de groupes Office 365 créés et utilisés.</span><span class="sxs-lookup"><span data-stu-id="0c21e-109">**Office 365 groups activity**: View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="0c21e-110">**Activité de messagerie**: afficher des informations sur le nombre de messages envoyés, reçus et lus dans l’ensemble de votre organisation, ainsi que sur des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0c21e-110">**Email activity**: View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="0c21e-111">**Utilisation**des applications de messagerie : Affichez des informations sur les applications de messagerie utilisées.</span><span class="sxs-lookup"><span data-stu-id="0c21e-111">**Email app usage**: View information about the email apps that are used.</span></span> <span data-ttu-id="0c21e-112">Ceci inclut le nombre total de connexions pour chaque application et les versions de Outlook qui se connectent.</span><span class="sxs-lookup"><span data-stu-id="0c21e-112">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="0c21e-113">**Utilisation des boîtes aux lettres**: afficher des informations sur l’espace de stockage utilisé, la consommation de quota, le nombre d’éléments et la dernière activité (activité d’envoi ou de lecture) pour les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c21e-113">**Mailbox usage**: View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="0c21e-114">Pour plus d'informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c21e-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="0c21e-115">Rapports Office 365 dans le centre d’administration-groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="0c21e-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610)

- [<span data-ttu-id="0c21e-116">Rapports Office 365 dans le Centre d'administration - Activité du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="0c21e-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706)

- [<span data-ttu-id="0c21e-117">Rapports Office 365 dans le Centre d'administration - Utilisation des applications de messagerie</span><span class="sxs-lookup"><span data-stu-id="0c21e-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)

- [<span data-ttu-id="0c21e-118">Rapports Office 365 dans le Centre d'administration - Utilisation des boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="0c21e-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security--compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0c21e-119">Sécurité & des rapports de conformité dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0c21e-119">Security & compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0c21e-120">Ces rapports améliorés fournissent une expérience de création de rapports interactive pour les administrateurs EOP, qui inclut des informations récapitulatives et la possibilité d’approfondir plus en détail.</span><span class="sxs-lookup"><span data-stu-id="0c21e-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="0c21e-121">**Protection avancée contre les menaces (ATP)**: Affichez des informations sur les liens fiables et les pièces jointes fiables qui font partie de l’ATP.</span><span class="sxs-lookup"><span data-stu-id="0c21e-121">**Advanced Threat Protection (ATP)**: View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="0c21e-122">**EOP**: Affichez des informations sur les détections de programmes malveillants, le courrier falsifié, les détections de courrier indésirable et le flux de messagerie vers et depuis votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c21e-122">**EOP**: View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="0c21e-123">Afficher les rapports de protection avancée contre les menaces et Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0c21e-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409)

## <a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="0c21e-124">Rapports personnalisés à l’aide de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="0c21e-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="0c21e-125">Créer par programme des rapports qui sont disponibles dans le centre d’administration Microsoft 365 à l’aide de Microsoft Graph, consultez les sous-rubriques relatives à l’utilisation des [rapports d’utilisation d’Office 365 dans Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span><span class="sxs-lookup"><span data-stu-id="0c21e-125">Programmatically create reports that are available in the Microsoft 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span>

## <a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="0c21e-126">Rapports personnalisés à l’aide des services web de rapport</span><span class="sxs-lookup"><span data-stu-id="0c21e-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="0c21e-127">Créer par programme des rapports à partir des applets de commande Exchange Online Protection PowerShell disponibles à l’aide du filtrage des requêtes REST/ODATA2.</span><span class="sxs-lookup"><span data-stu-id="0c21e-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="0c21e-128">Voir les [services Web de création de rapports Office 365](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span><span class="sxs-lookup"><span data-stu-id="0c21e-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span>

## <a name="message-trace"></a><span data-ttu-id="0c21e-129">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="0c21e-129">Message trace</span></span>

<span data-ttu-id="0c21e-130">Suit les messages électroniques pendant qu'ils circulent dans EOP.</span><span class="sxs-lookup"><span data-stu-id="0c21e-130">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="0c21e-131">Vous pouvez déterminer si un message électronique a été reçu, rejeté, différé ou remis par le service.</span><span class="sxs-lookup"><span data-stu-id="0c21e-131">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="0c21e-132">Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.</span><span class="sxs-lookup"><span data-stu-id="0c21e-132">It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="0c21e-133">Vous pouvez ainsi répondre efficacement aux questions de vos utilisateurs, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie, tout en réduisant la nécessité de demander de l'aide à l'assistance technique.</span><span class="sxs-lookup"><span data-stu-id="0c21e-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="0c21e-134">Voir [suivi d’un message électronique](https://docs.microsoft.com/exchange/monitoring/trace-an-email-message/trace-an-email-message)</span><span class="sxs-lookup"><span data-stu-id="0c21e-134">See [Trace an email message](https://docs.microsoft.com/exchange/monitoring/trace-an-email-message/trace-an-email-message)</span></span>

## <a name="audit-logging"></a><span data-ttu-id="0c21e-135">Journalisation d'audit</span><span class="sxs-lookup"><span data-stu-id="0c21e-135">Audit logging</span></span>

<span data-ttu-id="0c21e-136">Effectue le suivi des modifications spécifiques apportées par les administrateurs à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c21e-136">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="0c21e-137">Ces rapports peuvent vous aider à résoudre les problèmes de configuration ou à trouver la cause des problèmes de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="0c21e-137">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span> <span data-ttu-id="0c21e-138">Consultez la rubrique [Auditing reports in EOP](auditing-reports-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="0c21e-138">See [Auditing reports in EOP](auditing-reports-in-eop.md).</span></span>

## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="0c21e-139">Disponibilité et latence des rapports et des données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="0c21e-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="0c21e-140">Le tableau suivant présente la disponibilité des rapports et des données de suivi des messages EOP, ainsi que leur latence.</span><span class="sxs-lookup"><span data-stu-id="0c21e-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="0c21e-141">**Type de rapport**</span><span class="sxs-lookup"><span data-stu-id="0c21e-141">**Report type**</span></span>|<span data-ttu-id="0c21e-142">**Données disponibles pendant (période rétrospective)**</span><span class="sxs-lookup"><span data-stu-id="0c21e-142">**Data available for (look back period)**</span></span>|<span data-ttu-id="0c21e-143">**Latence**</span><span class="sxs-lookup"><span data-stu-id="0c21e-143">**Latency**</span></span>|
|<span data-ttu-id="0c21e-144">Rapports de synthèse de la protection de la messagerie</span><span class="sxs-lookup"><span data-stu-id="0c21e-144">Mail protection summary reports</span></span>|<span data-ttu-id="0c21e-145">90 jours</span><span class="sxs-lookup"><span data-stu-id="0c21e-145">90 days</span></span>|<span data-ttu-id="0c21e-p106">L'agrégation quasi-complète des données des messages dure entre 24 et 48 heures. Des modifications agrégées incrémentielles mineures peuvent se produire jusqu'à 5 jours.</span><span class="sxs-lookup"><span data-stu-id="0c21e-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>|
|<span data-ttu-id="0c21e-148">Rapports détaillés de la protection de messagerie</span><span class="sxs-lookup"><span data-stu-id="0c21e-148">Mail protection detail reports</span></span>|<span data-ttu-id="0c21e-149">90 jours</span><span class="sxs-lookup"><span data-stu-id="0c21e-149">90 days</span></span>|<span data-ttu-id="0c21e-p107">Pour les messages de moins de 7 jours, les données détaillées apparaissent normalement dans les 24 heures, mais leur génération peut durer jusqu'à 48 heures. Il est possible que des modifications incrémentielles mineures soient apportées pendant 5 jours.</span><span class="sxs-lookup"><span data-stu-id="0c21e-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span> <br/><br/> <span data-ttu-id="0c21e-152">Pour les messages remontant à plus de sept jours, la génération des résultats détaillés peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="0c21e-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|
|<span data-ttu-id="0c21e-153">Données de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="0c21e-153">Message trace data</span></span>|<span data-ttu-id="0c21e-154">90 jours</span><span class="sxs-lookup"><span data-stu-id="0c21e-154">90 days</span></span>|<span data-ttu-id="0c21e-155">Lorsque vous effectuez un suivi de messages remontant à moins de 7 jours, ces derniers apparaissent normalement dans les 5 à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="0c21e-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span><br/><br/> <span data-ttu-id="0c21e-156">Lorsque vous effectuez un suivi de messages remontant à plus de 7 jours, la génération des résultats peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="0c21e-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>|

> [!NOTE]
> <span data-ttu-id="0c21e-157">La disponibilité et la latence des données sont les mêmes, qu’elles soient demandées via le centre d’administration Microsoft 365 ou PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="0c21e-157">Data availability and latency is the same whether requested via the Microsoft 365 admin center or remote PowerShell.</span></span> 
