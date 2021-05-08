---
title: Planifier les mises à jour Antivirus Microsoft Defender protection des données
description: Planifier le jour, l’heure et l’intervalle de téléchargement des mises à jour de protection
keywords: mises à jour, bases de référence de sécurité, planifier des mises à jour
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
search.appverid: met150
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: pahuijbr
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 26b88b8677c27a5d6615776a371326e37034afd4
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275035"
---
# <a name="manage-the-schedule-for-when-protection-updates-should-be-downloaded-and-applied"></a><span data-ttu-id="2a810-104">Gérer le calendrier de téléchargement et d’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="2a810-104">Manage the schedule for when protection updates should be downloaded and applied</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="2a810-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2a810-105">**Applies to:**</span></span>

- [<span data-ttu-id="2a810-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2a810-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="2a810-107">Antivirus Microsoft Defender vous permet de déterminer quand il doit rechercher et télécharger les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2a810-107">Microsoft Defender Antivirus lets you determine when it should look for and download updates.</span></span>

<span data-ttu-id="2a810-108">Vous pouvez planifier des mises à jour pour vos points de terminaison en :</span><span class="sxs-lookup"><span data-stu-id="2a810-108">You can schedule updates for your endpoints by:</span></span> 

- <span data-ttu-id="2a810-109">Spécification du jour de la semaine pour vérifier les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-109">Specifying the day of the week to check for protection updates</span></span> 
- <span data-ttu-id="2a810-110">Spécification de l’intervalle de recherche des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-110">Specifying the interval to check for protection updates</span></span>
- <span data-ttu-id="2a810-111">Spécification de l’heure de recherche des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-111">Specifying the time to check for protection updates</span></span>

<span data-ttu-id="2a810-112">Vous pouvez également aléatoirer les heures où chaque point de terminaison vérifie et télécharge les mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="2a810-112">You can also randomize the times when each endpoint checks and downloads protection updates.</span></span> <span data-ttu-id="2a810-113">Pour plus [d’informations, consultez](scheduled-catch-up-scans-microsoft-defender-antivirus.md) la rubrique Analyses de planification.</span><span class="sxs-lookup"><span data-stu-id="2a810-113">See the [Schedule scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md) topic for more information.</span></span>

## <a name="use-configuration-manager-to-schedule-protection-updates"></a><span data-ttu-id="2a810-114">Utiliser Configuration Manager pour planifier des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-114">Use Configuration Manager to schedule protection updates</span></span>

1.  <span data-ttu-id="2a810-115">Sur votre console Microsoft Endpoint Manager, ouvrez la stratégie anti-programme malveillant à modifier (cliquez sur Ressources et conformité dans le volet de navigation à gauche, puis développez l’arborescence Vue d’ensemble Endpoint Protection **Stratégies**  >    >  **anti-programme** malveillant)</span><span class="sxs-lookup"><span data-stu-id="2a810-115">On your Microsoft Endpoint Manager console, open the antimalware policy you want to change (click **Assets and Compliance** in the navigation pane on the left, then expand the tree to **Overview** > **Endpoint Protection** > **Antimalware Policies**)</span></span>

2.  <span data-ttu-id="2a810-116">Go to the **Security intelligence updates** section.</span><span class="sxs-lookup"><span data-stu-id="2a810-116">Go to the **Security intelligence updates** section.</span></span>

3. <span data-ttu-id="2a810-117">Pour vérifier et télécharger les mises à jour à un moment certain :</span><span class="sxs-lookup"><span data-stu-id="2a810-117">To check and download updates at a certain time:</span></span>
      1. <span data-ttu-id="2a810-118">Définissez **Check for Endpoint Protection security intelligence updates at a specific interval...** to **0**.</span><span class="sxs-lookup"><span data-stu-id="2a810-118">Set **Check for Endpoint Protection security intelligence updates at a specific interval...** to **0**.</span></span>
      2. <span data-ttu-id="2a810-119">Définissez La vérification Endpoint Protection mises à jour de l’intelligence de sécurité **quotidiennement à...** au moment où les mises à jour doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="2a810-119">Set **Check for Endpoint Protection security intelligence updates daily at...** to the time when updates should be checked.</span></span>
      <span data-ttu-id="2a810-120">3</span><span class="sxs-lookup"><span data-stu-id="2a810-120">3</span></span>
4. <span data-ttu-id="2a810-121">Pour vérifier et télécharger les mises à jour sur un intervalle continu, définissez vérifier les mises à jour de l’intelligence de sécurité Endpoint Protection à un intervalle **spécifique...** au nombre d’heures qui doivent se produire entre les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2a810-121">To check and download updates on a continual interval, Set **Check for Endpoint Protection security intelligence updates at a specific interval...** to the number of hours that should occur between updates.</span></span>

5.  <span data-ttu-id="2a810-122">[Déployez la stratégie mise à jour comme d’habitude.](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers)</span><span class="sxs-lookup"><span data-stu-id="2a810-122">[Deploy the updated policy as usual](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers).</span></span>

## <a name="use-group-policy-to-schedule-protection-updates"></a><span data-ttu-id="2a810-123">Utiliser une stratégie de groupe pour planifier des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-123">Use Group Policy to schedule protection updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a810-124">Par défaut, Antivirus Microsoft Defender recherche une mise à jour 15 minutes avant l’heure des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="2a810-124">By default, Microsoft Defender Antivirus will check for an update 15 minutes before the time of any scheduled scans.</span></span> <span data-ttu-id="2a810-125">L’activation de ces paramètres remplace cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a810-125">Enabling these settings will override that default.</span></span>

1.  <span data-ttu-id="2a810-126">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="2a810-126">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="2a810-127">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="2a810-127">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="2a810-128">Cliquez **sur Stratégies** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="2a810-128">Click **Policies** then **Administrative templates**.</span></span>

5.  <span data-ttu-id="2a810-129">Développez l’arborescence **Windows composants Antivirus Microsoft Defender** mises à jour Signature Intelligence et  >    >   configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2a810-129">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Signature Intelligence Updates** and configure the following settings:</span></span>

    1. <span data-ttu-id="2a810-130">Double-cliquez sur **Spécifier le jour de** la semaine pour vérifier le paramètre des mises à jour de l’intelligence de la sécurité et définir l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="2a810-130">Double-click the **Specify the day of the week to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="2a810-131">Entrez le jour de la semaine pour vérifier les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2a810-131">Enter the day of the week to check for updates.</span></span> <span data-ttu-id="2a810-132">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a810-132">Click **OK**.</span></span>
    2. <span data-ttu-id="2a810-133">Double-cliquez sur **spécifier l’intervalle pour vérifier** le paramètre des mises à jour de l’intelligence de la sécurité et définir l’option **sur Activé**.</span><span class="sxs-lookup"><span data-stu-id="2a810-133">Double-click the **Specify the interval to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="2a810-134">Entrez le nombre d’heures entre les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2a810-134">Enter the number of hours between updates.</span></span> <span data-ttu-id="2a810-135">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a810-135">Click **OK**.</span></span>
    3. <span data-ttu-id="2a810-136">Double-cliquez sur **le paramètre Spécifier l’heure** à définir pour les mises à jour de l’intelligence de la sécurité et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="2a810-136">Double-click the **Specify the time to check for security intelligence updates** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="2a810-137">Entrez l’heure à quel moment les mises à jour doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="2a810-137">Enter the time when updates should be checked.</span></span> <span data-ttu-id="2a810-138">L’heure est basée sur l’heure locale du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2a810-138">The time is based on the local time of the endpoint.</span></span> <span data-ttu-id="2a810-139">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a810-139">Click **OK**.</span></span>


## <a name="use-powershell-cmdlets-to-schedule-protection-updates"></a><span data-ttu-id="2a810-140">Utiliser les cmdlets PowerShell pour planifier des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="2a810-140">Use PowerShell cmdlets to schedule protection updates</span></span>

<span data-ttu-id="2a810-141">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a810-141">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -SignatureScheduleDay
Set-MpPreference -SignatureScheduleTime
Set-MpPreference -SignatureUpdateInterval
```

<span data-ttu-id="2a810-142">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="2a810-142">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md)  and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="use-windows-management-instruction-wmi-to-schedule-protection-updates"></a><span data-ttu-id="2a810-143">Utiliser Windows Management Instruction (WMI) pour planifier des mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="2a810-143">Use Windows Management Instruction (WMI) to schedule protection updates</span></span>

<span data-ttu-id="2a810-144">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a810-144">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
SignatureScheduleDay
SignatureScheduleTime
SignatureUpdateInterval
```

<span data-ttu-id="2a810-145">Pour plus d’informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a810-145">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="2a810-146">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="2a810-146">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


## <a name="related-articles"></a><span data-ttu-id="2a810-147">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="2a810-147">Related articles</span></span>

- [<span data-ttu-id="2a810-148">Déployer Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="2a810-148">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="2a810-149">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="2a810-149">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="2a810-150">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="2a810-150">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md)
- [<span data-ttu-id="2a810-151">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="2a810-151">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md)
- [<span data-ttu-id="2a810-152">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="2a810-152">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)
- [<span data-ttu-id="2a810-153">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="2a810-153">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)