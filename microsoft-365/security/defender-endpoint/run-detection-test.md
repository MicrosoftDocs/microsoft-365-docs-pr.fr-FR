---
title: Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré
description: Exécutez le script de détection sur un appareil nouvellement intégré pour vérifier qu’il est correctement intégré au service Microsoft Defender for Endpoint.
keywords: test de détection, détection, powershell, script, vérifier, intégration, microsoft defender pour l’intégration de point de terminaison, clients, serveurs, test
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 2bb1fde1bfd8ddfa358d1141c3821843e532a8bf
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311999"
---
# <a name="run-a-detection-test-on-a-newly-onboarded-microsoft-defender-for-endpoint-device"></a><span data-ttu-id="e81d4-104">Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="e81d4-104">Run a detection test on a newly onboarded Microsoft Defender for Endpoint device</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="e81d4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e81d4-105">**Applies to:**</span></span>
- <span data-ttu-id="e81d4-106">Versions Windows 10 pris en charge</span><span class="sxs-lookup"><span data-stu-id="e81d4-106">Supported Windows 10 versions</span></span>
- <span data-ttu-id="e81d4-107">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e81d4-107">Windows Server 2012 R2</span></span>
- <span data-ttu-id="e81d4-108">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e81d4-108">Windows Server 2016</span></span>
- <span data-ttu-id="e81d4-109">Windows Serveur, version 1803</span><span class="sxs-lookup"><span data-stu-id="e81d4-109">Windows Server, version 1803</span></span>
- <span data-ttu-id="e81d4-110">Windows Server, 2019</span><span class="sxs-lookup"><span data-stu-id="e81d4-110">Windows Server, 2019</span></span>
- [<span data-ttu-id="e81d4-111">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e81d4-111">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="e81d4-112">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e81d4-112">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="e81d4-113">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e81d4-113">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e81d4-114">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e81d4-114">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="e81d4-115">Exécutez le script PowerShell suivant sur un appareil nouvellement intégré pour vérifier qu’il est correctement signalé au service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e81d4-115">Run the following PowerShell script on a newly onboarded device to verify that it is properly reporting to the Defender for Endpoint service.</span></span>

1. <span data-ttu-id="e81d4-116">Créez un dossier : « C:\test-MDATP-test ».</span><span class="sxs-lookup"><span data-stu-id="e81d4-116">Create a folder:  'C:\test-MDATP-test'.</span></span>
2. <span data-ttu-id="e81d4-117">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="e81d4-117">Open an elevated command-line prompt on the device and run the script:</span></span>

   1. <span data-ttu-id="e81d4-118">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="e81d4-118">Go to **Start** and type **cmd**.</span></span>

   1. <span data-ttu-id="e81d4-119">Cliquez avec le bouton droit **sur Invite de** commandes et **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="e81d4-119">Right-click **Command Prompt** and select **Run as administrator**.</span></span>

      ![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu’administrateur](images/run-as-admin.png)

3. <span data-ttu-id="e81d4-121">À l’invite, copiez et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e81d4-121">At the prompt, copy and run the following command:</span></span>

   ```powershell
   powershell.exe -NoExit -ExecutionPolicy Bypass -WindowStyle Hidden $ErrorActionPreference = 'silentlycontinue';(New-Object System.Net.WebClient).DownloadFile('http://127.0.0.1/1.exe', 'C:\\test-MDATP-test\\invoice.exe');Start-Process 'C:\\test-MDATP-test\\invoice.exe'
   ```

<span data-ttu-id="e81d4-122">La fenêtre d’invite de commandes se ferme automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e81d4-122">The Command Prompt window will close automatically.</span></span> <span data-ttu-id="e81d4-123">Si elle réussit, le test de détection est marqué comme terminé et une nouvelle alerte s’affiche dans le portail pour l’appareil intégré dans environ 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="e81d4-123">If successful, the detection test will be marked as completed and a new alert will appear in the portal for the onboarded device in approximately 10 minutes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e81d4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e81d4-124">Related topics</span></span>
- [<span data-ttu-id="e81d4-125">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="e81d4-125">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="e81d4-126">Serveurs intégrés</span><span class="sxs-lookup"><span data-stu-id="e81d4-126">Onboard servers</span></span>](configure-server-endpoints.md)
- [<span data-ttu-id="e81d4-127">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="e81d4-127">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/troubleshoot-onboarding)
