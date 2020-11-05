---
title: En savoir plus sur les points de terminaison de protection contre la perte de données Microsoft 365 (Preview)
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: 'Les points de terminaison contre la protection contre la perte de données Microsoft 365 étend la surveillance des activités des fichiers et des actions de protection pour les points de terminaison. Les fichiers sont rendus visibles dans les solutions de conformité Microsoft 365 '
ms.openlocfilehash: cbf4a53658885102226d2b874180f5cc5f264a91
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48841860"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention-preview"></a><span data-ttu-id="a191f-104">En savoir plus sur les points de terminaison de protection contre la perte de données Microsoft 365 (Preview)</span><span class="sxs-lookup"><span data-stu-id="a191f-104">Learn about Microsoft 365 Endpoint data loss prevention (preview)</span></span>

<span data-ttu-id="a191f-105">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour contrôler les actions effectuées sur les éléments que vous avez jugés confidentiels et contribuer à empêcher le partage involontaire de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="a191f-105">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items.</span></span> <span data-ttu-id="a191f-106">Pour plus d’informations sur DPL, reportez-vous à [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a191f-106">For more information on DLP, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span>

<span data-ttu-id="a191f-107">**Les points de terminaison contre la protection contre la perte de données** (Endpoint DLP) étend les fonctionnalités de surveillance et de protection des activités de DLP aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a191f-107">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="a191f-108">Une fois que les appareils sont intégrés aux solutions de conformité Microsoft 365, les informations relatives à ce que les utilisateurs font avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="a191f-108">Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="a191f-109">Activités de point de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="a191f-109">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="a191f-110">Les points de terminaison Microsoft DLP vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a191f-110">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span> <span data-ttu-id="a191f-111">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a191f-111">This includes:</span></span>


|<span data-ttu-id="a191f-112">activité sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a191f-112">activity on item</span></span> |<span data-ttu-id="a191f-113">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-113">auditable/restrictable</span></span>  |
|---------|---------|
|<span data-ttu-id="a191f-114">créé</span><span class="sxs-lookup"><span data-stu-id="a191f-114">created</span></span>    | <span data-ttu-id="a191f-115">auditable</span><span class="sxs-lookup"><span data-stu-id="a191f-115">auditable</span></span>      |
|<span data-ttu-id="a191f-116">renommé</span><span class="sxs-lookup"><span data-stu-id="a191f-116">renamed</span></span>    |  <span data-ttu-id="a191f-117">auditable</span><span class="sxs-lookup"><span data-stu-id="a191f-117">auditable</span></span>       |
|<span data-ttu-id="a191f-118">copié sur un support amovible ou créé sur celui-ci</span><span class="sxs-lookup"><span data-stu-id="a191f-118">copied to or created on removable media</span></span>     |     <span data-ttu-id="a191f-119">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-119">auditable and restrictable</span></span>|
|<span data-ttu-id="a191f-120">copié sur le partage réseau, par exemple, \\My-server\fileshare</span><span class="sxs-lookup"><span data-stu-id="a191f-120">copied to network share, e.g. \\my-server\fileshare</span></span>   |     <span data-ttu-id="a191f-121">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-121">auditable and restrictable</span></span>    |
|<span data-ttu-id="a191f-122">imprimé</span><span class="sxs-lookup"><span data-stu-id="a191f-122">printed</span></span> |    <span data-ttu-id="a191f-123">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-123">auditable and restrictable</span></span>       |
|<span data-ttu-id="a191f-124">copier vers le Cloud via Chromium Edge</span><span class="sxs-lookup"><span data-stu-id="a191f-124">copied to cloud via Chromium Edge</span></span>    |   <span data-ttu-id="a191f-125">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-125">auditable and restrictable</span></span>        |
|<span data-ttu-id="a191f-126">consulté par une application ou navigateur non autorisé</span><span class="sxs-lookup"><span data-stu-id="a191f-126">accessed by unallowed apps and browsers</span></span>    |  <span data-ttu-id="a191f-127">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="a191f-127">auditable and restrictable</span></span>       |

## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="a191f-128">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="a191f-128">What's different in Endpoint DLP</span></span>

<span data-ttu-id="a191f-129">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="a191f-129">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="a191f-130">Activation de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="a191f-130">Enabling Device management</span></span>

<span data-ttu-id="a191f-131">La gestion des appareils est une fonctionnalité qui permet d’assembler la télémétrie à partir d’appareils et de l’intégrer à des solutions de conformité Microsoft 365 telles que point de terminaison DLP et [ gestionnaire des risques Insider](insider-risk-management.md).</span><span class="sxs-lookup"><span data-stu-id="a191f-131">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md).</span></span> <span data-ttu-id="a191f-132">Vous devez intégrer tous les appareils que vous voulez utiliser en tant qu’emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="a191f-132">You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)

<span data-ttu-id="a191f-134">L’intégration et déclassement sont gérés à l’aide de scripts téléchargés à partir du centre de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="a191f-134">Onboarding and offboarding are handled via scripts you download from the Device management center.</span></span> <span data-ttu-id="a191f-135">Le centre inclut des scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="a191f-135">The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="a191f-136">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="a191f-136">local script (up to 10 machines)</span></span>
- <span data-ttu-id="a191f-137">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a191f-137">Group policy</span></span>
- <span data-ttu-id="a191f-138">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a191f-138">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="a191f-139">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a191f-139">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="a191f-140">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="a191f-140">VDI onboarding scripts for non-persistent machines</span></span>

![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)

 <span data-ttu-id="a191f-142">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="a191f-142">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="a191f-143">Si vous avez des appareils intégrés via [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="a191f-143">If you have onboarded devices through [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="a191f-145">Affichage des données DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a191f-145">Viewing Endpoint DLP data</span></span>

 <span data-ttu-id="a191f-146">Le point de terminaison DLP de point de terminaison affiche le type MIME basé sur l’activité, de sorte que les activités sont capturées même si l’extension de fichier est modifiée.</span><span class="sxs-lookup"><span data-stu-id="a191f-146">Endpoint DLP monitors activity based om MIME type, so activities will be captured even if the file extension is changed.</span></span> <span data-ttu-id="a191f-147">Dans la version public Preview, il observe tous les :</span><span class="sxs-lookup"><span data-stu-id="a191f-147">At public preview it watches all:</span></span>

- <span data-ttu-id="a191f-148">Fichiers Word</span><span class="sxs-lookup"><span data-stu-id="a191f-148">Word files</span></span>
- <span data-ttu-id="a191f-149">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="a191f-149">PowerPoint files</span></span>
- <span data-ttu-id="a191f-150">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="a191f-150">Excel files</span></span>
- <span data-ttu-id="a191f-151">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="a191f-151">PDF files</span></span>
- <span data-ttu-id="a191f-152">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="a191f-152">.csv files</span></span>
- <span data-ttu-id="a191f-153">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="a191f-153">.tsv files</span></span>
- <span data-ttu-id="a191f-154">fichiers c</span><span class="sxs-lookup"><span data-stu-id="a191f-154">c files</span></span>
- <span data-ttu-id="a191f-155">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="a191f-155">class files</span></span>
- <span data-ttu-id="a191f-156">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="a191f-156">cpp files</span></span>
- <span data-ttu-id="a191f-157">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="a191f-157">cs files</span></span>
- <span data-ttu-id="a191f-158">fichiers h</span><span class="sxs-lookup"><span data-stu-id="a191f-158">h files</span></span>
- <span data-ttu-id="a191f-159">fichiers Java</span><span class="sxs-lookup"><span data-stu-id="a191f-159">java files</span></span>

> [!NOTE]
> <span data-ttu-id="a191f-160">Les fichiers. txt et de code source ne sont pas audités par défaut, DLP les évalue par rapport aux stratégies appliquées, puis les actions des utilisateurs sont auditées ou bloquées en conséquence.</span><span class="sxs-lookup"><span data-stu-id="a191f-160">.txt and source code files are not audited by default, DLP evaluates them against the applied policies and then user actions are audited or blocked accordingly.</span></span>

<span data-ttu-id="a191f-161">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, même avant de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="a191f-161">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

![événements de point de terminaison DLP dans l’Explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)

<span data-ttu-id="a191f-163">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="a191f-163">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="a191f-164">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="a191f-164">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="a191f-165">type d’activité</span><span class="sxs-lookup"><span data-stu-id="a191f-165">activity type</span></span>
- <span data-ttu-id="a191f-166">IP Client</span><span class="sxs-lookup"><span data-stu-id="a191f-166">client IP</span></span>
- <span data-ttu-id="a191f-167">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="a191f-167">target file path</span></span>
- <span data-ttu-id="a191f-168">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="a191f-168">happened timestamp</span></span>
- <span data-ttu-id="a191f-169">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="a191f-169">file name</span></span>
- <span data-ttu-id="a191f-170">utilisateur</span><span class="sxs-lookup"><span data-stu-id="a191f-170">user</span></span>
- <span data-ttu-id="a191f-171">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="a191f-171">file extension</span></span>
- <span data-ttu-id="a191f-172">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="a191f-172">file size</span></span>
- <span data-ttu-id="a191f-173">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="a191f-173">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="a191f-174">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="a191f-174">sha1 value</span></span>
- <span data-ttu-id="a191f-175">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="a191f-175">sha256 value</span></span>
- <span data-ttu-id="a191f-176">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="a191f-176">previous file name</span></span>
- <span data-ttu-id="a191f-177">emplacement</span><span class="sxs-lookup"><span data-stu-id="a191f-177">location</span></span>
- <span data-ttu-id="a191f-178">parent</span><span class="sxs-lookup"><span data-stu-id="a191f-178">parent</span></span>
- <span data-ttu-id="a191f-179">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a191f-179">filepath</span></span>
- <span data-ttu-id="a191f-180">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="a191f-180">source location type</span></span>
- <span data-ttu-id="a191f-181">platform</span><span class="sxs-lookup"><span data-stu-id="a191f-181">platform</span></span>
- <span data-ttu-id="a191f-182">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="a191f-182">device name</span></span>
- <span data-ttu-id="a191f-183">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="a191f-183">destination location type</span></span>
- <span data-ttu-id="a191f-184">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="a191f-184">application that performed the copy</span></span>
- <span data-ttu-id="a191f-185">ID de l’appareil Microsoft Defender pour point de terminaison (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="a191f-185">Microsoft Defender for Endpoint device ID (if applicable)</span></span>
- <span data-ttu-id="a191f-186">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="a191f-186">removable media device manufacturer</span></span>
- <span data-ttu-id="a191f-187">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="a191f-187">removable media device model</span></span>
- <span data-ttu-id="a191f-188">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="a191f-188">removable media device serial number</span></span>

![attributs d’activité copier vers USB](../media/endpoint-dlp-learn-about-5-activity-attributes.png)

## <a name="next-steps"></a><span data-ttu-id="a191f-190">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a191f-190">Next steps</span></span>

<span data-ttu-id="a191f-191">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a191f-191">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1) [<span data-ttu-id="a191f-192">Prise en main des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="a191f-192">Getting started with Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-getting-started.md)
2) [<span data-ttu-id="a191f-193">Utilisation des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="a191f-193">Using Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="a191f-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a191f-194">See also</span></span>

- [<span data-ttu-id="a191f-195">Prise en main des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="a191f-195">Getting started with Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="a191f-196">Utilisation des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="a191f-196">Using Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="a191f-197">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="a191f-197">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="a191f-198">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="a191f-198">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="a191f-199">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="a191f-199">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="a191f-200">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a191f-200">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- [<span data-ttu-id="a191f-201">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="a191f-201">Insider Risk management</span></span>](insider-risk-management.md)