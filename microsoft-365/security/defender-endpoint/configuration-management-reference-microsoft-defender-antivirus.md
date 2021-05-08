---
title: Gérer Windows Defender dans votre entreprise
description: Découvrez comment utiliser la stratégie de groupe, Configuration Manager, PowerShell, WMI, Intune et la ligne de commande pour gérer Microsoft Defender AV
keywords: stratégie de groupe, gpo, gestionnaire de config, sccm, scep, powershell, wmi, intune, defender, antivirus, anti-programme malveillant, sécurité, protection
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 05/06/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 2265f3680e425ade062d444685fbd8873eaa02ca
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274963"
---
# <a name="manage-microsoft-defender-antivirus-in-your-business"></a><span data-ttu-id="4eabe-104">Gérer Antivirus Microsoft Defender dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="4eabe-104">Manage Microsoft Defender Antivirus in your business</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="4eabe-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4eabe-105">**Applies to:**</span></span>

- [<span data-ttu-id="4eabe-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4eabe-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="4eabe-107">Vous pouvez gérer et configurer les Antivirus Microsoft Defender à l’aide des outils suivants :</span><span class="sxs-lookup"><span data-stu-id="4eabe-107">You can manage and configure Microsoft Defender Antivirus with the following tools:</span></span>

- <span data-ttu-id="4eabe-108">[Microsoft Intune](/mem/intune/protect/endpoint-security-antivirus-policy) (fait désormais partie de Microsoft Endpoint Manager)</span><span class="sxs-lookup"><span data-stu-id="4eabe-108">[Microsoft Intune](/mem/intune/protect/endpoint-security-antivirus-policy) (now part of Microsoft Endpoint Manager)</span></span>
- <span data-ttu-id="4eabe-109">[Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection-configure) (fait désormais partie de Microsoft Endpoint Manager)</span><span class="sxs-lookup"><span data-stu-id="4eabe-109">[Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection-configure) (now part of Microsoft Endpoint Manager)</span></span>
- [<span data-ttu-id="4eabe-110">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="4eabe-110">Group Policy</span></span>](./use-group-policy-microsoft-defender-antivirus.md)
- [<span data-ttu-id="4eabe-111">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="4eabe-111">PowerShell cmdlets</span></span>](./use-powershell-cmdlets-microsoft-defender-antivirus.md)
- [<span data-ttu-id="4eabe-112">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="4eabe-112">Windows Management Instrumentation (WMI)</span></span>](./use-wmi-microsoft-defender-antivirus.md)
- <span data-ttu-id="4eabe-113">Utilitaire de ligne de commande microsoft de protection contre les programmes [malveillants](./command-line-arguments-microsoft-defender-antivirus.md) (appelé *utilitairempcmdrun.exe* logiciel</span><span class="sxs-lookup"><span data-stu-id="4eabe-113">The [Microsoft Malware Protection Command Line Utility](./command-line-arguments-microsoft-defender-antivirus.md) (referred to as the *mpcmdrun.exe* utility</span></span>

<span data-ttu-id="4eabe-114">Les articles suivants fournissent des informations supplémentaires, des liens et des ressources pour l’utilisation de ces outils pour gérer et configurer Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4eabe-114">The following articles provide further information, links, and resources for using these tools to manage and configure Microsoft Defender Antivirus.</span></span>

| <span data-ttu-id="4eabe-115">Article</span><span class="sxs-lookup"><span data-stu-id="4eabe-115">Article</span></span> | <span data-ttu-id="4eabe-116">Description</span><span class="sxs-lookup"><span data-stu-id="4eabe-116">Description</span></span> |
|:---|:---|
|[<span data-ttu-id="4eabe-117">Gérer Antivirus Microsoft Defender avec Microsoft Intune et Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4eabe-117">Manage Microsoft Defender Antivirus with Microsoft Intune and Microsoft Endpoint Configuration Manager</span></span>](use-intune-config-manager-microsoft-defender-antivirus.md)|<span data-ttu-id="4eabe-118">Informations sur l’utilisation d’Intune et de Configuration Manager pour déployer, gérer, signaler et configurer Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4eabe-118">Information about using Intune and Configuration Manager to deploy, manage, report, and configure Microsoft Defender Antivirus</span></span> |
|[<span data-ttu-id="4eabe-119">Gérer les Antivirus Microsoft Defender avec les paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="4eabe-119">Manage Microsoft Defender Antivirus with Group Policy settings</span></span>](use-group-policy-microsoft-defender-antivirus.md)|<span data-ttu-id="4eabe-120">Liste de tous les paramètres de stratégie de groupe situés dans les modèles ADMX</span><span class="sxs-lookup"><span data-stu-id="4eabe-120">List of all Group Policy settings located in ADMX templates</span></span> |
|[<span data-ttu-id="4eabe-121">Gérer Antivirus Microsoft Defender avec les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="4eabe-121">Manage Microsoft Defender Antivirus with PowerShell cmdlets</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)|<span data-ttu-id="4eabe-122">Instructions d’utilisation des cmdlets PowerShell pour gérer les Antivirus Microsoft Defender, ainsi que des liens vers la documentation pour toutes les cmdlets et paramètres autorisés</span><span class="sxs-lookup"><span data-stu-id="4eabe-122">Instructions for using PowerShell cmdlets to manage Microsoft Defender Antivirus, plus links to documentation for all cmdlets and allowed parameters</span></span> |
|[<span data-ttu-id="4eabe-123">Gérer Antivirus Microsoft Defender avec Windows Management Instrumentation (WMI)</span><span class="sxs-lookup"><span data-stu-id="4eabe-123">Manage Microsoft Defender Antivirus with Windows Management Instrumentation (WMI)</span></span>](use-wmi-microsoft-defender-antivirus.md)| <span data-ttu-id="4eabe-124">Instructions d’utilisation de WMI pour gérer les Antivirus Microsoft Defender, ainsi que des liens vers la documentation pour les API WMIv2 (y compris toutes les classes, méthodes et propriétés)</span><span class="sxs-lookup"><span data-stu-id="4eabe-124">Instructions for using WMI to manage Microsoft Defender Antivirus, plus links to documentation for the WMIv2 APIs (including all classes, methods, and properties)</span></span> |
|[<span data-ttu-id="4eabe-125">Gérer Antivirus Microsoft Defender’aide de lmpcmdrun.exe de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="4eabe-125">Manage Microsoft Defender Antivirus with the mpcmdrun.exe command-line tool</span></span>](command-line-arguments-microsoft-defender-antivirus.md)|<span data-ttu-id="4eabe-126">Instructions sur l’utilisation de l’outil en ligne de commande dédié pour gérer et utiliser Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4eabe-126">Instructions on using the dedicated command-line tool to manage and use Microsoft Defender Antivirus</span></span> |