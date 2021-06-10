---
title: Configurer des exclusions pour Antivirus Microsoft Defender analyses
description: Vous pouvez exclure les fichiers (y compris les fichiers modifiés par des processus spécifiés) et les dossiers d’être analysés par Antivirus Microsoft Defender. Validez vos exclusions avec PowerShell.
keywords: ''
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ksarens
manager: dansimp
ms.technology: mde
ms.audience: ITPro
ms.topic: how-to
ms.openlocfilehash: 7065aa7cd1975b2f5a38e79da8618ba3efdcdac5
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275119"
---
# <a name="configure-and-validate-exclusions-for-microsoft-defender-antivirus-scans"></a><span data-ttu-id="d01e5-104">Configurer et valider des exclusions pour Antivirus Microsoft Defender analyses</span><span class="sxs-lookup"><span data-stu-id="d01e5-104">Configure and validate exclusions for Microsoft Defender Antivirus scans</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="d01e5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d01e5-105">**Applies to:**</span></span>

- [<span data-ttu-id="d01e5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d01e5-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="d01e5-107">Vous pouvez exclure certains fichiers, dossiers, processus et fichiers ouverts par des processus Antivirus Microsoft Defender analyses.</span><span class="sxs-lookup"><span data-stu-id="d01e5-107">You can exclude certain files, folders, processes, and process-opened files from Microsoft Defender Antivirus scans.</span></span> <span data-ttu-id="d01e5-108">Ces exclusions s’appliquent [aux analyses programmées,](scheduled-catch-up-scans-microsoft-defender-antivirus.md)aux analyses à la demande [et](run-scan-microsoft-defender-antivirus.md)à la protection et à la surveillance en temps réel toujours en [temps réel.](configure-real-time-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="d01e5-108">Such exclusions apply to [scheduled scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md), [on-demand scans](run-scan-microsoft-defender-antivirus.md), and [always-on real-time protection and monitoring](configure-real-time-protection-microsoft-defender-antivirus.md).</span></span> <span data-ttu-id="d01e5-109">Les exclusions pour les fichiers ouverts par le processus s’appliquent uniquement à la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d01e5-109">Exclusions for process-opened files only apply to real-time protection.</span></span>

## <a name="configure-and-validate-exclusions"></a><span data-ttu-id="d01e5-110">Configurer et valider des exclusions</span><span class="sxs-lookup"><span data-stu-id="d01e5-110">Configure and validate exclusions</span></span>

<span data-ttu-id="d01e5-111">Pour configurer et valider des exclusions, consultez les procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="d01e5-111">To configure and validate exclusions, see the following:</span></span>

- <span data-ttu-id="d01e5-112">[Configurez et validez les exclusions en fonction du nom de fichier, de l’extension et de l’emplacement du dossier.](configure-extension-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="d01e5-112">[Configure and validate exclusions based on file name, extension, and folder location](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span></span> <span data-ttu-id="d01e5-113">Vous pouvez exclure des fichiers des Antivirus Microsoft Defender en fonction de leur extension de fichier, de leur nom de fichier ou de leur emplacement.</span><span class="sxs-lookup"><span data-stu-id="d01e5-113">You can exclude files from Microsoft Defender Antivirus scans based on their file extension, file name, or location.</span></span>

- <span data-ttu-id="d01e5-114">[Configurez et validez les exclusions pour les fichiers ouverts par des processus.](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="d01e5-114">[Configure and validate exclusions for files opened by processes](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md).</span></span> <span data-ttu-id="d01e5-115">Vous pouvez exclure des fichiers des analyses qui ont été ouvertes par un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="d01e5-115">You can exclude files from scans that have been opened by a specific process.</span></span>

## <a name="recommendations-for-defining-exclusions"></a><span data-ttu-id="d01e5-116">Recommandations définition des exclusions</span><span class="sxs-lookup"><span data-stu-id="d01e5-116">Recommendations for defining exclusions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d01e5-117">Antivirus Microsoft Defender inclut de nombreuses exclusions automatiques basées sur les comportements connus du système d’exploitation et les fichiers de gestion classiques, tels que ceux utilisés dans la gestion d’entreprise, la gestion des bases de données et d’autres scénarios et situations d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d01e5-117">Microsoft Defender Antivirus includes many automatic exclusions based on known operating system behaviors and typical management files, such as those used in enterprise management, database management, and other enterprise scenarios and situations.</span></span>  
> 
> <span data-ttu-id="d01e5-118">La définition d’exclusions réduit la protection offerte par Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="d01e5-118">Defining exclusions lowers the protection offered by Microsoft Defender Antivirus.</span></span> <span data-ttu-id="d01e5-119">Vous devez toujours évaluer les risques associés à l’implémentation d’exclusions, et vous devez exclure uniquement les fichiers dont vous êtes certain qu’ils ne sont pas malveillants.</span><span class="sxs-lookup"><span data-stu-id="d01e5-119">You should always evaluate the risks that are associated with implementing exclusions, and you should only exclude files that you are confident are not malicious.</span></span>

<span data-ttu-id="d01e5-120">Gardez les points suivants à l’esprit lorsque vous définissez des exclusions :</span><span class="sxs-lookup"><span data-stu-id="d01e5-120">Keep the following points in mind when you are defining exclusions:</span></span>  

- <span data-ttu-id="d01e5-121">Les exclusions sont techniquement un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="d01e5-121">Exclusions are technically a protection gap.</span></span> <span data-ttu-id="d01e5-122">Envisagez toujours les atténuations lors de la définition d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="d01e5-122">Always consider mitigations when defining exclusions.</span></span> <span data-ttu-id="d01e5-123">D’autres atténuations peuvent être aussi simples que de s’assurer que l’emplacement exclu dispose des listes de contrôle d’accès (ACA) appropriées, de la stratégie d’audit, est traitée par un logiciel à jour, etc.</span><span class="sxs-lookup"><span data-stu-id="d01e5-123">Other mitigations could be as simple as making sure the excluded location has the appropriate access-control lists (ACLs), audit policy, is processed by an up-to-date software, etc.</span></span>

- <span data-ttu-id="d01e5-124">Examinez régulièrement les exclusions.</span><span class="sxs-lookup"><span data-stu-id="d01e5-124">Review the exclusions periodically.</span></span> <span data-ttu-id="d01e5-125">Revérifiez et appliquez de nouveau les atténuations dans le cadre du processus de révision.</span><span class="sxs-lookup"><span data-stu-id="d01e5-125">Recheck and re-enforce the mitigations as part of the review process.</span></span>

- <span data-ttu-id="d01e5-126">Dans l’idéal, évitez de définir des exclusions qui doivent être proactives.</span><span class="sxs-lookup"><span data-stu-id="d01e5-126">Ideally, avoid defining exclusions intending to be proactive.</span></span> <span data-ttu-id="d01e5-127">Par exemple, n’excluez pas quelque chose simplement parce que vous pensez qu’il pourrait s’agir d’un problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d01e5-127">For instance, don't exclude something just because you think it might be a problem in the future.</span></span> <span data-ttu-id="d01e5-128">Utilisez des exclusions uniquement pour des problèmes spécifiques, tels que ceux relatifs aux performances ou à la compatibilité des applications que les exclusions peuvent atténuer.</span><span class="sxs-lookup"><span data-stu-id="d01e5-128">Use exclusions only for specific issues, such as those pertaining to performance or application compatibility that exclusions could mitigate.</span></span>

- <span data-ttu-id="d01e5-129">Auditez les modifications apportées à la liste d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="d01e5-129">Audit the exclusion list changes.</span></span> <span data-ttu-id="d01e5-130">L’administrateur de sécurité doit conserver suffisamment de contexte sur la raison pour laquelle une certaine exclusion a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="d01e5-130">The security admin should preserve enough context around why a certain exclusion was added.</span></span> <span data-ttu-id="d01e5-131">Vous devriez être en mesure de fournir une réponse avec un raisonnement spécifique quant à la raison pour laquelle un certain chemin d’accès a été exclu.</span><span class="sxs-lookup"><span data-stu-id="d01e5-131">You should be able to provide answer with specific reasoning as to why a certain path was excluded.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d01e5-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d01e5-132">Related articles</span></span>

- [<span data-ttu-id="d01e5-133">Antivirus Microsoft Defender exclusions sur Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d01e5-133">Microsoft Defender Antivirus exclusions on Windows Server 2016</span></span>](configure-server-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="d01e5-134">Erreurs courantes à éviter lors de la définition d’exclusions</span><span class="sxs-lookup"><span data-stu-id="d01e5-134">Common mistakes to avoid when defining exclusions</span></span>](common-exclusion-mistakes-microsoft-defender-antivirus.md)
