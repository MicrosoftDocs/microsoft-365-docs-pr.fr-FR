---
title: Conditions minimales requises pour Microsoft Defender pour le point de terminaison
description: Comprendre les conditions requises en matière de licences pour l’intégration d’appareils au service
keywords: exigences minimales, licences, tableau de comparaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: ccff6abcfcd1a2da32a8e1614a2de45afed69aef
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842997"
---
# <a name="minimum-requirements-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="fa0dc-104">Conditions minimales requises pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa0dc-104">Minimum requirements for Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fa0dc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fa0dc-105">**Applies to:**</span></span>

- [<span data-ttu-id="fa0dc-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa0dc-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="fa0dc-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fa0dc-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="fa0dc-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fa0dc-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fa0dc-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-minreqs-abovefoldlink)


<span data-ttu-id="fa0dc-110">Certaines conditions minimales sont requises pour l’intégration d’appareils au service.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-110">There are some minimum requirements for onboarding devices to the service.</span></span> <span data-ttu-id="fa0dc-111">Découvrez les licences, la configuration matérielle et logicielle requise et d’autres paramètres de configuration pour intégrer des appareils au service.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-111">Learn about the licensing, hardware and software requirements, and other configuration settings to onboard devices to the service.</span></span>

> [!TIP]
> - <span data-ttu-id="fa0dc-112">Découvrez les dernières améliorations apportées à Defender for Endpoint : [Defender for Endpoint Tech Community](https://techcommunity.microsoft.com/t5/Windows-Defender-Advanced-Threat/ct-p/WindowsDefenderAdvanced).</span><span class="sxs-lookup"><span data-stu-id="fa0dc-112">Learn about the latest enhancements in Defender for Endpoint: [Defender for Endpoint Tech Community](https://techcommunity.microsoft.com/t5/Windows-Defender-Advanced-Threat/ct-p/WindowsDefenderAdvanced).</span></span>
> - <span data-ttu-id="fa0dc-113">Defender pour le point de terminaison a démontré les fonctionnalités d’optique et de détection de pointe du secteur dans l’évaluation MITRE récente.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-113">Defender for Endpoint demonstrated industry-leading optics and detection capabilities in the recent MITRE evaluation.</span></span> <span data-ttu-id="fa0dc-114">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span><span class="sxs-lookup"><span data-stu-id="fa0dc-114">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="fa0dc-115">Conditions d'octroi de licence</span><span class="sxs-lookup"><span data-stu-id="fa0dc-115">Licensing requirements</span></span>

<span data-ttu-id="fa0dc-116">Microsoft Defender pour le point de terminaison nécessite l’une des offres de licence en volume Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-116">Microsoft Defender for Endpoint requires one of the following Microsoft volume licensing offers:</span></span>

- <span data-ttu-id="fa0dc-117">Windows 10 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-117">Windows 10 Enterprise E5</span></span>
- <span data-ttu-id="fa0dc-118">Windows 10 Éducation A5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-118">Windows 10 Education A5</span></span>
- <span data-ttu-id="fa0dc-119">Microsoft 365 E5 (M365 E5) qui inclut Windows 10 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-119">Microsoft 365 E5 (M365 E5) which includes Windows 10 Enterprise E5</span></span>
- <span data-ttu-id="fa0dc-120">Microsoft 365 A5 (M365 A5)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-120">Microsoft 365 A5 (M365 A5)</span></span>
- <span data-ttu-id="fa0dc-121">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="fa0dc-121">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="fa0dc-122">Sécurité Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-122">Microsoft 365 A5 Security</span></span>
- <span data-ttu-id="fa0dc-123">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa0dc-123">Microsoft Defender for Endpoint</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-124">Les utilisateurs titulaires d’une licence éligible peuvent utiliser Microsoft Defender pour endpoint sur cinq appareils simultanés au plus.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-124">Eligible licensed users may use Microsoft Defender for Endpoint on up to five concurrent devices.</span></span>
> <span data-ttu-id="fa0dc-125">Microsoft Defender for Endpoint est également disponible à l’achat auprès d’un fournisseur de solutions Cloud (CSP).</span><span class="sxs-lookup"><span data-stu-id="fa0dc-125">Microsoft Defender for Endpoint is also available for purchase from a Cloud Solution Provider (CSP).</span></span>
> <span data-ttu-id="fa0dc-126">Les VM RDSH ne nécessitent pas de licence Defender for Endpoint distincte.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-126">RDSH VMs do not require a separate Defender for Endpoint license.</span></span>

<span data-ttu-id="fa0dc-127">Microsoft Defender pour le point de terminaison pour les serveurs nécessite l’une des options de licence suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-127">Microsoft Defender for Endpoint for servers requires one of the following licensing options:</span></span>

- [<span data-ttu-id="fa0dc-128">Centre de sécurité Azure avec Azure Defender activé</span><span class="sxs-lookup"><span data-stu-id="fa0dc-128">Azure Security Center with Azure Defender enabled</span></span>](/azure/security-center/security-center-pricing)
- <span data-ttu-id="fa0dc-129">Microsoft Defender for Endpoint for Server (un par serveur couvert)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-129">Microsoft Defender for Endpoint for Server (one per covered server)</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-130">Les clients peuvent acquérir des licences serveur (une par environnement de système d’exploitation de serveur couvert) pour Microsoft Defender pour Endpoint for Servers s’ils ont un minimum combiné de 50 licences pour une ou plusieurs des licences utilisateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-130">Customers may acquire server licenses (one per covered server Operating System Environment (OSE)) for Microsoft Defender for Endpoint for Servers if they have a combined minimum of 50 licenses for one or more of the following user licenses:</span></span>
>
> * <span data-ttu-id="fa0dc-131">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa0dc-131">Microsoft Defender for Endpoint</span></span>
> * <span data-ttu-id="fa0dc-132">Windows E5/A5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-132">Windows E5/A5</span></span>
> * <span data-ttu-id="fa0dc-133">Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-133">Microsoft 365 E5/A5</span></span>
> * <span data-ttu-id="fa0dc-134">Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="fa0dc-134">Microsoft 365 E5/A5 Security</span></span>

<span data-ttu-id="fa0dc-135">Pour obtenir des informations détaillées sur les licences, consultez le [site](https://www.microsoft.com/licensing/terms/) Termes du produit et travaillez avec votre équipe de compte pour en savoir plus sur les conditions générales.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-135">For detailed licensing information, see the [Product Terms site](https://www.microsoft.com/licensing/terms/) and work with your account team to learn more about the terms and conditions.</span></span>

<span data-ttu-id="fa0dc-136">Pour plus d’informations sur le tableau des fonctionnalités Windows 10 éditions, voir [Comparer Windows 10 éditions.](https://www.microsoft.com/windowsforbusiness/compare)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-136">For more information on the array of features in Windows 10 editions, see [Compare Windows 10 editions](https://www.microsoft.com/windowsforbusiness/compare).</span></span>

<span data-ttu-id="fa0dc-137">Pour obtenir un tableau de comparaison détaillé de Windows 10 d’édition commerciale, voir [la comparaison PDF](https://wfbdevicemanagementprod.blob.core.windows.net/windowsforbusiness/Windows10_CommercialEdition_Comparison.pdf).</span><span class="sxs-lookup"><span data-stu-id="fa0dc-137">For a detailed comparison table of Windows 10 commercial edition comparison, see the [comparison PDF](https://wfbdevicemanagementprod.blob.core.windows.net/windowsforbusiness/Windows10_CommercialEdition_Comparison.pdf).</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="fa0dc-138">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="fa0dc-138">Browser requirements</span></span>

<span data-ttu-id="fa0dc-139">L’accès à Defender pour le point de terminaison s’fait par le biais d’un navigateur, qui permet de prendre en charge les navigateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-139">Access to Defender for Endpoint is done through a browser, supporting the following browsers:</span></span>

- <span data-ttu-id="fa0dc-140">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fa0dc-140">Microsoft Edge</span></span>
- <span data-ttu-id="fa0dc-141">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="fa0dc-141">Google Chrome</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-142">Bien que d’autres navigateurs fonctionnent, les navigateurs mentionnés sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-142">While other browsers might work, the mentioned browsers are the ones supported.</span></span>


## <a name="hardware-and-software-requirements"></a><span data-ttu-id="fa0dc-143">Configuration matérielle et logicielle requise</span><span class="sxs-lookup"><span data-stu-id="fa0dc-143">Hardware and software requirements</span></span>

### <a name="supported-windows-versions"></a><span data-ttu-id="fa0dc-144">Versions Windows pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0dc-144">Supported Windows versions</span></span>

- <span data-ttu-id="fa0dc-145">Windows 7 SP1 Enterprise ([Nécessite ESU pour la prise en charge.)](/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-145">Windows 7 SP1 Enterprise ([Requires ESU for support](/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span></span>
- <span data-ttu-id="fa0dc-146">Windows 7 SP1 Pro ([Nécessite ESU pour la prise en charge.)](/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-146">Windows 7 SP1 Pro ([Requires ESU for support](/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span></span>
- <span data-ttu-id="fa0dc-147">Windows 8.1 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fa0dc-147">Windows 8.1 Enterprise</span></span>
- <span data-ttu-id="fa0dc-148">Windows 8.1 Professionnel</span><span class="sxs-lookup"><span data-stu-id="fa0dc-148">Windows 8.1 Pro</span></span>
- <span data-ttu-id="fa0dc-149">Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fa0dc-149">Windows 10 Enterprise</span></span>
- [<span data-ttu-id="fa0dc-150">Windows 10 Entreprise LTSC 2016 (ou une ultérieure)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-150">Windows 10 Enterprise LTSC 2016 (or later)</span></span>](/windows/whats-new/ltsc/)
- <span data-ttu-id="fa0dc-151">Windows 10 Éducation</span><span class="sxs-lookup"><span data-stu-id="fa0dc-151">Windows 10 Education</span></span>
- <span data-ttu-id="fa0dc-152">Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="fa0dc-152">Windows 10 Pro</span></span>
- <span data-ttu-id="fa0dc-153">Windows 10 Professionnel Éducation</span><span class="sxs-lookup"><span data-stu-id="fa0dc-153">Windows 10 Pro Education</span></span>
- <span data-ttu-id="fa0dc-154">Windows serveur</span><span class="sxs-lookup"><span data-stu-id="fa0dc-154">Windows server</span></span>
  - <span data-ttu-id="fa0dc-155">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="fa0dc-155">Windows Server 2008 R2 SP1</span></span>
  - <span data-ttu-id="fa0dc-156">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa0dc-156">Windows Server 2012 R2</span></span>
  - <span data-ttu-id="fa0dc-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fa0dc-157">Windows Server 2016</span></span>
  - <span data-ttu-id="fa0dc-158">Windows Serveur, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="fa0dc-158">Windows Server, version 1803 or later</span></span>
  - <span data-ttu-id="fa0dc-159">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="fa0dc-159">Windows Server 2019</span></span>
- <span data-ttu-id="fa0dc-160">Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="fa0dc-160">Windows Virtual Desktop</span></span>

<span data-ttu-id="fa0dc-161">Les appareils de votre réseau doivent être en cours d’exécution dans l’une de ces éditions.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-161">Devices on your network must be running one of these editions.</span></span>

<span data-ttu-id="fa0dc-162">La configuration matérielle requise pour Defender pour Endpoint sur les appareils est la même pour les éditions pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-162">The hardware requirements for Defender for Endpoint on devices are the same for the supported editions.</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-163">Les ordinateurs exécutant des versions mobiles de Windows (tels que Windows CE et Windows 10 Mobile) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-163">Machines running mobile versions of Windows (such as Windows CE and Windows 10 Mobile) aren't supported.</span></span>
>
> <span data-ttu-id="fa0dc-164">Les ordinateurs virtuels Windows 10 Entreprise 2016 LTSB peuvent rencontrer des problèmes de performances s’ils sont exécutés sur des plateformes de virtualisation autres que Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-164">Virtual Machines running Windows 10 Enterprise 2016 LTSB may encounter performance issues if run on non-Microsoft virtualization platforms.</span></span>
>
> <span data-ttu-id="fa0dc-165">Pour les environnements virtuels, nous vous recommandons Windows 10 Entreprise LTSC 2019 ou une ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-165">For virtual environments, we recommend using Windows 10 Enterprise LTSC 2019 or later.</span></span>


### <a name="other-supported-operating-systems"></a><span data-ttu-id="fa0dc-166">Autres systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0dc-166">Other supported operating systems</span></span>

- [<span data-ttu-id="fa0dc-167">Android</span><span class="sxs-lookup"><span data-stu-id="fa0dc-167">Android</span></span>](microsoft-defender-endpoint-android.md)
- [<span data-ttu-id="fa0dc-168">iOS</span><span class="sxs-lookup"><span data-stu-id="fa0dc-168">iOS</span></span>](microsoft-defender-endpoint-ios.md)
- [<span data-ttu-id="fa0dc-169">Linux</span><span class="sxs-lookup"><span data-stu-id="fa0dc-169">Linux</span></span>](microsoft-defender-endpoint-linux.md)
- [<span data-ttu-id="fa0dc-170">MacOS</span><span class="sxs-lookup"><span data-stu-id="fa0dc-170">macOS</span></span>](microsoft-defender-endpoint-mac.md)

> [!NOTE]
> <span data-ttu-id="fa0dc-171">Vous devez vérifier que les distributions linux et les versions d’Android, iOS et macOS sont compatibles avec Defender for Endpoint pour que l’intégration fonctionne.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-171">You'll need to confirm the Linux distributions and versions of Android, iOS, and macOS are compatible with Defender for Endpoint for the integration to work.</span></span>



### <a name="network-and-data-storage-and-configuration-requirements"></a><span data-ttu-id="fa0dc-172">Configuration requise pour le stockage réseau et les données</span><span class="sxs-lookup"><span data-stu-id="fa0dc-172">Network and data storage and configuration requirements</span></span>

<span data-ttu-id="fa0dc-173">Lorsque vous exécutez l’Assistant d’intégration pour la première fois, vous devez choisir l’endroit où sont stockées vos informations relatives aux points de terminaison Microsoft Defender : dans l’Union européenne, le Royaume-Uni ou le centre de données des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-173">When you run the onboarding wizard for the first time, you must choose where your Microsoft Defender for Endpoint-related information is stored: in the European Union, the United Kingdom, or the United States datacenter.</span></span>

> [!NOTE]
> - <span data-ttu-id="fa0dc-174">Vous ne pouvez pas modifier votre emplacement de stockage de données après la première installation.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-174">You cannot change your data storage location after the first-time setup.</span></span>
> - <span data-ttu-id="fa0dc-175">Pour plus d’informations sur l’endroit et la façon dont Microsoft stocke vos données, voir Microsoft Defender for [Endpoint data storage and privacy.](data-storage-privacy.md)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-175">Review the [Microsoft Defender for Endpoint data storage and privacy](data-storage-privacy.md) for more information on where and how Microsoft stores your data.</span></span>


### <a name="diagnostic-data-settings"></a><span data-ttu-id="fa0dc-176">Paramètres de données de diagnostic</span><span class="sxs-lookup"><span data-stu-id="fa0dc-176">Diagnostic data settings</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-177">Microsoft Defender pour point de terminaison ne nécessite aucun niveau de diagnostic spécifique tant qu’il est activé.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-177">Microsoft Defender for Endpoint doesn't require any specific diagnostic level as long as it's enabled.</span></span>

<span data-ttu-id="fa0dc-178">Assurez-vous que le service de données de diagnostic est activé sur tous les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-178">Make sure that the diagnostic data service is enabled on all the devices in your organization.</span></span>
<span data-ttu-id="fa0dc-179">Par défaut, ce service est activé.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-179">By default, this service is enabled.</span></span> <span data-ttu-id="fa0dc-180">Il est bon de vérifier que vous obtenez des données de capteur à partir de ces données.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-180">It's good practice to check to ensure that you'll get sensor data from them.</span></span>

<span data-ttu-id="fa0dc-181">**Utilisez la ligne de commande pour vérifier le type** Windows 10 de démarrage du service de données de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-181">**Use the command line to check the Windows 10 diagnostic data service startup type**:</span></span>

1. <span data-ttu-id="fa0dc-182">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-182">Open an elevated command-line prompt on the device:</span></span>

   1.  <span data-ttu-id="fa0dc-183">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-183">Go to **Start** and type **cmd**.</span></span>

   1.  <span data-ttu-id="fa0dc-184">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-184">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="fa0dc-185">Entrez la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="fa0dc-185">Enter the following command, and press **Enter**:</span></span>

   ```console
   sc qc diagtrack
   ```

   <span data-ttu-id="fa0dc-186">Si le service est activé, le résultat doit ressembler à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-186">If the service is enabled, then the result should look like the following screenshot:</span></span>

   ![Résultat de la commande de requête sc pour diagtrack](images/windefatp-sc-qc-diagtrack.png)


<span data-ttu-id="fa0dc-188">Vous devez configurer le service pour qu’il démarre automatiquement si la START_TYPE n’est pas définie sur **AUTO_START**. </span><span class="sxs-lookup"><span data-stu-id="fa0dc-188">You'll need to set the service to automatically start if the **START_TYPE** isn't set to **AUTO_START**.</span></span>


<span data-ttu-id="fa0dc-189">**Utilisez la ligne de commande pour configurer Windows 10 service de données de diagnostic pour démarrer automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="fa0dc-189">**Use the command line to set the Windows 10 diagnostic data service to automatically start:**</span></span>

1.  <span data-ttu-id="fa0dc-190">Ouvrez une invite de ligne de commande avec élévation de niveaux sur le point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="fa0dc-190">Open an elevated command-line prompt on the endpoint:</span></span>

    1. <span data-ttu-id="fa0dc-191">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-191">Go to **Start** and type **cmd**.</span></span>

    1. <span data-ttu-id="fa0dc-192">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-192">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2.  <span data-ttu-id="fa0dc-193">Entrez la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="fa0dc-193">Enter the following command, and press **Enter**:</span></span>

    ```console
    sc config diagtrack start=auto
    ```

3.  <span data-ttu-id="fa0dc-194">Un message de réussite s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-194">A success message is displayed.</span></span> <span data-ttu-id="fa0dc-195">Vérifiez la modification en entrant la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="fa0dc-195">Verify the change by entering the following command, and press **Enter**:</span></span>

    ```console
    sc qc diagtrack
    ```


#### <a name="internet-connectivity"></a><span data-ttu-id="fa0dc-196">Connexion à Internet</span><span class="sxs-lookup"><span data-stu-id="fa0dc-196">Internet connectivity</span></span>

<span data-ttu-id="fa0dc-197">La connectivité Internet sur les appareils est requise directement ou par proxy.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-197">Internet connectivity on devices is required either directly or through proxy.</span></span>

<span data-ttu-id="fa0dc-198">Le capteur Defender pour point de terminaison peut utiliser une bande passante moyenne quotidienne de 5 Mo pour communiquer avec le service cloud Defender for Endpoint et signaler les cyber-données.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-198">The Defender for Endpoint sensor can use a daily average bandwidth of 5 MB to communicate with the Defender for Endpoint cloud service and report cyber data.</span></span> <span data-ttu-id="fa0dc-199">Les activités non limitées, telles que les téléchargements de fichiers et la collecte de packages d’enquête, ne sont pas incluses dans cette bande passante moyenne quotidienne.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-199">One-off activities such as file uploads and investigation package collection aren't included in this daily average bandwidth.</span></span>

<span data-ttu-id="fa0dc-200">Pour plus d’informations sur les paramètres de configuration proxy supplémentaires, voir Configurer les [paramètres de proxy d’appareil](configure-proxy-internet.md)et de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-200">For more information on additional proxy configuration settings, see [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md).</span></span>

<span data-ttu-id="fa0dc-201">Avant d’intégrer des appareils, le service de données de diagnostic doit être activé.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-201">Before you onboard devices, the diagnostic data service must be enabled.</span></span> <span data-ttu-id="fa0dc-202">Le service est activé par défaut dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-202">The service is enabled by default in Windows 10.</span></span>


## <a name="microsoft-defender-antivirus-configuration-requirement"></a><span data-ttu-id="fa0dc-203">Antivirus Microsoft Defender configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa0dc-203">Microsoft Defender Antivirus configuration requirement</span></span>

<span data-ttu-id="fa0dc-204">L’agent Defender for Endpoint dépend de la capacité de l’Antivirus Microsoft Defender analyser les fichiers et de fournir des informations les concernant.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-204">The Defender for Endpoint agent depends on the ability of Microsoft Defender Antivirus to scan files and provide information about them.</span></span>

<span data-ttu-id="fa0dc-205">Configurez les mises à jour d’intelligence de sécurité sur les appareils Defender for Endpoint, Antivirus Microsoft Defender est le logiciel anti-programme malveillant actif ou non.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-205">Configure Security intelligence updates on the Defender for Endpoint devices whether Microsoft Defender Antivirus is the active antimalware or not.</span></span> <span data-ttu-id="fa0dc-206">Pour plus d’informations, [voir Gérer Antivirus Microsoft Defender mises à jour et appliquer les lignes de base.](/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-206">For more information, see [Manage Microsoft Defender Antivirus updates and apply baselines](/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus).</span></span>

<span data-ttu-id="fa0dc-207">Lorsque Antivirus Microsoft Defender n’est pas le logiciel anti-programme malveillant actif dans votre organisation et que vous utilisez le service Defender pour point de terminaison, Antivirus Microsoft Defender passe en mode passif.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-207">When Microsoft Defender Antivirus isn't the active antimalware in your organization and you use the Defender for Endpoint service, Microsoft Defender Antivirus goes on passive mode.</span></span>

<span data-ttu-id="fa0dc-208">Si votre organisation a désactivé la Antivirus Microsoft Defender par le biais d’une stratégie de groupe ou d’autres méthodes, les appareils intégrés doivent être exclus de cette stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-208">If your organization has turned off Microsoft Defender Antivirus through group policy or other methods, devices that are onboarded must be excluded from this group policy.</span></span>

<span data-ttu-id="fa0dc-209">Si vous intégrer des serveurs et que Antivirus Microsoft Defender n’est pas le logiciel anti-programme malveillant actif sur vos serveurs, Antivirus Microsoft Defender doit être configuré pour passer en mode passif ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-209">If you're onboarding servers and Microsoft Defender Antivirus isn't the active antimalware on your servers, Microsoft Defender Antivirus will either need to be configured to go on passive mode or uninstalled.</span></span> <span data-ttu-id="fa0dc-210">La configuration dépend de la version du serveur.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-210">The configuration is dependent on the server version.</span></span> <span data-ttu-id="fa0dc-211">Pour plus d’informations, [voir Antivirus Microsoft Defender compatibilité.](/security/defender-endpoint/microsoft-defender-antivirus-compatibility)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-211">For more information, see [Microsoft Defender Antivirus compatibility](/security/defender-endpoint/microsoft-defender-antivirus-compatibility).</span></span>

> [!NOTE]
> <span data-ttu-id="fa0dc-212">Votre stratégie de groupe normale ne s’applique pas à la protection contre les falsifications et les modifications apportées aux paramètres Antivirus Microsoft Defender sont ignorées lorsque la protection contre la falsification est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-212">Your regular group policy doesn't apply to Tamper Protection, and changes to Microsoft Defender Antivirus settings will be ignored when Tamper Protection is on.</span></span>


## <a name="microsoft-defender-antivirus-early-launch-antimalware-elam-driver-is-enabled"></a><span data-ttu-id="fa0dc-213">Antivirus Microsoft Defender Le pilote ELAM (Anti-programme malveillant à lancement précoce) est activé</span><span class="sxs-lookup"><span data-stu-id="fa0dc-213">Microsoft Defender Antivirus Early Launch Antimalware (ELAM) driver is enabled</span></span>

<span data-ttu-id="fa0dc-214">Si vous exécutez Antivirus Microsoft Defender en tant que produit anti-programme malveillant principal sur vos appareils, l’agent Defender pour Endpoint est correctement intégré.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-214">If you're running Microsoft Defender Antivirus as the primary antimalware product on your devices, the Defender for Endpoint agent will successfully onboard.</span></span>

<span data-ttu-id="fa0dc-215">Si vous exécutez un client anti-programme malveillant tiers et que vous utilisez des solutions de gestion des périphériques mobiles ou des Microsoft Endpoint Manager (branche actuelle), vous devez vous assurer que le pilote ELAM Antivirus Microsoft Defender est activé.</span><span class="sxs-lookup"><span data-stu-id="fa0dc-215">If you're running a third-party antimalware client and use Mobile Device Management solutions or Microsoft Endpoint Manager (current branch), you'll need to ensure the Microsoft Defender Antivirus ELAM driver is enabled.</span></span> <span data-ttu-id="fa0dc-216">Pour plus d’informations, [voir s’assurer Antivirus Microsoft Defender n’est pas désactivé par la stratégie.](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)</span><span class="sxs-lookup"><span data-stu-id="fa0dc-216">For more information, see [Ensure that Microsoft Defender Antivirus is not disabled by policy](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy).</span></span>


## <a name="related-topics"></a><span data-ttu-id="fa0dc-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa0dc-217">Related topics</span></span>

- [<span data-ttu-id="fa0dc-218">Configurer Microsoft Defender pour le déploiement de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa0dc-218">Set up Microsoft Defender for Endpoint deployment</span></span>](production-deployment.md)
- [<span data-ttu-id="fa0dc-219">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="fa0dc-219">Onboard devices</span></span>](onboard-configure.md)
