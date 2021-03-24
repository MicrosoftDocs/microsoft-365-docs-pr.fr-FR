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
ms.openlocfilehash: 7581c606a7903bd6d32c1e192f35992899289f30
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51061398"
---
# <a name="minimum-requirements-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="8255e-104">Conditions minimales requises pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8255e-104">Minimum requirements for Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="8255e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8255e-105">**Applies to:**</span></span>
- [<span data-ttu-id="8255e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8255e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="8255e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8255e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="8255e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8255e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8255e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8255e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="8255e-110">Certaines conditions minimales sont requises pour l’intégration d’appareils au service.</span><span class="sxs-lookup"><span data-stu-id="8255e-110">There are some minimum requirements for onboarding devices to the service.</span></span> <span data-ttu-id="8255e-111">Découvrez les licences, la configuration matérielle et logicielle requise et d’autres paramètres de configuration pour intégrer des appareils au service.</span><span class="sxs-lookup"><span data-stu-id="8255e-111">Learn about the licensing, hardware and software requirements, and other configuration settings to onboard devices to the service.</span></span>

> <span data-ttu-id="8255e-112">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8255e-112">Want to experience Microsoft Defender for Endpoint?</span></span> <span data-ttu-id="8255e-113">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-minreqs-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="8255e-113">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-minreqs-abovefoldlink).</span></span>

> [!TIP]
> - <span data-ttu-id="8255e-114">Découvrez les dernières améliorations apportées à Defender for Endpoint : [Defender for Endpoint Tech Community](https://techcommunity.microsoft.com/t5/Windows-Defender-Advanced-Threat/ct-p/WindowsDefenderAdvanced).</span><span class="sxs-lookup"><span data-stu-id="8255e-114">Learn about the latest enhancements in Defender for Endpoint: [Defender for Endpoint Tech Community](https://techcommunity.microsoft.com/t5/Windows-Defender-Advanced-Threat/ct-p/WindowsDefenderAdvanced).</span></span>
> - <span data-ttu-id="8255e-115">Defender pour le point de terminaison a démontré les fonctionnalités d’optique et de détection de pointe du secteur dans l’évaluation MITRE récente.</span><span class="sxs-lookup"><span data-stu-id="8255e-115">Defender for Endpoint demonstrated industry-leading optics and detection capabilities in the recent MITRE evaluation.</span></span> <span data-ttu-id="8255e-116">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span><span class="sxs-lookup"><span data-stu-id="8255e-116">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="8255e-117">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="8255e-117">Licensing requirements</span></span>
<span data-ttu-id="8255e-118">Microsoft Defender for Endpoint nécessite l’une des offres de licence en volume Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="8255e-118">Microsoft Defender for Endpoint requires one of the following Microsoft volume licensing offers:</span></span>

- <span data-ttu-id="8255e-119">Windows 10 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="8255e-119">Windows 10 Enterprise E5</span></span>
- <span data-ttu-id="8255e-120">Windows 10 Éducation A5</span><span class="sxs-lookup"><span data-stu-id="8255e-120">Windows 10 Education A5</span></span>
- <span data-ttu-id="8255e-121">Microsoft 365 E5 (M365 E5) qui inclut Windows 10 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="8255e-121">Microsoft 365 E5 (M365 E5) which includes Windows 10 Enterprise E5</span></span>
- <span data-ttu-id="8255e-122">Microsoft 365 A5 (M365 A5)</span><span class="sxs-lookup"><span data-stu-id="8255e-122">Microsoft 365 A5 (M365 A5)</span></span>
- <span data-ttu-id="8255e-123">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="8255e-123">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="8255e-124">Sécurité Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="8255e-124">Microsoft 365 A5 Security</span></span>
- <span data-ttu-id="8255e-125">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8255e-125">Microsoft Defender for Endpoint</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-126">Les utilisateurs titulaires d’une licence éligible peuvent utiliser Microsoft Defender pour endpoint sur cinq appareils simultanés au plus.</span><span class="sxs-lookup"><span data-stu-id="8255e-126">Eligible licensed users may use Microsoft Defender for Endpoint on up to five concurrent devices.</span></span>
> <span data-ttu-id="8255e-127">Microsoft Defender for Endpoint est également disponible à l’achat auprès d’un fournisseur de solutions Cloud (CSP).</span><span class="sxs-lookup"><span data-stu-id="8255e-127">Microsoft Defender for Endpoint is also available for purchase from a Cloud Solution Provider (CSP).</span></span>

<span data-ttu-id="8255e-128">Microsoft Defender pour le point de terminaison pour les serveurs nécessite l’une des options de licence suivantes :</span><span class="sxs-lookup"><span data-stu-id="8255e-128">Microsoft Defender for Endpoint for servers requires one of the following licensing options:</span></span>

- [<span data-ttu-id="8255e-129">Centre de sécurité Azure avec Azure Defender activé</span><span class="sxs-lookup"><span data-stu-id="8255e-129">Azure Security Center with Azure Defender enabled</span></span>](https://docs.microsoft.com/azure/security-center/security-center-pricing)
- <span data-ttu-id="8255e-130">Microsoft Defender for Endpoint for Server (un par serveur couvert)</span><span class="sxs-lookup"><span data-stu-id="8255e-130">Microsoft Defender for Endpoint for Server (one per covered server)</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-131">Les clients peuvent acquérir des licences serveur (une par environnement de système d’exploitation de serveur couvert) pour Microsoft Defender pour Endpoint for Servers s’ils ont un minimum combiné de 50 licences pour une ou plusieurs des licences utilisateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="8255e-131">Customers may acquire server licenses (one per covered server Operating System Environment (OSE)) for Microsoft Defender for Endpoint for Servers if they have a combined minimum of 50 licenses for one or more of the following user licenses:</span></span>
>
> * <span data-ttu-id="8255e-132">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8255e-132">Microsoft Defender for Endpoint</span></span>
> * <span data-ttu-id="8255e-133">Windows E5/A5</span><span class="sxs-lookup"><span data-stu-id="8255e-133">Windows E5/A5</span></span>
> * <span data-ttu-id="8255e-134">Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="8255e-134">Microsoft 365 E5/A5</span></span>
> * <span data-ttu-id="8255e-135">Sécurité Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="8255e-135">Microsoft 365 E5/A5 Security</span></span>

<span data-ttu-id="8255e-136">Pour obtenir des informations détaillées sur les licences, consultez le [site](https://www.microsoft.com/licensing/terms/) Termes du produit et travaillez avec votre équipe de compte pour en savoir plus sur les conditions générales.</span><span class="sxs-lookup"><span data-stu-id="8255e-136">For detailed licensing information, see the [Product Terms site](https://www.microsoft.com/licensing/terms/) and work with your account team to learn more about the terms and conditions.</span></span>

<span data-ttu-id="8255e-137">Pour plus d’informations sur le tableau des fonctionnalités des éditions de Windows 10, voir [Comparer les éditions de Windows 10.](https://www.microsoft.com/windowsforbusiness/compare)</span><span class="sxs-lookup"><span data-stu-id="8255e-137">For more information on the array of features in Windows 10 editions, see [Compare Windows 10 editions](https://www.microsoft.com/windowsforbusiness/compare).</span></span>

<span data-ttu-id="8255e-138">Pour obtenir un tableau de comparaison détaillé de la comparaison des éditions commerciales de Windows 10, consultez la comparaison [PDF](https://wfbdevicemanagementprod.blob.core.windows.net/windowsforbusiness/Windows10_CommercialEdition_Comparison.pdf).</span><span class="sxs-lookup"><span data-stu-id="8255e-138">For a detailed comparison table of Windows 10 commercial edition comparison, see the [comparison PDF](https://wfbdevicemanagementprod.blob.core.windows.net/windowsforbusiness/Windows10_CommercialEdition_Comparison.pdf).</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="8255e-139">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="8255e-139">Browser requirements</span></span>
<span data-ttu-id="8255e-140">L’accès à Defender pour le point de terminaison s’fait par le biais d’un navigateur, qui permet de prendre en charge les navigateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8255e-140">Access to Defender for Endpoint is done through a browser, supporting the following browsers:</span></span>

- <span data-ttu-id="8255e-141">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8255e-141">Microsoft Edge</span></span>
- <span data-ttu-id="8255e-142">Internet Explorer version 11</span><span class="sxs-lookup"><span data-stu-id="8255e-142">Internet Explorer version 11</span></span>
- <span data-ttu-id="8255e-143">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="8255e-143">Google Chrome</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-144">Bien que d’autres navigateurs fonctionnent, les navigateurs mentionnés sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8255e-144">While other browsers might work, the mentioned browsers are the ones supported.</span></span>


## <a name="hardware-and-software-requirements"></a><span data-ttu-id="8255e-145">Configuration matérielle et logicielle requise</span><span class="sxs-lookup"><span data-stu-id="8255e-145">Hardware and software requirements</span></span>

### <a name="supported-windows-versions"></a><span data-ttu-id="8255e-146">Versions de Windows prise en charge</span><span class="sxs-lookup"><span data-stu-id="8255e-146">Supported Windows versions</span></span>
- <span data-ttu-id="8255e-147">Windows 7 SP1 Entreprise ([Nécessite ESU pour la prise en charge](https://docs.microsoft.com/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span><span class="sxs-lookup"><span data-stu-id="8255e-147">Windows 7 SP1 Enterprise ([Requires ESU for support](https://docs.microsoft.com/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span></span>
- <span data-ttu-id="8255e-148">Windows 7 SP1 Professionnel ([Nécessite ESU pour la prise en charge](https://docs.microsoft.com/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span><span class="sxs-lookup"><span data-stu-id="8255e-148">Windows 7 SP1 Pro ([Requires ESU for support](https://docs.microsoft.com/troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq).)</span></span>
- <span data-ttu-id="8255e-149">Windows 8.1 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8255e-149">Windows 8.1 Enterprise</span></span>
- <span data-ttu-id="8255e-150">Windows 8.1 Professionnel</span><span class="sxs-lookup"><span data-stu-id="8255e-150">Windows 8.1 Pro</span></span>
- <span data-ttu-id="8255e-151">Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8255e-151">Windows 10 Enterprise</span></span>
- [<span data-ttu-id="8255e-152">Windows 10 Entreprise LTSC</span><span class="sxs-lookup"><span data-stu-id="8255e-152">Windows 10 Enterprise LTSC</span></span>](https://docs.microsoft.com/windows/whats-new/ltsc/)
- <span data-ttu-id="8255e-153">Windows 10 Éducation</span><span class="sxs-lookup"><span data-stu-id="8255e-153">Windows 10 Education</span></span>
- <span data-ttu-id="8255e-154">Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="8255e-154">Windows 10 Pro</span></span>
- <span data-ttu-id="8255e-155">Windows 10 Professionnel Éducation</span><span class="sxs-lookup"><span data-stu-id="8255e-155">Windows 10 Pro Education</span></span>
- <span data-ttu-id="8255e-156">Serveur Windows</span><span class="sxs-lookup"><span data-stu-id="8255e-156">Windows server</span></span>
  - <span data-ttu-id="8255e-157">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="8255e-157">Windows Server 2008 R2 SP1</span></span>
  - <span data-ttu-id="8255e-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8255e-158">Windows Server 2012 R2</span></span>
  - <span data-ttu-id="8255e-159">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8255e-159">Windows Server 2016</span></span>
  - <span data-ttu-id="8255e-160">Windows Server, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8255e-160">Windows Server, version 1803 or later</span></span>
  - <span data-ttu-id="8255e-161">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="8255e-161">Windows Server 2019</span></span>
- <span data-ttu-id="8255e-162">Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="8255e-162">Windows Virtual Desktop</span></span>

<span data-ttu-id="8255e-163">Les appareils de votre réseau doivent être en cours d’exécution dans l’une de ces éditions.</span><span class="sxs-lookup"><span data-stu-id="8255e-163">Devices on your network must be running one of these editions.</span></span>

<span data-ttu-id="8255e-164">La configuration matérielle requise pour Defender pour Endpoint sur les appareils est la même pour les éditions pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8255e-164">The hardware requirements for Defender for Endpoint on devices are the same for the supported editions.</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-165">Les ordinateurs exécutant des versions mobiles de Windows (comme Windows CE et Windows 10 Mobile) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8255e-165">Machines running mobile versions of Windows (such as Windows CE and Windows 10 Mobile) are not supported.</span></span>
>
> <span data-ttu-id="8255e-166">Les ordinateurs virtuels exécutant Windows 10 Entreprise 2016 LTSB peuvent rencontrer des problèmes de performances s’ils sont exécutés sur des plateformes de virtualisation autres que Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8255e-166">Virtual Machines running Windows 10 Enterprise 2016 LTSB may encounter performance issues if run on non-Microsoft virtualization platforms.</span></span>
>
> <span data-ttu-id="8255e-167">Pour les environnements virtuels, nous vous recommandons d’utiliser Windows 10 Entreprise LTSC 2019 ou une édition ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8255e-167">For virtual environments, we recommend using Windows 10 Enterprise LTSC 2019 or later.</span></span>


### <a name="other-supported-operating-systems"></a><span data-ttu-id="8255e-168">Autres systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="8255e-168">Other supported operating systems</span></span>
- <span data-ttu-id="8255e-169">Android</span><span class="sxs-lookup"><span data-stu-id="8255e-169">Android</span></span>
- <span data-ttu-id="8255e-170">Linux</span><span class="sxs-lookup"><span data-stu-id="8255e-170">Linux</span></span>
- <span data-ttu-id="8255e-171">macOS</span><span class="sxs-lookup"><span data-stu-id="8255e-171">macOS</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-172">Vous devez connaître les distributions linux exactes et les versions d’Android et de macOS compatibles avec Defender for Endpoint pour que l’intégration fonctionne.</span><span class="sxs-lookup"><span data-stu-id="8255e-172">You'll need to know the exact Linux distributions and versions of Android and macOS that are compatible with Defender for Endpoint for the integration to work.</span></span>



### <a name="network-and-data-storage-and-configuration-requirements"></a><span data-ttu-id="8255e-173">Configuration requise pour le stockage réseau et les données</span><span class="sxs-lookup"><span data-stu-id="8255e-173">Network and data storage and configuration requirements</span></span>
<span data-ttu-id="8255e-174">Lorsque vous exécutez l’Assistant d’intégration pour la première fois, vous devez choisir l’endroit où sont stockées vos informations relatives au point de terminaison Microsoft Defender : dans l’Union européenne, le Royaume-Uni ou le centre de données des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="8255e-174">When you run the onboarding wizard for the first time, you must choose where your Microsoft Defender for Endpoint-related information is stored: in the European Union, the United Kingdom, or the United States datacenter.</span></span>

> [!NOTE]
> - <span data-ttu-id="8255e-175">Vous ne pouvez pas modifier votre emplacement de stockage de données après la première installation.</span><span class="sxs-lookup"><span data-stu-id="8255e-175">You cannot change your data storage location after the first-time setup.</span></span>
> - <span data-ttu-id="8255e-176">Pour plus d’informations sur l’endroit et la façon dont Microsoft stocke vos données, voir Microsoft Defender for [Endpoint data storage and privacy.](data-storage-privacy.md)</span><span class="sxs-lookup"><span data-stu-id="8255e-176">Review the [Microsoft Defender for Endpoint data storage and privacy](data-storage-privacy.md) for more information on where and how Microsoft stores your data.</span></span>


### <a name="diagnostic-data-settings"></a><span data-ttu-id="8255e-177">Paramètres des données de diagnostic</span><span class="sxs-lookup"><span data-stu-id="8255e-177">Diagnostic data settings</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-178">Microsoft Defender pour le point de terminaison ne requiert aucun niveau de diagnostic spécifique tant qu’il est activé.</span><span class="sxs-lookup"><span data-stu-id="8255e-178">Microsoft Defender for Endpoint doesn't require any specific diagnostic level as long as it's enabled.</span></span>

<span data-ttu-id="8255e-179">Assurez-vous que le service de données de diagnostic est activé sur tous les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8255e-179">Make sure that the diagnostic data service is enabled on all the devices in your organization.</span></span>
<span data-ttu-id="8255e-180">Par défaut, ce service est activé.</span><span class="sxs-lookup"><span data-stu-id="8255e-180">By default, this service is enabled.</span></span> <span data-ttu-id="8255e-181">Il est bon de vérifier que vous obtenez des données de capteur à partir de ces données.</span><span class="sxs-lookup"><span data-stu-id="8255e-181">It's good practice to check to ensure that you'll get sensor data from them.</span></span>

<span data-ttu-id="8255e-182">Utilisez la ligne de commande pour vérifier le type de démarrage du service de données de **diagnostic Windows 10**:</span><span class="sxs-lookup"><span data-stu-id="8255e-182">**Use the command line to check the Windows 10 diagnostic data service startup type**:</span></span>

1. <span data-ttu-id="8255e-183">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="8255e-183">Open an elevated command-line prompt on the device:</span></span>

   1.  <span data-ttu-id="8255e-184">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="8255e-184">Go to **Start** and type **cmd**.</span></span>

   1.  <span data-ttu-id="8255e-185">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="8255e-185">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="8255e-186">Entrez la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="8255e-186">Enter the following command, and press **Enter**:</span></span>

   ```console
   sc qc diagtrack
   ```

   <span data-ttu-id="8255e-187">Si le service est activé, le résultat doit ressembler à la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="8255e-187">If the service is enabled, then the result should look like the following screenshot:</span></span>

   ![Résultat de la commande de requête sc pour diagtrack](images/windefatp-sc-qc-diagtrack.png)


<span data-ttu-id="8255e-189">Vous devez configurer le service pour qu’il démarre automatiquement si la START_TYPE **n’est** pas définie sur **AUTO_START**.</span><span class="sxs-lookup"><span data-stu-id="8255e-189">You'll need to set the service to automatically start if the **START_TYPE** is not set to **AUTO_START**.</span></span>


<span data-ttu-id="8255e-190">**Utilisez la ligne de commande pour configurer le service de données de diagnostic Windows 10 pour démarrer automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="8255e-190">**Use the command line to set the Windows 10 diagnostic data service to automatically start:**</span></span>

1.  <span data-ttu-id="8255e-191">Ouvrez une invite de ligne de commande avec élévation de niveaux sur le point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="8255e-191">Open an elevated command-line prompt on the endpoint:</span></span>

    1. <span data-ttu-id="8255e-192">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="8255e-192">Go to **Start** and type **cmd**.</span></span>

    1. <span data-ttu-id="8255e-193">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="8255e-193">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2.  <span data-ttu-id="8255e-194">Entrez la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="8255e-194">Enter the following command, and press **Enter**:</span></span>

    ```console
    sc config diagtrack start=auto
    ```

3.  <span data-ttu-id="8255e-195">Un message de réussite s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8255e-195">A success message is displayed.</span></span> <span data-ttu-id="8255e-196">Vérifiez la modification en entrant la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="8255e-196">Verify the change by entering the following command, and press **Enter**:</span></span>

    ```console
    sc qc diagtrack
    ```


#### <a name="internet-connectivity"></a><span data-ttu-id="8255e-197">Connexion à Internet</span><span class="sxs-lookup"><span data-stu-id="8255e-197">Internet connectivity</span></span>
<span data-ttu-id="8255e-198">La connectivité Internet sur les appareils est requise directement ou par proxy.</span><span class="sxs-lookup"><span data-stu-id="8255e-198">Internet connectivity on devices is required either directly or through proxy.</span></span>

<span data-ttu-id="8255e-199">Le capteur Defender pour point de terminaison peut utiliser une bande passante moyenne quotidienne de 5 Mo pour communiquer avec le service cloud Defender for Endpoint et signaler les cyber-données.</span><span class="sxs-lookup"><span data-stu-id="8255e-199">The Defender for Endpoint sensor can utilize a daily average bandwidth of 5 MB to communicate with the Defender for Endpoint cloud service and report cyber data.</span></span> <span data-ttu-id="8255e-200">Les activités non limitées, telles que les téléchargements de fichiers et la collecte de packages d’enquête, ne sont pas incluses dans cette bande passante moyenne quotidienne.</span><span class="sxs-lookup"><span data-stu-id="8255e-200">One-off activities such as file uploads and investigation package collection are not included in this daily average bandwidth.</span></span>

<span data-ttu-id="8255e-201">Pour plus d’informations sur les paramètres de configuration de proxy supplémentaires, voir Configurer les [paramètres de proxy d’appareil](configure-proxy-internet.md)et de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="8255e-201">For more information on additional proxy configuration settings, see [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md).</span></span>

<span data-ttu-id="8255e-202">Avant d’intégrer des appareils, le service de données de diagnostic doit être activé.</span><span class="sxs-lookup"><span data-stu-id="8255e-202">Before you onboard devices, the diagnostic data service must be enabled.</span></span> <span data-ttu-id="8255e-203">Le service est activé par défaut dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8255e-203">The service is enabled by default in Windows 10.</span></span>


## <a name="microsoft-defender-antivirus-configuration-requirement"></a><span data-ttu-id="8255e-204">Configuration requise pour l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="8255e-204">Microsoft Defender Antivirus configuration requirement</span></span>
<span data-ttu-id="8255e-205">L’agent Defender for Endpoint dépend de la capacité de l’Antivirus Microsoft Defender à analyser les fichiers et à fournir des informations les concernant.</span><span class="sxs-lookup"><span data-stu-id="8255e-205">The Defender for Endpoint agent depends on the ability of Microsoft Defender Antivirus to scan files and provide information about them.</span></span>

<span data-ttu-id="8255e-206">Configurez les mises à jour d’intelligence de sécurité sur les appareils Defender for Endpoint, que l’Antivirus Microsoft Defender soit ou non le logiciel anti-programme malveillant actif.</span><span class="sxs-lookup"><span data-stu-id="8255e-206">Configure Security intelligence updates on the Defender for Endpoint devices whether Microsoft Defender Antivirus is the active antimalware or not.</span></span> <span data-ttu-id="8255e-207">Pour plus d’informations, voir Gérer les mises à [jour de l’Antivirus Microsoft Defender et appliquer les lignes de base.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="8255e-207">For more information, see [Manage Microsoft Defender Antivirus updates and apply baselines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus).</span></span>

<span data-ttu-id="8255e-208">Lorsque l’Antivirus Microsoft Defender n’est pas le logiciel anti-programme malveillant actif dans votre organisation et que vous utilisez le service Defender pour point de terminaison, l’Antivirus Microsoft Defender passe en mode passif.</span><span class="sxs-lookup"><span data-stu-id="8255e-208">When Microsoft Defender Antivirus is not the active antimalware in your organization and you use the Defender for Endpoint service, Microsoft Defender Antivirus goes on passive mode.</span></span>

<span data-ttu-id="8255e-209">Si votre organisation a désactivé l’Antivirus Microsoft Defender par le biais d’une stratégie de groupe ou d’autres méthodes, les appareils intégrés doivent être exclus de cette stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8255e-209">If your organization has turned off Microsoft Defender Antivirus through group policy or other methods, devices that are onboarded must be excluded from this group policy.</span></span>

<span data-ttu-id="8255e-210">Si vous intégrer des serveurs et que l’Antivirus Microsoft Defender n’est pas le logiciel anti-programme malveillant actif sur vos serveurs, l’Antivirus Microsoft Defender doit être configuré pour passer en mode passif ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="8255e-210">If you are onboarding servers and Microsoft Defender Antivirus is not the active antimalware on your servers, Microsoft Defender Antivirus will either need to be configured to go on passive mode or uninstalled.</span></span> <span data-ttu-id="8255e-211">La configuration dépend de la version du serveur.</span><span class="sxs-lookup"><span data-stu-id="8255e-211">The configuration is dependent on the server version.</span></span> <span data-ttu-id="8255e-212">Pour plus d’informations, [voir Compatibilité de l’Antivirus Microsoft Defender.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="8255e-212">For more information, see [Microsoft Defender Antivirus compatibility](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus-compatibility.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8255e-213">Votre stratégie de groupe normale ne s’applique pas à la Protection contre les falsifications et les modifications apportées aux paramètres de l’Antivirus Microsoft Defender sont ignorées lorsque la protection contre la falsification est en cours.</span><span class="sxs-lookup"><span data-stu-id="8255e-213">Your regular group policy doesn't apply to Tamper Protection, and changes to Microsoft Defender Antivirus settings will be ignored when Tamper Protection is on.</span></span>


## <a name="microsoft-defender-antivirus-early-launch-antimalware-elam-driver-is-enabled"></a><span data-ttu-id="8255e-214">Le pilote ELAM (Logiciel anti-programme malveillant à lancement rapide) de l’Antivirus Microsoft Defender est activé</span><span class="sxs-lookup"><span data-stu-id="8255e-214">Microsoft Defender Antivirus Early Launch Antimalware (ELAM) driver is enabled</span></span>
<span data-ttu-id="8255e-215">Si vous exécutez l’Antivirus Microsoft Defender en tant que produit anti-programme malveillant principal sur vos appareils, l’agent Defender pour Endpoint est correctement intégré.</span><span class="sxs-lookup"><span data-stu-id="8255e-215">If you're running Microsoft Defender Antivirus as the primary antimalware product on your devices, the Defender for Endpoint agent will successfully onboard.</span></span>

<span data-ttu-id="8255e-216">Si vous exécutez un client anti-programme malveillant tiers et utilisez des solutions de gestion des périphériques mobiles ou Microsoft Endpoint Manager (branche actuelle), vous devez vous assurer que le pilote ELAM de l’Antivirus Microsoft Defender est activé.</span><span class="sxs-lookup"><span data-stu-id="8255e-216">If you're running a third-party antimalware client and use Mobile Device Management solutions or Microsoft Endpoint Manager (current branch), you'll need to ensure that the Microsoft Defender Antivirus ELAM driver is enabled.</span></span> <span data-ttu-id="8255e-217">Pour plus d’informations, [voir s’assurer que l’Antivirus Microsoft Defender n’est pas désactivé par la stratégie.](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)</span><span class="sxs-lookup"><span data-stu-id="8255e-217">For more information, see [Ensure that Microsoft Defender Antivirus is not disabled by policy](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy).</span></span>


## <a name="related-topics"></a><span data-ttu-id="8255e-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8255e-218">Related topics</span></span>
- [<span data-ttu-id="8255e-219">Configurer Microsoft Defender pour le déploiement de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8255e-219">Set up Microsoft Defender for Endpoint deployment</span></span>](production-deployment.md)
- [<span data-ttu-id="8255e-220">Appareils intégrés</span><span class="sxs-lookup"><span data-stu-id="8255e-220">Onboard devices</span></span>](onboard-configure.md)
