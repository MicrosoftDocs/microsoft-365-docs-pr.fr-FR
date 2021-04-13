---
title: Configurer l'Antivirus Microsoft Defender avec WMI
description: Découvrez comment configurer et gérer l'Antivirus Microsoft Defender à l'aide de scripts WMI pour récupérer, modifier et mettre à jour les paramètres dans Microsoft Defender pour le point de terminaison.
keywords: wmi, scripts, instrumentation de gestion Windows, configuration
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 8d24a08ae3b8db710ca1727821690e5c87f056c3
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690531"
---
# <a name="use-windows-management-instrumentation-wmi-to-configure-and-manage-microsoft-defender-antivirus"></a><span data-ttu-id="54eaf-104">Utiliser Windows Management Instrumentation (WMI) pour configurer et gérer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="54eaf-104">Use Windows Management Instrumentation (WMI) to configure and manage Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="54eaf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="54eaf-105">**Applies to:**</span></span>

- [<span data-ttu-id="54eaf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="54eaf-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="54eaf-107">Windows Management Instrumentation (WMI) est une interface de script qui vous permet de récupérer, modifier et mettre à jour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="54eaf-107">Windows Management Instrumentation (WMI) is a scripting interface that allows you to retrieve, modify, and update settings.</span></span>

<span data-ttu-id="54eaf-108">Pour en savoir plus sur WMI, consultez la bibliothèque [Microsoft Developer Network System Administration.](/windows/win32/wmisdk/wmi-start-page)</span><span class="sxs-lookup"><span data-stu-id="54eaf-108">Read more about WMI at the [Microsoft Developer Network System Administration library](/windows/win32/wmisdk/wmi-start-page).</span></span>

<span data-ttu-id="54eaf-109">L'Antivirus Microsoft Defender possède un certain nombre de classes WMI spécifiques qui peuvent être utilisées pour effectuer la plupart des mêmes fonctions que la stratégie de groupe et d'autres outils de gestion.</span><span class="sxs-lookup"><span data-stu-id="54eaf-109">Microsoft Defender Antivirus has a number of specific WMI classes that can be used to perform most of the same functions as Group Policy and other management tools.</span></span> <span data-ttu-id="54eaf-110">La plupart des classes sont analogues aux [cmdlets Defender PowerShell.](use-powershell-cmdlets-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="54eaf-110">Many of the classes are analogous to [Defender PowerShell cmdlets](use-powershell-cmdlets-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="54eaf-111">La bibliothèque de référence du fournisseur [MSDN Windows Defender WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) répertorie les classes WMI disponibles pour l'Antivirus Microsoft Defender et inclut des exemples de scripts.</span><span class="sxs-lookup"><span data-stu-id="54eaf-111">The [MSDN Windows Defender WMIv2 Provider reference library](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) lists the available WMI classes for Microsoft Defender Antivirus, and includes example scripts.</span></span>

<span data-ttu-id="54eaf-112">Les modifications apportées avec WMI affecteront les paramètres locaux sur le point de terminaison où les modifications sont déployées ou apportées.</span><span class="sxs-lookup"><span data-stu-id="54eaf-112">Changes made with WMI will affect local settings on the endpoint where the changes are deployed or made.</span></span> <span data-ttu-id="54eaf-113">Cela signifie que les déploiements de stratégie avec la stratégie de groupe, Microsoft Endpoint Configuration Manager ou Microsoft Intune peuvent modifier les modifications apportées avec WMI.</span><span class="sxs-lookup"><span data-stu-id="54eaf-113">This means that deployments of policy with Group Policy, Microsoft Endpoint Configuration Manager, or Microsoft Intune can overwrite changes made with WMI.</span></span> 

<span data-ttu-id="54eaf-114">Vous pouvez configurer les paramètres qui peuvent être remplacer localement avec les [remplacements de stratégie locale.](configure-local-policy-overrides-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="54eaf-114">You can [configure which settings can be overridden locally  with local policy overrides](configure-local-policy-overrides-microsoft-defender-antivirus.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54eaf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54eaf-115">Related topics</span></span>

- [<span data-ttu-id="54eaf-116">Rubriques de référence pour les outils de gestion et de configuration</span><span class="sxs-lookup"><span data-stu-id="54eaf-116">Reference topics for management and configuration tools</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="54eaf-117">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="54eaf-117">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)