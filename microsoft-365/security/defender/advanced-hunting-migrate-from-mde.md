---
title: Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison
description: Découvrez comment ajuster vos requêtes Microsoft Defender for Endpoint afin de pouvoir les utiliser dans Microsoft 365 Defender
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, Microsoft Defender pour le point de terminaison, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, mappage
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.custom: seo-marvel-apr2020
ms.technology: m365d
ms.openlocfilehash: ba6f84f9f08d0635dab6ac65eaa697b8e0e73df7
ms.sourcegitcommit: fb6c5e04ade1e82b26b2f911577b5ac721f1c544
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "52470687"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-for-endpoint"></a><span data-ttu-id="8bc05-104">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8bc05-104">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8bc05-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8bc05-105">**Applies to:**</span></span>
- <span data-ttu-id="8bc05-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8bc05-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="8bc05-107">Déplacez vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison pour qu’ils recherchent de manière proactive les menaces à l’aide d’un ensemble plus large de données.</span><span class="sxs-lookup"><span data-stu-id="8bc05-107">Move your advanced hunting workflows from Microsoft Defender for Endpoint to proactively hunt for threats using a broader set of data.</span></span> <span data-ttu-id="8bc05-108">Dans Microsoft 365 Defender, vous avez accès aux données à partir d’autres solutions Microsoft 365 sécurité, notamment :</span><span class="sxs-lookup"><span data-stu-id="8bc05-108">In Microsoft 365 Defender, you get access to data from other Microsoft 365 security solutions, including:</span></span>

- <span data-ttu-id="8bc05-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8bc05-109">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="8bc05-110">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8bc05-110">Microsoft Defender for Office 365</span></span>
- <span data-ttu-id="8bc05-111">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="8bc05-111">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="8bc05-112">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="8bc05-112">Microsoft Defender for Identity</span></span>

>[!NOTE]
><span data-ttu-id="8bc05-113">La plupart des clients Microsoft Defender pour Endpoint peuvent [utiliser Microsoft 365 Defender sans licences supplémentaires.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="8bc05-113">Most Microsoft Defender for Endpoint customers can [use Microsoft 365 Defender without additional licenses](prerequisites.md#licensing-requirements).</span></span> <span data-ttu-id="8bc05-114">Pour commencer la transition de vos flux de travail de recherche avancée à partir de Defender pour Endpoint, Microsoft 365 [Defender](m365d-enable.md).</span><span class="sxs-lookup"><span data-stu-id="8bc05-114">To start transitioning your advanced hunting workflows from Defender for Endpoint, [turn on Microsoft 365 Defender](m365d-enable.md).</span></span>

<span data-ttu-id="8bc05-115">Vous pouvez faire la transition sans affecter vos flux de travail Defender for Endpoint existants.</span><span class="sxs-lookup"><span data-stu-id="8bc05-115">You can transition without affecting your existing Defender for Endpoint workflows.</span></span> <span data-ttu-id="8bc05-116">Les requêtes enregistrées restent intactes et les règles de détection personnalisées continuent à s’exécuter et à générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="8bc05-116">Saved queries remain intact, and custom detection rules continue to run and generate alerts.</span></span> <span data-ttu-id="8bc05-117">Toutefois, elles seront visibles dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8bc05-117">They will, however, be visible in Microsoft 365 Defender.</span></span> 

## <a name="schema-tables-in-microsoft-365-defender-only"></a><span data-ttu-id="8bc05-118">Tables de schéma dans Microsoft 365 Defender uniquement</span><span class="sxs-lookup"><span data-stu-id="8bc05-118">Schema tables in Microsoft 365 Defender only</span></span>
<span data-ttu-id="8bc05-119">Le [Microsoft 365 de recherche](advanced-hunting-schema-tables.md) avancée Defender fournit des tableaux supplémentaires contenant des données provenant de Microsoft 365 solutions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8bc05-119">The [Microsoft 365 Defender advanced hunting schema](advanced-hunting-schema-tables.md) provides additional tables containing data from various Microsoft 365 security solutions.</span></span> <span data-ttu-id="8bc05-120">Les tableaux suivants sont disponibles uniquement dans Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="8bc05-120">The following tables are available only in Microsoft 365 Defender:</span></span>

| <span data-ttu-id="8bc05-121">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="8bc05-121">Table name</span></span> | <span data-ttu-id="8bc05-122">Description</span><span class="sxs-lookup"><span data-stu-id="8bc05-122">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="8bc05-123">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="8bc05-123">AlertEvidence</span></span>](advanced-hunting-alertevidence-table.md) | <span data-ttu-id="8bc05-124">Fichiers, adresses IP, URL, utilisateurs ou appareils associés à des alertes</span><span class="sxs-lookup"><span data-stu-id="8bc05-124">Files, IP addresses, URLs, users, or devices associated with alerts</span></span> |
| [<span data-ttu-id="8bc05-125">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="8bc05-125">AlertInfo</span></span>](advanced-hunting-alertinfo-table.md) | <span data-ttu-id="8bc05-126">Alertes de Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité, y compris les informations de gravité et les catégories de menaces</span><span class="sxs-lookup"><span data-stu-id="8bc05-126">Alerts from Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity, including severity information and threat categories</span></span>  |
| [<span data-ttu-id="8bc05-127">EmailAttachmentInfo</span><span class="sxs-lookup"><span data-stu-id="8bc05-127">EmailAttachmentInfo</span></span>](advanced-hunting-emailattachmentinfo-table.md) | <span data-ttu-id="8bc05-128">Informations sur les fichiers joints aux e-mails</span><span class="sxs-lookup"><span data-stu-id="8bc05-128">Information about files attached to emails</span></span> |
| [<span data-ttu-id="8bc05-129">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-129">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="8bc05-130">Microsoft 365 e-mail, y compris la remise et le blocage des événements</span><span class="sxs-lookup"><span data-stu-id="8bc05-130">Microsoft 365 email events, including email delivery and blocking events</span></span> |
| [<span data-ttu-id="8bc05-131">EmailPostDeliveryEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-131">EmailPostDeliveryEvents</span></span>](advanced-hunting-emailpostdeliveryevents-table.md) | <span data-ttu-id="8bc05-132">Événements de sécurité qui se produisent après la remise, Microsoft 365 les e-mails à la boîte aux lettres du destinataire</span><span class="sxs-lookup"><span data-stu-id="8bc05-132">Security events that occur post-delivery, after Microsoft 365 has delivered the emails to the recipient mailbox</span></span> |
| [<span data-ttu-id="8bc05-133">EmailUrlInfo</span><span class="sxs-lookup"><span data-stu-id="8bc05-133">EmailUrlInfo</span></span>](advanced-hunting-emailurlinfo-table.md) | <span data-ttu-id="8bc05-134">Informations sur les URL des e-mails</span><span class="sxs-lookup"><span data-stu-id="8bc05-134">Information about URLs on emails</span></span> |
| [<span data-ttu-id="8bc05-135">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-135">IdentityDirectoryEvents</span></span>](advanced-hunting-identitydirectoryevents-table.md) | <span data-ttu-id="8bc05-136">Événements impliquant un contrôleur de domaine local exécutant Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="8bc05-136">Events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="8bc05-137">Ce tableau couvre une plage d’événements liés à l’identité et d’événements système sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="8bc05-137">This table covers a range of identity-related events and system events on the domain controller.</span></span> |
| [<span data-ttu-id="8bc05-138">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="8bc05-138">IdentityInfo</span></span>](advanced-hunting-identityinfo-table.md) | <span data-ttu-id="8bc05-139">Informations de compte provenant de différentes sources, notamment Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8bc05-139">Account information from various sources, including Azure Active Directory</span></span> |
| [<span data-ttu-id="8bc05-140">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-140">IdentityLogonEvents</span></span>](advanced-hunting-identitylogonevents-table.md) | <span data-ttu-id="8bc05-141">Événements d’authentification sur Active Directory et les services en ligne Microsoft</span><span class="sxs-lookup"><span data-stu-id="8bc05-141">Authentication events on Active Directory and Microsoft online services</span></span> |
| [<span data-ttu-id="8bc05-142">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-142">IdentityQueryEvents</span></span>](advanced-hunting-identityqueryevents-table.md) | <span data-ttu-id="8bc05-143">Requêtes pour les objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines</span><span class="sxs-lookup"><span data-stu-id="8bc05-143">Queries for Active Directory objects, such as users, groups, devices, and domains</span></span> |

>[!IMPORTANT]
> <span data-ttu-id="8bc05-144">Les requêtes et les détections personnalisées qui utilisent des tables de schéma qui sont uniquement disponibles dans Microsoft 365 Defender ne peuvent être vues que dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8bc05-144">Queries and custom detections which use schema tables that are only available in Microsoft 365 Defender can only be viewed in Microsoft 365 Defender.</span></span>

## <a name="map-devicealertevents-table"></a><span data-ttu-id="8bc05-145">Table Map DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-145">Map DeviceAlertEvents table</span></span>
<span data-ttu-id="8bc05-146">Les `AlertInfo` `AlertEvidence` tableaux et les tables `DeviceAlertEvents` remplacent le tableau dans le schéma Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="8bc05-146">The `AlertInfo` and `AlertEvidence` tables replace the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="8bc05-147">En plus des données sur les alertes d’appareil, ces deux tableaux incluent des données sur les alertes pour les identités, les applications et les e-mails.</span><span class="sxs-lookup"><span data-stu-id="8bc05-147">In addition to data about device alerts, these two tables include data about alerts for identities, apps, and emails.</span></span>

<span data-ttu-id="8bc05-148">Utilisez le tableau suivant pour vérifier la façon dont les `DeviceAlertEvents` colonnes sont m mapées aux colonnes des `AlertInfo` tableaux et des `AlertEvidence` colonnes.</span><span class="sxs-lookup"><span data-stu-id="8bc05-148">Use the following table to check how `DeviceAlertEvents` columns map to columns in the `AlertInfo` and `AlertEvidence` tables.</span></span>

>[!TIP]
><span data-ttu-id="8bc05-149">Outre les colonnes du tableau suivant, le tableau inclut de nombreuses autres colonnes qui fournissent une image plus globale des alertes provenant de `AlertEvidence` différentes sources.</span><span class="sxs-lookup"><span data-stu-id="8bc05-149">In addition to the columns in the following table, the `AlertEvidence` table includes many other columns that provide a more holistic picture of alerts from various sources.</span></span> [<span data-ttu-id="8bc05-150">Voir toutes les colonnes AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="8bc05-150">See all AlertEvidence columns</span></span>](advanced-hunting-alertevidence-table.md) 

| <span data-ttu-id="8bc05-151">Colonne DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-151">DeviceAlertEvents column</span></span> | <span data-ttu-id="8bc05-152">Où trouver les mêmes données dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8bc05-152">Where to find the same data in Microsoft 365 Defender</span></span> |
|-------------|-----------|-------------|-------------|
| `AlertId` | <span data-ttu-id="8bc05-153">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="8bc05-153">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `Timestamp` | <span data-ttu-id="8bc05-154">`AlertInfo` et  `AlertEvidence` tableaux</span><span class="sxs-lookup"><span data-stu-id="8bc05-154">`AlertInfo` and  `AlertEvidence` tables</span></span> |
| `DeviceId` | <span data-ttu-id="8bc05-155">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-155">`AlertEvidence` table</span></span> |
| `DeviceName` | <span data-ttu-id="8bc05-156">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-156">`AlertEvidence` table</span></span> |
| `Severity` | <span data-ttu-id="8bc05-157">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-157">`AlertInfo` table</span></span> |
| `Category` | <span data-ttu-id="8bc05-158">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-158">`AlertInfo` table</span></span> |
| `Title` | <span data-ttu-id="8bc05-159">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-159">`AlertInfo` table</span></span> |
| `FileName` | <span data-ttu-id="8bc05-160">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-160">`AlertEvidence` table</span></span> |
| `SHA1` | <span data-ttu-id="8bc05-161">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-161">`AlertEvidence` table</span></span> |
| `RemoteUrl` | <span data-ttu-id="8bc05-162">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-162">`AlertEvidence` table</span></span> |
| `RemoteIP` | <span data-ttu-id="8bc05-163">`AlertEvidence` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-163">`AlertEvidence` table</span></span> |
| `AttackTechniques` | <span data-ttu-id="8bc05-164">`AlertInfo` table</span><span class="sxs-lookup"><span data-stu-id="8bc05-164">`AlertInfo` table</span></span> |
| `ReportId` | <span data-ttu-id="8bc05-165">Cette colonne est généralement utilisée dans Microsoft Defender pour point de terminaison pour rechercher des enregistrements connexes dans d’autres tables.</span><span class="sxs-lookup"><span data-stu-id="8bc05-165">This column is typically used in Microsoft Defender for Endpoint to locate related records in other tables.</span></span> <span data-ttu-id="8bc05-166">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="8bc05-166">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |
| `Table` | <span data-ttu-id="8bc05-167">Cette colonne est généralement utilisée dans Microsoft Defender pour point de terminaison pour des informations supplémentaires sur les événements dans d’autres tableaux.</span><span class="sxs-lookup"><span data-stu-id="8bc05-167">This column is typically used in Microsoft Defender for Endpoint for additional event information in other tables.</span></span> <span data-ttu-id="8bc05-168">Dans Microsoft 365 Defender, vous pouvez obtenir des données associées directement à partir du `AlertEvidence` tableau.</span><span class="sxs-lookup"><span data-stu-id="8bc05-168">In Microsoft 365 Defender, you can get related data directly from the `AlertEvidence` table.</span></span> |

## <a name="adjust-existing-microsoft-defender-for-endpoint-queries"></a><span data-ttu-id="8bc05-169">Ajuster les requêtes Microsoft Defender pour les points de terminaison existantes</span><span class="sxs-lookup"><span data-stu-id="8bc05-169">Adjust existing Microsoft Defender for Endpoint queries</span></span>
<span data-ttu-id="8bc05-170">Les requêtes Microsoft Defender pour les points de terminaison fonctionneront telles qu’elles sont sauf si elles font référence au `DeviceAlertEvents` tableau.</span><span class="sxs-lookup"><span data-stu-id="8bc05-170">Microsoft Defender for Endpoint queries will work as-is unless they reference the `DeviceAlertEvents` table.</span></span> <span data-ttu-id="8bc05-171">Pour utiliser ces requêtes dans Microsoft 365 Defender, appliquez les modifications ci-après :</span><span class="sxs-lookup"><span data-stu-id="8bc05-171">To use these queries in Microsoft 365 Defender, apply these changes:</span></span>

- <span data-ttu-id="8bc05-172">Remplacez `DeviceAlertEvents` par `AlertInfo` .</span><span class="sxs-lookup"><span data-stu-id="8bc05-172">Replace `DeviceAlertEvents` with `AlertInfo`.</span></span>
- <span data-ttu-id="8bc05-173">Joignez les `AlertInfo` tables et les tables pour obtenir des données `AlertEvidence` `AlertId` équivalentes.</span><span class="sxs-lookup"><span data-stu-id="8bc05-173">Join the `AlertInfo` and the `AlertEvidence` tables on `AlertId` to get equivalent data.</span></span>

### <a name="original-query"></a><span data-ttu-id="8bc05-174">Requête d’origine</span><span class="sxs-lookup"><span data-stu-id="8bc05-174">Original query</span></span>
<span data-ttu-id="8bc05-175">La requête suivante utilise Microsoft Defender pour le point de terminaison pour obtenir les alertes qui `DeviceAlertEvents` impliquent _powershell.exe_:</span><span class="sxs-lookup"><span data-stu-id="8bc05-175">The following query uses `DeviceAlertEvents` in Microsoft Defender for Endpoint to get the alerts that involve _powershell.exe_:</span></span>

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a><span data-ttu-id="8bc05-176">Requête modifiée</span><span class="sxs-lookup"><span data-stu-id="8bc05-176">Modified query</span></span>
<span data-ttu-id="8bc05-177">La requête suivante a été ajustée pour être Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8bc05-177">The following query has been adjusted for use in Microsoft 365 Defender.</span></span> <span data-ttu-id="8bc05-178">Au lieu de vérifier le nom de fichier directement à partir de , il joint et recherche le nom de fichier `DeviceAlertEvents` `AlertEvidence` dans cette table.</span><span class="sxs-lookup"><span data-stu-id="8bc05-178">Instead of checking the file name directly from `DeviceAlertEvents`, it joins `AlertEvidence` and checks for the file name in that table.</span></span>

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```

## <a name="migrate-custom-detection-rules"></a><span data-ttu-id="8bc05-179">Migrer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="8bc05-179">Migrate custom detection rules</span></span>

<span data-ttu-id="8bc05-180">Lorsque les règles microsoft Defender pour les points de terminaison sont modifiées sur Microsoft 365 Defender, elles continuent de fonctionner comme avant si la requête résultante examine uniquement les tables des appareils.</span><span class="sxs-lookup"><span data-stu-id="8bc05-180">When Microsoft Defender for Endpoint rules are edited on Microsoft 365 Defender, they continue to function as before if the resulting query looks at device tables only.</span></span> 

<span data-ttu-id="8bc05-181">Par exemple, les alertes générées par des règles de détection personnalisées qui interrogent uniquement les tables des appareils continueront d’être remis à votre SIEM et de générer des notifications par courrier électronique, selon la façon dont vous les avez configurées dans Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="8bc05-181">For example, alerts generated by custom detection rules that query only device tables will continue to be delivered to your SIEM and generate email notifications, depending on how you’ve configured these in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="8bc05-182">Toutes les règles de suppression existantes dans Defender pour le point de terminaison continueront également de s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="8bc05-182">Any existing suppression rules in Defender for Endpoint will also continue to apply.</span></span>

<span data-ttu-id="8bc05-183">Une fois que vous avez modifié une règle Defender for Endpoint afin qu’elle interroge les tables d’identité et de messagerie, qui sont uniquement disponibles dans Microsoft 365 Defender, la règle est automatiquement déplacée vers Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8bc05-183">Once you edit a Defender for Endpoint rule so that it queries identity and email tables, which are only available in Microsoft 365 Defender, the rule is automatically moved to Microsoft 365 Defender.</span></span> 

<span data-ttu-id="8bc05-184">Alertes générées par la règle migré :</span><span class="sxs-lookup"><span data-stu-id="8bc05-184">Alerts generated by the migrated rule:</span></span>

- <span data-ttu-id="8bc05-185">Ne sont plus visibles dans le portail Defender pour point de terminaison (Centre de sécurité Microsoft Defender)</span><span class="sxs-lookup"><span data-stu-id="8bc05-185">Are no longer visible in the Defender for Endpoint portal (Microsoft Defender Security Center)</span></span>
- <span data-ttu-id="8bc05-186">Ne plus être remis à votre SIEM ou générer des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8bc05-186">Stop being delivered to your SIEM or generate email notifications.</span></span> <span data-ttu-id="8bc05-187">Pour contourner ce changement, configurez les notifications via Microsoft 365 Defender pour obtenir les alertes.</span><span class="sxs-lookup"><span data-stu-id="8bc05-187">To work around this change, configure notifications through Microsoft 365 Defender to get the alerts.</span></span> <span data-ttu-id="8bc05-188">Vous pouvez utiliser [l’API Microsoft 365 Defender pour](api-incident.md) recevoir des notifications pour les alertes de détection des clients ou les incidents connexes.</span><span class="sxs-lookup"><span data-stu-id="8bc05-188">You can use the [Microsoft 365 Defender API](api-incident.md) to receive notifications for customer detection alerts or related incidents.</span></span>
- <span data-ttu-id="8bc05-189">Ne sera pas supprimé par les règles de suppression des points de terminaison de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8bc05-189">Won't be suppressed by Microsoft Defender for Endpoint suppression rules.</span></span> <span data-ttu-id="8bc05-190">Pour empêcher la générer des alertes pour certains utilisateurs, périphériques ou boîtes aux lettres, modifiez les requêtes correspondantes pour exclure explicitement ces entités.</span><span class="sxs-lookup"><span data-stu-id="8bc05-190">To prevent alerts from being generated for certain users, devices, or mailboxes, modify the corresponding queries to exclude those entities explicitly.</span></span>

<span data-ttu-id="8bc05-191">Si vous modifiez une règle de cette façon, vous serez invité à confirmer avant que de telles modifications ne soient appliquées.</span><span class="sxs-lookup"><span data-stu-id="8bc05-191">If you edit a rule this way, you will be prompted for confirmation before such changes are applied.</span></span>

<span data-ttu-id="8bc05-192">Les nouvelles alertes générées par des règles de détection personnalisées dans Microsoft 365 Portail Defender sont affichées dans une page d’alerte qui fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bc05-192">New alerts generated by custom detection rules in Microsoft 365 Defender portal are displayed in an alert page that provides the following information:</span></span>

- <span data-ttu-id="8bc05-193">Titre et description de l’alerte</span><span class="sxs-lookup"><span data-stu-id="8bc05-193">Alert title and description</span></span> 
- <span data-ttu-id="8bc05-194">Ressources impactées</span><span class="sxs-lookup"><span data-stu-id="8bc05-194">Impacted assets</span></span>
- <span data-ttu-id="8bc05-195">Actions prises en réponse à l’alerte</span><span class="sxs-lookup"><span data-stu-id="8bc05-195">Actions taken in response to the alert</span></span>
- <span data-ttu-id="8bc05-196">Résultats de la requête qui ont déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="8bc05-196">Query results that triggered the alert</span></span> 
- <span data-ttu-id="8bc05-197">Informations sur la règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="8bc05-197">Information on the custom detection rule</span></span> 
 
> [!div class="mx-imgBorder"]
> <span data-ttu-id="8bc05-198">![Image de la nouvelle page d’alerte](../../media/new-alert-page.png)</span><span class="sxs-lookup"><span data-stu-id="8bc05-198">![Image of new alert page](../../media/new-alert-page.png)</span></span>

## <a name="write-queries-without-devicealertevents"></a><span data-ttu-id="8bc05-199">Écrire des requêtes sans DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="8bc05-199">Write queries without DeviceAlertEvents</span></span>

<span data-ttu-id="8bc05-200">Dans le Microsoft 365 Defender, les tableaux et les tableaux sont fournis pour prendre en charge les diverses informations qui accompagnent les alertes provenant de `AlertInfo` `AlertEvidence` différentes sources.</span><span class="sxs-lookup"><span data-stu-id="8bc05-200">In the Microsoft 365 Defender schema, the `AlertInfo` and `AlertEvidence` tables are provided to accommodate the diverse set of information that accompany alerts from various sources.</span></span> 

<span data-ttu-id="8bc05-201">Pour obtenir les mêmes informations d’alerte que vous avez utilisées pour obtenir à partir de la table dans le schéma Microsoft Defender for Endpoint, filtrez la table, puis joignez chaque ID unique à la table, qui fournit des informations détaillées sur l’événement et `DeviceAlertEvents` `AlertInfo` l’entité. `ServiceSource` `AlertEvidence`</span><span class="sxs-lookup"><span data-stu-id="8bc05-201">To get the same alert information that you used to get from the `DeviceAlertEvents` table in the Microsoft Defender for Endpoint schema, filter the `AlertInfo` table by `ServiceSource` and then join each unique ID with the `AlertEvidence` table, which provides detailed event and entity information.</span></span> 

<span data-ttu-id="8bc05-202">Consultez l’exemple de requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="8bc05-202">See the sample query below:</span></span>

```kusto
AlertInfo
| where Timestamp > ago(7d)
| where ServiceSource == "Microsoft Defender for Endpoint"
| join AlertEvidence on AlertId
```

<span data-ttu-id="8bc05-203">Cette requête produit beaucoup plus de colonnes que dans le schéma `DeviceAlertEvents` Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="8bc05-203">This query yields many more columns than `DeviceAlertEvents` in the Microsoft Defender for Endpoint schema.</span></span> <span data-ttu-id="8bc05-204">Pour que les résultats restent gérables, utilisez cette rubrique `project` pour obtenir uniquement les colonnes qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="8bc05-204">To keep results manageable, use `project` to get only the columns you are interested in.</span></span> <span data-ttu-id="8bc05-205">L’exemple ci-dessous projete les colonnes qui peuvent vous intéresser lorsque l’enquête a détecté une activité PowerShell :</span><span class="sxs-lookup"><span data-stu-id="8bc05-205">The example below projects columns you might be interested in when the investigation detected PowerShell activity:</span></span>

```kusto
AlertInfo
| where Timestamp > ago(7d)
| where ServiceSource == "Microsoft Defender for Endpoint"
    and AttackTechniques has "powershell"
| join AlertEvidence on AlertId
| project Timestamp, Title, AlertId, DeviceName, FileName, ProcessCommandLine 
```

<span data-ttu-id="8bc05-206">Si vous souhaitez filtrer des entités spécifiques impliquées dans les alertes, vous pouvez le faire en spécifiant le type d’entité et la valeur que vous souhaitez `EntityType` filtrer.</span><span class="sxs-lookup"><span data-stu-id="8bc05-206">If you'd like to filter for specific entities involved in the alerts, you can do so by specifying the entity type in `EntityType` and the value you would like to filter for.</span></span> <span data-ttu-id="8bc05-207">L’exemple suivant recherche une adresse IP spécifique :</span><span class="sxs-lookup"><span data-stu-id="8bc05-207">The following example looks for a specific IP address:</span></span>

```kusto
AlertInfo
| where Title == "Insert_your_alert_title"
| join AlertEvidence on AlertId 
| where EntityType == "Ip" and RemoteIP == "192.88.99.01" 
```

## <a name="see-also"></a><span data-ttu-id="8bc05-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bc05-208">See also</span></span>
- [<span data-ttu-id="8bc05-209">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8bc05-209">Turn on Microsoft 365 Defender</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8bc05-210">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8bc05-210">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8bc05-211">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8bc05-211">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="8bc05-212">Recherche avancée dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8bc05-212">Advanced hunting in Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)