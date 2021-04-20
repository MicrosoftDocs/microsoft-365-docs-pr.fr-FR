---
title: Protéger les données de votre organisation avec le contrôle d'appareil
description: Surveillez la sécurité des données de votre organisation via des rapports de contrôle des appareils.
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
ms.author: dansimp
author: dansimp
ms.reviewer: dansimp
ms.topic: article
manager: dansimp
audience: ITPro
ms.technology: mde
ms.openlocfilehash: ee8e7be20076bde41867981008e53a70c134e47e
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893724"
---
# <a name="protect-your-organizations-data-with-device-control"></a><span data-ttu-id="17421-103">Protéger les données de votre organisation avec le contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="17421-103">Protect your organization’s data with device control</span></span>

<span data-ttu-id="17421-104">**S'applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2069559)</span><span class="sxs-lookup"><span data-stu-id="17421-104">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2069559)</span></span>

<span data-ttu-id="17421-105">Le contrôle d'appareil Microsoft Defender pour points de terminaison protège contre la perte de données en surveillant et en contrôlant l'utilisation des supports par les appareils de votre organisation, tels que l'utilisation de périphériques de stockage amovibles et de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="17421-105">Microsoft Defender for Endpoint device control protects against data loss, by monitoring and controlling media use by devices in your organization, such as the use of removable storage devices and USB drives.</span></span>

<span data-ttu-id="17421-106">Avec le rapport de contrôle d'appareil, vous pouvez afficher les événements liés à l'utilisation des médias, tels que :</span><span class="sxs-lookup"><span data-stu-id="17421-106">With the device control report, you can view events that relate to media usage, such as:</span></span>

- <span data-ttu-id="17421-107">**Événements d'audit :** Indique le nombre d'événements d'audit qui se produisent lorsque des médias externes sont connectés.</span><span class="sxs-lookup"><span data-stu-id="17421-107">**Audit events:** Shows the number of audit events that occur when external media is connected.</span></span>
- <span data-ttu-id="17421-108">**Événements de stratégie :** Indique le nombre d'événements de stratégie qui se produisent lorsqu'une stratégie de contrôle d'appareil est déclenchée.</span><span class="sxs-lookup"><span data-stu-id="17421-108">**Policy events:** Shows the number of policy events that occur when a device control policy is triggered.</span></span>

> [!NOTE]
> <span data-ttu-id="17421-109">L'événement d'audit permettant de suivre l'utilisation des médias est activé par défaut pour les appareils intégrés à Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="17421-109">The audit event to track media usage is enabled by default for devices onboarded to Microsoft Defender for Endpoint.</span></span>

## <a name="understanding-the-audit-events"></a><span data-ttu-id="17421-110">Comprendre les événements d'audit</span><span class="sxs-lookup"><span data-stu-id="17421-110">Understanding the audit events</span></span>

<span data-ttu-id="17421-111">Les événements d'audit sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="17421-111">The audit events include:</span></span>

- <span data-ttu-id="17421-112">**Montage et démontage du lecteur USB :** Auditer les événements générés lorsqu'un lecteur USB est monté ou démonté.</span><span class="sxs-lookup"><span data-stu-id="17421-112">**USB drive mount and unmount:** Audit events that are generated when a USB drive is mounted or unmounted.</span></span>
- <span data-ttu-id="17421-113">**PnP :** Les événements d'audit plug-and-play sont générés lorsque le stockage amovible, une imprimante ou Bluetooth multimédia est connecté.</span><span class="sxs-lookup"><span data-stu-id="17421-113">**PnP:** Plug and Play audit events are generated when removable storage, a printer, or Bluetooth media is connected.</span></span>

## <a name="monitor-device-control-security"></a><span data-ttu-id="17421-114">Surveiller la sécurité des contrôles d'appareil</span><span class="sxs-lookup"><span data-stu-id="17421-114">Monitor device control security</span></span>

<span data-ttu-id="17421-115">Le contrôle d'appareil dans Microsoft Defender pour point de terminaison permet aux administrateurs de sécurité d'utiliser des outils qui leur permettent de suivre la sécurité des contrôles d'appareil de leur organisation via des rapports.</span><span class="sxs-lookup"><span data-stu-id="17421-115">Device control in Microsoft Defender for Endpoint empowers security administrators with tools that enable them to track their organization’s device control security through reports.</span></span> <span data-ttu-id="17421-116">Vous pouvez trouver le rapport de contrôle d'appareil dans le Centre de sécurité Microsoft 365 en allant à **Rapports > protection des appareils.**</span><span class="sxs-lookup"><span data-stu-id="17421-116">You can find the device control report in the Microsoft 365 security center by going to **Reports > Device protection**.</span></span>

<span data-ttu-id="17421-117">La carte de  protection des appareils du tableau de bord Rapports indique le nombre d'événements d'audit générés par type de média au cours des 180 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="17421-117">The Device protection card on the **Reports** dashboard shows the number of audit events generated by media type, over the last 180 days.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="17421-118">![DeviceControlReportCard](images/devicecontrolcard.png)</span><span class="sxs-lookup"><span data-stu-id="17421-118">![DeviceControlReportCard](images/devicecontrolcard.png)</span></span>

<span data-ttu-id="17421-119">Le **bouton Afficher les détails** affiche davantage de données d'utilisation des médias dans la page de rapport de contrôle **d'appareil.**</span><span class="sxs-lookup"><span data-stu-id="17421-119">The **View details** button shows more media usage data in the **device control report** page.</span></span>

<span data-ttu-id="17421-120">La page fournit un tableau de bord avec un nombre agrégé d'événements par type et une liste d'événements.</span><span class="sxs-lookup"><span data-stu-id="17421-120">The page provides a dashboard with aggregated number of events per type and a list of events.</span></span> <span data-ttu-id="17421-121">Les administrateurs peuvent filtrer sur la plage de temps, le nom de la classe multimédia et l'ID de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="17421-121">Administrators can filter on time range, media class name, and device ID.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="17421-122">![DeviceControlReportDetails](images/Detaileddevicecontrolreport.png)</span><span class="sxs-lookup"><span data-stu-id="17421-122">![DeviceControlReportDetails](images/Detaileddevicecontrolreport.png)</span></span>

<span data-ttu-id="17421-123">Lorsque vous sélectionnez un événement, un flyout s'affiche pour vous fournir plus d'informations :</span><span class="sxs-lookup"><span data-stu-id="17421-123">When you select an event, a flyout appears that shows you more information:</span></span>

- <span data-ttu-id="17421-124">**Détails généraux :** Date, mode Action et stratégie de cet événement.</span><span class="sxs-lookup"><span data-stu-id="17421-124">**General details:** Date, Action mode, and the policy of this event.</span></span>
- <span data-ttu-id="17421-125">**Informations multimédias :** Les informations multimédias incluent le nom du média, le nom de classe, le GUID de classe, l'ID de périphérique, l'ID du fournisseur, le volume, le numéro de série et le type de bus.</span><span class="sxs-lookup"><span data-stu-id="17421-125">**Media information:** Media information includes Media name, Class name, Class GUID, Device ID, Vendor ID, Volume, Serial number, and Bus type.</span></span>
- <span data-ttu-id="17421-126">**Détails de l'emplacement :** Nom de l'appareil et ID de l'appareil MDATP.</span><span class="sxs-lookup"><span data-stu-id="17421-126">**Location details:** Device name and MDATP device ID.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="17421-127">![FilterOnDeviceControlReport](images/devicecontrolreportfilter.png)</span><span class="sxs-lookup"><span data-stu-id="17421-127">![FilterOnDeviceControlReport](images/devicecontrolreportfilter.png)</span></span>

<span data-ttu-id="17421-128">Pour voir l'activité en temps réel de ce média au sein de l'organisation, sélectionnez le bouton de recherche **Open Advanced.**</span><span class="sxs-lookup"><span data-stu-id="17421-128">To see real-time activity for this media across the organization, select the **Open Advanced hunting** button.</span></span> <span data-ttu-id="17421-129">Cela inclut une requête prédéfinie incorporée.</span><span class="sxs-lookup"><span data-stu-id="17421-129">This includes an embedded, pre-defined query.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="17421-130">![QueryOnDeviceControlReport](images/Devicecontrolreportquery.png)</span><span class="sxs-lookup"><span data-stu-id="17421-130">![QueryOnDeviceControlReport](images/Devicecontrolreportquery.png)</span></span>

<span data-ttu-id="17421-131">Pour voir la sécurité de l'appareil, sélectionnez le bouton Ouvrir la page de **l'appareil** dans le volant.</span><span class="sxs-lookup"><span data-stu-id="17421-131">To see the security of the device, select the **Open device page** button on the flyout.</span></span> <span data-ttu-id="17421-132">Ce bouton ouvre la page d'entité de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="17421-132">This button opens the device entity page.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="17421-133">![DeviceEntityPage](images/Devicesecuritypage.png)</span><span class="sxs-lookup"><span data-stu-id="17421-133">![DeviceEntityPage](images/Devicesecuritypage.png)</span></span>

## <a name="reporting-delays"></a><span data-ttu-id="17421-134">Signalement des retards</span><span class="sxs-lookup"><span data-stu-id="17421-134">Reporting delays</span></span>

<span data-ttu-id="17421-135">Le rapport de contrôle d'appareil peut avoir un délai de 12 heures entre le moment où une connexion multimédia se produit et le moment où l'événement est reflété dans la carte ou dans la liste des domaines.</span><span class="sxs-lookup"><span data-stu-id="17421-135">The device control report can have a 12-hour delay from the time a media connection occurs to the time the event is reflected in the card or in the domain list.</span></span>
