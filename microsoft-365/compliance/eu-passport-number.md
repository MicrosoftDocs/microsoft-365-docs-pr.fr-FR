---
title: Numéro de passeport UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: fa3be04dec0f71a2568e046abd6b0af3e20181c5
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079270"
---
# <a name="eu-passport-number"></a><span data-ttu-id="a40cf-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="a40cf-104">EU Passport Number</span></span>

<span data-ttu-id="a40cf-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE.</span><span class="sxs-lookup"><span data-stu-id="a40cf-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="a40cf-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="a40cf-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a40cf-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="a40cf-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-108">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-108">Format</span></span>

<span data-ttu-id="a40cf-109">Une lettre suivie d’un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-110">Pattern</span></span>

<span data-ttu-id="a40cf-111">Une combinaison d’une lettre, de sept chiffres et d’un espace :</span><span class="sxs-lookup"><span data-stu-id="a40cf-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="a40cf-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="a40cf-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="a40cf-113">One space (optional)</span></span>
    
- <span data-ttu-id="a40cf-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-115">Checksum</span></span>

<span data-ttu-id="a40cf-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-117">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-117">Definition</span></span>

<span data-ttu-id="a40cf-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-119">L’expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-121">Keywords</span></span>

<span data-ttu-id="a40cf-122">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-122"></span></span>
|<span data-ttu-id="a40cf-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-124">passport number</span></span>  <br/> <span data-ttu-id="a40cf-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="a40cf-125">austrian passport number</span></span>  <br/> <span data-ttu-id="a40cf-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-126">passport no</span></span>  <br/> <span data-ttu-id="a40cf-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="a40cf-127">reisepass</span></span>  <br/> <span data-ttu-id="a40cf-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="a40cf-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a40cf-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="a40cf-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-130">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-130">Format</span></span>

<span data-ttu-id="a40cf-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-132">Pattern</span></span>

<span data-ttu-id="a40cf-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-134">Checksum</span></span>

<span data-ttu-id="a40cf-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-136">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-136">Definition</span></span>

<span data-ttu-id="a40cf-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-138">L’expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-140">Keywords</span></span>

<span data-ttu-id="a40cf-141">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-141"></span></span>
|<span data-ttu-id="a40cf-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-143">passport number</span></span>  <br/> <span data-ttu-id="a40cf-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="a40cf-144">belgian passport number</span></span>  <br/> <span data-ttu-id="a40cf-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-145">passport no</span></span>  <br/> <span data-ttu-id="a40cf-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="a40cf-146">paspoort</span></span>  <br/> <span data-ttu-id="a40cf-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="a40cf-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="a40cf-148">reisepass kein</span></span>  <br/> <span data-ttu-id="a40cf-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="a40cf-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a40cf-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="a40cf-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-151">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-151">Format</span></span>

<span data-ttu-id="a40cf-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-153">Pattern</span></span>

 <span data-ttu-id="a40cf-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a40cf-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-155">Checksum</span></span>

<span data-ttu-id="a40cf-156">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-157">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-157">Definition</span></span>

<span data-ttu-id="a40cf-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-159">L’expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-161">Keywords</span></span>

<span data-ttu-id="a40cf-162">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-162"></span></span>
|<span data-ttu-id="a40cf-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-164">passport number</span></span>  <br/> <span data-ttu-id="a40cf-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="a40cf-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="a40cf-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-166">passport no</span></span>  <br/> <span data-ttu-id="a40cf-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="a40cf-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a40cf-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="a40cf-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-169">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-169">Format</span></span>

<span data-ttu-id="a40cf-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-171">Pattern</span></span>

 <span data-ttu-id="a40cf-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a40cf-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-173">Checksum</span></span>

<span data-ttu-id="a40cf-174">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-175">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-175">Definition</span></span>

<span data-ttu-id="a40cf-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-177">L’expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-179">Keywords</span></span>

<span data-ttu-id="a40cf-180">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-180"></span></span>
|<span data-ttu-id="a40cf-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-182">passport number</span></span>  <br/> <span data-ttu-id="a40cf-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="a40cf-183">croatian passport number</span></span>  <br/> <span data-ttu-id="a40cf-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-184">passport no</span></span>  <br/> <span data-ttu-id="a40cf-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="a40cf-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a40cf-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="a40cf-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-187">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-187">Format</span></span>

<span data-ttu-id="a40cf-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-189">Pattern</span></span>

<span data-ttu-id="a40cf-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-191">Checksum</span></span>

<span data-ttu-id="a40cf-192">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-193">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-193">Definition</span></span>

<span data-ttu-id="a40cf-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-195">L’expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-197">Keywords</span></span>

<span data-ttu-id="a40cf-198">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-198"></span></span>
|<span data-ttu-id="a40cf-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-200">passport number</span></span>  <br/> <span data-ttu-id="a40cf-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="a40cf-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="a40cf-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-202">passport no</span></span>  <br/> <span data-ttu-id="a40cf-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="a40cf-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a40cf-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="a40cf-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-205">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-205">Format</span></span>

<span data-ttu-id="a40cf-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-207">Pattern</span></span>

<span data-ttu-id="a40cf-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-209">Checksum</span></span>

<span data-ttu-id="a40cf-210">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-211">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-211">Definition</span></span>

<span data-ttu-id="a40cf-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-213">L’expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-215">Keywords</span></span>

<span data-ttu-id="a40cf-216">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-216"></span></span>
|<span data-ttu-id="a40cf-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-218">passport number</span></span>  <br/> <span data-ttu-id="a40cf-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="a40cf-219">czech passport number</span></span>  <br/> <span data-ttu-id="a40cf-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-220">passport no</span></span>  <br/> <span data-ttu-id="a40cf-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="a40cf-221">cestovní pas</span></span>  <br/> <span data-ttu-id="a40cf-222">boîte</span><span class="sxs-lookup"><span data-stu-id="a40cf-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a40cf-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="a40cf-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-224">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-224">Format</span></span>

<span data-ttu-id="a40cf-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-226">Pattern</span></span>

 <span data-ttu-id="a40cf-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a40cf-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-228">Checksum</span></span>

<span data-ttu-id="a40cf-229">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-230">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-230">Definition</span></span>

<span data-ttu-id="a40cf-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-232">L’expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-234">Keywords</span></span>

<span data-ttu-id="a40cf-235">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-235"></span></span>
|<span data-ttu-id="a40cf-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-237">passport number</span></span>  <br/> <span data-ttu-id="a40cf-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="a40cf-238">danish passport number</span></span>  <br/> <span data-ttu-id="a40cf-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-239">passport no</span></span>  <br/> <span data-ttu-id="a40cf-240">boîte</span><span class="sxs-lookup"><span data-stu-id="a40cf-240">pas</span></span>  <br/> <span data-ttu-id="a40cf-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a40cf-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="a40cf-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-243">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-243">Format</span></span>

<span data-ttu-id="a40cf-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-245">Pattern</span></span>

<span data-ttu-id="a40cf-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-247">Checksum</span></span>

<span data-ttu-id="a40cf-248">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-249">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-249">Definition</span></span>

<span data-ttu-id="a40cf-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-251">L’expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-253">Keywords</span></span>

<span data-ttu-id="a40cf-254">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-254"></span></span>
|<span data-ttu-id="a40cf-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-256">passport number</span></span>  <br/> <span data-ttu-id="a40cf-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="a40cf-257">estonian passport number</span></span>  <br/> <span data-ttu-id="a40cf-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-258">passport no</span></span>  <br/> <span data-ttu-id="a40cf-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="a40cf-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a40cf-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="a40cf-260">Finland</span></span>

<span data-ttu-id="a40cf-261">Pour plus d’informations, consultez la section « numéro de passeport de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="a40cf-262">France</span><span class="sxs-lookup"><span data-stu-id="a40cf-262">France</span></span>

<span data-ttu-id="a40cf-263">Pour plus d’informations, consultez la section « numéro de passeport français » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a40cf-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="a40cf-264">Germany</span></span>

<span data-ttu-id="a40cf-265">Pour plus d’informations, reportez-vous à la section « numéro de passeport allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a40cf-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="a40cf-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-267">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-267">Format</span></span>

<span data-ttu-id="a40cf-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-269">Pattern</span></span>

<span data-ttu-id="a40cf-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-271">Checksum</span></span>

<span data-ttu-id="a40cf-272">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-273">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-273">Definition</span></span>

<span data-ttu-id="a40cf-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-275">L’expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-277">Keywords</span></span>

<span data-ttu-id="a40cf-278">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-278"></span></span>
|<span data-ttu-id="a40cf-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-280">passport number</span></span>  <br/> <span data-ttu-id="a40cf-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="a40cf-281">greek passport number</span></span>  <br/> <span data-ttu-id="a40cf-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-282">passport no</span></span>  <br/> <span data-ttu-id="a40cf-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="a40cf-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a40cf-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="a40cf-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-285">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-285">Format</span></span>

<span data-ttu-id="a40cf-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-287">Pattern</span></span>

<span data-ttu-id="a40cf-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-289">Checksum</span></span>

<span data-ttu-id="a40cf-290">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-291">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-291">Definition</span></span>

<span data-ttu-id="a40cf-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-293">L’expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-295">Keywords</span></span>

<span data-ttu-id="a40cf-296">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-296"></span></span>
|<span data-ttu-id="a40cf-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-298">passport number</span></span>  <br/> <span data-ttu-id="a40cf-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="a40cf-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="a40cf-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-300">passport no</span></span>  <br/> <span data-ttu-id="a40cf-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="a40cf-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a40cf-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="a40cf-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-303">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-303">Format</span></span>

<span data-ttu-id="a40cf-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-305">Pattern</span></span>

<span data-ttu-id="a40cf-306">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="a40cf-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="a40cf-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-309">Checksum</span></span>

<span data-ttu-id="a40cf-310">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-311">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-311">Definition</span></span>

<span data-ttu-id="a40cf-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-313">L’expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-315">Keywords</span></span>

<span data-ttu-id="a40cf-316">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-316"></span></span>
|<span data-ttu-id="a40cf-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-318">passport number</span></span>  <br/> <span data-ttu-id="a40cf-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="a40cf-319">irish passport number</span></span>  <br/> <span data-ttu-id="a40cf-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-320">passport no</span></span>  <br/> <span data-ttu-id="a40cf-321">boîte</span><span class="sxs-lookup"><span data-stu-id="a40cf-321">pas</span></span>  <br/> <span data-ttu-id="a40cf-322">tel</span><span class="sxs-lookup"><span data-stu-id="a40cf-322">passport</span></span>  <br/> <span data-ttu-id="a40cf-323">passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-323">passeport</span></span>  <br/> <span data-ttu-id="a40cf-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="a40cf-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a40cf-325">Italie</span><span class="sxs-lookup"><span data-stu-id="a40cf-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-326">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-326">Format</span></span>

<span data-ttu-id="a40cf-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-328">Pattern</span></span>

<span data-ttu-id="a40cf-329">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="a40cf-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="a40cf-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-332">Checksum</span></span>

<span data-ttu-id="a40cf-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-334">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-334">Definition</span></span>

<span data-ttu-id="a40cf-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-336">L’expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-338">Keywords</span></span>

<span data-ttu-id="a40cf-339">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-339"></span></span>
|<span data-ttu-id="a40cf-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="a40cf-341">italian passport number</span></span>  <br/> <span data-ttu-id="a40cf-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="a40cf-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="a40cf-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="a40cf-343">passaporto</span></span>  <br/> <span data-ttu-id="a40cf-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="a40cf-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="a40cf-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-345">passport number</span></span>  <br/> <span data-ttu-id="a40cf-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="a40cf-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="a40cf-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="a40cf-347">passaporto numero</span></span>  <br/> <span data-ttu-id="a40cf-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="a40cf-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="a40cf-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="a40cf-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="a40cf-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-351">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-351">Format</span></span>

<span data-ttu-id="a40cf-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-353">Pattern</span></span>

<span data-ttu-id="a40cf-354">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="a40cf-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="a40cf-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-357">Checksum</span></span>

<span data-ttu-id="a40cf-358">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-359">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-359">Definition</span></span>

<span data-ttu-id="a40cf-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-361">L’expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-363">Keywords</span></span>

<span data-ttu-id="a40cf-364">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-364"></span></span>
|<span data-ttu-id="a40cf-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-366">passport number</span></span>  <br/> <span data-ttu-id="a40cf-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="a40cf-367">latvian passport number</span></span>  <br/> <span data-ttu-id="a40cf-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-368">passport no</span></span>  <br/> <span data-ttu-id="a40cf-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a40cf-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="a40cf-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-371">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-371">Format</span></span>

<span data-ttu-id="a40cf-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-373">Pattern</span></span>

<span data-ttu-id="a40cf-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-375">Checksum</span></span>

<span data-ttu-id="a40cf-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-377">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-377">Definition</span></span>

<span data-ttu-id="a40cf-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-379">L’expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-381">Keywords</span></span>

<span data-ttu-id="a40cf-382">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-382"></span></span>
|<span data-ttu-id="a40cf-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-384">passport number</span></span>  <br/> <span data-ttu-id="a40cf-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="a40cf-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="a40cf-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-386">passport no</span></span>  <br/> <span data-ttu-id="a40cf-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a40cf-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="a40cf-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-389">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-389">Format</span></span>

<span data-ttu-id="a40cf-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-391">Pattern</span></span>

<span data-ttu-id="a40cf-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-393">Checksum</span></span>

<span data-ttu-id="a40cf-394">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-395">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-395">Definition</span></span>

<span data-ttu-id="a40cf-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-397">L’expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-399">Keywords</span></span>

<span data-ttu-id="a40cf-400">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-400"></span></span>
|<span data-ttu-id="a40cf-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-402">passport number</span></span>  <br/> <span data-ttu-id="a40cf-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="a40cf-403">latvian passport number</span></span>  <br/> <span data-ttu-id="a40cf-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-404">passport no</span></span>  <br/> <span data-ttu-id="a40cf-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a40cf-406">Malte</span><span class="sxs-lookup"><span data-stu-id="a40cf-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-407">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-407">Format</span></span>

<span data-ttu-id="a40cf-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-409">Pattern</span></span>

 <span data-ttu-id="a40cf-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a40cf-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-411">Checksum</span></span>

<span data-ttu-id="a40cf-412">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-413">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-413">Definition</span></span>

<span data-ttu-id="a40cf-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-415">L’expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-417">Keywords</span></span>

<span data-ttu-id="a40cf-418">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-418"></span></span>
|<span data-ttu-id="a40cf-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-420">passport number</span></span>  <br/> <span data-ttu-id="a40cf-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="a40cf-421">maltese passport number</span></span>  <br/> <span data-ttu-id="a40cf-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-422">passport no</span></span>  <br/> <span data-ttu-id="a40cf-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="a40cf-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a40cf-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="a40cf-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-425">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-425">Format</span></span>

<span data-ttu-id="a40cf-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-427">Pattern</span></span>

<span data-ttu-id="a40cf-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-429">Checksum</span></span>

<span data-ttu-id="a40cf-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-431">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-431">Definition</span></span>

<span data-ttu-id="a40cf-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-433">L’expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-435">Keywords</span></span>

<span data-ttu-id="a40cf-436">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-436"></span></span>
|<span data-ttu-id="a40cf-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="a40cf-438">dutch passport number</span></span>  <br/> <span data-ttu-id="a40cf-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-439">passport number</span></span>  <br/> <span data-ttu-id="a40cf-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="a40cf-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="a40cf-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="a40cf-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="a40cf-442">paspoort</span></span>  <br/> <span data-ttu-id="a40cf-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="a40cf-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="a40cf-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a40cf-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="a40cf-445">Poland</span></span>

<span data-ttu-id="a40cf-446">Pour plus d’informations, reportez-vous à la section « numéro de passeport polonais » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="a40cf-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="a40cf-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-448">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-448">Format</span></span>

<span data-ttu-id="a40cf-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-450">Pattern</span></span>

<span data-ttu-id="a40cf-451">Une lettre suivie de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="a40cf-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="a40cf-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="a40cf-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-454">Checksum</span></span>

<span data-ttu-id="a40cf-455">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-456">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-456">Definition</span></span>

<span data-ttu-id="a40cf-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-458">L’expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-460">Keywords</span></span>

<span data-ttu-id="a40cf-461">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-461"></span></span>
|<span data-ttu-id="a40cf-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-463">passport number</span></span>  <br/> <span data-ttu-id="a40cf-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="a40cf-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="a40cf-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-465">passport no</span></span>  <br/> <span data-ttu-id="a40cf-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="a40cf-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a40cf-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="a40cf-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-468">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-468">Format</span></span>

<span data-ttu-id="a40cf-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-470">Pattern</span></span>

<span data-ttu-id="a40cf-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-472">Checksum</span></span>

<span data-ttu-id="a40cf-473">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-474">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-474">Definition</span></span>

<span data-ttu-id="a40cf-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-476">L’expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-478">Keywords</span></span>

<span data-ttu-id="a40cf-479">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-479"></span></span>
|<span data-ttu-id="a40cf-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-481">passport number</span></span>  <br/> <span data-ttu-id="a40cf-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="a40cf-482">romanian passport number</span></span>  <br/> <span data-ttu-id="a40cf-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-483">passport no</span></span>  <br/> <span data-ttu-id="a40cf-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="a40cf-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a40cf-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="a40cf-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-486">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-486">Format</span></span>

<span data-ttu-id="a40cf-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-488">Pattern</span></span>

<span data-ttu-id="a40cf-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a40cf-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-490">Checksum</span></span>

<span data-ttu-id="a40cf-491">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-492">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-492">Definition</span></span>

<span data-ttu-id="a40cf-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-494">L’expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-496">Keywords</span></span>

<span data-ttu-id="a40cf-497">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-497"></span></span>
|<span data-ttu-id="a40cf-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-499">passport number</span></span>  <br/> <span data-ttu-id="a40cf-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="a40cf-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="a40cf-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-501">passport no</span></span>  <br/> <span data-ttu-id="a40cf-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="a40cf-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a40cf-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="a40cf-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-504">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-504">Format</span></span>

<span data-ttu-id="a40cf-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-506">Pattern</span></span>

<span data-ttu-id="a40cf-507">Deux lettres suivies de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="a40cf-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="a40cf-508">The letter "P"</span></span>
    
- <span data-ttu-id="a40cf-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="a40cf-509">One uppercase letter</span></span>
    
- <span data-ttu-id="a40cf-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-511">Checksum</span></span>

<span data-ttu-id="a40cf-512">Non</span><span class="sxs-lookup"><span data-stu-id="a40cf-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-513">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-513">Definition</span></span>

<span data-ttu-id="a40cf-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-515">L’expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-517">Keywords</span></span>

<span data-ttu-id="a40cf-518">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-518"></span></span>
|<span data-ttu-id="a40cf-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-520">passport number</span></span>  <br/> <span data-ttu-id="a40cf-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="a40cf-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="a40cf-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-522">passport no</span></span>  <br/> <span data-ttu-id="a40cf-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="a40cf-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a40cf-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="a40cf-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a40cf-525">Format</span><span class="sxs-lookup"><span data-stu-id="a40cf-525">Format</span></span>

<span data-ttu-id="a40cf-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="a40cf-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a40cf-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="a40cf-527">Pattern</span></span>

<span data-ttu-id="a40cf-528">Combinaison de huit ou neuf caractères de lettres et de chiffres :</span><span class="sxs-lookup"><span data-stu-id="a40cf-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="a40cf-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="a40cf-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="a40cf-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="a40cf-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="a40cf-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="a40cf-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a40cf-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="a40cf-532">Checksum</span></span>

<span data-ttu-id="a40cf-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a40cf-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a40cf-534">Définition</span><span class="sxs-lookup"><span data-stu-id="a40cf-534">Definition</span></span>

<span data-ttu-id="a40cf-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="a40cf-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a40cf-536">L’expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="a40cf-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a40cf-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="a40cf-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a40cf-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a40cf-538">Keywords</span></span>

<span data-ttu-id="a40cf-539">| |</span><span class="sxs-lookup"><span data-stu-id="a40cf-539"></span></span>
|<span data-ttu-id="a40cf-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="a40cf-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="a40cf-541">tel</span><span class="sxs-lookup"><span data-stu-id="a40cf-541">passport</span></span>  <br/> <span data-ttu-id="a40cf-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="a40cf-542">spain passport</span></span>  <br/> <span data-ttu-id="a40cf-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-543">passport book</span></span>  <br/> <span data-ttu-id="a40cf-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-544">passport number</span></span>  <br/> <span data-ttu-id="a40cf-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a40cf-545">passport no</span></span>  <br/> <span data-ttu-id="a40cf-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="a40cf-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="a40cf-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="a40cf-547">número pasaporte</span></span>  <br/> <span data-ttu-id="a40cf-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="a40cf-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="a40cf-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="a40cf-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a40cf-550">Suède</span><span class="sxs-lookup"><span data-stu-id="a40cf-550">Sweden</span></span>

<span data-ttu-id="a40cf-551">Pour plus d’informations, reportez-vous à la section « numéro de passeport Suède » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="a40cf-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="a40cf-552">UK</span></span>

<span data-ttu-id="a40cf-553">Pour plus d’informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="a40cf-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="a40cf-554">Numéro de passeport» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a40cf-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a40cf-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a40cf-555">See also</span></span>

[<span data-ttu-id="a40cf-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a40cf-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

