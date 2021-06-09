---
title: Configurer les Antivirus Microsoft Defender l’Microsoft Endpoint Manager
description: Utilisez les Microsoft Endpoint Manager et Microsoft Intune pour configurer l’Antivirus Microsoft Defender et les Endpoint Protection
keywords: scep, intune, endpoint protection, configuration
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 05/24/2021
ms.reviewer: phuijbr, oogunrinde
manager: dansimp
ms.technology: mde
audience: ITPro
ms.topic: how-to
ms.openlocfilehash: ab77f3ab5ac9385d1ce049061730d2192e3bcb0c
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683750"
---
# <a name="use-microsoft-endpoint-manager-to-configure-and-manage-microsoft-defender-antivirus"></a><span data-ttu-id="5046e-104">Utilisez Microsoft Endpoint Manager pour configurer et gérer les Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5046e-104">Use Microsoft Endpoint Manager to configure and manage Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="5046e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5046e-105">**Applies to:**</span></span>

- [<span data-ttu-id="5046e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5046e-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="5046e-107">Vous pouvez utiliser [Microsoft Endpoint Manager](/mem/endpoint-manager-overview) pour configurer des analyses Antivirus Microsoft Defender’analyse.</span><span class="sxs-lookup"><span data-stu-id="5046e-107">You can use [Microsoft Endpoint Manager](/mem/endpoint-manager-overview) to configure Microsoft Defender Antivirus scans.</span></span> <span data-ttu-id="5046e-108">[Microsoft Intune](/mem/intune/fundamentals/what-is-intune) configuration [Manager](/mem/configmgr/core/understand/introduction) font désormais partie de Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="5046e-108">[Microsoft Intune](/mem/intune/fundamentals/what-is-intune) and [Configuration Manager](/mem/configmgr/core/understand/introduction) are now part of Endpoint Manager.</span></span>  

## <a name="configure-microsoft-defender-antivirus-scans-in-endpoint-manager"></a><span data-ttu-id="5046e-109">Configurer des analyses Antivirus Microsoft Defender dans Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="5046e-109">Configure Microsoft Defender Antivirus scans in Endpoint Manager</span></span>

1. <span data-ttu-id="5046e-110">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ), and sign in.</span><span class="sxs-lookup"><span data-stu-id="5046e-110">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), and sign in.</span></span>

2. <span data-ttu-id="5046e-111">Accédez **à Sécurité des points de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="5046e-111">Navigate to **Endpoint Security**.</span></span>

3. <span data-ttu-id="5046e-112">Under **Manage**, choose **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="5046e-112">Under **Manage**, choose **Antivirus**.</span></span>

4. <span data-ttu-id="5046e-113">Sélectionnez votre stratégie Antivirus Microsoft Defender de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5046e-113">Select your Microsoft Defender Antivirus policy.</span></span> 

5. <span data-ttu-id="5046e-114">Sous **Gérer**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5046e-114">Under **Manage**, choose **Properties**.</span></span>

6. <span data-ttu-id="5046e-115">Près de **Paramètres de configuration**, choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="5046e-115">Next to **Configuration settings**, choose **Edit**.</span></span>

7. <span data-ttu-id="5046e-116">Développez  la section Analyse, puis examinez ou modifiez vos paramètres d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5046e-116">Expand the **Scan** section, and review or edit your scanning settings.</span></span>

8. <span data-ttu-id="5046e-117">Choose **Review + save**</span><span class="sxs-lookup"><span data-stu-id="5046e-117">Choose **Review + save**</span></span>


> [!TIP]
> <span data-ttu-id="5046e-118">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="5046e-118">Need help?</span></span> <span data-ttu-id="5046e-119">Voir [Gérer la sécurité des points de terminaison dans Microsoft Intune](/mem/intune/protect/endpoint-security).</span><span class="sxs-lookup"><span data-stu-id="5046e-119">See [Manage endpoint security in Microsoft Intune](/mem/intune/protect/endpoint-security).</span></span>


## <a name="related-articles"></a><span data-ttu-id="5046e-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="5046e-120">Related articles</span></span>

- [<span data-ttu-id="5046e-121">Articles de référence pour les outils de gestion et de configuration</span><span class="sxs-lookup"><span data-stu-id="5046e-121">Reference articles for management and configuration tools</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="5046e-122">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="5046e-122">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)