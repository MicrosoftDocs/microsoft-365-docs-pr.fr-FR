---
title: Prise en charge de la traduction d'adresses réseau (NAT) avec Office 365
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 1/24/2017
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- BCS160
ms.assetid: 170e96ea-d65d-4e51-acac-1de56abe39b9
description: Cet article fournit des détails sur la façon d’obtenir une valeur approximative du nombre de clients que vous pouvez utiliser par adresse IP dans votre organisation à l’aide de nat.
ms.openlocfilehash: f48874853c3acb80927933761862b14379b6d4bd
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689612"
---
# <a name="nat-support-with-office-365"></a><span data-ttu-id="c4801-103">Prise en charge de la traduction d'adresses réseau (NAT) avec Office 365</span><span class="sxs-lookup"><span data-stu-id="c4801-103">NAT support with Office 365</span></span>

<span data-ttu-id="c4801-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="c4801-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="c4801-105">Auparavant, les conseils suggéraient que le nombre maximal de clients Exchange que vous devez utiliser par adresse IP pour vous connecter à Office 365 était d’environ 2 000 clients par port réseau.</span><span class="sxs-lookup"><span data-stu-id="c4801-105">Previously, guidance suggested that the maximum number of Exchange clients you should use per IP address to connect to Office 365 was about 2,000 clients per network port.</span></span>
  
## <a name="why-use-nat"></a><span data-ttu-id="c4801-106">Pourquoi utiliser NAT ?</span><span class="sxs-lookup"><span data-stu-id="c4801-106">Why use NAT?</span></span>

<span data-ttu-id="c4801-107">À l’aide de nat, des milliers de personnes sur un réseau d’entreprise peuvent « partager » quelques adresses IP routables publiquement.</span><span class="sxs-lookup"><span data-stu-id="c4801-107">By using NAT, thousands of people on a corporate network can "share" a few publicly routable IP addresses.</span></span>
  
<span data-ttu-id="c4801-108">La plupart des réseaux d’entreprise utilisent un espace d’adressare IP privé (RFC1918).</span><span class="sxs-lookup"><span data-stu-id="c4801-108">Most corporate networks use private (RFC1918) IP address space.</span></span> <span data-ttu-id="c4801-109">L’espace d’adressag privé est alloué par l’IANA (Internet Assigned Numbers Authority) et destiné uniquement aux réseaux qui ne sont pas acheminés directement vers et depuis Internet.</span><span class="sxs-lookup"><span data-stu-id="c4801-109">Private address space is allocated by the Internet Assigned Numbers Authority (IANA) and intended solely for networks that do not route directly to and from the global Internet.</span></span>
  
<span data-ttu-id="c4801-110">Pour fournir un accès Internet aux appareils sur un espace d’adressa visite IP privé, les organisations utilisent des technologies de passerelle telles que les pare-feux et les proxies qui fournissent des services de traduction d’adresses réseau (NAT) ou de traduction d’adresses de port (PAT).</span><span class="sxs-lookup"><span data-stu-id="c4801-110">To provide Internet access to devices on a private IP address space, organizations use gateway technologies like firewalls and proxies that provide network address translation (NAT) or port address translation (PAT) services.</span></span> <span data-ttu-id="c4801-111">Ces passerelles font en sorte que le trafic provenant d’appareils internes vers Internet (y compris Office 365) semble être provenant d’une ou plusieurs adresses IP routables publiquement.</span><span class="sxs-lookup"><span data-stu-id="c4801-111">These gateways make traffic from internal devices to the Internet (including Office 365) appear to be coming from one or more publicly routable IP addresses.</span></span> <span data-ttu-id="c4801-112">Chaque connexion sortante d’un appareil interne se traduit par un port TCP source différent sur l’adresse IP publique.</span><span class="sxs-lookup"><span data-stu-id="c4801-112">Each outbound connection from an internal device translates to a different source TCP port on the public IP address.</span></span> 
  
## <a name="why-do-you-need-to-have-so-many-connections-open-to-office-365-at-the-same-time"></a><span data-ttu-id="c4801-113">Pourquoi devez-vous avoir autant de connexions ouvertes à Office 365 en même temps ?</span><span class="sxs-lookup"><span data-stu-id="c4801-113">Why do you need to have so many connections open to Office 365 at the same time?</span></span>

<span data-ttu-id="c4801-114">Outlook peut ouvrir huit connexions ou plus (dans les situations où il existe des modules de 2013, des calendriers partagés, des boîtes aux lettres, etc.).</span><span class="sxs-lookup"><span data-stu-id="c4801-114">Outlook may open eight or more connections (in situations where there are add-ins, shared calendars, mailboxes, etc.).</span></span> <span data-ttu-id="c4801-115">Étant donné qu’un maximum de 64 000 ports sont disponibles sur un périphérique NAT basé sur Windows, il peut y avoir 8 000 utilisateurs au maximum derrière une adresse IP avant que les ports ne soient épuisés.</span><span class="sxs-lookup"><span data-stu-id="c4801-115">Because there are a maximum of 64,000 ports available on a Windows-based NAT device, there can be a maximum of 8,000 users behind an IP address before the ports are exhausted.</span></span> <span data-ttu-id="c4801-116">Notez que si les clients utilisent des appareils non basés sur le système d’exploitation Windows pour nat, le nombre total de ports disponibles dépend de l’appareil ou du logiciel NAT utilisé.</span><span class="sxs-lookup"><span data-stu-id="c4801-116">Note that if customers are using non-Windows OS-based devices for NAT, the total available ports are dependent on what NAT device or software is being used.</span></span> <span data-ttu-id="c4801-117">Dans ce scénario, le nombre maximal de ports peut être inférieur à 64 000.</span><span class="sxs-lookup"><span data-stu-id="c4801-117">In this scenario, the maximum number of ports could be less than 64,000.</span></span> <span data-ttu-id="c4801-118">La disponibilité des ports est également affectée par d’autres facteurs tels que Windows limitant 4 000 ports pour son propre usage, ce qui réduit le nombre total de ports disponibles à 60 000.</span><span class="sxs-lookup"><span data-stu-id="c4801-118">Availability of ports is also affected by other factors such as Windows restricting 4,000 ports for its own use, which reduces the total number of available ports to 60,000.</span></span> <span data-ttu-id="c4801-119">Il peut y avoir d’autres applications, telles qu’Internet Explorer, qui peuvent se connecter en même temps, nécessitant des ports supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c4801-119">There may be other applications, such as Internet Explorer, that could connect at the same time, requiring additional ports.</span></span>
  
## <a name="calculating-maximum-supported-devices-behind-a-single-public-ip-address-with-office-365"></a><span data-ttu-id="c4801-120">Calcul du nombre maximal d’appareils pris en charge derrière une adresse IP publique unique avec Office 365</span><span class="sxs-lookup"><span data-stu-id="c4801-120">Calculating maximum supported devices behind a single public IP address with Office 365</span></span>

<span data-ttu-id="c4801-121">Pour déterminer le nombre maximal d’appareils derrière une seule adresse IP publique, vous devez surveiller le trafic réseau afin de déterminer la consommation maximale des ports par client.</span><span class="sxs-lookup"><span data-stu-id="c4801-121">To determine the maximum number of devices behind a single public IP address, you should monitor network traffic to determine peak port consumption per client.</span></span> <span data-ttu-id="c4801-122">En outre, un facteur de pointe doit être utilisé pour l’utilisation du port (minimum 4).</span><span class="sxs-lookup"><span data-stu-id="c4801-122">Also, a peak factor should be used for the port usage (minimum 4).</span></span> 
  
 <span data-ttu-id="c4801-123">**Utilisez la formule suivante pour calculer le nombre d’appareils pris en charge par adresse IP :**</span><span class="sxs-lookup"><span data-stu-id="c4801-123">**Use the following formula to calculate the number of supported devices per IP address:**</span></span>
  
<span data-ttu-id="c4801-124">Nombre maximal d’appareils pris en charge derrière une seule adresse IP publique = (64 000 - ports restreints)/(Consommation maximale des ports + facteur de pointe)</span><span class="sxs-lookup"><span data-stu-id="c4801-124">Maximum supported devices behind a single public IP address = (64,000 - restricted ports)/(Peak port consumption + peak factor)</span></span>
  
 <span data-ttu-id="c4801-125">**Par exemple, si les valeurs suivantes sont vraies :**</span><span class="sxs-lookup"><span data-stu-id="c4801-125">**For example, if the following were true:**</span></span>
  
- <span data-ttu-id="c4801-126">**Ports restreints :** 4 000 pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c4801-126">**Restricted ports:** 4,000 for the operating system</span></span>

- <span data-ttu-id="c4801-127">**Consommation maximale des ports :** 6 par appareil</span><span class="sxs-lookup"><span data-stu-id="c4801-127">**Peak port consumption:** 6 per device</span></span>

- <span data-ttu-id="c4801-128">**Facteur de pointe :** 4</span><span class="sxs-lookup"><span data-stu-id="c4801-128">**Peak factor:** 4</span></span>

<span data-ttu-id="c4801-129">Ensuite, le nombre maximal d’appareils pris en charge derrière une seule adresse IP publique = (64 000 - 4 000)/(6 + 4) = 6 000</span><span class="sxs-lookup"><span data-stu-id="c4801-129">Then, the maximum supported devices behind a single public IP address = (64,000 - 4,000)/(6 + 4) = 6,000</span></span>
  
<span data-ttu-id="c4801-130">Avec la publication du pack d’hébergement Office 365, inclus dans les mises à jour de septembre 2011 pour Microsoft Office Outlook 2007 ou novembre 2011 pour Microsoft Outlook 2010, ou d’une mise à jour ultérieure, le nombre de connexions de Outlook (Office Outlook 2007 avec Service Pack 2 et Outlook 2010) à Exchange peut être aussi petit que 2.</span><span class="sxs-lookup"><span data-stu-id="c4801-130">With the release of Office 365 hosting pack, included in the updates from September 2011 for Microsoft Office Outlook 2007, or November 2011 for Microsoft Outlook 2010, or a later update, the number of connections from Outlook (both Office Outlook 2007 with Service Pack 2 and Outlook 2010) to Exchange can be as few as 2.</span></span> <span data-ttu-id="c4801-131">Vous devez prendre en compte les différents systèmes d’exploitation, les comportements des utilisateurs, etc. pour déterminer le nombre minimal et maximal de ports dont votre réseau aura besoin au maximum.</span><span class="sxs-lookup"><span data-stu-id="c4801-131">You'll need to factor in the different operating systems, user behaviors, and so on to determine the minimum and maximum number of ports that your network will require at peak.</span></span>
  
<span data-ttu-id="c4801-132">Si vous souhaitez prendre en charge davantage d’appareils derrière une seule adresse IP publique, suivez les étapes décrites pour évaluer le nombre maximal d’appareils qui peuvent être pris en charge :</span><span class="sxs-lookup"><span data-stu-id="c4801-132">If you want to support more devices behind a single public IP address, follow the steps outlined to assess the maximum number of devices that can be supported:</span></span>
  
<span data-ttu-id="c4801-133">Surveillez le trafic réseau pour déterminer la consommation maximale des ports par client.</span><span class="sxs-lookup"><span data-stu-id="c4801-133">Monitor network traffic to determine peak port consumption per client.</span></span> <span data-ttu-id="c4801-134">Vous devez collecter les données ci-après :</span><span class="sxs-lookup"><span data-stu-id="c4801-134">You should collect this data:</span></span>
  
- <span data-ttu-id="c4801-135">À partir de plusieurs emplacements</span><span class="sxs-lookup"><span data-stu-id="c4801-135">From multiple locations</span></span>
    
- <span data-ttu-id="c4801-136">À partir de plusieurs appareils</span><span class="sxs-lookup"><span data-stu-id="c4801-136">From multiple devices</span></span>
    
- <span data-ttu-id="c4801-137">À plusieurs reprises</span><span class="sxs-lookup"><span data-stu-id="c4801-137">At multiple times</span></span>
    
<span data-ttu-id="c4801-138">Utilisez la formule précédente pour calculer le nombre maximal d’utilisateurs par adresse IP qui peuvent être pris en charge dans leur environnement.</span><span class="sxs-lookup"><span data-stu-id="c4801-138">Use the preceding formula to calculate the maximum users per IP address that can be supported in their environment.</span></span>
  
<span data-ttu-id="c4801-139">Il existe différentes méthodes pour répartir la charge du client entre des adresses IP publiques supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c4801-139">There are various methods for distributing client load across additional public IP addresses.</span></span> <span data-ttu-id="c4801-140">Les stratégies disponibles dépendent des fonctionnalités de la solution de passerelle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c4801-140">Strategies available depend on the capabilities of the corporate gateway solution.</span></span> <span data-ttu-id="c4801-141">La solution la plus simple consiste à segmenter l’espace d’adressa ment de l’utilisateur et à « attribuer » de manière statique un certain nombre d’adresses IP à chaque passerelle.</span><span class="sxs-lookup"><span data-stu-id="c4801-141">The simplest solution is to segment your user address space and statically "assign" a number of IP addresses to each gateway.</span></span> <span data-ttu-id="c4801-142">De nombreux périphériques de passerelle offrent également la possibilité d’utiliser un pool d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="c4801-142">Another alternative that many gateway devices offer is the ability to use a pool of IP addresses.</span></span> <span data-ttu-id="c4801-143">L’avantage du pool d’adresses est qu’il est beaucoup plus dynamique et moins susceptible de nécessiter un ajustement à mesure que votre base d’utilisateurs augmente.</span><span class="sxs-lookup"><span data-stu-id="c4801-143">The benefit of the address pool is that it is much more dynamic and less likely to require adjustment as your user base grows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4801-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4801-144">See also</span></span>

[<span data-ttu-id="c4801-145">Gestion des points de terminaison Office 365</span><span class="sxs-lookup"><span data-stu-id="c4801-145">Managing Office 365 endpoints</span></span>](https://support.office.com/article/99cab9d4-ef59-4207-9f2b-3728eb46bf9a)
  
[<span data-ttu-id="c4801-146">Points de terminaison Office 365 - FAQ</span><span class="sxs-lookup"><span data-stu-id="c4801-146">Office 365 endpoints FAQ</span></span>](https://support.office.com/article/d4088321-1c89-4b96-9c99-54c75cae2e6d)
