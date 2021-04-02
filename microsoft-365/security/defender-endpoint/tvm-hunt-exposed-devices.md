---
title: Repérer des appareils exposés
description: Découvrez comment la gestion des menaces et des vulnérabilités peut être utilisée pour aider les administrateurs de sécurité, les administrateurs informatiques et SecOps à collaborer.
keywords: scénarios mdatp-tvm, mdatp, tvm, tvm scenarios, réduire l’exposition aux vulnérabilités de & de menace, réduire les menaces et vulnérabilités, améliorer la configuration de la sécurité, augmenter le Degré de sécurisation Microsoft pour les appareils, augmenter le niveau de sécurité microsoft & vulnérabilité Microsoft Secure Score pour les appareils, Degré de sécurisation Microsoft pour les appareils, score d’exposition, contrôles de sécurité
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: b8e3a80e73d9847837ae0a1542e7d16ee8ae0f29
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500090"
---
# <a name="hunt-for-exposed-devices---threat-and-vulnerability-management"></a><span data-ttu-id="59291-104">Recherche des appareils exposés : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="59291-104">Hunt for exposed devices - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="59291-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="59291-105">**Applies to:**</span></span>

- [<span data-ttu-id="59291-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="59291-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="59291-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="59291-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="59291-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="59291-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="59291-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="59291-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="59291-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="59291-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

## <a name="use-advanced-hunting-to-find-devices-with-vulnerabilities"></a><span data-ttu-id="59291-111">Utiliser le recherche avancée pour rechercher des appareils avec des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="59291-111">Use advanced hunting to find devices with vulnerabilities</span></span>

<span data-ttu-id="59291-112">Le repérage avancé est un outil de repérage de menaces basé sur des requêtes qui vous permet d’explorer jusqu’à 30 jours de données brutes.</span><span class="sxs-lookup"><span data-stu-id="59291-112">Advanced hunting is a query-based threat-hunting tool that lets you explore up to 30 days of raw data.</span></span> <span data-ttu-id="59291-113">Vous pouvez inspecter de manière proactive les événements de votre réseau pour localiser les indicateurs et entités de menace.</span><span class="sxs-lookup"><span data-stu-id="59291-113">You can proactively inspect events in your network to locate threat indicators and entities.</span></span> <span data-ttu-id="59291-114">L’accès flexible aux données permet un recherche sans contraintes pour les menaces connues et potentielles.</span><span class="sxs-lookup"><span data-stu-id="59291-114">The flexible access to data enables unconstrained hunting for both known and potential threats.</span></span> [<span data-ttu-id="59291-115">En savoir plus sur le chasse avancée</span><span class="sxs-lookup"><span data-stu-id="59291-115">Learn more about advanced hunting</span></span>](advanced-hunting-overview.md)

### <a name="schema-tables"></a><span data-ttu-id="59291-116">Tableaux de schéma</span><span class="sxs-lookup"><span data-stu-id="59291-116">Schema tables</span></span>

- <span data-ttu-id="59291-117">[DeviceTvmSoftwareInventory](advanced-hunting-devicetvmsoftwareinventory-table.md) : inventaire des logiciels installés sur les appareils, y compris les informations de version et l’état de fin de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59291-117">[DeviceTvmSoftwareInventory](advanced-hunting-devicetvmsoftwareinventory-table.md) - Inventory of software installed on devices, including their version information and end-of-support status.</span></span>

- <span data-ttu-id="59291-118">[DeviceTvmSoftwareVulnerabilities](advanced-hunting-devicetvmsoftwarevulnerabilities-table.md) : vulnérabilités logicielles trouvées sur les appareils et liste des mises à jour de sécurité disponibles qui s’adressent à chaque vulnérabilité.</span><span class="sxs-lookup"><span data-stu-id="59291-118">[DeviceTvmSoftwareVulnerabilities](advanced-hunting-devicetvmsoftwarevulnerabilities-table.md) - Software vulnerabilities found on devices and the list of available security updates that address each vulnerability.</span></span>

- <span data-ttu-id="59291-119">[DeviceTvmSoftwareVulnerabilitiesKB](advanced-hunting-devicetvmsoftwarevulnerabilitieskb-table.md) : base de connaissances sur les vulnérabilités divulguées publiquement, notamment si le code d’exploitation est disponible publiquement.</span><span class="sxs-lookup"><span data-stu-id="59291-119">[DeviceTvmSoftwareVulnerabilitiesKB](advanced-hunting-devicetvmsoftwarevulnerabilitieskb-table.md) - Knowledge base of publicly disclosed vulnerabilities, including whether exploit code is publicly available.</span></span>

- <span data-ttu-id="59291-120">[DeviceTvmSecureConfigurationAssessment](advanced-hunting-devicetvmsecureconfigurationassessment-table.md) : événements d’évaluation de la gestion des menaces et des vulnérabilités, indiquant l’état de différentes configurations de sécurité sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="59291-120">[DeviceTvmSecureConfigurationAssessment](advanced-hunting-devicetvmsecureconfigurationassessment-table.md) - Threat and vulnerability management assessment events, indicating the status of various security configurations on devices.</span></span>

- <span data-ttu-id="59291-121">[DeviceTvmSecureConfigurationAssessmentKB](advanced-hunting-devicetvmsecureconfigurationassessmentkb-table.md) : base de connaissances sur les différentes configurations de sécurité utilisées par la gestion des menaces & des vulnérabilités pour évaluer les appareils ; inclut des mappages à différentes normes et critères</span><span class="sxs-lookup"><span data-stu-id="59291-121">[DeviceTvmSecureConfigurationAssessmentKB](advanced-hunting-devicetvmsecureconfigurationassessmentkb-table.md) - Knowledge base of various security configurations used by Threat & Vulnerability Management to assess devices; includes mappings to various standards and benchmarks</span></span>

## <a name="check-which-devices-are-involved-in-high-severity-alerts"></a><span data-ttu-id="59291-122">Vérifier les appareils impliqués dans les alertes de gravité élevée</span><span class="sxs-lookup"><span data-stu-id="59291-122">Check which devices are involved in high severity alerts</span></span>

1. <span data-ttu-id="59291-123">Go to **Advanced hunting** from the left-hand navigation pane of the Microsoft Defender Security Center.</span><span class="sxs-lookup"><span data-stu-id="59291-123">Go to **Advanced hunting** from the left-hand navigation pane of the Microsoft Defender Security Center.</span></span>

2. <span data-ttu-id="59291-124">Faites défiler vers le bas jusqu’aux schémas de recherche avancée TVM pour vous familiariser avec les noms des colonnes.</span><span class="sxs-lookup"><span data-stu-id="59291-124">Scroll down to the TVM advanced hunting schemas to familiarize yourself with the column names.</span></span>

3. <span data-ttu-id="59291-125">Entrez les requêtes suivantes :</span><span class="sxs-lookup"><span data-stu-id="59291-125">Enter the following queries:</span></span>

```kusto
// Search for devices with High active alerts or Critical CVE public exploit
DeviceTvmSoftwareVulnerabilities
| join kind=inner(DeviceTvmSoftwareVulnerabilitiesKB) on CveId
| where IsExploitAvailable == 1 and CvssScore >= 7
| summarize NumOfVulnerabilities=dcount(CveId),
DeviceName=any(DeviceName) by DeviceId
| join kind =inner(DeviceAlertEvents) on DeviceId  
| summarize NumOfVulnerabilities=any(NumOfVulnerabilities),
DeviceName=any(DeviceName) by DeviceId, AlertId
| project DeviceName, NumOfVulnerabilities, AlertId  
| order by NumOfVulnerabilities desc
```

## <a name="related-topics"></a><span data-ttu-id="59291-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59291-126">Related topics</span></span>

- [<span data-ttu-id="59291-127">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="59291-127">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="59291-128">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="59291-128">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="59291-129">API</span><span class="sxs-lookup"><span data-stu-id="59291-129">APIs</span></span>](next-gen-threat-and-vuln-mgt.md#apis)
- [<span data-ttu-id="59291-130">Configurer l’accès aux données pour les rôles de gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="59291-130">Configure data access for threat and vulnerability management roles</span></span>](user-roles.md#create-roles-and-assign-the-role-to-an-azure-active-directory-group)
- [<span data-ttu-id="59291-131">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="59291-131">Advanced hunting overview</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)
- [<span data-ttu-id="59291-132">Toutes les tables de recherche avancées</span><span class="sxs-lookup"><span data-stu-id="59291-132">All advanced hunting tables</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference.md)
