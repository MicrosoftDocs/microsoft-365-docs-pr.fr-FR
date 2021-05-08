---
title: Activer la protection cloud dans Antivirus Microsoft Defender
description: Activer la protection cloud pour bénéficier des fonctionnalités de protection rapide et avancée.
keywords: Antivirus Microsoft Defender logiciel anti-programme malveillant, sécurité, cloud, bloquer à la première vue
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.date: 04/30/2021
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 2b3d22fc50335516e6c50a9dfef9f7835c00a95b
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275263"
---
# <a name="turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-104">Activer la protection par le cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-104">Turn on cloud-delivered protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="cfa44-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cfa44-105">**Applies to:**</span></span>

- [<span data-ttu-id="cfa44-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cfa44-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!NOTE]
> <span data-ttu-id="cfa44-107">Le Antivirus Microsoft Defender cloud est un mécanisme permettant de fournir une protection mise à jour à votre réseau et points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="cfa44-107">The Microsoft Defender Antivirus cloud service is a mechanism for delivering updated protection to your network and endpoints.</span></span> <span data-ttu-id="cfa44-108">Bien qu’il soit appelé service cloud, il ne s’agit pas simplement de la protection des fichiers stockés dans le cloud . Au lieu de cela, il utilise des ressources distribuées et l’apprentissage automatique pour fournir une protection à vos points de terminaison à une vitesse beaucoup plus rapide que les mises à jour d’intelligence de sécurité traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="cfa44-108">Although it is called a cloud service, it is not simply protection for files stored in the cloud; rather, it uses distributed resources and machine learning to deliver protection to your endpoints at a rate that is far faster than traditional Security intelligence updates.</span></span>

<span data-ttu-id="cfa44-109">Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour offrir une protection précise, en temps réel et intelligente.</span><span class="sxs-lookup"><span data-stu-id="cfa44-109">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, real-time, and intelligent protection.</span></span> <span data-ttu-id="cfa44-110">Faire connaître les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point de [terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="cfa44-110">[Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>
<span data-ttu-id="cfa44-111">![Liste des moteurs de Microsoft Defender AV](images/microsoft-defender-atp-next-generation-protection-engines.png)</span><span class="sxs-lookup"><span data-stu-id="cfa44-111">![List of Microsoft Defender AV engines](images/microsoft-defender-atp-next-generation-protection-engines.png)</span></span>  

<span data-ttu-id="cfa44-112">Vous pouvez activer ou désactiver Antivirus Microsoft Defender protection cloud de plusieurs manières :</span><span class="sxs-lookup"><span data-stu-id="cfa44-112">You can turn Microsoft Defender Antivirus cloud-delivered protection on or off in several ways:</span></span>

- <span data-ttu-id="cfa44-113">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="cfa44-113">Microsoft Intune</span></span>
- <span data-ttu-id="cfa44-114">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="cfa44-114">Microsoft Endpoint Manager</span></span>
- <span data-ttu-id="cfa44-115">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cfa44-115">Group Policy</span></span>
- <span data-ttu-id="cfa44-116">Cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cfa44-116">PowerShell cmdlets.</span></span>

 <span data-ttu-id="cfa44-117">Vous pouvez également l’activer ou le désactiver dans des clients individuels à l’Sécurité Windows’application.</span><span class="sxs-lookup"><span data-stu-id="cfa44-117">You can also turn it on or off in individual clients with the Windows Security app.</span></span>

<span data-ttu-id="cfa44-118">Voir [Utiliser la protection microsoft cloud pour](cloud-protection-microsoft-defender-antivirus.md) une vue d’ensemble Antivirus Microsoft Defender protection cloud.</span><span class="sxs-lookup"><span data-stu-id="cfa44-118">See [Use Microsoft cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) for an overview of Microsoft Defender Antivirus cloud-delivered protection.</span></span>

<span data-ttu-id="cfa44-119">Pour plus d’informations sur les exigences spécifiques en matière de connectivité réseau pour vous assurer que vos points de terminaison peuvent se connecter au service de protection assurée par le cloud, voir Configurer et valider les [connexions réseau.](configure-network-connections-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="cfa44-119">For more information about the specific network-connectivity requirements to ensure your endpoints can connect to the cloud-delivered protection service, see [Configure and validate network connections](configure-network-connections-microsoft-defender-antivirus.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cfa44-120">Dans Windows 10, il n’existe aucune  différence  entre les options de rapports de base et avancées décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="cfa44-120">In Windows 10, there is no difference between the **Basic** and **Advanced** reporting options described in this topic.</span></span> <span data-ttu-id="cfa44-121">Il s’agit d’une distinction héritée et le choix de l’un ou l’autre des paramètres entraîne le même niveau de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="cfa44-121">This is a legacy distinction and choosing either setting will result in the same level of cloud-delivered protection.</span></span> <span data-ttu-id="cfa44-122">Il n’existe aucune différence dans le type ou la quantité d’informations partagées.</span><span class="sxs-lookup"><span data-stu-id="cfa44-122">There is no difference in the type or amount of information that is shared.</span></span> <span data-ttu-id="cfa44-123">Pour plus d’informations sur ce que nous collectons, voir la déclaration [de confidentialité de Microsoft.](https://go.microsoft.com/fwlink/?linkid=521839)</span><span class="sxs-lookup"><span data-stu-id="cfa44-123">For more information on what we collect, see the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=521839).</span></span>

## <a name="use-intune-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-124">Utiliser Intune pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-124">Use Intune to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="cfa44-125">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="cfa44-125">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="cfa44-126">Dans le **volet Accueil,** sélectionnez Configuration de l'> **profils.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-126">On the **Home** pane, select **Device configuration > Profiles**.</span></span>

3. <span data-ttu-id="cfa44-127">Sélectionnez le type **de profil restrictions d’appareil** que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="cfa44-127">Select the **Device restrictions** profile type you want to configure.</span></span> <span data-ttu-id="cfa44-128">Si vous devez créer un type de profil de restrictions [d’appareil,](/intune/device-restrictions-configure)voir Configurer les **paramètres** de restriction d’appareil dans Microsoft Intune .</span><span class="sxs-lookup"><span data-stu-id="cfa44-128">If you need to create a new **Device restrictions** profile type, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="cfa44-129">Sélectionnez **les**  >  **paramètres de configuration des propriétés :**  >  **Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="cfa44-129">Select **Properties** > **Configuration settings: Edit** > **Microsoft Defender Antivirus**.</span></span>

5. <span data-ttu-id="cfa44-130">Sur le **commutateur de protection cloud,** sélectionnez **Activer.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-130">On the **Cloud-delivered protection** switch, select **Enable**.</span></span>

6. <span data-ttu-id="cfa44-131">Dans la demande **d’utilisateurs avant la** soumission d’exemples, **sélectionnez Envoyer toutes les données automatiquement.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-131">In the **Prompt users before sample submission** dropdown, select **Send all data automatically**.</span></span>

<span data-ttu-id="cfa44-132">Pour plus d’informations sur les profils d’appareil Intune, notamment sur la création et la configuration de leurs paramètres, voir Quelles sont les [Microsoft Intune’appareil ?](/intune/device-profiles)</span><span class="sxs-lookup"><span data-stu-id="cfa44-132">For more information about Intune device profiles, including how to create and configure their settings, see [What are Microsoft Intune device profiles?](/intune/device-profiles)</span></span>

## <a name="use-microsoft-endpoint-manager-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-133">Utiliser Microsoft Endpoint Manager pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-133">Use Microsoft Endpoint Manager to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="cfa44-134">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="cfa44-134">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="cfa44-135">Choisissez **l’Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-135">Choose **Endpoint security** > **Antivirus**.</span></span>

3. <span data-ttu-id="cfa44-136">Sélectionnez un profil antivirus.</span><span class="sxs-lookup"><span data-stu-id="cfa44-136">Select an antivirus profile.</span></span> <span data-ttu-id="cfa44-137">(Si vous n’en avez pas encore, ou si vous souhaitez créer un profil, voir Configurer les [paramètres](/intune/device-restrictions-configure)de restriction d’appareil dans Microsoft Intune .</span><span class="sxs-lookup"><span data-stu-id="cfa44-137">(If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="cfa44-138">Sélectionnez **les propriétés.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-138">Select **Properties**.</span></span> <span data-ttu-id="cfa44-139">Ensuite, en de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-139">Then, next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="cfa44-140">Développez **la protection** cloud, puis dans la liste des niveaux de **protection** cloud, sélectionnez l’une des listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfa44-140">Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:</span></span>
   - <span data-ttu-id="cfa44-141">**Élevé**: applique un niveau élevé de détection.</span><span class="sxs-lookup"><span data-stu-id="cfa44-141">**High**: Applies a strong level of detection.</span></span>
   - <span data-ttu-id="cfa44-142">**Plus élevé**: utilise le **niveau élevé** et applique des mesures de protection supplémentaires (peut avoir un impact sur les performances du client).</span><span class="sxs-lookup"><span data-stu-id="cfa44-142">**High plus**: Uses the **High** level and applies additional protection measures (may impact client performance).</span></span>
   - <span data-ttu-id="cfa44-143">**Tolérance zéro :** bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="cfa44-143">**Zero tolerance**: Blocks all unknown executables.</span></span>

6. <span data-ttu-id="cfa44-144">Sélectionnez **Révision + Enregistrer,** puis **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-144">Select **Review + save**, then choose **Save**.</span></span>

<span data-ttu-id="cfa44-145">Pour plus d’informations sur la configuration Microsoft Endpoint Configuration Manager, voir Comment créer et déployer des stratégies [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)malveillant : service de protection cloud .</span><span class="sxs-lookup"><span data-stu-id="cfa44-145">For more information about configuring Microsoft Endpoint Configuration Manager, see [How to create and deploy antimalware policies: Cloud-protection service](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service).</span></span>

## <a name="use-group-policy-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-146">Utiliser une stratégie de groupe pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-146">Use Group Policy to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="cfa44-147">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-147">On your Group Policy management device, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="cfa44-148">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration de l’ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-148">In the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

3. <span data-ttu-id="cfa44-149">Sélectionnez **modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-149">Select **Administrative templates**.</span></span>

4. <span data-ttu-id="cfa44-150">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > MAPS**</span><span class="sxs-lookup"><span data-stu-id="cfa44-150">Expand the tree to **Windows components > Microsoft Defender Antivirus > MAPS**</span></span>

5. <span data-ttu-id="cfa44-151">Double-cliquez sur **Rejoindre Microsoft MAPS.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-151">Double-click **Join Microsoft MAPS**.</span></span> <span data-ttu-id="cfa44-152">Assurez-vous que l’option est allumée et définie sur **Maps de base** ou Cartes **avancées.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-152">Ensure the option is turned on and set to **Basic MAPS** or **Advanced MAPS**.</span></span> <span data-ttu-id="cfa44-153">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfa44-153">Select **OK**.</span></span>

6. <span data-ttu-id="cfa44-154">Double-cliquez sur **Envoyer des exemples de fichier lorsque d’autres analyses sont nécessaires.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-154">Double-click **Send file samples when further analysis is required**.</span></span> <span data-ttu-id="cfa44-155">Assurez-vous que la première option est définie sur **Activé** et que les autres options sont définies sur :</span><span class="sxs-lookup"><span data-stu-id="cfa44-155">Ensure that the first option is set to **Enabled** and that the other options are set to either:</span></span>

    1. <span data-ttu-id="cfa44-156">**Envoyer des exemples sécurisés** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa44-156">**Send safe samples** (1)</span></span>
    2. <span data-ttu-id="cfa44-157">**Envoyer tous les exemples** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa44-157">**Send all samples** (3)</span></span>

        >[!NOTE]
        > <span data-ttu-id="cfa44-158">**L’option Envoyer des échantillons sûrs** (1) signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cfa44-158">The **Send safe samples** (1) option means that most samples will be sent automatically.</span></span> <span data-ttu-id="cfa44-159">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="cfa44-159">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>
        > <span data-ttu-id="cfa44-160">La définition de **l’option sur Always Prompt** (0) réduit l’état de protection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cfa44-160">Setting the option to **Always Prompt** (0) will lower the protection state of the device.</span></span> <span data-ttu-id="cfa44-161">Le fait de la définir sur [](configure-block-at-first-sight-microsoft-defender-antivirus.md) **Ne** jamais envoyer (2) signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de terminaison ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="cfa44-161">Setting it to **Never send** (2) means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

7. <span data-ttu-id="cfa44-162">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfa44-162">Select **OK**.</span></span>

## <a name="use-powershell-cmdlets-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-163">Utiliser les cmdlets PowerShell pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-163">Use PowerShell cmdlets to turn on cloud-delivered protection</span></span>

<span data-ttu-id="cfa44-164">Les cmdlets suivantes peuvent activer la protection cloud :</span><span class="sxs-lookup"><span data-stu-id="cfa44-164">The following cmdlets can turn on cloud-delivered protection:</span></span>

```PowerShell
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendAllSamples
```

<span data-ttu-id="cfa44-165">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="cfa44-165">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span> <span data-ttu-id="cfa44-166">[Stratégie CSP - Defender](/windows/client-management/mdm/policy-csp-defender) a également plus d’informations spécifiques sur [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span><span class="sxs-lookup"><span data-stu-id="cfa44-166">[Policy CSP - Defender](/windows/client-management/mdm/policy-csp-defender) also has more information specifically on [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span></span>

>[!NOTE]
> <span data-ttu-id="cfa44-167">Vous pouvez également définir **-SubmitSamplesConsent** sur (paramètre par `SendSafeSamples` défaut), `NeverSend` ou `AlwaysPrompt` .</span><span class="sxs-lookup"><span data-stu-id="cfa44-167">You can also set **-SubmitSamplesConsent** to `SendSafeSamples` (the default setting), `NeverSend`, or `AlwaysPrompt`.</span></span> <span data-ttu-id="cfa44-168">Le `SendSafeSamples` paramètre signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cfa44-168">The `SendSafeSamples` setting means that most samples will be sent automatically.</span></span> <span data-ttu-id="cfa44-169">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="cfa44-169">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>

>[!WARNING]
> <span data-ttu-id="cfa44-170">Setting **-SubmitSamplesConsent** to `NeverSend` or will lower the protection level of the `AlwaysPrompt` device.</span><span class="sxs-lookup"><span data-stu-id="cfa44-170">Setting **-SubmitSamplesConsent** to `NeverSend` or `AlwaysPrompt` will lower the protection level of the device.</span></span> <span data-ttu-id="cfa44-171">En outre, sa définition signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de `NeverSend` terminaison ne fonctionne pas. [](configure-block-at-first-sight-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="cfa44-171">In addition, setting it to `NeverSend` means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

## <a name="use-windows-management-instruction-wmi-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="cfa44-172">Utiliser Windows Management Instruction (WMI) pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-172">Use Windows Management Instruction (WMI) to turn on cloud-delivered protection</span></span>

<span data-ttu-id="cfa44-173">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfa44-173">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) class for the following properties:</span></span>

```WMI
MAPSReporting
SubmitSamplesConsent
```

<span data-ttu-id="cfa44-174">Pour plus d’informations sur les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="cfa44-174">For more information about allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="turn-on-cloud-delivered-protection-on-individual-clients-with-the-windows-security-app"></a><span data-ttu-id="cfa44-175">Activer la protection cloud sur des clients individuels avec l’application Sécurité Windows cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-175">Turn on cloud-delivered protection on individual clients with the Windows Security app</span></span>

> [!NOTE]
> <span data-ttu-id="cfa44-176">Si le paramètre Configurer le remplacement de paramètre local pour la création de rapports sur la stratégie de groupe **Microsoft MAPS** est **désactivé,** le paramètre de protection basée sur le **cloud** dans Windows Paramètres est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="cfa44-176">If the **Configure local setting override for reporting Microsoft MAPS** Group Policy setting is set to **Disabled**, then the **Cloud-based protection** setting in Windows Settings will be greyed-out and unavailable.</span></span> <span data-ttu-id="cfa44-177">Les modifications apportées via un objet de stratégie de groupe doivent d’abord être déployées sur des points de terminaison individuels avant que le paramètre ne soit mis à jour dans Windows Paramètres.</span><span class="sxs-lookup"><span data-stu-id="cfa44-177">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

1. <span data-ttu-id="cfa44-178">Ouvrez l’Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-178">Open the Windows Security app by selecting the shield icon in the task bar, or by searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="cfa44-179">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis l’étiquette **paramètres** de protection contre & virus :</span><span class="sxs-lookup"><span data-stu-id="cfa44-179">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Virus & threat protection settings** label:</span></span>

    ![Capture d’écran de l’étiquette des paramètres de protection contre & virus dans l’application Sécurité Windows virus](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="cfa44-181">Confirmez que **la protection basée sur le cloud et** **l’envoi** automatique d’échantillons sont **activés.**</span><span class="sxs-lookup"><span data-stu-id="cfa44-181">Confirm that **Cloud-based Protection** and **Automatic sample submission** are switched to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="cfa44-182">Si l’envoi automatique d’échantillons a été configuré avec la stratégie de groupe, le paramètre est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="cfa44-182">If automatic sample submission has been configured with Group Policy then the setting will be greyed-out and unavailable.</span></span>

## <a name="related-articles"></a><span data-ttu-id="cfa44-183">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="cfa44-183">Related articles</span></span>

- [<span data-ttu-id="cfa44-184">Configurer le délai de blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-184">Configure the cloud block timeout period</span></span>](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md)
- [<span data-ttu-id="cfa44-185">Configurer bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="cfa44-185">Configure block at first sight</span></span>](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [<span data-ttu-id="cfa44-186">Utiliser des cmdlets PowerShell pour gérer l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="cfa44-186">Use PowerShell cmdlets to manage Microsoft Defender Antivirus</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- <span data-ttu-id="cfa44-187">[Sécurisation de Windows PC avec Endpoint Protection pour Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span><span class="sxs-lookup"><span data-stu-id="cfa44-187">[Help secure Windows PCs with Endpoint Protection for Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span></span>
- [<span data-ttu-id="cfa44-188">Cmdlets Defender</span><span class="sxs-lookup"><span data-stu-id="cfa44-188">Defender cmdlets</span></span>](/powershell/module/defender/)
- [<span data-ttu-id="cfa44-189">Utiliser la protection microsoft cloud dans Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="cfa44-189">Use Microsoft cloud-delivered protection in Microsoft Defender Antivirus</span></span>](cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="cfa44-190">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="cfa44-190">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)
- [<span data-ttu-id="cfa44-191">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="cfa44-191">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
