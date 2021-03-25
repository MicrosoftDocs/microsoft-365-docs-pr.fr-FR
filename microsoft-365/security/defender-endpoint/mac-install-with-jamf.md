---
title: Déploiement de Microsoft Defender ATP pour macOS avec Jamf Pro
description: Déploiement de Microsoft Defender ATP pour macOS avec Jamf Pro
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamfpro, macos,pépé, mojave, high sierra
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
ms.openlocfilehash: 56f5e860bd2a9dd47ce16379b5e1ca1a263d62d0
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187408"
---
# <a name="deploying-microsoft-defender-for-endpoint-for-macos-with-jamf-pro"></a><span data-ttu-id="9f77f-104">Déploiement de Microsoft Defender pour endpoint pour macOS avec Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="9f77f-104">Deploying Microsoft Defender for Endpoint for macOS with Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="9f77f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9f77f-105">**Applies to:**</span></span>
- [<span data-ttu-id="9f77f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9f77f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9f77f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9f77f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="9f77f-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="9f77f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9f77f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9f77f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="9f77f-110">Découvrez comment déployer Microsoft Defender pour endpoint pour macOS avec Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="9f77f-110">Learn how to deploy Microsoft Defender for Endpoint for macOS with Jamf Pro.</span></span>

> [!NOTE]
> <span data-ttu-id="9f77f-111">Si vous utilisez macOS Fonctionnalité (10.15.4) ou des versions plus récentes de macOS, voir Nouveaux profils de configuration pour macOS Et les versions plus récentes de [macOS.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-sysext-policies)</span><span class="sxs-lookup"><span data-stu-id="9f77f-111">If you are using macOS Catalina (10.15.4) or newer versions of macOS, see [New configuration profiles for macOS Catalina and newer versions of macOS](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-sysext-policies).</span></span>

<span data-ttu-id="9f77f-112">Il s’agit d’un processus en plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="9f77f-112">This is a multi step process.</span></span> <span data-ttu-id="9f77f-113">Vous devez effectuer toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f77f-113">You'll need to complete all of the following steps:</span></span>

- [<span data-ttu-id="9f77f-114">Connexion au portail Jamf</span><span class="sxs-lookup"><span data-stu-id="9f77f-114">Login to the Jamf Portal</span></span>](mac-install-jamfpro-login.md)
- [<span data-ttu-id="9f77f-115">Configuration de Microsoft Defender pour le point de terminaison pour les groupes d’appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="9f77f-115">Setup the Microsoft Defender for Endpoint for macOS device groups in Jamf Pro</span></span>](mac-jamfpro-device-groups.md)
- [<span data-ttu-id="9f77f-116">Configuration de Microsoft Defender pour le point de terminaison pour les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="9f77f-116">Setup the Microsoft Defender for Endpoint for macOS policies in Jamf Pro</span></span>](mac-jamfpro-policies.md)
- [<span data-ttu-id="9f77f-117">Inscrire Microsoft Defender pour le point de terminaison pour les appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="9f77f-117">Enroll the Microsoft Defender for Endpoint for macOS devices into Jamf Pro</span></span>](mac-jamfpro-enroll-devices.md)




