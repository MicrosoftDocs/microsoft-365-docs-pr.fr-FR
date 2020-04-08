---
title: Numéro de passeport UE
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 0032d3e50d7dab0b696d9000242e70956469052e
ms.sourcegitcommit: 053d42480d8aa3792ecb0027ddd53d383a029474
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2020
ms.locfileid: "41592115"
---
# <a name="eu-passport-number"></a><span data-ttu-id="8eeaf-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="8eeaf-104">EU Passport Number</span></span>

<span data-ttu-id="8eeaf-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles du numéro de passeport de l’UE.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="8eeaf-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="8eeaf-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="8eeaf-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-108">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-108">Format</span></span>

<span data-ttu-id="8eeaf-109">Une lettre suivie d’un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-110">Pattern</span></span>

<span data-ttu-id="8eeaf-111">Une combinaison d’une lettre, de sept chiffres et d’un espace :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="8eeaf-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="8eeaf-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-113">One space (optional)</span></span>
    
- <span data-ttu-id="8eeaf-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-115">Checksum</span></span>

<span data-ttu-id="8eeaf-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-117">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-117">Definition</span></span>

<span data-ttu-id="8eeaf-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-119">L’expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-121">Keywords</span></span>

<span data-ttu-id="8eeaf-122">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-122">| |</span></span>
|<span data-ttu-id="8eeaf-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-124">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="8eeaf-125">austrian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-126">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="8eeaf-127">reisepass</span></span>  <br/> <span data-ttu-id="8eeaf-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="8eeaf-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="8eeaf-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="8eeaf-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-130">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-130">Format</span></span>

<span data-ttu-id="8eeaf-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-132">Pattern</span></span>

<span data-ttu-id="8eeaf-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-134">Checksum</span></span>

<span data-ttu-id="8eeaf-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-136">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-136">Definition</span></span>

<span data-ttu-id="8eeaf-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-138">L’expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-140">Keywords</span></span>

<span data-ttu-id="8eeaf-141">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-141">| |</span></span>
|<span data-ttu-id="8eeaf-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-143">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="8eeaf-144">belgian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-145">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="8eeaf-146">paspoort</span></span>  <br/> <span data-ttu-id="8eeaf-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="8eeaf-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="8eeaf-148">reisepass kein</span></span>  <br/> <span data-ttu-id="8eeaf-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="8eeaf-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="8eeaf-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-151">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-151">Format</span></span>

<span data-ttu-id="8eeaf-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-153">Pattern</span></span>

 <span data-ttu-id="8eeaf-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-155">Checksum</span></span>

<span data-ttu-id="8eeaf-156">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-157">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-157">Definition</span></span>

<span data-ttu-id="8eeaf-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-159">L’expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-161">Keywords</span></span>

<span data-ttu-id="8eeaf-162">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-162">| |</span></span>
|<span data-ttu-id="8eeaf-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-164">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="8eeaf-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-166">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="8eeaf-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="8eeaf-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-169">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-169">Format</span></span>

<span data-ttu-id="8eeaf-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-171">Pattern</span></span>

 <span data-ttu-id="8eeaf-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-173">Checksum</span></span>

<span data-ttu-id="8eeaf-174">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-175">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-175">Definition</span></span>

<span data-ttu-id="8eeaf-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-177">L’expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-179">Keywords</span></span>

<span data-ttu-id="8eeaf-180">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-180">| |</span></span>
|<span data-ttu-id="8eeaf-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-182">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="8eeaf-183">croatian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-184">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="8eeaf-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="8eeaf-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="8eeaf-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-187">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-187">Format</span></span>

<span data-ttu-id="8eeaf-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-189">Pattern</span></span>

<span data-ttu-id="8eeaf-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-191">Checksum</span></span>

<span data-ttu-id="8eeaf-192">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-193">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-193">Definition</span></span>

<span data-ttu-id="8eeaf-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-195">L’expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-197">Keywords</span></span>

<span data-ttu-id="8eeaf-198">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-198">| |</span></span>
|<span data-ttu-id="8eeaf-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-200">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="8eeaf-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="8eeaf-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-202">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="8eeaf-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="8eeaf-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="8eeaf-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-205">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-205">Format</span></span>

<span data-ttu-id="8eeaf-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-207">Pattern</span></span>

<span data-ttu-id="8eeaf-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-209">Checksum</span></span>

<span data-ttu-id="8eeaf-210">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-211">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-211">Definition</span></span>

<span data-ttu-id="8eeaf-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-213">L’expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-215">Keywords</span></span>

<span data-ttu-id="8eeaf-216">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-216">| |</span></span>
|<span data-ttu-id="8eeaf-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-218">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="8eeaf-219">czech passport number</span></span>  <br/> <span data-ttu-id="8eeaf-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-220">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="8eeaf-221">cestovní pas</span></span>  <br/> <span data-ttu-id="8eeaf-222">boîte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="8eeaf-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="8eeaf-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-224">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-224">Format</span></span>

<span data-ttu-id="8eeaf-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-226">Pattern</span></span>

 <span data-ttu-id="8eeaf-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-228">Checksum</span></span>

<span data-ttu-id="8eeaf-229">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-230">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-230">Definition</span></span>

<span data-ttu-id="8eeaf-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-232">L’expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-234">Keywords</span></span>

<span data-ttu-id="8eeaf-235">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-235">| |</span></span>
|<span data-ttu-id="8eeaf-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-237">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="8eeaf-238">danish passport number</span></span>  <br/> <span data-ttu-id="8eeaf-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-239">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-240">boîte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-240">pas</span></span>  <br/> <span data-ttu-id="8eeaf-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="8eeaf-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-243">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-243">Format</span></span>

<span data-ttu-id="8eeaf-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-245">Pattern</span></span>

<span data-ttu-id="8eeaf-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-247">Checksum</span></span>

<span data-ttu-id="8eeaf-248">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-249">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-249">Definition</span></span>

<span data-ttu-id="8eeaf-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-251">L’expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-253">Keywords</span></span>

<span data-ttu-id="8eeaf-254">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-254">| |</span></span>
|<span data-ttu-id="8eeaf-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-256">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="8eeaf-257">estonian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-258">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="8eeaf-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="8eeaf-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="8eeaf-260">Finland</span></span>

<span data-ttu-id="8eeaf-261">Pour plus d’informations, consultez la section « numéro de passeport de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="8eeaf-262">France</span><span class="sxs-lookup"><span data-stu-id="8eeaf-262">France</span></span>

<span data-ttu-id="8eeaf-263">Pour plus d’informations, consultez la section « numéro de passeport français » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="8eeaf-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="8eeaf-264">Germany</span></span>

<span data-ttu-id="8eeaf-265">Pour plus d’informations, consultez la section « numéro de passeport allemand » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-265">For details, see the section "German Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="8eeaf-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="8eeaf-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-267">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-267">Format</span></span>

<span data-ttu-id="8eeaf-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-269">Pattern</span></span>

<span data-ttu-id="8eeaf-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-271">Checksum</span></span>

<span data-ttu-id="8eeaf-272">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-273">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-273">Definition</span></span>

<span data-ttu-id="8eeaf-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-275">L’expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-277">Keywords</span></span>

<span data-ttu-id="8eeaf-278">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-278">| |</span></span>
|<span data-ttu-id="8eeaf-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-280">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="8eeaf-281">greek passport number</span></span>  <br/> <span data-ttu-id="8eeaf-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-282">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="8eeaf-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="8eeaf-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-285">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-285">Format</span></span>

<span data-ttu-id="8eeaf-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-287">Pattern</span></span>

<span data-ttu-id="8eeaf-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-289">Checksum</span></span>

<span data-ttu-id="8eeaf-290">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-291">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-291">Definition</span></span>

<span data-ttu-id="8eeaf-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-293">L’expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-295">Keywords</span></span>

<span data-ttu-id="8eeaf-296">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-296">| |</span></span>
|<span data-ttu-id="8eeaf-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-298">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="8eeaf-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-300">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="8eeaf-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="8eeaf-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="8eeaf-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-303">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-303">Format</span></span>

<span data-ttu-id="8eeaf-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-305">Pattern</span></span>

<span data-ttu-id="8eeaf-306">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8eeaf-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8eeaf-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-309">Checksum</span></span>

<span data-ttu-id="8eeaf-310">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-311">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-311">Definition</span></span>

<span data-ttu-id="8eeaf-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-313">L’expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-315">Keywords</span></span>

<span data-ttu-id="8eeaf-316">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-316">| |</span></span>
|<span data-ttu-id="8eeaf-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-318">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="8eeaf-319">irish passport number</span></span>  <br/> <span data-ttu-id="8eeaf-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-320">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-321">boîte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-321">pas</span></span>  <br/> <span data-ttu-id="8eeaf-322">tel</span><span class="sxs-lookup"><span data-stu-id="8eeaf-322">passport</span></span>  <br/> <span data-ttu-id="8eeaf-323">passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-323">passeport</span></span>  <br/> <span data-ttu-id="8eeaf-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="8eeaf-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="8eeaf-325">Italie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-326">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-326">Format</span></span>

<span data-ttu-id="8eeaf-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-328">Pattern</span></span>

<span data-ttu-id="8eeaf-329">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8eeaf-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8eeaf-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-332">Checksum</span></span>

<span data-ttu-id="8eeaf-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-334">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-334">Definition</span></span>

<span data-ttu-id="8eeaf-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-336">L’expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-338">Keywords</span></span>

<span data-ttu-id="8eeaf-339">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-339">| |</span></span>
|<span data-ttu-id="8eeaf-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="8eeaf-341">italian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="8eeaf-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="8eeaf-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="8eeaf-343">passaporto</span></span>  <br/> <span data-ttu-id="8eeaf-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="8eeaf-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="8eeaf-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-345">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="8eeaf-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="8eeaf-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="8eeaf-347">passaporto numero</span></span>  <br/> <span data-ttu-id="8eeaf-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="8eeaf-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="8eeaf-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="8eeaf-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-351">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-351">Format</span></span>

<span data-ttu-id="8eeaf-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-353">Pattern</span></span>

<span data-ttu-id="8eeaf-354">Deux lettres ou chiffres suivis de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8eeaf-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8eeaf-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-357">Checksum</span></span>

<span data-ttu-id="8eeaf-358">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-359">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-359">Definition</span></span>

<span data-ttu-id="8eeaf-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-361">L’expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-363">Keywords</span></span>

<span data-ttu-id="8eeaf-364">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-364">| |</span></span>
|<span data-ttu-id="8eeaf-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-366">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="8eeaf-367">latvian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-368">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="8eeaf-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-371">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-371">Format</span></span>

<span data-ttu-id="8eeaf-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-373">Pattern</span></span>

<span data-ttu-id="8eeaf-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-375">Checksum</span></span>

<span data-ttu-id="8eeaf-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-377">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-377">Definition</span></span>

<span data-ttu-id="8eeaf-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-379">L’expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-381">Keywords</span></span>

<span data-ttu-id="8eeaf-382">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-382">| |</span></span>
|<span data-ttu-id="8eeaf-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-384">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="8eeaf-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-386">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="8eeaf-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="8eeaf-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-389">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-389">Format</span></span>

<span data-ttu-id="8eeaf-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-391">Pattern</span></span>

<span data-ttu-id="8eeaf-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-393">Checksum</span></span>

<span data-ttu-id="8eeaf-394">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-395">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-395">Definition</span></span>

<span data-ttu-id="8eeaf-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-397">L’expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-399">Keywords</span></span>

<span data-ttu-id="8eeaf-400">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-400">| |</span></span>
|<span data-ttu-id="8eeaf-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-402">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="8eeaf-403">latvian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-404">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="8eeaf-406">Malte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-407">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-407">Format</span></span>

<span data-ttu-id="8eeaf-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-409">Pattern</span></span>

 <span data-ttu-id="8eeaf-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-411">Checksum</span></span>

<span data-ttu-id="8eeaf-412">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-413">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-413">Definition</span></span>

<span data-ttu-id="8eeaf-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-415">L’expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-417">Keywords</span></span>

<span data-ttu-id="8eeaf-418">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-418">| |</span></span>
|<span data-ttu-id="8eeaf-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-420">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="8eeaf-421">maltese passport number</span></span>  <br/> <span data-ttu-id="8eeaf-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-422">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="8eeaf-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="8eeaf-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-425">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-425">Format</span></span>

<span data-ttu-id="8eeaf-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-427">Pattern</span></span>

<span data-ttu-id="8eeaf-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-429">Checksum</span></span>

<span data-ttu-id="8eeaf-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-431">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-431">Definition</span></span>

<span data-ttu-id="8eeaf-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-433">L’expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-435">Keywords</span></span>

<span data-ttu-id="8eeaf-436">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-436">| |</span></span>
|<span data-ttu-id="8eeaf-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="8eeaf-438">dutch passport number</span></span>  <br/> <span data-ttu-id="8eeaf-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-439">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="8eeaf-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="8eeaf-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="8eeaf-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="8eeaf-442">paspoort</span></span>  <br/> <span data-ttu-id="8eeaf-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="8eeaf-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="8eeaf-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="8eeaf-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="8eeaf-445">Poland</span></span>

<span data-ttu-id="8eeaf-446">Pour plus d’informations, reportez-vous à la section « numéro de passeport polonais » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="8eeaf-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="8eeaf-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-448">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-448">Format</span></span>

<span data-ttu-id="8eeaf-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-450">Pattern</span></span>

<span data-ttu-id="8eeaf-451">Une lettre suivie de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="8eeaf-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="8eeaf-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-454">Checksum</span></span>

<span data-ttu-id="8eeaf-455">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-456">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-456">Definition</span></span>

<span data-ttu-id="8eeaf-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-458">L’expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-460">Keywords</span></span>

<span data-ttu-id="8eeaf-461">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-461">| |</span></span>
|<span data-ttu-id="8eeaf-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-463">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="8eeaf-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="8eeaf-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-465">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="8eeaf-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-468">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-468">Format</span></span>

<span data-ttu-id="8eeaf-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-470">Pattern</span></span>

<span data-ttu-id="8eeaf-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-472">Checksum</span></span>

<span data-ttu-id="8eeaf-473">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-474">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-474">Definition</span></span>

<span data-ttu-id="8eeaf-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-476">L’expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-478">Keywords</span></span>

<span data-ttu-id="8eeaf-479">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-479">| |</span></span>
|<span data-ttu-id="8eeaf-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-481">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="8eeaf-482">romanian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-483">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="8eeaf-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="8eeaf-485">Slovaquie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-486">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-486">Format</span></span>

<span data-ttu-id="8eeaf-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-488">Pattern</span></span>

<span data-ttu-id="8eeaf-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8eeaf-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-490">Checksum</span></span>

<span data-ttu-id="8eeaf-491">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-492">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-492">Definition</span></span>

<span data-ttu-id="8eeaf-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-494">L’expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-496">Keywords</span></span>

<span data-ttu-id="8eeaf-497">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-497">| |</span></span>
|<span data-ttu-id="8eeaf-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-499">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="8eeaf-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-501">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="8eeaf-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="8eeaf-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="8eeaf-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-504">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-504">Format</span></span>

<span data-ttu-id="8eeaf-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-506">Pattern</span></span>

<span data-ttu-id="8eeaf-507">Deux lettres suivies de sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="8eeaf-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="8eeaf-508">The letter "P"</span></span>
    
- <span data-ttu-id="8eeaf-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="8eeaf-509">One uppercase letter</span></span>
    
- <span data-ttu-id="8eeaf-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-511">Checksum</span></span>

<span data-ttu-id="8eeaf-512">Non</span><span class="sxs-lookup"><span data-stu-id="8eeaf-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-513">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-513">Definition</span></span>

<span data-ttu-id="8eeaf-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-515">L’expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-517">Keywords</span></span>

<span data-ttu-id="8eeaf-518">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-518">| |</span></span>
|<span data-ttu-id="8eeaf-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-520">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="8eeaf-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="8eeaf-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-522">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="8eeaf-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="8eeaf-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="8eeaf-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="8eeaf-525">Format</span><span class="sxs-lookup"><span data-stu-id="8eeaf-525">Format</span></span>

<span data-ttu-id="8eeaf-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8eeaf-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8eeaf-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-527">Pattern</span></span>

<span data-ttu-id="8eeaf-528">Combinaison de huit ou neuf caractères de lettres et de chiffres :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="8eeaf-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="8eeaf-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="8eeaf-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="8eeaf-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="8eeaf-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8eeaf-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8eeaf-532">Checksum</span></span>

<span data-ttu-id="8eeaf-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8eeaf-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8eeaf-534">Définition</span><span class="sxs-lookup"><span data-stu-id="8eeaf-534">Definition</span></span>

<span data-ttu-id="8eeaf-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8eeaf-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8eeaf-536">L’expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8eeaf-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8eeaf-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8eeaf-538">Keywords</span></span>

<span data-ttu-id="8eeaf-539">| |</span><span class="sxs-lookup"><span data-stu-id="8eeaf-539">| |</span></span>
|<span data-ttu-id="8eeaf-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="8eeaf-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8eeaf-541">tel</span><span class="sxs-lookup"><span data-stu-id="8eeaf-541">passport</span></span>  <br/> <span data-ttu-id="8eeaf-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="8eeaf-542">spain passport</span></span>  <br/> <span data-ttu-id="8eeaf-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-543">passport book</span></span>  <br/> <span data-ttu-id="8eeaf-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-544">passport number</span></span>  <br/> <span data-ttu-id="8eeaf-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="8eeaf-545">passport no</span></span>  <br/> <span data-ttu-id="8eeaf-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="8eeaf-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-547">número pasaporte</span></span>  <br/> <span data-ttu-id="8eeaf-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="8eeaf-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="8eeaf-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="8eeaf-550">Suède</span><span class="sxs-lookup"><span data-stu-id="8eeaf-550">Sweden</span></span>

<span data-ttu-id="8eeaf-551">Pour plus d’informations, reportez-vous à la section « numéro de passeport Suède » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="8eeaf-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-552">UK</span></span>

<span data-ttu-id="8eeaf-553">Pour plus d’informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="8eeaf-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="8eeaf-554">Numéro de passeport» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8eeaf-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8eeaf-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8eeaf-555">See also</span></span>

[<span data-ttu-id="8eeaf-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="8eeaf-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

