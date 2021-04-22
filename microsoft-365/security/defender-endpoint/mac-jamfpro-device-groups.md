---
title: Configurer des groupes d'appareils dans Jamf Pro
description: Découvrez comment configurer des groupes d'appareils dans Jamf Pro pour Microsoft Defender pour Endpoint sur macOS
keywords: device, group, microsoft, defender, Microsoft Defender for Endpoint, mac, installation, deploy, uninstallation, intune, jamfpro, macos,péra, mojave, high sierra
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
ms.openlocfilehash: 772b67ec84ae9614c9322763c140a60e7884644d
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933804"
---
# <a name="set-up-microsoft-defender-for-endpoint-on-macos-device-groups-in-jamf-pro"></a><span data-ttu-id="3e70e-104">Configurer Microsoft Defender pour le point de terminaison sur les groupes d'appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="3e70e-104">Set up Microsoft Defender for Endpoint on macOS device groups in Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3e70e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3e70e-105">**Applies to:**</span></span>
- [<span data-ttu-id="3e70e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e70e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3e70e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3e70e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3e70e-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3e70e-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3e70e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3e70e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="3e70e-110">Configurer les groupes d'appareils semblables aux groupes d'organisation de stratégie de groupe, à la collection d'appareils de Microsoft Endpoint Configuration Manager et aux groupes d'appareils d'Intune.</span><span class="sxs-lookup"><span data-stu-id="3e70e-110">Set up the device groups similar to Group policy  organizational unite (OUs), Microsoft Endpoint Configuration Manager's device collection, and Intune's device groups.</span></span>

1. <span data-ttu-id="3e70e-111">Accédez à **Groupes d'ordinateurs statiques.**</span><span class="sxs-lookup"><span data-stu-id="3e70e-111">Navigate to **Static Computer Groups**.</span></span>

2. <span data-ttu-id="3e70e-112">Sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="3e70e-112">Select **New**.</span></span> 

    ![Image de Jamf Pro1](images/jamf-pro-static-group.png)

3. <span data-ttu-id="3e70e-114">Fournissez un nom d'affichage et sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3e70e-114">Provide a display name and select **Save**.</span></span>

    ![Image de Jamf Pro2](images/jamfpro-machine-group.png)

4. <span data-ttu-id="3e70e-116">Vous verrez maintenant le groupe **d'ordinateurs de Contoso** sous **Groupes d'ordinateurs statiques.**</span><span class="sxs-lookup"><span data-stu-id="3e70e-116">Now you will see the **Contoso's Machine Group** under **Static Computer Groups**.</span></span>

    ![Image de Jamf Pro3](images/contoso-machine-group.png)

## <a name="next-step"></a><span data-ttu-id="3e70e-118">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3e70e-118">Next step</span></span>
- [<span data-ttu-id="3e70e-119">Configurer Microsoft Defender pour endpoint sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="3e70e-119">Set up Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>](mac-jamfpro-policies.md)
