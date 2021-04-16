---
title: Déploiement de Microsoft Defender pour endpoint pour macOS avec Jamf Pro
description: Déploiement de Microsoft Defender pour endpoint pour macOS avec Jamf Pro
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamfpro, macos,pérable, mojave, high sierra
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
ms.openlocfilehash: e49a56b138e792f06229345d19a5867c9f6438af
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51862258"
---
# <a name="deploying-microsoft-defender-for-endpoint-on-macos-with-jamf-pro"></a><span data-ttu-id="1a248-104">Déploiement de Microsoft Defender pour endpoint sur macOS avec Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="1a248-104">Deploying Microsoft Defender for Endpoint on macOS with Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1a248-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1a248-105">**Applies to:**</span></span>
- [<span data-ttu-id="1a248-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1a248-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1a248-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1a248-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="1a248-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1a248-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1a248-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1a248-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="1a248-110">Découvrez comment déployer Microsoft Defender pour Endpoint sur macOS avec Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="1a248-110">Learn how to deploy Microsoft Defender for Endpoint on macOS with Jamf Pro.</span></span>

> [!NOTE]
> <span data-ttu-id="1a248-111">Si vous utilisez macOS Fonctionnalité (10.15.4) ou des versions plus récentes de macOS, voir Nouveaux profils de configuration pour macOS Et les versions plus récentes de [macOS.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-sysext-policies)</span><span class="sxs-lookup"><span data-stu-id="1a248-111">If you are using macOS Catalina (10.15.4) or newer versions of macOS, see [New configuration profiles for macOS Catalina and newer versions of macOS](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-sysext-policies).</span></span>

<span data-ttu-id="1a248-112">Il s'agit d'un processus en plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="1a248-112">This is a multi step process.</span></span> <span data-ttu-id="1a248-113">Vous devez effectuer toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a248-113">You'll need to complete all of the following steps:</span></span>

- [<span data-ttu-id="1a248-114">Connexion au portail Jamf</span><span class="sxs-lookup"><span data-stu-id="1a248-114">Login to the Jamf Portal</span></span>](mac-install-jamfpro-login.md)
- [<span data-ttu-id="1a248-115">Configurer Microsoft Defender pour le point de terminaison sur les groupes d'appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="1a248-115">Setup the Microsoft Defender for Endpoint on macOS device groups in Jamf Pro</span></span>](mac-jamfpro-device-groups.md)
- [<span data-ttu-id="1a248-116">Configuration de Microsoft Defender pour le point de terminaison sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="1a248-116">Setup the Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>](mac-jamfpro-policies.md)
- [<span data-ttu-id="1a248-117">Inscrire Microsoft Defender pour le point de terminaison sur les appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="1a248-117">Enroll the Microsoft Defender for Endpoint on macOS devices into Jamf Pro</span></span>](mac-jamfpro-enroll-devices.md)




