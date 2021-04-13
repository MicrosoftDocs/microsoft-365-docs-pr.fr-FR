---
title: Appliquer les mises à jour de l'Antivirus Microsoft Defender après certains événements
description: Gérer la façon dont l'Antivirus Microsoft Defender applique les mises à jour de l'intelligence de sécurité après le démarrage ou la réception de rapports de détection remis par le cloud.
keywords: mises à jour, protection, forcer les mises à jour, événements, démarrage, vérifier les dernières mises à jour, notifications
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/17/2018
ms.reviewer: pahuijbr
manager: dansimp
ms.technology: mde
ms.openlocfilehash: b9f09878c645d54aadca21fe01749a0e73939c5f
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690435"
---
# <a name="manage-event-based-forced-updates"></a><span data-ttu-id="414de-104">Gérer les mises à jour forcées basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="414de-104">Manage event-based forced updates</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="414de-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="414de-105">**Applies to:**</span></span>

- [<span data-ttu-id="414de-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="414de-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="414de-107">L'Antivirus Microsoft Defender vous permet de déterminer si des mises à jour doivent (ou ne doivent pas) se produire après certains événements, par exemple au démarrage ou après la réception de rapports spécifiques du service de protection livré par le cloud.</span><span class="sxs-lookup"><span data-stu-id="414de-107">Microsoft Defender Antivirus allows you to determine if updates should (or should not) occur after certain events, such as at startup or after receiving specific reports from the cloud-delivered protection service.</span></span>

## <a name="check-for-protection-updates-before-running-a-scan"></a><span data-ttu-id="414de-108">Vérifier les mises à jour de la protection avant d'exécution d'une analyse</span><span class="sxs-lookup"><span data-stu-id="414de-108">Check for protection updates before running a scan</span></span>

<span data-ttu-id="414de-109">Vous pouvez utiliser Microsoft Endpoint Configuration Manager, la stratégie de groupe, les cmdlets PowerShell et WMI pour forcer l'Antivirus Microsoft Defender à vérifier et télécharger les mises à jour de la protection avant d'exécution d'une analyse programmée.</span><span class="sxs-lookup"><span data-stu-id="414de-109">You can use Microsoft Endpoint Configuration Manager, Group Policy, PowerShell cmdlets, and WMI to force Microsoft Defender Antivirus to check and download protection updates before running a scheduled scan.</span></span>

### <a name="use-configuration-manager-to-check-for-protection-updates-before-running-a-scan"></a><span data-ttu-id="414de-110">Utiliser Configuration Manager pour vérifier les mises à jour de la protection avant d'exécution d'une analyse</span><span class="sxs-lookup"><span data-stu-id="414de-110">Use Configuration Manager to check for protection updates before running a scan</span></span>

1. <span data-ttu-id="414de-111">Sur votre console Microsoft Endpoint Manager, ouvrez la stratégie anti-programme malveillant à modifier (cliquez sur Ressources et conformité dans le volet de navigation sur la gauche, puis développez l'arborescence Vue d'ensemble des **stratégies** anti-programme malveillant  >  **endpoint Protection)**  >  </span><span class="sxs-lookup"><span data-stu-id="414de-111">On your Microsoft Endpoint Manager console, open the antimalware policy you want to change (click **Assets and Compliance** in the navigation pane on the left, then expand the tree to **Overview** > **Endpoint Protection** > **Antimalware Policies**)</span></span>

2. <span data-ttu-id="414de-112">Go to the **Scheduled scans** section and set **Check for the latest security intelligence updates before running a scan** to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="414de-112">Go to the **Scheduled scans** section and set **Check for the latest security intelligence updates before running a scan** to **Yes**.</span></span>

3. <span data-ttu-id="414de-113">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-113">Click **OK**.</span></span>

4. <span data-ttu-id="414de-114">[Déployez la stratégie mise à jour comme d'habitude.](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers)</span><span class="sxs-lookup"><span data-stu-id="414de-114">[Deploy the updated policy as usual](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers).</span></span>

### <a name="use-group-policy-to-check-for-protection-updates-before-running-a-scan"></a><span data-ttu-id="414de-115">Utiliser la stratégie de groupe pour vérifier les mises à jour de la protection avant d'exécution d'une analyse</span><span class="sxs-lookup"><span data-stu-id="414de-115">Use Group Policy to check for protection updates before running a scan</span></span>

1. <span data-ttu-id="414de-116">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="414de-116">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="414de-117">À **l'aide de l'Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="414de-117">Using the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="414de-118">Cliquez **sur Stratégies** **puis Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="414de-118">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="414de-119">Développez l'arborescence **des composants Windows**  >  **Analyse antivirus Microsoft Defender.**  >  </span><span class="sxs-lookup"><span data-stu-id="414de-119">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

5. <span data-ttu-id="414de-120">Double-cliquez sur Vérifier les dernières définitions de virus et de **logiciels espions** avant d'exécutez une analyse programmée et définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="414de-120">Double-click **Check for the latest virus and spyware definitions before running a scheduled scan** and set the option to **Enabled**.</span></span>

6. <span data-ttu-id="414de-121">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-121">Click **OK**.</span></span>

### <a name="use-powershell-cmdlets-to-check-for-protection-updates-before-running-a-scan"></a><span data-ttu-id="414de-122">Utiliser les cmdlets PowerShell pour vérifier les mises à jour de la protection avant d'exécution d'une analyse</span><span class="sxs-lookup"><span data-stu-id="414de-122">Use PowerShell cmdlets to check for protection updates before running a scan</span></span>

<span data-ttu-id="414de-123">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="414de-123">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -CheckForSignaturesBeforeRunningScan
```

<span data-ttu-id="414de-124">Pour plus d'informations, voir [Utiliser les cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et [les cmdlets Defender.](/powershell/module/defender/index)</span><span class="sxs-lookup"><span data-stu-id="414de-124">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/index).</span></span>

### <a name="use-windows-management-instruction-wmi-to-check-for-protection-updates-before-running-a-scan"></a><span data-ttu-id="414de-125">Utiliser Windows Management Instruction (WMI) pour vérifier les mises à jour de la protection avant d'exécution d'une analyse</span><span class="sxs-lookup"><span data-stu-id="414de-125">Use Windows Management Instruction (WMI) to check for protection updates before running a scan</span></span>

<span data-ttu-id="414de-126">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="414de-126">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
CheckForSignaturesBeforeRunningScan
```

<span data-ttu-id="414de-127">Pour plus d'informations, [voir Windows Defender API WMIv2.](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="414de-127">For more information, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

## <a name="check-for-protection-updates-on-startup"></a><span data-ttu-id="414de-128">Vérifier les mises à jour de la protection au démarrage</span><span class="sxs-lookup"><span data-stu-id="414de-128">Check for protection updates on startup</span></span>

<span data-ttu-id="414de-129">Vous pouvez utiliser la stratégie de groupe pour forcer l'Antivirus Microsoft Defender à vérifier et télécharger les mises à jour de la protection lorsque l'ordinateur est démarré.</span><span class="sxs-lookup"><span data-stu-id="414de-129">You can use Group Policy to force Microsoft Defender Antivirus to check and download protection updates when the machine is started.</span></span>

1. <span data-ttu-id="414de-130">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="414de-130">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="414de-131">À **l'aide de l'Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="414de-131">Using the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="414de-132">Cliquez **sur Stratégies** **puis Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="414de-132">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="414de-133">Développez l'arborescence des **composants Windows**  >  **microsoft Defender Antivirus** Security Intelligence  >  **Updates.**</span><span class="sxs-lookup"><span data-stu-id="414de-133">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Security Intelligence Updates**.</span></span>

5. <span data-ttu-id="414de-134">Double-cliquez sur Vérifier les dernières définitions de virus et de **logiciels espions** au démarrage et définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="414de-134">Double-click **Check for the latest virus and spyware definitions on startup** and set the option to **Enabled**.</span></span> 

6. <span data-ttu-id="414de-135">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-135">Click **OK**.</span></span>

<span data-ttu-id="414de-136">Vous pouvez également utiliser la stratégie de groupe, PowerShell ou WMI pour configurer l'Antivirus Microsoft Defender afin de vérifier les mises à jour au démarrage, même lorsqu'il n'est pas en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="414de-136">You can also use Group Policy, PowerShell, or WMI to configure Microsoft Defender Antivirus to check for updates at startup even when it is not running.</span></span>

### <a name="use-group-policy-to-download-updates-when-microsoft-defender-antivirus-is-not-present"></a><span data-ttu-id="414de-137">Utiliser la stratégie de groupe pour télécharger les mises à jour lorsque l'Antivirus Microsoft Defender n'est pas présent</span><span class="sxs-lookup"><span data-stu-id="414de-137">Use Group Policy to download updates when Microsoft Defender Antivirus is not present</span></span>

1. <span data-ttu-id="414de-138">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="414de-138">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="414de-139">À l'aide **de l'Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="414de-139">Using the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

3. <span data-ttu-id="414de-140">Cliquez **sur Stratégies** **puis Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="414de-140">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="414de-141">Développez l'arborescence **des composants Windows**  >  **microsoft Defender Antivirus** Security Intelligence  >  **Updates.**</span><span class="sxs-lookup"><span data-stu-id="414de-141">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Security Intelligence Updates**.</span></span>

5. <span data-ttu-id="414de-142">Double-cliquez sur **Lancer la mise à jour de l'intelligence** de sécurité au démarrage et définissez l'option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="414de-142">Double-click **Initiate security intelligence update on startup** and set the option to **Enabled**.</span></span>

6. <span data-ttu-id="414de-143">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-143">Click **OK**.</span></span>

### <a name="use-powershell-cmdlets-to-download-updates-when-microsoft-defender-antivirus-is-not-present"></a><span data-ttu-id="414de-144">Utiliser les cmdlets PowerShell pour télécharger les mises à jour lorsque l'Antivirus Microsoft Defender n'est pas présent</span><span class="sxs-lookup"><span data-stu-id="414de-144">Use PowerShell cmdlets to download updates when Microsoft Defender Antivirus is not present</span></span>

<span data-ttu-id="414de-145">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="414de-145">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -SignatureDisableUpdateOnStartupWithoutEngine
```

<span data-ttu-id="414de-146">Pour plus d'informations, consultez les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour gérer l'Antivirus Microsoft Defender et les [cmdlets Defender](/powershell/module/defender/index) pour plus d'informations sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="414de-146">For more information, see [Use PowerShell cmdlets to manage Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/index) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-download-updates-when-microsoft-defender-antivirus-is-not-present"></a><span data-ttu-id="414de-147">Utiliser Windows Management Instruction (WMI) pour télécharger les mises à jour lorsque l'Antivirus Microsoft Defender n'est pas présent</span><span class="sxs-lookup"><span data-stu-id="414de-147">Use Windows Management Instruction (WMI) to download updates when Microsoft Defender Antivirus is not present</span></span>

<span data-ttu-id="414de-148">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="414de-148">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
SignatureDisableUpdateOnStartupWithoutEngine
```

<span data-ttu-id="414de-149">Pour plus d'informations, [voir Windows Defender API WMIv2.](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="414de-149">For more information, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

<a id="cloud-report-updates"></a>

## <a name="allow-ad-hoc-changes-to-protection-based-on-cloud-delivered-protection"></a><span data-ttu-id="414de-150">Autoriser des modifications ad hoc à la protection basée sur la protection fourni par le cloud</span><span class="sxs-lookup"><span data-stu-id="414de-150">Allow ad hoc changes to protection based on cloud-delivered protection</span></span>

<span data-ttu-id="414de-151">L'Antivirus Microsoft Defender peut apporter des modifications à sa protection en fonction de la protection livrée par le cloud.</span><span class="sxs-lookup"><span data-stu-id="414de-151">Microsoft Defender AV can make changes to its protection based on cloud-delivered protection.</span></span> <span data-ttu-id="414de-152">De telles modifications peuvent se produire en dehors des mises à jour de protection normales ou programmées.</span><span class="sxs-lookup"><span data-stu-id="414de-152">Such changes can occur outside of normal or scheduled protection updates.</span></span>

<span data-ttu-id="414de-153">Si vous avez activé la protection cloud, l'Antivirus Microsoft Defender envoie les fichiers qu'il suspecte au cloud Windows Defender cloud.</span><span class="sxs-lookup"><span data-stu-id="414de-153">If you have enabled cloud-delivered protection, Microsoft Defender AV will send files it is suspicious about to the Windows Defender cloud.</span></span> <span data-ttu-id="414de-154">Si le service cloud signale que le fichier est malveillant et qu'il est détecté dans une mise à jour de protection récente, vous pouvez utiliser la stratégie de groupe pour configurer Microsoft Defender AV afin qu'il reçoive automatiquement cette mise à jour de protection.</span><span class="sxs-lookup"><span data-stu-id="414de-154">If the cloud service reports that the file is malicious, and the file is detected in a recent protection update, you can use Group Policy to configure Microsoft Defender AV to automatically receive that protection update.</span></span> <span data-ttu-id="414de-155">D'autres mises à jour de protection importantes peuvent également être appliquées.</span><span class="sxs-lookup"><span data-stu-id="414de-155">Other important protection updates can also be applied.</span></span>

### <a name="use-group-policy-to-automatically-download-recent-updates-based-on-cloud-delivered-protection"></a><span data-ttu-id="414de-156">Utiliser la stratégie de groupe pour télécharger automatiquement les mises à jour récentes en fonction de la protection du cloud</span><span class="sxs-lookup"><span data-stu-id="414de-156">Use Group Policy to automatically download recent updates based on cloud-delivered protection</span></span>

1. <span data-ttu-id="414de-157">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="414de-157">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="414de-158">À **l'aide de l'Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="414de-158">Using the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="414de-159">Cliquez **sur Stratégies** **puis Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="414de-159">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="414de-160">Développez l'arborescence **des composants Windows**  >  **microsoft Defender Antivirus** Security Intelligence  >  **Updates.**</span><span class="sxs-lookup"><span data-stu-id="414de-160">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Security Intelligence Updates**.</span></span>

5. <span data-ttu-id="414de-161">Double-cliquez sur Autoriser les mises à jour d'informations de sécurité en temps réel **basées** sur les rapports de Microsoft MAPS et définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="414de-161">Double-click **Allow real-time security intelligence updates based on reports to Microsoft MAPS** and set the option to **Enabled**.</span></span> <span data-ttu-id="414de-162">Cliquez ensuite sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-162">Then click **OK**.</span></span>

6. <span data-ttu-id="414de-163">**Autoriser les notifications à désactiver les rapports** basés sur des définitions pour Microsoft MAPS et définir l'option sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="414de-163">**Allow notifications to disable definitions-based reports to Microsoft MAPS** and set the option to **Enabled**.</span></span> <span data-ttu-id="414de-164">Cliquez ensuite sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="414de-164">Then click **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="414de-165">**Autoriser les notifications à désactiver les** rapports basés sur des définitions permet à Microsoft MAPS de désactiver ces définitions connues pour provoquer des rapports faux positifs.</span><span class="sxs-lookup"><span data-stu-id="414de-165">**Allow notifications to disable definitions based reports** enables Microsoft MAPS to disable those definitions known to cause false-positive reports.</span></span> <span data-ttu-id="414de-166">Vous devez configurer votre ordinateur pour qu'il rejoigne Microsoft MAPS pour que cette fonction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="414de-166">You must configure your computer to join Microsoft MAPS for this function to work.</span></span>

## <a name="see-also"></a><span data-ttu-id="414de-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414de-167">See also</span></span>

- [<span data-ttu-id="414de-168">Déployer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="414de-168">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="414de-169">Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="414de-169">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="414de-170">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="414de-170">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md)
- [<span data-ttu-id="414de-171">Gérer les mises à jour des points de terminaison qui ne sont pas à jour</span><span class="sxs-lookup"><span data-stu-id="414de-171">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md)
- [<span data-ttu-id="414de-172">Gérer les mises à jour pour les périphériques mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="414de-172">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)
- [<span data-ttu-id="414de-173">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="414de-173">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)