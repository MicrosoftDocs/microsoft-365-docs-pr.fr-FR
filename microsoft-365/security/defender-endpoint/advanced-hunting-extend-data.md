---
title: Étendre la couverture de recherche avancée avec les bons paramètres
description: Vérifier les paramètres d’audit sur les appareils Windows et d’autres paramètres pour vous assurer que vous obtenez les données les plus complètes dans le cadre d’un recherche avancée
keywords: advanced hunting, incident, pivot, entity, audit settings, user account management, security group management, threat hunting, cyber threat hunting, search, query, telemetry, mdatp, Microsoft Defender ATP, Microsoft Defender for Endpoint, Windows Defender, Windows Defender ATP, Windows Defender Advanced Threat Protection
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 10/10/2020
ms.technology: mde
ms.openlocfilehash: 60e8710415e328d06fac4c02e428094e5e4bcc92
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067462"
---
# <a name="extend-advanced-hunting-coverage-with-the-right-settings"></a><span data-ttu-id="760d0-104">Étendre la couverture de recherche avancée avec les bons paramètres</span><span class="sxs-lookup"><span data-stu-id="760d0-104">Extend advanced hunting coverage with the right settings</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="760d0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="760d0-105">**Applies to:**</span></span>
- [<span data-ttu-id="760d0-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="760d0-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

<span data-ttu-id="760d0-107">[La recherche avancée](advanced-hunting-overview.md) repose sur des données provenant de l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="760d0-107">[Advanced hunting](advanced-hunting-overview.md) relies on data coming from across your organization.</span></span> <span data-ttu-id="760d0-108">Pour obtenir les données les plus complètes possibles, assurez-vous que vous avez les paramètres corrects dans les sources de données correspondantes.</span><span class="sxs-lookup"><span data-stu-id="760d0-108">To get the most comprehensive data possible, ensure that you have the correct settings in the corresponding data sources.</span></span>

## <a name="advanced-security-auditing-on-windows-devices"></a><span data-ttu-id="760d0-109">Audit de sécurité avancée sur les appareils Windows</span><span class="sxs-lookup"><span data-stu-id="760d0-109">Advanced security auditing on Windows devices</span></span>

<span data-ttu-id="760d0-110">Activer ces paramètres d’audit avancés pour vous assurer que vous obtenez des données sur les activités sur vos appareils, notamment la gestion des comptes local, la gestion des groupes de sécurité locaux et la création de services.</span><span class="sxs-lookup"><span data-stu-id="760d0-110">Turn on these advanced auditing settings to ensure you get data about activities on your devices, including local account management, local security group management, and service creation.</span></span>

<span data-ttu-id="760d0-111">Data</span><span class="sxs-lookup"><span data-stu-id="760d0-111">Data</span></span> | <span data-ttu-id="760d0-112">Description</span><span class="sxs-lookup"><span data-stu-id="760d0-112">Description</span></span> | <span data-ttu-id="760d0-113">Table schema</span><span class="sxs-lookup"><span data-stu-id="760d0-113">Schema table</span></span> | <span data-ttu-id="760d0-114">Procédure de configuration</span><span class="sxs-lookup"><span data-stu-id="760d0-114">How to configure</span></span>
-|-|-|-
<span data-ttu-id="760d0-115">Gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="760d0-115">Account management</span></span> | <span data-ttu-id="760d0-116">Événements capturés en tant que différentes valeurs indiquant la création, la suppression et d’autres activités liées `ActionType` au compte</span><span class="sxs-lookup"><span data-stu-id="760d0-116">Events captured as various `ActionType` values indicating local account creation, deletion, and other account-related activities</span></span> | [<span data-ttu-id="760d0-117">DeviceEvents</span><span class="sxs-lookup"><span data-stu-id="760d0-117">DeviceEvents</span></span>](advanced-hunting-deviceevents-table.md) | <span data-ttu-id="760d0-118">- Déployer une stratégie d’audit de sécurité avancée : [auditer la gestion des comptes d’utilisateurs](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-user-account-management)</span><span class="sxs-lookup"><span data-stu-id="760d0-118">- Deploy an advanced security audit policy: [Audit User Account Management](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-user-account-management)</span></span><br> <span data-ttu-id="760d0-119">- [En savoir plus sur les stratégies d’audit de sécurité avancées](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span><span class="sxs-lookup"><span data-stu-id="760d0-119">- [Learn about advanced security audit policies](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span></span>
<span data-ttu-id="760d0-120">Gestion des groupes de sécurité</span><span class="sxs-lookup"><span data-stu-id="760d0-120">Security group management</span></span> | <span data-ttu-id="760d0-121">Événements capturés en tant que différentes valeurs indiquant la création d’un groupe de `ActionType` sécurité local et d’autres activités de gestion des groupes locaux</span><span class="sxs-lookup"><span data-stu-id="760d0-121">Events captured as various `ActionType` values indicating local security group creation and other local group management activities</span></span> | [<span data-ttu-id="760d0-122">DeviceEvents</span><span class="sxs-lookup"><span data-stu-id="760d0-122">DeviceEvents</span></span>](advanced-hunting-deviceevents-table.md) | <span data-ttu-id="760d0-123">- Déployer une stratégie d’audit de sécurité avancée : [auditer la gestion des groupes de sécurité](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-security-group-management)</span><span class="sxs-lookup"><span data-stu-id="760d0-123">- Deploy an advanced security audit policy: [Audit Security Group Management](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-security-group-management)</span></span><br> <span data-ttu-id="760d0-124">- [En savoir plus sur les stratégies d’audit de sécurité avancées](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span><span class="sxs-lookup"><span data-stu-id="760d0-124">- [Learn about advanced security audit policies](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span></span>
<span data-ttu-id="760d0-125">Installation du service</span><span class="sxs-lookup"><span data-stu-id="760d0-125">Service installation</span></span> | <span data-ttu-id="760d0-126">Événements capturés `ActionType` avec la valeur , indiquant `ServiceInstalled` qu’un service a été créé</span><span class="sxs-lookup"><span data-stu-id="760d0-126">Events captured with the `ActionType` value `ServiceInstalled`, indicating that a service has been created</span></span> | [<span data-ttu-id="760d0-127">DeviceEvents</span><span class="sxs-lookup"><span data-stu-id="760d0-127">DeviceEvents</span></span>](advanced-hunting-deviceevents-table.md) | <span data-ttu-id="760d0-128">- Déployer une stratégie d’audit de sécurité avancée : [auditer l’extension du système de sécurité](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-security-system-extension)</span><span class="sxs-lookup"><span data-stu-id="760d0-128">- Deploy an advanced security audit policy: [Audit Security System Extension](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-security-system-extension)</span></span><br> <span data-ttu-id="760d0-129">- [En savoir plus sur les stratégies d’audit de sécurité avancées](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span><span class="sxs-lookup"><span data-stu-id="760d0-129">- [Learn about advanced security audit policies](https://docs.microsoft.com/windows/security/threat-protection/auditing/advanced-security-auditing)</span></span>

## <a name="related-topics"></a><span data-ttu-id="760d0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="760d0-130">Related topics</span></span>

- [<span data-ttu-id="760d0-131">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="760d0-131">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="760d0-132">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="760d0-132">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="760d0-133">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="760d0-133">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="760d0-134">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="760d0-134">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="760d0-135">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="760d0-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="760d0-136">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="760d0-136">Custom detections overview</span></span>](overview-custom-detections.md)
