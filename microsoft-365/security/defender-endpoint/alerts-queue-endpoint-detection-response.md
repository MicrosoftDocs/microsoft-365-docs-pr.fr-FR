---
title: File d’attente des alertes dans Centre de sécurité Microsoft Defender
ms.reviewer: ''
description: Afficher et gérer les alertes sur le Centre de sécurité Microsoft Defender
keywords: ''
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.date: 09/03/2018
ms.technology: mde
ms.openlocfilehash: d40fc887f26dfe62e05f7ee6ac7bbbb8ac45a402
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067401"
---
# <a name="alerts-queue-in-microsoft-defender-security-center"></a><span data-ttu-id="bf439-103">File d’attente des alertes dans Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="bf439-103">Alerts queue in Microsoft Defender Security Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="bf439-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bf439-104">**Applies to:**</span></span>
- [<span data-ttu-id="bf439-105">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf439-105">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

> <span data-ttu-id="bf439-106">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="bf439-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="bf439-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bf439-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="bf439-108">Découvrez comment afficher et gérer la file d’attente afin de pouvoir enquêter efficacement sur les menaces visibles sur des entités telles que des appareils, des fichiers ou des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf439-108">Learn how you can view and manage the queue so that you can effectively investigate threats seen on entities such as devices, files, or user accounts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf439-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bf439-109">In this section</span></span>
<span data-ttu-id="bf439-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bf439-110">Topic</span></span> | <span data-ttu-id="bf439-111">Description</span><span class="sxs-lookup"><span data-stu-id="bf439-111">Description</span></span> 
:---|:---
[<span data-ttu-id="bf439-112">Afficher et organiser la file d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="bf439-112">View and organize the Alerts queue</span></span>](alerts-queue.md) | <span data-ttu-id="bf439-113">Affiche la liste des alertes qui ont été signalées dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="bf439-113">Shows a list of alerts that were flagged in your network.</span></span>
[<span data-ttu-id="bf439-114">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="bf439-114">Manage alerts</span></span>](manage-alerts.md) | <span data-ttu-id="bf439-115">Découvrez comment gérer des alertes telles que modifier son état, l’affecter à un membre des opérations de sécurité et consulter l’historique d’une alerte.</span><span class="sxs-lookup"><span data-stu-id="bf439-115">Learn about how you can manage alerts such as change its status, assign it to a security operations member, and see the history of an alert.</span></span>
[<span data-ttu-id="bf439-116">Examiner des alertes</span><span class="sxs-lookup"><span data-stu-id="bf439-116">Investigate alerts</span></span>](investigate-alerts.md)| <span data-ttu-id="bf439-117">Examinez les alertes qui affectent votre réseau, comprenez ce qu’elles signifient et comment les résoudre.</span><span class="sxs-lookup"><span data-stu-id="bf439-117">Investigate alerts that are affecting your network, understand what they mean, and how to resolve them.</span></span>
[<span data-ttu-id="bf439-118">Examiner des fichiers</span><span class="sxs-lookup"><span data-stu-id="bf439-118">Investigate files</span></span>](investigate-files.md)| <span data-ttu-id="bf439-119">Examinez les détails d’un fichier associé à une alerte, un comportement ou un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf439-119">Investigate the details of a file associated with a specific alert, behavior, or event.</span></span> 
[<span data-ttu-id="bf439-120">Examiner des appareils</span><span class="sxs-lookup"><span data-stu-id="bf439-120">Investigate devices</span></span>](investigate-machines.md)| <span data-ttu-id="bf439-121">Examinez les détails d’un appareil associé à une alerte, un comportement ou un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf439-121">Investigate the details of a device associated with a specific alert, behavior, or event.</span></span> 
[<span data-ttu-id="bf439-122">Examiner une adresse IP</span><span class="sxs-lookup"><span data-stu-id="bf439-122">Investigate an IP address</span></span>](investigate-ip.md) | <span data-ttu-id="bf439-123">Examinez les communications possibles entre les appareils de votre réseau et les adresses IP externes.</span><span class="sxs-lookup"><span data-stu-id="bf439-123">Examine possible communication between devices in your network and external internet protocol (IP) addresses.</span></span>
[<span data-ttu-id="bf439-124">Examiner un domaine</span><span class="sxs-lookup"><span data-stu-id="bf439-124">Investigate a domain</span></span>](investigate-domain.md) | <span data-ttu-id="bf439-125">Examinez un domaine pour voir si les appareils et les serveurs de votre réseau communiquent avec un domaine malveillant connu.</span><span class="sxs-lookup"><span data-stu-id="bf439-125">Investigate a domain to see if devices and servers in your network have been communicating with a known malicious domain.</span></span> 
[<span data-ttu-id="bf439-126">Examiner un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bf439-126">Investigate a user account</span></span>](investigate-user.md) | <span data-ttu-id="bf439-127">Identifiez les comptes d’utilisateurs avec les alertes les plus actives et examinez les cas d’informations d’identification potentiellement compromises.</span><span class="sxs-lookup"><span data-stu-id="bf439-127">Identify user accounts with the most active alerts and investigate cases of potential compromised credentials.</span></span>  


