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
description: 'La prévention des pertes de données du Point de terminaison Microsoft 365 étend la surveillance des activités des fichiers et des actions de protection de ces aux points de terminaison. Les fichiers sont rendus visibles dans les solutions de conformité Microsoft 365 '
ms.openlocfilehash: 1dac32505144c3966ad2219cc69a33ba29f194dc
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49682625"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention"></a><span data-ttu-id="e2782-104">En savoir plus sur la protection contre la perte de données de point de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2782-104">Learn about Microsoft 365 Endpoint data loss prevention</span></span>

<span data-ttu-id="e2782-105">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour contrôler les actions effectuées sur les éléments que vous avez jugés confidentiels et contribuer à empêcher le partage involontaire de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="e2782-105">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items.</span></span> <span data-ttu-id="e2782-106">Pour plus d’informations sur DPL, reportez-vous à [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e2782-106">For more information on DLP, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span>

<span data-ttu-id="e2782-107">**Les points de terminaison contre la protection contre la perte de données** (Endpoint DLP) étend les fonctionnalités de surveillance et de protection des activités de DLP aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2782-107">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="e2782-108">Une fois que les appareils sont intégrés aux solutions de conformité Microsoft 365, les informations relatives à ce que les utilisateurs font avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="e2782-108">Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="e2782-109">Activités de point de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="e2782-109">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="e2782-110">Les points de terminaison Microsoft DLP vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2782-110">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span>


|<span data-ttu-id="e2782-111">activité</span><span class="sxs-lookup"><span data-stu-id="e2782-111">activity</span></span> |<span data-ttu-id="e2782-112">description</span><span class="sxs-lookup"><span data-stu-id="e2782-112">description</span></span>  | <span data-ttu-id="e2782-113">auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-113">auditable/restictable</span></span>|
|---------|---------|---------|
|<span data-ttu-id="e2782-114">téléchargement vers un service en ligne, ou accès par des navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="e2782-114">upload to cloud service, or access by unallowed browsers</span></span>    | <span data-ttu-id="e2782-115">Détecte lorsqu'un utilisateur tente de télécharger un article dans un domaine de service restreint ou d'accéder à un article par le biais d'un navigateur.</span><span class="sxs-lookup"><span data-stu-id="e2782-115">Detects when a user attempts to upload an item to a restricted service domain or access an item through a browser.</span></span>  <span data-ttu-id="e2782-116">S'ils utilisent un navigateur qui est répertorié dans DLP comme étant un navigateur non autorisé, l'activité de téléchargement sera bloquée et l'utilisateur sera redirigé pour utiliser Edge Chromium.</span><span class="sxs-lookup"><span data-stu-id="e2782-116">If they are using a browser that is listed in DLP as an being an unallowed browser, the upload activity will be blocked and the user is redirected to use Edge Chromium.</span></span> <span data-ttu-id="e2782-117">Edge Chromium autorisera ou bloquera alors le téléchargement ou l'accès en fonction de la configuration de la politique DLP</span><span class="sxs-lookup"><span data-stu-id="e2782-117">Edge Chromium will then either allow or block the upload or access based on the DLP policy configuration</span></span>         |<span data-ttu-id="e2782-118">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-118">auditable and restrictable</span></span>|
|<span data-ttu-id="e2782-119">copie vers une autre application</span><span class="sxs-lookup"><span data-stu-id="e2782-119">copy to other app</span></span>    |<span data-ttu-id="e2782-120">Détecte lorsqu'un utilisateur tente de copier des informations d'un élément protégé et de les coller ensuite dans une autre application, un autre processus ou un autre élément.</span><span class="sxs-lookup"><span data-stu-id="e2782-120">Detects when a user attempts to copy information from a protected item and then paste it into another app, process or item.</span></span> <span data-ttu-id="e2782-121">Copier et coller des informations dans la même application, le même processus ou le même élément n'est pas détecté par cette activité.</span><span class="sxs-lookup"><span data-stu-id="e2782-121">Copying and pasting information within the same app, process, or item is not detected by this activity.</span></span>         | <span data-ttu-id="e2782-122">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-122">auditable and restrictable</span></span>|
|<span data-ttu-id="e2782-123">copie sur support USB amovible</span><span class="sxs-lookup"><span data-stu-id="e2782-123">copy to USB removable media</span></span> |<span data-ttu-id="e2782-124">Détecte lorsqu'un utilisateur tente de copier un élément ou une information sur un support amovible ou un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="e2782-124">Detects when a user attempts to copy an item or information to removable media or USB device.</span></span>         | <span data-ttu-id="e2782-125">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-125">auditable and restrictable</span></span>|
|<span data-ttu-id="e2782-126">copier vers un partage réseau</span><span class="sxs-lookup"><span data-stu-id="e2782-126">copy to a network share</span></span>    |<span data-ttu-id="e2782-127">Détecte lorsqu'un utilisateur tente de copier un élément vers un partage réseau ou un disque réseau mappé</span><span class="sxs-lookup"><span data-stu-id="e2782-127">Detects when a user attempts to copy an item to a network share or mapped network drive</span></span>         |<span data-ttu-id="e2782-128">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-128">auditable and restrictable</span></span>|
|<span data-ttu-id="e2782-129">imprimer un document</span><span class="sxs-lookup"><span data-stu-id="e2782-129">print a document</span></span>    |<span data-ttu-id="e2782-130">Détecte lorsqu'un utilisateur tente d'imprimer un élément protégé sur une imprimante locale ou réseau.</span><span class="sxs-lookup"><span data-stu-id="e2782-130">Detects when a user attempts to print a protected item to a local or network printer.</span></span>| <span data-ttu-id="e2782-131">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="e2782-131">auditable and restrictable</span></span>         |
|<span data-ttu-id="e2782-132">créer un élément</span><span class="sxs-lookup"><span data-stu-id="e2782-132">create an item</span></span>|<span data-ttu-id="e2782-133">Détecte lorsqu'un utilisateur crée un article</span><span class="sxs-lookup"><span data-stu-id="e2782-133">Detects when a user creates an item</span></span>| <span data-ttu-id="e2782-134">vérifiable</span><span class="sxs-lookup"><span data-stu-id="e2782-134">auditable</span></span>|
|<span data-ttu-id="e2782-135">renommer un article</span><span class="sxs-lookup"><span data-stu-id="e2782-135">rename an item</span></span>|<span data-ttu-id="e2782-136">Détecte lorsqu'un utilisateur renomme un article</span><span class="sxs-lookup"><span data-stu-id="e2782-136">Detects when a user renames an item</span></span>| <span data-ttu-id="e2782-137">vérifiable</span><span class="sxs-lookup"><span data-stu-id="e2782-137">auditable</span></span>|


## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="e2782-138">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="e2782-138">What's different in Endpoint DLP</span></span>

<span data-ttu-id="e2782-139">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="e2782-139">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="e2782-140">Activation de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="e2782-140">Enabling Device management</span></span>

<span data-ttu-id="e2782-141">La gestion des appareils est une fonctionnalité qui permet d’assembler la télémétrie à partir d’appareils et de l’intégrer à des solutions de conformité Microsoft 365 telles que point de terminaison DLP et [ gestionnaire des risques Insider](insider-risk-management.md).</span><span class="sxs-lookup"><span data-stu-id="e2782-141">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md).</span></span> <span data-ttu-id="e2782-142">Vous devez intégrer tous les appareils que vous voulez utiliser en tant qu’emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="e2782-142">You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2782-143">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="e2782-143">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

<span data-ttu-id="e2782-144">L’intégration et déclassement sont gérés à l’aide de scripts téléchargés à partir du centre de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="e2782-144">Onboarding and offboarding are handled via scripts you download from the Device management center.</span></span> <span data-ttu-id="e2782-145">Le centre inclut des scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="e2782-145">The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="e2782-146">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="e2782-146">local script (up to 10 machines)</span></span>
- <span data-ttu-id="e2782-147">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e2782-147">Group policy</span></span>
- <span data-ttu-id="e2782-148">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="e2782-148">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="e2782-149">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="e2782-149">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="e2782-150">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="e2782-150">VDI onboarding scripts for non-persistent machines</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2782-151">![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span><span class="sxs-lookup"><span data-stu-id="e2782-151">![device onboarding page](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span></span>

 <span data-ttu-id="e2782-152">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="e2782-152">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="e2782-153">Si vous avez des appareils intégrés via [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="e2782-153">If you have onboarded devices through [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2782-154">![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)</span><span class="sxs-lookup"><span data-stu-id="e2782-154">![managed devices list](../media/endpoint-dlp-learn-about-2-device-list.png)</span></span>

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="e2782-155">Affichage des données DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e2782-155">Viewing Endpoint DLP data</span></span>

 <span data-ttu-id="e2782-156">Le DLP du point de terminaison contrôle l’activité basée sur le type MIME, de sorte que les activités sont capturées même si l’extension de fichier est modifiée.</span><span class="sxs-lookup"><span data-stu-id="e2782-156">Endpoint DLP monitors activity-based on MIME type, so activities will be captured even if the file extension is changed.</span></span> <span data-ttu-id="e2782-157">Pour l’instant, les types de fichiers suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="e2782-157">At this time the following file types are supported:</span></span>

- <span data-ttu-id="e2782-158">Fichiers Word</span><span class="sxs-lookup"><span data-stu-id="e2782-158">Word files</span></span>
- <span data-ttu-id="e2782-159">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="e2782-159">PowerPoint files</span></span>
- <span data-ttu-id="e2782-160">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="e2782-160">Excel files</span></span>
- <span data-ttu-id="e2782-161">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="e2782-161">PDF files</span></span>
- <span data-ttu-id="e2782-162">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="e2782-162">.csv files</span></span>
- <span data-ttu-id="e2782-163">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="e2782-163">.tsv files</span></span>
- <span data-ttu-id="e2782-164">fichiers .txt</span><span class="sxs-lookup"><span data-stu-id="e2782-164">.txt files</span></span>
- <span data-ttu-id="e2782-165">Fichiers RTF</span><span class="sxs-lookup"><span data-stu-id="e2782-165">.rtf files</span></span>
- <span data-ttu-id="e2782-166">fichiers c</span><span class="sxs-lookup"><span data-stu-id="e2782-166">.c files</span></span>
- <span data-ttu-id="e2782-167">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="e2782-167">.class files</span></span>
- <span data-ttu-id="e2782-168">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="e2782-168">.cpp files</span></span>
- <span data-ttu-id="e2782-169">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="e2782-169">.cs files</span></span>
- <span data-ttu-id="e2782-170">fichiers h</span><span class="sxs-lookup"><span data-stu-id="e2782-170">.h files</span></span>
- <span data-ttu-id="e2782-171">fichiers Java</span><span class="sxs-lookup"><span data-stu-id="e2782-171">.java files</span></span>

> [!NOTE]
> <span data-ttu-id="e2782-172">Le DLP du Point de terminaison évalue les fichiers de tous les types précités par rapport à la stratégie DLP et applique les actions de protection en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e2782-172">Endpoint DLP evaluates files of all the above types against the DLP policy and applies protection actions accordingly.</span></span> <span data-ttu-id="e2782-173">Tous les fichiers qui correspondent à une stratégie DLP sont audités pour toutes les actions prises en charge, même si elles ne sont pas bloquées.</span><span class="sxs-lookup"><span data-stu-id="e2782-173">All files that match a DLP policy are audited for all supported actions, even if they aren't blocked.</span></span> <span data-ttu-id="e2782-174">De plus, l’activité des fichiers effectuée sur un fichier Word, PowerPoint, Excel, PDF et. csv est auditée par défaut, indépendamment du fait qu’une stratégie DLP existe ou qu’elle corresponde à ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2782-174">In addition, file activity performed on any Word, PowerPoint, Excel, PDF, and .csv file is audited by default, independent of whether a DLP policy exists or matches these files.</span></span>

<span data-ttu-id="e2782-175">Vous pouvez afficher les alertes liées aux stratégies DLP appliquées sur les appareils de point de terminaison en accédant au [Tableau de bord de Gestion des Alertes DLP.](dlp-configure-view-alerts-policies.md)</span><span class="sxs-lookup"><span data-stu-id="e2782-175">You can view alerts related to DLP policies enforced on endpoint devices by going to the [DLP Alerts Management Dashboard](dlp-configure-view-alerts-policies.md).</span></span>

![Information d’alerte](../media/Alert-info-1.png)

<span data-ttu-id="e2782-177">Vous pouvez également afficher les détails de l’événement associé avec des métadonnées complètes dans le même tableau de bord</span><span class="sxs-lookup"><span data-stu-id="e2782-177">You can also view details of the associated event with rich metadata in the same dashboard</span></span>

![Informations sur l’événement](../media/Event-info-1.png)

<span data-ttu-id="e2782-179">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, même avant de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="e2782-179">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2782-180">![événements DLP du point de terminaison dans l’explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="e2782-180">![endpoint dlp events in activity explorer](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span></span>

<span data-ttu-id="e2782-181">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="e2782-181">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="e2782-182">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="e2782-182">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="e2782-183">type d’activité</span><span class="sxs-lookup"><span data-stu-id="e2782-183">activity type</span></span>
- <span data-ttu-id="e2782-184">IP Client</span><span class="sxs-lookup"><span data-stu-id="e2782-184">client IP</span></span>
- <span data-ttu-id="e2782-185">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="e2782-185">target file path</span></span>
- <span data-ttu-id="e2782-186">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="e2782-186">happened timestamp</span></span>
- <span data-ttu-id="e2782-187">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="e2782-187">file name</span></span>
- <span data-ttu-id="e2782-188">utilisateur</span><span class="sxs-lookup"><span data-stu-id="e2782-188">user</span></span>
- <span data-ttu-id="e2782-189">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="e2782-189">file extension</span></span>
- <span data-ttu-id="e2782-190">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="e2782-190">file size</span></span>
- <span data-ttu-id="e2782-191">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="e2782-191">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="e2782-192">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="e2782-192">sha1 value</span></span>
- <span data-ttu-id="e2782-193">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="e2782-193">sha256 value</span></span>
- <span data-ttu-id="e2782-194">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="e2782-194">previous file name</span></span>
- <span data-ttu-id="e2782-195">emplacement</span><span class="sxs-lookup"><span data-stu-id="e2782-195">location</span></span>
- <span data-ttu-id="e2782-196">parent</span><span class="sxs-lookup"><span data-stu-id="e2782-196">parent</span></span>
- <span data-ttu-id="e2782-197">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e2782-197">filepath</span></span>
- <span data-ttu-id="e2782-198">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="e2782-198">source location type</span></span>
- <span data-ttu-id="e2782-199">platform</span><span class="sxs-lookup"><span data-stu-id="e2782-199">platform</span></span>
- <span data-ttu-id="e2782-200">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="e2782-200">device name</span></span>
- <span data-ttu-id="e2782-201">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="e2782-201">destination location type</span></span>
- <span data-ttu-id="e2782-202">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="e2782-202">application that performed the copy</span></span>
- <span data-ttu-id="e2782-203">ID de l’appareil Microsoft Defender pour point de terminaison (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="e2782-203">Microsoft Defender for Endpoint device ID (if applicable)</span></span>
- <span data-ttu-id="e2782-204">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="e2782-204">removable media device manufacturer</span></span>
- <span data-ttu-id="e2782-205">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="e2782-205">removable media device model</span></span>
- <span data-ttu-id="e2782-206">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="e2782-206">removable media device serial number</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2782-207">![copier dans les attributs d’activités usb](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="e2782-207">![copy to usb activity attributes](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="e2782-208">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e2782-208">Next steps</span></span>

<span data-ttu-id="e2782-209">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2782-209">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1) [<span data-ttu-id="e2782-210">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="e2782-210">Getting started with Microsoft Endpoint data loss prevention </span></span>](endpoint-dlp-getting-started.md)
2) [<span data-ttu-id="e2782-211">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="e2782-211">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="e2782-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2782-212">See also</span></span>

- [<span data-ttu-id="e2782-213">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="e2782-213">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="e2782-214">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="e2782-214">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="e2782-215">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="e2782-215">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="e2782-216">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="e2782-216">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="e2782-217">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="e2782-217">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="e2782-218">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e2782-218">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- [<span data-ttu-id="e2782-219">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="e2782-219">Insider Risk management</span></span>](insider-risk-management.md)
