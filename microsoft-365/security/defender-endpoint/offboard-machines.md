---
title: Hors-carte des appareils à partir du service Microsoft Defender ATP
description: Intégrer des appareils Windows 10, des serveurs et des appareils autres que Windows à partir du service Microsoft Defender ATP
keywords: offboarding, microsoft defender for endpoint offboarding, windows atp offboarding
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
ms.technology: mde
ms.openlocfilehash: db22a19da58ba70ff09af781ca56e0b3c0d88dfd
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51061177"
---
# <a name="offboard-devices-from-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="438f2-104">Hors-carte des appareils à partir du service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="438f2-104">Offboard devices from the Microsoft Defender for Endpoint service</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="438f2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="438f2-105">**Applies to:**</span></span>
- [<span data-ttu-id="438f2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="438f2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="438f2-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="438f2-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="438f2-108">**Plateformes**</span><span class="sxs-lookup"><span data-stu-id="438f2-108">**Platforms**</span></span>
- <span data-ttu-id="438f2-109">macOS</span><span class="sxs-lookup"><span data-stu-id="438f2-109">macOS</span></span>
- <span data-ttu-id="438f2-110">Linux</span><span class="sxs-lookup"><span data-stu-id="438f2-110">Linux</span></span>
- <span data-ttu-id="438f2-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="438f2-111">Windows Server 2012 R2</span></span>
- <span data-ttu-id="438f2-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="438f2-112">Windows Server 2016</span></span>

><span data-ttu-id="438f2-113">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="438f2-113">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="438f2-114">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="438f2-114">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-offboarddevices-abovefoldlink)

<span data-ttu-id="438f2-115">Suivez les instructions correspondantes en fonction de votre méthode de déploiement préférée.</span><span class="sxs-lookup"><span data-stu-id="438f2-115">Follow the corresponding instructions depending on your preferred deployment method.</span></span>

>[!NOTE]
> <span data-ttu-id="438f2-116">L’état d’un appareil passe à [Inactif](fix-unhealthy-sensors.md#inactive-devices) 7 jours après laboardage.</span><span class="sxs-lookup"><span data-stu-id="438f2-116">The status of a device will be switched to [Inactive](fix-unhealthy-sensors.md#inactive-devices) 7 days after offboarding.</span></span> <br> <span data-ttu-id="438f2-117">Les données des appareils horsboard (par exemple, Chronologie, Alertes, Vulnérabilités, etc.) restent dans le portail jusqu’à l’expiration de la période de [rétention](data-storage-privacy.md#how-long-will-microsoft-store-my-data-what-is-microsofts-data-retention-policy) configurée.</span><span class="sxs-lookup"><span data-stu-id="438f2-117">Offboarded devices' data (such as Timeline, Alerts, Vulnerabilities, etc.) will remain in the portal until the configured [retention period](data-storage-privacy.md#how-long-will-microsoft-store-my-data-what-is-microsofts-data-retention-policy) expires.</span></span> <br>
> <span data-ttu-id="438f2-118">Le profil de l’appareil (sans [](machines-view-overview.md) données) reste dans la liste des appareils pendant 180 jours au plus.</span><span class="sxs-lookup"><span data-stu-id="438f2-118">The device's profile (without data) will remain in the [Devices List](machines-view-overview.md) for no longer than 180 days.</span></span>
> <span data-ttu-id="438f2-119">En outre, les appareils qui ne sont pas actifs au cours des 30 derniers jours ne sont pas factorés sur les données qui reflètent le [score](tvm-exposure-score.md) d’exposition de votre organisation en matière de gestion des menaces et des vulnérabilités et le Degré de sécurisation Microsoft pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="438f2-119">In addition, devices that are not active in the last 30 days are not factored in on the data that reflects your organization's threat and vulnerability management [exposure score](tvm-exposure-score.md) and Microsoft Secure Score for Devices.</span></span> <br>
> <span data-ttu-id="438f2-120">Pour afficher uniquement les appareils [](machines-view-overview.md#health-state)actifs, vous pouvez filtrer par état d’état d’état, [balises d’appareil](machine-tags.md) ou groupes [d’ordinateurs.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="438f2-120">To view only active devices, you can filter by [health state](machines-view-overview.md#health-state), [device tags](machine-tags.md) or [machine groups](machine-groups.md).</span></span> 

## <a name="offboard-windows-10-devices"></a><span data-ttu-id="438f2-121">Appareils Windows 10 hors windows 10</span><span class="sxs-lookup"><span data-stu-id="438f2-121">Offboard Windows 10 devices</span></span>
- [<span data-ttu-id="438f2-122">Hors-carte des appareils à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="438f2-122">Offboard devices using a local script</span></span>](configure-endpoints-script.md#offboard-devices-using-a-local-script)
- [<span data-ttu-id="438f2-123">Appareils de tableau de bord à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="438f2-123">Offboard devices using Group Policy</span></span>](configure-endpoints-gp.md#offboard-devices-using-group-policy)
- [<span data-ttu-id="438f2-124">Appareils de tableau de bord à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="438f2-124">Offboard devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md#offboard-and-monitor-devices-using-mobile-device-management-tools)

## <a name="offboard-servers"></a><span data-ttu-id="438f2-125">Serveurs horsboard</span><span class="sxs-lookup"><span data-stu-id="438f2-125">Offboard Servers</span></span>
- [<span data-ttu-id="438f2-126">Serveurs horsboard</span><span class="sxs-lookup"><span data-stu-id="438f2-126">Offboard servers</span></span>](configure-server-endpoints.md#offboard-windows-servers)

## <a name="offboard-non-windows-devices"></a><span data-ttu-id="438f2-127">Appareils non-Windows hors windows</span><span class="sxs-lookup"><span data-stu-id="438f2-127">Offboard non-Windows devices</span></span>
- [<span data-ttu-id="438f2-128">Appareils non-Windows hors windows</span><span class="sxs-lookup"><span data-stu-id="438f2-128">Offboard non-Windows devices</span></span>](configure-endpoints-non-windows.md#offboard-non-windows-devices)
