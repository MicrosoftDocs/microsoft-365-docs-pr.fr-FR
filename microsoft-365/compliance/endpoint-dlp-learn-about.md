---
title: Découvrir la protection contre la perte de données des point de terminaison de Microsoft 365
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
description: 'La protection contre la perte de données des point de terminaison de Microsoft 365 étend la surveillance des activités de fichiers et les actions de protection pour ces fichiers aux points de terminaison. Les fichiers sont rendus visibles dans les solutions de conformité Microsoft 365 '
ms.openlocfilehash: e469872dac19db08f7b525c8a5ada725c75bfa10
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49072973"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention"></a><span data-ttu-id="dcb09-104">Découvrir la protection contre la perte de données des point de terminaison de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="dcb09-104">Learn about Microsoft 365 Endpoint data loss prevention</span></span>

<span data-ttu-id="dcb09-p102">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour surveiller les actions entreprises sur les éléments que vous jugez sensibles et pour éviter le partage involontaire de ces éléments. Si vous souhaitez en savoir plus sur la DLP, consultez l’article [Présentation de la protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dcb09-p102">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items. For more information on DLP, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span>

<span data-ttu-id="dcb09-p103">La **protection contre la perte de données des point de terminaison** (DLP des points de terminaison) étend les capacités de surveillance et de protection de l’activité de la DLP aux éléments sensibles qui se trouvent sur les appareils Windows 10. Une fois les appareils intégrés dans les solutions de conformité Microsoft 365, les informations relatives à l’utilisation des éléments sensibles par les utilisateurs sont rendues visibles dans l’ [explorateur d’activités](data-classification-activity-explorer.md). Vous pouvez appliquer des actions de protection sur ces éléments via des [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="dcb09-p103">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices. Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="dcb09-109">Activités des points de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="dcb09-109">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="dcb09-p104">La protection contre la perte de données des point de terminaison Microsoft vous permet d’auditer et de gérer les types d’activités suivants, que les utilisateurs utilisent sur des éléments sensibles sur des appareils fonctionnant sous Windows 10. Cela comprend :</span><span class="sxs-lookup"><span data-stu-id="dcb09-p104">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10. This includes:</span></span>


|<span data-ttu-id="dcb09-112">activité sur l’élément</span><span class="sxs-lookup"><span data-stu-id="dcb09-112">activity on item</span></span> |<span data-ttu-id="dcb09-113">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-113">auditable/restrictable</span></span>  |
|---------|---------|
|<span data-ttu-id="dcb09-114">créé</span><span class="sxs-lookup"><span data-stu-id="dcb09-114">created</span></span>    | <span data-ttu-id="dcb09-115">auditable</span><span class="sxs-lookup"><span data-stu-id="dcb09-115">auditable</span></span>      |
|<span data-ttu-id="dcb09-116">renommé</span><span class="sxs-lookup"><span data-stu-id="dcb09-116">renamed</span></span>    |  <span data-ttu-id="dcb09-117">auditable</span><span class="sxs-lookup"><span data-stu-id="dcb09-117">auditable</span></span>       |
|<span data-ttu-id="dcb09-118">copié sur un support amovible ou créé sur celui-ci</span><span class="sxs-lookup"><span data-stu-id="dcb09-118">copied to or created on removable media</span></span>     |     <span data-ttu-id="dcb09-119">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-119">auditable and restrictable</span></span>|
|<span data-ttu-id="dcb09-120">copié sur le partage réseau, par exemple, \\My-server\fileshare</span><span class="sxs-lookup"><span data-stu-id="dcb09-120">copied to network share, e.g. \\my-server\fileshare</span></span>   |     <span data-ttu-id="dcb09-121">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-121">auditable and restrictable</span></span>    |
|<span data-ttu-id="dcb09-122">imprimé</span><span class="sxs-lookup"><span data-stu-id="dcb09-122">printed</span></span> |    <span data-ttu-id="dcb09-123">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-123">auditable and restrictable</span></span>       |
|<span data-ttu-id="dcb09-124">copier vers le Cloud via Chromium Edge</span><span class="sxs-lookup"><span data-stu-id="dcb09-124">copied to cloud via Chromium Edge</span></span>    |   <span data-ttu-id="dcb09-125">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-125">auditable and restrictable</span></span>        |
|<span data-ttu-id="dcb09-126">consulté par une application ou navigateur non autorisé</span><span class="sxs-lookup"><span data-stu-id="dcb09-126">accessed by unallowed apps and browsers</span></span>    |  <span data-ttu-id="dcb09-127">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="dcb09-127">auditable and restrictable</span></span>       |

## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="dcb09-128">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="dcb09-128">What's different in Endpoint DLP</span></span>

<span data-ttu-id="dcb09-129">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="dcb09-129">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="dcb09-130">Activer la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="dcb09-130">Enabling Device management</span></span>

<span data-ttu-id="dcb09-p105">La Gestion des appareils est la fonctionnalité qui permet la collecte des données de télémétrie à partir des appareils et qui les intègre dans les solutions de conformité Microsoft 365 telles que la protection contre la perte de données des point de terminaison et la [Gestion des risques internes](insider-risk-management.md). Vous devrez intégrer tous les appareils que vous souhaitez utiliser comme emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="dcb09-p105">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md). You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dcb09-133">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="dcb09-133">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

<span data-ttu-id="dcb09-p106">L’intégration et la désactivation sont gérées via des scripts que vous téléchargez à partir du centre de gestion des appareils. Le centre dispose de scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="dcb09-p106">Onboarding and offboarding are handled via scripts you download from the Device management center. The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="dcb09-136">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="dcb09-136">local script (up to 10 machines)</span></span>
- <span data-ttu-id="dcb09-137">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="dcb09-137">Group policy</span></span>
- <span data-ttu-id="dcb09-138">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="dcb09-138">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="dcb09-139">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="dcb09-139">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="dcb09-140">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="dcb09-140">VDI onboarding scripts for non-persistent machines</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dcb09-141">![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span><span class="sxs-lookup"><span data-stu-id="dcb09-141">![device onboarding page](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span></span>

 <span data-ttu-id="dcb09-142">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="dcb09-142">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="dcb09-143">Si vous avez des appareils intégrés via [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="dcb09-143">If you have onboarded devices through [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dcb09-144">![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)</span><span class="sxs-lookup"><span data-stu-id="dcb09-144">![managed devices list](../media/endpoint-dlp-learn-about-2-device-list.png)</span></span>

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="dcb09-145">Afficher les données de DLP des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="dcb09-145">Viewing Endpoint DLP data</span></span>

 <span data-ttu-id="dcb09-p107">La DLP des points de terminaison surveille l’activité en fonction du type MIME. Les activités seront donc capturées même si l’extension de fichier est modifiée. Dans la préversion publique, elle observe tous les :</span><span class="sxs-lookup"><span data-stu-id="dcb09-p107">Endpoint DLP monitors activity-based on MIME type, so activities will be captured even if the file extension is changed. At public preview it watches all:</span></span>

- <span data-ttu-id="dcb09-148">fichiers Word</span><span class="sxs-lookup"><span data-stu-id="dcb09-148">Word files</span></span>
- <span data-ttu-id="dcb09-149">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dcb09-149">PowerPoint files</span></span>
- <span data-ttu-id="dcb09-150">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="dcb09-150">Excel files</span></span>
- <span data-ttu-id="dcb09-151">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="dcb09-151">PDF files</span></span>
- <span data-ttu-id="dcb09-152">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="dcb09-152">.csv files</span></span>
- <span data-ttu-id="dcb09-153">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="dcb09-153">.tsv files</span></span>
- <span data-ttu-id="dcb09-154">fichiers .txt</span><span class="sxs-lookup"><span data-stu-id="dcb09-154">.txt files</span></span>
- <span data-ttu-id="dcb09-155">Fichiers RTF</span><span class="sxs-lookup"><span data-stu-id="dcb09-155">.rtf files</span></span>
- <span data-ttu-id="dcb09-156">fichiers c</span><span class="sxs-lookup"><span data-stu-id="dcb09-156">.c files</span></span>
- <span data-ttu-id="dcb09-157">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="dcb09-157">.class files</span></span>
- <span data-ttu-id="dcb09-158">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="dcb09-158">.cpp files</span></span>
- <span data-ttu-id="dcb09-159">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="dcb09-159">.cs files</span></span>
- <span data-ttu-id="dcb09-160">fichiers h</span><span class="sxs-lookup"><span data-stu-id="dcb09-160">.h files</span></span>
- <span data-ttu-id="dcb09-161">fichiers .java</span><span class="sxs-lookup"><span data-stu-id="dcb09-161">.java files</span></span>

> [!NOTE]
> <span data-ttu-id="dcb09-p108">La DLP des points de terminaison évalue les fichiers des types indiqués ci-dessus par rapport à la stratégie DLP et applique les actions de protection en conséquence. Tous les fichiers qui correspondent à une stratégie DLP sont audités pour toutes les actions prises en charge, même s’ils ne sont pas bloqués. De plus, l’activité des fichiers effectuée sur les fichiers Word, PowerPoint, Excel, PDF et .csv est auditée par défaut, indépendamment du fait qu’une stratégie DLP existe ou corresponde à ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="dcb09-p108">Endpoint DLP evaluates files of all the above types against the DLP policy and applies protection actions accordingly. All files that match a DLP policy are audited for all supported actions, even if they aren't blocked. In addition, file activity performed on any Word, PowerPoint, Excel, PDF, and .csv file is audited by default, independent of whether a DLP policy exists or matches these files.</span></span>

<span data-ttu-id="dcb09-165">Vous pouvez afficher les alertes liées aux stratégies DLP appliquées sur les appareils de point de terminaison en accédant au [Tableau de bord de Gestion des Alertes DLP.](dlp-configure-view-alerts-policies.md)</span><span class="sxs-lookup"><span data-stu-id="dcb09-165">You can view alerts related to DLP policies enforced on endpoint devices by going to the [DLP Alerts Management Dashboard](dlp-configure-view-alerts-policies.md).</span></span>

![Information d’alerte](../media/Alert-info-1.png)

<span data-ttu-id="dcb09-167">Vous pouvez également afficher les détails de l’événement associé avec des métadonnées complètes dans le même tableau de bord</span><span class="sxs-lookup"><span data-stu-id="dcb09-167">You can also view details of the associated event with rich metadata in the same dashboard</span></span>

![Informations sur l’événement](../media/Event-info-1.png)

<span data-ttu-id="dcb09-169">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, avant même de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="dcb09-169">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dcb09-170">![événements DLP du point de terminaison dans l’explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="dcb09-170">![endpoint dlp events in activity explorer](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span></span>

<span data-ttu-id="dcb09-171">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="dcb09-171">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="dcb09-172">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="dcb09-172">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="dcb09-173">type d’activité</span><span class="sxs-lookup"><span data-stu-id="dcb09-173">activity type</span></span>
- <span data-ttu-id="dcb09-174">IP Client</span><span class="sxs-lookup"><span data-stu-id="dcb09-174">client IP</span></span>
- <span data-ttu-id="dcb09-175">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="dcb09-175">target file path</span></span>
- <span data-ttu-id="dcb09-176">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="dcb09-176">happened timestamp</span></span>
- <span data-ttu-id="dcb09-177">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="dcb09-177">file name</span></span>
- <span data-ttu-id="dcb09-178">utilisateur</span><span class="sxs-lookup"><span data-stu-id="dcb09-178">user</span></span>
- <span data-ttu-id="dcb09-179">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="dcb09-179">file extension</span></span>
- <span data-ttu-id="dcb09-180">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="dcb09-180">file size</span></span>
- <span data-ttu-id="dcb09-181">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="dcb09-181">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="dcb09-182">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="dcb09-182">sha1 value</span></span>
- <span data-ttu-id="dcb09-183">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="dcb09-183">sha256 value</span></span>
- <span data-ttu-id="dcb09-184">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="dcb09-184">previous file name</span></span>
- <span data-ttu-id="dcb09-185">emplacement</span><span class="sxs-lookup"><span data-stu-id="dcb09-185">location</span></span>
- <span data-ttu-id="dcb09-186">parent</span><span class="sxs-lookup"><span data-stu-id="dcb09-186">parent</span></span>
- <span data-ttu-id="dcb09-187">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="dcb09-187">filepath</span></span>
- <span data-ttu-id="dcb09-188">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="dcb09-188">source location type</span></span>
- <span data-ttu-id="dcb09-189">platform</span><span class="sxs-lookup"><span data-stu-id="dcb09-189">platform</span></span>
- <span data-ttu-id="dcb09-190">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="dcb09-190">device name</span></span>
- <span data-ttu-id="dcb09-191">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="dcb09-191">destination location type</span></span>
- <span data-ttu-id="dcb09-192">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="dcb09-192">application that performed the copy</span></span>
- <span data-ttu-id="dcb09-193">ID de l’appareil Microsoft Defender pour point de terminaison (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="dcb09-193">Microsoft Defender for Endpoint device ID (if applicable)</span></span>
- <span data-ttu-id="dcb09-194">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="dcb09-194">removable media device manufacturer</span></span>
- <span data-ttu-id="dcb09-195">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="dcb09-195">removable media device model</span></span>
- <span data-ttu-id="dcb09-196">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="dcb09-196">removable media device serial number</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dcb09-197">![copier dans les attributs d’activités usb](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="dcb09-197">![copy to usb activity attributes](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="dcb09-198">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="dcb09-198">Next steps</span></span>

<span data-ttu-id="dcb09-199">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dcb09-199">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1) [<span data-ttu-id="dcb09-200">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="dcb09-200">Getting started with Microsoft Endpoint data loss prevention </span></span>](endpoint-dlp-getting-started.md)
2) [<span data-ttu-id="dcb09-201">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="dcb09-201">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="dcb09-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcb09-202">See also</span></span>

- [<span data-ttu-id="dcb09-203">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="dcb09-203">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="dcb09-204">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="dcb09-204">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="dcb09-205">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="dcb09-205">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="dcb09-206">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="dcb09-206">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="dcb09-207">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="dcb09-207">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="dcb09-208">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dcb09-208">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- [<span data-ttu-id="dcb09-209">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="dcb09-209">Insider Risk management</span></span>](insider-risk-management.md)
