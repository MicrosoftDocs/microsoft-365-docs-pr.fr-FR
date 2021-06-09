---
title: Vérifier l’état d’état du capteur dans Microsoft Defender pour le point de terminaison
description: Vérifiez l’état du capteur sur les appareils pour identifier ceux qui sont mal configurés, inactifs ou qui ne rapportent pas de données de capteur.
keywords: capteur, état du capteur, mal configuré, inactif, aucune donnée de capteur, données du capteur, communications altérées, communication
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
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: 0361b7956339670d006c9f050274e07d4e979bca
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51904163"
---
# <a name="check-sensor-health-state-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="2c875-104">Vérifier l’état d’état du capteur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2c875-104">Check sensor health state in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2c875-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2c875-105">**Applies to:**</span></span>
- [<span data-ttu-id="2c875-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2c875-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2c875-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2c875-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="2c875-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="2c875-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="2c875-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2c875-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-checksensor-abovefoldlink)

<span data-ttu-id="2c875-110">La vignette **Appareils avec problèmes de** capteur se trouve dans le tableau de bord Opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2c875-110">The **Devices with sensor issues** tile is found on the Security Operations dashboard.</span></span> <span data-ttu-id="2c875-111">Cette vignette fournit des informations sur la capacité de chaque appareil à fournir des données de détection à communiquer avec le service Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2c875-111">This tile provides information on the individual device’s ability to provide sensor data and communicate with the Defender for Endpoint service.</span></span> <span data-ttu-id="2c875-112">Elle indique le nombre d’appareils qui nécessitent une attention particulière et vous aide à identifier les appareils problématiques et à prendre des mesures pour les corriger.</span><span class="sxs-lookup"><span data-stu-id="2c875-112">It reports how many devices require attention and helps you identify problematic devices and take action to correct known issues.</span></span>

<span data-ttu-id="2c875-113">Il existe deux indicateurs d’état sur la vignette qui fournissent des informations sur le nombre d’appareils qui ne sont pas correctement signalés au service :</span><span class="sxs-lookup"><span data-stu-id="2c875-113">There are two status indicators on the tile that provide information on the number of devices that are not reporting properly to the service:</span></span>
- <span data-ttu-id="2c875-114">**Mal configuré :** ces appareils peuvent signaler partiellement des données de capteur au service Defender for Endpoint et peuvent avoir des erreurs de configuration qui doivent être corrigées.</span><span class="sxs-lookup"><span data-stu-id="2c875-114">**Misconfigured** - These devices might partially be reporting sensor data to the Defender for Endpoint service and might have configuration errors that need to be corrected.</span></span>
- <span data-ttu-id="2c875-115">**Inactif** : appareils qui ont cessé de signaler au service Defender for Endpoint pendant plus de sept jours au cours du mois précédent.</span><span class="sxs-lookup"><span data-stu-id="2c875-115">**Inactive** - Devices that have stopped reporting to the Defender for Endpoint service for more than seven days in the past month.</span></span>

<span data-ttu-id="2c875-116">Le fait de cliquer sur l’un des groupes vous dirige vers la liste **Appareils,** filtrée en fonction de votre choix.</span><span class="sxs-lookup"><span data-stu-id="2c875-116">Clicking any of the groups directs you to **Devices list**, filtered according to your choice.</span></span>

![Capture d’écran de la vignette Appareils avec problèmes de capteur](images/atp-devices-with-sensor-issues-tile.png)

<span data-ttu-id="2c875-118">Dans **la liste Appareils,** vous pouvez filtrer la liste d’état en fonction de l’état suivant :</span><span class="sxs-lookup"><span data-stu-id="2c875-118">On **Devices list**, you can filter the health state list by the following status:</span></span>
- <span data-ttu-id="2c875-119">**Actif** : appareils qui font activement des rapports au service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c875-119">**Active** - Devices that are actively reporting to the Defender for Endpoint service.</span></span>
- <span data-ttu-id="2c875-120">**Mal configuré :** ces appareils peuvent partiellement signaler des données de capteur au service Defender for Endpoint, mais ont des erreurs de configuration qui doivent être corrigées.</span><span class="sxs-lookup"><span data-stu-id="2c875-120">**Misconfigured** - These devices might partially be reporting sensor data to the Defender for Endpoint service but have configuration errors that need to be corrected.</span></span> <span data-ttu-id="2c875-121">Les appareils mal configurés peuvent avoir l’un ou l’autre des problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="2c875-121">Misconfigured devices can have either one or a combination of the following issues:</span></span>
  - <span data-ttu-id="2c875-122">**Aucune donnée de capteur** : les appareils ont cessé d’envoyer des données de capteur.</span><span class="sxs-lookup"><span data-stu-id="2c875-122">**No sensor data** - Devices has stopped sending sensor data.</span></span> <span data-ttu-id="2c875-123">Des alertes limitées peuvent être déclenchées à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c875-123">Limited alerts can be triggered from the device.</span></span>
  - <span data-ttu-id="2c875-124">**Communications réduites** : la capacité de communication avec l’appareil est réduite.</span><span class="sxs-lookup"><span data-stu-id="2c875-124">**Impaired communications** - Ability to communicate with device is impaired.</span></span> <span data-ttu-id="2c875-125">Il est possible que l'envoi de fichiers pour une analyse approfondie, le blocage de fichiers, l'isolement de l'appareil du réseau et d'autres actions qui nécessitent une communication avec l'appareil ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="2c875-125">Sending files for deep analysis, blocking files, isolating device from network and other actions that require communication with the device may not work.</span></span>
- <span data-ttu-id="2c875-126">**Inactif** : appareils qui ont cessé de signaler au service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c875-126">**Inactive** - Devices that have stopped reporting to the Defender for Endpoint service.</span></span>

<span data-ttu-id="2c875-127">Vous pouvez également télécharger la liste entière au format CSV à l’aide de la **fonctionnalité d’exportation.**</span><span class="sxs-lookup"><span data-stu-id="2c875-127">You can also download the entire list in CSV format using the **Export** feature.</span></span> <span data-ttu-id="2c875-128">Pour plus d’informations sur les filtres, voir [Afficher et organiser la liste des appareils.](machines-view-overview.md)</span><span class="sxs-lookup"><span data-stu-id="2c875-128">For more information on filters, see [View and organize the Devices list](machines-view-overview.md).</span></span>

>[!NOTE]
><span data-ttu-id="2c875-129">Exportez la liste au format CSV pour afficher les données non filtrées.</span><span class="sxs-lookup"><span data-stu-id="2c875-129">Export the list in CSV format to display the unfiltered data.</span></span> <span data-ttu-id="2c875-130">Le fichier CSV inclut tous les appareils de l’organisation, quel que soit le filtrage appliqué dans l’affichage lui-même et peut prendre beaucoup de temps à télécharger, en fonction de la taille de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2c875-130">The CSV file will include all devices in the organization, regardless of any filtering applied in the view itself and can take a significant amount of time to download, depending on how large your organization is.</span></span>

![Capture d’écran de la page liste Appareils](images/atp-devices-list-page.png)

<span data-ttu-id="2c875-132">Vous pouvez afficher les détails de l’appareil lorsque vous cliquez sur un appareil mal configuré ou inactif.</span><span class="sxs-lookup"><span data-stu-id="2c875-132">You can view the device details when you click on a misconfigured or inactive device.</span></span>

## <a name="related-topic"></a><span data-ttu-id="2c875-133">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="2c875-133">Related topic</span></span>
- [<span data-ttu-id="2c875-134">Corriger les capteurs défectueux dans Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2c875-134">Fix unhealthy sensors in Defender for Endpoint</span></span>](fix-unhealthy-sensors.md)
