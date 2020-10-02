---
title: Migrer les requêtes de chasse avancées à partir de Microsoft Defender ATP
description: Découvrez comment ajuster vos requêtes ATP Microsoft Defender afin de pouvoir les utiliser dans Microsoft Threat Protection
keywords: chasse aux menaces, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, Microsoft Defender ATP, mdatp, recherche, requête, télémétrie, détections personnalisées, schéma, Kusto, Microsoft 365, mappage
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: daa89ebf39f8fc6d2110720f61b8d02c074fb484
ms.sourcegitcommit: 0f48beaca3afa4df12d41847014975d50a4ebe7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "48338705"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-atp"></a><span data-ttu-id="9a1e8-104">Migrer les requêtes de chasse avancées à partir de Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="9a1e8-104">Migrate advanced hunting queries from Microsoft Defender ATP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="9a1e8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9a1e8-105">**Applies to:**</span></span>
- <span data-ttu-id="9a1e8-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9a1e8-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="9a1e8-107">Déplacez vos flux de travail de chasse avancés de Microsoft Defender ATP vers la recherche proactive de menaces à l’aide d’un ensemble plus large de données.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-107">Move your advanced hunting workflows from Microsoft Defender ATP to proactively hunt for threats using a broader set of data.</span></span> <span data-ttu-id="9a1e8-108">Dans Microsoft Threat Protection, vous pouvez accéder aux données à partir d’autres solutions de sécurité Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="9a1e8-108">In Microsoft Threat Protection, you get access to data from other Microsoft 365 security solutions, including:</span></span>

- <span data-ttu-id="9a1e8-109">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9a1e8-109">Microsoft Defender Advanced Threat Protection</span></span>
- <span data-ttu-id="9a1e8-110">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9a1e8-110">Office 365 Advanced Threat Protection</span></span>
- <span data-ttu-id="9a1e8-111">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9a1e8-111">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="9a1e8-112">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9a1e8-112">Azure Advanced Threat Protection</span></span>

>[!NOTE]
><span data-ttu-id="9a1e8-113">La plupart des clients Microsoft Defender ATP peuvent [utiliser la protection contre les menaces Microsoft sans licence supplémentaire](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="9a1e8-113">Most Microsoft Defender ATP customers can [use Microsoft Threat Protection without additional licenses](prerequisites.md#licensing-requirements).</span></span> <span data-ttu-id="9a1e8-114">Pour commencer la transition de vos flux de travail de chasse avancés à partir de Microsoft Defender ATP, [activez Microsoft Threat Protection](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="9a1e8-114">To start transitioning your advanced hunting workflows from Microsoft Defender ATP, [turn on Microsoft Threat Protection](mtp-enable.md).</span></span>

<span data-ttu-id="9a1e8-115">Vous pouvez procéder à une transition sans affecter vos flux de travail Microsoft Defender ATP existants.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-115">You can transition without affecting your existing Microsoft Defender ATP workflows.</span></span> <span data-ttu-id="9a1e8-116">Les requêtes enregistrées restent intactes et les règles de détection personnalisées continuent à s’exécuter et génèrent des alertes.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-116">Saved queries remain intact, and custom detection rules continue to run and generate alerts.</span></span> <span data-ttu-id="9a1e8-117">Elles seront toutefois visibles dans la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-117">They will, however, be visible in Microsoft Threat Protection.</span></span> 

## <a name="schema-tables-in-microsoft-threat-protection-only"></a><span data-ttu-id="9a1e8-118">Tables de schéma dans la protection Microsoft contre les menaces uniquement</span><span class="sxs-lookup"><span data-stu-id="9a1e8-118">Schema tables in Microsoft Threat Protection only</span></span>
<span data-ttu-id="9a1e8-119">Le [schéma de la chasse avancée à la protection de Microsoft contre les menaces](advanced-hunting-schema-tables.md) fournit des tables supplémentaires contenant des données provenant de différentes solutions de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-119">The [Microsoft Threat Protection advanced hunting schema](advanced-hunting-schema-tables.md) provides additional tables containing data from various Microsoft 365 security solutions.</span></span> <span data-ttu-id="9a1e8-120">Les tableaux suivants sont disponibles uniquement dans la protection contre les menaces Microsoft :</span><span class="sxs-lookup"><span data-stu-id="9a1e8-120">The following tables are available only in Microsoft Threat Protection:</span></span>

| <span data-ttu-id="9a1e8-121">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="9a1e8-121">Table name</span></span> | <span data-ttu-id="9a1e8-122">Description</span><span class="sxs-lookup"><span data-stu-id="9a1e8-122">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="9a1e8-123">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="9a1e8-123">AlertEvidence</span></span>](advanced-hunting-alertevidence-table.md) | <span data-ttu-id="9a1e8-124">Fichiers, adresses IP, URL, utilisateurs ou périphériques associés à des alertes</span><span class="sxs-lookup"><span data-stu-id="9a1e8-124">Files, IP addresses, URLs, users, or devices associated with alerts</span></span> |
| [<span data-ttu-id="9a1e8-125">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="9a1e8-125">AlertInfo</span></span>](advanced-hunting-alertinfo-table.md) | <span data-ttu-id="9a1e8-126">Alertes de Microsoft Defender ATP, Office 365 ATP, sécurité de l’application Cloud Microsoft et Azure ATP, y compris les informations de gravité et les catégories de menaces</span><span class="sxs-lookup"><span data-stu-id="9a1e8-126">Alerts from Microsoft Defender ATP, Office 365 ATP, Microsoft Cloud App Security, and Azure ATP, including severity information and threat categories</span></span>  |
| [<span data-ttu-id="9a1e8-127">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-127">AppFileEvents</span></span>](advanced-hunting-appfileevents-table.md) | <span data-ttu-id="9a1e8-128">Activités liées aux fichiers dans les applications et les services Cloud</span><span class="sxs-lookup"><span data-stu-id="9a1e8-128">File-related activities in cloud apps and services</span></span> |
| [<span data-ttu-id="9a1e8-129">EmailAttachmentInfo</span><span class="sxs-lookup"><span data-stu-id="9a1e8-129">EmailAttachmentInfo</span></span>](advanced-hunting-emailattachmentinfo-table.md) | <span data-ttu-id="9a1e8-130">Informations sur les fichiers joints aux courriers électroniques</span><span class="sxs-lookup"><span data-stu-id="9a1e8-130">Information about files attached to emails</span></span> |
| [<span data-ttu-id="9a1e8-131">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-131">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="9a1e8-132">Événements de messagerie Microsoft 365, y compris les événements de remise et de blocage du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="9a1e8-132">Microsoft 365 email events, including email delivery and blocking events</span></span> |
| [<span data-ttu-id="9a1e8-133">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-133">EmailPostDeliveryEvents</span></span>](advanced-hunting-emailpostdeliveryevents-table.md) | <span data-ttu-id="9a1e8-134">Événements de sécurité qui se produisent après la livraison, après que Microsoft 365 a remis les courriers électroniques à la boîte aux lettres du destinataire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-134">Security events that occur post-delivery, after Microsoft 365 has delivered the emails to the recipient mailbox</span></span> |
| [<span data-ttu-id="9a1e8-135">EmailUrlInfo</span><span class="sxs-lookup"><span data-stu-id="9a1e8-135">EmailUrlInfo</span></span>](advanced-hunting-emailurlinfo-table.md) | <span data-ttu-id="9a1e8-136">Informations sur les URL des courriers électroniques</span><span class="sxs-lookup"><span data-stu-id="9a1e8-136">Information about URLs on emails</span></span> |
| [<span data-ttu-id="9a1e8-137">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-137">IdentityDirectoryEvents</span></span>](advanced-hunting-identitydirectoryevents-table.md) | <span data-ttu-id="9a1e8-138">Événements impliquant un contrôleur de domaine sur site exécutant Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="9a1e8-138">Events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="9a1e8-139">Ce tableau couvre une série d’événements liés à l’identité et de système sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-139">This table covers a range of identity-related events and system events on the domain controller.</span></span> |
| [<span data-ttu-id="9a1e8-140">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="9a1e8-140">IdentityInfo</span></span>](advanced-hunting-identityinfo-table.md) | <span data-ttu-id="9a1e8-141">Informations de compte provenant de différentes sources, notamment Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9a1e8-141">Account information from various sources, including Azure Active Directory</span></span> |
| [<span data-ttu-id="9a1e8-142">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-142">IdentityLogonEvents</span></span>](advanced-hunting-identitylogonevents-table.md) | <span data-ttu-id="9a1e8-143">Événements d’authentification sur Active Directory et Microsoft Online Services</span><span class="sxs-lookup"><span data-stu-id="9a1e8-143">Authentication events on Active Directory and Microsoft online services</span></span> |
| [<span data-ttu-id="9a1e8-144">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-144">IdentityQueryEvents</span></span>](advanced-hunting-identityqueryevents-table.md) | <span data-ttu-id="9a1e8-145">Requêtes pour les objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines</span><span class="sxs-lookup"><span data-stu-id="9a1e8-145">Queries for Active Directory objects, such as users, groups, devices, and domains</span></span> |

## <a name="map-devicealertevents-table"></a><span data-ttu-id="9a1e8-146">Mapper la table DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-146">Map DeviceAlertEvents table</span></span>
<span data-ttu-id="9a1e8-147">Les `AlertInfo` `AlertEvidence` tables et remplacent la `DeviceAlertEvents` table dans le schéma ATP de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-147">The `AlertInfo` and `AlertEvidence` tables replace the `DeviceAlertEvents` table in the Microsoft Defender ATP schema.</span></span> <span data-ttu-id="9a1e8-148">En plus des données relatives aux alertes de périphérique, ces deux tables incluent des données sur les alertes pour les identités, les applications et les courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-148">In addition to data about device alerts, these two tables include data about alerts for identities, apps, and emails.</span></span>

<span data-ttu-id="9a1e8-149">Utilisez le tableau suivant pour vérifier la `DeviceAlertEvents` correspondance des colonnes et des colonnes dans les `AlertInfo` `AlertEvidence` tableaux et.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-149">Use the following table to check how `DeviceAlertEvents` columns map to columns in the `AlertInfo` and `AlertEvidence` tables.</span></span>

>[!TIP]
><span data-ttu-id="9a1e8-150">Outre les colonnes du tableau suivant, le `AlertEvidence` tableau inclut de nombreuses autres colonnes qui fournissent une image plus holistique des alertes provenant de différentes sources.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-150">In addition to the columns the following table, the `AlertEvidence` table includes many other columns that provide a more holistic picture of alerts from various sources.</span></span> [<span data-ttu-id="9a1e8-151">Afficher toutes les colonnes AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="9a1e8-151">See all AlertEvidence columns</span></span>](advanced-hunting-alertevidence-table.md) 

| <span data-ttu-id="9a1e8-152">Colonne DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="9a1e8-152">DeviceAlertEvents column</span></span> | <span data-ttu-id="9a1e8-153">Où trouver les mêmes données dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9a1e8-153">Where to find the same data in Microsoft Threat Protection</span></span> |
|-------------|-----------|-------------|-------------|
| `AlertId` | <span data-ttu-id="9a1e8-154">`AlertInfo` et des  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="9a1e8-154">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `Timestamp` | <span data-ttu-id="9a1e8-155">`AlertInfo` et des  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="9a1e8-155">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `DeviceId` | <span data-ttu-id="9a1e8-156">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-156">`AlertEvidence` table</span></span> |
| `DeviceName` | <span data-ttu-id="9a1e8-157">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-157">`AlertEvidence` table</span></span> |
| `Severity` | <span data-ttu-id="9a1e8-158">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-158">`AlertInfo` table</span></span> |
| `Category` | <span data-ttu-id="9a1e8-159">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-159">`AlertInfo` table</span></span> |
| `Title` | <span data-ttu-id="9a1e8-160">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-160">`AlertInfo` table</span></span> |
| `FileName` | <span data-ttu-id="9a1e8-161">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-161">`AlertEvidence` table</span></span> |
| `SHA1` | <span data-ttu-id="9a1e8-162">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-162">`AlertEvidence` table</span></span> |
| `RemoteUrl` | <span data-ttu-id="9a1e8-163">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-163">`AlertEvidence` table</span></span> |
| `RemoteIP` | <span data-ttu-id="9a1e8-164">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-164">`AlertEvidence` table</span></span> |
| `AttackTechniques` | <span data-ttu-id="9a1e8-165">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="9a1e8-165">`AlertInfo` table</span></span> |
| `ReportId` | <span data-ttu-id="9a1e8-166">Cette colonne est généralement utilisée dans Microsoft Defender ATP pour localiser des enregistrements connexes dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-166">This column is typically used in Microsoft Defender ATP to locate related records in other tables.</span></span> <span data-ttu-id="9a1e8-167">Dans Microsoft Threat Protection, vous pouvez obtenir des données connexes directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-167">In Microsoft Threat Protection, you can get related data directly from the `AlertEvidence` table.</span></span> |
| `Table` | <span data-ttu-id="9a1e8-168">Cette colonne est généralement utilisée dans Microsoft Defender ATP pour obtenir des informations supplémentaires sur les événements dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-168">This column is typically used in Microsoft Defender ATP for additional event information in other tables.</span></span> <span data-ttu-id="9a1e8-169">Dans Microsoft Threat Protection, vous pouvez obtenir des données connexes directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-169">In Microsoft Threat Protection, you can get related data directly from the `AlertEvidence` table.</span></span> |

## <a name="adjust-existing-microsoft-defender-atp-queries"></a><span data-ttu-id="9a1e8-170">Ajuster les requêtes Microsoft Defender ATP existantes</span><span class="sxs-lookup"><span data-stu-id="9a1e8-170">Adjust existing Microsoft Defender ATP queries</span></span>
<span data-ttu-id="9a1e8-171">Les requêtes Microsoft Defender ATP fonctionnent telles quelles, sauf si elles font référence à la `DeviceAlertEvents` table.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-171">Microsoft Defender ATP queries will work as-is unless they reference the `DeviceAlertEvents` table.</span></span> <span data-ttu-id="9a1e8-172">Pour utiliser ces requêtes dans Microsoft Threat Protection, appliquez les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a1e8-172">To use these queries in Microsoft Threat Protection, apply these changes:</span></span>

- <span data-ttu-id="9a1e8-173">Remplacez `DeviceAlertEvents` par `AlertInfo` .</span><span class="sxs-lookup"><span data-stu-id="9a1e8-173">Replace `DeviceAlertEvents` with `AlertInfo`.</span></span>
- <span data-ttu-id="9a1e8-174">Rejoignez les `AlertInfo` `AlertEvidence` tables et `AlertId` pour obtenir des données équivalentes.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-174">Join the `AlertInfo` and the `AlertEvidence` tables on `AlertId` to get equivalent data.</span></span>

### <a name="original-query"></a><span data-ttu-id="9a1e8-175">Requête d’origine</span><span class="sxs-lookup"><span data-stu-id="9a1e8-175">Original query</span></span>
<span data-ttu-id="9a1e8-176">La requête suivante utilise `DeviceAlertEvents` Microsoft Defender ATP pour obtenir les alertes qui impliquent des _powershell.exe_:</span><span class="sxs-lookup"><span data-stu-id="9a1e8-176">The following query uses `DeviceAlertEvents` in Microsoft Defender ATP to get the alerts that involve _powershell.exe_:</span></span>

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a><span data-ttu-id="9a1e8-177">Requête modifiée</span><span class="sxs-lookup"><span data-stu-id="9a1e8-177">Modified query</span></span>
<span data-ttu-id="9a1e8-178">La requête suivante a été ajustée pour une utilisation dans Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-178">The following query has been adjusted for use in Microsoft Threat Protection.</span></span> <span data-ttu-id="9a1e8-179">Au lieu de vérifier le nom de fichier directement à partir de `DeviceAlertEvents` , il rejoint `AlertEvidence` et recherche le nom de fichier dans cette table.</span><span class="sxs-lookup"><span data-stu-id="9a1e8-179">Instead of checking the file name directly from `DeviceAlertEvents`, it joins `AlertEvidence` and checks for the file name in that table.</span></span>

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```

## <a name="related-topics"></a><span data-ttu-id="9a1e8-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a1e8-180">Related topics</span></span>
- [<span data-ttu-id="9a1e8-181">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9a1e8-181">Turn on Microsoft Threat Protection</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="9a1e8-182">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="9a1e8-182">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="9a1e8-183">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="9a1e8-183">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="9a1e8-184">Chasse avancée dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="9a1e8-184">Advanced hunting in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)