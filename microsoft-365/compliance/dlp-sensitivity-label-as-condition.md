---
title: Utiliser les étiquettes de confidentialité comme conditions dans les stratégies DLP (préversion)
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
ms.openlocfilehash: 2f8eb30e23d722a5e8faf7d0ddaca6b9a94e279b
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48649633"
---
# <a name="use-sensitivity-labels-as-conditions-in-dlp-policies-preview"></a><span data-ttu-id="0d9e6-103">Utiliser les étiquettes de confidentialité comme conditions dans les stratégies DLP (préversion)</span><span class="sxs-lookup"><span data-stu-id="0d9e6-103">Use sensitivity labels as conditions in DLP policies (preview)</span></span>

<span data-ttu-id="0d9e6-104">Vous pouvez utiliser [ les étiquettes de confidentialité](sensitivity-labels.md)comme condition dans les stratégies de protection contre la perte de données pour cet emplacement:</span><span class="sxs-lookup"><span data-stu-id="0d9e6-104">You can use [sensitivity labels](sensitivity-labels.md) as a condition in DLP policies for these location:</span></span>

- <span data-ttu-id="0d9e6-105">Messagerie Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0d9e6-105">Exchange Online email messages</span></span>
- <span data-ttu-id="0d9e6-106">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d9e6-106">SharePoint Online</span></span>
- <span data-ttu-id="0d9e6-107">Sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="0d9e6-107">OneDrive for Business sites</span></span>
- <span data-ttu-id="0d9e6-108">Appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d9e6-108">Windows 10 devices</span></span>

<span data-ttu-id="0d9e6-109">Les étiquettes de confidentialité apparaissent comme une option dans la liste du **Contenu**.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-109">Sensitivity labels appear as an option in the **Content contains** list.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0d9e6-110">![étiquette de confidentialité comme condition](../media/dlp-sensitivity-label-as-a-condition.png)</span><span class="sxs-lookup"><span data-stu-id="0d9e6-110">![sensitivity label as a condition](../media/dlp-sensitivity-label-as-a-condition.png)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d9e6-111">**Les Etiquettes de Confidentialité** comme condition ne seront pas disponibles si vous avez sélectionné **Conversation d’équipe et messages de canaux** comme emplacement d’application de la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-111">**Sensitivity Labels** as a condition will not be available if you have selected **Teams chat and channel messages** as a location to apply the DLP policy.</span></span>


## <a name="supported-items-scenarios-and-policy-tips"></a><span data-ttu-id="0d9e6-112">Éléments, scénarios et conseils de stratégie pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-112">Supported items, scenarios, and policy tips</span></span>

<span data-ttu-id="0d9e6-113">Vous pouvez utiliser des étiquettes de confidentialité comme conditions sur ces éléments et dans ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-113">You can use sensitivity labels as conditions on these items and in these scenarios.</span></span>

### <a name="supported-items"></a><span data-ttu-id="0d9e6-114">Éléments non pris en charge </span><span class="sxs-lookup"><span data-stu-id="0d9e6-114">Supported items</span></span>

|<span data-ttu-id="0d9e6-115">Service</span><span class="sxs-lookup"><span data-stu-id="0d9e6-115">Service</span></span>  |<span data-ttu-id="0d9e6-116">Type d’élément</span><span class="sxs-lookup"><span data-stu-id="0d9e6-116">Item type</span></span>  |<span data-ttu-id="0d9e6-117">Disponible pour l’astuce de stratégie</span><span class="sxs-lookup"><span data-stu-id="0d9e6-117">Available to policy tip</span></span>  |<span data-ttu-id="0d9e6-118">Applicable</span><span class="sxs-lookup"><span data-stu-id="0d9e6-118">Enforceable</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="0d9e6-119">Exchange</span><span class="sxs-lookup"><span data-stu-id="0d9e6-119">Exchange</span></span>    |<span data-ttu-id="0d9e6-120">Message électronique</span><span class="sxs-lookup"><span data-stu-id="0d9e6-120">email message</span></span>         |<span data-ttu-id="0d9e6-121">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-121">yes</span></span>         |<span data-ttu-id="0d9e6-122">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-122">yes</span></span>         |
|<span data-ttu-id="0d9e6-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="0d9e6-123">Exchange</span></span>    |<span data-ttu-id="0d9e6-124">Pièce jointe</span><span class="sxs-lookup"><span data-stu-id="0d9e6-124">email attachment</span></span>         |<span data-ttu-id="0d9e6-125">non \*</span><span class="sxs-lookup"><span data-stu-id="0d9e6-125">no \*</span></span>         |<span data-ttu-id="0d9e6-126">non \*</span><span class="sxs-lookup"><span data-stu-id="0d9e6-126">no \*</span></span>         |
|<span data-ttu-id="0d9e6-127">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d9e6-127">SharePoint Online</span></span>     |<span data-ttu-id="0d9e6-128">éléments dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d9e6-128">items in SharePoint Online</span></span>         |<span data-ttu-id="0d9e6-129">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-129">yes</span></span>         |<span data-ttu-id="0d9e6-130">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-130">yes</span></span>         |
|<span data-ttu-id="0d9e6-131">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="0d9e6-131">OneDrive for Business</span></span>     |<span data-ttu-id="0d9e6-132">éléments</span><span class="sxs-lookup"><span data-stu-id="0d9e6-132">items</span></span>         |<span data-ttu-id="0d9e6-133">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-133">yes</span></span>         |<span data-ttu-id="0d9e6-134">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-134">yes</span></span>         |
|<span data-ttu-id="0d9e6-135">Teams</span><span class="sxs-lookup"><span data-stu-id="0d9e6-135">Teams</span></span>     |<span data-ttu-id="0d9e6-136">Teams et messages de canal</span><span class="sxs-lookup"><span data-stu-id="0d9e6-136">Teams and channel messages</span></span>         |<span data-ttu-id="0d9e6-137">non applicable</span><span class="sxs-lookup"><span data-stu-id="0d9e6-137">not applicable</span></span>         |<span data-ttu-id="0d9e6-138">non applicable</span><span class="sxs-lookup"><span data-stu-id="0d9e6-138">not applicable</span></span>         |
|<span data-ttu-id="0d9e6-139">Teams</span><span class="sxs-lookup"><span data-stu-id="0d9e6-139">Teams</span></span>     |<span data-ttu-id="0d9e6-140">pièces jointes</span><span class="sxs-lookup"><span data-stu-id="0d9e6-140">attachments</span></span>         |<span data-ttu-id="0d9e6-141">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="0d9e6-141">yes \*\*</span></span>         |<span data-ttu-id="0d9e6-142">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="0d9e6-142">yes \*\*</span></span>         |
|<span data-ttu-id="0d9e6-143">Appareils Windows 10 (préversion)</span><span class="sxs-lookup"><span data-stu-id="0d9e6-143">Windows 10 devices (preview)</span></span>     |<span data-ttu-id="0d9e6-144">éléments</span><span class="sxs-lookup"><span data-stu-id="0d9e6-144">items</span></span>         |<span data-ttu-id="0d9e6-145">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-145">yes</span></span>         |<span data-ttu-id="0d9e6-146">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-146">yes</span></span>         |
|<span data-ttu-id="0d9e6-147">MCAS (préversion)</span><span class="sxs-lookup"><span data-stu-id="0d9e6-147">MCAS (preview)</span></span> |<span data-ttu-id="0d9e6-148">éléments</span><span class="sxs-lookup"><span data-stu-id="0d9e6-148">items</span></span>         |<span data-ttu-id="0d9e6-149">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-149">yes</span></span>         |<span data-ttu-id="0d9e6-150">oui</span><span class="sxs-lookup"><span data-stu-id="0d9e6-150">yes</span></span>         |

<span data-ttu-id="0d9e6-151">\* La détection DLP des étiquettes de confidentialité sur les messages électroniques est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-151">\* DLP detection of sensitivity labels on emails are supported.</span></span> <span data-ttu-id="0d9e6-152">La détection DLP des pièces jointes à étiquettes de confidentialité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-152">DLP detection of sensitivity labeled email attachments are not.</span></span>

<span data-ttu-id="0d9e6-153">\*\* Les pièces jointes envoyées dans Teams au cours des conversations ou canaux de 1:1 sont chargées automatiquement sur OneDrive pour Entreprise et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-153">\*\* Attachments sent in Teams over 1:1 chat or channels are automatically uploaded to OneDrive for Business and SharePoint.</span></span> <span data-ttu-id="0d9e6-154">Par conséquent, si SharePoint Online ou OneDrive pour Entreprise sont inclus dans votre stratégie DLP, les pièces jointes à étiquettes envoyées dans Teams sont automatiquement incluses dans l’étendue de cette condition.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-154">So if SharePoint Online or OneDrive for Business are included as locations in your DLP policy, then labeled attachments sent in Teams will be automatically included in the scope of this condition.</span></span> <span data-ttu-id="0d9e6-155">Il n’est pas nécessaire de sélectionner Teams comme emplacement dans la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-155">Teams as a location does not need to be selected in the DLP policy.</span></span>

### <a name="supported-scenarios"></a><span data-ttu-id="0d9e6-156">Scénarios pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-156">Supported scenarios</span></span>

- <span data-ttu-id="0d9e6-157">L’administrateur DLP peut afficher la liste de toutes les étiquettes de confidentialité du client lorsqu’il choisit d’inclure une ou plusieurs étiquettes de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-157">DLP Admin will be able to see a list of all sensitivity labels in the tenant when they choose to include one or more sensitivity labels as a condition.</span></span>

- <span data-ttu-id="0d9e6-158">L’utilisation d’étiquettes de confidentialité comme condition est prise en charge dans toutes les charges de travail, comme indiqué dans la matrice de support ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-158">Using sensitivity labels as a condition is supported across all workloads as indicated in the support matrix above.</span></span>

- <span data-ttu-id="0d9e6-159">Les conseils de stratégie DLP continueront à être présentés dans les charges de travail (sauf Outlook Win32) pour les stratégies DLP qui contiennent une étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-159">DLP policy tips will continue to be shown across workloads (except Outlook Win32) for DLP policies which contain sensitivity label as a condition.</span></span>

- <span data-ttu-id="0d9e6-160">Les étiquettes de confidentialité s’affichent également dans le message de rapport d’incident si une stratégie DLP avec une étiquette de confidentialité comme condition est associée.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-160">Sensitivity labels will also appear as a part of the incident report email if a DLP policy with sensitivity label as a condition is matched.</span></span>

- <span data-ttu-id="0d9e6-161">Les détails de l’étiquette de confidentialité s’affichent également dans le journal d’audit de correspondance des règles DLP pour une correspondance de stratégie DLP qui contient l’étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="0d9e6-161">Sensitivity label details will also be shown in the DLP rule match audit log for a DLP policy match which contains sensitivity label as a condition.</span></span>


### <a name="support-policy-tips"></a><span data-ttu-id="0d9e6-162">Conseils de stratégie de support</span><span class="sxs-lookup"><span data-stu-id="0d9e6-162">Support policy tips</span></span>


|<span data-ttu-id="0d9e6-163">Charge de travail</span><span class="sxs-lookup"><span data-stu-id="0d9e6-163">Workload</span></span>  |<span data-ttu-id="0d9e6-164">Prise en charge/non prise en charge des conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="0d9e6-164">Policy tips supported/not supported</span></span>  |
|---------|---------|
|<span data-ttu-id="0d9e6-165">OWA</span><span class="sxs-lookup"><span data-stu-id="0d9e6-165">OWA</span></span> |    <span data-ttu-id="0d9e6-166">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-166">supported</span></span>     |
|<span data-ttu-id="0d9e6-167">Outlook Win 32</span><span class="sxs-lookup"><span data-stu-id="0d9e6-167">Outlook Win 32</span></span>    |  <span data-ttu-id="0d9e6-168">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-168">not supported</span></span>       |
|<span data-ttu-id="0d9e6-169">SharePoint</span><span class="sxs-lookup"><span data-stu-id="0d9e6-169">SharePoint</span></span>   |   <span data-ttu-id="0d9e6-170">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-170">supported</span></span>      |
|<span data-ttu-id="0d9e6-171">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="0d9e6-171">OneDrive for Business</span></span>    |    <span data-ttu-id="0d9e6-172">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-172">supported</span></span>     |
|<span data-ttu-id="0d9e6-173">appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0d9e6-173">endpoint devices</span></span>   |  <span data-ttu-id="0d9e6-174">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9e6-174">not supported</span></span>       |
