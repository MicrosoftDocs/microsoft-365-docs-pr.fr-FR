---
title: Déploiement de Microsoft Defender pour endpoint sur macOS avec Jamf Pro
description: Déploiement de Microsoft Defender pour endpoint sur macOS avec Jamf Pro
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mac, installation, déployer, désinstallation, intune, jamfpro, macos, magasin, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: b41c5ec827e110e0101c50ce7babeb6442096edb
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842889"
---
# <a name="deploying-microsoft-defender-for-endpoint-on-macos-with-jamf-pro"></a><span data-ttu-id="ea7c8-104">Déploiement de Microsoft Defender pour endpoint sur macOS avec Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="ea7c8-104">Deploying Microsoft Defender for Endpoint on macOS with Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ea7c8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ea7c8-105">**Applies to:**</span></span>
- [<span data-ttu-id="ea7c8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea7c8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ea7c8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea7c8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="ea7c8-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="ea7c8-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ea7c8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ea7c8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="ea7c8-110">Découvrez comment déployer Microsoft Defender pour Endpoint sur macOS avec Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="ea7c8-110">Learn how to deploy Microsoft Defender for Endpoint on macOS with Jamf Pro.</span></span>

> [!NOTE]
> <span data-ttu-id="ea7c8-111">Si vous utilisez macOS Souhaitez (10.15.4) ou des versions plus récentes de macOS, voir Nouveaux profils de configuration pour macOS Et les versions plus récentes de [macOS.](/microsoft-365/security/defender-endpoint/mac-sysext-policies)</span><span class="sxs-lookup"><span data-stu-id="ea7c8-111">If you are using macOS Catalina (10.15.4) or newer versions of macOS, see [New configuration profiles for macOS Catalina and newer versions of macOS](/microsoft-365/security/defender-endpoint/mac-sysext-policies).</span></span>

<span data-ttu-id="ea7c8-112">Il s’agit d’un processus en plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="ea7c8-112">This is a multi step process.</span></span> <span data-ttu-id="ea7c8-113">Vous devez effectuer toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea7c8-113">You'll need to complete all of the following steps:</span></span>

- [<span data-ttu-id="ea7c8-114">Connexion au portail Jamf</span><span class="sxs-lookup"><span data-stu-id="ea7c8-114">Login to the Jamf Portal</span></span>](mac-install-jamfpro-login.md)
- [<span data-ttu-id="ea7c8-115">Configurer Microsoft Defender pour le point de terminaison sur les groupes d’appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="ea7c8-115">Setup the Microsoft Defender for Endpoint on macOS device groups in Jamf Pro</span></span>](mac-jamfpro-device-groups.md)
- [<span data-ttu-id="ea7c8-116">Configuration de Microsoft Defender pour le point de terminaison sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="ea7c8-116">Setup the Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>](mac-jamfpro-policies.md)
- [<span data-ttu-id="ea7c8-117">Inscrivez Microsoft Defender for Endpoint sur les appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="ea7c8-117">Enroll the Microsoft Defender for Endpoint on macOS devices into Jamf Pro</span></span>](mac-jamfpro-enroll-devices.md)




