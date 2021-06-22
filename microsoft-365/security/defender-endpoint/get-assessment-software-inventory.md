---
title: Exporter l’évaluation de l’inventaire logiciel par appareil
description: Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion.
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
ms.openlocfilehash: 6a0bc142d8fa353e7e5910b0a5eba4842cd7ff50
ms.sourcegitcommit: 4d26a57c37ff7efbb8d235452c78498b06a59714
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53053166"
---
# <a name="export-software-inventory-assessment-per-device"></a><span data-ttu-id="82e17-104">Exporter l’évaluation de l’inventaire logiciel par appareil</span><span class="sxs-lookup"><span data-stu-id="82e17-104">Export software inventory assessment per device</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="82e17-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="82e17-105">**Applies to:**</span></span>

- [<span data-ttu-id="82e17-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82e17-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="82e17-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="82e17-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="82e17-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="82e17-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="82e17-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="82e17-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

>
<span data-ttu-id="82e17-110">Il existe différents appels d’API pour obtenir différents types de données.</span><span class="sxs-lookup"><span data-stu-id="82e17-110">There are different API calls to get different types of data.</span></span> <span data-ttu-id="82e17-111">Étant donné que la quantité de données peut être importante, il existe deux façons de les récupérer :</span><span class="sxs-lookup"><span data-stu-id="82e17-111">Because the amount of data can be large, there are two ways it can be retrieved:</span></span>

- <span data-ttu-id="82e17-112">[Exporter la réponse JSON de l’évaluation **de l’inventaire logiciel**](#1-export-software-inventory-assessment-json-response) L’API tire toutes les données de votre organisation en tant que réponses Json.</span><span class="sxs-lookup"><span data-stu-id="82e17-112">[Export software inventory assessment **JSON response**](#1-export-software-inventory-assessment-json-response) The API pulls all data in your organization as Json responses.</span></span> <span data-ttu-id="82e17-113">Cette méthode est la meilleure pour _les petites organisations avec moins de 100 Ko d’appareils._</span><span class="sxs-lookup"><span data-stu-id="82e17-113">This method is best for _small organizations with less than 100-K devices_.</span></span> <span data-ttu-id="82e17-114">La réponse est paginée, afin que vous pouvez utiliser le champ odata.nextLink de la réponse \@ pour récupérer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="82e17-114">The response is paginated, so you can use the \@odata.nextLink field from the response to fetch the next results.</span></span>

- <span data-ttu-id="82e17-115">[Exporter l’évaluation de l’inventaire **logiciel via des fichiers**](#2-export-software-inventory-assessment-via-files)  Cette solution d’API permet d’tirer plus rapidement et de manière plus fiable des données plus volumineuses.</span><span class="sxs-lookup"><span data-stu-id="82e17-115">[Export software inventory assessment **via files**](#2-export-software-inventory-assessment-via-files)  This API solution enables pulling larger amounts of data faster and more reliably.</span></span> <span data-ttu-id="82e17-116">Par conséquent, il est recommandé pour les grandes organisations, avec plus de 100 K appareils.</span><span class="sxs-lookup"><span data-stu-id="82e17-116">Therefore, it is recommended for large organizations, with more than 100-K devices.</span></span> <span data-ttu-id="82e17-117">Cette API tire toutes les données de votre organisation en tant que fichiers de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="82e17-117">This API pulls all data in your organization as download files.</span></span> <span data-ttu-id="82e17-118">La réponse contient des URL pour télécharger toutes les données à partir de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="82e17-118">The response contains URLs to download all the data from Azure Storage.</span></span> <span data-ttu-id="82e17-119">Cette API vous permet de télécharger toutes vos données à partir stockage Azure comme suit :</span><span class="sxs-lookup"><span data-stu-id="82e17-119">This API enables you to download all your data from Azure Storage as follows:</span></span>

  - <span data-ttu-id="82e17-120">Appelez l’API pour obtenir la liste des URL de téléchargement avec toutes les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82e17-120">Call the API to get a list of download URLs with all your organization data.</span></span>

  - <span data-ttu-id="82e17-121">Téléchargez tous les fichiers à l’aide des URL de téléchargement et traiter les données comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="82e17-121">Download all the files using the download URLs and process the data as you like.</span></span>

<span data-ttu-id="82e17-122">Les données collectées (à l’aide d’une réponse _Json_ ou _de_ fichiers) sont l’instantané actuel de l’état actuel et ne contiennent pas de données historiques.</span><span class="sxs-lookup"><span data-stu-id="82e17-122">Data that is collected (using either _Json response_ or _via files_) is the current snapshot of the current state, and does not contain historic data.</span></span> <span data-ttu-id="82e17-123">Pour collecter des données historiques, les clients doivent les enregistrer dans leurs propres stockages de données.</span><span class="sxs-lookup"><span data-stu-id="82e17-123">In order to collect historic data, customers must save the data in their own data storages.</span></span>

> [!Note]
>
> <span data-ttu-id="82e17-124">Sauf indication contraire, toutes les méthodes \*\*\*\* d’évaluation d’exportation répertoriées sont l’exportation complète et par appareil **_(également_** appelé **_par appareil)._**</span><span class="sxs-lookup"><span data-stu-id="82e17-124">Unless indicated otherwise, all export assessment methods listed are **_full export_** and **_by device_** (also referred to as **_per device_**).</span></span>

## <a name="1-export-software-inventory-assessment-json-response"></a><span data-ttu-id="82e17-125">1. Exporter l’évaluation de l’inventaire logiciel (réponse JSON)</span><span class="sxs-lookup"><span data-stu-id="82e17-125">1. Export software inventory assessment (JSON response)</span></span>

### <a name="11-api-method-description"></a><span data-ttu-id="82e17-126">1.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="82e17-126">1.1 API method description</span></span>

<span data-ttu-id="82e17-127">Cette réponse API contient toutes les données des logiciels installés par appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-127">This API response contains all the data of installed software per device.</span></span> <span data-ttu-id="82e17-128">Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion.</span><span class="sxs-lookup"><span data-stu-id="82e17-128">Returns a table with an entry for every unique combination of DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion.</span></span>

#### <a name="limitations"></a><span data-ttu-id="82e17-129">Limites</span><span class="sxs-lookup"><span data-stu-id="82e17-129">Limitations</span></span>

- <span data-ttu-id="82e17-130">La taille maximale de page est de 200 000.</span><span class="sxs-lookup"><span data-stu-id="82e17-130">Maximum page size is 200,000.</span></span>

- <span data-ttu-id="82e17-131">Les limites de taux pour cette API sont de 30 appels par minute et de 1 000 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="82e17-131">Rate limitations for this API are 30 calls per minute and 1000 calls per hour.</span></span>

### <a name="12-permissions"></a><span data-ttu-id="82e17-132">1.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="82e17-132">1.2 Permissions</span></span>

<span data-ttu-id="82e17-133">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="82e17-133">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="82e17-134">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="82e17-134">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="82e17-135">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-135">Permission type</span></span> | <span data-ttu-id="82e17-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-136">Permission</span></span> | <span data-ttu-id="82e17-137">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-137">Permission display name</span></span>
---|---|---
<span data-ttu-id="82e17-138">Application</span><span class="sxs-lookup"><span data-stu-id="82e17-138">Application</span></span> | <span data-ttu-id="82e17-139">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="82e17-139">Software.Read.All</span></span> | <span data-ttu-id="82e17-140">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="82e17-140">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="82e17-141">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="82e17-141">Delegated (work or school account)</span></span> | <span data-ttu-id="82e17-142">Software.Read</span><span class="sxs-lookup"><span data-stu-id="82e17-142">Software.Read</span></span> | <span data-ttu-id="82e17-143">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="82e17-143">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

### <a name="13-url"></a><span data-ttu-id="82e17-144">1.3 URL</span><span class="sxs-lookup"><span data-stu-id="82e17-144">1.3 URL</span></span>

```http
GET /api/machines/SoftwareInventoryByMachine
```

### <a name="14-parameters"></a><span data-ttu-id="82e17-145">1.4 Paramètres</span><span class="sxs-lookup"><span data-stu-id="82e17-145">1.4 Parameters</span></span>

- <span data-ttu-id="82e17-146">pageSize (valeur par défaut = 50 000) : nombre de résultats en réponse.</span><span class="sxs-lookup"><span data-stu-id="82e17-146">pageSize (default = 50,000) – number of results in response.</span></span>

- <span data-ttu-id="82e17-147">$top : nombre de résultats à renvoyer (ne retourne pas @odata.nextLink et, par conséquent, ne tire pas toutes les données)</span><span class="sxs-lookup"><span data-stu-id="82e17-147">$top – number of results to return (doesn’t return @odata.nextLink and therefore doesn’t pull all the data)</span></span>

### <a name="15-properties"></a><span data-ttu-id="82e17-148">1.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="82e17-148">1.5 Properties</span></span>

>[!NOTE]
>
>- <span data-ttu-id="82e17-149">Chaque enregistrement représente environ 0,5 KB de données.</span><span class="sxs-lookup"><span data-stu-id="82e17-149">Each record is approximately 0.5KB of data.</span></span> <span data-ttu-id="82e17-150">Vous devez prendre cela en compte lors du choix du paramètre pageSize approprié pour vous.</span><span class="sxs-lookup"><span data-stu-id="82e17-150">You should take this into account when choosing the correct pageSize parameter for you.</span></span>
>
>- <span data-ttu-id="82e17-151">Les propriétés définies dans le tableau suivant sont répertoriées par ordre alphabétique, par ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="82e17-151">The properties defined in the following table are listed alphabetically, by property ID.</span></span> <span data-ttu-id="82e17-152">Lors de l’exécution de cette API, la sortie résultante ne sera pas nécessairement renvoyée dans le même ordre que celui répertorié dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="82e17-152">When running this API, the resulting output will not necessarily be returned in the same order listed in this table.</span></span>
>
>- <span data-ttu-id="82e17-153">Certaines colonnes supplémentaires peuvent être renvoyées dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="82e17-153">Some additional columns might be returned in the response.</span></span> <span data-ttu-id="82e17-154">Ces colonnes sont temporaires et peuvent être supprimées. Utilisez uniquement les colonnes documentées.</span><span class="sxs-lookup"><span data-stu-id="82e17-154">These columns are temporary and might be removed, please use only the documented columns.</span></span>

<br/>

<span data-ttu-id="82e17-155">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="82e17-155">Property (ID)</span></span> | <span data-ttu-id="82e17-156">Type de données</span><span class="sxs-lookup"><span data-stu-id="82e17-156">Data type</span></span> | <span data-ttu-id="82e17-157">Description</span><span class="sxs-lookup"><span data-stu-id="82e17-157">Description</span></span> | <span data-ttu-id="82e17-158">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="82e17-158">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="82e17-159">DeviceId</span><span class="sxs-lookup"><span data-stu-id="82e17-159">DeviceId</span></span> | <span data-ttu-id="82e17-160">string</span><span class="sxs-lookup"><span data-stu-id="82e17-160">string</span></span> | <span data-ttu-id="82e17-161">Identificateur unique de l’appareil dans le service.</span><span class="sxs-lookup"><span data-stu-id="82e17-161">Unique identifier for the device in the service.</span></span> | <span data-ttu-id="82e17-162">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span><span class="sxs-lookup"><span data-stu-id="82e17-162">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span></span>
<span data-ttu-id="82e17-163">DeviceName</span><span class="sxs-lookup"><span data-stu-id="82e17-163">DeviceName</span></span> | <span data-ttu-id="82e17-164">string</span><span class="sxs-lookup"><span data-stu-id="82e17-164">string</span></span> | <span data-ttu-id="82e17-165">Nom de domaine complet (FQDN) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-165">Fully qualified domain name (FQDN) of the device.</span></span> | <span data-ttu-id="82e17-166">johnlaptop.europe.contoso.com</span><span class="sxs-lookup"><span data-stu-id="82e17-166">johnlaptop.europe.contoso.com</span></span>
<span data-ttu-id="82e17-167">DiskPaths</span><span class="sxs-lookup"><span data-stu-id="82e17-167">DiskPaths</span></span> | <span data-ttu-id="82e17-168">Array[string]</span><span class="sxs-lookup"><span data-stu-id="82e17-168">Array[string]</span></span>  | <span data-ttu-id="82e17-169">Preuve disque que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-169">Disk evidence that the product is installed on the device.</span></span> | <span data-ttu-id="82e17-170">[ « C: \\ Program Files (x86) \\ Microsoft \\ Silverlight \\ Application \\silverlight.exe » ]</span><span class="sxs-lookup"><span data-stu-id="82e17-170">[ "C:\\Program Files (x86)\\Microsoft\\Silverlight\\Application\\silverlight.exe" ]</span></span>
<span data-ttu-id="82e17-171">EndOfSupportDate</span><span class="sxs-lookup"><span data-stu-id="82e17-171">EndOfSupportDate</span></span> | <span data-ttu-id="82e17-172">string</span><span class="sxs-lookup"><span data-stu-id="82e17-172">string</span></span> | <span data-ttu-id="82e17-173">Date à laquelle la prise en charge de ce logiciel a ou va se terminer.</span><span class="sxs-lookup"><span data-stu-id="82e17-173">The date in which support for this software has or will end.</span></span> | <span data-ttu-id="82e17-174">2020-12-30</span><span class="sxs-lookup"><span data-stu-id="82e17-174">2020-12-30</span></span>
<span data-ttu-id="82e17-175">EndOfSupportStatus</span><span class="sxs-lookup"><span data-stu-id="82e17-175">EndOfSupportStatus</span></span> | <span data-ttu-id="82e17-176">string</span><span class="sxs-lookup"><span data-stu-id="82e17-176">string</span></span> | <span data-ttu-id="82e17-177">État de fin du support.</span><span class="sxs-lookup"><span data-stu-id="82e17-177">End of support status.</span></span> <span data-ttu-id="82e17-178">Peut contenir les valeurs possibles : None, EOS Version, Future EOS Version, EOS Software, Upcoming EOS Software.</span><span class="sxs-lookup"><span data-stu-id="82e17-178">Can contain these possible values: None, EOS Version, Upcoming EOS Version, EOS Software, Upcoming EOS Software.</span></span> | <span data-ttu-id="82e17-179">EOS à venir</span><span class="sxs-lookup"><span data-stu-id="82e17-179">Upcoming EOS</span></span>
<span data-ttu-id="82e17-180">ID</span><span class="sxs-lookup"><span data-stu-id="82e17-180">Id</span></span> | <span data-ttu-id="82e17-181">string</span><span class="sxs-lookup"><span data-stu-id="82e17-181">string</span></span> | <span data-ttu-id="82e17-182">Identificateur unique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="82e17-182">Unique identifier for the record.</span></span> | <span data-ttu-id="82e17-183">123ABG55_573AG&mnp!</span><span class="sxs-lookup"><span data-stu-id="82e17-183">123ABG55_573AG&mnp!</span></span>
<span data-ttu-id="82e17-184">NumberOfWeaknesses</span><span class="sxs-lookup"><span data-stu-id="82e17-184">NumberOfWeaknesses</span></span> | <span data-ttu-id="82e17-185">int</span><span class="sxs-lookup"><span data-stu-id="82e17-185">int</span></span> | <span data-ttu-id="82e17-186">Nombre de faiblesses sur ce logiciel sur cet appareil</span><span class="sxs-lookup"><span data-stu-id="82e17-186">Number of weaknesses on this software on this device</span></span> | <span data-ttu-id="82e17-187">3</span><span class="sxs-lookup"><span data-stu-id="82e17-187">3</span></span>
<span data-ttu-id="82e17-188">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="82e17-188">OSPlatform</span></span> | <span data-ttu-id="82e17-189">string</span><span class="sxs-lookup"><span data-stu-id="82e17-189">string</span></span> | <span data-ttu-id="82e17-190">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-190">Platform of the operating system running on the device.</span></span> <span data-ttu-id="82e17-191">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82e17-191">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> <span data-ttu-id="82e17-192">Pour plus d’informations, voir les systèmes d’exploitation et les plateformes pris en charge par tvm.</span><span class="sxs-lookup"><span data-stu-id="82e17-192">See tvm supported operating systems and platforms for details.</span></span> | <span data-ttu-id="82e17-193">Windows 10</span><span class="sxs-lookup"><span data-stu-id="82e17-193">Windows10</span></span>
<span data-ttu-id="82e17-194">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="82e17-194">RbacGroupName</span></span> | <span data-ttu-id="82e17-195">string</span><span class="sxs-lookup"><span data-stu-id="82e17-195">string</span></span> | <span data-ttu-id="82e17-196">Groupe de contrôle d’accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="82e17-196">The role-based access control (RBAC) group.</span></span> <span data-ttu-id="82e17-197">Si cet appareil n’est affecté à aucun groupe RBAC, la valeur sera « Unassigned ».</span><span class="sxs-lookup"><span data-stu-id="82e17-197">If this device is not assigned to any RBAC group, the value will be “Unassigned.”</span></span> <span data-ttu-id="82e17-198">Si l’organisation ne contient aucun groupe RBAC, la valeur sera « None ».</span><span class="sxs-lookup"><span data-stu-id="82e17-198">If the organization doesn’t contain any RBAC groups, the value will be “None.”</span></span> | <span data-ttu-id="82e17-199">Serveurs</span><span class="sxs-lookup"><span data-stu-id="82e17-199">Servers</span></span>
<span data-ttu-id="82e17-200">RegistryPaths</span><span class="sxs-lookup"><span data-stu-id="82e17-200">RegistryPaths</span></span> | <span data-ttu-id="82e17-201">Array[string]</span><span class="sxs-lookup"><span data-stu-id="82e17-201">Array[string]</span></span> | <span data-ttu-id="82e17-202">Preuve dans le Registre que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-202">Registry evidence that the product is installed in the device.</span></span> | <span data-ttu-id="82e17-203">[ « HKEY_LOCAL_MACHINE \\ SOFTWARE \\ WOW6432Node \\ Microsoft Windows \\ \\ CurrentVersion \\ Uninstall Microsoft \\ Silverlight » ]</span><span class="sxs-lookup"><span data-stu-id="82e17-203">[ "HKEY_LOCAL_MACHINE\\SOFTWARE\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Microsoft Silverlight" ]</span></span>
<span data-ttu-id="82e17-204">SoftwareFirstSeenTimestamp</span><span class="sxs-lookup"><span data-stu-id="82e17-204">SoftwareFirstSeenTimestamp</span></span> | <span data-ttu-id="82e17-205">string</span><span class="sxs-lookup"><span data-stu-id="82e17-205">string</span></span> | <span data-ttu-id="82e17-206">La première fois que ce logiciel a été vu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-206">The first time this software was seen on the device.</span></span> | <span data-ttu-id="82e17-207">2019-04-07 02:06:47</span><span class="sxs-lookup"><span data-stu-id="82e17-207">2019-04-07 02:06:47</span></span>
<span data-ttu-id="82e17-208">SoftwareName</span><span class="sxs-lookup"><span data-stu-id="82e17-208">SoftwareName</span></span> | <span data-ttu-id="82e17-209">string</span><span class="sxs-lookup"><span data-stu-id="82e17-209">string</span></span> | <span data-ttu-id="82e17-210">Nom du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="82e17-210">Name of the software product.</span></span> | <span data-ttu-id="82e17-211">Silverlight</span><span class="sxs-lookup"><span data-stu-id="82e17-211">Silverlight</span></span>
<span data-ttu-id="82e17-212">SoftwareVendor</span><span class="sxs-lookup"><span data-stu-id="82e17-212">SoftwareVendor</span></span> | <span data-ttu-id="82e17-213">string</span><span class="sxs-lookup"><span data-stu-id="82e17-213">string</span></span> | <span data-ttu-id="82e17-214">Nom du fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="82e17-214">Name of the software vendor.</span></span> | <span data-ttu-id="82e17-215">microsoft</span><span class="sxs-lookup"><span data-stu-id="82e17-215">microsoft</span></span>
<span data-ttu-id="82e17-216">SoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="82e17-216">SoftwareVersion</span></span> | <span data-ttu-id="82e17-217">string</span><span class="sxs-lookup"><span data-stu-id="82e17-217">string</span></span> | <span data-ttu-id="82e17-218">Numéro de version du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="82e17-218">Version number of the software product.</span></span> | <span data-ttu-id="82e17-219">81.0.4044.138</span><span class="sxs-lookup"><span data-stu-id="82e17-219">81.0.4044.138</span></span>

### <a name="16-examples"></a><span data-ttu-id="82e17-220">1.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="82e17-220">1.6 Examples</span></span>

#### <a name="161-request-example"></a><span data-ttu-id="82e17-221">1.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="82e17-221">1.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SoftwareInventoryByMachine?pageSize=5  &sinceTime=2021-05-19T18%3A35%3A49.924Z 
```

#### <a name="162-response-example"></a><span data-ttu-id="82e17-222">1.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="82e17-222">1.6.2 Response example</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(contoso.windowsDefenderATP.api.AssetSoftware)",
    "value": [
        {
            "deviceId": "00044f68765bbaf712342dbe6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18993b45912eeb224b2be2f5ea3142726e63f16a.DomainPII_21eeb80d086e79dbfa178eadfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "softwareVendor": "microsoft",
            "softwareName": "windows_10",
            "softwareVersion": "10.0.17763.1637",
            "numberOfWeaknesses": 58,
            "diskPaths": [],
            "registryPaths": [],
            "softwareFirstSeenTimestamp": "2020-12-30 11:07:15",
            "endOfSupportStatus": "Upcoming EOS Version",
            "endOfSupportDate": "2021-05-11T00:00:00+00:00"
        },
        {
            "deviceId": "00044f68765bbaf712342dbe6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18993b45912eeb224b2be2f5ea3142726e63f16a.DomainPII_21eeb80d086e79dbfa178eadfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "softwareVendor": "microsoft",
            "softwareName": ".net_framework",
            "softwareVersion": "4.0.0.0",
            "numberOfWeaknesses": 0,
            "diskPaths": [],
            "registryPaths": [
                "SOFTWARE\\Microsoft\\NET Framework Setup\\NDP\\v4.0\\Client\\Install"
            ],
            "softwareFirstSeenTimestamp": "2020-12-30 11:07:15",
            "endOfSupportStatus": "None",
            "endOfSupportDate": null
        },
        {
            "deviceId": "00044f68765bbaf712342dbe6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18993b45912eeb224b2be2f5ea3142726e63f16a.DomainPII_21eed80d086e79bdfa178eadfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "softwareVendor": "microsoft",
            "softwareName": "system_center_2012_endpoint_protection",
            "softwareVersion": "4.7.214.0",
            "numberOfWeaknesses": 0,
            "diskPaths": [],
            "registryPaths": [
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Microsoft Security Client"
            ],
            "softwareFirstSeenTimestamp": "2020-12-30 11:07:15",
            "endOfSupportStatus": "None",
            "endOfSupportDate": null
        },
        {
            "deviceId": "00044f68765ddaf71234bde6bd733d6a9c59ad4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18993b45912eeb224b2be2f5ea3142726e63f16a.DomainPII_21eeb80d086e79dbfa178aedfa25e8be9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "softwareVendor": "microsoft",
            "softwareName": "configuration_manager",
            "softwareVersion": "5.0.8634.1000",
            "numberOfWeaknesses": 0,
            "diskPaths": [],
            "registryPaths": [
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\{B7D3A842-E826-4542-B39B-1D883264B279}"
            ],
            "softwareFirstSeenTimestamp": "2020-12-30 11:07:15",
            "endOfSupportStatus": "None",
            "endOfSupportDate": null
        },
        {
            "deviceId": "00044f38765bbaf712342dbe6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18993b45912eeb224b2de2f5ea3142726e63f16a.DomainPII_21eeb80d086e79bdfa178eadfa25e8be9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "softwareVendor": "microsoft",
            "softwareName": "system_center_2012_endpoint_protection",
            "softwareVersion": "4.10.209.0",
            "numberOfWeaknesses": 0,
            "diskPaths": [],
            "registryPaths": [
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Microsoft Security Client"
            ],
            "softwareFirstSeenTimestamp": "2020-12-30 11:07:15",
            "endOfSupportStatus": "None",
            "endOfSupportDate": null
        }
    ],
    "@odata.nextLink": "https://api.securitycenter.microsoft.com/api/machines/SoftwareInventoryByMachine?pagesize=5&$skiptoken=eyJFeHBvcnREZWZpbml0aW9uIjp7IlRpbWVQYXRoIjoiMjAyMS0wMS0yNS8wMjAwLyJ9LCJFeHBvcnRGaWxlSW5kZXgiOjAsIkxpbmVTdG9wcGVkQXQiOjV9"
}
```

## <a name="2-export-software-inventory-assessment-via-files"></a><span data-ttu-id="82e17-223">2. Exporter l’évaluation de l’inventaire logiciel (via des fichiers)</span><span class="sxs-lookup"><span data-stu-id="82e17-223">2. Export software inventory assessment (via files)</span></span>

### <a name="21-api-method-description"></a><span data-ttu-id="82e17-224">2.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="82e17-224">2.1 API method description</span></span>

<span data-ttu-id="82e17-225">Cette réponse API contient toutes les données des logiciels installés par appareil.</span><span class="sxs-lookup"><span data-stu-id="82e17-225">This API response contains all the data of installed software per device.</span></span> <span data-ttu-id="82e17-226">Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion.</span><span class="sxs-lookup"><span data-stu-id="82e17-226">Returns a table with an entry for every unique combination of DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion.</span></span>

#### <a name="211-limitations"></a><span data-ttu-id="82e17-227">2.1.1 Limitations</span><span class="sxs-lookup"><span data-stu-id="82e17-227">2.1.1 Limitations</span></span>

<span data-ttu-id="82e17-228">Les limites de taux pour cette API sont de 5 appels par minute et de 20 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="82e17-228">Rate limitations for this API are 5 calls per minute and 20 calls per hour.</span></span>

### <a name="22-permissions"></a><span data-ttu-id="82e17-229">2.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="82e17-229">2.2 Permissions</span></span>

<span data-ttu-id="82e17-230">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="82e17-230">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="82e17-231">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="82e17-231">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="82e17-232">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-232">Permission type</span></span> | <span data-ttu-id="82e17-233">Autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-233">Permission</span></span> | <span data-ttu-id="82e17-234">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="82e17-234">Permission display name</span></span>
---|---|---
<span data-ttu-id="82e17-235">Application</span><span class="sxs-lookup"><span data-stu-id="82e17-235">Application</span></span> | <span data-ttu-id="82e17-236">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="82e17-236">Software.Read.All</span></span> | <span data-ttu-id="82e17-237">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="82e17-237">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="82e17-238">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="82e17-238">Delegated (work or school account)</span></span> | <span data-ttu-id="82e17-239">Software.Read</span><span class="sxs-lookup"><span data-stu-id="82e17-239">Software.Read</span></span> | <span data-ttu-id="82e17-240">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="82e17-240">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

### <a name="23-url"></a><span data-ttu-id="82e17-241">2.3 URL</span><span class="sxs-lookup"><span data-stu-id="82e17-241">2.3 URL</span></span>

```http
GET /api/machines/SoftwareInventoryExport
```

### <a name="parameters"></a><span data-ttu-id="82e17-242">Parameters</span><span class="sxs-lookup"><span data-stu-id="82e17-242">Parameters</span></span>

- <span data-ttu-id="82e17-243">sasValidHours : nombre d’heures pendant qui les URL de téléchargement seront valides (maximum 24 heures)</span><span class="sxs-lookup"><span data-stu-id="82e17-243">sasValidHours – The number of hours that the download URLs will be valid for (Maximum 24 hours)</span></span>

### <a name="25-properties"></a><span data-ttu-id="82e17-244">2.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="82e17-244">2.5 Properties</span></span>

>[!Note]
>
>- <span data-ttu-id="82e17-245">Les fichiers sont compressés gzip & au format JSON multiligne.</span><span class="sxs-lookup"><span data-stu-id="82e17-245">The files are gzip compressed & in multiline JSON format.</span></span>
>
>- <span data-ttu-id="82e17-246">Les URL de téléchargement ne sont valides que pendant 3 heures.</span><span class="sxs-lookup"><span data-stu-id="82e17-246">The download URLs are only valid for 3 hours.</span></span> <span data-ttu-id="82e17-247">Sinon, vous pouvez utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="82e17-247">Otherwise you can use the parameter.</span></span>
>
>- <span data-ttu-id="82e17-248">Pour une vitesse de téléchargement maximale de vos données, vous pouvez vous assurer que vous téléchargez à partir de la même région Azure que vos données résident.</span><span class="sxs-lookup"><span data-stu-id="82e17-248">For maximum download speed of your data, you can make sure you are downloading from the same Azure region that your data resides.</span></span>

<br/><br/>

<span data-ttu-id="82e17-249">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="82e17-249">Property (ID)</span></span> | <span data-ttu-id="82e17-250">Type de données</span><span class="sxs-lookup"><span data-stu-id="82e17-250">Data type</span></span> | <span data-ttu-id="82e17-251">Description</span><span class="sxs-lookup"><span data-stu-id="82e17-251">Description</span></span> | <span data-ttu-id="82e17-252">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="82e17-252">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="82e17-253">Exporter des fichiers</span><span class="sxs-lookup"><span data-stu-id="82e17-253">Export files</span></span> | <span data-ttu-id="82e17-254">chaîne de \[ tableau\]</span><span class="sxs-lookup"><span data-stu-id="82e17-254">array\[string\]</span></span> | <span data-ttu-id="82e17-255">Liste des URL de téléchargement pour les fichiers qui contiennent la capture instantanée actuelle de l’organisation</span><span class="sxs-lookup"><span data-stu-id="82e17-255">A list of download URLs for files holding the current snapshot of the organization</span></span> | <span data-ttu-id="82e17-256">[  Https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2” ]</span><span class="sxs-lookup"><span data-stu-id="82e17-256">[  Https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2” ]</span></span>
<span data-ttu-id="82e17-257">GeneratedTime</span><span class="sxs-lookup"><span data-stu-id="82e17-257">GeneratedTime</span></span> | <span data-ttu-id="82e17-258">string</span><span class="sxs-lookup"><span data-stu-id="82e17-258">string</span></span> | <span data-ttu-id="82e17-259">Heure de la générer.</span><span class="sxs-lookup"><span data-stu-id="82e17-259">The time that the export was generated.</span></span> | <span data-ttu-id="82e17-260">2021-05-20T08:00:00Z ]</span><span class="sxs-lookup"><span data-stu-id="82e17-260">2021-05-20T08:00:00Z  ]</span></span>

### <a name="26-examples"></a><span data-ttu-id="82e17-261">2.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="82e17-261">2.6 Examples</span></span>

#### <a name="261-request-example"></a><span data-ttu-id="82e17-262">2.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="82e17-262">2.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SoftwareInventoryExport
```

#### <a name="262-response-example"></a><span data-ttu-id="82e17-263">2.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="82e17-263">2.6.2 Response example</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.ExportFilesResponse",
    "exportFiles": [
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/SoftwareInventory/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00393-e423630d-4c69-4490-8769-a4f5468c4f25.c000.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/SoftwareInventory/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00394-e423630d-4c69-4490-8769-a4f5468c4f25.c000.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/SoftwareInventory/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00394-e423630d-4c69-4490-8769-a4f5468c4f25.c001.json.gz?sv=2019-12-12&st=2021-01-11T11%3A55%3A51Z&se=2021-01-11T14%3A55%3A51Z&sr=b&sp=r&sig=..."
    ],
    "generatedTime": "2021-01-11T11:01:00Z"
}
```

## <a name="see-also"></a><span data-ttu-id="82e17-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82e17-264">See also</span></span>

- [<span data-ttu-id="82e17-265">Exporter les méthodes et propriétés d’évaluation par appareil</span><span class="sxs-lookup"><span data-stu-id="82e17-265">Export assessment methods and properties per device</span></span>](get-assessment-methods-properties.md)

- [<span data-ttu-id="82e17-266">Exporter l’évaluation de la configuration sécurisée par appareil</span><span class="sxs-lookup"><span data-stu-id="82e17-266">Export secure configuration assessment per device</span></span>](get-assessment-secure-config.md)

- [<span data-ttu-id="82e17-267">Exporter l’évaluation des vulnérabilités logicielles par appareil</span><span class="sxs-lookup"><span data-stu-id="82e17-267">Export software vulnerabilities assessment per device</span></span>](get-assessment-software-vulnerabilities.md)

<span data-ttu-id="82e17-268">Autres associés</span><span class="sxs-lookup"><span data-stu-id="82e17-268">Other related</span></span>

- [<span data-ttu-id="82e17-269">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="82e17-269">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="82e17-270">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="82e17-270">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
