---
title: Migrer les requêtes de chasse avancées de Microsoft Defender pour le point de terminaison
description: Découvrez comment ajuster vos requêtes Microsoft Defender pour les points de terminaison afin de pouvoir les utiliser dans Microsoft 365 Defender
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8b69dff94cc5d3ba3331fd6d13b1d7de1402ac47
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846855"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-for-endpoint"></a><span data-ttu-id="b49fa-104">Migrer les requêtes de chasse avancées de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49fa-104">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="b49fa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b49fa-105">**Applies to:**</span></span>
- <span data-ttu-id="b49fa-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b49fa-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="b49fa-107">Déplacez vos flux de travail de chasse avancés de Microsoft Defender for Endpoint vers la recherche proactive de menaces à l’aide d’un ensemble plus large de données.</span><span class="sxs-lookup"><span data-stu-id="b49fa-107">Move your advanced hunting workflows from Microsoft Defender for Endpoint to proactively hunt for threats using a broader set of data.</span></span> <span data-ttu-id="b49fa-108">Dans Microsoft 365 Defender, vous pouvez accéder aux données à partir d’autres solutions de sécurité Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="b49fa-108">In Microsoft 365 Defender, you get access to data from other Microsoft 365 security solutions, including:</span></span>

- <span data-ttu-id="b49fa-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49fa-109">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="b49fa-110">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b49fa-110">Microsoft Defender for Office 365</span></span>
- <span data-ttu-id="b49fa-111">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b49fa-111">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="b49fa-112">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="b49fa-112">Microsoft Defender for Identity</span></span>

>[!NOTE]
><span data-ttu-id="b49fa-113">La plupart des clients Microsoft Defender pour les points de terminaison peuvent [utiliser microsoft 365 Defender sans licence supplémentaire](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="b49fa-113">Most Microsoft Defender for Endpoint customers can [use Microsoft 365 Defender without additional licenses](prerequisites.md#licensing-requirements).</span></span> <span data-ttu-id="b49fa-114">Pour commencer la transition de vos flux de travail de chasse avancés de Defender pour le point de terminaison, [activez Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="b49fa-114">To start transitioning your advanced hunting workflows from Defender for Endpoint, [turn on Microsoft 365 Defender](mtp-enable.md).</span></span>

<span data-ttu-id="b49fa-115">Vous pouvez procéder à une transition sans affecter votre Defender existant pour les flux de travail de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b49fa-115">You can transition without affecting your existing Defender for Endpoint workflows.</span></span> <span data-ttu-id="b49fa-116">Les requêtes enregistrées restent intactes et les règles de détection personnalisées continuent à s’exécuter et génèrent des alertes.</span><span class="sxs-lookup"><span data-stu-id="b49fa-116">Saved queries remain intact, and custom detection rules continue to run and generate alerts.</span></span> <span data-ttu-id="b49fa-117">Elles seront toutefois visibles dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b49fa-117">They will, however, be visible in Microsoft 365 Defender.</span></span> 

## <a name="schema-tables-in-microsoft-365-defender-only"></a><span data-ttu-id="b49fa-118">Tables de schéma dans Microsoft 365 Defender uniquement</span><span class="sxs-lookup"><span data-stu-id="b49fa-118">Schema tables in Microsoft 365 Defender only</span></span>
<span data-ttu-id="b49fa-119">Le [schéma de chasse avancé de microsoft 365 Defender](advanced-hunting-schema-tables.md) fournit des tables supplémentaires contenant des données provenant de différentes solutions de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b49fa-119">The [Microsoft 365 Defender advanced hunting schema](advanced-hunting-schema-tables.md) provides additional tables containing data from various Microsoft 365 security solutions.</span></span> <span data-ttu-id="b49fa-120">Les tableaux suivants sont disponibles uniquement dans Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="b49fa-120">The following tables are available only in Microsoft 365 Defender:</span></span>

| <span data-ttu-id="b49fa-121">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="b49fa-121">Table name</span></span> | <span data-ttu-id="b49fa-122">Description</span><span class="sxs-lookup"><span data-stu-id="b49fa-122">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="b49fa-123">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="b49fa-123">AlertEvidence</span></span>](advanced-hunting-alertevidence-table.md) | <span data-ttu-id="b49fa-124">Fichiers, adresses IP, URL, utilisateurs ou périphériques associés à des alertes</span><span class="sxs-lookup"><span data-stu-id="b49fa-124">Files, IP addresses, URLs, users, or devices associated with alerts</span></span> |
| [<span data-ttu-id="b49fa-125">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="b49fa-125">AlertInfo</span></span>](advanced-hunting-alertinfo-table.md) | <span data-ttu-id="b49fa-126">Alertes de Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security et Microsoft Defender for Identity, y compris les informations de gravité et les catégories de menaces</span><span class="sxs-lookup"><span data-stu-id="b49fa-126">Alerts from Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity, including severity information and threat categories</span></span>  |
| [<span data-ttu-id="b49fa-127">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-127">AppFileEvents</span></span>](advanced-hunting-appfileevents-table.md) | <span data-ttu-id="b49fa-128">Activités liées aux fichiers dans les applications et les services Cloud</span><span class="sxs-lookup"><span data-stu-id="b49fa-128">File-related activities in cloud apps and services</span></span> |
| [<span data-ttu-id="b49fa-129">EmailAttachmentInfo</span><span class="sxs-lookup"><span data-stu-id="b49fa-129">EmailAttachmentInfo</span></span>](advanced-hunting-emailattachmentinfo-table.md) | <span data-ttu-id="b49fa-130">Informations sur les fichiers joints aux courriers électroniques</span><span class="sxs-lookup"><span data-stu-id="b49fa-130">Information about files attached to emails</span></span> |
| [<span data-ttu-id="b49fa-131">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-131">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="b49fa-132">Événements de messagerie Microsoft 365, y compris les événements de remise et de blocage du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="b49fa-132">Microsoft 365 email events, including email delivery and blocking events</span></span> |
| [<span data-ttu-id="b49fa-133">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-133">EmailPostDeliveryEvents</span></span>](advanced-hunting-emailpostdeliveryevents-table.md) | <span data-ttu-id="b49fa-134">Événements de sécurité qui se produisent après la livraison, après que Microsoft 365 a remis les courriers électroniques à la boîte aux lettres du destinataire</span><span class="sxs-lookup"><span data-stu-id="b49fa-134">Security events that occur post-delivery, after Microsoft 365 has delivered the emails to the recipient mailbox</span></span> |
| [<span data-ttu-id="b49fa-135">EmailUrlInfo</span><span class="sxs-lookup"><span data-stu-id="b49fa-135">EmailUrlInfo</span></span>](advanced-hunting-emailurlinfo-table.md) | <span data-ttu-id="b49fa-136">Informations sur les URL des courriers électroniques</span><span class="sxs-lookup"><span data-stu-id="b49fa-136">Information about URLs on emails</span></span> |
| [<span data-ttu-id="b49fa-137">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-137">IdentityDirectoryEvents</span></span>](advanced-hunting-identitydirectoryevents-table.md) | <span data-ttu-id="b49fa-138">Événements impliquant un contrôleur de domaine sur site exécutant Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="b49fa-138">Events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="b49fa-139">Ce tableau couvre une série d’événements liés à l’identité et de système sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b49fa-139">This table covers a range of identity-related events and system events on the domain controller.</span></span> |
| [<span data-ttu-id="b49fa-140">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="b49fa-140">IdentityInfo</span></span>](advanced-hunting-identityinfo-table.md) | <span data-ttu-id="b49fa-141">Informations de compte provenant de différentes sources, notamment Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b49fa-141">Account information from various sources, including Azure Active Directory</span></span> |
| [<span data-ttu-id="b49fa-142">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-142">IdentityLogonEvents</span></span>](advanced-hunting-identitylogonevents-table.md) | <span data-ttu-id="b49fa-143">Événements d’authentification sur Active Directory et Microsoft Online Services</span><span class="sxs-lookup"><span data-stu-id="b49fa-143">Authentication events on Active Directory and Microsoft online services</span></span> |
| [<span data-ttu-id="b49fa-144">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-144">IdentityQueryEvents</span></span>](advanced-hunting-identityqueryevents-table.md) | <span data-ttu-id="b49fa-145">Requêtes pour les objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines</span><span class="sxs-lookup"><span data-stu-id="b49fa-145">Queries for Active Directory objects, such as users, groups, devices, and domains</span></span> |

## <a name="map-devicealertevents-table"></a><span data-ttu-id="b49fa-146">Mapper la table DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-146">Map DeviceAlertEvents table</span></span>
<span data-ttu-id="b49fa-147">Les `AlertInfo` `AlertEvidence` tables et remplacent la `DeviceAlertEvents` table dans le schéma Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b49fa-147">The `AlertInfo` and `AlertEvidence` tables replace the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="b49fa-148">En plus des données relatives aux alertes de périphérique, ces deux tables incluent des données sur les alertes pour les identités, les applications et les courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="b49fa-148">In addition to data about device alerts, these two tables include data about alerts for identities, apps, and emails.</span></span>

<span data-ttu-id="b49fa-149">Utilisez le tableau suivant pour vérifier la `DeviceAlertEvents` correspondance des colonnes et des colonnes dans les `AlertInfo` `AlertEvidence` tableaux et.</span><span class="sxs-lookup"><span data-stu-id="b49fa-149">Use the following table to check how `DeviceAlertEvents` columns map to columns in the `AlertInfo` and `AlertEvidence` tables.</span></span>

>[!TIP]
><span data-ttu-id="b49fa-150">Outre les colonnes du tableau suivant, le `AlertEvidence` tableau inclut de nombreuses autres colonnes qui fournissent une image plus holistique des alertes provenant de différentes sources.</span><span class="sxs-lookup"><span data-stu-id="b49fa-150">In addition to the columns the following table, the `AlertEvidence` table includes many other columns that provide a more holistic picture of alerts from various sources.</span></span> [<span data-ttu-id="b49fa-151">Afficher toutes les colonnes AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="b49fa-151">See all AlertEvidence columns</span></span>](advanced-hunting-alertevidence-table.md) 

| <span data-ttu-id="b49fa-152">Colonne DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="b49fa-152">DeviceAlertEvents column</span></span> | <span data-ttu-id="b49fa-153">Où trouver les mêmes données dans Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="b49fa-153">Where to find the same data in Microsoft 365 Defender</span></span> |
|-------------|-----------|-------------|-------------|
| `AlertId` | <span data-ttu-id="b49fa-154">`AlertInfo` et des  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="b49fa-154">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `Timestamp` | <span data-ttu-id="b49fa-155">`AlertInfo` et des  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="b49fa-155">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `DeviceId` | <span data-ttu-id="b49fa-156">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-156">`AlertEvidence` table</span></span> |
| `DeviceName` | <span data-ttu-id="b49fa-157">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-157">`AlertEvidence` table</span></span> |
| `Severity` | <span data-ttu-id="b49fa-158">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-158">`AlertInfo` table</span></span> |
| `Category` | <span data-ttu-id="b49fa-159">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-159">`AlertInfo` table</span></span> |
| `Title` | <span data-ttu-id="b49fa-160">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-160">`AlertInfo` table</span></span> |
| `FileName` | <span data-ttu-id="b49fa-161">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-161">`AlertEvidence` table</span></span> |
| `SHA1` | <span data-ttu-id="b49fa-162">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-162">`AlertEvidence` table</span></span> |
| `RemoteUrl` | <span data-ttu-id="b49fa-163">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-163">`AlertEvidence` table</span></span> |
| `RemoteIP` | <span data-ttu-id="b49fa-164">`AlertEvidence` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-164">`AlertEvidence` table</span></span> |
| `AttackTechniques` | <span data-ttu-id="b49fa-165">`AlertInfo` tabulaire</span><span class="sxs-lookup"><span data-stu-id="b49fa-165">`AlertInfo` table</span></span> |
| `ReportId` | <span data-ttu-id="b49fa-166">Cette colonne est généralement utilisée dans Microsoft Defender pour le point de terminaison pour localiser des enregistrements connexes dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="b49fa-166">This column is typically used in Microsoft Defender for Endpoint to locate related records in other tables.</span></span> <span data-ttu-id="b49fa-167">Dans Microsoft 365 Defender, vous pouvez obtenir des données connexes directement à partir de la `AlertEvidence` table.</span><span class="sxs-lookup"><span data-stu-id="b49fa-167">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |
| `Table` | <span data-ttu-id="b49fa-168">Cette colonne est généralement utilisée dans Microsoft Defender pour le point de terminaison pour obtenir des informations d’événement supplémentaires dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="b49fa-168">This column is typically used in Microsoft Defender for Endpoint for additional event information in other tables.</span></span> <span data-ttu-id="b49fa-169">Dans Microsoft 365 Defender, vous pouvez obtenir des données connexes directement à partir de la `AlertEvidence` table.</span><span class="sxs-lookup"><span data-stu-id="b49fa-169">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |

## <a name="adjust-existing-microsoft-defender-for-endpoint-queries"></a><span data-ttu-id="b49fa-170">Ajuster les requêtes Microsoft Defender existantes pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49fa-170">Adjust existing Microsoft Defender for Endpoint queries</span></span>
<span data-ttu-id="b49fa-171">Microsoft Defender pour les requêtes de points de terminaison fonctionnera, sauf s’ils font référence à la `DeviceAlertEvents` table.</span><span class="sxs-lookup"><span data-stu-id="b49fa-171">Microsoft Defender for Endpoint queries will work as-is unless they reference the `DeviceAlertEvents` table.</span></span> <span data-ttu-id="b49fa-172">Pour utiliser ces requêtes dans Microsoft 365 Defender, appliquez les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="b49fa-172">To use these queries in Microsoft 365 Defender, apply these changes:</span></span>

- <span data-ttu-id="b49fa-173">Remplacez `DeviceAlertEvents` par `AlertInfo` .</span><span class="sxs-lookup"><span data-stu-id="b49fa-173">Replace `DeviceAlertEvents` with `AlertInfo`.</span></span>
- <span data-ttu-id="b49fa-174">Rejoignez les `AlertInfo` `AlertEvidence` tables et `AlertId` pour obtenir des données équivalentes.</span><span class="sxs-lookup"><span data-stu-id="b49fa-174">Join the `AlertInfo` and the `AlertEvidence` tables on `AlertId` to get equivalent data.</span></span>

### <a name="original-query"></a><span data-ttu-id="b49fa-175">Requête d’origine</span><span class="sxs-lookup"><span data-stu-id="b49fa-175">Original query</span></span>
<span data-ttu-id="b49fa-176">La requête suivante utilise `DeviceAlertEvents` Microsoft Defender pour les points de terminaison pour obtenir les alertes qui impliquent des _powershell.exe_ :</span><span class="sxs-lookup"><span data-stu-id="b49fa-176">The following query uses `DeviceAlertEvents` in Microsoft Defender for Endpoint to get the alerts that involve _powershell.exe_ :</span></span>

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a><span data-ttu-id="b49fa-177">Requête modifiée</span><span class="sxs-lookup"><span data-stu-id="b49fa-177">Modified query</span></span>
<span data-ttu-id="b49fa-178">La requête suivante a été ajustée pour une utilisation dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b49fa-178">The following query has been adjusted for use in Microsoft 365 Defender.</span></span> <span data-ttu-id="b49fa-179">Au lieu de vérifier le nom de fichier directement à partir de `DeviceAlertEvents` , il rejoint `AlertEvidence` et recherche le nom de fichier dans cette table.</span><span class="sxs-lookup"><span data-stu-id="b49fa-179">Instead of checking the file name directly from `DeviceAlertEvents`, it joins `AlertEvidence` and checks for the file name in that table.</span></span>

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```

## <a name="related-topics"></a><span data-ttu-id="b49fa-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49fa-180">Related topics</span></span>
- [<span data-ttu-id="b49fa-181">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b49fa-181">Turn on Microsoft 365 Defender</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="b49fa-182">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="b49fa-182">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="b49fa-183">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="b49fa-183">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="b49fa-184">Chasse avancée dans Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49fa-184">Advanced hunting in Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)