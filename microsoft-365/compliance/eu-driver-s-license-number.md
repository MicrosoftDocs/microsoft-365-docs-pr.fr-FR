---
title: Numéro de permis de conduire de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: f1a95ecbaf6b6d1ac189290dd6d076cfd91ab30f
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079282"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="bc342-104">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="bc342-104">EU Driver's License Number</span></span>

<span data-ttu-id="bc342-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE.</span><span class="sxs-lookup"><span data-stu-id="bc342-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="bc342-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="bc342-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="bc342-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="bc342-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="bc342-108">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-108">Format</span></span>

<span data-ttu-id="bc342-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-110">Pattern</span></span>

<span data-ttu-id="bc342-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-112">Checksum</span></span>

<span data-ttu-id="bc342-113">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-114">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-114">Definition</span></span>

<span data-ttu-id="bc342-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-116">L’expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="bc342-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-118">Keywords</span></span>

<span data-ttu-id="bc342-119">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-119"></span></span>
|<span data-ttu-id="bc342-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-121">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-121">dl#</span></span>  <br/> <span data-ttu-id="bc342-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-122">driver license</span></span>  <br/> <span data-ttu-id="bc342-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-123">driver license number</span></span>  <br/> <span data-ttu-id="bc342-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-124">driver licence</span></span>  <br/> <span data-ttu-id="bc342-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-125">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-126">drivers license</span></span>  <br/> <span data-ttu-id="bc342-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-127">driver's licence</span></span>  <br/> <span data-ttu-id="bc342-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-128">driver's license</span></span>  <br/> <span data-ttu-id="bc342-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-129">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="bc342-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-131">driving license number</span></span>  <br/> <span data-ttu-id="bc342-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-132">dlno#</span></span>  <br/> <span data-ttu-id="bc342-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="bc342-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="bc342-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="bc342-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="bc342-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="bc342-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="bc342-136">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-136">Format</span></span>

<span data-ttu-id="bc342-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-138">Pattern</span></span>

<span data-ttu-id="bc342-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-140">Checksum</span></span>

<span data-ttu-id="bc342-141">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-142">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-142">Definition</span></span>

<span data-ttu-id="bc342-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-144">L’expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="bc342-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-146">Keywords</span></span>

<span data-ttu-id="bc342-147">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-147"></span></span>
|<span data-ttu-id="bc342-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-149">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-149">dl#</span></span>  <br/> <span data-ttu-id="bc342-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-150">driver license</span></span>  <br/> <span data-ttu-id="bc342-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-151">driver license number</span></span>  <br/> <span data-ttu-id="bc342-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-152">driver licence</span></span>  <br/> <span data-ttu-id="bc342-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-153">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-154">drivers license</span></span>  <br/> <span data-ttu-id="bc342-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-155">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-156">driver's license</span></span>  <br/> <span data-ttu-id="bc342-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-157">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-158">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-159">dlno#</span></span>  <br/> <span data-ttu-id="bc342-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="bc342-160">rijbewijs</span></span>  <br/> <span data-ttu-id="bc342-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="bc342-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="bc342-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="bc342-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="bc342-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="bc342-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="bc342-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="bc342-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="bc342-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="bc342-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="bc342-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="bc342-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="bc342-169">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-169">Format</span></span>

<span data-ttu-id="bc342-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-171">Pattern</span></span>

<span data-ttu-id="bc342-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-173">Checksum</span></span>

<span data-ttu-id="bc342-174">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-175">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-175">Definition</span></span>

<span data-ttu-id="bc342-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-177">L’expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="bc342-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-179">Keywords</span></span>

<span data-ttu-id="bc342-180">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-180"></span></span>
|<span data-ttu-id="bc342-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-182">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-182">dl#</span></span>  <br/> <span data-ttu-id="bc342-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-183">driver license</span></span>  <br/> <span data-ttu-id="bc342-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-184">driver license number</span></span>  <br/> <span data-ttu-id="bc342-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-185">driver licence</span></span>  <br/> <span data-ttu-id="bc342-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-186">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-187">drivers license</span></span>  <br/> <span data-ttu-id="bc342-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-188">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-189">driver's license</span></span>  <br/> <span data-ttu-id="bc342-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-190">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-191">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-192">driving license number</span></span>  <br/> <span data-ttu-id="bc342-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-193">dlno#</span></span>  <br/> <span data-ttu-id="bc342-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="bc342-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="bc342-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="bc342-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="bc342-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="bc342-196">сумпс</span></span>  <br/> <span data-ttu-id="bc342-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="bc342-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="bc342-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="bc342-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="bc342-199">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-199">Format</span></span>

<span data-ttu-id="bc342-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-201">Pattern</span></span>

<span data-ttu-id="bc342-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-203">Checksum</span></span>

<span data-ttu-id="bc342-204">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-205">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-205">Definition</span></span>

<span data-ttu-id="bc342-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-207">L’expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="bc342-209">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-209">Keywords</span></span>

<span data-ttu-id="bc342-210">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-210"></span></span>
|<span data-ttu-id="bc342-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-212">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-212">dl#</span></span>  <br/> <span data-ttu-id="bc342-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-213">driver license</span></span>  <br/> <span data-ttu-id="bc342-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-214">driver license number</span></span>  <br/> <span data-ttu-id="bc342-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-215">driver licence</span></span>  <br/> <span data-ttu-id="bc342-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-216">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-217">drivers license</span></span>  <br/> <span data-ttu-id="bc342-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-218">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-219">driver's license</span></span>  <br/> <span data-ttu-id="bc342-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-220">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-221">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-222">driving license number</span></span>  <br/> <span data-ttu-id="bc342-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-223">dlno#</span></span>  <br/> <span data-ttu-id="bc342-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="bc342-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="bc342-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="bc342-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="bc342-226">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-226">Format</span></span>

<span data-ttu-id="bc342-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-228">Pattern</span></span>

<span data-ttu-id="bc342-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-230">Checksum</span></span>

<span data-ttu-id="bc342-231">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-232">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-232">Definition</span></span>

<span data-ttu-id="bc342-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-234">L’expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-236">Keywords</span></span>

<span data-ttu-id="bc342-237">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-237"></span></span>
|<span data-ttu-id="bc342-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-239">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-239">dl#</span></span>  <br/> <span data-ttu-id="bc342-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-240">driver license</span></span>  <br/> <span data-ttu-id="bc342-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-241">driver license number</span></span>  <br/> <span data-ttu-id="bc342-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-242">driver licence</span></span>  <br/> <span data-ttu-id="bc342-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-243">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-244">drivers license</span></span>  <br/> <span data-ttu-id="bc342-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-245">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-246">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-247">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-248">driving license number</span></span>  <br/> <span data-ttu-id="bc342-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-249">dlno#</span></span>  <br/> <span data-ttu-id="bc342-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="bc342-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="bc342-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="bc342-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="bc342-252">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-252">Format</span></span>

<span data-ttu-id="bc342-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-254">Pattern</span></span>

<span data-ttu-id="bc342-255">Huit lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="bc342-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="bc342-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="bc342-257">A space (optional)</span></span>
    
- <span data-ttu-id="bc342-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-259">Checksum</span></span>

<span data-ttu-id="bc342-260">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-261">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-261">Definition</span></span>

<span data-ttu-id="bc342-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-263">L’expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="bc342-265">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-265">Keywords</span></span>

<span data-ttu-id="bc342-266">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-266"></span></span>
|<span data-ttu-id="bc342-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-268">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-268">dl#</span></span>  <br/> <span data-ttu-id="bc342-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-269">driver license</span></span>  <br/> <span data-ttu-id="bc342-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-270">driver license number</span></span>  <br/> <span data-ttu-id="bc342-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-271">driver licence</span></span>  <br/> <span data-ttu-id="bc342-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-272">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-273">drivers license</span></span>  <br/> <span data-ttu-id="bc342-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-274">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-275">driver's license</span></span>  <br/> <span data-ttu-id="bc342-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-276">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-277">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-278">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-279">driving license number</span></span>  <br/> <span data-ttu-id="bc342-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-280">dlno#</span></span>  <br/> <span data-ttu-id="bc342-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="bc342-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="bc342-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="bc342-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="bc342-283">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-283">Format</span></span>

<span data-ttu-id="bc342-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-285">Pattern</span></span>

<span data-ttu-id="bc342-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-287">Checksum</span></span>

<span data-ttu-id="bc342-288">Oui</span><span class="sxs-lookup"><span data-stu-id="bc342-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-289">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-289">Definition</span></span>

<span data-ttu-id="bc342-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-291">L’expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="bc342-293">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-293">Keywords</span></span>

<span data-ttu-id="bc342-294">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-294"></span></span>
|<span data-ttu-id="bc342-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-296">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-296">dl#</span></span>  <br/> <span data-ttu-id="bc342-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-297">driver license</span></span>  <br/> <span data-ttu-id="bc342-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-298">driver license number</span></span>  <br/> <span data-ttu-id="bc342-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-299">driver licence</span></span>  <br/> <span data-ttu-id="bc342-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-300">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-301">drivers license</span></span>  <br/> <span data-ttu-id="bc342-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-302">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-303">driver's license</span></span>  <br/> <span data-ttu-id="bc342-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-304">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-305">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-306">driving license number</span></span>  <br/> <span data-ttu-id="bc342-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-307">dlno#</span></span>  <br/> <span data-ttu-id="bc342-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="bc342-308">kørekort</span></span>  <br/> <span data-ttu-id="bc342-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="bc342-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="bc342-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="bc342-311">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-311">Format</span></span>

<span data-ttu-id="bc342-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-313">Pattern</span></span>

<span data-ttu-id="bc342-314">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="bc342-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="bc342-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-317">Checksum</span></span>

<span data-ttu-id="bc342-318">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-319">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-319">Definition</span></span>

<span data-ttu-id="bc342-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-321">L’expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-323">Keywords</span></span>

<span data-ttu-id="bc342-324">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-324"></span></span>
|<span data-ttu-id="bc342-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-326">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-326">dl#</span></span>  <br/> <span data-ttu-id="bc342-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-327">driver license</span></span>  <br/> <span data-ttu-id="bc342-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-328">driver license number</span></span>  <br/> <span data-ttu-id="bc342-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-329">driver license number</span></span>  <br/> <span data-ttu-id="bc342-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-330">driver licence</span></span>  <br/> <span data-ttu-id="bc342-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-331">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-332">drivers license</span></span>  <br/> <span data-ttu-id="bc342-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-333">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-334">driver's license</span></span>  <br/> <span data-ttu-id="bc342-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-335">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-336">driving license number</span></span>  <br/> <span data-ttu-id="bc342-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-337">dlno#</span></span>  <br/> <span data-ttu-id="bc342-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="bc342-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="bc342-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="bc342-340">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-340">Format</span></span>

<span data-ttu-id="bc342-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="bc342-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-342">Pattern</span></span>

<span data-ttu-id="bc342-343">10 chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="bc342-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="bc342-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-344">Six digits</span></span> 
    
- <span data-ttu-id="bc342-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="bc342-345">A hyphen</span></span>
    
-  <span data-ttu-id="bc342-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="bc342-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-347">Checksum</span></span>

<span data-ttu-id="bc342-348">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-349">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-349">Definition</span></span>

<span data-ttu-id="bc342-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-351">L’expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-353">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-353">Keywords</span></span>

<span data-ttu-id="bc342-354">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-354"></span></span>
|<span data-ttu-id="bc342-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-356">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-356">dl#</span></span>  <br/> <span data-ttu-id="bc342-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-357">driver license</span></span>  <br/> <span data-ttu-id="bc342-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-358">driver license number</span></span>  <br/> <span data-ttu-id="bc342-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-359">driver licence</span></span>  <br/> <span data-ttu-id="bc342-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-360">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-361">drivers license</span></span>  <br/> <span data-ttu-id="bc342-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-362">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-363">driver's license</span></span>  <br/> <span data-ttu-id="bc342-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-364">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-365">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-366">driving license number</span></span>  <br/> <span data-ttu-id="bc342-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-367">dlno#</span></span>  <br/> <span data-ttu-id="bc342-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="bc342-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="bc342-369">France</span><span class="sxs-lookup"><span data-stu-id="bc342-369">France</span></span>

<span data-ttu-id="bc342-370">Pour plus d’informations, reportez-vous à la section « numéro de permis de conduire France » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bc342-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="bc342-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="bc342-371">Germany</span></span>

<span data-ttu-id="bc342-372">Pour plus d’informations, consultez la section « numéro de permis de conduire allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bc342-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="bc342-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="bc342-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="bc342-374">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-374">Format</span></span>

<span data-ttu-id="bc342-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-376">Pattern</span></span>

 <span data-ttu-id="bc342-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bc342-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-378">Checksum</span></span>

<span data-ttu-id="bc342-379">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-380">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-380">Definition</span></span>

<span data-ttu-id="bc342-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-382">L’expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-384">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-384">Keywords</span></span>

<span data-ttu-id="bc342-385">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-385"></span></span>
|<span data-ttu-id="bc342-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-387">Fichier #</span><span class="sxs-lookup"><span data-stu-id="bc342-387">dlL#</span></span>  <br/> <span data-ttu-id="bc342-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-388">driver license</span></span>  <br/> <span data-ttu-id="bc342-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-389">driver license number</span></span>  <br/> <span data-ttu-id="bc342-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-390">driver licence</span></span>  <br/> <span data-ttu-id="bc342-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-391">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-392">drivers license</span></span>  <br/> <span data-ttu-id="bc342-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-393">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-394">driver's license</span></span>  <br/> <span data-ttu-id="bc342-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-395">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-396">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-397">driving license number</span></span>  <br/> <span data-ttu-id="bc342-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-398">dlno#</span></span>  <br/> <span data-ttu-id="bc342-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="bc342-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="bc342-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="bc342-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="bc342-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="bc342-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="bc342-402">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-402">Format</span></span>

<span data-ttu-id="bc342-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-404">Pattern</span></span>

<span data-ttu-id="bc342-405">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="bc342-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="bc342-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-408">Checksum</span></span>

<span data-ttu-id="bc342-409">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-410">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-410">Definition</span></span>

<span data-ttu-id="bc342-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-412">L’expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-414">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-414">Keywords</span></span>

<span data-ttu-id="bc342-415">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-415"></span></span>
|<span data-ttu-id="bc342-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-417">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-417">dl#</span></span>  <br/> <span data-ttu-id="bc342-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-418">driver license</span></span>  <br/> <span data-ttu-id="bc342-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-419">driver license number</span></span>  <br/> <span data-ttu-id="bc342-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-420">driver licence</span></span>  <br/> <span data-ttu-id="bc342-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-421">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-422">drivers license</span></span>  <br/> <span data-ttu-id="bc342-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-423">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-424">driver's license</span></span>  <br/> <span data-ttu-id="bc342-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-425">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-426">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-427">driving license number</span></span>  <br/> <span data-ttu-id="bc342-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-428">dlno#</span></span>  <br/> <span data-ttu-id="bc342-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="bc342-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="bc342-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="bc342-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="bc342-431">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-431">Format</span></span>

<span data-ttu-id="bc342-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="bc342-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-433">Pattern</span></span>

<span data-ttu-id="bc342-434">Six chiffres et quatre lettres :</span><span class="sxs-lookup"><span data-stu-id="bc342-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="bc342-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-435">Six digits</span></span>
    
- <span data-ttu-id="bc342-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-437">Checksum</span></span>

<span data-ttu-id="bc342-438">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-439">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-439">Definition</span></span>

<span data-ttu-id="bc342-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-441">L’expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-443">Keywords</span></span>

<span data-ttu-id="bc342-444">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-444"></span></span>
|<span data-ttu-id="bc342-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-446">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-446">dl#</span></span>  <br/> <span data-ttu-id="bc342-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-447">driver license</span></span>  <br/> <span data-ttu-id="bc342-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-448">driver license number</span></span>  <br/> <span data-ttu-id="bc342-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-449">driver licence</span></span>  <br/> <span data-ttu-id="bc342-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-450">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-451">drivers license</span></span>  <br/> <span data-ttu-id="bc342-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-452">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-453">driver's license</span></span>  <br/> <span data-ttu-id="bc342-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-454">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-455">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-456">driving license number</span></span>  <br/> <span data-ttu-id="bc342-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-457">dlno#</span></span>  <br/> <span data-ttu-id="bc342-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="bc342-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="bc342-459">Italie</span><span class="sxs-lookup"><span data-stu-id="bc342-459">Italy</span></span>

<span data-ttu-id="bc342-460">Pour plus d’informations, reportez-vous à la section « Italie numéro de permis de conduire » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bc342-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="bc342-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="bc342-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="bc342-462">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-462">Format</span></span>

<span data-ttu-id="bc342-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-464">Pattern</span></span>

<span data-ttu-id="bc342-465">Trois lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="bc342-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="bc342-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-468">Checksum</span></span>

<span data-ttu-id="bc342-469">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-470">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-470">Definition</span></span>

<span data-ttu-id="bc342-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-472">L’expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-474">Keywords</span></span>

<span data-ttu-id="bc342-475">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-475"></span></span>
|<span data-ttu-id="bc342-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-477">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-477">dl#</span></span>  <br/> <span data-ttu-id="bc342-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-478">driver license</span></span>  <br/> <span data-ttu-id="bc342-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-479">driver license number</span></span>  <br/> <span data-ttu-id="bc342-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-480">driver licence</span></span>  <br/> <span data-ttu-id="bc342-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-481">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-482">drivers license</span></span>  <br/> <span data-ttu-id="bc342-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-483">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-484">driver's license</span></span>  <br/> <span data-ttu-id="bc342-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-485">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-486">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-487">driving license number</span></span>  <br/> <span data-ttu-id="bc342-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-488">dlno#</span></span>  <br/> <span data-ttu-id="bc342-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="bc342-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="bc342-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="bc342-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="bc342-491">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-491">Format</span></span>

<span data-ttu-id="bc342-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-493">Pattern</span></span>

 <span data-ttu-id="bc342-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bc342-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-495">Checksum</span></span>

<span data-ttu-id="bc342-496">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-497">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-497">Definition</span></span>

<span data-ttu-id="bc342-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-499">L’expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-501">Keywords</span></span>

<span data-ttu-id="bc342-502">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-502"></span></span>
|<span data-ttu-id="bc342-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-504">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-504">dl#</span></span>  <br/> <span data-ttu-id="bc342-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-505">driver license</span></span>  <br/> <span data-ttu-id="bc342-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-506">driver license number</span></span>  <br/> <span data-ttu-id="bc342-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-507">driver licence</span></span>  <br/> <span data-ttu-id="bc342-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-508">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-509">drivers license</span></span>  <br/> <span data-ttu-id="bc342-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-510">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-511">driver's license</span></span>  <br/> <span data-ttu-id="bc342-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-512">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-513">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-514">driving license number</span></span>  <br/> <span data-ttu-id="bc342-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-515">dlno#</span></span>  <br/> <span data-ttu-id="bc342-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="bc342-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="bc342-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="bc342-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="bc342-518">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-518">Format</span></span>

<span data-ttu-id="bc342-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-520">Pattern</span></span>

 <span data-ttu-id="bc342-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bc342-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-522">Checksum</span></span>

<span data-ttu-id="bc342-523">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-524">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-524">Definition</span></span>

<span data-ttu-id="bc342-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-526">L’expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-528">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-528">Keywords</span></span>

<span data-ttu-id="bc342-529">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-529"></span></span>
|<span data-ttu-id="bc342-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-531">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-531">dl#</span></span>  <br/> <span data-ttu-id="bc342-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-532">driver license</span></span>  <br/> <span data-ttu-id="bc342-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-533">driver license number</span></span>  <br/> <span data-ttu-id="bc342-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-534">driver licence</span></span>  <br/> <span data-ttu-id="bc342-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-535">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-536">drivers license</span></span>  <br/> <span data-ttu-id="bc342-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-537">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-538">driver's license</span></span>  <br/> <span data-ttu-id="bc342-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-539">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-540">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-541">driving license number</span></span>  <br/> <span data-ttu-id="bc342-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-542">dlno#</span></span>  <br/> <span data-ttu-id="bc342-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="bc342-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="bc342-544">Malte</span><span class="sxs-lookup"><span data-stu-id="bc342-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="bc342-545">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-545">Format</span></span>

<span data-ttu-id="bc342-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="bc342-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-547">Pattern</span></span>

<span data-ttu-id="bc342-548">Combinaison de deux caractères et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="bc342-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="bc342-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="bc342-550">A space (optional)</span></span>
    
- <span data-ttu-id="bc342-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-551">Three digits</span></span>
    
- <span data-ttu-id="bc342-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="bc342-552">A space (optional)</span></span>
    
- <span data-ttu-id="bc342-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-554">Checksum</span></span>

<span data-ttu-id="bc342-555">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-556">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-556">Definition</span></span>

<span data-ttu-id="bc342-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-558">L’expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-560">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-560">Keywords</span></span>

<span data-ttu-id="bc342-561">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-561"></span></span>
|<span data-ttu-id="bc342-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-563">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-563">dl#</span></span>  <br/> <span data-ttu-id="bc342-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-564">driver license</span></span>  <br/> <span data-ttu-id="bc342-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-565">driver license number</span></span>  <br/> <span data-ttu-id="bc342-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-566">driver licence</span></span>  <br/> <span data-ttu-id="bc342-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-567">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-568">drivers license</span></span>  <br/> <span data-ttu-id="bc342-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-569">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-570">driver's license</span></span>  <br/> <span data-ttu-id="bc342-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-571">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-572">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-573">driving license number</span></span>  <br/> <span data-ttu-id="bc342-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-574">dlno#</span></span>  <br/> <span data-ttu-id="bc342-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="bc342-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="bc342-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="bc342-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="bc342-577">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-577">Format</span></span>

<span data-ttu-id="bc342-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-579">Pattern</span></span>

<span data-ttu-id="bc342-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-581">Checksum</span></span>

<span data-ttu-id="bc342-582">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-583">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-583">Definition</span></span>

<span data-ttu-id="bc342-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-585">L’expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-587">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-587">Keywords</span></span>

<span data-ttu-id="bc342-588">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-588"></span></span>
|<span data-ttu-id="bc342-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-590">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-590">dl#</span></span>  <br/> <span data-ttu-id="bc342-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-591">driver license</span></span>  <br/> <span data-ttu-id="bc342-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-592">driver license number</span></span>  <br/> <span data-ttu-id="bc342-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-593">driver licence</span></span>  <br/> <span data-ttu-id="bc342-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-594">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-595">drivers license</span></span>  <br/> <span data-ttu-id="bc342-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-596">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-597">driver's license</span></span>  <br/> <span data-ttu-id="bc342-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-598">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-599">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-600">driving license number</span></span>  <br/> <span data-ttu-id="bc342-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-601">dlno#</span></span>  <br/> <span data-ttu-id="bc342-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-602">permis de conduire</span></span>  <br/> <span data-ttu-id="bc342-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="bc342-603">rijbewijs</span></span>  <br/> <span data-ttu-id="bc342-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="bc342-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="bc342-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="bc342-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="bc342-606">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-606">Format</span></span>

<span data-ttu-id="bc342-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="bc342-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-608">Pattern</span></span>

<span data-ttu-id="bc342-609">14 chiffres et 2 barres obliques :</span><span class="sxs-lookup"><span data-stu-id="bc342-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="bc342-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-610">Five digits</span></span> 
    
- <span data-ttu-id="bc342-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="bc342-611">A forward slash</span></span>
    
- <span data-ttu-id="bc342-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-612">Two digits</span></span>
    
- <span data-ttu-id="bc342-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="bc342-613">A forward slash</span></span>
    
- <span data-ttu-id="bc342-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-615">Checksum</span></span>

<span data-ttu-id="bc342-616">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-617">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-617">Definition</span></span>

<span data-ttu-id="bc342-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-619">L’expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-621">Keywords</span></span>

<span data-ttu-id="bc342-622">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-622"></span></span>
|<span data-ttu-id="bc342-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-624">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-624">dl#</span></span>  <br/> <span data-ttu-id="bc342-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-625">driver license</span></span>  <br/> <span data-ttu-id="bc342-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-626">driver license number</span></span>  <br/> <span data-ttu-id="bc342-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-627">driver licence</span></span>  <br/> <span data-ttu-id="bc342-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-628">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-629">drivers license</span></span>  <br/> <span data-ttu-id="bc342-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-630">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-631">driver's license</span></span>  <br/> <span data-ttu-id="bc342-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-632">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-633">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-634">driving license number</span></span>  <br/> <span data-ttu-id="bc342-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-635">dlno#</span></span>  <br/> <span data-ttu-id="bc342-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="bc342-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="bc342-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="bc342-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="bc342-638">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-638">Format</span></span>

<span data-ttu-id="bc342-639">Deux lettres suivies d’un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="bc342-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-640">Pattern</span></span>

<span data-ttu-id="bc342-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux :</span><span class="sxs-lookup"><span data-stu-id="bc342-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="bc342-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="bc342-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="bc342-643">A hyphen</span></span>
    
- <span data-ttu-id="bc342-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-644">Six digits</span></span>
    
- <span data-ttu-id="bc342-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="bc342-645">A space</span></span>
    
- <span data-ttu-id="bc342-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="bc342-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-647">Checksum</span></span>

<span data-ttu-id="bc342-648">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-649">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-649">Definition</span></span>

<span data-ttu-id="bc342-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-651">L’expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-653">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-653">Keywords</span></span>

<span data-ttu-id="bc342-654">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-654"></span></span>
|<span data-ttu-id="bc342-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-656">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-656">dl#</span></span>  <br/> <span data-ttu-id="bc342-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-657">driver license</span></span>  <br/> <span data-ttu-id="bc342-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-658">driver license number</span></span>  <br/> <span data-ttu-id="bc342-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-659">driver licence</span></span>  <br/> <span data-ttu-id="bc342-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-660">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-661">drivers license</span></span>  <br/> <span data-ttu-id="bc342-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-662">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-663">driver's license</span></span>  <br/> <span data-ttu-id="bc342-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-664">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-665">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-666">driving license number</span></span>  <br/> <span data-ttu-id="bc342-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-667">dlno#</span></span>  <br/> <span data-ttu-id="bc342-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="bc342-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="bc342-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="bc342-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="bc342-670">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-670">Format</span></span>

<span data-ttu-id="bc342-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-672">Pattern</span></span>

<span data-ttu-id="bc342-673">Un caractère suivi de huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="bc342-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="bc342-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="bc342-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="bc342-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-676">Checksum</span></span>

<span data-ttu-id="bc342-677">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-678">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-678">Definition</span></span>

<span data-ttu-id="bc342-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-680">L’expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-682">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-682">Keywords</span></span>

<span data-ttu-id="bc342-683">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-683"></span></span>
|<span data-ttu-id="bc342-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-685">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-685">dl#</span></span>  <br/> <span data-ttu-id="bc342-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-686">driver license</span></span>  <br/> <span data-ttu-id="bc342-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-687">driver license number</span></span>  <br/> <span data-ttu-id="bc342-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-688">driver licence</span></span>  <br/> <span data-ttu-id="bc342-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-689">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-690">drivers license</span></span>  <br/> <span data-ttu-id="bc342-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-691">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-692">driver's license</span></span>  <br/> <span data-ttu-id="bc342-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-693">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-694">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-695">driving license number</span></span>  <br/> <span data-ttu-id="bc342-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-696">dlno#</span></span>  <br/> <span data-ttu-id="bc342-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="bc342-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="bc342-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="bc342-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="bc342-699">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-699">Format</span></span>

<span data-ttu-id="bc342-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-701">Pattern</span></span>

<span data-ttu-id="bc342-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="bc342-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="bc342-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="bc342-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="bc342-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-705">Checksum</span></span>

<span data-ttu-id="bc342-706">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-707">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-707">Definition</span></span>

<span data-ttu-id="bc342-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-709">L’expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-711">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-711">Keywords</span></span>

<span data-ttu-id="bc342-712">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-712"></span></span>
|<span data-ttu-id="bc342-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-714">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-714">dl#</span></span>  <br/> <span data-ttu-id="bc342-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-715">driver license</span></span>  <br/> <span data-ttu-id="bc342-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-716">driver license number</span></span>  <br/> <span data-ttu-id="bc342-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-717">driver licence</span></span>  <br/> <span data-ttu-id="bc342-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-718">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-719">drivers license</span></span>  <br/> <span data-ttu-id="bc342-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-720">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-721">driver's license</span></span>  <br/> <span data-ttu-id="bc342-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-722">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-723">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-724">driving license number</span></span>  <br/> <span data-ttu-id="bc342-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-725">dlno#</span></span>  <br/> <span data-ttu-id="bc342-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="bc342-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="bc342-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="bc342-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="bc342-728">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-728">Format</span></span>

<span data-ttu-id="bc342-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="bc342-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-730">Pattern</span></span>

<span data-ttu-id="bc342-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bc342-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-732">Checksum</span></span>

<span data-ttu-id="bc342-733">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-734">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-734">Definition</span></span>

<span data-ttu-id="bc342-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-736">L’expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-738">Keywords</span></span>

<span data-ttu-id="bc342-739">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-739"></span></span>
|<span data-ttu-id="bc342-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-741">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-741">dl#</span></span>  <br/> <span data-ttu-id="bc342-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-742">driver license</span></span>  <br/> <span data-ttu-id="bc342-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-743">driver license number</span></span>  <br/> <span data-ttu-id="bc342-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-744">driver licence</span></span>  <br/> <span data-ttu-id="bc342-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-745">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-746">drivers license</span></span>  <br/> <span data-ttu-id="bc342-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-747">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-748">driver's license</span></span>  <br/> <span data-ttu-id="bc342-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-749">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-750">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-751">driving license number</span></span>  <br/> <span data-ttu-id="bc342-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-752">dlno#</span></span>  <br/> <span data-ttu-id="bc342-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="bc342-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="bc342-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="bc342-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="bc342-755">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-755">Format</span></span>

<span data-ttu-id="bc342-756">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="bc342-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-757">Pattern</span></span>

<span data-ttu-id="bc342-758">Huit chiffres suivis d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="bc342-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="bc342-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-759">Eight digits</span></span> 
    
- <span data-ttu-id="bc342-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="bc342-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-761">Checksum</span></span>

<span data-ttu-id="bc342-762">Oui</span><span class="sxs-lookup"><span data-stu-id="bc342-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-763">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-763">Definition</span></span>

<span data-ttu-id="bc342-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bc342-767">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-767">Keywords</span></span>

<span data-ttu-id="bc342-768">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-768"></span></span>
|<span data-ttu-id="bc342-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-770">dlno#</span></span>  <br/> <span data-ttu-id="bc342-771">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-771">dl#</span></span>  <br/> <span data-ttu-id="bc342-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-772">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-773">driver licence</span></span>  <br/> <span data-ttu-id="bc342-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-774">driver license</span></span>  <br/> <span data-ttu-id="bc342-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-775">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-776">drivers license</span></span>  <br/> <span data-ttu-id="bc342-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-777">driver's licence</span></span>  <br/> <span data-ttu-id="bc342-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-778">driver's license</span></span>  <br/> <span data-ttu-id="bc342-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-779">driving licence</span></span>  <br/> <span data-ttu-id="bc342-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-780">driving license</span></span>  <br/> <span data-ttu-id="bc342-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-781">driver licence number</span></span>  <br/> <span data-ttu-id="bc342-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-782">driver license number</span></span>  <br/> <span data-ttu-id="bc342-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-783">drivers licence number</span></span>  <br/> <span data-ttu-id="bc342-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-784">drivers license number</span></span>  <br/> <span data-ttu-id="bc342-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-785">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-786">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-787">driving licence number</span></span>  <br/> <span data-ttu-id="bc342-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-788">driving license number</span></span>  <br/> <span data-ttu-id="bc342-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-789">driving permit</span></span>  <br/> <span data-ttu-id="bc342-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-790">driving permit number</span></span>  <br/> <span data-ttu-id="bc342-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="bc342-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="bc342-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="bc342-792">permiso conducción</span></span>  <br/> <span data-ttu-id="bc342-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="bc342-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="bc342-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="bc342-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="bc342-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-796">licencia conducir</span></span>  <br/> <span data-ttu-id="bc342-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="bc342-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="bc342-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="bc342-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-800">permiso conducir</span></span>  <br/> <span data-ttu-id="bc342-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="bc342-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="bc342-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="bc342-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="bc342-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="bc342-804">Suède</span><span class="sxs-lookup"><span data-stu-id="bc342-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="bc342-805">Format</span><span class="sxs-lookup"><span data-stu-id="bc342-805">Format</span></span>

<span data-ttu-id="bc342-806">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="bc342-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bc342-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="bc342-807">Pattern</span></span>

<span data-ttu-id="bc342-808">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="bc342-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="bc342-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-809">Six digits</span></span> 
    
- <span data-ttu-id="bc342-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="bc342-810">A hyphen</span></span>
    
- <span data-ttu-id="bc342-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="bc342-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bc342-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc342-812">Checksum</span></span>

<span data-ttu-id="bc342-813">Non</span><span class="sxs-lookup"><span data-stu-id="bc342-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bc342-814">Définition</span><span class="sxs-lookup"><span data-stu-id="bc342-814">Definition</span></span>

<span data-ttu-id="bc342-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="bc342-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bc342-816">L’expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc342-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bc342-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="bc342-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="bc342-818">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bc342-818">Keywords</span></span>

<span data-ttu-id="bc342-819">| |</span><span class="sxs-lookup"><span data-stu-id="bc342-819"></span></span>
|<span data-ttu-id="bc342-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="bc342-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="bc342-821">LD #</span><span class="sxs-lookup"><span data-stu-id="bc342-821">dl#</span></span>  <br/> <span data-ttu-id="bc342-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-822">driver license</span></span>  <br/> <span data-ttu-id="bc342-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-823">driver license number</span></span>  <br/> <span data-ttu-id="bc342-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-824">driver licence</span></span>  <br/> <span data-ttu-id="bc342-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="bc342-825">drivers lic.</span></span>  <br/> <span data-ttu-id="bc342-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-826">drivers license</span></span>  <br/> <span data-ttu-id="bc342-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-827">drivers licence</span></span>  <br/> <span data-ttu-id="bc342-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-828">driver's license</span></span>  <br/> <span data-ttu-id="bc342-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-829">driver's license number</span></span>  <br/> <span data-ttu-id="bc342-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-830">driver's licence number</span></span>  <br/> <span data-ttu-id="bc342-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="bc342-831">driving license number</span></span>  <br/> <span data-ttu-id="bc342-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="bc342-832">dlno#</span></span>  <br/> <span data-ttu-id="bc342-833">körkort</span><span class="sxs-lookup"><span data-stu-id="bc342-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="bc342-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="bc342-834">UK</span></span>

<span data-ttu-id="bc342-835">Pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="bc342-835">For details, see the section "U.K.</span></span> <span data-ttu-id="bc342-836">Numéro de permis de conduire» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bc342-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc342-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc342-837">See also</span></span>

[<span data-ttu-id="bc342-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="bc342-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

