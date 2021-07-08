---
title: Découvrir la protection contre la perte de données des point de terminaison de Microsoft 365
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
ms.openlocfilehash: c97368dd48515dc787dbac66aa93844889efbdbc
ms.sourcegitcommit: 8b0718f5607ab509092cb80bda854010d885c54f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53314415"
---
# <a name="learn-about-microsoft-365-endpoint-data-loss-prevention"></a><span data-ttu-id="4c0db-104">En savoir plus sur la protection contre la perte de données de point de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4c0db-104">Learn about Microsoft 365 Endpoint data loss prevention</span></span>

<span data-ttu-id="4c0db-105">Vous pouvez utiliser la protection contre la perte de données (DLP) de Microsoft 365 pour contrôler les actions effectuées sur les éléments que vous avez jugés confidentiels et contribuer à empêcher le partage involontaire de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="4c0db-105">You can use Microsoft 365 data loss prevention (DLP) to monitor the actions that are being taken on items you've determined to be sensitive and to help prevent the unintentional sharing of those items.</span></span> <span data-ttu-id="4c0db-106">Si vous souhaitez en savoir plus sur DLP, veuillez consulter la rubrique [En savoir plus sur la protection contre la perte de données](dlp-learn-about-dlp.md).</span><span class="sxs-lookup"><span data-stu-id="4c0db-106">For more information on DLP, see [Learn about data loss prevention](dlp-learn-about-dlp.md).</span></span>

<span data-ttu-id="4c0db-107">**Les points de terminaison contre la protection contre la perte de données** (Endpoint DLP) étend les fonctionnalités de surveillance et de protection des activités de DLP aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4c0db-107">**Endpoint data loss prevention** (Endpoint DLP) extends the activity monitoring and protection capabilities of DLP to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="4c0db-108">Une fois que les appareils sont intégrés aux solutions de conformité Microsoft 365, les informations relatives à ce que les utilisateurs font avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="4c0db-108">Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

> [!TIP]
> <span data-ttu-id="4c0db-109">Si vous recherchez le contrôle d’appareil pour le stockage amovible, consultez [Contrôle d’accès Stockage amovible Contrôle d’appareil Microsoft Defender pour Point de terminaison ](../security/defender-endpoint/device-control-removable-storage-access-control.md#microsoft-defender-for-endpoint-device-control-removable-storage-access-control).</span><span class="sxs-lookup"><span data-stu-id="4c0db-109">If you are looking for device control for removable storage, see [Microsoft Defender for Endpoint Device Control Removable Storage Access Control](../security/defender-endpoint/device-control-removable-storage-access-control.md#microsoft-defender-for-endpoint-device-control-removable-storage-access-control).</span></span>

## <a name="endpoint-activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="4c0db-110">Activités de point de terminaison que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="4c0db-110">Endpoint activities you can monitor and take action on</span></span>

<span data-ttu-id="4c0db-111">Les points de terminaison Microsoft DLP vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4c0db-111">Microsoft Endpoint DLP enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span>

|<span data-ttu-id="4c0db-112">Activité</span><span class="sxs-lookup"><span data-stu-id="4c0db-112">Activity</span></span> |<span data-ttu-id="4c0db-113">Description</span><span class="sxs-lookup"><span data-stu-id="4c0db-113">Description</span></span>  | <span data-ttu-id="4c0db-114">Auditable/restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-114">Auditable/restictable</span></span>|
|---------|---------|---------|
|<span data-ttu-id="4c0db-115">téléchargement vers un service en ligne, ou accès par des navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="4c0db-115">upload to cloud service, or access by unallowed browsers</span></span>    | <span data-ttu-id="4c0db-116">Détecte lorsqu'un utilisateur tente de télécharger un article dans un domaine de service restreint ou d'accéder à un article par le biais d'un navigateur.</span><span class="sxs-lookup"><span data-stu-id="4c0db-116">Detects when a user attempts to upload an item to a restricted service domain or access an item through a browser.</span></span>  <span data-ttu-id="4c0db-117">S'ils utilisent un navigateur qui est répertorié dans DLP comme étant un navigateur non autorisé, l'activité de téléchargement sera bloquée et l'utilisateur sera redirigé pour utiliser Edge Chromium.</span><span class="sxs-lookup"><span data-stu-id="4c0db-117">If they are using a browser that is listed in DLP as an being an unallowed browser, the upload activity will be blocked and the user is redirected to use Edge Chromium.</span></span> <span data-ttu-id="4c0db-118">Edge Chromium autorisera ou bloquera alors le téléchargement ou l'accès en fonction de la configuration de la politique DLP</span><span class="sxs-lookup"><span data-stu-id="4c0db-118">Edge Chromium will then either allow or block the upload or access based on the DLP policy configuration</span></span>         |<span data-ttu-id="4c0db-119">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-119">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-120">copie vers une autre application</span><span class="sxs-lookup"><span data-stu-id="4c0db-120">copy to other app</span></span>    |<span data-ttu-id="4c0db-121">Détecte lorsqu'un utilisateur tente de copier des informations d'un élément protégé et de les coller ensuite dans une autre application, un autre processus ou un autre élément.</span><span class="sxs-lookup"><span data-stu-id="4c0db-121">Detects when a user attempts to copy information from a protected item and then paste it into another app, process or item.</span></span> <span data-ttu-id="4c0db-122">Copier et coller des informations dans la même application, le même processus ou le même élément n'est pas détecté par cette activité.</span><span class="sxs-lookup"><span data-stu-id="4c0db-122">Copying and pasting information within the same app, process, or item is not detected by this activity.</span></span>         | <span data-ttu-id="4c0db-123">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-123">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-124">copie sur support USB amovible</span><span class="sxs-lookup"><span data-stu-id="4c0db-124">copy to USB removable media</span></span> |<span data-ttu-id="4c0db-125">Détecte lorsqu'un utilisateur tente de copier un élément ou une information sur un support amovible ou un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="4c0db-125">Detects when a user attempts to copy an item or information to removable media or USB device.</span></span>         | <span data-ttu-id="4c0db-126">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-126">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-127">copier vers un partage réseau</span><span class="sxs-lookup"><span data-stu-id="4c0db-127">copy to a network share</span></span>    |<span data-ttu-id="4c0db-128">Détecte lorsqu'un utilisateur tente de copier un élément vers un partage réseau ou un disque réseau mappé</span><span class="sxs-lookup"><span data-stu-id="4c0db-128">Detects when a user attempts to copy an item to a network share or mapped network drive</span></span>         |<span data-ttu-id="4c0db-129">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-129">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-130">imprimer un document</span><span class="sxs-lookup"><span data-stu-id="4c0db-130">print a document</span></span>    |<span data-ttu-id="4c0db-131">Détecte lorsqu'un utilisateur tente d'imprimer un élément protégé sur une imprimante locale ou réseau.</span><span class="sxs-lookup"><span data-stu-id="4c0db-131">Detects when a user attempts to print a protected item to a local or network printer.</span></span>| <span data-ttu-id="4c0db-132">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-132">auditable and restrictable</span></span>         |
|<span data-ttu-id="4c0db-133">copier vers une session à distance</span><span class="sxs-lookup"><span data-stu-id="4c0db-133">copy to a remote session</span></span>|<span data-ttu-id="4c0db-134">Détecte lorsqu'un utilisateur tente de copier un élément vers une session de bureau à distance</span><span class="sxs-lookup"><span data-stu-id="4c0db-134">Detects when a user attempts to copy an item to a remote desktop session</span></span> |  <span data-ttu-id="4c0db-135">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-135">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-136">copier vers appareil Bluetooth</span><span class="sxs-lookup"><span data-stu-id="4c0db-136">copy to a Bluetooth device</span></span>|<span data-ttu-id="4c0db-137">Détecte lorsqu'un utilisateur tente de copier un élément vers une application Bluetooth non autorisée (telle que définie dans la liste des applications Bluetooth non autorisées dans les paramètres DLP de point de terminaison).</span><span class="sxs-lookup"><span data-stu-id="4c0db-137">Detects when a user attempts to copy an item to an unallowed Bluetooth app (as defined in the list of unallowed Bluetooth aps in Endpoint DLP settings).</span></span>| <span data-ttu-id="4c0db-138">auditable et restreint</span><span class="sxs-lookup"><span data-stu-id="4c0db-138">auditable and restrictable</span></span>|
|<span data-ttu-id="4c0db-139">créer un élément</span><span class="sxs-lookup"><span data-stu-id="4c0db-139">create an item</span></span>|<span data-ttu-id="4c0db-140">Détecte lorsqu'un utilisateur crée un article</span><span class="sxs-lookup"><span data-stu-id="4c0db-140">Detects when a user creates an item</span></span>| <span data-ttu-id="4c0db-141">vérifiable</span><span class="sxs-lookup"><span data-stu-id="4c0db-141">auditable</span></span>|
|<span data-ttu-id="4c0db-142">renommer un article</span><span class="sxs-lookup"><span data-stu-id="4c0db-142">rename an item</span></span>|<span data-ttu-id="4c0db-143">Détecte lorsqu'un utilisateur renomme un article</span><span class="sxs-lookup"><span data-stu-id="4c0db-143">Detects when a user renames an item</span></span>| <span data-ttu-id="4c0db-144">vérifiable</span><span class="sxs-lookup"><span data-stu-id="4c0db-144">auditable</span></span>|

## <a name="monitored-files"></a><span data-ttu-id="4c0db-145">Fichiers analysées</span><span class="sxs-lookup"><span data-stu-id="4c0db-145">Monitored files</span></span>

<span data-ttu-id="4c0db-146">La DLP de point du terminaison prend en charge la surveillance de ces types de fichiers :</span><span class="sxs-lookup"><span data-stu-id="4c0db-146">Endpoint DLP supports monitoring of these file types:</span></span>

- <span data-ttu-id="4c0db-147">Fichiers Word</span><span class="sxs-lookup"><span data-stu-id="4c0db-147">Word files</span></span>
- <span data-ttu-id="4c0db-148">Fichiers PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4c0db-148">PowerPoint files</span></span>
- <span data-ttu-id="4c0db-149">Fichiers Excel</span><span class="sxs-lookup"><span data-stu-id="4c0db-149">Excel files</span></span>
- <span data-ttu-id="4c0db-150">Fichiers .pdf</span><span class="sxs-lookup"><span data-stu-id="4c0db-150">PDF files</span></span>
- <span data-ttu-id="4c0db-151">Fichiers .csv</span><span class="sxs-lookup"><span data-stu-id="4c0db-151">.csv files</span></span>
- <span data-ttu-id="4c0db-152">Fichiers .tsv</span><span class="sxs-lookup"><span data-stu-id="4c0db-152">.tsv files</span></span>
- <span data-ttu-id="4c0db-153">fichiers .txt</span><span class="sxs-lookup"><span data-stu-id="4c0db-153">.txt files</span></span>
- <span data-ttu-id="4c0db-154">Fichiers RTF</span><span class="sxs-lookup"><span data-stu-id="4c0db-154">.rtf files</span></span>
- <span data-ttu-id="4c0db-155">fichiers c</span><span class="sxs-lookup"><span data-stu-id="4c0db-155">.c files</span></span>
- <span data-ttu-id="4c0db-156">fichiers de classe</span><span class="sxs-lookup"><span data-stu-id="4c0db-156">.class files</span></span>
- <span data-ttu-id="4c0db-157">fichiers CPP</span><span class="sxs-lookup"><span data-stu-id="4c0db-157">.cpp files</span></span>
- <span data-ttu-id="4c0db-158">fichiers cs</span><span class="sxs-lookup"><span data-stu-id="4c0db-158">.cs files</span></span>
- <span data-ttu-id="4c0db-159">fichiers h</span><span class="sxs-lookup"><span data-stu-id="4c0db-159">.h files</span></span>
- <span data-ttu-id="4c0db-160">fichiers Java</span><span class="sxs-lookup"><span data-stu-id="4c0db-160">.java files</span></span>

<span data-ttu-id="4c0db-161">Par défaut, la DLP du point de terminaison audite les activités de ces types de fichiers, même s’il n’existe pas de correspondance de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4c0db-161">By default, endpoint DLP audits the activities for these file types, even if there isn't a policy match.</span></span> <span data-ttu-id="4c0db-162">Si vous souhaitez surveiller les données des correspondances de stratégie uniquement, vous pouvez désactiver l'option **Toujours auditer l’activité du fichier pour les appareils** dans les paramètres globaux DLP du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="4c0db-162">If you only want monitoring data from policy matches, you can turn off the **Always audit file activity for devices** in the endpoint DLP global settings.</span></span> <span data-ttu-id="4c0db-163">Si ce paramètre est utilisé, les activités sur les fichiers Word, PowerPoint, Excel, PDF, et .csv sont toujours auditées, même si l’appareil n’est ciblé par aucune stratégie.</span><span class="sxs-lookup"><span data-stu-id="4c0db-163">If this setting is on, activities on any Word, PowerPoint, Excel, PDF, and .csv file are always audited even if the device is not targeted by any policy.</span></span>

<span data-ttu-id="4c0db-164">Le DLP du point de terminaison contrôle l’activité basée sur le type MIME, de sorte que les activités sont capturées même si l’extension de fichier est modifiée.</span><span class="sxs-lookup"><span data-stu-id="4c0db-164">Endpoint DLP monitors activity-based on MIME type, so activities will be captured even if the file extension is changed.</span></span>

## <a name="whats-different-in-endpoint-dlp"></a><span data-ttu-id="4c0db-165">Différences avec Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="4c0db-165">What's different in Endpoint DLP</span></span>

<span data-ttu-id="4c0db-166">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’approfondir le point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="4c0db-166">There are a few extra concepts that you need to be aware of before you dig into Endpoint DLP.</span></span>

### <a name="enabling-device-management"></a><span data-ttu-id="4c0db-167">Activation de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="4c0db-167">Enabling Device management</span></span>

<span data-ttu-id="4c0db-168">La gestion des appareils est une fonctionnalité qui permet d’assembler la télémétrie à partir d’appareils et de l’intégrer à des solutions de conformité Microsoft 365 telles que point de terminaison DLP et [ gestionnaire des risques Insider](insider-risk-management.md).</span><span class="sxs-lookup"><span data-stu-id="4c0db-168">Device management is the functionality that enables the collection of telemetry from devices and brings it into Microsoft 365 compliance solutions like Endpoint DLP and [Insider Risk management](insider-risk-management.md).</span></span> <span data-ttu-id="4c0db-169">Vous devez intégrer tous les appareils que vous voulez utiliser en tant qu’emplacements dans les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="4c0db-169">You'll need to onboard all devices you want to use as locations in DLP policies.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-170">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-170">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

<span data-ttu-id="4c0db-171">L’intégration et déclassement sont gérés à l’aide de scripts téléchargés à partir du centre de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="4c0db-171">Onboarding and offboarding are handled via scripts you download from the Device management center.</span></span> <span data-ttu-id="4c0db-172">Le centre inclut des scripts personnalisés pour chacune de ces méthodes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="4c0db-172">The center has custom scripts for each of these deployment methods:</span></span>

- <span data-ttu-id="4c0db-173">script local (jusqu’à 10 ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="4c0db-173">local script (up to 10 machines)</span></span>
- <span data-ttu-id="4c0db-174">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="4c0db-174">Group policy</span></span>
- <span data-ttu-id="4c0db-175">System Center Configuration Manager, Version 1610 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4c0db-175">System Center Configuration Manager (version 1610 or later)</span></span>
- <span data-ttu-id="4c0db-176">Gestion des périphériques mobiles/Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="4c0db-176">Mobile Device Management/Microsoft Intune</span></span>
- <span data-ttu-id="4c0db-177">Scripts d’intégration VDI pour les machines non persistantes</span><span class="sxs-lookup"><span data-stu-id="4c0db-177">VDI onboarding scripts for non-persistent machines</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-178">![page d’intégration d’appareils](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-178">![device onboarding page](../media/endpoint-dlp-learn-about-3-device-onboarding-page.png)</span></span>

 <span data-ttu-id="4c0db-179">Utilisez les procédures décrites dans [Prise en main des points de terminaison Microsoft 365 DLP](endpoint-dlp-getting-started.md) vers les appareils intégrés.</span><span class="sxs-lookup"><span data-stu-id="4c0db-179">Use the procedures in [Getting started with Microsoft 365 Endpoint DLP](endpoint-dlp-getting-started.md) to onboard devices.</span></span>

<span data-ttu-id="4c0db-180">Si vous avez des appareils intégrés via [Microsoft Defender pour point de terminaison](/windows/security/threat-protection/), ces derniers apparaissent automatiquement dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="4c0db-180">If you have onboarded devices through [Microsoft Defender for Endpoint](/windows/security/threat-protection/), those devices will automatically show up in the list of devices.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-181">![liste des appareils gérés](../media/endpoint-dlp-learn-about-2-device-list.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-181">![managed devices list](../media/endpoint-dlp-learn-about-2-device-list.png)</span></span>

### <a name="viewing-endpoint-dlp-data"></a><span data-ttu-id="4c0db-182">Affichage des données DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4c0db-182">Viewing Endpoint DLP data</span></span>

<span data-ttu-id="4c0db-183">Vous pouvez afficher les alertes liées aux stratégies DLP appliquées sur les appareils de point de terminaison en accédant au [Tableau de bord de Gestion des Alertes DLP.](dlp-configure-view-alerts-policies.md)</span><span class="sxs-lookup"><span data-stu-id="4c0db-183">You can view alerts related to DLP policies enforced on endpoint devices by going to the [DLP Alerts Management Dashboard](dlp-configure-view-alerts-policies.md).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-184">![Information d’alerte](../media/Alert-info-1.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-184">![Alert info](../media/Alert-info-1.png)</span></span>

<span data-ttu-id="4c0db-185">Vous pouvez également afficher les détails de l’événement associé avec des métadonnées complètes dans le même tableau de bord</span><span class="sxs-lookup"><span data-stu-id="4c0db-185">You can also view details of the associated event with rich metadata in the same dashboard</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-186">![Informations sur un événement](../media/Event-info-1.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-186">![event info](../media/Event-info-1.png)</span></span>

<span data-ttu-id="4c0db-187">Une fois qu’un appareil est intégré, les informations relatives aux activités auditées sont transmises dans l’Explorateur d’activités, même avant de configurer et déployer des stratégies DLP qui ont des périphériques comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="4c0db-187">Once a device is onboarded, information about audited activities flows into Activity explorer even before you configure and deploy any DLP policies that have devices as a location.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-188">![événements DLP du point de terminaison dans l’explorateur d’activités](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-188">![endpoint dlp events in activity explorer](../media/endpoint-dlp-learn-about-4-activity-explorer.png)</span></span>

<span data-ttu-id="4c0db-189">Point de terminaison DLP recueille de nombreuses informations sur l’activité auditée.</span><span class="sxs-lookup"><span data-stu-id="4c0db-189">Endpoint DLP collects extensive information on audited activity.</span></span>

<span data-ttu-id="4c0db-190">Par exemple, si un fichier est copié sur un support USB amovible, les attributs suivants apparaissent dans les détails de l’activité :</span><span class="sxs-lookup"><span data-stu-id="4c0db-190">For example, if a file is copied to removable USB media, you'd see these attributes in the activity details:</span></span>

- <span data-ttu-id="4c0db-191">type d’activité</span><span class="sxs-lookup"><span data-stu-id="4c0db-191">activity type</span></span>
- <span data-ttu-id="4c0db-192">IP Client</span><span class="sxs-lookup"><span data-stu-id="4c0db-192">client IP</span></span>
- <span data-ttu-id="4c0db-193">Chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="4c0db-193">target file path</span></span>
- <span data-ttu-id="4c0db-194">horodatage arrivé</span><span class="sxs-lookup"><span data-stu-id="4c0db-194">happened timestamp</span></span>
- <span data-ttu-id="4c0db-195">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="4c0db-195">file name</span></span>
- <span data-ttu-id="4c0db-196">utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c0db-196">user</span></span>
- <span data-ttu-id="4c0db-197">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="4c0db-197">file extension</span></span>
- <span data-ttu-id="4c0db-198">taille du fichier</span><span class="sxs-lookup"><span data-stu-id="4c0db-198">file size</span></span>
- <span data-ttu-id="4c0db-199">type d’informations sensibles (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="4c0db-199">sensitive information type (if applicable)</span></span>
- <span data-ttu-id="4c0db-200">valeur SHA1</span><span class="sxs-lookup"><span data-stu-id="4c0db-200">sha1 value</span></span>
- <span data-ttu-id="4c0db-201">valeur SHA256</span><span class="sxs-lookup"><span data-stu-id="4c0db-201">sha256 value</span></span>
- <span data-ttu-id="4c0db-202">nom de fichier précédent</span><span class="sxs-lookup"><span data-stu-id="4c0db-202">previous file name</span></span>
- <span data-ttu-id="4c0db-203">emplacement</span><span class="sxs-lookup"><span data-stu-id="4c0db-203">location</span></span>
- <span data-ttu-id="4c0db-204">parent</span><span class="sxs-lookup"><span data-stu-id="4c0db-204">parent</span></span>
- <span data-ttu-id="4c0db-205">chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4c0db-205">filepath</span></span>
- <span data-ttu-id="4c0db-206">type d’emplacement source</span><span class="sxs-lookup"><span data-stu-id="4c0db-206">source location type</span></span>
- <span data-ttu-id="4c0db-207">platform</span><span class="sxs-lookup"><span data-stu-id="4c0db-207">platform</span></span>
- <span data-ttu-id="4c0db-208">nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="4c0db-208">device name</span></span>
- <span data-ttu-id="4c0db-209">type d’emplacement de destination</span><span class="sxs-lookup"><span data-stu-id="4c0db-209">destination location type</span></span>
- <span data-ttu-id="4c0db-210">application ayant effectué la copie</span><span class="sxs-lookup"><span data-stu-id="4c0db-210">application that performed the copy</span></span>
- <span data-ttu-id="4c0db-211">ID de l’appareil Microsoft Defender pour point de terminaison (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="4c0db-211">Microsoft Defender for Endpoint device ID (if applicable)</span></span>
- <span data-ttu-id="4c0db-212">fabricant de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="4c0db-212">removable media device manufacturer</span></span>
- <span data-ttu-id="4c0db-213">modèle d’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="4c0db-213">removable media device model</span></span>
- <span data-ttu-id="4c0db-214">numéro de série de l’appareil multimédia amovible</span><span class="sxs-lookup"><span data-stu-id="4c0db-214">removable media device serial number</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4c0db-215">![copier dans les attributs d’activités usb](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="4c0db-215">![copy to usb activity attributes](../media/endpoint-dlp-learn-about-5-activity-attributes.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="4c0db-216">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4c0db-216">Next steps</span></span>

<span data-ttu-id="4c0db-217">Maintenant que vous en savez plus sur les points de terminaison DLP, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c0db-217">Now that you've learned about Endpoint DLP, your next steps are:</span></span>

1. [<span data-ttu-id="4c0db-218">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="4c0db-218">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
2. [<span data-ttu-id="4c0db-219">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="4c0db-219">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="4c0db-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c0db-220">See also</span></span>

- [<span data-ttu-id="4c0db-221">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="4c0db-221">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="4c0db-222">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="4c0db-222">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="4c0db-223">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="4c0db-223">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="4c0db-224">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="4c0db-224">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="4c0db-225">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="4c0db-225">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="4c0db-226">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4c0db-226">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)
- [<span data-ttu-id="4c0db-227">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="4c0db-227">Insider Risk management</span></span>](insider-risk-management.md)
