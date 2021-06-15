---
title: Déployer et activer l’antivirus Microsoft Defender
description: Déployez Antivirus Microsoft Defender pour la protection de vos points de terminaison avec Microsoft Intune, Microsoft Endpoint Configuration Manager, stratégie de groupe, cmdlets PowerShell ou WMI.
keywords: déployer, activer, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
ms.topic: conceptual
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 01/06/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: a847e65adb0402d4c5f98e19424677ccdc1011da
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925742"
---
# <a name="deploy-and-enable-microsoft-defender-antivirus"></a><span data-ttu-id="6edcd-104">Déployer et activer l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="6edcd-104">Deploy and enable Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6edcd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6edcd-105">**Applies to:**</span></span>

- [<span data-ttu-id="6edcd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6edcd-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="6edcd-107">En fonction de l’outil de gestion que vous utilisez, vous devrez peut-être activer ou configurer spécifiquement Antivirus Microsoft Defender protection.</span><span class="sxs-lookup"><span data-stu-id="6edcd-107">Depending on the management tool you are using, you may need to specifically enable or configure Microsoft Defender Antivirus protection.</span></span> 

<span data-ttu-id="6edcd-108">Consultez le tableau dans [Déployer,](deploy-manage-report-microsoft-defender-antivirus.md#ref2) gérer et signaler Antivirus Microsoft Defender pour obtenir des instructions sur la façon d’activer la protection avec Microsoft Intune, Microsoft Endpoint Configuration Manager, stratégie de groupe, Active Directory, Microsoft Azure, cmdlets PowerShell et Windows Management Instruction (WMI).</span><span class="sxs-lookup"><span data-stu-id="6edcd-108">See the table in [Deploy, manage, and report on Microsoft Defender Antivirus](deploy-manage-report-microsoft-defender-antivirus.md#ref2) for instructions on how to enable protection with Microsoft Intune, Microsoft Endpoint Configuration Manager, Group Policy, Active Directory, Microsoft Azure, PowerShell cmdlets, and Windows Management Instruction (WMI).</span></span>

<span data-ttu-id="6edcd-109">Certains scénarios nécessitent davantage d’instructions sur la façon de déployer ou de configurer Antivirus Microsoft Defender protection, telles que les environnements VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="6edcd-109">Some scenarios require more guidance on how to successfully deploy or configure Microsoft Defender Antivirus protection, such as Virtual Desktop Infrastructure (VDI) environments.</span></span>

<span data-ttu-id="6edcd-110">L’article restant de cette section fournit des conseils de bout en bout et des meilleures pratiques pour la configuration de Antivirus Microsoft Defender sur des [machines virtuelles (VM)](deployment-vdi-microsoft-defender-antivirus.md)dans un environnement VDI ou RDS (Remote Desktop Services).</span><span class="sxs-lookup"><span data-stu-id="6edcd-110">The remaining article in this section provides end-to-end advice and best practices for [setting up Microsoft Defender Antivirus on virtual machines (VMs) in a VDI or Remote Desktop Services (RDS) environment](deployment-vdi-microsoft-defender-antivirus.md).</span></span>

## <a name="related-articles"></a><span data-ttu-id="6edcd-111">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6edcd-111">Related articles</span></span>

- [<span data-ttu-id="6edcd-112">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="6edcd-112">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="6edcd-113">Déployer, gérer les mises à jour et signaler les Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="6edcd-113">Deploy, manage updates, and report on Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="6edcd-114">Guide de déploiement de l’antivirus Microsoft Defender dans un environnement VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="6edcd-114">Deployment guide for Microsoft Defender Antivirus in a virtual desktop infrastructure (VDI) environment</span></span>](deployment-vdi-microsoft-defender-antivirus.md)