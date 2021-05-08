---
title: Appliquer les mises à jour de la protection de Microsoft Defender AV aux points de terminaison hors date
description: Définir quand et comment les mises à jour doivent être appliquées aux points de terminaison qui n’ont pas été mis à jour depuis un certain temps.
keywords: mises à jour, protection, obsolètes, obsolètes, ancien, rattrapage
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 4199f55488ef0dc5989af88e8be83a3d51190d1f
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275059"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-scans-for-endpoints-that-are-out-of-date"></a><span data-ttu-id="ffaca-104">Gérer les mises à jour de l'antivirus Microsoft Defender et les analyses des points de terminaison qui ne sont pas à jour</span><span class="sxs-lookup"><span data-stu-id="ffaca-104">Manage Microsoft Defender Antivirus updates and scans for endpoints that are out of date</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ffaca-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ffaca-105">**Applies to:**</span></span>

- [<span data-ttu-id="ffaca-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ffaca-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="ffaca-107">Antivirus Microsoft Defender vous permet de définir la durée pendant combien de temps un point de terminaison peut éviter une mise à jour ou le nombre d’analyses qu’il peut manquer avant d’être tenu de se mettre à jour et de s’analyser lui-même.</span><span class="sxs-lookup"><span data-stu-id="ffaca-107">Microsoft Defender Antivirus lets you define how long an endpoint can avoid an update or how many scans it can miss before it is required to update and scan itself.</span></span> <span data-ttu-id="ffaca-108">Cela est particulièrement utile dans les environnements où les appareils ne sont pas souvent connectés à un réseau d’entreprise ou externe, ou les appareils qui ne sont pas utilisés quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="ffaca-108">This is especially useful in environments where devices are not often connected to a corporate or external network, or devices that are not used on a daily basis.</span></span>

<span data-ttu-id="ffaca-109">Par exemple, un employé qui utilise un PC particulier est en pause pendant trois jours et ne se connecte pas à son PC pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="ffaca-109">For example, an employee that uses a particular PC is on break for three days and does not log on to their PC during that time.</span></span>

<span data-ttu-id="ffaca-110">Lorsque l’utilisateur revient au travail et se connecte à son PC, Antivirus Microsoft Defender vérifie et télécharge immédiatement les dernières mises à jour de la protection et exécute une analyse.</span><span class="sxs-lookup"><span data-stu-id="ffaca-110">When the user returns to work and logs on to their PC, Microsoft Defender Antivirus will immediately check and download the latest protection updates, and run a scan.</span></span>

## <a name="set-up-catch-up-protection-updates-for-endpoints-that-havent-updated-for-a-while"></a><span data-ttu-id="ffaca-111">Configurer des mises à jour de protection de rattrapage pour les points de terminaison qui n’ont pas été mis à jour pendant un certain temps</span><span class="sxs-lookup"><span data-stu-id="ffaca-111">Set up catch-up protection updates for endpoints that haven't updated for a while</span></span>

<span data-ttu-id="ffaca-112">Si Antivirus Microsoft Defender n’a pas téléchargé les mises à jour de protection pendant une période spécifiée, vous pouvez la configurer pour vérifier et télécharger automatiquement la dernière mise à jour lors de la prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="ffaca-112">If Microsoft Defender Antivirus did not download protection updates for a specified period, you can set it up to automatically check and download the latest update at the next log on.</span></span> <span data-ttu-id="ffaca-113">Cela est utile si vous avez désactivé globalement les téléchargements de mises à jour [automatiques au démarrage.](manage-event-based-updates-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="ffaca-113">This is useful if you have [globally disabled automatic update downloads on startup](manage-event-based-updates-microsoft-defender-antivirus.md).</span></span>

### <a name="use-configuration-manager-to-configure-catch-up-protection-updates"></a><span data-ttu-id="ffaca-114">Utiliser Configuration Manager pour configurer des mises à jour de protection de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-114">Use Configuration Manager to configure catch-up protection updates</span></span>

1.  <span data-ttu-id="ffaca-115">Sur votre console Microsoft Endpoint Manager, ouvrez la stratégie anti-programme malveillant à modifier (cliquez sur Ressources et conformité dans le volet de navigation à gauche, puis développez l’arborescence Vue d’ensemble Endpoint Protection **Stratégies**  >    >  **anti-programme** malveillant)</span><span class="sxs-lookup"><span data-stu-id="ffaca-115">On your Microsoft Endpoint Manager console, open the antimalware policy you want to change (click **Assets and Compliance** in the navigation pane on the left, then expand the tree to **Overview** > **Endpoint Protection** > **Antimalware Policies**)</span></span>

2.  <span data-ttu-id="ffaca-116">Go to the **Security intelligence updates** section and configure the following settings:</span><span class="sxs-lookup"><span data-stu-id="ffaca-116">Go to the **Security intelligence updates** section and configure the following settings:</span></span>

    1. <span data-ttu-id="ffaca-117">Définir forcer une mise à jour de l’intelligence de la sécurité si l’ordinateur client est hors connexion pendant plus de deux mises à jour **programmées consécutives** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-117">Set **Force a security intelligence update if the client computer is offline for more than two consecutive scheduled updates** to **Yes**.</span></span>
    2. <span data-ttu-id="ffaca-118">Pour le paramètre If Configuration Manager est utilisé comme source pour les mises à jour d’informations de  **sécurité...**, spécifiez les heures avant lesquelles les mises à jour de protection livrées par Configuration Manager doivent être considérées comme étant hors date.</span><span class="sxs-lookup"><span data-stu-id="ffaca-118">For the  **If Configuration Manager is used as a source for security intelligence updates...**, specify the hours before which the protection updates delivered by Configuration Manager should be considered out-of-date.</span></span> <span data-ttu-id="ffaca-119">Cela entraîne l’utilisation de l’emplacement de mise à jour suivant, en fonction de l’ordre [de source de base défini.](manage-protection-updates-microsoft-defender-antivirus.md#fallback-order)</span><span class="sxs-lookup"><span data-stu-id="ffaca-119">This will cause the next update location to be used, based on the defined [fallback source order](manage-protection-updates-microsoft-defender-antivirus.md#fallback-order).</span></span>

3. <span data-ttu-id="ffaca-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-120">Click **OK**.</span></span>

4.  <span data-ttu-id="ffaca-121">[Déployez la stratégie mise à jour comme d’habitude.](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers)</span><span class="sxs-lookup"><span data-stu-id="ffaca-121">[Deploy the updated policy as usual](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers).</span></span>

### <a name="use-group-policy-to-enable-and-configure-the-catch-up-update-feature"></a><span data-ttu-id="ffaca-122">Utiliser la stratégie de groupe pour activer et configurer la fonctionnalité de mise à jour de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-122">Use Group Policy to enable and configure the catch-up update feature</span></span>

1. <span data-ttu-id="ffaca-123">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-123">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="ffaca-124">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-124">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="ffaca-125">Cliquez **sur Stratégies** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-125">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="ffaca-126">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > mises à jour des signatures.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-126">Expand the tree to **Windows components > Microsoft Defender Antivirus > Signature Updates**.</span></span>

5. <span data-ttu-id="ffaca-127">Double-cliquez sur **le** paramètre Définir le nombre de jours après lequel une mise à jour de l’intelligence de sécurité de rattrapage est requise et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-127">Double-click the **Define the number of days after which a catch-up security intelligence update is required** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="ffaca-128">Entrez le nombre de jours après lesquels vous souhaitez que Microsoft Defender AV vérifie et télécharge la dernière mise à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="ffaca-128">Enter the number of days after which you want Microsoft Defender AV to check for and download the latest protection update.</span></span>

6. <span data-ttu-id="ffaca-129">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-129">Click **OK**.</span></span>

### <a name="use-powershell-cmdlets-to-configure-catch-up-protection-updates"></a><span data-ttu-id="ffaca-130">Utiliser les cmdlets PowerShell pour configurer les mises à jour de la protection de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-130">Use PowerShell cmdlets to configure catch-up protection updates</span></span>

<span data-ttu-id="ffaca-131">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-131">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -SignatureUpdateCatchupInterval
```

<span data-ttu-id="ffaca-132">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="ffaca-132">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md)  and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-configure-catch-up-protection-updates"></a><span data-ttu-id="ffaca-133">Utiliser Windows Management Instruction (WMI) pour configurer des mises à jour de protection de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-133">Use Windows Management Instruction (WMI) to configure catch-up protection updates</span></span>

<span data-ttu-id="ffaca-134">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-134">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
SignatureUpdateCatchupInterval
```

<span data-ttu-id="ffaca-135">Pour plus d’informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-135">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="ffaca-136">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="ffaca-136">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


## <a name="set-the-number-of-days-before-protection-is-reported-as-out-of-date"></a><span data-ttu-id="ffaca-137">Définir le nombre de jours avant que la protection ne soit signalée comme non à jour</span><span class="sxs-lookup"><span data-stu-id="ffaca-137">Set the number of days before protection is reported as out-of-date</span></span>

<span data-ttu-id="ffaca-138">Vous pouvez également spécifier le nombre de jours après lesquels la protection Antivirus Microsoft Defender est considérée comme ancienne ou non à jour.</span><span class="sxs-lookup"><span data-stu-id="ffaca-138">You can also specify the number of days after which Microsoft Defender Antivirus protection is considered old or out-of-date.</span></span> <span data-ttu-id="ffaca-139">Après le nombre de jours spécifié, le client se signale comme étant à jour et affiche une erreur à l’utilisateur du PC.</span><span class="sxs-lookup"><span data-stu-id="ffaca-139">After the specified number of days, the client will report itself as out-of-date, and show an error to the user of the PC.</span></span> <span data-ttu-id="ffaca-140">Cela peut également entraîner une tentative de Antivirus Microsoft Defender de télécharger une mise à jour à partir d’autres sources (en fonction de l’ordre de [source](manage-protection-updates-microsoft-defender-antivirus.md#fallback-order)de base défini), par exemple lors de l’utilisation de MMPC comme source secondaire après avoir défini WSUS ou Microsoft Update comme première source.</span><span class="sxs-lookup"><span data-stu-id="ffaca-140">It may also cause Microsoft Defender Antivirus to attempt to download an update from other sources (based on the defined [fallback source order](manage-protection-updates-microsoft-defender-antivirus.md#fallback-order)), such as when using MMPC as a secondary source after setting WSUS or Microsoft Update as the first source.</span></span>

### <a name="use-group-policy-to-specify-the-number-of-days-before-protection-is-considered-out-of-date"></a><span data-ttu-id="ffaca-141">Utiliser une stratégie de groupe pour spécifier le nombre de jours avant que la protection ne soit considérée comme non à jour</span><span class="sxs-lookup"><span data-stu-id="ffaca-141">Use Group Policy to specify the number of days before protection is considered out-of-date</span></span>

1.  <span data-ttu-id="ffaca-142">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-142">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="ffaca-143">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-143">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="ffaca-144">Cliquez **sur Stratégies** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-144">Click **Policies** then **Administrative templates**.</span></span>

5.  <span data-ttu-id="ffaca-145">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > mises** à jour des signatures et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffaca-145">Expand the tree to **Windows components > Microsoft Defender Antivirus > Signature Updates** and configure the following settings:</span></span>

    1.  <span data-ttu-id="ffaca-146">Double-cliquez sur Définir le nombre de jours avant que les définitions de **logiciels espions** ne soient considérées comme étant à jour et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-146">Double-click **Define the number of days before spyware definitions are considered out of date** and set the option to **Enabled**.</span></span> <span data-ttu-id="ffaca-147">Entrez le nombre de jours après lesquels vous souhaitez que Microsoft Defender AV considère les logiciels espions comme étant à jour.</span><span class="sxs-lookup"><span data-stu-id="ffaca-147">Enter the number of days after which you want Microsoft Defender AV to consider spyware Security intelligence to be out-of-date.</span></span>

    2. <span data-ttu-id="ffaca-148">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-148">Click **OK**.</span></span>

    3.  <span data-ttu-id="ffaca-149">Double-cliquez sur Définir le nombre de jours avant que les **définitions de virus** ne soient considérées comme étant à jour et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-149">Double-click **Define the number of days before virus definitions are considered out of date** and set the option to **Enabled**.</span></span> <span data-ttu-id="ffaca-150">Entrez le nombre de jours après lesquels vous souhaitez que l’Antivirus Microsoft Defender considère l’intelligence de sécurité antivirus comme étant à jour.</span><span class="sxs-lookup"><span data-stu-id="ffaca-150">Enter the number of days after which you want Microsoft Defender AV to consider virus Security intelligence to be out-of-date.</span></span>

    4. <span data-ttu-id="ffaca-151">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-151">Click **OK**.</span></span>


## <a name="set-up-catch-up-scans-for-endpoints-that-have-not-been-scanned-for-a-while"></a><span data-ttu-id="ffaca-152">Configurer des analyses de rattrapage pour les points de terminaison qui n’ont pas été analysés pendant un certain temps</span><span class="sxs-lookup"><span data-stu-id="ffaca-152">Set up catch-up scans for endpoints that have not been scanned for a while</span></span>

<span data-ttu-id="ffaca-153">Vous pouvez définir le nombre d’analyses programmées consécutives qui peuvent être manquées avant Antivirus Microsoft Defender forcer une analyse.</span><span class="sxs-lookup"><span data-stu-id="ffaca-153">You can set the number of consecutive scheduled scans that can be missed before Microsoft Defender Antivirus will force a scan.</span></span>

<span data-ttu-id="ffaca-154">Le processus d’activation de cette fonctionnalité est :</span><span class="sxs-lookup"><span data-stu-id="ffaca-154">The process for enabling this feature is:</span></span>

1. <span data-ttu-id="ffaca-155">Configurer au moins une analyse programmée (voir la rubrique Planifier [les analyses).](scheduled-catch-up-scans-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="ffaca-155">Set up at least one scheduled scan (see the [Schedule scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md) topic).</span></span>
2. <span data-ttu-id="ffaca-156">Activez la fonctionnalité d’analyse de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="ffaca-156">Enable the catch-up scan feature.</span></span>
3. <span data-ttu-id="ffaca-157">Définissez le nombre d’analyses qui peuvent être ignorées avant qu’une analyse de rattrapage ne se produise.</span><span class="sxs-lookup"><span data-stu-id="ffaca-157">Define the number of scans that can be skipped before a catch-up scan occurs.</span></span>

<span data-ttu-id="ffaca-158">Cette fonctionnalité peut être activée pour les analyses complètes et rapides.</span><span class="sxs-lookup"><span data-stu-id="ffaca-158">This feature can be enabled for both full and quick scans.</span></span>

### <a name="use-group-policy-to-enable-and-configure-the-catch-up-scan-feature"></a><span data-ttu-id="ffaca-159">Utiliser la stratégie de groupe pour activer et configurer la fonctionnalité d’analyse de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-159">Use Group Policy to enable and configure the catch-up scan feature</span></span>

1.  <span data-ttu-id="ffaca-160">Assurez-vous d’avoir installé au moins une analyse programmée.</span><span class="sxs-lookup"><span data-stu-id="ffaca-160">Ensure you have set up at least one scheduled scan.</span></span>

2.  <span data-ttu-id="ffaca-161">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-161">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="ffaca-162">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-162">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="ffaca-163">Cliquez **sur Stratégies** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-163">Click **Policies** then **Administrative templates**.</span></span>

5.  <span data-ttu-id="ffaca-164">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > scan et** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffaca-164">Expand the tree to **Windows components > Microsoft Defender Antivirus > Scan** and configure the following settings:</span></span>

    1.  <span data-ttu-id="ffaca-165">Si vous avez installé des analyses rapides programmées, **double-cliquez** sur le paramètre Activer l’analyse rapide de rattrapage et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-165">If you have set up scheduled quick scans, double-click the **Turn on catch-up quick scan** setting and set the option to **Enabled**.</span></span> 
    2. <span data-ttu-id="ffaca-166">Si vous avez installé des analyses complètes  programmées, double-cliquez sur le paramètre Activer l’analyse complète de rattrapage et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-166">If you have set up scheduled full scans, double-click the **Turn on catch-up full scan** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="ffaca-167">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-167">Click **OK**.</span></span>
    3. <span data-ttu-id="ffaca-168">Double-cliquez sur **Définir le nombre** de jours après lequel une analyse de rattrapage est forcée et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="ffaca-168">Double-click the **Define the number of days after which a catch-up scan is forced** setting and set the option to **Enabled**.</span></span> 
    4. <span data-ttu-id="ffaca-169">Entrez le nombre d’analyses qui peuvent être manquées avant qu’une analyse soit automatiquement exécuté lorsque l’utilisateur se connecte ensuite au PC.</span><span class="sxs-lookup"><span data-stu-id="ffaca-169">Enter the number of scans that can be missed before a scan will be automatically run when the user next logs on to the PC.</span></span> <span data-ttu-id="ffaca-170">Le type d’analyse qui est exécuté est déterminé par la spécification du **type** d’analyse à utiliser pour une analyse programmée (voir la rubrique Planification [des analyses).](scheduled-catch-up-scans-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="ffaca-170">The type of scan that is run is determined by the **Specify the scan type to use for a scheduled scan** (see the [Schedule scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md) topic).</span></span> <span data-ttu-id="ffaca-171">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-171">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="ffaca-172">Le titre du paramètre de stratégie de groupe fait référence au nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="ffaca-172">The Group Policy setting title refers to the number of days.</span></span> <span data-ttu-id="ffaca-173">Le paramètre, toutefois, est appliqué au nombre d’analyses (et non de jours) avant l’application de l’analyse de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="ffaca-173">The setting, however, is applied to the number of scans (not days) before the catch-up scan will be run.</span></span>

### <a name="use-powershell-cmdlets-to-configure-catch-up-scans"></a><span data-ttu-id="ffaca-174">Utiliser les cmdlets PowerShell pour configurer des analyses de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-174">Use PowerShell cmdlets to configure catch-up scans</span></span>

<span data-ttu-id="ffaca-175">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-175">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -DisableCatchupFullScan
Set-MpPreference -DisableCatchupQuickScan

```

<span data-ttu-id="ffaca-176">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, consultez les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour gérer les [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="ffaca-176">See [Use PowerShell cmdlets to manage Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md)  and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-configure-catch-up-scans"></a><span data-ttu-id="ffaca-177">Utiliser Windows Management Instruction (WMI) pour configurer des analyses de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-177">Use Windows Management Instruction (WMI) to configure catch-up scans</span></span>

<span data-ttu-id="ffaca-178">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-178">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
DisableCatchupFullScan
DisableCatchupQuickScan
```

<span data-ttu-id="ffaca-179">Pour plus d’informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffaca-179">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="ffaca-180">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="ffaca-180">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


### <a name="use-configuration-manager-to-configure-catch-up-scans"></a><span data-ttu-id="ffaca-181">Utiliser Configuration Manager pour configurer des analyses de rattrapage</span><span class="sxs-lookup"><span data-stu-id="ffaca-181">Use Configuration Manager to configure catch-up scans</span></span>

1.  <span data-ttu-id="ffaca-182">Sur votre console Microsoft Endpoint Manager, ouvrez la stratégie anti-programme malveillant à modifier (cliquez sur Ressources et conformité dans le volet de navigation à gauche, puis développez l’arborescence Vue d’ensemble Endpoint Protection **Stratégies**  >    >  **anti-programme** malveillant)</span><span class="sxs-lookup"><span data-stu-id="ffaca-182">On your Microsoft Endpoint Manager console, open the antimalware policy you want to change (click **Assets and Compliance** in the navigation pane on the left, then expand the tree to **Overview** > **Endpoint Protection** > **Antimalware Policies**)</span></span>

2.  <span data-ttu-id="ffaca-183">Go to the **Scheduled scans** section and **Force a scan of the selected scan type if client computer is offline...** to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-183">Go to the **Scheduled scans** section and **Force a scan of the selected scan type if client computer is offline...** to **Yes**.</span></span> 

3. <span data-ttu-id="ffaca-184">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaca-184">Click **OK**.</span></span>

4.  <span data-ttu-id="ffaca-185">[Déployez la stratégie mise à jour comme d’habitude.](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers)</span><span class="sxs-lookup"><span data-stu-id="ffaca-185">[Deploy the updated policy as usual](/sccm/protect/deploy-use/endpoint-antimalware-policies#deploy-an-antimalware-policy-to-client-computers).</span></span>

## <a name="related-articles"></a><span data-ttu-id="ffaca-186">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ffaca-186">Related articles</span></span>

- [<span data-ttu-id="ffaca-187">Déployer Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="ffaca-187">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ffaca-188">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="ffaca-188">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ffaca-189">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="ffaca-189">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ffaca-190">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="ffaca-190">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ffaca-191">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="ffaca-191">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ffaca-192">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="ffaca-192">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)