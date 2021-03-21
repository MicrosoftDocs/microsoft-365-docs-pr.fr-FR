---
title: Créer des notifications pour les activités de correspondance de données exactes (aperçu)
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: En savoir plus sur la création des notifications pour les activités de correspondance de données exactes.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 2e2f67ef0f276211483519bd5e246e4e041b2b15
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919360"
---
# <a name="create-notifications-for-exact-data-match-activities-preview"></a><span data-ttu-id="c2611-103">Créer des notifications pour les activités de correspondance de données exactes (aperçu)</span><span class="sxs-lookup"><span data-stu-id="c2611-103">Create notifications for exact data match activities (preview)</span></span>

<span data-ttu-id="c2611-104">Lorsque vous [Créer des types d’informations sensibles personnalisés à l’aide de la correspondance de données exacte (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) le [journal d’audit](search-the-audit-log-in-security-and-compliance.md#requirements-to-search-the-audit-log)crée un certain nombre d'activités.</span><span class="sxs-lookup"><span data-stu-id="c2611-104">When you [create custom sensitive information types with exact data match (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) there are a number of activities that are created in the [audit log](search-the-audit-log-in-security-and-compliance.md#requirements-to-search-the-audit-log).</span></span> <span data-ttu-id="c2611-105">Vous pouvez utiliser la cmdlet PowerShell [New-ProtectionAlert](/powershell/module/exchange/new-protectionalert?view=exchange-ps) pour créer des notifications qui vous avertiront de l’événement :</span><span class="sxs-lookup"><span data-stu-id="c2611-105">You can use the [New-ProtectionAlert](/powershell/module/exchange/new-protectionalert?view=exchange-ps) PowerShell cmdlet to create notifications that let you know when these activities occur:</span></span>

- <span data-ttu-id="c2611-106">CreateSchema</span><span class="sxs-lookup"><span data-stu-id="c2611-106">CreateSchema</span></span>
- <span data-ttu-id="c2611-107">EditSchema</span><span class="sxs-lookup"><span data-stu-id="c2611-107">EditSchema</span></span>
- <span data-ttu-id="c2611-108">RemoveSchema</span><span class="sxs-lookup"><span data-stu-id="c2611-108">RemoveSchema</span></span>
- <span data-ttu-id="c2611-109">UploadDataFailed</span><span class="sxs-lookup"><span data-stu-id="c2611-109">UploadDataFailed</span></span>
- <span data-ttu-id="c2611-110">UploadDataCompleted</span><span class="sxs-lookup"><span data-stu-id="c2611-110">UploadDataCompleted</span></span>

> [!NOTE]
> <span data-ttu-id="c2611-111">La possibilité de créer des notifications pour les activités de EDM n'est disponible que pour les clouds mondiaux et cloud de la communauté du secteur public.</span><span class="sxs-lookup"><span data-stu-id="c2611-111">The ability to create notifications for EDM activities is only available for the World Wide and GCC clouds only.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="c2611-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c2611-112">Pre-requisites</span></span>

<span data-ttu-id="c2611-113">Le compte que vous utilisez doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="c2611-113">The account you use must be one of the following:</span></span>

- <span data-ttu-id="c2611-114">un administrateur général</span><span class="sxs-lookup"><span data-stu-id="c2611-114">a global admin</span></span>
- <span data-ttu-id="c2611-115">administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="c2611-115">compliance administrator</span></span>
- <span data-ttu-id="c2611-116">Administrateur Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c2611-116">Exchange Online administrator</span></span>

<span data-ttu-id="c2611-117">Pour en avoir plus sur les autorisations DLP, consultez la section[Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="c2611-117">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

<span data-ttu-id="c2611-118">La classification EDM est incluse dans ces abonnements</span><span class="sxs-lookup"><span data-stu-id="c2611-118">EDM-based classification is included in these subscriptions</span></span>

- <span data-ttu-id="c2611-119">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="c2611-119">Office 365 E5</span></span>
- <span data-ttu-id="c2611-120">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="c2611-120">Microsoft 365 E5</span></span>
- <span data-ttu-id="c2611-121">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="c2611-121">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="c2611-122">Microsoft E5/A5 Information Protection et gouvernance</span><span class="sxs-lookup"><span data-stu-id="c2611-122">Microsoft E5/A5 Information Protection and Governance</span></span>

<span data-ttu-id="c2611-123">Si vous souhaitez en savoir plus les licences DLP, consultez la rubrique [Instructions relatives aux licences Microsoft 365 pour la sécurité et la conformité](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span><span class="sxs-lookup"><span data-stu-id="c2611-123">To learn more about DLP licensing, see [Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)</span></span>

## <a name="configure-notifications-for-edm-activities"></a><span data-ttu-id="c2611-124">Configurer les notifications pour les activités EDM</span><span class="sxs-lookup"><span data-stu-id="c2611-124">Configure notifications for EDM activities</span></span>

1. <span data-ttu-id="c2611-125">Se connecter à l’interface [PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="c2611-125">Connect to the [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell?view=exchange-ps)</span></span> 

2. <span data-ttu-id="c2611-126">Exécutez la cmdlet `New-ProtectionAlert` à l’aide de l’activité pour laquelle vous souhaitez créer la notification.</span><span class="sxs-lookup"><span data-stu-id="c2611-126">Run the `New-ProtectionAlert` cmdlet using the activity that you want to create the notification for.</span></span>  <span data-ttu-id="c2611-127">Par exemple, si vous souhaitez être averti de l'exécution de l'action **UploadDataCompleted**, exécutez</span><span class="sxs-lookup"><span data-stu-id="c2611-127">For example, if you want to be notified when the **UploadDataCompleted** action occured, run</span></span>

```powershell
New-ProtectionAlert -Name "EdmUploadCompleteAlertPolicy" -Category Others -NotifyUser <***address to send  notification to***> -ThreatType Activity -Operation UploadDataCompleted -Description "Custom alert policy to track when EDM upload Completed" -AggregationType None
```

<span data-ttu-id="c2611-128">pour l’action **UploadDataFailed** vous pouvez exécuter</span><span class="sxs-lookup"><span data-stu-id="c2611-128">for the **UploadDataFailed** you can run</span></span>

```powershell
New-ProtectionAlert -Name "EdmUploadFailAlertPolicy" -Category Others -NotifyUser <***SMTP address to send notification to***> -ThreatType Activity -Operation UploadDataFailed -Description "Custom alert policy to track when EDM upload Failed" -AggregationType None -Severity High
```

## <a name="related-articles"></a><span data-ttu-id="c2611-129">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="c2611-129">Related articles</span></span>

- [<span data-ttu-id="c2611-130">Créer des types d’informations sensibles personnalisés à l’aide de la correspondance de données exacte (EDM)</span><span class="sxs-lookup"><span data-stu-id="c2611-130">Create custom sensitive information types with exact data match (EDM)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)
- [<span data-ttu-id="c2611-131">New-ProtectionAlert</span><span class="sxs-lookup"><span data-stu-id="c2611-131">New-ProtectionAlert</span></span>](/powershell/module/exchange/new-protectionalert?view=exchange-ps)