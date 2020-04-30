---
title: Numéro d’identification fiscale de l’UE
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
description: Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles du numéro d’identification fiscale de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 5f779974266045d7099b599700c7168162d9d81e
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43938670"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="277d2-104">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="277d2-104">EU Tax Identification Number</span></span>

<span data-ttu-id="277d2-105">Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles de l’ID taxe de l’UE (TIN).</span><span class="sxs-lookup"><span data-stu-id="277d2-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="277d2-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="277d2-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="277d2-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="277d2-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="277d2-108">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-108">Format</span></span>

<span data-ttu-id="277d2-109">Neuf chiffres avec un trait d’union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="277d2-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-110">Pattern</span></span>

<span data-ttu-id="277d2-111">Neuf chiffres avec un trait d’Union et une barre oblique facultatifs :</span><span class="sxs-lookup"><span data-stu-id="277d2-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="277d2-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-112">Two digits</span></span> 
    
- <span data-ttu-id="277d2-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="277d2-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="277d2-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-114">Three digits</span></span>
    
- <span data-ttu-id="277d2-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="277d2-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="277d2-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-117">Checksum</span></span>

<span data-ttu-id="277d2-118">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-119">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-119">Definition</span></span>

<span data-ttu-id="277d2-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-125">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-125">Keywords</span></span>

#### <a name="keywords_austria_eu_tax_file_number"></a><span data-ttu-id="277d2-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-127">tax number</span></span>
  
<span data-ttu-id="277d2-128">number</span><span class="sxs-lookup"><span data-stu-id="277d2-128">number</span></span>
  
<span data-ttu-id="277d2-129">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-129">tax registration number</span></span>
  
<span data-ttu-id="277d2-130">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-130">tax id</span></span>
  
<span data-ttu-id="277d2-131">st.nr.</span><span class="sxs-lookup"><span data-stu-id="277d2-131">st.nr.</span></span>
  
<span data-ttu-id="277d2-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="277d2-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="277d2-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="277d2-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="277d2-134">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-134">Format</span></span>

<span data-ttu-id="277d2-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-136">Pattern</span></span>

<span data-ttu-id="277d2-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-137">11 digits:</span></span>
  
- <span data-ttu-id="277d2-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-138">Two digits</span></span>
    
- <span data-ttu-id="277d2-139">« 0 » ou « 1 »</span><span class="sxs-lookup"><span data-stu-id="277d2-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="277d2-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="277d2-140">One digit</span></span>
    
- <span data-ttu-id="277d2-141">« 0 » ou « 1 » ou « 2 » ou « 3 »</span><span class="sxs-lookup"><span data-stu-id="277d2-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="277d2-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-143">Checksum</span></span>

<span data-ttu-id="277d2-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-145">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-145">Definition</span></span>

<span data-ttu-id="277d2-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-147">L’expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-149">Keywords</span></span>

#### <a name="keywords_belgium_eu_tax_file_number"></a><span data-ttu-id="277d2-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-151">tax number</span></span>
  
<span data-ttu-id="277d2-152">Numéro d’enregistrement national</span><span class="sxs-lookup"><span data-stu-id="277d2-152">national registration number</span></span>
  
<span data-ttu-id="277d2-153">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-153">tax registration number</span></span>
  
<span data-ttu-id="277d2-154">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-154">tax id</span></span>
  
<span data-ttu-id="277d2-155">nPour</span><span class="sxs-lookup"><span data-stu-id="277d2-155">nif</span></span>
  
<span data-ttu-id="277d2-156">nPour #</span><span class="sxs-lookup"><span data-stu-id="277d2-156">nif#</span></span>
  
<span data-ttu-id="277d2-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="277d2-157">numéro de registre national</span></span>
  
<span data-ttu-id="277d2-158">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="277d2-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="277d2-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="277d2-160">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-160">Format</span></span>

<span data-ttu-id="277d2-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-162">Pattern</span></span>

<span data-ttu-id="277d2-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-164">Checksum</span></span>

<span data-ttu-id="277d2-165">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-166">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-166">Definition</span></span>

<span data-ttu-id="277d2-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-172">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-172">Keywords</span></span>

#### <a name="keywords_bulgaria_eu_tax_file_number"></a><span data-ttu-id="277d2-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-174">bucn</span><span class="sxs-lookup"><span data-stu-id="277d2-174">bucn</span></span>
  
<span data-ttu-id="277d2-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="277d2-175">uniform civil number</span></span>
  
<span data-ttu-id="277d2-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="277d2-176">bucn#</span></span>
  
<span data-ttu-id="277d2-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="277d2-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="277d2-178">uniform civil id</span></span>
  
<span data-ttu-id="277d2-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="277d2-179">uniform civil no</span></span>
  
<span data-ttu-id="277d2-180">egn</span><span class="sxs-lookup"><span data-stu-id="277d2-180">egn</span></span>
  
<span data-ttu-id="277d2-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="277d2-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="277d2-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="277d2-182">uniformcivilno#</span></span>
  
<span data-ttu-id="277d2-183">egn #</span><span class="sxs-lookup"><span data-stu-id="277d2-183">egn#</span></span>
  
<span data-ttu-id="277d2-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="277d2-184">униформ граждански номер</span></span>
  
<span data-ttu-id="277d2-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="277d2-185">униформ id</span></span>
  
<span data-ttu-id="277d2-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="277d2-186">униформ граждански id</span></span>
  
<span data-ttu-id="277d2-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="277d2-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="277d2-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="277d2-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="277d2-189">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-189">Format</span></span>

<span data-ttu-id="277d2-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-191">Pattern</span></span>

<span data-ttu-id="277d2-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-192">11 digits:</span></span>
  
- <span data-ttu-id="277d2-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="277d2-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="277d2-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-195">Checksum</span></span>

<span data-ttu-id="277d2-196">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-197">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-197">Definition</span></span>

<span data-ttu-id="277d2-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-203">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-203">Keywords</span></span>

#### <a name="keywords_croatia_eu_tax_file_number"></a><span data-ttu-id="277d2-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-205">tax number</span></span>
  
<span data-ttu-id="277d2-206">codes</span><span class="sxs-lookup"><span data-stu-id="277d2-206">tax</span></span>
  
<span data-ttu-id="277d2-207">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-207">tax id</span></span>
  
<span data-ttu-id="277d2-208">oid</span><span class="sxs-lookup"><span data-stu-id="277d2-208">oid</span></span>
  
<span data-ttu-id="277d2-209">OID #</span><span class="sxs-lookup"><span data-stu-id="277d2-209">oid#</span></span>
  
<span data-ttu-id="277d2-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="277d2-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="277d2-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="277d2-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="277d2-212">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-212">Format</span></span>

<span data-ttu-id="277d2-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-214">Pattern</span></span>

<span data-ttu-id="277d2-215">Huit chiffres et une lettre :</span><span class="sxs-lookup"><span data-stu-id="277d2-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="277d2-216">« 0 »</span><span class="sxs-lookup"><span data-stu-id="277d2-216">A "0"</span></span> 
    
- <span data-ttu-id="277d2-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-217">Seven digits</span></span>
    
- <span data-ttu-id="277d2-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-219">Checksum</span></span>

<span data-ttu-id="277d2-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-221">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-221">Definition</span></span>

<span data-ttu-id="277d2-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-227">Keywords</span></span>

#### <a name="keywords_cyprus_eu_tax_file_number"></a><span data-ttu-id="277d2-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-229">tax number</span></span>
  
<span data-ttu-id="277d2-230">codes</span><span class="sxs-lookup"><span data-stu-id="277d2-230">tax</span></span>
  
<span data-ttu-id="277d2-231">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-231">tax id</span></span>
  
<span data-ttu-id="277d2-232">code d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-232">tax identification code</span></span>
  
<span data-ttu-id="277d2-233">graduation</span><span class="sxs-lookup"><span data-stu-id="277d2-233">tic</span></span>
  
<span data-ttu-id="277d2-234">graduation #</span><span class="sxs-lookup"><span data-stu-id="277d2-234">tic#</span></span>
  
<span data-ttu-id="277d2-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="277d2-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="277d2-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="277d2-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="277d2-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="277d2-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="277d2-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="277d2-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="277d2-239">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-239">Format</span></span>

<span data-ttu-id="277d2-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="277d2-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-241">Pattern</span></span>

<span data-ttu-id="277d2-242">Neuf ou dix chiffres avec une barre oblique inverse facultative :</span><span class="sxs-lookup"><span data-stu-id="277d2-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="277d2-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-243">Six digits</span></span> 
    
- <span data-ttu-id="277d2-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="277d2-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="277d2-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-246">Checksum</span></span>

<span data-ttu-id="277d2-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-248">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-248">Definition</span></span>

<span data-ttu-id="277d2-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-250">L’expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-252">Keywords</span></span>

#### <a name="keywords_czech_republic_eu_tax_file_number"></a><span data-ttu-id="277d2-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-254">tax number</span></span>
  
<span data-ttu-id="277d2-255">codes</span><span class="sxs-lookup"><span data-stu-id="277d2-255">tax</span></span>
  
<span data-ttu-id="277d2-256">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-256">tax id</span></span>
  
<span data-ttu-id="277d2-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-257">personal number</span></span>
  
<span data-ttu-id="277d2-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="277d2-258">daňové číslo</span></span>
  
<span data-ttu-id="277d2-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="277d2-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="277d2-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="277d2-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="277d2-261">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-261">Format</span></span>

<span data-ttu-id="277d2-262">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="277d2-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-263">Pattern</span></span>

<span data-ttu-id="277d2-264">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="277d2-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="277d2-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="277d2-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="277d2-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="277d2-266">A hyphen</span></span>
    
- <span data-ttu-id="277d2-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l’individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="277d2-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-268">Checksum</span></span>

<span data-ttu-id="277d2-269">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-270">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-270">Definition</span></span>

<span data-ttu-id="277d2-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-276">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-276">Keywords</span></span>

#### <a name="keywords_denmark_eu_tax_file_number"></a><span data-ttu-id="277d2-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-278">tax number</span></span>
  
<span data-ttu-id="277d2-279">codes</span><span class="sxs-lookup"><span data-stu-id="277d2-279">tax</span></span>
  
<span data-ttu-id="277d2-280">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-280">tax id</span></span>
  
<span data-ttu-id="277d2-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="277d2-281">cpr number</span></span>
  
<span data-ttu-id="277d2-282">cardio #</span><span class="sxs-lookup"><span data-stu-id="277d2-282">cpr#</span></span>
  
<span data-ttu-id="277d2-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="277d2-283">skat nummer</span></span>
  
<span data-ttu-id="277d2-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="277d2-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="277d2-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="277d2-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="277d2-286">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-286">Format</span></span>

<span data-ttu-id="277d2-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-288">Pattern</span></span>

<span data-ttu-id="277d2-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-289">11 digits:</span></span>
  
-  <span data-ttu-id="277d2-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit : 1,2 pour le 19 siècle ; 3, 4 pour le vingtième siècle ; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="277d2-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="277d2-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="277d2-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="277d2-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="277d2-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="277d2-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-294">Checksum</span></span>

<span data-ttu-id="277d2-295">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-296">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-296">Definition</span></span>

<span data-ttu-id="277d2-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-302">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-302">Keywords</span></span>

#### <a name="keywords_estonia_eu_tax_file_number"></a><span data-ttu-id="277d2-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-304">tax number</span></span>
  
<span data-ttu-id="277d2-305">codes</span><span class="sxs-lookup"><span data-stu-id="277d2-305">tax</span></span>
  
<span data-ttu-id="277d2-306">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-306">tax id</span></span>
  
<span data-ttu-id="277d2-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-307">personal code</span></span>
  
<span data-ttu-id="277d2-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="277d2-308">maksunumber</span></span>
  
<span data-ttu-id="277d2-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="277d2-309">maksu id</span></span>
  
<span data-ttu-id="277d2-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="277d2-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="277d2-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="277d2-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="277d2-312">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-312">Format</span></span>

<span data-ttu-id="277d2-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="277d2-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-314">Pattern</span></span>

<span data-ttu-id="277d2-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins :</span><span class="sxs-lookup"><span data-stu-id="277d2-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="277d2-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-316">Six digits</span></span>
    
- <span data-ttu-id="277d2-317">L’une des options suivantes : un signe plus, un signe moins ou la lettre « A » (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et « A » désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="277d2-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="277d2-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-318">Three digits</span></span>
    
- <span data-ttu-id="277d2-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="277d2-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-320">Checksum</span></span>

<span data-ttu-id="277d2-321">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-322">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-322">Definition</span></span>

<span data-ttu-id="277d2-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-328">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-328">Keywords</span></span>

#### <a name="keywords_finland_eu_tax_file_number"></a><span data-ttu-id="277d2-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-330">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="277d2-330">identification number</span></span>
  
<span data-ttu-id="277d2-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-331">personal id</span></span>
  
<span data-ttu-id="277d2-332">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="277d2-332">identity number</span></span>
  
<span data-ttu-id="277d2-333">Numéro d’identification national finnois</span><span class="sxs-lookup"><span data-stu-id="277d2-333">finnish national id number</span></span>
  
<span data-ttu-id="277d2-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-334">personalidnumber#</span></span>
  
<span data-ttu-id="277d2-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="277d2-335">national identification number</span></span>
  
<span data-ttu-id="277d2-336">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="277d2-336">id number</span></span>
  
<span data-ttu-id="277d2-337">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="277d2-337">national id no.</span></span>
  
<span data-ttu-id="277d2-338">Numéro d’identification national</span><span class="sxs-lookup"><span data-stu-id="277d2-338">national id number</span></span>
  
<span data-ttu-id="277d2-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="277d2-339">id no</span></span>
  
<span data-ttu-id="277d2-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="277d2-340">tunnistenumero</span></span>
  
<span data-ttu-id="277d2-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="277d2-341">henkilötunnus</span></span>
  
<span data-ttu-id="277d2-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="277d2-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="277d2-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="277d2-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="277d2-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="277d2-344">identiteetti numero</span></span>
  
<span data-ttu-id="277d2-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="277d2-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="277d2-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="277d2-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="277d2-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="277d2-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="277d2-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="277d2-348">tunnusnumero</span></span>
  
<span data-ttu-id="277d2-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="277d2-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="277d2-350">France</span><span class="sxs-lookup"><span data-stu-id="277d2-350">France</span></span>

### <a name="format"></a><span data-ttu-id="277d2-351">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-351">Format</span></span>

<span data-ttu-id="277d2-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="277d2-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-353">Pattern</span></span>

<span data-ttu-id="277d2-354">13 chiffres pour les personnes :</span><span class="sxs-lookup"><span data-stu-id="277d2-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="277d2-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="277d2-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="277d2-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-356">12 digits</span></span>
    
<span data-ttu-id="277d2-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="277d2-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-358">Checksum</span></span>

<span data-ttu-id="277d2-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-360">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-360">Definition</span></span>

<span data-ttu-id="277d2-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-366">Keywords</span></span>

#### <a name="keywords_france_eu_tax_file_number"></a><span data-ttu-id="277d2-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-368">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-368">tax identification number</span></span>
  
<span data-ttu-id="277d2-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-369">tax number</span></span>
  
<span data-ttu-id="277d2-370">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-370">tax id</span></span>
  
<span data-ttu-id="277d2-371">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="277d2-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="277d2-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="277d2-373">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-373">Format</span></span>

<span data-ttu-id="277d2-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-375">Pattern</span></span>

<span data-ttu-id="277d2-376">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-376">11 digits :</span></span>
  
-  <span data-ttu-id="277d2-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-377">Ten digits</span></span> 
    
- <span data-ttu-id="277d2-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-379">Checksum</span></span>

<span data-ttu-id="277d2-380">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-381">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-381">Definition</span></span>

<span data-ttu-id="277d2-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-387">Keywords</span></span>

#### <a name="keywords_germany_eu_tax_file_number"></a><span data-ttu-id="277d2-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-389">tax number</span></span>
  
<span data-ttu-id="277d2-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-390">tax no.</span></span>
  
<span data-ttu-id="277d2-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-391">taxno#</span></span>
  
<span data-ttu-id="277d2-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-392">taxnumber#</span></span>
  
<span data-ttu-id="277d2-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-393">taxnumber</span></span>
  
<span data-ttu-id="277d2-394">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-394">tax id</span></span>
  
<span data-ttu-id="277d2-395">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-395">taxid#</span></span>
  
<span data-ttu-id="277d2-396">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-396">tax identification number</span></span>
  
<span data-ttu-id="277d2-397">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-397">tax identification no.</span></span>
  
<span data-ttu-id="277d2-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="277d2-398">steuernummer</span></span>
  
<span data-ttu-id="277d2-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="277d2-399">steuer id</span></span>
  
<span data-ttu-id="277d2-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="277d2-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="277d2-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="277d2-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="277d2-402">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-402">Format</span></span>

<span data-ttu-id="277d2-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-404">Pattern</span></span>

<span data-ttu-id="277d2-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-406">Checksum</span></span>

<span data-ttu-id="277d2-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-408">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-408">Definition</span></span>

<span data-ttu-id="277d2-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-410">L’expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-412">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-412">Keywords</span></span>

#### <a name="keywords_greece_eu_tax_file_number"></a><span data-ttu-id="277d2-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-414">financement</span><span class="sxs-lookup"><span data-stu-id="277d2-414">afm</span></span>
  
<span data-ttu-id="277d2-415">Etain</span><span class="sxs-lookup"><span data-stu-id="277d2-415">tin</span></span>
  
<span data-ttu-id="277d2-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-416">tax id no.</span></span>
  
<span data-ttu-id="277d2-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-417">tax id no</span></span>
  
<span data-ttu-id="277d2-418">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-418">tax identification number</span></span>
  
<span data-ttu-id="277d2-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="277d2-419">tax registry number</span></span>
  
<span data-ttu-id="277d2-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-420">tax registry no.</span></span>
  
<span data-ttu-id="277d2-421">financement #</span><span class="sxs-lookup"><span data-stu-id="277d2-421">afm#</span></span>
  
<span data-ttu-id="277d2-422">Etain #</span><span class="sxs-lookup"><span data-stu-id="277d2-422">tin#</span></span>
  
<span data-ttu-id="277d2-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="277d2-423">taxidno#</span></span>
  
<span data-ttu-id="277d2-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="277d2-424">taxregistryno#</span></span>
  
<span data-ttu-id="277d2-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="277d2-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="277d2-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="277d2-426">aφμ</span></span>
  
<span data-ttu-id="277d2-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="277d2-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="277d2-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="277d2-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="277d2-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="277d2-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="277d2-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="277d2-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="277d2-431">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-431">Format</span></span>

<span data-ttu-id="277d2-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-433">Pattern</span></span>

<span data-ttu-id="277d2-434">Dix chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-434">Ten digits:</span></span>
  
-  <span data-ttu-id="277d2-435">Un chiffre qui doit être « 8 »</span><span class="sxs-lookup"><span data-stu-id="277d2-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="277d2-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="277d2-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="277d2-437">Trois chiffres correspondant au nombre généré par l’opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="277d2-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="277d2-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-439">Checksum</span></span>

<span data-ttu-id="277d2-440">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-441">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-441">Definition</span></span>

<span data-ttu-id="277d2-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-447">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-447">Keywords</span></span>

#### <a name="keywords_hungary_eu_tax_file_number"></a><span data-ttu-id="277d2-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-449">Numéro d’identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="277d2-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="277d2-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="277d2-450">hungarian tin</span></span>
  
<span data-ttu-id="277d2-451">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-451">tax id number</span></span>
  
<span data-ttu-id="277d2-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="277d2-452">vat number</span></span>
  
<span data-ttu-id="277d2-453">Numéro de l’autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-453">tax authority no</span></span>
  
<span data-ttu-id="277d2-454">Numéro d’identité fiscale de l’ID taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-454">tax id tax identity number</span></span>
  
<span data-ttu-id="277d2-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-455">taxidnumber#</span></span>
  
<span data-ttu-id="277d2-456">Etain #</span><span class="sxs-lookup"><span data-stu-id="277d2-456">tin#</span></span>
  
<span data-ttu-id="277d2-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="277d2-457">hungatiantin#</span></span>
  
<span data-ttu-id="277d2-458">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-458">tax identification no</span></span>
  
<span data-ttu-id="277d2-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="277d2-459">taxidno#</span></span>
  
<span data-ttu-id="277d2-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="277d2-460">adóazonosító szám</span></span>
  
<span data-ttu-id="277d2-461">adószám</span><span class="sxs-lookup"><span data-stu-id="277d2-461">adószám</span></span>
  
<span data-ttu-id="277d2-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="277d2-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="277d2-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="277d2-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="277d2-464">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-464">Format</span></span>

<span data-ttu-id="277d2-465">Sept chiffres suivis d’une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-466">Pattern</span></span>

<span data-ttu-id="277d2-467">Sept chiffres suivis d’une lettre :</span><span class="sxs-lookup"><span data-stu-id="277d2-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="277d2-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-468">Seven digits</span></span> 
    
- <span data-ttu-id="277d2-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-470">Checksum</span></span>

<span data-ttu-id="277d2-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-472">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-472">Definition</span></span>

<span data-ttu-id="277d2-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-478">Keywords</span></span>

#### <a name="keywords_ireland_eu_tax_file_number"></a><span data-ttu-id="277d2-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="277d2-480">public service no</span></span>
  
<span data-ttu-id="277d2-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-481">personal public service no</span></span>
  
<span data-ttu-id="277d2-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="277d2-482">pps no</span></span>
  
<span data-ttu-id="277d2-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-483">personal service no</span></span>
  
<span data-ttu-id="277d2-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="277d2-484">pps service no</span></span>
  
<span data-ttu-id="277d2-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="277d2-485">ppsno#</span></span>
  
<span data-ttu-id="277d2-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="277d2-486">irish pps no</span></span>
  
<span data-ttu-id="277d2-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="277d2-487">publicserviceno#</span></span>
  
<span data-ttu-id="277d2-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="277d2-488">personal public service number</span></span>
  
<span data-ttu-id="277d2-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="277d2-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="277d2-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="277d2-490">pps uimh</span></span>
  
<span data-ttu-id="277d2-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="277d2-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="277d2-492">Italie</span><span class="sxs-lookup"><span data-stu-id="277d2-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="277d2-493">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-493">Format</span></span>

<span data-ttu-id="277d2-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-495">Pattern</span></span>

<span data-ttu-id="277d2-496">16 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="277d2-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="277d2-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="277d2-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="277d2-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="277d2-499">Deux chiffres correspondant aux derniers chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="277d2-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="277d2-500">Un chiffre correspondant au mois de naissance : les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="277d2-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="277d2-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="277d2-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="277d2-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="277d2-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="277d2-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-504">Checksum</span></span>

<span data-ttu-id="277d2-505">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-506">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-506">Definition</span></span>

<span data-ttu-id="277d2-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-512">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-512">Keywords</span></span>

#### <a name="keywords_italy_eu_tax_file_number"></a><span data-ttu-id="277d2-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-514">tax number</span></span>
  
<span data-ttu-id="277d2-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-515">tax no.</span></span>
  
<span data-ttu-id="277d2-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-516">taxno#</span></span>
  
<span data-ttu-id="277d2-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-517">taxnumber#</span></span>
  
<span data-ttu-id="277d2-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-518">taxnumber</span></span>
  
<span data-ttu-id="277d2-519">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-519">tax id</span></span>
  
<span data-ttu-id="277d2-520">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-520">taxid#</span></span>
  
<span data-ttu-id="277d2-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-521">fiscal code</span></span>
  
<span data-ttu-id="277d2-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="277d2-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="277d2-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="277d2-524">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-524">Format</span></span>

<span data-ttu-id="277d2-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-526">Pattern</span></span>

<span data-ttu-id="277d2-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="277d2-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="277d2-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="277d2-529">Un chiffre correspondant au siècle de naissance où « 0 » correspond à 19 siècle, « 1 » correspond au vingtième siècle et « 2 » au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="277d2-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="277d2-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-531">Checksum</span></span>

<span data-ttu-id="277d2-532">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-533">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-533">Definition</span></span>

<span data-ttu-id="277d2-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-539">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-539">Keywords</span></span>

#### <a name="keywords_latvia_eu_tax_file_number"></a><span data-ttu-id="277d2-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-541">tax number</span></span>
  
<span data-ttu-id="277d2-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-542">tax no.</span></span>
  
<span data-ttu-id="277d2-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-543">taxno#</span></span>
  
<span data-ttu-id="277d2-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-544">taxnumber#</span></span>
  
<span data-ttu-id="277d2-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-545">taxnumber</span></span>
  
<span data-ttu-id="277d2-546">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-546">tax id</span></span>
  
<span data-ttu-id="277d2-547">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-547">taxid#</span></span>
  
<span data-ttu-id="277d2-548">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-548">tax identification number</span></span>
  
<span data-ttu-id="277d2-549">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-549">tax identification no.</span></span>
  
<span data-ttu-id="277d2-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="277d2-550">nodokļa numurs</span></span>
  
<span data-ttu-id="277d2-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="277d2-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="277d2-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="277d2-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="277d2-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="277d2-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="277d2-554">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-554">Format</span></span>

<span data-ttu-id="277d2-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-556">Pattern</span></span>

<span data-ttu-id="277d2-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-558">Checksum</span></span>

<span data-ttu-id="277d2-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-560">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-560">Definition</span></span>

<span data-ttu-id="277d2-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-566">Keywords</span></span>

#### <a name="keywords_lithuania_eu_tax_file_number"></a><span data-ttu-id="277d2-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-568">tax number</span></span>
  
<span data-ttu-id="277d2-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-569">tax no.</span></span>
  
<span data-ttu-id="277d2-570">n ° taxe #</span><span class="sxs-lookup"><span data-stu-id="277d2-570">tax no#</span></span>
  
<span data-ttu-id="277d2-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-571">taxnumber#</span></span>
  
<span data-ttu-id="277d2-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-572">taxnumber</span></span>
  
<span data-ttu-id="277d2-573">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-573">tax id</span></span>
  
<span data-ttu-id="277d2-574">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-574">taxid#</span></span>
  
<span data-ttu-id="277d2-575">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-575">tax identification number</span></span>
  
<span data-ttu-id="277d2-576">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-576">tax identification no.</span></span>
  
<span data-ttu-id="277d2-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="277d2-577">mokesčių id</span></span>
  
<span data-ttu-id="277d2-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-578">mokesčių numeris</span></span>
  
<span data-ttu-id="277d2-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="277d2-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="277d2-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="277d2-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="277d2-581">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-581">Format</span></span>

<span data-ttu-id="277d2-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-583">Pattern</span></span>

<span data-ttu-id="277d2-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="277d2-584">13 digits:</span></span>
  
-  <span data-ttu-id="277d2-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-585">11 digits</span></span> 
    
- <span data-ttu-id="277d2-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-587">Checksum</span></span>

<span data-ttu-id="277d2-588">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-589">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-589">Definition</span></span>

<span data-ttu-id="277d2-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-595">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-595">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_tax_file_number"></a><span data-ttu-id="277d2-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-597">tax number</span></span>
  
<span data-ttu-id="277d2-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-598">tax no.</span></span>
  
<span data-ttu-id="277d2-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-599">taxno#</span></span>
  
<span data-ttu-id="277d2-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-600">taxnumber#</span></span>
  
<span data-ttu-id="277d2-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-601">taxnumber</span></span>
  
<span data-ttu-id="277d2-602">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-602">tax id</span></span>
  
<span data-ttu-id="277d2-603">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-603">taxid#</span></span>
  
<span data-ttu-id="277d2-604">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-604">tax identification number</span></span>
  
<span data-ttu-id="277d2-605">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-605">tax identification no.</span></span>
  
<span data-ttu-id="277d2-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="277d2-606">steuernummer</span></span>
  
<span data-ttu-id="277d2-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="277d2-607">steuer id</span></span>
  
<span data-ttu-id="277d2-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="277d2-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="277d2-609">Malte</span><span class="sxs-lookup"><span data-stu-id="277d2-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="277d2-610">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-610">Format</span></span>

<span data-ttu-id="277d2-611">Pour les ressortissants maltais : 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="277d2-612">Ressortissants non maltaises et entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-613">Pattern</span></span>

<span data-ttu-id="277d2-614">Ressortissants maltaises : 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="277d2-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="277d2-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-615">Seven digits</span></span> 
    
- <span data-ttu-id="277d2-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="277d2-617">Ressortissants non maltaises et entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="277d2-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="277d2-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-619">Checksum</span></span>

<span data-ttu-id="277d2-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-621">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-621">Definition</span></span>

<span data-ttu-id="277d2-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-627">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-627">Keywords</span></span>

#### <a name="keywords_malta_eu_tax_file_number"></a><span data-ttu-id="277d2-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-629">tax number</span></span>
  
<span data-ttu-id="277d2-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-630">tax no.</span></span>
  
<span data-ttu-id="277d2-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-631">taxno#</span></span>
  
<span data-ttu-id="277d2-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-632">taxnumber#</span></span>
  
<span data-ttu-id="277d2-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-633">taxnumber</span></span>
  
<span data-ttu-id="277d2-634">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-634">tax id</span></span>
  
<span data-ttu-id="277d2-635">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-635">taxid#</span></span>
  
<span data-ttu-id="277d2-636">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-636">tax identification number</span></span>
  
<span data-ttu-id="277d2-637">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-637">tax identification no.</span></span>
  
<span data-ttu-id="277d2-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="277d2-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="277d2-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="277d2-639">id tat-taxxa</span></span>
  
<span data-ttu-id="277d2-640">numru ta’IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="277d2-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="277d2-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="277d2-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="277d2-642">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-642">Format</span></span>

<span data-ttu-id="277d2-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-644">Pattern</span></span>

<span data-ttu-id="277d2-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="277d2-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-646">Checksum</span></span>

<span data-ttu-id="277d2-647">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-648">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-648">Definition</span></span>

<span data-ttu-id="277d2-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-654">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-654">Keywords</span></span>

#### <a name="keywords_netherlands_eu_tax_file_number"></a><span data-ttu-id="277d2-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-656">Numéro d’identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="277d2-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="277d2-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="277d2-657">netherlands tax identification</span></span>
  
<span data-ttu-id="277d2-658">Numéro d’identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="277d2-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="277d2-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="277d2-659">netherland's tax identification</span></span>
  
<span data-ttu-id="277d2-660">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-660">tax identification number</span></span>
  
<span data-ttu-id="277d2-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="277d2-661">dutch tax id</span></span>
  
<span data-ttu-id="277d2-662">Numéro d’identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="277d2-662">dutch tax identification number</span></span>
  
<span data-ttu-id="277d2-663">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-663">tax id</span></span>
  
<span data-ttu-id="277d2-664">ID de taxe #</span><span class="sxs-lookup"><span data-stu-id="277d2-664">tax id#</span></span>
  
<span data-ttu-id="277d2-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-665">tax number</span></span>
  
<span data-ttu-id="277d2-666">n ° taxe #</span><span class="sxs-lookup"><span data-stu-id="277d2-666">tax no#</span></span>
  
<span data-ttu-id="277d2-667">codes #</span><span class="sxs-lookup"><span data-stu-id="277d2-667">tax#</span></span>
  
<span data-ttu-id="277d2-668">Etain</span><span class="sxs-lookup"><span data-stu-id="277d2-668">tin</span></span>
  
<span data-ttu-id="277d2-669">Etain #</span><span class="sxs-lookup"><span data-stu-id="277d2-669">tin#</span></span>
  
<span data-ttu-id="277d2-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="277d2-670">netherlands tin</span></span>
  
<span data-ttu-id="277d2-671">Netherland d’étain</span><span class="sxs-lookup"><span data-stu-id="277d2-671">netherland's tin</span></span>
  
<span data-ttu-id="277d2-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="277d2-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="277d2-673">identificatienummer van à l’avant-dernière</span><span class="sxs-lookup"><span data-stu-id="277d2-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="277d2-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="277d2-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="277d2-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="277d2-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="277d2-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="277d2-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="277d2-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="277d2-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="277d2-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="277d2-678">btw nummer</span></span>
  
<span data-ttu-id="277d2-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="277d2-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="277d2-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="277d2-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="277d2-681">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-681">Format</span></span>

<span data-ttu-id="277d2-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-683">Pattern</span></span>

<span data-ttu-id="277d2-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-685">Checksum</span></span>

<span data-ttu-id="277d2-686">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-687">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-687">Definition</span></span>

<span data-ttu-id="277d2-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-693">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-693">Keywords</span></span>

#### <a name="keywords_poland_eu_tax_file_number"></a><span data-ttu-id="277d2-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-695">tax number</span></span>
  
<span data-ttu-id="277d2-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-696">tax no.</span></span>
  
<span data-ttu-id="277d2-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-697">taxno#</span></span>
  
<span data-ttu-id="277d2-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-698">taxnumber#</span></span>
  
<span data-ttu-id="277d2-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-699">taxnumber</span></span>
  
<span data-ttu-id="277d2-700">pince</span><span class="sxs-lookup"><span data-stu-id="277d2-700">nip</span></span>
  
<span data-ttu-id="277d2-701">pince #</span><span class="sxs-lookup"><span data-stu-id="277d2-701">nip#</span></span>
  
<span data-ttu-id="277d2-702">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-702">tax id</span></span>
  
<span data-ttu-id="277d2-703">ID de taxe #</span><span class="sxs-lookup"><span data-stu-id="277d2-703">tax id#</span></span>
  
<span data-ttu-id="277d2-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="277d2-704">nip id</span></span>
  
<span data-ttu-id="277d2-705">ID du NIP #</span><span class="sxs-lookup"><span data-stu-id="277d2-705">nip id#</span></span>
  
<span data-ttu-id="277d2-706">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-706">tax identification number</span></span>
  
<span data-ttu-id="277d2-707">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-707">tax identification no.</span></span>
  
<span data-ttu-id="277d2-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="277d2-708">vat number</span></span>
  
<span data-ttu-id="277d2-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="277d2-709">vat no.</span></span>
  
<span data-ttu-id="277d2-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="277d2-710">vatno#</span></span>
  
<span data-ttu-id="277d2-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="277d2-711">vat id</span></span>
  
<span data-ttu-id="277d2-712">Numéro de TVA #</span><span class="sxs-lookup"><span data-stu-id="277d2-712">vat id#</span></span>
  
<span data-ttu-id="277d2-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="277d2-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="277d2-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="277d2-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="277d2-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="277d2-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="277d2-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="277d2-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="277d2-717">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-717">Format</span></span>

<span data-ttu-id="277d2-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-719">Pattern</span></span>

<span data-ttu-id="277d2-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-721">Checksum</span></span>

<span data-ttu-id="277d2-722">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-723">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-723">Definition</span></span>

<span data-ttu-id="277d2-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-729">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-729">Keywords</span></span>

#### <a name="keywords_portugal_eu_tax_file_number"></a><span data-ttu-id="277d2-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-731">tax number</span></span>
  
<span data-ttu-id="277d2-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-732">tax no.</span></span>
  
<span data-ttu-id="277d2-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-733">taxno#</span></span>
  
<span data-ttu-id="277d2-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="277d2-734">taxnumber#</span></span>
  
<span data-ttu-id="277d2-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="277d2-735">taxnumber</span></span>
  
<span data-ttu-id="277d2-736">nPour</span><span class="sxs-lookup"><span data-stu-id="277d2-736">nif</span></span>
  
<span data-ttu-id="277d2-737">nPour #</span><span class="sxs-lookup"><span data-stu-id="277d2-737">nif#</span></span>
  
<span data-ttu-id="277d2-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="277d2-738">numero fiscal</span></span>
  
<span data-ttu-id="277d2-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="277d2-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="277d2-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="277d2-741">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-741">Format</span></span>

<span data-ttu-id="277d2-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-743">Pattern</span></span>

<span data-ttu-id="277d2-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-745">Checksum</span></span>

<span data-ttu-id="277d2-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-747">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-747">Definition</span></span>

<span data-ttu-id="277d2-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-749">L’expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-751">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-751">Keywords</span></span>

#### <a name="keywords_romania_eu_tax_file_number"></a><span data-ttu-id="277d2-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-753">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-753">tax id</span></span>
  
<span data-ttu-id="277d2-754">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-754">tax id number</span></span>
  
<span data-ttu-id="277d2-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-755">tax file no</span></span>
  
<span data-ttu-id="277d2-756">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-756">tax file number</span></span>
  
<span data-ttu-id="277d2-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-757">tax no</span></span>
  
<span data-ttu-id="277d2-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-758">tax number</span></span>
  
<span data-ttu-id="277d2-759">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-759">taxid#</span></span>
  
<span data-ttu-id="277d2-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-760">taxno#</span></span>
  
<span data-ttu-id="277d2-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="277d2-761">id-ul taxei</span></span>
  
<span data-ttu-id="277d2-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="277d2-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="277d2-763">Slovaquie</span><span class="sxs-lookup"><span data-stu-id="277d2-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="277d2-764">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-764">Format</span></span>

<span data-ttu-id="277d2-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-766">Pattern</span></span>

<span data-ttu-id="277d2-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-768">Checksum</span></span>

<span data-ttu-id="277d2-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="277d2-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-770">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-770">Definition</span></span>

<span data-ttu-id="277d2-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-772">L’expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-774">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-774">Keywords</span></span>

#### <a name="keywords_slovakia_eu_tax_file_number"></a><span data-ttu-id="277d2-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-776">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-776">tax id</span></span>
  
<span data-ttu-id="277d2-777">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-777">tax id number</span></span>
  
<span data-ttu-id="277d2-778">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="277d2-778">tin id</span></span>
  
<span data-ttu-id="277d2-779">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="277d2-779">tin no</span></span>
  
<span data-ttu-id="277d2-780">ID d’étain slovaque</span><span class="sxs-lookup"><span data-stu-id="277d2-780">slovakian tin id</span></span>
  
<span data-ttu-id="277d2-781">Etain</span><span class="sxs-lookup"><span data-stu-id="277d2-781">tin</span></span>
  
<span data-ttu-id="277d2-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-782">tax file no</span></span>
  
<span data-ttu-id="277d2-783">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-783">tax file number</span></span>
  
<span data-ttu-id="277d2-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-784">tax no</span></span>
  
<span data-ttu-id="277d2-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-785">tax number</span></span>
  
<span data-ttu-id="277d2-786">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-786">taxid#</span></span>
  
<span data-ttu-id="277d2-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-787">taxno#</span></span>
  
<span data-ttu-id="277d2-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="277d2-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="277d2-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="277d2-789">daňové číslo</span></span>
  
<span data-ttu-id="277d2-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="277d2-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="277d2-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="277d2-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="277d2-792">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-792">Format</span></span>

<span data-ttu-id="277d2-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-794">Pattern</span></span>

<span data-ttu-id="277d2-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-796">Checksum</span></span>

<span data-ttu-id="277d2-797">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-798">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-798">Definition</span></span>

<span data-ttu-id="277d2-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-804">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-804">Keywords</span></span>

#### <a name="keywords_slovenia_eu_tax_file_number"></a><span data-ttu-id="277d2-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-806">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-806">tax id</span></span>
  
<span data-ttu-id="277d2-807">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-807">tax id number</span></span>
  
<span data-ttu-id="277d2-808">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="277d2-808">tin id</span></span>
  
<span data-ttu-id="277d2-809">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="277d2-809">tin no</span></span>
  
<span data-ttu-id="277d2-810">ID d’étain slovène</span><span class="sxs-lookup"><span data-stu-id="277d2-810">slovenian tin id</span></span>
  
<span data-ttu-id="277d2-811">Etain</span><span class="sxs-lookup"><span data-stu-id="277d2-811">tin</span></span>
  
<span data-ttu-id="277d2-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-812">tax file no</span></span>
  
<span data-ttu-id="277d2-813">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-813">tax file number</span></span>
  
<span data-ttu-id="277d2-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-814">tax no</span></span>
  
<span data-ttu-id="277d2-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-815">tax number</span></span>
  
<span data-ttu-id="277d2-816">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-816">taxid#</span></span>
  
<span data-ttu-id="277d2-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-817">taxno#</span></span>
  
<span data-ttu-id="277d2-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="277d2-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="277d2-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="277d2-819">davčna številka</span></span>
  
<span data-ttu-id="277d2-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="277d2-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="277d2-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="277d2-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="277d2-822">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-822">Format</span></span>

<span data-ttu-id="277d2-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-824">Pattern</span></span>

<span data-ttu-id="277d2-825">Personnes physiques espagnoles avec une carte d’identité nationale d’Espagne :</span><span class="sxs-lookup"><span data-stu-id="277d2-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="277d2-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-826">Eight digits</span></span> 
    
- <span data-ttu-id="277d2-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="277d2-828">Spaniards non résident sans carte d’identité nationale d’Espagne</span><span class="sxs-lookup"><span data-stu-id="277d2-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="277d2-829">Une lettre majuscule « L » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="277d2-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-830">Seven digits</span></span>
    
- <span data-ttu-id="277d2-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="277d2-832">Spaniards résident de moins de 14 ans sans carte d’identité nationale (Espagne) :</span><span class="sxs-lookup"><span data-stu-id="277d2-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="277d2-833">Une lettre majuscule « K » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="277d2-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-834">Seven digits</span></span> 
    
- <span data-ttu-id="277d2-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="277d2-836">Foreigners avec le numéro d’identification d’un étranger</span><span class="sxs-lookup"><span data-stu-id="277d2-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="277d2-837">Une lettre majuscule qui est « X », « Y » ou « Z » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="277d2-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-838">Seven digits</span></span>
    
- <span data-ttu-id="277d2-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="277d2-840">Foreigners sans numéro d’identification étranger</span><span class="sxs-lookup"><span data-stu-id="277d2-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="277d2-841">Une lettre majuscule qui est « M » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="277d2-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="277d2-842">Seven digits</span></span>
    
- <span data-ttu-id="277d2-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="277d2-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="277d2-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-844">Checksum</span></span>

<span data-ttu-id="277d2-845">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-846">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-846">Definition</span></span>

<span data-ttu-id="277d2-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-852">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-852">Keywords</span></span>

#### <a name="keywords_spain_eu_tax_file_number"></a><span data-ttu-id="277d2-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-854">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-854">tax id</span></span>
  
<span data-ttu-id="277d2-855">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-855">tax id number</span></span>
  
<span data-ttu-id="277d2-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="277d2-856">cif id</span></span>
  
<span data-ttu-id="277d2-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="277d2-857">cif no</span></span>
  
<span data-ttu-id="277d2-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="277d2-858">spanish cif id</span></span>
  
<span data-ttu-id="277d2-859">importation</span><span class="sxs-lookup"><span data-stu-id="277d2-859">cif</span></span>
  
<span data-ttu-id="277d2-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-860">tax file no</span></span>
  
<span data-ttu-id="277d2-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="277d2-861">spanish cif number</span></span>
  
<span data-ttu-id="277d2-862">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-862">tax file number</span></span>
  
<span data-ttu-id="277d2-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="277d2-863">spanish cif no</span></span>
  
<span data-ttu-id="277d2-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-864">tax no</span></span>
  
<span data-ttu-id="277d2-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-865">tax number</span></span>
  
<span data-ttu-id="277d2-866">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-866">taxid#</span></span>
  
<span data-ttu-id="277d2-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="277d2-867">taxno#</span></span>
  
<span data-ttu-id="277d2-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="277d2-868">cifid#</span></span>
  
<span data-ttu-id="277d2-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="277d2-869">spanishcifid#</span></span>
  
<span data-ttu-id="277d2-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="277d2-870">spanishcifno#</span></span>
  
<span data-ttu-id="277d2-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="277d2-871">número de contribuyente</span></span>
  
<span data-ttu-id="277d2-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="277d2-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="277d2-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="277d2-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="277d2-874">cif número</span></span>
  
<span data-ttu-id="277d2-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="277d2-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="277d2-876">Suède</span><span class="sxs-lookup"><span data-stu-id="277d2-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="277d2-877">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-877">Format</span></span>

<span data-ttu-id="277d2-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="277d2-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-879">Pattern</span></span>

<span data-ttu-id="277d2-880">Dix chiffres et un symbole :</span><span class="sxs-lookup"><span data-stu-id="277d2-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="277d2-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="277d2-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="277d2-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="277d2-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="277d2-883">Trois chiffres qui permettent de définir le numéro d’identification unique :</span><span class="sxs-lookup"><span data-stu-id="277d2-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="277d2-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l’étranger.</span><span class="sxs-lookup"><span data-stu-id="277d2-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="277d2-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="277d2-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="277d2-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="277d2-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-887">Checksum</span></span>

<span data-ttu-id="277d2-888">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-889">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-889">Definition</span></span>

<span data-ttu-id="277d2-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="277d2-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-895">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-895">Keywords</span></span>

#### <a name="keywords_sweden_eu_tax_file_number"></a><span data-ttu-id="277d2-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-897">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-897">tax id</span></span>
  
<span data-ttu-id="277d2-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-898">tax id no.</span></span>
  
<span data-ttu-id="277d2-899">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-899">tax id number</span></span>
  
<span data-ttu-id="277d2-900">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-900">tax identification</span></span>
  
<span data-ttu-id="277d2-901">identification fiscale #</span><span class="sxs-lookup"><span data-stu-id="277d2-901">tax identification#</span></span>
  
<span data-ttu-id="277d2-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-902">tax no.</span></span>
  
<span data-ttu-id="277d2-903">codes #</span><span class="sxs-lookup"><span data-stu-id="277d2-903">tax#</span></span>
  
<span data-ttu-id="277d2-904">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-904">taxid#</span></span>
  
<span data-ttu-id="277d2-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-905">tax file</span></span>
  
<span data-ttu-id="277d2-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-906">tax file no.</span></span>
  
<span data-ttu-id="277d2-907">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="277d2-907">personal id number</span></span>
  
<span data-ttu-id="277d2-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="277d2-908">skatt id nummer</span></span>
  
<span data-ttu-id="277d2-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="277d2-909">skatt identifikation</span></span>
  
<span data-ttu-id="277d2-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="277d2-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="277d2-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="277d2-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="277d2-912">Format</span><span class="sxs-lookup"><span data-stu-id="277d2-912">Format</span></span>

<span data-ttu-id="277d2-913">Référence de contribuable unique (UTR) : 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="277d2-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="277d2-914">Numéro d’assurance nationale (NINO) : pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="277d2-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="277d2-915">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="277d2-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="277d2-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="277d2-916">Pattern</span></span>

<span data-ttu-id="277d2-917">Référence de contribuable unique (UTR) : 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="277d2-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="277d2-918">Numéro d’assurance nationale (NINO) : pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="277d2-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="277d2-919">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="277d2-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="277d2-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="277d2-920">Checksum</span></span>

<span data-ttu-id="277d2-921">Oui</span><span class="sxs-lookup"><span data-stu-id="277d2-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="277d2-922">Définition</span><span class="sxs-lookup"><span data-stu-id="277d2-922">Definition</span></span>

<span data-ttu-id="277d2-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="277d2-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="277d2-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="277d2-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="277d2-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="277d2-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="277d2-926">Mots clés</span><span class="sxs-lookup"><span data-stu-id="277d2-926">Keywords</span></span>

#### <a name="keywords_uk_eu_tax_file_number"></a><span data-ttu-id="277d2-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="277d2-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="277d2-928">id fiscal</span><span class="sxs-lookup"><span data-stu-id="277d2-928">tax id</span></span>
  
<span data-ttu-id="277d2-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-929">tax id no.</span></span>
  
<span data-ttu-id="277d2-930">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-930">tax id number</span></span>
  
<span data-ttu-id="277d2-931">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="277d2-931">tax identification</span></span>
  
<span data-ttu-id="277d2-932">identification fiscale #</span><span class="sxs-lookup"><span data-stu-id="277d2-932">tax identification#</span></span>
  
<span data-ttu-id="277d2-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-933">tax no.</span></span>
  
<span data-ttu-id="277d2-934">codes #</span><span class="sxs-lookup"><span data-stu-id="277d2-934">tax#</span></span>
  
<span data-ttu-id="277d2-935">taxi #</span><span class="sxs-lookup"><span data-stu-id="277d2-935">taxid#</span></span>
  
<span data-ttu-id="277d2-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-936">tax file</span></span>
  
<span data-ttu-id="277d2-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="277d2-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="277d2-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="277d2-938">See also</span></span>

[<span data-ttu-id="277d2-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="277d2-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

