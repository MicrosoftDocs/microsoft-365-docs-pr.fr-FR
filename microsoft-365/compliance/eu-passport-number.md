---
title: Numéro de passeport UE
ms.author: laurawi
author: laurawi
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 44ee6e7b46d79772bcd3aec0fd26265f58f6c4c6
ms.sourcegitcommit: 3fd6d175c1954ce463198e835d1d8f2f91d80d79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2019
ms.locfileid: "39662799"
---
# <a name="eu-passport-number"></a><span data-ttu-id="d3db3-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="d3db3-104">EU Passport Number</span></span>

<span data-ttu-id="d3db3-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE.</span><span class="sxs-lookup"><span data-stu-id="d3db3-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="d3db3-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="d3db3-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d3db3-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d3db3-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-108">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-108">Format</span></span>

<span data-ttu-id="d3db3-109">Une lettre suivie d’un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-110">Pattern</span></span>

<span data-ttu-id="d3db3-111">Une combinaison d’une lettre, de sept chiffres et d’un espace :</span><span class="sxs-lookup"><span data-stu-id="d3db3-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="d3db3-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d3db3-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d3db3-113">One space (optional)</span></span>
    
- <span data-ttu-id="d3db3-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-115">Checksum</span></span>

<span data-ttu-id="d3db3-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-117">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-117">Definition</span></span>

<span data-ttu-id="d3db3-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-119">L’expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-121">Keywords</span></span>

<span data-ttu-id="d3db3-122">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-122"></span></span>
|<span data-ttu-id="d3db3-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-124">passport number</span></span>  <br/> <span data-ttu-id="d3db3-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="d3db3-125">austrian passport number</span></span>  <br/> <span data-ttu-id="d3db3-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-126">passport no</span></span>  <br/> <span data-ttu-id="d3db3-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="d3db3-127">reisepass</span></span>  <br/> <span data-ttu-id="d3db3-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="d3db3-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="d3db3-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="d3db3-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-130">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-130">Format</span></span>

<span data-ttu-id="d3db3-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-132">Pattern</span></span>

<span data-ttu-id="d3db3-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-134">Checksum</span></span>

<span data-ttu-id="d3db3-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-136">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-136">Definition</span></span>

<span data-ttu-id="d3db3-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-138">L’expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-140">Keywords</span></span>

<span data-ttu-id="d3db3-141">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-141"></span></span>
|<span data-ttu-id="d3db3-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-143">passport number</span></span>  <br/> <span data-ttu-id="d3db3-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="d3db3-144">belgian passport number</span></span>  <br/> <span data-ttu-id="d3db3-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-145">passport no</span></span>  <br/> <span data-ttu-id="d3db3-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="d3db3-146">paspoort</span></span>  <br/> <span data-ttu-id="d3db3-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="d3db3-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="d3db3-148">reisepass kein</span></span>  <br/> <span data-ttu-id="d3db3-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="d3db3-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="d3db3-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d3db3-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-151">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-151">Format</span></span>

<span data-ttu-id="d3db3-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-153">Pattern</span></span>

 <span data-ttu-id="d3db3-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d3db3-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-155">Checksum</span></span>

<span data-ttu-id="d3db3-156">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-157">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-157">Definition</span></span>

<span data-ttu-id="d3db3-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-159">L’expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-161">Keywords</span></span>

<span data-ttu-id="d3db3-162">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-162"></span></span>
|<span data-ttu-id="d3db3-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-164">passport number</span></span>  <br/> <span data-ttu-id="d3db3-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="d3db3-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="d3db3-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-166">passport no</span></span>  <br/> <span data-ttu-id="d3db3-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="d3db3-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="d3db3-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="d3db3-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-169">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-169">Format</span></span>

<span data-ttu-id="d3db3-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-171">Pattern</span></span>

 <span data-ttu-id="d3db3-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d3db3-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-173">Checksum</span></span>

<span data-ttu-id="d3db3-174">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-175">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-175">Definition</span></span>

<span data-ttu-id="d3db3-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-177">L’expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-179">Keywords</span></span>

<span data-ttu-id="d3db3-180">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-180"></span></span>
|<span data-ttu-id="d3db3-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-182">passport number</span></span>  <br/> <span data-ttu-id="d3db3-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="d3db3-183">croatian passport number</span></span>  <br/> <span data-ttu-id="d3db3-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-184">passport no</span></span>  <br/> <span data-ttu-id="d3db3-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="d3db3-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="d3db3-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="d3db3-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-187">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-187">Format</span></span>

<span data-ttu-id="d3db3-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-189">Pattern</span></span>

<span data-ttu-id="d3db3-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-191">Checksum</span></span>

<span data-ttu-id="d3db3-192">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-193">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-193">Definition</span></span>

<span data-ttu-id="d3db3-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-195">L’expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-197">Keywords</span></span>

<span data-ttu-id="d3db3-198">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-198"></span></span>
|<span data-ttu-id="d3db3-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-200">passport number</span></span>  <br/> <span data-ttu-id="d3db3-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="d3db3-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="d3db3-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-202">passport no</span></span>  <br/> <span data-ttu-id="d3db3-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="d3db3-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="d3db3-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d3db3-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-205">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-205">Format</span></span>

<span data-ttu-id="d3db3-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-207">Pattern</span></span>

<span data-ttu-id="d3db3-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-209">Checksum</span></span>

<span data-ttu-id="d3db3-210">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-211">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-211">Definition</span></span>

<span data-ttu-id="d3db3-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-213">L’expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-215">Keywords</span></span>

<span data-ttu-id="d3db3-216">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-216"></span></span>
|<span data-ttu-id="d3db3-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-218">passport number</span></span>  <br/> <span data-ttu-id="d3db3-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="d3db3-219">czech passport number</span></span>  <br/> <span data-ttu-id="d3db3-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-220">passport no</span></span>  <br/> <span data-ttu-id="d3db3-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="d3db3-221">cestovní pas</span></span>  <br/> <span data-ttu-id="d3db3-222">boîte</span><span class="sxs-lookup"><span data-stu-id="d3db3-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="d3db3-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="d3db3-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-224">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-224">Format</span></span>

<span data-ttu-id="d3db3-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-226">Pattern</span></span>

 <span data-ttu-id="d3db3-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d3db3-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-228">Checksum</span></span>

<span data-ttu-id="d3db3-229">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-230">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-230">Definition</span></span>

<span data-ttu-id="d3db3-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-232">L’expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-234">Keywords</span></span>

<span data-ttu-id="d3db3-235">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-235"></span></span>
|<span data-ttu-id="d3db3-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-237">passport number</span></span>  <br/> <span data-ttu-id="d3db3-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="d3db3-238">danish passport number</span></span>  <br/> <span data-ttu-id="d3db3-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-239">passport no</span></span>  <br/> <span data-ttu-id="d3db3-240">boîte</span><span class="sxs-lookup"><span data-stu-id="d3db3-240">pas</span></span>  <br/> <span data-ttu-id="d3db3-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="d3db3-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="d3db3-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-243">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-243">Format</span></span>

<span data-ttu-id="d3db3-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-245">Pattern</span></span>

<span data-ttu-id="d3db3-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-247">Checksum</span></span>

<span data-ttu-id="d3db3-248">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-249">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-249">Definition</span></span>

<span data-ttu-id="d3db3-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-251">L’expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-253">Keywords</span></span>

<span data-ttu-id="d3db3-254">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-254"></span></span>
|<span data-ttu-id="d3db3-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-256">passport number</span></span>  <br/> <span data-ttu-id="d3db3-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="d3db3-257">estonian passport number</span></span>  <br/> <span data-ttu-id="d3db3-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-258">passport no</span></span>  <br/> <span data-ttu-id="d3db3-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="d3db3-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="d3db3-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="d3db3-260">Finland</span></span>

<span data-ttu-id="d3db3-261">Pour plus d’informations, consultez la section « numéro de passeport de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="d3db3-262">France</span><span class="sxs-lookup"><span data-stu-id="d3db3-262">France</span></span>

<span data-ttu-id="d3db3-263">Pour plus d’informations, consultez la section « numéro de passeport français » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="d3db3-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d3db3-264">Germany</span></span>

<span data-ttu-id="d3db3-265">Pour plus d’informations, consultez la section « numéro de passeport allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-265">For details, see the section "German Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="d3db3-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="d3db3-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-267">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-267">Format</span></span>

<span data-ttu-id="d3db3-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-269">Pattern</span></span>

<span data-ttu-id="d3db3-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-271">Checksum</span></span>

<span data-ttu-id="d3db3-272">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-273">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-273">Definition</span></span>

<span data-ttu-id="d3db3-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-275">L’expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-277">Keywords</span></span>

<span data-ttu-id="d3db3-278">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-278"></span></span>
|<span data-ttu-id="d3db3-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-280">passport number</span></span>  <br/> <span data-ttu-id="d3db3-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="d3db3-281">greek passport number</span></span>  <br/> <span data-ttu-id="d3db3-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-282">passport no</span></span>  <br/> <span data-ttu-id="d3db3-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="d3db3-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="d3db3-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d3db3-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-285">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-285">Format</span></span>

<span data-ttu-id="d3db3-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-287">Pattern</span></span>

<span data-ttu-id="d3db3-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-289">Checksum</span></span>

<span data-ttu-id="d3db3-290">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-291">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-291">Definition</span></span>

<span data-ttu-id="d3db3-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-293">L’expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-295">Keywords</span></span>

<span data-ttu-id="d3db3-296">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-296"></span></span>
|<span data-ttu-id="d3db3-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-298">passport number</span></span>  <br/> <span data-ttu-id="d3db3-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="d3db3-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="d3db3-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-300">passport no</span></span>  <br/> <span data-ttu-id="d3db3-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="d3db3-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="d3db3-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="d3db3-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-303">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-303">Format</span></span>

<span data-ttu-id="d3db3-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-305">Pattern</span></span>

<span data-ttu-id="d3db3-306">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d3db3-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d3db3-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-309">Checksum</span></span>

<span data-ttu-id="d3db3-310">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-311">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-311">Definition</span></span>

<span data-ttu-id="d3db3-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-313">L’expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-315">Keywords</span></span>

<span data-ttu-id="d3db3-316">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-316"></span></span>
|<span data-ttu-id="d3db3-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-318">passport number</span></span>  <br/> <span data-ttu-id="d3db3-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="d3db3-319">irish passport number</span></span>  <br/> <span data-ttu-id="d3db3-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-320">passport no</span></span>  <br/> <span data-ttu-id="d3db3-321">boîte</span><span class="sxs-lookup"><span data-stu-id="d3db3-321">pas</span></span>  <br/> <span data-ttu-id="d3db3-322">tel</span><span class="sxs-lookup"><span data-stu-id="d3db3-322">passport</span></span>  <br/> <span data-ttu-id="d3db3-323">passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-323">passeport</span></span>  <br/> <span data-ttu-id="d3db3-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="d3db3-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="d3db3-325">Italie</span><span class="sxs-lookup"><span data-stu-id="d3db3-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-326">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-326">Format</span></span>

<span data-ttu-id="d3db3-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-328">Pattern</span></span>

<span data-ttu-id="d3db3-329">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d3db3-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d3db3-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-332">Checksum</span></span>

<span data-ttu-id="d3db3-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-334">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-334">Definition</span></span>

<span data-ttu-id="d3db3-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-336">L’expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-338">Keywords</span></span>

<span data-ttu-id="d3db3-339">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-339"></span></span>
|<span data-ttu-id="d3db3-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="d3db3-341">italian passport number</span></span>  <br/> <span data-ttu-id="d3db3-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="d3db3-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="d3db3-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="d3db3-343">passaporto</span></span>  <br/> <span data-ttu-id="d3db3-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="d3db3-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="d3db3-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-345">passport number</span></span>  <br/> <span data-ttu-id="d3db3-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d3db3-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="d3db3-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d3db3-347">passaporto numero</span></span>  <br/> <span data-ttu-id="d3db3-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="d3db3-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="d3db3-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="d3db3-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d3db3-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-351">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-351">Format</span></span>

<span data-ttu-id="d3db3-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-353">Pattern</span></span>

<span data-ttu-id="d3db3-354">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d3db3-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d3db3-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-357">Checksum</span></span>

<span data-ttu-id="d3db3-358">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-359">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-359">Definition</span></span>

<span data-ttu-id="d3db3-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-361">L’expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-363">Keywords</span></span>

<span data-ttu-id="d3db3-364">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-364"></span></span>
|<span data-ttu-id="d3db3-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-366">passport number</span></span>  <br/> <span data-ttu-id="d3db3-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d3db3-367">latvian passport number</span></span>  <br/> <span data-ttu-id="d3db3-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-368">passport no</span></span>  <br/> <span data-ttu-id="d3db3-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="d3db3-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d3db3-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-371">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-371">Format</span></span>

<span data-ttu-id="d3db3-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-373">Pattern</span></span>

<span data-ttu-id="d3db3-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-375">Checksum</span></span>

<span data-ttu-id="d3db3-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-377">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-377">Definition</span></span>

<span data-ttu-id="d3db3-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-379">L’expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-381">Keywords</span></span>

<span data-ttu-id="d3db3-382">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-382"></span></span>
|<span data-ttu-id="d3db3-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-384">passport number</span></span>  <br/> <span data-ttu-id="d3db3-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="d3db3-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="d3db3-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-386">passport no</span></span>  <br/> <span data-ttu-id="d3db3-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="d3db3-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="d3db3-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-389">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-389">Format</span></span>

<span data-ttu-id="d3db3-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-391">Pattern</span></span>

<span data-ttu-id="d3db3-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-393">Checksum</span></span>

<span data-ttu-id="d3db3-394">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-395">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-395">Definition</span></span>

<span data-ttu-id="d3db3-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-397">L’expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-399">Keywords</span></span>

<span data-ttu-id="d3db3-400">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-400"></span></span>
|<span data-ttu-id="d3db3-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-402">passport number</span></span>  <br/> <span data-ttu-id="d3db3-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d3db3-403">latvian passport number</span></span>  <br/> <span data-ttu-id="d3db3-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-404">passport no</span></span>  <br/> <span data-ttu-id="d3db3-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="d3db3-406">Malte</span><span class="sxs-lookup"><span data-stu-id="d3db3-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-407">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-407">Format</span></span>

<span data-ttu-id="d3db3-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-409">Pattern</span></span>

 <span data-ttu-id="d3db3-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d3db3-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-411">Checksum</span></span>

<span data-ttu-id="d3db3-412">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-413">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-413">Definition</span></span>

<span data-ttu-id="d3db3-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-415">L’expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-417">Keywords</span></span>

<span data-ttu-id="d3db3-418">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-418"></span></span>
|<span data-ttu-id="d3db3-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-420">passport number</span></span>  <br/> <span data-ttu-id="d3db3-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="d3db3-421">maltese passport number</span></span>  <br/> <span data-ttu-id="d3db3-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-422">passport no</span></span>  <br/> <span data-ttu-id="d3db3-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="d3db3-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="d3db3-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d3db3-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-425">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-425">Format</span></span>

<span data-ttu-id="d3db3-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-427">Pattern</span></span>

<span data-ttu-id="d3db3-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-429">Checksum</span></span>

<span data-ttu-id="d3db3-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-431">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-431">Definition</span></span>

<span data-ttu-id="d3db3-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-433">L’expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-435">Keywords</span></span>

<span data-ttu-id="d3db3-436">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-436"></span></span>
|<span data-ttu-id="d3db3-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d3db3-438">dutch passport number</span></span>  <br/> <span data-ttu-id="d3db3-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-439">passport number</span></span>  <br/> <span data-ttu-id="d3db3-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d3db3-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="d3db3-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="d3db3-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="d3db3-442">paspoort</span></span>  <br/> <span data-ttu-id="d3db3-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="d3db3-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d3db3-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="d3db3-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="d3db3-445">Poland</span></span>

<span data-ttu-id="d3db3-446">Pour plus d’informations, reportez-vous à la section « numéro de passeport polonais » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d3db3-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="d3db3-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-448">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-448">Format</span></span>

<span data-ttu-id="d3db3-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-450">Pattern</span></span>

<span data-ttu-id="d3db3-451">Une lettre suivie de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="d3db3-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d3db3-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d3db3-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-454">Checksum</span></span>

<span data-ttu-id="d3db3-455">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-456">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-456">Definition</span></span>

<span data-ttu-id="d3db3-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-458">L’expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-460">Keywords</span></span>

<span data-ttu-id="d3db3-461">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-461"></span></span>
|<span data-ttu-id="d3db3-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-463">passport number</span></span>  <br/> <span data-ttu-id="d3db3-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="d3db3-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="d3db3-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-465">passport no</span></span>  <br/> <span data-ttu-id="d3db3-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="d3db3-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="d3db3-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d3db3-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-468">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-468">Format</span></span>

<span data-ttu-id="d3db3-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-470">Pattern</span></span>

<span data-ttu-id="d3db3-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-472">Checksum</span></span>

<span data-ttu-id="d3db3-473">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-474">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-474">Definition</span></span>

<span data-ttu-id="d3db3-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-476">L’expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-478">Keywords</span></span>

<span data-ttu-id="d3db3-479">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-479"></span></span>
|<span data-ttu-id="d3db3-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-481">passport number</span></span>  <br/> <span data-ttu-id="d3db3-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="d3db3-482">romanian passport number</span></span>  <br/> <span data-ttu-id="d3db3-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-483">passport no</span></span>  <br/> <span data-ttu-id="d3db3-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="d3db3-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="d3db3-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d3db3-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-486">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-486">Format</span></span>

<span data-ttu-id="d3db3-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-488">Pattern</span></span>

<span data-ttu-id="d3db3-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d3db3-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-490">Checksum</span></span>

<span data-ttu-id="d3db3-491">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-492">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-492">Definition</span></span>

<span data-ttu-id="d3db3-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-494">L’expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-496">Keywords</span></span>

<span data-ttu-id="d3db3-497">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-497"></span></span>
|<span data-ttu-id="d3db3-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-499">passport number</span></span>  <br/> <span data-ttu-id="d3db3-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="d3db3-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="d3db3-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-501">passport no</span></span>  <br/> <span data-ttu-id="d3db3-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="d3db3-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="d3db3-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d3db3-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-504">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-504">Format</span></span>

<span data-ttu-id="d3db3-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-506">Pattern</span></span>

<span data-ttu-id="d3db3-507">Deux lettres suivies de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="d3db3-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="d3db3-508">The letter "P"</span></span>
    
- <span data-ttu-id="d3db3-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="d3db3-509">One uppercase letter</span></span>
    
- <span data-ttu-id="d3db3-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-511">Checksum</span></span>

<span data-ttu-id="d3db3-512">Non</span><span class="sxs-lookup"><span data-stu-id="d3db3-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-513">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-513">Definition</span></span>

<span data-ttu-id="d3db3-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-515">L’expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-517">Keywords</span></span>

<span data-ttu-id="d3db3-518">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-518"></span></span>
|<span data-ttu-id="d3db3-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-520">passport number</span></span>  <br/> <span data-ttu-id="d3db3-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="d3db3-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="d3db3-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-522">passport no</span></span>  <br/> <span data-ttu-id="d3db3-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="d3db3-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="d3db3-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="d3db3-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="d3db3-525">Format</span><span class="sxs-lookup"><span data-stu-id="d3db3-525">Format</span></span>

<span data-ttu-id="d3db3-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d3db3-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d3db3-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="d3db3-527">Pattern</span></span>

<span data-ttu-id="d3db3-528">Combinaison de huit ou neuf caractères de lettres et de chiffres :</span><span class="sxs-lookup"><span data-stu-id="d3db3-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="d3db3-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="d3db3-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="d3db3-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d3db3-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="d3db3-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d3db3-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d3db3-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3db3-532">Checksum</span></span>

<span data-ttu-id="d3db3-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d3db3-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d3db3-534">Définition</span><span class="sxs-lookup"><span data-stu-id="d3db3-534">Definition</span></span>

<span data-ttu-id="d3db3-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d3db3-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d3db3-536">L’expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d3db3-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d3db3-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d3db3-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d3db3-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d3db3-538">Keywords</span></span>

<span data-ttu-id="d3db3-539">| |</span><span class="sxs-lookup"><span data-stu-id="d3db3-539"></span></span>
|<span data-ttu-id="d3db3-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d3db3-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d3db3-541">tel</span><span class="sxs-lookup"><span data-stu-id="d3db3-541">passport</span></span>  <br/> <span data-ttu-id="d3db3-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="d3db3-542">spain passport</span></span>  <br/> <span data-ttu-id="d3db3-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-543">passport book</span></span>  <br/> <span data-ttu-id="d3db3-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-544">passport number</span></span>  <br/> <span data-ttu-id="d3db3-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d3db3-545">passport no</span></span>  <br/> <span data-ttu-id="d3db3-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="d3db3-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="d3db3-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="d3db3-547">número pasaporte</span></span>  <br/> <span data-ttu-id="d3db3-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="d3db3-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="d3db3-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="d3db3-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="d3db3-550">Suède</span><span class="sxs-lookup"><span data-stu-id="d3db3-550">Sweden</span></span>

<span data-ttu-id="d3db3-551">Pour plus d’informations, reportez-vous à la section « numéro de passeport Suède » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="d3db3-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="d3db3-552">UK</span></span>

<span data-ttu-id="d3db3-553">Pour plus d’informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="d3db3-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="d3db3-554">Numéro de passeport» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d3db3-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3db3-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3db3-555">See also</span></span>

[<span data-ttu-id="d3db3-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d3db3-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

