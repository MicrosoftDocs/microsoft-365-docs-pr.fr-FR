---
title: Numéro de passeport UE
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 4afcf7b764eb8976e0588464515256f7cb1bdb8d
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40805947"
---
# <a name="eu-passport-number"></a><span data-ttu-id="4e329-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="4e329-104">EU Passport Number</span></span>

<span data-ttu-id="4e329-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE.</span><span class="sxs-lookup"><span data-stu-id="4e329-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="4e329-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="4e329-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="4e329-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="4e329-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="4e329-108">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-108">Format</span></span>

<span data-ttu-id="4e329-109">Une lettre suivie d’un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-110">Pattern</span></span>

<span data-ttu-id="4e329-111">Une combinaison d’une lettre, de sept chiffres et d’un espace :</span><span class="sxs-lookup"><span data-stu-id="4e329-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="4e329-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="4e329-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4e329-113">One space (optional)</span></span>
    
- <span data-ttu-id="4e329-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-115">Checksum</span></span>

<span data-ttu-id="4e329-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-117">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-117">Definition</span></span>

<span data-ttu-id="4e329-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-119">L’expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-121">Keywords</span></span>

<span data-ttu-id="4e329-122">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-122"></span></span>
|<span data-ttu-id="4e329-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-124">passport number</span></span>  <br/> <span data-ttu-id="4e329-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="4e329-125">austrian passport number</span></span>  <br/> <span data-ttu-id="4e329-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-126">passport no</span></span>  <br/> <span data-ttu-id="4e329-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="4e329-127">reisepass</span></span>  <br/> <span data-ttu-id="4e329-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="4e329-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="4e329-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="4e329-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="4e329-130">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-130">Format</span></span>

<span data-ttu-id="4e329-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-132">Pattern</span></span>

<span data-ttu-id="4e329-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-134">Checksum</span></span>

<span data-ttu-id="4e329-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-136">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-136">Definition</span></span>

<span data-ttu-id="4e329-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-138">L’expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-140">Keywords</span></span>

<span data-ttu-id="4e329-141">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-141"></span></span>
|<span data-ttu-id="4e329-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-143">passport number</span></span>  <br/> <span data-ttu-id="4e329-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="4e329-144">belgian passport number</span></span>  <br/> <span data-ttu-id="4e329-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-145">passport no</span></span>  <br/> <span data-ttu-id="4e329-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="4e329-146">paspoort</span></span>  <br/> <span data-ttu-id="4e329-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="4e329-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="4e329-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="4e329-148">reisepass kein</span></span>  <br/> <span data-ttu-id="4e329-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="4e329-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="4e329-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="4e329-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="4e329-151">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-151">Format</span></span>

<span data-ttu-id="4e329-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-153">Pattern</span></span>

 <span data-ttu-id="4e329-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4e329-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-155">Checksum</span></span>

<span data-ttu-id="4e329-156">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-157">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-157">Definition</span></span>

<span data-ttu-id="4e329-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-159">L’expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-161">Keywords</span></span>

<span data-ttu-id="4e329-162">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-162"></span></span>
|<span data-ttu-id="4e329-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-164">passport number</span></span>  <br/> <span data-ttu-id="4e329-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="4e329-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="4e329-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-166">passport no</span></span>  <br/> <span data-ttu-id="4e329-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="4e329-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="4e329-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="4e329-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="4e329-169">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-169">Format</span></span>

<span data-ttu-id="4e329-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-171">Pattern</span></span>

 <span data-ttu-id="4e329-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4e329-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-173">Checksum</span></span>

<span data-ttu-id="4e329-174">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-175">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-175">Definition</span></span>

<span data-ttu-id="4e329-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-177">L’expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-179">Keywords</span></span>

<span data-ttu-id="4e329-180">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-180"></span></span>
|<span data-ttu-id="4e329-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-182">passport number</span></span>  <br/> <span data-ttu-id="4e329-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="4e329-183">croatian passport number</span></span>  <br/> <span data-ttu-id="4e329-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-184">passport no</span></span>  <br/> <span data-ttu-id="4e329-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="4e329-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="4e329-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="4e329-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="4e329-187">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-187">Format</span></span>

<span data-ttu-id="4e329-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-189">Pattern</span></span>

<span data-ttu-id="4e329-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-191">Checksum</span></span>

<span data-ttu-id="4e329-192">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-193">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-193">Definition</span></span>

<span data-ttu-id="4e329-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-195">L’expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-197">Keywords</span></span>

<span data-ttu-id="4e329-198">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-198"></span></span>
|<span data-ttu-id="4e329-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-200">passport number</span></span>  <br/> <span data-ttu-id="4e329-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="4e329-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="4e329-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-202">passport no</span></span>  <br/> <span data-ttu-id="4e329-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="4e329-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="4e329-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="4e329-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="4e329-205">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-205">Format</span></span>

<span data-ttu-id="4e329-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-207">Pattern</span></span>

<span data-ttu-id="4e329-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-209">Checksum</span></span>

<span data-ttu-id="4e329-210">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-211">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-211">Definition</span></span>

<span data-ttu-id="4e329-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-213">L’expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-215">Keywords</span></span>

<span data-ttu-id="4e329-216">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-216"></span></span>
|<span data-ttu-id="4e329-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-218">passport number</span></span>  <br/> <span data-ttu-id="4e329-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="4e329-219">czech passport number</span></span>  <br/> <span data-ttu-id="4e329-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-220">passport no</span></span>  <br/> <span data-ttu-id="4e329-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="4e329-221">cestovní pas</span></span>  <br/> <span data-ttu-id="4e329-222">boîte</span><span class="sxs-lookup"><span data-stu-id="4e329-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="4e329-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="4e329-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="4e329-224">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-224">Format</span></span>

<span data-ttu-id="4e329-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-226">Pattern</span></span>

 <span data-ttu-id="4e329-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4e329-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-228">Checksum</span></span>

<span data-ttu-id="4e329-229">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-230">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-230">Definition</span></span>

<span data-ttu-id="4e329-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-232">L’expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-234">Keywords</span></span>

<span data-ttu-id="4e329-235">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-235"></span></span>
|<span data-ttu-id="4e329-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-237">passport number</span></span>  <br/> <span data-ttu-id="4e329-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="4e329-238">danish passport number</span></span>  <br/> <span data-ttu-id="4e329-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-239">passport no</span></span>  <br/> <span data-ttu-id="4e329-240">boîte</span><span class="sxs-lookup"><span data-stu-id="4e329-240">pas</span></span>  <br/> <span data-ttu-id="4e329-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="4e329-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="4e329-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="4e329-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="4e329-243">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-243">Format</span></span>

<span data-ttu-id="4e329-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-245">Pattern</span></span>

<span data-ttu-id="4e329-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-247">Checksum</span></span>

<span data-ttu-id="4e329-248">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-249">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-249">Definition</span></span>

<span data-ttu-id="4e329-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-251">L’expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-253">Keywords</span></span>

<span data-ttu-id="4e329-254">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-254"></span></span>
|<span data-ttu-id="4e329-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-256">passport number</span></span>  <br/> <span data-ttu-id="4e329-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="4e329-257">estonian passport number</span></span>  <br/> <span data-ttu-id="4e329-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-258">passport no</span></span>  <br/> <span data-ttu-id="4e329-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="4e329-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="4e329-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="4e329-260">Finland</span></span>

<span data-ttu-id="4e329-261">Pour plus d’informations, consultez la section « numéro de passeport de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="4e329-262">France</span><span class="sxs-lookup"><span data-stu-id="4e329-262">France</span></span>

<span data-ttu-id="4e329-263">Pour plus d’informations, consultez la section « numéro de passeport français » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="4e329-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="4e329-264">Germany</span></span>

<span data-ttu-id="4e329-265">Pour plus d’informations, consultez la section « numéro de passeport allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-265">For details, see the section "German Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="4e329-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="4e329-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="4e329-267">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-267">Format</span></span>

<span data-ttu-id="4e329-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-269">Pattern</span></span>

<span data-ttu-id="4e329-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-271">Checksum</span></span>

<span data-ttu-id="4e329-272">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-273">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-273">Definition</span></span>

<span data-ttu-id="4e329-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-275">L’expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-277">Keywords</span></span>

<span data-ttu-id="4e329-278">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-278"></span></span>
|<span data-ttu-id="4e329-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-280">passport number</span></span>  <br/> <span data-ttu-id="4e329-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="4e329-281">greek passport number</span></span>  <br/> <span data-ttu-id="4e329-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-282">passport no</span></span>  <br/> <span data-ttu-id="4e329-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="4e329-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="4e329-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="4e329-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="4e329-285">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-285">Format</span></span>

<span data-ttu-id="4e329-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-287">Pattern</span></span>

<span data-ttu-id="4e329-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-289">Checksum</span></span>

<span data-ttu-id="4e329-290">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-291">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-291">Definition</span></span>

<span data-ttu-id="4e329-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-293">L’expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-295">Keywords</span></span>

<span data-ttu-id="4e329-296">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-296"></span></span>
|<span data-ttu-id="4e329-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-298">passport number</span></span>  <br/> <span data-ttu-id="4e329-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="4e329-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="4e329-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-300">passport no</span></span>  <br/> <span data-ttu-id="4e329-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="4e329-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="4e329-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="4e329-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="4e329-303">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-303">Format</span></span>

<span data-ttu-id="4e329-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-305">Pattern</span></span>

<span data-ttu-id="4e329-306">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="4e329-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="4e329-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-309">Checksum</span></span>

<span data-ttu-id="4e329-310">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-311">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-311">Definition</span></span>

<span data-ttu-id="4e329-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-313">L’expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-315">Keywords</span></span>

<span data-ttu-id="4e329-316">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-316"></span></span>
|<span data-ttu-id="4e329-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-318">passport number</span></span>  <br/> <span data-ttu-id="4e329-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="4e329-319">irish passport number</span></span>  <br/> <span data-ttu-id="4e329-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-320">passport no</span></span>  <br/> <span data-ttu-id="4e329-321">boîte</span><span class="sxs-lookup"><span data-stu-id="4e329-321">pas</span></span>  <br/> <span data-ttu-id="4e329-322">tel</span><span class="sxs-lookup"><span data-stu-id="4e329-322">passport</span></span>  <br/> <span data-ttu-id="4e329-323">passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-323">passeport</span></span>  <br/> <span data-ttu-id="4e329-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="4e329-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="4e329-325">Italie</span><span class="sxs-lookup"><span data-stu-id="4e329-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="4e329-326">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-326">Format</span></span>

<span data-ttu-id="4e329-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-328">Pattern</span></span>

<span data-ttu-id="4e329-329">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="4e329-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="4e329-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-332">Checksum</span></span>

<span data-ttu-id="4e329-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-334">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-334">Definition</span></span>

<span data-ttu-id="4e329-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-336">L’expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-338">Keywords</span></span>

<span data-ttu-id="4e329-339">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-339"></span></span>
|<span data-ttu-id="4e329-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="4e329-341">italian passport number</span></span>  <br/> <span data-ttu-id="4e329-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="4e329-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="4e329-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="4e329-343">passaporto</span></span>  <br/> <span data-ttu-id="4e329-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="4e329-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="4e329-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-345">passport number</span></span>  <br/> <span data-ttu-id="4e329-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="4e329-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="4e329-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="4e329-347">passaporto numero</span></span>  <br/> <span data-ttu-id="4e329-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="4e329-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="4e329-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="4e329-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="4e329-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="4e329-351">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-351">Format</span></span>

<span data-ttu-id="4e329-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-353">Pattern</span></span>

<span data-ttu-id="4e329-354">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="4e329-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="4e329-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-357">Checksum</span></span>

<span data-ttu-id="4e329-358">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-359">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-359">Definition</span></span>

<span data-ttu-id="4e329-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-361">L’expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-363">Keywords</span></span>

<span data-ttu-id="4e329-364">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-364"></span></span>
|<span data-ttu-id="4e329-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-366">passport number</span></span>  <br/> <span data-ttu-id="4e329-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="4e329-367">latvian passport number</span></span>  <br/> <span data-ttu-id="4e329-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-368">passport no</span></span>  <br/> <span data-ttu-id="4e329-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="4e329-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="4e329-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="4e329-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="4e329-371">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-371">Format</span></span>

<span data-ttu-id="4e329-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-373">Pattern</span></span>

<span data-ttu-id="4e329-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-375">Checksum</span></span>

<span data-ttu-id="4e329-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-377">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-377">Definition</span></span>

<span data-ttu-id="4e329-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-379">L’expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-381">Keywords</span></span>

<span data-ttu-id="4e329-382">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-382"></span></span>
|<span data-ttu-id="4e329-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-384">passport number</span></span>  <br/> <span data-ttu-id="4e329-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="4e329-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="4e329-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-386">passport no</span></span>  <br/> <span data-ttu-id="4e329-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="4e329-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="4e329-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="4e329-389">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-389">Format</span></span>

<span data-ttu-id="4e329-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-391">Pattern</span></span>

<span data-ttu-id="4e329-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-393">Checksum</span></span>

<span data-ttu-id="4e329-394">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-395">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-395">Definition</span></span>

<span data-ttu-id="4e329-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-397">L’expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-399">Keywords</span></span>

<span data-ttu-id="4e329-400">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-400"></span></span>
|<span data-ttu-id="4e329-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-402">passport number</span></span>  <br/> <span data-ttu-id="4e329-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="4e329-403">latvian passport number</span></span>  <br/> <span data-ttu-id="4e329-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-404">passport no</span></span>  <br/> <span data-ttu-id="4e329-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="4e329-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="4e329-406">Malte</span><span class="sxs-lookup"><span data-stu-id="4e329-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="4e329-407">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-407">Format</span></span>

<span data-ttu-id="4e329-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-409">Pattern</span></span>

 <span data-ttu-id="4e329-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4e329-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-411">Checksum</span></span>

<span data-ttu-id="4e329-412">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-413">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-413">Definition</span></span>

<span data-ttu-id="4e329-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-415">L’expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-417">Keywords</span></span>

<span data-ttu-id="4e329-418">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-418"></span></span>
|<span data-ttu-id="4e329-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-420">passport number</span></span>  <br/> <span data-ttu-id="4e329-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="4e329-421">maltese passport number</span></span>  <br/> <span data-ttu-id="4e329-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-422">passport no</span></span>  <br/> <span data-ttu-id="4e329-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="4e329-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="4e329-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="4e329-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="4e329-425">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-425">Format</span></span>

<span data-ttu-id="4e329-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-427">Pattern</span></span>

<span data-ttu-id="4e329-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-429">Checksum</span></span>

<span data-ttu-id="4e329-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-431">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-431">Definition</span></span>

<span data-ttu-id="4e329-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-433">L’expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-435">Keywords</span></span>

<span data-ttu-id="4e329-436">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-436"></span></span>
|<span data-ttu-id="4e329-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="4e329-438">dutch passport number</span></span>  <br/> <span data-ttu-id="4e329-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-439">passport number</span></span>  <br/> <span data-ttu-id="4e329-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="4e329-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="4e329-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="4e329-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="4e329-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="4e329-442">paspoort</span></span>  <br/> <span data-ttu-id="4e329-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="4e329-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="4e329-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="4e329-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="4e329-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="4e329-445">Poland</span></span>

<span data-ttu-id="4e329-446">Pour plus d’informations, reportez-vous à la section « numéro de passeport polonais » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="4e329-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="4e329-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="4e329-448">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-448">Format</span></span>

<span data-ttu-id="4e329-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-450">Pattern</span></span>

<span data-ttu-id="4e329-451">Une lettre suivie de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="4e329-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="4e329-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="4e329-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-454">Checksum</span></span>

<span data-ttu-id="4e329-455">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-456">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-456">Definition</span></span>

<span data-ttu-id="4e329-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-458">L’expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-460">Keywords</span></span>

<span data-ttu-id="4e329-461">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-461"></span></span>
|<span data-ttu-id="4e329-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-463">passport number</span></span>  <br/> <span data-ttu-id="4e329-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="4e329-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="4e329-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-465">passport no</span></span>  <br/> <span data-ttu-id="4e329-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="4e329-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="4e329-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="4e329-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="4e329-468">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-468">Format</span></span>

<span data-ttu-id="4e329-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-470">Pattern</span></span>

<span data-ttu-id="4e329-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-472">Checksum</span></span>

<span data-ttu-id="4e329-473">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-474">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-474">Definition</span></span>

<span data-ttu-id="4e329-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-476">L’expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-478">Keywords</span></span>

<span data-ttu-id="4e329-479">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-479"></span></span>
|<span data-ttu-id="4e329-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-481">passport number</span></span>  <br/> <span data-ttu-id="4e329-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="4e329-482">romanian passport number</span></span>  <br/> <span data-ttu-id="4e329-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-483">passport no</span></span>  <br/> <span data-ttu-id="4e329-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="4e329-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="4e329-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="4e329-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="4e329-486">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-486">Format</span></span>

<span data-ttu-id="4e329-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-488">Pattern</span></span>

<span data-ttu-id="4e329-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4e329-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-490">Checksum</span></span>

<span data-ttu-id="4e329-491">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-492">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-492">Definition</span></span>

<span data-ttu-id="4e329-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-494">L’expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-496">Keywords</span></span>

<span data-ttu-id="4e329-497">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-497"></span></span>
|<span data-ttu-id="4e329-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-499">passport number</span></span>  <br/> <span data-ttu-id="4e329-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="4e329-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="4e329-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-501">passport no</span></span>  <br/> <span data-ttu-id="4e329-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="4e329-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="4e329-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="4e329-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="4e329-504">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-504">Format</span></span>

<span data-ttu-id="4e329-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-506">Pattern</span></span>

<span data-ttu-id="4e329-507">Deux lettres suivies de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="4e329-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="4e329-508">The letter "P"</span></span>
    
- <span data-ttu-id="4e329-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="4e329-509">One uppercase letter</span></span>
    
- <span data-ttu-id="4e329-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-511">Checksum</span></span>

<span data-ttu-id="4e329-512">Non</span><span class="sxs-lookup"><span data-stu-id="4e329-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-513">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-513">Definition</span></span>

<span data-ttu-id="4e329-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-515">L’expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-517">Keywords</span></span>

<span data-ttu-id="4e329-518">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-518"></span></span>
|<span data-ttu-id="4e329-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-520">passport number</span></span>  <br/> <span data-ttu-id="4e329-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="4e329-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="4e329-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-522">passport no</span></span>  <br/> <span data-ttu-id="4e329-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="4e329-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="4e329-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="4e329-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="4e329-525">Format</span><span class="sxs-lookup"><span data-stu-id="4e329-525">Format</span></span>

<span data-ttu-id="4e329-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="4e329-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4e329-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="4e329-527">Pattern</span></span>

<span data-ttu-id="4e329-528">Combinaison de huit ou neuf caractères de lettres et de chiffres :</span><span class="sxs-lookup"><span data-stu-id="4e329-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="4e329-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="4e329-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="4e329-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4e329-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="4e329-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="4e329-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4e329-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="4e329-532">Checksum</span></span>

<span data-ttu-id="4e329-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e329-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4e329-534">Définition</span><span class="sxs-lookup"><span data-stu-id="4e329-534">Definition</span></span>

<span data-ttu-id="4e329-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="4e329-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4e329-536">L’expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="4e329-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4e329-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e329-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4e329-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e329-538">Keywords</span></span>

<span data-ttu-id="4e329-539">| |</span><span class="sxs-lookup"><span data-stu-id="4e329-539"></span></span>
|<span data-ttu-id="4e329-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="4e329-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="4e329-541">tel</span><span class="sxs-lookup"><span data-stu-id="4e329-541">passport</span></span>  <br/> <span data-ttu-id="4e329-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="4e329-542">spain passport</span></span>  <br/> <span data-ttu-id="4e329-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-543">passport book</span></span>  <br/> <span data-ttu-id="4e329-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-544">passport number</span></span>  <br/> <span data-ttu-id="4e329-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="4e329-545">passport no</span></span>  <br/> <span data-ttu-id="4e329-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="4e329-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="4e329-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="4e329-547">número pasaporte</span></span>  <br/> <span data-ttu-id="4e329-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="4e329-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="4e329-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="4e329-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="4e329-550">Suède</span><span class="sxs-lookup"><span data-stu-id="4e329-550">Sweden</span></span>

<span data-ttu-id="4e329-551">Pour plus d’informations, reportez-vous à la section « numéro de passeport Suède » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="4e329-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="4e329-552">UK</span></span>

<span data-ttu-id="4e329-553">Pour plus d’informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="4e329-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="4e329-554">Numéro de passeport» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4e329-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e329-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e329-555">See also</span></span>

[<span data-ttu-id="4e329-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="4e329-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

