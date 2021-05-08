---
title: Vue d’ensemble de la découverte d’appareils
description: Découvrez comment tirer parti de la découverte de points de terminaison dans Microsoft 365 Defender pour rechercher des appareils non utilisés dans votre réseau
keywords: détection d’appareils, découverte, passif, proactif, réseau, visibilité, serveur, station de travail, intégration, appareils nonmanagés
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
ms.openlocfilehash: 2dee1193e9f852e66df324927bf38d37d736d251
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245947"
---
# <a name="device-discovery-overview"></a><span data-ttu-id="aa3d8-104">Vue d’ensemble de la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="aa3d8-104">Device discovery overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="aa3d8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="aa3d8-105">**Applies to:**</span></span>
- [<span data-ttu-id="aa3d8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="aa3d8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="aa3d8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="aa3d8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="aa3d8-108">La protection de votre environnement nécessite d’inventorier les appareils qui se sont connectés à votre réseau.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-108">Protecting your environment requires taking inventory of the devices that are in your network.</span></span> <span data-ttu-id="aa3d8-109">Toutefois, le mappage d’appareils dans un réseau peut souvent être coûteux, difficile et chronophage.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-109">However, mapping devices in a network can often be expensive, challenging, and time-consuming.</span></span> 

<span data-ttu-id="aa3d8-110">Microsoft Defender pour endpoint fournit une fonctionnalité de découverte d’appareils qui vous permet de trouver des appareils non utilisés connectés à votre réseau d’entreprise sans avoir besoin d’appliances supplémentaires ou de modifications de processus fastidieuses.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-110">Microsoft Defender for Endpoint provides a device discovery capability that helps you find unmanaged devices connected to your corporate network without the need for extra appliances or cumbersome process changes.</span></span>


<span data-ttu-id="aa3d8-111">La fonctionnalité de découverte d’appareils vous permet de :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-111">The device discovery capability allows you to:</span></span>

- <span data-ttu-id="aa3d8-112">**Découvrir les points de terminaison d’entreprise connectés à votre réseau d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="aa3d8-112">**Discover enterprise endpoints connected to your corporate network**</span></span> <br>
<span data-ttu-id="aa3d8-113">À l’aide des options de découverte standard ou de base, vous pouvez découvrir les stations de travail, les serveurs et les points de terminaison mobiles qui ne sont pas encore intégrés à Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-113">Using either basic or standard discovery options, you can discover workstations, servers, and mobile endpoints that are not yet onboarded to Microsoft Defender for Endpoint.</span></span>  

- <span data-ttu-id="aa3d8-114">**Intégrer les points de terminaison découverts**</span><span class="sxs-lookup"><span data-stu-id="aa3d8-114">**Onboard discovered endpoints**</span></span><br>
<span data-ttu-id="aa3d8-115">Les points de terminaison non pris en compte dans votre réseau introduisent des vulnérabilités et des risques pour votre réseau.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-115">Unmanaged endpoints in your network introduce vulnerabilities and risks to your network.</span></span> <span data-ttu-id="aa3d8-116">Leur intégration au service peut accroître leur visibilité sur la sécurité.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-116">Onboarding them to the service can increase the security visibility on them.</span></span> 

<span data-ttu-id="aa3d8-117">Parallèlement à cette fonctionnalité, une nouvelle recommandation de sécurité pour intégrer des appareils à Microsoft Defender pour le point de terminaison sera disponible dans le cadre de l’expérience de gestion des menaces et des vulnérabilités existante.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-117">In conjunction with this capability, a new security recommendation to onboard devices to Microsoft Defender for Endpoint will be available as part of the existing Threat and Vulnerability Management experience.</span></span>



## <a name="discovery-methods"></a><span data-ttu-id="aa3d8-118">Méthodes de découverte</span><span class="sxs-lookup"><span data-stu-id="aa3d8-118">Discovery methods</span></span>
<span data-ttu-id="aa3d8-119">Il existe deux modes de découverte :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-119">There are two modes of discovery:</span></span> 

-   <span data-ttu-id="aa3d8-120">Découverte de base</span><span class="sxs-lookup"><span data-stu-id="aa3d8-120">Basic discovery</span></span> 
-   <span data-ttu-id="aa3d8-121">Découverte standard (recommandé)</span><span class="sxs-lookup"><span data-stu-id="aa3d8-121">Standard discovery (recommended)</span></span> 


> [!IMPORTANT]
> <span data-ttu-id="aa3d8-122">La découverte est définie sur le mode de base.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-122">Discovery is set to basic mode.</span></span> <span data-ttu-id="aa3d8-123">Vous pouvez choisir de conserver cette configuration via la page paramètres.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-123">You can choose to retain this configuration through the settings page.</span></span> <span data-ttu-id="aa3d8-124">La découverte standard sera le mode par défaut pour tous les clients de prévisualisation à compter du 10 mai 2021, sauf si elle est modifiée via la page des paramètres avant cette date.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-124">Standard discovery will be the default mode for all preview customers starting May 10, 2021 - unless modified through the settings page before this date.</span></span>

### <a name="basic-discovery"></a><span data-ttu-id="aa3d8-125">Découverte de base</span><span class="sxs-lookup"><span data-stu-id="aa3d8-125">Basic discovery</span></span> 

<span data-ttu-id="aa3d8-126">Dans ce mode, les points de terminaison collectent passivement des événements dans votre réseau et extraient les informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-126">In this mode, endpoints will passively collect events in your network and extract device information from them.</span></span> <span data-ttu-id="aa3d8-127">La découverte de base utilise SenseNDR.exe binaire pour la collecte de données réseau passives et aucun trafic réseau n’est initié.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-127">Basic discovery uses the SenseNDR.exe binary for passive network data collection and no network traffic will be initiated.</span></span> <span data-ttu-id="aa3d8-128">Les points de terminaison extraient simplement les données de chaque trafic réseau visible par un appareil intégré.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-128">Endpoints will simply extract data from every network traffic that is seen by an onboarded device.</span></span> 

### <a name="standard-discovery"></a><span data-ttu-id="aa3d8-129">Découverte standard</span><span class="sxs-lookup"><span data-stu-id="aa3d8-129">Standard discovery</span></span> 

<span data-ttu-id="aa3d8-130">Ce mode permet aux points de terminaison de sonder activement les appareils observés dans le réseau pour enrichir les données collectées, ce qui vous aide à créer un inventaire fiable et cohérent des appareils.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-130">This mode allows endpoints to actively probe observed devices in the network to enrich collected data - helping you build a reliable and coherent device inventory.</span></span> <span data-ttu-id="aa3d8-131">Le mode standard utilise l’analyse intelligente et active pour découvrir encore plus d’informations sur les appareils observés afin d’enrichir les informations d’appareil existantes.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-131">Standard mode uses smart, active probing to discover even more information about observed devices to enrich existing device information.</span></span>  

<span data-ttu-id="aa3d8-132">Lorsque le mode Standard est activé, une activité réseau minime et négligeable générée par le capteur de découverte peut être observée par les outils de surveillance réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-132">When Standard mode is enabled, minimal and negligible network activity generated by the discovery sensor might be observed by network monitoring tools in your organization.</span></span>  

 <span data-ttu-id="aa3d8-133">Si vous choisissez de ne pas activer ce mode, vous n’aurez qu’une visibilité limitée des points de terminaison nonmanagés dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-133">If you choose not to enable this mode, you will only gain limited visibility of unmanaged endpoints in your network.</span></span>

<span data-ttu-id="aa3d8-134">La découverte standard utilise divers scripts PowerShell pour sonder activement les périphériques du réseau.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-134">Standard discovery uses various PowerShell scripts to actively probe devices in the network.</span></span> <span data-ttu-id="aa3d8-135">Ces scripts PowerShell sont signés par Microsoft et sont exécutés à partir de l’emplacement suivant `C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\*.ps` :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-135">Those PowerShell scripts are Microsoft signed and are executed from the following location: `C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\*.ps`.</span></span> <span data-ttu-id="aa3d8-136">Par exemple, `C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\UnicastScannerV1.1.0.ps1`.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-136">For example, `C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\UnicastScannerV1.1.0.ps1`.</span></span>

<span data-ttu-id="aa3d8-137">Vous pouvez modifier et personnaliser vos paramètres de découverte, pour plus d’informations, voir [Configurer la découverte d’appareils.](configure-device-discovery.md)</span><span class="sxs-lookup"><span data-stu-id="aa3d8-137">You can change and customize your discovery settings, for more information see [Configure device discovery](configure-device-discovery.md).</span></span>

> [!NOTE]
> <span data-ttu-id="aa3d8-138">Le moteur de découverte fait la distinction entre les événements réseau reçus dans le réseau d’entreprise et en dehors du réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-138">The discovery engine distinguishes between network events that are received in the corporate network versus outside of the corporate network.</span></span> <span data-ttu-id="aa3d8-139">Les appareils qui ne sont pas connectés à des réseaux d’entreprise ne seront pas découverts ou répertoriés dans l’inventaire des appareils.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-139">Devices that are not connected to corporate networks will not be discovered or listed in the device inventory.</span></span> 



## <a name="device-inventory"></a><span data-ttu-id="aa3d8-140">Inventaire des appareils</span><span class="sxs-lookup"><span data-stu-id="aa3d8-140">Device Inventory</span></span> 
<span data-ttu-id="aa3d8-141">Les appareils qui ont été découverts mais qui n’ont pas encore été intégrés et sécurisés par Microsoft Defender pour le point de terminaison sont répertoriés dans l’inventaire des appareils dans l’onglet Points de terminaison. Vous pouvez désormais utiliser un nouveau filtre dans la liste d’inventaire des appareils appelé État d’intégration, qui peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-141">Devices that have been discovered but have not yet been onboarded and secured by Microsoft Defender for Endpoint will be listed in Device Inventory within the Endpoints tab. You can now use a new filter in the device inventory list called Onboarding status which can have any of the following values:</span></span>

- <span data-ttu-id="aa3d8-142">Intégré : le point de terminaison est intégré à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-142">Onboarded – The endpoint is onboarded to Microsoft Defender for Endpoint.</span></span>
- <span data-ttu-id="aa3d8-143">Peut être intégré : le point de terminaison a été découvert dans le réseau et le système d’exploitation a été identifié comme étant pris en charge par Microsoft Defender pour le point de terminaison, mais il n’est pas actuellement intégré.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-143">Can be onboarded – The endpoint was discovered in the network and the Operating System was identified as one that is supported by Microsoft Defender for Endpoint, but it is not currently onboarded.</span></span> <span data-ttu-id="aa3d8-144">Nous vous recommandons vivement d’intégrer ces appareils.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-144">We highly recommend onboarding these devices.</span></span>
- <span data-ttu-id="aa3d8-145">Non pris en charge : le point de terminaison a été découvert dans le réseau, mais n’est pas pris en charge par Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-145">Unsupported – The endpoint was discovered in the network but is not supported by Microsoft Defender for Endpoint.</span></span>
- <span data-ttu-id="aa3d8-146">Informations insuffisantes : le système n’a pas pu déterminer la prise en charge de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-146">Insufficient info – The system could not determine the supportability of the device.</span></span> <span data-ttu-id="aa3d8-147">L’activation de la découverte standard sur d’autres appareils du réseau peut enrichir les attributs découverts.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-147">Enabling standard discovery on more devices in the network can enrich the discovered attributes.</span></span> 
 

![Image du tableau de bord d’inventaire des appareils](images/2b62255cd3a9dd42f3219e437b956fb9.png)

> [!TIP]
> <span data-ttu-id="aa3d8-149">Vous pouvez toujours appliquer des filtres pour exclure les appareils nonmanagés de la liste d’inventaire des appareils.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-149">You can always apply filters to exclude unmanaged devices from the device inventory list.</span></span> <span data-ttu-id="aa3d8-150">Vous pouvez également utiliser la colonne d’état d’intégration sur les requêtes API pour filtrer les appareils nonmanagés.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-150">You can also use the onboarding status column on API queries to filter out unmanaged devices.</span></span> 

## <a name="vulnerability-assessment-on-discovered-devices"></a><span data-ttu-id="aa3d8-151">Évaluation de la vulnérabilité sur les appareils détectés</span><span class="sxs-lookup"><span data-stu-id="aa3d8-151">Vulnerability assessment on discovered devices</span></span>
<span data-ttu-id="aa3d8-152">Les vulnérabilités et les risques sur vos appareils, ainsi que d’autres périphériques non utilisés détectés dans le réseau font partie des flux TVM actuels sous « Security Recommandations » et représentés dans les pages d’entité sur le portail.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-152">Vulnerabilities and risks on your devices as well as other discovered unmanaged devices in the network are part of the current TVM flows under "Security Recommendations" and represented in entity pages across the portal.</span></span> <span data-ttu-id="aa3d8-153">Recherchez les recommandations de sécurité « SSH » pour rechercher les vulnérabilités SSH liées aux appareils non gérés et gérés.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-153">Search for "SSH" related security recommendations to find SSH vulnerabilities that are related for unmanaged and managed devices.</span></span> 

![Image du tableau de bord recommandations en matière de sécurité](images/1156c82ffadd356ce329d1cf551e806c.png)  

## <a name="use-advanced-hunting-on-discovered-devices"></a><span data-ttu-id="aa3d8-155">Utiliser le service de recherche avancée sur les appareils détectés</span><span class="sxs-lookup"><span data-stu-id="aa3d8-155">Use Advanced Hunting on discovered devices</span></span>
<span data-ttu-id="aa3d8-156">Vous pouvez utiliser des requêtes de recherche avancée pour obtenir une visibilité sur les appareils détectés.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-156">You can use Advanced Hunting queries to gain visibility on discovered devices.</span></span>
<span data-ttu-id="aa3d8-157">Recherchez des détails sur les points de terminaison détectés dans la table DeviceInfo ou des informations réseau sur ces appareils dans la table DeviceNetworkInfo.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-157">Find details about discovered Endpoints in the DeviceInfo table, or network-related information about those devices in the DeviceNetworkInfo table.</span></span>
  

![Image de l’utilisation avancée du chasse](images/f48ba1779eddee9872f167453c24e5c9.png)


<span data-ttu-id="aa3d8-159">La découverte d’appareils tire parti de Microsoft Defender pour les appareils intégrés au point de terminaison en tant que source de données réseau pour attribuer des activités à des appareils non intégrés.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-159">Device discovery leverages Microsoft Defender for Endpoint onboarded devices as a network data source to attribute activities to non-onboarded devices.</span></span> <span data-ttu-id="aa3d8-160">Cela signifie que si un appareil intégré De Microsoft Defender pour point de terminaison a communiqué avec un appareil non intégré, les activités sur l’appareil non intégré peuvent être visibles sur la chronologie et via la table DeviceNetworkEvents de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-160">This means that if a Microsoft Defender for Endpoint onboarded device communicated with a non-onboarded device, activities on the non-onboarded device can be seen on the timeline and through the Advanced hunting DeviceNetworkEvents table.</span></span> 



<span data-ttu-id="aa3d8-161">Les nouveaux événements sont basés sur les connexions TCP (Transmission Control Protocol) et s’adaptent au schéma DeviceNetworkEvents actuel.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-161">New events are Transmission Control Protocol (TCP) connections-based and will fit to the current DeviceNetworkEvents scheme.</span></span> <span data-ttu-id="aa3d8-162">L’entrée TCP vers l’appareil Microsoft Defender pour point de terminaison activé à partir d’un autre que Microsoft Defender pour point de terminaison est activée.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-162">TCP ingress to the Microsoft Defender for Endpoint enabled device from a non-Microsoft Defender for Endpoint enabled.</span></span>  

<span data-ttu-id="aa3d8-163">Les types d’action suivants ont également été ajoutés :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-163">The following action types have also been added:</span></span>  

- <span data-ttu-id="aa3d8-164">ConnectionAttempt : tentative d’établissement d’une connexion TCP (syn)</span><span class="sxs-lookup"><span data-stu-id="aa3d8-164">ConnectionAttempt - An attempt to establish a TCP connection (syn)</span></span>  
- <span data-ttu-id="aa3d8-165">ConnectionAcknowledged : accusé de réception de l’acceptation d’une connexion TCP (syn\ack)</span><span class="sxs-lookup"><span data-stu-id="aa3d8-165">ConnectionAcknowledged - An acknowledgment that a TCP connection was accepted (syn\ack)</span></span>  

<span data-ttu-id="aa3d8-166">Vous pouvez essayer cette requête d’exemple :</span><span class="sxs-lookup"><span data-stu-id="aa3d8-166">You can try this example query:</span></span>  

```
DeviceNetworkEvents  
| where ActionType == "ConnectionAcknowledged" or ActionType == "ConnectionAttempt"  
| take 10  
```


## <a name="changed-behavior"></a><span data-ttu-id="aa3d8-167">Comportement modifié</span><span class="sxs-lookup"><span data-stu-id="aa3d8-167">Changed behavior</span></span>
<span data-ttu-id="aa3d8-168">La section suivante répertorie les modifications que vous observerez dans Microsoft Defender pour le point de terminaison et/ou Microsoft 365 centre de sécurité lorsque cette fonctionnalité est activée.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-168">The following section lists the changes you'll observe in Microsoft Defender for Endpoint and/or Microsoft 365 Security Center when this capability is enabled.</span></span> 
 
1.  <span data-ttu-id="aa3d8-169">Les appareils qui ne sont pas intégrés à Microsoft Defender au point de terminaison sont censés apparaître dans l’inventaire des appareils, le recherche avancée et les requêtes API.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-169">Devices that are not onboarded to Microsoft Defender to Endpoint are expected to appear in the device inventory, advanced hunting, and API queries.</span></span> <span data-ttu-id="aa3d8-170">Cela peut augmenter considérablement la taille des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-170">This may significantly increase the size of query results.</span></span> 
    1. <span data-ttu-id="aa3d8-171">Les tables « DeviceInfo » et « DeviceNetworkInfo » dans la recherche avancée vont maintenant contenir l’appareil détecté.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-171">"DeviceInfo" and "DeviceNetworkInfo" tables in Advanced Hunting will now hold discovered device.</span></span> <span data-ttu-id="aa3d8-172">Vous pouvez filtrer ces appareils à l’aide de l’attribut « OnboardingStatus ».</span><span class="sxs-lookup"><span data-stu-id="aa3d8-172">You can filter out those devices by using “OnboardingStatus” attribute.</span></span>

    2. <span data-ttu-id="aa3d8-173">Les appareils détectés sont censés apparaître dans les résultats de requête de l’API de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-173">Discovered devices are expected to appear in Streaming API query results.</span></span> <span data-ttu-id="aa3d8-174">Vous pouvez filtrer ces appareils à l’aide `OnboardingStatus` du filtre dans votre requête.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-174">You can filter out those devices by using the `OnboardingStatus` filter in your query.</span></span> 

2.  <span data-ttu-id="aa3d8-175">Les appareils non utilisés seront affectés à des groupes d’appareils existants en fonction des critères définis.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-175">Unmanaged devices will be assigned to existing device groups based on the defined criteria.</span></span> 
3.  <span data-ttu-id="aa3d8-176">Dans de rares cas, la découverte standard peut déclencher des alertes sur les moniteurs réseau ou les outils de sécurité.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-176">In rare cases, Standard discovery might trigger alerts on network monitors or security tools.</span></span> <span data-ttu-id="aa3d8-177">Veuillez nous faire part de vos commentaires, si vous faites l’expérience de tels événements, afin d’éviter que ces problèmes ne se répètent.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-177">Please provide feedback, if you experience such events, to help prevent these issues from recurring.</span></span> <span data-ttu-id="aa3d8-178">Vous pouvez exclure explicitement des cibles spécifiques ou des sous-réseaux entiers d’être activement sondés par la découverte standard.</span><span class="sxs-lookup"><span data-stu-id="aa3d8-178">You can explicitly exclude specific targets or entire subnets from being actively probed by Standard discovery.</span></span> 



## <a name="next-steps"></a><span data-ttu-id="aa3d8-179">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="aa3d8-179">Next steps</span></span>
- [<span data-ttu-id="aa3d8-180">Configurer la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="aa3d8-180">Configure device discovery</span></span>](configure-device-discovery.md)
- [<span data-ttu-id="aa3d8-181">FAQ sur la découverte d’appareils</span><span class="sxs-lookup"><span data-stu-id="aa3d8-181">Device discovery FAQs</span></span>](device-discovery-faq.md)
