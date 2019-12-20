---
title: Numéro de permis de conduire de l’UE
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
ms.openlocfilehash: 6df025caf8d06c617e09a3b53dc6c82d69aaf5a8
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40805957"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="a53e0-104">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="a53e0-104">EU Driver's License Number</span></span>

<span data-ttu-id="a53e0-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du pilote de l’UE.</span><span class="sxs-lookup"><span data-stu-id="a53e0-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="a53e0-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="a53e0-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a53e0-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="a53e0-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-108">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-108">Format</span></span>

<span data-ttu-id="a53e0-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-110">Pattern</span></span>

<span data-ttu-id="a53e0-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-112">Checksum</span></span>

<span data-ttu-id="a53e0-113">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-114">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-114">Definition</span></span>

<span data-ttu-id="a53e0-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-116">L’expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="a53e0-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-118">Keywords</span></span>

<span data-ttu-id="a53e0-119">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-119"></span></span>
|<span data-ttu-id="a53e0-120">**Keywords_austria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-121">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-121">dl#</span></span>  <br/> <span data-ttu-id="a53e0-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-122">driver license</span></span>  <br/> <span data-ttu-id="a53e0-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-123">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-124">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-125">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-126">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-127">driver's licence</span></span>  <br/> <span data-ttu-id="a53e0-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-128">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-129">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="a53e0-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-131">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-132">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a53e0-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="a53e0-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="a53e0-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a53e0-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="a53e0-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-136">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-136">Format</span></span>

<span data-ttu-id="a53e0-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-138">Pattern</span></span>

<span data-ttu-id="a53e0-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-140">Checksum</span></span>

<span data-ttu-id="a53e0-141">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-142">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-142">Definition</span></span>

<span data-ttu-id="a53e0-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-144">L’expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a53e0-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-146">Keywords</span></span>

<span data-ttu-id="a53e0-147">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-147"></span></span>
|<span data-ttu-id="a53e0-148">**Keywords__belgium_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-149">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-149">dl#</span></span>  <br/> <span data-ttu-id="a53e0-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-150">driver license</span></span>  <br/> <span data-ttu-id="a53e0-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-151">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-152">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-153">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-154">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-155">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-156">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-157">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-158">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-159">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a53e0-160">rijbewijs</span></span>  <br/> <span data-ttu-id="a53e0-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="a53e0-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="a53e0-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="a53e0-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="a53e0-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a53e0-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="a53e0-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a53e0-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="a53e0-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a53e0-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a53e0-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="a53e0-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-169">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-169">Format</span></span>

<span data-ttu-id="a53e0-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-171">Pattern</span></span>

<span data-ttu-id="a53e0-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-173">Checksum</span></span>

<span data-ttu-id="a53e0-174">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-175">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-175">Definition</span></span>

<span data-ttu-id="a53e0-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-177">L’expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="a53e0-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-179">Keywords</span></span>

<span data-ttu-id="a53e0-180">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-180"></span></span>
|<span data-ttu-id="a53e0-181">**Keywords_bulgaria_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-182">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-182">dl#</span></span>  <br/> <span data-ttu-id="a53e0-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-183">driver license</span></span>  <br/> <span data-ttu-id="a53e0-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-184">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-185">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-186">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-187">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-188">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-189">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-190">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-191">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-192">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-193">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="a53e0-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="a53e0-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="a53e0-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="a53e0-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="a53e0-196">сумпс</span></span>  <br/> <span data-ttu-id="a53e0-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="a53e0-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a53e0-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="a53e0-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-199">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-199">Format</span></span>

<span data-ttu-id="a53e0-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-201">Pattern</span></span>

<span data-ttu-id="a53e0-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-203">Checksum</span></span>

<span data-ttu-id="a53e0-204">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-205">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-205">Definition</span></span>

<span data-ttu-id="a53e0-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-207">L’expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a53e0-209">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-209">Keywords</span></span>

<span data-ttu-id="a53e0-210">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-210"></span></span>
|<span data-ttu-id="a53e0-211">**Keywords_croatia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-212">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-212">dl#</span></span>  <br/> <span data-ttu-id="a53e0-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-213">driver license</span></span>  <br/> <span data-ttu-id="a53e0-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-214">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-215">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-216">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-217">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-218">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-219">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-220">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-221">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-222">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-223">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="a53e0-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a53e0-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="a53e0-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-226">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-226">Format</span></span>

<span data-ttu-id="a53e0-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-228">Pattern</span></span>

<span data-ttu-id="a53e0-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-230">Checksum</span></span>

<span data-ttu-id="a53e0-231">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-232">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-232">Definition</span></span>

<span data-ttu-id="a53e0-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-234">L’expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-236">Keywords</span></span>

<span data-ttu-id="a53e0-237">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-237"></span></span>
|<span data-ttu-id="a53e0-238">**Keywords_cyprus_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-239">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-239">dl#</span></span>  <br/> <span data-ttu-id="a53e0-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-240">driver license</span></span>  <br/> <span data-ttu-id="a53e0-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-241">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-242">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-243">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-244">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-245">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-246">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-247">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-248">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-249">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a53e0-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a53e0-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="a53e0-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-252">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-252">Format</span></span>

<span data-ttu-id="a53e0-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-254">Pattern</span></span>

<span data-ttu-id="a53e0-255">Huit lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="a53e0-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="a53e0-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="a53e0-257">A space (optional)</span></span>
    
- <span data-ttu-id="a53e0-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-259">Checksum</span></span>

<span data-ttu-id="a53e0-260">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-261">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-261">Definition</span></span>

<span data-ttu-id="a53e0-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-263">L’expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a53e0-265">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-265">Keywords</span></span>

<span data-ttu-id="a53e0-266">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-266"></span></span>
|<span data-ttu-id="a53e0-267">**Keywords_czech_republic_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-268">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-268">dl#</span></span>  <br/> <span data-ttu-id="a53e0-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-269">driver license</span></span>  <br/> <span data-ttu-id="a53e0-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-270">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-271">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-272">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-273">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-274">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-275">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-276">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-277">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-278">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-279">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-280">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="a53e0-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a53e0-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="a53e0-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-283">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-283">Format</span></span>

<span data-ttu-id="a53e0-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-285">Pattern</span></span>

<span data-ttu-id="a53e0-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-287">Checksum</span></span>

<span data-ttu-id="a53e0-288">Oui</span><span class="sxs-lookup"><span data-stu-id="a53e0-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-289">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-289">Definition</span></span>

<span data-ttu-id="a53e0-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-291">L’expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a53e0-293">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-293">Keywords</span></span>

<span data-ttu-id="a53e0-294">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-294"></span></span>
|<span data-ttu-id="a53e0-295">**Keywords_denmark_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-296">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-296">dl#</span></span>  <br/> <span data-ttu-id="a53e0-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-297">driver license</span></span>  <br/> <span data-ttu-id="a53e0-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-298">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-299">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-300">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-301">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-302">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-303">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-304">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-305">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-306">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-307">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="a53e0-308">kørekort</span></span>  <br/> <span data-ttu-id="a53e0-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a53e0-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="a53e0-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-311">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-311">Format</span></span>

<span data-ttu-id="a53e0-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-313">Pattern</span></span>

<span data-ttu-id="a53e0-314">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a53e0-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a53e0-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-317">Checksum</span></span>

<span data-ttu-id="a53e0-318">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-319">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-319">Definition</span></span>

<span data-ttu-id="a53e0-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-321">L’expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-323">Keywords</span></span>

<span data-ttu-id="a53e0-324">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-324"></span></span>
|<span data-ttu-id="a53e0-325">**Keywords_estonia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-326">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-326">dl#</span></span>  <br/> <span data-ttu-id="a53e0-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-327">driver license</span></span>  <br/> <span data-ttu-id="a53e0-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-328">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-329">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-330">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-331">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-332">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-333">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-334">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-335">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-336">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-337">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a53e0-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="a53e0-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-340">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-340">Format</span></span>

<span data-ttu-id="a53e0-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="a53e0-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-342">Pattern</span></span>

<span data-ttu-id="a53e0-343">10 chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="a53e0-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a53e0-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-344">Six digits</span></span> 
    
- <span data-ttu-id="a53e0-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="a53e0-345">A hyphen</span></span>
    
-  <span data-ttu-id="a53e0-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a53e0-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-347">Checksum</span></span>

<span data-ttu-id="a53e0-348">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-349">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-349">Definition</span></span>

<span data-ttu-id="a53e0-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-351">L’expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-353">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-353">Keywords</span></span>

<span data-ttu-id="a53e0-354">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-354"></span></span>
|<span data-ttu-id="a53e0-355">**Keywords_finland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-356">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-356">dl#</span></span>  <br/> <span data-ttu-id="a53e0-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-357">driver license</span></span>  <br/> <span data-ttu-id="a53e0-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-358">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-359">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-360">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-361">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-362">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-363">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-364">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-365">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-366">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-367">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="a53e0-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="a53e0-369">France</span><span class="sxs-lookup"><span data-stu-id="a53e0-369">France</span></span>

<span data-ttu-id="a53e0-370">Pour plus d’informations, reportez-vous à la section « numéro de permis de conduire France » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a53e0-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a53e0-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="a53e0-371">Germany</span></span>

<span data-ttu-id="a53e0-372">Pour plus d’informations, consultez la section « numéro de permis de conduire allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a53e0-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a53e0-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="a53e0-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-374">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-374">Format</span></span>

<span data-ttu-id="a53e0-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-376">Pattern</span></span>

 <span data-ttu-id="a53e0-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a53e0-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-378">Checksum</span></span>

<span data-ttu-id="a53e0-379">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-380">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-380">Definition</span></span>

<span data-ttu-id="a53e0-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-382">L’expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-384">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-384">Keywords</span></span>

<span data-ttu-id="a53e0-385">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-385"></span></span>
|<span data-ttu-id="a53e0-386">**Keywords_greece_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-387">Fichier #</span><span class="sxs-lookup"><span data-stu-id="a53e0-387">dlL#</span></span>  <br/> <span data-ttu-id="a53e0-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-388">driver license</span></span>  <br/> <span data-ttu-id="a53e0-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-389">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-390">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-391">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-392">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-393">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-394">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-395">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-396">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-397">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-398">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a53e0-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="a53e0-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="a53e0-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a53e0-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="a53e0-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-402">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-402">Format</span></span>

<span data-ttu-id="a53e0-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-404">Pattern</span></span>

<span data-ttu-id="a53e0-405">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a53e0-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a53e0-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-408">Checksum</span></span>

<span data-ttu-id="a53e0-409">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-410">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-410">Definition</span></span>

<span data-ttu-id="a53e0-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-412">L’expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-414">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-414">Keywords</span></span>

<span data-ttu-id="a53e0-415">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-415"></span></span>
|<span data-ttu-id="a53e0-416">**Keywords_hungary_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-417">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-417">dl#</span></span>  <br/> <span data-ttu-id="a53e0-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-418">driver license</span></span>  <br/> <span data-ttu-id="a53e0-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-419">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-420">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-421">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-422">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-423">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-424">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-425">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-426">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-427">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-428">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="a53e0-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a53e0-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="a53e0-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-431">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-431">Format</span></span>

<span data-ttu-id="a53e0-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="a53e0-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-433">Pattern</span></span>

<span data-ttu-id="a53e0-434">Six chiffres et quatre lettres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="a53e0-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-435">Six digits</span></span>
    
- <span data-ttu-id="a53e0-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-437">Checksum</span></span>

<span data-ttu-id="a53e0-438">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-439">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-439">Definition</span></span>

<span data-ttu-id="a53e0-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-441">L’expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-443">Keywords</span></span>

<span data-ttu-id="a53e0-444">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-444"></span></span>
|<span data-ttu-id="a53e0-445">**Keywords_ireland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-446">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-446">dl#</span></span>  <br/> <span data-ttu-id="a53e0-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-447">driver license</span></span>  <br/> <span data-ttu-id="a53e0-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-448">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-449">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-450">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-451">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-452">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-453">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-454">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-455">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-456">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-457">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="a53e0-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a53e0-459">Italie</span><span class="sxs-lookup"><span data-stu-id="a53e0-459">Italy</span></span>

<span data-ttu-id="a53e0-460">Pour plus d’informations, reportez-vous à la section « Italie numéro de permis de conduire » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a53e0-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="a53e0-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="a53e0-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-462">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-462">Format</span></span>

<span data-ttu-id="a53e0-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-464">Pattern</span></span>

<span data-ttu-id="a53e0-465">Trois lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="a53e0-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a53e0-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-468">Checksum</span></span>

<span data-ttu-id="a53e0-469">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-470">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-470">Definition</span></span>

<span data-ttu-id="a53e0-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-472">L’expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-474">Keywords</span></span>

<span data-ttu-id="a53e0-475">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-475"></span></span>
|<span data-ttu-id="a53e0-476">**Keywords_latvia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-477">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-477">dl#</span></span>  <br/> <span data-ttu-id="a53e0-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-478">driver license</span></span>  <br/> <span data-ttu-id="a53e0-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-479">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-480">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-481">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-482">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-483">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-484">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-485">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-486">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-487">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-488">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="a53e0-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a53e0-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="a53e0-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-491">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-491">Format</span></span>

<span data-ttu-id="a53e0-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-493">Pattern</span></span>

 <span data-ttu-id="a53e0-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a53e0-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-495">Checksum</span></span>

<span data-ttu-id="a53e0-496">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-497">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-497">Definition</span></span>

<span data-ttu-id="a53e0-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-499">L’expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-501">Keywords</span></span>

<span data-ttu-id="a53e0-502">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-502"></span></span>
|<span data-ttu-id="a53e0-503">**Keywords_lithuania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-504">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-504">dl#</span></span>  <br/> <span data-ttu-id="a53e0-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-505">driver license</span></span>  <br/> <span data-ttu-id="a53e0-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-506">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-507">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-508">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-509">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-510">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-511">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-512">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-513">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-514">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-515">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="a53e0-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a53e0-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="a53e0-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-518">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-518">Format</span></span>

<span data-ttu-id="a53e0-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-520">Pattern</span></span>

 <span data-ttu-id="a53e0-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a53e0-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-522">Checksum</span></span>

<span data-ttu-id="a53e0-523">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-524">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-524">Definition</span></span>

<span data-ttu-id="a53e0-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-526">L’expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-528">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-528">Keywords</span></span>

<span data-ttu-id="a53e0-529">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-529"></span></span>
|<span data-ttu-id="a53e0-530">**Keywords_luxemburg_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-531">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-531">dl#</span></span>  <br/> <span data-ttu-id="a53e0-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-532">driver license</span></span>  <br/> <span data-ttu-id="a53e0-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-533">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-534">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-535">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-536">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-537">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-538">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-539">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-540">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-541">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-542">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="a53e0-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a53e0-544">Malte</span><span class="sxs-lookup"><span data-stu-id="a53e0-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-545">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-545">Format</span></span>

<span data-ttu-id="a53e0-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="a53e0-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-547">Pattern</span></span>

<span data-ttu-id="a53e0-548">Combinaison de deux caractères et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="a53e0-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="a53e0-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="a53e0-550">A space (optional)</span></span>
    
- <span data-ttu-id="a53e0-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-551">Three digits</span></span>
    
- <span data-ttu-id="a53e0-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="a53e0-552">A space (optional)</span></span>
    
- <span data-ttu-id="a53e0-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-554">Checksum</span></span>

<span data-ttu-id="a53e0-555">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-556">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-556">Definition</span></span>

<span data-ttu-id="a53e0-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-558">L’expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-560">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-560">Keywords</span></span>

<span data-ttu-id="a53e0-561">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-561"></span></span>
|<span data-ttu-id="a53e0-562">**Keywords_malta_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-563">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-563">dl#</span></span>  <br/> <span data-ttu-id="a53e0-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-564">driver license</span></span>  <br/> <span data-ttu-id="a53e0-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-565">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-566">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-567">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-568">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-569">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-570">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-571">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-572">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-573">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-574">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="a53e0-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a53e0-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="a53e0-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-577">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-577">Format</span></span>

<span data-ttu-id="a53e0-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-579">Pattern</span></span>

<span data-ttu-id="a53e0-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-581">Checksum</span></span>

<span data-ttu-id="a53e0-582">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-583">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-583">Definition</span></span>

<span data-ttu-id="a53e0-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-585">L’expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-587">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-587">Keywords</span></span>

<span data-ttu-id="a53e0-588">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-588"></span></span>
|<span data-ttu-id="a53e0-589">**Keywords_netherlands_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-590">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-590">dl#</span></span>  <br/> <span data-ttu-id="a53e0-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-591">driver license</span></span>  <br/> <span data-ttu-id="a53e0-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-592">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-593">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-594">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-595">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-596">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-597">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-598">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-599">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-600">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-601">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-602">permis de conduire</span></span>  <br/> <span data-ttu-id="a53e0-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a53e0-603">rijbewijs</span></span>  <br/> <span data-ttu-id="a53e0-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a53e0-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a53e0-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="a53e0-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-606">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-606">Format</span></span>

<span data-ttu-id="a53e0-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="a53e0-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-608">Pattern</span></span>

<span data-ttu-id="a53e0-609">14 chiffres et 2 barres obliques :</span><span class="sxs-lookup"><span data-stu-id="a53e0-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="a53e0-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-610">Five digits</span></span> 
    
- <span data-ttu-id="a53e0-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="a53e0-611">A forward slash</span></span>
    
- <span data-ttu-id="a53e0-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-612">Two digits</span></span>
    
- <span data-ttu-id="a53e0-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="a53e0-613">A forward slash</span></span>
    
- <span data-ttu-id="a53e0-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-615">Checksum</span></span>

<span data-ttu-id="a53e0-616">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-617">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-617">Definition</span></span>

<span data-ttu-id="a53e0-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-619">L’expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-621">Keywords</span></span>

<span data-ttu-id="a53e0-622">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-622"></span></span>
|<span data-ttu-id="a53e0-623">**Keywords_poland_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-624">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-624">dl#</span></span>  <br/> <span data-ttu-id="a53e0-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-625">driver license</span></span>  <br/> <span data-ttu-id="a53e0-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-626">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-627">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-628">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-629">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-630">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-631">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-632">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-633">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-634">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-635">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="a53e0-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="a53e0-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="a53e0-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-638">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-638">Format</span></span>

<span data-ttu-id="a53e0-639">Deux lettres suivies d’un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="a53e0-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-640">Pattern</span></span>

<span data-ttu-id="a53e0-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux :</span><span class="sxs-lookup"><span data-stu-id="a53e0-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="a53e0-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a53e0-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="a53e0-643">A hyphen</span></span>
    
- <span data-ttu-id="a53e0-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-644">Six digits</span></span>
    
- <span data-ttu-id="a53e0-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="a53e0-645">A space</span></span>
    
- <span data-ttu-id="a53e0-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="a53e0-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-647">Checksum</span></span>

<span data-ttu-id="a53e0-648">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-649">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-649">Definition</span></span>

<span data-ttu-id="a53e0-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-651">L’expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-653">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-653">Keywords</span></span>

<span data-ttu-id="a53e0-654">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-654"></span></span>
|<span data-ttu-id="a53e0-655">**Keywords_portugal_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-656">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-656">dl#</span></span>  <br/> <span data-ttu-id="a53e0-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-657">driver license</span></span>  <br/> <span data-ttu-id="a53e0-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-658">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-659">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-660">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-661">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-662">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-663">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-664">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-665">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-666">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-667">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a53e0-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a53e0-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="a53e0-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-670">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-670">Format</span></span>

<span data-ttu-id="a53e0-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-672">Pattern</span></span>

<span data-ttu-id="a53e0-673">Un caractère suivi de huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="a53e0-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="a53e0-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="a53e0-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="a53e0-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-676">Checksum</span></span>

<span data-ttu-id="a53e0-677">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-678">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-678">Definition</span></span>

<span data-ttu-id="a53e0-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-680">L’expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-682">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-682">Keywords</span></span>

<span data-ttu-id="a53e0-683">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-683"></span></span>
|<span data-ttu-id="a53e0-684">**Keywords_romania_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-685">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-685">dl#</span></span>  <br/> <span data-ttu-id="a53e0-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-686">driver license</span></span>  <br/> <span data-ttu-id="a53e0-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-687">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-688">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-689">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-690">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-691">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-692">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-693">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-694">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-695">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-696">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="a53e0-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a53e0-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="a53e0-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-699">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-699">Format</span></span>

<span data-ttu-id="a53e0-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-701">Pattern</span></span>

<span data-ttu-id="a53e0-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="a53e0-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="a53e0-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="a53e0-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a53e0-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-705">Checksum</span></span>

<span data-ttu-id="a53e0-706">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-707">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-707">Definition</span></span>

<span data-ttu-id="a53e0-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-709">L’expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-711">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-711">Keywords</span></span>

<span data-ttu-id="a53e0-712">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-712"></span></span>
|<span data-ttu-id="a53e0-713">**Keywords_slovakia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-714">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-714">dl#</span></span>  <br/> <span data-ttu-id="a53e0-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-715">driver license</span></span>  <br/> <span data-ttu-id="a53e0-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-716">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-717">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-718">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-719">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-720">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-721">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-722">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-723">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-724">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-725">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="a53e0-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a53e0-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="a53e0-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-728">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-728">Format</span></span>

<span data-ttu-id="a53e0-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a53e0-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-730">Pattern</span></span>

<span data-ttu-id="a53e0-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a53e0-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-732">Checksum</span></span>

<span data-ttu-id="a53e0-733">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-734">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-734">Definition</span></span>

<span data-ttu-id="a53e0-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-736">L’expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-738">Keywords</span></span>

<span data-ttu-id="a53e0-739">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-739"></span></span>
|<span data-ttu-id="a53e0-740">**Keywords_slovenia_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-741">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-741">dl#</span></span>  <br/> <span data-ttu-id="a53e0-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-742">driver license</span></span>  <br/> <span data-ttu-id="a53e0-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-743">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-744">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-745">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-746">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-747">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-748">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-749">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-750">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-751">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-752">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="a53e0-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a53e0-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="a53e0-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-755">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-755">Format</span></span>

<span data-ttu-id="a53e0-756">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="a53e0-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-757">Pattern</span></span>

<span data-ttu-id="a53e0-758">Huit chiffres suivis d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="a53e0-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="a53e0-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-759">Eight digits</span></span> 
    
- <span data-ttu-id="a53e0-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a53e0-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-761">Checksum</span></span>

<span data-ttu-id="a53e0-762">Oui</span><span class="sxs-lookup"><span data-stu-id="a53e0-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-763">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-763">Definition</span></span>

<span data-ttu-id="a53e0-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a53e0-767">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-767">Keywords</span></span>

<span data-ttu-id="a53e0-768">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-768"></span></span>
|<span data-ttu-id="a53e0-769">**Keywords_spain_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-770">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-771">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-771">dl#</span></span>  <br/> <span data-ttu-id="a53e0-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-772">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-773">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-774">driver license</span></span>  <br/> <span data-ttu-id="a53e0-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-775">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-776">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-777">driver's licence</span></span>  <br/> <span data-ttu-id="a53e0-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-778">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-779">driving licence</span></span>  <br/> <span data-ttu-id="a53e0-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-780">driving license</span></span>  <br/> <span data-ttu-id="a53e0-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-781">driver licence number</span></span>  <br/> <span data-ttu-id="a53e0-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-782">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-783">drivers licence number</span></span>  <br/> <span data-ttu-id="a53e0-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-784">drivers license number</span></span>  <br/> <span data-ttu-id="a53e0-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-785">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-786">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-787">driving licence number</span></span>  <br/> <span data-ttu-id="a53e0-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-788">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-789">driving permit</span></span>  <br/> <span data-ttu-id="a53e0-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-790">driving permit number</span></span>  <br/> <span data-ttu-id="a53e0-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="a53e0-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="a53e0-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="a53e0-792">permiso conducción</span></span>  <br/> <span data-ttu-id="a53e0-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="a53e0-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="a53e0-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="a53e0-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="a53e0-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-796">licencia conducir</span></span>  <br/> <span data-ttu-id="a53e0-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="a53e0-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="a53e0-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="a53e0-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-800">permiso conducir</span></span>  <br/> <span data-ttu-id="a53e0-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="a53e0-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="a53e0-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="a53e0-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="a53e0-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a53e0-804">Suède</span><span class="sxs-lookup"><span data-stu-id="a53e0-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="a53e0-805">Format</span><span class="sxs-lookup"><span data-stu-id="a53e0-805">Format</span></span>

<span data-ttu-id="a53e0-806">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="a53e0-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a53e0-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="a53e0-807">Pattern</span></span>

<span data-ttu-id="a53e0-808">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="a53e0-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a53e0-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-809">Six digits</span></span> 
    
- <span data-ttu-id="a53e0-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="a53e0-810">A hyphen</span></span>
    
- <span data-ttu-id="a53e0-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="a53e0-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a53e0-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a53e0-812">Checksum</span></span>

<span data-ttu-id="a53e0-813">Non</span><span class="sxs-lookup"><span data-stu-id="a53e0-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a53e0-814">Définition</span><span class="sxs-lookup"><span data-stu-id="a53e0-814">Definition</span></span>

<span data-ttu-id="a53e0-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a53e0-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a53e0-816">L’expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a53e0-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a53e0-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a53e0-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="a53e0-818">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a53e0-818">Keywords</span></span>

<span data-ttu-id="a53e0-819">| |</span><span class="sxs-lookup"><span data-stu-id="a53e0-819"></span></span>
|<span data-ttu-id="a53e0-820">**Keywords_sweden_eu_driver’s_license_number**</span><span class="sxs-lookup"><span data-stu-id="a53e0-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a53e0-821">LD #</span><span class="sxs-lookup"><span data-stu-id="a53e0-821">dl#</span></span>  <br/> <span data-ttu-id="a53e0-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-822">driver license</span></span>  <br/> <span data-ttu-id="a53e0-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-823">driver license number</span></span>  <br/> <span data-ttu-id="a53e0-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-824">driver licence</span></span>  <br/> <span data-ttu-id="a53e0-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="a53e0-825">drivers lic.</span></span>  <br/> <span data-ttu-id="a53e0-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-826">drivers license</span></span>  <br/> <span data-ttu-id="a53e0-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-827">drivers licence</span></span>  <br/> <span data-ttu-id="a53e0-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-828">driver's license</span></span>  <br/> <span data-ttu-id="a53e0-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-829">driver's license number</span></span>  <br/> <span data-ttu-id="a53e0-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-830">driver's licence number</span></span>  <br/> <span data-ttu-id="a53e0-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a53e0-831">driving license number</span></span>  <br/> <span data-ttu-id="a53e0-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="a53e0-832">dlno#</span></span>  <br/> <span data-ttu-id="a53e0-833">körkort</span><span class="sxs-lookup"><span data-stu-id="a53e0-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="a53e0-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="a53e0-834">UK</span></span>

<span data-ttu-id="a53e0-835">Pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="a53e0-835">For details, see the section "U.K.</span></span> <span data-ttu-id="a53e0-836">Numéro de permis de conduire» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a53e0-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a53e0-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a53e0-837">See also</span></span>

[<span data-ttu-id="a53e0-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a53e0-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

