---
title: Exporter l’évaluation des vulnérabilités logicielles par appareil
description: La réponse API est par appareil et contient les logiciels vulnérables installés sur vos appareils exposés, ainsi que les vulnérabilités connues dans ces produits logiciels. Cette table inclut également des informations sur le système d’exploitation, les ID CVE et sur la gravité des vulnérabilités.
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
ms.openlocfilehash: 87fb5c62b520168a686cc0b95a321becdd4656ba
ms.sourcegitcommit: 4d26a57c37ff7efbb8d235452c78498b06a59714
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53052962"
---
# <a name="export-software-vulnerabilities-assessment-per-device"></a><span data-ttu-id="f8f90-105">Exporter l’évaluation des vulnérabilités logicielles par appareil</span><span class="sxs-lookup"><span data-stu-id="f8f90-105">Export software vulnerabilities assessment per device</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f8f90-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f8f90-106">**Applies to:**</span></span>

- [<span data-ttu-id="f8f90-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f8f90-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f8f90-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f8f90-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f8f90-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f8f90-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f8f90-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f8f90-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

>
<span data-ttu-id="f8f90-111">Renvoie toutes les vulnérabilités logicielles connues et leurs détails pour tous les appareils, par appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-111">Returns all known software vulnerabilities and their details for all devices, on a per-device basis.</span></span>

<span data-ttu-id="f8f90-112">Il existe différents appels d’API pour obtenir différents types de données.</span><span class="sxs-lookup"><span data-stu-id="f8f90-112">There are different API calls to get different types of data.</span></span> <span data-ttu-id="f8f90-113">Étant donné que la quantité de données peut être très importante, il existe deux façons de les récupérer :</span><span class="sxs-lookup"><span data-stu-id="f8f90-113">Because the amount of data can be very large, there are two ways it can be retrieved:</span></span>

1. <span data-ttu-id="f8f90-114">[Exporter la réponse JSON de l’évaluation **des vulnérabilités logicielles**](#1-export-software-vulnerabilities-assessment-json-response)  L’API tire toutes les données de votre organisation en tant que réponses Json.</span><span class="sxs-lookup"><span data-stu-id="f8f90-114">[Export software vulnerabilities assessment **JSON response**](#1-export-software-vulnerabilities-assessment-json-response)  The API pulls all data in your organization as Json responses.</span></span> <span data-ttu-id="f8f90-115">Cette méthode est la meilleure pour _les petites organisations avec moins de 100 K appareils._</span><span class="sxs-lookup"><span data-stu-id="f8f90-115">This method is best for _small organizations with less than 100 K devices_.</span></span> <span data-ttu-id="f8f90-116">La réponse est paginée, afin que vous pouvez utiliser le champ odata.nextLink de la réponse \@ pour récupérer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="f8f90-116">The response is paginated, so you can use the \@odata.nextLink field from the response to fetch the next results.</span></span>

2. <span data-ttu-id="f8f90-117">[Exporter l’évaluation des vulnérabilités **logicielles via des fichiers**](#2-export-software-vulnerabilities-assessment-via-files) Cette solution d’API permet d’tirer plus rapidement et de manière plus fiable des données plus volumineuses.</span><span class="sxs-lookup"><span data-stu-id="f8f90-117">[Export software vulnerabilities assessment **via files**](#2-export-software-vulnerabilities-assessment-via-files) This API solution enables pulling larger amounts of data faster and more reliably.</span></span> <span data-ttu-id="f8f90-118">Les fichiers via les fichiers sont recommandés pour les grandes organisations, avec plus de 100 Périphériques K.</span><span class="sxs-lookup"><span data-stu-id="f8f90-118">Via-files is recommended for large organizations, with more than 100 K devices.</span></span> <span data-ttu-id="f8f90-119">Cette API tire toutes les données de votre organisation en tant que fichiers de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f8f90-119">This API pulls all data in your organization as download files.</span></span> <span data-ttu-id="f8f90-120">La réponse contient des URL pour télécharger toutes les données à partir de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f90-120">The response contains URLs to download all the data from Azure Storage.</span></span> <span data-ttu-id="f8f90-121">Cette API vous permet de télécharger toutes vos données à partir stockage Azure comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8f90-121">This API enables you to download all your data from Azure Storage as follows:</span></span>

   - <span data-ttu-id="f8f90-122">Appelez l’API pour obtenir la liste des URL de téléchargement avec toutes les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8f90-122">Call the API to get a list of download URLs with all your organization data.</span></span>

   - <span data-ttu-id="f8f90-123">Téléchargez tous les fichiers à l’aide des URL de téléchargement et traiter les données comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f8f90-123">Download all the files using the download URLs and process the data as you like.</span></span>

3. <span data-ttu-id="f8f90-124">[Réponse JSON de l’évaluation des vulnérabilités **logicielles d’exportation delta**](#3-delta-export-software-vulnerabilities-assessment-json-response)  Renvoie un tableau avec une entrée pour chaque combinaison unique de : DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CveId et EventTimestamp.</span><span class="sxs-lookup"><span data-stu-id="f8f90-124">[Delta export software vulnerabilities assessment **JSON response**](#3-delta-export-software-vulnerabilities-assessment-json-response)  Returns a table with an entry for every unique combination of: DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CveId, and EventTimestamp.</span></span>
<span data-ttu-id="f8f90-125">L’API tire les données de votre organisation en tant que réponses Json.</span><span class="sxs-lookup"><span data-stu-id="f8f90-125">The API pulls data in your organization as Json responses.</span></span> <span data-ttu-id="f8f90-126">La réponse est paginée, afin que vous pouvez utiliser le champ @odata.nextLink de la réponse pour récupérer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="f8f90-126">The response is paginated, so you can use the @odata.nextLink field from the response to fetch the next results.</span></span> <br><br> <span data-ttu-id="f8f90-127">Contrairement à l’évaluation complète des vulnérabilités logicielles (réponse JSON), qui permet d’obtenir un instantané complet de l’évaluation des vulnérabilités logicielles de votre organisation par appareil, l’appel de l’API d’exportation delta est utilisé pour récupérer uniquement les modifications qui se sont produites entre une date sélectionnée et la date actuelle (l’appel d’API « delta »).</span><span class="sxs-lookup"><span data-stu-id="f8f90-127">Unlike the full "software vulnerabilities assessment (JSON response)" - which is used to obtain an entire snapshot of the software vulnerabilities assessment of your organization by device - the delta export API call is used to fetch only the changes that have happened between a selected date and the current date (the “delta” API call).</span></span> <span data-ttu-id="f8f90-128">Au lieu d’obtenir une exportation complète avec une grande quantité de données à chaque fois, vous obtenez uniquement des informations spécifiques sur les vulnérabilités nouvelles, fixes et mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f8f90-128">Instead of getting a full export with a large amount of data every time, you’ll only get specific information on new, fixed, and updated vulnerabilities.</span></span> <span data-ttu-id="f8f90-129">L’appel de l’API de réponse JSON d’exportation delta peut également être utilisé pour calculer différents KPI, tels que « combien de vulnérabilités ont été corrigées ? »</span><span class="sxs-lookup"><span data-stu-id="f8f90-129">Delta export JSON response API call can also be used to calculate different KPIs such as “how many vulnerabilities were fixed?”</span></span> <span data-ttu-id="f8f90-130">ou « combien de nouvelles vulnérabilités ont été ajoutées à mon organisation ? »</span><span class="sxs-lookup"><span data-stu-id="f8f90-130">or “how many new vulnerabilities were added to my organization?”</span></span> <br><br> <span data-ttu-id="f8f90-131">Étant donné que l’appel de l’API de réponse JSON d’exportation delta pour les vulnérabilités logicielles renvoie des données uniquement pour une plage de dates ciblée, il n’est pas considéré comme _une exportation complète._</span><span class="sxs-lookup"><span data-stu-id="f8f90-131">Because the Delta export JSON response API call for software vulnerabilities returns data for only a targeted date range, it is not considered a _full export_.</span></span>

<span data-ttu-id="f8f90-132">Les données collectées (à l’aide d’une réponse _Json_ ou _de_ fichiers) sont l’instantané actuel de l’état actuel et ne contiennent pas de données historiques.</span><span class="sxs-lookup"><span data-stu-id="f8f90-132">Data that is collected (using either _Json response_ or _via files_) is the current snapshot of the current state, and does not contain historic data.</span></span> <span data-ttu-id="f8f90-133">Pour collecter des données historiques, les clients doivent les enregistrer dans leurs propres stockages de données.</span><span class="sxs-lookup"><span data-stu-id="f8f90-133">In order to collect historic data, customers must save the data in their own data storages.</span></span>

> [!Note]
>
> <span data-ttu-id="f8f90-134">Sauf indication contraire, toutes les méthodes \*\*\*\* d’évaluation d’exportation répertoriées sont l’exportation complète et par appareil **_(également_** appelé **_par appareil)._**</span><span class="sxs-lookup"><span data-stu-id="f8f90-134">Unless indicated otherwise, all export assessment methods listed are **_full export_** and **_by device_** (also referred to as **_per device_**).</span></span>

## <a name="1-export-software-vulnerabilities-assessment-json-response"></a><span data-ttu-id="f8f90-135">1. Exporter l’évaluation des vulnérabilités logicielles (réponse JSON)</span><span class="sxs-lookup"><span data-stu-id="f8f90-135">1. Export software vulnerabilities assessment (JSON response)</span></span>

### <a name="11-api-method-description"></a><span data-ttu-id="f8f90-136">1.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="f8f90-136">1.1 API method description</span></span>

<span data-ttu-id="f8f90-137">Cette réponse API contient toutes les données des logiciels installés par appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-137">This API response contains all the data of installed software per device.</span></span> <span data-ttu-id="f8f90-138">Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CVEID.</span><span class="sxs-lookup"><span data-stu-id="f8f90-138">Returns a table with an entry for every unique combination of DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CVEID.</span></span>

#### <a name="111-limitations"></a><span data-ttu-id="f8f90-139">1.1.1 Limitations</span><span class="sxs-lookup"><span data-stu-id="f8f90-139">1.1.1 Limitations</span></span>

- <span data-ttu-id="f8f90-140">La taille maximale de page est de 200 000.</span><span class="sxs-lookup"><span data-stu-id="f8f90-140">Maximum page size is 200,000.</span></span>

- <span data-ttu-id="f8f90-141">Les limites de taux pour cette API sont de 30 appels par minute et de 1 000 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f8f90-141">Rate limitations for this API are 30 calls per minute and 1000 calls per hour.</span></span>

### <a name="12-permissions"></a><span data-ttu-id="f8f90-142">1.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="f8f90-142">1.2 Permissions</span></span>

<span data-ttu-id="f8f90-143">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f8f90-143">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f8f90-144">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f8f90-144">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="f8f90-145">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-145">Permission type</span></span> | <span data-ttu-id="f8f90-146">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-146">Permission</span></span> | <span data-ttu-id="f8f90-147">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-147">Permission display name</span></span>
---|---|---
<span data-ttu-id="f8f90-148">Application</span><span class="sxs-lookup"><span data-stu-id="f8f90-148">Application</span></span> | <span data-ttu-id="f8f90-149">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="f8f90-149">Vulnerability.Read.All</span></span> | <span data-ttu-id="f8f90-150">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="f8f90-150">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="f8f90-151">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f8f90-151">Delegated (work or school account)</span></span> | <span data-ttu-id="f8f90-152">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="f8f90-152">Vulnerability.Read</span></span> | <span data-ttu-id="f8f90-153">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="f8f90-153">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

### <a name="13-url"></a><span data-ttu-id="f8f90-154">1.3 URL</span><span class="sxs-lookup"><span data-stu-id="f8f90-154">1.3 URL</span></span>

```http
GET /api/machines/SoftwareVulnerabilitiesByMachine
```

### <a name="14-parameters"></a><span data-ttu-id="f8f90-155">1.4 Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8f90-155">1.4 Parameters</span></span>

- <span data-ttu-id="f8f90-156">pageSize (valeur par défaut = 50 000) : nombre de résultats en réponse</span><span class="sxs-lookup"><span data-stu-id="f8f90-156">pageSize (default = 50,000) – number of results in response</span></span>
- <span data-ttu-id="f8f90-157">$top : nombre de résultats à renvoyer (ne retourne pas @odata.nextLink et, par conséquent, ne tire pas toutes les données)</span><span class="sxs-lookup"><span data-stu-id="f8f90-157">$top – number of results to return (doesn’t return @odata.nextLink and therefore doesn’t pull all the data)</span></span>

### <a name="15-properties"></a><span data-ttu-id="f8f90-158">1.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8f90-158">1.5 Properties</span></span>

>[!Note]
>
>- <span data-ttu-id="f8f90-159">Chaque enregistrement représente environ 1 Ko de données.</span><span class="sxs-lookup"><span data-stu-id="f8f90-159">Each record is approximately 1 KB of data.</span></span> <span data-ttu-id="f8f90-160">Vous devez prendre cela en compte lors du choix du paramètre pageSize approprié pour vous.</span><span class="sxs-lookup"><span data-stu-id="f8f90-160">You should take this into account when choosing the correct pageSize parameter for you.</span></span>
>
>- <span data-ttu-id="f8f90-161">Certaines colonnes supplémentaires peuvent être renvoyées dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="f8f90-161">Some additional columns might be returned in the response.</span></span> <span data-ttu-id="f8f90-162">Ces colonnes sont temporaires et peuvent être supprimées. Utilisez uniquement les colonnes documentées.</span><span class="sxs-lookup"><span data-stu-id="f8f90-162">These columns are temporary and might be removed, please use only the documented columns.</span></span>
>
>- <span data-ttu-id="f8f90-163">Les propriétés définies dans le tableau suivant sont répertoriées par ordre alphabétique, par ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="f8f90-163">The properties defined in the following table are listed alphabetically, by property ID.</span></span>  <span data-ttu-id="f8f90-164">Lors de l’exécution de cette API, la sortie résultante ne sera pas nécessairement renvoyée dans le même ordre que celui répertorié dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f8f90-164">When running this API, the resulting output will not necessarily be returned in the same order listed in this table.</span></span>

<br/>

<span data-ttu-id="f8f90-165">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="f8f90-165">Property (ID)</span></span> | <span data-ttu-id="f8f90-166">Type de données</span><span class="sxs-lookup"><span data-stu-id="f8f90-166">Data type</span></span> | <span data-ttu-id="f8f90-167">Description</span><span class="sxs-lookup"><span data-stu-id="f8f90-167">Description</span></span> | <span data-ttu-id="f8f90-168">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8f90-168">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="f8f90-169">CveId</span><span class="sxs-lookup"><span data-stu-id="f8f90-169">CveId</span></span> | <span data-ttu-id="f8f90-170">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-170">string</span></span> | <span data-ttu-id="f8f90-171">Identificateur unique affecté à la vulnérabilité de sécurité sous le système CVE (Common Vulnerabilities and Exposures).</span><span class="sxs-lookup"><span data-stu-id="f8f90-171">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system.</span></span> | <span data-ttu-id="f8f90-172">CVE-2020-15992</span><span class="sxs-lookup"><span data-stu-id="f8f90-172">CVE-2020-15992</span></span>
<span data-ttu-id="f8f90-173">CvssScore</span><span class="sxs-lookup"><span data-stu-id="f8f90-173">CvssScore</span></span> | <span data-ttu-id="f8f90-174">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-174">string</span></span> | <span data-ttu-id="f8f90-175">Score CVSS de la CVE.</span><span class="sxs-lookup"><span data-stu-id="f8f90-175">The CVSS score of the CVE.</span></span> | <span data-ttu-id="f8f90-176">6.2</span><span class="sxs-lookup"><span data-stu-id="f8f90-176">6.2</span></span>
<span data-ttu-id="f8f90-177">DeviceId</span><span class="sxs-lookup"><span data-stu-id="f8f90-177">DeviceId</span></span> | <span data-ttu-id="f8f90-178">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-178">string</span></span> | <span data-ttu-id="f8f90-179">Identificateur unique de l’appareil dans le service.</span><span class="sxs-lookup"><span data-stu-id="f8f90-179">Unique identifier for the device in the service.</span></span> | <span data-ttu-id="f8f90-180">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span><span class="sxs-lookup"><span data-stu-id="f8f90-180">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span></span>
<span data-ttu-id="f8f90-181">DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8f90-181">DeviceName</span></span> | <span data-ttu-id="f8f90-182">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-182">string</span></span> | <span data-ttu-id="f8f90-183">Nom de domaine complet (FQDN) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-183">Fully qualified domain name (FQDN) of the device.</span></span> | <span data-ttu-id="f8f90-184">johnlaptop.europe.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f8f90-184">johnlaptop.europe.contoso.com</span></span>
<span data-ttu-id="f8f90-185">DiskPaths</span><span class="sxs-lookup"><span data-stu-id="f8f90-185">DiskPaths</span></span>  | <span data-ttu-id="f8f90-186">Chaîne de \[ tableau\]</span><span class="sxs-lookup"><span data-stu-id="f8f90-186">Array\[string\]</span></span> | <span data-ttu-id="f8f90-187">Preuve disque que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-187">Disk evidence that the product is installed on the device.</span></span> | <span data-ttu-id="f8f90-188">[ « C:\Program Files (x86)\Microsoft\Silverlight\Application\silverlight.exe » ]</span><span class="sxs-lookup"><span data-stu-id="f8f90-188">[ "C:\Program Files (x86)\Microsoft\Silverlight\Application\silverlight.exe" ]</span></span>
<span data-ttu-id="f8f90-189">ExploitabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f8f90-189">ExploitabilityLevel</span></span> | <span data-ttu-id="f8f90-190">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-190">string</span></span> | <span data-ttu-id="f8f90-191">Le niveau d’exploitabilité de cette vulnérabilité (NoExploit, ExploitIsPublic, ExploitIsVerified, ExploitIsInKit)</span><span class="sxs-lookup"><span data-stu-id="f8f90-191">The exploitability level of this vulnerability (NoExploit, ExploitIsPublic, ExploitIsVerified, ExploitIsInKit)</span></span> | <span data-ttu-id="f8f90-192">ExploitIsInKit</span><span class="sxs-lookup"><span data-stu-id="f8f90-192">ExploitIsInKit</span></span>
<span data-ttu-id="f8f90-193">FirstSeenTimestamp</span><span class="sxs-lookup"><span data-stu-id="f8f90-193">FirstSeenTimestamp</span></span> | <span data-ttu-id="f8f90-194">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-194">string</span></span> | <span data-ttu-id="f8f90-195">Première fois que la CVE de ce produit a été vue sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-195">First time the CVE of this product was seen on the device.</span></span> | <span data-ttu-id="f8f90-196">2020-11-03 10:13:34.8476880</span><span class="sxs-lookup"><span data-stu-id="f8f90-196">2020-11-03 10:13:34.8476880</span></span>
<span data-ttu-id="f8f90-197">ID</span><span class="sxs-lookup"><span data-stu-id="f8f90-197">Id</span></span> | <span data-ttu-id="f8f90-198">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-198">string</span></span> | <span data-ttu-id="f8f90-199">Identificateur unique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f8f90-199">Unique identifier for the record.</span></span> | <span data-ttu-id="f8f90-200">123ABG55_573AG&mnp!</span><span class="sxs-lookup"><span data-stu-id="f8f90-200">123ABG55_573AG&mnp!</span></span>
<span data-ttu-id="f8f90-201">LastSeenTimestamp</span><span class="sxs-lookup"><span data-stu-id="f8f90-201">LastSeenTimestamp</span></span> | <span data-ttu-id="f8f90-202">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-202">string</span></span> | <span data-ttu-id="f8f90-203">Dernière fois que la CVE a été vue sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-203">Last time the CVE was seen on the device.</span></span> | <span data-ttu-id="f8f90-204">2020-11-03 10:13:34.8476880</span><span class="sxs-lookup"><span data-stu-id="f8f90-204">2020-11-03 10:13:34.8476880</span></span>
<span data-ttu-id="f8f90-205">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="f8f90-205">OSPlatform</span></span> | <span data-ttu-id="f8f90-206">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-206">string</span></span> | <span data-ttu-id="f8f90-207">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-207">Platform of the operating system running on the device.</span></span> <span data-ttu-id="f8f90-208">Cette propriété indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8f90-208">This property indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> <span data-ttu-id="f8f90-209">Pour plus d’informations, voir les systèmes d’exploitation et les plateformes pris en charge par tvm.</span><span class="sxs-lookup"><span data-stu-id="f8f90-209">See tvm supported operating systems and platforms for details.</span></span> | <span data-ttu-id="f8f90-210">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f8f90-210">Windows10</span></span>
<span data-ttu-id="f8f90-211">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f90-211">RbacGroupName</span></span>  | <span data-ttu-id="f8f90-212">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-212">string</span></span> | <span data-ttu-id="f8f90-213">Groupe de contrôle d’accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="f8f90-213">The role-based access control (RBAC) group.</span></span> <span data-ttu-id="f8f90-214">Si cet appareil n’est affecté à aucun groupe RBAC, la valeur sera « Unassigned ».</span><span class="sxs-lookup"><span data-stu-id="f8f90-214">If this device is not assigned to any RBAC group, the value will be “Unassigned.”</span></span> <span data-ttu-id="f8f90-215">Si l’organisation ne contient aucun groupe RBAC, la valeur sera « None ».</span><span class="sxs-lookup"><span data-stu-id="f8f90-215">If the organization doesn’t contain any RBAC groups, the value will be “None.”</span></span> | <span data-ttu-id="f8f90-216">Serveurs</span><span class="sxs-lookup"><span data-stu-id="f8f90-216">Servers</span></span>
<span data-ttu-id="f8f90-217">RecommendationReference</span><span class="sxs-lookup"><span data-stu-id="f8f90-217">RecommendationReference</span></span> | <span data-ttu-id="f8f90-218">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-218">string</span></span> | <span data-ttu-id="f8f90-219">Référence à l’ID de recommandation associé à ce logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-219">A reference to the recommendation ID related to this software.</span></span> | <span data-ttu-id="f8f90-220">va-_-microsoft-_-silverlight</span><span class="sxs-lookup"><span data-stu-id="f8f90-220">va-_-microsoft-_-silverlight</span></span>
<span data-ttu-id="f8f90-221">RecommendedSecurityUpdate (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f8f90-221">RecommendedSecurityUpdate (optional)</span></span> | <span data-ttu-id="f8f90-222">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-222">string</span></span> | <span data-ttu-id="f8f90-223">Nom ou description de la mise à jour de sécurité fournie par le fournisseur de logiciels pour résoudre la vulnérabilité.</span><span class="sxs-lookup"><span data-stu-id="f8f90-223">Name or description of the security update provided by the software vendor to address the vulnerability.</span></span> | <span data-ttu-id="f8f90-224">Mises à jour de sécurité d’avril 2020</span><span class="sxs-lookup"><span data-stu-id="f8f90-224">April 2020 Security Updates</span></span>
<span data-ttu-id="f8f90-225">RecommendedSecurityUpdateId (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f8f90-225">RecommendedSecurityUpdateId (optional)</span></span> | <span data-ttu-id="f8f90-226">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-226">string</span></span> | <span data-ttu-id="f8f90-227">Identificateur des mises à jour de sécurité applicables ou identificateur pour les articles de base de connaissances ou de conseils correspondants</span><span class="sxs-lookup"><span data-stu-id="f8f90-227">Identifier of the applicable security updates or identifier for the corresponding guidance or knowledge base (KB) articles</span></span> | <span data-ttu-id="f8f90-228">4550961</span><span class="sxs-lookup"><span data-stu-id="f8f90-228">4550961</span></span>
<span data-ttu-id="f8f90-229">RegistryPaths</span><span class="sxs-lookup"><span data-stu-id="f8f90-229">RegistryPaths</span></span>  | <span data-ttu-id="f8f90-230">Chaîne de \[ tableau\]</span><span class="sxs-lookup"><span data-stu-id="f8f90-230">Array\[string\]</span></span> | <span data-ttu-id="f8f90-231">Preuve dans le Registre que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-231">Registry evidence that the product is installed in the device.</span></span> | <span data-ttu-id="f8f90-232">[ « HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall\MicrosoftSilverlight » ]</span><span class="sxs-lookup"><span data-stu-id="f8f90-232">[ "HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall\MicrosoftSilverlight" ]</span></span>
<span data-ttu-id="f8f90-233">SoftwareName</span><span class="sxs-lookup"><span data-stu-id="f8f90-233">SoftwareName</span></span> | <span data-ttu-id="f8f90-234">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-234">string</span></span> | <span data-ttu-id="f8f90-235">Nom du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-235">Name of the software product.</span></span> | <span data-ttu-id="f8f90-236">chrome</span><span class="sxs-lookup"><span data-stu-id="f8f90-236">chrome</span></span>
<span data-ttu-id="f8f90-237">SoftwareVendor</span><span class="sxs-lookup"><span data-stu-id="f8f90-237">SoftwareVendor</span></span> | <span data-ttu-id="f8f90-238">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-238">string</span></span> | <span data-ttu-id="f8f90-239">Nom du fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="f8f90-239">Name of the software vendor.</span></span> | <span data-ttu-id="f8f90-240">google</span><span class="sxs-lookup"><span data-stu-id="f8f90-240">google</span></span>
<span data-ttu-id="f8f90-241">SoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="f8f90-241">SoftwareVersion</span></span> | <span data-ttu-id="f8f90-242">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-242">string</span></span> | <span data-ttu-id="f8f90-243">Numéro de version du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-243">Version number of the software product.</span></span> | <span data-ttu-id="f8f90-244">81.0.4044.138</span><span class="sxs-lookup"><span data-stu-id="f8f90-244">81.0.4044.138</span></span>
<span data-ttu-id="f8f90-245">VulnerabilitySeverityLevel</span><span class="sxs-lookup"><span data-stu-id="f8f90-245">VulnerabilitySeverityLevel</span></span>  | <span data-ttu-id="f8f90-246">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-246">string</span></span> | <span data-ttu-id="f8f90-247">Niveau de gravité affecté à la vulnérabilité de sécurité en fonction du score CVSS et des facteurs dynamiques influencés par le paysage des menaces.</span><span class="sxs-lookup"><span data-stu-id="f8f90-247">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape.</span></span> | <span data-ttu-id="f8f90-248">Moyenne</span><span class="sxs-lookup"><span data-stu-id="f8f90-248">Medium</span></span>

### <a name="16-examples"></a><span data-ttu-id="f8f90-249">1.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="f8f90-249">1.6 Examples</span></span>

#### <a name="161-request-example"></a><span data-ttu-id="f8f90-250">1.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="f8f90-250">1.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SoftwareVulnerabilitiesByMachine?pageSize=5
```

#### <a name="162-response-example"></a><span data-ttu-id="f8f90-251">1.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="f8f90-251">1.6.2 Response example</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.AssetVulnerability)",
    "value": [
        {
            "id": "00044f612345baf759462dbe6db733b6a9c59ab4_edge_10.0.17763.1637__",
            "deviceId": "00044f612345daf756462bde6bd733b9a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663b45912eed224b2de2f5ea3142726e63f16a.DomainPII_21eeb80d089e79bdfa178eabfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "osArchitecture": "x64",
            "softwareVendor": "microsoft",
            "softwareName": "edge",
            "softwareVersion": "10.0.17763.1637",
            "cveId": null,
            "vulnerabilitySeverityLevel": null,
            "recommendedSecurityUpdate": null,
            "recommendedSecurityUpdateId": null,
            "recommendedSecurityUpdateUrl": null,
            "diskPaths": [],
            "registryPaths": [],
            "lastSeenTimestamp": "2020-12-30 14:17:26",
            "firstSeenTimestamp": "2020-12-30 11:07:15",
            "exploitabilityLevel": "NoExploit",
            "recommendationReference": "va-_-microsoft-_-edge"
        },
        {
            "id": "00044f912345baf756462bde6db733b9a9c56ad4_.net_framework_4.0.0.0__",
            "deviceId": "00044f912345daf756462bde6db733b6a9c59ad4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663b45912eed224b2be2f5ea3142726e63f16a.DomainPII_21eeb80b086e79bdfa178eabfa25e8de6acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "osArchitecture": "x64",
            "softwareVendor": "microsoft",
            "softwareName": ".net_framework",
            "softwareVersion": "4.0.0.0",
            "cveId": null,
            "vulnerabilitySeverityLevel": null,
            "recommendedSecurityUpdate": null,
            "recommendedSecurityUpdateId": null,
            "recommendedSecurityUpdateUrl": null,
            "diskPaths": [],
            "registryPaths": [
                "SOFTWARE\\Microsoft\\NET Framework Setup\\NDP\\v4.0\\Client\\Install"
            ],
            "lastSeenTimestamp": "2020-12-30 13:18:33",
            "firstSeenTimestamp": "2020-12-30 11:07:15",
            "exploitabilityLevel": "NoExploit",
            "recommendationReference": "va-_-microsoft-_-.net_framework"
        },
        {
            "id": "00044f912345baf756462dbe6db733d6a9c59ab4_system_center_2012_endpoint_protection_4.10.209.0__",
            "deviceId": "00044f912345daf756462bde6db733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663b45912eed224b2be2f5ea3142726e63f16a.DomainPII_21eed80b089e79bdfa178eadfa25e8be6acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "osArchitecture": "x64",
            "softwareVendor": "microsoft",
            "softwareName": "system_center_2012_endpoint_protection",
            "softwareVersion": "4.10.209.0",
            "cveId": null,
            "vulnerabilitySeverityLevel": null,
            "recommendedSecurityUpdate": null,
            "recommendedSecurityUpdateId": null,
            "recommendedSecurityUpdateUrl": null,
            "diskPaths": [],
            "registryPaths": [
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Microsoft Security Client"
            ],
            "lastSeenTimestamp": "2020-12-30 14:17:26",
            "firstSeenTimestamp": "2020-12-30 11:07:15",
            "exploitabilityLevel": "NoExploit",
            "recommendationReference": "va-_-microsoft-_-system_center_2012_endpoint_protection"
        },
        {
            "id": "00044f612345bdaf759462dbe6bd733b6a9c59ab4_onedrive_20.245.1206.2__",
            "deviceId": "00044f91234daf759492dbe6bd733b6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_189663d45612eed224b2be2f5ea3142729e63f16a.DomainPII_21eed80b086e79bdfa178eadfa25e8de6acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "osArchitecture": "x64",
            "softwareVendor": "microsoft",
            "softwareName": "onedrive",
            "softwareVersion": "20.245.1206.2",
            "cveId": null,
            "vulnerabilitySeverityLevel": null,
            "recommendedSecurityUpdate": null,
            "recommendedSecurityUpdateId": null,
            "recommendedSecurityUpdateUrl": null,
            "diskPaths": [],
            "registryPaths": [
                "HKEY_USERS\\S-1-5-21-2944539346-1310925172-2349113062-1001\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\OneDriveSetup.exe"
            ],
            "lastSeenTimestamp": "2020-12-30 13:18:33",
            "firstSeenTimestamp": "2020-12-30 11:07:15",
            "exploitabilityLevel": "NoExploit",
            "recommendationReference": "va-_-microsoft-_-onedrive"
        },
        {
            "id": "00044f912345daf759462bde6db733b6a9c56ab4_windows_10_10.0.17763.1637__",
            "deviceId": "00044f912345daf756462dbe6db733d6a9c59ab4",
            "rbacGroupName": "hhh",
            "deviceName": "ComputerPII_18663b45912eeb224d2be2f5ea3142729e63f16a.DomainPII_21eeb80d086e79bdfa178eadfa25e8de6acfa346.corp.contoso.com",
            "osPlatform": "Windows10",
            "osVersion": "10.0.17763.1637",
            "osArchitecture": "x64",
            "softwareVendor": "microsoft",
            "softwareName": "windows_10",
            "softwareVersion": "10.0.17763.1637",
            "cveId": null,
            "vulnerabilitySeverityLevel": null,
            "recommendedSecurityUpdate": null,
            "recommendedSecurityUpdateId": null,
            "recommendedSecurityUpdateUrl": null,
            "diskPaths": [],
            "registryPaths": [],
            "lastSeenTimestamp": "2020-12-30 14:17:26",
            "firstSeenTimestamp": "2020-12-30 11:07:15",
            "exploitabilityLevel": "NoExploit",
            "recommendationReference": "va-_-microsoft-_-windows_10"
        }
    ],
    "@odata.nextLink": "https://api.securitycenter.microsoft.com/api/machines/SoftwareVulnerabilitiesByMachine?pagesize=5&$skiptoken=eyJFeHBvcnREZWZpbml0aW9uIjp7IlRpbWVQYXRoIjoiMjAyMS0wMS0xMS8xMTAxLyJ9LCJFeHBvcnRGaWxlSW5kZXgiOjAsIkxpbmVTdG9wcGVkQXQiOjV9"
}
```

## <a name="2-export-software-vulnerabilities-assessment-via-files"></a><span data-ttu-id="f8f90-252">2. Exporter l’évaluation des vulnérabilités logicielles (via des fichiers)</span><span class="sxs-lookup"><span data-stu-id="f8f90-252">2. Export software vulnerabilities assessment (via files)</span></span>

### <a name="21-api-method-description"></a><span data-ttu-id="f8f90-253">2.1 Description de la méthode API</span><span class="sxs-lookup"><span data-stu-id="f8f90-253">2.1 API method description</span></span>

<span data-ttu-id="f8f90-254">Cette réponse API contient toutes les données des logiciels installés par appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-254">This API response contains all the data of installed software per device.</span></span> <span data-ttu-id="f8f90-255">Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CVEID.</span><span class="sxs-lookup"><span data-stu-id="f8f90-255">Returns a table with an entry for every unique combination of DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CVEID.</span></span>

#### <a name="212-limitations"></a><span data-ttu-id="f8f90-256">2.1.2 Limitations</span><span class="sxs-lookup"><span data-stu-id="f8f90-256">2.1.2 Limitations</span></span>

<span data-ttu-id="f8f90-257">Les limites de taux pour cette API sont de 5 appels par minute et de 20 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f8f90-257">Rate limitations for this API are 5 calls per minute and 20 calls per hour.</span></span>

### <a name="22-permissions"></a><span data-ttu-id="f8f90-258">2.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="f8f90-258">2.2 Permissions</span></span>

<span data-ttu-id="f8f90-259">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f8f90-259">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f8f90-260">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f8f90-260">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details](apis-intro.md).</span></span>

<span data-ttu-id="f8f90-261">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-261">Permission type</span></span> | <span data-ttu-id="f8f90-262">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-262">Permission</span></span> | <span data-ttu-id="f8f90-263">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-263">Permission display name</span></span>
---|---|---
<span data-ttu-id="f8f90-264">Application</span><span class="sxs-lookup"><span data-stu-id="f8f90-264">Application</span></span> | <span data-ttu-id="f8f90-265">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="f8f90-265">Vulnerability.Read.All</span></span> | <span data-ttu-id="f8f90-266">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="f8f90-266">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="f8f90-267">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f8f90-267">Delegated (work or school account)</span></span> | <span data-ttu-id="f8f90-268">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="f8f90-268">Vulnerability.Read</span></span> | <span data-ttu-id="f8f90-269">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="f8f90-269">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

### <a name="23-url"></a><span data-ttu-id="f8f90-270">2.3 URL</span><span class="sxs-lookup"><span data-stu-id="f8f90-270">2.3 URL</span></span>

```http
GET /api/machines/SoftwareVulnerabilitiesExport
```

### <a name="24-parameters"></a><span data-ttu-id="f8f90-271">2.4 Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8f90-271">2.4 Parameters</span></span>

- <span data-ttu-id="f8f90-272">sasValidHours : nombre d’heures pendant qui les URL de téléchargement seront valides (maximum 24 heures)</span><span class="sxs-lookup"><span data-stu-id="f8f90-272">sasValidHours – The number of hours that the download URLs will be valid for (Maximum 24 hours)</span></span>

### <a name="25-properties"></a><span data-ttu-id="f8f90-273">2.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8f90-273">2.5 Properties</span></span>

>[!Note]
>
>- <span data-ttu-id="f8f90-274">Les fichiers sont compressés gzip & au format Json multiligne.</span><span class="sxs-lookup"><span data-stu-id="f8f90-274">The files are gzip compressed & in multiline Json format.</span></span>
>
>- <span data-ttu-id="f8f90-275">Les URL de téléchargement ne sont valides que pendant 3 heures . Sinon, vous pouvez utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8f90-275">The download URLs are only valid for 3 hours; otherwise you can use the parameter.</span></span>
>
>- <span data-ttu-id="f8f90-276">Pour une vitesse de téléchargement maximale de vos données, vous pouvez vous assurer que vous téléchargez à partir de la même région Azure que vos données résident.</span><span class="sxs-lookup"><span data-stu-id="f8f90-276">For maximum download speed of your data, you can make sure you are downloading from the same Azure region that your data resides.</span></span>
>

>[!Note]
>
>- <span data-ttu-id="f8f90-277">Chaque enregistrement représente environ 1 To de données.</span><span class="sxs-lookup"><span data-stu-id="f8f90-277">Each record is approximately 1KB of data.</span></span> <span data-ttu-id="f8f90-278">Vous devez prendre cela en compte lors du choix du paramètre pageSize approprié pour vous.</span><span class="sxs-lookup"><span data-stu-id="f8f90-278">You should take this into account when choosing the correct pageSize parameter for you.</span></span>
>
>- <span data-ttu-id="f8f90-279">Certaines colonnes supplémentaires peuvent être renvoyées dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="f8f90-279">Some additional columns might be returned in the response.</span></span> <span data-ttu-id="f8f90-280">Ces colonnes sont temporaires et peuvent être supprimées. Utilisez uniquement les colonnes documentées.</span><span class="sxs-lookup"><span data-stu-id="f8f90-280">These columns are temporary and might be removed, please use only the documented columns.</span></span>
>

<span data-ttu-id="f8f90-281">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="f8f90-281">Property (ID)</span></span> | <span data-ttu-id="f8f90-282">Type de données</span><span class="sxs-lookup"><span data-stu-id="f8f90-282">Data type</span></span> | <span data-ttu-id="f8f90-283">Description</span><span class="sxs-lookup"><span data-stu-id="f8f90-283">Description</span></span> | <span data-ttu-id="f8f90-284">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8f90-284">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="f8f90-285">Exporter des fichiers</span><span class="sxs-lookup"><span data-stu-id="f8f90-285">Export files</span></span> | <span data-ttu-id="f8f90-286">chaîne de \[ tableau\]</span><span class="sxs-lookup"><span data-stu-id="f8f90-286">array\[string\]</span></span>  | <span data-ttu-id="f8f90-287">Liste des URL de téléchargement pour les fichiers qui contiennent la capture instantanée actuelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8f90-287">A list of download URLs for files holding the current snapshot of the organization.</span></span> | <span data-ttu-id="f8f90-288">[  “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2”  ]</span><span class="sxs-lookup"><span data-stu-id="f8f90-288">[  “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...1”, “https://tvmexportstrstgeus.blob.core.windows.net/tvm-export...2”  ]</span></span>
<span data-ttu-id="f8f90-289">GeneratedTime</span><span class="sxs-lookup"><span data-stu-id="f8f90-289">GeneratedTime</span></span> | <span data-ttu-id="f8f90-290">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-290">string</span></span> | <span data-ttu-id="f8f90-291">Heure de la générer.</span><span class="sxs-lookup"><span data-stu-id="f8f90-291">The time that the export was generated.</span></span> | <span data-ttu-id="f8f90-292">2021-05-20T08:00:00Z</span><span class="sxs-lookup"><span data-stu-id="f8f90-292">2021-05-20T08:00:00Z</span></span>

### <a name="26-examples"></a><span data-ttu-id="f8f90-293">2.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="f8f90-293">2.6 Examples</span></span>

#### <a name="261-request-example"></a><span data-ttu-id="f8f90-294">2.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="f8f90-294">2.6.1 Request example</span></span>

```http
GET https://api-us.securitycenter.contoso.com/api/machines/SoftwareVulnerabilitiesExport
```

#### <a name="262-response-example"></a><span data-ttu-id="f8f90-295">2.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="f8f90-295">2.6.2 Response example</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.ExportFilesResponse",
    "exportFiles": [
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/VaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00393-bcc26c4f-e531-48db-9892-c93ac5d72d5c.c000.json.gz?sv=2019-12-12&st=2021-01-11T11%3A35%3A13Z&se=2021-01-11T14%3A35%3A13Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/VaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00393-bcc26c4f-e531-48db-9892-c93ac5d72d5c.c001.json.gz?sv=2019-12-12&st=2021-01-11T11%3A35%3A13Z&se=2021-01-11T14%3A35%3A13Z&sr=b&sp=r&sig=...",
        "https://tvmexportstrstgeus.blob.core.windows.net/tvm-export/2021-01-11/1101/VaExport/json/OrgId=12345678-195f-4223-9c7a-99fb420fd000/part-00393-bcc26c4f-e531-48db-9892-c93ac5d72d5c.c002.json.gz?sv=2019-12-12&st=2021-01-11T11%3A35%3A13Z&se=2021-01-11T14%3A35%3A13Z&sr=b&sp=r&sig=..."
    ],
    "generatedTime": "2021-01-11T11:01:00Z"
}
```

## <a name="3-delta-export-software-vulnerabilities-assessment-json-response"></a><span data-ttu-id="f8f90-296">3. Évaluation des vulnérabilités logicielles d’exportation delta (réponse JSON)</span><span class="sxs-lookup"><span data-stu-id="f8f90-296">3. Delta export software vulnerabilities assessment (JSON response)</span></span>

### <a name="31-api-method-description"></a><span data-ttu-id="f8f90-297">3.1 Description de la méthode d’API</span><span class="sxs-lookup"><span data-stu-id="f8f90-297">3.1 API method description</span></span>

<span data-ttu-id="f8f90-298">Renvoie un tableau avec une entrée pour chaque combinaison unique de DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CveId.</span><span class="sxs-lookup"><span data-stu-id="f8f90-298">Returns a table with an entry for every unique combination of DeviceId, SoftwareVendor, SoftwareName, SoftwareVersion, CveId.</span></span> <span data-ttu-id="f8f90-299">L’API tire les données de votre organisation en tant que réponses Json.</span><span class="sxs-lookup"><span data-stu-id="f8f90-299">The API pulls data in your organization as Json responses.</span></span> <span data-ttu-id="f8f90-300">La réponse est paginée, afin que vous pouvez utiliser le champ @odata.nextLink de la réponse pour récupérer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="f8f90-300">The response is paginated, so you can use the @odata.nextLink field from the response to fetch the next results.</span></span> <span data-ttu-id="f8f90-301">Contrairement à l’évaluation complète des vulnérabilités logicielles (réponse JSON), qui permet d’obtenir un instantané complet de l’évaluation des vulnérabilités logicielles de votre organisation par périphérique, l’appel de l’API de réponse JSON d’exportation delta est utilisé pour récupérer uniquement les modifications qui se sont produites entre une date sélectionnée et la date actuelle (l’appel d’API « delta »).</span><span class="sxs-lookup"><span data-stu-id="f8f90-301">Unlike the full software vulnerabilities assessment (JSON response)—which is used to obtain an entire snapshot of the software vulnerabilities assessment of your organization by device—the delta export JSON response API call is used to fetch only the changes that have happened between a selected date and the current date (the “delta” API call).</span></span> <span data-ttu-id="f8f90-302">Au lieu d’obtenir une exportation complète avec une grande quantité de données à chaque fois, vous obtenez uniquement des informations spécifiques sur les vulnérabilités nouvelles, fixes et mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f8f90-302">Instead of getting a full export with a large amount of data every time, you’ll only get specific information on new, fixed, and updated vulnerabilities.</span></span> <span data-ttu-id="f8f90-303">L’appel de l’API de réponse JSON d’exportation delta peut également être utilisé pour calculer différents KPI, tels que « combien de vulnérabilités ont été corrigées ? »</span><span class="sxs-lookup"><span data-stu-id="f8f90-303">Delta export JSON response API call can also be used to calculate different KPIs such as “how many vulnerabilities were fixed?”</span></span> <span data-ttu-id="f8f90-304">ou « combien de nouvelles vulnérabilités ont été ajoutées à mon organisation ? »</span><span class="sxs-lookup"><span data-stu-id="f8f90-304">or “how many new vulnerabilities were added to my organization?”</span></span>

>[!NOTE]
>
><span data-ttu-id="f8f90-305">Il est vivement recommandé d’utiliser l’évaluation complète des vulnérabilités logicielles d’exportation par appel d’API d’appareil au moins une fois par semaine, et cette exportation supplémentaire de vulnérabilités logicielles change par l’API d’appareil (delta) tous les autres jours de la semaine.</span><span class="sxs-lookup"><span data-stu-id="f8f90-305">It is highly recommended you use the full export software vulnerabilities assessment by device API call at least once a week, and this additional export software vulnerabilities changes by device (delta) API call all the other days of the week.</span></span>  <span data-ttu-id="f8f90-306">Contrairement aux autres API de réponse JSON d’évaluations, l'« exportation delta » n’est pas une exportation complète.</span><span class="sxs-lookup"><span data-stu-id="f8f90-306">Unlike the other Assessments JSON response APIs, the “delta export” is not a full export.</span></span> <span data-ttu-id="f8f90-307">L’exportation delta inclut uniquement les modifications qui se sont produites entre une date sélectionnée et la date actuelle (l’appel d’API « delta »).</span><span class="sxs-lookup"><span data-stu-id="f8f90-307">The delta export includes only the changes that have happened between a selected date and the current date (the “delta” API call).</span></span>

#### <a name="311-limitations"></a><span data-ttu-id="f8f90-308">3.1.1 Limitations</span><span class="sxs-lookup"><span data-stu-id="f8f90-308">3.1.1 Limitations</span></span>

- <span data-ttu-id="f8f90-309">La taille maximale de page est de 200 000.</span><span class="sxs-lookup"><span data-stu-id="f8f90-309">Maximum page size is 200,000.</span></span>

- <span data-ttu-id="f8f90-310">Le paramètre sinceTime a un maximum de 14 jours.</span><span class="sxs-lookup"><span data-stu-id="f8f90-310">The sinceTime parameter has a maximum of 14 days.</span></span>

- <span data-ttu-id="f8f90-311">Les limites de taux pour cette API sont de 30 appels par minute et de 1 000 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f8f90-311">Rate limitations for this API are 30 calls per minute and 1000 calls per hour.</span></span>

### <a name="32-permissions"></a><span data-ttu-id="f8f90-312">3.2 Autorisations</span><span class="sxs-lookup"><span data-stu-id="f8f90-312">3.2 Permissions</span></span>

<span data-ttu-id="f8f90-313">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f8f90-313">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f8f90-314">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f8f90-314">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="f8f90-315">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-315">Permission type</span></span> | <span data-ttu-id="f8f90-316">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-316">Permission</span></span> | <span data-ttu-id="f8f90-317">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-317">Permission display name</span></span>
---|---|---
<span data-ttu-id="f8f90-318">Application</span><span class="sxs-lookup"><span data-stu-id="f8f90-318">Application</span></span> | <span data-ttu-id="f8f90-319">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="f8f90-319">Vulnerability.Read.All</span></span> | <span data-ttu-id="f8f90-320">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="f8f90-320">'Read Threat and Vulnerability Management vulnerability information'</span></span>
<span data-ttu-id="f8f90-321">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f8f90-321">Delegated (work or school account)</span></span> | <span data-ttu-id="f8f90-322">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="f8f90-322">Vulnerability.Read</span></span> | <span data-ttu-id="f8f90-323">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="f8f90-323">'Read Threat and Vulnerability Management vulnerability information'</span></span>

### <a name="33-url"></a><span data-ttu-id="f8f90-324">3.3 URL</span><span class="sxs-lookup"><span data-stu-id="f8f90-324">3.3 URL</span></span>

```http
GET /api/machines/SoftwareVulnerabilityChangesByMachine 
```

### <a name="34-parameters"></a><span data-ttu-id="f8f90-325">3.4 Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8f90-325">3.4 Parameters</span></span>

- <span data-ttu-id="f8f90-326">sinceTime (obligatoire) : données entre une heure sélectionnée et aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="f8f90-326">sinceTime (required) – The data between a selected time and today.</span></span>
- <span data-ttu-id="f8f90-327">pageSize (valeur par défaut = 50 000) : nombre de résultats en réponse</span><span class="sxs-lookup"><span data-stu-id="f8f90-327">pageSize (default = 50,000) – number of results in response</span></span>
- <span data-ttu-id="f8f90-328">$top : nombre de résultats à renvoyer (ne retourne pas @odata.nextLink et, par conséquent, ne tire pas toutes les données)</span><span class="sxs-lookup"><span data-stu-id="f8f90-328">$top – number of results to return (doesn’t return @odata.nextLink and therefore doesn’t pull all the data)</span></span>

### <a name="35-properties"></a><span data-ttu-id="f8f90-329">3.5 Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8f90-329">3.5 Properties</span></span>

<span data-ttu-id="f8f90-330">Chaque enregistrement renvoyé contient toutes les données de l’évaluation complète des vulnérabilités logicielles d’exportation par API d’appareil, ainsi que deux champs supplémentaires :  _**EventTimestamp**_ et _**Status**_.</span><span class="sxs-lookup"><span data-stu-id="f8f90-330">Each returned record contains all the data from the full export software vulnerabilities assessment by device API, plus two additional fields:  _**EventTimestamp**_ and _**Status**_.</span></span>

>[!NOTE]
>- <span data-ttu-id="f8f90-331">Certaines colonnes supplémentaires peuvent être renvoyées dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="f8f90-331">Some additional columns might be returned in the response.</span></span> <span data-ttu-id="f8f90-332">Ces colonnes sont temporaires et peuvent être supprimées. Utilisez donc uniquement les colonnes documentées.</span><span class="sxs-lookup"><span data-stu-id="f8f90-332">These columns are temporary and might be removed, so please use only the documented columns.</span></span>
>
>- <span data-ttu-id="f8f90-333">Les propriétés définies dans le tableau suivant sont répertoriées par ordre alphabétique, par ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="f8f90-333">The properties defined in the following table are listed alphabetically, by property ID.</span></span>  <span data-ttu-id="f8f90-334">Lors de l’exécution de cette API, la sortie résultante ne sera pas nécessairement renvoyée dans le même ordre que celui répertorié dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f8f90-334">When running this API, the resulting output will not necessarily be returned in the same order listed in this table.</span></span>
<br><br/>

<span data-ttu-id="f8f90-335">Propriété (ID)</span><span class="sxs-lookup"><span data-stu-id="f8f90-335">Property (ID)</span></span> | <span data-ttu-id="f8f90-336">Type de données</span><span class="sxs-lookup"><span data-stu-id="f8f90-336">Data type</span></span> | <span data-ttu-id="f8f90-337">Description</span><span class="sxs-lookup"><span data-stu-id="f8f90-337">Description</span></span> | <span data-ttu-id="f8f90-338">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8f90-338">Example of returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="f8f90-339">CveId</span><span class="sxs-lookup"><span data-stu-id="f8f90-339">CveId</span></span> | <span data-ttu-id="f8f90-340">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-340">string</span></span> | <span data-ttu-id="f8f90-341">Identificateur unique affecté à la vulnérabilité de sécurité sous le système CVE (Common Vulnerabilities and Exposures).</span><span class="sxs-lookup"><span data-stu-id="f8f90-341">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system.</span></span> | <span data-ttu-id="f8f90-342">CVE-2020-15992</span><span class="sxs-lookup"><span data-stu-id="f8f90-342">CVE-2020-15992</span></span>  
<span data-ttu-id="f8f90-343">CvssScore</span><span class="sxs-lookup"><span data-stu-id="f8f90-343">CvssScore</span></span> | <span data-ttu-id="f8f90-344">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-344">string</span></span> | <span data-ttu-id="f8f90-345">Score CVSS de la CVE.</span><span class="sxs-lookup"><span data-stu-id="f8f90-345">The CVSS score of the CVE.</span></span> | <span data-ttu-id="f8f90-346">6.2</span><span class="sxs-lookup"><span data-stu-id="f8f90-346">6.2</span></span>  
<span data-ttu-id="f8f90-347">DeviceId</span><span class="sxs-lookup"><span data-stu-id="f8f90-347">DeviceId</span></span> | <span data-ttu-id="f8f90-348">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-348">string</span></span> | <span data-ttu-id="f8f90-349">Identificateur unique de l’appareil dans le service.</span><span class="sxs-lookup"><span data-stu-id="f8f90-349">Unique identifier for the device in the service.</span></span> | <span data-ttu-id="f8f90-350">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span><span class="sxs-lookup"><span data-stu-id="f8f90-350">9eaf3a8b5962e0e6b1af9ec756664a9b823df2d1</span></span>  
<span data-ttu-id="f8f90-351">DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8f90-351">DeviceName</span></span> | <span data-ttu-id="f8f90-352">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-352">string</span></span> | <span data-ttu-id="f8f90-353">Nom de domaine complet (FQDN) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-353">Fully qualified domain name (FQDN) of the device.</span></span> | <span data-ttu-id="f8f90-354">johnlaptop.europe.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f8f90-354">johnlaptop.europe.contoso.com</span></span>  
<span data-ttu-id="f8f90-355">DiskPaths</span><span class="sxs-lookup"><span data-stu-id="f8f90-355">DiskPaths</span></span> | <span data-ttu-id="f8f90-356">Array[string]</span><span class="sxs-lookup"><span data-stu-id="f8f90-356">Array[string]</span></span> | <span data-ttu-id="f8f90-357">Preuve disque que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-357">Disk evidence that the product is installed on the device.</span></span> | <span data-ttu-id="f8f90-358">[ « C:\Program Files (x86)\Microsoft\Silverlight\Application\silverlight.exe » ]</span><span class="sxs-lookup"><span data-stu-id="f8f90-358">[ "C:\Program Files (x86)\Microsoft\Silverlight\Application\silverlight.exe" ]</span></span>  
<span data-ttu-id="f8f90-359">EventTimestamp</span><span class="sxs-lookup"><span data-stu-id="f8f90-359">EventTimestamp</span></span> | <span data-ttu-id="f8f90-360">String</span><span class="sxs-lookup"><span data-stu-id="f8f90-360">String</span></span> | <span data-ttu-id="f8f90-361">Heure de la découverte de cet événement delta.</span><span class="sxs-lookup"><span data-stu-id="f8f90-361">The time this delta event was found.</span></span> | <span data-ttu-id="f8f90-362">2021-01-11T11:06:08.291Z</span><span class="sxs-lookup"><span data-stu-id="f8f90-362">2021-01-11T11:06:08.291Z</span></span>
<span data-ttu-id="f8f90-363">ExploitabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f8f90-363">ExploitabilityLevel</span></span> | <span data-ttu-id="f8f90-364">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-364">string</span></span> | <span data-ttu-id="f8f90-365">Le niveau d’exploitabilité de cette vulnérabilité (NoExploit, ExploitIsPublic, ExploitIsVerified, ExploitIsInKit)</span><span class="sxs-lookup"><span data-stu-id="f8f90-365">The exploitability level of this vulnerability (NoExploit, ExploitIsPublic, ExploitIsVerified, ExploitIsInKit)</span></span> | <span data-ttu-id="f8f90-366">ExploitIsInKit</span><span class="sxs-lookup"><span data-stu-id="f8f90-366">ExploitIsInKit</span></span>  
<span data-ttu-id="f8f90-367">FirstSeenTimestamp</span><span class="sxs-lookup"><span data-stu-id="f8f90-367">FirstSeenTimestamp</span></span> | <span data-ttu-id="f8f90-368">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-368">string</span></span> | <span data-ttu-id="f8f90-369">Première fois que la CVE de ce produit a été vue sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-369">First time the CVE of this product was seen on the device.</span></span> | <span data-ttu-id="f8f90-370">2020-11-03 10:13:34.8476880</span><span class="sxs-lookup"><span data-stu-id="f8f90-370">2020-11-03 10:13:34.8476880</span></span>  
<span data-ttu-id="f8f90-371">ID</span><span class="sxs-lookup"><span data-stu-id="f8f90-371">Id</span></span> | <span data-ttu-id="f8f90-372">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-372">string</span></span> | <span data-ttu-id="f8f90-373">Identificateur unique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f8f90-373">Unique identifier for the record.</span></span> | <span data-ttu-id="f8f90-374">123ABG55_573AG&mnp!</span><span class="sxs-lookup"><span data-stu-id="f8f90-374">123ABG55_573AG&mnp!</span></span>  
<span data-ttu-id="f8f90-375">LastSeenTimestamp</span><span class="sxs-lookup"><span data-stu-id="f8f90-375">LastSeenTimestamp</span></span> | <span data-ttu-id="f8f90-376">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-376">string</span></span> | <span data-ttu-id="f8f90-377">Dernière fois que la CVE a été vue sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-377">Last time the CVE was seen on the device.</span></span> | <span data-ttu-id="f8f90-378">2020-11-03 10:13:34.8476880</span><span class="sxs-lookup"><span data-stu-id="f8f90-378">2020-11-03 10:13:34.8476880</span></span>  
<span data-ttu-id="f8f90-379">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="f8f90-379">OSPlatform</span></span> | <span data-ttu-id="f8f90-380">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-380">string</span></span> | <span data-ttu-id="f8f90-381">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-381">Platform of the operating system running on the device.</span></span> <span data-ttu-id="f8f90-382">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8f90-382">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> <span data-ttu-id="f8f90-383">Pour plus d’informations, voir les systèmes d’exploitation et les plateformes pris en charge par tvm.</span><span class="sxs-lookup"><span data-stu-id="f8f90-383">See tvm supported operating systems and platforms for details.</span></span> | <span data-ttu-id="f8f90-384">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f8f90-384">Windows10</span></span>  
<span data-ttu-id="f8f90-385">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f90-385">RbacGroupName</span></span> | <span data-ttu-id="f8f90-386">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-386">string</span></span> | <span data-ttu-id="f8f90-387">Groupe de contrôle d’accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="f8f90-387">The role-based access control (RBAC) group.</span></span> <span data-ttu-id="f8f90-388">Si cet appareil n’est affecté à aucun groupe RBAC, la valeur sera « Unassigned ».</span><span class="sxs-lookup"><span data-stu-id="f8f90-388">If this device is not assigned to any RBAC group, the value will be “Unassigned.”</span></span> <span data-ttu-id="f8f90-389">Si l’organisation ne contient aucun groupe RBAC, la valeur sera « None ».</span><span class="sxs-lookup"><span data-stu-id="f8f90-389">If the organization doesn’t contain any RBAC groups, the value will be “None.”</span></span> | <span data-ttu-id="f8f90-390">Serveurs</span><span class="sxs-lookup"><span data-stu-id="f8f90-390">Servers</span></span>  
<span data-ttu-id="f8f90-391">RecommendationReference</span><span class="sxs-lookup"><span data-stu-id="f8f90-391">RecommendationReference</span></span> | <span data-ttu-id="f8f90-392">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-392">string</span></span> | <span data-ttu-id="f8f90-393">Référence à l’ID de recommandation associé à ce logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-393">A reference to the recommendation ID related to this software.</span></span> | <span data-ttu-id="f8f90-394">va--microsoft--silverlight</span><span class="sxs-lookup"><span data-stu-id="f8f90-394">va--microsoft--silverlight</span></span>  
<span data-ttu-id="f8f90-395">RecommendedSecurityUpdate</span><span class="sxs-lookup"><span data-stu-id="f8f90-395">RecommendedSecurityUpdate</span></span>  | <span data-ttu-id="f8f90-396">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-396">string</span></span> | <span data-ttu-id="f8f90-397">Nom ou description de la mise à jour de sécurité fournie par le fournisseur de logiciels pour résoudre la vulnérabilité.</span><span class="sxs-lookup"><span data-stu-id="f8f90-397">Name or description of the security update provided by the software vendor to address the vulnerability.</span></span> | <span data-ttu-id="f8f90-398">Mises à jour de sécurité d’avril 2020</span><span class="sxs-lookup"><span data-stu-id="f8f90-398">April 2020 Security Updates</span></span>  
<span data-ttu-id="f8f90-399">RecommendedSecurityUpdateId</span><span class="sxs-lookup"><span data-stu-id="f8f90-399">RecommendedSecurityUpdateId</span></span>  | <span data-ttu-id="f8f90-400">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-400">string</span></span> | <span data-ttu-id="f8f90-401">Identificateur des mises à jour de sécurité applicables ou identificateur pour les articles de base de connaissances ou de conseils correspondants</span><span class="sxs-lookup"><span data-stu-id="f8f90-401">Identifier of the applicable security updates or identifier for the corresponding guidance or knowledge base (KB) articles</span></span> | <span data-ttu-id="f8f90-402">4550961</span><span class="sxs-lookup"><span data-stu-id="f8f90-402">4550961</span></span>  
<span data-ttu-id="f8f90-403">RegistryPaths</span><span class="sxs-lookup"><span data-stu-id="f8f90-403">RegistryPaths</span></span>  | <span data-ttu-id="f8f90-404">Array[string]</span><span class="sxs-lookup"><span data-stu-id="f8f90-404">Array[string]</span></span> | <span data-ttu-id="f8f90-405">Preuve dans le Registre que le produit est installé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8f90-405">Registry evidence that the product is installed in the device.</span></span> | <span data-ttu-id="f8f90-406">[ « HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall\Google Chrome » ]</span><span class="sxs-lookup"><span data-stu-id="f8f90-406">[ "HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall\Google Chrome" ]</span></span>  
<span data-ttu-id="f8f90-407">SoftwareName</span><span class="sxs-lookup"><span data-stu-id="f8f90-407">SoftwareName</span></span> | <span data-ttu-id="f8f90-408">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-408">string</span></span> | <span data-ttu-id="f8f90-409">Nom du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-409">Name of the software product.</span></span> | <span data-ttu-id="f8f90-410">chrome</span><span class="sxs-lookup"><span data-stu-id="f8f90-410">chrome</span></span>  
<span data-ttu-id="f8f90-411">SoftwareVendor</span><span class="sxs-lookup"><span data-stu-id="f8f90-411">SoftwareVendor</span></span> | <span data-ttu-id="f8f90-412">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-412">string</span></span> | <span data-ttu-id="f8f90-413">Nom du fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="f8f90-413">Name of the software vendor.</span></span> | <span data-ttu-id="f8f90-414">google</span><span class="sxs-lookup"><span data-stu-id="f8f90-414">google</span></span>  
<span data-ttu-id="f8f90-415">SoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="f8f90-415">SoftwareVersion</span></span> | <span data-ttu-id="f8f90-416">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-416">string</span></span> | <span data-ttu-id="f8f90-417">Numéro de version du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f8f90-417">Version number of the software product.</span></span> | <span data-ttu-id="f8f90-418">81.0.4044.138</span><span class="sxs-lookup"><span data-stu-id="f8f90-418">81.0.4044.138</span></span>  
<span data-ttu-id="f8f90-419">Statut</span><span class="sxs-lookup"><span data-stu-id="f8f90-419">Status</span></span> | <span data-ttu-id="f8f90-420">String</span><span class="sxs-lookup"><span data-stu-id="f8f90-420">String</span></span> | <span data-ttu-id="f8f90-421">**Nouveau**   (pour une nouvelle vulnérabilité introduite sur un appareil)  (1) **Corrigé**(si cette vulnérabilité n’existe plus sur l’appareil, ce qui signifie   qu’elle a été corrigée).</span><span class="sxs-lookup"><span data-stu-id="f8f90-421">**New** (for a new vulnerability introduced on a device)  (1) **Fixed** (if this vulnerability doesn’t exist anymore on the device, which means it was remediated).</span></span> <span data-ttu-id="f8f90-422">(2)  **Mise à jour**   (si une vulnérabilité sur un appareil a changé.</span><span class="sxs-lookup"><span data-stu-id="f8f90-422">(2) **Updated** (if a vulnerability on a device has changed.</span></span> <span data-ttu-id="f8f90-423">Les modifications possibles sont les suivants : score CVSS, niveau d’exploitabilité, niveau de gravité, DiskPaths, RegistryPaths, RecommendedSecurityUpdate).</span><span class="sxs-lookup"><span data-stu-id="f8f90-423">The possible changes are: CVSS score, exploitability level, severity level, DiskPaths, RegistryPaths, RecommendedSecurityUpdate).</span></span> | <span data-ttu-id="f8f90-424">Fixed</span><span class="sxs-lookup"><span data-stu-id="f8f90-424">Fixed</span></span>
<span data-ttu-id="f8f90-425">VulnerabilitySeverityLevel</span><span class="sxs-lookup"><span data-stu-id="f8f90-425">VulnerabilitySeverityLevel</span></span> | <span data-ttu-id="f8f90-426">string</span><span class="sxs-lookup"><span data-stu-id="f8f90-426">string</span></span> | <span data-ttu-id="f8f90-427">Niveau de gravité affecté à la vulnérabilité de sécurité en fonction du score CVSS et des facteurs dynamiques influencés par le paysage des menaces.</span><span class="sxs-lookup"><span data-stu-id="f8f90-427">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape.</span></span> | <span data-ttu-id="f8f90-428">Moyenne</span><span class="sxs-lookup"><span data-stu-id="f8f90-428">Medium</span></span>  

#### <a name="clarifications"></a><span data-ttu-id="f8f90-429">Clarifications</span><span class="sxs-lookup"><span data-stu-id="f8f90-429">Clarifications</span></span>

- <span data-ttu-id="f8f90-430">Si le logiciel a été mis à jour de la version 1.0 à la version 2.0 et que les deux versions sont exposées à CVE-A, vous recevrez 2 événements distincts :</span><span class="sxs-lookup"><span data-stu-id="f8f90-430">If the software was updated from version 1.0 to version 2.0, and both versions are exposed to CVE-A, you will receive 2 separate events:</span></span>  
   1. <span data-ttu-id="f8f90-431">Fixe : CVE-A sur la version 1.0 a été corrigé</span><span class="sxs-lookup"><span data-stu-id="f8f90-431">Fixed – CVE-A on version 1.0 was fixed</span></span>  
   1. <span data-ttu-id="f8f90-432">Nouveau : CVE-A sur la version 2.0 a été ajouté</span><span class="sxs-lookup"><span data-stu-id="f8f90-432">New – CVE-A on version 2.0 was added</span></span>

- <span data-ttu-id="f8f90-433">Si une vulnérabilité spécifique (par exemple, CVE-A) a été vue pour la première fois à un moment spécifique (par exemple, le 10 janvier) sur un logiciel avec la version 1.0, et quelques jours plus tard, ce logiciel a été mis à jour vers la version 2.0 qui a également été exposée au même CVE-A, vous recevrez ces deux événements séparés :</span><span class="sxs-lookup"><span data-stu-id="f8f90-433">If a specific vulnerability (for example, CVE-A) was first seen at a specific time (for example, January 10) on software with version 1.0, and a few days later that software was updated to version 2.0 which also exposed to the same CVE-A, you will receive these two separated events:</span></span>  
   1. <span data-ttu-id="f8f90-434">Fixed – CVE-X, FirstSeenTimestamp 10 janvier, version 1,0.</span><span class="sxs-lookup"><span data-stu-id="f8f90-434">Fixed – CVE-X, FirstSeenTimestamp January 10, version 1,0.</span></span>  
   1. <span data-ttu-id="f8f90-435">Nouveauté : CVE-X, FirstSeenTimestamp 10 janvier, version 2.0.</span><span class="sxs-lookup"><span data-stu-id="f8f90-435">New – CVE-X, FirstSeenTimestamp January 10, version 2.0.</span></span>

### <a name="36-examples"></a><span data-ttu-id="f8f90-436">3.6 Exemples</span><span class="sxs-lookup"><span data-stu-id="f8f90-436">3.6 Examples</span></span>

#### <a name="361-request-example"></a><span data-ttu-id="f8f90-437">3.6.1 Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="f8f90-437">3.6.1 Request example</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/SoftwareVulnerabilityChangesByMachine?pageSize=5&sinceTime=2021-05-19T18%3A35%3A49.924Z
```

#### <a name="362-response-example"></a><span data-ttu-id="f8f90-438">3.6.2 Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="f8f90-438">3.6.2 Response example</span></span>

```json
{ 
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.DeltaAssetVulnerability)", 
    "value": [ 
        { 
            "id": "008198251234544f7dfa715e278d4cec0c16c171_chrome_87.0.4280.88__", 
            "deviceId": "008198251234544f7dfa715e278b4cec0c19c171",  
            "rbacGroupName": "hhh", 
            "deviceName": "ComputerPII_1c8fee370690ca24b6a0d3f34d193b0424943a8b8.DomainPII_0dc1aee0fa366d175e514bd91a9e7a5b2b07ee8e.corp.contoso.com", 
            "osPlatform": "Windows10", 
            "osVersion": "10.0.19042.685", 
            "osArchitecture": "x64", 
            "softwareVendor": "google", 
            "softwareName": "chrome", 
            "softwareVersion": "87.0.4280.88", 
            "cveId": null, 
            "vulnerabilitySeverityLevel": null, 
            "recommendedSecurityUpdate": null, 
            "recommendedSecurityUpdateId": null, 
            "recommendedSecurityUpdateUrl": null, 
            "diskPaths": [ 
                "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe" 
            ], 
            "registryPaths": [ 
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Google Chrome" 
            ], 
            "lastSeenTimestamp": "2021-01-04 00:29:42", 
            "firstSeenTimestamp": "2020-11-06 03:12:44", 
            "exploitabilityLevel": "NoExploit", 
            "recommendationReference": "va-_-google-_-chrome", 
            "status": "Fixed", 
            "eventTimestamp": "2021-01-11T11:06:08.291Z" 
        }, 
        { 
            "id": "00e59c61234533860738ecf488eec8abf296e41e_onedrive_20.64.329.3__", 
            "deviceId": "00e56c91234533860738ecf488eec8abf296e41e",  
            "rbacGroupName": "hhh", 
            "deviceName": "ComputerPII_82c13a8ad8cf3dbaf7bf34fada9fa3aebc124116.DomainPII_21eeb80d086e79dbfa178eadfa25e8de9acfa346.corp.contoso.com", 
            "osPlatform": "Windows10", 
            "osVersion": "10.0.18363.1256", 
            "osArchitecture": "x64", 
            "softwareVendor": "microsoft", 
            "softwareName": "onedrive", 
            "softwareVersion": "20.64.329.3", 
            "cveId": null, 
            "vulnerabilitySeverityLevel": null, 
            "recommendedSecurityUpdate": null, 
            "recommendedSecurityUpdateId": null, 
            "recommendedSecurityUpdateUrl": null, 
            "diskPaths": [], 
            "registryPaths": [ 
                "HKEY_USERS\\S-1-5-21-2127521184-1604012920-1887927527-24918864\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\OneDriveSetup.exe" 
            ], 
            "lastSeenTimestamp": "2020-12-11 19:49:48", 
            "firstSeenTimestamp": "2020-12-07 18:25:47", 
            "exploitabilityLevel": "NoExploit", 
            "recommendationReference": "va-_-microsoft-_-onedrive", 
            "status": "Fixed", 
            "eventTimestamp": "2021-01-11T11:06:08.291Z" 
        }, 
        { 
            "id": "01aa8c73095bb12345918663f3f94ce322107d24_firefox_83.0.0.0_CVE-2020-26971_", 
            "deviceId": "01aa8c73065bb12345918693f3f94ce322107d24", 
            "rbacGroupName": "hhh", 
            "deviceName": "ComputerPII_42684eb981bea2d670027e7ad2caafd3f2b381a3.DomainPII_21eed80b086e76dbfa178eabfa25e8de9acfa346.corp.contoso.com", 
            "osPlatform": "Windows10", 
            "osVersion": "10.0.19042.685", 
            "osArchitecture": "x64", 
            "softwareVendor": "mozilla", 
            "softwareName": "firefox", 
            "softwareVersion": "83.0.0.0", 
            "cveId": "CVE-2020-26971", 
            "vulnerabilitySeverityLevel": "High", 
            "recommendedSecurityUpdate": "193220", 
            "recommendedSecurityUpdateId": null, 
            "recommendedSecurityUpdateUrl": null, 
            "diskPaths": [ 
                "C:\\Program Files (x86)\\Mozilla Firefox\\firefox.exe" 
            ], 
            "registryPaths": [ 
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\Mozilla Firefox 83.0 (x86 en-US)" 
            ], 
            "lastSeenTimestamp": "2021-01-05 17:04:30", 
            "firstSeenTimestamp": "2020-05-06 12:42:19", 
            "exploitabilityLevel": "NoExploit", 
            "recommendationReference": "va-_-mozilla-_-firefox", 
            "status": "Fixed", 
            "eventTimestamp": "2021-01-11T11:06:08.291Z" 
        }, 
        { 
            "id": "026f0fcb12345fbd2decd1a339702131422d362e_project_16.0.13701.20000__", 
            "deviceId": "029f0fcb13245fbd2decd1a336702131422d392e", 
            "rbacGroupName": "hhh", 
            "deviceName": "ComputerPII_a5706750acba75f15d69cd17f4a7fcd268d6422c.DomainPII_f290e982685f7e8eee168b4332e0ae5d2a069cd6.corp.contoso.com", 
            "osPlatform": "Windows10", 
            "osVersion": "10.0.19042.685", 
            "osArchitecture": "x64", 
            "softwareVendor": "microsoft", 
            "softwareName": "project", 
            "softwareVersion": "16.0.13701.20000", 
            "cveId": null, 
            "vulnerabilitySeverityLevel": null, 
            "recommendedSecurityUpdate": null, 
            "recommendedSecurityUpdateId": null, 
            "recommendedSecurityUpdateUrl": null, 
            "diskPaths": [], 
            "registryPaths": [ 
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\ProjectProRetail - en-us" 
            ], 
            "lastSeenTimestamp": "2021-01-03 23:38:03", 
            "firstSeenTimestamp": "2019-08-01 22:56:12", 
            "exploitabilityLevel": "NoExploit", 
            "recommendationReference": "va-_-microsoft-_-project", 
            "status": "Fixed", 
            "eventTimestamp": "2021-01-11T11:06:08.291Z" 
        }, 
        { 
            "id": "038df381234510b357ac19d0113ef622e4e212b3_chrome_81.0.4044.138_CVE-2020-16011_", 
            "deviceId": "038df381234510d357ac19b0113ef922e4e212b3",  
            "rbacGroupName": "hhh", 
            "deviceName": "ComputerPII_365f5c0bb7202c163937dad3d017969b2d760eb4.DomainPII_29596a43a2ef2bbfa00f6a16c0cb1d108bc63e32.DomainPII_3c5fefd2e6fda2f36257359404f6c1092aa6d4b8.net", 
            "osPlatform": "Windows10", 
            "osVersion": "10.0.18363.1256", 
            "osArchitecture": "x64", 
            "softwareVendor": "google", 
            "softwareName": "chrome", 
            "softwareVersion": "81.0.4044.138", 
            "cveId": "CVE-2020-16011", 
            "vulnerabilitySeverityLevel": "High", 
            "recommendedSecurityUpdate": "ADV 200002", 
            "recommendedSecurityUpdateId": null, 
            "recommendedSecurityUpdateUrl": null, 
            "diskPaths": [ 
                "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe" 
            ], 
            "registryPaths": [ 
                "HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Uninstall\\{C4EBFDFD-0C55-3E5F-A919-E3C54949024A}" 
            ], 
            "lastSeenTimestamp": "2020-12-10 22:45:41", 
            "firstSeenTimestamp": "2020-07-26 02:13:43", 
            "exploitabilityLevel": "NoExploit", 
            "recommendationReference": "va-_-google-_-chrome", 
            "status": "Fixed", 
            "eventTimestamp": "2021-01-11T11:06:08.291Z" 
        } 
    ], 
    "@odata.nextLink": "https://wpatdadi-eus-stg.cloudapp.net/api/machines/SoftwareVulnerabilitiesTimeline?sincetime=2021-01-11&pagesize=5&$skiptoken=eyJFeHBvcnREZWZpbml0aW9uIjp7IlRpbWVQYXRoIjoiMjAyMS0wMS0xMS8xMTAxLyJ9LCJFeHBvcnRGaWxlSW5kZXgiOjAsIkxpbmVTdG9wcGVkQXQiOjV9" 
} 
```

## <a name="see-also"></a><span data-ttu-id="f8f90-439">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8f90-439">See also</span></span>

- [<span data-ttu-id="f8f90-440">Exporter les méthodes et propriétés d’évaluation par appareil</span><span class="sxs-lookup"><span data-stu-id="f8f90-440">Export assessment methods and properties per device</span></span>](get-assessment-methods-properties.md)

- [<span data-ttu-id="f8f90-441">Exporter l’évaluation de la configuration sécurisée par appareil</span><span class="sxs-lookup"><span data-stu-id="f8f90-441">Export secure configuration assessment per device</span></span>](get-assessment-secure-config.md)

- [<span data-ttu-id="f8f90-442">Exporter l’évaluation de l’inventaire logiciel par appareil</span><span class="sxs-lookup"><span data-stu-id="f8f90-442">Export software inventory assessment per device</span></span>](get-assessment-software-inventory.md)

<span data-ttu-id="f8f90-443">Autres associés</span><span class="sxs-lookup"><span data-stu-id="f8f90-443">Other related</span></span>

- [<span data-ttu-id="f8f90-444">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="f8f90-444">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="f8f90-445">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="f8f90-445">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
