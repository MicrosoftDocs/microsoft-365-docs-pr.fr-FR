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
- SPO_Content
search.appverid:
- MET150
description: 'Les points de terminaison contre la protection contre la perte de données Microsoft 365 étend la surveillance des activités des fichiers et des actions de protection pour les points de terminaison. Les fichiers sont rendus visibles dans les solutions de conformité Microsoft 365 '
ms.openlocfilehash: 5dfe8fae1e000b97d7c2a17d3d7582fd1b24934e
ms.sourcegitcommit: a08103bc120bdec7cfeaf67c1be4e221241e69ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2020
ms.locfileid: "45199982"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention-preview"></a><span data-ttu-id="bd4a6-104">En savoir plus sur les points de terminaison de protection contre la perte de données Microsoft 365 (Preview)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-104">Learn about Microsoft 365 Endpoint data loss prevention (preview)</span></span>

<span data-ttu-id="bd4a6-105">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour contrôler les actions effectuées sur les éléments que vous avez jugés confidentiels et contribuer à empêcher le partage involontaire de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-105">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items.</span></span> <span data-ttu-id="bd4a6-106">Pour plus d’informations sur DPL, reportez-vous à [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="bd4a6-106">For more information on DLP, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span>

<span data-ttu-id="bd4a6-107">**Les points de terminaison contre la protection contre la perte de données** (Endpoint DLP) étend les fonctionnalités de surveillance et de protection des activités de DLP aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-107">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="bd4a6-108">Une fois que les appareils sont intégrés à la gestion des appareils, les informations relatives à ce que les utilisateurs effectuent avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="bd4a6-108">Once devices are onboarded into device management, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="bd4a6-109">Activités de point de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="bd4a6-109">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="bd4a6-110">Les points de terminaison Microsoft DLP vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-110">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span> <span data-ttu-id="bd4a6-111">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd4a6-111">This includes:</span></span>


|<span data-ttu-id="bd4a6-112">activité sur l’élément</span><span class="sxs-lookup"><span data-stu-id="bd4a6-112">activity on item</span></span> |<span data-ttu-id="bd4a6-113">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-113">auditable/restrictable</span></span>  |
|---------|---------|
|<span data-ttu-id="bd4a6-114">créé</span><span class="sxs-lookup"><span data-stu-id="bd4a6-114">created</span></span>    | <span data-ttu-id="bd4a6-115">auditable</span><span class="sxs-lookup"><span data-stu-id="bd4a6-115">auditable</span></span>      |
|<span data-ttu-id="bd4a6-116">renommé</span><span class="sxs-lookup"><span data-stu-id="bd4a6-116">renamed</span></span>    |  <span data-ttu-id="bd4a6-117">auditable</span><span class="sxs-lookup"><span data-stu-id="bd4a6-117">auditable</span></span>       |
|<span data-ttu-id="bd4a6-118">copié sur un support amovible ou créé sur celui-ci</span><span class="sxs-lookup"><span data-stu-id="bd4a6-118">copied to or created on removable media</span></span>     |     <span data-ttu-id="bd4a6-119">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-119">auditable and restrictable</span></span>|
|<span data-ttu-id="bd4a6-120">copié sur le partage réseau, par exemple, \\My-server\fileshare</span><span class="sxs-lookup"><span data-stu-id="bd4a6-120">copied to network share, e.g. \\my-server\fileshare</span></span>   |     <span data-ttu-id="bd4a6-121">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-121">auditable and restrictable</span></span>    |
|<span data-ttu-id="bd4a6-122">imprimé</span><span class="sxs-lookup"><span data-stu-id="bd4a6-122">printed</span></span> |    <span data-ttu-id="bd4a6-123">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-123">auditable and restrictable</span></span>       |
|<span data-ttu-id="bd4a6-124">copier vers le Cloud via Chromium Edge</span><span class="sxs-lookup"><span data-stu-id="bd4a6-124">copied to cloud via Chromium Edge</span></span>    |   <span data-ttu-id="bd4a6-125">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-125">auditable and restrictable</span></span>        |
|<span data-ttu-id="bd4a6-126">consulté par une application ou navigateur non autorisé</span><span class="sxs-lookup"><span data-stu-id="bd4a6-126">accessed by unallowed apps and browsers</span></span>    |  <span data-ttu-id="bd4a6-127">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-127">auditable and restrictable</span></span>       |

## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="bd4a6-128">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="bd4a6-128">What's different in Endpoint DLP</span></span>

<span data-ttu-id="bd4a6-129">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-129">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="bd4a6-130">Activation de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="bd4a6-130">Enabling Device management</span></span>

<span data-ttu-id="bd4a6-131">La gestion des appareils est une fonctionnalité qui permet d’assembler la télémétrie à partir d’appareils et de l’intégrer à des solutions de conformité Microsoft 365 telles que point de terminaison DLP et [ gestionnaire des risques Insider](insider-risk-management.md).</span><span class="sxs-lookup"><span data-stu-id="bd4a6-131">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md).</span></span> <span data-ttu-id="bd4a6-132">Vous devez intégrer tous les appareils que vous voulez utiliser en tant qu’emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-132">You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)

<span data-ttu-id="bd4a6-134">L’intégration et déclassement sont gérés à l’aide de scripts téléchargés à partir du centre de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-134">Onboarding and offboarding are handled via scripts you download from the Device management center.</span></span> <span data-ttu-id="bd4a6-135">Le centre inclut des scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="bd4a6-135">The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="bd4a6-136">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-136">local script (up to 10 machines)</span></span>
- <span data-ttu-id="bd4a6-137">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd4a6-137">Group policy</span></span>
- <span data-ttu-id="bd4a6-138">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bd4a6-138">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="bd4a6-139">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="bd4a6-139">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="bd4a6-140">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="bd4a6-140">VDI onboarding scripts for non-persistent machines</span></span>

![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)

 <span data-ttu-id="bd4a6-142">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-142">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="bd4a6-143">Si vous avez des appareils intégrés via [Protection avancée contre les menaces Microsoft Defender (Microsoft Defender ATP)](https://docs.microsoft.com/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-143">If you have onboarded devices through [Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)](https://docs.microsoft.com/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="bd4a6-145">Affichage des données DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bd4a6-145">Viewing Endpoint DLP data</span></span>

 <span data-ttu-id="bd4a6-146">Le point de terminaison DLP de point de terminaison affiche le type MIME basé sur l’activité, de sorte que les activités sont capturées même si l’extension de fichier est modifiée.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-146">Endpoint DLP monitors activity based om MIME type, so activities will be captured even if the file extension is changed.</span></span> <span data-ttu-id="bd4a6-147">Dans la version public Preview, il observe tous les :</span><span class="sxs-lookup"><span data-stu-id="bd4a6-147">At public preview it watches all:</span></span>

- <span data-ttu-id="bd4a6-148">Fichiers Word</span><span class="sxs-lookup"><span data-stu-id="bd4a6-148">Word files</span></span>
- <span data-ttu-id="bd4a6-149">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="bd4a6-149">PowerPoint files</span></span>
- <span data-ttu-id="bd4a6-150">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="bd4a6-150">Excel files</span></span>
- <span data-ttu-id="bd4a6-151">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="bd4a6-151">PDF files</span></span>
- <span data-ttu-id="bd4a6-152">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="bd4a6-152">.csv files</span></span>
- <span data-ttu-id="bd4a6-153">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="bd4a6-153">.tsv files</span></span>
- <span data-ttu-id="bd4a6-154">fichiers c</span><span class="sxs-lookup"><span data-stu-id="bd4a6-154">c files</span></span>
- <span data-ttu-id="bd4a6-155">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="bd4a6-155">class files</span></span>
- <span data-ttu-id="bd4a6-156">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="bd4a6-156">cpp files</span></span>
- <span data-ttu-id="bd4a6-157">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="bd4a6-157">cs files</span></span>
- <span data-ttu-id="bd4a6-158">fichiers h</span><span class="sxs-lookup"><span data-stu-id="bd4a6-158">h files</span></span>
- <span data-ttu-id="bd4a6-159">fichiers Java</span><span class="sxs-lookup"><span data-stu-id="bd4a6-159">java files</span></span>

> [!NOTE]
> <span data-ttu-id="bd4a6-160">Les fichiers. txt et de code source ne sont pas audités par défaut, DLP les évalue par rapport aux stratégies appliquées, puis les actions des utilisateurs sont auditées ou bloquées en conséquence.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-160">.txt and source code files are not audited by default, DLP evaluates them against the applied policies and then user actions are audited or blocked accordingly.</span></span>

<span data-ttu-id="bd4a6-161">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, même avant de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-161">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

![événements de point de terminaison DLP dans l’Explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)

<span data-ttu-id="bd4a6-163">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="bd4a6-163">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="bd4a6-164">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="bd4a6-164">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="bd4a6-165">type d’activité</span><span class="sxs-lookup"><span data-stu-id="bd4a6-165">activity type</span></span>
- <span data-ttu-id="bd4a6-166">IP Client</span><span class="sxs-lookup"><span data-stu-id="bd4a6-166">client IP</span></span>
- <span data-ttu-id="bd4a6-167">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="bd4a6-167">target file path</span></span>
- <span data-ttu-id="bd4a6-168">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="bd4a6-168">happened timestamp</span></span>
- <span data-ttu-id="bd4a6-169">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="bd4a6-169">file name</span></span>
- <span data-ttu-id="bd4a6-170">utilisateur</span><span class="sxs-lookup"><span data-stu-id="bd4a6-170">user</span></span>
- <span data-ttu-id="bd4a6-171">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="bd4a6-171">file extension</span></span>
- <span data-ttu-id="bd4a6-172">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="bd4a6-172">file size</span></span>
- <span data-ttu-id="bd4a6-173">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-173">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="bd4a6-174">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="bd4a6-174">sha1 value</span></span>
- <span data-ttu-id="bd4a6-175">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="bd4a6-175">sha256 value</span></span>
- <span data-ttu-id="bd4a6-176">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="bd4a6-176">previous file name</span></span>
- <span data-ttu-id="bd4a6-177">emplacement</span><span class="sxs-lookup"><span data-stu-id="bd4a6-177">location</span></span>
- <span data-ttu-id="bd4a6-178">parent</span><span class="sxs-lookup"><span data-stu-id="bd4a6-178">parent</span></span>
- <span data-ttu-id="bd4a6-179">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bd4a6-179">filepath</span></span>
- <span data-ttu-id="bd4a6-180">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="bd4a6-180">source location type</span></span>
- <span data-ttu-id="bd4a6-181">platform</span><span class="sxs-lookup"><span data-stu-id="bd4a6-181">platform</span></span>
- <span data-ttu-id="bd4a6-182">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="bd4a6-182">device name</span></span>
- <span data-ttu-id="bd4a6-183">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="bd4a6-183">destination location type</span></span>
- <span data-ttu-id="bd4a6-184">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="bd4a6-184">application that performed the copy</span></span>
- <span data-ttu-id="bd4a6-185">ID d’appareil MDATP (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-185">MDATP device ID (if applicable)</span></span>
- <span data-ttu-id="bd4a6-186">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="bd4a6-186">removable media device manufacturer</span></span>
- <span data-ttu-id="bd4a6-187">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="bd4a6-187">removable media device model</span></span>
- <span data-ttu-id="bd4a6-188">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="bd4a6-188">removable media device serial number</span></span>

![attributs d’activité copier vers USB](../media/endpoint-dlp-learn-about-5-activity-attributes.png)

## <a name="next-steps"></a><span data-ttu-id="bd4a6-190">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="bd4a6-190">Next steps</span></span>

<span data-ttu-id="bd4a6-191">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd4a6-191">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1) [<span data-ttu-id="bd4a6-192">Prise en main des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-192">Getting started with Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-getting-started.md)
2) [<span data-ttu-id="bd4a6-193">Utilisation des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-193">Using Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="bd4a6-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd4a6-194">See also</span></span>

- [<span data-ttu-id="bd4a6-195">Prise en main des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-195">Getting started with Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="bd4a6-196">Utilisation des points de terminaison de protection contre la perte de données Microsoft (Preview)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-196">Using Microsoft Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="bd4a6-197">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="bd4a6-197">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="bd4a6-198">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="bd4a6-198">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="bd4a6-199">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="bd4a6-199">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="bd4a6-200">Microsoft Defender – Protection avancée contre les menaces (Microsoft Defender ATP)</span><span class="sxs-lookup"><span data-stu-id="bd4a6-200">Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- [<span data-ttu-id="bd4a6-201">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="bd4a6-201">Insider Risk management</span></span>](insider-risk-management.md)