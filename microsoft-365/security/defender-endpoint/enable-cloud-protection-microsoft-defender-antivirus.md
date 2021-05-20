---
title: Activez la protection fournie par le cloud dans Antivirus Microsoft Defender
description: Activez la protection fournie par le cloud pour bénéficier de fonctionnalités de protection rapides et avancées.
keywords: Antivirus Microsoft Defender, antimalware, sécurité, cloud, bloc à première vue
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.date: 05/18/2021
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 8c45fb4b60e3c20c2001cc0008ecc8154e854273
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572056"
---
# <a name="turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-104">Activer la protection par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-104">Turn on cloud-delivered protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="52927-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="52927-105">**Applies to:**</span></span>

- [<span data-ttu-id="52927-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="52927-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!NOTE]
> <span data-ttu-id="52927-107">Le service Antivirus Microsoft Defender cloud est un mécanisme permettant d’offrir une protection mise à jour à votre réseau et à vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="52927-107">The Microsoft Defender Antivirus cloud service is a mechanism for delivering updated protection to your network and endpoints.</span></span> <span data-ttu-id="52927-108">Bien qu’il soit appelé un service cloud, il n’est pas simplement une protection pour les fichiers stockés dans le cloud; il utilise plutôt des ressources distribuées et l’apprentissage automatique pour fournir une protection à vos points de terminaison à un rythme beaucoup plus rapide que les mises à jour traditionnelles du renseignement de sécurité.</span><span class="sxs-lookup"><span data-stu-id="52927-108">Although it is called a cloud service, it is not simply protection for files stored in the cloud; rather, it uses distributed resources and machine learning to deliver protection to your endpoints at a rate that is far faster than traditional Security intelligence updates.</span></span>

<span data-ttu-id="52927-109">Antivirus Microsoft Defender utilise de multiples technologies de détection et de prévention pour offrir une protection précise, en temps réel et intelligente.</span><span class="sxs-lookup"><span data-stu-id="52927-109">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, real-time, and intelligent protection.</span></span> <span data-ttu-id="52927-110">[Faites la point de vue des technologies de pointe au cœur de Microsoft Defender pour la protection de prochaine génération Endpoint.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="52927-110">[Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>

<span data-ttu-id="52927-111">Vous pouvez activer Antivirus Microsoft Defender protection fournie par le cloud de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="52927-111">You can turn Microsoft Defender Antivirus cloud-delivered protection on or off in several ways:</span></span>

- <span data-ttu-id="52927-112">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="52927-112">Microsoft Intune</span></span>
- <span data-ttu-id="52927-113">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="52927-113">Microsoft Endpoint Manager</span></span>
- <span data-ttu-id="52927-114">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="52927-114">Group Policy</span></span>
- <span data-ttu-id="52927-115">Cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52927-115">PowerShell cmdlets.</span></span>

 <span data-ttu-id="52927-116">Vous pouvez également l’activer ou l’éteindre chez des clients individuels avec l’application Sécurité Windows’application.</span><span class="sxs-lookup"><span data-stu-id="52927-116">You can also turn it on or off in individual clients with the Windows Security app.</span></span>

<span data-ttu-id="52927-117">Consultez [la protection microsoft fournie par le cloud](cloud-protection-microsoft-defender-antivirus.md) pour une vue d’ensemble Antivirus Microsoft Defender protection fournie par le cloud.</span><span class="sxs-lookup"><span data-stu-id="52927-117">See [Use Microsoft cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) for an overview of Microsoft Defender Antivirus cloud-delivered protection.</span></span>

<span data-ttu-id="52927-118">Pour plus d’informations sur les exigences spécifiques de connectivité réseau pour vous assurer que vos points de terminaison peuvent se connecter au service de protection livré dans le cloud, [consultez Configurer et valider les connexions réseau.](configure-network-connections-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="52927-118">For more information about the specific network-connectivity requirements to ensure your endpoints can connect to the cloud-delivered protection service, see [Configure and validate network connections](configure-network-connections-microsoft-defender-antivirus.md).</span></span>

> [!NOTE]
> <span data-ttu-id="52927-119">En Windows 10, il n’y a pas de différence entre les options **de** rapports **de** base et avancées décrites dans ce sujet.</span><span class="sxs-lookup"><span data-stu-id="52927-119">In Windows 10, there is no difference between the **Basic** and **Advanced** reporting options described in this topic.</span></span> <span data-ttu-id="52927-120">Il s’agit d’une distinction héritée et le choix de l’un ou l’autre paramètre se traduira par le même niveau de protection fournie par le cloud.</span><span class="sxs-lookup"><span data-stu-id="52927-120">This is a legacy distinction and choosing either setting will result in the same level of cloud-delivered protection.</span></span> <span data-ttu-id="52927-121">Il n’y a aucune différence dans le type ou la quantité d’informations qui sont partagées.</span><span class="sxs-lookup"><span data-stu-id="52927-121">There is no difference in the type or amount of information that is shared.</span></span> <span data-ttu-id="52927-122">Pour plus d’informations sur ce que nous recueillons, consultez la [déclaration de confidentialité de Microsoft](https://go.microsoft.com/fwlink/?linkid=521839).</span><span class="sxs-lookup"><span data-stu-id="52927-122">For more information on what we collect, see the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=521839).</span></span>

## <a name="use-intune-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-123">Utilisez Intune pour activer la protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-123">Use Intune to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="52927-124">Allez au centre Microsoft Endpoint Manager admin [https://endpoint.microsoft.com](https://endpoint.microsoft.com) () et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="52927-124">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="52927-125">Sur le **volet Accueil,** sélectionnez la **configuration de l'> profils**.</span><span class="sxs-lookup"><span data-stu-id="52927-125">On the **Home** pane, select **Device configuration > Profiles**.</span></span>

3. <span data-ttu-id="52927-126">Sélectionnez le type **de profil** de restriction s’appliquant à l’appareil que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="52927-126">Select the **Device restrictions** profile type you want to configure.</span></span> <span data-ttu-id="52927-127">Si vous avez besoin de créer un nouveau type **de profil de restriction** s’appliquant aux périphériques, consultez les paramètres de restriction de [l’appareil Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="52927-127">If you need to create a new **Device restrictions** profile type, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="52927-128">Sélectionnez **Paramètres**  >  **de configuration propriétés :**  >  **Modifiez Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="52927-128">Select **Properties** > **Configuration settings: Edit** > **Microsoft Defender Antivirus**.</span></span>

5. <span data-ttu-id="52927-129">Sur le **commutateur de protection livré par Cloud,** sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="52927-129">On the **Cloud-delivered protection** switch, select **Enable**.</span></span>

6. <span data-ttu-id="52927-130">Dans les utilisateurs **prompts avant la baisse de soumission** de l’échantillon, **sélectionnez Envoyer toutes les données automatiquement**.</span><span class="sxs-lookup"><span data-stu-id="52927-130">In the **Prompt users before sample submission** dropdown, select **Send all data automatically**.</span></span>

<span data-ttu-id="52927-131">Pour plus d’informations sur les profils des périphériques Intune, y compris la façon de créer et de configurer leurs paramètres, voir [Quels sont les profils Microsoft Intune’appareils ?](/intune/device-profiles)</span><span class="sxs-lookup"><span data-stu-id="52927-131">For more information about Intune device profiles, including how to create and configure their settings, see [What are Microsoft Intune device profiles?](/intune/device-profiles)</span></span>

## <a name="use-microsoft-endpoint-manager-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-132">Utilisez Microsoft Endpoint Manager pour activer la protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-132">Use Microsoft Endpoint Manager to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="52927-133">Allez au centre Microsoft Endpoint Manager admin [https://endpoint.microsoft.com](https://endpoint.microsoft.com) () et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="52927-133">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="52927-134">Choisissez **Endpoint security**  >  **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="52927-134">Choose **Endpoint security** > **Antivirus**.</span></span>

3. <span data-ttu-id="52927-135">Sélectionnez un profil antivirus.</span><span class="sxs-lookup"><span data-stu-id="52927-135">Select an antivirus profile.</span></span> <span data-ttu-id="52927-136">(Si vous n’en avez pas encore, ou si vous souhaitez créer un nouveau profil, consultez les paramètres [de restriction de l’appareil Configure dans Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="52927-136">(If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="52927-137">Sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="52927-137">Select **Properties**.</span></span> <span data-ttu-id="52927-138">Ensuite, à côté des **paramètres de configuration,** choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="52927-138">Then, next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="52927-139">Élargissez **la protection** cloud, puis dans la liste de **niveau de protection fournie par cloud,** sélectionnez l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="52927-139">Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:</span></span>
   - <span data-ttu-id="52927-140">**Haut**: Applique un fort niveau de détection.</span><span class="sxs-lookup"><span data-stu-id="52927-140">**High**: Applies a strong level of detection.</span></span>
   - <span data-ttu-id="52927-141">**High plus :** Utilise le niveau élevé **et** applique des mesures de protection supplémentaires (peuvent avoir une incidence sur les performances des clients).</span><span class="sxs-lookup"><span data-stu-id="52927-141">**High plus**: Uses the **High** level and applies additional protection measures (may impact client performance).</span></span>
   - <span data-ttu-id="52927-142">**Tolérance zéro**: Bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="52927-142">**Zero tolerance**: Blocks all unknown executables.</span></span>

6. <span data-ttu-id="52927-143">Sélectionnez **Examen + enregistrer**, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="52927-143">Select **Review + save**, then choose **Save**.</span></span>

<span data-ttu-id="52927-144">Pour plus d’informations sur la configuration Microsoft Endpoint Configuration Manager, voir [Comment créer et déployer des stratégies antimalware : service de protection cloud](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service).</span><span class="sxs-lookup"><span data-stu-id="52927-144">For more information about configuring Microsoft Endpoint Configuration Manager, see [How to create and deploy antimalware policies: Cloud-protection service](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service).</span></span>

## <a name="use-group-policy-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-145">Utilisez la stratégie de groupe pour activer la protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-145">Use Group Policy to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="52927-146">Sur votre appareil de gestion de stratégie de groupe, ouvrez [la console de gestion de stratégie de](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))groupe, cliquez à droite sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionner **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="52927-146">On your Group Policy management device, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="52927-147">Dans le **Group Policy Management Editor**, aller à la configuration **informatique**.</span><span class="sxs-lookup"><span data-stu-id="52927-147">In the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

3. <span data-ttu-id="52927-148">Sélectionnez **Modèles administratifs**.</span><span class="sxs-lookup"><span data-stu-id="52927-148">Select **Administrative templates**.</span></span>

4. <span data-ttu-id="52927-149">Étendre l’arbre **aux Windows composants > Antivirus Microsoft Defender > MAPS**</span><span class="sxs-lookup"><span data-stu-id="52927-149">Expand the tree to **Windows components > Microsoft Defender Antivirus > MAPS**</span></span>

5. <span data-ttu-id="52927-150">Double-cliquez **sur Rejoindre Microsoft MAPS**.</span><span class="sxs-lookup"><span data-stu-id="52927-150">Double-click **Join Microsoft MAPS**.</span></span> <span data-ttu-id="52927-151">Assurez-vous que l’option est activée et réglée **sur maps de base** ou cartes **avancées.**</span><span class="sxs-lookup"><span data-stu-id="52927-151">Ensure the option is turned on and set to **Basic MAPS** or **Advanced MAPS**.</span></span> <span data-ttu-id="52927-152">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="52927-152">Select **OK**.</span></span>

6. <span data-ttu-id="52927-153">Double-cliquez envoyer **des échantillons de fichiers lorsque d’autres analyses sont nécessaires**.</span><span class="sxs-lookup"><span data-stu-id="52927-153">Double-click **Send file samples when further analysis is required**.</span></span> <span data-ttu-id="52927-154">Assurez-vous que la première option est définie sur **Activé et** que les autres options sont définies sur l’une ou l’autre :</span><span class="sxs-lookup"><span data-stu-id="52927-154">Ensure that the first option is set to **Enabled** and that the other options are set to either:</span></span>

    1. <span data-ttu-id="52927-155">**Envoyer des échantillons sûrs** (1)</span><span class="sxs-lookup"><span data-stu-id="52927-155">**Send safe samples** (1)</span></span>
    2. <span data-ttu-id="52927-156">**Envoyer tous les échantillons** (3)</span><span class="sxs-lookup"><span data-stu-id="52927-156">**Send all samples** (3)</span></span>

        >[!NOTE]
        > <span data-ttu-id="52927-157">**L’option Envoyer des échantillons** sûrs (1) signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="52927-157">The **Send safe samples** (1) option means that most samples will be sent automatically.</span></span> <span data-ttu-id="52927-158">Les fichiers susceptibles de contenir des renseignements personnels seront toujours rapides et nécessiteront une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="52927-158">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>
        > <span data-ttu-id="52927-159">Définir l’option de **Toujours prompt** (0) abaissera l’état de protection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52927-159">Setting the option to **Always Prompt** (0) will lower the protection state of the device.</span></span> <span data-ttu-id="52927-160">Le définir pour **ne jamais envoyer** (2) signifie que la fonction Block at First [Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) de Microsoft Defender pour Endpoint ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="52927-160">Setting it to **Never send** (2) means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

7. <span data-ttu-id="52927-161">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="52927-161">Select **OK**.</span></span>

## <a name="use-powershell-cmdlets-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-162">Utilisez des cmdlets PowerShell pour activer la protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-162">Use PowerShell cmdlets to turn on cloud-delivered protection</span></span>

<span data-ttu-id="52927-163">Les cmdlets suivants peuvent activer la protection fournie par le cloud :</span><span class="sxs-lookup"><span data-stu-id="52927-163">The following cmdlets can turn on cloud-delivered protection:</span></span>

```PowerShell
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendAllSamples
```

<span data-ttu-id="52927-164">Pour plus d’informations sur la façon d’utiliser PowerShell avec Antivirus Microsoft Defender, [consultez les cmdlets PowerShell pour configurer et exécuter Antivirus Microsoft Defender](use-powershell-cmdlets-microsoft-defender-antivirus.md) [cmdlets Defender](/powershell/module/defender/).</span><span class="sxs-lookup"><span data-stu-id="52927-164">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span> <span data-ttu-id="52927-165">[Politique CSP - Defender a](/windows/client-management/mdm/policy-csp-defender) également plus d’informations spécifiquement sur [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span><span class="sxs-lookup"><span data-stu-id="52927-165">[Policy CSP - Defender](/windows/client-management/mdm/policy-csp-defender) also has more information specifically on [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span></span>

>[!NOTE]
> <span data-ttu-id="52927-166">Vous pouvez également définir **-SubmitSamplesConsent à** `SendSafeSamples` (le paramètre par défaut), `NeverSend` ou `AlwaysPrompt` .</span><span class="sxs-lookup"><span data-stu-id="52927-166">You can also set **-SubmitSamplesConsent** to `SendSafeSamples` (the default setting), `NeverSend`, or `AlwaysPrompt`.</span></span> <span data-ttu-id="52927-167">Le `SendSafeSamples` paramètre signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="52927-167">The `SendSafeSamples` setting means that most samples will be sent automatically.</span></span> <span data-ttu-id="52927-168">Les fichiers susceptibles de contenir des renseignements personnels seront toujours rapides et nécessiteront une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="52927-168">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>

>[!WARNING]
> <span data-ttu-id="52927-169">Réglage **-SubmitSamplesConsent ou** `NeverSend` `AlwaysPrompt` abaissera le niveau de protection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52927-169">Setting **-SubmitSamplesConsent** to `NeverSend` or `AlwaysPrompt` will lower the protection level of the device.</span></span> <span data-ttu-id="52927-170">En outre, le définir signifie `NeverSend` que la fonction Block at First [Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) de Microsoft Defender pour Endpoint ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="52927-170">In addition, setting it to `NeverSend` means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

## <a name="use-windows-management-instruction-wmi-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="52927-171">Utilisez Windows instruction de gestion des systèmes (WMI) pour activer la protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="52927-171">Use Windows Management Instruction (WMI) to turn on cloud-delivered protection</span></span>

<span data-ttu-id="52927-172">Utilisez la [ **méthode** Set de la **MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) classe pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="52927-172">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) class for the following properties:</span></span>

```WMI
MAPSReporting
SubmitSamplesConsent
```

<span data-ttu-id="52927-173">Pour plus d’informations sur les paramètres autorisés, [Windows Defender les API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="52927-173">For more information about allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="turn-on-cloud-delivered-protection-on-individual-clients-with-the-windows-security-app"></a><span data-ttu-id="52927-174">Activez la protection fournie par le cloud sur les clients individuels avec l’application Sécurité Windows cloud</span><span class="sxs-lookup"><span data-stu-id="52927-174">Turn on cloud-delivered protection on individual clients with the Windows Security app</span></span>

> [!NOTE]
> <span data-ttu-id="52927-175">Si le **paramètre local Configure remplace le paramètre de stratégie de groupe Microsoft MAPS** est défini sur **Désactivé,** le **paramètre de protection basé sur le Cloud** en Windows Paramètres sera grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="52927-175">If the **Configure local setting override for reporting Microsoft MAPS** Group Policy setting is set to **Disabled**, then the **Cloud-based protection** setting in Windows Settings will be greyed-out and unavailable.</span></span> <span data-ttu-id="52927-176">Les modifications apportées via un objet de stratégie de groupe doivent d’abord être déployées vers les points de terminaison individuels avant que le paramètre soit mis à jour dans les Paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="52927-176">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

1. <span data-ttu-id="52927-177">Ouvrez l Sécurité Windows appe en sélectionnant l’icône bouclier dans la barre des tâches, ou en recherchant le menu de démarrage pour **Defender**.</span><span class="sxs-lookup"><span data-stu-id="52927-177">Open the Windows Security app by selecting the shield icon in the task bar, or by searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="52927-178">Sélectionnez **la vignette de protection contre & virus** (ou l’icône bouclier sur la barre de menu gauche) puis **l’étiquette paramètres de protection contre les menaces virus &** :</span><span class="sxs-lookup"><span data-stu-id="52927-178">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Virus & threat protection settings** label:</span></span>

    ![Capture d’écran de l’étiquette des paramètres de protection contre les virus et les menaces dans l’application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="52927-180">Confirmez que **la protection basée sur le Cloud** et la soumission automatique **de** l’échantillon sont commutées **à On**.</span><span class="sxs-lookup"><span data-stu-id="52927-180">Confirm that **Cloud-based Protection** and **Automatic sample submission** are switched to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="52927-181">Si la soumission automatique de l’échantillon a été configurée avec la stratégie de groupe, le paramètre sera grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="52927-181">If automatic sample submission has been configured with Group Policy then the setting will be greyed-out and unavailable.</span></span>

## <a name="related-articles"></a><span data-ttu-id="52927-182">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="52927-182">Related articles</span></span>

- [<span data-ttu-id="52927-183">Configurer le délai de blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="52927-183">Configure the cloud block timeout period</span></span>](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md)
- [<span data-ttu-id="52927-184">Configurer le bloc à première vue</span><span class="sxs-lookup"><span data-stu-id="52927-184">Configure block at first sight</span></span>](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [<span data-ttu-id="52927-185">Utiliser des cmdlets PowerShell pour gérer l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="52927-185">Use PowerShell cmdlets to manage Microsoft Defender Antivirus</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- <span data-ttu-id="52927-186">[Aider à sécuriser Windows PC avec Endpoint Protection pour Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span><span class="sxs-lookup"><span data-stu-id="52927-186">[Help secure Windows PCs with Endpoint Protection for Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span></span>
- [<span data-ttu-id="52927-187">Cmdlets defender</span><span class="sxs-lookup"><span data-stu-id="52927-187">Defender cmdlets</span></span>](/powershell/module/defender/)
- [<span data-ttu-id="52927-188">Utilisez la protection microsoft cloud livrée dans Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="52927-188">Use Microsoft cloud-delivered protection in Microsoft Defender Antivirus</span></span>](cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="52927-189">Comment créer et déployer des stratégies antimalware : service de protection contre le Cloud</span><span class="sxs-lookup"><span data-stu-id="52927-189">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)
- [<span data-ttu-id="52927-190">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="52927-190">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
