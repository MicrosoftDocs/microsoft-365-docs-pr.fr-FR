---
title: Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison
description: Découvrez comment ajuster vos requêtes Microsoft Defender for Endpoint afin de pouvoir les utiliser dans Microsoft 365 Defender
keywords: repérage avancé, repérage de menace, repérage de cybermenace, protection microsoft contre les menaces, microsoft 365, mtp, m365, microsoft defender atp, mdatp, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, microsoft 365, mappage
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.custom: seo-marvel-apr2020
ms.technology: m365d
ms.openlocfilehash: 521b5fc2a8efee83b6a2931e7dbc1c713bd63cd2
ms.sourcegitcommit: c0cfb9b354db56fdd329aec2a89a9b2cf160c4b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "50094806"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-for-endpoint"></a><span data-ttu-id="7db54-104">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7db54-104">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="7db54-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7db54-105">**Applies to:**</span></span>
- <span data-ttu-id="7db54-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7db54-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="7db54-107">Déplacez vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison pour qu’ils recherchent de manière proactive les menaces à l’aide d’un ensemble plus large de données.</span><span class="sxs-lookup"><span data-stu-id="7db54-107">Move your advanced hunting workflows from Microsoft Defender for Endpoint to proactively hunt for threats using a broader set of data.</span></span> <span data-ttu-id="7db54-108">Dans Microsoft 365 Defender, vous avez accès aux données à partir d’autres solutions de sécurité Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="7db54-108">In Microsoft 365 Defender, you get access to data from other Microsoft 365 security solutions, including:</span></span>

- <span data-ttu-id="7db54-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7db54-109">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="7db54-110">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7db54-110">Microsoft Defender for Office 365</span></span>
- <span data-ttu-id="7db54-111">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="7db54-111">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="7db54-112">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="7db54-112">Microsoft Defender for Identity</span></span>

>[!NOTE]
><span data-ttu-id="7db54-113">La plupart des clients Microsoft Defender pour Endpoint peuvent [utiliser Microsoft 365 Defender sans licences supplémentaires.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="7db54-113">Most Microsoft Defender for Endpoint customers can [use Microsoft 365 Defender without additional licenses](prerequisites.md#licensing-requirements).</span></span> <span data-ttu-id="7db54-114">Pour commencer la transition de vos flux de travail de recherche avancée à partir de Defender for Endpoint, [activer Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="7db54-114">To start transitioning your advanced hunting workflows from Defender for Endpoint, [turn on Microsoft 365 Defender](mtp-enable.md).</span></span>

<span data-ttu-id="7db54-115">Vous pouvez faire la transition sans affecter vos flux de travail Defender for Endpoint existants.</span><span class="sxs-lookup"><span data-stu-id="7db54-115">You can transition without affecting your existing Defender for Endpoint workflows.</span></span> <span data-ttu-id="7db54-116">Les requêtes enregistrées restent intactes et les règles de détection personnalisées continuent à s’exécuter et à générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="7db54-116">Saved queries remain intact, and custom detection rules continue to run and generate alerts.</span></span> <span data-ttu-id="7db54-117">Toutefois, elles seront visibles dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="7db54-117">They will, however, be visible in Microsoft 365 Defender.</span></span> 

## <a name="schema-tables-in-microsoft-365-defender-only"></a><span data-ttu-id="7db54-118">Tableaux de schéma dans Microsoft 365 Defender uniquement</span><span class="sxs-lookup"><span data-stu-id="7db54-118">Schema tables in Microsoft 365 Defender only</span></span>
<span data-ttu-id="7db54-119">Le [schéma de recherche avancée Microsoft 365 Defender](advanced-hunting-schema-tables.md) fournit des tableaux supplémentaires contenant des données provenant de différentes solutions de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7db54-119">The [Microsoft 365 Defender advanced hunting schema](advanced-hunting-schema-tables.md) provides additional tables containing data from various Microsoft 365 security solutions.</span></span> <span data-ttu-id="7db54-120">Les tableaux suivants sont disponibles uniquement dans Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="7db54-120">The following tables are available only in Microsoft 365 Defender:</span></span>

| <span data-ttu-id="7db54-121">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="7db54-121">Table name</span></span> | <span data-ttu-id="7db54-122">Description</span><span class="sxs-lookup"><span data-stu-id="7db54-122">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="7db54-123">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="7db54-123">AlertEvidence</span></span>](advanced-hunting-alertevidence-table.md) | <span data-ttu-id="7db54-124">Fichiers, adresses IP, URL, utilisateurs ou appareils associés à des alertes</span><span class="sxs-lookup"><span data-stu-id="7db54-124">Files, IP addresses, URLs, users, or devices associated with alerts</span></span> |
| [<span data-ttu-id="7db54-125">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="7db54-125">AlertInfo</span></span>](advanced-hunting-alertinfo-table.md) | <span data-ttu-id="7db54-126">Alertes de Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité, y compris les informations de gravité et les catégories de menace</span><span class="sxs-lookup"><span data-stu-id="7db54-126">Alerts from Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity, including severity information and threat categories</span></span>  |
| [<span data-ttu-id="7db54-127">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-127">AppFileEvents</span></span>](advanced-hunting-appfileevents-table.md) | <span data-ttu-id="7db54-128">Activités liées aux fichiers dans les applications et services cloud</span><span class="sxs-lookup"><span data-stu-id="7db54-128">File-related activities in cloud apps and services</span></span> |
| [<span data-ttu-id="7db54-129">EmailAttachmentInfo</span><span class="sxs-lookup"><span data-stu-id="7db54-129">EmailAttachmentInfo</span></span>](advanced-hunting-emailattachmentinfo-table.md) | <span data-ttu-id="7db54-130">Informations sur les fichiers joints aux e-mails</span><span class="sxs-lookup"><span data-stu-id="7db54-130">Information about files attached to emails</span></span> |
| [<span data-ttu-id="7db54-131">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-131">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="7db54-132">Événements de messagerie Microsoft 365, y compris la remise et le blocage des messages électroniques</span><span class="sxs-lookup"><span data-stu-id="7db54-132">Microsoft 365 email events, including email delivery and blocking events</span></span> |
| [<span data-ttu-id="7db54-133">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-133">EmailPostDeliveryEvents</span></span>](advanced-hunting-emailpostdeliveryevents-table.md) | <span data-ttu-id="7db54-134">Événements de sécurité qui se produisent après la remise, une fois que Microsoft 365 a remis les messages électroniques à la boîte aux lettres du destinataire</span><span class="sxs-lookup"><span data-stu-id="7db54-134">Security events that occur post-delivery, after Microsoft 365 has delivered the emails to the recipient mailbox</span></span> |
| [<span data-ttu-id="7db54-135">EmailUrlInfo</span><span class="sxs-lookup"><span data-stu-id="7db54-135">EmailUrlInfo</span></span>](advanced-hunting-emailurlinfo-table.md) | <span data-ttu-id="7db54-136">Informations sur les URL des e-mails</span><span class="sxs-lookup"><span data-stu-id="7db54-136">Information about URLs on emails</span></span> |
| [<span data-ttu-id="7db54-137">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-137">IdentityDirectoryEvents</span></span>](advanced-hunting-identitydirectoryevents-table.md) | <span data-ttu-id="7db54-138">Événements impliquant un contrôleur de domaine local exécutant Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="7db54-138">Events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="7db54-139">Ce tableau couvre une plage d’événements liés à l’identité et d’événements système sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="7db54-139">This table covers a range of identity-related events and system events on the domain controller.</span></span> |
| [<span data-ttu-id="7db54-140">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="7db54-140">IdentityInfo</span></span>](advanced-hunting-identityinfo-table.md) | <span data-ttu-id="7db54-141">Informations de compte provenant de différentes sources, notamment Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7db54-141">Account information from various sources, including Azure Active Directory</span></span> |
| [<span data-ttu-id="7db54-142">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-142">IdentityLogonEvents</span></span>](advanced-hunting-identitylogonevents-table.md) | <span data-ttu-id="7db54-143">Événements d’authentification sur Active Directory et les services en ligne Microsoft</span><span class="sxs-lookup"><span data-stu-id="7db54-143">Authentication events on Active Directory and Microsoft online services</span></span> |
| [<span data-ttu-id="7db54-144">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-144">IdentityQueryEvents</span></span>](advanced-hunting-identityqueryevents-table.md) | <span data-ttu-id="7db54-145">Requêtes pour les objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines</span><span class="sxs-lookup"><span data-stu-id="7db54-145">Queries for Active Directory objects, such as users, groups, devices, and domains</span></span> |

## <a name="map-devicealertevents-table"></a><span data-ttu-id="7db54-146">Table Map DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-146">Map DeviceAlertEvents table</span></span>
<span data-ttu-id="7db54-147">Les `AlertInfo` `AlertEvidence` tableaux et les tables `DeviceAlertEvents` remplacent le tableau dans le schéma Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="7db54-147">The `AlertInfo` and `AlertEvidence` tables replace the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="7db54-148">En plus des données sur les alertes d’appareil, ces deux tableaux incluent des données sur les alertes pour les identités, les applications et les e-mails.</span><span class="sxs-lookup"><span data-stu-id="7db54-148">In addition to data about device alerts, these two tables include data about alerts for identities, apps, and emails.</span></span>

<span data-ttu-id="7db54-149">Utilisez le tableau suivant pour vérifier la façon dont les `DeviceAlertEvents` colonnes sont m mapées aux colonnes dans `AlertInfo` les tableaux et les `AlertEvidence` colonnes.</span><span class="sxs-lookup"><span data-stu-id="7db54-149">Use the following table to check how `DeviceAlertEvents` columns map to columns in the `AlertInfo` and `AlertEvidence` tables.</span></span>

>[!TIP]
><span data-ttu-id="7db54-150">Outre les colonnes du tableau suivant, le tableau inclut de nombreuses autres colonnes qui fournissent une image plus globale des alertes provenant de `AlertEvidence` différentes sources.</span><span class="sxs-lookup"><span data-stu-id="7db54-150">In addition to the columns the following table, the `AlertEvidence` table includes many other columns that provide a more holistic picture of alerts from various sources.</span></span> [<span data-ttu-id="7db54-151">Voir toutes les colonnes AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="7db54-151">See all AlertEvidence columns</span></span>](advanced-hunting-alertevidence-table.md) 

| <span data-ttu-id="7db54-152">Colonne DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="7db54-152">DeviceAlertEvents column</span></span> | <span data-ttu-id="7db54-153">Où trouver les mêmes données dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7db54-153">Where to find the same data in Microsoft 365 Defender</span></span> |
|-------------|-----------|-------------|-------------|
| `AlertId` | <span data-ttu-id="7db54-154">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="7db54-154">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `Timestamp` | <span data-ttu-id="7db54-155">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="7db54-155">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `DeviceId` | <span data-ttu-id="7db54-156">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-156">`AlertEvidence` table</span></span> |
| `DeviceName` | <span data-ttu-id="7db54-157">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-157">`AlertEvidence` table</span></span> |
| `Severity` | <span data-ttu-id="7db54-158">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="7db54-158">`AlertInfo` table</span></span> |
| `Category` | <span data-ttu-id="7db54-159">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="7db54-159">`AlertInfo` table</span></span> |
| `Title` | <span data-ttu-id="7db54-160">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="7db54-160">`AlertInfo` table</span></span> |
| `FileName` | <span data-ttu-id="7db54-161">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-161">`AlertEvidence` table</span></span> |
| `SHA1` | <span data-ttu-id="7db54-162">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-162">`AlertEvidence` table</span></span> |
| `RemoteUrl` | <span data-ttu-id="7db54-163">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-163">`AlertEvidence` table</span></span> |
| `RemoteIP` | <span data-ttu-id="7db54-164">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="7db54-164">`AlertEvidence` table</span></span> |
| `AttackTechniques` | <span data-ttu-id="7db54-165">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="7db54-165">`AlertInfo` table</span></span> |
| `ReportId` | <span data-ttu-id="7db54-166">Cette colonne est généralement utilisée dans Microsoft Defender pour point de terminaison pour rechercher des enregistrements connexes dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="7db54-166">This column is typically used in Microsoft Defender for Endpoint to locate related records in other tables.</span></span> <span data-ttu-id="7db54-167">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="7db54-167">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |
| `Table` | <span data-ttu-id="7db54-168">Cette colonne est généralement utilisée dans Microsoft Defender pour le point de terminaison pour des informations supplémentaires sur les événements dans d’autres tableaux.</span><span class="sxs-lookup"><span data-stu-id="7db54-168">This column is typically used in Microsoft Defender for Endpoint for additional event information in other tables.</span></span> <span data-ttu-id="7db54-169">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="7db54-169">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |

## <a name="adjust-existing-microsoft-defender-for-endpoint-queries"></a><span data-ttu-id="7db54-170">Ajuster les requêtes Microsoft Defender pour les points de terminaison existantes</span><span class="sxs-lookup"><span data-stu-id="7db54-170">Adjust existing Microsoft Defender for Endpoint queries</span></span>
<span data-ttu-id="7db54-171">Les requêtes Microsoft Defender pour les points de terminaison fonctionneront telles qu’elles sont sauf si elles font référence au `DeviceAlertEvents` tableau.</span><span class="sxs-lookup"><span data-stu-id="7db54-171">Microsoft Defender for Endpoint queries will work as-is unless they reference the `DeviceAlertEvents` table.</span></span> <span data-ttu-id="7db54-172">Pour utiliser ces requêtes dans Microsoft 365 Defender, appliquez les modifications ci-après :</span><span class="sxs-lookup"><span data-stu-id="7db54-172">To use these queries in Microsoft 365 Defender, apply these changes:</span></span>

- <span data-ttu-id="7db54-173">Remplacez `DeviceAlertEvents` par `AlertInfo` .</span><span class="sxs-lookup"><span data-stu-id="7db54-173">Replace `DeviceAlertEvents` with `AlertInfo`.</span></span>
- <span data-ttu-id="7db54-174">Joignez les `AlertInfo` tables et les tables pour obtenir des données `AlertEvidence` `AlertId` équivalentes.</span><span class="sxs-lookup"><span data-stu-id="7db54-174">Join the `AlertInfo` and the `AlertEvidence` tables on `AlertId` to get equivalent data.</span></span>

### <a name="original-query"></a><span data-ttu-id="7db54-175">Requête d’origine</span><span class="sxs-lookup"><span data-stu-id="7db54-175">Original query</span></span>
<span data-ttu-id="7db54-176">La requête suivante utilise Microsoft Defender for Endpoint pour obtenir les alertes qui `DeviceAlertEvents` impliquent _powershell.exe_:</span><span class="sxs-lookup"><span data-stu-id="7db54-176">The following query uses `DeviceAlertEvents` in Microsoft Defender for Endpoint to get the alerts that involve _powershell.exe_:</span></span>

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a><span data-ttu-id="7db54-177">Requête modifiée</span><span class="sxs-lookup"><span data-stu-id="7db54-177">Modified query</span></span>
<span data-ttu-id="7db54-178">La requête suivante a été ajustée pour être utilisé dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="7db54-178">The following query has been adjusted for use in Microsoft 365 Defender.</span></span> <span data-ttu-id="7db54-179">Au lieu de vérifier le nom de fichier directement à partir de , il joint et recherche le nom de fichier `DeviceAlertEvents` `AlertEvidence` dans cette table.</span><span class="sxs-lookup"><span data-stu-id="7db54-179">Instead of checking the file name directly from `DeviceAlertEvents`, it joins `AlertEvidence` and checks for the file name in that table.</span></span>

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```



## <a name="see-also"></a><span data-ttu-id="7db54-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7db54-180">See also</span></span>
- [<span data-ttu-id="7db54-181">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7db54-181">Turn on Microsoft 365 Defender</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="7db54-182">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="7db54-182">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="7db54-183">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="7db54-183">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="7db54-184">Recherche avancée dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7db54-184">Advanced hunting in Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)