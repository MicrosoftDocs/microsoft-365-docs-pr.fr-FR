---
title: Gérer Windows Defender dans votre entreprise
description: Découvrez comment utiliser la stratégie de groupe, Configuration Manager, PowerShell, WMI, Intune et la ligne de commande pour gérer Microsoft Defender AV
keywords: stratégie de groupe, gpo, gestionnaire de config, sccm, scep, powershell, wmi, intune, defender, antivirus, anti-programme malveillant, sécurité, protection
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 12/16/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 6b9845812763f9e3f1fdecf5566824eb76971dad
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764866"
---
# <a name="manage-microsoft-defender-antivirus-in-your-business"></a><span data-ttu-id="d76c2-104">Gérer l'Antivirus Microsoft Defender dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="d76c2-104">Manage Microsoft Defender Antivirus in your business</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="d76c2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d76c2-105">**Applies to:**</span></span>

- [<span data-ttu-id="d76c2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d76c2-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="d76c2-107">Vous pouvez gérer et configurer l'Antivirus Microsoft Defender avec les outils suivants :</span><span class="sxs-lookup"><span data-stu-id="d76c2-107">You can manage and configure Microsoft Defender Antivirus with the following tools:</span></span>

- <span data-ttu-id="d76c2-108">[Microsoft Intune](/mem/intune/protect/endpoint-security-antivirus-policy) (désormais partie intégrante de Microsoft Endpoint Manager)</span><span class="sxs-lookup"><span data-stu-id="d76c2-108">[Microsoft Intune](/mem/intune/protect/endpoint-security-antivirus-policy) (now part of Microsoft Endpoint Manager)</span></span>
- <span data-ttu-id="d76c2-109">[Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection-configure) (qui fait désormais partie de Microsoft Endpoint Manager)</span><span class="sxs-lookup"><span data-stu-id="d76c2-109">[Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection-configure) (now part of Microsoft Endpoint Manager)</span></span>
- [<span data-ttu-id="d76c2-110">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d76c2-110">Group Policy</span></span>](./use-group-policy-microsoft-defender-antivirus.md)
- [<span data-ttu-id="d76c2-111">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="d76c2-111">PowerShell cmdlets</span></span>](./use-powershell-cmdlets-microsoft-defender-antivirus.md)
- [<span data-ttu-id="d76c2-112">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="d76c2-112">Windows Management Instrumentation (WMI)</span></span>](./use-wmi-microsoft-defender-antivirus.md)
- <span data-ttu-id="d76c2-113">Utilitaire de ligne de commande microsoft de protection contre les programmes [malveillants](./command-line-arguments-microsoft-defender-antivirus.md) (appelé *utilitairempcmdrun.exe* logiciel</span><span class="sxs-lookup"><span data-stu-id="d76c2-113">The [Microsoft Malware Protection Command Line Utility](./command-line-arguments-microsoft-defender-antivirus.md) (referred to as the *mpcmdrun.exe* utility</span></span>

<span data-ttu-id="d76c2-114">Les articles suivants fournissent des informations supplémentaires, des liens et des ressources pour l'utilisation de ces outils pour gérer et configurer l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="d76c2-114">The following articles provide further information, links, and resources for using these tools to manage and configure Microsoft Defender Antivirus.</span></span>

| <span data-ttu-id="d76c2-115">Article</span><span class="sxs-lookup"><span data-stu-id="d76c2-115">Article</span></span> | <span data-ttu-id="d76c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="d76c2-116">Description</span></span> |
|:---|:---|
|[<span data-ttu-id="d76c2-117">Gérer l'Antivirus Microsoft Defender avec Microsoft Intune et Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d76c2-117">Manage Microsoft Defender Antivirus with Microsoft Intune and Microsoft Endpoint Configuration Manager</span></span>](use-intune-config-manager-microsoft-defender-antivirus.md)|<span data-ttu-id="d76c2-118">Informations sur l'utilisation d'Intune et de Configuration Manager pour déployer, gérer, signaler et configurer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="d76c2-118">Information about using Intune and Configuration Manager to deploy, manage, report, and configure Microsoft Defender Antivirus</span></span> |
|[<span data-ttu-id="d76c2-119">Gérer l'Antivirus Microsoft Defender avec les paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d76c2-119">Manage Microsoft Defender Antivirus with Group Policy settings</span></span>](use-group-policy-microsoft-defender-antivirus.md)|<span data-ttu-id="d76c2-120">Liste de tous les paramètres de stratégie de groupe situés dans les modèles ADMX</span><span class="sxs-lookup"><span data-stu-id="d76c2-120">List of all Group Policy settings located in ADMX templates</span></span> |
|[<span data-ttu-id="d76c2-121">Gérer l'Antivirus Microsoft Defender avec les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="d76c2-121">Manage Microsoft Defender Antivirus with PowerShell cmdlets</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)|<span data-ttu-id="d76c2-122">Instructions d'utilisation des cmdlets PowerShell pour gérer l'Antivirus Microsoft Defender, ainsi que des liens vers la documentation pour toutes les cmdlets et paramètres autorisés</span><span class="sxs-lookup"><span data-stu-id="d76c2-122">Instructions for using PowerShell cmdlets to manage Microsoft Defender Antivirus, plus links to documentation for all cmdlets and allowed parameters</span></span> |
|[<span data-ttu-id="d76c2-123">Gérer l'Antivirus Microsoft Defender avec Windows Management Instrumentation (WMI)</span><span class="sxs-lookup"><span data-stu-id="d76c2-123">Manage Microsoft Defender Antivirus with Windows Management Instrumentation (WMI)</span></span>](use-wmi-microsoft-defender-antivirus.md)| <span data-ttu-id="d76c2-124">Instructions sur l'utilisation de WMI pour gérer l'Antivirus Microsoft Defender, ainsi que des liens vers la documentation pour les API WMIv2 (y compris toutes les classes, méthodes et propriétés)</span><span class="sxs-lookup"><span data-stu-id="d76c2-124">Instructions for using WMI to manage Microsoft Defender Antivirus, plus links to documentation for the WMIv2 APIs (including all classes, methods, and properties)</span></span> |
|[<span data-ttu-id="d76c2-125">Gérer l'Antivirus Microsoft Defender avec lmpcmdrun.exe de ligne de commande microsoft</span><span class="sxs-lookup"><span data-stu-id="d76c2-125">Manage Microsoft Defender Antivirus with the mpcmdrun.exe command-line tool</span></span>](command-line-arguments-microsoft-defender-antivirus.md)|<span data-ttu-id="d76c2-126">Instructions sur l'utilisation de l'outil en ligne de commande dédié pour gérer et utiliser l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="d76c2-126">Instructions on using the dedicated command-line tool to manage and use Microsoft Defender Antivirus</span></span> |