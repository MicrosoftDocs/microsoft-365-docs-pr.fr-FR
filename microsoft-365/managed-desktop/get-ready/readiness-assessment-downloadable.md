---
title: Téléchargeable readiness assessment checker
description: Vérifie les paramètres du périphérique et du réseau, y compris les points de terminaison requis
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 2080b2fc924320f38d9972c82c0425fa1d8026e7
ms.sourcegitcommit: 7ecd10b302b3b3dfa4ba3be3a6986dd3c189fbff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "49921970"
---
# <a name="downloadable-readiness-assessment-checker"></a><span data-ttu-id="9772a-104">Téléchargeable readiness assessment checker</span><span class="sxs-lookup"><span data-stu-id="9772a-104">Downloadable readiness assessment checker</span></span>

<span data-ttu-id="9772a-105">Pour fonctionner avec le Bureau géré Microsoft, les appareils doivent répondre à certaines exigences en matière de matériel et de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9772a-105">To work well with Microsoft Managed Desktop, devices must meet certain requirements for hardware and settings.</span></span> <span data-ttu-id="9772a-106">En outre, chaque appareil doit être en mesure d’atteindre les points de terminaison clés.</span><span class="sxs-lookup"><span data-stu-id="9772a-106">Also, each device must be able to reach key endpoints.</span></span> <span data-ttu-id="9772a-107">Téléchargez et exécutez cet outil pour obtenir un rapport HTML, afficher les résultats, puis prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="9772a-107">Download and run this tool to obtain an HTML report, view results, and then take action.</span></span> <span data-ttu-id="9772a-108">Vous devrez télécharger l’outil et les fichiers de prise en charge, puis l’exécuter manuellement sur chaque appareil que vous souhaitez inscrire dans Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9772a-108">You will need to download the tool and supporting files, and then run it manually on each device you want to enroll in Microsoft Managed Desktop.</span></span>

<span data-ttu-id="9772a-109">Pour chaque vérification, l’outil signalera l’un des trois résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="9772a-109">For each check, the tool will report one of three possible results:</span></span>


|<span data-ttu-id="9772a-110">Résultat</span><span class="sxs-lookup"><span data-stu-id="9772a-110">Result</span></span>  |<span data-ttu-id="9772a-111">Signification</span><span class="sxs-lookup"><span data-stu-id="9772a-111">Meaning</span></span>  |
|---------|---------|
|<span data-ttu-id="9772a-112">Prêt</span><span class="sxs-lookup"><span data-stu-id="9772a-112">Ready</span></span>     | <span data-ttu-id="9772a-113">Aucune action n’est requise avant de terminer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="9772a-113">No action is required before you complete enrollment.</span></span>        |
|<span data-ttu-id="9772a-114">Avis</span><span class="sxs-lookup"><span data-stu-id="9772a-114">Advisory</span></span>    | <span data-ttu-id="9772a-115">Suivez les étapes de l’outil pour une expérience de l’inscription et pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9772a-115">Follow the steps in the tool for the best experience with enrollment and for users.</span></span> <span data-ttu-id="9772a-116">Vous *pouvez terminer* l’inscription, mais vous devez résoudre ces problèmes avant de déployer votre premier appareil.</span><span class="sxs-lookup"><span data-stu-id="9772a-116">You *can* complete enrollment, but you must fix these issues before you deploy your first device.</span></span>        |
|<span data-ttu-id="9772a-117">Non prêt</span><span class="sxs-lookup"><span data-stu-id="9772a-117">Not ready</span></span> | <span data-ttu-id="9772a-118">*L’inscription échoue* si vous ne corrigez pas ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="9772a-118">*Enrollment will fail* if you don't fix these issues.</span></span> <span data-ttu-id="9772a-119">Suivez les étapes de l’outil pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="9772a-119">Follow the steps in the tool to resolve them.</span></span>        |

## <a name="obtain-the-checker"></a><span data-ttu-id="9772a-120">Obtenir le coche</span><span class="sxs-lookup"><span data-stu-id="9772a-120">Obtain the checker</span></span>

<span data-ttu-id="9772a-121">Téléchargez le fichier .zip à partir https://aka.ms/mmddratoolv0 de .</span><span class="sxs-lookup"><span data-stu-id="9772a-121">Download the .zip file from https://aka.ms/mmddratoolv0.</span></span>

> [!NOTE]
> <span data-ttu-id="9772a-122">L’utilisateur qui exécute l’outil doit avoir des droits d’administrateur local sur l’appareil sur lequel il l’exécute.</span><span class="sxs-lookup"><span data-stu-id="9772a-122">The user running the tool must have local Administrator rights on the device where they're running it.</span></span>

 <span data-ttu-id="9772a-123">Exécutez ensuite l’outil en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9772a-123">Then run the tool by following these steps:</span></span>

1. <span data-ttu-id="9772a-124">Copiez le fichier .zip téléchargé sur chaque appareil que vous souhaitez vérifier.</span><span class="sxs-lookup"><span data-stu-id="9772a-124">Copy the downloaded .zip file to each device you want to check.</span></span>
2. <span data-ttu-id="9772a-125">Extrayez tous les fichiers dans le téléchargement compressé.</span><span class="sxs-lookup"><span data-stu-id="9772a-125">Extract all files in the compressed download.</span></span>
3. <span data-ttu-id="9772a-126">Exécutez **Microsoft.MMD.DeviceReadinessAssessmentTool.exe**.</span><span class="sxs-lookup"><span data-stu-id="9772a-126">Run **Microsoft.MMD.DeviceReadinessAssessmentTool.exe**.</span></span>
4. <span data-ttu-id="9772a-127">Lorsque l’invite de contrôle d’accès utilisateur s’affiche, **sélectionnez Oui**.</span><span class="sxs-lookup"><span data-stu-id="9772a-127">When the User Access Control prompt appears, select **Yes**.</span></span> <span data-ttu-id="9772a-128">L’outil s’exécute et ouvre un rapport dans votre navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9772a-128">The tool runs and opens a report in your default browser.</span></span>

<span data-ttu-id="9772a-129">Vous pouvez également télécharger et extraire l’archive  .zip vers un emplacement partagé, accéder auxMicrosoft.MMD.DeviceReadinessAssessmentTool.exeà partir de chaque appareil, puis l’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="9772a-129">You could also download and extract the .zip archive to a shared location, access **Microsoft.MMD.DeviceReadinessAssessmentTool.exe** from each device, and then run it locally.</span></span>


## <a name="checks"></a><span data-ttu-id="9772a-130">Vérifications</span><span class="sxs-lookup"><span data-stu-id="9772a-130">Checks</span></span>

<span data-ttu-id="9772a-131">L’outil téléchargeable vérifie les éléments liés à l’appareil et au réseau :</span><span class="sxs-lookup"><span data-stu-id="9772a-131">The downloadable tool checks these device- and network-related items:</span></span>

### <a name="hardware"></a><span data-ttu-id="9772a-132">Matériel</span><span class="sxs-lookup"><span data-stu-id="9772a-132">Hardware</span></span>

<span data-ttu-id="9772a-133">Les appareils doivent répondre à des exigences matérielles spécifiques pour fonctionner avec le Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9772a-133">Devices must meet specific hardware requirements to work with Microsoft Managed Desktop.</span></span> <span data-ttu-id="9772a-134">Actuellement, seuls des [appareils approuvés spécifiques](../service-description/device-list.md) sont autorisés à s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="9772a-134">Currently, only specific [approved devices](../service-description/device-list.md) are allowed to enroll.</span></span> 

<span data-ttu-id="9772a-135">Si votre appareil échoue à l’une des vérifications, il n’est pas compatible avec bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9772a-135">If your device fails any of the checks, it's not compatible with Microsoft Managed Desktop.</span></span>

### <a name="network-endpoints"></a><span data-ttu-id="9772a-136">Points de terminaison réseau</span><span class="sxs-lookup"><span data-stu-id="9772a-136">Network endpoints</span></span>

<span data-ttu-id="9772a-137">Les appareils sont en grande partie en mesure d’atteindre plusieurs [points de terminaison clés](network.md) pour fonctionner avec bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9772a-137">Devices much be able to reach several [key endpoints](network.md) to work with Microsoft Managed Desktop.</span></span>

<span data-ttu-id="9772a-138">Si l’outil **signale** un résultat non prêt, consultez le rapport détaillé pour savoir quels points de terminaison n’ont pas été accessibles.</span><span class="sxs-lookup"><span data-stu-id="9772a-138">If the tool reports a **Not ready** result, see the detailed report to find out which endpoints weren't reachable.</span></span> <span data-ttu-id="9772a-139">Ajustez ensuite votre pare-feu ou d’autres paramètres réseau pour vous assurer que ces points de terminaison sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="9772a-139">Then adjust your firewall or other network settings to ensure those endpoints can be reached.</span></span>

### <a name="other-settings"></a><span data-ttu-id="9772a-140">Autres paramètres</span><span class="sxs-lookup"><span data-stu-id="9772a-140">Other settings</span></span>

#### <a name="enterprise-wi-fi-profiles"></a><span data-ttu-id="9772a-141">Profils Wi-Fi d’entreprise</span><span class="sxs-lookup"><span data-stu-id="9772a-141">Enterprise wi-fi profiles</span></span>

<span data-ttu-id="9772a-142">Un **résultat d’avis** signifie que vous utilisez certains profils wi-fi qui ont besoin de certificats et de profils pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="9772a-142">An **Advisory** result means that you are using some wi-fi profiles that need certificates and profiles to work properly.</span></span> <span data-ttu-id="9772a-143">Pour plus d’informations, voir Déployer des certificats et profil [Wi-Fi/VPN.](certs-wifi-lan.md#deploy-certificates-and-wi-fivpn-profile)</span><span class="sxs-lookup"><span data-stu-id="9772a-143">For more information, see [Deploy certificates and Wi-Fi/VPN profile](certs-wifi-lan.md#deploy-certificates-and-wi-fivpn-profile).</span></span>

#### <a name="lan-profiles"></a><span data-ttu-id="9772a-144">Profils LAN</span><span class="sxs-lookup"><span data-stu-id="9772a-144">LAN profiles</span></span>

<span data-ttu-id="9772a-145">Un **résultat d’avis** signifie que vous avez des lans qui ont besoin de certificats et de profils pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="9772a-145">An **Advisory** result means that you have LANs that need certificates and profiles to work properly.</span></span> <span data-ttu-id="9772a-146">Pour plus d’informations, voir [Préparer les certificats et les profils réseau pour bureau géré Microsoft.](certs-wifi-lan.md)</span><span class="sxs-lookup"><span data-stu-id="9772a-146">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>

#### <a name="vpn-profiles"></a><span data-ttu-id="9772a-147">Profils VPN</span><span class="sxs-lookup"><span data-stu-id="9772a-147">VPN profiles</span></span>

<span data-ttu-id="9772a-148">Un **résultat d’avis** signifie que vous utilisez un réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="9772a-148">An **Advisory** result means that you're using a virtual private network (VPN).</span></span> <span data-ttu-id="9772a-149">Créez un profil VPN qui déploie des certificats intégrés à Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="9772a-149">Create a VPN profile that deploys certificates integrated with Microsoft Intune.</span></span> <span data-ttu-id="9772a-150">Pour plus d’informations, voir [Préparer les certificats et les profils réseau pour bureau géré Microsoft.](certs-wifi-lan.md)</span><span class="sxs-lookup"><span data-stu-id="9772a-150">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>

#### <a name="mapped-drives"></a><span data-ttu-id="9772a-151">Lecteurs mappés</span><span class="sxs-lookup"><span data-stu-id="9772a-151">Mapped drives</span></span>

<span data-ttu-id="9772a-152">Un **résultat d’avis** signifie que vous avez des lecteurs mappés, ce qui n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="9772a-152">An **Advisory** result means that you have some mapped drives, which aren't recommended.</span></span> <span data-ttu-id="9772a-153">Pour plus d’informations, voir [Préparer les lecteurs mappés pour le Bureau géré Microsoft.](mapped-drives.md)</span><span class="sxs-lookup"><span data-stu-id="9772a-153">For more information, see [Prepare mapped drives for Microsoft Managed Desktop](mapped-drives.md).</span></span>

#### <a name="print-queues"></a><span data-ttu-id="9772a-154">Imprimer les files d’attente</span><span class="sxs-lookup"><span data-stu-id="9772a-154">Print queues</span></span>

<span data-ttu-id="9772a-155">Un **résultat d’avis** signifie que vous avez des files d’attente d’impression en attente, ce qui n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="9772a-155">An **Advisory** result means that you have some outstanding print queues, which aren't recommended.</span></span> <span data-ttu-id="9772a-156">Une solution consiste à utiliser l’impression cloud.</span><span class="sxs-lookup"><span data-stu-id="9772a-156">One solution is to use cloud printing.</span></span> <span data-ttu-id="9772a-157">Pour plus d’informations, voir [Préparer les ressources d’impression pour le Bureau géré Microsoft.](printing.md)</span><span class="sxs-lookup"><span data-stu-id="9772a-157">For more information, see [Prepare printing resources for Microsoft Managed Desktop](printing.md).</span></span>

#### <a name="proxies"></a><span data-ttu-id="9772a-158">Proxies</span><span class="sxs-lookup"><span data-stu-id="9772a-158">Proxies</span></span>

<span data-ttu-id="9772a-159">Un **résultat d’avis** signifie que vous avez un serveur proxy en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9772a-159">An **Advisory** result means that you have a proxy server in use.</span></span> <span data-ttu-id="9772a-160">Pour plus d’informations, [voir Configuration réseau pour bureau géré Microsoft.](network.md)</span><span class="sxs-lookup"><span data-stu-id="9772a-160">For more information, see [Network configuration for Microsoft Managed Desktop](network.md).</span></span>

