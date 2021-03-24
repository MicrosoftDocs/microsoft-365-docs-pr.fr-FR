---
title: Passer en revue les alertes dans Microsoft Defender pour le point de terminaison
description: Passer en revue les informations d’alerte, y compris un article d’alerte visualisé et des détails pour chaque étape de la chaîne.
keywords: incident, incidents, ordinateurs, appareils, utilisateurs, alertes, alerte, enquête, graphique, preuves
ms.prod: m365-security
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: daniha
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.date: 5/1/2020
ms.technology: mde
ms.openlocfilehash: b791f2b62cb4a3f8062c80ceeb04ccfa72f704bc
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062134"
---
# <a name="review-alerts-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="33828-104">Passer en revue les alertes dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="33828-104">Review alerts in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="33828-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="33828-105">**Applies to:**</span></span>
- [<span data-ttu-id="33828-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="33828-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="33828-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="33828-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="33828-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="33828-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-managealerts-abovefoldlink)

<span data-ttu-id="33828-109">La page d’alerte dans Microsoft Defender pour le point de terminaison fournit un contexte complet à l’alerte, en combinant les signaux d’attaque et les alertes associées à l’alerte sélectionnée, pour créer un article d’alerte détaillé.</span><span class="sxs-lookup"><span data-stu-id="33828-109">The alert page in Microsoft Defender for Endpoint provides full context to the alert, by combining attack signals and alerts related to the selected alert, to construct a detailed alert story.</span></span>

<span data-ttu-id="33828-110">Triez rapidement, examinez et prenez des mesures efficaces sur les alertes qui affectent votre organisation.</span><span class="sxs-lookup"><span data-stu-id="33828-110">Quickly triage, investigate, and take effective action on alerts that affect your organization.</span></span> <span data-ttu-id="33828-111">Comprendre pourquoi ils ont été déclenchés et leur impact à partir d’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="33828-111">Understand why they were triggered, and their impact from one location.</span></span> <span data-ttu-id="33828-112">En savoir plus dans cette vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="33828-112">Learn more in this overview.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yiO5]

## <a name="getting-started-with-an-alert"></a><span data-ttu-id="33828-113">Mise en place d’une alerte</span><span class="sxs-lookup"><span data-stu-id="33828-113">Getting started with an alert</span></span>

<span data-ttu-id="33828-114">Si vous sélectionnez le nom d’une alerte dans Defender pour le point de terminaison, vous serez sur sa page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="33828-114">Selecting an alert's name in Defender for Endpoint will land you on its alert page.</span></span> <span data-ttu-id="33828-115">Sur la page d’alerte, toutes les informations s’afficheront dans le contexte de l’alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="33828-115">On the alert page, all the information will be shown in context of the selected alert.</span></span> <span data-ttu-id="33828-116">Chaque page d’alerte se compose de 4 sections :</span><span class="sxs-lookup"><span data-stu-id="33828-116">Each alert page consists of 4 sections:</span></span>

1. <span data-ttu-id="33828-117">**Le titre de l’alerte** affiche le nom de l’alerte et est là pour vous rappeler quelle alerte a démarré votre enquête en cours, indépendamment de ce que vous avez sélectionné sur la page.</span><span class="sxs-lookup"><span data-stu-id="33828-117">**The alert title** shows the alert's name and is there to remind you which alert started your current investigation regardless of what you have selected on the page.</span></span>
2. <span data-ttu-id="33828-118">[**Les ressources affectées**](#review-affected-assets) répertorient les cartes d’appareils et d’utilisateurs affectés par cette alerte qui peuvent être cliquées pour plus d’informations et d’actions.</span><span class="sxs-lookup"><span data-stu-id="33828-118">[**Affected assets**](#review-affected-assets) lists cards of devices and users affected by this alert that are clickable for further information and actions.</span></span>
3. <span data-ttu-id="33828-119">**L’article d’alerte** affiche toutes les entités liées à l’alerte, interconnectées par une arborescence.</span><span class="sxs-lookup"><span data-stu-id="33828-119">The **alert story** displays all entities related to the alert, interconnected by a tree view.</span></span> <span data-ttu-id="33828-120">L’alerte dans le titre est celle qui est sélectionnée lorsque vous vous pointez pour la première fois sur la page de votre alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="33828-120">The alert in the title will be the one in focus when you first land on your selected alert's page.</span></span> <span data-ttu-id="33828-121">Les entités dans l’article d’alerte sont ex expandables et cliquables, pour fournir des informations supplémentaires et accélérer la réponse en vous permettant d’agir directement dans le contexte de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="33828-121">Entities in the alert story are expandable and clickable, to provide additional information and expedite response by allowing you to take actions right in the context of the alert page.</span></span> <span data-ttu-id="33828-122">Utilisez l’article d’alerte pour lancer votre enquête.</span><span class="sxs-lookup"><span data-stu-id="33828-122">Use the alert story to start your investigation.</span></span> <span data-ttu-id="33828-123">Découvrez comment examiner [les alertes dans Microsoft Defender pour le point de terminaison.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts)</span><span class="sxs-lookup"><span data-stu-id="33828-123">Learn how in [Investigate alerts in Microsoft Defender for Endpoint](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts).</span></span>
4. <span data-ttu-id="33828-124">Le **volet d’informations** affiche d’abord les détails de l’alerte sélectionnée, ainsi que les détails et les actions associés à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="33828-124">The **details pane** will show the details of the selected alert at first, with details and actions related to this alert.</span></span> <span data-ttu-id="33828-125">Si vous sélectionnez l’une des ressources ou entités affectées dans l’article d’alerte, le volet d’informations change pour fournir des informations contextuelles et des actions pour l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="33828-125">If you select any of the affected assets or entities in the alert story, the details pane will change to provide contextual information and actions for the selected object.</span></span>

<span data-ttu-id="33828-126">Notez l’état de détection de votre alerte.</span><span class="sxs-lookup"><span data-stu-id="33828-126">Note the detection status for your alert.</span></span> 
- <span data-ttu-id="33828-127">Interdit : la tentative d’action suspecte a été évitée.</span><span class="sxs-lookup"><span data-stu-id="33828-127">Prevented – The attempted suspicious action was avoided.</span></span> <span data-ttu-id="33828-128">Par exemple, un fichier n’a pas été écrit sur le disque ou exécuté.</span><span class="sxs-lookup"><span data-stu-id="33828-128">For example, a file either wasn’t written to disk or executed.</span></span>
<span data-ttu-id="33828-129">![Page d’alerte indiquant que la menace a été empêchée](images/detstat-prevented.png)</span><span class="sxs-lookup"><span data-stu-id="33828-129">![An alert page showing threat was prevented](images/detstat-prevented.png)</span></span>
- <span data-ttu-id="33828-130">Bloqué : un comportement suspect a été exécuté, puis bloqué.</span><span class="sxs-lookup"><span data-stu-id="33828-130">Blocked – Suspicious behavior was executed and then blocked.</span></span> <span data-ttu-id="33828-131">Par exemple, un processus a été exécuté, mais comme il a par la suite présenté des comportements suspects, le processus a été interrompu.</span><span class="sxs-lookup"><span data-stu-id="33828-131">For example, a process was executed but because it subsequently exhibited suspicious behaviors, the process was terminated.</span></span>
<span data-ttu-id="33828-132">![Page d’alerte indiquant que la menace a été bloquée](images/detstat-blocked.png)</span><span class="sxs-lookup"><span data-stu-id="33828-132">![An alert page showing threat was blocked](images/detstat-blocked.png)</span></span>
- <span data-ttu-id="33828-133">Détecté : une attaque a été détectée et est éventuellement toujours active.</span><span class="sxs-lookup"><span data-stu-id="33828-133">Detected – An attack was detected and is possibly still active.</span></span>
<span data-ttu-id="33828-134">![Page d’alerte indiquant que la menace a été détectée](images/detstat-detected.png)</span><span class="sxs-lookup"><span data-stu-id="33828-134">![An alert page showing threat was detected](images/detstat-detected.png)</span></span>




<span data-ttu-id="33828-135">Vous pouvez ensuite consulter les *détails* de l’enquête automatisée dans le volet d’informations de votre alerte pour voir quelles actions ont déjà été entreprises, ainsi que lire la description de l’alerte pour les actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="33828-135">You can then also review the *automated investigation details* in your alert's details pane, to see which actions were already taken, as well as reading the alert's description for recommended actions.</span></span>

![Extrait du volet d’informations avec la description de l’alerte et les sections d’examen automatique mises en évidence](images/alert-air-and-alert-description.png)

<span data-ttu-id="33828-137">Les autres informations disponibles dans le volet d’informations à l’ouverture de l’alerte incluent les techniques MITRE, la source et des détails contextuels supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="33828-137">Other information available in the details pane when the alert opens includes MITRE techniques, source, and additional contextual details.</span></span>




## <a name="review-affected-assets"></a><span data-ttu-id="33828-138">Passer en revue les biens affectés</span><span class="sxs-lookup"><span data-stu-id="33828-138">Review affected assets</span></span>

<span data-ttu-id="33828-139">La sélection d’un appareil ou d’une carte utilisateur dans les sections ressources affectées bascule vers les détails de l’appareil ou de l’utilisateur dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="33828-139">Selecting a device or a user card in the affected assets sections will switch to the details of the device or user in the details pane.</span></span>

- <span data-ttu-id="33828-140">**Pour les appareils,** le volet d’informations affiche des informations sur l’appareil lui-même, comme domaine, système d’exploitation et IP.</span><span class="sxs-lookup"><span data-stu-id="33828-140">**For devices**, the details pane will display information about the device itself, like Domain, Operating System, and IP.</span></span> <span data-ttu-id="33828-141">Les alertes actives et les utilisateurs connectés sur cet appareil sont également disponibles.</span><span class="sxs-lookup"><span data-stu-id="33828-141">Active alerts and the logged on users on that device are also available.</span></span> <span data-ttu-id="33828-142">Vous pouvez prendre des mesures immédiates en isolant l’appareil, en limitant l’exécution de l’application ou en exécutant une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="33828-142">You can take immediate action by isolating the device, restricting app execution, or running an antivirus scan.</span></span> <span data-ttu-id="33828-143">Vous pouvez également collecter un package d’enquête, lancer une enquête automatisée ou vous rendre sur la page de l’appareil pour l’examiner du point de vue de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33828-143">Alternatively, you could collect an investigation package, initiate an automated investigation, or go to the device page to investigate from the device's point of view.</span></span>

   ![Extrait du volet d’informations lorsqu’un appareil est sélectionné](images/device-page-details.png)

- <span data-ttu-id="33828-145">Pour les utilisateurs, le volet d’informations affiche des informations détaillées sur l’utilisateur, telles que le nom SAM et le SID de l’utilisateur, ainsi que les types d’accès effectués par cet utilisateur, ainsi que les alertes et incidents qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="33828-145">**For users**, the details pane will display detailed user information, such as the user's SAM name and SID, as well as logon types performed by this user and any alerts and incidents related to it.</span></span> <span data-ttu-id="33828-146">Vous pouvez sélectionner *Ouvrir la page utilisateur pour* poursuivre l’examen du point de vue de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="33828-146">You can select *Open user page* to continue the investigation from that user's point of view.</span></span>

   ![Extrait du volet d’informations lorsqu’un utilisateur est sélectionné](images/user-page-details.png)


## <a name="related-topics"></a><span data-ttu-id="33828-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33828-148">Related topics</span></span>

- [<span data-ttu-id="33828-149">Afficher et organiser la file d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="33828-149">View and organize the incidents queue</span></span>](view-incidents-queue.md)
- [<span data-ttu-id="33828-150">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="33828-150">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="33828-151">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="33828-151">Manage incidents</span></span>](manage-incidents.md)
