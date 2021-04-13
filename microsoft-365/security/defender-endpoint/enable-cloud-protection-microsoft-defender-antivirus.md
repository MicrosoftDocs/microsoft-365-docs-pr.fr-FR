---
title: Activer la protection cloud dans l'Antivirus Microsoft Defender
description: Activer la protection cloud pour bénéficier des fonctionnalités de protection rapide et avancée.
keywords: Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, cloud, bloquer à la première vue
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.date: 11/13/2020
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.openlocfilehash: cfaf4563e96568ae26bd990678462836b9202656
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690716"
---
# <a name="turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-104">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-104">Turn on cloud-delivered protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5994e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5994e-105">**Applies to:**</span></span>

- [<span data-ttu-id="5994e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5994e-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!NOTE]
> <span data-ttu-id="5994e-107">Le service cloud de l'Antivirus Microsoft Defender est un mécanisme permettant de fournir une protection mise à jour à votre réseau et points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5994e-107">The Microsoft Defender Antivirus cloud service is a mechanism for delivering updated protection to your network and endpoints.</span></span> <span data-ttu-id="5994e-108">Bien qu'il soit appelé service cloud, il ne s'agit pas simplement de la protection des fichiers stockés dans le cloud . Au lieu de cela, il utilise des ressources distribuées et l'apprentissage automatique pour fournir une protection à vos points de terminaison à une vitesse beaucoup plus rapide que les mises à jour d'intelligence de sécurité traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="5994e-108">Although it is called a cloud service, it is not simply protection for files stored in the cloud; rather, it uses distributed resources and machine learning to deliver protection to your endpoints at a rate that is far faster than traditional Security intelligence updates.</span></span>

<span data-ttu-id="5994e-109">L'Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour offrir une protection précise, en temps réel et intelligente.</span><span class="sxs-lookup"><span data-stu-id="5994e-109">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, real-time, and intelligent protection.</span></span> <span data-ttu-id="5994e-110">Faire connaître les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point de [terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="5994e-110">[Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>
<span data-ttu-id="5994e-111">![Liste des moteurs de Microsoft Defender AV](images/microsoft-defender-atp-next-generation-protection-engines.png)</span><span class="sxs-lookup"><span data-stu-id="5994e-111">![List of Microsoft Defender AV engines](images/microsoft-defender-atp-next-generation-protection-engines.png)</span></span>  

<span data-ttu-id="5994e-112">Vous pouvez activer ou désactiver la protection de l'Antivirus Microsoft Defender sur le cloud de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="5994e-112">You can turn Microsoft Defender Antivirus cloud-delivered protection on or off in several ways:</span></span>

- <span data-ttu-id="5994e-113">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="5994e-113">Microsoft Intune</span></span>
- <span data-ttu-id="5994e-114">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5994e-114">Microsoft Endpoint Configuration Manager</span></span>
- <span data-ttu-id="5994e-115">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5994e-115">Group Policy</span></span>
- <span data-ttu-id="5994e-116">Cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5994e-116">PowerShell cmdlets.</span></span>

 <span data-ttu-id="5994e-117">Vous pouvez également l'activer ou le désactiver dans des clients individuels avec l'application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="5994e-117">You can also turn it on or off in individual clients with the Windows Security app.</span></span>

<span data-ttu-id="5994e-118">Pour [obtenir une](cloud-protection-microsoft-defender-antivirus.md) vue d'ensemble de la protection de l'antivirus Microsoft Defender, voir Utiliser la protection microsoft cloud.</span><span class="sxs-lookup"><span data-stu-id="5994e-118">See [Use Microsoft cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) for an overview of Microsoft Defender Antivirus cloud-delivered protection.</span></span>

<span data-ttu-id="5994e-119">Pour plus d'informations sur les exigences de connectivité réseau spécifiques pour vous assurer que vos points de terminaison peuvent se connecter au service de protection livré par le cloud, voir Configurer et valider les [connexions réseau.](configure-network-connections-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="5994e-119">For more information about the specific network-connectivity requirements to ensure your endpoints can connect to the cloud-delivered protection service, see [Configure and validate network connections](configure-network-connections-microsoft-defender-antivirus.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5994e-120">Dans Windows 10, il n'existe  aucune différence entre les options de rapports de base et avancées décrites dans cette rubrique. </span><span class="sxs-lookup"><span data-stu-id="5994e-120">In Windows 10, there is no difference between the **Basic** and **Advanced** reporting options described in this topic.</span></span> <span data-ttu-id="5994e-121">Il s'agit d'une distinction héritée et le choix de l'un ou l'autre des paramètres entraîne le même niveau de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="5994e-121">This is a legacy distinction and choosing either setting will result in the same level of cloud-delivered protection.</span></span> <span data-ttu-id="5994e-122">Il n'existe aucune différence dans le type ou la quantité d'informations partagées.</span><span class="sxs-lookup"><span data-stu-id="5994e-122">There is no difference in the type or amount of information that is shared.</span></span> <span data-ttu-id="5994e-123">Pour plus d'informations sur ce que nous collectons, voir la déclaration [de confidentialité de Microsoft.](https://go.microsoft.com/fwlink/?linkid=521839)</span><span class="sxs-lookup"><span data-stu-id="5994e-123">For more information on what we collect, see the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=521839).</span></span>

## <a name="use-intune-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-124">Utiliser Intune pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-124">Use Intune to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="5994e-125">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="5994e-125">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>
2. <span data-ttu-id="5994e-126">Dans le **volet Accueil,** sélectionnez Configuration de l'> **profils.**</span><span class="sxs-lookup"><span data-stu-id="5994e-126">On the **Home** pane, select **Device configuration > Profiles**.</span></span>
3. <span data-ttu-id="5994e-127">Sélectionnez le type **de profil restrictions d'appareil** que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="5994e-127">Select the **Device restrictions** profile type you want to configure.</span></span> <span data-ttu-id="5994e-128">Si vous devez créer un type de profil de **restrictions** d'appareil, voir Configurer les [paramètres de restriction d'appareil dans Microsoft Intune.](/intune/device-restrictions-configure)</span><span class="sxs-lookup"><span data-stu-id="5994e-128">If you need to create a new **Device restrictions** profile type, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>
4. <span data-ttu-id="5994e-129">Sélectionnez **les**  >  **paramètres de configuration des propriétés : modifier**  >  **l'Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="5994e-129">Select **Properties** > **Configuration settings: Edit** > **Microsoft Defender Antivirus**.</span></span>
5. <span data-ttu-id="5994e-130">Sur le **commutateur de protection cloud,** sélectionnez **Activer.**</span><span class="sxs-lookup"><span data-stu-id="5994e-130">On the **Cloud-delivered protection** switch, select **Enable**.</span></span>
6. <span data-ttu-id="5994e-131">Dans la demande **d'utilisateurs avant la** soumission d'exemples, **sélectionnez Envoyer toutes les données automatiquement.**</span><span class="sxs-lookup"><span data-stu-id="5994e-131">In the **Prompt users before sample submission** dropdown, select **Send all data automatically**.</span></span>

<span data-ttu-id="5994e-132">Pour plus d'informations sur les profils d'appareil Intune, notamment sur la création et la configuration de leurs paramètres, voir Qu'est-ce que les profils [d'appareil Microsoft Intune ?](/intune/device-profiles)</span><span class="sxs-lookup"><span data-stu-id="5994e-132">For more information about Intune device profiles, including how to create and configure their settings, see [What are Microsoft Intune device profiles?](/intune/device-profiles)</span></span>

## <a name="use-microsoft-endpoint-manager-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-133">Utiliser Microsoft Endpoint Manager pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-133">Use Microsoft Endpoint Manager to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="5994e-134">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="5994e-134">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>
2. <span data-ttu-id="5994e-135">Choisissez **l'Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="5994e-135">Choose **Endpoint security** > **Antivirus**.</span></span>
3. <span data-ttu-id="5994e-136">Sélectionnez un profil antivirus.</span><span class="sxs-lookup"><span data-stu-id="5994e-136">Select an antivirus profile.</span></span> <span data-ttu-id="5994e-137">(Si vous n'en avez pas encore, ou si vous souhaitez créer un profil, voir Configurer les paramètres de [restriction d'appareil dans Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="5994e-137">(If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>
4. <span data-ttu-id="5994e-138">Sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5994e-138">Select **Properties**.</span></span> <span data-ttu-id="5994e-139">Ensuite, en de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="5994e-139">Then, next to **Configuration settings**, choose **Edit**.</span></span>
5. <span data-ttu-id="5994e-140">Développez **la protection** cloud, puis dans la liste des niveaux de **protection** cloud, sélectionnez l'une des listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5994e-140">Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:</span></span>
    1. <span data-ttu-id="5994e-141">**Élevé**: applique un niveau élevé de détection.</span><span class="sxs-lookup"><span data-stu-id="5994e-141">**High**: Applies a strong level of detection.</span></span>
    2. <span data-ttu-id="5994e-142">**Plus élevé**: utilise le **niveau élevé** et applique des mesures de protection supplémentaires (peut avoir un impact sur les performances du client).</span><span class="sxs-lookup"><span data-stu-id="5994e-142">**High plus**: Uses the **High** level and applies additional protection measures (may impact client performance).</span></span>
    3. <span data-ttu-id="5994e-143">**Tolérance zéro :** bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="5994e-143">**Zero tolerance**: Blocks all unknown executables.</span></span>
6. <span data-ttu-id="5994e-144">Sélectionnez **Révision + Enregistrer,** puis **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="5994e-144">Select **Review + save**, then choose **Save**.</span></span>

<span data-ttu-id="5994e-145">Pour plus d'informations sur la configuration de Microsoft Endpoint Configuration Manager, voir Comment créer et déployer des stratégies [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)malveillant : service de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="5994e-145">For more information about configuring Microsoft Endpoint Configuration Manager, see [How to create and deploy antimalware policies: Cloud-protection service](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service).</span></span>

## <a name="use-group-policy-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-146">Utiliser une stratégie de groupe pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-146">Use Group Policy to turn on cloud-delivered protection</span></span>

1. <span data-ttu-id="5994e-147">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="5994e-147">On your Group Policy management device, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="5994e-148">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration de l'ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="5994e-148">In the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

3. <span data-ttu-id="5994e-149">Sélectionnez **modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="5994e-149">Select **Administrative templates**.</span></span>

4. <span data-ttu-id="5994e-150">Développez l'arborescence **des composants Windows >'antivirus Microsoft Defender > MAPS**</span><span class="sxs-lookup"><span data-stu-id="5994e-150">Expand the tree to **Windows components > Microsoft Defender Antivirus > MAPS**</span></span>

5. <span data-ttu-id="5994e-151">Double-cliquez sur **Rejoindre Microsoft MAPS.**</span><span class="sxs-lookup"><span data-stu-id="5994e-151">Double-click **Join Microsoft MAPS**.</span></span> <span data-ttu-id="5994e-152">Assurez-vous que l'option est allumée et définie sur **Maps de base** ou Cartes **avancées.**</span><span class="sxs-lookup"><span data-stu-id="5994e-152">Ensure the option is turned on and set to **Basic MAPS** or **Advanced MAPS**.</span></span> <span data-ttu-id="5994e-153">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="5994e-153">Select **OK**.</span></span>

6. <span data-ttu-id="5994e-154">Double-cliquez sur **Envoyer des exemples de fichier lorsque d'autres analyses sont nécessaires.**</span><span class="sxs-lookup"><span data-stu-id="5994e-154">Double-click **Send file samples when further analysis is required**.</span></span> <span data-ttu-id="5994e-155">Assurez-vous que la première option est définie sur **Activé** et que les autres options sont définies sur :</span><span class="sxs-lookup"><span data-stu-id="5994e-155">Ensure that the first option is set to **Enabled** and that the other options are set to either:</span></span>

    1. <span data-ttu-id="5994e-156">**Envoyer des exemples sécurisés** (1)</span><span class="sxs-lookup"><span data-stu-id="5994e-156">**Send safe samples** (1)</span></span>
    2. <span data-ttu-id="5994e-157">**Envoyer tous les exemples** (3)</span><span class="sxs-lookup"><span data-stu-id="5994e-157">**Send all samples** (3)</span></span>

        >[!NOTE]
        > <span data-ttu-id="5994e-158">**L'option Envoyer des échantillons sûrs** (1) signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5994e-158">The **Send safe samples** (1) option means that most samples will be sent automatically.</span></span> <span data-ttu-id="5994e-159">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5994e-159">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>

        > [!WARNING]
        > <span data-ttu-id="5994e-160">Définir l'option **sur Always Prompt** (0) réduit l'état de protection de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="5994e-160">Setting the option to **Always Prompt** (0) will lower the protection state of the device.</span></span> <span data-ttu-id="5994e-161">Le fait de la définir sur [](configure-block-at-first-sight-microsoft-defender-antivirus.md) **Ne** jamais envoyer (2) signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de terminaison ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="5994e-161">Setting it to **Never send** (2) means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

7. <span data-ttu-id="5994e-162">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="5994e-162">Select **OK**.</span></span>

## <a name="use-powershell-cmdlets-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-163">Utiliser les cmdlets PowerShell pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-163">Use PowerShell cmdlets to turn on cloud-delivered protection</span></span>

<span data-ttu-id="5994e-164">Les cmdlets suivantes peuvent activer la protection cloud :</span><span class="sxs-lookup"><span data-stu-id="5994e-164">The following cmdlets can turn on cloud-delivered protection:</span></span>

```PowerShell
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendAllSamples
```

<span data-ttu-id="5994e-165">Pour plus d'informations sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et les [cmdlets Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="5994e-165">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span> <span data-ttu-id="5994e-166">[Stratégie CSP - Defender](/windows/client-management/mdm/policy-csp-defender) a également plus d'informations spécifiques sur [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span><span class="sxs-lookup"><span data-stu-id="5994e-166">[Policy CSP - Defender](/windows/client-management/mdm/policy-csp-defender) also has more information specifically on [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).</span></span>

>[!NOTE]
> <span data-ttu-id="5994e-167">Vous pouvez également définir **-SubmitSamplesConsent** sur (paramètre par `SendSafeSamples` défaut), `NeverSend` ou `AlwaysPrompt` .</span><span class="sxs-lookup"><span data-stu-id="5994e-167">You can also set **-SubmitSamplesConsent** to `SendSafeSamples` (the default setting), `NeverSend`, or `AlwaysPrompt`.</span></span> <span data-ttu-id="5994e-168">Le `SendSafeSamples` paramètre signifie que la plupart des échantillons seront envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5994e-168">The `SendSafeSamples` setting means that most samples will be sent automatically.</span></span> <span data-ttu-id="5994e-169">Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5994e-169">Files that are likely to contain personal information will still prompt and require additional confirmation.</span></span>

>[!WARNING]
> <span data-ttu-id="5994e-170">Setting **-SubmitSamplesConsent** to `NeverSend` or will lower the protection level of the `AlwaysPrompt` device.</span><span class="sxs-lookup"><span data-stu-id="5994e-170">Setting **-SubmitSamplesConsent** to `NeverSend` or `AlwaysPrompt` will lower the protection level of the device.</span></span> <span data-ttu-id="5994e-171">En outre, sa définition signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de `NeverSend` terminaison ne fonctionne pas. [](configure-block-at-first-sight-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="5994e-171">In addition, setting it to `NeverSend` means that the [Block at First Sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) feature of Microsoft Defender for Endpoint won't work.</span></span>

## <a name="use-windows-management-instruction-wmi-to-turn-on-cloud-delivered-protection"></a><span data-ttu-id="5994e-172">Utiliser Windows Management Instruction (WMI) pour activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-172">Use Windows Management Instruction (WMI) to turn on cloud-delivered protection</span></span>

<span data-ttu-id="5994e-173">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="5994e-173">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) class for the following properties:</span></span>

```WMI
MAPSReporting
SubmitSamplesConsent
```

<span data-ttu-id="5994e-174">Pour plus d'informations sur les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="5994e-174">For more information about allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="turn-on-cloud-delivered-protection-on-individual-clients-with-the-windows-security-app"></a><span data-ttu-id="5994e-175">Activer la protection cloud sur des clients individuels avec l'application Sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="5994e-175">Turn on cloud-delivered protection on individual clients with the Windows Security app</span></span>

> [!NOTE]
> <span data-ttu-id="5994e-176">Si le paramètre Configurer le remplacement de paramètre local pour la création de rapports sur la stratégie de groupe **Microsoft MAPS** est **désactivé,** le paramètre de protection basée sur le **cloud** dans les paramètres Windows est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="5994e-176">If the **Configure local setting override for reporting Microsoft MAPS** Group Policy setting is set to **Disabled**, then the **Cloud-based protection** setting in Windows Settings will be greyed-out and unavailable.</span></span> <span data-ttu-id="5994e-177">Les modifications apportées via un objet de stratégie de groupe doivent d'abord être déployées sur des points de terminaison individuels avant que le paramètre ne soit mis à jour dans les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="5994e-177">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

1. <span data-ttu-id="5994e-178">Ouvrez l'application Sécurité Windows en sélectionnant l'icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="5994e-178">Open the Windows Security app by selecting the shield icon in the task bar, or by searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="5994e-179">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l'icône de bouclier dans la barre de menus de gauche), puis l'étiquette des **paramètres** de protection contre & virus :</span><span class="sxs-lookup"><span data-stu-id="5994e-179">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Virus & threat protection settings** label:</span></span>

    ![Capture d'écran de l'étiquette & protection contre les virus dans l'application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="5994e-181">Confirmez que **la protection basée sur le cloud et** **l'envoi** automatique d'échantillons sont **activés.**</span><span class="sxs-lookup"><span data-stu-id="5994e-181">Confirm that **Cloud-based Protection** and **Automatic sample submission** are switched to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="5994e-182">Si l'envoi automatique d'échantillons a été configuré avec la stratégie de groupe, le paramètre est grisé et indisponible.</span><span class="sxs-lookup"><span data-stu-id="5994e-182">If automatic sample submission has been configured with Group Policy then the setting will be greyed-out and unavailable.</span></span>

## <a name="related-articles"></a><span data-ttu-id="5994e-183">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="5994e-183">Related articles</span></span>

- [<span data-ttu-id="5994e-184">Configurer le délai d'attente du blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-184">Configure the cloud block timeout period</span></span>](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md)
- [<span data-ttu-id="5994e-185">Configurer bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="5994e-185">Configure block at first sight</span></span>](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [<span data-ttu-id="5994e-186">Utiliser les cmdlets PowerShell pour gérer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5994e-186">Use PowerShell cmdlets to manage Microsoft Defender Antivirus</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- <span data-ttu-id="5994e-187">[Sécurisation des PC Windows avec Endpoint Protection pour Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span><span class="sxs-lookup"><span data-stu-id="5994e-187">[Help secure Windows PCs with Endpoint Protection for Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]</span></span>
- [<span data-ttu-id="5994e-188">Cmdlets Defender</span><span class="sxs-lookup"><span data-stu-id="5994e-188">Defender cmdlets</span></span>](/powershell/module/defender/)
- [<span data-ttu-id="5994e-189">Utiliser la protection microsoft cloud dans l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5994e-189">Use Microsoft cloud-delivered protection in Microsoft Defender Antivirus</span></span>](cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="5994e-190">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="5994e-190">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)
- [<span data-ttu-id="5994e-191">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="5994e-191">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)