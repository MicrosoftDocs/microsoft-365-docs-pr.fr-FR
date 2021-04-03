---
title: Vérifier la préparation d’évaluation téléchargeable
description: Vérifie les paramètres du périphérique et du réseau, y compris les points de terminaison requis
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: eec6bdff2e494e0f55b06cb581c5775d3ffeb9e3
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51581033"
---
# <a name="downloadable-readiness-assessment-checker"></a><span data-ttu-id="05bd2-104">Vérifier la préparation d’évaluation téléchargeable</span><span class="sxs-lookup"><span data-stu-id="05bd2-104">Downloadable readiness assessment checker</span></span>

<span data-ttu-id="05bd2-105">Pour fonctionner avec le Bureau géré Microsoft, les appareils doivent répondre à certaines exigences en matière de matériel et de paramètres.</span><span class="sxs-lookup"><span data-stu-id="05bd2-105">To work well with Microsoft Managed Desktop, devices must meet certain requirements for hardware and settings.</span></span> <span data-ttu-id="05bd2-106">En outre, chaque appareil doit être en mesure d’atteindre les points de terminaison clés.</span><span class="sxs-lookup"><span data-stu-id="05bd2-106">Also, each device must be able to reach key endpoints.</span></span> <span data-ttu-id="05bd2-107">Téléchargez et exécutez cet outil pour obtenir un rapport HTML, afficher les résultats, puis prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="05bd2-107">Download and run this tool to obtain an HTML report, view results, and then take action.</span></span> <span data-ttu-id="05bd2-108">Vous devez télécharger l’outil et les fichiers de prise en charge, puis l’exécuter manuellement sur chaque appareil que vous souhaitez inscrire dans Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05bd2-108">You will need to download the tool and supporting files, and then run it manually on each device you want to enroll in Microsoft Managed Desktop.</span></span>

<span data-ttu-id="05bd2-109">Pour chaque vérification, l’outil signalera l’un des trois résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="05bd2-109">For each check, the tool will report one of three possible results:</span></span>


|<span data-ttu-id="05bd2-110">Résultat</span><span class="sxs-lookup"><span data-stu-id="05bd2-110">Result</span></span>  |<span data-ttu-id="05bd2-111">Signification</span><span class="sxs-lookup"><span data-stu-id="05bd2-111">Meaning</span></span>  |
|---------|---------|
|<span data-ttu-id="05bd2-112">Prêt</span><span class="sxs-lookup"><span data-stu-id="05bd2-112">Ready</span></span>     | <span data-ttu-id="05bd2-113">Aucune action n’est requise avant de terminer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="05bd2-113">No action is required before you complete enrollment.</span></span>        |
|<span data-ttu-id="05bd2-114">Avertissement</span><span class="sxs-lookup"><span data-stu-id="05bd2-114">Advisory</span></span>    | <span data-ttu-id="05bd2-115">Suivez les étapes de l’outil pour une expérience de l’inscription et pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05bd2-115">Follow the steps in the tool for the best experience with enrollment and for users.</span></span> <span data-ttu-id="05bd2-116">Vous *pouvez terminer* l’inscription, mais vous devez résoudre ces problèmes avant de déployer votre premier appareil.</span><span class="sxs-lookup"><span data-stu-id="05bd2-116">You *can* complete enrollment, but you must fix these issues before you deploy your first device.</span></span>        |
|<span data-ttu-id="05bd2-117">Non prêt</span><span class="sxs-lookup"><span data-stu-id="05bd2-117">Not ready</span></span> | <span data-ttu-id="05bd2-118">*L’inscription échoue* si vous ne corrigez pas ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="05bd2-118">*Enrollment will fail* if you don't fix these issues.</span></span> <span data-ttu-id="05bd2-119">Suivez les étapes de l’outil pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="05bd2-119">Follow the steps in the tool to resolve them.</span></span>        |

## <a name="obtain-the-checker"></a><span data-ttu-id="05bd2-120">Obtenir le coche</span><span class="sxs-lookup"><span data-stu-id="05bd2-120">Obtain the checker</span></span>

<span data-ttu-id="05bd2-121">Téléchargez le fichier .zip à partir https://aka.ms/mmddratoolv0 de .</span><span class="sxs-lookup"><span data-stu-id="05bd2-121">Download the .zip file from https://aka.ms/mmddratoolv0.</span></span>

> [!NOTE]
> <span data-ttu-id="05bd2-122">L’utilisateur qui exécute l’outil doit avoir des droits d’administrateur local sur l’appareil sur lequel il l’exécute.</span><span class="sxs-lookup"><span data-stu-id="05bd2-122">The user running the tool must have local Administrator rights on the device where they're running it.</span></span>

 <span data-ttu-id="05bd2-123">Exécutez ensuite l’outil en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="05bd2-123">Then run the tool by following these steps:</span></span>

1. <span data-ttu-id="05bd2-124">Copiez le fichier .zip téléchargé sur chaque appareil que vous souhaitez vérifier.</span><span class="sxs-lookup"><span data-stu-id="05bd2-124">Copy the downloaded .zip file to each device you want to check.</span></span>
2. <span data-ttu-id="05bd2-125">Extrayez tous les fichiers dans le téléchargement compressé.</span><span class="sxs-lookup"><span data-stu-id="05bd2-125">Extract all files in the compressed download.</span></span>
3. <span data-ttu-id="05bd2-126">Exécutez **Microsoft.MMD.DeviceReadinessAssessmentTool.exe**.</span><span class="sxs-lookup"><span data-stu-id="05bd2-126">Run **Microsoft.MMD.DeviceReadinessAssessmentTool.exe**.</span></span>
4. <span data-ttu-id="05bd2-127">Lorsque l’invite de contrôle d’accès utilisateur s’affiche, **sélectionnez Oui.**</span><span class="sxs-lookup"><span data-stu-id="05bd2-127">When the User Access Control prompt appears, select **Yes**.</span></span> <span data-ttu-id="05bd2-128">L’outil s’exécute et ouvre un rapport dans votre navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="05bd2-128">The tool runs and opens a report in your default browser.</span></span>

<span data-ttu-id="05bd2-129">Vous pouvez également télécharger et extraire l’archive  .zip vers un emplacement partagé, accéder auxMicrosoft.MMD.DeviceReadinessAssessmentTool.exeà partir de chaque appareil, puis l’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="05bd2-129">You could also download and extract the .zip archive to a shared location, access **Microsoft.MMD.DeviceReadinessAssessmentTool.exe** from each device, and then run it locally.</span></span>


## <a name="checks"></a><span data-ttu-id="05bd2-130">Vérifications</span><span class="sxs-lookup"><span data-stu-id="05bd2-130">Checks</span></span>

<span data-ttu-id="05bd2-131">L’outil téléchargeable vérifie les éléments liés à l’appareil et au réseau :</span><span class="sxs-lookup"><span data-stu-id="05bd2-131">The downloadable tool checks these device- and network-related items:</span></span>

### <a name="hardware"></a><span data-ttu-id="05bd2-132">Matériel</span><span class="sxs-lookup"><span data-stu-id="05bd2-132">Hardware</span></span>

<span data-ttu-id="05bd2-133">Les appareils doivent répondre à des exigences matérielles spécifiques pour fonctionner avec le Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05bd2-133">Devices must meet specific hardware requirements to work with Microsoft Managed Desktop.</span></span> <span data-ttu-id="05bd2-134">Actuellement, seuls des [appareils approuvés spécifiques](../service-description/device-list.md) sont autorisés à s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="05bd2-134">Currently, only specific [approved devices](../service-description/device-list.md) are allowed to enroll.</span></span> 

<span data-ttu-id="05bd2-135">Si votre appareil échoue à l’une des vérifications, il n’est pas compatible avec bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05bd2-135">If your device fails any of the checks, it's not compatible with Microsoft Managed Desktop.</span></span>

### <a name="network-endpoints"></a><span data-ttu-id="05bd2-136">Points de terminaison réseau</span><span class="sxs-lookup"><span data-stu-id="05bd2-136">Network endpoints</span></span>

<span data-ttu-id="05bd2-137">Les appareils sont en grande partie en mesure d’atteindre plusieurs [points de terminaison clés](network.md) pour fonctionner avec bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05bd2-137">Devices much be able to reach several [key endpoints](network.md) to work with Microsoft Managed Desktop.</span></span>

<span data-ttu-id="05bd2-138">Si l’outil **signale** un résultat non prêt, consultez le rapport détaillé pour savoir quels points de terminaison n’ont pas été accessibles.</span><span class="sxs-lookup"><span data-stu-id="05bd2-138">If the tool reports a **Not ready** result, see the detailed report to find out which endpoints weren't reachable.</span></span> <span data-ttu-id="05bd2-139">Ajustez ensuite votre pare-feu ou d’autres paramètres réseau pour vous assurer que ces points de terminaison sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="05bd2-139">Then adjust your firewall or other network settings to ensure those endpoints can be reached.</span></span>

### <a name="other-settings"></a><span data-ttu-id="05bd2-140">Autres paramètres</span><span class="sxs-lookup"><span data-stu-id="05bd2-140">Other settings</span></span>

#### <a name="enterprise-wi-fi-profiles"></a><span data-ttu-id="05bd2-141">Profils Wi-Fi d’entreprise</span><span class="sxs-lookup"><span data-stu-id="05bd2-141">Enterprise wi-fi profiles</span></span>

<span data-ttu-id="05bd2-142">Un **résultat d’avis** signifie que vous utilisez certains profils Wi-Fi qui ont besoin de certificats et de profils pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="05bd2-142">An **Advisory** result means that you are using some wi-fi profiles that need certificates and profiles to work properly.</span></span> <span data-ttu-id="05bd2-143">Pour plus d’informations, voir Déployer des certificats et profil [Wi-Fi/VPN.](certs-wifi-lan.md#deploy-certificates-and-wi-fivpn-profile)</span><span class="sxs-lookup"><span data-stu-id="05bd2-143">For more information, see [Deploy certificates and Wi-Fi/VPN profile](certs-wifi-lan.md#deploy-certificates-and-wi-fivpn-profile).</span></span>

#### <a name="lan-profiles"></a><span data-ttu-id="05bd2-144">Profils LAN</span><span class="sxs-lookup"><span data-stu-id="05bd2-144">LAN profiles</span></span>

<span data-ttu-id="05bd2-145">Un **résultat d’avis** signifie que vous avez des lans qui ont besoin de certificats et de profils pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="05bd2-145">An **Advisory** result means that you have LANs that need certificates and profiles to work properly.</span></span> <span data-ttu-id="05bd2-146">Pour plus d’informations, voir [Préparer les certificats et les profils réseau pour le Bureau géré Microsoft.](certs-wifi-lan.md)</span><span class="sxs-lookup"><span data-stu-id="05bd2-146">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>

#### <a name="vpn-profiles"></a><span data-ttu-id="05bd2-147">Profils VPN</span><span class="sxs-lookup"><span data-stu-id="05bd2-147">VPN profiles</span></span>

<span data-ttu-id="05bd2-148">Un **résultat d’avis** signifie que vous utilisez un réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="05bd2-148">An **Advisory** result means that you're using a virtual private network (VPN).</span></span> <span data-ttu-id="05bd2-149">Créez un profil VPN qui déploie des certificats intégrés à Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="05bd2-149">Create a VPN profile that deploys certificates integrated with Microsoft Intune.</span></span> <span data-ttu-id="05bd2-150">Pour plus d’informations, voir [Préparer les certificats et les profils réseau pour le Bureau géré Microsoft.](certs-wifi-lan.md)</span><span class="sxs-lookup"><span data-stu-id="05bd2-150">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>

#### <a name="mapped-drives"></a><span data-ttu-id="05bd2-151">Lecteurs mappés</span><span class="sxs-lookup"><span data-stu-id="05bd2-151">Mapped drives</span></span>

<span data-ttu-id="05bd2-152">Un **résultat d’avis** signifie que vous avez des lecteurs mappés, ce qui n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="05bd2-152">An **Advisory** result means that you have some mapped drives, which aren't recommended.</span></span> <span data-ttu-id="05bd2-153">Pour plus d’informations, voir [Préparer les lecteurs mappés pour le Bureau géré Microsoft.](mapped-drives.md)</span><span class="sxs-lookup"><span data-stu-id="05bd2-153">For more information, see [Prepare mapped drives for Microsoft Managed Desktop](mapped-drives.md).</span></span>

#### <a name="print-queues"></a><span data-ttu-id="05bd2-154">Imprimer les files d’attente</span><span class="sxs-lookup"><span data-stu-id="05bd2-154">Print queues</span></span>

<span data-ttu-id="05bd2-155">Un **résultat d’avis** signifie que vous avez des files d’attente d’impression en attente, ce qui n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="05bd2-155">An **Advisory** result means that you have some outstanding print queues, which aren't recommended.</span></span> <span data-ttu-id="05bd2-156">Une solution consiste à utiliser l’impression cloud.</span><span class="sxs-lookup"><span data-stu-id="05bd2-156">One solution is to use cloud printing.</span></span> <span data-ttu-id="05bd2-157">Pour plus d’informations, voir [Préparer les ressources d’impression pour le Bureau géré Microsoft.](printing.md)</span><span class="sxs-lookup"><span data-stu-id="05bd2-157">For more information, see [Prepare printing resources for Microsoft Managed Desktop](printing.md).</span></span>

#### <a name="proxies"></a><span data-ttu-id="05bd2-158">Proxies</span><span class="sxs-lookup"><span data-stu-id="05bd2-158">Proxies</span></span>

<span data-ttu-id="05bd2-159">Un **résultat d’avis** signifie que vous avez un serveur proxy en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="05bd2-159">An **Advisory** result means that you have a proxy server in use.</span></span> <span data-ttu-id="05bd2-160">Pour plus d’informations, [voir Configuration réseau pour bureau géré Microsoft.](network.md)</span><span class="sxs-lookup"><span data-stu-id="05bd2-160">For more information, see [Network configuration for Microsoft Managed Desktop](network.md).</span></span>

