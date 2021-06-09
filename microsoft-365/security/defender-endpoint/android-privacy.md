---
title: 'Microsoft Defender pour point de terminaison Android : informations sur la confidentialité'
description: Contrôles de confidentialité, comment configurer les paramètres de stratégie qui ont une incidence sur la confidentialité et les informations sur les données de diagnostic collectées dans Microsoft Defender pour Endpoint sur Android.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, android, confidentialité, diagnostic
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
ms.openlocfilehash: c72e9491303d3f14ddb184e6a302a518643f709d
ms.sourcegitcommit: 5377b00703b6f559092afe44fb61462e97968a60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52694340"
---
#  <a name="microsoft-defender-for-endpoint-on-android---privacy-information"></a><span data-ttu-id="3a05e-104">Microsoft Defender pour point de terminaison Android : informations sur la confidentialité</span><span class="sxs-lookup"><span data-stu-id="3a05e-104">Microsoft Defender for Endpoint on Android - Privacy information</span></span>

<span data-ttu-id="3a05e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a05e-105">**Applies to:**</span></span>
- [<span data-ttu-id="3a05e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3a05e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3a05e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3a05e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3a05e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3a05e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3a05e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3a05e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


<span data-ttu-id="3a05e-110">Defender pour le point de terminaison sur Android collecte des informations à partir de vos appareils Android configurés et les stocke dans le même client que celui où vous avez Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="3a05e-110">Defender for Endpoint on Android collects information from your configured Android devices and stores it in the same tenant where you have Defender for Endpoint.</span></span> <span data-ttu-id="3a05e-111">Les informations sont collectées pour aider à maintenir defender pour point de terminaison pour Android sécurisé, à jour, performant comme prévu et pour prendre en charge le service.</span><span class="sxs-lookup"><span data-stu-id="3a05e-111">The information is collected to help keep Defender for Endpoint for Android secure, up-to-date, performing as expected, and to support the service.</span></span>

<span data-ttu-id="3a05e-112">Pour plus d’informations sur le stockage des données, voir Microsoft Defender pour le stockage et la confidentialité des données de point [de terminaison.](data-storage-privacy.md)</span><span class="sxs-lookup"><span data-stu-id="3a05e-112">For more information about data storage, see [Microsoft Defender for Endpoint data storage and privacy](data-storage-privacy.md).</span></span>

<span data-ttu-id="3a05e-113">Des informations sont collectées pour aider à maintenir defender pour point de terminaison pour Android sécurisé, à jour, en cours d’application et pour prendre en charge le service.</span><span class="sxs-lookup"><span data-stu-id="3a05e-113">Information is collected to help keep Defender for Endpoint for Android secure, up-to-date, performing as expected and to support the service.</span></span>

<span data-ttu-id="3a05e-114">Pour plus d’informations sur les questions de confidentialité les plus courantes concernant Microsoft Defender pour point de terminaison sur les appareils mobiles Android et iOS, consultez Microsoft Defender pour endpoint et votre confidentialité sur les appareils mobiles Android et [iOS.](https://support.microsoft.com/topic/microsoft-defender-for-endpoint-and-your-privacy-on-android-and-ios-mobile-devices-4109bc54-8ec5-4433-9c33-d359b75ac22a)</span><span class="sxs-lookup"><span data-stu-id="3a05e-114">For more information on most common privacy questions about Microsoft Defender for Endpoint on Android and iOS mobile devices, see [Microsoft Defender for Endpoint and your privacy on Android and iOS mobile devices](https://support.microsoft.com/topic/microsoft-defender-for-endpoint-and-your-privacy-on-android-and-ios-mobile-devices-4109bc54-8ec5-4433-9c33-d359b75ac22a).</span></span>

## <a name="required-data"></a><span data-ttu-id="3a05e-115">Données requises</span><span class="sxs-lookup"><span data-stu-id="3a05e-115">Required Data</span></span> 

<span data-ttu-id="3a05e-116">Les données requises sont constituées de données qui sont nécessaires pour que Defender for Endpoint for Android fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="3a05e-116">Required data consists of data that is necessary to make Defender for Endpoint for Android work as expected.</span></span> <span data-ttu-id="3a05e-117">Ces données sont essentielles au fonctionnement du service et peuvent inclure des données relatives à l’utilisateur final, à l’organisation, à l’appareil et aux applications.</span><span class="sxs-lookup"><span data-stu-id="3a05e-117">This data is essential to the operation of the service and can include data related to the end user, organization, device, and apps.</span></span> <span data-ttu-id="3a05e-118">Voici une liste des types de données collectées :</span><span class="sxs-lookup"><span data-stu-id="3a05e-118">Here's a list of the types of data being collected:</span></span>

### <a name="app-information"></a><span data-ttu-id="3a05e-119">Informations sur l’application</span><span class="sxs-lookup"><span data-stu-id="3a05e-119">App information</span></span>

<span data-ttu-id="3a05e-120">Informations sur **les** packages d’application Android malveillants (APK) sur l’appareil, y compris</span><span class="sxs-lookup"><span data-stu-id="3a05e-120">Information about **malicious** Android application packages (APKs) on the device including</span></span>

-  <span data-ttu-id="3a05e-121">Source d’installation</span><span class="sxs-lookup"><span data-stu-id="3a05e-121">Install source</span></span>
-  <span data-ttu-id="3a05e-122">Stockage emplacement (chemin d’accès du fichier) de l’APIK</span><span class="sxs-lookup"><span data-stu-id="3a05e-122">Storage location (file path) of the APK</span></span>
-  <span data-ttu-id="3a05e-123">Heure d’installation, taille de l’API et autorisations</span><span class="sxs-lookup"><span data-stu-id="3a05e-123">Time of install, size of APK and permissions</span></span>

### <a name="web-page--network-information"></a><span data-ttu-id="3a05e-124">Page Web / Informations réseau</span><span class="sxs-lookup"><span data-stu-id="3a05e-124">Web page / Network information</span></span>

- <span data-ttu-id="3a05e-125">URL complète du site web uniquement lorsqu’une connexion malveillante ou une page web est détectée.</span><span class="sxs-lookup"><span data-stu-id="3a05e-125">Full URL of the website only when a malicious connection or web page is detected.</span></span>
- <span data-ttu-id="3a05e-126">Informations de connexion</span><span class="sxs-lookup"><span data-stu-id="3a05e-126">Connection information</span></span>
- <span data-ttu-id="3a05e-127">Type de protocole (par exemple, HTTP, HTTPS, etc.)</span><span class="sxs-lookup"><span data-stu-id="3a05e-127">Protocol type (such as HTTP, HTTPS, etc.)</span></span>


### <a name="device-and-account-information"></a><span data-ttu-id="3a05e-128">Informations sur l’appareil et le compte</span><span class="sxs-lookup"><span data-stu-id="3a05e-128">Device and account information</span></span>

- <span data-ttu-id="3a05e-129">Informations sur l’appareil telles que l'& date, la version Android, le modèle OEM, les informations sur l’UC et l’identificateur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="3a05e-129">Device information such as date & time, Android version, OEM model, CPU       info, and Device identifier</span></span>
- <span data-ttu-id="3a05e-130">L’identificateur de l’appareil est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a05e-130">Device identifier is one of the below:</span></span>
    - <span data-ttu-id="3a05e-131">Wi-Fi'adaptateur MAC</span><span class="sxs-lookup"><span data-stu-id="3a05e-131">Wi-Fi adapter MAC address</span></span>
    - <span data-ttu-id="3a05e-132">[ID Android](https://developer.android.com/reference/android/provider/Settings.Secure#ANDROID_ID) (tel que généré par Android au moment du premier démarrage de l’appareil)</span><span class="sxs-lookup"><span data-stu-id="3a05e-132">[Android       ID](https://developer.android.com/reference/android/provider/Settings.Secure#ANDROID_ID) (as generated by Android at the time of first boot of the device)</span></span>
    - <span data-ttu-id="3a05e-133">Identificateur global unique (GUID) généré de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="3a05e-133">Randomly generated globally unique identifier (GUID)</span></span>

- <span data-ttu-id="3a05e-134">Informations sur le client, l’appareil et l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a05e-134">Tenant, Device and User information</span></span>
    -   <span data-ttu-id="3a05e-135">Azure Active Directory (AD) Device ID et Azure User ID : identifie de manière unique l’appareil, Utilisateur, respectivement dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a05e-135">Azure Active Directory (AD) Device ID and Azure User ID: Uniquely     identifies the device, User respectively at Azure Active directory.</span></span>

    -   <span data-ttu-id="3a05e-136">ID de client Azure : GUID qui identifie votre organisation dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3a05e-136">Azure tenant ID - GUID that identifies your organization within     Azure Active Directory</span></span>

    -   <span data-ttu-id="3a05e-137">ID d’organisation Microsoft Defender pour point de terminaison : identificateur unique associé à l’entreprise à qui appartient l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3a05e-137">Microsoft Defender for Endpoint org ID - Unique identifier associated with the enterprise that the device belongs to.</span></span> <span data-ttu-id="3a05e-138">Permet à Microsoft d’identifier si les problèmes ont un impact sur un ensemble d’entreprises sélectionné et le nombre d’entreprises qui en sont touchées</span><span class="sxs-lookup"><span data-stu-id="3a05e-138">Allows Microsoft to identify whether issues are impacting a select set of enterprises and how many enterprises are impacted</span></span> 

    -   <span data-ttu-id="3a05e-139">Nom d’utilisateur principal – ID de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a05e-139">User Principal Name – Email ID of the user</span></span>

### <a name="product-and-service-usage-data"></a><span data-ttu-id="3a05e-140">Données d’utilisation des produits et services</span><span class="sxs-lookup"><span data-stu-id="3a05e-140">Product and service usage data</span></span>

<span data-ttu-id="3a05e-141">Les informations suivantes sont collectées uniquement pour l’application Microsoft Defender for Endpoint installée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3a05e-141">The following information is collected only for Microsoft Defender for Endpoint app installed on the device.</span></span> 

-   <span data-ttu-id="3a05e-142">Informations sur le package d’application, y compris le nom, la version et l’état de la mise à niveau de l’application</span><span class="sxs-lookup"><span data-stu-id="3a05e-142">App package info, including name, version, and app upgrade status</span></span>

-   <span data-ttu-id="3a05e-143">Actions effectuées dans l’application</span><span class="sxs-lookup"><span data-stu-id="3a05e-143">Actions performed in the app</span></span>

-   <span data-ttu-id="3a05e-144">Informations sur la détection des menaces, telles que le nom de la menace, la catégorie, etc.</span><span class="sxs-lookup"><span data-stu-id="3a05e-144">Threat detection information, such as threat name, category, etc.</span></span>

-   <span data-ttu-id="3a05e-145">Journaux de rapport d’incident générés par Android</span><span class="sxs-lookup"><span data-stu-id="3a05e-145">Crash report logs generated by Android</span></span>

## <a name="optional-data"></a><span data-ttu-id="3a05e-146">Données facultatives</span><span class="sxs-lookup"><span data-stu-id="3a05e-146">Optional Data</span></span>

<span data-ttu-id="3a05e-147">Les données facultatives incluent les données de diagnostic et les données de commentaires.</span><span class="sxs-lookup"><span data-stu-id="3a05e-147">Optional data includes diagnostic data and feedback data.</span></span> <span data-ttu-id="3a05e-148">Les données de diagnostic facultatives nous aident à améliorer le produit et nous fournissent des informations complémentaires pour détecter, diagnostiquer et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="3a05e-148">Optional diagnostic data is additional data that helps us make product improvements and provides enhanced information to help us detect, diagnose, and fix issues.</span></span> <span data-ttu-id="3a05e-149">Les données de diagnostic facultatives incluent :</span><span class="sxs-lookup"><span data-stu-id="3a05e-149">Optional diagnostic data includes:</span></span>

-   <span data-ttu-id="3a05e-150">Utilisation de l’application, de l’UC et du réseau</span><span class="sxs-lookup"><span data-stu-id="3a05e-150">App, CPU, and network usage</span></span>

-   <span data-ttu-id="3a05e-151">État de l’appareil du point de vue de l’application, y compris l’état de l’analyse, le minutage de l’analyse, les autorisations d’application accordées et l’état de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="3a05e-151">State of the device from the app perspective, including scan status, scan timings, app permissions granted, and upgrade status</span></span>

-   <span data-ttu-id="3a05e-152">Fonctionnalités configurées par l’administrateur</span><span class="sxs-lookup"><span data-stu-id="3a05e-152">Features configured by the admin</span></span>

-   <span data-ttu-id="3a05e-153">Informations de base sur les navigateurs sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="3a05e-153">Basic information about the browsers on the device</span></span>

<span data-ttu-id="3a05e-154">**Les données de** commentaires sont collectées par le biais de commentaires dans l’application fournis par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a05e-154">**Feedback Data** is collected through in-app feedback provided by the user</span></span>

-   <span data-ttu-id="3a05e-155">L’adresse e-mail de l’utilisateur, s’il choisit de la fournir</span><span class="sxs-lookup"><span data-stu-id="3a05e-155">The user’s email address, if they choose to provide it</span></span>

-   <span data-ttu-id="3a05e-156">Type de commentaires (souris, frown, idée) et tous les commentaires envoyés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a05e-156">Feedback type (smile, frown, idea) and any feedback comments submitted by the user</span></span>
