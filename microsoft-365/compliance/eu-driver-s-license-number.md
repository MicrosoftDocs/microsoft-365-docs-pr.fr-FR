---
title: Numéro de permis de conduire de l’UE
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 2e75a8724dc91ef2d895c977fdd5fcc21e7a1da4
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43938828"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="79978-104">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="79978-104">EU Driver's License Number</span></span>

<span data-ttu-id="79978-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE.</span><span class="sxs-lookup"><span data-stu-id="79978-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="79978-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="79978-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="79978-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="79978-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="79978-108">Format</span><span class="sxs-lookup"><span data-stu-id="79978-108">Format</span></span>

<span data-ttu-id="79978-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-110">Pattern</span></span>

<span data-ttu-id="79978-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-112">Checksum</span></span>

<span data-ttu-id="79978-113">Non</span><span class="sxs-lookup"><span data-stu-id="79978-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-114">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-114">Definition</span></span>

<span data-ttu-id="79978-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-116">L’expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="79978-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-118">Keywords</span></span>

<span data-ttu-id="79978-119">| |</span><span class="sxs-lookup"><span data-stu-id="79978-119">| |</span></span>
|<span data-ttu-id="79978-120">**Keywords_austria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-121">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-121">dl#</span></span>  <br/> <span data-ttu-id="79978-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-122">driver license</span></span>  <br/> <span data-ttu-id="79978-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-123">driver license number</span></span>  <br/> <span data-ttu-id="79978-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-124">driver licence</span></span>  <br/> <span data-ttu-id="79978-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-125">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-126">drivers license</span></span>  <br/> <span data-ttu-id="79978-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-127">driver's licence</span></span>  <br/> <span data-ttu-id="79978-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-128">driver's license</span></span>  <br/> <span data-ttu-id="79978-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-129">driver's license number</span></span>  <br/> <span data-ttu-id="79978-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="79978-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-131">driving license number</span></span>  <br/> <span data-ttu-id="79978-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-132">dlno#</span></span>  <br/> <span data-ttu-id="79978-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="79978-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="79978-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="79978-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="79978-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="79978-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="79978-136">Format</span><span class="sxs-lookup"><span data-stu-id="79978-136">Format</span></span>

<span data-ttu-id="79978-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-138">Pattern</span></span>

<span data-ttu-id="79978-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-140">Checksum</span></span>

<span data-ttu-id="79978-141">Non</span><span class="sxs-lookup"><span data-stu-id="79978-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-142">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-142">Definition</span></span>

<span data-ttu-id="79978-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-144">L’expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="79978-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-146">Keywords</span></span>

<span data-ttu-id="79978-147">| |</span><span class="sxs-lookup"><span data-stu-id="79978-147">| |</span></span>
|<span data-ttu-id="79978-148">**Keywords__belgium_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-149">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-149">dl#</span></span>  <br/> <span data-ttu-id="79978-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-150">driver license</span></span>  <br/> <span data-ttu-id="79978-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-151">driver license number</span></span>  <br/> <span data-ttu-id="79978-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-152">driver licence</span></span>  <br/> <span data-ttu-id="79978-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-153">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-154">drivers license</span></span>  <br/> <span data-ttu-id="79978-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-155">drivers licence</span></span>  <br/> <span data-ttu-id="79978-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-156">driver's license</span></span>  <br/> <span data-ttu-id="79978-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-157">driver's license number</span></span>  <br/> <span data-ttu-id="79978-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-158">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-159">dlno#</span></span>  <br/> <span data-ttu-id="79978-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="79978-160">rijbewijs</span></span>  <br/> <span data-ttu-id="79978-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="79978-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="79978-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="79978-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="79978-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="79978-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="79978-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="79978-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="79978-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="79978-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="79978-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="79978-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="79978-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="79978-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="79978-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="79978-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="79978-169">Format</span><span class="sxs-lookup"><span data-stu-id="79978-169">Format</span></span>

<span data-ttu-id="79978-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-171">Pattern</span></span>

<span data-ttu-id="79978-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-173">Checksum</span></span>

<span data-ttu-id="79978-174">Non</span><span class="sxs-lookup"><span data-stu-id="79978-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-175">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-175">Definition</span></span>

<span data-ttu-id="79978-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-177">L’expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="79978-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-179">Keywords</span></span>

<span data-ttu-id="79978-180">| |</span><span class="sxs-lookup"><span data-stu-id="79978-180">| |</span></span>
|<span data-ttu-id="79978-181">**Keywords_bulgaria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-182">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-182">dl#</span></span>  <br/> <span data-ttu-id="79978-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-183">driver license</span></span>  <br/> <span data-ttu-id="79978-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-184">driver license number</span></span>  <br/> <span data-ttu-id="79978-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-185">driver licence</span></span>  <br/> <span data-ttu-id="79978-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-186">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-187">drivers license</span></span>  <br/> <span data-ttu-id="79978-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-188">drivers licence</span></span>  <br/> <span data-ttu-id="79978-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-189">driver's license</span></span>  <br/> <span data-ttu-id="79978-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-190">driver's license number</span></span>  <br/> <span data-ttu-id="79978-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-191">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-192">driving license number</span></span>  <br/> <span data-ttu-id="79978-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-193">dlno#</span></span>  <br/> <span data-ttu-id="79978-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="79978-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="79978-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="79978-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="79978-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="79978-196">сумпс</span></span>  <br/> <span data-ttu-id="79978-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="79978-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="79978-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="79978-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="79978-199">Format</span><span class="sxs-lookup"><span data-stu-id="79978-199">Format</span></span>

<span data-ttu-id="79978-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-201">Pattern</span></span>

<span data-ttu-id="79978-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-203">Checksum</span></span>

<span data-ttu-id="79978-204">Non</span><span class="sxs-lookup"><span data-stu-id="79978-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-205">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-205">Definition</span></span>

<span data-ttu-id="79978-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-207">L’expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="79978-209">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-209">Keywords</span></span>

<span data-ttu-id="79978-210">| |</span><span class="sxs-lookup"><span data-stu-id="79978-210">| |</span></span>
|<span data-ttu-id="79978-211">**Keywords_croatia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-212">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-212">dl#</span></span>  <br/> <span data-ttu-id="79978-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-213">driver license</span></span>  <br/> <span data-ttu-id="79978-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-214">driver license number</span></span>  <br/> <span data-ttu-id="79978-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-215">driver licence</span></span>  <br/> <span data-ttu-id="79978-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-216">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-217">drivers license</span></span>  <br/> <span data-ttu-id="79978-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-218">drivers licence</span></span>  <br/> <span data-ttu-id="79978-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-219">driver's license</span></span>  <br/> <span data-ttu-id="79978-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-220">driver's license number</span></span>  <br/> <span data-ttu-id="79978-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-221">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-222">driving license number</span></span>  <br/> <span data-ttu-id="79978-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-223">dlno#</span></span>  <br/> <span data-ttu-id="79978-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="79978-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="79978-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="79978-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="79978-226">Format</span><span class="sxs-lookup"><span data-stu-id="79978-226">Format</span></span>

<span data-ttu-id="79978-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-228">Pattern</span></span>

<span data-ttu-id="79978-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-230">Checksum</span></span>

<span data-ttu-id="79978-231">Non</span><span class="sxs-lookup"><span data-stu-id="79978-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-232">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-232">Definition</span></span>

<span data-ttu-id="79978-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-234">L’expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-236">Keywords</span></span>

<span data-ttu-id="79978-237">| |</span><span class="sxs-lookup"><span data-stu-id="79978-237">| |</span></span>
|<span data-ttu-id="79978-238">**Keywords_cyprus_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-239">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-239">dl#</span></span>  <br/> <span data-ttu-id="79978-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-240">driver license</span></span>  <br/> <span data-ttu-id="79978-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-241">driver license number</span></span>  <br/> <span data-ttu-id="79978-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-242">driver licence</span></span>  <br/> <span data-ttu-id="79978-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-243">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-244">drivers license</span></span>  <br/> <span data-ttu-id="79978-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-245">drivers licence</span></span>  <br/> <span data-ttu-id="79978-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-246">driver's license number</span></span>  <br/> <span data-ttu-id="79978-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-247">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-248">driving license number</span></span>  <br/> <span data-ttu-id="79978-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-249">dlno#</span></span>  <br/> <span data-ttu-id="79978-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="79978-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="79978-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="79978-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="79978-252">Format</span><span class="sxs-lookup"><span data-stu-id="79978-252">Format</span></span>

<span data-ttu-id="79978-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-254">Pattern</span></span>

<span data-ttu-id="79978-255">Huit lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="79978-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="79978-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="79978-257">A space (optional)</span></span>
    
- <span data-ttu-id="79978-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-259">Checksum</span></span>

<span data-ttu-id="79978-260">Non</span><span class="sxs-lookup"><span data-stu-id="79978-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-261">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-261">Definition</span></span>

<span data-ttu-id="79978-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-263">L’expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="79978-265">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-265">Keywords</span></span>

<span data-ttu-id="79978-266">| |</span><span class="sxs-lookup"><span data-stu-id="79978-266">| |</span></span>
|<span data-ttu-id="79978-267">**Keywords_czech_republic_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-268">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-268">dl#</span></span>  <br/> <span data-ttu-id="79978-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-269">driver license</span></span>  <br/> <span data-ttu-id="79978-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-270">driver license number</span></span>  <br/> <span data-ttu-id="79978-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-271">driver licence</span></span>  <br/> <span data-ttu-id="79978-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-272">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-273">drivers license</span></span>  <br/> <span data-ttu-id="79978-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-274">drivers licence</span></span>  <br/> <span data-ttu-id="79978-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-275">driver's license</span></span>  <br/> <span data-ttu-id="79978-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-276">driver's license number</span></span>  <br/> <span data-ttu-id="79978-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-277">driver's license number</span></span>  <br/> <span data-ttu-id="79978-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-278">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-279">driving license number</span></span>  <br/> <span data-ttu-id="79978-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-280">dlno#</span></span>  <br/> <span data-ttu-id="79978-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="79978-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="79978-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="79978-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="79978-283">Format</span><span class="sxs-lookup"><span data-stu-id="79978-283">Format</span></span>

<span data-ttu-id="79978-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-285">Pattern</span></span>

<span data-ttu-id="79978-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-287">Checksum</span></span>

<span data-ttu-id="79978-288">Oui</span><span class="sxs-lookup"><span data-stu-id="79978-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-289">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-289">Definition</span></span>

<span data-ttu-id="79978-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-291">L’expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="79978-293">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-293">Keywords</span></span>

<span data-ttu-id="79978-294">| |</span><span class="sxs-lookup"><span data-stu-id="79978-294">| |</span></span>
|<span data-ttu-id="79978-295">**Keywords_denmark_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-296">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-296">dl#</span></span>  <br/> <span data-ttu-id="79978-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-297">driver license</span></span>  <br/> <span data-ttu-id="79978-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-298">driver license number</span></span>  <br/> <span data-ttu-id="79978-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-299">driver licence</span></span>  <br/> <span data-ttu-id="79978-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-300">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-301">drivers license</span></span>  <br/> <span data-ttu-id="79978-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-302">drivers licence</span></span>  <br/> <span data-ttu-id="79978-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-303">driver's license</span></span>  <br/> <span data-ttu-id="79978-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-304">driver's license number</span></span>  <br/> <span data-ttu-id="79978-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-305">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-306">driving license number</span></span>  <br/> <span data-ttu-id="79978-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-307">dlno#</span></span>  <br/> <span data-ttu-id="79978-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="79978-308">kørekort</span></span>  <br/> <span data-ttu-id="79978-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="79978-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="79978-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="79978-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="79978-311">Format</span><span class="sxs-lookup"><span data-stu-id="79978-311">Format</span></span>

<span data-ttu-id="79978-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-313">Pattern</span></span>

<span data-ttu-id="79978-314">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="79978-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="79978-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-317">Checksum</span></span>

<span data-ttu-id="79978-318">Non</span><span class="sxs-lookup"><span data-stu-id="79978-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-319">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-319">Definition</span></span>

<span data-ttu-id="79978-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-321">L’expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-323">Keywords</span></span>

<span data-ttu-id="79978-324">| |</span><span class="sxs-lookup"><span data-stu-id="79978-324">| |</span></span>
|<span data-ttu-id="79978-325">**Keywords_estonia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-326">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-326">dl#</span></span>  <br/> <span data-ttu-id="79978-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-327">driver license</span></span>  <br/> <span data-ttu-id="79978-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-328">driver license number</span></span>  <br/> <span data-ttu-id="79978-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-329">driver license number</span></span>  <br/> <span data-ttu-id="79978-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-330">driver licence</span></span>  <br/> <span data-ttu-id="79978-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-331">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-332">drivers license</span></span>  <br/> <span data-ttu-id="79978-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-333">drivers licence</span></span>  <br/> <span data-ttu-id="79978-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-334">driver's license</span></span>  <br/> <span data-ttu-id="79978-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-335">driver's license number</span></span>  <br/> <span data-ttu-id="79978-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-336">driving license number</span></span>  <br/> <span data-ttu-id="79978-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-337">dlno#</span></span>  <br/> <span data-ttu-id="79978-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="79978-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="79978-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="79978-340">Format</span><span class="sxs-lookup"><span data-stu-id="79978-340">Format</span></span>

<span data-ttu-id="79978-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="79978-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-342">Pattern</span></span>

<span data-ttu-id="79978-343">10 chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="79978-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="79978-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-344">Six digits</span></span> 
    
- <span data-ttu-id="79978-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="79978-345">A hyphen</span></span>
    
-  <span data-ttu-id="79978-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="79978-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-347">Checksum</span></span>

<span data-ttu-id="79978-348">Non</span><span class="sxs-lookup"><span data-stu-id="79978-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-349">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-349">Definition</span></span>

<span data-ttu-id="79978-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-351">L’expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-353">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-353">Keywords</span></span>

<span data-ttu-id="79978-354">| |</span><span class="sxs-lookup"><span data-stu-id="79978-354">| |</span></span>
|<span data-ttu-id="79978-355">**Keywords_finland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-356">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-356">dl#</span></span>  <br/> <span data-ttu-id="79978-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-357">driver license</span></span>  <br/> <span data-ttu-id="79978-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-358">driver license number</span></span>  <br/> <span data-ttu-id="79978-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-359">driver licence</span></span>  <br/> <span data-ttu-id="79978-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-360">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-361">drivers license</span></span>  <br/> <span data-ttu-id="79978-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-362">drivers licence</span></span>  <br/> <span data-ttu-id="79978-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-363">driver's license</span></span>  <br/> <span data-ttu-id="79978-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-364">driver's license number</span></span>  <br/> <span data-ttu-id="79978-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-365">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-366">driving license number</span></span>  <br/> <span data-ttu-id="79978-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-367">dlno#</span></span>  <br/> <span data-ttu-id="79978-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="79978-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="79978-369">France</span><span class="sxs-lookup"><span data-stu-id="79978-369">France</span></span>

<span data-ttu-id="79978-370">Pour plus d’informations, reportez-vous à la section « numéro de permis de conduire France » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="79978-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="79978-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="79978-371">Germany</span></span>

<span data-ttu-id="79978-372">Pour plus d’informations, consultez la section « numéro de permis de conduire allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="79978-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="79978-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="79978-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="79978-374">Format</span><span class="sxs-lookup"><span data-stu-id="79978-374">Format</span></span>

<span data-ttu-id="79978-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-376">Pattern</span></span>

 <span data-ttu-id="79978-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="79978-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-378">Checksum</span></span>

<span data-ttu-id="79978-379">Non</span><span class="sxs-lookup"><span data-stu-id="79978-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-380">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-380">Definition</span></span>

<span data-ttu-id="79978-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-382">L’expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-384">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-384">Keywords</span></span>

<span data-ttu-id="79978-385">| |</span><span class="sxs-lookup"><span data-stu-id="79978-385">| |</span></span>
|<span data-ttu-id="79978-386">**Keywords_greece_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-387">Fichier #</span><span class="sxs-lookup"><span data-stu-id="79978-387">dlL#</span></span>  <br/> <span data-ttu-id="79978-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-388">driver license</span></span>  <br/> <span data-ttu-id="79978-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-389">driver license number</span></span>  <br/> <span data-ttu-id="79978-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-390">driver licence</span></span>  <br/> <span data-ttu-id="79978-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-391">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-392">drivers license</span></span>  <br/> <span data-ttu-id="79978-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-393">drivers licence</span></span>  <br/> <span data-ttu-id="79978-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-394">driver's license</span></span>  <br/> <span data-ttu-id="79978-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-395">driver's license number</span></span>  <br/> <span data-ttu-id="79978-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-396">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-397">driving license number</span></span>  <br/> <span data-ttu-id="79978-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-398">dlno#</span></span>  <br/> <span data-ttu-id="79978-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="79978-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="79978-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="79978-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="79978-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="79978-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="79978-402">Format</span><span class="sxs-lookup"><span data-stu-id="79978-402">Format</span></span>

<span data-ttu-id="79978-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-404">Pattern</span></span>

<span data-ttu-id="79978-405">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="79978-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="79978-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-408">Checksum</span></span>

<span data-ttu-id="79978-409">Non</span><span class="sxs-lookup"><span data-stu-id="79978-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-410">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-410">Definition</span></span>

<span data-ttu-id="79978-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-412">L’expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-414">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-414">Keywords</span></span>

<span data-ttu-id="79978-415">| |</span><span class="sxs-lookup"><span data-stu-id="79978-415">| |</span></span>
|<span data-ttu-id="79978-416">**Keywords_hungary_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-417">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-417">dl#</span></span>  <br/> <span data-ttu-id="79978-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-418">driver license</span></span>  <br/> <span data-ttu-id="79978-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-419">driver license number</span></span>  <br/> <span data-ttu-id="79978-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-420">driver licence</span></span>  <br/> <span data-ttu-id="79978-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-421">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-422">drivers license</span></span>  <br/> <span data-ttu-id="79978-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-423">drivers licence</span></span>  <br/> <span data-ttu-id="79978-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-424">driver's license</span></span>  <br/> <span data-ttu-id="79978-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-425">driver's license number</span></span>  <br/> <span data-ttu-id="79978-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-426">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-427">driving license number</span></span>  <br/> <span data-ttu-id="79978-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-428">dlno#</span></span>  <br/> <span data-ttu-id="79978-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="79978-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="79978-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="79978-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="79978-431">Format</span><span class="sxs-lookup"><span data-stu-id="79978-431">Format</span></span>

<span data-ttu-id="79978-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="79978-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-433">Pattern</span></span>

<span data-ttu-id="79978-434">Six chiffres et quatre lettres :</span><span class="sxs-lookup"><span data-stu-id="79978-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="79978-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-435">Six digits</span></span>
    
- <span data-ttu-id="79978-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-437">Checksum</span></span>

<span data-ttu-id="79978-438">Non</span><span class="sxs-lookup"><span data-stu-id="79978-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-439">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-439">Definition</span></span>

<span data-ttu-id="79978-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-441">L’expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-443">Keywords</span></span>

<span data-ttu-id="79978-444">| |</span><span class="sxs-lookup"><span data-stu-id="79978-444">| |</span></span>
|<span data-ttu-id="79978-445">**Keywords_ireland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-446">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-446">dl#</span></span>  <br/> <span data-ttu-id="79978-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-447">driver license</span></span>  <br/> <span data-ttu-id="79978-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-448">driver license number</span></span>  <br/> <span data-ttu-id="79978-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-449">driver licence</span></span>  <br/> <span data-ttu-id="79978-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-450">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-451">drivers license</span></span>  <br/> <span data-ttu-id="79978-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-452">drivers licence</span></span>  <br/> <span data-ttu-id="79978-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-453">driver's license</span></span>  <br/> <span data-ttu-id="79978-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-454">driver's license number</span></span>  <br/> <span data-ttu-id="79978-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-455">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-456">driving license number</span></span>  <br/> <span data-ttu-id="79978-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-457">dlno#</span></span>  <br/> <span data-ttu-id="79978-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="79978-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="79978-459">Italie</span><span class="sxs-lookup"><span data-stu-id="79978-459">Italy</span></span>

<span data-ttu-id="79978-460">Pour plus d’informations, reportez-vous à la section « Italie numéro de permis de conduire » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="79978-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="79978-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="79978-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="79978-462">Format</span><span class="sxs-lookup"><span data-stu-id="79978-462">Format</span></span>

<span data-ttu-id="79978-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-464">Pattern</span></span>

<span data-ttu-id="79978-465">Trois lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="79978-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="79978-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-468">Checksum</span></span>

<span data-ttu-id="79978-469">Non</span><span class="sxs-lookup"><span data-stu-id="79978-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-470">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-470">Definition</span></span>

<span data-ttu-id="79978-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-472">L’expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-474">Keywords</span></span>

<span data-ttu-id="79978-475">| |</span><span class="sxs-lookup"><span data-stu-id="79978-475">| |</span></span>
|<span data-ttu-id="79978-476">**Keywords_latvia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-477">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-477">dl#</span></span>  <br/> <span data-ttu-id="79978-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-478">driver license</span></span>  <br/> <span data-ttu-id="79978-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-479">driver license number</span></span>  <br/> <span data-ttu-id="79978-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-480">driver licence</span></span>  <br/> <span data-ttu-id="79978-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-481">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-482">drivers license</span></span>  <br/> <span data-ttu-id="79978-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-483">drivers licence</span></span>  <br/> <span data-ttu-id="79978-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-484">driver's license</span></span>  <br/> <span data-ttu-id="79978-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-485">driver's license number</span></span>  <br/> <span data-ttu-id="79978-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-486">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-487">driving license number</span></span>  <br/> <span data-ttu-id="79978-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-488">dlno#</span></span>  <br/> <span data-ttu-id="79978-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="79978-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="79978-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="79978-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="79978-491">Format</span><span class="sxs-lookup"><span data-stu-id="79978-491">Format</span></span>

<span data-ttu-id="79978-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-493">Pattern</span></span>

 <span data-ttu-id="79978-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="79978-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-495">Checksum</span></span>

<span data-ttu-id="79978-496">Non</span><span class="sxs-lookup"><span data-stu-id="79978-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-497">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-497">Definition</span></span>

<span data-ttu-id="79978-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-499">L’expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-501">Keywords</span></span>

<span data-ttu-id="79978-502">| |</span><span class="sxs-lookup"><span data-stu-id="79978-502">| |</span></span>
|<span data-ttu-id="79978-503">**Keywords_lithuania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-504">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-504">dl#</span></span>  <br/> <span data-ttu-id="79978-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-505">driver license</span></span>  <br/> <span data-ttu-id="79978-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-506">driver license number</span></span>  <br/> <span data-ttu-id="79978-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-507">driver licence</span></span>  <br/> <span data-ttu-id="79978-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-508">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-509">drivers license</span></span>  <br/> <span data-ttu-id="79978-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-510">drivers licence</span></span>  <br/> <span data-ttu-id="79978-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-511">driver's license</span></span>  <br/> <span data-ttu-id="79978-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-512">driver's license number</span></span>  <br/> <span data-ttu-id="79978-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-513">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-514">driving license number</span></span>  <br/> <span data-ttu-id="79978-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-515">dlno#</span></span>  <br/> <span data-ttu-id="79978-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="79978-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="79978-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="79978-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="79978-518">Format</span><span class="sxs-lookup"><span data-stu-id="79978-518">Format</span></span>

<span data-ttu-id="79978-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-520">Pattern</span></span>

 <span data-ttu-id="79978-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="79978-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-522">Checksum</span></span>

<span data-ttu-id="79978-523">Non</span><span class="sxs-lookup"><span data-stu-id="79978-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-524">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-524">Definition</span></span>

<span data-ttu-id="79978-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-526">L’expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-528">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-528">Keywords</span></span>

<span data-ttu-id="79978-529">| |</span><span class="sxs-lookup"><span data-stu-id="79978-529">| |</span></span>
|<span data-ttu-id="79978-530">**Keywords_luxemburg_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-531">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-531">dl#</span></span>  <br/> <span data-ttu-id="79978-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-532">driver license</span></span>  <br/> <span data-ttu-id="79978-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-533">driver license number</span></span>  <br/> <span data-ttu-id="79978-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-534">driver licence</span></span>  <br/> <span data-ttu-id="79978-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-535">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-536">drivers license</span></span>  <br/> <span data-ttu-id="79978-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-537">drivers licence</span></span>  <br/> <span data-ttu-id="79978-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-538">driver's license</span></span>  <br/> <span data-ttu-id="79978-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-539">driver's license number</span></span>  <br/> <span data-ttu-id="79978-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-540">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-541">driving license number</span></span>  <br/> <span data-ttu-id="79978-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-542">dlno#</span></span>  <br/> <span data-ttu-id="79978-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="79978-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="79978-544">Malte</span><span class="sxs-lookup"><span data-stu-id="79978-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="79978-545">Format</span><span class="sxs-lookup"><span data-stu-id="79978-545">Format</span></span>

<span data-ttu-id="79978-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="79978-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-547">Pattern</span></span>

<span data-ttu-id="79978-548">Combinaison de deux caractères et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="79978-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="79978-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="79978-550">A space (optional)</span></span>
    
- <span data-ttu-id="79978-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-551">Three digits</span></span>
    
- <span data-ttu-id="79978-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="79978-552">A space (optional)</span></span>
    
- <span data-ttu-id="79978-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-554">Checksum</span></span>

<span data-ttu-id="79978-555">Non</span><span class="sxs-lookup"><span data-stu-id="79978-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-556">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-556">Definition</span></span>

<span data-ttu-id="79978-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-558">L’expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-560">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-560">Keywords</span></span>

<span data-ttu-id="79978-561">| |</span><span class="sxs-lookup"><span data-stu-id="79978-561">| |</span></span>
|<span data-ttu-id="79978-562">**Keywords_malta_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-563">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-563">dl#</span></span>  <br/> <span data-ttu-id="79978-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-564">driver license</span></span>  <br/> <span data-ttu-id="79978-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-565">driver license number</span></span>  <br/> <span data-ttu-id="79978-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-566">driver licence</span></span>  <br/> <span data-ttu-id="79978-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-567">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-568">drivers license</span></span>  <br/> <span data-ttu-id="79978-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-569">drivers licence</span></span>  <br/> <span data-ttu-id="79978-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-570">driver's license</span></span>  <br/> <span data-ttu-id="79978-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-571">driver's license number</span></span>  <br/> <span data-ttu-id="79978-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-572">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-573">driving license number</span></span>  <br/> <span data-ttu-id="79978-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-574">dlno#</span></span>  <br/> <span data-ttu-id="79978-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="79978-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="79978-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="79978-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="79978-577">Format</span><span class="sxs-lookup"><span data-stu-id="79978-577">Format</span></span>

<span data-ttu-id="79978-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-579">Pattern</span></span>

<span data-ttu-id="79978-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-581">Checksum</span></span>

<span data-ttu-id="79978-582">Non</span><span class="sxs-lookup"><span data-stu-id="79978-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-583">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-583">Definition</span></span>

<span data-ttu-id="79978-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-585">L’expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-587">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-587">Keywords</span></span>

<span data-ttu-id="79978-588">| |</span><span class="sxs-lookup"><span data-stu-id="79978-588">| |</span></span>
|<span data-ttu-id="79978-589">**Keywords_netherlands_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-590">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-590">dl#</span></span>  <br/> <span data-ttu-id="79978-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-591">driver license</span></span>  <br/> <span data-ttu-id="79978-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-592">driver license number</span></span>  <br/> <span data-ttu-id="79978-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-593">driver licence</span></span>  <br/> <span data-ttu-id="79978-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-594">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-595">drivers license</span></span>  <br/> <span data-ttu-id="79978-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-596">drivers licence</span></span>  <br/> <span data-ttu-id="79978-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-597">driver's license</span></span>  <br/> <span data-ttu-id="79978-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-598">driver's license number</span></span>  <br/> <span data-ttu-id="79978-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-599">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-600">driving license number</span></span>  <br/> <span data-ttu-id="79978-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-601">dlno#</span></span>  <br/> <span data-ttu-id="79978-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-602">permis de conduire</span></span>  <br/> <span data-ttu-id="79978-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="79978-603">rijbewijs</span></span>  <br/> <span data-ttu-id="79978-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="79978-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="79978-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="79978-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="79978-606">Format</span><span class="sxs-lookup"><span data-stu-id="79978-606">Format</span></span>

<span data-ttu-id="79978-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="79978-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-608">Pattern</span></span>

<span data-ttu-id="79978-609">14 chiffres et 2 barres obliques :</span><span class="sxs-lookup"><span data-stu-id="79978-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="79978-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-610">Five digits</span></span> 
    
- <span data-ttu-id="79978-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="79978-611">A forward slash</span></span>
    
- <span data-ttu-id="79978-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-612">Two digits</span></span>
    
- <span data-ttu-id="79978-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="79978-613">A forward slash</span></span>
    
- <span data-ttu-id="79978-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-615">Checksum</span></span>

<span data-ttu-id="79978-616">Non</span><span class="sxs-lookup"><span data-stu-id="79978-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-617">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-617">Definition</span></span>

<span data-ttu-id="79978-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-619">L’expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-621">Keywords</span></span>

<span data-ttu-id="79978-622">| |</span><span class="sxs-lookup"><span data-stu-id="79978-622">| |</span></span>
|<span data-ttu-id="79978-623">**Keywords_poland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-624">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-624">dl#</span></span>  <br/> <span data-ttu-id="79978-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-625">driver license</span></span>  <br/> <span data-ttu-id="79978-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-626">driver license number</span></span>  <br/> <span data-ttu-id="79978-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-627">driver licence</span></span>  <br/> <span data-ttu-id="79978-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-628">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-629">drivers license</span></span>  <br/> <span data-ttu-id="79978-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-630">drivers licence</span></span>  <br/> <span data-ttu-id="79978-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-631">driver's license</span></span>  <br/> <span data-ttu-id="79978-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-632">driver's license number</span></span>  <br/> <span data-ttu-id="79978-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-633">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-634">driving license number</span></span>  <br/> <span data-ttu-id="79978-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-635">dlno#</span></span>  <br/> <span data-ttu-id="79978-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="79978-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="79978-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="79978-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="79978-638">Format</span><span class="sxs-lookup"><span data-stu-id="79978-638">Format</span></span>

<span data-ttu-id="79978-639">Deux lettres suivies d’un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="79978-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-640">Pattern</span></span>

<span data-ttu-id="79978-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux :</span><span class="sxs-lookup"><span data-stu-id="79978-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="79978-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="79978-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="79978-643">A hyphen</span></span>
    
- <span data-ttu-id="79978-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-644">Six digits</span></span>
    
- <span data-ttu-id="79978-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="79978-645">A space</span></span>
    
- <span data-ttu-id="79978-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="79978-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-647">Checksum</span></span>

<span data-ttu-id="79978-648">Non</span><span class="sxs-lookup"><span data-stu-id="79978-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-649">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-649">Definition</span></span>

<span data-ttu-id="79978-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-651">L’expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-653">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-653">Keywords</span></span>

<span data-ttu-id="79978-654">| |</span><span class="sxs-lookup"><span data-stu-id="79978-654">| |</span></span>
|<span data-ttu-id="79978-655">**Keywords_portugal_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-656">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-656">dl#</span></span>  <br/> <span data-ttu-id="79978-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-657">driver license</span></span>  <br/> <span data-ttu-id="79978-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-658">driver license number</span></span>  <br/> <span data-ttu-id="79978-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-659">driver licence</span></span>  <br/> <span data-ttu-id="79978-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-660">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-661">drivers license</span></span>  <br/> <span data-ttu-id="79978-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-662">drivers licence</span></span>  <br/> <span data-ttu-id="79978-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-663">driver's license</span></span>  <br/> <span data-ttu-id="79978-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-664">driver's license number</span></span>  <br/> <span data-ttu-id="79978-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-665">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-666">driving license number</span></span>  <br/> <span data-ttu-id="79978-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-667">dlno#</span></span>  <br/> <span data-ttu-id="79978-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="79978-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="79978-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="79978-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="79978-670">Format</span><span class="sxs-lookup"><span data-stu-id="79978-670">Format</span></span>

<span data-ttu-id="79978-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-672">Pattern</span></span>

<span data-ttu-id="79978-673">Un caractère suivi de huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="79978-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="79978-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="79978-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="79978-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-676">Checksum</span></span>

<span data-ttu-id="79978-677">Non</span><span class="sxs-lookup"><span data-stu-id="79978-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-678">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-678">Definition</span></span>

<span data-ttu-id="79978-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-680">L’expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-682">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-682">Keywords</span></span>

<span data-ttu-id="79978-683">| |</span><span class="sxs-lookup"><span data-stu-id="79978-683">| |</span></span>
|<span data-ttu-id="79978-684">**Keywords_romania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-685">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-685">dl#</span></span>  <br/> <span data-ttu-id="79978-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-686">driver license</span></span>  <br/> <span data-ttu-id="79978-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-687">driver license number</span></span>  <br/> <span data-ttu-id="79978-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-688">driver licence</span></span>  <br/> <span data-ttu-id="79978-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-689">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-690">drivers license</span></span>  <br/> <span data-ttu-id="79978-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-691">drivers licence</span></span>  <br/> <span data-ttu-id="79978-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-692">driver's license</span></span>  <br/> <span data-ttu-id="79978-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-693">driver's license number</span></span>  <br/> <span data-ttu-id="79978-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-694">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-695">driving license number</span></span>  <br/> <span data-ttu-id="79978-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-696">dlno#</span></span>  <br/> <span data-ttu-id="79978-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="79978-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="79978-698">Slovaquie</span><span class="sxs-lookup"><span data-stu-id="79978-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="79978-699">Format</span><span class="sxs-lookup"><span data-stu-id="79978-699">Format</span></span>

<span data-ttu-id="79978-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-701">Pattern</span></span>

<span data-ttu-id="79978-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="79978-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="79978-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="79978-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="79978-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-705">Checksum</span></span>

<span data-ttu-id="79978-706">Non</span><span class="sxs-lookup"><span data-stu-id="79978-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-707">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-707">Definition</span></span>

<span data-ttu-id="79978-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-709">L’expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-711">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-711">Keywords</span></span>

<span data-ttu-id="79978-712">| |</span><span class="sxs-lookup"><span data-stu-id="79978-712">| |</span></span>
|<span data-ttu-id="79978-713">**Keywords_slovakia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-714">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-714">dl#</span></span>  <br/> <span data-ttu-id="79978-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-715">driver license</span></span>  <br/> <span data-ttu-id="79978-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-716">driver license number</span></span>  <br/> <span data-ttu-id="79978-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-717">driver licence</span></span>  <br/> <span data-ttu-id="79978-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-718">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-719">drivers license</span></span>  <br/> <span data-ttu-id="79978-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-720">drivers licence</span></span>  <br/> <span data-ttu-id="79978-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-721">driver's license</span></span>  <br/> <span data-ttu-id="79978-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-722">driver's license number</span></span>  <br/> <span data-ttu-id="79978-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-723">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-724">driving license number</span></span>  <br/> <span data-ttu-id="79978-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-725">dlno#</span></span>  <br/> <span data-ttu-id="79978-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="79978-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="79978-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="79978-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="79978-728">Format</span><span class="sxs-lookup"><span data-stu-id="79978-728">Format</span></span>

<span data-ttu-id="79978-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="79978-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-730">Pattern</span></span>

<span data-ttu-id="79978-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="79978-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-732">Checksum</span></span>

<span data-ttu-id="79978-733">Non</span><span class="sxs-lookup"><span data-stu-id="79978-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-734">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-734">Definition</span></span>

<span data-ttu-id="79978-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-736">L’expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-738">Keywords</span></span>

<span data-ttu-id="79978-739">| |</span><span class="sxs-lookup"><span data-stu-id="79978-739">| |</span></span>
|<span data-ttu-id="79978-740">**Keywords_slovenia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-741">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-741">dl#</span></span>  <br/> <span data-ttu-id="79978-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-742">driver license</span></span>  <br/> <span data-ttu-id="79978-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-743">driver license number</span></span>  <br/> <span data-ttu-id="79978-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-744">driver licence</span></span>  <br/> <span data-ttu-id="79978-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-745">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-746">drivers license</span></span>  <br/> <span data-ttu-id="79978-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-747">drivers licence</span></span>  <br/> <span data-ttu-id="79978-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-748">driver's license</span></span>  <br/> <span data-ttu-id="79978-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-749">driver's license number</span></span>  <br/> <span data-ttu-id="79978-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-750">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-751">driving license number</span></span>  <br/> <span data-ttu-id="79978-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-752">dlno#</span></span>  <br/> <span data-ttu-id="79978-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="79978-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="79978-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="79978-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="79978-755">Format</span><span class="sxs-lookup"><span data-stu-id="79978-755">Format</span></span>

<span data-ttu-id="79978-756">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="79978-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-757">Pattern</span></span>

<span data-ttu-id="79978-758">Huit chiffres suivis d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="79978-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="79978-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-759">Eight digits</span></span> 
    
- <span data-ttu-id="79978-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="79978-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-761">Checksum</span></span>

<span data-ttu-id="79978-762">Oui</span><span class="sxs-lookup"><span data-stu-id="79978-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-763">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-763">Definition</span></span>

<span data-ttu-id="79978-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="79978-767">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-767">Keywords</span></span>

<span data-ttu-id="79978-768">| |</span><span class="sxs-lookup"><span data-stu-id="79978-768">| |</span></span>
|<span data-ttu-id="79978-769">**Keywords_spain_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-770">dlno#</span></span>  <br/> <span data-ttu-id="79978-771">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-771">dl#</span></span>  <br/> <span data-ttu-id="79978-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-772">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-773">driver licence</span></span>  <br/> <span data-ttu-id="79978-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-774">driver license</span></span>  <br/> <span data-ttu-id="79978-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-775">drivers licence</span></span>  <br/> <span data-ttu-id="79978-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-776">drivers license</span></span>  <br/> <span data-ttu-id="79978-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-777">driver's licence</span></span>  <br/> <span data-ttu-id="79978-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-778">driver's license</span></span>  <br/> <span data-ttu-id="79978-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-779">driving licence</span></span>  <br/> <span data-ttu-id="79978-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-780">driving license</span></span>  <br/> <span data-ttu-id="79978-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-781">driver licence number</span></span>  <br/> <span data-ttu-id="79978-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-782">driver license number</span></span>  <br/> <span data-ttu-id="79978-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-783">drivers licence number</span></span>  <br/> <span data-ttu-id="79978-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-784">drivers license number</span></span>  <br/> <span data-ttu-id="79978-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-785">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-786">driver's license number</span></span>  <br/> <span data-ttu-id="79978-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-787">driving licence number</span></span>  <br/> <span data-ttu-id="79978-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-788">driving license number</span></span>  <br/> <span data-ttu-id="79978-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-789">driving permit</span></span>  <br/> <span data-ttu-id="79978-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-790">driving permit number</span></span>  <br/> <span data-ttu-id="79978-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="79978-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="79978-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="79978-792">permiso conducción</span></span>  <br/> <span data-ttu-id="79978-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="79978-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="79978-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="79978-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="79978-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="79978-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="79978-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="79978-796">licencia conducir</span></span>  <br/> <span data-ttu-id="79978-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="79978-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="79978-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="79978-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="79978-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="79978-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="79978-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="79978-800">permiso conducir</span></span>  <br/> <span data-ttu-id="79978-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="79978-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="79978-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="79978-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="79978-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="79978-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="79978-804">Suède</span><span class="sxs-lookup"><span data-stu-id="79978-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="79978-805">Format</span><span class="sxs-lookup"><span data-stu-id="79978-805">Format</span></span>

<span data-ttu-id="79978-806">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="79978-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="79978-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="79978-807">Pattern</span></span>

<span data-ttu-id="79978-808">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="79978-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="79978-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-809">Six digits</span></span> 
    
- <span data-ttu-id="79978-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="79978-810">A hyphen</span></span>
    
- <span data-ttu-id="79978-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="79978-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="79978-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="79978-812">Checksum</span></span>

<span data-ttu-id="79978-813">Non</span><span class="sxs-lookup"><span data-stu-id="79978-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="79978-814">Définition</span><span class="sxs-lookup"><span data-stu-id="79978-814">Definition</span></span>

<span data-ttu-id="79978-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="79978-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="79978-816">L’expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="79978-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="79978-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="79978-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="79978-818">Mots clés</span><span class="sxs-lookup"><span data-stu-id="79978-818">Keywords</span></span>

<span data-ttu-id="79978-819">| |</span><span class="sxs-lookup"><span data-stu-id="79978-819">| |</span></span>
|<span data-ttu-id="79978-820">**Keywords_sweden_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="79978-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="79978-821">LD #</span><span class="sxs-lookup"><span data-stu-id="79978-821">dl#</span></span>  <br/> <span data-ttu-id="79978-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-822">driver license</span></span>  <br/> <span data-ttu-id="79978-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-823">driver license number</span></span>  <br/> <span data-ttu-id="79978-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-824">driver licence</span></span>  <br/> <span data-ttu-id="79978-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="79978-825">drivers lic.</span></span>  <br/> <span data-ttu-id="79978-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-826">drivers license</span></span>  <br/> <span data-ttu-id="79978-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-827">drivers licence</span></span>  <br/> <span data-ttu-id="79978-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-828">driver's license</span></span>  <br/> <span data-ttu-id="79978-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-829">driver's license number</span></span>  <br/> <span data-ttu-id="79978-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-830">driver's licence number</span></span>  <br/> <span data-ttu-id="79978-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="79978-831">driving license number</span></span>  <br/> <span data-ttu-id="79978-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="79978-832">dlno#</span></span>  <br/> <span data-ttu-id="79978-833">körkort</span><span class="sxs-lookup"><span data-stu-id="79978-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="79978-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="79978-834">UK</span></span>

<span data-ttu-id="79978-835">Pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="79978-835">For details, see the section "U.K.</span></span> <span data-ttu-id="79978-836">Numéro de permis de conduire» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="79978-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79978-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79978-837">See also</span></span>

[<span data-ttu-id="79978-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="79978-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

