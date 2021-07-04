---
title: Utilisation du scanneur local de protection contre la perte de données Microsoft 365 (préversion)
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: how-to
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Découvrez comment utiliser le scanneur de protection contre la perte de données Microsoft 365 en local pour analyser les données au repos, puis implémenter des actions de protection pour les partages de fichiers locaux, pour les dossiers locaux et les bibliothèques de documents SharePoint locales.
ms.openlocfilehash: b2512c47b82ab3624d892d349611dd3f1e5aed3c
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289174"
---
# <a name="use-the-microsoft-365-data-loss-prevention-on-premises-scanner-preview"></a><span data-ttu-id="1a39a-103">Utilisation du scanneur local de protection contre la perte de données Microsoft 365 (préversion)</span><span class="sxs-lookup"><span data-stu-id="1a39a-103">Use the Microsoft 365 data loss prevention on-premises scanner (preview)</span></span>

<span data-ttu-id="1a39a-104">Pour vous familiariser avec les fonctionnalités locales DLP et la manière dont elles se trouvent dans les stratégies DLP, nous avons rassemblé certains scénarios que vous pouvez suivre.</span><span class="sxs-lookup"><span data-stu-id="1a39a-104">To help familiarize you with DLP on-premises features and how they surface in DLP policies, we've put together some scenarios for you to follow.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a39a-105">Ces scénarios locaux DLP ne sont pas les procédures officielles de création et de réglage des stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="1a39a-105">These DLP on-premises scenarios are not the official procedures for creating and tuning DLP policies.</span></span> <span data-ttu-id="1a39a-106">Reportez-vous aux rubriques ci-dessous lorsque vous devez utiliser les stratégies DLP dans les situations générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a39a-106">Refer to the below topics when you need to work with DLP policies in general situations:</span></span>
>
> - [<span data-ttu-id="1a39a-107">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="1a39a-107">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
> - [<span data-ttu-id="1a39a-108">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="1a39a-108">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
> - [<span data-ttu-id="1a39a-109">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="1a39a-109">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
> - [<span data-ttu-id="1a39a-110">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-110">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

### <a name="scenario-discover-files-matching-dlp-rules"></a><span data-ttu-id="1a39a-111">Scénario : découvrir les fichiers correspondant aux règles DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-111">Scenario: Discover files matching DLP rules</span></span>

<span data-ttu-id="1a39a-112">Les données du scanneur local DLP apparaissent dans plusieurs zones</span><span class="sxs-lookup"><span data-stu-id="1a39a-112">Data from DLP on-premises scanner surfaces in several areas</span></span>

#### <a name="activity-explorer"></a><span data-ttu-id="1a39a-113">Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="1a39a-113">Activity explorer</span></span>

 <span data-ttu-id="1a39a-114">Microsoft DLP en local détecte les correspondances de règles DLP, puis les signale à [l’Explorateur d’activités](https://compliance.microsoft.com/dataclassification?viewid=activitiesexplorer).</span><span class="sxs-lookup"><span data-stu-id="1a39a-114">Microsoft DLP for on-premises detects DLP rule matches and reports them to [Activity Explorer](https://compliance.microsoft.com/dataclassification?viewid=activitiesexplorer).</span></span>

#### <a name="microsoft-365-audit-log"></a><span data-ttu-id="1a39a-115">Journal d’audit Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1a39a-115">Microsoft 365 Audit log</span></span>

<span data-ttu-id="1a39a-116">Dans la préversion publique, les correspondances de règle DLP sont disponibles dans l’interface utilisateur du journal d’audit. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Rechercher le journal d'audit dans le centre de conformité](search-the-audit-log-in-security-and-compliance.md). Elles sont également accessibles via [Search-UnifiedAuditLog](/powershell/module/exchange/search-unifiedauditlog) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a39a-116">During the public preview the DLP rule matches are available in Audit log UI, see [Search the audit log in the compliance center](search-the-audit-log-in-security-and-compliance.md)  or accessible by [Search-UnifiedAuditLog](/powershell/module/exchange/search-unifiedauditlog) PowerShell.</span></span>

#### <a name="aip"></a><span data-ttu-id="1a39a-117">AIP</span><span class="sxs-lookup"><span data-stu-id="1a39a-117">AIP</span></span>

<span data-ttu-id="1a39a-118">Les données de découverte sont disponibles dans un rapport local au format csv stocké sous :</span><span class="sxs-lookup"><span data-stu-id="1a39a-118">Discovery data is available in a local report in csv format which is stored under:</span></span>

<span data-ttu-id="1a39a-119">**%localappdata%\Microsoft\MSIP\Scanner\Reports\DetailedReport_%timestamp%.csv report**.</span><span class="sxs-lookup"><span data-stu-id="1a39a-119">**%localappdata%\Microsoft\MSIP\Scanner\Reports\DetailedReport_%timestamp%.csv report**.</span></span>

 <span data-ttu-id="1a39a-120">Recherchez les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a39a-120">Look for the following columns:</span></span>

- <span data-ttu-id="1a39a-121">Mode DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-121">DLP Mode</span></span>
- <span data-ttu-id="1a39a-122">État DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-122">DLP Status</span></span>
- <span data-ttu-id="1a39a-123">Commentaire DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-123">DLP Comment</span></span>
- <span data-ttu-id="1a39a-124">Nom de la règle DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-124">DLP Rule Name</span></span>
- <span data-ttu-id="1a39a-125">Actions DLP </span><span class="sxs-lookup"><span data-stu-id="1a39a-125">DLP Actions</span></span>
- <span data-ttu-id="1a39a-126">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="1a39a-126">Owner</span></span>
- <span data-ttu-id="1a39a-127">Autorisations NTFS actuelles (SDDL)</span><span class="sxs-lookup"><span data-stu-id="1a39a-127">Current NTFS Permissions (SDDL)</span></span>
- <span data-ttu-id="1a39a-128">Autorisations NTFS appliquées (SDDL)</span><span class="sxs-lookup"><span data-stu-id="1a39a-128">Applied NTFS Permissions (SDDL)</span></span>
- <span data-ttu-id="1a39a-129">Type d’autorisations NTFS</span><span class="sxs-lookup"><span data-stu-id="1a39a-129">NTFS permissions type</span></span>

### <a name="scenario-enforce-dlp-rule"></a><span data-ttu-id="1a39a-130">Scénario : appliquer une règle DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-130">Scenario: Enforce DLP rule</span></span>

<span data-ttu-id="1a39a-131">Si vous souhaitez appliquer des règles DLP aux fichiers analysés, vous devez activer la mise en application sur le travail d’analyse de contenu dans AIP et au niveau de la stratégie dans DLP.</span><span class="sxs-lookup"><span data-stu-id="1a39a-131">If you want to enforce DLP rules on the scanned files, enforcement must be enabled on both the content scan job in AIP and at the policy level in DLP.</span></span>

#### <a name="configure-dlp-to-enforce-policy-actions"></a><span data-ttu-id="1a39a-132">Configurer DLP pour appliquer les actions de la stratégie</span><span class="sxs-lookup"><span data-stu-id="1a39a-132">Configure DLP to enforce policy actions</span></span>

1. <span data-ttu-id="1a39a-133">Ouvrez la [page Protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies), puis sélectionnez la stratégie DLP ciblée pour les référentiels d’emplacements locaux que vous avez configurés dans AIP.</span><span class="sxs-lookup"><span data-stu-id="1a39a-133">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies) and select the DLP policy that is targeted to the on-premises location repositories you have configured in AIP.</span></span>
2. <span data-ttu-id="1a39a-134">Modifiez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1a39a-134">Edit the policy.</span></span>
3. <span data-ttu-id="1a39a-135">À la page **Test or turn on the policy** (Tester ou activer la stratégie), **Yes, turn it on right away** (Oui, l’activer immédiatement).</span><span class="sxs-lookup"><span data-stu-id="1a39a-135">On the **Test or turn on the policy** page, select **Yes, turn it on right away**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a39a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a39a-136">See also</span></span>

- [<span data-ttu-id="1a39a-137">En savoir plus sur le scanneur local de protection contre la perte de données (préversion)</span><span class="sxs-lookup"><span data-stu-id="1a39a-137">Learn about DLP on-premises scanner (preview)</span></span>](dlp-on-premises-scanner-learn.md)
- [<span data-ttu-id="1a39a-138">Prise en main du scanner local de protection contre la perte de données (préversion)</span><span class="sxs-lookup"><span data-stu-id="1a39a-138">Get started with  DLP on-premises scanner (preview)</span></span>](dlp-on-premises-scanner-get-started.md)
- [<span data-ttu-id="1a39a-139">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="1a39a-139">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="1a39a-140">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="1a39a-140">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="1a39a-141">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="1a39a-141">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
