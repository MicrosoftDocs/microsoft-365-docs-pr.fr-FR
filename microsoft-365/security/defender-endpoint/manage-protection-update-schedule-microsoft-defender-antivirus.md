---
title: Planifier les mises à jour de la protection antivirus Microsoft Defender
description: Planifier le jour, l'heure et l'intervalle de téléchargement des mises à jour de protection
keywords: mises à jour, bases de référence de sécurité, planifier des mises à jour
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
search.appverid: met150
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: pahuijbr
manager: dansimp
ms.technology: mde
ms.openlocfilehash: e4ba9a438ff4640a556a236b50b0be6e816fc7e8
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690426"
---
# <a name="manage-the-schedule-for-when-protection-updates-should-be-downloaded-and-applied"></a><span data-ttu-id="b1b47-104">Gérer la planification du téléchargement et de l'application des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-104">Manage the schedule for when protection updates should be downloaded and applied</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b1b47-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b1b47-105">**Applies to:**</span></span>

- [<span data-ttu-id="b1b47-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b1b47-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="b1b47-107">L'Antivirus Microsoft Defender vous permet de déterminer quand il doit rechercher et télécharger les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b1b47-107">Microsoft Defender Antivirus lets you determine when it should look for and download updates.</span></span>

<span data-ttu-id="b1b47-108">Vous pouvez planifier des mises à jour pour vos points de terminaison en :</span><span class="sxs-lookup"><span data-stu-id="b1b47-108">You can schedule updates for your endpoints by:</span></span> 

- <span data-ttu-id="b1b47-109">Spécification du jour de la semaine pour vérifier les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-109">Specifying the day of the week to check for protection updates</span></span> 
- <span data-ttu-id="b1b47-110">Spécification de l'intervalle de recherche des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-110">Specifying the interval to check for protection updates</span></span>
- <span data-ttu-id="b1b47-111">Spécification de l'heure de recherche des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-111">Specifying the time to check for protection updates</span></span>

<span data-ttu-id="b1b47-112">Vous pouvez également aléatoirer le moment où chaque point de terminaison vérifie et télécharge les mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="b1b47-112">You can also randomize the times when each endpoint checks and downloads protection updates.</span></span> <span data-ttu-id="b1b47-113">Pour plus [d'informations, voir](scheduled-catch-up-scans-microsoft-defender-antivirus.md) la rubrique Planifier les analyses.</span><span class="sxs-lookup"><span data-stu-id="b1b47-113">See the [Schedule scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md) topic for more information.</span></span>

## <a name="use-configuration-manager-to-schedule-protection-updates"></a><span data-ttu-id="b1b47-114">Utiliser Configuration Manager pour planifier des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-114">Use Configuration Manager to schedule protection updates</span></span>

1.  <span data-ttu-id="b1b47-115">Sur votre console Microsoft Endpoint Manager, ouvrez la stratégie anti-programme malveillant à modifier (cliquez sur Ressources et conformité dans le volet de navigation à gauche, puis développez l'arborescence Vue d'ensemble des **stratégies** anti-programme malveillant  >  **endpoint Protection)**  >  </span><span class="sxs-lookup"><span data-stu-id="b1b47-115">On your Microsoft Endpoint Manager console, open the antimalware policy you want to change (click **Assets and Compliance** in the navigation pane on the left, then expand the tree to **Overview** > **Endpoint Protection** > **Antimalware Policies**)</span></span>

2.  <span data-ttu-id="b1b47-116">Go to the **Security intelligence updates** section.</span><span class="sxs-lookup"><span data-stu-id="b1b47-116">Go to the **Security intelligence updates** section.</span></span>

3. <span data-ttu-id="b1b47-117">Pour vérifier et télécharger les mises à jour à un moment certain :</span><span class="sxs-lookup"><span data-stu-id="b1b47-117">To check and download updates at a certain time:</span></span>
      1. <span data-ttu-id="b1b47-118">Définissez **Check for Endpoint Protection security intelligence updates at a specific interval...** to **0**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-118">Set **Check for Endpoint Protection security intelligence updates at a specific interval...** to **0**.</span></span>
      2. <span data-ttu-id="b1b47-119">Définissez Vérifier les mises à jour **de l'intelligence** de sécurité endpoint Protection quotidiennement à l'heure où les mises à jour doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="b1b47-119">Set **Check for Endpoint Protection security intelligence updates daily at...** to the time when updates should be checked.</span></span>
      <span data-ttu-id="b1b47-120">3</span><span class="sxs-lookup"><span data-stu-id="b1b47-120">3</span></span>
4. <span data-ttu-id="b1b47-121">Pour vérifier et télécharger les mises à jour sur un intervalle continu, définissez Vérifier les mises à jour de l'intelligence de sécurité **endpoint Protection** à un intervalle spécifique... sur le nombre d'heures qui doivent se produire entre les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b1b47-121">To check and download updates on a continual interval, Set **Check for Endpoint Protection security intelligence updates at a specific interval...** to the number of hours that should occur between updates.</span></span>

5.  <span data-ttu-id="b1b47-122">[Déployez la stratégie mise à jour comme d'habitude.](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers)</span><span class="sxs-lookup"><span data-stu-id="b1b47-122">[Deploy the updated policy as usual](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers).</span></span>

## <a name="use-group-policy-to-schedule-protection-updates"></a><span data-ttu-id="b1b47-123">Utiliser la stratégie de groupe pour planifier des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-123">Use Group Policy to schedule protection updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1b47-124">Par défaut, l'Antivirus Microsoft Defender recherche une mise à jour 15 minutes avant l'heure des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="b1b47-124">By default, Microsoft Defender Antivirus will check for an update 15 minutes before the time of any scheduled scans.</span></span> <span data-ttu-id="b1b47-125">L'activation de ces paramètres remplace cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1b47-125">Enabling these settings will override that default.</span></span>

1.  <span data-ttu-id="b1b47-126">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b1b47-126">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="b1b47-127">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b1b47-127">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="b1b47-128">Cliquez **sur Stratégies** **puis Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="b1b47-128">Click **Policies** then **Administrative templates**.</span></span>

5.  <span data-ttu-id="b1b47-129">Développez l'arborescence **des composants Windows** mises à jour  >  **de l'Antivirus Microsoft Defender** Signature Intelligence et  >   configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b1b47-129">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Signature Intelligence Updates** and configure the following settings:</span></span>

    1. <span data-ttu-id="b1b47-130">Double-cliquez sur **spécifier le jour de** la semaine pour vérifier le paramètre des mises à jour de l'intelligence de la sécurité et définir l'option **sur Activé**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-130">Double-click the **Specify the day of the week to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="b1b47-131">Entrez le jour de la semaine pour vérifier les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b1b47-131">Enter the day of the week to check for updates.</span></span> <span data-ttu-id="b1b47-132">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-132">Click **OK**.</span></span>
    2. <span data-ttu-id="b1b47-133">Double-cliquez sur **spécifier l'intervalle pour vérifier** le paramètre des mises à jour de l'intelligence de la sécurité et définir l'option **sur Activé**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-133">Double-click the **Specify the interval to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="b1b47-134">Entrez le nombre d'heures entre les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b1b47-134">Enter the number of hours between updates.</span></span> <span data-ttu-id="b1b47-135">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-135">Click **OK**.</span></span>
    3. <span data-ttu-id="b1b47-136">Double-cliquez sur **le paramètre Spécifier l'heure** à définir pour les mises à jour de l'intelligence de la sécurité et définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="b1b47-136">Double-click the **Specify the time to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="b1b47-137">Entrez l'heure à quel moment les mises à jour doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="b1b47-137">Enter the time when updates should be checked.</span></span> <span data-ttu-id="b1b47-138">L'heure est basée sur l'heure locale du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b1b47-138">The time is based on the local time of the endpoint.</span></span> <span data-ttu-id="b1b47-139">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b47-139">Click **OK**.</span></span>


## <a name="use-powershell-cmdlets-to-schedule-protection-updates"></a><span data-ttu-id="b1b47-140">Utiliser les cmdlets PowerShell pour planifier des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-140">Use PowerShell cmdlets to schedule protection updates</span></span>

<span data-ttu-id="b1b47-141">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1b47-141">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -SignatureScheduleDay
Set-MpPreference -SignatureScheduleTime
Set-MpPreference -SignatureUpdateInterval
```

<span data-ttu-id="b1b47-142">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md)  sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les cmdlets Utiliser PowerShell pour configurer et exécuter les [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="b1b47-142">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md)  and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="use-windows-management-instruction-wmi-to-schedule-protection-updates"></a><span data-ttu-id="b1b47-143">Utiliser Windows Management Instruction (WMI) pour planifier des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="b1b47-143">Use Windows Management Instruction (WMI) to schedule protection updates</span></span>

<span data-ttu-id="b1b47-144">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1b47-144">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
SignatureScheduleDay
SignatureScheduleTime
SignatureUpdateInterval
```

<span data-ttu-id="b1b47-145">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1b47-145">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="b1b47-146">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="b1b47-146">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


## <a name="related-articles"></a><span data-ttu-id="b1b47-147">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b1b47-147">Related articles</span></span>

- [<span data-ttu-id="b1b47-148">Déployer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b1b47-148">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b1b47-149">Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="b1b47-149">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b1b47-150">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="b1b47-150">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b1b47-151">Gérer les mises à jour forcées basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="b1b47-151">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b1b47-152">Gérer les mises à jour pour les périphériques mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="b1b47-152">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b1b47-153">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="b1b47-153">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)