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
# <a name="turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-104">Activer la protection par le cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-104">Turn on cloud-delivered protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b43d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b43d6-105">**Applies to:**</span></span>

- [<span data-ttu-id="b43d6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b43d6-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!NOTE]
> <span data-ttu-id="b43d6-107">Le Antivirus Microsoft Defender cloud est un mécanisme permettant de fournir une protection mise à jour à votre réseau et points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b43d6-107">The Microsoft Defender Antivirus cloud service is a mechanism for delivering updated protection to your network and endpoints.</span></span> <span data-ttu-id="b43d6-108">Bien qu’il soit appelé service cloud, il ne s’agit pas simplement de la protection des fichiers stockés dans le cloud . Au lieu de cela, il utilise des ressources distribuées et l’apprentissage automatique pour fournir une protection à vos points de terminaison à une vitesse beaucoup plus rapide que les mises à jour d’intelligence de sécurité traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="b43d6-108">Although it is called a cloud service, it is not simply protection for files stored in the cloud; rather, it uses distributed resources and machine learning to deliver protection to your endpoints at a rate that is far faster than traditional Security intelligence updates.</span></span>

<span data-ttu-id="b43d6-109">Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour offrir une protection précise, en temps réel et intelligente.</span><span class="sxs-lookup"><span data-stu-id="b43d6-109">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, real-time, and intelligent protection.</span></span> <span data-ttu-id="b43d6-110">Faire connaître les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point de [terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="b43d6-110">[Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>

<span data-ttu-id="b43d6-111">Vous pouvez activer ou désactiver Antivirus Microsoft Defender protection cloud de plusieurs manières :</span><span class="sxs-lookup"><span data-stu-id="b43d6-111">You can turn Microsoft Defender Antivirus cloud-delivered protection on or off in several ways:</span></span>

- <span data-ttu-id="b43d6-112">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="b43d6-112">Microsoft Intune</span></span>
- <span data-ttu-id="b43d6-113">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="b43d6-113">Microsoft Endpoint Manager</span></span>
- <span data-ttu-id="b43d6-114">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b43d6-114">Group Policy</span></span>
- <span data-ttu-id="b43d6-115">Cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b43d6-115">PowerShell cmdlets.</span></span>

 <span data-ttu-id="b43d6-116">Vous pouvez également l’activer ou le désactiver dans des clients individuels à l’Sécurité Windows’application.</span><span class="sxs-lookup"><span data-stu-id="b43d6-116">You can also turn it on or off in individual clients with the Windows Security app.</span></span>

<span data-ttu-id="b43d6-117">Voir [Utiliser la protection microsoft cloud pour](cloud-protection-microsoft-defender-antivirus.md) une vue d’ensemble Antivirus Microsoft Defender protection cloud.</span><span class="sxs-lookup"><span data-stu-id="b43d6-117">See [Use Microsoft cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) for an overview of Microsoft Defender Antivirus cloud-delivered protection.</span></span>

<span data-ttu-id="b43d6-118">Pour plus d’informations sur les exigences spécifiques en matière de connectivité réseau pour vous assurer que vos points de terminaison peuvent se connecter au service de protection assurée par le cloud, voir Configurer et valider les [connexions réseau.](configure-network-connections-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="b43d6-118">For more information about the specific network-connectivity requirements to ensure your endpoints can connect to the cloud-delivered protection service, see [Configure and validate network connections](configure-network-connections-microsoft-defender-antivirus.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b43d6-119">Dans Windows 10, il n’existe aucune  différence  entre les options de rapports de base et avancées décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b43d6-119">In Windows 10, there is no difference between the **Basic** and **Advanced** reporting options described in this topic.</span></span> <span data-ttu-id="b43d6-120">Il s’agit d’une distinction héritée et le choix de l’un ou l’autre des paramètres entraîne le même niveau de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="b43d6-120">This is a legacy distinction and choosing either setting will result in the same level of cloud-delivered protection.</span></span> <span data-ttu-id="b43d6-121">Il n’existe aucune différence dans le type ou la quantité d’informations partagées.</span><span class="sxs-lookup"><span data-stu-id="b43d6-121">There is no difference in the type or amount of information that is shared.</span></span> <span data-ttu-id="b43d6-122">Pour plus d’informations sur ce que nous collectons, voir la déclaration [de confidentialité de Microsoft.](https://go.microsoft.com/fwlink/?linkid=521839)</span><span class="sxs-lookup"><span data-stu-id="b43d6-122">For more information on what we collect, see the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=521839).</span></span>

## <a name="use-intune-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-123">Utiliser Intune pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-123">Use Intune to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="b43d6-124">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="b43d6-124">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="b43d6-125">Dans le **volet Accueil,** sélectionnez Configuration de l'> **profils.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-125">On the **Home** pane, select **Device configuration > Profiles**.</span></span>

3. <span data-ttu-id="b43d6-126">Sélectionnez le type **de profil restrictions d’appareil** que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="b43d6-126">Select the **Device restrictions** profile type you want to configure.</span></span> <span data-ttu-id="b43d6-127">Si vous devez créer un type de profil **de restrictions** d’appareil, voir Configurer les paramètres de [restriction d’appareil dans Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="b43d6-127">If you need to create a new **Device restrictions** profile type, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="b43d6-128">Sélectionnez **les**  >  **paramètres de configuration des propriétés :**  >  **Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="b43d6-128">Select **Properties** > **Configuration settings: Edit** > **Microsoft Defender Antivirus**.</span></span>

5. <span data-ttu-id="b43d6-129">Sur le **commutateur de protection cloud,** sélectionnez **Activer.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-129">On the **Cloud-delivered protection** switch, select **Enable**.</span></span>

6. <span data-ttu-id="b43d6-130">Dans la demande **d’utilisateurs avant la** soumission d’exemples, **sélectionnez Envoyer toutes les données automatiquement.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-130">In the **Prompt users before sample submission** dropdown, select **Send all data automatically**.</span></span>

<span data-ttu-id="b43d6-131">Pour plus d’informations sur les profils d’appareil Intune, notamment sur la création et la configuration de leurs paramètres, voir Quelles sont les [Microsoft Intune’appareil ?](/intune/device-profiles)</span><span class="sxs-lookup"><span data-stu-id="b43d6-131">For more information about Intune device profiles, including how to create and configure their settings, see [What are Microsoft Intune device profiles?](/intune/device-profiles)</span></span>

## <a name="use-microsoft-endpoint-manager-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-132">Utiliser Microsoft Endpoint Manager pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-132">Use Microsoft Endpoint Manager to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="b43d6-133">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="b43d6-133">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="b43d6-134">Choisissez **l’Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-134">Choose **Endpoint security** > **Antivirus**.</span></span>

3. <span data-ttu-id="b43d6-135">Sélectionnez un profil antivirus.</span><span class="sxs-lookup"><span data-stu-id="b43d6-135">Select an antivirus profile.</span></span> <span data-ttu-id="b43d6-136">(Si vous n’en avez pas encore, ou si vous souhaitez créer un profil, voir Configurer les [paramètres](/intune/device-restrictions-configure)de restriction d’appareil dans Microsoft Intune .</span><span class="sxs-lookup"><span data-stu-id="b43d6-136">(If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="b43d6-137">Sélectionnez **les propriétés.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-137">Select **Properties**.</span></span> <span data-ttu-id="b43d6-138">Ensuite, en de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-138">Then, next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="b43d6-139">Développez **la protection** cloud, puis dans la liste des niveaux de **protection** cloud, sélectionnez l’une des listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43d6-139">Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:</span></span>
   - <span data-ttu-id="b43d6-140">**Élevé**: applique un niveau de détection élevé.</span><span class="sxs-lookup"><span data-stu-id="b43d6-140">**High**: Applies a strong level of detection.</span></span>
   - <span data-ttu-id="b43d6-141">**Plus élevé**: utilise le **niveau élevé** et applique des mesures de protection supplémentaires (peut avoir un impact sur les performances du client).</span><span class="sxs-lookup"><span data-stu-id="b43d6-141">**High plus**: Uses the **High** level and applies additional protection measures (may impact client performance).</span></span>
   - <span data-ttu-id="b43d6-142">**Tolérance zéro :** bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="b43d6-142">**Zero tolerance**: Blocks all unknown executables.</span></span>

6. <span data-ttu-id="b43d6-143">Sélectionnez **Révision + Enregistrer,** puis **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-143">Select **Review + save**, then choose **Save**.</span></span>

<span data-ttu-id="b43d6-144">Pour plus d’informations sur la configuration Microsoft Endpoint Configuration Manager, voir Comment créer et déployer des stratégies [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)malveillant : service de protection cloud .</span><span class="sxs-lookup"><span data-stu-id="b43d6-144">For more information about configuring Microsoft Endpoint Configuration Manager, see [How to create and deploy antimalware policies: Cloud-protection service](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service).</span></span>

## <a name="use-group-policy-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-145">Utiliser la stratégie de groupe pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-145">Use Group Policy to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="b43d6-146">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-146">On your Group Policy management device, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="b43d6-147">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration de l’ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-147">In the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

3. <span data-ttu-id="b43d6-148">Sélectionnez **modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-148">Select **Administrative templates**.</span></span>

4. <span data-ttu-id="b43d6-149">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > MAPS**</span><span class="sxs-lookup"><span data-stu-id="b43d6-149">Expand the tree to **Windows components > Microsoft Defender Antivirus > MAPS**</span></span>

5. <span data-ttu-id="b43d6-150">Double-cliquez sur **Rejoindre Microsoft MAPS.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-150">Double-click **Join Microsoft MAPS**.</span></span> <span data-ttu-id="b43d6-151">Assurez-vous que l’option est allumée et définie sur **Maps de base** ou Cartes **avancées.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-151">Ensure the option is turned on and set to **Basic MAPS** or **Advanced MAPS**.</span></span> <span data-ttu-id="b43d6-152">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="b43d6-152">Select **OK**.</span></span>

6. <span data-ttu-id="b43d6-153">Double-cliquez sur **Envoyer des exemples de fichier lorsque d’autres analyses sont nécessaires.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-153">Double-click **Send file samples when further analysis is required**.</span></span> <span data-ttu-id="b43d6-154">Assurez-vous que la première option est définie sur **Activé** et que les autres options sont définies sur :</span><span class="sxs-lookup"><span data-stu-id="b43d6-154">Ensure that the first option is set to **Enabled** and that the other options are set to either:</span></span>

    1. <span data-ttu-id="b43d6-155">**Envoyer des exemples sécurisés** (1)</span><span class="sxs-lookup"><span data-stu-id="b43d6-155">**Send safe samples** (1)</span></span>
    2. <span data-ttu-id="b43d6-156">**Envoyer tous les exemples** (3)</span><span class="sxs-lookup"><span data-stu-id="b43d6-156">**Send all samples** (3)</span></span>

        >[!NOTE]
        > <span data-ttu-id="b43d6-157">**L’option Envoyer des échantillons sûrs** (1) signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b43d6-157">The **Send safe samples** (1) option means that most samples will be sent automatically.</span></span> <span data-ttu-id="b43d6-158">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b43d6-158">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>
        > <span data-ttu-id="b43d6-159">La définition de **l’option sur Always Prompt** (0) réduit l’état de protection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b43d6-159">Setting the option to **Always Prompt** (0) will lower the protection state of the device.</span></span> <span data-ttu-id="b43d6-160">Le fait de la définir sur [](configure-block-at-first-sight-microsoft-defender-antivirus.md) **Ne** jamais envoyer (2) signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de terminaison ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="b43d6-160">Setting it to **Never send** (2) means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

7. <span data-ttu-id="b43d6-161">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="b43d6-161">Select **OK**.</span></span>

## <a name="use-powershell-cmdlets-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-162">Utiliser les cmdlets PowerShell pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-162">Use PowerShell cmdlets to turn on cloud-delivered protection</span></span>

<span data-ttu-id="b43d6-163">Les cmdlets suivantes peuvent activer la protection cloud :</span><span class="sxs-lookup"><span data-stu-id="b43d6-163">The following cmdlets can turn on cloud-delivered protection:</span></span>

```PowerShell
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendAllSamples
```

<span data-ttu-id="b43d6-164">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="b43d6-164">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span> <span data-ttu-id="b43d6-165">[Stratégie CSP - Defender](/windows/client-management/mdm/policy-csp-defender) a également plus d’informations spécifiques sur [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span><span class="sxs-lookup"><span data-stu-id="b43d6-165">[Policy CSP - Defender](/windows/client-management/mdm/policy-csp-defender) also has more information specifically on [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span></span>

>[!NOTE]
> <span data-ttu-id="b43d6-166">Vous pouvez également définir **-SubmitSamplesConsent** sur (paramètre par `SendSafeSamples` défaut), `NeverSend` ou `AlwaysPrompt` .</span><span class="sxs-lookup"><span data-stu-id="b43d6-166">You can also set **-SubmitSamplesConsent** to `SendSafeSamples` (the default setting), `NeverSend`, or `AlwaysPrompt`.</span></span> <span data-ttu-id="b43d6-167">Le `SendSafeSamples` paramètre signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b43d6-167">The `SendSafeSamples` setting means that most samples will be sent automatically.</span></span> <span data-ttu-id="b43d6-168">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b43d6-168">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>

>[!WARNING]
> <span data-ttu-id="b43d6-169">Setting **-SubmitSamplesConsent** to `NeverSend` or will lower the protection level of the `AlwaysPrompt` device.</span><span class="sxs-lookup"><span data-stu-id="b43d6-169">Setting **-SubmitSamplesConsent** to `NeverSend` or `AlwaysPrompt` will lower the protection level of the device.</span></span> <span data-ttu-id="b43d6-170">En outre, sa définition signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de `NeverSend` terminaison ne fonctionne pas. [](configure-block-at-first-sight-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="b43d6-170">In addition, setting it to `NeverSend` means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

## <a name="use-windows-management-instruction-wmi-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="b43d6-171">Utiliser Windows Management Instruction (WMI) pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-171">Use Windows Management Instruction (WMI) to turn on cloud-delivered protection</span></span>

<span data-ttu-id="b43d6-172">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43d6-172">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) class for the following properties:</span></span>

```WMI
MAPSReporting
SubmitSamplesConsent
```

<span data-ttu-id="b43d6-173">Pour plus d’informations sur les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="b43d6-173">For more information about allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="turn-on-cloud-delivered-protection-on-individual-clients-with-the-windows-security-app"></a><span data-ttu-id="b43d6-174">Activer la protection cloud sur des clients individuels avec l’application Sécurité Windows cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-174">Turn on cloud-delivered protection on individual clients with the Windows Security app</span></span>

> [!NOTE]
> <span data-ttu-id="b43d6-175">Si le paramètre Configurer le paramètre local de remplacement pour la création de rapports sur la stratégie de groupe **Microsoft MAPS** est **désactivé,** le paramètre de protection basée sur le **cloud** dans Windows Paramètres est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="b43d6-175">If the **Configure local setting override for reporting Microsoft MAPS** Group Policy setting is set to **Disabled**, then the **Cloud-based protection** setting in Windows Settings will be greyed-out and unavailable.</span></span> <span data-ttu-id="b43d6-176">Les modifications apportées via un objet de stratégie de groupe doivent d’abord être déployées vers les points de terminaison individuels avant que le paramètre soit mis à jour dans les Paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="b43d6-176">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

1. <span data-ttu-id="b43d6-177">Ouvrez l’Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-177">Open the Windows Security app by selecting the shield icon in the task bar, or by searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="b43d6-178">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis l’étiquette **paramètres** de protection contre & virus :</span><span class="sxs-lookup"><span data-stu-id="b43d6-178">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Virus & threat protection settings** label:</span></span>

    ![Capture d’écran de l’étiquette des paramètres de protection contre les virus et les menaces dans l’application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="b43d6-180">Confirmez que **la protection basée sur le cloud et** **l’envoi** automatique d’échantillons sont **activés.**</span><span class="sxs-lookup"><span data-stu-id="b43d6-180">Confirm that **Cloud-based Protection** and **Automatic sample submission** are switched to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="b43d6-181">Si l’envoi automatique d’échantillons a été configuré avec la stratégie de groupe, le paramètre est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="b43d6-181">If automatic sample submission has been configured with Group Policy then the setting will be greyed-out and unavailable.</span></span>

## <a name="related-articles"></a><span data-ttu-id="b43d6-182">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b43d6-182">Related articles</span></span>

- [<span data-ttu-id="b43d6-183">Configurer le délai de blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-183">Configure the cloud block timeout period</span></span>](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b43d6-184">Configurer bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="b43d6-184">Configure block at first sight</span></span>](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b43d6-185">Utiliser des cmdlets PowerShell pour gérer l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b43d6-185">Use PowerShell cmdlets to manage Microsoft Defender Antivirus</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- <span data-ttu-id="b43d6-186">[Sécurisation de Windows PC avec Endpoint Protection pour Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span><span class="sxs-lookup"><span data-stu-id="b43d6-186">[Help secure Windows PCs with Endpoint Protection for Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span></span>
- [<span data-ttu-id="b43d6-187">Cmdlets Defender</span><span class="sxs-lookup"><span data-stu-id="b43d6-187">Defender cmdlets</span></span>](/powershell/module/defender/)
- [<span data-ttu-id="b43d6-188">Utiliser la protection microsoft cloud dans Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b43d6-188">Use Microsoft cloud-delivered protection in Microsoft Defender Antivirus</span></span>](cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b43d6-189">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="b43d6-189">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)
- [<span data-ttu-id="b43d6-190">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="b43d6-190">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
