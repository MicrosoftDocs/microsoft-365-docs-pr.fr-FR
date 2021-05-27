---
title: Utiliser les étiquettes de confidentialité comme condition dans les stratégies de protection contre la perte de données
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MET150
ms.custom:
- seo-marvel-apr2020
description: en savoir plus sur les types de services et d’éléments dont vous pouvez utiliser les étiquettes de confidentialité comme conditions dans les stratégies DLP
ms.openlocfilehash: b33e6704a3311740c1e386f77f1c751382ee6958
ms.sourcegitcommit: 07e536f1a6e335f114da55048844e4a866fe731b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "52651091"
---
# <a name="use-sensitivity-labels-as-conditions-in-dlp-policies"></a><span data-ttu-id="a34c6-103">Utiliser les étiquettes de confidentialité comme condition dans les stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="a34c6-103">Use sensitivity labels as conditions in DLP policies</span></span>

<span data-ttu-id="a34c6-104">Vous pouvez utiliser [ les étiquettes de confidentialité](sensitivity-labels.md)comme condition dans les stratégies de protection contre la perte de données pour cet emplacement:</span><span class="sxs-lookup"><span data-stu-id="a34c6-104">You can use [sensitivity labels](sensitivity-labels.md) as a condition in DLP policies for these location:</span></span>

- <span data-ttu-id="a34c6-105">Messagerie Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a34c6-105">Exchange Online email messages</span></span>
- <span data-ttu-id="a34c6-106">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a34c6-106">SharePoint Online</span></span>
- <span data-ttu-id="a34c6-107">Sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="a34c6-107">OneDrive for Business sites</span></span>
- <span data-ttu-id="a34c6-108">Appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="a34c6-108">Windows 10 devices</span></span>

<span data-ttu-id="a34c6-109">Les étiquettes de confidentialité apparaissent comme une option dans la liste du **Contenu**.</span><span class="sxs-lookup"><span data-stu-id="a34c6-109">Sensitivity labels appear as an option in the **Content contains** list.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="a34c6-110">![étiquette de confidentialité comme condition](../media/dlp-sensitivity-label-as-a-condition.png)</span><span class="sxs-lookup"><span data-stu-id="a34c6-110">![sensitivity label as a condition](../media/dlp-sensitivity-label-as-a-condition.png)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a34c6-111">**Les Etiquettes de Confidentialité** comme condition ne seront pas disponibles si vous avez sélectionné **Conversation d’équipe et messages de canaux** comme emplacement d’application de la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="a34c6-111">**Sensitivity Labels** as a condition will not be available if you have selected **Teams chat and channel messages** as a location to apply the DLP policy.</span></span>


## <a name="supported-items-scenarios-and-policy-tips"></a><span data-ttu-id="a34c6-112">Éléments, scénarios et conseils de stratégie pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-112">Supported items, scenarios, and policy tips</span></span>

<span data-ttu-id="a34c6-113">Vous pouvez utiliser des étiquettes de confidentialité comme conditions sur ces éléments et dans ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="a34c6-113">You can use sensitivity labels as conditions on these items and in these scenarios.</span></span>

### <a name="supported-items"></a><span data-ttu-id="a34c6-114">Éléments non pris en charge </span><span class="sxs-lookup"><span data-stu-id="a34c6-114">Supported items</span></span>

|<span data-ttu-id="a34c6-115">Service</span><span class="sxs-lookup"><span data-stu-id="a34c6-115">Service</span></span>  |<span data-ttu-id="a34c6-116">Type d’élément</span><span class="sxs-lookup"><span data-stu-id="a34c6-116">Item type</span></span>  |<span data-ttu-id="a34c6-117">Disponible pour l’astuce de stratégie</span><span class="sxs-lookup"><span data-stu-id="a34c6-117">Available to policy tip</span></span>  |<span data-ttu-id="a34c6-118">Applicable</span><span class="sxs-lookup"><span data-stu-id="a34c6-118">Enforceable</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="a34c6-119">Exchange</span><span class="sxs-lookup"><span data-stu-id="a34c6-119">Exchange</span></span>    |<span data-ttu-id="a34c6-120">Message électronique</span><span class="sxs-lookup"><span data-stu-id="a34c6-120">email message</span></span>         |<span data-ttu-id="a34c6-121">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-121">yes</span></span>         |<span data-ttu-id="a34c6-122">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-122">yes</span></span>         |
|<span data-ttu-id="a34c6-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="a34c6-123">Exchange</span></span>    |<span data-ttu-id="a34c6-124">Pièce jointe</span><span class="sxs-lookup"><span data-stu-id="a34c6-124">email attachment</span></span>         |<span data-ttu-id="a34c6-125">non</span><span class="sxs-lookup"><span data-stu-id="a34c6-125">no</span></span>         |<span data-ttu-id="a34c6-126">oui \*\*</span><span class="sxs-lookup"><span data-stu-id="a34c6-126">yes \*</span></span>         |
|<span data-ttu-id="a34c6-127">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a34c6-127">SharePoint Online</span></span>     |<span data-ttu-id="a34c6-128">éléments dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a34c6-128">items in SharePoint Online</span></span>         |<span data-ttu-id="a34c6-129">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-129">yes</span></span>         |<span data-ttu-id="a34c6-130">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-130">yes</span></span>         |
|<span data-ttu-id="a34c6-131">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="a34c6-131">OneDrive for Business</span></span>     |<span data-ttu-id="a34c6-132">éléments</span><span class="sxs-lookup"><span data-stu-id="a34c6-132">items</span></span>         |<span data-ttu-id="a34c6-133">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-133">yes</span></span>         |<span data-ttu-id="a34c6-134">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-134">yes</span></span>         |
|<span data-ttu-id="a34c6-135">Teams</span><span class="sxs-lookup"><span data-stu-id="a34c6-135">Teams</span></span>     |<span data-ttu-id="a34c6-136">Teams et messages de canal</span><span class="sxs-lookup"><span data-stu-id="a34c6-136">Teams and channel messages</span></span>         |<span data-ttu-id="a34c6-137">non applicable</span><span class="sxs-lookup"><span data-stu-id="a34c6-137">not applicable</span></span>         |<span data-ttu-id="a34c6-138">non applicable</span><span class="sxs-lookup"><span data-stu-id="a34c6-138">not applicable</span></span>         |
|<span data-ttu-id="a34c6-139">Teams</span><span class="sxs-lookup"><span data-stu-id="a34c6-139">Teams</span></span>     |<span data-ttu-id="a34c6-140">pièces jointes</span><span class="sxs-lookup"><span data-stu-id="a34c6-140">attachments</span></span>         |<span data-ttu-id="a34c6-141">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="a34c6-141">yes \*\*</span></span>         |<span data-ttu-id="a34c6-142">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="a34c6-142">yes \*\*</span></span>         |
|<span data-ttu-id="a34c6-143">Appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="a34c6-143">Windows 10 devices</span></span>     |<span data-ttu-id="a34c6-144">éléments</span><span class="sxs-lookup"><span data-stu-id="a34c6-144">items</span></span>         |<span data-ttu-id="a34c6-145">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-145">yes</span></span>         |<span data-ttu-id="a34c6-146">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-146">yes</span></span>         |
|<span data-ttu-id="a34c6-147">MCAS (préversion)</span><span class="sxs-lookup"><span data-stu-id="a34c6-147">MCAS (preview)</span></span> |<span data-ttu-id="a34c6-148">éléments</span><span class="sxs-lookup"><span data-stu-id="a34c6-148">items</span></span>         |<span data-ttu-id="a34c6-149">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-149">yes</span></span>         |<span data-ttu-id="a34c6-150">oui</span><span class="sxs-lookup"><span data-stu-id="a34c6-150">yes</span></span>         |

<span data-ttu-id="a34c6-151">\* La détection DLP des pièces jointes de courrier associées à une étiquette de confidentialité est uniquement prise en charge par les types de fichier Office.</span><span class="sxs-lookup"><span data-stu-id="a34c6-151">\* DLP detection of sensitivity labeled email attachments are supported for Office file types only.</span></span>

<span data-ttu-id="a34c6-152">\*\* Les pièces jointes envoyées dans Teams au cours des conversations ou canaux de 1:1 sont chargées automatiquement sur OneDrive pour Entreprise et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a34c6-152">\*\* Attachments sent in Teams over 1:1 chat or channels are automatically uploaded to OneDrive for Business and SharePoint.</span></span> <span data-ttu-id="a34c6-153">Par conséquent, si SharePoint Online ou OneDrive pour Entreprise sont inclus dans votre stratégie DLP, les pièces jointes à étiquettes envoyées dans Teams sont automatiquement incluses dans l’étendue de cette condition.</span><span class="sxs-lookup"><span data-stu-id="a34c6-153">So if SharePoint Online or OneDrive for Business are included as locations in your DLP policy, then labeled attachments sent in Teams will be automatically included in the scope of this condition.</span></span> <span data-ttu-id="a34c6-154">Il n’est pas nécessaire de sélectionner Teams comme emplacement dans la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="a34c6-154">Teams as a location does not need to be selected in the DLP policy.</span></span>

### <a name="supported-scenarios"></a><span data-ttu-id="a34c6-155">Scénarios pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-155">Supported scenarios</span></span>

- <span data-ttu-id="a34c6-156">L’administrateur DLP peut afficher la liste de toutes les étiquettes de confidentialité du client lorsqu’il choisit d’inclure une ou plusieurs étiquettes de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="a34c6-156">DLP Admin will be able to see a list of all sensitivity labels in the tenant when they choose to include one or more sensitivity labels as a condition.</span></span>

- <span data-ttu-id="a34c6-157">L’utilisation d’étiquettes de confidentialité comme condition est prise en charge dans toutes les charges de travail, comme indiqué dans la matrice de support ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a34c6-157">Using sensitivity labels as a condition is supported across all workloads as indicated in the support matrix above.</span></span>

- <span data-ttu-id="a34c6-158">Les conseils de stratégie DLP continueront à être présentés dans les charges de travail (sauf Outlook Win32) pour les stratégies DLP qui contiennent une étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="a34c6-158">DLP policy tips will continue to be shown across workloads (except Outlook Win32) for DLP policies which contain sensitivity label as a condition.</span></span>

- <span data-ttu-id="a34c6-159">Les étiquettes de confidentialité s’affichent également dans le message de rapport d’incident si une stratégie DLP avec une étiquette de confidentialité comme condition est associée.</span><span class="sxs-lookup"><span data-stu-id="a34c6-159">Sensitivity labels will also appear as a part of the incident report email if a DLP policy with sensitivity label as a condition is matched.</span></span>

- <span data-ttu-id="a34c6-160">Les détails de l’étiquette de confidentialité s’affichent également dans le journal d’audit de correspondance des règles DLP pour une correspondance de stratégie DLP qui contient l’étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="a34c6-160">Sensitivity label details will also be shown in the DLP rule match audit log for a DLP policy match which contains sensitivity label as a condition.</span></span>


### <a name="support-policy-tips"></a><span data-ttu-id="a34c6-161">Conseils de stratégie de support</span><span class="sxs-lookup"><span data-stu-id="a34c6-161">Support policy tips</span></span>


|<span data-ttu-id="a34c6-162">Charge de travail</span><span class="sxs-lookup"><span data-stu-id="a34c6-162">Workload</span></span>  |<span data-ttu-id="a34c6-163">Prise en charge/non prise en charge des conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="a34c6-163">Policy tips supported/not supported</span></span>  |
|---------|---------|
|<span data-ttu-id="a34c6-164">OWA</span><span class="sxs-lookup"><span data-stu-id="a34c6-164">OWA</span></span> |    <span data-ttu-id="a34c6-165">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-165">supported</span></span>     |
|<span data-ttu-id="a34c6-166">Outlook Win 32</span><span class="sxs-lookup"><span data-stu-id="a34c6-166">Outlook Win 32</span></span>    |  <span data-ttu-id="a34c6-167">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-167">not supported</span></span>       |
|<span data-ttu-id="a34c6-168">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a34c6-168">SharePoint</span></span>   |   <span data-ttu-id="a34c6-169">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-169">supported</span></span>      |
|<span data-ttu-id="a34c6-170">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="a34c6-170">OneDrive for Business</span></span>    |    <span data-ttu-id="a34c6-171">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-171">supported</span></span>     |
|<span data-ttu-id="a34c6-172">appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a34c6-172">endpoint devices</span></span>   |  <span data-ttu-id="a34c6-173">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a34c6-173">not supported</span></span>       |
