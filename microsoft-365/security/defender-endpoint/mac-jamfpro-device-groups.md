---
title: Configurer des groupes d'appareils dans Jamf Pro
description: Découvrez comment configurer des groupes d'appareils dans Jamf Pro pour Microsoft Defender ATP pour macOS
keywords: device, group, microsoft, defender, atp, mac, installation, deploy, uninstallation, intune, jamfpro, macos,pépé, mojave, high sierra
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
ms.openlocfilehash: 6c1d6ae5d4635186bf0a1cbb55c7f906e8584f01
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689688"
---
# <a name="set-up-microsoft-defender-for-endpoint-on-macos-device-groups-in-jamf-pro"></a><span data-ttu-id="f55e3-104">Configurer Microsoft Defender pour le point de terminaison sur les groupes d'appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="f55e3-104">Set up Microsoft Defender for Endpoint on macOS device groups in Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f55e3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f55e3-105">**Applies to:**</span></span>
- [<span data-ttu-id="f55e3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f55e3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f55e3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f55e3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f55e3-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f55e3-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f55e3-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f55e3-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="f55e3-110">Configurer les groupes d'appareils semblables aux groupes d'organisation de stratégie de groupe, à la collection d'appareils de Microsoft Endpoint Configuration Manager et aux groupes d'appareils d'Intune.</span><span class="sxs-lookup"><span data-stu-id="f55e3-110">Set up the device groups similar to Group policy  organizational unite (OUs), Microsoft Endpoint Configuration Manager's device collection, and Intune's device groups.</span></span>

1. <span data-ttu-id="f55e3-111">Accédez à **Groupes d'ordinateurs statiques.**</span><span class="sxs-lookup"><span data-stu-id="f55e3-111">Navigate to **Static Computer Groups**.</span></span>

2. <span data-ttu-id="f55e3-112">Sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f55e3-112">Select **New**.</span></span> 

    ![Image de Jamf Pro1](images/jamf-pro-static-group.png)

3. <span data-ttu-id="f55e3-114">Fournissez un nom d'affichage et sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="f55e3-114">Provide a display name and select **Save**.</span></span>

    ![Image de Jamf Pro2](images/jamfpro-machine-group.png)

4. <span data-ttu-id="f55e3-116">Vous verrez maintenant le groupe **d'ordinateurs de Contoso** sous **Groupes d'ordinateurs statiques.**</span><span class="sxs-lookup"><span data-stu-id="f55e3-116">Now you will see the **Contoso's Machine Group** under **Static Computer Groups**.</span></span>

    ![Image de Jamf Pro3](images/contoso-machine-group.png)

## <a name="next-step"></a><span data-ttu-id="f55e3-118">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="f55e3-118">Next step</span></span>
- [<span data-ttu-id="f55e3-119">Configurer Microsoft Defender pour endpoint sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="f55e3-119">Set up Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>](mac-jamfpro-policies.md)
