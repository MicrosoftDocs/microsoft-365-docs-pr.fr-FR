---
title: Résoudre les problèmes d’extension du noyau dans Microsoft Defender pour Endpoint pour Mac
description: Résoudre les problèmes liés à l’extension du noyau dans Microsoft Defender pour Endpoint pour Mac.
keywords: microsoft, defender, atp, mac, noyau, extension
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
ms.openlocfilehash: 877cc619d3ba048cdf6ecc8149f073461d9eac8e
ms.sourcegitcommit: a965c498e6b3890877f895d5197898b306092813
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51379507"
---
# <a name="troubleshoot-kernel-extension-issues-in-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="a067f-104">Résoudre les problèmes d’extension du noyau dans Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="a067f-104">Troubleshoot kernel extension issues in Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="a067f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a067f-105">**Applies to:**</span></span>

- [<span data-ttu-id="a067f-106">Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="a067f-106">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="a067f-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a067f-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="a067f-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a067f-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="a067f-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="a067f-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="a067f-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a067f-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="a067f-111">Cet article fournit des informations sur la résolution des problèmes avec l’extension de noyau installée dans le cadre de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="a067f-111">This article provides information on how to troubleshoot issues with the kernel extension that is installed as part of Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="a067f-112">À partir de macOS High Sierra (10.13), macOS exige que toutes les extensions de noyau soient approuvées explicitement avant d’être autorisées à s’exécuter sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a067f-112">Starting with macOS High Sierra (10.13), macOS requires all kernel extensions to be explicitly approved before they're allowed to run on the device.</span></span>

<span data-ttu-id="a067f-113">Si vous n’avez pas approuvé l’extension du noyau pendant le déploiement/l’installation de Microsoft Defender pour Endpoint pour Mac, l’application affiche une bannière vous invite à l’activer :</span><span class="sxs-lookup"><span data-stu-id="a067f-113">If you didn't approve the kernel extension during the deployment/installation of Microsoft Defender for Endpoint for Mac, the application displays a banner prompting you to enable it:</span></span>

   ![Capture d’écran rtp désactivée](images/mdatp-32-main-app-fix.png)

<span data-ttu-id="a067f-115">Vous pouvez également exécuter ```mdatp health``` .</span><span class="sxs-lookup"><span data-stu-id="a067f-115">You can also run ```mdatp health```.</span></span> <span data-ttu-id="a067f-116">Il indique si la protection en temps réel est activée mais non disponible.</span><span class="sxs-lookup"><span data-stu-id="a067f-116">It reports if real-time protection is enabled but not available.</span></span> <span data-ttu-id="a067f-117">Cela indique que l’extension du noyau n’est pas approuvée pour s’exécuter sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="a067f-117">This indicates that the kernel extension isn't approved to run on your device.</span></span>

```bash
mdatp health
```
```Output
...
real_time_protection_enabled                : false
real_time_protection_available              : true
...
```

<span data-ttu-id="a067f-118">Les sections suivantes fournissent des instructions sur la façon de résoudre ce problème, en fonction de la méthode que vous avez utilisée pour déployer Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="a067f-118">The following sections provide guidance on how to address this issue, depending on the method that you used to deploy Microsoft Defender for Endpoint for Mac.</span></span>

## <a name="managed-deployment"></a><span data-ttu-id="a067f-119">Déploiement géré</span><span class="sxs-lookup"><span data-stu-id="a067f-119">Managed deployment</span></span>

<span data-ttu-id="a067f-120">Consultez les instructions correspondant à l’outil de gestion que vous avez utilisé pour déployer le produit :</span><span class="sxs-lookup"><span data-stu-id="a067f-120">See the instructions corresponding to the management tool that you used to deploy the product:</span></span>

- [<span data-ttu-id="a067f-121">Déploiement basé sur JAMF</span><span class="sxs-lookup"><span data-stu-id="a067f-121">JAMF-based deployment</span></span>](mac-install-with-jamf.md)
- [<span data-ttu-id="a067f-122">Déploiement basé sur Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a067f-122">Microsoft Intune-based deployment</span></span>](mac-install-with-intune.md#create-system-configuration-profiles)

## <a name="manual-deployment"></a><span data-ttu-id="a067f-123">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="a067f-123">Manual deployment</span></span>

<span data-ttu-id="a067f-124">Si moins de 30 minutes se sont écoulées depuis l’installation du produit, accédez à La sécurité des préférences système & Confidentialité , où vous devez autoriser les **logiciels** système des développeurs  >  « Microsoft Corporation ». </span><span class="sxs-lookup"><span data-stu-id="a067f-124">If less than 30 minutes have passed since the product was installed, navigate to **System Preferences** > **Security & Privacy**, where you have to **Allow** system software from developers "Microsoft Corporation".</span></span>

<span data-ttu-id="a067f-125">Si vous ne voyez pas cette invite, cela signifie que 30 minutes ou plus se sont écoulées et que l’extension du noyau n’a toujours pas été approuvée pour s’exécuter sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="a067f-125">If you don't see this prompt, it means that 30 or more minutes have passed, and the kernel extension still not been approved to run on your device:</span></span>

![Fenêtre de sécurité et de confidentialité après la capture d’écran de l’invite expirée](images/mdatp-33-securityprivacysettings-noprompt.png)

<span data-ttu-id="a067f-127">Dans ce cas, vous devez effectuer les étapes suivantes pour déclencher à nouveau le flux d’approbation.</span><span class="sxs-lookup"><span data-stu-id="a067f-127">In this case, you need to perform the following steps to trigger the approval flow again.</span></span>

1. <span data-ttu-id="a067f-128">Dans Terminal, essayez d’installer le pilote.</span><span class="sxs-lookup"><span data-stu-id="a067f-128">In Terminal, attempt to install the driver.</span></span> <span data-ttu-id="a067f-129">L’opération suivante échoue, car l’extension du noyau n’a pas été approuvée pour s’exécuter sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a067f-129">The following operation will fail, because the kernel extension wasn't approved to run on the device.</span></span> <span data-ttu-id="a067f-130">Toutefois, il déclenche à nouveau le flux d’approbation.</span><span class="sxs-lookup"><span data-stu-id="a067f-130">However, it will trigger the approval flow again.</span></span>

    ```bash
    sudo kextutil /Library/Extensions/wdavkext.kext
    ```
    
    ```Output
    Kext rejected due to system policy: <OSKext 0x7fc34d528390 [0x7fffa74aa8e0]> { URL = "file:///Library/StagedExtensions/Library/Extensions/wdavkext.kext/", ID = "com.microsoft.wdavkext" }
    Kext rejected due to system policy: <OSKext 0x7fc34d528390 [0x7fffa74aa8e0]> { URL = "file:///Library/StagedExtensions/Library/Extensions/wdavkext.kext/", ID = "com.microsoft.wdavkext" }
    Diagnostics for /Library/Extensions/wdavkext.kext:
    ```

2. <span data-ttu-id="a067f-131">Ouvrez **La sécurité des préférences** système &  >  **confidentialité** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="a067f-131">Open **System Preferences** > **Security & Privacy** from the menu.</span></span> <span data-ttu-id="a067f-132">(Fermez-le d’abord, s’il est ouvert.)</span><span class="sxs-lookup"><span data-stu-id="a067f-132">(Close it first, if it's opened.)</span></span>

3. <span data-ttu-id="a067f-133">**Autoriser les** logiciels système des développeurs « Microsoft Corporation »</span><span class="sxs-lookup"><span data-stu-id="a067f-133">**Allow** system software from developers "Microsoft Corporation"</span></span>

4. <span data-ttu-id="a067f-134">Dans Terminal, installez à nouveau le pilote.</span><span class="sxs-lookup"><span data-stu-id="a067f-134">In Terminal, install the driver again.</span></span> <span data-ttu-id="a067f-135">Cette fois, l’opération réussit :</span><span class="sxs-lookup"><span data-stu-id="a067f-135">This time the operation will succeed:</span></span>

    ```bash
    sudo kextutil /Library/Extensions/wdavkext.kext
    ```

    <span data-ttu-id="a067f-136">La bannière doit disparaître de l’application Defender et doit maintenant signaler que la protection en temps réel est à la fois ```mdatp health``` activée et disponible :</span><span class="sxs-lookup"><span data-stu-id="a067f-136">The banner should disappear from the Defender application, and ```mdatp health``` should now report that real-time protection is both enabled and available:</span></span>

    ```bash
    mdatp health
    ```

    ```Output
    ...
    real_time_protection_enabled                : true
    real_time_protection_available              : true
    ...
    ```
