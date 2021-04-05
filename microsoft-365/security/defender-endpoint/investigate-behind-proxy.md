---
title: Examiner des événements de connexion qui se produisent d’arrière vers l’avant des proxys
description: Découvrez comment utiliser la surveillance avancée au niveau HTTP par le biais de la protection réseau dans Microsoft Defender ATP, qui utilise une cible réelle, au lieu d’un proxy.
keywords: proxy, protection réseau, proxy avant, événements réseau, audit, bloc, noms de domaine, domaine
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 28d8a113ed77e9624bd914571b1af4a7ece2aa5c
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587562"
---
# <a name="investigate-connection-events-that-occur-behind-forward-proxies"></a><span data-ttu-id="4fb93-104">Examiner des événements de connexion qui se produisent d’arrière vers l’avant des proxys</span><span class="sxs-lookup"><span data-stu-id="4fb93-104">Investigate connection events that occur behind forward proxies</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4fb93-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4fb93-105">**Applies to:**</span></span>
- [<span data-ttu-id="4fb93-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4fb93-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="4fb93-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4fb93-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="4fb93-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="4fb93-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="4fb93-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="4fb93-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatemachines-abovefoldlink)

<span data-ttu-id="4fb93-110">Defender pour le point de terminaison prend en charge la surveillance des connexions réseau à partir de différents niveaux de la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="4fb93-110">Defender for Endpoint supports network connection monitoring from different levels of the network stack.</span></span> <span data-ttu-id="4fb93-111">Un cas difficile est celui où le réseau utilise un proxy avant comme passerelle vers Internet.</span><span class="sxs-lookup"><span data-stu-id="4fb93-111">A challenging case is when the network uses a forward proxy as a gateway to the Internet.</span></span>

<span data-ttu-id="4fb93-112">Le proxy agit comme s’il s’agissait du point de terminaison cible.</span><span class="sxs-lookup"><span data-stu-id="4fb93-112">The proxy acts as if it was the target endpoint.</span></span>  <span data-ttu-id="4fb93-113">Dans ce cas, les moniteurs de connexion réseau simples auditent les connexions avec le proxy, ce qui est correct mais qui a une valeur d’investigation inférieure.</span><span class="sxs-lookup"><span data-stu-id="4fb93-113">In these cases, simple network connection monitors will audit the connections with the proxy which is correct but has lower investigation value.</span></span> 

<span data-ttu-id="4fb93-114">Defender pour le point de terminaison prend en charge la surveillance avancée au niveau HTTP via la protection réseau.</span><span class="sxs-lookup"><span data-stu-id="4fb93-114">Defender for Endpoint supports advanced HTTP level monitoring through network protection.</span></span> <span data-ttu-id="4fb93-115">Lorsqu’il est allumé, un nouveau type d’événement est exposé, qui expose les noms de domaine cibles réels.</span><span class="sxs-lookup"><span data-stu-id="4fb93-115">When turned on, a new type of event is surfaced which exposes the real target domain names.</span></span>

## <a name="use-network-protection-to-monitor-network-connection-behind-a-firewall"></a><span data-ttu-id="4fb93-116">Utiliser la protection réseau pour surveiller la connexion réseau derrière un pare-feu</span><span class="sxs-lookup"><span data-stu-id="4fb93-116">Use network protection to monitor network connection behind a firewall</span></span>
<span data-ttu-id="4fb93-117">La surveillance de la connexion réseau derrière un proxy avant est possible en raison d’événements réseau supplémentaires qui proviennent de la protection du réseau.</span><span class="sxs-lookup"><span data-stu-id="4fb93-117">Monitoring network connection behind a forward proxy is possible due to additional network events that originate from network protection.</span></span> <span data-ttu-id="4fb93-118">Pour les voir sur une chronologie d’appareil, activer la protection réseau (au minimum en mode audit).</span><span class="sxs-lookup"><span data-stu-id="4fb93-118">To see them on a device timeline, turn network protection on (at the minimum in audit mode).</span></span> 

<span data-ttu-id="4fb93-119">La protection réseau peut être contrôlée à l’aide des modes suivants :</span><span class="sxs-lookup"><span data-stu-id="4fb93-119">Network protection can be controlled using the following modes:</span></span>

- <span data-ttu-id="4fb93-120">**Bloquer**</span><span class="sxs-lookup"><span data-stu-id="4fb93-120">**Block**</span></span> <br> <span data-ttu-id="4fb93-121">Les utilisateurs ou les applications ne pourront pas se connecter à des domaines dangereux.</span><span class="sxs-lookup"><span data-stu-id="4fb93-121">Users or apps will be blocked from connecting to dangerous domains.</span></span> <span data-ttu-id="4fb93-122">Vous pourrez voir cette activité dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4fb93-122">You will be able to see this activity in Microsoft Defender Security Center.</span></span>
- <span data-ttu-id="4fb93-123">**Audit**</span><span class="sxs-lookup"><span data-stu-id="4fb93-123">**Audit**</span></span> <br> <span data-ttu-id="4fb93-124">La connexion à des domaines dangereux ne sera pas bloquée pour les utilisateurs ou les applications.</span><span class="sxs-lookup"><span data-stu-id="4fb93-124">Users or apps will not be blocked from connecting to dangerous domains.</span></span> <span data-ttu-id="4fb93-125">Toutefois, vous verrez toujours cette activité dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4fb93-125">However, you will still see this activity in Microsoft Defender Security Center.</span></span>


<span data-ttu-id="4fb93-126">Si vous désactiver la protection réseau, les utilisateurs ou les applications ne seront pas bloqués pour se connecter à des domaines dangereux.</span><span class="sxs-lookup"><span data-stu-id="4fb93-126">If you turn network protection off, users or apps will not be blocked from connecting to dangerous domains.</span></span> <span data-ttu-id="4fb93-127">Vous ne verrez aucune activité réseau dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4fb93-127">You will not see any network activity in Microsoft Defender Security Center.</span></span>

<span data-ttu-id="4fb93-128">Si vous ne la configurez pas, le blocage du réseau est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="4fb93-128">If you do not configure it, network blocking will be turned off by default.</span></span>

<span data-ttu-id="4fb93-129">Pour plus d’informations, voir [Activer la protection réseau.](enable-network-protection.md)</span><span class="sxs-lookup"><span data-stu-id="4fb93-129">For more information, see [Enable network protection](enable-network-protection.md).</span></span>

## <a name="investigation-impact"></a><span data-ttu-id="4fb93-130">Impact de l’examen</span><span class="sxs-lookup"><span data-stu-id="4fb93-130">Investigation impact</span></span>
<span data-ttu-id="4fb93-131">Lorsque la protection réseau est allumée, vous verrez que, sur la chronologie d’un appareil, l’adresse IP continuera à représenter le proxy, tandis que l’adresse cible réelle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4fb93-131">When network protection is turned on, you'll see that on a device's timeline the IP address will keep representing the proxy, while the real target address shows up.</span></span>

![Image des événements réseau sur la chronologie de l’appareil](images/atp-proxy-investigation.png)

<span data-ttu-id="4fb93-133">D’autres événements déclenchés par la couche de protection réseau sont désormais disponibles pour faire surface des noms de domaine réels, même derrière un proxy.</span><span class="sxs-lookup"><span data-stu-id="4fb93-133">Additional events triggered by the network protection layer are now available to surface the real domain names even behind a proxy.</span></span>

<span data-ttu-id="4fb93-134">Informations sur l’événement :</span><span class="sxs-lookup"><span data-stu-id="4fb93-134">Event's information:</span></span>

![Image d’un événement réseau unique](images/atp-proxy-investigation-event.png)



## <a name="hunt-for-connection-events-using-advanced-hunting"></a><span data-ttu-id="4fb93-136">Recherche des événements de connexion à l’aide de la recherche avancée</span><span class="sxs-lookup"><span data-stu-id="4fb93-136">Hunt for connection events using advanced hunting</span></span> 
<span data-ttu-id="4fb93-137">Tous les nouveaux événements de connexion sont également disponibles pour la recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="4fb93-137">All new connection events are available for you to hunt on through advanced hunting as well.</span></span> <span data-ttu-id="4fb93-138">Étant donné que ces événements sont des événements de connexion, vous pouvez les trouver sous la table DeviceNetworkEvents sous le `ConnecionSuccess` type d’action.</span><span class="sxs-lookup"><span data-stu-id="4fb93-138">Since these events are connection events, you can find them under the DeviceNetworkEvents table under the `ConnecionSuccess` action type.</span></span>

<span data-ttu-id="4fb93-139">L’utilisation de cette requête simple vous montre tous les événements pertinents :</span><span class="sxs-lookup"><span data-stu-id="4fb93-139">Using this simple query will show you all the relevant events:</span></span>

```
DeviceNetworkEvents
| where ActionType == "ConnectionSuccess" 
| take 10
```

![Image d’une requête de recherche avancée](images/atp-proxy-investigation-ah.png)

<span data-ttu-id="4fb93-141">Vous pouvez également filtrer les événements liés à la connexion au proxy lui-même.</span><span class="sxs-lookup"><span data-stu-id="4fb93-141">You can also filter out  events that are related to connection to the proxy itself.</span></span> 

<span data-ttu-id="4fb93-142">Utilisez la requête suivante pour filtrer les connexions au proxy :</span><span class="sxs-lookup"><span data-stu-id="4fb93-142">Use the following query to filter out the connections to the proxy:</span></span>

```
DeviceNetworkEvents
| where ActionType == "ConnectionSuccess" and RemoteIP != "ProxyIP"  
| take 10
```



## <a name="related-topics"></a><span data-ttu-id="4fb93-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fb93-143">Related topics</span></span>
- [<span data-ttu-id="4fb93-144">Application de la protection réseau avec la stratégie de groupe - CSP de stratégie</span><span class="sxs-lookup"><span data-stu-id="4fb93-144">Applying network protection with GP - policy CSP</span></span>](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
