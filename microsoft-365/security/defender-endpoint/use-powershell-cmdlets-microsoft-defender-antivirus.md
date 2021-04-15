---
title: Utiliser les cmdlets PowerShell pour configurer et exécuter Microsoft Defender AV
description: Dans Windows 10, vous pouvez utiliser les cmdlets PowerShell pour exécuter des analyses, mettre à jour les informations de sécurité et modifier les paramètres dans l'Antivirus Microsoft Defender.
keywords: analyse, ligne de commande, mpcmdrun, defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 07/23/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
audience: ITPro
ms.topic: how-to
ms.openlocfilehash: 0fd1e6b2eec1be722af58e0753e158c050b56c6b
ms.sourcegitcommit: 07dea2aa98daf0c4086f8590375167830027c802
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51749875"
---
# <a name="use-powershell-cmdlets-to-configure-and-manage-microsoft-defender-antivirus"></a><span data-ttu-id="33387-104">Utiliser les cmdlets PowerShell pour configurer et gérer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="33387-104">Use PowerShell cmdlets to configure and manage Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="33387-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="33387-105">**Applies to:**</span></span>

- [<span data-ttu-id="33387-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="33387-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="33387-107">Vous pouvez utiliser PowerShell pour effectuer diverses fonctions dans Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="33387-107">You can use PowerShell to perform various functions in Windows Defender.</span></span> <span data-ttu-id="33387-108">À l'exemple de l'invite de commandes ou de la ligne de commande, PowerShell est un shell de ligne de commande basé sur des tâches et un langage de script spécialement conçu pour l'administration du système.</span><span class="sxs-lookup"><span data-stu-id="33387-108">Similar to the command prompt or command line, PowerShell is a task-based command-line shell and scripting language designed especially for system administration.</span></span> <span data-ttu-id="33387-109">Pour en savoir plus, consultez le hub [PowerShell sur MSDN.](/previous-versions/msdn10/mt173057(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="33387-109">You can read more about it at the [PowerShell hub on MSDN](/previous-versions/msdn10/mt173057(v=msdn.10)).</span></span>

<span data-ttu-id="33387-110">Pour obtenir la liste des cmdlets, leurs fonctions et les paramètres disponibles, consultez la rubrique sur les [cmdlets Defender.](/powershell/module/defender)</span><span class="sxs-lookup"><span data-stu-id="33387-110">For a list of the cmdlets and their functions and available parameters, see the [Defender cmdlets](/powershell/module/defender) topic.</span></span>

<span data-ttu-id="33387-111">Les cmdlets PowerShell sont particulièrement utiles dans les environnements Windows Server qui ne reposent pas sur une interface utilisateur graphique (GUI) pour configurer des logiciels.</span><span class="sxs-lookup"><span data-stu-id="33387-111">PowerShell cmdlets are most useful in Windows Server environments that don't rely on a graphical user interface (GUI) to configure software.</span></span>

> [!NOTE]
> <span data-ttu-id="33387-112">Les cmdlets PowerShell ne doivent pas être utilisées en remplacement d'une infrastructure de gestion de stratégie de réseau complète, telle que [Microsoft Endpoint Configuration Manager,](/configmgr)la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe ou les [modèles ADMX](https://www.microsoft.com/download/101445)de stratégie de groupe antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="33387-112">PowerShell cmdlets should not be used as a replacement for a full network policy management infrastructure, such as [Microsoft Endpoint Configuration Manager](/configmgr), [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), or [Microsoft Defender Antivirus Group Policy ADMX templates](https://www.microsoft.com/download/101445).</span></span>

<span data-ttu-id="33387-113">Les modifications apportées avec PowerShell affecteront les paramètres locaux sur le point de terminaison où les modifications sont déployées ou apportées.</span><span class="sxs-lookup"><span data-stu-id="33387-113">Changes made with PowerShell will affect local settings on the endpoint where the changes are deployed or made.</span></span> <span data-ttu-id="33387-114">Cela signifie que les déploiements de stratégie avec la stratégie de groupe, Microsoft Endpoint Configuration Manager ou Microsoft Intune peuvent modifier les modifications apportées avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33387-114">This means that deployments of policy with Group Policy, Microsoft Endpoint Configuration Manager, or Microsoft Intune can overwrite changes made with PowerShell.</span></span>

<span data-ttu-id="33387-115">Vous pouvez configurer les paramètres qui peuvent être remplacer localement avec les [remplacements de stratégie locale.](configure-local-policy-overrides-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="33387-115">You can [configure which settings can be overridden locally with local policy overrides](configure-local-policy-overrides-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="33387-116">PowerShell est généralement installé sous le `%SystemRoot%\system32\WindowsPowerShell` dossier.</span><span class="sxs-lookup"><span data-stu-id="33387-116">PowerShell is typically installed under the folder `%SystemRoot%\system32\WindowsPowerShell`.</span></span>

## <a name="use-microsoft-defender-antivirus-powershell-cmdlets"></a><span data-ttu-id="33387-117">Utiliser les cmdlets De l'Antivirus Microsoft Defender PowerShell</span><span class="sxs-lookup"><span data-stu-id="33387-117">Use Microsoft Defender Antivirus PowerShell cmdlets</span></span>

1. <span data-ttu-id="33387-118">Dans la barre de recherche Windows, tapez **powershell.**</span><span class="sxs-lookup"><span data-stu-id="33387-118">In the Windows search bar, type **powershell**.</span></span>
2. <span data-ttu-id="33387-119">Sélectionnez **Windows PowerShell** dans les résultats pour ouvrir l'interface.</span><span class="sxs-lookup"><span data-stu-id="33387-119">Select **Windows PowerShell** from the results to open the interface.</span></span>
3. <span data-ttu-id="33387-120">Entrez la commande PowerShell et tous les paramètres.</span><span class="sxs-lookup"><span data-stu-id="33387-120">Enter the PowerShell command and any parameters.</span></span>

> [!NOTE]
> <span data-ttu-id="33387-121">Vous devrez peut-être ouvrir PowerShell en mode administrateur.</span><span class="sxs-lookup"><span data-stu-id="33387-121">You may need to open PowerShell in administrator mode.</span></span> <span data-ttu-id="33387-122">Cliquez avec le bouton droit sur l'élément dans le menu Démarrer, cliquez sur Exécuter **en** tant qu'administrateur et cliquez sur **Oui** à l'invite d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="33387-122">Right-click the item in the Start menu, click **Run as administrator** and click **Yes** at the permissions prompt.</span></span>

<span data-ttu-id="33387-123">Pour ouvrir l'aide en ligne pour l'une des cmdlets, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="33387-123">To open online help for any of the cmdlets type the following:</span></span>

```PowerShell
Get-Help <cmdlet> -Online
```

<span data-ttu-id="33387-124">Omettez le `-online` paramètre pour obtenir de l'aide mise en cache localement.</span><span class="sxs-lookup"><span data-stu-id="33387-124">Omit the `-online` parameter to get locally cached help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33387-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33387-125">Related topics</span></span>

- [<span data-ttu-id="33387-126">Rubriques de référence pour les outils de gestion et de configuration</span><span class="sxs-lookup"><span data-stu-id="33387-126">Reference topics for management and configuration tools</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="33387-127">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="33387-127">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="33387-128">Cmdlets de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="33387-128">Microsoft Defender Antivirus Cmdlets</span></span>](/powershell/module/defender)