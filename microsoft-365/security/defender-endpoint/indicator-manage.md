---
title: Gérer les indicateurs
ms.reviewer: ''
description: Gérer les indicateurs pour un hachage de fichier, une adresse IP, des URL ou des domaines qui définissent la détection, la prévention et l’exclusion des entités.
keywords: import, indicator, list, ioc, csv, manage, allowed, blocked, block, clean, malicious, file hash, ip address, urls, domain
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 9fd36f63450335247bf57c4cc1f98d6f0d32a9d5
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185944"
---
# <a name="manage-indicators"></a><span data-ttu-id="28a54-104">Gérer les indicateurs</span><span class="sxs-lookup"><span data-stu-id="28a54-104">Manage indicators</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="28a54-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="28a54-105">**Applies to:**</span></span>
- [<span data-ttu-id="28a54-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="28a54-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="28a54-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="28a54-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="28a54-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="28a54-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="28a54-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="28a54-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)


1. <span data-ttu-id="28a54-110">Dans le volet de navigation, sélectionnez **Indicateurs**  >  **de paramètres.**</span><span class="sxs-lookup"><span data-stu-id="28a54-110">In the navigation pane, select **Settings** > **Indicators**.</span></span>

2. <span data-ttu-id="28a54-111">Sélectionnez l’onglet du type d’entité que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="28a54-111">Select the tab of the entity type you'd like to manage.</span></span>  

3. <span data-ttu-id="28a54-112">Mettez à jour les détails de  l’indicateur et cliquez sur Enregistrer ou cliquer sur le bouton Supprimer si vous souhaitez supprimer l’entité de la liste. </span><span class="sxs-lookup"><span data-stu-id="28a54-112">Update the details of the indicator and click **Save** or click the **Delete** button if you'd like to remove the entity from the list.</span></span>

## <a name="import-a-list-of-iocs"></a><span data-ttu-id="28a54-113">Importer une liste d’IoCs</span><span class="sxs-lookup"><span data-stu-id="28a54-113">Import a list of IoCs</span></span>

<span data-ttu-id="28a54-114">Vous pouvez également choisir de télécharger un fichier CSV qui définit les attributs des indicateurs, l’action à prendre et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="28a54-114">You can also choose to upload a CSV file that defines the attributes of indicators, the action to be taken, and other details.</span></span>

<span data-ttu-id="28a54-115">Téléchargez l’exemple CSV pour connaître les attributs de colonne pris en charge.</span><span class="sxs-lookup"><span data-stu-id="28a54-115">Download the sample CSV to know the supported column attributes.</span></span>

1. <span data-ttu-id="28a54-116">Dans le volet de navigation, sélectionnez **Indicateurs**  >  **de paramètres.**</span><span class="sxs-lookup"><span data-stu-id="28a54-116">In the navigation pane, select **Settings** > **Indicators**.</span></span>

2. <span data-ttu-id="28a54-117">Sélectionnez l’onglet du type d’entité pour qui vous souhaitez importer des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="28a54-117">Select the tab of the entity type you'd like to import indicators for.</span></span>

3. <span data-ttu-id="28a54-118">Sélectionnez **Importer**  >  **un fichier .**</span><span class="sxs-lookup"><span data-stu-id="28a54-118">Select **Import** > **Choose file**.</span></span> 

4. <span data-ttu-id="28a54-119">Sélectionnez **Importer**.</span><span class="sxs-lookup"><span data-stu-id="28a54-119">Select **Import**.</span></span> <span data-ttu-id="28a54-120">Faites-le pour tous les fichiers que vous souhaitez importer.</span><span class="sxs-lookup"><span data-stu-id="28a54-120">Do this for all the files you'd like to import.</span></span> 

5. <span data-ttu-id="28a54-121">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="28a54-121">Select **Done**.</span></span>

<span data-ttu-id="28a54-122">Le tableau suivant indique les paramètres pris en charge.</span><span class="sxs-lookup"><span data-stu-id="28a54-122">The following table shows the supported parameters.</span></span>

<span data-ttu-id="28a54-123">Paramètre</span><span class="sxs-lookup"><span data-stu-id="28a54-123">Parameter</span></span> | <span data-ttu-id="28a54-124">Type</span><span class="sxs-lookup"><span data-stu-id="28a54-124">Type</span></span>    |   <span data-ttu-id="28a54-125">Description</span><span class="sxs-lookup"><span data-stu-id="28a54-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="28a54-126">indicatorType</span><span class="sxs-lookup"><span data-stu-id="28a54-126">indicatorType</span></span> | <span data-ttu-id="28a54-127">Énum</span><span class="sxs-lookup"><span data-stu-id="28a54-127">Enum</span></span> | <span data-ttu-id="28a54-128">Type de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28a54-128">Type of the indicator.</span></span> <span data-ttu-id="28a54-129">Les valeurs possibles sont les suivantes : « FileSha1 », « FileSha256 », « IpAddress », « DomainName » et « Url ».</span><span class="sxs-lookup"><span data-stu-id="28a54-129">Possible values are: "FileSha1", "FileSha256", "IpAddress", "DomainName" and "Url".</span></span> <span data-ttu-id="28a54-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28a54-130">**Required**</span></span>
<span data-ttu-id="28a54-131">indicatorValue</span><span class="sxs-lookup"><span data-stu-id="28a54-131">indicatorValue</span></span> | <span data-ttu-id="28a54-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-132">String</span></span> | <span data-ttu-id="28a54-133">Identité de [l’entité Indicateur.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="28a54-133">Identity of the [Indicator](ti-indicator.md) entity.</span></span> <span data-ttu-id="28a54-134">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28a54-134">**Required**</span></span>
<span data-ttu-id="28a54-135">action</span><span class="sxs-lookup"><span data-stu-id="28a54-135">action</span></span> | <span data-ttu-id="28a54-136">Énum</span><span class="sxs-lookup"><span data-stu-id="28a54-136">Enum</span></span> | <span data-ttu-id="28a54-137">Action qui sera entreprise si l’indicateur est détecté dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="28a54-137">The action that will be taken if the indicator will be discovered in the organization.</span></span> <span data-ttu-id="28a54-138">Les valeurs possibles sont : « Alert », « AlertAndBlock » et « Allowed ».</span><span class="sxs-lookup"><span data-stu-id="28a54-138">Possible values are: "Alert", "AlertAndBlock", and "Allowed".</span></span> <span data-ttu-id="28a54-139">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28a54-139">**Required**</span></span>
<span data-ttu-id="28a54-140">title</span><span class="sxs-lookup"><span data-stu-id="28a54-140">title</span></span> | <span data-ttu-id="28a54-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-141">String</span></span> | <span data-ttu-id="28a54-142">Titre de l’alerte de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28a54-142">Indicator alert title.</span></span> <span data-ttu-id="28a54-143">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28a54-143">**Required**</span></span>
<span data-ttu-id="28a54-144">description</span><span class="sxs-lookup"><span data-stu-id="28a54-144">description</span></span> | <span data-ttu-id="28a54-145">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-145">String</span></span> |  <span data-ttu-id="28a54-146">Description de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28a54-146">Description of the indicator.</span></span> <span data-ttu-id="28a54-147">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28a54-147">**Required**</span></span>
<span data-ttu-id="28a54-148">expirationTime</span><span class="sxs-lookup"><span data-stu-id="28a54-148">expirationTime</span></span> | <span data-ttu-id="28a54-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28a54-149">DateTimeOffset</span></span> | <span data-ttu-id="28a54-150">Heure d’expiration de l’indicateur au format suivant AAA-MM-JDTHH:MM:SS.0Z.</span><span class="sxs-lookup"><span data-stu-id="28a54-150">The expiration time of the indicator in the following format YYYY-MM-DDTHH:MM:SS.0Z.</span></span> <span data-ttu-id="28a54-151">**Optional**</span><span class="sxs-lookup"><span data-stu-id="28a54-151">**Optional**</span></span>
<span data-ttu-id="28a54-152">Sévérité </span><span class="sxs-lookup"><span data-stu-id="28a54-152">severity</span></span> | <span data-ttu-id="28a54-153">Énum</span><span class="sxs-lookup"><span data-stu-id="28a54-153">Enum</span></span> | <span data-ttu-id="28a54-154">Gravité de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28a54-154">The severity of the indicator.</span></span> <span data-ttu-id="28a54-155">Les valeurs possibles sont : « Informational », « Low », « Medium » et « High ».</span><span class="sxs-lookup"><span data-stu-id="28a54-155">Possible values are: "Informational", "Low", "Medium" and "High".</span></span> <span data-ttu-id="28a54-156">**Optional**</span><span class="sxs-lookup"><span data-stu-id="28a54-156">**Optional**</span></span>
<span data-ttu-id="28a54-157">recommendedActions</span><span class="sxs-lookup"><span data-stu-id="28a54-157">recommendedActions</span></span> | <span data-ttu-id="28a54-158">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-158">String</span></span> | <span data-ttu-id="28a54-159">Actions recommandées pour l’alerte d’indicateur TI.</span><span class="sxs-lookup"><span data-stu-id="28a54-159">TI indicator alert recommended actions.</span></span> <span data-ttu-id="28a54-160">**Optional**</span><span class="sxs-lookup"><span data-stu-id="28a54-160">**Optional**</span></span>
<span data-ttu-id="28a54-161">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="28a54-161">rbacGroupNames</span></span> | <span data-ttu-id="28a54-162">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-162">String</span></span> | <span data-ttu-id="28a54-163">Liste séparée par des virgules des noms de groupe RBAC à appliquer à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28a54-163">Comma-separated list of RBAC group names the indicator would be applied to.</span></span> <span data-ttu-id="28a54-164">**Optional**</span><span class="sxs-lookup"><span data-stu-id="28a54-164">**Optional**</span></span>
<span data-ttu-id="28a54-165">category</span><span class="sxs-lookup"><span data-stu-id="28a54-165">category</span></span> | <span data-ttu-id="28a54-166">String</span><span class="sxs-lookup"><span data-stu-id="28a54-166">String</span></span> | <span data-ttu-id="28a54-167">Catégorie de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="28a54-167">Category of the alert.</span></span> <span data-ttu-id="28a54-168">Exemples : exécution et accès aux informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="28a54-168">Examples include: Execution and credential access.</span></span> <span data-ttu-id="28a54-169">**Optional**</span><span class="sxs-lookup"><span data-stu-id="28a54-169">**Optional**</span></span>
<span data-ttu-id="28a54-170">mitretechniques</span><span class="sxs-lookup"><span data-stu-id="28a54-170">mitretechniques</span></span>| <span data-ttu-id="28a54-171">Chaîne</span><span class="sxs-lookup"><span data-stu-id="28a54-171">String</span></span> | <span data-ttu-id="28a54-172">MITRE techniques code/id (séparés par des virgules).</span><span class="sxs-lookup"><span data-stu-id="28a54-172">MITRE techniques code/id (comma separated).</span></span> <span data-ttu-id="28a54-173">Pour plus d’informations, [voir tactiques d’entreprise.](https://attack.mitre.org/tactics/enterprise/)</span><span class="sxs-lookup"><span data-stu-id="28a54-173">For more information, see [Enterprise tactics](https://attack.mitre.org/tactics/enterprise/).</span></span> <span data-ttu-id="28a54-174">**Facultatif** Il est recommandé d’ajouter une valeur dans la catégorie lorsqu’une technique MITRE.</span><span class="sxs-lookup"><span data-stu-id="28a54-174">**Optional** It is recommended to add a value in category when a MITRE technique.</span></span>

<span data-ttu-id="28a54-175">Pour plus d’informations, consultez Microsoft Defender pour les catégories d’alerte de point de terminaison sont désormais alignées avec [MITRE ATT&CK!](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/microsoft-defender-atp-alert-categories-are-now-aligned-with/ba-p/732748).</span><span class="sxs-lookup"><span data-stu-id="28a54-175">For more information, see [Microsoft Defender for Endpoint alert categories are now aligned with MITRE ATT&CK!](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/microsoft-defender-atp-alert-categories-are-now-aligned-with/ba-p/732748).</span></span>


## <a name="see-also"></a><span data-ttu-id="28a54-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28a54-176">See also</span></span>
- [<span data-ttu-id="28a54-177">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="28a54-177">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="28a54-178">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="28a54-178">Create indicators for files</span></span>](indicator-file.md)
- [<span data-ttu-id="28a54-179">Créer des indicateurs pour les adresses IP et les URL/domaines</span><span class="sxs-lookup"><span data-stu-id="28a54-179">Create indicators for IPs and URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="28a54-180">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="28a54-180">Create indicators based on certificates</span></span>](indicator-certificates.md)
