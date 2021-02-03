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
ms.openlocfilehash: 4e008488bdd733c9a7ce5b418fb838e0fe880d9d
ms.sourcegitcommit: d354727303d9574991b5a0fd298d2c9414e19f6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "50080738"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-for-endpoint"></a><span data-ttu-id="b802d-104">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b802d-104">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="b802d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b802d-105">**Applies to:**</span></span>
- <span data-ttu-id="b802d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b802d-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="b802d-107">Déplacez vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison pour qu’ils recherchent de manière proactive les menaces à l’aide d’un ensemble plus large de données.</span><span class="sxs-lookup"><span data-stu-id="b802d-107">Move your advanced hunting workflows from Microsoft Defender for Endpoint to proactively hunt for threats using a broader set of data.</span></span> <span data-ttu-id="b802d-108">Dans Microsoft 365 Defender, vous avez accès aux données à partir d’autres solutions de sécurité Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="b802d-108">In Microsoft 365 Defender, you get access to data from other Microsoft 365 security solutions, including:</span></span>

- <span data-ttu-id="b802d-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b802d-109">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="b802d-110">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b802d-110">Microsoft Defender for Office 365</span></span>
- <span data-ttu-id="b802d-111">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b802d-111">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="b802d-112">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="b802d-112">Microsoft Defender for Identity</span></span>

>[!NOTE]
><span data-ttu-id="b802d-113">La plupart des clients Microsoft Defender pour Endpoint peuvent [utiliser Microsoft 365 Defender sans licences supplémentaires.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="b802d-113">Most Microsoft Defender for Endpoint customers can [use Microsoft 365 Defender without additional licenses](prerequisites.md#licensing-requirements).</span></span> <span data-ttu-id="b802d-114">Pour commencer la transition de vos flux de travail de recherche avancée à partir de Defender for Endpoint, [activer Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="b802d-114">To start transitioning your advanced hunting workflows from Defender for Endpoint, [turn on Microsoft 365 Defender](mtp-enable.md).</span></span>

<span data-ttu-id="b802d-115">Vous pouvez faire la transition sans affecter vos flux de travail Defender for Endpoint existants.</span><span class="sxs-lookup"><span data-stu-id="b802d-115">You can transition without affecting your existing Defender for Endpoint workflows.</span></span> <span data-ttu-id="b802d-116">Les requêtes enregistrées restent intactes et les règles de détection personnalisées continuent à s’exécuter et à générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="b802d-116">Saved queries remain intact, and custom detection rules continue to run and generate alerts.</span></span> <span data-ttu-id="b802d-117">Toutefois, elles seront visibles dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b802d-117">They will, however, be visible in Microsoft 365 Defender.</span></span> 

## <a name="schema-tables-in-microsoft-365-defender-only"></a><span data-ttu-id="b802d-118">Tableaux de schéma dans Microsoft 365 Defender uniquement</span><span class="sxs-lookup"><span data-stu-id="b802d-118">Schema tables in Microsoft 365 Defender only</span></span>
<span data-ttu-id="b802d-119">Le schéma de [recherche avancée Microsoft 365 Defender](advanced-hunting-schema-tables.md) fournit des tableaux supplémentaires contenant des données provenant de différentes solutions de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b802d-119">The [Microsoft 365 Defender advanced hunting schema](advanced-hunting-schema-tables.md) provides additional tables containing data from various Microsoft 365 security solutions.</span></span> <span data-ttu-id="b802d-120">Les tableaux suivants sont disponibles uniquement dans Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="b802d-120">The following tables are available only in Microsoft 365 Defender:</span></span>

| <span data-ttu-id="b802d-121">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="b802d-121">Table name</span></span> | <span data-ttu-id="b802d-122">Description</span><span class="sxs-lookup"><span data-stu-id="b802d-122">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="b802d-123">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="b802d-123">AlertEvidence</span></span>](advanced-hunting-alertevidence-table.md) | <span data-ttu-id="b802d-124">Fichiers, adresses IP, URL, utilisateurs ou appareils associés à des alertes</span><span class="sxs-lookup"><span data-stu-id="b802d-124">Files, IP addresses, URLs, users, or devices associated with alerts</span></span> |
| [<span data-ttu-id="b802d-125">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="b802d-125">AlertInfo</span></span>](advanced-hunting-alertinfo-table.md) | <span data-ttu-id="b802d-126">Alertes de Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité, y compris les informations de gravité et les catégories de menaces</span><span class="sxs-lookup"><span data-stu-id="b802d-126">Alerts from Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity, including severity information and threat categories</span></span>  |
| [<span data-ttu-id="b802d-127">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-127">AppFileEvents</span></span>](advanced-hunting-appfileevents-table.md) | <span data-ttu-id="b802d-128">Activités liées aux fichiers dans les applications et services cloud</span><span class="sxs-lookup"><span data-stu-id="b802d-128">File-related activities in cloud apps and services</span></span> |
| [<span data-ttu-id="b802d-129">EmailAttachmentInfo</span><span class="sxs-lookup"><span data-stu-id="b802d-129">EmailAttachmentInfo</span></span>](advanced-hunting-emailattachmentinfo-table.md) | <span data-ttu-id="b802d-130">Informations sur les fichiers joints aux e-mails</span><span class="sxs-lookup"><span data-stu-id="b802d-130">Information about files attached to emails</span></span> |
| [<span data-ttu-id="b802d-131">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-131">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="b802d-132">Événements de messagerie Microsoft 365, y compris la remise et le blocage des messages électroniques</span><span class="sxs-lookup"><span data-stu-id="b802d-132">Microsoft 365 email events, including email delivery and blocking events</span></span> |
| [<span data-ttu-id="b802d-133">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-133">EmailPostDeliveryEvents</span></span>](advanced-hunting-emailpostdeliveryevents-table.md) | <span data-ttu-id="b802d-134">Événements de sécurité qui se produisent après la remise, une fois que Microsoft 365 a remis les messages électroniques à la boîte aux lettres du destinataire</span><span class="sxs-lookup"><span data-stu-id="b802d-134">Security events that occur post-delivery, after Microsoft 365 has delivered the emails to the recipient mailbox</span></span> |
| [<span data-ttu-id="b802d-135">EmailUrlInfo</span><span class="sxs-lookup"><span data-stu-id="b802d-135">EmailUrlInfo</span></span>](advanced-hunting-emailurlinfo-table.md) | <span data-ttu-id="b802d-136">Informations sur les URL des e-mails</span><span class="sxs-lookup"><span data-stu-id="b802d-136">Information about URLs on emails</span></span> |
| [<span data-ttu-id="b802d-137">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-137">IdentityDirectoryEvents</span></span>](advanced-hunting-identitydirectoryevents-table.md) | <span data-ttu-id="b802d-138">Événements impliquant un contrôleur de domaine local exécutant Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="b802d-138">Events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="b802d-139">Ce tableau couvre une plage d’événements liés à l’identité et d’événements système sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b802d-139">This table covers a range of identity-related events and system events on the domain controller.</span></span> |
| [<span data-ttu-id="b802d-140">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="b802d-140">IdentityInfo</span></span>](advanced-hunting-identityinfo-table.md) | <span data-ttu-id="b802d-141">Informations de compte provenant de différentes sources, notamment Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b802d-141">Account information from various sources, including Azure Active Directory</span></span> |
| [<span data-ttu-id="b802d-142">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-142">IdentityLogonEvents</span></span>](advanced-hunting-identitylogonevents-table.md) | <span data-ttu-id="b802d-143">Événements d’authentification sur Active Directory et les services en ligne Microsoft</span><span class="sxs-lookup"><span data-stu-id="b802d-143">Authentication events on Active Directory and Microsoft online services</span></span> |
| [<span data-ttu-id="b802d-144">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-144">IdentityQueryEvents</span></span>](advanced-hunting-identityqueryevents-table.md) | <span data-ttu-id="b802d-145">Requêtes pour les objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines</span><span class="sxs-lookup"><span data-stu-id="b802d-145">Queries for Active Directory objects, such as users, groups, devices, and domains</span></span> |

## <a name="map-devicealertevents-table"></a><span data-ttu-id="b802d-146">Table Map DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-146">Map DeviceAlertEvents table</span></span>
<span data-ttu-id="b802d-147">Les `AlertInfo` `AlertEvidence` tableaux et les tables `DeviceAlertEvents` remplacent le tableau dans le schéma Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b802d-147">The `AlertInfo` and `AlertEvidence` tables replace the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="b802d-148">En plus des données sur les alertes d’appareil, ces deux tableaux incluent des données sur les alertes pour les identités, les applications et les e-mails.</span><span class="sxs-lookup"><span data-stu-id="b802d-148">In addition to data about device alerts, these two tables include data about alerts for identities, apps, and emails.</span></span>

<span data-ttu-id="b802d-149">Utilisez le tableau suivant pour vérifier la façon dont les `DeviceAlertEvents` colonnes sont m mapées aux colonnes des `AlertInfo` tableaux et des `AlertEvidence` colonnes.</span><span class="sxs-lookup"><span data-stu-id="b802d-149">Use the following table to check how `DeviceAlertEvents` columns map to columns in the `AlertInfo` and `AlertEvidence` tables.</span></span>

>[!TIP]
><span data-ttu-id="b802d-150">Outre les colonnes du tableau suivant, le tableau inclut de nombreuses autres colonnes qui fournissent une image plus globale des alertes provenant de `AlertEvidence` différentes sources.</span><span class="sxs-lookup"><span data-stu-id="b802d-150">In addition to the columns the following table, the `AlertEvidence` table includes many other columns that provide a more holistic picture of alerts from various sources.</span></span> [<span data-ttu-id="b802d-151">Voir toutes les colonnes AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="b802d-151">See all AlertEvidence columns</span></span>](advanced-hunting-alertevidence-table.md) 

| <span data-ttu-id="b802d-152">Colonne DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-152">DeviceAlertEvents column</span></span> | <span data-ttu-id="b802d-153">Où trouver les mêmes données dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b802d-153">Where to find the same data in Microsoft 365 Defender</span></span> |
|-------------|-----------|-------------|-------------|
| `AlertId` | <span data-ttu-id="b802d-154">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="b802d-154">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `Timestamp` | <span data-ttu-id="b802d-155">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="b802d-155">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `DeviceId` | <span data-ttu-id="b802d-156">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-156">`AlertEvidence` table</span></span> |
| `DeviceName` | <span data-ttu-id="b802d-157">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-157">`AlertEvidence` table</span></span> |
| `Severity` | <span data-ttu-id="b802d-158">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="b802d-158">`AlertInfo` table</span></span> |
| `Category` | <span data-ttu-id="b802d-159">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="b802d-159">`AlertInfo` table</span></span> |
| `Title` | <span data-ttu-id="b802d-160">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="b802d-160">`AlertInfo` table</span></span> |
| `FileName` | <span data-ttu-id="b802d-161">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-161">`AlertEvidence` table</span></span> |
| `SHA1` | <span data-ttu-id="b802d-162">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-162">`AlertEvidence` table</span></span> |
| `RemoteUrl` | <span data-ttu-id="b802d-163">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-163">`AlertEvidence` table</span></span> |
| `RemoteIP` | <span data-ttu-id="b802d-164">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="b802d-164">`AlertEvidence` table</span></span> |
| `AttackTechniques` | <span data-ttu-id="b802d-165">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="b802d-165">`AlertInfo` table</span></span> |
| `ReportId` | <span data-ttu-id="b802d-166">Cette colonne est généralement utilisée dans Microsoft Defender pour point de terminaison pour rechercher des enregistrements connexes dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="b802d-166">This column is typically used in Microsoft Defender for Endpoint to locate related records in other tables.</span></span> <span data-ttu-id="b802d-167">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="b802d-167">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |
| `Table` | <span data-ttu-id="b802d-168">Cette colonne est généralement utilisée dans Microsoft Defender pour le point de terminaison pour des informations supplémentaires sur les événements dans d’autres tableaux.</span><span class="sxs-lookup"><span data-stu-id="b802d-168">This column is typically used in Microsoft Defender for Endpoint for additional event information in other tables.</span></span> <span data-ttu-id="b802d-169">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="b802d-169">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |

## <a name="adjust-existing-microsoft-defender-for-endpoint-queries"></a><span data-ttu-id="b802d-170">Ajuster les requêtes Microsoft Defender pour les points de terminaison existantes</span><span class="sxs-lookup"><span data-stu-id="b802d-170">Adjust existing Microsoft Defender for Endpoint queries</span></span>
<span data-ttu-id="b802d-171">Les requêtes Microsoft Defender pour les points de terminaison fonctionneront telles qu’elles sont sauf si elles font référence au `DeviceAlertEvents` tableau.</span><span class="sxs-lookup"><span data-stu-id="b802d-171">Microsoft Defender for Endpoint queries will work as-is unless they reference the `DeviceAlertEvents` table.</span></span> <span data-ttu-id="b802d-172">Pour utiliser ces requêtes dans Microsoft 365 Defender, appliquez les modifications ci-après :</span><span class="sxs-lookup"><span data-stu-id="b802d-172">To use these queries in Microsoft 365 Defender, apply these changes:</span></span>

- <span data-ttu-id="b802d-173">Remplacez `DeviceAlertEvents` par `AlertInfo` .</span><span class="sxs-lookup"><span data-stu-id="b802d-173">Replace `DeviceAlertEvents` with `AlertInfo`.</span></span>
- <span data-ttu-id="b802d-174">Joignez les `AlertInfo` tables et les tables pour obtenir des données `AlertEvidence` `AlertId` équivalentes.</span><span class="sxs-lookup"><span data-stu-id="b802d-174">Join the `AlertInfo` and the `AlertEvidence` tables on `AlertId` to get equivalent data.</span></span>

### <a name="original-query"></a><span data-ttu-id="b802d-175">Requête d’origine</span><span class="sxs-lookup"><span data-stu-id="b802d-175">Original query</span></span>
<span data-ttu-id="b802d-176">La requête suivante utilise Microsoft Defender pour le point de terminaison pour obtenir les alertes qui `DeviceAlertEvents` impliquent _powershell.exe_:</span><span class="sxs-lookup"><span data-stu-id="b802d-176">The following query uses `DeviceAlertEvents` in Microsoft Defender for Endpoint to get the alerts that involve _powershell.exe_:</span></span>

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a><span data-ttu-id="b802d-177">Requête modifiée</span><span class="sxs-lookup"><span data-stu-id="b802d-177">Modified query</span></span>
<span data-ttu-id="b802d-178">La requête suivante a été ajustée pour être utilisé dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b802d-178">The following query has been adjusted for use in Microsoft 365 Defender.</span></span> <span data-ttu-id="b802d-179">Au lieu de vérifier le nom de fichier directement à partir de , il joint et vérifie le nom de fichier `DeviceAlertEvents` `AlertEvidence` dans cette table.</span><span class="sxs-lookup"><span data-stu-id="b802d-179">Instead of checking the file name directly from `DeviceAlertEvents`, it joins `AlertEvidence` and checks for the file name in that table.</span></span>

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```

## <a name="migrate-custom-detection-rules"></a><span data-ttu-id="b802d-180">Migrer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="b802d-180">Migrate custom detection rules</span></span>

<span data-ttu-id="b802d-181">Lorsque les règles microsoft Defender pour les points de terminaison sont modifiées sur Microsoft 365 Defender, elles continuent de fonctionner comme avant si la requête résultante examine uniquement les tables des appareils.</span><span class="sxs-lookup"><span data-stu-id="b802d-181">When Microsoft Defender for Endpoint rules are edited on Microsoft 365 Defender, they continue to function as before if the resulting query looks at device tables only.</span></span> <span data-ttu-id="b802d-182">Par exemple, les alertes générées par des règles de détection personnalisées qui interrogent uniquement les tables des appareils continueront d’être remis à votre SIEM et de générer des notifications par courrier électronique, selon la façon dont vous les avez configurées dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b802d-182">For example, alerts generated by custom detection rules that query only device tables will continue to be delivered to your SIEM and generate email notifications, depending on how you’ve configured these in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="b802d-183">Toutes les règles de suppression existantes dans Defender pour le point de terminaison continueront également de s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="b802d-183">Any existing suppression rules in Defender for Endpoint will also continue to apply.</span></span>

<span data-ttu-id="b802d-184">Une fois que vous avez modifié une règle Defender pour point de terminaison afin qu’elle interroge les tables d’identité et de messagerie, qui sont uniquement disponibles dans Microsoft 365 Defender, la règle est automatiquement déplacée vers Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b802d-184">Once you edit a Defender for Endpoint rule so that it queries identity and email tables, which are only available in Microsoft 365 Defender, the rule is automatically moved to Microsoft 365 Defender.</span></span> 

<span data-ttu-id="b802d-185">Alertes générées par la règle migré :</span><span class="sxs-lookup"><span data-stu-id="b802d-185">Alerts generated by the migrated rule:</span></span>

- <span data-ttu-id="b802d-186">Ne sont plus visibles dans le portail Defender pour point de terminaison (Centre de sécurité Microsoft Defender)</span><span class="sxs-lookup"><span data-stu-id="b802d-186">Are no longer visible in the Defender for Endpoint portal (Microsoft Defender Security Center)</span></span>
- <span data-ttu-id="b802d-187">Ne plus être remis à votre SIEM ou générer des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="b802d-187">Stop being delivered to your SIEM or generate email notifications.</span></span> <span data-ttu-id="b802d-188">Pour contourner ce changement, configurez les notifications via Microsoft 365 Defender pour obtenir les alertes.</span><span class="sxs-lookup"><span data-stu-id="b802d-188">To work around this change, configure notifications through Microsoft 365 Defender to get the alerts.</span></span> <span data-ttu-id="b802d-189">Vous pouvez utiliser [l’API Microsoft 365 Defender](api-incident.md) pour recevoir des notifications pour les alertes de détection des clients ou les incidents connexes.</span><span class="sxs-lookup"><span data-stu-id="b802d-189">You can use the [Microsoft 365 Defender API](api-incident.md) to receive notifications for customer detection alerts or related incidents.</span></span>
- <span data-ttu-id="b802d-190">Ne sera pas supprimé par les règles de suppression des points de terminaison de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b802d-190">Won't be suppressed by Microsoft Defender for Endpoint suppression rules.</span></span> <span data-ttu-id="b802d-191">Pour empêcher la générer des alertes pour certains utilisateurs, périphériques ou boîtes aux lettres, modifiez les requêtes correspondantes pour exclure explicitement ces entités.</span><span class="sxs-lookup"><span data-stu-id="b802d-191">To prevent alerts from being generated for certain users, devices, or mailboxes, modify the corresponding queries to exclude those entities explicitly.</span></span>

<span data-ttu-id="b802d-192">Si vous modifiez une règle de cette façon, vous serez invité à confirmer l’application de ces modifications.</span><span class="sxs-lookup"><span data-stu-id="b802d-192">If you do edit a rule this way, you will be prompted for confirmation before such changes are applied.</span></span>

<span data-ttu-id="b802d-193">Les nouvelles alertes générées par des règles de détection personnalisées dans le portail Microsoft 365 Defender sont affichées dans une page d’alerte qui fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b802d-193">New alerts generated by custom detection rules in Microsoft 365 Defender portal are displayed in an alert page that provides the following information:</span></span>

- <span data-ttu-id="b802d-194">Titre et description de l’alerte</span><span class="sxs-lookup"><span data-stu-id="b802d-194">Alert title and description</span></span> 
- <span data-ttu-id="b802d-195">Ressources impactées</span><span class="sxs-lookup"><span data-stu-id="b802d-195">Impacted assets</span></span>
- <span data-ttu-id="b802d-196">Actions prises en réponse à l’alerte</span><span class="sxs-lookup"><span data-stu-id="b802d-196">Actions taken in response to the alert</span></span>
- <span data-ttu-id="b802d-197">Résultats de la requête qui ont déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="b802d-197">Query results that triggered the alert</span></span> 
- <span data-ttu-id="b802d-198">Informations sur la règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="b802d-198">Information on the custom detection rule</span></span> 
 
![Image de la nouvelle page d’alerte](../../media/newalertpage.png)

## <a name="write-queries-without-devicealertevents"></a><span data-ttu-id="b802d-200">Écrire des requêtes sans DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="b802d-200">Write queries without DeviceAlertEvents</span></span>

<span data-ttu-id="b802d-201">Dans le schéma Microsoft 365 Defender, les tableaux et les tableaux sont fournis pour prendre en charge les diverses informations qui accompagnent les alertes provenant de `AlertInfo` `AlertEvidence` différentes sources.</span><span class="sxs-lookup"><span data-stu-id="b802d-201">In the Microsoft 365 Defender schema, the `AlertInfo` and `AlertEvidence` tables are provided to accommodate the diverse set of information that accompany alerts from various sources.</span></span> 

<span data-ttu-id="b802d-202">Pour obtenir les mêmes informations d’alerte que vous avez utilisées pour obtenir à partir de la table dans le schéma Microsoft Defender for Endpoint, filtrez la table, puis joignez chaque ID unique à la table, qui fournit des informations détaillées sur l’événement et `DeviceAlertEvents` `AlertInfo` l’entité. `ServiceSource` `AlertEvidence`</span><span class="sxs-lookup"><span data-stu-id="b802d-202">To get the same alert information that you used to get from the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema, filter the `AlertInfo` table by `ServiceSource` and then join each unique ID with the `AlertEvidence` table, which provides detailed event and entity information.</span></span> 

<span data-ttu-id="b802d-203">Consultez l’exemple de requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b802d-203">See the sample query below:</span></span>

```kusto
AlertInfo
| where Timestamp > ago(7d)
| where ServiceSource == "Microsoft Defender for Endpoint"
| join AlertEvidence on AlertId
```

<span data-ttu-id="b802d-204">Cette requête produit beaucoup plus de colonnes que dans le schéma `DeviceAlertEvents` Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b802d-204">This query yields many more columns than `DeviceAlertEvents` in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="b802d-205">Pour que les résultats restent gérables, utilisez cette rubrique `project` pour obtenir uniquement les colonnes qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="b802d-205">To keep results manageable, use `project` to get only the columns you are interested in.</span></span> <span data-ttu-id="b802d-206">L’exemple ci-dessous projete les colonnes qui peuvent vous intéresser lorsque l’enquête a détecté une activité PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b802d-206">The example below projects columns you might be interested in when the investigation detected PowerShell activity:</span></span>

```kusto
AlertInfo
| where Timestamp > ago(7d)
| where ServiceSource == "Microsoft Defender for Endpoint"
    and AttackTechniques has "powershell"
| join AlertEvidence on AlertId
| project Timestamp, Title, AlertId, DeviceName, FileName, ProcessCommandLine 
```

<span data-ttu-id="b802d-207">Si vous souhaitez filtrer des entités spécifiques impliquées dans les alertes, vous pouvez le faire en spécifiant le type d’entité et la valeur que vous souhaitez `EntityType` filtrer.</span><span class="sxs-lookup"><span data-stu-id="b802d-207">If you'd like to filter for specific entities involved in the alerts, you can do so by specifying the entity type in `EntityType` and the value you would like to filter for.</span></span> <span data-ttu-id="b802d-208">L’exemple suivant recherche une adresse IP spécifique :</span><span class="sxs-lookup"><span data-stu-id="b802d-208">The following example looks for a specific IP address:</span></span>

```kusto
AlertInfo
| where Title == "Insert_your_alert_title"
| join AlertEvidence on AlertId 
| where EntityType == "Ip" and RemoteIP == "192.88.99.01" 
```

## <a name="see-also"></a><span data-ttu-id="b802d-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b802d-209">See also</span></span>
- [<span data-ttu-id="b802d-210">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b802d-210">Turn on Microsoft 365 Defender</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="b802d-211">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="b802d-211">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="b802d-212">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="b802d-212">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="b802d-213">Recherche avancée dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b802d-213">Advanced hunting in Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)