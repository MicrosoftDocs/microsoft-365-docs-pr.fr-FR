---
title: Configurer la découverte d’appareils
description: Découvrez comment configurer la découverte d’appareils dans Microsoft 365 Defender à l’aide de la découverte standard ou de base
keywords: de base, standard, configurer la découverte de point de terminaison, la découverte d’appareils
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.technology: m365d
ms.openlocfilehash: 0d722b4f4bef5b4d178edc5f2142c887690d4c63
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765250"
---
# <a name="configure-device-discovery"></a><span data-ttu-id="e747f-104">Configurer la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="e747f-104">Configure device discovery</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e747f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e747f-105">**Applies to:**</span></span>
- [<span data-ttu-id="e747f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e747f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="e747f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e747f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="e747f-108">La découverte peut être configurée pour être en mode standard ou de base.</span><span class="sxs-lookup"><span data-stu-id="e747f-108">Discovery can be configured to be on standard or basic mode.</span></span> <span data-ttu-id="e747f-109">Utilisez l’option standard pour rechercher activement des appareils dans votre réseau, ce qui garantit mieux la découverte des points de terminaison et fournit une classification d’appareil plus riche.</span><span class="sxs-lookup"><span data-stu-id="e747f-109">Use the standard option to actively find devices in your network, which will better guarantee the discovery of endpoints and provide richer device classification.</span></span> 

<span data-ttu-id="e747f-110">Vous pouvez personnaliser la liste des appareils utilisés pour effectuer une découverte standard.</span><span class="sxs-lookup"><span data-stu-id="e747f-110">You can customize the list of devices that are used to perform standard discovery.</span></span> <span data-ttu-id="e747f-111">Vous pouvez activer la découverte standard sur tous les appareils intégrés qui également prendre en charge cette fonctionnalité (actuellement - appareils Windows 10 uniquement) ou sélectionner un sous-ensemble ou des sous-ensembles de vos appareils en spécifiant leurs balises d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e747f-111">You can either enable standard discovery on all the onboarded devices that also support this capability (currently - Windows 10 devices only) or select a subset or subsets of your devices by specifying their device tags.</span></span> 


> [!IMPORTANT]
> <span data-ttu-id="e747f-112">Pour la prévisualisation, vous devez d’abord activer les fonctionnalités d’aperçu dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e747f-112">For preview, you'll first need to turn on the Preview features in Microsoft Defender Security Center.</span></span>
> <span data-ttu-id="e747f-113">Vous pouvez ensuite accéder à la configuration de découverte d’appareils Microsoft 365 centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e747f-113">You can then access the device discovery configuration in Microsoft 365 security center.</span></span> <span data-ttu-id="e747f-114">La liste des appareils non utilisés et les recommandations de sécurité seront disponibles dans le centre de sécurité Centre de sécurité Microsoft Defender et Microsoft 365, tandis que les vignettes de tableau de bord ne seront disponibles que dans Microsoft 365 centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e747f-114">The list of unmanaged devices and security recommendations will be available in both Microsoft Defender Security Center and Microsoft 365 security center, while the dashboard tiles will only be available in Microsoft 365 security center.</span></span>


<span data-ttu-id="e747f-115">Prenez les étapes de configuration suivantes dans Microsoft 365 de sécurité :</span><span class="sxs-lookup"><span data-stu-id="e747f-115">Take the following configuration steps in Microsoft 365 security center:</span></span>

1.  <span data-ttu-id="e747f-116">Accédez à **Paramètres > détection d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e747f-116">Navigate to **Settings > Device discovery**.</span></span>
2.  <span data-ttu-id="e747f-117">Sélectionnez le mode de découverte à utiliser sur vos appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="e747f-117">Select the discovery mode to use on your onboarded devices.</span></span> 
3.  <span data-ttu-id="e747f-118">Si vous avez choisi d’utiliser la découverte standard, sélectionnez les appareils à utiliser pour l’analyse active : tous les appareils ou sur un sous-ensemble en spécifiant leurs balises d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e747f-118">If you've selected to use standard discovery, select which devices to use for active probing: all devices or on a subset by specifying their device tags.</span></span>
4. <span data-ttu-id="e747f-119">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e747f-119">Click **Save**.</span></span>


## <a name="exclude-devices-from-being-actively-probed-in-standard-discovery"></a><span data-ttu-id="e747f-120">Exclure les appareils d’être activement sondés dans la découverte standard</span><span class="sxs-lookup"><span data-stu-id="e747f-120">Exclude devices from being actively probed in standard discovery</span></span>
<span data-ttu-id="e747f-121">S’il existe des appareils sur votre réseau qui ne doivent pas être analysés activement (par exemple, les appareils utilisés comme des honeypots pour un autre outil de sécurité), vous pouvez également définir une liste d’exclusions pour empêcher leur analyse.</span><span class="sxs-lookup"><span data-stu-id="e747f-121">If there are devices on your network which should not be actively scanned (for example, devices used as honeypots for another security tool), you can also define a list of exclusions to prevent them from being scanned.</span></span> <span data-ttu-id="e747f-122">Notez que les appareils peuvent toujours être découverts en mode de découverte de base.</span><span class="sxs-lookup"><span data-stu-id="e747f-122">Note that devices can still be discovered using Basic discovery mode.</span></span> <span data-ttu-id="e747f-123">Ces appareils seront découverts passivement, mais ne seront pas activement sondés.</span><span class="sxs-lookup"><span data-stu-id="e747f-123">Those devices will be passively discovered but won't be actively probed.</span></span> 

## <a name="select-networks-to-monitor"></a><span data-ttu-id="e747f-124">Sélectionner les réseaux à surveiller</span><span class="sxs-lookup"><span data-stu-id="e747f-124">Select networks to monitor</span></span>
 <span data-ttu-id="e747f-125">Microsoft Defender pour point de terminaison analyse un réseau et détermine s’il s’agit d’un réseau d’entreprise qui doit être surveillé ou d’un réseau non professionnel qui peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="e747f-125">Microsoft Defender for Endpoint analyzes a network and determines if it is a corporate network that needs to be monitored or a non-corporate network that can be ignored.</span></span> <span data-ttu-id="e747f-126">Les réseaux d’entreprise sont généralement choisis pour être surveillés.</span><span class="sxs-lookup"><span data-stu-id="e747f-126">Corporate networks are typically chosen to be monitored.</span></span> <span data-ttu-id="e747f-127">Toutefois, vous pouvez remplacer cette décision en choisissant de surveiller les réseaux autres que ceux de l’entreprise où se trouvent les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="e747f-127">However, you can override this decision by choosing to monitor non-corporate networks where onboarded devices are found.</span></span> 

<span data-ttu-id="e747f-128">Vous pouvez configurer l’endroit où la découverte d’appareils peut être effectuée en spécifiant les réseaux à surveiller.</span><span class="sxs-lookup"><span data-stu-id="e747f-128">You can configure where device discovery can be performed by specifying which networks to monitor.</span></span> <span data-ttu-id="e747f-129">Lorsqu’un réseau est surveillé, la découverte d’appareils peut être effectuée sur ce réseau.</span><span class="sxs-lookup"><span data-stu-id="e747f-129">When a network is monitored, device discovery can be performed on it.</span></span> 

<span data-ttu-id="e747f-130">La liste des réseaux sur lequel la découverte d’appareils peut être effectuée est affichée dans la page **Réseaux surveillés.**</span><span class="sxs-lookup"><span data-stu-id="e747f-130">A list of networks where device discovery can be performed is shown in the **Monitored networks** page.</span></span> 


>[!NOTE]
> <span data-ttu-id="e747f-131">Seuls les 50 premiers réseaux (en fonction du nombre d’appareils associés) seront disponibles dans la liste réseau.</span><span class="sxs-lookup"><span data-stu-id="e747f-131">Only top 50 networks (according to the number of associated devices) will be available in the network list.</span></span> 


<span data-ttu-id="e747f-132">La liste des réseaux surveillés est triée en fonction du nombre total d’appareils observés sur le réseau au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="e747f-132">The list of monitored networks is sorted based upon the total number of devices seen on the network in the last 7 days.</span></span>


<span data-ttu-id="e747f-133">Vous pouvez appliquer un filtre pour afficher l’un des états de découverte réseau suivants :</span><span class="sxs-lookup"><span data-stu-id="e747f-133">You can apply a filter to view any of the following network discovery states:</span></span>

- <span data-ttu-id="e747f-134">**Réseaux surveillés** : réseaux où la découverte d’appareils est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e747f-134">**Monitored networks** - Networks where device discovery is performed.</span></span>
- <span data-ttu-id="e747f-135">**Réseaux ignorés** : ce réseau sera ignoré et la découverte d’appareils ne sera pas effectuée sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e747f-135">**Ignored networks** - This network will be ignored and device discovery will not be performed on it.</span></span>
- <span data-ttu-id="e747f-136">**Tous** : les réseaux surveillés et ignorés s’affichent.</span><span class="sxs-lookup"><span data-stu-id="e747f-136">**All** - Both monitored and ignored networks will be displayed.</span></span> 


### <a name="configure-the-network-monitor-state"></a><span data-ttu-id="e747f-137">Configurer l’état du moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="e747f-137">Configure the network monitor state</span></span>
<span data-ttu-id="e747f-138">Vous contrôlez l’endroit où la découverte d’appareils a lieu.</span><span class="sxs-lookup"><span data-stu-id="e747f-138">You control where device discovery takes place.</span></span> <span data-ttu-id="e747f-139">Les réseaux surveillés sont l’endroit où la découverte d’appareils est effectuée et qui sont généralement des réseaux d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e747f-139">Monitored networks is where device discovery will be performed and are typically corporate networks.</span></span> <span data-ttu-id="e747f-140">Vous pouvez également choisir d’ignorer les réseaux ou de sélectionner la classification de découverte initiale après avoir modifié un état.</span><span class="sxs-lookup"><span data-stu-id="e747f-140">You can also choose to ignore networks or select the initial discovery classification after modifying a state.</span></span> 

<span data-ttu-id="e747f-141">Le choix de la classification de découverte initiale implique l’application de l’état du moniteur réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="e747f-141">Choosing the initial discovery classification means applying the default system-made network monitor state.</span></span> <span data-ttu-id="e747f-142">Si vous sélectionnez l’état du moniteur réseau par défaut, les réseaux identifiés comme étant des réseaux d’entreprise seront surveillés et ceux identifiés comme non professionnels seront ignorés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e747f-142">Selecting the default system-made network monitor state means that networks that were identified to be corporate, will be monitored, and ones identified as non-corporate, will be ignored automatically.</span></span>
 
1. <span data-ttu-id="e747f-143">Sélectionnez **Paramètres > détection d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e747f-143">Select **Settings > Device discovery**.</span></span>
2. <span data-ttu-id="e747f-144">Sélectionnez **Réseaux surveillés.**</span><span class="sxs-lookup"><span data-stu-id="e747f-144">Select **Monitored networks**.</span></span> 
3. <span data-ttu-id="e747f-145">Afficher la liste des réseaux.</span><span class="sxs-lookup"><span data-stu-id="e747f-145">View the list of networks.</span></span> 
4. <span data-ttu-id="e747f-146">Sélectionnez les trois points en côté du nom du réseau.</span><span class="sxs-lookup"><span data-stu-id="e747f-146">Select the three dots next to the network name.</span></span> 
5. <span data-ttu-id="e747f-147">Choisissez si vous souhaitez surveiller, ignorer ou utiliser la classification de découverte initiale.</span><span class="sxs-lookup"><span data-stu-id="e747f-147">Choose whether you want to monitor, ignore, or use the initial discovery classification.</span></span> 
    
    > [!WARNING]
    >- <span data-ttu-id="e747f-148">Choisir de surveiller un réseau qui n’a pas été identifié par Microsoft Defender pour Endpoint comme réseau d’entreprise peut entraîner la découverte d’appareils en dehors de votre réseau d’entreprise, et par conséquent détecter des appareils d’entreprise ou d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="e747f-148">Choosing to monitor a network that was not identified by Microsoft Defender for Endpoint as a corporate network can cause device discovery outside of your corporate network, and may therefore detect home or other non-corporate devices.</span></span> 
    > - <span data-ttu-id="e747f-149">Choisir d’ignorer un réseau arrête la surveillance et la découverte d’appareils dans ce réseau.</span><span class="sxs-lookup"><span data-stu-id="e747f-149">Choosing to ignore a network will stop monitoring and discovering devices in that network.</span></span> <span data-ttu-id="e747f-150">Les appareils qui ont déjà été découverts ne seront pas supprimés de l’inventaire, mais ne seront plus mis à jour et les détails seront conservés jusqu’à l’expiration de la période de rétention des données de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e747f-150">Devices that were already discovered will not be removed from the inventory, but will no longer be updated, and details will be retained until the data retention period of the Defender for Endpoint expires.</span></span>
    > - <span data-ttu-id="e747f-151">Avant de choisir de surveiller les réseaux non professionnels, vous devez vous assurer que vous êtes autorisé à le faire.</span><span class="sxs-lookup"><span data-stu-id="e747f-151">Before choosing to monitor non-corporate networks, you must ensure you have permission to do so.</span></span> <br>


6. <span data-ttu-id="e747f-152">Confirmez que vous souhaitez apporter la modification.</span><span class="sxs-lookup"><span data-stu-id="e747f-152">Confirm that you want to make the change.</span></span> 




## <a name="see-also"></a><span data-ttu-id="e747f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e747f-153">See also</span></span>
- [<span data-ttu-id="e747f-154">Vue d’ensemble de la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="e747f-154">Device discovery overview</span></span>](device-discovery.md)
- [<span data-ttu-id="e747f-155">FAQ sur la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="e747f-155">Device discovery FAQs</span></span>](device-discovery-faq.md)