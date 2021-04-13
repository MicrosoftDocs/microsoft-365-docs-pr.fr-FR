---
title: Résoudre les problèmes de réponse en direct de Microsoft Defender pour les points de terminaison
description: Résoudre les problèmes qui peuvent survenir lors de l'utilisation d'une réponse en direct dans Microsoft Defender pour le point de terminaison
keywords: résoudre les problèmes de réponse en direct, en direct, réponse, verrouillé, fichier
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
ms.topic: troubleshooting
ms.technology: mde
ms.openlocfilehash: 2601001687fc22da98ca3cd81010237d12705ea4
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51687410"
---
# <a name="troubleshoot-microsoft-defender-for-endpoint-live-response-issues"></a><span data-ttu-id="6e2f1-104">Résoudre les problèmes de réponse en direct de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="6e2f1-104">Troubleshoot Microsoft Defender for Endpoint live response issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6e2f1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6e2f1-105">**Applies to:**</span></span>
- [<span data-ttu-id="6e2f1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6e2f1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6e2f1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6e2f1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6e2f1-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6e2f1-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6e2f1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

<span data-ttu-id="6e2f1-110">Cette page fournit des étapes détaillées pour résoudre les problèmes de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-110">This page provides detailed steps to troubleshoot live response issues.</span></span>

## <a name="file-cannot-be-accessed-during-live-response-sessions"></a><span data-ttu-id="6e2f1-111">Impossible d'accéder au fichier pendant les sessions de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="6e2f1-111">File cannot be accessed during live response sessions</span></span>
<span data-ttu-id="6e2f1-112">Si, lors d'une tentative d'action au cours d'une session de réponse en direct, vous rencontrez un message d'erreur indiquant que le fichier n'est pas accessible, vous devez suivre les étapes ci-dessous pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-112">If while trying to take an action during a live response session, you encounter an error message stating that the file can't be accessed, you'll need to use the steps below to address the issue.</span></span>

1. <span data-ttu-id="6e2f1-113">Copiez l'extrait de code de script suivant et enregistrez-le en tant que fichier PS1 :</span><span class="sxs-lookup"><span data-stu-id="6e2f1-113">Copy the following script code snippet and save it as a PS1 file:</span></span>

    ```
    $copied_file_path=$args[0] 
    $action=Copy-Item $copied_file_path -Destination $env:TEMP -PassThru -ErrorAction silentlyContinue
        
    if ($action){
         Write-Host "You copied the file specified in $copied_file_path to $env:TEMP Succesfully"
    }
    
    else{
        Write-Output "Error occoured while trying to copy a file, details:"
        Write-Output  $error[0].exception.message
 
    }
    ```


2. <span data-ttu-id="6e2f1-114">Ajoutez le script à la bibliothèque de réponses en direct.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-114">Add the script to the live response library.</span></span>
3. <span data-ttu-id="6e2f1-115">Exécutez le script avec un paramètre : le chemin d'accès au fichier à copier.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-115">Run the script with one parameter: the file path of the file to be copied.</span></span>
4. <span data-ttu-id="6e2f1-116">Accédez à votre dossier TEMP.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-116">Navigate to your TEMP folder.</span></span>
5. <span data-ttu-id="6e2f1-117">Exécutez l'action que vous souhaitez exécuter sur le fichier copié.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-117">Run the action you wanted to take on the copied file.</span></span>

## <a name="slow-live-response-sessions-or-delays-during-initial-connections"></a><span data-ttu-id="6e2f1-118">Sessions de réponse en direct lentes ou retards pendant les connexions initiales</span><span class="sxs-lookup"><span data-stu-id="6e2f1-118">Slow live response sessions or delays during initial connections</span></span>
<span data-ttu-id="6e2f1-119">Live Response tire parti de Defender pour l'inscription du capteur de point de terminaison avec le service WNS dans Windows.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-119">Live response leverages Defender for Endpoint sensor registration with WNS service in Windows.</span></span> <span data-ttu-id="6e2f1-120">Si vous avez des problèmes de connectivité avec la réponse en direct, confirmez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="6e2f1-120">If you are having connectivity issues with live response, confirm the following details:</span></span>
1. <span data-ttu-id="6e2f1-121">`notify.windows.com` n'est pas bloqué dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-121">`notify.windows.com` is not blocked in your environment.</span></span> <span data-ttu-id="6e2f1-122">Pour plus d'informations, voir Configurer [les paramètres de proxy d'appareil et de connectivité Internet.](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="6e2f1-122">For more information, see, [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span>
2. <span data-ttu-id="6e2f1-123">WpnService (service système de notifications Push Windows) n'est pas désactivé.</span><span class="sxs-lookup"><span data-stu-id="6e2f1-123">WpnService (Windows Push Notifications System Service) is not disabled.</span></span>

<span data-ttu-id="6e2f1-124">Reportez-vous aux articles ci-dessous pour bien comprendre le comportement et les exigences du service WpnService :</span><span class="sxs-lookup"><span data-stu-id="6e2f1-124">Refer to the articles below to fully understand the WpnService service behavior and requirements:</span></span>
- [<span data-ttu-id="6e2f1-125">Vue d'ensemble Notification Services Windows Push (WNS)</span><span class="sxs-lookup"><span data-stu-id="6e2f1-125">Windows Push Notification Services (WNS) overview</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/windows-push-notification-services--wns--overview)
- [<span data-ttu-id="6e2f1-126">Configurations de pare-feu et de proxy d'entreprise pour prendre en charge le trafic WNS</span><span class="sxs-lookup"><span data-stu-id="6e2f1-126">Enterprise Firewall and Proxy Configurations to Support WNS Traffic</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)
- [<span data-ttu-id="6e2f1-127">Plages IP publiques MPNS (Microsoft Push Notifications Service)</span><span class="sxs-lookup"><span data-stu-id="6e2f1-127">Microsoft Push Notifications Service (MPNS) Public IP ranges</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=44535)

