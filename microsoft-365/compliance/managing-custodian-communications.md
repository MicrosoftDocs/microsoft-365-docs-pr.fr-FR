---
title: Travailler avec les communications dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Advanced eDiscovery facilite la gestion du flux de travail de notification de conservation légale autour de la notification aux dépositaires dans les enquêtes juridiques.
ms.openlocfilehash: 28b719a83cbc1608ad5468e401a8b7946cb8da5f
ms.sourcegitcommit: bd51f626f0c7788c2a3cf89deee25264659aebd5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "43551238"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a><span data-ttu-id="d7f0b-103">Travailler avec les communications dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d7f0b-103">Work with communications in Advanced eDiscovery</span></span>

<span data-ttu-id="d7f0b-104">Advanced eDiscovery permet aux services juridiques de simplifier leurs processus de suivi et de distribution des notifications de mise en attente légale.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-104">Advanced eDiscovery allows legal departments to simplify their processes around tracking and distributing legal hold notifications.</span></span> <span data-ttu-id="d7f0b-105">L’outil de communication du dépositaire permet aux services juridiques de gérer et d’automatiser l’ensemble du processus de conservation légale, des notifications initiales aux rappels et aux escalades, le tout dans un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-105">The custodian communications tool enables legal departments to manage and automate the entire legal hold process, from initial notifications, to reminders, and to escalations, all in one location.</span></span>

## <a name="what-is-a-legal-hold-notification"></a><span data-ttu-id="d7f0b-106">Qu’est-ce qu’une notification de mise en attente légale ?</span><span class="sxs-lookup"><span data-stu-id="d7f0b-106">What is a legal hold notification?</span></span>

<span data-ttu-id="d7f0b-107">Une notification de conservation légale (également appelée mise en attente pour *litige)* est une notification envoyée par le service juridique d’une organisation aux employés, au personnel subordonné ou aux dépositaires des données qui peuvent être pertinentes pour une enquête juridique.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-107">A legal hold (also known as a *litigation hold*) notice is a notification sent from an organization’s legal department to employees, contingent staff, or custodians of data that may be relevant to a legal investigation.</span></span> <span data-ttu-id="d7f0b-108">Ces notifications indiquent aux dépositaires de conserver les informations stockées électroniquement, ainsi que tout contenu qui peut être pertinent pour une affaire juridique active ou imminente.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-108">These notifications instruct custodians to preserve electronically stored information as well as any content that may be relevant to an active or impending legal matter.</span></span> <span data-ttu-id="d7f0b-109">Les équipes juridiques doivent savoir que chaque dépositaire a reçu, lu, compris et a accepté de se conformer aux instructions données.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-109">Legal teams must know that each custodian has received, read, understood, and has agreed to comply with the given instructions.</span></span>

## <a name="the-legal-hold-notification-process"></a><span data-ttu-id="d7f0b-110">Processus de notification de mise en attente légale</span><span class="sxs-lookup"><span data-stu-id="d7f0b-110">The legal hold notification process</span></span>

<span data-ttu-id="d7f0b-111">Une organisation a l’obligation de conserver les informations pertinentes lorsqu’elle apprend un litige ou une enquête réglementaire.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-111">An organization has a duty to preserve relevant information when it learns about an impending litigation or regulatory investigation.</span></span> <span data-ttu-id="d7f0b-112">Pour se conformer aux exigences de conservation d’un examen, l’organisation doit immédiatement informer les dépositaires potentiels de leur obligation de conserver les informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-112">To comply with the preservation requirements of an investigation, the organization should immediately inform potential custodians about their duty to preserve relevant information.</span></span>

<span data-ttu-id="d7f0b-113">Avec Advanced eDiscovery, les équipes juridiques peuvent créer et personnaliser leur flux de travail de notification de mise en attente légale.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-113">With Advanced eDiscovery, legal teams can create and customize their legal hold notification workflow.</span></span> <span data-ttu-id="d7f0b-114">L’outil de communication du dépositaire permet aux équipes juridiques de configurer les notifications et les flux de travail suivants :</span><span class="sxs-lookup"><span data-stu-id="d7f0b-114">The custodian communications tool lets legal teams to configure the following notices and workflows:</span></span>

1. <span data-ttu-id="d7f0b-115">**Avis d’émission :** Une notification de conservation légale est émise (ou initiée) par une notification du service juridique aux dépositaires qui peuvent avoir des informations pertinentes sur le cas.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-115">**Issuance notice:** A legal hold notice is issued (or initiated) by a notification from the legal department to custodians who may have relevant information about the case matter.</span></span> <span data-ttu-id="d7f0b-116">Cet avis enjoint aux consignataires de conserver les informations qui peuvent être nécessaires à la découverte.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-116">This notice instructs the custodians to preserve any information that may be needed for discovery.</span></span>

2. <span data-ttu-id="d7f0b-117">**Avis de ré-émission :** Dans un cas, les dépositaires peuvent être tenus de conserver du contenu supplémentaire (ou moins de contenu) que ce qui a été demandé précédemment.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-117">**Re-Issuance notice:** During a case, custodians may be required to preserve additional content (or less content) than was previously requested.</span></span> <span data-ttu-id="d7f0b-118">Pour ce scénario, vous pouvez mettre à jour l’avis de conservation existant et le ré-émettre aux dépositaires.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-118">For this scenario, you can update the existing hold notice and re-issue it to custodians.</span></span>

3. <span data-ttu-id="d7f0b-119">**Avis de publication :** Une fois qu’un problème est résolu et que le dépositaire n’est plus soumis à une obligation de conservation, le dépositaire peut être libéré du cas.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-119">**Release notice:** Once a matter is resolved and the custodian is no longer subject to a preservation requirement, the custodian can be released from the case.</span></span> <span data-ttu-id="d7f0b-120">En outre, vous pouvez informer le dépositaire qu’il n’est plus tenu de conserver le contenu et fournir des instructions sur la façon de reprendre son activité de travail normale en ce qui concerne ses données.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-120">Additionally, you can notify the custodian that they are no longer required to preserve content, and provide instructions about how to resume their normal work activity with regard to their data.</span></span>

4. <span data-ttu-id="d7f0b-121">**Rappels et escalades :** Dans certains cas, la simple émission d’un avis ne suffit pas pour satisfaire aux exigences de découverte légale.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-121">**Reminders and escalations:** In some instances, just issuing a notice isn't enough to satisfy legal discovery requirements.</span></span> <span data-ttu-id="d7f0b-122">Avec chaque notification, les équipes juridiques peuvent planifier un ensemble de flux de rappels et de notifications d’escalade pour assurer automatiquement le suivi du consignataire non réactifs.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-122">With each notification, legal teams can schedule a set of reminder and escalation workflows to automatically follow up with unresponsive custodians.</span></span>

   - <span data-ttu-id="d7f0b-123">**Rappels :** Une fois qu’une notification de conservation légale a été émise ou ré-émise à un ensemble de dépositaires, une organisation peut configurer des rappels pour alerter les dépositaires qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-123">**Reminders:** After a legal hold notice has been issued or re-issued to a set of custodians, an organization can set up reminders to alert unresponsive custodians.</span></span>

   - <span data-ttu-id="d7f0b-124">**Escalades :** Dans certains cas, si un dépositaire ne répond pas même après un ensemble de rappels sur une période de temps, l’équipe juridique peut configurer un flux de travail d’escalade pour avertir les dépositaires qui ne répond pas et leur responsable.</span><span class="sxs-lookup"><span data-stu-id="d7f0b-124">**Escalations:** In some cases, if a custodian remains unresponsive even after a set of reminders over a period of time, the legal team can set up an escalation workflow to notify unresponsive custodians and their manager.</span></span>

<span data-ttu-id="d7f0b-125">Pour plus d’informations sur la gestion du processus de communication des dépositaires, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7f0b-125">For more information about managing the custodian communication process, see the following:</span></span> 

- [<span data-ttu-id="d7f0b-126">Créer une notification de non-droit</span><span class="sxs-lookup"><span data-stu-id="d7f0b-126">Create a legal hold notice</span></span>](create-hold-notification.md)

- [<span data-ttu-id="d7f0b-127">Utiliser l’éditeur de communications</span><span class="sxs-lookup"><span data-stu-id="d7f0b-127">Use the communications editor</span></span>](using-communications-editor.md)

- [<span data-ttu-id="d7f0b-128">Gérer les notifications de conservation</span><span class="sxs-lookup"><span data-stu-id="d7f0b-128">Manage hold notifications</span></span>](manage-hold-notification.md)

- [<span data-ttu-id="d7f0b-129">Reconnaitre une notification de conservation</span><span class="sxs-lookup"><span data-stu-id="d7f0b-129">Acknowledge a hold notification</span></span>](acknowledge-hold-notification.md)