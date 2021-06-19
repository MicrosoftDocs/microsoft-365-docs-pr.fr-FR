---
title: Exporter l’évaluation de la configuration sécurisée par appareil
description: Renvoie une entrée pour chaque combinaison unique de DeviceId, ConfigurationId.
keywords: api, api, évaluation d’exportation, évaluation par appareil, rapport d’évaluation des vulnérabilités, évaluation des vulnérabilités d’appareils, rapport de vulnérabilité d’appareil, évaluation de la configuration sécurisée, rapport de configuration sécurisé, évaluation des vulnérabilités logicielles, rapport de vulnérabilité logicielle, rapport de vulnérabilité par ordinateur,
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-jweston
author: jweston-1
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.custom: api
ms.openlocfilehash: ad8b2030da4fb4815eb71ca53fb2dbac67a05d79
ms.sourcegitcommit: bc64d9f619259bd0a94e43a9010aae5cffb4d6c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53022389"
---
# <a name="export-secure-configuration-assessment-per-device"></a><span data-ttu-id="363f9-104">Exporter l’évaluation de la configuration sécurisée par appareil</span><span class="sxs-lookup"><span data-stu-id="363f9-104">Export secure configuration assessment per device</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="363f9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="363f9-105">**Applies to:**</span></span>

- [<span data-ttu-id="363f9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="363f9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="363f9-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="363f9-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="363f9-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="363f9-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="363f9-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="363f9-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

>
<span data-ttu-id="363f9-110">Renvoie toutes les configurations et leur état, par appareil.</span><span class="sxs-lookup"><span data-stu-id="363f9-110">Returns all of the configurations and their status, on a per-device basis.</span></span>

<span data-ttu-id="363f9-111">Il existe différents appels d’API pour obtenir différents types de données.</span><span class="sxs-lookup"><span data-stu-id="363f9-111">There are different API calls to get different types of data.</span></span> <span data-ttu-id="363f9-112">Étant donné que la quantité de données peut être importante, il existe deux façons de les récupérer :</span><span class="sxs-lookup"><span data-stu-id="363f9-112">Because the amount of data can be large, there are two ways it can be retrieved:</span></span>

- <span data-ttu-id="363f9-113">[Exporter la réponse **JSON**](#1-export-secure-configuration-assessment-json-response)d’évaluation de la configuration sécurisée : l’API tire toutes les données de votre organisation en tant que réponses Json.</span><span class="sxs-lookup"><span data-stu-id="363f9-113">[Export secure configuration assessment **JSON response**](#1-export-secure-configuration-assessment-json-response):  The API pulls all data in your organization as Json responses.</span></span> <span data-ttu-id="363f9-114">Cette méthode est la meilleure pour _les petites organisations avec moins de 100 Ko d’appareils._</span><span class="sxs-lookup"><span data-stu-id="363f9-114">This method is best for _small organizations with less than 100-K devices_.</span></span> <span data-ttu-id="363f9-115">La réponse est paginée, afin que vous pouvez utiliser le champ odata.nextLink de la réponse \@ pour récupérer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="363f9-115">The response is paginated, so you can use the \@odata.nextLink field from the response to fetch the next results.</span></span>

- <span data-ttu-id="363f9-116">[Exporter l’évaluation de la configuration **sécurisée via des fichiers**](#2-export-secure-configuration-assessment-via-files): cette solution API permet d’obtenir plus de données plus rapidement et de manière plus fiable.</span><span class="sxs-lookup"><span data-stu-id="363f9-116">[Export secure configuration assessment **via files**](#2-export-secure-configuration-assessment-via-files): This API solution enables pulling larger amounts of data faster and more reliably.</span></span> <span data-ttu-id="363f9-117">Par conséquent, il est recommandé pour les grandes organisations, avec plus de 100 K appareils.</span><span class="sxs-lookup"><span data-stu-id="363f9-117">Therefore, it is recommended for large organizations, with more than 100-K devices.</span></span> <span data-ttu-id="363f9-118">Cette API tire toutes les données de votre organisation en tant que fichiers de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="363f9-118">This API pulls all data in your organization as download files.</span></span> <span data-ttu-id="363f9-119">La réponse contient des URL pour télécharger toutes les données à partir de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="363f9-119">The response contains URLs to download all the data from Azure Storage.</span></span> <span data-ttu-id="363f9-120">Cette API vous permet de télécharger toutes vos données à partir Azure Storage comme suit :</span><span class="sxs-lookup"><span data-stu-id="363f9-120">This API enables you to download all your data from Azure Storage as follows:</span></span>

  - <span data-ttu-id="363f9-121">Appelez l’API pour obtenir la liste des URL de téléchargement avec toutes les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="363f9-121">Call the API to get a list of download URLs with all your organization data.</span></span>

  - <span data-ttu-id="363f9-122">Téléchargez tous les fichiers à l’aide des URL de téléchargement et traiter les données comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="363f9-122">Download all the files using the download URLs and process the data as you like.</span></span>

<span data-ttu-id="363f9-123">Les données collectées (à l’aide _d’OData_ ou _via_ des fichiers) sont l’instantané actuel de l’état actuel et ne contiennent pas de données historiques.</span><span class="sxs-lookup"><span data-stu-id="363f9-123">Data that is collected (using either _OData_ or _via files_) is the current snapshot of the current state, and does not contain historic data.</span></span> <span data-ttu-id="363f9-124">Pour collecter des données historiques, les clients doivent les enregistrer dans leurs propres stockages de données.</span><span class="sxs-lookup"><span data-stu-id="363f9-124">In order to collect historic data, customers must save the data in their own data storages.</span></span>

> [!Note]
>
> <span data-ttu-id="363f9-125">Sauf indication contraire, toutes les méthodes \*\*\*\* d’évaluation d’exportation répertoriées sont l’exportation complète et par appareil **_(également_** appelé **_par appareil)._**</span><span class="sxs-lookup"><span data-stu-id="363f9-125">Unless indicated otherwise, all export assessment methods listed are **_full export_** and **_by device_** (also referred to as **_per device_**).</span></span>

## <a name="1-export-secure-configuration-assessment-json-response"></a><span data-ttu-id="363f9-126">1. Exporter l’évaluation de la configuration sécurisée (réponse JSON)</span><span class="sxs-lookup"><span data-stu-id="363f9-126">1. Export secure configuration assessment (JSON response)</span></span>

### <a name="11-api-method-description"></a><span data-ttu-id="363f9-127">1.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="363f9-127">1.1 API method description</span></span>

<span data-ttu-id="363f9-128">Cette réponse API contient l’évaluation de la configuration sécurisée sur vos appareils exposés et renvoie une entrée pour chaque combinaison unique de DeviceId, ConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="363f9-128">This API response contains the Secure Configuration Assessment on your exposed devices, and returns an entry for every unique combination of DeviceId, ConfigurationId.</span></span>

#### <a name="111-limitations"></a><span data-ttu-id="363f9-129">1.1.1 Limitations</span><span class="sxs-lookup"><span data-stu-id="363f9-129">1.1.1 Limitations</span></span>

- <span data-ttu-id="363f9-130">La taille maximale de page est de 200 000.</span><span class="sxs-lookup"><span data-stu-id="363f9-130">Maximum page size is 200,000.</span></span>

- <span data-ttu-id="363f9-131">Les limites de taux pour cette API sont de 30 appels par minute et de 1 000 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="363f9-131">Rate limitations for this API are 30 calls per minute and 1000 calls per hour.</span></span>

### <a name="12-permissions"></a><span data-ttu-id="363f9-132">1.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="363f9-132">1.2 Permissions</span></span>

<span data-ttu-id="363f9-133">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="363f9-133">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="363f9-134">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="363f9-134">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="363f9-135">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-135">Permission type</span></span> | <span data-ttu-id="363f9-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-136">Permission</span></span> | <span data-ttu-id="363f9-137">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-137">Permission display name</span></span>
---|---|---
<span data-ttu-id="363f9-138">Application</span><span class="sxs-lookup"><span data-stu-id="363f9-138">Application</span></span> | <span data-ttu-id="363f9-139">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="363f9-139">Vulnerability.Read.All</span></span> | <span data-ttu-id="363f9-140">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="363f9-140">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="363f9-141">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="363f9-141">Delegated (work or school account)</span></span> | <span data-ttu-id="363f9-142">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="363f9-142">Vulnerability.Read</span></span> | <span data-ttu-id="363f9-143">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="363f9-143">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

### <a name="13-url"></a><span data-ttu-id="363f9-144">1.3 URL</span><span class="sxs-lookup"><span data-stu-id="363f9-144">1.3 URL</span></span>

```http
GET /api/machines/SecureConfigurationsAssessmentByMachine
```

### <a name="14-parameters"></a><span data-ttu-id="363f9-145">1.4 Paramètres</span><span class="sxs-lookup"><span data-stu-id="363f9-145">1.4 Parameters</span></span>

- <span data-ttu-id="363f9-146">pageSize \( par défaut = 50 000 : nombre de résultats en \) réponse</span><span class="sxs-lookup"><span data-stu-id="363f9-146">pageSize \(default = 50,000\) – number of results in response</span></span>

- <span data-ttu-id="363f9-147">\$top : le nombre de résultats à renvoyer ne \( retourne pas odata.nextLink et par conséquent ne tire pas \@ toutes les données\)</span><span class="sxs-lookup"><span data-stu-id="363f9-147">\$top – number of results to return \(doesn’t return \@odata.nextLink and therefore doesn’t pull all the data\)</span></span>

### <a name="15-properties"></a><span data-ttu-id="363f9-148">1.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="363f9-148">1.5 Properties</span></span>

>[!Note]
>
>- <span data-ttu-id="363f9-149">Les propriétés définies dans le tableau suivant sont répertoriées par ordre alphabétique, par ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="363f9-149">The properties defined in the following table are listed alphabetically, by property ID.</span></span>  <span data-ttu-id="363f9-150">Lors de l’exécution de cette API, la sortie résultante ne sera pas nécessairement renvoyée dans le même ordre que celui répertorié dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="363f9-150">When running this API, the resulting output will not necessarily be returned in the same order listed in this table.</span></span>
>
>- <span data-ttu-id="363f9-151">Certaines colonnes supplémentaires peuvent être renvoyées dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="363f9-151">Some additional columns might be returned in the response.</span></span> <span data-ttu-id="363f9-152">Ces colonnes sont temporaires et peuvent être supprimées. Utilisez uniquement les colonnes documentées.</span><span class="sxs-lookup"><span data-stu-id="363f9-152">These columns are temporary and might be removed, please use only the documented columns.</span></span>
>

<span data-ttu-id="363f9-153">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="363f9-153">Property (ID)</span></span> | <span data-ttu-id="363f9-154">Type de données</span><span class="sxs-lookup"><span data-stu-id="363f9-154">Data type</span></span> | <span data-ttu-id="363f9-155">Description</span><span class="sxs-lookup"><span data-stu-id="363f9-155">Description</span></span> | <span data-ttu-id="363f9-156">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="363f9-156">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="363f9-157">ConfigurationCategory</span><span class="sxs-lookup"><span data-stu-id="363f9-157">ConfigurationCategory</span></span> | <span data-ttu-id="363f9-158">string</span><span class="sxs-lookup"><span data-stu-id="363f9-158">string</span></span> | <span data-ttu-id="363f9-159">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="363f9-159">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> | <span data-ttu-id="363f9-160">Contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="363f9-160">Security controls</span></span>
<span data-ttu-id="363f9-161">ConfigurationId</span><span class="sxs-lookup"><span data-stu-id="363f9-161">ConfigurationId</span></span> | <span data-ttu-id="363f9-162">string</span><span class="sxs-lookup"><span data-stu-id="363f9-162">string</span></span> | <span data-ttu-id="363f9-163">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="363f9-163">Unique identifier for a specific configuration</span></span> | <span data-ttu-id="363f9-164">scid-10000</span><span class="sxs-lookup"><span data-stu-id="363f9-164">scid-10000</span></span>
<span data-ttu-id="363f9-165">ConfigurationImpact</span><span class="sxs-lookup"><span data-stu-id="363f9-165">ConfigurationImpact</span></span> | <span data-ttu-id="363f9-166">string</span><span class="sxs-lookup"><span data-stu-id="363f9-166">string</span></span> | <span data-ttu-id="363f9-167">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="363f9-167">Rated impact of the configuration to the overall configuration score (1-10)</span></span> | <span data-ttu-id="363f9-168">9 </span><span class="sxs-lookup"><span data-stu-id="363f9-168">9</span></span>
<span data-ttu-id="363f9-169">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="363f9-169">ConfigurationName</span></span> | <span data-ttu-id="363f9-170">string</span><span class="sxs-lookup"><span data-stu-id="363f9-170">string</span></span> | <span data-ttu-id="363f9-171">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="363f9-171">Display name of the configuration</span></span> | <span data-ttu-id="363f9-172">Intégrer des appareils à Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="363f9-172">Onboard devices to Microsoft Defender for Endpoint</span></span>
<span data-ttu-id="363f9-173">ConfigurationSubcategory</span><span class="sxs-lookup"><span data-stu-id="363f9-173">ConfigurationSubcategory</span></span> | <span data-ttu-id="363f9-174">string</span><span class="sxs-lookup"><span data-stu-id="363f9-174">string</span></span> | <span data-ttu-id="363f9-175">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="363f9-175">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="363f9-176">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="363f9-176">In many cases, this describes specific capabilities or features.</span></span> | <span data-ttu-id="363f9-177">Appareils intégrés</span><span class="sxs-lookup"><span data-stu-id="363f9-177">Onboard Devices</span></span>
<span data-ttu-id="363f9-178">DeviceId</span><span class="sxs-lookup"><span data-stu-id="363f9-178">DeviceId</span></span> | <span data-ttu-id="363f9-179">string</span><span class="sxs-lookup"><span data-stu-id="363f9-179">string</span></span> | <span data-ttu-id="363f9-180">Identificateur unique de l’appareil dans le service.</span><span class="sxs-lookup"><span data-stu-id="363f9-180">Unique identifier for the device in the service.</span></span> | <span data-ttu-id="363f9-181">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span><span class="sxs-lookup"><span data-stu-id="363f9-181">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span></span>
<span data-ttu-id="363f9-182">DeviceName</span><span class="sxs-lookup"><span data-stu-id="363f9-182">DeviceName</span></span> | <span data-ttu-id="363f9-183">string</span><span class="sxs-lookup"><span data-stu-id="363f9-183">string</span></span> | <span data-ttu-id="363f9-184">Nom de domaine complet (FQDN) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="363f9-184">Fully qualified domain name (FQDN) of the device.</span></span> | <span data-ttu-id="363f9-185">johnlaptop.europe.contoso.com</span><span class="sxs-lookup"><span data-stu-id="363f9-185">johnlaptop.europe.contoso.com</span></span>
<span data-ttu-id="363f9-186">IsApplicable</span><span class="sxs-lookup"><span data-stu-id="363f9-186">IsApplicable</span></span> | <span data-ttu-id="363f9-187">bool</span><span class="sxs-lookup"><span data-stu-id="363f9-187">bool</span></span> | <span data-ttu-id="363f9-188">Indique si la configuration ou la stratégie est applicable</span><span class="sxs-lookup"><span data-stu-id="363f9-188">Indicates whether the configuration or policy is applicable</span></span> | <span data-ttu-id="363f9-189">true</span><span class="sxs-lookup"><span data-stu-id="363f9-189">true</span></span>
<span data-ttu-id="363f9-190">IsCompliant</span><span class="sxs-lookup"><span data-stu-id="363f9-190">IsCompliant</span></span> | <span data-ttu-id="363f9-191">bool</span><span class="sxs-lookup"><span data-stu-id="363f9-191">bool</span></span> | <span data-ttu-id="363f9-192">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="363f9-192">Indicates whether the configuration or policy is properly configured</span></span> | <span data-ttu-id="363f9-193">false</span><span class="sxs-lookup"><span data-stu-id="363f9-193">false</span></span>
<span data-ttu-id="363f9-194">IsExpectedUserImpact</span><span class="sxs-lookup"><span data-stu-id="363f9-194">IsExpectedUserImpact</span></span> | <span data-ttu-id="363f9-195">bool</span><span class="sxs-lookup"><span data-stu-id="363f9-195">bool</span></span> | <span data-ttu-id="363f9-196">Indique s’il y aura un impact sur l’utilisateur si la configuration est appliquée</span><span class="sxs-lookup"><span data-stu-id="363f9-196">Indicates whether there will be user impact if the configuration will be applied</span></span> | <span data-ttu-id="363f9-197">true</span><span class="sxs-lookup"><span data-stu-id="363f9-197">true</span></span>
<span data-ttu-id="363f9-198">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="363f9-198">OSPlatform</span></span> | <span data-ttu-id="363f9-199">string</span><span class="sxs-lookup"><span data-stu-id="363f9-199">string</span></span> | <span data-ttu-id="363f9-200">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="363f9-200">Platform of the operating system running on the device.</span></span> <span data-ttu-id="363f9-201">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="363f9-201">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> <span data-ttu-id="363f9-202">Pour plus d’informations, voir les systèmes d’exploitation et les plateformes pris en charge par tvm.</span><span class="sxs-lookup"><span data-stu-id="363f9-202">See tvm supported operating systems and platforms for details.</span></span> | <span data-ttu-id="363f9-203">Windows 10</span><span class="sxs-lookup"><span data-stu-id="363f9-203">Windows10</span></span>
<span data-ttu-id="363f9-204">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="363f9-204">RbacGroupName</span></span> | <span data-ttu-id="363f9-205">string</span><span class="sxs-lookup"><span data-stu-id="363f9-205">string</span></span> | <span data-ttu-id="363f9-206">Groupe de contrôle d’accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="363f9-206">The role-based access control (RBAC) group.</span></span> <span data-ttu-id="363f9-207">Si cet appareil n’est affecté à aucun groupe RBAC, la valeur sera « Unassigned ».</span><span class="sxs-lookup"><span data-stu-id="363f9-207">If this device is not assigned to any RBAC group, the value will be “Unassigned.”</span></span> <span data-ttu-id="363f9-208">Si l’organisation ne contient aucun groupe RBAC, la valeur sera « None ».</span><span class="sxs-lookup"><span data-stu-id="363f9-208">If the organization doesn’t contain any RBAC groups, the value will be “None.”</span></span> | <span data-ttu-id="363f9-209">Serveurs</span><span class="sxs-lookup"><span data-stu-id="363f9-209">Servers</span></span>
<span data-ttu-id="363f9-210">RecommendationReference</span><span class="sxs-lookup"><span data-stu-id="363f9-210">RecommendationReference</span></span> | <span data-ttu-id="363f9-211">string</span><span class="sxs-lookup"><span data-stu-id="363f9-211">string</span></span> | <span data-ttu-id="363f9-212">Référence à l’ID de recommandation associé à ce logiciel.</span><span class="sxs-lookup"><span data-stu-id="363f9-212">A reference to the recommendation ID related to this software.</span></span> | <span data-ttu-id="363f9-213">sca-_-scid-20000</span><span class="sxs-lookup"><span data-stu-id="363f9-213">sca-_-scid-20000</span></span>
<span data-ttu-id="363f9-214">Timestamp</span><span class="sxs-lookup"><span data-stu-id="363f9-214">Timestamp</span></span> | <span data-ttu-id="363f9-215">string</span><span class="sxs-lookup"><span data-stu-id="363f9-215">string</span></span> | <span data-ttu-id="363f9-216">Dernière fois que la configuration a été vue sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="363f9-216">Last time the configuration was seen on the device</span></span> | <span data-ttu-id="363f9-217">2020-11-03 10:13:34.8476880</span><span class="sxs-lookup"><span data-stu-id="363f9-217">2020-11-03 10:13:34.8476880</span></span>

### <a name="16-examples"></a><span data-ttu-id="363f9-218">1.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="363f9-218">1.6 Examples</span></span>

#### <a name="161-request-example"></a><span data-ttu-id="363f9-219">1.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="363f9-219">1.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SecureConfigurationsAssessmentByMachine?pageSize=5 
```

#### <a name="162-response-example"></a><span data-ttu-id="363f9-220">1.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="363f9-220">1.6.2 Response example</span></span>

```json
{
    "@odata.context": "api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.AssetConfiguration)",
    "value": [
        {
            "deviceId": "00013ee62c6b12345b10214e1801b217b50ab455c293d",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_5d96860d69c73fdd06fc8d1679e1eb73eceb8330",
            "osPlatform": "Windows10",
            "osVersion": "NT kernel 6.x",
            "timestamp": "2021-01-11 09:47:58.854",
            "configurationId": "scid-10000",
            "configurationCategory": "Network",
            "configurationSubcategory": "",
            "configurationImpact": 5,
            "isCompliant": true,
            "isApplicable": true,
            "isExpectedUserImpact": false,
            "configurationName": "Disable insecure administration protocol – Telnet",
            "recommendationReference": "sca-_-scid-10000"
        },
        {
            "deviceId": "0002a1be533813b9a8c6de739785365bce7910",
            "rbacGroupName": "hhh",
            "deviceName": null,
            "osPlatform": "Windows10",
            "osVersion": "10.0",
            "timestamp": "2021-01-11 09:47:58.854",
            "configurationId": "scid-20000",
            "configurationCategory": "Security controls",
            "configurationSubcategory": "Onboard Devices",
            "configurationImpact": 9,
            "isCompliant": false,
            "isApplicable": true,
            "isExpectedUserImpact": false,
            "configurationName": "Onboard devices to Microsoft Defender for Endpoint",
            "recommendationReference": "sca-_-scid-20000"
        },
        {
            "deviceId": "0002a1de123456a8c06de736785395d4ce7610",
            "rbacGroupName": "hhh",
            "deviceName": null,
            "osPlatform": "Windows10",
            "osVersion": "10.0",
            "timestamp": "2021-01-11 09:47:58.854",
            "configurationId": "scid-10000",
            "configurationCategory": "Network",
            "configurationSubcategory": "",
            "configurationImpact": 5,
            "isCompliant": true,
            "isApplicable": true,
            "isExpectedUserImpact": false,
            "configurationName": "Disable insecure administration protocol – Telnet",
            "recommendationReference": "sca-_-scid-10000"
        },
        {
            "deviceId": "00044f912345bdaf756492dbe6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663d45912eed224b2be2f5ea3142726e63f16a.DomainPII_21eeb80b086e76bdfa178eadfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "timestamp": "2021-01-11 09:47:58.854",
            "configurationId": "scid-39",
            "configurationCategory": "OS",
            "configurationSubcategory": "",
            "configurationImpact": 5,
            "isCompliant": true,
            "isApplicable": true,
            "isExpectedUserImpact": false,
            "configurationName": "Enable 'Domain member: Digitally sign secure channel data (when possible)'",
            "recommendationReference": "sca-_-scid-39"
        },
        {
            "deviceId": "00044f912345daf759462bde6bd733d6a9c56ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663b45612eeb224d2de2f5ea3142726e63f16a.DomainPII_21eed80d086e76dbfa178eadfa25e8be9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "timestamp": "2021-01-11 09:47:58.854",
            "configurationId": "scid-6093",
            "configurationCategory": "Security controls",
            "configurationSubcategory": "Antivirus",
            "configurationImpact": 5,
            "isCompliant": false,
            "isApplicable": false,
            "isExpectedUserImpact": false,
            "configurationName": "Enable Microsoft Defender Antivirus real-time behavior monitoring for Linux",
            "recommendationReference": "sca-_-scid-6093"
        }
    ],
    "@odata.nextLink": "https://api.securitycenter.microsoft.com/api/machines/SecureConfigurationsAssessmentByMachine?pagesize=5&$skiptoken=eyJFeHBvcnREZWZpbml0aW9uIjp7IlRpbWVQYXRoIjoiMjAyMS0wMS0xMS8xMTAxLyJ9LCJFeHBvcnRGaWxlSW5kZXgiOjAsIkxpbmVTdG9wcGVkQXQiOjV9"
}
```

## <a name="2-export-secure-configuration-assessment-via-files"></a><span data-ttu-id="363f9-221">2. Exporter l’évaluation de la configuration sécurisée (via des fichiers)</span><span class="sxs-lookup"><span data-stu-id="363f9-221">2. Export secure configuration assessment (via files)</span></span>

### <a name="21-api-method-description"></a><span data-ttu-id="363f9-222">2.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="363f9-222">2.1 API method description</span></span>

<span data-ttu-id="363f9-223">Cette réponse API contient l’évaluation de la configuration sécurisée sur vos appareils exposés et renvoie une entrée pour chaque combinaison unique de DeviceId, ConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="363f9-223">This API response contains the Secure Configuration Assessment on your exposed devices, and returns an entry for every unique combination of DeviceId, ConfigurationId.</span></span>

#### <a name="212-limitations"></a><span data-ttu-id="363f9-224">2.1.2 Limitations</span><span class="sxs-lookup"><span data-stu-id="363f9-224">2.1.2 Limitations</span></span>

<span data-ttu-id="363f9-225">Les limites de taux pour cette API sont de 5 appels par minute et de 20 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="363f9-225">Rate limitations for this API are 5 calls per minute and 20 calls per hour.</span></span>

### <a name="22-permissions"></a><span data-ttu-id="363f9-226">2.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="363f9-226">2.2 Permissions</span></span>

<span data-ttu-id="363f9-227">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="363f9-227">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="363f9-228">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="363f9-228">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="363f9-229">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-229">Permission type</span></span> | <span data-ttu-id="363f9-230">Autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-230">Permission</span></span> | <span data-ttu-id="363f9-231">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="363f9-231">Permission display name</span></span>
---|---|---
<span data-ttu-id="363f9-232">Application</span><span class="sxs-lookup"><span data-stu-id="363f9-232">Application</span></span> | <span data-ttu-id="363f9-233">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="363f9-233">Vulnerability.Read.All</span></span> | <span data-ttu-id="363f9-234">\'Lire les informations Gestion des menaces et des vulnérabilités vulnérabilité « Gestion des menaces et des vulnérabilités »\'</span><span class="sxs-lookup"><span data-stu-id="363f9-234">\'Read "threat and vulnerability management" vulnerability information\'</span></span>
<span data-ttu-id="363f9-235">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="363f9-235">Delegated (work or school account)</span></span> | <span data-ttu-id="363f9-236">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="363f9-236">Vulnerability.Read</span></span> | <span data-ttu-id="363f9-237">\'Lire les informations Gestion des menaces et des vulnérabilités vulnérabilité « Gestion des menaces et des vulnérabilités »\'</span><span class="sxs-lookup"><span data-stu-id="363f9-237">\'Read "threat and vulnerability management" vulnerability information\'</span></span>

### <a name="23-url"></a><span data-ttu-id="363f9-238">2.3 URL</span><span class="sxs-lookup"><span data-stu-id="363f9-238">2.3 URL</span></span>

```http
GET /api/machines/SecureConfigurationsAssessmentExport
```

### <a name="parameters"></a><span data-ttu-id="363f9-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="363f9-239">Parameters</span></span>

- <span data-ttu-id="363f9-240">sasValidHours : nombre d’heures pendant qui les URL de téléchargement seront valides (maximum 24 heures).</span><span class="sxs-lookup"><span data-stu-id="363f9-240">sasValidHours – The number of hours that the download URLs will be valid for (Maximum 24 hours).</span></span>

### <a name="25-properties"></a><span data-ttu-id="363f9-241">2.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="363f9-241">2.5 Properties</span></span>

>[!Note]
>
>- <span data-ttu-id="363f9-242">Les fichiers sont compressés gzip & au format Json multiligne.</span><span class="sxs-lookup"><span data-stu-id="363f9-242">The files are gzip compressed & in multiline Json format.</span></span>
>
>- <span data-ttu-id="363f9-243">Les URL de téléchargement ne sont valides que pendant 3 heures . Sinon, vous pouvez utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="363f9-243">The download URLs are only valid for 3 hours; otherwise you can use the parameter.</span></span>
>
>- <span data-ttu-id="363f9-244">Pour une vitesse de téléchargement maximale de vos données, vous pouvez vous assurer que vous téléchargez à partir de la même région Azure dans laquelle résident vos données.</span><span class="sxs-lookup"><span data-stu-id="363f9-244">For maximum download speed of your data, you can make sure you are downloading from the same Azure region in which your data resides.</span></span>
>
<span data-ttu-id="363f9-245">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="363f9-245">Property (ID)</span></span> | <span data-ttu-id="363f9-246">Type de données</span><span class="sxs-lookup"><span data-stu-id="363f9-246">Data type</span></span> | <span data-ttu-id="363f9-247">Description</span><span class="sxs-lookup"><span data-stu-id="363f9-247">Description</span></span> | <span data-ttu-id="363f9-248">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="363f9-248">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="363f9-249">Exporter des fichiers</span><span class="sxs-lookup"><span data-stu-id="363f9-249">Export files</span></span> | <span data-ttu-id="363f9-250">chaîne de \[ tableau\]</span><span class="sxs-lookup"><span data-stu-id="363f9-250">array\[string\]</span></span> | <span data-ttu-id="363f9-251">Liste des URL de téléchargement pour les fichiers qui contiennent la capture instantanée actuelle de l’organisation</span><span class="sxs-lookup"><span data-stu-id="363f9-251">A list of download URLs for files holding the current snapshot of the organization</span></span> | <span data-ttu-id="363f9-252">[  Https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2” ]</span><span class="sxs-lookup"><span data-stu-id="363f9-252">[  Https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2” ]</span></span>
<span data-ttu-id="363f9-253">GeneratedTime</span><span class="sxs-lookup"><span data-stu-id="363f9-253">GeneratedTime</span></span> | <span data-ttu-id="363f9-254">string</span><span class="sxs-lookup"><span data-stu-id="363f9-254">string</span></span> | <span data-ttu-id="363f9-255">Heure de la générer.</span><span class="sxs-lookup"><span data-stu-id="363f9-255">The time that the export was generated.</span></span> | <span data-ttu-id="363f9-256">2021-05-20T08:00:00Z ]</span><span class="sxs-lookup"><span data-stu-id="363f9-256">2021-05-20T08:00:00Z  ]</span></span>

### <a name="26-examples"></a><span data-ttu-id="363f9-257">2.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="363f9-257">2.6 Examples</span></span>

#### <a name="261-request-example"></a><span data-ttu-id="363f9-258">2.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="363f9-258">2.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SecureConfigurationsAssessmentExport
```

#### <a name="262-response-example"></a><span data-ttu-id="363f9-259">2.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="363f9-259">2.6.2 Response example</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#contoso.windowsDefenderATP.api.ExportFilesResponse",
    "exportFiles": [
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/ScaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00393-e423630d-4c69-4490-8769-a4f5468c4f25.c000.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/ScaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00394-e423630d-4c69-4490-8769-a4f5468c4f25.c000.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/ScaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00394-e423630d-4c69-4490-8769-a4f5468c4f25.c001.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=..."
    ],
    "generatedTime": "2021-01-11T11:01:00Z"
}
```

## <a name="see-also"></a><span data-ttu-id="363f9-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="363f9-260">See also</span></span>

- [<span data-ttu-id="363f9-261">Exporter les méthodes et propriétés d’évaluation par appareil</span><span class="sxs-lookup"><span data-stu-id="363f9-261">Export assessment methods and properties per device</span></span>](get-assessment-methods-properties.md)

- [<span data-ttu-id="363f9-262">Exporter l’évaluation de l’inventaire logiciel par appareil</span><span class="sxs-lookup"><span data-stu-id="363f9-262">Export software inventory assessment per device</span></span>](get-assessment-software-inventory.md)

- [<span data-ttu-id="363f9-263">Exporter l’évaluation des vulnérabilités logicielles par appareil</span><span class="sxs-lookup"><span data-stu-id="363f9-263">Export software vulnerabilities assessment per device</span></span>](get-assessment-software-vulnerabilities.md)

<span data-ttu-id="363f9-264">Autres associés</span><span class="sxs-lookup"><span data-stu-id="363f9-264">Other related</span></span>

- [<span data-ttu-id="363f9-265">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="363f9-265">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="363f9-266">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="363f9-266">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
