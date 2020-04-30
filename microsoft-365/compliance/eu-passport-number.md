---
title: Numéro de passeport UE
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 56eb79dd067ca89600f92ea57eaaf01e562f9388
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43938738"
---
# <a name="eu-passport-number"></a><span data-ttu-id="d8fbd-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="d8fbd-104">EU Passport Number</span></span>

<span data-ttu-id="d8fbd-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="d8fbd-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d8fbd-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d8fbd-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-108">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-108">Format</span></span>

<span data-ttu-id="d8fbd-109">Une lettre suivie d’un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-110">Pattern</span></span>

<span data-ttu-id="d8fbd-111">Une combinaison d’une lettre, de sept chiffres et d’un espace :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="d8fbd-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d8fbd-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-113">One space (optional)</span></span>
    
- <span data-ttu-id="d8fbd-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-115">Checksum</span></span>

<span data-ttu-id="d8fbd-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-117">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-117">Definition</span></span>

<span data-ttu-id="d8fbd-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-119">L’expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-121">Keywords</span></span>

<span data-ttu-id="d8fbd-122">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-122">| |</span></span>
|<span data-ttu-id="d8fbd-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-124">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="d8fbd-125">austrian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-126">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="d8fbd-127">reisepass</span></span>  <br/> <span data-ttu-id="d8fbd-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="d8fbd-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="d8fbd-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="d8fbd-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-130">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-130">Format</span></span>

<span data-ttu-id="d8fbd-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-132">Pattern</span></span>

<span data-ttu-id="d8fbd-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-134">Checksum</span></span>

<span data-ttu-id="d8fbd-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-136">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-136">Definition</span></span>

<span data-ttu-id="d8fbd-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-138">L’expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-140">Keywords</span></span>

<span data-ttu-id="d8fbd-141">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-141">| |</span></span>
|<span data-ttu-id="d8fbd-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-143">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="d8fbd-144">belgian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-145">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="d8fbd-146">paspoort</span></span>  <br/> <span data-ttu-id="d8fbd-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="d8fbd-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="d8fbd-148">reisepass kein</span></span>  <br/> <span data-ttu-id="d8fbd-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="d8fbd-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="d8fbd-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-151">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-151">Format</span></span>

<span data-ttu-id="d8fbd-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-153">Pattern</span></span>

 <span data-ttu-id="d8fbd-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-155">Checksum</span></span>

<span data-ttu-id="d8fbd-156">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-157">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-157">Definition</span></span>

<span data-ttu-id="d8fbd-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-159">L’expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-161">Keywords</span></span>

<span data-ttu-id="d8fbd-162">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-162">| |</span></span>
|<span data-ttu-id="d8fbd-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-164">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="d8fbd-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-166">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="d8fbd-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="d8fbd-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-169">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-169">Format</span></span>

<span data-ttu-id="d8fbd-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-171">Pattern</span></span>

 <span data-ttu-id="d8fbd-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-173">Checksum</span></span>

<span data-ttu-id="d8fbd-174">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-175">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-175">Definition</span></span>

<span data-ttu-id="d8fbd-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-177">L’expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-179">Keywords</span></span>

<span data-ttu-id="d8fbd-180">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-180">| |</span></span>
|<span data-ttu-id="d8fbd-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-182">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="d8fbd-183">croatian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-184">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="d8fbd-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="d8fbd-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="d8fbd-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-187">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-187">Format</span></span>

<span data-ttu-id="d8fbd-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-189">Pattern</span></span>

<span data-ttu-id="d8fbd-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-191">Checksum</span></span>

<span data-ttu-id="d8fbd-192">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-193">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-193">Definition</span></span>

<span data-ttu-id="d8fbd-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-195">L’expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-197">Keywords</span></span>

<span data-ttu-id="d8fbd-198">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-198">| |</span></span>
|<span data-ttu-id="d8fbd-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-200">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="d8fbd-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="d8fbd-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-202">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="d8fbd-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="d8fbd-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d8fbd-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-205">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-205">Format</span></span>

<span data-ttu-id="d8fbd-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-207">Pattern</span></span>

<span data-ttu-id="d8fbd-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-209">Checksum</span></span>

<span data-ttu-id="d8fbd-210">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-211">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-211">Definition</span></span>

<span data-ttu-id="d8fbd-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-213">L’expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-215">Keywords</span></span>

<span data-ttu-id="d8fbd-216">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-216">| |</span></span>
|<span data-ttu-id="d8fbd-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-218">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="d8fbd-219">czech passport number</span></span>  <br/> <span data-ttu-id="d8fbd-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-220">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="d8fbd-221">cestovní pas</span></span>  <br/> <span data-ttu-id="d8fbd-222">boîte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="d8fbd-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="d8fbd-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-224">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-224">Format</span></span>

<span data-ttu-id="d8fbd-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-226">Pattern</span></span>

 <span data-ttu-id="d8fbd-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-228">Checksum</span></span>

<span data-ttu-id="d8fbd-229">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-230">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-230">Definition</span></span>

<span data-ttu-id="d8fbd-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-232">L’expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-234">Keywords</span></span>

<span data-ttu-id="d8fbd-235">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-235">| |</span></span>
|<span data-ttu-id="d8fbd-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-237">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="d8fbd-238">danish passport number</span></span>  <br/> <span data-ttu-id="d8fbd-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-239">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-240">boîte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-240">pas</span></span>  <br/> <span data-ttu-id="d8fbd-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="d8fbd-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-243">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-243">Format</span></span>

<span data-ttu-id="d8fbd-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-245">Pattern</span></span>

<span data-ttu-id="d8fbd-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-247">Checksum</span></span>

<span data-ttu-id="d8fbd-248">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-249">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-249">Definition</span></span>

<span data-ttu-id="d8fbd-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-251">L’expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-253">Keywords</span></span>

<span data-ttu-id="d8fbd-254">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-254">| |</span></span>
|<span data-ttu-id="d8fbd-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-256">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="d8fbd-257">estonian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-258">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="d8fbd-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="d8fbd-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="d8fbd-260">Finland</span></span>

<span data-ttu-id="d8fbd-261">Pour plus d’informations, consultez la section « numéro de passeport de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="d8fbd-262">France</span><span class="sxs-lookup"><span data-stu-id="d8fbd-262">France</span></span>

<span data-ttu-id="d8fbd-263">Pour plus d’informations, consultez la section « numéro de passeport français » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="d8fbd-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d8fbd-264">Germany</span></span>

<span data-ttu-id="d8fbd-265">Pour plus d’informations, consultez la section « numéro de passeport allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-265">For details, see the section "German Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="d8fbd-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="d8fbd-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-267">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-267">Format</span></span>

<span data-ttu-id="d8fbd-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-269">Pattern</span></span>

<span data-ttu-id="d8fbd-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-271">Checksum</span></span>

<span data-ttu-id="d8fbd-272">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-273">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-273">Definition</span></span>

<span data-ttu-id="d8fbd-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-275">L’expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-277">Keywords</span></span>

<span data-ttu-id="d8fbd-278">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-278">| |</span></span>
|<span data-ttu-id="d8fbd-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-280">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="d8fbd-281">greek passport number</span></span>  <br/> <span data-ttu-id="d8fbd-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-282">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="d8fbd-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="d8fbd-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-285">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-285">Format</span></span>

<span data-ttu-id="d8fbd-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-287">Pattern</span></span>

<span data-ttu-id="d8fbd-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-289">Checksum</span></span>

<span data-ttu-id="d8fbd-290">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-291">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-291">Definition</span></span>

<span data-ttu-id="d8fbd-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-293">L’expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-295">Keywords</span></span>

<span data-ttu-id="d8fbd-296">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-296">| |</span></span>
|<span data-ttu-id="d8fbd-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-298">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="d8fbd-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-300">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="d8fbd-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="d8fbd-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="d8fbd-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-303">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-303">Format</span></span>

<span data-ttu-id="d8fbd-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-305">Pattern</span></span>

<span data-ttu-id="d8fbd-306">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d8fbd-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d8fbd-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-309">Checksum</span></span>

<span data-ttu-id="d8fbd-310">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-311">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-311">Definition</span></span>

<span data-ttu-id="d8fbd-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-313">L’expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-315">Keywords</span></span>

<span data-ttu-id="d8fbd-316">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-316">| |</span></span>
|<span data-ttu-id="d8fbd-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-318">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="d8fbd-319">irish passport number</span></span>  <br/> <span data-ttu-id="d8fbd-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-320">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-321">boîte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-321">pas</span></span>  <br/> <span data-ttu-id="d8fbd-322">tel</span><span class="sxs-lookup"><span data-stu-id="d8fbd-322">passport</span></span>  <br/> <span data-ttu-id="d8fbd-323">passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-323">passeport</span></span>  <br/> <span data-ttu-id="d8fbd-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="d8fbd-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="d8fbd-325">Italie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-326">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-326">Format</span></span>

<span data-ttu-id="d8fbd-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-328">Pattern</span></span>

<span data-ttu-id="d8fbd-329">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d8fbd-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d8fbd-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-332">Checksum</span></span>

<span data-ttu-id="d8fbd-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-334">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-334">Definition</span></span>

<span data-ttu-id="d8fbd-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-336">L’expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-338">Keywords</span></span>

<span data-ttu-id="d8fbd-339">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-339">| |</span></span>
|<span data-ttu-id="d8fbd-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="d8fbd-341">italian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="d8fbd-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="d8fbd-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="d8fbd-343">passaporto</span></span>  <br/> <span data-ttu-id="d8fbd-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="d8fbd-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="d8fbd-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-345">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d8fbd-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="d8fbd-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d8fbd-347">passaporto numero</span></span>  <br/> <span data-ttu-id="d8fbd-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="d8fbd-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="d8fbd-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="d8fbd-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-351">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-351">Format</span></span>

<span data-ttu-id="d8fbd-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-353">Pattern</span></span>

<span data-ttu-id="d8fbd-354">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d8fbd-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d8fbd-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-357">Checksum</span></span>

<span data-ttu-id="d8fbd-358">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-359">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-359">Definition</span></span>

<span data-ttu-id="d8fbd-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-361">L’expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-363">Keywords</span></span>

<span data-ttu-id="d8fbd-364">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-364">| |</span></span>
|<span data-ttu-id="d8fbd-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-366">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d8fbd-367">latvian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-368">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="d8fbd-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-371">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-371">Format</span></span>

<span data-ttu-id="d8fbd-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-373">Pattern</span></span>

<span data-ttu-id="d8fbd-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-375">Checksum</span></span>

<span data-ttu-id="d8fbd-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-377">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-377">Definition</span></span>

<span data-ttu-id="d8fbd-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-379">L’expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-381">Keywords</span></span>

<span data-ttu-id="d8fbd-382">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-382">| |</span></span>
|<span data-ttu-id="d8fbd-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-384">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="d8fbd-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-386">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="d8fbd-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="d8fbd-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-389">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-389">Format</span></span>

<span data-ttu-id="d8fbd-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-391">Pattern</span></span>

<span data-ttu-id="d8fbd-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-393">Checksum</span></span>

<span data-ttu-id="d8fbd-394">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-395">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-395">Definition</span></span>

<span data-ttu-id="d8fbd-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-397">L’expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-399">Keywords</span></span>

<span data-ttu-id="d8fbd-400">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-400">| |</span></span>
|<span data-ttu-id="d8fbd-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-402">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d8fbd-403">latvian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-404">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="d8fbd-406">Malte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-407">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-407">Format</span></span>

<span data-ttu-id="d8fbd-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-409">Pattern</span></span>

 <span data-ttu-id="d8fbd-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-411">Checksum</span></span>

<span data-ttu-id="d8fbd-412">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-413">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-413">Definition</span></span>

<span data-ttu-id="d8fbd-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-415">L’expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-417">Keywords</span></span>

<span data-ttu-id="d8fbd-418">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-418">| |</span></span>
|<span data-ttu-id="d8fbd-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-420">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="d8fbd-421">maltese passport number</span></span>  <br/> <span data-ttu-id="d8fbd-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-422">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="d8fbd-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d8fbd-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-425">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-425">Format</span></span>

<span data-ttu-id="d8fbd-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-427">Pattern</span></span>

<span data-ttu-id="d8fbd-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-429">Checksum</span></span>

<span data-ttu-id="d8fbd-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-431">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-431">Definition</span></span>

<span data-ttu-id="d8fbd-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-433">L’expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-435">Keywords</span></span>

<span data-ttu-id="d8fbd-436">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-436">| |</span></span>
|<span data-ttu-id="d8fbd-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d8fbd-438">dutch passport number</span></span>  <br/> <span data-ttu-id="d8fbd-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-439">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d8fbd-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="d8fbd-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="d8fbd-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="d8fbd-442">paspoort</span></span>  <br/> <span data-ttu-id="d8fbd-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="d8fbd-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d8fbd-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="d8fbd-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="d8fbd-445">Poland</span></span>

<span data-ttu-id="d8fbd-446">Pour plus d’informations, reportez-vous à la section « numéro de passeport polonais » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d8fbd-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="d8fbd-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-448">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-448">Format</span></span>

<span data-ttu-id="d8fbd-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-450">Pattern</span></span>

<span data-ttu-id="d8fbd-451">Une lettre suivie de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="d8fbd-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d8fbd-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-454">Checksum</span></span>

<span data-ttu-id="d8fbd-455">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-456">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-456">Definition</span></span>

<span data-ttu-id="d8fbd-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-458">L’expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-460">Keywords</span></span>

<span data-ttu-id="d8fbd-461">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-461">| |</span></span>
|<span data-ttu-id="d8fbd-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-463">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="d8fbd-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="d8fbd-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-465">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="d8fbd-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-468">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-468">Format</span></span>

<span data-ttu-id="d8fbd-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-470">Pattern</span></span>

<span data-ttu-id="d8fbd-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-472">Checksum</span></span>

<span data-ttu-id="d8fbd-473">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-474">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-474">Definition</span></span>

<span data-ttu-id="d8fbd-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-476">L’expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-478">Keywords</span></span>

<span data-ttu-id="d8fbd-479">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-479">| |</span></span>
|<span data-ttu-id="d8fbd-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-481">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="d8fbd-482">romanian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-483">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="d8fbd-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="d8fbd-485">Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-486">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-486">Format</span></span>

<span data-ttu-id="d8fbd-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-488">Pattern</span></span>

<span data-ttu-id="d8fbd-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d8fbd-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-490">Checksum</span></span>

<span data-ttu-id="d8fbd-491">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-492">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-492">Definition</span></span>

<span data-ttu-id="d8fbd-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-494">L’expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-496">Keywords</span></span>

<span data-ttu-id="d8fbd-497">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-497">| |</span></span>
|<span data-ttu-id="d8fbd-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-499">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="d8fbd-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-501">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="d8fbd-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="d8fbd-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d8fbd-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-504">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-504">Format</span></span>

<span data-ttu-id="d8fbd-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-506">Pattern</span></span>

<span data-ttu-id="d8fbd-507">Deux lettres suivies de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="d8fbd-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="d8fbd-508">The letter "P"</span></span>
    
- <span data-ttu-id="d8fbd-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="d8fbd-509">One uppercase letter</span></span>
    
- <span data-ttu-id="d8fbd-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-511">Checksum</span></span>

<span data-ttu-id="d8fbd-512">Non</span><span class="sxs-lookup"><span data-stu-id="d8fbd-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-513">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-513">Definition</span></span>

<span data-ttu-id="d8fbd-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-515">L’expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-517">Keywords</span></span>

<span data-ttu-id="d8fbd-518">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-518">| |</span></span>
|<span data-ttu-id="d8fbd-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-520">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="d8fbd-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="d8fbd-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-522">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="d8fbd-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="d8fbd-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="d8fbd-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="d8fbd-525">Format</span><span class="sxs-lookup"><span data-stu-id="d8fbd-525">Format</span></span>

<span data-ttu-id="d8fbd-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8fbd-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d8fbd-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-527">Pattern</span></span>

<span data-ttu-id="d8fbd-528">Combinaison de huit ou neuf caractères de lettres et de chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="d8fbd-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="d8fbd-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d8fbd-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="d8fbd-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8fbd-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d8fbd-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8fbd-532">Checksum</span></span>

<span data-ttu-id="d8fbd-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d8fbd-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d8fbd-534">Définition</span><span class="sxs-lookup"><span data-stu-id="d8fbd-534">Definition</span></span>

<span data-ttu-id="d8fbd-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8fbd-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d8fbd-536">L’expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d8fbd-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8fbd-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8fbd-538">Keywords</span></span>

<span data-ttu-id="d8fbd-539">| |</span><span class="sxs-lookup"><span data-stu-id="d8fbd-539">| |</span></span>
|<span data-ttu-id="d8fbd-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d8fbd-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d8fbd-541">tel</span><span class="sxs-lookup"><span data-stu-id="d8fbd-541">passport</span></span>  <br/> <span data-ttu-id="d8fbd-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="d8fbd-542">spain passport</span></span>  <br/> <span data-ttu-id="d8fbd-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-543">passport book</span></span>  <br/> <span data-ttu-id="d8fbd-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-544">passport number</span></span>  <br/> <span data-ttu-id="d8fbd-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8fbd-545">passport no</span></span>  <br/> <span data-ttu-id="d8fbd-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="d8fbd-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-547">número pasaporte</span></span>  <br/> <span data-ttu-id="d8fbd-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="d8fbd-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="d8fbd-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="d8fbd-550">Suède</span><span class="sxs-lookup"><span data-stu-id="d8fbd-550">Sweden</span></span>

<span data-ttu-id="d8fbd-551">Pour plus d’informations, reportez-vous à la section « numéro de passeport Suède » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="d8fbd-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-552">UK</span></span>

<span data-ttu-id="d8fbd-553">Pour plus d’informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="d8fbd-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="d8fbd-554">Numéro de passeport» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbd-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8fbd-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8fbd-555">See also</span></span>

[<span data-ttu-id="d8fbd-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d8fbd-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

