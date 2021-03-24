---
title: Examiner une adresse IP associée à une alerte
description: Utilisez les options d’examen pour examiner les communications possibles entre les appareils et les adresses IP externes.
keywords: examiner, examen, adresse IP, alerte, microsoft defender atp, IP externe
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: ca7f5e9126ffd57f7e858210e006bc05459d567b
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062606"
---
# <a name="investigate-an-ip-address-associated-with-a-microsoft-defender-for-endpoint-alert"></a><span data-ttu-id="401aa-104">Examiner une adresse IP associée à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-104">Investigate an IP address associated with a Microsoft Defender for Endpoint alert</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="401aa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="401aa-105">**Applies to:**</span></span>
- [<span data-ttu-id="401aa-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="401aa-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="401aa-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="401aa-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="401aa-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="401aa-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="401aa-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="401aa-110">Examinez les communications possibles entre vos appareils et les adresses IP externes.</span><span class="sxs-lookup"><span data-stu-id="401aa-110">Examine possible communication between your devices and external internet protocol (IP) addresses.</span></span>

<span data-ttu-id="401aa-111">L’identification de tous les appareils de l’organisation ayant communiqué avec une adresse IP malveillante suspectée ou connue, telle que les serveurs de commande et de contrôle (C2), permet de déterminer l’étendue potentielle de la violation, des fichiers associés et des appareils infectés.</span><span class="sxs-lookup"><span data-stu-id="401aa-111">Identifying all devices in the organization that communicated with a suspected or known malicious IP address, such as Command and Control (C2) servers, helps determine the potential scope of breach, associated files, and infected devices.</span></span>

<span data-ttu-id="401aa-112">Vous trouverez des informations dans les sections suivantes dans l’affichage des adresses IP :</span><span class="sxs-lookup"><span data-stu-id="401aa-112">You can find information from the following sections in the IP address view:</span></span>

- <span data-ttu-id="401aa-113">IP dans le monde entier</span><span class="sxs-lookup"><span data-stu-id="401aa-113">IP worldwide</span></span>
- <span data-ttu-id="401aa-114">Noms DNS inversés</span><span class="sxs-lookup"><span data-stu-id="401aa-114">Reverse DNS names</span></span>
- <span data-ttu-id="401aa-115">Alertes associées à cette adresse IP</span><span class="sxs-lookup"><span data-stu-id="401aa-115">Alerts related to this IP</span></span>
- <span data-ttu-id="401aa-116">IP dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="401aa-116">IP in organization</span></span>
- <span data-ttu-id="401aa-117">Prévalence</span><span class="sxs-lookup"><span data-stu-id="401aa-117">Prevalence</span></span>

## <a name="ip-worldwide-and-reverse-dns-names"></a><span data-ttu-id="401aa-118">Noms DNS IP dans le monde entier et inverses</span><span class="sxs-lookup"><span data-stu-id="401aa-118">IP Worldwide and Reverse DNS names</span></span>

<span data-ttu-id="401aa-119">La section Détails de l’adresse IP affiche les attributs de l’adresse IP, tels que son ASN et ses noms DNS inverses.</span><span class="sxs-lookup"><span data-stu-id="401aa-119">The IP address details section shows attributes of the IP address such as its ASN and its Reverse DNS names.</span></span>

## <a name="alerts-related-to-this-ip"></a><span data-ttu-id="401aa-120">Alertes associées à cette adresse IP</span><span class="sxs-lookup"><span data-stu-id="401aa-120">Alerts related to this IP</span></span>

<span data-ttu-id="401aa-121">Les **alertes associées à cette** section IP fournissent une liste des alertes associées à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="401aa-121">The **Alerts related to this IP** section provides a list of alerts that are associated with the IP.</span></span>

## <a name="ip-in-organization"></a><span data-ttu-id="401aa-122">IP dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="401aa-122">IP in organization</span></span>

<span data-ttu-id="401aa-123">La section **IP de l’organisation** fournit des détails sur la prévalence de l’adresse IP dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="401aa-123">The **IP in organization** section provides details on the prevalence of the IP address in the organization.</span></span>

## <a name="prevalence"></a><span data-ttu-id="401aa-124">Prévalence</span><span class="sxs-lookup"><span data-stu-id="401aa-124">Prevalence</span></span>

<span data-ttu-id="401aa-125">La section **Prévalence** affiche le nombre d’appareils connectés à cette adresse IP et le moment où l’adresse IP a été vue pour la première et la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="401aa-125">The **Prevalence** section displays how many devices have connected to this IP address, and when the IP was first and last seen.</span></span> <span data-ttu-id="401aa-126">Vous pouvez filtrer les résultats de cette section par période . la période par défaut est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="401aa-126">You can filter the results of this section by time period; the default period is 30 days.</span></span>

## <a name="most-recent-observed-devices-with-ip"></a><span data-ttu-id="401aa-127">Appareils les plus récemment observés avec ip</span><span class="sxs-lookup"><span data-stu-id="401aa-127">Most recent observed devices with IP</span></span>

<span data-ttu-id="401aa-128">La section **Appareils les plus récemment observés** avec ip fournit une vue chronologique des événements et des alertes associées observés sur l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="401aa-128">The **Most recent observed devices** with IP section provides a chronological view on the events and associated alerts that were observed on the IP address.</span></span>

<span data-ttu-id="401aa-129">**Examinez une adresse IP externe :**</span><span class="sxs-lookup"><span data-stu-id="401aa-129">**Investigate an external IP:**</span></span>

1. <span data-ttu-id="401aa-130">Sélectionnez **l’adresse IP** dans **le** menu déroulant de la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="401aa-130">Select **IP** from the **Search bar** drop-down menu.</span></span>
2. <span data-ttu-id="401aa-131">Entrez l’adresse IP dans le **champ** Recherche.</span><span class="sxs-lookup"><span data-stu-id="401aa-131">Enter the IP address in the **Search** field.</span></span>
3. <span data-ttu-id="401aa-132">Cliquez sur l’icône de recherche ou appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="401aa-132">Click the search icon or press **Enter**.</span></span>

<span data-ttu-id="401aa-133">Des détails sur l’adresse IP sont affichés, notamment : les détails d’inscription (le cas contraire), les adresses IP inversées (par exemple, les domaines), la prévalence des appareils de l’organisation qui ont communiqué avec cette adresse IP (pendant la période sélectionnable) et les périphériques de l’organisation qui ont été observés pour communiquer avec cette adresse IP.</span><span class="sxs-lookup"><span data-stu-id="401aa-133">Details about the IP address are displayed, including: registration details (if available), reverse IPs (for example, domains), prevalence of devices in the organization that communicated with this IP Address (during selectable time period), and the devices in the organization that were observed communicating with this IP address.</span></span>

> [!NOTE]
> <span data-ttu-id="401aa-134">Les résultats de la recherche seront renvoyés uniquement pour les adresses IP observées lors de la communication avec les appareils de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="401aa-134">Search results will only be returned for IP addresses observed in communication with devices in the organization.</span></span>

<span data-ttu-id="401aa-135">Utilisez les filtres de recherche pour définir les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="401aa-135">Use the search filters to define the search criteria.</span></span> <span data-ttu-id="401aa-136">Vous pouvez également utiliser la zone de recherche de chronologie pour filtrer les résultats affichés de tous les appareils de l’organisation observés en communication avec l’adresse IP, le fichier associé à la communication et la dernière date observée.</span><span class="sxs-lookup"><span data-stu-id="401aa-136">You can also use the timeline search box to filter the displayed results of all devices in the organization observed communicating with the IP address, the file associated with the communication and the last date observed.</span></span>

<span data-ttu-id="401aa-137">En cliquant sur l’un des noms d’appareils, vous pouvez continuer à examiner les alertes, comportements et événements signalés.</span><span class="sxs-lookup"><span data-stu-id="401aa-137">Clicking any of the device names will take you to that device's view, where you can continue investigate reported alerts, behaviors, and events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="401aa-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="401aa-138">Related topics</span></span>

- [<span data-ttu-id="401aa-139">Afficher et organiser la file d’attente des alertes de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-139">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="401aa-140">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-140">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="401aa-141">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-141">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="401aa-142">Examiner un fichier associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-142">Investigate a file associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="401aa-143">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-143">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="401aa-144">Examiner un domaine associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-144">Investigate a domain associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-domain.md)
- [<span data-ttu-id="401aa-145">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="401aa-145">Investigate a user account in Microsoft Defender for Endpoint</span></span>](investigate-user.md)
