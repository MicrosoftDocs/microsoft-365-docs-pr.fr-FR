---
title: Résoudre les problèmes de performances pour Microsoft Defender ATP pour Mac
description: Résolution des problèmes de performances dans Microsoft Defender ATP pour Mac.
keywords: microsoft, defender, atp, mac, performances
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
ms.openlocfilehash: dbd82bae86ac4181497ecc87bc74181f7a502e15
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062222"
---
# <a name="troubleshoot-performance-issues-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="f1e9e-104">Résoudre les problèmes de performances pour Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="f1e9e-104">Troubleshoot performance issues for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f1e9e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f1e9e-105">**Applies to:**</span></span>

- [<span data-ttu-id="f1e9e-106">Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="f1e9e-106">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="f1e9e-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f1e9e-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="f1e9e-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f1e9e-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f1e9e-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f1e9e-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f1e9e-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="f1e9e-111">Cette rubrique fournit quelques étapes générales qui peuvent être utilisées pour affiner les problèmes de performances liés à Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-111">This topic provides some general steps that can be used to narrow down performance issues related to Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="f1e9e-112">La protection en temps réel (RTP) est une fonctionnalité de Microsoft Defender pour Endpoint pour Mac qui surveille et protège en permanence votre appareil contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-112">Real-time protection (RTP) is a feature of Microsoft Defender for Endpoint for Mac that continuously monitors and protects your device against threats.</span></span> <span data-ttu-id="f1e9e-113">Il se compose de la surveillance des fichiers et des processus et d’autres heuristiques.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-113">It consists of file and process monitoring and other heuristics.</span></span>

<span data-ttu-id="f1e9e-114">Selon les applications que vous exécutez et les caractéristiques de votre appareil, vous pouvez obtenir des performances sous-optimales lors de l’exécution de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-114">Depending on the applications that you are running and your device characteristics, you may experience suboptimal performance when running Microsoft Defender for Endpoint for Mac.</span></span> <span data-ttu-id="f1e9e-115">En particulier, les applications ou les processus système qui accèdent à de nombreuses ressources sur un court laps de temps peuvent entraîner des problèmes de performances dans Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-115">In particular, applications or system processes that access many resources over a short timespan can lead to performance issues in Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="f1e9e-116">Les étapes suivantes peuvent être utilisées pour résoudre et atténuer ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="f1e9e-116">The following steps can be used to troubleshoot and mitigate these issues:</span></span>

1. <span data-ttu-id="f1e9e-117">Désactivez la protection en temps réel à l’aide de l’une des méthodes suivantes et observez si les performances sont améliorées.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-117">Disable real-time protection using one of the following methods and observe whether the performance improves.</span></span> <span data-ttu-id="f1e9e-118">Cette approche permet de déterminer si Microsoft Defender pour Endpoint pour Mac contribue aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-118">This approach helps narrow down whether Microsoft Defender for Endpoint for Mac is contributing to the performance issues.</span></span>

    <span data-ttu-id="f1e9e-119">Si votre appareil n’est pas géré par votre organisation, la protection en temps réel peut être désactivée à l’aide de l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1e9e-119">If your device is not managed by your organization, real-time protection can be disabled using one of the following options:</span></span>

    - <span data-ttu-id="f1e9e-120">À partir de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-120">From the user interface.</span></span> <span data-ttu-id="f1e9e-121">Ouvrez Microsoft Defender pour le point de terminaison pour Mac et accédez **à Gérer les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="f1e9e-121">Open Microsoft Defender for Endpoint for Mac and navigate to **Manage settings**.</span></span>

      ![Capture d’écran gérer la protection en temps réel](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-36-rtp)

    - <span data-ttu-id="f1e9e-123">À partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-123">From the Terminal.</span></span> <span data-ttu-id="f1e9e-124">Pour des raisons de sécurité, cette opération nécessite une élévation.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-124">For security purposes, this operation requires elevation.</span></span>

      ```bash
      mdatp config real-time-protection --value disabled
      ```

    <span data-ttu-id="f1e9e-125">Si votre appareil est géré par votre organisation, la protection en temps réel peut être désactivée par votre administrateur à l’aide des instructions dans Définir les préférences pour [Microsoft Defender pour Endpoint pour Mac.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="f1e9e-125">If your device is managed by your organization, real-time protection can be disabled by your administrator using the instructions in [Set preferences for Microsoft Defender for Endpoint for Mac](mac-preferences.md).</span></span>

2. <span data-ttu-id="f1e9e-126">Ouvrez Finder et accédez aux  >  **utilitaires d’applications.**</span><span class="sxs-lookup"><span data-stu-id="f1e9e-126">Open Finder and navigate to **Applications** > **Utilities**.</span></span> <span data-ttu-id="f1e9e-127">Ouvrez **l’Analyseur** d’activité et analysez les applications qui utilisent les ressources de votre système.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-127">Open **Activity Monitor** and analyze which applications are using the resources on your system.</span></span> <span data-ttu-id="f1e9e-128">Les compilateurs et les outils de mise à jour logicielles sont des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-128">Typical examples include software updaters and compilers.</span></span>

3. <span data-ttu-id="f1e9e-129">Configurez Microsoft Defender pour endpoint pour Mac avec des exclusions pour les processus ou les emplacements de disque qui contribuent aux problèmes de performances et activez à nouveau la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="f1e9e-129">Configure Microsoft Defender for Endpoint for Mac with exclusions for the processes or disk locations that contribute to the performance issues and re-enable real-time protection.</span></span>

    <span data-ttu-id="f1e9e-130">Pour plus d’informations, voir Configurer et valider des [exclusions pour Microsoft Defender pour Endpoint pour Mac.](mac-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="f1e9e-130">See [Configure and validate exclusions for Microsoft Defender for Endpoint for Mac](mac-exclusions.md) for details.</span></span>
