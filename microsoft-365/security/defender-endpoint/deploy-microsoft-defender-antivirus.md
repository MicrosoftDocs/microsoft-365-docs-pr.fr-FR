---
title: Déployer et activer l'Antivirus Microsoft Defender
description: Déployez l'Antivirus Microsoft Defender pour la protection de vos points de terminaison avec Microsoft Intune, Microsoft Endpoint Configuration Manager, la stratégie de groupe, les cmdlets PowerShell ou WMI.
keywords: déployer, activer, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 01/06/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: efc2aa0f48cb2bc55e729b65c892a07b74c1bc46
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690723"
---
# <a name="deploy-and-enable-microsoft-defender-antivirus"></a><span data-ttu-id="e20f4-104">Déployer et activer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="e20f4-104">Deploy and enable Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="e20f4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e20f4-105">**Applies to:**</span></span>

- [<span data-ttu-id="e20f4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e20f4-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="e20f4-107">En fonction de l'outil de gestion que vous utilisez, vous devrez peut-être activer ou configurer spécifiquement la protection antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e20f4-107">Depending on the management tool you are using, you may need to specifically enable or configure Microsoft Defender Antivirus protection.</span></span> 

<span data-ttu-id="e20f4-108">Consultez le tableau dans [Déployer,](deploy-manage-report-microsoft-defender-antivirus.md#ref2) gérer et signaler l'Antivirus Microsoft Defender pour obtenir des instructions sur la façon d'activer la protection avec Microsoft Intune, Microsoft Endpoint Configuration Manager, la stratégie de groupe, Active Directory, Microsoft Azure, les cmdlets PowerShell et windows Management Instruction (WMI).</span><span class="sxs-lookup"><span data-stu-id="e20f4-108">See the table in [Deploy, manage, and report on Microsoft Defender Antivirus](deploy-manage-report-microsoft-defender-antivirus.md#ref2) for instructions on how to enable protection with Microsoft Intune, Microsoft Endpoint Configuration Manager, Group Policy, Active Directory, Microsoft Azure, PowerShell cmdlets, and Windows Management Instruction (WMI).</span></span>

<span data-ttu-id="e20f4-109">Certains scénarios nécessitent plus d'instructions sur la façon de déployer ou de configurer correctement la protection antivirus Microsoft Defender, telles que les environnements vDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="e20f4-109">Some scenarios require more guidance on how to successfully deploy or configure Microsoft Defender Antivirus protection, such as Virtual Desktop Infrastructure (VDI) environments.</span></span>

<span data-ttu-id="e20f4-110">L'article restant de cette section fournit des conseils de bout en bout et des meilleures pratiques pour la configuration de l'Antivirus Microsoft Defender sur des [machines virtuelles (VM)](deployment-vdi-microsoft-defender-antivirus.md)dans un environnement VDI ou RDS (Remote Desktop Services).</span><span class="sxs-lookup"><span data-stu-id="e20f4-110">The remaining article in this section provides end-to-end advice and best practices for [setting up Microsoft Defender Antivirus on virtual machines (VMs) in a VDI or Remote Desktop Services (RDS) environment](deployment-vdi-microsoft-defender-antivirus.md).</span></span>

## <a name="related-articles"></a><span data-ttu-id="e20f4-111">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="e20f4-111">Related articles</span></span>

- [<span data-ttu-id="e20f4-112">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="e20f4-112">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="e20f4-113">Déployer, gérer les mises à jour et signaler l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="e20f4-113">Deploy, manage updates, and report on Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="e20f4-114">Guide de déploiement de l'Antivirus Microsoft Defender dans un environnement d'infrastructure de bureau virtuel (VDI)</span><span class="sxs-lookup"><span data-stu-id="e20f4-114">Deployment guide for Microsoft Defender Antivirus in a virtual desktop infrastructure (VDI) environment</span></span>](deployment-vdi-microsoft-defender-antivirus.md)