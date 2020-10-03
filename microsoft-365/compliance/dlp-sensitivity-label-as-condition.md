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
ms.openlocfilehash: 561a6cbd7b8aeb9082862319c5cc6419fd79c896
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321109"
---
# <a name="use-sensitivity-labels-as-conditions-in-dlp-policies-preview"></a><span data-ttu-id="7a8fd-103">Utiliser les étiquettes de confidentialité comme conditions dans les stratégies DLP (préversion)</span><span class="sxs-lookup"><span data-stu-id="7a8fd-103">Use sensitivity labels as conditions in DLP policies (preview)</span></span>

<span data-ttu-id="7a8fd-104">Vous pouvez utiliser [ les étiquettes de confidentialité](sensitivity-labels.md)comme condition dans les stratégies de protection contre la perte de données pour cet emplacement:</span><span class="sxs-lookup"><span data-stu-id="7a8fd-104">You can use [sensitivity labels](sensitivity-labels.md) as a condition in DLP policies for these location:</span></span>

- <span data-ttu-id="7a8fd-105">Messagerie Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7a8fd-105">Exchange Online email messages</span></span>
- <span data-ttu-id="7a8fd-106">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="7a8fd-106">SharePoint Online</span></span>
- <span data-ttu-id="7a8fd-107">Sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="7a8fd-107">OneDrive for Business sites</span></span>
- <span data-ttu-id="7a8fd-108">Appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a8fd-108">Windows 10 devices</span></span>

<span data-ttu-id="7a8fd-109">Les étiquettes de confidentialité apparaissent comme une option dans la liste du **Contenu**.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-109">Sensitivity labels appear as an option in the **Content contains** list.</span></span>

![Étiquette de confidentialité comme condition](../media/dlp-sensitivity-label-as-a-condition.png)

## <a name="supported-items-scenarios-and-policy-tips"></a><span data-ttu-id="7a8fd-111">Éléments, scénarios et conseils de stratégie pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-111">Supported items, scenarios, and policy tips</span></span>

<span data-ttu-id="7a8fd-112">Vous pouvez utiliser des étiquettes de confidentialité comme conditions sur ces éléments et dans ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-112">You can use sensitivity labels as conditions on these items and in these scenarios.</span></span>

### <a name="supported-items"></a><span data-ttu-id="7a8fd-113">Éléments non pris en charge </span><span class="sxs-lookup"><span data-stu-id="7a8fd-113">Supported items</span></span>

|<span data-ttu-id="7a8fd-114">service</span><span class="sxs-lookup"><span data-stu-id="7a8fd-114">service</span></span>  |<span data-ttu-id="7a8fd-115">type d’élément</span><span class="sxs-lookup"><span data-stu-id="7a8fd-115">item type</span></span>  |<span data-ttu-id="7a8fd-116">disponible pour l’astuce de stratégie</span><span class="sxs-lookup"><span data-stu-id="7a8fd-116">available to policy tip</span></span>  |<span data-ttu-id="7a8fd-117">applicable</span><span class="sxs-lookup"><span data-stu-id="7a8fd-117">enforceable</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="7a8fd-118">Exchange</span><span class="sxs-lookup"><span data-stu-id="7a8fd-118">Exchange</span></span>    |<span data-ttu-id="7a8fd-119">Message électronique</span><span class="sxs-lookup"><span data-stu-id="7a8fd-119">email message</span></span>         |<span data-ttu-id="7a8fd-120">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-120">yes</span></span>         |<span data-ttu-id="7a8fd-121">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-121">yes</span></span>         |
|<span data-ttu-id="7a8fd-122">Exchange</span><span class="sxs-lookup"><span data-stu-id="7a8fd-122">Exchange</span></span>    |<span data-ttu-id="7a8fd-123">Pièce jointe</span><span class="sxs-lookup"><span data-stu-id="7a8fd-123">email attachment</span></span>         |<span data-ttu-id="7a8fd-124">non \*</span><span class="sxs-lookup"><span data-stu-id="7a8fd-124">no \*</span></span>         |<span data-ttu-id="7a8fd-125">non \*</span><span class="sxs-lookup"><span data-stu-id="7a8fd-125">no \*</span></span>         |
|<span data-ttu-id="7a8fd-126">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="7a8fd-126">SharePoint Online</span></span>     |<span data-ttu-id="7a8fd-127">éléments dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="7a8fd-127">items in SharePoint Online</span></span>         |<span data-ttu-id="7a8fd-128">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-128">yes</span></span>         |<span data-ttu-id="7a8fd-129">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-129">yes</span></span>         |
|<span data-ttu-id="7a8fd-130">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="7a8fd-130">OneDrive for Business</span></span>     |<span data-ttu-id="7a8fd-131">éléments</span><span class="sxs-lookup"><span data-stu-id="7a8fd-131">items</span></span>         |<span data-ttu-id="7a8fd-132">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-132">yes</span></span>         |<span data-ttu-id="7a8fd-133">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-133">yes</span></span>         |
|<span data-ttu-id="7a8fd-134">Teams</span><span class="sxs-lookup"><span data-stu-id="7a8fd-134">Teams</span></span>     |<span data-ttu-id="7a8fd-135">Teams et messages de canal</span><span class="sxs-lookup"><span data-stu-id="7a8fd-135">Teams and channel messages</span></span>         |<span data-ttu-id="7a8fd-136">non applicable</span><span class="sxs-lookup"><span data-stu-id="7a8fd-136">not applicable</span></span>         |<span data-ttu-id="7a8fd-137">non applicable</span><span class="sxs-lookup"><span data-stu-id="7a8fd-137">not applicable</span></span>         |
|<span data-ttu-id="7a8fd-138">Teams</span><span class="sxs-lookup"><span data-stu-id="7a8fd-138">Teams</span></span>     |<span data-ttu-id="7a8fd-139">pièces jointes</span><span class="sxs-lookup"><span data-stu-id="7a8fd-139">attachments</span></span>         |<span data-ttu-id="7a8fd-140">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="7a8fd-140">yes \*\*</span></span>         |<span data-ttu-id="7a8fd-141">Oui \*\*</span><span class="sxs-lookup"><span data-stu-id="7a8fd-141">yes \*\*</span></span>         |
|<span data-ttu-id="7a8fd-142">Appareils Windows 10 (préversion)</span><span class="sxs-lookup"><span data-stu-id="7a8fd-142">Windows 10 devices (preview)</span></span>     |<span data-ttu-id="7a8fd-143">éléments</span><span class="sxs-lookup"><span data-stu-id="7a8fd-143">items</span></span>         |<span data-ttu-id="7a8fd-144">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-144">yes</span></span>         |<span data-ttu-id="7a8fd-145">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-145">yes</span></span>         |
|<span data-ttu-id="7a8fd-146">MCAS (préversion)</span><span class="sxs-lookup"><span data-stu-id="7a8fd-146">MCAS (preview)</span></span> |<span data-ttu-id="7a8fd-147">éléments</span><span class="sxs-lookup"><span data-stu-id="7a8fd-147">items</span></span>         |<span data-ttu-id="7a8fd-148">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-148">yes</span></span>         |<span data-ttu-id="7a8fd-149">oui</span><span class="sxs-lookup"><span data-stu-id="7a8fd-149">yes</span></span>         |

<span data-ttu-id="7a8fd-150">\* La détection DLP des étiquettes de confidentialité sur les messages électroniques est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-150">\* DLP detection of sensitivity labels on emails are supported.</span></span> <span data-ttu-id="7a8fd-151">La détection DLP des pièces jointes à étiquettes de confidentialité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-151">DLP detection of sensitivity labeled email attachments are not.</span></span>

<span data-ttu-id="7a8fd-152">\*\* Les pièces jointes envoyées dans Teams au cours des conversations ou canaux de 1:1 sont chargées automatiquement sur OneDrive pour Entreprise et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-152">\*\* Attachments sent in Teams over 1:1 chat or channels are automatically uploaded to OneDrive for Business and SharePoint.</span></span> <span data-ttu-id="7a8fd-153">Par conséquent, si SharePoint Online ou OneDrive pour Entreprise sont inclus dans votre stratégie DLP, les pièces jointes à étiquettes envoyées dans Teams sont automatiquement incluses dans l’étendue de cette condition.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-153">So if SharePoint Online or OneDrive for Business are included as locations in your DLP policy, then labeled attachments sent in Teams will be automatically included in the scope of this condition.</span></span> <span data-ttu-id="7a8fd-154">Il n’est pas nécessaire de sélectionner Teams comme emplacement dans la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-154">Teams as a location does not need to be selected in the DLP policy.</span></span>

### <a name="supported-scenarios"></a><span data-ttu-id="7a8fd-155">Scénarios pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-155">Supported scenarios</span></span>

- <span data-ttu-id="7a8fd-156">L’administrateur DLP peut afficher la liste de toutes les étiquettes de confidentialité du client lorsqu’il choisit d’inclure une ou plusieurs étiquettes de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-156">DLP Admin will be able to see a list of all sensitivity labels in the tenant when they choose to include one or more sensitivity labels as a condition.</span></span>
- <span data-ttu-id="7a8fd-157">L’utilisation d’étiquettes de confidentialité comme condition est prise en charge dans toutes les charges de travail, comme indiqué dans la matrice de support ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-157">Using sensitivity labels as a condition is supported across all workloads as indicated in the support matrix above</span></span>
- <span data-ttu-id="7a8fd-158">Les conseils de stratégie DLP continueront à être présentés dans les charges de travail (sauf Outlook Win32) pour les stratégies DLP qui contiennent une étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-158">DLP policy tips will continue to be shown across workloads (except Outlook Win32) for DLP policies which contain sensitivity label as a condition.</span></span>
- <span data-ttu-id="7a8fd-159">Les étiquettes de confidentialité s’affichent également dans le message de rapport d’incident si une stratégie DLP avec une étiquette de confidentialité comme condition est associée.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-159">Sensitivity labels will also appear as a part of the incident report email if a DLP policy with sensitivity label as a condition is matched.</span></span>
- <span data-ttu-id="7a8fd-160">Les détails de l’étiquette de confidentialité s’affichent également dans le journal d’audit de correspondance des règles DLP pour une correspondance de stratégie DLP qui contient l’étiquette de confidentialité comme condition.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-160">Sensitivity label details will also be shown in the DLP rule match audit log for a DLP policy match which contains sensitivity label as a condition.</span></span>


### <a name="support-policy-tips"></a><span data-ttu-id="7a8fd-161">Conseils de stratégie de support</span><span class="sxs-lookup"><span data-stu-id="7a8fd-161">Support policy tips</span></span>


|<span data-ttu-id="7a8fd-162">charge de travail</span><span class="sxs-lookup"><span data-stu-id="7a8fd-162">workload</span></span>  |<span data-ttu-id="7a8fd-163">conseils de stratégie pris en charge/non pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-163">policy tips supported/not supported</span></span>  |
|---------|---------|
|<span data-ttu-id="7a8fd-164">OWA</span><span class="sxs-lookup"><span data-stu-id="7a8fd-164">OWA</span></span> |    <span data-ttu-id="7a8fd-165">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-165">supported</span></span>     |
|<span data-ttu-id="7a8fd-166">Outlook Win 32</span><span class="sxs-lookup"><span data-stu-id="7a8fd-166">Outlook Win 32</span></span>    |  <span data-ttu-id="7a8fd-167">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-167">not supported</span></span>       |
|<span data-ttu-id="7a8fd-168">SharePoint</span><span class="sxs-lookup"><span data-stu-id="7a8fd-168">SharePoint</span></span>   |   <span data-ttu-id="7a8fd-169">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-169">supported</span></span>      |
|<span data-ttu-id="7a8fd-170">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="7a8fd-170">OneDrive for Business</span></span>    |    <span data-ttu-id="7a8fd-171">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-171">supported</span></span>     |
|<span data-ttu-id="7a8fd-172">appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7a8fd-172">endpoint devices</span></span>   |  <span data-ttu-id="7a8fd-173">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8fd-173">not supported</span></span>       |
