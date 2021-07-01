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
ms.openlocfilehash: 39474f54440ba33c8d7140981c1495a5c46bf0fc
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53226682"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention"></a><span data-ttu-id="2ce73-104">En savoir plus sur la protection contre la perte de données de point de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2ce73-104">Learn about Microsoft 365 Endpoint data loss prevention</span></span>

<span data-ttu-id="2ce73-105">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour contrôler les actions effectuées sur les éléments que vous avez jugés confidentiels et contribuer à empêcher le partage involontaire de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="2ce73-105">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items.</span></span> <span data-ttu-id="2ce73-106">Si vous souhaitez en savoir plus sur DLP, veuillez consulter la rubrique [En savoir plus sur la protection contre la perte de données](dlp-learn-about-dlp.md).</span><span class="sxs-lookup"><span data-stu-id="2ce73-106">For more information on DLP, see [Learn about data loss prevention](dlp-learn-about-dlp.md).</span></span>

<span data-ttu-id="2ce73-107">**Les points de terminaison contre la protection contre la perte de données** (Endpoint DLP) étend les fonctionnalités de surveillance et de protection des activités de DLP aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2ce73-107">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="2ce73-108">Une fois que les appareils sont intégrés aux solutions de conformité Microsoft 365, les informations relatives à ce que les utilisateurs font avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="2ce73-108">Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="2ce73-109">Activités de point de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="2ce73-109">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="2ce73-110">Les points de terminaison Microsoft DLP vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2ce73-110">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span>

|<span data-ttu-id="2ce73-111">Activité</span><span class="sxs-lookup"><span data-stu-id="2ce73-111">Activity</span></span> |<span data-ttu-id="2ce73-112">Description</span><span class="sxs-lookup"><span data-stu-id="2ce73-112">Description</span></span>  | <span data-ttu-id="2ce73-113">Auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-113">Auditable/restictable</span></span>|
|---------|---------|---------|
|<span data-ttu-id="2ce73-114">téléchargement vers un service en ligne, ou accès par des navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="2ce73-114">upload to cloud service, or access by unallowed browsers</span></span>    | <span data-ttu-id="2ce73-115">Détecte lorsqu'un utilisateur tente de télécharger un article dans un domaine de service restreint ou d'accéder à un article par le biais d'un navigateur.</span><span class="sxs-lookup"><span data-stu-id="2ce73-115">Detects when a user attempts to upload an item to a restricted service domain or access an item through a browser.</span></span>  <span data-ttu-id="2ce73-116">S'ils utilisent un navigateur qui est répertorié dans DLP comme étant un navigateur non autorisé, l'activité de téléchargement sera bloquée et l'utilisateur sera redirigé pour utiliser Edge Chromium.</span><span class="sxs-lookup"><span data-stu-id="2ce73-116">If they are using a browser that is listed in DLP as an being an unallowed browser, the upload activity will be blocked and the user is redirected to use Edge Chromium.</span></span> <span data-ttu-id="2ce73-117">Edge Chromium autorisera ou bloquera alors le téléchargement ou l'accès en fonction de la configuration de la politique DLP</span><span class="sxs-lookup"><span data-stu-id="2ce73-117">Edge Chromium will then either allow or block the upload or access based on the DLP policy configuration</span></span>         |<span data-ttu-id="2ce73-118">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-118">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-119">copie vers une autre application</span><span class="sxs-lookup"><span data-stu-id="2ce73-119">copy to other app</span></span>    |<span data-ttu-id="2ce73-120">Détecte lorsqu'un utilisateur tente de copier des informations d'un élément protégé et de les coller ensuite dans une autre application, un autre processus ou un autre élément.</span><span class="sxs-lookup"><span data-stu-id="2ce73-120">Detects when a user attempts to copy information from a protected item and then paste it into another app, process or item.</span></span> <span data-ttu-id="2ce73-121">Copier et coller des informations dans la même application, le même processus ou le même élément n'est pas détecté par cette activité.</span><span class="sxs-lookup"><span data-stu-id="2ce73-121">Copying and pasting information within the same app, process, or item is not detected by this activity.</span></span>         | <span data-ttu-id="2ce73-122">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-122">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-123">copie sur support USB amovible</span><span class="sxs-lookup"><span data-stu-id="2ce73-123">copy to USB removable media</span></span> |<span data-ttu-id="2ce73-124">Détecte lorsqu'un utilisateur tente de copier un élément ou une information sur un support amovible ou un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="2ce73-124">Detects when a user attempts to copy an item or information to removable media or USB device.</span></span>         | <span data-ttu-id="2ce73-125">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-125">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-126">copier vers un partage réseau</span><span class="sxs-lookup"><span data-stu-id="2ce73-126">copy to a network share</span></span>    |<span data-ttu-id="2ce73-127">Détecte lorsqu'un utilisateur tente de copier un élément vers un partage réseau ou un disque réseau mappé</span><span class="sxs-lookup"><span data-stu-id="2ce73-127">Detects when a user attempts to copy an item to a network share or mapped network drive</span></span>         |<span data-ttu-id="2ce73-128">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-128">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-129">imprimer un document</span><span class="sxs-lookup"><span data-stu-id="2ce73-129">print a document</span></span>    |<span data-ttu-id="2ce73-130">Détecte lorsqu'un utilisateur tente d'imprimer un élément protégé sur une imprimante locale ou réseau.</span><span class="sxs-lookup"><span data-stu-id="2ce73-130">Detects when a user attempts to print a protected item to a local or network printer.</span></span>| <span data-ttu-id="2ce73-131">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-131">auditable and restrictable</span></span>         |
|<span data-ttu-id="2ce73-132">copier vers une session à distance</span><span class="sxs-lookup"><span data-stu-id="2ce73-132">copy to a remote session</span></span>|<span data-ttu-id="2ce73-133">Détecte lorsqu'un utilisateur tente de copier un élément vers une session de bureau à distance</span><span class="sxs-lookup"><span data-stu-id="2ce73-133">Detects when a user attempts to copy an item to a remote desktop session</span></span> |  <span data-ttu-id="2ce73-134">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-134">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-135">copier vers appareil Bluetooth</span><span class="sxs-lookup"><span data-stu-id="2ce73-135">copy to a Bluetooth device</span></span>|<span data-ttu-id="2ce73-136">Détecte lorsqu'un utilisateur tente de copier un élément vers une application Bluetooth non autorisée (telle que définie dans la liste des applications Bluetooth non autorisées dans les paramètres DLP de point de terminaison).</span><span class="sxs-lookup"><span data-stu-id="2ce73-136">Detects when a user attempts to copy an item to an unallowed Bluetooth app (as defined in the list of unallowed Bluetooth aps in Endpoint DLP settings).</span></span>| <span data-ttu-id="2ce73-137">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="2ce73-137">auditable and restrictable</span></span>|
|<span data-ttu-id="2ce73-138">créer un élément</span><span class="sxs-lookup"><span data-stu-id="2ce73-138">create an item</span></span>|<span data-ttu-id="2ce73-139">Détecte lorsqu'un utilisateur crée un article</span><span class="sxs-lookup"><span data-stu-id="2ce73-139">Detects when a user creates an item</span></span>| <span data-ttu-id="2ce73-140">vérifiable</span><span class="sxs-lookup"><span data-stu-id="2ce73-140">auditable</span></span>|
|<span data-ttu-id="2ce73-141">renommer un article</span><span class="sxs-lookup"><span data-stu-id="2ce73-141">rename an item</span></span>|<span data-ttu-id="2ce73-142">Détecte lorsqu'un utilisateur renomme un article</span><span class="sxs-lookup"><span data-stu-id="2ce73-142">Detects when a user renames an item</span></span>| <span data-ttu-id="2ce73-143">vérifiable</span><span class="sxs-lookup"><span data-stu-id="2ce73-143">auditable</span></span>|

## <a name="monitored-files"></a><span data-ttu-id="2ce73-144">Fichiers analysées</span><span class="sxs-lookup"><span data-stu-id="2ce73-144">Monitored files</span></span>

<span data-ttu-id="2ce73-145">La DLP de point du terminaison prend en charge la surveillance de ces types de fichiers :</span><span class="sxs-lookup"><span data-stu-id="2ce73-145">Endpoint DLP supports monitoring of these file types:</span></span>

- <span data-ttu-id="2ce73-146">Fichiers Word</span><span class="sxs-lookup"><span data-stu-id="2ce73-146">Word files</span></span>
- <span data-ttu-id="2ce73-147">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="2ce73-147">PowerPoint files</span></span>
- <span data-ttu-id="2ce73-148">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="2ce73-148">Excel files</span></span>
- <span data-ttu-id="2ce73-149">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="2ce73-149">PDF files</span></span>
- <span data-ttu-id="2ce73-150">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="2ce73-150">.csv files</span></span>
- <span data-ttu-id="2ce73-151">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="2ce73-151">.tsv files</span></span>
- <span data-ttu-id="2ce73-152">fichiers .txt</span><span class="sxs-lookup"><span data-stu-id="2ce73-152">.txt files</span></span>
- <span data-ttu-id="2ce73-153">Fichiers RTF</span><span class="sxs-lookup"><span data-stu-id="2ce73-153">.rtf files</span></span>
- <span data-ttu-id="2ce73-154">fichiers c</span><span class="sxs-lookup"><span data-stu-id="2ce73-154">.c files</span></span>
- <span data-ttu-id="2ce73-155">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="2ce73-155">.class files</span></span>
- <span data-ttu-id="2ce73-156">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="2ce73-156">.cpp files</span></span>
- <span data-ttu-id="2ce73-157">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="2ce73-157">.cs files</span></span>
- <span data-ttu-id="2ce73-158">fichiers h</span><span class="sxs-lookup"><span data-stu-id="2ce73-158">.h files</span></span>
- <span data-ttu-id="2ce73-159">fichiers Java</span><span class="sxs-lookup"><span data-stu-id="2ce73-159">.java files</span></span>

<span data-ttu-id="2ce73-160">Par défaut, la DLP du point de terminaison audite les activités de ces types de fichiers, même s’il n’existe pas de correspondance de stratégie.</span><span class="sxs-lookup"><span data-stu-id="2ce73-160">By default, endpoint DLP audits the activities for these file types, even if there isn't a policy match.</span></span> <span data-ttu-id="2ce73-161">Si vous souhaitez surveiller les données des correspondances de stratégie uniquement, vous pouvez désactiver l'option **Toujours auditer l’activité du fichier pour les appareils** dans les paramètres globaux DLP du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2ce73-161">If you only want monitoring data from policy matches, you can turn off the **Always audit file activity for devices** in the endpoint DLP global settings.</span></span> <span data-ttu-id="2ce73-162">Si ce paramètre est utilisé, les activités sur les fichiers Word, PowerPoint, Excel, PDF, et .csv sont toujours auditées, même si l’appareil n’est ciblé par aucune stratégie.</span><span class="sxs-lookup"><span data-stu-id="2ce73-162">If this setting is on, activities on any Word, PowerPoint, Excel, PDF, and .csv file are always audited even if the device is not targeted by any policy.</span></span>

<span data-ttu-id="2ce73-163">Le DLP du point de terminaison contrôle l’activité basée sur le type MIME, de sorte que les activités sont capturées même si l’extension de fichier est modifiée.</span><span class="sxs-lookup"><span data-stu-id="2ce73-163">Endpoint DLP monitors activity-based on MIME type, so activities will be captured even if the file extension is changed.</span></span>

## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="2ce73-164">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="2ce73-164">What's different in Endpoint DLP</span></span>

<span data-ttu-id="2ce73-165">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="2ce73-165">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="2ce73-166">Activation de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="2ce73-166">Enabling Device management</span></span>

<span data-ttu-id="2ce73-167">La gestion des appareils est une fonctionnalité qui permet d’assembler la télémétrie à partir d’appareils et de l’intégrer à des solutions de conformité Microsoft 365 telles que point de terminaison DLP et [ gestionnaire des risques Insider](insider-risk-management.md).</span><span class="sxs-lookup"><span data-stu-id="2ce73-167">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md).</span></span> <span data-ttu-id="2ce73-168">Vous devez intégrer tous les appareils que vous voulez utiliser en tant qu’emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="2ce73-168">You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-169">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-169">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

<span data-ttu-id="2ce73-170">L’intégration et déclassement sont gérés à l’aide de scripts téléchargés à partir du centre de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="2ce73-170">Onboarding and offboarding are handled via scripts you download from the Device management center.</span></span> <span data-ttu-id="2ce73-171">Le centre inclut des scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="2ce73-171">The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="2ce73-172">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="2ce73-172">local script (up to 10 machines)</span></span>
- <span data-ttu-id="2ce73-173">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2ce73-173">Group policy</span></span>
- <span data-ttu-id="2ce73-174">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ce73-174">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="2ce73-175">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="2ce73-175">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="2ce73-176">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="2ce73-176">VDI onboarding scripts for non-persistent machines</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-177">![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-177">![device onboarding page](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span></span>

 <span data-ttu-id="2ce73-178">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="2ce73-178">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="2ce73-179">Si vous avez des appareils intégrés via [Microsoft Defender pour point de terminaison](/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="2ce73-179">If you have onboarded devices through [Microsoft Defender for Endpoint](/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-180">![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-180">![managed devices list](../media/endpoint-dlp-learn-about-2-device-list.png)</span></span>

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="2ce73-181">Affichage des données DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2ce73-181">Viewing Endpoint DLP data</span></span>

<span data-ttu-id="2ce73-182">Vous pouvez afficher les alertes liées aux stratégies DLP appliquées sur les appareils de point de terminaison en accédant au [Tableau de bord de Gestion des Alertes DLP.](dlp-configure-view-alerts-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2ce73-182">You can view alerts related to DLP policies enforced on endpoint devices by going to the [DLP Alerts Management Dashboard](dlp-configure-view-alerts-policies.md).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-183">![Information d’alerte](../media/Alert-info-1.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-183">![Alert info](../media/Alert-info-1.png)</span></span>

<span data-ttu-id="2ce73-184">Vous pouvez également afficher les détails de l’événement associé avec des métadonnées complètes dans le même tableau de bord</span><span class="sxs-lookup"><span data-stu-id="2ce73-184">You can also view details of the associated event with rich metadata in the same dashboard</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-185">![Informations sur un événement](../media/Event-info-1.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-185">![event info](../media/Event-info-1.png)</span></span>

<span data-ttu-id="2ce73-186">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, même avant de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="2ce73-186">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-187">![événements DLP du point de terminaison dans l’explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-187">![endpoint dlp events in activity explorer](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span></span>

<span data-ttu-id="2ce73-188">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="2ce73-188">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="2ce73-189">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="2ce73-189">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="2ce73-190">type d’activité</span><span class="sxs-lookup"><span data-stu-id="2ce73-190">activity type</span></span>
- <span data-ttu-id="2ce73-191">IP Client</span><span class="sxs-lookup"><span data-stu-id="2ce73-191">client IP</span></span>
- <span data-ttu-id="2ce73-192">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="2ce73-192">target file path</span></span>
- <span data-ttu-id="2ce73-193">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="2ce73-193">happened timestamp</span></span>
- <span data-ttu-id="2ce73-194">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="2ce73-194">file name</span></span>
- <span data-ttu-id="2ce73-195">utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ce73-195">user</span></span>
- <span data-ttu-id="2ce73-196">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="2ce73-196">file extension</span></span>
- <span data-ttu-id="2ce73-197">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="2ce73-197">file size</span></span>
- <span data-ttu-id="2ce73-198">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="2ce73-198">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="2ce73-199">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="2ce73-199">sha1 value</span></span>
- <span data-ttu-id="2ce73-200">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="2ce73-200">sha256 value</span></span>
- <span data-ttu-id="2ce73-201">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="2ce73-201">previous file name</span></span>
- <span data-ttu-id="2ce73-202">emplacement</span><span class="sxs-lookup"><span data-stu-id="2ce73-202">location</span></span>
- <span data-ttu-id="2ce73-203">parent</span><span class="sxs-lookup"><span data-stu-id="2ce73-203">parent</span></span>
- <span data-ttu-id="2ce73-204">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2ce73-204">filepath</span></span>
- <span data-ttu-id="2ce73-205">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="2ce73-205">source location type</span></span>
- <span data-ttu-id="2ce73-206">platform</span><span class="sxs-lookup"><span data-stu-id="2ce73-206">platform</span></span>
- <span data-ttu-id="2ce73-207">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="2ce73-207">device name</span></span>
- <span data-ttu-id="2ce73-208">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="2ce73-208">destination location type</span></span>
- <span data-ttu-id="2ce73-209">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="2ce73-209">application that performed the copy</span></span>
- <span data-ttu-id="2ce73-210">ID de l’appareil Microsoft Defender pour point de terminaison (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="2ce73-210">Microsoft Defender for Endpoint device ID (if applicable)</span></span>
- <span data-ttu-id="2ce73-211">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="2ce73-211">removable media device manufacturer</span></span>
- <span data-ttu-id="2ce73-212">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="2ce73-212">removable media device model</span></span>
- <span data-ttu-id="2ce73-213">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="2ce73-213">removable media device serial number</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2ce73-214">![copier dans les attributs d’activités usb](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="2ce73-214">![copy to usb activity attributes](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="2ce73-215">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2ce73-215">Next steps</span></span>

<span data-ttu-id="2ce73-216">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ce73-216">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1. [<span data-ttu-id="2ce73-217">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="2ce73-217">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
2. [<span data-ttu-id="2ce73-218">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="2ce73-218">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="2ce73-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce73-219">See also</span></span>

- [<span data-ttu-id="2ce73-220">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="2ce73-220">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="2ce73-221">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="2ce73-221">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="2ce73-222">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="2ce73-222">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="2ce73-223">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="2ce73-223">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="2ce73-224">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="2ce73-224">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="2ce73-225">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2ce73-225">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)
- [<span data-ttu-id="2ce73-226">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="2ce73-226">Insider Risk management</span></span>](insider-risk-management.md)
