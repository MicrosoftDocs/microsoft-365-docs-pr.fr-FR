---
title: Résoudre les problèmes liés aux outils de rapport pour Microsoft Defender AV
description: Identifier et résoudre les problèmes courants lors de la tentative de signalement de l'état de protection de l'Antivirus Microsoft Defender dans Update Compliance
keywords: résoudre les problèmes, erreur, corriger, mettre à jour la conformité, oms, surveiller, signaler, Microsoft Defender AV
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 3b1a1c807c86aa95148300298484319001b59963
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690771"
---
# <a name="troubleshoot-microsoft-defender-antivirus-reporting-in-update-compliance"></a><span data-ttu-id="cbae0-104">Résoudre les problèmes de rapport de l'Antivirus Microsoft Defender dans Update Compliance</span><span class="sxs-lookup"><span data-stu-id="cbae0-104">Troubleshoot Microsoft Defender Antivirus reporting in Update Compliance</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="cbae0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cbae0-105">**Applies to:**</span></span>

- [<span data-ttu-id="cbae0-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cbae0-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!IMPORTANT]
> <span data-ttu-id="cbae0-107">Le 31 mars 2020, la fonctionnalité de rapport de l'Antivirus Microsoft Defender de la conformité des mises à jour sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="cbae0-107">On March 31, 2020, the Microsoft Defender Antivirus reporting feature of Update Compliance will be removed.</span></span> <span data-ttu-id="cbae0-108">Vous pouvez continuer à définir et à passer en revue les stratégies de conformité de sécurité à l'aide de [Microsoft Endpoint Manager,](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager)ce qui permet un contrôle plus fin sur les fonctionnalités de sécurité et les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="cbae0-108">You can continue to define and review security compliance policies using [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager), which allows finer control over security features and updates.</span></span>

<span data-ttu-id="cbae0-109">Vous pouvez utiliser l'Antivirus Microsoft Defender avec update compliance.</span><span class="sxs-lookup"><span data-stu-id="cbae0-109">You can use Microsoft Defender Antivirus with Update Compliance.</span></span> <span data-ttu-id="cbae0-110">Vous verrez l'état des licences E3, B, F1, VL et Pro.</span><span class="sxs-lookup"><span data-stu-id="cbae0-110">You’ll see status for E3, B, F1, VL, and Pro licenses.</span></span> <span data-ttu-id="cbae0-111">Toutefois, pour les licences E5, vous devez utiliser le [portail Microsoft Defender pour points de terminaison.](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span><span class="sxs-lookup"><span data-stu-id="cbae0-111">However, for E5 licenses, you need to use the [Microsoft Defender for Endpoint portal](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="cbae0-112">Pour en savoir plus sur les options de licence, voir les options de licence de produit [Windows 10.](https://www.microsoft.com/licensing/product-licensing/windows10.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbae0-112">To learn more about licensing options, see [Windows 10 product licensing options](https://www.microsoft.com/licensing/product-licensing/windows10.aspx).</span></span>

<span data-ttu-id="cbae0-113">Lorsque vous utilisez la conformité des mises à jour [Windows Analytics](/windows/deployment/update/update-compliance-using#wdav-assessment) pour obtenir des rapports sur l'état de protection des appareils ou des points de terminaison de votre réseau qui utilisent l'Antivirus Microsoft Defender, vous pouvez rencontrer des problèmes ou des problèmes.</span><span class="sxs-lookup"><span data-stu-id="cbae0-113">When you use [Windows Analytics Update Compliance to obtain reporting into the protection status of devices or endpoints](/windows/deployment/update/update-compliance-using#wdav-assessment) in your network that are using Microsoft Defender Antivirus, you might encounter problems or issues.</span></span>

<span data-ttu-id="cbae0-114">En règle générale, les indicateurs les plus courants d'un problème sont :</span><span class="sxs-lookup"><span data-stu-id="cbae0-114">Typically, the most common indicators of a problem are:</span></span>
- <span data-ttu-id="cbae0-115">Vous ne voyez qu'un petit nombre ou un sous-ensemble de tous les appareils que vous attendiez à voir</span><span class="sxs-lookup"><span data-stu-id="cbae0-115">You only see a small number or subset of all the devices you were expecting to see</span></span>
- <span data-ttu-id="cbae0-116">Vous ne voyez aucun appareil</span><span class="sxs-lookup"><span data-stu-id="cbae0-116">You do not see any devices at all</span></span>
- <span data-ttu-id="cbae0-117">Les rapports et informations que vous voyez sont obsolètes (plus de quelques jours)</span><span class="sxs-lookup"><span data-stu-id="cbae0-117">The reports and information you do see is outdated (older than a few days)</span></span>

<span data-ttu-id="cbae0-118">Pour obtenir des codes d'erreur courants et des ID d'événement liés au service Antivirus Microsoft Defender qui ne sont pas liés à update compliance, consultez les événements de [l'Antivirus Microsoft Defender.](troubleshoot-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="cbae0-118">For common error codes and event IDs related to the Microsoft Defender Antivirus service that are not related to Update Compliance, see [Microsoft Defender Antivirus events](troubleshoot-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="cbae0-119">La résolution de ces problèmes se fait en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="cbae0-119">There are three steps to troubleshooting these problems:</span></span>

1. <span data-ttu-id="cbae0-120">Vérifier que vous avez satisfait à toutes les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="cbae0-120">Confirm that you have met all prerequisites</span></span>
2. <span data-ttu-id="cbae0-121">Vérifier votre connectivité au service Windows Defender cloud</span><span class="sxs-lookup"><span data-stu-id="cbae0-121">Check your connectivity to the Windows Defender cloud-based service</span></span>
3. <span data-ttu-id="cbae0-122">Envoyer les journaux de support</span><span class="sxs-lookup"><span data-stu-id="cbae0-122">Submit support logs</span></span>

>[!IMPORTANT]
><span data-ttu-id="cbae0-123">L'apparition des appareils dans update Compliance prend généralement 3 jours.</span><span class="sxs-lookup"><span data-stu-id="cbae0-123">It typically takes 3 days for devices to start appearing in Update Compliance.</span></span>


## <a name="confirm-prerequisites"></a><span data-ttu-id="cbae0-124">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="cbae0-124">Confirm prerequisites</span></span>

<span data-ttu-id="cbae0-125">Pour que les appareils s'affichent correctement dans Update Compliance, vous devez respecter certaines conditions préalables pour le service de conformité des mises à jour et pour l'Antivirus Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="cbae0-125">In order for devices to properly show up in Update Compliance, you have to meet certain prerequisites for both the Update Compliance service and for Microsoft Defender Antivirus:</span></span>

>[!div class="checklist"]
>- <span data-ttu-id="cbae0-126">Les points de terminaison utilisent l'Antivirus Microsoft Defender comme seule application de protection antivirus.</span><span class="sxs-lookup"><span data-stu-id="cbae0-126">Endpoints are using Microsoft Defender Antivirus as the sole antivirus protection app.</span></span> <span data-ttu-id="cbae0-127">[L'utilisation d'une autre application antivirus](microsoft-defender-antivirus-compatibility.md) entraîne la désactivation de Microsoft Defender AV et le point de terminaison n'est pas signalé dans Update Compliance.</span><span class="sxs-lookup"><span data-stu-id="cbae0-127">[Using any other antivirus app will cause Microsoft Defender AV to disable itself](microsoft-defender-antivirus-compatibility.md) and the endpoint will not be reported in Update Compliance.</span></span>
> - <span data-ttu-id="cbae0-128">[La protection cloud est activée.](enable-cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="cbae0-128">[Cloud-delivered protection is enabled](enable-cloud-protection-microsoft-defender-antivirus.md).</span></span>
> - <span data-ttu-id="cbae0-129">Les points de terminaison [peuvent se connecter au cloud de Microsoft Defender AV](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="cbae0-129">Endpoints can [connect to the Microsoft Defender AV cloud](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud)</span></span>
> - <span data-ttu-id="cbae0-130">Si le point de terminaison exécute Windows 10 version 1607 ou antérieure, les données de [diagnostic Windows 10](/windows/configuration/configure-windows-diagnostic-data-in-your-organization#enhanced-level)doivent être définies sur le niveau Amélioré.</span><span class="sxs-lookup"><span data-stu-id="cbae0-130">If the endpoint is running Windows 10 version 1607 or earlier, [Windows 10 diagnostic data must be set to the Enhanced level](/windows/configuration/configure-windows-diagnostic-data-in-your-organization#enhanced-level).</span></span>
> - <span data-ttu-id="cbae0-131">Cela fait 3 jours que toutes les conditions requises ont été satisfaites</span><span class="sxs-lookup"><span data-stu-id="cbae0-131">It has been 3 days since all requirements have been met</span></span>

<span data-ttu-id="cbae0-132">« Vous pouvez utiliser l'Antivirus Microsoft Defender avec update compliance.</span><span class="sxs-lookup"><span data-stu-id="cbae0-132">“You can use Microsoft Defender Antivirus with Update Compliance.</span></span> <span data-ttu-id="cbae0-133">Vous verrez l'état des licences E3, B, F1, VL et Pro.</span><span class="sxs-lookup"><span data-stu-id="cbae0-133">You’ll see status for E3, B, F1, VL, and Pro licenses.</span></span> <span data-ttu-id="cbae0-134">Toutefois, pour les licences E5, vous devez utiliser le portail Microsoft Defender pour points de terminaison ( https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints) .</span><span class="sxs-lookup"><span data-stu-id="cbae0-134">However, for E5 licenses, you need to use the Microsoft Defender for Endpoint portal (https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="cbae0-135">Pour en savoir plus sur les options de licence, voir les options de licence de produit Windows 10 »</span><span class="sxs-lookup"><span data-stu-id="cbae0-135">To learn more about licensing options, see Windows 10 product licensing options"</span></span>

<span data-ttu-id="cbae0-136">Si les conditions préalables ci-dessus ont toutes été remplies, vous devrez peut-être passer à l'étape suivante pour collecter des informations de diagnostic et nous les envoyer.</span><span class="sxs-lookup"><span data-stu-id="cbae0-136">If the above prerequisites have all been met, you might need to proceed to the next step to collect diagnostic information and send it to us.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="cbae0-137">Collecter des données de diagnostic pour le dépannage de la conformité des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cbae0-137">Collect diagnostic data for Update Compliance troubleshooting</span></span>](collect-diagnostic-data.md)  

## <a name="related-topics"></a><span data-ttu-id="cbae0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbae0-138">Related topics</span></span>

- [<span data-ttu-id="cbae0-139">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="cbae0-139">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="cbae0-140">Déployer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="cbae0-140">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)