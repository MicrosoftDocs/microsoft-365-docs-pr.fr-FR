---
title: Exécuter et personnaliser des analyses programmées et à la demande
description: Personnalisez et lancez Antivirus Microsoft Defender analyses sur les points de terminaison sur votre réseau.
keywords: analyser, planifier, personnaliser, exclusions, exclure des fichiers, correction, résultats de l’analyse, mise en quarantaine, supprimer une menace, analyse rapide, analyse complète, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: f3e0cc7ffccf02e24b9746d539a44d3a72810ead
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2021
ms.locfileid: "52286184"
---
# <a name="customize-initiate-and-review-the-results-of-microsoft-defender-antivirus-scans--remediation"></a><span data-ttu-id="3dc29-104">Personnaliser, lancer et passer en revue les résultats de Antivirus Microsoft Defender analyses & correction</span><span class="sxs-lookup"><span data-stu-id="3dc29-104">Customize, initiate, and review the results of Microsoft Defender Antivirus scans & remediation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3dc29-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3dc29-105">**Applies to:**</span></span>

- [<span data-ttu-id="3dc29-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3dc29-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="3dc29-107">Vous pouvez utiliser la stratégie de groupe, PowerShell et Windows Management Instrumentation (WMI) pour configurer Antivirus Microsoft Defender analyses.</span><span class="sxs-lookup"><span data-stu-id="3dc29-107">You can use Group Policy, PowerShell, and Windows Management Instrumentation (WMI) to configure Microsoft Defender Antivirus scans.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="3dc29-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3dc29-108">In this section</span></span>

| <span data-ttu-id="3dc29-109">Article</span><span class="sxs-lookup"><span data-stu-id="3dc29-109">Article</span></span> | <span data-ttu-id="3dc29-110">Description</span><span class="sxs-lookup"><span data-stu-id="3dc29-110">Description</span></span> |
|:---|:---|
|[<span data-ttu-id="3dc29-111">Configurer et valider des exclusions de fichiers, de dossiers et de fichiers ouverts par processus dans Antivirus Microsoft Defender analyses</span><span class="sxs-lookup"><span data-stu-id="3dc29-111">Configure and validate file, folder, and process-opened file exclusions in Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-112">Vous pouvez exclure les fichiers (y compris les fichiers modifiés par des processus spécifiés) et les dossiers des analyses à la demande, des analyses programmées et de l’analyse et de l’analyse de la protection en temps réel toujours en temps réel</span><span class="sxs-lookup"><span data-stu-id="3dc29-112">You can exclude files (including files modified by specified processes) and folders from on-demand scans, scheduled scans, and always-on real-time protection monitoring and scanning</span></span> |
|[<span data-ttu-id="3dc29-113">Configurer les options d’analyse de l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="3dc29-113">Configure Microsoft Defender Antivirus scanning options</span></span>](configure-advanced-scan-types-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-114">Vous pouvez configurer Antivirus Microsoft Defender pour inclure certains types de fichiers de stockage de courrier électronique, des points de stockage ou d’analyse, ainsi que des fichiers archivés (tels que des fichiers .zip) dans les analyses.</span><span class="sxs-lookup"><span data-stu-id="3dc29-114">You can configure Microsoft Defender Antivirus to include certain types of email storage files, back-up or reparse points, and archived files (such as .zip files) in scans.</span></span> <span data-ttu-id="3dc29-115">Vous pouvez également activer l’analyse des fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="3dc29-115">You can also enable network file scanning</span></span> |
|[<span data-ttu-id="3dc29-116">Configurer la correction pour les analyses</span><span class="sxs-lookup"><span data-stu-id="3dc29-116">Configure remediation for scans</span></span>](configure-remediation-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-117">Configurer ce que Antivirus Microsoft Defender doit faire lorsqu’il détecte une menace et combien de temps les fichiers mis en quarantaine doivent être conservés dans le dossier de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="3dc29-117">Configure what Microsoft Defender Antivirus should do when it detects a threat, and how long quarantined files should be retained in the quarantine folder</span></span> |
|[<span data-ttu-id="3dc29-118">Configurer des analyses programmées</span><span class="sxs-lookup"><span data-stu-id="3dc29-118">Configure scheduled scans</span></span>](scheduled-catch-up-scans-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-119">Configurer des analyses périodiques (programmées), notamment quand elles doivent s’exécuter et s’ils s’exécutent en tant qu’analyses complètes ou rapides</span><span class="sxs-lookup"><span data-stu-id="3dc29-119">Set up recurring (scheduled) scans, including when they should run and whether they run as full or quick scans</span></span> |
|[<span data-ttu-id="3dc29-120">Configurer et exécuter des analyses</span><span class="sxs-lookup"><span data-stu-id="3dc29-120">Configure and run scans</span></span>](run-scan-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-121">Exécuter et configurer des analyses à la demande à l’aide de PowerShell, Windows Management Instrumentation ou individuellement sur les points de terminaison avec l Sécurité Windows appl.</span><span class="sxs-lookup"><span data-stu-id="3dc29-121">Run and configure on-demand scans using PowerShell, Windows Management Instrumentation, or individually on endpoints with the Windows Security app</span></span> |
|[<span data-ttu-id="3dc29-122">Passer en revue les résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="3dc29-122">Review scan results</span></span>](review-scan-results-microsoft-defender-antivirus.md) | <span data-ttu-id="3dc29-123">Passer en revue les résultats des analyses à l’aide Microsoft Endpoint Configuration Manager, Microsoft Intune ou l’application Sécurité Windows de données</span><span class="sxs-lookup"><span data-stu-id="3dc29-123">Review the results of scans using  Microsoft Endpoint Configuration Manager, Microsoft Intune, or the Windows Security app</span></span> |