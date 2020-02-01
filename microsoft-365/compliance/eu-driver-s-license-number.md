---
title: Numéro de permis de conduire de l’UE
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: c54fcefcda08d0bc2ec500d25c74bb5789e27398
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41592655"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="e4b5b-104">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="e4b5b-104">EU Driver's License Number</span></span>

<span data-ttu-id="e4b5b-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="e4b5b-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e4b5b-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="e4b5b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-108">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-108">Format</span></span>

<span data-ttu-id="e4b5b-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-110">Pattern</span></span>

<span data-ttu-id="e4b5b-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-112">Checksum</span></span>

<span data-ttu-id="e4b5b-113">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-114">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-114">Definition</span></span>

<span data-ttu-id="e4b5b-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-116">L’expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-118">Keywords</span></span>

<span data-ttu-id="e4b5b-119">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-119">| |</span></span>
|<span data-ttu-id="e4b5b-120">**Keywords_austria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-121">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-121">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-122">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-123">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-124">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-125">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-126">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-127">driver's licence</span></span>  <br/> <span data-ttu-id="e4b5b-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-128">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-129">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="e4b5b-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-131">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-132">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e4b5b-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="e4b5b-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="e4b5b-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="e4b5b-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="e4b5b-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-136">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-136">Format</span></span>

<span data-ttu-id="e4b5b-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-138">Pattern</span></span>

<span data-ttu-id="e4b5b-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-140">Checksum</span></span>

<span data-ttu-id="e4b5b-141">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-142">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-142">Definition</span></span>

<span data-ttu-id="e4b5b-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-144">L’expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-146">Keywords</span></span>

<span data-ttu-id="e4b5b-147">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-147">| |</span></span>
|<span data-ttu-id="e4b5b-148">**Keywords__belgium_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-149">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-149">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-150">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-151">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-152">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-153">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-154">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-155">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-156">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-157">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-158">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-159">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-160">rijbewijs</span></span>  <br/> <span data-ttu-id="e4b5b-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="e4b5b-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="e4b5b-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="e4b5b-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="e4b5b-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="e4b5b-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="e4b5b-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="e4b5b-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="e4b5b-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="e4b5b-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="e4b5b-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-169">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-169">Format</span></span>

<span data-ttu-id="e4b5b-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-171">Pattern</span></span>

<span data-ttu-id="e4b5b-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-173">Checksum</span></span>

<span data-ttu-id="e4b5b-174">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-175">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-175">Definition</span></span>

<span data-ttu-id="e4b5b-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-177">L’expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-179">Keywords</span></span>

<span data-ttu-id="e4b5b-180">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-180">| |</span></span>
|<span data-ttu-id="e4b5b-181">**Keywords_bulgaria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-182">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-182">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-183">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-184">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-185">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-186">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-187">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-188">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-189">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-190">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-191">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-192">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-193">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="e4b5b-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="e4b5b-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="e4b5b-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="e4b5b-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="e4b5b-196">сумпс</span></span>  <br/> <span data-ttu-id="e4b5b-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="e4b5b-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="e4b5b-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-199">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-199">Format</span></span>

<span data-ttu-id="e4b5b-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-201">Pattern</span></span>

<span data-ttu-id="e4b5b-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-203">Checksum</span></span>

<span data-ttu-id="e4b5b-204">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-205">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-205">Definition</span></span>

<span data-ttu-id="e4b5b-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-207">L’expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-209">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-209">Keywords</span></span>

<span data-ttu-id="e4b5b-210">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-210">| |</span></span>
|<span data-ttu-id="e4b5b-211">**Keywords_croatia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-212">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-212">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-213">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-214">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-215">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-216">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-217">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-218">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-219">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-220">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-221">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-222">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-223">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="e4b5b-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="e4b5b-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="e4b5b-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-226">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-226">Format</span></span>

<span data-ttu-id="e4b5b-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-228">Pattern</span></span>

<span data-ttu-id="e4b5b-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-230">Checksum</span></span>

<span data-ttu-id="e4b5b-231">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-232">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-232">Definition</span></span>

<span data-ttu-id="e4b5b-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-234">L’expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-236">Keywords</span></span>

<span data-ttu-id="e4b5b-237">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-237">| |</span></span>
|<span data-ttu-id="e4b5b-238">**Keywords_cyprus_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-239">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-239">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-240">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-241">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-242">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-243">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-244">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-245">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-246">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-247">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-248">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-249">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="e4b5b-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="e4b5b-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="e4b5b-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-252">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-252">Format</span></span>

<span data-ttu-id="e4b5b-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-254">Pattern</span></span>

<span data-ttu-id="e4b5b-255">Huit lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="e4b5b-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="e4b5b-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="e4b5b-257">A space (optional)</span></span>
    
- <span data-ttu-id="e4b5b-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-259">Checksum</span></span>

<span data-ttu-id="e4b5b-260">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-261">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-261">Definition</span></span>

<span data-ttu-id="e4b5b-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-263">L’expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-265">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-265">Keywords</span></span>

<span data-ttu-id="e4b5b-266">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-266">| |</span></span>
|<span data-ttu-id="e4b5b-267">**Keywords_czech_republic_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-268">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-268">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-269">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-270">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-271">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-272">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-273">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-274">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-275">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-276">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-277">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-278">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-279">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-280">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="e4b5b-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="e4b5b-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="e4b5b-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-283">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-283">Format</span></span>

<span data-ttu-id="e4b5b-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-285">Pattern</span></span>

<span data-ttu-id="e4b5b-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-287">Checksum</span></span>

<span data-ttu-id="e4b5b-288">Oui</span><span class="sxs-lookup"><span data-stu-id="e4b5b-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-289">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-289">Definition</span></span>

<span data-ttu-id="e4b5b-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-291">L’expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="e4b5b-293">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-293">Keywords</span></span>

<span data-ttu-id="e4b5b-294">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-294">| |</span></span>
|<span data-ttu-id="e4b5b-295">**Keywords_denmark_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-296">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-296">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-297">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-298">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-299">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-300">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-301">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-302">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-303">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-304">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-305">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-306">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-307">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="e4b5b-308">kørekort</span></span>  <br/> <span data-ttu-id="e4b5b-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="e4b5b-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-311">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-311">Format</span></span>

<span data-ttu-id="e4b5b-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-313">Pattern</span></span>

<span data-ttu-id="e4b5b-314">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="e4b5b-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="e4b5b-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-317">Checksum</span></span>

<span data-ttu-id="e4b5b-318">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-319">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-319">Definition</span></span>

<span data-ttu-id="e4b5b-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-321">L’expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-323">Keywords</span></span>

<span data-ttu-id="e4b5b-324">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-324">| |</span></span>
|<span data-ttu-id="e4b5b-325">**Keywords_estonia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-326">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-326">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-327">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-328">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-329">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-330">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-331">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-332">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-333">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-334">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-335">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-336">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-337">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="e4b5b-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="e4b5b-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-340">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-340">Format</span></span>

<span data-ttu-id="e4b5b-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="e4b5b-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-342">Pattern</span></span>

<span data-ttu-id="e4b5b-343">10 chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="e4b5b-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-344">Six digits</span></span> 
    
- <span data-ttu-id="e4b5b-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="e4b5b-345">A hyphen</span></span>
    
-  <span data-ttu-id="e4b5b-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-347">Checksum</span></span>

<span data-ttu-id="e4b5b-348">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-349">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-349">Definition</span></span>

<span data-ttu-id="e4b5b-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-351">L’expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-353">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-353">Keywords</span></span>

<span data-ttu-id="e4b5b-354">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-354">| |</span></span>
|<span data-ttu-id="e4b5b-355">**Keywords_finland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-356">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-356">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-357">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-358">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-359">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-360">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-361">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-362">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-363">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-364">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-365">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-366">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-367">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="e4b5b-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="e4b5b-369">France</span><span class="sxs-lookup"><span data-stu-id="e4b5b-369">France</span></span>

<span data-ttu-id="e4b5b-370">Pour plus d’informations, reportez-vous à la section « numéro de permis de conduire France » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e4b5b-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="e4b5b-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="e4b5b-371">Germany</span></span>

<span data-ttu-id="e4b5b-372">Pour plus d’informations, consultez la section « numéro de permis de conduire allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e4b5b-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="e4b5b-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="e4b5b-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-374">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-374">Format</span></span>

<span data-ttu-id="e4b5b-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-376">Pattern</span></span>

 <span data-ttu-id="e4b5b-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-378">Checksum</span></span>

<span data-ttu-id="e4b5b-379">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-380">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-380">Definition</span></span>

<span data-ttu-id="e4b5b-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-382">L’expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-384">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-384">Keywords</span></span>

<span data-ttu-id="e4b5b-385">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-385">| |</span></span>
|<span data-ttu-id="e4b5b-386">**Keywords_greece_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-387">Fichier #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-387">dlL#</span></span>  <br/> <span data-ttu-id="e4b5b-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-388">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-389">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-390">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-391">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-392">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-393">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-394">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-395">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-396">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-397">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-398">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="e4b5b-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="e4b5b-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="e4b5b-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="e4b5b-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-402">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-402">Format</span></span>

<span data-ttu-id="e4b5b-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-404">Pattern</span></span>

<span data-ttu-id="e4b5b-405">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="e4b5b-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="e4b5b-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-408">Checksum</span></span>

<span data-ttu-id="e4b5b-409">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-410">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-410">Definition</span></span>

<span data-ttu-id="e4b5b-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-412">L’expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-414">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-414">Keywords</span></span>

<span data-ttu-id="e4b5b-415">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-415">| |</span></span>
|<span data-ttu-id="e4b5b-416">**Keywords_hungary_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-417">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-417">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-418">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-419">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-420">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-421">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-422">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-423">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-424">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-425">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-426">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-427">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-428">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="e4b5b-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="e4b5b-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="e4b5b-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-431">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-431">Format</span></span>

<span data-ttu-id="e4b5b-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-433">Pattern</span></span>

<span data-ttu-id="e4b5b-434">Six chiffres et quatre lettres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="e4b5b-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-435">Six digits</span></span>
    
- <span data-ttu-id="e4b5b-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-437">Checksum</span></span>

<span data-ttu-id="e4b5b-438">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-439">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-439">Definition</span></span>

<span data-ttu-id="e4b5b-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-441">L’expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-443">Keywords</span></span>

<span data-ttu-id="e4b5b-444">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-444">| |</span></span>
|<span data-ttu-id="e4b5b-445">**Keywords_ireland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-446">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-446">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-447">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-448">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-449">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-450">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-451">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-452">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-453">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-454">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-455">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-456">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-457">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="e4b5b-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="e4b5b-459">Italie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-459">Italy</span></span>

<span data-ttu-id="e4b5b-460">Pour plus d’informations, reportez-vous à la section « Italie numéro de permis de conduire » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e4b5b-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="e4b5b-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-462">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-462">Format</span></span>

<span data-ttu-id="e4b5b-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-464">Pattern</span></span>

<span data-ttu-id="e4b5b-465">Trois lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="e4b5b-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="e4b5b-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-468">Checksum</span></span>

<span data-ttu-id="e4b5b-469">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-470">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-470">Definition</span></span>

<span data-ttu-id="e4b5b-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-472">L’expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-474">Keywords</span></span>

<span data-ttu-id="e4b5b-475">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-475">| |</span></span>
|<span data-ttu-id="e4b5b-476">**Keywords_latvia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-477">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-477">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-478">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-479">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-480">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-481">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-482">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-483">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-484">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-485">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-486">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-487">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-488">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="e4b5b-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="e4b5b-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-491">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-491">Format</span></span>

<span data-ttu-id="e4b5b-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-493">Pattern</span></span>

 <span data-ttu-id="e4b5b-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-495">Checksum</span></span>

<span data-ttu-id="e4b5b-496">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-497">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-497">Definition</span></span>

<span data-ttu-id="e4b5b-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-499">L’expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-501">Keywords</span></span>

<span data-ttu-id="e4b5b-502">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-502">| |</span></span>
|<span data-ttu-id="e4b5b-503">**Keywords_lithuania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-504">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-504">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-505">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-506">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-507">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-508">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-509">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-510">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-511">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-512">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-513">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-514">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-515">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="e4b5b-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="e4b5b-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="e4b5b-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-518">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-518">Format</span></span>

<span data-ttu-id="e4b5b-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-520">Pattern</span></span>

 <span data-ttu-id="e4b5b-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-522">Checksum</span></span>

<span data-ttu-id="e4b5b-523">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-524">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-524">Definition</span></span>

<span data-ttu-id="e4b5b-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-526">L’expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-528">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-528">Keywords</span></span>

<span data-ttu-id="e4b5b-529">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-529">| |</span></span>
|<span data-ttu-id="e4b5b-530">**Keywords_luxemburg_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-531">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-531">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-532">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-533">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-534">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-535">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-536">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-537">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-538">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-539">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-540">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-541">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-542">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="e4b5b-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="e4b5b-544">Malte</span><span class="sxs-lookup"><span data-stu-id="e4b5b-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-545">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-545">Format</span></span>

<span data-ttu-id="e4b5b-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e4b5b-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-547">Pattern</span></span>

<span data-ttu-id="e4b5b-548">Combinaison de deux caractères et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="e4b5b-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="e4b5b-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="e4b5b-550">A space (optional)</span></span>
    
- <span data-ttu-id="e4b5b-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-551">Three digits</span></span>
    
- <span data-ttu-id="e4b5b-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="e4b5b-552">A space (optional)</span></span>
    
- <span data-ttu-id="e4b5b-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-554">Checksum</span></span>

<span data-ttu-id="e4b5b-555">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-556">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-556">Definition</span></span>

<span data-ttu-id="e4b5b-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-558">L’expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-560">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-560">Keywords</span></span>

<span data-ttu-id="e4b5b-561">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-561">| |</span></span>
|<span data-ttu-id="e4b5b-562">**Keywords_malta_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-563">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-563">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-564">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-565">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-566">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-567">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-568">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-569">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-570">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-571">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-572">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-573">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-574">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="e4b5b-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="e4b5b-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="e4b5b-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-577">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-577">Format</span></span>

<span data-ttu-id="e4b5b-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-579">Pattern</span></span>

<span data-ttu-id="e4b5b-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-581">Checksum</span></span>

<span data-ttu-id="e4b5b-582">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-583">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-583">Definition</span></span>

<span data-ttu-id="e4b5b-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-585">L’expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-587">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-587">Keywords</span></span>

<span data-ttu-id="e4b5b-588">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-588">| |</span></span>
|<span data-ttu-id="e4b5b-589">**Keywords_netherlands_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-590">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-590">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-591">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-592">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-593">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-594">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-595">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-596">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-597">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-598">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-599">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-600">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-601">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-602">permis de conduire</span></span>  <br/> <span data-ttu-id="e4b5b-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-603">rijbewijs</span></span>  <br/> <span data-ttu-id="e4b5b-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="e4b5b-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="e4b5b-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="e4b5b-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-606">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-606">Format</span></span>

<span data-ttu-id="e4b5b-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="e4b5b-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-608">Pattern</span></span>

<span data-ttu-id="e4b5b-609">14 chiffres et 2 barres obliques :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="e4b5b-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-610">Five digits</span></span> 
    
- <span data-ttu-id="e4b5b-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="e4b5b-611">A forward slash</span></span>
    
- <span data-ttu-id="e4b5b-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-612">Two digits</span></span>
    
- <span data-ttu-id="e4b5b-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="e4b5b-613">A forward slash</span></span>
    
- <span data-ttu-id="e4b5b-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-615">Checksum</span></span>

<span data-ttu-id="e4b5b-616">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-617">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-617">Definition</span></span>

<span data-ttu-id="e4b5b-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-619">L’expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-621">Keywords</span></span>

<span data-ttu-id="e4b5b-622">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-622">| |</span></span>
|<span data-ttu-id="e4b5b-623">**Keywords_poland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-624">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-624">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-625">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-626">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-627">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-628">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-629">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-630">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-631">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-632">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-633">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-634">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-635">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="e4b5b-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="e4b5b-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="e4b5b-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-638">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-638">Format</span></span>

<span data-ttu-id="e4b5b-639">Deux lettres suivies d’un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e4b5b-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-640">Pattern</span></span>

<span data-ttu-id="e4b5b-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="e4b5b-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="e4b5b-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="e4b5b-643">A hyphen</span></span>
    
- <span data-ttu-id="e4b5b-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-644">Six digits</span></span>
    
- <span data-ttu-id="e4b5b-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="e4b5b-645">A space</span></span>
    
- <span data-ttu-id="e4b5b-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="e4b5b-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-647">Checksum</span></span>

<span data-ttu-id="e4b5b-648">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-649">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-649">Definition</span></span>

<span data-ttu-id="e4b5b-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-651">L’expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-653">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-653">Keywords</span></span>

<span data-ttu-id="e4b5b-654">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-654">| |</span></span>
|<span data-ttu-id="e4b5b-655">**Keywords_portugal_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-656">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-656">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-657">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-658">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-659">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-660">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-661">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-662">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-663">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-664">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-665">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-666">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-667">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="e4b5b-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="e4b5b-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-670">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-670">Format</span></span>

<span data-ttu-id="e4b5b-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-672">Pattern</span></span>

<span data-ttu-id="e4b5b-673">Un caractère suivi de huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="e4b5b-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="e4b5b-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="e4b5b-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-676">Checksum</span></span>

<span data-ttu-id="e4b5b-677">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-678">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-678">Definition</span></span>

<span data-ttu-id="e4b5b-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-680">L’expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-682">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-682">Keywords</span></span>

<span data-ttu-id="e4b5b-683">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-683">| |</span></span>
|<span data-ttu-id="e4b5b-684">**Keywords_romania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-685">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-685">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-686">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-687">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-688">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-689">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-690">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-691">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-692">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-693">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-694">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-695">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-696">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="e4b5b-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="e4b5b-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-699">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-699">Format</span></span>

<span data-ttu-id="e4b5b-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-701">Pattern</span></span>

<span data-ttu-id="e4b5b-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="e4b5b-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="e4b5b-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="e4b5b-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-705">Checksum</span></span>

<span data-ttu-id="e4b5b-706">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-707">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-707">Definition</span></span>

<span data-ttu-id="e4b5b-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-709">L’expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-711">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-711">Keywords</span></span>

<span data-ttu-id="e4b5b-712">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-712">| |</span></span>
|<span data-ttu-id="e4b5b-713">**Keywords_slovakia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-714">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-714">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-715">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-716">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-717">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-718">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-719">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-720">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-721">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-722">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-723">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-724">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-725">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="e4b5b-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="e4b5b-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="e4b5b-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-728">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-728">Format</span></span>

<span data-ttu-id="e4b5b-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e4b5b-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-730">Pattern</span></span>

<span data-ttu-id="e4b5b-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e4b5b-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-732">Checksum</span></span>

<span data-ttu-id="e4b5b-733">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-734">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-734">Definition</span></span>

<span data-ttu-id="e4b5b-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-736">L’expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-738">Keywords</span></span>

<span data-ttu-id="e4b5b-739">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-739">| |</span></span>
|<span data-ttu-id="e4b5b-740">**Keywords_slovenia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-741">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-741">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-742">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-743">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-744">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-745">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-746">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-747">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-748">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-749">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-750">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-751">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-752">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="e4b5b-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="e4b5b-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="e4b5b-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-755">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-755">Format</span></span>

<span data-ttu-id="e4b5b-756">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="e4b5b-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-757">Pattern</span></span>

<span data-ttu-id="e4b5b-758">Huit chiffres suivis d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="e4b5b-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-759">Eight digits</span></span> 
    
- <span data-ttu-id="e4b5b-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e4b5b-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-761">Checksum</span></span>

<span data-ttu-id="e4b5b-762">Oui</span><span class="sxs-lookup"><span data-stu-id="e4b5b-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-763">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-763">Definition</span></span>

<span data-ttu-id="e4b5b-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-767">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-767">Keywords</span></span>

<span data-ttu-id="e4b5b-768">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-768">| |</span></span>
|<span data-ttu-id="e4b5b-769">**Keywords_spain_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-770">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-771">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-771">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-772">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-773">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-774">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-775">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-776">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-777">driver's licence</span></span>  <br/> <span data-ttu-id="e4b5b-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-778">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-779">driving licence</span></span>  <br/> <span data-ttu-id="e4b5b-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-780">driving license</span></span>  <br/> <span data-ttu-id="e4b5b-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-781">driver licence number</span></span>  <br/> <span data-ttu-id="e4b5b-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-782">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-783">drivers licence number</span></span>  <br/> <span data-ttu-id="e4b5b-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-784">drivers license number</span></span>  <br/> <span data-ttu-id="e4b5b-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-785">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-786">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-787">driving licence number</span></span>  <br/> <span data-ttu-id="e4b5b-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-788">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-789">driving permit</span></span>  <br/> <span data-ttu-id="e4b5b-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-790">driving permit number</span></span>  <br/> <span data-ttu-id="e4b5b-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="e4b5b-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="e4b5b-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="e4b5b-792">permiso conducción</span></span>  <br/> <span data-ttu-id="e4b5b-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="e4b5b-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="e4b5b-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="e4b5b-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="e4b5b-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-796">licencia conducir</span></span>  <br/> <span data-ttu-id="e4b5b-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="e4b5b-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="e4b5b-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="e4b5b-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-800">permiso conducir</span></span>  <br/> <span data-ttu-id="e4b5b-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="e4b5b-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="e4b5b-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="e4b5b-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="e4b5b-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="e4b5b-804">Suède</span><span class="sxs-lookup"><span data-stu-id="e4b5b-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="e4b5b-805">Format</span><span class="sxs-lookup"><span data-stu-id="e4b5b-805">Format</span></span>

<span data-ttu-id="e4b5b-806">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="e4b5b-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e4b5b-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-807">Pattern</span></span>

<span data-ttu-id="e4b5b-808">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="e4b5b-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-809">Six digits</span></span> 
    
- <span data-ttu-id="e4b5b-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="e4b5b-810">A hyphen</span></span>
    
- <span data-ttu-id="e4b5b-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="e4b5b-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e4b5b-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e4b5b-812">Checksum</span></span>

<span data-ttu-id="e4b5b-813">Non</span><span class="sxs-lookup"><span data-stu-id="e4b5b-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="e4b5b-814">Définition</span><span class="sxs-lookup"><span data-stu-id="e4b5b-814">Definition</span></span>

<span data-ttu-id="e4b5b-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e4b5b-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e4b5b-816">L’expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e4b5b-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="e4b5b-818">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e4b5b-818">Keywords</span></span>

<span data-ttu-id="e4b5b-819">| |</span><span class="sxs-lookup"><span data-stu-id="e4b5b-819">| |</span></span>
|<span data-ttu-id="e4b5b-820">**Keywords_sweden_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="e4b5b-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="e4b5b-821">LD #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-821">dl#</span></span>  <br/> <span data-ttu-id="e4b5b-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-822">driver license</span></span>  <br/> <span data-ttu-id="e4b5b-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-823">driver license number</span></span>  <br/> <span data-ttu-id="e4b5b-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-824">driver licence</span></span>  <br/> <span data-ttu-id="e4b5b-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-825">drivers lic.</span></span>  <br/> <span data-ttu-id="e4b5b-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-826">drivers license</span></span>  <br/> <span data-ttu-id="e4b5b-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-827">drivers licence</span></span>  <br/> <span data-ttu-id="e4b5b-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-828">driver's license</span></span>  <br/> <span data-ttu-id="e4b5b-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-829">driver's license number</span></span>  <br/> <span data-ttu-id="e4b5b-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-830">driver's licence number</span></span>  <br/> <span data-ttu-id="e4b5b-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e4b5b-831">driving license number</span></span>  <br/> <span data-ttu-id="e4b5b-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="e4b5b-832">dlno#</span></span>  <br/> <span data-ttu-id="e4b5b-833">körkort</span><span class="sxs-lookup"><span data-stu-id="e4b5b-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="e4b5b-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="e4b5b-834">UK</span></span>

<span data-ttu-id="e4b5b-835">Pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="e4b5b-835">For details, see the section "U.K.</span></span> <span data-ttu-id="e4b5b-836">Numéro de permis de conduire» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e4b5b-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4b5b-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b5b-837">See also</span></span>

[<span data-ttu-id="e4b5b-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="e4b5b-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

