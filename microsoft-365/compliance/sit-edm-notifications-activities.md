---
title: Créer des notifications pour les activités de correspondance de données exactes
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
ms.openlocfilehash: 263dc319d7e7d3ee5f12ebe374e8f5bd44c4cc8c
ms.sourcegitcommit: 5db5047c24b56f3af90c2bc5c830a7a13eeeccad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53341675"
---
# <a name="create-notifications-for-exact-data-match-activities"></a><span data-ttu-id="a034d-103">Créer des notifications pour les activités de correspondance de données exactes</span><span class="sxs-lookup"><span data-stu-id="a034d-103">Create notifications for exact data match activities</span></span>

<span data-ttu-id="a034d-104">Lorsque vous [Créer des types d’informations sensibles personnalisés à l’aide de la correspondance de données exacte (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) le [journal d’audit](search-the-audit-log-in-security-and-compliance.md#before-you-search-the-audit-log)crée un certain nombre d'activités.</span><span class="sxs-lookup"><span data-stu-id="a034d-104">When you [create custom sensitive information types with exact data match (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) there are a number of activities that are created in the [audit log](search-the-audit-log-in-security-and-compliance.md#before-you-search-the-audit-log).</span></span> <span data-ttu-id="a034d-105">Vous pouvez utiliser la cmdlet PowerShell [New-ProtectionAlert](/powershell/module/exchange/new-protectionalert) pour créer des notifications qui vous avertiront de l’événement :</span><span class="sxs-lookup"><span data-stu-id="a034d-105">You can use the [New-ProtectionAlert](/powershell/module/exchange/new-protectionalert) PowerShell cmdlet to create notifications that let you know when these activities occur:</span></span>

- <span data-ttu-id="a034d-106">CreateSchema</span><span class="sxs-lookup"><span data-stu-id="a034d-106">CreateSchema</span></span>
- <span data-ttu-id="a034d-107">EditSchema</span><span class="sxs-lookup"><span data-stu-id="a034d-107">EditSchema</span></span>
- <span data-ttu-id="a034d-108">RemoveSchema</span><span class="sxs-lookup"><span data-stu-id="a034d-108">RemoveSchema</span></span>
- <span data-ttu-id="a034d-109">UploadDataFailed</span><span class="sxs-lookup"><span data-stu-id="a034d-109">UploadDataFailed</span></span>
- <span data-ttu-id="a034d-110">UploadDataCompleted</span><span class="sxs-lookup"><span data-stu-id="a034d-110">UploadDataCompleted</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="a034d-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="a034d-111">Pre-requisites</span></span>

<span data-ttu-id="a034d-112">Le compte que vous utilisez doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="a034d-112">The account you use must be one of the following:</span></span>

- <span data-ttu-id="a034d-113">un administrateur général</span><span class="sxs-lookup"><span data-stu-id="a034d-113">a global admin</span></span>
- <span data-ttu-id="a034d-114">administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="a034d-114">compliance administrator</span></span>
- <span data-ttu-id="a034d-115">Administrateur Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a034d-115">Exchange Online administrator</span></span>

<span data-ttu-id="a034d-116">Pour en avoir plus sur les autorisations DLP, consultez la section[Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="a034d-116">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

<span data-ttu-id="a034d-117">La classification basée sur EDM est incluse dans les abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="a034d-117">EDM-based classification is included in these subscriptions:</span></span>

- <span data-ttu-id="a034d-118">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="a034d-118">Office 365 E5</span></span>
- <span data-ttu-id="a034d-119">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="a034d-119">Microsoft 365 E5</span></span>
- <span data-ttu-id="a034d-120">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="a034d-120">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="a034d-121">Microsoft E5/A5 Information Protection et gouvernance</span><span class="sxs-lookup"><span data-stu-id="a034d-121">Microsoft E5/A5 Information Protection and Governance</span></span>

<span data-ttu-id="a034d-122">Si vous souhaitez en savoir plus les licences DLP, consultez la rubrique [Instructions relatives aux licences Microsoft 365 pour la sécurité et la conformité](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span><span class="sxs-lookup"><span data-stu-id="a034d-122">To learn more about DLP licensing, see [Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span></span>

## <a name="configure-notifications-for-edm-activities"></a><span data-ttu-id="a034d-123">Configurer les notifications pour les activités EDM</span><span class="sxs-lookup"><span data-stu-id="a034d-123">Configure notifications for EDM activities</span></span>

1. <span data-ttu-id="a034d-124">Se connecter à l’interface [PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="a034d-124">Connect to the [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="a034d-125">Exécutez l’applet de commande `New-ProtectionAlert` à l’aide de l’activité pour laquelle vous souhaitez créer la notification.</span><span class="sxs-lookup"><span data-stu-id="a034d-125">Run the `New-ProtectionAlert` cmdlet using the activity that you want to create the notification for.</span></span>  <span data-ttu-id="a034d-126">Par exemple, si vous souhaitez être averti de l'exécution de l'action **UploadDataCompleted**, exécutez :</span><span class="sxs-lookup"><span data-stu-id="a034d-126">For example, if you want to be notified when the **UploadDataCompleted** action occurred, run:</span></span>

    ```powershell
    New-ProtectionAlert -Name "EdmUploadCompleteAlertPolicy" -Category Others -NotifyUser <address to send notification to> -ThreatType Activity -Operation UploadDataCompleted -Description "Custom alert policy to track when EDM upload Completed" -AggregationType None
    ```
    
    <span data-ttu-id="a034d-127">pour l’action **UploadDataFailed** vous pouvez exécuter :</span><span class="sxs-lookup"><span data-stu-id="a034d-127">for the **UploadDataFailed** you can run:</span></span>
    
    ```powershell
    New-ProtectionAlert -Name "EdmUploadFailAlertPolicy" -Category Others -NotifyUser <SMTP address to send notification to> -ThreatType Activity -Operation UploadDataFailed -Description "Custom alert policy to track when EDM upload Failed" -AggregationType None -Severity High
    ```

## <a name="related-articles"></a><span data-ttu-id="a034d-128">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a034d-128">Related articles</span></span>

- [<span data-ttu-id="a034d-129">Créer des types d’informations sensibles personnalisés à l’aide de la correspondance de données exacte (EDM)</span><span class="sxs-lookup"><span data-stu-id="a034d-129">Create custom sensitive information types with exact data match (EDM)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)
- [<span data-ttu-id="a034d-130">New-ProtectionAlert</span><span class="sxs-lookup"><span data-stu-id="a034d-130">New-ProtectionAlert</span></span>](/powershell/module/exchange/new-protectionalert)