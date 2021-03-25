---
title: 'Microsoft Defender ATP pour Android : informations de confidentialité'
description: Contrôles de confidentialité, comment configurer les paramètres de stratégie qui ont une incidence sur la confidentialité et les informations sur les données de diagnostic collectées dans Microsoft Defender ATP pour Android.
keywords: microsoft, defender, atp, android, confidentialité, diagnostic
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
ms.openlocfilehash: abb22b2e733d1e40bd4f2733ef2d25767c69ccf7
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163326"
---
#  <a name="microsoft-defender-for-endpoint-for-android---privacy-information"></a><span data-ttu-id="d0f82-104">Microsoft Defender pour le point de terminaison pour Android : informations de confidentialité</span><span class="sxs-lookup"><span data-stu-id="d0f82-104">Microsoft Defender for Endpoint for Android - Privacy information</span></span>

<span data-ttu-id="d0f82-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d0f82-105">**Applies to:**</span></span>
- [<span data-ttu-id="d0f82-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d0f82-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d0f82-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d0f82-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="d0f82-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d0f82-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d0f82-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d0f82-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


<span data-ttu-id="d0f82-110">Defender pour le point de terminaison pour Android collecte des informations à partir de vos appareils Android configurés et les stocke dans le même client que celui où vous avez Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d0f82-110">Defender for Endpoint for Android collects information from your configured Android devices and stores it in the same tenant where you have Defender for Endpoint.</span></span>

<span data-ttu-id="d0f82-111">Des informations sont collectées pour aider à maintenir defender pour point de terminaison pour Android sécurisé, à jour, en cours d’application et pour prendre en charge le service.</span><span class="sxs-lookup"><span data-stu-id="d0f82-111">Information is collected to help keep Defender for Endpoint for Android secure, up-to-date, performing as expected and to support the service.</span></span>

## <a name="required-data"></a><span data-ttu-id="d0f82-112">Données requises</span><span class="sxs-lookup"><span data-stu-id="d0f82-112">Required Data</span></span> 

<span data-ttu-id="d0f82-113">Les données requises sont constituées de données nécessaires pour que Defender for Endpoint for Android fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="d0f82-113">Required data consists of data that is necessary to make Defender for Endpoint for Android work as expected.</span></span> <span data-ttu-id="d0f82-114">Ces données sont essentielles au fonctionnement du service et peuvent inclure des données relatives à l’utilisateur final, à l’organisation, à l’appareil et aux applications.</span><span class="sxs-lookup"><span data-stu-id="d0f82-114">This data is essential to the operation of the service and can include data related to the end user, organization, device, and apps.</span></span> <span data-ttu-id="d0f82-115">Voici une liste des types de données collectées :</span><span class="sxs-lookup"><span data-stu-id="d0f82-115">Here's a list of the types of data being collected:</span></span>

### <a name="app-information"></a><span data-ttu-id="d0f82-116">Informations sur l’application</span><span class="sxs-lookup"><span data-stu-id="d0f82-116">App information</span></span>

<span data-ttu-id="d0f82-117">Informations sur les packages d’application Android (APK) sur l’appareil, y compris</span><span class="sxs-lookup"><span data-stu-id="d0f82-117">Information about Android application packages (APKs) on the device including</span></span>

-  <span data-ttu-id="d0f82-118">Source d’installation</span><span class="sxs-lookup"><span data-stu-id="d0f82-118">Install source</span></span>
-  <span data-ttu-id="d0f82-119">Emplacement de stockage (chemin d’accès au fichier) de l’APIK</span><span class="sxs-lookup"><span data-stu-id="d0f82-119">Storage location (file path) of the APK</span></span>
-  <span data-ttu-id="d0f82-120">Heure d’installation, taille de l’API et autorisations</span><span class="sxs-lookup"><span data-stu-id="d0f82-120">Time of install, size of APK and permissions</span></span>

### <a name="web-page--network-information"></a><span data-ttu-id="d0f82-121">Page Web / Informations réseau</span><span class="sxs-lookup"><span data-stu-id="d0f82-121">Web page / Network information</span></span>

- <span data-ttu-id="d0f82-122">URL complète (sur les navigateurs pris en charge) lorsque l’utilisateur clique dessus</span><span class="sxs-lookup"><span data-stu-id="d0f82-122">Full URL (on supported browsers), when clicked</span></span>
- <span data-ttu-id="d0f82-123">Informations de connexion</span><span class="sxs-lookup"><span data-stu-id="d0f82-123">Connection information</span></span>
- <span data-ttu-id="d0f82-124">Type de protocole (par exemple, HTTP, HTTPS, etc.)</span><span class="sxs-lookup"><span data-stu-id="d0f82-124">Protocol type (such as HTTP, HTTPS, etc.)</span></span>


### <a name="device-and-account-information"></a><span data-ttu-id="d0f82-125">Informations sur l’appareil et le compte</span><span class="sxs-lookup"><span data-stu-id="d0f82-125">Device and account information</span></span>

- <span data-ttu-id="d0f82-126">Informations sur l’appareil telles que l'& date, la version Android, le modèle OEM, les informations sur l’UC et l’identificateur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d0f82-126">Device information such as date & time, Android version, OEM model, CPU       info, and Device identifier</span></span>
- <span data-ttu-id="d0f82-127">L’identificateur de l’appareil est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d0f82-127">Device identifier is one of the below:</span></span>
    - <span data-ttu-id="d0f82-128">Wi-Fi'adaptateur MAC</span><span class="sxs-lookup"><span data-stu-id="d0f82-128">Wi-Fi adapter MAC address</span></span>
    - <span data-ttu-id="d0f82-129">[ID Android](https://developer.android.com/reference/android/provider/Settings.Secure#ANDROID_ID) (tel que généré par Android au moment du premier démarrage de l’appareil)</span><span class="sxs-lookup"><span data-stu-id="d0f82-129">[Android       ID](https://developer.android.com/reference/android/provider/Settings.Secure#ANDROID_ID) (as generated by Android at the time of first boot of the device)</span></span>
    - <span data-ttu-id="d0f82-130">Identificateur global unique (GUID) généré de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="d0f82-130">Randomly generated globally unique identifier (GUID)</span></span>

- <span data-ttu-id="d0f82-131">Informations sur le client, l’appareil et l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d0f82-131">Tenant, Device and User information</span></span>
    -   <span data-ttu-id="d0f82-132">ID d’appareil Azure Active Directory (AD) et ID utilisateur Azure : identifie de manière unique l’appareil, utilisateur, respectivement dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0f82-132">Azure Active Directory (AD) Device ID and Azure User ID: Uniquely     identifies the device, User respectively at Azure Active directory.</span></span>

    -   <span data-ttu-id="d0f82-133">ID client Azure : GUID qui identifie votre organisation dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d0f82-133">Azure tenant ID - GUID that identifies your organization within     Azure Active Directory</span></span>

    -   <span data-ttu-id="d0f82-134">ID d’organisation Microsoft Defender ATP : identificateur unique associé à l’entreprise à qui appartient l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d0f82-134">Microsoft Defender ATP org ID - Unique identifier associated with the enterprise that the device belongs to.</span></span> <span data-ttu-id="d0f82-135">Permet à Microsoft d’identifier si les problèmes ont un impact sur un ensemble d’entreprises sélectionné et le nombre d’entreprises qui en sont touchées</span><span class="sxs-lookup"><span data-stu-id="d0f82-135">Allows Microsoft to identify whether issues are impacting a select set of enterprises and how many enterprises are impacted</span></span> 

    -   <span data-ttu-id="d0f82-136">Nom d’utilisateur principal – ID de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d0f82-136">User Principal Name – Email ID of the user</span></span>

### <a name="product-and-service-usage-data"></a><span data-ttu-id="d0f82-137">Données d’utilisation des produits et services</span><span class="sxs-lookup"><span data-stu-id="d0f82-137">Product and service usage data</span></span>
-   <span data-ttu-id="d0f82-138">Informations sur le package d’application, y compris le nom, la version et l’état de la mise à niveau de l’application</span><span class="sxs-lookup"><span data-stu-id="d0f82-138">App package info, including name, version, and app upgrade status</span></span>

-   <span data-ttu-id="d0f82-139">Actions effectuées dans l’application</span><span class="sxs-lookup"><span data-stu-id="d0f82-139">Actions performed in the app</span></span>

-   <span data-ttu-id="d0f82-140">Informations sur la détection des menaces, telles que le nom de la menace, la catégorie, etc.</span><span class="sxs-lookup"><span data-stu-id="d0f82-140">Threat detection information, such as threat name, category, etc.</span></span>

-   <span data-ttu-id="d0f82-141">Journaux de rapport d’incident générés par Android</span><span class="sxs-lookup"><span data-stu-id="d0f82-141">Crash report logs generated by Android</span></span>

## <a name="optional-data"></a><span data-ttu-id="d0f82-142">Données facultatives</span><span class="sxs-lookup"><span data-stu-id="d0f82-142">Optional Data</span></span>

<span data-ttu-id="d0f82-143">Les données facultatives incluent les données de diagnostic et les données de commentaires.</span><span class="sxs-lookup"><span data-stu-id="d0f82-143">Optional data includes diagnostic data and feedback data.</span></span> <span data-ttu-id="d0f82-144">Les données de diagnostic facultatives nous aident à améliorer le produit et nous fournissent des informations complémentaires pour détecter, diagnostiquer et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="d0f82-144">Optional diagnostic data is additional data that helps us make product improvements and provides enhanced information to help us detect, diagnose, and fix issues.</span></span> <span data-ttu-id="d0f82-145">Les données de diagnostic facultatives incluent :</span><span class="sxs-lookup"><span data-stu-id="d0f82-145">Optional diagnostic data includes:</span></span>

-   <span data-ttu-id="d0f82-146">Utilisation de l’application, du processeur et du réseau</span><span class="sxs-lookup"><span data-stu-id="d0f82-146">App, CPU, and network usage</span></span>

-   <span data-ttu-id="d0f82-147">État de l’appareil du point de vue de l’application, y compris l’état de l’analyse, le minutage de l’analyse, les autorisations d’application accordées et l’état de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="d0f82-147">State of the device from the app perspective, including scan status, scan timings, app permissions granted, and upgrade status</span></span>

-   <span data-ttu-id="d0f82-148">Fonctionnalités configurées par l’administrateur</span><span class="sxs-lookup"><span data-stu-id="d0f82-148">Features configured by the admin</span></span>

-   <span data-ttu-id="d0f82-149">Informations de base sur les navigateurs sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="d0f82-149">Basic information about the browsers on the device</span></span>

<span data-ttu-id="d0f82-150">**Les données de** commentaires sont collectées par le biais de commentaires dans l’application fournis par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d0f82-150">**Feedback Data** is collected through in-app feedback provided by the user</span></span>

-   <span data-ttu-id="d0f82-151">L’adresse e-mail de l’utilisateur, s’il choisit de la fournir</span><span class="sxs-lookup"><span data-stu-id="d0f82-151">The user’s email address, if they choose to provide it</span></span>

-   <span data-ttu-id="d0f82-152">Type de commentaires (souris, frown, idée) et tous les commentaires envoyés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d0f82-152">Feedback type (smile, frown, idea) and any feedback comments submitted by the user</span></span>
